---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: CB621890-EF8A-4F14-8F18-D8806E624DAB
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/new-azautomationschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationSchedule.md
ms.openlocfilehash: 9f9cd5b779fcc4e1b9dd6f3df7ed0255adeaa3af
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94047928"
---
# <span data-ttu-id="63e2e-101">New-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="63e2e-101">New-AzAutomationSchedule</span></span>

## <span data-ttu-id="63e2e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="63e2e-102">SYNOPSIS</span></span>
<span data-ttu-id="63e2e-103">자동화 일정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="63e2e-103">Creates an Automation schedule.</span></span>

## <span data-ttu-id="63e2e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="63e2e-104">SYNTAX</span></span>

### <span data-ttu-id="63e2e-105">일별 (기본값)</span><span class="sxs-lookup"><span data-stu-id="63e2e-105">ByDaily (Default)</span></span>
```
New-AzAutomationSchedule [-Name] <String> [-StartTime] <DateTimeOffset> [-Description <String>]
 [-ExpiryTime <DateTimeOffset>] -DayInterval <Byte> [-TimeZone <String>] [-ForUpdateConfiguration]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="63e2e-106">ByWeekly</span><span class="sxs-lookup"><span data-stu-id="63e2e-106">ByWeekly</span></span>
```
New-AzAutomationSchedule [-Name] <String> [-StartTime] <DateTimeOffset> [-Description <String>]
 [-DaysOfWeek <DayOfWeek[]>] [-ExpiryTime <DateTimeOffset>] -WeekInterval <Byte> [-TimeZone <String>]
 [-ForUpdateConfiguration] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="63e2e-107">ByMonthlyDaysOfMonth</span><span class="sxs-lookup"><span data-stu-id="63e2e-107">ByMonthlyDaysOfMonth</span></span>
```
New-AzAutomationSchedule [-Name] <String> [-StartTime] <DateTimeOffset> [-Description <String>]
 [-DaysOfMonth <DaysOfMonth[]>] [-ExpiryTime <DateTimeOffset>] -MonthInterval <Byte> [-TimeZone <String>]
 [-ForUpdateConfiguration] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="63e2e-108">ByMonthlyDayOfWeek</span><span class="sxs-lookup"><span data-stu-id="63e2e-108">ByMonthlyDayOfWeek</span></span>
```
New-AzAutomationSchedule [-Name] <String> [-StartTime] <DateTimeOffset> [-Description <String>]
 [-DayOfWeek <DayOfWeek>] [-DayOfWeekOccurrence <DayOfWeekOccurrence>] [-ExpiryTime <DateTimeOffset>]
 -MonthInterval <Byte> [-TimeZone <String>] [-ForUpdateConfiguration] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="63e2e-109">ByOneTime</span><span class="sxs-lookup"><span data-stu-id="63e2e-109">ByOneTime</span></span>
```
New-AzAutomationSchedule [-Name] <String> [-StartTime] <DateTimeOffset> [-Description <String>] [-OneTime]
 [-TimeZone <String>] [-ForUpdateConfiguration] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="63e2e-110">매 시간</span><span class="sxs-lookup"><span data-stu-id="63e2e-110">ByHourly</span></span>
```
New-AzAutomationSchedule [-Name] <String> [-StartTime] <DateTimeOffset> [-Description <String>]
 [-ExpiryTime <DateTimeOffset>] -HourInterval <Byte> [-TimeZone <String>] [-ForUpdateConfiguration]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="63e2e-111">설명은</span><span class="sxs-lookup"><span data-stu-id="63e2e-111">DESCRIPTION</span></span>
<span data-ttu-id="63e2e-112">**AzAutomationSchedule** Cmdlet은 Azure Automation에서 일정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="63e2e-112">The **New-AzAutomationSchedule** cmdlet creates a schedule in Azure Automation.</span></span>

