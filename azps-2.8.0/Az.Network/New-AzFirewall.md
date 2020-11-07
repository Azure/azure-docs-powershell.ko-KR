---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A3D60CF1-2E66-4EE5-9C68-932DD8DF80BD
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewall
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewall.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewall.md
ms.openlocfilehash: 8d8d3ce0a236acb511eac715385b53c821f1dceb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93869949"
---
# <span data-ttu-id="340eb-101">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="340eb-101">New-AzFirewall</span></span>

## <span data-ttu-id="340eb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="340eb-102">SYNOPSIS</span></span>
<span data-ttu-id="340eb-103">리소스 그룹에 새 방화벽을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="340eb-103">Creates a new Firewall in a resource group.</span></span>

## <span data-ttu-id="340eb-104">구문과</span><span class="sxs-lookup"><span data-stu-id="340eb-104">SYNTAX</span></span>

### <span data-ttu-id="340eb-105">기본값 (기본값)</span><span class="sxs-lookup"><span data-stu-id="340eb-105">Default (Default)</span></span>
```
New-AzFirewall -Name <String> -ResourceGroupName <String> -Location <String>
 [-ApplicationRuleCollection <PSAzureFirewallApplicationRuleCollection[]>]
 [-NatRuleCollection <PSAzureFirewallNatRuleCollection[]>]
 [-NetworkRuleCollection <PSAzureFirewallNetworkRuleCollection[]>] [-Zone <String[]>] [-ThreatIntelMode <String>]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="340eb-106">OldIpConfigurationParameterValues</span><span class="sxs-lookup"><span data-stu-id="340eb-106">OldIpConfigurationParameterValues</span></span>
```
New-AzFirewall -Name <String> -ResourceGroupName <String> -Location <String> -VirtualNetworkName <String>
 -PublicIpName <String> [-ApplicationRuleCollection <PSAzureFirewallApplicationRuleCollection[]>]
 [-NatRuleCollection <PSAzureFirewallNatRuleCollection[]>]
 [-NetworkRuleCollection <PSAzureFirewallNetworkRuleCollection[]>] [-Zone <String[]>] [-ThreatIntelMode <String>]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="340eb-107">IpConfigurationParameterValues</span><span class="sxs-lookup"><span data-stu-id="340eb-107">IpConfigurationParameterValues</span></span>
```
New-AzFirewall -Name <String> -ResourceGroupName <String> -Location <String> -VirtualNetwork <PSVirtualNetwork>
 -PublicIpAddress <PSPublicIpAddress[]>
 [-ApplicationRuleCollection <PSAzureFirewallApplicationRuleCollection[]>]
 [-NatRuleCollection <PSAzureFirewallNatRuleCollection[]>]
 [-NetworkRuleCollection <PSAzureFirewallNetworkRuleCollection[]>] [-ThreatIntelMode <String>]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="340eb-108">설명은</span><span class="sxs-lookup"><span data-stu-id="340eb-108">DESCRIPTION</span></span>
<span data-ttu-id="340eb-109">**새 AzFirewall** Cmdlet은 Azure 방화벽을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="340eb-109">The **New-AzFirewall** cmdlet creates an Azure Firewall.</span></span>

## <span data-ttu-id="340eb-110">예제의</span><span class="sxs-lookup"><span data-stu-id="340eb-110">EXAMPLES</span></span>

### <span data-ttu-id="340eb-111">1: 가상 네트워크에 연결 된 방화벽 만들기</span><span class="sxs-lookup"><span data-stu-id="340eb-111">1:  Create a Firewall attached to a virtual network</span></span>
```
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip
```

<span data-ttu-id="340eb-112">이 예제에서는 방화벽과 동일한 리소스 그룹의 가상 네트워크 "vnet"에 연결 된 방화벽을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="340eb-112">This example creates a Firewall attached to virtual network "vnet" in the same resource group as the firewall.</span></span>
<span data-ttu-id="340eb-113">규칙은 지정 되지 않았으므로 방화벽은 모든 트래픽을 차단 합니다 (기본 동작).</span><span class="sxs-lookup"><span data-stu-id="340eb-113">Since no rules were specified, the firewall will block all traffic (default behavior).</span></span>
<span data-ttu-id="340eb-114">또한 인텔은 기본적 모드-경고-즉, 악의적인 소통량이 기록 되지만 거부 되지 않음을 의미 합니다.</span><span class="sxs-lookup"><span data-stu-id="340eb-114">Threat Intel will also run in default mode - Alert - which means malicious traffic will be logged, but not denied.</span></span>

### <span data-ttu-id="340eb-115">2: 모든 HTTPS 트래픽을 허용 하는 방화벽 만들기</span><span class="sxs-lookup"><span data-stu-id="340eb-115">2:  Create a Firewall which allows all HTTPS traffic</span></span>
```
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"

