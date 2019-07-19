---
ms.openlocfilehash: ffeba2cff2e157e7ec0fb7639f9d4075c359c85e
ms.sourcegitcommit: 0b644bfecf4224b2ea83520d1a6a956734d9fba4
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/12/2019
ms.locfileid: "67863831"
---
## <a name="180---april-2019"></a><span data-ttu-id="cb7b9-101">1.8.0 - 2019년 4월</span><span class="sxs-lookup"><span data-stu-id="cb7b9-101">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="cb7b9-102">마지막 주 릴리스 이후의 주요 사항</span><span class="sxs-lookup"><span data-stu-id="cb7b9-102">Highlights since the last major release</span></span>
* <span data-ttu-id="cb7b9-103">`Az` 모듈 일반 공급</span><span class="sxs-lookup"><span data-stu-id="cb7b9-103">General availability of `Az` module</span></span>
* <span data-ttu-id="cb7b9-104">`Az` 모듈에 대한 자세한 내용은 https://aka.ms/azps-announce 를 방문하세요.</span><span class="sxs-lookup"><span data-stu-id="cb7b9-104">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="cb7b9-105">Location, ResourceGroup 및 ResourceName 완성자가 추가되었습니다(https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/ ).</span><span class="sxs-lookup"><span data-stu-id="cb7b9-105">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="cb7b9-106">와일드카드 지원이 Az.Compute 및 Az.Network에 대한 Get cmdlet에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="cb7b9-106">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="cb7b9-107">Windows PowerShell 5.1 전용 대화형 사용자 이름/암호 인증이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="cb7b9-107">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="cb7b9-108">Python 2 Runbook 지원이 Az.Automation에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="cb7b9-108">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="cb7b9-109">Az.LogicApp: 통합 계정 어셈블리 및 일괄 처리 구성을 위한 새로운 cmdlet입니다.</span><span class="sxs-lookup"><span data-stu-id="cb7b9-109">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="cb7b9-110">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="cb7b9-110">Az.Accounts</span></span>
* <span data-ttu-id="cb7b9-111">Mac에서 모듈을 올바르게 삭제하기 위해 Uninstall-AzureRm을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="cb7b9-111">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="cb7b9-112">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="cb7b9-112">Az.Batch</span></span>
* <span data-ttu-id="cb7b9-113">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="cb7b9-113">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="cb7b9-114">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="cb7b9-114">Az.Cdn</span></span>
* <span data-ttu-id="cb7b9-115">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="cb7b9-115">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="cb7b9-116">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="cb7b9-116">Az.CognitiveServices</span></span>
* <span data-ttu-id="cb7b9-117">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="cb7b9-117">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="cb7b9-118">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cb7b9-118">Az.Compute</span></span>
* <span data-ttu-id="cb7b9-119">디스크의 리소스 ID에 리소스 ID의 소문자 resourcegroups가 있는 경우 AEM 설치 문제 수정</span><span class="sxs-lookup"><span data-stu-id="cb7b9-119">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="cb7b9-120">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="cb7b9-120">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="cb7b9-121">와일드 카드에 대한 설명서 수정</span><span class="sxs-lookup"><span data-stu-id="cb7b9-121">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="cb7b9-122">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="cb7b9-122">Az.DataFactory</span></span>
* <span data-ttu-id="cb7b9-123">NodeCount가 관리형 통합 런타임에 대해 Null이 아닌 경우 SsisProperties를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="cb7b9-123">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="cb7b9-124">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="cb7b9-124">Az.DataLakeStore</span></span>
* <span data-ttu-id="cb7b9-125">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="cb7b9-125">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="cb7b9-126">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="cb7b9-126">Az.EventGrid</span></span>
* <span data-ttu-id="cb7b9-127">이벤트 구독 cmdlet 만들기/업데이트를 사용하기 전에 리소스를 만들어야 함을 나타내기 위해 엔드포인트의 도움말 텍스트가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="cb7b9-127">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="cb7b9-128">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="cb7b9-128">Az.EventHub</span></span>
* <span data-ttu-id="cb7b9-129">네임스페이스의 NetworkRuleSet에 대한 새 cmdlet가 추가되었습니다</span><span class="sxs-lookup"><span data-stu-id="cb7b9-129">Added new cmdlets for NetworkRuleSet of Namespace</span></span> 

#### <a name="azhdinsight"></a><span data-ttu-id="cb7b9-130">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="cb7b9-130">Az.HDInsight</span></span>
* <span data-ttu-id="cb7b9-131">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="cb7b9-131">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="cb7b9-132">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="cb7b9-132">Az.IotHub</span></span>
* <span data-ttu-id="cb7b9-133">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="cb7b9-133">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="cb7b9-134">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="cb7b9-134">Az.KeyVault</span></span>
* <span data-ttu-id="cb7b9-135">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="cb7b9-135">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="cb7b9-136">와일드 카드에 대한 설명서 수정</span><span class="sxs-lookup"><span data-stu-id="cb7b9-136">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="cb7b9-137">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="cb7b9-137">Az.MachineLearning</span></span>
* <span data-ttu-id="cb7b9-138">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="cb7b9-138">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="cb7b9-139">Az.Media</span><span class="sxs-lookup"><span data-stu-id="cb7b9-139">Az.Media</span></span>
* <span data-ttu-id="cb7b9-140">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="cb7b9-140">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="cb7b9-141">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="cb7b9-141">Az.Monitor</span></span>
  * <span data-ttu-id="cb7b9-142">GenV2(비 클래식) 메트릭 기반 경고 규칙에 대한 새 cmdlet</span><span class="sxs-lookup"><span data-stu-id="cb7b9-142">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="cb7b9-143">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="cb7b9-143">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="cb7b9-144">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="cb7b9-144">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="cb7b9-145">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="cb7b9-145">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="cb7b9-146">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="cb7b9-146">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="cb7b9-147">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="cb7b9-147">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="cb7b9-148">모니터 SDK가 버전 0.22.0-preview로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="cb7b9-148">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="cb7b9-149">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cb7b9-149">Az.Network</span></span>
* <span data-ttu-id="cb7b9-150">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="cb7b9-150">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="cb7b9-151">와일드 카드에 대한 설명서 수정</span><span class="sxs-lookup"><span data-stu-id="cb7b9-151">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="cb7b9-152">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="cb7b9-152">Az.NotificationHubs</span></span>
* <span data-ttu-id="cb7b9-153">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="cb7b9-153">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="cb7b9-154">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="cb7b9-154">Az.OperationalInsights</span></span>
* <span data-ttu-id="cb7b9-155">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="cb7b9-155">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="cb7b9-156">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="cb7b9-156">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="cb7b9-157">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="cb7b9-157">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="cb7b9-158">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="cb7b9-158">Az.RecoveryServices</span></span>
* <span data-ttu-id="cb7b9-159">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="cb7b9-159">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="cb7b9-160">Azure VM의 SQL용 테이블 형식이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="cb7b9-160">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="cb7b9-161">AzureFileShare에서 위치를 가져오는 대체 메서드가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="cb7b9-161">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="cb7b9-162">시간대에 따라 SchedulePolicy 개체의 ScheduleRunDays가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="cb7b9-162">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="cb7b9-163">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="cb7b9-163">Az.RedisCache</span></span>
* <span data-ttu-id="cb7b9-164">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="cb7b9-164">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="cb7b9-165">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cb7b9-165">Az.Resources</span></span>
* <span data-ttu-id="cb7b9-166">와일드 카드에 대한 설명서 수정</span><span class="sxs-lookup"><span data-stu-id="cb7b9-166">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="cb7b9-167">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cb7b9-167">Az.Sql</span></span>
* <span data-ttu-id="cb7b9-168">Monitor SDK의 종속성을 공용 코드로 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="cb7b9-168">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="cb7b9-169">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="cb7b9-169">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="cb7b9-170">다중 열 분류 프로세스가 향상되었습니다.</span><span class="sxs-lookup"><span data-stu-id="cb7b9-170">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="cb7b9-171">기본적으로 Get-AzSqlServerServiceObjective의 응답으로 SKU 속성(SKU 이름, 제품군, 용량)과 테이블 형식을 포함합니다.</span><span class="sxs-lookup"><span data-stu-id="cb7b9-171">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="cb7b9-172">해당 지역에 기존 서버 없이 위치별로 Get-AzSqlServerServiceObjective를 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cb7b9-172">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="cb7b9-173">관리형 인스턴스 생성 시 표준 시간대 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="cb7b9-173">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="cb7b9-174">와일드 카드에 대한 설명서 수정</span><span class="sxs-lookup"><span data-stu-id="cb7b9-174">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="cb7b9-175">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="cb7b9-175">Az.Websites</span></span>
* <span data-ttu-id="cb7b9-176">실행 시 태그를 제거하지 않도록 Set-AzWebApp 및 Set-AzWebAppSlot를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="cb7b9-176">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="cb7b9-177">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="cb7b9-177">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="cb7b9-178">WebSites SDK가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="cb7b9-178">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="cb7b9-179">PSAppServicePlan에서 AdminSiteName 속성을 제거했습니다.</span><span class="sxs-lookup"><span data-stu-id="cb7b9-179">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="cb7b9-180">1.7.0 - 2019년 4월</span><span class="sxs-lookup"><span data-stu-id="cb7b9-180">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="cb7b9-181">마지막 주 릴리스 이후의 주요 사항</span><span class="sxs-lookup"><span data-stu-id="cb7b9-181">Highlights since the last major release</span></span>
* <span data-ttu-id="cb7b9-182">`Az` 모듈 일반 공급</span><span class="sxs-lookup"><span data-stu-id="cb7b9-182">General availability of `Az` module</span></span>
* <span data-ttu-id="cb7b9-183">`Az` 모듈에 대한 자세한 내용은 https://aka.ms/azps-announce 를 방문하세요.</span><span class="sxs-lookup"><span data-stu-id="cb7b9-183">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="cb7b9-184">Location, ResourceGroup 및 ResourceName 완성자가 추가되었습니다(https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/ ).</span><span class="sxs-lookup"><span data-stu-id="cb7b9-184">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="cb7b9-185">와일드카드 지원이 Az.Compute 및 Az.Network에 대한 Get cmdlet에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="cb7b9-185">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="cb7b9-186">Windows PowerShell 5.1 전용 대화형 사용자 이름/암호 인증이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="cb7b9-186">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="cb7b9-187">Python 2 Runbook 지원이 Az.Automation에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="cb7b9-187">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="cb7b9-188">Az.LogicApp: 통합 계정 어셈블리 및 일괄 처리 구성을 위한 새로운 cmdlet입니다.</span><span class="sxs-lookup"><span data-stu-id="cb7b9-188">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="cb7b9-189">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="cb7b9-189">Az.Accounts</span></span>
* <span data-ttu-id="cb7b9-190">매개 변수 AzureAnalysisServicesEndpointResourceId를 허용하도록 Add-AzEnvironment 및 Set-AzEnvironment 업데이트</span><span class="sxs-lookup"><span data-stu-id="cb7b9-190">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="cb7b9-191">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="cb7b9-191">Az.AnalysisServices</span></span>
* <span data-ttu-id="cb7b9-192">데이터 평면 cmdlet에서 ServiceClient 사용 및 원본 인증 논리 제거</span><span class="sxs-lookup"><span data-stu-id="cb7b9-192">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="cb7b9-193">호환성이 손상되는 변경을 방지하기 위해 Add-AzureASAccount를 Connect-AzAccount의 래퍼로 만듦</span><span class="sxs-lookup"><span data-stu-id="cb7b9-193">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="cb7b9-194">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="cb7b9-194">Az.Automation</span></span>
* <span data-ttu-id="cb7b9-195">포함에 대한 New-AzAutomationSoftwareUpdateConfiguration cmdlet 버그 수정</span><span class="sxs-lookup"><span data-stu-id="cb7b9-195">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="cb7b9-196">이제 매개 변수 IncludedKbNumber 및 IncludedPackageNameMask가 작동함</span><span class="sxs-lookup"><span data-stu-id="cb7b9-196">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="cb7b9-197">Azure 자동화 업데이트 관리 동적 그룹에 대한 버그 수정</span><span class="sxs-lookup"><span data-stu-id="cb7b9-197">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="cb7b9-198">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cb7b9-198">Az.Compute</span></span>
* <span data-ttu-id="cb7b9-199">New-AzDiskConfig 및 New-AzSnapshotConfig에 HyperVGeneration 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="cb7b9-199">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="cb7b9-200">다른 테넌트의 갤러리 이미지를 사용하여 VM을 만들 수 있음</span><span class="sxs-lookup"><span data-stu-id="cb7b9-200">Allow VM creation with galley image from other tenants.</span></span> 

