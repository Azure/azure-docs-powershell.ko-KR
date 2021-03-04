---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 5224BDF5-D492-4160-893E-4BB5F76C22F3
online version: https://docs.microsoft.com/powershell/module/az.datafactory/get-azdatafactorypipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryPipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryPipeline.md
ms.openlocfilehash: 5db024152a01fdab8233e388da5ae176849f4b7d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101975408"
---
# Get-AzDataFactoryPipeline

## SYNOPSIS
Azure Data Factory에서 파이프라인에 대한 정보를 얻습니다.

## 구문

### ByFactoryName(기본값)
```
Get-AzDataFactoryPipeline [[-Name] <String>] [-DataFactoryName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByFactoryObject
```
Get-AzDataFactoryPipeline [[-Name] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명
**Get-AzDataFactoryPipeline** cmdlet은 Azure Data Factory의 파이프라인에 대한 정보를 얻습니다.
파이프라인의 이름을 지정하는 경우 이 cmdlet은 해당 파이프라인에 대한 정보를 얻습니다.
이름을 지정하지 않으면 이 cmdlet은 데이터 팩터리의 모든 파이프라인에 대한 정보를 제공합니다.

## 예제

### 예제 1: 모든 파이프라인에 대한 정보 보기
```
PS C:\>Get-AzDataFactoryPipeline -ResourceGroupName "ADF" -DataFactoryName "WikiADF"
```

이 명령은 WikiADF라는 데이터 팩터리의 모든 파이프라인에 대한 정보를 얻습니다.
다음 예제 명령 중 하나를 사용할 수 있습니다.
두 번째 개체는 **DataFactory 개체를** 매개 변수로 사용합니다.

### 예제 2: 특정 파이프라인에 대한 정보 보기
```
PS C:\>Get-AzDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF" | Format-List
PipelineName      : DPWikisample
ResourceGroupName : ADF
DataFactoryName   : WikiADF
Properties        : Microsoft.DataFactories.PipelineProperties
```

이 명령은 WikiADF라는 데이터 팩터리에서 DPWikisample이라는 파이프라인에 대한 정보를 얻습니다.
명령은 파이프라인 연산자를 사용하여 해당 Format-List cmdlet에 전달합니다.
이 cmdlet은 결과를 서식 지정합니다.
자세한 내용은 `Get-Help Format-List` 를 입력합니다.

### 예제 3: 특정 파이프라인에 대한 속성 얻기
```
PS C:\> (Get-AzDataFactoryPipeline -ResourceGroupName "ADF" -Name DPWikisample -DataFactoryName "WikiADF").Properties
Activities  : {WikiHiveActivity, BlobToSqlCopyActivity}
Description : DP Wikipedia Sample Pipelines
End         : 6/6/2014 8:00:00 AM
IsPaused    : 
RuntimeInfo : Microsoft.DataFactories.PipelineRuntimeInfo
Start       : 6/5/2014 8:00:00 PM
```

이 명령은 WikiADF라는 데이터 팩터리에서 DPWikisample이라는 파이프라인에 대한 정보를 얻은 다음 표준 점표를 사용하여 해당 파이프라인과 연결된 **속성** 속성을 볼 수 있습니다.

### 예제 4: 특정 파이프라인에 대한 활동 보기
```
PS C:\>(Get-AzDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF").Properties.Activities
Transformation    : Microsoft.DataFactories.HDInsightActivityProperties
Description       : 
Inputs            : {DAWikipediaClickEvents}
LinkedServiceName : HDILinkedService
Name              : WikiHiveActivity
Outputs           : {DACuratedWikiData}
Policy            : Microsoft.DataFactories.ActivityPolicy

Transformation    : Microsoft.DataFactories.CopyActivityProperties
Description       : 
Inputs            : {DACuratedWikiData}
LinkedServiceName : HDILinkedService
Name              : BlobToSqlCopyActivity
Outputs           : {DAWikiAggregatedData}
Policy            : Microsoft.DataFactories.ActivityPolicy
```

이 명령은 WikiADF라는 데이터 팩터리에서 DPWikisample이라는 파이프라인에 대한 정보를 얻은 다음, 표준 점표를 사용하여 해당 파이프라인과 연결된 **활동** 속성을 볼 수 있습니다.

### 예제 5: 특정 파이프라인에 대한 런타임 정보 보기
```
PS C:\>(Get-AzDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF").Properties.RuntimeInfo
DeploymentTime
--------------
6/5/2014 10:36:46 PM
```

이 명령은 WikiADF라는 데이터 팩터리에서 DPWikisample이라는 파이프라인에 대한 정보를 얻은 다음 표준 점표를 사용하여 해당 파이프라인과 연결된 **RuntimeInfo** 속성을 볼 수 있습니다.

### 예제 6: 첫 번째 활동에 대한 입력에 대한 정보 얻습니다.
```
PS C:\>(Get-AzDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF11").Properties.Activities[0].Inputs | Format-List
EndTime   : 
Length    : 
Name      : DAWikipediaClickEvents
StartTime :
```

이 명령은 WikiADF라는 데이터 팩터리에서 DPWikisample이라는 파이프라인에 대한 정보를 얻은 다음, 표준 점표를 사용하여 해당 파이프라인과 연결된 **활동** 속성을 볼 수 있습니다.
명령은 **서식** 목록 을 사용하여 활동  배열의 첫 번째 요소의 **Inputs 속성을 표시합니다.**

## 매개 변수

### -DataFactory
**PSDataFactory 개체를 지정합니다.**
이 cmdlet은 이 매개 변수가 지정하는 데이터 팩터리에 속하는 파이프라인을 제공합니다.

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
이 cmdlet은 이 매개 변수가 지정하는 데이터 팩터리에 속하는 파이프라인을 제공합니다.

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

### -Name
정보를 얻을 파이프라인의 이름을 지정합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Azure 리소스 그룹의 이름을 지정합니다.
이 cmdlet은 이 매개 변수가 지정하는 그룹에 속하는 파이프라인을 제공합니다.

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

### CommonParameters
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.

## 입력

### System.String

### Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory

## 출력

### Microsoft.Azure.Commands.DataFactories.Models.PSPipeline

## 참고 사항
* 키워드: azure, azurerm, arm, 리소스, 관리, 관리자, 데이터, 팩터리

## 관련 링크

[New-AzDataFactoryPipeline](./New-AzDataFactoryPipeline.md)

[Remove-AzDataFactoryPipeline](./Remove-AzDataFactoryPipeline.md)

[Resume-AzDataFactoryPipeline](./Resume-AzDataFactoryPipeline.md)

[Set-AzDataFactoryPipelineActivePeriod](./Set-AzDataFactoryPipelineActivePeriod.md)

[suspend-AzDataFactoryPipeline](./Suspend-AzDataFactoryPipeline.md)


