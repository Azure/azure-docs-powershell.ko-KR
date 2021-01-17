---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 352A4B94-E433-413B-91D1-6AA347563959
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/new-azdatafactorydataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryDataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryDataset.md
ms.openlocfilehash: 38af817205f8d80615fa94799eee5a7a54f05e78
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98326521"
---
# New-AzDataFactoryDataset

## SYNOPSIS
Data Factory에서 데이터 세트를 만듭니다.

## 구문

### ByFactoryName(기본값)
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

## 설명
**New-AzDataFactoryDataset** cmdlet은 Azure Data Factory에서 데이터 세트를 만듭니다.
이미 존재하는 데이터 세트의 이름을 지정하는 경우 이 cmdlet은 데이터 세트를 바꾸기 전에 확인하라는 메시지를 표시합니다.
Force 매개 *변수를 지정하면* cmdlet이 확인 없이 기존 데이터 세트를 대체합니다.
다음 순서로 이러한 작업을 수행할 수 있습니다. 
- 데이터 팩터리 만들기 
- 연결된 서비스를 만들 수 있습니다. 
- 데이터 세트를 만들 수 있습니다. 
- 파이프라인을 만들 수 있습니다.
동일한 이름의 데이터 세트가 데이터 팩터리에 이미 있는 경우 이 cmdlet은 기존 데이터 세트를 새 데이터 세트로 덮어써야 하는지 여부를 확인하라는 메시지를 제공합니다.
기존 데이터 세트를 덮어들이는 것이 확인되면 데이터 세트 정의도 대체됩니다.

## 예제

### 예제 1: 데이터 세트 만들기
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

이 명령은 WikiADF라는 DA_WikipediaClickEvents 팩터리에 이름의 데이터 세트를 만듭니다.
이 명령은 데이터 세트를 on 파일의 DAWikipediaClickEvents.js기반입니다.

### 예제 2: 새 데이터 세트의 가용성 보기
```
PS C:\>$Dataset = New-AzDataFactoryDataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikipediaClickEvents" -File "C:\\samples\\WikiSample\\DA_WikipediaClickEvents.json"
PS C:\> $Dataset.Availability
AnchorDateTime : 
Frequency      : Hour
Interval       : 1
Offset         : 
WaitOnExternal : Microsoft.DataFactories.WaitOnExternal
```

첫 번째 명령은 이전 예제와 DA_WikipediaClickEvents 이름의 데이터 세트를 만든 다음 해당 데이터 세트를 $Dataset 할당합니다.
두 번째 명령은 표준 점 표시를 사용하여 데이터 세트의 가용성 속성에 대한 세부 정보를 표시합니다.

### 예제 3: 새 데이터 세트의 위치 보기
```
PS C:\>$Dataset = New-AzDataFactoryDataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikipediaClickEvents" -File "C:\\samples\\WikiSample\\DA_WikipediaClickEvents.json"
PS C:\> $Dataset.Location
BlobPath          : wikidatagateway/wikisampledatain/
FilenamePrefix    : 
Format            : 
LinkedServiceName : LinkedServiceWikipediaClickEvents
PartitionBy       : {}
```

첫 번째 명령은 이전 예제와 DA_WikipediaClickEvents 이름의 데이터 세트를 만든 다음 해당 데이터 세트를 $Dataset 할당합니다.
두 번째 명령은 데이터 세트의 Location 속성에 대한 세부 정보를 표시합니다.

### 예제 4: 새 데이터 세트에 대한 유효성 검사 규칙 보기
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

첫 번째 명령은 이전 예제와 DA_WikipediaClickEvents 이름의 데이터 세트를 만든 다음 해당 데이터 세트를 $Dataset 할당합니다.
두 번째 명령은 데이터 세트에 대한 유효성 검사 규칙에 대한 세부 정보를 확인한 다음, 파이프라인 연산자를 사용하여 Format-List cmdlet에 전달합니다.
이 Windows PowerShell 형식을 지정합니다.
자세한 내용은 `Get-Help Format-List` .를 입력합니다.

## PARAMETERS

### -DataFactory
**PSDataFactory 개체를 지정합니다.**
이 cmdlet은 데이터 팩터리에서 이 매개 변수가 지정하는 데이터 세트를 만듭니다.

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
이 cmdlet은 데이터 팩터리에서 이 매개 변수가 지정하는 데이터 세트를 만듭니다.

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

### -File
데이터 세트에 대한 설명이 포함된 JSON(JavaScript Object Notation) 파일의 전체 경로를 지정합니다.

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
확인 메시지를 표시하지 않고 이 cmdlet이 기존 데이터 세트를 대체하는지 나타냅니다.

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

### -Name
만들 데이터 세트의 이름을 지정합니다.

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
Azure 리소스 그룹의 이름을 지정합니다.
이 cmdlet은 이 매개 변수가 지정하는 그룹에 데이터 세트를 만듭니다.

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

### -Confirm
cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.

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
cmdlet이 실행되는 경우의 결과 표시
cmdlet이 실행되지 않습니다.

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
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.

## 입력

### Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory

### System.String

## 출력

### Microsoft.Azure.Commands.DataFactories.Models.PSDataset

## 참고 사항
* 키워드: azure, azurerm, arm, 리소스, 관리, 관리자, 데이터, 팩터리

## 관련 링크

[Get-AzDataFactoryDataset](./Get-AzDataFactoryDataset.md)

[Remove-AzDataFactoryDataset](./Remove-AzDataFactoryDataset.md)


