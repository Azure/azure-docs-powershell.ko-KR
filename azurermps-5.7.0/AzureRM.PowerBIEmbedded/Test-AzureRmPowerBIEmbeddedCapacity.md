---
external help file: Microsoft.Azure.Commands.PowerBI.dll-Help.xml
Module Name: AzureRM.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.powerbiembedded/test-azurermpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/Test-AzureRmPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/Test-AzureRmPowerBIEmbeddedCapacity.md
ms.openlocfilehash: 8f6e161ad9ae2078da15dda659f1aea13929eec9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525044"
---
# Test-AzureRmPowerBIEmbeddedCapacity

## SYNOPSIS
PowerBI 포함 용량의 인스턴스가 있는지 테스트 합니다.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 구문과

```
Test-AzureRmPowerBIEmbeddedCapacity 
    [-Name] <String> 
    [<CommonParameters>]
```

## 설명은
Test-AzureRmPowerBIEmbeddedCapacity cmdlet은 PowerBI 포함 용량의 인스턴스가 있는지 테스트 합니다.

## 예제의

### 예제 1
```
PS C:\> Test-AzureRmPowerBIEmbeddedCapacity -Name "testcapacity"
True
```

이 명령은 testcapacity 라는 용량이 있는지 테스트 합니다.

## 변수

### -이름
PowerBI 포함 용량의 이름입니다.

```yaml
Type: String
Aliases: 

Required: True
Position: 0
Default value: None
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### 않아야
이 cmdlet은 입력을 허용 하지 않습니다.

## 출력

### 시스템 부울

## 상속자

## 관련 링크

[Get-AzureRmPowerBIEmbeddedCapacity](./Get-AzureRmPowerBIEmbeddedCapacity.md)

[제거-AzureRmPowerBIEmbeddedCapacity](./Remove-AzureRmPowerBIEmbeddedCapacity.md)
