---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Consumption.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/get-azconsumptionmarketplace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzConsumptionMarketplace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzConsumptionMarketplace.md
ms.openlocfilehash: 4533ed3c522cbd1633184b86de68288a3c8dd1ca
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93697672"
---
# <span data-ttu-id="57d23-101">Get-AzConsumptionMarketplace</span><span class="sxs-lookup"><span data-stu-id="57d23-101">Get-AzConsumptionMarketplace</span></span>

## <span data-ttu-id="57d23-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="57d23-102">SYNOPSIS</span></span>
<span data-ttu-id="57d23-103">플랜의 마켓플레이스을 받으세요.</span><span class="sxs-lookup"><span data-stu-id="57d23-103">Get marketplaces of the subscription.</span></span>

## <span data-ttu-id="57d23-104">구문과</span><span class="sxs-lookup"><span data-stu-id="57d23-104">SYNTAX</span></span>

```
Get-AzConsumptionMarketplace [-BillingPeriodName <String>] [-EndDate <DateTime>] [-InstanceId <String>]
 [-InstanceName <String>] [-ResourceGroup <String>] [-StartDate <DateTime>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="57d23-105">설명은</span><span class="sxs-lookup"><span data-stu-id="57d23-105">DESCRIPTION</span></span>
<span data-ttu-id="57d23-106">**AzConsumptionMarketplace** cmdlet은 구독의 마켓플레이스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="57d23-106">The **Get-AzConsumptionMarketplace** cmdlet gets marketplaces of the subscription.</span></span>

## <span data-ttu-id="57d23-107">예제의</span><span class="sxs-lookup"><span data-stu-id="57d23-107">EXAMPLES</span></span>

### <span data-ttu-id="57d23-108">예제 1: 마켓플레이스 사용 가져오기</span><span class="sxs-lookup"><span data-stu-id="57d23-108">Example 1: Get marketplaces usage</span></span>
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

### <span data-ttu-id="57d23-109">예제 2: 날짜 범위를 사용 하 여 마켓플레이스 사용법 가져오기</span><span class="sxs-lookup"><span data-stu-id="57d23-109">Example 2: Get marketplace usage with date range</span></span>
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

### <span data-ttu-id="57d23-110">예제 3: BillingPeriodName의 마켓플레이스 사용법 가져오기</span><span class="sxs-lookup"><span data-stu-id="57d23-110">Example 3: Get marketplace usage of BillingPeriodName</span></span>
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

### <span data-ttu-id="57d23-111">예제 4: InstanceName 필터를 사용 하 여 마켓플레이스 사용 가져오기</span><span class="sxs-lookup"><span data-stu-id="57d23-111">Example 4: Get marketplace usage with InstanceName filter</span></span>
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

## <span data-ttu-id="57d23-112">변수</span><span class="sxs-lookup"><span data-stu-id="57d23-112">PARAMETERS</span></span>

### <span data-ttu-id="57d23-113">-BillingPeriodName</span><span class="sxs-lookup"><span data-stu-id="57d23-113">-BillingPeriodName</span></span>
<span data-ttu-id="57d23-114">연결 하는 마켓플레이스를 받을 특정 청구 기간의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="57d23-114">Name of a specific billing period to get the marketplace that associate with.</span></span>

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

### <span data-ttu-id="57d23-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57d23-115">-DefaultProfile</span></span>
<span data-ttu-id="57d23-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="57d23-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="57d23-117">-EndDate</span><span class="sxs-lookup"><span data-stu-id="57d23-117">-EndDate</span></span>
<span data-ttu-id="57d23-118">필터링 할 마켓플레이스 끝 날짜 (UTC)입니다.</span><span class="sxs-lookup"><span data-stu-id="57d23-118">The end date (in UTC) of the marketplaces to filter.</span></span>

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

### <span data-ttu-id="57d23-119">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="57d23-119">-InstanceId</span></span>
<span data-ttu-id="57d23-120">필터링 할 마켓플레이스의 인스턴스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="57d23-120">The instance id of the marketplaces to filter.</span></span>

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

### <span data-ttu-id="57d23-121">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="57d23-121">-InstanceName</span></span>
<span data-ttu-id="57d23-122">필터링 할 마켓플레이스의 인스턴스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="57d23-122">The instance name of the marketplaces to filter.</span></span>

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

### <span data-ttu-id="57d23-123">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="57d23-123">-ResourceGroup</span></span>
<span data-ttu-id="57d23-124">필터링 할 마켓플레이스의 리소스 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="57d23-124">The resource group of the marketplaces to filter.</span></span>

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

### <span data-ttu-id="57d23-125">-시작 날짜</span><span class="sxs-lookup"><span data-stu-id="57d23-125">-StartDate</span></span>
<span data-ttu-id="57d23-126">필터링 할 마켓플레이스 시작 날짜 (UTC)입니다.</span><span class="sxs-lookup"><span data-stu-id="57d23-126">The start date (in UTC) of the marketplaces to filter.</span></span>

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

### <span data-ttu-id="57d23-127">-위쪽</span><span class="sxs-lookup"><span data-stu-id="57d23-127">-Top</span></span>
<span data-ttu-id="57d23-128">반환할 최대 레코드 수를 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="57d23-128">Determine the maximum number of records to return.</span></span>

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

### <span data-ttu-id="57d23-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57d23-129">CommonParameters</span></span>
<span data-ttu-id="57d23-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="57d23-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57d23-131">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="57d23-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57d23-132">입력</span><span class="sxs-lookup"><span data-stu-id="57d23-132">INPUTS</span></span>

### <span data-ttu-id="57d23-133">않아야</span><span class="sxs-lookup"><span data-stu-id="57d23-133">None</span></span>

## <span data-ttu-id="57d23-134">출력</span><span class="sxs-lookup"><span data-stu-id="57d23-134">OUTPUTS</span></span>

### <span data-ttu-id="57d23-135">Microsoft. i. m a. 모델. PSMarketplace</span><span class="sxs-lookup"><span data-stu-id="57d23-135">Microsoft.Azure.Commands.Consumption.Models.PSMarketplace</span></span>

## <span data-ttu-id="57d23-136">상속자</span><span class="sxs-lookup"><span data-stu-id="57d23-136">NOTES</span></span>

## <span data-ttu-id="57d23-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="57d23-137">RELATED LINKS</span></span>
