---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A3D60CF1-2E66-4EE5-9C68-932DD8DF80BD
online version: https://docs.microsoft.com/powershell/module/az.network/new-azfirewall
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewall.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewall.md
ms.openlocfilehash: e1d1e0668458d35496bf6bc3b0f7883c9f3ed00c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101973664"
---
# <span data-ttu-id="3abbd-101">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="3abbd-101">New-AzFirewall</span></span>

## <span data-ttu-id="3abbd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3abbd-102">SYNOPSIS</span></span>
<span data-ttu-id="3abbd-103">리소스 그룹에 새 방화벽을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="3abbd-103">Creates a new Firewall in a resource group.</span></span>

## <span data-ttu-id="3abbd-104">구문</span><span class="sxs-lookup"><span data-stu-id="3abbd-104">SYNTAX</span></span>

### <span data-ttu-id="3abbd-105">기본값(기본값)</span><span class="sxs-lookup"><span data-stu-id="3abbd-105">Default (Default)</span></span>
```
New-AzFirewall -Name <String> -ResourceGroupName <String> -Location <String>
 [-ApplicationRuleCollection <PSAzureFirewallApplicationRuleCollection[]>]
 [-NatRuleCollection <PSAzureFirewallNatRuleCollection[]>]
 [-NetworkRuleCollection <PSAzureFirewallNetworkRuleCollection[]>] [-ThreatIntelMode <String>]
 [-ThreatIntelWhitelist <PSAzureFirewallThreatIntelWhitelist>] [-PrivateRange <String[]>] [-EnableDnsProxy]
 [-DnsServer <String[]>] [-Tag <Hashtable>] [-Force] [-AsJob] [-Zone <String[]>] [-SkuName <String>]
 [-SkuTier <String>] [-VirtualHubId <String>] [-HubIPAddress <PSAzureFirewallHubIpAddresses>]
 [-FirewallPolicyId <String>] [-AllowActiveFTP] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3abbd-106">OldIpConfigurationParameterValues</span><span class="sxs-lookup"><span data-stu-id="3abbd-106">OldIpConfigurationParameterValues</span></span>
```
New-AzFirewall -Name <String> -ResourceGroupName <String> -Location <String> -VirtualNetworkName <String>
 -PublicIpName <String> [-ApplicationRuleCollection <PSAzureFirewallApplicationRuleCollection[]>]
 [-NatRuleCollection <PSAzureFirewallNatRuleCollection[]>]
 [-NetworkRuleCollection <PSAzureFirewallNetworkRuleCollection[]>] [-ThreatIntelMode <String>]
 [-ThreatIntelWhitelist <PSAzureFirewallThreatIntelWhitelist>] [-PrivateRange <String[]>] [-EnableDnsProxy]
 [-DnsServer <String[]>] [-Tag <Hashtable>] [-Force] [-AsJob] [-Zone <String[]>] [-SkuName <String>]
 [-SkuTier <String>] [-VirtualHubId <String>] [-HubIPAddress <PSAzureFirewallHubIpAddresses>]
 [-FirewallPolicyId <String>] [-AllowActiveFTP] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3abbd-107">IpConfigurationParameterValues</span><span class="sxs-lookup"><span data-stu-id="3abbd-107">IpConfigurationParameterValues</span></span>
