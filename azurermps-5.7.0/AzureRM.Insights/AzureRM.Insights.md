---
Module Name: AzureRM.Insights
Module Guid: 698c387c-bd6b-41c6-82ce-721f1ef39548
Download Help Link:
  object Object: 
Help Version:
  object Object: 
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/AzureRM.Insights.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/AzureRM.Insights.md
ms.openlocfilehash: d4f7819a3ddbf49f4a3c4ed56cd8273b1f2e1848
ms.sourcegitcommit: 43f4bdf2a59dd82fd881512aa9761bf72eb5703c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/23/2019
ms.locfileid: "93522816"
---
# <span data-ttu-id="82c45-101">AzureRM 모듈</span><span class="sxs-lookup"><span data-stu-id="82c45-101">AzureRM.Insights Module</span></span>
## <span data-ttu-id="82c45-102">설명은</span><span class="sxs-lookup"><span data-stu-id="82c45-102">Description</span></span>
<span data-ttu-id="82c45-103">이 항목에서는 Azure Insights Cmdlet에 대 한 도움말 항목을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="82c45-103">This topic displays help topics for the Azure Insights Cmdlets.</span></span>

## <span data-ttu-id="82c45-104">AzureRM Cmdlet</span><span class="sxs-lookup"><span data-stu-id="82c45-104">AzureRM.Insights Cmdlets</span></span>
### [<span data-ttu-id="82c45-105">추가-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="82c45-105">Add-AzureRmAutoscaleSetting</span></span>](Add-AzureRmAutoscaleSetting.md)
<span data-ttu-id="82c45-106">자동 크기 조정 설정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="82c45-106">Creates an Autoscale setting.</span></span>

### [<span data-ttu-id="82c45-107">추가-AzureRmLogAlertRule</span><span class="sxs-lookup"><span data-stu-id="82c45-107">Add-AzureRmLogAlertRule</span></span>](Add-AzureRmLogAlertRule.md)
<span data-ttu-id="82c45-108">로그 알림 규칙을 추가 하거나 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="82c45-108">Adds or replaces a log alert rule.</span></span>

### [<span data-ttu-id="82c45-109">추가-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="82c45-109">Add-AzureRmLogProfile</span></span>](Add-AzureRmLogProfile.md)
<span data-ttu-id="82c45-110">새 활동 로그 프로필을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="82c45-110">Creates a new activity log profile.</span></span> <span data-ttu-id="82c45-111">이 프로필을 사용 하 여 활동 로그를 Azure storage 계정에 보관 하거나 같은 구독의 Azure 이벤트 허브에 스트리밍할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="82c45-111">This profile is used to either archive the activity log to an Azure storage account or stream it to an Azure event hub in the same subscription.</span></span> 

- <span data-ttu-id="82c45-112">**저장소 계정** -표준 저장소 계정 (premium 저장소 계정 (지원 되지 않음)이 지원 되지 않음).</span><span class="sxs-lookup"><span data-stu-id="82c45-112">**Storage Account** - Only standard storage account (premium storage account is not supported) is supported.</span></span> <span data-ttu-id="82c45-113">ARM 또는 클래식 형식이 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="82c45-113">It could either be of type ARM or Classic.</span></span> <span data-ttu-id="82c45-114">저장소 계정에 기록 된 경우 활동 로그를 저장 하는 비용은 표준 저장소 요금으로 청구 됩니다.</span><span class="sxs-lookup"><span data-stu-id="82c45-114">If it's logged to a storage account, the cost of storing the activity log is billed at normal standard storage rates.</span></span> <span data-ttu-id="82c45-115">구독 당 하나의 로그 프로필만 있을 수 있습니다 consequentially 활동 로그 내보내기에는 구독 당 하나의 저장소 계정만 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="82c45-115">There could be only one log profile per subscription consequentially only one storage account per subscription can be used to export activity log.</span></span> 

- <span data-ttu-id="82c45-116">**이벤트 허브** -구독 당 하나의 로그 프로필만 사용할 수 있습니다 consequentially 활동 로그 내보내기에는 구독 당 하나의 이벤트 허브가 있을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="82c45-116">**Event Hub** - There could be only one log profile per subscription consequentially only one event hub per subscription can be used to export activity log.</span></span> <span data-ttu-id="82c45-117">활동 로그가 이벤트 허브로 스트리밍되는 경우 표준 이벤트 허브 가격이 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="82c45-117">If activity log is streamed to an event hub, standard event hub pricing will apply.</span></span> 

