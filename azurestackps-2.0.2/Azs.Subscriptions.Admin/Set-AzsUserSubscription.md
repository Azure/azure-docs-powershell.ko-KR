---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/set-azsusersubscription
schema: 2.0.0
ms.openlocfilehash: fcf6254cfbb29add4990197dddf3fb188e665937
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/08/2020
ms.locfileid: "94047157"
---
# <span data-ttu-id="5f024-101">Set-AzsUserSubscription</span><span class="sxs-lookup"><span data-stu-id="5f024-101">Set-AzsUserSubscription</span></span>

## <span data-ttu-id="5f024-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5f024-102">SYNOPSIS</span></span>
<span data-ttu-id="5f024-103">지정 된 구독을 만들거나 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="5f024-103">Creates or updates the specified subscription.</span></span>

## <span data-ttu-id="5f024-104">구문과</span><span class="sxs-lookup"><span data-stu-id="5f024-104">SYNTAX</span></span>

### <span data-ttu-id="5f024-105">UpdateExpanded 됨 (기본값)</span><span class="sxs-lookup"><span data-stu-id="5f024-105">UpdateExpanded (Default)</span></span>
```
Set-AzsUserSubscription -TargetSubscriptionId <String> [-SubscriptionId <String>]
 [-DelegatedProviderSubscriptionId <String>] [-DisplayName <String>] [-ExternalReferenceId <String>]
 [-Id <String>] [-OfferId <String>] [-Owner <String>] [-RoutingResourceManagerType <ResourceManagerType>]
 [-State <SubscriptionState>] [-SubscriptionId1 <String>] [-TenantId <String>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="5f024-106">Update</span><span class="sxs-lookup"><span data-stu-id="5f024-106">Update</span></span>
```
Set-AzsUserSubscription -SubscriptionDefinition <ISubscriptionDefinition> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="5f024-107">설명은</span><span class="sxs-lookup"><span data-stu-id="5f024-107">DESCRIPTION</span></span>
<span data-ttu-id="5f024-108">지정 된 구독을 만들거나 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="5f024-108">Creates or updates the specified subscription.</span></span>

## <span data-ttu-id="5f024-109">예제의</span><span class="sxs-lookup"><span data-stu-id="5f024-109">EXAMPLES</span></span>

### <span data-ttu-id="5f024-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="5f024-110">Example 1</span></span>
```powershell
PS C:\> $Subscription = Get-AzsUserSubscription | Select-Object -First 1
$Subscription.DisplayName = 'Update User Subscription'
$Subscription | Set-AzsUserSubscription | fl *

DelegatedProviderSubscriptionId : d77ed1d7-cb62-4658-a777-386a8ae523dd
DisplayName                     : Update User Subscription
ExternalReferenceId             : 
Id                              : /subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/providers/Microsoft.Subscriptions.Admin/subscriptions/ffbffbe5-8905-4f51-b2ed-4717049de782
OfferId                         : /subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/resourceGroups/DRPTestResourceGroup5056/providers/Microsoft.Subscriptions.Admin/offers/DRPTestOffer5056
Owner                           : user@microsoft.com
RoutingResourceManagerType      : Default
State                           : Enabled
SubscriptionId                  : ffbffbe5-8905-4f51-b2ed-4717049de782
TenantId                        : 76440dfb-c97c-4fee-8f6c-dff8ddbe816f
```

<span data-ttu-id="5f024-111">구독 업데이트</span><span class="sxs-lookup"><span data-stu-id="5f024-111">Updates a subscription</span></span>

## <span data-ttu-id="5f024-112">변수</span><span class="sxs-lookup"><span data-stu-id="5f024-112">PARAMETERS</span></span>

### <span data-ttu-id="5f024-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f024-113">-DefaultProfile</span></span>
<span data-ttu-id="5f024-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5f024-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5f024-115">-DelegatedProviderSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="5f024-115">-DelegatedProviderSubscriptionId</span></span>
<span data-ttu-id="5f024-116">부모 DelegatedProvider 구독 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="5f024-116">Parent DelegatedProvider subscription identifier.</span></span>

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

