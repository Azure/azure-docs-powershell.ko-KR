---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/az.reservations/new-azreservation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/New-AzReservation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/New-AzReservation.md
ms.openlocfilehash: 60de1572afda000c8c1a99f53df1344b9b0fbfda
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94213356"
---
# <span data-ttu-id="0c02c-101">New-AzReservation</span><span class="sxs-lookup"><span data-stu-id="0c02c-101">New-AzReservation</span></span>

## <span data-ttu-id="0c02c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0c02c-102">SYNOPSIS</span></span>
<span data-ttu-id="0c02c-103">예약 구입</span><span class="sxs-lookup"><span data-stu-id="0c02c-103">Purchase a reservation</span></span>

## <span data-ttu-id="0c02c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="0c02c-104">SYNTAX</span></span>

```
New-AzReservation -ReservationOrderId <String> -ReservedResourceType <String> -Sku <String>
 [-Location <String>] -BillingScopeId <String> -Term <String> [-BillingPlan <String>] -Quantity <Int32>
 -DisplayName <String> -AppliedScopeType <String> [-AppliedScope <String>] [-Renew <Boolean>]
 [-InstanceFlexibility <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0c02c-105">설명은</span><span class="sxs-lookup"><span data-stu-id="0c02c-105">DESCRIPTION</span></span>
<span data-ttu-id="0c02c-106">예약 인스턴스 구매 및 혜택 받기</span><span class="sxs-lookup"><span data-stu-id="0c02c-106">Purchase a reservation Instance and get benefit</span></span>

## <span data-ttu-id="0c02c-107">예제의</span><span class="sxs-lookup"><span data-stu-id="0c02c-107">EXAMPLES</span></span>

### <span data-ttu-id="0c02c-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="0c02c-108">Example 1</span></span>
```powershell
PS C:\> New-AzReservation -ReservationOrderId "112382d9-9af7-4fd5-b136-b71f0a69a1d0" -ReservedResourceType "VirtualMachines" [-Sku "standard b1"] -Location "centralus"
-BillingScopeId "/subscriptions/79c182d9-9af7-4fd5-b136-b71f0a69a1d0" -Term "P1Y" [-BillingPlan "Monthly"] -Quantity 2 [-DisplayName "demo"] -AppliedScopeType "Shared" [-AppliedScopes ""]
```

<span data-ttu-id="0c02c-109">가격이 계산 된 후, 고객은 RI가 calculatePrice 제공 하는 것을 purcahse 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0c02c-109">After calculate price, customer could purcahse that RI provide by calculatePrice</span></span>

## <span data-ttu-id="0c02c-110">변수</span><span class="sxs-lookup"><span data-stu-id="0c02c-110">PARAMETERS</span></span>

### <span data-ttu-id="0c02c-111">-AppliedScope</span><span class="sxs-lookup"><span data-stu-id="0c02c-111">-AppliedScope</span></span>
<span data-ttu-id="0c02c-112">혜택을 적용할 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0c02c-112">Subscription that the benefit will be applied.</span></span> <span data-ttu-id="0c02c-113">필수--적용 됨-범위 형식이 Single 인 경우 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="0c02c-113">Required if --applied-scope-type is Single.</span></span> <span data-ttu-id="0c02c-114">--적용 됨-범위 형식이 공유 인지 여부를 지정 하지 마세요.</span><span class="sxs-lookup"><span data-stu-id="0c02c-114">Do not specify if --applied-scope-type is Shared.</span></span>

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

### <span data-ttu-id="0c02c-115">-AppliedScopeType</span><span class="sxs-lookup"><span data-stu-id="0c02c-115">-AppliedScopeType</span></span>
<span data-ttu-id="0c02c-116">예약을 "단일" 또는 "공유"로 업데이트 하는 적용 된 범위의 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="0c02c-116">Type of the Applied Scope to update the reservation with "Single" or "Shared"</span></span>

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

### <span data-ttu-id="0c02c-117">-BillingPlan</span><span class="sxs-lookup"><span data-stu-id="0c02c-117">-BillingPlan</span></span>
<span data-ttu-id="0c02c-118">이 SKU에 대해 사용할 수 있는 청구 계획 옵션입니다.</span><span class="sxs-lookup"><span data-stu-id="0c02c-118">The billing plan options available for this SKU.</span></span> <span data-ttu-id="0c02c-119">"월 단위" 또는 "선행"</span><span class="sxs-lookup"><span data-stu-id="0c02c-119">"Monthly" or "Upfront"</span></span>

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

### <span data-ttu-id="0c02c-120">-BillingScopeId</span><span class="sxs-lookup"><span data-stu-id="0c02c-120">-BillingScopeId</span></span>
<span data-ttu-id="0c02c-121">플랜 구입을 위해 요금이 부과 되는 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0c02c-121">Subscription that will be charged for purchasing Reservation.</span></span>

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

### <span data-ttu-id="0c02c-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c02c-122">-DefaultProfile</span></span>
<span data-ttu-id="0c02c-123">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0c02c-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0c02c-124">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="0c02c-124">-DisplayName</span></span>
<span data-ttu-id="0c02c-125">예약을 쉽게 식별 하는 사용자에 게 친근 한 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0c02c-125">Friendly name for user to easily identified the reservation.</span></span>

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

### <span data-ttu-id="0c02c-126">-InstanceFlexibility</span><span class="sxs-lookup"><span data-stu-id="0c02c-126">-InstanceFlexibility</span></span>
<span data-ttu-id="0c02c-127">{{InstanceFlexibility 설명 채우기}}</span><span class="sxs-lookup"><span data-stu-id="0c02c-127">{{ Fill InstanceFlexibility Description }}</span></span>

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

### <span data-ttu-id="0c02c-128">-위치</span><span class="sxs-lookup"><span data-stu-id="0c02c-128">-Location</span></span>
<span data-ttu-id="0c02c-129">SKU를 사용할 수 있는 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="0c02c-129">Location that the SKU is available.</span></span>

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

### <span data-ttu-id="0c02c-130">-수량</span><span class="sxs-lookup"><span data-stu-id="0c02c-130">-Quantity</span></span>
<span data-ttu-id="0c02c-131">가격 또는 구매를 계산 하기 위한 제품의 수량입니다.</span><span class="sxs-lookup"><span data-stu-id="0c02c-131">Quantity of product for calculating price or purchasing.</span></span>

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

### <span data-ttu-id="0c02c-132">-갱신</span><span class="sxs-lookup"><span data-stu-id="0c02c-132">-Renew</span></span>
<span data-ttu-id="0c02c-133">이를 true로 설정 하면 만료 날짜 시간에 새 예약이 자동으로 구입 합니다.</span><span class="sxs-lookup"><span data-stu-id="0c02c-133">Set this to true will automatically purchase a new reservation on the expiration date time.</span></span>

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

### <span data-ttu-id="0c02c-134">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="0c02c-134">-ReservationOrderId</span></span>
<span data-ttu-id="0c02c-135">구매할 예약 순서에 대 한 Id, az 예약 예약 주문 계산에서 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0c02c-135">Id of reservation order to purchase, generate by az reservations reservation-order calculate.</span></span>

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

### <span data-ttu-id="0c02c-136">-ReservedResourceType</span><span class="sxs-lookup"><span data-stu-id="0c02c-136">-ReservedResourceType</span></span>
<span data-ttu-id="0c02c-137">Sku를 제공 해야 하는 리소스의 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="0c02c-137">Type of the resource for which the skus should be provided.</span></span>

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

### <span data-ttu-id="0c02c-138">-Sku</span><span class="sxs-lookup"><span data-stu-id="0c02c-138">-Sku</span></span>
<span data-ttu-id="0c02c-139">Sku 이름</span><span class="sxs-lookup"><span data-stu-id="0c02c-139">Sku name</span></span>

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

### <span data-ttu-id="0c02c-140">기간</span><span class="sxs-lookup"><span data-stu-id="0c02c-140">-Term</span></span>
<span data-ttu-id="0c02c-141">이 리소스에 대해 사용 가능한 예약 용어입니다.</span><span class="sxs-lookup"><span data-stu-id="0c02c-141">Available reservation terms for this resource.</span></span>


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

### <span data-ttu-id="0c02c-142">-확인</span><span class="sxs-lookup"><span data-stu-id="0c02c-142">-Confirm</span></span>
<span data-ttu-id="0c02c-143">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="0c02c-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0c02c-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0c02c-144">-WhatIf</span></span>
<span data-ttu-id="0c02c-145">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="0c02c-145">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0c02c-146">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0c02c-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0c02c-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c02c-147">CommonParameters</span></span>
<span data-ttu-id="0c02c-148">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0c02c-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c02c-149">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="0c02c-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c02c-150">입력</span><span class="sxs-lookup"><span data-stu-id="0c02c-150">INPUTS</span></span>

### <span data-ttu-id="0c02c-151">않아야</span><span class="sxs-lookup"><span data-stu-id="0c02c-151">None</span></span>

## <span data-ttu-id="0c02c-152">출력</span><span class="sxs-lookup"><span data-stu-id="0c02c-152">OUTPUTS</span></span>

### <span data-ttu-id="0c02c-153">ReservationOrderResponse를 통해 관리 합니다.</span><span class="sxs-lookup"><span data-stu-id="0c02c-153">Microsoft.Azure.Management.Reservations.Models.ReservationOrderResponse</span></span>

## <span data-ttu-id="0c02c-154">상속자</span><span class="sxs-lookup"><span data-stu-id="0c02c-154">NOTES</span></span>

## <span data-ttu-id="0c02c-155">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0c02c-155">RELATED LINKS</span></span>
