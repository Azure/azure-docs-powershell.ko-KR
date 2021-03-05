---
external help file: ''
Module Name: Az.MonitoringSolutions
online version: https://docs.microsoft.com/powershell/module/az.monitoringsolutions/new-azmonitorloganalyticssolution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MonitoringSolutions/help/New-AzMonitorLogAnalyticsSolution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MonitoringSolutions/help/New-AzMonitorLogAnalyticsSolution.md
ms.openlocfilehash: ff9a54852d84d7c1183e81cb8b597279f357ebe8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101965739"
---
# <span data-ttu-id="6dffc-101">New-AzMonitorLogAnalyticsSolution</span><span class="sxs-lookup"><span data-stu-id="6dffc-101">New-AzMonitorLogAnalyticsSolution</span></span>

## <span data-ttu-id="6dffc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6dffc-102">SYNOPSIS</span></span>
<span data-ttu-id="6dffc-103">로그 분석 솔루션을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="6dffc-103">Creates a log analytics solution.</span></span>

## <span data-ttu-id="6dffc-104">구문</span><span class="sxs-lookup"><span data-stu-id="6dffc-104">SYNTAX</span></span>

```
New-AzMonitorLogAnalyticsSolution -ResourceGroupName <String> -Location <String> -Type <String>
 -WorkspaceResourceId <String> [-SubscriptionId <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="6dffc-105">설명</span><span class="sxs-lookup"><span data-stu-id="6dffc-105">DESCRIPTION</span></span>
<span data-ttu-id="6dffc-106">로그 분석 솔루션을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="6dffc-106">Creates a log analytics solution.</span></span>

## <span data-ttu-id="6dffc-107">예제</span><span class="sxs-lookup"><span data-stu-id="6dffc-107">EXAMPLES</span></span>

### <span data-ttu-id="6dffc-108">예제 1: 로그 분석 작업 영역의 모니터 로그 분석 솔루션 만들기</span><span class="sxs-lookup"><span data-stu-id="6dffc-108">Example 1: Create a monitor log analytics solution for the log analytics workspace</span></span>
```powershell
PS C:\> $workspace = Get-AzOperationalInsightsWorkspace -ResourceGroupName azureps-manual-test -Name monitoringworkspace-2vob7n
PS C:\> New-AzMonitorLogAnalyticsSolution -Type Containers -ResourceGroupName azureps-manual-test -Location $workspace.Location -WorkspaceResourceId $workspace.ResourceId

