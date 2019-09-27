---
ms.openlocfilehash: 96e6d7bc0cc29adc1c0e49ba344d27349454c214
ms.sourcegitcommit: 92722d603b60dc769660e7517da60110133d9959
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/24/2019
ms.locfileid: "71226442"
---
## <a name="270---september-2019"></a><span data-ttu-id="74567-101">2.7.0 - 2019년 9월</span><span class="sxs-lookup"><span data-stu-id="74567-101">2.7.0 - September 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="74567-102">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="74567-102">Az.ApiManagement</span></span>
* <span data-ttu-id="74567-103">'Set-AzApiManagementPolicy' 참조 설명서에서 '-Format' 매개 변수 설명이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="74567-103">Update '-Format' parameter description in 'Set-AzApiManagementPolicy' reference documentation</span></span>
* <span data-ttu-id="74567-104">참조 설명서에서 사용되지 않는 cmdlet 'Update-AzApiManagementDeployment'의 참조를 제거했습니다.</span><span class="sxs-lookup"><span data-stu-id="74567-104">Removed references of deprecated cmdlet 'Update-AzApiManagementDeployment' from reference documentation.</span></span> <span data-ttu-id="74567-105">그 대신 'Set-AzApiManagement'를 사용하세요.</span><span class="sxs-lookup"><span data-stu-id="74567-105">Use 'Set-AzApiManagement' instead.</span></span>

#### <a name="azautomation"></a><span data-ttu-id="74567-106">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="74567-106">Az.Automation</span></span>
* <span data-ttu-id="74567-107">'Register-AzAutomationDscNode'에 대한 참조 설명서의 예제 오타가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="74567-107">Fixed example typo in reference documentation for 'Register-AzAutomationDscNode'</span></span>
* <span data-ttu-id="74567-108">Register-AzAutomationDSCNode에 OS 제한에 대한 설명이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="74567-108">Added clarification on OS restriction to Register-AzAutomationDSCNode</span></span>
* <span data-ttu-id="74567-109">-Wait 옵션에 대한 Start-AzAutomationRunbook cmdlet Null 참조 예외가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="74567-109">Fixed Start-AzAutomationRunbook cmdlet Null reference exception for -Wait option.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="74567-110">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="74567-110">Az.Compute</span></span>
* <span data-ttu-id="74567-111">New-AzDiskConfig에 UploadSizeInBytes 매개 변수가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="74567-111">Add UploadSizeInBytes parameter tp New-AzDiskConfig</span></span>
* <span data-ttu-id="74567-112">New-AzSnapshotConfig에 증분 매개 변수가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="74567-112">Add Incremental parameter to New-AzSnapshotConfig</span></span>
* <span data-ttu-id="74567-113">다음과 같은 낮은 우선 순위의 가상 머신 기능이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="74567-113">Add a low priority virtual machine feature:</span></span>
    - <span data-ttu-id="74567-114">MaxPrice, EvictionPolicy 및 Priority 매개 변수가 New-AzVMConfig에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="74567-114">MaxPrice, EvictionPolicy and Priority parameters are added to New-AzVMConfig.</span></span>
    - <span data-ttu-id="74567-115">MaxPrice 매개 변수는 New-AzVmssConfig, Update-AzVM 및 Update-AzVmss cmdlet에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="74567-115">MaxPrice parameter is added to New-AzVmssConfig, Update-AzVM and Update-AzVmss cmdlets.</span></span>
* <span data-ttu-id="74567-116">구독의 모든 가용성 세트를 나열할 때 발생하는 Get-AzAvailabilitySet cmdlet에 대한 VM 참조 이슈가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="74567-116">Fix VM reference issue for Get-AzAvailabilitySet cmdlet when it lists all availability sets in the subscription.</span></span>
* <span data-ttu-id="74567-117">Get-AzRemoteDesktopFile에 대한 null 예외가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="74567-117">Fix the null exception for Get-AzRemoteDesktopFile.</span></span>
* <span data-ttu-id="74567-118">종료 상대 위치에 대한 VHD 검색 메서드가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="74567-118">Fix VHD Seek method for end-relative position.</span></span>
* <span data-ttu-id="74567-119">New-AzVM 및 Update-AzVM에 대한 UltraSSD 이슈가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="74567-119">Fix UltraSSD issue for New-AzVM and Update-AzVM.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="74567-120">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="74567-120">Az.DataFactory</span></span>
* <span data-ttu-id="74567-121">ADF V2에 대한 3가지 새 명령 Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription 및 Get-AzDataFactoryV2TriggerSubscriptionStatus가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="74567-121">Adding 3 new commands for ADF V2 - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription, and Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>
* <span data-ttu-id="74567-122">ADF .Net SDK 버전이 4.1.3으로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="74567-122">Updated ADF .Net SDK version to 4.1.3</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="74567-123">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="74567-123">Az.HDInsight</span></span>
* <span data-ttu-id="74567-124">호출 주요 변경 내용</span><span class="sxs-lookup"><span data-stu-id="74567-124">Call out breaking changes</span></span>

#### <a name="aziothub"></a><span data-ttu-id="74567-125">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="74567-125">Az.IotHub</span></span>
* <span data-ttu-id="74567-126">지역 쌍 재해 복구 지역에 IotHub에 대한 장애 조치(failover) 호출 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="74567-126">Add support to invoke failover for an IotHub to the geo-paired disaster recovery region.</span></span>
* <span data-ttu-id="74567-127">IotHub에 대한 메시지 보강 관리 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="74567-127">Add support to manage message enrichment for an IotHub.</span></span> <span data-ttu-id="74567-128">새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="74567-128">New cmdlets are:</span></span>
    - <span data-ttu-id="74567-129">Add-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="74567-129">Add-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="74567-130">Get-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="74567-130">Get-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="74567-131">Remove-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="74567-131">Remove-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="74567-132">Set-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="74567-132">Set-AzIotHubMessageEnrichment</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="74567-133">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="74567-133">Az.Monitor</span></span>
* <span data-ttu-id="74567-134">최신 모니터링 SDK, 즉, 0.24.1-preview를 가리킵니다.</span><span class="sxs-lookup"><span data-stu-id="74567-134">Pointing to the most recent Monitor SDK, i.e. 0.24.1-preview</span></span>
   - <span data-ttu-id="74567-135">메트릭 cmdlet에 줄 바꿈하지 않는 변경 내용을 추가합니다. 즉, 단위 열거형은 여러 새 값을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="74567-135">Adds non-braking changes to the Metrics cmdlets, i.e. the Unit enumeration supports several new values.</span></span> <span data-ttu-id="74567-136">이러한 cmdlet은 읽기 전용이므로 cmdlet 입력이 변경되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="74567-136">These are read-only cmdlets, so there would be no change in the input of the cmdlets.</span></span>
   - <span data-ttu-id="74567-137">이제 **ActionGroups** 요청의 api 버전은 **2019-06-01**이고, 이전에는 **2018-03-01**였습니다.</span><span class="sxs-lookup"><span data-stu-id="74567-137">The api-version of the **ActionGroups** requests is now **2019-06-01**, before it was **2018-03-01**.</span></span> <span data-ttu-id="74567-138">시나리오 테스트가 이 변경 내용에 맞게 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="74567-138">The scenario tests have been updated to accommodate for this change.</span></span>
   - <span data-ttu-id="74567-139">**EmailReceiver** 및 **WebhookReceiver** 클래스에 대한 생성자가 새 필수 인수, 즉, **useCommonAlertSchema**라는 부울 값을 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="74567-139">The constructors for the classes **EmailReceiver** and **WebhookReceiver** added one new mandatory argument, i.e. a Boolean value called **useCommonAlertSchema**.</span></span> <span data-ttu-id="74567-140">현재 이 값은 cmdlet의 주요 변경 사항을 숨기도록 **false**로 고정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="74567-140">Currently, the value is fixed to **false** to hide this breaking change from the cmdlets.</span></span> <span data-ttu-id="74567-141">**참고**: 이 변경 사항은 경고 팀에서 유효성을 검사해야 하는 임시 변경 내용입니다.</span><span class="sxs-lookup"><span data-stu-id="74567-141">**NOTE**: this is a temporary change that must be validated by the Alerts team.</span></span>
   - <span data-ttu-id="74567-142">이전 SDK에서 변경된 **Source** 클래스(**ScheduledQueryRuleSource** 클래스와 관련됨)의 생성자에 대한 인수 순서입니다.</span><span class="sxs-lookup"><span data-stu-id="74567-142">The order of the arguments for the constructor of the class **Source** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="74567-143">이번 변화로 인해 두 개의 단위 테스트를 수정해야 했습니다. 즉, 두 단위 테스트가 컴파일되었지만 테스트를 통과하지 못했습니다.</span><span class="sxs-lookup"><span data-stu-id="74567-143">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
   - <span data-ttu-id="74567-144">이전 SDK에서 변경된 **AlertingAction** 클래스(**ScheduledQueryRuleSource** 클래스와 관련됨)의 생성자에 대한 인수 순서입니다.</span><span class="sxs-lookup"><span data-stu-id="74567-144">The order of the arguments for the constructor of the class **AlertingAction** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="74567-145">이번 변화로 인해 두 개의 단위 테스트를 수정해야 했습니다. 즉, 두 단위 테스트가 컴파일되었지만 테스트를 통과하지 못했습니다.</span><span class="sxs-lookup"><span data-stu-id="74567-145">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
* <span data-ttu-id="74567-146">메트릭 경고 V2에 대한 동적 임계값 기준 지원</span><span class="sxs-lookup"><span data-stu-id="74567-146">Support Dynamic Threshold criteria for metric alert V2</span></span>
    - <span data-ttu-id="74567-147">AzMetricAlertRuleV2Criteria: 이제 동적 임계값 조건도 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="74567-147">New-AzMetricAlertRuleV2Criteria: now creats dynamic threshold criteria also</span></span>
    - <span data-ttu-id="74567-148">Add-AzMetricAlertRuleV2: 이제 동적 임계값 조건도 수락합니다.</span><span class="sxs-lookup"><span data-stu-id="74567-148">Add-AzMetricAlertRuleV2: now accept dynamic threshold criteria also</span></span>
* <span data-ttu-id="74567-149">SQR(예약된 쿼리 규칙)의 향상된 기능</span><span class="sxs-lookup"><span data-stu-id="74567-149">Improvements in Scheduled Query Rule cmdlets (SQR)</span></span>
 - <span data-ttu-id="74567-150">Cmdlet이 'Location' 매개 변수를 두 가지 형식(eastus 같은 위치 또는 미국 동부 같은 위치 표시 이름)으로 모두 허용합니다.</span><span class="sxs-lookup"><span data-stu-id="74567-150">Cmdlets will accept 'Location' paramater in both formats, either the location (e.g. eastus) or the location display name (e.g. East US)</span></span>
 - <span data-ttu-id="74567-151">도움말 파일에 적절하게 표시된 'Enabled' 매개 변수</span><span class="sxs-lookup"><span data-stu-id="74567-151">Illustrated 'Enabled' parameter in help files properly</span></span>
 - <span data-ttu-id="74567-152">선택적 매개 변수 'ActionGroup'에 대한 예제가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="74567-152">Added examples for 'ActionGroup' optional parameter</span></span>
 - <span data-ttu-id="74567-153">도움말 파일이 전체적으로 개선되었습니다.</span><span class="sxs-lookup"><span data-stu-id="74567-153">Overall improved help files</span></span>
* <span data-ttu-id="74567-154">'Set-AzActionRule'의 범위 유형 결정 버그를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="74567-154">Fix bug in determining scope type for 'Set-AzActionRule'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="74567-155">Az.Network</span><span class="sxs-lookup"><span data-stu-id="74567-155">Az.Network</span></span>
* <span data-ttu-id="74567-156">'New-AzApplicationGateway' 참조 설명서의 잘못된 예제가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="74567-156">Fix incorrect example in 'New-AzApplicationGateway' reference documentation</span></span> 
* <span data-ttu-id="74567-157">'Get-AzNetworkWatcherPacketCapture' 참조 설명서에 패킷 캡처를 위한 모든 속성 검색과 관련된 메모가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="74567-157">Add note in 'Get-AzNetworkWatcherPacketCapture' reference documentation about retrieving all properties for a packet capture</span></span>
* <span data-ttu-id="74567-158">NIC를 올바르게 열거하도록 'Test-AzNetworkWatcherIPFlow' 참조 설명서의 예제가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="74567-158">Fixed example in 'Test-AzNetworkWatcherIPFlow' reference documentation to correctly enumerate NICs</span></span>
* <span data-ttu-id="74567-159">추가 세부 정보가 있는 경우 추가 세부 정보를 표시하도록 클라우드 예외 구문 분석이 향상되었습니다.</span><span class="sxs-lookup"><span data-stu-id="74567-159">Improved cloud exception parsing to display additional details if they are present</span></span>
* <span data-ttu-id="74567-160">더 많은 형식의 SDK 예외를 처리하도록 클라우드 예외 구문 분석이 향상되었습니다.</span><span class="sxs-lookup"><span data-stu-id="74567-160">Improved cloud exception parsing to handle additional type of SDK exception</span></span>
* <span data-ttu-id="74567-161">보안 규칙 모델의 잘못된 매핑이 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="74567-161">Fixed incorrect mapping of Security Rule models</span></span>
* <span data-ttu-id="74567-162">네트워크 인터페이스에 개인 IP 기능을 위한 속성이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="74567-162">Added properties to network interface for private ip feature</span></span>
    - <span data-ttu-id="74567-163">PSNetworkInterface에 'PrivateEndpoint' 속성이 PSResourceId 형식으로 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="74567-163">Added property 'PrivateEndpoint' as type of PSResourceId to PSNetworkInterface</span></span>
    - <span data-ttu-id="74567-164">PSNetworkInterfaceIPConfiguration에 'PrivateLinkConnectionProperties' 속성이 PSIpConfigurationConnectivityInformation 형식으로 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="74567-164">Added property 'PrivateLinkConnectionProperties' as type of PSIpConfigurationConnectivityInformation to PSNetworkInterfaceIPConfiguration</span></span>
    - <span data-ttu-id="74567-165">새 모델 클래스 PSIpConfigurationConnectivityInformation이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="74567-165">Added new model class PSIpConfigurationConnectivityInformation</span></span>
* <span data-ttu-id="74567-166">Azure Firewall 리소스에 대한 새 ApplicationRuleProtocolType 'mssql'이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="74567-166">Added new ApplicationRuleProtocolType 'mssql' for Azure Firewall resource</span></span>
* <span data-ttu-id="74567-167">Virtual WAN에서 멀티 링크를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="74567-167">MultiLink support in Virtual WAN</span></span>
    - <span data-ttu-id="74567-168">새 cmdlet</span><span class="sxs-lookup"><span data-stu-id="74567-168">New cmdlets</span></span>
        - <span data-ttu-id="74567-169">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="74567-169">New-AzVpnSiteLink</span></span>
        - <span data-ttu-id="74567-170">New-AzVpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="74567-170">New-AzVpnSiteLinkConnection</span></span>
    - <span data-ttu-id="74567-171">업데이트된 cmdlet:</span><span class="sxs-lookup"><span data-stu-id="74567-171">Updated cmdlet:</span></span>
        - <span data-ttu-id="74567-172">New-VpnSite</span><span class="sxs-lookup"><span data-stu-id="74567-172">New-VpnSite</span></span>
        - <span data-ttu-id="74567-173">Update-VpnSite</span><span class="sxs-lookup"><span data-stu-id="74567-173">Update-VpnSite</span></span>
        - <span data-ttu-id="74567-174">New-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="74567-174">New-VpnConnection</span></span>
        - <span data-ttu-id="74567-175">Update-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="74567-175">Update-VpnConnection</span></span>
* <span data-ttu-id="74567-176">AzureRM cmdlet 대신 Az cmdlet을 사용하도록 일부 PowerShell 예제의 문서가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="74567-176">Fixed documents for some PowerShell examples to use Az cmdlets instead of AzureRM cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="74567-177">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="74567-177">Az.RecoveryServices</span></span>
* <span data-ttu-id="74567-178">AzureVMpolicy 개체가 ProtectedItemsCount 특성으로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="74567-178">Update AzureVMpolicy Object with ProtectedItemsCount Attribute</span></span>
* <span data-ttu-id="74567-179">VM 정책 및 원래 스토리지 계정 복원에 대한 테스트가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="74567-179">Added Tests for VM policy and Original Storage Account Restore</span></span>

#### <a name="azresources"></a><span data-ttu-id="74567-180">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="74567-180">Az.Resources</span></span>
* <span data-ttu-id="74567-181">매개 변수 범위 없이 AzRoleAssignment를 호출할 수 없는 버그가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="74567-181">Fix bug where New-AzRoleAssignment could not be called without parameter Scope.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="74567-182">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="74567-182">Az.ServiceFabric</span></span>
* <span data-ttu-id="74567-183">'AzServiceFabricReliability' 참조 설명서에 대한 예제의 오타가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="74567-183">Fixed typo in example for 'Update-AzServiceFabricReliability' reference documentation</span></span>
* <span data-ttu-id="74567-184">애플리케이션 및 서비스를 관리하는 다음과 같은 새 cmdlet이 추가됩니다.</span><span class="sxs-lookup"><span data-stu-id="74567-184">Adding new cmdlets to manage appliaction and services:</span></span>
    - <span data-ttu-id="74567-185">New-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="74567-185">New-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="74567-186">New-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="74567-186">New-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="74567-187">New-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="74567-187">New-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="74567-188">New-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="74567-188">New-AzServiceFabricService</span></span>
    - <span data-ttu-id="74567-189">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="74567-189">Update-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="74567-190">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="74567-190">Get-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="74567-191">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="74567-191">Get-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="74567-192">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="74567-192">Get-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="74567-193">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="74567-193">Get-AzServiceFabricService</span></span>
    - <span data-ttu-id="74567-194">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="74567-194">Remove-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="74567-195">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="74567-195">Remove-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="74567-196">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="74567-196">Remove-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="74567-197">Remove-AzServiceFabricServic</span><span class="sxs-lookup"><span data-stu-id="74567-197">Remove-AzServiceFabricServic</span></span>
