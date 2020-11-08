---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallpolicynatrulecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyNatRuleCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyNatRuleCollection.md
ms.openlocfilehash: 010fd83d8b8e26e67e35afcc54b03ca0c1a5bd5a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94042980"
---
# <span data-ttu-id="c08b1-101">New-AzFirewallPolicyNatRuleCollection</span><span class="sxs-lookup"><span data-stu-id="c08b1-101">New-AzFirewallPolicyNatRuleCollection</span></span>

## <span data-ttu-id="c08b1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c08b1-102">SYNOPSIS</span></span>
<span data-ttu-id="c08b1-103">새 Azure 방화벽 정책 Nat 규칙 모음 만들기</span><span class="sxs-lookup"><span data-stu-id="c08b1-103">Create a new Azure Firewall Policy Nat Rule Collection</span></span>

## <span data-ttu-id="c08b1-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c08b1-104">SYNTAX</span></span>

```
New-AzFirewallPolicyNatRuleCollection -Name <String> -Priority <UInt32>
 -Rule <PSAzureFirewallPolicyNetworkRule> -ActionType <String> -TranslatedAddress <String>
 -TranslatedPort <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c08b1-105">설명은</span><span class="sxs-lookup"><span data-stu-id="c08b1-105">DESCRIPTION</span></span>
<span data-ttu-id="c08b1-106">**AzFirewallPolicyNatRuleCollection** Cmdlet은 Azure 방화벽 정책에 대 한 Nat 규칙 컬렉션을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c08b1-106">The **New-AzFirewallPolicyNatRuleCollection** cmdlet creates a Nat rule collection for a Azure Firewall Policy.</span></span>

## <span data-ttu-id="c08b1-107">예제의</span><span class="sxs-lookup"><span data-stu-id="c08b1-107">EXAMPLES</span></span>

### <span data-ttu-id="c08b1-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="c08b1-108">Example 1</span></span>
```powershell
PS C:\> New-AzFirewallPolicyNatRuleCollection -Name NatRule1 -Priority 200 -Rule $netRule1 -ActionType "Dnat" -TranslatedAddress "192.168.0.1" -TranslatedPort "100"
```

<span data-ttu-id="c08b1-109">이 예제에서는 네트워크 규칙을 사용 하 여 nat 규칙 모음을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c08b1-109">This example creates a nat rule collection with a network rule</span></span>

## <span data-ttu-id="c08b1-110">변수</span><span class="sxs-lookup"><span data-stu-id="c08b1-110">PARAMETERS</span></span>

### <span data-ttu-id="c08b1-111">-ActionType</span><span class="sxs-lookup"><span data-stu-id="c08b1-111">-ActionType</span></span>
<span data-ttu-id="c08b1-112">규칙 동작의 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="c08b1-112">The type of the rule action</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Dnat

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c08b1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c08b1-113">-DefaultProfile</span></span>
<span data-ttu-id="c08b1-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c08b1-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c08b1-115">-이름</span><span class="sxs-lookup"><span data-stu-id="c08b1-115">-Name</span></span>
<span data-ttu-id="c08b1-116">네트워크 규칙 모음의 이름</span><span class="sxs-lookup"><span data-stu-id="c08b1-116">The name of the Network Rule Collection</span></span>

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

### <span data-ttu-id="c08b1-117">-우선 순위</span><span class="sxs-lookup"><span data-stu-id="c08b1-117">-Priority</span></span>
<span data-ttu-id="c08b1-118">규칙 컬렉션의 우선 순위</span><span class="sxs-lookup"><span data-stu-id="c08b1-118">The priority of the rule collection</span></span>

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c08b1-119">-규칙</span><span class="sxs-lookup"><span data-stu-id="c08b1-119">-Rule</span></span>
<span data-ttu-id="c08b1-120">네트워크 규칙 목록</span><span class="sxs-lookup"><span data-stu-id="c08b1-120">The list of network rules</span></span>

```yaml
Type: PSAzureFirewallPolicyNetworkRule
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c08b1-121">-TranslatedAddress</span><span class="sxs-lookup"><span data-stu-id="c08b1-121">-TranslatedAddress</span></span>
<span data-ttu-id="c08b1-122">이 NAT 규칙의 번역 된 주소</span><span class="sxs-lookup"><span data-stu-id="c08b1-122">The translated address for this NAT rule</span></span>

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

### <span data-ttu-id="c08b1-123">-TranslatedPort</span><span class="sxs-lookup"><span data-stu-id="c08b1-123">-TranslatedPort</span></span>
<span data-ttu-id="c08b1-124">이 NAT 규칙에 대 한 변환 된 포트</span><span class="sxs-lookup"><span data-stu-id="c08b1-124">The translated port for this NAT rule</span></span>

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

### <span data-ttu-id="c08b1-125">-확인</span><span class="sxs-lookup"><span data-stu-id="c08b1-125">-Confirm</span></span>
<span data-ttu-id="c08b1-126">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="c08b1-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c08b1-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c08b1-127">-WhatIf</span></span>
<span data-ttu-id="c08b1-128">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="c08b1-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c08b1-129">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c08b1-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c08b1-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c08b1-130">CommonParameters</span></span>
<span data-ttu-id="c08b1-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c08b1-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c08b1-132">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="c08b1-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c08b1-133">입력</span><span class="sxs-lookup"><span data-stu-id="c08b1-133">INPUTS</span></span>

### <span data-ttu-id="c08b1-134">않아야</span><span class="sxs-lookup"><span data-stu-id="c08b1-134">None</span></span>

## <span data-ttu-id="c08b1-135">출력</span><span class="sxs-lookup"><span data-stu-id="c08b1-135">OUTPUTS</span></span>

### <span data-ttu-id="c08b1-136">PSAzureFirewallNetworkRuleCollection에 대 한.</span><span class="sxs-lookup"><span data-stu-id="c08b1-136">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRuleCollection</span></span>

## <span data-ttu-id="c08b1-137">상속자</span><span class="sxs-lookup"><span data-stu-id="c08b1-137">NOTES</span></span>

## <span data-ttu-id="c08b1-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c08b1-138">RELATED LINKS</span></span>
