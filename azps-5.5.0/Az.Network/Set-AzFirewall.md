---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 40E56EC1-3327-4DFF-8262-E2EEBB5E4447
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azfirewall
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzFirewall.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzFirewall.md
ms.openlocfilehash: 1ab3d82b494d5598081ea229a7ae50d486b8ca20
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100189521"
---
# <span data-ttu-id="06de5-101">Set-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="06de5-101">Set-AzFirewall</span></span>

## <span data-ttu-id="06de5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="06de5-102">SYNOPSIS</span></span>
<span data-ttu-id="06de5-103">수정된 방화벽을 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="06de5-103">Saves a modified Firewall.</span></span>

## <span data-ttu-id="06de5-104">구문</span><span class="sxs-lookup"><span data-stu-id="06de5-104">SYNTAX</span></span>

```
Set-AzFirewall -AzureFirewall <PSAzureFirewall> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="06de5-105">설명</span><span class="sxs-lookup"><span data-stu-id="06de5-105">DESCRIPTION</span></span>
<span data-ttu-id="06de5-106">**Set-AzFirewall** cmdlet은 Azure Firewall을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="06de5-106">The **Set-AzFirewall** cmdlet updates an Azure Firewall.</span></span>

## <span data-ttu-id="06de5-107">예제</span><span class="sxs-lookup"><span data-stu-id="06de5-107">EXAMPLES</span></span>

### <span data-ttu-id="06de5-108">1: 방화벽 애플리케이션 규칙 컬렉션의 업데이트 우선 순위</span><span class="sxs-lookup"><span data-stu-id="06de5-108">1:  Update priority of a Firewall application rule collection</span></span>
```
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$ruleCollection = $azFw.GetApplicationRuleCollectionByName("ruleCollectionName")
$ruleCollection.Priority = 101
Set-AzFirewall -AzureFirewall $azFw
```

<span data-ttu-id="06de5-109">이 예제에서는 Azure Firewall의 기존 규칙 컬렉션의 우선 순위를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="06de5-109">This example updates the priority of an existing rule collection of an Azure Firewall.</span></span>
<span data-ttu-id="06de5-110">리소스 그룹 "rg"의 Azure Firewall "AzureFirewall"에 "ruleCollectionName"이라는 애플리케이션 규칙 컬렉션이 포함되어 있는 경우 위의 명령은 해당 규칙 컬렉션의 우선 순위를 변경하고 이후에 Azure Firewall을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="06de5-110">Assuming Azure Firewall "AzureFirewall" in resource group "rg" contains an application rule collection named "ruleCollectionName", the commands above will change the priority of that rule collection and update the Azure Firewall afterwards.</span></span> <span data-ttu-id="06de5-111">Set-AzFirewall 경우 로컬 $azFw 개체에서 수행된 모든 작업은 서버에 반영되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="06de5-111">Without the Set-AzFirewall command, all operations performed on the local $azFw object are not reflected on the server.</span></span>

### <span data-ttu-id="06de5-112">2: Azure Firewall 만들기 및 나중에 애플리케이션 규칙 컬렉션 설정</span><span class="sxs-lookup"><span data-stu-id="06de5-112">2:  Create a Azure Firewall and set an application rule collection later</span></span>
```
$azFw = New-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg" -VirtualNetworkName "vnet-name" -PublicIpName "pip-name"

$rule = New-AzFirewallApplicationRule -Name R1 -Protocol "http:80","https:443" -TargetFqdn "*google.com", "*microsoft.com" -SourceAddress "10.0.0.0"
$RuleCollection = New-AzFirewallApplicationRuleCollection -Name RC1 -Priority 100 -Rule $rule -ActionType "Allow"
$azFw.ApplicationRuleCollections = $RuleCollection

