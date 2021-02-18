---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: CB621890-EF8A-4F14-8F18-D8806E624DAB
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/new-azautomationschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationSchedule.md
ms.openlocfilehash: 9f9cd5b779fcc4e1b9dd6f3df7ed0255adeaa3af
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100201044"
---
# <span data-ttu-id="60aa4-101">New-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="60aa4-101">New-AzAutomationSchedule</span></span>

## <span data-ttu-id="60aa4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="60aa4-102">SYNOPSIS</span></span>
<span data-ttu-id="60aa4-103">Automation 일정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="60aa4-103">Creates an Automation schedule.</span></span>

## <span data-ttu-id="60aa4-104">구문</span><span class="sxs-lookup"><span data-stu-id="60aa4-104">SYNTAX</span></span>

### <span data-ttu-id="60aa4-105">ByDaily(기본값)</span><span class="sxs-lookup"><span data-stu-id="60aa4-105">ByDaily (Default)</span></span>
```
New-AzAutomationSchedule [-Name] <String> [-StartTime] <DateTimeOffset> [-Description <String>]
 [-ExpiryTime <DateTimeOffset>] -DayInterval <Byte> [-TimeZone <String>] [-ForUpdateConfiguration]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="60aa4-106">ByWeekly</span><span class="sxs-lookup"><span data-stu-id="60aa4-106">ByWeekly</span></span>
```
New-AzAutomationSchedule [-Name] <String> [-StartTime] <DateTimeOffset> [-Description <String>]
 [-DaysOfWeek <DayOfWeek[]>] [-ExpiryTime <DateTimeOffset>] -WeekInterval <Byte> [-TimeZone <String>]
 [-ForUpdateConfiguration] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="60aa4-107">ByMonthlyDaysOfMonth</span><span class="sxs-lookup"><span data-stu-id="60aa4-107">ByMonthlyDaysOfMonth</span></span>
```
New-AzAutomationSchedule [-Name] <String> [-StartTime] <DateTimeOffset> [-Description <String>]
 [-DaysOfMonth <DaysOfMonth[]>] [-ExpiryTime <DateTimeOffset>] -MonthInterval <Byte> [-TimeZone <String>]
 [-ForUpdateConfiguration] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="60aa4-108">ByMonthlyDayOfWeek</span><span class="sxs-lookup"><span data-stu-id="60aa4-108">ByMonthlyDayOfWeek</span></span>
```
New-AzAutomationSchedule [-Name] <String> [-StartTime] <DateTimeOffset> [-Description <String>]
 [-DayOfWeek <DayOfWeek>] [-DayOfWeekOccurrence <DayOfWeekOccurrence>] [-ExpiryTime <DateTimeOffset>]
 -MonthInterval <Byte> [-TimeZone <String>] [-ForUpdateConfiguration] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="60aa4-109">ByOneTime</span><span class="sxs-lookup"><span data-stu-id="60aa4-109">ByOneTime</span></span>
```
New-AzAutomationSchedule [-Name] <String> [-StartTime] <DateTimeOffset> [-Description <String>] [-OneTime]
 [-TimeZone <String>] [-ForUpdateConfiguration] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="60aa4-110">ByHourly</span><span class="sxs-lookup"><span data-stu-id="60aa4-110">ByHourly</span></span>
```
New-AzAutomationSchedule [-Name] <String> [-StartTime] <DateTimeOffset> [-Description <String>]
 [-ExpiryTime <DateTimeOffset>] -HourInterval <Byte> [-TimeZone <String>] [-ForUpdateConfiguration]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="60aa4-111">설명</span><span class="sxs-lookup"><span data-stu-id="60aa4-111">DESCRIPTION</span></span>
<span data-ttu-id="60aa4-112">**New-AzAutomationSchedule** cmdlet은 Azure Automation에서 일정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="60aa4-112">The **New-AzAutomationSchedule** cmdlet creates a schedule in Azure Automation.</span></span>

## <span data-ttu-id="60aa4-113">예제</span><span class="sxs-lookup"><span data-stu-id="60aa4-113">EXAMPLES</span></span>

