---
external help file: Microsoft.Azure.Commands.Consumption.dll-Help.xml
Module Name: AzureRM.Consumption
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.consumption/get-azurermconsumptionusagedetail
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Consumption/Commands.Consumption/help/Get-AzureRmConsumptionUsageDetail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Consumption/Commands.Consumption/help/Get-AzureRmConsumptionUsageDetail.md
ms.openlocfilehash: 2694ce516b1bb3202fc194e1c1eec55610f7b92a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525228"
---
# <span data-ttu-id="acea2-101">Get-AzureRmConsumptionUsageDetail</span><span class="sxs-lookup"><span data-stu-id="acea2-101">Get-AzureRmConsumptionUsageDetail</span></span>

## <span data-ttu-id="acea2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="acea2-102">SYNOPSIS</span></span>
<span data-ttu-id="acea2-103">구독에 대 한 사용 현황 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="acea2-103">Get usage details of the subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="acea2-104">구문과</span><span class="sxs-lookup"><span data-stu-id="acea2-104">SYNTAX</span></span>

### <span data-ttu-id="acea2-105">구독 (기본값)</span><span class="sxs-lookup"><span data-stu-id="acea2-105">Subscription (Default)</span></span>
```
Get-AzureRmConsumptionUsageDetail [-MaxCount <Int32>] [-IncludeMeterDetails] [-IncludeAdditionalProperties]
 [-StartDate <DateTime>] [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="acea2-106">청구</span><span class="sxs-lookup"><span data-stu-id="acea2-106">Invoice</span></span>
```
Get-AzureRmConsumptionUsageDetail -InvoiceName <String> [-MaxCount <Int32>] [-IncludeMeterDetails]
 [-IncludeAdditionalProperties] [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="acea2-107">BillingPeriod</span><span class="sxs-lookup"><span data-stu-id="acea2-107">BillingPeriod</span></span>
```
Get-AzureRmConsumptionUsageDetail -BillingPeriodName <String> [-MaxCount <Int32>] [-IncludeMeterDetails]
 [-IncludeAdditionalProperties] [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="acea2-108">설명은</span><span class="sxs-lookup"><span data-stu-id="acea2-108">DESCRIPTION</span></span>
<span data-ttu-id="acea2-109">**AzureRmConsumptionUsageDetail** cmdlet은 구독에 대 한 사용 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="acea2-109">The **Get-AzureRmConsumptionUsageDetail** cmdlet gets usage details of the subscription.</span></span> 

## <span data-ttu-id="acea2-110">예제의</span><span class="sxs-lookup"><span data-stu-id="acea2-110">EXAMPLES</span></span>

### <span data-ttu-id="acea2-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="acea2-111">Example 1</span></span>
```
PS C:\> Get-AzureRmConsumptionUsageDetail -IncludeMeterDetails -InvoiceName 201704-117283130069214
```

<span data-ttu-id="acea2-112">지정 된 이름을 사용 하 여 송장의 사용 정보를 가져오고 결과에 MeterDetails 속성을 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="acea2-112">Get usage details of the invoice with specified name, and include MeterDetails property in the result.</span></span>

### <span data-ttu-id="acea2-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="acea2-113">Example 2</span></span>
```
PS C:\> Get-AzureRmConsumptionUsageDetail -IncludeAdditionalProperties -BillingPeriodName 201704-1
```

<span data-ttu-id="acea2-114">지정 된 이름의 청구 기간에 대 한 사용 세부 정보를 얻고 결과에 AdditionalProperties 속성을 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="acea2-114">Get usage details of the billing period with specified name, and include AdditionalProperties property in the result.</span></span>

### <span data-ttu-id="acea2-115">예제 3</span><span class="sxs-lookup"><span data-stu-id="acea2-115">Example 3</span></span>
```
PS C:\> Get-AzureRmConsumptionUsageDetail -StartDate 2017-01-17 -EndDate 2017-01-19
```

<span data-ttu-id="acea2-116">2017-01-17에서 2017-01-19 사이의 구독에 대 한 사용 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="acea2-116">Get usage details of the subscription that is between 2017-01-17 to 2017-01-19.</span></span>

## <span data-ttu-id="acea2-117">변수</span><span class="sxs-lookup"><span data-stu-id="acea2-117">PARAMETERS</span></span>

### <span data-ttu-id="acea2-118">-BillingPeriodName</span><span class="sxs-lookup"><span data-stu-id="acea2-118">-BillingPeriodName</span></span>
<span data-ttu-id="acea2-119">와 연결 되는 사용 세부 정보를 가져올 특정 청구 기간의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="acea2-119">Name of a specific billing period to get the usage details that associate with.</span></span>

```yaml
Type: String
Parameter Sets: BillingPeriod
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="acea2-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="acea2-120">-DefaultProfile</span></span>
<span data-ttu-id="acea2-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="acea2-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="acea2-122">-EndDate</span><span class="sxs-lookup"><span data-stu-id="acea2-122">-EndDate</span></span>
<span data-ttu-id="acea2-123">사용의 끝 날짜 (UTC)입니다.</span><span class="sxs-lookup"><span data-stu-id="acea2-123">The end date (in UTC) of the usages.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="acea2-124">-IncludeAdditionalProperties</span><span class="sxs-lookup"><span data-stu-id="acea2-124">-IncludeAdditionalProperties</span></span>
<span data-ttu-id="acea2-125">용도에 추가 속성을 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="acea2-125">Include additional properties in the usages.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="acea2-126">-IncludeMeterDetails</span><span class="sxs-lookup"><span data-stu-id="acea2-126">-IncludeMeterDetails</span></span>
<span data-ttu-id="acea2-127">용도에 측정기 세부 정보를 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="acea2-127">Include meter details in the usages.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="acea2-128">-InvoiceName</span><span class="sxs-lookup"><span data-stu-id="acea2-128">-InvoiceName</span></span>
<span data-ttu-id="acea2-129">에 연결 되는 사용 현황 정보를 가져올 특정 송장의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="acea2-129">Name of a specific invoice to get the usage details that associate with.</span></span>

```yaml
Type: String
Parameter Sets: Invoice
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="acea2-130">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="acea2-130">-MaxCount</span></span>
<span data-ttu-id="acea2-131">반환할 최대 레코드 수를 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="acea2-131">Determine the maximum number of records to return.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="acea2-132">-시작 날짜</span><span class="sxs-lookup"><span data-stu-id="acea2-132">-StartDate</span></span>
<span data-ttu-id="acea2-133">용도 시작 날짜 (UTC)입니다.</span><span class="sxs-lookup"><span data-stu-id="acea2-133">The start date (in UTC) of the usages.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="acea2-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="acea2-134">CommonParameters</span></span>
<span data-ttu-id="acea2-135">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="acea2-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="acea2-136">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="acea2-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="acea2-137">입력</span><span class="sxs-lookup"><span data-stu-id="acea2-137">INPUTS</span></span>

### <span data-ttu-id="acea2-138">않아야</span><span class="sxs-lookup"><span data-stu-id="acea2-138">None</span></span>

## <span data-ttu-id="acea2-139">출력</span><span class="sxs-lookup"><span data-stu-id="acea2-139">OUTPUTS</span></span>

### <span data-ttu-id="acea2-140">System.webserver. List ' 1 [[Microsoft PSUsageDetail, Microsoft azure. 0.1.0.0, Version =, Culture = 중립, PublicKeyToken = null]])</span><span class="sxs-lookup"><span data-stu-id="acea2-140">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Consumption.Models.PSUsageDetail, Microsoft.Azure.Commands.Consumption, Version=0.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="acea2-141">상속자</span><span class="sxs-lookup"><span data-stu-id="acea2-141">NOTES</span></span>

## <span data-ttu-id="acea2-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="acea2-142">RELATED LINKS</span></span>

