---
external help file: Microsoft.Azure.Commands.Consumption.dll-Help.xml
Module Name: AzureRM.Consumption
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.consumption/get-azurermconsumptionpricesheet
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Consumption/Commands.Consumption/help/Get-AzureRmConsumptionPriceSheet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Consumption/Commands.Consumption/help/Get-AzureRmConsumptionPriceSheet.md
ms.openlocfilehash: 46e38df713483b60735247c7fafe984fc5fb6d52
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93528559"
---
# <span data-ttu-id="6f2c0-101">Get-AzureRmConsumptionPriceSheet</span><span class="sxs-lookup"><span data-stu-id="6f2c0-101">Get-AzureRmConsumptionPriceSheet</span></span>

## <span data-ttu-id="6f2c0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6f2c0-102">SYNOPSIS</span></span>
<span data-ttu-id="6f2c0-103">플랜의 가격 시트를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6f2c0-103">Get price sheets of the subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6f2c0-104">구문과</span><span class="sxs-lookup"><span data-stu-id="6f2c0-104">SYNTAX</span></span>

```
Get-AzureRmConsumptionPriceSheet [-BillingPeriodName <String>] [-ExpandMeterDetail] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6f2c0-105">설명은</span><span class="sxs-lookup"><span data-stu-id="6f2c0-105">DESCRIPTION</span></span>
<span data-ttu-id="6f2c0-106">**AzureRmConsumptionPriceSheet** cmdlet은 구독에 대 한 가격 시트를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6f2c0-106">The **Get-AzureRmConsumptionPriceSheet** cmdlet gets price sheets of the subscription.</span></span>

## <span data-ttu-id="6f2c0-107">예제의</span><span class="sxs-lookup"><span data-stu-id="6f2c0-107">EXAMPLES</span></span>

### <span data-ttu-id="6f2c0-108">예제 1: 가격 시트 가져오기</span><span class="sxs-lookup"><span data-stu-id="6f2c0-108">Example 1: Get price sheets</span></span>
```powershell
PS C:\> Get-AzureRmConsumptionPriceSheet
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

### <span data-ttu-id="6f2c0-109">예제 2: MeterDetails 확대 된 가격 시트 가져오기</span><span class="sxs-lookup"><span data-stu-id="6f2c0-109">Example 2: Get price sheets with expand of MeterDetails</span></span>
```powershell
PS C:\> Get-AzureRmConsumptionPriceSheet -ExpandMeterDetail
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

### <span data-ttu-id="6f2c0-110">예제 3: BillingPeriodName의 가격 시트 가져오기</span><span class="sxs-lookup"><span data-stu-id="6f2c0-110">Example 3: Get price sheets of BillingPeriodName</span></span>
```powershell
PS C:\> Get-AzureRmConsumptionPriceSheet -BillingPeriodName 201712
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

### <span data-ttu-id="6f2c0-111">예제 4: 가격 시트의 상위 5 개 레코드 가져오기</span><span class="sxs-lookup"><span data-stu-id="6f2c0-111">Example 4: Get top 5 records of price sheets</span></span>
```powershell
PS C:\> Get-AzureRmConsumptionPriceSheet -Top 5
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

## <span data-ttu-id="6f2c0-112">변수</span><span class="sxs-lookup"><span data-stu-id="6f2c0-112">PARAMETERS</span></span>

### <span data-ttu-id="6f2c0-113">-BillingPeriodName</span><span class="sxs-lookup"><span data-stu-id="6f2c0-113">-BillingPeriodName</span></span>
<span data-ttu-id="6f2c0-114">특정 청구 기간의 이름에 연결 된 가격 시트를 가져오는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6f2c0-114">Name of a specific billing period to get the price sheets that associate with.</span></span>

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

### <span data-ttu-id="6f2c0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f2c0-115">-DefaultProfile</span></span>
<span data-ttu-id="6f2c0-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6f2c0-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6f2c0-117">-ExpandMeterDetail</span><span class="sxs-lookup"><span data-stu-id="6f2c0-117">-ExpandMeterDetail</span></span>
<span data-ttu-id="6f2c0-118">MeterDetails를 기반으로 가격 시트를 확장 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f2c0-118">Expand the price sheets based on MeterDetails.</span></span>

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

### <span data-ttu-id="6f2c0-119">-위쪽</span><span class="sxs-lookup"><span data-stu-id="6f2c0-119">-Top</span></span>
<span data-ttu-id="6f2c0-120">반환할 최대 레코드 수를 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f2c0-120">Determine the maximum number of records to return.</span></span>

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

### <span data-ttu-id="6f2c0-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f2c0-121">CommonParameters</span></span>
<span data-ttu-id="6f2c0-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f2c0-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f2c0-123">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6f2c0-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f2c0-124">입력</span><span class="sxs-lookup"><span data-stu-id="6f2c0-124">INPUTS</span></span>

### <span data-ttu-id="6f2c0-125">않아야</span><span class="sxs-lookup"><span data-stu-id="6f2c0-125">None</span></span>

## <span data-ttu-id="6f2c0-126">출력</span><span class="sxs-lookup"><span data-stu-id="6f2c0-126">OUTPUTS</span></span>

### <span data-ttu-id="6f2c0-127">PSPriceSheet를 사용 하 여 명령을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f2c0-127">Microsoft.Azure.Commands.Consumption.Models.PSPriceSheet</span></span>

## <span data-ttu-id="6f2c0-128">상속자</span><span class="sxs-lookup"><span data-stu-id="6f2c0-128">NOTES</span></span>

## <span data-ttu-id="6f2c0-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6f2c0-129">RELATED LINKS</span></span>