$rule = New-AzFirewallApplicationRule -Name R1 -Protocol "https:443" -TargetFqdn "*" 
$ruleCollection = New-AzFirewallApplicationRuleCollection -Name RC1 -Priority 100 -Rule $rule -ActionType "Allow"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -ApplicationRuleCollection $ruleCollection
```

<span data-ttu-id="340eb-116">이 예제에서는 포트 443에서 모든 HTTPS 트래픽을 허용 하는 방화벽을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="340eb-116">This example creates a Firewall which allows all HTTPS traffic on port 443.</span></span>
<span data-ttu-id="340eb-117">인텔은 기본 모드-경고-알림-악의적인 트래픽이 기록 되지만 거부 되지 않음을 의미 합니다.</span><span class="sxs-lookup"><span data-stu-id="340eb-117">Threat Intel will run in default mode - Alert - which means malicious traffic will be logged, but not denied.</span></span>

### <span data-ttu-id="340eb-118">3:10.1.2.3:80으로 전송 되는 DNAT 리디렉션 트래픽을 10.2.3.4:8080으로</span><span class="sxs-lookup"><span data-stu-id="340eb-118">3:  DNAT - redirect traffic destined to 10.1.2.3:80 to 10.2.3.4:8080</span></span>
```
$rule = New-AzFirewallNatRule -Name "natRule" -Protocol "TCP" -SourceAddress "*" -DestinationAddress "10.1.2.3" -DestinationPort "80" -TranslatedAddress "10.2.3.4" -TranslatedPort "8080"
$ruleCollection = New-AzFirewallNatRuleCollection -Name "NatRuleCollection" -Priority 1000 -Rule $rule
New-AzFirewall -Name "azFw" -ResourceGroupName "rg" -Location centralus -NatRuleCollection $ruleCollection -ThreatIntelMode Off
```

<span data-ttu-id="340eb-119">이 예제에서는 10.1.2.3:80으로 보내는 모든 패킷의 대상 IP 및 포트를 10.2.3.4:8080 위협으로 변환 하는 방화벽을 만들었습니다 .이 예제에서는 Intel이 해제 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="340eb-119">This example created a Firewall which translated the destination IP and port of all packets destined to 10.1.2.3:80 to 10.2.3.4:8080 Threat Intel is turned off in this example.</span></span>

### <span data-ttu-id="340eb-120">4: 규칙을 사용 하지 않고 위협에 대 한 방화벽 만들기 (경고 모드의 경우)</span><span class="sxs-lookup"><span data-stu-id="340eb-120">4:  Create a Firewall with no rules and with Threat Intel in Alert mode</span></span>
```
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -ThreatIntelMode Alert
```

<span data-ttu-id="340eb-121">이 예제에서는 모든 트래픽을 차단 하는 방화벽을 만들고 (기본 동작) 위협 Intel이 알림 모드로 실행 되 고 있습니다.</span><span class="sxs-lookup"><span data-stu-id="340eb-121">This example creates a Firewall which blocks all traffic (default behavior) and has Threat Intel running in Alert mode.</span></span>
<span data-ttu-id="340eb-122">즉,이 경우에는 다른 규칙을 적용 하기 전에 악의적인 트래픽에 대 한 경고 로그가 생성 됩니다 (이 경우에는 기본 규칙-모두 거부만 해당).</span><span class="sxs-lookup"><span data-stu-id="340eb-122">This means alerting logs are emitted for malicious traffic before applying the other rules (in this case just the default rule - Deny All)</span></span>

### <span data-ttu-id="340eb-123">5: 포트 8080에서 모든 HTTP 트래픽을 허용 하지만 위협으로 식별 된 악의적인 도메인을 차단 하는 방화벽 만들기</span><span class="sxs-lookup"><span data-stu-id="340eb-123">5:  Create a Firewall which allows all HTTP traffic on port 8080, but blocks malicious domains identified by Threat Intel</span></span>
```
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"

