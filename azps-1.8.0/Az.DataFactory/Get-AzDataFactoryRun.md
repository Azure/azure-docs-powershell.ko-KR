---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 7100B5F0-A07B-4305-BF80-1F52647A03AB
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryrun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryRun.md
ms.openlocfilehash: b3524f0886c5c433c6ec36d907126e6ca04828de
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93868773"
---
# Get-AzDataFactoryRun

## SYNOPSIS
Azure Data Factory에서 dataset의 데이터 조각에 대 한 실행을 가져옵니다.

## 구문과

### ByFactoryName (기본값)
```
Get-AzDataFactoryRun [-DataFactoryName] <String> [-DatasetName] <String> [-StartDateTime] <DateTime>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByFactoryObject
```
Get-AzDataFactoryRun [-DataFactory] <PSDataFactory> [-DatasetName] <String> [-StartDateTime] <DateTime>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명은
**AzDataFactoryRun** Cmdlet은 Azure data Factory에서 dataset의 데이터 조각에 대 한 실행을 가져옵니다.
Data factory의 데이터 집합은 시간 축을 기준으로 분할 영역으로 구성 됩니다.
조각의 너비는 일정에 따라 매시간 또는 일 수 있습니다.
실행은 조각의 처리 단위입니다.
다시 시도 하는 경우 또는 오류가 발생 하 여 조각을 실행 하는 경우 조각에 대해 하나 이상의 실행이 있을 수 있습니다.
조각은 시작 시간으로 식별 됩니다.
조각의 시작 시간을 얻으려면 Get-AzDataFactorySlice cmdlet을 사용 합니다.
예를 들어 다음 조각의 실행을 가져오려면 시작 시간 2015-04-02 T20:00:00을 사용 합니다.
ResourceGroupName: ADF DataFactoryName: SPDataFactory0924 DatasetName: MarketingCampaignEffectivenessBlobDataset 시작: 5/2/2014 8:00:00 PM 끝: 5/3/2014 8:00:00 PM RetryCount: 0 상태: 준비 LatencyStatus:

## 예제의

### 예제 1: 데이터 집합 가져오기
```
PS C:\>Get-AzDataFactoryRun -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -DatasetName "DAWikiAggregatedData" -StartDateTime 2014-05-21T16:00:00Z
Id                  : a7c4913c-9623-49b3-ae1e-3e45e2b68819
ResourceGroupName   : ADF
DataFactoryName     : WikiADF
DatasetName           : DAWikiAggregatedData
PipelineName        : 249ea141-ca00-8597-fad9-a148e5e7bdba
ActivityId          : fcefe2bd-39b1-2d7a-7b35-bcc2b0432300
ResumptionToken     : a7c4913c-9623-49b3-ae1e-3e45e2b68819
ContinuationToken   : 
ProcessingStartTime : 5/21/2014 5:02:41 PM
ProcessingEndTime   : 5/21/2014 5:04:12 PM
PercentComplete     : 100
DataSliceStart      : 5/21/2014 4:00:00 PM
DataSliceEnd        : 5/21/2014 5:00:00 PM
Status              : Succeeded
Timestamp           : 5/21/2014 5:02:41 PM
RetryAttempt        : 0
Properties          : {[errors, ]} 
ErrorMessage        :
```

이 명령은 05/21/2014의 오후 4 시 GMT에서 시작 하는 WikiADF 라는 data factory의 DAWikiAggregatedData 이라는 데이터 집합의 조각에 대 한 모든 실행을 가져옵니다.

## 변수

### -DataFactory
**PSDataFactory** 개체를 지정 합니다.
이 cmdlet은이 매개 변수에서 지정 하는 데이터 팩터리에 속한 슬라이스에 대해 실행 됩니다.

```yaml
Type: Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DataFactoryName
Data factory의 이름을 지정 합니다.
이 cmdlet은이 매개 변수에서 지정 하는 데이터 팩터리에 속한 슬라이스에 대해 실행 됩니다.

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DatasetName
데이터 집합의 이름을 지정 합니다.
이 cmdlet은이 매개 변수에서 지정 하는 데이터 집합에 속하는 슬라이스에 대해 실행 됩니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

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

### -ResourceGroupName
Azure 리소스 그룹의 이름을 지정 합니다.
이 cmdlet은이 매개 변수에서 지정 하는 그룹에 속하는 슬라이스에 대 한 팩토리 실행을 가져옵니다.

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StartDateTime
시간 기간의 시작 **날짜를 DateTime** 개체로 지정 합니다.
이 cmdlet은이 기간에 일치 하는 데이터 조각에 대해 실행 됩니다.
*StartDateTime* 는 다음 예제와 같이 ISO8601 형식으로 지정 해야 합니다. 2015-01-01z 2015-01-01T00:00:00z 2015-01-01t00:00:00.000 z (UTC) 2015-01-01T00:00:00-08:00 (태평양 표준시) 기본 시간대 지정자는 UTC입니다.

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory

### System. 문자열

## 출력

### Microsoft.Azure.Commands.DataFactories.Models.PSDataSliceRun

## 상속자
* 키워드: azure, azurerm, arm, resource, 관리, manager, data, 팩토리

## 관련 링크

[Get-AzDataFactorySlice](./Get-AzDataFactorySlice.md)


