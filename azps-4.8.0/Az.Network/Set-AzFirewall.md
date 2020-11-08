---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 40E56EC1-3327-4DFF-8262-E2EEBB5E4447
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azfirewall
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzFirewall.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzFirewall.md
ms.openlocfilehash: 9ef4d8f2638fdb853fa83b896bb51f95d1ef119e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94214777"
---
# <span data-ttu-id="9cc68-101">Set-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="9cc68-101">Set-AzFirewall</span></span>

## <span data-ttu-id="9cc68-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9cc68-102">SYNOPSIS</span></span>
<span data-ttu-id="9cc68-103">수정 된 방화벽을 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="9cc68-103">Saves a modified Firewall.</span></span>

## <span data-ttu-id="9cc68-104">구문과</span><span class="sxs-lookup"><span data-stu-id="9cc68-104">SYNTAX</span></span>

```
Set-AzFirewall -AzureFirewall <PSAzureFirewall> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9cc68-105">설명은</span><span class="sxs-lookup"><span data-stu-id="9cc68-105">DESCRIPTION</span></span>
<span data-ttu-id="9cc68-106">**AzFirewall** Cmdlet은 Azure 방화벽을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="9cc68-106">The **Set-AzFirewall** cmdlet updates an Azure Firewall.</span></span>

## <span data-ttu-id="9cc68-107">예제의</span><span class="sxs-lookup"><span data-stu-id="9cc68-107">EXAMPLES</span></span>

### <span data-ttu-id="9cc68-108">1: 방화벽 응용 프로그램 규칙 모음의 우선 순위 업데이트</span><span class="sxs-lookup"><span data-stu-id="9cc68-108">1:  Update priority of a Firewall application rule collection</span></span>
```
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$ruleCollection = $azFw.GetApplicationRuleCollectionByName("ruleCollectionName")
$ruleCollection.Priority = 101
Set-AzFirewall -AzureFirewall $azFw
```

<span data-ttu-id="9cc68-109">이 예제에서는 Azure 방화벽의 기존 규칙 컬렉션에 대 한 우선 순위를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="9cc68-109">This example updates the priority of an existing rule collection of an Azure Firewall.</span></span>
<span data-ttu-id="9cc68-110">"Rg" 리소스 그룹의 Azure 방화벽 "AzureFirewall"에 "ruleCollectionName" 이라는 응용 프로그램 규칙 컬렉션이 포함 되어 있는 경우 위의 명령은 해당 규칙 모음의 우선 순위를 변경 하 고 나중에 Azure 방화벽을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="9cc68-110">Assuming Azure Firewall "AzureFirewall" in resource group "rg" contains an application rule collection named "ruleCollectionName", the commands above will change the priority of that rule collection and update the Azure Firewall afterwards.</span></span> <span data-ttu-id="9cc68-111">Set-AzFirewall 명령이 없으면 로컬 $azFw 개체에서 수행 된 모든 작업이 서버에 반영 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9cc68-111">Without the Set-AzFirewall command, all operations performed on the local $azFw object are not reflected on the server.</span></span>

### <span data-ttu-id="9cc68-112">2: Azure 방화벽을 만들고 나중에 응용 프로그램 규칙 컬렉션 설정</span><span class="sxs-lookup"><span data-stu-id="9cc68-112">2:  Create a Azure Firewall and set an application rule collection later</span></span>
```
$azFw = New-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg" -VirtualNetworkName "vnet-name" -PublicIpName "pip-name"

$rule = New-AzFirewallApplicationRule -Name R1 -Protocol "http:80","https:443" -TargetFqdn "*google.com", "*microsoft.com" -SourceAddress "10.0.0.0"
$RuleCollection = New-AzFirewallApplicationRuleCollection -Name RC1 -Priority 100 -Rule $rule -ActionType "Allow"
$azFw.ApplicationRuleCollections = $RuleCollection

