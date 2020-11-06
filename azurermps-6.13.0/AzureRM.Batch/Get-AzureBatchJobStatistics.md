---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: E655684D-9601-4A0B-BB09-EFB787EB2B1B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/get-azurebatchjobstatistics
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchJobStatistics.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchJobStatistics.md
ms.openlocfilehash: 0a43f98a926da76f2127589477e8c9f771a032cc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93524591"
---
# Get-AzureBatchJobStatistics

## SYNOPSIS
일괄 처리 계정에 대 한 작업 요약 통계를 가져옵니다.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 구문과

```
Get-AzureBatchJobStatistics -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## 설명은
**Get-AzureBatchJobStatistics** Cmdlet은 Azure Batch 계정의 모든 작업에 대 한 수명 요약 통계를 가져옵니다.
통계는 계정 만들기부터 통계의 마지막 업데이트 시간까지 계정에 있던 모든 작업에 대해 집계 됩니다.

## 예제의

### 예제 1: 모든 작업에 대 한 요약 통계 가져오기
```
PS C:\>Get-AzureBatchJobStatistics -BatchContext $Context
FailedTaskCount    : 330
KernelCpuTime      : 00:24:31.8440000
LastUpdateTime     : 5/16/2016 6:00:00 PM
ReadIOGiB          : 38.1271341182292
ReadIOps           : 26546054
StartTime          : 11/3/2015 9:47:14 PM
SucceededTaskCount : 766
TaskRetryCount     : 0
Url                : https://accountname.westus.batch.azure.com/lifetimejobstats
UserCpuTime        : 20:55:50.3200000
WaitTime           : 03:54:49.8530000
WallClockTime      : 20:55:50.3200000
WriteIOGiB         : 0.159623090177774
WriteIOps          : 146946
```

첫 번째 명령은 **Get-AzureRmBatchAccountKeys** 를 사용 하 여 ContosoBatchAccount 라는 일괄 계정에 대 한 계정 키에 대 한 개체 참조를 만듭니다.
명령이이 개체 참조를 $Context 변수에 저장 합니다.
두 번째 명령은 모든 작업에 대 한 요약 통계를 가져옵니다.
명령에서 첫 번째 명령의 $Context 값을 사용 합니다.

## 변수

### -BatchContext
이 cmdlet이 일괄 처리 서비스와 상호 작용 하는 데 사용 하는 **Batchaccountcontext** 인스턴스를 지정 합니다.
Get-AzureRmBatchAccount cmdlet을 사용 하 여 BatchAccountContext를 가져오는 경우, 일괄 서비스와 상호 작용할 때 Azure Active Directory 인증이 사용 됩니다. 대신 공유 키 인증을 사용 하려면 Get-AzureRmBatchAccountKeys cmdlet을 사용 하 여 선택 키가 채워진 BatchAccountContext 개체를 가져옵니다. 공유 키 인증을 사용 하는 경우 기본 선택 키가 기본적으로 사용 됩니다. 사용할 키를 변경 하려면 BatchAccountContext 속성을 설정 합니다.

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

### -DefaultProfile
Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### Microsoft.Azure.Commands.Batch.BatchAccountContext
매개 변수: BatchContext (ByValue)

## 출력

### Microsoft.Azure.Commands.Batch. PSJobStatistics

## 상속자

## 관련 링크

[Get-AzureRmBatchAccountKeys](./Get-AzureRmBatchAccountKeys.md)

[Get-AzureBatchPoolStatistics](./Get-AzureBatchPoolStatistics.md)

[Get-AzureBatchPoolUsageMetrics](./Get-AzureBatchPoolUsageMetrics.md)