### <span data-ttu-id="60aa4-114">예제 1: 현지 시간으로 일회성 일정 만들기</span><span class="sxs-lookup"><span data-stu-id="60aa4-114">Example 1: Create a one-time schedule in local time</span></span>
```
PS C:\> $TimeZone = ([System.TimeZoneInfo]::Local).Id
PS C:\> New-AzAutomationSchedule -AutomationAccountName "Contoso17" -Name "Schedule01" -StartTime "23:00" -OneTime -ResourceGroupName "ResourceGroup01" -TimeZone $TimeZone
```

<span data-ttu-id="60aa4-115">첫 번째 명령은 시스템에서 표준 시간대 ID를 사용하여 표준 시간대 ID를 $TimeZone 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="60aa4-115">The first command gets the time zone ID from the system and stores it in the $TimeZone variable.</span></span>
<span data-ttu-id="60aa4-116">두 번째 명령은 지정된 표준 시간대의 오후 11시에 현재 날짜에 한 번 실행되는 일정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="60aa4-116">The second command creates a schedule that runs one time on the current date at 11:00 PM in the specified time zone..</span></span>

### <span data-ttu-id="60aa4-117">예제 2: 재발 일정 만들기</span><span class="sxs-lookup"><span data-stu-id="60aa4-117">Example 2: Create a recurring schedule</span></span>
```
PS C:\> $StartTime = Get-Date "13:00:00"
PS C:\> $EndTime = $StartTime.AddYears(1)
PS C:\> New-AzAutomationSchedule -AutomationAccountName "Contoso17" -Name "Schedule02" -StartTime $StartTime -ExpiryTime $EndTime -DayInterval 1 -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="60aa4-118">첫 번째 명령은 **Get-Date** cmdlet을 사용하여 날짜 개체를 만든 다음, $StartDate 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="60aa4-118">The first command creates a date object by using the **Get-Date** cmdlet, and then stores the object in the $StartDate variable.</span></span>
<span data-ttu-id="60aa4-119">향후 최소 5분의 시간을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="60aa4-119">Specify a time that is at least five minutes in the future.</span></span>
<span data-ttu-id="60aa4-120">두 번째 명령은 **Get-Date** cmdlet을 사용하여 날짜 개체를 만든 다음, $EndDate 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="60aa4-120">The second command creates a date object by using the **Get-Date** cmdlet, and then stores the object in the $EndDate variable.</span></span>
<span data-ttu-id="60aa4-121">이 명령은 향후 시간을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="60aa4-121">The command specifies a future time.</span></span>
<span data-ttu-id="60aa4-122">마지막 명령은 Schedule02라는 일별 일정을 만들어 일정에 저장된 $StartDate 시작하고 일정에 저장된 $EndDate.</span><span class="sxs-lookup"><span data-stu-id="60aa4-122">The final command creates a daily schedule named Schedule02 to begin at the time stored in $StartDate and expire at the time stored in $EndDate.</span></span>

### <span data-ttu-id="60aa4-123">예제 3: 매주 일정 만들기</span><span class="sxs-lookup"><span data-stu-id="60aa4-123">Example 3: Create a weekly recurring schedule</span></span>
```
PS C:\> $StartTime = (Get-Date "13:00:00").AddDays(1)
PS C:\> [System.DayOfWeek[]]$WeekDays = @([System.DayOfWeek]::Monday..[System.DayOfWeek]::Friday)
PS C:\> New-AzAutomationSchedule -AutomationAccountName "Contoso17" -Name "Schedule03" -StartTime $StartTime - WeekInterval 1 -DaysOfWeek $WeekDays -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="60aa4-124">첫 번째 명령은 **Get-Date** cmdlet을 사용하여 날짜 개체를 만든 다음, $StartDate 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="60aa4-124">The first command creates a date object by using the **Get-Date** cmdlet, and then stores the object in the $StartDate variable.</span></span>
<span data-ttu-id="60aa4-125">두 번째 명령은 월요일, 화요일, 수요일, 목요일 및 금요일을 포함하는 주의 일 배열을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="60aa4-125">The second command creates an array of week days that contains Monday, Tuesday, Wednesday, Thursday and Friday.</span></span>
<span data-ttu-id="60aa4-126">마지막 명령은 매주 월요일~금요일 13:00에 실행될 Schedule03이라는 매일 일정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="60aa4-126">The final command creates a daily schedule named Schedule03 that will run Monday to Friday each week at 13:00.</span></span> <span data-ttu-id="60aa4-127">일정은 만료되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="60aa4-127">The schedule will never expire.</span></span>

