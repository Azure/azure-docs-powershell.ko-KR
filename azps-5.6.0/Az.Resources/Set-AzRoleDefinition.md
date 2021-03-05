---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 115A7612-4856-47AE-AEE4-918350CD7009
online version: https://docs.microsoft.com/powershell/module/az.resources/set-azroledefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzRoleDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzRoleDefinition.md
ms.openlocfilehash: 18488b44ff99c44d6362de68de45e81853418e0c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101971760"
---
# Set-AzRoleDefinition

## SYNOPSIS
Azure RBAC에서 사용자 지정 역할을 수정합니다.
수정된 역할 정의를 JSON 파일로 또는 PSRoleDefinition으로 제공합니다.
먼저 Get-AzRoleDefinition 명령을 사용하여 수정할 사용자 지정 역할을 검색합니다.
그런 다음 변경할 속성을 수정합니다.
마지막으로 이 명령을 사용하여 역할 정의를 저장합니다.

## 구문

### InputFileParameterSet
```
Set-AzRoleDefinition -InputFile <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### RoleDefinitionParameterSet
```
Set-AzRoleDefinition -Role <PSRoleDefinition> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명
Set-AzRoleDefinition cmdlet은 Azure Role-Based 사용자 지정 역할을 업데이트합니다.
JSON 파일 또는 PSRoleDefinition 개체로 명령에 대한 입력으로 업데이트된 역할 정의를 입력합니다.
업데이트된 사용자 지정 역할에 대한 역할 정의에는 업데이트되지 않은 경우에도 역할의 ID 및 기타 모든 필수 속성(DisplayName, 설명, 작업, 할당 가능Scopes)이 포함되어야 합니다.
NotActions, DataActions, NotDataActions는 선택 사항입니다.
다음은 "52a6cc13-ff92-47a8-a39b-2a8205c3087e", "이름": "업데이트된 역할", "설명": "모든 리소스를 모니터링하고 가상 머신을 시작하고 다시 시작할 수 있습니다"에 대한 샘플 업데이트된 역할 Set-AzRoleDefinition 정의 json입니다. "작업": \[ *"/read", "Microsoft.ClassicCompute/virtualmachines/restart/action", "Microsoft.ClassicCompute/virtualmachines/start/action" \] , "NotActions": \[ "DataActions":* \] \[ "Microsoft.Storage/storageAccounts/blobServices/containers/blobs/read" \] , "NotDataAction" \[ "Microsoft.Storage/storageAccounts/blobServices/containers/blobs/write" \] , "AssignableScopes": \[ "/subscriptions/xxxxx-xxx-xx-xx" \] }

## 예제

### 예제 1: PSRoleDefinitionObject를 사용하여 업데이트
```powershell
PS C:\> $roleDef = Get-AzRoleDefinition "Contoso On-Call"
PS C:\> $roleDef.Actions.Add("Microsoft.ClassicCompute/virtualmachines/start/action")
PS C:\> $roleDef.Description = "Can monitor all resources and start and restart virtual machines"
PS C:\> $roleDef.AssignableScopes = @("/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx", "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx")
PS C:\> Set-AzRoleDefinition -Role $roleDef
```

### 예제 2: JSON 파일을 사용하여 만들기
```powershell
PS C:\> Set-AzRoleDefinition -InputFile C:\Temp\roleDefinition.json
```

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

### -InputFile
업데이트할 단일 json 역할 정의를 포함하는 파일 이름입니다.
JSON에서 업데이트할 속성만 포함합니다.
ID 속성이 필요합니다.

```yaml
Type: System.String
Parameter Sets: InputFileParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -역할
업데이트할 역할 정의 개체

```yaml
Type: Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition
Parameter Sets: RoleDefinitionParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## 입력

### Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition

## 출력

### Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition

## 참고 사항
키워드: azure, azurerm, arm, 리소스, 관리, 관리자, 리소스, 그룹, 템플릿, 배포

## 관련 링크

[Get-AzProviderOperation](./Get-AzProviderOperation.md)

[Get-AzRoleDefinition](./Get-AzRoleDefinition.md)

[New-AzRoleDefinition](./New-AzRoleDefinition.md)

[Remove-AzRoleDefinition](./Remove-AzRoleDefinition.md)

