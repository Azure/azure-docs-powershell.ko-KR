---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 717023DA-AA2D-4F1B-AE46-67ED75AA0D15
online version: ''
schema: 2.0.0
ms.openlocfilehash: b6d8dae704946680dd72ff8227d2a88d55f8b77a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046271"
---
# <span data-ttu-id="30345-101">Get-AzureWebsiteMetric</span><span class="sxs-lookup"><span data-stu-id="30345-101">Get-AzureWebsiteMetric</span></span>

## <span data-ttu-id="30345-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="30345-102">SYNOPSIS</span></span>
<span data-ttu-id="30345-103">현재 구독의 Azure 웹 사이트에 대 한 메트릭을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="30345-103">Gets metrics for the Azure website in the current subscription.</span></span>

## <span data-ttu-id="30345-104">구문과</span><span class="sxs-lookup"><span data-stu-id="30345-104">SYNTAX</span></span>

```
Get-AzureWebsiteMetric [-MetricNames <String[]>] [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-TimeGrain <String>] [-InstanceDetails] [-SlotView] [-Name <String>] [-Slot <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="30345-105">설명은</span><span class="sxs-lookup"><span data-stu-id="30345-105">DESCRIPTION</span></span>
<span data-ttu-id="30345-106">이 항목에서는 0.8.10 버전의 Microsoft Azure PowerShell 모듈에 대 한 cmdlet에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="30345-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="30345-107">사용 중인 모듈 버전을 Azure PowerShell 콘솔에 가져오려면 다음을 입력 `(Get-Module -Name Azure).Version` 합니다.</span><span class="sxs-lookup"><span data-stu-id="30345-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="30345-108">**AzureWebsiteMetric** cmdlet은 현재 구독의 Azure 웹 사이트에 대 한 메트릭을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="30345-108">The **Get-AzureWebsiteMetric** cmdlet gets metrics for the Azure website in the current subscription.</span></span>

## <span data-ttu-id="30345-109">예제의</span><span class="sxs-lookup"><span data-stu-id="30345-109">EXAMPLES</span></span>

### <span data-ttu-id="30345-110">예제 1: 웹 사이트의 인스턴스 별 수준에서 지난 3 시간에 대 한 메트릭 가져오기</span><span class="sxs-lookup"><span data-stu-id="30345-110">Example 1: Get metrics for the last three hours on a per-instance level for a website</span></span>
```
PS C:\> Get-AzureWebsiteMetric -Name "ContosoWebSite" -StartDate (get-date).AddHours(-3) -MetricNames "Requests" -InstanceDetails -SlotView -TimeGrain "PT1M" 
PS C:\> $metrics[1].Data Name : Requests 

Unit : Count 

StartTime : 8/11/2014 7:05:00 AM 

EndTime : 8/11/2014 5:06:01 PM 

