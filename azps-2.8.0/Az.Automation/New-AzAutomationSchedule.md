---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: CB621890-EF8A-4F14-8F18-D8806E624DAB
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/new-azautomationschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationSchedule.md
ms.openlocfilehash: 41cb8c91a38e1e0bf004ece1ed1c2e7618b8c44d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93697796"
---
# <span data-ttu-id="13d87-101">New-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="13d87-101">New-AzAutomationSchedule</span></span>

## <span data-ttu-id="13d87-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="13d87-102">SYNOPSIS</span></span>
<span data-ttu-id="13d87-103">자동화 일정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="13d87-103">Creates an Automation schedule.</span></span>

## <span data-ttu-id="13d87-104">구문과</span><span class="sxs-lookup"><span data-stu-id="13d87-104">SYNTAX</span></span>

### <span data-ttu-id="13d87-105">일별 (기본값)</span><span class="sxs-lookup"><span data-stu-id="13d87-105">ByDaily (Default)</span></span>
```
New-AzAutomationSchedule [-Name] <String> [-StartTime] <DateTimeOffset> [-Description <String>]
 [-ExpiryTime <DateTimeOffset>] -DayInterval <Byte> [-TimeZone <String>] [-ForUpdateConfiguration]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="13d87-106">ByWeekly</span><span class="sxs-lookup"><span data-stu-id="13d87-106">ByWeekly</span></span>
```
New-AzAutomationSchedule [-Name] <String> [-StartTime] <DateTimeOffset> [-Description <String>]
 [-DaysOfWeek <DayOfWeek[]>] [-ExpiryTime <DateTimeOffset>] -WeekInterval <Byte> [-TimeZone <String>]
 [-ForUpdateConfiguration] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="13d87-107">ByMonthlyDaysOfMonth</span><span class="sxs-lookup"><span data-stu-id="13d87-107">ByMonthlyDaysOfMonth</span></span>
```
New-AzAutomationSchedule [-Name] <String> [-StartTime] <DateTimeOffset> [-Description <String>]
 [-DaysOfMonth <DaysOfMonth[]>] [-ExpiryTime <DateTimeOffset>] -MonthInterval <Byte> [-TimeZone <String>]
 [-ForUpdateConfiguration] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="13d87-108">ByMonthlyDayOfWeek</span><span class="sxs-lookup"><span data-stu-id="13d87-108">ByMonthlyDayOfWeek</span></span>
```
New-AzAutomationSchedule [-Name] <String> [-StartTime] <DateTimeOffset> [-Description <String>]
 [-DayOfWeek <DayOfWeek>] [-DayOfWeekOccurrence <DayOfWeekOccurrence>] [-ExpiryTime <DateTimeOffset>]
 -MonthInterval <Byte> [-TimeZone <String>] [-ForUpdateConfiguration] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="13d87-109">ByOneTime</span><span class="sxs-lookup"><span data-stu-id="13d87-109">ByOneTime</span></span>
```
New-AzAutomationSchedule [-Name] <String> [-StartTime] <DateTimeOffset> [-Description <String>] [-OneTime]
 [-TimeZone <String>] [-ForUpdateConfiguration] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="13d87-110">매 시간</span><span class="sxs-lookup"><span data-stu-id="13d87-110">ByHourly</span></span>
```
New-AzAutomationSchedule [-Name] <String> [-StartTime] <DateTimeOffset> [-Description <String>]
 [-ExpiryTime <DateTimeOffset>] -HourInterval <Byte> [-TimeZone <String>] [-ForUpdateConfiguration]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="13d87-111">설명은</span><span class="sxs-lookup"><span data-stu-id="13d87-111">DESCRIPTION</span></span>
<span data-ttu-id="13d87-112">**AzAutomationSchedule** Cmdlet은 Azure Automation에서 일정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="13d87-112">The **New-AzAutomationSchedule** cmdlet creates a schedule in Azure Automation.</span></span>

## <span data-ttu-id="13d87-113">예제의</span><span class="sxs-lookup"><span data-stu-id="13d87-113">EXAMPLES</span></span>

### <span data-ttu-id="13d87-114">예제 1: 현지 시간에 일회성 일정 만들기</span><span class="sxs-lookup"><span data-stu-id="13d87-114">Example 1: Create a one-time schedule in local time</span></span>
```
PS C:\> $TimeZone = ([System.TimeZoneInfo]::Local).Id
PS C:\> New-AzAutomationSchedule -AutomationAccountName "Contoso17" -Name "Schedule01" -StartTime "23:00" -OneTime -ResourceGroupName "ResourceGroup01" -TimeZone $TimeZone
```