<span data-ttu-id="82c45-118">활동 로그에서 이벤트는 지역과 관련이 있거나 "전역" 일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="82c45-118">In the activity log, events can pertain to a region or could be "Global".</span></span> <span data-ttu-id="82c45-119">전역 본질적으로 이러한 이벤트는 영역 agnostics 지역에 관계 없이 대부분의 이벤트가이 범주에 속합니다.</span><span class="sxs-lookup"><span data-stu-id="82c45-119">Global essentially means these events are region agnostics and are independent of region, in fact majority of events fall into this category.</span></span> <span data-ttu-id="82c45-120">활동 로그 프로필이 포털에서 설정 된 경우 사용자 인터페이스에서 선택한 다른 지역과 함께 "Global"이 암시적으로 추가 됩니다.</span><span class="sxs-lookup"><span data-stu-id="82c45-120">If the activity log profile is set from the portal, it implicitly adds "Global" along with any other region selected in the user interface.</span></span> <span data-ttu-id="82c45-121">Cmdlet을 사용 하는 경우에는 "전역"으로 위치를 명시적으로 다른 지역과 별도로 언급 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="82c45-121">When using the cmdlet, the location as "Global" must be explicitly mentioned apart from any other region.</span></span> 

<span data-ttu-id="82c45-122">**참고** : **위치에 "Global"을 설정 하지 않으면 대부분의 활동 로그가 내보내지지 않습니다.**</span><span class="sxs-lookup"><span data-stu-id="82c45-122">**Note** :- **Failing to set "Global" in the locations will result in a majority of activity log not getting exported.**</span></span> 

### [<span data-ttu-id="82c45-123">추가-AzureRmMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="82c45-123">Add-AzureRmMetricAlertRule</span></span>](Add-AzureRmMetricAlertRule.md)
<span data-ttu-id="82c45-124">메트릭 기반 알림 규칙을 추가 하거나 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="82c45-124">Adds or updates a metric-based alert rule.</span></span>

### [<span data-ttu-id="82c45-125">추가-AzureRmWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="82c45-125">Add-AzureRmWebtestAlertRule</span></span>](Add-AzureRmWebtestAlertRule.md)
<span data-ttu-id="82c45-126">Webtest 경고 규칙을 추가 하거나 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="82c45-126">Adds or updates a webtest alert rule.</span></span>

### [<span data-ttu-id="82c45-127">Disable-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="82c45-127">Disable-AzureRmActivityLogAlert</span></span>](Disable-AzureRmActivityLogAlert.md)
<span data-ttu-id="82c45-128">활동 로그 알림을 비활성화 하 고 해당 태그를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="82c45-128">Disables an activity log alert and sets its tags.</span></span>

### [<span data-ttu-id="82c45-129">Enable-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="82c45-129">Enable-AzureRmActivityLogAlert</span></span>](Enable-AzureRmActivityLogAlert.md)
<span data-ttu-id="82c45-130">활동 로그 알림을 사용 하 고 해당 태그를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="82c45-130">Enables an activity log alert and sets its Tags.</span></span>

### [<span data-ttu-id="82c45-131">Get-AzureRmActionGroup</span><span class="sxs-lookup"><span data-stu-id="82c45-131">Get-AzureRmActionGroup</span></span>](Get-AzureRmActionGroup.md)
<span data-ttu-id="82c45-132">작업 그룹을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="82c45-132">Gets action group(s).</span></span>

### [<span data-ttu-id="82c45-133">Get-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="82c45-133">Get-AzureRmActivityLogAlert</span></span>](Get-AzureRmActivityLogAlert.md)
<span data-ttu-id="82c45-134">하나 이상의 활동 로그 알림 리소스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="82c45-134">Gets one or more activity log alert resources.</span></span>

### [<span data-ttu-id="82c45-135">Get-AzureRmAlertHistory</span><span class="sxs-lookup"><span data-stu-id="82c45-135">Get-AzureRmAlertHistory</span></span>](Get-AzureRmAlertHistory.md)
<span data-ttu-id="82c45-136">알림 기록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="82c45-136">Gets the history of alerts.</span></span>

### [<span data-ttu-id="82c45-137">Get-AzureRmAlertRule</span><span class="sxs-lookup"><span data-stu-id="82c45-137">Get-AzureRmAlertRule</span></span>](Get-AzureRmAlertRule.md)
<span data-ttu-id="82c45-138">알림 규칙을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="82c45-138">Gets alert rules.</span></span>

