---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 2DEF8B3A-4E91-4D39-AD39-1871F9FECE10
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5a59c93c9de0d2445f2839d9a66f4750751c987f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046510"
---
# <span data-ttu-id="58efc-101">Get-AzureWebHostingPlanMetric</span><span class="sxs-lookup"><span data-stu-id="58efc-101">Get-AzureWebHostingPlanMetric</span></span>

## <span data-ttu-id="58efc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="58efc-102">SYNOPSIS</span></span>
<span data-ttu-id="58efc-103">Azure 웹 사이트 호스팅 계획에 대 한 메트릭을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="58efc-103">Gets metrics for Azure website hosting plans.</span></span>

## <span data-ttu-id="58efc-104">구문과</span><span class="sxs-lookup"><span data-stu-id="58efc-104">SYNTAX</span></span>

```
Get-AzureWebHostingPlanMetric [-MetricNames <String[]>] [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-TimeGrain <String>] [-InstanceDetails] [-WebSpaceName <String>] [-Name <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="58efc-105">설명은</span><span class="sxs-lookup"><span data-stu-id="58efc-105">DESCRIPTION</span></span>
<span data-ttu-id="58efc-106">이 항목에서는 0.8.10 버전의 Microsoft Azure PowerShell 모듈에 대 한 cmdlet에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="58efc-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="58efc-107">사용 중인 모듈 버전을 Azure PowerShell 콘솔에 가져오려면 다음을 입력 `(Get-Module -Name Azure).Version` 합니다.</span><span class="sxs-lookup"><span data-stu-id="58efc-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="58efc-108">**AzureWebHostingPlanMetric** cmdlet은 구독에서 Azure 웹 호스팅 계획에 대 한 메트릭을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="58efc-108">The **Get-AzureWebHostingPlanMetric** cmdlet gets metrics for Azure web hosting plans in a subscription.</span></span>

## <span data-ttu-id="58efc-109">예제의</span><span class="sxs-lookup"><span data-stu-id="58efc-109">EXAMPLES</span></span>

### <span data-ttu-id="58efc-110">예제 1: 인스턴스 당 수준에서 마지막 3 시간에 대 한 메트릭 가져오기</span><span class="sxs-lookup"><span data-stu-id="58efc-110">Example 1: Get metrics for the last three hours at a per-instance level</span></span>
```
PS C:\> Get-AzureWebHostingPlanMetric -WebSpaceName "eastuswebspace" -StartDate (get-date).AddHours(-3) -InstanceDetails $Metrics[1].Data 

Name : CpuPercentage 
Unit : Percent 
StartTime : 8/11/2014 7:00:00 AM 
EndTime : 8/11/2014 5:00:23 PM 
TimeGrain : PT1H 
PrimaryAggregationType : Instance 
Values : {Time:8/11/2014 7:00:00 AM, Total:2, Min:9, Max:0, Time:8/11/2014 8:00:00 AM, Total:2, Min:9, Max:0, 
Time:8/11/2014 9:00:00 AM, Total:2, Min:9, Max:0, Time:8/11/2014 10:00:00 AM, Total:2, Min:8, Max:0...} $metrics[1].Data.Values | ft 
TimeCreated Total Minimum Maximum Count InstanceName
 ----------- ----- ------- ------- ----- ------------ 
