---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 81D55C43-C9A3-4DA7-A469-A3A7550FE9A4
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetwork.md
ms.openlocfilehash: d131b4aa22f46fed151486ed2d87f32684b6035a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98491769"
---
# New-AzVirtualNetwork

## SYNOPSIS
가상 네트워크를 만듭니다.

## 구문

```
New-AzVirtualNetwork -Name <String> -ResourceGroupName <String> -Location <String> -AddressPrefix <String[]>
 [-DnsServer <String[]>] [-Subnet <PSSubnet[]>] [-BgpCommunity <String>] [-Tag <Hashtable>]
 [-EnableDdosProtection] [-DdosProtectionPlanId <String>] [-IpAllocation <PSIpAllocation[]>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 설명
**New-AzVirtualNetwork** cmdlet은 Azure 가상 네트워크를 만듭니다.

## 예제

### 예제 1: 두 개의 서브넷이 있는 가상 네트워크 만들기
```powershell
New-AzResourceGroup -Name TestResourceGroup -Location centralus
$frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
$backendSubnet  = New-AzVirtualNetworkSubnetConfig -Name backendSubnet  -AddressPrefix "10.0.2.0/24"
New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet
```

이 예제에서는 두 개의 서브넷이 있는 가상 네트워크를 만듭니다. 먼저 중앙 지역에 새 리소스 그룹이 만들어집니다. 그런 다음, 이 예제에서는 두 서브넷의 메모리 내 표현을 만듭니다. New-AzVirtualNetworkSubnetConfig cmdlet은 서버 쪽에서 서브넷을 만들지 않습니다. frontendSubnet이라는 하나의 서브넷과 backendSubnet이라는 서브넷이 있습니다. 그런 New-AzVirtualNetwork cmdlet은 CIDR 10.0.0.0/16을 주소 연결 및 두 개의 서브넷으로 사용하여 가상 네트워크를 만듭니다.

### 예제 2: DNS 설정을 사용하여 가상 네트워크 만들기
```powershell
New-AzResourceGroup -Name TestResourceGroup -Location centralus
$frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
$backendSubnet  = New-AzVirtualNetworkSubnetConfig -Name backendSubnet  -AddressPrefix "10.0.2.0/24"
New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet -DnsServer 10.0.1.5,10.0.1.6
```

이 예제에서는 두 개의 서브넷과 두 개의 DNS 서버가 있는 가상 네트워크를 생성합니다. 가상 네트워크에 DNS 서버를 지정하면 이 가상 네트워크에 배포된 NIC/VM이 이러한 DNS 서버를 기본값으로 상속합니다. 이러한 기본값은 NIC 수준 설정을 통해 NIC당 덮어질 수 있습니다. VNET에 DNS 서버가 지정되지 않은 경우 NI에 DNS 서버가 없는 경우 DNS 확인에 기본 Azure DNS 서버가 사용됩니다.

### 예제 3: 네트워크 보안 그룹을 참조하는 서브넷이 있는 가상 네트워크 만들기
```powershell
New-AzResourceGroup -Name TestResourceGroup -Location centralus
$rdpRule              = New-AzNetworkSecurityRuleConfig -Name rdp-rule -Description "Allow RDP" -Access Allow -Protocol Tcp -Direction Inbound -Priority 100 -SourceAddressPrefix Internet -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 3389
$networkSecurityGroup = New-AzNetworkSecurityGroup -ResourceGroupName TestResourceGroup -Location centralus -Name "NSG-FrontEnd" -SecurityRules $rdpRule
$frontendSubnet       = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24" -NetworkSecurityGroup $networkSecurityGroup
$backendSubnet        = New-AzVirtualNetworkSubnetConfig -Name backendSubnet  -AddressPrefix "10.0.2.0/24" -NetworkSecurityGroup $networkSecurityGroup
New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet
```

이 예제에서는 네트워크 보안 그룹을 참조하는 서브넷이 있는 가상 네트워크를 만듭니다. 먼저, 이 예제에서는 만들 리소스에 대한 컨테이너로 리소스 그룹을 만듭니다. 그런 다음 인바운드 RDP 액세스를 허용하지만 그렇지 않으면 기본 네트워크 보안 그룹 규칙을 적용하는 네트워크 보안 그룹이 만들어집니다. 그런 New-AzVirtualNetworkSubnetConfig cmdlet은 생성된 네트워크 보안 그룹을 참조하는 두 서브넷의 메모리 내 표현을 만듭니다. 그런 New-AzVirtualNetwork 가상 네트워크를 만듭니다.

## PARAMETERS

### -AddressPrefix
가상 네트워크에 대한 IP 주소 범위를 지정합니다.

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

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

### -BgpCommunity
ExpressRoute를 통해 보급된 BGP 커뮤니티입니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DdosProtectionPlanId
가상 네트워크와 연결된 DDoS 보호 계획 리소스에 대한 참조입니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### -DnsServer
서브넷에 대한 DNS 서버를 지정합니다.

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -EnableDdosProtection
DDoS 보호를 사용하도록 설정하는지 아니면 그렇지 않은지 나타내는 스위치 매개 변수입니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force
사용자 확인을 요청하지 않고 명령을 강제로 실행합니다.

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

### -IpAllocation
가상 네트워크에 대한 IpAllocations를 지정합니다.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSIpAllocation[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Location
가상 네트워크에 대한 지역을 지정합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name
이 cmdlet에서 만드는 가상 네트워크의 이름을 지정합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
가상 네트워크를 포함할 리소스 그룹의 이름을 지정합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Subnet
가상 네트워크와 연결하기 위한 서브넷 목록을 지정합니다.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSSubnet[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Tag
해시 테이블 형식의 키-값 쌍입니다. 예: @{key0="value0";key1=$null;key2="value2"}

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Confirm
cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
cmdlet이 실행되는 경우의 결과 표시
cmdlet이 실행되지 않습니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.

## 입력

### System.String

### System.String[]

### Microsoft.Azure.Commands.Network.Models.PSSubnet[]

### System.Collections.Hashtable

## 출력

### Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork

## 참고 사항

## 관련 링크

[Get-AzVirtualNetwork](./Get-AzVirtualNetwork.md)

[Remove-AzVirtualNetwork](./Remove-AzVirtualNetwork.md)

[Set-AzVirtualNetwork](./Set-AzVirtualNetwork.md)

[New-AzDdosProtectionPlan](./New-AzDdosProtectionPlan.md)