## <span data-ttu-id="63e2e-113">예제의</span><span class="sxs-lookup"><span data-stu-id="63e2e-113">EXAMPLES</span></span>

### <span data-ttu-id="63e2e-114">예제 1: 현지 시간에 일회성 일정 만들기</span><span class="sxs-lookup"><span data-stu-id="63e2e-114">Example 1: Create a one-time schedule in local time</span></span>
```
PS C:\> $TimeZone = ([System.TimeZoneInfo]::Local).Id
PS C:\> New-AzAutomationSchedule -AutomationAccountName "Contoso17" -Name "Schedule01" -StartTime "23:00" -OneTime -ResourceGroupName "ResourceGroup01" -TimeZone $TimeZone
```

<span data-ttu-id="63e2e-115">첫 번째 명령은 시스템에서 표준 시간대 ID를 가져와 $TimeZone 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="63e2e-115">The first command gets the time zone ID from the system and stores it in the $TimeZone variable.</span></span>
<span data-ttu-id="63e2e-116">두 번째 명령은 지정 된 표준 시간대의 11:00 PM에서 현재 날짜에 대해 한 번 실행 되는 일정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="63e2e-116">The second command creates a schedule that runs one time on the current date at 11:00 PM in the specified time zone..</span></span>

### <span data-ttu-id="63e2e-117">예제 2: 되풀이 일정 만들기</span><span class="sxs-lookup"><span data-stu-id="63e2e-117">Example 2: Create a recurring schedule</span></span>
```
PS C:\> $StartTime = Get-Date "13:00:00"
PS C:\> $EndTime = $StartTime.AddYears(1)
PS C:\> New-AzAutomationSchedule -AutomationAccountName "Contoso17" -Name "Schedule02" -StartTime $StartTime -ExpiryTime $EndTime -DayInterval 1 -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="63e2e-118">첫 번째 명령은 데이터 **가져오기** cmdlet을 사용 하 여 date 개체를 만든 다음 개체를 $StartDate 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="63e2e-118">The first command creates a date object by using the **Get-Date** cmdlet, and then stores the object in the $StartDate variable.</span></span>
<span data-ttu-id="63e2e-119">5 분 이상 이후 시간을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="63e2e-119">Specify a time that is at least five minutes in the future.</span></span>
<span data-ttu-id="63e2e-120">두 번째 명령은 데이터 **가져오기** cmdlet을 사용 하 여 date 개체를 만든 다음 개체를 $EndDate 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="63e2e-120">The second command creates a date object by using the **Get-Date** cmdlet, and then stores the object in the $EndDate variable.</span></span>
<span data-ttu-id="63e2e-121">이 명령은 이후 시간을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="63e2e-121">The command specifies a future time.</span></span>
<span data-ttu-id="63e2e-122">마지막 명령은 $StartDate에 저장 된 시간에 시작 하 고 $EndDate에 저장 된 시간에 만료 되는 Schedule02 라는 일일 일정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="63e2e-122">The final command creates a daily schedule named Schedule02 to begin at the time stored in $StartDate and expire at the time stored in $EndDate.</span></span>

### <span data-ttu-id="63e2e-123">예제 3: 주간 되풀이 일정 만들기</span><span class="sxs-lookup"><span data-stu-id="63e2e-123">Example 3: Create a weekly recurring schedule</span></span>
```
PS C:\> $StartTime = (Get-Date "13:00:00").AddDays(1)
PS C:\> [System.DayOfWeek[]]$WeekDays = @([System.DayOfWeek]::Monday..[System.DayOfWeek]::Friday)
PS C:\> New-AzAutomationSchedule -AutomationAccountName "Contoso17" -Name "Schedule03" -StartTime $StartTime - WeekInterval 1 -DaysOfWeek $WeekDays -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="63e2e-124">첫 번째 명령은 데이터 **가져오기** cmdlet을 사용 하 여 date 개체를 만든 다음 개체를 $StartDate 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="63e2e-124">The first command creates a date object by using the **Get-Date** cmdlet, and then stores the object in the $StartDate variable.</span></span>
<span data-ttu-id="63e2e-125">두 번째 명령은 월요일, 화요일, 수요일, 목요일, 금요일이 포함 된 주 일 배열을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="63e2e-125">The second command creates an array of week days that contains Monday, Tuesday, Wednesday, Thursday and Friday.</span></span>
<span data-ttu-id="63e2e-126">마지막 명령은 13:00에서 매주 금요일에 월요일까지 실행 되는 Schedule03 라는 일일 일정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="63e2e-126">The final command creates a daily schedule named Schedule03 that will run Monday to Friday each week at 13:00.</span></span> <span data-ttu-id="63e2e-127">일정이 만료 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="63e2e-127">The schedule will never expire.</span></span>

