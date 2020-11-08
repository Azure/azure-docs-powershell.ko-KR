---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Consumption.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/new-azconsumptionbudget
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/New-AzConsumptionBudget.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/New-AzConsumptionBudget.md
ms.openlocfilehash: 1b6e815a8ccb02fe462393df8a91af9800b425df
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94204079"
---
# <span data-ttu-id="bb36a-101">New-AzConsumptionBudget</span><span class="sxs-lookup"><span data-stu-id="bb36a-101">New-AzConsumptionBudget</span></span>

## <span data-ttu-id="bb36a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bb36a-102">SYNOPSIS</span></span>
<span data-ttu-id="bb36a-103">구독 또는 리소스 그룹에서 예산을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="bb36a-103">Create a budget in either a subscription or a resource group.</span></span>

## <span data-ttu-id="bb36a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="bb36a-104">SYNTAX</span></span>

### <span data-ttu-id="bb36a-105">구독 (기본값)</span><span class="sxs-lookup"><span data-stu-id="bb36a-105">Subscription (Default)</span></span>
```
New-AzConsumptionBudget [-DefaultProfile <IAzureContextContainer>] -Name <String> -Amount <Decimal>
 -Category <String> -TimeGrain <String> -StartDate <DateTime> [-EndDate <DateTime>]
 [-ResourceGroupName <String>] [-MeterFilter <String[]>] [-ResourceFilter <String[]>]
 [-ResourceGroupFilter <String[]>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bb36a-106">메시지</span><span class="sxs-lookup"><span data-stu-id="bb36a-106">Notification</span></span>
```
New-AzConsumptionBudget [-DefaultProfile <IAzureContextContainer>] -Name <String> -Amount <Decimal>
 -Category <String> -TimeGrain <String> -StartDate <DateTime> [-EndDate <DateTime>]
 [-ResourceGroupName <String>] [-MeterFilter <String[]>] [-ResourceFilter <String[]>]
 [-ResourceGroupFilter <String[]>] -NotificationKey <String> [-NotificationEnabled]
 -NotificationThreshold <Decimal> -ContactEmail <String[]> [-ContactGroup <String[]>] [-ContactRole <String[]>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bb36a-107">설명은</span><span class="sxs-lookup"><span data-stu-id="bb36a-107">DESCRIPTION</span></span>
<span data-ttu-id="bb36a-108">New-AzConsumptionBudget cmdlet은 구독 또는 리소스 그룹에 예산을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="bb36a-108">The New-AzConsumptionBudget cmdlet creates a budget in either a subscription or a resource group.</span></span>

## <span data-ttu-id="bb36a-109">예제의</span><span class="sxs-lookup"><span data-stu-id="bb36a-109">EXAMPLES</span></span>

### <span data-ttu-id="bb36a-110">예제 1: 구독 수준에서 예산 이름으로 비용 예산 만들기</span><span class="sxs-lookup"><span data-stu-id="bb36a-110">Example 1: Create a cost budget with a budget name at subscription level</span></span>
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

### <span data-ttu-id="bb36a-111">예제 2: 자원 그룹 수준에서 예산 이름으로 비용 예산 만들기</span><span class="sxs-lookup"><span data-stu-id="bb36a-111">Example 2: Create a cost budget with a budget name at resource group level</span></span>
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

## <span data-ttu-id="bb36a-112">변수</span><span class="sxs-lookup"><span data-stu-id="bb36a-112">PARAMETERS</span></span>

### <span data-ttu-id="bb36a-113">-금액</span><span class="sxs-lookup"><span data-stu-id="bb36a-113">-Amount</span></span>
<span data-ttu-id="bb36a-114">예산 금액입니다.</span><span class="sxs-lookup"><span data-stu-id="bb36a-114">Amount of a budget.</span></span>

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

### <span data-ttu-id="bb36a-115">-범주</span><span class="sxs-lookup"><span data-stu-id="bb36a-115">-Category</span></span>
<span data-ttu-id="bb36a-116">예산 범주는 비용 또는 사용 현황 일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bb36a-116">Category of the budget can be cost or usage.</span></span>

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

### <span data-ttu-id="bb36a-117">-ContactEmail</span><span class="sxs-lookup"><span data-stu-id="bb36a-117">-ContactEmail</span></span>
<span data-ttu-id="bb36a-118">임계값이 초과 되는 경우 예산 알림을 보내는 전자 메일 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="bb36a-118">Email addresses to send the budget notification to when the threshold is exceeded.</span></span>

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

### <span data-ttu-id="bb36a-119">-연락처 그룹</span><span class="sxs-lookup"><span data-stu-id="bb36a-119">-ContactGroup</span></span>
<span data-ttu-id="bb36a-120">작업 그룹-임계값이 초과 되는 경우 예산 알림을 보냅니다.</span><span class="sxs-lookup"><span data-stu-id="bb36a-120">Action groups to send the budget notification to when the threshold is exceeded.</span></span>

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

### <span data-ttu-id="bb36a-121">-연락처 역할</span><span class="sxs-lookup"><span data-stu-id="bb36a-121">-ContactRole</span></span>
<span data-ttu-id="bb36a-122">대화 상대 역할-임계값을 초과한 시간에 예산 알림을 보냅니다.</span><span class="sxs-lookup"><span data-stu-id="bb36a-122">Contact roles to send the budget notification to when the threshold is exceeded.</span></span>

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

### <span data-ttu-id="bb36a-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb36a-123">-DefaultProfile</span></span>
<span data-ttu-id="bb36a-124">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="bb36a-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bb36a-125">-EndDate</span><span class="sxs-lookup"><span data-stu-id="bb36a-125">-EndDate</span></span>
<span data-ttu-id="bb36a-126">예산에 대 한 기간에 대 한 종료 날짜 (UTC의 YYYY-MM-DD)</span><span class="sxs-lookup"><span data-stu-id="bb36a-126">End date (YYYY-MM-DD in UTC) of time period of a budget.</span></span>

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

### <span data-ttu-id="bb36a-127">-MeterFilter</span><span class="sxs-lookup"><span data-stu-id="bb36a-127">-MeterFilter</span></span>
<span data-ttu-id="bb36a-128">필터링 할 미터의 쉼표로 구분 된 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="bb36a-128">Comma-separated list of meters to filter on.</span></span>
<span data-ttu-id="bb36a-129">범주가 사용 인 경우 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="bb36a-129">Required if category is usage.</span></span>

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

### <span data-ttu-id="bb36a-130">-이름</span><span class="sxs-lookup"><span data-stu-id="bb36a-130">-Name</span></span>
<span data-ttu-id="bb36a-131">예산 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bb36a-131">Name of a budget.</span></span>

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

### <span data-ttu-id="bb36a-132">-NotificationEnabled</span><span class="sxs-lookup"><span data-stu-id="bb36a-132">-NotificationEnabled</span></span>
<span data-ttu-id="bb36a-133">알림을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bb36a-133">The notification is enabled or not.</span></span>

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

### <span data-ttu-id="bb36a-134">-NotificationKey</span><span class="sxs-lookup"><span data-stu-id="bb36a-134">-NotificationKey</span></span>
<span data-ttu-id="bb36a-135">예산과 관련 된 알림의 키로, 알림 사용 가능 전환, 알림 임계값, 연락처 전자 메일, 연락처 그룹 또는 연락처 역할에 대 한 알림을 만드는 데 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="bb36a-135">Key of a notification associated with a budget, required to create a notification with notification enabled switch, notification threshold, contact emails, contact groups, or contact roles.</span></span>

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

### <span data-ttu-id="bb36a-136">-NotificationThreshold</span><span class="sxs-lookup"><span data-stu-id="bb36a-136">-NotificationThreshold</span></span>
<span data-ttu-id="bb36a-137">알림과 관련 된 임계값 값입니다.</span><span class="sxs-lookup"><span data-stu-id="bb36a-137">Threshold value associated with a notification.</span></span>
<span data-ttu-id="bb36a-138">요금 또는 사용량이 임계값을 초과한 경우 알림이 전송 됩니다.</span><span class="sxs-lookup"><span data-stu-id="bb36a-138">Notification is sent when the cost or usage exceeded the threshold.</span></span>
<span data-ttu-id="bb36a-139">항상 백분율이 며 0과 1000 사이 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="bb36a-139">It is always percent and has to be between 0 and 1000.</span></span>

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

### <span data-ttu-id="bb36a-140">-ResourceFilter</span><span class="sxs-lookup"><span data-stu-id="bb36a-140">-ResourceFilter</span></span>
<span data-ttu-id="bb36a-141">필터링 할 리소스 인스턴스의 쉼표로 구분 된 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="bb36a-141">Comma-separated list of resource instances to filter on.</span></span>

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

### <span data-ttu-id="bb36a-142">-ResourceGroupFilter</span><span class="sxs-lookup"><span data-stu-id="bb36a-142">-ResourceGroupFilter</span></span>
<span data-ttu-id="bb36a-143">필터링 할 리소스 그룹의 쉼표로 구분 된 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="bb36a-143">Comma-separated list of resource groups to filter on.</span></span>

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

### <span data-ttu-id="bb36a-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bb36a-144">-ResourceGroupName</span></span>
<span data-ttu-id="bb36a-145">예산에 대 한 자원 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="bb36a-145">Resource Group of a budget.</span></span>

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

### <span data-ttu-id="bb36a-146">-시작 날짜</span><span class="sxs-lookup"><span data-stu-id="bb36a-146">-StartDate</span></span>
<span data-ttu-id="bb36a-147">예산에 대 한 기간에 대 한 시작 날짜 (UTC의 YYYY-MM-DD 단위)입니다.</span><span class="sxs-lookup"><span data-stu-id="bb36a-147">Start date (YYYY-MM-DD in UTC) of time period of a budget.</span></span>
<span data-ttu-id="bb36a-148">월간 시간 세분화에는 현재 달 이전이 아닙니다.</span><span class="sxs-lookup"><span data-stu-id="bb36a-148">Not prior to current month for monthly time grain.</span></span>
<span data-ttu-id="bb36a-149">분기별 시간 세분화의 경우 3 개월 전</span><span class="sxs-lookup"><span data-stu-id="bb36a-149">Not prior to three months for quarterly time grain.</span></span>
<span data-ttu-id="bb36a-150">연간 시간 세분화에는 12 개월 이전이 아닙니다.</span><span class="sxs-lookup"><span data-stu-id="bb36a-150">Not prior to twelve months for yearly time grain.</span></span>
<span data-ttu-id="bb36a-151">이후 시작 날짜는 3 개월을 초과할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="bb36a-151">Future start date not more than three months.</span></span>

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

### <span data-ttu-id="bb36a-152">-TimeGrain</span><span class="sxs-lookup"><span data-stu-id="bb36a-152">-TimeGrain</span></span>
<span data-ttu-id="bb36a-153">예산에 대 한 시간 세분화는 월별, 분기별 또는 매년 일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bb36a-153">Time grain of the budget can be monthly, quarterly, or annually.</span></span>

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

### <span data-ttu-id="bb36a-154">-확인</span><span class="sxs-lookup"><span data-stu-id="bb36a-154">-Confirm</span></span>
<span data-ttu-id="bb36a-155">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="bb36a-155">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bb36a-156">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bb36a-156">-WhatIf</span></span>
<span data-ttu-id="bb36a-157">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="bb36a-157">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bb36a-158">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="bb36a-158">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bb36a-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb36a-159">CommonParameters</span></span>
<span data-ttu-id="bb36a-160">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="bb36a-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb36a-161">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bb36a-161">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb36a-162">입력</span><span class="sxs-lookup"><span data-stu-id="bb36a-162">INPUTS</span></span>

### <span data-ttu-id="bb36a-163">않아야</span><span class="sxs-lookup"><span data-stu-id="bb36a-163">None</span></span>

## <span data-ttu-id="bb36a-164">출력</span><span class="sxs-lookup"><span data-stu-id="bb36a-164">OUTPUTS</span></span>

### <span data-ttu-id="bb36a-165">Microsoft. a. 모든 모델에 대 한 PSBudget</span><span class="sxs-lookup"><span data-stu-id="bb36a-165">Microsoft.Azure.Commands.Consumption.Models.PSBudget</span></span>

## <span data-ttu-id="bb36a-166">상속자</span><span class="sxs-lookup"><span data-stu-id="bb36a-166">NOTES</span></span>

## <span data-ttu-id="bb36a-167">관련 링크</span><span class="sxs-lookup"><span data-stu-id="bb36a-167">RELATED LINKS</span></span>
