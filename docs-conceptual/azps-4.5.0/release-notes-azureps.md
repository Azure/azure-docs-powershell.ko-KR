---
title: Azure PowerShell 릴리스 정보
description: Azure PowerShell 모듈의 모든 최신 업데이트에 대해 알아봅니다.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/10/2020
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: 86413b426db1b17349c6256f9c70f542c6a62a2f
ms.sourcegitcommit: 8b3126b5c79f453464d90669f0046ba86b7a3424
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/01/2020
ms.locfileid: "89242294"
---
# <a name="azure-powershell-release-notes"></a><span data-ttu-id="73f1f-103">Azure PowerShell 릴리스 정보</span><span class="sxs-lookup"><span data-stu-id="73f1f-103">Azure PowerShell release notes</span></span>

## <a name="450---august-2020"></a><span data-ttu-id="73f1f-104">4.5.0 - 2020년 8월</span><span class="sxs-lookup"><span data-stu-id="73f1f-104">4.5.0 - August 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="73f1f-105">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="73f1f-105">Az.Accounts</span></span>
* <span data-ttu-id="73f1f-106">매개 변수 'MaxContextPopulation'을 허용하도록 'Connect-AzAccount' 업데이트됨 [# 9865]</span><span class="sxs-lookup"><span data-stu-id="73f1f-106">Updated 'Connect-AzAccount' to accept parameter 'MaxContextPopulation' [#9865]</span></span>
* <span data-ttu-id="73f1f-107">SubscriptionClient 버전이 2019-06-01로 업데이트되고 테넌트 도메인을 표시 [#9838]</span><span class="sxs-lookup"><span data-stu-id="73f1f-107">Updated SubscriptionClient version to 2019-06-01 and display tenant domains [#9838]</span></span>
* <span data-ttu-id="73f1f-108">구독의 managedBy 테넌트 정보 및 홈 테넌트 지원</span><span class="sxs-lookup"><span data-stu-id="73f1f-108">Supported home tenant and managedBy tenant information of subscription</span></span>
* <span data-ttu-id="73f1f-109">원격 분석 데이터의 모듈 이름, 버전 정보 수정</span><span class="sxs-lookup"><span data-stu-id="73f1f-109">Corrected module name, version info in telemetry data</span></span>
* <span data-ttu-id="73f1f-110">환경 메타데이터 엔드포인트가 호환되지 않는 값을 반환하는 경우 SqlDatabaseDnsSuffix 및 ServiceManagementUrl이 조정됨</span><span class="sxs-lookup"><span data-stu-id="73f1f-110">Adjusted SqlDatabaseDnsSuffix and ServiceManagementUrl if environment metadata endpoint returns incompatible value</span></span>

#### <a name="azaks"></a><span data-ttu-id="73f1f-111">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="73f1f-111">Az.Aks</span></span>
* <span data-ttu-id="73f1f-112">'ClientIdAndSecret'을 'ServicePrincipalIdAndSecret'으로 제거하고 'ClientIdAndSecret'을 별칭으로 설정함 [#12381]</span><span class="sxs-lookup"><span data-stu-id="73f1f-112">Removed 'ClientIdAndSecret' to 'ServicePrincipalIdAndSecret' and set 'ClientIdAndSecret' as an alias [#12381].</span></span>
* <span data-ttu-id="73f1f-113">'Get-AzAks'/'New-AzAks'/'Remove-AzAks'/'Set-AzAks'를 'Get-AzAksCluster'/'New-AzAksCluster'/'Remove-AzAksCluster'/'Set-AzAksCluster'로 제거하고 원본을 별칭으로 설정함 [#12373].</span><span class="sxs-lookup"><span data-stu-id="73f1f-113">Removed 'Get-AzAks'/'New-AzAks'/'Remove-AzAks'/'Set-AzAks' to 'Get-AzAksCluster'/'New-AzAksCluster'/'Remove-AzAksCluster'/'Set-AzAksCluster' and set the original ones as alias [#12373].</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="73f1f-114">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="73f1f-114">Az.ApiManagement</span></span>
* <span data-ttu-id="73f1f-115">새 'Add-AzApiManagementApiToGateway' cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-115">Added new 'Add-AzApiManagementApiToGateway' cmdlet.</span></span>
* <span data-ttu-id="73f1f-116">새 'Get-AzApiManagementGateway' cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-116">Added new 'Get-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="73f1f-117">새 'Get-AzApiManagementGatewayHostnameConfiguration' cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-117">Added new 'Get-AzApiManagementGatewayHostnameConfiguration' cmdlet.</span></span>
* <span data-ttu-id="73f1f-118">새 'Get-AzApiManagementGatewayKey' cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-118">Added new 'Get-AzApiManagementGatewayKey' cmdlet.</span></span>
* <span data-ttu-id="73f1f-119">새 'New-AzApiManagementGateway' cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-119">Added new 'New-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="73f1f-120">새 'New-AzApiManagementGatewayHostnameConfiguration' cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-120">Added new 'New-AzApiManagementGatewayHostnameConfiguration' cmdlet.</span></span>
* <span data-ttu-id="73f1f-121">새 'New-AzApiManagementResourceLocationObject' cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-121">Added new 'New-AzApiManagementResourceLocationObject' cmdlet.</span></span>
* <span data-ttu-id="73f1f-122">새 'Remove-AzApiManagementApiFromGateway' cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-122">Added new 'Remove-AzApiManagementApiFromGateway' cmdlet.</span></span>
* <span data-ttu-id="73f1f-123">새 'Remove-AzApiManagementGateway' cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-123">Added new 'Remove-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="73f1f-124">새 'Remove-AzApiManagementGatewayHostnameConfiguration' cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-124">Added new 'Remove-AzApiManagementGatewayHostnameConfiguration' cmdlet.</span></span>
* <span data-ttu-id="73f1f-125">새 'Update-AzApiManagementGateway' cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-125">Added new 'Update-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="73f1f-126">'Get-AzApiManagementApi' cmdlet에 선택적 [-GatewayId] 매개 변수가 새로 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-126">Added new optional [-GatewayId] parameter to the 'Get-AzApiManagementApi' cmdlet.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="73f1f-127">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="73f1f-127">Az.CognitiveServices</span></span>
* <span data-ttu-id="73f1f-128">'Deny'가 특히 NetworkRules 기본 작업으로 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-128">Used 'Deny' specifically as NetworkRules default action.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="73f1f-129">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="73f1f-129">Az.FrontDoor</span></span>
* <span data-ttu-id="73f1f-130">Enum.Parse가 null 값을 Enabled 또는 Disabled 열거형 값으로 강제 변환하려는 경우 예외가 throw되는 문제를 수정했습니다. [#12344]</span><span class="sxs-lookup"><span data-stu-id="73f1f-130">Fixed an issue where an exception is being thrown when Enum.Parse tries to coerce a null value to an Enabled or Disabled enum values [#12344]</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="73f1f-131">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="73f1f-131">Az.HDInsight</span></span>
* <span data-ttu-id="73f1f-132">전송 중 암호화 기능을 사용하여 클러스터를 만드는 것이 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-132">Supported creating cluster with encryption in transit feature.</span></span>
    - <span data-ttu-id="73f1f-133">cmdlet 'New-AzHDInsightCluster'에 새 매개 변수 'EncryptionInTransit' 추가</span><span class="sxs-lookup"><span data-stu-id="73f1f-133">Add new parameter 'EncryptionInTransit' to the cmdlet 'New-AzHDInsightCluster'</span></span>
    - <span data-ttu-id="73f1f-134">cmdlet 'New-AzHDInsightClusterConfig'에 새 매개 변수 'EncryptionInTransit' 추가</span><span class="sxs-lookup"><span data-stu-id="73f1f-134">Add new parameter 'EncryptionInTransit' to the cmdlet 'New-AzHDInsightClusterConfig'</span></span>
* <span data-ttu-id="73f1f-135">프라이빗 링크 기능을 사용하여 클러스터를 만드는 것이 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-135">Supported creating cluster with private link feature:</span></span>
    - <span data-ttu-id="73f1f-136">cmdlet 'New-AzHDInsightCluster'에 새 매개 변수 'PublicNetworkAccessType' 및 'OutboundPublicNetworkAccessType' 추가</span><span class="sxs-lookup"><span data-stu-id="73f1f-136">Add new parameter 'PublicNetworkAccessType' and 'OutboundPublicNetworkAccessType' to the cmdlet 'New-AzHDInsightCluster'</span></span>
    - <span data-ttu-id="73f1f-137">cmdlet 'New-AzHDInsightClusterConfig'에 새 매개 변수 'PublicNetworkAccessType' 및 'OutboundPublicNetworkAccessType' 추가</span><span class="sxs-lookup"><span data-stu-id="73f1f-137">Add new parameter 'PublicNetworkAccessType' and 'OutboundPublicNetworkAccessType' to the cmdlet 'New-AzHDInsightClusterConfig'</span></span>
* <span data-ttu-id="73f1f-138">'New-AzHDInsightCluster' 또는 'Get-AzHDInsightCluster'를 호출하는 경우 가상 네트워크 정보가 반환됨</span><span class="sxs-lookup"><span data-stu-id="73f1f-138">Returned virtual network information when calling 'New-AzHDInsightCluster' or 'Get-AzHDInsightCluster'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="73f1f-139">Az.Network</span><span class="sxs-lookup"><span data-stu-id="73f1f-139">Az.Network</span></span>
* <span data-ttu-id="73f1f-140">'Remove-AzExpressRouteCircuitConnectionConfig'에 AddressPrefixType 매개 변수 지원 추가</span><span class="sxs-lookup"><span data-stu-id="73f1f-140">Added support for AddressPrefixType parameter to 'Remove-AzExpressRouteCircuitConnectionConfig'</span></span>
* <span data-ttu-id="73f1f-141">작업을 중단하지 않는 변경이 추가됨: 'Remove-AzExpressRouteCircutPeeringConfig'의 프라이빗 피어링을 위한 PeerAddressType 기능</span><span class="sxs-lookup"><span data-stu-id="73f1f-141">Added non-breaking changes: PeerAddressType functionality for Private Peering in 'Remove-AzExpressRouteCircutPeeringConfig'.</span></span>
* <span data-ttu-id="73f1f-142">AddressPrefixType 및 PeerAddressType 매개 변수의 대/소문자를 무시하도록 코드가 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-142">Code changed to ignore case for AddressPrefixType and PeerAddressType parameter.</span></span>
* <span data-ttu-id="73f1f-143">'New-AzLoadBalancerFrontendIpConfig', 'New-AzPublicIpAddress' 및 'New-AzPublicIpPrefix'에 대한 경고 메시지를 수정했습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-143">Modified the warning message for 'New-AzLoadBalancerFrontendIpConfig', 'New-AzPublicIpAddress' and 'New-AzPublicIpPrefix'.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="73f1f-144">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="73f1f-144">Az.OperationalInsights</span></span>
* <span data-ttu-id="73f1f-145">'Remove-AzOperationalInsightsworkspace'에 대한 '-ForceDelete' 옵션이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-145">Added '-ForceDelete' option for 'Remove-AzOperationalInsightsworkspace'</span></span>
* <span data-ttu-id="73f1f-146">새 cmdlet 'Get-AzOperationalInsightsDeletedWorkspace'가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-146">Added new cmdlet 'Get-AzOperationalInsightsDeletedWorkspace'</span></span>
* <span data-ttu-id="73f1f-147">새 cmdlet 'Restore-AzOperationalInsightsWorkspace'가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-147">Added new cmdlet 'Restore-AzOperationalInsightsWorkspace'</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="73f1f-148">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="73f1f-148">Az.RecoveryServices</span></span>
* <span data-ttu-id="73f1f-149">Azure Backup 컨테이너/항목 검색 환경이 개선되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-149">Improved the Azure Backup container/item discovery experience.</span></span>

#### <a name="azresources"></a><span data-ttu-id="73f1f-150">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="73f1f-150">Az.Resources</span></span>
* <span data-ttu-id="73f1f-151">'New-AzRoleAssignment'에 'Condition', 'ConditionVersion' 및 'Description' 속성을 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-151">Added properties 'Condition', 'ConditionVersion' and 'Description' to 'New-AzRoleAssignment'</span></span>
    - <span data-ttu-id="73f1f-152">여기에는 데이터 모델과 관련된 모든 변경 사항이 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-152">This included all the relevant changes to the data models</span></span>

#### <a name="azsql"></a><span data-ttu-id="73f1f-153">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="73f1f-153">Az.Sql</span></span>
* <span data-ttu-id="73f1f-154">'New-AzSqlServer' 'Set-AzSqlServer'에서 서버 이름 대/소문자를 구분하지 않는 잠재적인 오류를 수정했습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-154">Fixed potential server name case insensitive error in 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>
* <span data-ttu-id="73f1f-155">'New-AzSqlDatabaseSecondary'의 기존 데이터베이스 오류에서 반환되는 잘못된 데이터베이스 이름을 수정했습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-155">Fixed wrong database name returned on existing database error in 'New-AzSqlDatabaseSecondary'</span></span>

#### <a name="azstorage"></a><span data-ttu-id="73f1f-156">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="73f1f-156">Az.Storage</span></span>
* <span data-ttu-id="73f1f-157">새 권한 x,t를 사용하여 컨테이너/blob Sas 토큰 만들기 지원</span><span class="sxs-lookup"><span data-stu-id="73f1f-157">Supported create container/blob Sas token with new permission x,t</span></span>
    -  <span data-ttu-id="73f1f-158">'New-AzStorageBlobSASToken'</span><span class="sxs-lookup"><span data-stu-id="73f1f-158">'New-AzStorageBlobSASToken'</span></span>
    -  <span data-ttu-id="73f1f-159">'New-AzStorageContainerSASToken'</span><span class="sxs-lookup"><span data-stu-id="73f1f-159">'New-AzStorageContainerSASToken'</span></span>
* <span data-ttu-id="73f1f-160">새 권한 x,t,f를 사용하여 계정 Sas 토큰 만들기 지원</span><span class="sxs-lookup"><span data-stu-id="73f1f-160">Supported create account Sas token with new permission x,t,f</span></span>
    -  <span data-ttu-id="73f1f-161">'New-AzStorageAccountSASToken'</span><span class="sxs-lookup"><span data-stu-id="73f1f-161">'New-AzStorageAccountSASToken'</span></span>
* <span data-ttu-id="73f1f-162">단일 파일 사용량 공유 가져오기 지원</span><span class="sxs-lookup"><span data-stu-id="73f1f-162">Supported get single file share usage</span></span>
    - <span data-ttu-id="73f1f-163">'Get-AzRmStorageShare'</span><span class="sxs-lookup"><span data-stu-id="73f1f-163">'Get-AzRmStorageShare'</span></span>

## <a name="440---july-2020"></a><span data-ttu-id="73f1f-164">4.4.0 - 2020년 7월</span><span class="sxs-lookup"><span data-stu-id="73f1f-164">4.4.0 - July 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="73f1f-165">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="73f1f-165">Az.Accounts</span></span>
* <span data-ttu-id="73f1f-166">새 cmdlet 'Invoke-AzRestMethod' 추가</span><span class="sxs-lookup"><span data-stu-id="73f1f-166">Added new cmdlet 'Invoke-AzRestMethod'</span></span>
* <span data-ttu-id="73f1f-167">'Start-Job'을 사용하여 여러 Azure PowerShell cmdlet을 실행하는 등 다중 프로세스 시나리오에서 인증 오류를 발생시킬 수 있는 문제 해결 [#9448]</span><span class="sxs-lookup"><span data-stu-id="73f1f-167">Fixed an issue that may cause authentication errors in multi-process scenarios such as running multiple Azure PowerShell cmdlets using 'Start-Job' [#9448]</span></span>

#### <a name="azaks"></a><span data-ttu-id="73f1f-168">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="73f1f-168">Az.Aks</span></span>
* <span data-ttu-id="73f1f-169">'Get-AzAks'가 모든 클러스터를 가져오지 않는 버그 수정 [#12296]</span><span class="sxs-lookup"><span data-stu-id="73f1f-169">Fixed bug 'Get-AzAks' doesn't get all clusters [#12296]</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="73f1f-170">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="73f1f-170">Az.AnalysisServices</span></span>
* <span data-ttu-id="73f1f-171">인증에 대한 프로젝트 참조 제거</span><span class="sxs-lookup"><span data-stu-id="73f1f-171">Removed project reference to Authentication</span></span>

#### <a name="azautomation"></a><span data-ttu-id="73f1f-172">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="73f1f-172">Az.Automation</span></span>
* <span data-ttu-id="73f1f-173">이스케이프 문자를 포함하는 문자열을 json 개체로 변환할 수 없는 문제 해결</span><span class="sxs-lookup"><span data-stu-id="73f1f-173">Fixed the issue that string with escape chars cannot be converted into json object.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="73f1f-174">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="73f1f-174">Az.Compute</span></span>
* <span data-ttu-id="73f1f-175">'latest' 이미지 버전이 없는 'New-AzVmss'를 사용하는 경우 경고 추가</span><span class="sxs-lookup"><span data-stu-id="73f1f-175">Added warning when using 'New-AzVmss' without 'latest' image version</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="73f1f-176">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="73f1f-176">Az.DataFactory</span></span>
* <span data-ttu-id="73f1f-177">Data Factory에 대한 전역 매개 변수를 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-177">Added global parameters to Data Factory.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="73f1f-178">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="73f1f-178">Az.EventGrid</span></span>
* <span data-ttu-id="73f1f-179">2020-06-01 API 버전을 사용하도록 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-179">Updated to use the 2020-06-01 API version.</span></span>
* <span data-ttu-id="73f1f-180">추가된 새로운 기능:</span><span class="sxs-lookup"><span data-stu-id="73f1f-180">Added new features:</span></span>
    - <span data-ttu-id="73f1f-181">입력 매핑</span><span class="sxs-lookup"><span data-stu-id="73f1f-181">Input mapping</span></span>
    - <span data-ttu-id="73f1f-182">이벤트 배달 스키마</span><span class="sxs-lookup"><span data-stu-id="73f1f-182">Event Delivery Schema</span></span>
    - <span data-ttu-id="73f1f-183">Private Link</span><span class="sxs-lookup"><span data-stu-id="73f1f-183">Private Link</span></span>
    - <span data-ttu-id="73f1f-184">클라우드 이벤트 V10 스키마</span><span class="sxs-lookup"><span data-stu-id="73f1f-184">Cloud Event V10 Schema</span></span>
    - <span data-ttu-id="73f1f-185">대상으로 Service Bus 항목</span><span class="sxs-lookup"><span data-stu-id="73f1f-185">Service Bus Topic As Destination</span></span>
    - <span data-ttu-id="73f1f-186">대상으로 Azure 함수</span><span class="sxs-lookup"><span data-stu-id="73f1f-186">Azure Function As Destination</span></span>
    - <span data-ttu-id="73f1f-187">WebHook 일괄 처리</span><span class="sxs-lookup"><span data-stu-id="73f1f-187">WebHook Batching</span></span>
    - <span data-ttu-id="73f1f-188">보안 웹후크(AAD 지원)</span><span class="sxs-lookup"><span data-stu-id="73f1f-188">Secure webhook (AAD support)</span></span>
    - <span data-ttu-id="73f1f-189">IpFiltering</span><span class="sxs-lookup"><span data-stu-id="73f1f-189">IpFiltering</span></span>
* <span data-ttu-id="73f1f-190">다음 Cmdlet이 업데이트 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-190">Updated cmdlets:</span></span>
    - <span data-ttu-id="73f1f-191">'New-AzEventGridSubscription'/'Update-AzEventGridSubscription':</span><span class="sxs-lookup"><span data-stu-id="73f1f-191">'New-AzEventGridSubscription'/'Update-AzEventGridSubscription':</span></span>
        - <span data-ttu-id="73f1f-192">웹후크 일괄 처리를 지원하기 위해 새로운 선택적 매개 변수를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-192">Add new optional parameters to support webhook batching.</span></span>
        - <span data-ttu-id="73f1f-193">AAD를 사용하여 보안 웹후크를 지원하는 새로운 선택적 매개 변수를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-193">Add new optional parameters to support secured webhook using AAD.</span></span>
        - <span data-ttu-id="73f1f-194">Azure 함수 및 Service Bus 항목을 새 대상으로 지원하기 위해 EndpointType 매개 변수에 대한 새 열거형을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-194">Add new enum for EndpointType parameter to support azure function and service bus topic as new destinations.</span></span>
        - <span data-ttu-id="73f1f-195">배달 스키마에 대한 새로운 선택적 매개 변수를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-195">Add new optional parameter for delivery schema.</span></span>
    - <span data-ttu-id="73f1f-196">'New-AzEventGridTopic'/'Update-AzEventGridTopic' 및 'New-AzEventGridDomain'/'Update-AzEventGridDomain':</span><span class="sxs-lookup"><span data-stu-id="73f1f-196">'New-AzEventGridTopic'/'Update-AzEventGridTopic' and 'New-AzEventGridDomain'/'Update-AzEventGridDomain':</span></span>
        - <span data-ttu-id="73f1f-197">IpFiltering을 지원하기 위해 새로운 선택적 매개 변수를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-197">Add new optional parameters to support IpFiltering.</span></span>
    - <span data-ttu-id="73f1f-198">'New-AzEventGridTopic'/'New-AzEventGridDomain':</span><span class="sxs-lookup"><span data-stu-id="73f1f-198">'New-AzEventGridTopic'/'New-AzEventGridDomain':</span></span>
        - <span data-ttu-id="73f1f-199">입력 매핑을 지원하기 위해 새로운 선택적 매개 변수를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-199">Add new optional parameters to support Input mapping.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="73f1f-200">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="73f1f-200">Az.FrontDoor</span></span>
* <span data-ttu-id="73f1f-201">API 2020-05-01을 사용하도록 업데이트된 모듈</span><span class="sxs-lookup"><span data-stu-id="73f1f-201">Updated module to use API 2020-05-01</span></span>
* <span data-ttu-id="73f1f-202">Storage, Keyvault 및 Web App Service 리소스에 대한 프라이빗 링크 지원을 추가함</span><span class="sxs-lookup"><span data-stu-id="73f1f-202">Added Private link support for Storage, Keyvault and Web App Service resources</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="73f1f-203">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="73f1f-203">Az.HDInsight</span></span>
* <span data-ttu-id="73f1f-204">국가 클라우드에서 ADLSGen1/2 스토리지로 클러스터를 만드는 것이 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-204">Supported creating cluster with ADLSGen1/2 storage in national clouds.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="73f1f-205">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="73f1f-205">Az.Monitor</span></span>
* <span data-ttu-id="73f1f-206">메트릭 또는 로그가 null인 경우 'Get-AzDiagnosticSetting'에 대한 버그 수정 [#12272]</span><span class="sxs-lookup"><span data-stu-id="73f1f-206">Fixed bug for 'Get-AzDiagnosticSetting' when metrics or logs are null [#12272]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="73f1f-207">Az.Network</span><span class="sxs-lookup"><span data-stu-id="73f1f-207">Az.Network</span></span>
* <span data-ttu-id="73f1f-208">VWan HubVnet 연결의 매개 변수 교환 수정</span><span class="sxs-lookup"><span data-stu-id="73f1f-208">Fixed parameters swap in VWan HubVnet connection</span></span>
* <span data-ttu-id="73f1f-209">Azure Network Virtual Appliance 사이트에 대한 새 cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="73f1f-209">Added new cmdlets for Azure Network Virtual Appliance Sites</span></span>
    - <span data-ttu-id="73f1f-210">'Get-AzVirtualApplianceSite'</span><span class="sxs-lookup"><span data-stu-id="73f1f-210">'Get-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="73f1f-211">'New-AzVirtualApplianceSite'</span><span class="sxs-lookup"><span data-stu-id="73f1f-211">'New-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="73f1f-212">'Remove-AzVirtualApplianceSite'</span><span class="sxs-lookup"><span data-stu-id="73f1f-212">'Remove-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="73f1f-213">'Update-AzVirtualApplianceSite'</span><span class="sxs-lookup"><span data-stu-id="73f1f-213">'Update-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="73f1f-214">'New-AzOffice365PolicyProperty'</span><span class="sxs-lookup"><span data-stu-id="73f1f-214">'New-AzOffice365PolicyProperty'</span></span>
* <span data-ttu-id="73f1f-215">Azure Network Virtual Appliance에 대한 새 cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="73f1f-215">Added new cmdlets for Azure Network Virtual Appliance</span></span>
    - <span data-ttu-id="73f1f-216">'Get-AzNetworkVirtualAppliance'</span><span class="sxs-lookup"><span data-stu-id="73f1f-216">'Get-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="73f1f-217">'New-AzNetworkVirtualAppliance'</span><span class="sxs-lookup"><span data-stu-id="73f1f-217">'New-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="73f1f-218">'Remove-AzNetworkVirtualAppliance'</span><span class="sxs-lookup"><span data-stu-id="73f1f-218">'Remove-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="73f1f-219">'Update-AzNetworkVirtualAppliance'</span><span class="sxs-lookup"><span data-stu-id="73f1f-219">'Update-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="73f1f-220">'Get-AzNetworkVirtualApplianceSku'</span><span class="sxs-lookup"><span data-stu-id="73f1f-220">'Get-AzNetworkVirtualApplianceSku'</span></span>
    - <span data-ttu-id="73f1f-221">'New-AzVirtualApplianceSkuProperty'</span><span class="sxs-lookup"><span data-stu-id="73f1f-221">'New-AzVirtualApplianceSkuProperty'</span></span>
* <span data-ttu-id="73f1f-222">Application Gateway를 Private Link 공통 cmdlet에 온보딩</span><span class="sxs-lookup"><span data-stu-id="73f1f-222">Onboarded Application Gateway to Private Link Common Cmdlets</span></span>
* <span data-ttu-id="73f1f-223">StorageSync를 Private Link 공통 cmdlet에 온보딩</span><span class="sxs-lookup"><span data-stu-id="73f1f-223">Onboarded StorageSync to Private Link Common Cmdlets</span></span>
* <span data-ttu-id="73f1f-224">SignalR을 Private Link 공통 cmdlet에 온보딩</span><span class="sxs-lookup"><span data-stu-id="73f1f-224">Onboarded SignalR to Private Link Common Cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="73f1f-225">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="73f1f-225">Az.RecoveryServices</span></span>
* <span data-ttu-id="73f1f-226">인증에 대한 프로젝트 참조 제거</span><span class="sxs-lookup"><span data-stu-id="73f1f-226">Removed project reference to Authentication</span></span>
* <span data-ttu-id="73f1f-227">Azure Backup 튜닝 cmdlet은 텍스트를 보다 정확하게 작성하는 데 도움이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-227">Azure Backup tuned cmdlets help text to be more accurate.</span></span>
* <span data-ttu-id="73f1f-228">Azure Backup은 'Get-AzRecoveryServicesBackupJob' cmdlet을 사용하여 MAB 에이전트 작업을 가져오는 지원을 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-228">Azure Backup added support for fetching MAB agent jobs using 'Get-AzRecoveryServicesBackupJob' cmdlet.</span></span>

#### <a name="azresources"></a><span data-ttu-id="73f1f-229">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="73f1f-229">Az.Resources</span></span>
* <span data-ttu-id="73f1f-230">SDK를 사용하도록 'Save-AzResourceGroupDeploymentTemplate'을 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-230">Updated 'Save-AzResourceGroupDeploymentTemplate' to use the SDK.</span></span>
* <span data-ttu-id="73f1f-231">'Unregister-AzResourceProvider' cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-231">Added 'Unregister-AzResourceProvider' cmdlet.</span></span>

#### <a name="azsql"></a><span data-ttu-id="73f1f-232">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="73f1f-232">Az.Sql</span></span>
* <span data-ttu-id="73f1f-233">Set-AzSqlInstanceActiveDirectoryAdministrator cmdlet에서 서비스 주체 및 게스트 사용자에 대한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-233">Added support for Service principal and guest users in Set-AzSqlInstanceActiveDirectoryAdministrator cmdlet'</span></span>
* <span data-ttu-id="73f1f-234">데이터 분류 cmdlet의 버그를 수정했습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-234">Fixed a bug in Data Classification cmdlets.'</span></span>
* <span data-ttu-id="73f1f-235">다음의 Azure SQL Managed Instance 장애 조치에 대한 지원 추가: 'Invoke-AzSqlInstanceFailover'</span><span class="sxs-lookup"><span data-stu-id="73f1f-235">Added support for Azure SQL Managed Instance failover: 'Invoke-AzSqlInstanceFailover'</span></span>

#### <a name="azstorage"></a><span data-ttu-id="73f1f-236">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="73f1f-236">Az.Storage</span></span>
* <span data-ttu-id="73f1f-237">일부 데이터 평면 cmdlet에 대해 UserAgent가 추가되지 않는 문제를 해결했습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-237">Fixed the issue that UserAgent is not added for some data plane cmdlets.</span></span>
* <span data-ttu-id="73f1f-238">MinimumTlsVersion 및 AllowBlobPublicAccess로 스토리지 계정 만들기/업데이트 지원</span><span class="sxs-lookup"><span data-stu-id="73f1f-238">Supported create/update Storage account with MinimumTlsVersion and AllowBlobPublicAccess</span></span>
    -  <span data-ttu-id="73f1f-239">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="73f1f-239">'New-AzStorageAccount'</span></span>
    -  <span data-ttu-id="73f1f-240">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="73f1f-240">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="73f1f-241">스토리지 계정의 Blob Service에서 버전 관리 사용/사용 안 함 지원</span><span class="sxs-lookup"><span data-stu-id="73f1f-241">Support enable/disable versioning on Blob Service of a Storage account</span></span>
    - <span data-ttu-id="73f1f-242">'Update-AzStorageBlobServiceProperty'</span><span class="sxs-lookup"><span data-stu-id="73f1f-242">'Update-AzStorageBlobServiceProperty'</span></span>
* <span data-ttu-id="73f1f-243">Blob 버전 관리로 Blob 나열 지원</span><span class="sxs-lookup"><span data-stu-id="73f1f-243">Support list blobs with blob versions</span></span>
    - <span data-ttu-id="73f1f-244">'Get-AzStorageBlob'</span><span class="sxs-lookup"><span data-stu-id="73f1f-244">'Get-AzStorageBlob'</span></span>
* <span data-ttu-id="73f1f-245">단일 Blob 스냅샷 또는 Blob 버전 가져오기/제거 지원</span><span class="sxs-lookup"><span data-stu-id="73f1f-245">Support get/remove single blob snapshot or blob version</span></span>
    - <span data-ttu-id="73f1f-246">'Get-AzStorageBlob'</span><span class="sxs-lookup"><span data-stu-id="73f1f-246">'Get-AzStorageBlob'</span></span>
    - <span data-ttu-id="73f1f-247">'Remove-AzStorageBlob'</span><span class="sxs-lookup"><span data-stu-id="73f1f-247">'Remove-AzStorageBlob'</span></span>
* <span data-ttu-id="73f1f-248">Azure.Storage.Blobs V12에서 생성된 Blob 개체의 파이프라인 지원</span><span class="sxs-lookup"><span data-stu-id="73f1f-248">Support pipeline from blob object generated from Azure.Storage.Blobs V12</span></span>
    - <span data-ttu-id="73f1f-249">'Get-AzStorageBlobContent'</span><span class="sxs-lookup"><span data-stu-id="73f1f-249">'Get-AzStorageBlobContent'</span></span>
    - <span data-ttu-id="73f1f-250">'New-AzStorageBlobSASToken'</span><span class="sxs-lookup"><span data-stu-id="73f1f-250">'New-AzStorageBlobSASToken'</span></span>
    - <span data-ttu-id="73f1f-251">'Remove-AzStorageBlob'</span><span class="sxs-lookup"><span data-stu-id="73f1f-251">'Remove-AzStorageBlob'</span></span>
    - <span data-ttu-id="73f1f-252">'Set-AzStorageBlobContent'</span><span class="sxs-lookup"><span data-stu-id="73f1f-252">'Set-AzStorageBlobContent'</span></span>
    - <span data-ttu-id="73f1f-253">'Start-AzStorageBlobCopy'</span><span class="sxs-lookup"><span data-stu-id="73f1f-253">'Start-AzStorageBlobCopy'</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="73f1f-254">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="73f1f-254">Az.StorageSync</span></span>
* <span data-ttu-id="73f1f-255">ApiVersion 2020-03-01을 대상으로 하는 새 버전의 StorageSync SDK 추가</span><span class="sxs-lookup"><span data-stu-id="73f1f-255">Added a new version StorageSync SDK targeting ApiVersion 2020-03-01</span></span>
* <span data-ttu-id="73f1f-256">스토리지 동기화 서비스 업데이트 cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="73f1f-256">Added Update Storage Sync Service cmdlet</span></span>
    - <span data-ttu-id="73f1f-257">'Set-AzStorageSyncService'</span><span class="sxs-lookup"><span data-stu-id="73f1f-257">'Set-AzStorageSyncService'</span></span>
* <span data-ttu-id="73f1f-258">IncomingTrafficPolicy 및 PrivateEndpointConnections가 StorageSyncService cmdlet에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-258">Added IncomingTrafficPolicy and PrivateEndpointConnections to StorageSyncService cmdlets.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="73f1f-259">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="73f1f-259">Az.Websites</span></span>
* <span data-ttu-id="73f1f-260">App Service 계획과 동일한 리소스 그룹에 속하지 않는 슬롯에 대한 작업을 수행하기 위한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="73f1f-260">Added support to perform operations for Slots not in the same resource group as the App Service Plan</span></span>

## <a name="430---june-2020"></a><span data-ttu-id="73f1f-261">4.3.0 - 2020년 6월</span><span class="sxs-lookup"><span data-stu-id="73f1f-261">4.3.0 - June 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="73f1f-262">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="73f1f-262">Az.Accounts</span></span>
* <span data-ttu-id="73f1f-263">기본적으로 환경 검색 설정이 지원되며 'Add-AzEnvironment'를 통해 환경을 추가할 수 있음</span><span class="sxs-lookup"><span data-stu-id="73f1f-263">Supported discovering environment setting by default and adding environment via 'Add-AzEnvironment'</span></span>
* <span data-ttu-id="73f1f-264">미리 로드된 어셈블리 업데이트 [#12024], [#11976]</span><span class="sxs-lookup"><span data-stu-id="73f1f-264">Update preloaded assemblies [#12024], [#11976]</span></span>
* <span data-ttu-id="73f1f-265">Azure.Core 어셈블리 업데이트</span><span class="sxs-lookup"><span data-stu-id="73f1f-265">Updated Azure.Core assembly</span></span>
* <span data-ttu-id="73f1f-266">다중 스레드 실행에서 'Connect-AzAccount'가 실패할 수 있는 문제 해결 [#11201]</span><span class="sxs-lookup"><span data-stu-id="73f1f-266">Fixed an issue that may cause 'Connect-AzAccount' to fail in multi-threaded execution [#11201]</span></span>

#### <a name="azaks"></a><span data-ttu-id="73f1f-267">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="73f1f-267">Az.Aks</span></span>
* <span data-ttu-id="73f1f-268">이전에 사용하던 [AccessProfile API](https://docs.microsoft.com/rest/api/aks/managedclusters/getaccessprofile)를 [ListClusterAdmin](https://docs.microsoft.com/rest/api/aks/managedclusters/listclusteradmincredentials) 및 [ListClusterUser](https://docs.microsoft.com/rest/api/aks/managedclusters/listclusterusercredentials) API 호출로 대체</span><span class="sxs-lookup"><span data-stu-id="73f1f-268">Replaced usage of old [AccessProfile API](https://docs.microsoft.com/rest/api/aks/managedclusters/getaccessprofile) with calls to [ListClusterAdmin](https://docs.microsoft.com/rest/api/aks/managedclusters/listclusteradmincredentials) and [ListClusterUser](https://docs.microsoft.com/rest/api/aks/managedclusters/listclusterusercredentials) APIs</span></span>

#### <a name="azbatch"></a><span data-ttu-id="73f1f-269">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="73f1f-269">Az.Batch</span></span>
* <span data-ttu-id="73f1f-270">'Microsoft.Azure.Management.Batch' SDK 버전 11.0.0을 사용하도록 Az.Batch 업데이트</span><span class="sxs-lookup"><span data-stu-id="73f1f-270">Updated Az.Batch to use 'Microsoft.Azure.Management.Batch' SDK version to 11.0.0</span></span>
* <span data-ttu-id="73f1f-271">'New-AzBatchAccount' cmdlet에서 BatchAccount ID를 설정하는 기능 추가</span><span class="sxs-lookup"><span data-stu-id="73f1f-271">Added the ability to set the BatchAccount Identity in the 'New-AzBatchAccount' cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="73f1f-272">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="73f1f-272">Az.CognitiveServices</span></span>
* <span data-ttu-id="73f1f-273">계정 기능 표시 지원</span><span class="sxs-lookup"><span data-stu-id="73f1f-273">Supported displaying account capabilities.</span></span>
* <span data-ttu-id="73f1f-274">PublicNetworkAccess 수정 지원</span><span class="sxs-lookup"><span data-stu-id="73f1f-274">Supported modifying PublicNetworkAccess.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="73f1f-275">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="73f1f-275">Az.Compute</span></span>
* <span data-ttu-id="73f1f-276">Set-AzVM 및 Set-AzVmssVM cmdlet에 SimulateEviction 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="73f1f-276">Added SimulateEviction parameter to Set-AzVM and Set-AzVmssVM cmdlets.</span></span>
* <span data-ttu-id="73f1f-277">AzGalleryImageVersion cmdlet에 대한 StorageAccountType 매개 변수의 인수 완성자에 'Premium_LRS' 추가</span><span class="sxs-lookup"><span data-stu-id="73f1f-277">Added 'Premium_LRS' to the argument completer of StorageAccountType parameter for New-AzGalleryImageVersion cmdlet.</span></span>
* <span data-ttu-id="73f1f-278">VMCustomScriptExtension에 Substatuses 추가 [#11297]</span><span class="sxs-lookup"><span data-stu-id="73f1f-278">Added Substatuses to VMCustomScriptExtension [#11297]</span></span>
* <span data-ttu-id="73f1f-279">New-AzVM 및 New-AzVMConfig cmdlet에 대한 EvictionPolicy 매개 변수의 인수 완성자에 'Delete' 추가</span><span class="sxs-lookup"><span data-stu-id="73f1f-279">Added 'Delete' to the argument completer of EvictionPolicy parameter for New-AzVM and New-AzVMConfig cmdlets.</span></span>
* <span data-ttu-id="73f1f-280">새 SAP용 VM 확장의 이름 수정</span><span class="sxs-lookup"><span data-stu-id="73f1f-280">Fixed name of new VM Extension for SAP</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="73f1f-281">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="73f1f-281">Az.DataFactory</span></span>
* <span data-ttu-id="73f1f-282">ADF .Net SDK 버전을 4.9.0으로 업데이트</span><span class="sxs-lookup"><span data-stu-id="73f1f-282">Updated ADF .Net SDK version to 4.9.0</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="73f1f-283">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="73f1f-283">Az.EventHub</span></span>
* <span data-ttu-id="73f1f-284">'New-AzEventHubNamespace' 및 'Set-AzEventHubNamespace' cmdlet에 관리 ID 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="73f1f-284">Added Managed Identity parameters to 'New-AzEventHubNamespace' and 'Set-AzEventHubNamespace' cmdlets</span></span>

#### <a name="azfunctions"></a><span data-ttu-id="73f1f-285">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="73f1f-285">Az.Functions</span></span>
* <span data-ttu-id="73f1f-286">PowerShell 7.0 및 Java 11 함수 앱을 만드는 지원 추가</span><span class="sxs-lookup"><span data-stu-id="73f1f-286">Added support to create PowerShell 7.0 and Java 11 function apps</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="73f1f-287">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="73f1f-287">Az.HDInsight</span></span>
* <span data-ttu-id="73f1f-288">호스트를 나열하고 HDInsight 클러스터의 특정 호스트를 다시 시작하는 기능 지원</span><span class="sxs-lookup"><span data-stu-id="73f1f-288">Supported listing hosts and restart specific hosts of the HDInsight cluster.</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="73f1f-289">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="73f1f-289">Az.HealthcareApis</span></span>
* <span data-ttu-id="73f1f-290">SDK 버전을 1.1.0으로 업데이트</span><span class="sxs-lookup"><span data-stu-id="73f1f-290">Updated the SDK version to 1.1.0</span></span>
* <span data-ttu-id="73f1f-291">설정 및 관리 ID 내보내기에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="73f1f-291">Added support for Export settings and Managed Identity</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="73f1f-292">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="73f1f-292">Az.Monitor</span></span>
* <span data-ttu-id="73f1f-293">'Set-AzActivityLogAlert'에 대한 입력 개체 매개 변수 수정</span><span class="sxs-lookup"><span data-stu-id="73f1f-293">Fixed input object parameter for 'Set-AzActivityLogAlert'</span></span>
* <span data-ttu-id="73f1f-294">'Set-AzActionGroup'에 대한 'InputObject' 매개 변수 수정 [#10868]</span><span class="sxs-lookup"><span data-stu-id="73f1f-294">Fixed 'InputObject' parameter for 'Set-AzActionGroup' [#10868]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="73f1f-295">Az.Network</span><span class="sxs-lookup"><span data-stu-id="73f1f-295">Az.Network</span></span>
* <span data-ttu-id="73f1f-296">'Remove-AzExpressRouteCircuitConnectionConfig'에 AddressPrefixType 매개 변수 지원 추가</span><span class="sxs-lookup"><span data-stu-id="73f1f-296">Added support for AddressPrefixType parameter to 'Remove-AzExpressRouteCircuitConnectionConfig'</span></span>
* <span data-ttu-id="73f1f-297">Azure FirewallPolicy에 대한 새 cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="73f1f-297">Added new cmdlets for Azure FirewallPolicy</span></span>
    - <span data-ttu-id="73f1f-298">'New-AzFirewallPolicyDnsSetting'</span><span class="sxs-lookup"><span data-stu-id="73f1f-298">'New-AzFirewallPolicyDnsSetting'</span></span>
    - <span data-ttu-id="73f1f-299">방화벽 정책에 대한 네트워크 규칙에서 대상 FQDN 지원</span><span class="sxs-lookup"><span data-stu-id="73f1f-299">Support for Destination FQDN in Network Rules for Firewall Policy</span></span>
* <span data-ttu-id="73f1f-300">백 엔드 주소 풀 작업에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="73f1f-300">Added support for backend address pool operations</span></span>
    - <span data-ttu-id="73f1f-301">'New-AzLoadBalancerBackendAddressConfig'</span><span class="sxs-lookup"><span data-stu-id="73f1f-301">'New-AzLoadBalancerBackendAddressConfig'</span></span>
    - <span data-ttu-id="73f1f-302">'New-AzLoadBalancerBackendAddressPool'</span><span class="sxs-lookup"><span data-stu-id="73f1f-302">'New-AzLoadBalancerBackendAddressPool'</span></span>
    - <span data-ttu-id="73f1f-303">'Set-AzLoadBalancerBackendAddressPool'</span><span class="sxs-lookup"><span data-stu-id="73f1f-303">'Set-AzLoadBalancerBackendAddressPool'</span></span>
    - <span data-ttu-id="73f1f-304">'Remove-AzLoadBalancerBackendAddressPool'</span><span class="sxs-lookup"><span data-stu-id="73f1f-304">'Remove-AzLoadBalancerBackendAddressPool'</span></span>
    - <span data-ttu-id="73f1f-305">'Get-AzLoadBalancerBackendAddressPool'</span><span class="sxs-lookup"><span data-stu-id="73f1f-305">'Get-AzLoadBalancerBackendAddressPool'</span></span>
* <span data-ttu-id="73f1f-306">'New-AzIpGroup'에 대한 이름 유효성 검사 추가</span><span class="sxs-lookup"><span data-stu-id="73f1f-306">Added name validation for 'New-AzIpGroup'</span></span>
* <span data-ttu-id="73f1f-307">Azure FirewallPolicy에 대한 새 cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="73f1f-307">Added new cmdlets for Azure FirewallPolicy</span></span>
    - <span data-ttu-id="73f1f-308">'New-AzFirewallPolicyThreatIntelWhitelist'</span><span class="sxs-lookup"><span data-stu-id="73f1f-308">'New-AzFirewallPolicyThreatIntelWhitelist'</span></span>
* <span data-ttu-id="73f1f-309">기능에 대한 새로운 명령이 업데이트됨: VirtualWan P2SVpnGateway에서 사용자 지정 dns 서버 설정/제거</span><span class="sxs-lookup"><span data-stu-id="73f1f-309">Updated below commands for feature: Custom dns servers set/remove on VirtualWan P2SVpnGateway.</span></span>
    - <span data-ttu-id="73f1f-310">New-AzP2sVpnGateway 업데이트됨: 고객이 P2SVpnGateway에 설정할 dns 서버를 지정할 수 있는 선택적 매개 변수 '-CustomDnsServer'가 추가되었으며, 이 매개 변수는 지점 및 사이트 간 클라이언트에서 사용 가능</span><span class="sxs-lookup"><span data-stu-id="73f1f-310">Updated New-AzP2sVpnGateway: Added optional parameter '-CustomDnsServer' for customers to specify their dns servers to set on P2SVpnGateway, which can be used by Point to site clients.</span></span>
    - <span data-ttu-id="73f1f-311">Update-AzP2sVpnGateway 업데이트됨: 고객이 P2SVpnGateway에 설정할 dns 서버를 지정할 수 있는 선택적 매개 변수 '-CustomDnsServer'가 추가되었으며, 이 매개 변수는 지점 및 사이트 간 클라이언트에서 사용 가능</span><span class="sxs-lookup"><span data-stu-id="73f1f-311">Updated Update-AzP2sVpnGateway: Added optional parameter '-CustomDnsServer' for customers to specify their dns servers to set on P2SVpnGateway, which can be used by Point to site clients.</span></span>
* <span data-ttu-id="73f1f-312">'Update-AzVpnGateway' 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="73f1f-312">Updated 'Update-AzVpnGateway'</span></span>
    - <span data-ttu-id="73f1f-313">고객이 VpnGateway에 설정할 사용자 지정 bgps를 지정할 수 있도록 선택적 매개 변수 '-BgpPeeringAddress' 추가</span><span class="sxs-lookup"><span data-stu-id="73f1f-313">Added optional parameter '-BgpPeeringAddress' for customers to specify their custom bgps to set on VpnGateway.</span></span>
* <span data-ttu-id="73f1f-314">VirtualHub 리소스의 라우팅 상태 초기화를 지원하는 새 cmdlet 추가:</span><span class="sxs-lookup"><span data-stu-id="73f1f-314">Added new cmdlet to support resetting the routing state of a VirtualHub resource:</span></span>
    - <span data-ttu-id="73f1f-315">'Reset-AzHubRouter'</span><span class="sxs-lookup"><span data-stu-id="73f1f-315">'Reset-AzHubRouter'</span></span>
* <span data-ttu-id="73f1f-316">방화벽 정책에 대한 최근 Swagger 변화에 따라 아래 항목 업데이트</span><span class="sxs-lookup"><span data-stu-id="73f1f-316">Updated below things based on recent swagger change for Firewall Policy</span></span>
    - <span data-ttu-id="73f1f-317">RuleGroup, RuleCollectionGroup 및 RuleType의 이름 변경</span><span class="sxs-lookup"><span data-stu-id="73f1f-317">Changes names for RuleGroup, RuleCollectionGroup and RuleType</span></span>
    - <span data-ttu-id="73f1f-318">여러 NAT 규칙 컬렉션을 지원하도록 방화벽 정책 NAT 규칙 컬렉션에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="73f1f-318">Added support for Firewall Policy NAT Rule Collections to support multiple NAT Rule Collection</span></span>
* <span data-ttu-id="73f1f-319">[호환성이 손상되는 변경] 'New-AzFirewallPolicyApplicationRule' 및 'New-AzFirewallPolicyNetworkRule'에 대한 필수 매개 변수 'SourceIpGroup' 추가</span><span class="sxs-lookup"><span data-stu-id="73f1f-319">[Breaking Change] Added mandatory parameter 'SourceIpGroup' for 'New-AzFirewallPolicyApplicationRule' and 'New-AzFirewallPolicyNetworkRule'.</span></span>
* <span data-ttu-id="73f1f-320">[호환성이 손상되는 변경] 'New-AzFirewallPolicyApplicationRule' 수정, 'SourceAddress' 매개 변수를 필수로 변경</span><span class="sxs-lookup"><span data-stu-id="73f1f-320">[Breaking Change] Fixed 'New-AzFirewallPolicyApplicationRule', parameter 'SourceAddress' to be mandatory.</span></span>
* <span data-ttu-id="73f1f-321">[호환성이 손상되는 변경] 'New-AzFirewallPolicyApplicationRule' 수정, 'SourceAddress' 매개 변수를 필수로 변경</span><span class="sxs-lookup"><span data-stu-id="73f1f-321">[Breaking Change] Fixed 'New-AzFirewallPolicyApplicationRule', parameter 'SourceAddress' to be mandatory.</span></span>
* <span data-ttu-id="73f1f-322">[호환성이 손상되는 변경] 다음 필수 매개 변수 제거: 'New-AzFirewallPolicyNatRuleCollection'의 'TranslatedAddress', 'TranslatedPort'</span><span class="sxs-lookup"><span data-stu-id="73f1f-322">[Breaking Change] Removed mandatory parameters: 'TranslatedAddress', 'TranslatedPort' for 'New-AzFirewallPolicyNatRuleCollection'.</span></span>
* <span data-ttu-id="73f1f-323">PrivateLink On Application Gateway를 지원하는 새 cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="73f1f-323">Added new cmdlets to support PrivateLink On Application Gateway</span></span>
    - <span data-ttu-id="73f1f-324">'New-AzApplicationGatewayPrivateLinkConfiguration'</span><span class="sxs-lookup"><span data-stu-id="73f1f-324">'New-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="73f1f-325">'Get-AzApplicationGatewayPrivateLinkConfiguration'</span><span class="sxs-lookup"><span data-stu-id="73f1f-325">'Get-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="73f1f-326">'New-AzApplicationGatewayPrivateLinkConfiguration'</span><span class="sxs-lookup"><span data-stu-id="73f1f-326">'New-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="73f1f-327">'Set-AzApplicationGatewayPrivateLinkConfiguration'</span><span class="sxs-lookup"><span data-stu-id="73f1f-327">'Set-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="73f1f-328">'Remove-AzApplicationGatewayPrivateLinkConfiguration'</span><span class="sxs-lookup"><span data-stu-id="73f1f-328">'Remove-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="73f1f-329">'New-AzApplicationGatewayPrivateLinkIpConfiguration'</span><span class="sxs-lookup"><span data-stu-id="73f1f-329">'New-AzApplicationGatewayPrivateLinkIpConfiguration'</span></span>
* <span data-ttu-id="73f1f-330">VirtualHub의 HubRouteTables 자식 리소스에 대한 새 cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="73f1f-330">Added new cmdlets for HubRouteTables child resource of VirtualHub.</span></span>
    - <span data-ttu-id="73f1f-331">'New-AzVHubRoute'</span><span class="sxs-lookup"><span data-stu-id="73f1f-331">'New-AzVHubRoute'</span></span>
    - <span data-ttu-id="73f1f-332">'New-AzVHubRouteTable'</span><span class="sxs-lookup"><span data-stu-id="73f1f-332">'New-AzVHubRouteTable'</span></span>
    - <span data-ttu-id="73f1f-333">'Get-AzVHubRouteTable'</span><span class="sxs-lookup"><span data-stu-id="73f1f-333">'Get-AzVHubRouteTable'</span></span>
    - <span data-ttu-id="73f1f-334">'Update-AzVHubRouteTable'</span><span class="sxs-lookup"><span data-stu-id="73f1f-334">'Update-AzVHubRouteTable'</span></span>
    - <span data-ttu-id="73f1f-335">'Remove-AzVHubRouteTable'</span><span class="sxs-lookup"><span data-stu-id="73f1f-335">'Remove-AzVHubRouteTable'</span></span>
* <span data-ttu-id="73f1f-336">VirtualWan의 사용자 지정 라우팅에 대한 선택적 RoutingConfiguration 입력 매개 변수를 지원하도록 기존 cmdlet 업데이트</span><span class="sxs-lookup"><span data-stu-id="73f1f-336">Updated existing cmdlets to support optional RoutingConfiguration input parameter for custom routing in VirtualWan.</span></span>
    - <span data-ttu-id="73f1f-337">'New-AzExpressRouteConnection'</span><span class="sxs-lookup"><span data-stu-id="73f1f-337">'New-AzExpressRouteConnection'</span></span>
    - <span data-ttu-id="73f1f-338">'Set-AzExpressRouteConnection'</span><span class="sxs-lookup"><span data-stu-id="73f1f-338">'Set-AzExpressRouteConnection'</span></span>
    - <span data-ttu-id="73f1f-339">'New-AzVirtualHubVnetConnection'</span><span class="sxs-lookup"><span data-stu-id="73f1f-339">'New-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="73f1f-340">'Update-AzVirtualHubVnetConnection'</span><span class="sxs-lookup"><span data-stu-id="73f1f-340">'Update-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="73f1f-341">'New-AzVpnConnection'</span><span class="sxs-lookup"><span data-stu-id="73f1f-341">'New-AzVpnConnection'</span></span>
    - <span data-ttu-id="73f1f-342">'Update-AzVpnConnection'</span><span class="sxs-lookup"><span data-stu-id="73f1f-342">'Update-AzVpnConnection'</span></span>
    - <span data-ttu-id="73f1f-343">'New-AzP2sVpnGateway'</span><span class="sxs-lookup"><span data-stu-id="73f1f-343">'New-AzP2sVpnGateway'</span></span>
    - <span data-ttu-id="73f1f-344">'Update-AzP2sVpnGateway'</span><span class="sxs-lookup"><span data-stu-id="73f1f-344">'Update-AzP2sVpnGateway'</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="73f1f-345">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="73f1f-345">Az.OperationalInsights</span></span>
* <span data-ttu-id="73f1f-346">PSWorkspace가 IOperationalInsightsWorkspace를 구현하지 않는 버그 수정 [#12135]</span><span class="sxs-lookup"><span data-stu-id="73f1f-346">Fixed bug PSWorkspace doesn't implement IOperationalInsightsWorkspace [#12135]</span></span>
* <span data-ttu-id="73f1f-347">'Set-AzOperationalInsightsWorkspace'에서 'Sku' 매개 변수의 올바른 값 세트에 'pergb2018' 추가</span><span class="sxs-lookup"><span data-stu-id="73f1f-347">Added 'pergb2018' to valid value set of parameter 'Sku' in 'Set-AzOperationalInsightsWorkspace'</span></span> 
* <span data-ttu-id="73f1f-348">매개 변수 'FunctionParameter'에 대한 별칭 'FunctionParameters' 추가</span><span class="sxs-lookup"><span data-stu-id="73f1f-348">Added alias 'FunctionParameters' for parameter 'FunctionParameter' to</span></span>
    - <span data-ttu-id="73f1f-349">'New-AzOperationalInsightsSavedSearch'</span><span class="sxs-lookup"><span data-stu-id="73f1f-349">'New-AzOperationalInsightsSavedSearch'</span></span>
    - <span data-ttu-id="73f1f-350">'Set-AzOperationalInsightsSavedSearch'</span><span class="sxs-lookup"><span data-stu-id="73f1f-350">'Set-AzOperationalInsightsSavedSearch'</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="73f1f-351">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="73f1f-351">Az.RecoveryServices</span></span>
* <span data-ttu-id="73f1f-352">Azure Backup에서 MAB 항목을 가져오기 위한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="73f1f-352">Azure Backup added support for fetching MAB items.</span></span>
* <span data-ttu-id="73f1f-353">Azure Site Recovery에서 'StandardSSD_LRS' 디스크 형식 지원</span><span class="sxs-lookup"><span data-stu-id="73f1f-353">Azure Site Recovery supports disk type 'StandardSSD_LRS'</span></span>

#### <a name="azresources"></a><span data-ttu-id="73f1f-354">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="73f1f-354">Az.Resources</span></span>
* <span data-ttu-id="73f1f-355">'PSADUser'에서 'UsageLocation', 'GivenName', 'Surname', 'AccountEnabled', 'MailNickname', 'Mail' 추가 [#10526] [#10497]</span><span class="sxs-lookup"><span data-stu-id="73f1f-355">Added 'UsageLocation', 'GivenName', 'Surname', 'AccountEnabled', 'MailNickname', 'Mail' on 'PSADUser' [#10526] [#10497]</span></span>
* <span data-ttu-id="73f1f-356">'Get-AzADUser'에서 '-Mail'이 작동하지 않는 문제 해결 [#11981]</span><span class="sxs-lookup"><span data-stu-id="73f1f-356">Fixed issue that '-Mail' doesn't work on 'Get-AzADUser' [#11981]</span></span>
* <span data-ttu-id="73f1f-357">'Get-AzDeploymentWhatIfResult' 및 'Get-AzResourceGroupDeploymentWhatIfResult'에 '-ExcludeChangeType' 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="73f1f-357">Added '-ExcludeChangeType' parameter to 'Get-AzDeploymentWhatIfResult' and 'Get-AzResourceGroupDeploymentWhatIfResult'</span></span>
* <span data-ttu-id="73f1f-358">'New-AzDeployment' 및 'New-AzResourceGroupDeployment'에 '-WhatIfExcludeChangeType' 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="73f1f-358">Added '-WhatIfExcludeChangeType' parameter to 'New-AzDeployment' and 'New-AzResourceGroupDeployment'</span></span>
* <span data-ttu-id="73f1f-359">보다 나은 오류 메시지를 표시하도록 'Test-Az\*Deployment' cmdlet 업데이트</span><span class="sxs-lookup"><span data-stu-id="73f1f-359">Updated 'Test-Az\*Deployment' cmdlets to show better error messages</span></span>
* <span data-ttu-id="73f1f-360">deployment create 및 What-If cmdlet의 '-Name' 매개 변수에 대한 도움말 메시지 수정</span><span class="sxs-lookup"><span data-stu-id="73f1f-360">Fixed help message for '-Name' parameter of deployment create and What-If cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="73f1f-361">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="73f1f-361">Az.Sql</span></span>
* <span data-ttu-id="73f1f-362">Set SQL Server Azure Active Directory Admin cmdlet의 서비스 주체에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="73f1f-362">Added support for service principal for Set SQL Server Azure Active Directory Admin cmdlet</span></span>
* <span data-ttu-id="73f1f-363">데이터 분류 cmdlet의 동기화 문제 해결</span><span class="sxs-lookup"><span data-stu-id="73f1f-363">Fixed sync issue in Data Classification cmdlets.</span></span>
* <span data-ttu-id="73f1f-364">'Set-AzSqlServerActiveDirectoryAdministrator'에서 메일로 사용자 검색 지원 [#12192]</span><span class="sxs-lookup"><span data-stu-id="73f1f-364">Supported searching user by mail on 'Set-AzSqlServerActiveDirectoryAdministrator' [#12192]</span></span>

#### <a name="azstorage"></a><span data-ttu-id="73f1f-365">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="73f1f-365">Az.Storage</span></span>
* <span data-ttu-id="73f1f-366">RequireInfrastructureEncryption을 사용하여 스토리지 계정 만들기 지원</span><span class="sxs-lookup"><span data-stu-id="73f1f-366">Supported create Storage account with RequireInfrastructureEncryption</span></span>
    -  <span data-ttu-id="73f1f-367">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="73f1f-367">'New-AzStorageAccount'</span></span>
* <span data-ttu-id="73f1f-368">Azure.Core 로딩 논리를 Az.Accounts로 이동</span><span class="sxs-lookup"><span data-stu-id="73f1f-368">Moved the logic of loading Azure.Core to Az.Accounts</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="73f1f-369">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="73f1f-369">Az.Websites</span></span>
* <span data-ttu-id="73f1f-370">'Restore-AzDeletedWebApp'에서 복원이 실패할 경우 생성된 웹앱을 삭제하는 보호 기능 추가</span><span class="sxs-lookup"><span data-stu-id="73f1f-370">Added safeguard to delete created webapp if restore failed in 'Restore-AzDeletedWebApp'</span></span>
* <span data-ttu-id="73f1f-371">'New-AzWebApp' 및 'New-AzWebAppSlot'에 대한 'SourceWebApp.Location' 추가</span><span class="sxs-lookup"><span data-stu-id="73f1f-371">Added 'SourceWebApp.Location' for 'New-AzWebApp' and 'New-AzWebAppSlot'</span></span>
* <span data-ttu-id="73f1f-372">'Set-AzWebApp' 및 'Set-AzWebAppSlot'에서 컨테이너 설정을 변경할 수 없는 버그 수정</span><span class="sxs-lookup"><span data-stu-id="73f1f-372">Fixed bug that prevented changing Container settings in 'Set-AzWebApp' and 'Set-AzWebAppSlot'</span></span>
* <span data-ttu-id="73f1f-373">Get-AzWebApp에 대한 -Name을 제공하지 않으면 SiteConfig를 가져오는 버그 수정</span><span class="sxs-lookup"><span data-stu-id="73f1f-373">Fixed bug to get SiteConfig when -Name is not given for Get-AzWebApp</span></span>
* <span data-ttu-id="73f1f-374">Linux 앱용 ASP를 만드는 지원 추가</span><span class="sxs-lookup"><span data-stu-id="73f1f-374">Added a support to create ASP for Linux Apps</span></span>
* <span data-ttu-id="73f1f-375">리소스 그룹 간 복제에 대한 예외 추가</span><span class="sxs-lookup"><span data-stu-id="73f1f-375">Added exceptions for clone across resource groups</span></span>

## <a name="420---june-2020"></a><span data-ttu-id="73f1f-376">4.2.0 - 2020년 6월</span><span class="sxs-lookup"><span data-stu-id="73f1f-376">4.2.0 - June 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="73f1f-377">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="73f1f-377">Az.Accounts</span></span>
* <span data-ttu-id="73f1f-378">Azure Automation 또는 PowerShell 작업에서 Az가 로그를 건너뛸 수 있는 문제 수정[#11492]</span><span class="sxs-lookup"><span data-stu-id="73f1f-378">Fixed an issue that may cause Az to skip logs in Azure Automation or PowerShell jobs [#11492]</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="73f1f-379">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="73f1f-379">Az.AnalysisServices</span></span>
* <span data-ttu-id="73f1f-380">데이터 평면 cmdlet의 어셈블리 버전 업데이트</span><span class="sxs-lookup"><span data-stu-id="73f1f-380">Updated assembly version of data plane cmdlets</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="73f1f-381">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="73f1f-381">Az.ApiManagement</span></span>
* <span data-ttu-id="73f1f-382">서비스 관리 cmdlet의 어셈블리 버전 업데이트</span><span class="sxs-lookup"><span data-stu-id="73f1f-382">Updated assembly version of service management cmdlets</span></span>

#### <a name="azbilling"></a><span data-ttu-id="73f1f-383">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="73f1f-383">Az.Billing</span></span>
* <span data-ttu-id="73f1f-384">소비 cmdlet의 어셈블리 버전 업데이트</span><span class="sxs-lookup"><span data-stu-id="73f1f-384">Updated assembly version of consumption cmdlets</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="73f1f-385">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="73f1f-385">Az.CognitiveServices</span></span>
* <span data-ttu-id="73f1f-386">PrivateEndpoint 및 PublicNetworkAccess control을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-386">Support PrivateEndpoint and PublicNetworkAccess control.</span></span> 

#### <a name="azdatafactory"></a><span data-ttu-id="73f1f-387">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="73f1f-387">Az.DataFactory</span></span>
* <span data-ttu-id="73f1f-388">데이터 팩터리 V2 cmdlet의 어셈블리 버전 업데이트</span><span class="sxs-lookup"><span data-stu-id="73f1f-388">Updated assembly version of data factory V2 cmdlets</span></span>

#### <a name="azdatashare"></a><span data-ttu-id="73f1f-389">Az.DataShare</span><span class="sxs-lookup"><span data-stu-id="73f1f-389">Az.DataShare</span></span>
* <span data-ttu-id="73f1f-390">''Az.DataShare'' 모듈의 일반 공급</span><span class="sxs-lookup"><span data-stu-id="73f1f-390">General availability of ''Az.DataShare'' module</span></span>

#### <a name="azdesktopvirtualization"></a><span data-ttu-id="73f1f-391">Az.DesktopVirtualization</span><span class="sxs-lookup"><span data-stu-id="73f1f-391">Az.DesktopVirtualization</span></span>
* <span data-ttu-id="73f1f-392">''Az.DesktopVirtualization'' 모듈의 일반 공급</span><span class="sxs-lookup"><span data-stu-id="73f1f-392">General availability of ''Az.DesktopVirtualization'' module</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="73f1f-393">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="73f1f-393">Az.OperationalInsights</span></span>
* <span data-ttu-id="73f1f-394">SDK를 0.21.0으로 업그레이드</span><span class="sxs-lookup"><span data-stu-id="73f1f-394">Upgraded SDK to 0.21.0</span></span>
* <span data-ttu-id="73f1f-395">다음에 선택적 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="73f1f-395">Added optional parameters to</span></span> 
    - <span data-ttu-id="73f1f-396">'New-AzOperationalInsightsSavedSearch'</span><span class="sxs-lookup"><span data-stu-id="73f1f-396">'New-AzOperationalInsightsSavedSearch'</span></span>
    - <span data-ttu-id="73f1f-397">'Set-AzOperationalInsightsSavedSearch'</span><span class="sxs-lookup"><span data-stu-id="73f1f-397">'Set-AzOperationalInsightsSavedSearch'</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="73f1f-398">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="73f1f-398">Az.PolicyInsights</span></span>
* <span data-ttu-id="73f1f-399">'Start-AzPolicyComplianceScan'의 예제 3 수정</span><span class="sxs-lookup"><span data-stu-id="73f1f-399">Corrected example 3 for 'Start-AzPolicyComplianceScan'</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="73f1f-400">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="73f1f-400">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="73f1f-401">PowerBI cmdlet의 어셈블리 버전 업데이트</span><span class="sxs-lookup"><span data-stu-id="73f1f-401">Updated assembly version of PowerBI cmdlets</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="73f1f-402">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="73f1f-402">Az.PrivateDns</span></span>
* <span data-ttu-id="73f1f-403">Remove-AzPrivateDnsRecordSet에 대한 자세한 정보 출력 문자열 형식 수정</span><span class="sxs-lookup"><span data-stu-id="73f1f-403">Corrected verbose output string formatting for Remove-AzPrivateDnsRecordSet</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="73f1f-404">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="73f1f-404">Az.RecoveryServices</span></span>
* <span data-ttu-id="73f1f-405">xml 입력에서 영역 간 복제를 위한 복구 계획을 세우기 위한 Azure Site Recovery 지원.</span><span class="sxs-lookup"><span data-stu-id="73f1f-405">Azure Site Recovery support for creating recovery plan for zone to zone replication from xml input.</span></span>
* <span data-ttu-id="73f1f-406">SiteRecovery 및 Backup cmdlet의 어셈블리 버전 업데이트</span><span class="sxs-lookup"><span data-stu-id="73f1f-406">Updated assembly version of SiteRecovery and Backup cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="73f1f-407">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="73f1f-407">Az.Resources</span></span>
* <span data-ttu-id="73f1f-408">Get-AzDeploymentScriptLog 및 Save-AzDeploymentScriptLog cmdlet에 Tail 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="73f1f-408">Added Tail parameter to Get-AzDeploymentScriptLog and Save-AzDeploymentScriptLog cmdlets</span></span>
* <span data-ttu-id="73f1f-409">형식이 지정된 출력 속성을 Get-AzDeploymentScript cmdlet 출력에 표시</span><span class="sxs-lookup"><span data-stu-id="73f1f-409">Formatted Output property and show it on the Get-AzDeploymentScript cmdlet output</span></span>
* <span data-ttu-id="73f1f-410">-DeploymentScriptInputObject 매개 변수의 이름이 -DeploymentScriptObject로 변경</span><span class="sxs-lookup"><span data-stu-id="73f1f-410">Renamed -DeploymentScriptInputObject parameter to -DeploymentScriptObject</span></span>
* <span data-ttu-id="73f1f-411">cmdlet 메시지에서 누락된 파일/대상 이름이 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-411">Fixed missing file/target name in cmdlet messages.</span></span>
* <span data-ttu-id="73f1f-412">리소스 관리자 및 태그 cmdlet의 어셈블리 버전 업데이트</span><span class="sxs-lookup"><span data-stu-id="73f1f-412">Updated assembly version of resource manager and tags cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="73f1f-413">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="73f1f-413">Az.Sql</span></span>
* <span data-ttu-id="73f1f-414">UsePrivateLinkConnection을 'New-AzSqlSyncGroup', 'Update-AzSqlSyncGroup', 'New-AzSqlSyncMember' 및 'Update-AzSqlSyncMember'에 추가</span><span class="sxs-lookup"><span data-stu-id="73f1f-414">Added UsePrivateLinkConnection to 'New-AzSqlSyncGroup', 'Update-AzSqlSyncGroup', 'New-AzSqlSyncMember' and 'Update-AzSqlSyncMember'</span></span>
* <span data-ttu-id="73f1f-415">SyncMemberAzureDatabaseResourceId를 'New-AzSqlSyncMember' 및 'Update-AzSqlSyncMember'에 추가</span><span class="sxs-lookup"><span data-stu-id="73f1f-415">Added SyncMemberAzureDatabaseResourceId to 'New-AzSqlSyncMember' and 'Update-AzSqlSyncMember'</span></span>
* <span data-ttu-id="73f1f-416">SQL Server Azure Active Directory Admin cmdlet을 설정하는 게스트 사용자 조회 지원 추가</span><span class="sxs-lookup"><span data-stu-id="73f1f-416">Added Guest user lookup support to Set SQL Server Azure Active Directory Admin cmdlet</span></span>

#### <a name="azstorage"></a><span data-ttu-id="73f1f-417">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="73f1f-417">Az.Storage</span></span>
* <span data-ttu-id="73f1f-418">데이터 평면 cmdlet의 어셈블리 버전 업데이트</span><span class="sxs-lookup"><span data-stu-id="73f1f-418">Updated assembly version of data plane cmdlets</span></span>

## <a name="410---may-2020"></a><span data-ttu-id="73f1f-419">4.1.0 - 2020년 5월</span><span class="sxs-lookup"><span data-stu-id="73f1f-419">4.1.0 - May 2020</span></span>
### <a name="highlights-since-the-last-release"></a><span data-ttu-id="73f1f-420">마지막 릴리스 이후의 주요 사항</span><span class="sxs-lookup"><span data-stu-id="73f1f-420">Highlights since the last release</span></span>
* <span data-ttu-id="73f1f-421">지원되는 PowerShell 버전: Windows PowerShell 5.1, PowerShell Core 6.2.4 이상, PowerShell 7</span><span class="sxs-lookup"><span data-stu-id="73f1f-421">Supported PowerShell versions: Windows PowerShell 5.1, PowerShell Core 6.2.4+, PowerShell 7</span></span>
* <span data-ttu-id="73f1f-422">Az.Functions 일반 공급</span><span class="sxs-lookup"><span data-stu-id="73f1f-422">General availability of Az.Functions</span></span> 
* <span data-ttu-id="73f1f-423">Az.ApiManagement, Az.Batch, Az.Compute, Az.KeyVault, Az.Monitor, Az.Network, Az.OperationalInsights, Az.Resources 및 Az.Storage의 주요 릴리스 출시</span><span class="sxs-lookup"><span data-stu-id="73f1f-423">Az.ApiManagement, Az.Batch, Az.Compute, Az.KeyVault, Az.Monitor, Az.Network, Az.OperationalInsights, Az.Resources, and Az.Storage have major release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="73f1f-424">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="73f1f-424">Az.Accounts</span></span>
* <span data-ttu-id="73f1f-425">'AzureSynapseAnalyticsEndpointResourceId' 및 'AzureSynapseAnalyticsEndpointSuffix' 매개 변수를 허용하도록 'Add-AzEnvironment' 및 'Set-AzEnvironment' 업데이트</span><span class="sxs-lookup"><span data-stu-id="73f1f-425">Updated 'Add-AzEnvironment' and 'Set-AzEnvironment' to accept parameters 'AzureSynapseAnalyticsEndpointResourceId' and 'AzureSynapseAnalyticsEndpointSuffix'</span></span>
* <span data-ttu-id="73f1f-426">Az.Accounts에 Azure.Core 관련 어셈블리가 추가되었으며 지원되는 PowerShell 플랫폼은 Windows PowerShell 5.1, PowerShell Core 6.2.4, PowerShell 7+입니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-426">Added Azure.Core related assemblies into Az.Accounts, supported PowerShell platforms include Windows PowerShell 5.1, PowerShell Core 6.2.4, PowerShell 7+</span></span>

#### <a name="azaks"></a><span data-ttu-id="73f1f-427">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="73f1f-427">Az.Aks</span></span>
* <span data-ttu-id="73f1f-428">API 버전을 2019-10-01로 업그레이드</span><span class="sxs-lookup"><span data-stu-id="73f1f-428">Upgraded API Version to 2019-10-01</span></span>
* <span data-ttu-id="73f1f-429">Windows 컨테이너를 사용하여 AKS 만들기 지원</span><span class="sxs-lookup"><span data-stu-id="73f1f-429">Supported to create AKS using Windows container</span></span>
* <span data-ttu-id="73f1f-430">새 cmdlet 추가: 'New-AzAksNodePool', 'Update-AzAksNodePool', 'Remove-AzAksNodePool', 'Get-AzAksNodePool', 'Install-AzAksKubectl', 'Get-AzAksVersion'</span><span class="sxs-lookup"><span data-stu-id="73f1f-430">Provided new cmdlets: 'New-AzAksNodePool', 'Update-AzAksNodePool', 'Remove-AzAksNodePool',        'Get-AzAksNodePool', 'Install-AzAksKubectl', 'Get-AzAksVersion'</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="73f1f-431">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="73f1f-431">Az.ApiManagement</span></span>
* <span data-ttu-id="73f1f-432">'New-AzApiManagement' 및 'Set-AzApiManagement': [-AssignIdentity] 매개 변수 이름을 [-SystemAssignedIdentity]로 변경</span><span class="sxs-lookup"><span data-stu-id="73f1f-432">'New-AzApiManagement' and 'Set-AzApiManagement': [-AssignIdentity] parameter renamed as [-SystemAssignedIdentity]</span></span>
* <span data-ttu-id="73f1f-433">'New-AzApiManagement' 및 'Set-AzApiManagement': 새 매개 변수 추가: [-UserAssignedIdentity <String[]>]</span><span class="sxs-lookup"><span data-stu-id="73f1f-433">'New-AzApiManagement' and 'Set-AzApiManagement': New parameter added: [-UserAssignedIdentity <String[]>]</span></span>
* <span data-ttu-id="73f1f-434">'Get-AzApiManagementProperty': 'Get-AzApiManagementNamedValue'로 이름 변경.</span><span class="sxs-lookup"><span data-stu-id="73f1f-434">'Get-AzApiManagementProperty': renamed as 'Get-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="73f1f-435">PropertyId 매개 변수 이름을 NamedValueId로 변경.</span><span class="sxs-lookup"><span data-stu-id="73f1f-435">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="73f1f-436">'New-AzApiManagementProperty': 'New-AzApiManagementNamedValue'로 이름 변경.</span><span class="sxs-lookup"><span data-stu-id="73f1f-436">'New-AzApiManagementProperty': renamed as 'New-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="73f1f-437">PropertyId 매개 변수 이름을 NamedValueId로 변경.</span><span class="sxs-lookup"><span data-stu-id="73f1f-437">PropertyId parameter renamed as NamedValueId.</span></span> 
* <span data-ttu-id="73f1f-438">'Set-AzApiManagementProperty': 'Set-AzApiManagementNamedValue'로 이름 변경.</span><span class="sxs-lookup"><span data-stu-id="73f1f-438">'Set-AzApiManagementProperty': renamed as 'Set-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="73f1f-439">PropertyId 매개 변수 이름을 NamedValueId로 변경.</span><span class="sxs-lookup"><span data-stu-id="73f1f-439">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="73f1f-440">'Remove-AzApiManagementProperty': 'Remove-AzApiManagementNamedValue'로 이름 변경.</span><span class="sxs-lookup"><span data-stu-id="73f1f-440">'Remove-AzApiManagementProperty': renamed as 'Remove-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="73f1f-441">PropertyId 매개 변수 이름을 NamedValueId로 변경.</span><span class="sxs-lookup"><span data-stu-id="73f1f-441">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="73f1f-442">새 'Get-AzApiManagementAuthorizationServerClientSecret' cmdlet이 추가되었으며 'Get-AzApiManagementAuthorizationServer'는 더 이상 클라이언트 암호를 반환하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-442">Added new 'Get-AzApiManagementAuthorizationServerClientSecret' cmdlet and 'Get-AzApiManagementAuthorizationServer' will not return client secret anymore.</span></span>
* <span data-ttu-id="73f1f-443">새 'Get-AzApiManagementNamedValueSecretValue' cmdlet이 추가되었으며 'Get-AzApiManagementNamedValue'는 더 이상 비밀 값을 반환하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-443">Added new 'Get-AzApiManagementNamedValueSecretValue' cmdlet and 'Get-AzApiManagementNamedValue' will not return secret value.</span></span>
* <span data-ttu-id="73f1f-444">새 'Get-AzApiManagementOpenIdConnectProviderClientSecret' cmdlet이 추가되었으며 'Get-AzApiManagementOpenIdConnectProvider'는 더 이상 클라이언트 암호를 반환하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-444">Added new 'Get-AzApiManagementOpenIdConnectProviderClientSecret' cmdlet and 'Get-AzApiManagementOpenIdConnectProvider' will not return client secret anymore.</span></span>
* <span data-ttu-id="73f1f-445">새 'Get-AzApiManagementSubscriptionKey' cmdlet이 추가되었으며 'Get-AzApiManagementSubscription'은 더 이상 구독 키를 반환하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-445">Added new 'Get-AzApiManagementSubscriptionKey' cmdlet and 'Get-AzApiManagementSubscription' will not return subscription keys anymore.</span></span>
* <span data-ttu-id="73f1f-446">새 'Get-AzApiManagementTenantAccessSecret' cmdlet이 추가되었으며 'Get-AzApiManagementTenantAccess'는 더 이상 키를 반환하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-446">Added new 'Get-AzApiManagementTenantAccessSecret' cmdlet and 'Get-AzApiManagementTenantAccess' will not return keys anymore.</span></span>
* <span data-ttu-id="73f1f-447">새 'Get-AzApiManagementTenantGitAccessSecret' cmdlet이 추가되었으며 'Get-AzApiManagementTenantGitAccess'는 더 이상 키를 반환하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-447">Added new 'Get-AzApiManagementTenantGitAccessSecret' cmdlet and 'Get-AzApiManagementTenantGitAccess' will not return keys anymore.</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="73f1f-448">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="73f1f-448">Az.ApplicationInsights</span></span>
* <span data-ttu-id="73f1f-449">매개 변수 추가: 'New-AzApplicationInsights'에 대한 'RetentionInDays' 'PublicNetworkAccessForIngestion' 'PublicNetworkAccessForQuery'</span><span class="sxs-lookup"><span data-stu-id="73f1f-449">Added Parameters: 'RetentionInDays' 'PublicNetworkAccessForIngestion' 'PublicNetworkAccessForQuery' for 'New-AzApplicationInsights'</span></span>
* <span data-ttu-id="73f1f-450">'Update-AzApplicationInsights' cmdlet 작성</span><span class="sxs-lookup"><span data-stu-id="73f1f-450">Created cmdlet 'Update-AzApplicationInsights'</span></span>
* <span data-ttu-id="73f1f-451">연결된 스토리지 계정에 대한 cmdlet 작성</span><span class="sxs-lookup"><span data-stu-id="73f1f-451">Created cmdlets for Linked Storage Account</span></span>

#### <a name="azbatch"></a><span data-ttu-id="73f1f-452">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="73f1f-452">Az.Batch</span></span>
* <span data-ttu-id="73f1f-453">'Microsoft.Azure.Batch' SDK 버전 13.0.0 및 'Microsoft.Azure.Management.Batch' SDK 버전 9.0.0을 사용하도록 Az.Batch가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-453">Updated Az.Batch to use 'Microsoft.Azure.Batch' SDK version 13.0.0 and 'Microsoft.Azure.Management.Batch' SDK version 9.0.0.</span></span>
* <span data-ttu-id="73f1f-454">새 '-CertificateKind' 매개 변수를 사용하여 'AzBatchCertificate'에 추가할 인증서 종류를 선택하는 기능이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-454">Added the ability to select the kind of certificate being added using the new '-CertificateKind' parameter to 'New-AzBatchCertificate'.</span></span>
* <span data-ttu-id="73f1f-455">이전에 항상 ''였던 'ApplicationPackages' 속성이 'PSApplication'에서 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-455">Removed 'ApplicationPackages' property from 'PSApplication' which was previously always ''.</span></span>
  - <span data-ttu-id="73f1f-456">이제 'Get-AzBatchApplicationPackage'를 사용하여 애플리케이션 내부의 특정 패키지를 검색할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-456">The specific packages inside of an application now can be retrieved using 'Get-AzBatchApplicationPackage'.</span></span> <span data-ttu-id="73f1f-457">예를 들면 다음과 같습니다. 'Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication'.</span><span class="sxs-lookup"><span data-stu-id="73f1f-457">For example: 'Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication'.</span></span>
* <span data-ttu-id="73f1f-458">'New-AzBatchPool'을 사용하여 풀을 만들 때 'PSImageReference'의 'VirtualMachineImageId' 속성은 이제 Shared Image Gallery 이미지만 참조할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-458">When creating a pool using 'New-AzBatchPool', the 'VirtualMachineImageId' property of 'PSImageReference' can now only refer to a Shared Image Gallery image.</span></span>
* <span data-ttu-id="73f1f-459">'New-AzBatchPool'을 사용하여 풀을 만들 때 공용 IP 없이 'PSNetworkConfiguration'의 새 'PublicIPAddressConfiguration'을 사용하여 풀을 프로비저닝할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-459">When creating a pool using 'New-AzBatchPool', the pool can be provisioned without a public IP using the new 'PublicIPAddressConfiguration' property of 'PSNetworkConfiguration'.</span></span>
  - <span data-ttu-id="73f1f-460">'PSNetworkConfiguration'의 'PublicIPs' 속성도 'PSPublicIPAddressConfiguration'으로 이동되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-460">The 'PublicIPs' property of 'PSNetworkConfiguration' has moved in to 'PSPublicIPAddressConfiguration' as well.</span></span> <span data-ttu-id="73f1f-461">이 속성은 'IPAddressProvisioningType'이 'UserManaged'인 경우에만 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-461">This property can only be specified if 'IPAddressProvisioningType' is 'UserManaged'.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="73f1f-462">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="73f1f-462">Az.Compute</span></span>
* <span data-ttu-id="73f1f-463">'Update-AzVM' cmdlet에 HostId 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="73f1f-463">Added HostId parameter to 'Update-AzVM' cmdlet</span></span>
* <span data-ttu-id="73f1f-464">'New-AzVMConfig', 'New-AzVmssConfig', 'Update-AzVmss', 'Set-AzVMOperatingSystem' 및 'Set-AzVmssOsProfile' cmdlet의 도움말 문서가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-464">Updated Help documents for 'New-AzVMConfig', 'New-AzVmssConfig', 'Update-AzVmss', 'Set-AzVMOperatingSystem' and 'Set-AzVmssOsProfile' cmdlets.</span></span>
* <span data-ttu-id="73f1f-465">주요 변경 내용</span><span class="sxs-lookup"><span data-stu-id="73f1f-465">Breaking changes</span></span>
    - <span data-ttu-id="73f1f-466">'Get-AzVMImage' cmdlet에서 FilterExpression 매개 변수가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-466">FilterExpression parameter is removed from 'Get-AzVMImage' cmdlet.</span></span>
    - <span data-ttu-id="73f1f-467">'New-AzVmssConfig', 'New-AzVMConfig' 및 'Update-AzVM' cmdlet에서 AssignIdentity 매개 변수가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-467">AssignIdentity parameter is removed from 'New-AzVmssConfig', 'New-AzVMConfig' and 'Update-AzVM' cmdlets.</span></span>
    - <span data-ttu-id="73f1f-468">'New-AzVmssConfig' 및 'Update-AzVmss' cmdlet에서 AutomaticRepairMaxInstanceRepairsPercent가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-468">AutomaticRepairMaxInstanceRepairsPercent is removed from 'New-AzVmssConfig' and 'Update-AzVmss' cmdlets.</span></span>
    - <span data-ttu-id="73f1f-469">ProximityPlacementGroup에서 AvailabilitySetsColocationStatus, VirtualMachinesColocationStatus 및 VirtualMachineScaleSetsColocationStatus 속성이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-469">AvailabilitySetsColocationStatus, VirtualMachinesColocationStatus and VirtualMachineScaleSetsColocationStatus properties are removed from ProximityPlacementGroup.</span></span>
    - <span data-ttu-id="73f1f-470">AutomaticRepairsPolicy에서 MaxInstanceRepairsPercent 속성이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-470">MaxInstanceRepairsPercent property is removed from AutomaticRepairsPolicy.</span></span>
    - <span data-ttu-id="73f1f-471">AvailabilitySets, VirtualMachines 및 VirtualMachineScaleSets 형식이 IList<SubResource>에서 IList<SubResourceWithColocationStatus>로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-471">The types of AvailabilitySets, VirtualMachines and VirtualMachineScaleSets are changed from IList<SubResource> to IList<SubResourceWithColocationStatus>.</span></span>
* <span data-ttu-id="73f1f-472">'Get-AzVM' cmdlet에 대한 설명이 보다 정확하게 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-472">Description for 'Get-AzVM' cmdlet has been updated to better describe it.</span></span> 

#### <a name="azdatafactory"></a><span data-ttu-id="73f1f-473">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="73f1f-473">Az.DataFactory</span></span>
* <span data-ttu-id="73f1f-474">Managed IR에서 데이터 흐름 런타임 속성의 CRUD를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-474">Supported CRUD of data flow runtime properties in Managed IR.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="73f1f-475">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="73f1f-475">Az.FrontDoor</span></span>
* <span data-ttu-id="73f1f-476">Front Door 규칙 엔진 개체를 생성, 업데이트, 검색 및 삭제할 수 있는 새 cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="73f1f-476">Added new cmdlets for creation, update, retreival, and deletion of Front Door Rules Engine object</span></span>
* <span data-ttu-id="73f1f-477">Front Door 규칙 엔진 개체를 작성할 수 있는 도우미 cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="73f1f-477">Added helper cmdlets for construction of Front Door Rules Engine object</span></span>
* <span data-ttu-id="73f1f-478">Front Door 회람 규칙 개체에 대한 규칙 엔진 참조 추가</span><span class="sxs-lookup"><span data-stu-id="73f1f-478">Added Rules Engine reference to Front Door Routing Rule object.</span></span>
* <span data-ttu-id="73f1f-479">Front Door 백 엔드 개체에 Private Link 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="73f1f-479">Added Private Link parameters to Front Door Backend object</span></span>

#### <a name="azfunctions"></a><span data-ttu-id="73f1f-480">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="73f1f-480">Az.Functions</span></span>
* <span data-ttu-id="73f1f-481">''Az.Functions'' 모듈의 일반 공급</span><span class="sxs-lookup"><span data-stu-id="73f1f-481">General availability of ''Az.Functions'' module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="73f1f-482">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="73f1f-482">Az.HDInsight</span></span>
* <span data-ttu-id="73f1f-483">고객 관리형 키 디스크 암호화 지원</span><span class="sxs-lookup"><span data-stu-id="73f1f-483">Supported Customer-managed key disk encryption.</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="73f1f-484">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="73f1f-484">Az.HealthcareApis</span></span>
* <span data-ttu-id="73f1f-485">더 이상 액세스 정책이 기본적으로 현재 보안 주체로 설정되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-485">Access policies are no longer defaulted to the current principal</span></span>

#### <a name="aziothub"></a><span data-ttu-id="73f1f-486">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="73f1f-486">Az.IotHub</span></span>
* <span data-ttu-id="73f1f-487">SQL과 비슷한 언어를 사용하여 정보를 검색하기 위해 IoT 허브에서 쿼리를 호출하는 cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-487">Added cmdlet to invoke a query in an IoT hub to retrieve information using a SQL-like language.</span></span>
* <span data-ttu-id="73f1f-488">'Add-AzIotHubDevice'가 자식 디바이스 없는 에지 지원 디바이스를 만들 수 없는 문제 해결 [#11597]</span><span class="sxs-lookup"><span data-stu-id="73f1f-488">Fix issue that 'Add-AzIotHubDevice' fails to create Edge Enabled Device without child devices [#11597]</span></span>
* <span data-ttu-id="73f1f-489">IoT Hub, 디바이스 또는 모듈에 대한 SAS 토큰을 생성하는 cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-489">Added cmdlet to generate SAS token for Iot Hub, device or module.</span></span>
* <span data-ttu-id="73f1f-490">구성 메트릭 쿼리를 호출하는 cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-490">Added cmdlet to invoke configuration metrics query.</span></span>
* <span data-ttu-id="73f1f-491">IoT Edge 자동 배포를 대규모로 관리합니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-491">Manage IoT Edge automatic deployment at scale.</span></span> <span data-ttu-id="73f1f-492">새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-492">New cmdlets are:</span></span>
    - <span data-ttu-id="73f1f-493">'Add-AzIotHubDeployment'</span><span class="sxs-lookup"><span data-stu-id="73f1f-493">'Add-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="73f1f-494">'Get-AzIotHubDeployment'</span><span class="sxs-lookup"><span data-stu-id="73f1f-494">'Get-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="73f1f-495">'Remove-AzIotHubDeployment'</span><span class="sxs-lookup"><span data-stu-id="73f1f-495">'Remove-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="73f1f-496">'Set-AzIotHubDeployment'</span><span class="sxs-lookup"><span data-stu-id="73f1f-496">'Set-AzIotHubDeployment'</span></span>
* <span data-ttu-id="73f1f-497">IoT Edge 배포 메트릭 쿼리를 호출하는 cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-497">Added cmdlet to invoke an IoT Edge deployment metrics query.</span></span>
* <span data-ttu-id="73f1f-498">지정된 에지 디바이스에 구성 콘텐츠를 적용하는 cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-498">Added cmdlet to apply the configuration content to the specified edge device.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="73f1f-499">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="73f1f-499">Az.KeyVault</span></span>
* <span data-ttu-id="73f1f-500">다음 별칭 제거: 'New-AzKeyVaultCertificateAdministratorDetails' 및 'New-AzKeyVaultCertificateOrganizationDetails'</span><span class="sxs-lookup"><span data-stu-id="73f1f-500">Removed two aliases: 'New-AzKeyVaultCertificateAdministratorDetails' and 'New-AzKeyVaultCertificateOrganizationDetails'</span></span>
* <span data-ttu-id="73f1f-501">키 자격 증명 모음을 만들 때 기본적으로 일시 삭제 사용</span><span class="sxs-lookup"><span data-stu-id="73f1f-501">Enabled soft delete by default when creating a key vault</span></span>
* <span data-ttu-id="73f1f-502">키 자격 증명 모음을 만들 때 특정 네트워크 위치의 액세스를 제어하도록 네트워크 규칙을 설정할 수 있음</span><span class="sxs-lookup"><span data-stu-id="73f1f-502">Network rules can be set to govern the accessibility from specific network locations when creating a key vault</span></span>
* <span data-ttu-id="73f1f-503">BYOK(Bring Your Own Key) 지원 추가</span><span class="sxs-lookup"><span data-stu-id="73f1f-503">Added support to bring your own key (BYOK)</span></span>
    - <span data-ttu-id="73f1f-504">'Add-AzKeyVaultKey'가 키 교환 키 생성 지원</span><span class="sxs-lookup"><span data-stu-id="73f1f-504">'Add-AzKeyVaultKey' supports generating a key exchange key</span></span>
    - <span data-ttu-id="73f1f-505">'Get-AzKeyVaultKey'가 PEM 형식의 공개 키 다운로드 지원</span><span class="sxs-lookup"><span data-stu-id="73f1f-505">'Get-AzKeyVaultKey' supports downloading a public key in PEM format</span></span>
* <span data-ttu-id="73f1f-506">'AzKeyVaultKey' 도움말 문서의 'KeyOps' 부분 업데이트</span><span class="sxs-lookup"><span data-stu-id="73f1f-506">Updated the 'KeyOps' part of the help document of 'Add-AzKeyVaultKey'</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="73f1f-507">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="73f1f-507">Az.Monitor</span></span>
* <span data-ttu-id="73f1f-508">'Set-AzDiagnosticSettings'의 버그 수정, 일부 범주에는 보존 정책이 적용되지 않음 [#11589]</span><span class="sxs-lookup"><span data-stu-id="73f1f-508">Fixed bug for 'Set-AzDiagnosticSettings', retention policy won't apply to all categories [#11589]</span></span>
* <span data-ttu-id="73f1f-509">메트릭 경고 V2에 WebTest를 사용하기 위한 조건 지원</span><span class="sxs-lookup"><span data-stu-id="73f1f-509">Supported WebTest availability criteria for metric alert V2</span></span>
    - <span data-ttu-id="73f1f-510">'New-AzMetricAlertRuleV2Criteria': webtest 사용 조건을 만드는 옵션 추가</span><span class="sxs-lookup"><span data-stu-id="73f1f-510">'New-AzMetricAlertRuleV2Criteria': an option to create webtest availability criteria was added</span></span>
    - <span data-ttu-id="73f1f-511">'Add-AzMetricAlertRuleV2': 새 webtest 사용 조건 지원</span><span class="sxs-lookup"><span data-stu-id="73f1f-511">'Add-AzMetricAlertRuleV2': supports the new webtest availability criteria</span></span>
* <span data-ttu-id="73f1f-512">PSLogProfile에서 RetentionPolicy에 대한 중복 정의 제거 [#7608]</span><span class="sxs-lookup"><span data-stu-id="73f1f-512">Removed redundant definition for RetentionPolicy in PSLogProfile [#7608]</span></span>
* <span data-ttu-id="73f1f-513">PSEventData에 정의된 중복 속성 제거 [#11353]</span><span class="sxs-lookup"><span data-stu-id="73f1f-513">Removed redundant properties difined in PSEventData [#11353]</span></span>
* <span data-ttu-id="73f1f-514">'Get-AzLog'를 'Get-AzActivityLog'로 이름 변경</span><span class="sxs-lookup"><span data-stu-id="73f1f-514">Renamed 'Get-AzLog' to 'Get-AzActivityLog'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="73f1f-515">Az.Network</span><span class="sxs-lookup"><span data-stu-id="73f1f-515">Az.Network</span></span>
* <span data-ttu-id="73f1f-516">영역 기본 동작이 변경된다는 것을 알리기 위해 주요 변경 특성을 추가</span><span class="sxs-lookup"><span data-stu-id="73f1f-516">Added breaking change attribute to notify that Zone default behaviour will be changed</span></span>
    - <span data-ttu-id="73f1f-517">'New-AzPublicIpAddress'</span><span class="sxs-lookup"><span data-stu-id="73f1f-517">'New-AzPublicIpAddress'</span></span>
    - <span data-ttu-id="73f1f-518">'New-AzPublicIpPrefix'</span><span class="sxs-lookup"><span data-stu-id="73f1f-518">'New-AzPublicIpPrefix'</span></span>
    - <span data-ttu-id="73f1f-519">'New-AzLoadBalancerFrontendIpConfig'</span><span class="sxs-lookup"><span data-stu-id="73f1f-519">'New-AzLoadBalancerFrontendIpConfig'</span></span>
* <span data-ttu-id="73f1f-520">새로운 최상위 리소스 SecurityPartnerProvider에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="73f1f-520">Added support for a new top level resource SecurityPartnerProvider</span></span>
    - <span data-ttu-id="73f1f-521">추가된 새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-521">New cmdlets added:</span></span>
        - <span data-ttu-id="73f1f-522">New-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="73f1f-522">New-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="73f1f-523">Remove-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="73f1f-523">Remove-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="73f1f-524">Get-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="73f1f-524">Get-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="73f1f-525">Set-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="73f1f-525">Set-AzSecurityPartnerProvider</span></span>
* <span data-ttu-id="73f1f-526">'PSPrivateEndpointConnection'의 'PSPrivateLinkResource' 및 'GroupId'에서 'RequiredZoneNames' 추가</span><span class="sxs-lookup"><span data-stu-id="73f1f-526">Added 'RequiredZoneNames' on 'PSPrivateLinkResource' and 'GroupId' on 'PSPrivateEndpointConnection'</span></span>
* <span data-ttu-id="73f1f-527">New-AzNetworkWatcherConnectionMonitorTestConfigurationObject에 대한 잘못된 형식의 SuccessThresholdRoundTripTimeMs 매개 변수 수정</span><span class="sxs-lookup"><span data-stu-id="73f1f-527">Fixed incorrect type of SuccessThresholdRoundTripTimeMs parameter for New-AzNetworkWatcherConnectionMonitorTestConfigurationObject</span></span>
* <span data-ttu-id="73f1f-528">AllowVnetToVnetTraffic 인수의 기본값을 True로 설정하도록 VirtualWan cmdlet 업데이트</span><span class="sxs-lookup"><span data-stu-id="73f1f-528">Updated VirtualWan cmdlets to set default value of AllowVnetToVnetTraffic argument to True.</span></span>
    - <span data-ttu-id="73f1f-529">'New-AzVirtualWan'</span><span class="sxs-lookup"><span data-stu-id="73f1f-529">'New-AzVirtualWan'</span></span>
    - <span data-ttu-id="73f1f-530">'Update-AzVirtualWan'</span><span class="sxs-lookup"><span data-stu-id="73f1f-530">'Update-AzVirtualWan'</span></span>
* <span data-ttu-id="73f1f-531">프라이빗 엔드포인트에 대한 DNS 영역 그룹을 지원하는 새 cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="73f1f-531">Added new cmdlets to support DNS zone group for private endpoint</span></span>
    - <span data-ttu-id="73f1f-532">'New-AzPrivateDnsZoneConfig'</span><span class="sxs-lookup"><span data-stu-id="73f1f-532">'New-AzPrivateDnsZoneConfig'</span></span>
    - <span data-ttu-id="73f1f-533">'Get-AzPrivateDnsZoneGroup'</span><span class="sxs-lookup"><span data-stu-id="73f1f-533">'Get-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="73f1f-534">'New-AzPrivateDnsZoneGroup'</span><span class="sxs-lookup"><span data-stu-id="73f1f-534">'New-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="73f1f-535">'Set-AzPrivateDnsZoneGroup'</span><span class="sxs-lookup"><span data-stu-id="73f1f-535">'Set-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="73f1f-536">'Remove-AzPrivateDnsZoneGroup'</span><span class="sxs-lookup"><span data-stu-id="73f1f-536">'Remove-AzPrivateDnsZoneGroup'</span></span>
* <span data-ttu-id="73f1f-537">'AzureFirewall'에 'DNSEnableProxy', 'DNSRequireProxyForNetworkRules' 및 'DNSServers' 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="73f1f-537">Added 'DNSEnableProxy', 'DNSRequireProxyForNetworkRules' and 'DNSServers' parameters to 'AzureFirewall'</span></span>
* <span data-ttu-id="73f1f-538">'AzureFirewall'에 'EnableDnsProxy', 'DnsProxyNotRequiredForNetworkRule' 및 'DnsServer' 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="73f1f-538">Added 'EnableDnsProxy', 'DnsProxyNotRequiredForNetworkRule' and 'DnsServer' parameters to 'AzureFirewall'</span></span>
    - <span data-ttu-id="73f1f-539">업데이트된 cmdlet:</span><span class="sxs-lookup"><span data-stu-id="73f1f-539">Updated cmdlet:</span></span>
        - <span data-ttu-id="73f1f-540">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="73f1f-540">New-AzFirewall</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="73f1f-541">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="73f1f-541">Az.OperationalInsights</span></span>
* <span data-ttu-id="73f1f-542">새로 생성된 SDK를 적용하도록 레거시 코드 업데이트</span><span class="sxs-lookup"><span data-stu-id="73f1f-542">Updated legacy code to apply new generated SDK</span></span>
* <span data-ttu-id="73f1f-543">사용되지 않는 API 때문에 cmdlet 삭제</span><span class="sxs-lookup"><span data-stu-id="73f1f-543">Deleted cmdlets due to deprecated APIs</span></span>
    - <span data-ttu-id="73f1f-544">'Get-AzOperationalInsightsSavedSearchResult'(별칭 'Get-AzOperationalInsightsSavedSearchResults')</span><span class="sxs-lookup"><span data-stu-id="73f1f-544">'Get-AzOperationalInsightsSavedSearchResult' (alias 'Get-AzOperationalInsightsSavedSearchResults')</span></span>
    - <span data-ttu-id="73f1f-545">'Get-AzOperationalInsightsSearchResult'(별칭 'Get-AzOperationalInsightsSearchResults')</span><span class="sxs-lookup"><span data-stu-id="73f1f-545">'Get-AzOperationalInsightsSearchResult' (alias 'Get-AzOperationalInsightsSearchResults')</span></span>
    - <span data-ttu-id="73f1f-546">'Get-AzOperationalInsightsLinkTarget'(별칭 'Get-AzOperationalInsightsLinkTargets')</span><span class="sxs-lookup"><span data-stu-id="73f1f-546">'Get-AzOperationalInsightsLinkTarget' (alias 'Get-AzOperationalInsightsLinkTargets')</span></span>
* <span data-ttu-id="73f1f-547">'Set-AzOperationalInsightsWorkspace' 및 'New-AzOperationalInsightsWorkspace'에 대한 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="73f1f-547">Added parameters for 'Set-AzOperationalInsightsWorkspace' and 'New-AzOperationalInsightsWorkspace'</span></span>
* <span data-ttu-id="73f1f-548">연결된 스토리지 계정에 대한 cmdlet 작성</span><span class="sxs-lookup"><span data-stu-id="73f1f-548">Created cmdlets for Linked Stoarge Account</span></span>
* <span data-ttu-id="73f1f-549">클러스터 및 연결된 서비스에 대한 cmdlet 작성</span><span class="sxs-lookup"><span data-stu-id="73f1f-549">Created cmdlets for Clusters and Linked Service</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="73f1f-550">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="73f1f-550">Az.RecoveryServices</span></span>
* <span data-ttu-id="73f1f-551">Azure Site Recovery - Azure와 Azure 공급자 간 근접 배치 그룹 가상 머신을 보호하기 위한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-551">Azure Site Recovery added support for protecting proximity placement group virtual machines for Azure to Azure provider.</span></span>
* <span data-ttu-id="73f1f-552">Azure Site Recovery - 영역 간 복제에 대한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-552">Azure Site Recovery added support for zone to zone replication.</span></span>
* <span data-ttu-id="73f1f-553">Azure Backup - Azure 파일 공유 복구 지점의 장기 보존 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-553">Azure Backup Added Long term retention support for Azure FileShare Recovery Points.</span></span>
* <span data-ttu-id="73f1f-554">Azure Backup - 'Get-AzRecoveryServicesBackupItem' cmdlet 출력에 디스크 제외 속성이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-554">Azure Backup Added disk exclusion properties to 'Get-AzRecoveryServicesBackupItem' cmdlet output.</span></span>
* <span data-ttu-id="73f1f-555">사이트 복구 서비스용 Vault 자격 증명 파일에 대한 프라이빗 엔드포인트가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-555">Added private endpoint for Vault credential file for site recovery service.</span></span>

#### <a name="azresources"></a><span data-ttu-id="73f1f-556">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="73f1f-556">Az.Resources</span></span>
* <span data-ttu-id="73f1f-557">새 역할 정의를 만들 때 보기 지연에 대한 메시지 경고 추가</span><span class="sxs-lookup"><span data-stu-id="73f1f-557">Added message warning about view delay when creating a new Role Definition</span></span>
* <span data-ttu-id="73f1f-558">강력한 형식의 개체를 출력하도록 정책 cmdlet 변경</span><span class="sxs-lookup"><span data-stu-id="73f1f-558">Changed policy cmdlets to output strongly-typed objects</span></span>
* <span data-ttu-id="73f1f-559">'Get-AzResourceLock' cmdlet에 사용되는 '-TenantLevel' 매개 변수 제거 [#11335]</span><span class="sxs-lookup"><span data-stu-id="73f1f-559">Removed '-TenantLevel' parameter used for on the 'Get-AzResourceLock' cmdlet [#11335]</span></span>
* <span data-ttu-id="73f1f-560">'Remove-AzResourceGroup -Id ResourceId' 수정[#9882]</span><span class="sxs-lookup"><span data-stu-id="73f1f-560">Fixed 'Remove-AzResourceGroup -Id ResourceId'[#9882]</span></span>
* <span data-ttu-id="73f1f-561">리소스 그룹 범위에서 ARM 템플릿 가상 시나리오 결과를 가져오는 새 cmdlet 추가: 'Get-AzDeploymentResourceGroupWhatIfResult'</span><span class="sxs-lookup"><span data-stu-id="73f1f-561">Added new cmdlet for getting ARM template What-If results at resource group scope: 'Get-AzDeploymentResourceGroupWhatIfResult'</span></span>
* <span data-ttu-id="73f1f-562">구독 범위에서 ARM 템플릿 가상 시나리오 결과를 가져오는 새 cmdlet 추가: 'Get-AzDeploymentWhatIfResult'</span><span class="sxs-lookup"><span data-stu-id="73f1f-562">Added new cmdlet for getting ARM template What-If results at subscription scope: 'Get-AzDeploymentWhatIfResult'</span></span>
   - <span data-ttu-id="73f1f-563">별칭: 'Get-AzSubscriptionDeploymentWhatIf'</span><span class="sxs-lookup"><span data-stu-id="73f1f-563">Alias: 'Get-AzSubscriptionDeploymentWhatIf'</span></span>
* <span data-ttu-id="73f1f-564">ARM 템플릿 가상 시나리오 결과를 사용하도록 'New-AzDeployment' 및 'New-AzResourceGroupDeployment'에 대한 '-WhatIf' 및 '-Confirm' 매개 변수 재정의</span><span class="sxs-lookup"><span data-stu-id="73f1f-564">Overrode '-WhatIf' and '-Confirm' parameters for 'New-AzDeployment' and 'New-AzResourceGroupDeployment' to use ARM template What-If results</span></span>
* <span data-ttu-id="73f1f-565">배포 cmdlet에서 'ApiVersion' 매개 변수의 사용 중단 메시지 추가</span><span class="sxs-lookup"><span data-stu-id="73f1f-565">Added deprecation message for 'ApiVersion' parameter in deployment cmdlets</span></span>
* <span data-ttu-id="73f1f-566">배포 오류에 대한 향상된 오류 메시지를 표시하는 기능 추가</span><span class="sxs-lookup"><span data-stu-id="73f1f-566">Added capability to show improved error messages for deployment failures</span></span>
* <span data-ttu-id="73f1f-567">배포 오류에 대한 correlationId 로깅 추가</span><span class="sxs-lookup"><span data-stu-id="73f1f-567">Added correlationId logging for deployment failures</span></span>
* <span data-ttu-id="73f1f-568">배포 스크립트 출력에 'error' 속성 추가</span><span class="sxs-lookup"><span data-stu-id="73f1f-568">Added 'error' property to the deployment script output</span></span>
* <span data-ttu-id="73f1f-569">nuget Microsoft.Azure.Management.ResourceManager를 '3.7.1-preview'로 업데이트</span><span class="sxs-lookup"><span data-stu-id="73f1f-569">Updated nuget Microsoft.Azure.Management.ResourceManager to '3.7.1-preview'</span></span>
* <span data-ttu-id="73f1f-570">nuget 3.7.1-preview에서 DeploymentValidateResult의 Error 속성이 readonly로 변경되어 특정 테스트 사례를 제거</span><span class="sxs-lookup"><span data-stu-id="73f1f-570">Removed specific test cases as Error property in DeploymentValidateResult has changed to readonly from nuget 3.7.1-preview</span></span>
* <span data-ttu-id="73f1f-571">SDK ResourceManager 3.7.1-preview의 GenericResourceExpanded 도입</span><span class="sxs-lookup"><span data-stu-id="73f1f-571">Brought GenericResourceExpanded from SDK ResourceManager 3.7.1-preview</span></span>
* <span data-ttu-id="73f1f-572">모든 배포용 Get cmdlet에 대한 태그 지원 추가</span><span class="sxs-lookup"><span data-stu-id="73f1f-572">Added tag support for all Get cmdlets for deployment, as well as</span></span>
    - <span data-ttu-id="73f1f-573">'New-AzDeployment'</span><span class="sxs-lookup"><span data-stu-id="73f1f-573">'New-AzDeployment'</span></span>
    - <span data-ttu-id="73f1f-574">'New-AzManagementGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="73f1f-574">'New-AzManagementGroupDeployment'</span></span>
    - <span data-ttu-id="73f1f-575">'New-AzResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="73f1f-575">'New-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="73f1f-576">'New-AzTenantDeployment'</span><span class="sxs-lookup"><span data-stu-id="73f1f-576">'New-AzTenantDeployment'</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="73f1f-577">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="73f1f-577">Az.ServiceFabric</span></span>
* <span data-ttu-id="73f1f-578">잘못된 인증서 지문을 가져오는 --SecretIdentifier를 사용한 인증서 추가의 버그 수정</span><span class="sxs-lookup"><span data-stu-id="73f1f-578">Fixed bug in add certificate using --SecretIdentifier that was getting the wrong certificate thumbprint</span></span>

#### <a name="azsql"></a><span data-ttu-id="73f1f-579">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="73f1f-579">Az.Sql</span></span>
* <span data-ttu-id="73f1f-580">성능 강화:</span><span class="sxs-lookup"><span data-stu-id="73f1f-580">Enhance performance of:</span></span>
    - <span data-ttu-id="73f1f-581">'Set-AzSqlDatabaseSensitivityClassification'</span><span class="sxs-lookup"><span data-stu-id="73f1f-581">'Set-AzSqlDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="73f1f-582">'Set-AzSqlInstanceDatabaseSensitivityClassification'</span><span class="sxs-lookup"><span data-stu-id="73f1f-582">'Set-AzSqlInstanceDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="73f1f-583">'Remove-AzSqlDatabaseSensitivityClassification'</span><span class="sxs-lookup"><span data-stu-id="73f1f-583">'Remove-AzSqlDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="73f1f-584">'Remove-AzSqlInstanceDatabaseSensitivityClassification'</span><span class="sxs-lookup"><span data-stu-id="73f1f-584">'Remove-AzSqlInstanceDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="73f1f-585">'Enable-AzSqlDatabaseSensitivityRecommendation'</span><span class="sxs-lookup"><span data-stu-id="73f1f-585">'Enable-AzSqlDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="73f1f-586">'Enable-AzSqlInstanceDatabaseSensitivityRecommendation'</span><span class="sxs-lookup"><span data-stu-id="73f1f-586">'Enable-AzSqlInstanceDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="73f1f-587">'Disable-AzSqlDatabaseSensitivityRecommendation'</span><span class="sxs-lookup"><span data-stu-id="73f1f-587">'Disable-AzSqlDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="73f1f-588">'Disable-AzSqlInstanceDatabaseSensitivityRecommendation'</span><span class="sxs-lookup"><span data-stu-id="73f1f-588">'Disable-AzSqlInstanceDatabaseSensitivityRecommendation'</span></span>
* <span data-ttu-id="73f1f-589">'Set-AzSqlDatabaseBackupShortTermRetentionPolicy' cmdlet에서 'RetentionDays' 매개 변수의 클라이언트 쪽 유효성 검사 제거</span><span class="sxs-lookup"><span data-stu-id="73f1f-589">Removed client-side validation of 'RetentionDays' parameter from cmdlet 'Set-AzSqlDatabaseBackupShortTermRetentionPolicy'</span></span>
* <span data-ttu-id="73f1f-590">Vnet에서 스토리지 계정을 감사하고, Storage Blob 데이터 기여자 역할을 만들 때 발생하는 버그 수정</span><span class="sxs-lookup"><span data-stu-id="73f1f-590">Auditing to a storage account in Vnet, fixing a bug when creating a Storage Blob Data Contributor role.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="73f1f-591">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="73f1f-591">Az.Storage</span></span>
* <span data-ttu-id="73f1f-592">get/list account cmdlet 'Get-AzStorageAccount'에 '-AsJob' 추가</span><span class="sxs-lookup"><span data-stu-id="73f1f-592">Added '-AsJob' to get/list account cmdlet 'Get-AzStorageAccount'</span></span>
* <span data-ttu-id="73f1f-593">키 자동 회전을 지원하기 위해 스토리지 계정을 KeyvaultEncryption으로 업데이트할 때 KeyVersion을 선택 사항으로 지정</span><span class="sxs-lookup"><span data-stu-id="73f1f-593">Make KeyVersion to optional when update Storage account with KeyvaultEncryption, to support key auto-rotation</span></span>
    - <span data-ttu-id="73f1f-594">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="73f1f-594">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="73f1f-595">파이프라인을 사용하여 Azure 파일 디렉터리 제거 오류 수정</span><span class="sxs-lookup"><span data-stu-id="73f1f-595">Fixed remove Azure File Directory fail with pipeline</span></span>
    - <span data-ttu-id="73f1f-596">'Remove-AzStorageDirectory'</span><span class="sxs-lookup"><span data-stu-id="73f1f-596">'Remove-AzStorageDirectory'</span></span>
* <span data-ttu-id="73f1f-597">수정 [#9880]: Swagger에 맞게 NetWorkRule DefaultAction 값 정의 변경</span><span class="sxs-lookup"><span data-stu-id="73f1f-597">Fixed [#9880]: Change NetWorkRule DefaultAction value defination to align with swagger.</span></span>
    - <span data-ttu-id="73f1f-598">'Update-AzStorageAccountNetworkRuleSet'</span><span class="sxs-lookup"><span data-stu-id="73f1f-598">'Update-AzStorageAccountNetworkRuleSet'</span></span>
    - <span data-ttu-id="73f1f-599">'Get-AzStorageAccountNetworkRuleSet'</span><span class="sxs-lookup"><span data-stu-id="73f1f-599">'Get-AzStorageAccountNetworkRuleSet'</span></span>
* <span data-ttu-id="73f1f-600">수정 [#11624]: 서버 오류를 방지하기 위해 NetworkRules를 추가할 때 중복 규칙 건너뛰기</span><span class="sxs-lookup"><span data-stu-id="73f1f-600">Fixed [#11624]: Skip duplicated rules when add NetworkRules, to avoid server failure</span></span>
    - <span data-ttu-id="73f1f-601">'Add-AzStorageAccountNetworkRule'</span><span class="sxs-lookup"><span data-stu-id="73f1f-601">'Add-AzStorageAccountNetworkRule'</span></span>
* <span data-ttu-id="73f1f-602">Microsoft.Azure.Cosmos.Table SDK를 1.0.7로 업그레이드</span><span class="sxs-lookup"><span data-stu-id="73f1f-602">Upgraded Microsoft.Azure.Cosmos.Table SDK to 1.0.7</span></span>
* <span data-ttu-id="73f1f-603">DataLake Gen2 항목 목록에 부품 항목만 반환되는 경우 ContinuationToken을 사용하여 다시 나열하라고 사용자에게 알리는 경고 메시지 추가</span><span class="sxs-lookup"><span data-stu-id="73f1f-603">Added a warning message to remind user to list again with ContinuationToken when only part items are returned in list DataLake Gen2 Items,</span></span>
    - <span data-ttu-id="73f1f-604">'Get-AzDataLakeGen2ChildItem'</span><span class="sxs-lookup"><span data-stu-id="73f1f-604">'Get-AzDataLakeGen2ChildItem'</span></span>
* <span data-ttu-id="73f1f-605">Azure Files Active Directory 도메인 서비스 인증을 사용하여 스토리지 계정을 만들거나 업데이트하는 기능 지원</span><span class="sxs-lookup"><span data-stu-id="73f1f-605">Supported to create or update Storage account with Azure Files Active Directory Domain Service Authentication</span></span>
    -  <span data-ttu-id="73f1f-606">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="73f1f-606">'New-AzStorageAccount'</span></span>
    -  <span data-ttu-id="73f1f-607">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="73f1f-607">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="73f1f-608">스토리지 계정의 Kerberos 키 새로 만들기 또는 나열 지원</span><span class="sxs-lookup"><span data-stu-id="73f1f-608">Supported to new or list Kerberos keys of Storage account</span></span>
    -  <span data-ttu-id="73f1f-609">'New-AzStorageAccountKey'</span><span class="sxs-lookup"><span data-stu-id="73f1f-609">'New-AzStorageAccountKey'</span></span>
    -  <span data-ttu-id="73f1f-610">'Get-AzStorageAccountKey'</span><span class="sxs-lookup"><span data-stu-id="73f1f-610">'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="73f1f-611">스토리지 계정 장애 조치(failover) 지원</span><span class="sxs-lookup"><span data-stu-id="73f1f-611">Supported failover Storage account</span></span>
    - <span data-ttu-id="73f1f-612">'Invoke-AzStorageAccountFailover'</span><span class="sxs-lookup"><span data-stu-id="73f1f-612">'Invoke-AzStorageAccountFailover'</span></span>
* <span data-ttu-id="73f1f-613">'Get-AzStorageBlobCopyState'의 도움말 업데이트</span><span class="sxs-lookup"><span data-stu-id="73f1f-613">Updated help of 'Get-AzStorageBlobCopyState'</span></span>
* <span data-ttu-id="73f1f-614">'Get-AzStorageFileCopyState' 및 'Start-AzStorageBlobCopy'의 도움말 업데이트</span><span class="sxs-lookup"><span data-stu-id="73f1f-614">Updated help of 'Get-AzStorageFileCopyState' and 'Start-AzStorageBlobCopy'</span></span>
* <span data-ttu-id="73f1f-615">스토리지 클라이언트 라이브러리 v12를 큐 및 파일 cmdlet에 통합</span><span class="sxs-lookup"><span data-stu-id="73f1f-615">Integrated Storage client library v12 to Queue and File cmdlets</span></span>
* <span data-ttu-id="73f1f-616">출력 형식을 CloudFile에서 AzureStorageFile로 변경했으며, 원래 출력은 새 출력의 자식 속성이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-616">Changed output type from CloudFile to AzureStorageFile, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="73f1f-617">'Get-AzStorageFile'</span><span class="sxs-lookup"><span data-stu-id="73f1f-617">'Get-AzStorageFile'</span></span>
    - <span data-ttu-id="73f1f-618">'Remove-AzStorageFile'</span><span class="sxs-lookup"><span data-stu-id="73f1f-618">'Remove-AzStorageFile'</span></span>
    - <span data-ttu-id="73f1f-619">'Get-AzStorageFileContent'</span><span class="sxs-lookup"><span data-stu-id="73f1f-619">'Get-AzStorageFileContent'</span></span>
    - <span data-ttu-id="73f1f-620">'Set-AzStorageFileContent'</span><span class="sxs-lookup"><span data-stu-id="73f1f-620">'Set-AzStorageFileContent'</span></span>
    - <span data-ttu-id="73f1f-621">'Start-AzStorageFileCopy'</span><span class="sxs-lookup"><span data-stu-id="73f1f-621">'Start-AzStorageFileCopy'</span></span>
* <span data-ttu-id="73f1f-622">출력 형식을 CloudFileDirectory에서 AzureStorageFileDirectory로 변경했으며, 원래 출력은 새 출력의 자식 속성이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-622">Changed output type from CloudFileDirectory to AzureStorageFileDirectory, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="73f1f-623">'New-AzStorageDirectory'</span><span class="sxs-lookup"><span data-stu-id="73f1f-623">'New-AzStorageDirectory'</span></span>
    - <span data-ttu-id="73f1f-624">'Remove-AzStorageDirectory'</span><span class="sxs-lookup"><span data-stu-id="73f1f-624">'Remove-AzStorageDirectory'</span></span>
* <span data-ttu-id="73f1f-625">출력 형식을 CloudFileShare에서 AzureStorageFileShare로 변경했으며, 원래 출력은 새 출력의 자식 속성이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-625">Changed output type from CloudFileShare to AzureStorageFileShare, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="73f1f-626">'Get-AzStorageShare'</span><span class="sxs-lookup"><span data-stu-id="73f1f-626">'Get-AzStorageShare'</span></span>
    - <span data-ttu-id="73f1f-627">'New-AzStorageShare'</span><span class="sxs-lookup"><span data-stu-id="73f1f-627">'New-AzStorageShare'</span></span>
    - <span data-ttu-id="73f1f-628">'Remove-AzStorageShare'</span><span class="sxs-lookup"><span data-stu-id="73f1f-628">'Remove-AzStorageShare'</span></span>
* <span data-ttu-id="73f1f-629">출력 형식을 FileShareProperties에서 AzureStorageFileShare로 변경했으며, 원래 출력은 새 출력의 하위 자식 속성이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-629">Changed output type from FileShareProperties to AzureStorageFileShare, the original output will become a sub child property of the new output</span></span>
    - <span data-ttu-id="73f1f-630">'Set-AzStorageShareQuota'</span><span class="sxs-lookup"><span data-stu-id="73f1f-630">'Set-AzStorageShareQuota'</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="73f1f-631">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="73f1f-631">Az.TrafficManager</span></span>
* <span data-ttu-id="73f1f-632">'DisableAzureTrafficManagerEndpoint' 자세한 정보 출력에서 잘못된 프로필 이름 수정</span><span class="sxs-lookup"><span data-stu-id="73f1f-632">Fixed incorrect profile name in 'DisableAzureTrafficManagerEndpoint' verbose output</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="73f1f-633">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="73f1f-633">Az.Websites</span></span>
* <span data-ttu-id="73f1f-634">'Update-AzWebAppAccessRestrictionConfig'의 도움말에서 철자 오류 수정</span><span class="sxs-lookup"><span data-stu-id="73f1f-634">Fixed typo on help of 'Update-AzWebAppAccessRestrictionConfig'.</span></span>

## <a name="380---april-2020"></a><span data-ttu-id="73f1f-635">3.8.0 - 2020년 4월</span><span class="sxs-lookup"><span data-stu-id="73f1f-635">3.8.0 - April 2020</span></span>
### <a name="highlights-since-the-last-release"></a><span data-ttu-id="73f1f-636">마지막 릴리스 이후의 주요 사항</span><span class="sxs-lookup"><span data-stu-id="73f1f-636">Highlights since the last release</span></span>
* <span data-ttu-id="73f1f-637">Az.Storage에서 지원하는 PowerShell 버전: Windows PowerShell 5.1, PowerShell Core 6.2.4 이상, PowerShell 7</span><span class="sxs-lookup"><span data-stu-id="73f1f-637">PowerShell versions that Az.Storage supports: Windows PowerShell 5.1, PowerShell Core 6.2.4+, PowerShell 7</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="73f1f-638">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="73f1f-638">Az.Accounts</span></span>
* <span data-ttu-id="73f1f-639">'Resolve-AzError'에서 Azure PowerShell 설문 조사 URL이 업데이트되었습니다. [#11507]</span><span class="sxs-lookup"><span data-stu-id="73f1f-639">Updated Azure PowerShell survey URL in 'Resolve-AzError' [#11507]</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="73f1f-640">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="73f1f-640">Az.ApiManagement</span></span>
* <span data-ttu-id="73f1f-641">향후 릴리스의 Azure File cmdlet 출력 변경에 대한 호환성이 손상되는 변경 공지가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-641">Added breaking change notice for Azure File cmdlets output change in a future release</span></span>
* <span data-ttu-id="73f1f-642">'Set-AzApiManagementGroup' - GroupId 매개 변수를 지정하도록 설명서가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-642">'Set-AzApiManagementGroup' Updated documentation to specify the GroupId parameter</span></span>

#### <a name="azcdn"></a><span data-ttu-id="73f1f-643">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="73f1f-643">Az.Cdn</span></span>
* <span data-ttu-id="73f1f-644">ChinaCDN 관련 가격 책정 SKU 표시가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-644">Fixed ChinaCDN related pricing SKU display</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="73f1f-645">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="73f1f-645">Az.CognitiveServices</span></span>
* <span data-ttu-id="73f1f-646">Identity, Encryption, UserOwnedStorage가 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-646">Supported Identity, Encryption, UserOwnedStorage</span></span>

#### <a name="azcompute"></a><span data-ttu-id="73f1f-647">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="73f1f-647">Az.Compute</span></span>
* <span data-ttu-id="73f1f-648">'Set-AzVmssOrchestrationServiceState' cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-648">Added 'Set-AzVmssOrchestrationServiceState' cmdlet.</span></span>
* <span data-ttu-id="73f1f-649">-InstanceView가 있는 'Get-AzVmss'는 OrchestrationService 상태를 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-649">'Get-AzVmss' with -InstanceView shows OrchestrationService states.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="73f1f-650">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="73f1f-650">Az.IotHub</span></span>
* <span data-ttu-id="73f1f-651">IoT 디바이스 쌍 구성을 관리합니다. 새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-651">Manage IoT device twin configuration, New cmdlets are:</span></span>
    - <span data-ttu-id="73f1f-652">'Get-AzIotHubDeviceTwin'</span><span class="sxs-lookup"><span data-stu-id="73f1f-652">'Get-AzIotHubDeviceTwin'</span></span>
    - <span data-ttu-id="73f1f-653">'Update-AzIotHubDeviceTwin'</span><span class="sxs-lookup"><span data-stu-id="73f1f-653">'Update-AzIotHubDeviceTwin'</span></span>
* <span data-ttu-id="73f1f-654">IoT Hub에서 디바이스에 대한 직접 메서드를 호출하는 cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-654">Added cmdlet to invoke direct method on a device in an Iot Hub.</span></span>
* <span data-ttu-id="73f1f-655">IoT 디바이스 모듈 쌍 구성을 관리합니다. 새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-655">Manage IoT device module twin configuration, New cmdlets are:</span></span>
    - <span data-ttu-id="73f1f-656">'Get-AzIotHubModuleTwin'</span><span class="sxs-lookup"><span data-stu-id="73f1f-656">'Get-AzIotHubModuleTwin'</span></span>
    - <span data-ttu-id="73f1f-657">'Update-AzIotHubModuleTwin'</span><span class="sxs-lookup"><span data-stu-id="73f1f-657">'Update-AzIotHubModuleTwin'</span></span>
* <span data-ttu-id="73f1f-658">IoT 자동 디바이스 관리 구성을 대규모로 관리합니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-658">Manage IoT automatic device management configuration at scale.</span></span> <span data-ttu-id="73f1f-659">새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-659">New cmdlets are:</span></span>
    - <span data-ttu-id="73f1f-660">'Add-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="73f1f-660">'Add-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="73f1f-661">'Get-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="73f1f-661">'Get-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="73f1f-662">'Remove-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="73f1f-662">'Remove-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="73f1f-663">'Set-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="73f1f-663">'Set-AzIotHubConfiguration'</span></span>
* <span data-ttu-id="73f1f-664">Iot Hub에서 에지 모듈 메서드를 호출하는 cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-664">Added cmdlet to invoke an edge module method in an Iot Hub.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="73f1f-665">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="73f1f-665">Az.KeyVault</span></span>
* <span data-ttu-id="73f1f-666">자격 증명 모음에서 일시 삭제 및 제거 보호를 사용하도록 설정할 수 있는 새 cmdlet 'Update-AzKeyVault'가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-666">Added a new cmdlet 'Update-AzKeyVault' that can enable soft delete and purge protection on a vault</span></span>
* <span data-ttu-id="73f1f-667">Microsoft.PowerShell.SecretManagement에 대한 지원이 추가되었습니다. [#11178]</span><span class="sxs-lookup"><span data-stu-id="73f1f-667">Added support to Microsoft.PowerShell.SecretManagement [#11178]</span></span>
* <span data-ttu-id="73f1f-668">'Remove-AzKeyVaultManagedStorageSasDefinition' 예제의 오류가 해결되었습니다. [#11479]</span><span class="sxs-lookup"><span data-stu-id="73f1f-668">Fixed error in the examples of 'Remove-AzKeyVaultManagedStorageSasDefinition' [#11479]</span></span>
* <span data-ttu-id="73f1f-669">프라이빗 엔드포인트에 대한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-669">Added support to private endpoint</span></span>

#### <a name="azmaintenance"></a><span data-ttu-id="73f1f-670">Az.Maintenance</span><span class="sxs-lookup"><span data-stu-id="73f1f-670">Az.Maintenance</span></span>
* <span data-ttu-id="73f1f-671">GA용 유지 관리 cmdlet의 릴리스 버전 게시</span><span class="sxs-lookup"><span data-stu-id="73f1f-671">Publishing release version of Maintenance cmdlets for GA</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="73f1f-672">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="73f1f-672">Az.Monitor</span></span>
* <span data-ttu-id="73f1f-673">프라이빗 링크 범위용 cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-673">Added cmdlets for private link scope</span></span>
    - <span data-ttu-id="73f1f-674">'Get-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="73f1f-674">'Get-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="73f1f-675">'Remove-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="73f1f-675">'Remove-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="73f1f-676">'New-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="73f1f-676">'New-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="73f1f-677">'Update-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="73f1f-677">'Update-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="73f1f-678">'Get-AzInsightsPrivateLinkScopedResource'</span><span class="sxs-lookup"><span data-stu-id="73f1f-678">'Get-AzInsightsPrivateLinkScopedResource'</span></span>
    - <span data-ttu-id="73f1f-679">'New-AzInsightsPrivateLinkScopedResource'</span><span class="sxs-lookup"><span data-stu-id="73f1f-679">'New-AzInsightsPrivateLinkScopedResource'</span></span>
    - <span data-ttu-id="73f1f-680">'Remove-AzInsightsPrivateLinkScopedResource'</span><span class="sxs-lookup"><span data-stu-id="73f1f-680">'Remove-AzInsightsPrivateLinkScopedResource'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="73f1f-681">Az.Network</span><span class="sxs-lookup"><span data-stu-id="73f1f-681">Az.Network</span></span>
* <span data-ttu-id="73f1f-682">Virtual Network 게이트웨이의 개인 IP에 대한 연결을 사용하도록 설정하는 cmdlet이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-682">Updated cmdlets to enable connection on private IP for Virtual Network Gateway.</span></span>
    - <span data-ttu-id="73f1f-683">'New-AzVirtualNetworkGateway'</span><span class="sxs-lookup"><span data-stu-id="73f1f-683">'New-AzVirtualNetworkGateway'</span></span>
    - <span data-ttu-id="73f1f-684">'Set-AzVirtualNetworkGateway'</span><span class="sxs-lookup"><span data-stu-id="73f1f-684">'Set-AzVirtualNetworkGateway'</span></span>
    - <span data-ttu-id="73f1f-685">'New-AzVirtualNetworkGatewayConnection'</span><span class="sxs-lookup"><span data-stu-id="73f1f-685">'New-AzVirtualNetworkGatewayConnection'</span></span>
    - <span data-ttu-id="73f1f-686">'Set-AzVirtualNetworkGatewayConnection'</span><span class="sxs-lookup"><span data-stu-id="73f1f-686">'Set-AzVirtualNetworkGatewayConnection'</span></span>
* <span data-ttu-id="73f1f-687">FQDN 기반 LocalNetworkGateways 및 VpnSites를 사용하도록 설정하는 cmdlet이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-687">Updated cmdlets to enable FQDN based LocalNetworkGateways and VpnSites</span></span>
    - <span data-ttu-id="73f1f-688">'New-AzLocalNetworkGateway'</span><span class="sxs-lookup"><span data-stu-id="73f1f-688">'New-AzLocalNetworkGateway'</span></span>
    - <span data-ttu-id="73f1f-689">'New-AzVpnSiteLink'</span><span class="sxs-lookup"><span data-stu-id="73f1f-689">'New-AzVpnSiteLink'</span></span>
* <span data-ttu-id="73f1f-690">ExpressRouteCircuitConnectionConfig(Global Reach)의 IPv6 주소 패밀리에 대한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-690">Added support for IPv6 address family in ExpressRouteCircuitConnectionConfig (Global Reach)</span></span>
    - <span data-ttu-id="73f1f-691">'Set-AzExpressRouteCircuitConnectionConfig'가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-691">Added 'Set-AzExpressRouteCircuitConnectionConfig'</span></span>
        - <span data-ttu-id="73f1f-692">IPv6CircuitConnectionProperties를 포함한 모든 기존 속성을 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-692">allows setting of all the existing properties including the IPv6CircuitConnectionProperties</span></span>
    - <span data-ttu-id="73f1f-693">'Add-AzExpressRouteCircuitConnectionConfig'가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-693">Updated 'Add-AzExpressRouteCircuitConnectionConfig'</span></span>
        - <span data-ttu-id="73f1f-694">주소 접두사의 주소 패밀리를 지정하는 또 다른 선택적 매개 변수 AddressPrefixType이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-694">Added another optional parameter AddressPrefixType to specify the address family of address prefix</span></span>
* <span data-ttu-id="73f1f-695">Virtual Network 게이트웨이 연결에서 DPD 시간 제한 설정을 사용하도록 cmdlet이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-695">Updated cmdlets to enable setting of DPD Timeout on Virtual Network Gateway Connections.</span></span>
    - <span data-ttu-id="73f1f-696">New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="73f1f-696">New-AzVirtualNetworkGatewayConnection</span></span>
    - <span data-ttu-id="73f1f-697">Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="73f1f-697">Set-AzVirtualNetworkGatewayConnection</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="73f1f-698">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="73f1f-698">Az.PolicyInsights</span></span>
* <span data-ttu-id="73f1f-699">정책 준수 검사를 트리거하기 위한 'Start-AzPolicyComplianceScan' cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-699">Added 'Start-AzPolicyComplianceScan' cmdlet for triggering policy compliance scans</span></span>
* <span data-ttu-id="73f1f-700">'Get-AzPolicyState' 출력에 정책 정의, 집합 정의 및 할당 버전이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-700">Added policy definition, set definition, and assignment versions to 'Get-AzPolicyState' output</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="73f1f-701">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="73f1f-701">Az.ServiceFabric</span></span>
* <span data-ttu-id="73f1f-702">'New-AzServiceFabricCluster' 예제의 코드 서식 및 사용 편의성이 개선되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-702">Improved code formatting and usability of 'New-AzServiceFabricCluster' examples</span></span>

#### <a name="azsql"></a><span data-ttu-id="73f1f-703">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="73f1f-703">Az.Sql</span></span>
* <span data-ttu-id="73f1f-704">'Get-AzSqlInstanceOperation' 및 'Stop-AzSqlInstanceOperation' cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-704">Added cmdlets 'Get-AzSqlInstanceOperation' and 'Stop-AzSqlInstanceOperation'</span></span>
* <span data-ttu-id="73f1f-705">VNet에서 스토리지 계정에 대한 감사가 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-705">Supported auditing to a storage account in VNet.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="73f1f-706">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="73f1f-706">Az.Storage</span></span>
* <span data-ttu-id="73f1f-707">향후 릴리스의 Azure File cmdlet 출력 변경에 대한 호환성이 손상되는 변경 공지가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-707">Added breaking change notice for Azure File cmdlets output change in a future release</span></span>
* <span data-ttu-id="73f1f-708">스토리지 계정 생성/업데이트 시 새로운 SkuName StandardGZRS, StandardRAGZRS가 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-708">Supported new SkuName StandardGZRS, StandardRAGZRS when create/update Storage account</span></span>
    - <span data-ttu-id="73f1f-709">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="73f1f-709">'New-AzStorageAccount'</span></span>
    - <span data-ttu-id="73f1f-710">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="73f1f-710">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="73f1f-711">DataLake Gen2가 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-711">Supported DataLake Gen2</span></span>
    - <span data-ttu-id="73f1f-712">'New-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="73f1f-712">'New-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="73f1f-713">'Get-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="73f1f-713">'Get-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="73f1f-714">'Get-AzDataLakeGen2ChildItem'</span><span class="sxs-lookup"><span data-stu-id="73f1f-714">'Get-AzDataLakeGen2ChildItem'</span></span>
    - <span data-ttu-id="73f1f-715">'Move-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="73f1f-715">'Move-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="73f1f-716">'Set-AzDataLakeGen2ItemAclObject'</span><span class="sxs-lookup"><span data-stu-id="73f1f-716">'Set-AzDataLakeGen2ItemAclObject'</span></span>
    - <span data-ttu-id="73f1f-717">'Update-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="73f1f-717">'Update-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="73f1f-718">'Get-AzDataLakeGen2ItemContent'</span><span class="sxs-lookup"><span data-stu-id="73f1f-718">'Get-AzDataLakeGen2ItemContent'</span></span>
    - <span data-ttu-id="73f1f-719">'Remove-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="73f1f-719">'Remove-AzDataLakeGen2Item'</span></span>

## <a name="0100-preview---april-2020"></a><span data-ttu-id="73f1f-720">0.10.0-preview - 2020년 4월</span><span class="sxs-lookup"><span data-stu-id="73f1f-720">0.10.0-preview - April 2020</span></span>
### <a name="general"></a><span data-ttu-id="73f1f-721">일반</span><span class="sxs-lookup"><span data-stu-id="73f1f-721">General</span></span>
* <span data-ttu-id="73f1f-722">이제 Az 모듈이 Azure Stack Hub에서 미리 보기로 제공됩니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-722">Az modules is now available in preview on Azure Stack Hub.</span></span> <span data-ttu-id="73f1f-723">따라서 Linux 및 macOS와의 플랫폼 간 호환성이 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-723">This allows for cross-platform compatibility with Linux and macOs.</span></span> <span data-ttu-id="73f1f-724">Azure Stack Hub는 이제 Az 모듈을 사용하여 PowerShell Core를 지원합니다. 자세한 내용은 [여기](https://aka.ms/az4AzureStack)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="73f1f-724">Azure Stack Hub now supports PowerShell core with the Az modules, more information [here](https://aka.ms/az4AzureStack)</span></span>
* <span data-ttu-id="73f1f-725">Az 모듈은 2019-03-01-hybrid 프로필을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-725">Az modules support profile 2019-03-01-hybrid:</span></span>
  - <span data-ttu-id="73f1f-726">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="73f1f-726">Az.Billing</span></span>
  - <span data-ttu-id="73f1f-727">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="73f1f-727">Az.Compute</span></span>
  - <span data-ttu-id="73f1f-728">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="73f1f-728">Az.DataBoxEdge</span></span>
  - <span data-ttu-id="73f1f-729">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="73f1f-729">Az.EventHub</span></span>
  - <span data-ttu-id="73f1f-730">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="73f1f-730">Az.IotHub</span></span>
  - <span data-ttu-id="73f1f-731">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="73f1f-731">Az.KeyVault</span></span>
  - <span data-ttu-id="73f1f-732">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="73f1f-732">Az.Monitor</span></span>
  - <span data-ttu-id="73f1f-733">Az.Network</span><span class="sxs-lookup"><span data-stu-id="73f1f-733">Az.Network</span></span>
  - <span data-ttu-id="73f1f-734">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="73f1f-734">Az.Resources</span></span>
  - <span data-ttu-id="73f1f-735">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="73f1f-735">Az.Storage</span></span>
  - <span data-ttu-id="73f1f-736">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="73f1f-736">Az.Websites</span></span>
* <span data-ttu-id="73f1f-737">Azure Stack Hub와 함께 작동하는 az용 새 PowerShell 모듈 3개(Az.Databox, Az.IotHub 및 Az.EventHub)가 도입되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-737">Three new PowerShell modules for az have been introduced that work with Azure Stack Hub, which are Az.Databox, Az.IotHub, and Az.EventHub</span></span>
* <span data-ttu-id="73f1f-738">AzureRM을 Az로 변경하는 것과 같은 사소한 변경을 수행하면 명령이 비교적 동일하게 유지됩니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-738">Commands remain relatively the same, with minor changes such as changing AzureRM to Az</span></span>
* <span data-ttu-id="73f1f-739">Azure Stack Hub에 대한 PowerShell 설명서의 업데이트된 링크는 [여기](https://aka.ms/InstallASHPowerShell)에서 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-739">Updated link to PowerShell documentation for Azure Stack Hub can be found [here](https://aka.ms/InstallASHPowerShell)</span></span>

## <a name="370---march-2020"></a><span data-ttu-id="73f1f-740">3.7.0 - 2020년 3월</span><span class="sxs-lookup"><span data-stu-id="73f1f-740">3.7.0 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="73f1f-741">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="73f1f-741">Az.Accounts</span></span>
* <span data-ttu-id="73f1f-742">로그인하지 않을 때 'Get-AzTenant'/'Get-AzDefault'/'Set-AzDefault'에서 NullReferenceException이 발생하는 문제가 해결되었습니다. [# 10292]</span><span class="sxs-lookup"><span data-stu-id="73f1f-742">Fixed 'Get-AzTenant'/'Get-AzDefault'/'Set-AzDefault' throw NullReferenceException when not login [#10292]</span></span>

#### <a name="azcompute"></a><span data-ttu-id="73f1f-743">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="73f1f-743">Az.Compute</span></span>
* <span data-ttu-id="73f1f-744">'New-AzDiskConfig' cmdlet에 다음 매개 변수를 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-744">Added the following parameters to 'New-AzDiskConfig' cmdlet:</span></span>
    - <span data-ttu-id="73f1f-745">DiskIOPSReadOnly, DiskMBpsReadOnly, MaxSharesCount, GalleryImageReference</span><span class="sxs-lookup"><span data-stu-id="73f1f-745">DiskIOPSReadOnly, DiskMBpsReadOnly, MaxSharesCount, GalleryImageReference</span></span>
* <span data-ttu-id="73f1f-746">암호화 속성이 'New-AzGalleryImageVersion'cmdlet의 대상 매개 변수에 허용되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-746">Allowed Encryption property to Target parameter of 'New-AzGalleryImageVersion' cmdlet.</span></span>
* <span data-ttu-id="73f1f-747">'Set-AzVmss'-Reimage 및 'Invoke-AzVMReimage'cmdlet에 대한 tempDisk 이슈가 해결되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-747">Fixed tempDisk issue for 'Set-AzVmss' -Reimage and 'Invoke-AzVMReimage' cmdlets.</span></span> <span data-ttu-id="73f1f-748">[#11354]</span><span class="sxs-lookup"><span data-stu-id="73f1f-748">[#11354]</span></span>
* <span data-ttu-id="73f1f-749">새로운 SAP 확장을 위해 아래 cmdlet에 대한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-749">Added support to below cmdlets for new SAP Extension</span></span>
    - <span data-ttu-id="73f1f-750">'Set-AzVMAEMExtension'</span><span class="sxs-lookup"><span data-stu-id="73f1f-750">'Set-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="73f1f-751">'Get-AzVMAEMExtension'</span><span class="sxs-lookup"><span data-stu-id="73f1f-751">'Get-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="73f1f-752">'Remove-AzVMAEMExtension'</span><span class="sxs-lookup"><span data-stu-id="73f1f-752">'Remove-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="73f1f-753">'Update-AzVMAEMExtension'</span><span class="sxs-lookup"><span data-stu-id="73f1f-753">'Update-AzVMAEMExtension'</span></span>
* <span data-ttu-id="73f1f-754">도움말 문서의 예제에서 오류가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-754">Fixed errors in examples of help document</span></span>
* <span data-ttu-id="73f1f-755">VM PowerState의 정확한 문자열 값을 테이블 형식으로 표시했습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-755">Showed the exact string value for VM PowerState in the table format.</span></span>
* <span data-ttu-id="73f1f-756">'New-AzVmssConfig': SinglePlacementGroup이 비활성화된 경우 AutomaticRepairs 속성의 직렬화가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-756">'New-AzVmssConfig': fixed serialization of AutomaticRepairs property when SinglePlacementGroup is disabled.</span></span> <span data-ttu-id="73f1f-757">[#11257]</span><span class="sxs-lookup"><span data-stu-id="73f1f-757">[#11257]</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="73f1f-758">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="73f1f-758">Az.DataFactory</span></span>
* <span data-ttu-id="73f1f-759">ADF .Net SDK 버전이 4.8.0으로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-759">Updated ADF .Net SDK version to 4.8.0</span></span>
* <span data-ttu-id="73f1f-760">재실행을 지원하기 위해 'Invoke-AzDataFactoryV2Pipeline' 명령에 선택적 매개 변수를 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-760">Added optional parameters to 'Invoke-AzDataFactoryV2Pipeline' command to support rerun</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="73f1f-761">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="73f1f-761">Az.DataLakeStore</span></span>
* <span data-ttu-id="73f1f-762">'Export-AzDataLakeStoreItem' 및 'Import-AzDataLakeStoreItem'에 대해 호환성이 손상되는 변경 설명을 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-762">Added breaking change description for 'Export-AzDataLakeStoreItem' and 'Import-AzDataLakeStoreItem'</span></span>
* <span data-ttu-id="73f1f-763">'New-AzDataLakeStoreItem', 'Add-AzDAtaLakeStoreItemContent' 및 'Get-AzDAtaLakeStoreItemContent'에 대한 바이트 인코딩 옵션이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-763">Added option of Byte encoding for 'New-AzDataLakeStoreItem', 'Add-AzDAtaLakeStoreItemContent', and 'Get-AzDAtaLakeStoreItemContent'</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="73f1f-764">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="73f1f-764">Az.HDInsight</span></span>
* <span data-ttu-id="73f1f-765">클러스터 생성 시 최소 지원 TLS 버전 지정이 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-765">Supported specifying minimal supported TLS version when creating cluster.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="73f1f-766">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="73f1f-766">Az.IotHub</span></span>
* <span data-ttu-id="73f1f-767">디바이스별 분산 설정을 관리하기 위한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-767">Added support to manage distributed settings per-device.</span></span> <span data-ttu-id="73f1f-768">새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-768">New Cmdlets are:</span></span>
    - <span data-ttu-id="73f1f-769">'Get-AzIotHubDistributedTracing'</span><span class="sxs-lookup"><span data-stu-id="73f1f-769">'Get-AzIotHubDistributedTracing'</span></span>
    - <span data-ttu-id="73f1f-770">'Set-AzIotHubDistributedTracing'</span><span class="sxs-lookup"><span data-stu-id="73f1f-770">'Set-AzIotHubDistributedTracing'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="73f1f-771">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="73f1f-771">Az.KeyVault</span></span>
* <span data-ttu-id="73f1f-772">'New-AzKeyVault'에 대해 호환성이 손상되는 변경 속성이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-772">Added breaking change attributes to 'New-AzKeyVault'</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="73f1f-773">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="73f1f-773">Az.Monitor</span></span>
* <span data-ttu-id="73f1f-774">'New-AzScheduledQueryRuleLogMetricTrigger'에 대한 설명서가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-774">Updated documentation for 'New-AzScheduledQueryRuleLogMetricTrigger'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="73f1f-775">Az.Network</span><span class="sxs-lookup"><span data-stu-id="73f1f-775">Az.Network</span></span>
* <span data-ttu-id="73f1f-776">교차 테넌트 VirtualHubVnetConnections를 허용하도록 cmdlet이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-776">Updated cmdlets to allow cross-tenant VirtualHubVnetConnections</span></span>
    - <span data-ttu-id="73f1f-777">'New-AzVirtualHubVnetConnection'</span><span class="sxs-lookup"><span data-stu-id="73f1f-777">'New-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="73f1f-778">'Update-AzVirtualHubVnetConnection'</span><span class="sxs-lookup"><span data-stu-id="73f1f-778">'Update-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="73f1f-779">'New-AzVirtualHub'</span><span class="sxs-lookup"><span data-stu-id="73f1f-779">'New-AzVirtualHub'</span></span>
    - <span data-ttu-id="73f1f-780">'Update-AzVirtualHub'</span><span class="sxs-lookup"><span data-stu-id="73f1f-780">'Update-AzVirtualHub'</span></span>
* <span data-ttu-id="73f1f-781">SQL Management SDK 종속성이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-781">Removed Sql Management SDK dependency</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="73f1f-782">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="73f1f-782">Az.PolicyInsights</span></span>
* <span data-ttu-id="73f1f-783">오류 메시지가 향상되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-783">Improved error messages</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="73f1f-784">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="73f1f-784">Az.RecoveryServices</span></span>
* <span data-ttu-id="73f1f-785">Azure Site Recovery는 Azure 디스크 암호화 Virtual Machines에 대한 VM 속성을 다시 보호하고 업데이트하는 기능을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-785">Azure Site Recovery added support for doing reprotect and updated vm properties for Azure disk encrypted Virtual Machines.</span></span>
* <span data-ttu-id="73f1f-786">Azure Site Recovery VmwareToAzure 속성 DR 모니터링이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-786">Added Azure Site Recovery VmwareToAzure properties DR monitoring</span></span>
* <span data-ttu-id="73f1f-787">Azure Backup은 실패한 항목에 대한 정책 업데이트 재시도 지원을 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-787">Azure Backup added support for retrying policy update for failed items.</span></span>
* <span data-ttu-id="73f1f-788">Azure Backup은 백업 및 복원 중에 디스크 제외 설정에 대한 지원을 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-788">Azure Backup Added support for disk exclusion settings during backup and restore.</span></span>
* <span data-ttu-id="73f1f-789">Azure Backup은 AzureFileShare에서 여러 파일/폴더 복원을 위한 지원을 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-789">Azure Backup Added Support for Restoring Multiple files/folders in AzureFileShare</span></span>
* <span data-ttu-id="73f1f-790">Azure Backup은 IaasVM 정책을 업데이트하는 동안 사용자 지정 리소스 그룹 지원에 대한 지원을 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-790">Azure Backup Added support for User-specified Resourcegroup support while updating IaasVM Policy</span></span>

#### <a name="azresources"></a><span data-ttu-id="73f1f-791">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="73f1f-791">Az.Resources</span></span>
* <span data-ttu-id="73f1f-792">'Get-AzResource -ResourceGroupName -Name -ExpandProperties -ResourceType'이 기본 apiVersion 대신 실제 apiVersion 리소스를 사용하도록 수정했습니다. [# 11267]</span><span class="sxs-lookup"><span data-stu-id="73f1f-792">Fixed 'Get-AzResource -ResourceGroupName -Name -ExpandProperties -ResourceType' to use actual apiVersion of resources instead of default apiVersion [#11267]</span></span>
* <span data-ttu-id="73f1f-793">오류 시나리오에 대해 correlationId 로깅이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-793">Added correlationId logging for error scenarios</span></span>
* <span data-ttu-id="73f1f-794">작은 설명서가 'Get-AzResourceLock'으로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-794">Small documentation change to 'Get-AzResourceLock'.</span></span> <span data-ttu-id="73f1f-795">예제가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-795">Added example.</span></span>
* <span data-ttu-id="73f1f-796">'Get-AzADUser'의 매개 변수 값에서 작은 따옴표를 이스케이프 처리하였습니다. [# 11317]</span><span class="sxs-lookup"><span data-stu-id="73f1f-796">Escaped single quote in parameter value of 'Get-AzADUser' [#11317]</span></span>
* <span data-ttu-id="73f1f-797">배포 스크립트('Get-AzDeploymentScript', 'Get-AzDeploymentScriptLog', 'Save-AzDeploymentScriptLog', 'Remove-AzDeploymentScript')에 대한 새로운 cmdlet 추가가 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-797">Added new cmdlets for Deployment Scripts ('Get-AzDeploymentScript', 'Get-AzDeploymentScriptLog', 'Save-AzDeploymentScriptLog', 'Remove-AzDeploymentScript')</span></span>

#### <a name="azsql"></a><span data-ttu-id="73f1f-798">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="73f1f-798">Az.Sql</span></span>
* <span data-ttu-id="73f1f-799">'Invoke-AzSqlDatabaseFailover'에 읽기 가능한 보조 매개 변수를 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-799">Added readable secondary parameter to 'Invoke-AzSqlDatabaseFailover'</span></span>
* <span data-ttu-id="73f1f-800">'Disable-AzSqlServerActiveDirectoryOnlyAuthentication' cmdlet을 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-800">Added cmdlet 'Disable-AzSqlServerActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="73f1f-801">데이터베이스에서 열을 분류할 때 저장된 민감도 순위입니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-801">Saved sensitivity rank when classifying columns in the database.</span></span>

#### <a name="azsupport"></a><span data-ttu-id="73f1f-802">Az.Support</span><span class="sxs-lookup"><span data-stu-id="73f1f-802">Az.Support</span></span>
* <span data-ttu-id="73f1f-803">'Az.Support' 모듈의 일반 공급</span><span class="sxs-lookup"><span data-stu-id="73f1f-803">General availability of 'Az.Support' module</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="73f1f-804">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="73f1f-804">Az.Websites</span></span>
* <span data-ttu-id="73f1f-805">아래의 새로운 cmdlet을 통해 webapp 트래픽 라우팅 규칙을 사용하는 작업에 대한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-805">Added support for working with webapp Traffic Routing Rules via below new cmdlets</span></span>
    - <span data-ttu-id="73f1f-806">'Get-AzWebAppTrafficRouting'</span><span class="sxs-lookup"><span data-stu-id="73f1f-806">'Get-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="73f1f-807">'Update-AzWebAppTrafficRouting'</span><span class="sxs-lookup"><span data-stu-id="73f1f-807">'Update-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="73f1f-808">'Add-AzWebAppTrafficRouting'</span><span class="sxs-lookup"><span data-stu-id="73f1f-808">'Add-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="73f1f-809">'Remove-AzWebAppTrafficRouting'</span><span class="sxs-lookup"><span data-stu-id="73f1f-809">'Remove-AzWebAppTrafficRouting'</span></span>

## <a name="361---march-2020"></a><span data-ttu-id="73f1f-810">3.6.1 - 2020년 3월</span><span class="sxs-lookup"><span data-stu-id="73f1f-810">3.6.1 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="73f1f-811">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="73f1f-811">Az.Accounts</span></span>
* <span data-ttu-id="73f1f-812">'피드백 보내기'에서 Azure PowerShell 설문 조사 페이지가 열립니다[#11020].</span><span class="sxs-lookup"><span data-stu-id="73f1f-812">Open Azure PowerShell survey page in 'Send-Feedback' [#11020]</span></span>
* <span data-ttu-id="73f1f-813">'오류 해결'에서 Azure PowerShell 설문 조사 URL이 표시됩니다[#11021].</span><span class="sxs-lookup"><span data-stu-id="73f1f-813">Display Azure PowerShell survey URL in 'Resolve-Error' [#11021]</span></span>
* <span data-ttu-id="73f1f-814">UserAgent에서 Az 버전이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-814">Added Az version in UserAgent</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="73f1f-815">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="73f1f-815">Az.ApiManagement</span></span>
* <span data-ttu-id="73f1f-816">DeveloperPortal 엔드포인트에서 사용자 지정 도메인을 검색하고 구성하기 위한 지원이 추가되었습니다[#11007].</span><span class="sxs-lookup"><span data-stu-id="73f1f-816">Added support for retrieving and configuring Custom Domain on the DeveloperPortal Endpoint [#11007]</span></span>
* <span data-ttu-id="73f1f-817">Json 형식의 API 정의를 다운로드하기 위한 'Export-AzApiManagementApi' 지원이 추가되었습니다[#9987].</span><span class="sxs-lookup"><span data-stu-id="73f1f-817">'Export-AzApiManagementApi' Added support for downloading Api Definition in Json format [#9987]</span></span>
* <span data-ttu-id="73f1f-818">Json 문서에서 OpenApi 3.0 정의를 가져오기 위한 'Import-AzApiManagementApi' 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-818">'Import-AzApiManagementApi' Added support for importing OpenApi 3.0 definition from Json document</span></span>
* <span data-ttu-id="73f1f-819">AAD B2C 공급자에 대한 '로그인 테넌트'를 구성하기 위한 'New-AzApiManagementIdentityProvider' 및 'Set-AzApiManagementIdentityProvider' 지원이 추가되었습니다[#9784].</span><span class="sxs-lookup"><span data-stu-id="73f1f-819">'New-AzApiManagementIdentityProvider' and 'Set-AzApiManagementIdentityProvider' Added support for configuring 'Signin Tenant' for AAD B2C Provider [#9784]</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="73f1f-820">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="73f1f-820">Az.DataLakeStore</span></span>
* <span data-ttu-id="73f1f-821">csproj 및 psd1에서 System.Buffers에 대한 참조가 명시적으로 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-821">Added reference to System.Buffers explicitly in csproj and psd1.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="73f1f-822">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="73f1f-822">Az.IotHub</span></span>
* <span data-ttu-id="73f1f-823">Iot Hub에서 디바이스를 관리하기 위한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-823">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="73f1f-824">새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-824">New Cmdlets are:</span></span>
    - <span data-ttu-id="73f1f-825">'Add-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="73f1f-825">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="73f1f-826">'Get-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="73f1f-826">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="73f1f-827">'Remove-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="73f1f-827">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="73f1f-828">'Set-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="73f1f-828">'Set-AzIotHubDevice'</span></span>
* <span data-ttu-id="73f1f-829">Iot Hub의 대상 IoT 디바이스에서 모듈을 관리하기 위한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-829">Added support to manage modules on a target Iot device in an Iot Hub.</span></span> <span data-ttu-id="73f1f-830">새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-830">New Cmdlets are:</span></span>
    - <span data-ttu-id="73f1f-831">'Add-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="73f1f-831">'Add-AzIotHubModule'</span></span>
    - <span data-ttu-id="73f1f-832">'Get-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="73f1f-832">'Get-AzIotHubModule'</span></span>
    - <span data-ttu-id="73f1f-833">'Remove-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="73f1f-833">'Remove-AzIotHubModule'</span></span>
    - <span data-ttu-id="73f1f-834">'Set-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="73f1f-834">'Set-AzIotHubModule'</span></span>
* <span data-ttu-id="73f1f-835">Iot Hub에서 대상 IoT 디바이스에 대한 연결 문자열을 가져오는 cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-835">Added cmdlet to get the connection string of a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="73f1f-836">Iot Hub에서 대상 IoT 디바이스의 모듈에 대한 연결 문자열을 가져오는 cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-836">Added cmdlet to get the connection string of a module on a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="73f1f-837">IoT 디바이스의 부모 디바이스를 가져오거나 설정하기 위한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-837">Added support to get/set parent device of an IoT device.</span></span> <span data-ttu-id="73f1f-838">새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-838">New Cmdlets are:</span></span>
    - <span data-ttu-id="73f1f-839">'Get-AzIotHubDeviceParent'</span><span class="sxs-lookup"><span data-stu-id="73f1f-839">'Get-AzIotHubDeviceParent'</span></span>
    - <span data-ttu-id="73f1f-840">'Set-AzIotHubDeviceParent'</span><span class="sxs-lookup"><span data-stu-id="73f1f-840">'Set-AzIotHubDeviceParent'</span></span>
* <span data-ttu-id="73f1f-841">디바이스 부모-자식 관계를 관리하기 위한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-841">Added support to manage device parent-child relationship.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="73f1f-842">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="73f1f-842">Az.Monitor</span></span>
* <span data-ttu-id="73f1f-843">'Get-AzMetricDefinition'에 대한 출력 값이 수정되었습니다[#9714].</span><span class="sxs-lookup"><span data-stu-id="73f1f-843">Fixed output value for 'Get-AzMetricDefinition' [#9714]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="73f1f-844">Az.Network</span><span class="sxs-lookup"><span data-stu-id="73f1f-844">Az.Network</span></span>
* <span data-ttu-id="73f1f-845">SQL Management SDK가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-845">Updated Sql Management SDK.</span></span>
* <span data-ttu-id="73f1f-846">PrivateLinkServiceConnectionState 클래스의 명명 차이 문제가 해결되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-846">Fixed a naming-difference issue in PrivateLinkServiceConnectionState class.</span></span>
    - <span data-ttu-id="73f1f-847">ActionsRequired 필드가 ActionRequired에 매핑됩니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-847">Mapping the field ActionsRequired to ActionRequired.</span></span>
* <span data-ttu-id="73f1f-848">PublicNetworkAccess가 'New-AzSqlServer' 및 'Set-AzSqlServer'에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-848">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>

#### <a name="azresources"></a><span data-ttu-id="73f1f-849">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="73f1f-849">Az.Resources</span></span>
* <span data-ttu-id="73f1f-850">Get-AzRoleAssignment'의 null 참조 버그가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-850">Fixed for null reference bug in 'Get-AzRoleAssignment'</span></span>
* <span data-ttu-id="73f1f-851">'Remove-AzADGroup'에서 '-Force' 및 '-PassThru' 스위치가 선택적으로 표시됩니다[#10849].</span><span class="sxs-lookup"><span data-stu-id="73f1f-851">Marked switch '-Force' and '-PassThru' optional in 'Remove-AzADGroup' [#10849]</span></span>
* <span data-ttu-id="73f1f-852">'Remove-AzADGroup'에서 'MailNickname'이 반환되지 않는 문제가 해결되었습니다[#11167].</span><span class="sxs-lookup"><span data-stu-id="73f1f-852">Fixed issue that 'MailNickname' doesn't return in 'Remove-AzADGroup' [#11167]</span></span>
* <span data-ttu-id="73f1f-853">'Remove-AzADGroup' 파이프 작업이 작동하지 않는 문제가 해결되었습니다[#11171].</span><span class="sxs-lookup"><span data-stu-id="73f1f-853">Fixed issue that 'Remove-AzADGroup' pipe operation doesn't work [#11171]</span></span>
* <span data-ttu-id="73f1f-854">GetAzureRoleAssignmentCommand의 null 참조 버그가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-854">Fixed for null reference bug in GetAzureRoleAssignmentCommand</span></span>
* <span data-ttu-id="73f1f-855">예정된 정책 cmdlet 변경에 대한 호환성이 손상되는 변경 특성이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-855">Added breaking change attributes for upcoming changes to policy cmdlets</span></span>
* <span data-ttu-id="73f1f-856">서버 쪽에서 리소스 그룹 태그 필터링을 수행하도록 'Get-AzResourceGroup'이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-856">Updated 'Get-AzResourceGroup' to perform resource group tag filtering on server-side</span></span>
* <span data-ttu-id="73f1f-857">-ResourceId를 허용하도록 Tag cmdlet이 확장되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-857">Extended Tag cmdlets to accept -ResourceId</span></span>
    - <span data-ttu-id="73f1f-858">Get-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="73f1f-858">Get-AzTag -ResourceId</span></span>
    - <span data-ttu-id="73f1f-859">New-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="73f1f-859">New-AzTag -ResourceId</span></span>
    - <span data-ttu-id="73f1f-860">Remove-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="73f1f-860">Remove-AzTag -ResourceId</span></span>
* <span data-ttu-id="73f1f-861">새 Tag cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-861">Added new Tag cmdlet</span></span>
    - <span data-ttu-id="73f1f-862">Update-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="73f1f-862">Update-AzTag -ResourceId</span></span>
* <span data-ttu-id="73f1f-863">SDK 3.3.0에서 ScopedDeployment를 가져왔습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-863">Brought ScopedDeployment from SDK 3.3.0</span></span>

#### <a name="azsql"></a><span data-ttu-id="73f1f-864">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="73f1f-864">Az.Sql</span></span>
* <span data-ttu-id="73f1f-865">PublicNetworkAccess가 'New-AzSqlServer' 및 'Set-AzSqlServer'에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-865">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>
* <span data-ttu-id="73f1f-866">관리형 데이터베이스에 대한 장기 보존 백업 구성에 대한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-866">Added support for Long Term Retention backup configuration for Managed Databases</span></span>
    - <span data-ttu-id="73f1f-867">관리형 데이터베이스에서 LTR 정책을 가져오거나 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-867">Get/Set LTR policy on a managed database</span></span>
    - <span data-ttu-id="73f1f-868">관리형 데이터베이스, 관리형 인스턴스 또는 위치를 기준으로 LTR 백업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-868">Get LTR backup(s) by managed database, managed instance, or by location</span></span>
    - <span data-ttu-id="73f1f-869">LTR 백업을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-869">Remove an LTR backup</span></span>
    - <span data-ttu-id="73f1f-870">LTR 백업을 복원하여 새 관리형 데이터베이스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-870">Restore an LTR backup to create a new managed database</span></span>
* <span data-ttu-id="73f1f-871">MinimalTlsVersion이 New-AzSqlServer 및 Set-AzSqlServer에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-871">Added MinimalTlsVersion to New-AzSqlServer and Set-AzSqlServer</span></span>
* <span data-ttu-id="73f1f-872">MinimalTlsVersion을 New-AzSqlInstance 및 Set-AzSqlInstance에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-872">Added MinimalTlsVersion to New-AzSqlInstance and Set-AzSqlInstance</span></span>
* <span data-ttu-id="73f1f-873">Az.Network에 대한 SQL SDK 버전이 높아졌습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-873">Bumped SQL SDK version for Az.Network</span></span>

#### <a name="azstorage"></a><span data-ttu-id="73f1f-874">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="73f1f-874">Az.Storage</span></span>
* <span data-ttu-id="73f1f-875">ImmutabilityPolicy에서 AllowProtectedAppendWrite가 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-875">Supported AllowProtectedAppendWrite in ImmutabilityPolicy</span></span>
    - <span data-ttu-id="73f1f-876">'Set-AzRmStorageContainerImmutabilityPolicy'</span><span class="sxs-lookup"><span data-stu-id="73f1f-876">'Set-AzRmStorageContainerImmutabilityPolicy'</span></span>
* <span data-ttu-id="73f1f-877">이후 릴리스에서 AzureStorageTable 형식 변경에 대한 호환성이 손상되는 변경 경고 메시지가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-877">Added breaking change warning message for AzureStorageTable type change in a future release</span></span>
    - <span data-ttu-id="73f1f-878">'New-AzStorageTable'</span><span class="sxs-lookup"><span data-stu-id="73f1f-878">'New-AzStorageTable'</span></span>
    - <span data-ttu-id="73f1f-879">'Get-AzStorageTable'</span><span class="sxs-lookup"><span data-stu-id="73f1f-879">'Get-AzStorageTable'</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="73f1f-880">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="73f1f-880">Az.Websites</span></span>
* <span data-ttu-id="73f1f-881">'New-AzAppServicePlan' 및 'Set-AzAppServicePlan'에 대한 Tag 매개 변수가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-881">Added Tag parameter for 'New-AzAppServicePlan' and 'Set-AzAppServicePlan'</span></span>
* <span data-ttu-id="73f1f-882">웹 사이트에 사용자 지정 도메인을 추가할 때 예외가 throw되면 cmdlet 실행을 중지합니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-882">Stop cmdlet execution if an exception is thrown when adding a custom domain to a website</span></span>
* <span data-ttu-id="73f1f-883">App Service 계획과 동일한 리소스 그룹에 속하지 않는 App Services에 대한 작업을 수행하기 위한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-883">Added support to perform operations for App Services not in the same resource group as the App Service Plan</span></span>
* <span data-ttu-id="73f1f-884">다른 리소스 그룹의 WebApp/Function에 대한 액세스 제한이 적용되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-884">Applied access restriction to WebApp/Function in different resource groups</span></span>
* <span data-ttu-id="73f1f-885">WebAppSlot에 대한 사용자 지정 호스트 이름을 설정하는 문제가 해결되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-885">Fixed issue to set custom hostnames for WebAppSlots</span></span>

## <a name="350---february-2020"></a><span data-ttu-id="73f1f-886">3.5.0 - 2020년 2월</span><span class="sxs-lookup"><span data-stu-id="73f1f-886">3.5.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="73f1f-887">마지막 주 릴리스 이후의 주요 사항</span><span class="sxs-lookup"><span data-stu-id="73f1f-887">Highlights since the last major release</span></span>
* <span data-ttu-id="73f1f-888">클라이언트 쪽 원격 분석이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-888">Updated client side telemetry.</span></span>
* <span data-ttu-id="73f1f-889">디바이스 관리를 지원하는 cmdlet이 Az.IotHub에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-889">Az.IotHub added cmdlets to support to manage devices.</span></span>
* <span data-ttu-id="73f1f-890">가용성 그룹 수신기에 대한 cmdlet이 Az.SqlVirtualMachine에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-890">Az.SqlVirtualMachine added cmdlets for Availability Group Listener.</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="73f1f-891">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="73f1f-891">Az.Accounts</span></span>
* <span data-ttu-id="73f1f-892">SubscriptionId, TenantId 및 실행 시간이 클라이언트 쪽 원격 분석에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-892">Added SubscriptionId, TenantId, and execution time into data of client side telemetry</span></span>

#### <a name="azautomation"></a><span data-ttu-id="73f1f-893">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="73f1f-893">Az.Automation</span></span>
* <span data-ttu-id="73f1f-894">'New-AzAutomationSoftwareUpdateConfiguration' 참조 설명서의 예제 1에 있는 오타가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-894">Fixed typo in Example 1 in reference documentation for 'New-AzAutomationSoftwareUpdateConfiguration'</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="73f1f-895">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="73f1f-895">Az.CognitiveServices</span></span>
* <span data-ttu-id="73f1f-896">SDK가 7.0으로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-896">Updated SDK to 7.0</span></span>
* <span data-ttu-id="73f1f-897">서버 응답 본문이 비어 있는 경우 표시되는 오류 메시지가 향상되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-897">Improved error message when server responses empty body</span></span>

#### <a name="azcompute"></a><span data-ttu-id="73f1f-898">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="73f1f-898">Az.Compute</span></span>
* <span data-ttu-id="73f1f-899">업데이트하는 동안 빈 값이 ProximityPlacementGroupId에 허용되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-899">Allowed empty value for ProximityPlacementGroupId during update</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="73f1f-900">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="73f1f-900">Az.FrontDoor</span></span>
* <span data-ttu-id="73f1f-901">WAF에서 사용할 수 있는 관리형 규칙 정의를 가져오는 cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-901">Added cmdlet to get managed rule definitions that can be used in WAF</span></span>

#### <a name="aziothub"></a><span data-ttu-id="73f1f-902">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="73f1f-902">Az.IotHub</span></span>
* <span data-ttu-id="73f1f-903">Iot Hub에서 디바이스를 관리하기 위한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-903">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="73f1f-904">새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-904">New Cmdlets are:</span></span>
    - <span data-ttu-id="73f1f-905">'Add-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="73f1f-905">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="73f1f-906">'Get-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="73f1f-906">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="73f1f-907">'Remove-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="73f1f-907">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="73f1f-908">'Set-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="73f1f-908">'Set-AzIotHubDevice'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="73f1f-909">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="73f1f-909">Az.KeyVault</span></span>
* <span data-ttu-id="73f1f-910">Add-AzKeyVaultKey.md에 대해 중복된 텍스트가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-910">Fixed duplicated text for Add-AzKeyVaultKey.md</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="73f1f-911">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="73f1f-911">Az.Monitor</span></span>
* <span data-ttu-id="73f1f-912">Get-AzLog cmdlet에 대한 설명이 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-912">Fixed description of the Get-AzLog cmdlet.</span></span>
* <span data-ttu-id="73f1f-913">ActionGroupId라는 새 매개 변수가 'New-AzMetricAlertRuleV2' 명령에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-913">A new parameter called ActionGroupId was added to 'New-AzMetricAlertRuleV2' command.</span></span>
    - <span data-ttu-id="73f1f-914">사용자는 ActionGroupId(string) 또는 ActionGorup(ActivityLogAlertActionGroup) 중 하나를 제공할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-914">The user can provide either ActionGroupId(string) or ActionGorup(ActivityLogAlertActionGroup).</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="73f1f-915">Az.Network</span><span class="sxs-lookup"><span data-stu-id="73f1f-915">Az.Network</span></span>
* <span data-ttu-id="73f1f-916">'New-AzPrivateLinkService' cmdlet의 '-EnableProxyProtocol' 매개 변수에 대한 하나의 추가 매개 변수 메모가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-916">Added one extra parameter note for parameter '-EnableProxyProtocol' for 'New-AzPrivateLinkService' cmdlet.</span></span>
* <span data-ttu-id="73f1f-917">Start-AzVirtualNetworkGatewayConnectionPacketCapture.md 및 Start-AzVirtualnetworkGatewayPacketCapture.md의 FilterData 예제가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-917">Fixed FilterData example in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="73f1f-918">Start-AzVirtualNetworkGatewayConnectionPacketCapture.md 및 Start-AzVirtualnetworkGatewayPacketCapture.md의 모든 내부 및 외부 패킷을 캡처하는 패킷 캡처 예제가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-918">Added Packet Capture example for capture all inner and outer packets in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="73f1f-919">VNet 방화벽에서 Azure Firewall 정책이 지원됩니다</span><span class="sxs-lookup"><span data-stu-id="73f1f-919">Supported Azure Firewall Policy on VNet Firewalls</span></span>
    - <span data-ttu-id="73f1f-920">새로 추가된 cmdlet이 없습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-920">No new cmdlets are added.</span></span> <span data-ttu-id="73f1f-921">VNet 방화벽에서 방화벽 정책 제한이 완화되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-921">Relaxing the restriction for firewall policy on VNet firewalls</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="73f1f-922">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="73f1f-922">Az.RecoveryServices</span></span>
* <span data-ttu-id="73f1f-923">SQL Database에 대한 파일로 복원 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-923">Added Support for Restore-as-files for SQL Databases.</span></span>

#### <a name="azresources"></a><span data-ttu-id="73f1f-924">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="73f1f-924">Az.Resources</span></span>
* <span data-ttu-id="73f1f-925">템플릿 배포 cmdlet이 리팩터링되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-925">Refactored template deployment cmdlets</span></span>
    - <span data-ttu-id="73f1f-926">관리 그룹에서 배포를 관리하는 새 \*-AzManagementGroupDeployment cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-926">Added new cmdlets for managing deployments at management group: \*-AzManagementGroupDeployment</span></span>
    - <span data-ttu-id="73f1f-927">테넌트 범위에서 배포를 관리하는 새 \*-AzTenantDeployment cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-927">Added new cmdlets for managing deployments at tenant scope: \*-AzTenantDeployment</span></span>
    - <span data-ttu-id="73f1f-928">구독 범위에서 구체적으로 작동하도록 \*-AzDeployment cmdlet이 리팩터링되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-928">Refactored \*-AzDeployment cmdlets to work specifically at subscription scope</span></span>
    - <span data-ttu-id="73f1f-929">\*-AzDeployment cmdlet에 대한 \*-AzSubscriptionDeployment 별칭이 만들어졌습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-929">Created aliases \*-AzSubscriptionDeployment for \*-AzDeployment cmdlets</span></span>
* <span data-ttu-id="73f1f-930">'AvailableToOtherTenants' 매개 변수가 설정되지 않는 'Update-AzADApplication'이 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-930">Fixed 'Update-AzADApplication' when parameter 'AvailableToOtherTenants' is not set</span></span>
* <span data-ttu-id="73f1f-931">AmbiguousParameterSetException을 방지하기 위해 ApplicationObjectWithoutCredentialParameterSet이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-931">Removed ApplicationObjectWithoutCredentialParameterSet to avoid AmbiguousParameterSetException.</span></span>
* <span data-ttu-id="73f1f-932">도움말 파일이 다시 생성되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-932">Regenerated help files</span></span>

#### <a name="azsql"></a><span data-ttu-id="73f1f-933">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="73f1f-933">Az.Sql</span></span>
* <span data-ttu-id="73f1f-934">Managed Instance에서 구독 간 특정 시점 복원에 대한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-934">Added support for cross subscription point in time restore on Managed Instances.</span></span>
* <span data-ttu-id="73f1f-935">기존 SQL Managed Instance 하드웨어 생성 변경에 대한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-935">Added support for changing existing Sql Managed Instance hardware generation</span></span>
* <span data-ttu-id="73f1f-936">'Update-AzSqlServerVulnerabilityAssessmentSetting' 도움말 예제(매개 변수/속성 출력 -EmailAdmins)가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-936">Fixed 'Update-AzSqlServerVulnerabilityAssessmentSetting' help examples: parameter/property output - EmailAdmins</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="73f1f-937">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="73f1f-937">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="73f1f-938">가용성 그룹 수신기에 대한 cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-938">Added cmdlets for Availability Group Listener</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="73f1f-939">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="73f1f-939">Az.StorageSync</span></span>
* <span data-ttu-id="73f1f-940">'Invoke-AzStorageSyncCompatibilityCheck'에서 지원되는 문자 세트가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-940">Updated supported character sets in 'Invoke-AzStorageSyncCompatibilityCheck'.</span></span>

## <a name="340---february-2020"></a><span data-ttu-id="73f1f-941">3.4.0 - 2020년 2월</span><span class="sxs-lookup"><span data-stu-id="73f1f-941">3.4.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="73f1f-942">마지막 주 릴리스 이후의 주요 사항</span><span class="sxs-lookup"><span data-stu-id="73f1f-942">Highlights since the last major release</span></span>
* <span data-ttu-id="73f1f-943">Az. CosmosDB 초기 버전 0.1.0 출시</span><span class="sxs-lookup"><span data-stu-id="73f1f-943">Az.CosmosDB initial version 0.1.0 released</span></span>
* <span data-ttu-id="73f1f-944">Az.Network ConnectionMonitor V2 지원 추가</span><span class="sxs-lookup"><span data-stu-id="73f1f-944">Az.Network ConnectionMonitor V2 support added</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="73f1f-945">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="73f1f-945">Az.Accounts</span></span>
* <span data-ttu-id="73f1f-946">AzureRmContext.json을 사용할 수 없을 때 컨텍스트 자동 저장 사용 안 함</span><span class="sxs-lookup"><span data-stu-id="73f1f-946">Disable context auto saving when AzureRmContext.json not available</span></span>
* <span data-ttu-id="73f1f-947">Azure Powershell Common 참조를 1.3.5-preview로 업데이트</span><span class="sxs-lookup"><span data-stu-id="73f1f-947">Update the reference to Azure Powershell Common to 1.3.5-preview</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="73f1f-948">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="73f1f-948">Az.ApiManagement</span></span>
* <span data-ttu-id="73f1f-949">**Get-AzApiManagementApiSchema** API와 연결된 Open-Api 스키마 가져오기 수정   https://github.com/Azure/azure-powershell/issues/10626</span><span class="sxs-lookup"><span data-stu-id="73f1f-949">**Get-AzApiManagementApiSchema** Fixed getting Open-Api Schema associated with an API   https://github.com/Azure/azure-powershell/issues/10626</span></span>
* <span data-ttu-id="73f1f-950">**New-AzApiManagementProduct**\* 및 **Set-AzApiManagementProduct**</span><span class="sxs-lookup"><span data-stu-id="73f1f-950">**New-AzApiManagementProduct**\* and **Set-AzApiManagementProduct**</span></span>
  - <span data-ttu-id="73f1f-951">https://github.com/Azure/azure-powershell/issues/10472 설명서 수정</span><span class="sxs-lookup"><span data-stu-id="73f1f-951">Fix documentation for https://github.com/Azure/azure-powershell/issues/10472</span></span>
* <span data-ttu-id="73f1f-952">**Set-AzApiManagementApi** cmdlet을 사용하여 ServiceUrl을 업데이트하는 방법을 보여주는 예제 추가</span><span class="sxs-lookup"><span data-stu-id="73f1f-952">**Set-AzApiManagementApi** Added example to show how to update the ServiceUrl using the cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="73f1f-953">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="73f1f-953">Az.Compute</span></span>
* <span data-ttu-id="73f1f-954">VM 이름을 사용하지 않고 Get-AzVM -Status를 수행할 때 제한을 피하기 위해 VM 상태 수를 100개로 제한</span><span class="sxs-lookup"><span data-stu-id="73f1f-954">Limit the number of VM status to 100 to avoid throttling when Get-AzVM -Status is performed without VM name.</span></span>
* <span data-ttu-id="73f1f-955">Update-AzDiskEncryptionSet cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="73f1f-955">Add Update-AzDiskEncryptionSet cmdlet</span></span>
* <span data-ttu-id="73f1f-956">다음 cmdlet에 EncryptionType 및 DiskEncryptionSetId 매개 변수 추가:</span><span class="sxs-lookup"><span data-stu-id="73f1f-956">Add EncryptionType and DiskEncryptionSetId parameters to the following cmdlets:</span></span>
    - <span data-ttu-id="73f1f-957">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="73f1f-957">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span></span>
* <span data-ttu-id="73f1f-958">Get-AzProximityPlacementGroup cmdlet에 ColocationStatus 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="73f1f-958">Add ColocationStatus parameter to Get-AzProximityPlacementGroup cmdlet.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="73f1f-959">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="73f1f-959">Az.DataFactory</span></span>
* <span data-ttu-id="73f1f-960">ADF .Net SDK 버전을 4.7.0으로 업데이트</span><span class="sxs-lookup"><span data-stu-id="73f1f-960">Update ADF .Net SDK version to 4.7.0</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="73f1f-961">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="73f1f-961">Az.DeploymentManager</span></span>
* <span data-ttu-id="73f1f-962">리소스에 대한 LIST 작업 추가</span><span class="sxs-lookup"><span data-stu-id="73f1f-962">Adds LIST operations for resources</span></span>
* <span data-ttu-id="73f1f-963">상태 검사 단계에 대한 작업을 수행하는 기능 추가</span><span class="sxs-lookup"><span data-stu-id="73f1f-963">Adds capability for performing operations on Health Check steps</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="73f1f-964">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="73f1f-964">Az.HDInsight</span></span>
* <span data-ttu-id="73f1f-965">AzHDInsightCluster의 문서 오류 수정</span><span class="sxs-lookup"><span data-stu-id="73f1f-965">Fix document error of New-AzHDInsightCluster.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="73f1f-966">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="73f1f-966">Az.KeyVault</span></span>
* <span data-ttu-id="73f1f-967">Remove-AzureKeyVault가 새 New-AzureKeyVault와 일관성을 유지하도록 VaultName 특성에 이름 별칭 추가</span><span class="sxs-lookup"><span data-stu-id="73f1f-967">Add Name alias to VaultName attribute to make Remove-AzureKeyVault consistent with New-AzureKeyVault.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="73f1f-968">Az.Network</span><span class="sxs-lookup"><span data-stu-id="73f1f-968">Az.Network</span></span>
* <span data-ttu-id="73f1f-969">Set-AzNetworkWatcherConfigFlowLog.md에 트래픽 분석 사용 안 함 시나리오를 보여주는 새 예제 추가</span><span class="sxs-lookup"><span data-stu-id="73f1f-969">New example added to Set-AzNetworkWatcherConfigFlowLog.md to demonstrate Traffic Analytics disable scenario.</span></span>
* <span data-ttu-id="73f1f-970">Azure Firewall에 관리 IP 구성을 할당하는 지원 추가 - 방화벽에서 관리 트래픽에 사용할 전용 서브넷 및 공용 IP</span><span class="sxs-lookup"><span data-stu-id="73f1f-970">Add support for assigning management IP configuration to Azure Firewall - a dedicated subnet and Public IP that the firewall will use for its management traffic</span></span>
    - <span data-ttu-id="73f1f-971">New-AzFirewall cmdlet이 업데이트됨:</span><span class="sxs-lookup"><span data-stu-id="73f1f-971">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="73f1f-972">공용 IP 주소 개체를 허용하는 -ManagementPublicIpAddress 매개 변수(필수 아님) 추가</span><span class="sxs-lookup"><span data-stu-id="73f1f-972">Added parameter -ManagementPublicIpAddress (not mandatory) which accepts a Public IP Address object</span></span>
        - <span data-ttu-id="73f1f-973">방화벽 개체에 SetManagementIpConfiguration 메서드 추가 - 입력으로 서브넷 및 공용 IP 주소 필요 - 서브넷 이름은 'AzureFirewallManagementSubnet'이어야 함</span><span class="sxs-lookup"><span data-stu-id="73f1f-973">Added method SetManagementIpConfiguration on firewall object - requires a subnet and a Public IP address as input - subnet name must be 'AzureFirewallManagementSubnet'</span></span>
* <span data-ttu-id="73f1f-974">네트워크 인터페이스 대신 NSG 예제를 보여주도록 AzNetworkSecurityGroup 예제 수정</span><span class="sxs-lookup"><span data-stu-id="73f1f-974">Corrected Get-AzNetworkSecurityGroup examples to show examples for NSG's instead of network interfaces.</span></span>
* <span data-ttu-id="73f1f-975">리소스 id 완성자가 매개 변수를 완성하지 못하게 방해하던 New-AzVpnSite 명령의 오타 수정</span><span class="sxs-lookup"><span data-stu-id="73f1f-975">Fixed typo in New-AzVpnSite command that was preventing resource id completer from completing a parameter.</span></span>
* <span data-ttu-id="73f1f-976">Application Gateway의 다시 쓰기 규칙 작업 세트에서 Url 구성에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="73f1f-976">Added support for Url Confiugration in Rewrite Rules Action Set in the Application Gateway</span></span>
    - <span data-ttu-id="73f1f-977">추가된 새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-977">New cmdlets added:</span></span>
        - <span data-ttu-id="73f1f-978">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="73f1f-978">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span></span>
    - <span data-ttu-id="73f1f-979">선택적 매개 변수를 사용하도록 Cmdlet 업데이트 - UrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="73f1f-979">Cmdlets updated with optional parameter - UrlConfiguration</span></span>
        - <span data-ttu-id="73f1f-980">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="73f1f-980">New-AzApplicationGatewayRewriteRuleActionSet</span></span>
* <span data-ttu-id="73f1f-981">NetworkWatcher ConnectionMonitor 버전 2 리소스에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="73f1f-981">Add suppport for NetworkWatcher ConnectionMonitor version 2 resources</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="73f1f-982">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="73f1f-982">Az.PolicyInsights</span></span>
* <span data-ttu-id="73f1f-983">수정할 리소스를 결정하기 전에 규정 준수 평가 지원</span><span class="sxs-lookup"><span data-stu-id="73f1f-983">Support evaluating compliance prior to determining what resource to remediate</span></span>
    - <span data-ttu-id="73f1f-984">Start-AzPolicyRemediation에 '-ResourceDiscoverMode' 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="73f1f-984">Add '-ResourceDiscoverMode' parameter to Start-AzPolicyRemediation</span></span>
* <span data-ttu-id="73f1f-985">정책 메타데이터 리소스를 가져오는 Get-AzPolicyMetadata cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="73f1f-985">Add Get-AzPolicyMetadata cmdlet for getting policy metadata resources</span></span>
* <span data-ttu-id="73f1f-986">API 버전 2019-10-01의 Get-AzPolicyState 및 Get-AzPolicyStateSummary 업데이트</span><span class="sxs-lookup"><span data-stu-id="73f1f-986">Updated Get-AzPolicyState and Get-AzPolicyStateSummary for API version 2019-10-01</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="73f1f-987">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="73f1f-987">Az.RecoveryServices</span></span>
* <span data-ttu-id="73f1f-988">복제된 디스크를 제거할 수 있도록 Azure Site Recovery에 지원 추가</span><span class="sxs-lookup"><span data-stu-id="73f1f-988">Azure Site Recovery support for removing a replicated disk.</span></span>
* <span data-ttu-id="73f1f-989">Recovery Services 자격 증명 모음을 만드는 동안 태그를 추가할 수 있도록 Azure Backup에 지원 추가</span><span class="sxs-lookup"><span data-stu-id="73f1f-989">Azure Backup added support for adding tags while creating a Recovery Services Vault.</span></span>

#### <a name="azresources"></a><span data-ttu-id="73f1f-990">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="73f1f-990">Az.Resources</span></span>
* <span data-ttu-id="73f1f-991">컨텍스트 구독을 기본값으로 하는 \*-AzPolicyAssignment cmdlet에서 -Scope를 선택 사항으로 설정</span><span class="sxs-lookup"><span data-stu-id="73f1f-991">Make -Scope optional in \*-AzPolicyAssignment cmdlets with default to context subscription</span></span>
* <span data-ttu-id="73f1f-992">암호 및 키 자격 증명을 사용하여 ADServicePrincipal을 만드는 예제 추가</span><span class="sxs-lookup"><span data-stu-id="73f1f-992">Add examples of creating ADServicePrincipal with password and key credential</span></span>

#### <a name="azsql"></a><span data-ttu-id="73f1f-993">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="73f1f-993">Az.Sql</span></span>
<span data-ttu-id="73f1f-994">DatabaseName 대신 PartnerDatabaseName이 있는지 확인하도록 New-AzSqlDatabaseSecondary cmdlet 수정</span><span class="sxs-lookup"><span data-stu-id="73f1f-994">Fix New-AzSqlDatabaseSecondary cmdlet to check for PartnerDatabaseName existence instead of DatabaseName existence.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="73f1f-995">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="73f1f-995">Az.Storage</span></span>
* <span data-ttu-id="73f1f-996">스토리지 계정 만들기에서 테이블/큐 암호화 Keytype 설정 지원</span><span class="sxs-lookup"><span data-stu-id="73f1f-996">Support set Table/Queue Encryption Keytype in Create Storage Account</span></span>
    - <span data-ttu-id="73f1f-997">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="73f1f-997">New-AzStorageAccount</span></span>
* <span data-ttu-id="73f1f-998">StorageException에 ExtendedErrorInformation이 없으면 RequestId 표시</span><span class="sxs-lookup"><span data-stu-id="73f1f-998">Show RequestId when StorageException don't have ExtendedErrorInformation</span></span>
* <span data-ttu-id="73f1f-999">cmdlet Start-AzStorageBlobCopy의 예제 6 수정</span><span class="sxs-lookup"><span data-stu-id="73f1f-999">Fix the Example 6 of cmdlet Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="73f1f-1000">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="73f1f-1000">Az.Websites</span></span>
* <span data-ttu-id="73f1f-1001">Set-AzWebapp 및 Set-AzWebappSlot이 AlwaysOn, MinTls 및 FtpsState 속성 지원</span><span class="sxs-lookup"><span data-stu-id="73f1f-1001">Set-AzWebapp and Set-AzWebappSlot supports AlwaysOn, MinTls and FtpsState properties</span></span>
* <span data-ttu-id="73f1f-1002">단일 Set-AzWebApp 명령을 사용하여 AppservicePlan을 변경하는 동시에 HttpsOnly를 설정하면 HttpsOnly가 기본값으로 다시 설정되는 문제 수정</span><span class="sxs-lookup"><span data-stu-id="73f1f-1002">Fixing issue where setting HttpsOnly along with changing AppservicePlan at the same time using the single Set-AzWebApp Command, was resetting HttpsOnly to default value</span></span>

## <a name="330---january-2020"></a><span data-ttu-id="73f1f-1003">3.3.0 - 2020년 1월</span><span class="sxs-lookup"><span data-stu-id="73f1f-1003">3.3.0 - January 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="73f1f-1004">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="73f1f-1004">Az.Accounts</span></span>
* <span data-ttu-id="73f1f-1005">AzureAttestationServiceEndpointResourceId 및 AzureAttestationServiceEndpointSuffix 매개 변수를 허용하도록 Add-AzEnvironment 및 Set-AzEnvironment가 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="73f1f-1005">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameters AzureAttestationServiceEndpointResourceId and AzureAttestationServiceEndpointSuffix</span></span>

#### <a name="azcdn"></a><span data-ttu-id="73f1f-1006">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="73f1f-1006">Az.Cdn</span></span>
* <span data-ttu-id="73f1f-1007">New-AzCdnEndpoint cmdlet에서 오류 응답 세부 정보 표시</span><span class="sxs-lookup"><span data-stu-id="73f1f-1007">Display error response detail in New-AzCdnEndpoint cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="73f1f-1008">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="73f1f-1008">Az.Compute</span></span>
* <span data-ttu-id="73f1f-1009">OS 프로필이 없는 관리 OD 디스크가 있는 VM의 Set-AzVMCustomScriptExtension cmdlet을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1009">Fix Set-AzVMCustomScriptExtension cmdlet for a VM with managed OD disk which does not have OS profile.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="73f1f-1010">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="73f1f-1010">Az.ContainerInstance</span></span>
* <span data-ttu-id="73f1f-1011">New-AzContainerGroup의 예에서 사용되는 고정 매개 변수 이름</span><span class="sxs-lookup"><span data-stu-id="73f1f-1011">Fixed parameter names used by example of New-AzContainerGroup</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="73f1f-1012">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="73f1f-1012">Az.DataBoxEdge</span></span>
* <span data-ttu-id="73f1f-1013">'Get-AzDataBoxEdgeStorageContainer' cmdlet 추가됨</span><span class="sxs-lookup"><span data-stu-id="73f1f-1013">Added cmdlet 'Get-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="73f1f-1014">Edge 스토리지 컨테이너 가져오기</span><span class="sxs-lookup"><span data-stu-id="73f1f-1014">Get the Edge Storage Container</span></span>
* <span data-ttu-id="73f1f-1015">'New-AzDataBoxEdgeStorageContainer' cmdlet 추가됨</span><span class="sxs-lookup"><span data-stu-id="73f1f-1015">Added cmdlet 'New-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="73f1f-1016">새 Edge 스토리지 컨테이너 만들기</span><span class="sxs-lookup"><span data-stu-id="73f1f-1016">Create new Edge Strorage Container</span></span>
* <span data-ttu-id="73f1f-1017">'Remove-AzDataBoxEdgeStorageContainer' cmdlet 추가됨</span><span class="sxs-lookup"><span data-stu-id="73f1f-1017">Added cmdlet 'Remove-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="73f1f-1018">Edge 스토리지 컨테이너 제거</span><span class="sxs-lookup"><span data-stu-id="73f1f-1018">Remove the Edge Storage Container</span></span>
* <span data-ttu-id="73f1f-1019">'Invoke-AzDataBoxEdgeStorageContainer' cmdlet 추가됨</span><span class="sxs-lookup"><span data-stu-id="73f1f-1019">Added cmdlet 'Invoke-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="73f1f-1020">Edge 스토리지 컨테이너에서 데이터를 새로 고치는 작업 호출</span><span class="sxs-lookup"><span data-stu-id="73f1f-1020">Invoke action to refresh data on Edge Storage Container</span></span>
* <span data-ttu-id="73f1f-1021">'Get-AzDataBoxEdgeStorageAccount' cmdlet 추가됨</span><span class="sxs-lookup"><span data-stu-id="73f1f-1021">Added cmdlet 'Get-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="73f1f-1022">Edge 스토리지 계정 가져오기</span><span class="sxs-lookup"><span data-stu-id="73f1f-1022">Get the Edge Storage Account</span></span>
* <span data-ttu-id="73f1f-1023">'New-AzDataBoxEdgeStorageAccount' cmdlet 추가됨</span><span class="sxs-lookup"><span data-stu-id="73f1f-1023">Added cmdlet 'New-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="73f1f-1024">새 Edge 스토리지 계정 만들기</span><span class="sxs-lookup"><span data-stu-id="73f1f-1024">Create new Edge Storage Account</span></span>
* <span data-ttu-id="73f1f-1025">'Remove-AzDataBoxEdgeStorageAccount' cmdlet 추가됨</span><span class="sxs-lookup"><span data-stu-id="73f1f-1025">Added cmdlet 'Remove-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="73f1f-1026">Edge 스토리지 계정 제거</span><span class="sxs-lookup"><span data-stu-id="73f1f-1026">Remove the Edge Storage Account</span></span>
* <span data-ttu-id="73f1f-1027">'Invoke-AzDataBoxEdgeShare' cmdlet 호출</span><span class="sxs-lookup"><span data-stu-id="73f1f-1027">Invoke cmdlet 'Invoke-AzDataBoxEdgeShare'</span></span>
  - <span data-ttu-id="73f1f-1028">공유에서 데이터를 새로 고치는 작업 호출</span><span class="sxs-lookup"><span data-stu-id="73f1f-1028">Invoke action to refresh data on share</span></span>
* <span data-ttu-id="73f1f-1029">'Set-AzDataBoxEdgeStorageAccountCredential' cmdlet 추가됨</span><span class="sxs-lookup"><span data-stu-id="73f1f-1029">Added cmdlet 'Set-AzDataBoxEdgeStorageAccountCredential'</span></span>
  - <span data-ttu-id="73f1f-1030">az databoxedge 스토리지 계정 자격 증명 설정</span><span class="sxs-lookup"><span data-stu-id="73f1f-1030">Set the az databoxedge storage account credential</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="73f1f-1031">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="73f1f-1031">Az.DataFactory</span></span>
* <span data-ttu-id="73f1f-1032">Get-AzDataFactoryV2IntegrationRuntime cmd에 AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId 및 VersionStatus 속성 추가</span><span class="sxs-lookup"><span data-stu-id="73f1f-1032">Add AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId and VersionStatus properties for Get-AzDataFactoryV2IntegrationRuntime cmd</span></span>
* <span data-ttu-id="73f1f-1033">ADF .Net SDK 버전을 4.6.0으로 업데이트</span><span class="sxs-lookup"><span data-stu-id="73f1f-1033">Update ADF .Net SDK version to 4.6.0</span></span>
* <span data-ttu-id="73f1f-1034">고정 공용 IP 주소로 Azure-SSIS IR을 만들 수 있도록 'Set-AzureRmDataFactoryV2IntegrationRuntime'cmd에 대해 'PublicIPs' 매개 변수를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1034">Add parameter 'PublicIPs' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable create Azure-SSIS IR with static public IP addresses.</span></span>

#### <a name="azdevtestlabs"></a><span data-ttu-id="73f1f-1035">Az.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="73f1f-1035">Az.DevTestLabs</span></span>
* <span data-ttu-id="73f1f-1036">Get-AzDtlAllowedVMSizesPolicy.md에서 끊어진 링크 제거</span><span class="sxs-lookup"><span data-stu-id="73f1f-1036">Remove the broken link in Get-AzDtlAllowedVMSizesPolicy.md</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="73f1f-1037">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="73f1f-1037">Az.EventHub</span></span>
* <span data-ttu-id="73f1f-1038">10634 문제 해결: eventhubnamespace 제거에 대한 null 개체 참조 수정</span><span class="sxs-lookup"><span data-stu-id="73f1f-1038">Fix for issue 10634 : Fix the null Object reference for remove eventhubnamespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="73f1f-1039">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="73f1f-1039">Az.HDInsight</span></span>
* <span data-ttu-id="73f1f-1040">Invoke-AzHDInsightHiveJob.md 오류를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1040">Fix Invoke-AzHDInsightHiveJob.md error.</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="73f1f-1041">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="73f1f-1041">Az.MachineLearning</span></span>
* <span data-ttu-id="73f1f-1042">MachineLearningCompute를 더 이상 사용할 수 없게 되어 아래 cmdlet이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1042">Removed below cmdlets because MachineLearningCompute is not available any longer</span></span>
  - <span data-ttu-id="73f1f-1043">Get-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="73f1f-1043">Get-AzMlOpCluster</span></span>
  - <span data-ttu-id="73f1f-1044">Get-AzMlOpClusterKey</span><span class="sxs-lookup"><span data-stu-id="73f1f-1044">Get-AzMlOpClusterKey</span></span>
  - <span data-ttu-id="73f1f-1045">New-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="73f1f-1045">New-AzMlOpCluster</span></span>
  - <span data-ttu-id="73f1f-1046">Remove-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="73f1f-1046">Remove-AzMlOpCluster</span></span>
  - <span data-ttu-id="73f1f-1047">Set-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="73f1f-1047">Set-AzMlOpCluster</span></span>
  - <span data-ttu-id="73f1f-1048">Test-AzMlOpClusterSystemServicesUpdateAvailability</span><span class="sxs-lookup"><span data-stu-id="73f1f-1048">Test-AzMlOpClusterSystemServicesUpdateAvailability</span></span>
  - <span data-ttu-id="73f1f-1049">Update-AzMlOpClusterSystemService</span><span class="sxs-lookup"><span data-stu-id="73f1f-1049">Update-AzMlOpClusterSystemService</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="73f1f-1050">Az.Network</span><span class="sxs-lookup"><span data-stu-id="73f1f-1050">Az.Network</span></span>
* <span data-ttu-id="73f1f-1051">Microsoft.Azure.Management.Sql의 종속성을 1.36-preview에서 1.37-preview로 업그레이드</span><span class="sxs-lookup"><span data-stu-id="73f1f-1051">Upgrade dependency of Microsoft.Azure.Management.Sql from 1.36-preview to 1.37-preview</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="73f1f-1052">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="73f1f-1052">Az.RecoveryServices</span></span>
* <span data-ttu-id="73f1f-1053">Azure Site Recovery는 Azure 간 공급자를 위해 고객 관리 키와 함께 유휴 상태에서 암호화된 관리 디스크 vms의 변경을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1053">Azure Site Recovery change support for managed disk vms encrypted at rest with customer managed keys for Azure to Azure provider.</span></span>
* <span data-ttu-id="73f1f-1054">Azure Site Recovery는 VMware에서 Azure로를 위해 보호를 사용할 때 선택적 입력으로서 디스크 암호화 집합 ID를 입력하도록 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1054">Azure Site Recovery support to input disk encryption Set Id as optional input at enabling protection for Vmware to Azure.</span></span>
* <span data-ttu-id="73f1f-1055">Azure Site Recovery는 VMware에서 Azure로를 위해 보호를 사용하기 위해 디스크 수준의 선택적 입력으로서 디스크 암호화 집합 ID를 입력하도록 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1055">Azure Site Recovery support to input disk encryption Set Id as optional input at disk level to enable protection for Vmware to Azure.</span></span>
* <span data-ttu-id="73f1f-1056">Azure Site Recovery는 HyperV에서 Azure로를 위해 디스크 암호화 집합 맵을 사용하여 복제 보호된 항목을 업데이트하도록 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1056">Azure Site Recovery support to update replication protected item with disk encryption set Map for HyperV to Azure.</span></span>

#### <a name="azresources"></a><span data-ttu-id="73f1f-1057">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="73f1f-1057">Az.Resources</span></span>
* <span data-ttu-id="73f1f-1058">'Remove-AzTag'의 도움말 문서에서 오류를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1058">Fix an error in help document of 'Remove-AzTag'.</span></span>

#### <a name="azsql"></a><span data-ttu-id="73f1f-1059">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="73f1f-1059">Az.Sql</span></span>
* <span data-ttu-id="73f1f-1060">Azure Database의 마스터 DB에서 작동하도록 취약성 평가 세트 기준 cmdlet 기능을 수정하고 관리형 인스턴스 시스템 데이터베이스에서 이를 제한합니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1060">Fix vulnerability assessment set baseline cmdlets functionality to work on master db for azure database and limit it on managed instance system databases.</span></span>
* <span data-ttu-id="73f1f-1061">SQL 인스턴스 장애 조치(failover) 그룹을 만들 때 오류 수정</span><span class="sxs-lookup"><span data-stu-id="73f1f-1061">Fix an error when creating SQL instance failover group</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="73f1f-1062">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="73f1f-1062">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="73f1f-1063">올바른 새 라이선스 형식으로 DR 추가</span><span class="sxs-lookup"><span data-stu-id="73f1f-1063">Add DR as a new valid License type</span></span>

#### <a name="azstorage"></a><span data-ttu-id="73f1f-1064">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="73f1f-1064">Az.Storage</span></span>
* <span data-ttu-id="73f1f-1065">다음 릴리스에서 DefaultAction Value 변경에 대해 호환성이 손상되는 변경 경고 메시지 추가</span><span class="sxs-lookup"><span data-stu-id="73f1f-1065">Add breaking change warning message for DefaultAction Value change in a future release</span></span>
    - <span data-ttu-id="73f1f-1066">Update-AzStorageAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="73f1f-1066">Update-AzStorageAccountNetworkRuleSet</span></span>
* <span data-ttu-id="73f1f-1067">-IncludeGeoReplicationStats 매개 변수와 함께 get-AzureRMStorageAccount를 실행하여 스토리지 계정의 마지막 동기화 시간 가져오기 지원</span><span class="sxs-lookup"><span data-stu-id="73f1f-1067">Support Get last sync time of Storage account by run get-AzureRMStorageAccount with parameter -IncludeGeoReplicationStats</span></span>
    - <span data-ttu-id="73f1f-1068">Get-AzureRMStorageAccount</span><span class="sxs-lookup"><span data-stu-id="73f1f-1068">Get-AzureRMStorageAccount</span></span>

## <a name="320---december-2019"></a><span data-ttu-id="73f1f-1069">3.2.0 - 2019년 12월</span><span class="sxs-lookup"><span data-stu-id="73f1f-1069">3.2.0 - December 2019</span></span>

### <a name="general"></a><span data-ttu-id="73f1f-1070">일반</span><span class="sxs-lookup"><span data-stu-id="73f1f-1070">General</span></span>
* <span data-ttu-id="73f1f-1071">모든 모듈의 상대 경로를 사용하기 위해 .psd1의 참조 업데이트</span><span class="sxs-lookup"><span data-stu-id="73f1f-1071">Update references in .psd1 to use relative path for all modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="73f1f-1072">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="73f1f-1072">Az.Accounts</span></span>
* <span data-ttu-id="73f1f-1073">Az 4.0 미리 보기를 위해 클라이언트 측 원격 분석에 대해 UserAgent를 올바르게 설정</span><span class="sxs-lookup"><span data-stu-id="73f1f-1073">Set correct UserAgent for client-side telemetry for Az 4.0 preview</span></span>
* <span data-ttu-id="73f1f-1074">Az 4.0 미리 보기에서 컨텍스트가 null인 경우 사용자에게 친숙한 오류 메시지로 표시</span><span class="sxs-lookup"><span data-stu-id="73f1f-1074">Display user friendly error message when context is null in Az 4.0 preview</span></span>

#### <a name="azbatch"></a><span data-ttu-id="73f1f-1075">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="73f1f-1075">Az.Batch</span></span>
* <span data-ttu-id="73f1f-1076">**New-AzBatchPool**이 'VirtualMachineConfiguration.ContainerConfiguration' 또는 'VirtualMachineConfiguration.DataDisks'를 서버로 제대로 보내지 않는 [#10602](https://github.com/Azure/azure-powershell/issues/10602) 문제 수정</span><span class="sxs-lookup"><span data-stu-id="73f1f-1076">Fix issue [#10602](https://github.com/Azure/azure-powershell/issues/10602), where **New-AzBatchPool** did not properly send 'VirtualMachineConfiguration.ContainerConfiguration' or 'VirtualMachineConfiguration.DataDisks' to the server.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="73f1f-1077">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="73f1f-1077">Az.DataFactory</span></span>
* <span data-ttu-id="73f1f-1078">ADF .Net SDK 버전을 4.5.0으로 업데이트</span><span class="sxs-lookup"><span data-stu-id="73f1f-1078">Update ADF .Net SDK version to 4.5.0</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="73f1f-1079">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="73f1f-1079">Az.FrontDoor</span></span>
* <span data-ttu-id="73f1f-1080">WAF 관리 규칙 제외 지원 추가됨</span><span class="sxs-lookup"><span data-stu-id="73f1f-1080">Added WAF managed rules exclusion support</span></span>
* <span data-ttu-id="73f1f-1081">자동 완성에 SocketAddr 추가</span><span class="sxs-lookup"><span data-stu-id="73f1f-1081">Add SocketAddr to auto-complete</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="73f1f-1082">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="73f1f-1082">Az.HealthcareApis</span></span>
* <span data-ttu-id="73f1f-1083">예외 처리</span><span class="sxs-lookup"><span data-stu-id="73f1f-1083">Exception Handling</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="73f1f-1084">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="73f1f-1084">Az.KeyVault</span></span>
* <span data-ttu-id="73f1f-1085">잠재적으로 설정되지 않은 오류 액세스 값 수정</span><span class="sxs-lookup"><span data-stu-id="73f1f-1085">Fixed error accessing value that is potentially not set</span></span>
* <span data-ttu-id="73f1f-1086">타원 곡선 암호화 인증서 관리</span><span class="sxs-lookup"><span data-stu-id="73f1f-1086">Elliptic Curve Cryptography Certificate Managment</span></span>
    - <span data-ttu-id="73f1f-1087">인증서 정책에 대한 곡선 지정을 위한 지원 추가됨</span><span class="sxs-lookup"><span data-stu-id="73f1f-1087">Added support to specify the Curve for Certificate Policies</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="73f1f-1088">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="73f1f-1088">Az.Monitor</span></span>
* <span data-ttu-id="73f1f-1089">진단 설정 추가 명령에 선택적 인수 추가</span><span class="sxs-lookup"><span data-stu-id="73f1f-1089">Adding optional argument to the Add Diagnostic Settings command.</span></span> <span data-ttu-id="73f1f-1090">스위치 인수(있는 경우)는 Log Analytics로 내보내기가 고정 스키마(전용 데이터 유형)가 되어야 함을</span><span class="sxs-lookup"><span data-stu-id="73f1f-1090">A switch argument that if present indicates that the export to Log Analytics must be to a fixed schema (a.k.a.</span></span> <span data-ttu-id="73f1f-1091">나타냄</span><span class="sxs-lookup"><span data-stu-id="73f1f-1091">dedicated, data type)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="73f1f-1092">Az.Network</span><span class="sxs-lookup"><span data-stu-id="73f1f-1092">Az.Network</span></span>
* <span data-ttu-id="73f1f-1093">AzureFirewall 애플리케이션, NAT 및 네트워크 규칙에서 IpGroups 지원.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1093">Support for IpGroups in AzureFirewall Application,Nat & Network Rules.</span></span>

#### <a name="azresources"></a><span data-ttu-id="73f1f-1094">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="73f1f-1094">Az.Resources</span></span>
* <span data-ttu-id="73f1f-1095">이름이 일부 내장 매개 변수 이름과 충돌하는 경우 템플릿 배포가 템플릿 매개 변수를 읽지 못하는 문제 수정.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1095">Fix an issue where template deployment fails to read a template parameter if its name conflicts with some built-in parameter name.</span></span>
* <span data-ttu-id="73f1f-1096">정책 세트 정의 내에 그룹화 지원을 도입하는 새로운 API 버전 2019-09-01을 사용하도록 정책 cmdlet 업데이트.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1096">Updated policy cmdlets to use new api version 2019-09-01 that introduces grouping support within policy set definitions.</span></span>

#### <a name="azsql"></a><span data-ttu-id="73f1f-1097">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="73f1f-1097">Az.Sql</span></span>
* <span data-ttu-id="73f1f-1098">취약성 평가 자동 활성화에서 스토리지 생성을 StorageV2로 업그레이드</span><span class="sxs-lookup"><span data-stu-id="73f1f-1098">Upgraded storage creation in Vulnerability Assessment auto enablement to StorageV2</span></span>

#### <a name="azstorage"></a><span data-ttu-id="73f1f-1099">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="73f1f-1099">Az.Storage</span></span>
* <span data-ttu-id="73f1f-1100">Oauth 인증을 기반으로 스토리지 컨텍스트를 사용하여 Blob/컨테이너 ID 기반 SAS 토큰 생성 지원</span><span class="sxs-lookup"><span data-stu-id="73f1f-1100">Support generate Blob/Constainer Idenity based SAS token with Storage Context based on Oauth authentication</span></span>
    - <span data-ttu-id="73f1f-1101">New-AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="73f1f-1101">New-AzStorageContainerSASToken</span></span>
    - <span data-ttu-id="73f1f-1102">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="73f1f-1102">New-AzStorageBlobSASToken</span></span>
* <span data-ttu-id="73f1f-1103">모든 Idenity SAS 토큰을 해지할 수 있도록 스토리지 계정 사용자 위임 키 해지 지원</span><span class="sxs-lookup"><span data-stu-id="73f1f-1103">Support revoke Storage Account User Delegation Keys, so all Idenity SAS tokens are revoked</span></span>
    - <span data-ttu-id="73f1f-1104">Revoke-AzStorageAccountUserDelegationKeys</span><span class="sxs-lookup"><span data-stu-id="73f1f-1104">Revoke-AzStorageAccountUserDelegationKeys</span></span>
* <span data-ttu-id="73f1f-1105">새로운 API 버전 2019-06-01을 지원하기 위해 Microsoft.Azure.Management.Storage 14.2.0으로 업그레이드.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1105">Upgrade to Microsoft.Azure.Management.Storage 14.2.0, to support new API version 2019-06-01.</span></span>
* <span data-ttu-id="73f1f-1106">File Share cmdlet의 관리 평면에서 5120을 초과하는 값에 대해 QuotaGiB(Gibyby의 공유 할당량)를 지원하고 'Quota' 매개 변수 별칭을 'QuotaGiB' 매개 변수에 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1106">Support of QuotaGiB (Share Quota in Gibibye) for values of more than 5120 in the Management plane of File Share cmdlets and added the 'Quota' parameter alias to the 'QuotaGiB' parameter.</span></span>
    - <span data-ttu-id="73f1f-1107">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="73f1f-1107">New-AzRmStorageShare</span></span>
    - <span data-ttu-id="73f1f-1108">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="73f1f-1108">Update-AzRmStorageShare</span></span>
* <span data-ttu-id="73f1f-1109">매개 변수 'Quota'에 매개 변수 별칭 'QuotaGiB' 추가</span><span class="sxs-lookup"><span data-stu-id="73f1f-1109">Add parameter alias 'QuotaGiB' to parameter 'Quota'</span></span>
    - <span data-ttu-id="73f1f-1110">Set-AzStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="73f1f-1110">Set-AzStorageShareQuota</span></span>
* <span data-ttu-id="73f1f-1111">Set-AzStorageContainerAcl가 저장된 액세스 정책을 정리할 수 있는 문제 수정</span><span class="sxs-lookup"><span data-stu-id="73f1f-1111">Fix the issue that Set-AzStorageContainerAcl can clean up the stored Access Policy</span></span>
    - <span data-ttu-id="73f1f-1112">Set-AzStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="73f1f-1112">Set-AzStorageContainerAcl</span></span>

## <a name="310---november-2019"></a><span data-ttu-id="73f1f-1113">3.1.0 - 2019년 11월</span><span class="sxs-lookup"><span data-stu-id="73f1f-1113">3.1.0 - November 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="73f1f-1114">마지막 주 릴리스 이후의 주요 사항</span><span class="sxs-lookup"><span data-stu-id="73f1f-1114">Highlights since the last major release</span></span>
* <span data-ttu-id="73f1f-1115">Az.DataBoxEdge 1.0.0 릴리스됨</span><span class="sxs-lookup"><span data-stu-id="73f1f-1115">Az.DataBoxEdge 1.0.0 released</span></span>
* <span data-ttu-id="73f1f-1116">Az.SqlVirtualMachine 1.0.0 릴리스됨</span><span class="sxs-lookup"><span data-stu-id="73f1f-1116">Az.SqlVirtualMachine 1.0.0 released</span></span>

#### <a name="azcompute"></a><span data-ttu-id="73f1f-1117">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="73f1f-1117">Az.Compute</span></span>
* <span data-ttu-id="73f1f-1118">VM Reapply 기능</span><span class="sxs-lookup"><span data-stu-id="73f1f-1118">VM Reapply feature</span></span>
    - <span data-ttu-id="73f1f-1119">Set-AzVM cmdlet에 Reapply 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="73f1f-1119">Add Reapply parameter to Set-AzVM cmdlet</span></span>
* <span data-ttu-id="73f1f-1120">VM 확장 집합 AutomaticRepairs 기능:</span><span class="sxs-lookup"><span data-stu-id="73f1f-1120">VM Scale Set AutomaticRepairs feature:</span></span>
    - <span data-ttu-id="73f1f-1121">다음 cmdlet에 EnableAutomaticRepair, AutomaticRepairGracePeriod 및 AutomaticRepairMaxInstanceRepairsPercent 매개 변수를 추가합니다.   New-AzVmssConfig   Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="73f1f-1121">Add EnableAutomaticRepair, AutomaticRepairGracePeriod, and AutomaticRepairMaxInstanceRepairsPercent parameters to the following cmdlets:   New-AzVmssConfig   Update-AzVmss</span></span>
* <span data-ttu-id="73f1f-1122">New-AzVM에 대한 교차 테넌트 갤러리 이미지 지원</span><span class="sxs-lookup"><span data-stu-id="73f1f-1122">Cross tenant gallery image support for New-AzVM</span></span>
* <span data-ttu-id="73f1f-1123">New-AzVM, New-AzVMConfig 및 New-AzVmss cmdlet의 Priority 매개 변수의 인수 완성자에 'Spot' 추가</span><span class="sxs-lookup"><span data-stu-id="73f1f-1123">Add 'Spot' to the argument completer of Priority parameter in New-AzVM, New-AzVMConfig and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="73f1f-1124">Add-AzVmssDataDisk cmdlet에 DiskIOPSReadWrite 및 DiskMBpsReadWrite 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="73f1f-1124">Add DiskIOPSReadWrite and DiskMBpsReadWrite parameters to Add-AzVmssDataDisk cmdlet</span></span>
* <span data-ttu-id="73f1f-1125">New-AzGalleryImageVersion cmdlet의 SourceImageId 매개 변수를 선택 사항으로 변경</span><span class="sxs-lookup"><span data-stu-id="73f1f-1125">Change SourceImageId parameter of New-AzGalleryImageVersion cmdlet to optional</span></span>
* <span data-ttu-id="73f1f-1126">New-AzGalleryImageVersion cmdlet에 OSDiskImage 및 DataDiskImage 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="73f1f-1126">Add OSDiskImage and DataDiskImage parameters to New-AzGalleryImageVersion cmdlet</span></span>
* <span data-ttu-id="73f1f-1127">New-AzGalleryImageDefinition cmdlet에 HyperVGeneration 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="73f1f-1127">Add HyperVGeneration parameter to New-AzGalleryImageDefinition cmdlet</span></span>
* <span data-ttu-id="73f1f-1128">New-AzVmss, New-AzVmssConfig 및 Update-AzVmss cmdlet에 SkipExtensionsOnOverprovisionedVMs 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="73f1f-1128">Add SkipExtensionsOnOverprovisionedVMs parameters to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="73f1f-1129">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="73f1f-1129">Az.DataBoxEdge</span></span>
* <span data-ttu-id="73f1f-1130">cmdlet `Get-AzDataBoxEdgeOrder` 추가됨</span><span class="sxs-lookup"><span data-stu-id="73f1f-1130">Added cmdlet `Get-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="73f1f-1131">주문 가져오기</span><span class="sxs-lookup"><span data-stu-id="73f1f-1131">Get the Order</span></span>
* <span data-ttu-id="73f1f-1132">cmdlet `New-AzDataBoxEdgeOrder` 추가됨</span><span class="sxs-lookup"><span data-stu-id="73f1f-1132">Added cmdlet `New-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="73f1f-1133">새 주문 만들기</span><span class="sxs-lookup"><span data-stu-id="73f1f-1133">Create new Order</span></span>
* <span data-ttu-id="73f1f-1134">cmdlet `Remove-AzDataBoxEdgeOrder` 추가됨</span><span class="sxs-lookup"><span data-stu-id="73f1f-1134">Added cmdlet `Remove-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="73f1f-1135">주문 제거</span><span class="sxs-lookup"><span data-stu-id="73f1f-1135">Remove the Order</span></span>
* <span data-ttu-id="73f1f-1136">cmdlet `New-AzDataBoxEdgeShare` 변경</span><span class="sxs-lookup"><span data-stu-id="73f1f-1136">Change in cmdlet `New-AzDataBoxEdgeShare`</span></span>
    - <span data-ttu-id="73f1f-1137">이제 로컬 공유를 만듬</span><span class="sxs-lookup"><span data-stu-id="73f1f-1137">Now creates Local Share</span></span>
* <span data-ttu-id="73f1f-1138">cmdlet `Set-AzDataBoxEdgeRole` 추가됨</span><span class="sxs-lookup"><span data-stu-id="73f1f-1138">Added cmdlet `Set-AzDataBoxEdgeRole`</span></span>
    - <span data-ttu-id="73f1f-1139">이제 IotRole을 공유에 매핑할 수 있음</span><span class="sxs-lookup"><span data-stu-id="73f1f-1139">Now IotRole can be mapped to Share</span></span>
* <span data-ttu-id="73f1f-1140">cmdlet `Invoke-AzDataBoxEdgeDevice` 추가됨</span><span class="sxs-lookup"><span data-stu-id="73f1f-1140">Added cmdlet `Invoke-AzDataBoxEdgeDevice`</span></span>
    - <span data-ttu-id="73f1f-1141">스캔 업데이트 호출, 업데이트 다운로드, 디바이스에 업데이트 설치</span><span class="sxs-lookup"><span data-stu-id="73f1f-1141">Invoke scan update, download update, install updates on the device</span></span>
* <span data-ttu-id="73f1f-1142">cmdlet `Get-AzDataBoxEdgeTrigger` 추가됨</span><span class="sxs-lookup"><span data-stu-id="73f1f-1142">Added cmdlet `Get-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="73f1f-1143">트리거에 대한 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="73f1f-1143">Gets the information about Triggers</span></span>
* <span data-ttu-id="73f1f-1144">cmdlet `New-AzDataBoxEdgeTrigger` 추가됨</span><span class="sxs-lookup"><span data-stu-id="73f1f-1144">Added cmdlet `New-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="73f1f-1145">새 트리거 만들기</span><span class="sxs-lookup"><span data-stu-id="73f1f-1145">Create new Triggers</span></span>
* <span data-ttu-id="73f1f-1146">cmdlet `Remove-AzDataBoxEdgeTrigger` 추가됨</span><span class="sxs-lookup"><span data-stu-id="73f1f-1146">Added cmdlet `Remove-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="73f1f-1147">트리거 제거</span><span class="sxs-lookup"><span data-stu-id="73f1f-1147">Remove the Triggers</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="73f1f-1148">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="73f1f-1148">Az.DataFactory</span></span>
* <span data-ttu-id="73f1f-1149">ADF .Net SDK 버전을 4.4.0으로 업데이트</span><span class="sxs-lookup"><span data-stu-id="73f1f-1149">Update ADF .Net SDK version to 4.4.0</span></span>
* <span data-ttu-id="73f1f-1150">'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd에 'ExpressCustomSetup' 매개 변수를 추가하여 사용자 지정 설치 스크립트 없이 설치 구성 및 타사 구성 요소를 사용하도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1150">Add parameter 'ExpressCustomSetup' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable setup configurations and 3rd party components without custom setup script.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="73f1f-1151">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="73f1f-1151">Az.DataLakeStore</span></span>
* <span data-ttu-id="73f1f-1152">Get-AzDataLakeStoreDeletedItem 및 Restore-AzDataLakeStoreDeletedItem의 설명서 업데이트</span><span class="sxs-lookup"><span data-stu-id="73f1f-1152">Update documentation of Get-AzDataLakeStoreDeletedItem and Restore-AzDataLakeStoreDeletedItem</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="73f1f-1153">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="73f1f-1153">Az.EventHub</span></span>
* <span data-ttu-id="73f1f-1154">10301 문제 해결: SAS 토큰 날짜 형식 수정</span><span class="sxs-lookup"><span data-stu-id="73f1f-1154">Fix for issue 10301 : Fix the SAS Token date format</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="73f1f-1155">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="73f1f-1155">Az.FrontDoor</span></span>
* <span data-ttu-id="73f1f-1156">Enable-AzFrontDoorCustomDomainHttps 및 New-AzFrontDoorFrontendEndpointObject에 MinimumTlsVersion 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="73f1f-1156">Add MinimumTlsVersion parameter to Enable-AzFrontDoorCustomDomainHttps and New-AzFrontDoorFrontendEndpointObject</span></span>
* <span data-ttu-id="73f1f-1157">New-AzFrontDoorHealthProbeSettingObject에 HealthProbeMethod 및 EnabledState 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="73f1f-1157">Add HealthProbeMethod and EnabledState parameters to New-AzFrontDoorHealthProbeSettingObject</span></span>
* <span data-ttu-id="73f1f-1158">BackendPoolsSettings 개체를 생성하여 Front Door 생성/업데이트에 전달하는 새 cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="73f1f-1158">Add new cmdlet to create BackendPoolsSettings objec to pass into creation/update of Front Door</span></span>
    - <span data-ttu-id="73f1f-1159">New-AzFrontDoorBackendPoolsSettingObject</span><span class="sxs-lookup"><span data-stu-id="73f1f-1159">New-AzFrontDoorBackendPoolsSettingObject</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="73f1f-1160">Az.Network</span><span class="sxs-lookup"><span data-stu-id="73f1f-1160">Az.Network</span></span>
* <span data-ttu-id="73f1f-1161">'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' 및 'Start-AzVirtualnetworkGatewayPacketCapture.md' FilterData 옵션 예제를 변경합니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1161">Change 'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' and 'Start-AzVirtualnetworkGatewayPacketCapture.md' FilterData option examples.</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="73f1f-1162">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="73f1f-1162">Az.PrivateDns</span></span>
* <span data-ttu-id="73f1f-1163">PrivateDns .net sdk를 버전 1.0.0으로 업데이트함</span><span class="sxs-lookup"><span data-stu-id="73f1f-1163">Updated PrivateDns .net sdk to version 1.0.0</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="73f1f-1164">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="73f1f-1164">Az.RecoveryServices</span></span>
* <span data-ttu-id="73f1f-1165">보호를 사용하도록 설정할 때 디스크 유형을 선택하도록 Azure Site Recovery 지원</span><span class="sxs-lookup"><span data-stu-id="73f1f-1165">Azure Site Recovery support to select disk type at enabling protection.</span></span>
* <span data-ttu-id="73f1f-1166">복구 계획 동작 편집을 위한 Azure Site Recovery 버그 수정</span><span class="sxs-lookup"><span data-stu-id="73f1f-1166">Azure Site Recovery bug fix for recovery plan action edit.</span></span>
* <span data-ttu-id="73f1f-1167">파일 스트림 DB를 허용하도록 Azure Backup SQL 복원 지원</span><span class="sxs-lookup"><span data-stu-id="73f1f-1167">Azure Backup SQL Restore support to accept filestream DBs.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="73f1f-1168">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="73f1f-1168">Az.RedisCache</span></span>
* <span data-ttu-id="73f1f-1169">'New-AzRedisCache' 및 'Set-AzRedisCache' cmdlet에 'MinimumTlsVersion' 매개 변수가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1169">Added 'MinimumTlsVersion' parameter in 'New-AzRedisCache' and 'Set-AzRedisCache' cmdlets.</span></span> <span data-ttu-id="73f1f-1170">'Get-AzRedisCache' cmdlet 출력에 'MinimumTlsVersion'도 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1170">Also, added 'MinimumTlsVersion' in the output of 'Get-AzRedisCache' cmdlet.</span></span>
* <span data-ttu-id="73f1f-1171">'Set-AzRedisCache' 및 'New-AzRedisCache' cmdlet의 '-Size' 매개 변수에 대한 유효성 검사가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1171">Added validation on '-Size' parameter for 'Set-AzRedisCache' and 'New-AzRedisCache' cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="73f1f-1172">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="73f1f-1172">Az.Resources</span></span>
- <span data-ttu-id="73f1f-1173">정책 할당에 새로운 EnforcementMode 속성이 있는 새 api 버전 2019-06-01을 사용하도록 정책 cmdlet이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1173">Updated policy cmdlets to use new api version 2019-06-01 that has new EnforcementMode property in policy assignment.</span></span>
- <span data-ttu-id="73f1f-1174">정책 정의 만들기 도움말 예제가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1174">Updated create policy definition help example</span></span>
- <span data-ttu-id="73f1f-1175">Remove-AZADServicePrincipal -ServicePrincipalName 버그를 수정하고, 서비스 사용자 이름을 찾을 수 없으면 null 참조를 throw합니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1175">Fix bug Remove-AZADServicePrincipal -ServicePrincipalName, throw null reference when service principal name not found.</span></span>
- <span data-ttu-id="73f1f-1176">New-AZADServicePrincipal 버그를 수정하고, 테넌트에 구독이 없으면 null 참조를 throw합니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1176">Fix bug New-AZADServicePrincipal, throw null reference when tenant doesn't have any subscription.</span></span>
- <span data-ttu-id="73f1f-1177">연결된 애플리케이션에만 자격 증명을 추가하도록 New-AzAdServicePrincipal을 변경합니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1177">Change New-AzAdServicePrincipal to add credentials only to associated application.</span></span>

#### <a name="azsql"></a><span data-ttu-id="73f1f-1178">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="73f1f-1178">Az.Sql</span></span>
* <span data-ttu-id="73f1f-1179">데이터베이스 ReadReplicaCount에 대한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1179">Added support for database ReadReplicaCount.</span></span>
* <span data-ttu-id="73f1f-1180">영역 중복이 설정되지 않은 경우 Set-AzSqlDatabase가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1180">Fixed Set-AzSqlDatabase when zone redundancy not set</span></span>

## <a name="300---november-2019"></a><span data-ttu-id="73f1f-1181">3.0.0 - 2019년 11월</span><span class="sxs-lookup"><span data-stu-id="73f1f-1181">3.0.0 - November 2019</span></span>
### <a name="general"></a><span data-ttu-id="73f1f-1182">일반</span><span class="sxs-lookup"><span data-stu-id="73f1f-1182">General</span></span>
* <span data-ttu-id="73f1f-1183">Az.PrivateDns 1.0.0 릴리스</span><span class="sxs-lookup"><span data-stu-id="73f1f-1183">Az.PrivateDns 1.0.0 released</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="73f1f-1184">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="73f1f-1184">Az.Accounts</span></span>
* <span data-ttu-id="73f1f-1185">'Resolve-Error' 별칭에 사용 중단 메시지를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1185">Add a deprecation message for 'Resolve-Error' alias.</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="73f1f-1186">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="73f1f-1186">Az.Advisor</span></span>
* <span data-ttu-id="73f1f-1187">Get-AzAdvisorRecommendation cmdlet에 새로운 '운영 효율성' 범주가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1187">Added new category 'Operational Excellence' to Get-AzAdvisorRecommendation cmdlet.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="73f1f-1188">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="73f1f-1188">Az.Batch</span></span>
* <span data-ttu-id="73f1f-1189">`BatchAccountContext`의 `CoreQuota` 이름이 `DedicatedCoreQuota`로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1189">Renamed `CoreQuota` on `BatchAccountContext` to `DedicatedCoreQuota`.</span></span> <span data-ttu-id="73f1f-1190">또한 `LowPriorityCoreQuota`가 새로 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1190">There is also a new `LowPriorityCoreQuota`.</span></span>
  - <span data-ttu-id="73f1f-1191">이 변경 사항은 **Get-AzBatchAccount**에 영향을 줍니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1191">This impacts **Get-AzBatchAccount**.</span></span>
* <span data-ttu-id="73f1f-1192">이제 **New-AzBatchTask** `-ResourceFile` 매개 변수는 새로운 **New-AzBatchResourceFile** cmdlet을 사용하여 구성할 수 있는 `PSResourceFile` 개체의 컬렉션을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1192">**New-AzBatchTask** `-ResourceFile` parameter now takes a collection of `PSResourceFile` objects, which can be constructed using the new **New-AzBatchResourceFile** cmdlet.</span></span>
* <span data-ttu-id="73f1f-1193">새로운 **New-AzBatchResourceFile** cmdlet을 통해 `PSResourceFile` 개체를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1193">New **New-AzBatchResourceFile** cmdlet to help create `PSResourceFile` objects.</span></span> <span data-ttu-id="73f1f-1194">이들은 `-ResourceFile` 매개 변수의 **New-AzBatchTask**에 제공될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1194">These can be supplied to **New-AzBatchTask** on the `-ResourceFile` parameter.</span></span>
  - <span data-ttu-id="73f1f-1195">그에 따라 기존 `HttpUrl` 방법 외에도 두 가지 종류의 리소스 파일이 새롭게 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1195">This supports two new kinds of resource file in addition to the existing `HttpUrl` way:</span></span>
    - <span data-ttu-id="73f1f-1196">`AutoStorageContainerName` 기반 리소스 파일은 전체 자동 스토리지 컨테이너를 일괄 처리 노드에 다운로드합니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1196">`AutoStorageContainerName` based resource files download an entire auto-storage container to the Batch node.</span></span>
    - <span data-ttu-id="73f1f-1197">`StorageContainerUrl` 기반 리소스 파일은 URL에 지정된 컨테이너를 일괄 처리 노드에 다운로드합니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1197">`StorageContainerUrl` based resource files download the container specified in the URL to the Batch node.</span></span>
* <span data-ttu-id="73f1f-1198">**Get-AzBatchApplication**으로 반환되는 `PSApplication`의 `ApplicationPackages` 속성이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1198">Removed `ApplicationPackages` property of `PSApplication` returned by **Get-AzBatchApplication**.</span></span>
  - <span data-ttu-id="73f1f-1199">이제 **Get-AzBatchApplicationPackage**를 사용하여 애플리케이션 내부의 특정 패키지를 검색할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1199">The specific packages inside of an application now can be retrieved using **Get-AzBatchApplicationPackage**.</span></span> <span data-ttu-id="73f1f-1200">예: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`</span><span class="sxs-lookup"><span data-stu-id="73f1f-1200">For example: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span></span>
* <span data-ttu-id="73f1f-1201">**Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication** 및 **Set-AzBatchApplication**에서 `ApplicationId` 이름이 `ApplicationName`으로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1201">Renamed `ApplicationId` to `ApplicationName` on **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication**, and **Set-AzBatchApplication**.</span></span>
  - <span data-ttu-id="73f1f-1202">이제 `ApplicationId`는 `ApplicationName`의 별칭입니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1202">`ApplicationId` now is an alias of `ApplicationName`.</span></span>
* <span data-ttu-id="73f1f-1203">새로운 `PSWindowsUserConfiguration` 속성이 `PSUserAccount`에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1203">Added new `PSWindowsUserConfiguration` property to `PSUserAccount`.</span></span>
* <span data-ttu-id="73f1f-1204">`PSApplicationPackage`에서 `Version` 이름이 `Name`으로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1204">Renamed `Version` to `Name` on `PSApplicationPackage`.</span></span>
* <span data-ttu-id="73f1f-1205">`PSResourceFile`에서 `BlobSource` 이름이 `HttpUrl`으로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1205">Renamed `BlobSource` to `HttpUrl` on `PSResourceFile`.</span></span>
* <span data-ttu-id="73f1f-1206">`PSVirtualMachineConfiguration`에서 `OSDisk` 속성이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1206">Removed `OSDisk` property from `PSVirtualMachineConfiguration`.</span></span>
* <span data-ttu-id="73f1f-1207">**Set-AzBatchPoolOSVersion**이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1207">Removed **Set-AzBatchPoolOSVersion**.</span></span> <span data-ttu-id="73f1f-1208">이 작업은 더 이상 지원되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1208">This operation is no longer supported.</span></span>
* <span data-ttu-id="73f1f-1209">`PSCloudServiceConfiguration`에서 `TargetOSVersion`이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1209">Removed `TargetOSVersion` from `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="73f1f-1210">`PSCloudServiceConfiguration`에서 `CurrentOSVersion` 이름이 `OSVersion`으로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1210">Renamed `CurrentOSVersion` to `OSVersion` on `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="73f1f-1211">`PSPoolUsageMetrics`에서 `DataEgressGiB` 및 `DataIngressGiB`가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1211">Removed `DataEgressGiB` and `DataIngressGiB` from `PSPoolUsageMetrics`.</span></span>
* <span data-ttu-id="73f1f-1212">**Get-AzBatchNodeAgentSku**가 제거되고 **Get-AzBatchSupportedImage**로 대체되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1212">Removed **Get-AzBatchNodeAgentSku** and replaced it with  **Get-AzBatchSupportedImage**.</span></span>
  - <span data-ttu-id="73f1f-1213">**Get-AzBatchSupportedImage**가 **Get-AzBatchNodeAgentSku**와 동일한 데이터를 반환하지만 더 친숙한 형식이 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1213">**Get-AzBatchSupportedImage** returns the same data as **Get-AzBatchNodeAgentSku** but in a more friendly format.</span></span>
  - <span data-ttu-id="73f1f-1214">이제 확인되지 않은 이미지도 새롭게 반환됩니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1214">New non-verified images are also now returned.</span></span> <span data-ttu-id="73f1f-1215">각 이미지의 `Capabilities` 및 `BatchSupportEndOfLife`에 대한 추가 정보도 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1215">Additional information about `Capabilities` and `BatchSupportEndOfLife` for each image is also included.</span></span>
* <span data-ttu-id="73f1f-1216">**New-AzBatchPool**의 새로운 `MountConfiguration` 매개 변수를 통해 풀의 각 노드에서 원격 파일 시스템을 마운트할 수 있는 기능이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1216">Added ability to mount remote file-systems on each node of a pool via the new `MountConfiguration` parameter of **New-AzBatchPool**.</span></span>
* <span data-ttu-id="73f1f-1217">이제 트래픽의 소스 포트를 기준으로 풀에 대한 네트워크 액세스를 차단하는 네트워크 보안 규칙이 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1217">Now support network security rules blocking network access to a pool based on the source port of the traffic.</span></span> <span data-ttu-id="73f1f-1218">이 작업은 `PSNetworkSecurityGroupRule`에서 `SourcePortRanges` 속성을 통해 수행됩니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1218">This is done via the `SourcePortRanges` property on `PSNetworkSecurityGroupRule`.</span></span>
* <span data-ttu-id="73f1f-1219">컨테이너를 실행할 때 Batch는 이제 컨테이너 작업 디렉터리 또는 일괄 처리 태스크 작업 디렉터리에서 작업 실행을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1219">When running a container, Batch now supports executing the task in the container working directory or in the Batch task working directory.</span></span> <span data-ttu-id="73f1f-1220">이 작업은 `PSTaskContainerSettings`에서 `WorkingDirectory` 속성에 의해 제어됩니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1220">This is controlled by the `WorkingDirectory` property on `PSTaskContainerSettings`.</span></span>
* <span data-ttu-id="73f1f-1221">새로운 `PublicIPs` 속성을 통해 `PSNetworkConfiguration`에서 공용 IP의 컬렉션을 지정할 수 있는 기능이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1221">Added ability to specify a collection of public IPs on `PSNetworkConfiguration` via the new `PublicIPs` property.</span></span> <span data-ttu-id="73f1f-1222">그 결과 사용자 제공 IP 목록의 IP가 풀에 있는 노드에 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1222">This guarantees nodes in the Pool will have an IP from the list user provided IPs.</span></span>
* <span data-ttu-id="73f1f-1223">지정하지 않은 경우 이제 `PSSTartTask`에서 `WaitForSuccess`의 기본값은 `$True`입니다(이전에는 `$False`).</span><span class="sxs-lookup"><span data-stu-id="73f1f-1223">When not specified, the default value of `WaitForSuccess` on `PSSTartTask` is now `$True` (was `$False`).</span></span>
* <span data-ttu-id="73f1f-1224">지정하지 않은 경우 이제 `PSAutoUserSpecification`에서 `Scope`의 기본값은 `Pool`입니다(이전에는 Windows의 경우 `Task`, Linux의 경우에는 `Pool`).</span><span class="sxs-lookup"><span data-stu-id="73f1f-1224">When not specified, the default value of `Scope` on `PSAutoUserSpecification` is now `Pool` (was `Task` on Windows and `Pool` on Linux).</span></span>

#### <a name="azcdn"></a><span data-ttu-id="73f1f-1225">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="73f1f-1225">Az.Cdn</span></span>
* <span data-ttu-id="73f1f-1226">RulesEngine에 UrlRewriteAction 및 CacheKeyQueryStringAction이 도입되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1226">Introduced UrlRewriteAction and CacheKeyQueryStringAction to RulesEngine.</span></span>
* <span data-ttu-id="73f1f-1227">New-AzDeliveryRuleCondition cmdlet에서 'Selector' 입력 누락과 같은 여러 버그가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1227">Fixed several bugs like missing 'Selector' Input in New-AzDeliveryRuleCondition cmdlet.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="73f1f-1228">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="73f1f-1228">Az.Compute</span></span>
* <span data-ttu-id="73f1f-1229">디스크 암호화 집합 기능</span><span class="sxs-lookup"><span data-stu-id="73f1f-1229">Disk Encryption Set feature</span></span>
    - <span data-ttu-id="73f1f-1230">새 cmdlet:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="73f1f-1230">New cmdlets:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span></span>
    - <span data-ttu-id="73f1f-1231">DiskEncryptionSetId 매개 변수가 다음 cmdlet에 추가되었습니다.   Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="73f1f-1231">DiskEncryptionSetId parameter is added to the following cmdlets:   Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span></span>
    - <span data-ttu-id="73f1f-1232">DiskEncryptionSetId 및 EncryptionType 매개 변수가 다음 cmdlet에 추가되었습니다.   New-AzDiskConfig   New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="73f1f-1232">DiskEncryptionSetId and EncryptionType parameters are added to the following cmdlets:   New-AzDiskConfig   New-AzSnapshotConfig</span></span>
* <span data-ttu-id="73f1f-1233">New-AzVmssIPConfig에 PublicIPAddressVersion 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="73f1f-1233">Add PublicIPAddressVersion parameter to New-AzVmssIPConfig</span></span>
* <span data-ttu-id="73f1f-1234">사용자 지정 스크립트 확장의 FileUris를 공용 설정에서 보호된 설정으로 이동</span><span class="sxs-lookup"><span data-stu-id="73f1f-1234">Move FileUris of custom script extension from public setting to protected setting</span></span>
* <span data-ttu-id="73f1f-1235">New-AzVmss, New-AzVmssConfig 및 Update-AzVmss cmdlet에 ScaleInPolicy 추가</span><span class="sxs-lookup"><span data-stu-id="73f1f-1235">Add ScaleInPolicy to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>
* <span data-ttu-id="73f1f-1236">주요 변경 내용</span><span class="sxs-lookup"><span data-stu-id="73f1f-1236">Breaking changes</span></span>
    - <span data-ttu-id="73f1f-1237">CreateOption이 업로드일 때 UploadSizeInBytes 매개 변수가 New-AzDiskConfig에 대해 DiskSizeGB 대신 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1237">UploadSizeInBytes parameter is used instead of DiskSizeGB for New-AzDiskConfig when CreateOption is Upload</span></span>
    - <span data-ttu-id="73f1f-1238">GalleryImageVersion 개체에서 PublishingProfile.Source.ManagedImage.Id가 StorageProfile.Source.Id로 바뀝니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1238">PublishingProfile.Source.ManagedImage.Id is replaced with StorageProfile.Source.Id in GalleryImageVersion object</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="73f1f-1239">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="73f1f-1239">Az.DataFactory</span></span>
* <span data-ttu-id="73f1f-1240">ADF .Net SDK 버전을 4.3.0으로 업데이트</span><span class="sxs-lookup"><span data-stu-id="73f1f-1240">Update ADF .Net SDK version to 4.3.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="73f1f-1241">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="73f1f-1241">Az.DataLakeStore</span></span>
* <span data-ttu-id="73f1f-1242">ADLS SDK 버전 업데이트(https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha) , 다음 수정 사항 제공</span><span class="sxs-lookup"><span data-stu-id="73f1f-1242">Update ADLS SDK version (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), brings following fixes</span></span>
* <span data-ttu-id="73f1f-1243">휴지통 또는 디렉터리 항목의 creationtime을 역직렬화할 수 없을 때 예외가 발생하지 않도록 방지합니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1243">Avoid throwing exception while unable to deserialize the creationtime of the trash or directory entry.</span></span>
* <span data-ttu-id="73f1f-1244">adlsclient에서 요청별 시간 제한 설정 노출</span><span class="sxs-lookup"><span data-stu-id="73f1f-1244">Expose setting per request timeout in adlsclient</span></span>
* <span data-ttu-id="73f1f-1245">badoffset 복구를 위한 원본 syncflag 전달 수정</span><span class="sxs-lookup"><span data-stu-id="73f1f-1245">Fix passing the original syncflag for badoffset recovery</span></span>
* <span data-ttu-id="73f1f-1246">응답이 확인된 후 연속 토큰을 검색하기 위한 EnumerateDirectory 수정</span><span class="sxs-lookup"><span data-stu-id="73f1f-1246">Fix EnumerateDirectory to retrieve continuation token once response is checked</span></span>
* <span data-ttu-id="73f1f-1247">Concat 버그 수정</span><span class="sxs-lookup"><span data-stu-id="73f1f-1247">Fix Concat Bug</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="73f1f-1248">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="73f1f-1248">Az.FrontDoor</span></span>
* <span data-ttu-id="73f1f-1249">모듈 간 기타 오타가 수정됨</span><span class="sxs-lookup"><span data-stu-id="73f1f-1249">Fixed miscellaneous typos across module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="73f1f-1250">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="73f1f-1250">Az.HDInsight</span></span>
* <span data-ttu-id="73f1f-1251">ADLSGen1 스토리지가 포함된 클러스터를 가져오기 위해 Get-AzHDInsightCluster를 사용할 때 고객에게 '올바른 Base-64 문자열이 아닙니다' 오류가 표시되는 버그가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1251">Fixed the bug that customer will get 'Not a valid Base-64 string' error when using Get-AzHDInsightCluster to get the cluster with ADLSGen1 storage.</span></span>
* <span data-ttu-id="73f1f-1252">고객이 Azure Data Lake에 액세스하기 위해 서비스 주체 애플리케이션 ID를 제공할 수 있도록 세 가지 cmdlet Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig 및 New-AzHDInsightCluster에 이름이 'ApplicationId'인 매개 변수를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1252">Add a parameter named 'ApplicationId' to three cmdlets Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig and New-AzHDInsightCluster so that customer can provide the service principal application id for accessing Azure Data Lake.</span></span>
* <span data-ttu-id="73f1f-1253">Microsoft.Azure.Management.HDInsight가 2.1.0에서 5.1.0으로 변경됨</span><span class="sxs-lookup"><span data-stu-id="73f1f-1253">Changed Microsoft.Azure.Management.HDInsight from 2.1.0 to 5.1.0</span></span>
* <span data-ttu-id="73f1f-1254">다음 5가지 cmdlet이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1254">Removed five cmdlets:</span></span>
    - <span data-ttu-id="73f1f-1255">Get-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="73f1f-1255">Get-AzHDInsightOMS</span></span>
    - <span data-ttu-id="73f1f-1256">Enable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="73f1f-1256">Enable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="73f1f-1257">Disable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="73f1f-1257">Disable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="73f1f-1258">Grant-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="73f1f-1258">Grant-AzHDInsightRdpServicesAccess</span></span>
    - <span data-ttu-id="73f1f-1259">Revoke-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="73f1f-1259">Revoke-AzHDInsightRdpServicesAccess</span></span>
* <span data-ttu-id="73f1f-1260">다음 3가지 cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1260">Added three cmdlets:</span></span>
    - <span data-ttu-id="73f1f-1261">Get-AzHDInsightOMS 대신 Get-AzHDInsightMonitoring</span><span class="sxs-lookup"><span data-stu-id="73f1f-1261">Get-AzHDInsightMonitoring to replace Get-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="73f1f-1262">Get-AzHDInsightOMS 대신 Get-AzHDInsightMonitoring</span><span class="sxs-lookup"><span data-stu-id="73f1f-1262">Enable-AzHDInsightMonitoring to replace Enable-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="73f1f-1263">Disable-AzHDInsightOMS 대신 Disable-AzHDInsightMonitoring</span><span class="sxs-lookup"><span data-stu-id="73f1f-1263">Disable-AzHDInsightMonitoring to replace Disable-AzHDInsightOMS.</span></span>
* <span data-ttu-id="73f1f-1264">특정 위치의 기능 정보 가져오기를 지원하도록 cmdlet Get-AzHDInsightProperties가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1264">Fixed cmdlet Get-AzHDInsightProperties to support get capabilities information from a specific location.</span></span>
* <span data-ttu-id="73f1f-1265">Add-AzHDInsightConfigValue에서 매개 변수 집합('Spark1', 'Spark2')이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1265">Removed parameter sets('Spark1', 'Spark2') from Add-AzHDInsightConfigValue.</span></span>
* <span data-ttu-id="73f1f-1266">cmdlet Add-AzHDInsightSecurityProfile의 도움말 문서에 예제를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1266">Add examples to the help documents of cmdlet Add-AzHDInsightSecurityProfile.</span></span>
* <span data-ttu-id="73f1f-1267">다음 cmdlet의 출력 유형이 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1267">Changed output type of the following cmdlets:</span></span>
*  - <span data-ttu-id="73f1f-1268">Get-AzHDInsightProperties의 출력 유형이 CapabilitiesResponse에서 AzureHDInsightCapabilities로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1268">Changed the output type of Get-AzHDInsightProperties from  CapabilitiesResponse to AzureHDInsightCapabilities.</span></span>
*  - <span data-ttu-id="73f1f-1269">Remove-AzHDInsightCluster의 출력 유형이 ClusterGetResponse에서 bool로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1269">Changed the output type of Remove-AzHDInsightCluster from ClusterGetResponse to bool.</span></span>
*  - <span data-ttu-id="73f1f-1270">Set-AzHDInsightGatewaySettings의 출력 유형이 HttpConnectivitySettings에서 GatewaySettings로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1270">Changed the output type of Set-AzHDInsightGatewaySettings HttpConnectivitySettings to GatewaySettings.</span></span>
* <span data-ttu-id="73f1f-1271">몇 가지 시나리오 테스트 사례가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1271">Added some scenario test cases.</span></span>
* <span data-ttu-id="73f1f-1272">일부 별칭 제거: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1272">Remove some alias: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="73f1f-1273">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="73f1f-1273">Az.IotHub</span></span>
* <span data-ttu-id="73f1f-1274">주요 변경 내용:</span><span class="sxs-lookup"><span data-stu-id="73f1f-1274">Breaking changes:</span></span>
    - <span data-ttu-id="73f1f-1275">'Add-AzIotHubEventHubConsumerGroup' cmdlet이 'EventHubEndpointName' 매개 변수를 더 이상 지원하지 않으며 원래 매개 변수 이름에 대해 별칭을 찾을 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1275">The cmdlet 'Add-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="73f1f-1276">'Add-AzIotHubEventHubConsumerGroup' cmdlet에 대한 매개 변수 집합 '__AllParameterSets'가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1276">The parameter set '__AllParameterSets' for cmdlet 'Add-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="73f1f-1277">'Get-AzIotHubEventHubConsumerGroup' cmdlet이 'EventHubEndpointName' 매개 변수를 더 이상 지원하지 않으며 원래 매개 변수 이름에 대해 별칭을 찾을 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1277">The cmdlet 'Get-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="73f1f-1278">'Get-AzIotHubEventHubConsumerGroup' cmdlet에 대한 매개 변수 집합 '__AllParameterSets'가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1278">The parameter set '__AllParameterSets' for cmdlet 'Get-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="73f1f-1279">'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' 유형의 'OperationsMonitoringProperties' 속성이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1279">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' has been removed.</span></span>
    - <span data-ttu-id="73f1f-1280">'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' 유형의 'OperationsMonitoringProperties' 속성이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1280">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' has been removed.</span></span>
    - <span data-ttu-id="73f1f-1281">'New-AzIotHubExportDevice' cmdlet이 더 이상 'New-AzIotHubExportDevices' 별칭을 지원하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1281">The cmdlet 'New-AzIotHubExportDevice' no longer supports the alias 'New-AzIotHubExportDevices'.</span></span>
    - <span data-ttu-id="73f1f-1282">'New-AzIotHubImportDevice' cmdlet이 더 이상 'New-AzIotHubImportDevices' 별칭을 지원하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1282">The cmdlet 'New-AzIotHubImportDevice' no longer supports the alias 'New-AzIotHubImportDevices'.</span></span>
    - <span data-ttu-id="73f1f-1283">'Remove-AzIotHubEventHubConsumerGroup' cmdlet이 'EventHubEndpointName' 매개 변수를 더 이상 지원하지 않으며 원래 매개 변수 이름에 대해 별칭을 찾을 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1283">The cmdlet 'Remove-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="73f1f-1284">'Remove-AzIotHubEventHubConsumerGroup' cmdlet에 대한 매개 변수 집합 '__AllParameterSets'가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1284">The parameter set '__AllParameterSets' for cmdlet 'Remove-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="73f1f-1285">'Set-AzIotHub' cmdlet이 'OperationsMonitoringProperties' 매개 변수를 더 이상 지원하지 않으며 원래 매개 변수 이름에 대해 별칭을 찾을 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1285">The cmdlet 'Set-AzIotHub' no longer supports the parameter 'OperationsMonitoringProperties' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="73f1f-1286">'Set-AzIotHub' cmdlet에 대한 매개 변수 집합 'UpdateOperationsMonitoringProperties'가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1286">The parameter set 'UpdateOperationsMonitoringProperties' for cmdlet 'Set-AzIotHub' has been removed.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="73f1f-1287">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="73f1f-1287">Az.RecoveryServices</span></span>
* <span data-ttu-id="73f1f-1288">Azure Site Recovery가 Azure-Azure를 위한 NSG, 공용 IP 및 내부 부하 분산 장치와 같은 네트워킹 리소스 구성을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1288">Azure Site Recovery support to configure networking resources like NSG, public IP and internal load balancers for Azure to Azure.</span></span>
* <span data-ttu-id="73f1f-1289">Azure Site Recovery가 vMWare-Azure를 위한 관리 디스크에 쓰기를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1289">Azure Site Recovery Support to write to managed disk for vMWare to Azure.</span></span>
* <span data-ttu-id="73f1f-1290">Azure Site Recovery가 vMWare-Azure를 위한 NIC 감소를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1290">Azure Site Recovery Support to NIC reduction for vMWare to Azure.</span></span>
* <span data-ttu-id="73f1f-1291">Azure Site Recovery가 Azure-Azure를 위한 가속 네트워킹을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1291">Azure Site Recovery Support to accelerated networking for Azure to Azure.</span></span>
* <span data-ttu-id="73f1f-1292">Azure Site Recovery가 Azure-Azure를 위한 에이전트 자동 업데이트를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1292">Azure Site Recovery Support to agent auto update for Azure to Azure.</span></span>
* <span data-ttu-id="73f1f-1293">Azure Site Recovery가 Azure-Azure를 위한 표준 SSD를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1293">Azure Site Recovery Support to Standard SSD for Azure to Azure.</span></span>
* <span data-ttu-id="73f1f-1294">Azure Site Recovery가 Azure-Azure를 위한 두 가지 Azure 디스크 암호화 전달을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1294">Azure Site Recovery Support to Azure Disk Encryption two pass for Azure to Azure.</span></span>
* <span data-ttu-id="73f1f-1295">Azure Site Recovery가 Azure-Azure를 위한 새로 추가된 디스크 보호를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1295">Azure Site Recovery Support to protect newly added disk for Azure to Azure.</span></span>
* <span data-ttu-id="73f1f-1296">VM을 위한 SoftDelete 기능 및 softdelete를 위한 테스트가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1296">Added SoftDelete feature for VM and added tests for softdelete</span></span>

#### <a name="azresources"></a><span data-ttu-id="73f1f-1297">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="73f1f-1297">Az.Resources</span></span>
* <span data-ttu-id="73f1f-1298">종속성 어셈블리 Microsoft.Extensions.Caching.Memory가 1.1.1에서 2.2로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1298">Update dependency assembly Microsoft.Extensions.Caching.Memory from 1.1.1 to 2.2</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="73f1f-1299">Az.Network</span><span class="sxs-lookup"><span data-stu-id="73f1f-1299">Az.Network</span></span>
* <span data-ttu-id="73f1f-1300">일반 서비스 공급자 지원을 위해 PrivateEndpointConnection에 대한 모든 cmdlet이 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1300">Change all cmdlets for PrivateEndpointConnection to support generic service provider.</span></span>
    - <span data-ttu-id="73f1f-1301">업데이트된 cmdlet:</span><span class="sxs-lookup"><span data-stu-id="73f1f-1301">Updated cmdlet:</span></span>
        - <span data-ttu-id="73f1f-1302">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="73f1f-1302">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="73f1f-1303">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="73f1f-1303">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="73f1f-1304">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="73f1f-1304">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="73f1f-1305">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="73f1f-1305">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="73f1f-1306">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="73f1f-1306">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="73f1f-1307">PrivateLinkResource에 대한 새 cmdlet이 추가되었고 일반 서비스 공급자도 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1307">Add new cmdlet for PrivateLinkResource and it also support generic service provider.</span></span>
    - <span data-ttu-id="73f1f-1308">새 cmdlet:</span><span class="sxs-lookup"><span data-stu-id="73f1f-1308">New cmdlet:</span></span>
        - <span data-ttu-id="73f1f-1309">Get-AzPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="73f1f-1309">Get-AzPrivateLinkResource</span></span>
* <span data-ttu-id="73f1f-1310">Proxy Protocol V2 기능에 대한 새 필드 및 매개 변수가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1310">Add new fields and parameter for the feature Proxy Protocol V2.</span></span>
    - <span data-ttu-id="73f1f-1311">PrivateLinkService에서 EnableProxyProtocol 속성 추가</span><span class="sxs-lookup"><span data-stu-id="73f1f-1311">Add property EnableProxyProtocol in PrivateLinkService</span></span>
    - <span data-ttu-id="73f1f-1312">PrivateEndpointConnection에서 LinkIdentifier 속성 추가</span><span class="sxs-lookup"><span data-stu-id="73f1f-1312">Add property LinkIdentifier in PrivateEndpointConnection</span></span>
    - <span data-ttu-id="73f1f-1313">새로운 선택적인 매개 변수인 EnableProxyProtocol을 추가하도록 New-AzPrivateLinkService가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1313">Updated New-AzPrivateLinkService to add a new optional parameter EnableProxyProtocol.</span></span>
* <span data-ttu-id="73f1f-1314">'New-AzApplicationGatewaySku' 참조 설명서의 잘못된 매개 변수 설명 수정</span><span class="sxs-lookup"><span data-stu-id="73f1f-1314">Fix incorrect parameter description in 'New-AzApplicationGatewaySku' reference documentation</span></span>
* <span data-ttu-id="73f1f-1315">Azure 방화벽 정책을 지원하는 새로운 cmdlet</span><span class="sxs-lookup"><span data-stu-id="73f1f-1315">New cmdlets to support the azure firewall policy</span></span>
* <span data-ttu-id="73f1f-1316">VirtualHub의 자식 리소스 RouteTables에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="73f1f-1316">Add support for child resource RouteTables of VirtualHub</span></span>
    - <span data-ttu-id="73f1f-1317">추가된 새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1317">New cmdlets added:</span></span>
        - <span data-ttu-id="73f1f-1318">Add-AzVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="73f1f-1318">Add-AzVirtualHubRoute</span></span>
        - <span data-ttu-id="73f1f-1319">Add-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="73f1f-1319">Add-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="73f1f-1320">Get-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="73f1f-1320">Get-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="73f1f-1321">Remove-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="73f1f-1321">Remove-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="73f1f-1322">Set-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="73f1f-1322">Set-AzVirtualHub</span></span>
* <span data-ttu-id="73f1f-1323">VirtualHub의 새로운 속성 Sku 및 VirtualWan의 VirtualWANType에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="73f1f-1323">Add support for new properties Sku of VirtualHub and VirtualWANType of VirtualWan</span></span>
    - <span data-ttu-id="73f1f-1324">선택적 매개 변수로 다음 cmdlet이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1324">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="73f1f-1325">New-AzVirtualHub: 추가된 매개 변수 Sku</span><span class="sxs-lookup"><span data-stu-id="73f1f-1325">New-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="73f1f-1326">Update-AzVirtualHub: 추가된 매개 변수 Sku</span><span class="sxs-lookup"><span data-stu-id="73f1f-1326">Update-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="73f1f-1327">New-AzVirtualWan: 추가된 매개 변수 VirtualWANType</span><span class="sxs-lookup"><span data-stu-id="73f1f-1327">New-AzVirtualWan : added parameter VirtualWANType</span></span>
        - <span data-ttu-id="73f1f-1328">Update-AzVirtualWan: 추가된 매개 변수 VirtualWANType</span><span class="sxs-lookup"><span data-stu-id="73f1f-1328">Update-AzVirtualWan : added parameter VirtualWANType</span></span>
* <span data-ttu-id="73f1f-1329">HubVnetConnection, VpnConnection 및 ExpressRouteConnection에 대한 EnableInternetSecurity 속성 지원 추가</span><span class="sxs-lookup"><span data-stu-id="73f1f-1329">Add support for EnableInternetSecurity property for HubVnetConnection, VpnConnection and ExpressRouteConnection</span></span>
    - <span data-ttu-id="73f1f-1330">추가된 새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1330">New cmdlets added:</span></span>
        - <span data-ttu-id="73f1f-1331">Update-AzureRmVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="73f1f-1331">Update-AzureRmVirtualHubVnetConnection</span></span>
    - <span data-ttu-id="73f1f-1332">선택적 매개 변수로 다음 cmdlet이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1332">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="73f1f-1333">New-AzureRmVirtualHubVnetConnection: 추가된 매개 변수 EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="73f1f-1333">New-AzureRmVirtualHubVnetConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="73f1f-1334">New-AzureRmVpnConnection: 추가된 매개 변수 EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="73f1f-1334">New-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="73f1f-1335">Update-AzureRmVpnConnection: 추가된 매개 변수 EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="73f1f-1335">Update-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="73f1f-1336">New-AzureRmExpressRouteConnection: 추가된 매개 변수 EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="73f1f-1336">New-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="73f1f-1337">Set-AzureRmExpressRouteConnection: 추가된 매개 변수 EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="73f1f-1337">Set-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
* <span data-ttu-id="73f1f-1338">TopLevel WebApplicationFirewall 정책 구성을 위한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="73f1f-1338">Add support for Configuring TopLevel WebApplicationFirewall Policy</span></span>
    - <span data-ttu-id="73f1f-1339">추가된 새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1339">New cmdlets added:</span></span>
        - <span data-ttu-id="73f1f-1340">New-AzApplicationGatewayFirewallPolicySetting</span><span class="sxs-lookup"><span data-stu-id="73f1f-1340">New-AzApplicationGatewayFirewallPolicySetting</span></span>
        - <span data-ttu-id="73f1f-1341">New-AzApplicationGatewayFirewallPolicyExclusion</span><span class="sxs-lookup"><span data-stu-id="73f1f-1341">New-AzApplicationGatewayFirewallPolicyExclusion</span></span>
        - <span data-ttu-id="73f1f-1342">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="73f1f-1342">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span></span>
        - <span data-ttu-id="73f1f-1343">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="73f1f-1343">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span></span>
        - <span data-ttu-id="73f1f-1344">New-AzApplicationGatewayFirewallPolicyManagedRule</span><span class="sxs-lookup"><span data-stu-id="73f1f-1344">New-AzApplicationGatewayFirewallPolicyManagedRule</span></span>
        - <span data-ttu-id="73f1f-1345">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="73f1f-1345">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span></span>
    - <span data-ttu-id="73f1f-1346">선택적 매개 변수로 다음 cmdlet이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1346">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="73f1f-1347">New-AzApplicationGatewayFirewallPolicy: 추가된 매개 변수 PolicySetting, ManagedRule</span><span class="sxs-lookup"><span data-stu-id="73f1f-1347">New-AzApplicationGatewayFirewallPolicy : added parameter PolicySetting, ManagedRule</span></span>
* <span data-ttu-id="73f1f-1348">CustomRule에서 Geo-Match 연산자를 위한 지원 추가됨</span><span class="sxs-lookup"><span data-stu-id="73f1f-1348">Added support for Geo-Match operator on CustomRule</span></span>
    - <span data-ttu-id="73f1f-1349">FirewallCondition에서 연산자에 GeoMatch 추가됨</span><span class="sxs-lookup"><span data-stu-id="73f1f-1349">Added GeoMatch to the operator on the FirewallCondition</span></span>
* <span data-ttu-id="73f1f-1350">perListener 및 perSite 방화벽 규칙에 대한 지원 추가됨</span><span class="sxs-lookup"><span data-stu-id="73f1f-1350">Added support for perListener and perSite Firewall policy</span></span>
    - <span data-ttu-id="73f1f-1351">선택적 매개 변수로 다음 cmdlet이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1351">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="73f1f-1352">New-AzApplicationGatewayHttpListener: 추가된 매개 변수 FirewallPolicy, FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="73f1f-1352">New-AzApplicationGatewayHttpListener : added parameter FirewallPolicy, FirewallPolicyId</span></span>
        - <span data-ttu-id="73f1f-1353">New-AzApplicationGatewayPathRuleConfig: 추가된 매개 변수 FirewallPolicy, FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="73f1f-1353">New-AzApplicationGatewayPathRuleConfig : added parameter FirewallPolicy, FirewallPolicyId</span></span>
* <span data-ttu-id="73f1f-1354">'PSBastion'에서 이름이 AzureBastionSubnet인 필수 서브넷의 수정은 대소문자를 구분하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1354">Fix required subnet with name AzureBastionSubnet in 'PSBastion' can be case insensitive</span></span>
* <span data-ttu-id="73f1f-1355">Azure Firewall을 위한 네트워크 규칙의 대상 FQDN 및 NAT 규칙의 번역된 FQDN 지원</span><span class="sxs-lookup"><span data-stu-id="73f1f-1355">Support for Destination FQDNs in Network Rules and Translated FQDN in NAT Rules for Azure Firewall</span></span>
* <span data-ttu-id="73f1f-1356">IpGroup의 최상위 리소스 RouteTables에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="73f1f-1356">Add support for top level resource RouteTables of IpGroup</span></span>
    - <span data-ttu-id="73f1f-1357">추가된 새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1357">New cmdlets added:</span></span>
        - <span data-ttu-id="73f1f-1358">New-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="73f1f-1358">New-AzIpGroup</span></span>
        - <span data-ttu-id="73f1f-1359">Remove-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="73f1f-1359">Remove-AzIpGroup</span></span>
        - <span data-ttu-id="73f1f-1360">Get-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="73f1f-1360">Get-AzIpGroup</span></span>
        - <span data-ttu-id="73f1f-1361">Set-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="73f1f-1361">Set-AzIpGroup</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="73f1f-1362">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="73f1f-1362">Az.ServiceFabric</span></span>
* <span data-ttu-id="73f1f-1363">Add-AzVmssSecret에서 지원되기 때문에 Add-AzServiceFabricApplicationCertificate cmdlet이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1363">Remove Add-AzServiceFabricApplicationCertificate cmdlet as this scenario is covered by Add-AzVmssSecret.</span></span>

#### <a name="azsql"></a><span data-ttu-id="73f1f-1364">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="73f1f-1364">Az.Sql</span></span>
* <span data-ttu-id="73f1f-1365">Managed Instances에서 삭제된 데이터베이스의 복원을 위한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1365">Added support for restore of dropped databases on Managed Instances.</span></span>
* <span data-ttu-id="73f1f-1366">이전의 감사 cmdlet 코드가 사용되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1366">Deprecated from code old auditing cmdlets.</span></span>
* <span data-ttu-id="73f1f-1367">사용되지 않는 별칭이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1367">Removed deprecated aliases:</span></span>
* <span data-ttu-id="73f1f-1368">Get-AzSqlDatabaseIndexRecommendations(대신 Get-AzSqlDatabaseIndexRecommendation 사용)</span><span class="sxs-lookup"><span data-stu-id="73f1f-1368">Get-AzSqlDatabaseIndexRecommendations (use Get-AzSqlDatabaseIndexRecommendation instead)</span></span>
* <span data-ttu-id="73f1f-1369">Get-AzSqlDatabaseRestorePoints(대신 Get-AzSqlDatabaseRestorePoint 사용)</span><span class="sxs-lookup"><span data-stu-id="73f1f-1369">Get-AzSqlDatabaseRestorePoints (use Get-AzSqlDatabaseRestorePoint instead)</span></span>
* <span data-ttu-id="73f1f-1370">Get-AzSqlDatabaseSecureConnectionPolicy cmdlet 제거</span><span class="sxs-lookup"><span data-stu-id="73f1f-1370">Remove Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="73f1f-1371">사용되지 않는 취약성 평가 설정 cmdlet에 대한 별칭 제거</span><span class="sxs-lookup"><span data-stu-id="73f1f-1371">Remove aliases for deprecated Vulnerability Assessment Settings cmdlets</span></span>
* <span data-ttu-id="73f1f-1372">지능형 위협 탐지 설정 cmdlet 사용 중단</span><span class="sxs-lookup"><span data-stu-id="73f1f-1372">Deprecate Advanced Threat Detection Settings cmdlets</span></span>
* <span data-ttu-id="73f1f-1373">데이터베이스의 열에 대한 민감도 권장 사항의 사용 여부를 제어하는 cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1373">Adding cmdlets to Disable and enable sensitivity recommendations on columns in a database.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="73f1f-1374">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="73f1f-1374">Az.Storage</span></span>
* <span data-ttu-id="73f1f-1375">스토리지 계정을 만들거나 업데이트할 때 큰 파일 공유 사용 지원</span><span class="sxs-lookup"><span data-stu-id="73f1f-1375">Support enable Large File share when create or update Storage account</span></span>
    -  <span data-ttu-id="73f1f-1376">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="73f1f-1376">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="73f1f-1377">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="73f1f-1377">Set-AzStorageAccount</span></span>
* <span data-ttu-id="73f1f-1378">파일 핸들을 닫거나/가져올 때, DeletePending 상태의 개체로 인한 오류를 방지하기 위해 입력 경로가 파일 디렉터리인지 또는 파일인지를 확인하는 과정을 건너뜁니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1378">When close/get File handle, skip check the input path is File directory or File, to avoid failure with object in DeletePending status</span></span>
    -  <span data-ttu-id="73f1f-1379">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="73f1f-1379">Get-AzStorageFileHandle</span></span>
    -  <span data-ttu-id="73f1f-1380">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="73f1f-1380">Close-AzStorageFileHandle</span></span>

## <a name="280---october-2019"></a><span data-ttu-id="73f1f-1381">2.8.0 - 2019년 10월</span><span class="sxs-lookup"><span data-stu-id="73f1f-1381">2.8.0 - October 2019</span></span>
### <a name="general"></a><span data-ttu-id="73f1f-1382">일반</span><span class="sxs-lookup"><span data-stu-id="73f1f-1382">General</span></span>
* <span data-ttu-id="73f1f-1383">Az.HealthcareApis 1.0.0 릴리스</span><span class="sxs-lookup"><span data-stu-id="73f1f-1383">Az.HealthcareApis 1.0.0 release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="73f1f-1384">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="73f1f-1384">Az.Accounts</span></span>
* <span data-ttu-id="73f1f-1385">생성된 모듈에 대한 원격 분석 및 URL 다시 작성이 업데이트되고, Windows 단위 테스트가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1385">Update telemetry and url rewriting for generated modules, fix windows unit tests.</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="73f1f-1386">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="73f1f-1386">Az.ApiManagement</span></span>
* <span data-ttu-id="73f1f-1387">**Set-AzApiManagementApi** - API 업데이트 지원이 ApiVersionSet에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1387">**Set-AzApiManagementApi** - Added support for Updating Api into ApiVersionSet</span></span>
    - <span data-ttu-id="73f1f-1388">문제 https://github.com/Azure/azure-powershell/issues/10068 수정</span><span class="sxs-lookup"><span data-stu-id="73f1f-1388">Fix for issue https://github.com/Azure/azure-powershell/issues/10068</span></span>

#### <a name="azautomation"></a><span data-ttu-id="73f1f-1389">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="73f1f-1389">Az.Automation</span></span>
* <span data-ttu-id="73f1f-1390">Linux 다시 부팅 설정 매개 변수에 대한 New-AzureAutomationSoftwareUpdateConfiguration cmdlet이 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1390">Fixed New-AzureAutomationSoftwareUpdateConfiguration cmdlet for Linux reboot setting parameter.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="73f1f-1391">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="73f1f-1391">Az.Batch</span></span>
* <span data-ttu-id="73f1f-1392">**Get-AzBatchNodeAgentSku**가 더 이상 사용되지 않으며, 2.0.0 버전의 **Get-AzBatchSupportImage**로 대체되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1392">**Get-AzBatchNodeAgentSku** is deprecated and will be replaced by **Get-AzBatchSupportImage** in version 2.0.0.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="73f1f-1393">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="73f1f-1393">Az.Compute</span></span>
* <span data-ttu-id="73f1f-1394">Priority, EvictionPolicy 및 MaxPrice 매개 변수가 New-AzVM 및 New-AzVmss cmdlet에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1394">Add Priority, EvictionPolicy, and MaxPrice parameters to New-AzVM and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="73f1f-1395">Add-AzVMAdditionalUnattendContent 및 Add-AzVMSshPublicKey cmdlet에 대한 경고 메시지와 도움말 문서가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1395">Fix warning message and help document for Add-AzVMAdditionalUnattendContent and Add-AzVMSshPublicKey cmdlets</span></span>
* <span data-ttu-id="73f1f-1396">Set-AzVMDiskEncryptionExtension의 관리 디스크가 있는 Linux VM에 대한 -skipVmBackup 예외가 해결되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1396">Fix -skipVmBackup exception for Linux VMs with managed disks for Set-AzVMDiskEncryptionExtension.</span></span>
* <span data-ttu-id="73f1f-1397">Set-AzVMDiskEncryptionExtension의 두 가지 패스 시나리오에서 발생하는 암호화 설정 업데이트의 버그가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1397">Fix bug in update encryption settings in Set-AzVMDiskEncryptionExtension, two pass scenario.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="73f1f-1398">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="73f1f-1398">Az.DataFactory</span></span>
* <span data-ttu-id="73f1f-1399">ADF V2 데이터 흐름에 대한 CRUD 명령으로 Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow 및 Get-AzDataFactoryV2DataFlow가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1399">Adding CRUD commands for ADF V2 data flow: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow, and Get-AzDataFactoryV2DataFlow.</span></span>
* <span data-ttu-id="73f1f-1400">ADF V2 데이터 흐름 디버그 세션에 대한 작업 명령으로 Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand 및 Stop-AzDataFactoryV2DataFlowDebugSession이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1400">Adding action commands for ADF V2 data flow debug Session: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand and Stop-AzDataFactoryV2DataFlowDebugSession.</span></span>
* <span data-ttu-id="73f1f-1401">ADF .Net SDK 버전이 4.2.0으로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1401">Update ADF .Net SDK version to 4.2.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="73f1f-1402">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="73f1f-1402">Az.DataLakeStore</span></span>
* <span data-ttu-id="73f1f-1403">도메인 없이 '-'가 있는 계정을 전달할 수 있도록 계정 유효성 검사가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1403">Fix account validation so that accounts with '-' can be passed without domain</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="73f1f-1404">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="73f1f-1404">Az.HealthcareApis</span></span>
* <span data-ttu-id="73f1f-1405">PowerShell 버전이 1.0.0으로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1405">Updated the powershell version to 1.0.0</span></span>
* <span data-ttu-id="73f1f-1406">SDK 버전이 1.0.2로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1406">Updated the SDK version to 1.0.2</span></span>
* <span data-ttu-id="73f1f-1407">새 SDK 버전을 참조하도록 테스트가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1407">Update in tests to refer to new SDK version</span></span>
* <span data-ttu-id="73f1f-1408">출력이 중첩 구조에서 평면화 구조로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1408">Updated the output structure from nested to flattened.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="73f1f-1409">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="73f1f-1409">Az.IotHub</span></span>
* <span data-ttu-id="73f1f-1410">새 라우팅 원본 추가: DigitalTwinChangeEvents</span><span class="sxs-lookup"><span data-stu-id="73f1f-1410">Add new routing source: DigitalTwinChangeEvents</span></span>
* <span data-ttu-id="73f1f-1411">사소한 버그 수정: Get-AzIothub에서 subscriptionId를 반환하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1411">Minor bug fix: Get-AzIothub not returning subscriptionId</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="73f1f-1412">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="73f1f-1412">Az.Monitor</span></span>
* <span data-ttu-id="73f1f-1413">작업 그룹에 대한 새 작업 그룹 수신기로 -ItsmReceiver, -VoiceReceiver, -ArmRoleReceiver, -AzureFunctionReceiver, -LogicAppReceiver, -AutomationRunbookReceiver, -AzureAppPushReceiver가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1413">New action group receivers added for action group   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span></span>
* <span data-ttu-id="73f1f-1414">수신기에 사용하도록 설정된 일반 경고 스키마가 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1414">Use common alert schema enabled for the receivers.</span></span> <span data-ttu-id="73f1f-1415">SMS, Azure 앱 푸시, ITSM 및 음성 수신기에는 적용되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1415">This is not applicable for SMS, Azure App push , ITSM and Voice recievers</span></span>
* <span data-ttu-id="73f1f-1416">웹후크에서 이제 Azure Active Directory 인증을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1416">Webhooks now supports Azure active directory authentication .</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="73f1f-1417">Az.Network</span><span class="sxs-lookup"><span data-stu-id="73f1f-1417">Az.Network</span></span>
* <span data-ttu-id="73f1f-1418">서비스 엔드포인트 정책에 사용할 수 있는 별칭을 가져오기 위해 호출할 수 있는 새 Get-AzAvailableServiceAlias cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1418">Add new cmdlet Get-AzAvailableServiceAlias which can be called to get the aliases that can be used for Service Endpoint Policies.</span></span>
* <span data-ttu-id="73f1f-1419">트래픽 선택기를 Virtual Network 게이트웨이 연결에 추가할 수 있는 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1419">Added support for the adding traffic selectors to Virtual Network Gateway Connections</span></span>
    - <span data-ttu-id="73f1f-1420">추가된 새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1420">New cmdlets added:</span></span>
        - <span data-ttu-id="73f1f-1421">New-AzureRmTrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="73f1f-1421">New-AzureRmTrafficSelectorPolicy</span></span>
    - <span data-ttu-id="73f1f-1422">cmdlet이 선택적인 -TrafficSelectorPolicies, -New-AzureRmVirtualNetworkGatewayConnection, -Set-AzureRmVirtualNetworkGatewayConnection 매개 변수로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1422">Cmdlets updated with optional parameter -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="73f1f-1423">ESP 및 AH 프로토콜 지원이 네트워크 보안 규칙 구성에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1423">Add support for ESP and AH protocols in network security rule configurations</span></span>
    - <span data-ttu-id="73f1f-1424">다음 Cmdlet이 업데이트 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1424">Updated cmdlets:</span></span>
        - <span data-ttu-id="73f1f-1425">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="73f1f-1425">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="73f1f-1426">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="73f1f-1426">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="73f1f-1427">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="73f1f-1427">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="73f1f-1428">Cortex cmdlet의 예외 처리가 향상되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1428">Improve handling of exceptions in Cortex cmdlets</span></span>
* <span data-ttu-id="73f1f-1429">새 VirtualNetworkGateways 세대 및 SKU</span><span class="sxs-lookup"><span data-stu-id="73f1f-1429">New Generations and SKUs for VirtualNetworkGateways</span></span>
  - <span data-ttu-id="73f1f-1430">새 VirtualNetworkGateways 세대가 도입되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1430">Introduce new Generations for VirtualNetworkGateways.</span></span>
  - <span data-ttu-id="73f1f-1431">높은 처리량의 새 VirtualNetworkGateways SKU가 도입되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1431">Introduce new high throughput SKUs for VirtualNetworkGateways.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="73f1f-1432">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="73f1f-1432">Az.RedisCache</span></span>
* <span data-ttu-id="73f1f-1433">'-Size' 매개 변수에 대한 누락 값을 포함하도록 'Set-AzRedisCache' 참조 설명서가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1433">Updated 'Set-AzRedisCache' reference documentation to include missing values for '-Size' parameter</span></span>

#### <a name="azsql"></a><span data-ttu-id="73f1f-1434">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="73f1f-1434">Az.Sql</span></span>
* <span data-ttu-id="73f1f-1435">Managed Instance에서 Active Directory 관리자를 설정할 수 있는 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1435">Add support for setting Active Directory Administrator on Managed Instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="73f1f-1436">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="73f1f-1436">Az.Storage</span></span>
* <span data-ttu-id="73f1f-1437">스토리지 클라이언트 라이브러리가 11.1.0으로 업그레이드되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1437">Upgrade Storage Client Library to 11.1.0</span></span>
* <span data-ttu-id="73f1f-1438">관리 평면 API를 사용하여 컨테이너를 나열하면 NextPageLink를 통해 나열됩니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1438">List containers with Management plane API, will list with NextPageLink</span></span>
    -  <span data-ttu-id="73f1f-1439">Get-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="73f1f-1439">Get-AzRmStorageContainer</span></span>
* <span data-ttu-id="73f1f-1440">구독에서 스토리지 계정을 나열하면 NextPageLink를 통해 나열됩니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1440">List Storage accounts from subscription, will list with NextPageLink</span></span>
    -  <span data-ttu-id="73f1f-1441">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="73f1f-1441">Get-AzStorageAccount</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="73f1f-1442">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="73f1f-1442">Az.StorageSync</span></span>
* <span data-ttu-id="73f1f-1443">Reset-AzStorageSyncServerCertificate의 9810 문제가 해결되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1443">Fix Issue 9810 in Reset-AzStorageSyncServerCertificate.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="73f1f-1444">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="73f1f-1444">Az.Websites</span></span>
* <span data-ttu-id="73f1f-1445">앱의 ASP를 업데이트하는 Set-AzWebApp이 실패했습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1445">Set-AzWebApp updating ASP of an app was failing</span></span>

## <a name="270---september-2019"></a><span data-ttu-id="73f1f-1446">2.7.0 - 2019년 9월</span><span class="sxs-lookup"><span data-stu-id="73f1f-1446">2.7.0 - September 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="73f1f-1447">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="73f1f-1447">Az.ApiManagement</span></span>
* <span data-ttu-id="73f1f-1448">'Set-AzApiManagementPolicy' 참조 설명서에서 '-Format' 매개 변수 설명이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1448">Update '-Format' parameter description in 'Set-AzApiManagementPolicy' reference documentation</span></span>
* <span data-ttu-id="73f1f-1449">참조 설명서에서 사용되지 않는 cmdlet 'Update-AzApiManagementDeployment'의 참조를 제거했습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1449">Removed references of deprecated cmdlet 'Update-AzApiManagementDeployment' from reference documentation.</span></span> <span data-ttu-id="73f1f-1450">그 대신 'Set-AzApiManagement'를 사용하세요.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1450">Use 'Set-AzApiManagement' instead.</span></span>

#### <a name="azautomation"></a><span data-ttu-id="73f1f-1451">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="73f1f-1451">Az.Automation</span></span>
* <span data-ttu-id="73f1f-1452">'Register-AzAutomationDscNode'에 대한 참조 설명서의 예제 오타가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1452">Fixed example typo in reference documentation for 'Register-AzAutomationDscNode'</span></span>
* <span data-ttu-id="73f1f-1453">Register-AzAutomationDSCNode에 OS 제한에 대한 설명이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1453">Added clarification on OS restriction to Register-AzAutomationDSCNode</span></span>
* <span data-ttu-id="73f1f-1454">-Wait 옵션에 대한 Start-AzAutomationRunbook cmdlet Null 참조 예외가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1454">Fixed Start-AzAutomationRunbook cmdlet Null reference exception for -Wait option.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="73f1f-1455">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="73f1f-1455">Az.Compute</span></span>
* <span data-ttu-id="73f1f-1456">New-AzDiskConfig에 UploadSizeInBytes 매개 변수가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1456">Add UploadSizeInBytes parameter tp New-AzDiskConfig</span></span>
* <span data-ttu-id="73f1f-1457">New-AzSnapshotConfig에 증분 매개 변수가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1457">Add Incremental parameter to New-AzSnapshotConfig</span></span>
* <span data-ttu-id="73f1f-1458">다음과 같은 낮은 우선 순위의 가상 머신 기능이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1458">Add a low priority virtual machine feature:</span></span>
    - <span data-ttu-id="73f1f-1459">MaxPrice, EvictionPolicy 및 Priority 매개 변수가 New-AzVMConfig에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1459">MaxPrice, EvictionPolicy and Priority parameters are added to New-AzVMConfig.</span></span>
    - <span data-ttu-id="73f1f-1460">MaxPrice 매개 변수는 New-AzVmssConfig, Update-AzVM 및 Update-AzVmss cmdlet에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1460">MaxPrice parameter is added to New-AzVmssConfig, Update-AzVM and Update-AzVmss cmdlets.</span></span>
* <span data-ttu-id="73f1f-1461">구독의 모든 가용성 세트를 나열할 때 발생하는 Get-AzAvailabilitySet cmdlet에 대한 VM 참조 이슈가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1461">Fix VM reference issue for Get-AzAvailabilitySet cmdlet when it lists all availability sets in the subscription.</span></span>
* <span data-ttu-id="73f1f-1462">Get-AzRemoteDesktopFile에 대한 null 예외가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1462">Fix the null exception for Get-AzRemoteDesktopFile.</span></span>
* <span data-ttu-id="73f1f-1463">종료 상대 위치에 대한 VHD 검색 메서드가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1463">Fix VHD Seek method for end-relative position.</span></span>
* <span data-ttu-id="73f1f-1464">New-AzVM 및 Update-AzVM에 대한 UltraSSD 이슈가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1464">Fix UltraSSD issue for New-AzVM and Update-AzVM.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="73f1f-1465">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="73f1f-1465">Az.DataFactory</span></span>
* <span data-ttu-id="73f1f-1466">ADF V2에 대한 3가지 새 명령 Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription 및 Get-AzDataFactoryV2TriggerSubscriptionStatus가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1466">Adding 3 new commands for ADF V2 - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription, and Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>
* <span data-ttu-id="73f1f-1467">ADF .Net SDK 버전이 4.1.3으로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1467">Updated ADF .Net SDK version to 4.1.3</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="73f1f-1468">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="73f1f-1468">Az.HDInsight</span></span>
* <span data-ttu-id="73f1f-1469">호출 주요 변경 내용</span><span class="sxs-lookup"><span data-stu-id="73f1f-1469">Call out breaking changes</span></span>

#### <a name="aziothub"></a><span data-ttu-id="73f1f-1470">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="73f1f-1470">Az.IotHub</span></span>
* <span data-ttu-id="73f1f-1471">지역 쌍 재해 복구 지역에 IotHub에 대한 장애 조치(failover) 호출 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1471">Add support to invoke failover for an IotHub to the geo-paired disaster recovery region.</span></span>
* <span data-ttu-id="73f1f-1472">IotHub에 대한 메시지 보강 관리 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1472">Add support to manage message enrichment for an IotHub.</span></span> <span data-ttu-id="73f1f-1473">새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1473">New cmdlets are:</span></span>
    - <span data-ttu-id="73f1f-1474">Add-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="73f1f-1474">Add-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="73f1f-1475">Get-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="73f1f-1475">Get-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="73f1f-1476">Remove-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="73f1f-1476">Remove-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="73f1f-1477">Set-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="73f1f-1477">Set-AzIotHubMessageEnrichment</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="73f1f-1478">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="73f1f-1478">Az.Monitor</span></span>
* <span data-ttu-id="73f1f-1479">최신 모니터링 SDK, 즉, 0.24.1-preview를 가리킵니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1479">Pointing to the most recent Monitor SDK, i.e. 0.24.1-preview</span></span>
   - <span data-ttu-id="73f1f-1480">메트릭 cmdlet에 줄 바꿈하지 않는 변경 내용을 추가합니다. 즉, 단위 열거형은 여러 새 값을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1480">Adds non-braking changes to the Metrics cmdlets, i.e. the Unit enumeration supports several new values.</span></span> <span data-ttu-id="73f1f-1481">이러한 cmdlet은 읽기 전용이므로 cmdlet 입력이 변경되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1481">These are read-only cmdlets, so there would be no change in the input of the cmdlets.</span></span>
   - <span data-ttu-id="73f1f-1482">이제 **ActionGroups** 요청의 api 버전은 **2019-06-01**이고, 이전에는 **2018-03-01**였습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1482">The api-version of the **ActionGroups** requests is now **2019-06-01**, before it was **2018-03-01**.</span></span> <span data-ttu-id="73f1f-1483">시나리오 테스트가 이 변경 내용에 맞게 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1483">The scenario tests have been updated to accommodate for this change.</span></span>
   - <span data-ttu-id="73f1f-1484">**EmailReceiver** 및 **WebhookReceiver** 클래스에 대한 생성자가 새 필수 인수, 즉, **useCommonAlertSchema**라는 부울 값을 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1484">The constructors for the classes **EmailReceiver** and **WebhookReceiver** added one new mandatory argument, i.e. a Boolean value called **useCommonAlertSchema**.</span></span> <span data-ttu-id="73f1f-1485">현재 이 값은 cmdlet의 주요 변경 사항을 숨기도록 **false**로 고정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1485">Currently, the value is fixed to **false** to hide this breaking change from the cmdlets.</span></span> <span data-ttu-id="73f1f-1486">**참고**: 이 변경 사항은 경고 팀에서 유효성을 검사해야 하는 임시 변경 내용입니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1486">**NOTE**: this is a temporary change that must be validated by the Alerts team.</span></span>
   - <span data-ttu-id="73f1f-1487">이전 SDK에서 변경된 **Source** 클래스(**ScheduledQueryRuleSource** 클래스와 관련됨)의 생성자에 대한 인수 순서입니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1487">The order of the arguments for the constructor of the class **Source** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="73f1f-1488">이번 변화로 인해 두 개의 단위 테스트를 수정해야 했습니다. 즉, 두 단위 테스트가 컴파일되었지만 테스트를 통과하지 못했습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1488">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
   - <span data-ttu-id="73f1f-1489">이전 SDK에서 변경된 **AlertingAction** 클래스(**ScheduledQueryRuleSource** 클래스와 관련됨)의 생성자에 대한 인수 순서입니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1489">The order of the arguments for the constructor of the class **AlertingAction** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="73f1f-1490">이번 변화로 인해 두 개의 단위 테스트를 수정해야 했습니다. 즉, 두 단위 테스트가 컴파일되었지만 테스트를 통과하지 못했습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1490">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
* <span data-ttu-id="73f1f-1491">메트릭 경고 V2에 대한 동적 임계값 기준 지원</span><span class="sxs-lookup"><span data-stu-id="73f1f-1491">Support Dynamic Threshold criteria for metric alert V2</span></span>
    - <span data-ttu-id="73f1f-1492">AzMetricAlertRuleV2Criteria: 이제 동적 임계값 조건도 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1492">New-AzMetricAlertRuleV2Criteria: now creats dynamic threshold criteria also</span></span>
    - <span data-ttu-id="73f1f-1493">Add-AzMetricAlertRuleV2: 이제 동적 임계값 조건도 수락합니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1493">Add-AzMetricAlertRuleV2: now accept dynamic threshold criteria also</span></span>
* <span data-ttu-id="73f1f-1494">SQR(예약된 쿼리 규칙)의 향상된 기능</span><span class="sxs-lookup"><span data-stu-id="73f1f-1494">Improvements in Scheduled Query Rule cmdlets (SQR)</span></span>
 - <span data-ttu-id="73f1f-1495">Cmdlet이 'Location' 매개 변수를 두 가지 형식(eastus 같은 위치 또는 미국 동부 같은 위치 표시 이름)으로 모두 허용합니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1495">Cmdlets will accept 'Location' paramater in both formats, either the location (e.g. eastus) or the location display name (e.g. East US)</span></span>
 - <span data-ttu-id="73f1f-1496">도움말 파일에 적절하게 표시된 'Enabled' 매개 변수</span><span class="sxs-lookup"><span data-stu-id="73f1f-1496">Illustrated 'Enabled' parameter in help files properly</span></span>
 - <span data-ttu-id="73f1f-1497">선택적 매개 변수 'ActionGroup'에 대한 예제가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1497">Added examples for 'ActionGroup' optional parameter</span></span>
 - <span data-ttu-id="73f1f-1498">도움말 파일이 전체적으로 개선되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1498">Overall improved help files</span></span>
* <span data-ttu-id="73f1f-1499">'Set-AzActionRule'의 범위 유형 결정 버그를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1499">Fix bug in determining scope type for 'Set-AzActionRule'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="73f1f-1500">Az.Network</span><span class="sxs-lookup"><span data-stu-id="73f1f-1500">Az.Network</span></span>
* <span data-ttu-id="73f1f-1501">'New-AzApplicationGateway' 참조 설명서의 잘못된 예제가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1501">Fix incorrect example in 'New-AzApplicationGateway' reference documentation</span></span>
* <span data-ttu-id="73f1f-1502">'Get-AzNetworkWatcherPacketCapture' 참조 설명서에 패킷 캡처를 위한 모든 속성 검색과 관련된 메모가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1502">Add note in 'Get-AzNetworkWatcherPacketCapture' reference documentation about retrieving all properties for a packet capture</span></span>
* <span data-ttu-id="73f1f-1503">NIC를 올바르게 열거하도록 'Test-AzNetworkWatcherIPFlow' 참조 설명서의 예제가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1503">Fixed example in 'Test-AzNetworkWatcherIPFlow' reference documentation to correctly enumerate NICs</span></span>
* <span data-ttu-id="73f1f-1504">추가 세부 정보가 있는 경우 추가 세부 정보를 표시하도록 클라우드 예외 구문 분석이 향상되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1504">Improved cloud exception parsing to display additional details if they are present</span></span>
* <span data-ttu-id="73f1f-1505">더 많은 형식의 SDK 예외를 처리하도록 클라우드 예외 구문 분석이 향상되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1505">Improved cloud exception parsing to handle additional type of SDK exception</span></span>
* <span data-ttu-id="73f1f-1506">보안 규칙 모델의 잘못된 매핑이 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1506">Fixed incorrect mapping of Security Rule models</span></span>
* <span data-ttu-id="73f1f-1507">네트워크 인터페이스에 개인 IP 기능을 위한 속성이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1507">Added properties to network interface for private ip feature</span></span>
    - <span data-ttu-id="73f1f-1508">PSNetworkInterface에 'PrivateEndpoint' 속성이 PSResourceId 형식으로 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1508">Added property 'PrivateEndpoint' as type of PSResourceId to PSNetworkInterface</span></span>
    - <span data-ttu-id="73f1f-1509">PSNetworkInterfaceIPConfiguration에 'PrivateLinkConnectionProperties' 속성이 PSIpConfigurationConnectivityInformation 형식으로 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1509">Added property 'PrivateLinkConnectionProperties' as type of PSIpConfigurationConnectivityInformation to PSNetworkInterfaceIPConfiguration</span></span>
    - <span data-ttu-id="73f1f-1510">새 모델 클래스 PSIpConfigurationConnectivityInformation이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1510">Added new model class PSIpConfigurationConnectivityInformation</span></span>
* <span data-ttu-id="73f1f-1511">Azure Firewall 리소스에 대한 새 ApplicationRuleProtocolType 'mssql'이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1511">Added new ApplicationRuleProtocolType 'mssql' for Azure Firewall resource</span></span>
* <span data-ttu-id="73f1f-1512">Virtual WAN에서 멀티 링크를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1512">MultiLink support in Virtual WAN</span></span>
    - <span data-ttu-id="73f1f-1513">새로운 cmdlet</span><span class="sxs-lookup"><span data-stu-id="73f1f-1513">New cmdlets</span></span>
        - <span data-ttu-id="73f1f-1514">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="73f1f-1514">New-AzVpnSiteLink</span></span>
        - <span data-ttu-id="73f1f-1515">New-AzVpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="73f1f-1515">New-AzVpnSiteLinkConnection</span></span>
    - <span data-ttu-id="73f1f-1516">업데이트된 cmdlet:</span><span class="sxs-lookup"><span data-stu-id="73f1f-1516">Updated cmdlet:</span></span>
        - <span data-ttu-id="73f1f-1517">New-VpnSite</span><span class="sxs-lookup"><span data-stu-id="73f1f-1517">New-VpnSite</span></span>
        - <span data-ttu-id="73f1f-1518">Update-VpnSite</span><span class="sxs-lookup"><span data-stu-id="73f1f-1518">Update-VpnSite</span></span>
        - <span data-ttu-id="73f1f-1519">New-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="73f1f-1519">New-VpnConnection</span></span>
        - <span data-ttu-id="73f1f-1520">Update-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="73f1f-1520">Update-VpnConnection</span></span>
* <span data-ttu-id="73f1f-1521">AzureRM cmdlet 대신 Az cmdlet을 사용하도록 일부 PowerShell 예제의 문서가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1521">Fixed documents for some PowerShell examples to use Az cmdlets instead of AzureRM cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="73f1f-1522">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="73f1f-1522">Az.RecoveryServices</span></span>
* <span data-ttu-id="73f1f-1523">AzureVMpolicy 개체가 ProtectedItemsCount 특성으로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1523">Update AzureVMpolicy Object with ProtectedItemsCount Attribute</span></span>
* <span data-ttu-id="73f1f-1524">VM 정책 및 원래 스토리지 계정 복원에 대한 테스트가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1524">Added Tests for VM policy and Original Storage Account Restore</span></span>

#### <a name="azresources"></a><span data-ttu-id="73f1f-1525">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="73f1f-1525">Az.Resources</span></span>
* <span data-ttu-id="73f1f-1526">매개 변수 범위 없이 AzRoleAssignment를 호출할 수 없는 버그가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1526">Fix bug where New-AzRoleAssignment could not be called without parameter Scope.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="73f1f-1527">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="73f1f-1527">Az.ServiceFabric</span></span>
* <span data-ttu-id="73f1f-1528">'AzServiceFabricReliability' 참조 설명서에 대한 예제의 오타가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1528">Fixed typo in example for 'Update-AzServiceFabricReliability' reference documentation</span></span>
* <span data-ttu-id="73f1f-1529">애플리케이션 및 서비스를 관리하는 다음과 같은 새 cmdlet이 추가됩니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1529">Adding new cmdlets to manage appliaction and services:</span></span>
    - <span data-ttu-id="73f1f-1530">New-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="73f1f-1530">New-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="73f1f-1531">New-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="73f1f-1531">New-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="73f1f-1532">New-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="73f1f-1532">New-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="73f1f-1533">New-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="73f1f-1533">New-AzServiceFabricService</span></span>
    - <span data-ttu-id="73f1f-1534">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="73f1f-1534">Update-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="73f1f-1535">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="73f1f-1535">Get-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="73f1f-1536">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="73f1f-1536">Get-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="73f1f-1537">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="73f1f-1537">Get-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="73f1f-1538">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="73f1f-1538">Get-AzServiceFabricService</span></span>
    - <span data-ttu-id="73f1f-1539">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="73f1f-1539">Remove-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="73f1f-1540">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="73f1f-1540">Remove-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="73f1f-1541">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="73f1f-1541">Remove-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="73f1f-1542">Remove-AzServiceFabricServic</span><span class="sxs-lookup"><span data-stu-id="73f1f-1542">Remove-AzServiceFabricServic</span></span>
* <span data-ttu-id="73f1f-1543">Service Fabric SDK가 Service Fabric 리소스 공급자 api 버전 2019-03-01을 사용하는 1.2.0 버전으로 업그레이드되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1543">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2019-03-01.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="73f1f-1544">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="73f1f-1544">Az.SignalR</span></span>
* <span data-ttu-id="73f1f-1545">Update, Restart, CheckNameAvailability, GetUsage Cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1545">Add Update, Restart, CheckNameAvailability, GetUsage Cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="73f1f-1546">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="73f1f-1546">Az.Sql</span></span>
* <span data-ttu-id="73f1f-1547">'Get-AzSqlElasticPool'에 대한 참조 설명서의 예제가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1547">Update example in reference documentation for 'Get-AzSqlElasticPool'</span></span>
* <span data-ttu-id="73f1f-1548">탄력적 풀을 만드는 vCore 예제가 추가되었습니다(AzSqlElasticPool).</span><span class="sxs-lookup"><span data-stu-id="73f1f-1548">Added vCore example to creating an elastic pool (New-AzSqlElasticPool).</span></span>
* <span data-ttu-id="73f1f-1549">Set-AzSqlServerAdvancedThreatProtectionPolicy 및 Set-AzSqlDatabaseAdvancedThreatProtectionPolicy에서 EmailAddresses가 비어 있는 경우 EmailAddresses의 유효성을 검사하고 EmailAdmins가 false가 아닌지 확인하는 기능이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1549">Remove the validation of EmailAddresses and the check that EmailAdmins is not false in case EmailAddresses is empty in Set-AzSqlServerAdvancedThreatProtectionPolicy and Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="73f1f-1550">감사 범주를 사용하는 여러 진단 설정이 있는 경우 서버/데이터베이스 감사 설정을 제거하도록 설정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1550">Enabled removal of server/database auditing settings when multiple diagnostic settings that enable audit category exist.</span></span>
* <span data-ttu-id="73f1f-1551">여러 Sql 취약성 평가 cmdlet에서 이메일 주소 유효성 검사가 수정되었습니다(Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting 및 Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span><span class="sxs-lookup"><span data-stu-id="73f1f-1551">Fix email addresses validation in multiple Sql Vulnerability Assessment cmdlets (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting and Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span></span>

#### <a name="azstorage"></a><span data-ttu-id="73f1f-1552">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="73f1f-1552">Az.Storage</span></span>
* <span data-ttu-id="73f1f-1553">'Get-AzStorageAccountKey'에 대한 참조 설명서의 예제가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1553">Updated example in reference documentation for 'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="73f1f-1554">Azure 파일 업로드/다운에서, 원본 파일 SMB 속성(파일 특성, 파일 생성 시간, 파일을 마지막으로 쓴 시간)을 대상 파일에 보존하는 기능이 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1554">In upload/Downalod Azure File,support perserve the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the destination file</span></span>
    -  <span data-ttu-id="73f1f-1555">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="73f1f-1555">Set-AzStorageFileContent</span></span>
    -  <span data-ttu-id="73f1f-1556">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="73f1f-1556">Get-AzStorageFileContent</span></span>
* <span data-ttu-id="73f1f-1557">컨테이너가 사용되는 ImmutabilityPolicy에서 properties/metadate fail을 사용하여 블록 Blob 업로드가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1557">Fix Upload block blob with properties/metadate fail on container enabled ImmutabilityPolicy.</span></span>
    -  <span data-ttu-id="73f1f-1558">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="73f1f-1558">Set-AzStorageBlobContent</span></span>
* <span data-ttu-id="73f1f-1559">관리 평면 API를 사용하여 Azure 파일 공유 관리를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1559">Support manage Azure File shares with Management plane API</span></span>
    -  <span data-ttu-id="73f1f-1560">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="73f1f-1560">New-AzRmStorageShare</span></span>
    -  <span data-ttu-id="73f1f-1561">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="73f1f-1561">Get-AzRmStorageShare</span></span>
    -  <span data-ttu-id="73f1f-1562">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="73f1f-1562">Update-AzRmStorageShare</span></span>
    -  <span data-ttu-id="73f1f-1563">Remove-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="73f1f-1563">Remove-AzRmStorageShare</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="73f1f-1564">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="73f1f-1564">Az.Websites</span></span>
* <span data-ttu-id="73f1f-1565">앱을 새 ASP로 마이그레이션할 때 웹앱 태그가 삭제되는 이슈가 해결되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1565">Fixing issue where webapp Tags were getting deleted when migrating App to new ASPwhere webapp Tags were getting deleted when migrating App to new ASP</span></span>
* <span data-ttu-id="73f1f-1566">Linux와 Windows에서 모두 작동하도록 Publish-AzureWebapp이 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1566">Fixing the Publish-AzureWebapp to work across Linux and windows</span></span>
* <span data-ttu-id="73f1f-1567">'Get-AzWebAppPublishingProfile' 참조 설명서의 예제가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1567">Update example in 'Get-AzWebAppPublishingProfile' reference documentation</span></span>

## <a name="260---august-2019"></a><span data-ttu-id="73f1f-1568">2.6.0 - 2019년 8월</span><span class="sxs-lookup"><span data-stu-id="73f1f-1568">2.6.0 - August 2019</span></span>
#### <a name="general"></a><span data-ttu-id="73f1f-1569">일반</span><span class="sxs-lookup"><span data-stu-id="73f1f-1569">General</span></span>
* <span data-ttu-id="73f1f-1570">여러 모듈에서 기타 오타가 수정됨</span><span class="sxs-lookup"><span data-stu-id="73f1f-1570">Fixed miscellaneous typos across numerous modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="73f1f-1571">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="73f1f-1571">Az.Accounts</span></span>
* <span data-ttu-id="73f1f-1572">Azure Functions 인증에서 사용자가 할당한 MSI가 지원됨(# 9479)</span><span class="sxs-lookup"><span data-stu-id="73f1f-1572">Support user-assigned MSI in Azure Functiosn Authentication (#9479)</span></span>

#### <a name="azaks"></a><span data-ttu-id="73f1f-1573">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="73f1f-1573">Az.Aks</span></span>
* <span data-ttu-id="73f1f-1574">'Get-AzAks' 출력 관련 문제가 해결됨</span><span class="sxs-lookup"><span data-stu-id="73f1f-1574">Fix issue with output for 'Get-AzAks'</span></span>
    * <span data-ttu-id="73f1f-1575">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/9847 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1575">More information here: https://github.com/Azure/azure-powershell/issues/9847</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="73f1f-1576">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="73f1f-1576">Az.ApiManagement</span></span>
* <span data-ttu-id="73f1f-1577">문제 https://github.com/Azure/azure-powershell/issues/9351 수정</span><span class="sxs-lookup"><span data-stu-id="73f1f-1577">Fix for issue https://github.com/Azure/azure-powershell/issues/9351</span></span>
    - <span data-ttu-id="73f1f-1578">productId, apiId, groupId 및 userId에 대한 제한을 적용하지 않는 .Net NuGet 버전이 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="73f1f-1578">Update .net nuget version, which does not enforce restrictions on productId, apiId, groupId and userId</span></span>
* <span data-ttu-id="73f1f-1579">**Get-AzApiManagementProduct** - API를 사용하는 제품에 대한 쿼리 지원이 추가됨</span><span class="sxs-lookup"><span data-stu-id="73f1f-1579">**Get-AzApiManagementProduct** - Added support for querying products using Api.</span></span>
  https://github.com/Azure/azure-powershell/issues/9482
* <span data-ttu-id="73f1f-1580">**New-AzApiManagementApiRevision** - 새 API 수정(https://github.com/Azure/azure-powershell/issues/9752 )을 만들 때 ApiRevisionDescription이 설정되지 않은 문제가 해결됨</span><span class="sxs-lookup"><span data-stu-id="73f1f-1580">**New-AzApiManagementApiRevision** - Fix for issue where ApiRevisionDescription was not being set when creating new api revision https://github.com/Azure/azure-powershell/issues/9752</span></span>
* <span data-ttu-id="73f1f-1581">'PsApiManagementOAuth2AuthrozationServer' 모델의 오타가 'PsApiManagementOAuth2AuthorizationServer'로 수정됨</span><span class="sxs-lookup"><span data-stu-id="73f1f-1581">Fixed typo in model 'PsApiManagementOAuth2AuthrozationServer' to 'PsApiManagementOAuth2AuthorizationServer'</span></span>

#### <a name="azbatch"></a><span data-ttu-id="73f1f-1582">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="73f1f-1582">Az.Batch</span></span>
* <span data-ttu-id="73f1f-1583">도움말 메시지 및 설명서에서 Windows를 대문자로 시작하도록 오타가 수정됨</span><span class="sxs-lookup"><span data-stu-id="73f1f-1583">Fixed typo in help message and documentation to capitalize Windows</span></span>

#### <a name="azcdn"></a><span data-ttu-id="73f1f-1584">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="73f1f-1584">Az.Cdn</span></span>
* <span data-ttu-id="73f1f-1585">CDN 모듈 변환 도우미의 오타가 수정됨</span><span class="sxs-lookup"><span data-stu-id="73f1f-1585">Fixed a typo in CDN module conversion helper</span></span>

#### <a name="azcompute"></a><span data-ttu-id="73f1f-1586">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="73f1f-1586">Az.Compute</span></span>
* <span data-ttu-id="73f1f-1587">VmssId가 New-AzVMConfig cmdlet에 추가됨</span><span class="sxs-lookup"><span data-stu-id="73f1f-1587">Add VmssId to New-AzVMConfig cmdlet</span></span>
* <span data-ttu-id="73f1f-1588">TerminateScheduledEvents 및 TerminateScheduledEventNotBeforeTimeoutInMinutes 매개 변수가 New-AzVmssConfig 및 Update-AzVmss에 추가됨</span><span class="sxs-lookup"><span data-stu-id="73f1f-1588">Add TerminateScheduledEvents and TerminateScheduledEventNotBeforeTimeoutInMinutes parameters to New-AzVmssConfig and Update-AzVmss</span></span>
* <span data-ttu-id="73f1f-1589">HyperVGeneration 속성이 VM 이미지 개체에 추가됨</span><span class="sxs-lookup"><span data-stu-id="73f1f-1589">Add HyperVGeneration property to VM image object</span></span>
* <span data-ttu-id="73f1f-1590">Host 및 HostGroup 기능이 추가됨</span><span class="sxs-lookup"><span data-stu-id="73f1f-1590">Add Host and HostGroup features</span></span>
    - <span data-ttu-id="73f1f-1591">새 cmdlet:   New-AzHostGroup, New-AzHost, Get-AzHostGroup, Get-AzHost, Remove-AzHostGroup, Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="73f1f-1591">New cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span></span>
    - <span data-ttu-id="73f1f-1592">HostId 매개 변수가 New-AzVMConfig 및 New-AzVM 추가됨</span><span class="sxs-lookup"><span data-stu-id="73f1f-1592">HostId parameter is added to New-AzVMConfig and New-AzVM</span></span>
* <span data-ttu-id="73f1f-1593">'Invoke-AzVMRunCommand' 설명서의 예제에서 올바른 매개 변수 이름을 사용하도록 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="73f1f-1593">Update example in 'Invoke-AzVMRunCommand' documentation to use correct parameter name</span></span>
* <span data-ttu-id="73f1f-1594">'Set-AzVMDiskEncryptionExtension' 및 'Set-AzVmssDiskEncryptionExtension' 참조 설명서의 '-VolumeType' 설명이 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="73f1f-1594">Update '-VolumeType' description in 'Set-AzVMDiskEncryptionExtension' and 'Set-AzVmssDiskEncryptionExtension' reference documentation</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="73f1f-1595">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="73f1f-1595">Az.DataFactory</span></span>
* <span data-ttu-id="73f1f-1596">'New-AzDataFactoryEncryptValue' 설명서에서 'Windows'를 대문자로 시작하도록 오타가 수정됨</span><span class="sxs-lookup"><span data-stu-id="73f1f-1596">Fix typo to capitalize 'Windows' in 'New-AzDataFactoryEncryptValue' documentation</span></span>
* <span data-ttu-id="73f1f-1597">ADF .Net SDK 버전이 4.1.2로 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="73f1f-1597">Updated ADF .Net SDK version to 4.1.2</span></span>
* <span data-ttu-id="73f1f-1598">자체 호스팅 통합 런타임을 SSIS Integration Runtime의 프록시로 설정할 수 있도록 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' 및 'DataProxyStagingPath' 매개 변수가 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd에 추가됨</span><span class="sxs-lookup"><span data-stu-id="73f1f-1598">Add parameter 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' and 'DataProxyStagingPath' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable set up Self-Hosted Integration Runtime as a proxy for SSIS Integration Runtime</span></span>
* <span data-ttu-id="73f1f-1599">PSTriggerRun에서 트리거된 파이프라인, 메시지 및 속성을 표시하고, PSActivityRun에서 작업 유형을 표시하도록 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="73f1f-1599">Updated PSTriggerRun to show the triggered pipelines, message and properties, and PSActivityRun to show the activity type</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="73f1f-1600">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="73f1f-1600">Az.DataLakeStore</span></span>
* <span data-ttu-id="73f1f-1601">오류 또는 원격 예외에 대한 Get-DataLakeStoreDeletedItem 중단이 수정됨</span><span class="sxs-lookup"><span data-stu-id="73f1f-1601">Fix hanging of Get-DataLakeStoreDeletedItem for any errors or remote exceptions.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="73f1f-1602">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="73f1f-1602">Az.EventHub</span></span>
* <span data-ttu-id="73f1f-1603">#9658 문제 해결: Set-AzEventHubNetworkRuleSet의 VirtualNteworkRule 매개 변수에 대한 오타</span><span class="sxs-lookup"><span data-stu-id="73f1f-1603">Fix for issue #9658 : Typo VirtualNteworkRule parameter in Set-AzEventHubNetworkRuleSet</span></span>
* <span data-ttu-id="73f1f-1604">#9558 문제 해결: Set-AzEventHubNamespace에서 PUT 대신 PATCH가 사용됨</span><span class="sxs-lookup"><span data-stu-id="73f1f-1604">Fix for issue #9558 : Set-AzEventHubNamespace is using PATCH instead of PUT</span></span>
* <span data-ttu-id="73f1f-1605">EnableKafka 매개 변수가 Set-AzEventHubNamespace cmdlet에 추가됨</span><span class="sxs-lookup"><span data-stu-id="73f1f-1605">added EnableKafka parameter to Set-AzEventHubNamespace cmdlet</span></span>
* <span data-ttu-id="73f1f-1606">#9786 문제 해결: Listen(수신 대기) 전용 권한이 있는 규칙을 만들 수 없음</span><span class="sxs-lookup"><span data-stu-id="73f1f-1606">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>

#### <a name="azmarketplaceordering"></a><span data-ttu-id="73f1f-1607">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="73f1f-1607">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="73f1f-1608">'Azure'가 모두 소문자인 설명서의 오타가 수정됨</span><span class="sxs-lookup"><span data-stu-id="73f1f-1608">Fixed documentation typo where 'Azure' was all lowercase letters</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="73f1f-1609">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="73f1f-1609">Az.Monitor</span></span>
* <span data-ttu-id="73f1f-1610">도움말 설명서에서 잘못된 매개 변수 이름이 수정됨</span><span class="sxs-lookup"><span data-stu-id="73f1f-1610">Fixed incorrect parameter name in help documentation</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="73f1f-1611">Az.Network</span><span class="sxs-lookup"><span data-stu-id="73f1f-1611">Az.Network</span></span>
* <span data-ttu-id="73f1f-1612">New-AzPrivateLinkServiceIpConfig가 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="73f1f-1612">Updated New-AzPrivateLinkServiceIpConfig</span></span>
    - <span data-ttu-id="73f1f-1613">서버 쪽에서 사용되지 않으므로 'PublicIpAddress' 매개 변수가 사용되지 않음</span><span class="sxs-lookup"><span data-stu-id="73f1f-1613">Deprecated the paramster 'PublicIpAddress' since this is never used in the server side.</span></span>
    - <span data-ttu-id="73f1f-1614">현재 IP 구성이 기본 구성인지 여부를 나타내는 하나의 선택적 'Primary' 매개 변수가 추가됨</span><span class="sxs-lookup"><span data-stu-id="73f1f-1614">Added one optional parameter 'Primary' that indicate the current ip configuration is primary one or not.</span></span>
* <span data-ttu-id="73f1f-1615">SDK의 요청 오류 예외 처리가 향상됨 - 이전의 SDK 예외가 올바르게 처리되지 않아 주요 오류 세부 정보가 표시되지 않은 문제가 해결됨</span><span class="sxs-lookup"><span data-stu-id="73f1f-1615">Improved handling of request error exception from SDK   -Fixes the issue that previously SDK exceptions aren't handled correctly which results in key error details not being displayed</span></span>
* <span data-ttu-id="73f1f-1616">올바른 IPv6 접두사 길이를 확인하기 위해 Ipv6 IP 접두사에 대한 유효성 검사 논리가 조정됨</span><span class="sxs-lookup"><span data-stu-id="73f1f-1616">Adjusted validation logic for Ipv6 IP Prefix to check for correct IPv6 prefix length.</span></span>
* <span data-ttu-id="73f1f-1617">Get-AzVirtualNetworkSubnetConfig가 업데이트됨: 서브넷 리소스 ID별로 가져오도록 설정되는 매개 변수 세트가 추가됨</span><span class="sxs-lookup"><span data-stu-id="73f1f-1617">Updated Get-AzVirtualNetworkSubnetConfig: Added parameter set to get by subnet resource id.</span></span>
* <span data-ttu-id="73f1f-1618">AzNetworkServiceTag의 Location(위치) 매개 변수에 대한 설명이 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="73f1f-1618">Updated description of Location parameter for AzNetworkServiceTag</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="73f1f-1619">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="73f1f-1619">Az.OperationalInsights</span></span>
* <span data-ttu-id="73f1f-1620">'New-AzOperationalInsightsLinuxSyslogDataSource'에 대한 설명서가 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="73f1f-1620">Updated documentation for 'New-AzOperationalInsightsLinuxSyslogDataSource'</span></span>
    - <span data-ttu-id="73f1f-1621">예제가 추가됨</span><span class="sxs-lookup"><span data-stu-id="73f1f-1621">Added example</span></span>
    - <span data-ttu-id="73f1f-1622">'-Name' 매개 변수에 대한 설명이 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="73f1f-1622">Updated description for '-Name' parameter</span></span>
* <span data-ttu-id="73f1f-1623">New-AzOperationalInsightsWindowsEventDataSource에 대한 예제가 추가됨</span><span class="sxs-lookup"><span data-stu-id="73f1f-1623">Added an example for New-AzOperationalInsightsWindowsEventDataSource</span></span>
* <span data-ttu-id="73f1f-1624">New-AzOperationalInsightsWindowsEventDataSource의 -Name 매개 변수에 대한 설명이 변경됨</span><span class="sxs-lookup"><span data-stu-id="73f1f-1624">Changed the description of the -Name parameter for New-AzOperationalInsightsWindowsEventDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="73f1f-1625">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="73f1f-1625">Az.RecoveryServices</span></span>
* <span data-ttu-id="73f1f-1626">'Get-AzRecoveryServicesBackupJobDetail.md'가 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="73f1f-1626">Update 'Get-AzRecoveryServicesBackupJobDetail.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="73f1f-1627">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="73f1f-1627">Az.Resources</span></span>
* <span data-ttu-id="73f1f-1628">Microsoft 리소스에 대한 새 2019-05-10 API 버전 지원이 추가됨</span><span class="sxs-lookup"><span data-stu-id="73f1f-1628">Add support for new api version 2019-05-10 for Microsoft.Resource</span></span>
    - <span data-ttu-id="73f1f-1629">변수, 리소스 및 속성에 대한 'copy.count = 0' 지원이 추가됨</span><span class="sxs-lookup"><span data-stu-id="73f1f-1629">Add support for 'copy.count = 0' for variables, resources and properties</span></span>
    - <span data-ttu-id="73f1f-1630">'condition = false' 또는 'copy.count = 0'인 리소스가 완료 모드에서 삭제됨</span><span class="sxs-lookup"><span data-stu-id="73f1f-1630">Resources with 'condition = false' or 'copy.count = 0' will be deleted in complete mode</span></span>
* <span data-ttu-id="73f1f-1631">정책을 구독 수준에서 도움말 문서에 할당하는 예제가 추가됨</span><span class="sxs-lookup"><span data-stu-id="73f1f-1631">Add an example of assigning policy at subscription level to help doc</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="73f1f-1632">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="73f1f-1632">Az.ServiceBus</span></span>
* <span data-ttu-id="73f1f-1633">#9658 문제 해결: Set-AzServiceBusNetworkRuleSet의 VirtualNetworkRule 매개 변수에 대한 오타</span><span class="sxs-lookup"><span data-stu-id="73f1f-1633">Fix for issue #9658 : Typo VirtualNetworkRule parameter in Set-AzServiceBusNetworkRuleSet</span></span>
* <span data-ttu-id="73f1f-1634">#9786 문제 해결: Listen(수신 대기) 전용 권한이 있는 규칙을 만들 수 없음</span><span class="sxs-lookup"><span data-stu-id="73f1f-1634">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>
* <span data-ttu-id="73f1f-1635">큐 및 토픽에 대한 이름 가용성을 확인하는 새 'Test-AzServiceBusNameAvailability' 명령이 추가됨</span><span class="sxs-lookup"><span data-stu-id="73f1f-1635">Added new command 'Test-AzServiceBusNameAvailability' to check the name availability for queue and topic</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="73f1f-1636">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="73f1f-1636">Az.ServiceFabric</span></span>
* <span data-ttu-id="73f1f-1637">노드 유형 추가 cmdlet 버그 수정:</span><span class="sxs-lookup"><span data-stu-id="73f1f-1637">Fix add node type cmdlet bugs:</span></span>
    - <span data-ttu-id="73f1f-1638">서비스 패브릭 클러스터와 관련이 없는 다른 vmss가 리소스 그룹에 있을 때 발생하는 NullReferenceException 버그</span><span class="sxs-lookup"><span data-stu-id="73f1f-1638">NullReferenceException bug when resource group had other vmss not related to the service fabric cluster.</span></span> <span data-ttu-id="73f1f-1639">문제 해결: https://github.com/Azure/azure-powershell/issues/8681</span><span class="sxs-lookup"><span data-stu-id="73f1f-1639">Fixes issue: https://github.com/Azure/azure-powershell/issues/8681</span></span>
    - <span data-ttu-id="73f1f-1640">virtualNetwork가 클러스터의 다른 리소스 그룹에 있을 때 cmdlet이 실패하는 버그가 수정됨</span><span class="sxs-lookup"><span data-stu-id="73f1f-1640">Fix bug where cmdlet failed if virtualNetwork was in a different resource group that the cluster.</span></span> <span data-ttu-id="73f1f-1641">문제 해결: https://github.com/Azure/azure-powershell/issues/8407</span><span class="sxs-lookup"><span data-stu-id="73f1f-1641">fixes issue: https://github.com/Azure/azure-powershell/issues/8407</span></span>
    - <span data-ttu-id="73f1f-1642">Add-AzServiceFabricApplicationCertificate cmdlet이 사용되지 않음</span><span class="sxs-lookup"><span data-stu-id="73f1f-1642">Deprecating Add-AzServiceFabricApplicationCertificate cmdlet</span></span>

#### <a name="azsql"></a><span data-ttu-id="73f1f-1643">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="73f1f-1643">Az.Sql</span></span>
* <span data-ttu-id="73f1f-1644">이전의 Auditing(감사) cmdlet에 대한 설명서가 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="73f1f-1644">Update documentation of old Auditing cmdlets.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="73f1f-1645">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="73f1f-1645">Az.Storage</span></span>
* <span data-ttu-id="73f1f-1646">더 많은 시나리오를 cmdlet 예제에 추가하고 매개 변수 설명을 업데이트하여 Get/Close-AzStorageFileHandle에 대한 도움말이 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="73f1f-1646">Update help for Get/Close-AzStorageFileHandle, by add more scenarios to cmdlet examples and update parameter descriptions</span></span>
* <span data-ttu-id="73f1f-1647">Blob 업로드 및 Blob 복사에서 StandardBlobTier가 지원됨</span><span class="sxs-lookup"><span data-stu-id="73f1f-1647">Support StandardBlobTier in upload blob and copy blob</span></span>
    -  <span data-ttu-id="73f1f-1648">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="73f1f-1648">Set-AzStorageBlobContent</span></span>
    -  <span data-ttu-id="73f1f-1649">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="73f1f-1649">Start-AzStorageBlobCopy</span></span>
* <span data-ttu-id="73f1f-1650">Blob 복사에서 우선 순위 리하이드레이션이 지원됨</span><span class="sxs-lookup"><span data-stu-id="73f1f-1650">Support Rehydrate Priority in copy blob</span></span>
    -  <span data-ttu-id="73f1f-1651">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="73f1f-1651">Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="73f1f-1652">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="73f1f-1652">Az.Websites</span></span>
* <span data-ttu-id="73f1f-1653">Set-AzWebApp 및 Set-AzWebAppSlot에서 -AppSettings 매개 변수에 대한 설명이 추가됨</span><span class="sxs-lookup"><span data-stu-id="73f1f-1653">Add clarification around -AppSettings parameter in Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <a name="250---july-2019"></a><span data-ttu-id="73f1f-1654">2.5.0 - 2019년 7월</span><span class="sxs-lookup"><span data-stu-id="73f1f-1654">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="73f1f-1655">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="73f1f-1655">Az.Accounts</span></span>
* <span data-ttu-id="73f1f-1656">ClientRuntime의 최신 버전을 사용하도록 일반적인 코드를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1656">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="73f1f-1657">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="73f1f-1657">Az.ApplicationInsights</span></span>
* <span data-ttu-id="73f1f-1658">'Remove-AzApplicationInsightsApiKey' 설명서의 예제 오타 수정</span><span class="sxs-lookup"><span data-stu-id="73f1f-1658">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span>

#### <a name="azautomation"></a><span data-ttu-id="73f1f-1659">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="73f1f-1659">Az.Automation</span></span>
* <span data-ttu-id="73f1f-1660">리소스 문자열의 오타 수정</span><span class="sxs-lookup"><span data-stu-id="73f1f-1660">Fix typo in resource string</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="73f1f-1661">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="73f1f-1661">Az.CognitiveServices</span></span>
* <span data-ttu-id="73f1f-1662">NetworkRuleSet 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1662">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="73f1f-1663">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="73f1f-1663">Az.Compute</span></span>
* <span data-ttu-id="73f1f-1664">VM 인스턴스 보기 개체의 누락된 속성(ComputerName, OsName, OsVersion 및 HyperVGeneration)을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1664">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="73f1f-1665">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="73f1f-1665">Az.ContainerRegistry</span></span>
* <span data-ttu-id="73f1f-1666">복제 매개 변수의 Remove-AzContainerRegistryReplication에서 오타 수정</span><span class="sxs-lookup"><span data-stu-id="73f1f-1666">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="73f1f-1667">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/9633 을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1667">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="73f1f-1668">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="73f1f-1668">Az.DataFactory</span></span>
* <span data-ttu-id="73f1f-1669">ADF .Net SDK 버전을 4.1.0으로 업데이트</span><span class="sxs-lookup"><span data-stu-id="73f1f-1669">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="73f1f-1670">'Get-AzDataFactoryV2PipelineRun' 설명서의 오타 수정</span><span class="sxs-lookup"><span data-stu-id="73f1f-1670">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="73f1f-1671">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="73f1f-1671">Az.EventHub</span></span>
* <span data-ttu-id="73f1f-1672">SAS 토큰을 생성하기 위해 추가된 새로운 cmmdlet 추가: New-AzEventHubAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="73f1f-1672">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="73f1f-1673">'관리'만 지정된 경우 authorizationrules 권한에 대한 확인 및 오류 메시지 추가</span><span class="sxs-lookup"><span data-stu-id="73f1f-1673">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="73f1f-1674">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="73f1f-1674">Az.KeyVault</span></span>
* <span data-ttu-id="73f1f-1675">인증서 정책에 대한 KeySize 지정을 위한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="73f1f-1675">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="73f1f-1676">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="73f1f-1676">Az.LogicApp</span></span>
* <span data-ttu-id="73f1f-1677">모든 맵 유형을 나열하도록 Get-AzIntegrationAccountMap 수정</span><span class="sxs-lookup"><span data-stu-id="73f1f-1677">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="73f1f-1678">필터링을 위해 새 MapType 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="73f1f-1678">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="73f1f-1679">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="73f1f-1679">Az.ManagedServices</span></span>
* <span data-ttu-id="73f1f-1680">API 버전 2019-06-01(GA)에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="73f1f-1680">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="73f1f-1681">Az.Network</span><span class="sxs-lookup"><span data-stu-id="73f1f-1681">Az.Network</span></span>
* <span data-ttu-id="73f1f-1682">프라이빗 엔드포인트 및 프라이빗 링크 서비스에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="73f1f-1682">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="73f1f-1683">새로운 cmdlet</span><span class="sxs-lookup"><span data-stu-id="73f1f-1683">New cmdlets</span></span>
        - <span data-ttu-id="73f1f-1684">Set-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="73f1f-1684">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="73f1f-1685">Set-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="73f1f-1685">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="73f1f-1686">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="73f1f-1686">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="73f1f-1687">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="73f1f-1687">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="73f1f-1688">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="73f1f-1688">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="73f1f-1689">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="73f1f-1689">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="73f1f-1690">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="73f1f-1690">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="73f1f-1691">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="73f1f-1691">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="73f1f-1692">기능에 대한 새로운 명령이 업데이트됨: Virtualnetwork의 서브넷에 있는 PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies 플래그</span><span class="sxs-lookup"><span data-stu-id="73f1f-1692">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="73f1f-1693">업데이트된 New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="73f1f-1693">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="73f1f-1694">이 서브넷의 프라이빗 엔드포인트에 네트워크 정책을 적용할지 여부를 나타내는 선택적 매개 변수 -PrivateEndpointNetworkPoliciesFlag가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1694">Added optional parameter -PrivateEndpointNetworkPoliciesFlag that configures whether to apply network policies on private endpoint in this subnet.</span></span>
        - <span data-ttu-id="73f1f-1695">이 서브넷의 프라이빗 연결 서비스에 네트워크 정책을 적용할지 여부를 나타내는 선택적 매개 변수 -PrivateLinkServiceNetworkPoliciesFlag가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1695">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag that configures whether to apply network policies network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="73f1f-1696">AzPrivateLinkService의 cmdlet 매개 변수 'ServiceName'이 이전 버전과의 호환성을 위해 별칭 'ServiceName'을 사용한 'Name'으로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1696">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="73f1f-1697">네트워크 보안 규칙 구성에 ICMP 프로토콜 사용</span><span class="sxs-lookup"><span data-stu-id="73f1f-1697">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="73f1f-1698">다음 Cmdlet이 업데이트 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1698">Updated cmdlets</span></span>
        - <span data-ttu-id="73f1f-1699">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="73f1f-1699">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="73f1f-1700">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="73f1f-1700">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="73f1f-1701">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="73f1f-1701">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="73f1f-1702">New-AzVirtualNetworkGatewayConnection에 대한 구성 가능한 매개 변수로 ConnectionProtocolType (Ikev1/Ikev2) 추가</span><span class="sxs-lookup"><span data-stu-id="73f1f-1702">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="73f1f-1703">LoadBalancerFrontendIpConfiguration에 PrivateIpAddressVersion 추가</span><span class="sxs-lookup"><span data-stu-id="73f1f-1703">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="73f1f-1704">업데이트된 cmdlet:</span><span class="sxs-lookup"><span data-stu-id="73f1f-1704">Updated cmdlet:</span></span>
        - <span data-ttu-id="73f1f-1705">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="73f1f-1705">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="73f1f-1706">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="73f1f-1706">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="73f1f-1707">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="73f1f-1707">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="73f1f-1708">프로브에서 사용자 지정 포트를 지원하기 위한 Application Gateway New-AzApplicationGatewayProbeConfig 명령 업데이트</span><span class="sxs-lookup"><span data-stu-id="73f1f-1708">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="73f1f-1709">업데이트된 New-AzApplicationGatewayProbeConfig: 백 엔드 서버 검색에 사용되는 선택적 매개 변수 포트가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1709">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="73f1f-1710">이 매개 변수는 Standard_V2 및 WAF_V2 SKU에 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1710">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="73f1f-1711">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="73f1f-1711">Az.OperationalInsights</span></span>
* <span data-ttu-id="73f1f-1712">저장된 검색의 기본 버전이 1로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1712">Updated default version for saved searches to be 1.</span></span>
* <span data-ttu-id="73f1f-1713">사용자 지정 로그 null regex 처리가 수정됨</span><span class="sxs-lookup"><span data-stu-id="73f1f-1713">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="73f1f-1714">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="73f1f-1714">Az.RecoveryServices</span></span>
* <span data-ttu-id="73f1f-1715">'Get-AzRecoveryServicesBackupJob.md' 업데이트</span><span class="sxs-lookup"><span data-stu-id="73f1f-1715">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="73f1f-1716">'Get-AzRecoveryServicesBackupContainer.md' 업데이트</span><span class="sxs-lookup"><span data-stu-id="73f1f-1716">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="73f1f-1717">'Get-AzRecoveryServicesVault.md' 업데이트</span><span class="sxs-lookup"><span data-stu-id="73f1f-1717">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="73f1f-1718">'Wait-AzRecoveryServicesBackupJob.md' 업데이트</span><span class="sxs-lookup"><span data-stu-id="73f1f-1718">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="73f1f-1719">'Set-AzRecoveryServicesVaultContext.md' 업데이트</span><span class="sxs-lookup"><span data-stu-id="73f1f-1719">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="73f1f-1720">'Get-AzRecoveryServicesBackupItem.md' 업데이트</span><span class="sxs-lookup"><span data-stu-id="73f1f-1720">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="73f1f-1721">'Get-AzRecoveryServicesBackupRecoveryPoint.md' 업데이트</span><span class="sxs-lookup"><span data-stu-id="73f1f-1721">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="73f1f-1722">'Restore-AzRecoveryServicesBackupItem.md' 업데이트</span><span class="sxs-lookup"><span data-stu-id="73f1f-1722">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="73f1f-1723">Azure 파일 공유용 컨테이너를 등록 취소하기 위해 서비스 요청 업데이트</span><span class="sxs-lookup"><span data-stu-id="73f1f-1723">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="73f1f-1724">'Set-AzRecoveryServicesAsrAlertSetting.md' 업데이트</span><span class="sxs-lookup"><span data-stu-id="73f1f-1724">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="73f1f-1725">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="73f1f-1725">Az.Resources</span></span>
- <span data-ttu-id="73f1f-1726">'New-AzResourceGroupDeployment' 설명서에서 참조된 누락 cmdlet 제거</span><span class="sxs-lookup"><span data-stu-id="73f1f-1726">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="73f1f-1727">새 API 버전 2019-01-01을 사용하도록 정책 cmdlet 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="73f1f-1727">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="73f1f-1728">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="73f1f-1728">Az.ServiceBus</span></span>
* <span data-ttu-id="73f1f-1729">SAS 토큰을 생성하기 위해 추가된 새로운 cmmdlet 추가: New-AzServiceBusAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="73f1f-1729">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="73f1f-1730">'관리'만 지정된 경우 authorizationrules 권한에 대한 확인 및 오류 메시지 추가</span><span class="sxs-lookup"><span data-stu-id="73f1f-1730">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="73f1f-1731">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="73f1f-1731">Az.Sql</span></span>
* <span data-ttu-id="73f1f-1732">Set-AzSqlDatabaseSecondary cmdlet에 대한 누락된 예제 수정</span><span class="sxs-lookup"><span data-stu-id="73f1f-1732">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="73f1f-1733">이메일 주소를 제공하지 않고 설정된 취약성 평가 반복 검색 수정</span><span class="sxs-lookup"><span data-stu-id="73f1f-1733">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="73f1f-1734">경고 메시지의 작은 오타를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1734">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="73f1f-1735">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="73f1f-1735">Az.Storage</span></span>
* <span data-ttu-id="73f1f-1736">'Get-AzStorageAccount'에 대한 참조 설명서의 예제를 업데이트하여 올바른 매개 변수 이름 사용</span><span class="sxs-lookup"><span data-stu-id="73f1f-1736">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="73f1f-1737">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="73f1f-1737">Az.StorageSync</span></span>
* <span data-ttu-id="73f1f-1738">Invoke-AzStorageSyncChangeDetection cmdlet을 추가하는 중입니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1738">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="73f1f-1739">TierFilesOlderThanDays를 기념하는 문제 9551 수정</span><span class="sxs-lookup"><span data-stu-id="73f1f-1739">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="73f1f-1740">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="73f1f-1740">Az.Websites</span></span>
* <span data-ttu-id="73f1f-1741">Get-AzWebApp 및 Set-AzWebApp에서 일부 SiteConfig 속성을 반환하지 않은 버그 수정</span><span class="sxs-lookup"><span data-stu-id="73f1f-1741">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="73f1f-1742">Get-AzDeletedWebApp 및 Restore-AzDeletedWebApp에 새 위치 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="73f1f-1742">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="73f1f-1743">AzWebApp-IncludeSourceWebAppSlots을 사용하여 웹앱 슬롯을 복제하는 버그를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1743">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="73f1f-1744">2.4.0 - 2019년 7월</span><span class="sxs-lookup"><span data-stu-id="73f1f-1744">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="73f1f-1745">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="73f1f-1745">Az.Accounts</span></span>
* <span data-ttu-id="73f1f-1746">프로필 cmdlet에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="73f1f-1746">Add support for profile cmdlets</span></span>
* <span data-ttu-id="73f1f-1747">생성된 cmdlet에서 환경 및 데이터 평면에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="73f1f-1747">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="73f1f-1748">Windows PowerShell의 데이터 평면 cmdlet에대해 일부 경우 잘못된 엔드포인트가 사용되는 버그 수정</span><span class="sxs-lookup"><span data-stu-id="73f1f-1748">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="73f1f-1749">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="73f1f-1749">Az.Advisor</span></span>
* <span data-ttu-id="73f1f-1750">Az.Advisor의 GA 릴리스</span><span class="sxs-lookup"><span data-stu-id="73f1f-1750">GA release of Az.Advisor</span></span>
* <span data-ttu-id="73f1f-1751">이 모듈은 이제 롤업 `Az` 모듈의 일부로 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1751">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="73f1f-1752">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="73f1f-1752">Az.ApiManagement</span></span>
* <span data-ttu-id="73f1f-1753">문제 https://github.com/Azure/azure-powershell/issues/8671 수정</span><span class="sxs-lookup"><span data-stu-id="73f1f-1753">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="73f1f-1754">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="73f1f-1754">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="73f1f-1755">사용자 및 제품별 구독을 쿼리하기 위한 지원이 추가됨</span><span class="sxs-lookup"><span data-stu-id="73f1f-1755">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="73f1f-1756">범위 '/', '/ api, '/ api/echo api'를 사용하여 쿼리하기 위한 지원이 추가됨</span><span class="sxs-lookup"><span data-stu-id="73f1f-1756">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="73f1f-1757">[https://github.com/Azure/azure-powershell/issues/9307](https://github.com/Azure/azure-powershell/issues/9307 ) 및 https://github.com/Azure/azure-powershell/issues/8432 문제 수정</span><span class="sxs-lookup"><span data-stu-id="73f1f-1757">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="73f1f-1758">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="73f1f-1758">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="73f1f-1759">Apis를 가져올 때 'ApiVersion' 및 'ApiVersionSetId'를 지정하기 위한 지원이 추가됨</span><span class="sxs-lookup"><span data-stu-id="73f1f-1759">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="73f1f-1760">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="73f1f-1760">Az.Automation</span></span>
* <span data-ttu-id="73f1f-1761">문자열 값을 처리하기 위해 Set-AzAutomationConnectionFieldValue cmdlet 버그를 수정했습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1761">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="73f1f-1762">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="73f1f-1762">Az.Compute</span></span>
* <span data-ttu-id="73f1f-1763">New-AzImageConfig에 HyperVGeneration 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="73f1f-1763">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="73f1f-1764">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="73f1f-1764">Az.DataFactory</span></span>
* <span data-ttu-id="73f1f-1765">get activity runs, get pipeline runs, get trigger runs ADF cmdlet의 출력을 업데이트하여 Select-Object pipe를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1765">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="73f1f-1766">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="73f1f-1766">Az.EventGrid</span></span>
* <span data-ttu-id="73f1f-1767">'New-AzEventGridSubcription' 설명서의 오타 수정</span><span class="sxs-lookup"><span data-stu-id="73f1f-1767">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="73f1f-1768">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="73f1f-1768">Az.IotHub</span></span>
* <span data-ttu-id="73f1f-1769">권한 부여 정책 키를 다시 생성하기 위한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="73f1f-1769">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="73f1f-1770">Az.Network</span><span class="sxs-lookup"><span data-stu-id="73f1f-1770">Az.Network</span></span>
* <span data-ttu-id="73f1f-1771">'RoutingPreference'를 공용 IP 태그에 추가함</span><span class="sxs-lookup"><span data-stu-id="73f1f-1771">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="73f1f-1772">'Get-AzNetworkServiceTag' 참조 설명서의 예제 개선</span><span class="sxs-lookup"><span data-stu-id="73f1f-1772">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="73f1f-1773">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="73f1f-1773">Az.PolicyInsights</span></span>
* <span data-ttu-id="73f1f-1774">Get-AzPolicyState의 null 참조 문제 해결</span><span class="sxs-lookup"><span data-stu-id="73f1f-1774">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="73f1f-1775">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/9446 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1775">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="73f1f-1776">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="73f1f-1776">Az.OperationalInsights</span></span>
* <span data-ttu-id="73f1f-1777">Get-AzOperationalInsightsDataSource에 반환된 CustomLog datasource 모델 수정됨</span><span class="sxs-lookup"><span data-stu-id="73f1f-1777">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="73f1f-1778">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="73f1f-1778">Az.RecoveryServices</span></span>
* <span data-ttu-id="73f1f-1779">IaaSVMs에 대한 get-policy 명령 수정</span><span class="sxs-lookup"><span data-stu-id="73f1f-1779">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="73f1f-1780">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="73f1f-1780">Az.Resources</span></span>
    - <span data-ttu-id="73f1f-1781">Get-AzPolicyState -Top 매개 변수에 대한 도움말 텍스트 수정</span><span class="sxs-lookup"><span data-stu-id="73f1f-1781">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="73f1f-1782">Get-AzPolicyAlias에 대한 클라이언트 쪽 페이징 지원 추가</span><span class="sxs-lookup"><span data-stu-id="73f1f-1782">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="73f1f-1783">Set-AzPolicyAssignment, -PolicyParameters 및 -PolicyParametersObject에 대한 새 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="73f1f-1783">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="73f1f-1784">Policy cmdlet에 대한 몇 가지 문서 및 예제 업데이트</span><span class="sxs-lookup"><span data-stu-id="73f1f-1784">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="73f1f-1785">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="73f1f-1785">Az.ServiceBus</span></span>
* <span data-ttu-id="73f1f-1786">문제 #4938 수정 - MaxSizeInMegabytes를 설정할 때 New-AzureRmServiceBusQueue가 BadRequest 반환</span><span class="sxs-lookup"><span data-stu-id="73f1f-1786">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="73f1f-1787">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="73f1f-1787">Az.Sql</span></span>
* <span data-ttu-id="73f1f-1788">미리 보기 릴리스에서 공개 릴리스로 인스턴스 장애 조치(Failover) 그룹 cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="73f1f-1788">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="73f1f-1789">새 cmdlet으로 Azure SQL Server\Database Auditing을 지원하세요.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1789">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="73f1f-1790">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="73f1f-1790">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="73f1f-1791">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="73f1f-1791">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="73f1f-1792">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="73f1f-1792">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="73f1f-1793">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="73f1f-1793">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="73f1f-1794">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="73f1f-1794">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="73f1f-1795">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="73f1f-1795">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="73f1f-1796">취약성 평가 설정에서 이메일 제약 조건 제거</span><span class="sxs-lookup"><span data-stu-id="73f1f-1796">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="73f1f-1797">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="73f1f-1797">Az.Storage</span></span>
* <span data-ttu-id="73f1f-1798">다음 cmdlet에서 2개의 매개 변수 '-IndexDocument' 및 '-ErrorDocument404Path'를 필수에서 선택으로 변경하세요.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1798">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="73f1f-1799">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="73f1f-1799">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="73f1f-1800">예제를 추가하여 Get-AzStorageBlobContent의 도움말 업데이트</span><span class="sxs-lookup"><span data-stu-id="73f1f-1800">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="73f1f-1801">StorageException으로 cmdlet이 실패한 경우 자세한 오류 정보 표시</span><span class="sxs-lookup"><span data-stu-id="73f1f-1801">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="73f1f-1802">Azure Files AAD DS 인증으로 스토리지 계정 생성 또는 업데이트 지원</span><span class="sxs-lookup"><span data-stu-id="73f1f-1802">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="73f1f-1803">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="73f1f-1803">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="73f1f-1804">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="73f1f-1804">Set-AzStorageAccount</span></span>
* <span data-ttu-id="73f1f-1805">파일 공유, 파일 디렉터리 또는 파일의 목록 지원 또는 파일 핸들 닫기</span><span class="sxs-lookup"><span data-stu-id="73f1f-1805">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="73f1f-1806">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="73f1f-1806">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="73f1f-1807">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="73f1f-1807">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="73f1f-1808">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="73f1f-1808">Az.StorageSync</span></span>
* <span data-ttu-id="73f1f-1809">이 모듈은 이제 롤업 `Az` 모듈의 일부로 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1809">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="73f1f-1810">2.3.2 - 2019년 6월</span><span class="sxs-lookup"><span data-stu-id="73f1f-1810">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="73f1f-1811">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="73f1f-1811">Az.Accounts</span></span>
* <span data-ttu-id="73f1f-1812">함수 호출에 대해 일부 경우 잘못된 URL이 사용되는 버그 수정</span><span class="sxs-lookup"><span data-stu-id="73f1f-1812">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="73f1f-1813">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/8983 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1813">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="73f1f-1814">AzureRM에서 Az cmdlet으로의 별칭 문제 해결</span><span class="sxs-lookup"><span data-stu-id="73f1f-1814">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="73f1f-1815">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="73f1f-1815">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="73f1f-1816">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="73f1f-1816">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="73f1f-1817">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="73f1f-1817">Az.Compute</span></span>
* <span data-ttu-id="73f1f-1818">New-AzVm 및 New-AzVmss 단순 매개 변수 집합은 이제 'ProximityPlacementGroup'매개 변수를 허용합니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1818">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="73f1f-1819">'New-AzVM' 참조 설명서에서 오타 수정</span><span class="sxs-lookup"><span data-stu-id="73f1f-1819">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="73f1f-1820">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="73f1f-1820">Az.Dns</span></span>
* <span data-ttu-id="73f1f-1821">'Set-AzDnsZone' 도움말 예제의 오타가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1821">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="73f1f-1822">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="73f1f-1822">Az.EventGrid</span></span>
* <span data-ttu-id="73f1f-1823">2019-06-01 API 버전을 사용하도록 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1823">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="73f1f-1824">새 cmdlet:</span><span class="sxs-lookup"><span data-stu-id="73f1f-1824">New cmdlets:</span></span>
    - <span data-ttu-id="73f1f-1825">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="73f1f-1825">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="73f1f-1826">새 Azure Event Grid 도메인을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1826">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="73f1f-1827">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="73f1f-1827">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="73f1f-1828">Event Grid 도메인의 세부 정보를 가져오거나 현재 Azure 구독의 모든 Event Grid 도메인 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1828">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="73f1f-1829">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="73f1f-1829">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="73f1f-1830">Azure Event Grid 도메인을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1830">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="73f1f-1831">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="73f1f-1831">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="73f1f-1832">Azure Event Grid 도메인에 대한 공유 액세스 키를 다시 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1832">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="73f1f-1833">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="73f1f-1833">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="73f1f-1834">Event Grid 도메인 이벤트를 게시하는 데 사용되는 공유 액세스 키를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1834">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="73f1f-1835">New-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="73f1f-1835">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="73f1f-1836">새 Azure Event Grid 도메인 토픽을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1836">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="73f1f-1837">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="73f1f-1837">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="73f1f-1838">Event Grid 도메인 토픽의 세부 사항을 가져오거나, 현재 Azure의 특정 Event Grid 도메인 아래의 모든 Event Grid 도메인 토픽 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1838">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span>
    - <span data-ttu-id="73f1f-1839">Remove-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="73f1f-1839">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="73f1f-1840">기존 Azure Event Grid 도메인 토픽을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1840">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="73f1f-1841">다음 Cmdlet이 업데이트 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1841">Updated cmdlets:</span></span>
    - <span data-ttu-id="73f1f-1842">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="73f1f-1842">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="73f1f-1843">새로운 Event Grid 도메인 및 Event Grid 도메인 토픽에 대한 파이핑을 지원하기 위해 새로운 필수 매개 변수를 추가하여 이러한 리소스 아래에 새 이벤트 구독을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1843">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="73f1f-1844">새로운 Event Grid 도메인 이름 및 Event Grid 도메인 토픽 이름을 지정하기 위해 새로운 필수 매개 변수를 추가하여 이러한 리소스 아래에 새 이벤트 구독을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1844">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="73f1f-1845">기존 매개 변수(예: EndPointType, SubjectBeginsWith 등)를 재사용할 수 있도록 도메인 및 도메인 토픽에 대한 새로운 매개 변수 집합을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1845">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="73f1f-1846">지정을 위한 새로운 선택적 매개 변수를 추가</span><span class="sxs-lookup"><span data-stu-id="73f1f-1846">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="73f1f-1847">이벤트 구독 만료 날짜,</span><span class="sxs-lookup"><span data-stu-id="73f1f-1847">Event subscription expiration date,</span></span>
            - <span data-ttu-id="73f1f-1848">고급 필터링 매개 변수.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1848">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="73f1f-1849">대상으로 servicebusqueue에 대한 새 열거형을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1849">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="73f1f-1850">-IncludedEventType 옵션에서 'All' 사용을 허용하지 않고 다음으로 대체함</span><span class="sxs-lookup"><span data-stu-id="73f1f-1850">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span>
    - <span data-ttu-id="73f1f-1851">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="73f1f-1851">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="73f1f-1852">결과 페이지 매김 및 필터링을 지원하는 새로운 선택적 매개 변수(Top, ODataQuery 및 NextLink)를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1852">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="73f1f-1853">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="73f1f-1853">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="73f1f-1854">Event Grid 도메인 및 Event Grid 도메인 토픽에 대한 파이핑을 지원하기 위해 새로운 필수 매개 변수를 추가하여 이러한 리소스 아래에 기존 이벤트 구독을 제거할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1854">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="73f1f-1855">Event Grid 도메인 이름 및 Event Grid 도메인 토픽 이름을 지정하기 위해 새로운 필수 매개 변수를 추가하여 이러한 리소스 아래에 기존 이벤트 구독을 제거할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1855">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="73f1f-1856">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="73f1f-1856">Az.FrontDoor</span></span>
* <span data-ttu-id="73f1f-1857">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="73f1f-1857">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="73f1f-1858">변환 지원 및 새 연산자 자동 완성 값(RegEx)을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1858">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="73f1f-1859">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="73f1f-1859">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="73f1f-1860">새 자동 완성 값 추가</span><span class="sxs-lookup"><span data-stu-id="73f1f-1860">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="73f1f-1861">Az.Network</span><span class="sxs-lookup"><span data-stu-id="73f1f-1861">Az.Network</span></span>
* <span data-ttu-id="73f1f-1862">Microsoft Azure Virtual Network 게이트웨이 리소스에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="73f1f-1862">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="73f1f-1863">새로운 cmdlet</span><span class="sxs-lookup"><span data-stu-id="73f1f-1863">New cmdlets</span></span>
        - <span data-ttu-id="73f1f-1864">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="73f1f-1864">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="73f1f-1865">AvailablePrivateEndpointType 추가</span><span class="sxs-lookup"><span data-stu-id="73f1f-1865">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="73f1f-1866">새로운 cmdlet</span><span class="sxs-lookup"><span data-stu-id="73f1f-1866">New cmdlets</span></span>
        - <span data-ttu-id="73f1f-1867">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="73f1f-1867">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="73f1f-1868">PrivatePrivateLinkService 추가</span><span class="sxs-lookup"><span data-stu-id="73f1f-1868">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="73f1f-1869">새로운 cmdlet</span><span class="sxs-lookup"><span data-stu-id="73f1f-1869">New cmdlets</span></span>
        - <span data-ttu-id="73f1f-1870">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="73f1f-1870">Get-AzPrivateLinkService</span></span>
        - <span data-ttu-id="73f1f-1871">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="73f1f-1871">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="73f1f-1872">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="73f1f-1872">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="73f1f-1873">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="73f1f-1873">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="73f1f-1874">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="73f1f-1874">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="73f1f-1875">PrivateEndpoint 추가</span><span class="sxs-lookup"><span data-stu-id="73f1f-1875">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="73f1f-1876">새로운 cmdlet</span><span class="sxs-lookup"><span data-stu-id="73f1f-1876">New cmdlets</span></span>
        - <span data-ttu-id="73f1f-1877">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="73f1f-1877">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="73f1f-1878">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="73f1f-1878">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="73f1f-1879">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="73f1f-1879">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="73f1f-1880">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="73f1f-1880">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="73f1f-1881">기능에 대한 새로운 명령이 업데이트됨: VpnConnection 상의 UseLocalAzureIpAddress 플래그</span><span class="sxs-lookup"><span data-stu-id="73f1f-1881">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="73f1f-1882">New-AzVpnConnection이 업데이트됨: 선택적 매개 변수 -UseLocalAzureIpAddress를 추가하여 로컬 Azure IP 주소가 연결을 시작하는 동안 소스 주소로 사용되어야 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1882">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="73f1f-1883">Set-AzVpnConnection이 업데이트됨: 선택적 매개 변수 -UseLocalAzureIpAddress를 추가하여 로컬 Azure IP 주소가 연결을 시작하는 동안 소스 주소로 사용되어야 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1883">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="73f1f-1884">ExpressRoute 피어링에 읽기 전용 필드 PeeredConnections가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1884">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="73f1f-1885">ExpressRoute에 읽기 전용 필드 GlobalReachEnabled가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1885">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="73f1f-1886">ExpressRouteCircuit 모델에서 AllowGlobalReach 필드의 사용 중단을 부르는 호환성이 손상되는 변경 속성이 추가됨</span><span class="sxs-lookup"><span data-stu-id="73f1f-1886">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="73f1f-1887">AzApplicationGatewayRedirectConfiguration cmdlet에서 TargetListenerID를 사용하는 중의 8756 오류 문제가 해결됨</span><span class="sxs-lookup"><span data-stu-id="73f1f-1887">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="73f1f-1888">다시 쓰기 규칙 세트가 설정되지 못하게 하는 New-AzApplicationGatewayPathRuleConfig의 버그를 수정했습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1888">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="73f1f-1889">NetworkInterfaceIpConfiguration에 VirtualNetworkTaps가 표시되는 방식이 수정됨</span><span class="sxs-lookup"><span data-stu-id="73f1f-1889">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="73f1f-1890">모든 파트를 나열하도록 Cortex Get cmdlet이 수정됨</span><span class="sxs-lookup"><span data-stu-id="73f1f-1890">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="73f1f-1891">ExpressRouteGateways, VpnGateway에 대한 VirtualHub 참조 생성 수정됨</span><span class="sxs-lookup"><span data-stu-id="73f1f-1891">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="73f1f-1892">AzureFirewall 및 NatGateway의 가용성 영역에 대한 지원 추가됨</span><span class="sxs-lookup"><span data-stu-id="73f1f-1892">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="73f1f-1893">Get-AzNetworkServiceTag cmdlet 추가됨</span><span class="sxs-lookup"><span data-stu-id="73f1f-1893">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="73f1f-1894">Azure Firewall에 대한 여러 공용 IP 주소에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="73f1f-1894">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="73f1f-1895">New-AzFirewall cmdlet이 업데이트됨:</span><span class="sxs-lookup"><span data-stu-id="73f1f-1895">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="73f1f-1896">하나 이상의 공용 IP 주소 개체를 허용하는 매개 변수 -PublicIpAddress 추가됨</span><span class="sxs-lookup"><span data-stu-id="73f1f-1896">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="73f1f-1897">Virtual Network 개체를 허용하는 매개 변수 -VirtualNetwork 추가됨</span><span class="sxs-lookup"><span data-stu-id="73f1f-1897">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="73f1f-1898">방화벽 개체에 AddPublicIpAddress 및 RemovePublicIpAddress 메서드 추가됨 - 공용 IP 주소 개체를 입력으로 허용</span><span class="sxs-lookup"><span data-stu-id="73f1f-1898">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="73f1f-1899">매개 변수 -PublicIpName 및 -VirtualNetworkName이 더 이상 사용되지 않음</span><span class="sxs-lookup"><span data-stu-id="73f1f-1899">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span>
* <span data-ttu-id="73f1f-1900">기능에 대한 새로운 명령이 업데이트됨: VpnClient AAD 인증 옵션을 가상 네트워크 게이트웨이 리소스로 설정했습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1900">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span>
    - <span data-ttu-id="73f1f-1901">New-AzVirtualNetworkGateway가 업데이트됨: 게이트웨이에서 VpnClient AAD 인증 옵션을 설정할 수 있도록 선택적 매개 변수 AadTenantUri, AadAudienceId, AadIssuerUri가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1901">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="73f1f-1902">Set-AzVirtualNetworkGateway가 업데이트됨: 게이트웨이에서 VpnClient AAD 인증 옵션을 설정할 수 있도록 선택적 매개 변수 AadTenantUri, AadAudienceId, AadIssuerUri가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1902">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="73f1f-1903">Set-AzVirtualNetworkGateway가 업데이트됨: 게이트웨이에서 VpnClient AAD 인증 옵션을 제거할 수 있도록 선택적인 스위치 매개 변수 RemoveAadAuthentication이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1903">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="73f1f-1904">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="73f1f-1904">Az.OperationalInsights</span></span>
* <span data-ttu-id="73f1f-1905">'New-AzureRmOperationalInsightsWorkspace' 명령에서 **pergb2018** 가격 책정 계층 사용</span><span class="sxs-lookup"><span data-stu-id="73f1f-1905">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="73f1f-1906">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="73f1f-1906">Az.Resources</span></span>
* <span data-ttu-id="73f1f-1907">추가 템플릿 내보내기 옵션 지원</span><span class="sxs-lookup"><span data-stu-id="73f1f-1907">Support for additional Template Export options</span></span>
    - <span data-ttu-id="73f1f-1908">Export-AzResourceGroup에 '-SkipResourceNameParameterization' 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="73f1f-1908">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="73f1f-1909">Export-AzResourceGroup에 '-SkipAllParameterization' 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="73f1f-1909">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="73f1f-1910">내보낸 리소스 필터링을 위해 Export-AzResourceGroup에 '-Resource' 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="73f1f-1910">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="73f1f-1911">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="73f1f-1911">Az.ServiceFabric</span></span>
* <span data-ttu-id="73f1f-1912">일부 경우 잘못된 지문을 가져오는 추가 인증서 ByExistingKeyVault 수정</span><span class="sxs-lookup"><span data-stu-id="73f1f-1912">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="73f1f-1913">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="73f1f-1913">Az.Sql</span></span>
* <span data-ttu-id="73f1f-1914">Advanced Threat Protection 스토리지 엔드포인트 접미사 수정</span><span class="sxs-lookup"><span data-stu-id="73f1f-1914">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="73f1f-1915">Advanced Data Security가 Advanced Threat Protection 정책을 재정의하는 것을 수정</span><span class="sxs-lookup"><span data-stu-id="73f1f-1915">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="73f1f-1916">고객이 TDE 키를 추가하고 관리되는 인스턴스에 TDE 보호기를 설정할 수 있도록 Management.Sql용 새 Cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="73f1f-1916">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="73f1f-1917">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="73f1f-1917">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="73f1f-1918">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="73f1f-1918">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="73f1f-1919">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="73f1f-1919">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="73f1f-1920">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="73f1f-1920">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="73f1f-1921">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="73f1f-1921">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="73f1f-1922">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="73f1f-1922">Az.Storage</span></span>
* <span data-ttu-id="73f1f-1923">스토리지 계정 생성 시 종류 FileStorage 및 SkuName Premium_ZRS 지원</span><span class="sxs-lookup"><span data-stu-id="73f1f-1923">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="73f1f-1924">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="73f1f-1924">New-AzStorageAccount</span></span>
* <span data-ttu-id="73f1f-1925">BLOB immutability cmdlet의 설명 명확화</span><span class="sxs-lookup"><span data-stu-id="73f1f-1925">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="73f1f-1926">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="73f1f-1926">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="73f1f-1927">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="73f1f-1927">Az.Websites</span></span>
* <span data-ttu-id="73f1f-1928">Get-AzWebAppCertificate를 클라이언트 대신 서버의 리소스 그룹별로 필터링하도록 최적화</span><span class="sxs-lookup"><span data-stu-id="73f1f-1928">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="73f1f-1929">Get-AzWebAppSnapshot에 -UseDisasterRecovery 스위치 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="73f1f-1929">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="73f1f-1930">2.2.0 - 2019년 6월</span><span class="sxs-lookup"><span data-stu-id="73f1f-1930">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="73f1f-1931">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="73f1f-1931">Az.Cdn</span></span>
* <span data-ttu-id="73f1f-1932">cmdlet에서 2019-04-15 API 버전 기반의 rulesEngine 기능을 지원하도록 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1932">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="73f1f-1933">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="73f1f-1933">Az.Compute</span></span>
* <span data-ttu-id="73f1f-1934">작업을 시작하여 완료되기 전에 즉시 반환하는 `NoWait` 매개 변수가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1934">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="73f1f-1935">다음 Cmdlet이 업데이트 되었습니다.   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="73f1f-1935">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="73f1f-1936">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="73f1f-1936">Az.EventHub</span></span>
* <span data-ttu-id="73f1f-1937">#9231 수정 - Get-AzEventHubNamespace에서 태그를 반환하지 않음</span><span class="sxs-lookup"><span data-stu-id="73f1f-1937">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="73f1f-1938">#9230 수정 - Get-AzEventHubNamespace에서 ResourceGroupName 대신 ResourceGroup을 반환함</span><span class="sxs-lookup"><span data-stu-id="73f1f-1938">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="73f1f-1939">Az.Network</span><span class="sxs-lookup"><span data-stu-id="73f1f-1939">Az.Network</span></span>
* <span data-ttu-id="73f1f-1940">Nat Gateway에 대한 ResourceId 및 InputObject 업데이트</span><span class="sxs-lookup"><span data-stu-id="73f1f-1940">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="73f1f-1941">ResourceId 및 InputObject에 대한 별칭 추가</span><span class="sxs-lookup"><span data-stu-id="73f1f-1941">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="73f1f-1942">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="73f1f-1942">Az.PolicyInsights</span></span>
* <span data-ttu-id="73f1f-1943">Get-AzPolicyEvent에서 Null 참조 문제 해결</span><span class="sxs-lookup"><span data-stu-id="73f1f-1943">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="73f1f-1944">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="73f1f-1944">Az.RecoveryServices</span></span>
* <span data-ttu-id="73f1f-1945">IaaSVM 정책 최소 보존 기간(일)이 1에서 7로 변경됨</span><span class="sxs-lookup"><span data-stu-id="73f1f-1945">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="73f1f-1946">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="73f1f-1946">Az.ServiceBus</span></span>
* <span data-ttu-id="73f1f-1947">#9182 문제 해결 - Get-AzServiceBusNamespace에서 ResourceGroupName 대신 ResourceGroup을 반환</span><span class="sxs-lookup"><span data-stu-id="73f1f-1947">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="73f1f-1948">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="73f1f-1948">Az.ServiceFabric</span></span>
* <span data-ttu-id="73f1f-1949">'Update-AzServiceFabricReliability' 오류 메시지의 오타 수정</span><span class="sxs-lookup"><span data-stu-id="73f1f-1949">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="73f1f-1950">Service Fabric 명령줄에서 누락된 문자 수정</span><span class="sxs-lookup"><span data-stu-id="73f1f-1950">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="73f1f-1951">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="73f1f-1951">Az.Sql</span></span>
* <span data-ttu-id="73f1f-1952">Managed Instance에 대한 AutoDr을 지원하기 위해 New-AzureSqlInstance cmdlet에 대한 DnsZonePartner 매개 변수를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1952">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="73f1f-1953">Get-AzSqlDatabaseSecureConnectionPolicy cmdlet 사용 중단</span><span class="sxs-lookup"><span data-stu-id="73f1f-1953">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="73f1f-1954">Threat Detection(위협 탐지) cmdlet 이름을 Advanced Threat Protection으로 변경함</span><span class="sxs-lookup"><span data-stu-id="73f1f-1954">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="73f1f-1955">새 AzSqlInstance -StorageSizeInGB 및 -LicenseType 매개 변수는 이제 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1955">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="73f1f-1956">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="73f1f-1956">Az.Websites</span></span>
* <span data-ttu-id="73f1f-1957">-WebApp 속성에서 Set-AzWebApp 및 Set-AzWebAppSlot을 사용하면 태그가 제거되는 문제를 해결함</span><span class="sxs-lookup"><span data-stu-id="73f1f-1957">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="73f1f-1958">2.1.0 - 2019년 5월</span><span class="sxs-lookup"><span data-stu-id="73f1f-1958">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="73f1f-1959">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="73f1f-1959">Az.ApiManagement</span></span>
* <span data-ttu-id="73f1f-1960">글로벌 및 API 범위에서 진단을 관리하기 위한 새 cmdlet을 만들었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1960">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="73f1f-1961">**Get-AzApiManagementDiagnostic** - 글로벌 또는 API 범위가 구성된 진단 가져오기</span><span class="sxs-lookup"><span data-stu-id="73f1f-1961">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="73f1f-1962">**New-AzApiManagementDiagnostic** - 글로벌 범위 또는 API 범위에서 새 진단 만들기</span><span class="sxs-lookup"><span data-stu-id="73f1f-1962">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="73f1f-1963">**New-AzApiManagementHttpMessageDiagnostic** - 기록할 Headers(헤더) 및 Body Bytes(본문 바이트 수) 크기에 대한 진단 설정 만들기</span><span class="sxs-lookup"><span data-stu-id="73f1f-1963">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="73f1f-1964">**New-AzApiManagementPipelineDiagnosticSetting** - 게이트웨이로 들어오고 나가는 HTTP 메시지에 대한 진단 설정 만들기</span><span class="sxs-lookup"><span data-stu-id="73f1f-1964">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="73f1f-1965">**New-AzApiManagementSamplingSetting** - 진단 요청/응답에 대한 샘플링 설정 만들기</span><span class="sxs-lookup"><span data-stu-id="73f1f-1965">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="73f1f-1966">**Remove-AzApiManagementDiagnostic** - 글로벌 또는 API 범위에서 진단 엔터티 제거</span><span class="sxs-lookup"><span data-stu-id="73f1f-1966">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="73f1f-1967">**Set-AzApiManagementDiagnostic** - 글로벌 또는 API 범위에서 진단 엔터티 업데이트</span><span class="sxs-lookup"><span data-stu-id="73f1f-1967">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="73f1f-1968">ApiManagement 서비스에서 캐시를 관리하기 위한 새 cmdlet을 만들었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1968">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="73f1f-1969">**Get-AzApiManagementCache** - 식별자 또는 모든 캐시로 지정된 캐시의 세부 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="73f1f-1969">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="73f1f-1970">**New-AzApiManagementCache** - 특정 Azure 'region'(지역)에 새 'default'(기본) 캐시 만들기</span><span class="sxs-lookup"><span data-stu-id="73f1f-1970">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="73f1f-1971">**Remove-AzApiManagementCache** - 캐시 제거</span><span class="sxs-lookup"><span data-stu-id="73f1f-1971">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="73f1f-1972">**Update-AzApiManagementCache** - 캐시 업데이트</span><span class="sxs-lookup"><span data-stu-id="73f1f-1972">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="73f1f-1973">API 스키마 관리하기 위한 새 cmdlet을 만들었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1973">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="73f1f-1974">**New-AzApiManagementSchema** - API에 대한 새 스키마 만들기</span><span class="sxs-lookup"><span data-stu-id="73f1f-1974">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="73f1f-1975">**Get-AzApiManagementSchema** - API에 구성된 스키마 가져오기</span><span class="sxs-lookup"><span data-stu-id="73f1f-1975">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="73f1f-1976">**Remove-AzApiManagementSchema** - API에 구성된 스키마 제거</span><span class="sxs-lookup"><span data-stu-id="73f1f-1976">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="73f1f-1977">**Set-AzApiManagementSchema** - API에 구성된 스키마 업데이트</span><span class="sxs-lookup"><span data-stu-id="73f1f-1977">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="73f1f-1978">사용자 토큰을 생성하기 위한 새 cmdlet을 만들었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1978">Created new Cmdlet for generating a User Token.</span></span>
    - <span data-ttu-id="73f1f-1979">**New-AzApiManagementUserToken** - 기본적으로 8시간 동안 유효한 새 사용자 토큰을 생성합니다. 'GIT' 사용자에 대한 토큰은 이 cmdlet을 사용하여 생성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1979">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="73f1f-1980">네트워크 상태를 검색하기 위한 새 cmdlet을 만들었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1980">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="73f1f-1981">**Get-AzApiManagementNetworkStatus** - API Management 서비스에서 사용하는 리소스의 네트워크 상태 연결을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1981">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="73f1f-1982">ApiManagement 서비스를 가상 네트워크에 배포하고 종속성이 손상되었는지 여부를 확인할 때 유용합니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1982">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="73f1f-1983">**New-AzApiManagement** cmdlet에서 ApiManagement 서비스를 관리하도록 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1983">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span>
    - <span data-ttu-id="73f1f-1984">새 '소비' SKU 지원이 추가됨</span><span class="sxs-lookup"><span data-stu-id="73f1f-1984">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="73f1f-1985">'소비' SKU에 대해 'EnableClientCertificate' 플래그를 설정하기 위한 지원이 추가됨</span><span class="sxs-lookup"><span data-stu-id="73f1f-1985">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="73f1f-1986">새 **New-AzApiManagementSslSetting** cmdlet을 사용하면 'Backend(백 엔드)' 및 'Frontend'(프런트 엔드)에서 'TLS/SSL' 설정을 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1986">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="73f1f-1987">또한 ApiManagement 서비스의 'Frontend'에서 '3DES'와 같은 'Ciphers'와 'Http2'와 같은 'ServerProtocols'를 구성하는 데 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1987">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="73f1f-1988">ApiManagement 서비스에서 'DeveloperPortal' 호스트 이름을 구성하기 위한 지원이 추가됨</span><span class="sxs-lookup"><span data-stu-id="73f1f-1988">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="73f1f-1989">**Get-AzApiManagementSsoToken** cmdlet에서 'PsApiManagement' 개체를 입력으로 사용하도록 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1989">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="73f1f-1990">cmdlet에서 오류 메시지를 인라인으로 표시하도록 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1990">Updated the cmdlet to display Error Messages inline</span></span>
     > <span data-ttu-id="73f1f-1991">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : 오류 코드: ValidationError 오류 메시지: 하나 이상의 필드에 잘못된 값이 있습니다. 오류 세부 정보:    [Code=ValidationError, Message=줄 3, 열 10의 'log-to-eventhub' 요소에 오류가 있습니다.: 로거를 찾지 못함, Target=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="73f1f-1991">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="73f1f-1992">**Export-AzApiManagementApi** cmdlet에서 API를 'OpenApi 3.0' 형식으로 내보내도록 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1992">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="73f1f-1993">**Import-AzApiManagementApi** cmdlet을 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1993">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="73f1f-1994">'OpenApi 3.0' 문서 사양에서 API 가져오기</span><span class="sxs-lookup"><span data-stu-id="73f1f-1994">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="73f1f-1995">문서('Swagger', 'Wadl', 'Wsdl', 'OpenApi')에 지정된 'PsApiManagementSchema' 속성 재정의</span><span class="sxs-lookup"><span data-stu-id="73f1f-1995">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="73f1f-1996">문서에 지정된 'ServiceUrl' 속성 재정의</span><span class="sxs-lookup"><span data-stu-id="73f1f-1996">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="73f1f-1997">**Get-AzApiManagementPolicy** cmdlet에서 'rawxml'을 사용하여 이스케이프된 비 Xml 'format'(형식)의 정책을 반환하도록 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1997">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="73f1f-1998">**Set-AzApiManagementPolicy** cmdlet에서 'rawxml'을 사용하여 이스케이프된 비 Xml 'format'의 정책을 수락하고, 'xml'을 사용하여 이스케이프된 Xml 'format'의 정책을 수락하도록 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1998">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="73f1f-1999">**New-AzApiManagementApi** cmdlet을 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-1999">Updated cmdlet **New-AzApiManagementApi**</span></span>
    - <span data-ttu-id="73f1f-2000">'OpenId' 권한 부여 서버를 사용하여 API 구성</span><span class="sxs-lookup"><span data-stu-id="73f1f-2000">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="73f1f-2001">'ApiVersionSet'에서 API 만들기</span><span class="sxs-lookup"><span data-stu-id="73f1f-2001">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="73f1f-2002">'SourceApiId' 및 'SourceApiRevision'을 사용하여 API 복제</span><span class="sxs-lookup"><span data-stu-id="73f1f-2002">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="73f1f-2003">API 범위에서 'SubscriptionRequired' 구성 가능</span><span class="sxs-lookup"><span data-stu-id="73f1f-2003">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="73f1f-2004">**Set-AzApiManagementApi** cmdlet을 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-2004">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="73f1f-2005">'OpenId' 권한 부여 서버를 사용하여 API 구성</span><span class="sxs-lookup"><span data-stu-id="73f1f-2005">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="73f1f-2006">API를 'ApiVersionSet'으로 업데이트</span><span class="sxs-lookup"><span data-stu-id="73f1f-2006">To updated an API into an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="73f1f-2007">API 범위에서 'SubscriptionRequired' 구성 가능</span><span class="sxs-lookup"><span data-stu-id="73f1f-2007">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="73f1f-2008">**New-AzApiManagementRevision** cmdlet을 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-2008">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="73f1f-2009">'SourceApiRevision'을 사용하여 기존 수정 버전 복제(태그, 제품, 작업 및 정책 복사).</span><span class="sxs-lookup"><span data-stu-id="73f1f-2009">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="73f1f-2010">새 수정 버전은 부모의 'ApiId'를 가정합니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-2010">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="73f1f-2011">'ApiRevisionDescription' 제공</span><span class="sxs-lookup"><span data-stu-id="73f1f-2011">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="73f1f-2012">API 복제 시 'ServiceUrl' 재정의</span><span class="sxs-lookup"><span data-stu-id="73f1f-2012">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="73f1f-2013">**New-AzApiManagementIdentityProvider** cmdlet을 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-2013">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="73f1f-2014">'Authority'를 사용하여 'AAD' 또는 'AADB2C' 구성</span><span class="sxs-lookup"><span data-stu-id="73f1f-2014">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="73f1f-2015">'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' 및 'PasswordResetPolicy' 설정</span><span class="sxs-lookup"><span data-stu-id="73f1f-2015">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="73f1f-2016">**New-AzApiManagementSubscription** cmdlet을 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-2016">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="73f1f-2017">'Scope' 및 'UserId'를 사용하여 새 SubscriptonModel 설명</span><span class="sxs-lookup"><span data-stu-id="73f1f-2017">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="73f1f-2018">'ProductId' 및 'UserId'를 사용하여 이전 구독 모델 설명</span><span class="sxs-lookup"><span data-stu-id="73f1f-2018">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="73f1f-2019">구독 수준에서 'AllowTracing'을 사용하도록 설정하는 지원 추가</span><span class="sxs-lookup"><span data-stu-id="73f1f-2019">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="73f1f-2020">**Set-AzApiManagementSubscription** cmdlet을 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-2020">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="73f1f-2021">'Scope' 및 'UserId'를 사용하여 새 SubscriptonModel 설명</span><span class="sxs-lookup"><span data-stu-id="73f1f-2021">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="73f1f-2022">'ProductId' 및 'UserId'를 사용하여 이전 구독 모델 설명</span><span class="sxs-lookup"><span data-stu-id="73f1f-2022">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="73f1f-2023">구독 수준에서 'AllowTracing'을 사용하도록 설정하는 지원 추가</span><span class="sxs-lookup"><span data-stu-id="73f1f-2023">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="73f1f-2024">다음 cmdlet에서 'ResourceId'를 입력으로 수락하도록 업데이트했습니다</span><span class="sxs-lookup"><span data-stu-id="73f1f-2024">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="73f1f-2025">'New-AzApiManagementContext'</span><span class="sxs-lookup"><span data-stu-id="73f1f-2025">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="73f1f-2026">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="73f1f-2026">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="73f1f-2027">'Get-AzApiManagementApiRelease'</span><span class="sxs-lookup"><span data-stu-id="73f1f-2027">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="73f1f-2028">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="73f1f-2028">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="73f1f-2029">'Get-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="73f1f-2029">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="73f1f-2030">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="73f1f-2030">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="73f1f-2031">'Get-AzApiManagementAuthorizationServer'</span><span class="sxs-lookup"><span data-stu-id="73f1f-2031">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="73f1f-2032">'Get-AzApiManagementBackend'</span><span class="sxs-lookup"><span data-stu-id="73f1f-2032">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="73f1f-2033">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="73f1f-2033">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="73f1f-2034">'Get-AzApiManagementCertificate'</span><span class="sxs-lookup"><span data-stu-id="73f1f-2034">'Get-AzApiManagementCertificate'</span></span>
    - <span data-ttu-id="73f1f-2035">'Remove-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="73f1f-2035">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="73f1f-2036">'Remove-AzApiManagementSubscription'</span><span class="sxs-lookup"><span data-stu-id="73f1f-2036">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="73f1f-2037">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="73f1f-2037">Az.Automation</span></span>
* <span data-ttu-id="73f1f-2038">Get-AzAutomationJobOutputRecord에서 JSON 및 Text 레코드 값을 처리하도록 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-2038">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="73f1f-2039">문제 https://github.com/Azure/azure-powershell/issues/7977 수정</span><span class="sxs-lookup"><span data-stu-id="73f1f-2039">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="73f1f-2040">문제 https://github.com/Azure/azure-powershell/issues/8600 수정</span><span class="sxs-lookup"><span data-stu-id="73f1f-2040">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="73f1f-2041">Start-AzAutomationDscCompilationJob에서 완료될 때까지 기다리지 않고 작업을 바로 시작하도록 변경했습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-2041">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="73f1f-2042">문제 https://github.com/Azure/azure-powershell/issues/8347 수정</span><span class="sxs-lookup"><span data-stu-id="73f1f-2042">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="73f1f-2043">-Name을 사용하면 모든 노드를 반환하는 Get-AzAutomationDscNode 수정.</span><span class="sxs-lookup"><span data-stu-id="73f1f-2043">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="73f1f-2044">이제 일치하는 노드만 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-2044">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="73f1f-2045">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="73f1f-2045">Az.Compute</span></span>
* <span data-ttu-id="73f1f-2046">ProtectFromScaleIn 및 ProtectFromScaleSetAction 매개 변수를 Update-AzVmssVM cmdlet에 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-2046">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="73f1f-2047">'East US'(미국 동부)가 지원되지 않는 경우 이제 New-AzVM wimple 매개 변수 집합에서 기본적으로 사용 가능한 위치를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-2047">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="73f1f-2048">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="73f1f-2048">Az.DataLakeStore</span></span>
* <span data-ttu-id="73f1f-2049">ADLS SDK에서 httpclient를 사용하도록 업데이트하고, 데이터 평면 테스트를 Azure 프레임워크와 통합합니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-2049">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="73f1f-2050">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="73f1f-2050">Az.Monitor</span></span>
* <span data-ttu-id="73f1f-2051">도움말 예제에서 잘못된 매개 변수 이름을 수정했습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-2051">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="73f1f-2052">Az.Network</span><span class="sxs-lookup"><span data-stu-id="73f1f-2052">Az.Network</span></span>
* <span data-ttu-id="73f1f-2053">DisableBgpRoutePropagation 플래그를 유효 경로 테이블 출력에 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-2053">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="73f1f-2054">업데이트된 cmdlet:</span><span class="sxs-lookup"><span data-stu-id="73f1f-2054">Updated cmdlet:</span></span>
        - <span data-ttu-id="73f1f-2055">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="73f1f-2055">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="73f1f-2056">New-AzApplicationGatewayTrustedRootCertificate 설명서에서 이중 파선을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-2056">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="73f1f-2057">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="73f1f-2057">Az.Resources</span></span>
* <span data-ttu-id="73f1f-2058">할당 거부를 검색하기 위한 새 Get-AzureRmDenyAssignment cmdlet을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-2058">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="73f1f-2059">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="73f1f-2059">Az.Sql</span></span>
* <span data-ttu-id="73f1f-2060">Advanced Threat Protection cmdlet의 이름을 Advanced Data Security로 변경하고, 취약성 평가를 기본적으로 사용하도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-2060">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="73f1f-2061">2.0.0 - 2019년 5월</span><span class="sxs-lookup"><span data-stu-id="73f1f-2061">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="73f1f-2062">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="73f1f-2062">Az.Accounts</span></span>
* <span data-ttu-id="73f1f-2063">사용자 이름/비밀번호 인증을 사용하여 ADFS 문제를 해결하도록 인증 라이브러리 업데이트</span><span class="sxs-lookup"><span data-stu-id="73f1f-2063">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="73f1f-2064">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="73f1f-2064">Az.CognitiveServices</span></span>
* <span data-ttu-id="73f1f-2065">Bing Search 서비스에 대해서만 Bing 면책 조항을 표시하세요.</span><span class="sxs-lookup"><span data-stu-id="73f1f-2065">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="73f1f-2066">계정 생성 실패 시 오류 개선.</span><span class="sxs-lookup"><span data-stu-id="73f1f-2066">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="73f1f-2067">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="73f1f-2067">Az.Compute</span></span>
* <span data-ttu-id="73f1f-2068">근접 배치 그룹 기능</span><span class="sxs-lookup"><span data-stu-id="73f1f-2068">Proximity placement group feature.</span></span>
    - <span data-ttu-id="73f1f-2069">다음과 같은 새 cmdlet을 추가했습니다.   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="73f1f-2069">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="73f1f-2070">새 매개 변수 ProximityPlacementGroupId가 다음 cmdlet에 추가됩니다.   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="73f1f-2070">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="73f1f-2071">New-AzGalleryImageVersion에 StorageAccountType 매개 변수가 추가됩니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-2071">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="73f1f-2072">New-AzGalleryImageVersion의 TargetRegion이 StorageAccountType를 포함할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-2072">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="73f1f-2073">SkipShutdown 스위치 매개 변수가 Stop-AzVM 및 Stop-AzVmss에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-2073">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>
* <span data-ttu-id="73f1f-2074">주요 변경 내용</span><span class="sxs-lookup"><span data-stu-id="73f1f-2074">Breaking changes</span></span>
    - <span data-ttu-id="73f1f-2075">Set-AzVMBootDiagnostics이 Set-AzVMBootDiagnostic으로 변경됩니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-2075">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="73f1f-2076">Export-AzLogAnalyticThrottledRequests이 Export-AzLogAnalyticThrottledRequests로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-2076">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="73f1f-2077">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="73f1f-2077">Az.DeploymentManager</span></span>
* <span data-ttu-id="73f1f-2078">Azure 배포 관리자 cmdlet의 일반적으로 사용 가능한 첫 번째 릴리스</span><span class="sxs-lookup"><span data-stu-id="73f1f-2078">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="73f1f-2079">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="73f1f-2079">Az.Dns</span></span>
* <span data-ttu-id="73f1f-2080">자동 DNS 이름 서버 위임</span><span class="sxs-lookup"><span data-stu-id="73f1f-2080">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="73f1f-2081">DNS 영역 만들기 cmdlet은 추가 선택적 매개 변수로 부모 영역 이름을 허용합니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-2081">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="73f1f-2082">새로 생성 된 자식 영역의 부모 영역에 NS 레코드를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-2082">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="73f1f-2083">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="73f1f-2083">Az.FrontDoor</span></span>
* <span data-ttu-id="73f1f-2084">Azure FrontDoor cmdlet의 일반적으로 사용 가능한 첫 번째 릴리스</span><span class="sxs-lookup"><span data-stu-id="73f1f-2084">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="73f1f-2085">'Waf'를 포함하도록 WAF cmdlet의 이름 바꾸기</span><span class="sxs-lookup"><span data-stu-id="73f1f-2085">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="73f1f-2086">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="73f1f-2086">Az.HDInsight</span></span>
* <span data-ttu-id="73f1f-2087">두 개의 cmdlet을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-2087">Removed two cmdlets:</span></span>
    - <span data-ttu-id="73f1f-2088">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="73f1f-2088">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="73f1f-2089">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="73f1f-2089">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="73f1f-2090">Grant-AzHDInsightHttpServicesAccess를 대체할 새 cmdlet Set-AzHDInsightGatewayCredential을 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-2090">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="73f1f-2091">reader 역할과 HDInsight 운영자 역할을 구분하도록 cmdlet Get-AzHDInsightJobOutput 업데이트:</span><span class="sxs-lookup"><span data-stu-id="73f1f-2091">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="73f1f-2092">reader 역할을 가진 사용자는 'DefaultStorageAccountKey'매개 변수를 명시적으로 지정해야 합니다. 그렇지 않으면 오류가 발생합니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-2092">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="73f1f-2093">Hdinsight 운영자 역할을 가진 사용자를 영향을 받지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-2093">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="73f1f-2094">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="73f1f-2094">Az.Monitor</span></span>
* <span data-ttu-id="73f1f-2095">SQR API(예약 쿼리 규칙)용 새 cmdlet</span><span class="sxs-lookup"><span data-stu-id="73f1f-2095">New cmdlets for SQR API (Scheduled Query Rule)</span></span>
    - <span data-ttu-id="73f1f-2096">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="73f1f-2096">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="73f1f-2097">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="73f1f-2097">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="73f1f-2098">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="73f1f-2098">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="73f1f-2099">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="73f1f-2099">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="73f1f-2100">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="73f1f-2100">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="73f1f-2101">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="73f1f-2101">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="73f1f-2102">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="73f1f-2102">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="73f1f-2103">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="73f1f-2103">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="73f1f-2104">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="73f1f-2104">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="73f1f-2105">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="73f1f-2105">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="73f1f-2106">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="73f1f-2106">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="73f1f-2107">SQR API에 대한 [자세한 내용](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules)</span><span class="sxs-lookup"><span data-stu-id="73f1f-2107">[More](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="73f1f-2108">GenV2(비 클래식) 메트릭 기반 경고 규칙에 대한 cmdlet을 포함하도록 Az.Monitor.md가 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="73f1f-2108">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="73f1f-2109">Az.Network</span><span class="sxs-lookup"><span data-stu-id="73f1f-2109">Az.Network</span></span>
* <span data-ttu-id="73f1f-2110">Nat 게이트웨이 리소스에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="73f1f-2110">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="73f1f-2111">새로운 cmdlet</span><span class="sxs-lookup"><span data-stu-id="73f1f-2111">New cmdlets</span></span>
        - <span data-ttu-id="73f1f-2112">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="73f1f-2112">New-AzNatGateway</span></span>
        - <span data-ttu-id="73f1f-2113">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="73f1f-2113">Get-AzNatGateway</span></span>
        - <span data-ttu-id="73f1f-2114">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="73f1f-2114">Set-AzNatGateway</span></span>
        - <span data-ttu-id="73f1f-2115">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="73f1f-2115">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="73f1f-2116">다음 Cmdlet이 업데이트 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-2116">Updated cmdlets</span></span>
        - <span data-ttu-id="73f1f-2117">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="73f1f-2117">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="73f1f-2118">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="73f1f-2118">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="73f1f-2119">기능에 대한 새로운 명령이 업데이트됨: Brooklyn Gateway에서 사용자 지정 경로 설정/제거.</span><span class="sxs-lookup"><span data-stu-id="73f1f-2119">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="73f1f-2120">New-AzVirtualNetworkGateway가 업데이트됨: 선택적 매개 변수 -CustomRoute를 추가하여 게이트웨이에서 설정할 사용자 지정 경로로 주소 접두사를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-2120">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="73f1f-2121">Set-AzVirtualNetworkGateway가 업데이트됨: 선택적 매개 변수 -CustomRoute를 추가하여 게이트웨이에서 설정할 사용자 지정 경로로 주소 접두사를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-2121">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="73f1f-2122">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="73f1f-2122">Az.PolicyInsights</span></span>
* <span data-ttu-id="73f1f-2123">정책 평가 세부 정보 쿼리 지원</span><span class="sxs-lookup"><span data-stu-id="73f1f-2123">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="73f1f-2124">Get-AzPolicyState에 '-Expand'매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="73f1f-2124">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="73f1f-2125">'-Expand PolicyEvaluationDetails' 지원</span><span class="sxs-lookup"><span data-stu-id="73f1f-2125">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="73f1f-2126">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="73f1f-2126">Az.RecoveryServices</span></span>
* <span data-ttu-id="73f1f-2127">크로스 구독 Azure에서 Azure 사이트 복구 지원</span><span class="sxs-lookup"><span data-stu-id="73f1f-2127">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="73f1f-2128">Azure Site Recovery에 대한 호환성이 손상되는 변경 표시</span><span class="sxs-lookup"><span data-stu-id="73f1f-2128">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="73f1f-2129">Azure Site Recovery 복구 계획 최종 실행 계획에 대한 수정</span><span class="sxs-lookup"><span data-stu-id="73f1f-2129">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="73f1f-2130">Azure에서 Azure에 대한 Azure Site Recovery 업데이트 네트워크 매핑 수정</span><span class="sxs-lookup"><span data-stu-id="73f1f-2130">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="73f1f-2131">관리 디스크에 대한 Azure에서 Azure에 대한 Azure Site Recovery 업데이트 보호 방향 수정</span><span class="sxs-lookup"><span data-stu-id="73f1f-2131">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="73f1f-2132">기타 사소한 수정.</span><span class="sxs-lookup"><span data-stu-id="73f1f-2132">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="73f1f-2133">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="73f1f-2133">Az.Relay</span></span>
* <span data-ttu-id="73f1f-2134">고객 관련 메시지의 철자 오류 수정</span><span class="sxs-lookup"><span data-stu-id="73f1f-2134">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="73f1f-2135">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="73f1f-2135">Az.ServiceBus</span></span>
* <span data-ttu-id="73f1f-2136">네임스페이스의 NetworkRuleSet에 대한 새 cmdlet가 추가되었습니다</span><span class="sxs-lookup"><span data-stu-id="73f1f-2136">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="73f1f-2137">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="73f1f-2137">Az.Storage</span></span>
* <span data-ttu-id="73f1f-2138">저장소 클라이언트 라이브러리 10.0.1로 업그레이드(이 SDK의 모든 개체의 네임스페이스가 'Microsoft.WindowsAzure.Storage. *'에서 'Microsoft.Azure.Storage.* '로 변경됨)</span><span class="sxs-lookup"><span data-stu-id="73f1f-2138">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="73f1f-2139">새로운 API 버전 2019-04-01을 지원하기 위해 Microsoft.Azure.Management.Storage 11.0.0으로 업그레이드합니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-2139">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="73f1f-2140">스토리지 생성 계정의 기본 스토리지 계정 종류가 'Storage'에서 'StorageV2'로 변경됩니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-2140">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="73f1f-2141">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="73f1f-2141">New-AzStorageAccount</span></span>
* <span data-ttu-id="73f1f-2142">'StandardLRS'가 'Standard_LRS'로 변경되는 것과 같이 '-'을 추가하여 입력 SkuName과 정렬되도록 스토리지 계정 cmdlet 출력 Sku.Name을 변경합니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-2142">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="73f1f-2143">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="73f1f-2143">New-AzStorageAccount</span></span>
    - <span data-ttu-id="73f1f-2144">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="73f1f-2144">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="73f1f-2145">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="73f1f-2145">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="73f1f-2146">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="73f1f-2146">Az.Websites</span></span>
* <span data-ttu-id="73f1f-2147">Get-AzWebApp에서 반환한 PSSite 개체에 대해 'Kind'속성이 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-2147">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="73f1f-2148">Get-AzWebApp\* 메트릭 및 Get-AzAppServicePlanMetrics가 사용되지 않음으로 표시되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-2148">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="73f1f-2149">1.8.0 - 2019년 4월</span><span class="sxs-lookup"><span data-stu-id="73f1f-2149">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="73f1f-2150">마지막 주 릴리스 이후의 주요 사항</span><span class="sxs-lookup"><span data-stu-id="73f1f-2150">Highlights since the last major release</span></span>
* <span data-ttu-id="73f1f-2151">`Az` 모듈 일반 공급</span><span class="sxs-lookup"><span data-stu-id="73f1f-2151">General availability of `Az` module</span></span>
* <span data-ttu-id="73f1f-2152">`Az` 모듈에 대한 자세한 내용은 https://aka.ms/azps-announce 를 방문하세요.</span><span class="sxs-lookup"><span data-stu-id="73f1f-2152">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="73f1f-2153">Location, ResourceGroup 및 ResourceName 완성자가 추가되었습니다(https://azure.microsoft.com/blog/completers-in-azure-powershell/ ).</span><span class="sxs-lookup"><span data-stu-id="73f1f-2153">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="73f1f-2154">와일드카드 지원이 Az.Compute 및 Az.Network에 대한 Get cmdlet에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-2154">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="73f1f-2155">Windows PowerShell 5.1 전용 대화형 사용자 이름/암호 인증이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-2155">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="73f1f-2156">Python 2 Runbook 지원이 Az.Automation에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-2156">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="73f1f-2157">Az.LogicApp: 통합 계정 어셈블리 및 일괄 처리 구성을 위한 새로운 cmdlet입니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-2157">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="73f1f-2158">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="73f1f-2158">Az.Accounts</span></span>
* <span data-ttu-id="73f1f-2159">Mac에서 모듈을 올바르게 삭제하기 위해 Uninstall-AzureRm을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-2159">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="73f1f-2160">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="73f1f-2160">Az.Batch</span></span>
* <span data-ttu-id="73f1f-2161">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-2161">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="73f1f-2162">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="73f1f-2162">Az.Cdn</span></span>
* <span data-ttu-id="73f1f-2163">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-2163">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="73f1f-2164">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="73f1f-2164">Az.CognitiveServices</span></span>
* <span data-ttu-id="73f1f-2165">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-2165">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="73f1f-2166">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="73f1f-2166">Az.Compute</span></span>
* <span data-ttu-id="73f1f-2167">디스크의 리소스 ID에 리소스 ID의 소문자 resourcegroups가 있는 경우 AEM 설치 문제 수정</span><span class="sxs-lookup"><span data-stu-id="73f1f-2167">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="73f1f-2168">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-2168">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="73f1f-2169">와일드 카드에 대한 설명서 수정</span><span class="sxs-lookup"><span data-stu-id="73f1f-2169">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="73f1f-2170">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="73f1f-2170">Az.DataFactory</span></span>
* <span data-ttu-id="73f1f-2171">NodeCount가 관리형 통합 런타임에 대해 Null이 아닌 경우 SsisProperties를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-2171">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="73f1f-2172">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="73f1f-2172">Az.DataLakeStore</span></span>
* <span data-ttu-id="73f1f-2173">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-2173">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="73f1f-2174">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="73f1f-2174">Az.EventGrid</span></span>
* <span data-ttu-id="73f1f-2175">이벤트 구독 cmdlet 만들기/업데이트를 사용하기 전에 리소스를 만들어야 함을 나타내기 위해 엔드포인트의 도움말 텍스트가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-2175">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="73f1f-2176">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="73f1f-2176">Az.EventHub</span></span>
* <span data-ttu-id="73f1f-2177">네임스페이스의 NetworkRuleSet에 대한 새 cmdlet가 추가되었습니다</span><span class="sxs-lookup"><span data-stu-id="73f1f-2177">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="73f1f-2178">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="73f1f-2178">Az.HDInsight</span></span>
* <span data-ttu-id="73f1f-2179">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-2179">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="73f1f-2180">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="73f1f-2180">Az.IotHub</span></span>
* <span data-ttu-id="73f1f-2181">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-2181">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="73f1f-2182">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="73f1f-2182">Az.KeyVault</span></span>
* <span data-ttu-id="73f1f-2183">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-2183">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="73f1f-2184">와일드 카드에 대한 설명서 수정</span><span class="sxs-lookup"><span data-stu-id="73f1f-2184">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="73f1f-2185">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="73f1f-2185">Az.MachineLearning</span></span>
* <span data-ttu-id="73f1f-2186">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-2186">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="73f1f-2187">Az.Media</span><span class="sxs-lookup"><span data-stu-id="73f1f-2187">Az.Media</span></span>
* <span data-ttu-id="73f1f-2188">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-2188">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="73f1f-2189">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="73f1f-2189">Az.Monitor</span></span>
  * <span data-ttu-id="73f1f-2190">GenV2(비 클래식) 메트릭 기반 경고 규칙에 대한 새 cmdlet</span><span class="sxs-lookup"><span data-stu-id="73f1f-2190">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="73f1f-2191">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="73f1f-2191">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="73f1f-2192">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="73f1f-2192">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="73f1f-2193">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="73f1f-2193">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="73f1f-2194">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="73f1f-2194">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="73f1f-2195">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="73f1f-2195">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="73f1f-2196">모니터 SDK가 버전 0.22.0-preview로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-2196">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="73f1f-2197">Az.Network</span><span class="sxs-lookup"><span data-stu-id="73f1f-2197">Az.Network</span></span>
* <span data-ttu-id="73f1f-2198">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-2198">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="73f1f-2199">와일드 카드에 대한 설명서 수정</span><span class="sxs-lookup"><span data-stu-id="73f1f-2199">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="73f1f-2200">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="73f1f-2200">Az.NotificationHubs</span></span>
* <span data-ttu-id="73f1f-2201">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-2201">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="73f1f-2202">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="73f1f-2202">Az.OperationalInsights</span></span>
* <span data-ttu-id="73f1f-2203">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-2203">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="73f1f-2204">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="73f1f-2204">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="73f1f-2205">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-2205">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="73f1f-2206">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="73f1f-2206">Az.RecoveryServices</span></span>
* <span data-ttu-id="73f1f-2207">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-2207">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="73f1f-2208">Azure VM의 SQL용 테이블 형식이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-2208">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="73f1f-2209">AzureFileShare에서 위치를 가져오는 대체 메서드가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-2209">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="73f1f-2210">시간대에 따라 SchedulePolicy 개체의 ScheduleRunDays가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-2210">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="73f1f-2211">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="73f1f-2211">Az.RedisCache</span></span>
* <span data-ttu-id="73f1f-2212">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-2212">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="73f1f-2213">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="73f1f-2213">Az.Resources</span></span>
* <span data-ttu-id="73f1f-2214">와일드 카드에 대한 설명서 수정</span><span class="sxs-lookup"><span data-stu-id="73f1f-2214">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="73f1f-2215">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="73f1f-2215">Az.Sql</span></span>
* <span data-ttu-id="73f1f-2216">Monitor SDK의 종속성을 공용 코드로 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-2216">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="73f1f-2217">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-2217">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="73f1f-2218">다중 열 분류 프로세스가 향상되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-2218">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="73f1f-2219">기본적으로 Get-AzSqlServerServiceObjective의 응답으로 SKU 속성(SKU 이름, 제품군, 용량)과 테이블 형식을 포함합니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-2219">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="73f1f-2220">해당 지역에 기존 서버 없이 위치별로 Get-AzSqlServerServiceObjective를 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-2220">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="73f1f-2221">관리형 인스턴스 생성 시 표준 시간대 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-2221">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="73f1f-2222">와일드 카드에 대한 설명서 수정</span><span class="sxs-lookup"><span data-stu-id="73f1f-2222">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="73f1f-2223">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="73f1f-2223">Az.Websites</span></span>
* <span data-ttu-id="73f1f-2224">실행 시 태그를 제거하지 않도록 Set-AzWebApp 및 Set-AzWebAppSlot를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-2224">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="73f1f-2225">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-2225">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="73f1f-2226">WebSites SDK가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-2226">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="73f1f-2227">PSAppServicePlan에서 AdminSiteName 속성을 제거했습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-2227">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="73f1f-2228">1.7.0 - 2019년 4월</span><span class="sxs-lookup"><span data-stu-id="73f1f-2228">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="73f1f-2229">마지막 주 릴리스 이후의 주요 사항</span><span class="sxs-lookup"><span data-stu-id="73f1f-2229">Highlights since the last major release</span></span>
* <span data-ttu-id="73f1f-2230">`Az` 모듈 일반 공급</span><span class="sxs-lookup"><span data-stu-id="73f1f-2230">General availability of `Az` module</span></span>
* <span data-ttu-id="73f1f-2231">`Az` 모듈에 대한 자세한 내용은 https://aka.ms/azps-announce 를 방문하세요.</span><span class="sxs-lookup"><span data-stu-id="73f1f-2231">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="73f1f-2232">Location, ResourceGroup 및 ResourceName 완성자가 추가되었습니다(https://azure.microsoft.com/blog/completers-in-azure-powershell/ ).</span><span class="sxs-lookup"><span data-stu-id="73f1f-2232">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="73f1f-2233">와일드카드 지원이 Az.Compute 및 Az.Network에 대한 Get cmdlet에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-2233">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="73f1f-2234">Windows PowerShell 5.1 전용 대화형 사용자 이름/암호 인증이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-2234">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="73f1f-2235">Python 2 Runbook 지원이 Az.Automation에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-2235">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="73f1f-2236">Az.LogicApp: 통합 계정 어셈블리 및 일괄 처리 구성을 위한 새로운 cmdlet입니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-2236">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="73f1f-2237">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="73f1f-2237">Az.Accounts</span></span>
* <span data-ttu-id="73f1f-2238">매개 변수 AzureAnalysisServicesEndpointResourceId를 허용하도록 Add-AzEnvironment 및 Set-AzEnvironment 업데이트</span><span class="sxs-lookup"><span data-stu-id="73f1f-2238">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="73f1f-2239">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="73f1f-2239">Az.AnalysisServices</span></span>
* <span data-ttu-id="73f1f-2240">데이터 평면 cmdlet에서 ServiceClient 사용 및 원본 인증 논리 제거</span><span class="sxs-lookup"><span data-stu-id="73f1f-2240">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="73f1f-2241">호환성이 손상되는 변경을 방지하기 위해 Add-AzureASAccount를 Connect-AzAccount의 래퍼로 만듦</span><span class="sxs-lookup"><span data-stu-id="73f1f-2241">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="73f1f-2242">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="73f1f-2242">Az.Automation</span></span>
* <span data-ttu-id="73f1f-2243">포함에 대한 New-AzAutomationSoftwareUpdateConfiguration cmdlet 버그 수정</span><span class="sxs-lookup"><span data-stu-id="73f1f-2243">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="73f1f-2244">이제 매개 변수 IncludedKbNumber 및 IncludedPackageNameMask가 작동함</span><span class="sxs-lookup"><span data-stu-id="73f1f-2244">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="73f1f-2245">Azure 자동화 업데이트 관리 동적 그룹에 대한 버그 수정</span><span class="sxs-lookup"><span data-stu-id="73f1f-2245">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="73f1f-2246">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="73f1f-2246">Az.Compute</span></span>
* <span data-ttu-id="73f1f-2247">New-AzDiskConfig 및 New-AzSnapshotConfig에 HyperVGeneration 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="73f1f-2247">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="73f1f-2248">다른 테넌트의 갤러리 이미지를 사용하여 VM을 만들 수 있음</span><span class="sxs-lookup"><span data-stu-id="73f1f-2248">Allow VM creation with galley image from other tenants.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="73f1f-2249">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="73f1f-2249">Az.ContainerInstance</span></span>
* <span data-ttu-id="73f1f-2250">후행 빈 인수를 추가한 New-AzContainerGroup의 -Command 매개 변수의 문제 수정</span><span class="sxs-lookup"><span data-stu-id="73f1f-2250">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="73f1f-2251">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="73f1f-2251">Az.DataFactory</span></span>
* <span data-ttu-id="73f1f-2252">ADF .Net SDK 버전을 3.0.2로 업데이트</span><span class="sxs-lookup"><span data-stu-id="73f1f-2252">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="73f1f-2253">RepoConfiguration 관련 설정에 대한 추가 매개 변수로 Set-AzDataFactoryV2 cmdlet을 업데이트</span><span class="sxs-lookup"><span data-stu-id="73f1f-2253">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="73f1f-2254">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="73f1f-2254">Az.Resources</span></span>
* <span data-ttu-id="73f1f-2255">'-ResourceId' 또는 '-ResourceGroupName', '-Name' 및 '-ResourceType' 매개 변수를 제공할 때 'Get-AzResource'에 대한 공급자 처리 개선</span><span class="sxs-lookup"><span data-stu-id="73f1f-2255">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="73f1f-2256">'Test-AzDeployment' 및 'Test-AzResourceGroupDeployment'에 대한 오류 처리 개선</span><span class="sxs-lookup"><span data-stu-id="73f1f-2256">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="73f1f-2257">배포 유효성 검사 외부에서 발생한 오류를 처리하고 그 대신 명령의 출력에 포함</span><span class="sxs-lookup"><span data-stu-id="73f1f-2257">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="73f1f-2258">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/6856 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="73f1f-2258">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="73f1f-2259">배포 cmdlet 세트에 스크립트 및 작업 시나리오에서 프롬프트를 건너뛰는 '-IgnoreDynamicParameters' 스위치 추가</span><span class="sxs-lookup"><span data-stu-id="73f1f-2259">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="73f1f-2260">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/6856 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="73f1f-2260">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="73f1f-2261">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="73f1f-2261">Az.Sql</span></span>
* <span data-ttu-id="73f1f-2262">데이터베이스 데이터 분류 지원</span><span class="sxs-lookup"><span data-stu-id="73f1f-2262">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="73f1f-2263">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="73f1f-2263">Az.Storage</span></span>
* <span data-ttu-id="73f1f-2264">매개 변수 -UseConnectedAccount를 사용하여 스토리지 컨텍스트를 만들 때 자세한 오류 보고(단, 로그인 Azure 계정 없이)</span><span class="sxs-lookup"><span data-stu-id="73f1f-2264">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="73f1f-2265">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="73f1f-2265">New-AzStorageContext</span></span>
* <span data-ttu-id="73f1f-2266">관리 평면 API를 사용하여 지정한 스토리지 계정의 BLOB 서비스 속성 관리 지원</span><span class="sxs-lookup"><span data-stu-id="73f1f-2266">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="73f1f-2267">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="73f1f-2267">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="73f1f-2268">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="73f1f-2268">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="73f1f-2269">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="73f1f-2269">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="73f1f-2270">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="73f1f-2270">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="73f1f-2271">BLOB 및 파일 업로드/다운로드 cmdlet에 대한 -AsJob 지원</span><span class="sxs-lookup"><span data-stu-id="73f1f-2271">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="73f1f-2272">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="73f1f-2272">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="73f1f-2273">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="73f1f-2273">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="73f1f-2274">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="73f1f-2274">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="73f1f-2275">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="73f1f-2275">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="73f1f-2276">1.6.0 - 2019년 3월</span><span class="sxs-lookup"><span data-stu-id="73f1f-2276">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="73f1f-2277">마지막 주 릴리스 이후의 주요 사항</span><span class="sxs-lookup"><span data-stu-id="73f1f-2277">Highlights since the last major release</span></span>
* <span data-ttu-id="73f1f-2278">`Az` 모듈 일반 공급</span><span class="sxs-lookup"><span data-stu-id="73f1f-2278">General availability of `Az` module</span></span>
* <span data-ttu-id="73f1f-2279">`Az` 모듈에 대한 자세한 내용은 https://aka.ms/azps-announce 를 방문하세요.</span><span class="sxs-lookup"><span data-stu-id="73f1f-2279">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="73f1f-2280">Location, ResourceGroup 및 ResourceName 완성자가 추가되었습니다(https://azure.microsoft.com/blog/completers-in-azure-powershell/ ).</span><span class="sxs-lookup"><span data-stu-id="73f1f-2280">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="73f1f-2281">와일드카드 지원이 Az.Compute 및 Az.Network에 대한 Get cmdlet에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-2281">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="73f1f-2282">Windows PowerShell 5.1 전용 대화형 사용자 이름/암호 인증이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-2282">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="73f1f-2283">Python 2 Runbook 지원이 Az.Automation에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-2283">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="73f1f-2284">Az.LogicApp: 통합 계정 어셈블리 및 일괄 처리 구성을 위한 새로운 cmdlet입니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-2284">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="73f1f-2285">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="73f1f-2285">Az.Automation</span></span>
* <span data-ttu-id="73f1f-2286">Azure 자동화 업데이트 관리에서 변경된 지원 기능은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-2286">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="73f1f-2287">동적 그룹화</span><span class="sxs-lookup"><span data-stu-id="73f1f-2287">Dynamic grouping</span></span>
    * <span data-ttu-id="73f1f-2288">사전 스크립트</span><span class="sxs-lookup"><span data-stu-id="73f1f-2288">Pre-Post script</span></span>
    * <span data-ttu-id="73f1f-2289">다시 부팅 설정</span><span class="sxs-lookup"><span data-stu-id="73f1f-2289">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="73f1f-2290">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="73f1f-2290">Az.Compute</span></span>
* <span data-ttu-id="73f1f-2291">Get-AzVmBootDiagnosticsData의 경로 확인 문제가 해결되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-2291">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="73f1f-2292">Compute 클라이언트 라이브러리가 25.0.0으로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-2292">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="73f1f-2293">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="73f1f-2293">Az.KeyVault</span></span>
* <span data-ttu-id="73f1f-2294">와일드카드 지원이 KeyVault cmdlet에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-2294">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="73f1f-2295">Az.Network</span><span class="sxs-lookup"><span data-stu-id="73f1f-2295">Az.Network</span></span>
* <span data-ttu-id="73f1f-2296">Azure Firewall에 대한 위협 인텔리전스 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-2296">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="73f1f-2297">Application Gateway 방화벽 정책의 최상위 수준 리소스 및 사용자 지정 규칙이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-2297">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="73f1f-2298">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="73f1f-2298">Az.RecoveryServices</span></span>
* <span data-ttu-id="73f1f-2299">인스턴트 RP를 지원하기 위해 SnapshotRetentionInDays가 Azure VM 정책에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-2299">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="73f1f-2300">컨테이너 등록을 취소하는 파이프 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-2300">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="73f1f-2301">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="73f1f-2301">Az.Resources</span></span>
* <span data-ttu-id="73f1f-2302">Get-AzResource 및 Get-AzResourceGroup에 대한 와일드카드 지원을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-2302">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="73f1f-2303">ARM에 대한 일반 호출을 수행할 때 사용되는 자격 증명을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-2303">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="73f1f-2304">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="73f1f-2304">Az.Sql</span></span>
* <span data-ttu-id="73f1f-2305">위협 탐지의 cmdlet 매개 변수(ExcludeDetectionType)가 DetectionType에서 string[]으로 변경되어 새 DetectionType이 추가되면 이후의 증명이 되고 자동 완성도 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-2305">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="73f1f-2306">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="73f1f-2306">Az.Storage</span></span>
* <span data-ttu-id="73f1f-2307">스토리지 계정에 대한 관리 정책 가져오기/설정/제거를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-2307">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="73f1f-2308">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="73f1f-2308">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="73f1f-2309">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="73f1f-2309">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="73f1f-2310">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="73f1f-2310">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="73f1f-2311">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="73f1f-2311">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="73f1f-2312">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="73f1f-2312">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="73f1f-2313">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="73f1f-2313">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="73f1f-2314">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="73f1f-2314">Az.Websites</span></span>
* <span data-ttu-id="73f1f-2315">'New-AzWebApp -IncludeSourceWebAppSlots'를 사용하여 모든 슬롯의 복제를 중단하는 ARM 템플릿 버그가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-2315">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span>

## <a name="150---march-2019"></a><span data-ttu-id="73f1f-2316">1.5.0 - 2019년 3월</span><span class="sxs-lookup"><span data-stu-id="73f1f-2316">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="73f1f-2317">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="73f1f-2317">Az.Accounts</span></span>
* <span data-ttu-id="73f1f-2318">'Register-AzModule' 명령을 추가하여 AutoRest 생성 cmdlet을 지원</span><span class="sxs-lookup"><span data-stu-id="73f1f-2318">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="73f1f-2319">Connect-AzAccount 예제 업데이트</span><span class="sxs-lookup"><span data-stu-id="73f1f-2319">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="73f1f-2320">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="73f1f-2320">Az.Automation</span></span>
* <span data-ttu-id="73f1f-2321">몇몇 Azure Automation cmdlet에서 특정 월별 일정을 검색할 때 발생하는 문제 수정</span><span class="sxs-lookup"><span data-stu-id="73f1f-2321">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="73f1f-2322">상위 20개 노드를 반환하도록 Get-AzAutomationDscNode를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-2322">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="73f1f-2323">이제 모든 노드 반환</span><span class="sxs-lookup"><span data-stu-id="73f1f-2323">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="73f1f-2324">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="73f1f-2324">Az.Cdn</span></span>
* <span data-ttu-id="73f1f-2325">사용자 지정 도메인 Https 사용/사용 안 함에 대한 새 Powershell cmdlet이 추가되었으며 기존의 것은 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-2325">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="73f1f-2326">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="73f1f-2326">Az.Compute</span></span>
* <span data-ttu-id="73f1f-2327">Get cmdlet에 와일드 카드 지원 추가</span><span class="sxs-lookup"><span data-stu-id="73f1f-2327">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="73f1f-2328">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="73f1f-2328">Az.DataFactory</span></span>
* <span data-ttu-id="73f1f-2329">ADF.Net SDK 버전이 3.0.1로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-2329">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="73f1f-2330">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="73f1f-2330">Az.LogicApp</span></span>
* <span data-ttu-id="73f1f-2331">첫 결과 페이지 검색 시에만 ListWorkflows 수정</span><span class="sxs-lookup"><span data-stu-id="73f1f-2331">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="73f1f-2332">Az.Network</span><span class="sxs-lookup"><span data-stu-id="73f1f-2332">Az.Network</span></span>
* <span data-ttu-id="73f1f-2333">Network cmdlet에 와일드 카드 지원 추가</span><span class="sxs-lookup"><span data-stu-id="73f1f-2333">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="73f1f-2334">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="73f1f-2334">Az.RecoveryServices</span></span>
* <span data-ttu-id="73f1f-2335">Azure VM 지원에 SQL 서버가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-2335">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="73f1f-2336">SDK 업데이트</span><span class="sxs-lookup"><span data-stu-id="73f1f-2336">SDK Update</span></span>
* <span data-ttu-id="73f1f-2337">VMappContainer 체크 인 Get-ProtectableItem 제거</span><span class="sxs-lookup"><span data-stu-id="73f1f-2337">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="73f1f-2338">Get ProtectableItem의 매개 변수로 Name과 ServerName이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-2338">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="73f1f-2339">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="73f1f-2339">Az.Resources</span></span>
* <span data-ttu-id="73f1f-2340">`-TemplateObject` 매개 변수를 추가하여 cmdlet을 배포</span><span class="sxs-lookup"><span data-stu-id="73f1f-2340">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="73f1f-2341">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/2933 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="73f1f-2341">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="73f1f-2342">`Get-AzResource`의 결과를 `Set-AzResource`(으)로 파이프할 때 발생하는 문제 수정</span><span class="sxs-lookup"><span data-stu-id="73f1f-2342">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="73f1f-2343">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/8240 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="73f1f-2343">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="73f1f-2344">실행 시 JSON 데이터 형식 문제 해결 `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="73f1f-2344">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="73f1f-2345">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/7930 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="73f1f-2345">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="73f1f-2346">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="73f1f-2346">Az.Sql</span></span>
* <span data-ttu-id="73f1f-2347">AuditingEndpointsCommunicator를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-2347">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="73f1f-2348">새 진단 설정을 생성할 때 에지 사례의 동작을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-2348">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="73f1f-2349">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="73f1f-2349">Az.Storage</span></span>
* <span data-ttu-id="73f1f-2350">스토리지 계정      - New-AzStorageAccount를 생성할 때 종류 BlockBlobStorage를 지원</span><span class="sxs-lookup"><span data-stu-id="73f1f-2350">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="73f1f-2351">1.4.0 - 2019년 2월</span><span class="sxs-lookup"><span data-stu-id="73f1f-2351">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="73f1f-2352">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="73f1f-2352">Az.AnalysisServices</span></span>
* <span data-ttu-id="73f1f-2353">사용되지 않는 AddAzureASAccount cmdlet</span><span class="sxs-lookup"><span data-stu-id="73f1f-2353">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="73f1f-2354">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="73f1f-2354">Az.Automation</span></span>
* <span data-ttu-id="73f1f-2355">Import-AzAutomationDscNodeConfiguration 도움말 업데이트</span><span class="sxs-lookup"><span data-stu-id="73f1f-2355">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="73f1f-2356">Import-AzAutomationDscConfiguration cmdlet 구성 이름 유효성 검사 추가</span><span class="sxs-lookup"><span data-stu-id="73f1f-2356">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="73f1f-2357">Import-AzAutomationDscConfiguration cmdlet 오류 처리 개선</span><span class="sxs-lookup"><span data-stu-id="73f1f-2357">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="73f1f-2358">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="73f1f-2358">Az.CognitiveServices</span></span>
* <span data-ttu-id="73f1f-2359">리소스의 하위 도메인을 지정하는 데 사용되는 New-AzCognitiveServicesAccount에 대한 새 선택적 매개 변수로 CustomSubdomainName이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-2359">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="73f1f-2360">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="73f1f-2360">Az.Compute</span></span>
* <span data-ttu-id="73f1f-2361">ID 매개 변수 집합 문제 해결</span><span class="sxs-lookup"><span data-stu-id="73f1f-2361">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="73f1f-2362">Name 매개 변수를 제공하지 않으면 Get-AzVMExtension이 설치된 모든 확장을 열거하도록 업데이트</span><span class="sxs-lookup"><span data-stu-id="73f1f-2362">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="73f1f-2363">Update-AzImage cmdlet에 태그 및 ResourceId 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="73f1f-2363">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="73f1f-2364">인스턴스 ID가 없는 Get-AzVmssVM과 InstanceView를 사용하면 인스턴스 보기가 있는 VMSS VM을 나열할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-2364">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="73f1f-2365">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="73f1f-2365">Az.DataLakeStore</span></span>
* <span data-ttu-id="73f1f-2366">ADL 삭제된 항목 열거 및 복원에 대한 cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="73f1f-2366">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="73f1f-2367">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="73f1f-2367">Az.EventHub</span></span>
* <span data-ttu-id="73f1f-2368">Eventhub의 CaptureDescription 클래스에서 빈 보관을 건너뛰는 새 부울 속성 SkipEmptyArchives가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-2368">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="73f1f-2369">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="73f1f-2369">Az.KeyVault</span></span>
* <span data-ttu-id="73f1f-2370">Set-AzKeyVaultSecret 태그 지정 수정</span><span class="sxs-lookup"><span data-stu-id="73f1f-2370">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="73f1f-2371">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="73f1f-2371">Az.LogicApp</span></span>
* <span data-ttu-id="73f1f-2372">통합 계정에 대한 기본 sku 추가</span><span class="sxs-lookup"><span data-stu-id="73f1f-2372">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="73f1f-2373">XSLT 2.0, XSLT 3.0, Liquid 맵 형식 추가</span><span class="sxs-lookup"><span data-stu-id="73f1f-2373">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="73f1f-2374">통합 계정 어셈블리에 대한 새 cmdlet</span><span class="sxs-lookup"><span data-stu-id="73f1f-2374">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="73f1f-2375">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="73f1f-2375">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="73f1f-2376">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="73f1f-2376">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="73f1f-2377">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="73f1f-2377">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="73f1f-2378">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="73f1f-2378">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="73f1f-2379">통합 계정 일괄 처리 구성에 대한 새 cmdlet</span><span class="sxs-lookup"><span data-stu-id="73f1f-2379">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="73f1f-2380">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="73f1f-2380">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="73f1f-2381">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="73f1f-2381">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="73f1f-2382">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="73f1f-2382">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="73f1f-2383">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="73f1f-2383">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="73f1f-2384">논리 앱 SDK를 버전 4.1.0으로 업데이트</span><span class="sxs-lookup"><span data-stu-id="73f1f-2384">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="73f1f-2385">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="73f1f-2385">Az.Monitor</span></span>
* <span data-ttu-id="73f1f-2386">Get-AzMetric에 대한 도움말 업데이트</span><span class="sxs-lookup"><span data-stu-id="73f1f-2386">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="73f1f-2387">Az.Network</span><span class="sxs-lookup"><span data-stu-id="73f1f-2387">Az.Network</span></span>
* <span data-ttu-id="73f1f-2388">Add-AzApplicationGatewayCustomError에 대한 도움말 예제 업데이트</span><span class="sxs-lookup"><span data-stu-id="73f1f-2388">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="73f1f-2389">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="73f1f-2389">Az.OperationalInsights</span></span>
* <span data-ttu-id="73f1f-2390">New 및 Get ApplicationInsights 데이터 소스에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="73f1f-2390">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="73f1f-2391">지정된 작업 영역에 대한 특정 또는 전체 ApplicationInsights 데이터 원본 가져오기를 지원하기 위한 새로운 'ApplicationInsights' 종류가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-2391">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span>
    - <span data-ttu-id="73f1f-2392">지정된 Application-Insights 리소스 매개 변수(구독 ID, resourceGroupName 및 이름)별로 데이터 원본을 만들기 위한 New-AzOperationalInsightsApplicationInsightsDataSource cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-2392">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span>

#### <a name="azresources"></a><span data-ttu-id="73f1f-2393">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="73f1f-2393">Az.Resources</span></span>
* <span data-ttu-id="73f1f-2394">문제 https://github.com/Azure/azure-powershell/issues/8166 수정</span><span class="sxs-lookup"><span data-stu-id="73f1f-2394">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="73f1f-2395">문제 https://github.com/Azure/azure-powershell/issues/8235 수정</span><span class="sxs-lookup"><span data-stu-id="73f1f-2395">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="73f1f-2396">문제 https://github.com/Azure/azure-powershell/issues/6219 수정</span><span class="sxs-lookup"><span data-stu-id="73f1f-2396">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="73f1f-2397">KeyCredentials 반복 만들기를 방지하기 위해 버그 수정</span><span class="sxs-lookup"><span data-stu-id="73f1f-2397">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="73f1f-2398">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="73f1f-2398">Az.Sql</span></span>
* <span data-ttu-id="73f1f-2399">SQL DB 하이퍼스케일에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="73f1f-2399">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="73f1f-2400">복원 요청에서 불필요한 속성을 설정하여 복원이 실패할 수 있는 버그 수정</span><span class="sxs-lookup"><span data-stu-id="73f1f-2400">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="73f1f-2401">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="73f1f-2401">Az.Websites</span></span>
* <span data-ttu-id="73f1f-2402">Get-AzWebAppSlotMetrics 내 올바른 예제</span><span class="sxs-lookup"><span data-stu-id="73f1f-2402">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="73f1f-2403">1.3.0 - 2019년 2월</span><span class="sxs-lookup"><span data-stu-id="73f1f-2403">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="73f1f-2404">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="73f1f-2404">Az.Accounts</span></span>
* <span data-ttu-id="73f1f-2405">ClientRuntime 최신 버전 업데이트</span><span class="sxs-lookup"><span data-stu-id="73f1f-2405">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="73f1f-2406">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="73f1f-2406">Az.AnalysisServices</span></span>
<span data-ttu-id="73f1f-2407">Az.AnalysisServices 모듈의 전반적인 가용성.</span><span class="sxs-lookup"><span data-stu-id="73f1f-2407">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="73f1f-2408">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="73f1f-2408">Az.Compute</span></span>
* <span data-ttu-id="73f1f-2409">AEM 확장: UltraSSD 및 P60, P70, P80 디스크에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="73f1f-2409">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="73f1f-2410">Set-AzVMBootDiagnostics에 대한 도움말 업데이트</span><span class="sxs-lookup"><span data-stu-id="73f1f-2410">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="73f1f-2411">Update-AzImage에 대한 도움말 및 예제 업데이트</span><span class="sxs-lookup"><span data-stu-id="73f1f-2411">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="73f1f-2412">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="73f1f-2412">Az.RecoveryServices</span></span>
<span data-ttu-id="73f1f-2413">Az.RecoveryServices 모듈의 전반적인 가용성.</span><span class="sxs-lookup"><span data-stu-id="73f1f-2413">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="73f1f-2414">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="73f1f-2414">Az.Resources</span></span>
* <span data-ttu-id="73f1f-2415">리소스 그룹 관련 태그 수정</span><span class="sxs-lookup"><span data-stu-id="73f1f-2415">Fix tagging for resource groups</span></span>
    - <span data-ttu-id="73f1f-2416">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/8166 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="73f1f-2416">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="73f1f-2417">`Get-AzureRmRoleAssignment`이(가) -ErrorAction을 준수하지 않는 문제 수정</span><span class="sxs-lookup"><span data-stu-id="73f1f-2417">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span>
    - <span data-ttu-id="73f1f-2418">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/8235 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="73f1f-2418">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="73f1f-2419">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="73f1f-2419">Az.Sql</span></span>
* <span data-ttu-id="73f1f-2420">AzSqlDatabaseBackupShortTermRetentionPolicy 가져오기/설정하기 추가</span><span class="sxs-lookup"><span data-stu-id="73f1f-2420">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="73f1f-2421">SQL cmdlet을 실행할 경우 Azure 계정에 로그인되어 있지 않은 것이 nullref 예외를 초래하는 문제 수정</span><span class="sxs-lookup"><span data-stu-id="73f1f-2421">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="73f1f-2422">Get-AzSqlCapability의 nullref 예외 수정</span><span class="sxs-lookup"><span data-stu-id="73f1f-2422">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="73f1f-2423">1.2.1 - 2019년 1월</span><span class="sxs-lookup"><span data-stu-id="73f1f-2423">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="73f1f-2424">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="73f1f-2424">Az.Accounts</span></span>
* <span data-ttu-id="73f1f-2425">올바른 인증 버전을 사용하여 릴리스</span><span class="sxs-lookup"><span data-stu-id="73f1f-2425">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="73f1f-2426">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="73f1f-2426">Az.AnalysisServices</span></span>
* <span data-ttu-id="73f1f-2427">업데이트된 인증 종속성을 사용하여 릴리스</span><span class="sxs-lookup"><span data-stu-id="73f1f-2427">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="73f1f-2428">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="73f1f-2428">Az.RecoveryServices</span></span>
* <span data-ttu-id="73f1f-2429">업데이트된 인증 종속성을 사용하여 릴리스</span><span class="sxs-lookup"><span data-stu-id="73f1f-2429">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="73f1f-2430">1.2.0 - 2019년 1월</span><span class="sxs-lookup"><span data-stu-id="73f1f-2430">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="73f1f-2431">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="73f1f-2431">Az.Accounts</span></span>
* <span data-ttu-id="73f1f-2432">Windows PowerShell 5.1 전용 대화형 사용자 이름/암호 인증 추가</span><span class="sxs-lookup"><span data-stu-id="73f1f-2432">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="73f1f-2433">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="73f1f-2433">Update incorrect online help URLs</span></span>
* <span data-ttu-id="73f1f-2434">Uninstall-AzureRm 관련 PS Core에 경고 메시지 추가</span><span class="sxs-lookup"><span data-stu-id="73f1f-2434">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="73f1f-2435">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="73f1f-2435">Az.Aks</span></span>
* <span data-ttu-id="73f1f-2436">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="73f1f-2436">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="73f1f-2437">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="73f1f-2437">Az.Automation</span></span>
* <span data-ttu-id="73f1f-2438">Python 2 Runbook에 대한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-2438">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="73f1f-2439">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="73f1f-2439">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="73f1f-2440">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="73f1f-2440">Az.Cdn</span></span>
* <span data-ttu-id="73f1f-2441">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="73f1f-2441">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="73f1f-2442">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="73f1f-2442">Az.Compute</span></span>
* <span data-ttu-id="73f1f-2443">Invoke-AzVMReimage cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="73f1f-2443">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="73f1f-2444">Set-AzVmss에 TempDisk 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="73f1f-2444">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="73f1f-2445">New-AzVM 경고 메시지 수정</span><span class="sxs-lookup"><span data-stu-id="73f1f-2445">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="73f1f-2446">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="73f1f-2446">Az.ContainerRegistry</span></span>
* <span data-ttu-id="73f1f-2447">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="73f1f-2447">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="73f1f-2448">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="73f1f-2448">Az.DataFactory</span></span>
* <span data-ttu-id="73f1f-2449">ADF.Net SDK 버전이 3.0.0으로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-2449">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="73f1f-2450">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="73f1f-2450">Az.DataLakeStore</span></span>
* <span data-ttu-id="73f1f-2451">MSI를 사용할 때 ADLS 엔드포인트 문제 수정</span><span class="sxs-lookup"><span data-stu-id="73f1f-2451">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="73f1f-2452">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/7462 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="73f1f-2452">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="73f1f-2453">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="73f1f-2453">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="73f1f-2454">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="73f1f-2454">Az.IotHub</span></span>
* <span data-ttu-id="73f1f-2455">Add-IotHubRoutingEndpoint cmdlet에 인코딩 형식을 추가하세요.</span><span class="sxs-lookup"><span data-stu-id="73f1f-2455">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="73f1f-2456">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="73f1f-2456">Az.KeyVault</span></span>
* <span data-ttu-id="73f1f-2457">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="73f1f-2457">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="73f1f-2458">Az.Network</span><span class="sxs-lookup"><span data-stu-id="73f1f-2458">Az.Network</span></span>
* <span data-ttu-id="73f1f-2459">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="73f1f-2459">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="73f1f-2460">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="73f1f-2460">Az.Resources</span></span>
* <span data-ttu-id="73f1f-2461">'New-AzADAppCredential' 및 'New-AzADSpCredential' 참조 설명서의 잘못된 예제 수정</span><span class="sxs-lookup"><span data-stu-id="73f1f-2461">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="73f1f-2462">리소스 그룹 배포 cmdlet 실행 전 '-TemplateFile' 매개 변수 경로가 확인되지 않는 문제 수정</span><span class="sxs-lookup"><span data-stu-id="73f1f-2462">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="73f1f-2463">Az.Resources: New-AzureRmPolicyDefinition -Mode 기본값에 대한 올바른 설명서</span><span class="sxs-lookup"><span data-stu-id="73f1f-2463">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="73f1f-2464">Az.Resources: 문제 https://github.com/Azure/azure-powershell/issues/7522 수정</span><span class="sxs-lookup"><span data-stu-id="73f1f-2464">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="73f1f-2465">Az.Resources: 문제 https://github.com/Azure/azure-powershell/issues/5747 수정</span><span class="sxs-lookup"><span data-stu-id="73f1f-2465">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="73f1f-2466">'PSResourceGroupDeployment' 개체의 서식 문제 수정</span><span class="sxs-lookup"><span data-stu-id="73f1f-2466">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="73f1f-2467">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/2123 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="73f1f-2467">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="73f1f-2468">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="73f1f-2468">Az.ServiceFabric</span></span>
* <span data-ttu-id="73f1f-2469">인증서가 VMSS 모델에 추가되었는데도 예외가 발생할 경우 롤백합니다. 이는 버그 https://github.com/Azure/service-fabric-issues/issues/932 를 수정하기 위함입니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-2469">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="73f1f-2470">일부 오류 메시지를 수정하세요.</span><span class="sxs-lookup"><span data-stu-id="73f1f-2470">Fix some error messages.</span></span>
* <span data-ttu-id="73f1f-2471">Az로의 마이그레이션을 통해서는 작동하지 않는 New-AzServiceFabriCluster를 위해 기본값 ARM 템플릿을 가진 클러스터 만들기를 수정하세요.</span><span class="sxs-lookup"><span data-stu-id="73f1f-2471">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="73f1f-2472">확장에서 클러스터 id를 확인하여 클러스터에 해당하는 VMSS에만 추가되도록 클러스터/애플리케이션 인증서 추가를 수정하세요.</span><span class="sxs-lookup"><span data-stu-id="73f1f-2472">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="73f1f-2473">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="73f1f-2473">Az.SignalR</span></span>
* <span data-ttu-id="73f1f-2474">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="73f1f-2474">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="73f1f-2475">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="73f1f-2475">Az.Sql</span></span>
* <span data-ttu-id="73f1f-2476">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="73f1f-2476">Update incorrect online help URLs</span></span>
* <span data-ttu-id="73f1f-2477">가능한 값을 가진 LicenseType 매개 변수에 대한 매개 변수 설명이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-2477">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="73f1f-2478">유일하게 업데이트된 속성인데 작동하지 않는 관리되는 인스턴스 ID의 업데이트 수정</span><span class="sxs-lookup"><span data-stu-id="73f1f-2478">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="73f1f-2479">관리되는 인스턴스에서의 사용자 지정 데이터 정렬에 대한 지원</span><span class="sxs-lookup"><span data-stu-id="73f1f-2479">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="73f1f-2480">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="73f1f-2480">Az.Storage</span></span>
* <span data-ttu-id="73f1f-2481">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="73f1f-2481">Update incorrect online help URLs</span></span>
* <span data-ttu-id="73f1f-2482">Premium Storage 계정이 클래식 로깅/메트릭을 지원하지 않기 때문에, Premium Storage 계정의 클래식 로깅/메트릭을 가져올/설정할 때 상세한 오류 메시지를 제공해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-2482">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="73f1f-2483">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="73f1f-2483">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="73f1f-2484">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="73f1f-2484">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="73f1f-2485">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="73f1f-2485">Az.TrafficManager</span></span>
* <span data-ttu-id="73f1f-2486">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="73f1f-2486">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="73f1f-2487">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="73f1f-2487">Az.Websites</span></span>
* <span data-ttu-id="73f1f-2488">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="73f1f-2488">Update incorrect online help URLs</span></span>
* <span data-ttu-id="73f1f-2489">앱이 ASE에 호스팅되면 'New-AzWebAppSSLBinding'을 수정하여 올바른 resourcegroup+location에 인증서를 업로드합니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-2489">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="73f1f-2490">'New-AzWebAppSSLBinding'을 수정하여 SSL 인증서를 앱에 바인딩하는 데 붙는 태그를 덮어쓰지 않도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-2490">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="73f1f-2491">1.1.0 - 2019년 1월</span><span class="sxs-lookup"><span data-stu-id="73f1f-2491">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="73f1f-2492">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="73f1f-2492">Az.Accounts</span></span>
* <span data-ttu-id="73f1f-2493">Enable-AzureRmAlias에 'Local' 범위 추가</span><span class="sxs-lookup"><span data-stu-id="73f1f-2493">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="73f1f-2494">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="73f1f-2494">Az.Compute</span></span>
* <span data-ttu-id="73f1f-2495">이름이 Restart/Start/Stop/Remove/Set-AzVM과 Save-AzVMImage에 설정된 ID 매개 변수에서 선택 사항이 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-2495">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="73f1f-2496">도움말 파일의 ID에 대한 설명이 업데이트 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-2496">Updated the description of ID in help files</span></span>
* <span data-ttu-id="73f1f-2497">Az.Accounts 모듈을 사용할 때의 이전 버전과의 호환성 문제를 해결합니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-2497">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="73f1f-2498">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="73f1f-2498">Az.DataLakeStore</span></span>
* <span data-ttu-id="73f1f-2499">SDK 수정을 위해 데이터 평면의 SDK 버전을 1.1.14로 업데이트하세요.</span><span class="sxs-lookup"><span data-stu-id="73f1f-2499">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="73f1f-2500">getfilestatus 및 liststatus에 대한 음수 acesstime 및 modificationtime 수정, 비동기 취소 토큰 수정</span><span class="sxs-lookup"><span data-stu-id="73f1f-2500">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="73f1f-2501">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="73f1f-2501">Az.EventGrid</span></span>
* <span data-ttu-id="73f1f-2502">2019-01-01 API 버전을 사용하도록 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-2502">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="73f1f-2503">2019-01-01 API 버전에서 새 시나리오를 지원하도록 다음 cmdlet을 업데이트</span><span class="sxs-lookup"><span data-stu-id="73f1f-2503">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="73f1f-2504">New-AzureRmEventGridSubscription: 지정을 위한 새로운 선택적 매개 변수를 추가</span><span class="sxs-lookup"><span data-stu-id="73f1f-2504">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="73f1f-2505">이벤트 Time-to-Live</span><span class="sxs-lookup"><span data-stu-id="73f1f-2505">Event Time-To-Live,</span></span>
        - <span data-ttu-id="73f1f-2506">이벤트에 대한 최대 배달 시도</span><span class="sxs-lookup"><span data-stu-id="73f1f-2506">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="73f1f-2507">배달 못한 편지의 엔드포인트입니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-2507">Dead letter endpoint.</span></span>
    - <span data-ttu-id="73f1f-2508">Update-AzureRmEventGridSubscription: 지정을 위한 새로운 선택적 매개 변수를 추가</span><span class="sxs-lookup"><span data-stu-id="73f1f-2508">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="73f1f-2509">이벤트 Time-to-Live</span><span class="sxs-lookup"><span data-stu-id="73f1f-2509">Event Time-To-Live,</span></span>
        - <span data-ttu-id="73f1f-2510">이벤트에 대한 최대 배달 시도</span><span class="sxs-lookup"><span data-stu-id="73f1f-2510">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="73f1f-2511">배달 못한 편지의 엔드포인트입니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-2511">Dead letter endpoint.</span></span>
* <span data-ttu-id="73f1f-2512">New-AzureRmEventGridSubscription 및 Update-AzureRmEventGridSubscription cmdlet의 EndpointType 옵션에 새 열거형 값(즉, storageQueue 및 hybridConnection)을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-2512">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="73f1f-2513">이벤트 구독을 생성 또는 업데이트할 때 사용자가 직접 조치를 취해야 할 경우 경고 메시지를 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-2513">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="73f1f-2514">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="73f1f-2514">Az.IotHub</span></span>
* <span data-ttu-id="73f1f-2515">최신 버전의 Azure IotHub SDK로 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="73f1f-2515">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="73f1f-2516">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="73f1f-2516">Az.LogicApp</span></span>
* <span data-ttu-id="73f1f-2517">지정된 이름이 없는 모든 Get-AzLogicApp 목록</span><span class="sxs-lookup"><span data-stu-id="73f1f-2517">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="73f1f-2518">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="73f1f-2518">Az.Resources</span></span>
* <span data-ttu-id="73f1f-2519">'Get-AzResource'에 '-ODataQuery'및 '-ResourceId' 매개 변수를 제공할 때 매개 변수 집합 문제 수정</span><span class="sxs-lookup"><span data-stu-id="73f1f-2519">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="73f1f-2520">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/7875 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="73f1f-2520">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="73f1f-2521">New/Set-AzPolicyDefinition에서 -Custom 매개 변수 처리 문제 수정</span><span class="sxs-lookup"><span data-stu-id="73f1f-2521">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="73f1f-2522">New-AzDeployment 설명서에서 오타 수정</span><span class="sxs-lookup"><span data-stu-id="73f1f-2522">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="73f1f-2523">'New-AzADUser'에 '-MailNickname'매개 변수가 필수 항목으로 지정됨</span><span class="sxs-lookup"><span data-stu-id="73f1f-2523">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="73f1f-2524">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/8220 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="73f1f-2524">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="73f1f-2525">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="73f1f-2525">Az.SignalR</span></span>
* <span data-ttu-id="73f1f-2526">Az.Accounts 모듈을 사용할 때의 이전 버전과의 호환성 문제를 해결합니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-2526">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="73f1f-2527">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="73f1f-2527">Az.Sql</span></span>
* <span data-ttu-id="73f1f-2528">Storage 관리 클라이언트 종속성을 일반적인 SDK 구현으로 변환했습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-2528">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="73f1f-2529">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="73f1f-2529">Az.Storage</span></span>
* <span data-ttu-id="73f1f-2530">Sas Token, OAuth 또는 Anonymous를 사용하여 스토리지 컨텍스트의 StorageAccountName을 실제 스토리지 계정 이름으로 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-2530">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="73f1f-2531">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="73f1f-2531">New-AzStorageContext</span></span>
* <span data-ttu-id="73f1f-2532">'-FullUri' 매개 변수를 사용하여 Blob 스냅샷 개체의 Sas Token을 생성하고 반환된 Uri를 스냅샷 Uri로 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-2532">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="73f1f-2533">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="73f1f-2533">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="73f1f-2534">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="73f1f-2534">Az.Websites</span></span>
* <span data-ttu-id="73f1f-2535">'Get-AzDeletedWebApp'의 날짜 구문 분석 버그를 수정했습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-2535">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="73f1f-2536">Az.Accounts 모듈을 사용할 때의 이전 버전과의 호환성 문제를 해결합니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-2536">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="73f1f-2537">1.0.0 - 2018년 12월</span><span class="sxs-lookup"><span data-stu-id="73f1f-2537">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="73f1f-2538">일반</span><span class="sxs-lookup"><span data-stu-id="73f1f-2538">General</span></span>

- <span data-ttu-id="73f1f-2539">Az 모듈 일반 공급</span><span class="sxs-lookup"><span data-stu-id="73f1f-2539">General Availability of Az Module</span></span>
- <span data-ttu-id="73f1f-2540">각 모듈에 대 한 온라인 도움말</span><span class="sxs-lookup"><span data-stu-id="73f1f-2540">Online help for each module</span></span>
- <span data-ttu-id="73f1f-2541">자세한 내용과 로드맵은 [Az 알림 페이지](https://aka.ms/azps-announce)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="73f1f-2541">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="73f1f-2542">AzureRM에서 마이그레이션하는 것에 대한 정보는 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="73f1f-2542">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="73f1f-2543">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="73f1f-2543">Az.Accounts</span></span>
- <span data-ttu-id="73f1f-2544">Az.Profile에서 변경</span><span class="sxs-lookup"><span data-stu-id="73f1f-2544">Changed from Az.Profile</span></span>
- <span data-ttu-id="73f1f-2545">프로필 및 컨텍스트 형식에 대한 표 형식 수정</span><span class="sxs-lookup"><span data-stu-id="73f1f-2545">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="73f1f-2546">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="73f1f-2546">Az.ApiManagement</span></span>
- <span data-ttu-id="73f1f-2547">#7002에 대한 수정</span><span class="sxs-lookup"><span data-stu-id="73f1f-2547">Fixes for #7002</span></span>
- <span data-ttu-id="73f1f-2548">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="73f1f-2548">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="73f1f-2549">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="73f1f-2549">Az.Batch</span></span>
- <span data-ttu-id="73f1f-2550">`PSComputeNode`의 새로운 `NodeAgentInformation` 속성을 통해 풀의 각 VM에서 실행 중인 Azure Batch 노드 에이전트의 버전을 확인하는 기능이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-2550">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="73f1f-2551">`PSDataDisk`에 대한 `Caching` 기본 값은 이제 `None` 대신 `ReadWrite`입니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-2551">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="73f1f-2552">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="73f1f-2552">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="73f1f-2553">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="73f1f-2553">Az.Billing</span></span>
- <span data-ttu-id="73f1f-2554">청구, 소비 및 UsageAggregates cmdlet 결합 cmdlet에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="73f1f-2554">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="73f1f-2555">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="73f1f-2555">Az.CognitivServices</span></span>
- <span data-ttu-id="73f1f-2556">New-AzureRmCognitiveServicesAccount 작업에서 사용 가능한 SkuName 및 Typem에 대한 완성자 추가</span><span class="sxs-lookup"><span data-stu-id="73f1f-2556">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="73f1f-2557">Get-AzCognitiveServicesAccountSkus에서 GetSkusWithAccountParamSetName 매개 변수 집합을 제거</span><span class="sxs-lookup"><span data-stu-id="73f1f-2557">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="73f1f-2558">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="73f1f-2558">Az.ContainerInstance</span></span>
- <span data-ttu-id="73f1f-2559">ManagedIdentity 지원이 추가됨</span><span class="sxs-lookup"><span data-stu-id="73f1f-2559">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="73f1f-2560">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="73f1f-2560">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="73f1f-2561">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="73f1f-2561">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="73f1f-2562">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="73f1f-2562">Az.DataLakeStore</span></span>
- <span data-ttu-id="73f1f-2563">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="73f1f-2563">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="73f1f-2564">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="73f1f-2564">Az.Monitor</span></span>
- <span data-ttu-id="73f1f-2565">Az.Monitor 이름 변경 및 기타 사소한 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="73f1f-2565">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="73f1f-2566">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="73f1f-2566">Az.KeyVault</span></span>
- <span data-ttu-id="73f1f-2567">출력 형식에서 사용되지 않는 'PurgeDisabled' 속성 제거</span><span class="sxs-lookup"><span data-stu-id="73f1f-2567">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="73f1f-2568">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="73f1f-2568">Az.MachineLearning</span></span>
- <span data-ttu-id="73f1f-2569">Az.MachineLearningCompute 모듈의 cmdlet 포함</span><span class="sxs-lookup"><span data-stu-id="73f1f-2569">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="73f1f-2570">Az.Media</span><span class="sxs-lookup"><span data-stu-id="73f1f-2570">Az.Media</span></span>
- <span data-ttu-id="73f1f-2571">New-AzMediaService에서 사용되지 않는 -Tags 별칭이 제거됨</span><span class="sxs-lookup"><span data-stu-id="73f1f-2571">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="73f1f-2572">Az.Network</span><span class="sxs-lookup"><span data-stu-id="73f1f-2572">Az.Network</span></span>
<span data-ttu-id="73f1f-2573">Application Gateway에서 RewriteRuleSets를 구성하는 것에 대한 지원이 추가됨</span><span class="sxs-lookup"><span data-stu-id="73f1f-2573">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="73f1f-2574">추가된 새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-2574">New cmdlets added:</span></span>
        - <span data-ttu-id="73f1f-2575">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="73f1f-2575">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="73f1f-2576">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="73f1f-2576">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="73f1f-2577">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="73f1f-2577">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="73f1f-2578">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="73f1f-2578">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="73f1f-2579">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="73f1f-2579">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="73f1f-2580">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="73f1f-2580">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="73f1f-2581">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="73f1f-2581">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="73f1f-2582">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="73f1f-2582">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="73f1f-2583">선택적 매개 변수를 사용하도록 cmdlet이 업데이트됨 -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="73f1f-2583">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="73f1f-2584">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="73f1f-2584">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="73f1f-2585">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="73f1f-2585">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="73f1f-2586">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="73f1f-2586">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="73f1f-2587">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="73f1f-2587">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="73f1f-2588">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="73f1f-2588">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="73f1f-2589">New-AzureRmApplicationGatewayUrlPathMapConfig로 ID를 사용하여 Application Gateway에 KeyVault 지원을 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-2589">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="73f1f-2590">선택적 매개 변수를 사용하도록 cmdlet이 업데이트됨 -KeyVaultSecretId, -KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="73f1f-2590">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="73f1f-2591">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="73f1f-2591">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="73f1f-2592">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="73f1f-2592">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="73f1f-2593">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="73f1f-2593">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="73f1f-2594">New-AzApplicationGateway cmdlet이 선택적 매개 변수를 사용하도록 업데이트됨 -UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="73f1f-2594">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="73f1f-2595">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="73f1f-2595">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="73f1f-2596">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="73f1f-2596">Az.OperationalInsights</span></span>
- <span data-ttu-id="73f1f-2597">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="73f1f-2597">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="73f1f-2598">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="73f1f-2598">Az.Profile</span></span>
- <span data-ttu-id="73f1f-2599">Az.Accounts에 모듈 이름이 변경됨</span><span class="sxs-lookup"><span data-stu-id="73f1f-2599">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="73f1f-2600">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="73f1f-2600">Az.RecoveryServices</span></span>
- <span data-ttu-id="73f1f-2601">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="73f1f-2601">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="73f1f-2602">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="73f1f-2602">Az.Resources</span></span>
- <span data-ttu-id="73f1f-2603">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="73f1f-2603">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="73f1f-2604">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="73f1f-2604">Az.ServiceFabric</span></span>
- <span data-ttu-id="73f1f-2605">일반 이름과 지문으로 지정 인증서 지원</span><span class="sxs-lookup"><span data-stu-id="73f1f-2605">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="73f1f-2606">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="73f1f-2606">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="73f1f-2607">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="73f1f-2607">Az.SIgnalR</span></span>
- <span data-ttu-id="73f1f-2608">SIgnalR에 대한 PowerShell cmdlet에 대한 일반 공급</span><span class="sxs-lookup"><span data-stu-id="73f1f-2608">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="73f1f-2609">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="73f1f-2609">Az.Sql</span></span>
- <span data-ttu-id="73f1f-2610">위협 탐지의 cmdlet에 새로운 Data_Exfiltration 및 Unsafe_Action 검색 유형 추가</span><span class="sxs-lookup"><span data-stu-id="73f1f-2610">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="73f1f-2611">Sql 감사 cmdlet에 대한 설명서 예제 업데이트</span><span class="sxs-lookup"><span data-stu-id="73f1f-2611">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="73f1f-2612">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="73f1f-2612">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="73f1f-2613">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="73f1f-2613">Az.Storage</span></span>
- <span data-ttu-id="73f1f-2614">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="73f1f-2614">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="73f1f-2615">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="73f1f-2615">Az.Websites</span></span>
- <span data-ttu-id="73f1f-2616">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="73f1f-2616">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="73f1f-2617">0.7.0 - 2018년 12월</span><span class="sxs-lookup"><span data-stu-id="73f1f-2617">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="73f1f-2618">일반</span><span class="sxs-lookup"><span data-stu-id="73f1f-2618">General</span></span>

* <span data-ttu-id="73f1f-2619">AzureRM에서 Az 전환 예정에 대한 사소한 변경</span><span class="sxs-lookup"><span data-stu-id="73f1f-2619">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="73f1f-2620">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="73f1f-2620">Az.Compute</span></span>

* <span data-ttu-id="73f1f-2621">`New-AzVm(ss)` cmdlet에 대한 간단한 매개 변수 집합에 UltraSSD 및 갤러리 이미지에 대한 지원을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-2621">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="73f1f-2622">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="73f1f-2622">Az.DataLakeStore</span></span>

* <span data-ttu-id="73f1f-2623">ADLS 계정의 도메인의 후행 슬래시를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-2623">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="73f1f-2624">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="73f1f-2624">Az.FrontDoor</span></span>

* <span data-ttu-id="73f1f-2625">일부 끊어진 링크 수정</span><span class="sxs-lookup"><span data-stu-id="73f1f-2625">Fixed some broken links</span></span>
    - <span data-ttu-id="73f1f-2626">New-AzureRmFrontDoor 및 Set-AzureRmFrontDoor 아티클에서 New-AzureRmFrontDoorHealthProbeSettingObject cmdlet 아티클에 대한 링크가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-2626">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="73f1f-2627">New-AzureRmFrontDoorManagedRuleObject 아티클에서 New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet 아티클에 대한 링크가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-2627">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="73f1f-2628">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="73f1f-2628">Az.RecoveryServices</span></span>

* <span data-ttu-id="73f1f-2629">Azure File Share 복원 작업에 클라이언트 측 유효성 검사가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-2629">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="73f1f-2630">afs 복원의 경우 storageAccountName 및 storageAccountResourceGroupName을 선택적으로 만들었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-2630">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="73f1f-2631">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="73f1f-2631">Az.Resources</span></span>

* <span data-ttu-id="73f1f-2632">https://github.com/Azure/azure-powershell/issues/7679 에 대한 수정</span><span class="sxs-lookup"><span data-stu-id="73f1f-2632">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="73f1f-2633">기본 관리자를 요청할 때 구독 범위가 제공되는 경우 Get-AzureRmRoleAssignment를 업데이트하여 구독 범위를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-2633">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="73f1f-2634">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="73f1f-2634">Az.Sql</span></span>

* <span data-ttu-id="73f1f-2635">AzureRM에서 Az 전환 예정에 대한 사소한 변경</span><span class="sxs-lookup"><span data-stu-id="73f1f-2635">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="73f1f-2636">DotNet 코어에서 Get-AzureRmSqlDatabaseVulnerabilityAssessment를 사용하는 문제 해결</span><span class="sxs-lookup"><span data-stu-id="73f1f-2636">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="73f1f-2637">SQL 감사 cmdlet과 관련된 도움말 메시지의 설명서가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-2637">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="73f1f-2638">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="73f1f-2638">Az.Storage</span></span>

* <span data-ttu-id="73f1f-2639">New-AzureRmStorageAccount에 -EnableHierarchicalNamespace 추가</span><span class="sxs-lookup"><span data-stu-id="73f1f-2639">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="73f1f-2640">파일 복사 cmdlet이 -DestContext 입력이 없을 때 대상의 원본 컨텍스트를 다시 사용할 수 없는 문제 수정</span><span class="sxs-lookup"><span data-stu-id="73f1f-2640">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="73f1f-2641">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="73f1f-2641">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="73f1f-2642">고정적인 웹 사이트 구성 지원</span><span class="sxs-lookup"><span data-stu-id="73f1f-2642">Support Static Website configuration</span></span>
    - <span data-ttu-id="73f1f-2643">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="73f1f-2643">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="73f1f-2644">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="73f1f-2644">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="73f1f-2645">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="73f1f-2645">Az.Websites</span></span>

* <span data-ttu-id="73f1f-2646">Set-AzureRmWebApp 및 Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="73f1f-2646">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span>
    - <span data-ttu-id="73f1f-2647">Windows 및 Linux 컨테이너 응용 프로그램에 탑재할 Azure Storage 경로를 지정하기 위해 새 매개 변수(-AzureStoragePath)가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-2647">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="73f1f-2648">새 cmdlet New-AzureRmWebAppAzureStoragePath의 출력을 매개 변수로 사용하여 Azure Storage 경로를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-2648">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="73f1f-2649">0.6.1 - 2018년 11월</span><span class="sxs-lookup"><span data-stu-id="73f1f-2649">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="73f1f-2650">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="73f1f-2650">Az.ApiManagement</span></span>
* <span data-ttu-id="73f1f-2651">형식 매핑 문제에 대한 종속성 업데이트</span><span class="sxs-lookup"><span data-stu-id="73f1f-2651">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="73f1f-2652">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="73f1f-2652">Az.Automation</span></span>
* <span data-ttu-id="73f1f-2653">Azure Automation cmdlet 기반 Swagger</span><span class="sxs-lookup"><span data-stu-id="73f1f-2653">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="73f1f-2654">업데이트 관리 cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="73f1f-2654">Added Update Management cmdlets</span></span>
* <span data-ttu-id="73f1f-2655">소스 제어 cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="73f1f-2655">Added Source Control cmdlets</span></span>
* <span data-ttu-id="73f1f-2656">Remove-AzureRmAutomationHybridWorkerGroup cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="73f1f-2656">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="73f1f-2657">DSC 노드 등록 명령 수정</span><span class="sxs-lookup"><span data-stu-id="73f1f-2657">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="73f1f-2658">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="73f1f-2658">Az.Compute</span></span>
* <span data-ttu-id="73f1f-2659">SystemAssigned ID에 대한 ID 문제 수정</span><span class="sxs-lookup"><span data-stu-id="73f1f-2659">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="73f1f-2660">형식 매핑 문제에 대한 종속성 업데이트</span><span class="sxs-lookup"><span data-stu-id="73f1f-2660">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="73f1f-2661">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="73f1f-2661">Az.ContainerInstance</span></span>
* <span data-ttu-id="73f1f-2662">형식 매핑 문제에 대한 종속성 업데이트</span><span class="sxs-lookup"><span data-stu-id="73f1f-2662">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="73f1f-2663">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="73f1f-2663">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="73f1f-2664">마켓플레이스 cmdlet에 대한 예제 설명 업데이트</span><span class="sxs-lookup"><span data-stu-id="73f1f-2664">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="73f1f-2665">Az.Network</span><span class="sxs-lookup"><span data-stu-id="73f1f-2665">Az.Network</span></span>
* <span data-ttu-id="73f1f-2666">New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="73f1f-2666">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="73f1f-2667">지원되는 AzureFirewall 네트워크 프로토콜에 ICMP 다시 추가</span><span class="sxs-lookup"><span data-stu-id="73f1f-2667">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="73f1f-2668">Test-AzureRmNetworkWatcherConnectivity cmdlet을 업데이트하여 대상 ID, 주소 및 포트 유효성 검사를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-2668">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span>
* <span data-ttu-id="73f1f-2669">VirtualNetwork 맵의 메모리 사용 문제 해결</span><span class="sxs-lookup"><span data-stu-id="73f1f-2669">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="73f1f-2670">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="73f1f-2670">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="73f1f-2671">보호된 파일 공유에 대한 정책을 수정하는 것에 대해 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-2671">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="73f1f-2672">정책 표준 시간대를 대문자로 변환했습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-2672">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="73f1f-2673">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="73f1f-2673">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="73f1f-2674">New-AzureRmRecoveryServicesAsrProtectableItem의 예제 정정</span><span class="sxs-lookup"><span data-stu-id="73f1f-2674">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="73f1f-2675">형식 매핑 문제에 대한 종속성 업데이트</span><span class="sxs-lookup"><span data-stu-id="73f1f-2675">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="73f1f-2676">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="73f1f-2676">Az.Relay</span></span>
* <span data-ttu-id="73f1f-2677">선택적 매개 변수 -KeyValue를 New-AzureRmRelayKey cmdlet에 추가하여 사용자가 KeyValue를 제공할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-2677">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="73f1f-2678">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="73f1f-2678">Az.Resources</span></span>
* <span data-ttu-id="73f1f-2679">`New-AzureRmPolicyAssignment` 및 `Set-AzureRmPolicyAssignment`의 자원 ID 관련 매개 변수에 대한 도움말 문서를 업데이트함</span><span class="sxs-lookup"><span data-stu-id="73f1f-2679">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="73f1f-2680">-Metadata를 사용하는 New-AzureRmPolicyDefinition에 대한 예제 추가</span><span class="sxs-lookup"><span data-stu-id="73f1f-2680">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="73f1f-2681">NetStandard의 태그 키에서 대소문자 보존을 허용하도록 수정: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="73f1f-2681">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="73f1f-2682">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="73f1f-2682">Az.ServiceFabric</span></span>
* <span data-ttu-id="73f1f-2683">향후 호환성이 손상되는 변경에 대한 사용 중단 메시지 추가</span><span class="sxs-lookup"><span data-stu-id="73f1f-2683">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="73f1f-2684">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="73f1f-2684">Az.Sql</span></span>
* <span data-ttu-id="73f1f-2685">Azure Sql Database Managed Instance 및 Azure Sql Managed Database에 CRUD 작업을 위한 새 cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="73f1f-2685">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="73f1f-2686">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="73f1f-2686">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="73f1f-2687">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="73f1f-2687">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="73f1f-2688">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="73f1f-2688">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="73f1f-2689">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="73f1f-2689">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="73f1f-2690">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="73f1f-2690">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="73f1f-2691">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="73f1f-2691">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="73f1f-2692">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="73f1f-2692">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="73f1f-2693">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="73f1f-2693">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="73f1f-2694">서버 또는 데이터베이스에서 확장 감사 정책 관리를 활성화했습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-2694">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="73f1f-2695">새 매개 변수(PredicateExpression)가 감사 로그 필터링을 사용하도록 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-2695">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="73f1f-2696">Cmdlet이 레거시 클라이언트 대신 SQL 클라이언트를 사용하도록 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-2696">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="73f1f-2697">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="73f1f-2697">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="73f1f-2698">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="73f1f-2698">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="73f1f-2699">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="73f1f-2699">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="73f1f-2700">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="73f1f-2700">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="73f1f-2701">스토리지 계정 이름 매개 변수가 설정된 Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings를 사용할 때의 문제 해결</span><span class="sxs-lookup"><span data-stu-id="73f1f-2701">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="73f1f-2702">0.5.0 - 2018년 11월</span><span class="sxs-lookup"><span data-stu-id="73f1f-2702">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="73f1f-2703">일반</span><span class="sxs-lookup"><span data-stu-id="73f1f-2703">General</span></span>
* <span data-ttu-id="73f1f-2704">많은 핵심 cmdlet에 Resource Completers를 추가하여 대화형으로 cmdlet을 호출할 때 기존 리소스 이름을 탭으로 이동할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-2704">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="73f1f-2705">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="73f1f-2705">Az.Profile</span></span>
* <span data-ttu-id="73f1f-2706">ClientRuntime의 최신 버전을 사용하도록 일반적인 코드를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-2706">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="73f1f-2707">Connect-AzAccount cmdlet의 매개 변수 TenantId 이름을 Tenant로 바꾸고 TenantId의 별칭을 추가합니다</span><span class="sxs-lookup"><span data-stu-id="73f1f-2707">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="73f1f-2708">Connect-AzAccount의 업데이트된 TenantId 설명</span><span class="sxs-lookup"><span data-stu-id="73f1f-2708">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="73f1f-2709">테넌트 도메인을 제공할 때 실패한 로그인에 대한 오류 메시지 수정</span><span class="sxs-lookup"><span data-stu-id="73f1f-2709">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="73f1f-2710">테넌트에 구독이 없는 계정의 컨텍스트 이름 충돌 문제 수정</span><span class="sxs-lookup"><span data-stu-id="73f1f-2710">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="73f1f-2711">MSI를 사용할 때 DataLake 엔드포인트 문제 수정</span><span class="sxs-lookup"><span data-stu-id="73f1f-2711">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="73f1f-2712">연결되지 않은 경우 'Disconnect-AzAccount'가 throw하는 문제 수정</span><span class="sxs-lookup"><span data-stu-id="73f1f-2712">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="73f1f-2713">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="73f1f-2713">Az.CognitiveServices</span></span>
* <span data-ttu-id="73f1f-2714">Get-AzCognitiveServicesAccountSkus 작업을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-2714">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="73f1f-2715">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="73f1f-2715">Az.Compute</span></span>
* <span data-ttu-id="73f1f-2716">Add-AzVmssVMDataDisk 및 Remove-AzVmssVMDataDisk cmdlet를 추가합니다</span><span class="sxs-lookup"><span data-stu-id="73f1f-2716">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="73f1f-2717">Get-AzVMImage는 AutomaticOSUpgradeProperties를 표시합니다</span><span class="sxs-lookup"><span data-stu-id="73f1f-2717">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="73f1f-2718">수정된 SetAzVMChefExtension -BootstrapOptions 및 -JsonAttribute option 값이 json 형식으로 설정하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-2718">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="73f1f-2719">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="73f1f-2719">Az.DataLakeStore</span></span>
* <span data-ttu-id="73f1f-2720">DataLake 패키지를 1.1.10으로 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-2720">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="73f1f-2721">기본 동시성을 다중 스레드 작업에 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-2721">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="73f1f-2722">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="73f1f-2722">Az.Insights</span></span>
* <span data-ttu-id="73f1f-2723">해결된 문제 #7267(자동 크기 조정 영역)</span><span class="sxs-lookup"><span data-stu-id="73f1f-2723">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="73f1f-2724">열거된 매개 변수를 제대로 설정하지 않은 새 자동 크기 조정 규칙을 만드는 데 문제가 있습니다(이를 항상 기본값으로 설정함).</span><span class="sxs-lookup"><span data-stu-id="73f1f-2724">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="73f1f-2725">해결된 문제 # 7513[자세한 정보] Set-AzDiagnosticSetting은 설정을 생성하는 동안 범주를 명시적으로 지정해야 합니다</span><span class="sxs-lookup"><span data-stu-id="73f1f-2725">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="73f1f-2726">이제 cmdlet은 생성 중에 사용할 범주를 명시적으로 표시할 필요가 없습니다. 즉, 문서화된대로 작동합니다</span><span class="sxs-lookup"><span data-stu-id="73f1f-2726">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="73f1f-2727">Az.Network</span><span class="sxs-lookup"><span data-stu-id="73f1f-2727">Az.Network</span></span>
* <span data-ttu-id="73f1f-2728">다음 cmdlet에 대해 PeeringType을 필수 매개 변수로 변경했습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-2728">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="73f1f-2729">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="73f1f-2729">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="73f1f-2730">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="73f1f-2730">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="73f1f-2731">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="73f1f-2731">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="73f1f-2732">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="73f1f-2732">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="73f1f-2733">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="73f1f-2733">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="73f1f-2734">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="73f1f-2734">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="73f1f-2735">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="73f1f-2735">Az.PolicyInsights</span></span>
* <span data-ttu-id="73f1f-2736">추가된 정책 재구성 cmdlet</span><span class="sxs-lookup"><span data-stu-id="73f1f-2736">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="73f1f-2737">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="73f1f-2737">Az.Resources</span></span>
* <span data-ttu-id="73f1f-2738">https://github.com/Azure/azure-powershell/issues/7402 에 대한 수정</span><span class="sxs-lookup"><span data-stu-id="73f1f-2738">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="73f1f-2739">'Get-AzResource'에 대해 '-ResourceId' 매개 변수를 사용하여 리소스 나열 허용</span><span class="sxs-lookup"><span data-stu-id="73f1f-2739">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="73f1f-2740">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="73f1f-2740">Az.ServiceBus</span></span>
* <span data-ttu-id="73f1f-2741">마이그레이션 상태를 알 수 있도록 PSServiceBusMigrationConfigurationAttributes에 MigrationState 읽기 전용 속성 추가.</span><span class="sxs-lookup"><span data-stu-id="73f1f-2741">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="73f1f-2742">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="73f1f-2742">Az.ServiceFabric</span></span>
* <span data-ttu-id="73f1f-2743">Linux Vmss에 인증서 추가 수정.</span><span class="sxs-lookup"><span data-stu-id="73f1f-2743">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="73f1f-2744">Add-AzServiceFabricClusterCertificate 수정</span><span class="sxs-lookup"><span data-stu-id="73f1f-2744">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="73f1f-2745">새 인증서(Azure/service-fabric-issues#932)에서 올바른 지문을 사용.</span><span class="sxs-lookup"><span data-stu-id="73f1f-2745">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="73f1f-2746">올바르게 예외 표시(Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="73f1f-2746">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="73f1f-2747">Vmss CreateOrUpdate 작업을 시작하기 전에 'Update-AzServiceFabricDurability'를 수정하여 클러스터 구성 업데이트.</span><span class="sxs-lookup"><span data-stu-id="73f1f-2747">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="73f1f-2748">0.4.0 - 2018년 10월</span><span class="sxs-lookup"><span data-stu-id="73f1f-2748">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="73f1f-2749">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="73f1f-2749">Az.Profile</span></span>
* <span data-ttu-id="73f1f-2750">CloudShell에서 Get-AzSubscription을 사용하여 문제를 해결합니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-2750">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="73f1f-2751">ClientRuntime의 최신 버전을 사용하도록 일반적인 코드를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-2751">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="73f1f-2752">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="73f1f-2752">Az.Compute</span></span>
* <span data-ttu-id="73f1f-2753">'New-AzVm'에 대해 간단한 매개 변수를 사용하는 경우 가속화된 네트워킹을 설정하기 위해 새 크기가 VM 크기의 허용 목록에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-2753">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="73f1f-2754">모든 cmdlet에 ResourceName 인수 완성자가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-2754">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="73f1f-2755">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="73f1f-2755">Az.DataLakeStore</span></span>
* <span data-ttu-id="73f1f-2756">Virtual Network 규칙에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="73f1f-2756">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="73f1f-2757">Get-AzDataLakeStoreVirtualNetworkRule: Azure Data Lake Store 가상 네트워크 규칙을 가져오거나 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-2757">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="73f1f-2758">Add-AzDataLakeStoreVirtualNetworkRule: 지정된 Data Lake Store 계정에 가상 네트워크 규칙을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-2758">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="73f1f-2759">Set-AzDataLakeStoreVirtualNetworkRule: 지정된 Data Lake Store 계정에 지정된 가상 네트워크 규칙을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-2759">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="73f1f-2760">Remove-AzDataLakeStoreVirtualNetworkRule: Azure Data Lake Store 가상 네트워크 규칙을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-2760">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="73f1f-2761">Az.Network</span><span class="sxs-lookup"><span data-stu-id="73f1f-2761">Az.Network</span></span>
* <span data-ttu-id="73f1f-2762">Test-AzNetworkWatcherConnectivity cmdlet을 업데이트하고, 백 엔드에 프로토콜 값을 전달합니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-2762">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="73f1f-2763">모든 cmdlet에 ResourceName 인수 완성자가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-2763">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="73f1f-2764">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="73f1f-2764">Az.Resources</span></span>
* <span data-ttu-id="73f1f-2765">(기본 프로필에 구독이 없고 범위가 지정되지 않은 경우) 시나리오에서 의미 있는 예외를 추가하여 Get-AzRoleDefinition이 인식할 수 없는 예외를 throw하는 문제를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-2765">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="73f1f-2766">또한 기본 매개 변수 집합을 'RoleDefinitionNameParameterSet'으로 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-2766">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="73f1f-2767">0.3.0 - 2018년 10월</span><span class="sxs-lookup"><span data-stu-id="73f1f-2767">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="73f1f-2768">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="73f1f-2768">Azure.Storage</span></span>
* <span data-ttu-id="73f1f-2769">대상에 메타데이터가 있을 때 Blob/파일이 메타 데이터를 복사하지 않는 문제 수정</span><span class="sxs-lookup"><span data-stu-id="73f1f-2769">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="73f1f-2770">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="73f1f-2770">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="73f1f-2771">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="73f1f-2771">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="73f1f-2772">특정 위치의 스토리지 리소스 사용을 지원하고 글로벌 스토리지 리소스 사용 가져오기는 더 이상 사용되지 않는다는 경고 메시지를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-2772">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="73f1f-2773">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="73f1f-2773">Get-AzStorageUsage</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="73f1f-2774">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="73f1f-2774">Az.CognitiveServices</span></span>
* <span data-ttu-id="73f1f-2775">기존 계정이 없는 Get-AzCognitiveServicesAccountSkus를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-2775">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="73f1f-2776">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="73f1f-2776">Az.Compute</span></span>
* <span data-ttu-id="73f1f-2777">Get-AzVM -ResourceGroupName <rg>가 필요한 경우 50개가 넘는 결과를 반환하도록 수정</span><span class="sxs-lookup"><span data-stu-id="73f1f-2777">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="73f1f-2778">'SimpleParameterSet' 예제가 New-AzVmss cmdlet 도움말에 추가됨</span><span class="sxs-lookup"><span data-stu-id="73f1f-2778">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="73f1f-2779">Azure Disk Encryption 진행률 메시지의 오타를 수정</span><span class="sxs-lookup"><span data-stu-id="73f1f-2779">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="73f1f-2780">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="73f1f-2780">Az.DataFactoryV2</span></span>
* <span data-ttu-id="73f1f-2781">ADF.Net SDK 버전을 2.3.0으로 업데이트</span><span class="sxs-lookup"><span data-stu-id="73f1f-2781">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="73f1f-2782">Az.Network</span><span class="sxs-lookup"><span data-stu-id="73f1f-2782">Az.Network</span></span>
* <span data-ttu-id="73f1f-2783">NetworkProfile 기능 추가</span><span class="sxs-lookup"><span data-stu-id="73f1f-2783">Added NetworkProfile functionality.</span></span> <span data-ttu-id="73f1f-2784">추가된 새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-2784">new cmdlets added</span></span>
    - <span data-ttu-id="73f1f-2785">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="73f1f-2785">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="73f1f-2786">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="73f1f-2786">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="73f1f-2787">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="73f1f-2787">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="73f1f-2788">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="73f1f-2788">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="73f1f-2789">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="73f1f-2789">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="73f1f-2790">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="73f1f-2790">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="73f1f-2791">서브넷 모델에 서비스 연결 링크 추가</span><span class="sxs-lookup"><span data-stu-id="73f1f-2791">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="73f1f-2792">New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="73f1f-2792">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="73f1f-2793">Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="73f1f-2793">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="73f1f-2794">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="73f1f-2794">Az.RedisCache</span></span>
* <span data-ttu-id="73f1f-2795">모든 문자열을 Size 매개 변수로 진행되도록 허용</span><span class="sxs-lookup"><span data-stu-id="73f1f-2795">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="73f1f-2796">PSArgumentCompleter 팝업에 P5 추가</span><span class="sxs-lookup"><span data-stu-id="73f1f-2796">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="73f1f-2797">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="73f1f-2797">Az.Resources</span></span>
* <span data-ttu-id="73f1f-2798">-Mode 매개 변수를 Set-AzPolicyDefinition에 추가</span><span class="sxs-lookup"><span data-stu-id="73f1f-2798">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="73f1f-2799">사용자가 포함된 Origin 작업에서 Get-AzProviderOperation commandlet 버그 수정</span><span class="sxs-lookup"><span data-stu-id="73f1f-2799">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="73f1f-2800">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="73f1f-2800">Az.Sql</span></span>
* <span data-ttu-id="73f1f-2801">일부 백업 cmdlet이 현재 azure 구독을 인식하지 않는 문제 해결</span><span class="sxs-lookup"><span data-stu-id="73f1f-2801">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="73f1f-2802">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="73f1f-2802">Az.Websites</span></span>
* <span data-ttu-id="73f1f-2803">새 cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - 컨테이너 지속적인 배포 Webhook URL을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-2803">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="73f1f-2804">새 cmdlet New-AzWebAppContainerPSSession 및 Enter-WebAppContainerPSSession -  windows 컨테이너 앱에 PowerShell 원격 세션을 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="73f1f-2804">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="73f1f-2805">0.2.0 - 2018년 9월</span><span class="sxs-lookup"><span data-stu-id="73f1f-2805">0.2.0 - September 2018</span></span>
 <span data-ttu-id="73f1f-2806">초기 릴리스</span><span class="sxs-lookup"><span data-stu-id="73f1f-2806">Initial Release</span></span>
