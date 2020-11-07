---
external help file: Microsoft.Azure.Commands.Consumption.dll-Help.xml
Module Name: AzureRM.Consumption
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.consumption/get-azurermconsumptionreservationdetail
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Consumption/Commands.Consumption/help/Get-AzureRmConsumptionReservationDetail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Consumption/Commands.Consumption/help/Get-AzureRmConsumptionReservationDetail.md
ms.openlocfilehash: a7a4b50198a63329b0d45986f2bce60edb927777
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93702113"
---
# <span data-ttu-id="8a316-101">Get-AzureRmConsumptionReservationDetail</span><span class="sxs-lookup"><span data-stu-id="8a316-101">Get-AzureRmConsumptionReservationDetail</span></span>

## <span data-ttu-id="8a316-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8a316-102">SYNOPSIS</span></span>
<span data-ttu-id="8a316-103">제공 된 날짜 범위에 대 한 예약 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8a316-103">Get reservations details for provided date range.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8a316-104">구문과</span><span class="sxs-lookup"><span data-stu-id="8a316-104">SYNTAX</span></span>

```
Get-AzureRmConsumptionReservationDetail -StartDate <DateTime> -EndDate <DateTime> -ReservationOrderId <String>
 [-ReservationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8a316-105">설명은</span><span class="sxs-lookup"><span data-stu-id="8a316-105">DESCRIPTION</span></span>
<span data-ttu-id="8a316-106">**AzureRmConsumptionReservationDetail** cmdlet은 제공 된 날짜 범위에 대 한 예약 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8a316-106">The **Get-AzureRmConsumptionReservationDetail** cmdlet gets reservations details for provided date range.</span></span>

## <span data-ttu-id="8a316-107">예제의</span><span class="sxs-lookup"><span data-stu-id="8a316-107">EXAMPLES</span></span>

### <span data-ttu-id="8a316-108">예제 1: 제공 된 날짜 범위의 예약 주문 Id를 사용 하 여 예약 세부 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="8a316-108">Example 1: Get reservation details with reservation order Id for provided date range</span></span>
```powershell
PS C:\> Get-AzureRmConsumptionReservationDetail -ReservationOrderId ca69259e-bd4f-45c3-bf28-3f353f9cce9b -StartDate 2017-10-01 -EndDate 2017-12-07
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

### <span data-ttu-id="8a316-109">예제 2: 예약 주문 Id 및 제공 된 날짜 범위에 대 한 예약 Id를 사용 하 여 예약 세부 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="8a316-109">Example 2: Get reservation details with reservation order Id and reservation Id for provided date range</span></span>
```powershell
PS C:\> Get-AzureRmConsumptionReservationDetail -ReservationOrderId ca69259e-bd4f-45c3-bf28-3f353f9cce9b -ReservationId f37f4b70-52ba-4344-a8bd-28abfd21d640 -StartDate 2017-10-01 -EndDate 2017-12-07
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

## <span data-ttu-id="8a316-110">변수</span><span class="sxs-lookup"><span data-stu-id="8a316-110">PARAMETERS</span></span>

### <span data-ttu-id="8a316-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a316-111">-DefaultProfile</span></span>
<span data-ttu-id="8a316-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8a316-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a316-113">-EndDate</span><span class="sxs-lookup"><span data-stu-id="8a316-113">-EndDate</span></span>
<span data-ttu-id="8a316-114">예약 정보에 대 한 최종 데이터 (UTC의 YYYY-MM-DD)입니다.</span><span class="sxs-lookup"><span data-stu-id="8a316-114">The end data (YYYY-MM-DD in UTC) of the reservation detail.</span></span>

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

### <span data-ttu-id="8a316-115">-ReservationId</span><span class="sxs-lookup"><span data-stu-id="8a316-115">-ReservationId</span></span>
<span data-ttu-id="8a316-116">예약 순서 내에서 예약의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="8a316-116">The identifier of a reservation within a reservation order.</span></span>

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

### <span data-ttu-id="8a316-117">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="8a316-117">-ReservationOrderId</span></span>
<span data-ttu-id="8a316-118">예약 구입의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="8a316-118">The identifier of a reservation purchase.</span></span>

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

### <span data-ttu-id="8a316-119">-시작 날짜</span><span class="sxs-lookup"><span data-stu-id="8a316-119">-StartDate</span></span>
<span data-ttu-id="8a316-120">예약 정보에 대 한 시작 데이터 (UTC의 YYYY-MM-DD)입니다.</span><span class="sxs-lookup"><span data-stu-id="8a316-120">The start data (YYYY-MM-DD in UTC) of the reservation detail.</span></span>

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

### <span data-ttu-id="8a316-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a316-121">CommonParameters</span></span>
<span data-ttu-id="8a316-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8a316-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a316-123">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8a316-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a316-124">입력</span><span class="sxs-lookup"><span data-stu-id="8a316-124">INPUTS</span></span>

### <span data-ttu-id="8a316-125">않아야</span><span class="sxs-lookup"><span data-stu-id="8a316-125">None</span></span>

## <span data-ttu-id="8a316-126">출력</span><span class="sxs-lookup"><span data-stu-id="8a316-126">OUTPUTS</span></span>

### <span data-ttu-id="8a316-127">PSReservationDetail를 사용 하 여 명령을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="8a316-127">Microsoft.Azure.Commands.Consumption.Models.PSReservationDetail</span></span>

## <span data-ttu-id="8a316-128">상속자</span><span class="sxs-lookup"><span data-stu-id="8a316-128">NOTES</span></span>

## <span data-ttu-id="8a316-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8a316-129">RELATED LINKS</span></span>
