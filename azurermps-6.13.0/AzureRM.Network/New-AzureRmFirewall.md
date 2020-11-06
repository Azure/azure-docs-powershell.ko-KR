---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: A3D60CF1-2E66-4EE5-9C68-932DD8DF80BD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermfirewall
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmFirewall.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmFirewall.md
ms.openlocfilehash: 6486c7db87e8c71b0703b90a765fa30287b82769
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93536588"
---
# <span data-ttu-id="3f092-101">New-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="3f092-101">New-AzureRmFirewall</span></span>

## <span data-ttu-id="3f092-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3f092-102">SYNOPSIS</span></span>
<span data-ttu-id="3f092-103">리소스 그룹에 새 방화벽을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="3f092-103">Creates a new Firewall in a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3f092-104">구문과</span><span class="sxs-lookup"><span data-stu-id="3f092-104">SYNTAX</span></span>

```
New-AzureRmFirewall -Name <String> -ResourceGroupName <String> -Location <String>
 [-VirtualNetworkName <String>] [-PublicIpName <String>]
 [-ApplicationRuleCollection <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSAzureFirewallApplicationRuleCollection]>]
 [-NatRuleCollection <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNatRuleCollection]>]
 [-NetworkRuleCollection <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRuleCollection]>]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3f092-105">설명은</span><span class="sxs-lookup"><span data-stu-id="3f092-105">DESCRIPTION</span></span>
<span data-ttu-id="3f092-106">**새 AzureRmFirewall** Cmdlet은 Azure 방화벽을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="3f092-106">The **New-AzureRmFirewall** cmdlet creates an Azure Firewall.</span></span>

## <span data-ttu-id="3f092-107">예제의</span><span class="sxs-lookup"><span data-stu-id="3f092-107">EXAMPLES</span></span>

### <span data-ttu-id="3f092-108">1: 가상 네트워크에 연결 된 방화벽 만들기</span><span class="sxs-lookup"><span data-stu-id="3f092-108">1:  Create a Firewall attached to a virtual network</span></span>
```
New-AzureRmFirewall -Name "azFw" -ResourceGroupName "rg" -Location centralus -VirtualNetworkName "vnet" -PublicIpName "pip-name"
```

<span data-ttu-id="3f092-109">이 예제에서는 방화벽과 동일한 리소스 그룹의 가상 네트워크 "vnet"에 연결 된 방화벽을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="3f092-109">This example creates a Firewall attached to virtual network "vnet" in the same resource group as the firewall.</span></span>
<span data-ttu-id="3f092-110">규칙은 지정 되지 않았으므로 방화벽은 모든 트래픽을 차단 합니다 (기본 동작).</span><span class="sxs-lookup"><span data-stu-id="3f092-110">Since no rules were specified, the firewall will block all traffic (default behavior).</span></span>

### <span data-ttu-id="3f092-111">2: 모든 HTTPS 트래픽을 허용 하는 방화벽 만들기</span><span class="sxs-lookup"><span data-stu-id="3f092-111">2:  Create a Firewall which allows all HTTPS traffic</span></span>
```
$rule = New-AzureRmFirewallApplicationRule -Name R1 -Protocol "https:443" -TargetFqdn "*" 
$ruleCollection = New-AzureRmFirewallApplicationRuleCollection -Name RC1 -Priority 100 -Rule $rule -ActionType "Allow"
New-AzureRmFirewall -Name "azFw" -ResourceGroupName "rg" -Location centralus -VirtualNetworkName "vnet" -PublicIpName "pip-name" -ApplicationRuleCollection $ruleCollection
```

<span data-ttu-id="3f092-112">이 예제에서는 포트 443에서 모든 HTTPS 트래픽을 허용 하는 방화벽을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="3f092-112">This example creates a Firewall which allows all HTTPS traffic on port 443.</span></span>

### <span data-ttu-id="3f092-113">3:10.1.2.3:80으로 전송 되는 DNAT 리디렉션 트래픽을 10.2.3.4:8080으로</span><span class="sxs-lookup"><span data-stu-id="3f092-113">3:  DNAT - redirect traffic destined to 10.1.2.3:80 to 10.2.3.4:8080</span></span>
```
$rule = New-AzureRmFirewallNatRule -Name "natRule" -Protocol "TCP" -SourceAddress "*" -DestinationAddress "10.1.2.3" -DestinationPort "80" -TranslatedAddress "10.2.3.4" -TranslatedPort "8080"
$ruleCollection = New-AzureRmFirewallNatRuleCollection -Name "NatRuleCollection" -Priority 1000 -Rule $rule
New-AzureRmFirewall -Name "azFw" -ResourceGroupName "rg" -Location centralus -NatRuleCollection $ruleCollection
```

<span data-ttu-id="3f092-114">이 예제에서는 10.1.2.3:80으로 보내는 모든 패킷의 대상 IP 및 포트를 10.2.3.4:8080으로 변환 하는 방화벽을 만들었습니다.</span><span class="sxs-lookup"><span data-stu-id="3f092-114">This example created a Firewall which translated the destination IP and port of all packets destined to 10.1.2.3:80 to 10.2.3.4:8080</span></span>

## <span data-ttu-id="3f092-115">변수</span><span class="sxs-lookup"><span data-stu-id="3f092-115">PARAMETERS</span></span>

### <span data-ttu-id="3f092-116">-ApplicationRuleCollection</span><span class="sxs-lookup"><span data-stu-id="3f092-116">-ApplicationRuleCollection</span></span>
<span data-ttu-id="3f092-117">새 방화벽에 대 한 응용 프로그램 규칙의 컬렉션을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3f092-117">Specifies the collections of application rules for the new Firewall.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSAzureFirewallApplicationRuleCollection]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3f092-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3f092-118">-AsJob</span></span>
<span data-ttu-id="3f092-119">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="3f092-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3f092-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f092-120">-DefaultProfile</span></span>
<span data-ttu-id="3f092-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3f092-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f092-122">-Force</span><span class="sxs-lookup"><span data-stu-id="3f092-122">-Force</span></span>
<span data-ttu-id="3f092-123">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="3f092-123">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="3f092-124">-위치</span><span class="sxs-lookup"><span data-stu-id="3f092-124">-Location</span></span>
<span data-ttu-id="3f092-125">방화벽의 영역을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3f092-125">Specifies the region for the Firewall.</span></span>

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

### <span data-ttu-id="3f092-126">-이름</span><span class="sxs-lookup"><span data-stu-id="3f092-126">-Name</span></span>
<span data-ttu-id="3f092-127">이 cmdlet이 만드는 Azure 방화벽의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3f092-127">Specifies the name of the Azure Firewall that this cmdlet creates.</span></span>

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

### <span data-ttu-id="3f092-128">-NatRuleCollection</span><span class="sxs-lookup"><span data-stu-id="3f092-128">-NatRuleCollection</span></span>
<span data-ttu-id="3f092-129">AzureFirewallNatRuleCollections 목록</span><span class="sxs-lookup"><span data-stu-id="3f092-129">The list of AzureFirewallNatRuleCollections</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNatRuleCollection]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3f092-130">-NetworkRuleCollection</span><span class="sxs-lookup"><span data-stu-id="3f092-130">-NetworkRuleCollection</span></span>
<span data-ttu-id="3f092-131">AzureFirewallNetworkRuleCollections 목록</span><span class="sxs-lookup"><span data-stu-id="3f092-131">The list of AzureFirewallNetworkRuleCollections</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRuleCollection]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3f092-132">-PublicIpName</span><span class="sxs-lookup"><span data-stu-id="3f092-132">-PublicIpName</span></span>
<span data-ttu-id="3f092-133">공용 Ip 이름.</span><span class="sxs-lookup"><span data-stu-id="3f092-133">Public Ip Name.</span></span> <span data-ttu-id="3f092-134">공용 IP는 표준 SKU를 사용 해야 하며 방화벽과 동일한 리소스 그룹에 속해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="3f092-134">The Public IP must use Standard SKU and must belong to the same resource group as the Firewall.</span></span>

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

### <span data-ttu-id="3f092-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3f092-135">-ResourceGroupName</span></span>
<span data-ttu-id="3f092-136">방화벽을 포함할 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3f092-136">Specifies the name of a resource group to contain the Firewall.</span></span>

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

### <span data-ttu-id="3f092-137">태그</span><span class="sxs-lookup"><span data-stu-id="3f092-137">-Tag</span></span>
<span data-ttu-id="3f092-138">해시 테이블 형태의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="3f092-138">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="3f092-139">예를 들어:</span><span class="sxs-lookup"><span data-stu-id="3f092-139">For example:</span></span>

<span data-ttu-id="3f092-140">@ {key0 = "value0", key1 = $null, key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="3f092-140">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="3f092-141">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="3f092-141">-VirtualNetworkName</span></span>
<span data-ttu-id="3f092-142">방화벽을 배포할 가상 네트워크의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3f092-142">Specifies the name of the virtual network for which the Firewall will be deployed.</span></span> <span data-ttu-id="3f092-143">가상 네트워크와 방화벽은 동일한 리소스 그룹에 속해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="3f092-143">Virtual network and Firewall must belong to the same resource group.</span></span>

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

### <span data-ttu-id="3f092-144">-확인</span><span class="sxs-lookup"><span data-stu-id="3f092-144">-Confirm</span></span>
<span data-ttu-id="3f092-145">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="3f092-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3f092-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3f092-146">-WhatIf</span></span>
<span data-ttu-id="3f092-147">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="3f092-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3f092-148">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3f092-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3f092-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f092-149">CommonParameters</span></span>
<span data-ttu-id="3f092-150">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="3f092-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f092-151">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3f092-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f092-152">입력</span><span class="sxs-lookup"><span data-stu-id="3f092-152">INPUTS</span></span>

### <span data-ttu-id="3f092-153">않아야</span><span class="sxs-lookup"><span data-stu-id="3f092-153">None</span></span>
<span data-ttu-id="3f092-154">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3f092-154">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="3f092-155">출력</span><span class="sxs-lookup"><span data-stu-id="3f092-155">OUTPUTS</span></span>

### <span data-ttu-id="3f092-156">Microsoft. 네트워크. 모델. m i a 방화벽</span><span class="sxs-lookup"><span data-stu-id="3f092-156">Microsoft.Azure.Commands.Network.Models.PSFirewall</span></span>

## <span data-ttu-id="3f092-157">상속자</span><span class="sxs-lookup"><span data-stu-id="3f092-157">NOTES</span></span>

## <span data-ttu-id="3f092-158">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3f092-158">RELATED LINKS</span></span>

[<span data-ttu-id="3f092-159">Get-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="3f092-159">Get-AzureRmFirewall</span></span>](./Get-AzureRmFirewall.md)

[<span data-ttu-id="3f092-160">제거-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="3f092-160">Remove-AzureRmFirewall</span></span>](./Remove-AzureRmFirewall.md)

[<span data-ttu-id="3f092-161">Set-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="3f092-161">Set-AzureRmFirewall</span></span>](./Set-AzureRmFirewall.md)

[<span data-ttu-id="3f092-162">새로운 AzureRmFirewallApplicationRuleCollection</span><span class="sxs-lookup"><span data-stu-id="3f092-162">New-AzureRmFirewallApplicationRuleCollection</span></span>](./New-AzureRmFirewallApplicationRuleCollection.md)

[<span data-ttu-id="3f092-163">새로운 AzureRmFirewallNatRuleCollection</span><span class="sxs-lookup"><span data-stu-id="3f092-163">New-AzureRmFirewallNatRuleCollection</span></span>](./New-AzureRmFirewallNatRuleCollection.md)

[<span data-ttu-id="3f092-164">새로운 AzureRmFirewallNetworkRuleCollection</span><span class="sxs-lookup"><span data-stu-id="3f092-164">New-AzureRmFirewallNetworkRuleCollection</span></span>](./New-AzureRmFirewallNetworkRuleCollection.md)
