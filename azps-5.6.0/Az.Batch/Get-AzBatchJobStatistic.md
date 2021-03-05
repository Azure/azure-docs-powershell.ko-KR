---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: E655684D-9601-4A0B-BB09-EFB787EB2B1B
online version: https://docs.microsoft.com/powershell/module/az.batch/get-azbatchjobstatistic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchJobStatistic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchJobStatistic.md
ms.openlocfilehash: ec52f8b48433e52e86551a8346f4ec9a61b5727d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101987023"
---
# Get-AzBatchJobStatistic

## SYNOPSIS
Batch 계정에 대한 작업 요약 통계를 얻습니다.

## 구문

```
Get-AzBatchJobStatistic -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## 설명
**Get-AzBatchJobStatistic** cmdlet은 Azure Batch 계정의 모든 작업의 수명 요약 통계를 얻습니다.
통계는 계정 생성에서 통계의 마지막 업데이트 시간까지 계정에 있는 모든 작업에서 집계됩니다.

## 예제

### 예제 1: 모든 작업의 요약 통계를 얻습니다.
```
PS C:\>Get-AzBatchJobStatistic -BatchContext $Context
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

첫 번째 명령은 **Get-AzBatchAccountKey를 사용하여 ContosoBatchAccount라는** 일괄 처리 계정에 대한 계정 키에 대한 개체 참조를 만듭니다.
명령은 이 개체 참조를 $Context 저장합니다.
두 번째 명령은 모든 작업의 요약 통계를 얻습니다.
명령은 첫 $Context 값을 사용 합니다.

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

### CommonParameters
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## 입력

### Microsoft.Azure.Commands.Batch.BatchAccountContext

## 출력

### Microsoft.Azure.Commands.Bat. Models.PSJobStatistics

## 참고 사항

## 관련 링크

[Get-AzBatchAccountKey](./Get-AzBatchAccountKey.md)

[Get-AzBatchPoolStatistic](./Get-AzBatchPoolStatistic.md)

[Get-AzBatchPoolUsageMetrics](./Get-AzBatchPoolUsageMetric.md)