### [<span data-ttu-id="82c45-139">Get-AzureRmAutoscaleHistory</span><span class="sxs-lookup"><span data-stu-id="82c45-139">Get-AzureRmAutoscaleHistory</span></span>](Get-AzureRmAutoscaleHistory.md)
<span data-ttu-id="82c45-140">자동 크기 조정 기록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="82c45-140">Gets the Autoscale history.</span></span>

### [<span data-ttu-id="82c45-141">Get-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="82c45-141">Get-AzureRmAutoscaleSetting</span></span>](Get-AzureRmAutoscaleSetting.md)
<span data-ttu-id="82c45-142">자동 크기 조정 설정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="82c45-142">Gets Autoscale settings.</span></span>

### [<span data-ttu-id="82c45-143">Get-AzureRmDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="82c45-143">Get-AzureRmDiagnosticSetting</span></span>](Get-AzureRmDiagnosticSetting.md)
<span data-ttu-id="82c45-144">기록 된 범주와 시간 grains를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="82c45-144">Gets the logged categories and time grains.</span></span>

### [<span data-ttu-id="82c45-145">Get-AzureRmLog</span><span class="sxs-lookup"><span data-stu-id="82c45-145">Get-AzureRmLog</span></span>](Get-AzureRmLog.md)
<span data-ttu-id="82c45-146">이벤트의 로그를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="82c45-146">Gets a log of events.</span></span>

### [<span data-ttu-id="82c45-147">Get-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="82c45-147">Get-AzureRmLogProfile</span></span>](Get-AzureRmLogProfile.md)
<span data-ttu-id="82c45-148">로그 프로필을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="82c45-148">Gets a log profile.</span></span>

### [<span data-ttu-id="82c45-149">Get-AzureRmMetric</span><span class="sxs-lookup"><span data-stu-id="82c45-149">Get-AzureRmMetric</span></span>](Get-AzureRmMetric.md)
<span data-ttu-id="82c45-150">리소스의 메트릭 값을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="82c45-150">Gets the metric values of a resource.</span></span>

### [<span data-ttu-id="82c45-151">Get-AzureRmMetricDefinition</span><span class="sxs-lookup"><span data-stu-id="82c45-151">Get-AzureRmMetricDefinition</span></span>](Get-AzureRmMetricDefinition.md)
<span data-ttu-id="82c45-152">메트릭 정의를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="82c45-152">Gets metric definitions.</span></span>

### [<span data-ttu-id="82c45-153">Get-AzureRmUsage</span><span class="sxs-lookup"><span data-stu-id="82c45-153">Get-AzureRmUsage</span></span>](Get-AzureRmUsage.md)
<span data-ttu-id="82c45-154">리소스에 대 한 사용 메트릭을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="82c45-154">Gets the usage metrics for a resource.</span></span>

### [<span data-ttu-id="82c45-155">새로운 AzureRmActionGroup</span><span class="sxs-lookup"><span data-stu-id="82c45-155">New-AzureRmActionGroup</span></span>](New-AzureRmActionGroup.md)
<span data-ttu-id="82c45-156">메모리에 ActionGroup reference 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="82c45-156">Creates an ActionGroup reference object in memory.</span></span>

### [<span data-ttu-id="82c45-157">새로운 AzureRmActionGroupReceiver</span><span class="sxs-lookup"><span data-stu-id="82c45-157">New-AzureRmActionGroupReceiver</span></span>](New-AzureRmActionGroupReceiver.md)
<span data-ttu-id="82c45-158">새 작업 그룹 수신기를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="82c45-158">Creates an new action group receiver.</span></span>

### [<span data-ttu-id="82c45-159">새로운 AzureRmActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="82c45-159">New-AzureRmActivityLogAlertCondition</span></span>](New-AzureRmActivityLogAlertCondition.md)
<span data-ttu-id="82c45-160">메모리에 새 활동 로그 알림 조건 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="82c45-160">Creates an new activity log alert condition object in memory.</span></span>

### [<span data-ttu-id="82c45-161">새로운 AzureRmAlertRuleEmail</span><span class="sxs-lookup"><span data-stu-id="82c45-161">New-AzureRmAlertRuleEmail</span></span>](New-AzureRmAlertRuleEmail.md)
<span data-ttu-id="82c45-162">경고 규칙에 대 한 전자 메일 작업을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="82c45-162">Creates an email action for an alert rule.</span></span>

### [<span data-ttu-id="82c45-163">새로운 AzureRmAlertRuleWebhook</span><span class="sxs-lookup"><span data-stu-id="82c45-163">New-AzureRmAlertRuleWebhook</span></span>](New-AzureRmAlertRuleWebhook.md)
<span data-ttu-id="82c45-164">알림 규칙 webhook을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="82c45-164">Creates an alert rule webhook.</span></span>

