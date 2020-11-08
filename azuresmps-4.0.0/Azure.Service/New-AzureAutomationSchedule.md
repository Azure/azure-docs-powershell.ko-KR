---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: D28DD808-E8EF-4C71-A353-8BF1E458DF6F
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9fcae4a0232331a020a716b3f7284b8f6dfc3212
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046219"
---
# <span data-ttu-id="39efb-101">New-AzureAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="39efb-101">New-AzureAutomationSchedule</span></span>

## <span data-ttu-id="39efb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="39efb-102">SYNOPSIS</span></span>

<span data-ttu-id="39efb-103">자동화 일정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="39efb-103">Creates an Automation schedule.</span></span>

## <span data-ttu-id="39efb-104">구문과</span><span class="sxs-lookup"><span data-stu-id="39efb-104">SYNTAX</span></span>

### <span data-ttu-id="39efb-105">일별 (기본값)</span><span class="sxs-lookup"><span data-stu-id="39efb-105">ByDaily (Default)</span></span>
```
New-AzureAutomationSchedule -Name <String> -StartTime <DateTimeOffset> [-Description <String>]
 [-ExpiryTime <DateTimeOffset>] -DayInterval <Byte> -AutomationAccountName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="39efb-106">ByOneTime</span><span class="sxs-lookup"><span data-stu-id="39efb-106">ByOneTime</span></span>
```
New-AzureAutomationSchedule -Name <String> -StartTime <DateTimeOffset> [-Description <String>] [-OneTime]
 -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="39efb-107">매 시간</span><span class="sxs-lookup"><span data-stu-id="39efb-107">ByHourly</span></span>
```
New-AzureAutomationSchedule -Name <String> -StartTime <DateTimeOffset> [-Description <String>]
 [-ExpiryTime <DateTimeOffset>] -HourInterval <Byte> -AutomationAccountName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="39efb-108">설명은</span><span class="sxs-lookup"><span data-stu-id="39efb-108">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="39efb-109">**새-AzureAutomationSchedule** Cmdlet은 Microsoft Azure 자동화에서 일정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="39efb-109">The **New-AzureAutomationSchedule** cmdlet creates a schedule in Microsoft Azure Automation.</span></span>

## <span data-ttu-id="39efb-110">예제의</span><span class="sxs-lookup"><span data-stu-id="39efb-110">EXAMPLES</span></span>

### <span data-ttu-id="39efb-111">예제 1: 일회성 일정 만들기</span><span class="sxs-lookup"><span data-stu-id="39efb-111">Example 1: Create a one-time schedule</span></span>
```
PS C:\> New-AzureAutomationSchedule -AutomationAccountName "Contoso17" -Name "Schedule01" -StartTime "23:00" -OneTime
```

<span data-ttu-id="39efb-112">다음 명령은 11:00 PM에서 현재 날짜에 한 번 실행 되는 일정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="39efb-112">The following command creates a schedule that runs one time on the current date at 11:00 PM.</span></span>

### <span data-ttu-id="39efb-113">예제 2: 되풀이 일정 만들기</span><span class="sxs-lookup"><span data-stu-id="39efb-113">Example 2: Create a recurring schedule</span></span>
```
PS C:\> $StartTime = Get-Date "13:00:00"
PS C:\> $EndTime = $StartTime.AddYears(1)
PS C:\> New-AzureAutomationSchedule -AutomationAccountName "Contoso17" -Name "Schedule02" -StartTime $StartTime -ExpiryTime $EndTime -DailyInterval 1
```

<span data-ttu-id="39efb-114">다음 명령은 현재 날짜부터 1 년 동안 매일 1:00 PM에 실행 되는 새 일정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="39efb-114">The following commands create a new schedule that runs at 1:00 PM every day for one year starting on the current day.</span></span>

## <span data-ttu-id="39efb-115">변수</span><span class="sxs-lookup"><span data-stu-id="39efb-115">PARAMETERS</span></span>

### <span data-ttu-id="39efb-116">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="39efb-116">-AutomationAccountName</span></span>
<span data-ttu-id="39efb-117">Automation 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="39efb-117">Specifies the name of an Automation account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="39efb-118">-DayInterval</span><span class="sxs-lookup"><span data-stu-id="39efb-118">-DayInterval</span></span>
<span data-ttu-id="39efb-119">일정에 대 한 간격 (일)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="39efb-119">Specifies an interval, in days, for the schedule.</span></span>

```yaml
Type: Byte
Parameter Sets: ByDaily
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39efb-120">-설명</span><span class="sxs-lookup"><span data-stu-id="39efb-120">-Description</span></span>
<span data-ttu-id="39efb-121">설명을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="39efb-121">Specifies a description.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="39efb-122">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="39efb-122">-ExpiryTime</span></span>
<span data-ttu-id="39efb-123">일정의 만료 시간을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="39efb-123">Specifies the expiry time of a schedule.</span></span>
<span data-ttu-id="39efb-124">유효한 **날짜/시간** 으로 변환할 수 있는 경우 문자열을 제공할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="39efb-124">A string can be provided if it can be converted to a valid **DateTime**.</span></span>

