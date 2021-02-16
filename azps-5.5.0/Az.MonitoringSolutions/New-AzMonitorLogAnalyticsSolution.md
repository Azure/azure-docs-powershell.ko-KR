---
external help file: ''
Module Name: Az.MonitoringSolutions
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitoringsolutions/new-azmonitorloganalyticssolution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MonitoringSolutions/help/New-AzMonitorLogAnalyticsSolution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MonitoringSolutions/help/New-AzMonitorLogAnalyticsSolution.md
ms.openlocfilehash: 6747a53f9e714926c5a4d1358e15cb387ddae69a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100187345"
---
# <span data-ttu-id="83e90-101">New-AzMonitorLogAnalyticsSolution</span><span class="sxs-lookup"><span data-stu-id="83e90-101">New-AzMonitorLogAnalyticsSolution</span></span>

## <span data-ttu-id="83e90-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="83e90-102">SYNOPSIS</span></span>
<span data-ttu-id="83e90-103">로그 분석 솔루션을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="83e90-103">Creates a log analytics solution.</span></span>

## <span data-ttu-id="83e90-104">구문</span><span class="sxs-lookup"><span data-stu-id="83e90-104">SYNTAX</span></span>

```
New-AzMonitorLogAnalyticsSolution -ResourceGroupName <String> -Location <String> -Type <String>
 -WorkspaceResourceId <String> [-SubscriptionId <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="83e90-105">설명</span><span class="sxs-lookup"><span data-stu-id="83e90-105">DESCRIPTION</span></span>
<span data-ttu-id="83e90-106">로그 분석 솔루션을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="83e90-106">Creates a log analytics solution.</span></span>

## <span data-ttu-id="83e90-107">예제</span><span class="sxs-lookup"><span data-stu-id="83e90-107">EXAMPLES</span></span>

### <span data-ttu-id="83e90-108">예제 1: 로그 분석 작업 영역용 모니터 로그 분석 솔루션 만들기</span><span class="sxs-lookup"><span data-stu-id="83e90-108">Example 1: Create a monitor log analytics solution for the log analytics workspace</span></span>
```powershell
PS C:\> $workspace = Get-AzOperationalInsightsWorkspace -ResourceGroupName azureps-manual-test -Name monitoringworkspace-2vob7n
PS C:\> New-AzMonitorLogAnalyticsSolution -Type Containers -ResourceGroupName azureps-manual-test -Location $workspace.Location -WorkspaceResourceId $workspace.ResourceId

