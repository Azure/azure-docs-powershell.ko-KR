---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 7100B5F0-A07B-4305-BF80-1F52647A03AB
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryrun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryRun.md
ms.openlocfilehash: f04f2d2d96dd0b293850ca3150568eb015ab5bbb
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98354513"
---
# Get-AzDataFactoryRun

## SYNOPSIS
Azure Data Factory에서 데이터 세트의 데이터 조각에 대해 실행됩니다.

## 구문

### ByFactoryName(기본값)
```
Get-AzDataFactoryRun [-DataFactoryName] <String> [-DatasetName] <String> [-StartDateTime] <DateTime>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByFactoryObject
```
Get-AzDataFactoryRun [-DataFactory] <PSDataFactory> [-DatasetName] <String> [-StartDateTime] <DateTime>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명
**Get-AzDataFactoryRun** cmdlet은 Azure Data Factory에서 데이터 세트의 데이터 조각에 대한 실행을 얻습니다.
데이터 팩터리의 데이터 세트는 시간 축에 대한 조각으로 구성됩니다.
조각의 너비는 시간별 또는 매일 일정에 따라 결정됩니다.
실행은 조각에 대한 처리 단위입니다.
재시도의 경우 또는 실패로 인해 조각을 다시 실행하는 경우 조각에 대해 하나 이상의 실행이 있을 수 있습니다.
조각은 시작 시간으로 식별됩니다.
조각의 시작 시간을 얻습니다. Get-AzDataFactorySlice cmdlet을 사용 합니다.
예를 들어 다음 조각에 대한 실행을 얻습니다. 시작 시간 2015-04-02T20:00:00을 사용 합니다.
ResourceGroupName : ADF DataFactoryName : SPDataFactory0924 DatasetName : MarketingCampaignEffectivenessBlobDataset Start : 5/2/2 014 8:00:00 PM 종료: 2014/5/3 오후 8:00:00 PM RetryCount : 0 상태 : Ready LatencyStatus:

## 예제

### 예제 1: 데이터 세트 얻기
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

이 명령은 2014년 5월 21일 오후 4시 GMT에서 시작하는 WikiADF라는 데이터 팩터리에서 DAWikiAggregatedData라는 데이터 세트의 조각에 대한 모든 실행을 얻습니다.

## PARAMETERS

### -DataFactory
**PSDataFactory 개체를 지정합니다.**
이 cmdlet은 이 매개 변수가 지정하는 데이터 팩터리에 속하는 조각에 대해 실행됩니다.

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
데이터 팩터리의 이름을 지정합니다.
이 cmdlet은 이 매개 변수가 지정하는 데이터 팩터리에 속하는 조각에 대해 실행됩니다.

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
데이터 세트의 이름을 지정합니다.
이 cmdlet은 이 매개 변수가 지정하는 데이터 세트에 속하는 조각에 대해 실행됩니다.

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
Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독

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
Azure 리소스 그룹의 이름을 지정합니다.
이 cmdlet은 이 매개 변수가 지정하는 그룹에 속한 조각에 대해 팩터리 실행을 얻습니다.

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
기간의 시작을 **DateTime 개체로 지정합니다.**
이 cmdlet은 이 기간과 일치하는 데이터 조각에 대해 실행됩니다.
*StartDateTime은* 다음 예제와 같이 ISO8601 형식으로 지정해야 합니다. 2015-01-01Z 2015-01-01T00:00:00Z 2015-01-00 1T00:00:00.000Z(UTC) 2015-01-01T00:00:00-08:00(태평양 표준시) 기본 표준 시간대 지정자는 UTC입니다.

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
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.

## 입력

### Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory

### System.String

## 출력

### Microsoft.Azure.Commands.DataFactories.Models.PSDataSliceRun

## 참고 사항
* 키워드: azure, azurerm, arm, 리소스, 관리, 관리자, 데이터, 팩터리

## 관련 링크

[Get-AzDataFactorySlice](./Get-AzDataFactorySlice.md)