$azFw | Set-AzFirewall
```

<span data-ttu-id="06de5-113">이 예제에서는 애플리케이션 규칙 컬렉션 없이 방화벽이 먼저 만들어집니다.</span><span class="sxs-lookup"><span data-stu-id="06de5-113">In this example, a Firewall is created first without any application rule collections.</span></span> <span data-ttu-id="06de5-114">그런 다음 애플리케이션 규칙 및 애플리케이션 규칙 컬렉션이 생성되면 클라우드의 실제 구성에 영향을 주지 않고 메모리에서 방화벽 개체가 수정됩니다.</span><span class="sxs-lookup"><span data-stu-id="06de5-114">Afterwards a Application Rule and Application Rule Collection are created, then the Firewall object is modified in memory, without affecting the real configuration in cloud.</span></span> <span data-ttu-id="06de5-115">변경 내용을 클라우드에 반영하려면 Set-AzFirewall 호출해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="06de5-115">For changes to be reflected in cloud, Set-AzFirewall must be called.</span></span>

### <span data-ttu-id="06de5-116">3: Azure Firewall의 위협 Intel 작업 모드 업데이트</span><span class="sxs-lookup"><span data-stu-id="06de5-116">3:  Update Threat Intel operation mode of Azure Firewall</span></span>
```
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$azFw.ThreatIntelMode = "Deny"
Set-AzFirewall -Firewall $azFw
```

<span data-ttu-id="06de5-117">이 예제에서는 리소스 그룹 "rg"에서 Azure Firewall "AzureFirewall"의 Threat Intel 작업 모드를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="06de5-117">This example updates the Threat Intel operation mode of Azure Firewall "AzureFirewall" in resource group "rg".</span></span>
<span data-ttu-id="06de5-118">Set-AzFirewall 경우 로컬 $azFw 개체에서 수행된 모든 작업은 서버에 반영되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="06de5-118">Without the Set-AzFirewall command, all operations performed on the local $azFw object are not reflected on the server.</span></span>

### <span data-ttu-id="06de5-119">4: 방화벽 할당을 할당해제 및 할당</span><span class="sxs-lookup"><span data-stu-id="06de5-119">4: Deallocate and allocate the Firewall</span></span>
```
$firewall=Get-AzFirewall -ResourceGroupName rgName -Name azFw
$firewall.Deallocate()
$firewall | Set-AzFirewall

$vnet = Get-AzVirtualNetwork -ResourceGroupName rgName -Name anotherVNetName
$pip = Get-AzPublicIpAddress -ResourceGroupName rgName -Name publicIpName
$firewall.Allocate($vnet, $pip)
$firewall | Set-AzFirewall
```
<span data-ttu-id="06de5-120">이 예제에서는 방화벽을 검색하고, 방화벽의 재배치 및 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="06de5-120">This example retrieves a Firewall, deallocates the firewall, and saves it.</span></span> <span data-ttu-id="06de5-121">Deallocate 명령은 실행 중인 서비스를 제거하지만 방화벽의 구성은 보존합니다.</span><span class="sxs-lookup"><span data-stu-id="06de5-121">The Deallocate command removes the running service but preserves the firewall's configuration.</span></span> <span data-ttu-id="06de5-122">변경 내용을 클라우드에 반영하려면 Set-AzFirewall 호출해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="06de5-122">For changes to be reflected in cloud, Set-AzFirewall must be called.</span></span>
<span data-ttu-id="06de5-123">사용자가 서비스를 다시 시작하려는 경우 방화벽에서 Allocate 메서드를 호출해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="06de5-123">If user wants to start the service again, the Allocate method should be called on the firewall.</span></span>
<span data-ttu-id="06de5-124">새 VNet 및 공용 IP는 방화벽과 동일한 리소스 그룹에 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="06de5-124">The new VNet and Public IP must be in the same resource group as the Firewall.</span></span> <span data-ttu-id="06de5-125">다시, 클라우드에 변경 내용을 반영하려면 Set-AzFirewall 합니다.</span><span class="sxs-lookup"><span data-stu-id="06de5-125">Again, for changes to be reflected in cloud, Set-AzFirewall must be called.</span></span>

### <span data-ttu-id="06de5-126">5: 강제 터널링 시나리오에 대한 관리 공용 IP 주소로 할당</span><span class="sxs-lookup"><span data-stu-id="06de5-126">5: Allocate with a management public IP address for forced tunneling scenarios</span></span>
```
$vnet = Get-AzVirtualNetwork -ResourceGroupName rgName -Name anotherVNetName
$pip = Get-AzPublicIpAddress -ResourceGroupName rgName -Name publicIpName
$mgmtPip = Get-AzPublicIpAddress -ResourceGroupName rgName -Name MgmtPublicIpName
$firewall.Allocate($vnet, $pip, $mgmtPip)
$firewall | Set-AzFirewall
```
<span data-ttu-id="06de5-127">이 예제에서는 강제 터널링 시나리오에 대한 관리 공용 IP 주소 및 서브넷을 통해 방화벽을 할당합니다.</span><span class="sxs-lookup"><span data-stu-id="06de5-127">This example allocates the firewall with a management public IP address and subnet for forced tunneling scenarios.</span></span> <span data-ttu-id="06de5-128">VNet은 "AzureFirewallManagementSubnet"이라는 서브넷을 포함해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="06de5-128">The VNet must contain a subnet called "AzureFirewallManagementSubnet".</span></span>

### <span data-ttu-id="06de5-129">6: Azure Firewall에 공용 IP 주소 추가</span><span class="sxs-lookup"><span data-stu-id="06de5-129">6:  Add a Public IP address to an Azure Firewall</span></span>
```
$pip = New-AzPublicIpAddress -Name "azFwPublicIp1" -ResourceGroupName "rg" -Sku "Standard" -Location "centralus" -AllocationMethod Static
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$azFw.AddPublicIpAddress($pip)

