---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 7C8B47B4-2F6A-45EF-A351-88C8C3F9D0D3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermapplicationgateway
schema: 2.0.0
ms.openlocfilehash: 1b852be30b513963f5d311940162078bdf6f692a
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93882818"
---
# Set-AzureRmApplicationGateway

## SYNOPSIS
응용 프로그램 게이트웨이를 업데이트 합니다.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 구문과

```
Set-AzureRmApplicationGateway -ApplicationGateway <PSApplicationGateway> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명은
**AzureRmApplicationGateway** Cmdlet은 Azure application gateway를 업데이트 합니다.

## 예제의

### 예제 1: 응용 프로그램 게이트웨이 업데이트
```
PS C:\>$UpdatedAppGw = Set-AzureRmApplicationGateway -ApplicationGateway $AppGw
```

이 명령은 $AppGw 변수의 설정을 사용 하 여 응용 프로그램 게이트웨이를 업데이트 하 고 업데이트 된 게이트웨이를 $UpdatedAppGw 변수에 저장 합니다.

## 변수

### -ApplicationGateway
응용 프로그램 게이트웨이를 설정 해야 하는 상태를 나타내는 응용 프로그램 게이트웨이 개체를 지정 합니다.

```yaml
Type: PSApplicationGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -AsJob
백그라운드에서 cmdlet 실행

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

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### PSApplicationGateway
' ApplicationGateway ' 매개 변수는 파이프라인에서 ' PSApplicationGateway ' 형식의 값을 허용 합니다.

## 출력

### Microsoft. * PSApplicationGateway

## 상속자

## 관련 링크

[시작-AzureRmApplicationGateway](./Start-AzureRmApplicationGateway.md)


