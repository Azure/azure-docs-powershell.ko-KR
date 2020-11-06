---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: C0E1D4DF-232F-49C6-BE4C-05C8E8038329
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermfirewallnatrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmFirewallNatRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmFirewallNatRule.md
ms.openlocfilehash: 0bad5133dd57ec0bee88949fbc9536a6389d6112
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531394"
---
# <span data-ttu-id="9ea5b-101">New-AzureRmFirewallNatRule</span><span class="sxs-lookup"><span data-stu-id="9ea5b-101">New-AzureRmFirewallNatRule</span></span>

## <span data-ttu-id="9ea5b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9ea5b-102">SYNOPSIS</span></span>
<span data-ttu-id="9ea5b-103">방화벽 NAT 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9ea5b-103">Creates a Firewall NAT Rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9ea5b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="9ea5b-104">SYNTAX</span></span>

```
New-AzureRmFirewallNatRule -Name <String> [-Description <String>]
 -SourceAddress <System.Collections.Generic.List`1[System.String]>
 -DestinationAddress <System.Collections.Generic.List`1[System.String]>
 -DestinationPort <System.Collections.Generic.List`1[System.String]>
 -Protocol <System.Collections.Generic.List`1[System.String]> -TranslatedAddress <String>
 -TranslatedPort <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9ea5b-105">설명은</span><span class="sxs-lookup"><span data-stu-id="9ea5b-105">DESCRIPTION</span></span>
<span data-ttu-id="9ea5b-106">**AzureRmFirewallNatRule** Cmdlet은 Azure 방화벽에 대 한 NAT 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9ea5b-106">The **New-AzureRmFirewallNatRule** cmdlet creates a NAT rule for Azure Firewall.</span></span>

## <span data-ttu-id="9ea5b-107">예제의</span><span class="sxs-lookup"><span data-stu-id="9ea5b-107">EXAMPLES</span></span>

### <span data-ttu-id="9ea5b-108">1: 대상 10.1.2.3:80에서 대상 10.4.5.6:8080으로 10.0.0.0/24의 모든 TCP 트래픽에 대해 DNAT 대 한 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9ea5b-108">1:  Create a rule to DNAT all TCP traffic from 10.0.0.0/24 with destination 10.1.2.3:80 to destination 10.4.5.6:8080</span></span>
```
New-AzureRmFirewallNatRule -Name "dnat-rule" -Protocol "TCP" -SourceAddress "10.0.0.0/24" -DestinationAddress "10.1.2.3" -DestinationPort "80" -TranslatedAddress "10.4.5.6" -TranslatedPort "8080"
```

<span data-ttu-id="9ea5b-109">이 예제에서는 대상 10.1.2.3:80에서 10.4.5.6:8080으로 10.0.0.0/24에서 발생 하는 모든 트래픽에 DNAT에 해당 하는 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9ea5b-109">This example creates a rule which will DNAT all traffic originating in 10.0.0.0/24 with destination 10.1.2.3:80 to 10.4.5.6:8080</span></span>

## <span data-ttu-id="9ea5b-110">변수</span><span class="sxs-lookup"><span data-stu-id="9ea5b-110">PARAMETERS</span></span>

### <span data-ttu-id="9ea5b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ea5b-111">-DefaultProfile</span></span>
<span data-ttu-id="9ea5b-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9ea5b-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ea5b-113">-설명</span><span class="sxs-lookup"><span data-stu-id="9ea5b-113">-Description</span></span>
<span data-ttu-id="9ea5b-114">이 규칙에 대 한 설명을 선택적으로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ea5b-114">Specifies an optional description of this rule.</span></span>

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

### <span data-ttu-id="9ea5b-115">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="9ea5b-115">-DestinationAddress</span></span>
<span data-ttu-id="9ea5b-116">규칙의 대상 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="9ea5b-116">The destination addresses of the rule.</span></span>

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

### <span data-ttu-id="9ea5b-117">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="9ea5b-117">-DestinationPort</span></span>
<span data-ttu-id="9ea5b-118">규칙의 대상 포트</span><span class="sxs-lookup"><span data-stu-id="9ea5b-118">The destination ports of the rule</span></span>

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

### <span data-ttu-id="9ea5b-119">-이름</span><span class="sxs-lookup"><span data-stu-id="9ea5b-119">-Name</span></span>
<span data-ttu-id="9ea5b-120">이 NAT 규칙의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ea5b-120">Specifies the name of this NAT rule.</span></span> <span data-ttu-id="9ea5b-121">이름은 규칙 컬렉션 내에서 고유 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ea5b-121">The name must be unique inside a rule collection.</span></span>

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

### <span data-ttu-id="9ea5b-122">-프로토콜</span><span class="sxs-lookup"><span data-stu-id="9ea5b-122">-Protocol</span></span>
<span data-ttu-id="9ea5b-123">이 규칙에 따라 필터링 할 트래픽 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ea5b-123">Specifies the type of traffic to be filtered by this rule.</span></span>
<span data-ttu-id="9ea5b-124">지원 되는 프로토콜은 TCP 및 UDP입니다.</span><span class="sxs-lookup"><span data-stu-id="9ea5b-124">The supported protocols are TCP and UDP.</span></span>
<span data-ttu-id="9ea5b-125">특별 한 "모든" 값을 사용할 수 있으며,이는 TCP 및 UDP와 다른 프로토콜은 일치 하지 않는다는 의미입니다.</span><span class="sxs-lookup"><span data-stu-id="9ea5b-125">A special value "Any" is allowed, meaning it will match both TCP and UDP, but no other protocols.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:
Accepted values: Any, TCP, UDP

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ea5b-126">-SourceAddress</span><span class="sxs-lookup"><span data-stu-id="9ea5b-126">-SourceAddress</span></span>
<span data-ttu-id="9ea5b-127">규칙의 원본 주소</span><span class="sxs-lookup"><span data-stu-id="9ea5b-127">The source addresses of the rule</span></span>

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

### <span data-ttu-id="9ea5b-128">-TranslatedAddress</span><span class="sxs-lookup"><span data-stu-id="9ea5b-128">-TranslatedAddress</span></span>
<span data-ttu-id="9ea5b-129">주소 변환의 원하는 결과를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ea5b-129">Specifies the desired result of the address translation</span></span>

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

### <span data-ttu-id="9ea5b-130">-TranslatedPort</span><span class="sxs-lookup"><span data-stu-id="9ea5b-130">-TranslatedPort</span></span>
<span data-ttu-id="9ea5b-131">포트 변환의 원하는 결과를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ea5b-131">Specifies the desired result of the port translation</span></span>

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

### <span data-ttu-id="9ea5b-132">-확인</span><span class="sxs-lookup"><span data-stu-id="9ea5b-132">-Confirm</span></span>
<span data-ttu-id="9ea5b-133">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ea5b-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9ea5b-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9ea5b-134">-WhatIf</span></span>
<span data-ttu-id="9ea5b-135">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="9ea5b-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9ea5b-136">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9ea5b-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9ea5b-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ea5b-137">CommonParameters</span></span>
<span data-ttu-id="9ea5b-138">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ea5b-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ea5b-139">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9ea5b-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ea5b-140">입력</span><span class="sxs-lookup"><span data-stu-id="9ea5b-140">INPUTS</span></span>

### <span data-ttu-id="9ea5b-141">않아야</span><span class="sxs-lookup"><span data-stu-id="9ea5b-141">None</span></span>
<span data-ttu-id="9ea5b-142">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9ea5b-142">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="9ea5b-143">출력</span><span class="sxs-lookup"><span data-stu-id="9ea5b-143">OUTPUTS</span></span>

### <span data-ttu-id="9ea5b-144">PSFirewallNatRule에 대 한.</span><span class="sxs-lookup"><span data-stu-id="9ea5b-144">Microsoft.Azure.Commands.Network.Models.PSFirewallNatRule</span></span>

## <span data-ttu-id="9ea5b-145">상속자</span><span class="sxs-lookup"><span data-stu-id="9ea5b-145">NOTES</span></span>

## <span data-ttu-id="9ea5b-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9ea5b-146">RELATED LINKS</span></span>

[<span data-ttu-id="9ea5b-147">새로운 AzureRmFirewallNatRuleCollection</span><span class="sxs-lookup"><span data-stu-id="9ea5b-147">New-AzureRmFirewallNatRuleCollection</span></span>](./New-AzureRmFirewallNatRuleCollection.md)

[<span data-ttu-id="9ea5b-148">새로운 AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="9ea5b-148">New-AzureRmFirewall</span></span>](./New-AzureRmFirewall.md)

[<span data-ttu-id="9ea5b-149">Get-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="9ea5b-149">Get-AzureRmFirewall</span></span>](./Get-AzureRmFirewall.md)