```
New-AzFirewall -Name <String> -ResourceGroupName <String> -Location <String> -VirtualNetwork <PSVirtualNetwork>
 -PublicIpAddress <PSPublicIpAddress[]> [-ManagementPublicIpAddress <PSPublicIpAddress>]
 [-ApplicationRuleCollection <PSAzureFirewallApplicationRuleCollection[]>]
 [-NatRuleCollection <PSAzureFirewallNatRuleCollection[]>]
 [-NetworkRuleCollection <PSAzureFirewallNetworkRuleCollection[]>] [-ThreatIntelMode <String>]
 [-ThreatIntelWhitelist <PSAzureFirewallThreatIntelWhitelist>] [-PrivateRange <String[]>] [-EnableDnsProxy]
 [-DnsServer <String[]>] [-Tag <Hashtable>] [-Force] [-AsJob] [-Zone <String[]>] [-SkuName <String>]
 [-SkuTier <String>] [-VirtualHubId <String>] [-HubIPAddress <PSAzureFirewallHubIpAddresses>]
 [-FirewallPolicyId <String>] [-AllowActiveFTP] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3abbd-108">설명</span><span class="sxs-lookup"><span data-stu-id="3abbd-108">DESCRIPTION</span></span>
<span data-ttu-id="3abbd-109">**New-AzFirewall** cmdlet은 Azure 방화벽을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="3abbd-109">The **New-AzFirewall** cmdlet creates an Azure Firewall.</span></span>

## <span data-ttu-id="3abbd-110">예제</span><span class="sxs-lookup"><span data-stu-id="3abbd-110">EXAMPLES</span></span>

### <span data-ttu-id="3abbd-111">예제 1: 가상 네트워크에 연결된 방화벽 만들기</span><span class="sxs-lookup"><span data-stu-id="3abbd-111">Example 1: Create a Firewall attached to a virtual network</span></span>
```powershell
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip
```

<span data-ttu-id="3abbd-112">이 예제에서는 방화벽과 동일한 리소스 그룹에 가상 네트워크 "vnet"에 연결된 방화벽을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="3abbd-112">This example creates a Firewall attached to virtual network "vnet" in the same resource group as the firewall.</span></span>
<span data-ttu-id="3abbd-113">규칙이 지정되지 않은 경우 방화벽은 모든 트래픽(기본 동작)을 차단합니다.</span><span class="sxs-lookup"><span data-stu-id="3abbd-113">Since no rules were specified, the firewall will block all traffic (default behavior).</span></span>
<span data-ttu-id="3abbd-114">또한 위협 인텔은 기본 모드인 경고에서 실행됩니다. 즉 악의적인 트래픽이 기록되지만 거부되지는 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3abbd-114">Threat Intel will also run in default mode - Alert - which means malicious traffic will be logged, but not denied.</span></span>

### <span data-ttu-id="3abbd-115">예제 2: 모든 HTTPS 트래픽을 허용하는 방화벽 만들기</span><span class="sxs-lookup"><span data-stu-id="3abbd-115">Example 2: Create a Firewall which allows all HTTPS traffic</span></span>
```powershell
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"

$rule = New-AzFirewallApplicationRule -Name R1 -Protocol "https:443" -TargetFqdn "*" 
$ruleCollection = New-AzFirewallApplicationRuleCollection -Name RC1 -Priority 100 -Rule $rule -ActionType "Allow"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -ApplicationRuleCollection $ruleCollection
```

<span data-ttu-id="3abbd-116">이 예제에서는 포트 443의 모든 HTTPS 트래픽을 허용하는 방화벽을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="3abbd-116">This example creates a Firewall which allows all HTTPS traffic on port 443.</span></span>
<span data-ttu-id="3abbd-117">위협 인텔은 기본 모드인 경고에서 실행됩니다. 즉 악의적인 트래픽이 기록되지만 거부되지는 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3abbd-117">Threat Intel will run in default mode - Alert - which means malicious traffic will be logged, but not denied.</span></span>

### <span data-ttu-id="3abbd-118">예제 3: DNAT - 10.1.2.3:80으로 예정된 트래픽을 10.2.3.4:8080으로 리디렉션합니다.</span><span class="sxs-lookup"><span data-stu-id="3abbd-118">Example 3: DNAT - redirect traffic destined to 10.1.2.3:80 to 10.2.3.4:8080</span></span>
```powershell
$rule = New-AzFirewallNatRule -Name "natRule" -Protocol "TCP" -SourceAddress "*" -DestinationAddress "10.1.2.3" -DestinationPort "80" -TranslatedAddress "10.2.3.4" -TranslatedPort "8080"
$ruleCollection = New-AzFirewallNatRuleCollection -Name "NatRuleCollection" -Priority 1000 -Rule $rule
New-AzFirewall -Name "azFw" -ResourceGroupName "rg" -Location centralus -NatRuleCollection $ruleCollection -ThreatIntelMode Off
```

<span data-ttu-id="3abbd-119">이 예제에서는 10.1.2.3:80에서 10.2.3.4:8080 위협 인텔으로 예정된 모든 패킷의 대상 IP 및 포트를 변환하는 방화벽을 만들었다.</span><span class="sxs-lookup"><span data-stu-id="3abbd-119">This example created a Firewall which translated the destination IP and port of all packets destined to 10.1.2.3:80 to 10.2.3.4:8080 Threat Intel is turned off in this example.</span></span>

### <span data-ttu-id="3abbd-120">예제 4: 경고 모드에서 위협 인텔을 사용하여 규칙이 없는 방화벽 만들기</span><span class="sxs-lookup"><span data-stu-id="3abbd-120">Example 4: Create a Firewall with no rules and with Threat Intel in Alert mode</span></span>
```powershell
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -ThreatIntelMode Alert
```

<span data-ttu-id="3abbd-121">이 예제에서는 모든 트래픽(기본 동작)을 차단하고 위협 인텔이 경고 모드에서 실행되는 방화벽을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="3abbd-121">This example creates a Firewall which blocks all traffic (default behavior) and has Threat Intel running in Alert mode.</span></span>
<span data-ttu-id="3abbd-122">즉, 다른 규칙을 적용하기 전에 악의적인 트래픽에 대해 경고 로그가 내보이게 됩니다(이 경우 기본 규칙만 - 모두 거부)</span><span class="sxs-lookup"><span data-stu-id="3abbd-122">This means alerting logs are emitted for malicious traffic before applying the other rules (in this case just the default rule - Deny All)</span></span>

### <span data-ttu-id="3abbd-123">예제 5: 포트 8080의 모든 HTTP 트래픽을 허용하지만 Threat Intel에서 식별된 악의적인 도메인을 차단하는 방화벽 만들기</span><span class="sxs-lookup"><span data-stu-id="3abbd-123">Example 5: Create a Firewall which allows all HTTP traffic on port 8080, but blocks malicious domains identified by Threat Intel</span></span>
```powershell
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"