$rule = New-AzFirewallApplicationRule -Name R1 -Protocol "http:8080" -TargetFqdn "*" 
$ruleCollection = New-AzFirewallApplicationRuleCollection -Name RC1 -Priority 100 -Rule $rule -ActionType "Allow"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -ApplicationRuleCollection $ruleCollection -ThreatIntelMode Deny
```

<span data-ttu-id="340eb-124">이 예제에서는 위협에 의해 악의적으로 간주 되지 않는 경우 포트 8080에서 모든 HTTP 트래픽을 허용 하는 방화벽을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="340eb-124">This example creates a Firewall which allows all HTTP traffic on port 8080 unless it is considered malicious by Threat Intel.</span></span>
<span data-ttu-id="340eb-125">경고와 달리 거부 모드로 실행 하는 경우 위협에 의해 악의적으로 간주 되는 트래픽은 인텔만 기록 되는 것이 아니라 차단 하기도 합니다.</span><span class="sxs-lookup"><span data-stu-id="340eb-125">When running in Deny mode, unlike Alert, traffic considered malicious by Threat Intel is not just logged, but also blocked.</span></span>

### <span data-ttu-id="340eb-126">6: 규칙 및 가용성 영역을 사용 하지 않고 방화벽 만들기</span><span class="sxs-lookup"><span data-stu-id="340eb-126">6:  Create a Firewall with no rules and with availability zones</span></span>
```
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetworkName $vnet.Name -PublicIpName $pip.Name -Zone 1,2,3
```

<span data-ttu-id="340eb-127">이 예제에서는 사용 가능한 모든 가용성 영역이 포함 된 방화벽을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="340eb-127">This example creates a Firewall with all available availability zones.</span></span>

### <span data-ttu-id="340eb-128">7: 두 개 이상의 공용 IP 주소를 사용 하 여 방화벽 만들기</span><span class="sxs-lookup"><span data-stu-id="340eb-128">7: Create a Firewall with two or more Public IP Addresses</span></span>
```
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -Name "vnet" -ResourceGroupName $rgName
$pip1 = New-AzPublicIpAddress -Name "AzFwPublicIp1" -ResourceGroupName "rg" -Sku "Standard" -Location "centralus" -AllocationMethod Static
$pip2 = New-AzPublicIpAddress -Name "AzFwPublicIp2" -ResourceGroupName "rg" -Sku "Standard" -Location "centralus" -AllocationMethod Static
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress @($pip1, $pip2)
```

<span data-ttu-id="340eb-129">이 예제에서는 두 개의 공용 IP 주소를 사용 하 여 가상 네트워크 "vnet"에 연결 된 방화벽을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="340eb-129">This example creates a Firewall attached to virtual network "vnet" with two public IP addresses.</span></span>

### <span data-ttu-id="340eb-130">8: 특정 SQL 데이터베이스에 대 한 MSSQL 트래픽을 허용 하는 방화벽 만들기</span><span class="sxs-lookup"><span data-stu-id="340eb-130">8: Create a Firewall which allows MSSQL traffic to specific SQL database</span></span>
```
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"