#### <a name="azcontainerinstance"></a><span data-ttu-id="cb7b9-201">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="cb7b9-201">Az.ContainerInstance</span></span>
* <span data-ttu-id="cb7b9-202">후행 빈 인수를 추가한 New-AzContainerGroup의 -Command 매개 변수의 문제 수정</span><span class="sxs-lookup"><span data-stu-id="cb7b9-202">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="cb7b9-203">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="cb7b9-203">Az.DataFactory</span></span>
* <span data-ttu-id="cb7b9-204">ADF .Net SDK 버전을 3.0.2로 업데이트</span><span class="sxs-lookup"><span data-stu-id="cb7b9-204">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="cb7b9-205">RepoConfiguration 관련 설정에 대한 추가 매개 변수로 Set-AzDataFactoryV2 cmdlet을 업데이트</span><span class="sxs-lookup"><span data-stu-id="cb7b9-205">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="cb7b9-206">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cb7b9-206">Az.Resources</span></span>
* <span data-ttu-id="cb7b9-207">'-ResourceId' 또는 '-ResourceGroupName', '-Name' 및 '-ResourceType' 매개 변수를 제공할 때 'Get-AzResource'에 대한 공급자 처리 개선</span><span class="sxs-lookup"><span data-stu-id="cb7b9-207">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="cb7b9-208">'Test-AzDeployment' 및 'Test-AzResourceGroupDeployment'에 대한 오류 처리 개선</span><span class="sxs-lookup"><span data-stu-id="cb7b9-208">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="cb7b9-209">배포 유효성 검사 외부에서 발생한 오류를 처리하고 그 대신 명령의 출력에 포함</span><span class="sxs-lookup"><span data-stu-id="cb7b9-209">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="cb7b9-210">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/6856 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="cb7b9-210">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="cb7b9-211">배포 cmdlet 세트에 스크립트 및 작업 시나리오에서 프롬프트를 건너뛰는 '-IgnoreDynamicParameters' 스위치 추가</span><span class="sxs-lookup"><span data-stu-id="cb7b9-211">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="cb7b9-212">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/6856 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="cb7b9-212">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="cb7b9-213">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cb7b9-213">Az.Sql</span></span>
* <span data-ttu-id="cb7b9-214">데이터베이스 데이터 분류 지원</span><span class="sxs-lookup"><span data-stu-id="cb7b9-214">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="cb7b9-215">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="cb7b9-215">Az.Storage</span></span>
* <span data-ttu-id="cb7b9-216">매개 변수 -UseConnectedAccount를 사용하여 스토리지 컨텍스트를 만들 때 자세한 오류 보고(단, 로그인 Azure 계정 없이)</span><span class="sxs-lookup"><span data-stu-id="cb7b9-216">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="cb7b9-217">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="cb7b9-217">New-AzStorageContext</span></span>
* <span data-ttu-id="cb7b9-218">관리 평면 API를 사용하여 지정한 스토리지 계정의 BLOB 서비스 속성 관리 지원</span><span class="sxs-lookup"><span data-stu-id="cb7b9-218">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="cb7b9-219">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="cb7b9-219">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="cb7b9-220">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="cb7b9-220">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="cb7b9-221">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="cb7b9-221">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="cb7b9-222">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="cb7b9-222">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="cb7b9-223">BLOB 및 파일 업로드/다운로드 cmdlet에 대한 -AsJob 지원</span><span class="sxs-lookup"><span data-stu-id="cb7b9-223">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="cb7b9-224">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="cb7b9-224">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="cb7b9-225">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="cb7b9-225">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="cb7b9-226">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="cb7b9-226">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="cb7b9-227">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="cb7b9-227">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="cb7b9-228">1.6.0 - 2019년 3월</span><span class="sxs-lookup"><span data-stu-id="cb7b9-228">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="cb7b9-229">마지막 주 릴리스 이후의 주요 사항</span><span class="sxs-lookup"><span data-stu-id="cb7b9-229">Highlights since the last major release</span></span>
* <span data-ttu-id="cb7b9-230">`Az` 모듈 일반 공급</span><span class="sxs-lookup"><span data-stu-id="cb7b9-230">General availability of `Az` module</span></span>
* <span data-ttu-id="cb7b9-231">`Az` 모듈에 대한 자세한 내용은 https://aka.ms/azps-announce 를 방문하세요.</span><span class="sxs-lookup"><span data-stu-id="cb7b9-231">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="cb7b9-232">Location, ResourceGroup 및 ResourceName 완성자가 추가되었습니다(https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/ ).</span><span class="sxs-lookup"><span data-stu-id="cb7b9-232">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="cb7b9-233">와일드카드 지원이 Az.Compute 및 Az.Network에 대한 Get cmdlet에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="cb7b9-233">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="cb7b9-234">Windows PowerShell 5.1 전용 대화형 사용자 이름/암호 인증이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="cb7b9-234">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="cb7b9-235">Python 2 Runbook 지원이 Az.Automation에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="cb7b9-235">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="cb7b9-236">Az.LogicApp: 통합 계정 어셈블리 및 일괄 처리 구성을 위한 새로운 cmdlet입니다.</span><span class="sxs-lookup"><span data-stu-id="cb7b9-236">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="cb7b9-237">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="cb7b9-237">Az.Automation</span></span>
* <span data-ttu-id="cb7b9-238">Azure 자동화 업데이트 관리에서 변경된 지원 기능은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="cb7b9-238">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="cb7b9-239">동적 그룹화</span><span class="sxs-lookup"><span data-stu-id="cb7b9-239">Dynamic grouping</span></span>
    * <span data-ttu-id="cb7b9-240">사전 스크립트</span><span class="sxs-lookup"><span data-stu-id="cb7b9-240">Pre-Post script</span></span>
    * <span data-ttu-id="cb7b9-241">다시 부팅 설정</span><span class="sxs-lookup"><span data-stu-id="cb7b9-241">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="cb7b9-242">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cb7b9-242">Az.Compute</span></span>
* <span data-ttu-id="cb7b9-243">Get-AzVmBootDiagnosticsData의 경로 확인 문제가 해결되었습니다.</span><span class="sxs-lookup"><span data-stu-id="cb7b9-243">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="cb7b9-244">Compute 클라이언트 라이브러리가 25.0.0으로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="cb7b9-244">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="cb7b9-245">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="cb7b9-245">Az.KeyVault</span></span>
* <span data-ttu-id="cb7b9-246">와일드카드 지원이 KeyVault cmdlet에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="cb7b9-246">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="cb7b9-247">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cb7b9-247">Az.Network</span></span>
* <span data-ttu-id="cb7b9-248">Azure Firewall에 대한 위협 인텔리전스 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="cb7b9-248">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="cb7b9-249">Application Gateway 방화벽 정책의 최상위 수준 리소스 및 사용자 지정 규칙이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="cb7b9-249">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="cb7b9-250">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="cb7b9-250">Az.RecoveryServices</span></span>
* <span data-ttu-id="cb7b9-251">인스턴트 RP를 지원하기 위해 SnapshotRetentionInDays가 Azure VM 정책에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="cb7b9-251">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="cb7b9-252">컨테이너 등록을 취소하는 파이프 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="cb7b9-252">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="cb7b9-253">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cb7b9-253">Az.Resources</span></span>
* <span data-ttu-id="cb7b9-254">Get-AzResource 및 Get-AzResourceGroup에 대한 와일드카드 지원을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="cb7b9-254">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="cb7b9-255">ARM에 대한 일반 호출을 수행할 때 사용되는 자격 증명을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="cb7b9-255">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="cb7b9-256">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cb7b9-256">Az.Sql</span></span>
* <span data-ttu-id="cb7b9-257">위협 탐지의 cmdlet 매개 변수(ExcludeDetectionType)가 DetectionType에서 string[]으로 변경되어 새 DetectionType이 추가되면 이후의 증명이 되고 자동 완성도 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="cb7b9-257">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="cb7b9-258">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="cb7b9-258">Az.Storage</span></span>
* <span data-ttu-id="cb7b9-259">스토리지 계정에 대한 관리 정책 가져오기/설정/제거를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="cb7b9-259">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="cb7b9-260">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="cb7b9-260">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="cb7b9-261">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="cb7b9-261">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="cb7b9-262">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="cb7b9-262">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="cb7b9-263">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="cb7b9-263">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="cb7b9-264">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="cb7b9-264">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="cb7b9-265">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="cb7b9-265">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="cb7b9-266">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="cb7b9-266">Az.Websites</span></span>
* <span data-ttu-id="cb7b9-267">'New-AzWebApp -IncludeSourceWebAppSlots'를 사용하여 모든 슬롯의 복제를 중단하는 ARM 템플릿 버그가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="cb7b9-267">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span> 

