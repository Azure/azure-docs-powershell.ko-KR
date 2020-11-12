---
title: Azure PowerShell로 Azure 서비스 주체 만들기
description: Azure PowerShell을 사용하여 서비스 주체를 만들고 사용하는 방법을 알아봅니다.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 04/23/2019
ms.custom: devx-track-azurepowershell
ms.service: azure-powershell
ms.openlocfilehash: a8ce4669d52e587bd171cbeab2496e5386029615
ms.sourcegitcommit: 2036538797dd088728aee5ac5021472454d82eb2
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/06/2020
ms.locfileid: "93407972"
---
# <a name="create-an-azure-service-principal-with-azure-powershell"></a>Azure PowerShell을 사용하여 Azure 서비스 주체 만들기

Azure 서비스를 사용하도록 자동화된 도구에는 항상 제한된 권한이 있어야 합니다. Azure는 애플리케이션에서 모든 권한이 있는 사용자로 로그인하도록 하는 대신 서비스 주체를 제공합니다.

Azure 서비스 주체는 애플리케이션, 호스팅된 서비스 및 자동화된 도구에서 사용하여 Azure 리소스에 액세스하기 위해 만든 ID입니다. 이 액세스는 서비스 주체에 할당된 역할로 제한되므로 액세스할 수 있는 리소스와 해당 수준을 제어할 수 있습니다. 보안상의 이유로 사용자 ID를 통해 로그인할 수 있게 하는 대신, 항상 자동화된 도구에서 서비스 주체를 사용하는 것이 좋습니다.

이 문서에서는 Azure PowerShell을 사용하여 서비스 주체를 만들고, 정보를 가져오고, 다시 설정하는 단계를 보여 줍니다.

