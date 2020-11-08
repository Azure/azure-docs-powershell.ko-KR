---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallpolicyfilterrulecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyFilterRuleCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyFilterRuleCollection.md
ms.openlocfilehash: d5871a9e1a99a27cc0b2728ca3638a0548f42fc6
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94216409"
---
# <span data-ttu-id="73ee5-101">New-AzFirewallPolicyFilterRuleCollection</span><span class="sxs-lookup"><span data-stu-id="73ee5-101">New-AzFirewallPolicyFilterRuleCollection</span></span>

## <span data-ttu-id="73ee5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="73ee5-102">SYNOPSIS</span></span>
<span data-ttu-id="73ee5-103">새 Azure 방화벽 정책 필터 규칙 모음 만들기</span><span class="sxs-lookup"><span data-stu-id="73ee5-103">Create a new Azure Firewall Policy Filter Rule Collection</span></span>

## <span data-ttu-id="73ee5-104">구문과</span><span class="sxs-lookup"><span data-stu-id="73ee5-104">SYNTAX</span></span>

```
New-AzFirewallPolicyFilterRuleCollection -Name <String> -Priority <UInt32> -Rule <PSAzureFirewallPolicyRule[]>
 -ActionType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="73ee5-105">설명은</span><span class="sxs-lookup"><span data-stu-id="73ee5-105">DESCRIPTION</span></span>
<span data-ttu-id="73ee5-106">**AzFirewallPolicyFilterRuleCollection** Cmdlet은 Azure 방화벽 정책에 대 한 필터 규칙 컬렉션을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="73ee5-106">The **New-AzFirewallPolicyFilterRuleCollection** cmdlet creates a Filter rule collection for a Azure Firewall Policy.</span></span>

## <span data-ttu-id="73ee5-107">예제의</span><span class="sxs-lookup"><span data-stu-id="73ee5-107">EXAMPLES</span></span>

### <span data-ttu-id="73ee5-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="73ee5-108">Example 1</span></span>
```powershell
PS C:\> New-AzFirewallPolicyFilterRuleCollection -Name FR1 -Priority 400 -Rule $appRule1 ,$appRule2 -ActionType "Allow"
```

<span data-ttu-id="73ee5-109">이 예제에서는 두 규칙 조건이 있는 필터 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="73ee5-109">This example creates a Filter rule with 2 rule conditions</span></span>

## <span data-ttu-id="73ee5-110">변수</span><span class="sxs-lookup"><span data-stu-id="73ee5-110">PARAMETERS</span></span>

### <span data-ttu-id="73ee5-111">-ActionType</span><span class="sxs-lookup"><span data-stu-id="73ee5-111">-ActionType</span></span>
<span data-ttu-id="73ee5-112">규칙 컬렉션의 동작</span><span class="sxs-lookup"><span data-stu-id="73ee5-112">The action of the rule collection</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Allow, Deny

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73ee5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73ee5-113">-DefaultProfile</span></span>
<span data-ttu-id="73ee5-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="73ee5-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="73ee5-115">-이름</span><span class="sxs-lookup"><span data-stu-id="73ee5-115">-Name</span></span>
<span data-ttu-id="73ee5-116">응용 프로그램 규칙 컬렉션의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="73ee5-116">The name of the Application Rule Collection</span></span>

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

### <span data-ttu-id="73ee5-117">-우선 순위</span><span class="sxs-lookup"><span data-stu-id="73ee5-117">-Priority</span></span>
<span data-ttu-id="73ee5-118">규칙 컬렉션의 우선 순위</span><span class="sxs-lookup"><span data-stu-id="73ee5-118">The priority of the rule collection</span></span>

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

### <span data-ttu-id="73ee5-119">-규칙</span><span class="sxs-lookup"><span data-stu-id="73ee5-119">-Rule</span></span>
<span data-ttu-id="73ee5-120">응용 프로그램 규칙 목록</span><span class="sxs-lookup"><span data-stu-id="73ee5-120">The list of application rules</span></span>

```yaml
Type: PSAzureFirewallPolicyRule[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73ee5-121">-확인</span><span class="sxs-lookup"><span data-stu-id="73ee5-121">-Confirm</span></span>
<span data-ttu-id="73ee5-122">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="73ee5-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="73ee5-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="73ee5-123">-WhatIf</span></span>
<span data-ttu-id="73ee5-124">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="73ee5-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="73ee5-125">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="73ee5-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="73ee5-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73ee5-126">CommonParameters</span></span>
<span data-ttu-id="73ee5-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="73ee5-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73ee5-128">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="73ee5-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73ee5-129">입력</span><span class="sxs-lookup"><span data-stu-id="73ee5-129">INPUTS</span></span>

### <span data-ttu-id="73ee5-130">않아야</span><span class="sxs-lookup"><span data-stu-id="73ee5-130">None</span></span>

## <span data-ttu-id="73ee5-131">출력</span><span class="sxs-lookup"><span data-stu-id="73ee5-131">OUTPUTS</span></span>

### <span data-ttu-id="73ee5-132">PSAzureFirewallPolicyRuleCollectionGroup에 대 한.</span><span class="sxs-lookup"><span data-stu-id="73ee5-132">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyRuleCollectionGroup</span></span>

## <span data-ttu-id="73ee5-133">상속자</span><span class="sxs-lookup"><span data-stu-id="73ee5-133">NOTES</span></span>

## <span data-ttu-id="73ee5-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="73ee5-134">RELATED LINKS</span></span>
