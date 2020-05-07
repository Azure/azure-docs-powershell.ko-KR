---
title: Azure PowerShell로 로그인
description: Azure PowerShell 사용자나 서비스 주체로 로그인 또는 Azure 리소스에 대한 관리 ID로 로그인하는 방법.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 09/09/2018
ms.openlocfilehash: 464d7efa640f1d1ffd1c34bfbe6cf13cbe5202b6
ms.sourcegitcommit: d661f38bec34e65bf73913db59028e11fd78b131
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/05/2020
ms.locfileid: "68863233"
---
# <a name="sign-in-with-azure-powershell"></a>Azure PowerShell로 로그인

[!INCLUDE [migrate-to-az](../includes/migrate-to-az.md)]

Azure PowerShell에서는 여러 인증 방법을 지원합니다. 가장 간단하게 시작하는 방법은 명령줄에서 대화형으로 로그인하는 것입니다.

## <a name="sign-in-interactively"></a>대화형으로 로그인

대화형으로 로그인하려면 [Connect-AzureRmAccount](/powershell/module/azurerm.profile/connect-azurermaccount) cmdlet을 사용합니다.

```azurepowershell-interactive
Connect-AzureRmAccount
```

이 cmdlet을 실행하면, 귀하의 Azure 계정과 연결된 이메일 주소와 암호를 묻는 대화 상자를 표시합니다. 이 인증은 현재 PowerShell 세션 동안 유지됩니다.

> [!IMPORTANT]
> Azure PowerShell 6.3.0부터는 Windows에 로그인한 상태를 유지하는 한, 여러 PowerShell 세션에서 자격 증명을 공유할 수 있습니다. 자세한 내용은 [영구 자격 증명](context-persistence.md)에 대한 아티클을 참조합니다.

## <a name="sign-in-with-a-service-principal"></a>서비스 주체를 사용하여 로그인

서비스 주체는 비대화형 Azure 계정입니다. 다른 사용자 계정과 마찬가지로 해당 권한은 Azure Active Directory를 사용하여 관리됩니다. 서비스 주체에 필요한 권한만 부여하여 자동화 스크립트 보안을 유지할 수 있습니다.

Azure PowerShell에 사용할 서비스 주체를 생성하는 방법을 보려면 [Azure PowerShell을 사용하여 Azure 서비스 주체 만들기](create-azure-service-principal-azureps.md)를 참조하세요.

서비스 주체로 로그인하려면 `-ServicePrincipal` cmdlet `Connect-AzureRmAccount`인수를 사용합니다. 또한 서비스 주체의 로그인 자격 증명 및 서비스 주체와 연결된 테넌트 ID가 필요합니다. 서비스 주체의 자격 증명을 적절한 개체로 가져오려면 [Get-credential](/powershell/module/microsoft.powershell.security/get-credential) cmdlet을 사용합니다. 이 cmdlet은 서비스 주체 사용자 ID와 암호를 입력하는 대화 상자를 표시합니다.

```azurepowershell-interactive
$pscredential = Get-Credential
Connect-AzureRmAccount -ServicePrincipal -Credential $pscredential -TenantId $tenantid
```

## <a name="sign-in-using-an-azure-managed-service-identity"></a>Azure 관리 서비스 ID를 사용하여 로그인

Azure 리소스에 대한 관리 ID는 Azure Active Directory의 기능입니다. 로그인에 관리 ID 서비스 주체를 사용할 수 있으며, 다른 리소스에 액세스하려면 앱 전용 액세스 토큰이 필요합니다. 관리 ID는 Azure 클라우드에서 실행 중인 가상 머신에서만 사용할 수 있습니다.

Azure 리소스의 관리 ID에 대한 자세한 내용은 [Azure VM에서 Azure 리소스에 대한 관리 ID를 사용하여 액세스 토큰을 획득하는 방법](/azure/active-directory/managed-identities-azure-resources/how-to-use-vm-token)을 참조하세요.

## <a name="sign-in-as-a-cloud-solution-provider-csp"></a>CSP(클라우드 솔루션 공급자)로 로그인

[CSP(클라우드 솔루션 공급자)](https://azure.microsoft.com/offers/ms-azr-0145p/) 로그인에는 `-TenantId`를 사용해야 합니다. 일반적으로 이 매개 변수를 테넌트 ID 또는 도메인 이름으로 제공할 수 있습니다. 그러나 CSP 로그인의 경우 **테넌트 ID**를 제공해야 합니다.

```azurepowershell-interactive
Connect-AzureRmAccount -TenantId 'xxxx-xxxx-xxxx-xxxx'
```

## <a name="sign-in-to-another-cloud"></a>다른 클라우드로 로그인

Azure 클라우드 서비스는 지역 데이터 처리 규정을 준수하는 환경을 제공합니다.
지역별 클라우드의 계정에 대해 로그인할 때 `-Environment` 인수를 사용해서 환경을 설정합니다.
예를 들어 계정이 중국 클라우드에 있는 경우:

```azurepowershell-interactive
Connect-AzureRmAccount -Environment AzureChinaCloud
```

다음 명령은 사용 가능한 환경 목록을 가져옵니다.

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
* [Set-AzureRmRoleDefinition](/powershell/module/AzureRM.Resources/Set-AzureRmRoleDefinition)
