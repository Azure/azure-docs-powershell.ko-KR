---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 352A4B94-E433-413B-91D1-6AA347563959
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/new-azdatafactorydataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryDataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryDataset.md
ms.openlocfilehash: 1d03ba1e4b025be933fd9cd409270d8deb93d1d1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93701144"
---
# New-AzDataFactoryDataset

## SYNOPSIS
Data Factory에서 데이터 집합을 만듭니다.

## 구문과

### ByFactoryName (기본값)
```
New-AzDataFactoryDataset [-DataFactoryName] <String> [[-Name] <String>] [-File] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ByFactoryObject
```
New-AzDataFactoryDataset [-DataFactory] <PSDataFactory> [[-Name] <String>] [-File] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 설명은
**AzDataFactoryDataset** Cmdlet은 Azure Data Factory에서 데이터 집합을 만듭니다.
이미 존재 하는 데이터 집합의 이름을 지정 하면이 cmdlet이 데이터 집합을 바꾸기 전에 확인을 요청 하는 메시지를 표시 합니다.
*Force* 매개 변수를 지정 하면 cmdlet은 확인 없이 기존 데이터 집합을 바꿉니다.
다음 순서 대로 이러한 작업을 수행 합니다. 
- Data factory를 만듭니다. 
- 연결 된 서비스를 만듭니다. 
- 데이터 집합을 만듭니다. 
- 파이프라인을 만듭니다.
데이터 팩터리에 동일한 이름을 가진 데이터 집합이 이미 있는 경우이 cmdlet은 기존 데이터 집합을 새 데이터 집합으로 덮어쓸지 여부를 확인 하는 메시지를 표시 합니다.
기존 데이터 집합을 덮어쓰려고 한다는 것을 확인 하면 데이터 집합 정의도 대체 됩니다.

## 예제의

### 예제 1: 데이터 집합 만들기
```
PS C:\>New-AzDataFactoryDataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikipediaClickEvents" -File "C:\\samples\\WikiSample\\DA_WikipediaClickEvents.json"
DatasetName         : DAWikipediaClickEvents
ResourceGroupName : ADF
DataFactoryName   : WikiADF
Availability      : Microsoft.DataFactories.Availability
Location          : Microsoft.DataFactories.AzureBlobLocation
Policy            : Microsoft.DataFactories.Policy
Structure         : {}
```

이 명령은 WikiADF 이라는 data factory에 DA_WikipediaClickEvents 이라는 데이터 집합을 만듭니다.
명령은 파일의 DAWikipediaClickEvents.js정보를 기준으로 데이터 집합을 기준으로 합니다.

### 예제 2: 새 데이터 집합의 사용 가능성 보기
```
PS C:\>$Dataset = New-AzDataFactoryDataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikipediaClickEvents" -File "C:\\samples\\WikiSample\\DA_WikipediaClickEvents.json"
PS C:\> $Dataset.Availability
AnchorDateTime : 
Frequency      : Hour
Interval       : 1
Offset         : 
WaitOnExternal : Microsoft.DataFactories.WaitOnExternal
```

첫 번째 명령은 이전 예제와 같이 DA_WikipediaClickEvents 라는 데이터 집합을 만든 다음 해당 데이터 집합을 $Dataset 변수에 할당 합니다.
두 번째 명령은 표준 점 표기법을 사용 하 여 데이터 집합의 Availability 속성에 대 한 세부 정보를 표시 합니다.

### 예제 3: 새 데이터 집합에 대 한 보기 위치
```
PS C:\>$Dataset = New-AzDataFactoryDataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikipediaClickEvents" -File "C:\\samples\\WikiSample\\DA_WikipediaClickEvents.json"
PS C:\> $Dataset.Location
BlobPath          : wikidatagateway/wikisampledatain/
FilenamePrefix    : 
Format            : 
LinkedServiceName : LinkedServiceWikipediaClickEvents
PartitionBy       : {}
```

첫 번째 명령은 이전 예제와 같이 DA_WikipediaClickEvents 라는 데이터 집합을 만든 다음 해당 데이터 집합을 $Dataset 변수에 할당 합니다.
두 번째 명령은 데이터 집합의 Location 속성에 대 한 세부 정보를 표시 합니다.

### 예제 4: 새 데이터 집합에 대 한 유효성 검사 규칙 보기
```
PS C:\>$Dataset = New-AzDataFactoryDataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikipediaClickEvents" -File "C:\\samples\\WikiSample\\DA_WikipediaClickEvents.json"
PS C:\> $Dataset.Policy.Validation | Format-List $dataset.Location
BlobPath          : wikidatagateway/wikisampledatain/
FilenamePrefix    : 
Format            : 
LinkedServiceName : LinkedServiceWikipediaClickEvents
PartitionBy       : {}

MinimumRows   : 
MinimumSizeMB : 1
```

첫 번째 명령은 이전 예제와 같이 DA_WikipediaClickEvents 라는 데이터 집합을 만든 다음 해당 데이터 집합을 $Dataset 변수에 할당 합니다.
두 번째 명령은 데이터 집합에 대 한 유효성 검사 규칙에 대 한 세부 정보를 가져온 다음 파이프라인 연산자를 사용 하 여 Format-List cmdlet에 전달 합니다.
해당 Windows PowerShell cmdlet이 결과 형식을 지정 합니다.
자세한 내용은을 입력 `Get-Help Format-List` 하세요.

## 변수

### -DataFactory
**PSDataFactory** 개체를 지정 합니다.
이 cmdlet은이 매개 변수에서 지정 하는 데이터 데이터 집합을 만듭니다.

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
이 cmdlet은이 매개 변수에서 지정 하는 데이터 데이터 집합을 만듭니다.

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

### -파일
데이터 집합에 대 한 설명을 포함 하는 JSON (JavaScript 개체 표기) 파일의 전체 경로를 지정 합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force
이 cmdlet이 기존 데이터 집합을 확인 메시지 없이 대체 함을 나타냅니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -이름
만들 데이터 집합의 이름을 지정 합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Azure 리소스 그룹의 이름을 지정 합니다.
이 cmdlet은이 매개 변수에서 지정 하는 그룹에 데이터 집합을 만듭니다.

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

### -확인
Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.
Cmdlet이 실행 되지 않습니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory

### System. 문자열

## 출력

### Microsoft.Azure.Commands.DataFactories.Models.PSDataset

## 상속자
* 키워드: azure, azurerm, arm, resource, 관리, manager, data, 팩토리

## 관련 링크

[Get-AzDataFactoryDataset](./Get-AzDataFactoryDataset.md)

[제거-AzDataFactoryDataset](./Remove-AzDataFactoryDataset.md)


