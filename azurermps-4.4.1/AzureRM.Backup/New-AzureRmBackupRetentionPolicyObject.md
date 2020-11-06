---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 9574CEB5-B699-4606-8C5E-CE2C0D01092D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/New-AzureRmBackupRetentionPolicyObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/New-AzureRmBackupRetentionPolicyObject.md
ms.openlocfilehash: 3637709ca347a8e00433f247c80ec1c916e42017
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93528283"
---
# <span data-ttu-id="0d9ce-101">New-AzureRmBackupRetentionPolicyObject</span><span class="sxs-lookup"><span data-stu-id="0d9ce-101">New-AzureRmBackupRetentionPolicyObject</span></span>

## <span data-ttu-id="0d9ce-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0d9ce-102">SYNOPSIS</span></span>
<span data-ttu-id="0d9ce-103">백업 보존 정책을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="0d9ce-103">Creates a Backup retention policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0d9ce-104">구문과</span><span class="sxs-lookup"><span data-stu-id="0d9ce-104">SYNTAX</span></span>

### <span data-ttu-id="0d9ce-105">DailyRetentionParamSet</span><span class="sxs-lookup"><span data-stu-id="0d9ce-105">DailyRetentionParamSet</span></span>
```
New-AzureRmBackupRetentionPolicyObject [-DailyRetention] -Retention <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0d9ce-106">WeeklyRetentionParamSet</span><span class="sxs-lookup"><span data-stu-id="0d9ce-106">WeeklyRetentionParamSet</span></span>
```
New-AzureRmBackupRetentionPolicyObject [-WeeklyRetention] -DaysOfWeek <String[]> -Retention <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0d9ce-107">Monthly Yformatoneset</span><span class="sxs-lookup"><span data-stu-id="0d9ce-107">MonthlyRetentionInDailyFormatParamSet</span></span>
```
New-AzureRmBackupRetentionPolicyObject [-MonthlyRetentionInDailyFormat]
 -DaysOfMonth <System.Collections.Generic.List`1[System.String]> -Retention <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0d9ce-108">MonthlyRetentionInWeeklyFormatParamSet</span><span class="sxs-lookup"><span data-stu-id="0d9ce-108">MonthlyRetentionInWeeklyFormatParamSet</span></span>
```
New-AzureRmBackupRetentionPolicyObject [-MonthlyRetentionInWeeklyFormat] -DaysOfWeek <String[]>
 -WeekNumber <String[]> -Retention <Int32> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0d9ce-109">YearlyRetentionInDailyFormatParamSet</span><span class="sxs-lookup"><span data-stu-id="0d9ce-109">YearlyRetentionInDailyFormatParamSet</span></span>
```
New-AzureRmBackupRetentionPolicyObject [-YearlyRetentionInDailyFormat]
 -DaysOfMonth <System.Collections.Generic.List`1[System.String]> -MonthsOfYear <String[]> -Retention <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0d9ce-110">YearlyRetentionInWeeklyFormatParamSet</span><span class="sxs-lookup"><span data-stu-id="0d9ce-110">YearlyRetentionInWeeklyFormatParamSet</span></span>
```
New-AzureRmBackupRetentionPolicyObject [-YearlyRetentionInWeeklyFormat] -DaysOfWeek <String[]>
 -WeekNumber <String[]> -MonthsOfYear <String[]> -Retention <Int32> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0d9ce-111">설명은</span><span class="sxs-lookup"><span data-stu-id="0d9ce-111">DESCRIPTION</span></span>
<span data-ttu-id="0d9ce-112">**새 AzureRmBackupRetentionPolicyObject** Cmdlet은 Azure 백업 보존 정책을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="0d9ce-112">The **New-AzureRmBackupRetentionPolicyObject** cmdlet creates an Azure Backup retention policy.</span></span>
<span data-ttu-id="0d9ce-113">보존 정책은 백업이 얼마나 오래 복구 지점을 유지 하는 정도를 정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="0d9ce-113">A retention policy defines how long Backup keeps a recovery point.</span></span>
<span data-ttu-id="0d9ce-114">보존 유형은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="0d9ce-114">The types of retention are the following:</span></span> 

