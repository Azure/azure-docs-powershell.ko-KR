---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/set-azsoffer
schema: 2.0.0
ms.openlocfilehash: 82be26ae402278d8cdc24195fd62ed09b67bdc14
ms.sourcegitcommit: 308ebca475d1c37624d7a10a2c02047594f44cdf
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/22/2020
ms.locfileid: "94045108"
---
# <span data-ttu-id="91afd-101">Set-AzsOffer</span><span class="sxs-lookup"><span data-stu-id="91afd-101">Set-AzsOffer</span></span>

## <span data-ttu-id="91afd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="91afd-102">SYNOPSIS</span></span>
<span data-ttu-id="91afd-103">제안을 만들거나 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="91afd-103">Create or update the offer.</span></span>

## <span data-ttu-id="91afd-104">구문과</span><span class="sxs-lookup"><span data-stu-id="91afd-104">SYNTAX</span></span>

### <span data-ttu-id="91afd-105">UpdateExpanded 됨 (기본값)</span><span class="sxs-lookup"><span data-stu-id="91afd-105">UpdateExpanded (Default)</span></span>
```
Set-AzsOffer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-AddonPlanDefinition <IAddonPlanDefinition[]>] [-BasePlanIds <String[]>] [-Description <String>]
 [-DisplayName <String>] [-ExternalReferenceId <String>] [-Location <String>]
 [-MaxSubscriptionsPerAccount <Int32>] [-PropertiesName <String>] [-State <AccessibilityState>]
 [-SubscriptionCount <Int32>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="91afd-106">Update</span><span class="sxs-lookup"><span data-stu-id="91afd-106">Update</span></span>
```
Set-AzsOffer -OfferDefinition <IOffer> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="91afd-107">설명은</span><span class="sxs-lookup"><span data-stu-id="91afd-107">DESCRIPTION</span></span>
<span data-ttu-id="91afd-108">제안을 만들거나 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="91afd-108">Create or update the offer.</span></span>

## <span data-ttu-id="91afd-109">예제의</span><span class="sxs-lookup"><span data-stu-id="91afd-109">EXAMPLES</span></span>

### <span data-ttu-id="91afd-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="91afd-110">Example 1</span></span>
```powershell
PS C:\> $Offer = Get-AzsAdminManagedOffer | Select-Object -First 1
$Offer.MaxSubscriptionsPerAccount = 18
$Offer | Set-AzsOffer

AddonPlans                 : {}
BasePlanIds                : {/subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/resourceGroups/DRPTestResourceGroup5056/providers/Microsoft.Subscriptions.Admin/plans/DRPTestPlan5056}
Description                : 
DisplayName                : DRPTestOffer5056
ExternalReferenceId        : 
Id                         : /subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/resourceGroups/DRPTestResourceGroup5056/providers/Microsoft.Subscriptions.Admin/offers/DRPTestOffer5056
Location                   : redmond
MaxSubscriptionsPerAccount : 18
Name                       : DRPTestOffer5056
PropertiesName             : DRPTestOffer5056
State                      : Private
SubscriptionCount          : 5
Tags                       : Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.ResourceTags
Type                       : Microsoft.Subscriptions.Admin/offers
```

<span data-ttu-id="91afd-111">제안을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="91afd-111">Update an offer.</span></span>

## <span data-ttu-id="91afd-112">변수</span><span class="sxs-lookup"><span data-stu-id="91afd-112">PARAMETERS</span></span>

### <span data-ttu-id="91afd-113">-AddonPlanDefinition</span><span class="sxs-lookup"><span data-stu-id="91afd-113">-AddonPlanDefinition</span></span>
<span data-ttu-id="91afd-114">테 넌 트가 제공의 일부로 선택적으로 얻을 수 있는 추가 기능 계획에 대 한 참조입니다.</span><span class="sxs-lookup"><span data-stu-id="91afd-114">References to add-on plans that a tenant can optionally acquire as a part of the offer.</span></span>
<span data-ttu-id="91afd-115">생성 하려면 ADDONPLANDEFINITION 속성에 대 한 메모 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="91afd-115">To construct, see NOTES section for ADDONPLANDEFINITION properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IAddonPlanDefinition[]
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="91afd-116">-Base계획 Id</span><span class="sxs-lookup"><span data-stu-id="91afd-116">-BasePlanIds</span></span>
<span data-ttu-id="91afd-117">테 넌 트가 제안에 구독 하는 즉시 테 넌 트에 사용할 수 있는 기본 계획의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="91afd-117">Identifiers of the base plans that become available to the tenant immediately when a tenant subscribes to the offer.</span></span>