$rule = New-AzFirewallApplicationRule -Name R1 -Protocol "http:8080" -TargetFqdn "*" 
$ruleCollection = New-AzFirewallApplicationRuleCollection -Name RC1 -Priority 100 -Rule $rule -ActionType "Allow"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -ApplicationRuleCollection $ruleCollection -ThreatIntelMode Deny
```

<span data-ttu-id="3abbd-124">이 예제에서는 위협 인텔에 의해 악의적인 것으로 간주되지 않는 한 포트 8080의 모든 HTTP 트래픽을 허용하는 방화벽을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="3abbd-124">This example creates a Firewall which allows all HTTP traffic on port 8080 unless it is considered malicious by Threat Intel.</span></span>
<span data-ttu-id="3abbd-125">거부 모드에서 실행되는 경우 경고와 달리 Threat Intel에서 악의적인 것으로 간주되는 트래픽은 기록될 뿐만 아니라 차단됩니다.</span><span class="sxs-lookup"><span data-stu-id="3abbd-125">When running in Deny mode, unlike Alert, traffic considered malicious by Threat Intel is not just logged, but also blocked.</span></span>

### <span data-ttu-id="3abbd-126">예제 6: 규칙이 없는 방화벽 만들기 및 가용성 영역</span><span class="sxs-lookup"><span data-stu-id="3abbd-126">Example 6: Create a Firewall with no rules and with availability zones</span></span>
```powershell
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetworkName $vnet.Name -PublicIpName $pip.Name -Zone 1,2,3
```

<span data-ttu-id="3abbd-127">이 예제에서는 사용 가능한 모든 가용성 영역이 있는 방화벽을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="3abbd-127">This example creates a Firewall with all available availability zones.</span></span>

### <span data-ttu-id="3abbd-128">예제 7: 둘 이상의 공용 IP 주소가 있는 방화벽 만들기</span><span class="sxs-lookup"><span data-stu-id="3abbd-128">Example 7: Create a Firewall with two or more Public IP Addresses</span></span>
```powershell
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -Name "vnet" -ResourceGroupName $rgName
$pip1 = New-AzPublicIpAddress -Name "AzFwPublicIp1" -ResourceGroupName "rg" -SkuName "AZFW_VNet" -SkuTier "Standard" -Location "centralus" -AllocationMethod Static
$pip2 = New-AzPublicIpAddress -Name "AzFwPublicIp2" -ResourceGroupName "rg" -SkuName "AZFW_VNet" -SkuTier "Standard" -Location "centralus" -AllocationMethod Static
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress @($pip1, $pip2)
```

<span data-ttu-id="3abbd-129">이 예제에서는 두 개의 공용 IP 주소가 있는 가상 네트워크 "vnet"에 연결된 방화벽을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="3abbd-129">This example creates a Firewall attached to virtual network "vnet" with two public IP addresses.</span></span>

### <span data-ttu-id="3abbd-130">예제 8: 특정 데이터베이스 데이터베이스에 MSSQL 트래픽을 허용하는 방화벽 SQL 만들기</span><span class="sxs-lookup"><span data-stu-id="3abbd-130">Example 8: Create a Firewall which allows MSSQL traffic to specific SQL database</span></span>
```powershell
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"

$rule = New-AzFirewallApplicationRule -Name R1 -Protocol "mssql:1433" -TargetFqdn "sql1.database.windows.net"
$ruleCollection = New-AzFirewallApplicationRuleCollection -Name RC1 -Priority 100 -Rule $rule -ActionType "Allow"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -ApplicationRuleCollection $ruleCollection -ThreatIntelMode Deny
```

<span data-ttu-id="3abbd-131">이 예제에서는 표준 포트 1433에서 MSSQL 트래픽이 데이터베이스 SQL 허용하는 방화벽을 sql1.database.windows.net.</span><span class="sxs-lookup"><span data-stu-id="3abbd-131">This example creates a Firewall which allows MSSQL traffic on standard port 1433 to SQL database sql1.database.windows.net.</span></span>

### <span data-ttu-id="3abbd-132">예제 9: 가상 허브에 연결된 방화벽 만들기</span><span class="sxs-lookup"><span data-stu-id="3abbd-132">Example 9: Create a Firewall attached to a virtual hub</span></span>
```powershell
$rgName = "resourceGroupName"
$fp = Get-AzFirewallPolicy -ResourceGroupName $rgName -Name "fp"
$fpId = $fp.Id
$vHub = Get-AzVirtualHub -Name "hub"
$vHubId = $vHub.Id

