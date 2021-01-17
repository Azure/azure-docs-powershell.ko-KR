---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 488229AF-FD6D-4E1B-B3DA-E57CA781D91E
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azroleassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzRoleAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzRoleAssignment.md
ms.openlocfilehash: 1b96617ce162f3b024cc8a5bd7df2d66c3820c38
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98490475"
---
# Get-AzRoleAssignment

## SYNOPSIS
지정된 범위에서 Azure RBAC 역할 할당을 나열합니다.
기본적으로 선택한 Azure 구독의 모든 역할 할당을 나열합니다.
해당 매개 변수를 사용하여 특정 사용자에게 할당을 나열하거나 특정 리소스 그룹 또는 리소스에 대한 할당을 나열합니다.

## 구문

### EmptyParameterSet(기본값)
```
Get-AzRoleAssignment [-RoleDefinitionName <String>] [-IncludeClassicAdministrators]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ObjectIdParameterSet
```
Get-AzRoleAssignment -ObjectId <String> [-RoleDefinitionName <String>] [-ExpandPrincipalGroups]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ResourceGroupWithObjectIdParameterSet
```
Get-AzRoleAssignment -ObjectId <String> -ResourceGroupName <String> [-RoleDefinitionName <String>]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ResourceWithObjectIdParameterSet
```
Get-AzRoleAssignment -ObjectId <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] [-RoleDefinitionName <String>]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ScopeWithObjectIdParameterSet
```
Get-AzRoleAssignment -ObjectId <String> [-RoleDefinitionName <String>] -Scope <String>
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### RoleIdWithScopeAndObjectIdParameterSet
```
Get-AzRoleAssignment [-ObjectId <String>] -RoleDefinitionId <Guid> [-Scope <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ResourceGroupWithSignInNameParameterSet
```
Get-AzRoleAssignment -SignInName <String> -ResourceGroupName <String> [-RoleDefinitionName <String>]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ResourceWithSignInNameParameterSet
```
Get-AzRoleAssignment -SignInName <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] [-RoleDefinitionName <String>]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ScopeWithSignInNameParameterSet
```
Get-AzRoleAssignment -SignInName <String> [-RoleDefinitionName <String>] -Scope <String>
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### SignInNameParameterSet
```
Get-AzRoleAssignment -SignInName <String> [-RoleDefinitionName <String>] [-ExpandPrincipalGroups]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ResourceGroupWithSPNParameterSet
```
Get-AzRoleAssignment -ServicePrincipalName <String> -ResourceGroupName <String> [-RoleDefinitionName <String>]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ResourceWithSPNParameterSet
```
Get-AzRoleAssignment -ServicePrincipalName <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] [-RoleDefinitionName <String>]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ScopeWithSPNParameterSet
```
Get-AzRoleAssignment -ServicePrincipalName <String> [-RoleDefinitionName <String>] -Scope <String>
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### SPNParameterSet
```
Get-AzRoleAssignment -ServicePrincipalName <String> [-RoleDefinitionName <String>]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ResourceGroupParameterSet
```
Get-AzRoleAssignment -ResourceGroupName <String> [-RoleDefinitionName <String>] [-IncludeClassicAdministrators]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ResourceParameterSet
```
Get-AzRoleAssignment -ResourceGroupName <String> -ResourceName <String> -ResourceType <String>
 [-ParentResource <String>] [-RoleDefinitionName <String>] [-IncludeClassicAdministrators]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ScopeParameterSet
