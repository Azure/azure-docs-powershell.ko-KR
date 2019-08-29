---
ms.openlocfilehash: f89d13d6bbedaea29b62287942d8c7a509abe32b
ms.sourcegitcommit: abca342d8687ca638679c049792d0cef6045837d
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/27/2019
ms.locfileid: "70052637"
---
## <a name="260---august-2019"></a><span data-ttu-id="e94b5-101">2.6.0 - 2019년 8월</span><span class="sxs-lookup"><span data-stu-id="e94b5-101">2.6.0 - August 2019</span></span>
#### <a name="general"></a><span data-ttu-id="e94b5-102">일반</span><span class="sxs-lookup"><span data-stu-id="e94b5-102">General</span></span>
* <span data-ttu-id="e94b5-103">여러 모듈에서 기타 오타가 수정됨</span><span class="sxs-lookup"><span data-stu-id="e94b5-103">Fixed miscellaneous typos across numerous modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="e94b5-104">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e94b5-104">Az.Accounts</span></span>
* <span data-ttu-id="e94b5-105">Azure Functions 인증에서 사용자가 할당한 MSI가 지원됨(# 9479)</span><span class="sxs-lookup"><span data-stu-id="e94b5-105">Support user-assigned MSI in Azure Functiosn Authentication (#9479)</span></span>

#### <a name="azaks"></a><span data-ttu-id="e94b5-106">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="e94b5-106">Az.Aks</span></span>
* <span data-ttu-id="e94b5-107">'Get-AzAks' 출력 관련 문제가 해결됨</span><span class="sxs-lookup"><span data-stu-id="e94b5-107">Fix issue with output for 'Get-AzAks'</span></span>
    * <span data-ttu-id="e94b5-108">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/9847 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="e94b5-108">More information here: https://github.com/Azure/azure-powershell/issues/9847</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="e94b5-109">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="e94b5-109">Az.ApiManagement</span></span>
* <span data-ttu-id="e94b5-110">문제 https://github.com/Azure/azure-powershell/issues/9351 수정</span><span class="sxs-lookup"><span data-stu-id="e94b5-110">Fix for issue https://github.com/Azure/azure-powershell/issues/9351</span></span>
    - <span data-ttu-id="e94b5-111">productId, apiId, groupId 및 userId에 대한 제한을 적용하지 않는 .Net NuGet 버전이 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="e94b5-111">Update .net nuget version, which does not enforce restrictions on productId, apiId, groupId and userId</span></span>
* <span data-ttu-id="e94b5-112">**Get-AzApiManagementProduct** - API를 사용하는 제품에 대한 쿼리 지원이 추가됨</span><span class="sxs-lookup"><span data-stu-id="e94b5-112">**Get-AzApiManagementProduct** - Added support for querying products using Api.</span></span>
  https://github.com/Azure/azure-powershell/issues/9482
* <span data-ttu-id="e94b5-113">**New-AzApiManagementApiRevision** - 새 API 수정(https://github.com/Azure/azure-powershell/issues/9752 )을 만들 때 ApiRevisionDescription이 설정되지 않은 문제가 해결됨</span><span class="sxs-lookup"><span data-stu-id="e94b5-113">**New-AzApiManagementApiRevision** - Fix for issue where ApiRevisionDescription was not being set when creating new api revision https://github.com/Azure/azure-powershell/issues/9752</span></span>
* <span data-ttu-id="e94b5-114">'PsApiManagementOAuth2AuthrozationServer' 모델의 오타가 'PsApiManagementOAuth2AuthorizationServer'로 수정됨</span><span class="sxs-lookup"><span data-stu-id="e94b5-114">Fixed typo in model 'PsApiManagementOAuth2AuthrozationServer' to 'PsApiManagementOAuth2AuthorizationServer'</span></span>

#### <a name="azbatch"></a><span data-ttu-id="e94b5-115">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="e94b5-115">Az.Batch</span></span>
* <span data-ttu-id="e94b5-116">도움말 메시지 및 설명서에서 Windows를 대문자로 시작하도록 오타가 수정됨</span><span class="sxs-lookup"><span data-stu-id="e94b5-116">Fixed typo in help message and documentation to capitalize Windows</span></span>

#### <a name="azcdn"></a><span data-ttu-id="e94b5-117">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="e94b5-117">Az.Cdn</span></span>
* <span data-ttu-id="e94b5-118">CDN 모듈 변환 도우미의 오타가 수정됨</span><span class="sxs-lookup"><span data-stu-id="e94b5-118">Fixed a typo in CDN module conversion helper</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e94b5-119">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e94b5-119">Az.Compute</span></span>
* <span data-ttu-id="e94b5-120">VmssId가 New-AzVMConfig cmdlet에 추가됨</span><span class="sxs-lookup"><span data-stu-id="e94b5-120">Add VmssId to New-AzVMConfig cmdlet</span></span>
* <span data-ttu-id="e94b5-121">TerminateScheduledEvents 및 TerminateScheduledEventNotBeforeTimeoutInMinutes 매개 변수가 New-AzVmssConfig 및 Update-AzVmss에 추가됨</span><span class="sxs-lookup"><span data-stu-id="e94b5-121">Add TerminateScheduledEvents and TerminateScheduledEventNotBeforeTimeoutInMinutes parameters to New-AzVmssConfig and Update-AzVmss</span></span>
* <span data-ttu-id="e94b5-122">HyperVGeneration 속성이 VM 이미지 개체에 추가됨</span><span class="sxs-lookup"><span data-stu-id="e94b5-122">Add HyperVGeneration property to VM image object</span></span>
* <span data-ttu-id="e94b5-123">Host 및 HostGroup 기능이 추가됨</span><span class="sxs-lookup"><span data-stu-id="e94b5-123">Add Host and HostGroup features</span></span>
    - <span data-ttu-id="e94b5-124">새 cmdlet:   New-AzHostGroup, New-AzHost, Get-AzHostGroup, Get-AzHost, Remove-AzHostGroup, Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="e94b5-124">New cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span></span>
    - <span data-ttu-id="e94b5-125">HostId 매개 변수가 New-AzVMConfig 및 New-AzVM 추가됨</span><span class="sxs-lookup"><span data-stu-id="e94b5-125">HostId parameter is added to New-AzVMConfig and New-AzVM</span></span>
* <span data-ttu-id="e94b5-126">'Invoke-AzVMRunCommand' 설명서의 예제에서 올바른 매개 변수 이름을 사용하도록 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="e94b5-126">Update example in 'Invoke-AzVMRunCommand' documentation to use correct parameter name</span></span>
* <span data-ttu-id="e94b5-127">'Set-AzVMDiskEncryptionExtension' 및 'Set-AzVmssDiskEncryptionExtension' 참조 설명서의 '-VolumeType' 설명이 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="e94b5-127">Update '-VolumeType' description in 'Set-AzVMDiskEncryptionExtension' and 'Set-AzVmssDiskEncryptionExtension' reference documentation</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="e94b5-128">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="e94b5-128">Az.DataFactory</span></span>
* <span data-ttu-id="e94b5-129">'New-AzDataFactoryEncryptValue' 설명서에서 'Windows'를 대문자로 시작하도록 오타가 수정됨</span><span class="sxs-lookup"><span data-stu-id="e94b5-129">Fix typo to capitalize 'Windows' in 'New-AzDataFactoryEncryptValue' documentation</span></span>
* <span data-ttu-id="e94b5-130">ADF .Net SDK 버전이 4.1.2로 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="e94b5-130">Updated ADF .Net SDK version to 4.1.2</span></span>
* <span data-ttu-id="e94b5-131">자체 호스팅 통합 런타임을 SSIS Integration Runtime의 프록시로 설정할 수 있도록 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' 및 'DataProxyStagingPath' 매개 변수가 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd에 추가됨</span><span class="sxs-lookup"><span data-stu-id="e94b5-131">Add parameter 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' and 'DataProxyStagingPath' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable set up Self-Hosted Integration Runtime as a proxy for SSIS Integration Runtime</span></span>
* <span data-ttu-id="e94b5-132">PSTriggerRun에서 트리거된 파이프라인, 메시지 및 속성을 표시하고, PSActivityRun에서 작업 유형을 표시하도록 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="e94b5-132">Updated PSTriggerRun to show the triggered pipelines, message and properties, and PSActivityRun to show the activity type</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="e94b5-133">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="e94b5-133">Az.DataLakeStore</span></span>
* <span data-ttu-id="e94b5-134">오류 또는 원격 예외에 대한 Get-DataLakeStoreDeletedItem 중단이 수정됨</span><span class="sxs-lookup"><span data-stu-id="e94b5-134">Fix hanging of Get-DataLakeStoreDeletedItem for any errors or remote exceptions.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="e94b5-135">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="e94b5-135">Az.EventHub</span></span>
* <span data-ttu-id="e94b5-136">#9658 문제 해결: Set-AzEventHubNetworkRuleSet의 VirtualNteworkRule 매개 변수에 대한 오타</span><span class="sxs-lookup"><span data-stu-id="e94b5-136">Fix for issue #9658 : Typo VirtualNteworkRule parameter in Set-AzEventHubNetworkRuleSet</span></span>
* <span data-ttu-id="e94b5-137">#9558 문제 해결: Set-AzEventHubNamespace에서 PUT 대신 PATCH가 사용됨</span><span class="sxs-lookup"><span data-stu-id="e94b5-137">Fix for issue #9558 : Set-AzEventHubNamespace is using PATCH instead of PUT</span></span>
* <span data-ttu-id="e94b5-138">EnableKafka 매개 변수가 Set-AzEventHubNamespace cmdlet에 추가됨</span><span class="sxs-lookup"><span data-stu-id="e94b5-138">added EnableKafka parameter to Set-AzEventHubNamespace cmdlet</span></span>
* <span data-ttu-id="e94b5-139">#9786 문제 해결: Listen(수신 대기) 전용 권한이 있는 규칙을 만들 수 없음</span><span class="sxs-lookup"><span data-stu-id="e94b5-139">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>

#### <a name="azmarketplaceordering"></a><span data-ttu-id="e94b5-140">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="e94b5-140">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="e94b5-141">'Azure'가 모두 소문자인 설명서의 오타가 수정됨</span><span class="sxs-lookup"><span data-stu-id="e94b5-141">Fixed documentation typo where 'Azure' was all lowercase letters</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="e94b5-142">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="e94b5-142">Az.Monitor</span></span>
* <span data-ttu-id="e94b5-143">도움말 설명서에서 잘못된 매개 변수 이름이 수정됨</span><span class="sxs-lookup"><span data-stu-id="e94b5-143">Fixed incorrect parameter name in help documentation</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e94b5-144">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e94b5-144">Az.Network</span></span>
* <span data-ttu-id="e94b5-145">New-AzPrivateLinkServiceIpConfig가 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="e94b5-145">Updated New-AzPrivateLinkServiceIpConfig</span></span>
    - <span data-ttu-id="e94b5-146">서버 쪽에서 사용되지 않으므로 'PublicIpAddress' 매개 변수가 사용되지 않음</span><span class="sxs-lookup"><span data-stu-id="e94b5-146">Deprecated the paramster 'PublicIpAddress' since this is never used in the server side.</span></span>
    - <span data-ttu-id="e94b5-147">현재 IP 구성이 기본 구성인지 여부를 나타내는 하나의 선택적 'Primary' 매개 변수가 추가됨</span><span class="sxs-lookup"><span data-stu-id="e94b5-147">Added one optional parameter 'Primary' that indicate the current ip configuration is primary one or not.</span></span>
* <span data-ttu-id="e94b5-148">SDK의 요청 오류 예외 처리가 향상됨 - 이전의 SDK 예외가 올바르게 처리되지 않아 주요 오류 세부 정보가 표시되지 않은 문제가 해결됨</span><span class="sxs-lookup"><span data-stu-id="e94b5-148">Improved handling of request error exception from SDK   -Fixes the issue that previously SDK exceptions aren't handled correctly which results in key error details not being displayed</span></span>
* <span data-ttu-id="e94b5-149">올바른 IPv6 접두사 길이를 확인하기 위해 Ipv6 IP 접두사에 대한 유효성 검사 논리가 조정됨</span><span class="sxs-lookup"><span data-stu-id="e94b5-149">Adjusted validation logic for Ipv6 IP Prefix to check for correct IPv6 prefix length.</span></span> 
* <span data-ttu-id="e94b5-150">Get-AzVirtualNetworkSubnetConfig가 업데이트됨: 서브넷 리소스 ID별로 가져오도록 설정되는 매개 변수 세트가 추가됨</span><span class="sxs-lookup"><span data-stu-id="e94b5-150">Updated Get-AzVirtualNetworkSubnetConfig: Added parameter set to get by subnet resource id.</span></span>
* <span data-ttu-id="e94b5-151">AzNetworkServiceTag의 Location(위치) 매개 변수에 대한 설명이 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="e94b5-151">Updated description of Location parameter for AzNetworkServiceTag</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="e94b5-152">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="e94b5-152">Az.OperationalInsights</span></span>
* <span data-ttu-id="e94b5-153">'New-AzOperationalInsightsLinuxSyslogDataSource'에 대한 설명서가 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="e94b5-153">Updated documentation for 'New-AzOperationalInsightsLinuxSyslogDataSource'</span></span>
    - <span data-ttu-id="e94b5-154">예제가 추가됨</span><span class="sxs-lookup"><span data-stu-id="e94b5-154">Added example</span></span>
    - <span data-ttu-id="e94b5-155">'-Name' 매개 변수에 대한 설명이 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="e94b5-155">Updated description for '-Name' parameter</span></span>
* <span data-ttu-id="e94b5-156">New-AzOperationalInsightsWindowsEventDataSource에 대한 예제가 추가됨</span><span class="sxs-lookup"><span data-stu-id="e94b5-156">Added an example for New-AzOperationalInsightsWindowsEventDataSource</span></span>
* <span data-ttu-id="e94b5-157">New-AzOperationalInsightsWindowsEventDataSource의 -Name 매개 변수에 대한 설명이 변경됨</span><span class="sxs-lookup"><span data-stu-id="e94b5-157">Changed the description of the -Name parameter for New-AzOperationalInsightsWindowsEventDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="e94b5-158">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="e94b5-158">Az.RecoveryServices</span></span>
* <span data-ttu-id="e94b5-159">'Get-AzRecoveryServicesBackupJobDetail.md'가 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="e94b5-159">Update 'Get-AzRecoveryServicesBackupJobDetail.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="e94b5-160">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e94b5-160">Az.Resources</span></span>
* <span data-ttu-id="e94b5-161">Microsoft 리소스에 대한 새 2019-05-10 API 버전 지원이 추가됨</span><span class="sxs-lookup"><span data-stu-id="e94b5-161">Add support for new api version 2019-05-10 for Microsoft.Resource</span></span>
    - <span data-ttu-id="e94b5-162">변수, 리소스 및 속성에 대한 'copy.count = 0' 지원이 추가됨</span><span class="sxs-lookup"><span data-stu-id="e94b5-162">Add support for 'copy.count = 0' for variables, resources and properties</span></span>
    - <span data-ttu-id="e94b5-163">'condition = false' 또는 'copy.count = 0'인 리소스가 완료 모드에서 삭제됨</span><span class="sxs-lookup"><span data-stu-id="e94b5-163">Resources with 'condition = false' or 'copy.count = 0' will be deleted in complete mode</span></span>
* <span data-ttu-id="e94b5-164">정책을 구독 수준에서 도움말 문서에 할당하는 예제가 추가됨</span><span class="sxs-lookup"><span data-stu-id="e94b5-164">Add an example of assigning policy at subscription level to help doc</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="e94b5-165">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="e94b5-165">Az.ServiceBus</span></span>
* <span data-ttu-id="e94b5-166">#9658 문제 해결: Set-AzServiceBusNetworkRuleSet의 VirtualNetworkRule 매개 변수에 대한 오타</span><span class="sxs-lookup"><span data-stu-id="e94b5-166">Fix for issue #9658 : Typo VirtualNetworkRule parameter in Set-AzServiceBusNetworkRuleSet</span></span>
* <span data-ttu-id="e94b5-167">#9786 문제 해결: Listen(수신 대기) 전용 권한이 있는 규칙을 만들 수 없음</span><span class="sxs-lookup"><span data-stu-id="e94b5-167">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>
* <span data-ttu-id="e94b5-168">큐 및 토픽에 대한 이름 가용성을 확인하는 새 'Test-AzServiceBusNameAvailability' 명령이 추가됨</span><span class="sxs-lookup"><span data-stu-id="e94b5-168">Added new command 'Test-AzServiceBusNameAvailability' to check the name availability for queue and topic</span></span> 

#### <a name="azservicefabric"></a><span data-ttu-id="e94b5-169">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="e94b5-169">Az.ServiceFabric</span></span>
* <span data-ttu-id="e94b5-170">노드 유형 추가 cmdlet 버그 수정:</span><span class="sxs-lookup"><span data-stu-id="e94b5-170">Fix add node type cmdlet bugs:</span></span>
    - <span data-ttu-id="e94b5-171">서비스 패브릭 클러스터와 관련이 없는 다른 vmss가 리소스 그룹에 있을 때 발생하는 NullReferenceException 버그</span><span class="sxs-lookup"><span data-stu-id="e94b5-171">NullReferenceException bug when resource group had other vmss not related to the service fabric cluster.</span></span> <span data-ttu-id="e94b5-172">문제 해결: https://github.com/Azure/azure-powershell/issues/8681</span><span class="sxs-lookup"><span data-stu-id="e94b5-172">Fixes issue: https://github.com/Azure/azure-powershell/issues/8681</span></span>
    - <span data-ttu-id="e94b5-173">virtualNetwork가 클러스터의 다른 리소스 그룹에 있을 때 cmdlet이 실패하는 버그가 수정됨</span><span class="sxs-lookup"><span data-stu-id="e94b5-173">Fix bug where cmdlet failed if virtualNetwork was in a different resource group that the cluster.</span></span> <span data-ttu-id="e94b5-174">문제 해결: https://github.com/Azure/azure-powershell/issues/8407</span><span class="sxs-lookup"><span data-stu-id="e94b5-174">fixes issue: https://github.com/Azure/azure-powershell/issues/8407</span></span>
    - <span data-ttu-id="e94b5-175">Add-AzServiceFabricApplicationCertificate cmdlet이 사용되지 않음</span><span class="sxs-lookup"><span data-stu-id="e94b5-175">Deprecating Add-AzServiceFabricApplicationCertificate cmdlet</span></span>

#### <a name="azsql"></a><span data-ttu-id="e94b5-176">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e94b5-176">Az.Sql</span></span>
* <span data-ttu-id="e94b5-177">이전의 Auditing(감사) cmdlet에 대한 설명서가 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="e94b5-177">Update documentation of old Auditing cmdlets.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="e94b5-178">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="e94b5-178">Az.Storage</span></span>
* <span data-ttu-id="e94b5-179">더 많은 시나리오를 cmdlet 예제에 추가하고 매개 변수 설명을 업데이트하여 Get/Close-AzStorageFileHandle에 대한 도움말이 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="e94b5-179">Update help for Get/Close-AzStorageFileHandle, by add more scenarios to cmdlet examples and update parameter descriptions</span></span>
* <span data-ttu-id="e94b5-180">Blob 업로드 및 Blob 복사에서 StandardBlobTier가 지원됨</span><span class="sxs-lookup"><span data-stu-id="e94b5-180">Support StandardBlobTier in upload blob and copy blob</span></span>
    -  <span data-ttu-id="e94b5-181">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="e94b5-181">Set-AzStorageBlobContent</span></span>
    -  <span data-ttu-id="e94b5-182">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="e94b5-182">Start-AzStorageBlobCopy</span></span>
* <span data-ttu-id="e94b5-183">Blob 복사에서 우선 순위 리하이드레이션이 지원됨</span><span class="sxs-lookup"><span data-stu-id="e94b5-183">Support Rehydrate Priority in copy blob</span></span>
    -  <span data-ttu-id="e94b5-184">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="e94b5-184">Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="e94b5-185">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="e94b5-185">Az.Websites</span></span>
* <span data-ttu-id="e94b5-186">Set-AzWebApp 및 Set-AzWebAppSlot에서 -AppSettings 매개 변수에 대한 설명이 추가됨</span><span class="sxs-lookup"><span data-stu-id="e94b5-186">Add clarification around -AppSettings parameter in Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <a name="250---july-2019"></a><span data-ttu-id="e94b5-187">2.5.0 - 2019년 7월</span><span class="sxs-lookup"><span data-stu-id="e94b5-187">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="e94b5-188">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e94b5-188">Az.Accounts</span></span>
* <span data-ttu-id="e94b5-189">ClientRuntime의 최신 버전을 사용하도록 일반적인 코드를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-189">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="e94b5-190">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="e94b5-190">Az.ApplicationInsights</span></span>
* <span data-ttu-id="e94b5-191">'Remove-AzApplicationInsightsApiKey' 설명서의 예제 오타 수정</span><span class="sxs-lookup"><span data-stu-id="e94b5-191">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span> 

#### <a name="azautomation"></a><span data-ttu-id="e94b5-192">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="e94b5-192">Az.Automation</span></span>
* <span data-ttu-id="e94b5-193">리소스 문자열의 오타 수정</span><span class="sxs-lookup"><span data-stu-id="e94b5-193">Fix typo in resource string</span></span> 

#### <a name="azcognitiveservices"></a><span data-ttu-id="e94b5-194">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="e94b5-194">Az.CognitiveServices</span></span>
* <span data-ttu-id="e94b5-195">NetworkRuleSet 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-195">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e94b5-196">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e94b5-196">Az.Compute</span></span>
* <span data-ttu-id="e94b5-197">VM 인스턴스 보기 개체의 누락된 속성(ComputerName, OsName, OsVersion 및 HyperVGeneration)을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-197">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="e94b5-198">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="e94b5-198">Az.ContainerRegistry</span></span>
* <span data-ttu-id="e94b5-199">복제 매개 변수의 Remove-AzContainerRegistryReplication에서 오타 수정</span><span class="sxs-lookup"><span data-stu-id="e94b5-199">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="e94b5-200">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/9633 을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="e94b5-200">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="e94b5-201">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="e94b5-201">Az.DataFactory</span></span>
* <span data-ttu-id="e94b5-202">ADF .Net SDK 버전을 4.1.0으로 업데이트</span><span class="sxs-lookup"><span data-stu-id="e94b5-202">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="e94b5-203">'Get-AzDataFactoryV2PipelineRun' 설명서의 오타 수정</span><span class="sxs-lookup"><span data-stu-id="e94b5-203">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="e94b5-204">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="e94b5-204">Az.EventHub</span></span>
* <span data-ttu-id="e94b5-205">SAS 토큰을 생성하기 위해 추가된 새로운 cmmdlet 추가: New-AzEventHubAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="e94b5-205">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="e94b5-206">'관리'만 지정된 경우 authorizationrules 권한에 대한 확인 및 오류 메시지 추가</span><span class="sxs-lookup"><span data-stu-id="e94b5-206">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="e94b5-207">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="e94b5-207">Az.KeyVault</span></span>
* <span data-ttu-id="e94b5-208">인증서 정책에 대한 KeySize 지정을 위한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="e94b5-208">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="e94b5-209">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="e94b5-209">Az.LogicApp</span></span>
* <span data-ttu-id="e94b5-210">모든 맵 유형을 나열하도록 Get-AzIntegrationAccountMap 수정</span><span class="sxs-lookup"><span data-stu-id="e94b5-210">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="e94b5-211">필터링을 위해 새 MapType 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="e94b5-211">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="e94b5-212">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="e94b5-212">Az.ManagedServices</span></span>
* <span data-ttu-id="e94b5-213">API 버전 2019-06-01(GA)에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="e94b5-213">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e94b5-214">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e94b5-214">Az.Network</span></span>
* <span data-ttu-id="e94b5-215">프라이빗 엔드포인트 및 프라이빗 링크 서비스에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="e94b5-215">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="e94b5-216">새 cmdlet</span><span class="sxs-lookup"><span data-stu-id="e94b5-216">New cmdlets</span></span>
        - <span data-ttu-id="e94b5-217">Set-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="e94b5-217">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="e94b5-218">Set-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="e94b5-218">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="e94b5-219">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="e94b5-219">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="e94b5-220">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="e94b5-220">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="e94b5-221">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="e94b5-221">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="e94b5-222">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="e94b5-222">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="e94b5-223">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="e94b5-223">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="e94b5-224">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="e94b5-224">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="e94b5-225">기능에 대한 새로운 명령이 업데이트됨: Virtualnetwork의 서브넷에 있는 PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies 플래그</span><span class="sxs-lookup"><span data-stu-id="e94b5-225">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="e94b5-226">업데이트된 New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="e94b5-226">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="e94b5-227">이 서브넷의 프라이빗 엔드포인트에 네트워크 정책을 적용하는지 적용하지 않는지 나타내는 선택적 매개 변수 -PrivateEndpointNetworkPoliciesFlag를 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-227">Added optional parameter -PrivateEndpointNetworkPoliciesFlag to indicate that enable or disable apply network policies on pivate endpoint in this subnet.</span></span>
        - <span data-ttu-id="e94b5-228">이 서브넷의 프라이빗 링크 서비스에 네트워크 정책을 적용하는지 적용하지 않는지 나타내는 선택적 매개 변수 -PrivateLinkServiceNetworkPoliciesFlag를 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-228">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag to indicate that enable or disable apply network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="e94b5-229">AzPrivateLinkService의 cmdlet 매개 변수 'ServiceName'이 이전 버전과의 호환성을 위해 별칭 'ServiceName'을 사용한 'Name'으로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-229">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="e94b5-230">네트워크 보안 규칙 구성에 ICMP 프로토콜 사용</span><span class="sxs-lookup"><span data-stu-id="e94b5-230">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="e94b5-231">다음 Cmdlet이 업데이트 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-231">Updated cmdlets</span></span>
        - <span data-ttu-id="e94b5-232">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e94b5-232">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="e94b5-233">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e94b5-233">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="e94b5-234">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e94b5-234">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="e94b5-235">New-AzVirtualNetworkGatewayConnection에 대한 구성 가능한 매개 변수로 ConnectionProtocolType (Ikev1/Ikev2) 추가</span><span class="sxs-lookup"><span data-stu-id="e94b5-235">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="e94b5-236">LoadBalancerFrontendIpConfiguration에 PrivateIpAddressVersion 추가</span><span class="sxs-lookup"><span data-stu-id="e94b5-236">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="e94b5-237">업데이트된 cmdlet:</span><span class="sxs-lookup"><span data-stu-id="e94b5-237">Updated cmdlet:</span></span>
        - <span data-ttu-id="e94b5-238">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="e94b5-238">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="e94b5-239">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="e94b5-239">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="e94b5-240">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="e94b5-240">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="e94b5-241">프로브에서 사용자 지정 포트를 지원하기 위한 Application Gateway New-AzApplicationGatewayProbeConfig 명령 업데이트</span><span class="sxs-lookup"><span data-stu-id="e94b5-241">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="e94b5-242">업데이트된 New-AzApplicationGatewayProbeConfig: 백 엔드 서버 검색에 사용되는 선택적 매개 변수 포트가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-242">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="e94b5-243">이 매개 변수는 Standard_V2 및 WAF_V2 SKU에 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-243">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="e94b5-244">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="e94b5-244">Az.OperationalInsights</span></span>
* <span data-ttu-id="e94b5-245">저장된 검색의 기본 버전이 1로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-245">Updated default version for saved searches to be 1.</span></span> 
* <span data-ttu-id="e94b5-246">사용자 지정 로그 null regex 처리가 수정됨</span><span class="sxs-lookup"><span data-stu-id="e94b5-246">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="e94b5-247">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="e94b5-247">Az.RecoveryServices</span></span>
* <span data-ttu-id="e94b5-248">'Get-AzRecoveryServicesBackupJob.md' 업데이트</span><span class="sxs-lookup"><span data-stu-id="e94b5-248">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="e94b5-249">'Get-AzRecoveryServicesBackupContainer.md' 업데이트</span><span class="sxs-lookup"><span data-stu-id="e94b5-249">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="e94b5-250">'Get-AzRecoveryServicesVault.md' 업데이트</span><span class="sxs-lookup"><span data-stu-id="e94b5-250">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="e94b5-251">'Wait-AzRecoveryServicesBackupJob.md' 업데이트</span><span class="sxs-lookup"><span data-stu-id="e94b5-251">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="e94b5-252">'Set-AzRecoveryServicesVaultContext.md' 업데이트</span><span class="sxs-lookup"><span data-stu-id="e94b5-252">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="e94b5-253">'Get-AzRecoveryServicesBackupItem.md' 업데이트</span><span class="sxs-lookup"><span data-stu-id="e94b5-253">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="e94b5-254">'Get-AzRecoveryServicesBackupRecoveryPoint.md' 업데이트</span><span class="sxs-lookup"><span data-stu-id="e94b5-254">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="e94b5-255">'Restore-AzRecoveryServicesBackupItem.md' 업데이트</span><span class="sxs-lookup"><span data-stu-id="e94b5-255">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="e94b5-256">Azure 파일 공유용 컨테이너를 등록 취소하기 위해 서비스 요청 업데이트</span><span class="sxs-lookup"><span data-stu-id="e94b5-256">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="e94b5-257">'Set-AzRecoveryServicesAsrAlertSetting.md' 업데이트</span><span class="sxs-lookup"><span data-stu-id="e94b5-257">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="e94b5-258">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e94b5-258">Az.Resources</span></span>
- <span data-ttu-id="e94b5-259">'New-AzResourceGroupDeployment' 설명서에서 참조된 누락 cmdlet 제거</span><span class="sxs-lookup"><span data-stu-id="e94b5-259">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="e94b5-260">새 API 버전 2019-01-01을 사용하도록 정책 cmdlet 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="e94b5-260">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="e94b5-261">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="e94b5-261">Az.ServiceBus</span></span>
* <span data-ttu-id="e94b5-262">SAS 토큰을 생성하기 위해 추가된 새로운 cmmdlet 추가: New-AzServiceBusAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="e94b5-262">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="e94b5-263">'관리'만 지정된 경우 authorizationrules 권한에 대한 확인 및 오류 메시지 추가</span><span class="sxs-lookup"><span data-stu-id="e94b5-263">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="e94b5-264">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e94b5-264">Az.Sql</span></span>
* <span data-ttu-id="e94b5-265">Set-AzSqlDatabaseSecondary cmdlet에 대한 누락된 예제 수정</span><span class="sxs-lookup"><span data-stu-id="e94b5-265">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="e94b5-266">이메일 주소를 제공하지 않고 설정된 취약성 평가 반복 검색 수정</span><span class="sxs-lookup"><span data-stu-id="e94b5-266">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="e94b5-267">경고 메시지의 작은 오타를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-267">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="e94b5-268">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="e94b5-268">Az.Storage</span></span>
* <span data-ttu-id="e94b5-269">'Get-AzStorageAccount'에 대한 참조 설명서의 예제를 업데이트하여 올바른 매개 변수 이름 사용</span><span class="sxs-lookup"><span data-stu-id="e94b5-269">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="e94b5-270">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="e94b5-270">Az.StorageSync</span></span>
* <span data-ttu-id="e94b5-271">Invoke-AzStorageSyncChangeDetection cmdlet을 추가하는 중입니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-271">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="e94b5-272">TierFilesOlderThanDays를 기념하는 문제 9551 수정</span><span class="sxs-lookup"><span data-stu-id="e94b5-272">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="e94b5-273">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="e94b5-273">Az.Websites</span></span>
* <span data-ttu-id="e94b5-274">Get-AzWebApp 및 Set-AzWebApp에서 일부 SiteConfig 속성을 반환하지 않은 버그 수정</span><span class="sxs-lookup"><span data-stu-id="e94b5-274">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="e94b5-275">Get-AzDeletedWebApp 및 Restore-AzDeletedWebApp에 새 위치 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="e94b5-275">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="e94b5-276">AzWebApp-IncludeSourceWebAppSlots을 사용하여 웹앱 슬롯을 복제하는 버그를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-276">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="e94b5-277">2.4.0 - 2019년 7월</span><span class="sxs-lookup"><span data-stu-id="e94b5-277">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="e94b5-278">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e94b5-278">Az.Accounts</span></span>
* <span data-ttu-id="e94b5-279">프로필 cmdlet에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="e94b5-279">Add support for profile cmdlets</span></span>
* <span data-ttu-id="e94b5-280">생성된 cmdlet에서 환경 및 데이터 평면에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="e94b5-280">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="e94b5-281">Windows PowerShell의 데이터 평면 cmdlet에대해 일부 경우 잘못된 엔드포인트가 사용되는 버그 수정</span><span class="sxs-lookup"><span data-stu-id="e94b5-281">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="e94b5-282">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="e94b5-282">Az.Advisor</span></span>
* <span data-ttu-id="e94b5-283">Az.Advisor의 GA 릴리스</span><span class="sxs-lookup"><span data-stu-id="e94b5-283">GA release of Az.Advisor</span></span>
* <span data-ttu-id="e94b5-284">이 모듈은 이제 롤업 `Az` 모듈의 일부로 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-284">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="e94b5-285">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="e94b5-285">Az.ApiManagement</span></span>
* <span data-ttu-id="e94b5-286">문제 https://github.com/Azure/azure-powershell/issues/8671 수정</span><span class="sxs-lookup"><span data-stu-id="e94b5-286">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="e94b5-287">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="e94b5-287">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="e94b5-288">사용자 및 제품별 구독을 쿼리하기 위한 지원이 추가됨</span><span class="sxs-lookup"><span data-stu-id="e94b5-288">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="e94b5-289">범위 '/', '/ api, '/ api/echo api'를 사용하여 쿼리하기 위한 지원이 추가됨</span><span class="sxs-lookup"><span data-stu-id="e94b5-289">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="e94b5-290">[https://github.com/Azure/azure-powershell/issues/9307](https://github.com/Azure/azure-powershell/issues/9307 ) 및 https://github.com/Azure/azure-powershell/issues/8432 문제 수정</span><span class="sxs-lookup"><span data-stu-id="e94b5-290">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="e94b5-291">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="e94b5-291">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="e94b5-292">Apis를 가져올 때 'ApiVersion' 및 'ApiVersionSetId'를 지정하기 위한 지원이 추가됨</span><span class="sxs-lookup"><span data-stu-id="e94b5-292">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="e94b5-293">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="e94b5-293">Az.Automation</span></span>
* <span data-ttu-id="e94b5-294">문자열 값을 처리하기 위해 Set-AzAutomationConnectionFieldValue cmdlet 버그를 수정했습니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-294">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e94b5-295">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e94b5-295">Az.Compute</span></span>
* <span data-ttu-id="e94b5-296">New-AzImageConfig에 HyperVGeneration 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="e94b5-296">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="e94b5-297">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="e94b5-297">Az.DataFactory</span></span>
* <span data-ttu-id="e94b5-298">get activity runs, get pipeline runs, get trigger runs ADF cmdlet의 출력을 업데이트하여 Select-Object pipe를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-298">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="e94b5-299">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="e94b5-299">Az.EventGrid</span></span>
* <span data-ttu-id="e94b5-300">'New-AzEventGridSubcription' 설명서의 오타 수정</span><span class="sxs-lookup"><span data-stu-id="e94b5-300">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="e94b5-301">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="e94b5-301">Az.IotHub</span></span>
* <span data-ttu-id="e94b5-302">권한 부여 정책 키를 다시 생성하기 위한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="e94b5-302">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e94b5-303">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e94b5-303">Az.Network</span></span>
* <span data-ttu-id="e94b5-304">'RoutingPreference'를 공용 IP 태그에 추가함</span><span class="sxs-lookup"><span data-stu-id="e94b5-304">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="e94b5-305">'Get-AzNetworkServiceTag' 참조 설명서의 예제 개선</span><span class="sxs-lookup"><span data-stu-id="e94b5-305">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="e94b5-306">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="e94b5-306">Az.PolicyInsights</span></span>
* <span data-ttu-id="e94b5-307">Get-AzPolicyState의 null 참조 문제 해결</span><span class="sxs-lookup"><span data-stu-id="e94b5-307">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="e94b5-308">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/9446 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="e94b5-308">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="e94b5-309">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="e94b5-309">Az.OperationalInsights</span></span>
* <span data-ttu-id="e94b5-310">Get-AzOperationalInsightsDataSource에 반환된 CustomLog datasource 모델 수정됨</span><span class="sxs-lookup"><span data-stu-id="e94b5-310">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="e94b5-311">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="e94b5-311">Az.RecoveryServices</span></span>
* <span data-ttu-id="e94b5-312">IaaSVMs에 대한 get-policy 명령 수정</span><span class="sxs-lookup"><span data-stu-id="e94b5-312">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="e94b5-313">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e94b5-313">Az.Resources</span></span>
    - <span data-ttu-id="e94b5-314">Get-AzPolicyState -Top 매개 변수에 대한 도움말 텍스트 수정</span><span class="sxs-lookup"><span data-stu-id="e94b5-314">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="e94b5-315">Get-AzPolicyAlias에 대한 클라이언트 쪽 페이징 지원 추가</span><span class="sxs-lookup"><span data-stu-id="e94b5-315">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="e94b5-316">Set-AzPolicyAssignment, -PolicyParameters 및 -PolicyParametersObject에 대한 새 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="e94b5-316">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="e94b5-317">Policy cmdlet에 대한 몇 가지 문서 및 예제 업데이트</span><span class="sxs-lookup"><span data-stu-id="e94b5-317">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="e94b5-318">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="e94b5-318">Az.ServiceBus</span></span>
* <span data-ttu-id="e94b5-319">문제 #4938 수정 - MaxSizeInMegabytes를 설정할 때 New-AzureRmServiceBusQueue가 BadRequest 반환</span><span class="sxs-lookup"><span data-stu-id="e94b5-319">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="e94b5-320">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e94b5-320">Az.Sql</span></span>
* <span data-ttu-id="e94b5-321">미리 보기 릴리스에서 공개 릴리스로 인스턴스 장애 조치(Failover) 그룹 cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="e94b5-321">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="e94b5-322">새 cmdlet으로 Azure SQL Server\Database Auditing을 지원하세요.</span><span class="sxs-lookup"><span data-stu-id="e94b5-322">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="e94b5-323">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="e94b5-323">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="e94b5-324">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="e94b5-324">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="e94b5-325">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="e94b5-325">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="e94b5-326">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="e94b5-326">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="e94b5-327">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="e94b5-327">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="e94b5-328">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="e94b5-328">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="e94b5-329">취약성 평가 설정에서 이메일 제약 조건 제거</span><span class="sxs-lookup"><span data-stu-id="e94b5-329">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="e94b5-330">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="e94b5-330">Az.Storage</span></span>
* <span data-ttu-id="e94b5-331">다음 cmdlet에서 2개의 매개 변수 '-IndexDocument' 및 '-ErrorDocument404Path'를 필수에서 선택으로 변경하세요.</span><span class="sxs-lookup"><span data-stu-id="e94b5-331">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="e94b5-332">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="e94b5-332">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="e94b5-333">예제를 추가하여 Get-AzStorageBlobContent의 도움말 업데이트</span><span class="sxs-lookup"><span data-stu-id="e94b5-333">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="e94b5-334">StorageException으로 cmdlet이 실패한 경우 자세한 오류 정보 표시</span><span class="sxs-lookup"><span data-stu-id="e94b5-334">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="e94b5-335">Azure Files AAD DS 인증으로 스토리지 계정 생성 또는 업데이트 지원</span><span class="sxs-lookup"><span data-stu-id="e94b5-335">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="e94b5-336">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="e94b5-336">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="e94b5-337">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="e94b5-337">Set-AzStorageAccount</span></span>
* <span data-ttu-id="e94b5-338">파일 공유, 파일 디렉터리 또는 파일의 목록 지원 또는 파일 핸들 닫기</span><span class="sxs-lookup"><span data-stu-id="e94b5-338">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="e94b5-339">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="e94b5-339">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="e94b5-340">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="e94b5-340">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="e94b5-341">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="e94b5-341">Az.StorageSync</span></span>
* <span data-ttu-id="e94b5-342">이 모듈은 이제 롤업 `Az` 모듈의 일부로 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-342">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="e94b5-343">2.3.2 - 2019년 6월</span><span class="sxs-lookup"><span data-stu-id="e94b5-343">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="e94b5-344">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e94b5-344">Az.Accounts</span></span>
* <span data-ttu-id="e94b5-345">함수 호출에 대해 일부 경우 잘못된 URL이 사용되는 버그 수정</span><span class="sxs-lookup"><span data-stu-id="e94b5-345">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="e94b5-346">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/8983 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="e94b5-346">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="e94b5-347">AzureRM에서 Az cmdlet으로의 별칭 문제 해결</span><span class="sxs-lookup"><span data-stu-id="e94b5-347">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="e94b5-348">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="e94b5-348">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="e94b5-349">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="e94b5-349">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e94b5-350">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e94b5-350">Az.Compute</span></span>
* <span data-ttu-id="e94b5-351">New-AzVm 및 New-AzVmss 단순 매개 변수 집합은 이제 'ProximityPlacementGroup'매개 변수를 허용합니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-351">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="e94b5-352">'New-AzVM' 참조 설명서에서 오타 수정</span><span class="sxs-lookup"><span data-stu-id="e94b5-352">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="e94b5-353">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="e94b5-353">Az.Dns</span></span>
* <span data-ttu-id="e94b5-354">'Set-AzDnsZone' 도움말 예제의 오타가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-354">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="e94b5-355">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="e94b5-355">Az.EventGrid</span></span>
* <span data-ttu-id="e94b5-356">2019-06-01 API 버전을 사용하도록 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-356">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="e94b5-357">새 cmdlet:</span><span class="sxs-lookup"><span data-stu-id="e94b5-357">New cmdlets:</span></span>
    - <span data-ttu-id="e94b5-358">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="e94b5-358">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="e94b5-359">새 Azure Event Grid 도메인을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-359">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="e94b5-360">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="e94b5-360">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="e94b5-361">Event Grid 도메인의 세부 정보를 가져오거나 현재 Azure 구독의 모든 Event Grid 도메인 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-361">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="e94b5-362">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="e94b5-362">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="e94b5-363">Azure Event Grid 도메인을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-363">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="e94b5-364">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="e94b5-364">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="e94b5-365">Azure Event Grid 도메인에 대한 공유 액세스 키를 다시 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-365">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="e94b5-366">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="e94b5-366">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="e94b5-367">Event Grid 도메인 이벤트를 게시하는 데 사용되는 공유 액세스 키를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-367">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="e94b5-368">New-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="e94b5-368">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="e94b5-369">새 Azure Event Grid 도메인 토픽을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-369">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="e94b5-370">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="e94b5-370">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="e94b5-371">Event Grid 도메인 토픽의 세부 사항을 가져오거나, 현재 Azure의 특정 Event Grid 도메인 아래의 모든 Event Grid 도메인 토픽 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-371">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span> 
    - <span data-ttu-id="e94b5-372">Remove-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="e94b5-372">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="e94b5-373">기존 Azure Event Grid 도메인 토픽을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-373">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="e94b5-374">다음 Cmdlet이 업데이트 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-374">Updated cmdlets:</span></span>
    - <span data-ttu-id="e94b5-375">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="e94b5-375">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="e94b5-376">새로운 Event Grid 도메인 및 Event Grid 도메인 토픽에 대한 파이핑을 지원하기 위해 새로운 필수 매개 변수를 추가하여 이러한 리소스 아래에 새 이벤트 구독을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-376">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="e94b5-377">새로운 Event Grid 도메인 이름 및 Event Grid 도메인 토픽 이름을 지정하기 위해 새로운 필수 매개 변수를 추가하여 이러한 리소스 아래에 새 이벤트 구독을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-377">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="e94b5-378">기존 매개 변수(예: EndPointType, SubjectBeginsWith 등)를 재사용할 수 있도록 도메인 및 도메인 토픽에 대한 새로운 매개 변수 집합을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-378">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="e94b5-379">지정을 위한 새로운 선택적 매개 변수를 추가</span><span class="sxs-lookup"><span data-stu-id="e94b5-379">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="e94b5-380">이벤트 구독 만료 날짜,</span><span class="sxs-lookup"><span data-stu-id="e94b5-380">Event subscription expiration date,</span></span>
            - <span data-ttu-id="e94b5-381">고급 필터링 매개 변수.</span><span class="sxs-lookup"><span data-stu-id="e94b5-381">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="e94b5-382">대상으로 servicebusqueue에 대한 새 열거형을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-382">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="e94b5-383">-IncludedEventType 옵션에서 'All' 사용을 허용하지 않고 다음으로 대체함</span><span class="sxs-lookup"><span data-stu-id="e94b5-383">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span> 
    - <span data-ttu-id="e94b5-384">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="e94b5-384">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="e94b5-385">결과 페이지 매김 및 필터링을 지원하는 새로운 선택적 매개 변수(Top, ODataQuery 및 NextLink)를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-385">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="e94b5-386">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="e94b5-386">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="e94b5-387">Event Grid 도메인 및 Event Grid 도메인 토픽에 대한 파이핑을 지원하기 위해 새로운 필수 매개 변수를 추가하여 이러한 리소스 아래에 기존 이벤트 구독을 제거할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-387">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="e94b5-388">Event Grid 도메인 이름 및 Event Grid 도메인 토픽 이름을 지정하기 위해 새로운 필수 매개 변수를 추가하여 이러한 리소스 아래에 기존 이벤트 구독을 제거할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-388">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="e94b5-389">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="e94b5-389">Az.FrontDoor</span></span>
* <span data-ttu-id="e94b5-390">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="e94b5-390">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="e94b5-391">변환 지원 및 새 연산자 자동 완성 값(RegEx)을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-391">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="e94b5-392">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="e94b5-392">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="e94b5-393">새 자동 완성 값 추가</span><span class="sxs-lookup"><span data-stu-id="e94b5-393">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e94b5-394">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e94b5-394">Az.Network</span></span>
* <span data-ttu-id="e94b5-395">Microsoft Azure Virtual Network 게이트웨이 리소스에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="e94b5-395">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="e94b5-396">새 cmdlet</span><span class="sxs-lookup"><span data-stu-id="e94b5-396">New cmdlets</span></span>
        - <span data-ttu-id="e94b5-397">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="e94b5-397">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="e94b5-398">AvailablePrivateEndpointType 추가</span><span class="sxs-lookup"><span data-stu-id="e94b5-398">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="e94b5-399">새 cmdlet</span><span class="sxs-lookup"><span data-stu-id="e94b5-399">New cmdlets</span></span> 
        - <span data-ttu-id="e94b5-400">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="e94b5-400">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="e94b5-401">PrivatePrivateLinkService 추가</span><span class="sxs-lookup"><span data-stu-id="e94b5-401">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="e94b5-402">새 cmdlet</span><span class="sxs-lookup"><span data-stu-id="e94b5-402">New cmdlets</span></span> 
        - <span data-ttu-id="e94b5-403">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="e94b5-403">Get-AzPrivateLinkService</span></span> 
        - <span data-ttu-id="e94b5-404">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="e94b5-404">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="e94b5-405">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="e94b5-405">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="e94b5-406">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="e94b5-406">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="e94b5-407">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="e94b5-407">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="e94b5-408">PrivateEndpoint 추가</span><span class="sxs-lookup"><span data-stu-id="e94b5-408">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="e94b5-409">새 cmdlet</span><span class="sxs-lookup"><span data-stu-id="e94b5-409">New cmdlets</span></span>
        - <span data-ttu-id="e94b5-410">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="e94b5-410">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="e94b5-411">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="e94b5-411">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="e94b5-412">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="e94b5-412">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="e94b5-413">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="e94b5-413">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="e94b5-414">기능에 대한 새로운 명령이 업데이트됨: VpnConnection 상의 UseLocalAzureIpAddress 플래그</span><span class="sxs-lookup"><span data-stu-id="e94b5-414">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="e94b5-415">New-AzVpnConnection이 업데이트됨: 선택적 매개 변수 -UseLocalAzureIpAddress를 추가하여 로컬 Azure IP 주소가 연결을 시작하는 동안 소스 주소로 사용되어야 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-415">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="e94b5-416">Set-AzVpnConnection이 업데이트됨: 선택적 매개 변수 -UseLocalAzureIpAddress를 추가하여 로컬 Azure IP 주소가 연결을 시작하는 동안 소스 주소로 사용되어야 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-416">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="e94b5-417">ExpressRoute 피어링에 읽기 전용 필드 PeeredConnections가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-417">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="e94b5-418">ExpressRoute에 읽기 전용 필드 GlobalReachEnabled가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-418">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="e94b5-419">ExpressRouteCircuit 모델에서 AllowGlobalReach 필드의 사용 중단을 부르는 호환성이 손상되는 변경 속성이 추가됨</span><span class="sxs-lookup"><span data-stu-id="e94b5-419">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="e94b5-420">AzApplicationGatewayRedirectConfiguration cmdlet에서 TargetListenerID를 사용하는 중의 8756 오류 문제가 해결됨</span><span class="sxs-lookup"><span data-stu-id="e94b5-420">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="e94b5-421">다시 쓰기 규칙 세트가 설정되지 못하게 하는 New-AzApplicationGatewayPathRuleConfig의 버그를 수정했습니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-421">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="e94b5-422">NetworkInterfaceIpConfiguration에 VirtualNetworkTaps가 표시되는 방식이 수정됨</span><span class="sxs-lookup"><span data-stu-id="e94b5-422">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="e94b5-423">모든 파트를 나열하도록 Cortex Get cmdlet이 수정됨</span><span class="sxs-lookup"><span data-stu-id="e94b5-423">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="e94b5-424">ExpressRouteGateways, VpnGateway에 대한 VirtualHub 참조 생성 수정됨</span><span class="sxs-lookup"><span data-stu-id="e94b5-424">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="e94b5-425">AzureFirewall 및 NatGateway의 가용성 영역에 대한 지원 추가됨</span><span class="sxs-lookup"><span data-stu-id="e94b5-425">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="e94b5-426">Get-AzNetworkServiceTag cmdlet 추가됨</span><span class="sxs-lookup"><span data-stu-id="e94b5-426">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="e94b5-427">Azure Firewall에 대한 여러 공용 IP 주소에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="e94b5-427">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="e94b5-428">New-AzFirewall cmdlet이 업데이트됨:</span><span class="sxs-lookup"><span data-stu-id="e94b5-428">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="e94b5-429">하나 이상의 공용 IP 주소 개체를 허용하는 매개 변수 -PublicIpAddress 추가됨</span><span class="sxs-lookup"><span data-stu-id="e94b5-429">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="e94b5-430">Virtual Network 개체를 허용하는 매개 변수 -VirtualNetwork 추가됨</span><span class="sxs-lookup"><span data-stu-id="e94b5-430">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="e94b5-431">방화벽 개체에 AddPublicIpAddress 및 RemovePublicIpAddress 메서드 추가됨 - 공용 IP 주소 개체를 입력으로 허용</span><span class="sxs-lookup"><span data-stu-id="e94b5-431">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="e94b5-432">매개 변수 -PublicIpName 및 -VirtualNetworkName이 더 이상 사용되지 않음</span><span class="sxs-lookup"><span data-stu-id="e94b5-432">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span> 
* <span data-ttu-id="e94b5-433">기능에 대한 새로운 명령이 업데이트됨: VpnClient AAD 인증 옵션을 가상 네트워크 게이트웨이 리소스로 설정했습니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-433">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span> 
    - <span data-ttu-id="e94b5-434">New-AzVirtualNetworkGateway가 업데이트됨: 게이트웨이에서 VpnClient AAD 인증 옵션을 설정할 수 있도록 선택적 매개 변수 AadTenantUri, AadAudienceId, AadIssuerUri가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-434">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="e94b5-435">Set-AzVirtualNetworkGateway가 업데이트됨: 게이트웨이에서 VpnClient AAD 인증 옵션을 설정할 수 있도록 선택적 매개 변수 AadTenantUri, AadAudienceId, AadIssuerUri가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-435">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="e94b5-436">Set-AzVirtualNetworkGateway가 업데이트됨: 게이트웨이에서 VpnClient AAD 인증 옵션을 제거할 수 있도록 선택적인 스위치 매개 변수 RemoveAadAuthentication이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-436">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="e94b5-437">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="e94b5-437">Az.OperationalInsights</span></span>
* <span data-ttu-id="e94b5-438">'New-AzureRmOperationalInsightsWorkspace' 명령에서 **pergb2018** 가격 책정 계층 사용</span><span class="sxs-lookup"><span data-stu-id="e94b5-438">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="e94b5-439">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e94b5-439">Az.Resources</span></span>
* <span data-ttu-id="e94b5-440">추가 템플릿 내보내기 옵션 지원</span><span class="sxs-lookup"><span data-stu-id="e94b5-440">Support for additional Template Export options</span></span>
    - <span data-ttu-id="e94b5-441">Export-AzResourceGroup에 '-SkipResourceNameParameterization' 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="e94b5-441">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="e94b5-442">Export-AzResourceGroup에 '-SkipAllParameterization' 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="e94b5-442">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="e94b5-443">내보낸 리소스 필터링을 위해 Export-AzResourceGroup에 '-Resource' 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="e94b5-443">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="e94b5-444">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="e94b5-444">Az.ServiceFabric</span></span>
* <span data-ttu-id="e94b5-445">일부 경우 잘못된 지문을 가져오는 추가 인증서 ByExistingKeyVault 수정</span><span class="sxs-lookup"><span data-stu-id="e94b5-445">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="e94b5-446">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e94b5-446">Az.Sql</span></span>
* <span data-ttu-id="e94b5-447">Advanced Threat Protection 스토리지 엔드포인트 접미사 수정</span><span class="sxs-lookup"><span data-stu-id="e94b5-447">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="e94b5-448">Advanced Data Security가 Advanced Threat Protection 정책을 재정의하는 것을 수정</span><span class="sxs-lookup"><span data-stu-id="e94b5-448">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="e94b5-449">고객이 TDE 키를 추가하고 관리되는 인스턴스에 TDE 보호기를 설정할 수 있도록 Management.Sql용 새 Cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="e94b5-449">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="e94b5-450">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="e94b5-450">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="e94b5-451">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="e94b5-451">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="e94b5-452">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="e94b5-452">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="e94b5-453">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="e94b5-453">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="e94b5-454">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="e94b5-454">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="e94b5-455">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="e94b5-455">Az.Storage</span></span>
* <span data-ttu-id="e94b5-456">스토리지 계정 생성 시 종류 FileStorage 및 SkuName Premium_ZRS 지원</span><span class="sxs-lookup"><span data-stu-id="e94b5-456">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="e94b5-457">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="e94b5-457">New-AzStorageAccount</span></span>
* <span data-ttu-id="e94b5-458">BLOB immutability cmdlet의 설명 명확화</span><span class="sxs-lookup"><span data-stu-id="e94b5-458">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="e94b5-459">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="e94b5-459">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="e94b5-460">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="e94b5-460">Az.Websites</span></span>
* <span data-ttu-id="e94b5-461">Get-AzWebAppCertificate를 클라이언트 대신 서버의 리소스 그룹별로 필터링하도록 최적화</span><span class="sxs-lookup"><span data-stu-id="e94b5-461">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="e94b5-462">Get-AzWebAppSnapshot에 -UseDisasterRecovery 스위치 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="e94b5-462">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="e94b5-463">2.2.0 - 2019년 6월</span><span class="sxs-lookup"><span data-stu-id="e94b5-463">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="e94b5-464">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="e94b5-464">Az.Cdn</span></span>
* <span data-ttu-id="e94b5-465">cmdlet에서 2019-04-15 API 버전 기반의 rulesEngine 기능을 지원하도록 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-465">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e94b5-466">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e94b5-466">Az.Compute</span></span>
* <span data-ttu-id="e94b5-467">작업을 시작하여 완료되기 전에 즉시 반환하는 `NoWait` 매개 변수가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-467">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="e94b5-468">다음 Cmdlet이 업데이트 되었습니다.   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="e94b5-468">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="e94b5-469">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="e94b5-469">Az.EventHub</span></span>
* <span data-ttu-id="e94b5-470">#9231 수정 - Get-AzEventHubNamespace에서 태그를 반환하지 않음</span><span class="sxs-lookup"><span data-stu-id="e94b5-470">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="e94b5-471">#9230 수정 - Get-AzEventHubNamespace에서 ResourceGroupName 대신 ResourceGroup을 반환함</span><span class="sxs-lookup"><span data-stu-id="e94b5-471">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e94b5-472">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e94b5-472">Az.Network</span></span>
* <span data-ttu-id="e94b5-473">Nat Gateway에 대한 ResourceId 및 InputObject 업데이트</span><span class="sxs-lookup"><span data-stu-id="e94b5-473">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="e94b5-474">ResourceId 및 InputObject에 대한 별칭 추가</span><span class="sxs-lookup"><span data-stu-id="e94b5-474">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="e94b5-475">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="e94b5-475">Az.PolicyInsights</span></span>
* <span data-ttu-id="e94b5-476">Get-AzPolicyEvent에서 Null 참조 문제 해결</span><span class="sxs-lookup"><span data-stu-id="e94b5-476">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="e94b5-477">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="e94b5-477">Az.RecoveryServices</span></span>
* <span data-ttu-id="e94b5-478">IaaSVM 정책 최소 보존 기간(일)이 1에서 7로 변경됨</span><span class="sxs-lookup"><span data-stu-id="e94b5-478">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="e94b5-479">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="e94b5-479">Az.ServiceBus</span></span>
* <span data-ttu-id="e94b5-480">#9182 문제 해결 - Get-AzServiceBusNamespace에서 ResourceGroupName 대신 ResourceGroup을 반환</span><span class="sxs-lookup"><span data-stu-id="e94b5-480">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="e94b5-481">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="e94b5-481">Az.ServiceFabric</span></span>
* <span data-ttu-id="e94b5-482">'Update-AzServiceFabricReliability' 오류 메시지의 오타 수정</span><span class="sxs-lookup"><span data-stu-id="e94b5-482">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="e94b5-483">Service Fabric 명령줄에서 누락된 문자 수정</span><span class="sxs-lookup"><span data-stu-id="e94b5-483">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="e94b5-484">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e94b5-484">Az.Sql</span></span>
* <span data-ttu-id="e94b5-485">Managed Instance에 대한 AutoDr을 지원하기 위해 New-AzureSqlInstance cmdlet에 대한 DnsZonePartner 매개 변수를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-485">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="e94b5-486">Get-AzSqlDatabaseSecureConnectionPolicy cmdlet 사용 중단</span><span class="sxs-lookup"><span data-stu-id="e94b5-486">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="e94b5-487">Threat Detection(위협 탐지) cmdlet 이름을 Advanced Threat Protection으로 변경함</span><span class="sxs-lookup"><span data-stu-id="e94b5-487">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="e94b5-488">새 AzSqlInstance -StorageSizeInGB 및 -LicenseType 매개 변수는 이제 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-488">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="e94b5-489">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="e94b5-489">Az.Websites</span></span>
* <span data-ttu-id="e94b5-490">-WebApp 속성에서 Set-AzWebApp 및 Set-AzWebAppSlot을 사용하면 태그가 제거되는 문제를 해결함</span><span class="sxs-lookup"><span data-stu-id="e94b5-490">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="e94b5-491">2.1.0 - 2019년 5월</span><span class="sxs-lookup"><span data-stu-id="e94b5-491">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="e94b5-492">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="e94b5-492">Az.ApiManagement</span></span>
* <span data-ttu-id="e94b5-493">글로벌 및 API 범위에서 진단을 관리하기 위한 새 cmdlet을 만들었습니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-493">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="e94b5-494">**Get-AzApiManagementDiagnostic** - 글로벌 또는 API 범위가 구성된 진단 가져오기</span><span class="sxs-lookup"><span data-stu-id="e94b5-494">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="e94b5-495">**New-AzApiManagementDiagnostic** - 글로벌 범위 또는 API 범위에서 새 진단 만들기</span><span class="sxs-lookup"><span data-stu-id="e94b5-495">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="e94b5-496">**New-AzApiManagementHttpMessageDiagnostic** - 기록할 Headers(헤더) 및 Body Bytes(본문 바이트 수) 크기에 대한 진단 설정 만들기</span><span class="sxs-lookup"><span data-stu-id="e94b5-496">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="e94b5-497">**New-AzApiManagementPipelineDiagnosticSetting** - 게이트웨이로 들어오고 나가는 HTTP 메시지에 대한 진단 설정 만들기</span><span class="sxs-lookup"><span data-stu-id="e94b5-497">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="e94b5-498">**New-AzApiManagementSamplingSetting** - 진단 요청/응답에 대한 샘플링 설정 만들기</span><span class="sxs-lookup"><span data-stu-id="e94b5-498">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="e94b5-499">**Remove-AzApiManagementDiagnostic** - 글로벌 또는 API 범위에서 진단 엔터티 제거</span><span class="sxs-lookup"><span data-stu-id="e94b5-499">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="e94b5-500">**Set-AzApiManagementDiagnostic** - 글로벌 또는 API 범위에서 진단 엔터티 업데이트</span><span class="sxs-lookup"><span data-stu-id="e94b5-500">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="e94b5-501">ApiManagement 서비스에서 캐시를 관리하기 위한 새 cmdlet을 만들었습니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-501">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="e94b5-502">**Get-AzApiManagementCache** - 식별자 또는 모든 캐시로 지정된 캐시의 세부 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="e94b5-502">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="e94b5-503">**New-AzApiManagementCache** - 특정 Azure 'region'(지역)에 새 'default'(기본) 캐시 만들기</span><span class="sxs-lookup"><span data-stu-id="e94b5-503">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="e94b5-504">**Remove-AzApiManagementCache** - 캐시 제거</span><span class="sxs-lookup"><span data-stu-id="e94b5-504">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="e94b5-505">**Update-AzApiManagementCache** - 캐시 업데이트</span><span class="sxs-lookup"><span data-stu-id="e94b5-505">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="e94b5-506">API 스키마 관리하기 위한 새 cmdlet을 만들었습니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-506">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="e94b5-507">**New-AzApiManagementSchema** - API에 대한 새 스키마 만들기</span><span class="sxs-lookup"><span data-stu-id="e94b5-507">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="e94b5-508">**Get-AzApiManagementSchema** - API에 구성된 스키마 가져오기</span><span class="sxs-lookup"><span data-stu-id="e94b5-508">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="e94b5-509">**Remove-AzApiManagementSchema** - API에 구성된 스키마 제거</span><span class="sxs-lookup"><span data-stu-id="e94b5-509">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="e94b5-510">**Set-AzApiManagementSchema** - API에 구성된 스키마 업데이트</span><span class="sxs-lookup"><span data-stu-id="e94b5-510">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="e94b5-511">사용자 토큰을 생성하기 위한 새 cmdlet을 만들었습니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-511">Created new Cmdlet for generating a User Token.</span></span> 
    - <span data-ttu-id="e94b5-512">**New-AzApiManagementUserToken** - 기본적으로 8시간 동안 유효한 새 사용자 토큰을 생성합니다. 'GIT' 사용자에 대한 토큰은 이 cmdlet을 사용하여 생성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-512">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="e94b5-513">네트워크 상태를 검색하기 위한 새 cmdlet을 만들었습니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-513">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="e94b5-514">**Get-AzApiManagementNetworkStatus** - API Management 서비스에서 사용하는 리소스의 네트워크 상태 연결을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-514">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="e94b5-515">ApiManagement 서비스를 가상 네트워크에 배포하고 종속성이 손상되었는지 여부를 확인할 때 유용합니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-515">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="e94b5-516">**New-AzApiManagement** cmdlet에서 ApiManagement 서비스를 관리하도록 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-516">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span> 
    - <span data-ttu-id="e94b5-517">새 '소비' SKU 지원이 추가됨</span><span class="sxs-lookup"><span data-stu-id="e94b5-517">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="e94b5-518">'소비' SKU에 대해 'EnableClientCertificate' 플래그를 설정하기 위한 지원이 추가됨</span><span class="sxs-lookup"><span data-stu-id="e94b5-518">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="e94b5-519">새 **New-AzApiManagementSslSetting** cmdlet을 사용하면 'Backend(백 엔드)' 및 'Frontend'(프런트 엔드)에서 'TLS/SSL' 설정을 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-519">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="e94b5-520">또한 ApiManagement 서비스의 'Frontend'에서 '3DES'와 같은 'Ciphers'와 'Http2'와 같은 'ServerProtocols'를 구성하는 데 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-520">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="e94b5-521">ApiManagement 서비스에서 'DeveloperPortal' 호스트 이름을 구성하기 위한 지원이 추가됨</span><span class="sxs-lookup"><span data-stu-id="e94b5-521">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="e94b5-522">**Get-AzApiManagementSsoToken** cmdlet에서 'PsApiManagement' 개체를 입력으로 사용하도록 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-522">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="e94b5-523">cmdlet에서 오류 메시지를 인라인으로 표시하도록 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-523">Updated the cmdlet to display Error Messages inline</span></span> 
     > <span data-ttu-id="e94b5-524">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : 오류 코드: ValidationError 오류 메시지: 하나 이상의 필드에 잘못된 값이 있습니다. 오류 세부 정보:    [Code=ValidationError, Message=줄 3, 열 10의 'log-to-eventhub' 요소에 오류가 있습니다.: 로거를 찾지 못함, Target=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="e94b5-524">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="e94b5-525">**Export-AzApiManagementApi** cmdlet에서 API를 'OpenApi 3.0' 형식으로 내보내도록 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-525">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="e94b5-526">**Import-AzApiManagementApi** cmdlet을 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-526">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="e94b5-527">'OpenApi 3.0' 문서 사양에서 API 가져오기</span><span class="sxs-lookup"><span data-stu-id="e94b5-527">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="e94b5-528">문서('Swagger', 'Wadl', 'Wsdl', 'OpenApi')에 지정된 'PsApiManagementSchema' 속성 재정의</span><span class="sxs-lookup"><span data-stu-id="e94b5-528">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="e94b5-529">문서에 지정된 'ServiceUrl' 속성 재정의</span><span class="sxs-lookup"><span data-stu-id="e94b5-529">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="e94b5-530">**Get-AzApiManagementPolicy** cmdlet에서 'rawxml'을 사용하여 이스케이프된 비 Xml 'format'(형식)의 정책을 반환하도록 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-530">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="e94b5-531">**Set-AzApiManagementPolicy** cmdlet에서 'rawxml'을 사용하여 이스케이프된 비 Xml 'format'의 정책을 수락하고, 'xml'을 사용하여 이스케이프된 Xml 'format'의 정책을 수락하도록 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-531">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="e94b5-532">**New-AzApiManagementApi** cmdlet을 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-532">Updated cmdlet **New-AzApiManagementApi**</span></span> 
    - <span data-ttu-id="e94b5-533">'OpenId' 권한 부여 서버를 사용하여 API 구성</span><span class="sxs-lookup"><span data-stu-id="e94b5-533">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="e94b5-534">'ApiVersionSet'에서 API 만들기</span><span class="sxs-lookup"><span data-stu-id="e94b5-534">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="e94b5-535">'SourceApiId' 및 'SourceApiRevision'을 사용하여 API 복제</span><span class="sxs-lookup"><span data-stu-id="e94b5-535">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="e94b5-536">API 범위에서 'SubscriptionRequired' 구성 가능</span><span class="sxs-lookup"><span data-stu-id="e94b5-536">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="e94b5-537">**Set-AzApiManagementApi** cmdlet을 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-537">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="e94b5-538">'OpenId' 권한 부여 서버를 사용하여 API 구성</span><span class="sxs-lookup"><span data-stu-id="e94b5-538">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="e94b5-539">API를 'ApiVersionSet'으로 업데이트</span><span class="sxs-lookup"><span data-stu-id="e94b5-539">To updated an API into an 'ApiVersionSet'</span></span>    
    - <span data-ttu-id="e94b5-540">API 범위에서 'SubscriptionRequired' 구성 가능</span><span class="sxs-lookup"><span data-stu-id="e94b5-540">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="e94b5-541">**New-AzApiManagementRevision** cmdlet을 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-541">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="e94b5-542">'SourceApiRevision'을 사용하여 기존 수정 버전 복제(태그, 제품, 작업 및 정책 복사).</span><span class="sxs-lookup"><span data-stu-id="e94b5-542">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="e94b5-543">새 수정 버전은 부모의 'ApiId'를 가정합니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-543">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="e94b5-544">'ApiRevisionDescription' 제공</span><span class="sxs-lookup"><span data-stu-id="e94b5-544">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="e94b5-545">API 복제 시 'ServiceUrl' 재정의</span><span class="sxs-lookup"><span data-stu-id="e94b5-545">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="e94b5-546">**New-AzApiManagementIdentityProvider** cmdlet을 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-546">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="e94b5-547">'Authority'를 사용하여 'AAD' 또는 'AADB2C' 구성</span><span class="sxs-lookup"><span data-stu-id="e94b5-547">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="e94b5-548">'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' 및 'PasswordResetPolicy' 설정</span><span class="sxs-lookup"><span data-stu-id="e94b5-548">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="e94b5-549">**New-AzApiManagementSubscription** cmdlet을 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-549">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="e94b5-550">'Scope' 및 'UserId'를 사용하여 새 SubscriptonModel 설명</span><span class="sxs-lookup"><span data-stu-id="e94b5-550">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="e94b5-551">'ProductId' 및 'UserId'를 사용하여 이전 구독 모델 설명</span><span class="sxs-lookup"><span data-stu-id="e94b5-551">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="e94b5-552">구독 수준에서 'AllowTracing'을 사용하도록 설정하는 지원 추가</span><span class="sxs-lookup"><span data-stu-id="e94b5-552">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="e94b5-553">**Set-AzApiManagementSubscription** cmdlet을 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-553">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="e94b5-554">'Scope' 및 'UserId'를 사용하여 새 SubscriptonModel 설명</span><span class="sxs-lookup"><span data-stu-id="e94b5-554">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="e94b5-555">'ProductId' 및 'UserId'를 사용하여 이전 구독 모델 설명</span><span class="sxs-lookup"><span data-stu-id="e94b5-555">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="e94b5-556">구독 수준에서 'AllowTracing'을 사용하도록 설정하는 지원 추가</span><span class="sxs-lookup"><span data-stu-id="e94b5-556">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="e94b5-557">다음 cmdlet에서 'ResourceId'를 입력으로 수락하도록 업데이트했습니다</span><span class="sxs-lookup"><span data-stu-id="e94b5-557">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="e94b5-558">'New-AzApiManagementContext'</span><span class="sxs-lookup"><span data-stu-id="e94b5-558">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="e94b5-559">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="e94b5-559">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="e94b5-560">'Get-AzApiManagementApiRelease'</span><span class="sxs-lookup"><span data-stu-id="e94b5-560">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="e94b5-561">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="e94b5-561">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="e94b5-562">'Get-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="e94b5-562">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="e94b5-563">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="e94b5-563">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="e94b5-564">'Get-AzApiManagementAuthorizationServer'</span><span class="sxs-lookup"><span data-stu-id="e94b5-564">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="e94b5-565">'Get-AzApiManagementBackend'</span><span class="sxs-lookup"><span data-stu-id="e94b5-565">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="e94b5-566">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="e94b5-566">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="e94b5-567">'Get-AzApiManagementCertificate'</span><span class="sxs-lookup"><span data-stu-id="e94b5-567">'Get-AzApiManagementCertificate'</span></span> 
    - <span data-ttu-id="e94b5-568">'Remove-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="e94b5-568">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="e94b5-569">'Remove-AzApiManagementSubscription'</span><span class="sxs-lookup"><span data-stu-id="e94b5-569">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="e94b5-570">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="e94b5-570">Az.Automation</span></span>
* <span data-ttu-id="e94b5-571">Get-AzAutomationJobOutputRecord에서 JSON 및 Text 레코드 값을 처리하도록 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-571">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="e94b5-572">문제 https://github.com/Azure/azure-powershell/issues/7977 수정</span><span class="sxs-lookup"><span data-stu-id="e94b5-572">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="e94b5-573">문제 https://github.com/Azure/azure-powershell/issues/8600 수정</span><span class="sxs-lookup"><span data-stu-id="e94b5-573">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="e94b5-574">Start-AzAutomationDscCompilationJob에서 완료될 때까지 기다리지 않고 작업을 바로 시작하도록 변경했습니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-574">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="e94b5-575">문제 https://github.com/Azure/azure-powershell/issues/8347 수정</span><span class="sxs-lookup"><span data-stu-id="e94b5-575">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="e94b5-576">-Name을 사용하면 모든 노드를 반환하는 Get-AzAutomationDscNode 수정.</span><span class="sxs-lookup"><span data-stu-id="e94b5-576">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="e94b5-577">이제 일치하는 노드만 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-577">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e94b5-578">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e94b5-578">Az.Compute</span></span>
* <span data-ttu-id="e94b5-579">ProtectFromScaleIn 및 ProtectFromScaleSetAction 매개 변수를 Update-AzVmssVM cmdlet에 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-579">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="e94b5-580">'East US'(미국 동부)가 지원되지 않는 경우 이제 New-AzVM wimple 매개 변수 집합에서 기본적으로 사용 가능한 위치를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-580">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="e94b5-581">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="e94b5-581">Az.DataLakeStore</span></span>
* <span data-ttu-id="e94b5-582">ADLS SDK에서 httpclient를 사용하도록 업데이트하고, 데이터 평면 테스트를 Azure 프레임워크와 통합합니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-582">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="e94b5-583">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="e94b5-583">Az.Monitor</span></span>
* <span data-ttu-id="e94b5-584">도움말 예제에서 잘못된 매개 변수 이름을 수정했습니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-584">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e94b5-585">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e94b5-585">Az.Network</span></span>
* <span data-ttu-id="e94b5-586">DisableBgpRoutePropagation 플래그를 유효 경로 테이블 출력에 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-586">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="e94b5-587">업데이트된 cmdlet:</span><span class="sxs-lookup"><span data-stu-id="e94b5-587">Updated cmdlet:</span></span>
        - <span data-ttu-id="e94b5-588">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="e94b5-588">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="e94b5-589">New-AzApplicationGatewayTrustedRootCertificate 설명서에서 이중 파선을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-589">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="e94b5-590">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e94b5-590">Az.Resources</span></span>
* <span data-ttu-id="e94b5-591">할당 거부를 검색하기 위한 새 Get-AzureRmDenyAssignment cmdlet을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-591">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="e94b5-592">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e94b5-592">Az.Sql</span></span>
* <span data-ttu-id="e94b5-593">Advanced Threat Protection cmdlet의 이름을 Advanced Data Security로 변경하고, 취약성 평가를 기본적으로 사용하도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-593">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="e94b5-594">2.0.0 - 2019년 5월</span><span class="sxs-lookup"><span data-stu-id="e94b5-594">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="e94b5-595">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e94b5-595">Az.Accounts</span></span>
* <span data-ttu-id="e94b5-596">사용자 이름/비밀번호 인증을 사용하여 ADFS 문제를 해결하도록 인증 라이브러리 업데이트</span><span class="sxs-lookup"><span data-stu-id="e94b5-596">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="e94b5-597">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="e94b5-597">Az.CognitiveServices</span></span>
* <span data-ttu-id="e94b5-598">Bing Search 서비스에 대해서만 Bing 면책 조항을 표시하세요.</span><span class="sxs-lookup"><span data-stu-id="e94b5-598">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="e94b5-599">계정 생성 실패 시 오류 개선.</span><span class="sxs-lookup"><span data-stu-id="e94b5-599">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e94b5-600">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e94b5-600">Az.Compute</span></span>
* <span data-ttu-id="e94b5-601">근접 배치 그룹 기능</span><span class="sxs-lookup"><span data-stu-id="e94b5-601">Proximity placement group feature.</span></span>
    - <span data-ttu-id="e94b5-602">다음과 같은 새 cmdlet을 추가했습니다.   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="e94b5-602">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="e94b5-603">새 매개 변수 ProximityPlacementGroupId가 다음 cmdlet에 추가됩니다.   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="e94b5-603">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="e94b5-604">New-AzGalleryImageVersion에 StorageAccountType 매개 변수가 추가됩니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-604">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="e94b5-605">New-AzGalleryImageVersion의 TargetRegion이 StorageAccountType를 포함할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-605">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="e94b5-606">SkipShutdown 스위치 매개 변수가 Stop-AzVM 및 Stop-AzVmss에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-606">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>       
* <span data-ttu-id="e94b5-607">주요 변경 내용</span><span class="sxs-lookup"><span data-stu-id="e94b5-607">Breaking changes</span></span>
    - <span data-ttu-id="e94b5-608">Set-AzVMBootDiagnostics이 Set-AzVMBootDiagnostic으로 변경됩니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-608">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="e94b5-609">Export-AzLogAnalyticThrottledRequests이 Export-AzLogAnalyticThrottledRequests로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-609">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="e94b5-610">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="e94b5-610">Az.DeploymentManager</span></span>
* <span data-ttu-id="e94b5-611">Azure 배포 관리자 cmdlet의 일반적으로 사용 가능한 첫 번째 릴리스</span><span class="sxs-lookup"><span data-stu-id="e94b5-611">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="e94b5-612">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="e94b5-612">Az.Dns</span></span>
* <span data-ttu-id="e94b5-613">자동 DNS 이름 서버 위임</span><span class="sxs-lookup"><span data-stu-id="e94b5-613">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="e94b5-614">DNS 영역 만들기 cmdlet은 추가 선택적 매개 변수로 부모 영역 이름을 허용합니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-614">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="e94b5-615">새로 생성 된 자식 영역의 부모 영역에 NS 레코드를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-615">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="e94b5-616">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="e94b5-616">Az.FrontDoor</span></span>
* <span data-ttu-id="e94b5-617">Azure FrontDoor cmdlet의 일반적으로 사용 가능한 첫 번째 릴리스</span><span class="sxs-lookup"><span data-stu-id="e94b5-617">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="e94b5-618">'Waf'를 포함하도록 WAF cmdlet의 이름 바꾸기</span><span class="sxs-lookup"><span data-stu-id="e94b5-618">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="e94b5-619">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="e94b5-619">Az.HDInsight</span></span>
* <span data-ttu-id="e94b5-620">두 개의 cmdlet을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-620">Removed two cmdlets:</span></span>
    - <span data-ttu-id="e94b5-621">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="e94b5-621">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="e94b5-622">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="e94b5-622">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="e94b5-623">Grant-AzHDInsightHttpServicesAccess를 대체할 새 cmdlet Set-AzHDInsightGatewayCredential을 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-623">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="e94b5-624">reader 역할과 HDInsight 운영자 역할을 구분하도록 cmdlet Get-AzHDInsightJobOutput 업데이트:</span><span class="sxs-lookup"><span data-stu-id="e94b5-624">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="e94b5-625">reader 역할을 가진 사용자는 'DefaultStorageAccountKey'매개 변수를 명시적으로 지정해야 합니다. 그렇지 않으면 오류가 발생합니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-625">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="e94b5-626">Hdinsight 운영자 역할을 가진 사용자를 영향을 받지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-626">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="e94b5-627">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="e94b5-627">Az.Monitor</span></span>
* <span data-ttu-id="e94b5-628">SQR API(예약 쿼리 규칙)용 새 cmdlet</span><span class="sxs-lookup"><span data-stu-id="e94b5-628">New cmdlets for SQR API (Scheduled Query Rule)</span></span>  
    - <span data-ttu-id="e94b5-629">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="e94b5-629">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="e94b5-630">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="e94b5-630">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="e94b5-631">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="e94b5-631">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="e94b5-632">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="e94b5-632">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="e94b5-633">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="e94b5-633">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="e94b5-634">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="e94b5-634">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="e94b5-635">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="e94b5-635">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="e94b5-636">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="e94b5-636">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="e94b5-637">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="e94b5-637">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="e94b5-638">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="e94b5-638">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="e94b5-639">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="e94b5-639">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="e94b5-640">SQR API에 대한 [자세한 내용](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules)</span><span class="sxs-lookup"><span data-stu-id="e94b5-640">[More](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="e94b5-641">GenV2(비 클래식) 메트릭 기반 경고 규칙에 대한 cmdlet을 포함하도록 Az.Monitor.md가 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="e94b5-641">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e94b5-642">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e94b5-642">Az.Network</span></span>
* <span data-ttu-id="e94b5-643">Nat 게이트웨이 리소스에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="e94b5-643">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="e94b5-644">새 cmdlet</span><span class="sxs-lookup"><span data-stu-id="e94b5-644">New cmdlets</span></span>
        - <span data-ttu-id="e94b5-645">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="e94b5-645">New-AzNatGateway</span></span>
        - <span data-ttu-id="e94b5-646">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="e94b5-646">Get-AzNatGateway</span></span>
        - <span data-ttu-id="e94b5-647">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="e94b5-647">Set-AzNatGateway</span></span>
        - <span data-ttu-id="e94b5-648">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="e94b5-648">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="e94b5-649">다음 Cmdlet이 업데이트 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-649">Updated cmdlets</span></span>
        - <span data-ttu-id="e94b5-650">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="e94b5-650">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="e94b5-651">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="e94b5-651">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="e94b5-652">기능에 대한 새로운 명령이 업데이트됨: Brooklyn Gateway에서 사용자 지정 경로 설정/제거.</span><span class="sxs-lookup"><span data-stu-id="e94b5-652">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="e94b5-653">New-AzVirtualNetworkGateway가 업데이트됨: 선택적 매개 변수 -CustomRoute를 추가하여 게이트웨이에서 설정할 사용자 지정 경로로 주소 접두사를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-653">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="e94b5-654">Set-AzVirtualNetworkGateway가 업데이트됨: 선택적 매개 변수 -CustomRoute를 추가하여 게이트웨이에서 설정할 사용자 지정 경로로 주소 접두사를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-654">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="e94b5-655">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="e94b5-655">Az.PolicyInsights</span></span>
* <span data-ttu-id="e94b5-656">정책 평가 세부 정보 쿼리 지원</span><span class="sxs-lookup"><span data-stu-id="e94b5-656">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="e94b5-657">Get-AzPolicyState에 '-Expand'매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="e94b5-657">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="e94b5-658">'-Expand PolicyEvaluationDetails' 지원</span><span class="sxs-lookup"><span data-stu-id="e94b5-658">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="e94b5-659">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="e94b5-659">Az.RecoveryServices</span></span>
* <span data-ttu-id="e94b5-660">크로스 구독 Azure에서 Azure 사이트 복구 지원</span><span class="sxs-lookup"><span data-stu-id="e94b5-660">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="e94b5-661">Azure Site Recovery에 대한 호환성이 손상되는 변경 표시</span><span class="sxs-lookup"><span data-stu-id="e94b5-661">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="e94b5-662">Azure Site Recovery 복구 계획 최종 실행 계획에 대한 수정</span><span class="sxs-lookup"><span data-stu-id="e94b5-662">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="e94b5-663">Azure에서 Azure에 대한 Azure Site Recovery 업데이트 네트워크 매핑 수정</span><span class="sxs-lookup"><span data-stu-id="e94b5-663">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="e94b5-664">관리 디스크에 대한 Azure에서 Azure에 대한 Azure Site Recovery 업데이트 보호 방향 수정</span><span class="sxs-lookup"><span data-stu-id="e94b5-664">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="e94b5-665">기타 사소한 수정.</span><span class="sxs-lookup"><span data-stu-id="e94b5-665">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="e94b5-666">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="e94b5-666">Az.Relay</span></span>
* <span data-ttu-id="e94b5-667">고객 관련 메시지의 철자 오류 수정</span><span class="sxs-lookup"><span data-stu-id="e94b5-667">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="e94b5-668">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="e94b5-668">Az.ServiceBus</span></span>
* <span data-ttu-id="e94b5-669">네임스페이스의 NetworkRuleSet에 대한 새 cmdlet가 추가되었습니다</span><span class="sxs-lookup"><span data-stu-id="e94b5-669">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="e94b5-670">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="e94b5-670">Az.Storage</span></span>
* <span data-ttu-id="e94b5-671">저장소 클라이언트 라이브러리 10.0.1로 업그레이드(이 SDK의 모든 개체의 네임스페이스가 'Microsoft.WindowsAzure.Storage. *'에서 'Microsoft.Azure.Storage.* '로 변경됨)</span><span class="sxs-lookup"><span data-stu-id="e94b5-671">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="e94b5-672">새로운 API 버전 2019-04-01을 지원하기 위해 Microsoft.Azure.Management.Storage 11.0.0으로 업그레이드합니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-672">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="e94b5-673">스토리지 생성 계정의 기본 스토리지 계정 종류가 'Storage'에서 'StorageV2'로 변경됩니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-673">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="e94b5-674">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="e94b5-674">New-AzStorageAccount</span></span>
* <span data-ttu-id="e94b5-675">'StandardLRS'가 'Standard_LRS'로 변경되는 것과 같이 '-'을 추가하여 입력 SkuName과 정렬되도록 스토리지 계정 cmdlet 출력 Sku.Name을 변경합니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-675">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="e94b5-676">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="e94b5-676">New-AzStorageAccount</span></span>
    - <span data-ttu-id="e94b5-677">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="e94b5-677">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="e94b5-678">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="e94b5-678">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="e94b5-679">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="e94b5-679">Az.Websites</span></span>
* <span data-ttu-id="e94b5-680">Get-AzWebApp에서 반환한 PSSite 개체에 대해 'Kind'속성이 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-680">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="e94b5-681">Get-AzWebApp\* 메트릭 및 Get-AzAppServicePlanMetrics가 사용되지 않음으로 표시되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-681">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="e94b5-682">1.8.0 - 2019년 4월</span><span class="sxs-lookup"><span data-stu-id="e94b5-682">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="e94b5-683">마지막 주 릴리스 이후의 주요 사항</span><span class="sxs-lookup"><span data-stu-id="e94b5-683">Highlights since the last major release</span></span>
* <span data-ttu-id="e94b5-684">`Az` 모듈 일반 공급</span><span class="sxs-lookup"><span data-stu-id="e94b5-684">General availability of `Az` module</span></span>
* <span data-ttu-id="e94b5-685">`Az` 모듈에 대한 자세한 내용은 https://aka.ms/azps-announce 를 방문하세요.</span><span class="sxs-lookup"><span data-stu-id="e94b5-685">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="e94b5-686">Location, ResourceGroup 및 ResourceName 완성자가 추가되었습니다(https://azure.microsoft.com/blog/completers-in-azure-powershell/ ).</span><span class="sxs-lookup"><span data-stu-id="e94b5-686">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="e94b5-687">와일드카드 지원이 Az.Compute 및 Az.Network에 대한 Get cmdlet에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-687">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="e94b5-688">Windows PowerShell 5.1 전용 대화형 사용자 이름/암호 인증이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-688">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="e94b5-689">Python 2 Runbook 지원이 Az.Automation에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-689">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="e94b5-690">Az.LogicApp: 통합 계정 어셈블리 및 일괄 처리 구성을 위한 새로운 cmdlet입니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-690">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="e94b5-691">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e94b5-691">Az.Accounts</span></span>
* <span data-ttu-id="e94b5-692">Mac에서 모듈을 올바르게 삭제하기 위해 Uninstall-AzureRm을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-692">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="e94b5-693">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="e94b5-693">Az.Batch</span></span>
* <span data-ttu-id="e94b5-694">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-694">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="e94b5-695">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="e94b5-695">Az.Cdn</span></span>
* <span data-ttu-id="e94b5-696">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-696">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="e94b5-697">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="e94b5-697">Az.CognitiveServices</span></span>
* <span data-ttu-id="e94b5-698">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-698">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e94b5-699">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e94b5-699">Az.Compute</span></span>
* <span data-ttu-id="e94b5-700">디스크의 리소스 ID에 리소스 ID의 소문자 resourcegroups가 있는 경우 AEM 설치 문제 수정</span><span class="sxs-lookup"><span data-stu-id="e94b5-700">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="e94b5-701">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-701">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="e94b5-702">와일드 카드에 대한 설명서 수정</span><span class="sxs-lookup"><span data-stu-id="e94b5-702">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="e94b5-703">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="e94b5-703">Az.DataFactory</span></span>
* <span data-ttu-id="e94b5-704">NodeCount가 관리형 통합 런타임에 대해 Null이 아닌 경우 SsisProperties를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-704">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="e94b5-705">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="e94b5-705">Az.DataLakeStore</span></span>
* <span data-ttu-id="e94b5-706">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-706">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="e94b5-707">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="e94b5-707">Az.EventGrid</span></span>
* <span data-ttu-id="e94b5-708">이벤트 구독 cmdlet 만들기/업데이트를 사용하기 전에 리소스를 만들어야 함을 나타내기 위해 엔드포인트의 도움말 텍스트가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-708">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="e94b5-709">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="e94b5-709">Az.EventHub</span></span>
* <span data-ttu-id="e94b5-710">네임스페이스의 NetworkRuleSet에 대한 새 cmdlet가 추가되었습니다</span><span class="sxs-lookup"><span data-stu-id="e94b5-710">Added new cmdlets for NetworkRuleSet of Namespace</span></span> 

#### <a name="azhdinsight"></a><span data-ttu-id="e94b5-711">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="e94b5-711">Az.HDInsight</span></span>
* <span data-ttu-id="e94b5-712">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-712">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="e94b5-713">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="e94b5-713">Az.IotHub</span></span>
* <span data-ttu-id="e94b5-714">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-714">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="e94b5-715">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="e94b5-715">Az.KeyVault</span></span>
* <span data-ttu-id="e94b5-716">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-716">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="e94b5-717">와일드 카드에 대한 설명서 수정</span><span class="sxs-lookup"><span data-stu-id="e94b5-717">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="e94b5-718">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="e94b5-718">Az.MachineLearning</span></span>
* <span data-ttu-id="e94b5-719">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-719">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="e94b5-720">Az.Media</span><span class="sxs-lookup"><span data-stu-id="e94b5-720">Az.Media</span></span>
* <span data-ttu-id="e94b5-721">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-721">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="e94b5-722">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="e94b5-722">Az.Monitor</span></span>
  * <span data-ttu-id="e94b5-723">GenV2(비 클래식) 메트릭 기반 경고 규칙에 대한 새 cmdlet</span><span class="sxs-lookup"><span data-stu-id="e94b5-723">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="e94b5-724">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="e94b5-724">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="e94b5-725">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="e94b5-725">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="e94b5-726">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="e94b5-726">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="e94b5-727">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="e94b5-727">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="e94b5-728">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="e94b5-728">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="e94b5-729">모니터 SDK가 버전 0.22.0-preview로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-729">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e94b5-730">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e94b5-730">Az.Network</span></span>
* <span data-ttu-id="e94b5-731">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-731">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="e94b5-732">와일드 카드에 대한 설명서 수정</span><span class="sxs-lookup"><span data-stu-id="e94b5-732">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="e94b5-733">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="e94b5-733">Az.NotificationHubs</span></span>
* <span data-ttu-id="e94b5-734">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-734">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="e94b5-735">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="e94b5-735">Az.OperationalInsights</span></span>
* <span data-ttu-id="e94b5-736">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-736">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="e94b5-737">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="e94b5-737">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="e94b5-738">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-738">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="e94b5-739">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="e94b5-739">Az.RecoveryServices</span></span>
* <span data-ttu-id="e94b5-740">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-740">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="e94b5-741">Azure VM의 SQL용 테이블 형식이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-741">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="e94b5-742">AzureFileShare에서 위치를 가져오는 대체 메서드가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-742">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="e94b5-743">시간대에 따라 SchedulePolicy 개체의 ScheduleRunDays가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-743">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="e94b5-744">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="e94b5-744">Az.RedisCache</span></span>
* <span data-ttu-id="e94b5-745">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-745">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="e94b5-746">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e94b5-746">Az.Resources</span></span>
* <span data-ttu-id="e94b5-747">와일드 카드에 대한 설명서 수정</span><span class="sxs-lookup"><span data-stu-id="e94b5-747">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="e94b5-748">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e94b5-748">Az.Sql</span></span>
* <span data-ttu-id="e94b5-749">Monitor SDK의 종속성을 공용 코드로 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-749">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="e94b5-750">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-750">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="e94b5-751">다중 열 분류 프로세스가 향상되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-751">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="e94b5-752">기본적으로 Get-AzSqlServerServiceObjective의 응답으로 SKU 속성(SKU 이름, 제품군, 용량)과 테이블 형식을 포함합니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-752">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="e94b5-753">해당 지역에 기존 서버 없이 위치별로 Get-AzSqlServerServiceObjective를 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-753">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="e94b5-754">관리형 인스턴스 생성 시 표준 시간대 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-754">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="e94b5-755">와일드 카드에 대한 설명서 수정</span><span class="sxs-lookup"><span data-stu-id="e94b5-755">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="e94b5-756">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="e94b5-756">Az.Websites</span></span>
* <span data-ttu-id="e94b5-757">실행 시 태그를 제거하지 않도록 Set-AzWebApp 및 Set-AzWebAppSlot를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-757">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="e94b5-758">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-758">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="e94b5-759">WebSites SDK가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-759">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="e94b5-760">PSAppServicePlan에서 AdminSiteName 속성을 제거했습니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-760">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="e94b5-761">1.7.0 - 2019년 4월</span><span class="sxs-lookup"><span data-stu-id="e94b5-761">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="e94b5-762">마지막 주 릴리스 이후의 주요 사항</span><span class="sxs-lookup"><span data-stu-id="e94b5-762">Highlights since the last major release</span></span>
* <span data-ttu-id="e94b5-763">`Az` 모듈 일반 공급</span><span class="sxs-lookup"><span data-stu-id="e94b5-763">General availability of `Az` module</span></span>
* <span data-ttu-id="e94b5-764">`Az` 모듈에 대한 자세한 내용은 https://aka.ms/azps-announce 를 방문하세요.</span><span class="sxs-lookup"><span data-stu-id="e94b5-764">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="e94b5-765">Location, ResourceGroup 및 ResourceName 완성자가 추가되었습니다(https://azure.microsoft.com/blog/completers-in-azure-powershell/ ).</span><span class="sxs-lookup"><span data-stu-id="e94b5-765">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="e94b5-766">와일드카드 지원이 Az.Compute 및 Az.Network에 대한 Get cmdlet에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-766">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="e94b5-767">Windows PowerShell 5.1 전용 대화형 사용자 이름/암호 인증이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-767">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="e94b5-768">Python 2 Runbook 지원이 Az.Automation에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-768">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="e94b5-769">Az.LogicApp: 통합 계정 어셈블리 및 일괄 처리 구성을 위한 새로운 cmdlet입니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-769">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="e94b5-770">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e94b5-770">Az.Accounts</span></span>
* <span data-ttu-id="e94b5-771">매개 변수 AzureAnalysisServicesEndpointResourceId를 허용하도록 Add-AzEnvironment 및 Set-AzEnvironment 업데이트</span><span class="sxs-lookup"><span data-stu-id="e94b5-771">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="e94b5-772">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="e94b5-772">Az.AnalysisServices</span></span>
* <span data-ttu-id="e94b5-773">데이터 평면 cmdlet에서 ServiceClient 사용 및 원본 인증 논리 제거</span><span class="sxs-lookup"><span data-stu-id="e94b5-773">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="e94b5-774">호환성이 손상되는 변경을 방지하기 위해 Add-AzureASAccount를 Connect-AzAccount의 래퍼로 만듦</span><span class="sxs-lookup"><span data-stu-id="e94b5-774">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="e94b5-775">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="e94b5-775">Az.Automation</span></span>
* <span data-ttu-id="e94b5-776">포함에 대한 New-AzAutomationSoftwareUpdateConfiguration cmdlet 버그 수정</span><span class="sxs-lookup"><span data-stu-id="e94b5-776">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="e94b5-777">이제 매개 변수 IncludedKbNumber 및 IncludedPackageNameMask가 작동함</span><span class="sxs-lookup"><span data-stu-id="e94b5-777">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="e94b5-778">Azure 자동화 업데이트 관리 동적 그룹에 대한 버그 수정</span><span class="sxs-lookup"><span data-stu-id="e94b5-778">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e94b5-779">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e94b5-779">Az.Compute</span></span>
* <span data-ttu-id="e94b5-780">New-AzDiskConfig 및 New-AzSnapshotConfig에 HyperVGeneration 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="e94b5-780">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="e94b5-781">다른 테넌트의 갤러리 이미지를 사용하여 VM을 만들 수 있음</span><span class="sxs-lookup"><span data-stu-id="e94b5-781">Allow VM creation with galley image from other tenants.</span></span> 

#### <a name="azcontainerinstance"></a><span data-ttu-id="e94b5-782">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="e94b5-782">Az.ContainerInstance</span></span>
* <span data-ttu-id="e94b5-783">후행 빈 인수를 추가한 New-AzContainerGroup의 -Command 매개 변수의 문제 수정</span><span class="sxs-lookup"><span data-stu-id="e94b5-783">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="e94b5-784">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="e94b5-784">Az.DataFactory</span></span>
* <span data-ttu-id="e94b5-785">ADF .Net SDK 버전을 3.0.2로 업데이트</span><span class="sxs-lookup"><span data-stu-id="e94b5-785">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="e94b5-786">RepoConfiguration 관련 설정에 대한 추가 매개 변수로 Set-AzDataFactoryV2 cmdlet을 업데이트</span><span class="sxs-lookup"><span data-stu-id="e94b5-786">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="e94b5-787">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e94b5-787">Az.Resources</span></span>
* <span data-ttu-id="e94b5-788">'-ResourceId' 또는 '-ResourceGroupName', '-Name' 및 '-ResourceType' 매개 변수를 제공할 때 'Get-AzResource'에 대한 공급자 처리 개선</span><span class="sxs-lookup"><span data-stu-id="e94b5-788">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="e94b5-789">'Test-AzDeployment' 및 'Test-AzResourceGroupDeployment'에 대한 오류 처리 개선</span><span class="sxs-lookup"><span data-stu-id="e94b5-789">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="e94b5-790">배포 유효성 검사 외부에서 발생한 오류를 처리하고 그 대신 명령의 출력에 포함</span><span class="sxs-lookup"><span data-stu-id="e94b5-790">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="e94b5-791">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/6856 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="e94b5-791">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="e94b5-792">배포 cmdlet 세트에 스크립트 및 작업 시나리오에서 프롬프트를 건너뛰는 '-IgnoreDynamicParameters' 스위치 추가</span><span class="sxs-lookup"><span data-stu-id="e94b5-792">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="e94b5-793">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/6856 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="e94b5-793">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="e94b5-794">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e94b5-794">Az.Sql</span></span>
* <span data-ttu-id="e94b5-795">데이터베이스 데이터 분류 지원</span><span class="sxs-lookup"><span data-stu-id="e94b5-795">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="e94b5-796">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="e94b5-796">Az.Storage</span></span>
* <span data-ttu-id="e94b5-797">매개 변수 -UseConnectedAccount를 사용하여 스토리지 컨텍스트를 만들 때 자세한 오류 보고(단, 로그인 Azure 계정 없이)</span><span class="sxs-lookup"><span data-stu-id="e94b5-797">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="e94b5-798">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="e94b5-798">New-AzStorageContext</span></span>
* <span data-ttu-id="e94b5-799">관리 평면 API를 사용하여 지정한 스토리지 계정의 BLOB 서비스 속성 관리 지원</span><span class="sxs-lookup"><span data-stu-id="e94b5-799">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="e94b5-800">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="e94b5-800">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="e94b5-801">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="e94b5-801">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="e94b5-802">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="e94b5-802">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="e94b5-803">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="e94b5-803">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="e94b5-804">BLOB 및 파일 업로드/다운로드 cmdlet에 대한 -AsJob 지원</span><span class="sxs-lookup"><span data-stu-id="e94b5-804">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="e94b5-805">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="e94b5-805">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="e94b5-806">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="e94b5-806">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="e94b5-807">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="e94b5-807">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="e94b5-808">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="e94b5-808">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="e94b5-809">1.6.0 - 2019년 3월</span><span class="sxs-lookup"><span data-stu-id="e94b5-809">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="e94b5-810">마지막 주 릴리스 이후의 주요 사항</span><span class="sxs-lookup"><span data-stu-id="e94b5-810">Highlights since the last major release</span></span>
* <span data-ttu-id="e94b5-811">`Az` 모듈 일반 공급</span><span class="sxs-lookup"><span data-stu-id="e94b5-811">General availability of `Az` module</span></span>
* <span data-ttu-id="e94b5-812">`Az` 모듈에 대한 자세한 내용은 https://aka.ms/azps-announce 를 방문하세요.</span><span class="sxs-lookup"><span data-stu-id="e94b5-812">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="e94b5-813">Location, ResourceGroup 및 ResourceName 완성자가 추가되었습니다(https://azure.microsoft.com/blog/completers-in-azure-powershell/ ).</span><span class="sxs-lookup"><span data-stu-id="e94b5-813">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="e94b5-814">와일드카드 지원이 Az.Compute 및 Az.Network에 대한 Get cmdlet에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-814">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="e94b5-815">Windows PowerShell 5.1 전용 대화형 사용자 이름/암호 인증이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-815">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="e94b5-816">Python 2 Runbook 지원이 Az.Automation에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-816">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="e94b5-817">Az.LogicApp: 통합 계정 어셈블리 및 일괄 처리 구성을 위한 새로운 cmdlet입니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-817">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="e94b5-818">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="e94b5-818">Az.Automation</span></span>
* <span data-ttu-id="e94b5-819">Azure 자동화 업데이트 관리에서 변경된 지원 기능은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-819">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="e94b5-820">동적 그룹화</span><span class="sxs-lookup"><span data-stu-id="e94b5-820">Dynamic grouping</span></span>
    * <span data-ttu-id="e94b5-821">사전 스크립트</span><span class="sxs-lookup"><span data-stu-id="e94b5-821">Pre-Post script</span></span>
    * <span data-ttu-id="e94b5-822">다시 부팅 설정</span><span class="sxs-lookup"><span data-stu-id="e94b5-822">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e94b5-823">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e94b5-823">Az.Compute</span></span>
* <span data-ttu-id="e94b5-824">Get-AzVmBootDiagnosticsData의 경로 확인 문제가 해결되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-824">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="e94b5-825">Compute 클라이언트 라이브러리가 25.0.0으로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-825">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="e94b5-826">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="e94b5-826">Az.KeyVault</span></span>
* <span data-ttu-id="e94b5-827">와일드카드 지원이 KeyVault cmdlet에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-827">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e94b5-828">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e94b5-828">Az.Network</span></span>
* <span data-ttu-id="e94b5-829">Azure Firewall에 대한 위협 인텔리전스 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-829">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="e94b5-830">Application Gateway 방화벽 정책의 최상위 수준 리소스 및 사용자 지정 규칙이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-830">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="e94b5-831">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="e94b5-831">Az.RecoveryServices</span></span>
* <span data-ttu-id="e94b5-832">인스턴트 RP를 지원하기 위해 SnapshotRetentionInDays가 Azure VM 정책에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-832">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="e94b5-833">컨테이너 등록을 취소하는 파이프 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-833">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="e94b5-834">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e94b5-834">Az.Resources</span></span>
* <span data-ttu-id="e94b5-835">Get-AzResource 및 Get-AzResourceGroup에 대한 와일드카드 지원을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-835">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="e94b5-836">ARM에 대한 일반 호출을 수행할 때 사용되는 자격 증명을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-836">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="e94b5-837">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e94b5-837">Az.Sql</span></span>
* <span data-ttu-id="e94b5-838">위협 탐지의 cmdlet 매개 변수(ExcludeDetectionType)가 DetectionType에서 string[]으로 변경되어 새 DetectionType이 추가되면 이후의 증명이 되고 자동 완성도 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-838">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="e94b5-839">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="e94b5-839">Az.Storage</span></span>
* <span data-ttu-id="e94b5-840">스토리지 계정에 대한 관리 정책 가져오기/설정/제거를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-840">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="e94b5-841">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="e94b5-841">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="e94b5-842">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="e94b5-842">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="e94b5-843">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="e94b5-843">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="e94b5-844">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="e94b5-844">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="e94b5-845">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="e94b5-845">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="e94b5-846">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="e94b5-846">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="e94b5-847">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="e94b5-847">Az.Websites</span></span>
* <span data-ttu-id="e94b5-848">'New-AzWebApp -IncludeSourceWebAppSlots'를 사용하여 모든 슬롯의 복제를 중단하는 ARM 템플릿 버그가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-848">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span> 

## <a name="150---march-2019"></a><span data-ttu-id="e94b5-849">1.5.0 - 2019년 3월</span><span class="sxs-lookup"><span data-stu-id="e94b5-849">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="e94b5-850">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e94b5-850">Az.Accounts</span></span>
* <span data-ttu-id="e94b5-851">'Register-AzModule' 명령을 추가하여 AutoRest 생성 cmdlet을 지원</span><span class="sxs-lookup"><span data-stu-id="e94b5-851">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="e94b5-852">Connect-AzAccount 예제 업데이트</span><span class="sxs-lookup"><span data-stu-id="e94b5-852">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="e94b5-853">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="e94b5-853">Az.Automation</span></span>
* <span data-ttu-id="e94b5-854">몇몇 Azure Automation cmdlet에서 특정 월별 일정을 검색할 때 발생하는 문제 수정</span><span class="sxs-lookup"><span data-stu-id="e94b5-854">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="e94b5-855">상위 20개 노드를 반환하도록 Get-AzAutomationDscNode를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-855">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="e94b5-856">이제 모든 노드 반환</span><span class="sxs-lookup"><span data-stu-id="e94b5-856">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="e94b5-857">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="e94b5-857">Az.Cdn</span></span>
* <span data-ttu-id="e94b5-858">사용자 지정 도메인 Https 사용/사용 안 함에 대한 새 Powershell cmdlet이 추가되었으며 기존의 것은 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-858">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e94b5-859">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e94b5-859">Az.Compute</span></span>
* <span data-ttu-id="e94b5-860">Get cmdlet에 와일드 카드 지원 추가</span><span class="sxs-lookup"><span data-stu-id="e94b5-860">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="e94b5-861">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="e94b5-861">Az.DataFactory</span></span>
* <span data-ttu-id="e94b5-862">ADF.Net SDK 버전이 3.0.1로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-862">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="e94b5-863">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="e94b5-863">Az.LogicApp</span></span>
* <span data-ttu-id="e94b5-864">첫 결과 페이지 검색 시에만 ListWorkflows 수정</span><span class="sxs-lookup"><span data-stu-id="e94b5-864">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e94b5-865">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e94b5-865">Az.Network</span></span>
* <span data-ttu-id="e94b5-866">Network cmdlet에 와일드 카드 지원 추가</span><span class="sxs-lookup"><span data-stu-id="e94b5-866">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="e94b5-867">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="e94b5-867">Az.RecoveryServices</span></span>
* <span data-ttu-id="e94b5-868">Azure VM 지원에 SQL 서버가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-868">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="e94b5-869">SDK 업데이트</span><span class="sxs-lookup"><span data-stu-id="e94b5-869">SDK Update</span></span>
* <span data-ttu-id="e94b5-870">VMappContainer 체크 인 Get-ProtectableItem 제거</span><span class="sxs-lookup"><span data-stu-id="e94b5-870">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="e94b5-871">Get ProtectableItem의 매개 변수로 Name과 ServerName이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-871">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="e94b5-872">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e94b5-872">Az.Resources</span></span>
* <span data-ttu-id="e94b5-873">`-TemplateObject` 매개 변수를 추가하여 cmdlet을 배포</span><span class="sxs-lookup"><span data-stu-id="e94b5-873">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="e94b5-874">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/2933 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="e94b5-874">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="e94b5-875">`Get-AzResource`의 결과를 `Set-AzResource`(으)로 파이프할 때 발생하는 문제 수정</span><span class="sxs-lookup"><span data-stu-id="e94b5-875">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="e94b5-876">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/8240 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="e94b5-876">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="e94b5-877">실행 시 JSON 데이터 형식 문제 해결 `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="e94b5-877">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="e94b5-878">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/7930 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="e94b5-878">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="e94b5-879">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e94b5-879">Az.Sql</span></span>
* <span data-ttu-id="e94b5-880">AuditingEndpointsCommunicator를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-880">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="e94b5-881">새 진단 설정을 생성할 때 에지 사례의 동작을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-881">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="e94b5-882">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="e94b5-882">Az.Storage</span></span>
* <span data-ttu-id="e94b5-883">스토리지 계정      - New-AzStorageAccount를 생성할 때 종류 BlockBlobStorage를 지원</span><span class="sxs-lookup"><span data-stu-id="e94b5-883">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="e94b5-884">1.4.0 - 2019년 2월</span><span class="sxs-lookup"><span data-stu-id="e94b5-884">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="e94b5-885">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="e94b5-885">Az.AnalysisServices</span></span>
* <span data-ttu-id="e94b5-886">사용되지 않는 AddAzureASAccount cmdlet</span><span class="sxs-lookup"><span data-stu-id="e94b5-886">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="e94b5-887">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="e94b5-887">Az.Automation</span></span>
* <span data-ttu-id="e94b5-888">Import-AzAutomationDscNodeConfiguration 도움말 업데이트</span><span class="sxs-lookup"><span data-stu-id="e94b5-888">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="e94b5-889">Import-AzAutomationDscConfiguration cmdlet 구성 이름 유효성 검사 추가</span><span class="sxs-lookup"><span data-stu-id="e94b5-889">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="e94b5-890">Import-AzAutomationDscConfiguration cmdlet 오류 처리 개선</span><span class="sxs-lookup"><span data-stu-id="e94b5-890">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="e94b5-891">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="e94b5-891">Az.CognitiveServices</span></span>
* <span data-ttu-id="e94b5-892">리소스의 하위 도메인을 지정하는 데 사용되는 New-AzCognitiveServicesAccount에 대한 새 선택적 매개 변수로 CustomSubdomainName이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-892">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e94b5-893">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e94b5-893">Az.Compute</span></span>
* <span data-ttu-id="e94b5-894">ID 매개 변수 집합 문제 해결</span><span class="sxs-lookup"><span data-stu-id="e94b5-894">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="e94b5-895">Name 매개 변수를 제공하지 않으면 Get-AzVMExtension이 설치된 모든 확장을 열거하도록 업데이트</span><span class="sxs-lookup"><span data-stu-id="e94b5-895">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="e94b5-896">Update-AzImage cmdlet에 태그 및 ResourceId 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="e94b5-896">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="e94b5-897">인스턴스 ID가 없는 Get-AzVmssVM과 InstanceView를 사용하면 인스턴스 보기가 있는 VMSS VM을 나열할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-897">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="e94b5-898">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="e94b5-898">Az.DataLakeStore</span></span>
* <span data-ttu-id="e94b5-899">ADL 삭제된 항목 열거 및 복원에 대한 cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="e94b5-899">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="e94b5-900">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="e94b5-900">Az.EventHub</span></span>
* <span data-ttu-id="e94b5-901">Eventhub의 CaptureDescription 클래스에서 빈 보관을 건너뛰는 새 부울 속성 SkipEmptyArchives가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-901">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span> 

#### <a name="azkeyvault"></a><span data-ttu-id="e94b5-902">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="e94b5-902">Az.KeyVault</span></span>
* <span data-ttu-id="e94b5-903">Set-AzKeyVaultSecret 태그 지정 수정</span><span class="sxs-lookup"><span data-stu-id="e94b5-903">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="e94b5-904">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="e94b5-904">Az.LogicApp</span></span>
* <span data-ttu-id="e94b5-905">통합 계정에 대한 기본 sku 추가</span><span class="sxs-lookup"><span data-stu-id="e94b5-905">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="e94b5-906">XSLT 2.0, XSLT 3.0, Liquid 맵 형식 추가</span><span class="sxs-lookup"><span data-stu-id="e94b5-906">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="e94b5-907">통합 계정 어셈블리에 대한 새 cmdlet</span><span class="sxs-lookup"><span data-stu-id="e94b5-907">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="e94b5-908">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="e94b5-908">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="e94b5-909">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="e94b5-909">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="e94b5-910">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="e94b5-910">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="e94b5-911">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="e94b5-911">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="e94b5-912">통합 계정 일괄 처리 구성에 대한 새 cmdlet</span><span class="sxs-lookup"><span data-stu-id="e94b5-912">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="e94b5-913">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="e94b5-913">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="e94b5-914">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="e94b5-914">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="e94b5-915">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="e94b5-915">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="e94b5-916">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="e94b5-916">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="e94b5-917">논리 앱 SDK를 버전 4.1.0으로 업데이트</span><span class="sxs-lookup"><span data-stu-id="e94b5-917">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="e94b5-918">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="e94b5-918">Az.Monitor</span></span>
* <span data-ttu-id="e94b5-919">Get-AzMetric에 대한 도움말 업데이트</span><span class="sxs-lookup"><span data-stu-id="e94b5-919">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e94b5-920">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e94b5-920">Az.Network</span></span>
* <span data-ttu-id="e94b5-921">Add-AzApplicationGatewayCustomError에 대한 도움말 예제 업데이트</span><span class="sxs-lookup"><span data-stu-id="e94b5-921">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="e94b5-922">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="e94b5-922">Az.OperationalInsights</span></span>
* <span data-ttu-id="e94b5-923">New 및 Get ApplicationInsights 데이터 소스에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="e94b5-923">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="e94b5-924">지정된 작업 영역에 대한 특정 또는 전체 ApplicationInsights 데이터 원본 가져오기를 지원하기 위한 새로운 'ApplicationInsights' 종류가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-924">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span> 
    - <span data-ttu-id="e94b5-925">지정된 Application-Insights 리소스 매개 변수(구독 ID, resourceGroupName 및 이름)별로 데이터 원본을 만들기 위한 New-AzOperationalInsightsApplicationInsightsDataSource cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-925">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span> 

#### <a name="azresources"></a><span data-ttu-id="e94b5-926">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e94b5-926">Az.Resources</span></span>
* <span data-ttu-id="e94b5-927">문제 https://github.com/Azure/azure-powershell/issues/8166 수정</span><span class="sxs-lookup"><span data-stu-id="e94b5-927">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="e94b5-928">문제 https://github.com/Azure/azure-powershell/issues/8235 수정</span><span class="sxs-lookup"><span data-stu-id="e94b5-928">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="e94b5-929">문제 https://github.com/Azure/azure-powershell/issues/6219 수정</span><span class="sxs-lookup"><span data-stu-id="e94b5-929">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="e94b5-930">KeyCredentials 반복 만들기를 방지하기 위해 버그 수정</span><span class="sxs-lookup"><span data-stu-id="e94b5-930">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="e94b5-931">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e94b5-931">Az.Sql</span></span>
* <span data-ttu-id="e94b5-932">SQL DB 하이퍼스케일에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="e94b5-932">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="e94b5-933">복원 요청에서 불필요한 속성을 설정하여 복원이 실패할 수 있는 버그 수정</span><span class="sxs-lookup"><span data-stu-id="e94b5-933">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="e94b5-934">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="e94b5-934">Az.Websites</span></span>
* <span data-ttu-id="e94b5-935">Get-AzWebAppSlotMetrics 내 올바른 예제</span><span class="sxs-lookup"><span data-stu-id="e94b5-935">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="e94b5-936">1.3.0 - 2019년 2월</span><span class="sxs-lookup"><span data-stu-id="e94b5-936">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="e94b5-937">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e94b5-937">Az.Accounts</span></span>
* <span data-ttu-id="e94b5-938">ClientRuntime 최신 버전 업데이트</span><span class="sxs-lookup"><span data-stu-id="e94b5-938">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="e94b5-939">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="e94b5-939">Az.AnalysisServices</span></span>
<span data-ttu-id="e94b5-940">Az.AnalysisServices 모듈의 전반적인 가용성.</span><span class="sxs-lookup"><span data-stu-id="e94b5-940">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e94b5-941">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e94b5-941">Az.Compute</span></span>
* <span data-ttu-id="e94b5-942">AEM 확장: UltraSSD 및 P60, P70, P80 디스크에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="e94b5-942">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="e94b5-943">Set-AzVMBootDiagnostics에 대한 도움말 업데이트</span><span class="sxs-lookup"><span data-stu-id="e94b5-943">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="e94b5-944">Update-AzImage에 대한 도움말 및 예제 업데이트</span><span class="sxs-lookup"><span data-stu-id="e94b5-944">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="e94b5-945">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="e94b5-945">Az.RecoveryServices</span></span>
<span data-ttu-id="e94b5-946">Az.RecoveryServices 모듈의 전반적인 가용성.</span><span class="sxs-lookup"><span data-stu-id="e94b5-946">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="e94b5-947">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e94b5-947">Az.Resources</span></span>
* <span data-ttu-id="e94b5-948">리소스 그룹 관련 태그 수정</span><span class="sxs-lookup"><span data-stu-id="e94b5-948">Fix tagging for resource groups</span></span> 
    - <span data-ttu-id="e94b5-949">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/8166 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="e94b5-949">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="e94b5-950">`Get-AzureRmRoleAssignment`이(가) -ErrorAction을 준수하지 않는 문제 수정</span><span class="sxs-lookup"><span data-stu-id="e94b5-950">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span> 
    - <span data-ttu-id="e94b5-951">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/8235 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="e94b5-951">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="e94b5-952">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e94b5-952">Az.Sql</span></span>
* <span data-ttu-id="e94b5-953">AzSqlDatabaseBackupShortTermRetentionPolicy 가져오기/설정하기 추가</span><span class="sxs-lookup"><span data-stu-id="e94b5-953">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="e94b5-954">SQL cmdlet을 실행할 경우 Azure 계정에 로그인되어 있지 않은 것이 nullref 예외를 초래하는 문제 수정</span><span class="sxs-lookup"><span data-stu-id="e94b5-954">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="e94b5-955">Get-AzSqlCapability의 nullref 예외 수정</span><span class="sxs-lookup"><span data-stu-id="e94b5-955">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="e94b5-956">1.2.1 - 2019년 1월</span><span class="sxs-lookup"><span data-stu-id="e94b5-956">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="e94b5-957">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e94b5-957">Az.Accounts</span></span>
* <span data-ttu-id="e94b5-958">올바른 인증 버전을 사용하여 릴리스</span><span class="sxs-lookup"><span data-stu-id="e94b5-958">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="e94b5-959">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="e94b5-959">Az.AnalysisServices</span></span>
* <span data-ttu-id="e94b5-960">업데이트된 인증 종속성을 사용하여 릴리스</span><span class="sxs-lookup"><span data-stu-id="e94b5-960">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="e94b5-961">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="e94b5-961">Az.RecoveryServices</span></span>
* <span data-ttu-id="e94b5-962">업데이트된 인증 종속성을 사용하여 릴리스</span><span class="sxs-lookup"><span data-stu-id="e94b5-962">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="e94b5-963">1.2.0 - 2019년 1월</span><span class="sxs-lookup"><span data-stu-id="e94b5-963">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="e94b5-964">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e94b5-964">Az.Accounts</span></span>
* <span data-ttu-id="e94b5-965">Windows PowerShell 5.1 전용 대화형 사용자 이름/암호 인증 추가</span><span class="sxs-lookup"><span data-stu-id="e94b5-965">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="e94b5-966">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="e94b5-966">Update incorrect online help URLs</span></span>
* <span data-ttu-id="e94b5-967">Uninstall-AzureRm 관련 PS Core에 경고 메시지 추가</span><span class="sxs-lookup"><span data-stu-id="e94b5-967">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="e94b5-968">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="e94b5-968">Az.Aks</span></span>
* <span data-ttu-id="e94b5-969">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="e94b5-969">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="e94b5-970">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="e94b5-970">Az.Automation</span></span>
* <span data-ttu-id="e94b5-971">Python 2 Runbook에 대한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-971">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="e94b5-972">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="e94b5-972">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="e94b5-973">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="e94b5-973">Az.Cdn</span></span>
* <span data-ttu-id="e94b5-974">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="e94b5-974">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e94b5-975">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e94b5-975">Az.Compute</span></span>
* <span data-ttu-id="e94b5-976">Invoke-AzVMReimage cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="e94b5-976">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="e94b5-977">Set-AzVmss에 TempDisk 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="e94b5-977">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="e94b5-978">New-AzVM 경고 메시지 수정</span><span class="sxs-lookup"><span data-stu-id="e94b5-978">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="e94b5-979">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="e94b5-979">Az.ContainerRegistry</span></span>
* <span data-ttu-id="e94b5-980">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="e94b5-980">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="e94b5-981">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="e94b5-981">Az.DataFactory</span></span>
* <span data-ttu-id="e94b5-982">ADF.Net SDK 버전이 3.0.0으로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-982">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="e94b5-983">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="e94b5-983">Az.DataLakeStore</span></span>
* <span data-ttu-id="e94b5-984">MSI를 사용할 때 ADLS 엔드포인트 문제 수정</span><span class="sxs-lookup"><span data-stu-id="e94b5-984">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="e94b5-985">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/7462 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="e94b5-985">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="e94b5-986">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="e94b5-986">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="e94b5-987">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="e94b5-987">Az.IotHub</span></span>
* <span data-ttu-id="e94b5-988">Add-IotHubRoutingEndpoint cmdlet에 인코딩 형식을 추가하세요.</span><span class="sxs-lookup"><span data-stu-id="e94b5-988">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="e94b5-989">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="e94b5-989">Az.KeyVault</span></span>
* <span data-ttu-id="e94b5-990">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="e94b5-990">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e94b5-991">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e94b5-991">Az.Network</span></span>
* <span data-ttu-id="e94b5-992">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="e94b5-992">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="e94b5-993">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e94b5-993">Az.Resources</span></span>
* <span data-ttu-id="e94b5-994">'New-AzADAppCredential' 및 'New-AzADSpCredential' 참조 설명서의 잘못된 예제 수정</span><span class="sxs-lookup"><span data-stu-id="e94b5-994">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="e94b5-995">리소스 그룹 배포 cmdlet 실행 전 '-TemplateFile' 매개 변수 경로가 확인되지 않는 문제 수정</span><span class="sxs-lookup"><span data-stu-id="e94b5-995">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="e94b5-996">Az.Resources: New-AzureRmPolicyDefinition -Mode 기본값에 대한 올바른 설명서</span><span class="sxs-lookup"><span data-stu-id="e94b5-996">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="e94b5-997">Az.Resources: 문제 https://github.com/Azure/azure-powershell/issues/7522 수정</span><span class="sxs-lookup"><span data-stu-id="e94b5-997">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="e94b5-998">Az.Resources: 문제 https://github.com/Azure/azure-powershell/issues/5747 수정</span><span class="sxs-lookup"><span data-stu-id="e94b5-998">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="e94b5-999">'PSResourceGroupDeployment' 개체의 서식 문제 수정</span><span class="sxs-lookup"><span data-stu-id="e94b5-999">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="e94b5-1000">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/2123 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="e94b5-1000">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="e94b5-1001">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="e94b5-1001">Az.ServiceFabric</span></span>
* <span data-ttu-id="e94b5-1002">인증서가 VMSS 모델에 추가되었는데도 예외가 발생할 경우 롤백합니다. 이는 버그 https://github.com/Azure/service-fabric-issues/issues/932 를 수정하기 위함입니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-1002">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="e94b5-1003">일부 오류 메시지를 수정하세요.</span><span class="sxs-lookup"><span data-stu-id="e94b5-1003">Fix some error messages.</span></span>
* <span data-ttu-id="e94b5-1004">Az로의 마이그레이션을 통해서는 작동하지 않는 New-AzServiceFabriCluster를 위해 기본값 ARM 템플릿을 가진 클러스터 만들기를 수정하세요.</span><span class="sxs-lookup"><span data-stu-id="e94b5-1004">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="e94b5-1005">확장에서 클러스터 id를 확인하여 클러스터에 해당하는 VMSS에만 추가되도록 클러스터/애플리케이션 인증서 추가를 수정하세요.</span><span class="sxs-lookup"><span data-stu-id="e94b5-1005">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="e94b5-1006">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="e94b5-1006">Az.SignalR</span></span>
* <span data-ttu-id="e94b5-1007">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="e94b5-1007">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="e94b5-1008">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e94b5-1008">Az.Sql</span></span>
* <span data-ttu-id="e94b5-1009">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="e94b5-1009">Update incorrect online help URLs</span></span>
* <span data-ttu-id="e94b5-1010">가능한 값을 가진 LicenseType 매개 변수에 대한 매개 변수 설명이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-1010">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="e94b5-1011">유일하게 업데이트된 속성인데 작동하지 않는 관리되는 인스턴스 ID의 업데이트 수정</span><span class="sxs-lookup"><span data-stu-id="e94b5-1011">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="e94b5-1012">관리되는 인스턴스에서의 사용자 지정 데이터 정렬에 대한 지원</span><span class="sxs-lookup"><span data-stu-id="e94b5-1012">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="e94b5-1013">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="e94b5-1013">Az.Storage</span></span>
* <span data-ttu-id="e94b5-1014">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="e94b5-1014">Update incorrect online help URLs</span></span>
* <span data-ttu-id="e94b5-1015">Premium Storage 계정이 클래식 로깅/메트릭을 지원하지 않기 때문에, Premium Storage 계정의 클래식 로깅/메트릭을 가져올/설정할 때 상세한 오류 메시지를 제공해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-1015">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="e94b5-1016">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="e94b5-1016">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="e94b5-1017">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="e94b5-1017">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="e94b5-1018">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="e94b5-1018">Az.TrafficManager</span></span>
* <span data-ttu-id="e94b5-1019">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="e94b5-1019">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="e94b5-1020">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="e94b5-1020">Az.Websites</span></span>
* <span data-ttu-id="e94b5-1021">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="e94b5-1021">Update incorrect online help URLs</span></span>
* <span data-ttu-id="e94b5-1022">앱이 ASE에 호스팅되면 'New-AzWebAppSSLBinding'을 수정하여 올바른 resourcegroup+location에 인증서를 업로드합니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-1022">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="e94b5-1023">'New-AzWebAppSSLBinding'을 수정하여 SSL 인증서를 앱에 바인딩하는 데 붙는 태그를 덮어쓰지 않도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-1023">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="e94b5-1024">1.1.0 - 2019년 1월</span><span class="sxs-lookup"><span data-stu-id="e94b5-1024">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="e94b5-1025">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e94b5-1025">Az.Accounts</span></span>
* <span data-ttu-id="e94b5-1026">Enable-AzureRmAlias에 'Local' 범위 추가</span><span class="sxs-lookup"><span data-stu-id="e94b5-1026">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e94b5-1027">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e94b5-1027">Az.Compute</span></span>
* <span data-ttu-id="e94b5-1028">이름이 Restart/Start/Stop/Remove/Set-AzVM과 Save-AzVMImage에 설정된 ID 매개 변수에서 선택 사항이 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-1028">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="e94b5-1029">도움말 파일의 ID에 대한 설명이 업데이트 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-1029">Updated the description of ID in help files</span></span>
* <span data-ttu-id="e94b5-1030">Az.Accounts 모듈을 사용할 때의 이전 버전과의 호환성 문제를 해결합니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-1030">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="e94b5-1031">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="e94b5-1031">Az.DataLakeStore</span></span>
* <span data-ttu-id="e94b5-1032">SDK 수정을 위해 데이터 평면의 SDK 버전을 1.1.14로 업데이트하세요.</span><span class="sxs-lookup"><span data-stu-id="e94b5-1032">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="e94b5-1033">getfilestatus 및 liststatus에 대한 음수 acesstime 및 modificationtime 수정, 비동기 취소 토큰 수정</span><span class="sxs-lookup"><span data-stu-id="e94b5-1033">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="e94b5-1034">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="e94b5-1034">Az.EventGrid</span></span>
* <span data-ttu-id="e94b5-1035">2019-01-01 API 버전을 사용하도록 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-1035">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="e94b5-1036">2019-01-01 API 버전에서 새 시나리오를 지원하도록 다음 cmdlet을 업데이트</span><span class="sxs-lookup"><span data-stu-id="e94b5-1036">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="e94b5-1037">New-AzureRmEventGridSubscription: 지정을 위한 새로운 선택적 매개 변수를 추가</span><span class="sxs-lookup"><span data-stu-id="e94b5-1037">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="e94b5-1038">이벤트 Time-to-Live</span><span class="sxs-lookup"><span data-stu-id="e94b5-1038">Event Time-To-Live,</span></span>
        - <span data-ttu-id="e94b5-1039">이벤트에 대한 최대 배달 시도</span><span class="sxs-lookup"><span data-stu-id="e94b5-1039">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="e94b5-1040">배달 못한 편지의 엔드포인트입니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-1040">Dead letter endpoint.</span></span>
    - <span data-ttu-id="e94b5-1041">Update-AzureRmEventGridSubscription: 지정을 위한 새로운 선택적 매개 변수를 추가</span><span class="sxs-lookup"><span data-stu-id="e94b5-1041">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="e94b5-1042">이벤트 Time-to-Live</span><span class="sxs-lookup"><span data-stu-id="e94b5-1042">Event Time-To-Live,</span></span>
        - <span data-ttu-id="e94b5-1043">이벤트에 대한 최대 배달 시도</span><span class="sxs-lookup"><span data-stu-id="e94b5-1043">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="e94b5-1044">배달 못한 편지의 엔드포인트입니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-1044">Dead letter endpoint.</span></span>
* <span data-ttu-id="e94b5-1045">New-AzureRmEventGridSubscription 및 Update-AzureRmEventGridSubscription cmdlet의 EndpointType 옵션에 새 열거형 값(즉, storageQueue 및 hybridConnection)을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-1045">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="e94b5-1046">이벤트 구독을 생성 또는 업데이트할 때 사용자가 직접 조치를 취해야 할 경우 경고 메시지를 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-1046">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="e94b5-1047">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="e94b5-1047">Az.IotHub</span></span>
* <span data-ttu-id="e94b5-1048">최신 버전의 Azure IotHub SDK로 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="e94b5-1048">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="e94b5-1049">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="e94b5-1049">Az.LogicApp</span></span>
* <span data-ttu-id="e94b5-1050">지정된 이름이 없는 모든 Get-AzLogicApp 목록</span><span class="sxs-lookup"><span data-stu-id="e94b5-1050">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="e94b5-1051">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e94b5-1051">Az.Resources</span></span>
* <span data-ttu-id="e94b5-1052">'Get-AzResource'에 '-ODataQuery'및 '-ResourceId' 매개 변수를 제공할 때 매개 변수 집합 문제 수정</span><span class="sxs-lookup"><span data-stu-id="e94b5-1052">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="e94b5-1053">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/7875 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="e94b5-1053">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="e94b5-1054">New/Set-AzPolicyDefinition에서 -Custom 매개 변수 처리 문제 수정</span><span class="sxs-lookup"><span data-stu-id="e94b5-1054">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="e94b5-1055">New-AzDeployment 설명서에서 오타 수정</span><span class="sxs-lookup"><span data-stu-id="e94b5-1055">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="e94b5-1056">'New-AzADUser'에 '-MailNickname'매개 변수가 필수 항목으로 지정됨</span><span class="sxs-lookup"><span data-stu-id="e94b5-1056">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="e94b5-1057">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/8220 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="e94b5-1057">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="e94b5-1058">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="e94b5-1058">Az.SignalR</span></span>
* <span data-ttu-id="e94b5-1059">Az.Accounts 모듈을 사용할 때의 이전 버전과의 호환성 문제를 해결합니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-1059">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="e94b5-1060">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e94b5-1060">Az.Sql</span></span>
* <span data-ttu-id="e94b5-1061">Storage 관리 클라이언트 종속성을 일반적인 SDK 구현으로 변환했습니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-1061">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="e94b5-1062">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="e94b5-1062">Az.Storage</span></span>
* <span data-ttu-id="e94b5-1063">Sas Token, OAuth 또는 Anonymous를 사용하여 스토리지 컨텍스트의 StorageAccountName을 실제 스토리지 계정 이름으로 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-1063">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="e94b5-1064">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="e94b5-1064">New-AzStorageContext</span></span>
* <span data-ttu-id="e94b5-1065">'-FullUri' 매개 변수를 사용하여 Blob 스냅샷 개체의 Sas Token을 생성하고 반환된 Uri를 스냅샷 Uri로 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-1065">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="e94b5-1066">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="e94b5-1066">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="e94b5-1067">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="e94b5-1067">Az.Websites</span></span>
* <span data-ttu-id="e94b5-1068">'Get-AzDeletedWebApp'의 날짜 구문 분석 버그를 수정했습니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-1068">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="e94b5-1069">Az.Accounts 모듈을 사용할 때의 이전 버전과의 호환성 문제를 해결합니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-1069">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="e94b5-1070">1.0.0 - 2018년 12월</span><span class="sxs-lookup"><span data-stu-id="e94b5-1070">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="e94b5-1071">일반</span><span class="sxs-lookup"><span data-stu-id="e94b5-1071">General</span></span>

- <span data-ttu-id="e94b5-1072">Az 모듈 일반 공급</span><span class="sxs-lookup"><span data-stu-id="e94b5-1072">General Availability of Az Module</span></span>
- <span data-ttu-id="e94b5-1073">각 모듈에 대 한 온라인 도움말</span><span class="sxs-lookup"><span data-stu-id="e94b5-1073">Online help for each module</span></span>
- <span data-ttu-id="e94b5-1074">자세한 내용과 로드맵은 [Az 알림 페이지](https://aka.ms/azps-announce)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="e94b5-1074">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="e94b5-1075">AzureRM에서 마이그레이션하는 것에 대한 정보는 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="e94b5-1075">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="e94b5-1076">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e94b5-1076">Az.Accounts</span></span>
- <span data-ttu-id="e94b5-1077">Az.Profile에서 변경</span><span class="sxs-lookup"><span data-stu-id="e94b5-1077">Changed from Az.Profile</span></span>
- <span data-ttu-id="e94b5-1078">프로필 및 컨텍스트 형식에 대한 표 형식 수정</span><span class="sxs-lookup"><span data-stu-id="e94b5-1078">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="e94b5-1079">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="e94b5-1079">Az.ApiManagement</span></span>
- <span data-ttu-id="e94b5-1080">#7002에 대한 수정</span><span class="sxs-lookup"><span data-stu-id="e94b5-1080">Fixes for #7002</span></span>
- <span data-ttu-id="e94b5-1081">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="e94b5-1081">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="e94b5-1082">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="e94b5-1082">Az.Batch</span></span>
- <span data-ttu-id="e94b5-1083">`PSComputeNode`의 새로운 `NodeAgentInformation` 속성을 통해 풀의 각 VM에서 실행 중인 Azure Batch 노드 에이전트의 버전을 확인하는 기능이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-1083">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="e94b5-1084">`PSDataDisk`에 대한 `Caching` 기본 값은 이제 `None` 대신 `ReadWrite`입니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-1084">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="e94b5-1085">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="e94b5-1085">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="e94b5-1086">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="e94b5-1086">Az.Billing</span></span>
- <span data-ttu-id="e94b5-1087">청구, 소비 및 UsageAggregates cmdlet 결합 cmdlet에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="e94b5-1087">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="e94b5-1088">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="e94b5-1088">Az.CognitivServices</span></span>
- <span data-ttu-id="e94b5-1089">New-AzureRmCognitiveServicesAccount 작업에서 사용 가능한 SkuName 및 Typem에 대한 완성자 추가</span><span class="sxs-lookup"><span data-stu-id="e94b5-1089">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="e94b5-1090">Get-AzCognitiveServicesAccountSkus에서 GetSkusWithAccountParamSetName 매개 변수 집합을 제거</span><span class="sxs-lookup"><span data-stu-id="e94b5-1090">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="e94b5-1091">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="e94b5-1091">Az.ContainerInstance</span></span>
- <span data-ttu-id="e94b5-1092">ManagedIdentity 지원이 추가됨</span><span class="sxs-lookup"><span data-stu-id="e94b5-1092">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="e94b5-1093">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="e94b5-1093">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="e94b5-1094">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="e94b5-1094">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="e94b5-1095">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="e94b5-1095">Az.DataLakeStore</span></span>
- <span data-ttu-id="e94b5-1096">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="e94b5-1096">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="e94b5-1097">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="e94b5-1097">Az.Monitor</span></span>
- <span data-ttu-id="e94b5-1098">Az.Monitor 이름 변경 및 기타 사소한 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="e94b5-1098">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="e94b5-1099">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="e94b5-1099">Az.KeyVault</span></span>
- <span data-ttu-id="e94b5-1100">출력 형식에서 사용되지 않는 'PurgeDisabled' 속성 제거</span><span class="sxs-lookup"><span data-stu-id="e94b5-1100">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="e94b5-1101">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="e94b5-1101">Az.MachineLearning</span></span>
- <span data-ttu-id="e94b5-1102">Az.MachineLearningCompute 모듈의 cmdlet 포함</span><span class="sxs-lookup"><span data-stu-id="e94b5-1102">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="e94b5-1103">Az.Media</span><span class="sxs-lookup"><span data-stu-id="e94b5-1103">Az.Media</span></span>
- <span data-ttu-id="e94b5-1104">New-AzMediaService에서 사용되지 않는 -Tags 별칭이 제거됨</span><span class="sxs-lookup"><span data-stu-id="e94b5-1104">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="e94b5-1105">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e94b5-1105">Az.Network</span></span>
<span data-ttu-id="e94b5-1106">Application Gateway에서 RewriteRuleSets를 구성하는 것에 대한 지원이 추가됨</span><span class="sxs-lookup"><span data-stu-id="e94b5-1106">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="e94b5-1107">추가된 새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-1107">New cmdlets added:</span></span>
        - <span data-ttu-id="e94b5-1108">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="e94b5-1108">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="e94b5-1109">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="e94b5-1109">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="e94b5-1110">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="e94b5-1110">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="e94b5-1111">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="e94b5-1111">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="e94b5-1112">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="e94b5-1112">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="e94b5-1113">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="e94b5-1113">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="e94b5-1114">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="e94b5-1114">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="e94b5-1115">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="e94b5-1115">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="e94b5-1116">선택적 매개 변수를 사용하도록 cmdlet이 업데이트됨 -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="e94b5-1116">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="e94b5-1117">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e94b5-1117">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="e94b5-1118">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="e94b5-1118">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="e94b5-1119">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="e94b5-1119">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="e94b5-1120">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e94b5-1120">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="e94b5-1121">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="e94b5-1121">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="e94b5-1122">New-AzureRmApplicationGatewayUrlPathMapConfig로 ID를 사용하여 Application Gateway에 KeyVault 지원을 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-1122">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="e94b5-1123">선택적 매개 변수를 사용하도록 cmdlet이 업데이트됨 -KeyVaultSecretId, -KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="e94b5-1123">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="e94b5-1124">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="e94b5-1124">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="e94b5-1125">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="e94b5-1125">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="e94b5-1126">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="e94b5-1126">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="e94b5-1127">New-AzApplicationGateway cmdlet이 선택적 매개 변수를 사용하도록 업데이트됨 -UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="e94b5-1127">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="e94b5-1128">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="e94b5-1128">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="e94b5-1129">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="e94b5-1129">Az.OperationalInsights</span></span>
- <span data-ttu-id="e94b5-1130">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="e94b5-1130">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="e94b5-1131">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="e94b5-1131">Az.Profile</span></span>
- <span data-ttu-id="e94b5-1132">Az.Accounts에 모듈 이름이 변경됨</span><span class="sxs-lookup"><span data-stu-id="e94b5-1132">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="e94b5-1133">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="e94b5-1133">Az.RecoveryServices</span></span>
- <span data-ttu-id="e94b5-1134">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="e94b5-1134">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="e94b5-1135">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e94b5-1135">Az.Resources</span></span>
- <span data-ttu-id="e94b5-1136">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="e94b5-1136">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="e94b5-1137">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="e94b5-1137">Az.ServiceFabric</span></span>
- <span data-ttu-id="e94b5-1138">일반 이름과 지문으로 지정 인증서 지원</span><span class="sxs-lookup"><span data-stu-id="e94b5-1138">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="e94b5-1139">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="e94b5-1139">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="e94b5-1140">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="e94b5-1140">Az.SIgnalR</span></span>
- <span data-ttu-id="e94b5-1141">SIgnalR에 대한 PowerShell cmdlet에 대한 일반 공급</span><span class="sxs-lookup"><span data-stu-id="e94b5-1141">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="e94b5-1142">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e94b5-1142">Az.Sql</span></span>
- <span data-ttu-id="e94b5-1143">위협 탐지의 cmdlet에 새로운 Data_Exfiltration 및 Unsafe_Action 검색 유형 추가</span><span class="sxs-lookup"><span data-stu-id="e94b5-1143">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="e94b5-1144">Sql 감사 cmdlet에 대한 설명서 예제 업데이트</span><span class="sxs-lookup"><span data-stu-id="e94b5-1144">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="e94b5-1145">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="e94b5-1145">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="e94b5-1146">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="e94b5-1146">Az.Storage</span></span>
- <span data-ttu-id="e94b5-1147">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="e94b5-1147">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="e94b5-1148">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="e94b5-1148">Az.Websites</span></span>
- <span data-ttu-id="e94b5-1149">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="e94b5-1149">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="e94b5-1150">0.7.0 - 2018년 12월</span><span class="sxs-lookup"><span data-stu-id="e94b5-1150">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="e94b5-1151">일반</span><span class="sxs-lookup"><span data-stu-id="e94b5-1151">General</span></span>

* <span data-ttu-id="e94b5-1152">AzureRM에서 Az 전환 예정에 대한 사소한 변경</span><span class="sxs-lookup"><span data-stu-id="e94b5-1152">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="e94b5-1153">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e94b5-1153">Az.Compute</span></span>

* <span data-ttu-id="e94b5-1154">`New-AzVm(ss)` cmdlet에 대한 간단한 매개 변수 집합에 UltraSSD 및 갤러리 이미지에 대한 지원을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-1154">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="e94b5-1155">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="e94b5-1155">Az.DataLakeStore</span></span>

* <span data-ttu-id="e94b5-1156">ADLS 계정의 도메인의 후행 슬래시를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-1156">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="e94b5-1157">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="e94b5-1157">Az.FrontDoor</span></span>

* <span data-ttu-id="e94b5-1158">일부 끊어진 링크 수정</span><span class="sxs-lookup"><span data-stu-id="e94b5-1158">Fixed some broken links</span></span>
    - <span data-ttu-id="e94b5-1159">New-AzureRmFrontDoor 및 Set-AzureRmFrontDoor 아티클에서 New-AzureRmFrontDoorHealthProbeSettingObject cmdlet 아티클에 대한 링크가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-1159">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="e94b5-1160">New-AzureRmFrontDoorManagedRuleObject 아티클에서 New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet 아티클에 대한 링크가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-1160">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="e94b5-1161">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="e94b5-1161">Az.RecoveryServices</span></span>

* <span data-ttu-id="e94b5-1162">Azure File Share 복원 작업에 클라이언트 측 유효성 검사가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-1162">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="e94b5-1163">afs 복원의 경우 storageAccountName 및 storageAccountResourceGroupName을 선택적으로 만들었습니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-1163">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="e94b5-1164">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e94b5-1164">Az.Resources</span></span>

* <span data-ttu-id="e94b5-1165">에 대 한 수정 https://github.com/Azure/azure-powershell/issues/7679</span><span class="sxs-lookup"><span data-stu-id="e94b5-1165">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="e94b5-1166">기본 관리자를 요청할 때 구독 범위가 제공되는 경우 Get-AzureRmRoleAssignment를 업데이트하여 구독 범위를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-1166">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="e94b5-1167">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e94b5-1167">Az.Sql</span></span>

* <span data-ttu-id="e94b5-1168">AzureRM에서 Az 전환 예정에 대한 사소한 변경</span><span class="sxs-lookup"><span data-stu-id="e94b5-1168">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="e94b5-1169">DotNet 코어에서 Get-AzureRmSqlDatabaseVulnerabilityAssessment를 사용하는 문제 해결</span><span class="sxs-lookup"><span data-stu-id="e94b5-1169">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="e94b5-1170">SQL 감사 cmdlet과 관련된 도움말 메시지의 설명서가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-1170">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="e94b5-1171">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="e94b5-1171">Az.Storage</span></span>

* <span data-ttu-id="e94b5-1172">New-AzureRmStorageAccount에 -EnableHierarchicalNamespace 추가</span><span class="sxs-lookup"><span data-stu-id="e94b5-1172">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="e94b5-1173">파일 복사 cmdlet이 -DestContext 입력이 없을 때 대상의 원본 컨텍스트를 다시 사용할 수 없는 문제 수정</span><span class="sxs-lookup"><span data-stu-id="e94b5-1173">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="e94b5-1174">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="e94b5-1174">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="e94b5-1175">고정적인 웹 사이트 구성 지원</span><span class="sxs-lookup"><span data-stu-id="e94b5-1175">Support Static Website configuration</span></span>
    - <span data-ttu-id="e94b5-1176">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="e94b5-1176">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="e94b5-1177">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="e94b5-1177">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="e94b5-1178">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="e94b5-1178">Az.Websites</span></span>

* <span data-ttu-id="e94b5-1179">Set-AzureRmWebApp 및 Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="e94b5-1179">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span> 
    - <span data-ttu-id="e94b5-1180">Windows 및 Linux 컨테이너 응용 프로그램에 탑재할 Azure Storage 경로를 지정하기 위해 새 매개 변수(-AzureStoragePath)가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-1180">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="e94b5-1181">새 cmdlet New-AzureRmWebAppAzureStoragePath의 출력을 매개 변수로 사용하여 Azure Storage 경로를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-1181">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="e94b5-1182">0.6.1 - 2018년 11월</span><span class="sxs-lookup"><span data-stu-id="e94b5-1182">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="e94b5-1183">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="e94b5-1183">Az.ApiManagement</span></span>
* <span data-ttu-id="e94b5-1184">형식 매핑 문제에 대한 종속성 업데이트</span><span class="sxs-lookup"><span data-stu-id="e94b5-1184">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="e94b5-1185">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="e94b5-1185">Az.Automation</span></span>
* <span data-ttu-id="e94b5-1186">Azure Automation cmdlet 기반 Swagger</span><span class="sxs-lookup"><span data-stu-id="e94b5-1186">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="e94b5-1187">업데이트 관리 cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="e94b5-1187">Added Update Management cmdlets</span></span>
* <span data-ttu-id="e94b5-1188">소스 제어 cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="e94b5-1188">Added Source Control cmdlets</span></span>
* <span data-ttu-id="e94b5-1189">Remove-AzureRmAutomationHybridWorkerGroup cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="e94b5-1189">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="e94b5-1190">DSC 노드 등록 명령 수정</span><span class="sxs-lookup"><span data-stu-id="e94b5-1190">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="e94b5-1191">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e94b5-1191">Az.Compute</span></span>
* <span data-ttu-id="e94b5-1192">SystemAssigned ID에 대한 ID 문제 수정</span><span class="sxs-lookup"><span data-stu-id="e94b5-1192">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="e94b5-1193">형식 매핑 문제에 대한 종속성 업데이트</span><span class="sxs-lookup"><span data-stu-id="e94b5-1193">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="e94b5-1194">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="e94b5-1194">Az.ContainerInstance</span></span>
* <span data-ttu-id="e94b5-1195">형식 매핑 문제에 대한 종속성 업데이트</span><span class="sxs-lookup"><span data-stu-id="e94b5-1195">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="e94b5-1196">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="e94b5-1196">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="e94b5-1197">마켓플레이스 cmdlet에 대한 예제 설명 업데이트</span><span class="sxs-lookup"><span data-stu-id="e94b5-1197">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="e94b5-1198">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e94b5-1198">Az.Network</span></span>
* <span data-ttu-id="e94b5-1199">New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="e94b5-1199">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="e94b5-1200">지원되는 AzureFirewall 네트워크 프로토콜에 ICMP 다시 추가</span><span class="sxs-lookup"><span data-stu-id="e94b5-1200">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="e94b5-1201">Test-AzureRmNetworkWatcherConnectivity cmdlet을 업데이트하여 대상 ID, 주소 및 포트 유효성 검사를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-1201">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span> 
* <span data-ttu-id="e94b5-1202">VirtualNetwork 맵의 메모리 사용 문제 해결</span><span class="sxs-lookup"><span data-stu-id="e94b5-1202">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="e94b5-1203">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="e94b5-1203">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="e94b5-1204">보호된 파일 공유에 대한 정책을 수정하는 것에 대해 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-1204">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="e94b5-1205">정책 표준 시간대를 대문자로 변환했습니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-1205">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="e94b5-1206">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="e94b5-1206">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="e94b5-1207">New-AzureRmRecoveryServicesAsrProtectableItem의 예제 정정</span><span class="sxs-lookup"><span data-stu-id="e94b5-1207">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="e94b5-1208">형식 매핑 문제에 대한 종속성 업데이트</span><span class="sxs-lookup"><span data-stu-id="e94b5-1208">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="e94b5-1209">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="e94b5-1209">Az.Relay</span></span>
* <span data-ttu-id="e94b5-1210">선택적 매개 변수 -KeyValue를 New-AzureRmRelayKey cmdlet에 추가하여 사용자가 KeyValue를 제공할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-1210">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="e94b5-1211">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e94b5-1211">Az.Resources</span></span>
* <span data-ttu-id="e94b5-1212">`New-AzureRmPolicyAssignment` 및 `Set-AzureRmPolicyAssignment`의 자원 ID 관련 매개 변수에 대한 도움말 문서를 업데이트함</span><span class="sxs-lookup"><span data-stu-id="e94b5-1212">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="e94b5-1213">-Metadata를 사용하는 New-AzureRmPolicyDefinition에 대한 예제 추가</span><span class="sxs-lookup"><span data-stu-id="e94b5-1213">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="e94b5-1214">NetStandard의 태그 키에서 대소문자 보존을 허용하도록 수정: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="e94b5-1214">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="e94b5-1215">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="e94b5-1215">Az.ServiceFabric</span></span>
* <span data-ttu-id="e94b5-1216">향후 호환성이 손상되는 변경에 대한 사용 중단 메시지 추가</span><span class="sxs-lookup"><span data-stu-id="e94b5-1216">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="e94b5-1217">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e94b5-1217">Az.Sql</span></span>
* <span data-ttu-id="e94b5-1218">Azure Sql Database Managed Instance 및 Azure Sql Managed Database에 CRUD 작업을 위한 새 cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="e94b5-1218">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="e94b5-1219">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="e94b5-1219">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="e94b5-1220">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="e94b5-1220">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="e94b5-1221">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="e94b5-1221">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="e94b5-1222">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="e94b5-1222">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="e94b5-1223">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="e94b5-1223">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="e94b5-1224">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="e94b5-1224">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="e94b5-1225">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="e94b5-1225">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="e94b5-1226">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="e94b5-1226">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="e94b5-1227">서버 또는 데이터베이스에서 확장 감사 정책 관리를 활성화했습니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-1227">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="e94b5-1228">새 매개 변수(PredicateExpression)가 감사 로그 필터링을 사용하도록 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-1228">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="e94b5-1229">Cmdlet이 레거시 클라이언트 대신 SQL 클라이언트를 사용하도록 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-1229">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="e94b5-1230">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="e94b5-1230">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="e94b5-1231">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="e94b5-1231">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="e94b5-1232">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="e94b5-1232">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="e94b5-1233">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="e94b5-1233">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="e94b5-1234">스토리지 계정 이름 매개 변수가 설정된 Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings를 사용할 때의 문제 해결</span><span class="sxs-lookup"><span data-stu-id="e94b5-1234">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="e94b5-1235">0.5.0 - 2018년 11월</span><span class="sxs-lookup"><span data-stu-id="e94b5-1235">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="e94b5-1236">일반</span><span class="sxs-lookup"><span data-stu-id="e94b5-1236">General</span></span>
* <span data-ttu-id="e94b5-1237">많은 핵심 cmdlet에 Resource Completers를 추가하여 대화형으로 cmdlet을 호출할 때 기존 리소스 이름을 탭으로 이동할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-1237">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="e94b5-1238">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="e94b5-1238">Az.Profile</span></span>
* <span data-ttu-id="e94b5-1239">ClientRuntime의 최신 버전을 사용하도록 일반적인 코드를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-1239">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="e94b5-1240">Connect-AzAccount cmdlet의 매개 변수 TenantId 이름을 Tenant로 바꾸고 TenantId의 별칭을 추가합니다</span><span class="sxs-lookup"><span data-stu-id="e94b5-1240">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="e94b5-1241">Connect-AzAccount의 업데이트된 TenantId 설명</span><span class="sxs-lookup"><span data-stu-id="e94b5-1241">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="e94b5-1242">테넌트 도메인을 제공할 때 실패한 로그인에 대한 오류 메시지 수정</span><span class="sxs-lookup"><span data-stu-id="e94b5-1242">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="e94b5-1243">테넌트에 구독이 없는 계정의 컨텍스트 이름 충돌 문제 수정</span><span class="sxs-lookup"><span data-stu-id="e94b5-1243">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="e94b5-1244">MSI를 사용할 때 DataLake 엔드포인트 문제 수정</span><span class="sxs-lookup"><span data-stu-id="e94b5-1244">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="e94b5-1245">연결되지 않은 경우 'Disconnect-AzAccount'가 throw하는 문제 수정</span><span class="sxs-lookup"><span data-stu-id="e94b5-1245">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="e94b5-1246">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="e94b5-1246">Az.CognitiveServices</span></span>
* <span data-ttu-id="e94b5-1247">Get-AzCognitiveServicesAccountSkus 작업을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-1247">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e94b5-1248">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e94b5-1248">Az.Compute</span></span>
* <span data-ttu-id="e94b5-1249">Add-AzVmssVMDataDisk 및 Remove-AzVmssVMDataDisk cmdlet를 추가합니다</span><span class="sxs-lookup"><span data-stu-id="e94b5-1249">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="e94b5-1250">Get-AzVMImage는 AutomaticOSUpgradeProperties를 표시합니다</span><span class="sxs-lookup"><span data-stu-id="e94b5-1250">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="e94b5-1251">수정된 SetAzVMChefExtension -BootstrapOptions 및 -JsonAttribute option 값이 json 형식으로 설정하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-1251">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="e94b5-1252">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="e94b5-1252">Az.DataLakeStore</span></span>
* <span data-ttu-id="e94b5-1253">DataLake 패키지를 1.1.10으로 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-1253">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="e94b5-1254">기본 동시성을 다중 스레드 작업에 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-1254">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="e94b5-1255">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="e94b5-1255">Az.Insights</span></span>
* <span data-ttu-id="e94b5-1256">해결된 문제 #7267(자동 크기 조정 영역)</span><span class="sxs-lookup"><span data-stu-id="e94b5-1256">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="e94b5-1257">열거된 매개 변수를 제대로 설정하지 않은 새 자동 크기 조정 규칙을 만드는 데 문제가 있습니다(이를 항상 기본값으로 설정함).</span><span class="sxs-lookup"><span data-stu-id="e94b5-1257">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="e94b5-1258">해결된 문제 # 7513[자세한 정보] Set-AzDiagnosticSetting은 설정을 생성하는 동안 범주를 명시적으로 지정해야 합니다</span><span class="sxs-lookup"><span data-stu-id="e94b5-1258">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="e94b5-1259">이제 cmdlet은 생성 중에 사용할 범주를 명시적으로 표시할 필요가 없습니다. 즉, 문서화된대로 작동합니다</span><span class="sxs-lookup"><span data-stu-id="e94b5-1259">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e94b5-1260">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e94b5-1260">Az.Network</span></span>
* <span data-ttu-id="e94b5-1261">다음 cmdlet에 대해 PeeringType을 필수 매개 변수로 변경했습니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-1261">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="e94b5-1262">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="e94b5-1262">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="e94b5-1263">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="e94b5-1263">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="e94b5-1264">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="e94b5-1264">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="e94b5-1265">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="e94b5-1265">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="e94b5-1266">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="e94b5-1266">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="e94b5-1267">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="e94b5-1267">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="e94b5-1268">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="e94b5-1268">Az.PolicyInsights</span></span>
* <span data-ttu-id="e94b5-1269">추가된 정책 재구성 cmdlet</span><span class="sxs-lookup"><span data-stu-id="e94b5-1269">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="e94b5-1270">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e94b5-1270">Az.Resources</span></span>
* <span data-ttu-id="e94b5-1271">에 대 한 수정 https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="e94b5-1271">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="e94b5-1272">'Get-AzResource'에 대해 '-ResourceId' 매개 변수를 사용하여 리소스 나열 허용</span><span class="sxs-lookup"><span data-stu-id="e94b5-1272">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="e94b5-1273">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="e94b5-1273">Az.ServiceBus</span></span>
* <span data-ttu-id="e94b5-1274">마이그레이션 상태를 알 수 있도록 PSServiceBusMigrationConfigurationAttributes에 MigrationState 읽기 전용 속성 추가.</span><span class="sxs-lookup"><span data-stu-id="e94b5-1274">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="e94b5-1275">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="e94b5-1275">Az.ServiceFabric</span></span>
* <span data-ttu-id="e94b5-1276">Linux Vmss에 인증서 추가 수정.</span><span class="sxs-lookup"><span data-stu-id="e94b5-1276">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="e94b5-1277">Add-AzServiceFabricClusterCertificate 수정</span><span class="sxs-lookup"><span data-stu-id="e94b5-1277">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="e94b5-1278">새 인증서(Azure/service-fabric-issues#932)에서 올바른 지문을 사용.</span><span class="sxs-lookup"><span data-stu-id="e94b5-1278">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="e94b5-1279">올바르게 예외 표시(Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="e94b5-1279">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="e94b5-1280">Vmss CreateOrUpdate 작업을 시작하기 전에 'Update-AzServiceFabricDurability'를 수정하여 클러스터 구성 업데이트.</span><span class="sxs-lookup"><span data-stu-id="e94b5-1280">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="e94b5-1281">0.4.0 - 2018년 10월</span><span class="sxs-lookup"><span data-stu-id="e94b5-1281">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="e94b5-1282">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="e94b5-1282">Az.Profile</span></span>
* <span data-ttu-id="e94b5-1283">CloudShell에서 Get-AzSubscription을 사용하여 문제를 해결합니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-1283">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="e94b5-1284">ClientRuntime의 최신 버전을 사용하도록 일반적인 코드를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-1284">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e94b5-1285">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e94b5-1285">Az.Compute</span></span>
* <span data-ttu-id="e94b5-1286">'New-AzVm'에 대해 간단한 매개 변수를 사용하는 경우 가속화된 네트워킹을 설정하기 위해 새 크기가 VM 크기의 허용 목록에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-1286">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="e94b5-1287">모든 cmdlet에 ResourceName 인수 완성자가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-1287">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="e94b5-1288">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="e94b5-1288">Az.DataLakeStore</span></span>
* <span data-ttu-id="e94b5-1289">Virtual Network 규칙에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="e94b5-1289">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="e94b5-1290">Get-AzDataLakeStoreVirtualNetworkRule: Azure Data Lake Store 가상 네트워크 규칙을 가져오거나 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-1290">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="e94b5-1291">Add-AzDataLakeStoreVirtualNetworkRule: 지정된 Data Lake Store 계정에 가상 네트워크 규칙을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-1291">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="e94b5-1292">Set-AzDataLakeStoreVirtualNetworkRule: 지정된 Data Lake Store 계정에 지정된 가상 네트워크 규칙을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-1292">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="e94b5-1293">Remove-AzDataLakeStoreVirtualNetworkRule: Azure Data Lake Store 가상 네트워크 규칙을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-1293">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e94b5-1294">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e94b5-1294">Az.Network</span></span>
* <span data-ttu-id="e94b5-1295">Test-AzNetworkWatcherConnectivity cmdlet을 업데이트하고, 백 엔드에 프로토콜 값을 전달합니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-1295">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="e94b5-1296">모든 cmdlet에 ResourceName 인수 완성자가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-1296">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="e94b5-1297">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e94b5-1297">Az.Resources</span></span>
* <span data-ttu-id="e94b5-1298">(기본 프로필에 구독이 없고 범위가 지정되지 않은 경우) 시나리오에서 의미 있는 예외를 추가하여 Get-AzRoleDefinition이 인식할 수 없는 예외를 throw하는 문제를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-1298">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="e94b5-1299">또한 기본 매개 변수 집합을 'RoleDefinitionNameParameterSet'으로 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-1299">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="e94b5-1300">0.3.0 - 2018년 10월</span><span class="sxs-lookup"><span data-stu-id="e94b5-1300">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="e94b5-1301">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="e94b5-1301">Azure.Storage</span></span>
* <span data-ttu-id="e94b5-1302">대상에 메타데이터가 있을 때 Blob/파일이 메타 데이터를 복사하지 않는 문제 수정</span><span class="sxs-lookup"><span data-stu-id="e94b5-1302">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="e94b5-1303">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="e94b5-1303">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="e94b5-1304">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="e94b5-1304">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="e94b5-1305">특정 위치의 스토리지 리소스 사용을 지원하고 글로벌 스토리지 리소스 사용 가져오기는 더 이상 사용되지 않는다는 경고 메시지를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-1305">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="e94b5-1306">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="e94b5-1306">Get-AzStorageUsage</span></span>
    
#### <a name="azcognitiveservices"></a><span data-ttu-id="e94b5-1307">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="e94b5-1307">Az.CognitiveServices</span></span>
* <span data-ttu-id="e94b5-1308">기존 계정이 없는 Get-AzCognitiveServicesAccountSkus를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-1308">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e94b5-1309">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e94b5-1309">Az.Compute</span></span>
* <span data-ttu-id="e94b5-1310">Get-AzVM -ResourceGroupName <rg>가 필요한 경우 50개가 넘는 결과를 반환하도록 수정</span><span class="sxs-lookup"><span data-stu-id="e94b5-1310">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="e94b5-1311">'SimpleParameterSet' 예제가 New-AzVmss cmdlet 도움말에 추가됨</span><span class="sxs-lookup"><span data-stu-id="e94b5-1311">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="e94b5-1312">Azure Disk Encryption 진행률 메시지의 오타를 수정</span><span class="sxs-lookup"><span data-stu-id="e94b5-1312">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="e94b5-1313">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="e94b5-1313">Az.DataFactoryV2</span></span>
* <span data-ttu-id="e94b5-1314">ADF.Net SDK 버전을 2.3.0으로 업데이트</span><span class="sxs-lookup"><span data-stu-id="e94b5-1314">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e94b5-1315">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e94b5-1315">Az.Network</span></span>
* <span data-ttu-id="e94b5-1316">NetworkProfile 기능 추가</span><span class="sxs-lookup"><span data-stu-id="e94b5-1316">Added NetworkProfile functionality.</span></span> <span data-ttu-id="e94b5-1317">추가된 새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-1317">new cmdlets added</span></span>
    - <span data-ttu-id="e94b5-1318">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="e94b5-1318">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="e94b5-1319">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="e94b5-1319">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="e94b5-1320">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="e94b5-1320">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="e94b5-1321">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="e94b5-1321">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="e94b5-1322">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="e94b5-1322">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="e94b5-1323">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="e94b5-1323">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="e94b5-1324">서브넷 모델에 서비스 연결 링크 추가</span><span class="sxs-lookup"><span data-stu-id="e94b5-1324">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="e94b5-1325">New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="e94b5-1325">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="e94b5-1326">Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="e94b5-1326">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="e94b5-1327">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="e94b5-1327">Az.RedisCache</span></span>
* <span data-ttu-id="e94b5-1328">모든 문자열을 Size 매개 변수로 진행되도록 허용</span><span class="sxs-lookup"><span data-stu-id="e94b5-1328">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="e94b5-1329">PSArgumentCompleter 팝업에 P5 추가</span><span class="sxs-lookup"><span data-stu-id="e94b5-1329">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="e94b5-1330">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e94b5-1330">Az.Resources</span></span>
* <span data-ttu-id="e94b5-1331">-Mode 매개 변수를 Set-AzPolicyDefinition에 추가</span><span class="sxs-lookup"><span data-stu-id="e94b5-1331">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="e94b5-1332">사용자가 포함된 Origin 작업에서 Get-AzProviderOperation commandlet 버그 수정</span><span class="sxs-lookup"><span data-stu-id="e94b5-1332">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="e94b5-1333">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e94b5-1333">Az.Sql</span></span>
* <span data-ttu-id="e94b5-1334">일부 백업 cmdlet이 현재 azure 구독을 인식하지 않는 문제 해결</span><span class="sxs-lookup"><span data-stu-id="e94b5-1334">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="e94b5-1335">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="e94b5-1335">Az.Websites</span></span>
* <span data-ttu-id="e94b5-1336">새 cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - 컨테이너 지속적인 배포 Webhook URL을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-1336">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="e94b5-1337">새 cmdlet New-AzWebAppContainerPSSession 및 Enter-WebAppContainerPSSession -  windows 컨테이너 앱에 PowerShell 원격 세션을 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="e94b5-1337">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="e94b5-1338">0.2.0 - 2018년 9월</span><span class="sxs-lookup"><span data-stu-id="e94b5-1338">0.2.0 - September 2018</span></span>
 <span data-ttu-id="e94b5-1339">최초 릴리스</span><span class="sxs-lookup"><span data-stu-id="e94b5-1339">Initial Release</span></span>