$rule = New-AzFirewallApplicationRule -Name R1 -Protocol "mssql:1433" -TargetFqdn "sql1.database.windows.net"
$ruleCollection = New-AzFirewallApplicationRuleCollection -Name RC1 -Priority 100 -Rule $rule -ActionType "Allow"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -ApplicationRuleCollection $ruleCollection -ThreatIntelMode Deny
```

<span data-ttu-id="340eb-131">이 예제에서는 표준 포트 1433에서 SQL 데이터베이스 sql1.database.windows.net에 대 한 MSSQL 트래픽을 허용 하는 방화벽을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="340eb-131">This example creates a Firewall which allows MSSQL traffic on standard port 1433 to SQL database sql1.database.windows.net.</span></span>

## <span data-ttu-id="340eb-132">변수</span><span class="sxs-lookup"><span data-stu-id="340eb-132">PARAMETERS</span></span>

### <span data-ttu-id="340eb-133">-ApplicationRuleCollection</span><span class="sxs-lookup"><span data-stu-id="340eb-133">-ApplicationRuleCollection</span></span>
<span data-ttu-id="340eb-134">새 방화벽에 대 한 응용 프로그램 규칙의 컬렉션을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="340eb-134">Specifies the collections of application rules for the new Firewall.</span></span>

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

### <span data-ttu-id="340eb-135">-AsJob</span><span class="sxs-lookup"><span data-stu-id="340eb-135">-AsJob</span></span>
<span data-ttu-id="340eb-136">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="340eb-136">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="340eb-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="340eb-137">-DefaultProfile</span></span>
<span data-ttu-id="340eb-138">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="340eb-138">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="340eb-139">-Force</span><span class="sxs-lookup"><span data-stu-id="340eb-139">-Force</span></span>
<span data-ttu-id="340eb-140">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="340eb-140">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="340eb-141">-위치</span><span class="sxs-lookup"><span data-stu-id="340eb-141">-Location</span></span>
<span data-ttu-id="340eb-142">방화벽의 영역을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="340eb-142">Specifies the region for the Firewall.</span></span>

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

### <span data-ttu-id="340eb-143">-이름</span><span class="sxs-lookup"><span data-stu-id="340eb-143">-Name</span></span>
<span data-ttu-id="340eb-144">이 cmdlet이 만드는 Azure 방화벽의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="340eb-144">Specifies the name of the Azure Firewall that this cmdlet creates.</span></span>

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

### <span data-ttu-id="340eb-145">-NatRuleCollection</span><span class="sxs-lookup"><span data-stu-id="340eb-145">-NatRuleCollection</span></span>
<span data-ttu-id="340eb-146">AzureFirewallNatRuleCollections 목록</span><span class="sxs-lookup"><span data-stu-id="340eb-146">The list of AzureFirewallNatRuleCollections</span></span>

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

### <span data-ttu-id="340eb-147">-NetworkRuleCollection</span><span class="sxs-lookup"><span data-stu-id="340eb-147">-NetworkRuleCollection</span></span>
<span data-ttu-id="340eb-148">AzureFirewallNetworkRuleCollections 목록</span><span class="sxs-lookup"><span data-stu-id="340eb-148">The list of AzureFirewallNetworkRuleCollections</span></span>

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

### <span data-ttu-id="340eb-149">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="340eb-149">-PublicIpAddress</span></span>
<span data-ttu-id="340eb-150">하나 이상의 공용 IP 주소</span><span class="sxs-lookup"><span data-stu-id="340eb-150">One or more Public IP Addresses.</span></span> <span data-ttu-id="340eb-151">공용 IP 주소는 표준 SKU를 사용 해야 하며 방화벽과 동일한 리소스 그룹에 속해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="340eb-151">The Public IP addresses must use Standard SKU and must belong to the same resource group as the Firewall.</span></span>

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

### <span data-ttu-id="340eb-152">-PublicIpName</span><span class="sxs-lookup"><span data-stu-id="340eb-152">-PublicIpName</span></span>
<span data-ttu-id="340eb-153">공용 Ip 이름.</span><span class="sxs-lookup"><span data-stu-id="340eb-153">Public Ip Name.</span></span> <span data-ttu-id="340eb-154">공용 IP는 표준 SKU를 사용 해야 하며 방화벽과 동일한 리소스 그룹에 속해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="340eb-154">The Public IP must use Standard SKU and must belong to the same resource group as the Firewall.</span></span>

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

### <span data-ttu-id="340eb-155">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="340eb-155">-ResourceGroupName</span></span>
<span data-ttu-id="340eb-156">방화벽을 포함할 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="340eb-156">Specifies the name of a resource group to contain the Firewall.</span></span>

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

### <span data-ttu-id="340eb-157">-Zone</span><span class="sxs-lookup"><span data-stu-id="340eb-157">-Zone</span></span>
<span data-ttu-id="340eb-158">방화벽을 시작 해야 하는 위치를 나타내는 가용성 영역의 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="340eb-158">A list of availability zones denoting where the firewall needs to come from.</span></span>

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

### <span data-ttu-id="340eb-159">태그</span><span class="sxs-lookup"><span data-stu-id="340eb-159">-Tag</span></span>
<span data-ttu-id="340eb-160">해시 테이블 형태의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="340eb-160">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="340eb-161">예를 들어:</span><span class="sxs-lookup"><span data-stu-id="340eb-161">For example:</span></span>

<span data-ttu-id="340eb-162">@ {key0 = "value0", key1 = $null, key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="340eb-162">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="340eb-163">-ThreatIntelMode</span><span class="sxs-lookup"><span data-stu-id="340eb-163">-ThreatIntelMode</span></span>
<span data-ttu-id="340eb-164">위협 인텔리전스에 대 한 작동 모드를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="340eb-164">Specifies the operation mode for Threat Intelligence.</span></span> <span data-ttu-id="340eb-165">기본 모드는 해제 되지 않고 경고입니다.</span><span class="sxs-lookup"><span data-stu-id="340eb-165">Default mode is Alert, not Off.</span></span>

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

### <span data-ttu-id="340eb-166">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="340eb-166">-VirtualNetwork</span></span>
<span data-ttu-id="340eb-167">가상 네트워크</span><span class="sxs-lookup"><span data-stu-id="340eb-167">Virtual Network</span></span>

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

### <span data-ttu-id="340eb-168">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="340eb-168">-VirtualNetworkName</span></span>
<span data-ttu-id="340eb-169">방화벽을 배포할 가상 네트워크의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="340eb-169">Specifies the name of the virtual network for which the Firewall will be deployed.</span></span> <span data-ttu-id="340eb-170">가상 네트워크와 방화벽은 동일한 리소스 그룹에 속해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="340eb-170">Virtual network and Firewall must belong to the same resource group.</span></span>

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

### <span data-ttu-id="340eb-171">-확인</span><span class="sxs-lookup"><span data-stu-id="340eb-171">-Confirm</span></span>
<span data-ttu-id="340eb-172">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="340eb-172">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="340eb-173">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="340eb-173">-WhatIf</span></span>
<span data-ttu-id="340eb-174">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="340eb-174">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="340eb-175">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="340eb-175">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="340eb-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="340eb-176">CommonParameters</span></span>
<span data-ttu-id="340eb-177">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="340eb-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="340eb-178">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="340eb-178">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="340eb-179">입력</span><span class="sxs-lookup"><span data-stu-id="340eb-179">INPUTS</span></span>

### <span data-ttu-id="340eb-180">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="340eb-180">System.String</span></span>

### <span data-ttu-id="340eb-181">PSVirtualNetwork에 대 한.</span><span class="sxs-lookup"><span data-stu-id="340eb-181">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

### <span data-ttu-id="340eb-182">PSPublicIpAddress [] (으)로</span><span class="sxs-lookup"><span data-stu-id="340eb-182">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress[]</span></span>

### <span data-ttu-id="340eb-183">PSAzureFirewallApplicationRuleCollection [] (으)로</span><span class="sxs-lookup"><span data-stu-id="340eb-183">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallApplicationRuleCollection[]</span></span>

### <span data-ttu-id="340eb-184">PSAzureFirewallNatRuleCollection [] (으)로</span><span class="sxs-lookup"><span data-stu-id="340eb-184">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNatRuleCollection[]</span></span>

### <span data-ttu-id="340eb-185">PSAzureFirewallNetworkRuleCollection [] (으)로</span><span class="sxs-lookup"><span data-stu-id="340eb-185">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRuleCollection[]</span></span>

### <span data-ttu-id="340eb-186">System.webserver. 컬렉션 테이블</span><span class="sxs-lookup"><span data-stu-id="340eb-186">System.Collections.Hashtable</span></span>

## <span data-ttu-id="340eb-187">출력</span><span class="sxs-lookup"><span data-stu-id="340eb-187">OUTPUTS</span></span>

### <span data-ttu-id="340eb-188">Microsoft. \* PSAzureFirewall</span><span class="sxs-lookup"><span data-stu-id="340eb-188">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span></span>

## <span data-ttu-id="340eb-189">상속자</span><span class="sxs-lookup"><span data-stu-id="340eb-189">NOTES</span></span>

## <span data-ttu-id="340eb-190">관련 링크</span><span class="sxs-lookup"><span data-stu-id="340eb-190">RELATED LINKS</span></span>

[<span data-ttu-id="340eb-191">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="340eb-191">Get-AzFirewall</span></span>](./Get-AzFirewall.md)

[<span data-ttu-id="340eb-192">제거-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="340eb-192">Remove-AzFirewall</span></span>](./Remove-AzFirewall.md)

[<span data-ttu-id="340eb-193">Set-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="340eb-193">Set-AzFirewall</span></span>](./Set-AzFirewall.md)

[<span data-ttu-id="340eb-194">새로운 AzFirewallApplicationRuleCollection</span><span class="sxs-lookup"><span data-stu-id="340eb-194">New-AzFirewallApplicationRuleCollection</span></span>](./New-AzFirewallApplicationRuleCollection.md)

[<span data-ttu-id="340eb-195">새로운 AzFirewallNatRuleCollection</span><span class="sxs-lookup"><span data-stu-id="340eb-195">New-AzFirewallNatRuleCollection</span></span>](./New-AzFirewallNatRuleCollection.md)

[<span data-ttu-id="340eb-196">새로운 AzFirewallNetworkRuleCollection</span><span class="sxs-lookup"><span data-stu-id="340eb-196">New-AzFirewallNetworkRuleCollection</span></span>](./New-AzFirewallNetworkRuleCollection.md)
