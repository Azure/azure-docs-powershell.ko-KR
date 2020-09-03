---
title: Azure PowerShell 릴리스 정보
description: Azure PowerShell 모듈의 모든 최신 업데이트에 대해 알아봅니다.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 04/30/2019
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: 1cc7d6519ded41003daed558a8e78ee65ded072a
ms.sourcegitcommit: 8b3126b5c79f453464d90669f0046ba86b7a3424
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/01/2020
ms.locfileid: "89240967"
---
# <a name="azure-powershell-release-notes"></a><span data-ttu-id="6933a-103">Azure PowerShell 릴리스 정보</span><span class="sxs-lookup"><span data-stu-id="6933a-103">Azure PowerShell release notes</span></span>
## <a name="180---april-2019"></a><span data-ttu-id="6933a-104">1.8.0 - 2019년 4월</span><span class="sxs-lookup"><span data-stu-id="6933a-104">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="6933a-105">마지막 주 릴리스 이후의 주요 사항</span><span class="sxs-lookup"><span data-stu-id="6933a-105">Highlights since the last major release</span></span>
* <span data-ttu-id="6933a-106">`Az` 모듈 일반 공급</span><span class="sxs-lookup"><span data-stu-id="6933a-106">General availability of `Az` module</span></span>
* <span data-ttu-id="6933a-107">`Az` 모듈에 대한 자세한 내용은 https://aka.ms/azps-announce 를 방문하세요.</span><span class="sxs-lookup"><span data-stu-id="6933a-107">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="6933a-108">Location, ResourceGroup 및 ResourceName 완성자가 추가되었습니다(https://azure.microsoft.com/blog/completers-in-azure-powershell/ ).</span><span class="sxs-lookup"><span data-stu-id="6933a-108">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="6933a-109">와일드카드 지원이 Az.Compute 및 Az.Network에 대한 Get cmdlet에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6933a-109">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="6933a-110">Windows PowerShell 5.1 전용 대화형 사용자 이름/암호 인증이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6933a-110">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="6933a-111">Python 2 Runbook 지원이 Az.Automation에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6933a-111">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="6933a-112">Az.LogicApp: 통합 계정 어셈블리 및 일괄 처리 구성을 위한 새로운 cmdlet입니다.</span><span class="sxs-lookup"><span data-stu-id="6933a-112">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="6933a-113">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6933a-113">Az.Accounts</span></span>
* <span data-ttu-id="6933a-114">Mac에서 모듈을 올바르게 삭제하기 위해 Uninstall-AzureRm을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="6933a-114">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="6933a-115">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="6933a-115">Az.Batch</span></span>
* <span data-ttu-id="6933a-116">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="6933a-116">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="6933a-117">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="6933a-117">Az.Cdn</span></span>
* <span data-ttu-id="6933a-118">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="6933a-118">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="6933a-119">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="6933a-119">Az.CognitiveServices</span></span>
* <span data-ttu-id="6933a-120">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="6933a-120">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6933a-121">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6933a-121">Az.Compute</span></span>
* <span data-ttu-id="6933a-122">디스크의 리소스 ID에 리소스 ID의 소문자 resourcegroups가 있는 경우 AEM 설치 문제 수정</span><span class="sxs-lookup"><span data-stu-id="6933a-122">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="6933a-123">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="6933a-123">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="6933a-124">와일드 카드에 대한 설명서 수정</span><span class="sxs-lookup"><span data-stu-id="6933a-124">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="6933a-125">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="6933a-125">Az.DataFactory</span></span>
* <span data-ttu-id="6933a-126">NodeCount가 관리형 통합 런타임에 대해 Null이 아닌 경우 SsisProperties를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="6933a-126">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="6933a-127">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="6933a-127">Az.DataLakeStore</span></span>
* <span data-ttu-id="6933a-128">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="6933a-128">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="6933a-129">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="6933a-129">Az.EventGrid</span></span>
* <span data-ttu-id="6933a-130">이벤트 구독 cmdlet 만들기/업데이트를 사용하기 전에 리소스를 만들어야 함을 나타내기 위해 엔드포인트의 도움말 텍스트가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6933a-130">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="6933a-131">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="6933a-131">Az.EventHub</span></span>
* <span data-ttu-id="6933a-132">네임스페이스의 NetworkRuleSet에 대한 새 cmdlet가 추가되었습니다</span><span class="sxs-lookup"><span data-stu-id="6933a-132">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="6933a-133">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="6933a-133">Az.HDInsight</span></span>
* <span data-ttu-id="6933a-134">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="6933a-134">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="6933a-135">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="6933a-135">Az.IotHub</span></span>
* <span data-ttu-id="6933a-136">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="6933a-136">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="6933a-137">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="6933a-137">Az.KeyVault</span></span>
* <span data-ttu-id="6933a-138">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="6933a-138">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="6933a-139">와일드 카드에 대한 설명서 수정</span><span class="sxs-lookup"><span data-stu-id="6933a-139">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="6933a-140">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="6933a-140">Az.MachineLearning</span></span>
* <span data-ttu-id="6933a-141">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="6933a-141">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="6933a-142">Az.Media</span><span class="sxs-lookup"><span data-stu-id="6933a-142">Az.Media</span></span>
* <span data-ttu-id="6933a-143">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="6933a-143">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="6933a-144">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="6933a-144">Az.Monitor</span></span>
  * <span data-ttu-id="6933a-145">GenV2(비 클래식) 메트릭 기반 경고 규칙에 대한 새 cmdlet</span><span class="sxs-lookup"><span data-stu-id="6933a-145">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="6933a-146">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="6933a-146">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="6933a-147">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="6933a-147">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="6933a-148">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="6933a-148">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="6933a-149">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="6933a-149">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="6933a-150">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="6933a-150">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="6933a-151">모니터 SDK가 버전 0.22.0-preview로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6933a-151">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6933a-152">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6933a-152">Az.Network</span></span>
