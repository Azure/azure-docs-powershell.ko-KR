---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: A4C605DD-9B2E-4EE9-BD1F-1352D605C33F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/new-azurermautoscaleprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmAutoscaleProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmAutoscaleProfile.md
ms.openlocfilehash: 1d860c713c29fd10ba502150561e041c46a213aa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93711121"
---
# <span data-ttu-id="5a268-101">New-AzureRmAutoscaleProfile</span><span class="sxs-lookup"><span data-stu-id="5a268-101">New-AzureRmAutoscaleProfile</span></span>

## <span data-ttu-id="5a268-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5a268-102">SYNOPSIS</span></span>
<span data-ttu-id="5a268-103">자동 크기 조정 프로필을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5a268-103">Creates an Autoscale profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5a268-104">구문과</span><span class="sxs-lookup"><span data-stu-id="5a268-104">SYNTAX</span></span>

### <span data-ttu-id="5a268-105">CreateWithoutScheduledTimes</span><span class="sxs-lookup"><span data-stu-id="5a268-105">CreateWithoutScheduledTimes</span></span>
```
New-AzureRmAutoscaleProfile -Name <String> -DefaultCapacity <String> -MaximumCapacity <String>
 -MinimumCapacity <String>
 -Rule <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ScaleRule]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5a268-106">CreateWithFixedDateScheduling</span><span class="sxs-lookup"><span data-stu-id="5a268-106">CreateWithFixedDateScheduling</span></span>
```
New-AzureRmAutoscaleProfile -Name <String> -DefaultCapacity <String> -MaximumCapacity <String>
 -MinimumCapacity <String> -StartTimeWindow <DateTime> -EndTimeWindow <DateTime> -TimeWindowTimeZone <String>
 -Rule <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ScaleRule]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5a268-107">CreateUsingRecurrentScheduling</span><span class="sxs-lookup"><span data-stu-id="5a268-107">CreateUsingRecurrentScheduling</span></span>
```
New-AzureRmAutoscaleProfile -Name <String> -DefaultCapacity <String> -MaximumCapacity <String>
 -MinimumCapacity <String> -RecurrenceFrequency <RecurrenceFrequency>
 -ScheduleDay <System.Collections.Generic.List`1[System.String]>
 -ScheduleHour <System.Collections.Generic.List`1[System.Nullable`1[System.Int32]]>
 -ScheduleMinute <System.Collections.Generic.List`1[System.Nullable`1[System.Int32]]>
 -ScheduleTimeZone <String>
 -Rule <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ScaleRule]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5a268-108">설명은</span><span class="sxs-lookup"><span data-stu-id="5a268-108">DESCRIPTION</span></span>
<span data-ttu-id="5a268-109">**AzureRmAutoscaleProfile** Cmdlet은 자동 크기 조정 프로필을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5a268-109">The **New-AzureRmAutoscaleProfile** cmdlet creates an Autoscale profile.</span></span>

## <span data-ttu-id="5a268-110">예제의</span><span class="sxs-lookup"><span data-stu-id="5a268-110">EXAMPLES</span></span>

### <span data-ttu-id="5a268-111">예제 1: 고정 된 날짜를 사용 하 여 단일 프로필 만들기</span><span class="sxs-lookup"><span data-stu-id="5a268-111">Example 1: Create single profile with a fixed date</span></span>
```
PS C:\>$Rule = New-AzureRmAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1" 

PS C:\> $Profile = New-AzureRmAutoscaleProfile -DefaultCapacity "1" -MaximumCapacity "10" -MinimumCapacity "1" -StartTimeWindow 2015-03-05T14:00:00 -EndTimeWindow 2015-03-05T14:30:00 -TimeWindowTimeZone GMT -Rule $Rule -Name "Profile01"
Capacity   : Microsoft.Azure.Management.Insights.Models.ScaleCapacity
FixedDate  : Microsoft.Azure.Management.Insights.Models.TimeWindow
Name       : adios
Recurrence : 
Rules      : {Microsoft.Azure.Management.Insights.Models.ScaleRule, 
             Microsoft.Azure.Management.Insights.Models.ScaleRule}
```

<span data-ttu-id="5a268-112">첫 번째 명령은 요청 이라는 자동 크기 조정 규칙을 만든 다음이를 $Rule 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="5a268-112">The first command creates an Autoscale rule named Requests, and then stores it in the $Rule variable.</span></span>
<span data-ttu-id="5a268-113">두 번째 명령은 $Rule 규칙을 사용 하 여 고정 된 날짜의 Profile01 이라는 프로필을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5a268-113">The second command creates a profile named Profile01 with a fixed date using the rule in $Rule.</span></span>

