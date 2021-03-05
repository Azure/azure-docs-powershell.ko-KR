---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/powershell/module/az.reservations/new-azreservation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/New-AzReservation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/New-AzReservation.md
ms.openlocfilehash: 37be462c2af2c33987e6acd0118c3169b1e062d2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102000203"
---
# <span data-ttu-id="03646-101">New-AzReservation</span><span class="sxs-lookup"><span data-stu-id="03646-101">New-AzReservation</span></span>

## <span data-ttu-id="03646-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="03646-102">SYNOPSIS</span></span>
<span data-ttu-id="03646-103">예약 구매</span><span class="sxs-lookup"><span data-stu-id="03646-103">Purchase a reservation</span></span>

## <span data-ttu-id="03646-104">구문</span><span class="sxs-lookup"><span data-stu-id="03646-104">SYNTAX</span></span>

```
New-AzReservation -ReservationOrderId <String> -ReservedResourceType <String> -Sku <String>
 [-Location <String>] -BillingScopeId <String> -Term <String> [-BillingPlan <String>] -Quantity <Int32>
 -DisplayName <String> -AppliedScopeType <String> [-AppliedScope <String>] [-Renew <Boolean>]
 [-InstanceFlexibility <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="03646-105">설명</span><span class="sxs-lookup"><span data-stu-id="03646-105">DESCRIPTION</span></span>
<span data-ttu-id="03646-106">예약 인스턴스 구매 및 혜택 얻기</span><span class="sxs-lookup"><span data-stu-id="03646-106">Purchase a reservation Instance and get benefit</span></span>

## <span data-ttu-id="03646-107">예제</span><span class="sxs-lookup"><span data-stu-id="03646-107">EXAMPLES</span></span>

### <span data-ttu-id="03646-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="03646-108">Example 1</span></span>
```powershell
PS C:\> New-AzReservation -ReservationOrderId "112382d9-9af7-4fd5-b136-b71f0a69a1d0" -ReservedResourceType "VirtualMachines" [-Sku "standard b1"] -Location "centralus"
-BillingScopeId "/subscriptions/79c182d9-9af7-4fd5-b136-b71f0a69a1d0" -Term "P1Y" [-BillingPlan "Monthly"] -Quantity 2 [-DisplayName "demo"] -AppliedScopeType "Shared" [-AppliedScopes ""]
```

<span data-ttu-id="03646-109">가격을 계산한 후 고객이 RI에서 제공하는 purcahse를 계산하여 제공할 수 있습니다Price</span><span class="sxs-lookup"><span data-stu-id="03646-109">After calculate price, customer could purcahse that RI provide by calculatePrice</span></span>

## <span data-ttu-id="03646-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="03646-110">PARAMETERS</span></span>

### <span data-ttu-id="03646-111">-AppliedScope</span><span class="sxs-lookup"><span data-stu-id="03646-111">-AppliedScope</span></span>
<span data-ttu-id="03646-112">혜택이 적용되는 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="03646-112">Subscription that the benefit will be applied.</span></span> <span data-ttu-id="03646-113">--applied-scope-type이 Single인 경우 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="03646-113">Required if --applied-scope-type is Single.</span></span> <span data-ttu-id="03646-114">--applied-scope-type이 공유되는지 지정하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="03646-114">Do not specify if --applied-scope-type is Shared.</span></span>

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

### <span data-ttu-id="03646-115">-appliedScopeType</span><span class="sxs-lookup"><span data-stu-id="03646-115">-AppliedScopeType</span></span>
<span data-ttu-id="03646-116">예약을 "Single" 또는 "공유"로 업데이트하는 적용 범위 유형</span><span class="sxs-lookup"><span data-stu-id="03646-116">Type of the Applied Scope to update the reservation with "Single" or "Shared"</span></span>

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

### <span data-ttu-id="03646-117">-BillingPlan</span><span class="sxs-lookup"><span data-stu-id="03646-117">-BillingPlan</span></span>
<span data-ttu-id="03646-118">이 SKU에 사용할 수 있는 청구 계획 옵션입니다.</span><span class="sxs-lookup"><span data-stu-id="03646-118">The billing plan options available for this SKU.</span></span> <span data-ttu-id="03646-119">"월간" 또는 "선결제"</span><span class="sxs-lookup"><span data-stu-id="03646-119">"Monthly" or "Upfront"</span></span>

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

### <span data-ttu-id="03646-120">-BillingScopeId</span><span class="sxs-lookup"><span data-stu-id="03646-120">-BillingScopeId</span></span>
<span data-ttu-id="03646-121">예약 구매에 대한 요금이 청구될 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="03646-121">Subscription that will be charged for purchasing Reservation.</span></span>

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

### <span data-ttu-id="03646-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03646-122">-DefaultProfile</span></span>
<span data-ttu-id="03646-123">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="03646-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03646-124">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="03646-124">-DisplayName</span></span>
<span data-ttu-id="03646-125">사용자가 쉽게 예약을 식별할 수 있는 친숙한 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="03646-125">Friendly name for user to easily identified the reservation.</span></span>

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

### <span data-ttu-id="03646-126">-InstanceFlexibility</span><span class="sxs-lookup"><span data-stu-id="03646-126">-InstanceFlexibility</span></span>
<span data-ttu-id="03646-127">{{ InstanceFlexibility 설명 }} 채우기</span><span class="sxs-lookup"><span data-stu-id="03646-127">{{ Fill InstanceFlexibility Description }}</span></span>

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

### <span data-ttu-id="03646-128">-Location</span><span class="sxs-lookup"><span data-stu-id="03646-128">-Location</span></span>
<span data-ttu-id="03646-129">SKU를 사용할 수 있는 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="03646-129">Location that the SKU is available.</span></span>

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

### <span data-ttu-id="03646-130">-수량</span><span class="sxs-lookup"><span data-stu-id="03646-130">-Quantity</span></span>
<span data-ttu-id="03646-131">가격 또는 구매를 계산하기 위한 제품의 수량입니다.</span><span class="sxs-lookup"><span data-stu-id="03646-131">Quantity of product for calculating price or purchasing.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03646-132">-갱신</span><span class="sxs-lookup"><span data-stu-id="03646-132">-Renew</span></span>
<span data-ttu-id="03646-133">이를 true로 설정하면 만료 날짜에 자동으로 새 예약을 구매합니다.</span><span class="sxs-lookup"><span data-stu-id="03646-133">Set this to true will automatically purchase a new reservation on the expiration date time.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03646-134">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="03646-134">-ReservationOrderId</span></span>
<span data-ttu-id="03646-135">구매할 예약 주문의 ID, az reservations reservation-order 계산을 통해 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="03646-135">Id of reservation order to purchase, generate by az reservations reservation-order calculate.</span></span>

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

### <span data-ttu-id="03646-136">-ReservedResourceType</span><span class="sxs-lookup"><span data-stu-id="03646-136">-ReservedResourceType</span></span>
<span data-ttu-id="03646-137">스쿠를 제공해야 하는 리소스의 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="03646-137">Type of the resource for which the skus should be provided.</span></span>

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

### <span data-ttu-id="03646-138">-Sku</span><span class="sxs-lookup"><span data-stu-id="03646-138">-Sku</span></span>
<span data-ttu-id="03646-139">Sku 이름</span><span class="sxs-lookup"><span data-stu-id="03646-139">Sku name</span></span>

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

### <span data-ttu-id="03646-140">-Term</span><span class="sxs-lookup"><span data-stu-id="03646-140">-Term</span></span>
<span data-ttu-id="03646-141">이 리소스에 사용할 수 있는 예약 조건입니다.</span><span class="sxs-lookup"><span data-stu-id="03646-141">Available reservation terms for this resource.</span></span>


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

### <span data-ttu-id="03646-142">-확인</span><span class="sxs-lookup"><span data-stu-id="03646-142">-Confirm</span></span>
<span data-ttu-id="03646-143">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="03646-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="03646-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="03646-144">-WhatIf</span></span>
<span data-ttu-id="03646-145">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="03646-145">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="03646-146">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="03646-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="03646-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03646-147">CommonParameters</span></span>
<span data-ttu-id="03646-148">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="03646-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03646-149">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="03646-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03646-150">입력</span><span class="sxs-lookup"><span data-stu-id="03646-150">INPUTS</span></span>

### <span data-ttu-id="03646-151">없음</span><span class="sxs-lookup"><span data-stu-id="03646-151">None</span></span>

## <span data-ttu-id="03646-152">출력</span><span class="sxs-lookup"><span data-stu-id="03646-152">OUTPUTS</span></span>

### <span data-ttu-id="03646-153">Microsoft.Azure.Management.Reservations.Models.ReservationOrderResponse</span><span class="sxs-lookup"><span data-stu-id="03646-153">Microsoft.Azure.Management.Reservations.Models.ReservationOrderResponse</span></span>

## <span data-ttu-id="03646-154">참고 사항</span><span class="sxs-lookup"><span data-stu-id="03646-154">NOTES</span></span>

## <span data-ttu-id="03646-155">관련 링크</span><span class="sxs-lookup"><span data-stu-id="03646-155">RELATED LINKS</span></span>
