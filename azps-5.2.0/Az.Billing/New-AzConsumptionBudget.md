---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Consumption.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/new-azconsumptionbudget
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/New-AzConsumptionBudget.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/New-AzConsumptionBudget.md
ms.openlocfilehash: 1b6e815a8ccb02fe462393df8a91af9800b425df
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98344781"
---
# <span data-ttu-id="548ab-101">New-AzConsumptionBudget</span><span class="sxs-lookup"><span data-stu-id="548ab-101">New-AzConsumptionBudget</span></span>

## <span data-ttu-id="548ab-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="548ab-102">SYNOPSIS</span></span>
<span data-ttu-id="548ab-103">구독 또는 리소스 그룹에서 예산을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="548ab-103">Create a budget in either a subscription or a resource group.</span></span>

## <span data-ttu-id="548ab-104">구문</span><span class="sxs-lookup"><span data-stu-id="548ab-104">SYNTAX</span></span>

### <span data-ttu-id="548ab-105">구독(기본값)</span><span class="sxs-lookup"><span data-stu-id="548ab-105">Subscription (Default)</span></span>
```
New-AzConsumptionBudget [-DefaultProfile <IAzureContextContainer>] -Name <String> -Amount <Decimal>
 -Category <String> -TimeGrain <String> -StartDate <DateTime> [-EndDate <DateTime>]
 [-ResourceGroupName <String>] [-MeterFilter <String[]>] [-ResourceFilter <String[]>]
 [-ResourceGroupFilter <String[]>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="548ab-106">알림</span><span class="sxs-lookup"><span data-stu-id="548ab-106">Notification</span></span>
```
New-AzConsumptionBudget [-DefaultProfile <IAzureContextContainer>] -Name <String> -Amount <Decimal>
 -Category <String> -TimeGrain <String> -StartDate <DateTime> [-EndDate <DateTime>]
 [-ResourceGroupName <String>] [-MeterFilter <String[]>] [-ResourceFilter <String[]>]
 [-ResourceGroupFilter <String[]>] -NotificationKey <String> [-NotificationEnabled]
 -NotificationThreshold <Decimal> -ContactEmail <String[]> [-ContactGroup <String[]>] [-ContactRole <String[]>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="548ab-107">설명</span><span class="sxs-lookup"><span data-stu-id="548ab-107">DESCRIPTION</span></span>
<span data-ttu-id="548ab-108">New-AzConsumptionBudget cmdlet은 구독 또는 리소스 그룹에 예산을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="548ab-108">The New-AzConsumptionBudget cmdlet creates a budget in either a subscription or a resource group.</span></span>

## <span data-ttu-id="548ab-109">예제</span><span class="sxs-lookup"><span data-stu-id="548ab-109">EXAMPLES</span></span>

### <span data-ttu-id="548ab-110">예제 1: 구독 수준에서 예산 이름을 사용하여 비용 예산 만들기</span><span class="sxs-lookup"><span data-stu-id="548ab-110">Example 1: Create a cost budget with a budget name at subscription level</span></span>
```powershell
PS C:\> New-AzConsumptionBudget -Amount 60 -Name PSBudget -Category Cost -StartDate 2018-06-01 -EndDate 2018-11-01 -TimeGrain Monthly
Amount:  60     
Category:  Cost
CurrentSpend:  null
Id:  subscriptions/1caaa5a3-2b66-438e-8ab4-bce37d518c5d/providers/Microsoft.Consumption/budgets/PSBudget
Name:  PSBudget
TimeGrain:  Monthly
TimePeriod:  EndDate:  11/1/2018 12:00:00 AM
             StartDate:  6/1/2018 12:00:00 AM
Type:  Microsoft.Consumption/budgets
```

### <span data-ttu-id="548ab-111">예제 2: 리소스 그룹 수준에서 예산 이름을 사용하여 비용 예산 만들기</span><span class="sxs-lookup"><span data-stu-id="548ab-111">Example 2: Create a cost budget with a budget name at resource group level</span></span>
```powershell
PS C:\> New-AzConsumptionBudget -ResourceGroupName RGBudgets -Amount 60 -Name PSBudgetRG -Category Cost -StartDate 2018-06-01 -EndDate 2018-11-01 -TimeGrain Monthly
Amount:  60     
Category:  Cost
CurrentSpend:  null
Id:  subscriptions/1caaa5a3-2b66-438e-8ab4-bce37d518c5d/resourceGroups/RGBudgets/providers/Microsoft.Consumption/budgets/PSBudgetRG
Name:  PSBudgetRG
TimeGrain:  Monthly
TimePeriod:  EndDate:  11/1/2018 12:00:00 AM
             StartDate:  6/1/2018 12:00:00 AM
Type:  Microsoft.Consumption/budgets
```

## <span data-ttu-id="548ab-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="548ab-112">PARAMETERS</span></span>

### <span data-ttu-id="548ab-113">-Amount</span><span class="sxs-lookup"><span data-stu-id="548ab-113">-Amount</span></span>
<span data-ttu-id="548ab-114">예산의 양입니다.</span><span class="sxs-lookup"><span data-stu-id="548ab-114">Amount of a budget.</span></span>

```yaml
Type: System.Decimal
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="548ab-115">-Category</span><span class="sxs-lookup"><span data-stu-id="548ab-115">-Category</span></span>
<span data-ttu-id="548ab-116">예산의 범주는 비용 또는 사용량일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="548ab-116">Category of the budget can be cost or usage.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Cost, Usage

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="548ab-117">-ContactEmail</span><span class="sxs-lookup"><span data-stu-id="548ab-117">-ContactEmail</span></span>
<span data-ttu-id="548ab-118">임계값을 초과할 때 예산 알림을 보낼 전자 메일 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="548ab-118">Email addresses to send the budget notification to when the threshold is exceeded.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Notification
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="548ab-119">-ContactGroup</span><span class="sxs-lookup"><span data-stu-id="548ab-119">-ContactGroup</span></span>
<span data-ttu-id="548ab-120">임계값을 초과할 때 예산 알림을 보내는 작업 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="548ab-120">Action groups to send the budget notification to when the threshold is exceeded.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Notification
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="548ab-121">-ContactRole</span><span class="sxs-lookup"><span data-stu-id="548ab-121">-ContactRole</span></span>
<span data-ttu-id="548ab-122">임계값을 초과하는 경우 예산 알림을 보내기 위해 역할에 문의합니다.</span><span class="sxs-lookup"><span data-stu-id="548ab-122">Contact roles to send the budget notification to when the threshold is exceeded.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Notification
Aliases:
Accepted values: Owner, Reader, Contributor

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="548ab-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="548ab-123">-DefaultProfile</span></span>
<span data-ttu-id="548ab-124">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="548ab-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="548ab-125">-EndDate</span><span class="sxs-lookup"><span data-stu-id="548ab-125">-EndDate</span></span>
<span data-ttu-id="548ab-126">예산 기간의 종료 날짜(YYYY-MM-DD(UTC)입니다.</span><span class="sxs-lookup"><span data-stu-id="548ab-126">End date (YYYY-MM-DD in UTC) of time period of a budget.</span></span>

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

### <span data-ttu-id="548ab-127">-MeterFilter</span><span class="sxs-lookup"><span data-stu-id="548ab-127">-MeterFilter</span></span>
<span data-ttu-id="548ab-128">필터링할 콤마로 구분된 미터 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="548ab-128">Comma-separated list of meters to filter on.</span></span>
<span data-ttu-id="548ab-129">범주가 사용량인 경우 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="548ab-129">Required if category is usage.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="548ab-130">-Name</span><span class="sxs-lookup"><span data-stu-id="548ab-130">-Name</span></span>
<span data-ttu-id="548ab-131">예산의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="548ab-131">Name of a budget.</span></span>

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

### <span data-ttu-id="548ab-132">-NotificationEnabled</span><span class="sxs-lookup"><span data-stu-id="548ab-132">-NotificationEnabled</span></span>
<span data-ttu-id="548ab-133">알림이 사용하도록 설정되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="548ab-133">The notification is enabled or not.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Notification
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="548ab-134">-NotificationKey</span><span class="sxs-lookup"><span data-stu-id="548ab-134">-NotificationKey</span></span>
<span data-ttu-id="548ab-135">예산과 연결된 알림의 키로, 알림 사용 스위치, 알림 임계값, 연락처 전자 메일, 연락처 그룹 또는 연락처 역할로 알림을 만드는 데 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="548ab-135">Key of a notification associated with a budget, required to create a notification with notification enabled switch, notification threshold, contact emails, contact groups, or contact roles.</span></span>

```yaml
Type: System.String
Parameter Sets: Notification
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="548ab-136">-NotificationThreshold</span><span class="sxs-lookup"><span data-stu-id="548ab-136">-NotificationThreshold</span></span>
<span data-ttu-id="548ab-137">알림과 연결된 임계값입니다.</span><span class="sxs-lookup"><span data-stu-id="548ab-137">Threshold value associated with a notification.</span></span>
<span data-ttu-id="548ab-138">비용 또는 사용량이 임계값을 초과하면 알림이 전송됩니다.</span><span class="sxs-lookup"><span data-stu-id="548ab-138">Notification is sent when the cost or usage exceeded the threshold.</span></span>
<span data-ttu-id="548ab-139">항상 백분율로, 0~1000 사이가 됐습니다.</span><span class="sxs-lookup"><span data-stu-id="548ab-139">It is always percent and has to be between 0 and 1000.</span></span>

```yaml
Type: System.Nullable`1[System.Decimal]
Parameter Sets: Notification
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="548ab-140">-ResourceFilter</span><span class="sxs-lookup"><span data-stu-id="548ab-140">-ResourceFilter</span></span>
<span data-ttu-id="548ab-141">필터링할 리소스 인스턴스의 콤마로 구분된 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="548ab-141">Comma-separated list of resource instances to filter on.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="548ab-142">-ResourceGroupFilter</span><span class="sxs-lookup"><span data-stu-id="548ab-142">-ResourceGroupFilter</span></span>
<span data-ttu-id="548ab-143">필터링할 리소스 그룹의 콤마로 구분된 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="548ab-143">Comma-separated list of resource groups to filter on.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="548ab-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="548ab-144">-ResourceGroupName</span></span>
<span data-ttu-id="548ab-145">예산의 리소스 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="548ab-145">Resource Group of a budget.</span></span>

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

### <span data-ttu-id="548ab-146">-StartDate</span><span class="sxs-lookup"><span data-stu-id="548ab-146">-StartDate</span></span>
<span data-ttu-id="548ab-147">예산 기간의 시작 날짜(YYYY-MM-DD(UTC)입니다.</span><span class="sxs-lookup"><span data-stu-id="548ab-147">Start date (YYYY-MM-DD in UTC) of time period of a budget.</span></span>
<span data-ttu-id="548ab-148">월별 시간(월별 시간)에 대해 현재 월 이전이 아 않습니다.</span><span class="sxs-lookup"><span data-stu-id="548ab-148">Not prior to current month for monthly time grain.</span></span>
<span data-ttu-id="548ab-149">분기별 시간 세분화의 경우 3개월 이전이 아 않습니다.</span><span class="sxs-lookup"><span data-stu-id="548ab-149">Not prior to three months for quarterly time grain.</span></span>
<span data-ttu-id="548ab-150">연별 시간 세분화의 경우 12개월 전이 아니어도 됩니다.</span><span class="sxs-lookup"><span data-stu-id="548ab-150">Not prior to twelve months for yearly time grain.</span></span>
<span data-ttu-id="548ab-151">향후 시작 날짜는 3개월을 넘지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="548ab-151">Future start date not more than three months.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="548ab-152">-TimeGrain</span><span class="sxs-lookup"><span data-stu-id="548ab-152">-TimeGrain</span></span>
<span data-ttu-id="548ab-153">예산의 시간 세분화는 월별, 분기별 또는 연간일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="548ab-153">Time grain of the budget can be monthly, quarterly, or annually.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Monthly, Quarterly, Annually

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="548ab-154">-Confirm</span><span class="sxs-lookup"><span data-stu-id="548ab-154">-Confirm</span></span>
<span data-ttu-id="548ab-155">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="548ab-155">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="548ab-156">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="548ab-156">-WhatIf</span></span>
<span data-ttu-id="548ab-157">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="548ab-157">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="548ab-158">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="548ab-158">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="548ab-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="548ab-159">CommonParameters</span></span>
<span data-ttu-id="548ab-160">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="548ab-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="548ab-161">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="548ab-161">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="548ab-162">입력</span><span class="sxs-lookup"><span data-stu-id="548ab-162">INPUTS</span></span>

### <span data-ttu-id="548ab-163">없음</span><span class="sxs-lookup"><span data-stu-id="548ab-163">None</span></span>

## <span data-ttu-id="548ab-164">출력</span><span class="sxs-lookup"><span data-stu-id="548ab-164">OUTPUTS</span></span>

### <span data-ttu-id="548ab-165">Microsoft.Azure.Commands.Consumption.Models.PSBudget</span><span class="sxs-lookup"><span data-stu-id="548ab-165">Microsoft.Azure.Commands.Consumption.Models.PSBudget</span></span>

## <span data-ttu-id="548ab-166">참고 사항</span><span class="sxs-lookup"><span data-stu-id="548ab-166">NOTES</span></span>

## <span data-ttu-id="548ab-167">관련 링크</span><span class="sxs-lookup"><span data-stu-id="548ab-167">RELATED LINKS</span></span>
