---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallpolicyfilterrulecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyFilterRuleCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyFilterRuleCollection.md
ms.openlocfilehash: d5871a9e1a99a27cc0b2728ca3638a0548f42fc6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100191865"
---
# <span data-ttu-id="95d42-101">New-AzFirewallPolicyFilterRuleCollection</span><span class="sxs-lookup"><span data-stu-id="95d42-101">New-AzFirewallPolicyFilterRuleCollection</span></span>

## <span data-ttu-id="95d42-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="95d42-102">SYNOPSIS</span></span>
<span data-ttu-id="95d42-103">새 Azure Firewall 정책 필터 규칙 컬렉션 만들기</span><span class="sxs-lookup"><span data-stu-id="95d42-103">Create a new Azure Firewall Policy Filter Rule Collection</span></span>

## <span data-ttu-id="95d42-104">구문</span><span class="sxs-lookup"><span data-stu-id="95d42-104">SYNTAX</span></span>

```
New-AzFirewallPolicyFilterRuleCollection -Name <String> -Priority <UInt32> -Rule <PSAzureFirewallPolicyRule[]>
 -ActionType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="95d42-105">설명</span><span class="sxs-lookup"><span data-stu-id="95d42-105">DESCRIPTION</span></span>
<span data-ttu-id="95d42-106">**New-AzFirewallPolicyFilterRuleCollection** cmdlet은 Azure Firewall 정책에 대한 필터 규칙 컬렉션을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="95d42-106">The **New-AzFirewallPolicyFilterRuleCollection** cmdlet creates a Filter rule collection for a Azure Firewall Policy.</span></span>

## <span data-ttu-id="95d42-107">예제</span><span class="sxs-lookup"><span data-stu-id="95d42-107">EXAMPLES</span></span>

### <span data-ttu-id="95d42-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="95d42-108">Example 1</span></span>
```powershell
PS C:\> New-AzFirewallPolicyFilterRuleCollection -Name FR1 -Priority 400 -Rule $appRule1 ,$appRule2 -ActionType "Allow"
```

<span data-ttu-id="95d42-109">이 예제에서는 2개 규칙 조건이 있는 필터 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="95d42-109">This example creates a Filter rule with 2 rule conditions</span></span>

## <span data-ttu-id="95d42-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="95d42-110">PARAMETERS</span></span>

### <span data-ttu-id="95d42-111">-ActionType</span><span class="sxs-lookup"><span data-stu-id="95d42-111">-ActionType</span></span>
<span data-ttu-id="95d42-112">규칙 컬렉션의 작업</span><span class="sxs-lookup"><span data-stu-id="95d42-112">The action of the rule collection</span></span>

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

### <span data-ttu-id="95d42-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95d42-113">-DefaultProfile</span></span>
<span data-ttu-id="95d42-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="95d42-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="95d42-115">-Name</span><span class="sxs-lookup"><span data-stu-id="95d42-115">-Name</span></span>
<span data-ttu-id="95d42-116">애플리케이션 규칙 컬렉션의 이름</span><span class="sxs-lookup"><span data-stu-id="95d42-116">The name of the Application Rule Collection</span></span>

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

### <span data-ttu-id="95d42-117">-Priority</span><span class="sxs-lookup"><span data-stu-id="95d42-117">-Priority</span></span>
<span data-ttu-id="95d42-118">규칙 컬렉션의 우선 순위</span><span class="sxs-lookup"><span data-stu-id="95d42-118">The priority of the rule collection</span></span>

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

### <span data-ttu-id="95d42-119">-Rule</span><span class="sxs-lookup"><span data-stu-id="95d42-119">-Rule</span></span>
<span data-ttu-id="95d42-120">애플리케이션 규칙 목록</span><span class="sxs-lookup"><span data-stu-id="95d42-120">The list of application rules</span></span>

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

### <span data-ttu-id="95d42-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="95d42-121">-Confirm</span></span>
<span data-ttu-id="95d42-122">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="95d42-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="95d42-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="95d42-123">-WhatIf</span></span>
<span data-ttu-id="95d42-124">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="95d42-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="95d42-125">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="95d42-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="95d42-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95d42-126">CommonParameters</span></span>
<span data-ttu-id="95d42-127">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="95d42-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95d42-128">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="95d42-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95d42-129">입력</span><span class="sxs-lookup"><span data-stu-id="95d42-129">INPUTS</span></span>

### <span data-ttu-id="95d42-130">없음</span><span class="sxs-lookup"><span data-stu-id="95d42-130">None</span></span>

## <span data-ttu-id="95d42-131">출력</span><span class="sxs-lookup"><span data-stu-id="95d42-131">OUTPUTS</span></span>

### <span data-ttu-id="95d42-132">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyRuleCollectionGroup</span><span class="sxs-lookup"><span data-stu-id="95d42-132">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyRuleCollectionGroup</span></span>

## <span data-ttu-id="95d42-133">참고 사항</span><span class="sxs-lookup"><span data-stu-id="95d42-133">NOTES</span></span>

## <span data-ttu-id="95d42-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="95d42-134">RELATED LINKS</span></span>
