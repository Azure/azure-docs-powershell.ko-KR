---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: A4C605DD-9B2E-4EE9-BD1F-1352D605C33F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmAutoscaleProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmAutoscaleProfile.md
ms.openlocfilehash: a5cea42544f2f24ad6c1f1cc1ce64bf122e53440
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93536384"
---
# <span data-ttu-id="268ba-101">New-AzureRmAutoscaleProfile</span><span class="sxs-lookup"><span data-stu-id="268ba-101">New-AzureRmAutoscaleProfile</span></span>

## <span data-ttu-id="268ba-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="268ba-102">SYNOPSIS</span></span>
<span data-ttu-id="268ba-103">자동 크기 조정 프로필을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="268ba-103">Creates an Autoscale profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="268ba-104">구문과</span><span class="sxs-lookup"><span data-stu-id="268ba-104">SYNTAX</span></span>

### <span data-ttu-id="268ba-105">예약 된 시간 없이 New-AzureRmAutoscaleProfile cmdlet에 대 한 매개 변수</span><span class="sxs-lookup"><span data-stu-id="268ba-105">Parameters for New-AzureRmAutoscaleProfile cmdlet without scheduled times</span></span>
```
New-AzureRmAutoscaleProfile -Name <String> -DefaultCapacity <String> -MaximumCapacity <String>
 -MinimumCapacity <String>
 -Rules <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ScaleRule]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="268ba-106">해결 방법 수정 날짜 일정을 사용 하는 New-AzureRmAutoscaleProfile cmdlet의 매개 변수</span><span class="sxs-lookup"><span data-stu-id="268ba-106">Parameters for New-AzureRmAutoscaleProfile cmdlet using fix date scheduling</span></span>
```
New-AzureRmAutoscaleProfile -Name <String> -DefaultCapacity <String> -MaximumCapacity <String>
 -MinimumCapacity <String> -StartTimeWindow <DateTime> -EndTimeWindow <DateTime> -TimeWindowTimeZone <String>
 -Rules <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ScaleRule]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="268ba-107">되풀이 일정을 사용 하는 New-AzureRmAutoscaleProfile cmdlet에 대 한 매개 변수</span><span class="sxs-lookup"><span data-stu-id="268ba-107">Parameters for New-AzureRmAutoscaleProfile cmdlet using recurrent scheduling</span></span>
```
New-AzureRmAutoscaleProfile -Name <String> -DefaultCapacity <String> -MaximumCapacity <String>
 -MinimumCapacity <String> -RecurrenceFrequency <RecurrenceFrequency>
 -ScheduleDays <System.Collections.Generic.List`1[System.String]>
 -ScheduleHours <System.Collections.Generic.List`1[System.Nullable`1[System.Int32]]>
 -ScheduleMinutes <System.Collections.Generic.List`1[System.Nullable`1[System.Int32]]>
 -ScheduleTimeZone <String>
 -Rules <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ScaleRule]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="268ba-108">설명은</span><span class="sxs-lookup"><span data-stu-id="268ba-108">DESCRIPTION</span></span>
<span data-ttu-id="268ba-109">**AzureRmAutoscaleProfile** Cmdlet은 자동 크기 조정 프로필을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="268ba-109">The **New-AzureRmAutoscaleProfile** cmdlet creates an Autoscale profile.</span></span>

## <span data-ttu-id="268ba-110">예제의</span><span class="sxs-lookup"><span data-stu-id="268ba-110">EXAMPLES</span></span>

### <span data-ttu-id="268ba-111">예제 1: 고정 된 날짜를 사용 하 여 단일 프로필 만들기</span><span class="sxs-lookup"><span data-stu-id="268ba-111">Example 1: Create single profile with a fixed date</span></span>
```
PS C:\>$Rule = New-AzureRmAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1" 

PS C:\> $Profile = New-AzureRmAutoscaleProfile -DefaultCapacity "1" -MaximumCapacity "10" -MinimumCapacity "1" -StartTimeWindow 2015-03-05T14:00:00 -EndTimeWindow 2015-03-05T14:30:00 -TimeWindowTimeZone GMT -Rules $Rule -Name "Profile01"
Capacity   : Microsoft.Azure.Management.Insights.Models.ScaleCapacity
FixedDate  : Microsoft.Azure.Management.Insights.Models.TimeWindow
Name       : adios
Recurrence : 
Rules      : {Microsoft.Azure.Management.Insights.Models.ScaleRule, 
             Microsoft.Azure.Management.Insights.Models.ScaleRule}
```

