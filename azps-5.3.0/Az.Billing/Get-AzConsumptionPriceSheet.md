---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Consumption.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/get-azconsumptionpricesheet
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzConsumptionPriceSheet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzConsumptionPriceSheet.md
ms.openlocfilehash: 999466a754fdeeb98a3d8aaefd91f0b65a2810f7
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98496255"
---
# <span data-ttu-id="39551-101">Get-AzConsumptionPriceSheet</span><span class="sxs-lookup"><span data-stu-id="39551-101">Get-AzConsumptionPriceSheet</span></span>

## <span data-ttu-id="39551-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="39551-102">SYNOPSIS</span></span>
<span data-ttu-id="39551-103">구독의 가격표를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="39551-103">Get price sheets of the subscription.</span></span>

## <span data-ttu-id="39551-104">구문</span><span class="sxs-lookup"><span data-stu-id="39551-104">SYNTAX</span></span>

```
Get-AzConsumptionPriceSheet [-BillingPeriodName <String>] [-ExpandMeterDetail] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="39551-105">설명</span><span class="sxs-lookup"><span data-stu-id="39551-105">DESCRIPTION</span></span>
<span data-ttu-id="39551-106">**Get-AzConsumptionPriceSheet** cmdlet은 구독의 가격표를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="39551-106">The **Get-AzConsumptionPriceSheet** cmdlet gets price sheets of the subscription.</span></span>

## <span data-ttu-id="39551-107">예제</span><span class="sxs-lookup"><span data-stu-id="39551-107">EXAMPLES</span></span>

### <span data-ttu-id="39551-108">예제 1: 가격표를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="39551-108">Example 1: Get price sheets</span></span>
```powershell
PS C:\> Get-AzConsumptionPriceSheet
Id:  subscriptions/1caaa5a3-2b66-438e-8ab4-bce37d518c5d/providers/Microsoft.Billing/billingPeriods/20180601/providers/Microsoft.Consumption/pricesheets/default
Name:  default
Type:  Microsoft.Consumption/pricesheets
Pricesheets:  BillingPeriodId:  subscriptions/1caaa5a3-2b66-438e-8ab4-bce37d518c5d/providers/Microsoft.Billing/billingPeriods/20180601
              CurrencyCode:  USD
              IncludedQuantity:  0
              MeterId:  BACDDD36-2C2C-46BB-8CFA-D13C15EE4A7E
              PartNumber:  AAA-49135
              UnitOfMeasure:  10 Hours
              UnitPrice:  1.33
```

### <span data-ttu-id="39551-109">예제 2: MeterDetails 확장으로 가격표를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="39551-109">Example 2: Get price sheets with expand of MeterDetails</span></span>
```powershell
PS C:\> Get-AzConsumptionPriceSheet -ExpandMeterDetail
Id:  subscriptions/1caaa5a3-2b66-438e-8ab4-bce37d518c5d/providers/Microsoft.Billing/billingPeriods/20180601/providers/Microsoft.Consumption/pricesheets/default
Name:  default
Type:  Microsoft.Consumption/pricesheets
Pricesheets:  BillingPeriodId:  subscriptions/1caaa5a3-2b66-438e-8ab4-bce37d518c5d/providers/Microsoft.Billing/billingPeriods/20180601
              CurrencyCode:  USD
              IncludedQuantity:  0
              MeterDetails:  MeterCategory:  Virtual Machines
                             MeterLocation:  US North Central
                             MeterName:  Compute Hours
                             MeterSubCategory:  Standard_D11_v2 VM_Promo (Windows)
                             Unit:  Hours
              MeterId:  BACDDD36-2C2C-46BB-8CFA-D13C15EE4A7E
              PartNumber:  AAA-49135
              UnitOfMeasure:  10 Hours
              UnitPrice:  1.33
