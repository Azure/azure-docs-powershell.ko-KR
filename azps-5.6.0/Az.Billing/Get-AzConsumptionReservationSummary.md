---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Consumption.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/powershell/module/az.billing/get-azconsumptionreservationsummary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzConsumptionReservationSummary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzConsumptionReservationSummary.md
ms.openlocfilehash: 92647c861f2616d8c9cf8c44534dc2cf6a1138e7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102007323"
---
# <span data-ttu-id="2c64d-101">Get-AzConsumptionReservationSummary</span><span class="sxs-lookup"><span data-stu-id="2c64d-101">Get-AzConsumptionReservationSummary</span></span>

## <span data-ttu-id="2c64d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2c64d-102">SYNOPSIS</span></span>
<span data-ttu-id="2c64d-103">일별 또는 월간 곡물에 대한 예약 요약을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="2c64d-103">Get reservation summaries for daily or monthly grain.</span></span>

## <span data-ttu-id="2c64d-104">구문</span><span class="sxs-lookup"><span data-stu-id="2c64d-104">SYNTAX</span></span>

```
Get-AzConsumptionReservationSummary -Grain <String> -ReservationOrderId <String> [-ReservationId <String>]
 [-StartDate <DateTime>] [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2c64d-105">설명</span><span class="sxs-lookup"><span data-stu-id="2c64d-105">DESCRIPTION</span></span>
<span data-ttu-id="2c64d-106">**Get-AzConsumptionReservationSummary** cmdlet은 일별 또는 월간 그레인에 대한 예약 요약을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="2c64d-106">The **Get-AzConsumptionReservationSummary** cmdlet gets reservation summaries for daily or monthly grain.</span></span>

## <span data-ttu-id="2c64d-107">예제</span><span class="sxs-lookup"><span data-stu-id="2c64d-107">EXAMPLES</span></span>

### <span data-ttu-id="2c64d-108">예제 1: 월별 예약 주문 ID를 통해 예약 요약을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="2c64d-108">Example 1: Get reservation summaries with reservation order Id for monthly grain</span></span>
```powershell
PS C:\> Get-AzConsumptionReservationSummary -Grain monthly -ReservationOrderId ca69259e-bd4f-45c3-bf28-3f353f9cce9b
AvgUtilizationPercentage:  100
Id:  providers/Microsoft.Capacity/reservationOrders/ca69259e-bd4f-45c3-bf28-3f353f9cce9b/reservations/f37f4b70-52ba-4344-a8bd-28abfd21d640/providers/Microsoft.Consumption/reservationSummaries/20170901
MaxUtilizationPercentage:  100
MinUtilizationPercentage:  100
Name:  ca69259e-bd4f-45c3-bf28-3f353f9cce9b_f37f4b70-52ba-4344-a8bd-28abfd21d640_20170901
ReservationId:  f37f4b70-52ba-4344-a8bd-28abfd21d640
ReservationOrderId:  ca69259e-bd4f-45c3-bf28-3f353f9cce9b
ReservedHour:  288
SkuName:  Standard_DS2_v2
Type:  Microsoft.Consumption/reservationSummaries
UsageDate:  9/1/2017 12:00:00 AM
UsedHour:  288
```

### <span data-ttu-id="2c64d-109">예제 2: 예약 주문 ID 및 월별 예약 ID를 통해 예약 요약을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="2c64d-109">Example 2: Get reservation summaries with reservation order Id and reservation Id for monthly grain</span></span>
```powershell
PS C:\> Get-AzConsumptionReservationSummary -Grain monthly -ReservationOrderId ca69259e-bd4f-45c3-bf28-3f353f9cce9b -ReservationId f37f4b70-52ba-4344-a8bd-28abfd21d640
AvgUtilizationPercentage:  100
Id:  providers/Microsoft.Capacity/reservationOrders/ca69259e-bd4f-45c3-bf28-3f353f9cce9b/reservations/f37f4b70-52ba-4344-a8bd-28abfd21d640/providers/Microsoft.Consumption/reservationSummaries/20170901
MaxUtilizationPercentage:  100
MinUtilizationPercentage:  100
Name:  ca69259e-bd4f-45c3-bf28-3f353f9cce9b_f37f4b70-52ba-4344-a8bd-28abfd21d640_20170901
ReservationId:  f37f4b70-52ba-4344-a8bd-28abfd21d640
ReservationOrderId:  ca69259e-bd4f-45c3-bf28-3f353f9cce9b
ReservedHour:  288
SkuName:  Standard_DS2_v2
Type:  Microsoft.Consumption/reservationSummaries
UsageDate:  9/1/2017 12:00:00 AM
UsedHour:  288
```

### <span data-ttu-id="2c64d-110">예제 3: 매일 제공된 날짜 범위에 대한 예약 주문 ID가 있는 예약 요약을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="2c64d-110">Example 3: Get reservation summaries with reservation order Id for daily grain provided date range</span></span>
```powershell
PS C:\> Get-AzConsumptionReservationSummary -Grain daily -ReservationOrderId ca69259e-bd4f-45c3-bf28-3f353f9cce9b -StartDate 2017-10-01 -EndDate 2017-12-07
AvgUtilizationPercentage:  100
Id:  providers/Microsoft.Capacity/reservationOrders/ca69259e-bd4f-45c3-bf28-3f353f9cce9b/reservations/f37f4b70-52ba-4344-a8bd-28abfd21d640/providers/Microsoft.Consumption/reservationSummaries/20171101
MaxUtilizationPercentage:  100
MinUtilizationPercentage:  100
Name:  ca69259e-bd4f-45c3-bf28-3f353f9cce9b_f37f4b70-52ba-4344-a8bd-28abfd21d640_20171101
ReservationId:  f37f4b70-52ba-4344-a8bd-28abfd21d640
ReservationOrderId:  ca69259e-bd4f-45c3-bf28-3f353f9cce9b
ReservedHour:  24
SkuName:  Standard_DS2_v2
Type:  Microsoft.Consumption/reservationSummaries
UsageDate:  11/1/2017 12:00:00 AM
UsedHour:  24
```

### <span data-ttu-id="2c64d-111">예제 4: 예약 주문 ID 및 예약 ID가 제공된 일별 제공 날짜 범위에 대한 예약 요약을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="2c64d-111">Example 4: Get reservation summaries with reservation order Id and reservation Id for daily grain provided date range</span></span>
```powershell
PS C:\> Get-AzConsumptionReservationSummary -Grain daily -ReservationOrderId ca69259e-bd4f-45c3-bf28-3f353f9cce9b -ReservationId f37f4b70-52ba-4344-a8bd-28abfd21d640 -StartDate 2017-10-01 -EndDate 2017-12-07
AvgUtilizationPercentage:  100
Id:  providers/Microsoft.Capacity/reservationOrders/ca69259e-bd4f-45c3-bf28-3f353f9cce9b/reservations/f37f4b70-52ba-4344-a8bd-28abfd21d640/providers/Microsoft.Consumption/reservationSummaries/20171101
MaxUtilizationPercentage:  100
MinUtilizationPercentage:  100
Name:  ca69259e-bd4f-45c3-bf28-3f353f9cce9b_f37f4b70-52ba-4344-a8bd-28abfd21d640_20171101
ReservationId:  f37f4b70-52ba-4344-a8bd-28abfd21d640
ReservationOrderId:  ca69259e-bd4f-45c3-bf28-3f353f9cce9b
ReservedHour:  24
SkuName:  Standard_DS2_v2
Type:  Microsoft.Consumption/reservationSummaries
UsageDate:  11/1/2017 12:00:00 AM
UsedHour:  24
```

## <span data-ttu-id="2c64d-112">매개 변수</span><span class="sxs-lookup"><span data-stu-id="2c64d-112">PARAMETERS</span></span>

### <span data-ttu-id="2c64d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c64d-113">-DefaultProfile</span></span>
<span data-ttu-id="2c64d-114">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2c64d-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2c64d-115">-EndDate</span><span class="sxs-lookup"><span data-stu-id="2c64d-115">-EndDate</span></span>
<span data-ttu-id="2c64d-116">예약 요약의 최종 데이터(UTC의 YYYY-MM-DD)는 일별 그레인에만 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="2c64d-116">The end data (YYYY-MM-DD in UTC) of the reservation summary, required only for daily grain.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c64d-117">-Grain</span><span class="sxs-lookup"><span data-stu-id="2c64d-117">-Grain</span></span>
<span data-ttu-id="2c64d-118">예약 요약의 시간 입자는 매일 또는 월간일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2c64d-118">The time grain of the reservation summary, can be daily or monthly.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: daily, monthly

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c64d-119">-ReservationId</span><span class="sxs-lookup"><span data-stu-id="2c64d-119">-ReservationId</span></span>
<span data-ttu-id="2c64d-120">예약 주문 내에서 예약의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="2c64d-120">The identifier of a reservation within a reservation order.</span></span>

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

### <span data-ttu-id="2c64d-121">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="2c64d-121">-ReservationOrderId</span></span>
<span data-ttu-id="2c64d-122">예약 구매의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="2c64d-122">The identifier of a reservation purchase.</span></span>

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

### <span data-ttu-id="2c64d-123">-StartDate</span><span class="sxs-lookup"><span data-stu-id="2c64d-123">-StartDate</span></span>
<span data-ttu-id="2c64d-124">예약 요약의 시작 데이터(UTC의 YYYY-MM-DD)는 일별 그레인에만 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="2c64d-124">The start data (YYYY-MM-DD in UTC) of the reservation summary, required only for daily grain.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c64d-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c64d-125">CommonParameters</span></span>
<span data-ttu-id="2c64d-126">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="2c64d-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c64d-127">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="2c64d-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c64d-128">입력</span><span class="sxs-lookup"><span data-stu-id="2c64d-128">INPUTS</span></span>

### <span data-ttu-id="2c64d-129">없음</span><span class="sxs-lookup"><span data-stu-id="2c64d-129">None</span></span>

## <span data-ttu-id="2c64d-130">출력</span><span class="sxs-lookup"><span data-stu-id="2c64d-130">OUTPUTS</span></span>

### <span data-ttu-id="2c64d-131">Microsoft.Azure.Commands.Consumption.Models.PSReservationSummary</span><span class="sxs-lookup"><span data-stu-id="2c64d-131">Microsoft.Azure.Commands.Consumption.Models.PSReservationSummary</span></span>

## <span data-ttu-id="2c64d-132">참고 사항</span><span class="sxs-lookup"><span data-stu-id="2c64d-132">NOTES</span></span>

## <span data-ttu-id="2c64d-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2c64d-133">RELATED LINKS</span></span>