## <span data-ttu-id="63e2e-128">변수</span><span class="sxs-lookup"><span data-stu-id="63e2e-128">PARAMETERS</span></span>

### <span data-ttu-id="63e2e-129">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="63e2e-129">-AutomationAccountName</span></span>
<span data-ttu-id="63e2e-130">이 cmdlet이 일정을 만드는 Automation 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="63e2e-130">Specifies the name of an Automation account for which this cmdlet creates a schedule.</span></span>

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

### <span data-ttu-id="63e2e-131">-DayInterval</span><span class="sxs-lookup"><span data-stu-id="63e2e-131">-DayInterval</span></span>
<span data-ttu-id="63e2e-132">일정에 대 한 간격 (일)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="63e2e-132">Specifies an interval, in days, for the schedule.</span></span>
<span data-ttu-id="63e2e-133">이 매개 변수를 지정 하지 않고 *OneTime* 매개 변수를 지정 하지 않은 경우 기본값은 1입니다.</span><span class="sxs-lookup"><span data-stu-id="63e2e-133">If you do not specify this parameter, and you do not specify the *OneTime* parameter, the default value is one (1).</span></span>

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

### <span data-ttu-id="63e2e-134">-DayOfWeek</span><span class="sxs-lookup"><span data-stu-id="63e2e-134">-DayOfWeek</span></span>
<span data-ttu-id="63e2e-135">주간 일정에 대 한 요일 목록을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="63e2e-135">Specifies a list of days of the week for the weekly schedule.</span></span>

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

### <span data-ttu-id="63e2e-136">-DayOfWeekOccurrence</span><span class="sxs-lookup"><span data-stu-id="63e2e-136">-DayOfWeekOccurrence</span></span>
<span data-ttu-id="63e2e-137">일정에서 실행 되는 월의 주 발생을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="63e2e-137">Specifies the occurrence of the week within the month that the schedule runs.</span></span>
<span data-ttu-id="63e2e-138">psdx_paramvalues</span><span class="sxs-lookup"><span data-stu-id="63e2e-138">psdx_paramvalues</span></span>
- <span data-ttu-id="63e2e-139">raid-1</span><span class="sxs-lookup"><span data-stu-id="63e2e-139">1</span></span>
- <span data-ttu-id="63e2e-140">2</span><span class="sxs-lookup"><span data-stu-id="63e2e-140">2</span></span>
- <span data-ttu-id="63e2e-141">3-4</span><span class="sxs-lookup"><span data-stu-id="63e2e-141">3</span></span>
- <span data-ttu-id="63e2e-142">4(tcp/ipv4)</span><span class="sxs-lookup"><span data-stu-id="63e2e-142">4</span></span>
- <span data-ttu-id="63e2e-143">-1</span><span class="sxs-lookup"><span data-stu-id="63e2e-143">-1</span></span>
- <span data-ttu-id="63e2e-144">기본</span><span class="sxs-lookup"><span data-stu-id="63e2e-144">First</span></span>
- <span data-ttu-id="63e2e-145">두번째</span><span class="sxs-lookup"><span data-stu-id="63e2e-145">Second</span></span>
- <span data-ttu-id="63e2e-146">제 3</span><span class="sxs-lookup"><span data-stu-id="63e2e-146">Third</span></span>
- <span data-ttu-id="63e2e-147">커피</span><span class="sxs-lookup"><span data-stu-id="63e2e-147">Fourth</span></span>
- <span data-ttu-id="63e2e-148">마지막 일</span><span class="sxs-lookup"><span data-stu-id="63e2e-148">LastDay</span></span>

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