<span data-ttu-id="268ba-112">첫 번째 명령은 요청 이라는 자동 크기 조정 규칙을 만든 다음이를 $Rule 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="268ba-112">The first command creates an Autoscale rule named Requests, and then stores it in the $Rule variable.</span></span>

<span data-ttu-id="268ba-113">두 번째 명령은 $Rule 규칙을 사용 하 여 고정 된 날짜의 Profile01 이라는 프로필을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="268ba-113">The second command creates a profile named Profile01 with a fixed date using the rule in $Rule.</span></span>

### <span data-ttu-id="268ba-114">예제 2: 일정을 사용 하 여 프로필 만들기</span><span class="sxs-lookup"><span data-stu-id="268ba-114">Example 2: Create a profile with a schedule</span></span>
```
PS C:\>$Rule = New-AzureRmAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1" 

PS C:\> $Profile = New-AzureRmAutoscaleProfile -DefaultCapacity "1" -MaximumCapacity "10" -MinimumCapacity "1" -Rules $Rule -Name "SecondProfileName" -RecurrenceFrequency Minute -ScheduleDays "1", "2", "3" -ScheduleHours 5, 10, 15 -ScheduleMinutes 15, 30, 45 -ScheduleTimeZone GMT
Capacity   : Microsoft.Azure.Management.Insights.Models.ScaleCapacity
FixedDate  : 
Name       : secondProfileName
Recurrence : Microsoft.Azure.Management.Insights.Models.Recurrence
Rules      : {Microsoft.Azure.Management.Insights.Models.ScaleRule, 
             Microsoft.Azure.Management.Insights.Models.ScaleRule}
```

<span data-ttu-id="268ba-115">첫 번째 명령은 요청 이라는 자동 크기 조정 규칙을 만든 다음이를 $Rule 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="268ba-115">The first command creates an Autoscale rule named Requests, and then stores it in the $Rule variable.</span></span>

<span data-ttu-id="268ba-116">두 번째 명령은 $Rule에서 규칙을 사용 하 여 되풀이 일정으로 SecondProfileName 라는 프로필을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="268ba-116">The second command creates a profile named SecondProfileName with a recurring schedule using the rule in $Rule.</span></span>

### <span data-ttu-id="268ba-117">예제 3: 두 개의 규칙을 사용 하 여 프로필 만들기</span><span class="sxs-lookup"><span data-stu-id="268ba-117">Example 3: Create profiles with two rules</span></span>
```
PS C:\>$Rule1 = New-AzureRmAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1" 

PS C:\> $Rule2 = New-AzureRmAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:10:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "2"

PS C:\> $Profile1 = New-AzureRmAutoscaleProfile -DefaultCapacity "1" -MaximumCapacity "10" -MinimumCapacity "1" -StartTimeWindow 2015-03-05T14:00:00 -EndTimeWindow 2015-03-05T14:30:00 -TimeWindowTimeZone GMT -Rules $Rule1, $Rule2 -Name "ProfileName"

PS C:\> $Profile2 = New-AzureRmAutoscaleProfile -DefaultCapacity "1" -MaximumCapacity "10" -MinimumCapacity "1" -Rules $Rule1, $Rule2 -Name "SecondProfileName" -RecurrenceFrequency Week -ScheduleDays "1" -ScheduleHours 5 -ScheduleMinutes 15 -ScheduleTimeZone UTC
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

<span data-ttu-id="268ba-118">처음 두 명령은 규칙을 만들고이를 변수 $Rule 1 및 $Rule 2에 각각 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="268ba-118">The first two commands create rules, and store them in the variables $Rule1 and $Rule2, respectively.</span></span>

<span data-ttu-id="268ba-119">세 번째 명령은 Rule1 및 Rule2의 규칙을 사용 하 여/Profile 이라는 프로필을 만든 다음이를 $Profile 1 변수로 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="268ba-119">The third command creates a profile named ProfileName using the rules in Rule1 and Rule2, and then stores it in the $Profile1 variable.</span></span>

<span data-ttu-id="268ba-120">마지막 명령은 Rule1 및 Rule2의 규칙을 사용 하 여 SecondProfileName 이라는 프로필을 만든 다음이를 $Profile 2 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="268ba-120">The final command creates a profile named SecondProfileName using the rules in Rule1 and Rule2, and then stores it in the $Profile2 variable.</span></span>

### <span data-ttu-id="268ba-121">예제 4: 일정이 나 고정 된 날짜 없이 프로필 만들기</span><span class="sxs-lookup"><span data-stu-id="268ba-121">Example 4: Create a profile with no schedule or fixed date</span></span>
```
PS C:\>$Rule = New-AzureRmAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1" 

