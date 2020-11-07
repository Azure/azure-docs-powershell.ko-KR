---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.alertsmanagement/measure-azalertstatistic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Measure-AzAlertStatistic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Measure-AzAlertStatistic.md
ms.openlocfilehash: 1cd4029d9e5bcdf67706784228a8104ed4eb221c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93698183"
---
# <span data-ttu-id="e30a7-101">Measure-AzAlertStatistic</span><span class="sxs-lookup"><span data-stu-id="e30a7-101">Measure-AzAlertStatistic</span></span>

## <span data-ttu-id="e30a7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e30a7-102">SYNOPSIS</span></span>
<span data-ttu-id="e30a7-103">알림 요약 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e30a7-103">Gets Alert Summary Information</span></span>

## <span data-ttu-id="e30a7-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e30a7-104">SYNTAX</span></span>

### <span data-ttu-id="e30a7-105">SummaryTargetResourceIdFilter</span><span class="sxs-lookup"><span data-stu-id="e30a7-105">SummaryTargetResourceIdFilter</span></span>
```
Measure-AzAlertStatistic -GroupBy <String> [-TargetResourceId <String>] [-MonitorService <String>]
 [-MonitorCondition <String>] [-Severity <String>] [-State <String>] [-AlertRuleId <String>]
 [-TimeRange <String>] [-CustomTimeRange <String>] [-IncludeSmartGroupsCount <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e30a7-106">요약 필터</span><span class="sxs-lookup"><span data-stu-id="e30a7-106">SummaryFilter</span></span>
```
Measure-AzAlertStatistic -GroupBy <String> [-TargetResourceType <String>] [-TargetResourceGroup <String>]
 [-MonitorService <String>] [-MonitorCondition <String>] [-Severity <String>] [-State <String>]
 [-AlertRuleId <String>] [-TimeRange <String>] [-CustomTimeRange <String>] [-IncludeSmartGroupsCount <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e30a7-107">설명은</span><span class="sxs-lookup"><span data-stu-id="e30a7-107">DESCRIPTION</span></span>
<span data-ttu-id="e30a7-108">**AzAlertStatistic cmdlet은** 알림 요약 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e30a7-108">**Measure-AzAlertStatistic** cmdlet gets alert summary details.</span></span>

## <span data-ttu-id="e30a7-109">예제의</span><span class="sxs-lookup"><span data-stu-id="e30a7-109">EXAMPLES</span></span>

### <span data-ttu-id="e30a7-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="e30a7-110">Example 1</span></span>
```powershell
PS C:\> Measure-AzAlertStatistic -GroupBy "severity,alertstate" -State "Active"
```

<span data-ttu-id="e30a7-111">활성 상태별로 필터링 된 경고 수를 심각도 및 상태별로 그룹화 하 여 요약 합니다.</span><span class="sxs-lookup"><span data-stu-id="e30a7-111">Summarize alerts count grouped by severity and state filtered by Active state.</span></span>

## <span data-ttu-id="e30a7-112">변수</span><span class="sxs-lookup"><span data-stu-id="e30a7-112">PARAMETERS</span></span>

### <span data-ttu-id="e30a7-113">-AlertRuleId</span><span class="sxs-lookup"><span data-stu-id="e30a7-113">-AlertRuleId</span></span>
<span data-ttu-id="e30a7-114">경고 규칙 Id에 대 한 필터</span><span class="sxs-lookup"><span data-stu-id="e30a7-114">Filter on Alert Rule Id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e30a7-115">-CustomTimeRange</span><span class="sxs-lookup"><span data-stu-id="e30a7-115">-CustomTimeRange</span></span>
<span data-ttu-id="e30a7-116">지원 되는 형식- \< 시작 시간 \> / \< 종료 시간이 \> ISO-8601 형식으로 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e30a7-116">Supported format - \<start-time\>/\<end-time\> where time is in ISO-8601 format</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e30a7-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e30a7-117">-DefaultProfile</span></span>
<span data-ttu-id="e30a7-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e30a7-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e30a7-119">-GroupBy</span><span class="sxs-lookup"><span data-stu-id="e30a7-119">-GroupBy</span></span>
<span data-ttu-id="e30a7-120">속성으로 요약</span><span class="sxs-lookup"><span data-stu-id="e30a7-120">Summarize by property</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e30a7-121">-IncludeSmartGroupsCount</span><span class="sxs-lookup"><span data-stu-id="e30a7-121">-IncludeSmartGroupsCount</span></span>
<span data-ttu-id="e30a7-122">SmartGroups Count 포함</span><span class="sxs-lookup"><span data-stu-id="e30a7-122">Include SmartGroups Count</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e30a7-123">-MonitorCondition</span><span class="sxs-lookup"><span data-stu-id="e30a7-123">-MonitorCondition</span></span>
<span data-ttu-id="e30a7-124">모니터 조건에 따라 필터링</span><span class="sxs-lookup"><span data-stu-id="e30a7-124">Filter on Monitor Condition</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e30a7-125">-모니터 서비스</span><span class="sxs-lookup"><span data-stu-id="e30a7-125">-MonitorService</span></span>
<span data-ttu-id="e30a7-126">Moniter 서비스에 대 한 필터링</span><span class="sxs-lookup"><span data-stu-id="e30a7-126">Filter on Moniter Service</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e30a7-127">-심각도</span><span class="sxs-lookup"><span data-stu-id="e30a7-127">-Severity</span></span>
<span data-ttu-id="e30a7-128">알림의 심각도에 대 한 필터링</span><span class="sxs-lookup"><span data-stu-id="e30a7-128">Filter on Severity of alert</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e30a7-129">-상태</span><span class="sxs-lookup"><span data-stu-id="e30a7-129">-State</span></span>
<span data-ttu-id="e30a7-130">알림의 상태에 대 한 필터링</span><span class="sxs-lookup"><span data-stu-id="e30a7-130">Filter on State of alert</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e30a7-131">-TargetResourceGroup</span><span class="sxs-lookup"><span data-stu-id="e30a7-131">-TargetResourceGroup</span></span>
<span data-ttu-id="e30a7-132">경고 대상 리소스의 리소스 그룹 이름에 대 한 필터입니다.</span><span class="sxs-lookup"><span data-stu-id="e30a7-132">Filter on Resource group name of the target resource of alert.</span></span>

```yaml
Type: System.String
Parameter Sets: SummaryFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e30a7-133">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="e30a7-133">-TargetResourceId</span></span>
<span data-ttu-id="e30a7-134">경고 대상 리소스의 리소스 Id에 대 한 필터입니다.</span><span class="sxs-lookup"><span data-stu-id="e30a7-134">Filter on Resource Id of the target resource of alert.</span></span>

```yaml
Type: System.String
Parameter Sets: SummaryTargetResourceIdFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e30a7-135">-TargetResourceType</span><span class="sxs-lookup"><span data-stu-id="e30a7-135">-TargetResourceType</span></span>
<span data-ttu-id="e30a7-136">경고 대상 리소스의 리소스 종류에 대 한 필터입니다.</span><span class="sxs-lookup"><span data-stu-id="e30a7-136">Filter on Resource type of the target resource of alert.</span></span>

```yaml
Type: System.String
Parameter Sets: SummaryFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e30a7-137">-TimeRange</span><span class="sxs-lookup"><span data-stu-id="e30a7-137">-TimeRange</span></span>
<span data-ttu-id="e30a7-138">지원 되는 시간 범위 값-1h, 1d, 7d, 30d (기본값은 1d)</span><span class="sxs-lookup"><span data-stu-id="e30a7-138">Supported time range values - 1h, 1d, 7d, 30d (Default is 1d)</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e30a7-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e30a7-139">CommonParameters</span></span>
<span data-ttu-id="e30a7-140">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e30a7-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e30a7-141">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="e30a7-141">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e30a7-142">입력</span><span class="sxs-lookup"><span data-stu-id="e30a7-142">INPUTS</span></span>

### <span data-ttu-id="e30a7-143">않아야</span><span class="sxs-lookup"><span data-stu-id="e30a7-143">None</span></span>

## <span data-ttu-id="e30a7-144">출력</span><span class="sxs-lookup"><span data-stu-id="e30a7-144">OUTPUTS</span></span>

### <span data-ttu-id="e30a7-145">AlertsManagement 모델. PSAlertsSummary.</span><span class="sxs-lookup"><span data-stu-id="e30a7-145">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSAlertsSummary</span></span>

## <span data-ttu-id="e30a7-146">상속자</span><span class="sxs-lookup"><span data-stu-id="e30a7-146">NOTES</span></span>

## <span data-ttu-id="e30a7-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e30a7-147">RELATED LINKS</span></span>
