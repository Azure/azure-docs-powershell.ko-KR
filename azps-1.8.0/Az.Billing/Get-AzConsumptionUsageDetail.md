---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Consumption.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/get-azconsumptionusagedetail
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzConsumptionUsageDetail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzConsumptionUsageDetail.md
ms.openlocfilehash: 47794cc34f3d259a57f021a93c1b17250b3546f9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93869265"
---
# <span data-ttu-id="394c4-101">Get-AzConsumptionUsageDetail</span><span class="sxs-lookup"><span data-stu-id="394c4-101">Get-AzConsumptionUsageDetail</span></span>

## <span data-ttu-id="394c4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="394c4-102">SYNOPSIS</span></span>
<span data-ttu-id="394c4-103">구독에 대 한 사용 현황 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="394c4-103">Get usage details of the subscription.</span></span>

## <span data-ttu-id="394c4-104">구문과</span><span class="sxs-lookup"><span data-stu-id="394c4-104">SYNTAX</span></span>

```
Get-AzConsumptionUsageDetail [-BillingPeriodName <String>] [-Expand <String>] [-IncludeMeterDetails]
 [-IncludeAdditionalProperties] [-StartDate <DateTime>] [-EndDate <DateTime>] [-ResourceGroup <String>]
 [-InstanceName <String>] [-InstanceId <String>] [-Tag <String>] [-MaxCount <Int32>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="394c4-105">설명은</span><span class="sxs-lookup"><span data-stu-id="394c4-105">DESCRIPTION</span></span>
<span data-ttu-id="394c4-106">**AzConsumptionUsageDetail** cmdlet은 구독에 대 한 사용 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="394c4-106">The **Get-AzConsumptionUsageDetail** cmdlet gets usage details of the subscription.</span></span> 

## <span data-ttu-id="394c4-107">예제의</span><span class="sxs-lookup"><span data-stu-id="394c4-107">EXAMPLES</span></span>

### <span data-ttu-id="394c4-108">예제 1: MeterDetails 확장을 사용 하 여 사용 세부 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="394c4-108">Example 1: Get usage details with expand of MeterDetails</span></span>
```powershell
PS C:\> Get-AzConsumptionUsageDetail -Expand MeterDetails -Top 10
AccountName:  AAAA
BillingPeriodId:  subscriptions/1caaa5a3-2b66-438e-8ab4-bce37d518c5d/providers/Microsoft.Billing/billingPeriods/20180601
ConsumedService:  Microsoft.Compute
CostCenter:  XYZ987
Currency:  USD
DepartmentName:  Ama
Id:  subscriptions/1caaa5a3-2b66-438e-8ab4-bce37d518c5d/providers/Microsoft.Billing/billingPeriods/20180601/providers/Microsoft.Consumption/usageDetails/24b9dff0-f022-55a1-886b-17b330000db3
InstanceId:  subscriptions/1caaa5a3-2b66-438e-8ab4-bce37d518c5d/resourceGroups/MAR-CCM/providers/Microsoft.Compute/disks/mar-ccm-vm01_OsDisk_1_d0beead4b6ff4b4088a687701d355d61
InstanceLocation:  usnorthcentral
InstanceName:  mar-ccm-vm01_OsDisk_1_d0beead4b6ff4b4088a687701d355d61
IsEstimated:  true
MeterDetails:  MeterCategory:  Data Management
               MeterLocation:  usnorthcentral
               MeterName:  Standard Managed Disk Operations (in 10,000s)
               MeterSubCategory:  Data Management
               Unit:  Operations