* <span data-ttu-id="74567-198">Service Fabric SDK가 Service Fabric 리소스 공급자 api 버전 2019-03-01을 사용하는 1.2.0 버전으로 업그레이드되었습니다.</span><span class="sxs-lookup"><span data-stu-id="74567-198">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2019-03-01.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="74567-199">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="74567-199">Az.SignalR</span></span>
* <span data-ttu-id="74567-200">Update, Restart, CheckNameAvailability, GetUsage Cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="74567-200">Add Update, Restart, CheckNameAvailability, GetUsage Cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="74567-201">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="74567-201">Az.Sql</span></span>
* <span data-ttu-id="74567-202">'Get-AzSqlElasticPool'에 대한 참조 설명서의 예제가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="74567-202">Update example in reference documentation for 'Get-AzSqlElasticPool'</span></span>
* <span data-ttu-id="74567-203">탄력적 풀을 만드는 vCore 예제가 추가되었습니다(AzSqlElasticPool).</span><span class="sxs-lookup"><span data-stu-id="74567-203">Added vCore example to creating an elastic pool (New-AzSqlElasticPool).</span></span>
* <span data-ttu-id="74567-204">Set-AzSqlServerAdvancedThreatProtectionPolicy 및 Set-AzSqlDatabaseAdvancedThreatProtectionPolicy에서 EmailAddresses가 비어 있는 경우 EmailAddresses의 유효성을 검사하고 EmailAdmins가 false가 아닌지 확인하는 기능이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="74567-204">Remove the validation of EmailAddresses and the check that EmailAdmins is not false in case EmailAddresses is empty in Set-AzSqlServerAdvancedThreatProtectionPolicy and Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="74567-205">감사 범주를 사용하는 여러 진단 설정이 있는 경우 서버/데이터베이스 감사 설정을 제거하도록 설정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="74567-205">Enabled removal of server/database auditing settings when multiple diagnostic settings that enable audit category exist.</span></span>
* <span data-ttu-id="74567-206">여러 Sql 취약성 평가 cmdlet에서 이메일 주소 유효성 검사가 수정되었습니다(Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting 및 Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span><span class="sxs-lookup"><span data-stu-id="74567-206">Fix email addresses validation in multiple Sql Vulnerability Assessment cmdlets (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting and Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span></span>

#### <a name="azstorage"></a><span data-ttu-id="74567-207">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="74567-207">Az.Storage</span></span>
* <span data-ttu-id="74567-208">'Get-AzStorageAccountKey'에 대한 참조 설명서의 예제가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="74567-208">Updated example in reference documentation for 'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="74567-209">Azure 파일 업로드/다운에서, 원본 파일 SMB 속성(파일 특성, 파일 생성 시간, 파일을 마지막으로 쓴 시간)을 대상 파일에 보존하는 기능이 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="74567-209">In upload/Downalod Azure File,support perserve the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the destination file</span></span>
    -  <span data-ttu-id="74567-210">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="74567-210">Set-AzStorageFileContent</span></span>
    -  <span data-ttu-id="74567-211">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="74567-211">Get-AzStorageFileContent</span></span>
* <span data-ttu-id="74567-212">컨테이너가 사용되는 ImmutabilityPolicy에서 properties/metadate fail을 사용하여 블록 Blob 업로드가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="74567-212">Fix Upload block blob with properties/metadate fail on container enabled ImmutabilityPolicy.</span></span>
    -  <span data-ttu-id="74567-213">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="74567-213">Set-AzStorageBlobContent</span></span>
* <span data-ttu-id="74567-214">관리 평면 API를 사용하여 Azure 파일 공유 관리를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="74567-214">Support manage Azure File shares with Management plane API</span></span>
    -  <span data-ttu-id="74567-215">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="74567-215">New-AzRmStorageShare</span></span>
    -  <span data-ttu-id="74567-216">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="74567-216">Get-AzRmStorageShare</span></span>
    -  <span data-ttu-id="74567-217">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="74567-217">Update-AzRmStorageShare</span></span>
    -  <span data-ttu-id="74567-218">Remove-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="74567-218">Remove-AzRmStorageShare</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="74567-219">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="74567-219">Az.Websites</span></span>
* <span data-ttu-id="74567-220">앱을 새 ASP로 마이그레이션할 때 웹앱 태그가 삭제되는 이슈가 해결되었습니다.</span><span class="sxs-lookup"><span data-stu-id="74567-220">Fixing issue where webapp Tags were getting deleted when migrating App to new ASPwhere webapp Tags were getting deleted when migrating App to new ASP</span></span>
* <span data-ttu-id="74567-221">Linux와 Windows에서 모두 작동하도록 Publish-AzureWebapp이 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="74567-221">Fixing the Publish-AzureWebapp to work across Linux and windows</span></span>
* <span data-ttu-id="74567-222">'Get-AzWebAppPublishingProfile' 참조 설명서의 예제가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="74567-222">Update example in 'Get-AzWebAppPublishingProfile' reference documentation</span></span>

## <a name="260---august-2019"></a><span data-ttu-id="74567-223">2.6.0 - 2019년 8월</span><span class="sxs-lookup"><span data-stu-id="74567-223">2.6.0 - August 2019</span></span>
#### <a name="general"></a><span data-ttu-id="74567-224">일반</span><span class="sxs-lookup"><span data-stu-id="74567-224">General</span></span>
* <span data-ttu-id="74567-225">여러 모듈에서 기타 오타가 수정됨</span><span class="sxs-lookup"><span data-stu-id="74567-225">Fixed miscellaneous typos across numerous modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="74567-226">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="74567-226">Az.Accounts</span></span>
* <span data-ttu-id="74567-227">Azure Functions 인증에서 사용자가 할당한 MSI가 지원됨(# 9479)</span><span class="sxs-lookup"><span data-stu-id="74567-227">Support user-assigned MSI in Azure Functiosn Authentication (#9479)</span></span>

#### <a name="azaks"></a><span data-ttu-id="74567-228">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="74567-228">Az.Aks</span></span>
* <span data-ttu-id="74567-229">'Get-AzAks' 출력 관련 문제가 해결됨</span><span class="sxs-lookup"><span data-stu-id="74567-229">Fix issue with output for 'Get-AzAks'</span></span>
    * <span data-ttu-id="74567-230">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/9847 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="74567-230">More information here: https://github.com/Azure/azure-powershell/issues/9847</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="74567-231">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="74567-231">Az.ApiManagement</span></span>
* <span data-ttu-id="74567-232">문제 https://github.com/Azure/azure-powershell/issues/9351 수정</span><span class="sxs-lookup"><span data-stu-id="74567-232">Fix for issue https://github.com/Azure/azure-powershell/issues/9351</span></span>
    - <span data-ttu-id="74567-233">productId, apiId, groupId 및 userId에 대한 제한을 적용하지 않는 .Net NuGet 버전이 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="74567-233">Update .net nuget version, which does not enforce restrictions on productId, apiId, groupId and userId</span></span>
* <span data-ttu-id="74567-234">**Get-AzApiManagementProduct** - API를 사용하는 제품에 대한 쿼리 지원이 추가됨</span><span class="sxs-lookup"><span data-stu-id="74567-234">**Get-AzApiManagementProduct** - Added support for querying products using Api.</span></span>
  https://github.com/Azure/azure-powershell/issues/9482
* <span data-ttu-id="74567-235">**New-AzApiManagementApiRevision** - 새 API 수정(https://github.com/Azure/azure-powershell/issues/9752 )을 만들 때 ApiRevisionDescription이 설정되지 않은 문제가 해결됨</span><span class="sxs-lookup"><span data-stu-id="74567-235">**New-AzApiManagementApiRevision** - Fix for issue where ApiRevisionDescription was not being set when creating new api revision https://github.com/Azure/azure-powershell/issues/9752</span></span>
* <span data-ttu-id="74567-236">'PsApiManagementOAuth2AuthrozationServer' 모델의 오타가 'PsApiManagementOAuth2AuthorizationServer'로 수정됨</span><span class="sxs-lookup"><span data-stu-id="74567-236">Fixed typo in model 'PsApiManagementOAuth2AuthrozationServer' to 'PsApiManagementOAuth2AuthorizationServer'</span></span>

#### <a name="azbatch"></a><span data-ttu-id="74567-237">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="74567-237">Az.Batch</span></span>
* <span data-ttu-id="74567-238">도움말 메시지 및 설명서에서 Windows를 대문자로 시작하도록 오타가 수정됨</span><span class="sxs-lookup"><span data-stu-id="74567-238">Fixed typo in help message and documentation to capitalize Windows</span></span>

#### <a name="azcdn"></a><span data-ttu-id="74567-239">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="74567-239">Az.Cdn</span></span>
* <span data-ttu-id="74567-240">CDN 모듈 변환 도우미의 오타가 수정됨</span><span class="sxs-lookup"><span data-stu-id="74567-240">Fixed a typo in CDN module conversion helper</span></span>

#### <a name="azcompute"></a><span data-ttu-id="74567-241">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="74567-241">Az.Compute</span></span>
* <span data-ttu-id="74567-242">VmssId가 New-AzVMConfig cmdlet에 추가됨</span><span class="sxs-lookup"><span data-stu-id="74567-242">Add VmssId to New-AzVMConfig cmdlet</span></span>
* <span data-ttu-id="74567-243">TerminateScheduledEvents 및 TerminateScheduledEventNotBeforeTimeoutInMinutes 매개 변수가 New-AzVmssConfig 및 Update-AzVmss에 추가됨</span><span class="sxs-lookup"><span data-stu-id="74567-243">Add TerminateScheduledEvents and TerminateScheduledEventNotBeforeTimeoutInMinutes parameters to New-AzVmssConfig and Update-AzVmss</span></span>
* <span data-ttu-id="74567-244">HyperVGeneration 속성이 VM 이미지 개체에 추가됨</span><span class="sxs-lookup"><span data-stu-id="74567-244">Add HyperVGeneration property to VM image object</span></span>
* <span data-ttu-id="74567-245">Host 및 HostGroup 기능이 추가됨</span><span class="sxs-lookup"><span data-stu-id="74567-245">Add Host and HostGroup features</span></span>
    - <span data-ttu-id="74567-246">새 cmdlet:   New-AzHostGroup, New-AzHost, Get-AzHostGroup, Get-AzHost, Remove-AzHostGroup, Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="74567-246">New cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span></span>
    - <span data-ttu-id="74567-247">HostId 매개 변수가 New-AzVMConfig 및 New-AzVM 추가됨</span><span class="sxs-lookup"><span data-stu-id="74567-247">HostId parameter is added to New-AzVMConfig and New-AzVM</span></span>
* <span data-ttu-id="74567-248">'Invoke-AzVMRunCommand' 설명서의 예제에서 올바른 매개 변수 이름을 사용하도록 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="74567-248">Update example in 'Invoke-AzVMRunCommand' documentation to use correct parameter name</span></span>
* <span data-ttu-id="74567-249">'Set-AzVMDiskEncryptionExtension' 및 'Set-AzVmssDiskEncryptionExtension' 참조 설명서의 '-VolumeType' 설명이 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="74567-249">Update '-VolumeType' description in 'Set-AzVMDiskEncryptionExtension' and 'Set-AzVmssDiskEncryptionExtension' reference documentation</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="74567-250">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="74567-250">Az.DataFactory</span></span>
* <span data-ttu-id="74567-251">'New-AzDataFactoryEncryptValue' 설명서에서 'Windows'를 대문자로 시작하도록 오타가 수정됨</span><span class="sxs-lookup"><span data-stu-id="74567-251">Fix typo to capitalize 'Windows' in 'New-AzDataFactoryEncryptValue' documentation</span></span>
* <span data-ttu-id="74567-252">ADF .Net SDK 버전이 4.1.2로 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="74567-252">Updated ADF .Net SDK version to 4.1.2</span></span>
* <span data-ttu-id="74567-253">자체 호스팅 통합 런타임을 SSIS Integration Runtime의 프록시로 설정할 수 있도록 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' 및 'DataProxyStagingPath' 매개 변수가 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd에 추가됨</span><span class="sxs-lookup"><span data-stu-id="74567-253">Add parameter 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' and 'DataProxyStagingPath' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable set up Self-Hosted Integration Runtime as a proxy for SSIS Integration Runtime</span></span>
* <span data-ttu-id="74567-254">PSTriggerRun에서 트리거된 파이프라인, 메시지 및 속성을 표시하고, PSActivityRun에서 작업 유형을 표시하도록 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="74567-254">Updated PSTriggerRun to show the triggered pipelines, message and properties, and PSActivityRun to show the activity type</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="74567-255">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="74567-255">Az.DataLakeStore</span></span>
* <span data-ttu-id="74567-256">오류 또는 원격 예외에 대한 Get-DataLakeStoreDeletedItem 중단이 수정됨</span><span class="sxs-lookup"><span data-stu-id="74567-256">Fix hanging of Get-DataLakeStoreDeletedItem for any errors or remote exceptions.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="74567-257">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="74567-257">Az.EventHub</span></span>
* <span data-ttu-id="74567-258">#9658 문제 해결: Set-AzEventHubNetworkRuleSet의 VirtualNteworkRule 매개 변수에 대한 오타</span><span class="sxs-lookup"><span data-stu-id="74567-258">Fix for issue #9658 : Typo VirtualNteworkRule parameter in Set-AzEventHubNetworkRuleSet</span></span>
* <span data-ttu-id="74567-259">#9558 문제 해결: Set-AzEventHubNamespace에서 PUT 대신 PATCH가 사용됨</span><span class="sxs-lookup"><span data-stu-id="74567-259">Fix for issue #9558 : Set-AzEventHubNamespace is using PATCH instead of PUT</span></span>
* <span data-ttu-id="74567-260">EnableKafka 매개 변수가 Set-AzEventHubNamespace cmdlet에 추가됨</span><span class="sxs-lookup"><span data-stu-id="74567-260">added EnableKafka parameter to Set-AzEventHubNamespace cmdlet</span></span>
* <span data-ttu-id="74567-261">#9786 문제 해결: Listen(수신 대기) 전용 권한이 있는 규칙을 만들 수 없음</span><span class="sxs-lookup"><span data-stu-id="74567-261">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>

#### <a name="azmarketplaceordering"></a><span data-ttu-id="74567-262">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="74567-262">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="74567-263">'Azure'가 모두 소문자인 설명서의 오타가 수정됨</span><span class="sxs-lookup"><span data-stu-id="74567-263">Fixed documentation typo where 'Azure' was all lowercase letters</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="74567-264">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="74567-264">Az.Monitor</span></span>
* <span data-ttu-id="74567-265">도움말 설명서에서 잘못된 매개 변수 이름이 수정됨</span><span class="sxs-lookup"><span data-stu-id="74567-265">Fixed incorrect parameter name in help documentation</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="74567-266">Az.Network</span><span class="sxs-lookup"><span data-stu-id="74567-266">Az.Network</span></span>
* <span data-ttu-id="74567-267">New-AzPrivateLinkServiceIpConfig가 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="74567-267">Updated New-AzPrivateLinkServiceIpConfig</span></span>
    - <span data-ttu-id="74567-268">서버 쪽에서 사용되지 않으므로 'PublicIpAddress' 매개 변수가 사용되지 않음</span><span class="sxs-lookup"><span data-stu-id="74567-268">Deprecated the paramster 'PublicIpAddress' since this is never used in the server side.</span></span>
    - <span data-ttu-id="74567-269">현재 IP 구성이 기본 구성인지 여부를 나타내는 하나의 선택적 'Primary' 매개 변수가 추가됨</span><span class="sxs-lookup"><span data-stu-id="74567-269">Added one optional parameter 'Primary' that indicate the current ip configuration is primary one or not.</span></span>
* <span data-ttu-id="74567-270">SDK의 요청 오류 예외 처리가 향상됨 - 이전의 SDK 예외가 올바르게 처리되지 않아 주요 오류 세부 정보가 표시되지 않은 문제가 해결됨</span><span class="sxs-lookup"><span data-stu-id="74567-270">Improved handling of request error exception from SDK   -Fixes the issue that previously SDK exceptions aren't handled correctly which results in key error details not being displayed</span></span>
* <span data-ttu-id="74567-271">올바른 IPv6 접두사 길이를 확인하기 위해 Ipv6 IP 접두사에 대한 유효성 검사 논리가 조정됨</span><span class="sxs-lookup"><span data-stu-id="74567-271">Adjusted validation logic for Ipv6 IP Prefix to check for correct IPv6 prefix length.</span></span> 
* <span data-ttu-id="74567-272">Get-AzVirtualNetworkSubnetConfig가 업데이트됨: 서브넷 리소스 ID별로 가져오도록 설정되는 매개 변수 세트가 추가됨</span><span class="sxs-lookup"><span data-stu-id="74567-272">Updated Get-AzVirtualNetworkSubnetConfig: Added parameter set to get by subnet resource id.</span></span>
* <span data-ttu-id="74567-273">AzNetworkServiceTag의 Location(위치) 매개 변수에 대한 설명이 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="74567-273">Updated description of Location parameter for AzNetworkServiceTag</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="74567-274">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="74567-274">Az.OperationalInsights</span></span>
* <span data-ttu-id="74567-275">'New-AzOperationalInsightsLinuxSyslogDataSource'에 대한 설명서가 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="74567-275">Updated documentation for 'New-AzOperationalInsightsLinuxSyslogDataSource'</span></span>
    - <span data-ttu-id="74567-276">예제가 추가됨</span><span class="sxs-lookup"><span data-stu-id="74567-276">Added example</span></span>
    - <span data-ttu-id="74567-277">'-Name' 매개 변수에 대한 설명이 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="74567-277">Updated description for '-Name' parameter</span></span>
* <span data-ttu-id="74567-278">New-AzOperationalInsightsWindowsEventDataSource에 대한 예제가 추가됨</span><span class="sxs-lookup"><span data-stu-id="74567-278">Added an example for New-AzOperationalInsightsWindowsEventDataSource</span></span>
* <span data-ttu-id="74567-279">New-AzOperationalInsightsWindowsEventDataSource의 -Name 매개 변수에 대한 설명이 변경됨</span><span class="sxs-lookup"><span data-stu-id="74567-279">Changed the description of the -Name parameter for New-AzOperationalInsightsWindowsEventDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="74567-280">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="74567-280">Az.RecoveryServices</span></span>
* <span data-ttu-id="74567-281">'Get-AzRecoveryServicesBackupJobDetail.md'가 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="74567-281">Update 'Get-AzRecoveryServicesBackupJobDetail.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="74567-282">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="74567-282">Az.Resources</span></span>
* <span data-ttu-id="74567-283">Microsoft 리소스에 대한 새 2019-05-10 API 버전 지원이 추가됨</span><span class="sxs-lookup"><span data-stu-id="74567-283">Add support for new api version 2019-05-10 for Microsoft.Resource</span></span>
    - <span data-ttu-id="74567-284">변수, 리소스 및 속성에 대한 'copy.count = 0' 지원이 추가됨</span><span class="sxs-lookup"><span data-stu-id="74567-284">Add support for 'copy.count = 0' for variables, resources and properties</span></span>
    - <span data-ttu-id="74567-285">'condition = false' 또는 'copy.count = 0'인 리소스가 완료 모드에서 삭제됨</span><span class="sxs-lookup"><span data-stu-id="74567-285">Resources with 'condition = false' or 'copy.count = 0' will be deleted in complete mode</span></span>
* <span data-ttu-id="74567-286">정책을 구독 수준에서 도움말 문서에 할당하는 예제가 추가됨</span><span class="sxs-lookup"><span data-stu-id="74567-286">Add an example of assigning policy at subscription level to help doc</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="74567-287">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="74567-287">Az.ServiceBus</span></span>
* <span data-ttu-id="74567-288">#9658 문제 해결: Set-AzServiceBusNetworkRuleSet의 VirtualNetworkRule 매개 변수에 대한 오타</span><span class="sxs-lookup"><span data-stu-id="74567-288">Fix for issue #9658 : Typo VirtualNetworkRule parameter in Set-AzServiceBusNetworkRuleSet</span></span>
* <span data-ttu-id="74567-289">#9786 문제 해결: Listen(수신 대기) 전용 권한이 있는 규칙을 만들 수 없음</span><span class="sxs-lookup"><span data-stu-id="74567-289">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>
* <span data-ttu-id="74567-290">큐 및 토픽에 대한 이름 가용성을 확인하는 새 'Test-AzServiceBusNameAvailability' 명령이 추가됨</span><span class="sxs-lookup"><span data-stu-id="74567-290">Added new command 'Test-AzServiceBusNameAvailability' to check the name availability for queue and topic</span></span> 

#### <a name="azservicefabric"></a><span data-ttu-id="74567-291">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="74567-291">Az.ServiceFabric</span></span>
* <span data-ttu-id="74567-292">노드 유형 추가 cmdlet 버그 수정:</span><span class="sxs-lookup"><span data-stu-id="74567-292">Fix add node type cmdlet bugs:</span></span>
    - <span data-ttu-id="74567-293">서비스 패브릭 클러스터와 관련이 없는 다른 vmss가 리소스 그룹에 있을 때 발생하는 NullReferenceException 버그</span><span class="sxs-lookup"><span data-stu-id="74567-293">NullReferenceException bug when resource group had other vmss not related to the service fabric cluster.</span></span> <span data-ttu-id="74567-294">문제 해결: https://github.com/Azure/azure-powershell/issues/8681</span><span class="sxs-lookup"><span data-stu-id="74567-294">Fixes issue: https://github.com/Azure/azure-powershell/issues/8681</span></span>
    - <span data-ttu-id="74567-295">virtualNetwork가 클러스터의 다른 리소스 그룹에 있을 때 cmdlet이 실패하는 버그가 수정됨</span><span class="sxs-lookup"><span data-stu-id="74567-295">Fix bug where cmdlet failed if virtualNetwork was in a different resource group that the cluster.</span></span> <span data-ttu-id="74567-296">문제 해결: https://github.com/Azure/azure-powershell/issues/8407</span><span class="sxs-lookup"><span data-stu-id="74567-296">fixes issue: https://github.com/Azure/azure-powershell/issues/8407</span></span>
    - <span data-ttu-id="74567-297">Add-AzServiceFabricApplicationCertificate cmdlet이 사용되지 않음</span><span class="sxs-lookup"><span data-stu-id="74567-297">Deprecating Add-AzServiceFabricApplicationCertificate cmdlet</span></span>

#### <a name="azsql"></a><span data-ttu-id="74567-298">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="74567-298">Az.Sql</span></span>
* <span data-ttu-id="74567-299">이전의 Auditing(감사) cmdlet에 대한 설명서가 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="74567-299">Update documentation of old Auditing cmdlets.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="74567-300">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="74567-300">Az.Storage</span></span>
* <span data-ttu-id="74567-301">더 많은 시나리오를 cmdlet 예제에 추가하고 매개 변수 설명을 업데이트하여 Get/Close-AzStorageFileHandle에 대한 도움말이 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="74567-301">Update help for Get/Close-AzStorageFileHandle, by add more scenarios to cmdlet examples and update parameter descriptions</span></span>
* <span data-ttu-id="74567-302">Blob 업로드 및 Blob 복사에서 StandardBlobTier가 지원됨</span><span class="sxs-lookup"><span data-stu-id="74567-302">Support StandardBlobTier in upload blob and copy blob</span></span>
    -  <span data-ttu-id="74567-303">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="74567-303">Set-AzStorageBlobContent</span></span>
    -  <span data-ttu-id="74567-304">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="74567-304">Start-AzStorageBlobCopy</span></span>
* <span data-ttu-id="74567-305">Blob 복사에서 우선 순위 리하이드레이션이 지원됨</span><span class="sxs-lookup"><span data-stu-id="74567-305">Support Rehydrate Priority in copy blob</span></span>
    -  <span data-ttu-id="74567-306">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="74567-306">Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="74567-307">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="74567-307">Az.Websites</span></span>
* <span data-ttu-id="74567-308">Set-AzWebApp 및 Set-AzWebAppSlot에서 -AppSettings 매개 변수에 대한 설명이 추가됨</span><span class="sxs-lookup"><span data-stu-id="74567-308">Add clarification around -AppSettings parameter in Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <a name="250---july-2019"></a><span data-ttu-id="74567-309">2.5.0 - 2019년 7월</span><span class="sxs-lookup"><span data-stu-id="74567-309">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="74567-310">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="74567-310">Az.Accounts</span></span>
* <span data-ttu-id="74567-311">ClientRuntime의 최신 버전을 사용하도록 일반적인 코드를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="74567-311">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="74567-312">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="74567-312">Az.ApplicationInsights</span></span>
* <span data-ttu-id="74567-313">'Remove-AzApplicationInsightsApiKey' 설명서의 예제 오타 수정</span><span class="sxs-lookup"><span data-stu-id="74567-313">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span> 

#### <a name="azautomation"></a><span data-ttu-id="74567-314">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="74567-314">Az.Automation</span></span>
* <span data-ttu-id="74567-315">리소스 문자열의 오타 수정</span><span class="sxs-lookup"><span data-stu-id="74567-315">Fix typo in resource string</span></span> 

#### <a name="azcognitiveservices"></a><span data-ttu-id="74567-316">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="74567-316">Az.CognitiveServices</span></span>
* <span data-ttu-id="74567-317">NetworkRuleSet 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="74567-317">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="74567-318">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="74567-318">Az.Compute</span></span>
* <span data-ttu-id="74567-319">VM 인스턴스 보기 개체의 누락된 속성(ComputerName, OsName, OsVersion 및 HyperVGeneration)을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="74567-319">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="74567-320">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="74567-320">Az.ContainerRegistry</span></span>
* <span data-ttu-id="74567-321">복제 매개 변수의 Remove-AzContainerRegistryReplication에서 오타 수정</span><span class="sxs-lookup"><span data-stu-id="74567-321">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="74567-322">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/9633 을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="74567-322">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="74567-323">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="74567-323">Az.DataFactory</span></span>
* <span data-ttu-id="74567-324">ADF .Net SDK 버전을 4.1.0으로 업데이트</span><span class="sxs-lookup"><span data-stu-id="74567-324">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="74567-325">'Get-AzDataFactoryV2PipelineRun' 설명서의 오타 수정</span><span class="sxs-lookup"><span data-stu-id="74567-325">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="74567-326">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="74567-326">Az.EventHub</span></span>
* <span data-ttu-id="74567-327">SAS 토큰을 생성하기 위해 추가된 새로운 cmmdlet 추가: New-AzEventHubAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="74567-327">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="74567-328">'관리'만 지정된 경우 authorizationrules 권한에 대한 확인 및 오류 메시지 추가</span><span class="sxs-lookup"><span data-stu-id="74567-328">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="74567-329">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="74567-329">Az.KeyVault</span></span>
* <span data-ttu-id="74567-330">인증서 정책에 대한 KeySize 지정을 위한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="74567-330">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="74567-331">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="74567-331">Az.LogicApp</span></span>
* <span data-ttu-id="74567-332">모든 맵 유형을 나열하도록 Get-AzIntegrationAccountMap 수정</span><span class="sxs-lookup"><span data-stu-id="74567-332">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="74567-333">필터링을 위해 새 MapType 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="74567-333">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="74567-334">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="74567-334">Az.ManagedServices</span></span>
* <span data-ttu-id="74567-335">API 버전 2019-06-01(GA)에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="74567-335">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="74567-336">Az.Network</span><span class="sxs-lookup"><span data-stu-id="74567-336">Az.Network</span></span>
* <span data-ttu-id="74567-337">프라이빗 엔드포인트 및 프라이빗 링크 서비스에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="74567-337">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="74567-338">새 cmdlet</span><span class="sxs-lookup"><span data-stu-id="74567-338">New cmdlets</span></span>
        - <span data-ttu-id="74567-339">Set-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="74567-339">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="74567-340">Set-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="74567-340">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="74567-341">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="74567-341">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="74567-342">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="74567-342">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="74567-343">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="74567-343">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="74567-344">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="74567-344">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="74567-345">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="74567-345">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="74567-346">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="74567-346">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="74567-347">기능에 대한 새로운 명령이 업데이트됨: Virtualnetwork의 서브넷에 있는 PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies 플래그</span><span class="sxs-lookup"><span data-stu-id="74567-347">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="74567-348">업데이트된 New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="74567-348">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="74567-349">이 서브넷의 프라이빗 엔드포인트에 네트워크 정책을 적용할지 여부를 나타내는 선택적 매개 변수 -PrivateEndpointNetworkPoliciesFlag가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="74567-349">Added optional parameter -PrivateEndpointNetworkPoliciesFlag that configures whether to apply network policies on private endpoint in this subnet.</span></span>
        - <span data-ttu-id="74567-350">이 서브넷의 프라이빗 연결 서비스에 네트워크 정책을 적용할지 여부를 나타내는 선택적 매개 변수 -PrivateLinkServiceNetworkPoliciesFlag가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="74567-350">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag that configures whether to apply network policies network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="74567-351">AzPrivateLinkService의 cmdlet 매개 변수 'ServiceName'이 이전 버전과의 호환성을 위해 별칭 'ServiceName'을 사용한 'Name'으로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="74567-351">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="74567-352">네트워크 보안 규칙 구성에 ICMP 프로토콜 사용</span><span class="sxs-lookup"><span data-stu-id="74567-352">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="74567-353">다음 Cmdlet이 업데이트 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="74567-353">Updated cmdlets</span></span>
        - <span data-ttu-id="74567-354">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="74567-354">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="74567-355">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="74567-355">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="74567-356">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="74567-356">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="74567-357">New-AzVirtualNetworkGatewayConnection에 대한 구성 가능한 매개 변수로 ConnectionProtocolType (Ikev1/Ikev2) 추가</span><span class="sxs-lookup"><span data-stu-id="74567-357">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="74567-358">LoadBalancerFrontendIpConfiguration에 PrivateIpAddressVersion 추가</span><span class="sxs-lookup"><span data-stu-id="74567-358">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="74567-359">업데이트된 cmdlet:</span><span class="sxs-lookup"><span data-stu-id="74567-359">Updated cmdlet:</span></span>
        - <span data-ttu-id="74567-360">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="74567-360">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="74567-361">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="74567-361">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="74567-362">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="74567-362">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="74567-363">프로브에서 사용자 지정 포트를 지원하기 위한 Application Gateway New-AzApplicationGatewayProbeConfig 명령 업데이트</span><span class="sxs-lookup"><span data-stu-id="74567-363">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="74567-364">업데이트된 New-AzApplicationGatewayProbeConfig: 백 엔드 서버 검색에 사용되는 선택적 매개 변수 포트가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="74567-364">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="74567-365">이 매개 변수는 Standard_V2 및 WAF_V2 SKU에 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="74567-365">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="74567-366">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="74567-366">Az.OperationalInsights</span></span>
* <span data-ttu-id="74567-367">저장된 검색의 기본 버전이 1로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="74567-367">Updated default version for saved searches to be 1.</span></span> 
* <span data-ttu-id="74567-368">사용자 지정 로그 null regex 처리가 수정됨</span><span class="sxs-lookup"><span data-stu-id="74567-368">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="74567-369">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="74567-369">Az.RecoveryServices</span></span>
* <span data-ttu-id="74567-370">'Get-AzRecoveryServicesBackupJob.md' 업데이트</span><span class="sxs-lookup"><span data-stu-id="74567-370">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="74567-371">'Get-AzRecoveryServicesBackupContainer.md' 업데이트</span><span class="sxs-lookup"><span data-stu-id="74567-371">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="74567-372">'Get-AzRecoveryServicesVault.md' 업데이트</span><span class="sxs-lookup"><span data-stu-id="74567-372">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="74567-373">'Wait-AzRecoveryServicesBackupJob.md' 업데이트</span><span class="sxs-lookup"><span data-stu-id="74567-373">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="74567-374">'Set-AzRecoveryServicesVaultContext.md' 업데이트</span><span class="sxs-lookup"><span data-stu-id="74567-374">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="74567-375">'Get-AzRecoveryServicesBackupItem.md' 업데이트</span><span class="sxs-lookup"><span data-stu-id="74567-375">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="74567-376">'Get-AzRecoveryServicesBackupRecoveryPoint.md' 업데이트</span><span class="sxs-lookup"><span data-stu-id="74567-376">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="74567-377">'Restore-AzRecoveryServicesBackupItem.md' 업데이트</span><span class="sxs-lookup"><span data-stu-id="74567-377">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="74567-378">Azure 파일 공유용 컨테이너를 등록 취소하기 위해 서비스 요청 업데이트</span><span class="sxs-lookup"><span data-stu-id="74567-378">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="74567-379">'Set-AzRecoveryServicesAsrAlertSetting.md' 업데이트</span><span class="sxs-lookup"><span data-stu-id="74567-379">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="74567-380">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="74567-380">Az.Resources</span></span>
- <span data-ttu-id="74567-381">'New-AzResourceGroupDeployment' 설명서에서 참조된 누락 cmdlet 제거</span><span class="sxs-lookup"><span data-stu-id="74567-381">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="74567-382">새 API 버전 2019-01-01을 사용하도록 정책 cmdlet 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="74567-382">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="74567-383">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="74567-383">Az.ServiceBus</span></span>
* <span data-ttu-id="74567-384">SAS 토큰을 생성하기 위해 추가된 새로운 cmmdlet 추가: New-AzServiceBusAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="74567-384">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="74567-385">'관리'만 지정된 경우 authorizationrules 권한에 대한 확인 및 오류 메시지 추가</span><span class="sxs-lookup"><span data-stu-id="74567-385">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="74567-386">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="74567-386">Az.Sql</span></span>
* <span data-ttu-id="74567-387">Set-AzSqlDatabaseSecondary cmdlet에 대한 누락된 예제 수정</span><span class="sxs-lookup"><span data-stu-id="74567-387">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="74567-388">이메일 주소를 제공하지 않고 설정된 취약성 평가 반복 검색 수정</span><span class="sxs-lookup"><span data-stu-id="74567-388">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="74567-389">경고 메시지의 작은 오타를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="74567-389">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="74567-390">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="74567-390">Az.Storage</span></span>
* <span data-ttu-id="74567-391">'Get-AzStorageAccount'에 대한 참조 설명서의 예제를 업데이트하여 올바른 매개 변수 이름 사용</span><span class="sxs-lookup"><span data-stu-id="74567-391">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="74567-392">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="74567-392">Az.StorageSync</span></span>
* <span data-ttu-id="74567-393">Invoke-AzStorageSyncChangeDetection cmdlet을 추가하는 중입니다.</span><span class="sxs-lookup"><span data-stu-id="74567-393">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="74567-394">TierFilesOlderThanDays를 기념하는 문제 9551 수정</span><span class="sxs-lookup"><span data-stu-id="74567-394">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="74567-395">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="74567-395">Az.Websites</span></span>
* <span data-ttu-id="74567-396">Get-AzWebApp 및 Set-AzWebApp에서 일부 SiteConfig 속성을 반환하지 않은 버그 수정</span><span class="sxs-lookup"><span data-stu-id="74567-396">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="74567-397">Get-AzDeletedWebApp 및 Restore-AzDeletedWebApp에 새 위치 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="74567-397">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="74567-398">AzWebApp-IncludeSourceWebAppSlots을 사용하여 웹앱 슬롯을 복제하는 버그를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="74567-398">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="74567-399">2.4.0 - 2019년 7월</span><span class="sxs-lookup"><span data-stu-id="74567-399">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="74567-400">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="74567-400">Az.Accounts</span></span>
* <span data-ttu-id="74567-401">프로필 cmdlet에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="74567-401">Add support for profile cmdlets</span></span>
* <span data-ttu-id="74567-402">생성된 cmdlet에서 환경 및 데이터 평면에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="74567-402">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="74567-403">Windows PowerShell의 데이터 평면 cmdlet에대해 일부 경우 잘못된 엔드포인트가 사용되는 버그 수정</span><span class="sxs-lookup"><span data-stu-id="74567-403">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="74567-404">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="74567-404">Az.Advisor</span></span>
* <span data-ttu-id="74567-405">Az.Advisor의 GA 릴리스</span><span class="sxs-lookup"><span data-stu-id="74567-405">GA release of Az.Advisor</span></span>
* <span data-ttu-id="74567-406">이 모듈은 이제 롤업 `Az` 모듈의 일부로 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="74567-406">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="74567-407">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="74567-407">Az.ApiManagement</span></span>
* <span data-ttu-id="74567-408">문제 https://github.com/Azure/azure-powershell/issues/8671 수정</span><span class="sxs-lookup"><span data-stu-id="74567-408">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="74567-409">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="74567-409">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="74567-410">사용자 및 제품별 구독을 쿼리하기 위한 지원이 추가됨</span><span class="sxs-lookup"><span data-stu-id="74567-410">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="74567-411">범위 '/', '/ api, '/ api/echo api'를 사용하여 쿼리하기 위한 지원이 추가됨</span><span class="sxs-lookup"><span data-stu-id="74567-411">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="74567-412">[https://github.com/Azure/azure-powershell/issues/9307](https://github.com/Azure/azure-powershell/issues/9307 ) 및 https://github.com/Azure/azure-powershell/issues/8432 문제 수정</span><span class="sxs-lookup"><span data-stu-id="74567-412">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="74567-413">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="74567-413">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="74567-414">Apis를 가져올 때 'ApiVersion' 및 'ApiVersionSetId'를 지정하기 위한 지원이 추가됨</span><span class="sxs-lookup"><span data-stu-id="74567-414">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="74567-415">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="74567-415">Az.Automation</span></span>
* <span data-ttu-id="74567-416">문자열 값을 처리하기 위해 Set-AzAutomationConnectionFieldValue cmdlet 버그를 수정했습니다.</span><span class="sxs-lookup"><span data-stu-id="74567-416">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="74567-417">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="74567-417">Az.Compute</span></span>
* <span data-ttu-id="74567-418">New-AzImageConfig에 HyperVGeneration 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="74567-418">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="74567-419">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="74567-419">Az.DataFactory</span></span>
* <span data-ttu-id="74567-420">get activity runs, get pipeline runs, get trigger runs ADF cmdlet의 출력을 업데이트하여 Select-Object pipe를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="74567-420">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="74567-421">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="74567-421">Az.EventGrid</span></span>
* <span data-ttu-id="74567-422">'New-AzEventGridSubcription' 설명서의 오타 수정</span><span class="sxs-lookup"><span data-stu-id="74567-422">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="74567-423">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="74567-423">Az.IotHub</span></span>
* <span data-ttu-id="74567-424">권한 부여 정책 키를 다시 생성하기 위한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="74567-424">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="74567-425">Az.Network</span><span class="sxs-lookup"><span data-stu-id="74567-425">Az.Network</span></span>
* <span data-ttu-id="74567-426">'RoutingPreference'를 공용 IP 태그에 추가함</span><span class="sxs-lookup"><span data-stu-id="74567-426">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="74567-427">'Get-AzNetworkServiceTag' 참조 설명서의 예제 개선</span><span class="sxs-lookup"><span data-stu-id="74567-427">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="74567-428">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="74567-428">Az.PolicyInsights</span></span>
* <span data-ttu-id="74567-429">Get-AzPolicyState의 null 참조 문제 해결</span><span class="sxs-lookup"><span data-stu-id="74567-429">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="74567-430">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/9446 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="74567-430">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="74567-431">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="74567-431">Az.OperationalInsights</span></span>
* <span data-ttu-id="74567-432">Get-AzOperationalInsightsDataSource에 반환된 CustomLog datasource 모델 수정됨</span><span class="sxs-lookup"><span data-stu-id="74567-432">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="74567-433">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="74567-433">Az.RecoveryServices</span></span>
* <span data-ttu-id="74567-434">IaaSVMs에 대한 get-policy 명령 수정</span><span class="sxs-lookup"><span data-stu-id="74567-434">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="74567-435">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="74567-435">Az.Resources</span></span>
    - <span data-ttu-id="74567-436">Get-AzPolicyState -Top 매개 변수에 대한 도움말 텍스트 수정</span><span class="sxs-lookup"><span data-stu-id="74567-436">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="74567-437">Get-AzPolicyAlias에 대한 클라이언트 쪽 페이징 지원 추가</span><span class="sxs-lookup"><span data-stu-id="74567-437">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="74567-438">Set-AzPolicyAssignment, -PolicyParameters 및 -PolicyParametersObject에 대한 새 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="74567-438">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="74567-439">Policy cmdlet에 대한 몇 가지 문서 및 예제 업데이트</span><span class="sxs-lookup"><span data-stu-id="74567-439">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="74567-440">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="74567-440">Az.ServiceBus</span></span>
* <span data-ttu-id="74567-441">문제 #4938 수정 - MaxSizeInMegabytes를 설정할 때 New-AzureRmServiceBusQueue가 BadRequest 반환</span><span class="sxs-lookup"><span data-stu-id="74567-441">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="74567-442">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="74567-442">Az.Sql</span></span>
* <span data-ttu-id="74567-443">미리 보기 릴리스에서 공개 릴리스로 인스턴스 장애 조치(Failover) 그룹 cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="74567-443">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="74567-444">새 cmdlet으로 Azure SQL Server\Database Auditing을 지원하세요.</span><span class="sxs-lookup"><span data-stu-id="74567-444">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="74567-445">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="74567-445">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="74567-446">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="74567-446">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="74567-447">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="74567-447">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="74567-448">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="74567-448">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="74567-449">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="74567-449">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="74567-450">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="74567-450">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="74567-451">취약성 평가 설정에서 이메일 제약 조건 제거</span><span class="sxs-lookup"><span data-stu-id="74567-451">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="74567-452">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="74567-452">Az.Storage</span></span>
* <span data-ttu-id="74567-453">다음 cmdlet에서 2개의 매개 변수 '-IndexDocument' 및 '-ErrorDocument404Path'를 필수에서 선택으로 변경하세요.</span><span class="sxs-lookup"><span data-stu-id="74567-453">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="74567-454">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="74567-454">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="74567-455">예제를 추가하여 Get-AzStorageBlobContent의 도움말 업데이트</span><span class="sxs-lookup"><span data-stu-id="74567-455">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="74567-456">StorageException으로 cmdlet이 실패한 경우 자세한 오류 정보 표시</span><span class="sxs-lookup"><span data-stu-id="74567-456">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="74567-457">Azure Files AAD DS 인증으로 스토리지 계정 생성 또는 업데이트 지원</span><span class="sxs-lookup"><span data-stu-id="74567-457">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="74567-458">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="74567-458">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="74567-459">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="74567-459">Set-AzStorageAccount</span></span>
* <span data-ttu-id="74567-460">파일 공유, 파일 디렉터리 또는 파일의 목록 지원 또는 파일 핸들 닫기</span><span class="sxs-lookup"><span data-stu-id="74567-460">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="74567-461">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="74567-461">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="74567-462">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="74567-462">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="74567-463">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="74567-463">Az.StorageSync</span></span>
* <span data-ttu-id="74567-464">이 모듈은 이제 롤업 `Az` 모듈의 일부로 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="74567-464">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="74567-465">2.3.2 - 2019년 6월</span><span class="sxs-lookup"><span data-stu-id="74567-465">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="74567-466">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="74567-466">Az.Accounts</span></span>
* <span data-ttu-id="74567-467">함수 호출에 대해 일부 경우 잘못된 URL이 사용되는 버그 수정</span><span class="sxs-lookup"><span data-stu-id="74567-467">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="74567-468">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/8983 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="74567-468">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="74567-469">AzureRM에서 Az cmdlet으로의 별칭 문제 해결</span><span class="sxs-lookup"><span data-stu-id="74567-469">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="74567-470">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="74567-470">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="74567-471">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="74567-471">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="74567-472">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="74567-472">Az.Compute</span></span>
* <span data-ttu-id="74567-473">New-AzVm 및 New-AzVmss 단순 매개 변수 집합은 이제 'ProximityPlacementGroup'매개 변수를 허용합니다.</span><span class="sxs-lookup"><span data-stu-id="74567-473">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="74567-474">'New-AzVM' 참조 설명서에서 오타 수정</span><span class="sxs-lookup"><span data-stu-id="74567-474">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="74567-475">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="74567-475">Az.Dns</span></span>
* <span data-ttu-id="74567-476">'Set-AzDnsZone' 도움말 예제의 오타가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="74567-476">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="74567-477">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="74567-477">Az.EventGrid</span></span>
* <span data-ttu-id="74567-478">2019-06-01 API 버전을 사용하도록 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="74567-478">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="74567-479">새 cmdlet:</span><span class="sxs-lookup"><span data-stu-id="74567-479">New cmdlets:</span></span>
    - <span data-ttu-id="74567-480">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="74567-480">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="74567-481">새 Azure Event Grid 도메인을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="74567-481">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="74567-482">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="74567-482">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="74567-483">Event Grid 도메인의 세부 정보를 가져오거나 현재 Azure 구독의 모든 Event Grid 도메인 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="74567-483">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="74567-484">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="74567-484">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="74567-485">Azure Event Grid 도메인을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="74567-485">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="74567-486">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="74567-486">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="74567-487">Azure Event Grid 도메인에 대한 공유 액세스 키를 다시 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="74567-487">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="74567-488">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="74567-488">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="74567-489">Event Grid 도메인 이벤트를 게시하는 데 사용되는 공유 액세스 키를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="74567-489">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="74567-490">New-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="74567-490">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="74567-491">새 Azure Event Grid 도메인 토픽을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="74567-491">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="74567-492">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="74567-492">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="74567-493">Event Grid 도메인 토픽의 세부 사항을 가져오거나, 현재 Azure의 특정 Event Grid 도메인 아래의 모든 Event Grid 도메인 토픽 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="74567-493">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span> 
    - <span data-ttu-id="74567-494">Remove-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="74567-494">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="74567-495">기존 Azure Event Grid 도메인 토픽을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="74567-495">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="74567-496">다음 Cmdlet이 업데이트 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="74567-496">Updated cmdlets:</span></span>
    - <span data-ttu-id="74567-497">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="74567-497">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="74567-498">새로운 Event Grid 도메인 및 Event Grid 도메인 토픽에 대한 파이핑을 지원하기 위해 새로운 필수 매개 변수를 추가하여 이러한 리소스 아래에 새 이벤트 구독을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="74567-498">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="74567-499">새로운 Event Grid 도메인 이름 및 Event Grid 도메인 토픽 이름을 지정하기 위해 새로운 필수 매개 변수를 추가하여 이러한 리소스 아래에 새 이벤트 구독을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="74567-499">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="74567-500">기존 매개 변수(예: EndPointType, SubjectBeginsWith 등)를 재사용할 수 있도록 도메인 및 도메인 토픽에 대한 새로운 매개 변수 집합을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="74567-500">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="74567-501">지정을 위한 새로운 선택적 매개 변수를 추가</span><span class="sxs-lookup"><span data-stu-id="74567-501">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="74567-502">이벤트 구독 만료 날짜,</span><span class="sxs-lookup"><span data-stu-id="74567-502">Event subscription expiration date,</span></span>
            - <span data-ttu-id="74567-503">고급 필터링 매개 변수.</span><span class="sxs-lookup"><span data-stu-id="74567-503">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="74567-504">대상으로 servicebusqueue에 대한 새 열거형을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="74567-504">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="74567-505">-IncludedEventType 옵션에서 'All' 사용을 허용하지 않고 다음으로 대체함</span><span class="sxs-lookup"><span data-stu-id="74567-505">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span> 
    - <span data-ttu-id="74567-506">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="74567-506">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="74567-507">결과 페이지 매김 및 필터링을 지원하는 새로운 선택적 매개 변수(Top, ODataQuery 및 NextLink)를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="74567-507">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="74567-508">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="74567-508">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="74567-509">Event Grid 도메인 및 Event Grid 도메인 토픽에 대한 파이핑을 지원하기 위해 새로운 필수 매개 변수를 추가하여 이러한 리소스 아래에 기존 이벤트 구독을 제거할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="74567-509">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="74567-510">Event Grid 도메인 이름 및 Event Grid 도메인 토픽 이름을 지정하기 위해 새로운 필수 매개 변수를 추가하여 이러한 리소스 아래에 기존 이벤트 구독을 제거할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="74567-510">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="74567-511">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="74567-511">Az.FrontDoor</span></span>
* <span data-ttu-id="74567-512">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="74567-512">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="74567-513">변환 지원 및 새 연산자 자동 완성 값(RegEx)을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="74567-513">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="74567-514">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="74567-514">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="74567-515">새 자동 완성 값 추가</span><span class="sxs-lookup"><span data-stu-id="74567-515">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="74567-516">Az.Network</span><span class="sxs-lookup"><span data-stu-id="74567-516">Az.Network</span></span>
* <span data-ttu-id="74567-517">Microsoft Azure Virtual Network 게이트웨이 리소스에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="74567-517">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="74567-518">새 cmdlet</span><span class="sxs-lookup"><span data-stu-id="74567-518">New cmdlets</span></span>
        - <span data-ttu-id="74567-519">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="74567-519">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="74567-520">AvailablePrivateEndpointType 추가</span><span class="sxs-lookup"><span data-stu-id="74567-520">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="74567-521">새 cmdlet</span><span class="sxs-lookup"><span data-stu-id="74567-521">New cmdlets</span></span> 
        - <span data-ttu-id="74567-522">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="74567-522">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="74567-523">PrivatePrivateLinkService 추가</span><span class="sxs-lookup"><span data-stu-id="74567-523">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="74567-524">새 cmdlet</span><span class="sxs-lookup"><span data-stu-id="74567-524">New cmdlets</span></span> 
        - <span data-ttu-id="74567-525">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="74567-525">Get-AzPrivateLinkService</span></span> 
        - <span data-ttu-id="74567-526">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="74567-526">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="74567-527">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="74567-527">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="74567-528">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="74567-528">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="74567-529">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="74567-529">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="74567-530">PrivateEndpoint 추가</span><span class="sxs-lookup"><span data-stu-id="74567-530">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="74567-531">새 cmdlet</span><span class="sxs-lookup"><span data-stu-id="74567-531">New cmdlets</span></span>
        - <span data-ttu-id="74567-532">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="74567-532">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="74567-533">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="74567-533">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="74567-534">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="74567-534">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="74567-535">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="74567-535">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="74567-536">기능에 대한 새로운 명령이 업데이트됨: VpnConnection 상의 UseLocalAzureIpAddress 플래그</span><span class="sxs-lookup"><span data-stu-id="74567-536">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="74567-537">New-AzVpnConnection이 업데이트됨: 선택적 매개 변수 -UseLocalAzureIpAddress를 추가하여 로컬 Azure IP 주소가 연결을 시작하는 동안 소스 주소로 사용되어야 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="74567-537">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="74567-538">Set-AzVpnConnection이 업데이트됨: 선택적 매개 변수 -UseLocalAzureIpAddress를 추가하여 로컬 Azure IP 주소가 연결을 시작하는 동안 소스 주소로 사용되어야 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="74567-538">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="74567-539">ExpressRoute 피어링에 읽기 전용 필드 PeeredConnections가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="74567-539">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="74567-540">ExpressRoute에 읽기 전용 필드 GlobalReachEnabled가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="74567-540">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="74567-541">ExpressRouteCircuit 모델에서 AllowGlobalReach 필드의 사용 중단을 부르는 호환성이 손상되는 변경 속성이 추가됨</span><span class="sxs-lookup"><span data-stu-id="74567-541">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="74567-542">AzApplicationGatewayRedirectConfiguration cmdlet에서 TargetListenerID를 사용하는 중의 8756 오류 문제가 해결됨</span><span class="sxs-lookup"><span data-stu-id="74567-542">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="74567-543">다시 쓰기 규칙 세트가 설정되지 못하게 하는 New-AzApplicationGatewayPathRuleConfig의 버그를 수정했습니다.</span><span class="sxs-lookup"><span data-stu-id="74567-543">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="74567-544">NetworkInterfaceIpConfiguration에 VirtualNetworkTaps가 표시되는 방식이 수정됨</span><span class="sxs-lookup"><span data-stu-id="74567-544">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="74567-545">모든 파트를 나열하도록 Cortex Get cmdlet이 수정됨</span><span class="sxs-lookup"><span data-stu-id="74567-545">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="74567-546">ExpressRouteGateways, VpnGateway에 대한 VirtualHub 참조 생성 수정됨</span><span class="sxs-lookup"><span data-stu-id="74567-546">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="74567-547">AzureFirewall 및 NatGateway의 가용성 영역에 대한 지원 추가됨</span><span class="sxs-lookup"><span data-stu-id="74567-547">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="74567-548">Get-AzNetworkServiceTag cmdlet 추가됨</span><span class="sxs-lookup"><span data-stu-id="74567-548">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="74567-549">Azure Firewall에 대한 여러 공용 IP 주소에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="74567-549">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="74567-550">New-AzFirewall cmdlet이 업데이트됨:</span><span class="sxs-lookup"><span data-stu-id="74567-550">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="74567-551">하나 이상의 공용 IP 주소 개체를 허용하는 매개 변수 -PublicIpAddress 추가됨</span><span class="sxs-lookup"><span data-stu-id="74567-551">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="74567-552">Virtual Network 개체를 허용하는 매개 변수 -VirtualNetwork 추가됨</span><span class="sxs-lookup"><span data-stu-id="74567-552">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="74567-553">방화벽 개체에 AddPublicIpAddress 및 RemovePublicIpAddress 메서드 추가됨 - 공용 IP 주소 개체를 입력으로 허용</span><span class="sxs-lookup"><span data-stu-id="74567-553">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="74567-554">매개 변수 -PublicIpName 및 -VirtualNetworkName이 더 이상 사용되지 않음</span><span class="sxs-lookup"><span data-stu-id="74567-554">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span> 
* <span data-ttu-id="74567-555">기능에 대한 새로운 명령이 업데이트됨: VpnClient AAD 인증 옵션을 가상 네트워크 게이트웨이 리소스로 설정했습니다.</span><span class="sxs-lookup"><span data-stu-id="74567-555">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span> 
    - <span data-ttu-id="74567-556">New-AzVirtualNetworkGateway가 업데이트됨: 게이트웨이에서 VpnClient AAD 인증 옵션을 설정할 수 있도록 선택적 매개 변수 AadTenantUri, AadAudienceId, AadIssuerUri가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="74567-556">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="74567-557">Set-AzVirtualNetworkGateway가 업데이트됨: 게이트웨이에서 VpnClient AAD 인증 옵션을 설정할 수 있도록 선택적 매개 변수 AadTenantUri, AadAudienceId, AadIssuerUri가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="74567-557">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="74567-558">Set-AzVirtualNetworkGateway가 업데이트됨: 게이트웨이에서 VpnClient AAD 인증 옵션을 제거할 수 있도록 선택적인 스위치 매개 변수 RemoveAadAuthentication이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="74567-558">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="74567-559">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="74567-559">Az.OperationalInsights</span></span>
* <span data-ttu-id="74567-560">'New-AzureRmOperationalInsightsWorkspace' 명령에서 **pergb2018** 가격 책정 계층 사용</span><span class="sxs-lookup"><span data-stu-id="74567-560">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="74567-561">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="74567-561">Az.Resources</span></span>
* <span data-ttu-id="74567-562">추가 템플릿 내보내기 옵션 지원</span><span class="sxs-lookup"><span data-stu-id="74567-562">Support for additional Template Export options</span></span>
    - <span data-ttu-id="74567-563">Export-AzResourceGroup에 '-SkipResourceNameParameterization' 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="74567-563">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="74567-564">Export-AzResourceGroup에 '-SkipAllParameterization' 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="74567-564">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="74567-565">내보낸 리소스 필터링을 위해 Export-AzResourceGroup에 '-Resource' 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="74567-565">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="74567-566">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="74567-566">Az.ServiceFabric</span></span>
* <span data-ttu-id="74567-567">일부 경우 잘못된 지문을 가져오는 추가 인증서 ByExistingKeyVault 수정</span><span class="sxs-lookup"><span data-stu-id="74567-567">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="74567-568">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="74567-568">Az.Sql</span></span>
* <span data-ttu-id="74567-569">Advanced Threat Protection 스토리지 엔드포인트 접미사 수정</span><span class="sxs-lookup"><span data-stu-id="74567-569">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="74567-570">Advanced Data Security가 Advanced Threat Protection 정책을 재정의하는 것을 수정</span><span class="sxs-lookup"><span data-stu-id="74567-570">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="74567-571">고객이 TDE 키를 추가하고 관리되는 인스턴스에 TDE 보호기를 설정할 수 있도록 Management.Sql용 새 Cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="74567-571">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="74567-572">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="74567-572">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="74567-573">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="74567-573">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="74567-574">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="74567-574">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="74567-575">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="74567-575">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="74567-576">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="74567-576">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="74567-577">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="74567-577">Az.Storage</span></span>
* <span data-ttu-id="74567-578">스토리지 계정 생성 시 종류 FileStorage 및 SkuName Premium_ZRS 지원</span><span class="sxs-lookup"><span data-stu-id="74567-578">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="74567-579">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="74567-579">New-AzStorageAccount</span></span>
* <span data-ttu-id="74567-580">BLOB immutability cmdlet의 설명 명확화</span><span class="sxs-lookup"><span data-stu-id="74567-580">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="74567-581">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="74567-581">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="74567-582">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="74567-582">Az.Websites</span></span>
* <span data-ttu-id="74567-583">Get-AzWebAppCertificate를 클라이언트 대신 서버의 리소스 그룹별로 필터링하도록 최적화</span><span class="sxs-lookup"><span data-stu-id="74567-583">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="74567-584">Get-AzWebAppSnapshot에 -UseDisasterRecovery 스위치 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="74567-584">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="74567-585">2.2.0 - 2019년 6월</span><span class="sxs-lookup"><span data-stu-id="74567-585">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="74567-586">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="74567-586">Az.Cdn</span></span>
* <span data-ttu-id="74567-587">cmdlet에서 2019-04-15 API 버전 기반의 rulesEngine 기능을 지원하도록 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="74567-587">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="74567-588">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="74567-588">Az.Compute</span></span>
* <span data-ttu-id="74567-589">작업을 시작하여 완료되기 전에 즉시 반환하는 `NoWait` 매개 변수가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="74567-589">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="74567-590">다음 Cmdlet이 업데이트 되었습니다.   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="74567-590">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="74567-591">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="74567-591">Az.EventHub</span></span>
* <span data-ttu-id="74567-592">#9231 수정 - Get-AzEventHubNamespace에서 태그를 반환하지 않음</span><span class="sxs-lookup"><span data-stu-id="74567-592">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="74567-593">#9230 수정 - Get-AzEventHubNamespace에서 ResourceGroupName 대신 ResourceGroup을 반환함</span><span class="sxs-lookup"><span data-stu-id="74567-593">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="74567-594">Az.Network</span><span class="sxs-lookup"><span data-stu-id="74567-594">Az.Network</span></span>
* <span data-ttu-id="74567-595">Nat Gateway에 대한 ResourceId 및 InputObject 업데이트</span><span class="sxs-lookup"><span data-stu-id="74567-595">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="74567-596">ResourceId 및 InputObject에 대한 별칭 추가</span><span class="sxs-lookup"><span data-stu-id="74567-596">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="74567-597">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="74567-597">Az.PolicyInsights</span></span>
* <span data-ttu-id="74567-598">Get-AzPolicyEvent에서 Null 참조 문제 해결</span><span class="sxs-lookup"><span data-stu-id="74567-598">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="74567-599">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="74567-599">Az.RecoveryServices</span></span>
* <span data-ttu-id="74567-600">IaaSVM 정책 최소 보존 기간(일)이 1에서 7로 변경됨</span><span class="sxs-lookup"><span data-stu-id="74567-600">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="74567-601">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="74567-601">Az.ServiceBus</span></span>
* <span data-ttu-id="74567-602">#9182 문제 해결 - Get-AzServiceBusNamespace에서 ResourceGroupName 대신 ResourceGroup을 반환</span><span class="sxs-lookup"><span data-stu-id="74567-602">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="74567-603">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="74567-603">Az.ServiceFabric</span></span>
* <span data-ttu-id="74567-604">'Update-AzServiceFabricReliability' 오류 메시지의 오타 수정</span><span class="sxs-lookup"><span data-stu-id="74567-604">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="74567-605">Service Fabric 명령줄에서 누락된 문자 수정</span><span class="sxs-lookup"><span data-stu-id="74567-605">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="74567-606">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="74567-606">Az.Sql</span></span>
* <span data-ttu-id="74567-607">Managed Instance에 대한 AutoDr을 지원하기 위해 New-AzureSqlInstance cmdlet에 대한 DnsZonePartner 매개 변수를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="74567-607">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="74567-608">Get-AzSqlDatabaseSecureConnectionPolicy cmdlet 사용 중단</span><span class="sxs-lookup"><span data-stu-id="74567-608">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="74567-609">Threat Detection(위협 탐지) cmdlet 이름을 Advanced Threat Protection으로 변경함</span><span class="sxs-lookup"><span data-stu-id="74567-609">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="74567-610">새 AzSqlInstance -StorageSizeInGB 및 -LicenseType 매개 변수는 이제 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="74567-610">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="74567-611">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="74567-611">Az.Websites</span></span>
* <span data-ttu-id="74567-612">-WebApp 속성에서 Set-AzWebApp 및 Set-AzWebAppSlot을 사용하면 태그가 제거되는 문제를 해결함</span><span class="sxs-lookup"><span data-stu-id="74567-612">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="74567-613">2.1.0 - 2019년 5월</span><span class="sxs-lookup"><span data-stu-id="74567-613">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="74567-614">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="74567-614">Az.ApiManagement</span></span>
* <span data-ttu-id="74567-615">글로벌 및 API 범위에서 진단을 관리하기 위한 새 cmdlet을 만들었습니다.</span><span class="sxs-lookup"><span data-stu-id="74567-615">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="74567-616">**Get-AzApiManagementDiagnostic** - 글로벌 또는 API 범위가 구성된 진단 가져오기</span><span class="sxs-lookup"><span data-stu-id="74567-616">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="74567-617">**New-AzApiManagementDiagnostic** - 글로벌 범위 또는 API 범위에서 새 진단 만들기</span><span class="sxs-lookup"><span data-stu-id="74567-617">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="74567-618">**New-AzApiManagementHttpMessageDiagnostic** - 기록할 Headers(헤더) 및 Body Bytes(본문 바이트 수) 크기에 대한 진단 설정 만들기</span><span class="sxs-lookup"><span data-stu-id="74567-618">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="74567-619">**New-AzApiManagementPipelineDiagnosticSetting** - 게이트웨이로 들어오고 나가는 HTTP 메시지에 대한 진단 설정 만들기</span><span class="sxs-lookup"><span data-stu-id="74567-619">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="74567-620">**New-AzApiManagementSamplingSetting** - 진단 요청/응답에 대한 샘플링 설정 만들기</span><span class="sxs-lookup"><span data-stu-id="74567-620">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="74567-621">**Remove-AzApiManagementDiagnostic** - 글로벌 또는 API 범위에서 진단 엔터티 제거</span><span class="sxs-lookup"><span data-stu-id="74567-621">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="74567-622">**Set-AzApiManagementDiagnostic** - 글로벌 또는 API 범위에서 진단 엔터티 업데이트</span><span class="sxs-lookup"><span data-stu-id="74567-622">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="74567-623">ApiManagement 서비스에서 캐시를 관리하기 위한 새 cmdlet을 만들었습니다.</span><span class="sxs-lookup"><span data-stu-id="74567-623">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="74567-624">**Get-AzApiManagementCache** - 식별자 또는 모든 캐시로 지정된 캐시의 세부 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="74567-624">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="74567-625">**New-AzApiManagementCache** - 특정 Azure 'region'(지역)에 새 'default'(기본) 캐시 만들기</span><span class="sxs-lookup"><span data-stu-id="74567-625">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="74567-626">**Remove-AzApiManagementCache** - 캐시 제거</span><span class="sxs-lookup"><span data-stu-id="74567-626">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="74567-627">**Update-AzApiManagementCache** - 캐시 업데이트</span><span class="sxs-lookup"><span data-stu-id="74567-627">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="74567-628">API 스키마 관리하기 위한 새 cmdlet을 만들었습니다.</span><span class="sxs-lookup"><span data-stu-id="74567-628">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="74567-629">**New-AzApiManagementSchema** - API에 대한 새 스키마 만들기</span><span class="sxs-lookup"><span data-stu-id="74567-629">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="74567-630">**Get-AzApiManagementSchema** - API에 구성된 스키마 가져오기</span><span class="sxs-lookup"><span data-stu-id="74567-630">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="74567-631">**Remove-AzApiManagementSchema** - API에 구성된 스키마 제거</span><span class="sxs-lookup"><span data-stu-id="74567-631">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="74567-632">**Set-AzApiManagementSchema** - API에 구성된 스키마 업데이트</span><span class="sxs-lookup"><span data-stu-id="74567-632">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="74567-633">사용자 토큰을 생성하기 위한 새 cmdlet을 만들었습니다.</span><span class="sxs-lookup"><span data-stu-id="74567-633">Created new Cmdlet for generating a User Token.</span></span> 
    - <span data-ttu-id="74567-634">**New-AzApiManagementUserToken** - 기본적으로 8시간 동안 유효한 새 사용자 토큰을 생성합니다. 'GIT' 사용자에 대한 토큰은 이 cmdlet을 사용하여 생성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="74567-634">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="74567-635">네트워크 상태를 검색하기 위한 새 cmdlet을 만들었습니다.</span><span class="sxs-lookup"><span data-stu-id="74567-635">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="74567-636">**Get-AzApiManagementNetworkStatus** - API Management 서비스에서 사용하는 리소스의 네트워크 상태 연결을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="74567-636">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="74567-637">ApiManagement 서비스를 가상 네트워크에 배포하고 종속성이 손상되었는지 여부를 확인할 때 유용합니다.</span><span class="sxs-lookup"><span data-stu-id="74567-637">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="74567-638">**New-AzApiManagement** cmdlet에서 ApiManagement 서비스를 관리하도록 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="74567-638">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span> 
    - <span data-ttu-id="74567-639">새 '소비' SKU 지원이 추가됨</span><span class="sxs-lookup"><span data-stu-id="74567-639">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="74567-640">'소비' SKU에 대해 'EnableClientCertificate' 플래그를 설정하기 위한 지원이 추가됨</span><span class="sxs-lookup"><span data-stu-id="74567-640">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="74567-641">새 **New-AzApiManagementSslSetting** cmdlet을 사용하면 'Backend(백 엔드)' 및 'Frontend'(프런트 엔드)에서 'TLS/SSL' 설정을 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="74567-641">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="74567-642">또한 ApiManagement 서비스의 'Frontend'에서 '3DES'와 같은 'Ciphers'와 'Http2'와 같은 'ServerProtocols'를 구성하는 데 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="74567-642">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="74567-643">ApiManagement 서비스에서 'DeveloperPortal' 호스트 이름을 구성하기 위한 지원이 추가됨</span><span class="sxs-lookup"><span data-stu-id="74567-643">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="74567-644">**Get-AzApiManagementSsoToken** cmdlet에서 'PsApiManagement' 개체를 입력으로 사용하도록 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="74567-644">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="74567-645">cmdlet에서 오류 메시지를 인라인으로 표시하도록 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="74567-645">Updated the cmdlet to display Error Messages inline</span></span> 
     > <span data-ttu-id="74567-646">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : 오류 코드: ValidationError 오류 메시지: 하나 이상의 필드에 잘못된 값이 있습니다. 오류 세부 정보:    [Code=ValidationError, Message=줄 3, 열 10의 'log-to-eventhub' 요소에 오류가 있습니다.: 로거를 찾지 못함, Target=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="74567-646">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="74567-647">**Export-AzApiManagementApi** cmdlet에서 API를 'OpenApi 3.0' 형식으로 내보내도록 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="74567-647">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="74567-648">**Import-AzApiManagementApi** cmdlet을 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="74567-648">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="74567-649">'OpenApi 3.0' 문서 사양에서 API 가져오기</span><span class="sxs-lookup"><span data-stu-id="74567-649">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="74567-650">문서('Swagger', 'Wadl', 'Wsdl', 'OpenApi')에 지정된 'PsApiManagementSchema' 속성 재정의</span><span class="sxs-lookup"><span data-stu-id="74567-650">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="74567-651">문서에 지정된 'ServiceUrl' 속성 재정의</span><span class="sxs-lookup"><span data-stu-id="74567-651">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="74567-652">**Get-AzApiManagementPolicy** cmdlet에서 'rawxml'을 사용하여 이스케이프된 비 Xml 'format'(형식)의 정책을 반환하도록 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="74567-652">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="74567-653">**Set-AzApiManagementPolicy** cmdlet에서 'rawxml'을 사용하여 이스케이프된 비 Xml 'format'의 정책을 수락하고, 'xml'을 사용하여 이스케이프된 Xml 'format'의 정책을 수락하도록 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="74567-653">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="74567-654">**New-AzApiManagementApi** cmdlet을 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="74567-654">Updated cmdlet **New-AzApiManagementApi**</span></span> 
    - <span data-ttu-id="74567-655">'OpenId' 권한 부여 서버를 사용하여 API 구성</span><span class="sxs-lookup"><span data-stu-id="74567-655">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="74567-656">'ApiVersionSet'에서 API 만들기</span><span class="sxs-lookup"><span data-stu-id="74567-656">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="74567-657">'SourceApiId' 및 'SourceApiRevision'을 사용하여 API 복제</span><span class="sxs-lookup"><span data-stu-id="74567-657">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="74567-658">API 범위에서 'SubscriptionRequired' 구성 가능</span><span class="sxs-lookup"><span data-stu-id="74567-658">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="74567-659">**Set-AzApiManagementApi** cmdlet을 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="74567-659">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="74567-660">'OpenId' 권한 부여 서버를 사용하여 API 구성</span><span class="sxs-lookup"><span data-stu-id="74567-660">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="74567-661">API를 'ApiVersionSet'으로 업데이트</span><span class="sxs-lookup"><span data-stu-id="74567-661">To updated an API into an 'ApiVersionSet'</span></span>    
    - <span data-ttu-id="74567-662">API 범위에서 'SubscriptionRequired' 구성 가능</span><span class="sxs-lookup"><span data-stu-id="74567-662">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="74567-663">**New-AzApiManagementRevision** cmdlet을 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="74567-663">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="74567-664">'SourceApiRevision'을 사용하여 기존 수정 버전 복제(태그, 제품, 작업 및 정책 복사).</span><span class="sxs-lookup"><span data-stu-id="74567-664">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="74567-665">새 수정 버전은 부모의 'ApiId'를 가정합니다.</span><span class="sxs-lookup"><span data-stu-id="74567-665">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="74567-666">'ApiRevisionDescription' 제공</span><span class="sxs-lookup"><span data-stu-id="74567-666">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="74567-667">API 복제 시 'ServiceUrl' 재정의</span><span class="sxs-lookup"><span data-stu-id="74567-667">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="74567-668">**New-AzApiManagementIdentityProvider** cmdlet을 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="74567-668">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="74567-669">'Authority'를 사용하여 'AAD' 또는 'AADB2C' 구성</span><span class="sxs-lookup"><span data-stu-id="74567-669">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="74567-670">'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' 및 'PasswordResetPolicy' 설정</span><span class="sxs-lookup"><span data-stu-id="74567-670">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="74567-671">**New-AzApiManagementSubscription** cmdlet을 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="74567-671">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="74567-672">'Scope' 및 'UserId'를 사용하여 새 SubscriptonModel 설명</span><span class="sxs-lookup"><span data-stu-id="74567-672">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="74567-673">'ProductId' 및 'UserId'를 사용하여 이전 구독 모델 설명</span><span class="sxs-lookup"><span data-stu-id="74567-673">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="74567-674">구독 수준에서 'AllowTracing'을 사용하도록 설정하는 지원 추가</span><span class="sxs-lookup"><span data-stu-id="74567-674">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="74567-675">**Set-AzApiManagementSubscription** cmdlet을 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="74567-675">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="74567-676">'Scope' 및 'UserId'를 사용하여 새 SubscriptonModel 설명</span><span class="sxs-lookup"><span data-stu-id="74567-676">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="74567-677">'ProductId' 및 'UserId'를 사용하여 이전 구독 모델 설명</span><span class="sxs-lookup"><span data-stu-id="74567-677">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="74567-678">구독 수준에서 'AllowTracing'을 사용하도록 설정하는 지원 추가</span><span class="sxs-lookup"><span data-stu-id="74567-678">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="74567-679">다음 cmdlet에서 'ResourceId'를 입력으로 수락하도록 업데이트했습니다</span><span class="sxs-lookup"><span data-stu-id="74567-679">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="74567-680">'New-AzApiManagementContext'</span><span class="sxs-lookup"><span data-stu-id="74567-680">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="74567-681">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="74567-681">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="74567-682">'Get-AzApiManagementApiRelease'</span><span class="sxs-lookup"><span data-stu-id="74567-682">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="74567-683">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="74567-683">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="74567-684">'Get-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="74567-684">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="74567-685">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="74567-685">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="74567-686">'Get-AzApiManagementAuthorizationServer'</span><span class="sxs-lookup"><span data-stu-id="74567-686">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="74567-687">'Get-AzApiManagementBackend'</span><span class="sxs-lookup"><span data-stu-id="74567-687">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="74567-688">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="74567-688">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="74567-689">'Get-AzApiManagementCertificate'</span><span class="sxs-lookup"><span data-stu-id="74567-689">'Get-AzApiManagementCertificate'</span></span> 
    - <span data-ttu-id="74567-690">'Remove-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="74567-690">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="74567-691">'Remove-AzApiManagementSubscription'</span><span class="sxs-lookup"><span data-stu-id="74567-691">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="74567-692">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="74567-692">Az.Automation</span></span>
* <span data-ttu-id="74567-693">Get-AzAutomationJobOutputRecord에서 JSON 및 Text 레코드 값을 처리하도록 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="74567-693">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="74567-694">문제 https://github.com/Azure/azure-powershell/issues/7977 수정</span><span class="sxs-lookup"><span data-stu-id="74567-694">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="74567-695">문제 https://github.com/Azure/azure-powershell/issues/8600 수정</span><span class="sxs-lookup"><span data-stu-id="74567-695">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="74567-696">Start-AzAutomationDscCompilationJob에서 완료될 때까지 기다리지 않고 작업을 바로 시작하도록 변경했습니다.</span><span class="sxs-lookup"><span data-stu-id="74567-696">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="74567-697">문제 https://github.com/Azure/azure-powershell/issues/8347 수정</span><span class="sxs-lookup"><span data-stu-id="74567-697">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="74567-698">-Name을 사용하면 모든 노드를 반환하는 Get-AzAutomationDscNode 수정.</span><span class="sxs-lookup"><span data-stu-id="74567-698">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="74567-699">이제 일치하는 노드만 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="74567-699">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="74567-700">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="74567-700">Az.Compute</span></span>
* <span data-ttu-id="74567-701">ProtectFromScaleIn 및 ProtectFromScaleSetAction 매개 변수를 Update-AzVmssVM cmdlet에 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="74567-701">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="74567-702">'East US'(미국 동부)가 지원되지 않는 경우 이제 New-AzVM wimple 매개 변수 집합에서 기본적으로 사용 가능한 위치를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="74567-702">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="74567-703">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="74567-703">Az.DataLakeStore</span></span>
* <span data-ttu-id="74567-704">ADLS SDK에서 httpclient를 사용하도록 업데이트하고, 데이터 평면 테스트를 Azure 프레임워크와 통합합니다.</span><span class="sxs-lookup"><span data-stu-id="74567-704">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="74567-705">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="74567-705">Az.Monitor</span></span>
* <span data-ttu-id="74567-706">도움말 예제에서 잘못된 매개 변수 이름을 수정했습니다.</span><span class="sxs-lookup"><span data-stu-id="74567-706">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="74567-707">Az.Network</span><span class="sxs-lookup"><span data-stu-id="74567-707">Az.Network</span></span>
* <span data-ttu-id="74567-708">DisableBgpRoutePropagation 플래그를 유효 경로 테이블 출력에 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="74567-708">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="74567-709">업데이트된 cmdlet:</span><span class="sxs-lookup"><span data-stu-id="74567-709">Updated cmdlet:</span></span>
        - <span data-ttu-id="74567-710">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="74567-710">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="74567-711">New-AzApplicationGatewayTrustedRootCertificate 설명서에서 이중 파선을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="74567-711">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="74567-712">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="74567-712">Az.Resources</span></span>
* <span data-ttu-id="74567-713">할당 거부를 검색하기 위한 새 Get-AzureRmDenyAssignment cmdlet을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="74567-713">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="74567-714">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="74567-714">Az.Sql</span></span>
* <span data-ttu-id="74567-715">Advanced Threat Protection cmdlet의 이름을 Advanced Data Security로 변경하고, 취약성 평가를 기본적으로 사용하도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="74567-715">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="74567-716">2.0.0 - 2019년 5월</span><span class="sxs-lookup"><span data-stu-id="74567-716">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="74567-717">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="74567-717">Az.Accounts</span></span>
* <span data-ttu-id="74567-718">사용자 이름/비밀번호 인증을 사용하여 ADFS 문제를 해결하도록 인증 라이브러리 업데이트</span><span class="sxs-lookup"><span data-stu-id="74567-718">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="74567-719">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="74567-719">Az.CognitiveServices</span></span>
* <span data-ttu-id="74567-720">Bing Search 서비스에 대해서만 Bing 면책 조항을 표시하세요.</span><span class="sxs-lookup"><span data-stu-id="74567-720">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="74567-721">계정 생성 실패 시 오류 개선.</span><span class="sxs-lookup"><span data-stu-id="74567-721">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="74567-722">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="74567-722">Az.Compute</span></span>
* <span data-ttu-id="74567-723">근접 배치 그룹 기능</span><span class="sxs-lookup"><span data-stu-id="74567-723">Proximity placement group feature.</span></span>
    - <span data-ttu-id="74567-724">다음과 같은 새 cmdlet을 추가했습니다.   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="74567-724">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="74567-725">새 매개 변수 ProximityPlacementGroupId가 다음 cmdlet에 추가됩니다.   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="74567-725">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="74567-726">New-AzGalleryImageVersion에 StorageAccountType 매개 변수가 추가됩니다.</span><span class="sxs-lookup"><span data-stu-id="74567-726">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="74567-727">New-AzGalleryImageVersion의 TargetRegion이 StorageAccountType를 포함할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="74567-727">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="74567-728">SkipShutdown 스위치 매개 변수가 Stop-AzVM 및 Stop-AzVmss에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="74567-728">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>       
* <span data-ttu-id="74567-729">주요 변경 내용</span><span class="sxs-lookup"><span data-stu-id="74567-729">Breaking changes</span></span>
    - <span data-ttu-id="74567-730">Set-AzVMBootDiagnostics이 Set-AzVMBootDiagnostic으로 변경됩니다.</span><span class="sxs-lookup"><span data-stu-id="74567-730">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="74567-731">Export-AzLogAnalyticThrottledRequests이 Export-AzLogAnalyticThrottledRequests로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="74567-731">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="74567-732">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="74567-732">Az.DeploymentManager</span></span>
* <span data-ttu-id="74567-733">Azure 배포 관리자 cmdlet의 일반적으로 사용 가능한 첫 번째 릴리스</span><span class="sxs-lookup"><span data-stu-id="74567-733">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="74567-734">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="74567-734">Az.Dns</span></span>
* <span data-ttu-id="74567-735">자동 DNS 이름 서버 위임</span><span class="sxs-lookup"><span data-stu-id="74567-735">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="74567-736">DNS 영역 만들기 cmdlet은 추가 선택적 매개 변수로 부모 영역 이름을 허용합니다.</span><span class="sxs-lookup"><span data-stu-id="74567-736">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="74567-737">새로 생성 된 자식 영역의 부모 영역에 NS 레코드를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="74567-737">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="74567-738">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="74567-738">Az.FrontDoor</span></span>
* <span data-ttu-id="74567-739">Azure FrontDoor cmdlet의 일반적으로 사용 가능한 첫 번째 릴리스</span><span class="sxs-lookup"><span data-stu-id="74567-739">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="74567-740">'Waf'를 포함하도록 WAF cmdlet의 이름 바꾸기</span><span class="sxs-lookup"><span data-stu-id="74567-740">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="74567-741">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="74567-741">Az.HDInsight</span></span>
* <span data-ttu-id="74567-742">두 개의 cmdlet을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="74567-742">Removed two cmdlets:</span></span>
    - <span data-ttu-id="74567-743">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="74567-743">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="74567-744">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="74567-744">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="74567-745">Grant-AzHDInsightHttpServicesAccess를 대체할 새 cmdlet Set-AzHDInsightGatewayCredential을 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="74567-745">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="74567-746">reader 역할과 HDInsight 운영자 역할을 구분하도록 cmdlet Get-AzHDInsightJobOutput 업데이트:</span><span class="sxs-lookup"><span data-stu-id="74567-746">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="74567-747">reader 역할을 가진 사용자는 'DefaultStorageAccountKey'매개 변수를 명시적으로 지정해야 합니다. 그렇지 않으면 오류가 발생합니다.</span><span class="sxs-lookup"><span data-stu-id="74567-747">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="74567-748">Hdinsight 운영자 역할을 가진 사용자를 영향을 받지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="74567-748">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="74567-749">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="74567-749">Az.Monitor</span></span>
* <span data-ttu-id="74567-750">SQR API(예약 쿼리 규칙)용 새 cmdlet</span><span class="sxs-lookup"><span data-stu-id="74567-750">New cmdlets for SQR API (Scheduled Query Rule)</span></span>  
    - <span data-ttu-id="74567-751">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="74567-751">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="74567-752">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="74567-752">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="74567-753">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="74567-753">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="74567-754">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="74567-754">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="74567-755">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="74567-755">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="74567-756">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="74567-756">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="74567-757">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="74567-757">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="74567-758">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="74567-758">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="74567-759">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="74567-759">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="74567-760">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="74567-760">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="74567-761">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="74567-761">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="74567-762">SQR API에 대한 [자세한 내용](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules)</span><span class="sxs-lookup"><span data-stu-id="74567-762">[More](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="74567-763">GenV2(비 클래식) 메트릭 기반 경고 규칙에 대한 cmdlet을 포함하도록 Az.Monitor.md가 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="74567-763">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="74567-764">Az.Network</span><span class="sxs-lookup"><span data-stu-id="74567-764">Az.Network</span></span>
* <span data-ttu-id="74567-765">Nat 게이트웨이 리소스에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="74567-765">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="74567-766">새 cmdlet</span><span class="sxs-lookup"><span data-stu-id="74567-766">New cmdlets</span></span>
        - <span data-ttu-id="74567-767">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="74567-767">New-AzNatGateway</span></span>
        - <span data-ttu-id="74567-768">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="74567-768">Get-AzNatGateway</span></span>
        - <span data-ttu-id="74567-769">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="74567-769">Set-AzNatGateway</span></span>
        - <span data-ttu-id="74567-770">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="74567-770">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="74567-771">다음 Cmdlet이 업데이트 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="74567-771">Updated cmdlets</span></span>
        - <span data-ttu-id="74567-772">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="74567-772">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="74567-773">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="74567-773">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="74567-774">기능에 대한 새로운 명령이 업데이트됨: Brooklyn Gateway에서 사용자 지정 경로 설정/제거.</span><span class="sxs-lookup"><span data-stu-id="74567-774">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="74567-775">New-AzVirtualNetworkGateway가 업데이트됨: 선택적 매개 변수 -CustomRoute를 추가하여 게이트웨이에서 설정할 사용자 지정 경로로 주소 접두사를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="74567-775">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="74567-776">Set-AzVirtualNetworkGateway가 업데이트됨: 선택적 매개 변수 -CustomRoute를 추가하여 게이트웨이에서 설정할 사용자 지정 경로로 주소 접두사를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="74567-776">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="74567-777">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="74567-777">Az.PolicyInsights</span></span>
* <span data-ttu-id="74567-778">정책 평가 세부 정보 쿼리 지원</span><span class="sxs-lookup"><span data-stu-id="74567-778">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="74567-779">Get-AzPolicyState에 '-Expand'매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="74567-779">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="74567-780">'-Expand PolicyEvaluationDetails' 지원</span><span class="sxs-lookup"><span data-stu-id="74567-780">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="74567-781">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="74567-781">Az.RecoveryServices</span></span>
* <span data-ttu-id="74567-782">크로스 구독 Azure에서 Azure 사이트 복구 지원</span><span class="sxs-lookup"><span data-stu-id="74567-782">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="74567-783">Azure Site Recovery에 대한 호환성이 손상되는 변경 표시</span><span class="sxs-lookup"><span data-stu-id="74567-783">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="74567-784">Azure Site Recovery 복구 계획 최종 실행 계획에 대한 수정</span><span class="sxs-lookup"><span data-stu-id="74567-784">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="74567-785">Azure에서 Azure에 대한 Azure Site Recovery 업데이트 네트워크 매핑 수정</span><span class="sxs-lookup"><span data-stu-id="74567-785">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="74567-786">관리 디스크에 대한 Azure에서 Azure에 대한 Azure Site Recovery 업데이트 보호 방향 수정</span><span class="sxs-lookup"><span data-stu-id="74567-786">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="74567-787">기타 사소한 수정.</span><span class="sxs-lookup"><span data-stu-id="74567-787">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="74567-788">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="74567-788">Az.Relay</span></span>
* <span data-ttu-id="74567-789">고객 관련 메시지의 철자 오류 수정</span><span class="sxs-lookup"><span data-stu-id="74567-789">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="74567-790">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="74567-790">Az.ServiceBus</span></span>
* <span data-ttu-id="74567-791">네임스페이스의 NetworkRuleSet에 대한 새 cmdlet가 추가되었습니다</span><span class="sxs-lookup"><span data-stu-id="74567-791">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="74567-792">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="74567-792">Az.Storage</span></span>
* <span data-ttu-id="74567-793">저장소 클라이언트 라이브러리 10.0.1로 업그레이드(이 SDK의 모든 개체의 네임스페이스가 'Microsoft.WindowsAzure.Storage. *'에서 'Microsoft.Azure.Storage.* '로 변경됨)</span><span class="sxs-lookup"><span data-stu-id="74567-793">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="74567-794">새로운 API 버전 2019-04-01을 지원하기 위해 Microsoft.Azure.Management.Storage 11.0.0으로 업그레이드합니다.</span><span class="sxs-lookup"><span data-stu-id="74567-794">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="74567-795">스토리지 생성 계정의 기본 스토리지 계정 종류가 'Storage'에서 'StorageV2'로 변경됩니다.</span><span class="sxs-lookup"><span data-stu-id="74567-795">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="74567-796">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="74567-796">New-AzStorageAccount</span></span>
* <span data-ttu-id="74567-797">'StandardLRS'가 'Standard_LRS'로 변경되는 것과 같이 '-'을 추가하여 입력 SkuName과 정렬되도록 스토리지 계정 cmdlet 출력 Sku.Name을 변경합니다.</span><span class="sxs-lookup"><span data-stu-id="74567-797">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="74567-798">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="74567-798">New-AzStorageAccount</span></span>
    - <span data-ttu-id="74567-799">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="74567-799">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="74567-800">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="74567-800">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="74567-801">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="74567-801">Az.Websites</span></span>
* <span data-ttu-id="74567-802">Get-AzWebApp에서 반환한 PSSite 개체에 대해 'Kind'속성이 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="74567-802">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="74567-803">Get-AzWebApp\* 메트릭 및 Get-AzAppServicePlanMetrics가 사용되지 않음으로 표시되었습니다.</span><span class="sxs-lookup"><span data-stu-id="74567-803">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="74567-804">1.8.0 - 2019년 4월</span><span class="sxs-lookup"><span data-stu-id="74567-804">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="74567-805">마지막 주 릴리스 이후의 주요 사항</span><span class="sxs-lookup"><span data-stu-id="74567-805">Highlights since the last major release</span></span>
* <span data-ttu-id="74567-806">`Az` 모듈 일반 공급</span><span class="sxs-lookup"><span data-stu-id="74567-806">General availability of `Az` module</span></span>
* <span data-ttu-id="74567-807">`Az` 모듈에 대한 자세한 내용은 https://aka.ms/azps-announce 를 방문하세요.</span><span class="sxs-lookup"><span data-stu-id="74567-807">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="74567-808">Location, ResourceGroup 및 ResourceName 완성자가 추가되었습니다(https://azure.microsoft.com/blog/completers-in-azure-powershell/ ).</span><span class="sxs-lookup"><span data-stu-id="74567-808">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="74567-809">와일드카드 지원이 Az.Compute 및 Az.Network에 대한 Get cmdlet에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="74567-809">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="74567-810">Windows PowerShell 5.1 전용 대화형 사용자 이름/암호 인증이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="74567-810">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="74567-811">Python 2 Runbook 지원이 Az.Automation에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="74567-811">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="74567-812">Az.LogicApp: 통합 계정 어셈블리 및 일괄 처리 구성을 위한 새로운 cmdlet입니다.</span><span class="sxs-lookup"><span data-stu-id="74567-812">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="74567-813">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="74567-813">Az.Accounts</span></span>
* <span data-ttu-id="74567-814">Mac에서 모듈을 올바르게 삭제하기 위해 Uninstall-AzureRm을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="74567-814">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="74567-815">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="74567-815">Az.Batch</span></span>
* <span data-ttu-id="74567-816">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="74567-816">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="74567-817">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="74567-817">Az.Cdn</span></span>
* <span data-ttu-id="74567-818">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="74567-818">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="74567-819">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="74567-819">Az.CognitiveServices</span></span>
* <span data-ttu-id="74567-820">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="74567-820">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="74567-821">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="74567-821">Az.Compute</span></span>
* <span data-ttu-id="74567-822">디스크의 리소스 ID에 리소스 ID의 소문자 resourcegroups가 있는 경우 AEM 설치 문제 수정</span><span class="sxs-lookup"><span data-stu-id="74567-822">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="74567-823">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="74567-823">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="74567-824">와일드 카드에 대한 설명서 수정</span><span class="sxs-lookup"><span data-stu-id="74567-824">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="74567-825">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="74567-825">Az.DataFactory</span></span>
* <span data-ttu-id="74567-826">NodeCount가 관리형 통합 런타임에 대해 Null이 아닌 경우 SsisProperties를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="74567-826">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="74567-827">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="74567-827">Az.DataLakeStore</span></span>
* <span data-ttu-id="74567-828">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="74567-828">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="74567-829">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="74567-829">Az.EventGrid</span></span>
* <span data-ttu-id="74567-830">이벤트 구독 cmdlet 만들기/업데이트를 사용하기 전에 리소스를 만들어야 함을 나타내기 위해 엔드포인트의 도움말 텍스트가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="74567-830">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="74567-831">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="74567-831">Az.EventHub</span></span>
* <span data-ttu-id="74567-832">네임스페이스의 NetworkRuleSet에 대한 새 cmdlet가 추가되었습니다</span><span class="sxs-lookup"><span data-stu-id="74567-832">Added new cmdlets for NetworkRuleSet of Namespace</span></span> 

#### <a name="azhdinsight"></a><span data-ttu-id="74567-833">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="74567-833">Az.HDInsight</span></span>
* <span data-ttu-id="74567-834">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="74567-834">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="74567-835">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="74567-835">Az.IotHub</span></span>
* <span data-ttu-id="74567-836">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="74567-836">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="74567-837">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="74567-837">Az.KeyVault</span></span>
* <span data-ttu-id="74567-838">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="74567-838">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="74567-839">와일드 카드에 대한 설명서 수정</span><span class="sxs-lookup"><span data-stu-id="74567-839">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="74567-840">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="74567-840">Az.MachineLearning</span></span>
* <span data-ttu-id="74567-841">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="74567-841">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="74567-842">Az.Media</span><span class="sxs-lookup"><span data-stu-id="74567-842">Az.Media</span></span>
* <span data-ttu-id="74567-843">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="74567-843">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="74567-844">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="74567-844">Az.Monitor</span></span>
  * <span data-ttu-id="74567-845">GenV2(비 클래식) 메트릭 기반 경고 규칙에 대한 새 cmdlet</span><span class="sxs-lookup"><span data-stu-id="74567-845">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="74567-846">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="74567-846">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="74567-847">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="74567-847">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="74567-848">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="74567-848">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="74567-849">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="74567-849">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="74567-850">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="74567-850">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="74567-851">모니터 SDK가 버전 0.22.0-preview로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="74567-851">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="74567-852">Az.Network</span><span class="sxs-lookup"><span data-stu-id="74567-852">Az.Network</span></span>
* <span data-ttu-id="74567-853">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="74567-853">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="74567-854">와일드 카드에 대한 설명서 수정</span><span class="sxs-lookup"><span data-stu-id="74567-854">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="74567-855">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="74567-855">Az.NotificationHubs</span></span>
* <span data-ttu-id="74567-856">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="74567-856">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="74567-857">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="74567-857">Az.OperationalInsights</span></span>
* <span data-ttu-id="74567-858">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="74567-858">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="74567-859">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="74567-859">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="74567-860">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="74567-860">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="74567-861">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="74567-861">Az.RecoveryServices</span></span>
* <span data-ttu-id="74567-862">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="74567-862">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="74567-863">Azure VM의 SQL용 테이블 형식이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="74567-863">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="74567-864">AzureFileShare에서 위치를 가져오는 대체 메서드가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="74567-864">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="74567-865">시간대에 따라 SchedulePolicy 개체의 ScheduleRunDays가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="74567-865">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="74567-866">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="74567-866">Az.RedisCache</span></span>
* <span data-ttu-id="74567-867">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="74567-867">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="74567-868">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="74567-868">Az.Resources</span></span>
* <span data-ttu-id="74567-869">와일드 카드에 대한 설명서 수정</span><span class="sxs-lookup"><span data-stu-id="74567-869">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="74567-870">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="74567-870">Az.Sql</span></span>
* <span data-ttu-id="74567-871">Monitor SDK의 종속성을 공용 코드로 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="74567-871">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="74567-872">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="74567-872">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="74567-873">다중 열 분류 프로세스가 향상되었습니다.</span><span class="sxs-lookup"><span data-stu-id="74567-873">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="74567-874">기본적으로 Get-AzSqlServerServiceObjective의 응답으로 SKU 속성(SKU 이름, 제품군, 용량)과 테이블 형식을 포함합니다.</span><span class="sxs-lookup"><span data-stu-id="74567-874">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="74567-875">해당 지역에 기존 서버 없이 위치별로 Get-AzSqlServerServiceObjective를 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="74567-875">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="74567-876">관리형 인스턴스 생성 시 표준 시간대 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="74567-876">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="74567-877">와일드 카드에 대한 설명서 수정</span><span class="sxs-lookup"><span data-stu-id="74567-877">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="74567-878">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="74567-878">Az.Websites</span></span>
* <span data-ttu-id="74567-879">실행 시 태그를 제거하지 않도록 Set-AzWebApp 및 Set-AzWebAppSlot를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="74567-879">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="74567-880">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="74567-880">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="74567-881">WebSites SDK가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="74567-881">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="74567-882">PSAppServicePlan에서 AdminSiteName 속성을 제거했습니다.</span><span class="sxs-lookup"><span data-stu-id="74567-882">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="74567-883">1.7.0 - 2019년 4월</span><span class="sxs-lookup"><span data-stu-id="74567-883">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="74567-884">마지막 주 릴리스 이후의 주요 사항</span><span class="sxs-lookup"><span data-stu-id="74567-884">Highlights since the last major release</span></span>
* <span data-ttu-id="74567-885">`Az` 모듈 일반 공급</span><span class="sxs-lookup"><span data-stu-id="74567-885">General availability of `Az` module</span></span>
* <span data-ttu-id="74567-886">`Az` 모듈에 대한 자세한 내용은 https://aka.ms/azps-announce 를 방문하세요.</span><span class="sxs-lookup"><span data-stu-id="74567-886">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="74567-887">Location, ResourceGroup 및 ResourceName 완성자가 추가되었습니다(https://azure.microsoft.com/blog/completers-in-azure-powershell/ ).</span><span class="sxs-lookup"><span data-stu-id="74567-887">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="74567-888">와일드카드 지원이 Az.Compute 및 Az.Network에 대한 Get cmdlet에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="74567-888">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="74567-889">Windows PowerShell 5.1 전용 대화형 사용자 이름/암호 인증이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="74567-889">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="74567-890">Python 2 Runbook 지원이 Az.Automation에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="74567-890">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="74567-891">Az.LogicApp: 통합 계정 어셈블리 및 일괄 처리 구성을 위한 새로운 cmdlet입니다.</span><span class="sxs-lookup"><span data-stu-id="74567-891">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="74567-892">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="74567-892">Az.Accounts</span></span>
* <span data-ttu-id="74567-893">매개 변수 AzureAnalysisServicesEndpointResourceId를 허용하도록 Add-AzEnvironment 및 Set-AzEnvironment 업데이트</span><span class="sxs-lookup"><span data-stu-id="74567-893">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="74567-894">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="74567-894">Az.AnalysisServices</span></span>
* <span data-ttu-id="74567-895">데이터 평면 cmdlet에서 ServiceClient 사용 및 원본 인증 논리 제거</span><span class="sxs-lookup"><span data-stu-id="74567-895">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="74567-896">호환성이 손상되는 변경을 방지하기 위해 Add-AzureASAccount를 Connect-AzAccount의 래퍼로 만듦</span><span class="sxs-lookup"><span data-stu-id="74567-896">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="74567-897">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="74567-897">Az.Automation</span></span>
* <span data-ttu-id="74567-898">포함에 대한 New-AzAutomationSoftwareUpdateConfiguration cmdlet 버그 수정</span><span class="sxs-lookup"><span data-stu-id="74567-898">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="74567-899">이제 매개 변수 IncludedKbNumber 및 IncludedPackageNameMask가 작동함</span><span class="sxs-lookup"><span data-stu-id="74567-899">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="74567-900">Azure 자동화 업데이트 관리 동적 그룹에 대한 버그 수정</span><span class="sxs-lookup"><span data-stu-id="74567-900">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="74567-901">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="74567-901">Az.Compute</span></span>
* <span data-ttu-id="74567-902">New-AzDiskConfig 및 New-AzSnapshotConfig에 HyperVGeneration 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="74567-902">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="74567-903">다른 테넌트의 갤러리 이미지를 사용하여 VM을 만들 수 있음</span><span class="sxs-lookup"><span data-stu-id="74567-903">Allow VM creation with galley image from other tenants.</span></span> 

#### <a name="azcontainerinstance"></a><span data-ttu-id="74567-904">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="74567-904">Az.ContainerInstance</span></span>
* <span data-ttu-id="74567-905">후행 빈 인수를 추가한 New-AzContainerGroup의 -Command 매개 변수의 문제 수정</span><span class="sxs-lookup"><span data-stu-id="74567-905">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="74567-906">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="74567-906">Az.DataFactory</span></span>
* <span data-ttu-id="74567-907">ADF .Net SDK 버전을 3.0.2로 업데이트</span><span class="sxs-lookup"><span data-stu-id="74567-907">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="74567-908">RepoConfiguration 관련 설정에 대한 추가 매개 변수로 Set-AzDataFactoryV2 cmdlet을 업데이트</span><span class="sxs-lookup"><span data-stu-id="74567-908">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="74567-909">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="74567-909">Az.Resources</span></span>
* <span data-ttu-id="74567-910">'-ResourceId' 또는 '-ResourceGroupName', '-Name' 및 '-ResourceType' 매개 변수를 제공할 때 'Get-AzResource'에 대한 공급자 처리 개선</span><span class="sxs-lookup"><span data-stu-id="74567-910">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="74567-911">'Test-AzDeployment' 및 'Test-AzResourceGroupDeployment'에 대한 오류 처리 개선</span><span class="sxs-lookup"><span data-stu-id="74567-911">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="74567-912">배포 유효성 검사 외부에서 발생한 오류를 처리하고 그 대신 명령의 출력에 포함</span><span class="sxs-lookup"><span data-stu-id="74567-912">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="74567-913">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/6856 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="74567-913">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="74567-914">배포 cmdlet 세트에 스크립트 및 작업 시나리오에서 프롬프트를 건너뛰는 '-IgnoreDynamicParameters' 스위치 추가</span><span class="sxs-lookup"><span data-stu-id="74567-914">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="74567-915">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/6856 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="74567-915">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="74567-916">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="74567-916">Az.Sql</span></span>
* <span data-ttu-id="74567-917">데이터베이스 데이터 분류 지원</span><span class="sxs-lookup"><span data-stu-id="74567-917">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="74567-918">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="74567-918">Az.Storage</span></span>
* <span data-ttu-id="74567-919">매개 변수 -UseConnectedAccount를 사용하여 스토리지 컨텍스트를 만들 때 자세한 오류 보고(단, 로그인 Azure 계정 없이)</span><span class="sxs-lookup"><span data-stu-id="74567-919">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="74567-920">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="74567-920">New-AzStorageContext</span></span>
* <span data-ttu-id="74567-921">관리 평면 API를 사용하여 지정한 스토리지 계정의 BLOB 서비스 속성 관리 지원</span><span class="sxs-lookup"><span data-stu-id="74567-921">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="74567-922">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="74567-922">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="74567-923">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="74567-923">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="74567-924">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="74567-924">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="74567-925">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="74567-925">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="74567-926">BLOB 및 파일 업로드/다운로드 cmdlet에 대한 -AsJob 지원</span><span class="sxs-lookup"><span data-stu-id="74567-926">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="74567-927">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="74567-927">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="74567-928">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="74567-928">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="74567-929">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="74567-929">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="74567-930">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="74567-930">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="74567-931">1.6.0 - 2019년 3월</span><span class="sxs-lookup"><span data-stu-id="74567-931">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="74567-932">마지막 주 릴리스 이후의 주요 사항</span><span class="sxs-lookup"><span data-stu-id="74567-932">Highlights since the last major release</span></span>
* <span data-ttu-id="74567-933">`Az` 모듈 일반 공급</span><span class="sxs-lookup"><span data-stu-id="74567-933">General availability of `Az` module</span></span>
* <span data-ttu-id="74567-934">`Az` 모듈에 대한 자세한 내용은 https://aka.ms/azps-announce 를 방문하세요.</span><span class="sxs-lookup"><span data-stu-id="74567-934">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="74567-935">Location, ResourceGroup 및 ResourceName 완성자가 추가되었습니다(https://azure.microsoft.com/blog/completers-in-azure-powershell/ ).</span><span class="sxs-lookup"><span data-stu-id="74567-935">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="74567-936">와일드카드 지원이 Az.Compute 및 Az.Network에 대한 Get cmdlet에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="74567-936">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="74567-937">Windows PowerShell 5.1 전용 대화형 사용자 이름/암호 인증이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="74567-937">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="74567-938">Python 2 Runbook 지원이 Az.Automation에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="74567-938">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="74567-939">Az.LogicApp: 통합 계정 어셈블리 및 일괄 처리 구성을 위한 새로운 cmdlet입니다.</span><span class="sxs-lookup"><span data-stu-id="74567-939">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="74567-940">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="74567-940">Az.Automation</span></span>
* <span data-ttu-id="74567-941">Azure 자동화 업데이트 관리에서 변경된 지원 기능은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="74567-941">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="74567-942">동적 그룹화</span><span class="sxs-lookup"><span data-stu-id="74567-942">Dynamic grouping</span></span>
    * <span data-ttu-id="74567-943">사전 스크립트</span><span class="sxs-lookup"><span data-stu-id="74567-943">Pre-Post script</span></span>
    * <span data-ttu-id="74567-944">다시 부팅 설정</span><span class="sxs-lookup"><span data-stu-id="74567-944">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="74567-945">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="74567-945">Az.Compute</span></span>
* <span data-ttu-id="74567-946">Get-AzVmBootDiagnosticsData의 경로 확인 문제가 해결되었습니다.</span><span class="sxs-lookup"><span data-stu-id="74567-946">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="74567-947">Compute 클라이언트 라이브러리가 25.0.0으로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="74567-947">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="74567-948">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="74567-948">Az.KeyVault</span></span>
* <span data-ttu-id="74567-949">와일드카드 지원이 KeyVault cmdlet에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="74567-949">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="74567-950">Az.Network</span><span class="sxs-lookup"><span data-stu-id="74567-950">Az.Network</span></span>
* <span data-ttu-id="74567-951">Azure Firewall에 대한 위협 인텔리전스 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="74567-951">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="74567-952">Application Gateway 방화벽 정책의 최상위 수준 리소스 및 사용자 지정 규칙이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="74567-952">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="74567-953">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="74567-953">Az.RecoveryServices</span></span>
* <span data-ttu-id="74567-954">인스턴트 RP를 지원하기 위해 SnapshotRetentionInDays가 Azure VM 정책에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="74567-954">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="74567-955">컨테이너 등록을 취소하는 파이프 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="74567-955">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="74567-956">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="74567-956">Az.Resources</span></span>
* <span data-ttu-id="74567-957">Get-AzResource 및 Get-AzResourceGroup에 대한 와일드카드 지원을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="74567-957">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="74567-958">ARM에 대한 일반 호출을 수행할 때 사용되는 자격 증명을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="74567-958">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="74567-959">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="74567-959">Az.Sql</span></span>
* <span data-ttu-id="74567-960">위협 탐지의 cmdlet 매개 변수(ExcludeDetectionType)가 DetectionType에서 string[]으로 변경되어 새 DetectionType이 추가되면 이후의 증명이 되고 자동 완성도 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="74567-960">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="74567-961">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="74567-961">Az.Storage</span></span>
* <span data-ttu-id="74567-962">스토리지 계정에 대한 관리 정책 가져오기/설정/제거를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="74567-962">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="74567-963">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="74567-963">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="74567-964">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="74567-964">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="74567-965">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="74567-965">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="74567-966">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="74567-966">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="74567-967">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="74567-967">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="74567-968">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="74567-968">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="74567-969">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="74567-969">Az.Websites</span></span>
* <span data-ttu-id="74567-970">'New-AzWebApp -IncludeSourceWebAppSlots'를 사용하여 모든 슬롯의 복제를 중단하는 ARM 템플릿 버그가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="74567-970">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span> 

## <a name="150---march-2019"></a><span data-ttu-id="74567-971">1.5.0 - 2019년 3월</span><span class="sxs-lookup"><span data-stu-id="74567-971">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="74567-972">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="74567-972">Az.Accounts</span></span>
* <span data-ttu-id="74567-973">'Register-AzModule' 명령을 추가하여 AutoRest 생성 cmdlet을 지원</span><span class="sxs-lookup"><span data-stu-id="74567-973">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="74567-974">Connect-AzAccount 예제 업데이트</span><span class="sxs-lookup"><span data-stu-id="74567-974">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="74567-975">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="74567-975">Az.Automation</span></span>
* <span data-ttu-id="74567-976">몇몇 Azure Automation cmdlet에서 특정 월별 일정을 검색할 때 발생하는 문제 수정</span><span class="sxs-lookup"><span data-stu-id="74567-976">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="74567-977">상위 20개 노드를 반환하도록 Get-AzAutomationDscNode를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="74567-977">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="74567-978">이제 모든 노드 반환</span><span class="sxs-lookup"><span data-stu-id="74567-978">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="74567-979">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="74567-979">Az.Cdn</span></span>
* <span data-ttu-id="74567-980">사용자 지정 도메인 Https 사용/사용 안 함에 대한 새 Powershell cmdlet이 추가되었으며 기존의 것은 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="74567-980">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="74567-981">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="74567-981">Az.Compute</span></span>
* <span data-ttu-id="74567-982">Get cmdlet에 와일드 카드 지원 추가</span><span class="sxs-lookup"><span data-stu-id="74567-982">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="74567-983">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="74567-983">Az.DataFactory</span></span>
* <span data-ttu-id="74567-984">ADF.Net SDK 버전이 3.0.1로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="74567-984">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="74567-985">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="74567-985">Az.LogicApp</span></span>
* <span data-ttu-id="74567-986">첫 결과 페이지 검색 시에만 ListWorkflows 수정</span><span class="sxs-lookup"><span data-stu-id="74567-986">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="74567-987">Az.Network</span><span class="sxs-lookup"><span data-stu-id="74567-987">Az.Network</span></span>
* <span data-ttu-id="74567-988">Network cmdlet에 와일드 카드 지원 추가</span><span class="sxs-lookup"><span data-stu-id="74567-988">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="74567-989">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="74567-989">Az.RecoveryServices</span></span>
* <span data-ttu-id="74567-990">Azure VM 지원에 SQL 서버가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="74567-990">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="74567-991">SDK 업데이트</span><span class="sxs-lookup"><span data-stu-id="74567-991">SDK Update</span></span>
* <span data-ttu-id="74567-992">VMappContainer 체크 인 Get-ProtectableItem 제거</span><span class="sxs-lookup"><span data-stu-id="74567-992">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="74567-993">Get ProtectableItem의 매개 변수로 Name과 ServerName이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="74567-993">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="74567-994">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="74567-994">Az.Resources</span></span>
* <span data-ttu-id="74567-995">`-TemplateObject` 매개 변수를 추가하여 cmdlet을 배포</span><span class="sxs-lookup"><span data-stu-id="74567-995">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="74567-996">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/2933 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="74567-996">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="74567-997">`Get-AzResource`의 결과를 `Set-AzResource`(으)로 파이프할 때 발생하는 문제 수정</span><span class="sxs-lookup"><span data-stu-id="74567-997">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="74567-998">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/8240 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="74567-998">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="74567-999">실행 시 JSON 데이터 형식 문제 해결 `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="74567-999">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="74567-1000">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/7930 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="74567-1000">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="74567-1001">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="74567-1001">Az.Sql</span></span>
* <span data-ttu-id="74567-1002">AuditingEndpointsCommunicator를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="74567-1002">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="74567-1003">새 진단 설정을 생성할 때 에지 사례의 동작을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="74567-1003">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="74567-1004">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="74567-1004">Az.Storage</span></span>
* <span data-ttu-id="74567-1005">스토리지 계정      - New-AzStorageAccount를 생성할 때 종류 BlockBlobStorage를 지원</span><span class="sxs-lookup"><span data-stu-id="74567-1005">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="74567-1006">1.4.0 - 2019년 2월</span><span class="sxs-lookup"><span data-stu-id="74567-1006">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="74567-1007">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="74567-1007">Az.AnalysisServices</span></span>
* <span data-ttu-id="74567-1008">사용되지 않는 AddAzureASAccount cmdlet</span><span class="sxs-lookup"><span data-stu-id="74567-1008">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="74567-1009">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="74567-1009">Az.Automation</span></span>
* <span data-ttu-id="74567-1010">Import-AzAutomationDscNodeConfiguration 도움말 업데이트</span><span class="sxs-lookup"><span data-stu-id="74567-1010">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="74567-1011">Import-AzAutomationDscConfiguration cmdlet 구성 이름 유효성 검사 추가</span><span class="sxs-lookup"><span data-stu-id="74567-1011">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="74567-1012">Import-AzAutomationDscConfiguration cmdlet 오류 처리 개선</span><span class="sxs-lookup"><span data-stu-id="74567-1012">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="74567-1013">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="74567-1013">Az.CognitiveServices</span></span>
* <span data-ttu-id="74567-1014">리소스의 하위 도메인을 지정하는 데 사용되는 New-AzCognitiveServicesAccount에 대한 새 선택적 매개 변수로 CustomSubdomainName이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="74567-1014">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="74567-1015">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="74567-1015">Az.Compute</span></span>
* <span data-ttu-id="74567-1016">ID 매개 변수 집합 문제 해결</span><span class="sxs-lookup"><span data-stu-id="74567-1016">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="74567-1017">Name 매개 변수를 제공하지 않으면 Get-AzVMExtension이 설치된 모든 확장을 열거하도록 업데이트</span><span class="sxs-lookup"><span data-stu-id="74567-1017">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="74567-1018">Update-AzImage cmdlet에 태그 및 ResourceId 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="74567-1018">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="74567-1019">인스턴스 ID가 없는 Get-AzVmssVM과 InstanceView를 사용하면 인스턴스 보기가 있는 VMSS VM을 나열할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="74567-1019">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="74567-1020">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="74567-1020">Az.DataLakeStore</span></span>
* <span data-ttu-id="74567-1021">ADL 삭제된 항목 열거 및 복원에 대한 cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="74567-1021">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="74567-1022">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="74567-1022">Az.EventHub</span></span>
* <span data-ttu-id="74567-1023">Eventhub의 CaptureDescription 클래스에서 빈 보관을 건너뛰는 새 부울 속성 SkipEmptyArchives가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="74567-1023">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span> 

#### <a name="azkeyvault"></a><span data-ttu-id="74567-1024">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="74567-1024">Az.KeyVault</span></span>
* <span data-ttu-id="74567-1025">Set-AzKeyVaultSecret 태그 지정 수정</span><span class="sxs-lookup"><span data-stu-id="74567-1025">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="74567-1026">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="74567-1026">Az.LogicApp</span></span>
* <span data-ttu-id="74567-1027">통합 계정에 대한 기본 sku 추가</span><span class="sxs-lookup"><span data-stu-id="74567-1027">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="74567-1028">XSLT 2.0, XSLT 3.0, Liquid 맵 형식 추가</span><span class="sxs-lookup"><span data-stu-id="74567-1028">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="74567-1029">통합 계정 어셈블리에 대한 새 cmdlet</span><span class="sxs-lookup"><span data-stu-id="74567-1029">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="74567-1030">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="74567-1030">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="74567-1031">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="74567-1031">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="74567-1032">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="74567-1032">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="74567-1033">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="74567-1033">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="74567-1034">통합 계정 일괄 처리 구성에 대한 새 cmdlet</span><span class="sxs-lookup"><span data-stu-id="74567-1034">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="74567-1035">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="74567-1035">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="74567-1036">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="74567-1036">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="74567-1037">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="74567-1037">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="74567-1038">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="74567-1038">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="74567-1039">논리 앱 SDK를 버전 4.1.0으로 업데이트</span><span class="sxs-lookup"><span data-stu-id="74567-1039">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="74567-1040">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="74567-1040">Az.Monitor</span></span>
* <span data-ttu-id="74567-1041">Get-AzMetric에 대한 도움말 업데이트</span><span class="sxs-lookup"><span data-stu-id="74567-1041">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="74567-1042">Az.Network</span><span class="sxs-lookup"><span data-stu-id="74567-1042">Az.Network</span></span>
* <span data-ttu-id="74567-1043">Add-AzApplicationGatewayCustomError에 대한 도움말 예제 업데이트</span><span class="sxs-lookup"><span data-stu-id="74567-1043">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="74567-1044">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="74567-1044">Az.OperationalInsights</span></span>
* <span data-ttu-id="74567-1045">New 및 Get ApplicationInsights 데이터 소스에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="74567-1045">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="74567-1046">지정된 작업 영역에 대한 특정 또는 전체 ApplicationInsights 데이터 원본 가져오기를 지원하기 위한 새로운 'ApplicationInsights' 종류가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="74567-1046">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span> 
    - <span data-ttu-id="74567-1047">지정된 Application-Insights 리소스 매개 변수(구독 ID, resourceGroupName 및 이름)별로 데이터 원본을 만들기 위한 New-AzOperationalInsightsApplicationInsightsDataSource cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="74567-1047">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span> 

#### <a name="azresources"></a><span data-ttu-id="74567-1048">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="74567-1048">Az.Resources</span></span>
* <span data-ttu-id="74567-1049">문제 https://github.com/Azure/azure-powershell/issues/8166 수정</span><span class="sxs-lookup"><span data-stu-id="74567-1049">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="74567-1050">문제 https://github.com/Azure/azure-powershell/issues/8235 수정</span><span class="sxs-lookup"><span data-stu-id="74567-1050">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="74567-1051">문제 https://github.com/Azure/azure-powershell/issues/6219 수정</span><span class="sxs-lookup"><span data-stu-id="74567-1051">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="74567-1052">KeyCredentials 반복 만들기를 방지하기 위해 버그 수정</span><span class="sxs-lookup"><span data-stu-id="74567-1052">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="74567-1053">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="74567-1053">Az.Sql</span></span>
* <span data-ttu-id="74567-1054">SQL DB 하이퍼스케일에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="74567-1054">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="74567-1055">복원 요청에서 불필요한 속성을 설정하여 복원이 실패할 수 있는 버그 수정</span><span class="sxs-lookup"><span data-stu-id="74567-1055">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="74567-1056">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="74567-1056">Az.Websites</span></span>
* <span data-ttu-id="74567-1057">Get-AzWebAppSlotMetrics 내 올바른 예제</span><span class="sxs-lookup"><span data-stu-id="74567-1057">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="74567-1058">1.3.0 - 2019년 2월</span><span class="sxs-lookup"><span data-stu-id="74567-1058">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="74567-1059">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="74567-1059">Az.Accounts</span></span>
* <span data-ttu-id="74567-1060">ClientRuntime 최신 버전 업데이트</span><span class="sxs-lookup"><span data-stu-id="74567-1060">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="74567-1061">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="74567-1061">Az.AnalysisServices</span></span>
<span data-ttu-id="74567-1062">Az.AnalysisServices 모듈의 전반적인 가용성.</span><span class="sxs-lookup"><span data-stu-id="74567-1062">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="74567-1063">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="74567-1063">Az.Compute</span></span>
* <span data-ttu-id="74567-1064">AEM 확장: UltraSSD 및 P60, P70, P80 디스크에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="74567-1064">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="74567-1065">Set-AzVMBootDiagnostics에 대한 도움말 업데이트</span><span class="sxs-lookup"><span data-stu-id="74567-1065">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="74567-1066">Update-AzImage에 대한 도움말 및 예제 업데이트</span><span class="sxs-lookup"><span data-stu-id="74567-1066">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="74567-1067">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="74567-1067">Az.RecoveryServices</span></span>
<span data-ttu-id="74567-1068">Az.RecoveryServices 모듈의 전반적인 가용성.</span><span class="sxs-lookup"><span data-stu-id="74567-1068">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="74567-1069">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="74567-1069">Az.Resources</span></span>
* <span data-ttu-id="74567-1070">리소스 그룹 관련 태그 수정</span><span class="sxs-lookup"><span data-stu-id="74567-1070">Fix tagging for resource groups</span></span> 
    - <span data-ttu-id="74567-1071">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/8166 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="74567-1071">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="74567-1072">`Get-AzureRmRoleAssignment`이(가) -ErrorAction을 준수하지 않는 문제 수정</span><span class="sxs-lookup"><span data-stu-id="74567-1072">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span> 
    - <span data-ttu-id="74567-1073">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/8235 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="74567-1073">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="74567-1074">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="74567-1074">Az.Sql</span></span>
* <span data-ttu-id="74567-1075">AzSqlDatabaseBackupShortTermRetentionPolicy 가져오기/설정하기 추가</span><span class="sxs-lookup"><span data-stu-id="74567-1075">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="74567-1076">SQL cmdlet을 실행할 경우 Azure 계정에 로그인되어 있지 않은 것이 nullref 예외를 초래하는 문제 수정</span><span class="sxs-lookup"><span data-stu-id="74567-1076">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="74567-1077">Get-AzSqlCapability의 nullref 예외 수정</span><span class="sxs-lookup"><span data-stu-id="74567-1077">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="74567-1078">1.2.1 - 2019년 1월</span><span class="sxs-lookup"><span data-stu-id="74567-1078">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="74567-1079">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="74567-1079">Az.Accounts</span></span>
* <span data-ttu-id="74567-1080">올바른 인증 버전을 사용하여 릴리스</span><span class="sxs-lookup"><span data-stu-id="74567-1080">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="74567-1081">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="74567-1081">Az.AnalysisServices</span></span>
* <span data-ttu-id="74567-1082">업데이트된 인증 종속성을 사용하여 릴리스</span><span class="sxs-lookup"><span data-stu-id="74567-1082">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="74567-1083">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="74567-1083">Az.RecoveryServices</span></span>
* <span data-ttu-id="74567-1084">업데이트된 인증 종속성을 사용하여 릴리스</span><span class="sxs-lookup"><span data-stu-id="74567-1084">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="74567-1085">1.2.0 - 2019년 1월</span><span class="sxs-lookup"><span data-stu-id="74567-1085">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="74567-1086">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="74567-1086">Az.Accounts</span></span>
* <span data-ttu-id="74567-1087">Windows PowerShell 5.1 전용 대화형 사용자 이름/암호 인증 추가</span><span class="sxs-lookup"><span data-stu-id="74567-1087">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="74567-1088">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="74567-1088">Update incorrect online help URLs</span></span>
* <span data-ttu-id="74567-1089">Uninstall-AzureRm 관련 PS Core에 경고 메시지 추가</span><span class="sxs-lookup"><span data-stu-id="74567-1089">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="74567-1090">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="74567-1090">Az.Aks</span></span>
* <span data-ttu-id="74567-1091">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="74567-1091">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="74567-1092">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="74567-1092">Az.Automation</span></span>
* <span data-ttu-id="74567-1093">Python 2 Runbook에 대한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="74567-1093">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="74567-1094">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="74567-1094">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="74567-1095">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="74567-1095">Az.Cdn</span></span>
* <span data-ttu-id="74567-1096">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="74567-1096">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="74567-1097">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="74567-1097">Az.Compute</span></span>
* <span data-ttu-id="74567-1098">Invoke-AzVMReimage cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="74567-1098">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="74567-1099">Set-AzVmss에 TempDisk 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="74567-1099">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="74567-1100">New-AzVM 경고 메시지 수정</span><span class="sxs-lookup"><span data-stu-id="74567-1100">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="74567-1101">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="74567-1101">Az.ContainerRegistry</span></span>
* <span data-ttu-id="74567-1102">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="74567-1102">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="74567-1103">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="74567-1103">Az.DataFactory</span></span>
* <span data-ttu-id="74567-1104">ADF.Net SDK 버전이 3.0.0으로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="74567-1104">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="74567-1105">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="74567-1105">Az.DataLakeStore</span></span>
* <span data-ttu-id="74567-1106">MSI를 사용할 때 ADLS 엔드포인트 문제 수정</span><span class="sxs-lookup"><span data-stu-id="74567-1106">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="74567-1107">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/7462 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="74567-1107">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="74567-1108">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="74567-1108">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="74567-1109">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="74567-1109">Az.IotHub</span></span>
* <span data-ttu-id="74567-1110">Add-IotHubRoutingEndpoint cmdlet에 인코딩 형식을 추가하세요.</span><span class="sxs-lookup"><span data-stu-id="74567-1110">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="74567-1111">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="74567-1111">Az.KeyVault</span></span>
* <span data-ttu-id="74567-1112">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="74567-1112">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="74567-1113">Az.Network</span><span class="sxs-lookup"><span data-stu-id="74567-1113">Az.Network</span></span>
* <span data-ttu-id="74567-1114">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="74567-1114">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="74567-1115">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="74567-1115">Az.Resources</span></span>
* <span data-ttu-id="74567-1116">'New-AzADAppCredential' 및 'New-AzADSpCredential' 참조 설명서의 잘못된 예제 수정</span><span class="sxs-lookup"><span data-stu-id="74567-1116">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="74567-1117">리소스 그룹 배포 cmdlet 실행 전 '-TemplateFile' 매개 변수 경로가 확인되지 않는 문제 수정</span><span class="sxs-lookup"><span data-stu-id="74567-1117">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="74567-1118">Az.Resources: New-AzureRmPolicyDefinition -Mode 기본값에 대한 올바른 설명서</span><span class="sxs-lookup"><span data-stu-id="74567-1118">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="74567-1119">Az.Resources: 문제 https://github.com/Azure/azure-powershell/issues/7522 수정</span><span class="sxs-lookup"><span data-stu-id="74567-1119">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="74567-1120">Az.Resources: 문제 https://github.com/Azure/azure-powershell/issues/5747 수정</span><span class="sxs-lookup"><span data-stu-id="74567-1120">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="74567-1121">'PSResourceGroupDeployment' 개체의 서식 문제 수정</span><span class="sxs-lookup"><span data-stu-id="74567-1121">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="74567-1122">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/2123 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="74567-1122">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="74567-1123">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="74567-1123">Az.ServiceFabric</span></span>
* <span data-ttu-id="74567-1124">인증서가 VMSS 모델에 추가되었는데도 예외가 발생할 경우 롤백합니다. 이는 버그 https://github.com/Azure/service-fabric-issues/issues/932 를 수정하기 위함입니다.</span><span class="sxs-lookup"><span data-stu-id="74567-1124">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="74567-1125">일부 오류 메시지를 수정하세요.</span><span class="sxs-lookup"><span data-stu-id="74567-1125">Fix some error messages.</span></span>
* <span data-ttu-id="74567-1126">Az로의 마이그레이션을 통해서는 작동하지 않는 New-AzServiceFabriCluster를 위해 기본값 ARM 템플릿을 가진 클러스터 만들기를 수정하세요.</span><span class="sxs-lookup"><span data-stu-id="74567-1126">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="74567-1127">확장에서 클러스터 id를 확인하여 클러스터에 해당하는 VMSS에만 추가되도록 클러스터/애플리케이션 인증서 추가를 수정하세요.</span><span class="sxs-lookup"><span data-stu-id="74567-1127">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="74567-1128">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="74567-1128">Az.SignalR</span></span>
* <span data-ttu-id="74567-1129">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="74567-1129">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="74567-1130">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="74567-1130">Az.Sql</span></span>
* <span data-ttu-id="74567-1131">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="74567-1131">Update incorrect online help URLs</span></span>
* <span data-ttu-id="74567-1132">가능한 값을 가진 LicenseType 매개 변수에 대한 매개 변수 설명이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="74567-1132">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="74567-1133">유일하게 업데이트된 속성인데 작동하지 않는 관리되는 인스턴스 ID의 업데이트 수정</span><span class="sxs-lookup"><span data-stu-id="74567-1133">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="74567-1134">관리되는 인스턴스에서의 사용자 지정 데이터 정렬에 대한 지원</span><span class="sxs-lookup"><span data-stu-id="74567-1134">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="74567-1135">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="74567-1135">Az.Storage</span></span>
* <span data-ttu-id="74567-1136">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="74567-1136">Update incorrect online help URLs</span></span>
* <span data-ttu-id="74567-1137">Premium Storage 계정이 클래식 로깅/메트릭을 지원하지 않기 때문에, Premium Storage 계정의 클래식 로깅/메트릭을 가져올/설정할 때 상세한 오류 메시지를 제공해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="74567-1137">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="74567-1138">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="74567-1138">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="74567-1139">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="74567-1139">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="74567-1140">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="74567-1140">Az.TrafficManager</span></span>
* <span data-ttu-id="74567-1141">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="74567-1141">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="74567-1142">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="74567-1142">Az.Websites</span></span>
* <span data-ttu-id="74567-1143">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="74567-1143">Update incorrect online help URLs</span></span>
* <span data-ttu-id="74567-1144">앱이 ASE에 호스팅되면 'New-AzWebAppSSLBinding'을 수정하여 올바른 resourcegroup+location에 인증서를 업로드합니다.</span><span class="sxs-lookup"><span data-stu-id="74567-1144">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="74567-1145">'New-AzWebAppSSLBinding'을 수정하여 SSL 인증서를 앱에 바인딩하는 데 붙는 태그를 덮어쓰지 않도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="74567-1145">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="74567-1146">1.1.0 - 2019년 1월</span><span class="sxs-lookup"><span data-stu-id="74567-1146">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="74567-1147">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="74567-1147">Az.Accounts</span></span>
* <span data-ttu-id="74567-1148">Enable-AzureRmAlias에 'Local' 범위 추가</span><span class="sxs-lookup"><span data-stu-id="74567-1148">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="74567-1149">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="74567-1149">Az.Compute</span></span>
* <span data-ttu-id="74567-1150">이름이 Restart/Start/Stop/Remove/Set-AzVM과 Save-AzVMImage에 설정된 ID 매개 변수에서 선택 사항이 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="74567-1150">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="74567-1151">도움말 파일의 ID에 대한 설명이 업데이트 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="74567-1151">Updated the description of ID in help files</span></span>
* <span data-ttu-id="74567-1152">Az.Accounts 모듈을 사용할 때의 이전 버전과의 호환성 문제를 해결합니다.</span><span class="sxs-lookup"><span data-stu-id="74567-1152">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="74567-1153">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="74567-1153">Az.DataLakeStore</span></span>
* <span data-ttu-id="74567-1154">SDK 수정을 위해 데이터 평면의 SDK 버전을 1.1.14로 업데이트하세요.</span><span class="sxs-lookup"><span data-stu-id="74567-1154">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="74567-1155">getfilestatus 및 liststatus에 대한 음수 acesstime 및 modificationtime 수정, 비동기 취소 토큰 수정</span><span class="sxs-lookup"><span data-stu-id="74567-1155">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="74567-1156">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="74567-1156">Az.EventGrid</span></span>
* <span data-ttu-id="74567-1157">2019-01-01 API 버전을 사용하도록 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="74567-1157">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="74567-1158">2019-01-01 API 버전에서 새 시나리오를 지원하도록 다음 cmdlet을 업데이트</span><span class="sxs-lookup"><span data-stu-id="74567-1158">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="74567-1159">New-AzureRmEventGridSubscription: 지정을 위한 새로운 선택적 매개 변수를 추가</span><span class="sxs-lookup"><span data-stu-id="74567-1159">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="74567-1160">이벤트 Time-to-Live</span><span class="sxs-lookup"><span data-stu-id="74567-1160">Event Time-To-Live,</span></span>
        - <span data-ttu-id="74567-1161">이벤트에 대한 최대 배달 시도</span><span class="sxs-lookup"><span data-stu-id="74567-1161">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="74567-1162">배달 못한 편지의 엔드포인트입니다.</span><span class="sxs-lookup"><span data-stu-id="74567-1162">Dead letter endpoint.</span></span>
    - <span data-ttu-id="74567-1163">Update-AzureRmEventGridSubscription: 지정을 위한 새로운 선택적 매개 변수를 추가</span><span class="sxs-lookup"><span data-stu-id="74567-1163">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="74567-1164">이벤트 Time-to-Live</span><span class="sxs-lookup"><span data-stu-id="74567-1164">Event Time-To-Live,</span></span>
        - <span data-ttu-id="74567-1165">이벤트에 대한 최대 배달 시도</span><span class="sxs-lookup"><span data-stu-id="74567-1165">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="74567-1166">배달 못한 편지의 엔드포인트입니다.</span><span class="sxs-lookup"><span data-stu-id="74567-1166">Dead letter endpoint.</span></span>
* <span data-ttu-id="74567-1167">New-AzureRmEventGridSubscription 및 Update-AzureRmEventGridSubscription cmdlet의 EndpointType 옵션에 새 열거형 값(즉, storageQueue 및 hybridConnection)을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="74567-1167">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="74567-1168">이벤트 구독을 생성 또는 업데이트할 때 사용자가 직접 조치를 취해야 할 경우 경고 메시지를 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="74567-1168">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="74567-1169">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="74567-1169">Az.IotHub</span></span>
* <span data-ttu-id="74567-1170">최신 버전의 Azure IotHub SDK로 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="74567-1170">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="74567-1171">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="74567-1171">Az.LogicApp</span></span>
* <span data-ttu-id="74567-1172">지정된 이름이 없는 모든 Get-AzLogicApp 목록</span><span class="sxs-lookup"><span data-stu-id="74567-1172">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="74567-1173">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="74567-1173">Az.Resources</span></span>
* <span data-ttu-id="74567-1174">'Get-AzResource'에 '-ODataQuery'및 '-ResourceId' 매개 변수를 제공할 때 매개 변수 집합 문제 수정</span><span class="sxs-lookup"><span data-stu-id="74567-1174">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="74567-1175">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/7875 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="74567-1175">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="74567-1176">New/Set-AzPolicyDefinition에서 -Custom 매개 변수 처리 문제 수정</span><span class="sxs-lookup"><span data-stu-id="74567-1176">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="74567-1177">New-AzDeployment 설명서에서 오타 수정</span><span class="sxs-lookup"><span data-stu-id="74567-1177">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="74567-1178">'New-AzADUser'에 '-MailNickname'매개 변수가 필수 항목으로 지정됨</span><span class="sxs-lookup"><span data-stu-id="74567-1178">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="74567-1179">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/8220 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="74567-1179">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="74567-1180">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="74567-1180">Az.SignalR</span></span>
* <span data-ttu-id="74567-1181">Az.Accounts 모듈을 사용할 때의 이전 버전과의 호환성 문제를 해결합니다.</span><span class="sxs-lookup"><span data-stu-id="74567-1181">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="74567-1182">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="74567-1182">Az.Sql</span></span>
* <span data-ttu-id="74567-1183">Storage 관리 클라이언트 종속성을 일반적인 SDK 구현으로 변환했습니다.</span><span class="sxs-lookup"><span data-stu-id="74567-1183">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="74567-1184">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="74567-1184">Az.Storage</span></span>
* <span data-ttu-id="74567-1185">Sas Token, OAuth 또는 Anonymous를 사용하여 스토리지 컨텍스트의 StorageAccountName을 실제 스토리지 계정 이름으로 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="74567-1185">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="74567-1186">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="74567-1186">New-AzStorageContext</span></span>
* <span data-ttu-id="74567-1187">'-FullUri' 매개 변수를 사용하여 Blob 스냅샷 개체의 Sas Token을 생성하고 반환된 Uri를 스냅샷 Uri로 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="74567-1187">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="74567-1188">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="74567-1188">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="74567-1189">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="74567-1189">Az.Websites</span></span>
* <span data-ttu-id="74567-1190">'Get-AzDeletedWebApp'의 날짜 구문 분석 버그를 수정했습니다.</span><span class="sxs-lookup"><span data-stu-id="74567-1190">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="74567-1191">Az.Accounts 모듈을 사용할 때의 이전 버전과의 호환성 문제를 해결합니다.</span><span class="sxs-lookup"><span data-stu-id="74567-1191">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="74567-1192">1.0.0 - 2018년 12월</span><span class="sxs-lookup"><span data-stu-id="74567-1192">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="74567-1193">일반</span><span class="sxs-lookup"><span data-stu-id="74567-1193">General</span></span>

- <span data-ttu-id="74567-1194">Az 모듈 일반 공급</span><span class="sxs-lookup"><span data-stu-id="74567-1194">General Availability of Az Module</span></span>
- <span data-ttu-id="74567-1195">각 모듈에 대 한 온라인 도움말</span><span class="sxs-lookup"><span data-stu-id="74567-1195">Online help for each module</span></span>
- <span data-ttu-id="74567-1196">자세한 내용과 로드맵은 [Az 알림 페이지](https://aka.ms/azps-announce)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="74567-1196">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="74567-1197">AzureRM에서 마이그레이션하는 것에 대한 정보는 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="74567-1197">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="74567-1198">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="74567-1198">Az.Accounts</span></span>
- <span data-ttu-id="74567-1199">Az.Profile에서 변경</span><span class="sxs-lookup"><span data-stu-id="74567-1199">Changed from Az.Profile</span></span>
- <span data-ttu-id="74567-1200">프로필 및 컨텍스트 형식에 대한 표 형식 수정</span><span class="sxs-lookup"><span data-stu-id="74567-1200">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="74567-1201">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="74567-1201">Az.ApiManagement</span></span>
- <span data-ttu-id="74567-1202">#7002에 대한 수정</span><span class="sxs-lookup"><span data-stu-id="74567-1202">Fixes for #7002</span></span>
- <span data-ttu-id="74567-1203">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="74567-1203">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="74567-1204">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="74567-1204">Az.Batch</span></span>
- <span data-ttu-id="74567-1205">`PSComputeNode`의 새로운 `NodeAgentInformation` 속성을 통해 풀의 각 VM에서 실행 중인 Azure Batch 노드 에이전트의 버전을 확인하는 기능이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="74567-1205">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="74567-1206">`PSDataDisk`에 대한 `Caching` 기본 값은 이제 `None` 대신 `ReadWrite`입니다.</span><span class="sxs-lookup"><span data-stu-id="74567-1206">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="74567-1207">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="74567-1207">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="74567-1208">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="74567-1208">Az.Billing</span></span>
- <span data-ttu-id="74567-1209">청구, 소비 및 UsageAggregates cmdlet 결합 cmdlet에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="74567-1209">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="74567-1210">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="74567-1210">Az.CognitivServices</span></span>
- <span data-ttu-id="74567-1211">New-AzureRmCognitiveServicesAccount 작업에서 사용 가능한 SkuName 및 Typem에 대한 완성자 추가</span><span class="sxs-lookup"><span data-stu-id="74567-1211">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="74567-1212">Get-AzCognitiveServicesAccountSkus에서 GetSkusWithAccountParamSetName 매개 변수 집합을 제거</span><span class="sxs-lookup"><span data-stu-id="74567-1212">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="74567-1213">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="74567-1213">Az.ContainerInstance</span></span>
- <span data-ttu-id="74567-1214">ManagedIdentity 지원이 추가됨</span><span class="sxs-lookup"><span data-stu-id="74567-1214">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="74567-1215">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="74567-1215">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="74567-1216">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="74567-1216">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="74567-1217">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="74567-1217">Az.DataLakeStore</span></span>
- <span data-ttu-id="74567-1218">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="74567-1218">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="74567-1219">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="74567-1219">Az.Monitor</span></span>
- <span data-ttu-id="74567-1220">Az.Monitor 이름 변경 및 기타 사소한 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="74567-1220">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="74567-1221">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="74567-1221">Az.KeyVault</span></span>
- <span data-ttu-id="74567-1222">출력 형식에서 사용되지 않는 'PurgeDisabled' 속성 제거</span><span class="sxs-lookup"><span data-stu-id="74567-1222">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="74567-1223">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="74567-1223">Az.MachineLearning</span></span>
- <span data-ttu-id="74567-1224">Az.MachineLearningCompute 모듈의 cmdlet 포함</span><span class="sxs-lookup"><span data-stu-id="74567-1224">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="74567-1225">Az.Media</span><span class="sxs-lookup"><span data-stu-id="74567-1225">Az.Media</span></span>
- <span data-ttu-id="74567-1226">New-AzMediaService에서 사용되지 않는 -Tags 별칭이 제거됨</span><span class="sxs-lookup"><span data-stu-id="74567-1226">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="74567-1227">Az.Network</span><span class="sxs-lookup"><span data-stu-id="74567-1227">Az.Network</span></span>
<span data-ttu-id="74567-1228">Application Gateway에서 RewriteRuleSets를 구성하는 것에 대한 지원이 추가됨</span><span class="sxs-lookup"><span data-stu-id="74567-1228">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="74567-1229">추가된 새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="74567-1229">New cmdlets added:</span></span>
        - <span data-ttu-id="74567-1230">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="74567-1230">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="74567-1231">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="74567-1231">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="74567-1232">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="74567-1232">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="74567-1233">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="74567-1233">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="74567-1234">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="74567-1234">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="74567-1235">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="74567-1235">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="74567-1236">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="74567-1236">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="74567-1237">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="74567-1237">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="74567-1238">선택적 매개 변수를 사용하도록 cmdlet이 업데이트됨 -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="74567-1238">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="74567-1239">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="74567-1239">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="74567-1240">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="74567-1240">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="74567-1241">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="74567-1241">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="74567-1242">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="74567-1242">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="74567-1243">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="74567-1243">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="74567-1244">New-AzureRmApplicationGatewayUrlPathMapConfig로 ID를 사용하여 Application Gateway에 KeyVault 지원을 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="74567-1244">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="74567-1245">선택적 매개 변수를 사용하도록 cmdlet이 업데이트됨 -KeyVaultSecretId, -KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="74567-1245">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="74567-1246">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="74567-1246">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="74567-1247">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="74567-1247">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="74567-1248">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="74567-1248">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="74567-1249">New-AzApplicationGateway cmdlet이 선택적 매개 변수를 사용하도록 업데이트됨 -UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="74567-1249">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="74567-1250">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="74567-1250">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="74567-1251">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="74567-1251">Az.OperationalInsights</span></span>
- <span data-ttu-id="74567-1252">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="74567-1252">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="74567-1253">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="74567-1253">Az.Profile</span></span>
- <span data-ttu-id="74567-1254">Az.Accounts에 모듈 이름이 변경됨</span><span class="sxs-lookup"><span data-stu-id="74567-1254">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="74567-1255">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="74567-1255">Az.RecoveryServices</span></span>
- <span data-ttu-id="74567-1256">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="74567-1256">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="74567-1257">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="74567-1257">Az.Resources</span></span>
- <span data-ttu-id="74567-1258">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="74567-1258">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="74567-1259">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="74567-1259">Az.ServiceFabric</span></span>
- <span data-ttu-id="74567-1260">일반 이름과 지문으로 지정 인증서 지원</span><span class="sxs-lookup"><span data-stu-id="74567-1260">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="74567-1261">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="74567-1261">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="74567-1262">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="74567-1262">Az.SIgnalR</span></span>
- <span data-ttu-id="74567-1263">SIgnalR에 대한 PowerShell cmdlet에 대한 일반 공급</span><span class="sxs-lookup"><span data-stu-id="74567-1263">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="74567-1264">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="74567-1264">Az.Sql</span></span>
- <span data-ttu-id="74567-1265">위협 탐지의 cmdlet에 새로운 Data_Exfiltration 및 Unsafe_Action 검색 유형 추가</span><span class="sxs-lookup"><span data-stu-id="74567-1265">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="74567-1266">Sql 감사 cmdlet에 대한 설명서 예제 업데이트</span><span class="sxs-lookup"><span data-stu-id="74567-1266">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="74567-1267">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="74567-1267">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="74567-1268">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="74567-1268">Az.Storage</span></span>
- <span data-ttu-id="74567-1269">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="74567-1269">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="74567-1270">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="74567-1270">Az.Websites</span></span>
- <span data-ttu-id="74567-1271">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="74567-1271">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="74567-1272">0.7.0 - 2018년 12월</span><span class="sxs-lookup"><span data-stu-id="74567-1272">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="74567-1273">일반</span><span class="sxs-lookup"><span data-stu-id="74567-1273">General</span></span>

* <span data-ttu-id="74567-1274">AzureRM에서 Az 전환 예정에 대한 사소한 변경</span><span class="sxs-lookup"><span data-stu-id="74567-1274">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="74567-1275">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="74567-1275">Az.Compute</span></span>

* <span data-ttu-id="74567-1276">`New-AzVm(ss)` cmdlet에 대한 간단한 매개 변수 집합에 UltraSSD 및 갤러리 이미지에 대한 지원을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="74567-1276">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="74567-1277">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="74567-1277">Az.DataLakeStore</span></span>

* <span data-ttu-id="74567-1278">ADLS 계정의 도메인의 후행 슬래시를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="74567-1278">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="74567-1279">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="74567-1279">Az.FrontDoor</span></span>

* <span data-ttu-id="74567-1280">일부 끊어진 링크 수정</span><span class="sxs-lookup"><span data-stu-id="74567-1280">Fixed some broken links</span></span>
    - <span data-ttu-id="74567-1281">New-AzureRmFrontDoor 및 Set-AzureRmFrontDoor 아티클에서 New-AzureRmFrontDoorHealthProbeSettingObject cmdlet 아티클에 대한 링크가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="74567-1281">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="74567-1282">New-AzureRmFrontDoorManagedRuleObject 아티클에서 New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet 아티클에 대한 링크가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="74567-1282">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="74567-1283">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="74567-1283">Az.RecoveryServices</span></span>

* <span data-ttu-id="74567-1284">Azure File Share 복원 작업에 클라이언트 측 유효성 검사가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="74567-1284">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="74567-1285">afs 복원의 경우 storageAccountName 및 storageAccountResourceGroupName을 선택적으로 만들었습니다.</span><span class="sxs-lookup"><span data-stu-id="74567-1285">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="74567-1286">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="74567-1286">Az.Resources</span></span>

* <span data-ttu-id="74567-1287">에 대 한 수정 https://github.com/Azure/azure-powershell/issues/7679</span><span class="sxs-lookup"><span data-stu-id="74567-1287">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="74567-1288">기본 관리자를 요청할 때 구독 범위가 제공되는 경우 Get-AzureRmRoleAssignment를 업데이트하여 구독 범위를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="74567-1288">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="74567-1289">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="74567-1289">Az.Sql</span></span>

* <span data-ttu-id="74567-1290">AzureRM에서 Az 전환 예정에 대한 사소한 변경</span><span class="sxs-lookup"><span data-stu-id="74567-1290">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="74567-1291">DotNet 코어에서 Get-AzureRmSqlDatabaseVulnerabilityAssessment를 사용하는 문제 해결</span><span class="sxs-lookup"><span data-stu-id="74567-1291">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="74567-1292">SQL 감사 cmdlet과 관련된 도움말 메시지의 설명서가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="74567-1292">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="74567-1293">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="74567-1293">Az.Storage</span></span>

* <span data-ttu-id="74567-1294">New-AzureRmStorageAccount에 -EnableHierarchicalNamespace 추가</span><span class="sxs-lookup"><span data-stu-id="74567-1294">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="74567-1295">파일 복사 cmdlet이 -DestContext 입력이 없을 때 대상의 원본 컨텍스트를 다시 사용할 수 없는 문제 수정</span><span class="sxs-lookup"><span data-stu-id="74567-1295">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="74567-1296">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="74567-1296">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="74567-1297">고정적인 웹 사이트 구성 지원</span><span class="sxs-lookup"><span data-stu-id="74567-1297">Support Static Website configuration</span></span>
    - <span data-ttu-id="74567-1298">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="74567-1298">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="74567-1299">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="74567-1299">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="74567-1300">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="74567-1300">Az.Websites</span></span>

* <span data-ttu-id="74567-1301">Set-AzureRmWebApp 및 Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="74567-1301">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span> 
    - <span data-ttu-id="74567-1302">Windows 및 Linux 컨테이너 응용 프로그램에 탑재할 Azure Storage 경로를 지정하기 위해 새 매개 변수(-AzureStoragePath)가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="74567-1302">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="74567-1303">새 cmdlet New-AzureRmWebAppAzureStoragePath의 출력을 매개 변수로 사용하여 Azure Storage 경로를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="74567-1303">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="74567-1304">0.6.1 - 2018년 11월</span><span class="sxs-lookup"><span data-stu-id="74567-1304">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="74567-1305">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="74567-1305">Az.ApiManagement</span></span>
* <span data-ttu-id="74567-1306">형식 매핑 문제에 대한 종속성 업데이트</span><span class="sxs-lookup"><span data-stu-id="74567-1306">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="74567-1307">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="74567-1307">Az.Automation</span></span>
* <span data-ttu-id="74567-1308">Azure Automation cmdlet 기반 Swagger</span><span class="sxs-lookup"><span data-stu-id="74567-1308">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="74567-1309">업데이트 관리 cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="74567-1309">Added Update Management cmdlets</span></span>
* <span data-ttu-id="74567-1310">소스 제어 cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="74567-1310">Added Source Control cmdlets</span></span>
* <span data-ttu-id="74567-1311">Remove-AzureRmAutomationHybridWorkerGroup cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="74567-1311">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="74567-1312">DSC 노드 등록 명령 수정</span><span class="sxs-lookup"><span data-stu-id="74567-1312">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="74567-1313">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="74567-1313">Az.Compute</span></span>
* <span data-ttu-id="74567-1314">SystemAssigned ID에 대한 ID 문제 수정</span><span class="sxs-lookup"><span data-stu-id="74567-1314">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="74567-1315">형식 매핑 문제에 대한 종속성 업데이트</span><span class="sxs-lookup"><span data-stu-id="74567-1315">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="74567-1316">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="74567-1316">Az.ContainerInstance</span></span>
* <span data-ttu-id="74567-1317">형식 매핑 문제에 대한 종속성 업데이트</span><span class="sxs-lookup"><span data-stu-id="74567-1317">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="74567-1318">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="74567-1318">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="74567-1319">마켓플레이스 cmdlet에 대한 예제 설명 업데이트</span><span class="sxs-lookup"><span data-stu-id="74567-1319">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="74567-1320">Az.Network</span><span class="sxs-lookup"><span data-stu-id="74567-1320">Az.Network</span></span>
* <span data-ttu-id="74567-1321">New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="74567-1321">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="74567-1322">지원되는 AzureFirewall 네트워크 프로토콜에 ICMP 다시 추가</span><span class="sxs-lookup"><span data-stu-id="74567-1322">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="74567-1323">Test-AzureRmNetworkWatcherConnectivity cmdlet을 업데이트하여 대상 ID, 주소 및 포트 유효성 검사를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="74567-1323">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span> 
* <span data-ttu-id="74567-1324">VirtualNetwork 맵의 메모리 사용 문제 해결</span><span class="sxs-lookup"><span data-stu-id="74567-1324">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="74567-1325">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="74567-1325">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="74567-1326">보호된 파일 공유에 대한 정책을 수정하는 것에 대해 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="74567-1326">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="74567-1327">정책 표준 시간대를 대문자로 변환했습니다.</span><span class="sxs-lookup"><span data-stu-id="74567-1327">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="74567-1328">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="74567-1328">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="74567-1329">New-AzureRmRecoveryServicesAsrProtectableItem의 예제 정정</span><span class="sxs-lookup"><span data-stu-id="74567-1329">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="74567-1330">형식 매핑 문제에 대한 종속성 업데이트</span><span class="sxs-lookup"><span data-stu-id="74567-1330">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="74567-1331">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="74567-1331">Az.Relay</span></span>
* <span data-ttu-id="74567-1332">선택적 매개 변수 -KeyValue를 New-AzureRmRelayKey cmdlet에 추가하여 사용자가 KeyValue를 제공할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="74567-1332">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="74567-1333">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="74567-1333">Az.Resources</span></span>
* <span data-ttu-id="74567-1334">`New-AzureRmPolicyAssignment` 및 `Set-AzureRmPolicyAssignment`의 자원 ID 관련 매개 변수에 대한 도움말 문서를 업데이트함</span><span class="sxs-lookup"><span data-stu-id="74567-1334">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="74567-1335">-Metadata를 사용하는 New-AzureRmPolicyDefinition에 대한 예제 추가</span><span class="sxs-lookup"><span data-stu-id="74567-1335">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="74567-1336">NetStandard의 태그 키에서 대소문자 보존을 허용하도록 수정: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="74567-1336">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="74567-1337">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="74567-1337">Az.ServiceFabric</span></span>
* <span data-ttu-id="74567-1338">향후 호환성이 손상되는 변경에 대한 사용 중단 메시지 추가</span><span class="sxs-lookup"><span data-stu-id="74567-1338">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="74567-1339">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="74567-1339">Az.Sql</span></span>
* <span data-ttu-id="74567-1340">Azure Sql Database Managed Instance 및 Azure Sql Managed Database에 CRUD 작업을 위한 새 cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="74567-1340">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="74567-1341">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="74567-1341">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="74567-1342">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="74567-1342">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="74567-1343">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="74567-1343">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="74567-1344">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="74567-1344">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="74567-1345">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="74567-1345">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="74567-1346">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="74567-1346">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="74567-1347">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="74567-1347">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="74567-1348">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="74567-1348">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="74567-1349">서버 또는 데이터베이스에서 확장 감사 정책 관리를 활성화했습니다.</span><span class="sxs-lookup"><span data-stu-id="74567-1349">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="74567-1350">새 매개 변수(PredicateExpression)가 감사 로그 필터링을 사용하도록 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="74567-1350">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="74567-1351">Cmdlet이 레거시 클라이언트 대신 SQL 클라이언트를 사용하도록 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="74567-1351">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="74567-1352">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="74567-1352">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="74567-1353">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="74567-1353">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="74567-1354">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="74567-1354">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="74567-1355">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="74567-1355">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="74567-1356">스토리지 계정 이름 매개 변수가 설정된 Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings를 사용할 때의 문제 해결</span><span class="sxs-lookup"><span data-stu-id="74567-1356">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="74567-1357">0.5.0 - 2018년 11월</span><span class="sxs-lookup"><span data-stu-id="74567-1357">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="74567-1358">일반</span><span class="sxs-lookup"><span data-stu-id="74567-1358">General</span></span>
* <span data-ttu-id="74567-1359">많은 핵심 cmdlet에 Resource Completers를 추가하여 대화형으로 cmdlet을 호출할 때 기존 리소스 이름을 탭으로 이동할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="74567-1359">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="74567-1360">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="74567-1360">Az.Profile</span></span>
* <span data-ttu-id="74567-1361">ClientRuntime의 최신 버전을 사용하도록 일반적인 코드를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="74567-1361">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="74567-1362">Connect-AzAccount cmdlet의 매개 변수 TenantId 이름을 Tenant로 바꾸고 TenantId의 별칭을 추가합니다</span><span class="sxs-lookup"><span data-stu-id="74567-1362">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="74567-1363">Connect-AzAccount의 업데이트된 TenantId 설명</span><span class="sxs-lookup"><span data-stu-id="74567-1363">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="74567-1364">테넌트 도메인을 제공할 때 실패한 로그인에 대한 오류 메시지 수정</span><span class="sxs-lookup"><span data-stu-id="74567-1364">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="74567-1365">테넌트에 구독이 없는 계정의 컨텍스트 이름 충돌 문제 수정</span><span class="sxs-lookup"><span data-stu-id="74567-1365">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="74567-1366">MSI를 사용할 때 DataLake 엔드포인트 문제 수정</span><span class="sxs-lookup"><span data-stu-id="74567-1366">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="74567-1367">연결되지 않은 경우 'Disconnect-AzAccount'가 throw하는 문제 수정</span><span class="sxs-lookup"><span data-stu-id="74567-1367">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="74567-1368">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="74567-1368">Az.CognitiveServices</span></span>
* <span data-ttu-id="74567-1369">Get-AzCognitiveServicesAccountSkus 작업을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="74567-1369">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="74567-1370">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="74567-1370">Az.Compute</span></span>
* <span data-ttu-id="74567-1371">Add-AzVmssVMDataDisk 및 Remove-AzVmssVMDataDisk cmdlet를 추가합니다</span><span class="sxs-lookup"><span data-stu-id="74567-1371">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="74567-1372">Get-AzVMImage는 AutomaticOSUpgradeProperties를 표시합니다</span><span class="sxs-lookup"><span data-stu-id="74567-1372">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="74567-1373">수정된 SetAzVMChefExtension -BootstrapOptions 및 -JsonAttribute option 값이 json 형식으로 설정하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="74567-1373">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="74567-1374">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="74567-1374">Az.DataLakeStore</span></span>
* <span data-ttu-id="74567-1375">DataLake 패키지를 1.1.10으로 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="74567-1375">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="74567-1376">기본 동시성을 다중 스레드 작업에 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="74567-1376">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="74567-1377">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="74567-1377">Az.Insights</span></span>
* <span data-ttu-id="74567-1378">해결된 문제 #7267(자동 크기 조정 영역)</span><span class="sxs-lookup"><span data-stu-id="74567-1378">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="74567-1379">열거된 매개 변수를 제대로 설정하지 않은 새 자동 크기 조정 규칙을 만드는 데 문제가 있습니다(이를 항상 기본값으로 설정함).</span><span class="sxs-lookup"><span data-stu-id="74567-1379">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="74567-1380">해결된 문제 # 7513[자세한 정보] Set-AzDiagnosticSetting은 설정을 생성하는 동안 범주를 명시적으로 지정해야 합니다</span><span class="sxs-lookup"><span data-stu-id="74567-1380">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="74567-1381">이제 cmdlet은 생성 중에 사용할 범주를 명시적으로 표시할 필요가 없습니다. 즉, 문서화된대로 작동합니다</span><span class="sxs-lookup"><span data-stu-id="74567-1381">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="74567-1382">Az.Network</span><span class="sxs-lookup"><span data-stu-id="74567-1382">Az.Network</span></span>
* <span data-ttu-id="74567-1383">다음 cmdlet에 대해 PeeringType을 필수 매개 변수로 변경했습니다.</span><span class="sxs-lookup"><span data-stu-id="74567-1383">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="74567-1384">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="74567-1384">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="74567-1385">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="74567-1385">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="74567-1386">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="74567-1386">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="74567-1387">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="74567-1387">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="74567-1388">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="74567-1388">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="74567-1389">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="74567-1389">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="74567-1390">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="74567-1390">Az.PolicyInsights</span></span>
* <span data-ttu-id="74567-1391">추가된 정책 재구성 cmdlet</span><span class="sxs-lookup"><span data-stu-id="74567-1391">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="74567-1392">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="74567-1392">Az.Resources</span></span>
* <span data-ttu-id="74567-1393">에 대 한 수정 https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="74567-1393">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="74567-1394">'Get-AzResource'에 대해 '-ResourceId' 매개 변수를 사용하여 리소스 나열 허용</span><span class="sxs-lookup"><span data-stu-id="74567-1394">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="74567-1395">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="74567-1395">Az.ServiceBus</span></span>
* <span data-ttu-id="74567-1396">마이그레이션 상태를 알 수 있도록 PSServiceBusMigrationConfigurationAttributes에 MigrationState 읽기 전용 속성 추가.</span><span class="sxs-lookup"><span data-stu-id="74567-1396">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="74567-1397">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="74567-1397">Az.ServiceFabric</span></span>
* <span data-ttu-id="74567-1398">Linux Vmss에 인증서 추가 수정.</span><span class="sxs-lookup"><span data-stu-id="74567-1398">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="74567-1399">Add-AzServiceFabricClusterCertificate 수정</span><span class="sxs-lookup"><span data-stu-id="74567-1399">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="74567-1400">새 인증서(Azure/service-fabric-issues#932)에서 올바른 지문을 사용.</span><span class="sxs-lookup"><span data-stu-id="74567-1400">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="74567-1401">올바르게 예외 표시(Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="74567-1401">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="74567-1402">Vmss CreateOrUpdate 작업을 시작하기 전에 'Update-AzServiceFabricDurability'를 수정하여 클러스터 구성 업데이트.</span><span class="sxs-lookup"><span data-stu-id="74567-1402">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="74567-1403">0.4.0 - 2018년 10월</span><span class="sxs-lookup"><span data-stu-id="74567-1403">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="74567-1404">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="74567-1404">Az.Profile</span></span>
* <span data-ttu-id="74567-1405">CloudShell에서 Get-AzSubscription을 사용하여 문제를 해결합니다.</span><span class="sxs-lookup"><span data-stu-id="74567-1405">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="74567-1406">ClientRuntime의 최신 버전을 사용하도록 일반적인 코드를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="74567-1406">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="74567-1407">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="74567-1407">Az.Compute</span></span>
* <span data-ttu-id="74567-1408">'New-AzVm'에 대해 간단한 매개 변수를 사용하는 경우 가속화된 네트워킹을 설정하기 위해 새 크기가 VM 크기의 허용 목록에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="74567-1408">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="74567-1409">모든 cmdlet에 ResourceName 인수 완성자가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="74567-1409">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="74567-1410">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="74567-1410">Az.DataLakeStore</span></span>
* <span data-ttu-id="74567-1411">Virtual Network 규칙에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="74567-1411">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="74567-1412">Get-AzDataLakeStoreVirtualNetworkRule: Azure Data Lake Store 가상 네트워크 규칙을 가져오거나 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="74567-1412">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="74567-1413">Add-AzDataLakeStoreVirtualNetworkRule: 지정된 Data Lake Store 계정에 가상 네트워크 규칙을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="74567-1413">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="74567-1414">Set-AzDataLakeStoreVirtualNetworkRule: 지정된 Data Lake Store 계정에 지정된 가상 네트워크 규칙을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="74567-1414">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="74567-1415">Remove-AzDataLakeStoreVirtualNetworkRule: Azure Data Lake Store 가상 네트워크 규칙을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="74567-1415">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="74567-1416">Az.Network</span><span class="sxs-lookup"><span data-stu-id="74567-1416">Az.Network</span></span>
* <span data-ttu-id="74567-1417">Test-AzNetworkWatcherConnectivity cmdlet을 업데이트하고, 백 엔드에 프로토콜 값을 전달합니다.</span><span class="sxs-lookup"><span data-stu-id="74567-1417">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="74567-1418">모든 cmdlet에 ResourceName 인수 완성자가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="74567-1418">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="74567-1419">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="74567-1419">Az.Resources</span></span>
* <span data-ttu-id="74567-1420">(기본 프로필에 구독이 없고 범위가 지정되지 않은 경우) 시나리오에서 의미 있는 예외를 추가하여 Get-AzRoleDefinition이 인식할 수 없는 예외를 throw하는 문제를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="74567-1420">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="74567-1421">또한 기본 매개 변수 집합을 'RoleDefinitionNameParameterSet'으로 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="74567-1421">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="74567-1422">0.3.0 - 2018년 10월</span><span class="sxs-lookup"><span data-stu-id="74567-1422">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="74567-1423">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="74567-1423">Azure.Storage</span></span>
* <span data-ttu-id="74567-1424">대상에 메타데이터가 있을 때 Blob/파일이 메타 데이터를 복사하지 않는 문제 수정</span><span class="sxs-lookup"><span data-stu-id="74567-1424">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="74567-1425">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="74567-1425">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="74567-1426">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="74567-1426">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="74567-1427">특정 위치의 스토리지 리소스 사용을 지원하고 글로벌 스토리지 리소스 사용 가져오기는 더 이상 사용되지 않는다는 경고 메시지를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="74567-1427">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="74567-1428">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="74567-1428">Get-AzStorageUsage</span></span>
    
#### <a name="azcognitiveservices"></a><span data-ttu-id="74567-1429">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="74567-1429">Az.CognitiveServices</span></span>
* <span data-ttu-id="74567-1430">기존 계정이 없는 Get-AzCognitiveServicesAccountSkus를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="74567-1430">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="74567-1431">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="74567-1431">Az.Compute</span></span>
* <span data-ttu-id="74567-1432">Get-AzVM -ResourceGroupName <rg>가 필요한 경우 50개가 넘는 결과를 반환하도록 수정</span><span class="sxs-lookup"><span data-stu-id="74567-1432">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="74567-1433">'SimpleParameterSet' 예제가 New-AzVmss cmdlet 도움말에 추가됨</span><span class="sxs-lookup"><span data-stu-id="74567-1433">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="74567-1434">Azure Disk Encryption 진행률 메시지의 오타를 수정</span><span class="sxs-lookup"><span data-stu-id="74567-1434">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="74567-1435">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="74567-1435">Az.DataFactoryV2</span></span>
* <span data-ttu-id="74567-1436">ADF.Net SDK 버전을 2.3.0으로 업데이트</span><span class="sxs-lookup"><span data-stu-id="74567-1436">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="74567-1437">Az.Network</span><span class="sxs-lookup"><span data-stu-id="74567-1437">Az.Network</span></span>
* <span data-ttu-id="74567-1438">NetworkProfile 기능 추가</span><span class="sxs-lookup"><span data-stu-id="74567-1438">Added NetworkProfile functionality.</span></span> <span data-ttu-id="74567-1439">추가된 새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="74567-1439">new cmdlets added</span></span>
    - <span data-ttu-id="74567-1440">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="74567-1440">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="74567-1441">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="74567-1441">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="74567-1442">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="74567-1442">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="74567-1443">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="74567-1443">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="74567-1444">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="74567-1444">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="74567-1445">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="74567-1445">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="74567-1446">서브넷 모델에 서비스 연결 링크 추가</span><span class="sxs-lookup"><span data-stu-id="74567-1446">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="74567-1447">New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="74567-1447">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="74567-1448">Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="74567-1448">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="74567-1449">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="74567-1449">Az.RedisCache</span></span>
* <span data-ttu-id="74567-1450">모든 문자열을 Size 매개 변수로 진행되도록 허용</span><span class="sxs-lookup"><span data-stu-id="74567-1450">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="74567-1451">PSArgumentCompleter 팝업에 P5 추가</span><span class="sxs-lookup"><span data-stu-id="74567-1451">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="74567-1452">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="74567-1452">Az.Resources</span></span>
* <span data-ttu-id="74567-1453">-Mode 매개 변수를 Set-AzPolicyDefinition에 추가</span><span class="sxs-lookup"><span data-stu-id="74567-1453">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="74567-1454">사용자가 포함된 Origin 작업에서 Get-AzProviderOperation commandlet 버그 수정</span><span class="sxs-lookup"><span data-stu-id="74567-1454">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="74567-1455">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="74567-1455">Az.Sql</span></span>
* <span data-ttu-id="74567-1456">일부 백업 cmdlet이 현재 azure 구독을 인식하지 않는 문제 해결</span><span class="sxs-lookup"><span data-stu-id="74567-1456">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="74567-1457">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="74567-1457">Az.Websites</span></span>
* <span data-ttu-id="74567-1458">새 cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - 컨테이너 지속적인 배포 Webhook URL을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="74567-1458">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="74567-1459">새 cmdlet New-AzWebAppContainerPSSession 및 Enter-WebAppContainerPSSession -  windows 컨테이너 앱에 PowerShell 원격 세션을 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="74567-1459">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="74567-1460">0.2.0 - 2018년 9월</span><span class="sxs-lookup"><span data-stu-id="74567-1460">0.2.0 - September 2018</span></span>
 <span data-ttu-id="74567-1461">최초 릴리스</span><span class="sxs-lookup"><span data-stu-id="74567-1461">Initial Release</span></span>