---
ms.openlocfilehash: e72aae940b48543d6a99801032186112748ea48b
ms.sourcegitcommit: 6c0d296bfec7c1c35a1d15074ca5eacda6684ea4
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/30/2019
ms.locfileid: "68657963"
---
## <a name="250---july-2019"></a><span data-ttu-id="6295f-101">2.5.0 - 2019년 7월</span><span class="sxs-lookup"><span data-stu-id="6295f-101">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="6295f-102">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6295f-102">Az.Accounts</span></span>
* <span data-ttu-id="6295f-103">ClientRuntime의 최신 버전을 사용하도록 일반적인 코드를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-103">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="6295f-104">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="6295f-104">Az.ApplicationInsights</span></span>
* <span data-ttu-id="6295f-105">'Remove-AzApplicationInsightsApiKey' 설명서의 예제 오타 수정</span><span class="sxs-lookup"><span data-stu-id="6295f-105">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span> 

#### <a name="azautomation"></a><span data-ttu-id="6295f-106">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="6295f-106">Az.Automation</span></span>
* <span data-ttu-id="6295f-107">리소스 문자열의 오타 수정</span><span class="sxs-lookup"><span data-stu-id="6295f-107">Fix typo in resource string</span></span> 

#### <a name="azcognitiveservices"></a><span data-ttu-id="6295f-108">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="6295f-108">Az.CognitiveServices</span></span>
* <span data-ttu-id="6295f-109">NetworkRuleSet 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-109">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6295f-110">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6295f-110">Az.Compute</span></span>
* <span data-ttu-id="6295f-111">VM 인스턴스 보기 개체의 누락된 속성(ComputerName, OsName, OsVersion 및 HyperVGeneration)을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-111">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="6295f-112">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="6295f-112">Az.ContainerRegistry</span></span>
* <span data-ttu-id="6295f-113">복제 매개 변수의 Remove-AzContainerRegistryReplication에서 오타 수정</span><span class="sxs-lookup"><span data-stu-id="6295f-113">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="6295f-114">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/9633 을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="6295f-114">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="6295f-115">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="6295f-115">Az.DataFactory</span></span>
* <span data-ttu-id="6295f-116">ADF .Net SDK 버전을 4.1.0으로 업데이트</span><span class="sxs-lookup"><span data-stu-id="6295f-116">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="6295f-117">'Get-AzDataFactoryV2PipelineRun' 설명서의 오타 수정</span><span class="sxs-lookup"><span data-stu-id="6295f-117">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="6295f-118">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="6295f-118">Az.EventHub</span></span>
* <span data-ttu-id="6295f-119">SAS 토큰을 생성하기 위해 추가된 새로운 cmmdlet 추가: New-AzEventHubAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="6295f-119">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="6295f-120">'관리'만 지정된 경우 authorizationrules 권한에 대한 확인 및 오류 메시지 추가</span><span class="sxs-lookup"><span data-stu-id="6295f-120">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="6295f-121">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="6295f-121">Az.KeyVault</span></span>
* <span data-ttu-id="6295f-122">인증서 정책에 대한 KeySize 지정을 위한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="6295f-122">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="6295f-123">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="6295f-123">Az.LogicApp</span></span>
* <span data-ttu-id="6295f-124">모든 맵 유형을 나열하도록 Get-AzIntegrationAccountMap 수정</span><span class="sxs-lookup"><span data-stu-id="6295f-124">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="6295f-125">필터링을 위해 새 MapType 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="6295f-125">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="6295f-126">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="6295f-126">Az.ManagedServices</span></span>
* <span data-ttu-id="6295f-127">API 버전 2019-06-01(GA)에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="6295f-127">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6295f-128">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6295f-128">Az.Network</span></span>
* <span data-ttu-id="6295f-129">프라이빗 엔드포인트 및 프라이빗 링크 서비스에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="6295f-129">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="6295f-130">새 cmdlet</span><span class="sxs-lookup"><span data-stu-id="6295f-130">New cmdlets</span></span>
        - <span data-ttu-id="6295f-131">Set-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="6295f-131">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="6295f-132">Set-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="6295f-132">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="6295f-133">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="6295f-133">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="6295f-134">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="6295f-134">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="6295f-135">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="6295f-135">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="6295f-136">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="6295f-136">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="6295f-137">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="6295f-137">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="6295f-138">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="6295f-138">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="6295f-139">기능에 대한 새로운 명령이 업데이트됨: Virtualnetwork의 서브넷에 있는 PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies 플래그</span><span class="sxs-lookup"><span data-stu-id="6295f-139">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="6295f-140">업데이트된 New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="6295f-140">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="6295f-141">이 서브넷의 프라이빗 엔드포인트에 네트워크 정책을 적용하는지 적용하지 않는지 나타내는 선택적 매개 변수 -PrivateEndpointNetworkPoliciesFlag를 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-141">Added optional parameter -PrivateEndpointNetworkPoliciesFlag to indicate that enable or disable apply network policies on pivate endpoint in this subnet.</span></span>
        - <span data-ttu-id="6295f-142">이 서브넷의 프라이빗 링크 서비스에 네트워크 정책을 적용하는지 적용하지 않는지 나타내는 선택적 매개 변수 -PrivateLinkServiceNetworkPoliciesFlag를 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-142">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag to indicate that enable or disable apply network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="6295f-143">AzPrivateLinkService의 cmdlet 매개 변수 'ServiceName'이 이전 버전과의 호환성을 위해 별칭 'ServiceName'을 사용한 'Name'으로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-143">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="6295f-144">네트워크 보안 규칙 구성에 ICMP 프로토콜 사용</span><span class="sxs-lookup"><span data-stu-id="6295f-144">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="6295f-145">다음 Cmdlet이 업데이트 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-145">Updated cmdlets</span></span>
        - <span data-ttu-id="6295f-146">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="6295f-146">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="6295f-147">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="6295f-147">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="6295f-148">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="6295f-148">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="6295f-149">New-AzVirtualNetworkGatewayConnection에 대한 구성 가능한 매개 변수로 ConnectionProtocolType (Ikev1/Ikev2) 추가</span><span class="sxs-lookup"><span data-stu-id="6295f-149">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="6295f-150">LoadBalancerFrontendIpConfiguration에 PrivateIpAddressVersion 추가</span><span class="sxs-lookup"><span data-stu-id="6295f-150">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="6295f-151">업데이트된 cmdlet:</span><span class="sxs-lookup"><span data-stu-id="6295f-151">Updated cmdlet:</span></span>
        - <span data-ttu-id="6295f-152">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="6295f-152">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="6295f-153">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="6295f-153">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="6295f-154">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="6295f-154">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="6295f-155">프로브에서 사용자 지정 포트를 지원하기 위한 Application Gateway New-AzApplicationGatewayProbeConfig 명령 업데이트</span><span class="sxs-lookup"><span data-stu-id="6295f-155">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="6295f-156">업데이트된 New-AzApplicationGatewayProbeConfig: 백 엔드 서버 검색에 사용되는 선택적 매개 변수 포트가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-156">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="6295f-157">이 매개 변수는 Standard_V2 및 WAF_V2 SKU에 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-157">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="6295f-158">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="6295f-158">Az.OperationalInsights</span></span>
* <span data-ttu-id="6295f-159">저장된 검색의 기본 버전이 1로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-159">Updated default version for saved searches to be 1.</span></span> 
* <span data-ttu-id="6295f-160">사용자 지정 로그 null regex 처리가 수정됨</span><span class="sxs-lookup"><span data-stu-id="6295f-160">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="6295f-161">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="6295f-161">Az.RecoveryServices</span></span>
* <span data-ttu-id="6295f-162">'Get-AzRecoveryServicesBackupJob.md' 업데이트</span><span class="sxs-lookup"><span data-stu-id="6295f-162">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="6295f-163">'Get-AzRecoveryServicesBackupContainer.md' 업데이트</span><span class="sxs-lookup"><span data-stu-id="6295f-163">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="6295f-164">'Get-AzRecoveryServicesVault.md' 업데이트</span><span class="sxs-lookup"><span data-stu-id="6295f-164">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="6295f-165">'Wait-AzRecoveryServicesBackupJob.md' 업데이트</span><span class="sxs-lookup"><span data-stu-id="6295f-165">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="6295f-166">'Set-AzRecoveryServicesVaultContext.md' 업데이트</span><span class="sxs-lookup"><span data-stu-id="6295f-166">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="6295f-167">'Get-AzRecoveryServicesBackupItem.md' 업데이트</span><span class="sxs-lookup"><span data-stu-id="6295f-167">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="6295f-168">'Get-AzRecoveryServicesBackupRecoveryPoint.md' 업데이트</span><span class="sxs-lookup"><span data-stu-id="6295f-168">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="6295f-169">'Restore-AzRecoveryServicesBackupItem.md' 업데이트</span><span class="sxs-lookup"><span data-stu-id="6295f-169">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="6295f-170">Azure 파일 공유용 컨테이너를 등록 취소하기 위해 서비스 요청 업데이트</span><span class="sxs-lookup"><span data-stu-id="6295f-170">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="6295f-171">'Set-AzRecoveryServicesAsrAlertSetting.md' 업데이트</span><span class="sxs-lookup"><span data-stu-id="6295f-171">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="6295f-172">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6295f-172">Az.Resources</span></span>
- <span data-ttu-id="6295f-173">'New-AzResourceGroupDeployment' 설명서에서 참조된 누락 cmdlet 제거</span><span class="sxs-lookup"><span data-stu-id="6295f-173">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="6295f-174">새 API 버전 2019-01-01을 사용하도록 정책 cmdlet 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="6295f-174">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="6295f-175">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="6295f-175">Az.ServiceBus</span></span>
* <span data-ttu-id="6295f-176">SAS 토큰을 생성하기 위해 추가된 새로운 cmmdlet 추가: New-AzServiceBusAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="6295f-176">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="6295f-177">'관리'만 지정된 경우 authorizationrules 권한에 대한 확인 및 오류 메시지 추가</span><span class="sxs-lookup"><span data-stu-id="6295f-177">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="6295f-178">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6295f-178">Az.Sql</span></span>
* <span data-ttu-id="6295f-179">Set-AzSqlDatabaseSecondary cmdlet에 대한 누락된 예제 수정</span><span class="sxs-lookup"><span data-stu-id="6295f-179">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="6295f-180">이메일 주소를 제공하지 않고 설정된 취약성 평가 반복 검색 수정</span><span class="sxs-lookup"><span data-stu-id="6295f-180">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="6295f-181">경고 메시지의 작은 오타를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-181">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="6295f-182">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="6295f-182">Az.Storage</span></span>
* <span data-ttu-id="6295f-183">'Get-AzStorageAccount'에 대한 참조 설명서의 예제를 업데이트하여 올바른 매개 변수 이름 사용</span><span class="sxs-lookup"><span data-stu-id="6295f-183">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="6295f-184">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="6295f-184">Az.StorageSync</span></span>
* <span data-ttu-id="6295f-185">Invoke-AzStorageSyncChangeDetection cmdlet을 추가하는 중입니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-185">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="6295f-186">TierFilesOlderThanDays를 기념하는 문제 9551 수정</span><span class="sxs-lookup"><span data-stu-id="6295f-186">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="6295f-187">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="6295f-187">Az.Websites</span></span>
* <span data-ttu-id="6295f-188">Get-AzWebApp 및 Set-AzWebApp에서 일부 SiteConfig 속성을 반환하지 않은 버그 수정</span><span class="sxs-lookup"><span data-stu-id="6295f-188">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="6295f-189">Get-AzDeletedWebApp 및 Restore-AzDeletedWebApp에 새 위치 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="6295f-189">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="6295f-190">AzWebApp-IncludeSourceWebAppSlots을 사용하여 웹앱 슬롯을 복제하는 버그를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-190">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="6295f-191">2.4.0 - 2019년 7월</span><span class="sxs-lookup"><span data-stu-id="6295f-191">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="6295f-192">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6295f-192">Az.Accounts</span></span>
* <span data-ttu-id="6295f-193">프로필 cmdlet에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="6295f-193">Add support for profile cmdlets</span></span>
* <span data-ttu-id="6295f-194">생성된 cmdlet에서 환경 및 데이터 평면에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="6295f-194">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="6295f-195">Windows PowerShell의 데이터 평면 cmdlet에대해 일부 경우 잘못된 엔드포인트가 사용되는 버그 수정</span><span class="sxs-lookup"><span data-stu-id="6295f-195">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="6295f-196">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="6295f-196">Az.Advisor</span></span>
* <span data-ttu-id="6295f-197">Az.Advisor의 GA 릴리스</span><span class="sxs-lookup"><span data-stu-id="6295f-197">GA release of Az.Advisor</span></span>
* <span data-ttu-id="6295f-198">이 모듈은 이제 롤업 `Az` 모듈의 일부로 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-198">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="6295f-199">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="6295f-199">Az.ApiManagement</span></span>
* <span data-ttu-id="6295f-200">문제 https://github.com/Azure/azure-powershell/issues/8671 수정</span><span class="sxs-lookup"><span data-stu-id="6295f-200">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="6295f-201">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="6295f-201">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="6295f-202">사용자 및 제품별 구독을 쿼리하기 위한 지원이 추가됨</span><span class="sxs-lookup"><span data-stu-id="6295f-202">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="6295f-203">범위 '/', '/ api, '/ api/echo api'를 사용하여 쿼리하기 위한 지원이 추가됨</span><span class="sxs-lookup"><span data-stu-id="6295f-203">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="6295f-204">https://github.com/Azure/azure-powershell/issues/9307 및 https://github.com/Azure/azure-powershell/issues/8432 문제 수정</span><span class="sxs-lookup"><span data-stu-id="6295f-204">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="6295f-205">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="6295f-205">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="6295f-206">Apis를 가져올 때 'ApiVersion' 및 'ApiVersionSetId'를 지정하기 위한 지원이 추가됨</span><span class="sxs-lookup"><span data-stu-id="6295f-206">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="6295f-207">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="6295f-207">Az.Automation</span></span>
* <span data-ttu-id="6295f-208">문자열 값을 처리하기 위해 Set-AzAutomationConnectionFieldValue cmdlet 버그를 수정했습니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-208">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6295f-209">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6295f-209">Az.Compute</span></span>
* <span data-ttu-id="6295f-210">New-AzImageConfig에 HyperVGeneration 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="6295f-210">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="6295f-211">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="6295f-211">Az.DataFactory</span></span>
* <span data-ttu-id="6295f-212">get activity runs, get pipeline runs, get trigger runs ADF cmdlet의 출력을 업데이트하여 Select-Object pipe를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-212">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="6295f-213">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="6295f-213">Az.EventGrid</span></span>
* <span data-ttu-id="6295f-214">'New-AzEventGridSubcription' 설명서의 오타 수정</span><span class="sxs-lookup"><span data-stu-id="6295f-214">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="6295f-215">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="6295f-215">Az.IotHub</span></span>
* <span data-ttu-id="6295f-216">권한 부여 정책 키를 다시 생성하기 위한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="6295f-216">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6295f-217">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6295f-217">Az.Network</span></span>
* <span data-ttu-id="6295f-218">'RoutingPreference'를 공용 IP 태그에 추가함</span><span class="sxs-lookup"><span data-stu-id="6295f-218">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="6295f-219">'Get-AzNetworkServiceTag' 참조 설명서의 예제 개선</span><span class="sxs-lookup"><span data-stu-id="6295f-219">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="6295f-220">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="6295f-220">Az.PolicyInsights</span></span>
* <span data-ttu-id="6295f-221">Get-AzPolicyState의 null 참조 문제 해결</span><span class="sxs-lookup"><span data-stu-id="6295f-221">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="6295f-222">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/9446 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="6295f-222">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="6295f-223">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="6295f-223">Az.OperationalInsights</span></span>
* <span data-ttu-id="6295f-224">Get-AzOperationalInsightsDataSource에 반환된 CustomLog datasource 모델 수정됨</span><span class="sxs-lookup"><span data-stu-id="6295f-224">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="6295f-225">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="6295f-225">Az.RecoveryServices</span></span>
* <span data-ttu-id="6295f-226">IaaSVMs에 대한 get-policy 명령 수정</span><span class="sxs-lookup"><span data-stu-id="6295f-226">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="6295f-227">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6295f-227">Az.Resources</span></span>
    - <span data-ttu-id="6295f-228">Get-AzPolicyState -Top 매개 변수에 대한 도움말 텍스트 수정</span><span class="sxs-lookup"><span data-stu-id="6295f-228">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="6295f-229">Get-AzPolicyAlias에 대한 클라이언트 쪽 페이징 지원 추가</span><span class="sxs-lookup"><span data-stu-id="6295f-229">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="6295f-230">Set-AzPolicyAssignment, -PolicyParameters 및 -PolicyParametersObject에 대한 새 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="6295f-230">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="6295f-231">Policy cmdlet에 대한 몇 가지 문서 및 예제 업데이트</span><span class="sxs-lookup"><span data-stu-id="6295f-231">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="6295f-232">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="6295f-232">Az.ServiceBus</span></span>
