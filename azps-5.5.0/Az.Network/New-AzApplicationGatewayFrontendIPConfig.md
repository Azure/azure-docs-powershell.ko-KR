---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: AE8E26F2-CF8E-4340-936D-230731B5BA32
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFrontendIPConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFrontendIPConfig.md
ms.openlocfilehash: c1c2f9fc3cbe528687f0a276c1b5feed3bbdb4b9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100206853"
---
# New-AzApplicationGatewayFrontendIPConfig

## SYNOPSIS
애플리케이션 게이트웨이에 대한 프런트 엔드 IP 구성을 만듭니다.

## 구문

### SetByResourceId
```
New-AzApplicationGatewayFrontendIPConfig -Name <String> [-PrivateIPAddress <String>] [-SubnetId <String>]
 [-PublicIPAddressId <String>] [-PrivateLinkConfigurationId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### SetByResource
```
New-AzApplicationGatewayFrontendIPConfig -Name <String> [-PrivateIPAddress <String>] [-Subnet <PSSubnet>]
 [-PublicIPAddress <PSPublicIpAddress>]
 [-PrivateLinkConfiguration <PSApplicationGatewayPrivateLinkConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명
**New-AzApplicationGatewayFrontendIPConfig** cmdlet은 Azure 애플리케이션 게이트웨이에 대한 프런트 엔드 IP 구성을 만듭니다.
애플리케이션 게이트웨이는 두 가지 유형의 프런트 엔드 IP 구성을 지원합니다. 
- 공용 IP 주소 - ILB(내부 부하 분산)를 사용하는 개인 IP 주소입니다.
 애플리케이션 게이트웨이에는 공용 IP 주소와 개인 IP 주소가 하나씩 있습니다.
공용 IP 주소 및 개인 IP 주소는 프런트 엔드 IP 주소로 별도로 추가해야 합니다.

## 예제

### 예제 1: 공용 IP 리소스 개체를 사용하여 프런트 엔드 IP 구성 만들기
```
PS C:\>$PublicIP = New-AzPublicIpAddress -ResourceGroupName "ResourceGroup01" -Name "PublicIP01" -location "West US" -AllocationMethod Dynamic
PS C:\> $FrontEnd = New-AzApplicationGatewayFrontendIPConfig -Name "FrontEndIP01" -PublicIPAddress $PublicIP
```

첫 번째 명령은 공용 IP 리소스 개체를 만들고 공용 ip 리소스 $PublicIP 저장합니다.
두 번째 명령은 $PublicIP FrontEndIP01이라는 새 프런트 엔드 IP 구성을 만들고 $FrontEnd 변수에 저장합니다.

### 예제 2: 정적 개인 IP를 프런트 엔드 IP 주소로 만들기
```
PS C:\>$VNet = Get-AzVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet
PS C:\> $FrontEnd = New-AzApplicationGatewayFrontendIPConfig -Name "FrontendIP02" -Subnet $Subnet -PrivateIPAddress 10.0.1.1
```

첫 번째 명령은 ResourceGroup01이라는 리소스 그룹에 속하는 VNet01이라는 가상 네트워크를 $VNet 변수에 저장합니다.
두 번째 명령은 첫 번째 명령에서 $VNet 사용하여 Subnet01이라는 서브넷 구성을 $Subnet 변수에 저장합니다.
세 번째 명령은 두 번째 명령의 $Subnet 및 개인 IP 주소 10.0.1.1을 사용하여 FrontEndIP02라는 프런트 엔드 IP 구성을 만든 다음 $FrontEnd 변수에 저장합니다.

### 예제 3: 프런트 엔드 IP 주소로 동적 개인 IP 만들기
```
PS C:\>$VNet = Get-AzVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet
PS C:\> $FrontEnd = New-AzApplicationGatewayFrontendIPConfig -Name "FrontendIP03" -Subnet $Subnet
```

첫 번째 명령은 ResourceGroup01이라는 리소스 그룹에 속하는 VNet01이라는 가상 네트워크를 $VNet 변수에 저장합니다.
두 번째 명령은 첫 번째 명령에서 $VNet 사용하여 Subnet01이라는 서브넷 구성을 $Subnet 변수에 저장합니다.
세 번째 명령은 두 번째 명령의 $Subnet 사용하여 FrontEndIP03이라는 프런트 엔드 IP 구성을 만들고 $FrontEnd 변수에 저장합니다.

## PARAMETERS

### -DefaultProfile
Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
이 cmdlet에서 만드는 프런트 엔드 IP 구성의 이름을 지정합니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PrivateIPAddress
이 cmdlet이 애플리케이션 게이트웨이의 프런트 엔드 IP 주소와 연결되는 개인 IP 주소를 지정합니다.
이 지정은 서브넷이 지정된 경우만 지정할 수 있습니다.
이 IP는 서브넷에서 정적으로 할당됩니다.

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

### -PrivateLinkConfiguration
PrivateLinkConfiguration

```yaml
Type: PSApplicationGatewayPrivateLinkConfiguration
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PrivateLinkConfigurationId
PrivateLinkConfigurationId

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PublicIPAddress
이 cmdlet이 애플리케이션 게이트웨이의 프런트 엔드 IP 주소와 연결되는 공용 IP 주소 개체를 지정합니다.

```yaml
Type: PSPublicIpAddress
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PublicIPAddressId
이 cmdlet이 애플리케이션 게이트웨이의 프런트 엔드 IP와 연결되는 공용 IP 주소 ID를 지정합니다.

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Subnet
이 cmdlet이 애플리케이션 게이트웨이의 프런트 엔드 IP 주소와 연결되는 서브넷 개체를 지정합니다.
이 매개 변수를 지정하면 게이트웨이가 개인 IP 주소를 사용하게 됩니다.
*PrivateIPAddress* 매개 변수가 지정된 경우 이 매개 변수에 지정된 서브넷에 속해야 합니다.
*PrivateIPAddress를* 지정하지 않으면 이 서브넷의 IP 주소 중 하나는 애플리케이션 게이트웨이의 프런트 엔드 IP 주소로 동적으로 선택됩니다.

```yaml
Type: PSSubnet
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubnetId
이 cmdlet이 애플리케이션 게이트웨이의 프런트 엔드 IP 구성과 연결되는 서브넷 ID를 지정합니다.
서브넷 매개 *변수를* 지정하는 경우 게이트웨이가 개인 IP 주소를 사용함을 의미합니다.
*PrivateIPAddress* 매개 변수가 지정된 경우 서브넷에서 지정한 서브넷에 *속해야 합니다.*
*PrivateIPAddress를* 지정하지 않으면 이 서브넷의 IP 주소 중 하나는 애플리케이션 게이트웨이의 프런트 엔드 IP 주소로 동적으로 선택됩니다.

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.

## 입력

### 없음

## 출력

### Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendIPConfiguration

## 참고 사항

## 관련 링크

[Add-AzApplicationGatewayFrontendIPConfig](./Add-AzApplicationGatewayFrontendIPConfig.md)

[Get-AzApplicationGatewayFrontendIPConfig](./Get-AzApplicationGatewayFrontendIPConfig.md)

[Remove-AzApplicationGatewayFrontendIPConfig](./Remove-AzApplicationGatewayFrontendIPConfig.md)

[Set-AzApplicationGatewayFrontendIPConfig](./Set-AzApplicationGatewayFrontendIPConfig.md)


