---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 0AC0C4F9-4138-49EA-88CB-DC220DE7E9F4
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azappserviceplanmetric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzAppServicePlanMetric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzAppServicePlanMetric.md
ms.openlocfilehash: d3a2cd8d0907d26a137df547f1599c9ed09cb7b3
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94213133"
---
# <span data-ttu-id="ff2b4-101">Get-AzAppServicePlanMetric</span><span class="sxs-lookup"><span data-stu-id="ff2b4-101">Get-AzAppServicePlanMetric</span></span>

## <span data-ttu-id="ff2b4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ff2b4-102">SYNOPSIS</span></span>

## <span data-ttu-id="ff2b4-103">구문과</span><span class="sxs-lookup"><span data-stu-id="ff2b4-103">SYNTAX</span></span>

### <span data-ttu-id="ff2b4-104">S1</span><span class="sxs-lookup"><span data-stu-id="ff2b4-104">S1</span></span>
```
Get-AzAppServicePlanMetric [-Metrics] <String[]> [-StartTime] <DateTime> [[-EndTime] <DateTime>]
 [-Granularity] <String> [-InstanceDetails] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ff2b4-105">구성원과</span><span class="sxs-lookup"><span data-stu-id="ff2b4-105">S2</span></span>
```
Get-AzAppServicePlanMetric [-Metrics] <String[]> [-StartTime] <DateTime> [[-EndTime] <DateTime>]
 [-Granularity] <String> [-InstanceDetails] [-AppServicePlan] <PSAppServicePlan>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ff2b4-106">설명은</span><span class="sxs-lookup"><span data-stu-id="ff2b4-106">DESCRIPTION</span></span>
<span data-ttu-id="ff2b4-107">**Get-AzAppServicePlanMetric** 는 앱 서비스 계획 메트릭을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ff2b4-107">The **Get-AzAppServicePlanMetric** gets App Service Plan metrics.</span></span>

## <span data-ttu-id="ff2b4-108">예제의</span><span class="sxs-lookup"><span data-stu-id="ff2b4-108">EXAMPLES</span></span>

### <span data-ttu-id="ff2b4-109">raid-1</span><span class="sxs-lookup"><span data-stu-id="ff2b4-109">1:</span></span>
```
PS C:\>Get-AzAppServicePlanMetric -ResourceGroupName "Default-Web-WestUS" -Name "ContosoAppServPlan" -StartTime 2016-11-30T22:00:00Z -EndTime 2016-11-30T22:30:00Z -Granularity PT1M -Metrics "CPU Percentage"
```

<span data-ttu-id="ff2b4-110">이 명령은 StartTime 및 EndTime 사이의 분당 앱 서비스 계획의 PT1M-폴링 시간 1 분)의 CPU 백분율을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ff2b4-110">This command gets CPU percentage of the App Service Plan per minute(PT1M - Poll Time 1 minute) between StartTime and EndTime</span></span>

## <span data-ttu-id="ff2b4-111">변수</span><span class="sxs-lookup"><span data-stu-id="ff2b4-111">PARAMETERS</span></span>

### <span data-ttu-id="ff2b4-112">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="ff2b4-112">-AppServicePlan</span></span>
<span data-ttu-id="ff2b4-113">App Service 계획 개체</span><span class="sxs-lookup"><span data-stu-id="ff2b4-113">App Service Plan Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServicePlan
Parameter Sets: S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ff2b4-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff2b4-114">-DefaultProfile</span></span>
<span data-ttu-id="ff2b4-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ff2b4-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ff2b4-116">-EndTime</span><span class="sxs-lookup"><span data-stu-id="ff2b4-116">-EndTime</span></span>
<span data-ttu-id="ff2b4-117">UTC의 종료 시간</span><span class="sxs-lookup"><span data-stu-id="ff2b4-117">End Time in UTC</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff2b4-118">-세분성</span><span class="sxs-lookup"><span data-stu-id="ff2b4-118">-Granularity</span></span>
<span data-ttu-id="ff2b4-119">수준을</span><span class="sxs-lookup"><span data-stu-id="ff2b4-119">Granularity</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: PT1M, PT1H, P1D

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff2b4-120">-InstanceDetails</span><span class="sxs-lookup"><span data-stu-id="ff2b4-120">-InstanceDetails</span></span>
<span data-ttu-id="ff2b4-121">인스턴스 세부 정보</span><span class="sxs-lookup"><span data-stu-id="ff2b4-121">Instance Details</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff2b4-122">-메트릭스</span><span class="sxs-lookup"><span data-stu-id="ff2b4-122">-Metrics</span></span>
<span data-ttu-id="ff2b4-123">매트릭스</span><span class="sxs-lookup"><span data-stu-id="ff2b4-123">Metrics</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff2b4-124">-이름</span><span class="sxs-lookup"><span data-stu-id="ff2b4-124">-Name</span></span>
<span data-ttu-id="ff2b4-125">App Service 계획 이름</span><span class="sxs-lookup"><span data-stu-id="ff2b4-125">App Service Plan Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff2b4-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ff2b4-126">-ResourceGroupName</span></span>
<span data-ttu-id="ff2b4-127">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="ff2b4-127">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff2b4-128">-StartTime</span><span class="sxs-lookup"><span data-stu-id="ff2b4-128">-StartTime</span></span>
<span data-ttu-id="ff2b4-129">UTC의 시작 시간</span><span class="sxs-lookup"><span data-stu-id="ff2b4-129">Start Time in UTC</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff2b4-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff2b4-130">CommonParameters</span></span>
<span data-ttu-id="ff2b4-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ff2b4-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff2b4-132">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="ff2b4-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff2b4-133">입력</span><span class="sxs-lookup"><span data-stu-id="ff2b4-133">INPUTS</span></span>

### <span data-ttu-id="ff2b4-134">Web app. p i p. p i p.</span><span class="sxs-lookup"><span data-stu-id="ff2b4-134">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServicePlan</span></span>

## <span data-ttu-id="ff2b4-135">출력</span><span class="sxs-lookup"><span data-stu-id="ff2b4-135">OUTPUTS</span></span>

### <span data-ttu-id="ff2b4-136">ResourceMetric/. m i.</span><span class="sxs-lookup"><span data-stu-id="ff2b4-136">Microsoft.Azure.Management.WebSites.Models.ResourceMetric</span></span>

## <span data-ttu-id="ff2b4-137">상속자</span><span class="sxs-lookup"><span data-stu-id="ff2b4-137">NOTES</span></span>

## <span data-ttu-id="ff2b4-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ff2b4-138">RELATED LINKS</span></span>