### [<span data-ttu-id="82c45-165">새로운 AzureRmAutoscaleNotification</span><span class="sxs-lookup"><span data-stu-id="82c45-165">New-AzureRmAutoscaleNotification</span></span>](New-AzureRmAutoscaleNotification.md)
<span data-ttu-id="82c45-166">자동 크기 조정 전자 메일 알림을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="82c45-166">Creates an Autoscale email notification.</span></span>

### [<span data-ttu-id="82c45-167">새로운 AzureRmAutoscaleProfile</span><span class="sxs-lookup"><span data-stu-id="82c45-167">New-AzureRmAutoscaleProfile</span></span>](New-AzureRmAutoscaleProfile.md)
<span data-ttu-id="82c45-168">자동 크기 조정 프로필을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="82c45-168">Creates an Autoscale profile.</span></span>

### [<span data-ttu-id="82c45-169">새로운 AzureRmAutoscaleRule</span><span class="sxs-lookup"><span data-stu-id="82c45-169">New-AzureRmAutoscaleRule</span></span>](New-AzureRmAutoscaleRule.md)
<span data-ttu-id="82c45-170">자동 크기 조정 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="82c45-170">Creates an Autoscale rule.</span></span>

### [<span data-ttu-id="82c45-171">새로운 AzureRmAutoscaleWebhook</span><span class="sxs-lookup"><span data-stu-id="82c45-171">New-AzureRmAutoscaleWebhook</span></span>](New-AzureRmAutoscaleWebhook.md)
<span data-ttu-id="82c45-172">자동 크기 조정 webhook을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="82c45-172">Creates an Autoscale webhook.</span></span>

### [<span data-ttu-id="82c45-173">제거-AzureRmActionGroup</span><span class="sxs-lookup"><span data-stu-id="82c45-173">Remove-AzureRmActionGroup</span></span>](Remove-AzureRmActionGroup.md)
<span data-ttu-id="82c45-174">작업 그룹을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="82c45-174">Removes an action group.</span></span>

### [<span data-ttu-id="82c45-175">제거-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="82c45-175">Remove-AzureRmActivityLogAlert</span></span>](Remove-AzureRmActivityLogAlert.md)
<span data-ttu-id="82c45-176">활동 로그 알림을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="82c45-176">Removes an activity log alert.</span></span>

### [<span data-ttu-id="82c45-177">제거-AzureRmAlertRule</span><span class="sxs-lookup"><span data-stu-id="82c45-177">Remove-AzureRmAlertRule</span></span>](Remove-AzureRmAlertRule.md)
<span data-ttu-id="82c45-178">알림 규칙을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="82c45-178">Removes an alert rule.</span></span>

### [<span data-ttu-id="82c45-179">제거-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="82c45-179">Remove-AzureRmAutoscaleSetting</span></span>](Remove-AzureRmAutoscaleSetting.md)
<span data-ttu-id="82c45-180">자동 크기 조정 설정을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="82c45-180">Removes an Autoscale setting.</span></span>

### [<span data-ttu-id="82c45-181">제거-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="82c45-181">Remove-AzureRmLogProfile</span></span>](Remove-AzureRmLogProfile.md)
<span data-ttu-id="82c45-182">로그 프로필을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="82c45-182">Removes a log profile.</span></span>

### [<span data-ttu-id="82c45-183">Set-AzureRmActionGroup</span><span class="sxs-lookup"><span data-stu-id="82c45-183">Set-AzureRmActionGroup</span></span>](Set-AzureRmActionGroup.md)
<span data-ttu-id="82c45-184">새를 만들거나 기존 작업 그룹을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="82c45-184">Creates a new or updates an existing action group.</span></span>

### [<span data-ttu-id="82c45-185">Set-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="82c45-185">Set-AzureRmActivityLogAlert</span></span>](Set-AzureRmActivityLogAlert.md)
<span data-ttu-id="82c45-186">기존 활동 로그 알림을 새로 만들거나 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="82c45-186">Creates a new or sets an existing activity log alert.</span></span>

### [<span data-ttu-id="82c45-187">Set-AzureRmDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="82c45-187">Set-AzureRmDiagnosticSetting</span></span>](Set-AzureRmDiagnosticSetting.md)
<span data-ttu-id="82c45-188">리소스에 대 한 로그 및 메트릭 설정을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="82c45-188">Sets the logs and metrics settings for the resource.</span></span>