```yaml
Type: DateTimeOffset
Parameter Sets: ByDaily, ByHourly
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39efb-125">-HourInterval</span><span class="sxs-lookup"><span data-stu-id="39efb-125">-HourInterval</span></span>
<span data-ttu-id="39efb-126">일정에 대 한 간격 (시간)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="39efb-126">Specifies an interval, in hours, for the schedule.</span></span>

```yaml
Type: Byte
Parameter Sets: ByHourly
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39efb-127">-이름</span><span class="sxs-lookup"><span data-stu-id="39efb-127">-Name</span></span>
<span data-ttu-id="39efb-128">일정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="39efb-128">Specifies a name for the schedule.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="39efb-129">-OneTime</span><span class="sxs-lookup"><span data-stu-id="39efb-129">-OneTime</span></span>
<span data-ttu-id="39efb-130">이 작업으로 일회성 일정이 생성 됨을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="39efb-130">Indicates that this operation creates a one-time schedule.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ByOneTime
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39efb-131">-프로필</span><span class="sxs-lookup"><span data-stu-id="39efb-131">-Profile</span></span>
<span data-ttu-id="39efb-132">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="39efb-132">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="39efb-133">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="39efb-133">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39efb-134">-StartTime</span><span class="sxs-lookup"><span data-stu-id="39efb-134">-StartTime</span></span>
<span data-ttu-id="39efb-135">일정 시작 시간을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="39efb-135">Specifies the start time of a schedule.</span></span>
<span data-ttu-id="39efb-136">유효한 **날짜/시간** 으로 변환할 수 있는 경우 문자열을 제공할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="39efb-136">A string can be provided if it can be converted to a valid **DateTime**.</span></span>

```yaml
Type: DateTimeOffset
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="39efb-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39efb-137">CommonParameters</span></span>
<span data-ttu-id="39efb-138">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="39efb-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39efb-139">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="39efb-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39efb-140">입력</span><span class="sxs-lookup"><span data-stu-id="39efb-140">INPUTS</span></span>

## <span data-ttu-id="39efb-141">출력</span><span class="sxs-lookup"><span data-stu-id="39efb-141">OUTPUTS</span></span>

### <span data-ttu-id="39efb-142">Microsoft Azure. 명령. 일정</span><span class="sxs-lookup"><span data-stu-id="39efb-142">Microsoft.Azure.Commands.Automation.Model.Schedule</span></span>

## <span data-ttu-id="39efb-143">상속자</span><span class="sxs-lookup"><span data-stu-id="39efb-143">NOTES</span></span>

## <span data-ttu-id="39efb-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="39efb-144">RELATED LINKS</span></span>

[<span data-ttu-id="39efb-145">다운로드-AzureAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="39efb-145">Get-AzureAutomationSchedule</span></span>](./Get-AzureAutomationSchedule.md)

[<span data-ttu-id="39efb-146">-AzureAutomationSchedule 제거</span><span class="sxs-lookup"><span data-stu-id="39efb-146">Remove-AzureAutomationSchedule</span></span>](./Remove-AzureAutomationSchedule.md)

[<span data-ttu-id="39efb-147">Set-AzureAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="39efb-147">Set-AzureAutomationSchedule</span></span>](./Set-AzureAutomationSchedule.md)