```
Get-AzRoleAssignment [-RoleDefinitionName <String>] -Scope <String> [-IncludeClassicAdministrators]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명
Get-AzRoleAssignment 명령을 사용하여 범위에 효과적인 모든 역할 할당을 나열합니다.
매개 변수가 없는 경우 이 명령은 구독에서 수행된 모든 역할 할당을 반환합니다.
이 목록은 보안 주체, 역할 및 범위에 대한 필터링 매개 변수를 사용하여 필터링할 수 있습니다.
과제의 제목을 지정해야 합니다.
사용자를 지정하기 위해 SignInName 또는 Azure AD ObjectId 매개 변수를 사용합니다.
보안 그룹을 지정하기 위해 Azure AD ObjectId 매개 변수를 사용합니다.
Azure AD 애플리케이션을 지정하기 위해 ServicePrincipalName 또는 ObjectId 매개 변수를 사용합니다.
할당되는 역할은 RoleDefinitionName 매개 변수를 사용하여 지정해야 합니다.
액세스 권한이 부여되는 범위를 지정할 수 있습니다.
기본적으로 선택한 구독으로 설정됩니다. 할당의 범위는 다음 매개 변수 조합 a 중 하나를 사용하여 지정할 수 있습니다.
범위 - /subscriptions/로 시작하는 정식 \<subscriptionId\> 범위입니다.
이렇게 하면 해당 범위에 적용된 할당( 즉, 해당 범위 이상에 있는 모든 할당)을 필터링합니다.
b.
ResourceGroupName - 구독에 속한 모든 리소스 그룹의 이름입니다.
이렇게 하면 지정된 리소스 그룹 c에서 유효하게 할당을 필터링합니다.
ResourceName, ResourceType, ResourceGroupName 및 (선택 사항) ParentResource - 구독에서 특정 리소스를 식별하고 해당 리소스 범위에서 유효 할당을 필터링합니다.
구독에서 특정 사용자에게 어떤 액세스 권한이 있는지 확인하려면 ExpandPrincipalGroups 스위치를 사용하세요.
그러면 사용자 및 사용자가 구성원인 그룹에 할당된 모든 역할이 나열됩니다.
IncludeClassicAdministrators 스위치를 사용하여 구독 관리자 및 공동 관리자도 표시합니다.

## 예제

### 예제 1
```
PS C:\> Get-AzRoleAssignment
```

구독의 모든 역할 할당 나열

### 예제 2
```
PS C:\> Get-AzRoleAssignment -ResourceGroupName testRG -SignInName john.doe@contoso.com
```

testRG 범위 이상에서 사용자 및 해당 사용자가 구성원인 그룹에 대해 수행된 모든 역할 john.doe@contoso.com 할당을 얻습니다.

### 예제 3
```
PS C:\> Get-AzRoleAssignment -ServicePrincipalName "http://testapp1.com"
```

지정된 서비스 주체의 모든 역할 할당을 얻습니다.

### 예제 4
```
PS C:\> Get-AzRoleAssignment -Scope "/subscriptions/96231a05-34ce-4eb4-aa6a-70759cbb5e83/resourcegroups/rg1/providers/Microsoft.Web/sites/site1"
```

'site1' 웹 사이트 범위에서 역할 할당을 얻습니다.

## PARAMETERS

### -DefaultProfile
Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ExpandPrincipalGroups
지정된 경우 사용자 및 사용자가 멤버인 그룹에 직접 할당된 역할을 반환합니다(전이적).
사용자 계정에서만 지원됩니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ObjectIdParameterSet, SignInNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IncludeClassicAdministrators
지정된 경우 구독 클래식 관리자(공동 관리자, 서비스 관리자 등) 역할 할당도 나열합니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: EmptyParameterSet, ObjectIdParameterSet, ResourceGroupWithObjectIdParameterSet, ResourceWithObjectIdParameterSet, ScopeWithObjectIdParameterSet, ResourceGroupWithSignInNameParameterSet, ResourceWithSignInNameParameterSet, ScopeWithSignInNameParameterSet, SignInNameParameterSet, ResourceGroupWithSPNParameterSet, ResourceWithSPNParameterSet, ScopeWithSPNParameterSet, SPNParameterSet, ResourceGroupParameterSet, ResourceParameterSet, ScopeParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ObjectId
사용자, 그룹 또는 서비스 주체의 Azure AD ObjectId입니다.
지정된 보안 주체에 대해 수행된 모든 할당을 필터합니다.

```yaml
Type: System.String
Parameter Sets: ObjectIdParameterSet, ResourceGroupWithObjectIdParameterSet, ResourceWithObjectIdParameterSet, ScopeWithObjectIdParameterSet
Aliases: Id, PrincipalId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: RoleIdWithScopeAndObjectIdParameterSet
Aliases: Id, PrincipalId

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ParentResource
ResourceName 매개 변수를 사용하여 지정된 리소스의 계층 구조에 있는 부모 리소스입니다.
ResourceGroupName, ResourceType 및 ResourceName 매개 변수와 함께 사용되어야 합니다.

