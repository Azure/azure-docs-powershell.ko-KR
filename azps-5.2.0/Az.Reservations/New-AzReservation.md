---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/az.reservations/new-azreservation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/New-AzReservation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/New-AzReservation.md
ms.openlocfilehash: 60de1572afda000c8c1a99f53df1344b9b0fbfda
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98370063"
---
# <span data-ttu-id="fb6e7-101">New-AzReservation</span><span class="sxs-lookup"><span data-stu-id="fb6e7-101">New-AzReservation</span></span>

## <span data-ttu-id="fb6e7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fb6e7-102">SYNOPSIS</span></span>
<span data-ttu-id="fb6e7-103">예약 구매</span><span class="sxs-lookup"><span data-stu-id="fb6e7-103">Purchase a reservation</span></span>

## <span data-ttu-id="fb6e7-104">구문</span><span class="sxs-lookup"><span data-stu-id="fb6e7-104">SYNTAX</span></span>

```
New-AzReservation -ReservationOrderId <String> -ReservedResourceType <String> -Sku <String>
 [-Location <String>] -BillingScopeId <String> -Term <String> [-BillingPlan <String>] -Quantity <Int32>
 -DisplayName <String> -AppliedScopeType <String> [-AppliedScope <String>] [-Renew <Boolean>]
 [-InstanceFlexibility <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fb6e7-105">설명</span><span class="sxs-lookup"><span data-stu-id="fb6e7-105">DESCRIPTION</span></span>
<span data-ttu-id="fb6e7-106">예약 인스턴스 구매 및 혜택 얻기</span><span class="sxs-lookup"><span data-stu-id="fb6e7-106">Purchase a reservation Instance and get benefit</span></span>

## <span data-ttu-id="fb6e7-107">예제</span><span class="sxs-lookup"><span data-stu-id="fb6e7-107">EXAMPLES</span></span>

### <span data-ttu-id="fb6e7-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="fb6e7-108">Example 1</span></span>
```powershell
PS C:\> New-AzReservation -ReservationOrderId "112382d9-9af7-4fd5-b136-b71f0a69a1d0" -ReservedResourceType "VirtualMachines" [-Sku "standard b1"] -Location "centralus"
-BillingScopeId "/subscriptions/79c182d9-9af7-4fd5-b136-b71f0a69a1d0" -Term "P1Y" [-BillingPlan "Monthly"] -Quantity 2 [-DisplayName "demo"] -AppliedScopeType "Shared" [-AppliedScopes ""]
```

<span data-ttu-id="fb6e7-109">가격을 계산한 후 고객은 RI가 calculatePrice에서 제공하는 서비스를 제거할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fb6e7-109">After calculate price, customer could purcahse that RI provide by calculatePrice</span></span>

## <span data-ttu-id="fb6e7-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fb6e7-110">PARAMETERS</span></span>

### <span data-ttu-id="fb6e7-111">-AppliedScope</span><span class="sxs-lookup"><span data-stu-id="fb6e7-111">-AppliedScope</span></span>
<span data-ttu-id="fb6e7-112">혜택이 적용되는 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="fb6e7-112">Subscription that the benefit will be applied.</span></span> <span data-ttu-id="fb6e7-113">--applied-scope-type이 Single인 경우 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="fb6e7-113">Required if --applied-scope-type is Single.</span></span> <span data-ttu-id="fb6e7-114">--applied-scope-type이 공유인 경우를 지정하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fb6e7-114">Do not specify if --applied-scope-type is Shared.</span></span>

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

### <span data-ttu-id="fb6e7-115">-AppliedScopeType</span><span class="sxs-lookup"><span data-stu-id="fb6e7-115">-AppliedScopeType</span></span>
<span data-ttu-id="fb6e7-116">예약을 "단일" 또는 "공유"로 업데이트하는 적용된 범위의 유형</span><span class="sxs-lookup"><span data-stu-id="fb6e7-116">Type of the Applied Scope to update the reservation with "Single" or "Shared"</span></span>

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

### <span data-ttu-id="fb6e7-117">-BillingPlan</span><span class="sxs-lookup"><span data-stu-id="fb6e7-117">-BillingPlan</span></span>
<span data-ttu-id="fb6e7-118">이 SKU에 사용할 수 있는 청구 계획 옵션입니다.</span><span class="sxs-lookup"><span data-stu-id="fb6e7-118">The billing plan options available for this SKU.</span></span> <span data-ttu-id="fb6e7-119">"월별" 또는 "선행"</span><span class="sxs-lookup"><span data-stu-id="fb6e7-119">"Monthly" or "Upfront"</span></span>

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

### <span data-ttu-id="fb6e7-120">-BillingScopeId</span><span class="sxs-lookup"><span data-stu-id="fb6e7-120">-BillingScopeId</span></span>
<span data-ttu-id="fb6e7-121">예약 구매에 대해 청구될 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="fb6e7-121">Subscription that will be charged for purchasing Reservation.</span></span>

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

### <span data-ttu-id="fb6e7-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb6e7-122">-DefaultProfile</span></span>
<span data-ttu-id="fb6e7-123">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="fb6e7-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fb6e7-124">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="fb6e7-124">-DisplayName</span></span>
<span data-ttu-id="fb6e7-125">사용자가 쉽게 예약을 식별할 수 있는 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fb6e7-125">Friendly name for user to easily identified the reservation.</span></span>

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

### <span data-ttu-id="fb6e7-126">-InstanceFlexibility</span><span class="sxs-lookup"><span data-stu-id="fb6e7-126">-InstanceFlexibility</span></span>
<span data-ttu-id="fb6e7-127">{{ InstanceFlexibility Description }} 채우기</span><span class="sxs-lookup"><span data-stu-id="fb6e7-127">{{ Fill InstanceFlexibility Description }}</span></span>

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

### <span data-ttu-id="fb6e7-128">-Location</span><span class="sxs-lookup"><span data-stu-id="fb6e7-128">-Location</span></span>
<span data-ttu-id="fb6e7-129">SKU를 사용할 수 있는 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="fb6e7-129">Location that the SKU is available.</span></span>

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

### <span data-ttu-id="fb6e7-130">-Quantity</span><span class="sxs-lookup"><span data-stu-id="fb6e7-130">-Quantity</span></span>
<span data-ttu-id="fb6e7-131">가격 또는 구매를 계산하기 위한 제품의 수량입니다.</span><span class="sxs-lookup"><span data-stu-id="fb6e7-131">Quantity of product for calculating price or purchasing.</span></span>

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

### <span data-ttu-id="fb6e7-132">-Renew</span><span class="sxs-lookup"><span data-stu-id="fb6e7-132">-Renew</span></span>
<span data-ttu-id="fb6e7-133">이를 true로 설정하면 만료 날짜에 새 예약이 자동으로 구매됩니다.</span><span class="sxs-lookup"><span data-stu-id="fb6e7-133">Set this to true will automatically purchase a new reservation on the expiration date time.</span></span>

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

### <span data-ttu-id="fb6e7-134">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="fb6e7-134">-ReservationOrderId</span></span>
<span data-ttu-id="fb6e7-135">az reservations reservation-order calculate를 통해 구매, 생성할 예약 주문의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="fb6e7-135">Id of reservation order to purchase, generate by az reservations reservation-order calculate.</span></span>

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

### <span data-ttu-id="fb6e7-136">-ReservedResourceType</span><span class="sxs-lookup"><span data-stu-id="fb6e7-136">-ReservedResourceType</span></span>
<span data-ttu-id="fb6e7-137">SKU를 제공해야 하는 리소스의 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="fb6e7-137">Type of the resource for which the skus should be provided.</span></span>

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

### <span data-ttu-id="fb6e7-138">-Sku</span><span class="sxs-lookup"><span data-stu-id="fb6e7-138">-Sku</span></span>
<span data-ttu-id="fb6e7-139">SKU 이름</span><span class="sxs-lookup"><span data-stu-id="fb6e7-139">Sku name</span></span>

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

### <span data-ttu-id="fb6e7-140">-Term</span><span class="sxs-lookup"><span data-stu-id="fb6e7-140">-Term</span></span>
<span data-ttu-id="fb6e7-141">이 리소스에 사용 가능한 예약 조건입니다.</span><span class="sxs-lookup"><span data-stu-id="fb6e7-141">Available reservation terms for this resource.</span></span>


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

### <span data-ttu-id="fb6e7-142">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fb6e7-142">-Confirm</span></span>
<span data-ttu-id="fb6e7-143">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="fb6e7-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fb6e7-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fb6e7-144">-WhatIf</span></span>
<span data-ttu-id="fb6e7-145">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="fb6e7-145">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fb6e7-146">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fb6e7-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fb6e7-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb6e7-147">CommonParameters</span></span>
<span data-ttu-id="fb6e7-148">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="fb6e7-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb6e7-149">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="fb6e7-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb6e7-150">입력</span><span class="sxs-lookup"><span data-stu-id="fb6e7-150">INPUTS</span></span>

### <span data-ttu-id="fb6e7-151">없음</span><span class="sxs-lookup"><span data-stu-id="fb6e7-151">None</span></span>

## <span data-ttu-id="fb6e7-152">출력</span><span class="sxs-lookup"><span data-stu-id="fb6e7-152">OUTPUTS</span></span>

### <span data-ttu-id="fb6e7-153">Microsoft.Azure.Management.Reservations.Models.ReservationOrderResponse</span><span class="sxs-lookup"><span data-stu-id="fb6e7-153">Microsoft.Azure.Management.Reservations.Models.ReservationOrderResponse</span></span>

## <span data-ttu-id="fb6e7-154">참고 사항</span><span class="sxs-lookup"><span data-stu-id="fb6e7-154">NOTES</span></span>

## <span data-ttu-id="fb6e7-155">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fb6e7-155">RELATED LINKS</span></span>
