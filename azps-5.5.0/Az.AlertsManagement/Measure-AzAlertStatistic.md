---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.alertsmanagement/measure-azalertstatistic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Measure-AzAlertStatistic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Measure-AzAlertStatistic.md
ms.openlocfilehash: 96b83f6792babed9fed7c39cad44aec0ea0f26ed
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100205896"
---
# <span data-ttu-id="4192a-101">Measure-AzAlertStatistic</span><span class="sxs-lookup"><span data-stu-id="4192a-101">Measure-AzAlertStatistic</span></span>

## <span data-ttu-id="4192a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4192a-102">SYNOPSIS</span></span>
<span data-ttu-id="4192a-103">경고 요약 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="4192a-103">Gets Alert Summary Information</span></span>

## <span data-ttu-id="4192a-104">구문</span><span class="sxs-lookup"><span data-stu-id="4192a-104">SYNTAX</span></span>

### <span data-ttu-id="4192a-105">SummaryTargetResourceIdFilter</span><span class="sxs-lookup"><span data-stu-id="4192a-105">SummaryTargetResourceIdFilter</span></span>
```
Measure-AzAlertStatistic -GroupBy <String> [-TargetResourceId <String>] [-MonitorService <String>]
 [-MonitorCondition <String>] [-Severity <String>] [-State <String>] [-AlertRuleId <String>]
 [-TimeRange <String>] [-CustomTimeRange <String>] [-IncludeSmartGroupsCount <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4192a-106">SummaryFilter</span><span class="sxs-lookup"><span data-stu-id="4192a-106">SummaryFilter</span></span>
```
Measure-AzAlertStatistic -GroupBy <String> [-TargetResourceType <String>] [-TargetResourceGroup <String>]
 [-MonitorService <String>] [-MonitorCondition <String>] [-Severity <String>] [-State <String>]
 [-AlertRuleId <String>] [-TimeRange <String>] [-CustomTimeRange <String>] [-IncludeSmartGroupsCount <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4192a-107">설명</span><span class="sxs-lookup"><span data-stu-id="4192a-107">DESCRIPTION</span></span>
<span data-ttu-id="4192a-108">**Measure-AzAlertStatistic** cmdlet은 경고 요약 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="4192a-108">**Measure-AzAlertStatistic** cmdlet gets alert summary details.</span></span>

## <span data-ttu-id="4192a-109">예제</span><span class="sxs-lookup"><span data-stu-id="4192a-109">EXAMPLES</span></span>

### <span data-ttu-id="4192a-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="4192a-110">Example 1</span></span>
```powershell
PS C:\> Measure-AzAlertStatistic -GroupBy "severity,alertstate" -State "Active"
```

<span data-ttu-id="4192a-111">심각도 및 활성 상태로 필터링된 상태를 그룹화하여 경고 수를 요약합니다.</span><span class="sxs-lookup"><span data-stu-id="4192a-111">Summarize alerts count grouped by severity and state filtered by Active state.</span></span>

## <span data-ttu-id="4192a-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4192a-112">PARAMETERS</span></span>

### <span data-ttu-id="4192a-113">-AlertRuleId</span><span class="sxs-lookup"><span data-stu-id="4192a-113">-AlertRuleId</span></span>
<span data-ttu-id="4192a-114">경고 규칙 ID에 대한 필터링</span><span class="sxs-lookup"><span data-stu-id="4192a-114">Filter on Alert Rule Id</span></span>

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

### <span data-ttu-id="4192a-115">-CustomTimeRange</span><span class="sxs-lookup"><span data-stu-id="4192a-115">-CustomTimeRange</span></span>
<span data-ttu-id="4192a-116">지원되는 형식 - \<start-time\> / \<end-time\> 시간이 ISO-8601 형식인 경우</span><span class="sxs-lookup"><span data-stu-id="4192a-116">Supported format - \<start-time\>/\<end-time\> where time is in ISO-8601 format</span></span>

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

### <span data-ttu-id="4192a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4192a-117">-DefaultProfile</span></span>
<span data-ttu-id="4192a-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4192a-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4192a-119">-GroupBy</span><span class="sxs-lookup"><span data-stu-id="4192a-119">-GroupBy</span></span>
<span data-ttu-id="4192a-120">속성으로 요약</span><span class="sxs-lookup"><span data-stu-id="4192a-120">Summarize by property</span></span>

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

### <span data-ttu-id="4192a-121">-IncludeSmartGroupsCount</span><span class="sxs-lookup"><span data-stu-id="4192a-121">-IncludeSmartGroupsCount</span></span>
<span data-ttu-id="4192a-122">SmartGroups 개수 포함</span><span class="sxs-lookup"><span data-stu-id="4192a-122">Include SmartGroups Count</span></span>

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

### <span data-ttu-id="4192a-123">-MonitorCondition</span><span class="sxs-lookup"><span data-stu-id="4192a-123">-MonitorCondition</span></span>
<span data-ttu-id="4192a-124">모니터 조건에 대한 필터링</span><span class="sxs-lookup"><span data-stu-id="4192a-124">Filter on Monitor Condition</span></span>

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

### <span data-ttu-id="4192a-125">-MonitorService</span><span class="sxs-lookup"><span data-stu-id="4192a-125">-MonitorService</span></span>
<span data-ttu-id="4192a-126">Moniter Service에서 필터링</span><span class="sxs-lookup"><span data-stu-id="4192a-126">Filter on Moniter Service</span></span>

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

### <span data-ttu-id="4192a-127">-심각도</span><span class="sxs-lookup"><span data-stu-id="4192a-127">-Severity</span></span>
<span data-ttu-id="4192a-128">경고의 심각도 필터링</span><span class="sxs-lookup"><span data-stu-id="4192a-128">Filter on Severity of alert</span></span>

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

### <span data-ttu-id="4192a-129">-State</span><span class="sxs-lookup"><span data-stu-id="4192a-129">-State</span></span>
<span data-ttu-id="4192a-130">경고 상태 필터링</span><span class="sxs-lookup"><span data-stu-id="4192a-130">Filter on State of alert</span></span>

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

### <span data-ttu-id="4192a-131">-TargetResourceGroup</span><span class="sxs-lookup"><span data-stu-id="4192a-131">-TargetResourceGroup</span></span>
<span data-ttu-id="4192a-132">경고의 대상 리소스의 리소스 그룹 이름을 필터링합니다.</span><span class="sxs-lookup"><span data-stu-id="4192a-132">Filter on Resource group name of the target resource of alert.</span></span>

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

### <span data-ttu-id="4192a-133">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="4192a-133">-TargetResourceId</span></span>
<span data-ttu-id="4192a-134">경고의 대상 리소스의 리소스 ID를 필터링합니다.</span><span class="sxs-lookup"><span data-stu-id="4192a-134">Filter on Resource Id of the target resource of alert.</span></span>

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

### <span data-ttu-id="4192a-135">-TargetResourceType</span><span class="sxs-lookup"><span data-stu-id="4192a-135">-TargetResourceType</span></span>
<span data-ttu-id="4192a-136">경고의 대상 리소스의 리소스 종류를 필터링합니다.</span><span class="sxs-lookup"><span data-stu-id="4192a-136">Filter on Resource type of the target resource of alert.</span></span>

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

### <span data-ttu-id="4192a-137">-TimeRange</span><span class="sxs-lookup"><span data-stu-id="4192a-137">-TimeRange</span></span>
<span data-ttu-id="4192a-138">지원되는 시간 범위 값 - 1h, 1d, 7d, 30d(기본값: 1d)</span><span class="sxs-lookup"><span data-stu-id="4192a-138">Supported time range values - 1h, 1d, 7d, 30d (Default is 1d)</span></span>

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

### <span data-ttu-id="4192a-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4192a-139">CommonParameters</span></span>
<span data-ttu-id="4192a-140">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="4192a-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4192a-141">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="4192a-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4192a-142">입력</span><span class="sxs-lookup"><span data-stu-id="4192a-142">INPUTS</span></span>

### <span data-ttu-id="4192a-143">없음</span><span class="sxs-lookup"><span data-stu-id="4192a-143">None</span></span>

## <span data-ttu-id="4192a-144">출력</span><span class="sxs-lookup"><span data-stu-id="4192a-144">OUTPUTS</span></span>

### <span data-ttu-id="4192a-145">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSAlertsSummary</span><span class="sxs-lookup"><span data-stu-id="4192a-145">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSAlertsSummary</span></span>

## <span data-ttu-id="4192a-146">참고 사항</span><span class="sxs-lookup"><span data-stu-id="4192a-146">NOTES</span></span>

## <span data-ttu-id="4192a-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4192a-147">RELATED LINKS</span></span>
