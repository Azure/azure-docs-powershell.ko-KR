---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 2DF5FB4D-A5CB-439C-AC6F-DF2130AF33EC
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/disable-azbatchcomputenodescheduling
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Disable-AzBatchComputeNodeScheduling.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Disable-AzBatchComputeNodeScheduling.md
ms.openlocfilehash: 9e93d6fd17d4ba308e6d5752554fb03639fce769
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94216429"
---
# Disable-AzBatchComputeNodeScheduling

## SYNOPSIS
지정 된 계산 노드에서 작업 일정을 사용 하지 않도록 설정 합니다.

## 구문과

### Id (기본값)
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

## 설명은
**AzBatchComputeNodeScheduling** cmdlet은 지정 된 계산 노드에서 작업 일정을 사용 하지 않도록 설정 합니다.
계산 노드는 특정 응용 프로그램 작업을 전담 하는 Azure 가상 컴퓨터입니다.
계산 노드에서 작업 일정을 사용 하지 않도록 설정 하는 경우 현재 노드의 작업 큐에 있는 작업에 대해 할 일을 결정 하는 옵션도 있습니다.
**Disable-AzBatchComputeNodeScheduling** 다음을 수행할 수 있습니다. 
- 작업을 종료 하 고 작업 큐에 다시 둡니다.
이렇게 하면 다른 계산 노드에서 해당 작업의 일정을 재조정할 수 있습니다. 
- 작업을 종료 하 고 작업 큐에서 제거 합니다.
이 방법으로 중지 된 작업은 일정 조정 되지 않습니다. 
- 현재 실행 중인 모든 작업이 완료 될 때까지 기다린 다음 계산 노드에서 작업 일정을 사용 하지 않도록 설정 합니다. 
- 실행 중인 모든 작업이 완료 될 때까지 기다렸다가 모든 데이터 보존 기간이 만료 되 면 계산 노드에서 작업 일정을 사용 하지 않도록 설정 합니다.

## 예제의

### 예제 1: 계산 노드에서 작업 일정 사용 안 함
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName "contosobatchaccount"
PS C:\> Disable-AzBatchComputeNodeScheduling -PoolId "myPool" -Id "tvm-1783593343_34-20151117t222514z" -BatchContext $Context
```

이러한 명령은 계산 노드 tvm-1783593343_34-20151117t222514z에서 작업 일정을 사용 하지 않도록 설정 합니다.
이렇게 하려면 예제의 첫 번째 명령은 batch 계정 contosobatchaccount의 계정 키에 대 한 개체 참조를 만듭니다.
이 개체 참조는 $context 라는 변수에 저장 됩니다.
그런 다음 두 번째 명령은이 개체 참조 및 **AzBatchComputeNodeScheduling** cmdlet을 사용 하 여 풀 myPool에 연결 하 고 노드 tvm-1783593343_34-20151117t222514z에서 작업 일정을 사용 하지 않도록 설정 합니다.
*DisableComputeNodeSchedulingOptions* 매개 변수가 포함 되지 않았으므로 계산 노드에서 현재 실행 중인 작업은 다시 착신으로 설정 됩니다.

### 예제 2: 풀의 모든 계산 노드에서 작업 일정 사용 안 함
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName "contosobatchaccount"
PS C:\> Get-AzBatchComputeNode -PoolId "Pool06"  -BatchContext $Context | Disable-AzBatchComputeNodeScheduling -BatchContext $Context
```

이러한 명령은 일괄 처리 풀 Pool06의 모든 컴퓨터 노드에서 작업 일정을 사용 하지 않도록 설정 합니다.
이 작업을 수행 하기 위해 예제의 첫 번째 명령은 일괄 계정 contosobatchaccount의 계정 키에 대 한 개체 참조를 만듭니다.
이 개체 참조는 $context 라는 변수에 저장 됩니다.
그런 다음이 예제의 두 번째 명령은이 개체 참조를 사용 하 여 Pool06에 있는 모든 계산 노드의 컬렉션을 반환 합니다. **AzBatchComputeNode** .
그런 다음 해당 컬렉션을 파이프라인으로 **AzBatchComputeNodeScheduling cmdlet을 사용 하지 않도록 설정** 하 여 컬렉션의 각 계산 노드에서 작업 일정을 사용 하지 않도록 설정 합니다.
*DisableComputeNodeSchedulingOptions* 매개 변수가 포함 되지 않았으므로 계산 노드에서 현재 실행 중인 작업은 다시 착신으로 설정 됩니다.

## 변수

### -BatchContext
이 cmdlet이 일괄 처리 서비스와 상호 작용 하는 데 사용 하는 **Batchaccountcontext** 인스턴스를 지정 합니다.
Get-AzBatchAccount cmdlet을 사용 하 여 BatchAccountContext를 가져오는 경우, 일괄 서비스와 상호 작용할 때 Azure Active Directory 인증이 사용 됩니다. 대신 공유 키 인증을 사용 하려면 Get-AzBatchAccountKey cmdlet을 사용 하 여 선택 키가 채워진 BatchAccountContext 개체를 가져옵니다. 공유 키 인증을 사용 하는 경우 기본 선택 키가 기본적으로 사용 됩니다. 사용할 키를 변경 하려면 BatchAccountContext 속성을 설정 합니다.

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
작업 일정을 사용할 수 없는 계산 노드에 대 한 개체 참조를 지정 합니다.
이 개체 참조는 Get-AzBatchComputeNode cmdlet을 사용 하 여 만들고 반환 된 계산 노드 개체를 변수에 저장 합니다.

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
Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.

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
이 cmdlet이 예약을 사용 하지 않도록 설정 된 컴퓨터 노드에서 현재 실행 중인 작업을 처리 하는 방법을 지정 합니다.
이 매개 변수에 허용 되는 값은 다음과 같습니다.
- Requeue.
작업이 즉시 중지 되 고 작업 큐에 반환 됩니다.
이렇게 하면 다른 계산 노드에서 작업의 일정을 재조정할 수 있습니다.
이 값이 기본값입니다. 
- 종료.
작업이 즉시 중지 되 고 작업 큐에서 제거 됩니다.
이러한 작업의 일정이 조정 되지 않습니다. 
- TaskCompletion.
계산 노드에서 작업 일정을 사용 하지 않도록 설정 하기 전에 현재 실행 중인 작업을 완료할 수 있습니다.
이 노드에는 새 작업이 예정 되어 있지 않습니다. 
- RetainedData.
현재 실행 중인 작업은 완료할 수 있으며 데이터 보존 기간은 계산 노드에서 작업 일정을 사용 하지 않도록 설정 하기 전에 만료 될 수 있습니다.
이 노드에는 새 작업이 예정 되어 있지 않습니다.

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
작업 일정을 사용할 수 없는 계산 노드의 ID를 지정 합니다.

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
작업 일정을 사용 하지 않도록 설정 된 계산 노드를 포함 하는 일괄 처리 풀의 ID를 지정 합니다.
*PoolId* 매개 변수를 사용 하는 경우 동일한 명령에서 *ComputeNode* 매개 변수를 사용 하지 마세요.

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
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.

## 입력

### Microsoft.Azure.Commands.Batch. PSComputeNode

### Microsoft.Azure.Commands.Batch.BatchAccountContext

## 출력

### 시스템. i a o

## 상속자

## 관련 링크

[Get-AzBatchAccountKey](./Get-AzBatchAccountKey.md)

[Enable-AzBatchComputeNodeScheduling](./Enable-AzBatchComputeNodeScheduling.md)