* <span data-ttu-id="6295f-233">문제 #4938 수정 - MaxSizeInMegabytes를 설정할 때 New-AzureRmServiceBusQueue가 BadRequest 반환</span><span class="sxs-lookup"><span data-stu-id="6295f-233">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="6295f-234">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6295f-234">Az.Sql</span></span>
* <span data-ttu-id="6295f-235">미리 보기 릴리스에서 공개 릴리스로 인스턴스 장애 조치(Failover) 그룹 cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="6295f-235">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="6295f-236">새 cmdlet으로 Azure SQL Server\Database Auditing을 지원하세요.</span><span class="sxs-lookup"><span data-stu-id="6295f-236">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="6295f-237">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="6295f-237">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="6295f-238">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="6295f-238">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="6295f-239">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="6295f-239">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="6295f-240">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="6295f-240">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="6295f-241">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="6295f-241">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="6295f-242">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="6295f-242">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="6295f-243">취약성 평가 설정에서 이메일 제약 조건 제거</span><span class="sxs-lookup"><span data-stu-id="6295f-243">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="6295f-244">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="6295f-244">Az.Storage</span></span>
* <span data-ttu-id="6295f-245">다음 cmdlet에서 2개의 매개 변수 '-IndexDocument' 및 '-ErrorDocument404Path'를 필수에서 선택으로 변경하세요.</span><span class="sxs-lookup"><span data-stu-id="6295f-245">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="6295f-246">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="6295f-246">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="6295f-247">예제를 추가하여 Get-AzStorageBlobContent의 도움말 업데이트</span><span class="sxs-lookup"><span data-stu-id="6295f-247">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="6295f-248">StorageException으로 cmdlet이 실패한 경우 자세한 오류 정보 표시</span><span class="sxs-lookup"><span data-stu-id="6295f-248">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="6295f-249">Azure Files AAD DS 인증으로 스토리지 계정 생성 또는 업데이트 지원</span><span class="sxs-lookup"><span data-stu-id="6295f-249">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="6295f-250">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6295f-250">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="6295f-251">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6295f-251">Set-AzStorageAccount</span></span>
* <span data-ttu-id="6295f-252">파일 공유, 파일 디렉터리 또는 파일의 목록 지원 또는 파일 핸들 닫기</span><span class="sxs-lookup"><span data-stu-id="6295f-252">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="6295f-253">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="6295f-253">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="6295f-254">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="6295f-254">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="6295f-255">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="6295f-255">Az.StorageSync</span></span>
* <span data-ttu-id="6295f-256">이 모듈은 이제 롤업 `Az` 모듈의 일부로 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-256">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="6295f-257">2.3.2 - 2019년 6월</span><span class="sxs-lookup"><span data-stu-id="6295f-257">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="6295f-258">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6295f-258">Az.Accounts</span></span>
* <span data-ttu-id="6295f-259">함수 호출에 대해 일부 경우 잘못된 URL이 사용되는 버그 수정</span><span class="sxs-lookup"><span data-stu-id="6295f-259">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="6295f-260">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/8983 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="6295f-260">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="6295f-261">AzureRM에서 Az cmdlet으로의 별칭 문제 해결</span><span class="sxs-lookup"><span data-stu-id="6295f-261">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="6295f-262">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="6295f-262">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="6295f-263">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="6295f-263">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6295f-264">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6295f-264">Az.Compute</span></span>
* <span data-ttu-id="6295f-265">New-AzVm 및 New-AzVmss 단순 매개 변수 집합은 이제 'ProximityPlacementGroup'매개 변수를 허용합니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-265">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="6295f-266">'New-AzVM' 참조 설명서에서 오타 수정</span><span class="sxs-lookup"><span data-stu-id="6295f-266">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="6295f-267">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="6295f-267">Az.Dns</span></span>
* <span data-ttu-id="6295f-268">'Set-AzDnsZone' 도움말 예제의 오타가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-268">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="6295f-269">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="6295f-269">Az.EventGrid</span></span>
* <span data-ttu-id="6295f-270">2019-06-01 API 버전을 사용하도록 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-270">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="6295f-271">새 cmdlet:</span><span class="sxs-lookup"><span data-stu-id="6295f-271">New cmdlets:</span></span>
    - <span data-ttu-id="6295f-272">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="6295f-272">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="6295f-273">새 Azure Event Grid 도메인을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-273">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="6295f-274">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="6295f-274">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="6295f-275">Event Grid 도메인의 세부 정보를 가져오거나 현재 Azure 구독의 모든 Event Grid 도메인 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-275">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="6295f-276">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="6295f-276">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="6295f-277">Azure Event Grid 도메인을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-277">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="6295f-278">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="6295f-278">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="6295f-279">Azure Event Grid 도메인에 대한 공유 액세스 키를 다시 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-279">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="6295f-280">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="6295f-280">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="6295f-281">Event Grid 도메인 이벤트를 게시하는 데 사용되는 공유 액세스 키를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-281">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="6295f-282">New-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="6295f-282">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="6295f-283">새 Azure Event Grid 도메인 토픽을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-283">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="6295f-284">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="6295f-284">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="6295f-285">Event Grid 도메인 토픽의 세부 사항을 가져오거나, 현재 Azure의 특정 Event Grid 도메인 아래의 모든 Event Grid 도메인 토픽 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-285">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span> 
    - <span data-ttu-id="6295f-286">Remove-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="6295f-286">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="6295f-287">기존 Azure Event Grid 도메인 토픽을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-287">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="6295f-288">다음 Cmdlet이 업데이트 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-288">Updated cmdlets:</span></span>
    - <span data-ttu-id="6295f-289">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="6295f-289">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="6295f-290">새로운 Event Grid 도메인 및 Event Grid 도메인 토픽에 대한 파이핑을 지원하기 위해 새로운 필수 매개 변수를 추가하여 이러한 리소스 아래에 새 이벤트 구독을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-290">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="6295f-291">새로운 Event Grid 도메인 이름 및 Event Grid 도메인 토픽 이름을 지정하기 위해 새로운 필수 매개 변수를 추가하여 이러한 리소스 아래에 새 이벤트 구독을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-291">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="6295f-292">기존 매개 변수(예: EndPointType, SubjectBeginsWith 등)를 재사용할 수 있도록 도메인 및 도메인 토픽에 대한 새로운 매개 변수 집합을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-292">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="6295f-293">지정을 위한 새로운 선택적 매개 변수를 추가</span><span class="sxs-lookup"><span data-stu-id="6295f-293">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="6295f-294">이벤트 구독 만료 날짜,</span><span class="sxs-lookup"><span data-stu-id="6295f-294">Event subscription expiration date,</span></span>
            - <span data-ttu-id="6295f-295">고급 필터링 매개 변수.</span><span class="sxs-lookup"><span data-stu-id="6295f-295">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="6295f-296">대상으로 servicebusqueue에 대한 새 열거형을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-296">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="6295f-297">-IncludedEventType 옵션에서 'All' 사용을 허용하지 않고 다음으로 대체함</span><span class="sxs-lookup"><span data-stu-id="6295f-297">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span> 
    - <span data-ttu-id="6295f-298">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="6295f-298">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="6295f-299">결과 페이지 매김 및 필터링을 지원하는 새로운 선택적 매개 변수(Top, ODataQuery 및 NextLink)를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-299">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="6295f-300">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="6295f-300">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="6295f-301">Event Grid 도메인 및 Event Grid 도메인 토픽에 대한 파이핑을 지원하기 위해 새로운 필수 매개 변수를 추가하여 이러한 리소스 아래에 기존 이벤트 구독을 제거할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-301">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="6295f-302">Event Grid 도메인 이름 및 Event Grid 도메인 토픽 이름을 지정하기 위해 새로운 필수 매개 변수를 추가하여 이러한 리소스 아래에 기존 이벤트 구독을 제거할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-302">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="6295f-303">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="6295f-303">Az.FrontDoor</span></span>
* <span data-ttu-id="6295f-304">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="6295f-304">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="6295f-305">변환 지원 및 새 연산자 자동 완성 값(RegEx)을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-305">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="6295f-306">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="6295f-306">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="6295f-307">새 자동 완성 값 추가</span><span class="sxs-lookup"><span data-stu-id="6295f-307">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6295f-308">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6295f-308">Az.Network</span></span>
* <span data-ttu-id="6295f-309">Microsoft Azure Virtual Network 게이트웨이 리소스에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="6295f-309">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="6295f-310">새 cmdlet</span><span class="sxs-lookup"><span data-stu-id="6295f-310">New cmdlets</span></span>
        - <span data-ttu-id="6295f-311">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="6295f-311">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="6295f-312">AvailablePrivateEndpointType 추가</span><span class="sxs-lookup"><span data-stu-id="6295f-312">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="6295f-313">새 cmdlet</span><span class="sxs-lookup"><span data-stu-id="6295f-313">New cmdlets</span></span> 
        - <span data-ttu-id="6295f-314">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="6295f-314">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="6295f-315">PrivatePrivateLinkService 추가</span><span class="sxs-lookup"><span data-stu-id="6295f-315">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="6295f-316">새 cmdlet</span><span class="sxs-lookup"><span data-stu-id="6295f-316">New cmdlets</span></span> 
        - <span data-ttu-id="6295f-317">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="6295f-317">Get-AzPrivateLinkService</span></span> 
        - <span data-ttu-id="6295f-318">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="6295f-318">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="6295f-319">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="6295f-319">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="6295f-320">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="6295f-320">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="6295f-321">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="6295f-321">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="6295f-322">PrivateEndpoint 추가</span><span class="sxs-lookup"><span data-stu-id="6295f-322">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="6295f-323">새 cmdlet</span><span class="sxs-lookup"><span data-stu-id="6295f-323">New cmdlets</span></span>
        - <span data-ttu-id="6295f-324">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="6295f-324">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="6295f-325">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="6295f-325">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="6295f-326">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="6295f-326">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="6295f-327">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="6295f-327">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="6295f-328">기능에 대한 새로운 명령이 업데이트됨: VpnConnection 상의 UseLocalAzureIpAddress 플래그</span><span class="sxs-lookup"><span data-stu-id="6295f-328">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="6295f-329">New-AzVpnConnection이 업데이트됨: 선택적 매개 변수 -UseLocalAzureIpAddress를 추가하여 로컬 Azure IP 주소가 연결을 시작하는 동안 소스 주소로 사용되어야 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-329">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="6295f-330">Set-AzVpnConnection이 업데이트됨: 선택적 매개 변수 -UseLocalAzureIpAddress를 추가하여 로컬 Azure IP 주소가 연결을 시작하는 동안 소스 주소로 사용되어야 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-330">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="6295f-331">ExpressRoute 피어링에 읽기 전용 필드 PeeredConnections가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-331">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="6295f-332">ExpressRoute에 읽기 전용 필드 GlobalReachEnabled가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-332">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="6295f-333">ExpressRouteCircuit 모델에서 AllowGlobalReach 필드의 사용 중단을 부르는 호환성이 손상되는 변경 속성이 추가됨</span><span class="sxs-lookup"><span data-stu-id="6295f-333">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="6295f-334">AzApplicationGatewayRedirectConfiguration cmdlet에서 TargetListenerID를 사용하는 중의 8756 오류 문제가 해결됨</span><span class="sxs-lookup"><span data-stu-id="6295f-334">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="6295f-335">다시 쓰기 규칙 세트가 설정되지 못하게 하는 New-AzApplicationGatewayPathRuleConfig의 버그를 수정했습니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-335">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="6295f-336">NetworkInterfaceIpConfiguration에 VirtualNetworkTaps가 표시되는 방식이 수정됨</span><span class="sxs-lookup"><span data-stu-id="6295f-336">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="6295f-337">모든 파트를 나열하도록 Cortex Get cmdlet이 수정됨</span><span class="sxs-lookup"><span data-stu-id="6295f-337">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="6295f-338">ExpressRouteGateways, VpnGateway에 대한 VirtualHub 참조 생성 수정됨</span><span class="sxs-lookup"><span data-stu-id="6295f-338">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="6295f-339">AzureFirewall 및 NatGateway의 가용성 영역에 대한 지원 추가됨</span><span class="sxs-lookup"><span data-stu-id="6295f-339">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="6295f-340">Get-AzNetworkServiceTag cmdlet 추가됨</span><span class="sxs-lookup"><span data-stu-id="6295f-340">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="6295f-341">Azure Firewall에 대한 여러 공용 IP 주소에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="6295f-341">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="6295f-342">New-AzFirewall cmdlet이 업데이트됨:</span><span class="sxs-lookup"><span data-stu-id="6295f-342">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="6295f-343">하나 이상의 공용 IP 주소 개체를 허용하는 매개 변수 -PublicIpAddress 추가됨</span><span class="sxs-lookup"><span data-stu-id="6295f-343">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="6295f-344">Virtual Network 개체를 허용하는 매개 변수 -VirtualNetwork 추가됨</span><span class="sxs-lookup"><span data-stu-id="6295f-344">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="6295f-345">방화벽 개체에 AddPublicIpAddress 및 RemovePublicIpAddress 메서드 추가됨 - 공용 IP 주소 개체를 입력으로 허용</span><span class="sxs-lookup"><span data-stu-id="6295f-345">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="6295f-346">매개 변수 -PublicIpName 및 -VirtualNetworkName이 더 이상 사용되지 않음</span><span class="sxs-lookup"><span data-stu-id="6295f-346">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span> 
* <span data-ttu-id="6295f-347">기능에 대한 새로운 명령이 업데이트됨: VpnClient AAD 인증 옵션을 가상 네트워크 게이트웨이 리소스로 설정했습니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-347">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span> 
    - <span data-ttu-id="6295f-348">New-AzVirtualNetworkGateway가 업데이트됨: 게이트웨이에서 VpnClient AAD 인증 옵션을 설정할 수 있도록 선택적 매개 변수 AadTenantUri, AadAudienceId, AadIssuerUri가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-348">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="6295f-349">Set-AzVirtualNetworkGateway가 업데이트됨: 게이트웨이에서 VpnClient AAD 인증 옵션을 설정할 수 있도록 선택적 매개 변수 AadTenantUri, AadAudienceId, AadIssuerUri가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-349">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="6295f-350">Set-AzVirtualNetworkGateway가 업데이트됨: 게이트웨이에서 VpnClient AAD 인증 옵션을 제거할 수 있도록 선택적인 스위치 매개 변수 RemoveAadAuthentication이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-350">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="6295f-351">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="6295f-351">Az.OperationalInsights</span></span>
* <span data-ttu-id="6295f-352">'New-AzureRmOperationalInsightsWorkspace' 명령에서 **pergb2018** 가격 책정 계층 사용</span><span class="sxs-lookup"><span data-stu-id="6295f-352">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="6295f-353">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6295f-353">Az.Resources</span></span>
* <span data-ttu-id="6295f-354">추가 템플릿 내보내기 옵션 지원</span><span class="sxs-lookup"><span data-stu-id="6295f-354">Support for additional Template Export options</span></span>
    - <span data-ttu-id="6295f-355">Export-AzResourceGroup에 '-SkipResourceNameParameterization' 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="6295f-355">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="6295f-356">Export-AzResourceGroup에 '-SkipAllParameterization' 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="6295f-356">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="6295f-357">내보낸 리소스 필터링을 위해 Export-AzResourceGroup에 '-Resource' 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="6295f-357">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="6295f-358">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="6295f-358">Az.ServiceFabric</span></span>