* <span data-ttu-id="6933a-153">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="6933a-153">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="6933a-154">와일드 카드에 대한 설명서 수정</span><span class="sxs-lookup"><span data-stu-id="6933a-154">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="6933a-155">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="6933a-155">Az.NotificationHubs</span></span>
* <span data-ttu-id="6933a-156">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="6933a-156">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="6933a-157">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="6933a-157">Az.OperationalInsights</span></span>
* <span data-ttu-id="6933a-158">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="6933a-158">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="6933a-159">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="6933a-159">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="6933a-160">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="6933a-160">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="6933a-161">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="6933a-161">Az.RecoveryServices</span></span>
* <span data-ttu-id="6933a-162">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="6933a-162">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="6933a-163">Azure VM의 SQL용 테이블 형식이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6933a-163">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="6933a-164">AzureFileShare에서 위치를 가져오는 대체 메서드가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6933a-164">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="6933a-165">시간대에 따라 SchedulePolicy 개체의 ScheduleRunDays가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6933a-165">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="6933a-166">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="6933a-166">Az.RedisCache</span></span>
* <span data-ttu-id="6933a-167">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="6933a-167">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="6933a-168">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6933a-168">Az.Resources</span></span>
* <span data-ttu-id="6933a-169">와일드 카드에 대한 설명서 수정</span><span class="sxs-lookup"><span data-stu-id="6933a-169">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="6933a-170">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6933a-170">Az.Sql</span></span>
* <span data-ttu-id="6933a-171">Monitor SDK의 종속성을 공용 코드로 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="6933a-171">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="6933a-172">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="6933a-172">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="6933a-173">다중 열 분류 프로세스가 향상되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6933a-173">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="6933a-174">기본적으로 Get-AzSqlServerServiceObjective의 응답으로 SKU 속성(SKU 이름, 제품군, 용량)과 테이블 형식을 포함합니다.</span><span class="sxs-lookup"><span data-stu-id="6933a-174">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="6933a-175">해당 지역에 기존 서버 없이 위치별로 Get-AzSqlServerServiceObjective를 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6933a-175">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="6933a-176">관리형 인스턴스 생성 시 표준 시간대 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="6933a-176">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="6933a-177">와일드 카드에 대한 설명서 수정</span><span class="sxs-lookup"><span data-stu-id="6933a-177">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="6933a-178">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="6933a-178">Az.Websites</span></span>
* <span data-ttu-id="6933a-179">실행 시 태그를 제거하지 않도록 Set-AzWebApp 및 Set-AzWebAppSlot를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="6933a-179">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="6933a-180">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="6933a-180">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="6933a-181">WebSites SDK가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6933a-181">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="6933a-182">PSAppServicePlan에서 AdminSiteName 속성을 제거했습니다.</span><span class="sxs-lookup"><span data-stu-id="6933a-182">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="6933a-183">1.7.0 - 2019년 4월</span><span class="sxs-lookup"><span data-stu-id="6933a-183">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="6933a-184">마지막 주 릴리스 이후의 주요 사항</span><span class="sxs-lookup"><span data-stu-id="6933a-184">Highlights since the last major release</span></span>
* <span data-ttu-id="6933a-185">`Az` 모듈 일반 공급</span><span class="sxs-lookup"><span data-stu-id="6933a-185">General availability of `Az` module</span></span>
* <span data-ttu-id="6933a-186">`Az` 모듈에 대한 자세한 내용은 https://aka.ms/azps-announce 를 방문하세요.</span><span class="sxs-lookup"><span data-stu-id="6933a-186">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="6933a-187">Location, ResourceGroup 및 ResourceName 완성자가 추가되었습니다(https://azure.microsoft.com/blog/completers-in-azure-powershell/ ).</span><span class="sxs-lookup"><span data-stu-id="6933a-187">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="6933a-188">와일드카드 지원이 Az.Compute 및 Az.Network에 대한 Get cmdlet에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6933a-188">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="6933a-189">Windows PowerShell 5.1 전용 대화형 사용자 이름/암호 인증이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6933a-189">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="6933a-190">Python 2 Runbook 지원이 Az.Automation에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6933a-190">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="6933a-191">Az.LogicApp: 통합 계정 어셈블리 및 일괄 처리 구성을 위한 새로운 cmdlet입니다.</span><span class="sxs-lookup"><span data-stu-id="6933a-191">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="6933a-192">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6933a-192">Az.Accounts</span></span>
* <span data-ttu-id="6933a-193">매개 변수 AzureAnalysisServicesEndpointResourceId를 허용하도록 Add-AzEnvironment 및 Set-AzEnvironment 업데이트</span><span class="sxs-lookup"><span data-stu-id="6933a-193">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="6933a-194">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="6933a-194">Az.AnalysisServices</span></span>
* <span data-ttu-id="6933a-195">데이터 평면 cmdlet에서 ServiceClient 사용 및 원본 인증 논리 제거</span><span class="sxs-lookup"><span data-stu-id="6933a-195">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="6933a-196">호환성이 손상되는 변경을 방지하기 위해 Add-AzureASAccount를 Connect-AzAccount의 래퍼로 만듦</span><span class="sxs-lookup"><span data-stu-id="6933a-196">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="6933a-197">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="6933a-197">Az.Automation</span></span>
* <span data-ttu-id="6933a-198">포함에 대한 New-AzAutomationSoftwareUpdateConfiguration cmdlet 버그 수정</span><span class="sxs-lookup"><span data-stu-id="6933a-198">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="6933a-199">이제 매개 변수 IncludedKbNumber 및 IncludedPackageNameMask가 작동함</span><span class="sxs-lookup"><span data-stu-id="6933a-199">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="6933a-200">Azure 자동화 업데이트 관리 동적 그룹에 대한 버그 수정</span><span class="sxs-lookup"><span data-stu-id="6933a-200">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6933a-201">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6933a-201">Az.Compute</span></span>
* <span data-ttu-id="6933a-202">New-AzDiskConfig 및 New-AzSnapshotConfig에 HyperVGeneration 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="6933a-202">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="6933a-203">다른 테넌트의 갤러리 이미지를 사용하여 VM을 만들 수 있음</span><span class="sxs-lookup"><span data-stu-id="6933a-203">Allow VM creation with galley image from other tenants.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="6933a-204">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="6933a-204">Az.ContainerInstance</span></span>
* <span data-ttu-id="6933a-205">후행 빈 인수를 추가한 New-AzContainerGroup의 -Command 매개 변수의 문제 수정</span><span class="sxs-lookup"><span data-stu-id="6933a-205">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="6933a-206">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="6933a-206">Az.DataFactory</span></span>
* <span data-ttu-id="6933a-207">ADF .Net SDK 버전을 3.0.2로 업데이트</span><span class="sxs-lookup"><span data-stu-id="6933a-207">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="6933a-208">RepoConfiguration 관련 설정에 대한 추가 매개 변수로 Set-AzDataFactoryV2 cmdlet을 업데이트</span><span class="sxs-lookup"><span data-stu-id="6933a-208">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="6933a-209">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6933a-209">Az.Resources</span></span>
* <span data-ttu-id="6933a-210">'-ResourceId' 또는 '-ResourceGroupName', '-Name' 및 '-ResourceType' 매개 변수를 제공할 때 'Get-AzResource'에 대한 공급자 처리 개선</span><span class="sxs-lookup"><span data-stu-id="6933a-210">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="6933a-211">'Test-AzDeployment' 및 'Test-AzResourceGroupDeployment'에 대한 오류 처리 개선</span><span class="sxs-lookup"><span data-stu-id="6933a-211">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="6933a-212">배포 유효성 검사 외부에서 발생한 오류를 처리하고 그 대신 명령의 출력에 포함</span><span class="sxs-lookup"><span data-stu-id="6933a-212">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="6933a-213">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/6856 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="6933a-213">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="6933a-214">배포 cmdlet 세트에 스크립트 및 작업 시나리오에서 프롬프트를 건너뛰는 '-IgnoreDynamicParameters' 스위치 추가</span><span class="sxs-lookup"><span data-stu-id="6933a-214">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="6933a-215">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/6856 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="6933a-215">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="6933a-216">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6933a-216">Az.Sql</span></span>
* <span data-ttu-id="6933a-217">데이터베이스 데이터 분류 지원</span><span class="sxs-lookup"><span data-stu-id="6933a-217">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="6933a-218">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="6933a-218">Az.Storage</span></span>
* <span data-ttu-id="6933a-219">매개 변수 -UseConnectedAccount를 사용하여 스토리지 컨텍스트를 만들 때 자세한 오류 보고(단, 로그인 Azure 계정 없이)</span><span class="sxs-lookup"><span data-stu-id="6933a-219">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="6933a-220">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="6933a-220">New-AzStorageContext</span></span>
* <span data-ttu-id="6933a-221">관리 평면 API를 사용하여 지정한 스토리지 계정의 BLOB 서비스 속성 관리 지원</span><span class="sxs-lookup"><span data-stu-id="6933a-221">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="6933a-222">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="6933a-222">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="6933a-223">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="6933a-223">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="6933a-224">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="6933a-224">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="6933a-225">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="6933a-225">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="6933a-226">BLOB 및 파일 업로드/다운로드 cmdlet에 대한 -AsJob 지원</span><span class="sxs-lookup"><span data-stu-id="6933a-226">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="6933a-227">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="6933a-227">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="6933a-228">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="6933a-228">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="6933a-229">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="6933a-229">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="6933a-230">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="6933a-230">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="6933a-231">1.6.0 - 2019년 3월</span><span class="sxs-lookup"><span data-stu-id="6933a-231">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="6933a-232">마지막 주 릴리스 이후의 주요 사항</span><span class="sxs-lookup"><span data-stu-id="6933a-232">Highlights since the last major release</span></span>
* <span data-ttu-id="6933a-233">`Az` 모듈 일반 공급</span><span class="sxs-lookup"><span data-stu-id="6933a-233">General availability of `Az` module</span></span>
* <span data-ttu-id="6933a-234">`Az` 모듈에 대한 자세한 내용은 https://aka.ms/azps-announce 를 방문하세요.</span><span class="sxs-lookup"><span data-stu-id="6933a-234">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="6933a-235">Location, ResourceGroup 및 ResourceName 완성자가 추가되었습니다(https://azure.microsoft.com/blog/completers-in-azure-powershell/ ).</span><span class="sxs-lookup"><span data-stu-id="6933a-235">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="6933a-236">와일드카드 지원이 Az.Compute 및 Az.Network에 대한 Get cmdlet에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6933a-236">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="6933a-237">Windows PowerShell 5.1 전용 대화형 사용자 이름/암호 인증이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6933a-237">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="6933a-238">Python 2 Runbook 지원이 Az.Automation에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6933a-238">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="6933a-239">Az.LogicApp: 통합 계정 어셈블리 및 일괄 처리 구성을 위한 새로운 cmdlet입니다.</span><span class="sxs-lookup"><span data-stu-id="6933a-239">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="6933a-240">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="6933a-240">Az.Automation</span></span>
* <span data-ttu-id="6933a-241">Azure 자동화 업데이트 관리에서 변경된 지원 기능은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="6933a-241">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="6933a-242">동적 그룹화</span><span class="sxs-lookup"><span data-stu-id="6933a-242">Dynamic grouping</span></span>
    * <span data-ttu-id="6933a-243">사전 스크립트</span><span class="sxs-lookup"><span data-stu-id="6933a-243">Pre-Post script</span></span>
    * <span data-ttu-id="6933a-244">다시 부팅 설정</span><span class="sxs-lookup"><span data-stu-id="6933a-244">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6933a-245">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6933a-245">Az.Compute</span></span>
* <span data-ttu-id="6933a-246">Get-AzVmBootDiagnosticsData의 경로 확인 문제가 해결되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6933a-246">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="6933a-247">Compute 클라이언트 라이브러리가 25.0.0으로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6933a-247">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="6933a-248">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="6933a-248">Az.KeyVault</span></span>
* <span data-ttu-id="6933a-249">와일드카드 지원이 KeyVault cmdlet에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6933a-249">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6933a-250">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6933a-250">Az.Network</span></span>
* <span data-ttu-id="6933a-251">Azure Firewall에 대한 위협 인텔리전스 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6933a-251">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="6933a-252">Application Gateway 방화벽 정책의 최상위 수준 리소스 및 사용자 지정 규칙이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6933a-252">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="6933a-253">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="6933a-253">Az.RecoveryServices</span></span>
* <span data-ttu-id="6933a-254">인스턴트 RP를 지원하기 위해 SnapshotRetentionInDays가 Azure VM 정책에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6933a-254">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="6933a-255">컨테이너 등록을 취소하는 파이프 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6933a-255">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="6933a-256">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6933a-256">Az.Resources</span></span>
* <span data-ttu-id="6933a-257">Get-AzResource 및 Get-AzResourceGroup에 대한 와일드카드 지원을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="6933a-257">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="6933a-258">ARM에 대한 일반 호출을 수행할 때 사용되는 자격 증명을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="6933a-258">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="6933a-259">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6933a-259">Az.Sql</span></span>
* <span data-ttu-id="6933a-260">위협 탐지의 cmdlet 매개 변수(ExcludeDetectionType)가 DetectionType에서 string[]으로 변경되어 새 DetectionType이 추가되면 이후의 증명이 되고 자동 완성도 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="6933a-260">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="6933a-261">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="6933a-261">Az.Storage</span></span>
* <span data-ttu-id="6933a-262">스토리지 계정에 대한 관리 정책 가져오기/설정/제거를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="6933a-262">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="6933a-263">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="6933a-263">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="6933a-264">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="6933a-264">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="6933a-265">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="6933a-265">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="6933a-266">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="6933a-266">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="6933a-267">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="6933a-267">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="6933a-268">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="6933a-268">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="6933a-269">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="6933a-269">Az.Websites</span></span>
* <span data-ttu-id="6933a-270">'New-AzWebApp -IncludeSourceWebAppSlots'를 사용하여 모든 슬롯의 복제를 중단하는 ARM 템플릿 버그가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6933a-270">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span>

