---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: C102232A-C9C8-4CEE-8535-7C7A70057B06
online version: https://docs.microsoft.com/powershell/module/az.datafactory/get-azdatafactoryslice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactorySlice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactorySlice.md
ms.openlocfilehash: 497899400c05697fb9b273a89743172b672e4892
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101975312"
---
# Get-AzDataFactorySlice

## SYNOPSIS
Azure Data Factory에서 데이터 세트에 대한 데이터 조각을 얻습니다.

## 구문

### ByFactoryName(기본값)
```
Get-AzDataFactorySlice [[-EndDateTime] <DateTime>] [-DataFactoryName] <String> [-DatasetName] <String>
 [-StartDateTime] <DateTime> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### ByFactoryObject
```
Get-AzDataFactorySlice [[-EndDateTime] <DateTime>] [-DataFactory] <PSDataFactory> [-DatasetName] <String>
 [-StartDateTime] <DateTime> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명
**Get-AzDataFactorySlice** cmdlet은 Azure Data Factory의 데이터 세트에 대한 데이터 조각을 얻습니다.
시작 시간 및 종료 시간을 지정하여 볼 데이터 조각 범위를 정의합니다.
데이터 조각의 상태는 다음 값 중 하나입니다. 
- pendingExecution.
데이터 처리가 시작되지 않습니다. 
- InProgress.
데이터 처리가 진행 중입니다. 
- 준비되었습니다.
데이터 처리가 완료되었습니다.
데이터 조각은 종속 조각을 사용할 준비가 됩니다. 
- 실패했습니다.
조각을 생성하는 실행이 실패했습니다. 
- 건너뛰기.
Data Factory는 조각의 처리를 건너뜁합니다. 
- 다시 시도합니다.
Data Factory는 조각을 생성하는 실행을 다시 검색합니다. 
- 시간 외입니다. 데이터 처리 시간이 지날 수 있습니다. 
- 보류 중인Validation입니다.
데이터 조각이 처리되기 전에 유효성 검사가 대기 중입니다. 
- 유효성 검사를 다시 시도합니다.
Data Factory는 조각의 유효성 검사를 다시 검색합니다. 
- 유효성 검사에 실패했습니다.
조각의 유효성 검사가 실패했습니다.
각 조각에 대해 Get-AzDataFactoryRun cmdlet을 사용하여 조각을 생성하는 실행에 대한 자세한 정보를 볼 수 있습니다.

## 예제

### 예제 1: 데이터 세트에 대한 데이터 조각을 얻습니다.
```powershell
PS C:\>Get-AzDataFactorySlice -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -DatasetName "DAWikiAggregatedData" -StartDateTime 2014-05-20T10:00:00Z
ResourceGroupName : ADF
DataFactoryName   : WikiADF
DatasetName         : DAWikiAggregatedData
Start             : 5/21/2014 1:00:00 AM
End               : 5/21/2014 2:00:00 AM
RetryCount        : 0
Status            : Ready

ResourceGroupName : ADF
DataFactoryName   : WikiADF
DatasetName         : DAWikiAggregatedData
Start             : 5/21/2014 2:00:00 AM
End               : 5/21/2014 3:00:00 AM
RetryCount        : 0
Status            : Ready

. . . 

ResourceGroupName : ADF
DataFactoryName   : WikiADF
DatasetName         : DAWikiAggregatedData
Start             : 5/21/2014 8:00:00 PM
End               : 5/21/2014 9:00:00 PM
RetryCount        : 0
Status            : PendingExecution

ResourceGroupName : ADF
DataFactoryName   : WikiADF
DatasetName         : DAWikiAggregatedData
Start             : 5/21/2014 9:00:00 PM
End               : 5/21/2014 10:00:00 PM
RetryCount        : 0
Status            : PendingExecution

. . .
```

이 명령은 WikiADF라는 데이터 팩터리에서 WikiAggregatedData라는 데이터 세트에 대한 모든 데이터 조각을 얻습니다.
명령은 StartDateTime 매개 변수가 지정한 시간 후에 생성되는 조각을 얻습니다.
다음 예제 코드는 JSON(JavaScript 개체 표기법) 파일의 매시간 이 데이터 세트에 대한 가용성을 설정합니다.
가용성: {period: "Hour", periodMultiplier: 1 } 결과 중 일부는 준비되어 있으며 다른 결과는 pendingExecution입니다.
준비된 조각이 이미 실행되었습니다.
보류 중인 조각은 cmdlet에서 지정하는 간격으로 각 시간의 Set-AzDataFactoryPipelineActivePeriod 기다리고 있습니다.
이 예제에서는 파이프라인 및 조각에 대한 시작 및 종료 기간 모두 1일(24시간)의 값이 있습니다.

### 예제 2

Azure Data Factory에서 데이터 세트에 대한 데이터 조각을 얻습니다. (자동 재생)

```powershell <!-- Aladdin Generated Example --> 
Get-AzDataFactorySlice -DataFactoryName 'WikiADF' -DatasetName 'DAWikiAggregatedData' -EndDateTime 2014-05-22T16:00:00Z -ResourceGroupName 'ADF' -StartDateTime 2014-05-20T10:00:00Z
```

## 매개 변수

### -DataFactory
**PSDataFactory 개체를 지정합니다.**
이 cmdlet은 이 매개 변수가 지정하는 데이터 팩터리에 속하는 조각을 얻습니다.

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
이 cmdlet은 이 매개 변수가 지정하는 데이터 팩터리에 속하는 조각을 얻습니다.

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
이 cmdlet에서 조각을 얻을 데이터 세트의 이름을 지정합니다.

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

### -EndDateTime
기간의 끝을 **DateTime 개체로 지정합니다.**
이 cmdlet은 이 매개 변수가 지정하기 전에 생성되는 조각을 얻습니다.
**DateTime** 개체에 대한 자세한 내용은 `Get-Help Get-Date` 를 입력합니다.
*EndDateTime은* 2015-01-01Z 2015-01-00:00Z 2015-01-01-0과 같이 ISO8601 형식으로 지정해야 합니다. 1T00:00:00.000Z(UTC) 2015-01-01T00:00:00-08:00(태평양 표준시) 기본 표준 시간대 지정자는 UTC입니다.

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Azure 리소스 그룹의 이름을 지정합니다.
이 cmdlet은 이 매개 변수가 지정하는 그룹에 속하는 조각을 얻습니다.

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
이 cmdlet은 이 매개 변수가 지정한 시간 후에 생성되는 조각을 얻습니다.

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
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.

## 입력

### Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory

### System.String

## 출력

### Microsoft.Azure.Commands.DataFactories.Models.PSDataSlice

## 참고 사항
* 키워드: azure, azurerm, arm, 리소스, 관리, 관리자, 데이터, 팩터리

## 관련 링크

[Set-AzDataFactorySliceStatus](./Set-AzDataFactorySliceStatus.md)

[Get-AzDataFactoryRun](./Get-AzDataFactoryRun.md)

[Set-AzDataFactoryPipelineActivePeriod](./Set-AzDataFactoryPipelineActivePeriod.md)