8/11/2014 7:00:00 AM 2 9 0 1 RD00155DC24599 
8/11/2014 8:00:00 AM 2 9 0 1 RD00155DC24599 
8/11/2014 9:00:00 AM 2 9 0 1 RD00155DC24579 
8/11/2014 10:00:00 AM 2 8 0 1 RD00155DC24599 
8/11/2014 11:00:00 AM 2 9 0 1 RD00155DC24599 
8/11/2014 12:00:00 PM 2 6 0 1 RD00155DC24599 
8/11/2014 1:00:00 PM 2 15 0 1 RD00155DC24599 
8/11/2014 2:00:00 PM 3 21 0 1 RD00155DC24599 
8/11/2014 3:00:00 PM 2 13 0 1 RD00155DC24599 
8/11/2014 4:00:00 PM 2 14 0 1 RD00155DC24599
```

<span data-ttu-id="58efc-111">이 명령은 인스턴스 단위 수준에서 지난 3 시간 동안 웹 호스팅 계획 메트릭을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="58efc-111">This command gets web hosting plan metrics for last three hours on per-instance level.</span></span>

## <span data-ttu-id="58efc-112">변수</span><span class="sxs-lookup"><span data-stu-id="58efc-112">PARAMETERS</span></span>

### <span data-ttu-id="58efc-113">-EndDate</span><span class="sxs-lookup"><span data-stu-id="58efc-113">-EndDate</span></span>
<span data-ttu-id="58efc-114">메트릭을 반환할 종료 시간을 **DateTime** 개체로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="58efc-114">Specifies the end time, as a **DateTime** object, from which to return metrics.</span></span>
<span data-ttu-id="58efc-115">**DateTime** 개체를 가져오려면 **날짜 가져오기** cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="58efc-115">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span>
<span data-ttu-id="58efc-116">자세한 내용은을 입력 `Get-Help Get-Date` 하세요.</span><span class="sxs-lookup"><span data-stu-id="58efc-116">For more information, type `Get-Help Get-Date`.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="58efc-117">-InstanceDetails</span><span class="sxs-lookup"><span data-stu-id="58efc-117">-InstanceDetails</span></span>
<span data-ttu-id="58efc-118">이 cmdlet에 인스턴스별 수준에 대 한 세부 정보가 포함 되어 있음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="58efc-118">Indicates that this cmdlet includes details on a per-instance level.</span></span>
<span data-ttu-id="58efc-119">두 개 이상의 컴퓨터에서 웹 사이트 호스팅 계획이 실행 되는 경우이 cmdlet은 각 컴퓨터에 대 한 세부 정보 메트릭을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="58efc-119">If the website hosting plan runs on two or more machines, this cmdlet returns details metrics for each machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="58efc-120">-MetricNames</span><span class="sxs-lookup"><span data-stu-id="58efc-120">-MetricNames</span></span>
<span data-ttu-id="58efc-121">가져올 메트릭의 배열을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="58efc-121">Species an array of metrics to get.</span></span>
<span data-ttu-id="58efc-122">이 매개 변수에 대 한 값을 지정 하지 않으면이 cmdlet은 모든 메트릭을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="58efc-122">If you do not specify a value for this parameter, this cmdlet gets all metrics.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="58efc-123">-이름</span><span class="sxs-lookup"><span data-stu-id="58efc-123">-Name</span></span>
<span data-ttu-id="58efc-124">구독에 대 한 계획의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="58efc-124">Specifies the name of a plan in the subscription.</span></span>
<span data-ttu-id="58efc-125">기본적으로 **Get-AzureWebHostingPlanMetric** 는 현재 구독에 있는 모든 웹 사이트를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="58efc-125">By default, **Get-AzureWebHostingPlanMetric** gets all websites in the current subscription.</span></span>
<span data-ttu-id="58efc-126">이 매개 변수는 와일드 카드 문자를 지원 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="58efc-126">This parameter does not support wildcard characters.</span></span>

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

### <span data-ttu-id="58efc-127">-프로필</span><span class="sxs-lookup"><span data-stu-id="58efc-127">-Profile</span></span>
<span data-ttu-id="58efc-128">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="58efc-128">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="58efc-129">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="58efc-129">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="58efc-130">-시작 날짜</span><span class="sxs-lookup"><span data-stu-id="58efc-130">-StartDate</span></span>
<span data-ttu-id="58efc-131">메트릭을 가져올 시작 시간을 **DateTime** 개체로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="58efc-131">Specifies the start time, as a **DateTime** object, for which to get metrics.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="58efc-132">-TimeGrain</span><span class="sxs-lookup"><span data-stu-id="58efc-132">-TimeGrain</span></span>
<span data-ttu-id="58efc-133">메트릭을 가져올 시간 단위를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="58efc-133">Specifies the time unit for which to get metrics.</span></span>
<span data-ttu-id="58efc-134">유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="58efc-134">Valid values are:</span></span> 

- <span data-ttu-id="58efc-135">PT1M (분)</span><span class="sxs-lookup"><span data-stu-id="58efc-135">PT1M (Minute)</span></span> 
- <span data-ttu-id="58efc-136">PT1H (시간)</span><span class="sxs-lookup"><span data-stu-id="58efc-136">PT1H (Hour)</span></span> 
- <span data-ttu-id="58efc-137">P1D (일)</span><span class="sxs-lookup"><span data-stu-id="58efc-137">P1D (Day)</span></span>

<span data-ttu-id="58efc-138">기본 값은 PT1H입니다.</span><span class="sxs-lookup"><span data-stu-id="58efc-138">The default value is PT1H.</span></span>

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

### <span data-ttu-id="58efc-139">-WebSpaceName</span><span class="sxs-lookup"><span data-stu-id="58efc-139">-WebSpaceName</span></span>
<span data-ttu-id="58efc-140">구독에 있는 웹 스페이스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="58efc-140">Specifies the name of a webspace in the subscription.</span></span>
<span data-ttu-id="58efc-141">기본적으로 **Get-AzureWebHostingPlanMetric** 는 현재 구독에 있는 모든 계획을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="58efc-141">By default, **Get-AzureWebHostingPlanMetric** gets all plans in the current subscription.</span></span>
<span data-ttu-id="58efc-142">이 매개 변수는 와일드 카드 문자를 지원 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="58efc-142">This parameter does not support wildcard characters.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: WebSpace

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="58efc-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58efc-143">CommonParameters</span></span>
<span data-ttu-id="58efc-144">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="58efc-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58efc-145">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="58efc-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58efc-146">입력</span><span class="sxs-lookup"><span data-stu-id="58efc-146">INPUTS</span></span>

###  
<span data-ttu-id="58efc-147">속성 이름으로이 cmdlet에 대 한 입력을 전달할 수 있지만 값을 기준으로 하지는 않습니다.</span><span class="sxs-lookup"><span data-stu-id="58efc-147">You can pass input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="58efc-148">출력</span><span class="sxs-lookup"><span data-stu-id="58efc-148">OUTPUTS</span></span>

###  
<span data-ttu-id="58efc-149">WindowsAzure. MetricResponse에 대 한 유틸리티.</span><span class="sxs-lookup"><span data-stu-id="58efc-149">Microsoft.WindowsAzure.Commands.Utilities.Websites.Services.WebEntities.MetricResponse</span></span>

<span data-ttu-id="58efc-150">기본적으로 **Get-AzureWebHostingPlanMetric** 는 **MetricResponse** 개체의 배열을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="58efc-150">By default, **Get-AzureWebHostingPlanMetric** returns an array of **MetricResponse** objects.</span></span>

## <span data-ttu-id="58efc-151">상속자</span><span class="sxs-lookup"><span data-stu-id="58efc-151">NOTES</span></span>

## <span data-ttu-id="58efc-152">관련 링크</span><span class="sxs-lookup"><span data-stu-id="58efc-152">RELATED LINKS</span></span>

[<span data-ttu-id="58efc-153">Get-AzureWebHostingPlan</span><span class="sxs-lookup"><span data-stu-id="58efc-153">Get-AzureWebHostingPlan</span></span>](./Get-AzureWebHostingPlan.md)


