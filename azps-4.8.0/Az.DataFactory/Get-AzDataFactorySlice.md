---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: C102232A-C9C8-4CEE-8535-7C7A70057B06
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryslice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactorySlice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactorySlice.md
ms.openlocfilehash: a71ccc37fe1c6b6811b955c5d84353dfecd66c2f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94212334"
---
# Get-AzDataFactorySlice

## SYNOPSIS
Azure Data Factory에서 dataset에 대 한 데이터 조각을 가져옵니다.

## 구문과

### ByFactoryName (기본값)
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

## 설명은
**AzDataFactorySlice** Cmdlet은 Azure data Factory에서 dataset에 대 한 데이터 조각을 가져옵니다.
시작 시간 및 종료 시간을 지정 하 여 표시할 데이터 조각의 범위를 정의 합니다.
데이터 조각의 상태는 다음 값 중 하나입니다. 
- PendingExecution.
데이터 처리가 시작 되지 않았습니다. 
- InProgress.
데이터 처리가 진행 중입니다. 
- 수행할.
데이터 처리가 완료 되었습니다.
데이터 조각이 종속 슬라이스에 사용할 준비가 되었습니다. 
- 못함.
조각을 생성 하는 실행에 실패 했습니다. 
- [.
데이터 팩토리는 조각의 처리를 건너뜁니다. 
- 재시도.
데이터 팩토리는 조각을 생성 하는 실행을 다시 시도 합니다. 
- 시간이 초과 되었습니다. 데이터 처리 시간이 초과 되었습니다. 
- PendingValidation.
데이터 조각이 처리 되기 전에 유효성 검사를 기다리고 있습니다. 
- 유효성 검사를 다시 시도 합니다.
데이터 팩토리는 조각의 유효성 검사를 다시 시도 합니다. 
- 유효성 검사에 실패 했습니다.
조각의 유효성 검사에 실패 했습니다.
각 조각에 대해 Get-AzDataFactoryRun cmdlet을 사용 하 여 조각을 생성 하는 실행에 대 한 자세한 정보를 확인할 수 있습니다.

## 예제의

### 예제 1: 데이터 집합에 대 한 데이터 조각 가져오기
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

이 명령은 WikiADF 이라는 data factory의 WikiAggregatedData 이라는 데이터 집합에 대 한 모든 데이터 조각을 가져옵니다.
명령은 StartDateTime 매개 변수에서 지정 된 시간 후에 생성 되는 슬라이스를 가져옵니다.
다음 예제 코드에서는 JSON (JavaScript 개체 표기) 파일에서 각 시간에 대해이 데이터 집합의 가용성을 설정 합니다.
가용성: {period: "시간", periodMultiplier: 1} 일부 결과가 준비 되었고 다른 일부는 PendingExecution.
준비 된 슬라이스가 이미 실행 되었습니다.
보류 중인 슬라이스가 Set-AzDataFactoryPipelineActivePeriod cmdlet에서 지정 하는 간격으로 각 시간 끝에 실행 되기를 기다리고 있습니다.
이 예제에서는 파이프라인의 시작 및 종료 기간과 두 조각의 값이 모두 1 일 (24 시간)입니다.

### 예제 2

Azure Data Factory에서 dataset에 대 한 데이터 조각을 가져옵니다. 생성

```powershell <!-- Aladdin Generated Example --> 
Get-AzDataFactorySlice -DataFactoryName 'WikiADF' -DatasetName 'DAWikiAggregatedData' -EndDateTime 2014-05-22T16:00:00Z -ResourceGroupName 'ADF' -StartDateTime 2014-05-20T10:00:00Z
```

## 변수

### -DataFactory
**PSDataFactory** 개체를 지정 합니다.
이 cmdlet은이 매개 변수에서 지정 하는 데이터 팩터리에 속하는 슬라이스를 가져옵니다.

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
이 cmdlet은이 매개 변수에서 지정 하는 데이터 팩터리에 속하는 슬라이스를 가져옵니다.

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
이 cmdlet이 조각을 가져오는 데이터 집합의 이름을 지정 합니다.

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

### -EndDateTime
시간 기간의 끝 **날짜를 DateTime** 개체로 지정 합니다.
이 cmdlet은이 매개 변수에서 지정 하는 시간 전에 생성 된 슬라이스를 가져옵니다.
**DateTime** 개체에 대 한 자세한 내용은를 입력 `Get-Help Get-Date` 합니다.
*Enddatetime* 은 다음 예제와 같이 ISO8601 형식으로 지정 해야 합니다. 2015-01-01z 2015-01-01T00:00:00z 2015-01-01t00:00:00.000 z (UTC) 2015-01-01T00:00:00-08:00 (태평양 표준시) 기본 시간대 지정자는 UTC입니다.

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
Azure 리소스 그룹의 이름을 지정 합니다.
이 cmdlet은이 매개 변수에서 지정 하는 그룹에 속하는 슬라이스를 가져옵니다.

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
이 cmdlet은이 매개 변수에서 지정 된 시간 후에 생성 되는 슬라이스를 가져옵니다.

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
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory

### System. 문자열

## 출력

### Microsoft.Azure.Commands.DataFactories.Models.PSDataSlice

## 상속자
* 키워드: azure, azurerm, arm, resource, 관리, manager, data, 팩토리

## 관련 링크

[Set-AzDataFactorySliceStatus](./Set-AzDataFactorySliceStatus.md)

[Get-AzDataFactoryRun](./Get-AzDataFactoryRun.md)

[Set-AzDataFactoryPipelineActivePeriod](./Set-AzDataFactoryPipelineActivePeriod.md)