### <span data-ttu-id="5a268-114">예제 2: 일정을 사용 하 여 프로필 만들기</span><span class="sxs-lookup"><span data-stu-id="5a268-114">Example 2: Create a profile with a schedule</span></span>
```
PS C:\>$Rule = New-AzureRmAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1" 

PS C:\> $Profile = New-AzureRmAutoscaleProfile -DefaultCapacity "1" -MaximumCapacity "10" -MinimumCapacity "1" -Rule $Rule -Name "SecondProfileName" -RecurrenceFrequency Minute -ScheduleDays "1", "2", "3" -ScheduleHours 5, 10, 15 -ScheduleMinutes 15, 30, 45 -ScheduleTimeZone GMT
Capacity   : Microsoft.Azure.Management.Insights.Models.ScaleCapacity
FixedDate  : 
Name       : secondProfileName
Recurrence : Microsoft.Azure.Management.Insights.Models.Recurrence
Rules      : {Microsoft.Azure.Management.Insights.Models.ScaleRule, 
             Microsoft.Azure.Management.Insights.Models.ScaleRule}
```

<span data-ttu-id="5a268-115">첫 번째 명령은 요청 이라는 자동 크기 조정 규칙을 만든 다음이를 $Rule 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="5a268-115">The first command creates an Autoscale rule named Requests, and then stores it in the $Rule variable.</span></span>
<span data-ttu-id="5a268-116">두 번째 명령은 $Rule에서 규칙을 사용 하 여 되풀이 일정으로 SecondProfileName 라는 프로필을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5a268-116">The second command creates a profile named SecondProfileName with a recurring schedule using the rule in $Rule.</span></span>

### <span data-ttu-id="5a268-117">예제 3: 두 개의 규칙을 사용 하 여 프로필 만들기</span><span class="sxs-lookup"><span data-stu-id="5a268-117">Example 3: Create profiles with two rules</span></span>
```
PS C:\>$Rule1 = New-AzureRmAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1" 

PS C:\> $Rule2 = New-AzureRmAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:10:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "2"

PS C:\> $Profile1 = New-AzureRmAutoscaleProfile -DefaultCapacity "1" -MaximumCapacity "10" -MinimumCapacity "1" -StartTimeWindow 2015-03-05T14:00:00 -EndTimeWindow 2015-03-05T14:30:00 -TimeWindowTimeZone GMT -Rule $Rule1, $Rule2 -Name "ProfileName"

PS C:\> $Profile2 = New-AzureRmAutoscaleProfile -DefaultCapacity "1" -MaximumCapacity "10" -MinimumCapacity "1" -Rule $Rule1, $Rule2 -Name "SecondProfileName" -RecurrenceFrequency Week -ScheduleDays "1" -ScheduleHours 5 -ScheduleMinutes 15 -ScheduleTimeZone UTC
Capacity   : Microsoft.Azure.Management.Insights.Models.ScaleCapacity
FixedDate  : Microsoft.Azure.Management.Insights.Models.TimeWindow
Name       : profileName
Recurrence : 
Rules      : {Microsoft.Azure.Management.Insights.Models.ScaleRule, 
             Microsoft.Azure.Management.Insights.Models.ScaleRule}
Capacity   : Microsoft.Azure.Management.Insights.Models.ScaleCapacity
FixedDate  : 
Name       : secondProfileName
Recurrence : Microsoft.Azure.Management.Insights.Models.Recurrence
Rules      : {Microsoft.Azure.Management.Insights.Models.ScaleRule, 
             Microsoft.Azure.Management.Insights.Models.ScaleRule}
```

<span data-ttu-id="5a268-118">처음 두 명령은 규칙을 만들고이를 변수 $Rule 1 및 $Rule 2에 각각 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="5a268-118">The first two commands create rules, and store them in the variables $Rule1 and $Rule2, respectively.</span></span>
<span data-ttu-id="5a268-119">세 번째 명령은 Rule1 및 Rule2의 규칙을 사용 하 여/Profile 이라는 프로필을 만든 다음이를 $Profile 1 변수로 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="5a268-119">The third command creates a profile named ProfileName using the rules in Rule1 and Rule2, and then stores it in the $Profile1 variable.</span></span>
<span data-ttu-id="5a268-120">마지막 명령은 Rule1 및 Rule2의 규칙을 사용 하 여 SecondProfileName 이라는 프로필을 만든 다음이를 $Profile 2 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="5a268-120">The final command creates a profile named SecondProfileName using the rules in Rule1 and Rule2, and then stores it in the $Profile2 variable.</span></span>

### <span data-ttu-id="5a268-121">예제 4: 일정이 나 고정 된 날짜 없이 프로필 만들기</span><span class="sxs-lookup"><span data-stu-id="5a268-121">Example 4: Create a profile with no schedule or fixed date</span></span>
```
PS C:\>$Rule = New-AzureRmAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1" 

PS C:\> $Profile = New-AzureRmAutoscaleProfile -DefaultCapacity "1" -MaximumCapacity "10" -MinimumCapacity "1" -Rule $Rule -Name "ProfileName"
```

