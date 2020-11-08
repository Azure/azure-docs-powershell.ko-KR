---
external help file: ''
Module Name: Azs.Subscriptions
online version: https://docs.microsoft.com/powershell/module/azs.subscription/set-azssubscription
schema: 2.0.0
ms.openlocfilehash: d4636bb8f6e3fdbe9fc1911c173680f966e0f9e4
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/08/2020
ms.locfileid: "94047020"
---
# <span data-ttu-id="55338-101">Set-AzsSubscription</span><span class="sxs-lookup"><span data-stu-id="55338-101">Set-AzsSubscription</span></span>

## <span data-ttu-id="55338-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="55338-102">SYNOPSIS</span></span>
<span data-ttu-id="55338-103">구독을 만들거나 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="55338-103">Create or updates a subscription.</span></span>

## <span data-ttu-id="55338-104">구문과</span><span class="sxs-lookup"><span data-stu-id="55338-104">SYNTAX</span></span>

### <span data-ttu-id="55338-105">UpdateExpanded 됨 (기본값)</span><span class="sxs-lookup"><span data-stu-id="55338-105">UpdateExpanded (Default)</span></span>
```
Set-AzsSubscription -SubscriptionId <String> [-DisplayName <String>] [-Id <String>] [-OfferId <String>]
 [-State <SubscriptionState>] [-TenantId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="55338-106">Update</span><span class="sxs-lookup"><span data-stu-id="55338-106">Update</span></span>
```
Set-AzsSubscription -SubscriptionDefinition <ISubscription> [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="55338-107">설명은</span><span class="sxs-lookup"><span data-stu-id="55338-107">DESCRIPTION</span></span>
<span data-ttu-id="55338-108">구독을 만들거나 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="55338-108">Create or updates a subscription.</span></span>

## <span data-ttu-id="55338-109">예제의</span><span class="sxs-lookup"><span data-stu-id="55338-109">EXAMPLES</span></span>

### <span data-ttu-id="55338-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="55338-110">Example 1</span></span>
```powershell
PS C:\> $subscription = Get-AzsSubscription | where DisplayName -eq 'testsubscription'
$subscription.DisplayName = 'update subscription'
$subscription | Set-AzsSubscription | fl *

DisplayName    : update subscription
Id             : /subscriptions/f6f9665e-9831-4ac6-a2c3-26a591b9e6e8
OfferId        : /delegatedProviders/default/offers/TestOffer-fef68214-ba47-469c-89a7-07faf7947ad6
State          : Enabled
SubscriptionId : f6f9665e-9831-4ac6-a2c3-26a591b9e6e8
TenantId       : 6ca57aaf-0074-498a-9c96-2b097515e8cb
```

<span data-ttu-id="55338-111">구독을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="55338-111">Updates a subscription.</span></span>

## <span data-ttu-id="55338-112">변수</span><span class="sxs-lookup"><span data-stu-id="55338-112">PARAMETERS</span></span>

### <span data-ttu-id="55338-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55338-113">-DefaultProfile</span></span>
<span data-ttu-id="55338-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="55338-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="55338-115">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="55338-115">-DisplayName</span></span>
<span data-ttu-id="55338-116">구독 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="55338-116">Subscription name.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="55338-117">-Id</span><span class="sxs-lookup"><span data-stu-id="55338-117">-Id</span></span>
<span data-ttu-id="55338-118">정규화 된 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="55338-118">Fully qualified identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="55338-119">-OfferId</span><span class="sxs-lookup"><span data-stu-id="55338-119">-OfferId</span></span>
<span data-ttu-id="55338-120">위임 된 공급자 범위 아래에 있는 제안의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="55338-120">Identifier of the offer under the scope of a delegated provider.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="55338-121">-상태</span><span class="sxs-lookup"><span data-stu-id="55338-121">-State</span></span>
<span data-ttu-id="55338-122">구독 상태입니다.</span><span class="sxs-lookup"><span data-stu-id="55338-122">Subscription state.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Subscription.Support.SubscriptionState
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="55338-123">-구독 정의</span><span class="sxs-lookup"><span data-stu-id="55338-123">-SubscriptionDefinition</span></span>
<span data-ttu-id="55338-124">지원 되는 작업 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="55338-124">List of supported operations.</span></span>
<span data-ttu-id="55338-125">생성 하려면 구독 정의 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="55338-125">To construct, see NOTES section for SUBSCRIPTIONDEFINITION properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Subscription.Models.Api20151101.ISubscription
Parameter Sets: Update
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="55338-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="55338-126">-SubscriptionId</span></span>
<span data-ttu-id="55338-127">구독의 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="55338-127">Id of the subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="55338-128">-TenantId</span><span class="sxs-lookup"><span data-stu-id="55338-128">-TenantId</span></span>
<span data-ttu-id="55338-129">디렉터리 테 넌 트 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="55338-129">Directory tenant identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="55338-130">-확인</span><span class="sxs-lookup"><span data-stu-id="55338-130">-Confirm</span></span>
<span data-ttu-id="55338-131">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="55338-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="55338-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="55338-132">-WhatIf</span></span>
<span data-ttu-id="55338-133">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="55338-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="55338-134">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="55338-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="55338-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55338-135">CommonParameters</span></span>
<span data-ttu-id="55338-136">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="55338-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55338-137">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="55338-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55338-138">입력</span><span class="sxs-lookup"><span data-stu-id="55338-138">INPUTS</span></span>

### <span data-ttu-id="55338-139">Api20151101 (Microsoft. PowerShell. i i i 구독</span><span class="sxs-lookup"><span data-stu-id="55338-139">Microsoft.Azure.PowerShell.Cmdlets.Subscription.Models.Api20151101.ISubscription</span></span>

## <span data-ttu-id="55338-140">출력</span><span class="sxs-lookup"><span data-stu-id="55338-140">OUTPUTS</span></span>

### <span data-ttu-id="55338-141">Api20151101 (Microsoft. PowerShell. i i i 구독</span><span class="sxs-lookup"><span data-stu-id="55338-141">Microsoft.Azure.PowerShell.Cmdlets.Subscription.Models.Api20151101.ISubscription</span></span>



## <span data-ttu-id="55338-142">상속자</span><span class="sxs-lookup"><span data-stu-id="55338-142">NOTES</span></span>

<span data-ttu-id="55338-143">복잡 한 매개 변수 속성 아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="55338-143">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="55338-144">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="55338-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="55338-145">구독 정의 <ISubscription> : 지원 되는 작업 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="55338-145">SUBSCRIPTIONDEFINITION <ISubscription>: List of supported operations.</span></span>
  - <span data-ttu-id="55338-146">`[DisplayName <String>]`: 구독 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="55338-146">`[DisplayName <String>]`: Subscription name.</span></span>
  - <span data-ttu-id="55338-147">`[Id <String>]`: 정규화 된 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="55338-147">`[Id <String>]`: Fully qualified identifier.</span></span>
  - <span data-ttu-id="55338-148">`[OfferId <String>]`: 위임 된 공급자 범위 아래에 있는 제안의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="55338-148">`[OfferId <String>]`: Identifier of the offer under the scope of a delegated provider.</span></span>
  - <span data-ttu-id="55338-149">`[State <SubscriptionState?>]`: 구독 상태입니다.</span><span class="sxs-lookup"><span data-stu-id="55338-149">`[State <SubscriptionState?>]`: Subscription state.</span></span>
  - <span data-ttu-id="55338-150">`[SubscriptionId <String>]`: 구독 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="55338-150">`[SubscriptionId <String>]`: Subscription identifier.</span></span>
  - <span data-ttu-id="55338-151">`[TenantId <String>]`: 디렉터리 테 넌 트 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="55338-151">`[TenantId <String>]`: Directory tenant identifier.</span></span>

## <span data-ttu-id="55338-152">관련 링크</span><span class="sxs-lookup"><span data-stu-id="55338-152">RELATED LINKS</span></span>

