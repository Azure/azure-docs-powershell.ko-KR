---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallpolicynatrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyNatRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyNatRule.md
ms.openlocfilehash: f6a989a206c6fabf8e64cc82fb07741983f144c5
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94048903"
---
# <span data-ttu-id="7c8a7-101">New-AzFirewallPolicyNatRule</span><span class="sxs-lookup"><span data-stu-id="7c8a7-101">New-AzFirewallPolicyNatRule</span></span>

## <span data-ttu-id="7c8a7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7c8a7-102">SYNOPSIS</span></span>
<span data-ttu-id="7c8a7-103">새 Azure 방화벽 정책 NAT 규칙 만들기</span><span class="sxs-lookup"><span data-stu-id="7c8a7-103">Create a new Azure Firewall Policy NAT Rule</span></span>

## <span data-ttu-id="7c8a7-104">구문과</span><span class="sxs-lookup"><span data-stu-id="7c8a7-104">SYNTAX</span></span>

```
New-AzFirewallPolicyNatRule -Name <String> [-Description <String>] -SourceAddress <String[]>
 [-SourceIpGroup <String[]>] -DestinationAddress <String[]> -DestinationPort <String[]>
 -Protocols <String[]> -TranslatedAddress <String>
 -TranslatedPort <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7c8a7-105">설명은</span><span class="sxs-lookup"><span data-stu-id="7c8a7-105">DESCRIPTION</span></span>
<span data-ttu-id="7c8a7-106">**AzFirewallPolicyNatRule** Cmdlet은 Azure 방화벽 정책에 대 한 NAT 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="7c8a7-106">The **New-AzFirewallPolicyNatRule** cmdlet creates a NAT rule for a Azure Firewall Policy.</span></span>

## <span data-ttu-id="7c8a7-107">예제의</span><span class="sxs-lookup"><span data-stu-id="7c8a7-107">EXAMPLES</span></span>

### <span data-ttu-id="7c8a7-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="7c8a7-108">Example 1</span></span>
```powershell
PS C:\> New-AzFirewallPolicyNatRule -Name NatRule1 -Protocol "TCP" -SourceAddress "192.168.0.0/16" -DestinationAddress 10.20.30.40 -DestinationPort 1000 -TranslatedAddress "192.168.0.1" -TranslatedPort "100"
```

<span data-ttu-id="7c8a7-109">이 예제에서는 원본 주소, 프로토콜, 대상 주소, 대상 포트, 번역 된 주소 및 변환 된 포트를 사용 하 여 NAT 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="7c8a7-109">This example creates a NAT rule with the source address, protocol, destination address, destination port, translated address, and translated port.</span></span>

## <span data-ttu-id="7c8a7-110">변수</span><span class="sxs-lookup"><span data-stu-id="7c8a7-110">PARAMETERS</span></span>

### <span data-ttu-id="7c8a7-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c8a7-111">-DefaultProfile</span></span>
<span data-ttu-id="7c8a7-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7c8a7-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c8a7-113">-이름</span><span class="sxs-lookup"><span data-stu-id="7c8a7-113">-Name</span></span>
<span data-ttu-id="7c8a7-114">NAT 규칙 컬렉션의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7c8a7-114">The name of the NAT Rule Collection</span></span>

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

### <span data-ttu-id="7c8a7-115">-설명</span><span class="sxs-lookup"><span data-stu-id="7c8a7-115">-Description</span></span>
<span data-ttu-id="7c8a7-116">규칙에 대 한 설명</span><span class="sxs-lookup"><span data-stu-id="7c8a7-116">The description of the rule</span></span>

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

### <span data-ttu-id="7c8a7-117">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="7c8a7-117">-DestinationAddress</span></span>
<span data-ttu-id="7c8a7-118">규칙의 대상 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="7c8a7-118">The destination addresses of the rule.</span></span> <span data-ttu-id="7c8a7-119">이는 방화벽의 공용 IP 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c8a7-119">This has to be Public IP of the Firewall.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c8a7-120">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="7c8a7-120">-DestinationPort</span></span>
<span data-ttu-id="7c8a7-121">규칙의 대상 포트</span><span class="sxs-lookup"><span data-stu-id="7c8a7-121">The destination ports of the rule</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c8a7-122">-프로토콜</span><span class="sxs-lookup"><span data-stu-id="7c8a7-122">-Protocols</span></span>
<span data-ttu-id="7c8a7-123">규칙의 프로토콜</span><span class="sxs-lookup"><span data-stu-id="7c8a7-123">The protocols of the rule</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:
Accepted values: Any, TCP, UDP, ICMP

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c8a7-124">-SourceAddress</span><span class="sxs-lookup"><span data-stu-id="7c8a7-124">-SourceAddress</span></span>
<span data-ttu-id="7c8a7-125">규칙의 원본 주소</span><span class="sxs-lookup"><span data-stu-id="7c8a7-125">The source addresses of the rule</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c8a7-126">-SourceIpGroup</span><span class="sxs-lookup"><span data-stu-id="7c8a7-126">-SourceIpGroup</span></span>
<span data-ttu-id="7c8a7-127">규칙의 원본 ipgroups</span><span class="sxs-lookup"><span data-stu-id="7c8a7-127">The source ipgroups of the rule</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c8a7-128">-TranslatedAddress</span><span class="sxs-lookup"><span data-stu-id="7c8a7-128">-TranslatedAddress</span></span>
<span data-ttu-id="7c8a7-129">이 NAT 규칙의 번역 된 주소</span><span class="sxs-lookup"><span data-stu-id="7c8a7-129">The translated address for this NAT rule</span></span>

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

### <span data-ttu-id="7c8a7-130">-TranslatedPort</span><span class="sxs-lookup"><span data-stu-id="7c8a7-130">-TranslatedPort</span></span>
<span data-ttu-id="7c8a7-131">이 NAT 규칙에 대 한 변환 된 포트</span><span class="sxs-lookup"><span data-stu-id="7c8a7-131">The translated port for this NAT rule</span></span>

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

### <span data-ttu-id="7c8a7-132">-확인</span><span class="sxs-lookup"><span data-stu-id="7c8a7-132">-Confirm</span></span>
<span data-ttu-id="7c8a7-133">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c8a7-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c8a7-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7c8a7-134">-WhatIf</span></span>
<span data-ttu-id="7c8a7-135">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="7c8a7-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7c8a7-136">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7c8a7-136">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c8a7-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c8a7-137">CommonParameters</span></span>
<span data-ttu-id="7c8a7-138">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c8a7-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c8a7-139">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="7c8a7-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c8a7-140">입력</span><span class="sxs-lookup"><span data-stu-id="7c8a7-140">INPUTS</span></span>

### <span data-ttu-id="7c8a7-141">않아야</span><span class="sxs-lookup"><span data-stu-id="7c8a7-141">None</span></span>

## <span data-ttu-id="7c8a7-142">출력</span><span class="sxs-lookup"><span data-stu-id="7c8a7-142">OUTPUTS</span></span>

### <span data-ttu-id="7c8a7-143">PSAzureFirewallNatRule에 대 한.</span><span class="sxs-lookup"><span data-stu-id="7c8a7-143">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNatRule</span></span>

## <span data-ttu-id="7c8a7-144">상속자</span><span class="sxs-lookup"><span data-stu-id="7c8a7-144">NOTES</span></span>

## <span data-ttu-id="7c8a7-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7c8a7-145">RELATED LINKS</span></span>
