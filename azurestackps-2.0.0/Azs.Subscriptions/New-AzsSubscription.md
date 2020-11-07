---
external help file: ''
Module Name: Azs.Subscriptions
online version: https://docs.microsoft.com/powershell/module/azs.subscription/new-azssubscription
schema: 2.0.0
ms.openlocfilehash: ef8ee9ce81e8ba656a43330ac564c147bcd5d615
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93875244"
---
# <span data-ttu-id="0b622-101">New-AzsSubscription</span><span class="sxs-lookup"><span data-stu-id="0b622-101">New-AzsSubscription</span></span>

## <span data-ttu-id="0b622-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0b622-102">SYNOPSIS</span></span>
<span data-ttu-id="0b622-103">구독을 만들거나 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="0b622-103">Create or updates a subscription.</span></span>

## <span data-ttu-id="0b622-104">구문과</span><span class="sxs-lookup"><span data-stu-id="0b622-104">SYNTAX</span></span>

```
New-AzsSubscription -OfferId <String> [-SubscriptionId <String>] [-DisplayName <String>] [-Id <String>]
 [-State <SubscriptionState>] [-TenantId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="0b622-105">설명은</span><span class="sxs-lookup"><span data-stu-id="0b622-105">DESCRIPTION</span></span>
<span data-ttu-id="0b622-106">구독을 만들거나 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="0b622-106">Create or updates a subscription.</span></span>

## <span data-ttu-id="0b622-107">예제의</span><span class="sxs-lookup"><span data-stu-id="0b622-107">EXAMPLES</span></span>

### <span data-ttu-id="0b622-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="0b622-108">Example 1</span></span>
```powershell
PS C:\> New-AzsSubscription -OfferId '/delegatedProviders/default/offers/testoffer' -DisplayName 'testsubscription' | fl *

DisplayName    : testsubscription
Id             : /subscriptions/7b9d25c5-52ea-4940-8c6a-fe6749ab2e97
OfferId        : /delegatedProviders/default/offers/testoffer
State          : Enabled
SubscriptionId : 7b9d25c5-52ea-4940-8c6a-fe6749ab2e97
TenantId       : 6ca57aaf-0074-498a-9c96-2b097515e8cb
```

<span data-ttu-id="0b622-109">구독을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="0b622-109">Create a subscription.</span></span>

## <span data-ttu-id="0b622-110">변수</span><span class="sxs-lookup"><span data-stu-id="0b622-110">PARAMETERS</span></span>

### <span data-ttu-id="0b622-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b622-111">-DefaultProfile</span></span>
<span data-ttu-id="0b622-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0b622-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="0b622-113">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="0b622-113">-DisplayName</span></span>
<span data-ttu-id="0b622-114">구독 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0b622-114">Subscription name.</span></span>

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

### <span data-ttu-id="0b622-115">-Id</span><span class="sxs-lookup"><span data-stu-id="0b622-115">-Id</span></span>
<span data-ttu-id="0b622-116">정규화 된 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="0b622-116">Fully qualified identifier.</span></span>

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

### <span data-ttu-id="0b622-117">-OfferId</span><span class="sxs-lookup"><span data-stu-id="0b622-117">-OfferId</span></span>
<span data-ttu-id="0b622-118">위임 된 공급자 범위 아래에 있는 제안의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="0b622-118">Identifier of the offer under the scope of a delegated provider.</span></span>

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

### <span data-ttu-id="0b622-119">-상태</span><span class="sxs-lookup"><span data-stu-id="0b622-119">-State</span></span>
<span data-ttu-id="0b622-120">구독 상태입니다.</span><span class="sxs-lookup"><span data-stu-id="0b622-120">Subscription state.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Subscription.Support.SubscriptionState
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: Write-Output "Enabled"
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="0b622-121">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0b622-121">-SubscriptionId</span></span>
<span data-ttu-id="0b622-122">구독의 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="0b622-122">Id of the subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: $([Guid]::NewGuid().ToString())
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="0b622-123">-TenantId</span><span class="sxs-lookup"><span data-stu-id="0b622-123">-TenantId</span></span>
<span data-ttu-id="0b622-124">디렉터리 테 넌 트 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="0b622-124">Directory tenant identifier.</span></span>

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

### <span data-ttu-id="0b622-125">-확인</span><span class="sxs-lookup"><span data-stu-id="0b622-125">-Confirm</span></span>
<span data-ttu-id="0b622-126">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="0b622-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="0b622-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0b622-127">-WhatIf</span></span>
<span data-ttu-id="0b622-128">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="0b622-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0b622-129">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0b622-129">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="0b622-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b622-130">CommonParameters</span></span>
<span data-ttu-id="0b622-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0b622-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b622-132">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="0b622-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b622-133">입력</span><span class="sxs-lookup"><span data-stu-id="0b622-133">INPUTS</span></span>

## <span data-ttu-id="0b622-134">출력</span><span class="sxs-lookup"><span data-stu-id="0b622-134">OUTPUTS</span></span>

### <span data-ttu-id="0b622-135">Api20151101 (Microsoft. PowerShell. i i i 구독</span><span class="sxs-lookup"><span data-stu-id="0b622-135">Microsoft.Azure.PowerShell.Cmdlets.Subscription.Models.Api20151101.ISubscription</span></span>



## <span data-ttu-id="0b622-136">상속자</span><span class="sxs-lookup"><span data-stu-id="0b622-136">NOTES</span></span>

## <span data-ttu-id="0b622-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0b622-137">RELATED LINKS</span></span>