TimeGrain : PT1M 
PrimaryAggregationType : Instance 
Values : {Time:8/11/2014 7:05:00 AM, Total:4, Min:, Max:, Time:8/11/2014 7:06:00 AM, Total:3, Min:, Max:, 
Time:8/11/2014 7:07:00 AM, Total:3, Min:, Max:, Time:8/11/2014 7:08:00 AM, Total:12, Min:, Max:...} 
$metrics[1].Data.Values | ft 
TimeCreated Total Minimum Maximum Count InstanceName 
----------- ----- ------- ------- ----- ------------ 
8/11/2014 7:05:00 AM 4 1 RD00155DC24599 
8/11/2014 7:06:00 AM 3 1 RD00155DC24599 
8/11/2014 7:07:00 AM 3 1 RD00155DC24589 
8/11/2014 7:08:00 AM 12 1 RD00155DC24599
8/11/2014 7:09:00 AM 37 1 RD00155DC24599 
8/11/2014 7:10:00 AM 9 1 RD00155DC24599
```

<span data-ttu-id="30345-111">이 명령은 웹 사이트의 인스턴스 당 수준에서 지난 3 시간에 대 한 메트릭을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="30345-111">This command gets metrics for the last three hours on a per-instance level for a website.</span></span>

## <span data-ttu-id="30345-112">변수</span><span class="sxs-lookup"><span data-stu-id="30345-112">PARAMETERS</span></span>

### <span data-ttu-id="30345-113">-EndDate</span><span class="sxs-lookup"><span data-stu-id="30345-113">-EndDate</span></span>
<span data-ttu-id="30345-114">시간을 **DateTime** 개체로 지정 하 여 메트릭 가져오기를 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="30345-114">Specifies the time, as a **DateTime** object, to stop getting metrics.</span></span>
<span data-ttu-id="30345-115">**DateTime** 개체를 가져오려면 **날짜 가져오기** cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="30345-115">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span>
<span data-ttu-id="30345-116">자세한 내용은을 입력 `Get-Help Get-Date` 하세요.</span><span class="sxs-lookup"><span data-stu-id="30345-116">For more information, type `Get-Help Get-Date`.</span></span>

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

### <span data-ttu-id="30345-117">-InstanceDetails</span><span class="sxs-lookup"><span data-stu-id="30345-117">-InstanceDetails</span></span>
<span data-ttu-id="30345-118">이 cmdlet에 인스턴스별 수준에 대 한 세부 정보가 포함 되어 있음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="30345-118">Indicates that this cmdlet includes details on a per-instance level.</span></span>
<span data-ttu-id="30345-119">웹 호스팅 계획이 두 대 이상의 컴퓨터에서 실행 되는 경우이 cmdlet은 각 컴퓨터에 대 한 메트릭을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="30345-119">If the web hosting plan runs on two or more computers, this cmdlet returns metrics for each computer.</span></span>

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

### <span data-ttu-id="30345-120">-MetricNames</span><span class="sxs-lookup"><span data-stu-id="30345-120">-MetricNames</span></span>
<span data-ttu-id="30345-121">가져올 메트릭의 배열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="30345-121">Specifies an array of metrics to get.</span></span>
<span data-ttu-id="30345-122">이 매개 변수를 지정 하지 않으면 cmdlet에서 모든 메트릭을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="30345-122">If you do not specify this parameter, the cmdlet gets all metrics.</span></span>

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

### <span data-ttu-id="30345-123">-이름</span><span class="sxs-lookup"><span data-stu-id="30345-123">-Name</span></span>
<span data-ttu-id="30345-124">구독에서 웹 사이트의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="30345-124">Specifies the name of a website in the subscription.</span></span>
<span data-ttu-id="30345-125">이 매개 변수는 와일드 카드 문자를 지원 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="30345-125">This parameter does not support wildcard characters.</span></span>

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

### <span data-ttu-id="30345-126">-프로필</span><span class="sxs-lookup"><span data-stu-id="30345-126">-Profile</span></span>
<span data-ttu-id="30345-127">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="30345-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="30345-128">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="30345-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="30345-129">-슬롯</span><span class="sxs-lookup"><span data-stu-id="30345-129">-Slot</span></span>
<span data-ttu-id="30345-130">클라우드 서비스 배포 환경을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="30345-130">Specifies the environment of a cloud service deployment.</span></span>
<span data-ttu-id="30345-131">유효한 값은 프로덕션 및 준비입니다.</span><span class="sxs-lookup"><span data-stu-id="30345-131">Valid values are: Production and Staging.</span></span>

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

### <span data-ttu-id="30345-132">-SlotView</span><span class="sxs-lookup"><span data-stu-id="30345-132">-SlotView</span></span>
<span data-ttu-id="30345-133">이 cmdlet이 현재 슬롯에서 트래픽을 수신 하는 호스트 이름에 대 한 메트릭을 가져와 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="30345-133">Indicates that this cmdlet gets metrics for the host names that receive traffic at the current slot.</span></span>
<span data-ttu-id="30345-134">특정 기간 동안 교체가 발생 하는 경우 메트릭이 병합 됩니다.</span><span class="sxs-lookup"><span data-stu-id="30345-134">If a swap occurs during the time period, the metrics are merged.</span></span>

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

### <span data-ttu-id="30345-135">-시작 날짜</span><span class="sxs-lookup"><span data-stu-id="30345-135">-StartDate</span></span>
<span data-ttu-id="30345-136">시간을 **DateTime** 개체로 지정 하 고 메트릭을 가져오는 데 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="30345-136">Specifies the time, as a **DateTime** object, to start getting metrics.</span></span>

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

### <span data-ttu-id="30345-137">-TimeGrain</span><span class="sxs-lookup"><span data-stu-id="30345-137">-TimeGrain</span></span>
<span data-ttu-id="30345-138">메트릭의 시간 단위를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="30345-138">Specifies the time unit for metrics.</span></span>
<span data-ttu-id="30345-139">유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="30345-139">Valid values are:</span></span> 

- <span data-ttu-id="30345-140">PT1M (분)</span><span class="sxs-lookup"><span data-stu-id="30345-140">PT1M (Minute)</span></span> 
- <span data-ttu-id="30345-141">PT1H (시간)</span><span class="sxs-lookup"><span data-stu-id="30345-141">PT1H (Hour)</span></span> 
- <span data-ttu-id="30345-142">P1D (일)</span><span class="sxs-lookup"><span data-stu-id="30345-142">P1D (Day)</span></span>

<span data-ttu-id="30345-143">기본 값은 PT1H입니다.</span><span class="sxs-lookup"><span data-stu-id="30345-143">The default value is PT1H.</span></span>

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

### <span data-ttu-id="30345-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30345-144">CommonParameters</span></span>
<span data-ttu-id="30345-145">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="30345-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30345-146">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="30345-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30345-147">입력</span><span class="sxs-lookup"><span data-stu-id="30345-147">INPUTS</span></span>

###  
<span data-ttu-id="30345-148">속성 이름으로이 cmdlet에 대 한 입력을 전달할 수 있지만 값을 기준으로 하지는 않습니다.</span><span class="sxs-lookup"><span data-stu-id="30345-148">You can pass input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="30345-149">출력</span><span class="sxs-lookup"><span data-stu-id="30345-149">OUTPUTS</span></span>

### <span data-ttu-id="30345-150">WindowsAzure. MetricResponse에 대 한 유틸리티.</span><span class="sxs-lookup"><span data-stu-id="30345-150">Microsoft.WindowsAzure.Commands.Utilities.Websites.Services.WebEntities.MetricResponse</span></span>
<span data-ttu-id="30345-151">기본적으로 **Get-AzureWebsiteMetric** 는 **MetricResponse** 개체의 배열을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="30345-151">By default, **Get-AzureWebsiteMetric** returns an array of **MetricResponse** objects.</span></span>

## <span data-ttu-id="30345-152">상속자</span><span class="sxs-lookup"><span data-stu-id="30345-152">NOTES</span></span>

## <span data-ttu-id="30345-153">관련 링크</span><span class="sxs-lookup"><span data-stu-id="30345-153">RELATED LINKS</span></span>

[<span data-ttu-id="30345-154">Get-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="30345-154">Get-AzureWebsite</span></span>](./Get-AzureWebsite.md)


