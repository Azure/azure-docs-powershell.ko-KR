---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Consumption.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/get-azconsumptionreservationsummary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzConsumptionReservationSummary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzConsumptionReservationSummary.md
ms.openlocfilehash: a76254f1aeb369e6f93ed8edccfd6f74ff79ceb0
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98496248"
---
# <span data-ttu-id="8b43e-101">Get-AzConsumptionReservationSummary</span><span class="sxs-lookup"><span data-stu-id="8b43e-101">Get-AzConsumptionReservationSummary</span></span>

## <span data-ttu-id="8b43e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8b43e-102">SYNOPSIS</span></span>
<span data-ttu-id="8b43e-103">일별 또는 월별 정리에 대한 예약 요약을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="8b43e-103">Get reservation summaries for daily or monthly grain.</span></span>

## <span data-ttu-id="8b43e-104">구문</span><span class="sxs-lookup"><span data-stu-id="8b43e-104">SYNTAX</span></span>

```
Get-AzConsumptionReservationSummary -Grain <String> -ReservationOrderId <String> [-ReservationId <String>]
 [-StartDate <DateTime>] [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8b43e-105">설명</span><span class="sxs-lookup"><span data-stu-id="8b43e-105">DESCRIPTION</span></span>
<span data-ttu-id="8b43e-106">**Get-AzConsumptionReservationSummary** cmdlet은 일별 또는 월별 세분화에 대한 예약 요약을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="8b43e-106">The **Get-AzConsumptionReservationSummary** cmdlet gets reservation summaries for daily or monthly grain.</span></span>

## <span data-ttu-id="8b43e-107">예제</span><span class="sxs-lookup"><span data-stu-id="8b43e-107">EXAMPLES</span></span>

### <span data-ttu-id="8b43e-108">예제 1: 월별 예약 주문 ID를 통해 예약 요약을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="8b43e-108">Example 1: Get reservation summaries with reservation order Id for monthly grain</span></span>
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

### <span data-ttu-id="8b43e-109">예제 2: 월별 예약 주문 ID 및 예약 ID를 통해 예약 요약을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="8b43e-109">Example 2: Get reservation summaries with reservation order Id and reservation Id for monthly grain</span></span>
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

### <span data-ttu-id="8b43e-110">예제 3: 일별 제공 날짜 범위에 대한 예약 주문 ID를 통해 예약 요약을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="8b43e-110">Example 3: Get reservation summaries with reservation order Id for daily grain provided date range</span></span>
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

### <span data-ttu-id="8b43e-111">예제 4: 일별 제공 날짜 범위에 대한 예약 주문 ID 및 예약 ID를 통해 예약 요약을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="8b43e-111">Example 4: Get reservation summaries with reservation order Id and reservation Id for daily grain provided date range</span></span>
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

## <span data-ttu-id="8b43e-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8b43e-112">PARAMETERS</span></span>

### <span data-ttu-id="8b43e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b43e-113">-DefaultProfile</span></span>
<span data-ttu-id="8b43e-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8b43e-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8b43e-115">-EndDate</span><span class="sxs-lookup"><span data-stu-id="8b43e-115">-EndDate</span></span>
<span data-ttu-id="8b43e-116">예약 요약의 최종 데이터(UTC의 YYYY-MM-DD)는 일별 세분성에만 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="8b43e-116">The end data (YYYY-MM-DD in UTC) of the reservation summary, required only for daily grain.</span></span>

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

### <span data-ttu-id="8b43e-117">-Grain</span><span class="sxs-lookup"><span data-stu-id="8b43e-117">-Grain</span></span>
<span data-ttu-id="8b43e-118">예약 요약의 시간 세분화는 일별 또는 월별일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8b43e-118">The time grain of the reservation summary, can be daily or monthly.</span></span>

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

### <span data-ttu-id="8b43e-119">-ReservationId</span><span class="sxs-lookup"><span data-stu-id="8b43e-119">-ReservationId</span></span>
<span data-ttu-id="8b43e-120">예약 주문 내에서 예약의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="8b43e-120">The identifier of a reservation within a reservation order.</span></span>

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

### <span data-ttu-id="8b43e-121">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="8b43e-121">-ReservationOrderId</span></span>
<span data-ttu-id="8b43e-122">예약 구매의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="8b43e-122">The identifier of a reservation purchase.</span></span>

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

### <span data-ttu-id="8b43e-123">-StartDate</span><span class="sxs-lookup"><span data-stu-id="8b43e-123">-StartDate</span></span>
<span data-ttu-id="8b43e-124">예약 요약의 시작 데이터(UTC의 YYYY-MM-DD)는 일별 세분성에만 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="8b43e-124">The start data (YYYY-MM-DD in UTC) of the reservation summary, required only for daily grain.</span></span>

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

### <span data-ttu-id="8b43e-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b43e-125">CommonParameters</span></span>
<span data-ttu-id="8b43e-126">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="8b43e-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b43e-127">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="8b43e-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b43e-128">입력</span><span class="sxs-lookup"><span data-stu-id="8b43e-128">INPUTS</span></span>

### <span data-ttu-id="8b43e-129">없음</span><span class="sxs-lookup"><span data-stu-id="8b43e-129">None</span></span>

## <span data-ttu-id="8b43e-130">출력</span><span class="sxs-lookup"><span data-stu-id="8b43e-130">OUTPUTS</span></span>

### <span data-ttu-id="8b43e-131">Microsoft.Azure.Commands.Consumption.Models.PSReservationSummary</span><span class="sxs-lookup"><span data-stu-id="8b43e-131">Microsoft.Azure.Commands.Consumption.Models.PSReservationSummary</span></span>

## <span data-ttu-id="8b43e-132">참고 사항</span><span class="sxs-lookup"><span data-stu-id="8b43e-132">NOTES</span></span>

## <span data-ttu-id="8b43e-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8b43e-133">RELATED LINKS</span></span>
