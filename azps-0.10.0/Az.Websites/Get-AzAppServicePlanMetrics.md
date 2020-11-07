---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: 0AC0C4F9-4138-49EA-88CB-DC220DE7E9F4
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/get-Azappserviceplanmetrics
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Get-AzAppServicePlanMetrics.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Get-AzAppServicePlanMetrics.md
ms.openlocfilehash: c08ae63999582fd220005dde84316a2f4421d7b4
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93876165"
---
# <span data-ttu-id="2f4c2-101">Get-AzAppServicePlanMetrics</span><span class="sxs-lookup"><span data-stu-id="2f4c2-101">Get-AzAppServicePlanMetrics</span></span>

## <span data-ttu-id="2f4c2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2f4c2-102">SYNOPSIS</span></span>
<span data-ttu-id="2f4c2-103">Azure 웹 서비스 계획 메트릭을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="2f4c2-103">Gets Azure Web service plan metrics.</span></span>

## <span data-ttu-id="2f4c2-104">구문과</span><span class="sxs-lookup"><span data-stu-id="2f4c2-104">SYNTAX</span></span>

### <span data-ttu-id="2f4c2-105">S1</span><span class="sxs-lookup"><span data-stu-id="2f4c2-105">S1</span></span>
```
Get-AzAppServicePlanMetrics [-Metrics] <String[]> [-StartTime] <DateTime> [[-EndTime] <DateTime>]
 [-Granularity] <String> [-InstanceDetails] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2f4c2-106">구성원과</span><span class="sxs-lookup"><span data-stu-id="2f4c2-106">S2</span></span>
```
Get-AzAppServicePlanMetrics [-Metrics] <String[]> [-StartTime] <DateTime> [[-EndTime] <DateTime>]
 [-Granularity] <String> [-InstanceDetails] [-AppServicePlan] <AppServicePlan>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2f4c2-107">설명은</span><span class="sxs-lookup"><span data-stu-id="2f4c2-107">DESCRIPTION</span></span>
<span data-ttu-id="2f4c2-108">**Get-AzAppServicePlanMetrics** 는 앱 서비스 계획 메트릭을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="2f4c2-108">The **Get-AzAppServicePlanMetrics** gets App Service Plan metrics.</span></span>

## <span data-ttu-id="2f4c2-109">예제의</span><span class="sxs-lookup"><span data-stu-id="2f4c2-109">EXAMPLES</span></span>

### <span data-ttu-id="2f4c2-110">raid-1</span><span class="sxs-lookup"><span data-stu-id="2f4c2-110">1:</span></span>
```
PS C:\>Get-AzAppServicePlanMetrics -ResourceGroupName "Default-Web-WestUS" -Name "ContosoAppServPlan" -StartTime 2016-11-30T22:00:00Z -EndTime 2016-11-30T22:30:00Z -Granularity PT1M -Metrics ["CPU Percentage"]
```

<span data-ttu-id="2f4c2-111">이 명령은 StartTime 및 EndTime 사이의 분당 앱 서비스 계획의 PT1M-폴링 시간 1 분)의 CPU 백분율을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="2f4c2-111">This command gets CPU percentage of the App Service Plan per minute(PT1M - Poll Time 1 minute) between StartTime and EndTime</span></span>

## <span data-ttu-id="2f4c2-112">변수</span><span class="sxs-lookup"><span data-stu-id="2f4c2-112">PARAMETERS</span></span>

### <span data-ttu-id="2f4c2-113">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="2f4c2-113">-AppServicePlan</span></span>
<span data-ttu-id="2f4c2-114">App Service 계획 개체</span><span class="sxs-lookup"><span data-stu-id="2f4c2-114">App Service Plan Object</span></span>

```yaml
Type: AppServicePlan
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2f4c2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f4c2-115">-DefaultProfile</span></span>
<span data-ttu-id="2f4c2-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2f4c2-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f4c2-117">-EndTime</span><span class="sxs-lookup"><span data-stu-id="2f4c2-117">-EndTime</span></span>
<span data-ttu-id="2f4c2-118">UTC의 종료 시간</span><span class="sxs-lookup"><span data-stu-id="2f4c2-118">End Time in UTC</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f4c2-119">-세분성</span><span class="sxs-lookup"><span data-stu-id="2f4c2-119">-Granularity</span></span>
<span data-ttu-id="2f4c2-120">수준을</span><span class="sxs-lookup"><span data-stu-id="2f4c2-120">Granularity</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: PT1M, PT1H, P1D

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f4c2-121">-InstanceDetails</span><span class="sxs-lookup"><span data-stu-id="2f4c2-121">-InstanceDetails</span></span>
<span data-ttu-id="2f4c2-122">인스턴스 세부 정보</span><span class="sxs-lookup"><span data-stu-id="2f4c2-122">Instance Details</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f4c2-123">-메트릭스</span><span class="sxs-lookup"><span data-stu-id="2f4c2-123">-Metrics</span></span>
<span data-ttu-id="2f4c2-124">매트릭스</span><span class="sxs-lookup"><span data-stu-id="2f4c2-124">Metrics</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f4c2-125">-이름</span><span class="sxs-lookup"><span data-stu-id="2f4c2-125">-Name</span></span>
<span data-ttu-id="2f4c2-126">App Service 계획 이름</span><span class="sxs-lookup"><span data-stu-id="2f4c2-126">App Service Plan Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f4c2-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2f4c2-127">-ResourceGroupName</span></span>
<span data-ttu-id="2f4c2-128">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="2f4c2-128">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f4c2-129">-StartTime</span><span class="sxs-lookup"><span data-stu-id="2f4c2-129">-StartTime</span></span>
<span data-ttu-id="2f4c2-130">UTC의 시작 시간</span><span class="sxs-lookup"><span data-stu-id="2f4c2-130">Start Time in UTC</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f4c2-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f4c2-131">CommonParameters</span></span>
<span data-ttu-id="2f4c2-132">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2f4c2-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f4c2-133">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2f4c2-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f4c2-134">입력</span><span class="sxs-lookup"><span data-stu-id="2f4c2-134">INPUTS</span></span>

### <span data-ttu-id="2f4c2-135">ServerFarmWithRichSku</span><span class="sxs-lookup"><span data-stu-id="2f4c2-135">ServerFarmWithRichSku</span></span>
<span data-ttu-id="2f4c2-136">' AppServicePlan ' 매개 변수는 파이프라인에서 ' ServerFarmWithRichSku ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="2f4c2-136">Parameter 'AppServicePlan' accepts value of type 'ServerFarmWithRichSku' from the pipeline</span></span>

## <span data-ttu-id="2f4c2-137">출력</span><span class="sxs-lookup"><span data-stu-id="2f4c2-137">OUTPUTS</span></span>

## <span data-ttu-id="2f4c2-138">상속자</span><span class="sxs-lookup"><span data-stu-id="2f4c2-138">NOTES</span></span>

## <span data-ttu-id="2f4c2-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2f4c2-139">RELATED LINKS</span></span>