* <span data-ttu-id="6295f-359">일부 경우 잘못된 지문을 가져오는 추가 인증서 ByExistingKeyVault 수정</span><span class="sxs-lookup"><span data-stu-id="6295f-359">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="6295f-360">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6295f-360">Az.Sql</span></span>
* <span data-ttu-id="6295f-361">Advanced Threat Protection 스토리지 엔드포인트 접미사 수정</span><span class="sxs-lookup"><span data-stu-id="6295f-361">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="6295f-362">Advanced Data Security가 Advanced Threat Protection 정책을 재정의하는 것을 수정</span><span class="sxs-lookup"><span data-stu-id="6295f-362">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="6295f-363">고객이 TDE 키를 추가하고 관리되는 인스턴스에 TDE 보호기를 설정할 수 있도록 Management.Sql용 새 Cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="6295f-363">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="6295f-364">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="6295f-364">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="6295f-365">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="6295f-365">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="6295f-366">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="6295f-366">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="6295f-367">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="6295f-367">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="6295f-368">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="6295f-368">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="6295f-369">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="6295f-369">Az.Storage</span></span>
* <span data-ttu-id="6295f-370">스토리지 계정 생성 시 종류 FileStorage 및 SkuName Premium_ZRS 지원</span><span class="sxs-lookup"><span data-stu-id="6295f-370">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="6295f-371">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6295f-371">New-AzStorageAccount</span></span>
* <span data-ttu-id="6295f-372">BLOB immutability cmdlet의 설명 명확화</span><span class="sxs-lookup"><span data-stu-id="6295f-372">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="6295f-373">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="6295f-373">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="6295f-374">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="6295f-374">Az.Websites</span></span>
* <span data-ttu-id="6295f-375">Get-AzWebAppCertificate를 클라이언트 대신 서버의 리소스 그룹별로 필터링하도록 최적화</span><span class="sxs-lookup"><span data-stu-id="6295f-375">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="6295f-376">Get-AzWebAppSnapshot에 -UseDisasterRecovery 스위치 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="6295f-376">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="6295f-377">2.2.0 - 2019년 6월</span><span class="sxs-lookup"><span data-stu-id="6295f-377">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="6295f-378">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="6295f-378">Az.Cdn</span></span>
* <span data-ttu-id="6295f-379">cmdlet에서 2019-04-15 API 버전 기반의 rulesEngine 기능을 지원하도록 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-379">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6295f-380">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6295f-380">Az.Compute</span></span>
* <span data-ttu-id="6295f-381">작업을 시작하여 완료되기 전에 즉시 반환하는 `NoWait` 매개 변수가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-381">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="6295f-382">다음 Cmdlet이 업데이트 되었습니다.   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="6295f-382">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="6295f-383">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="6295f-383">Az.EventHub</span></span>
* <span data-ttu-id="6295f-384">#9231 수정 - Get-AzEventHubNamespace에서 태그를 반환하지 않음</span><span class="sxs-lookup"><span data-stu-id="6295f-384">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="6295f-385">#9230 수정 - Get-AzEventHubNamespace에서 ResourceGroupName 대신 ResourceGroup을 반환함</span><span class="sxs-lookup"><span data-stu-id="6295f-385">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6295f-386">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6295f-386">Az.Network</span></span>
* <span data-ttu-id="6295f-387">Nat Gateway에 대한 ResourceId 및 InputObject 업데이트</span><span class="sxs-lookup"><span data-stu-id="6295f-387">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="6295f-388">ResourceId 및 InputObject에 대한 별칭 추가</span><span class="sxs-lookup"><span data-stu-id="6295f-388">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="6295f-389">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="6295f-389">Az.PolicyInsights</span></span>
* <span data-ttu-id="6295f-390">Get-AzPolicyEvent에서 Null 참조 문제 해결</span><span class="sxs-lookup"><span data-stu-id="6295f-390">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="6295f-391">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="6295f-391">Az.RecoveryServices</span></span>
* <span data-ttu-id="6295f-392">IaaSVM 정책 최소 보존 기간(일)이 1에서 7로 변경됨</span><span class="sxs-lookup"><span data-stu-id="6295f-392">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="6295f-393">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="6295f-393">Az.ServiceBus</span></span>
* <span data-ttu-id="6295f-394">#9182 문제 해결 - Get-AzServiceBusNamespace에서 ResourceGroupName 대신 ResourceGroup을 반환</span><span class="sxs-lookup"><span data-stu-id="6295f-394">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="6295f-395">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="6295f-395">Az.ServiceFabric</span></span>
* <span data-ttu-id="6295f-396">'Update-AzServiceFabricReliability' 오류 메시지의 오타 수정</span><span class="sxs-lookup"><span data-stu-id="6295f-396">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="6295f-397">Service Fabric 명령줄에서 누락된 문자 수정</span><span class="sxs-lookup"><span data-stu-id="6295f-397">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="6295f-398">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6295f-398">Az.Sql</span></span>
* <span data-ttu-id="6295f-399">Managed Instance에 대한 AutoDr을 지원하기 위해 New-AzureSqlInstance cmdlet에 대한 DnsZonePartner 매개 변수를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-399">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="6295f-400">Get-AzSqlDatabaseSecureConnectionPolicy cmdlet 사용 중단</span><span class="sxs-lookup"><span data-stu-id="6295f-400">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="6295f-401">Threat Detection(위협 탐지) cmdlet 이름을 Advanced Threat Protection으로 변경함</span><span class="sxs-lookup"><span data-stu-id="6295f-401">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="6295f-402">새 AzSqlInstance -StorageSizeInGB 및 -LicenseType 매개 변수는 이제 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-402">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="6295f-403">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="6295f-403">Az.Websites</span></span>
* <span data-ttu-id="6295f-404">-WebApp 속성에서 Set-AzWebApp 및 Set-AzWebAppSlot을 사용하면 태그가 제거되는 문제를 해결함</span><span class="sxs-lookup"><span data-stu-id="6295f-404">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="6295f-405">2.1.0 - 2019년 5월</span><span class="sxs-lookup"><span data-stu-id="6295f-405">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="6295f-406">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="6295f-406">Az.ApiManagement</span></span>
* <span data-ttu-id="6295f-407">글로벌 및 API 범위에서 진단을 관리하기 위한 새 cmdlet을 만들었습니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-407">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="6295f-408">**Get-AzApiManagementDiagnostic** - 글로벌 또는 API 범위가 구성된 진단 가져오기</span><span class="sxs-lookup"><span data-stu-id="6295f-408">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="6295f-409">**New-AzApiManagementDiagnostic** - 글로벌 범위 또는 API 범위에서 새 진단 만들기</span><span class="sxs-lookup"><span data-stu-id="6295f-409">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="6295f-410">**New-AzApiManagementHttpMessageDiagnostic** - 기록할 Headers(헤더) 및 Body Bytes(본문 바이트 수) 크기에 대한 진단 설정 만들기</span><span class="sxs-lookup"><span data-stu-id="6295f-410">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="6295f-411">**New-AzApiManagementPipelineDiagnosticSetting** - 게이트웨이로 들어오고 나가는 HTTP 메시지에 대한 진단 설정 만들기</span><span class="sxs-lookup"><span data-stu-id="6295f-411">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="6295f-412">**New-AzApiManagementSamplingSetting** - 진단 요청/응답에 대한 샘플링 설정 만들기</span><span class="sxs-lookup"><span data-stu-id="6295f-412">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="6295f-413">**Remove-AzApiManagementDiagnostic** - 글로벌 또는 API 범위에서 진단 엔터티 제거</span><span class="sxs-lookup"><span data-stu-id="6295f-413">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="6295f-414">**Set-AzApiManagementDiagnostic** - 글로벌 또는 API 범위에서 진단 엔터티 업데이트</span><span class="sxs-lookup"><span data-stu-id="6295f-414">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="6295f-415">ApiManagement 서비스에서 캐시를 관리하기 위한 새 cmdlet을 만들었습니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-415">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="6295f-416">**Get-AzApiManagementCache** - 식별자 또는 모든 캐시로 지정된 캐시의 세부 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="6295f-416">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="6295f-417">**New-AzApiManagementCache** - 특정 Azure 'region'(지역)에 새 'default'(기본) 캐시 만들기</span><span class="sxs-lookup"><span data-stu-id="6295f-417">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="6295f-418">**Remove-AzApiManagementCache** - 캐시 제거</span><span class="sxs-lookup"><span data-stu-id="6295f-418">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="6295f-419">**Update-AzApiManagementCache** - 캐시 업데이트</span><span class="sxs-lookup"><span data-stu-id="6295f-419">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="6295f-420">API 스키마 관리하기 위한 새 cmdlet을 만들었습니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-420">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="6295f-421">**New-AzApiManagementSchema** - API에 대한 새 스키마 만들기</span><span class="sxs-lookup"><span data-stu-id="6295f-421">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="6295f-422">**Get-AzApiManagementSchema** - API에 구성된 스키마 가져오기</span><span class="sxs-lookup"><span data-stu-id="6295f-422">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="6295f-423">**Remove-AzApiManagementSchema** - API에 구성된 스키마 제거</span><span class="sxs-lookup"><span data-stu-id="6295f-423">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="6295f-424">**Set-AzApiManagementSchema** - API에 구성된 스키마 업데이트</span><span class="sxs-lookup"><span data-stu-id="6295f-424">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="6295f-425">사용자 토큰을 생성하기 위한 새 cmdlet을 만들었습니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-425">Created new Cmdlet for generating a User Token.</span></span> 
    - <span data-ttu-id="6295f-426">**New-AzApiManagementUserToken** - 기본적으로 8시간 동안 유효한 새 사용자 토큰을 생성합니다. 'GIT' 사용자에 대한 토큰은 이 cmdlet을 사용하여 생성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-426">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="6295f-427">네트워크 상태를 검색하기 위한 새 cmdlet을 만들었습니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-427">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="6295f-428">**Get-AzApiManagementNetworkStatus** - API Management 서비스에서 사용하는 리소스의 네트워크 상태 연결을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-428">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="6295f-429">ApiManagement 서비스를 가상 네트워크에 배포하고 종속성이 손상되었는지 여부를 확인할 때 유용합니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-429">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="6295f-430">**New-AzApiManagement** cmdlet에서 ApiManagement 서비스를 관리하도록 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-430">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span> 
    - <span data-ttu-id="6295f-431">새 '소비' SKU 지원이 추가됨</span><span class="sxs-lookup"><span data-stu-id="6295f-431">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="6295f-432">'소비' SKU에 대해 'EnableClientCertificate' 플래그를 설정하기 위한 지원이 추가됨</span><span class="sxs-lookup"><span data-stu-id="6295f-432">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="6295f-433">새 **New-AzApiManagementSslSetting** cmdlet을 사용하면 'Backend(백 엔드)' 및 'Frontend'(프런트 엔드)에서 'TLS/SSL' 설정을 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-433">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="6295f-434">또한 ApiManagement 서비스의 'Frontend'에서 '3DES'와 같은 'Ciphers'와 'Http2'와 같은 'ServerProtocols'를 구성하는 데 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-434">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="6295f-435">ApiManagement 서비스에서 'DeveloperPortal' 호스트 이름을 구성하기 위한 지원이 추가됨</span><span class="sxs-lookup"><span data-stu-id="6295f-435">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="6295f-436">**Get-AzApiManagementSsoToken** cmdlet에서 'PsApiManagement' 개체를 입력으로 사용하도록 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-436">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="6295f-437">cmdlet에서 오류 메시지를 인라인으로 표시하도록 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-437">Updated the cmdlet to display Error Messages inline</span></span> 
     > <span data-ttu-id="6295f-438">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : 오류 코드: ValidationError 오류 메시지: 하나 이상의 필드에 잘못된 값이 있습니다. 오류 세부 정보:    [Code=ValidationError, Message=줄 3, 열 10의 'log-to-eventhub' 요소에 오류가 있습니다.: 로거를 찾지 못함, Target=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="6295f-438">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="6295f-439">**Export-AzApiManagementApi** cmdlet에서 API를 'OpenApi 3.0' 형식으로 내보내도록 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-439">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="6295f-440">**Import-AzApiManagementApi** cmdlet을 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-440">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="6295f-441">'OpenApi 3.0' 문서 사양에서 API 가져오기</span><span class="sxs-lookup"><span data-stu-id="6295f-441">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="6295f-442">문서('Swagger', 'Wadl', 'Wsdl', 'OpenApi')에 지정된 'PsApiManagementSchema' 속성 재정의</span><span class="sxs-lookup"><span data-stu-id="6295f-442">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="6295f-443">문서에 지정된 'ServiceUrl' 속성 재정의</span><span class="sxs-lookup"><span data-stu-id="6295f-443">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="6295f-444">**Get-AzApiManagementPolicy** cmdlet에서 'rawxml'을 사용하여 이스케이프된 비 Xml 'format'(형식)의 정책을 반환하도록 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-444">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="6295f-445">**Set-AzApiManagementPolicy** cmdlet에서 'rawxml'을 사용하여 이스케이프된 비 Xml 'format'의 정책을 수락하고, 'xml'을 사용하여 이스케이프된 Xml 'format'의 정책을 수락하도록 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-445">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="6295f-446">**New-AzApiManagementApi** cmdlet을 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-446">Updated cmdlet **New-AzApiManagementApi**</span></span> 
    - <span data-ttu-id="6295f-447">'OpenId' 권한 부여 서버를 사용하여 API 구성</span><span class="sxs-lookup"><span data-stu-id="6295f-447">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="6295f-448">'ApiVersionSet'에서 API 만들기</span><span class="sxs-lookup"><span data-stu-id="6295f-448">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="6295f-449">'SourceApiId' 및 'SourceApiRevision'을 사용하여 API 복제</span><span class="sxs-lookup"><span data-stu-id="6295f-449">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="6295f-450">API 범위에서 'SubscriptionRequired' 구성 가능</span><span class="sxs-lookup"><span data-stu-id="6295f-450">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="6295f-451">**Set-AzApiManagementApi** cmdlet을 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-451">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="6295f-452">'OpenId' 권한 부여 서버를 사용하여 API 구성</span><span class="sxs-lookup"><span data-stu-id="6295f-452">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="6295f-453">API를 'ApiVersionSet'으로 업데이트</span><span class="sxs-lookup"><span data-stu-id="6295f-453">To updated an API into an 'ApiVersionSet'</span></span>    
    - <span data-ttu-id="6295f-454">API 범위에서 'SubscriptionRequired' 구성 가능</span><span class="sxs-lookup"><span data-stu-id="6295f-454">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="6295f-455">**New-AzApiManagementRevision** cmdlet을 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-455">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="6295f-456">'SourceApiRevision'을 사용하여 기존 수정 버전 복제(태그, 제품, 작업 및 정책 복사).</span><span class="sxs-lookup"><span data-stu-id="6295f-456">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="6295f-457">새 수정 버전은 부모의 'ApiId'를 가정합니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-457">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="6295f-458">'ApiRevisionDescription' 제공</span><span class="sxs-lookup"><span data-stu-id="6295f-458">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="6295f-459">API 복제 시 'ServiceUrl' 재정의</span><span class="sxs-lookup"><span data-stu-id="6295f-459">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="6295f-460">**New-AzApiManagementIdentityProvider** cmdlet을 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-460">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="6295f-461">'Authority'를 사용하여 'AAD' 또는 'AADB2C' 구성</span><span class="sxs-lookup"><span data-stu-id="6295f-461">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="6295f-462">'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' 및 'PasswordResetPolicy' 설정</span><span class="sxs-lookup"><span data-stu-id="6295f-462">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="6295f-463">**New-AzApiManagementSubscription** cmdlet을 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-463">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="6295f-464">'Scope' 및 'UserId'를 사용하여 새 SubscriptonModel 설명</span><span class="sxs-lookup"><span data-stu-id="6295f-464">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="6295f-465">'ProductId' 및 'UserId'를 사용하여 이전 구독 모델 설명</span><span class="sxs-lookup"><span data-stu-id="6295f-465">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="6295f-466">구독 수준에서 'AllowTracing'을 사용하도록 설정하는 지원 추가</span><span class="sxs-lookup"><span data-stu-id="6295f-466">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="6295f-467">**Set-AzApiManagementSubscription** cmdlet을 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-467">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="6295f-468">'Scope' 및 'UserId'를 사용하여 새 SubscriptonModel 설명</span><span class="sxs-lookup"><span data-stu-id="6295f-468">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="6295f-469">'ProductId' 및 'UserId'를 사용하여 이전 구독 모델 설명</span><span class="sxs-lookup"><span data-stu-id="6295f-469">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="6295f-470">구독 수준에서 'AllowTracing'을 사용하도록 설정하는 지원 추가</span><span class="sxs-lookup"><span data-stu-id="6295f-470">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="6295f-471">다음 cmdlet에서 'ResourceId'를 입력으로 수락하도록 업데이트했습니다</span><span class="sxs-lookup"><span data-stu-id="6295f-471">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="6295f-472">'New-AzApiManagementContext'</span><span class="sxs-lookup"><span data-stu-id="6295f-472">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="6295f-473">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="6295f-473">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="6295f-474">'Get-AzApiManagementApiRelease'</span><span class="sxs-lookup"><span data-stu-id="6295f-474">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="6295f-475">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="6295f-475">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="6295f-476">'Get-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="6295f-476">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="6295f-477">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="6295f-477">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="6295f-478">'Get-AzApiManagementAuthorizationServer'</span><span class="sxs-lookup"><span data-stu-id="6295f-478">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="6295f-479">'Get-AzApiManagementBackend'</span><span class="sxs-lookup"><span data-stu-id="6295f-479">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="6295f-480">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="6295f-480">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="6295f-481">'Get-AzApiManagementCertificate'</span><span class="sxs-lookup"><span data-stu-id="6295f-481">'Get-AzApiManagementCertificate'</span></span> 
    - <span data-ttu-id="6295f-482">'Remove-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="6295f-482">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="6295f-483">'Remove-AzApiManagementSubscription'</span><span class="sxs-lookup"><span data-stu-id="6295f-483">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="6295f-484">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="6295f-484">Az.Automation</span></span>
* <span data-ttu-id="6295f-485">Get-AzAutomationJobOutputRecord에서 JSON 및 Text 레코드 값을 처리하도록 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-485">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="6295f-486">문제 https://github.com/Azure/azure-powershell/issues/7977 수정</span><span class="sxs-lookup"><span data-stu-id="6295f-486">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="6295f-487">문제 https://github.com/Azure/azure-powershell/issues/8600 수정</span><span class="sxs-lookup"><span data-stu-id="6295f-487">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="6295f-488">Start-AzAutomationDscCompilationJob에서 완료될 때까지 기다리지 않고 작업을 바로 시작하도록 변경했습니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-488">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="6295f-489">문제 https://github.com/Azure/azure-powershell/issues/8347 수정</span><span class="sxs-lookup"><span data-stu-id="6295f-489">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="6295f-490">-Name을 사용하면 모든 노드를 반환하는 Get-AzAutomationDscNode 수정.</span><span class="sxs-lookup"><span data-stu-id="6295f-490">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="6295f-491">이제 일치하는 노드만 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-491">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6295f-492">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6295f-492">Az.Compute</span></span>
* <span data-ttu-id="6295f-493">ProtectFromScaleIn 및 ProtectFromScaleSetAction 매개 변수를 Update-AzVmssVM cmdlet에 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-493">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="6295f-494">'East US'(미국 동부)가 지원되지 않는 경우 이제 New-AzVM wimple 매개 변수 집합에서 기본적으로 사용 가능한 위치를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-494">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="6295f-495">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="6295f-495">Az.DataLakeStore</span></span>
* <span data-ttu-id="6295f-496">ADLS SDK에서 httpclient를 사용하도록 업데이트하고, 데이터 평면 테스트를 Azure 프레임워크와 통합합니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-496">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="6295f-497">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="6295f-497">Az.Monitor</span></span>
* <span data-ttu-id="6295f-498">도움말 예제에서 잘못된 매개 변수 이름을 수정했습니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-498">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6295f-499">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6295f-499">Az.Network</span></span>
* <span data-ttu-id="6295f-500">DisableBgpRoutePropagation 플래그를 유효 경로 테이블 출력에 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-500">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="6295f-501">업데이트된 cmdlet:</span><span class="sxs-lookup"><span data-stu-id="6295f-501">Updated cmdlet:</span></span>
        - <span data-ttu-id="6295f-502">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="6295f-502">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="6295f-503">New-AzApplicationGatewayTrustedRootCertificate 설명서에서 이중 파선을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-503">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="6295f-504">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6295f-504">Az.Resources</span></span>
* <span data-ttu-id="6295f-505">할당 거부를 검색하기 위한 새 Get-AzureRmDenyAssignment cmdlet을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-505">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="6295f-506">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6295f-506">Az.Sql</span></span>
* <span data-ttu-id="6295f-507">Advanced Threat Protection cmdlet의 이름을 Advanced Data Security로 변경하고, 취약성 평가를 기본적으로 사용하도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-507">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="6295f-508">2.0.0 - 2019년 5월</span><span class="sxs-lookup"><span data-stu-id="6295f-508">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="6295f-509">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6295f-509">Az.Accounts</span></span>
* <span data-ttu-id="6295f-510">사용자 이름/비밀번호 인증을 사용하여 ADFS 문제를 해결하도록 인증 라이브러리 업데이트</span><span class="sxs-lookup"><span data-stu-id="6295f-510">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="6295f-511">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="6295f-511">Az.CognitiveServices</span></span>
* <span data-ttu-id="6295f-512">Bing Search 서비스에 대해서만 Bing 면책 조항을 표시하세요.</span><span class="sxs-lookup"><span data-stu-id="6295f-512">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="6295f-513">계정 생성 실패 시 오류 개선.</span><span class="sxs-lookup"><span data-stu-id="6295f-513">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6295f-514">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6295f-514">Az.Compute</span></span>
* <span data-ttu-id="6295f-515">근접 배치 그룹 기능</span><span class="sxs-lookup"><span data-stu-id="6295f-515">Proximity placement group feature.</span></span>
    - <span data-ttu-id="6295f-516">다음과 같은 새 cmdlet을 추가했습니다.   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="6295f-516">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="6295f-517">새 매개 변수 ProximityPlacementGroupId가 다음 cmdlet에 추가됩니다.   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="6295f-517">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="6295f-518">New-AzGalleryImageVersion에 StorageAccountType 매개 변수가 추가됩니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-518">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="6295f-519">New-AzGalleryImageVersion의 TargetRegion이 StorageAccountType를 포함할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-519">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="6295f-520">SkipShutdown 스위치 매개 변수가 Stop-AzVM 및 Stop-AzVmss에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-520">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>       
* <span data-ttu-id="6295f-521">주요 변경 내용</span><span class="sxs-lookup"><span data-stu-id="6295f-521">Breaking changes</span></span>
    - <span data-ttu-id="6295f-522">Set-AzVMBootDiagnostics이 Set-AzVMBootDiagnostic으로 변경됩니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-522">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="6295f-523">Export-AzLogAnalyticThrottledRequests이 Export-AzLogAnalyticThrottledRequests로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-523">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="6295f-524">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="6295f-524">Az.DeploymentManager</span></span>
* <span data-ttu-id="6295f-525">Azure 배포 관리자 cmdlet의 일반적으로 사용 가능한 첫 번째 릴리스</span><span class="sxs-lookup"><span data-stu-id="6295f-525">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="6295f-526">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="6295f-526">Az.Dns</span></span>
* <span data-ttu-id="6295f-527">자동 DNS 이름 서버 위임</span><span class="sxs-lookup"><span data-stu-id="6295f-527">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="6295f-528">DNS 영역 만들기 cmdlet은 추가 선택적 매개 변수로 부모 영역 이름을 허용합니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-528">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="6295f-529">새로 생성 된 자식 영역의 부모 영역에 NS 레코드를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-529">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="6295f-530">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="6295f-530">Az.FrontDoor</span></span>
* <span data-ttu-id="6295f-531">Azure FrontDoor cmdlet의 일반적으로 사용 가능한 첫 번째 릴리스</span><span class="sxs-lookup"><span data-stu-id="6295f-531">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="6295f-532">'Waf'를 포함하도록 WAF cmdlet의 이름 바꾸기</span><span class="sxs-lookup"><span data-stu-id="6295f-532">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="6295f-533">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="6295f-533">Az.HDInsight</span></span>
* <span data-ttu-id="6295f-534">두 개의 cmdlet을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-534">Removed two cmdlets:</span></span>
    - <span data-ttu-id="6295f-535">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="6295f-535">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="6295f-536">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="6295f-536">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="6295f-537">Grant-AzHDInsightHttpServicesAccess를 대체할 새 cmdlet Set-AzHDInsightGatewayCredential을 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-537">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="6295f-538">reader 역할과 HDInsight 운영자 역할을 구분하도록 cmdlet Get-AzHDInsightJobOutput 업데이트:</span><span class="sxs-lookup"><span data-stu-id="6295f-538">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="6295f-539">reader 역할을 가진 사용자는 'DefaultStorageAccountKey'매개 변수를 명시적으로 지정해야 합니다. 그렇지 않으면 오류가 발생합니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-539">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="6295f-540">Hdinsight 운영자 역할을 가진 사용자를 영향을 받지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-540">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="6295f-541">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="6295f-541">Az.Monitor</span></span>
* <span data-ttu-id="6295f-542">SQR API(예약 쿼리 규칙)용 새 cmdlet</span><span class="sxs-lookup"><span data-stu-id="6295f-542">New cmdlets for SQR API (Scheduled Query Rule)</span></span>  
    - <span data-ttu-id="6295f-543">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="6295f-543">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="6295f-544">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="6295f-544">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="6295f-545">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="6295f-545">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="6295f-546">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="6295f-546">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="6295f-547">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="6295f-547">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="6295f-548">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="6295f-548">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="6295f-549">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="6295f-549">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="6295f-550">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="6295f-550">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="6295f-551">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="6295f-551">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="6295f-552">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="6295f-552">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="6295f-553">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="6295f-553">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="6295f-554">SQR API에 대한 [자세한 내용](https://docs.microsoft.com/en-us/rest/api/monitor/scheduledqueryrules)</span><span class="sxs-lookup"><span data-stu-id="6295f-554">[More](https://docs.microsoft.com/en-us/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="6295f-555">GenV2(비 클래식) 메트릭 기반 경고 규칙에 대한 cmdlet을 포함하도록 Az.Monitor.md가 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="6295f-555">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6295f-556">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6295f-556">Az.Network</span></span>
* <span data-ttu-id="6295f-557">Nat 게이트웨이 리소스에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="6295f-557">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="6295f-558">새 cmdlet</span><span class="sxs-lookup"><span data-stu-id="6295f-558">New cmdlets</span></span>
        - <span data-ttu-id="6295f-559">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="6295f-559">New-AzNatGateway</span></span>
        - <span data-ttu-id="6295f-560">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="6295f-560">Get-AzNatGateway</span></span>
        - <span data-ttu-id="6295f-561">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="6295f-561">Set-AzNatGateway</span></span>
        - <span data-ttu-id="6295f-562">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="6295f-562">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="6295f-563">다음 Cmdlet이 업데이트 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-563">Updated cmdlets</span></span>
        - <span data-ttu-id="6295f-564">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="6295f-564">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="6295f-565">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="6295f-565">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="6295f-566">기능에 대한 새로운 명령이 업데이트됨: Brooklyn Gateway에서 사용자 지정 경로 설정/제거.</span><span class="sxs-lookup"><span data-stu-id="6295f-566">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="6295f-567">New-AzVirtualNetworkGateway가 업데이트됨: 선택적 매개 변수 -CustomRoute를 추가하여 게이트웨이에서 설정할 사용자 지정 경로로 주소 접두사를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-567">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="6295f-568">Set-AzVirtualNetworkGateway가 업데이트됨: 선택적 매개 변수 -CustomRoute를 추가하여 게이트웨이에서 설정할 사용자 지정 경로로 주소 접두사를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-568">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="6295f-569">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="6295f-569">Az.PolicyInsights</span></span>
* <span data-ttu-id="6295f-570">정책 평가 세부 정보 쿼리 지원</span><span class="sxs-lookup"><span data-stu-id="6295f-570">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="6295f-571">Get-AzPolicyState에 '-Expand'매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="6295f-571">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="6295f-572">'-Expand PolicyEvaluationDetails' 지원</span><span class="sxs-lookup"><span data-stu-id="6295f-572">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="6295f-573">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="6295f-573">Az.RecoveryServices</span></span>
* <span data-ttu-id="6295f-574">크로스 구독 Azure에서 Azure 사이트 복구 지원</span><span class="sxs-lookup"><span data-stu-id="6295f-574">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="6295f-575">Azure Site Recovery에 대한 호환성이 손상되는 변경 표시</span><span class="sxs-lookup"><span data-stu-id="6295f-575">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="6295f-576">Azure Site Recovery 복구 계획 최종 실행 계획에 대한 수정</span><span class="sxs-lookup"><span data-stu-id="6295f-576">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="6295f-577">Azure에서 Azure에 대한 Azure Site Recovery 업데이트 네트워크 매핑 수정</span><span class="sxs-lookup"><span data-stu-id="6295f-577">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="6295f-578">관리 디스크에 대한 Azure에서 Azure에 대한 Azure Site Recovery 업데이트 보호 방향 수정</span><span class="sxs-lookup"><span data-stu-id="6295f-578">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="6295f-579">기타 사소한 수정.</span><span class="sxs-lookup"><span data-stu-id="6295f-579">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="6295f-580">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="6295f-580">Az.Relay</span></span>
* <span data-ttu-id="6295f-581">고객 관련 메시지의 철자 오류 수정</span><span class="sxs-lookup"><span data-stu-id="6295f-581">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="6295f-582">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="6295f-582">Az.ServiceBus</span></span>
* <span data-ttu-id="6295f-583">네임스페이스의 NetworkRuleSet에 대한 새 cmdlet가 추가되었습니다</span><span class="sxs-lookup"><span data-stu-id="6295f-583">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="6295f-584">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="6295f-584">Az.Storage</span></span>
* <span data-ttu-id="6295f-585">저장소 클라이언트 라이브러리 10.0.1로 업그레이드(이 SDK의 모든 개체의 네임스페이스가 'Microsoft.WindowsAzure.Storage. *'에서 'Microsoft.Azure.Storage.* '로 변경됨)</span><span class="sxs-lookup"><span data-stu-id="6295f-585">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="6295f-586">새로운 API 버전 2019-04-01을 지원하기 위해 Microsoft.Azure.Management.Storage 11.0.0으로 업그레이드합니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-586">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="6295f-587">스토리지 생성 계정의 기본 스토리지 계정 종류가 'Storage'에서 'StorageV2'로 변경됩니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-587">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="6295f-588">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6295f-588">New-AzStorageAccount</span></span>
* <span data-ttu-id="6295f-589">'StandardLRS'가 'Standard_LRS'로 변경되는 것과 같이 '-'을 추가하여 입력 SkuName과 정렬되도록 스토리지 계정 cmdlet 출력 Sku.Name을 변경합니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-589">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="6295f-590">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6295f-590">New-AzStorageAccount</span></span>
    - <span data-ttu-id="6295f-591">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6295f-591">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="6295f-592">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6295f-592">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="6295f-593">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="6295f-593">Az.Websites</span></span>
* <span data-ttu-id="6295f-594">Get-AzWebApp에서 반환한 PSSite 개체에 대해 'Kind'속성이 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-594">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="6295f-595">Get-AzWebApp\* 메트릭 및 Get-AzAppServicePlanMetrics가 사용되지 않음으로 표시되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-595">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="6295f-596">1.8.0 - 2019년 4월</span><span class="sxs-lookup"><span data-stu-id="6295f-596">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="6295f-597">마지막 주 릴리스 이후의 주요 사항</span><span class="sxs-lookup"><span data-stu-id="6295f-597">Highlights since the last major release</span></span>
* <span data-ttu-id="6295f-598">`Az` 모듈 일반 공급</span><span class="sxs-lookup"><span data-stu-id="6295f-598">General availability of `Az` module</span></span>
* <span data-ttu-id="6295f-599">`Az` 모듈에 대한 자세한 내용은 https://aka.ms/azps-announce 를 방문하세요.</span><span class="sxs-lookup"><span data-stu-id="6295f-599">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="6295f-600">Location, ResourceGroup 및 ResourceName 완성자가 추가되었습니다(https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/ ).</span><span class="sxs-lookup"><span data-stu-id="6295f-600">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="6295f-601">와일드카드 지원이 Az.Compute 및 Az.Network에 대한 Get cmdlet에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-601">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="6295f-602">Windows PowerShell 5.1 전용 대화형 사용자 이름/암호 인증이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-602">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="6295f-603">Python 2 Runbook 지원이 Az.Automation에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-603">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="6295f-604">Az.LogicApp: 통합 계정 어셈블리 및 일괄 처리 구성을 위한 새로운 cmdlet입니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-604">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="6295f-605">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6295f-605">Az.Accounts</span></span>
* <span data-ttu-id="6295f-606">Mac에서 모듈을 올바르게 삭제하기 위해 Uninstall-AzureRm을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-606">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="6295f-607">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="6295f-607">Az.Batch</span></span>
* <span data-ttu-id="6295f-608">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-608">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="6295f-609">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="6295f-609">Az.Cdn</span></span>
* <span data-ttu-id="6295f-610">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-610">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="6295f-611">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="6295f-611">Az.CognitiveServices</span></span>
* <span data-ttu-id="6295f-612">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-612">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6295f-613">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6295f-613">Az.Compute</span></span>
* <span data-ttu-id="6295f-614">디스크의 리소스 ID에 리소스 ID의 소문자 resourcegroups가 있는 경우 AEM 설치 문제 수정</span><span class="sxs-lookup"><span data-stu-id="6295f-614">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="6295f-615">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-615">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="6295f-616">와일드 카드에 대한 설명서 수정</span><span class="sxs-lookup"><span data-stu-id="6295f-616">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="6295f-617">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="6295f-617">Az.DataFactory</span></span>
* <span data-ttu-id="6295f-618">NodeCount가 관리형 통합 런타임에 대해 Null이 아닌 경우 SsisProperties를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-618">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="6295f-619">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="6295f-619">Az.DataLakeStore</span></span>
* <span data-ttu-id="6295f-620">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-620">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="6295f-621">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="6295f-621">Az.EventGrid</span></span>
* <span data-ttu-id="6295f-622">이벤트 구독 cmdlet 만들기/업데이트를 사용하기 전에 리소스를 만들어야 함을 나타내기 위해 엔드포인트의 도움말 텍스트가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-622">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="6295f-623">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="6295f-623">Az.EventHub</span></span>
* <span data-ttu-id="6295f-624">네임스페이스의 NetworkRuleSet에 대한 새 cmdlet가 추가되었습니다</span><span class="sxs-lookup"><span data-stu-id="6295f-624">Added new cmdlets for NetworkRuleSet of Namespace</span></span> 

#### <a name="azhdinsight"></a><span data-ttu-id="6295f-625">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="6295f-625">Az.HDInsight</span></span>
* <span data-ttu-id="6295f-626">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-626">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="6295f-627">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="6295f-627">Az.IotHub</span></span>
* <span data-ttu-id="6295f-628">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-628">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="6295f-629">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="6295f-629">Az.KeyVault</span></span>
* <span data-ttu-id="6295f-630">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-630">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="6295f-631">와일드 카드에 대한 설명서 수정</span><span class="sxs-lookup"><span data-stu-id="6295f-631">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="6295f-632">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="6295f-632">Az.MachineLearning</span></span>
* <span data-ttu-id="6295f-633">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-633">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="6295f-634">Az.Media</span><span class="sxs-lookup"><span data-stu-id="6295f-634">Az.Media</span></span>
* <span data-ttu-id="6295f-635">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-635">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="6295f-636">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="6295f-636">Az.Monitor</span></span>
  * <span data-ttu-id="6295f-637">GenV2(비 클래식) 메트릭 기반 경고 규칙에 대한 새 cmdlet</span><span class="sxs-lookup"><span data-stu-id="6295f-637">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="6295f-638">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="6295f-638">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="6295f-639">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="6295f-639">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="6295f-640">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="6295f-640">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="6295f-641">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="6295f-641">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="6295f-642">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="6295f-642">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="6295f-643">모니터 SDK가 버전 0.22.0-preview로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-643">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6295f-644">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6295f-644">Az.Network</span></span>
* <span data-ttu-id="6295f-645">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-645">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="6295f-646">와일드 카드에 대한 설명서 수정</span><span class="sxs-lookup"><span data-stu-id="6295f-646">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="6295f-647">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="6295f-647">Az.NotificationHubs</span></span>
* <span data-ttu-id="6295f-648">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-648">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="6295f-649">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="6295f-649">Az.OperationalInsights</span></span>
* <span data-ttu-id="6295f-650">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-650">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="6295f-651">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="6295f-651">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="6295f-652">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-652">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="6295f-653">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="6295f-653">Az.RecoveryServices</span></span>
* <span data-ttu-id="6295f-654">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-654">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="6295f-655">Azure VM의 SQL용 테이블 형식이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-655">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="6295f-656">AzureFileShare에서 위치를 가져오는 대체 메서드가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-656">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="6295f-657">시간대에 따라 SchedulePolicy 개체의 ScheduleRunDays가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-657">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="6295f-658">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="6295f-658">Az.RedisCache</span></span>
* <span data-ttu-id="6295f-659">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-659">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="6295f-660">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6295f-660">Az.Resources</span></span>
* <span data-ttu-id="6295f-661">와일드 카드에 대한 설명서 수정</span><span class="sxs-lookup"><span data-stu-id="6295f-661">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="6295f-662">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6295f-662">Az.Sql</span></span>
* <span data-ttu-id="6295f-663">Monitor SDK의 종속성을 공용 코드로 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-663">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="6295f-664">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-664">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="6295f-665">다중 열 분류 프로세스가 향상되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-665">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="6295f-666">기본적으로 Get-AzSqlServerServiceObjective의 응답으로 SKU 속성(SKU 이름, 제품군, 용량)과 테이블 형식을 포함합니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-666">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="6295f-667">해당 지역에 기존 서버 없이 위치별로 Get-AzSqlServerServiceObjective를 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-667">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="6295f-668">관리형 인스턴스 생성 시 표준 시간대 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-668">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="6295f-669">와일드 카드에 대한 설명서 수정</span><span class="sxs-lookup"><span data-stu-id="6295f-669">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="6295f-670">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="6295f-670">Az.Websites</span></span>
* <span data-ttu-id="6295f-671">실행 시 태그를 제거하지 않도록 Set-AzWebApp 및 Set-AzWebAppSlot를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-671">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="6295f-672">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-672">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="6295f-673">WebSites SDK가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-673">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="6295f-674">PSAppServicePlan에서 AdminSiteName 속성을 제거했습니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-674">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="6295f-675">1.7.0 - 2019년 4월</span><span class="sxs-lookup"><span data-stu-id="6295f-675">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="6295f-676">마지막 주 릴리스 이후의 주요 사항</span><span class="sxs-lookup"><span data-stu-id="6295f-676">Highlights since the last major release</span></span>
* <span data-ttu-id="6295f-677">`Az` 모듈 일반 공급</span><span class="sxs-lookup"><span data-stu-id="6295f-677">General availability of `Az` module</span></span>
* <span data-ttu-id="6295f-678">`Az` 모듈에 대한 자세한 내용은 https://aka.ms/azps-announce 를 방문하세요.</span><span class="sxs-lookup"><span data-stu-id="6295f-678">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="6295f-679">Location, ResourceGroup 및 ResourceName 완성자가 추가되었습니다(https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/ ).</span><span class="sxs-lookup"><span data-stu-id="6295f-679">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="6295f-680">와일드카드 지원이 Az.Compute 및 Az.Network에 대한 Get cmdlet에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-680">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="6295f-681">Windows PowerShell 5.1 전용 대화형 사용자 이름/암호 인증이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-681">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="6295f-682">Python 2 Runbook 지원이 Az.Automation에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-682">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="6295f-683">Az.LogicApp: 통합 계정 어셈블리 및 일괄 처리 구성을 위한 새로운 cmdlet입니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-683">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="6295f-684">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6295f-684">Az.Accounts</span></span>
* <span data-ttu-id="6295f-685">매개 변수 AzureAnalysisServicesEndpointResourceId를 허용하도록 Add-AzEnvironment 및 Set-AzEnvironment 업데이트</span><span class="sxs-lookup"><span data-stu-id="6295f-685">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="6295f-686">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="6295f-686">Az.AnalysisServices</span></span>
* <span data-ttu-id="6295f-687">데이터 평면 cmdlet에서 ServiceClient 사용 및 원본 인증 논리 제거</span><span class="sxs-lookup"><span data-stu-id="6295f-687">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="6295f-688">호환성이 손상되는 변경을 방지하기 위해 Add-AzureASAccount를 Connect-AzAccount의 래퍼로 만듦</span><span class="sxs-lookup"><span data-stu-id="6295f-688">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="6295f-689">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="6295f-689">Az.Automation</span></span>
* <span data-ttu-id="6295f-690">포함에 대한 New-AzAutomationSoftwareUpdateConfiguration cmdlet 버그 수정</span><span class="sxs-lookup"><span data-stu-id="6295f-690">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="6295f-691">이제 매개 변수 IncludedKbNumber 및 IncludedPackageNameMask가 작동함</span><span class="sxs-lookup"><span data-stu-id="6295f-691">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="6295f-692">Azure 자동화 업데이트 관리 동적 그룹에 대한 버그 수정</span><span class="sxs-lookup"><span data-stu-id="6295f-692">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6295f-693">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6295f-693">Az.Compute</span></span>
* <span data-ttu-id="6295f-694">New-AzDiskConfig 및 New-AzSnapshotConfig에 HyperVGeneration 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="6295f-694">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="6295f-695">다른 테넌트의 갤러리 이미지를 사용하여 VM을 만들 수 있음</span><span class="sxs-lookup"><span data-stu-id="6295f-695">Allow VM creation with galley image from other tenants.</span></span> 

#### <a name="azcontainerinstance"></a><span data-ttu-id="6295f-696">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="6295f-696">Az.ContainerInstance</span></span>
* <span data-ttu-id="6295f-697">후행 빈 인수를 추가한 New-AzContainerGroup의 -Command 매개 변수의 문제 수정</span><span class="sxs-lookup"><span data-stu-id="6295f-697">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="6295f-698">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="6295f-698">Az.DataFactory</span></span>
* <span data-ttu-id="6295f-699">ADF .Net SDK 버전을 3.0.2로 업데이트</span><span class="sxs-lookup"><span data-stu-id="6295f-699">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="6295f-700">RepoConfiguration 관련 설정에 대한 추가 매개 변수로 Set-AzDataFactoryV2 cmdlet을 업데이트</span><span class="sxs-lookup"><span data-stu-id="6295f-700">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="6295f-701">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6295f-701">Az.Resources</span></span>
* <span data-ttu-id="6295f-702">'-ResourceId' 또는 '-ResourceGroupName', '-Name' 및 '-ResourceType' 매개 변수를 제공할 때 'Get-AzResource'에 대한 공급자 처리 개선</span><span class="sxs-lookup"><span data-stu-id="6295f-702">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="6295f-703">'Test-AzDeployment' 및 'Test-AzResourceGroupDeployment'에 대한 오류 처리 개선</span><span class="sxs-lookup"><span data-stu-id="6295f-703">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="6295f-704">배포 유효성 검사 외부에서 발생한 오류를 처리하고 그 대신 명령의 출력에 포함</span><span class="sxs-lookup"><span data-stu-id="6295f-704">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="6295f-705">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/6856 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="6295f-705">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="6295f-706">배포 cmdlet 세트에 스크립트 및 작업 시나리오에서 프롬프트를 건너뛰는 '-IgnoreDynamicParameters' 스위치 추가</span><span class="sxs-lookup"><span data-stu-id="6295f-706">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="6295f-707">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/6856 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="6295f-707">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="6295f-708">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6295f-708">Az.Sql</span></span>
* <span data-ttu-id="6295f-709">데이터베이스 데이터 분류 지원</span><span class="sxs-lookup"><span data-stu-id="6295f-709">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="6295f-710">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="6295f-710">Az.Storage</span></span>
* <span data-ttu-id="6295f-711">매개 변수 -UseConnectedAccount를 사용하여 스토리지 컨텍스트를 만들 때 자세한 오류 보고(단, 로그인 Azure 계정 없이)</span><span class="sxs-lookup"><span data-stu-id="6295f-711">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="6295f-712">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="6295f-712">New-AzStorageContext</span></span>
* <span data-ttu-id="6295f-713">관리 평면 API를 사용하여 지정한 스토리지 계정의 BLOB 서비스 속성 관리 지원</span><span class="sxs-lookup"><span data-stu-id="6295f-713">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="6295f-714">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="6295f-714">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="6295f-715">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="6295f-715">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="6295f-716">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="6295f-716">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="6295f-717">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="6295f-717">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="6295f-718">BLOB 및 파일 업로드/다운로드 cmdlet에 대한 -AsJob 지원</span><span class="sxs-lookup"><span data-stu-id="6295f-718">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="6295f-719">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="6295f-719">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="6295f-720">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="6295f-720">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="6295f-721">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="6295f-721">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="6295f-722">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="6295f-722">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="6295f-723">1.6.0 - 2019년 3월</span><span class="sxs-lookup"><span data-stu-id="6295f-723">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="6295f-724">마지막 주 릴리스 이후의 주요 사항</span><span class="sxs-lookup"><span data-stu-id="6295f-724">Highlights since the last major release</span></span>
* <span data-ttu-id="6295f-725">`Az` 모듈 일반 공급</span><span class="sxs-lookup"><span data-stu-id="6295f-725">General availability of `Az` module</span></span>
* <span data-ttu-id="6295f-726">`Az` 모듈에 대한 자세한 내용은 https://aka.ms/azps-announce 를 방문하세요.</span><span class="sxs-lookup"><span data-stu-id="6295f-726">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="6295f-727">Location, ResourceGroup 및 ResourceName 완성자가 추가되었습니다(https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/ ).</span><span class="sxs-lookup"><span data-stu-id="6295f-727">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="6295f-728">와일드카드 지원이 Az.Compute 및 Az.Network에 대한 Get cmdlet에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-728">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="6295f-729">Windows PowerShell 5.1 전용 대화형 사용자 이름/암호 인증이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-729">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="6295f-730">Python 2 Runbook 지원이 Az.Automation에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-730">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="6295f-731">Az.LogicApp: 통합 계정 어셈블리 및 일괄 처리 구성을 위한 새로운 cmdlet입니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-731">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="6295f-732">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="6295f-732">Az.Automation</span></span>
* <span data-ttu-id="6295f-733">Azure 자동화 업데이트 관리에서 변경된 지원 기능은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-733">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="6295f-734">동적 그룹화</span><span class="sxs-lookup"><span data-stu-id="6295f-734">Dynamic grouping</span></span>
    * <span data-ttu-id="6295f-735">사전 스크립트</span><span class="sxs-lookup"><span data-stu-id="6295f-735">Pre-Post script</span></span>
    * <span data-ttu-id="6295f-736">다시 부팅 설정</span><span class="sxs-lookup"><span data-stu-id="6295f-736">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6295f-737">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6295f-737">Az.Compute</span></span>
* <span data-ttu-id="6295f-738">Get-AzVmBootDiagnosticsData의 경로 확인 문제가 해결되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-738">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="6295f-739">Compute 클라이언트 라이브러리가 25.0.0으로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-739">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="6295f-740">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="6295f-740">Az.KeyVault</span></span>
* <span data-ttu-id="6295f-741">와일드카드 지원이 KeyVault cmdlet에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-741">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6295f-742">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6295f-742">Az.Network</span></span>
* <span data-ttu-id="6295f-743">Azure Firewall에 대한 위협 인텔리전스 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-743">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="6295f-744">Application Gateway 방화벽 정책의 최상위 수준 리소스 및 사용자 지정 규칙이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-744">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="6295f-745">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="6295f-745">Az.RecoveryServices</span></span>
* <span data-ttu-id="6295f-746">인스턴트 RP를 지원하기 위해 SnapshotRetentionInDays가 Azure VM 정책에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-746">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="6295f-747">컨테이너 등록을 취소하는 파이프 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-747">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="6295f-748">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6295f-748">Az.Resources</span></span>
* <span data-ttu-id="6295f-749">Get-AzResource 및 Get-AzResourceGroup에 대한 와일드카드 지원을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-749">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="6295f-750">ARM에 대한 일반 호출을 수행할 때 사용되는 자격 증명을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-750">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="6295f-751">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6295f-751">Az.Sql</span></span>
* <span data-ttu-id="6295f-752">위협 탐지의 cmdlet 매개 변수(ExcludeDetectionType)가 DetectionType에서 string[]으로 변경되어 새 DetectionType이 추가되면 이후의 증명이 되고 자동 완성도 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-752">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="6295f-753">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="6295f-753">Az.Storage</span></span>
* <span data-ttu-id="6295f-754">스토리지 계정에 대한 관리 정책 가져오기/설정/제거를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-754">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="6295f-755">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="6295f-755">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="6295f-756">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="6295f-756">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="6295f-757">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="6295f-757">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="6295f-758">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="6295f-758">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="6295f-759">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="6295f-759">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="6295f-760">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="6295f-760">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="6295f-761">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="6295f-761">Az.Websites</span></span>
* <span data-ttu-id="6295f-762">'New-AzWebApp -IncludeSourceWebAppSlots'를 사용하여 모든 슬롯의 복제를 중단하는 ARM 템플릿 버그가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-762">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span> 

## <a name="150---march-2019"></a><span data-ttu-id="6295f-763">1.5.0 - 2019년 3월</span><span class="sxs-lookup"><span data-stu-id="6295f-763">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="6295f-764">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6295f-764">Az.Accounts</span></span>
* <span data-ttu-id="6295f-765">'Register-AzModule' 명령을 추가하여 AutoRest 생성 cmdlet을 지원</span><span class="sxs-lookup"><span data-stu-id="6295f-765">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="6295f-766">Connect-AzAccount 예제 업데이트</span><span class="sxs-lookup"><span data-stu-id="6295f-766">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="6295f-767">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="6295f-767">Az.Automation</span></span>
* <span data-ttu-id="6295f-768">몇몇 Azure Automation cmdlet에서 특정 월별 일정을 검색할 때 발생하는 문제 수정</span><span class="sxs-lookup"><span data-stu-id="6295f-768">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="6295f-769">상위 20개 노드를 반환하도록 Get-AzAutomationDscNode를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-769">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="6295f-770">이제 모든 노드 반환</span><span class="sxs-lookup"><span data-stu-id="6295f-770">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="6295f-771">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="6295f-771">Az.Cdn</span></span>
* <span data-ttu-id="6295f-772">사용자 지정 도메인 Https 사용/사용 안 함에 대한 새 Powershell cmdlet이 추가되었으며 기존의 것은 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-772">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6295f-773">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6295f-773">Az.Compute</span></span>
* <span data-ttu-id="6295f-774">Get cmdlet에 와일드 카드 지원 추가</span><span class="sxs-lookup"><span data-stu-id="6295f-774">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="6295f-775">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="6295f-775">Az.DataFactory</span></span>
* <span data-ttu-id="6295f-776">ADF.Net SDK 버전이 3.0.1로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-776">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="6295f-777">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="6295f-777">Az.LogicApp</span></span>
* <span data-ttu-id="6295f-778">첫 결과 페이지 검색 시에만 ListWorkflows 수정</span><span class="sxs-lookup"><span data-stu-id="6295f-778">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6295f-779">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6295f-779">Az.Network</span></span>
* <span data-ttu-id="6295f-780">Network cmdlet에 와일드 카드 지원 추가</span><span class="sxs-lookup"><span data-stu-id="6295f-780">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="6295f-781">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="6295f-781">Az.RecoveryServices</span></span>
* <span data-ttu-id="6295f-782">Azure VM 지원에 SQL 서버가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-782">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="6295f-783">SDK 업데이트</span><span class="sxs-lookup"><span data-stu-id="6295f-783">SDK Update</span></span>
* <span data-ttu-id="6295f-784">VMappContainer 체크 인 Get-ProtectableItem 제거</span><span class="sxs-lookup"><span data-stu-id="6295f-784">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="6295f-785">Get ProtectableItem의 매개 변수로 Name과 ServerName이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-785">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="6295f-786">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6295f-786">Az.Resources</span></span>
* <span data-ttu-id="6295f-787">`-TemplateObject` 매개 변수를 추가하여 cmdlet을 배포</span><span class="sxs-lookup"><span data-stu-id="6295f-787">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="6295f-788">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/2933 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="6295f-788">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="6295f-789">`Get-AzResource`의 결과를 `Set-AzResource`(으)로 파이프할 때 발생하는 문제 수정</span><span class="sxs-lookup"><span data-stu-id="6295f-789">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="6295f-790">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/8240 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="6295f-790">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="6295f-791">실행 시 JSON 데이터 형식 문제 해결 `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="6295f-791">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="6295f-792">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/7930 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="6295f-792">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="6295f-793">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6295f-793">Az.Sql</span></span>
* <span data-ttu-id="6295f-794">AuditingEndpointsCommunicator를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-794">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="6295f-795">새 진단 설정을 생성할 때 에지 사례의 동작을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-795">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="6295f-796">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="6295f-796">Az.Storage</span></span>
* <span data-ttu-id="6295f-797">스토리지 계정      - New-AzStorageAccount를 생성할 때 종류 BlockBlobStorage를 지원</span><span class="sxs-lookup"><span data-stu-id="6295f-797">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="6295f-798">1.4.0 - 2019년 2월</span><span class="sxs-lookup"><span data-stu-id="6295f-798">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="6295f-799">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="6295f-799">Az.AnalysisServices</span></span>
* <span data-ttu-id="6295f-800">사용되지 않는 AddAzureASAccount cmdlet</span><span class="sxs-lookup"><span data-stu-id="6295f-800">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="6295f-801">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="6295f-801">Az.Automation</span></span>
* <span data-ttu-id="6295f-802">Import-AzAutomationDscNodeConfiguration 도움말 업데이트</span><span class="sxs-lookup"><span data-stu-id="6295f-802">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="6295f-803">Import-AzAutomationDscConfiguration cmdlet 구성 이름 유효성 검사 추가</span><span class="sxs-lookup"><span data-stu-id="6295f-803">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="6295f-804">Import-AzAutomationDscConfiguration cmdlet 오류 처리 개선</span><span class="sxs-lookup"><span data-stu-id="6295f-804">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="6295f-805">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="6295f-805">Az.CognitiveServices</span></span>
* <span data-ttu-id="6295f-806">리소스의 하위 도메인을 지정하는 데 사용되는 New-AzCognitiveServicesAccount에 대한 새 선택적 매개 변수로 CustomSubdomainName이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-806">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6295f-807">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6295f-807">Az.Compute</span></span>
* <span data-ttu-id="6295f-808">ID 매개 변수 집합 문제 해결</span><span class="sxs-lookup"><span data-stu-id="6295f-808">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="6295f-809">Name 매개 변수를 제공하지 않으면 Get-AzVMExtension이 설치된 모든 확장을 열거하도록 업데이트</span><span class="sxs-lookup"><span data-stu-id="6295f-809">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="6295f-810">Update-AzImage cmdlet에 태그 및 ResourceId 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="6295f-810">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="6295f-811">인스턴스 ID가 없는 Get-AzVmssVM과 InstanceView를 사용하면 인스턴스 보기가 있는 VMSS VM을 나열할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-811">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="6295f-812">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="6295f-812">Az.DataLakeStore</span></span>
* <span data-ttu-id="6295f-813">ADL 삭제된 항목 열거 및 복원에 대한 cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="6295f-813">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="6295f-814">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="6295f-814">Az.EventHub</span></span>
* <span data-ttu-id="6295f-815">Eventhub의 CaptureDescription 클래스에서 빈 보관을 건너뛰는 새 부울 속성 SkipEmptyArchives가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-815">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span> 

#### <a name="azkeyvault"></a><span data-ttu-id="6295f-816">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="6295f-816">Az.KeyVault</span></span>
* <span data-ttu-id="6295f-817">Set-AzKeyVaultSecret 태그 지정 수정</span><span class="sxs-lookup"><span data-stu-id="6295f-817">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="6295f-818">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="6295f-818">Az.LogicApp</span></span>
* <span data-ttu-id="6295f-819">통합 계정에 대한 기본 sku 추가</span><span class="sxs-lookup"><span data-stu-id="6295f-819">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="6295f-820">XSLT 2.0, XSLT 3.0, Liquid 맵 형식 추가</span><span class="sxs-lookup"><span data-stu-id="6295f-820">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="6295f-821">통합 계정 어셈블리에 대한 새 cmdlet</span><span class="sxs-lookup"><span data-stu-id="6295f-821">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="6295f-822">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="6295f-822">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="6295f-823">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="6295f-823">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="6295f-824">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="6295f-824">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="6295f-825">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="6295f-825">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="6295f-826">통합 계정 일괄 처리 구성에 대한 새 cmdlet</span><span class="sxs-lookup"><span data-stu-id="6295f-826">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="6295f-827">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="6295f-827">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="6295f-828">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="6295f-828">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="6295f-829">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="6295f-829">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="6295f-830">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="6295f-830">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="6295f-831">논리 앱 SDK를 버전 4.1.0으로 업데이트</span><span class="sxs-lookup"><span data-stu-id="6295f-831">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="6295f-832">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="6295f-832">Az.Monitor</span></span>
* <span data-ttu-id="6295f-833">Get-AzMetric에 대한 도움말 업데이트</span><span class="sxs-lookup"><span data-stu-id="6295f-833">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6295f-834">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6295f-834">Az.Network</span></span>
* <span data-ttu-id="6295f-835">Add-AzApplicationGatewayCustomError에 대한 도움말 예제 업데이트</span><span class="sxs-lookup"><span data-stu-id="6295f-835">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="6295f-836">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="6295f-836">Az.OperationalInsights</span></span>
* <span data-ttu-id="6295f-837">New 및 Get ApplicationInsights 데이터 소스에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="6295f-837">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="6295f-838">지정된 작업 영역에 대한 특정 또는 전체 ApplicationInsights 데이터 원본 가져오기를 지원하기 위한 새로운 'ApplicationInsights' 종류가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-838">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span> 
    - <span data-ttu-id="6295f-839">지정된 Application-Insights 리소스 매개 변수(구독 ID, resourceGroupName 및 이름)별로 데이터 원본을 만들기 위한 New-AzOperationalInsightsApplicationInsightsDataSource cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-839">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span> 

#### <a name="azresources"></a><span data-ttu-id="6295f-840">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6295f-840">Az.Resources</span></span>
* <span data-ttu-id="6295f-841">문제 https://github.com/Azure/azure-powershell/issues/8166 수정</span><span class="sxs-lookup"><span data-stu-id="6295f-841">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="6295f-842">문제 https://github.com/Azure/azure-powershell/issues/8235 수정</span><span class="sxs-lookup"><span data-stu-id="6295f-842">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="6295f-843">문제 https://github.com/Azure/azure-powershell/issues/6219 수정</span><span class="sxs-lookup"><span data-stu-id="6295f-843">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="6295f-844">KeyCredentials 반복 만들기를 방지하기 위해 버그 수정</span><span class="sxs-lookup"><span data-stu-id="6295f-844">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="6295f-845">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6295f-845">Az.Sql</span></span>
* <span data-ttu-id="6295f-846">SQL DB 하이퍼스케일에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="6295f-846">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="6295f-847">복원 요청에서 불필요한 속성을 설정하여 복원이 실패할 수 있는 버그 수정</span><span class="sxs-lookup"><span data-stu-id="6295f-847">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="6295f-848">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="6295f-848">Az.Websites</span></span>
* <span data-ttu-id="6295f-849">Get-AzWebAppSlotMetrics 내 올바른 예제</span><span class="sxs-lookup"><span data-stu-id="6295f-849">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="6295f-850">1.3.0 - 2019년 2월</span><span class="sxs-lookup"><span data-stu-id="6295f-850">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="6295f-851">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6295f-851">Az.Accounts</span></span>
* <span data-ttu-id="6295f-852">ClientRuntime 최신 버전 업데이트</span><span class="sxs-lookup"><span data-stu-id="6295f-852">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="6295f-853">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="6295f-853">Az.AnalysisServices</span></span>
<span data-ttu-id="6295f-854">Az.AnalysisServices 모듈의 전반적인 가용성.</span><span class="sxs-lookup"><span data-stu-id="6295f-854">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6295f-855">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6295f-855">Az.Compute</span></span>
* <span data-ttu-id="6295f-856">AEM 확장: UltraSSD 및 P60, P70, P80 디스크에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="6295f-856">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="6295f-857">Set-AzVMBootDiagnostics에 대한 도움말 업데이트</span><span class="sxs-lookup"><span data-stu-id="6295f-857">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="6295f-858">Update-AzImage에 대한 도움말 및 예제 업데이트</span><span class="sxs-lookup"><span data-stu-id="6295f-858">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="6295f-859">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="6295f-859">Az.RecoveryServices</span></span>
<span data-ttu-id="6295f-860">Az.RecoveryServices 모듈의 전반적인 가용성.</span><span class="sxs-lookup"><span data-stu-id="6295f-860">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="6295f-861">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6295f-861">Az.Resources</span></span>
* <span data-ttu-id="6295f-862">리소스 그룹 관련 태그 수정</span><span class="sxs-lookup"><span data-stu-id="6295f-862">Fix tagging for resource groups</span></span> 
    - <span data-ttu-id="6295f-863">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/8166 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="6295f-863">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="6295f-864">`Get-AzureRmRoleAssignment`이(가) -ErrorAction을 준수하지 않는 문제 수정</span><span class="sxs-lookup"><span data-stu-id="6295f-864">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span> 
    - <span data-ttu-id="6295f-865">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/8235 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="6295f-865">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="6295f-866">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6295f-866">Az.Sql</span></span>
* <span data-ttu-id="6295f-867">AzSqlDatabaseBackupShortTermRetentionPolicy 가져오기/설정하기 추가</span><span class="sxs-lookup"><span data-stu-id="6295f-867">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="6295f-868">SQL cmdlet을 실행할 경우 Azure 계정에 로그인되어 있지 않은 것이 nullref 예외를 초래하는 문제 수정</span><span class="sxs-lookup"><span data-stu-id="6295f-868">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="6295f-869">Get-AzSqlCapability의 nullref 예외 수정</span><span class="sxs-lookup"><span data-stu-id="6295f-869">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="6295f-870">1.2.1 - 2019년 1월</span><span class="sxs-lookup"><span data-stu-id="6295f-870">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="6295f-871">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6295f-871">Az.Accounts</span></span>
* <span data-ttu-id="6295f-872">올바른 인증 버전을 사용하여 릴리스</span><span class="sxs-lookup"><span data-stu-id="6295f-872">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="6295f-873">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="6295f-873">Az.AnalysisServices</span></span>
* <span data-ttu-id="6295f-874">업데이트된 인증 종속성을 사용하여 릴리스</span><span class="sxs-lookup"><span data-stu-id="6295f-874">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="6295f-875">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="6295f-875">Az.RecoveryServices</span></span>
* <span data-ttu-id="6295f-876">업데이트된 인증 종속성을 사용하여 릴리스</span><span class="sxs-lookup"><span data-stu-id="6295f-876">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="6295f-877">1.2.0 - 2019년 1월</span><span class="sxs-lookup"><span data-stu-id="6295f-877">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="6295f-878">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6295f-878">Az.Accounts</span></span>
* <span data-ttu-id="6295f-879">Windows PowerShell 5.1 전용 대화형 사용자 이름/암호 인증 추가</span><span class="sxs-lookup"><span data-stu-id="6295f-879">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="6295f-880">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="6295f-880">Update incorrect online help URLs</span></span>
* <span data-ttu-id="6295f-881">Uninstall-AzureRm 관련 PS Core에 경고 메시지 추가</span><span class="sxs-lookup"><span data-stu-id="6295f-881">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="6295f-882">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="6295f-882">Az.Aks</span></span>
* <span data-ttu-id="6295f-883">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="6295f-883">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="6295f-884">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="6295f-884">Az.Automation</span></span>
* <span data-ttu-id="6295f-885">Python 2 Runbook에 대한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-885">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="6295f-886">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="6295f-886">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="6295f-887">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="6295f-887">Az.Cdn</span></span>
* <span data-ttu-id="6295f-888">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="6295f-888">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6295f-889">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6295f-889">Az.Compute</span></span>
* <span data-ttu-id="6295f-890">Invoke-AzVMReimage cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="6295f-890">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="6295f-891">Set-AzVmss에 TempDisk 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="6295f-891">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="6295f-892">New-AzVM 경고 메시지 수정</span><span class="sxs-lookup"><span data-stu-id="6295f-892">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="6295f-893">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="6295f-893">Az.ContainerRegistry</span></span>
* <span data-ttu-id="6295f-894">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="6295f-894">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="6295f-895">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="6295f-895">Az.DataFactory</span></span>
* <span data-ttu-id="6295f-896">ADF.Net SDK 버전이 3.0.0으로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-896">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="6295f-897">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="6295f-897">Az.DataLakeStore</span></span>
* <span data-ttu-id="6295f-898">MSI를 사용할 때 ADLS 엔드포인트 문제 수정</span><span class="sxs-lookup"><span data-stu-id="6295f-898">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="6295f-899">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/7462 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="6295f-899">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="6295f-900">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="6295f-900">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="6295f-901">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="6295f-901">Az.IotHub</span></span>
* <span data-ttu-id="6295f-902">Add-IotHubRoutingEndpoint cmdlet에 인코딩 형식을 추가하세요.</span><span class="sxs-lookup"><span data-stu-id="6295f-902">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="6295f-903">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="6295f-903">Az.KeyVault</span></span>
* <span data-ttu-id="6295f-904">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="6295f-904">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6295f-905">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6295f-905">Az.Network</span></span>
* <span data-ttu-id="6295f-906">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="6295f-906">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="6295f-907">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6295f-907">Az.Resources</span></span>
* <span data-ttu-id="6295f-908">'New-AzADAppCredential' 및 'New-AzADSpCredential' 참조 설명서의 잘못된 예제 수정</span><span class="sxs-lookup"><span data-stu-id="6295f-908">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="6295f-909">리소스 그룹 배포 cmdlet 실행 전 '-TemplateFile' 매개 변수 경로가 확인되지 않는 문제 수정</span><span class="sxs-lookup"><span data-stu-id="6295f-909">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="6295f-910">Az.Resources: New-AzureRmPolicyDefinition -Mode 기본값에 대한 올바른 설명서</span><span class="sxs-lookup"><span data-stu-id="6295f-910">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="6295f-911">Az.Resources: 문제 https://github.com/Azure/azure-powershell/issues/7522 수정</span><span class="sxs-lookup"><span data-stu-id="6295f-911">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="6295f-912">Az.Resources: 문제 https://github.com/Azure/azure-powershell/issues/5747 수정</span><span class="sxs-lookup"><span data-stu-id="6295f-912">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="6295f-913">'PSResourceGroupDeployment' 개체의 서식 문제 수정</span><span class="sxs-lookup"><span data-stu-id="6295f-913">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="6295f-914">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/2123 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="6295f-914">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="6295f-915">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="6295f-915">Az.ServiceFabric</span></span>
* <span data-ttu-id="6295f-916">인증서가 VMSS 모델에 추가되었는데도 예외가 발생할 경우 롤백합니다. 이는 버그 https://github.com/Azure/service-fabric-issues/issues/932 를 수정하기 위함입니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-916">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="6295f-917">일부 오류 메시지를 수정하세요.</span><span class="sxs-lookup"><span data-stu-id="6295f-917">Fix some error messages.</span></span>
* <span data-ttu-id="6295f-918">Az로의 마이그레이션을 통해서는 작동하지 않는 New-AzServiceFabriCluster를 위해 기본값 ARM 템플릿을 가진 클러스터 만들기를 수정하세요.</span><span class="sxs-lookup"><span data-stu-id="6295f-918">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="6295f-919">확장에서 클러스터 id를 확인하여 클러스터에 해당하는 VMSS에만 추가되도록 클러스터/애플리케이션 인증서 추가를 수정하세요.</span><span class="sxs-lookup"><span data-stu-id="6295f-919">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="6295f-920">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="6295f-920">Az.SignalR</span></span>
* <span data-ttu-id="6295f-921">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="6295f-921">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="6295f-922">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6295f-922">Az.Sql</span></span>
* <span data-ttu-id="6295f-923">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="6295f-923">Update incorrect online help URLs</span></span>
* <span data-ttu-id="6295f-924">가능한 값을 가진 LicenseType 매개 변수에 대한 매개 변수 설명이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-924">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="6295f-925">유일하게 업데이트된 속성인데 작동하지 않는 관리되는 인스턴스 ID의 업데이트 수정</span><span class="sxs-lookup"><span data-stu-id="6295f-925">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="6295f-926">관리되는 인스턴스에서의 사용자 지정 데이터 정렬에 대한 지원</span><span class="sxs-lookup"><span data-stu-id="6295f-926">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="6295f-927">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="6295f-927">Az.Storage</span></span>
* <span data-ttu-id="6295f-928">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="6295f-928">Update incorrect online help URLs</span></span>
* <span data-ttu-id="6295f-929">Premium Storage 계정이 클래식 로깅/메트릭을 지원하지 않기 때문에, Premium Storage 계정의 클래식 로깅/메트릭을 가져올/설정할 때 상세한 오류 메시지를 제공해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-929">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="6295f-930">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="6295f-930">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="6295f-931">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="6295f-931">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="6295f-932">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="6295f-932">Az.TrafficManager</span></span>
* <span data-ttu-id="6295f-933">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="6295f-933">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="6295f-934">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="6295f-934">Az.Websites</span></span>
* <span data-ttu-id="6295f-935">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="6295f-935">Update incorrect online help URLs</span></span>
* <span data-ttu-id="6295f-936">앱이 ASE에 호스팅되면 'New-AzWebAppSSLBinding'을 수정하여 올바른 resourcegroup+location에 인증서를 업로드합니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-936">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="6295f-937">'New-AzWebAppSSLBinding'을 수정하여 SSL 인증서를 앱에 바인딩하는 데 붙는 태그를 덮어쓰지 않도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-937">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="6295f-938">1.1.0 - 2019년 1월</span><span class="sxs-lookup"><span data-stu-id="6295f-938">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="6295f-939">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6295f-939">Az.Accounts</span></span>
* <span data-ttu-id="6295f-940">Enable-AzureRmAlias에 'Local' 범위 추가</span><span class="sxs-lookup"><span data-stu-id="6295f-940">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6295f-941">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6295f-941">Az.Compute</span></span>
* <span data-ttu-id="6295f-942">이름이 Restart/Start/Stop/Remove/Set-AzVM과 Save-AzVMImage에 설정된 ID 매개 변수에서 선택 사항이 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-942">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="6295f-943">도움말 파일의 ID에 대한 설명이 업데이트 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-943">Updated the description of ID in help files</span></span>
* <span data-ttu-id="6295f-944">Az.Accounts 모듈을 사용할 때의 이전 버전과의 호환성 문제를 해결합니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-944">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="6295f-945">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="6295f-945">Az.DataLakeStore</span></span>
* <span data-ttu-id="6295f-946">SDK 수정을 위해 데이터 평면의 SDK 버전을 1.1.14로 업데이트하세요.</span><span class="sxs-lookup"><span data-stu-id="6295f-946">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="6295f-947">getfilestatus 및 liststatus에 대한 음수 acesstime 및 modificationtime 수정, 비동기 취소 토큰 수정</span><span class="sxs-lookup"><span data-stu-id="6295f-947">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="6295f-948">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="6295f-948">Az.EventGrid</span></span>
* <span data-ttu-id="6295f-949">2019-01-01 API 버전을 사용하도록 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-949">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="6295f-950">2019-01-01 API 버전에서 새 시나리오를 지원하도록 다음 cmdlet을 업데이트</span><span class="sxs-lookup"><span data-stu-id="6295f-950">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="6295f-951">New-AzureRmEventGridSubscription: 지정을 위한 새로운 선택적 매개 변수를 추가</span><span class="sxs-lookup"><span data-stu-id="6295f-951">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="6295f-952">이벤트 Time-to-Live</span><span class="sxs-lookup"><span data-stu-id="6295f-952">Event Time-To-Live,</span></span>
        - <span data-ttu-id="6295f-953">이벤트에 대한 최대 배달 시도</span><span class="sxs-lookup"><span data-stu-id="6295f-953">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="6295f-954">배달 못한 편지의 엔드포인트입니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-954">Dead letter endpoint.</span></span>
    - <span data-ttu-id="6295f-955">Update-AzureRmEventGridSubscription: 지정을 위한 새로운 선택적 매개 변수를 추가</span><span class="sxs-lookup"><span data-stu-id="6295f-955">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="6295f-956">이벤트 Time-to-Live</span><span class="sxs-lookup"><span data-stu-id="6295f-956">Event Time-To-Live,</span></span>
        - <span data-ttu-id="6295f-957">이벤트에 대한 최대 배달 시도</span><span class="sxs-lookup"><span data-stu-id="6295f-957">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="6295f-958">배달 못한 편지의 엔드포인트입니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-958">Dead letter endpoint.</span></span>
* <span data-ttu-id="6295f-959">New-AzureRmEventGridSubscription 및 Update-AzureRmEventGridSubscription cmdlet의 EndpointType 옵션에 새 열거형 값(즉, storageQueue 및 hybridConnection)을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-959">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="6295f-960">이벤트 구독을 생성 또는 업데이트할 때 사용자가 직접 조치를 취해야 할 경우 경고 메시지를 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-960">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="6295f-961">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="6295f-961">Az.IotHub</span></span>
* <span data-ttu-id="6295f-962">최신 버전의 Azure IotHub SDK로 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="6295f-962">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="6295f-963">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="6295f-963">Az.LogicApp</span></span>
* <span data-ttu-id="6295f-964">지정된 이름이 없는 모든 Get-AzLogicApp 목록</span><span class="sxs-lookup"><span data-stu-id="6295f-964">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="6295f-965">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6295f-965">Az.Resources</span></span>
* <span data-ttu-id="6295f-966">'Get-AzResource'에 '-ODataQuery'및 '-ResourceId' 매개 변수를 제공할 때 매개 변수 집합 문제 수정</span><span class="sxs-lookup"><span data-stu-id="6295f-966">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="6295f-967">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/7875 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="6295f-967">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="6295f-968">New/Set-AzPolicyDefinition에서 -Custom 매개 변수 처리 문제 수정</span><span class="sxs-lookup"><span data-stu-id="6295f-968">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="6295f-969">New-AzDeployment 설명서에서 오타 수정</span><span class="sxs-lookup"><span data-stu-id="6295f-969">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="6295f-970">'New-AzADUser'에 '-MailNickname'매개 변수가 필수 항목으로 지정됨</span><span class="sxs-lookup"><span data-stu-id="6295f-970">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="6295f-971">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/8220 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="6295f-971">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="6295f-972">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="6295f-972">Az.SignalR</span></span>
* <span data-ttu-id="6295f-973">Az.Accounts 모듈을 사용할 때의 이전 버전과의 호환성 문제를 해결합니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-973">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="6295f-974">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6295f-974">Az.Sql</span></span>
* <span data-ttu-id="6295f-975">Storage 관리 클라이언트 종속성을 일반적인 SDK 구현으로 변환했습니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-975">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="6295f-976">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="6295f-976">Az.Storage</span></span>
* <span data-ttu-id="6295f-977">Sas Token, OAuth 또는 Anonymous를 사용하여 스토리지 컨텍스트의 StorageAccountName을 실제 스토리지 계정 이름으로 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-977">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="6295f-978">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="6295f-978">New-AzStorageContext</span></span>
* <span data-ttu-id="6295f-979">'-FullUri' 매개 변수를 사용하여 Blob 스냅샷 개체의 Sas Token을 생성하고 반환된 Uri를 스냅샷 Uri로 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-979">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="6295f-980">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="6295f-980">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="6295f-981">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="6295f-981">Az.Websites</span></span>
* <span data-ttu-id="6295f-982">'Get-AzDeletedWebApp'의 날짜 구문 분석 버그를 수정했습니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-982">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="6295f-983">Az.Accounts 모듈을 사용할 때의 이전 버전과의 호환성 문제를 해결합니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-983">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="6295f-984">1.0.0 - 2018년 12월</span><span class="sxs-lookup"><span data-stu-id="6295f-984">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="6295f-985">일반</span><span class="sxs-lookup"><span data-stu-id="6295f-985">General</span></span>

- <span data-ttu-id="6295f-986">Az 모듈 일반 공급</span><span class="sxs-lookup"><span data-stu-id="6295f-986">General Availability of Az Module</span></span>
- <span data-ttu-id="6295f-987">각 모듈에 대 한 온라인 도움말</span><span class="sxs-lookup"><span data-stu-id="6295f-987">Online help for each module</span></span>
- <span data-ttu-id="6295f-988">자세한 내용과 로드맵은 [Az 알림 페이지](https://aka.ms/azps-announce)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="6295f-988">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="6295f-989">AzureRM에서 마이그레이션하는 것에 대한 정보는 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="6295f-989">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="6295f-990">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6295f-990">Az.Accounts</span></span>
- <span data-ttu-id="6295f-991">Az.Profile에서 변경</span><span class="sxs-lookup"><span data-stu-id="6295f-991">Changed from Az.Profile</span></span>
- <span data-ttu-id="6295f-992">프로필 및 컨텍스트 형식에 대한 표 형식 수정</span><span class="sxs-lookup"><span data-stu-id="6295f-992">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="6295f-993">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="6295f-993">Az.ApiManagement</span></span>
- <span data-ttu-id="6295f-994">#7002에 대한 수정</span><span class="sxs-lookup"><span data-stu-id="6295f-994">Fixes for #7002</span></span>
- <span data-ttu-id="6295f-995">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="6295f-995">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="6295f-996">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="6295f-996">Az.Batch</span></span>
- <span data-ttu-id="6295f-997">`PSComputeNode`의 새로운 `NodeAgentInformation` 속성을 통해 풀의 각 VM에서 실행 중인 Azure Batch 노드 에이전트의 버전을 확인하는 기능이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-997">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="6295f-998">`PSDataDisk`에 대한 `Caching` 기본 값은 이제 `None` 대신 `ReadWrite`입니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-998">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="6295f-999">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="6295f-999">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="6295f-1000">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="6295f-1000">Az.Billing</span></span>
- <span data-ttu-id="6295f-1001">청구, 소비 및 UsageAggregates cmdlet 결합 cmdlet에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="6295f-1001">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="6295f-1002">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="6295f-1002">Az.CognitivServices</span></span>
- <span data-ttu-id="6295f-1003">New-AzureRmCognitiveServicesAccount 작업에서 사용 가능한 SkuName 및 Typem에 대한 완성자 추가</span><span class="sxs-lookup"><span data-stu-id="6295f-1003">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="6295f-1004">Get-AzCognitiveServicesAccountSkus에서 GetSkusWithAccountParamSetName 매개 변수 집합을 제거</span><span class="sxs-lookup"><span data-stu-id="6295f-1004">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="6295f-1005">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="6295f-1005">Az.ContainerInstance</span></span>
- <span data-ttu-id="6295f-1006">ManagedIdentity 지원이 추가됨</span><span class="sxs-lookup"><span data-stu-id="6295f-1006">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="6295f-1007">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="6295f-1007">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="6295f-1008">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="6295f-1008">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="6295f-1009">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="6295f-1009">Az.DataLakeStore</span></span>
- <span data-ttu-id="6295f-1010">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="6295f-1010">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="6295f-1011">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="6295f-1011">Az.Monitor</span></span>
- <span data-ttu-id="6295f-1012">Az.Monitor 이름 변경 및 기타 사소한 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="6295f-1012">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="6295f-1013">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="6295f-1013">Az.KeyVault</span></span>
- <span data-ttu-id="6295f-1014">출력 형식에서 사용되지 않는 'PurgeDisabled' 속성 제거</span><span class="sxs-lookup"><span data-stu-id="6295f-1014">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="6295f-1015">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="6295f-1015">Az.MachineLearning</span></span>
- <span data-ttu-id="6295f-1016">Az.MachineLearningCompute 모듈의 cmdlet 포함</span><span class="sxs-lookup"><span data-stu-id="6295f-1016">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="6295f-1017">Az.Media</span><span class="sxs-lookup"><span data-stu-id="6295f-1017">Az.Media</span></span>
- <span data-ttu-id="6295f-1018">New-AzMediaService에서 사용되지 않는 -Tags 별칭이 제거됨</span><span class="sxs-lookup"><span data-stu-id="6295f-1018">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="6295f-1019">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6295f-1019">Az.Network</span></span>
<span data-ttu-id="6295f-1020">Application Gateway에서 RewriteRuleSets를 구성하는 것에 대한 지원이 추가됨</span><span class="sxs-lookup"><span data-stu-id="6295f-1020">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="6295f-1021">추가된 새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-1021">New cmdlets added:</span></span>
        - <span data-ttu-id="6295f-1022">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="6295f-1022">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="6295f-1023">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="6295f-1023">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="6295f-1024">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="6295f-1024">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="6295f-1025">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="6295f-1025">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="6295f-1026">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="6295f-1026">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="6295f-1027">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="6295f-1027">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="6295f-1028">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="6295f-1028">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="6295f-1029">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="6295f-1029">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="6295f-1030">선택적 매개 변수를 사용하도록 cmdlet이 업데이트됨 -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="6295f-1030">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="6295f-1031">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6295f-1031">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="6295f-1032">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="6295f-1032">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="6295f-1033">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="6295f-1033">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="6295f-1034">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="6295f-1034">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="6295f-1035">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="6295f-1035">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="6295f-1036">New-AzureRmApplicationGatewayUrlPathMapConfig로 ID를 사용하여 Application Gateway에 KeyVault 지원을 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-1036">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="6295f-1037">선택적 매개 변수를 사용하도록 cmdlet이 업데이트됨 -KeyVaultSecretId, -KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="6295f-1037">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="6295f-1038">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="6295f-1038">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="6295f-1039">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="6295f-1039">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="6295f-1040">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="6295f-1040">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="6295f-1041">New-AzApplicationGateway cmdlet이 선택적 매개 변수를 사용하도록 업데이트됨 -UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="6295f-1041">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="6295f-1042">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="6295f-1042">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="6295f-1043">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="6295f-1043">Az.OperationalInsights</span></span>
- <span data-ttu-id="6295f-1044">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="6295f-1044">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="6295f-1045">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="6295f-1045">Az.Profile</span></span>
- <span data-ttu-id="6295f-1046">Az.Accounts에 모듈 이름이 변경됨</span><span class="sxs-lookup"><span data-stu-id="6295f-1046">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="6295f-1047">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="6295f-1047">Az.RecoveryServices</span></span>
- <span data-ttu-id="6295f-1048">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="6295f-1048">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="6295f-1049">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6295f-1049">Az.Resources</span></span>
- <span data-ttu-id="6295f-1050">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="6295f-1050">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="6295f-1051">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="6295f-1051">Az.ServiceFabric</span></span>
- <span data-ttu-id="6295f-1052">일반 이름과 지문으로 지정 인증서 지원</span><span class="sxs-lookup"><span data-stu-id="6295f-1052">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="6295f-1053">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="6295f-1053">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="6295f-1054">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="6295f-1054">Az.SIgnalR</span></span>
- <span data-ttu-id="6295f-1055">SIgnalR에 대한 PowerShell cmdlet에 대한 일반 공급</span><span class="sxs-lookup"><span data-stu-id="6295f-1055">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="6295f-1056">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6295f-1056">Az.Sql</span></span>
- <span data-ttu-id="6295f-1057">위협 탐지의 cmdlet에 새로운 Data_Exfiltration 및 Unsafe_Action 검색 유형 추가</span><span class="sxs-lookup"><span data-stu-id="6295f-1057">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="6295f-1058">Sql 감사 cmdlet에 대한 설명서 예제 업데이트</span><span class="sxs-lookup"><span data-stu-id="6295f-1058">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="6295f-1059">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="6295f-1059">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="6295f-1060">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="6295f-1060">Az.Storage</span></span>
- <span data-ttu-id="6295f-1061">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="6295f-1061">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="6295f-1062">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="6295f-1062">Az.Websites</span></span>
- <span data-ttu-id="6295f-1063">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="6295f-1063">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="6295f-1064">0.7.0 - 2018년 12월</span><span class="sxs-lookup"><span data-stu-id="6295f-1064">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="6295f-1065">일반</span><span class="sxs-lookup"><span data-stu-id="6295f-1065">General</span></span>

* <span data-ttu-id="6295f-1066">AzureRM에서 Az 전환 예정에 대한 사소한 변경</span><span class="sxs-lookup"><span data-stu-id="6295f-1066">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="6295f-1067">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6295f-1067">Az.Compute</span></span>

* <span data-ttu-id="6295f-1068">`New-AzVm(ss)` cmdlet에 대한 간단한 매개 변수 집합에 UltraSSD 및 갤러리 이미지에 대한 지원을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-1068">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="6295f-1069">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="6295f-1069">Az.DataLakeStore</span></span>

* <span data-ttu-id="6295f-1070">ADLS 계정의 도메인의 후행 슬래시를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-1070">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="6295f-1071">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="6295f-1071">Az.FrontDoor</span></span>

* <span data-ttu-id="6295f-1072">일부 끊어진 링크 수정</span><span class="sxs-lookup"><span data-stu-id="6295f-1072">Fixed some broken links</span></span>
    - <span data-ttu-id="6295f-1073">New-AzureRmFrontDoor 및 Set-AzureRmFrontDoor 아티클에서 New-AzureRmFrontDoorHealthProbeSettingObject cmdlet 아티클에 대한 링크가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-1073">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="6295f-1074">New-AzureRmFrontDoorManagedRuleObject 아티클에서 New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet 아티클에 대한 링크가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-1074">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="6295f-1075">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="6295f-1075">Az.RecoveryServices</span></span>

* <span data-ttu-id="6295f-1076">Azure File Share 복원 작업에 클라이언트 측 유효성 검사가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-1076">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="6295f-1077">afs 복원의 경우 storageAccountName 및 storageAccountResourceGroupName을 선택적으로 만들었습니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-1077">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="6295f-1078">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6295f-1078">Az.Resources</span></span>

* <span data-ttu-id="6295f-1079">에 대 한 수정 https://github.com/Azure/azure-powershell/issues/7679</span><span class="sxs-lookup"><span data-stu-id="6295f-1079">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="6295f-1080">기본 관리자를 요청할 때 구독 범위가 제공되는 경우 Get-AzureRmRoleAssignment를 업데이트하여 구독 범위를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-1080">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="6295f-1081">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6295f-1081">Az.Sql</span></span>

* <span data-ttu-id="6295f-1082">AzureRM에서 Az 전환 예정에 대한 사소한 변경</span><span class="sxs-lookup"><span data-stu-id="6295f-1082">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="6295f-1083">DotNet 코어에서 Get-AzureRmSqlDatabaseVulnerabilityAssessment를 사용하는 문제 해결</span><span class="sxs-lookup"><span data-stu-id="6295f-1083">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="6295f-1084">SQL 감사 cmdlet과 관련된 도움말 메시지의 설명서가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-1084">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="6295f-1085">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="6295f-1085">Az.Storage</span></span>

* <span data-ttu-id="6295f-1086">New-AzureRmStorageAccount에 -EnableHierarchicalNamespace 추가</span><span class="sxs-lookup"><span data-stu-id="6295f-1086">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="6295f-1087">파일 복사 cmdlet이 -DestContext 입력이 없을 때 대상의 원본 컨텍스트를 다시 사용할 수 없는 문제 수정</span><span class="sxs-lookup"><span data-stu-id="6295f-1087">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="6295f-1088">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="6295f-1088">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="6295f-1089">고정적인 웹 사이트 구성 지원</span><span class="sxs-lookup"><span data-stu-id="6295f-1089">Support Static Website configuration</span></span>
    - <span data-ttu-id="6295f-1090">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="6295f-1090">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="6295f-1091">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="6295f-1091">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="6295f-1092">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="6295f-1092">Az.Websites</span></span>

* <span data-ttu-id="6295f-1093">Set-AzureRmWebApp 및 Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="6295f-1093">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span> 
    - <span data-ttu-id="6295f-1094">Windows 및 Linux 컨테이너 응용 프로그램에 탑재할 Azure Storage 경로를 지정하기 위해 새 매개 변수(-AzureStoragePath)가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-1094">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="6295f-1095">새 cmdlet New-AzureRmWebAppAzureStoragePath의 출력을 매개 변수로 사용하여 Azure Storage 경로를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-1095">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="6295f-1096">0.6.1 - 2018년 11월</span><span class="sxs-lookup"><span data-stu-id="6295f-1096">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="6295f-1097">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="6295f-1097">Az.ApiManagement</span></span>
* <span data-ttu-id="6295f-1098">형식 매핑 문제에 대한 종속성 업데이트</span><span class="sxs-lookup"><span data-stu-id="6295f-1098">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="6295f-1099">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="6295f-1099">Az.Automation</span></span>
* <span data-ttu-id="6295f-1100">Azure Automation cmdlet 기반 Swagger</span><span class="sxs-lookup"><span data-stu-id="6295f-1100">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="6295f-1101">업데이트 관리 cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="6295f-1101">Added Update Management cmdlets</span></span>
* <span data-ttu-id="6295f-1102">소스 제어 cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="6295f-1102">Added Source Control cmdlets</span></span>
* <span data-ttu-id="6295f-1103">Remove-AzureRmAutomationHybridWorkerGroup cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="6295f-1103">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="6295f-1104">DSC 노드 등록 명령 수정</span><span class="sxs-lookup"><span data-stu-id="6295f-1104">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="6295f-1105">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6295f-1105">Az.Compute</span></span>
* <span data-ttu-id="6295f-1106">SystemAssigned ID에 대한 ID 문제 수정</span><span class="sxs-lookup"><span data-stu-id="6295f-1106">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="6295f-1107">형식 매핑 문제에 대한 종속성 업데이트</span><span class="sxs-lookup"><span data-stu-id="6295f-1107">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="6295f-1108">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="6295f-1108">Az.ContainerInstance</span></span>
* <span data-ttu-id="6295f-1109">형식 매핑 문제에 대한 종속성 업데이트</span><span class="sxs-lookup"><span data-stu-id="6295f-1109">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="6295f-1110">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="6295f-1110">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="6295f-1111">마켓플레이스 cmdlet에 대한 예제 설명 업데이트</span><span class="sxs-lookup"><span data-stu-id="6295f-1111">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="6295f-1112">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6295f-1112">Az.Network</span></span>
* <span data-ttu-id="6295f-1113">New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="6295f-1113">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="6295f-1114">지원되는 AzureFirewall 네트워크 프로토콜에 ICMP 다시 추가</span><span class="sxs-lookup"><span data-stu-id="6295f-1114">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="6295f-1115">Test-AzureRmNetworkWatcherConnectivity cmdlet을 업데이트하여 대상 ID, 주소 및 포트 유효성 검사를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-1115">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span> 
* <span data-ttu-id="6295f-1116">VirtualNetwork 맵의 메모리 사용 문제 해결</span><span class="sxs-lookup"><span data-stu-id="6295f-1116">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="6295f-1117">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="6295f-1117">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="6295f-1118">보호된 파일 공유에 대한 정책을 수정하는 것에 대해 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-1118">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="6295f-1119">정책 표준 시간대를 대문자로 변환했습니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-1119">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="6295f-1120">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="6295f-1120">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="6295f-1121">New-AzureRmRecoveryServicesAsrProtectableItem의 예제 정정</span><span class="sxs-lookup"><span data-stu-id="6295f-1121">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="6295f-1122">형식 매핑 문제에 대한 종속성 업데이트</span><span class="sxs-lookup"><span data-stu-id="6295f-1122">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="6295f-1123">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="6295f-1123">Az.Relay</span></span>
* <span data-ttu-id="6295f-1124">선택적 매개 변수 -KeyValue를 New-AzureRmRelayKey cmdlet에 추가하여 사용자가 KeyValue를 제공할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-1124">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="6295f-1125">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6295f-1125">Az.Resources</span></span>
* <span data-ttu-id="6295f-1126">`New-AzureRmPolicyAssignment` 및 `Set-AzureRmPolicyAssignment`의 자원 ID 관련 매개 변수에 대한 도움말 문서를 업데이트함</span><span class="sxs-lookup"><span data-stu-id="6295f-1126">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="6295f-1127">-Metadata를 사용하는 New-AzureRmPolicyDefinition에 대한 예제 추가</span><span class="sxs-lookup"><span data-stu-id="6295f-1127">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="6295f-1128">NetStandard의 태그 키에서 대소문자 보존을 허용하도록 수정: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="6295f-1128">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="6295f-1129">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="6295f-1129">Az.ServiceFabric</span></span>
* <span data-ttu-id="6295f-1130">향후 호환성이 손상되는 변경에 대한 사용 중단 메시지 추가</span><span class="sxs-lookup"><span data-stu-id="6295f-1130">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="6295f-1131">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6295f-1131">Az.Sql</span></span>
* <span data-ttu-id="6295f-1132">Azure Sql Database Managed Instance 및 Azure Sql Managed Database에 CRUD 작업을 위한 새 cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="6295f-1132">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="6295f-1133">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="6295f-1133">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="6295f-1134">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="6295f-1134">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="6295f-1135">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="6295f-1135">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="6295f-1136">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="6295f-1136">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="6295f-1137">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="6295f-1137">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="6295f-1138">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="6295f-1138">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="6295f-1139">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="6295f-1139">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="6295f-1140">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="6295f-1140">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="6295f-1141">서버 또는 데이터베이스에서 확장 감사 정책 관리를 활성화했습니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-1141">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="6295f-1142">새 매개 변수(PredicateExpression)가 감사 로그 필터링을 사용하도록 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-1142">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="6295f-1143">Cmdlet이 레거시 클라이언트 대신 SQL 클라이언트를 사용하도록 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-1143">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="6295f-1144">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="6295f-1144">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="6295f-1145">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="6295f-1145">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="6295f-1146">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="6295f-1146">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="6295f-1147">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="6295f-1147">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="6295f-1148">스토리지 계정 이름 매개 변수가 설정된 Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings를 사용할 때의 문제 해결</span><span class="sxs-lookup"><span data-stu-id="6295f-1148">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="6295f-1149">0.5.0 - 2018년 11월</span><span class="sxs-lookup"><span data-stu-id="6295f-1149">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="6295f-1150">일반</span><span class="sxs-lookup"><span data-stu-id="6295f-1150">General</span></span>
* <span data-ttu-id="6295f-1151">많은 핵심 cmdlet에 Resource Completers를 추가하여 대화형으로 cmdlet을 호출할 때 기존 리소스 이름을 탭으로 이동할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-1151">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="6295f-1152">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="6295f-1152">Az.Profile</span></span>
* <span data-ttu-id="6295f-1153">ClientRuntime의 최신 버전을 사용하도록 일반적인 코드를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-1153">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="6295f-1154">Connect-AzAccount cmdlet의 매개 변수 TenantId 이름을 Tenant로 바꾸고 TenantId의 별칭을 추가합니다</span><span class="sxs-lookup"><span data-stu-id="6295f-1154">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="6295f-1155">Connect-AzAccount의 업데이트된 TenantId 설명</span><span class="sxs-lookup"><span data-stu-id="6295f-1155">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="6295f-1156">테넌트 도메인을 제공할 때 실패한 로그인에 대한 오류 메시지 수정</span><span class="sxs-lookup"><span data-stu-id="6295f-1156">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="6295f-1157">테넌트에 구독이 없는 계정의 컨텍스트 이름 충돌 문제 수정</span><span class="sxs-lookup"><span data-stu-id="6295f-1157">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="6295f-1158">MSI를 사용할 때 DataLake 엔드포인트 문제 수정</span><span class="sxs-lookup"><span data-stu-id="6295f-1158">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="6295f-1159">연결되지 않은 경우 'Disconnect-AzAccount'가 throw하는 문제 수정</span><span class="sxs-lookup"><span data-stu-id="6295f-1159">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="6295f-1160">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="6295f-1160">Az.CognitiveServices</span></span>
* <span data-ttu-id="6295f-1161">Get-AzCognitiveServicesAccountSkus 작업을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-1161">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6295f-1162">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6295f-1162">Az.Compute</span></span>
* <span data-ttu-id="6295f-1163">Add-AzVmssVMDataDisk 및 Remove-AzVmssVMDataDisk cmdlet를 추가합니다</span><span class="sxs-lookup"><span data-stu-id="6295f-1163">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="6295f-1164">Get-AzVMImage는 AutomaticOSUpgradeProperties를 표시합니다</span><span class="sxs-lookup"><span data-stu-id="6295f-1164">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="6295f-1165">수정된 SetAzVMChefExtension -BootstrapOptions 및 -JsonAttribute option 값이 json 형식으로 설정하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-1165">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="6295f-1166">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="6295f-1166">Az.DataLakeStore</span></span>
* <span data-ttu-id="6295f-1167">DataLake 패키지를 1.1.10으로 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-1167">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="6295f-1168">기본 동시성을 다중 스레드 작업에 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-1168">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="6295f-1169">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="6295f-1169">Az.Insights</span></span>
* <span data-ttu-id="6295f-1170">해결된 문제 #7267(자동 크기 조정 영역)</span><span class="sxs-lookup"><span data-stu-id="6295f-1170">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="6295f-1171">열거된 매개 변수를 제대로 설정하지 않은 새 자동 크기 조정 규칙을 만드는 데 문제가 있습니다(이를 항상 기본값으로 설정함).</span><span class="sxs-lookup"><span data-stu-id="6295f-1171">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="6295f-1172">해결된 문제 # 7513[자세한 정보] Set-AzDiagnosticSetting은 설정을 생성하는 동안 범주를 명시적으로 지정해야 합니다</span><span class="sxs-lookup"><span data-stu-id="6295f-1172">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="6295f-1173">이제 cmdlet은 생성 중에 사용할 범주를 명시적으로 표시할 필요가 없습니다. 즉, 문서화된대로 작동합니다</span><span class="sxs-lookup"><span data-stu-id="6295f-1173">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6295f-1174">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6295f-1174">Az.Network</span></span>
* <span data-ttu-id="6295f-1175">다음 cmdlet에 대해 PeeringType을 필수 매개 변수로 변경했습니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-1175">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="6295f-1176">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="6295f-1176">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="6295f-1177">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="6295f-1177">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="6295f-1178">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="6295f-1178">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="6295f-1179">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="6295f-1179">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="6295f-1180">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="6295f-1180">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="6295f-1181">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="6295f-1181">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="6295f-1182">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="6295f-1182">Az.PolicyInsights</span></span>
* <span data-ttu-id="6295f-1183">추가된 정책 재구성 cmdlet</span><span class="sxs-lookup"><span data-stu-id="6295f-1183">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="6295f-1184">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6295f-1184">Az.Resources</span></span>
* <span data-ttu-id="6295f-1185">에 대 한 수정 https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="6295f-1185">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="6295f-1186">'Get-AzResource'에 대해 '-ResourceId' 매개 변수를 사용하여 리소스 나열 허용</span><span class="sxs-lookup"><span data-stu-id="6295f-1186">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="6295f-1187">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="6295f-1187">Az.ServiceBus</span></span>
* <span data-ttu-id="6295f-1188">마이그레이션 상태를 알 수 있도록 PSServiceBusMigrationConfigurationAttributes에 MigrationState 읽기 전용 속성 추가.</span><span class="sxs-lookup"><span data-stu-id="6295f-1188">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="6295f-1189">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="6295f-1189">Az.ServiceFabric</span></span>
* <span data-ttu-id="6295f-1190">Linux Vmss에 인증서 추가 수정.</span><span class="sxs-lookup"><span data-stu-id="6295f-1190">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="6295f-1191">Add-AzServiceFabricClusterCertificate 수정</span><span class="sxs-lookup"><span data-stu-id="6295f-1191">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="6295f-1192">새 인증서(Azure/service-fabric-issues#932)에서 올바른 지문을 사용.</span><span class="sxs-lookup"><span data-stu-id="6295f-1192">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="6295f-1193">올바르게 예외 표시(Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="6295f-1193">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="6295f-1194">Vmss CreateOrUpdate 작업을 시작하기 전에 'Update-AzServiceFabricDurability'를 수정하여 클러스터 구성 업데이트.</span><span class="sxs-lookup"><span data-stu-id="6295f-1194">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="6295f-1195">0.4.0 - 2018년 10월</span><span class="sxs-lookup"><span data-stu-id="6295f-1195">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="6295f-1196">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="6295f-1196">Az.Profile</span></span>
* <span data-ttu-id="6295f-1197">CloudShell에서 Get-AzSubscription을 사용하여 문제를 해결합니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-1197">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="6295f-1198">ClientRuntime의 최신 버전을 사용하도록 일반적인 코드를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-1198">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6295f-1199">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6295f-1199">Az.Compute</span></span>
* <span data-ttu-id="6295f-1200">'New-AzVm'에 대해 간단한 매개 변수를 사용하는 경우 가속화된 네트워킹을 설정하기 위해 새 크기가 VM 크기의 허용 목록에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-1200">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="6295f-1201">모든 cmdlet에 ResourceName 인수 완성자가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-1201">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="6295f-1202">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="6295f-1202">Az.DataLakeStore</span></span>
* <span data-ttu-id="6295f-1203">Virtual Network 규칙에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="6295f-1203">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="6295f-1204">Get-AzDataLakeStoreVirtualNetworkRule: Azure Data Lake Store 가상 네트워크 규칙을 가져오거나 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-1204">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="6295f-1205">Add-AzDataLakeStoreVirtualNetworkRule: 지정된 Data Lake Store 계정에 가상 네트워크 규칙을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-1205">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="6295f-1206">Set-AzDataLakeStoreVirtualNetworkRule: 지정된 Data Lake Store 계정에 지정된 가상 네트워크 규칙을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-1206">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="6295f-1207">Remove-AzDataLakeStoreVirtualNetworkRule: Azure Data Lake Store 가상 네트워크 규칙을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-1207">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6295f-1208">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6295f-1208">Az.Network</span></span>
* <span data-ttu-id="6295f-1209">Test-AzNetworkWatcherConnectivity cmdlet을 업데이트하고, 백 엔드에 프로토콜 값을 전달합니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-1209">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="6295f-1210">모든 cmdlet에 ResourceName 인수 완성자가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-1210">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="6295f-1211">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6295f-1211">Az.Resources</span></span>
* <span data-ttu-id="6295f-1212">(기본 프로필에 구독이 없고 범위가 지정되지 않은 경우) 시나리오에서 의미 있는 예외를 추가하여 Get-AzRoleDefinition이 인식할 수 없는 예외를 throw하는 문제를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-1212">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="6295f-1213">또한 기본 매개 변수 집합을 'RoleDefinitionNameParameterSet'으로 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-1213">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="6295f-1214">0.3.0 - 2018년 10월</span><span class="sxs-lookup"><span data-stu-id="6295f-1214">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="6295f-1215">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="6295f-1215">Azure.Storage</span></span>
* <span data-ttu-id="6295f-1216">대상에 메타데이터가 있을 때 Blob/파일이 메타 데이터를 복사하지 않는 문제 수정</span><span class="sxs-lookup"><span data-stu-id="6295f-1216">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="6295f-1217">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="6295f-1217">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="6295f-1218">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="6295f-1218">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="6295f-1219">특정 위치의 저장소 리소스 사용을 지원하고 글로벌 저장소 리소스 사용 가져오기는 더 이상 사용되지 않는다는 경고 메시지를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-1219">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="6295f-1220">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="6295f-1220">Get-AzStorageUsage</span></span>
    
#### <a name="azcognitiveservices"></a><span data-ttu-id="6295f-1221">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="6295f-1221">Az.CognitiveServices</span></span>
* <span data-ttu-id="6295f-1222">기존 계정이 없는 Get-AzCognitiveServicesAccountSkus를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-1222">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6295f-1223">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6295f-1223">Az.Compute</span></span>
* <span data-ttu-id="6295f-1224">Get-AzVM -ResourceGroupName <rg>가 필요한 경우 50개가 넘는 결과를 반환하도록 수정</span><span class="sxs-lookup"><span data-stu-id="6295f-1224">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="6295f-1225">'SimpleParameterSet' 예제가 New-AzVmss cmdlet 도움말에 추가됨</span><span class="sxs-lookup"><span data-stu-id="6295f-1225">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="6295f-1226">Azure Disk Encryption 진행률 메시지의 오타를 수정</span><span class="sxs-lookup"><span data-stu-id="6295f-1226">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="6295f-1227">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="6295f-1227">Az.DataFactoryV2</span></span>
* <span data-ttu-id="6295f-1228">ADF.Net SDK 버전을 2.3.0으로 업데이트</span><span class="sxs-lookup"><span data-stu-id="6295f-1228">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6295f-1229">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6295f-1229">Az.Network</span></span>
* <span data-ttu-id="6295f-1230">NetworkProfile 기능 추가</span><span class="sxs-lookup"><span data-stu-id="6295f-1230">Added NetworkProfile functionality.</span></span> <span data-ttu-id="6295f-1231">추가된 새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-1231">new cmdlets added</span></span>
    - <span data-ttu-id="6295f-1232">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="6295f-1232">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="6295f-1233">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="6295f-1233">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="6295f-1234">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="6295f-1234">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="6295f-1235">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="6295f-1235">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="6295f-1236">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="6295f-1236">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="6295f-1237">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="6295f-1237">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="6295f-1238">서브넷 모델에 서비스 연결 링크 추가</span><span class="sxs-lookup"><span data-stu-id="6295f-1238">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="6295f-1239">New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="6295f-1239">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="6295f-1240">Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="6295f-1240">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="6295f-1241">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="6295f-1241">Az.RedisCache</span></span>
* <span data-ttu-id="6295f-1242">모든 문자열을 Size 매개 변수로 진행되도록 허용</span><span class="sxs-lookup"><span data-stu-id="6295f-1242">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="6295f-1243">PSArgumentCompleter 팝업에 P5 추가</span><span class="sxs-lookup"><span data-stu-id="6295f-1243">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="6295f-1244">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6295f-1244">Az.Resources</span></span>
* <span data-ttu-id="6295f-1245">-Mode 매개 변수를 Set-AzPolicyDefinition에 추가</span><span class="sxs-lookup"><span data-stu-id="6295f-1245">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="6295f-1246">사용자가 포함된 Origin 작업에서 Get-AzProviderOperation commandlet 버그 수정</span><span class="sxs-lookup"><span data-stu-id="6295f-1246">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="6295f-1247">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6295f-1247">Az.Sql</span></span>
* <span data-ttu-id="6295f-1248">일부 백업 cmdlet이 현재 azure 구독을 인식하지 않는 문제 해결</span><span class="sxs-lookup"><span data-stu-id="6295f-1248">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="6295f-1249">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="6295f-1249">Az.Websites</span></span>
* <span data-ttu-id="6295f-1250">새 cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - 컨테이너 지속적인 배포 Webhook URL을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-1250">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="6295f-1251">새 cmdlet New-AzWebAppContainerPSSession 및 Enter-WebAppContainerPSSession -  windows 컨테이너 앱에 PowerShell 원격 세션을 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="6295f-1251">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="6295f-1252">0.2.0 - 2018년 9월</span><span class="sxs-lookup"><span data-stu-id="6295f-1252">0.2.0 - September 2018</span></span>
 <span data-ttu-id="6295f-1253">최초 릴리스</span><span class="sxs-lookup"><span data-stu-id="6295f-1253">Initial Release</span></span>