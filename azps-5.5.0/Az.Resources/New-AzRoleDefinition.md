---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 8300B143-E322-419E-BC98-DBA56DD90A59
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azroledefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzRoleDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzRoleDefinition.md
ms.openlocfilehash: 8916b35da467fb16fd3802b726a7e105093b1c7a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100183657"
---
# New-AzRoleDefinition

## SYNOPSIS
Azure RBAC에서 사용자 지정 역할을 만듭니다.
JSON 역할 정의 파일 또는 PSRoleDefinition 개체를 입력으로 입력합니다.
먼저 Get-AzRoleDefinition 명령을 사용하여 기준 역할 정의 개체를 생성합니다.
그런 다음, 필요한 경우 해당 속성을 수정합니다.
마지막으로, 이 명령을 사용하여 역할 정의를 사용하여 사용자 지정 역할을 만들 수 있습니다.

## 구문

### InputFileParameterSet
```
New-AzRoleDefinition [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### RoleDefinitionParameterSet
```
New-AzRoleDefinition [-Role] <PSRoleDefinition> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명
New-AzRoleDefinition cmdlet은 Azure Role-Based Access Control에서 사용자 지정 역할을 만듭니다.
JSON 파일 또는 PSRoleDefinition 개체로 명령에 대한 입력으로 역할 정의를 입력합니다.
입력 역할 정의는 반드시 다음 속성을 포함해야 합니다.
1) DisplayName: 사용자 지정 역할의 이름
2) 설명: 역할이 부여하는 액세스를 요약하는 역할에 대한 간략한 설명입니다.
3) 작업: 사용자 지정 역할이 액세스 권한을 부여하는 작업 집합입니다.
Azure Get-AzProviderOperation 사용하여 Azure RBAC를 사용하여 보호할 수 있는 Azure 리소스 공급자에 대한 작업을 얻습니다.
다음은 몇 가지 유효한 작업 문자열입니다.
 - "*/read"는 모든 Azure 리소스 공급자의 읽기 작업에 대한 액세스 권한을 부여합니다.
 - "Microsoft.Network/*/read"는 Azure의 Microsoft.Network 리소스 공급자에서 모든 리소스 종류에 대한 읽기 작업에 대한 액세스 권한을 부여합니다.
 - "Microsoft.Compute/virtualMachines/*"는 가상 머신 및 해당 자식 리소스 유형의 모든 작업에 대한 액세스 권한을 부여합니다.
4) AssignableScopes: 사용자 지정 역할을 할당에 사용할 수 있는 범위 집합(Azure 구독 또는 리소스 그룹)입니다.
AssignableScopes를 사용하면 사용자 지정 역할을 필요한 구독 또는 리소스 그룹에서만 할당할 수 있도록 할 수 있으며, 나머지 구독 또는 리소스 그룹에 대한 사용자 환경을 희미하게 만들 수 있습니다.
다음은 몇 가지 유효한 할당 가능한 범위입니다.
 - "/subscriptions/c276fc76-9cd4-44c9-99a7-4fd71546436e", "/subscriptions/e91d47c4-76f3-4271-a796-21b4ecfe3624": 역할을 두 구독에서 할당할 수 있도록 합니다.
 - "/subscriptions/c276fc76-9cd4-44c9-99a7-4fd71546436e": 역할을 단일 구독에서 할당할 수 있도록 합니다.
 - "/subscriptions/c276fc76-9cd4-44c9-99a7-4fd71546436e/resourceGroups/Network": 역할은 네트워크 리소스 그룹에서만 할당할 수 있도록 합니다.