### <span data-ttu-id="63e2e-149">-DaysOfMonth</span><span class="sxs-lookup"><span data-stu-id="63e2e-149">-DaysOfMonth</span></span>
<span data-ttu-id="63e2e-150">월간 일정에 대 한 월의 일 목록을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="63e2e-150">Specifies a list of days of the month for the monthly schedule.</span></span>

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

### <span data-ttu-id="63e2e-151">-DaysOfWeek</span><span class="sxs-lookup"><span data-stu-id="63e2e-151">-DaysOfWeek</span></span>
<span data-ttu-id="63e2e-152">주간 일정에 대 한 요일 목록을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="63e2e-152">Specifies a list of days of the week for the weekly schedule.</span></span>

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

### <span data-ttu-id="63e2e-153">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63e2e-153">-DefaultProfile</span></span>
<span data-ttu-id="63e2e-154">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="63e2e-154">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="63e2e-155">-설명</span><span class="sxs-lookup"><span data-stu-id="63e2e-155">-Description</span></span>
<span data-ttu-id="63e2e-156">일정에 대 한 설명을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="63e2e-156">Specifies a description for the schedule.</span></span>

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

### <span data-ttu-id="63e2e-157">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="63e2e-157">-ExpiryTime</span></span>
<span data-ttu-id="63e2e-158">일정의 만료 시간을 **DateTimeOffset** 개체로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="63e2e-158">Specifies the expiry time of a schedule as a **DateTimeOffset** object.</span></span>
<span data-ttu-id="63e2e-159">유효한 **DateTimeOffset** 으로 변환할 수 있는 문자열을 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="63e2e-159">You can specify a string that can be converted to a valid **DateTimeOffset**.</span></span>

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

### <span data-ttu-id="63e2e-160">-ForUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="63e2e-160">-ForUpdateConfiguration</span></span>
<span data-ttu-id="63e2e-161">이 일정 개체가 소프트웨어 업데이트 구성을 예약 하는 데 사용 됨을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="63e2e-161">Indicates that this schedule object will be used for scheduling a software update configuration</span></span>

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

### <span data-ttu-id="63e2e-162">-HourInterval</span><span class="sxs-lookup"><span data-stu-id="63e2e-162">-HourInterval</span></span>
<span data-ttu-id="63e2e-163">일정에 대 한 간격 (시간)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="63e2e-163">Specifies an interval, in hours, for the schedule.</span></span>

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

### <span data-ttu-id="63e2e-164">-MonthInterval</span><span class="sxs-lookup"><span data-stu-id="63e2e-164">-MonthInterval</span></span>
<span data-ttu-id="63e2e-165">일정에 대 한 간격을 개월 단위로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="63e2e-165">Specifies an interval, in Months, for the schedule.</span></span>

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

### <span data-ttu-id="63e2e-166">-이름</span><span class="sxs-lookup"><span data-stu-id="63e2e-166">-Name</span></span>
<span data-ttu-id="63e2e-167">일정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="63e2e-167">Specifies a name for the schedule.</span></span>

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

### <span data-ttu-id="63e2e-168">-OneTime</span><span class="sxs-lookup"><span data-stu-id="63e2e-168">-OneTime</span></span>
<span data-ttu-id="63e2e-169">Cmdlet에서 일회성 일정을 생성 하도록 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="63e2e-169">Specifies that the cmdlet creates a one-time schedule.</span></span>

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

