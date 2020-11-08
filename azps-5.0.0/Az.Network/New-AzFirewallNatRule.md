---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C0E1D4DF-232F-49C6-BE4C-05C8E8038329
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallnatrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallNatRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallNatRule.md
ms.openlocfilehash: efe8821ee1ec0978c42aa59fc856b4d6e07fa7dc
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94218321"
---
# <span data-ttu-id="aa39e-101">New-AzFirewallNatRule</span><span class="sxs-lookup"><span data-stu-id="aa39e-101">New-AzFirewallNatRule</span></span>

## <span data-ttu-id="aa39e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aa39e-102">SYNOPSIS</span></span>
<span data-ttu-id="aa39e-103">방화벽 NAT 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="aa39e-103">Creates a Firewall NAT Rule.</span></span>

## <span data-ttu-id="aa39e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="aa39e-104">SYNTAX</span></span>

```
New-AzFirewallNatRule -Name <String> [-Description <String>] [-SourceAddress <String[]>]
 [-SourceIpGroup <String[]>] -DestinationAddress <String[]> -DestinationPort <String[]> -Protocol <String[]>
 [-TranslatedAddress <String>] [-TranslatedFqdn <String>] -TranslatedPort <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aa39e-105">설명은</span><span class="sxs-lookup"><span data-stu-id="aa39e-105">DESCRIPTION</span></span>
<span data-ttu-id="aa39e-106">**AzFirewallNatRule** Cmdlet은 Azure 방화벽에 대 한 NAT 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="aa39e-106">The **New-AzFirewallNatRule** cmdlet creates a NAT rule for Azure Firewall.</span></span>

## <span data-ttu-id="aa39e-107">예제의</span><span class="sxs-lookup"><span data-stu-id="aa39e-107">EXAMPLES</span></span>

### <span data-ttu-id="aa39e-108">예제 1: 대상 10.1.2.3:80에서 대상 10.4.5.6:8080으로 10.0.0.0/24의 모든 TCP 트래픽에 대해 DNAT에 대 한 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="aa39e-108">Example 1: Create a rule to DNAT all TCP traffic from 10.0.0.0/24 with destination 10.1.2.3:80 to destination 10.4.5.6:8080</span></span>
```powershell
New-AzFirewallNatRule -Name "dnat-rule" -Protocol "TCP" -SourceAddress "10.0.0.0/24" -DestinationAddress "10.1.2.3" -DestinationPort "80" -TranslatedAddress "10.4.5.6" -TranslatedPort "8080"
```

<span data-ttu-id="aa39e-109">이 예제에서는 대상 10.1.2.3:80에서 10.4.5.6:8080으로 10.0.0.0/24에서 발생 하는 모든 트래픽에 DNAT에 해당 하는 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="aa39e-109">This example creates a rule which will DNAT all traffic originating in 10.0.0.0/24 with destination 10.1.2.3:80 to 10.4.5.6:8080</span></span>

## <span data-ttu-id="aa39e-110">변수</span><span class="sxs-lookup"><span data-stu-id="aa39e-110">PARAMETERS</span></span>

### <span data-ttu-id="aa39e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa39e-111">-DefaultProfile</span></span>
<span data-ttu-id="aa39e-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="aa39e-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="aa39e-113">-설명</span><span class="sxs-lookup"><span data-stu-id="aa39e-113">-Description</span></span>
<span data-ttu-id="aa39e-114">이 규칙에 대 한 설명을 선택적으로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="aa39e-114">Specifies an optional description of this rule.</span></span>

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

### <span data-ttu-id="aa39e-115">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="aa39e-115">-DestinationAddress</span></span>
<span data-ttu-id="aa39e-116">규칙의 대상 주소</span><span class="sxs-lookup"><span data-stu-id="aa39e-116">The destination addresses of the rule</span></span>

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

### <span data-ttu-id="aa39e-117">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="aa39e-117">-DestinationPort</span></span>
<span data-ttu-id="aa39e-118">규칙의 대상 포트</span><span class="sxs-lookup"><span data-stu-id="aa39e-118">The destination ports of the rule</span></span>

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

### <span data-ttu-id="aa39e-119">-이름</span><span class="sxs-lookup"><span data-stu-id="aa39e-119">-Name</span></span>
<span data-ttu-id="aa39e-120">이 NAT 규칙의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="aa39e-120">Specifies the name of this NAT rule.</span></span> <span data-ttu-id="aa39e-121">이름은 규칙 컬렉션 내에서 고유 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="aa39e-121">The name must be unique inside a rule collection.</span></span>

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

### <span data-ttu-id="aa39e-122">-프로토콜</span><span class="sxs-lookup"><span data-stu-id="aa39e-122">-Protocol</span></span>
<span data-ttu-id="aa39e-123">이 규칙에 따라 필터링 할 트래픽 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="aa39e-123">Specifies the type of traffic to be filtered by this rule.</span></span>
<span data-ttu-id="aa39e-124">지원 되는 프로토콜은 TCP 및 UDP입니다.</span><span class="sxs-lookup"><span data-stu-id="aa39e-124">The supported protocols are TCP and UDP.</span></span>
<span data-ttu-id="aa39e-125">특별 한 "모든" 값을 사용할 수 있으며,이는 TCP 및 UDP와 다른 프로토콜은 일치 하지 않는다는 의미입니다.</span><span class="sxs-lookup"><span data-stu-id="aa39e-125">A special value "Any" is allowed, meaning it will match both TCP and UDP, but no other protocols.</span></span>

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

### <span data-ttu-id="aa39e-126">-SourceAddress</span><span class="sxs-lookup"><span data-stu-id="aa39e-126">-SourceAddress</span></span>
<span data-ttu-id="aa39e-127">규칙의 원본 주소</span><span class="sxs-lookup"><span data-stu-id="aa39e-127">The source addresses of the rule</span></span>

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

### <span data-ttu-id="aa39e-128">-SourceIpGroup</span><span class="sxs-lookup"><span data-stu-id="aa39e-128">-SourceIpGroup</span></span>
<span data-ttu-id="aa39e-129">규칙의 원본 ipgroup</span><span class="sxs-lookup"><span data-stu-id="aa39e-129">The source ipgroup of the rule</span></span>

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

### <span data-ttu-id="aa39e-130">-TranslatedAddress</span><span class="sxs-lookup"><span data-stu-id="aa39e-130">-TranslatedAddress</span></span>
<span data-ttu-id="aa39e-131">주소 변환의 원하는 결과를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="aa39e-131">Specifies the desired result of the address translation</span></span>

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

### <span data-ttu-id="aa39e-132">-TranslatedFqdn</span><span class="sxs-lookup"><span data-stu-id="aa39e-132">-TranslatedFqdn</span></span>
<span data-ttu-id="aa39e-133">이 NAT 규칙에 대해 번역 된 FQDN</span><span class="sxs-lookup"><span data-stu-id="aa39e-133">The translated FQDN for this NAT rule</span></span>

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

### <span data-ttu-id="aa39e-134">-TranslatedPort</span><span class="sxs-lookup"><span data-stu-id="aa39e-134">-TranslatedPort</span></span>
<span data-ttu-id="aa39e-135">포트 변환의 원하는 결과를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="aa39e-135">Specifies the desired result of the port translation</span></span>

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

### <span data-ttu-id="aa39e-136">-확인</span><span class="sxs-lookup"><span data-stu-id="aa39e-136">-Confirm</span></span>
<span data-ttu-id="aa39e-137">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="aa39e-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aa39e-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aa39e-138">-WhatIf</span></span>
<span data-ttu-id="aa39e-139">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="aa39e-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aa39e-140">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="aa39e-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aa39e-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa39e-141">CommonParameters</span></span>
<span data-ttu-id="aa39e-142">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="aa39e-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa39e-143">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aa39e-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa39e-144">입력</span><span class="sxs-lookup"><span data-stu-id="aa39e-144">INPUTS</span></span>

### <span data-ttu-id="aa39e-145">않아야</span><span class="sxs-lookup"><span data-stu-id="aa39e-145">None</span></span>

## <span data-ttu-id="aa39e-146">출력</span><span class="sxs-lookup"><span data-stu-id="aa39e-146">OUTPUTS</span></span>

### <span data-ttu-id="aa39e-147">PSAzureFirewallNatRule에 대 한.</span><span class="sxs-lookup"><span data-stu-id="aa39e-147">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNatRule</span></span>

## <span data-ttu-id="aa39e-148">상속자</span><span class="sxs-lookup"><span data-stu-id="aa39e-148">NOTES</span></span>

## <span data-ttu-id="aa39e-149">관련 링크</span><span class="sxs-lookup"><span data-stu-id="aa39e-149">RELATED LINKS</span></span>

[<span data-ttu-id="aa39e-150">새로운 AzFirewallNatRuleCollection</span><span class="sxs-lookup"><span data-stu-id="aa39e-150">New-AzFirewallNatRuleCollection</span></span>](./New-AzFirewallNatRuleCollection.md)

[<span data-ttu-id="aa39e-151">새로운 AzFirewall</span><span class="sxs-lookup"><span data-stu-id="aa39e-151">New-AzFirewall</span></span>](./New-AzFirewall.md)

[<span data-ttu-id="aa39e-152">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="aa39e-152">Get-AzFirewall</span></span>](./Get-AzFirewall.md)