### <span data-ttu-id="5f024-117">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="5f024-117">-DisplayName</span></span>
<span data-ttu-id="5f024-118">구독 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5f024-118">Subscription name.</span></span>

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

### <span data-ttu-id="5f024-119">-ExternalReferenceId</span><span class="sxs-lookup"><span data-stu-id="5f024-119">-ExternalReferenceId</span></span>
<span data-ttu-id="5f024-120">외부 참조 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="5f024-120">External reference identifier.</span></span>

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

### <span data-ttu-id="5f024-121">-Id</span><span class="sxs-lookup"><span data-stu-id="5f024-121">-Id</span></span>
<span data-ttu-id="5f024-122">정규화 된 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="5f024-122">Fully qualified identifier.</span></span>

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

### <span data-ttu-id="5f024-123">-OfferId</span><span class="sxs-lookup"><span data-stu-id="5f024-123">-OfferId</span></span>
<span data-ttu-id="5f024-124">위임 된 공급자 범위 아래에 있는 제안의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="5f024-124">Identifier of the offer under the scope of a delegated provider.</span></span>

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

### <span data-ttu-id="5f024-125">-소유자</span><span class="sxs-lookup"><span data-stu-id="5f024-125">-Owner</span></span>
<span data-ttu-id="5f024-126">구독 소유자입니다.</span><span class="sxs-lookup"><span data-stu-id="5f024-126">Subscription owner.</span></span>

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

### <span data-ttu-id="5f024-127">-RoutingResourceManagerType</span><span class="sxs-lookup"><span data-stu-id="5f024-127">-RoutingResourceManagerType</span></span>
<span data-ttu-id="5f024-128">라우팅 리소스 관리자 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="5f024-128">Routing resource manager type.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Support.ResourceManagerType
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="5f024-129">-상태</span><span class="sxs-lookup"><span data-stu-id="5f024-129">-State</span></span>
<span data-ttu-id="5f024-130">구독 상태입니다.</span><span class="sxs-lookup"><span data-stu-id="5f024-130">Subscription state.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Support.SubscriptionState
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="5f024-131">-구독 정의</span><span class="sxs-lookup"><span data-stu-id="5f024-131">-SubscriptionDefinition</span></span>
<span data-ttu-id="5f024-132">구독 개체 속성입니다.</span><span class="sxs-lookup"><span data-stu-id="5f024-132">Subscription object properties.</span></span>
<span data-ttu-id="5f024-133">생성 하려면 구독 정의 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5f024-133">To construct, see NOTES section for SUBSCRIPTIONDEFINITION properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.ISubscriptionDefinition
Parameter Sets: Update
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="5f024-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="5f024-134">-SubscriptionId</span></span>
<span data-ttu-id="5f024-135">Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명입니다. 구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="5f024-135">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="5f024-136">-SubscriptionId1</span><span class="sxs-lookup"><span data-stu-id="5f024-136">-SubscriptionId1</span></span>
<span data-ttu-id="5f024-137">구독 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="5f024-137">Subscription identifier.</span></span>

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

### <span data-ttu-id="5f024-138">-TargetSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="5f024-138">-TargetSubscriptionId</span></span>
<span data-ttu-id="5f024-139">대상 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="5f024-139">The target subscription ID.</span></span>

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

### <span data-ttu-id="5f024-140">-TenantId</span><span class="sxs-lookup"><span data-stu-id="5f024-140">-TenantId</span></span>
<span data-ttu-id="5f024-141">디렉터리 테 넌 트 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="5f024-141">Directory tenant identifier.</span></span>

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

### <span data-ttu-id="5f024-142">-확인</span><span class="sxs-lookup"><span data-stu-id="5f024-142">-Confirm</span></span>
<span data-ttu-id="5f024-143">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="5f024-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5f024-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5f024-144">-WhatIf</span></span>
<span data-ttu-id="5f024-145">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="5f024-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5f024-146">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5f024-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5f024-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f024-147">CommonParameters</span></span>
<span data-ttu-id="5f024-148">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="5f024-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f024-149">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="5f024-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f024-150">입력</span><span class="sxs-lookup"><span data-stu-id="5f024-150">INPUTS</span></span>