### <span data-ttu-id="63e2e-170">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="63e2e-170">-ResourceGroupName</span></span>
<span data-ttu-id="63e2e-171">이 cmdlet에서 일정을 만드는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="63e2e-171">Specifies the name of a resource group for which this cmdlet creates a schedule.</span></span>

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

### <span data-ttu-id="63e2e-172">-StartTime</span><span class="sxs-lookup"><span data-stu-id="63e2e-172">-StartTime</span></span>
<span data-ttu-id="63e2e-173">일정 시작 시간을 **DateTimeOffset** 개체로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="63e2e-173">Specifies the start time of a schedule as a **DateTimeOffset** object.</span></span>
<span data-ttu-id="63e2e-174">유효한 **DateTimeOffset** 으로 변환할 수 있는 문자열을 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="63e2e-174">You can specify a string that can be converted to a valid **DateTimeOffset**.</span></span>
<span data-ttu-id="63e2e-175">*TimeZone* 매개 변수를 지정 하면 오프셋이 무시 되 고 지정 된 표준 시간대가 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="63e2e-175">If the *TimeZone* parameter is specified, the offset will be ignored and the time zone specified is used.</span></span>

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

### <span data-ttu-id="63e2e-176">-표준 시간대</span><span class="sxs-lookup"><span data-stu-id="63e2e-176">-TimeZone</span></span>
<span data-ttu-id="63e2e-177">일정에 대 한 표준 시간대를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="63e2e-177">Specifies the time zone for the schedule.</span></span>
<span data-ttu-id="63e2e-178">이 문자열은 IANA ID 또는 Windows 표준 시간대 ID 일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="63e2e-178">This string can be the IANA ID or the Windows Time Zone ID.</span></span>

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

### <span data-ttu-id="63e2e-179">-WeekInterval</span><span class="sxs-lookup"><span data-stu-id="63e2e-179">-WeekInterval</span></span>
<span data-ttu-id="63e2e-180">일정에 대 한 간격 (주)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="63e2e-180">Specifies an interval, in weeks, for the schedule.</span></span>

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

### <span data-ttu-id="63e2e-181">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63e2e-181">CommonParameters</span></span>
<span data-ttu-id="63e2e-182">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="63e2e-182">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63e2e-183">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="63e2e-183">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63e2e-184">입력</span><span class="sxs-lookup"><span data-stu-id="63e2e-184">INPUTS</span></span>

### <span data-ttu-id="63e2e-185">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="63e2e-185">System.String</span></span>

### <span data-ttu-id="63e2e-186">시스템 DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="63e2e-186">System.DateTimeOffset</span></span>

### <span data-ttu-id="63e2e-187">System.webserver 매개 변수</span><span class="sxs-lookup"><span data-stu-id="63e2e-187">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="63e2e-188">출력</span><span class="sxs-lookup"><span data-stu-id="63e2e-188">OUTPUTS</span></span>

### <span data-ttu-id="63e2e-189">Microsoft Azure. 명령. 일정</span><span class="sxs-lookup"><span data-stu-id="63e2e-189">Microsoft.Azure.Commands.Automation.Model.Schedule</span></span>

## <span data-ttu-id="63e2e-190">상속자</span><span class="sxs-lookup"><span data-stu-id="63e2e-190">NOTES</span></span>

## <span data-ttu-id="63e2e-191">관련 링크</span><span class="sxs-lookup"><span data-stu-id="63e2e-191">RELATED LINKS</span></span>

[<span data-ttu-id="63e2e-192">Get-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="63e2e-192">Get-AzAutomationSchedule</span></span>](./Get-AzAutomationSchedule.md)

[<span data-ttu-id="63e2e-193">제거-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="63e2e-193">Remove-AzAutomationSchedule</span></span>](./Remove-AzAutomationSchedule.md)

[<span data-ttu-id="63e2e-194">Set-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="63e2e-194">Set-AzAutomationSchedule</span></span>](./Set-AzAutomationSchedule.md)