<span data-ttu-id="5a268-122">첫 번째 명령은 요청 이라는 자동 크기 조정 규칙을 만든 다음이를 $Rule 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="5a268-122">The first command creates an Autoscale rule named Requests, and then stores it in the $Rule variable.</span></span>
<span data-ttu-id="5a268-123">두 번째 명령은 일정 또는 고정 날짜 없이 프로필을 만든 다음 $Profile 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="5a268-123">The second command creates a profile without a schedule or a fixed date, and then stores it in the $Profile variable.</span></span>

## <span data-ttu-id="5a268-124">변수</span><span class="sxs-lookup"><span data-stu-id="5a268-124">PARAMETERS</span></span>

### <span data-ttu-id="5a268-125">-DefaultCapacity</span><span class="sxs-lookup"><span data-stu-id="5a268-125">-DefaultCapacity</span></span>
<span data-ttu-id="5a268-126">기본 용량을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5a268-126">Specifies the default capacity.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a268-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a268-127">-DefaultProfile</span></span>
<span data-ttu-id="5a268-128">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="5a268-128">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5a268-129">-EndTimeWindow</span><span class="sxs-lookup"><span data-stu-id="5a268-129">-EndTimeWindow</span></span>
<span data-ttu-id="5a268-130">시간 창의 끝을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5a268-130">Specifies the end of the time window.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: CreateWithFixedDateScheduling
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a268-131">-MaximumCapacity</span><span class="sxs-lookup"><span data-stu-id="5a268-131">-MaximumCapacity</span></span>
<span data-ttu-id="5a268-132">최대 용량을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5a268-132">Specifies the maximum capacity.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a268-133">-가을 용량</span><span class="sxs-lookup"><span data-stu-id="5a268-133">-MinimumCapacity</span></span>
<span data-ttu-id="5a268-134">최소 용량을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5a268-134">Specifies the minimum capacity.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a268-135">-이름</span><span class="sxs-lookup"><span data-stu-id="5a268-135">-Name</span></span>
<span data-ttu-id="5a268-136">만들 프로필의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5a268-136">Specifies the name of the profile to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a268-137">-RecurrenceFrequency</span><span class="sxs-lookup"><span data-stu-id="5a268-137">-RecurrenceFrequency</span></span>
<span data-ttu-id="5a268-138">되풀이 빈도를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5a268-138">Specifies the frequency of recurrence.</span></span>
<span data-ttu-id="5a268-139">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="5a268-139">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="5a268-140">않아야</span><span class="sxs-lookup"><span data-stu-id="5a268-140">None</span></span>
- <span data-ttu-id="5a268-141">두번째</span><span class="sxs-lookup"><span data-stu-id="5a268-141">Second</span></span>
- <span data-ttu-id="5a268-142">길이의</span><span class="sxs-lookup"><span data-stu-id="5a268-142">Minute</span></span>
- <span data-ttu-id="5a268-143">시간씩</span><span class="sxs-lookup"><span data-stu-id="5a268-143">Hour</span></span>
- <span data-ttu-id="5a268-144">부활절</span><span class="sxs-lookup"><span data-stu-id="5a268-144">Day</span></span>
- <span data-ttu-id="5a268-145">이번</span><span class="sxs-lookup"><span data-stu-id="5a268-145">Week</span></span>
- <span data-ttu-id="5a268-146">달은</span><span class="sxs-lookup"><span data-stu-id="5a268-146">Month</span></span>
- <span data-ttu-id="5a268-147">Year 이러한 값 중 일부는 지원 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5a268-147">Year Not all of these values are supported.</span></span>

