---
title: Azure PowerShell을 사용하여 Azure 서비스 주체 만들기
description: Azure PowerShell을 사용하여 앱 또는 서비스의 서비스 주체를 만드는 방법을 알아봅니다.
keywords: Azure PowerShell, Azure Active Directory, Azure Active directory, AD, RBAC
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/15/2017
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: 225ee512e09ccc2afbe4e632a3257d91ce9deb5c
ms.sourcegitcommit: 8b3126b5c79f453464d90669f0046ba86b7a3424
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/01/2020
ms.locfileid: "89244299"
---
# <a name="create-an-azure-service-principal-with-azure-powershell"></a>Azure PowerShell을 사용하여 Azure 서비스 주체 만들기

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

Azure PowerShell을 사용하여 앱 또는 서비스를 관리하려는 경우 소유한 자격 증명 대신 AAD(Azure Active Directory) 서비스 주체에서 실행해야 합니다. 이 항목에서는 Azure PowerShell을 사용하여 보안 주체를 만드는 과정을 설명합니다.

> [!NOTE]
> Azure Portal을 통해 서비스 주체를 만들 수도 있습니다. 자세한 내용은 [포털을 사용하여 리소스에 액세스할 수 있는 Active Directory 애플리케이션 및 서비스 주체 만들기](/azure/azure-resource-manager/resource-group-create-service-principal-portal)를 참고하세요.

## <a name="what-is-a-service-principal"></a>'서비스 주체'란?

Azure 서비스 주체는 특정 Azure 리소스에 액세스하기 위해 사용자가 만든 앱과 서비스, 자동화 도구에서 사용하는 보안 ID입니다. 특정한 역할이 있는 '사용자 ID'(사용자 이름과 암호 또는 인증서)이며 엄격하게 통제된 권한을 갖습니다. 일반 사용자 ID와 달리 특정 작업만을 수행해야 합니다. 해당 관리 작업을 수행하는 데 필요한 최소 사용 권한 수준을 부여하면 보안이 향상됩니다.

## <a name="verify-your-own-permission-level"></a>고유한 사용 권한 수준 확인

먼저 Azure Active Directory와 Azure 구독에 대한 충분한 권한이 있어야 합니다. 특히, Active Directory에서 앱을 만들고 서비스 주체에 역할을 할당할 수 있어야 합니다.

