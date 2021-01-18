---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: DDB38A77-E5C0-47DD-BADD-94488F661CD5
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznetworkinterface
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkInterface.md
ms.openlocfilehash: 9b851bcbaa545dee99628dc066956854181df7f7
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98496496"
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
첫 번째 명령은 리소스 그룹 ResourceGroup1에서 NetworkInterface1이라는 네트워크 인터페이스를 얻습니다.
두 번째 명령은 IP 구성의 개인 IP 주소를 설정합니다.
세 번째 명령은 개인 IP 할당 방법을 고정으로 설정합니다.
네 번째 명령은 네트워크 인터페이스에 태그를 설정합니다.
다섯 번째 명령은 네트워크 인터페이스를 설정하기 위해 $Nic 변수에 저장된 정보를 사용합니다.

### 예제 2: 네트워크 인터페이스에서 DNS 설정 변경
```
$nic = Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$nic.DnsSettings.DnsServers.Add("192.168.1.100")
$nic | Set-AzNetworkInterface
```

첫 번째 명령은 리소스 그룹 ResourceGroup1 내에 있는 NetworkInterface1이라는 네트워크 인터페이스를 얻습니다. 두 번째 명령은 이 인터페이스에 DNS 서버 192.168.1.100을 추가합니다. 세 번째 명령은 네트워크 인터페이스에 이러한 변경 내용을 적용합니다. DNS 서버를 제거하려면 위에 나열된 명령을 따르지만 "을(를) 대체합니다. "을(를) 통해 "를 추가합니다. 두 번째 명령에서 "제거"를 실행합니다.

### 예제 3: 네트워크 인터페이스에서 IP 전달 사용
```
$nic = Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$nic.EnableIPForwarding = 1
$nic | Set-AzNetworkInterface
```

첫 번째 명령은 NetworkInterface1이라는 기존 네트워크 인터페이스를 $nic 변수에 저장합니다. 두 번째 명령은 IP 전달 값을 true로 변경합니다. 마지막으로 세 번째 명령은 네트워크 인터페이스에 변경 내용을 적용합니다. 네트워크 인터페이스에서 IP 전달을 사용하지 않도록 설정하는 경우 샘플 예제를 따르지만 두 번째 명령을 "연결"으로 $nic. EnableIPForwarding = 0".

### 예제 4: 네트워크 인터페이스의 서브넷 변경
```
$nic = Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$vnet = Get-AzVirtualNetwork -Name VNet1 -ResourceGroupName crosssubcrossversionpeering
$subnet2 = Get-AzVirtualNetworkSubnetConfig -Name Subnet2 -VirtualNetwork $vnet
$nic.IpConfigurations[0].Subnet.Id = $subnet2.Id
$nic | Set-AzNetworkInterface
```

첫 번째 명령은 NetworkInterface1 네트워크 인터페이스를 사용하여 네트워크 인터페이스를 $nic 변수에 저장합니다. 두 번째 명령은 네트워크 인터페이스가 연결될 서브넷과 연결된 가상 네트워크를 얻습니다. 두 번째 명령은 서브넷을 사용하여 $subnet 2 변수에 저장합니다. 세 번째 명령은 네트워크 인터페이스의 기본 개인 IP 주소를 새 서브넷과 연결했습니다. 마지막으로 마지막 명령은 네트워크 인터페이스에 이러한 변경 내용을 적용했습니다.
>[!NOTE] 
>서브넷을 변경하려면 먼저 IP 구성이 동적이 되어야 합니다. 고정 IP 구성이 있는 경우 계속하기 전에 동적 IP 구성으로 변경합니다. 
>[!NOTE]
>네트워크 인터페이스에 여러 IP 구성이 있는 경우 마지막 명령이 실행되기 전에 이러한 모든 IP 구성에 대해 Set-AzNetworkInterface 합니다. 이는 첫 번째 명령에서처럼 수행되지만 "0"을 적절한 숫자로 바꾸면 됩니다. 네트워크 인터페이스에 N IP 구성이 있는 경우 이러한 명령 중 N-1이 있어야 합니다.

### 예제 5: 네트워크 인터페이스에 네트워크 보안 그룹 연결/연결 해리
```
$nic = Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$nsg = Get-AzNetworkSecurityGroup -ResourceGroupName "ResourceGroup1" -Name "MyNSG"
$nic.NetworkSecurityGroup = $nsg
$nic | Set-AzNetworkInterface
```

첫 번째 명령은 NetworkInterface1이라는 기존 네트워크 인터페이스를 $nic 변수에 저장합니다. 두 번째 명령은 MyNSG라는 기존 네트워크 보안 그룹을 $nsg 변수에 저장합니다. 세 번째 명령은 $nsg 할당하는 $nic. 마지막으로, 첫 번째 명령은 네트워크 인터페이스에 변경 내용을 적용합니다. 네트워크 인터페이스에서 네트워크 보안 그룹을 해리하기 위해 세 번째 $nsg 네트워크 인터페이스로 $null.

## PARAMETERS

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
Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.

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
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.

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