Name                                   Type                                     Location
----                                   ----                                     --------
Containers(monitoringworkspace-2vob7n) Microsoft.OperationsManagement/solutions East US
```

<span data-ttu-id="6dffc-109">이 명령은 로그 분석 작업 영역의 모니터 로그 분석 솔루션을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="6dffc-109">This command creates a monitor log analytics solution for the log analytics workspace.</span></span>

<span data-ttu-id="6dffc-110">일반적으로 사용되는 형식은:</span><span class="sxs-lookup"><span data-stu-id="6dffc-110">Commonly used types are:</span></span>

| <span data-ttu-id="6dffc-111">형식</span><span class="sxs-lookup"><span data-stu-id="6dffc-111">Type</span></span> | <span data-ttu-id="6dffc-112">설명</span><span class="sxs-lookup"><span data-stu-id="6dffc-112">Description</span></span> |
| :-----| :----- |
| <span data-ttu-id="6dffc-113">SecurityCenterFree</span><span class="sxs-lookup"><span data-stu-id="6dffc-113">SecurityCenterFree</span></span> |  <span data-ttu-id="6dffc-114">Azure Security Center – 무료 버전</span><span class="sxs-lookup"><span data-stu-id="6dffc-114">Azure Security Center – Free Edition</span></span> |
| <span data-ttu-id="6dffc-115">보안</span><span class="sxs-lookup"><span data-stu-id="6dffc-115">Security</span></span> | <span data-ttu-id="6dffc-116">Azure Security Center</span><span class="sxs-lookup"><span data-stu-id="6dffc-116">Azure Security Center</span></span> |
| <span data-ttu-id="6dffc-117">업데이트</span><span class="sxs-lookup"><span data-stu-id="6dffc-117">Updates</span></span> | <span data-ttu-id="6dffc-118">업데이트 관리</span><span class="sxs-lookup"><span data-stu-id="6dffc-118">Update Management</span></span> |
| <span data-ttu-id="6dffc-119">ContainerInsights</span><span class="sxs-lookup"><span data-stu-id="6dffc-119">ContainerInsights</span></span> | <span data-ttu-id="6dffc-120">컨테이너용 Azure Monitor</span><span class="sxs-lookup"><span data-stu-id="6dffc-120">Azure Monitor for Containers</span></span> |
| <span data-ttu-id="6dffc-121">ServiceMap</span><span class="sxs-lookup"><span data-stu-id="6dffc-121">ServiceMap</span></span> | <span data-ttu-id="6dffc-122">서비스 맵</span><span class="sxs-lookup"><span data-stu-id="6dffc-122">Service Map</span></span> |
| <span data-ttu-id="6dffc-123">AzureActivity</span><span class="sxs-lookup"><span data-stu-id="6dffc-123">AzureActivity</span></span> | <span data-ttu-id="6dffc-124">활동 로그 분석</span><span class="sxs-lookup"><span data-stu-id="6dffc-124">Activity log analytics</span></span> |
| <span data-ttu-id="6dffc-125">ChangeTracking</span><span class="sxs-lookup"><span data-stu-id="6dffc-125">ChangeTracking</span></span> | <span data-ttu-id="6dffc-126">변경 내용 추적 및 인벤토리</span><span class="sxs-lookup"><span data-stu-id="6dffc-126">Change tracking and inventory</span></span> |
| <span data-ttu-id="6dffc-127">VMInsights</span><span class="sxs-lookup"><span data-stu-id="6dffc-127">VMInsights</span></span> | <span data-ttu-id="6dffc-128">VM용 Azure Monitor</span><span class="sxs-lookup"><span data-stu-id="6dffc-128">Azure Monitor for VMs</span></span> |
| <span data-ttu-id="6dffc-129">SecurityInsights</span><span class="sxs-lookup"><span data-stu-id="6dffc-129">SecurityInsights</span></span> | <span data-ttu-id="6dffc-130">Azure Sentinel</span><span class="sxs-lookup"><span data-stu-id="6dffc-130">Azure Sentinel</span></span> |
| <span data-ttu-id="6dffc-131">NetworkMonitoring</span><span class="sxs-lookup"><span data-stu-id="6dffc-131">NetworkMonitoring</span></span> | <span data-ttu-id="6dffc-132">네트워크 성능 모니터</span><span class="sxs-lookup"><span data-stu-id="6dffc-132">Network Performance Monitor</span></span> |
| <span data-ttu-id="6dffc-133">SQLVulnerabilityAssessment</span><span class="sxs-lookup"><span data-stu-id="6dffc-133">SQLVulnerabilityAssessment</span></span> | <span data-ttu-id="6dffc-134">SQL 취약성 평가</span><span class="sxs-lookup"><span data-stu-id="6dffc-134">SQL Vulnerability Assessment</span></span> |
| <span data-ttu-id="6dffc-135">SQLAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="6dffc-135">SQLAdvancedThreatProtection</span></span> | <span data-ttu-id="6dffc-136">SQL 위협 보호</span><span class="sxs-lookup"><span data-stu-id="6dffc-136">SQL Advanced Threat Protection</span></span> |
| <span data-ttu-id="6dffc-137">맬웨어 방지</span><span class="sxs-lookup"><span data-stu-id="6dffc-137">AntiMalware</span></span> | <span data-ttu-id="6dffc-138">맬웨어 방지 평가</span><span class="sxs-lookup"><span data-stu-id="6dffc-138">Antimalware Assessment</span></span> |
| <span data-ttu-id="6dffc-139">AzureAutomation</span><span class="sxs-lookup"><span data-stu-id="6dffc-139">AzureAutomation</span></span> | <span data-ttu-id="6dffc-140">Automation Hybrid Worker</span><span class="sxs-lookup"><span data-stu-id="6dffc-140">Automation Hybrid Worker</span></span> |
| <span data-ttu-id="6dffc-141">LogicAppsManagement</span><span class="sxs-lookup"><span data-stu-id="6dffc-141">LogicAppsManagement</span></span> | <span data-ttu-id="6dffc-142">Logic Apps Management</span><span class="sxs-lookup"><span data-stu-id="6dffc-142">Logic Apps Management</span></span> |
| <span data-ttu-id="6dffc-143">SQLDataClassification</span><span class="sxs-lookup"><span data-stu-id="6dffc-143">SQLDataClassification</span></span> | <span data-ttu-id="6dffc-144">SQL 데이터 검색 & 분류</span><span class="sxs-lookup"><span data-stu-id="6dffc-144">SQL Data Discovery & Classification</span></span> |

## <span data-ttu-id="6dffc-145">매개 변수</span><span class="sxs-lookup"><span data-stu-id="6dffc-145">PARAMETERS</span></span>

### <span data-ttu-id="6dffc-146">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6dffc-146">-DefaultProfile</span></span>
<span data-ttu-id="6dffc-147">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6dffc-147">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6dffc-148">-Location</span><span class="sxs-lookup"><span data-stu-id="6dffc-148">-Location</span></span>
<span data-ttu-id="6dffc-149">리소스 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="6dffc-149">Resource location.</span></span>
<span data-ttu-id="6dffc-150">로그 분석 작업 영역과 동일해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="6dffc-150">Must be the same as the log analytic workspace.</span></span>

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

### <span data-ttu-id="6dffc-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6dffc-151">-ResourceGroupName</span></span>
<span data-ttu-id="6dffc-152">얻을 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6dffc-152">The name of the resource group to get.</span></span>
<span data-ttu-id="6dffc-153">이름은 대소문자와 무관합니다.</span><span class="sxs-lookup"><span data-stu-id="6dffc-153">The name is case insensitive.</span></span>

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

### <span data-ttu-id="6dffc-154">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6dffc-154">-SubscriptionId</span></span>
<span data-ttu-id="6dffc-155">Microsoft Azure 구독을 고유하게 식별하는 구독 자격 증명을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="6dffc-155">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="6dffc-156">구독 ID는 모든 서비스 호출에 대한 URI의 일부를 형성합니다.</span><span class="sxs-lookup"><span data-stu-id="6dffc-156">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="6dffc-157">-Tag</span><span class="sxs-lookup"><span data-stu-id="6dffc-157">-Tag</span></span>
<span data-ttu-id="6dffc-158">리소스 태그</span><span class="sxs-lookup"><span data-stu-id="6dffc-158">Resource tags</span></span>

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

### <span data-ttu-id="6dffc-159">-Type</span><span class="sxs-lookup"><span data-stu-id="6dffc-159">-Type</span></span>
<span data-ttu-id="6dffc-160">만들 솔루션의 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="6dffc-160">Type of the solution to be created.</span></span>
<span data-ttu-id="6dffc-161">예를 들어 "컨테이너"입니다.</span><span class="sxs-lookup"><span data-stu-id="6dffc-161">For example "Container".</span></span>

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

### <span data-ttu-id="6dffc-162">-WorkspaceResourceId</span><span class="sxs-lookup"><span data-stu-id="6dffc-162">-WorkspaceResourceId</span></span>
<span data-ttu-id="6dffc-163">솔루션을 배포/사용하도록 설정하는 작업 영역의 Azure 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="6dffc-163">The Azure resource ID for the workspace where the solution will be deployed/enabled.</span></span>

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

### <span data-ttu-id="6dffc-164">-확인</span><span class="sxs-lookup"><span data-stu-id="6dffc-164">-Confirm</span></span>
<span data-ttu-id="6dffc-165">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="6dffc-165">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6dffc-166">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6dffc-166">-WhatIf</span></span>
<span data-ttu-id="6dffc-167">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="6dffc-167">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6dffc-168">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6dffc-168">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6dffc-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6dffc-169">CommonParameters</span></span>
<span data-ttu-id="6dffc-170">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="6dffc-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6dffc-171">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6dffc-171">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6dffc-172">입력</span><span class="sxs-lookup"><span data-stu-id="6dffc-172">INPUTS</span></span>

## <span data-ttu-id="6dffc-173">출력</span><span class="sxs-lookup"><span data-stu-id="6dffc-173">OUTPUTS</span></span>

### <span data-ttu-id="6dffc-174">Microsoft.Azure.PowerShell.Cmdlets.MonitoringSolutions.Models.Api20151101Preview.ISolution</span><span class="sxs-lookup"><span data-stu-id="6dffc-174">Microsoft.Azure.PowerShell.Cmdlets.MonitoringSolutions.Models.Api20151101Preview.ISolution</span></span>

## <span data-ttu-id="6dffc-175">참고 사항</span><span class="sxs-lookup"><span data-stu-id="6dffc-175">NOTES</span></span>

<span data-ttu-id="6dffc-176">별칭</span><span class="sxs-lookup"><span data-stu-id="6dffc-176">ALIASES</span></span>

## <span data-ttu-id="6dffc-177">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6dffc-177">RELATED LINKS</span></span>



[<span data-ttu-id="6dffc-178">Get-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="6dffc-178">Get-AzOperationalInsightsWorkspace</span></span>](https://docs.microsoft.com/powershell/module/az.operationalinsights/get-azoperationalinsightsworkspace)

