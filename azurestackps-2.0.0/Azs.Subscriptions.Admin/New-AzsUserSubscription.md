---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/new-azsusersubscription
schema: 2.0.0
ms.openlocfilehash: 6ccc47c6b6254e23050cf4341cae355bda78d8df
ms.sourcegitcommit: 308ebca475d1c37624d7a10a2c02047594f44cdf
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/22/2020
ms.locfileid: "94045116"
---
# <span data-ttu-id="e7f5c-101">New-AzsUserSubscription</span><span class="sxs-lookup"><span data-stu-id="e7f5c-101">New-AzsUserSubscription</span></span>

## <span data-ttu-id="e7f5c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e7f5c-102">SYNOPSIS</span></span>
<span data-ttu-id="e7f5c-103">지정 된 구독을 만들거나 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="e7f5c-103">Creates or updates the specified subscription.</span></span>

## <span data-ttu-id="e7f5c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e7f5c-104">SYNTAX</span></span>

### <span data-ttu-id="e7f5c-105">CreateExpanded (기본값)</span><span class="sxs-lookup"><span data-stu-id="e7f5c-105">CreateExpanded (Default)</span></span>
```
New-AzsUserSubscription -OfferId <String> -Owner <String> [-TargetSubscriptionId <String>]
 [-DelegatedProviderSubscriptionId <String>] [-DisplayName <String>] [-ExternalReferenceId <String>]
 [-Id <String>] [-RoutingResourceManagerType <ResourceManagerType>] [-State <SubscriptionState>]
 [-TenantId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="e7f5c-106">만드는</span><span class="sxs-lookup"><span data-stu-id="e7f5c-106">Create</span></span>
```
New-AzsUserSubscription -SubscriptionDefinition <ISubscriptionDefinition> [-TargetSubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="e7f5c-107">설명은</span><span class="sxs-lookup"><span data-stu-id="e7f5c-107">DESCRIPTION</span></span>
<span data-ttu-id="e7f5c-108">지정 된 구독을 만들거나 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="e7f5c-108">Creates or updates the specified subscription.</span></span>

## <span data-ttu-id="e7f5c-109">예제의</span><span class="sxs-lookup"><span data-stu-id="e7f5c-109">EXAMPLES</span></span>

### <span data-ttu-id="e7f5c-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="e7f5c-110">Example 1</span></span>
```powershell
PS C:\> New-AzsUserSubscription -Owner "user@contoso.com" -OfferId "/subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/resourceGroups/TenantResourceGroup/providers/Microsoft.Subscriptions.Admin/offers/TenantOffer" | fl *

DelegatedProviderSubscriptionId : d77ed1d7-cb62-4658-a777-386a8ae523dd
DisplayName                     : 
ExternalReferenceId             : 
Id                              : /subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/providers/Microsoft.Subscriptions.Admin/subscriptions/398466a8-7d43-455a-b842-772d356d119e
OfferId                         : /subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/resourceGroups/TenantResourceGroup/providers/Microsoft.Subscriptions.Admin/offers/TenantOff
                                  er
Owner                           : user@contoso.com
RoutingResourceManagerType      : Default
State                           : Enabled
SubscriptionId                  : 398466a8-7d43-455a-b842-772d356d119e
TenantId                        : 6ca57aaf-0074-498a-9c96-2b097515e8cb
```

<span data-ttu-id="e7f5c-111">새 사용자 구독 만들기</span><span class="sxs-lookup"><span data-stu-id="e7f5c-111">Creates a new user subscription</span></span>

## <span data-ttu-id="e7f5c-112">변수</span><span class="sxs-lookup"><span data-stu-id="e7f5c-112">PARAMETERS</span></span>

### <span data-ttu-id="e7f5c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7f5c-113">-DefaultProfile</span></span>
<span data-ttu-id="e7f5c-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e7f5c-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e7f5c-115">-DelegatedProviderSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e7f5c-115">-DelegatedProviderSubscriptionId</span></span>
<span data-ttu-id="e7f5c-116">부모 DelegatedProvider 구독 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="e7f5c-116">Parent DelegatedProvider subscription identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="e7f5c-117">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="e7f5c-117">-DisplayName</span></span>
<span data-ttu-id="e7f5c-118">구독 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e7f5c-118">Subscription name.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="e7f5c-119">-ExternalReferenceId</span><span class="sxs-lookup"><span data-stu-id="e7f5c-119">-ExternalReferenceId</span></span>
<span data-ttu-id="e7f5c-120">외부 참조 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="e7f5c-120">External reference identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="e7f5c-121">-Id</span><span class="sxs-lookup"><span data-stu-id="e7f5c-121">-Id</span></span>
<span data-ttu-id="e7f5c-122">정규화 된 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="e7f5c-122">Fully qualified identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="e7f5c-123">-OfferId</span><span class="sxs-lookup"><span data-stu-id="e7f5c-123">-OfferId</span></span>
<span data-ttu-id="e7f5c-124">위임 된 공급자 범위 아래에 있는 제안의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="e7f5c-124">Identifier of the offer under the scope of a delegated provider.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="e7f5c-125">-소유자</span><span class="sxs-lookup"><span data-stu-id="e7f5c-125">-Owner</span></span>
<span data-ttu-id="e7f5c-126">구독 소유자입니다.</span><span class="sxs-lookup"><span data-stu-id="e7f5c-126">Subscription owner.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="e7f5c-127">-RoutingResourceManagerType</span><span class="sxs-lookup"><span data-stu-id="e7f5c-127">-RoutingResourceManagerType</span></span>
<span data-ttu-id="e7f5c-128">라우팅 리소스 관리자 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="e7f5c-128">Routing resource manager type.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Support.ResourceManagerType
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: Write-Output "Default"
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="e7f5c-129">-상태</span><span class="sxs-lookup"><span data-stu-id="e7f5c-129">-State</span></span>
<span data-ttu-id="e7f5c-130">구독 상태입니다.</span><span class="sxs-lookup"><span data-stu-id="e7f5c-130">Subscription state.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Support.SubscriptionState
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: Write-Output "Enabled"
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="e7f5c-131">-구독 정의</span><span class="sxs-lookup"><span data-stu-id="e7f5c-131">-SubscriptionDefinition</span></span>
<span data-ttu-id="e7f5c-132">구독 개체 속성입니다.</span><span class="sxs-lookup"><span data-stu-id="e7f5c-132">Subscription object properties.</span></span>
<span data-ttu-id="e7f5c-133">생성 하려면 구독 정의 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e7f5c-133">To construct, see NOTES section for SUBSCRIPTIONDEFINITION properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.ISubscriptionDefinition
Parameter Sets: Create
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="e7f5c-134">-TargetSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e7f5c-134">-TargetSubscriptionId</span></span>
<span data-ttu-id="e7f5c-135">대상 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="e7f5c-135">The target subscription ID.</span></span>

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

### <span data-ttu-id="e7f5c-136">-TenantId</span><span class="sxs-lookup"><span data-stu-id="e7f5c-136">-TenantId</span></span>
<span data-ttu-id="e7f5c-137">디렉터리 테 넌 트 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="e7f5c-137">Directory tenant identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="e7f5c-138">-확인</span><span class="sxs-lookup"><span data-stu-id="e7f5c-138">-Confirm</span></span>
<span data-ttu-id="e7f5c-139">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="e7f5c-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e7f5c-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e7f5c-140">-WhatIf</span></span>
<span data-ttu-id="e7f5c-141">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="e7f5c-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e7f5c-142">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e7f5c-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e7f5c-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7f5c-143">CommonParameters</span></span>
<span data-ttu-id="e7f5c-144">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e7f5c-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7f5c-145">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="e7f5c-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7f5c-146">입력</span><span class="sxs-lookup"><span data-stu-id="e7f5c-146">INPUTS</span></span>

### <span data-ttu-id="e7f5c-147">SubscriptionsAdmin. Api20151101. i a PowerShell. ISubscriptionDefinition</span><span class="sxs-lookup"><span data-stu-id="e7f5c-147">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.ISubscriptionDefinition</span></span>

## <span data-ttu-id="e7f5c-148">출력</span><span class="sxs-lookup"><span data-stu-id="e7f5c-148">OUTPUTS</span></span>

### <span data-ttu-id="e7f5c-149">SubscriptionsAdmin. Api20151101. i a PowerShell. ISubscriptionDefinition</span><span class="sxs-lookup"><span data-stu-id="e7f5c-149">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.ISubscriptionDefinition</span></span>

<span data-ttu-id="e7f5c-150">별칭과</span><span class="sxs-lookup"><span data-stu-id="e7f5c-150">ALIASES</span></span>

## <span data-ttu-id="e7f5c-151">상속자</span><span class="sxs-lookup"><span data-stu-id="e7f5c-151">NOTES</span></span>

<span data-ttu-id="e7f5c-152">복잡 한 매개 변수 속성 아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="e7f5c-152">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e7f5c-153">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="e7f5c-153">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="e7f5c-154">SUBSCRIPTIONDEFINITION <ISubscriptionDefinition> : 구독 개체 속성입니다.</span><span class="sxs-lookup"><span data-stu-id="e7f5c-154">SUBSCRIPTIONDEFINITION <ISubscriptionDefinition>: Subscription object properties.</span></span>
  - <span data-ttu-id="e7f5c-155">`[DelegatedProviderSubscriptionId <String>]`: Parent DelegatedProvider 구독 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="e7f5c-155">`[DelegatedProviderSubscriptionId <String>]`: Parent DelegatedProvider subscription identifier.</span></span>
  - <span data-ttu-id="e7f5c-156">`[DisplayName <String>]`: 구독 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e7f5c-156">`[DisplayName <String>]`: Subscription name.</span></span>
  - <span data-ttu-id="e7f5c-157">`[ExternalReferenceId <String>]`: 외부 참조 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="e7f5c-157">`[ExternalReferenceId <String>]`: External reference identifier.</span></span>
  - <span data-ttu-id="e7f5c-158">`[Id <String>]`: 정규화 된 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="e7f5c-158">`[Id <String>]`: Fully qualified identifier.</span></span>
  - <span data-ttu-id="e7f5c-159">`[OfferId <String>]`: 위임 된 공급자 범위 아래에 있는 제안의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="e7f5c-159">`[OfferId <String>]`: Identifier of the offer under the scope of a delegated provider.</span></span>
  - <span data-ttu-id="e7f5c-160">`[Owner <String>]`: 구독 소유자입니다.</span><span class="sxs-lookup"><span data-stu-id="e7f5c-160">`[Owner <String>]`: Subscription owner.</span></span>
  - <span data-ttu-id="e7f5c-161">`[RoutingResourceManagerType <ResourceManagerType?>]`: 라우팅 리소스 관리자 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="e7f5c-161">`[RoutingResourceManagerType <ResourceManagerType?>]`: Routing resource manager type.</span></span>
  - <span data-ttu-id="e7f5c-162">`[State <SubscriptionState?>]`: 구독 상태입니다.</span><span class="sxs-lookup"><span data-stu-id="e7f5c-162">`[State <SubscriptionState?>]`: Subscription state.</span></span>
  - <span data-ttu-id="e7f5c-163">`[SubscriptionId <String>]`: 구독 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="e7f5c-163">`[SubscriptionId <String>]`: Subscription identifier.</span></span>
  - <span data-ttu-id="e7f5c-164">`[TenantId <String>]`: 디렉터리 테 넌 트 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="e7f5c-164">`[TenantId <String>]`: Directory tenant identifier.</span></span>

## <span data-ttu-id="e7f5c-165">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e7f5c-165">RELATED LINKS</span></span>

