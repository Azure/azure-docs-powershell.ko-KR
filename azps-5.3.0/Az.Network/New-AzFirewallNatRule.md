---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C0E1D4DF-232F-49C6-BE4C-05C8E8038329
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallnatrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallNatRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallNatRule.md
ms.openlocfilehash: efe8821ee1ec0978c42aa59fc856b4d6e07fa7dc
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98492629"
---
# <span data-ttu-id="45c59-101">New-AzFirewallNatRule</span><span class="sxs-lookup"><span data-stu-id="45c59-101">New-AzFirewallNatRule</span></span>

## <span data-ttu-id="45c59-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="45c59-102">SYNOPSIS</span></span>
<span data-ttu-id="45c59-103">방화벽 NAT 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="45c59-103">Creates a Firewall NAT Rule.</span></span>

## <span data-ttu-id="45c59-104">구문</span><span class="sxs-lookup"><span data-stu-id="45c59-104">SYNTAX</span></span>

```
New-AzFirewallNatRule -Name <String> [-Description <String>] [-SourceAddress <String[]>]
 [-SourceIpGroup <String[]>] -DestinationAddress <String[]> -DestinationPort <String[]> -Protocol <String[]>
 [-TranslatedAddress <String>] [-TranslatedFqdn <String>] -TranslatedPort <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="45c59-105">설명</span><span class="sxs-lookup"><span data-stu-id="45c59-105">DESCRIPTION</span></span>
<span data-ttu-id="45c59-106">**New-AzFirewallNatRule** cmdlet은 Azure Firewall에 대한 NAT 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="45c59-106">The **New-AzFirewallNatRule** cmdlet creates a NAT rule for Azure Firewall.</span></span>

## <span data-ttu-id="45c59-107">예제</span><span class="sxs-lookup"><span data-stu-id="45c59-107">EXAMPLES</span></span>

### <span data-ttu-id="45c59-108">예제 1: 10.0.0.0/24에서 대상 10.1.2.3:80에서 대상 10.4.5.6:8080까지의 모든 TCP 트래픽을 DNAT에 규칙 만들기</span><span class="sxs-lookup"><span data-stu-id="45c59-108">Example 1: Create a rule to DNAT all TCP traffic from 10.0.0.0/24 with destination 10.1.2.3:80 to destination 10.4.5.6:8080</span></span>
```powershell
New-AzFirewallNatRule -Name "dnat-rule" -Protocol "TCP" -SourceAddress "10.0.0.0/24" -DestinationAddress "10.1.2.3" -DestinationPort "80" -TranslatedAddress "10.4.5.6" -TranslatedPort "8080"
```

<span data-ttu-id="45c59-109">이 예제에서는 대상 10.1.2.3:80에서 10.4.5.6:8080으로 10.0.0.0/24에서 시작되는 모든 트래픽을 DNAT하는 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="45c59-109">This example creates a rule which will DNAT all traffic originating in 10.0.0.0/24 with destination 10.1.2.3:80 to 10.4.5.6:8080</span></span>

## <span data-ttu-id="45c59-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="45c59-110">PARAMETERS</span></span>

### <span data-ttu-id="45c59-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45c59-111">-DefaultProfile</span></span>
<span data-ttu-id="45c59-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="45c59-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="45c59-113">-Description</span><span class="sxs-lookup"><span data-stu-id="45c59-113">-Description</span></span>
<span data-ttu-id="45c59-114">이 규칙에 대한 선택적 설명을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="45c59-114">Specifies an optional description of this rule.</span></span>

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

### <span data-ttu-id="45c59-115">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="45c59-115">-DestinationAddress</span></span>
<span data-ttu-id="45c59-116">규칙의 대상 주소</span><span class="sxs-lookup"><span data-stu-id="45c59-116">The destination addresses of the rule</span></span>

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

### <span data-ttu-id="45c59-117">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="45c59-117">-DestinationPort</span></span>
<span data-ttu-id="45c59-118">규칙의 대상 포트</span><span class="sxs-lookup"><span data-stu-id="45c59-118">The destination ports of the rule</span></span>

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

### <span data-ttu-id="45c59-119">-Name</span><span class="sxs-lookup"><span data-stu-id="45c59-119">-Name</span></span>
<span data-ttu-id="45c59-120">이 NAT 규칙의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="45c59-120">Specifies the name of this NAT rule.</span></span> <span data-ttu-id="45c59-121">이름은 규칙 컬렉션 내에서 고유해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="45c59-121">The name must be unique inside a rule collection.</span></span>

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

### <span data-ttu-id="45c59-122">-Protocol</span><span class="sxs-lookup"><span data-stu-id="45c59-122">-Protocol</span></span>
<span data-ttu-id="45c59-123">이 규칙에 따라 필터링할 트래픽 유형을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="45c59-123">Specifies the type of traffic to be filtered by this rule.</span></span>
<span data-ttu-id="45c59-124">지원되는 프로토콜은 TCP 및 UDP입니다.</span><span class="sxs-lookup"><span data-stu-id="45c59-124">The supported protocols are TCP and UDP.</span></span>
<span data-ttu-id="45c59-125">특수 값 "Any"는 허용됩니다. 즉, TCP와 UDP는 일치하지만 다른 프로토콜은 일치하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="45c59-125">A special value "Any" is allowed, meaning it will match both TCP and UDP, but no other protocols.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:
Accepted values: Any, TCP, UDP

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45c59-126">-SourceAddress</span><span class="sxs-lookup"><span data-stu-id="45c59-126">-SourceAddress</span></span>
<span data-ttu-id="45c59-127">규칙의 원본 주소</span><span class="sxs-lookup"><span data-stu-id="45c59-127">The source addresses of the rule</span></span>

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

### <span data-ttu-id="45c59-128">-SourceIpGroup</span><span class="sxs-lookup"><span data-stu-id="45c59-128">-SourceIpGroup</span></span>
<span data-ttu-id="45c59-129">규칙의 원본 ipgroup</span><span class="sxs-lookup"><span data-stu-id="45c59-129">The source ipgroup of the rule</span></span>

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

### <span data-ttu-id="45c59-130">-TranslatedAddress</span><span class="sxs-lookup"><span data-stu-id="45c59-130">-TranslatedAddress</span></span>
<span data-ttu-id="45c59-131">주소 변환의 원하는 결과를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="45c59-131">Specifies the desired result of the address translation</span></span>

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

### <span data-ttu-id="45c59-132">-TranslatedFqdn</span><span class="sxs-lookup"><span data-stu-id="45c59-132">-TranslatedFqdn</span></span>
<span data-ttu-id="45c59-133">이 NAT 규칙에 대한 번역된 FQDN</span><span class="sxs-lookup"><span data-stu-id="45c59-133">The translated FQDN for this NAT rule</span></span>

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

### <span data-ttu-id="45c59-134">-TranslatedPort</span><span class="sxs-lookup"><span data-stu-id="45c59-134">-TranslatedPort</span></span>
<span data-ttu-id="45c59-135">포트 변환의 원하는 결과를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="45c59-135">Specifies the desired result of the port translation</span></span>

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

### <span data-ttu-id="45c59-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="45c59-136">-Confirm</span></span>
<span data-ttu-id="45c59-137">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="45c59-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="45c59-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="45c59-138">-WhatIf</span></span>
<span data-ttu-id="45c59-139">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="45c59-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="45c59-140">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="45c59-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="45c59-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45c59-141">CommonParameters</span></span>
<span data-ttu-id="45c59-142">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="45c59-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45c59-143">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="45c59-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45c59-144">입력</span><span class="sxs-lookup"><span data-stu-id="45c59-144">INPUTS</span></span>

### <span data-ttu-id="45c59-145">없음</span><span class="sxs-lookup"><span data-stu-id="45c59-145">None</span></span>

## <span data-ttu-id="45c59-146">출력</span><span class="sxs-lookup"><span data-stu-id="45c59-146">OUTPUTS</span></span>

### <span data-ttu-id="45c59-147">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNatRule</span><span class="sxs-lookup"><span data-stu-id="45c59-147">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNatRule</span></span>

## <span data-ttu-id="45c59-148">참고 사항</span><span class="sxs-lookup"><span data-stu-id="45c59-148">NOTES</span></span>

## <span data-ttu-id="45c59-149">관련 링크</span><span class="sxs-lookup"><span data-stu-id="45c59-149">RELATED LINKS</span></span>

[<span data-ttu-id="45c59-150">New-AzFirewallNatRuleCollection</span><span class="sxs-lookup"><span data-stu-id="45c59-150">New-AzFirewallNatRuleCollection</span></span>](./New-AzFirewallNatRuleCollection.md)

[<span data-ttu-id="45c59-151">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="45c59-151">New-AzFirewall</span></span>](./New-AzFirewall.md)

[<span data-ttu-id="45c59-152">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="45c59-152">Get-AzFirewall</span></span>](./Get-AzFirewall.md)
