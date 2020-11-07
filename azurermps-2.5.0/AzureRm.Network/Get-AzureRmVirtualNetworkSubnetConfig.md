---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 7688CE56-0A25-4409-9676-BF1B67C3F05F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvirtualnetworksubnetconfig
schema: 2.0.0
ms.openlocfilehash: ceb009dba1984f69e7da3e04a9ae57a9da14c067
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93882913"
---
# Get-AzureRmVirtualNetworkSubnetConfig

## SYNOPSIS
가상 네트워크의 서브넷을 가져옵니다.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 구문과

```
Get-AzureRmVirtualNetworkSubnetConfig [-Name <String>] -VirtualNetwork <PSVirtualNetwork>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명은
**AzureRmVirtualNetworkSubnetConfig** Cmdlet은 Azure 가상 네트워크에서 하나 이상의 서브넷 구성을 가져옵니다.

## 예제의

### 1: 가상 네트워크에서 서브넷 가져오기
```
New-AzureRmResourceGroup -Name TestResourceGroup -Location centralus
    $frontendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet 
    -AddressPrefix "10.0.1.0/24"
    $virtualNetwork = New-AzureRmVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName 
    TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet
    Get-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet -VirtualNetwork $virtualNetwork
```

이 예제에서는 리소스 그룹과 해당 리소스 그룹에 단일 서브넷이 있는 가상 네트워크를 만듭니다. 그런 다음 해당 서브넷에 대 한 데이터를 검색 합니다.

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

### -이름
이 cmdlet이 가져오는 서브넷 구성의 이름을 지정 합니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VirtualNetwork
이 cmdlet이 가져오는 서브넷 구성을 포함 하는 **VirtualNetwork** 개체를 지정 합니다.

```yaml
Type: PSVirtualNetwork
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

### PSVirtualNetwork
' VirtualNetwork ' 매개 변수는 파이프라인에서 ' PSVirtualNetwork ' 형식의 값을 허용 합니다.

## 출력

### Microsoft. 네트워크 모델. PSSubnet

## 상속자

## 관련 링크

[추가-AzureRmVirtualNetworkSubnetConfig](./Add-AzureRmVirtualNetworkSubnetConfig.md)

[새로운 AzureRmVirtualNetworkSubnetConfig](./New-AzureRmVirtualNetworkSubnetConfig.md)

[제거-AzureRmVirtualNetworkSubnetConfig](./Remove-AzureRmVirtualNetworkSubnetConfig.md)

[Set-AzureRmVirtualNetworkSubnetConfig](./Set-AzureRmVirtualNetworkSubnetConfig.md)


