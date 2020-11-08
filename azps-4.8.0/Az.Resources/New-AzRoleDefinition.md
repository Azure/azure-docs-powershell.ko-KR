---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 8300B143-E322-419E-BC98-DBA56DD90A59
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azroledefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzRoleDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzRoleDefinition.md
ms.openlocfilehash: 8916b35da467fb16fd3802b726a7e105093b1c7a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94204422"
---
# New-AzRoleDefinition

## SYNOPSIS
Azure RBAC에서 사용자 지정 역할을 만듭니다.
JSON 역할 정의 파일 또는 PSRoleDefinition 개체 중 하나를 입력으로 제공 합니다.
먼저 Get-AzRoleDefinition 명령을 사용 하 여 기준 역할 정의 개체를 생성 합니다.
그런 다음 필요에 따라 해당 속성을 수정 합니다.
마지막으로이 명령을 사용 하 여 역할 정의를 사용 하 여 사용자 지정 역할을 만듭니다.

## 구문과

### InputFileParameterSet
```
New-AzRoleDefinition [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### RoleDefinitionParameterSet
```
New-AzRoleDefinition [-Role] <PSRoleDefinition> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명은
New-AzRoleDefinition cmdlet은 Azure Role-Based 액세스 제어에서 사용자 지정 역할을 만듭니다.
역할 정의를 JSON 파일 또는 PSRoleDefinition 개체로 명령에 대 한 입력으로 제공 합니다.
입력 역할 정의에는 다음 속성이 포함 되어야 합니다.
1) DisplayName: 사용자 지정 역할의 이름입니다.
2) 설명: 역할이 부여 하는 액세스를 요약 하는 역할에 대 한 간략 한 설명입니다.
3) 작업: 사용자 지정 역할이 액세스를 허용 하는 작업 집합입니다.
Get-AzProviderOperation를 사용 하 여 Azure RBAC를 사용 하 여 보호할 수 있는 Azure 리소스 공급자에 대 한 작업을 가져옵니다.
다음은 유효한 작업 문자열입니다.
 - "*/read"는 모든 Azure 리소스 공급자의 읽기 작업에 대 한 액세스 권한을 부여 합니다.
 - "Microsoft. 네트워크/*/cread"는 Microsoft의 모든 리소스 종류에 대 한 읽기 작업에 대 한 액세스 권한을 Azure의 네트워크 리소스 공급자에 게 부여 합니다.
 - "Microsoft. Compute/virtualMachines/*"는 가상 컴퓨터 및 해당 자식 리소스 형식의 모든 작업에 대 한 액세스 권한을 부여 합니다.
4) AssignableScopes: 사용자 지정 역할을 할당할 수 있는 범위 (Azure 구독 또는 리소스 그룹) 집합입니다.
AssignableScopes를 사용 하면 사용자 지정 역할을 필요로 하는 구독 또는 리소스 그룹 에서만 할당할 수 있으며 나머지 구독 또는 리소스 그룹에 대 한 사용자 환경이 복잡 하지 않게 할 수 있습니다.
다음은 몇 가지 유효한 할당 가능한 범위입니다.
 - "/subscriptions/c276fc76-9cd4-44c9-99a7-4fd71546436e", "/subscriptions/e91d47c4-76f3-4271-a796-21b4ecfe3624": 두 구독에서 역할을 할당에 사용할 수 있도록 합니다.
 - "/subscriptions/c276fc76-9cd4-44c9-99a7-4fd71546436e": 단일 구독에서 역할을 할당에 사용할 수 있도록 합니다.
 - "/subscriptions/c276fc76-9cd4-44c9-99a7-4fd71546436e/resourceGroups/Network": 네트워크 리소스 그룹 에서만 역할을 할당에 사용할 수 있도록 합니다.
입력 역할 정의에는 다음 속성이 포함 될 수 있습니다.
1) NotActions (작업): 사용자 지정 역할에 대 한 유효 작업을 결정 하기 위해 작업에서 제외 해야 하는 작업 집합입니다.
사용자 지정 역할에 대 한 액세스 권한을 부여 하지 않으려는 특정 작업이 있는 경우 작업에서 특정 작업을 제외한 모든 작업을 지정 하는 대신 NotActions를 사용 하 여 제외 하면 편리 합니다.
2) DataActions: 사용자 지정 역할이 액세스를 허용 하는 데이터 작업 집합입니다.
3) NotDataActions: 사용자 지정 역할에 대 한 유효한 데이터 작업을 결정 하기 위해 DataActions에서 제외할 작업 집합입니다.
사용자 지정 역할에 대 한 액세스 권한을 부여 하지 않으려는 특정 데이터 작업이 있는 경우에는 작업에서 특정 작업을 제외한 모든 작업을 지정 하는 대신 NotDataActions를 사용 하 여이 작업을 수행 하는 것이 편리 합니다.
참고: 사용자에 게 NotActions에서 작업을 지정 하 고 다른 역할에 할당 된 동일한 작업에 대 한 액세스 권한을 부여 하는 역할이 할당 되 면 사용자가 해당 작업을 수행할 수 있습니다.
NotActions는 거부 규칙이 아니므로 특정 작업을 제외 해야 할 때 허용 되는 작업 집합을 만드는 간단한 방법입니다.
다음은 입력 {"Name": "업데이트 된 역할", "설명": "모든 리소스를 모니터링 하 고 가상 컴퓨터를 시작 하 고 다시 시작할 수 있음", "작업", "ClassicCompute/virtualmachines/다시 시작/실행"을 제공 하는 샘플 json 역할 정의입니다. \[ *Microsoft. ClassicCompute/virtualmachines/start/action " \] ," notactions ": \[ "* /Cwrite " \] ," Dataactions ":" \[ Microsoft 저장소/storageaccounts/blobservices/컨테이너/blob/read " \] ," Notdataaction ": \[ " microsoft. 저장소/storageaccounts/blobservices/컨테이너/blob/write " \] ," AssignableScopes ": \[ "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx " \] }

## 예제의

### 예제 1: PSRoleDefinitionObject를 사용 하 여 만들기
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

### 예제 2: JSON 파일을 사용 하 여 만들기
```powershell
PS C:\> New-AzRoleDefinition -InputFile C:\Temp\roleDefinition.json
```

## 변수

### -DefaultProfile
Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독

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
단일 json 역할 정의를 포함 하는 파일 이름입니다.

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

### -역할
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
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.

## 입력

### 않아야

## 출력

### Microsoft. a. PSRoleDefinition (.Resources.

## 상속자
키워드: azure, azurerm, arm, resource, 관리, 관리자, 리소스, 그룹, 서식 파일, 배포

## 관련 링크

[Get-AzProviderOperation](./Get-AzProviderOperation.md)

[Get-AzRoleDefinition](./Get-AzRoleDefinition.md)

[Set-AzRoleDefinition](./Set-AzRoleDefinition.md)

[제거-AzRoleDefinition](./Remove-AzRoleDefinition.md)

