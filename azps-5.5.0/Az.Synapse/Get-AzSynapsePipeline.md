---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsepipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapsePipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapsePipeline.md
ms.openlocfilehash: 6224a871aebff834693c8eed3026a75f22879ffa
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100207677"
---
# Get-AzSynapsePipeline

## SYNOPSIS
작업 영역의 파이프라인에 대한 정보를 얻습니다.

## 구문

### GetByName(기본값)
```
Get-AzSynapsePipeline -WorkspaceName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### GetByObject
```
Get-AzSynapsePipeline -WorkspaceObject <PSSynapseWorkspace> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명
**Get-AzSynapsePipeline** cmdlet은 작업 영역의 파이프라인에 대한 정보를 얻습니다. 파이프라인의 이름을 지정하는 경우 이 cmdlet은 해당 파이프라인에 대한 정보를 얻습니다. 이름을 지정하지 않으면 이 cmdlet은 작업 영역의 모든 파이프라인에 대한 정보를 얻습니다.

## 예제

### 예제 1
```powershell
PS C:\> Get-AzSynapsePipeline -WorkspaceName ContosoWorkspace
```

이 명령은 ContosoWorkspace라는 작업 영역의 모든 파이프라인에 대한 정보를 얻습니다.

### 예제 2
```powershell
PS C:\> Get-AzSynapsePipeline -WorkspaceName ContosoWorkspace -Name ContosoPipeline
```

이 명령은 ContosoWorkspace라는 작업 영역의 ContosoPipeline 파이프라인에 대한 정보를 얻습니다.

### 예제 3
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapsePipeline -Name ContosoPipeline
```

이 명령은 파이프라인을 통해 ContosoWorkspace라는 작업 영역의 ContosoPipeline이라는 파이프라인에 대한 정보를 얻습니다.

## PARAMETERS

### -DefaultProfile
Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.

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

### -Name
파이프라인 이름입니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: PipelineName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WorkspaceName
Synapse 작업 영역의 이름입니다.

```yaml
Type: System.String
Parameter Sets: GetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WorkspaceObject
일반적으로 파이프라인을 통해 전달되는 작업 영역 입력 개체입니다.

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: GetByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.

## 입력

### Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace

## 출력

### Microsoft.Azure.Commands.Synapse.Models.PSPipelineResource

## 참고 사항

## 관련 링크
