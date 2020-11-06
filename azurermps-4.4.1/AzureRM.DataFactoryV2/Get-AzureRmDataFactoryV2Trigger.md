---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2Trigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2Trigger.md
gitcommit: https://github.com/Azure/azure-powershell/blob/c396953644d237789e0f4e1f726b553913186d34
ms.openlocfilehash: bc60bbb5b48c4022e7db6a95e26a1f43ef891ae2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93537319"
---
# Get-AzureRmDataFactoryV2Trigger

## SYNOPSIS
Data factory의 트리거에 대 한 정보를 가져옵니다.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 구문과

### ByFactoryName (기본값)
```
Get-AzureRmDataFactoryV2Trigger [[-Name] <String>] [-ResourceGroupName] <String> [-DataFactoryName] <String>
```

### ByFactoryObject
```
Get-AzureRmDataFactoryV2Trigger [[-Name] <String>] [-DataFactory] <PSDataFactory>
```

## 설명은
**AzureRmDataFactoryV2Trigger** cmdlet은 data factory의 트리거에 대 한 정보를 가져옵니다. 트리거의 이름을 지정 하는 경우 cmdlet은 해당 트리거에 대 한 정보를 가져옵니다. 이름을 지정 하지 않으면 cmdlet은 data factory의 모든 트리거에 대 한 정보를 가져옵니다.


## 예제의

### 예제 1: 특정 트리거에 대 한 정보 가져오기
```
PS C:\> Get-AzureRmDataFactoryV2Trigger -ResourceGroupName "ADF" -DataFactoryName "WikiADF"

    TriggerName       : ScheduledTrigger
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Properties        : Microsoft.Azure.Management.DataFactory.Models.ScheduleTrigger
    RuntimeState      : Stopped

    TriggerName       : ScheduledTrigger2
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Properties        : Microsoft.Azure.Management.DataFactory.Models.ScheduleTrigger
    RuntimeState      : Stopped
```

Data factory "WikiADF"에서 생성 된 모든 트리거의 목록을 가져옵니다.

### 예제 2: 모든 트리거에 대 한 정보 가져오기

```
Get-AzureRmDataFactoryV2Trigger -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -TriggerName "ScheduledTrigger"

    TriggerName       : ScheduledTrigger
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Properties        : Microsoft.Azure.Management.DataFactory.Models.ScheduleTrigger
    RuntimeState      : Stopped
```

"WikiADF" 데이터 팩터리에 "ScheduledTrigger" 라는 단일 트리거를 가져옵니다.

## 변수

### -DataFactory
Data factory 개체입니다.

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
Data factory 이름입니다.

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
트리거 이름입니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: TriggerName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
리소스 그룹 이름입니다.

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

### DataFactoryV2 ' 1 [[Microsoft Azure. PSTrigger, Microsoft Azure. DataFactoryV2, Version = 0.1.9.0, Culture = 중립, PublicKeyToken = null]] 목록입니다.
DataFactoryV2. PSTrigger/.


## 상속자

## 관련 링크
[Set-AzureRmDataFactoryV2Trigger]()

[시작-AzureRmDataFactoryV2Trigger]()

[중지-AzureRmDataFactoryV2Trigger]()

[제거-AzureRmDataFactoryV2Trigger]()
