---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azfirewallpolicynatrulecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyNatRuleCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyNatRuleCollection.md
ms.openlocfilehash: 4dd93dec5aad6fe0e77e92e44884c687d5841e49
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101960411"
---
# <span data-ttu-id="7938d-101">New-AzFirewallPolicyNatRuleCollection</span><span class="sxs-lookup"><span data-stu-id="7938d-101">New-AzFirewallPolicyNatRuleCollection</span></span>

## <span data-ttu-id="7938d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7938d-102">SYNOPSIS</span></span>
<span data-ttu-id="7938d-103">새 Azure Firewall Policy Nat Rule Collection 만들기</span><span class="sxs-lookup"><span data-stu-id="7938d-103">Create a new Azure Firewall Policy Nat Rule Collection</span></span>

## <span data-ttu-id="7938d-104">구문</span><span class="sxs-lookup"><span data-stu-id="7938d-104">SYNTAX</span></span>

```
New-AzFirewallPolicyNatRuleCollection -Name <String> -Priority <UInt32>
 -Rule <PSAzureFirewallPolicyNetworkRule> -ActionType <String> -TranslatedAddress <String>
 -TranslatedPort <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7938d-105">설명</span><span class="sxs-lookup"><span data-stu-id="7938d-105">DESCRIPTION</span></span>
<span data-ttu-id="7938d-106">**New-AzFirewallPolicyNatRuleCollection** cmdlet은 Azure 방화벽 정책에 대한 Nat 규칙 컬렉션을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="7938d-106">The **New-AzFirewallPolicyNatRuleCollection** cmdlet creates a Nat rule collection for a Azure Firewall Policy.</span></span>

## <span data-ttu-id="7938d-107">예제</span><span class="sxs-lookup"><span data-stu-id="7938d-107">EXAMPLES</span></span>

### <span data-ttu-id="7938d-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="7938d-108">Example 1</span></span>
```powershell
PS C:\> New-AzFirewallPolicyNatRuleCollection -Name NatRule1 -Priority 200 -Rule $netRule1 -ActionType "Dnat" -TranslatedAddress "192.168.0.1" -TranslatedPort "100"
```

<span data-ttu-id="7938d-109">이 예제에서는 네트워크 규칙이 있는 nat 규칙 컬렉션을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="7938d-109">This example creates a nat rule collection with a network rule</span></span>

## <span data-ttu-id="7938d-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="7938d-110">PARAMETERS</span></span>

### <span data-ttu-id="7938d-111">-ActionType</span><span class="sxs-lookup"><span data-stu-id="7938d-111">-ActionType</span></span>
<span data-ttu-id="7938d-112">규칙 작업의 형식</span><span class="sxs-lookup"><span data-stu-id="7938d-112">The type of the rule action</span></span>

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

### <span data-ttu-id="7938d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7938d-113">-DefaultProfile</span></span>
<span data-ttu-id="7938d-114">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7938d-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7938d-115">-Name</span><span class="sxs-lookup"><span data-stu-id="7938d-115">-Name</span></span>
<span data-ttu-id="7938d-116">네트워크 규칙 컬렉션의 이름</span><span class="sxs-lookup"><span data-stu-id="7938d-116">The name of the Network Rule Collection</span></span>

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

### <span data-ttu-id="7938d-117">-Priority</span><span class="sxs-lookup"><span data-stu-id="7938d-117">-Priority</span></span>
<span data-ttu-id="7938d-118">규칙 컬렉션의 우선 순위</span><span class="sxs-lookup"><span data-stu-id="7938d-118">The priority of the rule collection</span></span>

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

### <span data-ttu-id="7938d-119">-Rule</span><span class="sxs-lookup"><span data-stu-id="7938d-119">-Rule</span></span>
<span data-ttu-id="7938d-120">네트워크 규칙 목록</span><span class="sxs-lookup"><span data-stu-id="7938d-120">The list of network rules</span></span>

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

### <span data-ttu-id="7938d-121">-TranslatedAddress</span><span class="sxs-lookup"><span data-stu-id="7938d-121">-TranslatedAddress</span></span>
<span data-ttu-id="7938d-122">이 NAT 규칙에 대한 번역된 주소</span><span class="sxs-lookup"><span data-stu-id="7938d-122">The translated address for this NAT rule</span></span>

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

### <span data-ttu-id="7938d-123">-TranslatedPort</span><span class="sxs-lookup"><span data-stu-id="7938d-123">-TranslatedPort</span></span>
<span data-ttu-id="7938d-124">이 NAT 규칙에 대한 번역된 포트</span><span class="sxs-lookup"><span data-stu-id="7938d-124">The translated port for this NAT rule</span></span>

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

### <span data-ttu-id="7938d-125">-확인</span><span class="sxs-lookup"><span data-stu-id="7938d-125">-Confirm</span></span>
<span data-ttu-id="7938d-126">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="7938d-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7938d-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7938d-127">-WhatIf</span></span>
<span data-ttu-id="7938d-128">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="7938d-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7938d-129">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7938d-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7938d-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7938d-130">CommonParameters</span></span>
<span data-ttu-id="7938d-131">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="7938d-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7938d-132">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7938d-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7938d-133">입력</span><span class="sxs-lookup"><span data-stu-id="7938d-133">INPUTS</span></span>

### <span data-ttu-id="7938d-134">없음</span><span class="sxs-lookup"><span data-stu-id="7938d-134">None</span></span>

## <span data-ttu-id="7938d-135">출력</span><span class="sxs-lookup"><span data-stu-id="7938d-135">OUTPUTS</span></span>

### <span data-ttu-id="7938d-136">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRuleCollection</span><span class="sxs-lookup"><span data-stu-id="7938d-136">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRuleCollection</span></span>

## <span data-ttu-id="7938d-137">참고 사항</span><span class="sxs-lookup"><span data-stu-id="7938d-137">NOTES</span></span>

## <span data-ttu-id="7938d-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7938d-138">RELATED LINKS</span></span>
