---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 36EB9CE6-EAC9-471C-97D6-14E882E0F710
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/enable-azbatchcomputenodescheduling
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Enable-AzBatchComputeNodeScheduling.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Enable-AzBatchComputeNodeScheduling.md
ms.openlocfilehash: 9969388d51abb337030a8a732805ee1a15368ea7
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93878530"
---
# Enable-AzBatchComputeNodeScheduling

## SYNOPSIS
지정 된 계산 노드에서 작업 일정을 사용 하도록 설정 합니다.

## 구문과

### Id (기본값)
```
Enable-AzBatchComputeNodeScheduling [-PoolId] <String> [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### InputObject
```
Enable-AzBatchComputeNodeScheduling [[-ComputeNode] <PSComputeNode>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명은
AzBatchComputeNodeScheduling cmdlet을 **사용** 하면 지정 된 계산 노드에서 작업을 예약할 수 있습니다.
계산 노드는 특정 응용 프로그램 작업을 전담 하는 Azure 가상 컴퓨터입니다.

## 예제의

### 예제 1: 계산 노드에서 작업 일정 사용
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName "contosobatchaccount"
PS C:\> Enable-AzBatchComputeNodeScheduling  -PoolId "myPool" -Id "tvm-1783593343_34-20151117t222514z" -BatchContext $Context
```

이러한 명령은 계산 노드 tvm-1783593343_34-20151117t222514z에서 작업 일정을 사용 하도록 설정 합니다.
이렇게 하려면 예제의 첫 번째 명령은 batch 계정 contosobatchaccount의 계정 키를 포함 하는 개체 참조를 만듭니다.
이 개체 참조는 $context 라는 변수에 저장 됩니다.
그런 다음 두 번째 명령은이 개체 참조 및 **enable-AzBatchComputeNodeScheduling** cmdlet을 사용 하 여 tvm-1783593343_34-20151117t222514z에서 풀 myPool에 연결 하 고 작업 예약을 사용 하도록 설정 합니다.

### 예제 2: 풀의 계산 노드에서 작업 예약 사용
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName "contosobatchaccount"
PS C:\> Get-AzBatchComputeNode -PoolId "Pool06"  -BatchContext $Context | Enable-AzBatchComputeNodeScheduling  -BatchContext $Context
```

이러한 명령을 사용 하면 풀 Pool06에 있는 모든 계산 노드에서 작업을 예약할 수 있습니다.
이 작업을 수행 하기 위해 예제의 첫 번째 명령은 일괄 계정 contosobatchaccount의 계정 키를 포함 하는 개체 참조를 만듭니다.
이 개체 참조는 $context 라는 변수에 저장 됩니다.
그런 다음이 예제의 두 번째 명령은이 개체 참조를 사용 하 여 Pool06에 있는 모든 계산 노드의 컬렉션을 반환 합니다. **AzBatchComputeNode** .
그런 다음 컬렉션의 각 계산 노드에서 작업 일정을 예약할 수 있도록 하는 **AzBatchComputeNodeScheduling** cmdlet으로 해당 컬렉션을 파이프 합니다.

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
작업 일정을 사용할 수 있는 계산 노드에 대 한 개체 참조를 지정 합니다.
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

### -Id
작업 일정을 사용할 수 있는 계산 노드의 ID를 지정 합니다.

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
작업 일정을 사용할 수 있는 계산 노드를 포함 하는 일괄 처리 풀의 ID를 지정 합니다.

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

[Disable-AzBatchComputeNodeScheduling](./Disable-AzBatchComputeNodeScheduling.md)


