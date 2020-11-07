---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 3702701E-428D-47E2-A227-0F38B055F881
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmusage
schema: 2.0.0
ms.openlocfilehash: 210c66f91836b40c719d91907fc78bd907d0fe86
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93883162"
---
# Get-AzureRmVMUsage

## SYNOPSIS
위치에 대 한 가상 컴퓨터 코어 수 사용량을 가져옵니다.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 구문과

```
Get-AzureRmVMUsage [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명은
**AzureRmVMUsage** cmdlet은 위치에 대 한 가상 컴퓨터 코어 수 사용량을 가져옵니다.

## 예제의

### 예제 1: 위치에 대 한 코어 카운트 사용 가져오기
```
PS C:\> Get-AzureRmVMUsage -Location "Central US"
```

이 명령은 위치 중앙 미국에 대 한 가상 컴퓨터 코어 수 사용량을 가져옵니다.

## 변수

### -DefaultProfile
Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -위치
이 cmdlet이 가상 컴퓨터 코어 수 사용량을 가져오는 위치를 지정 합니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### 않아야
이 cmdlet은 입력을 허용 하지 않습니다.

## 출력

### Microsoft. *. m a i. PSUsage

## 상속자

## 관련 링크

[Get-AzureRmVM](./Get-AzureRmVM.md)