```

### <span data-ttu-id="39551-110">예제 3: BillingPeriodName의 가격표를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="39551-110">Example 3: Get price sheets of BillingPeriodName</span></span>
```powershell
PS C:\> Get-AzConsumptionPriceSheet -BillingPeriodName 201712
Id:  subscriptions/1caaa5a3-2b66-438e-8ab4-bce37d518c5d/providers/Microsoft.Billing/billingPeriods/20180601/providers/Microsoft.Consumption/pricesheets/default
Name:  default
Type:  Microsoft.Consumption/pricesheets
Pricesheets:  BillingPeriodId:  subscriptions/1caaa5a3-2b66-438e-8ab4-bce37d518c5d/providers/Microsoft.Billing/billingPeriods/20180601
              CurrencyCode:  USD
              IncludedQuantity:  0
              MeterId:  46367D67-1E4C-4ED4-8267-4477083F581C
              PartNumber:  AAA-53590
              UnitOfMeasure:  10 Hours
              UnitPrice:  1.37
```

### <span data-ttu-id="39551-111">예제 4: 가격표의 상위 5개 레코드를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="39551-111">Example 4: Get top 5 records of price sheets</span></span>
```powershell
PS C:\> Get-AzConsumptionPriceSheet -Top 5
Id:  subscriptions/1caaa5a3-2b66-438e-8ab4-bce37d518c5d/providers/Microsoft.Billing/billingPeriods/20180601/providers/Microsoft.Consumption/pricesheets/default
Name:  default
Type:  Microsoft.Consumption/pricesheets
Pricesheets:  BillingPeriodId:  subscriptions/1caaa5a3-2b66-438e-8ab4-bce37d518c5d/providers/Microsoft.Billing/billingPeriods/20180601
              CurrencyCode:  USD
              IncludedQuantity:  0
              MeterId:  BACDDD36-2C2C-46BB-8CFA-D13C15EE4A7E
              PartNumber:  AAA-49135
              UnitOfMeasure:  10 Hours
              UnitPrice:  1.33
```

## <span data-ttu-id="39551-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="39551-112">PARAMETERS</span></span>

### <span data-ttu-id="39551-113">-BillingPeriodName</span><span class="sxs-lookup"><span data-stu-id="39551-113">-BillingPeriodName</span></span>
<span data-ttu-id="39551-114">연결된 가격표를 구할 특정 청구 기간의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="39551-114">Name of a specific billing period to get the price sheets that associate with.</span></span>

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

### <span data-ttu-id="39551-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39551-115">-DefaultProfile</span></span>
<span data-ttu-id="39551-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="39551-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="39551-117">-ExpandMeterDetail</span><span class="sxs-lookup"><span data-stu-id="39551-117">-ExpandMeterDetail</span></span>
<span data-ttu-id="39551-118">MeterDetails에 따라 가격표를 확장합니다.</span><span class="sxs-lookup"><span data-stu-id="39551-118">Expand the price sheets based on MeterDetails.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39551-119">-Top</span><span class="sxs-lookup"><span data-stu-id="39551-119">-Top</span></span>
<span data-ttu-id="39551-120">반환할 레코드의 최대 수를 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="39551-120">Determine the maximum number of records to return.</span></span>

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

### <span data-ttu-id="39551-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39551-121">CommonParameters</span></span>
<span data-ttu-id="39551-122">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="39551-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39551-123">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="39551-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39551-124">입력</span><span class="sxs-lookup"><span data-stu-id="39551-124">INPUTS</span></span>

### <span data-ttu-id="39551-125">없음</span><span class="sxs-lookup"><span data-stu-id="39551-125">None</span></span>

## <span data-ttu-id="39551-126">출력</span><span class="sxs-lookup"><span data-stu-id="39551-126">OUTPUTS</span></span>

### <span data-ttu-id="39551-127">Microsoft.Azure.Commands.Consumption.Models.PSPriceSheet</span><span class="sxs-lookup"><span data-stu-id="39551-127">Microsoft.Azure.Commands.Consumption.Models.PSPriceSheet</span></span>

## <span data-ttu-id="39551-128">참고 사항</span><span class="sxs-lookup"><span data-stu-id="39551-128">NOTES</span></span>

## <span data-ttu-id="39551-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="39551-129">RELATED LINKS</span></span>