PS C:\> $Profile = New-AzureRmAutoscaleProfile -DefaultCapacity "1" -MaximumCapacity "10" -MinimumCapacity "1" -Rules $Rule -Name "ProfileName"
```

<span data-ttu-id="268ba-122">첫 번째 명령은 요청 이라는 자동 크기 조정 규칙을 만든 다음이를 $Rule 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="268ba-122">The first command creates an Autoscale rule named Requests, and then stores it in the $Rule variable.</span></span>

<span data-ttu-id="268ba-123">두 번째 명령은 일정 또는 고정 날짜 없이 프로필을 만든 다음 $Profile 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="268ba-123">The second command creates a profile without a schedule or a fixed date, and then stores it in the $Profile variable.</span></span>

## <span data-ttu-id="268ba-124">변수</span><span class="sxs-lookup"><span data-stu-id="268ba-124">PARAMETERS</span></span>

### <span data-ttu-id="268ba-125">-DefaultCapacity</span><span class="sxs-lookup"><span data-stu-id="268ba-125">-DefaultCapacity</span></span>
<span data-ttu-id="268ba-126">기본 용량을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="268ba-126">Specifies the default capacity.</span></span>

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

### <span data-ttu-id="268ba-127">-EndTimeWindow</span><span class="sxs-lookup"><span data-stu-id="268ba-127">-EndTimeWindow</span></span>
<span data-ttu-id="268ba-128">시간 창의 끝을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="268ba-128">Specifies the end of the time window.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: Parameters for New-AzureRmAutoscaleProfile cmdlet using fix date scheduling
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="268ba-129">-MaximumCapacity</span><span class="sxs-lookup"><span data-stu-id="268ba-129">-MaximumCapacity</span></span>
<span data-ttu-id="268ba-130">최대 용량을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="268ba-130">Specifies the maximum capacity.</span></span>

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

### <span data-ttu-id="268ba-131">-가을 용량</span><span class="sxs-lookup"><span data-stu-id="268ba-131">-MinimumCapacity</span></span>
<span data-ttu-id="268ba-132">최소 용량을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="268ba-132">Specifies the minimum capacity.</span></span>

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

### <span data-ttu-id="268ba-133">-이름</span><span class="sxs-lookup"><span data-stu-id="268ba-133">-Name</span></span>
<span data-ttu-id="268ba-134">만들 프로필의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="268ba-134">Specifies the name of the profile to create.</span></span>

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

### <span data-ttu-id="268ba-135">-RecurrenceFrequency</span><span class="sxs-lookup"><span data-stu-id="268ba-135">-RecurrenceFrequency</span></span>
<span data-ttu-id="268ba-136">되풀이 빈도를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="268ba-136">Specifies the frequency of recurrence.</span></span>
<span data-ttu-id="268ba-137">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="268ba-137">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="268ba-138">않아야</span><span class="sxs-lookup"><span data-stu-id="268ba-138">None</span></span>
- <span data-ttu-id="268ba-139">두번째</span><span class="sxs-lookup"><span data-stu-id="268ba-139">Second</span></span>
- <span data-ttu-id="268ba-140">길이의</span><span class="sxs-lookup"><span data-stu-id="268ba-140">Minute</span></span>
- <span data-ttu-id="268ba-141">시간씩</span><span class="sxs-lookup"><span data-stu-id="268ba-141">Hour</span></span>
- <span data-ttu-id="268ba-142">부활절</span><span class="sxs-lookup"><span data-stu-id="268ba-142">Day</span></span>
- <span data-ttu-id="268ba-143">이번</span><span class="sxs-lookup"><span data-stu-id="268ba-143">Week</span></span>
- <span data-ttu-id="268ba-144">달은</span><span class="sxs-lookup"><span data-stu-id="268ba-144">Month</span></span>
- <span data-ttu-id="268ba-145">반기</span><span class="sxs-lookup"><span data-stu-id="268ba-145">Year</span></span>

<span data-ttu-id="268ba-146">이러한 값 중 일부는 지원 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="268ba-146">Not all of these values are supported.</span></span>

```yaml
Type: Microsoft.Azure.Management.Monitor.Management.Models.RecurrenceFrequency
Parameter Sets: Parameters for New-AzureRmAutoscaleProfile cmdlet using recurrent scheduling
Aliases: 
Accepted values: None, Second, Minute, Hour, Day, Week, Month, Year

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="268ba-147">-규칙</span><span class="sxs-lookup"><span data-stu-id="268ba-147">-Rules</span></span>
<span data-ttu-id="268ba-148">프로필에 추가할 규칙 목록을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="268ba-148">Specifies the list of rules to add to the profile.</span></span>

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

