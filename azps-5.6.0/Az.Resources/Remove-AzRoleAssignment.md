---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 8C1D738C-825D-4718-AD2A-9CFEAA7DBD3B
online version: https://docs.microsoft.com/powershell/module/az.resources/remove-azroleassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzRoleAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzRoleAssignment.md
ms.openlocfilehash: d941e5cc3bf4a3f2363aa8369a7f5b0518ba2e07
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102005803"
---
# Remove-AzRoleAssignment

## SYNOPSIS
특정 범위에서 특정 역할에 할당된 지정된 주체에 대한 역할 할당을 제거합니다.

## 구문

### EmptyParameterSet(기본값)
```
Remove-AzRoleAssignment -ObjectId <String> [-Scope <String>] -RoleDefinitionName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ResourceWithObjectIdParameterSet
```
Remove-AzRoleAssignment -ObjectId <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] -RoleDefinitionName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ResourceGroupWithObjectIdParameterSet
```
Remove-AzRoleAssignment -ObjectId <String> -ResourceGroupName <String> -RoleDefinitionName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ScopeWithObjectIdParameterSet
```
Remove-AzRoleAssignment -ObjectId <String> [-Scope <String>] -RoleDefinitionName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### RoleIdWithScopeAndObjectIdParameterSet
```
Remove-AzRoleAssignment -ObjectId <String> [-Scope <String>] -RoleDefinitionId <Guid> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ResourceWithSignInNameParameterSet
```
Remove-AzRoleAssignment -SignInName <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] -RoleDefinitionName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ResourceGroupWithSignInNameParameterSet
```
Remove-AzRoleAssignment -SignInName <String> -ResourceGroupName <String> -RoleDefinitionName <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ScopeWithSignInNameParameterSet
```
Remove-AzRoleAssignment -SignInName <String> [-Scope <String>] -RoleDefinitionName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ResourceWithSPNParameterSet
```
Remove-AzRoleAssignment -ServicePrincipalName <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] -RoleDefinitionName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ResourceGroupWithSPNParameterSet
```
Remove-AzRoleAssignment -ServicePrincipalName <String> -ResourceGroupName <String> -RoleDefinitionName <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ScopeWithSPNParameterSet
```
Remove-AzRoleAssignment -ServicePrincipalName <String> [-Scope <String>] -RoleDefinitionName <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### RoleAssignmentParameterSet
```
Remove-AzRoleAssignment [-PassThru] [-InputObject] <PSRoleAssignment>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 설명
명령 Remove-AzRoleAssignment 명령렛을 사용하여 주어진 범위 및 주어진 역할의 모든 주체에 대한 액세스를 취소합니다.
할당의 개체(예: 주체)를 지정해야 합니다.
주체는 사용자(SignInName 또는 ObjectId 매개 변수를 사용하여 사용자를 식별), 보안 그룹(ObjectId 매개 변수를 사용하여 그룹을 식별) 또는 서비스 주체(ServicePrincipalName 또는 ObjectId 매개 변수를 사용하여 ServicePrincipal을 식별할 수 있습니다.
역할DefinitionName 매개 변수를 사용하여 주체에 할당된 역할을 지정해야 합니다.
할당 범위를 지정할 수 있으며 지정하지 않으면 구독 범위에 기본값으로 지정됩니다. 구독 범위에서 지정된 주체 및 역할에 대한 할당을 삭제하려고 합니다.
다음 매개 변수 중 하나를 사용하여 할당 범위를 지정할 수 있습니다.
a.
범위 - /subscriptions/b로 시작하는 완전히 자격을 갖춘 \<subscriptionId\> 범위입니다.
ResourceGroupName - 구독 아래 리소스 그룹의 이름입니다.
c.
ResourceName, ResourceType, ResourceGroupName 및(선택 사항) ParentResource - 구독 아래에서 특정 리소스를 식별합니다.

## 예제

### 예제 1
```
PS C:\> Remove-AzRoleAssignment -ResourceGroupName rg1 -SignInName john.doe@contoso.com -RoleDefinitionName Reader
```

rg1 리소스 그룹 범위에서 Reader 역할에 할당된 사용자에 대한 역할 john.doe@contoso.com 할당을 제거합니다.

### 예제 2
```
PS C:\> Remove-AzRoleAssignment -ObjectId 36f81fc3-b00f-48cd-8218-3879f51ff39f -RoleDefinitionName Reader
```

ObjectId로 식별된 그룹 주체에 대한 역할 할당을 제거하고 판독기 역할에 할당됩니다.
기본적으로 현재 구독을 범위로 사용하여 삭제할 할당을 찾습니다.

### 예제 3
```
PS C:\> $roleassignment = Get-AzRoleAssignment |Select-Object -First 1 -Wait
PS C:\> Remove-AzRoleAssignment -InputObject $roleassignment
```

명령줄에서 페치되는 첫 번째 역할 할당 개체를 Get-AzRoleAssignment 제거합니다.

## 매개 변수

### -DefaultProfile
azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독

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

### -InputObject
역할 할당 개체입니다.

```yaml
Type: Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleAssignment
Parameter Sets: RoleAssignmentParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ObjectId
사용자, 그룹 또는 서비스 주체의 Azure AD ObjectId입니다.

```yaml
Type: System.String
Parameter Sets: EmptyParameterSet, ResourceWithObjectIdParameterSet, ResourceGroupWithObjectIdParameterSet, ScopeWithObjectIdParameterSet, RoleIdWithScopeAndObjectIdParameterSet
Aliases: Id, PrincipalId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ParentResource
있는 경우 계층 구조의 상위 리소스(ResourceName 매개 변수를 사용하여 지정한 리소스)입니다.
ResourceGroupName, ResourceType 및 ResourceName 매개 변수와 함께 사용하여 리소스를 식별하는 상대 URI의 형태로 계층적 범위를 구성해야 합니다.

```yaml
Type: System.String
Parameter Sets: ResourceWithObjectIdParameterSet, ResourceWithSignInNameParameterSet, ResourceWithSPNParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PassThru
지정한 경우 삭제된 역할 할당이 표시됩니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
역할에 할당된 리소스 그룹 이름입니다.
지정된 리소스 그룹 범위에서 할당을 삭제하려고 합니다.
ResourceName, ResourceType 및 (선택적으로) ParentResource 매개 변수와 함께 사용하는 경우 명령은 리소스를 식별하는 상대 URI의 형태로 계층적 범위를 생성합니다.

```yaml
Type: System.String
Parameter Sets: ResourceWithObjectIdParameterSet, ResourceGroupWithObjectIdParameterSet, ResourceWithSignInNameParameterSet, ResourceGroupWithSignInNameParameterSet, ResourceWithSPNParameterSet, ResourceGroupWithSPNParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceName
리소스 이름입니다.
예: storageaccountprod의 경우.
ResourceGroupName, ResourceType 및 (선택적) ParentResource 매개 변수와 함께 사용하여 리소스를 식별하고 해당 범위에서 할당을 삭제하는 상대 URI의 형태로 계층적 범위를 구성해야 합니다.

```yaml
Type: System.String
Parameter Sets: ResourceWithObjectIdParameterSet, ResourceWithSignInNameParameterSet, ResourceWithSPNParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceType
리소스 유형입니다.
예: Microsoft.Network/virtualNetworks입니다.
ResourceGroupName, ResourceName 및 (선택 사항) ParentResource 매개 변수와 함께 사용하여 리소스를 식별하고 해당 리소스 범위에서 할당을 삭제하는 상대 URI의 형태로 계층적 범위를 구성해야 합니다.

```yaml
Type: System.String
Parameter Sets: ResourceWithObjectIdParameterSet, ResourceWithSignInNameParameterSet, ResourceWithSPNParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -RoleDefinitionId
할당을 삭제해야 하는 RBAC 역할의 ID입니다.

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
과제를 삭제해야 하는 RBAC 역할의 이름(예: Reader, 참가자, 가상 네트워크 관리자 등)입니다.

```yaml
Type: System.String
Parameter Sets: EmptyParameterSet, ResourceWithObjectIdParameterSet, ResourceGroupWithObjectIdParameterSet, ScopeWithObjectIdParameterSet, ResourceWithSignInNameParameterSet, ResourceGroupWithSignInNameParameterSet, ScopeWithSignInNameParameterSet, ResourceWithSPNParameterSet, ResourceGroupWithSPNParameterSet, ScopeWithSPNParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Scope
삭제할 역할 할당의 범위입니다.
상대 URI 형식입니다.
예: "/subscriptions/9004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourceGroups/TestRG"의 경우.
지정하지 않으면 구독 수준에서 역할을 삭제하려고 합니다.
지정한 경우 "/subscriptions/{id}"로 시작해야 합니다.

```yaml
Type: System.String
Parameter Sets: EmptyParameterSet, ScopeWithObjectIdParameterSet, RoleIdWithScopeAndObjectIdParameterSet, ScopeWithSignInNameParameterSet, ScopeWithSPNParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ServicePrincipalName
Azure AD 애플리케이션의 ServicePrincipalName

```yaml
Type: System.String
Parameter Sets: ResourceWithSPNParameterSet, ResourceGroupWithSPNParameterSet, ScopeWithSPNParameterSet
Aliases: SPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SignInName
사용자의 전자 메일 주소 또는 사용자 주체 이름입니다.

```yaml
Type: System.String
Parameter Sets: ResourceWithSignInNameParameterSet, ResourceGroupWithSignInNameParameterSet, ScopeWithSignInNameParameterSet
Aliases: Email, UserPrincipalName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -확인
cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## 입력

### System.String

### System.Guid

### Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleAssignment

## 출력

### Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleAssignment

## 참고 사항
키워드: azure, azurerm, arm, 리소스, 관리, 관리자, 리소스, 그룹, 템플릿, 배포

## 관련 링크

[New-AzRoleAssignment](./New-AzRoleAssignment.md)

[Get-AzRoleAssignment](./Get-AzRoleAssignment.md)

[Get-AzRoleDefinition](./Get-AzRoleDefinition.md)

