---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Consumption.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/set-azconsumptionbudget
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Set-AzConsumptionBudget.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Set-AzConsumptionBudget.md
ms.openlocfilehash: 89d628790297bfb677dab11f0b19ba525d8b9e47
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98494036"
---
# <span data-ttu-id="1f3a4-101">Set-AzConsumptionBudget</span><span class="sxs-lookup"><span data-stu-id="1f3a4-101">Set-AzConsumptionBudget</span></span>

## <span data-ttu-id="1f3a4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1f3a4-102">SYNOPSIS</span></span>
<span data-ttu-id="1f3a4-103">구독 또는 리소스 그룹에서 예산을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="1f3a4-103">Update a budget in either a subscription or a resource group.</span></span>

## <span data-ttu-id="1f3a4-104">구문</span><span class="sxs-lookup"><span data-stu-id="1f3a4-104">SYNTAX</span></span>

### <span data-ttu-id="1f3a4-105">구독(기본값)</span><span class="sxs-lookup"><span data-stu-id="1f3a4-105">Subscription (Default)</span></span>
```
Set-AzConsumptionBudget [-DefaultProfile <IAzureContextContainer>] -Name <String> [-Amount <Decimal>]
 [-Category <String>] [-TimeGrain <String>] [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-ResourceGroupName <String>] [-MeterFilter <String[]>] [-ResourceFilter <String[]>]
 [-ResourceGroupFilter <String[]>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1f3a4-106">알림</span><span class="sxs-lookup"><span data-stu-id="1f3a4-106">Notification</span></span>
```
Set-AzConsumptionBudget [-DefaultProfile <IAzureContextContainer>] -Name <String> [-Amount <Decimal>]
 [-Category <String>] [-TimeGrain <String>] [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-ResourceGroupName <String>] [-MeterFilter <String[]>] [-ResourceFilter <String[]>]
 [-ResourceGroupFilter <String[]>] -NotificationKey <String> [-NotificationEnabled]
 [-NotificationThreshold <Decimal>] [-ContactEmail <String[]>] [-ContactGroup <String[]>]
 [-ContactRole <String[]>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1f3a4-107">파이핑</span><span class="sxs-lookup"><span data-stu-id="1f3a4-107">Piping</span></span>
```
Set-AzConsumptionBudget [-DefaultProfile <IAzureContextContainer>] -InputObject <PSBudget> [-Amount <Decimal>]
 [-Category <String>] [-TimeGrain <String>] [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-MeterFilter <String[]>] [-ResourceFilter <String[]>] [-ResourceGroupFilter <String[]>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1f3a4-108">파이핑 및 알림</span><span class="sxs-lookup"><span data-stu-id="1f3a4-108">Piping and Notification</span></span>
```
Set-AzConsumptionBudget [-DefaultProfile <IAzureContextContainer>] -InputObject <PSBudget> [-Amount <Decimal>]
 [-Category <String>] [-TimeGrain <String>] [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-MeterFilter <String[]>] [-ResourceFilter <String[]>] [-ResourceGroupFilter <String[]>]
 -NotificationKey <String> [-NotificationEnabled] [-NotificationThreshold <Decimal>] [-ContactEmail <String[]>]
 [-ContactGroup <String[]>] [-ContactRole <String[]>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1f3a4-109">설명</span><span class="sxs-lookup"><span data-stu-id="1f3a4-109">DESCRIPTION</span></span>
<span data-ttu-id="1f3a4-110">이 Set-AzConsumptionBudget cmdlet은 구독 또는 리소스 그룹의 예산을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="1f3a4-110">The Set-AzConsumptionBudget cmdlet updates a budget in either a subscription or a resource group.</span></span>

## <span data-ttu-id="1f3a4-111">예제</span><span class="sxs-lookup"><span data-stu-id="1f3a4-111">EXAMPLES</span></span>

### <span data-ttu-id="1f3a4-112">예제 1: 구독 수준에서 예산 이름으로 새 금액으로 예산 업데이트</span><span class="sxs-lookup"><span data-stu-id="1f3a4-112">Example 1: Update a budget by a new amount with a budget name at subscription level</span></span>
```powershell
PS C:\> Set-AzConsumptionBudget -Name PSBudget -Amount 75
Amount:  75     
Category:  Cost
CurrentSpend:  null
Id:  subscriptions/1caaa5a3-2b66-438e-8ab4-bce37d518c5d/providers/Microsoft.Consumption/budgets/PSBudget
Name:  PSBudget
TimeGrain:  Monthly
TimePeriod:  EndDate:  11/1/2018 12:00:00 AM
             StartDate:  6/1/2018 12:00:00 AM
Type:  Microsoft.Consumption/budgets
```

### <span data-ttu-id="1f3a4-113">예제 2: 비용 또는 사용량이 구독 수준에서 금액의 90% 임계값에 도달하면 알림으로 예산 업데이트</span><span class="sxs-lookup"><span data-stu-id="1f3a4-113">Example 2: Update a budget with a notification when cost or usage reaches a threshold of 90 percent of amount at subscription level</span></span>
```powershell
PS C:\> Set-AzConsumptionBudget -Name PSBudget -NotificationKey notificationKey-ps1234 -NotificationEnabled -NotificationThreshold 90 -ContactEmail johndoe@contoso.com,janesmith@contoso.com -ContactRole Owner,Reader,Contributor
Amount:  75     
Category:  Cost
CurrentSpend:  null
Id:  subscriptions/1caaa5a3-2b66-438e-8ab4-bce37d518c5d/providers/Microsoft.Consumption/budgets/PSBudget
Name:  PSBudget
Notification:  NotificationKey:  notificationKey-ps1234
               Threshold:  90
               Enabled:  true
               ContactEmail:  johndoe@contoso.com,janesmith@contoso.com
               ContactRole:  Owner,Reader,Contributor
TimeGrain:  Monthly
TimePeriod:  EndDate:  11/1/2018 12:00:00 AM
             StartDate:  6/1/2018 12:00:00 AM
Type:  Microsoft.Consumption/budgets
```

### <span data-ttu-id="1f3a4-114">예제 3: 자원 그룹 수준에서 예산 이름을 새 금액으로 업데이트</span><span class="sxs-lookup"><span data-stu-id="1f3a4-114">Example 3: Update a budget by a new amount with a budget name at resource group level</span></span>
```powershell
PS C:\> Set-AzConsumptionBudget -ResourceGroupName RGBudgets -Name PSBudgetRG -Amount 75
Amount:  75     
Category:  Cost
CurrentSpend:  null
Id:  subscriptions/1caaa5a3-2b66-438e-8ab4-bce37d518c5d/resourceGroups/RGBudgets/providers/Microsoft.Consumption/budgets/PSBudgetRG
Name:  PSBudgetRG
TimeGrain:  Monthly
TimePeriod:  EndDate:  11/1/2018 12:00:00 AM
             StartDate:  6/1/2018 12:00:00 AM
Type:  Microsoft.Consumption/budgets
```

## <span data-ttu-id="1f3a4-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1f3a4-115">PARAMETERS</span></span>

### <span data-ttu-id="1f3a4-116">-Amount</span><span class="sxs-lookup"><span data-stu-id="1f3a4-116">-Amount</span></span>
<span data-ttu-id="1f3a4-117">예산의 양입니다.</span><span class="sxs-lookup"><span data-stu-id="1f3a4-117">Amount of a budget.</span></span>

```yaml
Type: System.Nullable`1[System.Decimal]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f3a4-118">-Category</span><span class="sxs-lookup"><span data-stu-id="1f3a4-118">-Category</span></span>
<span data-ttu-id="1f3a4-119">예산의 범주는 비용 또는 사용량일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1f3a4-119">Category of the budget can be cost or usage.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Cost, Usage

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f3a4-120">-ContactEmail</span><span class="sxs-lookup"><span data-stu-id="1f3a4-120">-ContactEmail</span></span>
<span data-ttu-id="1f3a4-121">임계값을 초과할 때 예산 알림을 보낼 전자 메일 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="1f3a4-121">Email addresses to send the budget notification to when the threshold is exceeded.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Notification, Piping and Notification
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f3a4-122">-ContactGroup</span><span class="sxs-lookup"><span data-stu-id="1f3a4-122">-ContactGroup</span></span>
<span data-ttu-id="1f3a4-123">임계값을 초과할 때 예산 알림을 보내는 작업 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="1f3a4-123">Action groups to send the budget notification to when the threshold is exceeded.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Notification, Piping and Notification
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f3a4-124">-ContactRole</span><span class="sxs-lookup"><span data-stu-id="1f3a4-124">-ContactRole</span></span>
<span data-ttu-id="1f3a4-125">임계값을 초과하는 경우 예산 알림을 보내기 위해 역할에 문의합니다.</span><span class="sxs-lookup"><span data-stu-id="1f3a4-125">Contact roles to send the budget notification to when the threshold is exceeded.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Notification, Piping and Notification
Aliases:
Accepted values: Owner, Reader, Contributor

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f3a4-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f3a4-126">-DefaultProfile</span></span>
<span data-ttu-id="1f3a4-127">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1f3a4-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1f3a4-128">-EndDate</span><span class="sxs-lookup"><span data-stu-id="1f3a4-128">-EndDate</span></span>
<span data-ttu-id="1f3a4-129">예산 기간의 종료 날짜(YYYY-MM-DD(UTC)입니다.</span><span class="sxs-lookup"><span data-stu-id="1f3a4-129">End date (YYYY-MM-DD in UTC) of time period of a budget.</span></span>

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

### <span data-ttu-id="1f3a4-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1f3a4-130">-InputObject</span></span>
<span data-ttu-id="1f3a4-131">예산 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="1f3a4-131">Budget object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Consumption.Models.PSBudget
Parameter Sets: Piping, Piping and Notification
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1f3a4-132">-MeterFilter</span><span class="sxs-lookup"><span data-stu-id="1f3a4-132">-MeterFilter</span></span>
<span data-ttu-id="1f3a4-133">필터링할 콤마로 구분된 미터 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="1f3a4-133">Comma-separated list of meters to filter on.</span></span>
<span data-ttu-id="1f3a4-134">범주가 사용량인 경우 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="1f3a4-134">Required if category is usage.</span></span>

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

### <span data-ttu-id="1f3a4-135">-Name</span><span class="sxs-lookup"><span data-stu-id="1f3a4-135">-Name</span></span>
<span data-ttu-id="1f3a4-136">예산의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1f3a4-136">Name of a budget.</span></span>

```yaml
Type: System.String
Parameter Sets: Subscription, Notification
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f3a4-137">-NotificationEnabled</span><span class="sxs-lookup"><span data-stu-id="1f3a4-137">-NotificationEnabled</span></span>
<span data-ttu-id="1f3a4-138">알림이 사용하도록 설정되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1f3a4-138">The notification is enabled.</span></span>
<span data-ttu-id="1f3a4-139">지정하지 않으면 알림은 기본적으로 비활성화됩니다.</span><span class="sxs-lookup"><span data-stu-id="1f3a4-139">If not specified, the notification is disabled by default.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Notification, Piping and Notification
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f3a4-140">-NotificationKey</span><span class="sxs-lookup"><span data-stu-id="1f3a4-140">-NotificationKey</span></span>
<span data-ttu-id="1f3a4-141">예산과 연결된 알림의 키로, 알림 사용 스위치, 알림 임계값, 연락처 전자 메일, 연락처 그룹 또는 연락처 역할로 알림을 만드는 데 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="1f3a4-141">Key of a notification associated with a budget, required to create a notification with notification enabled switch, notification threshold, contact emails, contact groups, or contact roles.</span></span>

```yaml
Type: System.String
Parameter Sets: Notification, Piping and Notification
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f3a4-142">-NotificationThreshold</span><span class="sxs-lookup"><span data-stu-id="1f3a4-142">-NotificationThreshold</span></span>
<span data-ttu-id="1f3a4-143">알림과 연결된 임계값입니다.</span><span class="sxs-lookup"><span data-stu-id="1f3a4-143">Threshold value associated with a notification.</span></span>
<span data-ttu-id="1f3a4-144">비용 또는 사용량이 임계값을 초과하면 알림이 전송됩니다.</span><span class="sxs-lookup"><span data-stu-id="1f3a4-144">Notification is sent when the cost or usage exceeded the threshold.</span></span>
<span data-ttu-id="1f3a4-145">항상 백분율로, 0~1000 사이가 됐습니다.</span><span class="sxs-lookup"><span data-stu-id="1f3a4-145">It is always percent and has to be between 0 and 1000.</span></span>

```yaml
Type: System.Nullable`1[System.Decimal]
Parameter Sets: Notification, Piping and Notification
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f3a4-146">-ResourceFilter</span><span class="sxs-lookup"><span data-stu-id="1f3a4-146">-ResourceFilter</span></span>
<span data-ttu-id="1f3a4-147">필터링할 리소스 인스턴스의 콤마로 구분된 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="1f3a4-147">Comma-separated list of resource instances to filter on.</span></span>

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

### <span data-ttu-id="1f3a4-148">-ResourceGroupFilter</span><span class="sxs-lookup"><span data-stu-id="1f3a4-148">-ResourceGroupFilter</span></span>
<span data-ttu-id="1f3a4-149">필터링할 리소스 그룹의 콤마로 구분된 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="1f3a4-149">Comma-separated list of resource groups to filter on.</span></span>

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

### <span data-ttu-id="1f3a4-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1f3a4-150">-ResourceGroupName</span></span>
<span data-ttu-id="1f3a4-151">예산의 리소스 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="1f3a4-151">Resource Group of a budget.</span></span>

```yaml
Type: System.String
Parameter Sets: Subscription, Notification
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f3a4-152">-StartDate</span><span class="sxs-lookup"><span data-stu-id="1f3a4-152">-StartDate</span></span>
<span data-ttu-id="1f3a4-153">예산 기간의 시작 날짜(YYYY-MM-DD(UTC)입니다.</span><span class="sxs-lookup"><span data-stu-id="1f3a4-153">Start date (YYYY-MM-DD in UTC) of time period of a budget.</span></span>
<span data-ttu-id="1f3a4-154">월별 시간(월별 시간)에 대해 현재 월 이전이 아 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1f3a4-154">Not prior to current month for monthly time grain.</span></span>
<span data-ttu-id="1f3a4-155">분기별 시간 세분화의 경우 3개월 이전이 아 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1f3a4-155">Not prior to three months for quarterly time grain.</span></span>
<span data-ttu-id="1f3a4-156">연별 시간 세분화의 경우 12개월 전이 아니어도 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1f3a4-156">Not prior to twelve months for yearly time grain.</span></span>
<span data-ttu-id="1f3a4-157">향후 시작 날짜는 3개월을 넘지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1f3a4-157">Future start date not more than three months.</span></span>

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

### <span data-ttu-id="1f3a4-158">-TimeGrain</span><span class="sxs-lookup"><span data-stu-id="1f3a4-158">-TimeGrain</span></span>
<span data-ttu-id="1f3a4-159">예산의 시간 세분화는 월별, 분기별 또는 연간일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1f3a4-159">Time grain of the budget can be monthly, quarterly, or annually.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Monthly, Quarterly, Annually

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f3a4-160">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1f3a4-160">-Confirm</span></span>
<span data-ttu-id="1f3a4-161">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="1f3a4-161">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1f3a4-162">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1f3a4-162">-WhatIf</span></span>
<span data-ttu-id="1f3a4-163">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="1f3a4-163">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1f3a4-164">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1f3a4-164">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1f3a4-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f3a4-165">CommonParameters</span></span>
<span data-ttu-id="1f3a4-166">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="1f3a4-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f3a4-167">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="1f3a4-167">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f3a4-168">입력</span><span class="sxs-lookup"><span data-stu-id="1f3a4-168">INPUTS</span></span>

### <span data-ttu-id="1f3a4-169">Microsoft.Azure.Commands.Consumption.Models.PSBudget</span><span class="sxs-lookup"><span data-stu-id="1f3a4-169">Microsoft.Azure.Commands.Consumption.Models.PSBudget</span></span>

## <span data-ttu-id="1f3a4-170">출력</span><span class="sxs-lookup"><span data-stu-id="1f3a4-170">OUTPUTS</span></span>

### <span data-ttu-id="1f3a4-171">Microsoft.Azure.Commands.Consumption.Models.PSBudget</span><span class="sxs-lookup"><span data-stu-id="1f3a4-171">Microsoft.Azure.Commands.Consumption.Models.PSBudget</span></span>

## <span data-ttu-id="1f3a4-172">참고 사항</span><span class="sxs-lookup"><span data-stu-id="1f3a4-172">NOTES</span></span>

## <span data-ttu-id="1f3a4-173">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1f3a4-173">RELATED LINKS</span></span>