- <span data-ttu-id="0d9ce-115">Daily</span><span class="sxs-lookup"><span data-stu-id="0d9ce-115">Daily</span></span> 
- <span data-ttu-id="0d9ce-116">매주</span><span class="sxs-lookup"><span data-stu-id="0d9ce-116">Weekly</span></span> 
- <span data-ttu-id="0d9ce-117">월간</span><span class="sxs-lookup"><span data-stu-id="0d9ce-117">Monthly</span></span> 
- <span data-ttu-id="0d9ce-118">연도별</span><span class="sxs-lookup"><span data-stu-id="0d9ce-118">Yearly</span></span> 

<span data-ttu-id="0d9ce-119">사용할 각 보존 유형에 대해 하나의 보존 정책을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="0d9ce-119">Create one retention policy for each type of retention that you plan to use.</span></span>

<span data-ttu-id="0d9ce-120">백업 정책은 하나 이상의 보존 정책에 연결 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0d9ce-120">A backup policy is associated with at least one retention policy.</span></span>
<span data-ttu-id="0d9ce-121">백업 정책을 만들려면 New-AzureRmBackupProtectionPolicy cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="0d9ce-121">To create a backup policy, use the New-AzureRmBackupProtectionPolicy cmdlet.</span></span>
<span data-ttu-id="0d9ce-122">대신 Enable-AzureRmBackupProtection cmdlet에 보존 정책을 제공할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0d9ce-122">You can instead provide a retention policy to the Enable-AzureRmBackupProtection cmdlet.</span></span>

## <span data-ttu-id="0d9ce-123">예제의</span><span class="sxs-lookup"><span data-stu-id="0d9ce-123">EXAMPLES</span></span>

### <span data-ttu-id="0d9ce-124">예제 1: 일일 보존을 위한 보존 정책 만들기</span><span class="sxs-lookup"><span data-stu-id="0d9ce-124">Example 1: Create a retention policy for daily retention</span></span>
```
PS C:\>$Daily = New-AzureRmBackupRetentionPolicyObject -DailyRetention -Retention 30
PS C:\> $Daily
RetentionType      Retention          RetentionTimes
-------------      ---------          --------------
Daily              30
```

<span data-ttu-id="0d9ce-125">첫 번째 명령은 일일 보존 기간에 30 일간 보존 정책을 만든 다음 $Daily 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="0d9ce-125">The first command creates a retention policy for 30 days of daily retention, and then stores it in the $Daily variable.</span></span>

<span data-ttu-id="0d9ce-126">두 번째 명령은 $Daily의 내용을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="0d9ce-126">The second command displays the contents of $Daily.</span></span>

### <span data-ttu-id="0d9ce-127">예제 2: 월 보존 정책 만들기</span><span class="sxs-lookup"><span data-stu-id="0d9ce-127">Example 2: Create a monthly retention policy</span></span>
```
PS C:\>$Monthly = New-AzureRmBackupRetentionPolicyObject -MonthlyRetentionInDailyFormat -DaysOfMonth (10, 20) -Retention 12
PS C:\> $Monthly | select *
RetentionFormat : Daily
DaysOfMonth     : {10, 20}
WeekNumber      : 
DaysOfWeek      : 
RetentionType   : Monthly
Retention       : 12
RetentionTimes  :
```

<span data-ttu-id="0d9ce-128">첫 번째 명령은 12 개월 동안 각 월의 10 번째 백업을 유지 하는 보존 정책을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="0d9ce-128">The first command creates a retention policy that keeps the backup on the tenth and the twentieth of each month for twelve months.</span></span>
<span data-ttu-id="0d9ce-129">명령은 보존 정책을 $Monthly 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="0d9ce-129">The command stores the retention policy in the $Monthly variable.</span></span>

<span data-ttu-id="0d9ce-130">두 번째 명령은 $Monthly의 내용을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="0d9ce-130">The second command displays the contents of $Monthly.</span></span>

## <span data-ttu-id="0d9ce-131">변수</span><span class="sxs-lookup"><span data-stu-id="0d9ce-131">PARAMETERS</span></span>