MeterId:  82cd70ab-1aee-4b30-bc04-8b71e1204dbc
Name:  24b9dff0-f022-55a1-886b-17b330000db3
PretaxCost:  0
Product:  Data Management Standard Managed Disk Operations
SubscriptionGuid:  1caaa5a3-2b66-438e-8ab4-bce37d518c5d
SubscriptionName:  CCM - Microsoft Azure Enterprise - 1
Type:  Microsoft.Consumption/usageDetails
UsageEnd:  6/1/2018 11:59:59 PM
UsageQuantity:  3.8218
UsageStart:  6/1/2018 12:00:00 AM
```

### <span data-ttu-id="394c4-109">예제 2: 날짜 범위가 있는 사용 세부 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="394c4-109">Example 2: Get usage details with date range</span></span>
```powershell
PS C:\> Get-AzConsumptionUsageDetail -StartDate 2017-10-02 -EndDate 2017-10-05 -Top 10
AccountName:  AAAA
BillingPeriodId:  subscriptions/1caaa5a3-2b66-438e-8ab4-bce37d518c5d/providers/Microsoft.Billing/billingPeriods/20171001
ConsumedService:  Storage
CostCenter:  XYZ987
Currency:  USD
DepartmentName:  Ama
Id:  subscriptions/1caaa5a3-2b66-438e-8ab4-bce37d518c5d/providers/Microsoft.Billing/billingPeriods/20171001/providers/Microsoft.Consumption/usageDetails/732582e5-40ad-bb23-7a69-ca1ff7c8b004
InstanceId:  storsimplezc9q6r2t7f
InstanceLocation:  US West Central
InstanceName:  storsimplezc9q6r2t7f
IsEstimated:  false
MeterId:  ad22fac8-9da5-4577-8683-56ae94d39e42
Name:  732582e5-40ad-bb23-7a69-ca1ff7c8b004
PretaxCost:  0
Product:  Data Management Geo Redundant Standard IO - Table Write
SubscriptionGuid:  1caaa5a3-2b66-438e-8ab4-bce37d518c5d
SubscriptionName:  CCM - Microsoft Azure Enterprise - 1
Type:  Microsoft.Consumption/usageDetails
UsageEnd:  10/2/2017 11:59:59 PM
UsageQuantity:  0.0006
UsageStart:  10/2/2017 12:00:00 AM
```

### <span data-ttu-id="394c4-110">예제 3: InstanceName 필터를 사용 하 여 BillingPeriodName에 대 한 사용 세부 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="394c4-110">Example 3: Get usage details of BillingPeriodName with InstanceName filter</span></span>
```powershell
PS C:\> Get-AzConsumptionUsageDetail -BillingPeriodName 201710 -InstanceName 1c2052westus -Top 10
AccountName:  AAAA
BillingPeriodId:  subscriptions/1caaa5a3-2b66-438e-8ab4-bce37d518c5d/providers/Microsoft.Billing/billingPeriods/20171001
ConsumedService:  Microsoft.Storage
CostCenter:  XYZ987
Currency:  USD
DepartmentName:  Ama
Id:  subscriptions/1caaa5a3-2b66-438e-8ab4-bce37d518c5d/providers/Microsoft.Billing/billingPeriods/20171001/providers/Microsoft.Consumption/usageDetails/8abc8b65-e8f1-31e1-f02b-058a7572363f
InstanceId:  subscriptions/1caaa5a3-2b66-438e-8ab4-bce37d518c5d/resourceGroups/securitydata/providers/Microsoft.Storage/storageAccounts/1c2052westus
InstanceLocation:  uswest
InstanceName:  1c2052westus
IsEstimated:  false
MeterId:  9995d93a-7d35-4d3f-9c69-7a7fea447ef4
Name:  8abc8b65-e8f1-31e1-f02b-058a7572363f
PretaxCost:  0.000000693016692
Product:  Data Transfer Out - Zone 1
SubscriptionGuid:  1caaa5a3-2b66-438e-8ab4-bce37d518c5d
SubscriptionName:  CCM - Microsoft Azure Enterprise - 1
Type:  Microsoft.Consumption/usageDetails
UsageEnd:  10/1/2017 11:59:59 PM
UsageQuantity:  0.000009
UsageStart:  10/1/2017 12:00:00 AM
```

## <span data-ttu-id="394c4-111">변수</span><span class="sxs-lookup"><span data-stu-id="394c4-111">PARAMETERS</span></span>

### <span data-ttu-id="394c4-112">-BillingPeriodName</span><span class="sxs-lookup"><span data-stu-id="394c4-112">-BillingPeriodName</span></span>
<span data-ttu-id="394c4-113">와 연결 되는 사용 세부 정보를 가져올 특정 청구 기간의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="394c4-113">Name of a specific billing period to get the usage details that associate with.</span></span>

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

### <span data-ttu-id="394c4-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="394c4-114">-DefaultProfile</span></span>
<span data-ttu-id="394c4-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="394c4-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="394c4-116">-EndDate</span><span class="sxs-lookup"><span data-stu-id="394c4-116">-EndDate</span></span>
<span data-ttu-id="394c4-117">필터링 용도에 대 한 끝 날짜 (UTC)입니다.</span><span class="sxs-lookup"><span data-stu-id="394c4-117">The end date (in UTC) of the usages to filter.</span></span>

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

### <span data-ttu-id="394c4-118">-확장</span><span class="sxs-lookup"><span data-stu-id="394c4-118">-Expand</span></span>
<span data-ttu-id="394c4-119">MeterDetails 또는 AdditionalInfo를 기반으로 사용량을 확장 합니다.</span><span class="sxs-lookup"><span data-stu-id="394c4-119">Expand the usages based on MeterDetails, or AdditionalInfo.</span></span>

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

### <span data-ttu-id="394c4-120">-IncludeAdditionalProperties</span><span class="sxs-lookup"><span data-stu-id="394c4-120">-IncludeAdditionalProperties</span></span>
<span data-ttu-id="394c4-121">용도에 추가 속성을 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="394c4-121">Include additional properties in the usages.</span></span>

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

### <span data-ttu-id="394c4-122">-IncludeMeterDetails</span><span class="sxs-lookup"><span data-stu-id="394c4-122">-IncludeMeterDetails</span></span>
<span data-ttu-id="394c4-123">용도에 측정기 세부 정보를 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="394c4-123">Include meter details in the usages.</span></span>

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

### <span data-ttu-id="394c4-124">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="394c4-124">-InstanceId</span></span>
<span data-ttu-id="394c4-125">필터링 용도에 대 한 인스턴스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="394c4-125">The instance id of the usages to filter.</span></span>

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

### <span data-ttu-id="394c4-126">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="394c4-126">-InstanceName</span></span>
<span data-ttu-id="394c4-127">필터링 용도에 대 한 인스턴스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="394c4-127">The instance name of the usages to filter.</span></span>

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

### <span data-ttu-id="394c4-128">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="394c4-128">-MaxCount</span></span>
<span data-ttu-id="394c4-129">반환할 최대 레코드 수를 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="394c4-129">Determine the maximum number of records to return.</span></span>

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

### <span data-ttu-id="394c4-130">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="394c4-130">-ResourceGroup</span></span>
<span data-ttu-id="394c4-131">필터링 용도에 대 한 리소스 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="394c4-131">The resource group of the usages to filter.</span></span>

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

### <span data-ttu-id="394c4-132">-시작 날짜</span><span class="sxs-lookup"><span data-stu-id="394c4-132">-StartDate</span></span>
<span data-ttu-id="394c4-133">필터링 용도에 대 한 시작 날짜 (UTC)입니다.</span><span class="sxs-lookup"><span data-stu-id="394c4-133">The start date (in UTC) of the usages to filter.</span></span>

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

### <span data-ttu-id="394c4-134">태그</span><span class="sxs-lookup"><span data-stu-id="394c4-134">-Tag</span></span>
<span data-ttu-id="394c4-135">필터링 용도에 대 한 태그입니다.</span><span class="sxs-lookup"><span data-stu-id="394c4-135">The tag of the usages to filter.</span></span>

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

### <span data-ttu-id="394c4-136">-위쪽</span><span class="sxs-lookup"><span data-stu-id="394c4-136">-Top</span></span>
<span data-ttu-id="394c4-137">반환할 최대 레코드 수를 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="394c4-137">Determine the maximum number of records to return.</span></span>

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

### <span data-ttu-id="394c4-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="394c4-138">CommonParameters</span></span>
<span data-ttu-id="394c4-139">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="394c4-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="394c4-140">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="394c4-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="394c4-141">입력</span><span class="sxs-lookup"><span data-stu-id="394c4-141">INPUTS</span></span>

### <span data-ttu-id="394c4-142">않아야</span><span class="sxs-lookup"><span data-stu-id="394c4-142">None</span></span>

## <span data-ttu-id="394c4-143">출력</span><span class="sxs-lookup"><span data-stu-id="394c4-143">OUTPUTS</span></span>

### <span data-ttu-id="394c4-144">PSUsageDetail를 사용 하 여 명령을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="394c4-144">Microsoft.Azure.Commands.Consumption.Models.PSUsageDetail</span></span>

## <span data-ttu-id="394c4-145">상속자</span><span class="sxs-lookup"><span data-stu-id="394c4-145">NOTES</span></span>

## <span data-ttu-id="394c4-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="394c4-146">RELATED LINKS</span></span>
