---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 443F6492-EFA7-4417-943A-3A8D47F8C83C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/reset-azurermvirtualnetworkgateway
schema: 2.0.0
ms.openlocfilehash: f4039fb8a616a474a858728b6e222537c2d75c66
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93882838"
---
# Reset-AzureRmVirtualNetworkGateway

## SYNOPSIS

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 구문과

```
Reset-AzureRmVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewayVip <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명은

## 예제의

### raid-1
```

```

## 변수

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

### -게이트웨이 Vip
특정 게이트웨이 인스턴스를 다시 설정 하기 위한 게이트웨이 vip (예: Active-Active 기능을 사용할 수 있는 게이트웨이를 사용 하는 경우) 값이 전달 되지 않으면 기본적으로 게이트웨이 기본 인스턴스가 다시 설정 됩니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -VirtualNetworkGateway
```yaml
Type: PSVirtualNetworkGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### 이름
'. H i m ' 매개 변수는 파이프라인에서 ' String ' 형식의 값을 받습니다.

### PSVirtualNetworkGateway
' VirtualNetworkGateway ' 매개 변수는 파이프라인에서 ' PSVirtualNetworkGateway ' 형식의 값을 허용 합니다.

## 출력

### PSVirtualNetworkGateway에 대 한.

## 상속자

## 관련 링크

[Get-AzureRmVirtualNetworkGateway](./Get-AzureRmVirtualNetworkGateway.md)

[새로운 AzureRmVirtualNetworkGateway](./New-AzureRmVirtualNetworkGateway.md)

[제거-AzureRmVirtualNetworkGateway](./Remove-AzureRmVirtualNetworkGateway.md)

[크기 조정-AzureRmVirtualNetworkGateway](./Resize-AzureRmVirtualNetworkGateway.md)

[Set-AzureRmVirtualNetworkGateway](./Set-AzureRmVirtualNetworkGateway.md)


