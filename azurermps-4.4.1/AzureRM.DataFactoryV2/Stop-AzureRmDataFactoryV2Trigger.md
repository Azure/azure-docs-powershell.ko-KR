---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Stop-AzureRmDataFactoryV2Trigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Stop-AzureRmDataFactoryV2Trigger.md
gitcommit: https://github.com/Azure/azure-powershell/blob/db8032a9100d47fd3aa4248c7807d8e0bb538e83
ms.openlocfilehash: 3054824876ccaff24f319ae14c704cd975e79434
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93703774"
---
# Stop-AzureRmDataFactoryV2Trigger

## SYNOPSIS

데이터 팩터리에 트리거를 중지 합니다.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 구문과

### ByFactoryName (기본값)
```
Stop-AzureRmDataFactoryV2Trigger [-Name] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Force] [-WhatIf] [-Confirm]
```

### ByInputObject
```
Stop-AzureRmDataFactoryV2Trigger [-InputObject] <PSTrigger> [-Force] [-WhatIf] [-Confirm]
```

### ByResourceId
```
Stop-AzureRmDataFactoryV2Trigger [-ResourceId] <String> [-Force] [-WhatIf] [-Confirm]
```

## 설명은

**AzureRmDataFactoryV2Trigger** cmdlet은 데이터 팩터리에 트리거를 중지 합니다. 트리거가 ' 시작 됨 ' 상태인 경우 cmdlet은 트리거를 중지 하 고 더 이상 파이프라인을 호출 하지 않습니다. 트리거가 이미 ' 중지 됨 ' 상태인 경우에는이 cmdlet이 적용 되지 않습니다. Force 매개 변수를 지정 하면 cmdlet은 트리거를 중지 하기 전에 메시지를 표시 하지 않습니다.


## 예제의

### 예제 1: 트리거 중지

```
Stop-AzureRmDataFactoryV2Trigger -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -TriggerName "ScheduledTrigger"

Confirm
Are you sure you want to stop trigger 'ScheduledTrigger' in data factory 'TestFactory'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
True
```

Data factory "WikiADF"에서 "ScheduledTrigger" 이라는 트리거를 중지 합니다.


## 변수

### -확인
Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
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

### -Force
확인 메시지를 표시 하지 않고 cmdlet을 실행 합니다.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -이름
트리거 이름입니다.

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: TriggerName

Required: True
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

### -ResourceId
Azure 리소스 ID입니다.

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -InputObject
시작할 트리거 개체.

```yaml
Type: PSTrigger
Parameter Sets: ByInputObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -WhatIf
Cmdlet이 실행 되지만 cmdlet을 실행 하지 않는 경우의 결과를 보여 줍니다.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## 입력

### System. 문자열
DataFactoryV2. PSTrigger/.


## 출력

### DataFactoryV2 ' 1 [[Microsoft Azure. PSTrigger, Microsoft Azure. DataFactoryV2, Version = 0.1.9.0, Culture = 중립, PublicKeyToken = null]] 목록입니다.
DataFactoryV2. PSTrigger/.


## 상속자

## 관련 링크
[Get-AzureRmDataFactoryV2Trigger]()

[Set-AzureRmDataFactoryV2Trigger]()

[시작-AzureRmDataFactoryV2Trigger]()

[제거-AzureRmDataFactoryV2Trigger]()