New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -SkuName AZFW_Hub -VirtualHubId $vHubId -FirewallPolicyId -$fpId
```

<span data-ttu-id="3abbd-133">이 예제에서는 가상 허브 "vHub"에 연결된 방화벽을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="3abbd-133">This example creates a Firewall attached to virtual hub "vHub".</span></span> <span data-ttu-id="3abbd-134">방화벽 정책 $fp 방화벽에 연결됩니다.</span><span class="sxs-lookup"><span data-stu-id="3abbd-134">A firewall policy $fp will be attached to the firewall.</span></span> <span data-ttu-id="3abbd-135">이 방화벽은 방화벽 정책에 언급된 규칙에 따라 트래픽을 허용/$fp.</span><span class="sxs-lookup"><span data-stu-id="3abbd-135">This firewall allows/denies the traffic based on the rules mentioned in the firewall policy $fp.</span></span> <span data-ttu-id="3abbd-136">가상 허브와 방화벽은 동일한 지역에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3abbd-136">The virtual hub and the firewall should be in the same regions.</span></span>

### <span data-ttu-id="3abbd-137">예제 10: 위협 인텔리전스 허용 목록 설정으로 방화벽 만들기</span><span class="sxs-lookup"><span data-stu-id="3abbd-137">Example 10: Create a Firewall with threat intelligence whitelist setup</span></span>
```powershell
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"

$tiWhitelist = New-AzFirewallThreatIntelWhitelist -FQDN @("www.microsoft.com") -IpAddresses @("8.8.8.8")
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -ThreatIntelWhitelist $tiWhitelist
```

<span data-ttu-id="3abbd-138">이 예제에서는 위협 인텔리전스에서 "www.microsoft.com" 및 "8.8.8.8"을 허용 목록에 추가하는 방화벽을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="3abbd-138">This example creates a Firewall that whitelist "www.microsoft.com" and "8.8.8.8" from threat intelligence</span></span>

### <span data-ttu-id="3abbd-139">예제 11: 사용자 지정된 개인 범위 설정으로 방화벽 만들기</span><span class="sxs-lookup"><span data-stu-id="3abbd-139">Example 11: Create a Firewall with customized private range setup</span></span>
```powershell
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"

New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -PrivateRange @("99.99.99.0/24", "66.66.0.0/16")
```

<span data-ttu-id="3abbd-140">이 예제에서는 "99.99.99.0/24" 및 "66.66.0.0/16"을 개인 IP 범위로 처리하고 해당 주소에 대한 트래픽을 스나이트하지 않는 방화벽을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="3abbd-140">This example creates a Firewall that treats "99.99.99.0/24" and "66.66.0.0/16" as private ip ranges and won't snat traffic to those addresses</span></span>

### <span data-ttu-id="3abbd-141">예제 12: 관리 서브넷 및 공용 IP 주소를 사용하여 방화벽 만들기</span><span class="sxs-lookup"><span data-stu-id="3abbd-141">Example 12: Create a Firewall with a management subnet and Public IP address</span></span>
```powershell
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"
$mgmtPip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "managementPublicIpName"

