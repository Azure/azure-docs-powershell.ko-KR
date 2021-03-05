---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 36EB9CE6-EAC9-471C-97D6-14E882E0F710
online version: https://docs.microsoft.com/powershell/module/az.batch/enable-azbatchcomputenodescheduling
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Enable-AzBatchComputeNodeScheduling.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Enable-AzBatchComputeNodeScheduling.md
ms.openlocfilehash: 2897a21f25ac0a91fec11d83b77c8219d12f88ad
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101995722"
---
# Enable-AzBatchComputeNodeScheduling

## SYNOPSIS
지정된 계산 노드에서 작업 일정을 가능하게 합니다.

## 구문

### ID(기본값)
```
Enable-AzBatchComputeNodeScheduling [-PoolId] <String> [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### InputObject
```
Enable-AzBatchComputeNodeScheduling [[-ComputeNode] <PSComputeNode>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명
**Enable-AzBatchComputeNodeScheduling** cmdlet을 사용하면 지정된 계산 노드에서 태스크를 설정할 수 있습니다.
계산 노드는 특정 애플리케이션 워크로드 전용 Azure 가상 머신입니다.

## 예제

### 예제 1: 계산 노드에서 작업 예정 사용
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName "contosobatchaccount"
PS C:\> Enable-AzBatchComputeNodeScheduling  -PoolId "myPool" -Id "tvm-1783593343_34-20151117t222514z" -BatchContext $Context
```

이러한 명령은 계산 노드 tvm-1783593343_34-20151117t222514z에서 태스크를 설정할 수 있습니다.
이를 위해 예제의 첫 번째 명령은 일괄 처리 계정 contosobatchaccount에 대한 계정 키를 포함하는 개체 참조를 만듭니다.
이 개체 참조는 이라는 변수에 $context.
그런 다음, 두 번째 명령은 이 개체 참조와 **enable-AzBatchComputeNodeScheduling** cmdlet을 사용하여 풀 myPool에 연결하고 tvm-1783593343_34-20151117t222514z에서 작업 예정을 사용하도록 설정합니다.

### 예제 2: 풀의 계산 노드에서 작업 예정 사용
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName "contosobatchaccount"
PS C:\> Get-AzBatchComputeNode -PoolId "Pool06"  -BatchContext $Context | Enable-AzBatchComputeNodeScheduling  -BatchContext $Context
```

이러한 명령은 풀 풀06에서 찾은 모든 계산 노드에서 태스크를 설정할 수 있습니다.
이 작업을 수행하려면 예제의 첫 번째 명령은 일괄 처리 계정 contosobatchaccount에 대한 계정 키를 포함하는 개체 참조를 만듭니다.
이 개체 참조는 이라는 변수에 $context.
예제의 두 번째 명령은 이 개체 참조 및 **Get-AzBatchComputeNode를** 사용하여 Pool06에 있는 모든 계산 노드의 컬렉션을 반환합니다.
그런 다음 해당 컬렉션은 **Enable-AzBatchComputeNodeScheduling** cmdlet에 파이프됩니다. 이는 컬렉션의 각 계산 노드에서 태스크를 설정할 수 있습니다.

## 매개 변수

### -BatchContext
Batch 서비스와 상호 작용하는 데 이 cmdlet이 사용하는 **BatchAccountContext** 인스턴스를 지정합니다.
Get-AzBatchAccount cmdlet을 사용하여 BatchAccountContext를 얻으면 Batch 서비스와 상호 작용할 때 Azure Active Directory 인증이 사용됩니다. 대신 공유 키 인증을 사용 Get-AzBatchAccountKey cmdlet을 사용하여 액세스 키가 채워진 BatchAccountContext 개체를 얻습니다. 공유 키 인증을 사용하는 경우 기본 액세스 키는 기본적으로 사용됩니다. 사용할 키를 변경하기 위해 BatchAccountContext.KeyInUse 속성을 설정합니다.

```yaml
Type: Microsoft.Azure.Commands.Batch.BatchAccountContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ComputeNode
작업일정이 활성화된 계산 노드에 대한 개체 참조를 지정합니다.
이 개체 참조는 Get-AzBatchComputeNode cmdlet을 사용하고 반환된 계산 노드 개체를 변수에 저장하여 만들어집니다.

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSComputeNode
Parameter Sets: InputObject
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DefaultProfile
Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.

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

### -Id
작업일정이 활성화된 계산 노드의 ID를 지정합니다.

```yaml
Type: System.String
Parameter Sets: Id
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PoolId
작업 일괄 처리가 활성화된 계산 노드가 포함된 일괄 처리 풀의 ID를 지정합니다.

```yaml
Type: System.String
Parameter Sets: Id
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## 입력

### Microsoft.Azure.Commands.Bat. Models.PSComputeNode

### Microsoft.Azure.Commands.Batch.BatchAccountContext

## 출력

### System.Void

## 참고 사항

## 관련 링크

[Disable-AzBatchComputeNodeScheduling](./Disable-AzBatchComputeNodeScheduling.md)