```yaml
Type: System.String
Parameter Sets: ResourceWithObjectIdParameterSet, ResourceWithSignInNameParameterSet, ResourceWithSPNParameterSet, ResourceParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
리소스 그룹 이름입니다.
지정된 리소스 그룹에 효과적인 역할 할당을 나열합니다.
ResourceName, ResourceType 및 ParentResource 매개 변수와 함께 사용하는 경우 명령은 리소스 그룹 내의 리소스에서 효과적인 할당을 나열합니다.

```yaml
Type: System.String
Parameter Sets: ResourceGroupWithObjectIdParameterSet, ResourceWithObjectIdParameterSet, ResourceGroupWithSignInNameParameterSet, ResourceWithSignInNameParameterSet, ResourceGroupWithSPNParameterSet, ResourceWithSPNParameterSet, ResourceGroupParameterSet, ResourceParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceName
리소스 이름입니다.
예: storageaccountprod
ResourceGroupName, ResourceType 및 (선택 사항) ParentResource 매개 변수와 함께 사용되어야 합니다.

```yaml
Type: System.String
Parameter Sets: ResourceWithObjectIdParameterSet, ResourceWithSignInNameParameterSet, ResourceWithSPNParameterSet, ResourceParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceType
리소스 종류입니다.
예: Microsoft.Network/virtualNetworks
ResourceGroupName, ResourceName 및 (선택 사항) ParentResource 매개 변수와 함께 사용되어야 합니다.

```yaml
Type: System.String
Parameter Sets: ResourceWithObjectIdParameterSet, ResourceWithSignInNameParameterSet, ResourceWithSPNParameterSet, ResourceParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -RoleDefinitionId
보안 주체에 할당된 역할의 ID입니다.

```yaml
Type: System.Guid
Parameter Sets: RoleIdWithScopeAndObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -RoleDefinitionName
보안 주체에 할당된 역할(예: 읽기 권한자, 참가자, Virtual Network 관리자 등)

```yaml
Type: System.String
Parameter Sets: EmptyParameterSet, ObjectIdParameterSet, ResourceGroupWithObjectIdParameterSet, ResourceWithObjectIdParameterSet, ScopeWithObjectIdParameterSet, ResourceGroupWithSignInNameParameterSet, ResourceWithSignInNameParameterSet, ScopeWithSignInNameParameterSet, SignInNameParameterSet, ResourceGroupWithSPNParameterSet, ResourceWithSPNParameterSet, ScopeWithSPNParameterSet, SPNParameterSet, ResourceGroupParameterSet, ResourceParameterSet, ScopeParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Scope
역할 할당의 범위입니다.
상대 URI 형식입니다.
예: /subscriptions/9004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourceGroups/TestRG.
"/subscriptions/{id}"로 시작해야 합니다.
이 명령은 해당 범위에 적용된 모든 할당을 필터합니다.

```yaml
Type: System.String
Parameter Sets: ScopeWithObjectIdParameterSet, ScopeWithSignInNameParameterSet, ScopeWithSPNParameterSet, ScopeParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: RoleIdWithScopeAndObjectIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ServicePrincipalName
서비스 주체의 ServicePrincipalName입니다.
지정된 Azure AD 애플리케이션에 대해 수행된 모든 할당을 필터합니다.

```yaml
Type: System.String
Parameter Sets: ResourceGroupWithSPNParameterSet, ResourceWithSPNParameterSet, ScopeWithSPNParameterSet, SPNParameterSet
Aliases: SPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SignInName
사용자의 이메일 주소 또는 사용자 계정 이름입니다.
지정된 사용자에게 수행된 모든 할당을 필터합니다.

```yaml
Type: System.String
Parameter Sets: ResourceGroupWithSignInNameParameterSet, ResourceWithSignInNameParameterSet, ScopeWithSignInNameParameterSet, SignInNameParameterSet
Aliases: Email, UserPrincipalName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.

## 입력

### System.String

### System.Guid

## 출력

### Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleAssignment

## 참고 사항
키워드: azure, azurerm, arm, 리소스, 관리, 관리자, 리소스, 그룹, 템플릿, 배포

## 관련 링크

[New-AzRoleAssignment](./New-AzRoleAssignment.md)

[Remove-AzRoleAssignment](./Remove-AzRoleAssignment.md)

[Get-AzRoleDefinition](./Get-AzRoleDefinition.md)

