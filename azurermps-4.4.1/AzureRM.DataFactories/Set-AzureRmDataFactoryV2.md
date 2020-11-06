---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2.md
ms.openlocfilehash: b5e5d42ba114da87daa3fa3effb15d3ad8bab22c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525519"
---
# Set-AzureRmDataFactoryV2

## SYNOPSIS
Data factory를 만듭니다.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 구문과

```
Set-AzureRmDataFactoryV2 [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-Tag] <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## 설명은
**AzureRmDataFactoryV2** cmdlet은 지정 된 리소스 그룹 이름 및 위치를 사용 하 여 데이터 팩터리를 만듭니다.

다음 순서 대로 이러한 작업을 수행 합니다.

        -- Create a data factory.
        -- Create linked services.
        -- Create datasets.
        -- Create a pipeline.

## 예제의

### 예제 1: data factory 만들기
```
PS C:\> Set-AzureRmDataFactoryV2 -ResourceGroupName "ADF" -Name "WikiADF" -Location "WestUS"

    DataFactoryName   : WikiADF
    DataFactoryId     : /subscriptions/3e8e61b5-9a7d-4952-bfae-545ab997b9ea/resourceGroups/adf/providers/Microsoft.DataFactory/factories/wikiadf
    ResourceGroupName : ADF
    Location          : EastUS
    Tags              : {}
    Identity          : Microsoft.Azure.Management.DataFactory.Models.FactoryIdentity
    ProvisioningState : Succeeded
```

이 명령은 WestUS 위치에서 ADF 라는 리소스 그룹에 WikiADF 이라는 data factory를 만듭니다.

## 변수

### -확인
Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force
확인 메시지를 표시 하지 않고 cmdlet을 실행 합니다.

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

### -위치
이 지역에 데이터 팩터리가 생성 됩니다.

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

### -이름
Data factory 이름입니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DataFactoryName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
리소스 그룹 이름입니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### 태그
Data factory의 태그입니다.

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -WhatIf
Cmdlet이 실행 되지만 cmdlet을 실행 하지 않는 경우의 결과를 보여 줍니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### System. 문자열
System.webserver. 컬렉션 테이블

## 출력

### Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory

## 상속자
키워드: azure, azurerm, arm, resource, 관리, manager, data, 팩토리

## 관련 링크

[Get-AzureRmDataFactoryV2]()

[제거-AzureRmDataFactoryV2]()