$azFw | Set-AzFirewall
```

<span data-ttu-id="06de5-130">이 예제에서는 방화벽에 연결된 공용 IP 주소 "azFwPublicIp1"입니다.</span><span class="sxs-lookup"><span data-stu-id="06de5-130">In this example, the Public IP Address "azFwPublicIp1" as attached to the Firewall.</span></span>

### <span data-ttu-id="06de5-131">7: Azure Firewall에서 공용 IP 주소 제거</span><span class="sxs-lookup"><span data-stu-id="06de5-131">7:  Remove a Public IP address from an Azure Firewall</span></span>
```
$pip = Get-AzPublicIpAddress -Name "azFwPublicIp1" -ResourceGroupName "rg"
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$azFw.RemovePublicIpAddress($pip)

$azFw | Set-AzFirewall
```

<span data-ttu-id="06de5-132">이 예제에서는 방화벽에서 "azFwPublicIp1" 공용 IP 주소가 연결됩니다.</span><span class="sxs-lookup"><span data-stu-id="06de5-132">In this example, the Public IP Address "azFwPublicIp1" as detached from the Firewall.</span></span>

### <span data-ttu-id="06de5-133">8: Azure Firewall에서 관리 공용 IP 주소 변경</span><span class="sxs-lookup"><span data-stu-id="06de5-133">8:  Change the management public IP address on an Azure Firewall</span></span>
```
$newMgmtPip = New-AzPublicIpAddress -Name "azFwMgmtPublicIp2" -ResourceGroupName "rg" -Sku "Standard" -Location "centralus" -AllocationMethod Static
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$azFw.ManagementIpConfiguration.PublicIpAddress = $newMgmtPip

$azFw | Set-AzFirewall
```

<span data-ttu-id="06de5-134">이 예제에서는 방화벽의 관리 공용 IP 주소가 "AzFwMgmtPublicIp2"로 변경됩니다.</span><span class="sxs-lookup"><span data-stu-id="06de5-134">In this example, the management public IP address of the firewall will be changed to "AzFwMgmtPublicIp2"</span></span>

### <span data-ttu-id="06de5-135">9: Azure Firewall에 DNS 구성 추가</span><span class="sxs-lookup"><span data-stu-id="06de5-135">9:  Add DNS configuration to an Azure Firewall</span></span>
```
$dnsServers = @("10.10.10.1", "20.20.20.2")
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$azFw.DNSEnableProxy = $true
$azFw.DNSServer = $dnsServers