Name                                   Type                                     Location
----                                   ----                                     --------
Containers(monitoringworkspace-2vob7n) Microsoft.OperationsManagement/solutions East US
```

<span data-ttu-id="83e90-109">이 명령은 로그 분석 작업 영역용 모니터 로그 분석 솔루션을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="83e90-109">This command creates a monitor log analytics solution for the log analytics workspace.</span></span>

<span data-ttu-id="83e90-110">일반적으로 사용되는 형식은</span><span class="sxs-lookup"><span data-stu-id="83e90-110">Commonly used types are:</span></span>

| <span data-ttu-id="83e90-111">형식</span><span class="sxs-lookup"><span data-stu-id="83e90-111">Type</span></span> | <span data-ttu-id="83e90-112">설명</span><span class="sxs-lookup"><span data-stu-id="83e90-112">Description</span></span> |
| :-----| :----- |
| <span data-ttu-id="83e90-113">SecurityCenterFree</span><span class="sxs-lookup"><span data-stu-id="83e90-113">SecurityCenterFree</span></span> |  <span data-ttu-id="83e90-114">Azure Security Center – 무료 버전</span><span class="sxs-lookup"><span data-stu-id="83e90-114">Azure Security Center – Free Edition</span></span> |
| <span data-ttu-id="83e90-115">보안</span><span class="sxs-lookup"><span data-stu-id="83e90-115">Security</span></span> | <span data-ttu-id="83e90-116">Azure Security Center</span><span class="sxs-lookup"><span data-stu-id="83e90-116">Azure Security Center</span></span> |
| <span data-ttu-id="83e90-117">업데이트</span><span class="sxs-lookup"><span data-stu-id="83e90-117">Updates</span></span> | <span data-ttu-id="83e90-118">업데이트 관리</span><span class="sxs-lookup"><span data-stu-id="83e90-118">Update Management</span></span> |
| <span data-ttu-id="83e90-119">ContainerInsights</span><span class="sxs-lookup"><span data-stu-id="83e90-119">ContainerInsights</span></span> | <span data-ttu-id="83e90-120">컨테이너용 Azure Monitor</span><span class="sxs-lookup"><span data-stu-id="83e90-120">Azure Monitor for Containers</span></span> |
| <span data-ttu-id="83e90-121">ServiceMap</span><span class="sxs-lookup"><span data-stu-id="83e90-121">ServiceMap</span></span> | <span data-ttu-id="83e90-122">서비스 맵</span><span class="sxs-lookup"><span data-stu-id="83e90-122">Service Map</span></span> |
| <span data-ttu-id="83e90-123">AzureActivity</span><span class="sxs-lookup"><span data-stu-id="83e90-123">AzureActivity</span></span> | <span data-ttu-id="83e90-124">활동 로그 분석</span><span class="sxs-lookup"><span data-stu-id="83e90-124">Activity log analytics</span></span> |
| <span data-ttu-id="83e90-125">ChangeTracking</span><span class="sxs-lookup"><span data-stu-id="83e90-125">ChangeTracking</span></span> | <span data-ttu-id="83e90-126">변경 내용 추적 및 인벤토리</span><span class="sxs-lookup"><span data-stu-id="83e90-126">Change tracking and inventory</span></span> |
| <span data-ttu-id="83e90-127">VMInsights</span><span class="sxs-lookup"><span data-stu-id="83e90-127">VMInsights</span></span> | <span data-ttu-id="83e90-128">VM용 Azure Monitor</span><span class="sxs-lookup"><span data-stu-id="83e90-128">Azure Monitor for VMs</span></span> |
| <span data-ttu-id="83e90-129">SecurityInsights</span><span class="sxs-lookup"><span data-stu-id="83e90-129">SecurityInsights</span></span> | <span data-ttu-id="83e90-130">Azure Sentinel</span><span class="sxs-lookup"><span data-stu-id="83e90-130">Azure Sentinel</span></span> |
| <span data-ttu-id="83e90-131">NetworkMonitoring</span><span class="sxs-lookup"><span data-stu-id="83e90-131">NetworkMonitoring</span></span> | <span data-ttu-id="83e90-132">네트워크 성능 모니터</span><span class="sxs-lookup"><span data-stu-id="83e90-132">Network Performance Monitor</span></span> |
| <span data-ttu-id="83e90-133">SQLVulnerabilityAssessment</span><span class="sxs-lookup"><span data-stu-id="83e90-133">SQLVulnerabilityAssessment</span></span> | <span data-ttu-id="83e90-134">SQL 취약성 평가</span><span class="sxs-lookup"><span data-stu-id="83e90-134">SQL Vulnerability Assessment</span></span> |
| <span data-ttu-id="83e90-135">SQLAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="83e90-135">SQLAdvancedThreatProtection</span></span> | <span data-ttu-id="83e90-136">SQL Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="83e90-136">SQL Advanced Threat Protection</span></span> |
| <span data-ttu-id="83e90-137">맬웨어 방지</span><span class="sxs-lookup"><span data-stu-id="83e90-137">AntiMalware</span></span> | <span data-ttu-id="83e90-138">맬웨어 방지 평가</span><span class="sxs-lookup"><span data-stu-id="83e90-138">Antimalware Assessment</span></span> |
| <span data-ttu-id="83e90-139">AzureAutomation</span><span class="sxs-lookup"><span data-stu-id="83e90-139">AzureAutomation</span></span> | <span data-ttu-id="83e90-140">Automation Hybrid Worker</span><span class="sxs-lookup"><span data-stu-id="83e90-140">Automation Hybrid Worker</span></span> |
| <span data-ttu-id="83e90-141">LogicAppsManagement</span><span class="sxs-lookup"><span data-stu-id="83e90-141">LogicAppsManagement</span></span> | <span data-ttu-id="83e90-142">Logic Apps 관리</span><span class="sxs-lookup"><span data-stu-id="83e90-142">Logic Apps Management</span></span> |
| <span data-ttu-id="83e90-143">SQLDataClassification</span><span class="sxs-lookup"><span data-stu-id="83e90-143">SQLDataClassification</span></span> | <span data-ttu-id="83e90-144">SQL 데이터 검색 & 분류</span><span class="sxs-lookup"><span data-stu-id="83e90-144">SQL Data Discovery & Classification</span></span> |

## <span data-ttu-id="83e90-145">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="83e90-145">PARAMETERS</span></span>

### <span data-ttu-id="83e90-146">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83e90-146">-DefaultProfile</span></span>
<span data-ttu-id="83e90-147">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="83e90-147">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83e90-148">-Location</span><span class="sxs-lookup"><span data-stu-id="83e90-148">-Location</span></span>
<span data-ttu-id="83e90-149">리소스 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="83e90-149">Resource location.</span></span>
<span data-ttu-id="83e90-150">로그 분석 작업 영역과 동일해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="83e90-150">Must be the same as the log analytic workspace.</span></span>

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

### <span data-ttu-id="83e90-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="83e90-151">-ResourceGroupName</span></span>
<span data-ttu-id="83e90-152">얻을 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="83e90-152">The name of the resource group to get.</span></span>
<span data-ttu-id="83e90-153">이름은 대소문자 무관합니다.</span><span class="sxs-lookup"><span data-stu-id="83e90-153">The name is case insensitive.</span></span>

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

### <span data-ttu-id="83e90-154">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="83e90-154">-SubscriptionId</span></span>
<span data-ttu-id="83e90-155">Microsoft Azure 구독을 고유하게 식별하는 구독 자격 증명을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="83e90-155">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="83e90-156">구독 ID는 모든 서비스 호출에 대한 URI의 일부를 형성합니다.</span><span class="sxs-lookup"><span data-stu-id="83e90-156">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83e90-157">-Tag</span><span class="sxs-lookup"><span data-stu-id="83e90-157">-Tag</span></span>
<span data-ttu-id="83e90-158">리소스 태그</span><span class="sxs-lookup"><span data-stu-id="83e90-158">Resource tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83e90-159">-Type</span><span class="sxs-lookup"><span data-stu-id="83e90-159">-Type</span></span>
<span data-ttu-id="83e90-160">만들 솔루션의 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="83e90-160">Type of the solution to be created.</span></span>
<span data-ttu-id="83e90-161">예: "컨테이너".</span><span class="sxs-lookup"><span data-stu-id="83e90-161">For example "Container".</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SolutionType

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83e90-162">-WorkspaceResourceId</span><span class="sxs-lookup"><span data-stu-id="83e90-162">-WorkspaceResourceId</span></span>
<span data-ttu-id="83e90-163">솔루션을 배포/사용하도록 설정하는 작업 영역의 Azure 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="83e90-163">The Azure resource ID for the workspace where the solution will be deployed/enabled.</span></span>

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

### <span data-ttu-id="83e90-164">-Confirm</span><span class="sxs-lookup"><span data-stu-id="83e90-164">-Confirm</span></span>
<span data-ttu-id="83e90-165">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="83e90-165">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83e90-166">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="83e90-166">-WhatIf</span></span>
<span data-ttu-id="83e90-167">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="83e90-167">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="83e90-168">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="83e90-168">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83e90-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83e90-169">CommonParameters</span></span>
<span data-ttu-id="83e90-170">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="83e90-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83e90-171">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="83e90-171">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83e90-172">입력</span><span class="sxs-lookup"><span data-stu-id="83e90-172">INPUTS</span></span>

## <span data-ttu-id="83e90-173">출력</span><span class="sxs-lookup"><span data-stu-id="83e90-173">OUTPUTS</span></span>

### <span data-ttu-id="83e90-174">Microsoft.Azure.PowerShell.Cmdlets.MonitoringSolutions.Models.Api20151101Preview.ISolution</span><span class="sxs-lookup"><span data-stu-id="83e90-174">Microsoft.Azure.PowerShell.Cmdlets.MonitoringSolutions.Models.Api20151101Preview.ISolution</span></span>

## <span data-ttu-id="83e90-175">참고 사항</span><span class="sxs-lookup"><span data-stu-id="83e90-175">NOTES</span></span>

<span data-ttu-id="83e90-176">별칭</span><span class="sxs-lookup"><span data-stu-id="83e90-176">ALIASES</span></span>

## <span data-ttu-id="83e90-177">관련 링크</span><span class="sxs-lookup"><span data-stu-id="83e90-177">RELATED LINKS</span></span>



[<span data-ttu-id="83e90-178">Get-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="83e90-178">Get-AzOperationalInsightsWorkspace</span></span>](https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightsworkspace)