계정에 적절한 사용 권한이 있는지를 확인하는 가장 쉬운 방법은 포털을 통하는 것입니다. [필요한 사용 권한 확인](/azure/azure-resource-manager/resource-group-create-service-principal-portal#required-permissions)을 참조하세요.

## <a name="create-a-service-principal-for-your-app"></a>앱의 서비스 주체 만들기

Azure 계정에 로그인하면 서비스 주체를 만들 수 있습니다. 다음 방법 중 하나로 배포된 앱을 식별해야 합니다.

* 다음 예제처럼 "MyDemoWebApp"와 같은 배포된 앱의 고유 이름
* 애플리케이션 ID, 배포된 앱, 서비스 또는 개체와 관련된 고유 GUID

### <a name="get-information-about-your-application"></a>애플리케이션에 대한 정보 가져오기

`Get-AzureRmADApplication` cmdlet을 사용하여 애플리케이션에 대한 정보를 검색할 수 있습니다.

```powershell-interactive
Get-AzureRmADApplication -DisplayNameStartWith MyDemoWebApp
```

```output
DisplayName             : MyDemoWebApp
ObjectId                : 775f64cd-0ec8-4b9b-b69a-8b8946022d9f
IdentifierUris          : {http://MyDemoWebApp}
HomePage                : http://www.contoso.com
Type                    : Application
ApplicationId           : 00c01aaa-1603-49fc-b6df-b78c4e5138b4
AvailableToOtherTenants : False
AppPermissions          :
ReplyUrls               : {}
```

### <a name="create-a-service-principal-for-your-application"></a>애플리케이션의 서비스 주체 만들기

`New-AzureRmADServicePrincipal` cmdlet을 사용하여 서비스 주체를 만듭니다.

```powershell-interactive
Add-Type -Assembly System.Web
$password = [System.Web.Security.Membership]::GeneratePassword(16,3)
New-AzureRmADServicePrincipal -ApplicationId 00c01aaa-1603-49fc-b6df-b78c4e5138b4 -Password $password
```

```output
DisplayName                    Type                           ObjectId
-----------                    ----                           --------
MyDemoWebApp                   ServicePrincipal               698138e7-d7b6-4738-a866-b4e3081a69e4
```

### <a name="get-information-about-the-service-principal"></a>서비스 주체에 대한 정보 가져오기

```powershell-interactive
$svcprincipal = Get-AzureRmADServicePrincipal -ObjectId 698138e7-d7b6-4738-a866-b4e3081a69e4
$svcprincipal | Select-Object *
```

```output
ServicePrincipalNames : {http://MyDemoWebApp, 00c01aaa-1603-49fc-b6df-b78c4e5138b4}
ApplicationId         : 00c01aaa-1603-49fc-b6df-b78c4e5138b4
DisplayName           : MyDemoWebApp
Id                    : 698138e7-d7b6-4738-a866-b4e3081a69e4
Type                  : ServicePrincipal
```

### <a name="sign-in-using-the-service-principal"></a>서비스 주체를 사용하여 로그인

이제 제공한 *appId* 및 *암호*를 사용하여 앱에 새로운 서비스 주체로 로그인할 수 있습니다. 계정에 테넌트 ID를 제공해야 합니다. 개인 자격 증명을 사용하여 Azure에 로그인하는 경우 테넌트 ID가 표시됩니다.

```powershell-interactive
$cred = Get-Credential -UserName $svcprincipal.ApplicationId -Message "Enter Password"
Login-AzureRmAccount -Credential $cred -ServicePrincipal -TenantId XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
```

새 PowerShell 세션에서 이 명령을 실행합니다. 성공적으로 로그인한 후에 다음과 같은 출력이 표시됩니다.

```output
Environment           : AzureCloud
Account               : 00c01aaa-1603-49fc-b6df-b78c4e5138b4
TenantId              : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
SubscriptionId        :
SubscriptionName      :
CurrentStorageAccount :
```

축하합니다! 이러한 자격 증명을 사용하여 앱을 실행할 수 있습니다. 다음으로 서비스 주체의 사용 권한을 조정해야 합니다.

## <a name="managing-roles"></a>역할 관리

> [!NOTE]
> Azure 역할 기반 Access Control(RBAC)은 사용자 및 서비스 주체에 대한 역할을 정의하고 관리하기 위한 모델입니다. 역할에는 그와 관련된 일련의 사용 권한이 있으며 여기서 주체가 읽고 액세스하고 쓰고 관리할 수 있는 리소스를 결정합니다. RBAC와 역할에 대한 자세한 내용은 [RBAC: 기본 제공 역할](/azure/active-directory/role-based-access-built-in-roles)을 참조하세요.

Azure PowerShell은 역할 할당을 관리하는 다음과 같은 cmdlet을 제공합니다.

* [Get-AzureRmRoleAssignment](/powershell/module/azurerm.resources/get-azurermroleassignment)
* [New-AzureRmRoleAssignment](/powershell/module/azurerm.resources/new-azurermroleassignment)
* [Remove-AzureRmRoleAssignment](/powershell/module/azurerm.resources/remove-azurermroleassignment)

서비스 주체의 기본 역할은 **참가자**입니다. 광범위한 사용 권한을 고려하면 Azure 서비스와 앱의 상호 작용의 범위에 따라 최상의 선택이 아닐 수도 있습니다.
**읽기 권한자** 역할은 더 제한적이며 읽기 전용 앱의 경우에 좋은 선택이 될 수 있습니다. 역할 관련 사용 권한에 대한 세부 정보를 보거나 Azure Portal을 통해 사용자 지정 레코드를 만들 수 있습니다.

이 예제에서는 **읽기 권한자** 역할을 이전 예제에 추가하고 **참가자** 역할을 삭제합니다.

```powershell-interactive
New-AzureRmRoleAssignment -ResourceGroupName myRG -ObjectId 698138e7-d7b6-4738-a866-b4e3081a69e4 -RoleDefinitionName Reader
```

```output
RoleAssignmentId   : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/myRG/providers/Microsoft.Authorization/roleAssignments/818892f2-d075-46a1-a3a2-3a4e1a12fcd5
Scope              : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/myRG
DisplayName        : MyDemoWebApp
SignInName         :
RoleDefinitionName : Reader
RoleDefinitionId   : b24988ac-6180-42a0-ab88-20f7382dd24c
ObjectId           : 698138e7-d7b6-4738-a866-b4e3081a69e4
ObjectType         : ServicePrincipal
```

```powershell-interactive
Remove-AzureRmRoleAssignment -ResourceGroupName myRG -ObjectId 698138e7-d7b6-4738-a866-b4e3081a69e4 -RoleDefinitionName Contributor
```

현재 할당된 역할을 보려면:

```powershell-interactive
Get-AzureRmRoleAssignment -ResourceGroupName myRG -ObjectId 698138e7-d7b6-4738-a866-b4e3081a69e4
```

```output
RoleAssignmentId   : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/myRG/providers/Microsoft.Authorization/roleAssignments/0906bbd8-9982-4c03-8dae-aeaae8b13f9e
Scope              : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/myRG
DisplayName        : MyDemoWebApp
SignInName         :
RoleDefinitionName : Reader
RoleDefinitionId   : acdd72a7-3385-48ef-bd42-f606fba81ae7
ObjectId           : 698138e7-d7b6-4738-a866-b4e3081a69e4
ObjectType         : ServicePrincipal
```

역할 관리를 위한 기타 Azure PowerShell cmdlet:

* [Get-AzureRmRoleDefinition](/powershell/module/azurerm.resources/Get-AzureRmRoleDefinition)
* [New-AzureRmRoleDefinition](/powershell/module/azurerm.resources/New-AzureRmRoleDefinition)
* [Remove-AzureRmRoleDefinition](/powershell/module/azurerm.resources/Remove-AzureRmRoleDefinition)
* [Set-AzureRmRoleDefinition](/powershell/module/azurerm.resources/Set-AzureRmRoleDefinition)

## <a name="change-the-credentials-of-the-security-principal"></a>보안 주체의 자격 증명 변경

보안을 향상시키려면 사용 권한을 검토하고 암호를 정기적으로 업데이트하는 것이 좋습니다. 앱이 변경될 때 보안 자격 증명을 관리하고 수정할 수도 있습니다. 예를 들어, 새 암호를 만들고 이전 암호를 제거하여 서비스 주체의 암호를 변경할 수 있습니다.

### <a name="add-a-new-password-for-the-service-principal"></a>서비스 주체의 새 암호 추가

```powershell-interactive
$password = [System.Web.Security.Membership]::GeneratePassword(16,3)
New-AzureRmADSpCredential -ServicePrincipalName http://MyDemoWebApp -Password $password
```

```output
StartDate           EndDate             KeyId                                Type
---------           -------             -----                                ----
3/8/2017 5:58:24 PM 3/8/2018 5:58:24 PM 6f801c3e-6fcd-42b9-be8e-320b17ba1d36 Password
```

### <a name="get-a-list-of-credentials-for-the-service-principal"></a>서비스 주체의 자격 증명 목록 가져오기

```powershell-interactive
Get-AzureRmADSpCredential -ServicePrincipalName http://MyDemoWebApp
```

```output
StartDate           EndDate             KeyId                                Type
---------           -------             -----                                ----
3/8/2017 5:58:24 PM 3/8/2018 5:58:24 PM 6f801c3e-6fcd-42b9-be8e-320b17ba1d36 Password
5/5/2016 4:55:27 PM 5/5/2017 4:55:27 PM ca9d4846-4972-4c70-b6f5-a4effa60b9bc Password
```

### <a name="remove-the-old-password-from-the-service-principal"></a>서비스 주체에게서 이전 암호 제거

```powershell-interactive
Remove-AzureRmADSpCredential -ServicePrincipalName http://MyDemoWebApp -KeyId ca9d4846-4972-4c70-b6f5-a4effa60b9bc
```

```output
Confirm
Are you sure you want to remove credential with keyId '6f801c3e-6fcd-42b9-be8e-320b17ba1d36' for
service principal objectId '698138e7-d7b6-4738-a866-b4e3081a69e4'.
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

### <a name="verify-the-list-of-credentials-for-the-service-principal"></a>서비스 주체의 자격 증명 목록 확인

```powershell-interactive
Get-AzureRmADSpCredential -ServicePrincipalName http://MyDemoWebApp
```

```output
StartDate           EndDate             KeyId                                Type
---------           -------             -----                                ----
3/8/2017 5:58:24 PM 3/8/2018 5:58:24 PM 6f801c3e-6fcd-42b9-be8e-320b17ba1d36 Password
```