### <span data-ttu-id="0d9ce-132">-DailyRetention</span><span class="sxs-lookup"><span data-stu-id="0d9ce-132">-DailyRetention</span></span>
<span data-ttu-id="0d9ce-133">이 cmdlet이 일일 보존 정책을 생성 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="0d9ce-133">Indicates that this cmdlet creates a Daily retention policy.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DailyRetentionParamSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d9ce-134">-DaysOfMonth</span><span class="sxs-lookup"><span data-stu-id="0d9ce-134">-DaysOfMonth</span></span>
<span data-ttu-id="0d9ce-135">백업 보존 기간을 식별 하는 월의 날짜와 기간을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0d9ce-135">Specifies the days of the month that identify which recovery points Backup retains and for how long.</span></span>
<span data-ttu-id="0d9ce-136">이 매개 변수에 허용 되는 값은 1부터 28 까지의 정수입니다.</span><span class="sxs-lookup"><span data-stu-id="0d9ce-136">The acceptable values for this parameter are: integers from 1 through 28 and Last.</span></span>
<span data-ttu-id="0d9ce-137">*DailyRetention* , *monthlyYearlyRetentionInDailyFormat, onind보조 Yformat* 및 *YearlyRetentionInDailyFormat* 매개 변수를 지정 하는 경우이 매개 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0d9ce-137">Specify this parameter if you specify the *DailyRetention* , *MonthlyRetentionInDailyFormat* , and *YearlyRetentionInDailyFormat* parameters.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: MonthlyRetentionInDailyFormatParamSet, YearlyRetentionInDailyFormatParamSet
Aliases: 
Accepted values: 1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13, 14, 15, 16, 17, 18, 19, 20, 21, 22, 23, 24, 25, 26, 27, 28, Last

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d9ce-138">-DaysOfWeek</span><span class="sxs-lookup"><span data-stu-id="0d9ce-138">-DaysOfWeek</span></span>
<span data-ttu-id="0d9ce-139">요일의 배열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0d9ce-139">Specifies an array of days of the week.</span></span>
<span data-ttu-id="0d9ce-140">이 cmdlet이 지정 하는 날짜는 백업이 보존 하는 복구 지점 및 기간을 식별 합니다.</span><span class="sxs-lookup"><span data-stu-id="0d9ce-140">The days that this cmdlet specifies identify which recovery points that Backup retains and for how long.</span></span>
<span data-ttu-id="0d9ce-141">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="0d9ce-141">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="0d9ce-142">월요일</span><span class="sxs-lookup"><span data-stu-id="0d9ce-142">Monday</span></span> 
- <span data-ttu-id="0d9ce-143">시간은</span><span class="sxs-lookup"><span data-stu-id="0d9ce-143">Tuesday</span></span> 
- <span data-ttu-id="0d9ce-144">일</span><span class="sxs-lookup"><span data-stu-id="0d9ce-144">Wednesday</span></span> 
- <span data-ttu-id="0d9ce-145">목요일</span><span class="sxs-lookup"><span data-stu-id="0d9ce-145">Thursday</span></span> 
- <span data-ttu-id="0d9ce-146">금요일</span><span class="sxs-lookup"><span data-stu-id="0d9ce-146">Friday</span></span> 
- <span data-ttu-id="0d9ce-147">토요일</span><span class="sxs-lookup"><span data-stu-id="0d9ce-147">Saturday</span></span> 
- <span data-ttu-id="0d9ce-148">나타내고</span><span class="sxs-lookup"><span data-stu-id="0d9ce-148">Sunday</span></span>

<span data-ttu-id="0d9ce-149">*WeeklyRetention* , *MonthlyRetentionInWeeklyFormat* 및 *YearlyRetentionInWeeklyFormat* 매개 변수를 지정 하는 경우이 매개 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0d9ce-149">Specify this parameter if you specify the *WeeklyRetention* , *MonthlyRetentionInWeeklyFormat* , and *YearlyRetentionInWeeklyFormat* parameters.</span></span>