### <span data-ttu-id="5f024-151">SubscriptionsAdmin. Api20151101. i a PowerShell. ISubscriptionDefinition</span><span class="sxs-lookup"><span data-stu-id="5f024-151">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.ISubscriptionDefinition</span></span>

## <span data-ttu-id="5f024-152">출력</span><span class="sxs-lookup"><span data-stu-id="5f024-152">OUTPUTS</span></span>

### <span data-ttu-id="5f024-153">SubscriptionsAdmin. Api20151101. i a PowerShell. ISubscriptionDefinition</span><span class="sxs-lookup"><span data-stu-id="5f024-153">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.ISubscriptionDefinition</span></span>

<span data-ttu-id="5f024-154">별칭과</span><span class="sxs-lookup"><span data-stu-id="5f024-154">ALIASES</span></span>

## <span data-ttu-id="5f024-155">상속자</span><span class="sxs-lookup"><span data-stu-id="5f024-155">NOTES</span></span>

<span data-ttu-id="5f024-156">복잡 한 매개 변수 속성 아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="5f024-156">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="5f024-157">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="5f024-157">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="5f024-158">SUBSCRIPTIONDEFINITION <ISubscriptionDefinition> : 구독 개체 속성입니다.</span><span class="sxs-lookup"><span data-stu-id="5f024-158">SUBSCRIPTIONDEFINITION <ISubscriptionDefinition>: Subscription object properties.</span></span>
  - <span data-ttu-id="5f024-159">`[DelegatedProviderSubscriptionId <String>]`: Parent DelegatedProvider 구독 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="5f024-159">`[DelegatedProviderSubscriptionId <String>]`: Parent DelegatedProvider subscription identifier.</span></span>
  - <span data-ttu-id="5f024-160">`[DisplayName <String>]`: 구독 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5f024-160">`[DisplayName <String>]`: Subscription name.</span></span>
  - <span data-ttu-id="5f024-161">`[ExternalReferenceId <String>]`: 외부 참조 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="5f024-161">`[ExternalReferenceId <String>]`: External reference identifier.</span></span>
  - <span data-ttu-id="5f024-162">`[Id <String>]`: 정규화 된 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="5f024-162">`[Id <String>]`: Fully qualified identifier.</span></span>
  - <span data-ttu-id="5f024-163">`[OfferId <String>]`: 위임 된 공급자 범위 아래에 있는 제안의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="5f024-163">`[OfferId <String>]`: Identifier of the offer under the scope of a delegated provider.</span></span>
  - <span data-ttu-id="5f024-164">`[Owner <String>]`: 구독 소유자입니다.</span><span class="sxs-lookup"><span data-stu-id="5f024-164">`[Owner <String>]`: Subscription owner.</span></span>
  - <span data-ttu-id="5f024-165">`[RoutingResourceManagerType <ResourceManagerType?>]`: 라우팅 리소스 관리자 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="5f024-165">`[RoutingResourceManagerType <ResourceManagerType?>]`: Routing resource manager type.</span></span>
  - <span data-ttu-id="5f024-166">`[State <SubscriptionState?>]`: 구독 상태입니다.</span><span class="sxs-lookup"><span data-stu-id="5f024-166">`[State <SubscriptionState?>]`: Subscription state.</span></span>
  - <span data-ttu-id="5f024-167">`[SubscriptionId <String>]`: 구독 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="5f024-167">`[SubscriptionId <String>]`: Subscription identifier.</span></span>
  - <span data-ttu-id="5f024-168">`[TenantId <String>]`: 디렉터리 테 넌 트 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="5f024-168">`[TenantId <String>]`: Directory tenant identifier.</span></span>

## <span data-ttu-id="5f024-169">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5f024-169">RELATED LINKS</span></span>

