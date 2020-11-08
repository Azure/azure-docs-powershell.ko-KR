---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: DDB38A77-E5C0-47DD-BADD-94488F661CD5
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznetworkinterface
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkInterface.md
ms.openlocfilehash: 9b851bcbaa545dee99628dc066956854181df7f7
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94219196"
---
# Set-AzNetworkInterface

## SYNOPSIS
네트워크 인터페이스를 업데이트 합니다.

## 구문과

```
Set-AzNetworkInterface -NetworkInterface <PSNetworkInterface> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명은
**AzNetworkInterface** 는 네트워크 인터페이스를 업데이트 합니다.

## 예제의

### 예제 1: 네트워크 인터페이스 구성
```
$Nic = Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$Nic.IpConfigurations[0].PrivateIpAddress = "10.0.1.20"
$Nic.IpConfigurations[0].PrivateIpAllocationMethod = "Static"
$Nic.Tag = @{Name = "Name"; Value = "Value"}
Set-AzNetworkInterface -NetworkInterface $Nic
```

이 예제에서는 네트워크 인터페이스를 구성 합니다.
첫 번째 명령은 리소스 그룹 ResourceGroup1에서 NetworkInterface1 라는 네트워크 인터페이스를 가져옵니다.
두 번째 명령은 IP 구성의 개인 IP 주소를 설정 합니다.
세 번째 명령은 개인 IP 할당 방법을 Static으로 설정 합니다.
네 번째 명령은 네트워크 인터페이스에 태그를 설정 합니다.
다섯 번째 명령은 $Nic 변수에 저장 된 정보를 사용 하 여 네트워크 인터페이스를 설정 합니다.

### 예제 2: 네트워크 인터페이스에서 DNS 설정 변경
```
$nic = Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$nic.DnsSettings.DnsServers.Add("192.168.1.100")
$nic | Set-AzNetworkInterface
```

첫 번째 명령은 리소스 그룹 ResourceGroup1 내에 있는 NetworkInterface1 라는 네트워크 인터페이스를 가져옵니다. 두 번째 명령은이 인터페이스에 DNS 서버 192.168.1.100를 추가 합니다. 세 번째 명령은 이러한 변경 내용을 네트워크 인터페이스에 적용 합니다. DNS 서버를 제거 하려면 위에 나열 된 명령을 실행 하 되, 대체 "를 입력 합니다. "With"를 추가 합니다. "제거"를 두 번 명령 합니다.

### 예제 3: 네트워크 인터페이스에서 IP 전달 사용
```
$nic = Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$nic.EnableIPForwarding = 1
$nic | Set-AzNetworkInterface
```

첫 번째 명령은 NetworkInterface1 이라는 기존 네트워크 인터페이스를 가져와 $nic 변수에 저장 합니다. 두 번째 명령은 IP 전달 값을 true로 변경 합니다. 마지막으로 세 번째 명령은 네트워크 인터페이스에 변경 내용을 적용 합니다. 네트워크 인터페이스에서 IP 전달을 사용 하지 않도록 설정 하려면 예제 예제를 따르고, 두 번째 명령을 "$nic로 변경 하세요. EnableIPForwarding = 0 "입니다.

### 예제 4: 네트워크 인터페이스의 서브넷 변경
```
$nic = Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$vnet = Get-AzVirtualNetwork -Name VNet1 -ResourceGroupName crosssubcrossversionpeering
$subnet2 = Get-AzVirtualNetworkSubnetConfig -Name Subnet2 -VirtualNetwork $vnet
$nic.IpConfigurations[0].Subnet.Id = $subnet2.Id
$nic | Set-AzNetworkInterface
```

첫 번째 명령은 네트워크 인터페이스 NetworkInterface1를 가져와이를 $nic 변수에 저장 합니다. 두 번째 명령은 네트워크 인터페이스가 연결 될 서브넷과 연결 된 가상 네트워크를 가져옵니다. 두 번째 명령은 서브넷을 가져와 $subnet 2 변수에 저장 합니다. 세 번째 명령은 새 서브넷이 있는 네트워크 인터페이스의 기본 개인 IP 주소와 연결 된 것입니다. 마지막으로 네트워크 인터페이스에 이러한 변경 내용을 적용 했습니다.
>[!NOTE] 
>서브넷을 변경할 수 있으려면 먼저 IP 구성이 동적 이어야 합니다. 고정 IP 구성이 있는 경우 계속 하기 전에 동적으로 변경 합니다. 
>[!NOTE]
>네트워크 인터페이스에 여러 개의 IP 구성이 있는 경우 이러한 모든 IP 구성에 대해 위 명령에 대해 마지막 Set-AzNetworkInterface 명령을 실행 하기 전에 수행 해야 합니다. 위의 명령 에서처럼 "0"을 적절 한 번호로 바꾸어이 작업을 수행할 수 있습니다. 네트워크 인터페이스에 N 개의 IP 구성이 있는 경우 이러한 명령의 N-1이 있어야 합니다.

### 예제 5: 네트워크 인터페이스에 네트워크 보안 그룹 연결/분리
```
$nic = Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$nsg = Get-AzNetworkSecurityGroup -ResourceGroupName "ResourceGroup1" -Name "MyNSG"
$nic.NetworkSecurityGroup = $nsg
$nic | Set-AzNetworkInterface
```

첫 번째 명령은 NetworkInterface1 이라는 기존 네트워크 인터페이스를 가져와 $nic 변수에 저장 합니다. 두 번째 명령은 MyNSG 이라는 기존 네트워크 보안 그룹을 가져와 $nsg 변수에 저장 합니다. 세 번째 명령은 $nsg를 $nic에 할당 합니다. 마지막으로, 위의 명령은 네트워크 인터페이스에 변경 내용을 적용 합니다. 네트워크 인터페이스에서 네트워크 보안 그룹을 분리 하려면, 세 번째 명령에서 $null으로 $nsg을 간단히 바꿉니다.

## 변수

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

### -NetworkInterface
네트워크 인터페이스를 설정 해야 하는 상태를 나타내는 네트워크 인터페이스 개체를 지정 합니다.

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
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### PSNetworkInterface에 대 한.

## 출력

### PSNetworkInterface에 대 한.

## 상속자

## 관련 링크

[Get-AzNetworkInterface](./Get-AzNetworkInterface.md)

[Get-AzNetworkInterface](./Get-AzNetworkInterface.md)

[새로운 AzNetworkInterface](./New-AzNetworkInterface.md)

[제거-AzNetworkInterface](./Remove-AzNetworkInterface.md)
