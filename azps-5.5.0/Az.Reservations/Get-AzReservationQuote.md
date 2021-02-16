---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/az.reservations/get-azreservationquote
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationQuote.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationQuote.md
ms.openlocfilehash: 073a059063198e91a1bbcc67814c01c1b786e7c9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100176449"
---
# <span data-ttu-id="f543e-101">Get-AzReservationQuote</span><span class="sxs-lookup"><span data-stu-id="f543e-101">Get-AzReservationQuote</span></span>

## <span data-ttu-id="f543e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f543e-102">SYNOPSIS</span></span>
<span data-ttu-id="f543e-103">예약에 대한 견적을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="f543e-103">Get a quote for the reservation.</span></span> <span data-ttu-id="f543e-104">구매에 `New-AzReservation` 전달됩니다.</span><span class="sxs-lookup"><span data-stu-id="f543e-104">This is passed to `New-AzReservation` to purchase.</span></span>

## <span data-ttu-id="f543e-105">구문</span><span class="sxs-lookup"><span data-stu-id="f543e-105">SYNTAX</span></span>

```
Get-AzReservationQuote -ReservedResourceType <String> -Sku <String> [-Location <String>]
 -BillingScopeId <String> -Term <String> [-BillingPlan <String>] -Quantity <Int32> -DisplayName <String>
 -AppliedScopeType <String> [-AppliedScope <String>] [-Renew <Boolean>] [-InstanceFlexibility <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f543e-106">설명</span><span class="sxs-lookup"><span data-stu-id="f543e-106">DESCRIPTION</span></span>
<span data-ttu-id="f543e-107">예약 주문에 대한 가격을 계산합니다.</span><span class="sxs-lookup"><span data-stu-id="f543e-107">Calculate price for placing a reservation order.</span></span>

## <span data-ttu-id="f543e-108">예제</span><span class="sxs-lookup"><span data-stu-id="f543e-108">EXAMPLES</span></span>

### <span data-ttu-id="f543e-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="f543e-109">Example 1</span></span>
```powershell
PS C:\> Get-AzReservationQuote -ReservedResourceType "VirtualMachines" [-Sku "standard b1"] -Location "centralus"
-BillingScopeId "/subscriptions/79c182d9-9af7-4fd5-b136-b71f0a69a1d0" -Term "P1Y" [-BillingPlan "Monthly"] -Quantity 2 [-DisplayName "demo"] -AppliedScopeType "Shared" [-AppliedScopes ""]
```

<span data-ttu-id="f543e-110">카탈로그를 다운로드한 후 고객은 위치에 따라 다른 제품을 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f543e-110">After get catalog, customer can get the differe product based on location.</span></span> <span data-ttu-id="f543e-111">이러한 정보를 사용하여 가격을 올바르게 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="f543e-111">By using those infomation, check the price properly</span></span>

## <span data-ttu-id="f543e-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f543e-112">PARAMETERS</span></span>

### <span data-ttu-id="f543e-113">-AppliedScope</span><span class="sxs-lookup"><span data-stu-id="f543e-113">-AppliedScope</span></span>
<span data-ttu-id="f543e-114">혜택이 적용되는 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f543e-114">Subscription that the benefit will be applied.</span></span> <span data-ttu-id="f543e-115">--applied-scope-type이 Single인 경우 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="f543e-115">Required if --applied-scope-type is Single.</span></span> <span data-ttu-id="f543e-116">--applied-scope-type이 공유인 경우를 지정하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f543e-116">Do not specify if --applied-scope-type is Shared.</span></span>

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

### <span data-ttu-id="f543e-117">-AppliedScopeType</span><span class="sxs-lookup"><span data-stu-id="f543e-117">-AppliedScopeType</span></span>
<span data-ttu-id="f543e-118">예약을 "단일" 또는 "공유"로 업데이트하는 적용된 범위의 유형</span><span class="sxs-lookup"><span data-stu-id="f543e-118">Type of the Applied Scope to update the reservation with "Single" or "Shared"</span></span>

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

### <span data-ttu-id="f543e-119">-BillingPlan</span><span class="sxs-lookup"><span data-stu-id="f543e-119">-BillingPlan</span></span>
<span data-ttu-id="f543e-120">이 SKU에 사용할 수 있는 청구 계획 옵션입니다.</span><span class="sxs-lookup"><span data-stu-id="f543e-120">The billing plan options available for this SKU.</span></span> <span data-ttu-id="f543e-121">"월별" 또는 "선행"</span><span class="sxs-lookup"><span data-stu-id="f543e-121">"Monthly" or "Upfront"</span></span>

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

### <span data-ttu-id="f543e-122">-BillingScopeId</span><span class="sxs-lookup"><span data-stu-id="f543e-122">-BillingScopeId</span></span>
<span data-ttu-id="f543e-123">예약 구매에 대해 청구될 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f543e-123">Subscription that will be charged for purchasing Reservation.</span></span>

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

### <span data-ttu-id="f543e-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f543e-124">-DefaultProfile</span></span>
<span data-ttu-id="f543e-125">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f543e-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f543e-126">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="f543e-126">-DisplayName</span></span>
<span data-ttu-id="f543e-127">예약을 쉽게 식별할 수 있는 사용자에게 친숙한 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f543e-127">Friendly name for user to easily identified the reservation.</span></span>

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

### <span data-ttu-id="f543e-128">-InstanceFlexibility</span><span class="sxs-lookup"><span data-stu-id="f543e-128">-InstanceFlexibility</span></span>
<span data-ttu-id="f543e-129">예약을 업데이트할 인스턴스 유연성의 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="f543e-129">Type of the Instance Flexibility to update the reservation with.</span></span>

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

### <span data-ttu-id="f543e-130">-Location</span><span class="sxs-lookup"><span data-stu-id="f543e-130">-Location</span></span>
<span data-ttu-id="f543e-131">SKU를 사용할 수 있는 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="f543e-131">Location that the SKU is available.</span></span>

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

### <span data-ttu-id="f543e-132">-Quantity</span><span class="sxs-lookup"><span data-stu-id="f543e-132">-Quantity</span></span>
<span data-ttu-id="f543e-133">가격 또는 구매를 계산하기 위한 제품의 수량입니다.</span><span class="sxs-lookup"><span data-stu-id="f543e-133">Quantity of product for calculating price or purchasing.</span></span>

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

### <span data-ttu-id="f543e-134">-Renew</span><span class="sxs-lookup"><span data-stu-id="f543e-134">-Renew</span></span>
<span data-ttu-id="f543e-135">이를 true로 설정하면 만료 날짜에 새 예약이 자동으로 구매됩니다.</span><span class="sxs-lookup"><span data-stu-id="f543e-135">Set this to true will automatically purchase a new reservation on the expiration date time.</span></span>

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

### <span data-ttu-id="f543e-136">-ReservedResourceType</span><span class="sxs-lookup"><span data-stu-id="f543e-136">-ReservedResourceType</span></span>
<span data-ttu-id="f543e-137">SKU를 제공해야 하는 리소스의 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="f543e-137">Type of the resource for which the skus should be provided.</span></span>

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

### <span data-ttu-id="f543e-138">-Sku</span><span class="sxs-lookup"><span data-stu-id="f543e-138">-Sku</span></span>
<span data-ttu-id="f543e-139">Sku 이름, 명령 az reservations catalog show를 사용하여 SKU 목록을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="f543e-139">Sku name, get the sku list by using command az reservations catalog show</span></span>

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

### <span data-ttu-id="f543e-140">-Term</span><span class="sxs-lookup"><span data-stu-id="f543e-140">-Term</span></span>
<span data-ttu-id="f543e-141">이 리소스에 사용 가능한 예약 조건입니다.</span><span class="sxs-lookup"><span data-stu-id="f543e-141">Available reservation terms for this resource.</span></span>

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

### <span data-ttu-id="f543e-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f543e-142">CommonParameters</span></span>
<span data-ttu-id="f543e-143">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="f543e-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f543e-144">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="f543e-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f543e-145">입력</span><span class="sxs-lookup"><span data-stu-id="f543e-145">INPUTS</span></span>

### <span data-ttu-id="f543e-146">없음</span><span class="sxs-lookup"><span data-stu-id="f543e-146">None</span></span>

## <span data-ttu-id="f543e-147">출력</span><span class="sxs-lookup"><span data-stu-id="f543e-147">OUTPUTS</span></span>

### <span data-ttu-id="f543e-148">Microsoft.Azure.Management.Reservations.Models.CalculatePriceResponse</span><span class="sxs-lookup"><span data-stu-id="f543e-148">Microsoft.Azure.Management.Reservations.Models.CalculatePriceResponse</span></span>

## <span data-ttu-id="f543e-149">참고 사항</span><span class="sxs-lookup"><span data-stu-id="f543e-149">NOTES</span></span>

## <span data-ttu-id="f543e-150">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f543e-150">RELATED LINKS</span></span>
