---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Consumption.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/powershell/module/az.billing/get-azconsumptionreservationdetail
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzConsumptionReservationDetail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzConsumptionReservationDetail.md
ms.openlocfilehash: 43ecacc0c54a48091680a6f7a9b33c8294461cdb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101978896"
---
# <span data-ttu-id="0011e-101">Get-AzConsumptionReservationDetail</span><span class="sxs-lookup"><span data-stu-id="0011e-101">Get-AzConsumptionReservationDetail</span></span>

## <span data-ttu-id="0011e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0011e-102">SYNOPSIS</span></span>
<span data-ttu-id="0011e-103">제공된 날짜 범위에 대한 예약 세부 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="0011e-103">Get reservations details for provided date range.</span></span>

## <span data-ttu-id="0011e-104">구문</span><span class="sxs-lookup"><span data-stu-id="0011e-104">SYNTAX</span></span>

```
Get-AzConsumptionReservationDetail -StartDate <DateTime> -EndDate <DateTime> -ReservationOrderId <String>
 [-ReservationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0011e-105">설명</span><span class="sxs-lookup"><span data-stu-id="0011e-105">DESCRIPTION</span></span>
<span data-ttu-id="0011e-106">**Get-AzConsumptionReservationDetail** cmdlet은 제공된 날짜 범위에 대한 예약 세부 정보를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="0011e-106">The **Get-AzConsumptionReservationDetail** cmdlet gets reservations details for provided date range.</span></span>

## <span data-ttu-id="0011e-107">예제</span><span class="sxs-lookup"><span data-stu-id="0011e-107">EXAMPLES</span></span>

### <span data-ttu-id="0011e-108">예제 1: 제공된 날짜 범위에 대한 예약 주문 ID를 통해 예약 세부 정보 확인</span><span class="sxs-lookup"><span data-stu-id="0011e-108">Example 1: Get reservation details with reservation order Id for provided date range</span></span>
```powershell
PS C:\> Get-AzConsumptionReservationDetail -ReservationOrderId ca69259e-bd4f-45c3-bf28-3f353f9cce9b -StartDate 2017-10-01 -EndDate 2017-12-07
Id:  providers/Microsoft.Capacity/reservationOrders/ca69259e-bd4f-45c3-bf28-3f353f9cce9b/reservations/f37f4b70-52ba-4344-a8bd-28abfd21d640providers/Microsoft.Consumption/reservationDetails/20171007
InstanceId:  subscriptions/a98d6dc5-eb8f-46cf-8938-f1fb08f03706/resourcegroups/testrg/providers/microsoft.compute/virtualmachines/std2swindows
Name:  ca69259e-bd4f-45c3-bf28-3f353f9cce9b_f37f4b70-52ba-4344-a8bd-28abfd21d640_20171007
ReservationId:  f37f4b70-52ba-4344-a8bd-28abfd21d640
ReservationOrderId:  ca69259e-bd4f-45c3-bf28-3f353f9cce9b
ReservedHour:  24
SkuName:  Standard_DS2_v2
TotalReservedQuantity:  1
Type:  Microsoft.Consumption/reservationDetails
UsageDate:  10/7/2017 12:00:00 AM
UsedHour:  24
```

### <span data-ttu-id="0011e-109">예제 2: 제공된 날짜 범위에 대한 예약 주문 ID 및 예약 ID를 통해 예약 세부 정보 확인</span><span class="sxs-lookup"><span data-stu-id="0011e-109">Example 2: Get reservation details with reservation order Id and reservation Id for provided date range</span></span>
```powershell
PS C:\> Get-AzConsumptionReservationDetail -ReservationOrderId ca69259e-bd4f-45c3-bf28-3f353f9cce9b -ReservationId f37f4b70-52ba-4344-a8bd-28abfd21d640 -StartDate 2017-10-01 -EndDate 2017-12-07
Id:  providers/Microsoft.Capacity/reservationOrders/ca69259e-bd4f-45c3-bf28-3f353f9cce9b/reservations/f37f4b70-52ba-4344-a8bd-28abfd21d640providers/Microsoft.Consumption/reservationDetails/20171007
InstanceId:  subscriptions/a98d6dc5-eb8f-46cf-8938-f1fb08f03706/resourcegroups/testrg/providers/microsoft.compute/virtualmachines/std2swindows
Name:  ca69259e-bd4f-45c3-bf28-3f353f9cce9b_f37f4b70-52ba-4344-a8bd-28abfd21d640_20171007
ReservationId:  f37f4b70-52ba-4344-a8bd-28abfd21d640
ReservationOrderId:  ca69259e-bd4f-45c3-bf28-3f353f9cce9b
ReservedHour:  24
SkuName:  Standard_DS2_v2
TotalReservedQuantity:  1
Type:  Microsoft.Consumption/reservationDetails
UsageDate:  10/7/2017 12:00:00 AM
UsedHour:  24
```

## <span data-ttu-id="0011e-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="0011e-110">PARAMETERS</span></span>

### <span data-ttu-id="0011e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0011e-111">-DefaultProfile</span></span>
<span data-ttu-id="0011e-112">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0011e-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0011e-113">-EndDate</span><span class="sxs-lookup"><span data-stu-id="0011e-113">-EndDate</span></span>
<span data-ttu-id="0011e-114">예약 세부 정보의 최종 데이터(UTC의 YYYY-MM-DD)입니다.</span><span class="sxs-lookup"><span data-stu-id="0011e-114">The end data (YYYY-MM-DD in UTC) of the reservation detail.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0011e-115">-ReservationId</span><span class="sxs-lookup"><span data-stu-id="0011e-115">-ReservationId</span></span>
<span data-ttu-id="0011e-116">예약 주문 내에서 예약의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="0011e-116">The identifier of a reservation within a reservation order.</span></span>

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

### <span data-ttu-id="0011e-117">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="0011e-117">-ReservationOrderId</span></span>
<span data-ttu-id="0011e-118">예약 구매의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="0011e-118">The identifier of a reservation purchase.</span></span>

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

### <span data-ttu-id="0011e-119">-StartDate</span><span class="sxs-lookup"><span data-stu-id="0011e-119">-StartDate</span></span>
<span data-ttu-id="0011e-120">예약 세부 정보의 시작 데이터(UTC의 YYYY-MM-DD)입니다.</span><span class="sxs-lookup"><span data-stu-id="0011e-120">The start data (YYYY-MM-DD in UTC) of the reservation detail.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0011e-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0011e-121">CommonParameters</span></span>
<span data-ttu-id="0011e-122">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="0011e-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0011e-123">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="0011e-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0011e-124">입력</span><span class="sxs-lookup"><span data-stu-id="0011e-124">INPUTS</span></span>

### <span data-ttu-id="0011e-125">없음</span><span class="sxs-lookup"><span data-stu-id="0011e-125">None</span></span>

## <span data-ttu-id="0011e-126">출력</span><span class="sxs-lookup"><span data-stu-id="0011e-126">OUTPUTS</span></span>

### <span data-ttu-id="0011e-127">Microsoft.Azure.Commands.Consumption.Models.PSReservationDetail</span><span class="sxs-lookup"><span data-stu-id="0011e-127">Microsoft.Azure.Commands.Consumption.Models.PSReservationDetail</span></span>

## <span data-ttu-id="0011e-128">참고 사항</span><span class="sxs-lookup"><span data-stu-id="0011e-128">NOTES</span></span>

## <span data-ttu-id="0011e-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0011e-129">RELATED LINKS</span></span>