## <a name="150---march-2019"></a><span data-ttu-id="6933a-271">1.5.0 - 2019년 3월</span><span class="sxs-lookup"><span data-stu-id="6933a-271">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="6933a-272">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6933a-272">Az.Accounts</span></span>
* <span data-ttu-id="6933a-273">'Register-AzModule' 명령을 추가하여 AutoRest 생성 cmdlet을 지원</span><span class="sxs-lookup"><span data-stu-id="6933a-273">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="6933a-274">Connect-AzAccount 예제 업데이트</span><span class="sxs-lookup"><span data-stu-id="6933a-274">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="6933a-275">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="6933a-275">Az.Automation</span></span>
* <span data-ttu-id="6933a-276">몇몇 Azure Automation cmdlet에서 특정 월별 일정을 검색할 때 발생하는 문제 수정</span><span class="sxs-lookup"><span data-stu-id="6933a-276">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="6933a-277">상위 20개 노드를 반환하도록 Get-AzAutomationDscNode를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="6933a-277">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="6933a-278">이제 모든 노드 반환</span><span class="sxs-lookup"><span data-stu-id="6933a-278">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="6933a-279">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="6933a-279">Az.Cdn</span></span>
* <span data-ttu-id="6933a-280">사용자 지정 도메인 Https 사용/사용 안 함에 대한 새 Powershell cmdlet이 추가되었으며 기존의 것은 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="6933a-280">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6933a-281">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6933a-281">Az.Compute</span></span>
* <span data-ttu-id="6933a-282">Get cmdlet에 와일드 카드 지원 추가</span><span class="sxs-lookup"><span data-stu-id="6933a-282">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="6933a-283">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="6933a-283">Az.DataFactory</span></span>
* <span data-ttu-id="6933a-284">ADF.Net SDK 버전이 3.0.1로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6933a-284">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="6933a-285">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="6933a-285">Az.LogicApp</span></span>
* <span data-ttu-id="6933a-286">첫 결과 페이지 검색 시에만 ListWorkflows 수정</span><span class="sxs-lookup"><span data-stu-id="6933a-286">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6933a-287">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6933a-287">Az.Network</span></span>
* <span data-ttu-id="6933a-288">Network cmdlet에 와일드 카드 지원 추가</span><span class="sxs-lookup"><span data-stu-id="6933a-288">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="6933a-289">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="6933a-289">Az.RecoveryServices</span></span>
* <span data-ttu-id="6933a-290">Azure VM 지원에 SQL 서버가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6933a-290">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="6933a-291">SDK 업데이트</span><span class="sxs-lookup"><span data-stu-id="6933a-291">SDK Update</span></span>
* <span data-ttu-id="6933a-292">VMappContainer 체크 인 Get-ProtectableItem 제거</span><span class="sxs-lookup"><span data-stu-id="6933a-292">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="6933a-293">Get ProtectableItem의 매개 변수로 Name과 ServerName이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6933a-293">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="6933a-294">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6933a-294">Az.Resources</span></span>
* <span data-ttu-id="6933a-295">`-TemplateObject` 매개 변수를 추가하여 cmdlet을 배포</span><span class="sxs-lookup"><span data-stu-id="6933a-295">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="6933a-296">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/2933 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="6933a-296">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="6933a-297">`Get-AzResource`의 결과를 `Set-AzResource`(으)로 파이프할 때 발생하는 문제 수정</span><span class="sxs-lookup"><span data-stu-id="6933a-297">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="6933a-298">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/8240 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="6933a-298">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="6933a-299">실행 시 JSON 데이터 형식 문제 해결 `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="6933a-299">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="6933a-300">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/7930 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="6933a-300">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="6933a-301">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6933a-301">Az.Sql</span></span>
* <span data-ttu-id="6933a-302">AuditingEndpointsCommunicator를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="6933a-302">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="6933a-303">새 진단 설정을 생성할 때 에지 사례의 동작을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="6933a-303">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="6933a-304">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="6933a-304">Az.Storage</span></span>
* <span data-ttu-id="6933a-305">스토리지 계정      - New-AzStorageAccount를 생성할 때 종류 BlockBlobStorage를 지원</span><span class="sxs-lookup"><span data-stu-id="6933a-305">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="6933a-306">1.4.0 - 2019년 2월</span><span class="sxs-lookup"><span data-stu-id="6933a-306">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="6933a-307">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="6933a-307">Az.AnalysisServices</span></span>
* <span data-ttu-id="6933a-308">사용되지 않는 AddAzureASAccount cmdlet</span><span class="sxs-lookup"><span data-stu-id="6933a-308">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="6933a-309">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="6933a-309">Az.Automation</span></span>
* <span data-ttu-id="6933a-310">Import-AzAutomationDscNodeConfiguration 도움말 업데이트</span><span class="sxs-lookup"><span data-stu-id="6933a-310">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="6933a-311">Import-AzAutomationDscConfiguration cmdlet 구성 이름 유효성 검사 추가</span><span class="sxs-lookup"><span data-stu-id="6933a-311">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="6933a-312">Import-AzAutomationDscConfiguration cmdlet 오류 처리 개선</span><span class="sxs-lookup"><span data-stu-id="6933a-312">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="6933a-313">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="6933a-313">Az.CognitiveServices</span></span>
* <span data-ttu-id="6933a-314">리소스의 하위 도메인을 지정하는 데 사용되는 New-AzCognitiveServicesAccount에 대한 새 선택적 매개 변수로 CustomSubdomainName이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6933a-314">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6933a-315">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6933a-315">Az.Compute</span></span>
* <span data-ttu-id="6933a-316">ID 매개 변수 집합 문제 해결</span><span class="sxs-lookup"><span data-stu-id="6933a-316">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="6933a-317">Name 매개 변수를 제공하지 않으면 Get-AzVMExtension이 설치된 모든 확장을 열거하도록 업데이트</span><span class="sxs-lookup"><span data-stu-id="6933a-317">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="6933a-318">Update-AzImage cmdlet에 태그 및 ResourceId 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="6933a-318">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="6933a-319">인스턴스 ID가 없는 Get-AzVmssVM과 InstanceView를 사용하면 인스턴스 보기가 있는 VMSS VM을 나열할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6933a-319">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="6933a-320">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="6933a-320">Az.DataLakeStore</span></span>
* <span data-ttu-id="6933a-321">ADL 삭제된 항목 열거 및 복원에 대한 cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="6933a-321">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="6933a-322">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="6933a-322">Az.EventHub</span></span>
* <span data-ttu-id="6933a-323">Eventhub의 CaptureDescription 클래스에서 빈 보관을 건너뛰는 새 부울 속성 SkipEmptyArchives가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6933a-323">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="6933a-324">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="6933a-324">Az.KeyVault</span></span>
* <span data-ttu-id="6933a-325">Set-AzKeyVaultSecret 태그 지정 수정</span><span class="sxs-lookup"><span data-stu-id="6933a-325">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="6933a-326">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="6933a-326">Az.LogicApp</span></span>
* <span data-ttu-id="6933a-327">통합 계정에 대한 기본 sku 추가</span><span class="sxs-lookup"><span data-stu-id="6933a-327">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="6933a-328">XSLT 2.0, XSLT 3.0, Liquid 맵 형식 추가</span><span class="sxs-lookup"><span data-stu-id="6933a-328">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="6933a-329">통합 계정 어셈블리에 대한 새 cmdlet</span><span class="sxs-lookup"><span data-stu-id="6933a-329">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="6933a-330">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="6933a-330">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="6933a-331">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="6933a-331">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="6933a-332">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="6933a-332">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="6933a-333">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="6933a-333">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="6933a-334">통합 계정 일괄 처리 구성에 대한 새 cmdlet</span><span class="sxs-lookup"><span data-stu-id="6933a-334">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="6933a-335">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="6933a-335">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="6933a-336">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="6933a-336">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="6933a-337">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="6933a-337">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="6933a-338">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="6933a-338">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="6933a-339">논리 앱 SDK를 버전 4.1.0으로 업데이트</span><span class="sxs-lookup"><span data-stu-id="6933a-339">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="6933a-340">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="6933a-340">Az.Monitor</span></span>
* <span data-ttu-id="6933a-341">Get-AzMetric에 대한 도움말 업데이트</span><span class="sxs-lookup"><span data-stu-id="6933a-341">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6933a-342">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6933a-342">Az.Network</span></span>
* <span data-ttu-id="6933a-343">Add-AzApplicationGatewayCustomError에 대한 도움말 예제 업데이트</span><span class="sxs-lookup"><span data-stu-id="6933a-343">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="6933a-344">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="6933a-344">Az.OperationalInsights</span></span>
* <span data-ttu-id="6933a-345">New 및 Get ApplicationInsights 데이터 소스에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="6933a-345">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="6933a-346">지정된 작업 영역에 대한 특정 또는 전체 ApplicationInsights 데이터 원본 가져오기를 지원하기 위한 새로운 'ApplicationInsights' 종류가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6933a-346">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span>
    - <span data-ttu-id="6933a-347">지정된 Application-Insights 리소스 매개 변수(구독 ID, resourceGroupName 및 이름)별로 데이터 원본을 만들기 위한 New-AzOperationalInsightsApplicationInsightsDataSource cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6933a-347">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span>

#### <a name="azresources"></a><span data-ttu-id="6933a-348">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6933a-348">Az.Resources</span></span>
* <span data-ttu-id="6933a-349">문제 https://github.com/Azure/azure-powershell/issues/8166 수정</span><span class="sxs-lookup"><span data-stu-id="6933a-349">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="6933a-350">문제 https://github.com/Azure/azure-powershell/issues/8235 수정</span><span class="sxs-lookup"><span data-stu-id="6933a-350">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="6933a-351">문제 https://github.com/Azure/azure-powershell/issues/6219 수정</span><span class="sxs-lookup"><span data-stu-id="6933a-351">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="6933a-352">KeyCredentials 반복 만들기를 방지하기 위해 버그 수정</span><span class="sxs-lookup"><span data-stu-id="6933a-352">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="6933a-353">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6933a-353">Az.Sql</span></span>
* <span data-ttu-id="6933a-354">SQL DB 하이퍼스케일에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="6933a-354">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="6933a-355">복원 요청에서 불필요한 속성을 설정하여 복원이 실패할 수 있는 버그 수정</span><span class="sxs-lookup"><span data-stu-id="6933a-355">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="6933a-356">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="6933a-356">Az.Websites</span></span>
* <span data-ttu-id="6933a-357">Get-AzWebAppSlotMetrics 내 올바른 예제</span><span class="sxs-lookup"><span data-stu-id="6933a-357">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="6933a-358">1.3.0 - 2019년 2월</span><span class="sxs-lookup"><span data-stu-id="6933a-358">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="6933a-359">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6933a-359">Az.Accounts</span></span>
* <span data-ttu-id="6933a-360">ClientRuntime 최신 버전 업데이트</span><span class="sxs-lookup"><span data-stu-id="6933a-360">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="6933a-361">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="6933a-361">Az.AnalysisServices</span></span>
<span data-ttu-id="6933a-362">Az.AnalysisServices 모듈의 전반적인 가용성.</span><span class="sxs-lookup"><span data-stu-id="6933a-362">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6933a-363">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6933a-363">Az.Compute</span></span>
* <span data-ttu-id="6933a-364">AEM 확장: UltraSSD 및 P60, P70, P80 디스크에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="6933a-364">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="6933a-365">Set-AzVMBootDiagnostics에 대한 도움말 업데이트</span><span class="sxs-lookup"><span data-stu-id="6933a-365">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="6933a-366">Update-AzImage에 대한 도움말 및 예제 업데이트</span><span class="sxs-lookup"><span data-stu-id="6933a-366">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="6933a-367">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="6933a-367">Az.RecoveryServices</span></span>
<span data-ttu-id="6933a-368">Az.RecoveryServices 모듈의 전반적인 가용성.</span><span class="sxs-lookup"><span data-stu-id="6933a-368">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="6933a-369">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6933a-369">Az.Resources</span></span>
* <span data-ttu-id="6933a-370">리소스 그룹 관련 태그 수정</span><span class="sxs-lookup"><span data-stu-id="6933a-370">Fix tagging for resource groups</span></span>
    - <span data-ttu-id="6933a-371">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/8166 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="6933a-371">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="6933a-372">`Get-AzureRmRoleAssignment`이(가) -ErrorAction을 준수하지 않는 문제 수정</span><span class="sxs-lookup"><span data-stu-id="6933a-372">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span>
    - <span data-ttu-id="6933a-373">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/8235 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="6933a-373">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="6933a-374">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6933a-374">Az.Sql</span></span>
* <span data-ttu-id="6933a-375">AzSqlDatabaseBackupShortTermRetentionPolicy 가져오기/설정하기 추가</span><span class="sxs-lookup"><span data-stu-id="6933a-375">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="6933a-376">SQL cmdlet을 실행할 경우 Azure 계정에 로그인되어 있지 않은 것이 nullref 예외를 초래하는 문제 수정</span><span class="sxs-lookup"><span data-stu-id="6933a-376">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="6933a-377">Get-AzSqlCapability의 nullref 예외 수정</span><span class="sxs-lookup"><span data-stu-id="6933a-377">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="6933a-378">1.2.1 - 2019년 1월</span><span class="sxs-lookup"><span data-stu-id="6933a-378">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="6933a-379">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6933a-379">Az.Accounts</span></span>
* <span data-ttu-id="6933a-380">올바른 인증 버전을 사용하여 릴리스</span><span class="sxs-lookup"><span data-stu-id="6933a-380">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="6933a-381">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="6933a-381">Az.AnalysisServices</span></span>
* <span data-ttu-id="6933a-382">업데이트된 인증 종속성을 사용하여 릴리스</span><span class="sxs-lookup"><span data-stu-id="6933a-382">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="6933a-383">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="6933a-383">Az.RecoveryServices</span></span>
* <span data-ttu-id="6933a-384">업데이트된 인증 종속성을 사용하여 릴리스</span><span class="sxs-lookup"><span data-stu-id="6933a-384">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="6933a-385">1.2.0 - 2019년 1월</span><span class="sxs-lookup"><span data-stu-id="6933a-385">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="6933a-386">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6933a-386">Az.Accounts</span></span>
* <span data-ttu-id="6933a-387">Windows PowerShell 5.1 전용 대화형 사용자 이름/암호 인증 추가</span><span class="sxs-lookup"><span data-stu-id="6933a-387">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="6933a-388">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="6933a-388">Update incorrect online help URLs</span></span>
* <span data-ttu-id="6933a-389">Uninstall-AzureRm 관련 PS Core에 경고 메시지 추가</span><span class="sxs-lookup"><span data-stu-id="6933a-389">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="6933a-390">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="6933a-390">Az.Aks</span></span>
* <span data-ttu-id="6933a-391">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="6933a-391">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="6933a-392">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="6933a-392">Az.Automation</span></span>
* <span data-ttu-id="6933a-393">Python 2 Runbook에 대한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6933a-393">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="6933a-394">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="6933a-394">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="6933a-395">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="6933a-395">Az.Cdn</span></span>
* <span data-ttu-id="6933a-396">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="6933a-396">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6933a-397">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6933a-397">Az.Compute</span></span>
* <span data-ttu-id="6933a-398">Invoke-AzVMReimage cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="6933a-398">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="6933a-399">Set-AzVmss에 TempDisk 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="6933a-399">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="6933a-400">New-AzVM 경고 메시지 수정</span><span class="sxs-lookup"><span data-stu-id="6933a-400">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="6933a-401">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="6933a-401">Az.ContainerRegistry</span></span>
* <span data-ttu-id="6933a-402">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="6933a-402">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="6933a-403">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="6933a-403">Az.DataFactory</span></span>
* <span data-ttu-id="6933a-404">ADF.Net SDK 버전이 3.0.0으로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6933a-404">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="6933a-405">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="6933a-405">Az.DataLakeStore</span></span>
* <span data-ttu-id="6933a-406">MSI를 사용할 때 ADLS 엔드포인트 문제 수정</span><span class="sxs-lookup"><span data-stu-id="6933a-406">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="6933a-407">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/7462 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="6933a-407">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="6933a-408">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="6933a-408">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="6933a-409">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="6933a-409">Az.IotHub</span></span>
* <span data-ttu-id="6933a-410">Add-IotHubRoutingEndpoint cmdlet에 인코딩 형식을 추가하세요.</span><span class="sxs-lookup"><span data-stu-id="6933a-410">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="6933a-411">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="6933a-411">Az.KeyVault</span></span>
* <span data-ttu-id="6933a-412">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="6933a-412">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6933a-413">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6933a-413">Az.Network</span></span>
* <span data-ttu-id="6933a-414">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="6933a-414">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="6933a-415">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6933a-415">Az.Resources</span></span>
* <span data-ttu-id="6933a-416">'New-AzADAppCredential' 및 'New-AzADSpCredential' 참조 설명서의 잘못된 예제 수정</span><span class="sxs-lookup"><span data-stu-id="6933a-416">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="6933a-417">리소스 그룹 배포 cmdlet 실행 전 '-TemplateFile' 매개 변수 경로가 확인되지 않는 문제 수정</span><span class="sxs-lookup"><span data-stu-id="6933a-417">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="6933a-418">Az.Resources: New-AzureRmPolicyDefinition -Mode 기본값에 대한 올바른 설명서</span><span class="sxs-lookup"><span data-stu-id="6933a-418">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="6933a-419">Az.Resources: 문제 https://github.com/Azure/azure-powershell/issues/7522 수정</span><span class="sxs-lookup"><span data-stu-id="6933a-419">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="6933a-420">Az.Resources: 문제 https://github.com/Azure/azure-powershell/issues/5747 수정</span><span class="sxs-lookup"><span data-stu-id="6933a-420">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="6933a-421">'PSResourceGroupDeployment' 개체의 서식 문제 수정</span><span class="sxs-lookup"><span data-stu-id="6933a-421">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="6933a-422">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/2123 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="6933a-422">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="6933a-423">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="6933a-423">Az.ServiceFabric</span></span>
* <span data-ttu-id="6933a-424">인증서가 VMSS 모델에 추가되었는데도 예외가 발생할 경우 롤백합니다. 이는 버그 https://github.com/Azure/service-fabric-issues/issues/932 를 수정하기 위함입니다.</span><span class="sxs-lookup"><span data-stu-id="6933a-424">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="6933a-425">일부 오류 메시지를 수정하세요.</span><span class="sxs-lookup"><span data-stu-id="6933a-425">Fix some error messages.</span></span>
* <span data-ttu-id="6933a-426">Az로의 마이그레이션을 통해서는 작동하지 않는 New-AzServiceFabriCluster를 위해 기본값 ARM 템플릿을 가진 클러스터 만들기를 수정하세요.</span><span class="sxs-lookup"><span data-stu-id="6933a-426">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="6933a-427">확장에서 클러스터 id를 확인하여 클러스터에 해당하는 VMSS에만 추가되도록 클러스터/애플리케이션 인증서 추가를 수정하세요.</span><span class="sxs-lookup"><span data-stu-id="6933a-427">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="6933a-428">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="6933a-428">Az.SignalR</span></span>
* <span data-ttu-id="6933a-429">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="6933a-429">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="6933a-430">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6933a-430">Az.Sql</span></span>
* <span data-ttu-id="6933a-431">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="6933a-431">Update incorrect online help URLs</span></span>
* <span data-ttu-id="6933a-432">가능한 값을 가진 LicenseType 매개 변수에 대한 매개 변수 설명이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6933a-432">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="6933a-433">유일하게 업데이트된 속성인데 작동하지 않는 관리되는 인스턴스 ID의 업데이트 수정</span><span class="sxs-lookup"><span data-stu-id="6933a-433">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="6933a-434">관리되는 인스턴스에서의 사용자 지정 데이터 정렬에 대한 지원</span><span class="sxs-lookup"><span data-stu-id="6933a-434">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="6933a-435">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="6933a-435">Az.Storage</span></span>
* <span data-ttu-id="6933a-436">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="6933a-436">Update incorrect online help URLs</span></span>
* <span data-ttu-id="6933a-437">Premium Storage 계정이 클래식 로깅/메트릭을 지원하지 않기 때문에, Premium Storage 계정의 클래식 로깅/메트릭을 가져올/설정할 때 상세한 오류 메시지를 제공해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="6933a-437">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="6933a-438">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="6933a-438">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="6933a-439">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="6933a-439">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="6933a-440">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="6933a-440">Az.TrafficManager</span></span>
* <span data-ttu-id="6933a-441">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="6933a-441">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="6933a-442">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="6933a-442">Az.Websites</span></span>
* <span data-ttu-id="6933a-443">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="6933a-443">Update incorrect online help URLs</span></span>
* <span data-ttu-id="6933a-444">앱이 ASE에 호스팅되면 'New-AzWebAppSSLBinding'을 수정하여 올바른 resourcegroup+location에 인증서를 업로드합니다.</span><span class="sxs-lookup"><span data-stu-id="6933a-444">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="6933a-445">'New-AzWebAppSSLBinding'을 수정하여 SSL 인증서를 앱에 바인딩하는 데 붙는 태그를 덮어쓰지 않도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="6933a-445">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="6933a-446">1.1.0 - 2019년 1월</span><span class="sxs-lookup"><span data-stu-id="6933a-446">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="6933a-447">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6933a-447">Az.Accounts</span></span>
* <span data-ttu-id="6933a-448">Enable-AzureRmAlias에 'Local' 범위 추가</span><span class="sxs-lookup"><span data-stu-id="6933a-448">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6933a-449">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6933a-449">Az.Compute</span></span>
* <span data-ttu-id="6933a-450">이름이 Restart/Start/Stop/Remove/Set-AzVM과 Save-AzVMImage에 설정된 ID 매개 변수에서 선택 사항이 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6933a-450">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="6933a-451">도움말 파일의 ID에 대한 설명이 업데이트 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6933a-451">Updated the description of ID in help files</span></span>
* <span data-ttu-id="6933a-452">Az.Accounts 모듈을 사용할 때의 이전 버전과의 호환성 문제를 해결합니다.</span><span class="sxs-lookup"><span data-stu-id="6933a-452">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="6933a-453">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="6933a-453">Az.DataLakeStore</span></span>
* <span data-ttu-id="6933a-454">SDK 수정을 위해 데이터 평면의 SDK 버전을 1.1.14로 업데이트하세요.</span><span class="sxs-lookup"><span data-stu-id="6933a-454">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="6933a-455">getfilestatus 및 liststatus에 대한 음수 acesstime 및 modificationtime 수정, 비동기 취소 토큰 수정</span><span class="sxs-lookup"><span data-stu-id="6933a-455">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="6933a-456">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="6933a-456">Az.EventGrid</span></span>
* <span data-ttu-id="6933a-457">2019-01-01 API 버전을 사용하도록 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6933a-457">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="6933a-458">2019-01-01 API 버전에서 새 시나리오를 지원하도록 다음 cmdlet을 업데이트</span><span class="sxs-lookup"><span data-stu-id="6933a-458">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="6933a-459">New-AzureRmEventGridSubscription: 지정을 위한 새로운 선택적 매개 변수를 추가</span><span class="sxs-lookup"><span data-stu-id="6933a-459">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="6933a-460">이벤트 Time-to-Live</span><span class="sxs-lookup"><span data-stu-id="6933a-460">Event Time-To-Live,</span></span>
        - <span data-ttu-id="6933a-461">이벤트에 대한 최대 배달 시도</span><span class="sxs-lookup"><span data-stu-id="6933a-461">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="6933a-462">배달 못한 편지의 엔드포인트입니다.</span><span class="sxs-lookup"><span data-stu-id="6933a-462">Dead letter endpoint.</span></span>
    - <span data-ttu-id="6933a-463">Update-AzureRmEventGridSubscription: 지정을 위한 새로운 선택적 매개 변수를 추가</span><span class="sxs-lookup"><span data-stu-id="6933a-463">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="6933a-464">이벤트 Time-to-Live</span><span class="sxs-lookup"><span data-stu-id="6933a-464">Event Time-To-Live,</span></span>
        - <span data-ttu-id="6933a-465">이벤트에 대한 최대 배달 시도</span><span class="sxs-lookup"><span data-stu-id="6933a-465">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="6933a-466">배달 못한 편지의 엔드포인트입니다.</span><span class="sxs-lookup"><span data-stu-id="6933a-466">Dead letter endpoint.</span></span>
* <span data-ttu-id="6933a-467">New-AzureRmEventGridSubscription 및 Update-AzureRmEventGridSubscription cmdlet의 EndpointType 옵션에 새 열거형 값(즉, storageQueue 및 hybridConnection)을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="6933a-467">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="6933a-468">이벤트 구독을 생성 또는 업데이트할 때 사용자가 직접 조치를 취해야 할 경우 경고 메시지를 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="6933a-468">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="6933a-469">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="6933a-469">Az.IotHub</span></span>
* <span data-ttu-id="6933a-470">최신 버전의 Azure IotHub SDK로 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="6933a-470">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="6933a-471">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="6933a-471">Az.LogicApp</span></span>
* <span data-ttu-id="6933a-472">지정된 이름이 없는 모든 Get-AzLogicApp 목록</span><span class="sxs-lookup"><span data-stu-id="6933a-472">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="6933a-473">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6933a-473">Az.Resources</span></span>
* <span data-ttu-id="6933a-474">'Get-AzResource'에 '-ODataQuery'및 '-ResourceId' 매개 변수를 제공할 때 매개 변수 집합 문제 수정</span><span class="sxs-lookup"><span data-stu-id="6933a-474">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="6933a-475">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/7875 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="6933a-475">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="6933a-476">New/Set-AzPolicyDefinition에서 -Custom 매개 변수 처리 문제 수정</span><span class="sxs-lookup"><span data-stu-id="6933a-476">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="6933a-477">New-AzDeployment 설명서에서 오타 수정</span><span class="sxs-lookup"><span data-stu-id="6933a-477">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="6933a-478">'New-AzADUser'에 '-MailNickname'매개 변수가 필수 항목으로 지정됨</span><span class="sxs-lookup"><span data-stu-id="6933a-478">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="6933a-479">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/8220 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="6933a-479">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="6933a-480">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="6933a-480">Az.SignalR</span></span>
* <span data-ttu-id="6933a-481">Az.Accounts 모듈을 사용할 때의 이전 버전과의 호환성 문제를 해결합니다.</span><span class="sxs-lookup"><span data-stu-id="6933a-481">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="6933a-482">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6933a-482">Az.Sql</span></span>
* <span data-ttu-id="6933a-483">Storage 관리 클라이언트 종속성을 일반적인 SDK 구현으로 변환했습니다.</span><span class="sxs-lookup"><span data-stu-id="6933a-483">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="6933a-484">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="6933a-484">Az.Storage</span></span>
* <span data-ttu-id="6933a-485">Sas Token, OAuth 또는 Anonymous를 사용하여 스토리지 컨텍스트의 StorageAccountName을 실제 스토리지 계정 이름으로 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="6933a-485">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="6933a-486">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="6933a-486">New-AzStorageContext</span></span>
* <span data-ttu-id="6933a-487">'-FullUri' 매개 변수를 사용하여 Blob 스냅샷 개체의 Sas Token을 생성하고 반환된 Uri를 스냅샷 Uri로 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="6933a-487">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="6933a-488">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="6933a-488">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="6933a-489">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="6933a-489">Az.Websites</span></span>
* <span data-ttu-id="6933a-490">'Get-AzDeletedWebApp'의 날짜 구문 분석 버그를 수정했습니다.</span><span class="sxs-lookup"><span data-stu-id="6933a-490">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="6933a-491">Az.Accounts 모듈을 사용할 때의 이전 버전과의 호환성 문제를 해결합니다.</span><span class="sxs-lookup"><span data-stu-id="6933a-491">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="6933a-492">1.0.0 - 2018년 12월</span><span class="sxs-lookup"><span data-stu-id="6933a-492">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="6933a-493">일반</span><span class="sxs-lookup"><span data-stu-id="6933a-493">General</span></span>

- <span data-ttu-id="6933a-494">Az 모듈 일반 공급</span><span class="sxs-lookup"><span data-stu-id="6933a-494">General Availability of Az Module</span></span>
- <span data-ttu-id="6933a-495">각 모듈에 대 한 온라인 도움말</span><span class="sxs-lookup"><span data-stu-id="6933a-495">Online help for each module</span></span>
- <span data-ttu-id="6933a-496">자세한 내용과 로드맵은 [Az 알림 페이지](https://aka.ms/azps-announce)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="6933a-496">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="6933a-497">AzureRM에서 마이그레이션하는 것에 대한 정보는 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="6933a-497">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="6933a-498">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6933a-498">Az.Accounts</span></span>
- <span data-ttu-id="6933a-499">Az.Profile에서 변경</span><span class="sxs-lookup"><span data-stu-id="6933a-499">Changed from Az.Profile</span></span>
- <span data-ttu-id="6933a-500">프로필 및 컨텍스트 형식에 대한 표 형식 수정</span><span class="sxs-lookup"><span data-stu-id="6933a-500">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="6933a-501">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="6933a-501">Az.ApiManagement</span></span>
- <span data-ttu-id="6933a-502">#7002에 대한 수정</span><span class="sxs-lookup"><span data-stu-id="6933a-502">Fixes for #7002</span></span>
- <span data-ttu-id="6933a-503">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="6933a-503">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="6933a-504">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="6933a-504">Az.Batch</span></span>
- <span data-ttu-id="6933a-505">`PSComputeNode`의 새로운 `NodeAgentInformation` 속성을 통해 풀의 각 VM에서 실행 중인 Azure Batch 노드 에이전트의 버전을 확인하는 기능이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6933a-505">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="6933a-506">`PSDataDisk`에 대한 `Caching` 기본 값은 이제 `None` 대신 `ReadWrite`입니다.</span><span class="sxs-lookup"><span data-stu-id="6933a-506">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="6933a-507">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="6933a-507">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="6933a-508">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="6933a-508">Az.Billing</span></span>
- <span data-ttu-id="6933a-509">청구, 소비 및 UsageAggregates cmdlet 결합 cmdlet에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="6933a-509">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="6933a-510">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="6933a-510">Az.CognitivServices</span></span>
- <span data-ttu-id="6933a-511">New-AzureRmCognitiveServicesAccount 작업에서 사용 가능한 SkuName 및 Typem에 대한 완성자 추가</span><span class="sxs-lookup"><span data-stu-id="6933a-511">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="6933a-512">Get-AzCognitiveServicesAccountSkus에서 GetSkusWithAccountParamSetName 매개 변수 집합을 제거</span><span class="sxs-lookup"><span data-stu-id="6933a-512">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="6933a-513">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="6933a-513">Az.ContainerInstance</span></span>
- <span data-ttu-id="6933a-514">ManagedIdentity 지원이 추가됨</span><span class="sxs-lookup"><span data-stu-id="6933a-514">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="6933a-515">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="6933a-515">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="6933a-516">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="6933a-516">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="6933a-517">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="6933a-517">Az.DataLakeStore</span></span>
- <span data-ttu-id="6933a-518">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="6933a-518">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="6933a-519">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="6933a-519">Az.Monitor</span></span>
- <span data-ttu-id="6933a-520">Az.Monitor 이름 변경 및 기타 사소한 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="6933a-520">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="6933a-521">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="6933a-521">Az.KeyVault</span></span>
- <span data-ttu-id="6933a-522">출력 형식에서 사용되지 않는 'PurgeDisabled' 속성 제거</span><span class="sxs-lookup"><span data-stu-id="6933a-522">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="6933a-523">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="6933a-523">Az.MachineLearning</span></span>
- <span data-ttu-id="6933a-524">Az.MachineLearningCompute 모듈의 cmdlet 포함</span><span class="sxs-lookup"><span data-stu-id="6933a-524">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="6933a-525">Az.Media</span><span class="sxs-lookup"><span data-stu-id="6933a-525">Az.Media</span></span>
- <span data-ttu-id="6933a-526">New-AzMediaService에서 사용되지 않는 -Tags 별칭이 제거됨</span><span class="sxs-lookup"><span data-stu-id="6933a-526">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="6933a-527">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6933a-527">Az.Network</span></span>
<span data-ttu-id="6933a-528">Application Gateway에서 RewriteRuleSets를 구성하는 것에 대한 지원이 추가됨</span><span class="sxs-lookup"><span data-stu-id="6933a-528">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="6933a-529">추가된 새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="6933a-529">New cmdlets added:</span></span>
        - <span data-ttu-id="6933a-530">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="6933a-530">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="6933a-531">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="6933a-531">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="6933a-532">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="6933a-532">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="6933a-533">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="6933a-533">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="6933a-534">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="6933a-534">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="6933a-535">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="6933a-535">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="6933a-536">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="6933a-536">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="6933a-537">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="6933a-537">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="6933a-538">선택적 매개 변수를 사용하도록 cmdlet이 업데이트됨 -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="6933a-538">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="6933a-539">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6933a-539">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="6933a-540">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="6933a-540">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="6933a-541">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="6933a-541">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="6933a-542">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="6933a-542">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="6933a-543">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="6933a-543">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="6933a-544">New-AzureRmApplicationGatewayUrlPathMapConfig로 ID를 사용하여 Application Gateway에 KeyVault 지원을 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="6933a-544">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="6933a-545">선택적 매개 변수를 사용하도록 cmdlet이 업데이트됨 -KeyVaultSecretId, -KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="6933a-545">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="6933a-546">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="6933a-546">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="6933a-547">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="6933a-547">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="6933a-548">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="6933a-548">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="6933a-549">New-AzApplicationGateway cmdlet이 선택적 매개 변수를 사용하도록 업데이트됨 -UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="6933a-549">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="6933a-550">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="6933a-550">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="6933a-551">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="6933a-551">Az.OperationalInsights</span></span>
- <span data-ttu-id="6933a-552">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="6933a-552">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="6933a-553">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="6933a-553">Az.Profile</span></span>
- <span data-ttu-id="6933a-554">Az.Accounts에 모듈 이름이 변경됨</span><span class="sxs-lookup"><span data-stu-id="6933a-554">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="6933a-555">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="6933a-555">Az.RecoveryServices</span></span>
- <span data-ttu-id="6933a-556">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="6933a-556">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="6933a-557">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6933a-557">Az.Resources</span></span>
- <span data-ttu-id="6933a-558">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="6933a-558">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="6933a-559">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="6933a-559">Az.ServiceFabric</span></span>
- <span data-ttu-id="6933a-560">일반 이름과 지문으로 지정 인증서 지원</span><span class="sxs-lookup"><span data-stu-id="6933a-560">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="6933a-561">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="6933a-561">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="6933a-562">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="6933a-562">Az.SIgnalR</span></span>
- <span data-ttu-id="6933a-563">SIgnalR에 대한 PowerShell cmdlet에 대한 일반 공급</span><span class="sxs-lookup"><span data-stu-id="6933a-563">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="6933a-564">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6933a-564">Az.Sql</span></span>
- <span data-ttu-id="6933a-565">위협 탐지의 cmdlet에 새로운 Data_Exfiltration 및 Unsafe_Action 검색 유형 추가</span><span class="sxs-lookup"><span data-stu-id="6933a-565">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="6933a-566">Sql 감사 cmdlet에 대한 설명서 예제 업데이트</span><span class="sxs-lookup"><span data-stu-id="6933a-566">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="6933a-567">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="6933a-567">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="6933a-568">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="6933a-568">Az.Storage</span></span>
- <span data-ttu-id="6933a-569">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="6933a-569">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="6933a-570">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="6933a-570">Az.Websites</span></span>
- <span data-ttu-id="6933a-571">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="6933a-571">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="6933a-572">0.7.0 - 2018년 12월</span><span class="sxs-lookup"><span data-stu-id="6933a-572">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="6933a-573">일반</span><span class="sxs-lookup"><span data-stu-id="6933a-573">General</span></span>

* <span data-ttu-id="6933a-574">AzureRM에서 Az 전환 예정에 대한 사소한 변경</span><span class="sxs-lookup"><span data-stu-id="6933a-574">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="6933a-575">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6933a-575">Az.Compute</span></span>

* <span data-ttu-id="6933a-576">`New-AzVm(ss)` cmdlet에 대한 간단한 매개 변수 집합에 UltraSSD 및 갤러리 이미지에 대한 지원을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="6933a-576">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="6933a-577">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="6933a-577">Az.DataLakeStore</span></span>

* <span data-ttu-id="6933a-578">ADLS 계정의 도메인의 후행 슬래시를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="6933a-578">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="6933a-579">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="6933a-579">Az.FrontDoor</span></span>

* <span data-ttu-id="6933a-580">일부 끊어진 링크 수정</span><span class="sxs-lookup"><span data-stu-id="6933a-580">Fixed some broken links</span></span>
    - <span data-ttu-id="6933a-581">New-AzureRmFrontDoor 및 Set-AzureRmFrontDoor 아티클에서 New-AzureRmFrontDoorHealthProbeSettingObject cmdlet 아티클에 대한 링크가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6933a-581">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="6933a-582">New-AzureRmFrontDoorManagedRuleObject 아티클에서 New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet 아티클에 대한 링크가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6933a-582">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="6933a-583">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="6933a-583">Az.RecoveryServices</span></span>

* <span data-ttu-id="6933a-584">Azure File Share 복원 작업에 클라이언트 측 유효성 검사가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6933a-584">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="6933a-585">afs 복원의 경우 storageAccountName 및 storageAccountResourceGroupName을 선택적으로 만들었습니다.</span><span class="sxs-lookup"><span data-stu-id="6933a-585">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="6933a-586">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6933a-586">Az.Resources</span></span>

* <span data-ttu-id="6933a-587">https://github.com/Azure/azure-powershell/issues/7679 에 대한 수정</span><span class="sxs-lookup"><span data-stu-id="6933a-587">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="6933a-588">기본 관리자를 요청할 때 구독 범위가 제공되는 경우 Get-AzureRmRoleAssignment를 업데이트하여 구독 범위를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="6933a-588">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="6933a-589">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6933a-589">Az.Sql</span></span>

* <span data-ttu-id="6933a-590">AzureRM에서 Az 전환 예정에 대한 사소한 변경</span><span class="sxs-lookup"><span data-stu-id="6933a-590">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="6933a-591">DotNet 코어에서 Get-AzureRmSqlDatabaseVulnerabilityAssessment를 사용하는 문제 해결</span><span class="sxs-lookup"><span data-stu-id="6933a-591">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="6933a-592">SQL 감사 cmdlet과 관련된 도움말 메시지의 설명서가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6933a-592">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="6933a-593">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="6933a-593">Az.Storage</span></span>

* <span data-ttu-id="6933a-594">New-AzureRmStorageAccount에 -EnableHierarchicalNamespace 추가</span><span class="sxs-lookup"><span data-stu-id="6933a-594">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="6933a-595">파일 복사 cmdlet이 -DestContext 입력이 없을 때 대상의 원본 컨텍스트를 다시 사용할 수 없는 문제 수정</span><span class="sxs-lookup"><span data-stu-id="6933a-595">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="6933a-596">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="6933a-596">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="6933a-597">고정적인 웹 사이트 구성 지원</span><span class="sxs-lookup"><span data-stu-id="6933a-597">Support Static Website configuration</span></span>
    - <span data-ttu-id="6933a-598">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="6933a-598">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="6933a-599">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="6933a-599">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="6933a-600">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="6933a-600">Az.Websites</span></span>

* <span data-ttu-id="6933a-601">Set-AzureRmWebApp 및 Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="6933a-601">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span>
    - <span data-ttu-id="6933a-602">Windows 및 Linux 컨테이너 응용 프로그램에 탑재할 Azure Storage 경로를 지정하기 위해 새 매개 변수(-AzureStoragePath)가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6933a-602">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="6933a-603">새 cmdlet New-AzureRmWebAppAzureStoragePath의 출력을 매개 변수로 사용하여 Azure Storage 경로를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="6933a-603">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="6933a-604">0.6.1 - 2018년 11월</span><span class="sxs-lookup"><span data-stu-id="6933a-604">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="6933a-605">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="6933a-605">Az.ApiManagement</span></span>
* <span data-ttu-id="6933a-606">형식 매핑 문제에 대한 종속성 업데이트</span><span class="sxs-lookup"><span data-stu-id="6933a-606">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="6933a-607">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="6933a-607">Az.Automation</span></span>
* <span data-ttu-id="6933a-608">Azure Automation cmdlet 기반 Swagger</span><span class="sxs-lookup"><span data-stu-id="6933a-608">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="6933a-609">업데이트 관리 cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="6933a-609">Added Update Management cmdlets</span></span>
* <span data-ttu-id="6933a-610">소스 제어 cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="6933a-610">Added Source Control cmdlets</span></span>
* <span data-ttu-id="6933a-611">Remove-AzureRmAutomationHybridWorkerGroup cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="6933a-611">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="6933a-612">DSC 노드 등록 명령 수정</span><span class="sxs-lookup"><span data-stu-id="6933a-612">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="6933a-613">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6933a-613">Az.Compute</span></span>
* <span data-ttu-id="6933a-614">SystemAssigned ID에 대한 ID 문제 수정</span><span class="sxs-lookup"><span data-stu-id="6933a-614">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="6933a-615">형식 매핑 문제에 대한 종속성 업데이트</span><span class="sxs-lookup"><span data-stu-id="6933a-615">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="6933a-616">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="6933a-616">Az.ContainerInstance</span></span>
* <span data-ttu-id="6933a-617">형식 매핑 문제에 대한 종속성 업데이트</span><span class="sxs-lookup"><span data-stu-id="6933a-617">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="6933a-618">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="6933a-618">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="6933a-619">마켓플레이스 cmdlet에 대한 예제 설명 업데이트</span><span class="sxs-lookup"><span data-stu-id="6933a-619">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="6933a-620">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6933a-620">Az.Network</span></span>
* <span data-ttu-id="6933a-621">New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="6933a-621">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="6933a-622">지원되는 AzureFirewall 네트워크 프로토콜에 ICMP 다시 추가</span><span class="sxs-lookup"><span data-stu-id="6933a-622">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="6933a-623">Test-AzureRmNetworkWatcherConnectivity cmdlet을 업데이트하여 대상 ID, 주소 및 포트 유효성 검사를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="6933a-623">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span>
* <span data-ttu-id="6933a-624">VirtualNetwork 맵의 메모리 사용 문제 해결</span><span class="sxs-lookup"><span data-stu-id="6933a-624">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="6933a-625">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="6933a-625">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="6933a-626">보호된 파일 공유에 대한 정책을 수정하는 것에 대해 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="6933a-626">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="6933a-627">정책 표준 시간대를 대문자로 변환했습니다.</span><span class="sxs-lookup"><span data-stu-id="6933a-627">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="6933a-628">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="6933a-628">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="6933a-629">New-AzureRmRecoveryServicesAsrProtectableItem의 예제 정정</span><span class="sxs-lookup"><span data-stu-id="6933a-629">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="6933a-630">형식 매핑 문제에 대한 종속성 업데이트</span><span class="sxs-lookup"><span data-stu-id="6933a-630">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="6933a-631">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="6933a-631">Az.Relay</span></span>
* <span data-ttu-id="6933a-632">선택적 매개 변수 -KeyValue를 New-AzureRmRelayKey cmdlet에 추가하여 사용자가 KeyValue를 제공할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6933a-632">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="6933a-633">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6933a-633">Az.Resources</span></span>
* <span data-ttu-id="6933a-634">`New-AzureRmPolicyAssignment` 및 `Set-AzureRmPolicyAssignment`의 자원 ID 관련 매개 변수에 대한 도움말 문서를 업데이트함</span><span class="sxs-lookup"><span data-stu-id="6933a-634">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="6933a-635">-Metadata를 사용하는 New-AzureRmPolicyDefinition에 대한 예제 추가</span><span class="sxs-lookup"><span data-stu-id="6933a-635">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="6933a-636">NetStandard의 태그 키에서 대소문자 보존을 허용하도록 수정: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="6933a-636">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="6933a-637">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="6933a-637">Az.ServiceFabric</span></span>
* <span data-ttu-id="6933a-638">향후 호환성이 손상되는 변경에 대한 사용 중단 메시지 추가</span><span class="sxs-lookup"><span data-stu-id="6933a-638">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="6933a-639">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6933a-639">Az.Sql</span></span>
* <span data-ttu-id="6933a-640">Azure Sql Database Managed Instance 및 Azure Sql Managed Database에 CRUD 작업을 위한 새 cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="6933a-640">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="6933a-641">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="6933a-641">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="6933a-642">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="6933a-642">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="6933a-643">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="6933a-643">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="6933a-644">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="6933a-644">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="6933a-645">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="6933a-645">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="6933a-646">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="6933a-646">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="6933a-647">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="6933a-647">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="6933a-648">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="6933a-648">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="6933a-649">서버 또는 데이터베이스에서 확장 감사 정책 관리를 활성화했습니다.</span><span class="sxs-lookup"><span data-stu-id="6933a-649">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="6933a-650">새 매개 변수(PredicateExpression)가 감사 로그 필터링을 사용하도록 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6933a-650">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="6933a-651">Cmdlet이 레거시 클라이언트 대신 SQL 클라이언트를 사용하도록 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6933a-651">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="6933a-652">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="6933a-652">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="6933a-653">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="6933a-653">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="6933a-654">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="6933a-654">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="6933a-655">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="6933a-655">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="6933a-656">스토리지 계정 이름 매개 변수가 설정된 Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings를 사용할 때의 문제 해결</span><span class="sxs-lookup"><span data-stu-id="6933a-656">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="6933a-657">0.5.0 - 2018년 11월</span><span class="sxs-lookup"><span data-stu-id="6933a-657">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="6933a-658">일반</span><span class="sxs-lookup"><span data-stu-id="6933a-658">General</span></span>
* <span data-ttu-id="6933a-659">많은 핵심 cmdlet에 Resource Completers를 추가하여 대화형으로 cmdlet을 호출할 때 기존 리소스 이름을 탭으로 이동할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6933a-659">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="6933a-660">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="6933a-660">Az.Profile</span></span>
* <span data-ttu-id="6933a-661">ClientRuntime의 최신 버전을 사용하도록 일반적인 코드를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="6933a-661">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="6933a-662">Connect-AzAccount cmdlet의 매개 변수 TenantId 이름을 Tenant로 바꾸고 TenantId의 별칭을 추가합니다</span><span class="sxs-lookup"><span data-stu-id="6933a-662">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="6933a-663">Connect-AzAccount의 업데이트된 TenantId 설명</span><span class="sxs-lookup"><span data-stu-id="6933a-663">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="6933a-664">테넌트 도메인을 제공할 때 실패한 로그인에 대한 오류 메시지 수정</span><span class="sxs-lookup"><span data-stu-id="6933a-664">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="6933a-665">테넌트에 구독이 없는 계정의 컨텍스트 이름 충돌 문제 수정</span><span class="sxs-lookup"><span data-stu-id="6933a-665">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="6933a-666">MSI를 사용할 때 DataLake 엔드포인트 문제 수정</span><span class="sxs-lookup"><span data-stu-id="6933a-666">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="6933a-667">연결되지 않은 경우 'Disconnect-AzAccount'가 throw하는 문제 수정</span><span class="sxs-lookup"><span data-stu-id="6933a-667">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="6933a-668">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="6933a-668">Az.CognitiveServices</span></span>
* <span data-ttu-id="6933a-669">Get-AzCognitiveServicesAccountSkus 작업을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="6933a-669">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6933a-670">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6933a-670">Az.Compute</span></span>
* <span data-ttu-id="6933a-671">Add-AzVmssVMDataDisk 및 Remove-AzVmssVMDataDisk cmdlet를 추가합니다</span><span class="sxs-lookup"><span data-stu-id="6933a-671">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="6933a-672">Get-AzVMImage는 AutomaticOSUpgradeProperties를 표시합니다</span><span class="sxs-lookup"><span data-stu-id="6933a-672">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="6933a-673">수정된 SetAzVMChefExtension -BootstrapOptions 및 -JsonAttribute option 값이 json 형식으로 설정하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6933a-673">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="6933a-674">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="6933a-674">Az.DataLakeStore</span></span>
* <span data-ttu-id="6933a-675">DataLake 패키지를 1.1.10으로 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="6933a-675">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="6933a-676">기본 동시성을 다중 스레드 작업에 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="6933a-676">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="6933a-677">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="6933a-677">Az.Insights</span></span>
* <span data-ttu-id="6933a-678">해결된 문제 #7267(자동 크기 조정 영역)</span><span class="sxs-lookup"><span data-stu-id="6933a-678">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="6933a-679">열거된 매개 변수를 제대로 설정하지 않은 새 자동 크기 조정 규칙을 만드는 데 문제가 있습니다(이를 항상 기본값으로 설정함).</span><span class="sxs-lookup"><span data-stu-id="6933a-679">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="6933a-680">해결된 문제 # 7513[자세한 정보] Set-AzDiagnosticSetting은 설정을 생성하는 동안 범주를 명시적으로 지정해야 합니다</span><span class="sxs-lookup"><span data-stu-id="6933a-680">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="6933a-681">이제 cmdlet은 생성 중에 사용할 범주를 명시적으로 표시할 필요가 없습니다. 즉, 문서화된대로 작동합니다</span><span class="sxs-lookup"><span data-stu-id="6933a-681">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6933a-682">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6933a-682">Az.Network</span></span>
* <span data-ttu-id="6933a-683">다음 cmdlet에 대해 PeeringType을 필수 매개 변수로 변경했습니다.</span><span class="sxs-lookup"><span data-stu-id="6933a-683">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="6933a-684">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="6933a-684">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="6933a-685">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="6933a-685">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="6933a-686">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="6933a-686">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="6933a-687">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="6933a-687">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="6933a-688">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="6933a-688">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="6933a-689">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="6933a-689">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="6933a-690">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="6933a-690">Az.PolicyInsights</span></span>
* <span data-ttu-id="6933a-691">추가된 정책 재구성 cmdlet</span><span class="sxs-lookup"><span data-stu-id="6933a-691">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="6933a-692">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6933a-692">Az.Resources</span></span>
* <span data-ttu-id="6933a-693">https://github.com/Azure/azure-powershell/issues/7402 에 대한 수정</span><span class="sxs-lookup"><span data-stu-id="6933a-693">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="6933a-694">'Get-AzResource'에 대해 '-ResourceId' 매개 변수를 사용하여 리소스 나열 허용</span><span class="sxs-lookup"><span data-stu-id="6933a-694">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="6933a-695">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="6933a-695">Az.ServiceBus</span></span>
* <span data-ttu-id="6933a-696">마이그레이션 상태를 알 수 있도록 PSServiceBusMigrationConfigurationAttributes에 MigrationState 읽기 전용 속성 추가.</span><span class="sxs-lookup"><span data-stu-id="6933a-696">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="6933a-697">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="6933a-697">Az.ServiceFabric</span></span>
* <span data-ttu-id="6933a-698">Linux Vmss에 인증서 추가 수정.</span><span class="sxs-lookup"><span data-stu-id="6933a-698">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="6933a-699">Add-AzServiceFabricClusterCertificate 수정</span><span class="sxs-lookup"><span data-stu-id="6933a-699">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="6933a-700">새 인증서(Azure/service-fabric-issues#932)에서 올바른 지문을 사용.</span><span class="sxs-lookup"><span data-stu-id="6933a-700">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="6933a-701">올바르게 예외 표시(Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="6933a-701">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="6933a-702">Vmss CreateOrUpdate 작업을 시작하기 전에 'Update-AzServiceFabricDurability'를 수정하여 클러스터 구성 업데이트.</span><span class="sxs-lookup"><span data-stu-id="6933a-702">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="6933a-703">0.4.0 - 2018년 10월</span><span class="sxs-lookup"><span data-stu-id="6933a-703">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="6933a-704">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="6933a-704">Az.Profile</span></span>
* <span data-ttu-id="6933a-705">CloudShell에서 Get-AzSubscription을 사용하여 문제를 해결합니다.</span><span class="sxs-lookup"><span data-stu-id="6933a-705">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="6933a-706">ClientRuntime의 최신 버전을 사용하도록 일반적인 코드를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="6933a-706">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6933a-707">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6933a-707">Az.Compute</span></span>
* <span data-ttu-id="6933a-708">'New-AzVm'에 대해 간단한 매개 변수를 사용하는 경우 가속화된 네트워킹을 설정하기 위해 새 크기가 VM 크기의 허용 목록에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6933a-708">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="6933a-709">모든 cmdlet에 ResourceName 인수 완성자가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6933a-709">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="6933a-710">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="6933a-710">Az.DataLakeStore</span></span>
* <span data-ttu-id="6933a-711">Virtual Network 규칙에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="6933a-711">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="6933a-712">Get-AzDataLakeStoreVirtualNetworkRule: Azure Data Lake Store 가상 네트워크 규칙을 가져오거나 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="6933a-712">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="6933a-713">Add-AzDataLakeStoreVirtualNetworkRule: 지정된 Data Lake Store 계정에 가상 네트워크 규칙을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="6933a-713">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="6933a-714">Set-AzDataLakeStoreVirtualNetworkRule: 지정된 Data Lake Store 계정에 지정된 가상 네트워크 규칙을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="6933a-714">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="6933a-715">Remove-AzDataLakeStoreVirtualNetworkRule: Azure Data Lake Store 가상 네트워크 규칙을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="6933a-715">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6933a-716">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6933a-716">Az.Network</span></span>
* <span data-ttu-id="6933a-717">Test-AzNetworkWatcherConnectivity cmdlet을 업데이트하고, 백 엔드에 프로토콜 값을 전달합니다.</span><span class="sxs-lookup"><span data-stu-id="6933a-717">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="6933a-718">모든 cmdlet에 ResourceName 인수 완성자가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6933a-718">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="6933a-719">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6933a-719">Az.Resources</span></span>
* <span data-ttu-id="6933a-720">(기본 프로필에 구독이 없고 범위가 지정되지 않은 경우) 시나리오에서 의미 있는 예외를 추가하여 Get-AzRoleDefinition이 인식할 수 없는 예외를 throw하는 문제를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="6933a-720">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="6933a-721">또한 기본 매개 변수 집합을 'RoleDefinitionNameParameterSet'으로 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="6933a-721">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="6933a-722">0.3.0 - 2018년 10월</span><span class="sxs-lookup"><span data-stu-id="6933a-722">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="6933a-723">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="6933a-723">Azure.Storage</span></span>
* <span data-ttu-id="6933a-724">대상에 메타데이터가 있을 때 Blob/파일이 메타 데이터를 복사하지 않는 문제 수정</span><span class="sxs-lookup"><span data-stu-id="6933a-724">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="6933a-725">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="6933a-725">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="6933a-726">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="6933a-726">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="6933a-727">특정 위치의 스토리지 리소스 사용을 지원하고 글로벌 스토리지 리소스 사용 가져오기는 더 이상 사용되지 않는다는 경고 메시지를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="6933a-727">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="6933a-728">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="6933a-728">Get-AzStorageUsage</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="6933a-729">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="6933a-729">Az.CognitiveServices</span></span>
* <span data-ttu-id="6933a-730">기존 계정이 없는 Get-AzCognitiveServicesAccountSkus를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="6933a-730">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6933a-731">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6933a-731">Az.Compute</span></span>
* <span data-ttu-id="6933a-732">Get-AzVM -ResourceGroupName <rg>가 필요한 경우 50개가 넘는 결과를 반환하도록 수정</span><span class="sxs-lookup"><span data-stu-id="6933a-732">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="6933a-733">'SimpleParameterSet' 예제가 New-AzVmss cmdlet 도움말에 추가됨</span><span class="sxs-lookup"><span data-stu-id="6933a-733">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="6933a-734">Azure Disk Encryption 진행률 메시지의 오타를 수정</span><span class="sxs-lookup"><span data-stu-id="6933a-734">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="6933a-735">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="6933a-735">Az.DataFactoryV2</span></span>
* <span data-ttu-id="6933a-736">ADF.Net SDK 버전을 2.3.0으로 업데이트</span><span class="sxs-lookup"><span data-stu-id="6933a-736">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6933a-737">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6933a-737">Az.Network</span></span>
* <span data-ttu-id="6933a-738">NetworkProfile 기능 추가</span><span class="sxs-lookup"><span data-stu-id="6933a-738">Added NetworkProfile functionality.</span></span> <span data-ttu-id="6933a-739">추가된 새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="6933a-739">new cmdlets added</span></span>
    - <span data-ttu-id="6933a-740">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="6933a-740">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="6933a-741">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="6933a-741">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="6933a-742">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="6933a-742">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="6933a-743">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="6933a-743">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="6933a-744">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="6933a-744">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="6933a-745">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="6933a-745">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="6933a-746">서브넷 모델에 서비스 연결 링크 추가</span><span class="sxs-lookup"><span data-stu-id="6933a-746">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="6933a-747">New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="6933a-747">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="6933a-748">Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="6933a-748">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="6933a-749">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="6933a-749">Az.RedisCache</span></span>
* <span data-ttu-id="6933a-750">모든 문자열을 Size 매개 변수로 진행되도록 허용</span><span class="sxs-lookup"><span data-stu-id="6933a-750">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="6933a-751">PSArgumentCompleter 팝업에 P5 추가</span><span class="sxs-lookup"><span data-stu-id="6933a-751">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="6933a-752">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6933a-752">Az.Resources</span></span>
* <span data-ttu-id="6933a-753">-Mode 매개 변수를 Set-AzPolicyDefinition에 추가</span><span class="sxs-lookup"><span data-stu-id="6933a-753">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="6933a-754">사용자가 포함된 Origin 작업에서 Get-AzProviderOperation commandlet 버그 수정</span><span class="sxs-lookup"><span data-stu-id="6933a-754">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="6933a-755">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6933a-755">Az.Sql</span></span>
* <span data-ttu-id="6933a-756">일부 백업 cmdlet이 현재 azure 구독을 인식하지 않는 문제 해결</span><span class="sxs-lookup"><span data-stu-id="6933a-756">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="6933a-757">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="6933a-757">Az.Websites</span></span>
* <span data-ttu-id="6933a-758">새 cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - 컨테이너 지속적인 배포 Webhook URL을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6933a-758">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="6933a-759">새 cmdlet New-AzWebAppContainerPSSession 및 Enter-WebAppContainerPSSession -  windows 컨테이너 앱에 PowerShell 원격 세션을 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="6933a-759">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="6933a-760">0.2.0 - 2018년 9월</span><span class="sxs-lookup"><span data-stu-id="6933a-760">0.2.0 - September 2018</span></span>
 <span data-ttu-id="6933a-761">초기 릴리스</span><span class="sxs-lookup"><span data-stu-id="6933a-761">Initial Release</span></span>