<span data-ttu-id="13d87-115">첫 번째 명령은 시스템에서 표준 시간대 ID를 가져와 $TimeZone 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="13d87-115">The first command gets the time zone ID from the system and stores it in the $TimeZone variable.</span></span>
<span data-ttu-id="13d87-116">두 번째 명령은 지정 된 표준 시간대의 11:00 PM에서 현재 날짜에 대해 한 번 실행 되는 일정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="13d87-116">The second command creates a schedule that runs one time on the current date at 11:00 PM in the specified time zone..</span></span>

### <span data-ttu-id="13d87-117">예제 2: 되풀이 일정 만들기</span><span class="sxs-lookup"><span data-stu-id="13d87-117">Example 2: Create a recurring schedule</span></span>
```
PS C:\> $StartTime = Get-Date "13:00:00"
PS C:\> $EndTime = $StartTime.AddYears(1)
PS C:\> New-AzAutomationSchedule -AutomationAccountName "Contoso17" -Name "Schedule02" -StartTime $StartTime -ExpiryTime $EndTime -DayInterval 1 -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="13d87-118">첫 번째 명령은 데이터 **가져오기** cmdlet을 사용 하 여 date 개체를 만든 다음 개체를 $StartDate 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="13d87-118">The first command creates a date object by using the **Get-Date** cmdlet, and then stores the object in the $StartDate variable.</span></span>
<span data-ttu-id="13d87-119">5 분 이상 이후 시간을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="13d87-119">Specify a time that is at least five minutes in the future.</span></span>
<span data-ttu-id="13d87-120">두 번째 명령은 데이터 **가져오기** cmdlet을 사용 하 여 date 개체를 만든 다음 개체를 $EndDate 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="13d87-120">The second command creates a date object by using the **Get-Date** cmdlet, and then stores the object in the $EndDate variable.</span></span>
<span data-ttu-id="13d87-121">이 명령은 이후 시간을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="13d87-121">The command specifies a future time.</span></span>
<span data-ttu-id="13d87-122">마지막 명령은 $StartDate에 저장 된 시간에 시작 하 고 $EndDate에 저장 된 시간에 만료 되는 Schedule02 라는 일일 일정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="13d87-122">The final command creates a daily schedule named Schedule02 to begin at the time stored in $StartDate and expire at the time stored in $EndDate.</span></span>

### <span data-ttu-id="13d87-123">예제 3: 주간 되풀이 일정 만들기</span><span class="sxs-lookup"><span data-stu-id="13d87-123">Example 3: Create a weekly recurring schedule</span></span>
```
PS C:\> $StartTime = (Get-Date "13:00:00").AddDays(1)
PS C:\> [System.DayOfWeek[]]$WeekDays = @([System.DayOfWeek]::Monday..[System.DayOfWeek]::Friday)
PS C:\> New-AzAutomationSchedule -AutomationAccountName "Contoso17" -Name "Schedule03" -StartTime $StartTime - WeekInterval 1 -DaysOfWeek $WeekDays -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="13d87-124">첫 번째 명령은 데이터 **가져오기** cmdlet을 사용 하 여 date 개체를 만든 다음 개체를 $StartDate 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="13d87-124">The first command creates a date object by using the **Get-Date** cmdlet, and then stores the object in the $StartDate variable.</span></span>
<span data-ttu-id="13d87-125">두 번째 명령은 월요일, 화요일, 수요일, 목요일, 금요일이 포함 된 주 일 배열을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="13d87-125">The second command creates an array of week days that contains Monday, Tuesday, Wednesday, Thursday and Friday.</span></span>
<span data-ttu-id="13d87-126">마지막 명령은 13:00에서 매주 금요일에 월요일까지 실행 되는 Schedule03 라는 일일 일정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="13d87-126">The final command creates a daily schedule named Schedule03 that will run Monday to Friday each week at 13:00.</span></span> <span data-ttu-id="13d87-127">일정이 만료 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="13d87-127">The schedule will never expire.</span></span>

## <span data-ttu-id="13d87-128">변수</span><span class="sxs-lookup"><span data-stu-id="13d87-128">PARAMETERS</span></span>

### <span data-ttu-id="13d87-129">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="13d87-129">-AutomationAccountName</span></span>
<span data-ttu-id="13d87-130">이 cmdlet이 일정을 만드는 Automation 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="13d87-130">Specifies the name of an Automation account for which this cmdlet creates a schedule.</span></span>

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

### <span data-ttu-id="13d87-131">-DayInterval</span><span class="sxs-lookup"><span data-stu-id="13d87-131">-DayInterval</span></span>
<span data-ttu-id="13d87-132">일정에 대 한 간격 (일)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="13d87-132">Specifies an interval, in days, for the schedule.</span></span>
<span data-ttu-id="13d87-133">이 매개 변수를 지정 하지 않고 *OneTime* 매개 변수를 지정 하지 않은 경우 기본값은 1입니다.</span><span class="sxs-lookup"><span data-stu-id="13d87-133">If you do not specify this parameter, and you do not specify the *OneTime* parameter, the default value is one (1).</span></span>

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

