---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: D29C82CC-2080-48DA-880A-1AA83007E552
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkinterfaceipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkInterfaceIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkInterfaceIpConfig.md
ms.openlocfilehash: 80ffb0adf7703553d22cf991ad84a1af3b8e229c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94042137"
---
# New-AzNetworkInterfaceIpConfig

## SYNOPSIS
네트워크 인터페이스 IP 구성을 만듭니다.

## 구문과

### SetByResource (기본값)
```
New-AzNetworkInterfaceIpConfig -Name <String> [-PrivateIpAddressVersion <String>] [-PrivateIpAddress <String>]
 [-Primary] [-Subnet <PSSubnet>] [-PublicIpAddress <PSPublicIpAddress>]
 [-LoadBalancerBackendAddressPool <PSBackendAddressPool[]>] [-LoadBalancerInboundNatRule <PSInboundNatRule[]>]
 [-ApplicationGatewayBackendAddressPool <PSApplicationGatewayBackendAddressPool[]>]
 [-ApplicationSecurityGroup <PSApplicationSecurityGroup[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### SetByResourceId
```
New-AzNetworkInterfaceIpConfig -Name <String> [-PrivateIpAddressVersion <String>] [-PrivateIpAddress <String>]
 [-Primary] [-SubnetId <String>] [-PublicIpAddressId <String>] [-LoadBalancerBackendAddressPoolId <String[]>]
 [-LoadBalancerInboundNatRuleId <String[]>] [-ApplicationGatewayBackendAddressPoolId <String[]>]
 [-ApplicationSecurityGroupId <String[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명은
**AzNetworkInterfaceIpConfig** cmdlet은 네트워크 인터페이스에 대 한 Azure 네트워크 인터페이스 IP 구성을 만듭니다.

## 예제의

### 1: 네트워크 인터페이스용 공용 IP 주소를 사용 하 여 IP 구성 만들기
```
$vnet = Get-AzVirtualNetwork -Name myvnet -ResourceGroupName myrg
$Subnet = Get-AzVirtualNetworkSubnetConfig -Name mysubnet -VirtualNetwork $vnet
$PIP1 = Get-AzPublicIPAddress -Name "PIP1" -ResourceGroupName "RG1"

$IPConfig1 = New-AzNetworkInterfaceIpConfig -Name "IPConfig-1" -Subnet $Subnet -PublicIpAddress $PIP1
    -Primary

 $nic = New-AzNetworkInterface -Name $NicName -ResourceGroupName myrg -Location westus
    -IpConfiguration $IpConfig1
```

처음 두 명령은 myvnet 이라고 하는 가상 네트워크와 이전에 만든 myvnet 이라는 서브넷을 각각 가져옵니다. 이러한 두 가지는 $vnet 및 $Subnet에 각각 저장 됩니다. 세 번째 명령은 PIP1 이라는 이전에 만든 공용 IP 주소를 가져옵니다. 위의 명령은 공용 IP 주소가 연결 된 기본 IP 구성으로 "IPConfig-1" 이라는 새 IP 구성을 만듭니다.
마지막 명령은이 IP 구성을 사용 하 여 mynic1 라는 네트워크 인터페이스를 만듭니다.

### 2: 개인 IP 주소를 사용 하 여 IP 구성 만들기
```
$vnet = Get-AzVirtualNetwork -Name myvnet -ResourceGroupName myrg
$Subnet = Get-AzVirtualNetworkSubnetConfig -Name mysubnet -VirtualNetwork $vnet

$IPConfig2 = New-AzNetworkInterfaceIpConfig -Name "IP-Config2" -Subnet $Subnet -PrivateIpAddress
    10.0.0.5

$nic = New-AzNetworkInterface -Name mynic1 -ResourceGroupName myrg -Location westus -IpConfiguration
    $IpConfig2
```

처음 두 명령은 myvnet 이라고 하는 가상 네트워크와 이전에 만든 myvnet 이라는 서브넷을 각각 가져옵니다. 이러한 두 가지는 $vnet 및 $Subnet에 각각 저장 됩니다. 세 번째 명령은 개인 IP 주소와 연결 된 10.0.0.5 "IPConfig-2" 라는 새 IP 구성을 만듭니다.
마지막 명령은이 IP 구성을 사용 하 여 mynic1 라는 네트워크 인터페이스를 만듭니다.

## 변수

### -ApplicationGatewayBackendAddressPool
이 네트워크 인터페이스 IP 구성이 속한 응용 프로그램 게이트웨이 백 엔드 주소 풀 참조의 컬렉션을 지정 합니다.

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
이 네트워크 인터페이스 IP 구성이 속한 응용 프로그램 게이트웨이 백 엔드 주소 풀 참조의 컬렉션을 지정 합니다.

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
이 네트워크 인터페이스 IP 구성이 속한 응용 프로그램 보안 그룹 참조의 컬렉션을 지정 합니다.

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
이 네트워크 인터페이스 IP 구성이 속한 응용 프로그램 보안 그룹 참조의 컬렉션을 지정 합니다.

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

### -LoadBalancerBackendAddressPool
이 네트워크 인터페이스 IP 구성이 속한 부하 분산 장치 백 엔드 주소 풀 참조의 컬렉션을 지정 합니다.

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
이 네트워크 인터페이스 IP 구성이 속한 부하 분산 장치 백 엔드 주소 풀 참조의 컬렉션을 지정 합니다.

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
이 네트워크 인터페이스 IPConfiguration이 속한 부하 분산 장치 인바운드 Nat 규칙 참조의 컬렉션을 지정 합니다.

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
이 네트워크 인터페이스 IP 구성이 속한 부하 분산 장치 인바운드 네트워크 주소 변환 (NAT) 규칙 참조의 컬렉션을 지정 합니다.

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

### -이름
네트워크 인터페이스 IP 구성의 이름을 지정 합니다.

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

### -기본
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
네트워크 인터페이스 IP 구성의 고정 IP 주소를 지정 합니다.

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
네트워크 인터페이스 IP 구성의 IP 주소 버전을 지정 합니다.
이 매개 변수에 허용 되는 값은 다음과 같습니다.
- (Ipv4
- Ipv4/ipv6

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
**PublicIPAddress** 개체를 지정 합니다.
이 cmdlet은이 네트워크 인터페이스 IP 구성과 연결할 공용 IP 주소에 대 한 참조를 만듭니다.

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
이 cmdlet은이 네트워크 인터페이스 IP 구성과 연결할 공용 IP 주소에 대 한 참조를 만듭니다.

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
**서브넷** 개체를 지정 합니다.
이 cmdlet은이 네트워크 인터페이스 IP 구성을 만드는 서브넷에 대 한 참조를 만듭니다.

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
이 네트워크 인터페이스 IP 구성을 만드는 서브넷에 대 한 참조를 지정 합니다.

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
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### System.webserver []

### PSBackendAddressPool [] (으)로

### PSInboundNatRule [] (으)로

### PSApplicationGatewayBackendAddressPool [] (으)로

### Microsoft Azure. * PSApplicationSecurityGroup []

## 출력

### PSNetworkInterfaceIPConfiguration에 대 한.

## 상속자
* 키워드: azure, azurerm, arm, resource, 관리, 관리자, 네트워크, 네트워킹

## 관련 링크

[추가-AzNetworkInterfaceIpConfig](./Add-AzNetworkInterfaceIpConfig.md)

[Get-AzNetworkInterfaceIpConfig](./Get-AzNetworkInterfaceIpConfig.md)

[제거-AzNetworkInterfaceIpConfig](./Remove-AzNetworkInterfaceIpConfig.md)

[Set-AzNetworkInterfaceIpConfig](./Set-AzNetworkInterfaceIpConfig.md)
