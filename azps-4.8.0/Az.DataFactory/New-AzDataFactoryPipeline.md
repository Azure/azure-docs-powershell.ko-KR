---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 30C1AF6C-A8DC-4CA0-9E5F-10641A29D0E8
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/new-azdatafactorypipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryPipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryPipeline.md
ms.openlocfilehash: e8917b9c68cb0708d34faa0e0dfec8e0e912f54b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94212844"
---
# New-AzDataFactoryPipeline

## SYNOPSIS
Data Factory에서 파이프라인을 만듭니다.

## 구문과

### ByFactoryName (기본값)
```
New-AzDataFactoryPipeline [[-Name] <String>] [-DataFactoryName] <String> [-File] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ByFactoryObject
```
New-AzDataFactoryPipeline [[-Name] <String>] [-DataFactory] <PSDataFactory> [-File] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 설명은
**AzDataFactoryPipeline** Cmdlet은 Azure Data Factory에서 파이프라인을 만듭니다.
이미 존재 하는 파이프라인의 이름을 지정 하는 경우 cmdlet에서 파이프라인을 바꾸기 전에 확인을 요청 하는 메시지가 표시 됩니다.
*Force* 매개 변수를 지정 하면 cmdlet이 확인 없이 기존 파이프라인을 바꿉니다.
다음 순서 대로 이러한 작업을 수행 합니다. 
- Data factory를 만듭니다. 
- 연결 된 서비스를 만듭니다. 
- 데이터 집합을 만듭니다. 
- 파이프라인을 만듭니다.
이름이 같은 파이프라인이 데이터 팩터리에 이미 있는 경우이 cmdlet은 기존 파이프라인을 새 파이프라인으로 덮어쓸지 여부를 확인 하는 메시지를 표시 합니다.
기존 파이프라인을 덮어쓰려고 한다는 것을 확인 한 경우 파이프라인 정의도 대체 됩니다.

## 예제의

### 예제 1: 파이프라인 만들기
```
PS C:\>New-AzDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF" -File "C:\DPWikisample.json" 
PipelineName      : DPWikisample
ResourceGroupName : ADF
DataFactoryName   : WikiADF11
Properties        : Microsoft.DataFactories.PipelineProperties
```

이 명령은 ADF 라는 data factory에 DPWikisample 이라는 파이프라인을 만듭니다.
명령은 파일의 DPWikisample.js정보에 파이프라인을 기반으로 합니다.
이 파일에는 파이프라인의 복사본 활동 및 HDInsight 활동과 같은 작업에 대 한 정보가 포함 되어 있습니다.

## 변수

### -DataFactory
**PSDataFactory** 개체를 지정 합니다.
이 cmdlet은이 매개 변수에서 지정 하는 데이터 팩터리의 파이프라인을 만듭니다.

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
이 cmdlet은이 매개 변수에서 지정 하는 데이터 팩터리의 파이프라인을 만듭니다.

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
파이프라인에 대 한 설명을 포함 하는 JSON (JavaScript 개체 표기) 파일의 전체 경로를 지정 합니다.

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
이 cmdlet이 확인을 묻지 않고 기존 파이프라인을 대체 함을 나타냅니다.

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
만들 파이프라인의 이름을 지정 합니다.

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
Azure 리소스 그룹의 이름을 지정 합니다.
이 cmdlet은이 매개 변수에서 지정 하는 그룹에 대 한 파이프라인을 만듭니다.

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
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### System. 문자열

### Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory

## 출력

### DataFactories. PSPipeline/.

## 상속자
* 키워드: azure, azurerm, arm, resource, 관리, manager, data, 팩토리

## 관련 링크

[Get-AzDataFactoryPipeline](./Get-AzDataFactoryPipeline.md)

[제거-AzDataFactoryPipeline](./Remove-AzDataFactoryPipeline.md)

[이력서-AzDataFactoryPipeline](./Resume-AzDataFactoryPipeline.md)

[Set-AzDataFactoryPipelineActivePeriod](./Set-AzDataFactoryPipelineActivePeriod.md)

[일시 중단-AzDataFactoryPipeline](./Suspend-AzDataFactoryPipeline.md)


