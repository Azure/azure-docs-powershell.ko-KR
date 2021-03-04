---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Consumption.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/powershell/module/az.billing/get-azconsumptionusagedetail
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzConsumptionUsageDetail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzConsumptionUsageDetail.md
ms.openlocfilehash: 4c355565936a7aefc8d0adc9b9ee865a2414e880
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101952832"
---
# <span data-ttu-id="eb68d-101">Get-AzConsumptionUsageDetail</span><span class="sxs-lookup"><span data-stu-id="eb68d-101">Get-AzConsumptionUsageDetail</span></span>

## <span data-ttu-id="eb68d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eb68d-102">SYNOPSIS</span></span>
<span data-ttu-id="eb68d-103">구독의 사용 현황 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="eb68d-103">Get usage details of the subscription.</span></span>

## <span data-ttu-id="eb68d-104">구문</span><span class="sxs-lookup"><span data-stu-id="eb68d-104">SYNTAX</span></span>

```
Get-AzConsumptionUsageDetail [-BillingPeriodName <String>] [-Expand <String>] [-IncludeMeterDetails]
 [-IncludeAdditionalProperties] [-StartDate <DateTime>] [-EndDate <DateTime>] [-ResourceGroup <String>]
 [-InstanceName <String>] [-InstanceId <String>] [-Tag <String>] [-MaxCount <Int32>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="eb68d-105">설명</span><span class="sxs-lookup"><span data-stu-id="eb68d-105">DESCRIPTION</span></span>
<span data-ttu-id="eb68d-106">**Get-AzConsumptionUsageDetail** cmdlet은 구독의 사용 세부 정보를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="eb68d-106">The **Get-AzConsumptionUsageDetail** cmdlet gets usage details of the subscription.</span></span> 

## <span data-ttu-id="eb68d-107">예제</span><span class="sxs-lookup"><span data-stu-id="eb68d-107">EXAMPLES</span></span>

### <span data-ttu-id="eb68d-108">예제 1: MeterDetails의 확장을 통해 사용 세부 정보 확인</span><span class="sxs-lookup"><span data-stu-id="eb68d-108">Example 1: Get usage details with expand of MeterDetails</span></span>
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

### <span data-ttu-id="eb68d-109">예제 2: 날짜 범위가 있는 사용 현황 정보 확인</span><span class="sxs-lookup"><span data-stu-id="eb68d-109">Example 2: Get usage details with date range</span></span>
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

### <span data-ttu-id="eb68d-110">예제 3: InstanceName 필터를 사용하여 BillingPeriodName의 사용 세부 정보 확인</span><span class="sxs-lookup"><span data-stu-id="eb68d-110">Example 3: Get usage details of BillingPeriodName with InstanceName filter</span></span>
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

## <span data-ttu-id="eb68d-111">매개 변수</span><span class="sxs-lookup"><span data-stu-id="eb68d-111">PARAMETERS</span></span>

### <span data-ttu-id="eb68d-112">-BillingPeriodName</span><span class="sxs-lookup"><span data-stu-id="eb68d-112">-BillingPeriodName</span></span>
<span data-ttu-id="eb68d-113">연결된 사용량 세부 정보를 얻을 수 있는 특정 청구 기간의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="eb68d-113">Name of a specific billing period to get the usage details that associate with.</span></span>

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

### <span data-ttu-id="eb68d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb68d-114">-DefaultProfile</span></span>
<span data-ttu-id="eb68d-115">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="eb68d-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eb68d-116">-EndDate</span><span class="sxs-lookup"><span data-stu-id="eb68d-116">-EndDate</span></span>
<span data-ttu-id="eb68d-117">필터링할 사용량의 종료 날짜(UTC)입니다.</span><span class="sxs-lookup"><span data-stu-id="eb68d-117">The end date (in UTC) of the usages to filter.</span></span>

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

### <span data-ttu-id="eb68d-118">-확장</span><span class="sxs-lookup"><span data-stu-id="eb68d-118">-Expand</span></span>
<span data-ttu-id="eb68d-119">MeterDetails 또는 AdditionalInfo를 기반으로 사용량을 확장합니다.</span><span class="sxs-lookup"><span data-stu-id="eb68d-119">Expand the usages based on MeterDetails, or AdditionalInfo.</span></span>

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

### <span data-ttu-id="eb68d-120">-IncludeAdditionalProperties</span><span class="sxs-lookup"><span data-stu-id="eb68d-120">-IncludeAdditionalProperties</span></span>
<span data-ttu-id="eb68d-121">사용법에 추가 속성을 포함합니다.</span><span class="sxs-lookup"><span data-stu-id="eb68d-121">Include additional properties in the usages.</span></span>

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

### <span data-ttu-id="eb68d-122">-IncludeMeterDetails</span><span class="sxs-lookup"><span data-stu-id="eb68d-122">-IncludeMeterDetails</span></span>
<span data-ttu-id="eb68d-123">사용량에 미터 세부 정보를 포함합니다.</span><span class="sxs-lookup"><span data-stu-id="eb68d-123">Include meter details in the usages.</span></span>

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

### <span data-ttu-id="eb68d-124">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="eb68d-124">-InstanceId</span></span>
<span data-ttu-id="eb68d-125">필터링할 사용량의 인스턴스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="eb68d-125">The instance id of the usages to filter.</span></span>

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

### <span data-ttu-id="eb68d-126">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="eb68d-126">-InstanceName</span></span>
<span data-ttu-id="eb68d-127">필터링할 사용량의 인스턴스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="eb68d-127">The instance name of the usages to filter.</span></span>

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

### <span data-ttu-id="eb68d-128">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="eb68d-128">-MaxCount</span></span>
<span data-ttu-id="eb68d-129">반환할 레코드의 최대 수를 결정합니다.</span><span class="sxs-lookup"><span data-stu-id="eb68d-129">Determine the maximum number of records to return.</span></span>

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

### <span data-ttu-id="eb68d-130">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="eb68d-130">-ResourceGroup</span></span>
<span data-ttu-id="eb68d-131">필터링할 사용량의 리소스 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="eb68d-131">The resource group of the usages to filter.</span></span>

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

### <span data-ttu-id="eb68d-132">-StartDate</span><span class="sxs-lookup"><span data-stu-id="eb68d-132">-StartDate</span></span>
<span data-ttu-id="eb68d-133">필터링할 사용량의 시작 날짜(UTC)입니다.</span><span class="sxs-lookup"><span data-stu-id="eb68d-133">The start date (in UTC) of the usages to filter.</span></span>

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

### <span data-ttu-id="eb68d-134">-Tag</span><span class="sxs-lookup"><span data-stu-id="eb68d-134">-Tag</span></span>
<span data-ttu-id="eb68d-135">필터링할 사용량의 태그입니다.</span><span class="sxs-lookup"><span data-stu-id="eb68d-135">The tag of the usages to filter.</span></span>

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

### <span data-ttu-id="eb68d-136">-Top</span><span class="sxs-lookup"><span data-stu-id="eb68d-136">-Top</span></span>
<span data-ttu-id="eb68d-137">반환할 레코드의 최대 수를 결정합니다.</span><span class="sxs-lookup"><span data-stu-id="eb68d-137">Determine the maximum number of records to return.</span></span>

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

### <span data-ttu-id="eb68d-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb68d-138">CommonParameters</span></span>
<span data-ttu-id="eb68d-139">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="eb68d-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb68d-140">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="eb68d-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb68d-141">입력</span><span class="sxs-lookup"><span data-stu-id="eb68d-141">INPUTS</span></span>

### <span data-ttu-id="eb68d-142">없음</span><span class="sxs-lookup"><span data-stu-id="eb68d-142">None</span></span>

## <span data-ttu-id="eb68d-143">출력</span><span class="sxs-lookup"><span data-stu-id="eb68d-143">OUTPUTS</span></span>

### <span data-ttu-id="eb68d-144">Microsoft.Azure.Commands.Consumption.Models.PSUsageDetail</span><span class="sxs-lookup"><span data-stu-id="eb68d-144">Microsoft.Azure.Commands.Consumption.Models.PSUsageDetail</span></span>

## <span data-ttu-id="eb68d-145">참고 사항</span><span class="sxs-lookup"><span data-stu-id="eb68d-145">NOTES</span></span>

## <span data-ttu-id="eb68d-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="eb68d-146">RELATED LINKS</span></span>