$azFw | Set-AzFirewall
```

<span data-ttu-id="9cc68-113">이 예제에서는 응용 프로그램 규칙 컬렉션 없이 방화벽을 먼저 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9cc68-113">In this example, a Firewall is created first without any application rule collections.</span></span> <span data-ttu-id="9cc68-114">나중에 응용 프로그램 규칙과 응용 프로그램 규칙 컬렉션이 만들어지고, 방화벽 개체는 클라우드의 실제 구성에 영향을 주지 않고 메모리에서 수정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9cc68-114">Afterwards a Application Rule and Application Rule Collection are created, then the Firewall object is modified in memory, without affecting the real configuration in cloud.</span></span> <span data-ttu-id="9cc68-115">클라우드에 변경 내용을 반영 하려면 Set-AzFirewall를 호출 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="9cc68-115">For changes to be reflected in cloud, Set-AzFirewall must be called.</span></span>

### <span data-ttu-id="9cc68-116">3: Azure 방화벽의 위협 업데이트 인텔 작동 모드</span><span class="sxs-lookup"><span data-stu-id="9cc68-116">3:  Update Threat Intel operation mode of Azure Firewall</span></span>
```
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$azFw.ThreatIntelMode = "Deny"
Set-AzFirewall -Firewall $azFw
```

<span data-ttu-id="9cc68-117">이 예제에서는 리소스 그룹 "rg"에서 Azure 방화벽 "AzureFirewall"의 위협 Intel 작업 모드를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="9cc68-117">This example updates the Threat Intel operation mode of Azure Firewall "AzureFirewall" in resource group "rg".</span></span>
<span data-ttu-id="9cc68-118">Set-AzFirewall 명령이 없으면 로컬 $azFw 개체에서 수행 된 모든 작업이 서버에 반영 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9cc68-118">Without the Set-AzFirewall command, all operations performed on the local $azFw object are not reflected on the server.</span></span>

### <span data-ttu-id="9cc68-119">4: 방화벽을 할당 취소 하 고 할당</span><span class="sxs-lookup"><span data-stu-id="9cc68-119">4: Deallocate and allocate the Firewall</span></span>
```
$firewall=Get-AzFirewall -ResourceGroupName rgName -Name azFw
$firewall.Deallocate()
$firewall | Set-AzFirewall

$vnet = Get-AzVirtualNetwork -ResourceGroupName rgName -Name anotherVNetName
$pip = Get-AzPublicIpAddress - ResourceGroupName rgName -Name publicIpName
$firewall.Allocate($vnet, $pip)
$firewall | Set-AzFirewall
```
<span data-ttu-id="9cc68-120">이 예제에서는 방화벽을 검색 하 고 방화벽을 할당 해제 한 다음 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="9cc68-120">This example retrieves a Firewall, deallocates the firewall, and saves it.</span></span> <span data-ttu-id="9cc68-121">할당 취소 명령은 실행 중인 서비스를 제거 하지만 방화벽 구성을 유지 합니다.</span><span class="sxs-lookup"><span data-stu-id="9cc68-121">The Deallocate command removes the running service but preserves the firewall's configuration.</span></span> <span data-ttu-id="9cc68-122">클라우드에 변경 내용을 반영 하려면 Set-AzFirewall를 호출 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="9cc68-122">For changes to be reflected in cloud, Set-AzFirewall must be called.</span></span>
<span data-ttu-id="9cc68-123">사용자가 서비스를 다시 시작 하려고 하면 방화벽에서 Allocate 메서드를 호출 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="9cc68-123">If user wants to start the service again, the Allocate method should be called on the firewall.</span></span>
<span data-ttu-id="9cc68-124">새 VNet 및 공용 IP는 방화벽과 동일한 리소스 그룹에 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="9cc68-124">The new VNet and Public IP must be in the same resource group as the Firewall.</span></span> <span data-ttu-id="9cc68-125">이번에도 클라우드에 변경 내용을 반영 하려면 Set-AzFirewall를 호출 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="9cc68-125">Again, for changes to be reflected in cloud, Set-AzFirewall must be called.</span></span>

### <span data-ttu-id="9cc68-126">5: 관리 공개 IP 주소를 사용 하 여 강제 터널링 시나리오에 할당</span><span class="sxs-lookup"><span data-stu-id="9cc68-126">5: Allocate with a management public IP address for forced tunneling scenarios</span></span>
```
$vnet = Get-AzVirtualNetwork -ResourceGroupName rgName -Name anotherVNetName
$pip = Get-AzPublicIpAddress - ResourceGroupName rgName -Name publicIpName
$mgmtPip = Get-AzPublicIpAddress - ResourceGroupName rgName -Name MgmtPublicIpName
$firewall.Allocate($vnet, $pip, $mgmtPip)
$firewall | Set-AzFirewall
```
<span data-ttu-id="9cc68-127">이 예제에서는 강제 터널링 시나리오를 위해 관리 공용 IP 주소와 서브넷을 사용 하 여 방화벽을 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="9cc68-127">This example allocates the firewall with a management public IP address and subnet for forced tunneling scenarios.</span></span> <span data-ttu-id="9cc68-128">VNet에는 "AzureFirewallManagementSubnet" 이라는 서브넷이 포함 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="9cc68-128">The VNet must contain a subnet called "AzureFirewallManagementSubnet".</span></span>

### <span data-ttu-id="9cc68-129">6: 공용 IP 주소를 Azure 방화벽에 추가</span><span class="sxs-lookup"><span data-stu-id="9cc68-129">6:  Add a Public IP address to an Azure Firewall</span></span>
```
$pip = New-AzPublicIpAddress -Name "azFwPublicIp1" -ResourceGroupName "rg" -Sku "Standard" -Location "centralus" -AllocationMethod Static
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$azFw.AddPublicIpAddress($pip)

