---
title: Azure PowerShell로 로그인
description: Azure PowerShell 사용자나 서비스 주체로 로그인 또는 Azure 리소스에 대한 관리 ID로 로그인하는 방법.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/15/2017
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: e0174439078ffed2db67800f6bd43ff7e98d324e
ms.sourcegitcommit: 8b3126b5c79f453464d90669f0046ba86b7a3424
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/01/2020
ms.locfileid: "89243874"
---
# <a name="sign-in-with-azure-powershell"></a>Azure PowerShell로 로그인

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

Azure PowerShell에서는 여러 인증 방법을 지원합니다. 가장 간단하게 시작하는 방법은 명령줄에서 대화형으로 로그인하는 것입니다.

## <a name="sign-in-interactively"></a>대화형으로 로그인

대화형으로 로그인하려면 [Connect-AzureRmAccount](/powershell/module/azurerm.profile/connect-azurermaccount) cmdlet을 사용합니다.

```azurepowershell-interactive
Connect-AzureRmAccount
```

이 cmdlet을 실행하면, 귀하의 Azure 계정과 연결된 이메일 주소와 암호를 묻는 대화 상자를 표시합니다. 인증될 때, 현재 PowerShell 세션에 해당 정보가 저장됩니다. 대화 상자가 닫히고 모든 Azure PowerShell cmdlet에 액세스할 수 있습니다.

> [!IMPORTANT]
> 이 로그인은 현재 PowerShell 세션에 _대해서만_ 적용됩니다. 여러 세션에서 인증을 유지하려면 [영구 자격 증명](context-persistence.md) 아티클을 참조합니다.

## <a name="sign-in-with-a-service-principal"></a>서비스 주체를 사용하여 로그인

서비스 주체는 리소스를 조작하는 데 사용할 수 있는 비 대화형 계정을 만드는 방법을 제공합니다. 서비스 주체는 Azure Active Directory를 사용하여 규칙을 적용할 수 있는 사용자 계정과 비슷합니다. 서비스 주체에게 필요한 최소 사용 권한만 부여하여 자동화 스크립트를 훨씬 안전하게 보호할 수 있습니다.

Azure PowerShell에 사용할 서비스 주체를 생성하려면 [Azure PowerShell을 사용하여 Azure 서비스 주체 만들기](create-azure-service-principal-azureps.md)를 참조하세요.

서비스 주체로 로그인하려면 `Connect-AzureRmAccount` cmdlet `-ServicePrincipal`인수를 사용합니다. 또한 서비스 주체의 애플리케이션 ID, 로그인 자격 증명 및 서비스 주체와 연결된 테넌트 ID 가 필요합니다. 서비스 주체의 자격 증명을 적절한 개체로 가져오려면 [Get-credential](/powershell/module/microsoft.powershell.security/get-credential) cmdlet을 사용합니다. 이 cmdlet은 서비스 주체 사용자 ID와 암호를 입력하는 대화 상자를 표시합니다.

```azurepowershell-interactive
$pscredential = Get-Credential
Connect-AzureRmAccount -ServicePrincipal -ApplicationId  "http://my-app" -Credential $pscredential -TenantId $tenantid
```

## <a name="sign-in-using-managed-identities-for-azure-resources"></a>Azure 리소스에 대한 관리 ID를 사용하여 로그인

Azure 리소스에 대한 관리 ID는 Azure Active Directory의 기능입니다. 로그인에 관리 ID 서비스 주체를 사용할 수 있으며, 다른 리소스에 액세스하려면 앱 전용 액세스 토큰이 필요합니다. 관리 ID는 Azure 클라우드에서 실행 중인 가상 머신에서만 사용할 수 있습니다.

Azure 리소스의 관리 ID에 대한 자세한 내용은 [Azure VM에서 Azure 리소스에 대한 관리 ID를 사용하여 액세스 토큰을 획득하는 방법](/azure/active-directory/managed-identities-azure-resources/how-to-use-vm-token)을 참조하세요.

## <a name="sign-in-to-another-cloud"></a>다른 클라우드로 로그인

Azure Cloud Services는 다양한 지역의 데이터 처리 규정에 부합하는 다양한 환경을 제공합니다. Azure 계정이 이러한 지역과 관련된 클라우드에 있는 경우, 로그인 시 해당 환경을 지정해야 합니다. 예를 들어 계정이 중국 클라우드에 있으면 다음 명령을 사용하여 로그온합니다.

```azurepowershell-interactive
Connect-AzureRmAccount -Environment AzureChinaCloud
```

사용 가능한 환경 목록을 가져오려면 다음 명령을 사용합니다.

```azurepowershell-interactive
Get-AzureRmEnvironment | Select-Object Name
```

## <a name="learn-more-about-managing-azure-role-based-access"></a>Azure 역할 기반 액세스를 관리하는 방법에 대해 알아보기

Azure에서 인증 및 구독 관리에 대한 자세한 내용은 [계정, 구독 및 관리 역할 관리](/azure/active-directory/role-based-access-control-configure)를 참조하세요.

역할 관리를 위한 Azure PowerShell cmdlet:

* [Get-AzureRmRoleAssignment](/powershell/module/AzureRM.Resources/Get-AzureRmRoleAssignment)
* [Get-AzureRmRoleDefinition](/powershell/module/AzureRM.Resources/Get-AzureRmRoleDefinition)
* [New-AzureRmRoleAssignment](/powershell/module/AzureRM.Resources/New-AzureRmRoleAssignment)
* [New-AzureRmRoleDefinition](/powershell/module/AzureRM.Resources/New-AzureRmRoleDefinition)
* [Remove-AzureRmRoleAssignment](/powershell/module/AzureRM.Resources/Remove-AzureRmRoleAssignment)
* [Remove-AzureRmRoleDefinition](/powershell/module/AzureRM.Resources/Remove-AzureRmRoleDefinition)
* [Set-AzureRmRoleDefinition](/powershell/moduel/AzureRM.Resources/Set-AzureRmRoleDefinition)