## <span data-ttu-id="60aa4-128">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="60aa4-128">PARAMETERS</span></span>

### <span data-ttu-id="60aa4-129">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="60aa4-129">-AutomationAccountName</span></span>
<span data-ttu-id="60aa4-130">이 cmdlet이 일정을 만드는 Automation 계정의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="60aa4-130">Specifies the name of an Automation account for which this cmdlet creates a schedule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="60aa4-131">-DayInterval</span><span class="sxs-lookup"><span data-stu-id="60aa4-131">-DayInterval</span></span>
<span data-ttu-id="60aa4-132">일정에 대한 간격(일)을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="60aa4-132">Specifies an interval, in days, for the schedule.</span></span>
<span data-ttu-id="60aa4-133">이 매개 변수를 지정하지 않은 경우 *OneTime* 매개 변수를 지정하지 않으면 기본값은 1(1)입니다.</span><span class="sxs-lookup"><span data-stu-id="60aa4-133">If you do not specify this parameter, and you do not specify the *OneTime* parameter, the default value is one (1).</span></span>

```yaml
Type: System.Byte
Parameter Sets: ByDaily
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60aa4-134">-DayOfWeek</span><span class="sxs-lookup"><span data-stu-id="60aa4-134">-DayOfWeek</span></span>
<span data-ttu-id="60aa4-135">주간 일정에 대한 주중 일 목록을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="60aa4-135">Specifies a list of days of the week for the weekly schedule.</span></span>

```yaml
Type: System.Nullable`1[System.DayOfWeek]
Parameter Sets: ByMonthlyDayOfWeek
Aliases:
Accepted values: Sunday, Monday, Tuesday, Wednesday, Thursday, Friday, Saturday

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60aa4-136">-DayOfWeekOccurrence</span><span class="sxs-lookup"><span data-stu-id="60aa4-136">-DayOfWeekOccurrence</span></span>
<span data-ttu-id="60aa4-137">일정이 실행되는 월 내의 주를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="60aa4-137">Specifies the occurrence of the week within the month that the schedule runs.</span></span>
<span data-ttu-id="60aa4-138">psdx_paramvalues</span><span class="sxs-lookup"><span data-stu-id="60aa4-138">psdx_paramvalues</span></span>
- <span data-ttu-id="60aa4-139">1</span><span class="sxs-lookup"><span data-stu-id="60aa4-139">1</span></span>
- <span data-ttu-id="60aa4-140">2</span><span class="sxs-lookup"><span data-stu-id="60aa4-140">2</span></span>
- <span data-ttu-id="60aa4-141">3</span><span class="sxs-lookup"><span data-stu-id="60aa4-141">3</span></span>
- <span data-ttu-id="60aa4-142">4</span><span class="sxs-lookup"><span data-stu-id="60aa4-142">4</span></span>
- <span data-ttu-id="60aa4-143">-1</span><span class="sxs-lookup"><span data-stu-id="60aa4-143">-1</span></span>
- <span data-ttu-id="60aa4-144">First</span><span class="sxs-lookup"><span data-stu-id="60aa4-144">First</span></span>
- <span data-ttu-id="60aa4-145">초</span><span class="sxs-lookup"><span data-stu-id="60aa4-145">Second</span></span>
- <span data-ttu-id="60aa4-146">세 번째</span><span class="sxs-lookup"><span data-stu-id="60aa4-146">Third</span></span>
- <span data-ttu-id="60aa4-147">네 번째</span><span class="sxs-lookup"><span data-stu-id="60aa4-147">Fourth</span></span>
- <span data-ttu-id="60aa4-148">LastDay</span><span class="sxs-lookup"><span data-stu-id="60aa4-148">LastDay</span></span>

```yaml
Type: Microsoft.Azure.Commands.Automation.Cmdlet.DayOfWeekOccurrence
Parameter Sets: ByMonthlyDayOfWeek
Aliases:
Accepted values: First, Second, Third, Fourth, Last

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60aa4-149">-DaysOfMonth</span><span class="sxs-lookup"><span data-stu-id="60aa4-149">-DaysOfMonth</span></span>
<span data-ttu-id="60aa4-150">월별 일정에 대한 월의 일 목록을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="60aa4-150">Specifies a list of days of the month for the monthly schedule.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Automation.Cmdlet.DaysOfMonth[]
Parameter Sets: ByMonthlyDaysOfMonth
Aliases:
Accepted values: One, Two, Three, Four, Five, Six, Seventh, Eighth, Ninth, Tenth, Eleventh, Twelfth, Thirteenth, Fourteenth, Fifteenth, Sixteenth, Seventeenth, Eighteenth, Nineteenth, Twentieth, TwentyFirst, TwentySecond, TwentyThird, TwentyFourth, TwentyFifth, TwentySixth, TwentySeventh, TwentyEighth, TwentyNinth, Thirtieth, ThirtyFirst, LastDay

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60aa4-151">-DaysOfWeek</span><span class="sxs-lookup"><span data-stu-id="60aa4-151">-DaysOfWeek</span></span>
<span data-ttu-id="60aa4-152">주간 일정에 대한 주중 일 목록을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="60aa4-152">Specifies a list of days of the week for the weekly schedule.</span></span>