```yaml
Type: Microsoft.Azure.Management.Monitor.Management.Models.RecurrenceFrequency
Parameter Sets: CreateUsingRecurrentScheduling
Aliases:
Accepted values: None, Second, Minute, Hour, Day, Week, Month, Year

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a268-148">-규칙</span><span class="sxs-lookup"><span data-stu-id="5a268-148">-Rule</span></span>
<span data-ttu-id="5a268-149">프로필에 추가할 규칙 목록을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5a268-149">Specifies the list of rules to add to the profile.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ScaleRule]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a268-150">-ScheduleDay</span><span class="sxs-lookup"><span data-stu-id="5a268-150">-ScheduleDay</span></span>
<span data-ttu-id="5a268-151">예정 된 날짜를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5a268-151">Specifies the scheduled days.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: CreateUsingRecurrentScheduling
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a268-152">-ScheduleHour</span><span class="sxs-lookup"><span data-stu-id="5a268-152">-ScheduleHour</span></span>
<span data-ttu-id="5a268-153">예약 된 시간을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5a268-153">Specifies the scheduled hours.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.Nullable`1[System.Int32]]
Parameter Sets: CreateUsingRecurrentScheduling
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a268-154">-ScheduleMinute</span><span class="sxs-lookup"><span data-stu-id="5a268-154">-ScheduleMinute</span></span>
<span data-ttu-id="5a268-155">예정 된 시간 (분)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5a268-155">Specifies the scheduled minutes.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.Nullable`1[System.Int32]]
Parameter Sets: CreateUsingRecurrentScheduling
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a268-156">-ScheduleTimeZone</span><span class="sxs-lookup"><span data-stu-id="5a268-156">-ScheduleTimeZone</span></span>
<span data-ttu-id="5a268-157">일정의 시간대를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5a268-157">Specifies the time zone of the schedule.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateUsingRecurrentScheduling
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a268-158">-StartTimeWindow</span><span class="sxs-lookup"><span data-stu-id="5a268-158">-StartTimeWindow</span></span>
<span data-ttu-id="5a268-159">시간 창의 시작을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5a268-159">Specifies the start of the time window.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: CreateWithFixedDateScheduling
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a268-160">타임 창 표준 시간대</span><span class="sxs-lookup"><span data-stu-id="5a268-160">-TimeWindowTimeZone</span></span>
<span data-ttu-id="5a268-161">시간 창의 표준 시간대를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5a268-161">Specifies the time zone of the time window.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateWithFixedDateScheduling
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a268-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a268-162">CommonParameters</span></span>
<span data-ttu-id="5a268-163">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="5a268-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a268-164">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5a268-164">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a268-165">입력</span><span class="sxs-lookup"><span data-stu-id="5a268-165">INPUTS</span></span>

### <span data-ttu-id="5a268-166">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="5a268-166">System.String</span></span>

### <span data-ttu-id="5a268-167">시스템. 날짜/시간</span><span class="sxs-lookup"><span data-stu-id="5a268-167">System.DateTime</span></span>

### <span data-ttu-id="5a268-168">RecurrenceFrequency를 통해 관리 합니다.</span><span class="sxs-lookup"><span data-stu-id="5a268-168">Microsoft.Azure.Management.Monitor.Management.Models.RecurrenceFrequency</span></span>

### <span data-ttu-id="5a268-169">System.webserver. List ' 1 [[System. String, mscorlib, Version = 4.0.0.0, Culture = 중립, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="5a268-169">System.Collections.Generic.List\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="5a268-170">System.webserver. 목록 `1[[System.Nullable` 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = 중립, PublicKeyToken = b77a5c561934e089]], mscorlib, Version = 4.0.0.0, Culture = 중립, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="5a268-170">System.Collections.Generic.List`1[[System.Nullable`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]], mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="5a268-171">System.webserver. List ' 1 [[ScaleRule, Microsoft azure. 5.1.0.0, Version =, Culture = 중립, PublicKeyToken = null]]을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="5a268-171">System.Collections.Generic.List\`1[[Microsoft.Azure.Management.Monitor.Management.Models.ScaleRule, Microsoft.Azure.Commands.Insights, Version=5.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="5a268-172">출력</span><span class="sxs-lookup"><span data-stu-id="5a268-172">OUTPUTS</span></span>

### <span data-ttu-id="5a268-173">AutoscaleProfile를 통해 관리 합니다.</span><span class="sxs-lookup"><span data-stu-id="5a268-173">Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleProfile</span></span>

## <span data-ttu-id="5a268-174">상속자</span><span class="sxs-lookup"><span data-stu-id="5a268-174">NOTES</span></span>

## <span data-ttu-id="5a268-175">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5a268-175">RELATED LINKS</span></span>

[<span data-ttu-id="5a268-176">추가-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="5a268-176">Add-AzureRmAutoscaleSetting</span></span>](./Add-AzureRmAutoscaleSetting.md)

[<span data-ttu-id="5a268-177">Get-AzureRmAutoscaleHistory</span><span class="sxs-lookup"><span data-stu-id="5a268-177">Get-AzureRmAutoscaleHistory</span></span>](./Get-AzureRmAutoscaleHistory.md)

[<span data-ttu-id="5a268-178">Get-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="5a268-178">Get-AzureRmAutoscaleSetting</span></span>](./Get-AzureRmAutoscaleSetting.md)

[<span data-ttu-id="5a268-179">새로운 AzureRmAutoscaleRule</span><span class="sxs-lookup"><span data-stu-id="5a268-179">New-AzureRmAutoscaleRule</span></span>](./New-AzureRmAutoscaleRule.md)

[<span data-ttu-id="5a268-180">제거-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="5a268-180">Remove-AzureRmAutoscaleSetting</span></span>](./Remove-AzureRmAutoscaleSetting.md)