$azFw | Set-AzFirewall
```

<span data-ttu-id="9cc68-130">이 예제에서 공개 IP 주소 "azFwPublicIp1"는 방화벽에 연결 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9cc68-130">In this example, the Public IP Address "azFwPublicIp1" as attached to the Firewall.</span></span>

### <span data-ttu-id="9cc68-131">7: Azure 방화벽에서 공용 IP 주소 제거</span><span class="sxs-lookup"><span data-stu-id="9cc68-131">7:  Remove a Public IP address from an Azure Firewall</span></span>
```
$pip = Get-AzPublicIpAddress -Name "azFwPublicIp1" -ResourceGroupName "rg"
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$azFw.RemovePublicIpAddress($pip)

$azFw | Set-AzFirewall
```

<span data-ttu-id="9cc68-132">이 예제에서는 공개 IP 주소 "azFwPublicIp1"가 방화벽에서 분리 된 것으로 처리 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9cc68-132">In this example, the Public IP Address "azFwPublicIp1" as detached from the Firewall.</span></span>

### <span data-ttu-id="9cc68-133">8: Azure 방화벽에서 관리 공개 IP 주소 변경</span><span class="sxs-lookup"><span data-stu-id="9cc68-133">8:  Change the management public IP address on an Azure Firewall</span></span>
```
$newMgmtPip = New-AzPublicIpAddress -Name "azFwMgmtPublicIp2" -ResourceGroupName "rg" -Sku "Standard" -Location "centralus" -AllocationMethod Static
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$azFw.ManagementIpConfiguration.PublicIpAddress = $newMgmtPip

$azFw | Set-AzFirewall
```

<span data-ttu-id="9cc68-134">이 예제에서는 방화벽의 관리 공용 IP 주소를 "AzFwMgmtPublicIp2"로 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="9cc68-134">In this example, the management public IP address of the firewall will be changed to "AzFwMgmtPublicIp2"</span></span>

### <span data-ttu-id="9cc68-135">9: Azure 방화벽에 DNS 구성 추가</span><span class="sxs-lookup"><span data-stu-id="9cc68-135">9:  Add DNS configuration to an Azure Firewall</span></span>
```
$dnsServers = @("10.10.10.1", "20.20.20.2")
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$azFw.DNSEnableProxy = $true
$azFw.DNSServer = $dnsServers