### <span data-ttu-id="13d87-134">-DayOfWeek</span><span class="sxs-lookup"><span data-stu-id="13d87-134">-DayOfWeek</span></span>
<span data-ttu-id="13d87-135">주간 일정에 대 한 요일 목록을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="13d87-135">Specifies a list of days of the week for the weekly schedule.</span></span>

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

### <span data-ttu-id="13d87-136">-DayOfWeekOccurrence</span><span class="sxs-lookup"><span data-stu-id="13d87-136">-DayOfWeekOccurrence</span></span>
<span data-ttu-id="13d87-137">일정에서 실행 되는 월의 주 발생을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="13d87-137">Specifies the occurrence of the week within the month that the schedule runs.</span></span>
<span data-ttu-id="13d87-138">psdx_paramvalues</span><span class="sxs-lookup"><span data-stu-id="13d87-138">psdx_paramvalues</span></span>
- <span data-ttu-id="13d87-139">raid-1</span><span class="sxs-lookup"><span data-stu-id="13d87-139">1</span></span>
- <span data-ttu-id="13d87-140">2</span><span class="sxs-lookup"><span data-stu-id="13d87-140">2</span></span>
- <span data-ttu-id="13d87-141">3-4</span><span class="sxs-lookup"><span data-stu-id="13d87-141">3</span></span>
- <span data-ttu-id="13d87-142">4(tcp/ipv4)</span><span class="sxs-lookup"><span data-stu-id="13d87-142">4</span></span>
- <span data-ttu-id="13d87-143">-1</span><span class="sxs-lookup"><span data-stu-id="13d87-143">-1</span></span>
- <span data-ttu-id="13d87-144">기본</span><span class="sxs-lookup"><span data-stu-id="13d87-144">First</span></span>
- <span data-ttu-id="13d87-145">두번째</span><span class="sxs-lookup"><span data-stu-id="13d87-145">Second</span></span>
- <span data-ttu-id="13d87-146">제 3</span><span class="sxs-lookup"><span data-stu-id="13d87-146">Third</span></span>
- <span data-ttu-id="13d87-147">커피</span><span class="sxs-lookup"><span data-stu-id="13d87-147">Fourth</span></span>
- <span data-ttu-id="13d87-148">마지막 일</span><span class="sxs-lookup"><span data-stu-id="13d87-148">LastDay</span></span>

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

### <span data-ttu-id="13d87-149">-DaysOfMonth</span><span class="sxs-lookup"><span data-stu-id="13d87-149">-DaysOfMonth</span></span>
<span data-ttu-id="13d87-150">월간 일정에 대 한 월의 일 목록을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="13d87-150">Specifies a list of days of the month for the monthly schedule.</span></span>

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

### <span data-ttu-id="13d87-151">-DaysOfWeek</span><span class="sxs-lookup"><span data-stu-id="13d87-151">-DaysOfWeek</span></span>
<span data-ttu-id="13d87-152">주간 일정에 대 한 요일 목록을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="13d87-152">Specifies a list of days of the week for the weekly schedule.</span></span>

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

### <span data-ttu-id="13d87-153">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13d87-153">-DefaultProfile</span></span>
<span data-ttu-id="13d87-154">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="13d87-154">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="13d87-155">-설명</span><span class="sxs-lookup"><span data-stu-id="13d87-155">-Description</span></span>
<span data-ttu-id="13d87-156">일정에 대 한 설명을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="13d87-156">Specifies a description for the schedule.</span></span>

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

### <span data-ttu-id="13d87-157">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="13d87-157">-ExpiryTime</span></span>
<span data-ttu-id="13d87-158">일정의 만료 시간을 **DateTimeOffset** 개체로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="13d87-158">Specifies the expiry time of a schedule as a **DateTimeOffset** object.</span></span>
<span data-ttu-id="13d87-159">유효한 **DateTimeOffset** 으로 변환할 수 있는 문자열을 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="13d87-159">You can specify a string that can be converted to a valid **DateTimeOffset**.</span></span>

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

### <span data-ttu-id="13d87-160">-ForUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="13d87-160">-ForUpdateConfiguration</span></span>
<span data-ttu-id="13d87-161">이 일정 개체가 소프트웨어 업데이트 구성을 예약 하는 데 사용 됨을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="13d87-161">Indicates that this schedule object will be used for scheduling a software update configuration</span></span>

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

### <span data-ttu-id="13d87-162">-HourInterval</span><span class="sxs-lookup"><span data-stu-id="13d87-162">-HourInterval</span></span>
<span data-ttu-id="13d87-163">일정에 대 한 간격 (시간)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="13d87-163">Specifies an interval, in hours, for the schedule.</span></span>

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