입력 역할 정의에는 다음 속성이 포함될 수 있습니다.
1) NotActions: 사용자 지정 역할에 대한 유효 작업을 결정하기 위해 작업에서 제외해야 하는 작업 집합입니다.
사용자 지정 역할에 대한 액세스 권한을 부여하지 않을 특정 작업이 있는 경우 작업에서 특정 작업이 아닌 모든 작업을 지정하는 대신 NotActions를 사용하여 제외하는 것이 편리합니다.
2) DataActions: 사용자 지정 역할이 액세스 권한을 부여하는 데이터 작업 집합입니다.
3) NotDataActions: 사용자 지정 역할에 대한 효과적인 데이터 작업을 결정하기 위해 DataActions에서 제외해야 하는 작업 집합입니다.
사용자 지정 역할에서 액세스 권한을 부여하지 않을 특정 데이터 작업이 있는 경우 작업에서 해당 특정 작업이 아닌 모든 작업을 지정하는 대신 NotDataActions를 사용하여 제외하는 것이 편리합니다.
참고: NotActions에서 작업을 지정하는 역할이 사용자에게 할당되어 있으며 다른 역할이 동일한 작업에 대한 액세스 권한을 부여하는 경우 사용자는 해당 작업을 수행할 수 있습니다.
NotActions는 거부 규칙이 아니며 특정 작업을 제외해야 하는 경우 허용되는 작업 집합을 만드는 편리한 방법일 수 있습니다.
다음은 입력 { "이름": "업데이트된 역할", "설명": "모든 리소스를 모니터링하고 가상 머신을 시작 및 다시 시작할 수 있습니다", "작업": "/read"로 제공될 수 있는 샘플 json 역할 정의입니다. \[ *"Microsoft.ClassicCompute/virtualmachines/restart/action", "Microsoft.ClassicCompute/virtualmachines/start/action" \] , "NotActions": \[ "/write"* \] , "DataActions": \[ "Microsoft.Storage/storageAccounts/blobServices/containers/blobs/read" \] , "NotDataActions": \[ "Microsoft.Storage/storageAccounts/blobServices/containers/blobs/write" \] , "AssignableScopes": \[ "/subscriptions/xxxxxxxx-xxxx-xx-xx-xxx" \] }

## 예제

### 예제 1: PSRoleDefinitionObject를 사용하여 만들기
```powershell
PS C:\> $role = Get-AzRoleDefinition -Name "Virtual Machine Contributor"

PS C:\> $role.Id = $null
PS C:\> $role.Name = "Virtual Machine Operator"
PS C:\> $role.Description = "Can monitor, start, and restart virtual machines."
PS C:\> $role.Actions.RemoveRange(0,$role.Actions.Count)
PS C:\> $role.Actions.Add("Microsoft.Compute/*/read")
PS C:\> $role.Actions.Add("Microsoft.Compute/virtualMachines/start/action")
PS C:\> $role.Actions.Add("Microsoft.Compute/virtualMachines/restart/action")
PS C:\> $role.Actions.Add("Microsoft.Compute/virtualMachines/downloadRemoteDesktopConnectionFile/action")
PS C:\> $role.Actions.Add("Microsoft.Network/*/read")
PS C:\> $role.Actions.Add("Microsoft.Storage/*/read")
PS C:\> $role.Actions.Add("Microsoft.Authorization/*/read")
PS C:\> $role.Actions.Add("Microsoft.Resources/subscriptions/resourceGroups/read")
PS C:\> $role.Actions.Add("Microsoft.Resources/subscriptions/resourceGroups/resources/read")
PS C:\> $role.Actions.Add("Microsoft.Insights/alertRules/*")
PS C:\> $role.Actions.Add("Microsoft.Support/*")
PS C:\> $role.AssignableScopes.Clear()
PS C:\> $role.AssignableScopes.Add("/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx")

PS C:\> New-AzRoleDefinition -Role $role
```

### 예제 2: JSON 파일을 사용하여 만들기
```powershell
PS C:\> New-AzRoleDefinition -InputFile C:\Temp\roleDefinition.json
```

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

### -InputFile
단일 json 역할 정의를 포함하는 파일 이름입니다.

```yaml
Type: System.String
Parameter Sets: InputFileParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Role
역할 정의 개체입니다.

```yaml
Type: Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition
Parameter Sets: RoleDefinitionParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.

## 입력

### 없음

## 출력

### Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition

## 참고 사항
키워드: azure, azurerm, arm, 리소스, 관리, 관리자, 리소스, 그룹, 템플릿, 배포

## 관련 링크

[Get-AzProviderOperation](./Get-AzProviderOperation.md)

[Get-AzRoleDefinition](./Get-AzRoleDefinition.md)

[Set-AzRoleDefinition](./Set-AzRoleDefinition.md)

[Remove-AzRoleDefinition](./Remove-AzRoleDefinition.md)