> [!WARNING]
> [New-AzADServicePrincipal](/powershell/module/Az.Resources/New-AzADServicePrincipal) 명령을 사용하여 서비스 주체를 만들면 보호해야 하는 자격 증명이 출력에 포함됩니다. 이러한 자격 증명을 코드에 포함하지 않도록 하거나 소스 제어에 자격 증명을 확인해야 합니다. 또는 자격 증명을 사용할 필요가 없도록 [관리 ID](/azure/active-directory/managed-identities-azure-resources/overview)를 사용하는 것이 좋습니다.
>
> 기본적으로 [New-AzADServicePrincipal](/powershell/module/Az.Resources/New-AzADServicePrincipal)은 구독 범위에서 서비스 주체에 [Contributor](/azure/role-based-access-control/built-in-roles#contributor) 역할을 할당합니다. 서비스 주체가 손상될 위험을 줄이려면 보다 구체적인 역할을 할당하고 범위를 리소스 또는 리소스 그룹으로 좁힙니다. 자세한 내용은 [역할 할당을 추가하는 단계](/azure/role-based-access-control/role-assignments-steps)를 참조하세요.

## <a name="create-a-service-principal"></a>서비스 주체 만들기

[New-AzADServicePrincipal](/powershell/module/Az.Resources/New-AzADServicePrincipal) cmdlet을 사용하여 서비스 주체 만들기 서비스 주체를 만드는 경우 사용하는 로그인 인증 유형을 선택합니다.

> [!NOTE]
>
> 계정에 서비스 주체를 만들 수 있는 권한이 없는 경우 `New-AzADServicePrincipal`에서 "권한이 부족하여 작업을 완료할 수 없습니다."라는 오류 메시지를 반환합니다. 서비스 주체를 만들려면 Azure Active Directory 관리자에게 문의하십시오.

서비스 주체에 사용할 수 있는 인증 유형에는 암호 기반 인증 및 인증서 기반 인증의 두 가지 유형이 있습니다.

### <a name="password-based-authentication"></a>암호 기반 인증

다른 인증 매개 변수가 없으면 임의로 만든 암호를 통한 암호 기반 인증이 사용됩니다. 암호 기반 인증을 원하는 경우 이 메서드를 사용하는 것이 좋습니다.

```azurepowershell-interactive
$sp = New-AzADServicePrincipal -DisplayName ServicePrincipalName
```

반환된 개체는 생성된 암호를 포함하는 `Secret` 멤버인 `SecureString`을 포함합니다. 서비스 주체로 인증하려면 이 값을 안전한 곳에서 저장하세요. 해당 값은 콘솔 출력에 표시되지 __않습니다__. 암호를 잊어버린 경우 [서비스 주체 자격 증명을 다시 설정](#reset-credentials)하세요.

다음 코드를 사용하면 비밀을 내보낼 수 있습니다.

```azurepowershell-interactive
$BSTR = [System.Runtime.InteropServices.Marshal]::SecureStringToBSTR($sp.Secret)
$UnsecureSecret = [System.Runtime.InteropServices.Marshal]::PtrToStringAuto($BSTR)
```

사용자 제공한 암호의 경우, `-PasswordCredential` 인수는 `Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential` 개체를 취합니다. 이러한 개체는 유효한 `StartDate`, `EndDate`가 있어야 하며 일반 텍스트 `Password`를 취합니다. 암호를 만드는 경우 [Azure Active Directory 암호 규칙 및 제한](/azure/active-directory/active-directory-passwords-policy)을 따라야 합니다. 취약한 암호를 사용하거나 암호를 다시 사용하지 마세요.

```azurepowershell-interactive
Import-Module Az.Resources # Imports the PSADPasswordCredential object
$credentials = New-Object Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential -Property @{ StartDate=Get-Date; EndDate=Get-Date -Year 2024; Password=<Choose a strong password>}
$sp = New-AzAdServicePrincipal -DisplayName ServicePrincipalName -PasswordCredential $credentials
```

`New-AzADServicePrincipal`에서 반환된 개체는 `Id` 및 `DisplayName` 멤버를 포함하며, 이들은 서비스 주체로 로그인에 사용할 수 있는 멤버입니다.

> [!IMPORTANT]
>
> 서비스 주체로 로그인하려면 서비스 주체가 생성된 테넌트 ID가 필요합니다. 서비스 주체를 만들 때 활성 테넌트를 얻으려면 서비스 주체 생성 __직후에__ 다음 명령을 실행하세요.
>
> ```azurepowershell-interactive
> (Get-AzContext).Tenant.Id
> ```

### <a name="certificate-based-authentication"></a>인증서 기반 인증

인증서 기반 인증을 사용하는 서비스 주체는 `-CertValue` 매개 변수를 사용하여 만들어집니다. 이 매개 변수는 공용 인증서의 base64로 인코딩된 ASCII 문자열을 취합니다. 이는 PEM 파일 또는 텍스트 인코딩 CRT 또는 CER로 표시됩니다. 공용 인증서의 이진 인코딩은 지원되지 않습니다. 이러한 명령은 사용할 수 있는 인증서가 이미 있다고 가정합니다.

```azurepowershell-interactive
$cert = <public certificate as base64-encoded string>
$sp = New-AzADServicePrincipal -DisplayName ServicePrincipalName -CertValue $cert
```

`PSADKeyCredential` 개체를 사용하는 `-KeyCredential` 매개 변수를 사용할 수도 있습니다. 이러한 객체는 유효한 `StartDate`, `EndDate`가 있어야 하며 `CertValue` 멤버가 공용 인증서의 base64 인코딩 ASCII 문자열로 설정되어야 합니다.

```azurepowershell-interactive
$cert = <public certificate as base64-encoded string>
$credentials = New-Object Microsoft.Azure.Commands.ActiveDirectory.PSADKeyCredential -Property @{ StartDate=Get-Date; EndDate=Get-Date -Year 2024; KeyId=New-Guid; CertValue=$cert}
$sp = New-AzADServicePrincipal -DisplayName ServicePrincipalName -KeyCredential $credentials
```

`New-AzADServicePrincipal`에서 반환된 개체는 `Id` 및 `DisplayName` 멤버를 포함하며, 이들은 서비스 주체로 로그인에 사용할 수 있는 멤버입니다. 서비스 주체로 로그인하는 클라이언트는 인증서의 프라이빗 키에 액세스해야 합니다.

> [!IMPORTANT]
>
> 서비스 주체로 로그인하려면 서비스 주체가 생성된 테넌트 ID가 필요합니다. 서비스 주체를 만들 때 활성 테넌트를 얻으려면 서비스 주체 생성 __직후에__ 다음 명령을 실행하세요.
>
> ```azurepowershell-interactive
> (Get-AzContext).Tenant.Id
> ```

## <a name="get-an-existing-service-principal"></a>기존 서비스 주체 가져오기

현재 활동 중인 테넌트의 서비스 주체 목록은 [Get-AzADServicePrincipal](/powershell/module/az.resources/get-azadserviceprincipal)을 사용하여 검색할 수 있습니다. 기본적으로 이 명령은 테넌트의 __모든__ 서비스 주체를 반환하므로 대규모 조직의 경우 결과를 반환하는 데 오랜 시간이 걸릴 수 있습니다. 대신 선택적 서버 측 필터링 인수 중 하나를 사용하는 것이 좋습니다.

* `-DisplayNameBeginsWith`은 제공된 값과 일치하는 _접두사_ 가 있는 서비스 주체를 요청합니다. 서비스 주체의 표시 이름은 만드는 중에 `-DisplayName`으로 설정된 값입니다.
* `-DisplayName`은 서비스 주체 이름과 _정확히 일치하는_ 것을 요청합니다.

## <a name="manage-service-principal-roles"></a>서비스 주체 역할 관리

Azure PowerShell은 역할 할당을 관리하는 다음과 같은 cmdlet이 있습니다.

* [Get-AzRoleAssignment](/powershell/module/az.resources/get-azroleassignment)
* [New-AzRoleAssignment](/powershell/module/az.resources/new-azroleassignment)
* [Remove-AzRoleAssignment](/powershell/module/az.resources/remove-azroleassignment)

서비스 주체의 기본 역할은 **참가자** 입니다. 이 역할에는 Azure 계정에서 읽고 쓸 수 있는 모든 권한이 있습니다. **Reader** (읽기 권한자) 역할은 읽기 전용 액세스 권한으로 더 제한적입니다.  RBAC(역할 기반 액세스 제어)와 역할에 대한 자세한 내용은 [RBAC: 기본 제공 역할](/azure/active-directory/role-based-access-built-in-roles)을 참조하세요.

다음 예제에서는 **Reader** 역할을 추가하고 **Contributor** (기여자) 역할을 제거합니다.

```azurepowershell-interactive
New-AzRoleAssignment -ApplicationId <service principal application ID> -RoleDefinitionName "Reader"
Remove-AzRoleAssignment -ApplicationId <service principal application ID> -RoleDefinitionName "Contributor"
```

> [!IMPORTANT]
> 역할 할당 cmdlet은 서비스 사용자 주체 ID를 사용하지 않습니다. 생성 시 생성되는 관련 애플리케이션 ID를 사용합니다. 서비스 주체에 대한 애플리케이션 ID를 가져오려면 `Get-AzADServicePrincipal`을 사용합니다.

> [!NOTE]
> 계정에 역할을 할당할 수 있는 권한이 없으면 계정에 "'Microsoft.Authorization/roleAssignments/write' 작업을 수행할 수 있는 권한이 없습니다."라는 오류 메시지가 표시됩니다. 역할을 관리하려면 Azure Active Directory 관리자에게 문의하십시오.

역할을 추가해도 이전에 할당된 권한은 _제한되지 않습니다_. 서비스 주체 권한을 제한할 때는 __Contributor__ 역할을 제거해야 합니다.

변경 내용은 할당된 역할을 나열하여 확인할 수 있습니다.

```azurepowershell-interactive
Get-AzRoleAssignment -ServicePrincipalName ServicePrincipalName
```

## <a name="sign-in-using-a-service-principal"></a>서비스 주체를 사용하여 로그인

로그인하여 새 서비스 주체의 자격 증명과 권한을 테스트합니다. 서비스 주체로 로그인하려면 해당 서비스와 연결된 `applicationId` 값과 이 서비스가 생성된 테넌트가 필요합니다.

암호를 사용하는 서비스 주체로 로그인하려면 다음과 같습니다.

```azurepowershell-interactive
# Use the application ID as the username, and the secret as password
$credentials = Get-Credential
Connect-AzAccount -ServicePrincipal -Credential $credentials -Tenant <tenant ID> 
```

인증서 기반 인증을 사용하려면 Azure PowerShell이 인증서 지문을 기반으로 로컬 인증서 저장소에서 정보를 검색할 수 있어야 합니다.

```azurepowershell-interactive
Connect-AzAccount -ServicePrincipal -Tenant <tenant ID> -CertificateThumbprint <thumbprint>
```

PowerShell에서 액세스할 수 있는 자격 증명 저장소로 인증서를 가져오는 방법은 [Azure PowerShell로 로그인](authenticate-azureps.md#sp-signin)을 참조하세요.

## <a name="reset-credentials"></a>자격 증명 다시 설정

서비스 주체에 대한 자격 증명을 잊어 버린 경우 [New-AzADSpCredential](/powershell/module/az.resources/new-azadspcredential)을 사용하여 새 자격 증명을 추가하세요. 이 cmdlet은 `New-AzADServicePrincipal`과 동일한 자격 증명 인수 및 형식을 사용합니다. 자격 증명 인수가 없으면 무작위 암호가 있는 새로운 `PasswordCredential`이 생성됩니다.

> [!IMPORTANT]
> 새 자격 증명을 할당하기 전에 해당 로그인을 방지하기 위해 기존 자격 증명을 제거하는 것이 좋습니다. 이를 위해서는 [Remove-AzADSpCredential](/powershell/module/az.resources/remove-azadspcredential) cmdlet을 사용합니다.
>
> ```azurepowershell-interactive
> Remove-AzADSpCredential -DisplayName ServicePrincipalName
> ```

```azurepowershell-interactive
$newCredential = New-AzADSpCredential -ServicePrincipalName ServicePrincipalName
```
