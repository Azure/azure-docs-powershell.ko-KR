---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 2DF5FB4D-A5CB-439C-AC6F-DF2130AF33EC
online version: https://docs.microsoft.com/powershell/module/az.batch/disable-azbatchcomputenodescheduling
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Disable-AzBatchComputeNodeScheduling.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Disable-AzBatchComputeNodeScheduling.md
ms.openlocfilehash: 1e7438195b0749dabc5206238a32bc00be03ea31
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101994513"
---
# Disable-AzBatchComputeNodeScheduling

## SYNOPSIS
지정된 계산 노드에서 작업 일정을 사용하지 않도록 설정합니다.

## 구문

### ID(기본값)
```
Disable-AzBatchComputeNodeScheduling [-PoolId] <String> [-Id] <String>
 [-DisableSchedulingOption <DisableComputeNodeSchedulingOption>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### InputObject
```
Disable-AzBatchComputeNodeScheduling [[-ComputeNode] <PSComputeNode>]
 [-DisableSchedulingOption <DisableComputeNodeSchedulingOption>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명
**Disable-AzBatchComputeNodeScheduling** cmdlet은 지정된 계산 노드에서 작업 일정을 사용하지 않도록 설정합니다.
계산 노드는 특정 애플리케이션 워크로드 전용 Azure 가상 머신입니다.
계산 노드에서 작업 일자리를 사용하지 않도록 설정하면 현재 노드의 작업 큐에 있는 작업에 대해 무엇을 할지 결정할 수도 있습니다.
**Disable-AzBatchComputeNodeScheduling을** 사용하면 다음을 할 수 있습니다. 
- 작업을 종료하고 작업 큐에 다시 넣습니다.
이렇게 하면 해당 작업을 다른 계산 노드에서 다시 계획할 수 있습니다. 
- 작업을 종료하고 작업 큐에서 제거합니다.
이 방식으로 중지된 작업은 다시 계획되지 않습니다. 
- 현재 실행 중인 모든 작업이 완료될 때까지 기다렸다가 계산 노드에서 작업일정을 사용하지 않도록 설정합니다. 
- 실행 중인 모든 태스크가 완료될 때까지 기다렸다가 모든 데이터 보존 기간이 만료될 때까지 기다렸다가 계산 노드에서 작업 날짜를 사용하지 않도록 설정합니다.

## 예제

### 예제 1: 계산 노드에서 작업 예정 사용 안 하여
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName "contosobatchaccount"
PS C:\> Disable-AzBatchComputeNodeScheduling -PoolId "myPool" -Id "tvm-1783593343_34-20151117t222514z" -BatchContext $Context
```

이러한 명령은 계산 노드 tvm-1783593343_34-2015117t222514z에서 작업 일정을 사용하지 않도록 설정합니다.
이를 위해 예제의 첫 번째 명령은 일괄 처리 계정 contosobatchaccount에 대한 계정 키에 대한 개체 참조를 만듭니다.
이 개체 참조는 이라는 변수에 $context.
그런 다음 두 번째 명령은 이 개체 참조 및 **Disable-AzBatchComputeNodeScheduling** cmdlet을 사용하여 풀 myPool에 연결하고 노드 tvm-1783593343_34-20151117t222514z에서 작업 예정을 사용하지 않도록 설정합니다.
*DisableComputeNodeSchedulingOptions* 매개 변수에 현재 계산 노드에서 실행 중인 태스크가 포함되어 있지 않습니다.

### 예제 2: 풀의 모든 계산 노드에서 작업 일주를 사용하지 않도록 설정
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName "contosobatchaccount"
PS C:\> Get-AzBatchComputeNode -PoolId "Pool06"  -BatchContext $Context | Disable-AzBatchComputeNodeScheduling -BatchContext $Context
```

이러한 명령은 일괄 처리 풀 Pool06의 모든 컴퓨터 노드에서 작업 예정을 사용하지 않도록 설정합니다.
이 작업을 수행하려면 예제의 첫 번째 명령에서 일괄 처리 계정 contosobatchaccount에 대한 계정 키에 대한 개체 참조를 만듭니다.
이 개체 참조는 이라는 변수에 $context.
예제의 두 번째 명령은 이 개체 참조 및 **Get-AzBatchComputeNode를** 사용하여 Pool06에 있는 모든 계산 노드의 컬렉션을 반환합니다.
그런 다음, 해당 컬렉션을 **Disable-AzBatchComputeNodeScheduling** cmdlet으로 파이프하여 컬렉션의 각 계산 노드에서 작업 일주를 사용하지 않도록 설정합니다.
*DisableComputeNodeSchedulingOptions* 매개 변수에 현재 계산 노드에서 실행 중인 태스크가 포함되지 않습니다.

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
작업 일정을 사용할 수 없는 계산 노드에 대한 개체 참조를 지정합니다.
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

### -DisableSchedulingOption
이 cmdlet은 예약을 사용하지 않도록 설정하는 컴퓨터 노드에서 현재 실행 중인 모든 작업을 처리하는 방법을 지정합니다.
이 매개 변수에 대해 허용되는 값은 다음입니다.
- 다시 퀘이크합니다.
작업이 즉시 중지되어 작업 큐로 반환됩니다.
이렇게 하면 작업을 다른 계산 노드에서 다시 계획할 수 있습니다.
기본값입니다. 
- 종료합니다.
작업이 즉시 중지되고 작업 큐에서 제거됩니다.
이러한 작업은 다시 정해지지 않습니다. 
- TaskCompletion.
현재 실행 중인 작업은 계산 노드에서 작업일정을 사용하지 않도록 설정하기 전에 완료할 수 있습니다.
이 노드에는 새 작업이 예약되지 않습니다. 
- RetainedData.
현재 실행 중인 태스크는 완료할 수 있으며, 데이터 보존 기간은 계산 노드에서 작업 계획이 비활성화되기 전에 만료될 수 있습니다.
이 노드에는 새 작업이 예약되지 않습니다.

```yaml
Type: System.Nullable`1[Microsoft.Azure.Batch.Common.DisableComputeNodeSchedulingOption]
Parameter Sets: (All)
Aliases:
Accepted values: Requeue, Terminate, TaskCompletion

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Id
작업일정을 사용할 수 없는 계산 노드의 ID를 지정합니다.

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
작업 일괄 처리를 사용할 수 없는 계산 노드가 포함된 일괄 처리 풀의 ID를 지정합니다.
*PoolId* 매개 변수를 사용하는 경우 동일한 명령에서 *ComputeNode* 매개 변수를 사용하지 않습니다.

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

[Get-AzBatchAccountKey](./Get-AzBatchAccountKey.md)

[Enable-AzBatchComputeNodeScheduling](./Enable-AzBatchComputeNodeScheduling.md)


