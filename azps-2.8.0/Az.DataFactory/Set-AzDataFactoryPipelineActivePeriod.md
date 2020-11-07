---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: D853A91F-95E7-4C36-AC0F-2C10DFCF68F8
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/set-azdatafactorypipelineactiveperiod
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryPipelineActivePeriod.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryPipelineActivePeriod.md
ms.openlocfilehash: edb2e94900d383675bd183c09df16e295828aae1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93696980"
---
# Set-AzDataFactoryPipelineActivePeriod

## SYNOPSIS
데이터 조각에 대 한 활성 기간을 구성 합니다.

## 구문과

### ByFactoryName (기본값)
```
Set-AzDataFactoryPipelineActivePeriod [-PipelineName] <String> [-DataFactoryName] <String>
 [-StartDateTime] <DateTime> [[-EndDateTime] <DateTime>] [-AutoResolve] [-ForceRecalculate]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ByFactoryObject
```
Set-AzDataFactoryPipelineActivePeriod [-PipelineName] <String> [-DataFactory] <PSDataFactory>
 [-StartDateTime] <DateTime> [[-EndDateTime] <DateTime>] [-AutoResolve] [-ForceRecalculate]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 설명은
**AzDataFactoryPipelineActivePeriod** Cmdlet은 Azure data Factory의 파이프라인이 처리 하는 데이터 조각의 활성 기간을 구성 합니다.
Set-AzDataFactorySliceStatus cmdlet을 사용 하 여 데이터 집합의 슬라이스 상태를 수정 하는 경우 조각의 시작 시간 및 종료 시간이 파이프라인의 활성 기간에 있는지 확인 합니다.
파이프라인을 만든 후 데이터 처리가 발생 하는 기간을 지정할 수 있습니다.
파이프라인의 활성 기간을 지정 하면 데이터 조각이 각 데이터 팩토리 데이터 집합에 대해 정의 된 **가용성** 속성에 따라 처리 되는 기간을 정의 합니다.

## 예제의

### 예제 1: 활성 기간 구성
```
PS C:\>Set-AzDataFactoryPipelineActivePeriod -ResourceGroupName "ADF" -PipelineName "DPWikisample" -DataFactoryName "WikiADF" -StartDateTime 2014-05-21T16:00:00Z -EndDateTime 2014-05-22T16:00:00Z
Confirm
Are you sure you want to set pipeline 'DPWikisample' active period from '05/21/2014 16:00:00' to
'05/22/2014 16:00:00'? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
True
```

이 명령은 DPWikisample 이라는 파이프라인이 처리 하는 데이터 조각에 대 한 활성 기간을 구성 합니다.
명령은 데이터 조각의 시작 지점과 끝 지점을 값으로 제공 합니다.
이 명령은 $True 값을 반환 합니다.

## 변수

### -자동 해결
이 cmdlet이 자동 해결을 사용 함을 나타냅니다.

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

### -DataFactory
**PSDataFactory** 개체를 지정 합니다.
이 cmdlet은이 매개 변수에서 지정 하는 데이터 팩터리에 속한 파이프라인의 활성 기간을 수정 합니다.

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
이 cmdlet은이 매개 변수에서 지정 하는 데이터 팩터리에 속한 파이프라인의 활성 기간을 수정 합니다.

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

### -EndDateTime
시간 기간의 끝 **날짜를 DateTime** 개체로 지정 합니다.
데이터 처리가 발생 하거나이 기간 내에 데이터 조각이 처리 됩니다.
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

### -ForceRecalculate
이 cmdlet이 강제 다시 계산을 사용 함을 나타냅니다.

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

### -PipelineName
파이프라인의 이름을 지정 합니다.
이 cmdlet은이 매개 변수에서 지정 하는 파이프라인의 활성 기간을 설정 합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Azure 리소스 그룹의 이름을 지정 합니다.
이 cmdlet은이 매개 변수에서 지정 하는 그룹에 속하는 파이프라인의 활성 기간을 수정 합니다.

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
데이터 처리가 발생 하거나이 기간 내에 데이터 조각이 처리 됩니다.
*StartDateTime* 는 ISO8601 형식으로 지정 해야 합니다.

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

### System. 문자열

### Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory

## 출력

### 시스템 부울

## 상속자
* 키워드: azure, azurerm, arm, resource, 관리, manager, data, 팩토리

## 관련 링크

[새로운 AzDataFactoryPipeline](./New-AzDataFactoryPipeline.md)

[Set-AzDataFactorySliceStatus](./Set-AzDataFactorySliceStatus.md)