```yaml
Type: System.DayOfWeek[]
Parameter Sets: ByWeekly
Aliases:
Accepted values: Sunday, Monday, Tuesday, Wednesday, Thursday, Friday, Saturday

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60aa4-153">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60aa4-153">-DefaultProfile</span></span>
<span data-ttu-id="60aa4-154">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="60aa4-154">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="60aa4-155">-Description</span><span class="sxs-lookup"><span data-stu-id="60aa4-155">-Description</span></span>
<span data-ttu-id="60aa4-156">일정에 대한 설명을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="60aa4-156">Specifies a description for the schedule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="60aa4-157">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="60aa4-157">-ExpiryTime</span></span>
<span data-ttu-id="60aa4-158">일정의 만료 시간을 **DateTimeOffset** 개체로 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="60aa4-158">Specifies the expiry time of a schedule as a **DateTimeOffset** object.</span></span>
<span data-ttu-id="60aa4-159">유효한 **DateTimeOffset으로** 변환할 수 있는 문자열을 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="60aa4-159">You can specify a string that can be converted to a valid **DateTimeOffset**.</span></span>

```yaml
Type: System.DateTimeOffset
Parameter Sets: ByDaily, ByWeekly, ByMonthlyDaysOfMonth, ByMonthlyDayOfWeek, ByHourly
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60aa4-160">-ForUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="60aa4-160">-ForUpdateConfiguration</span></span>
<span data-ttu-id="60aa4-161">이 일정 개체가 소프트웨어 업데이트 구성 예약에 사용될 것 을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="60aa4-161">Indicates that this schedule object will be used for scheduling a software update configuration</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="60aa4-162">-HourInterval</span><span class="sxs-lookup"><span data-stu-id="60aa4-162">-HourInterval</span></span>
<span data-ttu-id="60aa4-163">일정에 대한 간격(시간)을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="60aa4-163">Specifies an interval, in hours, for the schedule.</span></span>

