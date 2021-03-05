---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 7610228A-61F9-41B8-A42A-CD7C793BB33F
online version: https://docs.microsoft.com/powershell/module/az.network/add-aznetworkinterfaceipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzNetworkInterfaceIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzNetworkInterfaceIpConfig.md
ms.openlocfilehash: 47ad7c00c2db310003dcc87b20405d05ec7f1f5a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102009483"
---
# Add-AzNetworkInterfaceIpConfig

## SYNOPSIS
네트워크 인터페이스 IP 구성을 네트워크 인터페이스에 추가합니다.

## 구문

### SetByResource(기본값)
```
Add-AzNetworkInterfaceIpConfig -Name <String> -NetworkInterface <PSNetworkInterface>
 [-PrivateIpAddressVersion <String>] [-PrivateIpAddress <String>] [-Primary] [-Subnet <PSSubnet>]
 [-PublicIpAddress <PSPublicIpAddress>] [-LoadBalancerBackendAddressPool <PSBackendAddressPool[]>]
 [-LoadBalancerInboundNatRule <PSInboundNatRule[]>]
 [-ApplicationGatewayBackendAddressPool <PSApplicationGatewayBackendAddressPool[]>]
 [-ApplicationSecurityGroup <PSApplicationSecurityGroup[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### SetByResourceId
```
Add-AzNetworkInterfaceIpConfig -Name <String> -NetworkInterface <PSNetworkInterface>
 [-PrivateIpAddressVersion <String>] [-PrivateIpAddress <String>] [-Primary] [-SubnetId <String>]
 [-PublicIpAddressId <String>] [-LoadBalancerBackendAddressPoolId <String[]>]
 [-LoadBalancerInboundNatRuleId <String[]>] [-ApplicationGatewayBackendAddressPoolId <String[]>]
 [-ApplicationSecurityGroupId <String[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명
**Add-AzNetworkInterfaceIpConfig** cmdlet은 Azure 네트워크 인터페이스에 네트워크 인터페이스 IP 구성을 추가합니다.

## 예제

### 예제 1: 애플리케이션 보안 그룹을 통해 새 IP 구성 추가
```
$subnet = New-AzVirtualNetworkSubnetConfig -Name MySubnet -AddressPrefix 10.0.1.0/24
$vnet = New-AzVirtualNetwork -Name MyVNET -ResourceGroupName MyResourceGroup -Location "West US" -AddressPrefix 10.0.0.0/16 -Subnet $subnet

$nic = New-AzNetworkInterface -Name MyNetworkInterface -ResourceGroupName MyResourceGroup -Location "West US" -Subnet $vnet.Subnets[0]

$asg = New-AzApplicationSecurityGroup -ResourceGroupName MyResourceGroup -Name MyASG -Location "West US"

$nic | Set-AzNetworkInterfaceIpConfig -Name $nic.IpConfigurations[0].Name -Subnet $vnet.Subnets[0] -ApplicationSecurityGroup $asg | Set-AzNetworkInterface

$nic | Add-AzNetworkInterfaceIpConfig -Name MyNewIpConfig -Subnet $vnet.Subnets[0] -ApplicationSecurityGroup $asg | Set-AzNetworkInterface
```

이 예제에서는 새 가상 네트워크 MyVNET의 서브넷에 속하는 새 네트워크 인터페이스 MyNetworkInterface를 생성합니다. 또한 네트워크 인터페이스의 IP 구성과 연결하기 위한 빈 애플리케이션 보안 그룹 MyASG도 생성합니다. 두 개체를 모두 만든 후 기본 IP 구성을 MyASG 개체에 연결합니다. 마지막으로 네트워크 인터페이스에서 애플리케이션 보안 그룹 개체와도 연결된 새 IP 구성을 만듭니다.

## 매개 변수

### -ApplicationGatewayBackendAddressPool
이 네트워크 인터페이스 IP 구성이 속한 애플리케이션 게이트웨이 백드 주소 풀 참조의 컬렉션을 지정합니다.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool[]
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ApplicationGatewayBackendAddressPoolId
이 네트워크 인터페이스 IP 구성이 속한 애플리케이션 게이트웨이 백드 주소 풀 참조의 컬렉션을 지정합니다.

```yaml
Type: System.String[]
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ApplicationSecurityGroup
이 네트워크 인터페이스 IP 구성이 속한 애플리케이션 보안 그룹 참조 컬렉션을 지정합니다.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup[]
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ApplicationSecurityGroupId
이 네트워크 인터페이스 IP 구성이 속한 애플리케이션 보안 그룹 참조 컬렉션을 지정합니다.

```yaml
Type: System.String[]
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.

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

### -LoadBalancerBackendAddressPool
이 네트워크 인터페이스 IP 구성이 속한 부하 균형 조정기 백end 주소 풀 참조의 컬렉션을 지정합니다.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool[]
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -LoadBalancerBackendAddressPoolId
이 네트워크 인터페이스 IP 구성이 속한 부하 균형 조정기 백end 주소 풀 참조의 컬렉션을 지정합니다.

```yaml
Type: System.String[]
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -LoadBalancerInboundNatRule
이 네트워크 인터페이스 IP 구성이 속한 NAT(Load Balancer 인바운드 네트워크 주소 변환) 규칙 참조의 컬렉션을 지정합니다.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSInboundNatRule[]
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -LoadBalancerInboundNatRuleId
이 네트워크 인터페이스 IP 구성이 속한 부하 균형기 인바운드 NAT 규칙 참조의 컬렉션을 지정합니다.

```yaml
Type: System.String[]
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name
네트워크 인터페이스 IP 구성의 이름을 지정합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NetworkInterface
**NetworkInterface 개체를 지정합니다.**
이 cmdlet은 이 매개 변수가 지정하는 개체에 네트워크 인터페이스 IP 구성을 추가합니다.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkInterface
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Primary
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

### -PrivateIpAddress
네트워크 인터페이스 IP 구성의 정적 IP 주소를 지정합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PrivateIpAddressVersion
네트워크 인터페이스 IP 구성의 IP 주소 버전을 지정합니다.
이 매개 변수에 대해 허용되는 값은 다음입니다.
- IPv4
- IPv6

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: IPv4, IPv6

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PublicIpAddress
**PublicIPAddress 개체를 지정합니다.**
이 cmdlet은 공용 IP 주소에 대한 참조를 만들어 이 네트워크 인터페이스 IP 구성과 연결합니다.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PublicIpAddressId
이 cmdlet은 공용 IP 주소에 대한 참조를 만들어 이 네트워크 인터페이스 IP 구성과 연결합니다.

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -서브넷
**서브넷** 개체를 지정합니다.
이 cmdlet은 이 네트워크 인터페이스 IP 구성이 생성되는 서브넷에 대한 참조를 만듭니다.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSSubnet
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubnetId
이 cmdlet은 이 네트워크 인터페이스 IP 구성이 생성되는 서브넷에 대한 참조를 만듭니다.

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.

## 입력

### Microsoft.Azure.Commands.Network.Models.PSNetworkInterface

### System.String[]

### Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool[]

### Microsoft.Azure.Commands.Network.Models.PSInboundNatRule[]

### Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool[]

### Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup[]

## 출력

### Microsoft.Azure.Commands.Network.Models.PSNetworkInterface

## 참고 사항
* 키워드: azure, azurerm, arm, 리소스, 관리, 관리자, 네트워크, 네트워킹

## 관련 링크

[Get-AzNetworkInterfaceIpConfig](./Get-AzNetworkInterfaceIpConfig.md)

[New-AzNetworkInterfaceIpConfig](./New-AzNetworkInterfaceIpConfig.md)

[Remove-AzNetworkInterfaceIpConfig](./Remove-AzNetworkInterfaceIpConfig.md)

[Set-AzNetworkInterfaceIpConfig](./Set-AzNetworkInterfaceIpConfig.md)
