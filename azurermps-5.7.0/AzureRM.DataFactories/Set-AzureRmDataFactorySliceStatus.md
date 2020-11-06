---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: 1D07222C-17D1-421C-8C9B-37043CBCF517
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/set-azurermdatafactoryslicestatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Set-AzureRmDataFactorySliceStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Set-AzureRmDataFactorySliceStatus.md
ms.openlocfilehash: 8e1d189173c9825876018351ef36a2b73f285a24
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526871"
---
# Set-AzureRmDataFactorySliceStatus

## SYNOPSIS
Azure Data Factory에서 데이터 집합의 슬라이스 상태를 설정 합니다.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 구문과

### ByFactoryName (기본값)
```
Set-AzureRmDataFactorySliceStatus [[-EndDateTime] <DateTime>] [-Status] <String> [[-UpdateType] <String>]
 [-DataFactoryName] <String> [-DatasetName] <String> [-StartDateTime] <DateTime> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByFactoryObject
```
Set-AzureRmDataFactorySliceStatus [[-EndDateTime] <DateTime>] [-Status] <String> [[-UpdateType] <String>]
 [-DataFactory] <PSDataFactory> [-DatasetName] <String> [-StartDateTime] <DateTime>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명은
**AzureRmDataFactorySliceStatus** Cmdlet은 Azure Data Factory에서 데이터 집합에 대 한 조각의 상태를 설정 합니다.

## 예제의

### 예제 1: 모든 조각의 상태 설정
```
PS C:\>Set-AzureRmDataFactorySliceStatus -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -DatasetName "DAWikiAggregatedData" -StartDateTime 2014-05-21T16:00:00Z -EndDateTime 2014-05-21T20:00:00Z -Status "Waiting" -UpdateType "UpstreamInPipeline"
True
```

이 명령은 DAWikiAggregatedData 이라는 데이터 집합에 대 한 모든 조각의 상태를 WikiADF 이라는 data factory에서 대기 하도록 설정 합니다.
*Updatetype* 매개 변수에는 UpstreamInPipeline 값이 있으므로이 명령은 데이터 집합 및 모든 종속 데이터 집합에 대 한 각 조각의 상태를 설정 합니다.
종속 데이터 집합은 파이프라인의 활동에 대 한 입력 데이터 집합으로 사용 됩니다.
이 명령은 $True 값을 반환 합니다.

## 변수

### -DataFactory
**PSDataFactory** 개체를 지정 합니다.
이 cmdlet은이 매개 변수에서 지정 하는 데이터 팩터리에 속하는 조각의 상태를 수정 합니다.

```yaml
Type: PSDataFactory
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
이 cmdlet은이 매개 변수에서 지정 하는 데이터 팩터리에 속하는 조각의 상태를 수정 합니다.

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DatasetName
이 cmdlet이 조각을 수정 하는 데이터 집합의 이름을 지정 합니다.

```yaml
Type: String
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
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EndDateTime
시간 기간의 끝 **날짜를 DateTime** 개체로 지정 합니다.
이 시간은 데이터 조각의 끝입니다.
**DateTime** 개체에 대 한 자세한 내용은를 입력 `Get-Help Get-Date` 합니다.

*Enddatetime* 은 다음 예제와 같이 ISO8601 형식으로 지정 해야 합니다. 

2015-01-01Z 2015-01-01T00:00:00Z 2015-01-01T00:00:00.000 Z (UTC) 2015-01-01T00:00:00-08:00 (태평양 표준시)

기본 표준 시간대 지정자는 UTC입니다.

```yaml
Type: DateTime
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
이 cmdlet은이 매개 변수에서 지정 하는 그룹에 속하는 조각의 상태를 수정 합니다.

```yaml
Type: String
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
이 시간은 데이터 조각의 시작 부분입니다.

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -상태
데이터 조각에 할당할 상태를 지정 합니다.
이 매개 변수에 허용 되는 값은 다음과 같습니다.

- 기다립니다.
데이터 조각이 처리 되기 전에 유효성 검사 정책에 대 한 유효성 검사를 기다리고 있습니다. 
- 수행할.
데이터 처리가 완료 되 고 데이터 조각이 준비 되었습니다.
- InProgress.
데이터 처리가 진행 중입니다. 
- 못함.
데이터 처리에 실패 했습니다.
- 건너뛰면.
데이터 조각 처리를 건너뛰었습니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Failed, InProgress, Ready, Skipped, Waiting

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UpdateType
조각에 대 한 업데이트 유형을 지정 합니다.
이 매개 변수에 허용 되는 값은 다음과 같습니다.

- 개별.
지정 된 시간 범위에서 데이터 집합에 대 한 각 조각의 상태를 설정 합니다. 
- UpstreamInPipeline입니다.
파이프라인의 활동에 대 한 입력 데이터 집합으로 사용 되는 데이터 집합 및 모든 종속 데이터 집합에 대 한 각 조각의 상태를 설정 합니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Individual, UpstreamInPipeline

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### 않아야
이 cmdlet은 입력을 허용 하지 않습니다.

## 출력

### 시스템 부울

## 상속자
* 키워드: azure, azurerm, arm, resource, 관리, manager, data, 팩토리

## 관련 링크

[Get-AzureRmDataFactorySlice](./Get-AzureRmDataFactorySlice.md)


