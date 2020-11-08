---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/az.reservations/get-azreservationquote
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationQuote.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationQuote.md
ms.openlocfilehash: 844e67f7491825fe0484a60d55cb254988cfb5c9
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94034778"
---
# <span data-ttu-id="bd50e-101">Get-AzReservationQuote</span><span class="sxs-lookup"><span data-stu-id="bd50e-101">Get-AzReservationQuote</span></span>

## <span data-ttu-id="bd50e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bd50e-102">SYNOPSIS</span></span>
<span data-ttu-id="bd50e-103">{{Synopsis 채우기}}</span><span class="sxs-lookup"><span data-stu-id="bd50e-103">{{ Fill in the Synopsis }}</span></span>

## <span data-ttu-id="bd50e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="bd50e-104">SYNTAX</span></span>

```
Get-AzReservationQuote -ReservedResourceType <String> -Sku <String> [-Location <String>]
 -BillingScopeId <String> -Term <String> [-BillingPlan <String>] -Quantity <Int32> -DisplayName <String>
 -AppliedScopeType <String> [-AppliedScope <String>] [-Renew <Boolean>] [-InstanceFlexibility <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bd50e-105">설명은</span><span class="sxs-lookup"><span data-stu-id="bd50e-105">DESCRIPTION</span></span>
<span data-ttu-id="bd50e-106">예약 주문을 배치할 가격을 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="bd50e-106">Calculate price for placing a reservation order.</span></span>

## <span data-ttu-id="bd50e-107">예제의</span><span class="sxs-lookup"><span data-stu-id="bd50e-107">EXAMPLES</span></span>

### <span data-ttu-id="bd50e-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="bd50e-108">Example 1</span></span>
```powershell
PS C:\> Get-AzReservationQuote -ReservedResourceType "VirtualMachines" [-Sku "standard b1"] -Location "centralus"
-BillingScopeId "/subscriptions/79c182d9-9af7-4fd5-b136-b71f0a69a1d0" -Term "P1Y" [-BillingPlan "Monthly"] -Quantity 2 [-DisplayName "demo"] -AppliedScopeType "Shared" [-AppliedScopes ""]
```

<span data-ttu-id="bd50e-109">카탈로그를 가져오면 고객이 위치를 기반으로 differe 제품을 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bd50e-109">After get catalog, customer can get the differe product based on location.</span></span> <span data-ttu-id="bd50e-110">이러한 정보를 사용 하 여 가격을 적절 하 게 확인 하세요.</span><span class="sxs-lookup"><span data-stu-id="bd50e-110">By using those infomation, check the price properly</span></span>

## <span data-ttu-id="bd50e-111">변수</span><span class="sxs-lookup"><span data-stu-id="bd50e-111">PARAMETERS</span></span>

### <span data-ttu-id="bd50e-112">-AppliedScope</span><span class="sxs-lookup"><span data-stu-id="bd50e-112">-AppliedScope</span></span>
<span data-ttu-id="bd50e-113">혜택을 적용할 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="bd50e-113">Subscription that the benefit will be applied.</span></span> <span data-ttu-id="bd50e-114">필수--적용 됨-범위 형식이 Single 인 경우 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="bd50e-114">Required if --applied-scope-type is Single.</span></span> <span data-ttu-id="bd50e-115">--적용 됨-범위 형식이 공유 인지 여부를 지정 하지 마세요.</span><span class="sxs-lookup"><span data-stu-id="bd50e-115">Do not specify if --applied-scope-type is Shared.</span></span>

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

### <span data-ttu-id="bd50e-116">-AppliedScopeType</span><span class="sxs-lookup"><span data-stu-id="bd50e-116">-AppliedScopeType</span></span>
<span data-ttu-id="bd50e-117">예약을 "단일" 또는 "공유"로 업데이트 하는 적용 된 범위의 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="bd50e-117">Type of the Applied Scope to update the reservation with "Single" or "Shared"</span></span>

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

### <span data-ttu-id="bd50e-118">-BillingPlan</span><span class="sxs-lookup"><span data-stu-id="bd50e-118">-BillingPlan</span></span>
<span data-ttu-id="bd50e-119">이 SKU에 대해 사용할 수 있는 청구 계획 옵션입니다.</span><span class="sxs-lookup"><span data-stu-id="bd50e-119">The billing plan options available for this SKU.</span></span> <span data-ttu-id="bd50e-120">"월 단위" 또는 "선행"</span><span class="sxs-lookup"><span data-stu-id="bd50e-120">"Monthly" or "Upfront"</span></span>

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

### <span data-ttu-id="bd50e-121">-BillingScopeId</span><span class="sxs-lookup"><span data-stu-id="bd50e-121">-BillingScopeId</span></span>
<span data-ttu-id="bd50e-122">플랜 구입을 위해 요금이 부과 되는 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="bd50e-122">Subscription that will be charged for purchasing Reservation.</span></span>

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

### <span data-ttu-id="bd50e-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd50e-123">-DefaultProfile</span></span>
<span data-ttu-id="bd50e-124">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="bd50e-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bd50e-125">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="bd50e-125">-DisplayName</span></span>
<span data-ttu-id="bd50e-126">예약을 쉽게 식별 하는 사용자에 게 친근 한 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bd50e-126">Friendly name for user to easily identified the reservation.</span></span>

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

### <span data-ttu-id="bd50e-127">-InstanceFlexibility</span><span class="sxs-lookup"><span data-stu-id="bd50e-127">-InstanceFlexibility</span></span>
<span data-ttu-id="bd50e-128">예약을 업데이트할 인스턴스 유연성의 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="bd50e-128">Type of the Instance Flexibility to update the reservation with.</span></span>

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

### <span data-ttu-id="bd50e-129">-위치</span><span class="sxs-lookup"><span data-stu-id="bd50e-129">-Location</span></span>
<span data-ttu-id="bd50e-130">SKU를 사용할 수 있는 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="bd50e-130">Location that the SKU is available.</span></span>

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

### <span data-ttu-id="bd50e-131">-수량</span><span class="sxs-lookup"><span data-stu-id="bd50e-131">-Quantity</span></span>
<span data-ttu-id="bd50e-132">가격 또는 구매를 계산 하기 위한 제품의 수량입니다.</span><span class="sxs-lookup"><span data-stu-id="bd50e-132">Quantity of product for calculating price or purchasing.</span></span>

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

### <span data-ttu-id="bd50e-133">-갱신</span><span class="sxs-lookup"><span data-stu-id="bd50e-133">-Renew</span></span>
<span data-ttu-id="bd50e-134">이를 true로 설정 하면 만료 날짜 시간에 새 예약이 자동으로 구입 합니다.</span><span class="sxs-lookup"><span data-stu-id="bd50e-134">Set this to true will automatically purchase a new reservation on the expiration date time.</span></span>

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

### <span data-ttu-id="bd50e-135">-ReservedResourceType</span><span class="sxs-lookup"><span data-stu-id="bd50e-135">-ReservedResourceType</span></span>
<span data-ttu-id="bd50e-136">Sku를 제공 해야 하는 리소스의 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="bd50e-136">Type of the resource for which the skus should be provided.</span></span>

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

### <span data-ttu-id="bd50e-137">-Sku</span><span class="sxs-lookup"><span data-stu-id="bd50e-137">-Sku</span></span>
<span data-ttu-id="bd50e-138">Sku 이름, command az 예약 카탈로그 표시를 사용 하 여 sku 목록 가져오기</span><span class="sxs-lookup"><span data-stu-id="bd50e-138">Sku name, get the sku list by using command az reservations catalog show</span></span>

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

### <span data-ttu-id="bd50e-139">기간</span><span class="sxs-lookup"><span data-stu-id="bd50e-139">-Term</span></span>
<span data-ttu-id="bd50e-140">이 리소스에 대해 사용 가능한 예약 용어입니다.</span><span class="sxs-lookup"><span data-stu-id="bd50e-140">Available reservation terms for this resource.</span></span>

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

### <span data-ttu-id="bd50e-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd50e-141">CommonParameters</span></span>
<span data-ttu-id="bd50e-142">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="bd50e-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd50e-143">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="bd50e-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd50e-144">입력</span><span class="sxs-lookup"><span data-stu-id="bd50e-144">INPUTS</span></span>

### <span data-ttu-id="bd50e-145">않아야</span><span class="sxs-lookup"><span data-stu-id="bd50e-145">None</span></span>

## <span data-ttu-id="bd50e-146">출력</span><span class="sxs-lookup"><span data-stu-id="bd50e-146">OUTPUTS</span></span>

### <span data-ttu-id="bd50e-147">CalculatePriceResponse를 통해 관리 합니다.</span><span class="sxs-lookup"><span data-stu-id="bd50e-147">Microsoft.Azure.Management.Reservations.Models.CalculatePriceResponse</span></span>

## <span data-ttu-id="bd50e-148">상속자</span><span class="sxs-lookup"><span data-stu-id="bd50e-148">NOTES</span></span>

## <span data-ttu-id="bd50e-149">관련 링크</span><span class="sxs-lookup"><span data-stu-id="bd50e-149">RELATED LINKS</span></span>
