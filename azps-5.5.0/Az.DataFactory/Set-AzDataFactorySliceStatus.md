---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 1D07222C-17D1-421C-8C9B-37043CBCF517
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/set-azdatafactoryslicestatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactorySliceStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactorySliceStatus.md
ms.openlocfilehash: 8b2c55a069463120b861f1ea928ac0163a4c37df
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100208704"
---
# Set-AzDataFactorySliceStatus

## SYNOPSIS
Azure Data Factory에서 데이터 세트에 대한 조각의 상태를 설정합니다.

## 구문

### ByFactoryName(기본값)
```
Set-AzDataFactorySliceStatus [[-EndDateTime] <DateTime>] [-Status] <String> [[-UpdateType] <String>]
 [-DataFactoryName] <String> [-DatasetName] <String> [-StartDateTime] <DateTime> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByFactoryObject
```
Set-AzDataFactorySliceStatus [[-EndDateTime] <DateTime>] [-Status] <String> [[-UpdateType] <String>]
 [-DataFactory] <PSDataFactory> [-DatasetName] <String> [-StartDateTime] <DateTime>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명
**Set-AzDataFactorySliceStatus** cmdlet은 Azure Data Factory의 데이터 세트에 대한 조각의 상태를 설정합니다.

## 예제

### 예제 1: 모든 조각의 상태 설정
```
PS C:\>Set-AzDataFactorySliceStatus -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -DatasetName "DAWikiAggregatedData" -StartDateTime 2014-05-21T16:00:00Z -EndDateTime 2014-05-21T20:00:00Z -Status "Waiting" -UpdateType "UpstreamInPipeline"
True
```

이 명령은 DAWikiAggregatedData라는 데이터 세트에 대한 모든 조각의 상태를 WikiADF라는 데이터 팩터리에서 Waiting으로 설정합니다.
*UpdateType* 매개 변수의 값은 UpstreamInPipeline이기 때문에 명령은 데이터 세트 및 모든 종속 데이터 세트에 대한 각 조각의 상태를 설정합니다.
종속 데이터 세트는 파이프라인의 활동에 대한 입력 데이터 세트로 사용됩니다.
이 명령은 $True.

## PARAMETERS

### -DataFactory
**PSDataFactory 개체를 지정합니다.**
이 cmdlet은 이 매개 변수가 지정하는 데이터 팩터리에 속하는 조각의 상태를 수정합니다.

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
이 cmdlet은 이 매개 변수가 지정하는 데이터 팩터리에 속하는 조각의 상태를 수정합니다.

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
이 cmdlet이 조각을 수정하는 데이터 세트의 이름을 지정합니다.

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

### -EndDateTime
기간의 끝을 **DateTime 개체로 지정합니다.**
이 시간은 데이터 조각의 끝입니다.
**DateTime** 개체에 대한 자세한 내용은 .를 입력합니다. `Get-Help Get-Date`
*EndDateTime은* 다음 예제와 같이 ISO8601 형식으로 지정해야 합니다. 2015-01-01Z 2015-01-01T00:00:00Z 2015-01-0 1T00:00:00.000Z(UTC) 2015-01-01T00:00:00-08:00(태평양 표준시) 기본 표준 시간대 지정자는 UTC입니다.

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
이 cmdlet은 이 매개 변수가 지정하는 그룹에 속하는 조각의 상태를 수정합니다.

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
이번은 데이터 조각의 시작입니다.

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

### -Status
데이터 조각에 할당할 상태를 지정합니다.
이 매개 변수에 허용되는 값은
- 대기 중입니다.
데이터 조각이 처리되기 전에 유효성 검사 정책에 대한 유효성 검사를 기다리고 있습니다. 
- 준비되었습니다.
데이터 처리가 완료되어 데이터 조각이 준비되었습니다.
- InProgress.
데이터 처리가 진행 중입니다. 
- 실패했습니다.
데이터 처리에 실패했습니다.
- 건너뜁니다.
데이터 조각 처리를 건너뜁니다.

```yaml
Type: System.String
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
조각에 대한 업데이트 유형을 지정합니다.
이 매개 변수에 허용되는 값은
- 개인.
지정된 시간 범위의 데이터 세트에 대한 각 조각의 상태를 설정합니다. 
- UpstreamInPipeline.
파이프라인의 활동에 대한 입력 데이터 세트로 사용되는 데이터 세트 및 모든 종속 데이터 세트에 대한 각 조각의 상태를 설정합니다.

```yaml
Type: System.String
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
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.

## 입력

### Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory

### System.String

## 출력

### System.Boolean

## 참고 사항
* 키워드: azure, azurerm, arm, 리소스, 관리, 관리자, 데이터, 팩터리

## 관련 링크

[Get-AzDataFactorySlice](./Get-AzDataFactorySlice.md)


