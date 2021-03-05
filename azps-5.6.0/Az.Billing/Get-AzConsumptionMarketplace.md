---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Consumption.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/powershell/module/az.billing/get-azconsumptionmarketplace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzConsumptionMarketplace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzConsumptionMarketplace.md
ms.openlocfilehash: abf94b678d7c9e4726cf919d4673ea0750a438f1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101983435"
---
# <span data-ttu-id="70593-101">Get-AzConsumptionMarketplace</span><span class="sxs-lookup"><span data-stu-id="70593-101">Get-AzConsumptionMarketplace</span></span>

## <span data-ttu-id="70593-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="70593-102">SYNOPSIS</span></span>
<span data-ttu-id="70593-103">구독의 마켓플레이스를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="70593-103">Get marketplaces of the subscription.</span></span>

## <span data-ttu-id="70593-104">구문</span><span class="sxs-lookup"><span data-stu-id="70593-104">SYNTAX</span></span>

```
Get-AzConsumptionMarketplace [-BillingPeriodName <String>] [-EndDate <DateTime>] [-InstanceId <String>]
 [-InstanceName <String>] [-ResourceGroup <String>] [-StartDate <DateTime>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="70593-105">설명</span><span class="sxs-lookup"><span data-stu-id="70593-105">DESCRIPTION</span></span>
<span data-ttu-id="70593-106">**Get-AzConsumptionMarketplace** cmdlet은 구독의 마켓플레이스를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="70593-106">The **Get-AzConsumptionMarketplace** cmdlet gets marketplaces of the subscription.</span></span>

## <span data-ttu-id="70593-107">예제</span><span class="sxs-lookup"><span data-stu-id="70593-107">EXAMPLES</span></span>

### <span data-ttu-id="70593-108">예제 1: 마켓플레이스 사용 현황 확인</span><span class="sxs-lookup"><span data-stu-id="70593-108">Example 1: Get marketplaces usage</span></span>
```powershell
PS C:\> Get-AzConsumptionMarketplace -Top 10
BillingPeriodId:  subscriptions/6b74c45b-9597-4939-a202-36b2ee8fbb3d/providers/Microsoft.Billing/billingPeriods/201807-1
ConsumedQuantity:  24
Currency:  USD
Id:  subscriptions/6b74c45b-9597-4939-a202-36b2ee8fbb3d/providers/Microsoft.Billing/billingPeriods/201807-1/providers/Microsoft.Consumption/marketplaces/018b7291-57a5-e194-65ea-28c3f1db76aa
InstanceId:  subscriptions/6b74c45b-9597-4939-a202-36b2ee8fbb3d/resourceGroups/TESTRG1/providers/Microsoft.Compute/virtualMachines/TestVM
InstanceName:  TestVM
IsEstimated:  false
Name:  018b7291-57a5-e194-65ea-28c3f1db76aa
OfferName:  2b380487-dc18-4e5d-981f-1ee2cc59e776
PretaxCost:  0
ResourceRate:  0
SubscriptionGuid:  6b74c45b-9597-4939-a202-36b2ee8fbb3d
Type:  Microsoft.Consumption/usageDetails
UsageEnd:  2018-04-29T00:00:00Z
UsageStart:  2018-04-28T00:00:00Z
```

### <span data-ttu-id="70593-109">예제 2: 날짜 범위로 마켓플레이스 사용량을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="70593-109">Example 2: Get marketplace usage with date range</span></span>
```powershell
PS C:\> Get-AzConsumptionMarketplace -StartDate 2018-01-03 -EndDate 2018-01-20 -Top 10
BillingPeriodId:  subscriptions/6b74c45b-9597-4939-a202-36b2ee8fbb3d/providers/Microsoft.Billing/billingPeriods/201803-1
ConsumedQuantity:  24
Currency:  USD
Id:  subscriptions/6b74c45b-9597-4939-a202-36b2ee8fbb3d/providers/Microsoft.Billing/billingPeriods/201803-1/providers/Microsoft.Consumption/marketplaces/0ec2bd1e-1cd6-0c75-3661-eaf3f635df33
InstanceId:  subscriptions/6b74c45b-9597-4939-a202-36b2ee8fbb3d/resourceGroups/TESTRG1/providers/Microsoft.Compute/virtualMachines/TestVM
InstanceName:  TestVM
IsEstimated:  false
Name:  0ec2bd1e-1cd6-0c75-3661-eaf3f635df33
OfferName:  2b380487-dc18-4e5d-981f-1ee2cc59e776
PretaxCost:  0
ResourceRate:  0
SubscriptionGuid:  6b74c45b-9597-4939-a202-36b2ee8fbb3d
Type:  Microsoft.Consumption/usageDetails
UsageEnd:  2018-01-04T00:00:00Z
UsageStart:  2018-01-03T00:00:00Z
```

### <span data-ttu-id="70593-110">예제 3: BillingPeriodName의 마켓플레이스 사용</span><span class="sxs-lookup"><span data-stu-id="70593-110">Example 3: Get marketplace usage of BillingPeriodName</span></span>
```powershell
PS C:\> Get-AzConsumptionMarketplace -BillingPeriodName 201801-1 -Top 10
BillingPeriodId:  subscriptions/6b74c45b-9597-4939-a202-36b2ee8fbb3d/providers/Microsoft.Billing/billingPeriods/201801-1
ConsumedQuantity:  24
Currency:  USD
Id:  subscriptions/6b74c45b-9597-4939-a202-36b2ee8fbb3d/providers/Microsoft.Billing/billingPeriods/201801-1/providers/Microsoft.Consumption/marketplaces/ea82233a-9f76-7eaa-4478-42bd61cf6287
InstanceId:  subscriptions/6b74c45b-9597-4939-a202-36b2ee8fbb3d/resourceGroups/TESTRG1/providers/Microsoft.Compute/virtualMachines/TestVM
InstanceName:  TestVM
IsEstimated:  false
Name:  ea82233a-9f76-7eaa-4478-42bd61cf6287
OfferName:  2b380487-dc18-4e5d-981f-1ee2cc59e776
PretaxCost:  0
ResourceRate:  0
SubscriptionGuid:  6b74c45b-9597-4939-a202-36b2ee8fbb3d
Type:  Microsoft.Consumption/usageDetails
UsageEnd:  2017-10-29T00:00:00Z
UsageStart:  2017-10-28T00:00:00Z
```

### <span data-ttu-id="70593-111">예제 4: InstanceName 필터를 사용하여 마켓플레이스 사용 현황 확인</span><span class="sxs-lookup"><span data-stu-id="70593-111">Example 4: Get marketplace usage with InstanceName filter</span></span>
```powershell
PS C:\> Get-AzConsumptionMarketplace -InstanceName TestVM -Top 10
BillingPeriodId:  subscriptions/6b74c45b-9597-4939-a202-36b2ee8fbb3d/providers/Microsoft.Billing/billingPeriods/201807-1
ConsumedQuantity:  24
Currency:  USD
Id:  subscriptions/6b74c45b-9597-4939-a202-36b2ee8fbb3d/providers/Microsoft.Billing/billingPeriods/201807-1/providers/Microsoft.Consumption/marketplaces/018b7291-57a5-e194-65ea-28c3f1db76aa
InstanceId:  subscriptions/6b74c45b-9597-4939-a202-36b2ee8fbb3d/resourceGroups/TESTRG1/providers/Microsoft.Compute/virtualMachines/TestVM
InstanceName:  TestVM
IsEstimated:  false
Name:  018b7291-57a5-e194-65ea-28c3f1db76aa
OfferName:  2b380487-dc18-4e5d-981f-1ee2cc59e776
PretaxCost:  0
ResourceRate:  0
SubscriptionGuid:  6b74c45b-9597-4939-a202-36b2ee8fbb3d
Type:  Microsoft.Consumption/usageDetails
UsageEnd:  2018-04-29T00:00:00Z
UsageStart:  2018-04-28T00:00:00Z
```

## <span data-ttu-id="70593-112">매개 변수</span><span class="sxs-lookup"><span data-stu-id="70593-112">PARAMETERS</span></span>

### <span data-ttu-id="70593-113">-BillingPeriodName</span><span class="sxs-lookup"><span data-stu-id="70593-113">-BillingPeriodName</span></span>
<span data-ttu-id="70593-114">연결된 마켓플레이스를 얻을 수 있는 특정 청구 기간의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="70593-114">Name of a specific billing period to get the marketplace that associate with.</span></span>

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

### <span data-ttu-id="70593-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70593-115">-DefaultProfile</span></span>
<span data-ttu-id="70593-116">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="70593-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="70593-117">-EndDate</span><span class="sxs-lookup"><span data-stu-id="70593-117">-EndDate</span></span>
<span data-ttu-id="70593-118">필터링할 마켓플레이스의 종료 날짜(UTC)입니다.</span><span class="sxs-lookup"><span data-stu-id="70593-118">The end date (in UTC) of the marketplaces to filter.</span></span>

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

### <span data-ttu-id="70593-119">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="70593-119">-InstanceId</span></span>
<span data-ttu-id="70593-120">필터링할 마켓플레이스의 인스턴스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="70593-120">The instance id of the marketplaces to filter.</span></span>

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

### <span data-ttu-id="70593-121">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="70593-121">-InstanceName</span></span>
<span data-ttu-id="70593-122">필터링할 마켓플레이스의 인스턴스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="70593-122">The instance name of the marketplaces to filter.</span></span>

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

### <span data-ttu-id="70593-123">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="70593-123">-ResourceGroup</span></span>
<span data-ttu-id="70593-124">필터링할 마켓플레이스의 리소스 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="70593-124">The resource group of the marketplaces to filter.</span></span>

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

### <span data-ttu-id="70593-125">-StartDate</span><span class="sxs-lookup"><span data-stu-id="70593-125">-StartDate</span></span>
<span data-ttu-id="70593-126">필터링할 마켓플레이스의 시작 날짜(UTC)입니다.</span><span class="sxs-lookup"><span data-stu-id="70593-126">The start date (in UTC) of the marketplaces to filter.</span></span>

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

### <span data-ttu-id="70593-127">-Top</span><span class="sxs-lookup"><span data-stu-id="70593-127">-Top</span></span>
<span data-ttu-id="70593-128">반환할 레코드의 최대 수를 결정합니다.</span><span class="sxs-lookup"><span data-stu-id="70593-128">Determine the maximum number of records to return.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70593-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70593-129">CommonParameters</span></span>
<span data-ttu-id="70593-130">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="70593-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70593-131">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="70593-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70593-132">입력</span><span class="sxs-lookup"><span data-stu-id="70593-132">INPUTS</span></span>

### <span data-ttu-id="70593-133">없음</span><span class="sxs-lookup"><span data-stu-id="70593-133">None</span></span>

## <span data-ttu-id="70593-134">출력</span><span class="sxs-lookup"><span data-stu-id="70593-134">OUTPUTS</span></span>

### <span data-ttu-id="70593-135">Microsoft.Azure.Commands.Consumption.Models.PSMarketplace</span><span class="sxs-lookup"><span data-stu-id="70593-135">Microsoft.Azure.Commands.Consumption.Models.PSMarketplace</span></span>

## <span data-ttu-id="70593-136">참고 사항</span><span class="sxs-lookup"><span data-stu-id="70593-136">NOTES</span></span>

## <span data-ttu-id="70593-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="70593-137">RELATED LINKS</span></span>