$azFw | Set-AzFirewall
```

<span data-ttu-id="9cc68-136">이 예제에서는 DNS 프록시와 DNS 서버 구성이 방화벽에 연결 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9cc68-136">In this example, DNS Proxy and DNS Server configuration is attached to the Firewall.</span></span>

### <span data-ttu-id="9cc68-137">10: 방화벽 응용 프로그램 규칙 모음 내에서 기존 규칙의 대상 업데이트</span><span class="sxs-lookup"><span data-stu-id="9cc68-137">10: Update destination of an existing rule within a Firewall application rule collection</span></span>
```
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$ruleCollection = $azFw.GetNetworkRuleCollectionByName("ruleCollectionName")
$rule=$ruleCollection.GetRuleByName("ruleName")
$rule.DestinationAddresses="10.10.10.10"
Set-AzFirewall -AzureFirewall $azFw
```

<span data-ttu-id="9cc68-138">이 예제에서는 Azure 방화벽의 규칙 컬렉션 내에서 기존 규칙의 대상을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="9cc68-138">This example updates the destination of an existing rule within a rule collection of an Azure Firewall.</span></span> <span data-ttu-id="9cc68-139">이렇게 하면 IP 주소가 동적으로 변경 될 때 규칙을 자동으로 업데이트할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9cc68-139">This allows you to automatically update your rules when IP addresses change dynamically.</span></span>

### <span data-ttu-id="9cc68-140">11: Azure 방화벽에서 액티브 FTP 허용</span><span class="sxs-lookup"><span data-stu-id="9cc68-140">11: Allow Active FTP on Azure Firewall</span></span>
```
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$azFw.AllowActiveFTP = $true

$azFw | Set-AzFirewall
```

<span data-ttu-id="9cc68-141">이 예제에서는 활성 FTP를 방화벽에서 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9cc68-141">In this example, Active FTP is allowed on the Firewall.</span></span>

## <span data-ttu-id="9cc68-142">변수</span><span class="sxs-lookup"><span data-stu-id="9cc68-142">PARAMETERS</span></span>

### <span data-ttu-id="9cc68-143">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9cc68-143">-AsJob</span></span>
<span data-ttu-id="9cc68-144">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="9cc68-144">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9cc68-145">-AzureFirewall</span><span class="sxs-lookup"><span data-stu-id="9cc68-145">-AzureFirewall</span></span>
<span data-ttu-id="9cc68-146">AzureFirewall</span><span class="sxs-lookup"><span data-stu-id="9cc68-146">The AzureFirewall</span></span>

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

### <span data-ttu-id="9cc68-147">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9cc68-147">-DefaultProfile</span></span>
<span data-ttu-id="9cc68-148">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9cc68-148">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9cc68-149">-확인</span><span class="sxs-lookup"><span data-stu-id="9cc68-149">-Confirm</span></span>
<span data-ttu-id="9cc68-150">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="9cc68-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9cc68-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9cc68-151">-WhatIf</span></span>
<span data-ttu-id="9cc68-152">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="9cc68-152">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9cc68-153">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9cc68-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9cc68-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9cc68-154">CommonParameters</span></span>
<span data-ttu-id="9cc68-155">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9cc68-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9cc68-156">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9cc68-156">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9cc68-157">입력</span><span class="sxs-lookup"><span data-stu-id="9cc68-157">INPUTS</span></span>

### <span data-ttu-id="9cc68-158">Microsoft. \* PSAzureFirewall</span><span class="sxs-lookup"><span data-stu-id="9cc68-158">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span></span>

## <span data-ttu-id="9cc68-159">출력</span><span class="sxs-lookup"><span data-stu-id="9cc68-159">OUTPUTS</span></span>

### <span data-ttu-id="9cc68-160">Microsoft. \* PSAzureFirewall</span><span class="sxs-lookup"><span data-stu-id="9cc68-160">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span></span>

## <span data-ttu-id="9cc68-161">상속자</span><span class="sxs-lookup"><span data-stu-id="9cc68-161">NOTES</span></span>

## <span data-ttu-id="9cc68-162">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9cc68-162">RELATED LINKS</span></span>

[<span data-ttu-id="9cc68-163">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="9cc68-163">Get-AzFirewall</span></span>](./Get-AzFirewall.md)

[<span data-ttu-id="9cc68-164">새로운 AzFirewall</span><span class="sxs-lookup"><span data-stu-id="9cc68-164">New-AzFirewall</span></span>](./New-AzFirewall.md)

[<span data-ttu-id="9cc68-165">제거-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="9cc68-165">Remove-AzFirewall</span></span>](./Remove-AzFirewall.md)