## <a name="150---march-2019"></a><span data-ttu-id="cb7b9-268">1.5.0 - 2019년 3월</span><span class="sxs-lookup"><span data-stu-id="cb7b9-268">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="cb7b9-269">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="cb7b9-269">Az.Accounts</span></span>
* <span data-ttu-id="cb7b9-270">'Register-AzModule' 명령을 추가하여 AutoRest 생성 cmdlet을 지원</span><span class="sxs-lookup"><span data-stu-id="cb7b9-270">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="cb7b9-271">Connect-AzAccount 예제 업데이트</span><span class="sxs-lookup"><span data-stu-id="cb7b9-271">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="cb7b9-272">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="cb7b9-272">Az.Automation</span></span>
* <span data-ttu-id="cb7b9-273">몇몇 Azure Automation cmdlet에서 특정 월별 일정을 검색할 때 발생하는 문제 수정</span><span class="sxs-lookup"><span data-stu-id="cb7b9-273">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="cb7b9-274">상위 20개 노드를 반환하도록 Get-AzAutomationDscNode를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="cb7b9-274">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="cb7b9-275">이제 모든 노드 반환</span><span class="sxs-lookup"><span data-stu-id="cb7b9-275">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="cb7b9-276">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="cb7b9-276">Az.Cdn</span></span>
* <span data-ttu-id="cb7b9-277">사용자 지정 도메인 Https 사용/사용 안 함에 대한 새 Powershell cmdlet이 추가되었으며 기존의 것은 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="cb7b9-277">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="cb7b9-278">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cb7b9-278">Az.Compute</span></span>
* <span data-ttu-id="cb7b9-279">Get cmdlet에 와일드 카드 지원 추가</span><span class="sxs-lookup"><span data-stu-id="cb7b9-279">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="cb7b9-280">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="cb7b9-280">Az.DataFactory</span></span>
* <span data-ttu-id="cb7b9-281">ADF.Net SDK 버전이 3.0.1로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="cb7b9-281">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="cb7b9-282">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="cb7b9-282">Az.LogicApp</span></span>
* <span data-ttu-id="cb7b9-283">첫 결과 페이지 검색 시에만 ListWorkflows 수정</span><span class="sxs-lookup"><span data-stu-id="cb7b9-283">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="cb7b9-284">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cb7b9-284">Az.Network</span></span>
* <span data-ttu-id="cb7b9-285">Network cmdlet에 와일드 카드 지원 추가</span><span class="sxs-lookup"><span data-stu-id="cb7b9-285">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="cb7b9-286">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="cb7b9-286">Az.RecoveryServices</span></span>
* <span data-ttu-id="cb7b9-287">Azure VM 지원에 SQL 서버가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="cb7b9-287">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="cb7b9-288">SDK 업데이트</span><span class="sxs-lookup"><span data-stu-id="cb7b9-288">SDK Update</span></span>
* <span data-ttu-id="cb7b9-289">VMappContainer 체크 인 Get-ProtectableItem 제거</span><span class="sxs-lookup"><span data-stu-id="cb7b9-289">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="cb7b9-290">Get ProtectableItem의 매개 변수로 Name과 ServerName이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="cb7b9-290">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="cb7b9-291">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cb7b9-291">Az.Resources</span></span>
* <span data-ttu-id="cb7b9-292">`-TemplateObject` 매개 변수를 추가하여 cmdlet을 배포</span><span class="sxs-lookup"><span data-stu-id="cb7b9-292">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="cb7b9-293">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/2933 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="cb7b9-293">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="cb7b9-294">`Get-AzResource`의 결과를 `Set-AzResource`(으)로 파이프할 때 발생하는 문제 수정</span><span class="sxs-lookup"><span data-stu-id="cb7b9-294">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="cb7b9-295">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/8240 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="cb7b9-295">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="cb7b9-296">실행 시 JSON 데이터 형식 문제 해결 `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="cb7b9-296">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="cb7b9-297">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/7930 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="cb7b9-297">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="cb7b9-298">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cb7b9-298">Az.Sql</span></span>
* <span data-ttu-id="cb7b9-299">AuditingEndpointsCommunicator를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="cb7b9-299">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="cb7b9-300">새 진단 설정을 생성할 때 에지 사례의 동작을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="cb7b9-300">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="cb7b9-301">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="cb7b9-301">Az.Storage</span></span>
* <span data-ttu-id="cb7b9-302">스토리지 계정      - New-AzStorageAccount를 생성할 때 종류 BlockBlobStorage를 지원</span><span class="sxs-lookup"><span data-stu-id="cb7b9-302">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="cb7b9-303">1.4.0 - 2019년 2월</span><span class="sxs-lookup"><span data-stu-id="cb7b9-303">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="cb7b9-304">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="cb7b9-304">Az.AnalysisServices</span></span>
* <span data-ttu-id="cb7b9-305">사용되지 않는 AddAzureASAccount cmdlet</span><span class="sxs-lookup"><span data-stu-id="cb7b9-305">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="cb7b9-306">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="cb7b9-306">Az.Automation</span></span>
* <span data-ttu-id="cb7b9-307">Import-AzAutomationDscNodeConfiguration 도움말 업데이트</span><span class="sxs-lookup"><span data-stu-id="cb7b9-307">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="cb7b9-308">Import-AzAutomationDscConfiguration cmdlet 구성 이름 유효성 검사 추가</span><span class="sxs-lookup"><span data-stu-id="cb7b9-308">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="cb7b9-309">Import-AzAutomationDscConfiguration cmdlet 오류 처리 개선</span><span class="sxs-lookup"><span data-stu-id="cb7b9-309">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="cb7b9-310">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="cb7b9-310">Az.CognitiveServices</span></span>
* <span data-ttu-id="cb7b9-311">리소스의 하위 도메인을 지정하는 데 사용되는 New-AzCognitiveServicesAccount에 대한 새 선택적 매개 변수로 CustomSubdomainName이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="cb7b9-311">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="cb7b9-312">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cb7b9-312">Az.Compute</span></span>
* <span data-ttu-id="cb7b9-313">ID 매개 변수 집합 문제 해결</span><span class="sxs-lookup"><span data-stu-id="cb7b9-313">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="cb7b9-314">Name 매개 변수를 제공하지 않으면 Get-AzVMExtension이 설치된 모든 확장을 열거하도록 업데이트</span><span class="sxs-lookup"><span data-stu-id="cb7b9-314">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="cb7b9-315">Update-AzImage cmdlet에 태그 및 ResourceId 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="cb7b9-315">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="cb7b9-316">인스턴스 ID가 없는 Get-AzVmssVM과 InstanceView를 사용하면 인스턴스 보기가 있는 VMSS VM을 나열할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cb7b9-316">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="cb7b9-317">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="cb7b9-317">Az.DataLakeStore</span></span>
* <span data-ttu-id="cb7b9-318">ADL 삭제된 항목 열거 및 복원에 대한 cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="cb7b9-318">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="cb7b9-319">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="cb7b9-319">Az.EventHub</span></span>
* <span data-ttu-id="cb7b9-320">Eventhub의 CaptureDescription 클래스에서 빈 보관을 건너뛰는 새 부울 속성 SkipEmptyArchives가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="cb7b9-320">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span> 

#### <a name="azkeyvault"></a><span data-ttu-id="cb7b9-321">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="cb7b9-321">Az.KeyVault</span></span>
* <span data-ttu-id="cb7b9-322">Set-AzKeyVaultSecret 태그 지정 수정</span><span class="sxs-lookup"><span data-stu-id="cb7b9-322">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="cb7b9-323">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="cb7b9-323">Az.LogicApp</span></span>
* <span data-ttu-id="cb7b9-324">통합 계정에 대한 기본 sku 추가</span><span class="sxs-lookup"><span data-stu-id="cb7b9-324">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="cb7b9-325">XSLT 2.0, XSLT 3.0, Liquid 맵 형식 추가</span><span class="sxs-lookup"><span data-stu-id="cb7b9-325">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="cb7b9-326">통합 계정 어셈블리에 대한 새 cmdlet</span><span class="sxs-lookup"><span data-stu-id="cb7b9-326">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="cb7b9-327">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="cb7b9-327">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="cb7b9-328">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="cb7b9-328">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="cb7b9-329">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="cb7b9-329">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="cb7b9-330">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="cb7b9-330">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="cb7b9-331">통합 계정 일괄 처리 구성에 대한 새 cmdlet</span><span class="sxs-lookup"><span data-stu-id="cb7b9-331">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="cb7b9-332">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="cb7b9-332">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="cb7b9-333">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="cb7b9-333">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="cb7b9-334">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="cb7b9-334">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="cb7b9-335">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="cb7b9-335">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="cb7b9-336">논리 앱 SDK를 버전 4.1.0으로 업데이트</span><span class="sxs-lookup"><span data-stu-id="cb7b9-336">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="cb7b9-337">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="cb7b9-337">Az.Monitor</span></span>
* <span data-ttu-id="cb7b9-338">Get-AzMetric에 대한 도움말 업데이트</span><span class="sxs-lookup"><span data-stu-id="cb7b9-338">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="cb7b9-339">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cb7b9-339">Az.Network</span></span>
* <span data-ttu-id="cb7b9-340">Add-AzApplicationGatewayCustomError에 대한 도움말 예제 업데이트</span><span class="sxs-lookup"><span data-stu-id="cb7b9-340">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="cb7b9-341">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="cb7b9-341">Az.OperationalInsights</span></span>
* <span data-ttu-id="cb7b9-342">New 및 Get ApplicationInsights 데이터 소스에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="cb7b9-342">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="cb7b9-343">지정된 작업 영역에 대한 특정 또는 전체 ApplicationInsights 데이터 원본 가져오기를 지원하기 위한 새로운 'ApplicationInsights' 종류가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="cb7b9-343">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span> 
    - <span data-ttu-id="cb7b9-344">지정된 Application-Insights 리소스 매개 변수(구독 ID, resourceGroupName 및 이름)별로 데이터 원본을 만들기 위한 New-AzOperationalInsightsApplicationInsightsDataSource cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="cb7b9-344">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span> 

#### <a name="azresources"></a><span data-ttu-id="cb7b9-345">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cb7b9-345">Az.Resources</span></span>
* <span data-ttu-id="cb7b9-346">문제 https://github.com/Azure/azure-powershell/issues/8166 수정</span><span class="sxs-lookup"><span data-stu-id="cb7b9-346">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="cb7b9-347">문제 https://github.com/Azure/azure-powershell/issues/8235 수정</span><span class="sxs-lookup"><span data-stu-id="cb7b9-347">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="cb7b9-348">문제 https://github.com/Azure/azure-powershell/issues/6219 수정</span><span class="sxs-lookup"><span data-stu-id="cb7b9-348">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="cb7b9-349">KeyCredentials 반복 만들기를 방지하기 위해 버그 수정</span><span class="sxs-lookup"><span data-stu-id="cb7b9-349">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="cb7b9-350">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cb7b9-350">Az.Sql</span></span>
* <span data-ttu-id="cb7b9-351">SQL DB 하이퍼스케일에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="cb7b9-351">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="cb7b9-352">복원 요청에서 불필요한 속성을 설정하여 복원이 실패할 수 있는 버그 수정</span><span class="sxs-lookup"><span data-stu-id="cb7b9-352">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="cb7b9-353">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="cb7b9-353">Az.Websites</span></span>
* <span data-ttu-id="cb7b9-354">Get-AzWebAppSlotMetrics 내 올바른 예제</span><span class="sxs-lookup"><span data-stu-id="cb7b9-354">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="cb7b9-355">1.3.0 - 2019년 2월</span><span class="sxs-lookup"><span data-stu-id="cb7b9-355">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="cb7b9-356">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="cb7b9-356">Az.Accounts</span></span>
* <span data-ttu-id="cb7b9-357">ClientRuntime 최신 버전 업데이트</span><span class="sxs-lookup"><span data-stu-id="cb7b9-357">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="cb7b9-358">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="cb7b9-358">Az.AnalysisServices</span></span>
<span data-ttu-id="cb7b9-359">Az.AnalysisServices 모듈의 전반적인 가용성.</span><span class="sxs-lookup"><span data-stu-id="cb7b9-359">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="cb7b9-360">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cb7b9-360">Az.Compute</span></span>
* <span data-ttu-id="cb7b9-361">AEM 확장: UltraSSD 및 P60, P70, P80 디스크에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="cb7b9-361">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="cb7b9-362">Set-AzVMBootDiagnostics에 대한 도움말 업데이트</span><span class="sxs-lookup"><span data-stu-id="cb7b9-362">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="cb7b9-363">Update-AzImage에 대한 도움말 및 예제 업데이트</span><span class="sxs-lookup"><span data-stu-id="cb7b9-363">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="cb7b9-364">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="cb7b9-364">Az.RecoveryServices</span></span>
<span data-ttu-id="cb7b9-365">Az.RecoveryServices 모듈의 전반적인 가용성.</span><span class="sxs-lookup"><span data-stu-id="cb7b9-365">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="cb7b9-366">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cb7b9-366">Az.Resources</span></span>
* <span data-ttu-id="cb7b9-367">리소스 그룹 관련 태그 수정</span><span class="sxs-lookup"><span data-stu-id="cb7b9-367">Fix tagging for resource groups</span></span> 
    - <span data-ttu-id="cb7b9-368">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/8166 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="cb7b9-368">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="cb7b9-369">`Get-AzureRmRoleAssignment`이(가) -ErrorAction을 준수하지 않는 문제 수정</span><span class="sxs-lookup"><span data-stu-id="cb7b9-369">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span> 
    - <span data-ttu-id="cb7b9-370">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/8235 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="cb7b9-370">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="cb7b9-371">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cb7b9-371">Az.Sql</span></span>
* <span data-ttu-id="cb7b9-372">AzSqlDatabaseBackupShortTermRetentionPolicy 가져오기/설정하기 추가</span><span class="sxs-lookup"><span data-stu-id="cb7b9-372">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="cb7b9-373">SQL cmdlet을 실행할 경우 Azure 계정에 로그인되어 있지 않은 것이 nullref 예외를 초래하는 문제 수정</span><span class="sxs-lookup"><span data-stu-id="cb7b9-373">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="cb7b9-374">Get-AzSqlCapability의 nullref 예외 수정</span><span class="sxs-lookup"><span data-stu-id="cb7b9-374">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="cb7b9-375">1.2.1 - 2019년 1월</span><span class="sxs-lookup"><span data-stu-id="cb7b9-375">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="cb7b9-376">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="cb7b9-376">Az.Accounts</span></span>
* <span data-ttu-id="cb7b9-377">올바른 인증 버전을 사용하여 릴리스</span><span class="sxs-lookup"><span data-stu-id="cb7b9-377">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="cb7b9-378">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="cb7b9-378">Az.AnalysisServices</span></span>
* <span data-ttu-id="cb7b9-379">업데이트된 인증 종속성을 사용하여 릴리스</span><span class="sxs-lookup"><span data-stu-id="cb7b9-379">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="cb7b9-380">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="cb7b9-380">Az.RecoveryServices</span></span>
* <span data-ttu-id="cb7b9-381">업데이트된 인증 종속성을 사용하여 릴리스</span><span class="sxs-lookup"><span data-stu-id="cb7b9-381">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="cb7b9-382">1.2.0 - 2019년 1월</span><span class="sxs-lookup"><span data-stu-id="cb7b9-382">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="cb7b9-383">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="cb7b9-383">Az.Accounts</span></span>
* <span data-ttu-id="cb7b9-384">Windows PowerShell 5.1 전용 대화형 사용자 이름/암호 인증 추가</span><span class="sxs-lookup"><span data-stu-id="cb7b9-384">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="cb7b9-385">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="cb7b9-385">Update incorrect online help URLs</span></span>
* <span data-ttu-id="cb7b9-386">Uninstall-AzureRm 관련 PS Core에 경고 메시지 추가</span><span class="sxs-lookup"><span data-stu-id="cb7b9-386">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="cb7b9-387">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="cb7b9-387">Az.Aks</span></span>
* <span data-ttu-id="cb7b9-388">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="cb7b9-388">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="cb7b9-389">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="cb7b9-389">Az.Automation</span></span>
* <span data-ttu-id="cb7b9-390">Python 2 Runbook에 대한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="cb7b9-390">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="cb7b9-391">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="cb7b9-391">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="cb7b9-392">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="cb7b9-392">Az.Cdn</span></span>
* <span data-ttu-id="cb7b9-393">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="cb7b9-393">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="cb7b9-394">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cb7b9-394">Az.Compute</span></span>
* <span data-ttu-id="cb7b9-395">Invoke-AzVMReimage cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="cb7b9-395">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="cb7b9-396">Set-AzVmss에 TempDisk 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="cb7b9-396">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="cb7b9-397">New-AzVM 경고 메시지 수정</span><span class="sxs-lookup"><span data-stu-id="cb7b9-397">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="cb7b9-398">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="cb7b9-398">Az.ContainerRegistry</span></span>
* <span data-ttu-id="cb7b9-399">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="cb7b9-399">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="cb7b9-400">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="cb7b9-400">Az.DataFactory</span></span>
* <span data-ttu-id="cb7b9-401">ADF.Net SDK 버전이 3.0.0으로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="cb7b9-401">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="cb7b9-402">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="cb7b9-402">Az.DataLakeStore</span></span>
* <span data-ttu-id="cb7b9-403">MSI를 사용할 때 ADLS 엔드포인트 문제 수정</span><span class="sxs-lookup"><span data-stu-id="cb7b9-403">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="cb7b9-404">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/7462 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="cb7b9-404">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="cb7b9-405">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="cb7b9-405">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="cb7b9-406">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="cb7b9-406">Az.IotHub</span></span>
* <span data-ttu-id="cb7b9-407">Add-IotHubRoutingEndpoint cmdlet에 인코딩 형식을 추가하세요.</span><span class="sxs-lookup"><span data-stu-id="cb7b9-407">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="cb7b9-408">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="cb7b9-408">Az.KeyVault</span></span>
* <span data-ttu-id="cb7b9-409">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="cb7b9-409">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="cb7b9-410">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cb7b9-410">Az.Network</span></span>
* <span data-ttu-id="cb7b9-411">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="cb7b9-411">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="cb7b9-412">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cb7b9-412">Az.Resources</span></span>
* <span data-ttu-id="cb7b9-413">'New-AzADAppCredential' 및 'New-AzADSpCredential' 참조 설명서의 잘못된 예제 수정</span><span class="sxs-lookup"><span data-stu-id="cb7b9-413">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="cb7b9-414">리소스 그룹 배포 cmdlet 실행 전 '-TemplateFile' 매개 변수 경로가 확인되지 않는 문제 수정</span><span class="sxs-lookup"><span data-stu-id="cb7b9-414">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="cb7b9-415">Az.Resources: New-AzureRmPolicyDefinition -Mode 기본값에 대한 올바른 설명서</span><span class="sxs-lookup"><span data-stu-id="cb7b9-415">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="cb7b9-416">Az.Resources: 문제 https://github.com/Azure/azure-powershell/issues/7522 수정</span><span class="sxs-lookup"><span data-stu-id="cb7b9-416">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="cb7b9-417">Az.Resources: 문제 https://github.com/Azure/azure-powershell/issues/5747 수정</span><span class="sxs-lookup"><span data-stu-id="cb7b9-417">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="cb7b9-418">'PSResourceGroupDeployment' 개체의 서식 문제 수정</span><span class="sxs-lookup"><span data-stu-id="cb7b9-418">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="cb7b9-419">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/2123 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="cb7b9-419">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="cb7b9-420">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="cb7b9-420">Az.ServiceFabric</span></span>
* <span data-ttu-id="cb7b9-421">인증서가 VMSS 모델에 추가되었는데도 예외가 발생할 경우 롤백합니다. 이는 버그 https://github.com/Azure/service-fabric-issues/issues/932 를 수정하기 위함입니다.</span><span class="sxs-lookup"><span data-stu-id="cb7b9-421">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="cb7b9-422">일부 오류 메시지를 수정하세요.</span><span class="sxs-lookup"><span data-stu-id="cb7b9-422">Fix some error messages.</span></span>
* <span data-ttu-id="cb7b9-423">Az로의 마이그레이션을 통해서는 작동하지 않는 New-AzServiceFabriCluster를 위해 기본값 ARM 템플릿을 가진 클러스터 만들기를 수정하세요.</span><span class="sxs-lookup"><span data-stu-id="cb7b9-423">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="cb7b9-424">확장에서 클러스터 id를 확인하여 클러스터에 해당하는 VMSS에만 추가되도록 클러스터/애플리케이션 인증서 추가를 수정하세요.</span><span class="sxs-lookup"><span data-stu-id="cb7b9-424">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="cb7b9-425">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="cb7b9-425">Az.SignalR</span></span>
* <span data-ttu-id="cb7b9-426">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="cb7b9-426">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="cb7b9-427">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cb7b9-427">Az.Sql</span></span>
* <span data-ttu-id="cb7b9-428">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="cb7b9-428">Update incorrect online help URLs</span></span>
* <span data-ttu-id="cb7b9-429">가능한 값을 가진 LicenseType 매개 변수에 대한 매개 변수 설명이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="cb7b9-429">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="cb7b9-430">유일하게 업데이트된 속성인데 작동하지 않는 관리되는 인스턴스 ID의 업데이트 수정</span><span class="sxs-lookup"><span data-stu-id="cb7b9-430">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="cb7b9-431">관리되는 인스턴스에서의 사용자 지정 데이터 정렬에 대한 지원</span><span class="sxs-lookup"><span data-stu-id="cb7b9-431">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="cb7b9-432">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="cb7b9-432">Az.Storage</span></span>
* <span data-ttu-id="cb7b9-433">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="cb7b9-433">Update incorrect online help URLs</span></span>
* <span data-ttu-id="cb7b9-434">Premium Storage 계정이 클래식 로깅/메트릭을 지원하지 않기 때문에, Premium Storage 계정의 클래식 로깅/메트릭을 가져올/설정할 때 상세한 오류 메시지를 제공해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="cb7b9-434">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="cb7b9-435">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="cb7b9-435">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="cb7b9-436">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="cb7b9-436">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="cb7b9-437">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="cb7b9-437">Az.TrafficManager</span></span>
* <span data-ttu-id="cb7b9-438">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="cb7b9-438">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="cb7b9-439">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="cb7b9-439">Az.Websites</span></span>
* <span data-ttu-id="cb7b9-440">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="cb7b9-440">Update incorrect online help URLs</span></span>
* <span data-ttu-id="cb7b9-441">앱이 ASE에 호스팅되면 'New-AzWebAppSSLBinding'을 수정하여 올바른 resourcegroup+location에 인증서를 업로드합니다.</span><span class="sxs-lookup"><span data-stu-id="cb7b9-441">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="cb7b9-442">'New-AzWebAppSSLBinding'을 수정하여 SSL 인증서를 앱에 바인딩하는 데 붙는 태그를 덮어쓰지 않도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="cb7b9-442">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="cb7b9-443">1.1.0 - 2019년 1월</span><span class="sxs-lookup"><span data-stu-id="cb7b9-443">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="cb7b9-444">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="cb7b9-444">Az.Accounts</span></span>
* <span data-ttu-id="cb7b9-445">Enable-AzureRmAlias에 'Local' 범위 추가</span><span class="sxs-lookup"><span data-stu-id="cb7b9-445">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="cb7b9-446">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cb7b9-446">Az.Compute</span></span>
* <span data-ttu-id="cb7b9-447">이름이 Restart/Start/Stop/Remove/Set-AzVM과 Save-AzVMImage에 설정된 ID 매개 변수에서 선택 사항이 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="cb7b9-447">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="cb7b9-448">도움말 파일의 ID에 대한 설명이 업데이트 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="cb7b9-448">Updated the description of ID in help files</span></span>
* <span data-ttu-id="cb7b9-449">Az.Accounts 모듈을 사용할 때의 이전 버전과의 호환성 문제를 해결합니다.</span><span class="sxs-lookup"><span data-stu-id="cb7b9-449">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="cb7b9-450">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="cb7b9-450">Az.DataLakeStore</span></span>
* <span data-ttu-id="cb7b9-451">SDK 수정을 위해 데이터 평면의 SDK 버전을 1.1.14로 업데이트하세요.</span><span class="sxs-lookup"><span data-stu-id="cb7b9-451">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="cb7b9-452">getfilestatus 및 liststatus에 대한 음수 acesstime 및 modificationtime 수정, 비동기 취소 토큰 수정</span><span class="sxs-lookup"><span data-stu-id="cb7b9-452">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="cb7b9-453">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="cb7b9-453">Az.EventGrid</span></span>
* <span data-ttu-id="cb7b9-454">2019-01-01 API 버전을 사용하도록 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="cb7b9-454">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="cb7b9-455">2019-01-01 API 버전에서 새 시나리오를 지원하도록 다음 cmdlet을 업데이트</span><span class="sxs-lookup"><span data-stu-id="cb7b9-455">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="cb7b9-456">New-AzureRmEventGridSubscription: 지정을 위한 새로운 선택적 매개 변수를 추가</span><span class="sxs-lookup"><span data-stu-id="cb7b9-456">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="cb7b9-457">이벤트 Time-to-Live</span><span class="sxs-lookup"><span data-stu-id="cb7b9-457">Event Time-To-Live,</span></span>
        - <span data-ttu-id="cb7b9-458">이벤트에 대한 최대 배달 시도</span><span class="sxs-lookup"><span data-stu-id="cb7b9-458">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="cb7b9-459">배달 못한 편지의 엔드포인트입니다.</span><span class="sxs-lookup"><span data-stu-id="cb7b9-459">Dead letter endpoint.</span></span>
    - <span data-ttu-id="cb7b9-460">Update-AzureRmEventGridSubscription: 지정을 위한 새로운 선택적 매개 변수를 추가</span><span class="sxs-lookup"><span data-stu-id="cb7b9-460">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="cb7b9-461">이벤트 Time-to-Live</span><span class="sxs-lookup"><span data-stu-id="cb7b9-461">Event Time-To-Live,</span></span>
        - <span data-ttu-id="cb7b9-462">이벤트에 대한 최대 배달 시도</span><span class="sxs-lookup"><span data-stu-id="cb7b9-462">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="cb7b9-463">배달 못한 편지의 엔드포인트입니다.</span><span class="sxs-lookup"><span data-stu-id="cb7b9-463">Dead letter endpoint.</span></span>
* <span data-ttu-id="cb7b9-464">New-AzureRmEventGridSubscription 및 Update-AzureRmEventGridSubscription cmdlet의 EndpointType 옵션에 새 열거형 값(즉, storageQueue 및 hybridConnection)을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="cb7b9-464">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="cb7b9-465">이벤트 구독을 생성 또는 업데이트할 때 사용자가 직접 조치를 취해야 할 경우 경고 메시지를 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="cb7b9-465">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="cb7b9-466">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="cb7b9-466">Az.IotHub</span></span>
* <span data-ttu-id="cb7b9-467">최신 버전의 Azure IotHub SDK로 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="cb7b9-467">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="cb7b9-468">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="cb7b9-468">Az.LogicApp</span></span>
* <span data-ttu-id="cb7b9-469">지정된 이름이 없는 모든 Get-AzLogicApp 목록</span><span class="sxs-lookup"><span data-stu-id="cb7b9-469">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="cb7b9-470">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cb7b9-470">Az.Resources</span></span>
* <span data-ttu-id="cb7b9-471">'Get-AzResource'에 '-ODataQuery'및 '-ResourceId' 매개 변수를 제공할 때 매개 변수 집합 문제 수정</span><span class="sxs-lookup"><span data-stu-id="cb7b9-471">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="cb7b9-472">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/7875 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="cb7b9-472">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="cb7b9-473">New/Set-AzPolicyDefinition에서 -Custom 매개 변수 처리 문제 수정</span><span class="sxs-lookup"><span data-stu-id="cb7b9-473">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="cb7b9-474">New-AzDeployment 설명서에서 오타 수정</span><span class="sxs-lookup"><span data-stu-id="cb7b9-474">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="cb7b9-475">'New-AzADUser'에 '-MailNickname'매개 변수가 필수 항목으로 지정됨</span><span class="sxs-lookup"><span data-stu-id="cb7b9-475">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="cb7b9-476">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/8220 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="cb7b9-476">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="cb7b9-477">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="cb7b9-477">Az.SignalR</span></span>
* <span data-ttu-id="cb7b9-478">Az.Accounts 모듈을 사용할 때의 이전 버전과의 호환성 문제를 해결합니다.</span><span class="sxs-lookup"><span data-stu-id="cb7b9-478">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="cb7b9-479">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cb7b9-479">Az.Sql</span></span>
* <span data-ttu-id="cb7b9-480">Storage 관리 클라이언트 종속성을 일반적인 SDK 구현으로 변환했습니다.</span><span class="sxs-lookup"><span data-stu-id="cb7b9-480">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="cb7b9-481">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="cb7b9-481">Az.Storage</span></span>
* <span data-ttu-id="cb7b9-482">Sas Token, OAuth 또는 Anonymous를 사용하여 스토리지 컨텍스트의 StorageAccountName을 실제 스토리지 계정 이름으로 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="cb7b9-482">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="cb7b9-483">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="cb7b9-483">New-AzStorageContext</span></span>
* <span data-ttu-id="cb7b9-484">'-FullUri' 매개 변수를 사용하여 Blob 스냅샷 개체의 Sas Token을 생성하고 반환된 Uri를 스냅샷 Uri로 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="cb7b9-484">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="cb7b9-485">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="cb7b9-485">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="cb7b9-486">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="cb7b9-486">Az.Websites</span></span>
* <span data-ttu-id="cb7b9-487">'Get-AzDeletedWebApp'의 날짜 구문 분석 버그를 수정했습니다.</span><span class="sxs-lookup"><span data-stu-id="cb7b9-487">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="cb7b9-488">Az.Accounts 모듈을 사용할 때의 이전 버전과의 호환성 문제를 해결합니다.</span><span class="sxs-lookup"><span data-stu-id="cb7b9-488">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="cb7b9-489">1.0.0 - 2018년 12월</span><span class="sxs-lookup"><span data-stu-id="cb7b9-489">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="cb7b9-490">일반</span><span class="sxs-lookup"><span data-stu-id="cb7b9-490">General</span></span>

- <span data-ttu-id="cb7b9-491">Az 모듈 일반 공급</span><span class="sxs-lookup"><span data-stu-id="cb7b9-491">General Availability of Az Module</span></span>
- <span data-ttu-id="cb7b9-492">각 모듈에 대 한 온라인 도움말</span><span class="sxs-lookup"><span data-stu-id="cb7b9-492">Online help for each module</span></span>
- <span data-ttu-id="cb7b9-493">자세한 내용과 로드맵은 [Az 알림 페이지](https://aka.ms/azps-announce)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="cb7b9-493">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="cb7b9-494">AzureRM에서 마이그레이션하는 것에 대한 정보는 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="cb7b9-494">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="cb7b9-495">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="cb7b9-495">Az.Accounts</span></span>
- <span data-ttu-id="cb7b9-496">Az.Profile에서 변경</span><span class="sxs-lookup"><span data-stu-id="cb7b9-496">Changed from Az.Profile</span></span>
- <span data-ttu-id="cb7b9-497">프로필 및 컨텍스트 형식에 대한 표 형식 수정</span><span class="sxs-lookup"><span data-stu-id="cb7b9-497">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="cb7b9-498">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="cb7b9-498">Az.ApiManagement</span></span>
- <span data-ttu-id="cb7b9-499">#7002에 대한 수정</span><span class="sxs-lookup"><span data-stu-id="cb7b9-499">Fixes for #7002</span></span>
- <span data-ttu-id="cb7b9-500">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="cb7b9-500">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="cb7b9-501">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="cb7b9-501">Az.Batch</span></span>
- <span data-ttu-id="cb7b9-502">`PSComputeNode`의 새로운 `NodeAgentInformation` 속성을 통해 풀의 각 VM에서 실행 중인 Azure Batch 노드 에이전트의 버전을 확인하는 기능이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="cb7b9-502">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="cb7b9-503">`PSDataDisk`에 대한 `Caching` 기본 값은 이제 `None` 대신 `ReadWrite`입니다.</span><span class="sxs-lookup"><span data-stu-id="cb7b9-503">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="cb7b9-504">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="cb7b9-504">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="cb7b9-505">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="cb7b9-505">Az.Billing</span></span>
- <span data-ttu-id="cb7b9-506">청구, 소비 및 UsageAggregates cmdlet 결합 cmdlet에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="cb7b9-506">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="cb7b9-507">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="cb7b9-507">Az.CognitivServices</span></span>
- <span data-ttu-id="cb7b9-508">New-AzureRmCognitiveServicesAccount 작업에서 사용 가능한 SkuName 및 Typem에 대한 완성자 추가</span><span class="sxs-lookup"><span data-stu-id="cb7b9-508">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="cb7b9-509">Get-AzCognitiveServicesAccountSkus에서 GetSkusWithAccountParamSetName 매개 변수 집합을 제거</span><span class="sxs-lookup"><span data-stu-id="cb7b9-509">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="cb7b9-510">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="cb7b9-510">Az.ContainerInstance</span></span>
- <span data-ttu-id="cb7b9-511">ManagedIdentity 지원이 추가됨</span><span class="sxs-lookup"><span data-stu-id="cb7b9-511">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="cb7b9-512">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="cb7b9-512">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="cb7b9-513">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="cb7b9-513">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="cb7b9-514">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="cb7b9-514">Az.DataLakeStore</span></span>
- <span data-ttu-id="cb7b9-515">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="cb7b9-515">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="cb7b9-516">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="cb7b9-516">Az.Monitor</span></span>
- <span data-ttu-id="cb7b9-517">Az.Monitor 이름 변경 및 기타 사소한 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="cb7b9-517">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="cb7b9-518">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="cb7b9-518">Az.KeyVault</span></span>
- <span data-ttu-id="cb7b9-519">출력 형식에서 사용되지 않는 'PurgeDisabled' 속성 제거</span><span class="sxs-lookup"><span data-stu-id="cb7b9-519">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="cb7b9-520">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="cb7b9-520">Az.MachineLearning</span></span>
- <span data-ttu-id="cb7b9-521">Az.MachineLearningCompute 모듈의 cmdlet 포함</span><span class="sxs-lookup"><span data-stu-id="cb7b9-521">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="cb7b9-522">Az.Media</span><span class="sxs-lookup"><span data-stu-id="cb7b9-522">Az.Media</span></span>
- <span data-ttu-id="cb7b9-523">New-AzMediaService에서 사용되지 않는 -Tags 별칭이 제거됨</span><span class="sxs-lookup"><span data-stu-id="cb7b9-523">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="cb7b9-524">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cb7b9-524">Az.Network</span></span>
<span data-ttu-id="cb7b9-525">Application Gateway에서 RewriteRuleSets를 구성하는 것에 대한 지원이 추가됨</span><span class="sxs-lookup"><span data-stu-id="cb7b9-525">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="cb7b9-526">추가된 새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="cb7b9-526">New cmdlets added:</span></span>
        - <span data-ttu-id="cb7b9-527">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="cb7b9-527">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="cb7b9-528">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="cb7b9-528">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="cb7b9-529">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="cb7b9-529">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="cb7b9-530">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="cb7b9-530">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="cb7b9-531">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="cb7b9-531">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="cb7b9-532">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="cb7b9-532">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="cb7b9-533">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="cb7b9-533">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="cb7b9-534">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="cb7b9-534">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="cb7b9-535">선택적 매개 변수를 사용하도록 cmdlet이 업데이트됨 -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="cb7b9-535">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="cb7b9-536">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="cb7b9-536">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="cb7b9-537">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="cb7b9-537">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="cb7b9-538">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="cb7b9-538">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="cb7b9-539">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="cb7b9-539">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="cb7b9-540">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="cb7b9-540">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="cb7b9-541">New-AzureRmApplicationGatewayUrlPathMapConfig로 ID를 사용하여 Application Gateway에 KeyVault 지원을 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="cb7b9-541">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="cb7b9-542">선택적 매개 변수를 사용하도록 cmdlet이 업데이트됨 -KeyVaultSecretId, -KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="cb7b9-542">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="cb7b9-543">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="cb7b9-543">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="cb7b9-544">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="cb7b9-544">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="cb7b9-545">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="cb7b9-545">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="cb7b9-546">New-AzApplicationGateway cmdlet이 선택적 매개 변수를 사용하도록 업데이트됨 -UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="cb7b9-546">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="cb7b9-547">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="cb7b9-547">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="cb7b9-548">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="cb7b9-548">Az.OperationalInsights</span></span>
- <span data-ttu-id="cb7b9-549">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="cb7b9-549">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="cb7b9-550">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="cb7b9-550">Az.Profile</span></span>
- <span data-ttu-id="cb7b9-551">Az.Accounts에 모듈 이름이 변경됨</span><span class="sxs-lookup"><span data-stu-id="cb7b9-551">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="cb7b9-552">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="cb7b9-552">Az.RecoveryServices</span></span>
- <span data-ttu-id="cb7b9-553">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="cb7b9-553">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="cb7b9-554">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cb7b9-554">Az.Resources</span></span>
- <span data-ttu-id="cb7b9-555">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="cb7b9-555">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="cb7b9-556">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="cb7b9-556">Az.ServiceFabric</span></span>
- <span data-ttu-id="cb7b9-557">일반 이름과 지문으로 지정 인증서 지원</span><span class="sxs-lookup"><span data-stu-id="cb7b9-557">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="cb7b9-558">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="cb7b9-558">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="cb7b9-559">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="cb7b9-559">Az.SIgnalR</span></span>
- <span data-ttu-id="cb7b9-560">SIgnalR에 대한 PowerShell cmdlet에 대한 일반 공급</span><span class="sxs-lookup"><span data-stu-id="cb7b9-560">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="cb7b9-561">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cb7b9-561">Az.Sql</span></span>
- <span data-ttu-id="cb7b9-562">위협 탐지의 cmdlet에 새로운 Data_Exfiltration 및 Unsafe_Action 검색 유형 추가</span><span class="sxs-lookup"><span data-stu-id="cb7b9-562">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="cb7b9-563">Sql 감사 cmdlet에 대한 설명서 예제 업데이트</span><span class="sxs-lookup"><span data-stu-id="cb7b9-563">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="cb7b9-564">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="cb7b9-564">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="cb7b9-565">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="cb7b9-565">Az.Storage</span></span>
- <span data-ttu-id="cb7b9-566">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="cb7b9-566">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="cb7b9-567">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="cb7b9-567">Az.Websites</span></span>
- <span data-ttu-id="cb7b9-568">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="cb7b9-568">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="cb7b9-569">0.7.0 - 2018년 12월</span><span class="sxs-lookup"><span data-stu-id="cb7b9-569">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="cb7b9-570">일반</span><span class="sxs-lookup"><span data-stu-id="cb7b9-570">General</span></span>

* <span data-ttu-id="cb7b9-571">AzureRM에서 Az 전환 예정에 대한 사소한 변경</span><span class="sxs-lookup"><span data-stu-id="cb7b9-571">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="cb7b9-572">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cb7b9-572">Az.Compute</span></span>

* <span data-ttu-id="cb7b9-573">`New-AzVm(ss)` cmdlet에 대한 간단한 매개 변수 집합에 UltraSSD 및 갤러리 이미지에 대한 지원을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="cb7b9-573">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="cb7b9-574">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="cb7b9-574">Az.DataLakeStore</span></span>

* <span data-ttu-id="cb7b9-575">ADLS 계정의 도메인의 후행 슬래시를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="cb7b9-575">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="cb7b9-576">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="cb7b9-576">Az.FrontDoor</span></span>

* <span data-ttu-id="cb7b9-577">일부 끊어진 링크 수정</span><span class="sxs-lookup"><span data-stu-id="cb7b9-577">Fixed some broken links</span></span>
    - <span data-ttu-id="cb7b9-578">New-AzureRmFrontDoor 및 Set-AzureRmFrontDoor 아티클에서 New-AzureRmFrontDoorHealthProbeSettingObject cmdlet 아티클에 대한 링크가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="cb7b9-578">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="cb7b9-579">New-AzureRmFrontDoorManagedRuleObject 아티클에서 New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet 아티클에 대한 링크가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="cb7b9-579">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="cb7b9-580">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="cb7b9-580">Az.RecoveryServices</span></span>

* <span data-ttu-id="cb7b9-581">Azure File Share 복원 작업에 클라이언트 측 유효성 검사가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="cb7b9-581">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="cb7b9-582">afs 복원의 경우 storageAccountName 및 storageAccountResourceGroupName을 선택적으로 만들었습니다.</span><span class="sxs-lookup"><span data-stu-id="cb7b9-582">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="cb7b9-583">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cb7b9-583">Az.Resources</span></span>

* <span data-ttu-id="cb7b9-584">에 대 한 수정 https://github.com/Azure/azure-powershell/issues/7679</span><span class="sxs-lookup"><span data-stu-id="cb7b9-584">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="cb7b9-585">기본 관리자를 요청할 때 구독 범위가 제공되는 경우 Get-AzureRmRoleAssignment를 업데이트하여 구독 범위를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="cb7b9-585">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="cb7b9-586">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cb7b9-586">Az.Sql</span></span>

* <span data-ttu-id="cb7b9-587">AzureRM에서 Az 전환 예정에 대한 사소한 변경</span><span class="sxs-lookup"><span data-stu-id="cb7b9-587">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="cb7b9-588">DotNet 코어에서 Get-AzureRmSqlDatabaseVulnerabilityAssessment를 사용하는 문제 해결</span><span class="sxs-lookup"><span data-stu-id="cb7b9-588">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="cb7b9-589">SQL 감사 cmdlet과 관련된 도움말 메시지의 설명서가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="cb7b9-589">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="cb7b9-590">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="cb7b9-590">Az.Storage</span></span>

* <span data-ttu-id="cb7b9-591">New-AzureRmStorageAccount에 -EnableHierarchicalNamespace 추가</span><span class="sxs-lookup"><span data-stu-id="cb7b9-591">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="cb7b9-592">파일 복사 cmdlet이 -DestContext 입력이 없을 때 대상의 원본 컨텍스트를 다시 사용할 수 없는 문제 수정</span><span class="sxs-lookup"><span data-stu-id="cb7b9-592">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="cb7b9-593">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="cb7b9-593">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="cb7b9-594">고정적인 웹 사이트 구성 지원</span><span class="sxs-lookup"><span data-stu-id="cb7b9-594">Support Static Website configuration</span></span>
    - <span data-ttu-id="cb7b9-595">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="cb7b9-595">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="cb7b9-596">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="cb7b9-596">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="cb7b9-597">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="cb7b9-597">Az.Websites</span></span>

* <span data-ttu-id="cb7b9-598">Set-AzureRmWebApp 및 Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="cb7b9-598">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span> 
    - <span data-ttu-id="cb7b9-599">Windows 및 Linux 컨테이너 응용 프로그램에 탑재할 Azure Storage 경로를 지정하기 위해 새 매개 변수(-AzureStoragePath)가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="cb7b9-599">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="cb7b9-600">새 cmdlet New-AzureRmWebAppAzureStoragePath의 출력을 매개 변수로 사용하여 Azure Storage 경로를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="cb7b9-600">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="cb7b9-601">0.6.1 - 2018년 11월</span><span class="sxs-lookup"><span data-stu-id="cb7b9-601">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="cb7b9-602">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="cb7b9-602">Az.ApiManagement</span></span>
* <span data-ttu-id="cb7b9-603">형식 매핑 문제에 대한 종속성 업데이트</span><span class="sxs-lookup"><span data-stu-id="cb7b9-603">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="cb7b9-604">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="cb7b9-604">Az.Automation</span></span>
* <span data-ttu-id="cb7b9-605">Azure Automation cmdlet 기반 Swagger</span><span class="sxs-lookup"><span data-stu-id="cb7b9-605">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="cb7b9-606">업데이트 관리 cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="cb7b9-606">Added Update Management cmdlets</span></span>
* <span data-ttu-id="cb7b9-607">소스 제어 cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="cb7b9-607">Added Source Control cmdlets</span></span>
* <span data-ttu-id="cb7b9-608">Remove-AzureRmAutomationHybridWorkerGroup cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="cb7b9-608">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="cb7b9-609">DSC 노드 등록 명령 수정</span><span class="sxs-lookup"><span data-stu-id="cb7b9-609">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="cb7b9-610">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cb7b9-610">Az.Compute</span></span>
* <span data-ttu-id="cb7b9-611">SystemAssigned ID에 대한 ID 문제 수정</span><span class="sxs-lookup"><span data-stu-id="cb7b9-611">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="cb7b9-612">형식 매핑 문제에 대한 종속성 업데이트</span><span class="sxs-lookup"><span data-stu-id="cb7b9-612">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="cb7b9-613">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="cb7b9-613">Az.ContainerInstance</span></span>
* <span data-ttu-id="cb7b9-614">형식 매핑 문제에 대한 종속성 업데이트</span><span class="sxs-lookup"><span data-stu-id="cb7b9-614">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="cb7b9-615">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="cb7b9-615">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="cb7b9-616">마켓플레이스 cmdlet에 대한 예제 설명 업데이트</span><span class="sxs-lookup"><span data-stu-id="cb7b9-616">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="cb7b9-617">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cb7b9-617">Az.Network</span></span>
* <span data-ttu-id="cb7b9-618">New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="cb7b9-618">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="cb7b9-619">지원되는 AzureFirewall 네트워크 프로토콜에 ICMP 다시 추가</span><span class="sxs-lookup"><span data-stu-id="cb7b9-619">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="cb7b9-620">Test-AzureRmNetworkWatcherConnectivity cmdlet을 업데이트하여 대상 ID, 주소 및 포트 유효성 검사를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="cb7b9-620">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span> 
* <span data-ttu-id="cb7b9-621">VirtualNetwork 맵의 메모리 사용 문제 해결</span><span class="sxs-lookup"><span data-stu-id="cb7b9-621">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="cb7b9-622">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="cb7b9-622">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="cb7b9-623">보호된 파일 공유에 대한 정책을 수정하는 것에 대해 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="cb7b9-623">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="cb7b9-624">정책 표준 시간대를 대문자로 변환했습니다.</span><span class="sxs-lookup"><span data-stu-id="cb7b9-624">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="cb7b9-625">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="cb7b9-625">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="cb7b9-626">New-AzureRmRecoveryServicesAsrProtectableItem의 예제 정정</span><span class="sxs-lookup"><span data-stu-id="cb7b9-626">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="cb7b9-627">형식 매핑 문제에 대한 종속성 업데이트</span><span class="sxs-lookup"><span data-stu-id="cb7b9-627">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="cb7b9-628">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="cb7b9-628">Az.Relay</span></span>
* <span data-ttu-id="cb7b9-629">선택적 매개 변수 -KeyValue를 New-AzureRmRelayKey cmdlet에 추가하여 사용자가 KeyValue를 제공할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cb7b9-629">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="cb7b9-630">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cb7b9-630">Az.Resources</span></span>
* <span data-ttu-id="cb7b9-631">`New-AzureRmPolicyAssignment` 및 `Set-AzureRmPolicyAssignment`의 자원 ID 관련 매개 변수에 대한 도움말 문서를 업데이트함</span><span class="sxs-lookup"><span data-stu-id="cb7b9-631">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="cb7b9-632">-Metadata를 사용하는 New-AzureRmPolicyDefinition에 대한 예제 추가</span><span class="sxs-lookup"><span data-stu-id="cb7b9-632">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="cb7b9-633">NetStandard의 태그 키에서 대소문자 보존을 허용하도록 수정: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="cb7b9-633">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="cb7b9-634">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="cb7b9-634">Az.ServiceFabric</span></span>
* <span data-ttu-id="cb7b9-635">향후 호환성이 손상되는 변경에 대한 사용 중단 메시지 추가</span><span class="sxs-lookup"><span data-stu-id="cb7b9-635">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="cb7b9-636">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cb7b9-636">Az.Sql</span></span>
* <span data-ttu-id="cb7b9-637">Azure Sql Database Managed Instance 및 Azure Sql Managed Database에 CRUD 작업을 위한 새 cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="cb7b9-637">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="cb7b9-638">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="cb7b9-638">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="cb7b9-639">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="cb7b9-639">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="cb7b9-640">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="cb7b9-640">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="cb7b9-641">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="cb7b9-641">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="cb7b9-642">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="cb7b9-642">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="cb7b9-643">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="cb7b9-643">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="cb7b9-644">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="cb7b9-644">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="cb7b9-645">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="cb7b9-645">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="cb7b9-646">서버 또는 데이터베이스에서 확장 감사 정책 관리를 활성화했습니다.</span><span class="sxs-lookup"><span data-stu-id="cb7b9-646">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="cb7b9-647">새 매개 변수(PredicateExpression)가 감사 로그 필터링을 사용하도록 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="cb7b9-647">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="cb7b9-648">Cmdlet이 레거시 클라이언트 대신 SQL 클라이언트를 사용하도록 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="cb7b9-648">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="cb7b9-649">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="cb7b9-649">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="cb7b9-650">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="cb7b9-650">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="cb7b9-651">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="cb7b9-651">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="cb7b9-652">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="cb7b9-652">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="cb7b9-653">스토리지 계정 이름 매개 변수가 설정된 Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings를 사용할 때의 문제 해결</span><span class="sxs-lookup"><span data-stu-id="cb7b9-653">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="cb7b9-654">0.5.0 - 2018년 11월</span><span class="sxs-lookup"><span data-stu-id="cb7b9-654">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="cb7b9-655">일반</span><span class="sxs-lookup"><span data-stu-id="cb7b9-655">General</span></span>
* <span data-ttu-id="cb7b9-656">많은 핵심 cmdlet에 Resource Completers를 추가하여 대화형으로 cmdlet을 호출할 때 기존 리소스 이름을 탭으로 이동할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cb7b9-656">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="cb7b9-657">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="cb7b9-657">Az.Profile</span></span>
* <span data-ttu-id="cb7b9-658">ClientRuntime의 최신 버전을 사용하도록 일반적인 코드를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="cb7b9-658">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="cb7b9-659">Connect-AzAccount cmdlet의 매개 변수 TenantId 이름을 Tenant로 바꾸고 TenantId의 별칭을 추가합니다</span><span class="sxs-lookup"><span data-stu-id="cb7b9-659">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="cb7b9-660">Connect-AzAccount의 업데이트된 TenantId 설명</span><span class="sxs-lookup"><span data-stu-id="cb7b9-660">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="cb7b9-661">테넌트 도메인을 제공할 때 실패한 로그인에 대한 오류 메시지 수정</span><span class="sxs-lookup"><span data-stu-id="cb7b9-661">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="cb7b9-662">테넌트에 구독이 없는 계정의 컨텍스트 이름 충돌 문제 수정</span><span class="sxs-lookup"><span data-stu-id="cb7b9-662">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="cb7b9-663">MSI를 사용할 때 DataLake 엔드포인트 문제 수정</span><span class="sxs-lookup"><span data-stu-id="cb7b9-663">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="cb7b9-664">연결되지 않은 경우 'Disconnect-AzAccount'가 throw하는 문제 수정</span><span class="sxs-lookup"><span data-stu-id="cb7b9-664">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="cb7b9-665">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="cb7b9-665">Az.CognitiveServices</span></span>
* <span data-ttu-id="cb7b9-666">Get-AzCognitiveServicesAccountSkus 작업을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="cb7b9-666">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="cb7b9-667">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cb7b9-667">Az.Compute</span></span>
* <span data-ttu-id="cb7b9-668">Add-AzVmssVMDataDisk 및 Remove-AzVmssVMDataDisk cmdlet를 추가합니다</span><span class="sxs-lookup"><span data-stu-id="cb7b9-668">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="cb7b9-669">Get-AzVMImage는 AutomaticOSUpgradeProperties를 표시합니다</span><span class="sxs-lookup"><span data-stu-id="cb7b9-669">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="cb7b9-670">수정된 SetAzVMChefExtension -BootstrapOptions 및 -JsonAttribute option 값이 json 형식으로 설정하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="cb7b9-670">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="cb7b9-671">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="cb7b9-671">Az.DataLakeStore</span></span>
* <span data-ttu-id="cb7b9-672">DataLake 패키지를 1.1.10으로 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="cb7b9-672">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="cb7b9-673">기본 동시성을 다중 스레드 작업에 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="cb7b9-673">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="cb7b9-674">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="cb7b9-674">Az.Insights</span></span>
* <span data-ttu-id="cb7b9-675">해결된 문제 #7267(자동 크기 조정 영역)</span><span class="sxs-lookup"><span data-stu-id="cb7b9-675">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="cb7b9-676">열거된 매개 변수를 제대로 설정하지 않은 새 자동 크기 조정 규칙을 만드는 데 문제가 있습니다(이를 항상 기본값으로 설정함).</span><span class="sxs-lookup"><span data-stu-id="cb7b9-676">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="cb7b9-677">해결된 문제 # 7513[자세한 정보] Set-AzDiagnosticSetting은 설정을 생성하는 동안 범주를 명시적으로 지정해야 합니다</span><span class="sxs-lookup"><span data-stu-id="cb7b9-677">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="cb7b9-678">이제 cmdlet은 생성 중에 사용할 범주를 명시적으로 표시할 필요가 없습니다. 즉, 문서화된대로 작동합니다</span><span class="sxs-lookup"><span data-stu-id="cb7b9-678">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="cb7b9-679">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cb7b9-679">Az.Network</span></span>
* <span data-ttu-id="cb7b9-680">다음 cmdlet에 대해 PeeringType을 필수 매개 변수로 변경했습니다.</span><span class="sxs-lookup"><span data-stu-id="cb7b9-680">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="cb7b9-681">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="cb7b9-681">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="cb7b9-682">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="cb7b9-682">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="cb7b9-683">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="cb7b9-683">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="cb7b9-684">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="cb7b9-684">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="cb7b9-685">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="cb7b9-685">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="cb7b9-686">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="cb7b9-686">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="cb7b9-687">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="cb7b9-687">Az.PolicyInsights</span></span>
* <span data-ttu-id="cb7b9-688">추가된 정책 재구성 cmdlet</span><span class="sxs-lookup"><span data-stu-id="cb7b9-688">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="cb7b9-689">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cb7b9-689">Az.Resources</span></span>
* <span data-ttu-id="cb7b9-690">에 대 한 수정 https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="cb7b9-690">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="cb7b9-691">'Get-AzResource'에 대해 '-ResourceId' 매개 변수를 사용하여 리소스 나열 허용</span><span class="sxs-lookup"><span data-stu-id="cb7b9-691">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="cb7b9-692">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="cb7b9-692">Az.ServiceBus</span></span>
* <span data-ttu-id="cb7b9-693">마이그레이션 상태를 알 수 있도록 PSServiceBusMigrationConfigurationAttributes에 MigrationState 읽기 전용 속성 추가.</span><span class="sxs-lookup"><span data-stu-id="cb7b9-693">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="cb7b9-694">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="cb7b9-694">Az.ServiceFabric</span></span>
* <span data-ttu-id="cb7b9-695">Linux Vmss에 인증서 추가 수정.</span><span class="sxs-lookup"><span data-stu-id="cb7b9-695">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="cb7b9-696">Add-AzServiceFabricClusterCertificate 수정</span><span class="sxs-lookup"><span data-stu-id="cb7b9-696">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="cb7b9-697">새 인증서(Azure/service-fabric-issues#932)에서 올바른 지문을 사용.</span><span class="sxs-lookup"><span data-stu-id="cb7b9-697">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="cb7b9-698">올바르게 예외 표시(Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="cb7b9-698">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="cb7b9-699">Vmss CreateOrUpdate 작업을 시작하기 전에 'Update-AzServiceFabricDurability'를 수정하여 클러스터 구성 업데이트.</span><span class="sxs-lookup"><span data-stu-id="cb7b9-699">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="cb7b9-700">0.4.0 - 2018년 10월</span><span class="sxs-lookup"><span data-stu-id="cb7b9-700">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="cb7b9-701">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="cb7b9-701">Az.Profile</span></span>
* <span data-ttu-id="cb7b9-702">CloudShell에서 Get-AzSubscription을 사용하여 문제를 해결합니다.</span><span class="sxs-lookup"><span data-stu-id="cb7b9-702">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="cb7b9-703">ClientRuntime의 최신 버전을 사용하도록 일반적인 코드를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="cb7b9-703">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="cb7b9-704">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cb7b9-704">Az.Compute</span></span>
* <span data-ttu-id="cb7b9-705">'New-AzVm'에 대해 간단한 매개 변수를 사용하는 경우 가속화된 네트워킹을 설정하기 위해 새 크기가 VM 크기의 허용 목록에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="cb7b9-705">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="cb7b9-706">모든 cmdlet에 ResourceName 인수 완성자가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="cb7b9-706">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="cb7b9-707">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="cb7b9-707">Az.DataLakeStore</span></span>
* <span data-ttu-id="cb7b9-708">Virtual Network 규칙에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="cb7b9-708">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="cb7b9-709">Get-AzDataLakeStoreVirtualNetworkRule: Azure Data Lake Store 가상 네트워크 규칙을 가져오거나 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="cb7b9-709">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="cb7b9-710">Add-AzDataLakeStoreVirtualNetworkRule: 지정된 Data Lake Store 계정에 가상 네트워크 규칙을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="cb7b9-710">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="cb7b9-711">Set-AzDataLakeStoreVirtualNetworkRule: 지정된 Data Lake Store 계정에 지정된 가상 네트워크 규칙을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="cb7b9-711">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="cb7b9-712">Remove-AzDataLakeStoreVirtualNetworkRule: Azure Data Lake Store 가상 네트워크 규칙을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="cb7b9-712">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="cb7b9-713">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cb7b9-713">Az.Network</span></span>
* <span data-ttu-id="cb7b9-714">Test-AzNetworkWatcherConnectivity cmdlet을 업데이트하고, 백 엔드에 프로토콜 값을 전달합니다.</span><span class="sxs-lookup"><span data-stu-id="cb7b9-714">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="cb7b9-715">모든 cmdlet에 ResourceName 인수 완성자가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="cb7b9-715">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="cb7b9-716">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cb7b9-716">Az.Resources</span></span>
* <span data-ttu-id="cb7b9-717">(기본 프로필에 구독이 없고 범위가 지정되지 않은 경우) 시나리오에서 의미 있는 예외를 추가하여 Get-AzRoleDefinition이 인식할 수 없는 예외를 throw하는 문제를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="cb7b9-717">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="cb7b9-718">또한 기본 매개 변수 집합을 'RoleDefinitionNameParameterSet'으로 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="cb7b9-718">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="cb7b9-719">0.3.0 - 2018년 10월</span><span class="sxs-lookup"><span data-stu-id="cb7b9-719">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="cb7b9-720">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="cb7b9-720">Azure.Storage</span></span>
* <span data-ttu-id="cb7b9-721">대상에 메타데이터가 있을 때 Blob/파일이 메타 데이터를 복사하지 않는 문제 수정</span><span class="sxs-lookup"><span data-stu-id="cb7b9-721">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="cb7b9-722">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="cb7b9-722">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="cb7b9-723">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="cb7b9-723">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="cb7b9-724">특정 위치의 저장소 리소스 사용을 지원하고 글로벌 저장소 리소스 사용 가져오기는 더 이상 사용되지 않는다는 경고 메시지를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="cb7b9-724">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="cb7b9-725">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="cb7b9-725">Get-AzStorageUsage</span></span>
    
#### <a name="azcognitiveservices"></a><span data-ttu-id="cb7b9-726">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="cb7b9-726">Az.CognitiveServices</span></span>
* <span data-ttu-id="cb7b9-727">기존 계정이 없는 Get-AzCognitiveServicesAccountSkus를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="cb7b9-727">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="cb7b9-728">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cb7b9-728">Az.Compute</span></span>
* <span data-ttu-id="cb7b9-729">Get-AzVM -ResourceGroupName <rg>가 필요한 경우 50개가 넘는 결과를 반환하도록 수정</span><span class="sxs-lookup"><span data-stu-id="cb7b9-729">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="cb7b9-730">'SimpleParameterSet' 예제가 New-AzVmss cmdlet 도움말에 추가됨</span><span class="sxs-lookup"><span data-stu-id="cb7b9-730">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="cb7b9-731">Azure Disk Encryption 진행률 메시지의 오타를 수정</span><span class="sxs-lookup"><span data-stu-id="cb7b9-731">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="cb7b9-732">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="cb7b9-732">Az.DataFactoryV2</span></span>
* <span data-ttu-id="cb7b9-733">ADF.Net SDK 버전을 2.3.0으로 업데이트</span><span class="sxs-lookup"><span data-stu-id="cb7b9-733">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="cb7b9-734">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cb7b9-734">Az.Network</span></span>
* <span data-ttu-id="cb7b9-735">NetworkProfile 기능 추가</span><span class="sxs-lookup"><span data-stu-id="cb7b9-735">Added NetworkProfile functionality.</span></span> <span data-ttu-id="cb7b9-736">추가된 새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="cb7b9-736">new cmdlets added</span></span>
    - <span data-ttu-id="cb7b9-737">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="cb7b9-737">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="cb7b9-738">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="cb7b9-738">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="cb7b9-739">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="cb7b9-739">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="cb7b9-740">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="cb7b9-740">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="cb7b9-741">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="cb7b9-741">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="cb7b9-742">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="cb7b9-742">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="cb7b9-743">서브넷 모델에 서비스 연결 링크 추가</span><span class="sxs-lookup"><span data-stu-id="cb7b9-743">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="cb7b9-744">New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="cb7b9-744">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="cb7b9-745">Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="cb7b9-745">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="cb7b9-746">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="cb7b9-746">Az.RedisCache</span></span>
* <span data-ttu-id="cb7b9-747">모든 문자열을 Size 매개 변수로 진행되도록 허용</span><span class="sxs-lookup"><span data-stu-id="cb7b9-747">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="cb7b9-748">PSArgumentCompleter 팝업에 P5 추가</span><span class="sxs-lookup"><span data-stu-id="cb7b9-748">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="cb7b9-749">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cb7b9-749">Az.Resources</span></span>
* <span data-ttu-id="cb7b9-750">-Mode 매개 변수를 Set-AzPolicyDefinition에 추가</span><span class="sxs-lookup"><span data-stu-id="cb7b9-750">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="cb7b9-751">사용자가 포함된 Origin 작업에서 Get-AzProviderOperation commandlet 버그 수정</span><span class="sxs-lookup"><span data-stu-id="cb7b9-751">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="cb7b9-752">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cb7b9-752">Az.Sql</span></span>
* <span data-ttu-id="cb7b9-753">일부 백업 cmdlet이 현재 azure 구독을 인식하지 않는 문제 해결</span><span class="sxs-lookup"><span data-stu-id="cb7b9-753">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="cb7b9-754">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="cb7b9-754">Az.Websites</span></span>
* <span data-ttu-id="cb7b9-755">새 cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - 컨테이너 지속적인 배포 Webhook URL을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="cb7b9-755">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="cb7b9-756">새 cmdlet New-AzWebAppContainerPSSession 및 Enter-WebAppContainerPSSession -  windows 컨테이너 앱에 PowerShell 원격 세션을 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="cb7b9-756">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="cb7b9-757">0.2.0 - 2018년 9월</span><span class="sxs-lookup"><span data-stu-id="cb7b9-757">0.2.0 - September 2018</span></span>
 <span data-ttu-id="cb7b9-758">최초 릴리스</span><span class="sxs-lookup"><span data-stu-id="cb7b9-758">Initial Release</span></span>