<span data-ttu-id="0d9ce-150">백업 및 보존을 위해 선택한 요일이 정렬 되어 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="0d9ce-150">Be sure that the days of the week you select for backup and for retention are aligned.</span></span>
<span data-ttu-id="0d9ce-151">예를 들어, 백업이 토요일에 설정 된 경우 보존 정책에도 토요일을 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="0d9ce-151">For example, if your backup is set for Saturdays, the retention policies must also use Saturday.</span></span>

```yaml
Type: System.String[]
Parameter Sets: WeeklyRetentionParamSet, MonthlyRetentionInWeeklyFormatParamSet, YearlyRetentionInWeeklyFormatParamSet
Aliases: 
Accepted values: Monday, Tuesday, Wednesday, Thursday, Friday, Saturday, Sunday

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d9ce-152">-Monthly Yonindformat</span><span class="sxs-lookup"><span data-stu-id="0d9ce-152">-MonthlyRetentionInDailyFormat</span></span>
<span data-ttu-id="0d9ce-153">이 cmdlet이 일일 형식으로 월 정책을 생성 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="0d9ce-153">Indicates that this cmdlet creates a Monthly policy in Daily format.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: MonthlyRetentionInDailyFormatParamSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d9ce-154">-MonthlyRetentionInWeeklyFormat</span><span class="sxs-lookup"><span data-stu-id="0d9ce-154">-MonthlyRetentionInWeeklyFormat</span></span>
<span data-ttu-id="0d9ce-155">이 cmdlet이 주간 형식으로 월 단위 정책을 만드는 것을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="0d9ce-155">Indicates that this cmdlet creates a Monthly policy in Weekly format.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: MonthlyRetentionInWeeklyFormatParamSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d9ce-156">-MonthsOfYear</span><span class="sxs-lookup"><span data-stu-id="0d9ce-156">-MonthsOfYear</span></span>
<span data-ttu-id="0d9ce-157">해당 연도의 월 중 백업을 연간 기준으로 유지 하는 복구 지점이 있는 개월 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0d9ce-157">Specifies which months of the year have the recovery points that Backup retains on a yearly basis.</span></span>
<span data-ttu-id="0d9ce-158">이 매개 변수에 허용 되는 값은: 1 월 또는 2 월 등의 월 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0d9ce-158">The acceptable values for this parameter are: names of months, such as January or February.</span></span>

```yaml
Type: System.String[]
Parameter Sets: YearlyRetentionInDailyFormatParamSet, YearlyRetentionInWeeklyFormatParamSet
Aliases: 
Accepted values: January, February, March, April, May, June, July, August, September, October, November, December

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d9ce-159">-보존</span><span class="sxs-lookup"><span data-stu-id="0d9ce-159">-Retention</span></span>
<span data-ttu-id="0d9ce-160">백업 지점을 저장할 보존 기간을 일, 월 또는 년 단위로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0d9ce-160">Specifies the retention period, in days, months, or years, for which Backup stores a backup point.</span></span>
<span data-ttu-id="0d9ce-161">단위는이 cmdlet이 매일, 매월 또는 매년 보존 옵션을 선택 하는지 여부에 따라 달라 집니다.</span><span class="sxs-lookup"><span data-stu-id="0d9ce-161">The unit depends on whether this cmdlet selects a daily, monthly, or yearly retention option.</span></span>
<span data-ttu-id="0d9ce-162">예를 들어 *DailyRetention* 매개 변수를 지정 하는 경우 cmdlet은 현재 매개 변수를 일 수로 해석 합니다.</span><span class="sxs-lookup"><span data-stu-id="0d9ce-162">For example, if specify the *DailyRetention* parameter, the cmdlet interprets the current parameter as a number of days.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d9ce-163">-WeeklyRetention</span><span class="sxs-lookup"><span data-stu-id="0d9ce-163">-WeeklyRetention</span></span>
<span data-ttu-id="0d9ce-164">이 cmdlet이 주간 보존 정책을 생성 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="0d9ce-164">Indicates that this cmdlet creates a Weekly retention policy.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: WeeklyRetentionParamSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d9ce-165">-WeekNumber</span><span class="sxs-lookup"><span data-stu-id="0d9ce-165">-WeekNumber</span></span>
<span data-ttu-id="0d9ce-166">백업 보존 기간을 식별 하는 월의 주를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0d9ce-166">Specifies the weeks of the month that identify which recovery points Backup retains and for how long.</span></span>
<span data-ttu-id="0d9ce-167">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="0d9ce-167">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="0d9ce-168">기본</span><span class="sxs-lookup"><span data-stu-id="0d9ce-168">First</span></span> 
- <span data-ttu-id="0d9ce-169">두번째</span><span class="sxs-lookup"><span data-stu-id="0d9ce-169">Second</span></span> 
- <span data-ttu-id="0d9ce-170">제 3</span><span class="sxs-lookup"><span data-stu-id="0d9ce-170">Third</span></span> 
- <span data-ttu-id="0d9ce-171">커피</span><span class="sxs-lookup"><span data-stu-id="0d9ce-171">Fourth</span></span> 
- <span data-ttu-id="0d9ce-172">마지막</span><span class="sxs-lookup"><span data-stu-id="0d9ce-172">Last</span></span>