New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -ManagementPublicIpAddress $mgmtPip
```

<span data-ttu-id="3abbd-142">이 예제에서는 방화벽과 동일한 리소스 그룹에 가상 네트워크 "vnet"에 연결된 방화벽을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="3abbd-142">This example creates a Firewall attached to virtual network "vnet" in the same resource group as the firewall.</span></span>
<span data-ttu-id="3abbd-143">규칙이 지정되지 않은 경우 방화벽은 모든 트래픽(기본 동작)을 차단합니다.</span><span class="sxs-lookup"><span data-stu-id="3abbd-143">Since no rules were specified, the firewall will block all traffic (default behavior).</span></span>
<span data-ttu-id="3abbd-144">또한 위협 인텔은 기본 모드인 경고에서 실행됩니다. 즉 악의적인 트래픽이 기록되지만 거부되지는 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3abbd-144">Threat Intel will also run in default mode - Alert - which means malicious traffic will be logged, but not denied.</span></span>

<span data-ttu-id="3abbd-145">"강제 터널링" 시나리오를 지원하기 위해 이 방화벽은 관리 트래픽에 대한 서브넷 "AzureFirewallManagementSubnet"과 관리 공용 IP 주소를 사용하게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="3abbd-145">To support "forced tunneling" scenarios, this firewall will use the subnet "AzureFirewallManagementSubnet" and the management public IP address for its management traffic</span></span>

### <span data-ttu-id="3abbd-146">예제 13: 가상 네트워크에 연결된 방화벽 정책을 사용하여 방화벽 만들기</span><span class="sxs-lookup"><span data-stu-id="3abbd-146">Example 13: Create a Firewall with Firewall Policy attached to a virtual network</span></span>
```powershell
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"
$fp = Get-AzFirewallPolicy -ResourceGroupName $rgName -Name "fp"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -FirewallPolicyId $fp
```

<span data-ttu-id="3abbd-147">이 예제에서는 방화벽과 동일한 리소스 그룹에 가상 네트워크 "vnet"에 연결된 방화벽을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="3abbd-147">This example creates a Firewall attached to virtual network "vnet" in the same resource group as the firewall.</span></span>
<span data-ttu-id="3abbd-148">방화벽에 적용되는 규칙 및 위협 인텔리전스가 방화벽 정책에서 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="3abbd-148">The rules and threat intelligence that will be applied to the firewall will be taken from the firewall policy</span></span>

### <span data-ttu-id="3abbd-149">예제 14: DNS 프록시 및 DNS 서버로 방화벽 만들기</span><span class="sxs-lookup"><span data-stu-id="3abbd-149">Example 14: Create a Firewall with DNS Proxy and DNS Servers</span></span>
```powershell
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -DnsServer @("10.10.10.1", "20.20.20.2")
```

<span data-ttu-id="3abbd-150">이 예제에서는 방화벽과 동일한 리소스 그룹에 가상 네트워크 "vnet"에 연결된 방화벽을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="3abbd-150">This example creates a Firewall attached to virtual network "vnet" in the same resource group as the firewall.</span></span>
<span data-ttu-id="3abbd-151">DNS 프록시는 이 방화벽에 대해 사용하도록 설정되어 있으며 2대의 DNS 서버가 제공됩니다.</span><span class="sxs-lookup"><span data-stu-id="3abbd-151">DNS Proxy is enabled for this firewall and 2 DNS Servers are provided.</span></span> <span data-ttu-id="3abbd-152">또한 네트워크 규칙에 대한 DNS 프록시 요구가 설정되어 있으므로 FQDNS를 사용하는 네트워크 규칙이 있는 경우 DNS 프록시도 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="3abbd-152">Also Require DNS Proxy for Network rules is set so if there are any Network rules with FQDNs then DNS proxy will be used for them too.</span></span>

### <span data-ttu-id="3abbd-153">예제 15: 여러 개의 IPS를 사용하여 방화벽 만들기</span><span class="sxs-lookup"><span data-stu-id="3abbd-153">Example 15: Create a Firewall with multiple IPs.</span></span> <span data-ttu-id="3abbd-154">방화벽은 Virtual Hub와 연결될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3abbd-154">The Firewall can be associated with the Virtual Hub</span></span>
```powershell
$rgName = "resourceGroupName"
$vHub = Get-AzVirtualHub -Name "hub"
$vHubId = $vHub.Id
$fwpips = New-AzFirewallHubPublicIpAddress -Count 2
$hubIpAddresses = New-AzFirewallHubIpAddress -PublicIPs $fwpips
$fw=New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location westus -SkuName AZFW_Hub -HubIPAddresses $hubIpAddresses -VirtualHubId $vHubId
```

<span data-ttu-id="3abbd-155">이 예제에서는 방화벽과 동일한 리소스 그룹에 가상 허브 "hub"에 연결된 방화벽을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="3abbd-155">This example creates a Firewall attached to virtual hub "hub" in the same resource group as the firewall.</span></span>
<span data-ttu-id="3abbd-156">방화벽은 암시적으로 생성된 2개 공용 IPS가 할당됩니다.</span><span class="sxs-lookup"><span data-stu-id="3abbd-156">The Firewall will be assigned 2 public IPs that are created implicitly.</span></span>

### <span data-ttu-id="3abbd-157">16: 활성 FTP 허용을 사용하여 방화벽 만들기</span><span class="sxs-lookup"><span data-stu-id="3abbd-157">16:  Create a Firewall with Allow Active FTP.</span></span>
```
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -AllowActiveFTP
```

<span data-ttu-id="3abbd-158">이 예제에서는 활성 FTP 플래그를 허용하는 방화벽을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="3abbd-158">This example creates a Firewall with allow active FTP flag.</span></span>

## <span data-ttu-id="3abbd-159">매개 변수</span><span class="sxs-lookup"><span data-stu-id="3abbd-159">PARAMETERS</span></span>

### <span data-ttu-id="3abbd-160">-AllowActiveFTP</span><span class="sxs-lookup"><span data-stu-id="3abbd-160">-AllowActiveFTP</span></span>
<span data-ttu-id="3abbd-161">방화벽에서 활성 FTP를 허용합니다.</span><span class="sxs-lookup"><span data-stu-id="3abbd-161">Allows Active FTP on the Firewall.</span></span> <span data-ttu-id="3abbd-162">기본적으로 사용하지 않도록 설정되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3abbd-162">By default it is disabled.</span></span>


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

### <span data-ttu-id="3abbd-163">-ApplicationRuleCollection</span><span class="sxs-lookup"><span data-stu-id="3abbd-163">-ApplicationRuleCollection</span></span>
<span data-ttu-id="3abbd-164">새 방화벽에 대한 애플리케이션 규칙 컬렉션을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="3abbd-164">Specifies the collections of application rules for the new Firewall.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSAzureFirewallApplicationRuleCollection[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3abbd-165">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3abbd-165">-AsJob</span></span>
<span data-ttu-id="3abbd-166">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="3abbd-166">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3abbd-167">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3abbd-167">-DefaultProfile</span></span>
<span data-ttu-id="3abbd-168">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3abbd-168">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3abbd-169">-DnsServer</span><span class="sxs-lookup"><span data-stu-id="3abbd-169">-DnsServer</span></span>
<span data-ttu-id="3abbd-170">DNS 확인에 사용할 DNS 서버 목록</span><span class="sxs-lookup"><span data-stu-id="3abbd-170">The list of DNS Servers to be used for DNS resolution,</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3abbd-171">-EnableDnsProxy</span><span class="sxs-lookup"><span data-stu-id="3abbd-171">-EnableDnsProxy</span></span>
<span data-ttu-id="3abbd-172">DNS 프록시를 사용하도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="3abbd-172">Enable DNS Proxy.</span></span> <span data-ttu-id="3abbd-173">기본적으로 사용하지 않도록 설정되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3abbd-173">By default it is disabled.</span></span>


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

### <span data-ttu-id="3abbd-174">-FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="3abbd-174">-FirewallPolicyId</span></span>
<span data-ttu-id="3abbd-175">방화벽에 연결된 방화벽 정책</span><span class="sxs-lookup"><span data-stu-id="3abbd-175">The firewall policy attached to the firewall</span></span>

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

### <span data-ttu-id="3abbd-176">-Force</span><span class="sxs-lookup"><span data-stu-id="3abbd-176">-Force</span></span>
<span data-ttu-id="3abbd-177">사용자 확인을 요청하지 않고 명령을 강제로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="3abbd-177">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="3abbd-178">-HubIPAddress</span><span class="sxs-lookup"><span data-stu-id="3abbd-178">-HubIPAddress</span></span>
<span data-ttu-id="3abbd-179">가상 허브에 연결된 방화벽의 IP 주소</span><span class="sxs-lookup"><span data-stu-id="3abbd-179">The ip addresses for the firewall attached to a virtual hub</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSAzureFirewallHubIpAddresses
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3abbd-180">-Location</span><span class="sxs-lookup"><span data-stu-id="3abbd-180">-Location</span></span>
<span data-ttu-id="3abbd-181">방화벽에 대한 지역을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="3abbd-181">Specifies the region for the Firewall.</span></span>

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

### <span data-ttu-id="3abbd-182">-ManagementPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="3abbd-182">-ManagementPublicIpAddress</span></span>
<span data-ttu-id="3abbd-183">관리 트래픽에 사용할 하나 이상의 공용 IP 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="3abbd-183">One or more Public IP Addresses to use for management traffic.</span></span> <span data-ttu-id="3abbd-184">공용 IP 주소는 표준 SKU를 사용하고 방화벽과 동일한 리소스 그룹에 속해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="3abbd-184">The Public IP addresses must use Standard SKU and must belong to the same resource group as the Firewall.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress
Parameter Sets: IpConfigurationParameterValues
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3abbd-185">-Name</span><span class="sxs-lookup"><span data-stu-id="3abbd-185">-Name</span></span>
<span data-ttu-id="3abbd-186">이 cmdlet이 만드는 Azure 방화벽의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="3abbd-186">Specifies the name of the Azure Firewall that this cmdlet creates.</span></span>

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

### <span data-ttu-id="3abbd-187">-NatRuleCollection</span><span class="sxs-lookup"><span data-stu-id="3abbd-187">-NatRuleCollection</span></span>
<span data-ttu-id="3abbd-188">AzureFirewallNatRuleCollections 목록</span><span class="sxs-lookup"><span data-stu-id="3abbd-188">The list of AzureFirewallNatRuleCollections</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNatRuleCollection[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3abbd-189">-NetworkRuleCollection</span><span class="sxs-lookup"><span data-stu-id="3abbd-189">-NetworkRuleCollection</span></span>
<span data-ttu-id="3abbd-190">AzureFirewallNetworkRuleCollections 목록</span><span class="sxs-lookup"><span data-stu-id="3abbd-190">The list of AzureFirewallNetworkRuleCollections</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRuleCollection[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3abbd-191">-PrivateRange</span><span class="sxs-lookup"><span data-stu-id="3abbd-191">-PrivateRange</span></span>
<span data-ttu-id="3abbd-192">트래픽이 SNAT에 사용되지 않는 개인 IP 범위</span><span class="sxs-lookup"><span data-stu-id="3abbd-192">The private IP ranges to which traffic won't be SNAT'ed</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3abbd-193">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="3abbd-193">-PublicIpAddress</span></span>
<span data-ttu-id="3abbd-194">하나 이상의 공용 IP 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="3abbd-194">One or more Public IP Addresses.</span></span> <span data-ttu-id="3abbd-195">공용 IP 주소는 표준 SKU를 사용하고 방화벽과 동일한 리소스 그룹에 속해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="3abbd-195">The Public IP addresses must use Standard SKU and must belong to the same resource group as the Firewall.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress[]
Parameter Sets: IpConfigurationParameterValues
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3abbd-196">-PublicIpName</span><span class="sxs-lookup"><span data-stu-id="3abbd-196">-PublicIpName</span></span>
<span data-ttu-id="3abbd-197">공용 IP 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3abbd-197">Public Ip Name.</span></span> <span data-ttu-id="3abbd-198">공용 IP는 표준 SKU를 사용하고 방화벽과 동일한 리소스 그룹에 속해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="3abbd-198">The Public IP must use Standard SKU and must belong to the same resource group as the Firewall.</span></span>

```yaml
Type: System.String
Parameter Sets: OldIpConfigurationParameterValues
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3abbd-199">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3abbd-199">-ResourceGroupName</span></span>
<span data-ttu-id="3abbd-200">방화벽을 포함할 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="3abbd-200">Specifies the name of a resource group to contain the Firewall.</span></span>

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