```yaml
Type: System.String[]
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="91afd-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91afd-118">-DefaultProfile</span></span>
<span data-ttu-id="91afd-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="91afd-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="91afd-120">-설명</span><span class="sxs-lookup"><span data-stu-id="91afd-120">-Description</span></span>
<span data-ttu-id="91afd-121">제안에 대 한 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="91afd-121">Description of offer.</span></span>

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

### <span data-ttu-id="91afd-122">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="91afd-122">-DisplayName</span></span>
<span data-ttu-id="91afd-123">제공의 표시 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="91afd-123">Display name of offer.</span></span>

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

### <span data-ttu-id="91afd-124">-ExternalReferenceId</span><span class="sxs-lookup"><span data-stu-id="91afd-124">-ExternalReferenceId</span></span>
<span data-ttu-id="91afd-125">외부 참조 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="91afd-125">External reference identifier.</span></span>

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

### <span data-ttu-id="91afd-126">-위치</span><span class="sxs-lookup"><span data-stu-id="91afd-126">-Location</span></span>
<span data-ttu-id="91afd-127">리소스 위치</span><span class="sxs-lookup"><span data-stu-id="91afd-127">Location of the resource</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="91afd-128">-MaxSubscriptionsPerAccount</span><span class="sxs-lookup"><span data-stu-id="91afd-128">-MaxSubscriptionsPerAccount</span></span>
<span data-ttu-id="91afd-129">계정 당 최대 구독 수.</span><span class="sxs-lookup"><span data-stu-id="91afd-129">Maximum subscriptions per account.</span></span>

```yaml
Type: System.Int32
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="91afd-130">-이름</span><span class="sxs-lookup"><span data-stu-id="91afd-130">-Name</span></span>
<span data-ttu-id="91afd-131">제안의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="91afd-131">Name of an offer.</span></span>

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

### <span data-ttu-id="91afd-132">-OfferDefinition</span><span class="sxs-lookup"><span data-stu-id="91afd-132">-OfferDefinition</span></span>
<span data-ttu-id="91afd-133">구독을 만들 수 있는 서비스를 제공 하는 것을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="91afd-133">Represents an offering of services against which a subscription can be created.</span></span>
<span data-ttu-id="91afd-134">생성 하려면 OFFERDEFINITION 속성에 대 한 메모 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="91afd-134">To construct, see NOTES section for OFFERDEFINITION properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IOffer
Parameter Sets: Update
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="91afd-135">-속성 이름</span><span class="sxs-lookup"><span data-stu-id="91afd-135">-PropertiesName</span></span>
<span data-ttu-id="91afd-136">제안의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="91afd-136">Name of the Offer.</span></span>

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

### <span data-ttu-id="91afd-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="91afd-137">-ResourceGroupName</span></span>
<span data-ttu-id="91afd-138">리소스가 있는 리소스 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="91afd-138">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="91afd-139">-상태</span><span class="sxs-lookup"><span data-stu-id="91afd-139">-State</span></span>
<span data-ttu-id="91afd-140">접근성 상태를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="91afd-140">Offer accessibility state.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Support.AccessibilityState
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="91afd-141">-구독 카운트</span><span class="sxs-lookup"><span data-stu-id="91afd-141">-SubscriptionCount</span></span>
<span data-ttu-id="91afd-142">현재 구독 수입니다.</span><span class="sxs-lookup"><span data-stu-id="91afd-142">Current subscription count.</span></span>

