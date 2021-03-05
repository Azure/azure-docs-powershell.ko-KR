---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C0E1D4DF-232F-49C6-BE4C-05C8E8038329
online version: https://docs.microsoft.com/powershell/module/az.network/new-azfirewallnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallNetworkRule.md
ms.openlocfilehash: 7b2c78793f5a5e5ae6de8c67ffc214ed5c9b9076
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101984433"
---
# <span data-ttu-id="04de8-101">New-AzFirewallNetworkRule</span><span class="sxs-lookup"><span data-stu-id="04de8-101">New-AzFirewallNetworkRule</span></span>

## <span data-ttu-id="04de8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="04de8-102">SYNOPSIS</span></span>
<span data-ttu-id="04de8-103">방화벽 네트워크 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="04de8-103">Creates a Firewall Network Rule.</span></span>

## <span data-ttu-id="04de8-104">구문</span><span class="sxs-lookup"><span data-stu-id="04de8-104">SYNTAX</span></span>

```
New-AzFirewallNetworkRule -Name <String> [-Description <String>] -SourceAddress <String[]>
 [-SourceIpGroup <String[]>] [-DestinationAddress <String[]>] [-DestinationIpGroup <String[]>]
 [-DestinationFqdn <String[]>] -DestinationPort <String[]> -Protocol <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="04de8-105">설명</span><span class="sxs-lookup"><span data-stu-id="04de8-105">DESCRIPTION</span></span>
<span data-ttu-id="04de8-106">**New-AzFirewallNetworkRule** cmdlet은 Azure Firewall에 대한 네트워크 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="04de8-106">The **New-AzFirewallNetworkRule** cmdlet creates an network rule for Azure Firewall.</span></span>

## <span data-ttu-id="04de8-107">예제</span><span class="sxs-lookup"><span data-stu-id="04de8-107">EXAMPLES</span></span>

### <span data-ttu-id="04de8-108">예제 1: 모든 TCP 트래픽에 대한 규칙 만들기</span><span class="sxs-lookup"><span data-stu-id="04de8-108">Example 1: Create a rule for all TCP traffic</span></span>
```powershell
$rule = New-AzFirewallNetworkRule -Name "all-tcp-traffic" -Description "Rule for all TCP traffic" -Protocol TCP -SourceAddress "*" -DestinationAddress "*" -DestinationPort "*"
```

<span data-ttu-id="04de8-109">이 예제에서는 모든 TCP 트래픽에 대한 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="04de8-109">This example creates a rule for all TCP traffic.</span></span> <span data-ttu-id="04de8-110">사용자는 연결된 규칙 컬렉션에 따라 규칙에 대해 트래픽을 허용하거나 거부할지 여부를 적용합니다.</span><span class="sxs-lookup"><span data-stu-id="04de8-110">User enforces whether traffic will be allowed or denied for a rule based on the rule collection it is associated with.</span></span>

### <span data-ttu-id="04de8-111">예제 2: 10.0.0.0에서 60.1.5.0:4040까지 모든 TCP 트래픽에 대한 규칙 만들기</span><span class="sxs-lookup"><span data-stu-id="04de8-111">Example 2: Create a rule for all TCP traffic from 10.0.0.0 to 60.1.5.0:4040</span></span>
```powershell
$rule = New-AzFirewallNetworkRule -Name "partial-tcp-rule" -Description "Rule for all TCP traffic from 10.0.0.0 to 60.1.5.0:4040" -Protocol TCP -SourceAddress "10.0.0.0" -DestinationAddress "60.1.5.0" -DestinationPort "4040"
```

<span data-ttu-id="04de8-112">이 예제에서는 10.0.0.0.0에서 60.1.5.0:4040까지의 모든 TCP 트래픽에 대한 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="04de8-112">This example creates a rule for all TCP traffic from 10.0.0.0 to 60.1.5.0:4040.</span></span> <span data-ttu-id="04de8-113">사용자는 연결된 규칙 컬렉션에 따라 규칙에 대해 트래픽을 허용하거나 거부할지 여부를 적용합니다.</span><span class="sxs-lookup"><span data-stu-id="04de8-113">User enforces whether traffic will be allowed or denied for a rule based on the rule collection it is associated with.</span></span>

### <span data-ttu-id="04de8-114">예제 3: 모든 원본에서 10.0.0.0/16으로 모든 TCP 및 ICMP 트래픽에 대한 규칙 만들기</span><span class="sxs-lookup"><span data-stu-id="04de8-114">Example 3: Create a rule for all TCP and ICMP traffic from any source to 10.0.0.0/16</span></span>
```powershell
$rule = New-AzFirewallNetworkRule -Name "tcp-and-icmp-rule" -Description "Rule for all TCP and ICMP traffic from any source to 10.0.0.0/16" -Protocol TCP,ICMP -SourceAddress * -DestinationAddress "10.0.0.0/16" -DestinationPort *
```

<span data-ttu-id="04de8-115">이 예제에서는 모든 원본에서 10.0.0.0/16으로 모든 TCP 트래픽에 대한 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="04de8-115">This example creates a rule for all TCP traffic from any source to 10.0.0.0/16.</span></span> <span data-ttu-id="04de8-116">사용자는 연결된 규칙 컬렉션에 따라 규칙에 대해 트래픽을 허용하거나 거부할지 여부를 적용합니다.</span><span class="sxs-lookup"><span data-stu-id="04de8-116">User enforces whether traffic will be allowed or denied for a rule based on the rule collection it is associated with.</span></span>

## <span data-ttu-id="04de8-117">매개 변수</span><span class="sxs-lookup"><span data-stu-id="04de8-117">PARAMETERS</span></span>

### <span data-ttu-id="04de8-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04de8-118">-DefaultProfile</span></span>
<span data-ttu-id="04de8-119">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="04de8-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="04de8-120">-Description</span><span class="sxs-lookup"><span data-stu-id="04de8-120">-Description</span></span>
<span data-ttu-id="04de8-121">이 규칙에 대한 선택적 설명을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="04de8-121">Specifies an optional description of this rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04de8-122">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="04de8-122">-DestinationAddress</span></span>
<span data-ttu-id="04de8-123">규칙의 대상 주소</span><span class="sxs-lookup"><span data-stu-id="04de8-123">The destination addresses of the rule</span></span>

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

### <span data-ttu-id="04de8-124">-DestinationFqdn</span><span class="sxs-lookup"><span data-stu-id="04de8-124">-DestinationFqdn</span></span>
<span data-ttu-id="04de8-125">규칙의 대상 FQDN</span><span class="sxs-lookup"><span data-stu-id="04de8-125">The destination FQDN of the rule</span></span>

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

### <span data-ttu-id="04de8-126">-DestinationIpGroup</span><span class="sxs-lookup"><span data-stu-id="04de8-126">-DestinationIpGroup</span></span>
<span data-ttu-id="04de8-127">규칙의 대상 ipgroup</span><span class="sxs-lookup"><span data-stu-id="04de8-127">The destination ipgroup of the rule</span></span>

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

### <span data-ttu-id="04de8-128">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="04de8-128">-DestinationPort</span></span>
<span data-ttu-id="04de8-129">규칙의 대상 포트</span><span class="sxs-lookup"><span data-stu-id="04de8-129">The destination ports of the rule</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04de8-130">-Name</span><span class="sxs-lookup"><span data-stu-id="04de8-130">-Name</span></span>
<span data-ttu-id="04de8-131">이 네트워크 규칙의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="04de8-131">Specifies the name of this network rule.</span></span> <span data-ttu-id="04de8-132">이름은 규칙 컬렉션 내에서 고유해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="04de8-132">The name must be unique inside a rule collection.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04de8-133">-Protocol</span><span class="sxs-lookup"><span data-stu-id="04de8-133">-Protocol</span></span>
<span data-ttu-id="04de8-134">이 규칙에서 필터링할 트래픽 유형을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="04de8-134">Specifies the type of traffic to be filtered by this rule.</span></span> <span data-ttu-id="04de8-135">가능한 값은 TCP, UDP, ICMP 및 Any입니다.</span><span class="sxs-lookup"><span data-stu-id="04de8-135">Possible values are TCP, UDP, ICMP and Any.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:
Accepted values: Any, TCP, UDP, ICMP

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04de8-136">-SourceAddress</span><span class="sxs-lookup"><span data-stu-id="04de8-136">-SourceAddress</span></span>
<span data-ttu-id="04de8-137">규칙의 원본 주소</span><span class="sxs-lookup"><span data-stu-id="04de8-137">The source addresses of the rule</span></span>

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

### <span data-ttu-id="04de8-138">-SourceIpGroup</span><span class="sxs-lookup"><span data-stu-id="04de8-138">-SourceIpGroup</span></span>
<span data-ttu-id="04de8-139">규칙의 원본 ipgroup</span><span class="sxs-lookup"><span data-stu-id="04de8-139">The source ipgroup of the rule</span></span>

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

### <span data-ttu-id="04de8-140">-확인</span><span class="sxs-lookup"><span data-stu-id="04de8-140">-Confirm</span></span>
<span data-ttu-id="04de8-141">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="04de8-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="04de8-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="04de8-142">-WhatIf</span></span>
<span data-ttu-id="04de8-143">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="04de8-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="04de8-144">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="04de8-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="04de8-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04de8-145">CommonParameters</span></span>
<span data-ttu-id="04de8-146">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="04de8-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04de8-147">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="04de8-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04de8-148">입력</span><span class="sxs-lookup"><span data-stu-id="04de8-148">INPUTS</span></span>

### <span data-ttu-id="04de8-149">없음</span><span class="sxs-lookup"><span data-stu-id="04de8-149">None</span></span>

## <span data-ttu-id="04de8-150">출력</span><span class="sxs-lookup"><span data-stu-id="04de8-150">OUTPUTS</span></span>

### <span data-ttu-id="04de8-151">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRule</span><span class="sxs-lookup"><span data-stu-id="04de8-151">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRule</span></span>

## <span data-ttu-id="04de8-152">참고 사항</span><span class="sxs-lookup"><span data-stu-id="04de8-152">NOTES</span></span>

## <span data-ttu-id="04de8-153">관련 링크</span><span class="sxs-lookup"><span data-stu-id="04de8-153">RELATED LINKS</span></span>

[<span data-ttu-id="04de8-154">New-AzFirewallNetworkRuleCollection</span><span class="sxs-lookup"><span data-stu-id="04de8-154">New-AzFirewallNetworkRuleCollection</span></span>](./New-AzFirewallNetworkRuleCollection.md)

[<span data-ttu-id="04de8-155">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="04de8-155">New-AzFirewall</span></span>](./New-AzFirewall.md)

[<span data-ttu-id="04de8-156">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="04de8-156">Get-AzFirewall</span></span>](./Get-AzFirewall.md)
