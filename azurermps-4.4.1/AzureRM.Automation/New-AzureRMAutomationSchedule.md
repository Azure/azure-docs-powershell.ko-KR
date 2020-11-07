---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: CB621890-EF8A-4F14-8F18-D8806E624DAB
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRMAutomationSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRMAutomationSchedule.md
ms.openlocfilehash: d82e63d21e18b7fb75282da9ac12be7644b0535a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93702885"
---
# <span data-ttu-id="f5d44-101">New-AzureRmAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="f5d44-101">New-AzureRmAutomationSchedule</span></span>

## <span data-ttu-id="f5d44-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f5d44-102">SYNOPSIS</span></span>
<span data-ttu-id="f5d44-103">자동화 일정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f5d44-103">Creates an Automation schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f5d44-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f5d44-104">SYNTAX</span></span>

### <span data-ttu-id="f5d44-105">일별 (기본값)</span><span class="sxs-lookup"><span data-stu-id="f5d44-105">ByDaily (Default)</span></span>
```
New-AzureRmAutomationSchedule [-Name] <String> [-StartTime] <DateTimeOffset> [-Description <String>]
 [-ExpiryTime <DateTimeOffset>] -DayInterval <Byte> [-TimeZone <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f5d44-106">ByWeekly</span><span class="sxs-lookup"><span data-stu-id="f5d44-106">ByWeekly</span></span>
```
New-AzureRmAutomationSchedule [-Name] <String> [-StartTime] <DateTimeOffset> [-Description <String>]
 [-DaysOfWeek <DayOfWeek[]>] [-ExpiryTime <DateTimeOffset>] -WeekInterval <Byte> [-TimeZone <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f5d44-107">ByMonthlyDaysOfMonth</span><span class="sxs-lookup"><span data-stu-id="f5d44-107">ByMonthlyDaysOfMonth</span></span>
```
New-AzureRmAutomationSchedule [-Name] <String> [-StartTime] <DateTimeOffset> [-Description <String>]
 [-DaysOfMonth <DaysOfMonth[]>] [-ExpiryTime <DateTimeOffset>] -MonthInterval <Byte> [-TimeZone <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f5d44-108">ByMonthlyDayOfWeek</span><span class="sxs-lookup"><span data-stu-id="f5d44-108">ByMonthlyDayOfWeek</span></span>
```
New-AzureRmAutomationSchedule [-Name] <String> [-StartTime] <DateTimeOffset> [-Description <String>]
 [-DayOfWeek <DayOfWeek>] [-DayOfWeekOccurrence <DayOfWeekOccurrence>] [-ExpiryTime <DateTimeOffset>]
 -MonthInterval <Byte> [-TimeZone <String>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f5d44-109">ByOneTime</span><span class="sxs-lookup"><span data-stu-id="f5d44-109">ByOneTime</span></span>
```
New-AzureRmAutomationSchedule [-Name] <String> [-StartTime] <DateTimeOffset> [-Description <String>] [-OneTime]
 [-TimeZone <String>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f5d44-110">매 시간</span><span class="sxs-lookup"><span data-stu-id="f5d44-110">ByHourly</span></span>
```
New-AzureRmAutomationSchedule [-Name] <String> [-StartTime] <DateTimeOffset> [-Description <String>]
 [-ExpiryTime <DateTimeOffset>] -HourInterval <Byte> [-TimeZone <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f5d44-111">설명은</span><span class="sxs-lookup"><span data-stu-id="f5d44-111">DESCRIPTION</span></span>
<span data-ttu-id="f5d44-112">**AzureRmAutomationSchedule** Cmdlet은 Azure Automation에서 일정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f5d44-112">The **New-AzureRmAutomationSchedule** cmdlet creates a schedule in Azure Automation.</span></span>

## <span data-ttu-id="f5d44-113">예제의</span><span class="sxs-lookup"><span data-stu-id="f5d44-113">EXAMPLES</span></span>

### <span data-ttu-id="f5d44-114">예제 1: 현지 시간에 일회성 일정 만들기</span><span class="sxs-lookup"><span data-stu-id="f5d44-114">Example 1: Create a one-time schedule in local time</span></span>
```
PS C:\>$TimeZone = ([System.TimeZoneInfo]::Local)Id
PS C:\> New-AzureRmAutomationSchedule -AutomationAccountName "Contoso17" -Name "Schedule01" -StartTime "23:00" -OneTime -ResourceGroupName "ResourceGroup01" -TimeZone $TimeZone
```

<span data-ttu-id="f5d44-115">첫 번째 명령은 시스템에서 표준 시간대 ID를 가져와 $TimeZone 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="f5d44-115">The first command gets the time zone ID from the system and stores it in the $TimeZone variable.</span></span>
<span data-ttu-id="f5d44-116">두 번째 명령은 지정 된 표준 시간대의 11:00 PM에서 현재 날짜에 대해 한 번 실행 되는 일정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f5d44-116">The second command creates a schedule that runs one time on the current date at 11:00 PM in the specified time zone..</span></span>

### <span data-ttu-id="f5d44-117">예제 2: 되풀이 일정 만들기</span><span class="sxs-lookup"><span data-stu-id="f5d44-117">Example 2: Create a recurring schedule</span></span>
```
PS C:\>$StartTime = Get-Date "13:00:00"
PS C:\> $EndTime = $StartTime.AddYears(1)
PS C:\> New-AzureRmAutomationSchedule -AutomationAccountName "Contoso17" -Name "Schedule02" -StartTime $StartTime -ExpiryTime $EndTime -DailyInterval 1 -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="f5d44-118">첫 번째 명령은 데이터 **가져오기** cmdlet을 사용 하 여 date 개체를 만든 다음 개체를 $StartDate 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="f5d44-118">The first command creates a date object by using the **Get-Date** cmdlet, and then stores the object in the $StartDate variable.</span></span>
<span data-ttu-id="f5d44-119">5 분 이상 이후 시간을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f5d44-119">Specify a time that is at least five minutes in the future.</span></span>

<span data-ttu-id="f5d44-120">두 번째 명령은 데이터 **가져오기** cmdlet을 사용 하 여 date 개체를 만든 다음 개체를 $EndDate 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="f5d44-120">The second command creates a date object by using the **Get-Date** cmdlet, and then stores the object in the $EndDate variable.</span></span>
<span data-ttu-id="f5d44-121">이 명령은 이후 시간을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f5d44-121">The command specifies a future time.</span></span>

<span data-ttu-id="f5d44-122">마지막 명령은 $StartDate에 저장 된 시간에 시작 하 고 $EndDate에 저장 된 시간에 만료 되는 Schedule01 라는 일일 일정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f5d44-122">The final command creates a daily schedule named Schedule01 to begin at the time stored in $StartDate and expire at the time stored in $EndDate.</span></span>

## <span data-ttu-id="f5d44-123">변수</span><span class="sxs-lookup"><span data-stu-id="f5d44-123">PARAMETERS</span></span>

### <span data-ttu-id="f5d44-124">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="f5d44-124">-AutomationAccountName</span></span>
<span data-ttu-id="f5d44-125">이 cmdlet이 일정을 만드는 Automation 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f5d44-125">Specifies the name of an Automation account for which this cmdlet creates a schedule.</span></span>

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

### <span data-ttu-id="f5d44-126">-DayInterval</span><span class="sxs-lookup"><span data-stu-id="f5d44-126">-DayInterval</span></span>
<span data-ttu-id="f5d44-127">일정에 대 한 간격 (일)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f5d44-127">Specifies an interval, in days, for the schedule.</span></span>
<span data-ttu-id="f5d44-128">이 매개 변수를 지정 하지 않고 *OneTime* 매개 변수를 지정 하지 않은 경우 기본값은 1입니다.</span><span class="sxs-lookup"><span data-stu-id="f5d44-128">If you do not specify this parameter, and you do not specify the *OneTime* parameter, the default value is one (1).</span></span>

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

### <span data-ttu-id="f5d44-129">-DayOfWeek</span><span class="sxs-lookup"><span data-stu-id="f5d44-129">-DayOfWeek</span></span>
<span data-ttu-id="f5d44-130">주간 일정에 대 한 요일 목록을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f5d44-130">Specifies a list of days of the week for the weekly schedule.</span></span>

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

### <span data-ttu-id="f5d44-131">-DayOfWeekOccurrence</span><span class="sxs-lookup"><span data-stu-id="f5d44-131">-DayOfWeekOccurrence</span></span>
<span data-ttu-id="f5d44-132">일정에서 실행 되는 월의 주 발생을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f5d44-132">Specifies the occurrence of the week within the month that the schedule runs.</span></span>
<span data-ttu-id="f5d44-133">psdx_paramvalues</span><span class="sxs-lookup"><span data-stu-id="f5d44-133">psdx_paramvalues</span></span>

- <span data-ttu-id="f5d44-134">raid-1</span><span class="sxs-lookup"><span data-stu-id="f5d44-134">1</span></span>
- <span data-ttu-id="f5d44-135">2</span><span class="sxs-lookup"><span data-stu-id="f5d44-135">2</span></span>
- <span data-ttu-id="f5d44-136">3-4</span><span class="sxs-lookup"><span data-stu-id="f5d44-136">3</span></span>
- <span data-ttu-id="f5d44-137">4(tcp/ipv4)</span><span class="sxs-lookup"><span data-stu-id="f5d44-137">4</span></span>
- <span data-ttu-id="f5d44-138">-1</span><span class="sxs-lookup"><span data-stu-id="f5d44-138">-1</span></span>
- <span data-ttu-id="f5d44-139">기본</span><span class="sxs-lookup"><span data-stu-id="f5d44-139">First</span></span>
- <span data-ttu-id="f5d44-140">두번째</span><span class="sxs-lookup"><span data-stu-id="f5d44-140">Second</span></span>
- <span data-ttu-id="f5d44-141">제 3</span><span class="sxs-lookup"><span data-stu-id="f5d44-141">Third</span></span>
- <span data-ttu-id="f5d44-142">커피</span><span class="sxs-lookup"><span data-stu-id="f5d44-142">Fourth</span></span>
- <span data-ttu-id="f5d44-143">마지막 일</span><span class="sxs-lookup"><span data-stu-id="f5d44-143">LastDay</span></span>

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

### <span data-ttu-id="f5d44-144">-DaysOfMonth</span><span class="sxs-lookup"><span data-stu-id="f5d44-144">-DaysOfMonth</span></span>
<span data-ttu-id="f5d44-145">월간 일정에 대 한 월의 일 목록을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f5d44-145">Specifies a list of days of the month for the monthly schedule.</span></span>

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

### <span data-ttu-id="f5d44-146">-DaysOfWeek</span><span class="sxs-lookup"><span data-stu-id="f5d44-146">-DaysOfWeek</span></span>
<span data-ttu-id="f5d44-147">주간 일정에 대 한 요일 목록을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f5d44-147">Specifies a list of days of the week for the weekly schedule.</span></span>

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

### <span data-ttu-id="f5d44-148">-설명</span><span class="sxs-lookup"><span data-stu-id="f5d44-148">-Description</span></span>
<span data-ttu-id="f5d44-149">일정에 대 한 설명을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f5d44-149">Specifies a description for the schedule.</span></span>

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

### <span data-ttu-id="f5d44-150">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="f5d44-150">-ExpiryTime</span></span>
<span data-ttu-id="f5d44-151">일정의 만료 시간을 **DateTimeOffest** 개체로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f5d44-151">Specifies the expiry time of a schedule as a **DateTimeOffest** object.</span></span>
<span data-ttu-id="f5d44-152">유효한 **DateTimeOffset** 으로 변환할 수 있는 문자열을 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f5d44-152">You can specify a string that can be converted to a valid **DateTimeOffset**.</span></span>

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

### <span data-ttu-id="f5d44-153">-HourInterval</span><span class="sxs-lookup"><span data-stu-id="f5d44-153">-HourInterval</span></span>
<span data-ttu-id="f5d44-154">일정에 대 한 간격 (시간)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f5d44-154">Specifies an interval, in hours, for the schedule.</span></span>

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

### <span data-ttu-id="f5d44-155">-MonthInterval</span><span class="sxs-lookup"><span data-stu-id="f5d44-155">-MonthInterval</span></span>
<span data-ttu-id="f5d44-156">일정에 대 한 간격을 개월 단위로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f5d44-156">Specifies an interval, in Months, for the schedule.</span></span>

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

### <span data-ttu-id="f5d44-157">-이름</span><span class="sxs-lookup"><span data-stu-id="f5d44-157">-Name</span></span>
<span data-ttu-id="f5d44-158">일정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f5d44-158">Specifies a name for the schedule.</span></span>

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

### <span data-ttu-id="f5d44-159">-OneTime</span><span class="sxs-lookup"><span data-stu-id="f5d44-159">-OneTime</span></span>
<span data-ttu-id="f5d44-160">Cmdlet에서 일회성 일정을 생성 하도록 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f5d44-160">Specifies that the cmdlet creates a one-time schedule.</span></span>

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

### <span data-ttu-id="f5d44-161">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f5d44-161">-ResourceGroupName</span></span>
<span data-ttu-id="f5d44-162">이 cmdlet에서 일정을 만드는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f5d44-162">Specifies the name of a resource group for which this cmdlet creates a schedule.</span></span>

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

### <span data-ttu-id="f5d44-163">-StartTime</span><span class="sxs-lookup"><span data-stu-id="f5d44-163">-StartTime</span></span>
<span data-ttu-id="f5d44-164">일정 시작 시간을 **DateTimeOffset** 개체로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f5d44-164">Specifies the start time of a schedule as a **DateTimeOffset** object.</span></span>
<span data-ttu-id="f5d44-165">유효한 **DateTimeOffset** 으로 변환할 수 있는 문자열을 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f5d44-165">You can specify a string that can be converted to a valid **DateTimeOffset**.</span></span>
<span data-ttu-id="f5d44-166">.</span><span class="sxs-lookup"><span data-stu-id="f5d44-166">.</span></span> <span data-ttu-id="f5d44-167">*TimeZone* 매개 변수를 지정 하면 오프셋이 무시 되 고 지정 된 표준 시간대가 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f5d44-167">If the *TimeZone* parameter is specified, the offset will be ignored and the time zone specified is used.</span></span>

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

### <span data-ttu-id="f5d44-168">-표준 시간대</span><span class="sxs-lookup"><span data-stu-id="f5d44-168">-TimeZone</span></span>
<span data-ttu-id="f5d44-169">일정에 대 한 표준 시간대를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f5d44-169">Specifies the time zone for the schedule.</span></span>
<span data-ttu-id="f5d44-170">이 문자열은 IANA ID 또는 Windows 표준 시간대 ID 일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f5d44-170">This string can be the IANA ID or the Windows Time Zone ID.</span></span>

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

### <span data-ttu-id="f5d44-171">-WeekInterval</span><span class="sxs-lookup"><span data-stu-id="f5d44-171">-WeekInterval</span></span>
<span data-ttu-id="f5d44-172">일정에 대 한 간격 (주)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f5d44-172">Specifies an interval, in weeks, for the schedule.</span></span>

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

### <span data-ttu-id="f5d44-173">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5d44-173">-DefaultProfile</span></span>
<span data-ttu-id="f5d44-174">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f5d44-174">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f5d44-175">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5d44-175">CommonParameters</span></span>
<span data-ttu-id="f5d44-176">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f5d44-176">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5d44-177">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f5d44-177">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5d44-178">입력</span><span class="sxs-lookup"><span data-stu-id="f5d44-178">INPUTS</span></span>

## <span data-ttu-id="f5d44-179">출력</span><span class="sxs-lookup"><span data-stu-id="f5d44-179">OUTPUTS</span></span>

### <span data-ttu-id="f5d44-180">Microsoft Azure. 명령. 일정</span><span class="sxs-lookup"><span data-stu-id="f5d44-180">Microsoft.Azure.Commands.Automation.Model.Schedule</span></span>

## <span data-ttu-id="f5d44-181">상속자</span><span class="sxs-lookup"><span data-stu-id="f5d44-181">NOTES</span></span>

## <span data-ttu-id="f5d44-182">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f5d44-182">RELATED LINKS</span></span>

[<span data-ttu-id="f5d44-183">Get-AzureRmAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="f5d44-183">Get-AzureRmAutomationSchedule</span></span>](./Get-AzureRMAutomationSchedule.md)

[<span data-ttu-id="f5d44-184">제거-AzureRmAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="f5d44-184">Remove-AzureRmAutomationSchedule</span></span>](./Remove-AzureRMAutomationSchedule.md)

[<span data-ttu-id="f5d44-185">Set-AzureRmAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="f5d44-185">Set-AzureRmAutomationSchedule</span></span>](./Set-AzureRMAutomationSchedule.md)


