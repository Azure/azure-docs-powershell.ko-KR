---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2Dataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2Dataset.md
gitcommit: https://github.com/Azure/azure-powershell/blob/c396953644d237789e0f4e1f726b553913186d34
ms.openlocfilehash: ec66f865c4a511935599b81b672cd60d6da78485
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93537339"
---
# Get-AzureRmDataFactoryV2Dataset

## SYNOPSIS
Data Factory의 데이터 집합에 대 한 정보를 가져옵니다.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 구문과

### ByFactoryName (기본값)
```
Get-AzureRmDataFactoryV2Dataset [[-Name] <String>] [-ResourceGroupName] <String> [-DataFactoryName] <String>
```

### ByFactoryObject
```
Get-AzureRmDataFactoryV2Dataset [[-Name] <String>] [-DataFactory] <PSDataFactory>
```

## 설명은
Get-AzureRmDataFactoryV2Dataset cmdlet은 Azure Data Factory의 데이터 집합에 대 한 정보를 가져옵니다.
데이터 집합의 이름을 지정 하는 경우이 cmdlet은 해당 데이터 집합에 대 한 정보를 가져옵니다.
이름을 지정 하지 않으면이 cmdlet은 data factory의 모든 데이터 집합에 대 한 정보를 가져옵니다.

## 예제의

### 예제 1: 모든 데이터 집합에 대 한 정보 가져오기
```
PS C:\> Get-AzureRmDataFactoryV2Dataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF"

    DatasetName       : DACuratedWikiData
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Structure         :
    Properties        : Microsoft.Azure.Management.DataFactory.Models.AzureBlobDataset

    DatasetName       : DAWikipediaClickEvents
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Structure         :
    Properties        : Microsoft.Azure.Management.DataFactory.Models.AzureBlobDataset

    DatasetName       : DAWikiAggregatedData
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Structure         :
    Properties        : Microsoft.Azure.Management.DataFactory.Models.AzureBlobDataset

```

이 명령은 WikiADF 이라는 data factory의 모든 데이터 집합에 대 한 정보를 가져옵니다.

### 예제 2: 특정 데이터 집합에 대 한 정보 가져오기
```
PS C:\> Get-AzureRmDataFactoryV2Dataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikipediaClickEvents"

    DatasetName       : DAWikipediaClickEvents
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Structure         :
    Properties        : Microsoft.Azure.Management.DataFactory.Models.AzureBlobDataset

```

이 명령은 WikiADF 이라는 data factory의 DAWikipediaClickEvents 이라는 데이터 집합에 대 한 정보를 가져옵니다.

## 변수

### -DataFactory
PSDataFactory 개체를 지정 합니다.
이 cmdlet은이 매개 변수에서 지정 하는 data factory에 속한 데이터 집합을 가져옵니다.


```yaml
Type: PSDataFactory
Parameter Sets: ByFactoryObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DataFactoryName
Data factory의 이름을 지정 합니다.
이 cmdlet은이 매개 변수에서 지정 하는 data factory에 속한 데이터 집합을 가져옵니다.

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

### -이름
정보를 가져올 데이터 집합의 이름을 지정 합니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: DatasetName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Azure 리소스 그룹의 이름을 지정 합니다.
이 cmdlet은이 매개 변수에서 지정 하는 그룹에 속하는 데이터 집합을 가져옵니다.

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

## 입력

### System. 문자열
Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory


## 출력

### Ataset ' 1 [[[Microsoft.Azure.Commands.DataFactoryV2.Models.PSD], Microsoft DataFactoryV2, Version = 0.1.9.0, Culture = 중립, PublicKeyToken = null])
Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset


## 상속자
키워드: azure, azurerm, arm, resource, 관리, manager, data, 팩토리

## 관련 링크
[Set-AzureRmDataFactoryV2Dataset]()

[제거-AzureRmDataFactoryV2Dataset]()
