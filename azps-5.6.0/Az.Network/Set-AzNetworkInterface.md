---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: DDB38A77-E5C0-47DD-BADD-94488F661CD5
online version: https://docs.microsoft.com/powershell/module/az.network/set-aznetworkinterface
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkInterface.md
ms.openlocfilehash: 0afd299103f1595afd100a7e9a72c4045896419d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101987700"
---
# Set-AzNetworkInterface

## SYNOPSIS
네트워크 인터페이스를 업데이트합니다.

## 구문

```
Set-AzNetworkInterface -NetworkInterface <PSNetworkInterface> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명
**Set-AzNetworkInterface는** 네트워크 인터페이스를 업데이트합니다.

## 예제

### 예제 1: 네트워크 인터페이스 구성
```
$Nic = Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$Nic.IpConfigurations[0].PrivateIpAddress = "10.0.1.20"
$Nic.IpConfigurations[0].PrivateIpAllocationMethod = "Static"
$Nic.Tag = @{Name = "Name"; Value = "Value"}
Set-AzNetworkInterface -NetworkInterface $Nic
```

이 예제에서는 네트워크 인터페이스를 구성합니다.
첫 번째 명령은 ResourceGroup1 리소스 그룹에서 NetworkInterface1이라는 네트워크 인터페이스를 얻습니다.
두 번째 명령은 IP 구성의 개인 IP 주소를 설정합니다.
세 번째 명령은 개인 IP 할당 메서드를 정적으로 설정합니다.
네 번째 명령은 네트워크 인터페이스에 태그를 설정합니다.
다섯 번째 명령은 네트워크 인터페이스를 설정하기 위해 $Nic 변수에 저장된 정보를 사용합니다.

### 예제 2: 네트워크 인터페이스에서 DNS 설정 변경
```
$nic = Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$nic.DnsSettings.DnsServers.Add("192.168.1.100")
$nic | Set-AzNetworkInterface
```

첫 번째 명령은 ResourceGroup1 리소스 그룹 내에 있는 NetworkInterface1이라는 네트워크 인터페이스를 얻습니다. 두 번째 명령은 DNS 서버 192.168.1.100을 이 인터페이스에 추가합니다. 세 번째 명령은 네트워크 인터페이스에 이러한 변경 내용을 적용합니다. DNS 서버를 제거하려면 위에 나열된 명령을 따르지만 "을 대체합니다. "를 "으로 추가합니다. 두 번째 명령에서 "제거"를 실행합니다.

### 예제 3: 네트워크 인터페이스에서 IP 전달 사용
```
$nic = Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$nic.EnableIPForwarding = 1
$nic | Set-AzNetworkInterface
```

첫 번째 명령은 NetworkInterface1이라는 기존 네트워크 인터페이스를 얻게 하여 $nic 변수에 저장합니다. 두 번째 명령은 IP 전달 값을 true로 변경합니다. 마지막으로 세 번째 명령은 네트워크 인터페이스에 변경 내용을 적용합니다. 네트워크 인터페이스에서 IP 전달을 사용하지 않도록 설정하기 위해 샘플 예제를 따르지만 두 번째 명령을 "$nic. EnableIPForwarding = 0".

### 예제 4: 네트워크 인터페이스의 서브넷 변경
```
$nic = Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$vnet = Get-AzVirtualNetwork -Name VNet1 -ResourceGroupName crosssubcrossversionpeering
$subnet2 = Get-AzVirtualNetworkSubnetConfig -Name Subnet2 -VirtualNetwork $vnet
$nic.IpConfigurations[0].Subnet.Id = $subnet2.Id
$nic | Set-AzNetworkInterface
```

첫 번째 명령은 NetworkInterface1 네트워크 인터페이스를 얻게 하여 $nic 변수에 저장합니다. 두 번째 명령은 네트워크 인터페이스가 연결될 서브넷과 연결된 가상 네트워크를 얻습니다. 두 번째 명령은 서브넷을 얻게 하여 $subnet 변수에 저장합니다. 세 번째 명령은 네트워크 인터페이스의 기본 개인 IP 주소를 새 서브넷과 연결했습니다. 마지막으로 마지막 명령은 네트워크 인터페이스에 이러한 변경 내용을 적용했습니다.
>[!NOTE] 
>서브넷을 변경하려면 먼저 IP 구성이 동적이 되어야 합니다. 정적 IP 구성이 있는 경우 계속하기 전에 동적으로 변경합니다. 
>[!NOTE]
>네트워크 인터페이스에 여러 IP 구성이 있는 경우 최종 명령이 실행되기 전에 이러한 모든 IP 구성에 대해 Set-AzNetworkInterface 해야 합니다. 이 명령은 첫 번째 명령에서처럼 수행되지만 "0"을 적절한 숫자로 대체하여 수행될 수 있습니다. 네트워크 인터페이스에 N IP 구성이 있는 경우 이러한 명령 중 N-1이 있어야 합니다.

### 예제 5: 네트워크 보안 그룹을 네트워크 인터페이스에 연결/해리합니다.
```
$nic = Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$nsg = Get-AzNetworkSecurityGroup -ResourceGroupName "ResourceGroup1" -Name "MyNSG"
$nic.NetworkSecurityGroup = $nsg
$nic | Set-AzNetworkInterface
```

첫 번째 명령은 NetworkInterface1이라는 기존 네트워크 인터페이스를 얻게 하여 $nic 변수에 저장합니다. 두 번째 명령은 MyNSG라는 기존 네트워크 보안 그룹을 얻게 $nsg 변수에 저장합니다. 세 번째 명령은 $nsg $nic. 마지막으로, 첫 번째 명령은 네트워크 인터페이스에 변경 내용을 적용합니다. 네트워크 인터페이스에서 네트워크 보안 그룹을 해리하기 위해 세 번째 명령에서 $nsg 간단한 $null.

## 매개 변수

### -AsJob
백그라운드에서 cmdlet 실행

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

### -NetworkInterface
네트워크 인터페이스를 설정해야 하는 상태를 나타내는 네트워크 인터페이스 개체를 지정합니다.

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

### CommonParameters
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.

## 입력

### Microsoft.Azure.Commands.Network.Models.PSNetworkInterface

## 출력

### Microsoft.Azure.Commands.Network.Models.PSNetworkInterface

## 참고 사항

## 관련 링크

[Get-AzNetworkInterface](./Get-AzNetworkInterface.md)

[Get-AzNetworkInterface](./Get-AzNetworkInterface.md)

[New-AzNetworkInterface](./New-AzNetworkInterface.md)

[Remove-AzNetworkInterface](./Remove-AzNetworkInterface.md)
