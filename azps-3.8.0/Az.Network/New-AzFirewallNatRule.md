---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C0E1D4DF-232F-49C6-BE4C-05C8E8038329
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallnatrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallNatRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallNatRule.md
ms.openlocfilehash: c0c6a1b3d868bb3189dc040baac9618e60130033
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93877354"
---
# <span data-ttu-id="43a6a-101">New-AzFirewallNatRule</span><span class="sxs-lookup"><span data-stu-id="43a6a-101">New-AzFirewallNatRule</span></span>

## <span data-ttu-id="43a6a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="43a6a-102">SYNOPSIS</span></span>
<span data-ttu-id="43a6a-103">방화벽 NAT 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="43a6a-103">Creates a Firewall NAT Rule.</span></span>

## <span data-ttu-id="43a6a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="43a6a-104">SYNTAX</span></span>

```
New-AzFirewallNatRule -Name <String> [-Description <String>] [-SourceAddress <String[]>]
 [-SourceIpGroup <String[]>] -DestinationAddress <String[]> -DestinationPort <String[]> -Protocol <String[]>
 [-TranslatedAddress <String>] [-TranslatedFqdn <String>] -TranslatedPort <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="43a6a-105">설명은</span><span class="sxs-lookup"><span data-stu-id="43a6a-105">DESCRIPTION</span></span>
<span data-ttu-id="43a6a-106">**AzFirewallNatRule** Cmdlet은 Azure 방화벽에 대 한 NAT 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="43a6a-106">The **New-AzFirewallNatRule** cmdlet creates a NAT rule for Azure Firewall.</span></span>

## <span data-ttu-id="43a6a-107">예제의</span><span class="sxs-lookup"><span data-stu-id="43a6a-107">EXAMPLES</span></span>

### <span data-ttu-id="43a6a-108">1: 대상 10.1.2.3:80에서 대상 10.4.5.6:8080으로 10.0.0.0/24의 모든 TCP 트래픽에 대해 DNAT 대 한 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="43a6a-108">1:  Create a rule to DNAT all TCP traffic from 10.0.0.0/24 with destination 10.1.2.3:80 to destination 10.4.5.6:8080</span></span>
```
New-AzFirewallNatRule -Name "dnat-rule" -Protocol "TCP" -SourceAddress "10.0.0.0/24" -DestinationAddress "10.1.2.3" -DestinationPort "80" -TranslatedAddress "10.4.5.6" -TranslatedPort "8080"
```

<span data-ttu-id="43a6a-109">이 예제에서는 대상 10.1.2.3:80에서 10.4.5.6:8080으로 10.0.0.0/24에서 발생 하는 모든 트래픽에 DNAT에 해당 하는 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="43a6a-109">This example creates a rule which will DNAT all traffic originating in 10.0.0.0/24 with destination 10.1.2.3:80 to 10.4.5.6:8080</span></span>

## <span data-ttu-id="43a6a-110">변수</span><span class="sxs-lookup"><span data-stu-id="43a6a-110">PARAMETERS</span></span>

### <span data-ttu-id="43a6a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43a6a-111">-DefaultProfile</span></span>
<span data-ttu-id="43a6a-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="43a6a-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="43a6a-113">-설명</span><span class="sxs-lookup"><span data-stu-id="43a6a-113">-Description</span></span>
<span data-ttu-id="43a6a-114">이 규칙에 대 한 설명을 선택적으로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="43a6a-114">Specifies an optional description of this rule.</span></span>

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

### <span data-ttu-id="43a6a-115">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="43a6a-115">-DestinationAddress</span></span>
<span data-ttu-id="43a6a-116">규칙의 대상 주소</span><span class="sxs-lookup"><span data-stu-id="43a6a-116">The destination addresses of the rule</span></span>

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

### <span data-ttu-id="43a6a-117">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="43a6a-117">-DestinationPort</span></span>
<span data-ttu-id="43a6a-118">규칙의 대상 포트</span><span class="sxs-lookup"><span data-stu-id="43a6a-118">The destination ports of the rule</span></span>

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

### <span data-ttu-id="43a6a-119">-이름</span><span class="sxs-lookup"><span data-stu-id="43a6a-119">-Name</span></span>
<span data-ttu-id="43a6a-120">이 NAT 규칙의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="43a6a-120">Specifies the name of this NAT rule.</span></span> <span data-ttu-id="43a6a-121">이름은 규칙 컬렉션 내에서 고유 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="43a6a-121">The name must be unique inside a rule collection.</span></span>

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

### <span data-ttu-id="43a6a-122">-프로토콜</span><span class="sxs-lookup"><span data-stu-id="43a6a-122">-Protocol</span></span>
<span data-ttu-id="43a6a-123">이 규칙에 따라 필터링 할 트래픽 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="43a6a-123">Specifies the type of traffic to be filtered by this rule.</span></span>
<span data-ttu-id="43a6a-124">지원 되는 프로토콜은 TCP 및 UDP입니다.</span><span class="sxs-lookup"><span data-stu-id="43a6a-124">The supported protocols are TCP and UDP.</span></span>
<span data-ttu-id="43a6a-125">특별 한 "모든" 값을 사용할 수 있으며,이는 TCP 및 UDP와 다른 프로토콜은 일치 하지 않는다는 의미입니다.</span><span class="sxs-lookup"><span data-stu-id="43a6a-125">A special value "Any" is allowed, meaning it will match both TCP and UDP, but no other protocols.</span></span>

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

### <span data-ttu-id="43a6a-126">-SourceAddress</span><span class="sxs-lookup"><span data-stu-id="43a6a-126">-SourceAddress</span></span>
<span data-ttu-id="43a6a-127">규칙의 원본 주소</span><span class="sxs-lookup"><span data-stu-id="43a6a-127">The source addresses of the rule</span></span>

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

### <span data-ttu-id="43a6a-128">-SourceIpGroup</span><span class="sxs-lookup"><span data-stu-id="43a6a-128">-SourceIpGroup</span></span>
<span data-ttu-id="43a6a-129">규칙의 원본 ipgroup</span><span class="sxs-lookup"><span data-stu-id="43a6a-129">The source ipgroup of the rule</span></span>

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

### <span data-ttu-id="43a6a-130">-TranslatedAddress</span><span class="sxs-lookup"><span data-stu-id="43a6a-130">-TranslatedAddress</span></span>
<span data-ttu-id="43a6a-131">주소 변환의 원하는 결과를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="43a6a-131">Specifies the desired result of the address translation</span></span>

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

### <span data-ttu-id="43a6a-132">-TranslatedFqdn</span><span class="sxs-lookup"><span data-stu-id="43a6a-132">-TranslatedFqdn</span></span>
<span data-ttu-id="43a6a-133">이 NAT 규칙에 대해 번역 된 FQDN</span><span class="sxs-lookup"><span data-stu-id="43a6a-133">The translated FQDN for this NAT rule</span></span>

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

### <span data-ttu-id="43a6a-134">-TranslatedPort</span><span class="sxs-lookup"><span data-stu-id="43a6a-134">-TranslatedPort</span></span>
<span data-ttu-id="43a6a-135">포트 변환의 원하는 결과를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="43a6a-135">Specifies the desired result of the port translation</span></span>

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

### <span data-ttu-id="43a6a-136">-확인</span><span class="sxs-lookup"><span data-stu-id="43a6a-136">-Confirm</span></span>
<span data-ttu-id="43a6a-137">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="43a6a-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="43a6a-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="43a6a-138">-WhatIf</span></span>
<span data-ttu-id="43a6a-139">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="43a6a-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="43a6a-140">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="43a6a-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="43a6a-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43a6a-141">CommonParameters</span></span>
<span data-ttu-id="43a6a-142">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="43a6a-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43a6a-143">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="43a6a-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43a6a-144">입력</span><span class="sxs-lookup"><span data-stu-id="43a6a-144">INPUTS</span></span>

### <span data-ttu-id="43a6a-145">않아야</span><span class="sxs-lookup"><span data-stu-id="43a6a-145">None</span></span>

## <span data-ttu-id="43a6a-146">출력</span><span class="sxs-lookup"><span data-stu-id="43a6a-146">OUTPUTS</span></span>

### <span data-ttu-id="43a6a-147">PSAzureFirewallNatRule에 대 한.</span><span class="sxs-lookup"><span data-stu-id="43a6a-147">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNatRule</span></span>

## <span data-ttu-id="43a6a-148">상속자</span><span class="sxs-lookup"><span data-stu-id="43a6a-148">NOTES</span></span>

## <span data-ttu-id="43a6a-149">관련 링크</span><span class="sxs-lookup"><span data-stu-id="43a6a-149">RELATED LINKS</span></span>

[<span data-ttu-id="43a6a-150">새로운 AzFirewallNatRuleCollection</span><span class="sxs-lookup"><span data-stu-id="43a6a-150">New-AzFirewallNatRuleCollection</span></span>](./New-AzFirewallNatRuleCollection.md)

[<span data-ttu-id="43a6a-151">새로운 AzFirewall</span><span class="sxs-lookup"><span data-stu-id="43a6a-151">New-AzFirewall</span></span>](./New-AzFirewall.md)

[<span data-ttu-id="43a6a-152">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="43a6a-152">Get-AzFirewall</span></span>](./Get-AzFirewall.md)