```yaml
Type: System.Byte
Parameter Sets: ByHourly
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60aa4-164">-MonthInterval</span><span class="sxs-lookup"><span data-stu-id="60aa4-164">-MonthInterval</span></span>
<span data-ttu-id="60aa4-165">일정에 대한 간격(월)을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="60aa4-165">Specifies an interval, in Months, for the schedule.</span></span>

```yaml
Type: System.Byte
Parameter Sets: ByMonthlyDaysOfMonth, ByMonthlyDayOfWeek
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60aa4-166">-Name</span><span class="sxs-lookup"><span data-stu-id="60aa4-166">-Name</span></span>
<span data-ttu-id="60aa4-167">일정의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="60aa4-167">Specifies a name for the schedule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="60aa4-168">-OneTime</span><span class="sxs-lookup"><span data-stu-id="60aa4-168">-OneTime</span></span>
<span data-ttu-id="60aa4-169">cmdlet이 일회성 일정을 만드는지 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="60aa4-169">Specifies that the cmdlet creates a one-time schedule.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByOneTime
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60aa4-170">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="60aa4-170">-ResourceGroupName</span></span>
<span data-ttu-id="60aa4-171">이 cmdlet이 일정을 만드는 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="60aa4-171">Specifies the name of a resource group for which this cmdlet creates a schedule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="60aa4-172">-StartTime</span><span class="sxs-lookup"><span data-stu-id="60aa4-172">-StartTime</span></span>
<span data-ttu-id="60aa4-173">일정의 시작 시간을 **DateTimeOffset** 개체로 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="60aa4-173">Specifies the start time of a schedule as a **DateTimeOffset** object.</span></span>
<span data-ttu-id="60aa4-174">유효한 **DateTimeOffset으로** 변환할 수 있는 문자열을 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="60aa4-174">You can specify a string that can be converted to a valid **DateTimeOffset**.</span></span>
<span data-ttu-id="60aa4-175">*TimeZone* 매개 변수를 지정하면 오프셋이 무시되고 지정된 표준 시간대가 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="60aa4-175">If the *TimeZone* parameter is specified, the offset will be ignored and the time zone specified is used.</span></span>

```yaml
Type: System.DateTimeOffset
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="60aa4-176">-TimeZone</span><span class="sxs-lookup"><span data-stu-id="60aa4-176">-TimeZone</span></span>
<span data-ttu-id="60aa4-177">일정에 대한 표준 시간대를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="60aa4-177">Specifies the time zone for the schedule.</span></span>
<span data-ttu-id="60aa4-178">이 문자열은 IANA ID 또는 Windows 표준 시간대 ID일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="60aa4-178">This string can be the IANA ID or the Windows Time Zone ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="60aa4-179">-WeekInterval</span><span class="sxs-lookup"><span data-stu-id="60aa4-179">-WeekInterval</span></span>
<span data-ttu-id="60aa4-180">일정에 대한 간격(주)을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="60aa4-180">Specifies an interval, in weeks, for the schedule.</span></span>

```yaml
Type: System.Byte
Parameter Sets: ByWeekly
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60aa4-181">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60aa4-181">CommonParameters</span></span>
<span data-ttu-id="60aa4-182">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="60aa4-182">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60aa4-183">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="60aa4-183">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60aa4-184">입력</span><span class="sxs-lookup"><span data-stu-id="60aa4-184">INPUTS</span></span>

### <span data-ttu-id="60aa4-185">System.String</span><span class="sxs-lookup"><span data-stu-id="60aa4-185">System.String</span></span>

### <span data-ttu-id="60aa4-186">System.DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="60aa4-186">System.DateTimeOffset</span></span>

### <span data-ttu-id="60aa4-187">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="60aa4-187">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="60aa4-188">출력</span><span class="sxs-lookup"><span data-stu-id="60aa4-188">OUTPUTS</span></span>

### <span data-ttu-id="60aa4-189">Microsoft.Azure.Commands.Automation.Model.Schedule</span><span class="sxs-lookup"><span data-stu-id="60aa4-189">Microsoft.Azure.Commands.Automation.Model.Schedule</span></span>

## <span data-ttu-id="60aa4-190">참고 사항</span><span class="sxs-lookup"><span data-stu-id="60aa4-190">NOTES</span></span>

## <span data-ttu-id="60aa4-191">관련 링크</span><span class="sxs-lookup"><span data-stu-id="60aa4-191">RELATED LINKS</span></span>

[<span data-ttu-id="60aa4-192">Get-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="60aa4-192">Get-AzAutomationSchedule</span></span>](./Get-AzAutomationSchedule.md)

[<span data-ttu-id="60aa4-193">Remove-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="60aa4-193">Remove-AzAutomationSchedule</span></span>](./Remove-AzAutomationSchedule.md)

[<span data-ttu-id="60aa4-194">Set-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="60aa4-194">Set-AzAutomationSchedule</span></span>](./Set-AzAutomationSchedule.md)