### <span data-ttu-id="268ba-149">-ScheduleDays</span><span class="sxs-lookup"><span data-stu-id="268ba-149">-ScheduleDays</span></span>
<span data-ttu-id="268ba-150">예정 된 날짜를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="268ba-150">Specifies the scheduled days.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: Parameters for New-AzureRmAutoscaleProfile cmdlet using recurrent scheduling
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="268ba-151">-ScheduleHours</span><span class="sxs-lookup"><span data-stu-id="268ba-151">-ScheduleHours</span></span>
<span data-ttu-id="268ba-152">예약 된 시간을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="268ba-152">Specifies the scheduled hours.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.Nullable`1[System.Int32]]
Parameter Sets: Parameters for New-AzureRmAutoscaleProfile cmdlet using recurrent scheduling
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="268ba-153">-ScheduleMinutes</span><span class="sxs-lookup"><span data-stu-id="268ba-153">-ScheduleMinutes</span></span>
<span data-ttu-id="268ba-154">예정 된 시간 (분)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="268ba-154">Specifies the scheduled minutes.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.Nullable`1[System.Int32]]
Parameter Sets: Parameters for New-AzureRmAutoscaleProfile cmdlet using recurrent scheduling
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="268ba-155">-ScheduleTimeZone</span><span class="sxs-lookup"><span data-stu-id="268ba-155">-ScheduleTimeZone</span></span>
<span data-ttu-id="268ba-156">일정의 시간대를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="268ba-156">Specifies the time zone of the schedule.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameters for New-AzureRmAutoscaleProfile cmdlet using recurrent scheduling
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="268ba-157">-StartTimeWindow</span><span class="sxs-lookup"><span data-stu-id="268ba-157">-StartTimeWindow</span></span>
<span data-ttu-id="268ba-158">시간 창의 시작을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="268ba-158">Specifies the start of the time window.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: Parameters for New-AzureRmAutoscaleProfile cmdlet using fix date scheduling
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="268ba-159">타임 창 표준 시간대</span><span class="sxs-lookup"><span data-stu-id="268ba-159">-TimeWindowTimeZone</span></span>
<span data-ttu-id="268ba-160">시간 창의 표준 시간대를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="268ba-160">Specifies the time zone of the time window.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameters for New-AzureRmAutoscaleProfile cmdlet using fix date scheduling
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="268ba-161">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="268ba-161">-DefaultProfile</span></span>
<span data-ttu-id="268ba-162">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="268ba-162">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="268ba-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="268ba-163">CommonParameters</span></span>
<span data-ttu-id="268ba-164">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="268ba-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="268ba-165">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="268ba-165">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="268ba-166">입력</span><span class="sxs-lookup"><span data-stu-id="268ba-166">INPUTS</span></span>

## <span data-ttu-id="268ba-167">출력</span><span class="sxs-lookup"><span data-stu-id="268ba-167">OUTPUTS</span></span>

### <span data-ttu-id="268ba-168">AutoscaleProfile를 통해 관리 합니다.</span><span class="sxs-lookup"><span data-stu-id="268ba-168">Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleProfile</span></span>

## <span data-ttu-id="268ba-169">상속자</span><span class="sxs-lookup"><span data-stu-id="268ba-169">NOTES</span></span>

## <span data-ttu-id="268ba-170">관련 링크</span><span class="sxs-lookup"><span data-stu-id="268ba-170">RELATED LINKS</span></span>

[<span data-ttu-id="268ba-171">추가-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="268ba-171">Add-AzureRmAutoscaleSetting</span></span>](./Add-AzureRmAutoscaleSetting.md)

[<span data-ttu-id="268ba-172">Get-AzureRmAutoscaleHistory</span><span class="sxs-lookup"><span data-stu-id="268ba-172">Get-AzureRmAutoscaleHistory</span></span>](./Get-AzureRmAutoscaleHistory.md)

[<span data-ttu-id="268ba-173">Get-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="268ba-173">Get-AzureRmAutoscaleSetting</span></span>](./Get-AzureRmAutoscaleSetting.md)

[<span data-ttu-id="268ba-174">새로운 AzureRmAutoscaleRule</span><span class="sxs-lookup"><span data-stu-id="268ba-174">New-AzureRmAutoscaleRule</span></span>](./New-AzureRmAutoscaleRule.md)

[<span data-ttu-id="268ba-175">제거-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="268ba-175">Remove-AzureRmAutoscaleSetting</span></span>](./Remove-AzureRmAutoscaleSetting.md)