$azFw | Set-AzFirewall
```

<span data-ttu-id="06de5-136">이 예제에서는 DNS 프록시 및 DNS 서버 구성이 방화벽에 연결됩니다.</span><span class="sxs-lookup"><span data-stu-id="06de5-136">In this example, DNS Proxy and DNS Server configuration is attached to the Firewall.</span></span>

### <span data-ttu-id="06de5-137">10: 방화벽 애플리케이션 규칙 컬렉션 내에서 기존 규칙의 대상 업데이트</span><span class="sxs-lookup"><span data-stu-id="06de5-137">10: Update destination of an existing rule within a Firewall application rule collection</span></span>
```
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$ruleCollection = $azFw.GetNetworkRuleCollectionByName("ruleCollectionName")
$rule=$ruleCollection.GetRuleByName("ruleName")
$rule.DestinationAddresses = "10.10.10.10"
Set-AzFirewall -AzureFirewall $azFw
```

<span data-ttu-id="06de5-138">이 예제에서는 Azure Firewall의 규칙 컬렉션 내에서 기존 규칙의 대상을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="06de5-138">This example updates the destination of an existing rule within a rule collection of an Azure Firewall.</span></span> <span data-ttu-id="06de5-139">이렇게 하면 IP 주소가 동적으로 변경될 때 규칙을 자동으로 업데이트할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="06de5-139">This allows you to automatically update your rules when IP addresses change dynamically.</span></span>

### <span data-ttu-id="06de5-140">11: Azure Firewall에서 활성 FTP 허용</span><span class="sxs-lookup"><span data-stu-id="06de5-140">11: Allow Active FTP on Azure Firewall</span></span>
```
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$azFw.AllowActiveFTP = $true

$azFw | Set-AzFirewall
```

<span data-ttu-id="06de5-141">이 예제에서는 방화벽에서 활성 FTP가 허용됩니다.</span><span class="sxs-lookup"><span data-stu-id="06de5-141">In this example, Active FTP is allowed on the Firewall.</span></span>

## <span data-ttu-id="06de5-142">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="06de5-142">PARAMETERS</span></span>

### <span data-ttu-id="06de5-143">-AsJob</span><span class="sxs-lookup"><span data-stu-id="06de5-143">-AsJob</span></span>
<span data-ttu-id="06de5-144">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="06de5-144">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="06de5-145">-AzureFirewall</span><span class="sxs-lookup"><span data-stu-id="06de5-145">-AzureFirewall</span></span>
<span data-ttu-id="06de5-146">The AzureFirewall</span><span class="sxs-lookup"><span data-stu-id="06de5-146">The AzureFirewall</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSAzureFirewall
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="06de5-147">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06de5-147">-DefaultProfile</span></span>
<span data-ttu-id="06de5-148">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="06de5-148">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="06de5-149">-Confirm</span><span class="sxs-lookup"><span data-stu-id="06de5-149">-Confirm</span></span>
<span data-ttu-id="06de5-150">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="06de5-150">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06de5-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="06de5-151">-WhatIf</span></span>
<span data-ttu-id="06de5-152">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="06de5-152">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="06de5-153">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="06de5-153">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06de5-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06de5-154">CommonParameters</span></span>
<span data-ttu-id="06de5-155">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="06de5-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06de5-156">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="06de5-156">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06de5-157">입력</span><span class="sxs-lookup"><span data-stu-id="06de5-157">INPUTS</span></span>

### <span data-ttu-id="06de5-158">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span><span class="sxs-lookup"><span data-stu-id="06de5-158">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span></span>

## <span data-ttu-id="06de5-159">출력</span><span class="sxs-lookup"><span data-stu-id="06de5-159">OUTPUTS</span></span>

### <span data-ttu-id="06de5-160">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span><span class="sxs-lookup"><span data-stu-id="06de5-160">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span></span>

## <span data-ttu-id="06de5-161">참고 사항</span><span class="sxs-lookup"><span data-stu-id="06de5-161">NOTES</span></span>

## <span data-ttu-id="06de5-162">관련 링크</span><span class="sxs-lookup"><span data-stu-id="06de5-162">RELATED LINKS</span></span>

[<span data-ttu-id="06de5-163">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="06de5-163">Get-AzFirewall</span></span>](./Get-AzFirewall.md)

[<span data-ttu-id="06de5-164">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="06de5-164">New-AzFirewall</span></span>](./New-AzFirewall.md)

[<span data-ttu-id="06de5-165">Remove-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="06de5-165">Remove-AzFirewall</span></span>](./Remove-AzFirewall.md)
