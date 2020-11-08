---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A3D60CF1-2E66-4EE5-9C68-932DD8DF80BD
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewall
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewall.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewall.md
ms.openlocfilehash: a7c38a264860ad4a8458dbdb3555980279a33ff0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94214861"
---
# <span data-ttu-id="696a2-101">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="696a2-101">New-AzFirewall</span></span>

## <span data-ttu-id="696a2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="696a2-102">SYNOPSIS</span></span>
<span data-ttu-id="696a2-103">리소스 그룹에 새 방화벽을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="696a2-103">Creates a new Firewall in a resource group.</span></span>

## <span data-ttu-id="696a2-104">구문과</span><span class="sxs-lookup"><span data-stu-id="696a2-104">SYNTAX</span></span>

### <span data-ttu-id="696a2-105">기본값 (기본값)</span><span class="sxs-lookup"><span data-stu-id="696a2-105">Default (Default)</span></span>
```
New-AzFirewall -Name <String> -ResourceGroupName <String> -Location <String>
 [-ApplicationRuleCollection <PSAzureFirewallApplicationRuleCollection[]>]
 [-NatRuleCollection <PSAzureFirewallNatRuleCollection[]>]
 [-NetworkRuleCollection <PSAzureFirewallNetworkRuleCollection[]>] [-ThreatIntelMode <String>]
 [-ThreatIntelWhitelist <PSAzureFirewallThreatIntelWhitelist>] [-PrivateRange <String[]>] [-EnableDnsProxy]
 [-DnsProxyNotRequiredForNetworkRule] [-DnsServer <String[]>] [-AllowActiveFTP] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-Zone <String[]>] [-Sku <String>] [-VirtualHubId <String>] [-HubIPAddresses <PSAzureFirewallHubIpAddresses>]
 [-FirewallPolicyId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="696a2-106">OldIpConfigurationParameterValues</span><span class="sxs-lookup"><span data-stu-id="696a2-106">OldIpConfigurationParameterValues</span></span>
```
New-AzFirewall -Name <String> -ResourceGroupName <String> -Location <String> -VirtualNetworkName <String>
 -PublicIpName <String> [-ApplicationRuleCollection <PSAzureFirewallApplicationRuleCollection[]>]
 [-NatRuleCollection <PSAzureFirewallNatRuleCollection[]>]
 [-NetworkRuleCollection <PSAzureFirewallNetworkRuleCollection[]>] [-ThreatIntelMode <String>]
 [-ThreatIntelWhitelist <PSAzureFirewallThreatIntelWhitelist>] [-PrivateRange <String[]>] [-EnableDnsProxy]
 [-DnsProxyNotRequiredForNetworkRule] [-DnsServer <String[]>] [-AllowActiveFTP] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-Zone <String[]>] [-Sku <String>] [-VirtualHubId <String>] [-HubIPAddresses <PSAzureFirewallHubIpAddresses>]
 [-FirewallPolicyId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="696a2-107">IpConfigurationParameterValues</span><span class="sxs-lookup"><span data-stu-id="696a2-107">IpConfigurationParameterValues</span></span>
```
New-AzFirewall -Name <String> -ResourceGroupName <String> -Location <String> -VirtualNetwork <PSVirtualNetwork>
 -PublicIpAddress <PSPublicIpAddress[]> [-ManagementPublicIpAddress <PSPublicIpAddress>]
 [-ApplicationRuleCollection <PSAzureFirewallApplicationRuleCollection[]>]
 [-NatRuleCollection <PSAzureFirewallNatRuleCollection[]>]
 [-NetworkRuleCollection <PSAzureFirewallNetworkRuleCollection[]>] [-ThreatIntelMode <String>]
 [-ThreatIntelWhitelist <PSAzureFirewallThreatIntelWhitelist>] [-PrivateRange <String[]>] [-EnableDnsProxy]
 [-DnsProxyNotRequiredForNetworkRule] [-DnsServer <String[]>] [-AllowActiveFTP] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-Zone <String[]>] [-Sku <String>] [-VirtualHubId <String>] [-HubIPAddresses <PSAzureFirewallHubIpAddresses>]
 [-FirewallPolicyId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="696a2-108">설명은</span><span class="sxs-lookup"><span data-stu-id="696a2-108">DESCRIPTION</span></span>
<span data-ttu-id="696a2-109">**새 AzFirewall** Cmdlet은 Azure 방화벽을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="696a2-109">The **New-AzFirewall** cmdlet creates an Azure Firewall.</span></span>

## <span data-ttu-id="696a2-110">예제의</span><span class="sxs-lookup"><span data-stu-id="696a2-110">EXAMPLES</span></span>

### <span data-ttu-id="696a2-111">예제 1: 가상 네트워크에 연결 된 방화벽 만들기</span><span class="sxs-lookup"><span data-stu-id="696a2-111">Example 1: Create a Firewall attached to a virtual network</span></span>
```powershell
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip
```

<span data-ttu-id="696a2-112">이 예제에서는 방화벽과 동일한 리소스 그룹의 가상 네트워크 "vnet"에 연결 된 방화벽을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="696a2-112">This example creates a Firewall attached to virtual network "vnet" in the same resource group as the firewall.</span></span>
<span data-ttu-id="696a2-113">규칙은 지정 되지 않았으므로 방화벽은 모든 트래픽을 차단 합니다 (기본 동작).</span><span class="sxs-lookup"><span data-stu-id="696a2-113">Since no rules were specified, the firewall will block all traffic (default behavior).</span></span>
<span data-ttu-id="696a2-114">또한 인텔은 기본적 모드-경고-즉, 악의적인 소통량이 기록 되지만 거부 되지 않음을 의미 합니다.</span><span class="sxs-lookup"><span data-stu-id="696a2-114">Threat Intel will also run in default mode - Alert - which means malicious traffic will be logged, but not denied.</span></span>

### <span data-ttu-id="696a2-115">예제 2: 모든 HTTPS 트래픽을 허용 하는 방화벽 만들기</span><span class="sxs-lookup"><span data-stu-id="696a2-115">Example 2: Create a Firewall which allows all HTTPS traffic</span></span>
```powershell
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"

$rule = New-AzFirewallApplicationRule -Name R1 -Protocol "https:443" -TargetFqdn "*" 
$ruleCollection = New-AzFirewallApplicationRuleCollection -Name RC1 -Priority 100 -Rule $rule -ActionType "Allow"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -ApplicationRuleCollection $ruleCollection
```

<span data-ttu-id="696a2-116">이 예제에서는 포트 443에서 모든 HTTPS 트래픽을 허용 하는 방화벽을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="696a2-116">This example creates a Firewall which allows all HTTPS traffic on port 443.</span></span>
<span data-ttu-id="696a2-117">인텔은 기본 모드-경고-알림-악의적인 트래픽이 기록 되지만 거부 되지 않음을 의미 합니다.</span><span class="sxs-lookup"><span data-stu-id="696a2-117">Threat Intel will run in default mode - Alert - which means malicious traffic will be logged, but not denied.</span></span>

### <span data-ttu-id="696a2-118">예제 3:10.1.2.3:80으로 보낸 DNAT 리디렉션 트래픽 10.2.3.4:8080</span><span class="sxs-lookup"><span data-stu-id="696a2-118">Example 3: DNAT - redirect traffic destined to 10.1.2.3:80 to 10.2.3.4:8080</span></span>
```powershell
$rule = New-AzFirewallNatRule -Name "natRule" -Protocol "TCP" -SourceAddress "*" -DestinationAddress "10.1.2.3" -DestinationPort "80" -TranslatedAddress "10.2.3.4" -TranslatedPort "8080"
$ruleCollection = New-AzFirewallNatRuleCollection -Name "NatRuleCollection" -Priority 1000 -Rule $rule
New-AzFirewall -Name "azFw" -ResourceGroupName "rg" -Location centralus -NatRuleCollection $ruleCollection -ThreatIntelMode Off
```

<span data-ttu-id="696a2-119">이 예제에서는 10.1.2.3:80으로 보내는 모든 패킷의 대상 IP 및 포트를 10.2.3.4:8080 위협으로 변환 하는 방화벽을 만들었습니다 .이 예제에서는 Intel이 해제 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="696a2-119">This example created a Firewall which translated the destination IP and port of all packets destined to 10.1.2.3:80 to 10.2.3.4:8080 Threat Intel is turned off in this example.</span></span>

### <span data-ttu-id="696a2-120">예제 4: 규칙 없이 또는 경고 모드에서의 위협에 대 한 방화벽 만들기</span><span class="sxs-lookup"><span data-stu-id="696a2-120">Example 4: Create a Firewall with no rules and with Threat Intel in Alert mode</span></span>
```powershell
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -ThreatIntelMode Alert
```

<span data-ttu-id="696a2-121">이 예제에서는 모든 트래픽을 차단 하는 방화벽을 만들고 (기본 동작) 위협 Intel이 알림 모드로 실행 되 고 있습니다.</span><span class="sxs-lookup"><span data-stu-id="696a2-121">This example creates a Firewall which blocks all traffic (default behavior) and has Threat Intel running in Alert mode.</span></span>
<span data-ttu-id="696a2-122">즉,이 경우에는 다른 규칙을 적용 하기 전에 악의적인 트래픽에 대 한 경고 로그가 생성 됩니다 (이 경우에는 기본 규칙-모두 거부만 해당).</span><span class="sxs-lookup"><span data-stu-id="696a2-122">This means alerting logs are emitted for malicious traffic before applying the other rules (in this case just the default rule - Deny All)</span></span>

### <span data-ttu-id="696a2-123">예제 5: 포트 8080에서 모든 HTTP 트래픽을 허용 하지만 위협으로 식별 된 악의적인 도메인을 차단 하는 방화벽 만들기</span><span class="sxs-lookup"><span data-stu-id="696a2-123">Example 5: Create a Firewall which allows all HTTP traffic on port 8080, but blocks malicious domains identified by Threat Intel</span></span>
```powershell
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"

$rule = New-AzFirewallApplicationRule -Name R1 -Protocol "http:8080" -TargetFqdn "*" 
$ruleCollection = New-AzFirewallApplicationRuleCollection -Name RC1 -Priority 100 -Rule $rule -ActionType "Allow"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -ApplicationRuleCollection $ruleCollection -ThreatIntelMode Deny
```

<span data-ttu-id="696a2-124">이 예제에서는 위협에 의해 악의적으로 간주 되지 않는 경우 포트 8080에서 모든 HTTP 트래픽을 허용 하는 방화벽을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="696a2-124">This example creates a Firewall which allows all HTTP traffic on port 8080 unless it is considered malicious by Threat Intel.</span></span>
<span data-ttu-id="696a2-125">경고와 달리 거부 모드로 실행 하는 경우 위협에 의해 악의적으로 간주 되는 트래픽은 인텔만 기록 되는 것이 아니라 차단 하기도 합니다.</span><span class="sxs-lookup"><span data-stu-id="696a2-125">When running in Deny mode, unlike Alert, traffic considered malicious by Threat Intel is not just logged, but also blocked.</span></span>

### <span data-ttu-id="696a2-126">예제 6: 규칙 및 가용성 영역을 사용 하지 않고 방화벽 만들기</span><span class="sxs-lookup"><span data-stu-id="696a2-126">Example 6: Create a Firewall with no rules and with availability zones</span></span>
```powershell
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetworkName $vnet.Name -PublicIpName $pip.Name -Zone 1,2,3
```

<span data-ttu-id="696a2-127">이 예제에서는 사용 가능한 모든 가용성 영역이 포함 된 방화벽을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="696a2-127">This example creates a Firewall with all available availability zones.</span></span>

### <span data-ttu-id="696a2-128">예제 7: 두 개 이상의 공용 IP 주소를 사용 하 여 방화벽 만들기</span><span class="sxs-lookup"><span data-stu-id="696a2-128">Example 7: Create a Firewall with two or more Public IP Addresses</span></span>
```powershell
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -Name "vnet" -ResourceGroupName $rgName
$pip1 = New-AzPublicIpAddress -Name "AzFwPublicIp1" -ResourceGroupName "rg" -Sku "Standard" -Location "centralus" -AllocationMethod Static
$pip2 = New-AzPublicIpAddress -Name "AzFwPublicIp2" -ResourceGroupName "rg" -Sku "Standard" -Location "centralus" -AllocationMethod Static
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress @($pip1, $pip2)
```

<span data-ttu-id="696a2-129">이 예제에서는 두 개의 공용 IP 주소를 사용 하 여 가상 네트워크 "vnet"에 연결 된 방화벽을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="696a2-129">This example creates a Firewall attached to virtual network "vnet" with two public IP addresses.</span></span>

### <span data-ttu-id="696a2-130">예제 8: 특정 SQL 데이터베이스에 대 한 MSSQL 트래픽을 허용 하는 방화벽 만들기</span><span class="sxs-lookup"><span data-stu-id="696a2-130">Example 8: Create a Firewall which allows MSSQL traffic to specific SQL database</span></span>
```powershell
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"

$rule = New-AzFirewallApplicationRule -Name R1 -Protocol "mssql:1433" -TargetFqdn "sql1.database.windows.net"
$ruleCollection = New-AzFirewallApplicationRuleCollection -Name RC1 -Priority 100 -Rule $rule -ActionType "Allow"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -ApplicationRuleCollection $ruleCollection -ThreatIntelMode Deny
```

<span data-ttu-id="696a2-131">이 예제에서는 표준 포트 1433에서 SQL 데이터베이스 sql1.database.windows.net에 대 한 MSSQL 트래픽을 허용 하는 방화벽을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="696a2-131">This example creates a Firewall which allows MSSQL traffic on standard port 1433 to SQL database sql1.database.windows.net.</span></span>

### <span data-ttu-id="696a2-132">예제 9: 가상 허브에 연결 된 방화벽 만들기</span><span class="sxs-lookup"><span data-stu-id="696a2-132">Example 9: Create a Firewall attached to a virtual hub</span></span>
```powershell
$rgName = "resourceGroupName"
$fp = Get-AzFirewallPolicy -ResourceGroupName $rgName -Name "fp"
$fpId = $fp.Id
$vHub = Get-AzVirtualHub -Name "hub"
$vHubId = $vHub.Id

New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -Sku AZFW_Hub -VirtualHubId $vHubId -FirewallPolicyId -$fpId
```

<span data-ttu-id="696a2-133">이 예제에서는 가상 허브 "vHub"에 연결 된 방화벽을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="696a2-133">This example creates a Firewall attached to virtual hub "vHub".</span></span> <span data-ttu-id="696a2-134">방화벽 정책 $fp 방화벽에 연결 됩니다.</span><span class="sxs-lookup"><span data-stu-id="696a2-134">A firewall policy $fp will be attached to the firewall.</span></span> <span data-ttu-id="696a2-135">이 방화벽은 방화벽 정책 $fp에 명시 된 규칙에 따라 트래픽을 허용 하거나 거부 합니다.</span><span class="sxs-lookup"><span data-stu-id="696a2-135">This firewall allows/denies the traffic based on the rules mentioned in the firewall policy $fp.</span></span> <span data-ttu-id="696a2-136">가상 허브와 방화벽은 동일한 지역에 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="696a2-136">The virtual hub and the firewall should be in the same regions.</span></span>

### <span data-ttu-id="696a2-137">예제 10: 위협 인텔리전스 허용 목록 설치를 사용 하 여 방화벽 만들기</span><span class="sxs-lookup"><span data-stu-id="696a2-137">Example 10: Create a Firewall with threat intelligence whitelist setup</span></span>
```powershell
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"

$tiWhitelist = New-AzFirewallThreatIntelWhitelist -FQDN @("www.microsoft.com") -IpAddresses @("8.8.8.8")
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -ThreatIntelWhitelist $tiWhitelist
```

<span data-ttu-id="696a2-138">이 예제에서는 위협 인텔리전스에서 "www.microsoft.com" 및 "8.8.8.8"를 허용 목록 하는 방화벽을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="696a2-138">This example creates a Firewall that whitelist "www.microsoft.com" and "8.8.8.8" from threat intelligence</span></span>

### <span data-ttu-id="696a2-139">예제 11: 사용자 지정 된 개인 범위 설정으로 방화벽 만들기</span><span class="sxs-lookup"><span data-stu-id="696a2-139">Example 11: Create a Firewall with customized private range setup</span></span>
```powershell
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"

New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -PrivateRange @("99.99.99.0/24", "66.66.0.0/16")
```

<span data-ttu-id="696a2-140">이 예제에서는 "99.99.99.0/24" 및 "66.66.0.0/16"을 개인 ip 범위로 처리 하 고 해당 주소에 대 한 트래픽을 snat 하지 않는 방화벽을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="696a2-140">This example creates a Firewall that treats "99.99.99.0/24" and "66.66.0.0/16" as private ip ranges and won't snat traffic to those addresses</span></span>

### <span data-ttu-id="696a2-141">예제 12: 관리 서브넷 및 공용 IP 주소를 사용 하 여 방화벽 만들기</span><span class="sxs-lookup"><span data-stu-id="696a2-141">Example 12: Create a Firewall with a management subnet and Public IP address</span></span>
```powershell
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"
$mgmtPip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "managementPublicIpName"

New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -ManagementPublicIpAddress $mgmtPip
```

<span data-ttu-id="696a2-142">이 예제에서는 방화벽과 동일한 리소스 그룹의 가상 네트워크 "vnet"에 연결 된 방화벽을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="696a2-142">This example creates a Firewall attached to virtual network "vnet" in the same resource group as the firewall.</span></span>
<span data-ttu-id="696a2-143">규칙은 지정 되지 않았으므로 방화벽은 모든 트래픽을 차단 합니다 (기본 동작).</span><span class="sxs-lookup"><span data-stu-id="696a2-143">Since no rules were specified, the firewall will block all traffic (default behavior).</span></span>
<span data-ttu-id="696a2-144">또한 인텔은 기본적 모드-경고-즉, 악의적인 소통량이 기록 되지만 거부 되지 않음을 의미 합니다.</span><span class="sxs-lookup"><span data-stu-id="696a2-144">Threat Intel will also run in default mode - Alert - which means malicious traffic will be logged, but not denied.</span></span>

<span data-ttu-id="696a2-145">"강제 터널링" 시나리오를 지원 하기 위해이 방화벽은 서브넷 "AzureFirewallManagementSubnet" 및 관리 공개 IP 주소 (관리 트래픽)를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="696a2-145">To support "forced tunneling" scenarios, this firewall will use the subnet "AzureFirewallManagementSubnet" and the management public IP address for its management traffic</span></span>

### <span data-ttu-id="696a2-146">예제 13: 가상 네트워크에 연결 된 방화벽 정책을 사용 하 여 방화벽 만들기</span><span class="sxs-lookup"><span data-stu-id="696a2-146">Example 13: Create a Firewall with Firewall Policy attached to a virtual network</span></span>
```powershell
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"
$fp = Get-AzFirewallPolicy -ResourceGroupName $rgName -Name "fp"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -FirewallPolicyId $fp
```

<span data-ttu-id="696a2-147">이 예제에서는 방화벽과 동일한 리소스 그룹의 가상 네트워크 "vnet"에 연결 된 방화벽을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="696a2-147">This example creates a Firewall attached to virtual network "vnet" in the same resource group as the firewall.</span></span>
<span data-ttu-id="696a2-148">방화벽에 적용 되는 규칙 및 위협 인텔리전스는 방화벽 정책에서 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="696a2-148">The rules and threat intelligence that will be applied to the firewall will be taken from the firewall policy</span></span>

### <span data-ttu-id="696a2-149">예 14: DNS 프록시 및 DNS 서버를 사용 하 여 방화벽 만들기</span><span class="sxs-lookup"><span data-stu-id="696a2-149">Example 14: Create a Firewall with DNS Proxy and DNS Servers</span></span>
```powershell
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -DnsServer @("10.10.10.1", "20.20.20.2")
```

<span data-ttu-id="696a2-150">이 예제에서는 방화벽과 동일한 리소스 그룹의 가상 네트워크 "vnet"에 연결 된 방화벽을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="696a2-150">This example creates a Firewall attached to virtual network "vnet" in the same resource group as the firewall.</span></span>
<span data-ttu-id="696a2-151">이 방화벽에 DNS 프록시를 사용할 수 있으며 2 개의 DNS 서버가 제공 됩니다.</span><span class="sxs-lookup"><span data-stu-id="696a2-151">DNS Proxy is enabled for this firewall and 2 DNS Servers are provided.</span></span> <span data-ttu-id="696a2-152">또한 네트워크 규칙에 대 한 DNS 프록시를 설정 해야 하므로 Fqdn이 있는 네트워크 규칙이 있으면 DNS 프록시를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="696a2-152">Also Require DNS Proxy for Network rules is set so if there are any Network rules with FQDNs then DNS proxy will be used for them too.</span></span>

### <span data-ttu-id="696a2-153">예 15: 여러 개의 Ip를 사용 하 여 방화벽 만들기</span><span class="sxs-lookup"><span data-stu-id="696a2-153">Example 15: Create a Firewall with multiple IPs.</span></span> <span data-ttu-id="696a2-154">방화벽을 가상 허브와 연결할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="696a2-154">The Firewall can be associated with the Virtual Hub</span></span>
```powershell
$rgName = "resourceGroupName"
$vHub = Get-AzVirtualHub -Name "hub"
$vHubId = $vHub.Id
$fwpips = New-AzFirewallHubPublicIpAddress -Count 2
$hubIpAddresses = New-AzFirewallHubIpAddress -PublicIPs $fwpips
$fw=New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location westus -Sku AZFW_Hub -HubIPAddresses $hubIpAddresses -VirtualHubId $vHubId
```

<span data-ttu-id="696a2-155">이 예제에서는 방화벽과 동일한 리소스 그룹에 있는 가상 허브 "허브"에 연결 된 방화벽을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="696a2-155">This example creates a Firewall attached to virtual hub "hub" in the same resource group as the firewall.</span></span>
<span data-ttu-id="696a2-156">방화벽에는 암시적으로 생성 되는 2 개의 공용 Ip가 할당 됩니다.</span><span class="sxs-lookup"><span data-stu-id="696a2-156">The Firewall will be assigned 2 public IPs that are created implicitly.</span></span>

### <span data-ttu-id="696a2-157">16: 액티브 FTP 허용을 사용 하 여 방화벽을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="696a2-157">16:  Create a Firewall with Allow Active FTP.</span></span>
```
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -AllowActiveFTP
```

<span data-ttu-id="696a2-158">이 예제에서는 액티브 FTP 허용 플래그를 사용 하 여 방화벽을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="696a2-158">This example creates a Firewall with allow active FTP flag.</span></span>

## <span data-ttu-id="696a2-159">변수</span><span class="sxs-lookup"><span data-stu-id="696a2-159">PARAMETERS</span></span>

### <span data-ttu-id="696a2-160">-ApplicationRuleCollection</span><span class="sxs-lookup"><span data-stu-id="696a2-160">-ApplicationRuleCollection</span></span>
<span data-ttu-id="696a2-161">새 방화벽에 대 한 응용 프로그램 규칙의 컬렉션을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="696a2-161">Specifies the collections of application rules for the new Firewall.</span></span>

```yaml
Type: PSAzureFirewallApplicationRuleCollection[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="696a2-162">-AsJob</span><span class="sxs-lookup"><span data-stu-id="696a2-162">-AsJob</span></span>
<span data-ttu-id="696a2-163">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="696a2-163">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="696a2-164">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="696a2-164">-DefaultProfile</span></span>
<span data-ttu-id="696a2-165">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="696a2-165">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="696a2-166">-DnsProxyNotRequiredForNetworkRule</span><span class="sxs-lookup"><span data-stu-id="696a2-166">-DnsProxyNotRequiredForNetworkRule</span></span>
<span data-ttu-id="696a2-167">네트워크 규칙 내에서 Fqdn에 대 한 DNS 프록시 기능이 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="696a2-167">Requires DNS Proxy functionality for FQDNs within Network Rules.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="696a2-168">-DnsServer</span><span class="sxs-lookup"><span data-stu-id="696a2-168">-DnsServer</span></span>
<span data-ttu-id="696a2-169">DNS 확인에 사용할 DNS 서버 목록</span><span class="sxs-lookup"><span data-stu-id="696a2-169">The list of DNS Servers to be used for DNS resolution,</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="696a2-170">-EnableDnsProxy</span><span class="sxs-lookup"><span data-stu-id="696a2-170">-EnableDnsProxy</span></span>
<span data-ttu-id="696a2-171">DNS 프록시를 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="696a2-171">Enable DNS Proxy.</span></span> <span data-ttu-id="696a2-172">기본적으로 사용 하지 않도록 설정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="696a2-172">By default it is disabled.</span></span>


```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="696a2-173">-AllowActiveFTP</span><span class="sxs-lookup"><span data-stu-id="696a2-173">-AllowActiveFTP</span></span>
<span data-ttu-id="696a2-174">방화벽에서 액티브 FTP를 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="696a2-174">Allows Active FTP on the Firewall.</span></span> <span data-ttu-id="696a2-175">기본적으로 사용 하지 않도록 설정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="696a2-175">By default it is disabled.</span></span>


```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="696a2-176">-FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="696a2-176">-FirewallPolicyId</span></span>
<span data-ttu-id="696a2-177">방화벽에 연결 된 방화벽 정책</span><span class="sxs-lookup"><span data-stu-id="696a2-177">The firewall policy attached to the firewall</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="696a2-178">-Force</span><span class="sxs-lookup"><span data-stu-id="696a2-178">-Force</span></span>
<span data-ttu-id="696a2-179">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="696a2-179">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="696a2-180">-HubIPAddresses</span><span class="sxs-lookup"><span data-stu-id="696a2-180">-HubIPAddresses</span></span>
<span data-ttu-id="696a2-181">가상 허브에 연결 된 방화벽의 ip 주소</span><span class="sxs-lookup"><span data-stu-id="696a2-181">The ip addresses for the firewall attached to a virtual hub</span></span>

```yaml
Type: PSAzureFirewallHubIpAddresses
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="696a2-182">-위치</span><span class="sxs-lookup"><span data-stu-id="696a2-182">-Location</span></span>
<span data-ttu-id="696a2-183">방화벽의 영역을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="696a2-183">Specifies the region for the Firewall.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="696a2-184">-ManagementPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="696a2-184">-ManagementPublicIpAddress</span></span>
<span data-ttu-id="696a2-185">관리 트래픽에 사용할 하나 이상의 공용 IP 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="696a2-185">One or more Public IP Addresses to use for management traffic.</span></span> <span data-ttu-id="696a2-186">공용 IP 주소는 표준 SKU를 사용 해야 하며 방화벽과 동일한 리소스 그룹에 속해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="696a2-186">The Public IP addresses must use Standard SKU and must belong to the same resource group as the Firewall.</span></span>

```yaml
Type: PSPublicIpAddress
Parameter Sets: IpConfigurationParameterValues
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="696a2-187">-이름</span><span class="sxs-lookup"><span data-stu-id="696a2-187">-Name</span></span>
<span data-ttu-id="696a2-188">이 cmdlet이 만드는 Azure 방화벽의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="696a2-188">Specifies the name of the Azure Firewall that this cmdlet creates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="696a2-189">-NatRuleCollection</span><span class="sxs-lookup"><span data-stu-id="696a2-189">-NatRuleCollection</span></span>
<span data-ttu-id="696a2-190">AzureFirewallNatRuleCollections 목록</span><span class="sxs-lookup"><span data-stu-id="696a2-190">The list of AzureFirewallNatRuleCollections</span></span>

```yaml
Type: PSAzureFirewallNatRuleCollection[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="696a2-191">-NetworkRuleCollection</span><span class="sxs-lookup"><span data-stu-id="696a2-191">-NetworkRuleCollection</span></span>
<span data-ttu-id="696a2-192">AzureFirewallNetworkRuleCollections 목록</span><span class="sxs-lookup"><span data-stu-id="696a2-192">The list of AzureFirewallNetworkRuleCollections</span></span>

```yaml
Type: PSAzureFirewallNetworkRuleCollection[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="696a2-193">-PrivateRange</span><span class="sxs-lookup"><span data-stu-id="696a2-193">-PrivateRange</span></span>
<span data-ttu-id="696a2-194">트래픽이 SNAT'ed 되지 않는 개인 IP 범위</span><span class="sxs-lookup"><span data-stu-id="696a2-194">The private IP ranges to which traffic won't be SNAT'ed</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="696a2-195">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="696a2-195">-PublicIpAddress</span></span>
<span data-ttu-id="696a2-196">하나 이상의 공용 IP 주소</span><span class="sxs-lookup"><span data-stu-id="696a2-196">One or more Public IP Addresses.</span></span> <span data-ttu-id="696a2-197">공용 IP 주소는 표준 SKU를 사용 해야 하며 방화벽과 동일한 리소스 그룹에 속해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="696a2-197">The Public IP addresses must use Standard SKU and must belong to the same resource group as the Firewall.</span></span>

```yaml
Type: PSPublicIpAddress[]
Parameter Sets: IpConfigurationParameterValues
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="696a2-198">-PublicIpName</span><span class="sxs-lookup"><span data-stu-id="696a2-198">-PublicIpName</span></span>
<span data-ttu-id="696a2-199">공용 Ip 이름.</span><span class="sxs-lookup"><span data-stu-id="696a2-199">Public Ip Name.</span></span> <span data-ttu-id="696a2-200">공용 IP는 표준 SKU를 사용 해야 하며 방화벽과 동일한 리소스 그룹에 속해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="696a2-200">The Public IP must use Standard SKU and must belong to the same resource group as the Firewall.</span></span>

```yaml
Type: String
Parameter Sets: OldIpConfigurationParameterValues
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="696a2-201">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="696a2-201">-ResourceGroupName</span></span>
<span data-ttu-id="696a2-202">방화벽을 포함할 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="696a2-202">Specifies the name of a resource group to contain the Firewall.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="696a2-203">-Sku</span><span class="sxs-lookup"><span data-stu-id="696a2-203">-Sku</span></span>
<span data-ttu-id="696a2-204">방화벽의 sku 형식</span><span class="sxs-lookup"><span data-stu-id="696a2-204">The sku type for firewall</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: AZFW_Hub, AZFW_VNet

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="696a2-205">태그</span><span class="sxs-lookup"><span data-stu-id="696a2-205">-Tag</span></span>
<span data-ttu-id="696a2-206">해시 테이블 형태의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="696a2-206">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="696a2-207">예를 들어:</span><span class="sxs-lookup"><span data-stu-id="696a2-207">For example:</span></span>

<span data-ttu-id="696a2-208">@ {key0 = "value0", key1 = $null, key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="696a2-208">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="696a2-209">-ThreatIntelMode</span><span class="sxs-lookup"><span data-stu-id="696a2-209">-ThreatIntelMode</span></span>
<span data-ttu-id="696a2-210">위협 인텔리전스에 대 한 작동 모드를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="696a2-210">Specifies the operation mode for Threat Intelligence.</span></span> <span data-ttu-id="696a2-211">기본 모드는 해제 되지 않고 경고입니다.</span><span class="sxs-lookup"><span data-stu-id="696a2-211">Default mode is Alert, not Off.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Alert, Deny, Off

Required: False
Position: Named
Default value: Alert
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="696a2-212">-ThreatIntelWhitelist</span><span class="sxs-lookup"><span data-stu-id="696a2-212">-ThreatIntelWhitelist</span></span>
<span data-ttu-id="696a2-213">위협 인텔리전스의 허용 목록</span><span class="sxs-lookup"><span data-stu-id="696a2-213">The whitelist for Threat Intelligence</span></span>

```yaml
Type: PSAzureFirewallThreatIntelWhitelist
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="696a2-214">-VirtualHubId</span><span class="sxs-lookup"><span data-stu-id="696a2-214">-VirtualHubId</span></span>
<span data-ttu-id="696a2-215">방화벽이 연결 된 가상 허브</span><span class="sxs-lookup"><span data-stu-id="696a2-215">The virtual hub that a firewall is attached to</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="696a2-216">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="696a2-216">-VirtualNetwork</span></span>
<span data-ttu-id="696a2-217">가상 네트워크</span><span class="sxs-lookup"><span data-stu-id="696a2-217">Virtual Network</span></span>

```yaml
Type: PSVirtualNetwork
Parameter Sets: IpConfigurationParameterValues
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="696a2-218">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="696a2-218">-VirtualNetworkName</span></span>
<span data-ttu-id="696a2-219">방화벽을 배포할 가상 네트워크의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="696a2-219">Specifies the name of the virtual network for which the Firewall will be deployed.</span></span> <span data-ttu-id="696a2-220">가상 네트워크와 방화벽은 동일한 리소스 그룹에 속해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="696a2-220">Virtual network and Firewall must belong to the same resource group.</span></span>

```yaml
Type: String
Parameter Sets: OldIpConfigurationParameterValues
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="696a2-221">-Zone</span><span class="sxs-lookup"><span data-stu-id="696a2-221">-Zone</span></span>
<span data-ttu-id="696a2-222">방화벽을 시작 해야 하는 위치를 나타내는 가용성 영역의 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="696a2-222">A list of availability zones denoting where the firewall needs to come from.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="696a2-223">-확인</span><span class="sxs-lookup"><span data-stu-id="696a2-223">-Confirm</span></span>
<span data-ttu-id="696a2-224">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="696a2-224">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="696a2-225">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="696a2-225">-WhatIf</span></span>
<span data-ttu-id="696a2-226">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="696a2-226">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="696a2-227">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="696a2-227">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="696a2-228">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="696a2-228">CommonParameters</span></span>
<span data-ttu-id="696a2-229">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="696a2-229">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="696a2-230">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="696a2-230">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="696a2-231">입력</span><span class="sxs-lookup"><span data-stu-id="696a2-231">INPUTS</span></span>

### <span data-ttu-id="696a2-232">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="696a2-232">System.String</span></span>

### <span data-ttu-id="696a2-233">PSVirtualNetwork에 대 한.</span><span class="sxs-lookup"><span data-stu-id="696a2-233">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

### <span data-ttu-id="696a2-234">PSPublicIpAddress [] (으)로</span><span class="sxs-lookup"><span data-stu-id="696a2-234">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress[]</span></span>

### <span data-ttu-id="696a2-235">PSPublicIpAddress에 대 한.</span><span class="sxs-lookup"><span data-stu-id="696a2-235">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

### <span data-ttu-id="696a2-236">PSAzureFirewallApplicationRuleCollection [] (으)로</span><span class="sxs-lookup"><span data-stu-id="696a2-236">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallApplicationRuleCollection[]</span></span>

### <span data-ttu-id="696a2-237">PSAzureFirewallNatRuleCollection [] (으)로</span><span class="sxs-lookup"><span data-stu-id="696a2-237">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNatRuleCollection[]</span></span>

### <span data-ttu-id="696a2-238">PSAzureFirewallNetworkRuleCollection [] (으)로</span><span class="sxs-lookup"><span data-stu-id="696a2-238">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRuleCollection[]</span></span>

### <span data-ttu-id="696a2-239">System.webserver. 컬렉션 테이블</span><span class="sxs-lookup"><span data-stu-id="696a2-239">System.Collections.Hashtable</span></span>

## <span data-ttu-id="696a2-240">출력</span><span class="sxs-lookup"><span data-stu-id="696a2-240">OUTPUTS</span></span>

### <span data-ttu-id="696a2-241">Microsoft. \* PSAzureFirewall</span><span class="sxs-lookup"><span data-stu-id="696a2-241">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span></span>

## <span data-ttu-id="696a2-242">상속자</span><span class="sxs-lookup"><span data-stu-id="696a2-242">NOTES</span></span>

## <span data-ttu-id="696a2-243">관련 링크</span><span class="sxs-lookup"><span data-stu-id="696a2-243">RELATED LINKS</span></span>

[<span data-ttu-id="696a2-244">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="696a2-244">Get-AzFirewall</span></span>](./Get-AzFirewall.md)

[<span data-ttu-id="696a2-245">제거-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="696a2-245">Remove-AzFirewall</span></span>](./Remove-AzFirewall.md)

[<span data-ttu-id="696a2-246">Set-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="696a2-246">Set-AzFirewall</span></span>](./Set-AzFirewall.md)

[<span data-ttu-id="696a2-247">새로운 AzFirewallApplicationRuleCollection</span><span class="sxs-lookup"><span data-stu-id="696a2-247">New-AzFirewallApplicationRuleCollection</span></span>](./New-AzFirewallApplicationRuleCollection.md)

[<span data-ttu-id="696a2-248">새로운 AzFirewallNatRuleCollection</span><span class="sxs-lookup"><span data-stu-id="696a2-248">New-AzFirewallNatRuleCollection</span></span>](./New-AzFirewallNatRuleCollection.md)

[<span data-ttu-id="696a2-249">새로운 AzFirewallNetworkRuleCollection</span><span class="sxs-lookup"><span data-stu-id="696a2-249">New-AzFirewallNetworkRuleCollection</span></span>](./New-AzFirewallNetworkRuleCollection.md)