### <span data-ttu-id="13d87-164">-MonthInterval</span><span class="sxs-lookup"><span data-stu-id="13d87-164">-MonthInterval</span></span>
<span data-ttu-id="13d87-165">일정에 대 한 간격을 개월 단위로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="13d87-165">Specifies an interval, in Months, for the schedule.</span></span>

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

### <span data-ttu-id="13d87-166">-이름</span><span class="sxs-lookup"><span data-stu-id="13d87-166">-Name</span></span>
<span data-ttu-id="13d87-167">일정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="13d87-167">Specifies a name for the schedule.</span></span>

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

### <span data-ttu-id="13d87-168">-OneTime</span><span class="sxs-lookup"><span data-stu-id="13d87-168">-OneTime</span></span>
<span data-ttu-id="13d87-169">Cmdlet에서 일회성 일정을 생성 하도록 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="13d87-169">Specifies that the cmdlet creates a one-time schedule.</span></span>

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

### <span data-ttu-id="13d87-170">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="13d87-170">-ResourceGroupName</span></span>
<span data-ttu-id="13d87-171">이 cmdlet에서 일정을 만드는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="13d87-171">Specifies the name of a resource group for which this cmdlet creates a schedule.</span></span>

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

### <span data-ttu-id="13d87-172">-StartTime</span><span class="sxs-lookup"><span data-stu-id="13d87-172">-StartTime</span></span>
<span data-ttu-id="13d87-173">일정 시작 시간을 **DateTimeOffset** 개체로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="13d87-173">Specifies the start time of a schedule as a **DateTimeOffset** object.</span></span>
<span data-ttu-id="13d87-174">유효한 **DateTimeOffset** 으로 변환할 수 있는 문자열을 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="13d87-174">You can specify a string that can be converted to a valid **DateTimeOffset**.</span></span>
<span data-ttu-id="13d87-175">*TimeZone* 매개 변수를 지정 하면 오프셋이 무시 되 고 지정 된 표준 시간대가 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="13d87-175">If the *TimeZone* parameter is specified, the offset will be ignored and the time zone specified is used.</span></span>

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

### <span data-ttu-id="13d87-176">-표준 시간대</span><span class="sxs-lookup"><span data-stu-id="13d87-176">-TimeZone</span></span>
<span data-ttu-id="13d87-177">일정에 대 한 표준 시간대를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="13d87-177">Specifies the time zone for the schedule.</span></span>
<span data-ttu-id="13d87-178">이 문자열은 IANA ID 또는 Windows 표준 시간대 ID 일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="13d87-178">This string can be the IANA ID or the Windows Time Zone ID.</span></span>

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

### <span data-ttu-id="13d87-179">-WeekInterval</span><span class="sxs-lookup"><span data-stu-id="13d87-179">-WeekInterval</span></span>
<span data-ttu-id="13d87-180">일정에 대 한 간격 (주)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="13d87-180">Specifies an interval, in weeks, for the schedule.</span></span>

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

### <span data-ttu-id="13d87-181">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13d87-181">CommonParameters</span></span>
<span data-ttu-id="13d87-182">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="13d87-182">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13d87-183">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="13d87-183">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13d87-184">입력</span><span class="sxs-lookup"><span data-stu-id="13d87-184">INPUTS</span></span>

### <span data-ttu-id="13d87-185">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="13d87-185">System.String</span></span>

### <span data-ttu-id="13d87-186">시스템 DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="13d87-186">System.DateTimeOffset</span></span>

### <span data-ttu-id="13d87-187">System.webserver 매개 변수</span><span class="sxs-lookup"><span data-stu-id="13d87-187">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="13d87-188">출력</span><span class="sxs-lookup"><span data-stu-id="13d87-188">OUTPUTS</span></span>

### <span data-ttu-id="13d87-189">Microsoft Azure. 명령. 일정</span><span class="sxs-lookup"><span data-stu-id="13d87-189">Microsoft.Azure.Commands.Automation.Model.Schedule</span></span>

## <span data-ttu-id="13d87-190">상속자</span><span class="sxs-lookup"><span data-stu-id="13d87-190">NOTES</span></span>

## <span data-ttu-id="13d87-191">관련 링크</span><span class="sxs-lookup"><span data-stu-id="13d87-191">RELATED LINKS</span></span>

[<span data-ttu-id="13d87-192">Get-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="13d87-192">Get-AzAutomationSchedule</span></span>](./Get-AzAutomationSchedule.md)

[<span data-ttu-id="13d87-193">제거-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="13d87-193">Remove-AzAutomationSchedule</span></span>](./Remove-AzAutomationSchedule.md)

[<span data-ttu-id="13d87-194">Set-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="13d87-194">Set-AzAutomationSchedule</span></span>](./Set-AzAutomationSchedule.md)


