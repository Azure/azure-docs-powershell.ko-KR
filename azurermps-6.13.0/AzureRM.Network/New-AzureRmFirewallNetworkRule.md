---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: C0E1D4DF-232F-49C6-BE4C-05C8E8038329
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermfirewallnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmFirewallNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmFirewallNetworkRule.md
ms.openlocfilehash: 1100e42934c493bf8aea30e7372acc683b46b60b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93528507"
---
# <span data-ttu-id="d425f-101">New-AzureRmFirewallNetworkRule</span><span class="sxs-lookup"><span data-stu-id="d425f-101">New-AzureRmFirewallNetworkRule</span></span>

## <span data-ttu-id="d425f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d425f-102">SYNOPSIS</span></span>
<span data-ttu-id="d425f-103">방화벽 네트워크 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d425f-103">Creates a Firewall Network Rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d425f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d425f-104">SYNTAX</span></span>

```
New-AzureRmFirewallNetworkRule -Name <String> [-Description <String>]
 -SourceAddress <System.Collections.Generic.List`1[System.String]>
 -DestinationAddress <System.Collections.Generic.List`1[System.String]>
 -DestinationPort <System.Collections.Generic.List`1[System.String]>
 -Protocol <System.Collections.Generic.List`1[System.String]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d425f-105">설명은</span><span class="sxs-lookup"><span data-stu-id="d425f-105">DESCRIPTION</span></span>
<span data-ttu-id="d425f-106">**AzureRmFirewallNetworkRule** Cmdlet은 Azure 방화벽에 대 한 네트워크 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d425f-106">The **New-AzureRmFirewallNetworkRule** cmdlet creates an network rule for Azure Firewall.</span></span>

## <span data-ttu-id="d425f-107">예제의</span><span class="sxs-lookup"><span data-stu-id="d425f-107">EXAMPLES</span></span>

### <span data-ttu-id="d425f-108">1: 모든 TCP 트래픽에 대 한 규칙 만들기</span><span class="sxs-lookup"><span data-stu-id="d425f-108">1:  Create a rule for all TCP traffic</span></span>
```
$rule = New-AzureRmFirewallNetworkRule -Name "all-tcp-traffic" -Description "Rule for all TCP traffic" -Protocol TCP -SourceAddress "*" -DestinationAddress "*" -DestinationPort "*"
```

<span data-ttu-id="d425f-109">이 예제에서는 모든 TCP 트래픽에 대 한 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d425f-109">This example creates a rule for all TCP traffic.</span></span> <span data-ttu-id="d425f-110">사용자는 연결 된 규칙 컬렉션을 기준으로 하는 규칙에 대해 트래픽을 허용할지 또는 거부할지를 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="d425f-110">User enforces whether traffic will be allowed or denied for a rule based on the rule collection it is associated with.</span></span>

### <span data-ttu-id="d425f-111">2:10.0.0.0에서 60.1.5.0:4040에 대 한 모든 TCP 트래픽에 대 한 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d425f-111">2:  Create a rule for all TCP traffic from 10.0.0.0 to 60.1.5.0:4040</span></span>
```
$rule = New-AzureRmFirewallNetworkRule -Name "partial-tcp-rule" -Description "Rule for all TCP traffic from 10.0.0.0 to 60.1.5.0:4040" -Protocol TCP -SourceAddress "10.0.0.0" -DestinationAddress "60.1.5.0" -DestinationPort "4040"
```

<span data-ttu-id="d425f-112">이 예제에서는 10.0.0.0에서 60.1.5.0:4040 까지의 모든 TCP 트래픽에 대 한 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d425f-112">This example creates a rule for all TCP traffic from 10.0.0.0 to 60.1.5.0:4040.</span></span> <span data-ttu-id="d425f-113">사용자는 연결 된 규칙 컬렉션을 기준으로 하는 규칙에 대해 트래픽을 허용할지 또는 거부할지를 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="d425f-113">User enforces whether traffic will be allowed or denied for a rule based on the rule collection it is associated with.</span></span>

### <span data-ttu-id="d425f-114">3: 모든 원본에서 10.0.0.0/16으로 모든 TCP 및 ICMP 트래픽에 대 한 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d425f-114">3: Create a rule for all TCP and ICMP traffic from any source to 10.0.0.0/16</span></span>
```
$rule = New-AzureRmFirewallNetworkRule -Name "tcp-and-icmp-rule" -Description "Rule for all TCP and ICMP traffic from any source to 10.0.0.0/16" -Protocol TCP,ICMP -SourceAddress * -DestinationAddress "10.0.0.0/16" -DestinationPort *
```

<span data-ttu-id="d425f-115">이 예제에서는 10.0.0.0에서 60.1.5.0:4040 까지의 모든 TCP 트래픽에 대 한 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d425f-115">This example creates a rule for all TCP traffic from 10.0.0.0 to 60.1.5.0:4040.</span></span> <span data-ttu-id="d425f-116">사용자는 연결 된 규칙 컬렉션을 기준으로 하는 규칙에 대해 트래픽을 허용할지 또는 거부할지를 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="d425f-116">User enforces whether traffic will be allowed or denied for a rule based on the rule collection it is associated with.</span></span>

## <span data-ttu-id="d425f-117">변수</span><span class="sxs-lookup"><span data-stu-id="d425f-117">PARAMETERS</span></span>

### <span data-ttu-id="d425f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d425f-118">-DefaultProfile</span></span>
<span data-ttu-id="d425f-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d425f-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d425f-120">-설명</span><span class="sxs-lookup"><span data-stu-id="d425f-120">-Description</span></span>
<span data-ttu-id="d425f-121">이 규칙에 대 한 설명을 선택적으로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d425f-121">Specifies an optional description of this rule.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d425f-122">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="d425f-122">-DestinationAddress</span></span>
<span data-ttu-id="d425f-123">규칙의 대상 주소</span><span class="sxs-lookup"><span data-stu-id="d425f-123">The destination addresses of the rule</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d425f-124">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="d425f-124">-DestinationPort</span></span>
<span data-ttu-id="d425f-125">규칙의 대상 포트</span><span class="sxs-lookup"><span data-stu-id="d425f-125">The destination ports of the rule</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d425f-126">-이름</span><span class="sxs-lookup"><span data-stu-id="d425f-126">-Name</span></span>
<span data-ttu-id="d425f-127">이 네트워크 규칙의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d425f-127">Specifies the name of this network rule.</span></span> <span data-ttu-id="d425f-128">이름은 규칙 컬렉션 내에서 고유 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d425f-128">The name must be unique inside a rule collection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d425f-129">-프로토콜</span><span class="sxs-lookup"><span data-stu-id="d425f-129">-Protocol</span></span>
<span data-ttu-id="d425f-130">이 규칙에 따라 필터링 할 트래픽 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d425f-130">Specifies the type of traffic to be filtered by this rule.</span></span> <span data-ttu-id="d425f-131">가능한 값은 TCP, UDP, ICMP 등입니다.</span><span class="sxs-lookup"><span data-stu-id="d425f-131">Possible values are TCP, UDP, ICMP and Any.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d425f-132">-SourceAddress</span><span class="sxs-lookup"><span data-stu-id="d425f-132">-SourceAddress</span></span>
<span data-ttu-id="d425f-133">규칙의 원본 주소</span><span class="sxs-lookup"><span data-stu-id="d425f-133">The source addresses of the rule</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d425f-134">-확인</span><span class="sxs-lookup"><span data-stu-id="d425f-134">-Confirm</span></span>
<span data-ttu-id="d425f-135">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="d425f-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d425f-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d425f-136">-WhatIf</span></span>
<span data-ttu-id="d425f-137">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="d425f-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d425f-138">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d425f-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d425f-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d425f-139">CommonParameters</span></span>
<span data-ttu-id="d425f-140">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d425f-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d425f-141">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d425f-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d425f-142">입력</span><span class="sxs-lookup"><span data-stu-id="d425f-142">INPUTS</span></span>

### <span data-ttu-id="d425f-143">않아야</span><span class="sxs-lookup"><span data-stu-id="d425f-143">None</span></span>
<span data-ttu-id="d425f-144">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d425f-144">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d425f-145">출력</span><span class="sxs-lookup"><span data-stu-id="d425f-145">OUTPUTS</span></span>

### <span data-ttu-id="d425f-146">PSFirewallNetworkRule에 대 한.</span><span class="sxs-lookup"><span data-stu-id="d425f-146">Microsoft.Azure.Commands.Network.Models.PSFirewallNetworkRule</span></span>

## <span data-ttu-id="d425f-147">상속자</span><span class="sxs-lookup"><span data-stu-id="d425f-147">NOTES</span></span>

## <span data-ttu-id="d425f-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d425f-148">RELATED LINKS</span></span>

[<span data-ttu-id="d425f-149">새로운 AzureRmFirewallNetworkRuleCollection</span><span class="sxs-lookup"><span data-stu-id="d425f-149">New-AzureRmFirewallNetworkRuleCollection</span></span>](./New-AzureRmFirewallNetworkRuleCollection.md)

[<span data-ttu-id="d425f-150">새로운 AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="d425f-150">New-AzureRmFirewall</span></span>](./New-AzureRmFirewall.md)

[<span data-ttu-id="d425f-151">Get-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="d425f-151">Get-AzureRmFirewall</span></span>](./Get-AzureRmFirewall.md)