### <span data-ttu-id="3abbd-201">-SkuName</span><span class="sxs-lookup"><span data-stu-id="3abbd-201">-SkuName</span></span>
<span data-ttu-id="3abbd-202">방화벽의 sku 이름</span><span class="sxs-lookup"><span data-stu-id="3abbd-202">The sku name for firewall</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Sku
Accepted values: AZFW_Hub, AZFW_VNet

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3abbd-203">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="3abbd-203">-SkuTier</span></span>
<span data-ttu-id="3abbd-204">방화벽에 대한 sku 계층</span><span class="sxs-lookup"><span data-stu-id="3abbd-204">The sku tier for firewall</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Standard, Premium

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3abbd-205">-Tag</span><span class="sxs-lookup"><span data-stu-id="3abbd-205">-Tag</span></span>
<span data-ttu-id="3abbd-206">해시 테이블의 형태로 키 값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="3abbd-206">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="3abbd-207">예를 들어:</span><span class="sxs-lookup"><span data-stu-id="3abbd-207">For example:</span></span>

<span data-ttu-id="3abbd-208">@{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="3abbd-208">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="3abbd-209">-ThreatIntelMode</span><span class="sxs-lookup"><span data-stu-id="3abbd-209">-ThreatIntelMode</span></span>
<span data-ttu-id="3abbd-210">위협 인텔리전스에 대한 작업 모드를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="3abbd-210">Specifies the operation mode for Threat Intelligence.</span></span> <span data-ttu-id="3abbd-211">기본 모드는 해제가 아닌 경고입니다.</span><span class="sxs-lookup"><span data-stu-id="3abbd-211">Default mode is Alert, not Off.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Alert, Deny, Off

Required: False
Position: Named
Default value: Alert
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3abbd-212">-ThreatIntelWhitelist</span><span class="sxs-lookup"><span data-stu-id="3abbd-212">-ThreatIntelWhitelist</span></span>
<span data-ttu-id="3abbd-213">위협 인텔리전스에 대한 화이트리스트</span><span class="sxs-lookup"><span data-stu-id="3abbd-213">The whitelist for Threat Intelligence</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSAzureFirewallThreatIntelWhitelist
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3abbd-214">-VirtualHubId</span><span class="sxs-lookup"><span data-stu-id="3abbd-214">-VirtualHubId</span></span>
<span data-ttu-id="3abbd-215">방화벽이 연결된 가상 허브</span><span class="sxs-lookup"><span data-stu-id="3abbd-215">The virtual hub that a firewall is attached to</span></span>

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

### <span data-ttu-id="3abbd-216">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="3abbd-216">-VirtualNetwork</span></span>
<span data-ttu-id="3abbd-217">가상 네트워크</span><span class="sxs-lookup"><span data-stu-id="3abbd-217">Virtual Network</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork
Parameter Sets: IpConfigurationParameterValues
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3abbd-218">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="3abbd-218">-VirtualNetworkName</span></span>
<span data-ttu-id="3abbd-219">방화벽이 배포될 가상 네트워크의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="3abbd-219">Specifies the name of the virtual network for which the Firewall will be deployed.</span></span> <span data-ttu-id="3abbd-220">가상 네트워크 및 방화벽은 동일한 리소스 그룹에 속해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="3abbd-220">Virtual network and Firewall must belong to the same resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: OldIpConfigurationParameterValues
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3abbd-221">-Zone</span><span class="sxs-lookup"><span data-stu-id="3abbd-221">-Zone</span></span>
<span data-ttu-id="3abbd-222">방화벽에서 제공해야 하는 위치를 표시하는 가용성 영역의 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="3abbd-222">A list of availability zones denoting where the firewall needs to come from.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3abbd-223">-확인</span><span class="sxs-lookup"><span data-stu-id="3abbd-223">-Confirm</span></span>
<span data-ttu-id="3abbd-224">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="3abbd-224">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3abbd-225">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3abbd-225">-WhatIf</span></span>
<span data-ttu-id="3abbd-226">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="3abbd-226">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3abbd-227">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3abbd-227">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3abbd-228">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3abbd-228">CommonParameters</span></span>
<span data-ttu-id="3abbd-229">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="3abbd-229">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3abbd-230">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3abbd-230">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3abbd-231">입력</span><span class="sxs-lookup"><span data-stu-id="3abbd-231">INPUTS</span></span>

### <span data-ttu-id="3abbd-232">System.String</span><span class="sxs-lookup"><span data-stu-id="3abbd-232">System.String</span></span>

### <span data-ttu-id="3abbd-233">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="3abbd-233">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

### <span data-ttu-id="3abbd-234">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress[]</span><span class="sxs-lookup"><span data-stu-id="3abbd-234">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress[]</span></span>

### <span data-ttu-id="3abbd-235">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="3abbd-235">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

### <span data-ttu-id="3abbd-236">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallApplicationRuleCollection[]</span><span class="sxs-lookup"><span data-stu-id="3abbd-236">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallApplicationRuleCollection[]</span></span>

### <span data-ttu-id="3abbd-237">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNatRuleCollection[]</span><span class="sxs-lookup"><span data-stu-id="3abbd-237">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNatRuleCollection[]</span></span>

### <span data-ttu-id="3abbd-238">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRuleCollection[]</span><span class="sxs-lookup"><span data-stu-id="3abbd-238">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRuleCollection[]</span></span>

### <span data-ttu-id="3abbd-239">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="3abbd-239">System.Collections.Hashtable</span></span>

## <span data-ttu-id="3abbd-240">출력</span><span class="sxs-lookup"><span data-stu-id="3abbd-240">OUTPUTS</span></span>

### <span data-ttu-id="3abbd-241">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span><span class="sxs-lookup"><span data-stu-id="3abbd-241">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span></span>

## <span data-ttu-id="3abbd-242">참고 사항</span><span class="sxs-lookup"><span data-stu-id="3abbd-242">NOTES</span></span>

## <span data-ttu-id="3abbd-243">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3abbd-243">RELATED LINKS</span></span>

[<span data-ttu-id="3abbd-244">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="3abbd-244">Get-AzFirewall</span></span>](./Get-AzFirewall.md)

[<span data-ttu-id="3abbd-245">Remove-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="3abbd-245">Remove-AzFirewall</span></span>](./Remove-AzFirewall.md)

[<span data-ttu-id="3abbd-246">Set-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="3abbd-246">Set-AzFirewall</span></span>](./Set-AzFirewall.md)

[<span data-ttu-id="3abbd-247">New-AzFirewallApplicationRuleCollection</span><span class="sxs-lookup"><span data-stu-id="3abbd-247">New-AzFirewallApplicationRuleCollection</span></span>](./New-AzFirewallApplicationRuleCollection.md)

[<span data-ttu-id="3abbd-248">New-AzFirewallNatRuleCollection</span><span class="sxs-lookup"><span data-stu-id="3abbd-248">New-AzFirewallNatRuleCollection</span></span>](./New-AzFirewallNatRuleCollection.md)

[<span data-ttu-id="3abbd-249">New-AzFirewallNetworkRuleCollection</span><span class="sxs-lookup"><span data-stu-id="3abbd-249">New-AzFirewallNetworkRuleCollection</span></span>](./New-AzFirewallNetworkRuleCollection.md)