```yaml
Type: System.String[]
Parameter Sets: MonthlyRetentionInWeeklyFormatParamSet, YearlyRetentionInWeeklyFormatParamSet
Aliases: 
Accepted values: First, Second, Third, Fourth, Last

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d9ce-173">-YearlyRetentionInDailyFormat</span><span class="sxs-lookup"><span data-stu-id="0d9ce-173">-YearlyRetentionInDailyFormat</span></span>
<span data-ttu-id="0d9ce-174">이 cmdlet이 일일 형식으로 연간 보존 정책을 생성 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="0d9ce-174">Indicates that this cmdlet creates a Yearly retention policy in Daily format.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: YearlyRetentionInDailyFormatParamSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d9ce-175">-YearlyRetentionInWeeklyFormat</span><span class="sxs-lookup"><span data-stu-id="0d9ce-175">-YearlyRetentionInWeeklyFormat</span></span>
<span data-ttu-id="0d9ce-176">이 cmdlet이 주간 형식으로 연간 보존 정책을 생성 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="0d9ce-176">Indicates that this cmdlet creates a Yearly retention policy in Weekly format.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: YearlyRetentionInWeeklyFormatParamSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d9ce-177">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d9ce-177">-DefaultProfile</span></span>
<span data-ttu-id="0d9ce-178">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0d9ce-178">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0d9ce-179">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d9ce-179">CommonParameters</span></span>
<span data-ttu-id="0d9ce-180">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0d9ce-180">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d9ce-181">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0d9ce-181">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d9ce-182">입력</span><span class="sxs-lookup"><span data-stu-id="0d9ce-182">INPUTS</span></span>

### <span data-ttu-id="0d9ce-183">않아야</span><span class="sxs-lookup"><span data-stu-id="0d9ce-183">None</span></span>

## <span data-ttu-id="0d9ce-184">출력</span><span class="sxs-lookup"><span data-stu-id="0d9ce-184">OUTPUTS</span></span>

### <span data-ttu-id="0d9ce-185">AzureRmBackupRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="0d9ce-185">AzureRmBackupRetentionPolicy</span></span>

## <span data-ttu-id="0d9ce-186">상속자</span><span class="sxs-lookup"><span data-stu-id="0d9ce-186">NOTES</span></span>
* <span data-ttu-id="0d9ce-187">않아야</span><span class="sxs-lookup"><span data-stu-id="0d9ce-187">None</span></span>

## <span data-ttu-id="0d9ce-188">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0d9ce-188">RELATED LINKS</span></span>

[<span data-ttu-id="0d9ce-189">Enable-AzureRmBackupProtection</span><span class="sxs-lookup"><span data-stu-id="0d9ce-189">Enable-AzureRmBackupProtection</span></span>](./Enable-AzureRmBackupProtection.md)

[<span data-ttu-id="0d9ce-190">새로운 AzureRmBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="0d9ce-190">New-AzureRmBackupProtectionPolicy</span></span>](./New-AzureRmBackupProtectionPolicy.md)