```yaml
Type: System.Int32
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="91afd-143">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="91afd-143">-SubscriptionId</span></span>
<span data-ttu-id="91afd-144">Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명입니다. 구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="91afd-144">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="91afd-145">-확인</span><span class="sxs-lookup"><span data-stu-id="91afd-145">-Confirm</span></span>
<span data-ttu-id="91afd-146">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="91afd-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="91afd-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="91afd-147">-WhatIf</span></span>
<span data-ttu-id="91afd-148">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="91afd-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="91afd-149">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="91afd-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="91afd-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91afd-150">CommonParameters</span></span>
<span data-ttu-id="91afd-151">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="91afd-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91afd-152">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="91afd-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91afd-153">입력</span><span class="sxs-lookup"><span data-stu-id="91afd-153">INPUTS</span></span>

### <span data-ttu-id="91afd-154">SubscriptionsAdmin. Api20151101. i a i.</span><span class="sxs-lookup"><span data-stu-id="91afd-154">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IOffer</span></span>

## <span data-ttu-id="91afd-155">출력</span><span class="sxs-lookup"><span data-stu-id="91afd-155">OUTPUTS</span></span>

### <span data-ttu-id="91afd-156">SubscriptionsAdmin. Api20151101. i a i.</span><span class="sxs-lookup"><span data-stu-id="91afd-156">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IOffer</span></span>

<span data-ttu-id="91afd-157">별칭과</span><span class="sxs-lookup"><span data-stu-id="91afd-157">ALIASES</span></span>

## <span data-ttu-id="91afd-158">상속자</span><span class="sxs-lookup"><span data-stu-id="91afd-158">NOTES</span></span>

<span data-ttu-id="91afd-159">복잡 한 매개 변수 속성 아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="91afd-159">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="91afd-160">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="91afd-160">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="91afd-161">ADDONPLANDEFINITION <IAddonPlanDefinition [] >: 테 넌 트가 제공의 일부로 선택적으로 얻을 수 있는 추가 기능 계획에 대 한 참조입니다.</span><span class="sxs-lookup"><span data-stu-id="91afd-161">ADDONPLANDEFINITION <IAddonPlanDefinition[]>: References to add-on plans that a tenant can optionally acquire as a part of the offer.</span></span>
  - <span data-ttu-id="91afd-162">`[MaxAcquisitionCount <Int32?>]`: 단일 구독에서 얻을 수 있는 최대 인스턴스 수입니다.</span><span class="sxs-lookup"><span data-stu-id="91afd-162">`[MaxAcquisitionCount <Int32?>]`: Maximum number of instances that can be acquired by a single subscription.</span></span> <span data-ttu-id="91afd-163">지정 하지 않으면 가정 값은 1입니다.</span><span class="sxs-lookup"><span data-stu-id="91afd-163">If not specified, the assumed value is 1.</span></span>
  - <span data-ttu-id="91afd-164">`[PlanId <String>]`: 계획 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="91afd-164">`[PlanId <String>]`: Plan identifier.</span></span>

<span data-ttu-id="91afd-165">OFFERDEFINITION <IOffer> : 구독을 만들 수 있는 서비스의 제공을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="91afd-165">OFFERDEFINITION <IOffer>: Represents an offering of services against which a subscription can be created.</span></span>
  - <span data-ttu-id="91afd-166">`[Location <String>]`: 리소스 위치</span><span class="sxs-lookup"><span data-stu-id="91afd-166">`[Location <String>]`: Location of the resource</span></span>
  - <span data-ttu-id="91afd-167">`[AddonPlans <IAddonPlanDefinition[]>]`: 테 넌 트가 제공의 일부로 선택적으로 얻을 수 있는 추가 기능 계획에 대 한 참조입니다.</span><span class="sxs-lookup"><span data-stu-id="91afd-167">`[AddonPlans <IAddonPlanDefinition[]>]`: References to add-on plans that a tenant can optionally acquire as a part of the offer.</span></span>
    - <span data-ttu-id="91afd-168">`[MaxAcquisitionCount <Int32?>]`: 단일 구독에서 얻을 수 있는 최대 인스턴스 수입니다.</span><span class="sxs-lookup"><span data-stu-id="91afd-168">`[MaxAcquisitionCount <Int32?>]`: Maximum number of instances that can be acquired by a single subscription.</span></span> <span data-ttu-id="91afd-169">지정 하지 않으면 가정 값은 1입니다.</span><span class="sxs-lookup"><span data-stu-id="91afd-169">If not specified, the assumed value is 1.</span></span>
    - <span data-ttu-id="91afd-170">`[PlanId <String>]`: 계획 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="91afd-170">`[PlanId <String>]`: Plan identifier.</span></span>
  - <span data-ttu-id="91afd-171">`[BasePlanIds <String[]>]`: 테 넌 트가 제안에 구독 하는 즉시 테 넌 트에 사용할 수 있는 기본 계획의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="91afd-171">`[BasePlanIds <String[]>]`: Identifiers of the base plans that become available to the tenant immediately when a tenant subscribes to the offer.</span></span>
  - <span data-ttu-id="91afd-172">`[Description <String>]`: 제안에 대 한 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="91afd-172">`[Description <String>]`: Description of offer.</span></span>
  - <span data-ttu-id="91afd-173">`[DisplayName <String>]`: 제공의 표시 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="91afd-173">`[DisplayName <String>]`: Display name of offer.</span></span>
  - <span data-ttu-id="91afd-174">`[ExternalReferenceId <String>]`: 외부 참조 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="91afd-174">`[ExternalReferenceId <String>]`: External reference identifier.</span></span>
  - <span data-ttu-id="91afd-175">`[MaxSubscriptionsPerAccount <Int32?>]`: 계정 당 최대 구독 수.</span><span class="sxs-lookup"><span data-stu-id="91afd-175">`[MaxSubscriptionsPerAccount <Int32?>]`: Maximum subscriptions per account.</span></span>
  - <span data-ttu-id="91afd-176">`[PropertiesName <String>]`: 제안의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="91afd-176">`[PropertiesName <String>]`: Name of the Offer.</span></span>
  - <span data-ttu-id="91afd-177">`[State <AccessibilityState?>]`: 접근성 상태를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="91afd-177">`[State <AccessibilityState?>]`: Offer accessibility state.</span></span>
  - <span data-ttu-id="91afd-178">`[SubscriptionCount <Int32?>]`: 현재 구독 수.</span><span class="sxs-lookup"><span data-stu-id="91afd-178">`[SubscriptionCount <Int32?>]`: Current subscription count.</span></span>

## <span data-ttu-id="91afd-179">관련 링크</span><span class="sxs-lookup"><span data-stu-id="91afd-179">RELATED LINKS</span></span>
