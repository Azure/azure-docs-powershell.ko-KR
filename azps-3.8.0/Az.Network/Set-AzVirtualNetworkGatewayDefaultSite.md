---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A27EE9C0-C7F5-4BF6-AE52-58087BD1B1C3
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azvirtualnetworkgatewaydefaultsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkGatewayDefaultSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkGatewayDefaultSite.md
ms.openlocfilehash: a4be0aed365517e1ae3ae11155f82ea097db309a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94034121"
---
# Set-AzVirtualNetworkGatewayDefaultSite

## SYNOPSIS
가상 네트워크 게이트웨이의 기본 사이트를 설정 합니다.

## 구문과

```
Set-AzVirtualNetworkGatewayDefaultSite -VirtualNetworkGateway <PSVirtualNetworkGateway>
 -GatewayDefaultSite <PSLocalNetworkGateway> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명은
**AzVirtualNetworkGatewayDefaultSite** cmdlet은 강제 터널링 기본 사이트를 가상 네트워크 게이트웨이에 할당 합니다.
강제 터널링은 Azure 가상 컴퓨터에서 온-프레미스 네트워크로 인터넷에 바인딩된 트래픽을 리디렉션할 수 있는 방법을 제공 합니다. 이렇게 하면 트래픽을 해제 하기 전에 검사 하 고 감사할 수 있습니다.
강제 터널링은 VPN (가상 사설망) 터널을 사용 하 여 수행 됩니다. 이 터널에는 모든 Azure 인터넷 바인딩 트래픽이 리디렉션되는 기본 사이트 (로컬 게이트웨이)가 필요 합니다.
**Set-AzVirtualNetworkGatewayDefaultSite** 는 게이트웨이에 할당 된 기본 사이트를 변경 하는 방법을 제공 합니다.

## 예제의

### 예제 1: 가상 네트워크 게이트웨이에 기본 사이트 할당
```
PS C:\>$LocalGateway = Get-AzLocalNetworkGateway -Name "ContosoLocalGateway " -ResourceGroup "ContosoResourceGroup"
PS C:\> $VirtualGateway = Get-AzVirtualNetworkGateway -Name "ContosoVirtualGateway"
PS C:\> Set-AzVirtualNetworkGatewayDefaultSite -GatewayDefaultSite $LocalGateway -VirtualNetworkGateway $VirtualGateway
```

이 예제에서는 ContosoVirtualGateway 이라는 가상 네트워크 게이트웨이에 기본 사이트를 할당 합니다.
첫 번째 명령은 ContosoLocalGateway 라는 로컬 게이트웨이에 대 한 개체 참조를 만듭니다.
$LocalGateway 라는 변수에 저장 된이 개체 참조는 기본 사이트로 구성 될 게이트웨이를 나타냅니다.
그런 다음 두 번째 명령은 가상 네트워크 게이트웨이에 대 한 개체 참조를 만들고 결과를 $VirtualGateway 라는 변수에 저장 합니다.
세 번째 명령은 **Set-AzVirtualNetworkGatewayDefaultSite** cmdlet을 사용 하 여 기본 사이트를 ContosoVirtualGateway에 할당 합니다.

## 변수

### -DefaultProfile
Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.

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

### -게이트웨이 Defaultsite
지정 된 가상 네트워크의 기본 사이트로 할당할 로컬 네트워크 게이트웨이에 대 한 개체 참조를 지정 합니다.
Get-AzLocalNetworkGateway cmdlet을 사용 하 여 로컬 게이트웨이에 대 한 개체 참조를 만들 수 있습니다.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VirtualNetworkGateway
기본 사이트가 할당 될 가상 네트워크 게이트웨이에 대 한 개체 참조를 지정 합니다.
**AzVirtualNetworkGateway** 를 사용 하 고 게이트웨이 이름을 지정 하 여 가상 네트워크 게이트웨이에 대 한 개체 참조를 만들 수 있습니다.
변수 $VirtualGateway는 *VirtualNetworkGateway* 매개 변수에 대 한 매개 변수 값으로 사용할 수 있습니다.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### PSVirtualNetworkGateway에 대 한.

### Microsoft. 네트워크. PSLocalNetworkGateway

## 출력

### PSVirtualNetworkGateway에 대 한.

## 상속자

## 관련 링크

[Get-AzLocalNetworkGateway](./Get-AzLocalNetworkGateway.md)

[Get-AzVirtualNetworkGateway](./Get-AzVirtualNetworkGateway.md)

[제거-AzVirtualNetworkGatewayDefaultSite](./Remove-AzVirtualNetworkGatewayDefaultSite.md)


