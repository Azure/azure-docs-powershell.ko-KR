---
title: Azure PowerShell 릴리스 정보
description: Azure PowerShell 모듈의 모든 최신 업데이트에 대해 알아봅니다.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/10/2020
ms.custom: devx-track-azurepowershell
ms.service: azure-powershell
ms.openlocfilehash: 8cf52259008b2551b780d4cf6f09b4876673723c
ms.sourcegitcommit: 12bb1a6d1f89789bf2a78992f9b8ca848691a4d7
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/19/2021
ms.locfileid: "98574115"
---
# <a name="azure-powershell-release-notes"></a><span data-ttu-id="76011-103">Azure PowerShell 릴리스 정보</span><span class="sxs-lookup"><span data-stu-id="76011-103">Azure PowerShell release notes</span></span>

## <a name="540---january-2021"></a><span data-ttu-id="76011-104">5.4.0 - 2021년 1월</span><span class="sxs-lookup"><span data-stu-id="76011-104">5.4.0 - January 2021</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="76011-105">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="76011-105">Az.Accounts</span></span>
* <span data-ttu-id="76011-106">디버그 메시지에 올바른 클라이언트 요청 ID 표시[#13745]</span><span class="sxs-lookup"><span data-stu-id="76011-106">Shown correct client request id on debug message [#13745]</span></span>
* <span data-ttu-id="76011-107">공용 Azure PowerShell 예외 형식 추가됨</span><span class="sxs-lookup"><span data-stu-id="76011-107">Added common Azure PowerShell exception type</span></span>
* <span data-ttu-id="76011-108">지원되는 스토리지 API 2019-06-01</span><span class="sxs-lookup"><span data-stu-id="76011-108">Supported storage API 2019-06-01</span></span>

#### <a name="azautomation"></a><span data-ttu-id="76011-109">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="76011-109">Az.Automation</span></span>
* <span data-ttu-id="76011-110">업데이트 관리 일정에 대한 설명이 채워지지 않은 문제 해결</span><span class="sxs-lookup"><span data-stu-id="76011-110">Fixed issue where description was not populated for update management schedules</span></span>

#### <a name="azcosmosdb"></a><span data-ttu-id="76011-111">Az.CosmosDB</span><span class="sxs-lookup"><span data-stu-id="76011-111">Az.CosmosDB</span></span>
* <span data-ttu-id="76011-112">'Az.CosmosDB' 모듈의 일반 공급</span><span class="sxs-lookup"><span data-stu-id="76011-112">General availability of 'Az.CosmosDB' module</span></span>
* <span data-ttu-id="76011-113">New-AzCosmosDBAccount cmdlet을 제한하여 기존 데이터베이스 계정에 대한 업데이트를 호출합니다.</span><span class="sxs-lookup"><span data-stu-id="76011-113">Restricting New-AzCosmosDBAccount cmdlet to make update calls to existing Database Accounts.</span></span>
* <span data-ttu-id="76011-114">SqlContainer에 AnalyticalStorageTTL를 소개합니다.</span><span class="sxs-lookup"><span data-stu-id="76011-114">Introducing AnalyticalStorageTTL in SqlContainer.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="76011-115">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="76011-115">Az.IotHub</span></span>
* <span data-ttu-id="76011-116">SAS 토큰 생성과 관련된 회귀 수정</span><span class="sxs-lookup"><span data-stu-id="76011-116">Fixed a regression regarding SAS token generation</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="76011-117">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="76011-117">Az.KeyVault</span></span>
* <span data-ttu-id="76011-118">비밀 관리 모듈의 문제 해결</span><span class="sxs-lookup"><span data-stu-id="76011-118">Fixed an issue in Secret Management module</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="76011-119">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="76011-119">Az.LogicApp</span></span>
* <span data-ttu-id="76011-120">'Get-AzLogicAppTriggerHistory' 및 'Get-AzLogicAppRunAction'이 결과의 첫 페이지만 검색하는 문제 해결[#9141]</span><span class="sxs-lookup"><span data-stu-id="76011-120">Fixed issue that 'Get-AzLogicAppTriggerHistory' and 'Get-AzLogicAppRunAction' only retrieving the first page of results [#9141]</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="76011-121">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="76011-121">Az.Monitor</span></span>
* <span data-ttu-id="76011-122">데이터 수집 규칙에 대한 cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-122">Added cmdlets for data collection rules:</span></span> 
    - <span data-ttu-id="76011-123">'Get-AzDataCollectionRule'</span><span class="sxs-lookup"><span data-stu-id="76011-123">'Get-AzDataCollectionRule'</span></span>
    - <span data-ttu-id="76011-124">'New-AzDataCollectionRule'</span><span class="sxs-lookup"><span data-stu-id="76011-124">'New-AzDataCollectionRule'</span></span>
    - <span data-ttu-id="76011-125">'Set-AzDataCollectionRule'</span><span class="sxs-lookup"><span data-stu-id="76011-125">'Set-AzDataCollectionRule'</span></span>
    - <span data-ttu-id="76011-126">'Update-AzDataCollectionRule'</span><span class="sxs-lookup"><span data-stu-id="76011-126">'Update-AzDataCollectionRule'</span></span>
    - <span data-ttu-id="76011-127">'Remove-AzDataCollectionRule'</span><span class="sxs-lookup"><span data-stu-id="76011-127">'Remove-AzDataCollectionRule'</span></span>
* <span data-ttu-id="76011-128">데이터 수집 규칙 연결에 대한 cmdlet이 추가됨</span><span class="sxs-lookup"><span data-stu-id="76011-128">Added cmdlets for data collection rules associations</span></span>
    - <span data-ttu-id="76011-129">'Get-AzDataCollectionRuleAssociation'</span><span class="sxs-lookup"><span data-stu-id="76011-129">'Get-AzDataCollectionRuleAssociation'</span></span>
    - <span data-ttu-id="76011-130">'New-AzDataCollectionRuleAssociation'</span><span class="sxs-lookup"><span data-stu-id="76011-130">'New-AzDataCollectionRuleAssociation'</span></span>
    - <span data-ttu-id="76011-131">'Remove-AzDataCollectionRuleAssociation'</span><span class="sxs-lookup"><span data-stu-id="76011-131">'Remove-AzDataCollectionRuleAssociation'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="76011-132">Az.Network</span><span class="sxs-lookup"><span data-stu-id="76011-132">Az.Network</span></span>
* <span data-ttu-id="76011-133">VpnGatewayNATRule의 CRUD에 대한 새 cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-133">Added new cmdlets for CRUD of VpnGatewayNATRule.</span></span>
    - <span data-ttu-id="76011-134">'New-AzAzVpnGatewayNatRule'</span><span class="sxs-lookup"><span data-stu-id="76011-134">'New-AzAzVpnGatewayNatRule'</span></span>
    - <span data-ttu-id="76011-135">'Update-AzAzVpnGatewayNatRule'</span><span class="sxs-lookup"><span data-stu-id="76011-135">'Update-AzAzVpnGatewayNatRule'</span></span>
    - <span data-ttu-id="76011-136">'Get-AzAzVpnGatewayNatRule'</span><span class="sxs-lookup"><span data-stu-id="76011-136">'Get-AzAzVpnGatewayNatRule'</span></span>
    - <span data-ttu-id="76011-137">'Remove-AzAzVpnGatewayNatRule'</span><span class="sxs-lookup"><span data-stu-id="76011-137">'Remove-AzAzVpnGatewayNatRule'</span></span>    
* <span data-ttu-id="76011-138">VpnGateway 리소스에서 NATRule을 설정하고 VpnSiteLinkConnection 리소스와 연결하도록 cmdlet이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-138">Updated cmdlets to set NATRule on VpnGateway resource and associate it with VpnSiteLinkConnection resource.</span></span>
    - <span data-ttu-id="76011-139">'New-AzVpnGateway'</span><span class="sxs-lookup"><span data-stu-id="76011-139">'New-AzVpnGateway'</span></span>
    - <span data-ttu-id="76011-140">'Update-AzVpnGateway'</span><span class="sxs-lookup"><span data-stu-id="76011-140">'Update-AzVpnGateway'</span></span> 
    - <span data-ttu-id="76011-141">'New-AzVpnSiteLinkConnection'</span><span class="sxs-lookup"><span data-stu-id="76011-141">'New-AzVpnSiteLinkConnection'</span></span>
* <span data-ttu-id="76011-142">Virtual Network 게이트웨이 연결에서 ConnectionMode 설정을 사용하도록 cmdlet이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-142">Updated cmdlets to enable setting of ConnectionMode on Virtual Network Gateway Connections.</span></span>
    - <span data-ttu-id="76011-143">'New-AzVirtualNetworkGatewayConnection'</span><span class="sxs-lookup"><span data-stu-id="76011-143">'New-AzVirtualNetworkGatewayConnection'</span></span>
    - <span data-ttu-id="76011-144">'Set-AzVirtualNetworkGatewayConnection'</span><span class="sxs-lookup"><span data-stu-id="76011-144">'Set-AzVirtualNetworkGatewayConnection'</span></span>
* <span data-ttu-id="76011-145">'New-AzFirewallPolicyApplicationRule' cmdlet 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-145">Updated 'New-AzFirewallPolicyApplicationRule' cmdlet:</span></span>
    - <span data-ttu-id="76011-146">매개 변수 TargetUrl이 추가됨</span><span class="sxs-lookup"><span data-stu-id="76011-146">Added parameter TargetUrl</span></span>
    - <span data-ttu-id="76011-147">매개 변수 TerminateTLS가 추가됨</span><span class="sxs-lookup"><span data-stu-id="76011-147">Added parameter TerminateTLS</span></span>
* <span data-ttu-id="76011-148">Azure Firewall Premium 기능에 대한 새 cmdlet이 추가됨</span><span class="sxs-lookup"><span data-stu-id="76011-148">Added new cmdlets for Azure Firewall Premium Features</span></span>
    - <span data-ttu-id="76011-149">'New-AzFirewallPolicyIntrusionDetection'</span><span class="sxs-lookup"><span data-stu-id="76011-149">'New-AzFirewallPolicyIntrusionDetection'</span></span>
    - <span data-ttu-id="76011-150">'New-AzFirewallPolicyIntrusionDetectionBypassTraffic'</span><span class="sxs-lookup"><span data-stu-id="76011-150">'New-AzFirewallPolicyIntrusionDetectionBypassTraffic'</span></span>
    - <span data-ttu-id="76011-151">'New-AzFirewallPolicyIntrusionDetectionSignatureOverride'</span><span class="sxs-lookup"><span data-stu-id="76011-151">'New-AzFirewallPolicyIntrusionDetectionSignatureOverride'</span></span>
* <span data-ttu-id="76011-152">New-AzFirewallPolicy cmdlet이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-152">Updated New-AzFirewallPolicy cmdlet:</span></span>
    - <span data-ttu-id="76011-153">매개 변수 -SkuTier 추가됨</span><span class="sxs-lookup"><span data-stu-id="76011-153">Added parameter -SkuTier</span></span>
    - <span data-ttu-id="76011-154">매개 변수 -Identity 추가됨</span><span class="sxs-lookup"><span data-stu-id="76011-154">Added parameter -Identity</span></span>
    - <span data-ttu-id="76011-155">매개 변수 -UserAssignedIdentityId 추가됨</span><span class="sxs-lookup"><span data-stu-id="76011-155">Added parameter -UserAssignedIdentityId</span></span>
    - <span data-ttu-id="76011-156">매개 변수 -IntrusionDetection 추가됨</span><span class="sxs-lookup"><span data-stu-id="76011-156">Added parameter -IntrusionDetection</span></span>
    - <span data-ttu-id="76011-157">매개 변수 -TransportSecurityName 추가됨</span><span class="sxs-lookup"><span data-stu-id="76011-157">Added parameter -TransportSecurityName</span></span>
    - <span data-ttu-id="76011-158">매개 변수 -TransportSecurityKeyVaultSecretId 추가됨</span><span class="sxs-lookup"><span data-stu-id="76011-158">Added parameter -TransportSecurityKeyVaultSecretId</span></span>
* <span data-ttu-id="76011-159">가상 네트워크 게이트웨이 연결에 대한 IKE 보안 연결을 가져오는 새 cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-159">Added new cmdlet to fetch IKE Security Associations for Virtual Network Gateway Connections.</span></span>
    - <span data-ttu-id="76011-160">'Get-AzVirtualNetworkGatewayConnectionIkeSa'</span><span class="sxs-lookup"><span data-stu-id="76011-160">'Get-AzVirtualNetworkGatewayConnectionIkeSa'</span></span>
* <span data-ttu-id="76011-161">p2sVpnGateway에 대한 여러 인증 지원이 추가됨</span><span class="sxs-lookup"><span data-stu-id="76011-161">Added multiple Authentication support for p2sVpnGateway</span></span>
    - <span data-ttu-id="76011-162">여러 인증 매개 변수를 설정할 수 있도록 New-AzVpnServerConfiguration 및 Update-AzVpnServerConfiguration이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-162">Updated New-AzVpnServerConfiguration and Update-AzVpnServerConfiguration to allow multiple authentication parameters to be set.</span></span>
* <span data-ttu-id="76011-163">'New-AzVpnGateway' 및 'New-AzP2sVpnGateway' cmdlet이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-163">Updated 'New-AzVpnGateway' and 'New-AzP2sVpnGateway' cmdlet:</span></span>
    - <span data-ttu-id="76011-164">매개 변수 EnableRoutingPreferenceInternetFlag 추가됨</span><span class="sxs-lookup"><span data-stu-id="76011-164">Added parameter EnableRoutingPreferenceInternetFlag</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="76011-165">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="76011-165">Az.RecoveryServices</span></span>
* <span data-ttu-id="76011-166">지역 간 복원 기능이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-166">Added Cross Region Restore feature.</span></span>  
* <span data-ttu-id="76011-167">대상 항목이 가용성 그룹인 경우 워크로드 구성 가져오기가 차단되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-167">Blocked getting workload config when target item is an availability group.</span></span>

#### <a name="azresources"></a><span data-ttu-id="76011-168">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="76011-168">Az.Resources</span></span>
* <span data-ttu-id="76011-169">New-Az\*Deployments cmdlet에서 -QueryString 매개 변수에 대한 지원 추가됨</span><span class="sxs-lookup"><span data-stu-id="76011-169">Added support for -QueryString parameter in New-Az\*Deployments cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="76011-170">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="76011-170">Az.Sql</span></span>
* <span data-ttu-id="76011-171">'Start-AzSqlInstanceDatabaseLogReplay'cmdlet 동기화, -AsJob 플래그 추가됨</span><span class="sxs-lookup"><span data-stu-id="76011-171">Made 'Start-AzSqlInstanceDatabaseLogReplay' cmdlet synchronous, added -AsJob flag</span></span>

#### <a name="azstorage"></a><span data-ttu-id="76011-172">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="76011-172">Az.Storage</span></span>
* <span data-ttu-id="76011-173">-IncludeVersion으로 BLOB을 나열할 때 ContinuationToken이 null이 되지 않도록 수정</span><span class="sxs-lookup"><span data-stu-id="76011-173">Fix ContinuationToken never null when list blob with -IncludeVersion</span></span>
    - <span data-ttu-id="76011-174">'Get-AzStorageBlob'</span><span class="sxs-lookup"><span data-stu-id="76011-174">'Get-AzStorageBlob'</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="76011-175">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="76011-175">Az.Websites</span></span>
* <span data-ttu-id="76011-176">App Service 관리형 인증서에 대한 지원이 추가됨</span><span class="sxs-lookup"><span data-stu-id="76011-176">Added support for App Service Managed certificates</span></span>
    - <span data-ttu-id="76011-177">'New-AzWebAppCertificate'</span><span class="sxs-lookup"><span data-stu-id="76011-177">'New-AzWebAppCertificate'</span></span>
    - <span data-ttu-id="76011-178">'Remove-AzWebAppCertificate'</span><span class="sxs-lookup"><span data-stu-id="76011-178">'Remove-AzWebAppCertificate'</span></span>
* <span data-ttu-id="76011-179">'Set-AzWebApp' 및 'Set-AzWebAppSlot'의 앱 설정에서 Docker 암호가 제거되는 문제 해결</span><span class="sxs-lookup"><span data-stu-id="76011-179">Fixed issue that causes Docker Password to be removed from appsettings in 'Set-AzWebApp' and 'Set-AzWebAppSlot'</span></span>

### <a name="thanks-to-our-community-contributors"></a><span data-ttu-id="76011-180">커뮤니티 기여자에게 감사드립니다.</span><span class="sxs-lookup"><span data-stu-id="76011-180">Thanks to our community contributors</span></span>
* <span data-ttu-id="76011-181">Ivan Akcheurov(@ivanakcheurov), Set-AzSecurityWorkspaceSetting.md 업데이트(#13877)</span><span class="sxs-lookup"><span data-stu-id="76011-181">Ivan Akcheurov (@ivanakcheurov), Update Set-AzSecurityWorkspaceSetting.md (#13877)</span></span>
* <span data-ttu-id="76011-182">@javiermarasco, 예제 업데이트(#13837)</span><span class="sxs-lookup"><span data-stu-id="76011-182">@javiermarasco, Update example (#13837)</span></span>
* <span data-ttu-id="76011-183">@jhaprakash26, Set-AzVirtualNetwork.md 업데이트(#13857)</span><span class="sxs-lookup"><span data-stu-id="76011-183">@jhaprakash26, Update Set-AzVirtualNetwork.md (#13857)</span></span>
* <span data-ttu-id="76011-184">Michael Holmes(@MichaelHolmesWP), New-AzStorageTableStoredAccessPolicy.md 업데이트(#13871)</span><span class="sxs-lookup"><span data-stu-id="76011-184">Michael Holmes (@MichaelHolmesWP), Update New-AzStorageTableStoredAccessPolicy.md (#13871)</span></span>
* <span data-ttu-id="76011-185">Michael James(@mikejwhat), Get-AzLogicAppTriggerHistory 및 Get-AzLogicAppRunAction이 30개 이상의 결과를 반환하도록 허용(#13846)</span><span class="sxs-lookup"><span data-stu-id="76011-185">Michael James (@mikejwhat), Allow Get-AzLogicAppTriggerHistory and Get-AzLogicAppRunAction to return more than 30 results (#13846)</span></span>
* <span data-ttu-id="76011-186">@Willem-J-an, Set-AzWebApp(슬롯)의 appsettings에서 Docker 암호가 제거되는 버그 수정(#13866)</span><span class="sxs-lookup"><span data-stu-id="76011-186">@Willem-J-an, Fix bug causing Docker Password to be removed from appsettings in Set-AzWebApp(Slot) (#13866)</span></span>

## <a name="530---december-2020"></a><span data-ttu-id="76011-187">5.3.0 - 2020년 12월</span><span class="sxs-lookup"><span data-stu-id="76011-187">5.3.0 - December 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="76011-188">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="76011-188">Az.Accounts</span></span>
* <span data-ttu-id="76011-189">Windows PowerShell에서 Http 프록시가 적용되지 않는 문제 해결[#13647]</span><span class="sxs-lookup"><span data-stu-id="76011-189">Fixed the issue that Http proxy is not respected in Windows PowerShell [#13647]</span></span>
* <span data-ttu-id="76011-190">생성된 모듈에서 장기 실행 작업의 디버그 로그 개선</span><span class="sxs-lookup"><span data-stu-id="76011-190">Improved debug log of long running operations in generated modules</span></span>

#### <a name="azautomation"></a><span data-ttu-id="76011-191">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="76011-191">Az.Automation</span></span>
* <span data-ttu-id="76011-192">'Start-AzAutomationRunbook'의 매개 변수가 PSObject 래핑된 문자열을 JSON 문자열로 변환할 수 없는 문제 해결[#13240]</span><span class="sxs-lookup"><span data-stu-id="76011-192">Fixed issue that parameters of 'Start-AzAutomationRunbook' cannot convert PSObject wrapped string to JSON string [#13240]</span></span>
* <span data-ttu-id="76011-193">New-AzAutomationUpdateManagementAzureQuery cmdlet에 대한 위치 완성기 수정</span><span class="sxs-lookup"><span data-stu-id="76011-193">Fixed location completer for New-AzAutomationUpdateManagementAzureQuery cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="76011-194">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="76011-194">Az.Compute</span></span>
* <span data-ttu-id="76011-195">새 매개 변수 집합 'VMParameterSet'의 새 매개 변수 'VM'이 'Get-AzVMDscExtensionStatus' 및 'Get-AzVMDscExtension' cmdlet에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-195">New parameter 'VM' in new parameter set 'VMParameterSet' added to 'Get-AzVMDscExtensionStatus' and 'Get-AzVMDscExtension' cmdlets.</span></span> 

#### <a name="azdatabricks"></a><span data-ttu-id="76011-196">Az.Databricks</span><span class="sxs-lookup"><span data-stu-id="76011-196">Az.Databricks</span></span>
* <span data-ttu-id="76011-197">'New-AzDatabricksVNetPeering'이 완전히 프로비저닝되기 전에 반환될 수 있는 문제 해결(https://github.com/Azure/autorest.powershell/issues/610)</span><span class="sxs-lookup"><span data-stu-id="76011-197">Fixed an issue that may cause 'New-AzDatabricksVNetPeering' to return before it is fully provisioned (https://github.com/Azure/autorest.powershell/issues/610)</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="76011-198">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="76011-198">Az.DataFactory</span></span>
* <span data-ttu-id="76011-199">SupportsShouldProcess 문제에 대해 'Invoke-AzDataFactoryV2Pipeline' 명령 수정</span><span class="sxs-lookup"><span data-stu-id="76011-199">Fixed the command 'Invoke-AzDataFactoryV2Pipeline' for SupportsShouldProcess issue</span></span>

#### <a name="azdesktopvirtualization"></a><span data-ttu-id="76011-200">Az.DesktopVirtualization</span><span class="sxs-lookup"><span data-stu-id="76011-200">Az.DesktopVirtualization</span></span>
* <span data-ttu-id="76011-201">호스트 풀에 StartVMOnConnect 속성을 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-201">Added StartVMOnConnect property to hostpool.</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="76011-202">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="76011-202">Az.HDInsight</span></span>
* <span data-ttu-id="76011-203">추가된 속성: AzureHDInsightHostInfo 클래스의 Fqdn 및 EffectiveDiskEncryptionKeyUrl.</span><span class="sxs-lookup"><span data-stu-id="76011-203">Added properties: Fqdn and EffectiveDiskEncryptionKeyUrl in the class AzureHDInsightHostInfo.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="76011-204">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="76011-204">Az.KeyVault</span></span>
* <span data-ttu-id="76011-205">비밀을 일반 텍스트로 직접 반환하기 위해 'Get-AzKeyVaultSecret'에 새 매개 변수 '-AsPlainText' 추가[#13630]</span><span class="sxs-lookup"><span data-stu-id="76011-205">Added a new parameter '-AsPlainText' to 'Get-AzKeyVaultSecret' to directly return the secret in plain text [#13630]</span></span>
* <span data-ttu-id="76011-206">관리되는 HSM 전체 백업에서 키 선택적 복원 지원[#13526]</span><span class="sxs-lookup"><span data-stu-id="76011-206">Supported selective restore a key from a managed HSM full backup [#13526]</span></span>
* <span data-ttu-id="76011-207">일부 사소한 문제 해결[#13583] [#13584]</span><span class="sxs-lookup"><span data-stu-id="76011-207">Fixed some minor issues [#13583] [#13584]</span></span>
* <span data-ttu-id="76011-208">SecretManagement 모듈에서 'Get-Secret'의 누락된 반환 개체 추가</span><span class="sxs-lookup"><span data-stu-id="76011-208">Added missing return objects of 'Get-Secret' in SecretManagement module</span></span>
* <span data-ttu-id="76011-209">기본 액세스 정책 없이 자격 증명 모음이 만들어질 수 있는 문제 해결[#13687]</span><span class="sxs-lookup"><span data-stu-id="76011-209">Fixed an issue that may cause vault to be created without default access policy [#13687]</span></span>

#### <a name="azkusto"></a><span data-ttu-id="76011-210">Az.Kusto</span><span class="sxs-lookup"><span data-stu-id="76011-210">Az.Kusto</span></span>
* <span data-ttu-id="76011-211">API 버전이 2020-09-18로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-211">Updated API version to 2020-09-18.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="76011-212">Az.Network</span><span class="sxs-lookup"><span data-stu-id="76011-212">Az.Network</span></span>
* <span data-ttu-id="76011-213">ExpressRouteCircuit 시나리오에서 피어링 및 연결 cmdlet 제거 문제 해결</span><span class="sxs-lookup"><span data-stu-id="76011-213">Fixed issue in remove peering and connection cmdlet for ExpressRouteCircuit scenario</span></span>
    - <span data-ttu-id="76011-214">'Remove-AzExpressRouteCircuitPeeringConfig' 및 'Remove-AzExpressRouteCircuitConnectionConfig'</span><span class="sxs-lookup"><span data-stu-id="76011-214">'Remove-AzExpressRouteCircuitPeeringConfig' and 'Remove-AzExpressRouteCircuitConnectionConfig'</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="76011-215">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="76011-215">Az.PolicyInsights</span></span>
* <span data-ttu-id="76011-216">Get-AzPolicyState에 대해 페이지를 매긴 결과를 반환하기 위한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="76011-216">Added support for returning paginated results for Get-AzPolicyState</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="76011-217">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="76011-217">Az.RecoveryServices</span></span>
* <span data-ttu-id="76011-218">SQL에 대해 일시 삭제 기능을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-218">Enabled softdelete feature for SQL.</span></span>
* <span data-ttu-id="76011-219">SQL AG 복원이 수정되었고 컨테이너 이름 확인이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-219">Fixed SQL AG restore and removed the container name check.</span></span>
* <span data-ttu-id="76011-220">Azure Files 백업 항목에 대한 컨테이너 이름 형식을 변경했습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-220">Changed container name format for Azure Files backup item.</span></span>
* <span data-ttu-id="76011-221">복구 서비스 자격 증명 모음에 대한 CMK 기능 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-221">Added CMK feature support for Recovery services vault.</span></span>

#### <a name="azresources"></a><span data-ttu-id="76011-222">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="76011-222">Az.Resources</span></span>
* <span data-ttu-id="76011-223">'New-AzureManagedApplication' 및 'Set-AzureManagedApplication'에서 NullRef 예외 문제를 해결했습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-223">Fixed a NullRef exception issue in 'New-AzureManagedApplication' and 'Set-AzureManagedApplication'.</span></span>
* <span data-ttu-id="76011-224">Azure Resource Manager SDK를 업데이트하여 최신 DeploymentScripts GA api-version: 2020-10-01을 사용하도록 했습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-224">Updated Azure Resource Manager SDK to use latest DeploymentScripts GA api-version: 2020-10-01.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="76011-225">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="76011-225">Az.ServiceFabric</span></span>
* <span data-ttu-id="76011-226">'Add-AzServiceFabricNodeType'을 수정했습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-226">Fixed 'Add-AzServiceFabricNodeType'.</span></span> <span data-ttu-id="76011-227">가상 머신 확장 집합을 만들기 전에 서비스 패브릭 클러스터에 노드 유형을 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-227">Added node type to service fabric cluster before creating virtual machine scale set.</span></span>

#### <a name="azsql"></a><span data-ttu-id="76011-228">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="76011-228">Az.Sql</span></span>
* <span data-ttu-id="76011-229">'InstanceFailoverGroup' 명령에 대한 매개 변수 설명을 수정했습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-229">Fixed parameter description for 'InstanceFailoverGroup' command.</span></span>
* <span data-ttu-id="76011-230">SQL 데이터 분류 명령의 ID에서 schemaName, tableName 및 columnName이 추출되는 논리를 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-230">Updated the logic in which schemaName, tableName and columnName are being extracted from the id of SQL Data Classification commands.</span></span>
* <span data-ttu-id="76011-231">문서를 준수하도록 'Get-AzSqlDatabaseImportExportStatus'의 Status 및 StatusMessage 필드 수정</span><span class="sxs-lookup"><span data-stu-id="76011-231">Fixed Status and StatusMessage fields in 'Get-AzSqlDatabaseImportExportStatus' to conform to documentation</span></span>
* <span data-ttu-id="76011-232">다음의 Microsoft 지원 작업(DevOps) 감사 cmdlet 추가: Get-AzSqlServerMSSupportAudit, Set-AzSqlServerMSSupportAudit, Remove-AzSqlServerMSSupportAudit</span><span class="sxs-lookup"><span data-stu-id="76011-232">Added Microsoft support operations (DevOps) auditing cmdlets: Get-AzSqlServerMSSupportAudit, Set-AzSqlServerMSSupportAudit, Remove-AzSqlServerMSSupportAudit</span></span>

#### <a name="azstorage"></a><span data-ttu-id="76011-233">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="76011-233">Az.Storage</span></span>
* <span data-ttu-id="76011-234">스토리지 계정의 EncryptionScope 생성/업데이트/가져오기/나열 지원</span><span class="sxs-lookup"><span data-stu-id="76011-234">Supported create/update/get/list EncryptionScope of a Storage account</span></span>
    - <span data-ttu-id="76011-235">'New-AzStorageEncryptionScope'</span><span class="sxs-lookup"><span data-stu-id="76011-235">'New-AzStorageEncryptionScope'</span></span>
    - <span data-ttu-id="76011-236">'Update-AzStorageEncryptionScope'</span><span class="sxs-lookup"><span data-stu-id="76011-236">'Update-AzStorageEncryptionScope'</span></span>
    - <span data-ttu-id="76011-237">'Get-AzStorageEncryptionScope'</span><span class="sxs-lookup"><span data-stu-id="76011-237">'Get-AzStorageEncryptionScope'</span></span>
* <span data-ttu-id="76011-238">암호화 범위 설정으로 컨테이너 만들기 및 Blob 업로드 지원</span><span class="sxs-lookup"><span data-stu-id="76011-238">Supported create container and upload blob with Encryption Scope setting</span></span>
    - <span data-ttu-id="76011-239">'New-AzRmStorageContainer'</span><span class="sxs-lookup"><span data-stu-id="76011-239">'New-AzRmStorageContainer'</span></span>
    - <span data-ttu-id="76011-240">'New-AzStorageContainer'</span><span class="sxs-lookup"><span data-stu-id="76011-240">'New-AzStorageContainer'</span></span>
    - <span data-ttu-id="76011-241">'Set-AzStorageBlobContent'</span><span class="sxs-lookup"><span data-stu-id="76011-241">'Set-AzStorageBlobContent'</span></span>

### <a name="thanks-to-our-community-contributors"></a><span data-ttu-id="76011-242">커뮤니티 기여자에게 감사드립니다.</span><span class="sxs-lookup"><span data-stu-id="76011-242">Thanks to our community contributors</span></span>
* <span data-ttu-id="76011-243">Andreas Wolter(@AndreasWolter), 마케팅 언어 제거, 예제 필터 개선(#13671)</span><span class="sxs-lookup"><span data-stu-id="76011-243">Andreas Wolter (@AndreasWolter), removed marketing language, better example filter (#13671)</span></span>
* <span data-ttu-id="76011-244">Tidjani Belmansour(@BelRarr), Get-AzBillingInvoice.md 업데이트(#13634)</span><span class="sxs-lookup"><span data-stu-id="76011-244">Tidjani Belmansour (@BelRarr), Update Get-AzBillingInvoice.md (#13634)</span></span>
* <span data-ttu-id="76011-245">David Klempfner(@DavidKlempfner)</span><span class="sxs-lookup"><span data-stu-id="76011-245">David Klempfner (@DavidKlempfner)</span></span>
  * <span data-ttu-id="76011-246">맞춤법 오류 수정(#13677)</span><span class="sxs-lookup"><span data-stu-id="76011-246">Fixed spelling mistake (#13677)</span></span>
  * <span data-ttu-id="76011-247">PSMetricNoDetails.cs 업데이트(#13676)</span><span class="sxs-lookup"><span data-stu-id="76011-247">Update PSMetricNoDetails.cs (#13676)</span></span>
* <span data-ttu-id="76011-248">@kilobyte97, 구성을 삭제하기 위해 cmdlet 제거에 대한 버그 수정(#13655)</span><span class="sxs-lookup"><span data-stu-id="76011-248">@kilobyte97, bugfix for remove cmdlet to delete config (#13655)</span></span>
* <span data-ttu-id="76011-249">@kongou-ae, Set-AzFirewall.md 업데이트(#13727)</span><span class="sxs-lookup"><span data-stu-id="76011-249">@kongou-ae, Update Set-AzFirewall.md (#13727)</span></span>
* <span data-ttu-id="76011-250">@MasterKuat, 설명서의 제목과 코드 간 스왑 수정(#13666)</span><span class="sxs-lookup"><span data-stu-id="76011-250">@MasterKuat, Fix swap between title and code in documentation (#13666)</span></span>
* <span data-ttu-id="76011-251">NickT(@nukeulis), Set-AzContext.md 업데이트(#13702)</span><span class="sxs-lookup"><span data-stu-id="76011-251">NickT (@nukeulis), Update Set-AzContext.md (#13702)</span></span>
* <span data-ttu-id="76011-252">@PaulHCode, Start-AzJitNetworkAccessPolicy.md 업데이트 - 시연 중인 cmdlet이 적절하게 표시되도록 예제 수정(#13713)</span><span class="sxs-lookup"><span data-stu-id="76011-252">@PaulHCode, Update Start-AzJitNetworkAccessPolicy.md - Fix the Example to display the proper cmdlet being demonstrated (#13713)</span></span>
* <span data-ttu-id="76011-253">Ryan Borstelmann (@ryanborMSFT), 구독 ID 제거(#13715)</span><span class="sxs-lookup"><span data-stu-id="76011-253">Ryan Borstelmann (@ryanborMSFT), Removed Subscription ID (#13715)</span></span>
* <span data-ttu-id="76011-254">Shashikant Shakya (@shshakya), Set-AzSqlDatabase.md 업데이트(#13674)</span><span class="sxs-lookup"><span data-stu-id="76011-254">Shashikant Shakya (@shshakya), Update Set-AzSqlDatabase.md (#13674)</span></span>
* <span data-ttu-id="76011-255">Sebastian Olsen(@Spacebjorn), Get-AzRecoveryServicesBackupItem.md 업데이트(#13719)</span><span class="sxs-lookup"><span data-stu-id="76011-255">Sebastian Olsen (@Spacebjorn), Update Get-AzRecoveryServicesBackupItem.md (#13719)</span></span>

## <a name="520---december-2020"></a><span data-ttu-id="76011-256">5.2.0 - 2020년 12월</span><span class="sxs-lookup"><span data-stu-id="76011-256">5.2.0 - December 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="76011-257">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="76011-257">Az.Accounts</span></span>
* <span data-ttu-id="76011-258">기본 라이브러리에서 가져올 수 없는 경우 원시 토큰에서 ExpiresOn 시간을 구문 분석하도록 관리됨</span><span class="sxs-lookup"><span data-stu-id="76011-258">Managed to parse ExpiresOn time from raw token if could not get from underlying library</span></span>
* <span data-ttu-id="76011-259">대화형 인증을 사용할 수 없는 경우 경고 메시지 향상됨</span><span class="sxs-lookup"><span data-stu-id="76011-259">Improved warning message if Interactive authentication is unavailable</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="76011-260">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="76011-260">Az.ApiManagement</span></span>
* <span data-ttu-id="76011-261">[호환성이 손상되는 변경] 기본적으로 'New-AzApiManagementProduct'는 구독 제한이 없습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-261">[Breaking change] 'New-AzApiManagementProduct' by default has no subscription limit.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="76011-262">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="76011-262">Az.Compute</span></span>
* <span data-ttu-id="76011-263">너무 많은 리소스로 인한 제한을 확인하기 전에 '-Name'으로 필터링하도록 Get-AzVm을 편집했습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-263">Edited Get-AzVm to filter by '-Name' prior to checking for throttling due to too many resources.</span></span> 
* <span data-ttu-id="76011-264">새 cmdlet 'Start-AzVmssRollingExtensionUpgrade'.</span><span class="sxs-lookup"><span data-stu-id="76011-264">New cmdlet 'Start-AzVmssRollingExtensionUpgrade'.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="76011-265">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="76011-265">Az.ContainerRegistry</span></span>
* <span data-ttu-id="76011-266">'Get-AzContainerRegistryUsage'에 대한 파이프라인 입력 및 값에 대해 'Name' 매개 변수 지원됨 [#13605]</span><span class="sxs-lookup"><span data-stu-id="76011-266">Supported parameter 'Name' for and value from pipeline input for 'Get-AzContainerRegistryUsage' [#13605]</span></span>
* <span data-ttu-id="76011-267">'Connect-AzContainerRegistry'에 대한 예외 수정됨</span><span class="sxs-lookup"><span data-stu-id="76011-267">Polished exceptions for 'Connect-AzContainerRegistry'</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="76011-268">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="76011-268">Az.DataFactory</span></span>
* <span data-ttu-id="76011-269">ADF .Net SDK 버전이 4.13.0으로 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="76011-269">Updated ADF .Net SDK version to 4.13.0</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="76011-270">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="76011-270">Az.HealthcareApis</span></span>
* <span data-ttu-id="76011-271">고객 관리형 키에 대한 지원 추가됨</span><span class="sxs-lookup"><span data-stu-id="76011-271">Added support for customer managed keys</span></span>

#### <a name="aziothub"></a><span data-ttu-id="76011-272">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="76011-272">Az.IotHub</span></span>
* <span data-ttu-id="76011-273">SAS 토큰의 문제가 해결되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-273">Fixed an issue of SAS token.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="76011-274">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="76011-274">Az.KeyVault</span></span>
* <span data-ttu-id="76011-275">키 자격 증명 모음 액세스 정책 설정 시 'all'이 옵션으로 지원됨</span><span class="sxs-lookup"><span data-stu-id="76011-275">Supported 'all' as an option when setting key vault access policies</span></span>
* <span data-ttu-id="76011-276">새 버전의 SecretManagement 모듈 지원됨 [#13366]</span><span class="sxs-lookup"><span data-stu-id="76011-276">Supported new version of SecretManagement module [#13366]</span></span>
* <span data-ttu-id="76011-277">SecretManagementModule의 'SecretValue'에 대해 ByteArray, String, PSCredential 및 Hashtable 지원됨 [#12190]</span><span class="sxs-lookup"><span data-stu-id="76011-277">Supported ByteArray, String, PSCredential and Hashtable for 'SecretValue' in SecretManagementModule [#12190]</span></span>
* <span data-ttu-id="76011-278">[호환성이 손상되는 변경] 관리형 HSM과 관련된 cmdlet의 API 표면을 다시 디자인했습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-278">[Breaking change] redesigned the API surface of cmdlets related to managed HSM.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="76011-279">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="76011-279">Az.Monitor</span></span>
* <span data-ttu-id="76011-280">'New-AzAutoscaleProfile'의 'Rule' 매개 변수가 빈 목록을 허용하도록 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-280">Changed parameter 'Rule' of 'New-AzAutoscaleProfile' to accept empty list.</span></span> <span data-ttu-id="76011-281">[#12903]</span><span class="sxs-lookup"><span data-stu-id="76011-281">[#12903]</span></span>
* <span data-ttu-id="76011-282">진단 설정을 보다 유연하게 만들 수 있도록 다음과 같은 새 cmdlet 추가됨</span><span class="sxs-lookup"><span data-stu-id="76011-282">Added new cmdlets to support creating diagnostic settings more flexible:</span></span>
    * <span data-ttu-id="76011-283">'Get-AzDiagnosticSettingCategory'</span><span class="sxs-lookup"><span data-stu-id="76011-283">'Get-AzDiagnosticSettingCategory'</span></span>
    * <span data-ttu-id="76011-284">'New-AzDiagnosticSetting'</span><span class="sxs-lookup"><span data-stu-id="76011-284">'New-AzDiagnosticSetting'</span></span>
    * <span data-ttu-id="76011-285">'New-AzDiagnosticDetailSetting'</span><span class="sxs-lookup"><span data-stu-id="76011-285">'New-AzDiagnosticDetailSetting'</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="76011-286">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="76011-286">Az.RecoveryServices</span></span>
* <span data-ttu-id="76011-287">도움말 텍스트 및 매개 변수 집합 이름이 'Restore-AzRecoveryServicesBackupItem' cmdlet으로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-287">Made help text and parameter set name changes to 'Restore-AzRecoveryServicesBackupItem' cmdlet.</span></span>

#### <a name="azresources"></a><span data-ttu-id="76011-288">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="76011-288">Az.Resources</span></span>
* <span data-ttu-id="76011-289">'Set-AzTemplateSpec' 및 'New-AzTemplateSpec'에 '-Tag' 매개 변수 지원 추가됨</span><span class="sxs-lookup"><span data-stu-id="76011-289">Added '-Tag' parameter support to 'Set-AzTemplateSpec' and 'New-AzTemplateSpec'</span></span>
* <span data-ttu-id="76011-290">템플릿 사양에 대한 기본 포맷터에 Tag 표시 지원 추가됨</span><span class="sxs-lookup"><span data-stu-id="76011-290">Added Tag display support to default formatter for Template Specs</span></span> 

#### <a name="azservicefabric"></a><span data-ttu-id="76011-291">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="76011-291">Az.ServiceFabric</span></span>
* <span data-ttu-id="76011-292">SettingsSectionDescription 매개 변수를 사용하여 'Set-AzServiceFabricSetting'에 예가 추가됨</span><span class="sxs-lookup"><span data-stu-id="76011-292">Added example to 'Set-AzServiceFabricSetting' with SettingsSectionDescription param</span></span>
* <span data-ttu-id="76011-293">ARM 배포 리소스에 대해서만 지원됨을 알리도록 애플리케이션 관련 cmdlet 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="76011-293">Updated application related cmdlets to call out that support is only for ARM deployed resources</span></span>
* <span data-ttu-id="76011-294">사용 중단 클러스터 인증서 cmdlet 'Add-AzureRmServiceFabricClusterCertificate' 및 'Remove-AzureRmServiceFabricClusterCertificate'로 표시됨</span><span class="sxs-lookup"><span data-stu-id="76011-294">Marked for deprecation cluster cert cmdlets 'Add-AzureRmServiceFabricClusterCertificate' and 'Remove-AzureRmServiceFabricClusterCertificate'</span></span>

#### <a name="azsql"></a><span data-ttu-id="76011-295">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="76011-295">Az.Sql</span></span>
* <span data-ttu-id="76011-296">SecondaryType이 다음에 추가됨</span><span class="sxs-lookup"><span data-stu-id="76011-296">Added SecondaryType to the following:</span></span> 
    - <span data-ttu-id="76011-297">'New-AzSqlDatabase'</span><span class="sxs-lookup"><span data-stu-id="76011-297">'New-AzSqlDatabase'</span></span>
    - <span data-ttu-id="76011-298">'Set-AzSqlDatabase'</span><span class="sxs-lookup"><span data-stu-id="76011-298">'Set-AzSqlDatabase'</span></span>
    - <span data-ttu-id="76011-299">'New-AzSqlDatabaseSecondary'</span><span class="sxs-lookup"><span data-stu-id="76011-299">'New-AzSqlDatabaseSecondary'</span></span>
* <span data-ttu-id="76011-300">HighAvailabilityReplicaCount가 다음에 추가됨</span><span class="sxs-lookup"><span data-stu-id="76011-300">Added HighAvailabilityReplicaCount to the following:</span></span> 
    - <span data-ttu-id="76011-301">'New-AzSqlDatabase'</span><span class="sxs-lookup"><span data-stu-id="76011-301">'New-AzSqlDatabase'</span></span>
    - <span data-ttu-id="76011-302">'Set-AzSqlDatabase'</span><span class="sxs-lookup"><span data-stu-id="76011-302">'Set-AzSqlDatabase'</span></span>
* <span data-ttu-id="76011-303">다음에서 HighAvailabilityReplicaCount의 별칭을 ReadReplicaCount로 지정됨</span><span class="sxs-lookup"><span data-stu-id="76011-303">Made ReadReplicaCount an alias of HighAvailabilityReplicaCount in the following:</span></span> 
    - <span data-ttu-id="76011-304">'New-AzSqlDatabase'</span><span class="sxs-lookup"><span data-stu-id="76011-304">'New-AzSqlDatabase'</span></span>
    - <span data-ttu-id="76011-305">'Set-AzSqlDatabase'</span><span class="sxs-lookup"><span data-stu-id="76011-305">'Set-AzSqlDatabase'</span></span>

#### <a name="azstorage"></a><span data-ttu-id="76011-306">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="76011-306">Az.Storage</span></span>
* <span data-ttu-id="76011-307">최대 4TiB까지 Azure 파일 업로드 지원됨</span><span class="sxs-lookup"><span data-stu-id="76011-307">Supported upload Azure File size up to 4 TiB</span></span>
    - <span data-ttu-id="76011-308">'Set-AzStorageFileContent'</span><span class="sxs-lookup"><span data-stu-id="76011-308">'Set-AzStorageFileContent'</span></span>
* <span data-ttu-id="76011-309">Azure.Storage.Blobs를 12.7.0으로 업그레이드</span><span class="sxs-lookup"><span data-stu-id="76011-309">Upgraded Azure.Storage.Blobs to 12.7.0</span></span>
* <span data-ttu-id="76011-310">Azure.Storage.Files.Shares를 12.5.0으로 업그레이드</span><span class="sxs-lookup"><span data-stu-id="76011-310">Upgraded Azure.Storage.Files.Shares to 12.5.0</span></span>
* <span data-ttu-id="76011-311">Azure.Storage.Files.DataLake를 12.5.0으로 업그레이드</span><span class="sxs-lookup"><span data-stu-id="76011-311">Upgraded Azure.Storage.Files.DataLake to 12.5.0</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="76011-312">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="76011-312">Az.StorageSync</span></span>
* <span data-ttu-id="76011-313">다운로드 정책 및 로컬 캐시 모드가 포함된 동기화 계층화 정책 기능 추가됨</span><span class="sxs-lookup"><span data-stu-id="76011-313">Added Sync tiering policy feature with download policy and local cache mode</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="76011-314">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="76011-314">Az.Websites</span></span>
* <span data-ttu-id="76011-315">중복 액세스 제한 규칙 방지</span><span class="sxs-lookup"><span data-stu-id="76011-315">Prevent duplicate access restriction rules</span></span>

### <a name="thanks-to-our-community-contributors"></a><span data-ttu-id="76011-316">커뮤니티 기여자에게 감사드립니다.</span><span class="sxs-lookup"><span data-stu-id="76011-316">Thanks to our community contributors</span></span>
* <span data-ttu-id="76011-317">Andrew Dawson(@dawsonar802), Get-AzKeyVaultCertificate.md 업데이트 - 인증서를 가져와서 PowerShell Core에서 작동하도록 pfx 섹션으로 저장(#13557)</span><span class="sxs-lookup"><span data-stu-id="76011-317">Andrew Dawson (@dawsonar802), Update Get-AzKeyVaultCertificate.md - Get cert and save it as pfx section to work with PowerShell Core (#13557)</span></span>
* <span data-ttu-id="76011-318">@iviark, 의료 API Powershell BYOK 업데이트(#13518)</span><span class="sxs-lookup"><span data-stu-id="76011-318">@iviark, Healthcare APIs Powershell BYOK Updates (#13518)</span></span>
* <span data-ttu-id="76011-319">John Duckmanton(@johnduckmanton) TagPatchOperation의 철자 수정(#13508)</span><span class="sxs-lookup"><span data-stu-id="76011-319">John Duckmanton (@johnduckmanton), Correct spelling of TagPatchOperation (#13508)</span></span>
* <span data-ttu-id="76011-320">Michael James(@mikejwhat)</span><span class="sxs-lookup"><span data-stu-id="76011-320">Michael James (@mikejwhat)</span></span>
  * <span data-ttu-id="76011-321">AzLogicAppRunHistory 도움말 정리(#13513)</span><span class="sxs-lookup"><span data-stu-id="76011-321">Get-AzLogicAppRunHistory Help Tidy (#13513)</span></span>
* <span data-ttu-id="76011-322">Richard de Zwart(@mountain65)</span><span class="sxs-lookup"><span data-stu-id="76011-322">Richard de Zwart (@mountain65)</span></span>
  * <span data-ttu-id="76011-323">Update-AzAppConfigurationStore.md 업데이트(#13485)</span><span class="sxs-lookup"><span data-stu-id="76011-323">Update Update-AzAppConfigurationStore.md (#13485)</span></span>
  * <span data-ttu-id="76011-324">New-AzCosmosDBAccount.md 업데이트(#13490)</span><span class="sxs-lookup"><span data-stu-id="76011-324">Update New-AzCosmosDBAccount.md (#13490)</span></span>
* <span data-ttu-id="76011-325">@SteppingRazor, New-AzApiManagementProduct: SubscriptionsLimit 매개 변수 기본값을 None으로 변경(#13457)</span><span class="sxs-lookup"><span data-stu-id="76011-325">@SteppingRazor, New-AzApiManagementProduct: Change SubscriptionsLimit parameter default value to None (#13457)</span></span>
* <span data-ttu-id="76011-326">Steve Burkett(@SteveBurkettNZ), 예에서 WorkspaceResourceId 매개 변수의 오타 수정(#13589).</span><span class="sxs-lookup"><span data-stu-id="76011-326">Steve Burkett (@SteveBurkettNZ), Fix Typo for WorkspaceResourceId parameter in example (#13589)</span></span>

## <a name="510---november-2020"></a><span data-ttu-id="76011-327">5.1.0 - 2020년 11월</span><span class="sxs-lookup"><span data-stu-id="76011-327">5.1.0 - November 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="76011-328">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="76011-328">Az.Accounts</span></span>
* <span data-ttu-id="76011-329">'Connect-AzAccount -DeviceCode'를 사용하는 경우 TenantId가 적용되지 않을 수 있는 문제가 해결됨 [#13477]</span><span class="sxs-lookup"><span data-stu-id="76011-329">Fixed an issue that TenantId may be not respected if using 'Connect-AzAccount -DeviceCode'[#13477]</span></span>
* <span data-ttu-id="76011-330">새 cmdlet 'Get-AzAccessToken'이 추가됨</span><span class="sxs-lookup"><span data-stu-id="76011-330">Added new cmdlet 'Get-AzAccessToken'</span></span>
* <span data-ttu-id="76011-331">사용자 프로필 경로에 액세스할 수 없는 경우 오류가 발생하는 문제가 해결됨</span><span class="sxs-lookup"><span data-stu-id="76011-331">Fixed an issue that error happens if user profile path is inaccessible</span></span>
* <span data-ttu-id="76011-332">Connect-AzAccount 중에 쓰기-개체 오류가 발생하는 문제가 해결됨 [#13419]</span><span class="sxs-lookup"><span data-stu-id="76011-332">Fixed an issue causing Write-Object error during Connect-AzAccount [#13419]</span></span>
* <span data-ttu-id="76011-333">'ContainerRegistryEndpointSuffix' 매개 변수가 'Add-AzEnvironment' 및 'Set-AzEnvironment'에 추가됨</span><span class="sxs-lookup"><span data-stu-id="76011-333">Added parameter 'ContainerRegistryEndpointSuffix' to: 'Add-AzEnvironment', 'Set-AzEnvironment'</span></span> 
* <span data-ttu-id="76011-334"><kbd>CTRL</kbd>+<kbd>C</kbd> 키를 눌러 로그인을 중단하는 기능이 지원됨</span><span class="sxs-lookup"><span data-stu-id="76011-334">Supported interrupting login by hitting <kbd>CTRL</kbd>+<kbd>C</kbd></span></span>
* <span data-ttu-id="76011-335">'Connect-AzAccount -KeyVaultAccessToken'이 작동하지 않는 문제가 해결됨 [#13127]</span><span class="sxs-lookup"><span data-stu-id="76011-335">Fixed an issue causing 'Connect-AzAccount -KeyVaultAccessToken' not working [#13127]</span></span>
* <span data-ttu-id="76011-336">'Invoke-AzRestMethod'에서 null 참조 및 메서드 대/소문자를 구분하지 않는 문제가 해결됨</span><span class="sxs-lookup"><span data-stu-id="76011-336">Fixed null reference and method case insensitive in 'Invoke-AzRestMethod'</span></span>

#### <a name="azaks"></a><span data-ttu-id="76011-337">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="76011-337">Az.Aks</span></span>
* <span data-ttu-id="76011-338">사용자가 서비스 주체를 사용하여 새 Kubernetes 클러스터를 만들 수 없는 문제가 해결됨</span><span class="sxs-lookup"><span data-stu-id="76011-338">Fixed the issue that user cannot use service principal to create a new Kubernetes cluster.</span></span> <span data-ttu-id="76011-339">[#13012]</span><span class="sxs-lookup"><span data-stu-id="76011-339">[#13012]</span></span>

#### <a name="azappconfiguration"></a><span data-ttu-id="76011-340">Az.AppConfiguration</span><span class="sxs-lookup"><span data-stu-id="76011-340">Az.AppConfiguration</span></span>
* <span data-ttu-id="76011-341">'Az.AppConfiguration' 모듈의 일반 공급</span><span class="sxs-lookup"><span data-stu-id="76011-341">General availability of 'Az.AppConfiguration' module</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="76011-342">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="76011-342">Az.DataFactory</span></span>
* <span data-ttu-id="76011-343">'New-AzDataFactoryV2LinkedServiceEncryptedCredential' 명령의 오류 메시지가 개선됨</span><span class="sxs-lookup"><span data-stu-id="76011-343">Improved error message of 'New-AzDataFactoryV2LinkedServiceEncryptedCredential' command</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="76011-344">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="76011-344">Az.DataLakeStore</span></span>
* <span data-ttu-id="76011-345">ADLS 데이터 평면 SDK가 1.2.4로 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="76011-345">Updated ADLS dataplane SDK to 1.2.4-alpha.</span></span> <span data-ttu-id="76011-346">변경 내용: https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-124-alpha</span><span class="sxs-lookup"><span data-stu-id="76011-346">Changes:https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-124-alpha</span></span>

#### <a name="azdesktopvirtualization"></a><span data-ttu-id="76011-347">Az.DesktopVirtualization</span><span class="sxs-lookup"><span data-stu-id="76011-347">Az.DesktopVirtualization</span></span>
* <span data-ttu-id="76011-348">새 MSIX 패키지 cmdlet 및 업데이트된 애플리케이션 cmdlet이 추가됨</span><span class="sxs-lookup"><span data-stu-id="76011-348">Added new MSIX Package cmdlets and updated Applications cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="76011-349">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="76011-349">Az.EventHub</span></span>
* <span data-ttu-id="76011-350">태그가 없는 EventHub 클러스터에 대한 클러스터 명령이 수정됨</span><span class="sxs-lookup"><span data-stu-id="76011-350">Fixed Cluster commands for EventHub cluster without tags</span></span>
* <span data-ttu-id="76011-351">AzEventHubGeoDRConfiguration 명령의 PartnerNamespace에 대한 도움말 텍스트가 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="76011-351">Updated help text for PartnerNamespace of AzEventHubGeoDRConfiguration commands</span></span> 

#### <a name="azhdinsight"></a><span data-ttu-id="76011-352">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="76011-352">Az.HDInsight</span></span>
* <span data-ttu-id="76011-353">릴레이 아웃바운드 및 프라이빗 링크 기능을 지원하기 위해 cmdlet 'New-AzHDInsightCluster'에 'ResourceProviderConnection' 및 'PrivateLink' 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="76011-353">Add parameters 'ResourceProviderConnection' and 'PrivateLink' to cmdlet 'New-AzHDInsightCluster' to support relay outbound and private link feature</span></span>
* <span data-ttu-id="76011-354">사용자 지정 Ambari 데이터베이스 기능을 지원하기 위해 cmdlet 'New-AzHDInsightCluster'에 'AmbariDatabase' 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="76011-354">Add parameter 'AmbariDatabase' to cmdlet 'New-AzHDInsightCluster' to support custom Ambari database feature</span></span>
* <span data-ttu-id="76011-355">cmdlet 'Add-AzHDInsightMetastore'의 'MetastoreType' 매개 변수에 accept 값 'AmbariDatabase' 추가</span><span class="sxs-lookup"><span data-stu-id="76011-355">Add accept value 'AmbariDatabase' to the parameter 'MetastoreType' of the cmdlet 'Add-AzHDInsightMetastore'</span></span>

#### <a name="aziothub"></a><span data-ttu-id="76011-356">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="76011-356">Az.IotHub</span></span>
* <span data-ttu-id="76011-357">IoT Hub create cmdlet에서 태그 허용</span><span class="sxs-lookup"><span data-stu-id="76011-357">Allowed tags in IoT Hub create cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="76011-358">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="76011-358">Az.KeyVault</span></span>
* <span data-ttu-id="76011-359">key vault 태그 업데이트 지원</span><span class="sxs-lookup"><span data-stu-id="76011-359">Supported updating key vault tag</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="76011-360">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="76011-360">Az.LogicApp</span></span>
* <span data-ttu-id="76011-361">Get-AzLogicAppRunHistory가 결과의 첫 번째 페이지만 검색하도록 수정됨</span><span class="sxs-lookup"><span data-stu-id="76011-361">Fixed for Get-AzLogicAppRunHistory only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="76011-362">Az.Network</span><span class="sxs-lookup"><span data-stu-id="76011-362">Az.Network</span></span>
* <span data-ttu-id="76011-363">아래 cmdlet이 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="76011-363">Updated below cmdlet</span></span> 
    - <span data-ttu-id="76011-364">'New-AzLoadBalancerFrontendIpConfigCommand', 'Set-AzLoadBalancerFrontendIpConfigCommand', 'Add-AzLoadBalancerFrontendIpConfigCommand':</span><span class="sxs-lookup"><span data-stu-id="76011-364">'New-AzLoadBalancerFrontendIpConfigCommand', 'Set-AzLoadBalancerFrontendIpConfigCommand', 'Add-AzLoadBalancerFrontendIpConfigCommand':</span></span>
        - <span data-ttu-id="76011-365">PublicIpAddressPrefix 속성이 추가됨</span><span class="sxs-lookup"><span data-stu-id="76011-365">Added PublicIpAddressPrefix property</span></span>
        - <span data-ttu-id="76011-366">PublicIpAddressPrefixId 속성이 추가됨</span><span class="sxs-lookup"><span data-stu-id="76011-366">Added PublicIpAddressPrefixId property</span></span>
* <span data-ttu-id="76011-367">글로벌 부하 분산을 허용하도록 다음 cmdlet에 새 속성이 추가됨</span><span class="sxs-lookup"><span data-stu-id="76011-367">Added new properties to the following cmdlets to allow for global load balancing</span></span>
    - <span data-ttu-id="76011-368">'New-AzLoadBalancer':</span><span class="sxs-lookup"><span data-stu-id="76011-368">'New-AzLoadBalancer':</span></span>
        - <span data-ttu-id="76011-369">Sku 계층 속성이 추가됨</span><span class="sxs-lookup"><span data-stu-id="76011-369">Added Sku Tier property</span></span>
    - <span data-ttu-id="76011-370">'New-AzPuplicIpAddress':</span><span class="sxs-lookup"><span data-stu-id="76011-370">'New-AzPuplicIpAddress':</span></span>
        - <span data-ttu-id="76011-371">Sku 계층 속성이 추가됨</span><span class="sxs-lookup"><span data-stu-id="76011-371">Added Sku Tier property</span></span>
    - <span data-ttu-id="76011-372">'New-AzPublicIpPrefix':</span><span class="sxs-lookup"><span data-stu-id="76011-372">'New-AzPublicIpPrefix':</span></span>
        - <span data-ttu-id="76011-373">Sku 계층 속성이 추가됨</span><span class="sxs-lookup"><span data-stu-id="76011-373">Added Sku Tier property</span></span>
    - <span data-ttu-id="76011-374">'New-AzLoadBalancerBackendAddressConfig':</span><span class="sxs-lookup"><span data-stu-id="76011-374">'New-AzLoadBalancerBackendAddressConfig':</span></span>
        - <span data-ttu-id="76011-375">LoadBalancerFrontendIPConfigurationId 속성이 추가됨</span><span class="sxs-lookup"><span data-stu-id="76011-375">Added LoadBalancerFrontendIPConfigurationId property</span></span>
* <span data-ttu-id="76011-376">cmdlet -'New-AzVirtualHubRoute', -'New-AzVirtualHubRouteTable', -'Add-AzVirtualHubRoute', -'Add-AzVirtualHubRouteTable', -'Get-AzVirtualHubRouteTable' 및 -'Remove-AzVirtualHubRouteTable'의 사용 중지 예정 경고가 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="76011-376">Updated planning to deprecate warnings for the following cmdlets   -'New-AzVirtualHubRoute'   -'New-AzVirtualHubRouteTable'   -'Add-AzVirtualHubRoute'   -'Add-AzVirtualHubRouteTable'   -'Get-AzVirtualHubRouteTable'   -'Remove-AzVirtualHubRouteTable'</span></span>
* <span data-ttu-id="76011-377">cmdlet -'New-AzVirtualHub', -'Set-AzVirtualHub' 및 -'Update-AzVirtualHub'에 대한 인수 'RouteTable'의 사용 중지 예정 경고가 추가됨</span><span class="sxs-lookup"><span data-stu-id="76011-377">Added planning to deprecate warnings on the argument 'RouteTable' for the following cmdlets   -'New-AzVirtualHub'   -'Set-AzVirtualHub'   -'Update-AzVirtualHub'</span></span>
* <span data-ttu-id="76011-378">'Set-AzExpressRouteGateway'에서 '-MinScaleUnits' 및 '-MaxScaleUnits' 인수가 선택적 인수로 변경됨</span><span class="sxs-lookup"><span data-stu-id="76011-378">Made arguments '-MinScaleUnits' and '-MaxScaleUnits' optional in 'Set-AzExpressRouteGateway'</span></span>
* <span data-ttu-id="76011-379">Application Gateway에서 상호 인증 및 SSL 프로필을 지원하기 위해 새 cmdlet이 추가됨</span><span class="sxs-lookup"><span data-stu-id="76011-379">Added new cmdlets to support Mutual Authentication and SSL Profiles on Application Gateway</span></span>
    - <span data-ttu-id="76011-380">'Get-AzApplicationGatewayClientAuthConfiguration'</span><span class="sxs-lookup"><span data-stu-id="76011-380">'Get-AzApplicationGatewayClientAuthConfiguration'</span></span>
    - <span data-ttu-id="76011-381">'New-AzApplicationGatewayClientAuthConfiguration'</span><span class="sxs-lookup"><span data-stu-id="76011-381">'New-AzApplicationGatewayClientAuthConfiguration'</span></span>
    - <span data-ttu-id="76011-382">'Remove-AzApplicationGatewayClientAuthConfiguration'</span><span class="sxs-lookup"><span data-stu-id="76011-382">'Remove-AzApplicationGatewayClientAuthConfiguration'</span></span>
    - <span data-ttu-id="76011-383">'Set-AzApplicationGatewayClientAuthConfiguration'</span><span class="sxs-lookup"><span data-stu-id="76011-383">'Set-AzApplicationGatewayClientAuthConfiguration'</span></span>
    - <span data-ttu-id="76011-384">'Add-AzApplicationGatewayTrustedClientCertificate'</span><span class="sxs-lookup"><span data-stu-id="76011-384">'Add-AzApplicationGatewayTrustedClientCertificate'</span></span> 
    - <span data-ttu-id="76011-385">'Get-AzApplicationGatewayTrustedClientCertificate'</span><span class="sxs-lookup"><span data-stu-id="76011-385">'Get-AzApplicationGatewayTrustedClientCertificate'</span></span> 
    - <span data-ttu-id="76011-386">'New-AzApplicationGatewayTrustedClientCertificate'</span><span class="sxs-lookup"><span data-stu-id="76011-386">'New-AzApplicationGatewayTrustedClientCertificate'</span></span> 
    - <span data-ttu-id="76011-387">'Remove-AzApplicationGatewayTrustedClientCertificate'</span><span class="sxs-lookup"><span data-stu-id="76011-387">'Remove-AzApplicationGatewayTrustedClientCertificate'</span></span> 
    - <span data-ttu-id="76011-388">'Set-AzApplicationGatewayTrustedClientCertificate'</span><span class="sxs-lookup"><span data-stu-id="76011-388">'Set-AzApplicationGatewayTrustedClientCertificate'</span></span>
    - <span data-ttu-id="76011-389">'Add-AzApplicationGatewaySslProfile'</span><span class="sxs-lookup"><span data-stu-id="76011-389">'Add-AzApplicationGatewaySslProfile'</span></span>
    - <span data-ttu-id="76011-390">'Get-AzApplicationGatewaySslProfile'</span><span class="sxs-lookup"><span data-stu-id="76011-390">'Get-AzApplicationGatewaySslProfile'</span></span>
    - <span data-ttu-id="76011-391">'New-AzApplicationGatewaySslProfile'</span><span class="sxs-lookup"><span data-stu-id="76011-391">'New-AzApplicationGatewaySslProfile'</span></span>
    - <span data-ttu-id="76011-392">'Remove-AzApplicationGatewaySslProfile'</span><span class="sxs-lookup"><span data-stu-id="76011-392">'Remove-AzApplicationGatewaySslProfile'</span></span>
    - <span data-ttu-id="76011-393">'Set-AzApplicationGatewaySslProfile'</span><span class="sxs-lookup"><span data-stu-id="76011-393">'Set-AzApplicationGatewaySslProfile'</span></span>
    - <span data-ttu-id="76011-394">'Get-AzApplicationGatewaySslProfilePolicy'</span><span class="sxs-lookup"><span data-stu-id="76011-394">'Get-AzApplicationGatewaySslProfilePolicy'</span></span>
    - <span data-ttu-id="76011-395">'Remove-AzApplicationGatewaySslProfilePolicy'</span><span class="sxs-lookup"><span data-stu-id="76011-395">'Remove-AzApplicationGatewaySslProfilePolicy'</span></span>
    - <span data-ttu-id="76011-396">'Set-AzApplicationGatewaySslProfilePolicy'</span><span class="sxs-lookup"><span data-stu-id="76011-396">'Set-AzApplicationGatewaySslProfilePolicy'</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="76011-397">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="76011-397">Az.RecoveryServices</span></span>
* <span data-ttu-id="76011-398">정책 BackupTime은 UTC로 지정.</span><span class="sxs-lookup"><span data-stu-id="76011-398">Specifying policy BackupTime is in UTC.</span></span>
* <span data-ttu-id="76011-399">Get-AzRecoveryServicesBackupJobDetails cmdlet에서 호환성이 손상되는 변경에 대한 경고를 수정하는 중</span><span class="sxs-lookup"><span data-stu-id="76011-399">Modifying breaking change warning in Get-AzRecoveryServicesBackupJobDetails cmdlet.</span></span>
* <span data-ttu-id="76011-400">Set-AzRecoveryServicesBackupProtectionPolicy cmdlet에 대한 샘플 스크립트 도움말 텍스트를 업데이트하는 중</span><span class="sxs-lookup"><span data-stu-id="76011-400">Updating sample script help text for Set-AzRecoveryServicesBackupProtectionPolicy cmdlet.</span></span>

#### <a name="azresources"></a><span data-ttu-id="76011-401">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="76011-401">Az.Resources</span></span>
* <span data-ttu-id="76011-402">가상 도구에서 대/소문자가 서로 다른 두 개의 리소스 그룹 범위를 표시하는 문제가 해결됨</span><span class="sxs-lookup"><span data-stu-id="76011-402">Fixed an issue where What-If shows two resource group scopes with different casing</span></span>
* <span data-ttu-id="76011-403">SDK를 사용하도록 'Export-AzResourceGroup'이 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="76011-403">Updated 'Export-AzResourceGroup' to use the SDK.</span></span>
* <span data-ttu-id="76011-404">구문 분석 메서드에 문화권 정보가 추가됨</span><span class="sxs-lookup"><span data-stu-id="76011-404">Added culture info to parse methods</span></span>

#### <a name="azsql"></a><span data-ttu-id="76011-405">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="76011-405">Az.Sql</span></span>
* <span data-ttu-id="76011-406">Set-AzSqlDatabaseAudit가 하이퍼스케일 데이터베이스를 지원하지 않아 데이터베이스 버전을 확인할 수 없는 문제가 해결됨</span><span class="sxs-lookup"><span data-stu-id="76011-406">Fixed issues where Set-AzSqlDatabaseAudit were not support Hyperscale database and database edition cannot be determined</span></span>
* <span data-ttu-id="76011-407">'New-AzSqlInstance' 및 'Set-AzSqlInstance'에 MaintenanceConfigurationId가 추가됨</span><span class="sxs-lookup"><span data-stu-id="76011-407">Added MaintenanceConfigurationId to 'New-AzSqlInstance' and 'Set-AzSqlInstance'</span></span>
* <span data-ttu-id="76011-408">PartnerServerName 매개 변수가 키가 아닌 값으로 확인되는 GetAzureSqlDatabaseReplicationLink.cs의 버그가 해결됨</span><span class="sxs-lookup"><span data-stu-id="76011-408">Fixed a bug in GetAzureSqlDatabaseReplicationLink.cs where PartnerServerName parameter was being checked for by value instead of key</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="76011-409">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="76011-409">Az.Websites</span></span>
* <span data-ttu-id="76011-410">다음과 같은 새 액세스 제한 기능에 대한 지원이 추가됨: ServiceTag, 다중 ip 및 http 헤더</span><span class="sxs-lookup"><span data-stu-id="76011-410">Added support for new access restriction features: ServiceTag, multi-ip and http-headers</span></span>

### <a name="thanks-to-our-community-contributors"></a><span data-ttu-id="76011-411">커뮤니티 기여자에게 감사드립니다.</span><span class="sxs-lookup"><span data-stu-id="76011-411">Thanks to our community contributors</span></span>
* <span data-ttu-id="76011-412">John Q. Martin(@johnmart82), 방화벽 필수 조건 정보 추가(#13385)</span><span class="sxs-lookup"><span data-stu-id="76011-412">John Q. Martin (@johnmart82), Adding firewall prerequisite information (#13385)</span></span>
* <span data-ttu-id="76011-413">Manikandan Duraisamy(@madurais-msft), PublicSubnetName 인수 수정(#13417)</span><span class="sxs-lookup"><span data-stu-id="76011-413">Manikandan Duraisamy (@madurais-msft), Corrected the PublicSubnetName argument (#13417)</span></span>
* <span data-ttu-id="76011-414">@mahortas, -HostNames 매개 변수 값 업데이트(#13349)</span><span class="sxs-lookup"><span data-stu-id="76011-414">@mahortas, Update for -HostNames parameter values (#13349)</span></span>
* <span data-ttu-id="76011-415">@MariachiForHire, 지원되는 TrafficAnalyticsInterval 값 추가(#13304)</span><span class="sxs-lookup"><span data-stu-id="76011-415">@MariachiForHire, added supported TrafficAnalyticsInterval values (#13304)</span></span>
* <span data-ttu-id="76011-416">Michael James(@mikejwhat), Get-AzLogicAppRunHistory에서 30개를 초과하는 항목을 반환할 수 있도록 허용(#13393)</span><span class="sxs-lookup"><span data-stu-id="76011-416">Michael James (@mikejwhat), Allow Get-AzLogicAppRunHistory to return more than 30 entries (#13393)</span></span>
* <span data-ttu-id="76011-417">Shashikant Shakya(@shshakya), Restore-AzSqlInstanceDatabase.md 업데이트(#13404)</span><span class="sxs-lookup"><span data-stu-id="76011-417">Shashikant Shakya (@shshakya), Update Restore-AzSqlInstanceDatabase.md (#13404)</span></span>

## <a name="500---october-2020"></a><span data-ttu-id="76011-418">5.0.0 - 2020년 10월</span><span class="sxs-lookup"><span data-stu-id="76011-418">5.0.0 - October 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="76011-419">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="76011-419">Az.Accounts</span></span>
* <span data-ttu-id="76011-420">[호환성이 손상되는 변경] 'Get-AzProfile' 및 'Select-AzProfile'이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-420">[Breaking Change] Removed 'Get-AzProfile' and 'Select-AzProfile'</span></span>
* <span data-ttu-id="76011-421">Azure Directory 인증 라이브러리가 MSAL(Microsoft 인증 라이브러리)로 대체되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-421">Replaced Azure Directory Authentication Library with Microsoft Authentication Library(MSAL)</span></span>

#### <a name="azaks"></a><span data-ttu-id="76011-422">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="76011-422">Az.Aks</span></span>
* <span data-ttu-id="76011-423">[호환성이 손상되는 변경] 'New-AzAksCluster' 및 'Set-AzAksCluster'에서 매개 변수 별칭 'ClientIdAndSecret'이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-423">[Breaking Change] Removed parameter alias 'ClientIdAndSecret' in 'New-AzAksCluster' and 'Set-AzAksCluster'.</span></span>
* <span data-ttu-id="76011-424">[호환성이 손상되는 변경] 'New-AzAksCluster'의 'NodeVmSetType' 기본값이 'AvailabilitySet'에서 'VirtualMachineScaleSets'로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-424">[Breaking Change] Changed the default value of 'NodeVmSetType' in 'New-AzAksCluster' from 'AvailabilitySet' to 'VirtualMachineScaleSets'.</span></span>
* <span data-ttu-id="76011-425">[호환성이 손상되는 변경] 'New-AzAksCluster'의 'NetworkPlugin' 기본값이 'None'에서 'azure'로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-425">[Breaking Change] Changed the default value of 'NetworkPlugin' in 'New-AzAksCluster' from 'None' to 'azure'.</span></span>
* <span data-ttu-id="76011-426">[호환성이 손상되는 변경] 'New-AzAksCluster'의 'NodeOsType' 매개 변수는 Linux라는 하나의 값만 지원하므로 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-426">[Breaking Change] Removed parameter 'NodeOsType' in 'New-AzAksCluster' as it supports only one value Linux.</span></span>

#### <a name="azbilling"></a><span data-ttu-id="76011-427">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="76011-427">Az.Billing</span></span>
* <span data-ttu-id="76011-428">'Get-AzBillingAccount' cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-428">Added 'Get-AzBillingAccount' cmdlet</span></span>
* <span data-ttu-id="76011-429">'Get-AzBillingProfile' cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-429">Added 'Get-AzBillingProfile' cmdlet</span></span>
* <span data-ttu-id="76011-430">'Get-AzInvoiceSection' cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-430">Added 'Get-AzInvoiceSection' cmdlet</span></span>
* <span data-ttu-id="76011-431">'Get-AzBillingInvoice' cmdlet에 새 매개 변수가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-431">Added new parameters in 'Get-AzBillingInvoice' cmdlet</span></span>
* <span data-ttu-id="76011-432">Get-AzBillingInvoice cmdlet의 응답에서 DownloadUrlExpiry, Type, BillingPeriodNames 속성이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-432">Removed properties DownloadUrlExpiry, Type, BillingPeriodNames from the response of Get-AzBillingInvoice cmdlet</span></span>

#### <a name="azcdn"></a><span data-ttu-id="76011-433">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="76011-433">Az.Cdn</span></span>
* <span data-ttu-id="76011-434">다중 원본 및 프라이빗 링크 기능을 지원하는 cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-434">Added cmdlets to support multi-origin and private link functionality</span></span> 

#### <a name="azcognitiveservices"></a><span data-ttu-id="76011-435">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="76011-435">Az.CognitiveServices</span></span>
* <span data-ttu-id="76011-436">SDK가 7.4.0-preview로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-436">Updated SDK to 7.4.0-preview.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="76011-437">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="76011-437">Az.Compute</span></span>
* <span data-ttu-id="76011-438">'New-AzVm'에 '-VmssId' 매개 변수가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-438">Added '-VmssId' parameter to 'New-AzVm'</span></span>
* <span data-ttu-id="76011-439">'New-AzVmss' cmdlet에 'PlatformFaultDomainCount' 매개 변수가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-439">Added 'PlatformFaultDomainCount' parameter to the 'New-AzVmss' cmdlet.</span></span>
* <span data-ttu-id="76011-440">새 cmdlet 'Get-AzDiskEncryptionSetAssociatedResource'</span><span class="sxs-lookup"><span data-stu-id="76011-440">New cmdlet 'Get-AzDiskEncryptionSetAssociatedResource'</span></span>
* <span data-ttu-id="76011-441">New-AzDiskConfig cmdlet에 선택적 매개 변수 'Tier' 및 'LogicalSectorSize'가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-441">Added 'Tier' and 'LogicalSectorSize' optional parameters to the New-AzDiskConfig cmdlet.</span></span> 
* <span data-ttu-id="76011-442">'New-AzDiskUpdateConfig' cmdlet에 선택적 매개 변수 'Tier', 'MaxSharesCount', 'DiskIOPSReadOnly' 및 'DiskMBpsReadOnly'가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-442">Added 'Tier', 'MaxSharesCount', 'DiskIOPSReadOnly', and 'DiskMBpsReadOnly' optional parameters to the 'New-AzDiskUpdateConfig' cmdlet.</span></span> 

#### <a name="azcontainerregistry"></a><span data-ttu-id="76011-443">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="76011-443">Az.ContainerRegistry</span></span>
* <span data-ttu-id="76011-444">[호환성이 손상되는 변경] API 버전이 2019-05-01로 업데이트됩니다.</span><span class="sxs-lookup"><span data-stu-id="76011-444">[Breaking Change] Updates API version to 2019-05-01</span></span>
* <span data-ttu-id="76011-445">[호환성이 손상되는 변경] 'New-AzContainerRegistry'에서 SKU 'Classic' 및 'StorageAccountName' 매개 변수가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-445">[Breaking Change] Removed SKU 'Classic' and parameter 'StorageAccountName' from 'New-AzContainerRegistry'</span></span>
* <span data-ttu-id="76011-446">새 cmdlet이 추가되었습니다. 'Connect-AzContainerRegistry', 'Import-AzContainerRegistry', 'Get-AzContainerRegistryUsage', 'New-AzContainerRegistryNetworkRule', 'Set-AzContainerRegistryNetworkRule'</span><span class="sxs-lookup"><span data-stu-id="76011-446">Added New cmdlets: 'Connect-AzContainerRegistry', 'Import-AzContainerRegistry', 'Get-AzContainerRegistryUsage', 'New-AzContainerRegistryNetworkRule', 'Set-AzContainerRegistryNetworkRule'</span></span>
* <span data-ttu-id="76011-447">'Update-AzContainerRegistry'에 새 매개 변수 'NetworkRuleSet'가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-447">Added new parameter 'NetworkRuleSet' to 'Update-AzContainerRegistry'</span></span>

#### <a name="azdatabricks"></a><span data-ttu-id="76011-448">Az.Databricks</span><span class="sxs-lookup"><span data-stu-id="76011-448">Az.Databricks</span></span>
* <span data-ttu-id="76011-449">`-EncryptionKeyVersion`이 없으면 databricks 작업 영역 업데이트가 실패하는 버그가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-449">Fixed a bug that may cause updating databricks workspace without `-EncryptionKeyVersion` to fail.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="76011-450">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="76011-450">Az.DataFactory</span></span>
* <span data-ttu-id="76011-451">ADF .Net SDK 버전이 4.12.0으로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-451">Updated ADF .Net SDK version to 4.12.0</span></span>
* <span data-ttu-id="76011-452">ADF 암호화 클라이언트 SDK 버전이 4.14.7587.7로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-452">Updated ADF encryption client SDK version to 4.14.7587.7</span></span>
* <span data-ttu-id="76011-453">'Stop-AzDataFactoryV2TriggerRun' 및 'Invoke-AzDataFactoryV2TriggerRun' 명령이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-453">Added 'Stop-AzDataFactoryV2TriggerRun' and 'Invoke-AzDataFactoryV2TriggerRun' commands</span></span>

#### <a name="azdesktopvirtualization"></a><span data-ttu-id="76011-454">Az.DesktopVirtualization</span><span class="sxs-lookup"><span data-stu-id="76011-454">Az.DesktopVirtualization</span></span>
* <span data-ttu-id="76011-455">최상위 arm 개체를 만들려면 Location 속성이 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="76011-455">Require Location property for creating top level arm objects.</span></span>
        <span data-ttu-id="76011-456">\* `New-AzWvdApplicationGroup`에 `ApplicationGroupType`이 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="76011-456">\* Made `ApplicationGroupType` required for `New-AzWvdApplicationGroup`.</span></span>
        <span data-ttu-id="76011-457">\* `New-AzWvdApplicationGroup`에 `HostPoolArmPath`가 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="76011-457">\* Made `HostPoolArmPath` required for `New-AzWvdApplicationGroup`.</span></span>
        <span data-ttu-id="76011-458">\* `New-AzWvdHostPool`에 `PreferredAppGroupType`이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-458">\* Added `PreferredAppGroupType` for `New-AzWvdHostPool`.</span></span>

#### <a name="azfunctions"></a><span data-ttu-id="76011-459">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="76011-459">Az.Functions</span></span>
* <span data-ttu-id="76011-460">[호환성이 손상되는 변경] 'Get-AzFunctionApp' 매개 변수 세트 하나를 제외한 모든 매개 변수 세트에서 'IncludeSlot' 스위치 매개 변수가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-460">[Breaking Change] Removed 'IncludeSlot' switch parameter from all but one parameter set of 'Get-AzFunctionApp'.</span></span> <span data-ttu-id="76011-461">이제 이 cmdlet은 '-IncludeSlot'이 지정된 경우 결과에서 배포 슬롯 검색을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="76011-461">The cmdlet now supports retrieving deployment slots in the results when '-IncludeSlot' is specified.</span></span> 
* <span data-ttu-id="76011-462">'New-AzFunctionApp'이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-462">Updated 'New-AzFunctionApp':</span></span>
  - <span data-ttu-id="76011-463">이 옵션을 지정할 경우 application insights 프로젝트가 생성되지 않도록 -DisableApplicationInsights가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-463">Fixed -DisableApplicationInsights so that no application insights project is created when this option is specified.</span></span> <span data-ttu-id="76011-464">[#12728]</span><span class="sxs-lookup"><span data-stu-id="76011-464">[#12728]</span></span>
  - <span data-ttu-id="76011-465">[호환성이 손상되는 변경] PowerShell 6.2 함수 앱을 만드는 지원 기능이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-465">[Breaking Change] Removed support to create PowerShell 6.2 function apps.</span></span>
  - <span data-ttu-id="76011-466">[호환성이 손상되는 변경] RuntimeVersion 매개 변수가 지정되지 않은 경우 PowerShell 함수 앱에 대한 Windows의 Functions 버전 3 기본 런타임 버전이 6.2에서 7.0으로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-466">[Breaking Change] Changed the default runtime version in Functions version 3 on Windows for PowerShell function apps from 6.2 to 7.0 when the RuntimeVersion parameter is not specified.</span></span>
  - <span data-ttu-id="76011-467">[호환성이 손상되는 변경] RuntimeVersion 매개 변수가 지정되지 않은 경우 Node 함수 앱에 대한 Windows 및 Linux의 Functions 버전 3 기본 런타임 버전이 10에서 12로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-467">[Breaking Change] Changed the default runtime version in Functions version 3 on Windows and Linux for Node function apps from 10 to 12 when the RuntimeVersion parameter is not specified.</span></span>
  - <span data-ttu-id="76011-468">[호환성이 손상되는 변경] RuntimeVersion 매개 변수가 지정되지 않은 경우 Python 함수 앱에 대한 Linux의 Functions 버전 3 기본 런타임 버전이 3.7에서 3.8로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-468">[Breaking Change] Changed the default runtime version in Functions version 3 on Linux for Python function apps from 3.7 to 3.8 when the RuntimeVersion parameter is not specified.</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="76011-469">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="76011-469">Az.HDInsight</span></span>
 * <span data-ttu-id="76011-470">AzHDInsightCluster cmdlet의 경우:</span><span class="sxs-lookup"><span data-stu-id="76011-470">For New-AzHDInsightCluster cmdlet:</span></span>
     - <span data-ttu-id="76011-471">'DefaultStorageAccountName' 매개 변수가 'StorageAccountResourceId'로 대체되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-471">Replaced parameter 'DefaultStorageAccountName' with 'StorageAccountResourceId'</span></span>
     - <span data-ttu-id="76011-472">'DefaultStorageAccountKey' 매개 변수가 'StorageAccountKey'로 대체되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-472">Replaced parameter 'DefaultStorageAccountKey' with 'StorageAccountKey'</span></span>
     - <span data-ttu-id="76011-473">'DefaultStorageAccountType' 매개 변수가 'StorageAccountType'으로 대체되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-473">Replaced parameter 'DefaultStorageAccountType' with 'StorageAccountType'</span></span>
     - <span data-ttu-id="76011-474">'PublicNetworkAccessType' 매개 변수가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-474">Removed parameter 'PublicNetworkAccessType'</span></span>
     - <span data-ttu-id="76011-475">'OutboundPublicNetworkAccessType' 매개 변수가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-475">Removed parameter 'OutboundPublicNetworkAccessType'</span></span>
     - <span data-ttu-id="76011-476">새 매개 변수가 추가되었습니다. ADLSGen2를 지원하기 위한 'StorageFileSystem' 및 'StorageAccountManagedIdentity'</span><span class="sxs-lookup"><span data-stu-id="76011-476">Added new parameters: 'StorageFileSystem' and 'StorageAccountManagedIdentity' to support ADLSGen2</span></span>
     - <span data-ttu-id="76011-477">HDInsight ID Broker를 지원하기 위해 새 매개 변수 'EnableIDBroker'가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-477">Added new parameter 'EnableIDBroker' to Support HDInsight ID Broker</span></span>
     - <span data-ttu-id="76011-478">새 매개 변수가 추가되었습니다. Kafka Rest Proxy를 지원하기 위한 'KafkaClientGroupId', 'KafkaClientGroupName' 및 'KafkaManagementNodeSize'</span><span class="sxs-lookup"><span data-stu-id="76011-478">Added new parameters: 'KafkaClientGroupId', 'KafkaClientGroupName' and 'KafkaManagementNodeSize' to support Kafka Rest Proxy</span></span>
 * <span data-ttu-id="76011-479">New-AzHDInsightClusterConfig cmdlet의 경우:</span><span class="sxs-lookup"><span data-stu-id="76011-479">For New-AzHDInsightClusterConfig cmdlet:</span></span>
     - <span data-ttu-id="76011-480">'DefaultStorageAccountName' 매개 변수가 'StorageAccountResourceId'로 대체되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-480">Replaced parameter 'DefaultStorageAccountName' with 'StorageAccountResourceId'</span></span>
     - <span data-ttu-id="76011-481">'DefaultStorageAccountKey' 매개 변수가 'StorageAccountKey'로 대체되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-481">Replaced parameter 'DefaultStorageAccountKey' with 'StorageAccountKey'</span></span>
     - <span data-ttu-id="76011-482">'DefaultStorageAccountType' 매개 변수가 'StorageAccountType'으로 대체되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-482">Replaced parameter 'DefaultStorageAccountType' with 'StorageAccountType'</span></span>
     - <span data-ttu-id="76011-483">'PublicNetworkAccessType' 매개 변수가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-483">Removed parameter 'PublicNetworkAccessType'</span></span>
     - <span data-ttu-id="76011-484">'OutboundPublicNetworkAccessType' 매개 변수가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-484">Removed parameter 'OutboundPublicNetworkAccessType'</span></span>
* <span data-ttu-id="76011-485">Set-AzHDInsightDefaultStorage cmdlet의 경우:</span><span class="sxs-lookup"><span data-stu-id="76011-485">For Set-AzHDInsightDefaultStorage cmdlet:</span></span>
    - <span data-ttu-id="76011-486">'StorageAccountName' 매개 변수가 'StorageAccountResourceId'로 대체되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-486">Replaced parameter 'StorageAccountName' with 'StorageAccountResourceId'</span></span>
* <span data-ttu-id="76011-487">Add-AzHDInsightSecurityProfile cmdlet의 경우:</span><span class="sxs-lookup"><span data-stu-id="76011-487">For Add-AzHDInsightSecurityProfile cmdlet:</span></span>
    - <span data-ttu-id="76011-488">'Domain' 매개 변수가 'DomainResourceId'로 대체되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-488">Replaced parameter 'Domain' with 'DomainResourceId'</span></span>
    - <span data-ttu-id="76011-489">'OrganizationalUnitDN' 매개 변수에 대한 필수 요구 사항이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-489">Removed the mandatory requirement for parameter 'OrganizationalUnitDN'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="76011-490">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="76011-490">Az.KeyVault</span></span>
* <span data-ttu-id="76011-491">[호환성이 손상되는 변경] 'New-AzKeyVault'의 DisableSoftDelete 매개 변수와 'Update-AzKeyVault'의 EnableSoftDelete 매개 변수가 더 이상 사용되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-491">[Breaking Change] Deprecated parameter DisableSoftDelete in 'New-AzKeyVault' and EnableSoftDelete in 'Update-AzKeyVault'</span></span>
* <span data-ttu-id="76011-492">[호환성이 손상되는 변경] SecretValue를 직접 표시하지 않도록 SecretValueText 특성이 제거되었습니다. [#12266]</span><span class="sxs-lookup"><span data-stu-id="76011-492">[Breaking Change] Removed attribute SecretValueText to avoid displaying SecretValue directly [#12266]</span></span>
* <span data-ttu-id="76011-493">새 리소스 유형 지원: 관리형 HSM</span><span class="sxs-lookup"><span data-stu-id="76011-493">Supported new resource type: managed HSM</span></span>
    - <span data-ttu-id="76011-494">관리형 HSM의 CRUD와 관리형 HSM에서 키를 작동하는 cmdlet</span><span class="sxs-lookup"><span data-stu-id="76011-494">CRUD of managed HSM and cmdlets to operate keys on managed HSM</span></span>
    - <span data-ttu-id="76011-495">전체 HSM 백업/복원, AES 키 생성, 보안 도메인 백업/복원, RBAC</span><span class="sxs-lookup"><span data-stu-id="76011-495">Full HSM backup/restore, AES key creation, security domain backup/restore, RBAC</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="76011-496">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="76011-496">Az.ManagedServices</span></span>
* <span data-ttu-id="76011-497">[호환성이 손상되는 변경] 업데이트된 매개 변수 명명 규칙 및 관련 예제</span><span class="sxs-lookup"><span data-stu-id="76011-497">[Breaking Change] Updated parameters naming conventions and associated examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="76011-498">Az.Network</span><span class="sxs-lookup"><span data-stu-id="76011-498">Az.Network</span></span>
* <span data-ttu-id="76011-499">[호환성이 손상되는 변경] 'HostedSubnet' 매개 변수가 제거되고 'Subnet'이 대신 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-499">[Breaking Change] Removed parameter 'HostedSubnet' and added 'Subnet' instead</span></span>
* <span data-ttu-id="76011-500">가상 라우터 피어 경로에 대한 새 cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-500">Added new cmdlets for Virtual Router Peer Routes</span></span>
    - <span data-ttu-id="76011-501">'Get-AzVirtualRouterPeerLearnedRoute'</span><span class="sxs-lookup"><span data-stu-id="76011-501">'Get-AzVirtualRouterPeerLearnedRoute'</span></span>
    - <span data-ttu-id="76011-502">'Get-AzVirtualRouterPeerAdvertisedRoute'</span><span class="sxs-lookup"><span data-stu-id="76011-502">'Get-AzVirtualRouterPeerAdvertisedRoute'</span></span>
* <span data-ttu-id="76011-503">New-AzFirewall cmdlet이 업데이트됨:</span><span class="sxs-lookup"><span data-stu-id="76011-503">Updated New-AzFirewall cmdlet:</span></span>
    - <span data-ttu-id="76011-504">'-SkuTier' 매개 변수가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-504">Added parameter '-SkuTier'</span></span>
    - <span data-ttu-id="76011-505">'-SkuName' 매개 변수가 추가되었으며 Sku가 이 매개 변수의 별칭이 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-505">Added parameter '-SkuName' and made Sku as Alias for this</span></span>
    - <span data-ttu-id="76011-506">'-Sku' 매개 변수가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-506">Removed parameter '-Sku'</span></span>
* <span data-ttu-id="76011-507">[호환성이 손상되는 변경] 'Start-AzVpnConnectionPacketCapture' 및 'Stop-AzVpnConnectionPacketCapture'에서 'Connectionlink' 인수가 필수가 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-507">[Breaking Change] Made 'Connectionlink' argument mandatory in 'Start-AzVpnConnectionPacketCapture' and 'Stop-AzVpnConnectionPacketCapture'</span></span>
* <span data-ttu-id="76011-508">[호환성이 손상되는 변경] '-Filter' 매개 변수를 제거하도록 'New-AzNetworkWatcherConnectionMonitorEndPointObject'가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-508">[Breaking Change] Updated 'New-AzNetworkWatcherConnectionMonitorEndPointObject' to remove parameter '-Filter'</span></span>
* <span data-ttu-id="76011-509">[호환성이 손상되는 변경] 'New-AzNetworkWatcherConnectionMonitorEndpointFilterItemObject' cmdlet이 'New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject'로 대체되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-509">[Breaking Change] Replaced 'New-AzNetworkWatcherConnectionMonitorEndpointFilterItemObject' cmdlet with 'New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject'</span></span>
* <span data-ttu-id="76011-510">'New-AzNetworkWatcherConnectionMonitorEndPointObject' cmdlet이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-510">Updated 'New-AzNetworkWatcherConnectionMonitorEndPointObject' cmdlet:</span></span>
    - <span data-ttu-id="76011-511">'-Type' 매개 변수가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-511">Added parameter '-Type'</span></span>
    - <span data-ttu-id="76011-512">'-CoverageLevel' 매개 변수가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-512">Added parameter '-CoverageLevel'</span></span>
    - <span data-ttu-id="76011-513">'-Scope' 매개 변수가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-513">Added parameter '-Scope'</span></span>
* <span data-ttu-id="76011-514">'New-AzNetworkWatcherConnectionMonitorProtocolConfigurationObject' cmdlet이 새 매개 변수 '-DestinationPortBehavior'로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-514">Updated 'New-AzNetworkWatcherConnectionMonitorProtocolConfigurationObject' cmdlet with new parameter '-DestinationPortBehavior'</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="76011-515">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="76011-515">Az.RecoveryServices</span></span>
* <span data-ttu-id="76011-516">기여자 권한을 위해 워크로드 복원을 수정하는 중입니다.</span><span class="sxs-lookup"><span data-stu-id="76011-516">Fixing Workload Restore for contributor permissions.</span></span>
* <span data-ttu-id="76011-517">Restore-AzRecoveryServicesBackupItem cmdlet에 대한 새 매개 변수 집합 및 유효성 검사가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-517">Added new parameter sets and validations for Restore-AzRecoveryServicesBackupItem cmdlet.</span></span>

#### <a name="azresources"></a><span data-ttu-id="76011-518">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="76011-518">Az.Resources</span></span>
* <span data-ttu-id="76011-519">구문 분석 버그가 해결되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-519">Fixed parsing bug</span></span>
* <span data-ttu-id="76011-520">결과에서 미리 보기 메시지를 제거하도록 ARM 템플릿 What-If cmdlet이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-520">Updated ARM template What-If cmdlets to remove preview message from results</span></span>
* <span data-ttu-id="76011-521">'-WhatIf'가 상위 범위에서 설정된 경우 템플릿 배포 cmdlet의 작동이 중단되는 문제가 해결되었습니다. [#13038]</span><span class="sxs-lookup"><span data-stu-id="76011-521">Fixed an issue where template deployment cmdlets crash if '-WhatIf' is set at a higher scope [#13038]</span></span>
* <span data-ttu-id="76011-522">템플릿 배포 cmdlet이 템플릿 매개 변수에서 대/소문자를 구분하지 않는 문제가 해결되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-522">Fixed an issue where template deployment cmdlets does not preserve case for template parameters</span></span>
* <span data-ttu-id="76011-523">'Export-AzResourceGroup' cmdlet에 사용되는 기본 API 버전이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-523">Added a default API version to be used in 'Export-AzResourceGroup' cmdlet</span></span>
* <span data-ttu-id="76011-524">템플릿 사양에 대한 cmdlet이 추가되었습니다('Get-AzTemplateSpec', 'Set-AzTemplateSpec', 'New-AzTemplateSpec', 'Remove-AzTemplateSpec', 'Export-AzTemplateSpec').</span><span class="sxs-lookup"><span data-stu-id="76011-524">Added cmdlets for Template Specs ('Get-AzTemplateSpec', 'Set-AzTemplateSpec', 'New-AzTemplateSpec', 'Remove-AzTemplateSpec', 'Export-AzTemplateSpec')</span></span>
* <span data-ttu-id="76011-525">새 -TemplateSpecId 매개 변수를 통해 기존 배포 cmdlet을 사용하여 템플릿 사양을 배포하도록 지원하는 기능이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-525">Added support for deploying Template Specs using existing deployment cmdlets (via the new -TemplateSpecId parameter)</span></span> 
* <span data-ttu-id="76011-526">SDK를 사용하도록 'Get-AzResourceGroupDeploymentOperation'이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-526">Updated 'Get-AzResourceGroupDeploymentOperation' to use the SDK.</span></span>
* <span data-ttu-id="76011-527">'\*-AzDeployment' cmdlet에서 '-ApiVersion' 매개 변수가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-527">Removed '-ApiVersion' parameter from '\*-AzDeployment' cmdlets.</span></span>

#### <a name="azsql"></a><span data-ttu-id="76011-528">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="76011-528">Az.Sql</span></span>
* <span data-ttu-id="76011-529">networkIsolation이 지정되지 않은 경우 New-AzSqlDatabaseExport가 실패하는 문제가 해결되었습니다. [#13097]</span><span class="sxs-lookup"><span data-stu-id="76011-529">Fixed issue where New-AzSqlDatabaseExport fails if networkIsolation not specified [#13097]</span></span>
* <span data-ttu-id="76011-530">New-AzSqlDatabaseExport 및 New-AzSqlDatabaseImport가 결과 개체에 OperationStatusLink를 반환하지 않는 문제가 해결되었습니다. [#13097]</span><span class="sxs-lookup"><span data-stu-id="76011-530">Fixed issue where New-AzSqlDatabaseExport and New-AzSqlDatabaseImport were not returning OperationStatusLink in the result object [#13097]</span></span>
* <span data-ttu-id="76011-531">백업 스토리지 중복성 경고에서 Azure 쌍을 이루는 지역 URL이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-531">Update Azure Paired Regions URL in Backup Storage Redundancy Warnings</span></span> 

#### <a name="azstorage"></a><span data-ttu-id="76011-532">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="76011-532">Az.Storage</span></span>
* <span data-ttu-id="76011-533">더 이상 사용되지 않는 RestorePolicy.LastEnabledTime 속성이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-533">Removed obsolete property RestorePolicy.LastEnabledTime</span></span>
    - <span data-ttu-id="76011-534">'Enable-AzStorageBlobRestorePolicy'</span><span class="sxs-lookup"><span data-stu-id="76011-534">'Enable-AzStorageBlobRestorePolicy'</span></span>
    - <span data-ttu-id="76011-535">'Disable-AzStorageBlobRestorePolicy'</span><span class="sxs-lookup"><span data-stu-id="76011-535">'Disable-AzStorageBlobRestorePolicy'</span></span>
    - <span data-ttu-id="76011-536">'Get-AzStorageBlobServiceProperty'</span><span class="sxs-lookup"><span data-stu-id="76011-536">'Get-AzStorageBlobServiceProperty'</span></span>
    - <span data-ttu-id="76011-537">'Update-AzStorageBlobServiceProperty'</span><span class="sxs-lookup"><span data-stu-id="76011-537">'Update-AzStorageBlobServiceProperty'</span></span>
* <span data-ttu-id="76011-538">DaysAfterModificationGreaterThan의 Type이 int에서 int?로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-538">Change Type of DaysAfterModificationGreaterThan from int to int?</span></span>
    - <span data-ttu-id="76011-539">'Set-AzStorageAccountManagementPolicy'</span><span class="sxs-lookup"><span data-stu-id="76011-539">'Set-AzStorageAccountManagementPolicy'</span></span>
    - <span data-ttu-id="76011-540">'Get-AzStorageAccountManagementPolicy'</span><span class="sxs-lookup"><span data-stu-id="76011-540">'Get-AzStorageAccountManagementPolicy'</span></span>
    - <span data-ttu-id="76011-541">'Add-AzStorageAccountManagementPolicyAction'</span><span class="sxs-lookup"><span data-stu-id="76011-541">'Add-AzStorageAccountManagementPolicyAction'</span></span>
    - <span data-ttu-id="76011-542">'New-AzStorageAccountManagementPolicyRule'</span><span class="sxs-lookup"><span data-stu-id="76011-542">'New-AzStorageAccountManagementPolicyRule'</span></span>
* <span data-ttu-id="76011-543">액세스 계층을 사용한 파일 공유 생성/업데이트가 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="76011-543">Supported create/update file share with access tier</span></span>
    - <span data-ttu-id="76011-544">'New-AzRmStorageShare'</span><span class="sxs-lookup"><span data-stu-id="76011-544">'New-AzRmStorageShare'</span></span>
    - <span data-ttu-id="76011-545">'Update-AzRmStorageShare'</span><span class="sxs-lookup"><span data-stu-id="76011-545">'Update-AzRmStorageShare'</span></span>
* <span data-ttu-id="76011-546">Datalake Gen2 항목에서 Acl의 재귀적 설정/업데이트/제거가 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="76011-546">Supported set/update/remove Acl recursively on Datalake Gen2 item</span></span> 
    -  <span data-ttu-id="76011-547">'Set-AzDataLakeGen2AclRecursive'</span><span class="sxs-lookup"><span data-stu-id="76011-547">'Set-AzDataLakeGen2AclRecursive'</span></span> 
    -  <span data-ttu-id="76011-548">'Update-AzDataLakeGen2AclRecursive'</span><span class="sxs-lookup"><span data-stu-id="76011-548">'Update-AzDataLakeGen2AclRecursive'</span></span> 
    -  <span data-ttu-id="76011-549">'Remove-AzDataLakeGen2AclRecursive'</span><span class="sxs-lookup"><span data-stu-id="76011-549">'Remove-AzDataLakeGen2AclRecursive'</span></span>
* <span data-ttu-id="76011-550">새 권한 x,t를 사용하여 컨테이너 액세스 정책 지원</span><span class="sxs-lookup"><span data-stu-id="76011-550">Supported Container access policy with new permission x,t</span></span>
    -  <span data-ttu-id="76011-551">'New-AzStorageContainerStoredAccessPolicy'</span><span class="sxs-lookup"><span data-stu-id="76011-551">'New-AzStorageContainerStoredAccessPolicy'</span></span>
    -  <span data-ttu-id="76011-552">'Set-AzStorageContainerStoredAccessPolicy'</span><span class="sxs-lookup"><span data-stu-id="76011-552">'Set-AzStorageContainerStoredAccessPolicy'</span></span>
* <span data-ttu-id="76011-553">자식 속성 권한 유형을 열거형에서 문자열로 변경하여 컨테이너 액세스 정책 가져오기/설정 cmdlet의 출력을 변경했습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-553">Changed the output of get/set Container access policy cmdlet, by change the child property Permission type from enum to String</span></span>
    -  <span data-ttu-id="76011-554">'Get-AzStorageContainerStoredAccessPolicy'</span><span class="sxs-lookup"><span data-stu-id="76011-554">'Get-AzStorageContainerStoredAccessPolicy'</span></span>
    -  <span data-ttu-id="76011-555">'Set-AzStorageContainerStoredAccessPolicy'</span><span class="sxs-lookup"><span data-stu-id="76011-555">'Set-AzStorageContainerStoredAccessPolicy'</span></span>
* <span data-ttu-id="76011-556">json을 사용한 관리 정책 설정의 샘플 스크립트 문제가 해결되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-556">Fixed a sample script issue of set management policy with json</span></span>
    -  <span data-ttu-id="76011-557">'Set-AzStorageAccountManagementPolicy'</span><span class="sxs-lookup"><span data-stu-id="76011-557">'Set-AzStorageAccountManagementPolicy'</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="76011-558">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="76011-558">Az.Websites</span></span>
* <span data-ttu-id="76011-559">Premium V3 가격 책정 계층에 대한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-559">Added support for Premium V3 pricing tier</span></span>
* <span data-ttu-id="76011-560">WebSites SDK가 3.1.0으로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-560">Updated the WebSites SDK to 3.1.0</span></span>

### <a name="thanks-to-our-community-contributors"></a><span data-ttu-id="76011-561">커뮤니티 기여자에게 감사드립니다.</span><span class="sxs-lookup"><span data-stu-id="76011-561">Thanks to our community contributors</span></span>
* <span data-ttu-id="76011-562">@atul-ram, Get-AzDelegation.md 업데이트(#13176)</span><span class="sxs-lookup"><span data-stu-id="76011-562">@atul-ram, Update Get-AzDelegation.md (#13176)</span></span>
* <span data-ttu-id="76011-563">@dineshreddy007, WAC 토큰을 사용하여 Stack HCI를 등록하는 경우 올바르게 할당된 앱 역할을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="76011-563">@dineshreddy007, Get the App Roles assigned correctly in case of Stack HCI registration using WAC token.</span></span> <span data-ttu-id="76011-564">(#13249)</span><span class="sxs-lookup"><span data-stu-id="76011-564">(#13249)</span></span>
* <span data-ttu-id="76011-565">@kongou-ae, New-AzOffice365PolicyProperty.md 업데이트(#13217)</span><span class="sxs-lookup"><span data-stu-id="76011-565">@kongou-ae, Update New-AzOffice365PolicyProperty.md (#13217)</span></span>
* <span data-ttu-id="76011-566">Lohith Chowdary Chilukuri(@Lochiluk), Set-AzApplicationGateway.md 업데이트(#13150)</span><span class="sxs-lookup"><span data-stu-id="76011-566">Lohith Chowdary Chilukuri (@Lochiluk), Update Set-AzApplicationGateway.md (#13150)</span></span>
* <span data-ttu-id="76011-567">Matthew Burleigh(@mburleigh)</span><span class="sxs-lookup"><span data-stu-id="76011-567">Matthew Burleigh (@mburleigh)</span></span>
  * <span data-ttu-id="76011-568">문서에서 참조된 PowerShell cmdlet에 대한 링크 추가(#13203)</span><span class="sxs-lookup"><span data-stu-id="76011-568">Add links to PowerShell cmdlets referenced in the document (#13203)</span></span>
  * <span data-ttu-id="76011-569">문서에서 참조된 PowerShell cmdlet에 대한 링크 추가(#13190)</span><span class="sxs-lookup"><span data-stu-id="76011-569">Add links to PowerShell cmdlets referenced in the document (#13190)</span></span>
  * <span data-ttu-id="76011-570">문서에서 참조된 PowerShell cmdlet에 대한 링크 추가(#13189)</span><span class="sxs-lookup"><span data-stu-id="76011-570">Add links to PowerShell cmdlets referenced in the document (#13189)</span></span>
  * <span data-ttu-id="76011-571">참조된 cmdlet에 대한 링크 추가(#13137)</span><span class="sxs-lookup"><span data-stu-id="76011-571">add links to referenced cmdlets (#13137)</span></span>
  * <span data-ttu-id="76011-572">문서에서 참조된 PowerShell cmdlet에 대한 링크 추가(#13204)</span><span class="sxs-lookup"><span data-stu-id="76011-572">Add links to PowerShell cmdlets referenced in the document (#13204)</span></span>
  * <span data-ttu-id="76011-573">문서에서 참조된 PowerShell cmdlet에 대한 링크 추가(#13205)</span><span class="sxs-lookup"><span data-stu-id="76011-573">Add links to PowerShell cmdlets referenced in the document (#13205)</span></span>

## <a name="480---october-2020"></a><span data-ttu-id="76011-574">4.8.0 - 2020년 10월</span><span class="sxs-lookup"><span data-stu-id="76011-574">4.8.0 - October 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="76011-575">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="76011-575">Az.Accounts</span></span>
* <span data-ttu-id="76011-576">공용 라이브러리의 DateTime 구문 분석 문제 해결[#13045]</span><span class="sxs-lookup"><span data-stu-id="76011-576">Fixed DateTime parse issue in common libraries [#13045]</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="76011-577">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="76011-577">Az.CognitiveServices</span></span>
* <span data-ttu-id="76011-578">'New-AzCognitiveServicesAccountApiProperty' cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-578">Added 'New-AzCognitiveServicesAccountApiProperty' cmdlet.</span></span>
* <span data-ttu-id="76011-579">'New-AzCognitiveServicesAccount' 및 'Set-AzCognitiveServicesAccount'에 대해 'ApiProperty' 매개 변수 지원됨</span><span class="sxs-lookup"><span data-stu-id="76011-579">Supported 'ApiProperty' parameter for 'New-AzCognitiveServicesAccount' and 'Set-AzCognitiveServicesAccount'</span></span>

#### <a name="azcompute"></a><span data-ttu-id="76011-580">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="76011-580">Az.Compute</span></span>
* <span data-ttu-id="76011-581">FailoverTypes를 채워서 'Update-ASRRecoveryPlan'의 문제 해결</span><span class="sxs-lookup"><span data-stu-id="76011-581">Fixed issue in 'Update-ASRRecoveryPlan' by populating FailoverTypes</span></span>
* <span data-ttu-id="76011-582">'Get-AzVmImage' cmdlet에 '-Top' 및 '-OrderBy' 선택적 매개 변수를 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-582">Added the '-Top' and '-OrderBy' optional parameters to the 'Get-AzVmImage' cmdlet.</span></span> 

#### <a name="azdatabricks"></a><span data-ttu-id="76011-583">Az.Databricks</span><span class="sxs-lookup"><span data-stu-id="76011-583">Az.Databricks</span></span>
* <span data-ttu-id="76011-584">'Az.Databricks' 모듈의 일반 공급</span><span class="sxs-lookup"><span data-stu-id="76011-584">General availability of 'Az.Databricks' module</span></span>
* <span data-ttu-id="76011-585">가상 네트워크 피어링에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="76011-585">Added support for virtual network peering</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="76011-586">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="76011-586">Az.DataFactory</span></span>
* <span data-ttu-id="76011-587">출력 메시지의 오타 수정</span><span class="sxs-lookup"><span data-stu-id="76011-587">Fixed typo in output messages</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="76011-588">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="76011-588">Az.EventHub</span></span>
* <span data-ttu-id="76011-589">선택적 스위치 매개 변수 'TrustedServiceAccessEnabled'를 'Set-AzEventHubNetworkRuleSet' cmdlet에 추가</span><span class="sxs-lookup"><span data-stu-id="76011-589">Added optional switch parameter 'TrustedServiceAccessEnabled' to 'Set-AzEventHubNetworkRuleSet' cmdlet</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="76011-590">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="76011-590">Az.HDInsight</span></span>
* <span data-ttu-id="76011-591">'PublicNetworkAccessType' 및 'OutboundPublicNetworkAccessType' 매개 변수 사용 중단 계획에 대한 경고 메시지 추가</span><span class="sxs-lookup"><span data-stu-id="76011-591">Added warning message for planning to deprecate the parameters 'PublicNetworkAccessType' and 'OutboundPublicNetworkAccessType'</span></span>
* <span data-ttu-id="76011-592">'DefaultStorageAccountName' 매개 변수를 'StorageAccountResourceId'로 바꾸려는 계획에 대한 경고 메시지 추가</span><span class="sxs-lookup"><span data-stu-id="76011-592">Added warning message for planning to replace the parameter 'DefaultStorageAccountName' with 'StorageAccountResourceId'</span></span>
* <span data-ttu-id="76011-593">'DefaultStorageAccountKey' 매개 변수를 'StorageAccountKey'로 바꾸려는 계획에 대한 경고 메시지 추가</span><span class="sxs-lookup"><span data-stu-id="76011-593">Added warning message for planning to replace the parameter 'DefaultStorageAccountKey' with 'StorageAccountKey'</span></span>
* <span data-ttu-id="76011-594">'DefaultStorageAccountType' 매개 변수를 'StorageAccountType'으로 바꾸려는 계획에 대한 경고 메시지 추가</span><span class="sxs-lookup"><span data-stu-id="76011-594">Added warning message for planning to replace the parameter 'DefaultStorageAccountType' with 'StorageAccountType'</span></span>
* <span data-ttu-id="76011-595">'DefaultStorageContainer' 매개 변수를 'StorageContainer'로 바꾸려는 계획에 대한 경고 메시지 추가</span><span class="sxs-lookup"><span data-stu-id="76011-595">Added warning message for planning to replace the parameter 'DefaultStorageContainer' with 'StorageContainer'</span></span>
* <span data-ttu-id="76011-596">'DefaultStorageRootPath' 매개 변수를 'StorageRootPath'로 바꾸려는 계획에 대한 경고 메시지 추가</span><span class="sxs-lookup"><span data-stu-id="76011-596">Added warning message for planning to replace the parameter 'DefaultStorageRootPath' with 'StorageRootPath'</span></span>

#### <a name="aziothub"></a><span data-ttu-id="76011-597">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="76011-597">Az.IotHub</span></span>
* <span data-ttu-id="76011-598">업데이트된 디바이스 SDK.</span><span class="sxs-lookup"><span data-stu-id="76011-598">Updated devices sdk.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="76011-599">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="76011-599">Az.KeyVault</span></span>
* <span data-ttu-id="76011-600">SecretValueText 속성 제거 세부 날짜 제공</span><span class="sxs-lookup"><span data-stu-id="76011-600">Provided the detailed date of removing property SecretValueText</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="76011-601">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="76011-601">Az.ManagedServices</span></span>
* <span data-ttu-id="76011-602">관리되는 서비스 할당 및 정의의 cmdlet에 대한 호환성이 손상되는 변경 경고가 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="76011-602">Updated breaking change warnings on cmdlets of managed services assignment and definition</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="76011-603">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="76011-603">Az.Monitor</span></span>
* <span data-ttu-id="76011-604">경고 메시지를 숨길 수 없는 버그를 수정했습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-604">Fixed the bug that warning message cannot be suppressed.</span></span> <span data-ttu-id="76011-605">[#12889]</span><span class="sxs-lookup"><span data-stu-id="76011-605">[#12889]</span></span>
* <span data-ttu-id="76011-606">경고 규칙 기준에서 'SkipMetricValidation' 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="76011-606">Supported 'SkipMetricValidation' parameter in alert rule criteria.</span></span> <span data-ttu-id="76011-607">메트릭 유효성 검사를 건너뛰도록 하여 아직 생성되지 않은 사용자 지정 메트릭에 대한 경고 규칙을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-607">Allows creating an alert rule on a custom metric that isn't yet emitted, by causing the metric validation to be skipped.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="76011-608">Az.Network</span><span class="sxs-lookup"><span data-stu-id="76011-608">Az.Network</span></span>
* <span data-ttu-id="76011-609">VPNSite 리소스에 Office365 정책 추가</span><span class="sxs-lookup"><span data-stu-id="76011-609">Added Office365 Policy to VPNSite Resource</span></span>
    - <span data-ttu-id="76011-610">'New-AzO365PolicyProperty'</span><span class="sxs-lookup"><span data-stu-id="76011-610">'New-AzO365PolicyProperty'</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="76011-611">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="76011-611">Az.RecoveryServices</span></span>
* <span data-ttu-id="76011-612">워크로드 백업에 대한 컨테이너 이름 유효성 검사가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-612">Added container name validation for workload backup.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="76011-613">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="76011-613">Az.RedisCache</span></span>
* <span data-ttu-id="76011-614">Microsoft.Cache RP 등록과 관련된 권한 문제로 인해 'New-AzRedisCache' 및 'Set-AzRedisCache' cmdlet이 실패하지 않도록 함</span><span class="sxs-lookup"><span data-stu-id="76011-614">Made 'New-AzRedisCache' and 'Set-AzRedisCache' cmdlets not fail because of permission issue related to registering Microsoft.Cache RP</span></span>

#### <a name="azsql"></a><span data-ttu-id="76011-615">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="76011-615">Az.Sql</span></span>
* <span data-ttu-id="76011-616">BackupStorageRedundancy가 다음에 추가됨</span><span class="sxs-lookup"><span data-stu-id="76011-616">Added BackupStorageRedundancy to the following:</span></span> 
    - <span data-ttu-id="76011-617">'Restore-AzureRmSqlDatabase'</span><span class="sxs-lookup"><span data-stu-id="76011-617">'Restore-AzureRmSqlDatabase'</span></span>
    - <span data-ttu-id="76011-618">'New-AzSqlDatabaseCopy'</span><span class="sxs-lookup"><span data-stu-id="76011-618">'New-AzSqlDatabaseCopy'</span></span>
    - <span data-ttu-id="76011-619">'New-AzSqlDatabaseSecondary'</span><span class="sxs-lookup"><span data-stu-id="76011-619">'New-AzSqlDatabaseSecondary'</span></span>
* <span data-ttu-id="76011-620">모든 SQL DB 참조에 대한 BackupStorageRedundancy 매개 변수의 대소문자 구분 제거</span><span class="sxs-lookup"><span data-stu-id="76011-620">Removed case sensitivity for BackupStorageRedundancy parameter for all SQL DB references</span></span> 
* <span data-ttu-id="76011-621">BackupStorageRedundancy 경고 메시지 이름 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="76011-621">Updated BackupStorageRedundancy warning message names</span></span>

#### <a name="azstorage"></a><span data-ttu-id="76011-622">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="76011-622">Az.Storage</span></span>
* <span data-ttu-id="76011-623">스토리지 계정의 파일 서비스에서 사용/사용하지 않음/공유 일시 삭제 속성 지원</span><span class="sxs-lookup"><span data-stu-id="76011-623">Supported enable/disable/get share soft delete properties on file Service of a Storage account</span></span>
    - <span data-ttu-id="76011-624">'Update-AzStorageFileServiceProperty'</span><span class="sxs-lookup"><span data-stu-id="76011-624">'Update-AzStorageFileServiceProperty'</span></span>
    - <span data-ttu-id="76011-625">'Get-AzStorageFileServiceProperty'</span><span class="sxs-lookup"><span data-stu-id="76011-625">'Get-AzStorageFileServiceProperty'</span></span>
* <span data-ttu-id="76011-626">지원되는 목록 파일 공유에는 스토리지 계정의 삭제된 공유와 단일 파일 공유 사용량 가져오기가 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="76011-626">Supported list file shares include the deleted ones of a Storage account, and Get single file share usage</span></span>
    - <span data-ttu-id="76011-627">'Get-AzRmStorageShare'</span><span class="sxs-lookup"><span data-stu-id="76011-627">'Get-AzRmStorageShare'</span></span>
* <span data-ttu-id="76011-628">삭제된 파일 공유 복원 지원</span><span class="sxs-lookup"><span data-stu-id="76011-628">Supported restore a deleted file share</span></span>
    - <span data-ttu-id="76011-629">'Restore-AzRmStorageShare'</span><span class="sxs-lookup"><span data-stu-id="76011-629">'Restore-AzRmStorageShare'</span></span>
* <span data-ttu-id="76011-630">Blob 서비스 속성을 수정하기 위한 cmdlet을 변경하여, 서버에서 원래 속성을 가져오지 않으며 수정된 속성만 서버로 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="76011-630">Changed the cmdlets for modify blob service properties, won't get the original properties from server, but only set the modified properties to server.</span></span>
    - <span data-ttu-id="76011-631">'Enable-AzStorageBlobDeleteRetentionPolicy'</span><span class="sxs-lookup"><span data-stu-id="76011-631">'Enable-AzStorageBlobDeleteRetentionPolicy'</span></span>
    - <span data-ttu-id="76011-632">'Disable-AzStorageBlobDeleteRetentionPolicy'</span><span class="sxs-lookup"><span data-stu-id="76011-632">'Disable-AzStorageBlobDeleteRetentionPolicy'</span></span>  
    - <span data-ttu-id="76011-633">'Enable-AzStorageBlobRestorePolicy'</span><span class="sxs-lookup"><span data-stu-id="76011-633">'Enable-AzStorageBlobRestorePolicy'</span></span>
    - <span data-ttu-id="76011-634">'Disable-AzStorageBlobRestorePolicy'</span><span class="sxs-lookup"><span data-stu-id="76011-634">'Disable-AzStorageBlobRestorePolicy'</span></span>
    - <span data-ttu-id="76011-635">'Update-AzStorageBlobServiceProperty'</span><span class="sxs-lookup"><span data-stu-id="76011-635">'Update-AzStorageBlobServiceProperty'</span></span>
* <span data-ttu-id="76011-636">New-AzStorageAccount 매개 변수 -Kind 기본값에 대한 도움말 문제 해결[#12189]</span><span class="sxs-lookup"><span data-stu-id="76011-636">Fixed help issue for New-AzStorageAccount parameter -Kind default value [#12189]</span></span>
* <span data-ttu-id="76011-637">Blob 업로드에서 올바른 ContentType을 설정하는 방법을 보여주는 예제를 추가하여 문제 해결[#12989]</span><span class="sxs-lookup"><span data-stu-id="76011-637">Fixed issue by add example to show how to set correct ContentType in blob upload [#12989]</span></span>

## <a name="470---september-2020"></a><span data-ttu-id="76011-638">4.7.0 - 2020년 9월</span><span class="sxs-lookup"><span data-stu-id="76011-638">4.7.0 - September 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="76011-639">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="76011-639">Az.Accounts</span></span>
* <span data-ttu-id="76011-640">예정된 호환성이 손상되는 변경 메시지의 형식이 지정됨</span><span class="sxs-lookup"><span data-stu-id="76011-640">Formatted the upcoming breaking change messages</span></span>
* <span data-ttu-id="76011-641">Azure.Core가 1.4.1로 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="76011-641">Updated Azure.Core to 1.4.1</span></span>

#### <a name="azaks"></a><span data-ttu-id="76011-642">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="76011-642">Az.Aks</span></span>
* <span data-ttu-id="76011-643">'New-AzAksCluster', 'Set-AzAksCluster' 및 'New-AzAksNodePool'에 대한 클라이언트 쪽 매개 변수 유효성 검사 논리가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-643">Added client side parameter validation logic for 'New-AzAksCluster', 'Set-AzAksCluster' and 'New-AzAksNodePool'.</span></span> <span data-ttu-id="76011-644">[#12372]</span><span class="sxs-lookup"><span data-stu-id="76011-644">[#12372]</span></span>
* <span data-ttu-id="76011-645">'New-AzAksCluster'에서 추가 항목에 대한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-645">Added support for add-ons in 'New-AzAksCluster'.</span></span> <span data-ttu-id="76011-646">[#11239]</span><span class="sxs-lookup"><span data-stu-id="76011-646">[#11239]</span></span>
* <span data-ttu-id="76011-647">추가 항목에 대한 'Enable-AzAksAddOn' 및 'Disable-AzAksAddOn' cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-647">Added cmdlets 'Enable-AzAksAddOn' and 'Disable-AzAksAddOn' for add-ons.</span></span> <span data-ttu-id="76011-648">[#11239]</span><span class="sxs-lookup"><span data-stu-id="76011-648">[#11239]</span></span>
* <span data-ttu-id="76011-649">'New-AzAksCluster'에 대한 매개 변수 'GenerateSshKey'가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-649">Added parameter 'GenerateSshKey' for 'New-AzAksCluster'.</span></span> <span data-ttu-id="76011-650">[#12371]</span><span class="sxs-lookup"><span data-stu-id="76011-650">[#12371]</span></span>
* <span data-ttu-id="76011-651">API 버전이 2020-06-01로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-651">Updated api version to 2020-06-01.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="76011-652">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="76011-652">Az.CognitiveServices</span></span>
* <span data-ttu-id="76011-653">특정 API에 대한 추가 법률 용어를 표시했습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-653">Showed additional legal terms for certain APIs.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="76011-654">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="76011-654">Az.Compute</span></span>
* <span data-ttu-id="76011-655">'New-AzVmDiskEncryptionSetConfig'에 '-EncryptionType' 선택적 매개 변수가 추가됨</span><span class="sxs-lookup"><span data-stu-id="76011-655">Added the '-EncryptionType' optional parameter to 'New-AzVmDiskEncryptionSetConfig'</span></span>
* <span data-ttu-id="76011-656">새 리소스 종류에 대한 새 cmdlet: DiskAccess 'Get-AzDiskAccess', 'New-AzDiskAccess', 'Get-AzDiskAccess'</span><span class="sxs-lookup"><span data-stu-id="76011-656">New cmdlets for new resource type: DiskAccess 'Get-AzDiskAccess', 'New-AzDiskAccess', 'Get-AzDiskAccess'</span></span>
* <span data-ttu-id="76011-657">'New-AzSnapshotConfig'에 선택적 매개 변수 '-DiskAccessId' 및 '-NetworkAccessPolicy'가 추가됨</span><span class="sxs-lookup"><span data-stu-id="76011-657">Added optional parameters '-DiskAccessId' and '-NetworkAccessPolicy' to 'New-AzSnapshotConfig'</span></span>
* <span data-ttu-id="76011-658">'New-AzDiskConfig'에 선택적 매개 변수 '-DiskAccessId' 및 '-NetworkAccessPolicy'가 추가됨</span><span class="sxs-lookup"><span data-stu-id="76011-658">Added optional parameters '-DiskAccessId' and '-NetworkAccessPolicy' to 'New-AzDiskConfig'</span></span>
* <span data-ttu-id="76011-659">VirtualMachine 인스턴스 보기에 'PatchStatus' 속성이 추가됨</span><span class="sxs-lookup"><span data-stu-id="76011-659">Added 'PatchStatus' property to VirtualMachine Instance View</span></span>
* <span data-ttu-id="76011-660">가상 머신의 인스턴스 보기에 'VMHealth' 속성이 추가됨. 이 속성은 'Get-AzVm'이 '-Status'로 호출될 때 반환되는 개체</span><span class="sxs-lookup"><span data-stu-id="76011-660">Added 'VMHealth' property to the virtual machine's instance view, which is the returned object when 'Get-AzVm' is invoked with '-Status'</span></span>
* <span data-ttu-id="76011-661">'Get-AzVM' 및 'Get-AzVmss' 인스턴스 보기에 'AssignedHost' 필드가 추가됨</span><span class="sxs-lookup"><span data-stu-id="76011-661">Added 'AssignedHost' field to 'Get-AzVM' and 'Get-AzVmss' instance views.</span></span> <span data-ttu-id="76011-662">필드는 가상 머신 인스턴스의 리소스 ID를 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="76011-662">The field shows the resource id of the virtual machine instance</span></span>
* <span data-ttu-id="76011-663">선택적 매개 변수 '-SupportAutomaticPlacement'가 'New-AzHostGroup'에 추가됨</span><span class="sxs-lookup"><span data-stu-id="76011-663">Added optional parameter '-SupportAutomaticPlacement' to 'New-AzHostGroup'</span></span> 
* <span data-ttu-id="76011-664">'-HostGroupId' 매개 변수가 'New-AzVm' 및 'New-AzVmss'에 추가됨</span><span class="sxs-lookup"><span data-stu-id="76011-664">Added the '-HostGroupId' parameter to 'New-AzVm' and 'New-AzVmss'</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="76011-665">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="76011-665">Az.DataFactory</span></span>
* <span data-ttu-id="76011-666">ADF .Net SDK 버전이 4.11.0으로 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="76011-666">Updated ADF .Net SDK version to 4.11.0</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="76011-667">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="76011-667">Az.EventHub</span></span>
* <span data-ttu-id="76011-668">새 클러스터 cmdlet 추가됨 - 'New-AzEventHubCluster', 'Set-AzEventHubCluster', 'Get-AzEventHubCluster', 'Remove-AzEventHubCluster', 'Get-AzEventHubClustersAvailableRegions'</span><span class="sxs-lookup"><span data-stu-id="76011-668">Added new Cluster cmdlets - 'New-AzEventHubCluster', 'Set-AzEventHubCluster', 'Get-AzEventHubCluster', 'Remove-AzEventHubCluster', 'Get-AzEventHubClustersAvailableRegions'.</span></span>
* <span data-ttu-id="76011-669">#10722 문제 해결됨: AuthorizationRule 권한에 'Listen'만 할당하는 문제가 해결되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-669">Fixed for issue #10722 : Fix for assigning only 'Listen' to AuthorizationRule rights.</span></span>

#### <a name="azfunctions"></a><span data-ttu-id="76011-670">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="76011-670">Az.Functions</span></span>
* <span data-ttu-id="76011-671">v2 Functions를 지원하지 않는 지역에서 생성하는 기능이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-671">Removed the ability to create v2 Functions in regions that do not support it.</span></span>
* <span data-ttu-id="76011-672">PowerShell 6.2가 사용되지 않음</span><span class="sxs-lookup"><span data-stu-id="76011-672">Deprecated PowerShell 6.2.</span></span> <span data-ttu-id="76011-673">사용자가 PowerShell 6.2 함수 앱을 만들 때 PowerShell 7.0 함수 앱을 만들도록 권장하는 경고가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-673">Added a warning for when a user creates a PowerShell 6.2 function app that advises them to create a PowerShell 7.0 function app instead.</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="76011-674">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="76011-674">Az.HDInsight</span></span>
* <span data-ttu-id="76011-675">자동 크기 조정 구성을 사용하여 클러스터 만들기 지원</span><span class="sxs-lookup"><span data-stu-id="76011-675">Supported creating cluster with Autoscale configuration</span></span>
    - <span data-ttu-id="76011-676">cmdlet 'New-AzHDInsightCluster'에 새 매개 변수 'AutoscaleConfiguration' 추가</span><span class="sxs-lookup"><span data-stu-id="76011-676">Add new parameter 'AutoscaleConfiguration' to the cmdlet 'New-AzHDInsightCluster'</span></span>
* <span data-ttu-id="76011-677">운영 클러스터의 자동 크기 조정 구성 지원됨</span><span class="sxs-lookup"><span data-stu-id="76011-677">Supported operating cluster's Autoscale configuration</span></span>
    - <span data-ttu-id="76011-678">새 cmdlet 'Get-AzHDInsihgtClusterAutoscaleConfiguration' 추가</span><span class="sxs-lookup"><span data-stu-id="76011-678">Add new cmdlet 'Get-AzHDInsihgtClusterAutoscaleConfiguration'</span></span>
    - <span data-ttu-id="76011-679">새 cmdlet 'New-AzHDInsihgtClusterAutoscaleConfiguration' 추가</span><span class="sxs-lookup"><span data-stu-id="76011-679">Add new cmdlet 'New-AzHDInsihgtClusterAutoscaleConfiguration'</span></span>
    - <span data-ttu-id="76011-680">새 cmdlet 'Set-AzHDInsihgtClusterAutoscaleConfiguration' 추가</span><span class="sxs-lookup"><span data-stu-id="76011-680">Add new cmdlet 'Set-AzHDInsihgtClusterAutoscaleConfiguration'</span></span>
    - <span data-ttu-id="76011-681">새 cmdlet 'Remove-AzHDInsihgtClusterAutoscaleConfiguration' 추가</span><span class="sxs-lookup"><span data-stu-id="76011-681">Add new cmdlet 'Remove-AzHDInsihgtClusterAutoscaleConfiguration'</span></span>
    - <span data-ttu-id="76011-682">새 cmdlet 'New-AzHDInsihgtClusterAutoscaleScheduleCondition' 추가</span><span class="sxs-lookup"><span data-stu-id="76011-682">Add new cmdlet 'New-AzHDInsihgtClusterAutoscaleScheduleCondition'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="76011-683">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="76011-683">Az.KeyVault</span></span>
* <span data-ttu-id="76011-684">RBAC 권한 부여에 대한 지원 추가됨 [#10557]</span><span class="sxs-lookup"><span data-stu-id="76011-684">Added support for RBAC authorization [#10557]</span></span>
* <span data-ttu-id="76011-685">'Set-AzKeyVaultAccessPolicy'에서 향상된 오류 처리 [#4007]</span><span class="sxs-lookup"><span data-stu-id="76011-685">Enhanced error handling in 'Set-AzKeyVaultAccessPolicy' [#4007]</span></span>

#### <a name="azkusto"></a><span data-ttu-id="76011-686">Az.Kusto</span><span class="sxs-lookup"><span data-stu-id="76011-686">Az.Kusto</span></span>
* <span data-ttu-id="76011-687">'Az.Kusto' 모듈의 일반 공급</span><span class="sxs-lookup"><span data-stu-id="76011-687">General availability of 'Az.Kusto' module</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="76011-688">Az.Network</span><span class="sxs-lookup"><span data-stu-id="76011-688">Az.Network</span></span>
* <span data-ttu-id="76011-689">[호환성이 손상되는 변경] 리소스 가상 라우터 및 가상 허브에 맞게 아래 cmdlet이 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="76011-689">[Breaking Change] Updated below cmdlets to align resource virtual router and virtual hub</span></span>
    - <span data-ttu-id="76011-690">'New-AzVirtualRouter':</span><span class="sxs-lookup"><span data-stu-id="76011-690">'New-AzVirtualRouter':</span></span> 
        - <span data-ttu-id="76011-691">IP 구성 자식 리소스를 지원하는 -HostedSubnet 매개 변수가 추가됨</span><span class="sxs-lookup"><span data-stu-id="76011-691">Added -HostedSubnet parameter to support IP configuration child resource</span></span>
        - <span data-ttu-id="76011-692">-HostedGateway 및 -HostedGatewayId 삭제됨</span><span class="sxs-lookup"><span data-stu-id="76011-692">deleted -HostedGateway and -HostedGatewayId</span></span>
    - <span data-ttu-id="76011-693">'Get-AzVirtualRouter':</span><span class="sxs-lookup"><span data-stu-id="76011-693">'Get-AzVirtualRouter':</span></span>
        - <span data-ttu-id="76011-694">구독 수준 매개 변수 집합이 추가됨</span><span class="sxs-lookup"><span data-stu-id="76011-694">Added subscription level parameter set</span></span>
    - <span data-ttu-id="76011-695">'Remove-AzVirtualRouter'</span><span class="sxs-lookup"><span data-stu-id="76011-695">'Remove-AzVirtualRouter'</span></span>
    - <span data-ttu-id="76011-696">'Add-AzVirtualRouterPeer'</span><span class="sxs-lookup"><span data-stu-id="76011-696">'Add-AzVirtualRouterPeer'</span></span>
    - <span data-ttu-id="76011-697">'Get-AzVirtualRouterPeer'</span><span class="sxs-lookup"><span data-stu-id="76011-697">'Get-AzVirtualRouterPeer'</span></span>
    - <span data-ttu-id="76011-698">'Remove-AzVirtualRouterPeer'</span><span class="sxs-lookup"><span data-stu-id="76011-698">'Remove-AzVirtualRouterPeer'</span></span>
* <span data-ttu-id="76011-699">Azure Express 경로 포트에 대해 새 cmdlet이 추가됨</span><span class="sxs-lookup"><span data-stu-id="76011-699">Added new cmdlet for Azure Express Route Port</span></span>
    - <span data-ttu-id="76011-700">'New-AzExpressRoutePortLOA'</span><span class="sxs-lookup"><span data-stu-id="76011-700">'New-AzExpressRoutePortLOA'</span></span>
* <span data-ttu-id="76011-701">VirtualNetwork 피어링 리소스에 RemoteBgpCommunities 속성이 추가됨</span><span class="sxs-lookup"><span data-stu-id="76011-701">Added RemoteBgpCommunities property to the VirtualNetwork Peering Resource</span></span>
* <span data-ttu-id="76011-702">'New-AzLoadBalancerFrontendIpConfig', 'New-AzPublicIpAddress' 및 'New-AzPublicIpPrefix'에 대한 경고 메시지를 수정했습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-702">Modified the warning message for 'New-AzLoadBalancerFrontendIpConfig', 'New-AzPublicIpAddress' and 'New-AzPublicIpPrefix'.</span></span>
* <span data-ttu-id="76011-703">'Get-AzVpnGateway' 출력에 VpnGatewayIpConfigurations가 추가됨</span><span class="sxs-lookup"><span data-stu-id="76011-703">Added VpnGatewayIpConfigurations to 'Get-AzVpnGateway' output</span></span>
* <span data-ttu-id="76011-704">'Set-AzApplicationGatewaySslCertificate'의 버그 수정됨 [#9488]</span><span class="sxs-lookup"><span data-stu-id="76011-704">Fixed bug for 'Set-AzApplicationGatewaySslCertificate' [#9488]</span></span>
* <span data-ttu-id="76011-705">'AzureFirewall'에 'AllowActiveFTP' 매개 변수가 추가됨</span><span class="sxs-lookup"><span data-stu-id="76011-705">Added 'AllowActiveFTP' parameter to 'AzureFirewall'</span></span>
* <span data-ttu-id="76011-706">기능에 대한 새로운 명령이 업데이트됨: VirtualWan P2SVpnGateway에서 인터넷 보안 설정 사용/제거</span><span class="sxs-lookup"><span data-stu-id="76011-706">Updated below commands for feature: Enable internet security set/remove on VirtualWan P2SVpnGateway.</span></span>
- <span data-ttu-id="76011-707">'New-AzP2sVpnGateway' 업데이트됨: 고객이 P2SVpnGateway에서 인터넷 보안을 사용하도록 true를 설정할 수 있는 선택적 스위치 매개 변수 'EnableInternetSecurityFlag'가 추가되었으며, 이는 지점 및 사이트 간 클라이언트에 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="76011-707">Updated 'New-AzP2sVpnGateway': Added optional switch parameter 'EnableInternetSecurityFlag' for customers to set true to enable internet security on P2SVpnGateway, which will be applied for Point to site clients.</span></span>
- <span data-ttu-id="76011-708">'Update-AzP2sVpnGateway' 업데이트됨: 고객이 P2SVpnGateway에서 인터넷 보안을 활성화/비활성화하도록 true/false를 설정할 수 있는 선택적 스위치 매개 변수 'EnableInternetSecurityFlag' 또는 'DisableInternetSecurityFlag'가 추가되었으며, 이는 지점 및 사이트 간 클라이언트에 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="76011-708">Updated 'Update-AzP2sVpnGateway': Added optional switch parameters 'EnableInternetSecurityFlag' or 'DisableInternetSecurityFlag' for customers to set true/false to enable/disable internet security on P2SVpnGateway, which will be applied for Point to site clients.</span></span>
* <span data-ttu-id="76011-709">문제 해결을 위해 VirtualWan P2SVPNGateway를 재설정/재부팅할 수 있도록 새 cmdlet 'Reset-AzP2sVpnGateway'를 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-709">Added new cmdlet 'Reset-AzP2sVpnGateway' for customers to reset/reboot their VirtualWan P2SVpnGateway for troubleshooting.</span></span>
* <span data-ttu-id="76011-710">문제 해결을 위해 VirtualWan VpnGateway를 재설정/재부팅할 수 있도록 새 cmdlet 'Reset-AzVpnGateway'를 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-710">Added new cmdlet 'Reset-AzVpnGateway' for customers to reset/reboot their VirtualWan VpnGateway for troubleshooting.</span></span>
* <span data-ttu-id="76011-711">'Set-AzVirtualNetworkSubnetConfig' 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="76011-711">Updated 'Set-AzVirtualNetworkSubnetConfig'</span></span>
    - <span data-ttu-id="76011-712">매개 변수에 명시적으로 설정된 경우 서브넷의 NSG 및 라우팅 테이블 속성을 null로 설정 [# 1548][# 9718]</span><span class="sxs-lookup"><span data-stu-id="76011-712">Set NSG and Route Table properties of subnet to null if explicitly set in parameters [#1548][#9718]</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="76011-713">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="76011-713">Az.RecoveryServices</span></span>
* <span data-ttu-id="76011-714">워크로드 백업 항목에 대한 삭제 상태가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-714">Fixed the Delete State for workload Backup Items.</span></span>

#### <a name="azresources"></a><span data-ttu-id="76011-715">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="76011-715">Az.Resources</span></span>
* <span data-ttu-id="76011-716">Set-AzRoleAssignment에 대한 누락된 검사 추가됨</span><span class="sxs-lookup"><span data-stu-id="76011-716">Added missing check for Set-AzRoleAssignment</span></span>
* <span data-ttu-id="76011-717">'Get-AzResourceGroupDeploymentOperation'의 'SubscriptionId' 매개 변수에 호환성이 손상되는 변경 특성이 추가됨</span><span class="sxs-lookup"><span data-stu-id="76011-717">Added breaking change attribute to 'SubscriptionId' parameter of 'Get-AzResourceGroupDeploymentOperation'</span></span>
* <span data-ttu-id="76011-718">마지막으로 'Ignore' 리소스 변경을 표시하도록 ARM 템플릿 What-If cmdlet이 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="76011-718">Updated ARM template What-If cmdlets to show 'Ignore' resource changes last</span></span>
* <span data-ttu-id="76011-719">배포 cmdlet에 대한 보안 및 배열 매개 변수 직렬화 문제가 해결됨 [#12773]</span><span class="sxs-lookup"><span data-stu-id="76011-719">Fixed secure and array parameter serialization issues for deployment cmdlets [#12773]</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="76011-720">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="76011-720">Az.ServiceFabric</span></span>
* <span data-ttu-id="76011-721">관리형 클러스터 및 노드 유형에 대해 다음과 같은 새 cmdlet가 추가됨</span><span class="sxs-lookup"><span data-stu-id="76011-721">Added new cmdlets for managed clusters and node types:</span></span>
    - <span data-ttu-id="76011-722">'New-AzServiceFabricManagedCluster'</span><span class="sxs-lookup"><span data-stu-id="76011-722">'New-AzServiceFabricManagedCluster'</span></span>
    - <span data-ttu-id="76011-723">'Get-AzServiceFabricManagedCluster'</span><span class="sxs-lookup"><span data-stu-id="76011-723">'Get-AzServiceFabricManagedCluster'</span></span>
    - <span data-ttu-id="76011-724">'Set-AzServiceFabricManagedCluster'</span><span class="sxs-lookup"><span data-stu-id="76011-724">'Set-AzServiceFabricManagedCluster'</span></span>
    - <span data-ttu-id="76011-725">'Remove-AzServiceFabricManagedCluster'</span><span class="sxs-lookup"><span data-stu-id="76011-725">'Remove-AzServiceFabricManagedCluster'</span></span>
    - <span data-ttu-id="76011-726">'Add-AzServiceFabricManagedClusterClientCertificate'</span><span class="sxs-lookup"><span data-stu-id="76011-726">'Add-AzServiceFabricManagedClusterClientCertificate'</span></span>
    - <span data-ttu-id="76011-727">'Remove-AzServiceFabricManagedClusterClientCertificate'</span><span class="sxs-lookup"><span data-stu-id="76011-727">'Remove-AzServiceFabricManagedClusterClientCertificate'</span></span>
    - <span data-ttu-id="76011-728">'New-AzServiceFabricManagedNodeType'</span><span class="sxs-lookup"><span data-stu-id="76011-728">'New-AzServiceFabricManagedNodeType'</span></span>
    - <span data-ttu-id="76011-729">'Get-AzServiceFabricManagedNodeType'</span><span class="sxs-lookup"><span data-stu-id="76011-729">'Get-AzServiceFabricManagedNodeType'</span></span>
    - <span data-ttu-id="76011-730">'Set-AzServiceFabricManagedNodeType'</span><span class="sxs-lookup"><span data-stu-id="76011-730">'Set-AzServiceFabricManagedNodeType'</span></span>
    - <span data-ttu-id="76011-731">'Remove-AzServiceFabricManagedNodeType'</span><span class="sxs-lookup"><span data-stu-id="76011-731">'Remove-AzServiceFabricManagedNodeType'</span></span>
    - <span data-ttu-id="76011-732">'Add-AzServiceFabricManagedNodeTypeVMExtension'</span><span class="sxs-lookup"><span data-stu-id="76011-732">'Add-AzServiceFabricManagedNodeTypeVMExtension'</span></span>
    - <span data-ttu-id="76011-733">'Add-AzServiceFabricManagedNodeTypeVMSecret'</span><span class="sxs-lookup"><span data-stu-id="76011-733">'Add-AzServiceFabricManagedNodeTypeVMSecret'</span></span>
    - <span data-ttu-id="76011-734">'Remove-AzServiceFabricManagedNodeTypeVMExtension'</span><span class="sxs-lookup"><span data-stu-id="76011-734">'Remove-AzServiceFabricManagedNodeTypeVMExtension'</span></span>
    - <span data-ttu-id="76011-735">'Restart-AzServiceFabricManagedNodeTyp'</span><span class="sxs-lookup"><span data-stu-id="76011-735">'Restart-AzServiceFabricManagedNodeTyp'</span></span>
* <span data-ttu-id="76011-736">Service Fabric SDK를 버전 1.2.0으로 업그레이드했으며, 현재 모델에서는 서비스 패브릭 리소스 제공자 api-version 2020-03-01을, 관리형 클러스터에서는 2020-01-01-preview를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="76011-736">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2020-03-01 for the current model and 2020-01-01-preview for managed clusters.</span></span>

#### <a name="azsql"></a><span data-ttu-id="76011-737">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="76011-737">Az.Sql</span></span>
* <span data-ttu-id="76011-738">BackupStorageRedundancy가 'New-AzSqlInstance' 및 'Get-AzSqlInstance'에 추가됨</span><span class="sxs-lookup"><span data-stu-id="76011-738">Added BackupStorageRedundancy to 'New-AzSqlInstance' and 'Get-AzSqlInstance'</span></span>
* <span data-ttu-id="76011-739">'Get-AzSqlServerActiveDirectoryOnlyAuthentication' cmdlet이 추가됨</span><span class="sxs-lookup"><span data-stu-id="76011-739">Added cmdlet 'Get-AzSqlServerActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="76011-740">'Enable-AzSqlServerActiveDirectoryOnlyAuthentication' cmdlet이 추가됨</span><span class="sxs-lookup"><span data-stu-id="76011-740">Added cmdlet 'Enable-AzSqlServerActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="76011-741">Force 매개 변수가 'New-AzSqlInstance'에 추가됨</span><span class="sxs-lookup"><span data-stu-id="76011-741">Added Force parameter to 'New-AzSqlInstance'</span></span>
* <span data-ttu-id="76011-742">관리되는 데이터베이스 로그 재생 서비스용 cmdlet이 추가됨</span><span class="sxs-lookup"><span data-stu-id="76011-742">Added cmdlets for Managed Database Log Replay service</span></span>
    - <span data-ttu-id="76011-743">'Start-AzSqlInstanceDatabaseLogReplay'</span><span class="sxs-lookup"><span data-stu-id="76011-743">'Start-AzSqlInstanceDatabaseLogReplay'</span></span>
    - <span data-ttu-id="76011-744">'Get-AzSqlInstanceDatabaseLogReplay'</span><span class="sxs-lookup"><span data-stu-id="76011-744">'Get-AzSqlInstanceDatabaseLogReplay'</span></span>
    - <span data-ttu-id="76011-745">'Complete-AzSqlInstanceDatabaseLogReplay'</span><span class="sxs-lookup"><span data-stu-id="76011-745">'Complete-AzSqlInstanceDatabaseLogReplay'</span></span>
    - <span data-ttu-id="76011-746">'Stop-AzSqlInstanceDatabaseLogReplay'</span><span class="sxs-lookup"><span data-stu-id="76011-746">'Stop-AzSqlInstanceDatabaseLogReplay'</span></span>
* <span data-ttu-id="76011-747">'Get-AzSqlInstanceActiveDirectoryOnlyAuthentication' cmdlet이 추가됨</span><span class="sxs-lookup"><span data-stu-id="76011-747">Added cmdlet 'Get-AzSqlInstanceActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="76011-748">'Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication' cmdlet이 추가됨</span><span class="sxs-lookup"><span data-stu-id="76011-748">Added cmdlet 'Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="76011-749">'Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication' cmdlet이 추가됨</span><span class="sxs-lookup"><span data-stu-id="76011-749">Added cmdlet 'Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="76011-750">네트워크 격리 기능을 지원하기 위해 'New-AzSqlDatabaseImport' 및 'New-AzSqlDatabaseExport' cmdlet이 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="76011-750">Updated cmdlets 'New-AzSqlDatabaseImport' and 'New-AzSqlDatabaseExport' to support network isolation functionality</span></span>
* <span data-ttu-id="76011-751">'New-AzSqlDatabaseImportExisting' cmdlet이 추가됨</span><span class="sxs-lookup"><span data-stu-id="76011-751">Added cmdlet 'New-AzSqlDatabaseImportExisting'</span></span>
* <span data-ttu-id="76011-752">백업 스토리지 유형 사양을 지원하도록 데이터베이스 cmdlet이 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="76011-752">Updated Databases cmdlets to support backup storage type specification</span></span>
* <span data-ttu-id="76011-753">Force 매개 변수가 'New-AzSqlDatabase'에 추가됨</span><span class="sxs-lookup"><span data-stu-id="76011-753">Added Force parameter to 'New-AzSqlDatabase'</span></span>
* <span data-ttu-id="76011-754">'New-AzSqlDatabase'의 영역 선택에서 BackupStorageRedundancy 구성에 대한 경고가 추가됨</span><span class="sxs-lookup"><span data-stu-id="76011-754">Added warning for BackupStorageRedundancy configuration in select regions in 'New-AzSqlDatabase'</span></span>
* <span data-ttu-id="76011-755">ResourceId 및 InputObject를 포함하도록 서버 및 인스턴스에 대한 ActiveDirectoryOnlyAuthentication cmdlet이 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="76011-755">Updated ActiveDirectoryOnlyAuthentication cmdlets for server and instance to include ResourceId and InputObject</span></span>

#### <a name="azstorage"></a><span data-ttu-id="76011-756">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="76011-756">Az.Storage</span></span>
* <span data-ttu-id="76011-757">Microsoft.Azure.Storage.DataMovement 2.0.0로 업그레이드하여 blob 업로드 실패 수정됨 [#12220]</span><span class="sxs-lookup"><span data-stu-id="76011-757">Fixed upload blob fail by upgrade to Microsoft.Azure.Storage.DataMovement 2.0.0 [#12220]</span></span>
* <span data-ttu-id="76011-758">지정 시간 복원 지원</span><span class="sxs-lookup"><span data-stu-id="76011-758">Supported Point In Time Restore</span></span>
    - <span data-ttu-id="76011-759">'Enable-AzStorageBlobRestorePolicy'</span><span class="sxs-lookup"><span data-stu-id="76011-759">'Enable-AzStorageBlobRestorePolicy'</span></span>
    - <span data-ttu-id="76011-760">'Disable-AzStorageBlobRestorePolicy'</span><span class="sxs-lookup"><span data-stu-id="76011-760">'Disable-AzStorageBlobRestorePolicy'</span></span>
    - <span data-ttu-id="76011-761">'New-AzStorageBlobRangeToRestore'</span><span class="sxs-lookup"><span data-stu-id="76011-761">'New-AzStorageBlobRangeToRestore'</span></span>
    - <span data-ttu-id="76011-762">'Restore-AzStorageBlobRange'</span><span class="sxs-lookup"><span data-stu-id="76011-762">'Restore-AzStorageBlobRange'</span></span>
* <span data-ttu-id="76011-763">-IncludeBlobRestoreStatus 매개 변수와 함께 get-AzureRMStorageAccount를 실행하여 스토리지 계정의 blob 복원 상태 가져오기 지원</span><span class="sxs-lookup"><span data-stu-id="76011-763">Supported get blob restore status of Storage account by run get-AzureRMStorageAccount with parameter -IncludeBlobRestoreStatus</span></span> 
    - <span data-ttu-id="76011-764">'Get-AzureRMStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="76011-764">'Get-AzureRMStorageAccount'</span></span>
* <span data-ttu-id="76011-765">예정된 cmdlet 출력 변경에 대해 호환성이 손상되는 변경 경고 메시지가 추가됨</span><span class="sxs-lookup"><span data-stu-id="76011-765">Added breaking change warning message for upcoming cmdlet output change</span></span>
    - <span data-ttu-id="76011-766">'Get-AzStorageContainerStoredAccessPolicy'</span><span class="sxs-lookup"><span data-stu-id="76011-766">'Get-AzStorageContainerStoredAccessPolicy'</span></span>
    - <span data-ttu-id="76011-767">'Set-AzStorageContainerStoredAccessPolicy'</span><span class="sxs-lookup"><span data-stu-id="76011-767">'Set-AzStorageContainerStoredAccessPolicy'</span></span>
    - <span data-ttu-id="76011-768">'Set-AzStorageAccountManagementPolicy'</span><span class="sxs-lookup"><span data-stu-id="76011-768">'Set-AzStorageAccountManagementPolicy'</span></span>
    - <span data-ttu-id="76011-769">'Get-AzStorageAccountManagementPolicy'</span><span class="sxs-lookup"><span data-stu-id="76011-769">'Get-AzStorageAccountManagementPolicy'</span></span>
    - <span data-ttu-id="76011-770">'Add-AzStorageAccountManagementPolicyAction'</span><span class="sxs-lookup"><span data-stu-id="76011-770">'Add-AzStorageAccountManagementPolicyAction'</span></span>
    - <span data-ttu-id="76011-771">'New-AzStorageAccountManagementPolicyRule'</span><span class="sxs-lookup"><span data-stu-id="76011-771">'New-AzStorageAccountManagementPolicyRule'</span></span>
* <span data-ttu-id="76011-772">Microsoft.Azure.Cosmos.Table SDK를 1.0.8로 업그레이드</span><span class="sxs-lookup"><span data-stu-id="76011-772">Upgraded Microsoft.Azure.Cosmos.Table SDK to 1.0.8</span></span>

### <a name="thanks-to-our-community-contributors"></a><span data-ttu-id="76011-773">커뮤니티 기여자에게 감사드립니다.</span><span class="sxs-lookup"><span data-stu-id="76011-773">Thanks to our community contributors</span></span>
* <span data-ttu-id="76011-774">Thomas Van Laere(@ThomVanL), Dockerfile-alpine-3.10 추가(#12911)</span><span class="sxs-lookup"><span data-stu-id="76011-774">Thomas Van Laere (@ThomVanL), Add Dockerfile-alpine-3.10 (#12911)</span></span> 
* <span data-ttu-id="76011-775">Lohith Chowdary Chilukuri(@Lochiluk), Remove-AzNetworkInterfaceIpConfig.md 업데이트(#12807)</span><span class="sxs-lookup"><span data-stu-id="76011-775">Lohith Chowdary Chilukuri (@Lochiluk), Update Remove-AzNetworkInterfaceIpConfig.md (#12807)</span></span> 
* <span data-ttu-id="76011-776">Roberth Strand(@roberthstrand), Get-AzResourceGroup - 새로운 예제 및 정리(#12828)</span><span class="sxs-lookup"><span data-stu-id="76011-776">Roberth Strand (@roberthstrand), Get-AzResourceGroup - New example, and cleanup (#12828)</span></span> 
* <span data-ttu-id="76011-777">Ravi Mishra(@inmishrar), Azure 웹앱 런타임 스택을 DOTNETCORE로 업데이트(#12833)</span><span class="sxs-lookup"><span data-stu-id="76011-777">Ravi Mishra (@inmishrar), update Azure Web App runtime stack to DOTNETCORE (#12833)</span></span> 
* <span data-ttu-id="76011-778">@jack-education, NSG 및 라우팅 테이블을 서브넷에서 제거할 수 있도록 Set-AzVirtualNetworkSubnetConfig를 업데이트(# 12351)</span><span class="sxs-lookup"><span data-stu-id="76011-778">@jack-education, Updated Set-AzVirtualNetworkSubnetConfig to allow NSG and Route Table to be removed from subnet (#12351)</span></span> 
* <span data-ttu-id="76011-779">@hagop-globanet, Add-AzApplicationGatewayCustomError.md 업데이트(#12784)</span><span class="sxs-lookup"><span data-stu-id="76011-779">@hagop-globanet, Update Add-AzApplicationGatewayCustomError.md (#12784)</span></span> 
* <span data-ttu-id="76011-780">Joshua Van Daalen(@greenSacrifice)</span><span class="sxs-lookup"><span data-stu-id="76011-780">Joshua Van Daalen (@greenSacrifice)</span></span>
  * <span data-ttu-id="76011-781">속성(Property) 철자를 속성(Property)으로 업데이트(#12821)</span><span class="sxs-lookup"><span data-stu-id="76011-781">Update spelling of Property to Property (#12821)</span></span> 
  * <span data-ttu-id="76011-782">New-AzResourceLock.md 예제 업데이트(#12806)</span><span class="sxs-lookup"><span data-stu-id="76011-782">Update New-AzResourceLock.md examples (#12806)</span></span>
* <span data-ttu-id="76011-783">Eragon Riddle(@eragonriddle), 예제에서 매개 변수 필드 이름 수정(#12825)</span><span class="sxs-lookup"><span data-stu-id="76011-783">Eragon Riddle (@eragonriddle), Corrected parameter field name in the example (#12825)</span></span> 
* <span data-ttu-id="76011-784">@rossifumax, New-AzConfigurationAssignment.md의 오타 수정(#12701)</span><span class="sxs-lookup"><span data-stu-id="76011-784">@rossifumax, Fix typo in New-AzConfigurationAssignment.md (#12701)</span></span>

## <a name="461---august-2020"></a><span data-ttu-id="76011-785">4.6.1 - 2020년 8월</span><span class="sxs-lookup"><span data-stu-id="76011-785">4.6.1 - August 2020</span></span>
#### <a name="azcompute"></a><span data-ttu-id="76011-786">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="76011-786">Az.Compute</span></span>
* <span data-ttu-id="76011-787">'New-AzVm'에서 '-EncryptionAtHost' 매개 변수를 패치하여 기본값인 false가 제거됨[#12776]</span><span class="sxs-lookup"><span data-stu-id="76011-787">Patched '-EncryptionAtHost' parameter in 'New-AzVm' to remove default value of false [#12776]</span></span>

## <a name="460---august-2020"></a><span data-ttu-id="76011-788">4.6.0 - 2020년 8월</span><span class="sxs-lookup"><span data-stu-id="76011-788">4.6.0 - August 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="76011-789">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="76011-789">Az.Accounts</span></span>
* <span data-ttu-id="76011-790">검색 엔드포인트가 기본 AzureCloud나 기타 공용 환경을 반환하지 않는 경우 모든 퍼블릭 클라우드 환경이 로드됨 [#12633]</span><span class="sxs-lookup"><span data-stu-id="76011-790">Loaded all public cloud environments when discovery endpoint doesn't return default AzureCloud or other public environments [#12633]</span></span>
* <span data-ttu-id="76011-791">'Get-AzSubscription'에서 SubscriptionPolicies가 노출됨 [#12551]</span><span class="sxs-lookup"><span data-stu-id="76011-791">Exposed SubscriptionPolicies in 'Get-AzSubscription' [#12551]</span></span>

#### <a name="azautomation"></a><span data-ttu-id="76011-792">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="76011-792">Az.Automation</span></span>
* <span data-ttu-id="76011-793">Hybrid Worker 그룹을 지정하기 위해 'Set-AzAutomationWebhook'에 '-RunOn' 매개 변수가 추가됨</span><span class="sxs-lookup"><span data-stu-id="76011-793">Added '-RunOn' parameters to 'Set-AzAutomationWebhook' to specify a Hybrid Worker Group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="76011-794">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="76011-794">Az.Compute</span></span>
* <span data-ttu-id="76011-795">'New-AzVm', 'New-AzVmss', 'New-AzVMConfig', 'New-AzVmssConfig', 'Update-AzVM', 'Update-AzVmss'에 '-EncryptionAtHost' 매개 변수가 추가됨</span><span class="sxs-lookup"><span data-stu-id="76011-795">Added '-EncryptionAtHost' parameter to 'New-AzVm', 'New-AzVmss', 'New-AzVMConfig', 'New-AzVmssConfig', 'Update-AzVM', and 'Update-AzVmss'</span></span>
* <span data-ttu-id="76011-796">'Get-AzVM' 및 'Get-AzVmss' 반환 개체에 'SecurityProfile'이 추가됨</span><span class="sxs-lookup"><span data-stu-id="76011-796">Added 'SecurityProfile' to 'Get-AzVM' and 'Get-AzVmss' return object</span></span>
* <span data-ttu-id="76011-797">'-InstanceView' 스위치가 'Get-AzHostGroup'에 선택적 매개 변수로 추가됨</span><span class="sxs-lookup"><span data-stu-id="76011-797">Added '-InstanceView' switch as optional parameter to 'Get-AzHostGroup'</span></span>
* <span data-ttu-id="76011-798">새 cmdlet 'Invoke-AzVmPatchAssessment'가 추가됨</span><span class="sxs-lookup"><span data-stu-id="76011-798">Added new cmdlet 'Invoke-AzVmPatchAssessment'</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="76011-799">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="76011-799">Az.DataFactory</span></span>
* <span data-ttu-id="76011-800">PSPipelineRun 클래스에 누락된 속성이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-800">Added missing properties to PSPipelineRun class.</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="76011-801">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="76011-801">Az.HDInsight</span></span>
* <span data-ttu-id="76011-802">호스트 기능에서 암호화를 사용하여 클러스터를 만드는 것이 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="76011-802">Supported creating cluster with encryption at host feature.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="76011-803">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="76011-803">Az.KeyVault</span></span>
* <span data-ttu-id="76011-804">일시 삭제 사용 안 함 계획에 대한 경고 메시지가 추가됨</span><span class="sxs-lookup"><span data-stu-id="76011-804">Added warning messages for planning to disable soft delete</span></span>
* <span data-ttu-id="76011-805">특성 SecretValueText 제거 계획에 대한 경고 메시지가 추가됨</span><span class="sxs-lookup"><span data-stu-id="76011-805">Added warning messages for planning to remove attribute SecretValueText</span></span>

#### <a name="azmaintenance"></a><span data-ttu-id="76011-806">Az.Maintenance</span><span class="sxs-lookup"><span data-stu-id="76011-806">Az.Maintenance</span></span>
* <span data-ttu-id="76011-807">'New-AzMaintenanceConfiguration'에 선택적 일정 관련 필드가 추가됨</span><span class="sxs-lookup"><span data-stu-id="76011-807">Added optional schedule related fields to 'New-AzMaintenanceConfiguration'</span></span>
* <span data-ttu-id="76011-808">'Get-AzMaintenancePublicConfiguration'에 대한 새 cmdlet이 추가됨</span><span class="sxs-lookup"><span data-stu-id="76011-808">Added new cmdlet for 'Get-AzMaintenancePublicConfiguration'</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="76011-809">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="76011-809">Az.ManagedServices</span></span>
* <span data-ttu-id="76011-810">관리되는 서비스 할당 및 정의의 cmdlet에 대한 호환성이 손상되는 변경 경고가 추가됨</span><span class="sxs-lookup"><span data-stu-id="76011-810">Added breaking change warnings on cmdlets of managed services assignment and definition</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="76011-811">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="76011-811">Az.Monitor</span></span>
* <span data-ttu-id="76011-812">로그 및 메트릭 사용을 분리하기 위해 'Set-AzDiagnosticSetting'에 설정된 매개 변수가 확장됨 [#12482]</span><span class="sxs-lookup"><span data-stu-id="76011-812">Extended the parameter set in 'Set-AzDiagnosticSetting' for separation of Logs and Metrics enablement [#12482]</span></span>
* <span data-ttu-id="76011-813">파이프라인에서 메트릭 경고를 가져오는 경우 'Add-AzMetricAlertRuleV2'에 대한 버그가 수정됨</span><span class="sxs-lookup"><span data-stu-id="76011-813">Fixed bug for 'Add-AzMetricAlertRuleV2' when getting metric alert from pipeline</span></span>

#### <a name="azresources"></a><span data-ttu-id="76011-814">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="76011-814">Az.Resources</span></span>
* <span data-ttu-id="76011-815">Azure Policy를 통해 별칭을 수정할 수 있는지 여부를 나타내는 정보를 포함하도록 'Get-AzPolicyAlias' 응답이 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="76011-815">Updated 'Get-AzPolicyAlias' response to include information indicating whether the alias is modifiable by Azure Policy.</span></span>
* <span data-ttu-id="76011-816">새 cmdlet 'Set-AzRoleAssignment'가 생성됨</span><span class="sxs-lookup"><span data-stu-id="76011-816">Created new cmdlet 'Set-AzRoleAssignment'</span></span>
* <span data-ttu-id="76011-817">관리 그룹 범위에서 ARM 템플릿 What-If 결과를 가져오는 'Get-AzDeploymentManagementGroupWhatIfResult'가 추가됨</span><span class="sxs-lookup"><span data-stu-id="76011-817">Added 'Get-AzDeploymentManagementGroupWhatIfResult' for getting ARM template What-If results at management Group scope</span></span>
* <span data-ttu-id="76011-818">테넌트 범위에서 ARM 템플릿 What-If 결과를 가져오는 'Get-AzTenantWhatIfResult' 새 cmdlet이 추가됨</span><span class="sxs-lookup"><span data-stu-id="76011-818">Added 'Get-AzTenantWhatIfResult' new cmdlet for getting ARM template What-If results at tenant scope</span></span>
* <span data-ttu-id="76011-819">ARM 템플릿 What-If 결과를 사용하도록 'New-AzManagementGroupDeployment' 및 'New-AzTenantDeployment'에 대한 '-WhatIf' 및 '-Confirm'이 재정의됨</span><span class="sxs-lookup"><span data-stu-id="76011-819">Overrode '-WhatIf' and '-Confirm' for 'New-AzManagementGroupDeployment' and 'New-AzTenantDeployment' to use ARM template What-If results</span></span>
* <span data-ttu-id="76011-820">새 배포 cmdlet에 대한 '-WhatIf' 및 '-Confirm' 동작이 False를 준수하도록 수정됨</span><span class="sxs-lookup"><span data-stu-id="76011-820">Fixed the behaviors of '-WhatIf' and '-Confirm' for new deployment cmdlets so they comply with False and</span></span> 
* <span data-ttu-id="76011-821">'-TemplateObject' 및 'TemplateParameterObject'에 대한 직렬화 오류가 수정됨 [#1528] [#6292]</span><span class="sxs-lookup"><span data-stu-id="76011-821">Fixed serialization error for '-TemplateObject' and 'TemplateParameterObject' [#1528] [#6292]</span></span>
* <span data-ttu-id="76011-822">예정된 출력 형식 변경을 위해 'Get-AzResourceGroupDeploymentOperation'에 호환성이 손상되는 변경 특성이 추가됨</span><span class="sxs-lookup"><span data-stu-id="76011-822">Added breaking change attribute to 'Get-AzResourceGroupDeploymentOperation' for the upcoming output type change</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="76011-823">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="76011-823">Az.SignalR</span></span>
* <span data-ttu-id="76011-824">'Restart-AzSignalR' 및 'Update-AzSignalR' 도움말 파일 오류가 수정됨</span><span class="sxs-lookup"><span data-stu-id="76011-824">Fixed 'Restart-AzSignalR' and 'Update-AzSignalR' help files errors</span></span>
* <span data-ttu-id="76011-825">'Update-AzSignalRNetworkAcl', 'Set-AzSignalRUpstream' cmdlet이 추가됨</span><span class="sxs-lookup"><span data-stu-id="76011-825">Added cmdlets 'Update-AzSignalRNetworkAcl', 'Set-AzSignalRUpstream'</span></span>

#### <a name="azstorage"></a><span data-ttu-id="76011-826">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="76011-826">Az.Storage</span></span>
* <span data-ttu-id="76011-827">지원되는 Blob 쿼리 가속</span><span class="sxs-lookup"><span data-stu-id="76011-827">Supported blob query acceleration</span></span>
    -  <span data-ttu-id="76011-828">'Get-AzStorageBlobQueryResult'</span><span class="sxs-lookup"><span data-stu-id="76011-828">'Get-AzStorageBlobQueryResult'</span></span>
    -  <span data-ttu-id="76011-829">'New-AzStorageBlobQueryConfig'</span><span class="sxs-lookup"><span data-stu-id="76011-829">'New-AzStorageBlobQueryConfig'</span></span>
* <span data-ttu-id="76011-830">도움말 파일 업데이트, 자세한 설명 추가 및 오타 수정</span><span class="sxs-lookup"><span data-stu-id="76011-830">Updated help file, added more description, and fixed typo</span></span>
    -  <span data-ttu-id="76011-831">'Start-AzStorageBlobCopy'</span><span class="sxs-lookup"><span data-stu-id="76011-831">'Start-AzStorageBlobCopy'</span></span>
    -  <span data-ttu-id="76011-832">'Get-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="76011-832">'Get-AzDataLakeGen2Item'</span></span>
* <span data-ttu-id="76011-833">관련 하위 디렉터리가 없는 경우 Blob 다운로드 실패가 수정됨 [#12592]</span><span class="sxs-lookup"><span data-stu-id="76011-833">Fixed download blob fail when related sub directory not exist [#12592]</span></span>
    -  <span data-ttu-id="76011-834">'Get-AzStorageBlobContent'</span><span class="sxs-lookup"><span data-stu-id="76011-834">'Get-AzStorageBlobContent'</span></span>
* <span data-ttu-id="76011-835">스토리지 계정에 대해 개체 복제 정책 설정/가져오기/제거가 지원됨</span><span class="sxs-lookup"><span data-stu-id="76011-835">Supported Set/Get/Remove Object Replication Policy on Storage accounts</span></span>
    - <span data-ttu-id="76011-836">'New-AzStorageObjectReplicationPolicyRule'</span><span class="sxs-lookup"><span data-stu-id="76011-836">'New-AzStorageObjectReplicationPolicyRule'</span></span>
    - <span data-ttu-id="76011-837">'Set-AzStorageObjectReplicationPolicy'</span><span class="sxs-lookup"><span data-stu-id="76011-837">'Set-AzStorageObjectReplicationPolicy'</span></span>
    - <span data-ttu-id="76011-838">'Get-AzStorageObjectReplicationPolicy'</span><span class="sxs-lookup"><span data-stu-id="76011-838">'Get-AzStorageObjectReplicationPolicy'</span></span>
    - <span data-ttu-id="76011-839">'Remove-AzStorageObjectReplicationPolicy'</span><span class="sxs-lookup"><span data-stu-id="76011-839">'Remove-AzStorageObjectReplicationPolicy'</span></span>
* <span data-ttu-id="76011-840">스토리지 계정의 Blob Service에서 ChangeFeed 사용/사용 안 함이 지원됨</span><span class="sxs-lookup"><span data-stu-id="76011-840">Supported enable/disable ChangeFeed on Blob Service of a Storage account</span></span>
    - <span data-ttu-id="76011-841">'Update-AzStorageBlobServiceProperty'</span><span class="sxs-lookup"><span data-stu-id="76011-841">'Update-AzStorageBlobServiceProperty'</span></span>

## <a name="450---august-2020"></a><span data-ttu-id="76011-842">4.5.0 - 2020년 8월</span><span class="sxs-lookup"><span data-stu-id="76011-842">4.5.0 - August 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="76011-843">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="76011-843">Az.Accounts</span></span>
* <span data-ttu-id="76011-844">매개 변수 'MaxContextPopulation'을 허용하도록 'Connect-AzAccount' 업데이트됨 [# 9865]</span><span class="sxs-lookup"><span data-stu-id="76011-844">Updated 'Connect-AzAccount' to accept parameter 'MaxContextPopulation' [#9865]</span></span>
* <span data-ttu-id="76011-845">SubscriptionClient 버전이 2019-06-01로 업데이트되고 테넌트 도메인을 표시 [#9838]</span><span class="sxs-lookup"><span data-stu-id="76011-845">Updated SubscriptionClient version to 2019-06-01 and display tenant domains [#9838]</span></span>
* <span data-ttu-id="76011-846">구독의 managedBy 테넌트 정보 및 홈 테넌트 지원</span><span class="sxs-lookup"><span data-stu-id="76011-846">Supported home tenant and managedBy tenant information of subscription</span></span>
* <span data-ttu-id="76011-847">원격 분석 데이터의 모듈 이름, 버전 정보 수정</span><span class="sxs-lookup"><span data-stu-id="76011-847">Corrected module name, version info in telemetry data</span></span>
* <span data-ttu-id="76011-848">환경 메타데이터 엔드포인트가 호환되지 않는 값을 반환하는 경우 SqlDatabaseDnsSuffix 및 ServiceManagementUrl이 조정됨</span><span class="sxs-lookup"><span data-stu-id="76011-848">Adjusted SqlDatabaseDnsSuffix and ServiceManagementUrl if environment metadata endpoint returns incompatible value</span></span>

#### <a name="azaks"></a><span data-ttu-id="76011-849">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="76011-849">Az.Aks</span></span>
* <span data-ttu-id="76011-850">'ClientIdAndSecret'을 'ServicePrincipalIdAndSecret'으로 제거하고 'ClientIdAndSecret'을 별칭으로 설정함 [#12381]</span><span class="sxs-lookup"><span data-stu-id="76011-850">Removed 'ClientIdAndSecret' to 'ServicePrincipalIdAndSecret' and set 'ClientIdAndSecret' as an alias [#12381].</span></span>
* <span data-ttu-id="76011-851">'Get-AzAks'/'New-AzAks'/'Remove-AzAks'/'Set-AzAks'를 'Get-AzAksCluster'/'New-AzAksCluster'/'Remove-AzAksCluster'/'Set-AzAksCluster'로 제거하고 원본을 별칭으로 설정함 [#12373].</span><span class="sxs-lookup"><span data-stu-id="76011-851">Removed 'Get-AzAks'/'New-AzAks'/'Remove-AzAks'/'Set-AzAks' to 'Get-AzAksCluster'/'New-AzAksCluster'/'Remove-AzAksCluster'/'Set-AzAksCluster' and set the original ones as alias [#12373].</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="76011-852">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="76011-852">Az.ApiManagement</span></span>
* <span data-ttu-id="76011-853">새 'Add-AzApiManagementApiToGateway' cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-853">Added new 'Add-AzApiManagementApiToGateway' cmdlet.</span></span>
* <span data-ttu-id="76011-854">새 'Get-AzApiManagementGateway' cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-854">Added new 'Get-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="76011-855">새 'Get-AzApiManagementGatewayHostnameConfiguration' cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-855">Added new 'Get-AzApiManagementGatewayHostnameConfiguration' cmdlet.</span></span>
* <span data-ttu-id="76011-856">새 'Get-AzApiManagementGatewayKey' cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-856">Added new 'Get-AzApiManagementGatewayKey' cmdlet.</span></span>
* <span data-ttu-id="76011-857">새 'New-AzApiManagementGateway' cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-857">Added new 'New-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="76011-858">새 'New-AzApiManagementGatewayHostnameConfiguration' cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-858">Added new 'New-AzApiManagementGatewayHostnameConfiguration' cmdlet.</span></span>
* <span data-ttu-id="76011-859">새 'New-AzApiManagementResourceLocationObject' cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-859">Added new 'New-AzApiManagementResourceLocationObject' cmdlet.</span></span>
* <span data-ttu-id="76011-860">새 'Remove-AzApiManagementApiFromGateway' cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-860">Added new 'Remove-AzApiManagementApiFromGateway' cmdlet.</span></span>
* <span data-ttu-id="76011-861">새 'Remove-AzApiManagementGateway' cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-861">Added new 'Remove-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="76011-862">새 'Remove-AzApiManagementGatewayHostnameConfiguration' cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-862">Added new 'Remove-AzApiManagementGatewayHostnameConfiguration' cmdlet.</span></span>
* <span data-ttu-id="76011-863">새 'Update-AzApiManagementGateway' cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-863">Added new 'Update-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="76011-864">'Get-AzApiManagementApi' cmdlet에 선택적 [-GatewayId] 매개 변수가 새로 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-864">Added new optional [-GatewayId] parameter to the 'Get-AzApiManagementApi' cmdlet.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="76011-865">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="76011-865">Az.CognitiveServices</span></span>
* <span data-ttu-id="76011-866">'Deny'가 특히 NetworkRules 기본 작업으로 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="76011-866">Used 'Deny' specifically as NetworkRules default action.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="76011-867">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="76011-867">Az.FrontDoor</span></span>
* <span data-ttu-id="76011-868">Enum.Parse가 null 값을 Enabled 또는 Disabled 열거형 값으로 강제 변환하려는 경우 예외가 throw되는 문제를 수정했습니다. [#12344]</span><span class="sxs-lookup"><span data-stu-id="76011-868">Fixed an issue where an exception is being thrown when Enum.Parse tries to coerce a null value to an Enabled or Disabled enum values [#12344]</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="76011-869">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="76011-869">Az.HDInsight</span></span>
* <span data-ttu-id="76011-870">전송 중 암호화 기능을 사용하여 클러스터를 만드는 것이 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="76011-870">Supported creating cluster with encryption in transit feature.</span></span>
    - <span data-ttu-id="76011-871">cmdlet 'New-AzHDInsightCluster'에 새 매개 변수 'EncryptionInTransit' 추가</span><span class="sxs-lookup"><span data-stu-id="76011-871">Add new parameter 'EncryptionInTransit' to the cmdlet 'New-AzHDInsightCluster'</span></span>
    - <span data-ttu-id="76011-872">cmdlet 'New-AzHDInsightClusterConfig'에 새 매개 변수 'EncryptionInTransit' 추가</span><span class="sxs-lookup"><span data-stu-id="76011-872">Add new parameter 'EncryptionInTransit' to the cmdlet 'New-AzHDInsightClusterConfig'</span></span>
* <span data-ttu-id="76011-873">프라이빗 링크 기능을 사용하여 클러스터를 만드는 것이 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="76011-873">Supported creating cluster with private link feature:</span></span>
    - <span data-ttu-id="76011-874">cmdlet 'New-AzHDInsightCluster'에 새 매개 변수 'PublicNetworkAccessType' 및 'OutboundPublicNetworkAccessType' 추가</span><span class="sxs-lookup"><span data-stu-id="76011-874">Add new parameter 'PublicNetworkAccessType' and 'OutboundPublicNetworkAccessType' to the cmdlet 'New-AzHDInsightCluster'</span></span>
    - <span data-ttu-id="76011-875">cmdlet 'New-AzHDInsightClusterConfig'에 새 매개 변수 'PublicNetworkAccessType' 및 'OutboundPublicNetworkAccessType' 추가</span><span class="sxs-lookup"><span data-stu-id="76011-875">Add new parameter 'PublicNetworkAccessType' and 'OutboundPublicNetworkAccessType' to the cmdlet 'New-AzHDInsightClusterConfig'</span></span>
* <span data-ttu-id="76011-876">'New-AzHDInsightCluster' 또는 'Get-AzHDInsightCluster'를 호출하는 경우 가상 네트워크 정보가 반환됨</span><span class="sxs-lookup"><span data-stu-id="76011-876">Returned virtual network information when calling 'New-AzHDInsightCluster' or 'Get-AzHDInsightCluster'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="76011-877">Az.Network</span><span class="sxs-lookup"><span data-stu-id="76011-877">Az.Network</span></span>
* <span data-ttu-id="76011-878">'Remove-AzExpressRouteCircuitConnectionConfig'에 AddressPrefixType 매개 변수 지원 추가</span><span class="sxs-lookup"><span data-stu-id="76011-878">Added support for AddressPrefixType parameter to 'Remove-AzExpressRouteCircuitConnectionConfig'</span></span>
* <span data-ttu-id="76011-879">작업을 중단하지 않는 변경이 추가됨: 'Remove-AzExpressRouteCircutPeeringConfig'의 프라이빗 피어링을 위한 PeerAddressType 기능</span><span class="sxs-lookup"><span data-stu-id="76011-879">Added non-breaking changes: PeerAddressType functionality for Private Peering in 'Remove-AzExpressRouteCircutPeeringConfig'.</span></span>
* <span data-ttu-id="76011-880">AddressPrefixType 및 PeerAddressType 매개 변수의 대/소문자를 무시하도록 코드가 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-880">Code changed to ignore case for AddressPrefixType and PeerAddressType parameter.</span></span>
* <span data-ttu-id="76011-881">'New-AzLoadBalancerFrontendIpConfig', 'New-AzPublicIpAddress' 및 'New-AzPublicIpPrefix'에 대한 경고 메시지를 수정했습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-881">Modified the warning message for 'New-AzLoadBalancerFrontendIpConfig', 'New-AzPublicIpAddress' and 'New-AzPublicIpPrefix'.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="76011-882">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="76011-882">Az.OperationalInsights</span></span>
* <span data-ttu-id="76011-883">'Remove-AzOperationalInsightsworkspace'에 대한 '-ForceDelete' 옵션이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-883">Added '-ForceDelete' option for 'Remove-AzOperationalInsightsworkspace'</span></span>
* <span data-ttu-id="76011-884">새 cmdlet 'Get-AzOperationalInsightsDeletedWorkspace'가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-884">Added new cmdlet 'Get-AzOperationalInsightsDeletedWorkspace'</span></span>
* <span data-ttu-id="76011-885">새 cmdlet 'Restore-AzOperationalInsightsWorkspace'가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-885">Added new cmdlet 'Restore-AzOperationalInsightsWorkspace'</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="76011-886">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="76011-886">Az.RecoveryServices</span></span>
* <span data-ttu-id="76011-887">Azure Backup 컨테이너/항목 검색 환경이 개선되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-887">Improved the Azure Backup container/item discovery experience.</span></span>

#### <a name="azresources"></a><span data-ttu-id="76011-888">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="76011-888">Az.Resources</span></span>
* <span data-ttu-id="76011-889">'New-AzRoleAssignment'에 'Condition', 'ConditionVersion' 및 'Description' 속성을 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-889">Added properties 'Condition', 'ConditionVersion' and 'Description' to 'New-AzRoleAssignment'</span></span>
    - <span data-ttu-id="76011-890">여기에는 데이터 모델과 관련된 모든 변경 사항이 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="76011-890">This included all the relevant changes to the data models</span></span>

#### <a name="azsql"></a><span data-ttu-id="76011-891">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="76011-891">Az.Sql</span></span>
* <span data-ttu-id="76011-892">'New-AzSqlServer' 'Set-AzSqlServer'에서 서버 이름 대/소문자를 구분하지 않는 잠재적인 오류를 수정했습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-892">Fixed potential server name case insensitive error in 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>
* <span data-ttu-id="76011-893">'New-AzSqlDatabaseSecondary'의 기존 데이터베이스 오류에서 반환되는 잘못된 데이터베이스 이름을 수정했습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-893">Fixed wrong database name returned on existing database error in 'New-AzSqlDatabaseSecondary'</span></span>

#### <a name="azstorage"></a><span data-ttu-id="76011-894">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="76011-894">Az.Storage</span></span>
* <span data-ttu-id="76011-895">새 권한 x,t를 사용하여 컨테이너/blob Sas 토큰 만들기 지원</span><span class="sxs-lookup"><span data-stu-id="76011-895">Supported create container/blob Sas token with new permission x,t</span></span>
    -  <span data-ttu-id="76011-896">'New-AzStorageBlobSASToken'</span><span class="sxs-lookup"><span data-stu-id="76011-896">'New-AzStorageBlobSASToken'</span></span>
    -  <span data-ttu-id="76011-897">'New-AzStorageContainerSASToken'</span><span class="sxs-lookup"><span data-stu-id="76011-897">'New-AzStorageContainerSASToken'</span></span>
* <span data-ttu-id="76011-898">새 권한 x,t,f를 사용하여 계정 Sas 토큰 만들기 지원</span><span class="sxs-lookup"><span data-stu-id="76011-898">Supported create account Sas token with new permission x,t,f</span></span>
    -  <span data-ttu-id="76011-899">'New-AzStorageAccountSASToken'</span><span class="sxs-lookup"><span data-stu-id="76011-899">'New-AzStorageAccountSASToken'</span></span>
* <span data-ttu-id="76011-900">단일 파일 사용량 공유 가져오기 지원</span><span class="sxs-lookup"><span data-stu-id="76011-900">Supported get single file share usage</span></span>
    - <span data-ttu-id="76011-901">'Get-AzRmStorageShare'</span><span class="sxs-lookup"><span data-stu-id="76011-901">'Get-AzRmStorageShare'</span></span>

## <a name="440---july-2020"></a><span data-ttu-id="76011-902">4.4.0 - 2020년 7월</span><span class="sxs-lookup"><span data-stu-id="76011-902">4.4.0 - July 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="76011-903">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="76011-903">Az.Accounts</span></span>
* <span data-ttu-id="76011-904">새 cmdlet 'Invoke-AzRestMethod' 추가</span><span class="sxs-lookup"><span data-stu-id="76011-904">Added new cmdlet 'Invoke-AzRestMethod'</span></span>
* <span data-ttu-id="76011-905">'Start-Job'을 사용하여 여러 Azure PowerShell cmdlet을 실행하는 등 다중 프로세스 시나리오에서 인증 오류를 발생시킬 수 있는 문제 해결 [#9448]</span><span class="sxs-lookup"><span data-stu-id="76011-905">Fixed an issue that may cause authentication errors in multi-process scenarios such as running multiple Azure PowerShell cmdlets using 'Start-Job' [#9448]</span></span>

#### <a name="azaks"></a><span data-ttu-id="76011-906">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="76011-906">Az.Aks</span></span>
* <span data-ttu-id="76011-907">'Get-AzAks'가 모든 클러스터를 가져오지 않는 버그 수정 [#12296]</span><span class="sxs-lookup"><span data-stu-id="76011-907">Fixed bug 'Get-AzAks' doesn't get all clusters [#12296]</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="76011-908">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="76011-908">Az.AnalysisServices</span></span>
* <span data-ttu-id="76011-909">인증에 대한 프로젝트 참조 제거</span><span class="sxs-lookup"><span data-stu-id="76011-909">Removed project reference to Authentication</span></span>

#### <a name="azautomation"></a><span data-ttu-id="76011-910">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="76011-910">Az.Automation</span></span>
* <span data-ttu-id="76011-911">이스케이프 문자를 포함하는 문자열을 json 개체로 변환할 수 없는 문제 해결</span><span class="sxs-lookup"><span data-stu-id="76011-911">Fixed the issue that string with escape chars cannot be converted into json object.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="76011-912">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="76011-912">Az.Compute</span></span>
* <span data-ttu-id="76011-913">'latest' 이미지 버전이 없는 'New-AzVmss'를 사용하는 경우 경고 추가</span><span class="sxs-lookup"><span data-stu-id="76011-913">Added warning when using 'New-AzVmss' without 'latest' image version</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="76011-914">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="76011-914">Az.DataFactory</span></span>
* <span data-ttu-id="76011-915">Data Factory에 대한 전역 매개 변수를 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-915">Added global parameters to Data Factory.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="76011-916">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="76011-916">Az.EventGrid</span></span>
* <span data-ttu-id="76011-917">2020-06-01 API 버전을 사용하도록 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-917">Updated to use the 2020-06-01 API version.</span></span>
* <span data-ttu-id="76011-918">추가된 새로운 기능:</span><span class="sxs-lookup"><span data-stu-id="76011-918">Added new features:</span></span>
    - <span data-ttu-id="76011-919">입력 매핑</span><span class="sxs-lookup"><span data-stu-id="76011-919">Input mapping</span></span>
    - <span data-ttu-id="76011-920">이벤트 배달 스키마</span><span class="sxs-lookup"><span data-stu-id="76011-920">Event Delivery Schema</span></span>
    - <span data-ttu-id="76011-921">Private Link</span><span class="sxs-lookup"><span data-stu-id="76011-921">Private Link</span></span>
    - <span data-ttu-id="76011-922">클라우드 이벤트 V10 스키마</span><span class="sxs-lookup"><span data-stu-id="76011-922">Cloud Event V10 Schema</span></span>
    - <span data-ttu-id="76011-923">대상으로 Service Bus 항목</span><span class="sxs-lookup"><span data-stu-id="76011-923">Service Bus Topic As Destination</span></span>
    - <span data-ttu-id="76011-924">대상으로 Azure 함수</span><span class="sxs-lookup"><span data-stu-id="76011-924">Azure Function As Destination</span></span>
    - <span data-ttu-id="76011-925">WebHook 일괄 처리</span><span class="sxs-lookup"><span data-stu-id="76011-925">WebHook Batching</span></span>
    - <span data-ttu-id="76011-926">보안 웹후크(AAD 지원)</span><span class="sxs-lookup"><span data-stu-id="76011-926">Secure webhook (AAD support)</span></span>
    - <span data-ttu-id="76011-927">IpFiltering</span><span class="sxs-lookup"><span data-stu-id="76011-927">IpFiltering</span></span>
* <span data-ttu-id="76011-928">다음 Cmdlet이 업데이트 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-928">Updated cmdlets:</span></span>
    - <span data-ttu-id="76011-929">'New-AzEventGridSubscription'/'Update-AzEventGridSubscription':</span><span class="sxs-lookup"><span data-stu-id="76011-929">'New-AzEventGridSubscription'/'Update-AzEventGridSubscription':</span></span>
        - <span data-ttu-id="76011-930">웹후크 일괄 처리를 지원하기 위해 새로운 선택적 매개 변수를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="76011-930">Add new optional parameters to support webhook batching.</span></span>
        - <span data-ttu-id="76011-931">AAD를 사용하여 보안 웹후크를 지원하는 새로운 선택적 매개 변수를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="76011-931">Add new optional parameters to support secured webhook using AAD.</span></span>
        - <span data-ttu-id="76011-932">Azure 함수 및 Service Bus 항목을 새 대상으로 지원하기 위해 EndpointType 매개 변수에 대한 새 열거형을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="76011-932">Add new enum for EndpointType parameter to support azure function and service bus topic as new destinations.</span></span>
        - <span data-ttu-id="76011-933">배달 스키마에 대한 새로운 선택적 매개 변수를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="76011-933">Add new optional parameter for delivery schema.</span></span>
    - <span data-ttu-id="76011-934">'New-AzEventGridTopic'/'Update-AzEventGridTopic' 및 'New-AzEventGridDomain'/'Update-AzEventGridDomain':</span><span class="sxs-lookup"><span data-stu-id="76011-934">'New-AzEventGridTopic'/'Update-AzEventGridTopic' and 'New-AzEventGridDomain'/'Update-AzEventGridDomain':</span></span>
        - <span data-ttu-id="76011-935">IpFiltering을 지원하기 위해 새로운 선택적 매개 변수를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="76011-935">Add new optional parameters to support IpFiltering.</span></span>
    - <span data-ttu-id="76011-936">'New-AzEventGridTopic'/'New-AzEventGridDomain':</span><span class="sxs-lookup"><span data-stu-id="76011-936">'New-AzEventGridTopic'/'New-AzEventGridDomain':</span></span>
        - <span data-ttu-id="76011-937">입력 매핑을 지원하기 위해 새로운 선택적 매개 변수를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="76011-937">Add new optional parameters to support Input mapping.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="76011-938">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="76011-938">Az.FrontDoor</span></span>
* <span data-ttu-id="76011-939">API 2020-05-01을 사용하도록 업데이트된 모듈</span><span class="sxs-lookup"><span data-stu-id="76011-939">Updated module to use API 2020-05-01</span></span>
* <span data-ttu-id="76011-940">Storage, Keyvault 및 Web App Service 리소스에 대한 프라이빗 링크 지원을 추가함</span><span class="sxs-lookup"><span data-stu-id="76011-940">Added Private link support for Storage, Keyvault and Web App Service resources</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="76011-941">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="76011-941">Az.HDInsight</span></span>
* <span data-ttu-id="76011-942">국가 클라우드에서 ADLSGen1/2 스토리지로 클러스터를 만드는 것이 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="76011-942">Supported creating cluster with ADLSGen1/2 storage in national clouds.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="76011-943">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="76011-943">Az.Monitor</span></span>
* <span data-ttu-id="76011-944">메트릭 또는 로그가 null인 경우 'Get-AzDiagnosticSetting'에 대한 버그 수정 [#12272]</span><span class="sxs-lookup"><span data-stu-id="76011-944">Fixed bug for 'Get-AzDiagnosticSetting' when metrics or logs are null [#12272]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="76011-945">Az.Network</span><span class="sxs-lookup"><span data-stu-id="76011-945">Az.Network</span></span>
* <span data-ttu-id="76011-946">VWan HubVnet 연결의 매개 변수 교환 수정</span><span class="sxs-lookup"><span data-stu-id="76011-946">Fixed parameters swap in VWan HubVnet connection</span></span>
* <span data-ttu-id="76011-947">Azure Network Virtual Appliance 사이트에 대한 새 cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="76011-947">Added new cmdlets for Azure Network Virtual Appliance Sites</span></span>
    - <span data-ttu-id="76011-948">'Get-AzVirtualApplianceSite'</span><span class="sxs-lookup"><span data-stu-id="76011-948">'Get-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="76011-949">'New-AzVirtualApplianceSite'</span><span class="sxs-lookup"><span data-stu-id="76011-949">'New-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="76011-950">'Remove-AzVirtualApplianceSite'</span><span class="sxs-lookup"><span data-stu-id="76011-950">'Remove-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="76011-951">'Update-AzVirtualApplianceSite'</span><span class="sxs-lookup"><span data-stu-id="76011-951">'Update-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="76011-952">'New-AzOffice365PolicyProperty'</span><span class="sxs-lookup"><span data-stu-id="76011-952">'New-AzOffice365PolicyProperty'</span></span>
* <span data-ttu-id="76011-953">Azure Network Virtual Appliance에 대한 새 cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="76011-953">Added new cmdlets for Azure Network Virtual Appliance</span></span>
    - <span data-ttu-id="76011-954">'Get-AzNetworkVirtualAppliance'</span><span class="sxs-lookup"><span data-stu-id="76011-954">'Get-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="76011-955">'New-AzNetworkVirtualAppliance'</span><span class="sxs-lookup"><span data-stu-id="76011-955">'New-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="76011-956">'Remove-AzNetworkVirtualAppliance'</span><span class="sxs-lookup"><span data-stu-id="76011-956">'Remove-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="76011-957">'Update-AzNetworkVirtualAppliance'</span><span class="sxs-lookup"><span data-stu-id="76011-957">'Update-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="76011-958">'Get-AzNetworkVirtualApplianceSku'</span><span class="sxs-lookup"><span data-stu-id="76011-958">'Get-AzNetworkVirtualApplianceSku'</span></span>
    - <span data-ttu-id="76011-959">'New-AzVirtualApplianceSkuProperty'</span><span class="sxs-lookup"><span data-stu-id="76011-959">'New-AzVirtualApplianceSkuProperty'</span></span>
* <span data-ttu-id="76011-960">Application Gateway를 Private Link 공통 cmdlet에 온보딩</span><span class="sxs-lookup"><span data-stu-id="76011-960">Onboarded Application Gateway to Private Link Common Cmdlets</span></span>
* <span data-ttu-id="76011-961">StorageSync를 Private Link 공통 cmdlet에 온보딩</span><span class="sxs-lookup"><span data-stu-id="76011-961">Onboarded StorageSync to Private Link Common Cmdlets</span></span>
* <span data-ttu-id="76011-962">SignalR을 Private Link 공통 cmdlet에 온보딩</span><span class="sxs-lookup"><span data-stu-id="76011-962">Onboarded SignalR to Private Link Common Cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="76011-963">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="76011-963">Az.RecoveryServices</span></span>
* <span data-ttu-id="76011-964">인증에 대한 프로젝트 참조 제거</span><span class="sxs-lookup"><span data-stu-id="76011-964">Removed project reference to Authentication</span></span>
* <span data-ttu-id="76011-965">Azure Backup 튜닝 cmdlet은 텍스트를 보다 정확하게 작성하는 데 도움이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="76011-965">Azure Backup tuned cmdlets help text to be more accurate.</span></span>
* <span data-ttu-id="76011-966">Azure Backup은 'Get-AzRecoveryServicesBackupJob' cmdlet을 사용하여 MAB 에이전트 작업을 가져오는 지원을 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-966">Azure Backup added support for fetching MAB agent jobs using 'Get-AzRecoveryServicesBackupJob' cmdlet.</span></span>

#### <a name="azresources"></a><span data-ttu-id="76011-967">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="76011-967">Az.Resources</span></span>
* <span data-ttu-id="76011-968">SDK를 사용하도록 'Save-AzResourceGroupDeploymentTemplate'을 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-968">Updated 'Save-AzResourceGroupDeploymentTemplate' to use the SDK.</span></span>
* <span data-ttu-id="76011-969">'Unregister-AzResourceProvider' cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-969">Added 'Unregister-AzResourceProvider' cmdlet.</span></span>

#### <a name="azsql"></a><span data-ttu-id="76011-970">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="76011-970">Az.Sql</span></span>
* <span data-ttu-id="76011-971">Set-AzSqlInstanceActiveDirectoryAdministrator cmdlet에서 서비스 주체 및 게스트 사용자에 대한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-971">Added support for Service principal and guest users in Set-AzSqlInstanceActiveDirectoryAdministrator cmdlet'</span></span>
* <span data-ttu-id="76011-972">데이터 분류 cmdlet의 버그를 수정했습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-972">Fixed a bug in Data Classification cmdlets.'</span></span>
* <span data-ttu-id="76011-973">다음의 Azure SQL Managed Instance 장애 조치에 대한 지원 추가: 'Invoke-AzSqlInstanceFailover'</span><span class="sxs-lookup"><span data-stu-id="76011-973">Added support for Azure SQL Managed Instance failover: 'Invoke-AzSqlInstanceFailover'</span></span>

#### <a name="azstorage"></a><span data-ttu-id="76011-974">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="76011-974">Az.Storage</span></span>
* <span data-ttu-id="76011-975">일부 데이터 평면 cmdlet에 대해 UserAgent가 추가되지 않는 문제를 해결했습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-975">Fixed the issue that UserAgent is not added for some data plane cmdlets.</span></span>
* <span data-ttu-id="76011-976">MinimumTlsVersion 및 AllowBlobPublicAccess로 스토리지 계정 만들기/업데이트 지원</span><span class="sxs-lookup"><span data-stu-id="76011-976">Supported create/update Storage account with MinimumTlsVersion and AllowBlobPublicAccess</span></span>
    -  <span data-ttu-id="76011-977">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="76011-977">'New-AzStorageAccount'</span></span>
    -  <span data-ttu-id="76011-978">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="76011-978">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="76011-979">스토리지 계정의 Blob Service에서 버전 관리 사용/사용 안 함 지원</span><span class="sxs-lookup"><span data-stu-id="76011-979">Support enable/disable versioning on Blob Service of a Storage account</span></span>
    - <span data-ttu-id="76011-980">'Update-AzStorageBlobServiceProperty'</span><span class="sxs-lookup"><span data-stu-id="76011-980">'Update-AzStorageBlobServiceProperty'</span></span>
* <span data-ttu-id="76011-981">Blob 버전 관리로 Blob 나열 지원</span><span class="sxs-lookup"><span data-stu-id="76011-981">Support list blobs with blob versions</span></span>
    - <span data-ttu-id="76011-982">'Get-AzStorageBlob'</span><span class="sxs-lookup"><span data-stu-id="76011-982">'Get-AzStorageBlob'</span></span>
* <span data-ttu-id="76011-983">단일 Blob 스냅샷 또는 Blob 버전 가져오기/제거 지원</span><span class="sxs-lookup"><span data-stu-id="76011-983">Support get/remove single blob snapshot or blob version</span></span>
    - <span data-ttu-id="76011-984">'Get-AzStorageBlob'</span><span class="sxs-lookup"><span data-stu-id="76011-984">'Get-AzStorageBlob'</span></span>
    - <span data-ttu-id="76011-985">'Remove-AzStorageBlob'</span><span class="sxs-lookup"><span data-stu-id="76011-985">'Remove-AzStorageBlob'</span></span>
* <span data-ttu-id="76011-986">Azure.Storage.Blobs V12에서 생성된 Blob 개체의 파이프라인 지원</span><span class="sxs-lookup"><span data-stu-id="76011-986">Support pipeline from blob object generated from Azure.Storage.Blobs V12</span></span>
    - <span data-ttu-id="76011-987">'Get-AzStorageBlobContent'</span><span class="sxs-lookup"><span data-stu-id="76011-987">'Get-AzStorageBlobContent'</span></span>
    - <span data-ttu-id="76011-988">'New-AzStorageBlobSASToken'</span><span class="sxs-lookup"><span data-stu-id="76011-988">'New-AzStorageBlobSASToken'</span></span>
    - <span data-ttu-id="76011-989">'Remove-AzStorageBlob'</span><span class="sxs-lookup"><span data-stu-id="76011-989">'Remove-AzStorageBlob'</span></span>
    - <span data-ttu-id="76011-990">'Set-AzStorageBlobContent'</span><span class="sxs-lookup"><span data-stu-id="76011-990">'Set-AzStorageBlobContent'</span></span>
    - <span data-ttu-id="76011-991">'Start-AzStorageBlobCopy'</span><span class="sxs-lookup"><span data-stu-id="76011-991">'Start-AzStorageBlobCopy'</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="76011-992">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="76011-992">Az.StorageSync</span></span>
* <span data-ttu-id="76011-993">ApiVersion 2020-03-01을 대상으로 하는 새 버전의 StorageSync SDK 추가</span><span class="sxs-lookup"><span data-stu-id="76011-993">Added a new version StorageSync SDK targeting ApiVersion 2020-03-01</span></span>
* <span data-ttu-id="76011-994">스토리지 동기화 서비스 업데이트 cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="76011-994">Added Update Storage Sync Service cmdlet</span></span>
    - <span data-ttu-id="76011-995">'Set-AzStorageSyncService'</span><span class="sxs-lookup"><span data-stu-id="76011-995">'Set-AzStorageSyncService'</span></span>
* <span data-ttu-id="76011-996">IncomingTrafficPolicy 및 PrivateEndpointConnections가 StorageSyncService cmdlet에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-996">Added IncomingTrafficPolicy and PrivateEndpointConnections to StorageSyncService cmdlets.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="76011-997">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="76011-997">Az.Websites</span></span>
* <span data-ttu-id="76011-998">App Service 계획과 동일한 리소스 그룹에 속하지 않는 슬롯에 대한 작업을 수행하기 위한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="76011-998">Added support to perform operations for Slots not in the same resource group as the App Service Plan</span></span>

## <a name="430---june-2020"></a><span data-ttu-id="76011-999">4.3.0 - 2020년 6월</span><span class="sxs-lookup"><span data-stu-id="76011-999">4.3.0 - June 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="76011-1000">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="76011-1000">Az.Accounts</span></span>
* <span data-ttu-id="76011-1001">기본적으로 환경 검색 설정이 지원되며 'Add-AzEnvironment'를 통해 환경을 추가할 수 있음</span><span class="sxs-lookup"><span data-stu-id="76011-1001">Supported discovering environment setting by default and adding environment via 'Add-AzEnvironment'</span></span>
* <span data-ttu-id="76011-1002">미리 로드된 어셈블리 업데이트 [#12024], [#11976]</span><span class="sxs-lookup"><span data-stu-id="76011-1002">Update preloaded assemblies [#12024], [#11976]</span></span>
* <span data-ttu-id="76011-1003">Azure.Core 어셈블리 업데이트</span><span class="sxs-lookup"><span data-stu-id="76011-1003">Updated Azure.Core assembly</span></span>
* <span data-ttu-id="76011-1004">다중 스레드 실행에서 'Connect-AzAccount'가 실패할 수 있는 문제 해결 [#11201]</span><span class="sxs-lookup"><span data-stu-id="76011-1004">Fixed an issue that may cause 'Connect-AzAccount' to fail in multi-threaded execution [#11201]</span></span>

#### <a name="azaks"></a><span data-ttu-id="76011-1005">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="76011-1005">Az.Aks</span></span>
* <span data-ttu-id="76011-1006">이전에 사용하던 [AccessProfile API](/rest/api/aks/managedclusters/getaccessprofile)를 [ListClusterAdmin](/rest/api/aks/managedclusters/listclusteradmincredentials) 및 [ListClusterUser](/rest/api/aks/managedclusters/listclusterusercredentials) API 호출로 대체</span><span class="sxs-lookup"><span data-stu-id="76011-1006">Replaced usage of old [AccessProfile API](/rest/api/aks/managedclusters/getaccessprofile) with calls to [ListClusterAdmin](/rest/api/aks/managedclusters/listclusteradmincredentials) and [ListClusterUser](/rest/api/aks/managedclusters/listclusterusercredentials) APIs</span></span>

#### <a name="azbatch"></a><span data-ttu-id="76011-1007">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="76011-1007">Az.Batch</span></span>
* <span data-ttu-id="76011-1008">'Microsoft.Azure.Management.Batch' SDK 버전 11.0.0을 사용하도록 Az.Batch 업데이트</span><span class="sxs-lookup"><span data-stu-id="76011-1008">Updated Az.Batch to use 'Microsoft.Azure.Management.Batch' SDK version to 11.0.0</span></span>
* <span data-ttu-id="76011-1009">'New-AzBatchAccount' cmdlet에서 BatchAccount ID를 설정하는 기능 추가</span><span class="sxs-lookup"><span data-stu-id="76011-1009">Added the ability to set the BatchAccount Identity in the 'New-AzBatchAccount' cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="76011-1010">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="76011-1010">Az.CognitiveServices</span></span>
* <span data-ttu-id="76011-1011">계정 기능 표시 지원</span><span class="sxs-lookup"><span data-stu-id="76011-1011">Supported displaying account capabilities.</span></span>
* <span data-ttu-id="76011-1012">PublicNetworkAccess 수정 지원</span><span class="sxs-lookup"><span data-stu-id="76011-1012">Supported modifying PublicNetworkAccess.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="76011-1013">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="76011-1013">Az.Compute</span></span>
* <span data-ttu-id="76011-1014">Set-AzVM 및 Set-AzVmssVM cmdlet에 SimulateEviction 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="76011-1014">Added SimulateEviction parameter to Set-AzVM and Set-AzVmssVM cmdlets.</span></span>
* <span data-ttu-id="76011-1015">AzGalleryImageVersion cmdlet에 대한 StorageAccountType 매개 변수의 인수 완성자에 'Premium_LRS' 추가</span><span class="sxs-lookup"><span data-stu-id="76011-1015">Added 'Premium_LRS' to the argument completer of StorageAccountType parameter for New-AzGalleryImageVersion cmdlet.</span></span>
* <span data-ttu-id="76011-1016">VMCustomScriptExtension에 Substatuses 추가 [#11297]</span><span class="sxs-lookup"><span data-stu-id="76011-1016">Added Substatuses to VMCustomScriptExtension [#11297]</span></span>
* <span data-ttu-id="76011-1017">New-AzVM 및 New-AzVMConfig cmdlet에 대한 EvictionPolicy 매개 변수의 인수 완성자에 'Delete' 추가</span><span class="sxs-lookup"><span data-stu-id="76011-1017">Added 'Delete' to the argument completer of EvictionPolicy parameter for New-AzVM and New-AzVMConfig cmdlets.</span></span>
* <span data-ttu-id="76011-1018">새 SAP용 VM 확장의 이름 수정</span><span class="sxs-lookup"><span data-stu-id="76011-1018">Fixed name of new VM Extension for SAP</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="76011-1019">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="76011-1019">Az.DataFactory</span></span>
* <span data-ttu-id="76011-1020">ADF .Net SDK 버전을 4.9.0으로 업데이트</span><span class="sxs-lookup"><span data-stu-id="76011-1020">Updated ADF .Net SDK version to 4.9.0</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="76011-1021">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="76011-1021">Az.EventHub</span></span>
* <span data-ttu-id="76011-1022">'New-AzEventHubNamespace' 및 'Set-AzEventHubNamespace' cmdlet에 관리 ID 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="76011-1022">Added Managed Identity parameters to 'New-AzEventHubNamespace' and 'Set-AzEventHubNamespace' cmdlets</span></span>

#### <a name="azfunctions"></a><span data-ttu-id="76011-1023">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="76011-1023">Az.Functions</span></span>
* <span data-ttu-id="76011-1024">PowerShell 7.0 및 Java 11 함수 앱을 만드는 지원 추가</span><span class="sxs-lookup"><span data-stu-id="76011-1024">Added support to create PowerShell 7.0 and Java 11 function apps</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="76011-1025">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="76011-1025">Az.HDInsight</span></span>
* <span data-ttu-id="76011-1026">호스트를 나열하고 HDInsight 클러스터의 특정 호스트를 다시 시작하는 기능 지원</span><span class="sxs-lookup"><span data-stu-id="76011-1026">Supported listing hosts and restart specific hosts of the HDInsight cluster.</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="76011-1027">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="76011-1027">Az.HealthcareApis</span></span>
* <span data-ttu-id="76011-1028">SDK 버전을 1.1.0으로 업데이트</span><span class="sxs-lookup"><span data-stu-id="76011-1028">Updated the SDK version to 1.1.0</span></span>
* <span data-ttu-id="76011-1029">설정 및 관리 ID 내보내기에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="76011-1029">Added support for Export settings and Managed Identity</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="76011-1030">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="76011-1030">Az.Monitor</span></span>
* <span data-ttu-id="76011-1031">'Set-AzActivityLogAlert'에 대한 입력 개체 매개 변수 수정</span><span class="sxs-lookup"><span data-stu-id="76011-1031">Fixed input object parameter for 'Set-AzActivityLogAlert'</span></span>
* <span data-ttu-id="76011-1032">'Set-AzActionGroup'에 대한 'InputObject' 매개 변수 수정 [#10868]</span><span class="sxs-lookup"><span data-stu-id="76011-1032">Fixed 'InputObject' parameter for 'Set-AzActionGroup' [#10868]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="76011-1033">Az.Network</span><span class="sxs-lookup"><span data-stu-id="76011-1033">Az.Network</span></span>
* <span data-ttu-id="76011-1034">'Remove-AzExpressRouteCircuitConnectionConfig'에 AddressPrefixType 매개 변수 지원 추가</span><span class="sxs-lookup"><span data-stu-id="76011-1034">Added support for AddressPrefixType parameter to 'Remove-AzExpressRouteCircuitConnectionConfig'</span></span>
* <span data-ttu-id="76011-1035">Azure FirewallPolicy에 대한 새 cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="76011-1035">Added new cmdlets for Azure FirewallPolicy</span></span>
    - <span data-ttu-id="76011-1036">'New-AzFirewallPolicyDnsSetting'</span><span class="sxs-lookup"><span data-stu-id="76011-1036">'New-AzFirewallPolicyDnsSetting'</span></span>
    - <span data-ttu-id="76011-1037">방화벽 정책에 대한 네트워크 규칙에서 대상 FQDN 지원</span><span class="sxs-lookup"><span data-stu-id="76011-1037">Support for Destination FQDN in Network Rules for Firewall Policy</span></span>
* <span data-ttu-id="76011-1038">백 엔드 주소 풀 작업에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="76011-1038">Added support for backend address pool operations</span></span>
    - <span data-ttu-id="76011-1039">'New-AzLoadBalancerBackendAddressConfig'</span><span class="sxs-lookup"><span data-stu-id="76011-1039">'New-AzLoadBalancerBackendAddressConfig'</span></span>
    - <span data-ttu-id="76011-1040">'New-AzLoadBalancerBackendAddressPool'</span><span class="sxs-lookup"><span data-stu-id="76011-1040">'New-AzLoadBalancerBackendAddressPool'</span></span>
    - <span data-ttu-id="76011-1041">'Set-AzLoadBalancerBackendAddressPool'</span><span class="sxs-lookup"><span data-stu-id="76011-1041">'Set-AzLoadBalancerBackendAddressPool'</span></span>
    - <span data-ttu-id="76011-1042">'Remove-AzLoadBalancerBackendAddressPool'</span><span class="sxs-lookup"><span data-stu-id="76011-1042">'Remove-AzLoadBalancerBackendAddressPool'</span></span>
    - <span data-ttu-id="76011-1043">'Get-AzLoadBalancerBackendAddressPool'</span><span class="sxs-lookup"><span data-stu-id="76011-1043">'Get-AzLoadBalancerBackendAddressPool'</span></span>
* <span data-ttu-id="76011-1044">'New-AzIpGroup'에 대한 이름 유효성 검사 추가</span><span class="sxs-lookup"><span data-stu-id="76011-1044">Added name validation for 'New-AzIpGroup'</span></span>
* <span data-ttu-id="76011-1045">Azure FirewallPolicy에 대한 새 cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="76011-1045">Added new cmdlets for Azure FirewallPolicy</span></span>
    - <span data-ttu-id="76011-1046">'New-AzFirewallPolicyThreatIntelWhitelist'</span><span class="sxs-lookup"><span data-stu-id="76011-1046">'New-AzFirewallPolicyThreatIntelWhitelist'</span></span>
* <span data-ttu-id="76011-1047">기능에 대한 새로운 명령이 업데이트됨: VirtualWan P2SVpnGateway에서 사용자 지정 dns 서버 설정/제거</span><span class="sxs-lookup"><span data-stu-id="76011-1047">Updated below commands for feature: Custom dns servers set/remove on VirtualWan P2SVpnGateway.</span></span>
    - <span data-ttu-id="76011-1048">New-AzP2sVpnGateway 업데이트됨: 고객이 P2SVpnGateway에 설정할 dns 서버를 지정할 수 있는 선택적 매개 변수 '-CustomDnsServer'가 추가되었으며, 이 매개 변수는 지점 및 사이트 간 클라이언트에서 사용 가능</span><span class="sxs-lookup"><span data-stu-id="76011-1048">Updated New-AzP2sVpnGateway: Added optional parameter '-CustomDnsServer' for customers to specify their dns servers to set on P2SVpnGateway, which can be used by Point to site clients.</span></span>
    - <span data-ttu-id="76011-1049">Update-AzP2sVpnGateway 업데이트됨: 고객이 P2SVpnGateway에 설정할 dns 서버를 지정할 수 있는 선택적 매개 변수 '-CustomDnsServer'가 추가되었으며, 이 매개 변수는 지점 및 사이트 간 클라이언트에서 사용 가능</span><span class="sxs-lookup"><span data-stu-id="76011-1049">Updated Update-AzP2sVpnGateway: Added optional parameter '-CustomDnsServer' for customers to specify their dns servers to set on P2SVpnGateway, which can be used by Point to site clients.</span></span>
* <span data-ttu-id="76011-1050">'Update-AzVpnGateway' 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="76011-1050">Updated 'Update-AzVpnGateway'</span></span>
    - <span data-ttu-id="76011-1051">고객이 VpnGateway에 설정할 사용자 지정 bgps를 지정할 수 있도록 선택적 매개 변수 '-BgpPeeringAddress' 추가</span><span class="sxs-lookup"><span data-stu-id="76011-1051">Added optional parameter '-BgpPeeringAddress' for customers to specify their custom bgps to set on VpnGateway.</span></span>
* <span data-ttu-id="76011-1052">VirtualHub 리소스의 라우팅 상태 초기화를 지원하는 새 cmdlet 추가:</span><span class="sxs-lookup"><span data-stu-id="76011-1052">Added new cmdlet to support resetting the routing state of a VirtualHub resource:</span></span>
    - <span data-ttu-id="76011-1053">'Reset-AzHubRouter'</span><span class="sxs-lookup"><span data-stu-id="76011-1053">'Reset-AzHubRouter'</span></span>
* <span data-ttu-id="76011-1054">방화벽 정책에 대한 최근 Swagger 변화에 따라 아래 항목 업데이트</span><span class="sxs-lookup"><span data-stu-id="76011-1054">Updated below things based on recent swagger change for Firewall Policy</span></span>
    - <span data-ttu-id="76011-1055">RuleGroup, RuleCollectionGroup 및 RuleType의 이름 변경</span><span class="sxs-lookup"><span data-stu-id="76011-1055">Changes names for RuleGroup, RuleCollectionGroup and RuleType</span></span>
    - <span data-ttu-id="76011-1056">여러 NAT 규칙 컬렉션을 지원하도록 방화벽 정책 NAT 규칙 컬렉션에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="76011-1056">Added support for Firewall Policy NAT Rule Collections to support multiple NAT Rule Collection</span></span>
* <span data-ttu-id="76011-1057">[호환성이 손상되는 변경] 'New-AzFirewallPolicyApplicationRule' 및 'New-AzFirewallPolicyNetworkRule'에 대한 필수 매개 변수 'SourceIpGroup' 추가</span><span class="sxs-lookup"><span data-stu-id="76011-1057">[Breaking Change] Added mandatory parameter 'SourceIpGroup' for 'New-AzFirewallPolicyApplicationRule' and 'New-AzFirewallPolicyNetworkRule'.</span></span>
* <span data-ttu-id="76011-1058">[호환성이 손상되는 변경] 'New-AzFirewallPolicyApplicationRule' 수정, 'SourceAddress' 매개 변수를 필수로 변경</span><span class="sxs-lookup"><span data-stu-id="76011-1058">[Breaking Change] Fixed 'New-AzFirewallPolicyApplicationRule', parameter 'SourceAddress' to be mandatory.</span></span>
* <span data-ttu-id="76011-1059">[호환성이 손상되는 변경] 'New-AzFirewallPolicyApplicationRule' 수정, 'SourceAddress' 매개 변수를 필수로 변경</span><span class="sxs-lookup"><span data-stu-id="76011-1059">[Breaking Change] Fixed 'New-AzFirewallPolicyApplicationRule', parameter 'SourceAddress' to be mandatory.</span></span>
* <span data-ttu-id="76011-1060">[호환성이 손상되는 변경] 다음 필수 매개 변수 제거: 'New-AzFirewallPolicyNatRuleCollection'의 'TranslatedAddress', 'TranslatedPort'</span><span class="sxs-lookup"><span data-stu-id="76011-1060">[Breaking Change] Removed mandatory parameters: 'TranslatedAddress', 'TranslatedPort' for 'New-AzFirewallPolicyNatRuleCollection'.</span></span>
* <span data-ttu-id="76011-1061">PrivateLink On Application Gateway를 지원하는 새 cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="76011-1061">Added new cmdlets to support PrivateLink On Application Gateway</span></span>
    - <span data-ttu-id="76011-1062">'New-AzApplicationGatewayPrivateLinkConfiguration'</span><span class="sxs-lookup"><span data-stu-id="76011-1062">'New-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="76011-1063">'Get-AzApplicationGatewayPrivateLinkConfiguration'</span><span class="sxs-lookup"><span data-stu-id="76011-1063">'Get-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="76011-1064">'New-AzApplicationGatewayPrivateLinkConfiguration'</span><span class="sxs-lookup"><span data-stu-id="76011-1064">'New-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="76011-1065">'Set-AzApplicationGatewayPrivateLinkConfiguration'</span><span class="sxs-lookup"><span data-stu-id="76011-1065">'Set-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="76011-1066">'Remove-AzApplicationGatewayPrivateLinkConfiguration'</span><span class="sxs-lookup"><span data-stu-id="76011-1066">'Remove-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="76011-1067">'New-AzApplicationGatewayPrivateLinkIpConfiguration'</span><span class="sxs-lookup"><span data-stu-id="76011-1067">'New-AzApplicationGatewayPrivateLinkIpConfiguration'</span></span>
* <span data-ttu-id="76011-1068">VirtualHub의 HubRouteTables 자식 리소스에 대한 새 cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="76011-1068">Added new cmdlets for HubRouteTables child resource of VirtualHub.</span></span>
    - <span data-ttu-id="76011-1069">'New-AzVHubRoute'</span><span class="sxs-lookup"><span data-stu-id="76011-1069">'New-AzVHubRoute'</span></span>
    - <span data-ttu-id="76011-1070">'New-AzVHubRouteTable'</span><span class="sxs-lookup"><span data-stu-id="76011-1070">'New-AzVHubRouteTable'</span></span>
    - <span data-ttu-id="76011-1071">'Get-AzVHubRouteTable'</span><span class="sxs-lookup"><span data-stu-id="76011-1071">'Get-AzVHubRouteTable'</span></span>
    - <span data-ttu-id="76011-1072">'Update-AzVHubRouteTable'</span><span class="sxs-lookup"><span data-stu-id="76011-1072">'Update-AzVHubRouteTable'</span></span>
    - <span data-ttu-id="76011-1073">'Remove-AzVHubRouteTable'</span><span class="sxs-lookup"><span data-stu-id="76011-1073">'Remove-AzVHubRouteTable'</span></span>
* <span data-ttu-id="76011-1074">VirtualWan의 사용자 지정 라우팅에 대한 선택적 RoutingConfiguration 입력 매개 변수를 지원하도록 기존 cmdlet 업데이트</span><span class="sxs-lookup"><span data-stu-id="76011-1074">Updated existing cmdlets to support optional RoutingConfiguration input parameter for custom routing in VirtualWan.</span></span>
    - <span data-ttu-id="76011-1075">'New-AzExpressRouteConnection'</span><span class="sxs-lookup"><span data-stu-id="76011-1075">'New-AzExpressRouteConnection'</span></span>
    - <span data-ttu-id="76011-1076">'Set-AzExpressRouteConnection'</span><span class="sxs-lookup"><span data-stu-id="76011-1076">'Set-AzExpressRouteConnection'</span></span>
    - <span data-ttu-id="76011-1077">'New-AzVirtualHubVnetConnection'</span><span class="sxs-lookup"><span data-stu-id="76011-1077">'New-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="76011-1078">'Update-AzVirtualHubVnetConnection'</span><span class="sxs-lookup"><span data-stu-id="76011-1078">'Update-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="76011-1079">'New-AzVpnConnection'</span><span class="sxs-lookup"><span data-stu-id="76011-1079">'New-AzVpnConnection'</span></span>
    - <span data-ttu-id="76011-1080">'Update-AzVpnConnection'</span><span class="sxs-lookup"><span data-stu-id="76011-1080">'Update-AzVpnConnection'</span></span>
    - <span data-ttu-id="76011-1081">'New-AzP2sVpnGateway'</span><span class="sxs-lookup"><span data-stu-id="76011-1081">'New-AzP2sVpnGateway'</span></span>
    - <span data-ttu-id="76011-1082">'Update-AzP2sVpnGateway'</span><span class="sxs-lookup"><span data-stu-id="76011-1082">'Update-AzP2sVpnGateway'</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="76011-1083">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="76011-1083">Az.OperationalInsights</span></span>
* <span data-ttu-id="76011-1084">PSWorkspace가 IOperationalInsightsWorkspace를 구현하지 않는 버그 수정 [#12135]</span><span class="sxs-lookup"><span data-stu-id="76011-1084">Fixed bug PSWorkspace doesn't implement IOperationalInsightsWorkspace [#12135]</span></span>
* <span data-ttu-id="76011-1085">'Set-AzOperationalInsightsWorkspace'에서 'Sku' 매개 변수의 올바른 값 세트에 'pergb2018' 추가</span><span class="sxs-lookup"><span data-stu-id="76011-1085">Added 'pergb2018' to valid value set of parameter 'Sku' in 'Set-AzOperationalInsightsWorkspace'</span></span> 
* <span data-ttu-id="76011-1086">매개 변수 'FunctionParameter'에 대한 별칭 'FunctionParameters' 추가</span><span class="sxs-lookup"><span data-stu-id="76011-1086">Added alias 'FunctionParameters' for parameter 'FunctionParameter' to</span></span>
    - <span data-ttu-id="76011-1087">'New-AzOperationalInsightsSavedSearch'</span><span class="sxs-lookup"><span data-stu-id="76011-1087">'New-AzOperationalInsightsSavedSearch'</span></span>
    - <span data-ttu-id="76011-1088">'Set-AzOperationalInsightsSavedSearch'</span><span class="sxs-lookup"><span data-stu-id="76011-1088">'Set-AzOperationalInsightsSavedSearch'</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="76011-1089">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="76011-1089">Az.RecoveryServices</span></span>
* <span data-ttu-id="76011-1090">Azure Backup에서 MAB 항목을 가져오기 위한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="76011-1090">Azure Backup added support for fetching MAB items.</span></span>
* <span data-ttu-id="76011-1091">Azure Site Recovery에서 'StandardSSD_LRS' 디스크 형식 지원</span><span class="sxs-lookup"><span data-stu-id="76011-1091">Azure Site Recovery supports disk type 'StandardSSD_LRS'</span></span>

#### <a name="azresources"></a><span data-ttu-id="76011-1092">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="76011-1092">Az.Resources</span></span>
* <span data-ttu-id="76011-1093">'PSADUser'에서 'UsageLocation', 'GivenName', 'Surname', 'AccountEnabled', 'MailNickname', 'Mail' 추가 [#10526] [#10497]</span><span class="sxs-lookup"><span data-stu-id="76011-1093">Added 'UsageLocation', 'GivenName', 'Surname', 'AccountEnabled', 'MailNickname', 'Mail' on 'PSADUser' [#10526] [#10497]</span></span>
* <span data-ttu-id="76011-1094">'Get-AzADUser'에서 '-Mail'이 작동하지 않는 문제 해결 [#11981]</span><span class="sxs-lookup"><span data-stu-id="76011-1094">Fixed issue that '-Mail' doesn't work on 'Get-AzADUser' [#11981]</span></span>
* <span data-ttu-id="76011-1095">'Get-AzDeploymentWhatIfResult' 및 'Get-AzResourceGroupDeploymentWhatIfResult'에 '-ExcludeChangeType' 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="76011-1095">Added '-ExcludeChangeType' parameter to 'Get-AzDeploymentWhatIfResult' and 'Get-AzResourceGroupDeploymentWhatIfResult'</span></span>
* <span data-ttu-id="76011-1096">'New-AzDeployment' 및 'New-AzResourceGroupDeployment'에 '-WhatIfExcludeChangeType' 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="76011-1096">Added '-WhatIfExcludeChangeType' parameter to 'New-AzDeployment' and 'New-AzResourceGroupDeployment'</span></span>
* <span data-ttu-id="76011-1097">보다 나은 오류 메시지를 표시하도록 'Test-Az\*Deployment' cmdlet 업데이트</span><span class="sxs-lookup"><span data-stu-id="76011-1097">Updated 'Test-Az\*Deployment' cmdlets to show better error messages</span></span>
* <span data-ttu-id="76011-1098">deployment create 및 What-If cmdlet의 '-Name' 매개 변수에 대한 도움말 메시지 수정</span><span class="sxs-lookup"><span data-stu-id="76011-1098">Fixed help message for '-Name' parameter of deployment create and What-If cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="76011-1099">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="76011-1099">Az.Sql</span></span>
* <span data-ttu-id="76011-1100">Set SQL Server Azure Active Directory Admin cmdlet의 서비스 주체에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="76011-1100">Added support for service principal for Set SQL Server Azure Active Directory Admin cmdlet</span></span>
* <span data-ttu-id="76011-1101">데이터 분류 cmdlet의 동기화 문제 해결</span><span class="sxs-lookup"><span data-stu-id="76011-1101">Fixed sync issue in Data Classification cmdlets.</span></span>
* <span data-ttu-id="76011-1102">'Set-AzSqlServerActiveDirectoryAdministrator'에서 메일로 사용자 검색 지원 [#12192]</span><span class="sxs-lookup"><span data-stu-id="76011-1102">Supported searching user by mail on 'Set-AzSqlServerActiveDirectoryAdministrator' [#12192]</span></span>

#### <a name="azstorage"></a><span data-ttu-id="76011-1103">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="76011-1103">Az.Storage</span></span>
* <span data-ttu-id="76011-1104">RequireInfrastructureEncryption을 사용하여 스토리지 계정 만들기 지원</span><span class="sxs-lookup"><span data-stu-id="76011-1104">Supported create Storage account with RequireInfrastructureEncryption</span></span>
    -  <span data-ttu-id="76011-1105">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="76011-1105">'New-AzStorageAccount'</span></span>
* <span data-ttu-id="76011-1106">Azure.Core 로딩 논리를 Az.Accounts로 이동</span><span class="sxs-lookup"><span data-stu-id="76011-1106">Moved the logic of loading Azure.Core to Az.Accounts</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="76011-1107">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="76011-1107">Az.Websites</span></span>
* <span data-ttu-id="76011-1108">'Restore-AzDeletedWebApp'에서 복원이 실패할 경우 생성된 웹앱을 삭제하는 보호 기능 추가</span><span class="sxs-lookup"><span data-stu-id="76011-1108">Added safeguard to delete created webapp if restore failed in 'Restore-AzDeletedWebApp'</span></span>
* <span data-ttu-id="76011-1109">'New-AzWebApp' 및 'New-AzWebAppSlot'에 대한 'SourceWebApp.Location' 추가</span><span class="sxs-lookup"><span data-stu-id="76011-1109">Added 'SourceWebApp.Location' for 'New-AzWebApp' and 'New-AzWebAppSlot'</span></span>
* <span data-ttu-id="76011-1110">'Set-AzWebApp' 및 'Set-AzWebAppSlot'에서 컨테이너 설정을 변경할 수 없는 버그 수정</span><span class="sxs-lookup"><span data-stu-id="76011-1110">Fixed bug that prevented changing Container settings in 'Set-AzWebApp' and 'Set-AzWebAppSlot'</span></span>
* <span data-ttu-id="76011-1111">Get-AzWebApp에 대한 -Name을 제공하지 않으면 SiteConfig를 가져오는 버그 수정</span><span class="sxs-lookup"><span data-stu-id="76011-1111">Fixed bug to get SiteConfig when -Name is not given for Get-AzWebApp</span></span>
* <span data-ttu-id="76011-1112">Linux 앱용 ASP를 만드는 지원 추가</span><span class="sxs-lookup"><span data-stu-id="76011-1112">Added a support to create ASP for Linux Apps</span></span>
* <span data-ttu-id="76011-1113">리소스 그룹 간 복제에 대한 예외 추가</span><span class="sxs-lookup"><span data-stu-id="76011-1113">Added exceptions for clone across resource groups</span></span>

## <a name="420---june-2020"></a><span data-ttu-id="76011-1114">4.2.0 - 2020년 6월</span><span class="sxs-lookup"><span data-stu-id="76011-1114">4.2.0 - June 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="76011-1115">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="76011-1115">Az.Accounts</span></span>
* <span data-ttu-id="76011-1116">Azure Automation 또는 PowerShell 작업에서 Az가 로그를 건너뛸 수 있는 문제 수정[#11492]</span><span class="sxs-lookup"><span data-stu-id="76011-1116">Fixed an issue that may cause Az to skip logs in Azure Automation or PowerShell jobs [#11492]</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="76011-1117">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="76011-1117">Az.AnalysisServices</span></span>
* <span data-ttu-id="76011-1118">데이터 평면 cmdlet의 어셈블리 버전 업데이트</span><span class="sxs-lookup"><span data-stu-id="76011-1118">Updated assembly version of data plane cmdlets</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="76011-1119">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="76011-1119">Az.ApiManagement</span></span>
* <span data-ttu-id="76011-1120">서비스 관리 cmdlet의 어셈블리 버전 업데이트</span><span class="sxs-lookup"><span data-stu-id="76011-1120">Updated assembly version of service management cmdlets</span></span>

#### <a name="azbilling"></a><span data-ttu-id="76011-1121">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="76011-1121">Az.Billing</span></span>
* <span data-ttu-id="76011-1122">소비 cmdlet의 어셈블리 버전 업데이트</span><span class="sxs-lookup"><span data-stu-id="76011-1122">Updated assembly version of consumption cmdlets</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="76011-1123">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="76011-1123">Az.CognitiveServices</span></span>
* <span data-ttu-id="76011-1124">PrivateEndpoint 및 PublicNetworkAccess control을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1124">Support PrivateEndpoint and PublicNetworkAccess control.</span></span> 

#### <a name="azdatafactory"></a><span data-ttu-id="76011-1125">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="76011-1125">Az.DataFactory</span></span>
* <span data-ttu-id="76011-1126">데이터 팩터리 V2 cmdlet의 어셈블리 버전 업데이트</span><span class="sxs-lookup"><span data-stu-id="76011-1126">Updated assembly version of data factory V2 cmdlets</span></span>

#### <a name="azdatashare"></a><span data-ttu-id="76011-1127">Az.DataShare</span><span class="sxs-lookup"><span data-stu-id="76011-1127">Az.DataShare</span></span>
* <span data-ttu-id="76011-1128">''Az.DataShare'' 모듈의 일반 공급</span><span class="sxs-lookup"><span data-stu-id="76011-1128">General availability of ''Az.DataShare'' module</span></span>

#### <a name="azdesktopvirtualization"></a><span data-ttu-id="76011-1129">Az.DesktopVirtualization</span><span class="sxs-lookup"><span data-stu-id="76011-1129">Az.DesktopVirtualization</span></span>
* <span data-ttu-id="76011-1130">''Az.DesktopVirtualization'' 모듈의 일반 공급</span><span class="sxs-lookup"><span data-stu-id="76011-1130">General availability of ''Az.DesktopVirtualization'' module</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="76011-1131">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="76011-1131">Az.OperationalInsights</span></span>
* <span data-ttu-id="76011-1132">SDK를 0.21.0으로 업그레이드</span><span class="sxs-lookup"><span data-stu-id="76011-1132">Upgraded SDK to 0.21.0</span></span>
* <span data-ttu-id="76011-1133">다음에 선택적 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="76011-1133">Added optional parameters to</span></span> 
    - <span data-ttu-id="76011-1134">'New-AzOperationalInsightsSavedSearch'</span><span class="sxs-lookup"><span data-stu-id="76011-1134">'New-AzOperationalInsightsSavedSearch'</span></span>
    - <span data-ttu-id="76011-1135">'Set-AzOperationalInsightsSavedSearch'</span><span class="sxs-lookup"><span data-stu-id="76011-1135">'Set-AzOperationalInsightsSavedSearch'</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="76011-1136">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="76011-1136">Az.PolicyInsights</span></span>
* <span data-ttu-id="76011-1137">'Start-AzPolicyComplianceScan'의 예제 3 수정</span><span class="sxs-lookup"><span data-stu-id="76011-1137">Corrected example 3 for 'Start-AzPolicyComplianceScan'</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="76011-1138">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="76011-1138">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="76011-1139">PowerBI cmdlet의 어셈블리 버전 업데이트</span><span class="sxs-lookup"><span data-stu-id="76011-1139">Updated assembly version of PowerBI cmdlets</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="76011-1140">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="76011-1140">Az.PrivateDns</span></span>
* <span data-ttu-id="76011-1141">Remove-AzPrivateDnsRecordSet에 대한 자세한 정보 출력 문자열 형식 수정</span><span class="sxs-lookup"><span data-stu-id="76011-1141">Corrected verbose output string formatting for Remove-AzPrivateDnsRecordSet</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="76011-1142">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="76011-1142">Az.RecoveryServices</span></span>
* <span data-ttu-id="76011-1143">xml 입력에서 영역 간 복제를 위한 복구 계획을 세우기 위한 Azure Site Recovery 지원.</span><span class="sxs-lookup"><span data-stu-id="76011-1143">Azure Site Recovery support for creating recovery plan for zone to zone replication from xml input.</span></span>
* <span data-ttu-id="76011-1144">SiteRecovery 및 Backup cmdlet의 어셈블리 버전 업데이트</span><span class="sxs-lookup"><span data-stu-id="76011-1144">Updated assembly version of SiteRecovery and Backup cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="76011-1145">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="76011-1145">Az.Resources</span></span>
* <span data-ttu-id="76011-1146">Get-AzDeploymentScriptLog 및 Save-AzDeploymentScriptLog cmdlet에 Tail 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="76011-1146">Added Tail parameter to Get-AzDeploymentScriptLog and Save-AzDeploymentScriptLog cmdlets</span></span>
* <span data-ttu-id="76011-1147">형식이 지정된 출력 속성을 Get-AzDeploymentScript cmdlet 출력에 표시</span><span class="sxs-lookup"><span data-stu-id="76011-1147">Formatted Output property and show it on the Get-AzDeploymentScript cmdlet output</span></span>
* <span data-ttu-id="76011-1148">-DeploymentScriptInputObject 매개 변수의 이름이 -DeploymentScriptObject로 변경</span><span class="sxs-lookup"><span data-stu-id="76011-1148">Renamed -DeploymentScriptInputObject parameter to -DeploymentScriptObject</span></span>
* <span data-ttu-id="76011-1149">cmdlet 메시지에서 누락된 파일/대상 이름이 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1149">Fixed missing file/target name in cmdlet messages.</span></span>
* <span data-ttu-id="76011-1150">리소스 관리자 및 태그 cmdlet의 어셈블리 버전 업데이트</span><span class="sxs-lookup"><span data-stu-id="76011-1150">Updated assembly version of resource manager and tags cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="76011-1151">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="76011-1151">Az.Sql</span></span>
* <span data-ttu-id="76011-1152">UsePrivateLinkConnection을 'New-AzSqlSyncGroup', 'Update-AzSqlSyncGroup', 'New-AzSqlSyncMember' 및 'Update-AzSqlSyncMember'에 추가</span><span class="sxs-lookup"><span data-stu-id="76011-1152">Added UsePrivateLinkConnection to 'New-AzSqlSyncGroup', 'Update-AzSqlSyncGroup', 'New-AzSqlSyncMember' and 'Update-AzSqlSyncMember'</span></span>
* <span data-ttu-id="76011-1153">SyncMemberAzureDatabaseResourceId를 'New-AzSqlSyncMember' 및 'Update-AzSqlSyncMember'에 추가</span><span class="sxs-lookup"><span data-stu-id="76011-1153">Added SyncMemberAzureDatabaseResourceId to 'New-AzSqlSyncMember' and 'Update-AzSqlSyncMember'</span></span>
* <span data-ttu-id="76011-1154">SQL Server Azure Active Directory Admin cmdlet을 설정하는 게스트 사용자 조회 지원 추가</span><span class="sxs-lookup"><span data-stu-id="76011-1154">Added Guest user lookup support to Set SQL Server Azure Active Directory Admin cmdlet</span></span>

#### <a name="azstorage"></a><span data-ttu-id="76011-1155">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="76011-1155">Az.Storage</span></span>
* <span data-ttu-id="76011-1156">데이터 평면 cmdlet의 어셈블리 버전 업데이트</span><span class="sxs-lookup"><span data-stu-id="76011-1156">Updated assembly version of data plane cmdlets</span></span>

## <a name="410---may-2020"></a><span data-ttu-id="76011-1157">4.1.0 - 2020년 5월</span><span class="sxs-lookup"><span data-stu-id="76011-1157">4.1.0 - May 2020</span></span>
### <a name="highlights-since-the-last-release"></a><span data-ttu-id="76011-1158">마지막 릴리스 이후의 주요 사항</span><span class="sxs-lookup"><span data-stu-id="76011-1158">Highlights since the last release</span></span>
* <span data-ttu-id="76011-1159">지원되는 PowerShell 버전: Windows PowerShell 5.1, PowerShell Core 6.2.4 이상, PowerShell 7</span><span class="sxs-lookup"><span data-stu-id="76011-1159">Supported PowerShell versions: Windows PowerShell 5.1, PowerShell Core 6.2.4+, PowerShell 7</span></span>
* <span data-ttu-id="76011-1160">Az.Functions 일반 공급</span><span class="sxs-lookup"><span data-stu-id="76011-1160">General availability of Az.Functions</span></span> 
* <span data-ttu-id="76011-1161">Az.ApiManagement, Az.Batch, Az.Compute, Az.KeyVault, Az.Monitor, Az.Network, Az.OperationalInsights, Az.Resources 및 Az.Storage의 주요 릴리스 출시</span><span class="sxs-lookup"><span data-stu-id="76011-1161">Az.ApiManagement, Az.Batch, Az.Compute, Az.KeyVault, Az.Monitor, Az.Network, Az.OperationalInsights, Az.Resources, and Az.Storage have major release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="76011-1162">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="76011-1162">Az.Accounts</span></span>
* <span data-ttu-id="76011-1163">'AzureSynapseAnalyticsEndpointResourceId' 및 'AzureSynapseAnalyticsEndpointSuffix' 매개 변수를 허용하도록 'Add-AzEnvironment' 및 'Set-AzEnvironment' 업데이트</span><span class="sxs-lookup"><span data-stu-id="76011-1163">Updated 'Add-AzEnvironment' and 'Set-AzEnvironment' to accept parameters 'AzureSynapseAnalyticsEndpointResourceId' and 'AzureSynapseAnalyticsEndpointSuffix'</span></span>
* <span data-ttu-id="76011-1164">Az.Accounts에 Azure.Core 관련 어셈블리가 추가되었으며 지원되는 PowerShell 플랫폼은 Windows PowerShell 5.1, PowerShell Core 6.2.4, PowerShell 7+입니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1164">Added Azure.Core related assemblies into Az.Accounts, supported PowerShell platforms include Windows PowerShell 5.1, PowerShell Core 6.2.4, PowerShell 7+</span></span>

#### <a name="azaks"></a><span data-ttu-id="76011-1165">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="76011-1165">Az.Aks</span></span>
* <span data-ttu-id="76011-1166">API 버전을 2019-10-01로 업그레이드</span><span class="sxs-lookup"><span data-stu-id="76011-1166">Upgraded API Version to 2019-10-01</span></span>
* <span data-ttu-id="76011-1167">Windows 컨테이너를 사용하여 AKS 만들기 지원</span><span class="sxs-lookup"><span data-stu-id="76011-1167">Supported to create AKS using Windows container</span></span>
* <span data-ttu-id="76011-1168">새 cmdlet 추가: 'New-AzAksNodePool', 'Update-AzAksNodePool', 'Remove-AzAksNodePool', 'Get-AzAksNodePool', 'Install-AzAksKubectl', 'Get-AzAksVersion'</span><span class="sxs-lookup"><span data-stu-id="76011-1168">Provided new cmdlets: 'New-AzAksNodePool', 'Update-AzAksNodePool', 'Remove-AzAksNodePool',        'Get-AzAksNodePool', 'Install-AzAksKubectl', 'Get-AzAksVersion'</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="76011-1169">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="76011-1169">Az.ApiManagement</span></span>
* <span data-ttu-id="76011-1170">'New-AzApiManagement' 및 'Set-AzApiManagement': [-AssignIdentity] 매개 변수 이름을 [-SystemAssignedIdentity]로 변경</span><span class="sxs-lookup"><span data-stu-id="76011-1170">'New-AzApiManagement' and 'Set-AzApiManagement': [-AssignIdentity] parameter renamed as [-SystemAssignedIdentity]</span></span>
* <span data-ttu-id="76011-1171">'New-AzApiManagement' 및 'Set-AzApiManagement': 새 매개 변수 추가: [-UserAssignedIdentity <String[]>]</span><span class="sxs-lookup"><span data-stu-id="76011-1171">'New-AzApiManagement' and 'Set-AzApiManagement': New parameter added: [-UserAssignedIdentity <String[]>]</span></span>
* <span data-ttu-id="76011-1172">'Get-AzApiManagementProperty': 'Get-AzApiManagementNamedValue'로 이름 변경.</span><span class="sxs-lookup"><span data-stu-id="76011-1172">'Get-AzApiManagementProperty': renamed as 'Get-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="76011-1173">PropertyId 매개 변수 이름을 NamedValueId로 변경.</span><span class="sxs-lookup"><span data-stu-id="76011-1173">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="76011-1174">'New-AzApiManagementProperty': 'New-AzApiManagementNamedValue'로 이름 변경.</span><span class="sxs-lookup"><span data-stu-id="76011-1174">'New-AzApiManagementProperty': renamed as 'New-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="76011-1175">PropertyId 매개 변수 이름을 NamedValueId로 변경.</span><span class="sxs-lookup"><span data-stu-id="76011-1175">PropertyId parameter renamed as NamedValueId.</span></span> 
* <span data-ttu-id="76011-1176">'Set-AzApiManagementProperty': 'Set-AzApiManagementNamedValue'로 이름 변경.</span><span class="sxs-lookup"><span data-stu-id="76011-1176">'Set-AzApiManagementProperty': renamed as 'Set-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="76011-1177">PropertyId 매개 변수 이름을 NamedValueId로 변경.</span><span class="sxs-lookup"><span data-stu-id="76011-1177">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="76011-1178">'Remove-AzApiManagementProperty': 'Remove-AzApiManagementNamedValue'로 이름 변경.</span><span class="sxs-lookup"><span data-stu-id="76011-1178">'Remove-AzApiManagementProperty': renamed as 'Remove-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="76011-1179">PropertyId 매개 변수 이름을 NamedValueId로 변경.</span><span class="sxs-lookup"><span data-stu-id="76011-1179">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="76011-1180">새 'Get-AzApiManagementAuthorizationServerClientSecret' cmdlet이 추가되었으며 'Get-AzApiManagementAuthorizationServer'는 더 이상 클라이언트 암호를 반환하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1180">Added new 'Get-AzApiManagementAuthorizationServerClientSecret' cmdlet and 'Get-AzApiManagementAuthorizationServer' will not return client secret anymore.</span></span>
* <span data-ttu-id="76011-1181">새 'Get-AzApiManagementNamedValueSecretValue' cmdlet이 추가되었으며 'Get-AzApiManagementNamedValue'는 더 이상 비밀 값을 반환하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1181">Added new 'Get-AzApiManagementNamedValueSecretValue' cmdlet and 'Get-AzApiManagementNamedValue' will not return secret value.</span></span>
* <span data-ttu-id="76011-1182">새 'Get-AzApiManagementOpenIdConnectProviderClientSecret' cmdlet이 추가되었으며 'Get-AzApiManagementOpenIdConnectProvider'는 더 이상 클라이언트 암호를 반환하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1182">Added new 'Get-AzApiManagementOpenIdConnectProviderClientSecret' cmdlet and 'Get-AzApiManagementOpenIdConnectProvider' will not return client secret anymore.</span></span>
* <span data-ttu-id="76011-1183">새 'Get-AzApiManagementSubscriptionKey' cmdlet이 추가되었으며 'Get-AzApiManagementSubscription'은 더 이상 구독 키를 반환하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1183">Added new 'Get-AzApiManagementSubscriptionKey' cmdlet and 'Get-AzApiManagementSubscription' will not return subscription keys anymore.</span></span>
* <span data-ttu-id="76011-1184">새 'Get-AzApiManagementTenantAccessSecret' cmdlet이 추가되었으며 'Get-AzApiManagementTenantAccess'는 더 이상 키를 반환하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1184">Added new 'Get-AzApiManagementTenantAccessSecret' cmdlet and 'Get-AzApiManagementTenantAccess' will not return keys anymore.</span></span>
* <span data-ttu-id="76011-1185">새 'Get-AzApiManagementTenantGitAccessSecret' cmdlet이 추가되었으며 'Get-AzApiManagementTenantGitAccess'는 더 이상 키를 반환하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1185">Added new 'Get-AzApiManagementTenantGitAccessSecret' cmdlet and 'Get-AzApiManagementTenantGitAccess' will not return keys anymore.</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="76011-1186">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="76011-1186">Az.ApplicationInsights</span></span>
* <span data-ttu-id="76011-1187">매개 변수 추가: 'New-AzApplicationInsights'에 대한 'RetentionInDays' 'PublicNetworkAccessForIngestion' 'PublicNetworkAccessForQuery'</span><span class="sxs-lookup"><span data-stu-id="76011-1187">Added Parameters: 'RetentionInDays' 'PublicNetworkAccessForIngestion' 'PublicNetworkAccessForQuery' for 'New-AzApplicationInsights'</span></span>
* <span data-ttu-id="76011-1188">'Update-AzApplicationInsights' cmdlet 작성</span><span class="sxs-lookup"><span data-stu-id="76011-1188">Created cmdlet 'Update-AzApplicationInsights'</span></span>
* <span data-ttu-id="76011-1189">연결된 스토리지 계정에 대한 cmdlet 작성</span><span class="sxs-lookup"><span data-stu-id="76011-1189">Created cmdlets for Linked Storage Account</span></span>

#### <a name="azbatch"></a><span data-ttu-id="76011-1190">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="76011-1190">Az.Batch</span></span>
* <span data-ttu-id="76011-1191">'Microsoft.Azure.Batch' SDK 버전 13.0.0 및 'Microsoft.Azure.Management.Batch' SDK 버전 9.0.0을 사용하도록 Az.Batch가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1191">Updated Az.Batch to use 'Microsoft.Azure.Batch' SDK version 13.0.0 and 'Microsoft.Azure.Management.Batch' SDK version 9.0.0.</span></span>
* <span data-ttu-id="76011-1192">새 '-CertificateKind' 매개 변수를 사용하여 'AzBatchCertificate'에 추가할 인증서 종류를 선택하는 기능이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1192">Added the ability to select the kind of certificate being added using the new '-CertificateKind' parameter to 'New-AzBatchCertificate'.</span></span>
* <span data-ttu-id="76011-1193">이전에 항상 ''였던 'ApplicationPackages' 속성이 'PSApplication'에서 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1193">Removed 'ApplicationPackages' property from 'PSApplication' which was previously always ''.</span></span>
  - <span data-ttu-id="76011-1194">이제 'Get-AzBatchApplicationPackage'를 사용하여 애플리케이션 내부의 특정 패키지를 검색할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1194">The specific packages inside of an application now can be retrieved using 'Get-AzBatchApplicationPackage'.</span></span> <span data-ttu-id="76011-1195">예를 들면 다음과 같습니다. 'Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication'.</span><span class="sxs-lookup"><span data-stu-id="76011-1195">For example: 'Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication'.</span></span>
* <span data-ttu-id="76011-1196">'New-AzBatchPool'을 사용하여 풀을 만들 때 'PSImageReference'의 'VirtualMachineImageId' 속성은 이제 Shared Image Gallery 이미지만 참조할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1196">When creating a pool using 'New-AzBatchPool', the 'VirtualMachineImageId' property of 'PSImageReference' can now only refer to a Shared Image Gallery image.</span></span>
* <span data-ttu-id="76011-1197">'New-AzBatchPool'을 사용하여 풀을 만들 때 공용 IP 없이 'PSNetworkConfiguration'의 새 'PublicIPAddressConfiguration'을 사용하여 풀을 프로비저닝할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1197">When creating a pool using 'New-AzBatchPool', the pool can be provisioned without a public IP using the new 'PublicIPAddressConfiguration' property of 'PSNetworkConfiguration'.</span></span>
  - <span data-ttu-id="76011-1198">'PSNetworkConfiguration'의 'PublicIPs' 속성도 'PSPublicIPAddressConfiguration'으로 이동되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1198">The 'PublicIPs' property of 'PSNetworkConfiguration' has moved in to 'PSPublicIPAddressConfiguration' as well.</span></span> <span data-ttu-id="76011-1199">이 속성은 'IPAddressProvisioningType'이 'UserManaged'인 경우에만 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1199">This property can only be specified if 'IPAddressProvisioningType' is 'UserManaged'.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="76011-1200">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="76011-1200">Az.Compute</span></span>
* <span data-ttu-id="76011-1201">'Update-AzVM' cmdlet에 HostId 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="76011-1201">Added HostId parameter to 'Update-AzVM' cmdlet</span></span>
* <span data-ttu-id="76011-1202">'New-AzVMConfig', 'New-AzVmssConfig', 'Update-AzVmss', 'Set-AzVMOperatingSystem' 및 'Set-AzVmssOsProfile' cmdlet의 도움말 문서가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1202">Updated Help documents for 'New-AzVMConfig', 'New-AzVmssConfig', 'Update-AzVmss', 'Set-AzVMOperatingSystem' and 'Set-AzVmssOsProfile' cmdlets.</span></span>
* <span data-ttu-id="76011-1203">주요 변경 내용</span><span class="sxs-lookup"><span data-stu-id="76011-1203">Breaking changes</span></span>
    - <span data-ttu-id="76011-1204">'Get-AzVMImage' cmdlet에서 FilterExpression 매개 변수가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1204">FilterExpression parameter is removed from 'Get-AzVMImage' cmdlet.</span></span>
    - <span data-ttu-id="76011-1205">'New-AzVmssConfig', 'New-AzVMConfig' 및 'Update-AzVM' cmdlet에서 AssignIdentity 매개 변수가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1205">AssignIdentity parameter is removed from 'New-AzVmssConfig', 'New-AzVMConfig' and 'Update-AzVM' cmdlets.</span></span>
    - <span data-ttu-id="76011-1206">'New-AzVmssConfig' 및 'Update-AzVmss' cmdlet에서 AutomaticRepairMaxInstanceRepairsPercent가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1206">AutomaticRepairMaxInstanceRepairsPercent is removed from 'New-AzVmssConfig' and 'Update-AzVmss' cmdlets.</span></span>
    - <span data-ttu-id="76011-1207">ProximityPlacementGroup에서 AvailabilitySetsColocationStatus, VirtualMachinesColocationStatus 및 VirtualMachineScaleSetsColocationStatus 속성이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1207">AvailabilitySetsColocationStatus, VirtualMachinesColocationStatus and VirtualMachineScaleSetsColocationStatus properties are removed from ProximityPlacementGroup.</span></span>
    - <span data-ttu-id="76011-1208">AutomaticRepairsPolicy에서 MaxInstanceRepairsPercent 속성이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1208">MaxInstanceRepairsPercent property is removed from AutomaticRepairsPolicy.</span></span>
    - <span data-ttu-id="76011-1209">AvailabilitySets, VirtualMachines 및 VirtualMachineScaleSets 형식이 IList<SubResource>에서 IList<SubResourceWithColocationStatus>로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1209">The types of AvailabilitySets, VirtualMachines and VirtualMachineScaleSets are changed from IList<SubResource> to IList<SubResourceWithColocationStatus>.</span></span>
* <span data-ttu-id="76011-1210">'Get-AzVM' cmdlet에 대한 설명이 보다 정확하게 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1210">Description for 'Get-AzVM' cmdlet has been updated to better describe it.</span></span> 

#### <a name="azdatafactory"></a><span data-ttu-id="76011-1211">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="76011-1211">Az.DataFactory</span></span>
* <span data-ttu-id="76011-1212">Managed IR에서 데이터 흐름 런타임 속성의 CRUD를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1212">Supported CRUD of data flow runtime properties in Managed IR.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="76011-1213">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="76011-1213">Az.FrontDoor</span></span>
* <span data-ttu-id="76011-1214">Front Door 규칙 엔진 개체를 생성, 업데이트, 검색 및 삭제할 수 있는 새 cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="76011-1214">Added new cmdlets for creation, update, retreival, and deletion of Front Door Rules Engine object</span></span>
* <span data-ttu-id="76011-1215">Front Door 규칙 엔진 개체를 작성할 수 있는 도우미 cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="76011-1215">Added helper cmdlets for construction of Front Door Rules Engine object</span></span>
* <span data-ttu-id="76011-1216">Front Door 회람 규칙 개체에 대한 규칙 엔진 참조 추가</span><span class="sxs-lookup"><span data-stu-id="76011-1216">Added Rules Engine reference to Front Door Routing Rule object.</span></span>
* <span data-ttu-id="76011-1217">Front Door 백 엔드 개체에 Private Link 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="76011-1217">Added Private Link parameters to Front Door Backend object</span></span>

#### <a name="azfunctions"></a><span data-ttu-id="76011-1218">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="76011-1218">Az.Functions</span></span>
* <span data-ttu-id="76011-1219">''Az.Functions'' 모듈의 일반 공급</span><span class="sxs-lookup"><span data-stu-id="76011-1219">General availability of ''Az.Functions'' module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="76011-1220">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="76011-1220">Az.HDInsight</span></span>
* <span data-ttu-id="76011-1221">고객 관리형 키 디스크 암호화 지원</span><span class="sxs-lookup"><span data-stu-id="76011-1221">Supported Customer-managed key disk encryption.</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="76011-1222">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="76011-1222">Az.HealthcareApis</span></span>
* <span data-ttu-id="76011-1223">더 이상 액세스 정책이 기본적으로 현재 보안 주체로 설정되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1223">Access policies are no longer defaulted to the current principal</span></span>

#### <a name="aziothub"></a><span data-ttu-id="76011-1224">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="76011-1224">Az.IotHub</span></span>
* <span data-ttu-id="76011-1225">SQL과 비슷한 언어를 사용하여 정보를 검색하기 위해 IoT 허브에서 쿼리를 호출하는 cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1225">Added cmdlet to invoke a query in an IoT hub to retrieve information using a SQL-like language.</span></span>
* <span data-ttu-id="76011-1226">'Add-AzIotHubDevice'가 자식 디바이스 없는 에지 지원 디바이스를 만들 수 없는 문제 해결 [#11597]</span><span class="sxs-lookup"><span data-stu-id="76011-1226">Fix issue that 'Add-AzIotHubDevice' fails to create Edge Enabled Device without child devices [#11597]</span></span>
* <span data-ttu-id="76011-1227">IoT Hub, 디바이스 또는 모듈에 대한 SAS 토큰을 생성하는 cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1227">Added cmdlet to generate SAS token for Iot Hub, device or module.</span></span>
* <span data-ttu-id="76011-1228">구성 메트릭 쿼리를 호출하는 cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1228">Added cmdlet to invoke configuration metrics query.</span></span>
* <span data-ttu-id="76011-1229">IoT Edge 자동 배포를 대규모로 관리합니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1229">Manage IoT Edge automatic deployment at scale.</span></span> <span data-ttu-id="76011-1230">새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1230">New cmdlets are:</span></span>
    - <span data-ttu-id="76011-1231">'Add-AzIotHubDeployment'</span><span class="sxs-lookup"><span data-stu-id="76011-1231">'Add-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="76011-1232">'Get-AzIotHubDeployment'</span><span class="sxs-lookup"><span data-stu-id="76011-1232">'Get-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="76011-1233">'Remove-AzIotHubDeployment'</span><span class="sxs-lookup"><span data-stu-id="76011-1233">'Remove-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="76011-1234">'Set-AzIotHubDeployment'</span><span class="sxs-lookup"><span data-stu-id="76011-1234">'Set-AzIotHubDeployment'</span></span>
* <span data-ttu-id="76011-1235">IoT Edge 배포 메트릭 쿼리를 호출하는 cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1235">Added cmdlet to invoke an IoT Edge deployment metrics query.</span></span>
* <span data-ttu-id="76011-1236">지정된 에지 디바이스에 구성 콘텐츠를 적용하는 cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1236">Added cmdlet to apply the configuration content to the specified edge device.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="76011-1237">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="76011-1237">Az.KeyVault</span></span>
* <span data-ttu-id="76011-1238">다음 별칭 제거: 'New-AzKeyVaultCertificateAdministratorDetails' 및 'New-AzKeyVaultCertificateOrganizationDetails'</span><span class="sxs-lookup"><span data-stu-id="76011-1238">Removed two aliases: 'New-AzKeyVaultCertificateAdministratorDetails' and 'New-AzKeyVaultCertificateOrganizationDetails'</span></span>
* <span data-ttu-id="76011-1239">키 자격 증명 모음을 만들 때 기본적으로 일시 삭제 사용</span><span class="sxs-lookup"><span data-stu-id="76011-1239">Enabled soft delete by default when creating a key vault</span></span>
* <span data-ttu-id="76011-1240">키 자격 증명 모음을 만들 때 특정 네트워크 위치의 액세스를 제어하도록 네트워크 규칙을 설정할 수 있음</span><span class="sxs-lookup"><span data-stu-id="76011-1240">Network rules can be set to govern the accessibility from specific network locations when creating a key vault</span></span>
* <span data-ttu-id="76011-1241">BYOK(Bring Your Own Key) 지원 추가</span><span class="sxs-lookup"><span data-stu-id="76011-1241">Added support to bring your own key (BYOK)</span></span>
    - <span data-ttu-id="76011-1242">'Add-AzKeyVaultKey'가 키 교환 키 생성 지원</span><span class="sxs-lookup"><span data-stu-id="76011-1242">'Add-AzKeyVaultKey' supports generating a key exchange key</span></span>
    - <span data-ttu-id="76011-1243">'Get-AzKeyVaultKey'가 PEM 형식의 공개 키 다운로드 지원</span><span class="sxs-lookup"><span data-stu-id="76011-1243">'Get-AzKeyVaultKey' supports downloading a public key in PEM format</span></span>
* <span data-ttu-id="76011-1244">'AzKeyVaultKey' 도움말 문서의 'KeyOps' 부분 업데이트</span><span class="sxs-lookup"><span data-stu-id="76011-1244">Updated the 'KeyOps' part of the help document of 'Add-AzKeyVaultKey'</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="76011-1245">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="76011-1245">Az.Monitor</span></span>
* <span data-ttu-id="76011-1246">'Set-AzDiagnosticSettings'의 버그 수정, 일부 범주에는 보존 정책이 적용되지 않음 [#11589]</span><span class="sxs-lookup"><span data-stu-id="76011-1246">Fixed bug for 'Set-AzDiagnosticSettings', retention policy won't apply to all categories [#11589]</span></span>
* <span data-ttu-id="76011-1247">메트릭 경고 V2에 WebTest를 사용하기 위한 조건 지원</span><span class="sxs-lookup"><span data-stu-id="76011-1247">Supported WebTest availability criteria for metric alert V2</span></span>
    - <span data-ttu-id="76011-1248">'New-AzMetricAlertRuleV2Criteria': webtest 사용 조건을 만드는 옵션 추가</span><span class="sxs-lookup"><span data-stu-id="76011-1248">'New-AzMetricAlertRuleV2Criteria': an option to create webtest availability criteria was added</span></span>
    - <span data-ttu-id="76011-1249">'Add-AzMetricAlertRuleV2': 새 webtest 사용 조건 지원</span><span class="sxs-lookup"><span data-stu-id="76011-1249">'Add-AzMetricAlertRuleV2': supports the new webtest availability criteria</span></span>
* <span data-ttu-id="76011-1250">PSLogProfile에서 RetentionPolicy에 대한 중복 정의 제거 [#7608]</span><span class="sxs-lookup"><span data-stu-id="76011-1250">Removed redundant definition for RetentionPolicy in PSLogProfile [#7608]</span></span>
* <span data-ttu-id="76011-1251">PSEventData에 정의된 중복 속성 제거 [#11353]</span><span class="sxs-lookup"><span data-stu-id="76011-1251">Removed redundant properties difined in PSEventData [#11353]</span></span>
* <span data-ttu-id="76011-1252">'Get-AzLog'를 'Get-AzActivityLog'로 이름 변경</span><span class="sxs-lookup"><span data-stu-id="76011-1252">Renamed 'Get-AzLog' to 'Get-AzActivityLog'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="76011-1253">Az.Network</span><span class="sxs-lookup"><span data-stu-id="76011-1253">Az.Network</span></span>
* <span data-ttu-id="76011-1254">영역 기본 동작이 변경된다는 것을 알리기 위해 주요 변경 특성을 추가</span><span class="sxs-lookup"><span data-stu-id="76011-1254">Added breaking change attribute to notify that Zone default behaviour will be changed</span></span>
    - <span data-ttu-id="76011-1255">'New-AzPublicIpAddress'</span><span class="sxs-lookup"><span data-stu-id="76011-1255">'New-AzPublicIpAddress'</span></span>
    - <span data-ttu-id="76011-1256">'New-AzPublicIpPrefix'</span><span class="sxs-lookup"><span data-stu-id="76011-1256">'New-AzPublicIpPrefix'</span></span>
    - <span data-ttu-id="76011-1257">'New-AzLoadBalancerFrontendIpConfig'</span><span class="sxs-lookup"><span data-stu-id="76011-1257">'New-AzLoadBalancerFrontendIpConfig'</span></span>
* <span data-ttu-id="76011-1258">새로운 최상위 리소스 SecurityPartnerProvider에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="76011-1258">Added support for a new top level resource SecurityPartnerProvider</span></span>
    - <span data-ttu-id="76011-1259">추가된 새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1259">New cmdlets added:</span></span>
        - <span data-ttu-id="76011-1260">New-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="76011-1260">New-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="76011-1261">Remove-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="76011-1261">Remove-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="76011-1262">Get-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="76011-1262">Get-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="76011-1263">Set-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="76011-1263">Set-AzSecurityPartnerProvider</span></span>
* <span data-ttu-id="76011-1264">'PSPrivateEndpointConnection'의 'PSPrivateLinkResource' 및 'GroupId'에서 'RequiredZoneNames' 추가</span><span class="sxs-lookup"><span data-stu-id="76011-1264">Added 'RequiredZoneNames' on 'PSPrivateLinkResource' and 'GroupId' on 'PSPrivateEndpointConnection'</span></span>
* <span data-ttu-id="76011-1265">New-AzNetworkWatcherConnectionMonitorTestConfigurationObject에 대한 잘못된 형식의 SuccessThresholdRoundTripTimeMs 매개 변수 수정</span><span class="sxs-lookup"><span data-stu-id="76011-1265">Fixed incorrect type of SuccessThresholdRoundTripTimeMs parameter for New-AzNetworkWatcherConnectionMonitorTestConfigurationObject</span></span>
* <span data-ttu-id="76011-1266">AllowVnetToVnetTraffic 인수의 기본값을 True로 설정하도록 VirtualWan cmdlet 업데이트</span><span class="sxs-lookup"><span data-stu-id="76011-1266">Updated VirtualWan cmdlets to set default value of AllowVnetToVnetTraffic argument to True.</span></span>
    - <span data-ttu-id="76011-1267">'New-AzVirtualWan'</span><span class="sxs-lookup"><span data-stu-id="76011-1267">'New-AzVirtualWan'</span></span>
    - <span data-ttu-id="76011-1268">'Update-AzVirtualWan'</span><span class="sxs-lookup"><span data-stu-id="76011-1268">'Update-AzVirtualWan'</span></span>
* <span data-ttu-id="76011-1269">프라이빗 엔드포인트에 대한 DNS 영역 그룹을 지원하는 새 cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="76011-1269">Added new cmdlets to support DNS zone group for private endpoint</span></span>
    - <span data-ttu-id="76011-1270">'New-AzPrivateDnsZoneConfig'</span><span class="sxs-lookup"><span data-stu-id="76011-1270">'New-AzPrivateDnsZoneConfig'</span></span>
    - <span data-ttu-id="76011-1271">'Get-AzPrivateDnsZoneGroup'</span><span class="sxs-lookup"><span data-stu-id="76011-1271">'Get-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="76011-1272">'New-AzPrivateDnsZoneGroup'</span><span class="sxs-lookup"><span data-stu-id="76011-1272">'New-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="76011-1273">'Set-AzPrivateDnsZoneGroup'</span><span class="sxs-lookup"><span data-stu-id="76011-1273">'Set-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="76011-1274">'Remove-AzPrivateDnsZoneGroup'</span><span class="sxs-lookup"><span data-stu-id="76011-1274">'Remove-AzPrivateDnsZoneGroup'</span></span>
* <span data-ttu-id="76011-1275">'AzureFirewall'에 'DNSEnableProxy', 'DNSRequireProxyForNetworkRules' 및 'DNSServers' 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="76011-1275">Added 'DNSEnableProxy', 'DNSRequireProxyForNetworkRules' and 'DNSServers' parameters to 'AzureFirewall'</span></span>
* <span data-ttu-id="76011-1276">'AzureFirewall'에 'EnableDnsProxy', 'DnsProxyNotRequiredForNetworkRule' 및 'DnsServer' 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="76011-1276">Added 'EnableDnsProxy', 'DnsProxyNotRequiredForNetworkRule' and 'DnsServer' parameters to 'AzureFirewall'</span></span>
    - <span data-ttu-id="76011-1277">업데이트된 cmdlet:</span><span class="sxs-lookup"><span data-stu-id="76011-1277">Updated cmdlet:</span></span>
        - <span data-ttu-id="76011-1278">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="76011-1278">New-AzFirewall</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="76011-1279">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="76011-1279">Az.OperationalInsights</span></span>
* <span data-ttu-id="76011-1280">새로 생성된 SDK를 적용하도록 레거시 코드 업데이트</span><span class="sxs-lookup"><span data-stu-id="76011-1280">Updated legacy code to apply new generated SDK</span></span>
* <span data-ttu-id="76011-1281">사용되지 않는 API 때문에 cmdlet 삭제</span><span class="sxs-lookup"><span data-stu-id="76011-1281">Deleted cmdlets due to deprecated APIs</span></span>
    - <span data-ttu-id="76011-1282">'Get-AzOperationalInsightsSavedSearchResult'(별칭 'Get-AzOperationalInsightsSavedSearchResults')</span><span class="sxs-lookup"><span data-stu-id="76011-1282">'Get-AzOperationalInsightsSavedSearchResult' (alias 'Get-AzOperationalInsightsSavedSearchResults')</span></span>
    - <span data-ttu-id="76011-1283">'Get-AzOperationalInsightsSearchResult'(별칭 'Get-AzOperationalInsightsSearchResults')</span><span class="sxs-lookup"><span data-stu-id="76011-1283">'Get-AzOperationalInsightsSearchResult' (alias 'Get-AzOperationalInsightsSearchResults')</span></span>
    - <span data-ttu-id="76011-1284">'Get-AzOperationalInsightsLinkTarget'(별칭 'Get-AzOperationalInsightsLinkTargets')</span><span class="sxs-lookup"><span data-stu-id="76011-1284">'Get-AzOperationalInsightsLinkTarget' (alias 'Get-AzOperationalInsightsLinkTargets')</span></span>
* <span data-ttu-id="76011-1285">'Set-AzOperationalInsightsWorkspace' 및 'New-AzOperationalInsightsWorkspace'에 대한 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="76011-1285">Added parameters for 'Set-AzOperationalInsightsWorkspace' and 'New-AzOperationalInsightsWorkspace'</span></span>
* <span data-ttu-id="76011-1286">연결된 스토리지 계정에 대한 cmdlet 작성</span><span class="sxs-lookup"><span data-stu-id="76011-1286">Created cmdlets for Linked Stoarge Account</span></span>
* <span data-ttu-id="76011-1287">클러스터 및 연결된 서비스에 대한 cmdlet 작성</span><span class="sxs-lookup"><span data-stu-id="76011-1287">Created cmdlets for Clusters and Linked Service</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="76011-1288">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="76011-1288">Az.RecoveryServices</span></span>
* <span data-ttu-id="76011-1289">Azure Site Recovery - Azure와 Azure 공급자 간 근접 배치 그룹 가상 머신을 보호하기 위한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1289">Azure Site Recovery added support for protecting proximity placement group virtual machines for Azure to Azure provider.</span></span>
* <span data-ttu-id="76011-1290">Azure Site Recovery - 영역 간 복제에 대한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1290">Azure Site Recovery added support for zone to zone replication.</span></span>
* <span data-ttu-id="76011-1291">Azure Backup - Azure 파일 공유 복구 지점의 장기 보존 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1291">Azure Backup Added Long term retention support for Azure FileShare Recovery Points.</span></span>
* <span data-ttu-id="76011-1292">Azure Backup - 'Get-AzRecoveryServicesBackupItem' cmdlet 출력에 디스크 제외 속성이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1292">Azure Backup Added disk exclusion properties to 'Get-AzRecoveryServicesBackupItem' cmdlet output.</span></span>
* <span data-ttu-id="76011-1293">사이트 복구 서비스용 Vault 자격 증명 파일에 대한 프라이빗 엔드포인트가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1293">Added private endpoint for Vault credential file for site recovery service.</span></span>

#### <a name="azresources"></a><span data-ttu-id="76011-1294">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="76011-1294">Az.Resources</span></span>
* <span data-ttu-id="76011-1295">새 역할 정의를 만들 때 보기 지연에 대한 메시지 경고 추가</span><span class="sxs-lookup"><span data-stu-id="76011-1295">Added message warning about view delay when creating a new Role Definition</span></span>
* <span data-ttu-id="76011-1296">강력한 형식의 개체를 출력하도록 정책 cmdlet 변경</span><span class="sxs-lookup"><span data-stu-id="76011-1296">Changed policy cmdlets to output strongly-typed objects</span></span>
* <span data-ttu-id="76011-1297">'Get-AzResourceLock' cmdlet에 사용되는 '-TenantLevel' 매개 변수 제거 [#11335]</span><span class="sxs-lookup"><span data-stu-id="76011-1297">Removed '-TenantLevel' parameter used for on the 'Get-AzResourceLock' cmdlet [#11335]</span></span>
* <span data-ttu-id="76011-1298">'Remove-AzResourceGroup -Id ResourceId' 수정[#9882]</span><span class="sxs-lookup"><span data-stu-id="76011-1298">Fixed 'Remove-AzResourceGroup -Id ResourceId'[#9882]</span></span>
* <span data-ttu-id="76011-1299">리소스 그룹 범위에서 ARM 템플릿 가상 시나리오 결과를 가져오는 새 cmdlet 추가: 'Get-AzDeploymentResourceGroupWhatIfResult'</span><span class="sxs-lookup"><span data-stu-id="76011-1299">Added new cmdlet for getting ARM template What-If results at resource group scope: 'Get-AzDeploymentResourceGroupWhatIfResult'</span></span>
* <span data-ttu-id="76011-1300">구독 범위에서 ARM 템플릿 가상 시나리오 결과를 가져오는 새 cmdlet 추가: 'Get-AzDeploymentWhatIfResult'</span><span class="sxs-lookup"><span data-stu-id="76011-1300">Added new cmdlet for getting ARM template What-If results at subscription scope: 'Get-AzDeploymentWhatIfResult'</span></span>
   - <span data-ttu-id="76011-1301">별칭: 'Get-AzSubscriptionDeploymentWhatIf'</span><span class="sxs-lookup"><span data-stu-id="76011-1301">Alias: 'Get-AzSubscriptionDeploymentWhatIf'</span></span>
* <span data-ttu-id="76011-1302">ARM 템플릿 가상 시나리오 결과를 사용하도록 'New-AzDeployment' 및 'New-AzResourceGroupDeployment'에 대한 '-WhatIf' 및 '-Confirm' 매개 변수 재정의</span><span class="sxs-lookup"><span data-stu-id="76011-1302">Overrode '-WhatIf' and '-Confirm' parameters for 'New-AzDeployment' and 'New-AzResourceGroupDeployment' to use ARM template What-If results</span></span>
* <span data-ttu-id="76011-1303">배포 cmdlet에서 'ApiVersion' 매개 변수의 사용 중단 메시지 추가</span><span class="sxs-lookup"><span data-stu-id="76011-1303">Added deprecation message for 'ApiVersion' parameter in deployment cmdlets</span></span>
* <span data-ttu-id="76011-1304">배포 오류에 대한 향상된 오류 메시지를 표시하는 기능 추가</span><span class="sxs-lookup"><span data-stu-id="76011-1304">Added capability to show improved error messages for deployment failures</span></span>
* <span data-ttu-id="76011-1305">배포 오류에 대한 correlationId 로깅 추가</span><span class="sxs-lookup"><span data-stu-id="76011-1305">Added correlationId logging for deployment failures</span></span>
* <span data-ttu-id="76011-1306">배포 스크립트 출력에 'error' 속성 추가</span><span class="sxs-lookup"><span data-stu-id="76011-1306">Added 'error' property to the deployment script output</span></span>
* <span data-ttu-id="76011-1307">nuget Microsoft.Azure.Management.ResourceManager를 '3.7.1-preview'로 업데이트</span><span class="sxs-lookup"><span data-stu-id="76011-1307">Updated nuget Microsoft.Azure.Management.ResourceManager to '3.7.1-preview'</span></span>
* <span data-ttu-id="76011-1308">nuget 3.7.1-preview에서 DeploymentValidateResult의 Error 속성이 readonly로 변경되어 특정 테스트 사례를 제거</span><span class="sxs-lookup"><span data-stu-id="76011-1308">Removed specific test cases as Error property in DeploymentValidateResult has changed to readonly from nuget 3.7.1-preview</span></span>
* <span data-ttu-id="76011-1309">SDK ResourceManager 3.7.1-preview의 GenericResourceExpanded 도입</span><span class="sxs-lookup"><span data-stu-id="76011-1309">Brought GenericResourceExpanded from SDK ResourceManager 3.7.1-preview</span></span>
* <span data-ttu-id="76011-1310">모든 배포용 Get cmdlet에 대한 태그 지원 추가</span><span class="sxs-lookup"><span data-stu-id="76011-1310">Added tag support for all Get cmdlets for deployment, as well as</span></span>
    - <span data-ttu-id="76011-1311">'New-AzDeployment'</span><span class="sxs-lookup"><span data-stu-id="76011-1311">'New-AzDeployment'</span></span>
    - <span data-ttu-id="76011-1312">'New-AzManagementGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="76011-1312">'New-AzManagementGroupDeployment'</span></span>
    - <span data-ttu-id="76011-1313">'New-AzResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="76011-1313">'New-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="76011-1314">'New-AzTenantDeployment'</span><span class="sxs-lookup"><span data-stu-id="76011-1314">'New-AzTenantDeployment'</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="76011-1315">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="76011-1315">Az.ServiceFabric</span></span>
* <span data-ttu-id="76011-1316">잘못된 인증서 지문을 가져오는 --SecretIdentifier를 사용한 인증서 추가의 버그 수정</span><span class="sxs-lookup"><span data-stu-id="76011-1316">Fixed bug in add certificate using --SecretIdentifier that was getting the wrong certificate thumbprint</span></span>

#### <a name="azsql"></a><span data-ttu-id="76011-1317">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="76011-1317">Az.Sql</span></span>
* <span data-ttu-id="76011-1318">성능 강화:</span><span class="sxs-lookup"><span data-stu-id="76011-1318">Enhance performance of:</span></span>
    - <span data-ttu-id="76011-1319">'Set-AzSqlDatabaseSensitivityClassification'</span><span class="sxs-lookup"><span data-stu-id="76011-1319">'Set-AzSqlDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="76011-1320">'Set-AzSqlInstanceDatabaseSensitivityClassification'</span><span class="sxs-lookup"><span data-stu-id="76011-1320">'Set-AzSqlInstanceDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="76011-1321">'Remove-AzSqlDatabaseSensitivityClassification'</span><span class="sxs-lookup"><span data-stu-id="76011-1321">'Remove-AzSqlDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="76011-1322">'Remove-AzSqlInstanceDatabaseSensitivityClassification'</span><span class="sxs-lookup"><span data-stu-id="76011-1322">'Remove-AzSqlInstanceDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="76011-1323">'Enable-AzSqlDatabaseSensitivityRecommendation'</span><span class="sxs-lookup"><span data-stu-id="76011-1323">'Enable-AzSqlDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="76011-1324">'Enable-AzSqlInstanceDatabaseSensitivityRecommendation'</span><span class="sxs-lookup"><span data-stu-id="76011-1324">'Enable-AzSqlInstanceDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="76011-1325">'Disable-AzSqlDatabaseSensitivityRecommendation'</span><span class="sxs-lookup"><span data-stu-id="76011-1325">'Disable-AzSqlDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="76011-1326">'Disable-AzSqlInstanceDatabaseSensitivityRecommendation'</span><span class="sxs-lookup"><span data-stu-id="76011-1326">'Disable-AzSqlInstanceDatabaseSensitivityRecommendation'</span></span>
* <span data-ttu-id="76011-1327">'Set-AzSqlDatabaseBackupShortTermRetentionPolicy' cmdlet에서 'RetentionDays' 매개 변수의 클라이언트 쪽 유효성 검사 제거</span><span class="sxs-lookup"><span data-stu-id="76011-1327">Removed client-side validation of 'RetentionDays' parameter from cmdlet 'Set-AzSqlDatabaseBackupShortTermRetentionPolicy'</span></span>
* <span data-ttu-id="76011-1328">Vnet에서 스토리지 계정을 감사하고, Storage Blob 데이터 기여자 역할을 만들 때 발생하는 버그 수정</span><span class="sxs-lookup"><span data-stu-id="76011-1328">Auditing to a storage account in Vnet, fixing a bug when creating a Storage Blob Data Contributor role.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="76011-1329">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="76011-1329">Az.Storage</span></span>
* <span data-ttu-id="76011-1330">get/list account cmdlet 'Get-AzStorageAccount'에 '-AsJob' 추가</span><span class="sxs-lookup"><span data-stu-id="76011-1330">Added '-AsJob' to get/list account cmdlet 'Get-AzStorageAccount'</span></span>
* <span data-ttu-id="76011-1331">키 자동 회전을 지원하기 위해 스토리지 계정을 KeyvaultEncryption으로 업데이트할 때 KeyVersion을 선택 사항으로 지정</span><span class="sxs-lookup"><span data-stu-id="76011-1331">Make KeyVersion to optional when update Storage account with KeyvaultEncryption, to support key auto-rotation</span></span>
    - <span data-ttu-id="76011-1332">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="76011-1332">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="76011-1333">파이프라인을 사용하여 Azure 파일 디렉터리 제거 오류 수정</span><span class="sxs-lookup"><span data-stu-id="76011-1333">Fixed remove Azure File Directory fail with pipeline</span></span>
    - <span data-ttu-id="76011-1334">'Remove-AzStorageDirectory'</span><span class="sxs-lookup"><span data-stu-id="76011-1334">'Remove-AzStorageDirectory'</span></span>
* <span data-ttu-id="76011-1335">수정 [#9880]: Swagger에 맞게 NetWorkRule DefaultAction 값 정의 변경</span><span class="sxs-lookup"><span data-stu-id="76011-1335">Fixed [#9880]: Change NetWorkRule DefaultAction value defination to align with swagger.</span></span>
    - <span data-ttu-id="76011-1336">'Update-AzStorageAccountNetworkRuleSet'</span><span class="sxs-lookup"><span data-stu-id="76011-1336">'Update-AzStorageAccountNetworkRuleSet'</span></span>
    - <span data-ttu-id="76011-1337">'Get-AzStorageAccountNetworkRuleSet'</span><span class="sxs-lookup"><span data-stu-id="76011-1337">'Get-AzStorageAccountNetworkRuleSet'</span></span>
* <span data-ttu-id="76011-1338">수정 [#11624]: 서버 오류를 방지하기 위해 NetworkRules를 추가할 때 중복 규칙 건너뛰기</span><span class="sxs-lookup"><span data-stu-id="76011-1338">Fixed [#11624]: Skip duplicated rules when add NetworkRules, to avoid server failure</span></span>
    - <span data-ttu-id="76011-1339">'Add-AzStorageAccountNetworkRule'</span><span class="sxs-lookup"><span data-stu-id="76011-1339">'Add-AzStorageAccountNetworkRule'</span></span>
* <span data-ttu-id="76011-1340">Microsoft.Azure.Cosmos.Table SDK를 1.0.7로 업그레이드</span><span class="sxs-lookup"><span data-stu-id="76011-1340">Upgraded Microsoft.Azure.Cosmos.Table SDK to 1.0.7</span></span>
* <span data-ttu-id="76011-1341">DataLake Gen2 항목 목록에 부품 항목만 반환되는 경우 ContinuationToken을 사용하여 다시 나열하라고 사용자에게 알리는 경고 메시지 추가</span><span class="sxs-lookup"><span data-stu-id="76011-1341">Added a warning message to remind user to list again with ContinuationToken when only part items are returned in list DataLake Gen2 Items,</span></span>
    - <span data-ttu-id="76011-1342">'Get-AzDataLakeGen2ChildItem'</span><span class="sxs-lookup"><span data-stu-id="76011-1342">'Get-AzDataLakeGen2ChildItem'</span></span>
* <span data-ttu-id="76011-1343">Azure Files Active Directory 도메인 서비스 인증을 사용하여 스토리지 계정을 만들거나 업데이트하는 기능 지원</span><span class="sxs-lookup"><span data-stu-id="76011-1343">Supported to create or update Storage account with Azure Files Active Directory Domain Service Authentication</span></span>
    -  <span data-ttu-id="76011-1344">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="76011-1344">'New-AzStorageAccount'</span></span>
    -  <span data-ttu-id="76011-1345">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="76011-1345">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="76011-1346">스토리지 계정의 Kerberos 키 새로 만들기 또는 나열 지원</span><span class="sxs-lookup"><span data-stu-id="76011-1346">Supported to new or list Kerberos keys of Storage account</span></span>
    -  <span data-ttu-id="76011-1347">'New-AzStorageAccountKey'</span><span class="sxs-lookup"><span data-stu-id="76011-1347">'New-AzStorageAccountKey'</span></span>
    -  <span data-ttu-id="76011-1348">'Get-AzStorageAccountKey'</span><span class="sxs-lookup"><span data-stu-id="76011-1348">'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="76011-1349">스토리지 계정 장애 조치(failover) 지원</span><span class="sxs-lookup"><span data-stu-id="76011-1349">Supported failover Storage account</span></span>
    - <span data-ttu-id="76011-1350">'Invoke-AzStorageAccountFailover'</span><span class="sxs-lookup"><span data-stu-id="76011-1350">'Invoke-AzStorageAccountFailover'</span></span>
* <span data-ttu-id="76011-1351">'Get-AzStorageBlobCopyState'의 도움말 업데이트</span><span class="sxs-lookup"><span data-stu-id="76011-1351">Updated help of 'Get-AzStorageBlobCopyState'</span></span>
* <span data-ttu-id="76011-1352">'Get-AzStorageFileCopyState' 및 'Start-AzStorageBlobCopy'의 도움말 업데이트</span><span class="sxs-lookup"><span data-stu-id="76011-1352">Updated help of 'Get-AzStorageFileCopyState' and 'Start-AzStorageBlobCopy'</span></span>
* <span data-ttu-id="76011-1353">스토리지 클라이언트 라이브러리 v12를 큐 및 파일 cmdlet에 통합</span><span class="sxs-lookup"><span data-stu-id="76011-1353">Integrated Storage client library v12 to Queue and File cmdlets</span></span>
* <span data-ttu-id="76011-1354">출력 형식을 CloudFile에서 AzureStorageFile로 변경했으며, 원래 출력은 새 출력의 자식 속성이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1354">Changed output type from CloudFile to AzureStorageFile, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="76011-1355">'Get-AzStorageFile'</span><span class="sxs-lookup"><span data-stu-id="76011-1355">'Get-AzStorageFile'</span></span>
    - <span data-ttu-id="76011-1356">'Remove-AzStorageFile'</span><span class="sxs-lookup"><span data-stu-id="76011-1356">'Remove-AzStorageFile'</span></span>
    - <span data-ttu-id="76011-1357">'Get-AzStorageFileContent'</span><span class="sxs-lookup"><span data-stu-id="76011-1357">'Get-AzStorageFileContent'</span></span>
    - <span data-ttu-id="76011-1358">'Set-AzStorageFileContent'</span><span class="sxs-lookup"><span data-stu-id="76011-1358">'Set-AzStorageFileContent'</span></span>
    - <span data-ttu-id="76011-1359">'Start-AzStorageFileCopy'</span><span class="sxs-lookup"><span data-stu-id="76011-1359">'Start-AzStorageFileCopy'</span></span>
* <span data-ttu-id="76011-1360">출력 형식을 CloudFileDirectory에서 AzureStorageFileDirectory로 변경했으며, 원래 출력은 새 출력의 자식 속성이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1360">Changed output type from CloudFileDirectory to AzureStorageFileDirectory, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="76011-1361">'New-AzStorageDirectory'</span><span class="sxs-lookup"><span data-stu-id="76011-1361">'New-AzStorageDirectory'</span></span>
    - <span data-ttu-id="76011-1362">'Remove-AzStorageDirectory'</span><span class="sxs-lookup"><span data-stu-id="76011-1362">'Remove-AzStorageDirectory'</span></span>
* <span data-ttu-id="76011-1363">출력 형식을 CloudFileShare에서 AzureStorageFileShare로 변경했으며, 원래 출력은 새 출력의 자식 속성이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1363">Changed output type from CloudFileShare to AzureStorageFileShare, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="76011-1364">'Get-AzStorageShare'</span><span class="sxs-lookup"><span data-stu-id="76011-1364">'Get-AzStorageShare'</span></span>
    - <span data-ttu-id="76011-1365">'New-AzStorageShare'</span><span class="sxs-lookup"><span data-stu-id="76011-1365">'New-AzStorageShare'</span></span>
    - <span data-ttu-id="76011-1366">'Remove-AzStorageShare'</span><span class="sxs-lookup"><span data-stu-id="76011-1366">'Remove-AzStorageShare'</span></span>
* <span data-ttu-id="76011-1367">출력 형식을 FileShareProperties에서 AzureStorageFileShare로 변경했으며, 원래 출력은 새 출력의 하위 자식 속성이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1367">Changed output type from FileShareProperties to AzureStorageFileShare, the original output will become a sub child property of the new output</span></span>
    - <span data-ttu-id="76011-1368">'Set-AzStorageShareQuota'</span><span class="sxs-lookup"><span data-stu-id="76011-1368">'Set-AzStorageShareQuota'</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="76011-1369">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="76011-1369">Az.TrafficManager</span></span>
* <span data-ttu-id="76011-1370">'DisableAzureTrafficManagerEndpoint' 자세한 정보 출력에서 잘못된 프로필 이름 수정</span><span class="sxs-lookup"><span data-stu-id="76011-1370">Fixed incorrect profile name in 'DisableAzureTrafficManagerEndpoint' verbose output</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="76011-1371">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="76011-1371">Az.Websites</span></span>
* <span data-ttu-id="76011-1372">'Update-AzWebAppAccessRestrictionConfig'의 도움말에서 철자 오류 수정</span><span class="sxs-lookup"><span data-stu-id="76011-1372">Fixed typo on help of 'Update-AzWebAppAccessRestrictionConfig'.</span></span>

## <a name="380---april-2020"></a><span data-ttu-id="76011-1373">3.8.0 - 2020년 4월</span><span class="sxs-lookup"><span data-stu-id="76011-1373">3.8.0 - April 2020</span></span>
### <a name="highlights-since-the-last-release"></a><span data-ttu-id="76011-1374">마지막 릴리스 이후의 주요 사항</span><span class="sxs-lookup"><span data-stu-id="76011-1374">Highlights since the last release</span></span>
* <span data-ttu-id="76011-1375">Az.Storage에서 지원하는 PowerShell 버전: Windows PowerShell 5.1, PowerShell Core 6.2.4 이상, PowerShell 7</span><span class="sxs-lookup"><span data-stu-id="76011-1375">PowerShell versions that Az.Storage supports: Windows PowerShell 5.1, PowerShell Core 6.2.4+, PowerShell 7</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="76011-1376">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="76011-1376">Az.Accounts</span></span>
* <span data-ttu-id="76011-1377">'Resolve-AzError'에서 Azure PowerShell 설문 조사 URL이 업데이트되었습니다. [#11507]</span><span class="sxs-lookup"><span data-stu-id="76011-1377">Updated Azure PowerShell survey URL in 'Resolve-AzError' [#11507]</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="76011-1378">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="76011-1378">Az.ApiManagement</span></span>
* <span data-ttu-id="76011-1379">향후 릴리스의 Azure File cmdlet 출력 변경에 대한 호환성이 손상되는 변경 공지가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1379">Added breaking change notice for Azure File cmdlets output change in a future release</span></span>
* <span data-ttu-id="76011-1380">'Set-AzApiManagementGroup' - GroupId 매개 변수를 지정하도록 설명서가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1380">'Set-AzApiManagementGroup' Updated documentation to specify the GroupId parameter</span></span>

#### <a name="azcdn"></a><span data-ttu-id="76011-1381">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="76011-1381">Az.Cdn</span></span>
* <span data-ttu-id="76011-1382">ChinaCDN 관련 가격 책정 SKU 표시가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1382">Fixed ChinaCDN related pricing SKU display</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="76011-1383">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="76011-1383">Az.CognitiveServices</span></span>
* <span data-ttu-id="76011-1384">Identity, Encryption, UserOwnedStorage가 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1384">Supported Identity, Encryption, UserOwnedStorage</span></span>

#### <a name="azcompute"></a><span data-ttu-id="76011-1385">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="76011-1385">Az.Compute</span></span>
* <span data-ttu-id="76011-1386">'Set-AzVmssOrchestrationServiceState' cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1386">Added 'Set-AzVmssOrchestrationServiceState' cmdlet.</span></span>
* <span data-ttu-id="76011-1387">-InstanceView가 있는 'Get-AzVmss'는 OrchestrationService 상태를 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1387">'Get-AzVmss' with -InstanceView shows OrchestrationService states.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="76011-1388">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="76011-1388">Az.IotHub</span></span>
* <span data-ttu-id="76011-1389">IoT 디바이스 쌍 구성을 관리합니다. 새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1389">Manage IoT device twin configuration, New cmdlets are:</span></span>
    - <span data-ttu-id="76011-1390">'Get-AzIotHubDeviceTwin'</span><span class="sxs-lookup"><span data-stu-id="76011-1390">'Get-AzIotHubDeviceTwin'</span></span>
    - <span data-ttu-id="76011-1391">'Update-AzIotHubDeviceTwin'</span><span class="sxs-lookup"><span data-stu-id="76011-1391">'Update-AzIotHubDeviceTwin'</span></span>
* <span data-ttu-id="76011-1392">IoT Hub에서 디바이스에 대한 직접 메서드를 호출하는 cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1392">Added cmdlet to invoke direct method on a device in an Iot Hub.</span></span>
* <span data-ttu-id="76011-1393">IoT 디바이스 모듈 쌍 구성을 관리합니다. 새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1393">Manage IoT device module twin configuration, New cmdlets are:</span></span>
    - <span data-ttu-id="76011-1394">'Get-AzIotHubModuleTwin'</span><span class="sxs-lookup"><span data-stu-id="76011-1394">'Get-AzIotHubModuleTwin'</span></span>
    - <span data-ttu-id="76011-1395">'Update-AzIotHubModuleTwin'</span><span class="sxs-lookup"><span data-stu-id="76011-1395">'Update-AzIotHubModuleTwin'</span></span>
* <span data-ttu-id="76011-1396">IoT 자동 디바이스 관리 구성을 대규모로 관리합니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1396">Manage IoT automatic device management configuration at scale.</span></span> <span data-ttu-id="76011-1397">새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1397">New cmdlets are:</span></span>
    - <span data-ttu-id="76011-1398">'Add-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="76011-1398">'Add-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="76011-1399">'Get-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="76011-1399">'Get-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="76011-1400">'Remove-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="76011-1400">'Remove-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="76011-1401">'Set-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="76011-1401">'Set-AzIotHubConfiguration'</span></span>
* <span data-ttu-id="76011-1402">Iot Hub에서 에지 모듈 메서드를 호출하는 cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1402">Added cmdlet to invoke an edge module method in an Iot Hub.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="76011-1403">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="76011-1403">Az.KeyVault</span></span>
* <span data-ttu-id="76011-1404">자격 증명 모음에서 일시 삭제 및 제거 보호를 사용하도록 설정할 수 있는 새 cmdlet 'Update-AzKeyVault'가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1404">Added a new cmdlet 'Update-AzKeyVault' that can enable soft delete and purge protection on a vault</span></span>
* <span data-ttu-id="76011-1405">Microsoft.PowerShell.SecretManagement에 대한 지원이 추가되었습니다. [#11178]</span><span class="sxs-lookup"><span data-stu-id="76011-1405">Added support to Microsoft.PowerShell.SecretManagement [#11178]</span></span>
* <span data-ttu-id="76011-1406">'Remove-AzKeyVaultManagedStorageSasDefinition' 예제의 오류가 해결되었습니다. [#11479]</span><span class="sxs-lookup"><span data-stu-id="76011-1406">Fixed error in the examples of 'Remove-AzKeyVaultManagedStorageSasDefinition' [#11479]</span></span>
* <span data-ttu-id="76011-1407">프라이빗 엔드포인트에 대한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1407">Added support to private endpoint</span></span>

#### <a name="azmaintenance"></a><span data-ttu-id="76011-1408">Az.Maintenance</span><span class="sxs-lookup"><span data-stu-id="76011-1408">Az.Maintenance</span></span>
* <span data-ttu-id="76011-1409">GA용 유지 관리 cmdlet의 릴리스 버전 게시</span><span class="sxs-lookup"><span data-stu-id="76011-1409">Publishing release version of Maintenance cmdlets for GA</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="76011-1410">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="76011-1410">Az.Monitor</span></span>
* <span data-ttu-id="76011-1411">프라이빗 링크 범위용 cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1411">Added cmdlets for private link scope</span></span>
    - <span data-ttu-id="76011-1412">'Get-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="76011-1412">'Get-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="76011-1413">'Remove-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="76011-1413">'Remove-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="76011-1414">'New-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="76011-1414">'New-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="76011-1415">'Update-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="76011-1415">'Update-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="76011-1416">'Get-AzInsightsPrivateLinkScopedResource'</span><span class="sxs-lookup"><span data-stu-id="76011-1416">'Get-AzInsightsPrivateLinkScopedResource'</span></span>
    - <span data-ttu-id="76011-1417">'New-AzInsightsPrivateLinkScopedResource'</span><span class="sxs-lookup"><span data-stu-id="76011-1417">'New-AzInsightsPrivateLinkScopedResource'</span></span>
    - <span data-ttu-id="76011-1418">'Remove-AzInsightsPrivateLinkScopedResource'</span><span class="sxs-lookup"><span data-stu-id="76011-1418">'Remove-AzInsightsPrivateLinkScopedResource'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="76011-1419">Az.Network</span><span class="sxs-lookup"><span data-stu-id="76011-1419">Az.Network</span></span>
* <span data-ttu-id="76011-1420">Virtual Network 게이트웨이의 개인 IP에 대한 연결을 사용하도록 설정하는 cmdlet이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1420">Updated cmdlets to enable connection on private IP for Virtual Network Gateway.</span></span>
    - <span data-ttu-id="76011-1421">'New-AzVirtualNetworkGateway'</span><span class="sxs-lookup"><span data-stu-id="76011-1421">'New-AzVirtualNetworkGateway'</span></span>
    - <span data-ttu-id="76011-1422">'Set-AzVirtualNetworkGateway'</span><span class="sxs-lookup"><span data-stu-id="76011-1422">'Set-AzVirtualNetworkGateway'</span></span>
    - <span data-ttu-id="76011-1423">'New-AzVirtualNetworkGatewayConnection'</span><span class="sxs-lookup"><span data-stu-id="76011-1423">'New-AzVirtualNetworkGatewayConnection'</span></span>
    - <span data-ttu-id="76011-1424">'Set-AzVirtualNetworkGatewayConnection'</span><span class="sxs-lookup"><span data-stu-id="76011-1424">'Set-AzVirtualNetworkGatewayConnection'</span></span>
* <span data-ttu-id="76011-1425">FQDN 기반 LocalNetworkGateways 및 VpnSites를 사용하도록 설정하는 cmdlet이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1425">Updated cmdlets to enable FQDN based LocalNetworkGateways and VpnSites</span></span>
    - <span data-ttu-id="76011-1426">'New-AzLocalNetworkGateway'</span><span class="sxs-lookup"><span data-stu-id="76011-1426">'New-AzLocalNetworkGateway'</span></span>
    - <span data-ttu-id="76011-1427">'New-AzVpnSiteLink'</span><span class="sxs-lookup"><span data-stu-id="76011-1427">'New-AzVpnSiteLink'</span></span>
* <span data-ttu-id="76011-1428">ExpressRouteCircuitConnectionConfig(Global Reach)의 IPv6 주소 패밀리에 대한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1428">Added support for IPv6 address family in ExpressRouteCircuitConnectionConfig (Global Reach)</span></span>
    - <span data-ttu-id="76011-1429">'Set-AzExpressRouteCircuitConnectionConfig'가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1429">Added 'Set-AzExpressRouteCircuitConnectionConfig'</span></span>
        - <span data-ttu-id="76011-1430">IPv6CircuitConnectionProperties를 포함한 모든 기존 속성을 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1430">allows setting of all the existing properties including the IPv6CircuitConnectionProperties</span></span>
    - <span data-ttu-id="76011-1431">'Add-AzExpressRouteCircuitConnectionConfig'가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1431">Updated 'Add-AzExpressRouteCircuitConnectionConfig'</span></span>
        - <span data-ttu-id="76011-1432">주소 접두사의 주소 패밀리를 지정하는 또 다른 선택적 매개 변수 AddressPrefixType이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1432">Added another optional parameter AddressPrefixType to specify the address family of address prefix</span></span>
* <span data-ttu-id="76011-1433">Virtual Network 게이트웨이 연결에서 DPD 시간 제한 설정을 사용하도록 cmdlet이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1433">Updated cmdlets to enable setting of DPD Timeout on Virtual Network Gateway Connections.</span></span>
    - <span data-ttu-id="76011-1434">New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="76011-1434">New-AzVirtualNetworkGatewayConnection</span></span>
    - <span data-ttu-id="76011-1435">Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="76011-1435">Set-AzVirtualNetworkGatewayConnection</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="76011-1436">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="76011-1436">Az.PolicyInsights</span></span>
* <span data-ttu-id="76011-1437">정책 준수 검사를 트리거하기 위한 'Start-AzPolicyComplianceScan' cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1437">Added 'Start-AzPolicyComplianceScan' cmdlet for triggering policy compliance scans</span></span>
* <span data-ttu-id="76011-1438">'Get-AzPolicyState' 출력에 정책 정의, 집합 정의 및 할당 버전이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1438">Added policy definition, set definition, and assignment versions to 'Get-AzPolicyState' output</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="76011-1439">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="76011-1439">Az.ServiceFabric</span></span>
* <span data-ttu-id="76011-1440">'New-AzServiceFabricCluster' 예제의 코드 서식 및 사용 편의성이 개선되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1440">Improved code formatting and usability of 'New-AzServiceFabricCluster' examples</span></span>

#### <a name="azsql"></a><span data-ttu-id="76011-1441">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="76011-1441">Az.Sql</span></span>
* <span data-ttu-id="76011-1442">'Get-AzSqlInstanceOperation' 및 'Stop-AzSqlInstanceOperation' cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1442">Added cmdlets 'Get-AzSqlInstanceOperation' and 'Stop-AzSqlInstanceOperation'</span></span>
* <span data-ttu-id="76011-1443">VNet에서 스토리지 계정에 대한 감사가 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1443">Supported auditing to a storage account in VNet.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="76011-1444">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="76011-1444">Az.Storage</span></span>
* <span data-ttu-id="76011-1445">향후 릴리스의 Azure File cmdlet 출력 변경에 대한 호환성이 손상되는 변경 공지가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1445">Added breaking change notice for Azure File cmdlets output change in a future release</span></span>
* <span data-ttu-id="76011-1446">스토리지 계정 생성/업데이트 시 새로운 SkuName StandardGZRS, StandardRAGZRS가 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1446">Supported new SkuName StandardGZRS, StandardRAGZRS when create/update Storage account</span></span>
    - <span data-ttu-id="76011-1447">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="76011-1447">'New-AzStorageAccount'</span></span>
    - <span data-ttu-id="76011-1448">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="76011-1448">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="76011-1449">DataLake Gen2가 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1449">Supported DataLake Gen2</span></span>
    - <span data-ttu-id="76011-1450">'New-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="76011-1450">'New-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="76011-1451">'Get-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="76011-1451">'Get-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="76011-1452">'Get-AzDataLakeGen2ChildItem'</span><span class="sxs-lookup"><span data-stu-id="76011-1452">'Get-AzDataLakeGen2ChildItem'</span></span>
    - <span data-ttu-id="76011-1453">'Move-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="76011-1453">'Move-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="76011-1454">'Set-AzDataLakeGen2ItemAclObject'</span><span class="sxs-lookup"><span data-stu-id="76011-1454">'Set-AzDataLakeGen2ItemAclObject'</span></span>
    - <span data-ttu-id="76011-1455">'Update-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="76011-1455">'Update-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="76011-1456">'Get-AzDataLakeGen2ItemContent'</span><span class="sxs-lookup"><span data-stu-id="76011-1456">'Get-AzDataLakeGen2ItemContent'</span></span>
    - <span data-ttu-id="76011-1457">'Remove-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="76011-1457">'Remove-AzDataLakeGen2Item'</span></span>

## <a name="0100-preview---april-2020"></a><span data-ttu-id="76011-1458">0.10.0-preview - 2020년 4월</span><span class="sxs-lookup"><span data-stu-id="76011-1458">0.10.0-preview - April 2020</span></span>
### <a name="general"></a><span data-ttu-id="76011-1459">일반</span><span class="sxs-lookup"><span data-stu-id="76011-1459">General</span></span>
* <span data-ttu-id="76011-1460">이제 Az 모듈이 Azure Stack Hub에서 미리 보기로 제공됩니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1460">Az modules is now available in preview on Azure Stack Hub.</span></span> <span data-ttu-id="76011-1461">따라서 Linux 및 macOS와의 플랫폼 간 호환성이 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1461">This allows for cross-platform compatibility with Linux and macOs.</span></span> <span data-ttu-id="76011-1462">Azure Stack Hub는 이제 Az 모듈을 사용하여 PowerShell Core를 지원합니다. 자세한 내용은 [여기](/azure-stack/operator/powershell-install-az-module)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="76011-1462">Azure Stack Hub now supports PowerShell core with the Az modules, more information [here](/azure-stack/operator/powershell-install-az-module)</span></span>
* <span data-ttu-id="76011-1463">Az 모듈은 2019-03-01-hybrid 프로필을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1463">Az modules support profile 2019-03-01-hybrid:</span></span>
  - <span data-ttu-id="76011-1464">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="76011-1464">Az.Billing</span></span>
  - <span data-ttu-id="76011-1465">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="76011-1465">Az.Compute</span></span>
  - <span data-ttu-id="76011-1466">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="76011-1466">Az.DataBoxEdge</span></span>
  - <span data-ttu-id="76011-1467">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="76011-1467">Az.EventHub</span></span>
  - <span data-ttu-id="76011-1468">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="76011-1468">Az.IotHub</span></span>
  - <span data-ttu-id="76011-1469">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="76011-1469">Az.KeyVault</span></span>
  - <span data-ttu-id="76011-1470">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="76011-1470">Az.Monitor</span></span>
  - <span data-ttu-id="76011-1471">Az.Network</span><span class="sxs-lookup"><span data-stu-id="76011-1471">Az.Network</span></span>
  - <span data-ttu-id="76011-1472">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="76011-1472">Az.Resources</span></span>
  - <span data-ttu-id="76011-1473">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="76011-1473">Az.Storage</span></span>
  - <span data-ttu-id="76011-1474">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="76011-1474">Az.Websites</span></span>
* <span data-ttu-id="76011-1475">Azure Stack Hub와 함께 작동하는 az용 새 PowerShell 모듈 3개(Az.Databox, Az.IotHub 및 Az.EventHub)가 도입되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1475">Three new PowerShell modules for az have been introduced that work with Azure Stack Hub, which are Az.Databox, Az.IotHub, and Az.EventHub</span></span>
* <span data-ttu-id="76011-1476">AzureRM을 Az로 변경하는 것과 같은 사소한 변경을 수행하면 명령이 비교적 동일하게 유지됩니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1476">Commands remain relatively the same, with minor changes such as changing AzureRM to Az</span></span>
* <span data-ttu-id="76011-1477">Azure Stack Hub에 대한 PowerShell 설명서의 업데이트된 링크는 [여기](/azure-stack/operator/powershell-install-az-module)에서 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1477">Updated link to PowerShell documentation for Azure Stack Hub can be found [here](/azure-stack/operator/powershell-install-az-module)</span></span>

## <a name="370---march-2020"></a><span data-ttu-id="76011-1478">3.7.0 - 2020년 3월</span><span class="sxs-lookup"><span data-stu-id="76011-1478">3.7.0 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="76011-1479">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="76011-1479">Az.Accounts</span></span>
* <span data-ttu-id="76011-1480">로그인하지 않을 때 'Get-AzTenant'/'Get-AzDefault'/'Set-AzDefault'에서 NullReferenceException이 발생하는 문제가 해결되었습니다. [# 10292]</span><span class="sxs-lookup"><span data-stu-id="76011-1480">Fixed 'Get-AzTenant'/'Get-AzDefault'/'Set-AzDefault' throw NullReferenceException when not login [#10292]</span></span>

#### <a name="azcompute"></a><span data-ttu-id="76011-1481">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="76011-1481">Az.Compute</span></span>
* <span data-ttu-id="76011-1482">'New-AzDiskConfig' cmdlet에 다음 매개 변수를 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1482">Added the following parameters to 'New-AzDiskConfig' cmdlet:</span></span>
    - <span data-ttu-id="76011-1483">DiskIOPSReadOnly, DiskMBpsReadOnly, MaxSharesCount, GalleryImageReference</span><span class="sxs-lookup"><span data-stu-id="76011-1483">DiskIOPSReadOnly, DiskMBpsReadOnly, MaxSharesCount, GalleryImageReference</span></span>
* <span data-ttu-id="76011-1484">암호화 속성이 'New-AzGalleryImageVersion'cmdlet의 대상 매개 변수에 허용되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1484">Allowed Encryption property to Target parameter of 'New-AzGalleryImageVersion' cmdlet.</span></span>
* <span data-ttu-id="76011-1485">'Set-AzVmss'-Reimage 및 'Invoke-AzVMReimage'cmdlet에 대한 tempDisk 이슈가 해결되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1485">Fixed tempDisk issue for 'Set-AzVmss' -Reimage and 'Invoke-AzVMReimage' cmdlets.</span></span> <span data-ttu-id="76011-1486">[#11354]</span><span class="sxs-lookup"><span data-stu-id="76011-1486">[#11354]</span></span>
* <span data-ttu-id="76011-1487">새로운 SAP 확장을 위해 아래 cmdlet에 대한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1487">Added support to below cmdlets for new SAP Extension</span></span>
    - <span data-ttu-id="76011-1488">'Set-AzVMAEMExtension'</span><span class="sxs-lookup"><span data-stu-id="76011-1488">'Set-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="76011-1489">'Get-AzVMAEMExtension'</span><span class="sxs-lookup"><span data-stu-id="76011-1489">'Get-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="76011-1490">'Remove-AzVMAEMExtension'</span><span class="sxs-lookup"><span data-stu-id="76011-1490">'Remove-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="76011-1491">'Update-AzVMAEMExtension'</span><span class="sxs-lookup"><span data-stu-id="76011-1491">'Update-AzVMAEMExtension'</span></span>
* <span data-ttu-id="76011-1492">도움말 문서의 예제에서 오류가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1492">Fixed errors in examples of help document</span></span>
* <span data-ttu-id="76011-1493">VM PowerState의 정확한 문자열 값을 테이블 형식으로 표시했습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1493">Showed the exact string value for VM PowerState in the table format.</span></span>
* <span data-ttu-id="76011-1494">'New-AzVmssConfig': SinglePlacementGroup이 비활성화된 경우 AutomaticRepairs 속성의 직렬화가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1494">'New-AzVmssConfig': fixed serialization of AutomaticRepairs property when SinglePlacementGroup is disabled.</span></span> <span data-ttu-id="76011-1495">[#11257]</span><span class="sxs-lookup"><span data-stu-id="76011-1495">[#11257]</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="76011-1496">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="76011-1496">Az.DataFactory</span></span>
* <span data-ttu-id="76011-1497">ADF .Net SDK 버전이 4.8.0으로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1497">Updated ADF .Net SDK version to 4.8.0</span></span>
* <span data-ttu-id="76011-1498">재실행을 지원하기 위해 'Invoke-AzDataFactoryV2Pipeline' 명령에 선택적 매개 변수를 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1498">Added optional parameters to 'Invoke-AzDataFactoryV2Pipeline' command to support rerun</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="76011-1499">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="76011-1499">Az.DataLakeStore</span></span>
* <span data-ttu-id="76011-1500">'Export-AzDataLakeStoreItem' 및 'Import-AzDataLakeStoreItem'에 대해 호환성이 손상되는 변경 설명을 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1500">Added breaking change description for 'Export-AzDataLakeStoreItem' and 'Import-AzDataLakeStoreItem'</span></span>
* <span data-ttu-id="76011-1501">'New-AzDataLakeStoreItem', 'Add-AzDAtaLakeStoreItemContent' 및 'Get-AzDAtaLakeStoreItemContent'에 대한 바이트 인코딩 옵션이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1501">Added option of Byte encoding for 'New-AzDataLakeStoreItem', 'Add-AzDAtaLakeStoreItemContent', and 'Get-AzDAtaLakeStoreItemContent'</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="76011-1502">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="76011-1502">Az.HDInsight</span></span>
* <span data-ttu-id="76011-1503">클러스터 생성 시 최소 지원 TLS 버전 지정이 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1503">Supported specifying minimal supported TLS version when creating cluster.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="76011-1504">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="76011-1504">Az.IotHub</span></span>
* <span data-ttu-id="76011-1505">디바이스별 분산 설정을 관리하기 위한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1505">Added support to manage distributed settings per-device.</span></span> <span data-ttu-id="76011-1506">새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1506">New Cmdlets are:</span></span>
    - <span data-ttu-id="76011-1507">'Get-AzIotHubDistributedTracing'</span><span class="sxs-lookup"><span data-stu-id="76011-1507">'Get-AzIotHubDistributedTracing'</span></span>
    - <span data-ttu-id="76011-1508">'Set-AzIotHubDistributedTracing'</span><span class="sxs-lookup"><span data-stu-id="76011-1508">'Set-AzIotHubDistributedTracing'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="76011-1509">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="76011-1509">Az.KeyVault</span></span>
* <span data-ttu-id="76011-1510">'New-AzKeyVault'에 대해 호환성이 손상되는 변경 속성이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1510">Added breaking change attributes to 'New-AzKeyVault'</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="76011-1511">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="76011-1511">Az.Monitor</span></span>
* <span data-ttu-id="76011-1512">'New-AzScheduledQueryRuleLogMetricTrigger'에 대한 설명서가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1512">Updated documentation for 'New-AzScheduledQueryRuleLogMetricTrigger'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="76011-1513">Az.Network</span><span class="sxs-lookup"><span data-stu-id="76011-1513">Az.Network</span></span>
* <span data-ttu-id="76011-1514">교차 테넌트 VirtualHubVnetConnections를 허용하도록 cmdlet이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1514">Updated cmdlets to allow cross-tenant VirtualHubVnetConnections</span></span>
    - <span data-ttu-id="76011-1515">'New-AzVirtualHubVnetConnection'</span><span class="sxs-lookup"><span data-stu-id="76011-1515">'New-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="76011-1516">'Update-AzVirtualHubVnetConnection'</span><span class="sxs-lookup"><span data-stu-id="76011-1516">'Update-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="76011-1517">'New-AzVirtualHub'</span><span class="sxs-lookup"><span data-stu-id="76011-1517">'New-AzVirtualHub'</span></span>
    - <span data-ttu-id="76011-1518">'Update-AzVirtualHub'</span><span class="sxs-lookup"><span data-stu-id="76011-1518">'Update-AzVirtualHub'</span></span>
* <span data-ttu-id="76011-1519">SQL Management SDK 종속성이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1519">Removed Sql Management SDK dependency</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="76011-1520">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="76011-1520">Az.PolicyInsights</span></span>
* <span data-ttu-id="76011-1521">오류 메시지가 향상되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1521">Improved error messages</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="76011-1522">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="76011-1522">Az.RecoveryServices</span></span>
* <span data-ttu-id="76011-1523">Azure Site Recovery는 Azure 디스크 암호화 Virtual Machines에 대한 VM 속성을 다시 보호하고 업데이트하는 기능을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1523">Azure Site Recovery added support for doing reprotect and updated vm properties for Azure disk encrypted Virtual Machines.</span></span>
* <span data-ttu-id="76011-1524">Azure Site Recovery VmwareToAzure 속성 DR 모니터링이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1524">Added Azure Site Recovery VmwareToAzure properties DR monitoring</span></span>
* <span data-ttu-id="76011-1525">Azure Backup은 실패한 항목에 대한 정책 업데이트 재시도 지원을 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1525">Azure Backup added support for retrying policy update for failed items.</span></span>
* <span data-ttu-id="76011-1526">Azure Backup은 백업 및 복원 중에 디스크 제외 설정에 대한 지원을 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1526">Azure Backup Added support for disk exclusion settings during backup and restore.</span></span>
* <span data-ttu-id="76011-1527">Azure Backup은 AzureFileShare에서 여러 파일/폴더 복원을 위한 지원을 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1527">Azure Backup Added Support for Restoring Multiple files/folders in AzureFileShare</span></span>
* <span data-ttu-id="76011-1528">Azure Backup은 IaasVM 정책을 업데이트하는 동안 사용자 지정 리소스 그룹 지원에 대한 지원을 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1528">Azure Backup Added support for User-specified Resourcegroup support while updating IaasVM Policy</span></span>

#### <a name="azresources"></a><span data-ttu-id="76011-1529">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="76011-1529">Az.Resources</span></span>
* <span data-ttu-id="76011-1530">'Get-AzResource -ResourceGroupName -Name -ExpandProperties -ResourceType'이 기본 apiVersion 대신 실제 apiVersion 리소스를 사용하도록 수정했습니다. [# 11267]</span><span class="sxs-lookup"><span data-stu-id="76011-1530">Fixed 'Get-AzResource -ResourceGroupName -Name -ExpandProperties -ResourceType' to use actual apiVersion of resources instead of default apiVersion [#11267]</span></span>
* <span data-ttu-id="76011-1531">오류 시나리오에 대해 correlationId 로깅이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1531">Added correlationId logging for error scenarios</span></span>
* <span data-ttu-id="76011-1532">작은 설명서가 'Get-AzResourceLock'으로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1532">Small documentation change to 'Get-AzResourceLock'.</span></span> <span data-ttu-id="76011-1533">예제가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1533">Added example.</span></span>
* <span data-ttu-id="76011-1534">'Get-AzADUser'의 매개 변수 값에서 작은 따옴표를 이스케이프 처리하였습니다. [# 11317]</span><span class="sxs-lookup"><span data-stu-id="76011-1534">Escaped single quote in parameter value of 'Get-AzADUser' [#11317]</span></span>
* <span data-ttu-id="76011-1535">배포 스크립트('Get-AzDeploymentScript', 'Get-AzDeploymentScriptLog', 'Save-AzDeploymentScriptLog', 'Remove-AzDeploymentScript')에 대한 새로운 cmdlet 추가가 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1535">Added new cmdlets for Deployment Scripts ('Get-AzDeploymentScript', 'Get-AzDeploymentScriptLog', 'Save-AzDeploymentScriptLog', 'Remove-AzDeploymentScript')</span></span>

#### <a name="azsql"></a><span data-ttu-id="76011-1536">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="76011-1536">Az.Sql</span></span>
* <span data-ttu-id="76011-1537">'Invoke-AzSqlDatabaseFailover'에 읽기 가능한 보조 매개 변수를 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1537">Added readable secondary parameter to 'Invoke-AzSqlDatabaseFailover'</span></span>
* <span data-ttu-id="76011-1538">'Disable-AzSqlServerActiveDirectoryOnlyAuthentication' cmdlet을 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1538">Added cmdlet 'Disable-AzSqlServerActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="76011-1539">데이터베이스에서 열을 분류할 때 저장된 민감도 순위입니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1539">Saved sensitivity rank when classifying columns in the database.</span></span>

#### <a name="azsupport"></a><span data-ttu-id="76011-1540">Az.Support</span><span class="sxs-lookup"><span data-stu-id="76011-1540">Az.Support</span></span>
* <span data-ttu-id="76011-1541">'Az.Support' 모듈의 일반 공급</span><span class="sxs-lookup"><span data-stu-id="76011-1541">General availability of 'Az.Support' module</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="76011-1542">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="76011-1542">Az.Websites</span></span>
* <span data-ttu-id="76011-1543">아래의 새로운 cmdlet을 통해 webapp 트래픽 라우팅 규칙을 사용하는 작업에 대한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1543">Added support for working with webapp Traffic Routing Rules via below new cmdlets</span></span>
    - <span data-ttu-id="76011-1544">'Get-AzWebAppTrafficRouting'</span><span class="sxs-lookup"><span data-stu-id="76011-1544">'Get-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="76011-1545">'Update-AzWebAppTrafficRouting'</span><span class="sxs-lookup"><span data-stu-id="76011-1545">'Update-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="76011-1546">'Add-AzWebAppTrafficRouting'</span><span class="sxs-lookup"><span data-stu-id="76011-1546">'Add-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="76011-1547">'Remove-AzWebAppTrafficRouting'</span><span class="sxs-lookup"><span data-stu-id="76011-1547">'Remove-AzWebAppTrafficRouting'</span></span>

## <a name="361---march-2020"></a><span data-ttu-id="76011-1548">3.6.1 - 2020년 3월</span><span class="sxs-lookup"><span data-stu-id="76011-1548">3.6.1 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="76011-1549">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="76011-1549">Az.Accounts</span></span>
* <span data-ttu-id="76011-1550">'피드백 보내기'에서 Azure PowerShell 설문 조사 페이지가 열립니다[#11020].</span><span class="sxs-lookup"><span data-stu-id="76011-1550">Open Azure PowerShell survey page in 'Send-Feedback' [#11020]</span></span>
* <span data-ttu-id="76011-1551">'오류 해결'에서 Azure PowerShell 설문 조사 URL이 표시됩니다[#11021].</span><span class="sxs-lookup"><span data-stu-id="76011-1551">Display Azure PowerShell survey URL in 'Resolve-Error' [#11021]</span></span>
* <span data-ttu-id="76011-1552">UserAgent에서 Az 버전이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1552">Added Az version in UserAgent</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="76011-1553">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="76011-1553">Az.ApiManagement</span></span>
* <span data-ttu-id="76011-1554">DeveloperPortal 엔드포인트에서 사용자 지정 도메인을 검색하고 구성하기 위한 지원이 추가되었습니다[#11007].</span><span class="sxs-lookup"><span data-stu-id="76011-1554">Added support for retrieving and configuring Custom Domain on the DeveloperPortal Endpoint [#11007]</span></span>
* <span data-ttu-id="76011-1555">Json 형식의 API 정의를 다운로드하기 위한 'Export-AzApiManagementApi' 지원이 추가되었습니다[#9987].</span><span class="sxs-lookup"><span data-stu-id="76011-1555">'Export-AzApiManagementApi' Added support for downloading Api Definition in Json format [#9987]</span></span>
* <span data-ttu-id="76011-1556">Json 문서에서 OpenApi 3.0 정의를 가져오기 위한 'Import-AzApiManagementApi' 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1556">'Import-AzApiManagementApi' Added support for importing OpenApi 3.0 definition from Json document</span></span>
* <span data-ttu-id="76011-1557">AAD B2C 공급자에 대한 '로그인 테넌트'를 구성하기 위한 'New-AzApiManagementIdentityProvider' 및 'Set-AzApiManagementIdentityProvider' 지원이 추가되었습니다[#9784].</span><span class="sxs-lookup"><span data-stu-id="76011-1557">'New-AzApiManagementIdentityProvider' and 'Set-AzApiManagementIdentityProvider' Added support for configuring 'Signin Tenant' for AAD B2C Provider [#9784]</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="76011-1558">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="76011-1558">Az.DataLakeStore</span></span>
* <span data-ttu-id="76011-1559">csproj 및 psd1에서 System.Buffers에 대한 참조가 명시적으로 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1559">Added reference to System.Buffers explicitly in csproj and psd1.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="76011-1560">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="76011-1560">Az.IotHub</span></span>
* <span data-ttu-id="76011-1561">Iot Hub에서 디바이스를 관리하기 위한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1561">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="76011-1562">새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1562">New Cmdlets are:</span></span>
    - <span data-ttu-id="76011-1563">'Add-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="76011-1563">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="76011-1564">'Get-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="76011-1564">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="76011-1565">'Remove-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="76011-1565">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="76011-1566">'Set-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="76011-1566">'Set-AzIotHubDevice'</span></span>
* <span data-ttu-id="76011-1567">Iot Hub의 대상 IoT 디바이스에서 모듈을 관리하기 위한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1567">Added support to manage modules on a target Iot device in an Iot Hub.</span></span> <span data-ttu-id="76011-1568">새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1568">New Cmdlets are:</span></span>
    - <span data-ttu-id="76011-1569">'Add-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="76011-1569">'Add-AzIotHubModule'</span></span>
    - <span data-ttu-id="76011-1570">'Get-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="76011-1570">'Get-AzIotHubModule'</span></span>
    - <span data-ttu-id="76011-1571">'Remove-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="76011-1571">'Remove-AzIotHubModule'</span></span>
    - <span data-ttu-id="76011-1572">'Set-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="76011-1572">'Set-AzIotHubModule'</span></span>
* <span data-ttu-id="76011-1573">Iot Hub에서 대상 IoT 디바이스에 대한 연결 문자열을 가져오는 cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1573">Added cmdlet to get the connection string of a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="76011-1574">Iot Hub에서 대상 IoT 디바이스의 모듈에 대한 연결 문자열을 가져오는 cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1574">Added cmdlet to get the connection string of a module on a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="76011-1575">IoT 디바이스의 부모 디바이스를 가져오거나 설정하기 위한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1575">Added support to get/set parent device of an IoT device.</span></span> <span data-ttu-id="76011-1576">새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1576">New Cmdlets are:</span></span>
    - <span data-ttu-id="76011-1577">'Get-AzIotHubDeviceParent'</span><span class="sxs-lookup"><span data-stu-id="76011-1577">'Get-AzIotHubDeviceParent'</span></span>
    - <span data-ttu-id="76011-1578">'Set-AzIotHubDeviceParent'</span><span class="sxs-lookup"><span data-stu-id="76011-1578">'Set-AzIotHubDeviceParent'</span></span>
* <span data-ttu-id="76011-1579">디바이스 부모-자식 관계를 관리하기 위한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1579">Added support to manage device parent-child relationship.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="76011-1580">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="76011-1580">Az.Monitor</span></span>
* <span data-ttu-id="76011-1581">'Get-AzMetricDefinition'에 대한 출력 값이 수정되었습니다[#9714].</span><span class="sxs-lookup"><span data-stu-id="76011-1581">Fixed output value for 'Get-AzMetricDefinition' [#9714]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="76011-1582">Az.Network</span><span class="sxs-lookup"><span data-stu-id="76011-1582">Az.Network</span></span>
* <span data-ttu-id="76011-1583">SQL Management SDK가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1583">Updated Sql Management SDK.</span></span>
* <span data-ttu-id="76011-1584">PrivateLinkServiceConnectionState 클래스의 명명 차이 문제가 해결되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1584">Fixed a naming-difference issue in PrivateLinkServiceConnectionState class.</span></span>
    - <span data-ttu-id="76011-1585">ActionsRequired 필드가 ActionRequired에 매핑됩니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1585">Mapping the field ActionsRequired to ActionRequired.</span></span>
* <span data-ttu-id="76011-1586">PublicNetworkAccess가 'New-AzSqlServer' 및 'Set-AzSqlServer'에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1586">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>

#### <a name="azresources"></a><span data-ttu-id="76011-1587">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="76011-1587">Az.Resources</span></span>
* <span data-ttu-id="76011-1588">Get-AzRoleAssignment'의 null 참조 버그가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1588">Fixed for null reference bug in 'Get-AzRoleAssignment'</span></span>
* <span data-ttu-id="76011-1589">'Remove-AzADGroup'에서 '-Force' 및 '-PassThru' 스위치가 선택적으로 표시됩니다[#10849].</span><span class="sxs-lookup"><span data-stu-id="76011-1589">Marked switch '-Force' and '-PassThru' optional in 'Remove-AzADGroup' [#10849]</span></span>
* <span data-ttu-id="76011-1590">'Remove-AzADGroup'에서 'MailNickname'이 반환되지 않는 문제가 해결되었습니다[#11167].</span><span class="sxs-lookup"><span data-stu-id="76011-1590">Fixed issue that 'MailNickname' doesn't return in 'Remove-AzADGroup' [#11167]</span></span>
* <span data-ttu-id="76011-1591">'Remove-AzADGroup' 파이프 작업이 작동하지 않는 문제가 해결되었습니다[#11171].</span><span class="sxs-lookup"><span data-stu-id="76011-1591">Fixed issue that 'Remove-AzADGroup' pipe operation doesn't work [#11171]</span></span>
* <span data-ttu-id="76011-1592">GetAzureRoleAssignmentCommand의 null 참조 버그가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1592">Fixed for null reference bug in GetAzureRoleAssignmentCommand</span></span>
* <span data-ttu-id="76011-1593">예정된 정책 cmdlet 변경에 대한 호환성이 손상되는 변경 특성이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1593">Added breaking change attributes for upcoming changes to policy cmdlets</span></span>
* <span data-ttu-id="76011-1594">서버 쪽에서 리소스 그룹 태그 필터링을 수행하도록 'Get-AzResourceGroup'이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1594">Updated 'Get-AzResourceGroup' to perform resource group tag filtering on server-side</span></span>
* <span data-ttu-id="76011-1595">-ResourceId를 허용하도록 Tag cmdlet이 확장되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1595">Extended Tag cmdlets to accept -ResourceId</span></span>
    - <span data-ttu-id="76011-1596">Get-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="76011-1596">Get-AzTag -ResourceId</span></span>
    - <span data-ttu-id="76011-1597">New-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="76011-1597">New-AzTag -ResourceId</span></span>
    - <span data-ttu-id="76011-1598">Remove-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="76011-1598">Remove-AzTag -ResourceId</span></span>
* <span data-ttu-id="76011-1599">새 Tag cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1599">Added new Tag cmdlet</span></span>
    - <span data-ttu-id="76011-1600">Update-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="76011-1600">Update-AzTag -ResourceId</span></span>
* <span data-ttu-id="76011-1601">SDK 3.3.0에서 ScopedDeployment를 가져왔습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1601">Brought ScopedDeployment from SDK 3.3.0</span></span>

#### <a name="azsql"></a><span data-ttu-id="76011-1602">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="76011-1602">Az.Sql</span></span>
* <span data-ttu-id="76011-1603">PublicNetworkAccess가 'New-AzSqlServer' 및 'Set-AzSqlServer'에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1603">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>
* <span data-ttu-id="76011-1604">관리형 데이터베이스에 대한 장기 보존 백업 구성에 대한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1604">Added support for Long Term Retention backup configuration for Managed Databases</span></span>
    - <span data-ttu-id="76011-1605">관리형 데이터베이스에서 LTR 정책을 가져오거나 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1605">Get/Set LTR policy on a managed database</span></span>
    - <span data-ttu-id="76011-1606">관리형 데이터베이스, 관리형 인스턴스 또는 위치를 기준으로 LTR 백업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1606">Get LTR backup(s) by managed database, managed instance, or by location</span></span>
    - <span data-ttu-id="76011-1607">LTR 백업을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1607">Remove an LTR backup</span></span>
    - <span data-ttu-id="76011-1608">LTR 백업을 복원하여 새 관리형 데이터베이스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1608">Restore an LTR backup to create a new managed database</span></span>
* <span data-ttu-id="76011-1609">MinimalTlsVersion이 New-AzSqlServer 및 Set-AzSqlServer에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1609">Added MinimalTlsVersion to New-AzSqlServer and Set-AzSqlServer</span></span>
* <span data-ttu-id="76011-1610">MinimalTlsVersion을 New-AzSqlInstance 및 Set-AzSqlInstance에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1610">Added MinimalTlsVersion to New-AzSqlInstance and Set-AzSqlInstance</span></span>
* <span data-ttu-id="76011-1611">Az.Network에 대한 SQL SDK 버전이 높아졌습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1611">Bumped SQL SDK version for Az.Network</span></span>

#### <a name="azstorage"></a><span data-ttu-id="76011-1612">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="76011-1612">Az.Storage</span></span>
* <span data-ttu-id="76011-1613">ImmutabilityPolicy에서 AllowProtectedAppendWrite가 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1613">Supported AllowProtectedAppendWrite in ImmutabilityPolicy</span></span>
    - <span data-ttu-id="76011-1614">'Set-AzRmStorageContainerImmutabilityPolicy'</span><span class="sxs-lookup"><span data-stu-id="76011-1614">'Set-AzRmStorageContainerImmutabilityPolicy'</span></span>
* <span data-ttu-id="76011-1615">이후 릴리스에서 AzureStorageTable 형식 변경에 대한 호환성이 손상되는 변경 경고 메시지가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1615">Added breaking change warning message for AzureStorageTable type change in a future release</span></span>
    - <span data-ttu-id="76011-1616">'New-AzStorageTable'</span><span class="sxs-lookup"><span data-stu-id="76011-1616">'New-AzStorageTable'</span></span>
    - <span data-ttu-id="76011-1617">'Get-AzStorageTable'</span><span class="sxs-lookup"><span data-stu-id="76011-1617">'Get-AzStorageTable'</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="76011-1618">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="76011-1618">Az.Websites</span></span>
* <span data-ttu-id="76011-1619">'New-AzAppServicePlan' 및 'Set-AzAppServicePlan'에 대한 Tag 매개 변수가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1619">Added Tag parameter for 'New-AzAppServicePlan' and 'Set-AzAppServicePlan'</span></span>
* <span data-ttu-id="76011-1620">웹 사이트에 사용자 지정 도메인을 추가할 때 예외가 throw되면 cmdlet 실행을 중지합니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1620">Stop cmdlet execution if an exception is thrown when adding a custom domain to a website</span></span>
* <span data-ttu-id="76011-1621">App Service 계획과 동일한 리소스 그룹에 속하지 않는 App Services에 대한 작업을 수행하기 위한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1621">Added support to perform operations for App Services not in the same resource group as the App Service Plan</span></span>
* <span data-ttu-id="76011-1622">다른 리소스 그룹의 WebApp/Function에 대한 액세스 제한이 적용되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1622">Applied access restriction to WebApp/Function in different resource groups</span></span>
* <span data-ttu-id="76011-1623">WebAppSlot에 대한 사용자 지정 호스트 이름을 설정하는 문제가 해결되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1623">Fixed issue to set custom hostnames for WebAppSlots</span></span>

## <a name="350---february-2020"></a><span data-ttu-id="76011-1624">3.5.0 - 2020년 2월</span><span class="sxs-lookup"><span data-stu-id="76011-1624">3.5.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="76011-1625">마지막 주 릴리스 이후의 주요 사항</span><span class="sxs-lookup"><span data-stu-id="76011-1625">Highlights since the last major release</span></span>
* <span data-ttu-id="76011-1626">클라이언트 쪽 원격 분석이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1626">Updated client side telemetry.</span></span>
* <span data-ttu-id="76011-1627">디바이스 관리를 지원하는 cmdlet이 Az.IotHub에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1627">Az.IotHub added cmdlets to support to manage devices.</span></span>
* <span data-ttu-id="76011-1628">가용성 그룹 수신기에 대한 cmdlet이 Az.SqlVirtualMachine에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1628">Az.SqlVirtualMachine added cmdlets for Availability Group Listener.</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="76011-1629">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="76011-1629">Az.Accounts</span></span>
* <span data-ttu-id="76011-1630">SubscriptionId, TenantId 및 실행 시간이 클라이언트 쪽 원격 분석에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1630">Added SubscriptionId, TenantId, and execution time into data of client side telemetry</span></span>

#### <a name="azautomation"></a><span data-ttu-id="76011-1631">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="76011-1631">Az.Automation</span></span>
* <span data-ttu-id="76011-1632">'New-AzAutomationSoftwareUpdateConfiguration' 참조 설명서의 예제 1에 있는 오타가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1632">Fixed typo in Example 1 in reference documentation for 'New-AzAutomationSoftwareUpdateConfiguration'</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="76011-1633">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="76011-1633">Az.CognitiveServices</span></span>
* <span data-ttu-id="76011-1634">SDK가 7.0으로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1634">Updated SDK to 7.0</span></span>
* <span data-ttu-id="76011-1635">서버 응답 본문이 비어 있는 경우 표시되는 오류 메시지가 향상되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1635">Improved error message when server responses empty body</span></span>

#### <a name="azcompute"></a><span data-ttu-id="76011-1636">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="76011-1636">Az.Compute</span></span>
* <span data-ttu-id="76011-1637">업데이트하는 동안 빈 값이 ProximityPlacementGroupId에 허용되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1637">Allowed empty value for ProximityPlacementGroupId during update</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="76011-1638">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="76011-1638">Az.FrontDoor</span></span>
* <span data-ttu-id="76011-1639">WAF에서 사용할 수 있는 관리형 규칙 정의를 가져오는 cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1639">Added cmdlet to get managed rule definitions that can be used in WAF</span></span>

#### <a name="aziothub"></a><span data-ttu-id="76011-1640">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="76011-1640">Az.IotHub</span></span>
* <span data-ttu-id="76011-1641">Iot Hub에서 디바이스를 관리하기 위한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1641">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="76011-1642">새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1642">New Cmdlets are:</span></span>
    - <span data-ttu-id="76011-1643">'Add-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="76011-1643">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="76011-1644">'Get-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="76011-1644">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="76011-1645">'Remove-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="76011-1645">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="76011-1646">'Set-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="76011-1646">'Set-AzIotHubDevice'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="76011-1647">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="76011-1647">Az.KeyVault</span></span>
* <span data-ttu-id="76011-1648">Add-AzKeyVaultKey.md에 대해 중복된 텍스트가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1648">Fixed duplicated text for Add-AzKeyVaultKey.md</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="76011-1649">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="76011-1649">Az.Monitor</span></span>
* <span data-ttu-id="76011-1650">Get-AzLog cmdlet에 대한 설명이 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1650">Fixed description of the Get-AzLog cmdlet.</span></span>
* <span data-ttu-id="76011-1651">ActionGroupId라는 새 매개 변수가 'New-AzMetricAlertRuleV2' 명령에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1651">A new parameter called ActionGroupId was added to 'New-AzMetricAlertRuleV2' command.</span></span>
    - <span data-ttu-id="76011-1652">사용자는 ActionGroupId(string) 또는 ActionGorup(ActivityLogAlertActionGroup) 중 하나를 제공할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1652">The user can provide either ActionGroupId(string) or ActionGorup(ActivityLogAlertActionGroup).</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="76011-1653">Az.Network</span><span class="sxs-lookup"><span data-stu-id="76011-1653">Az.Network</span></span>
* <span data-ttu-id="76011-1654">'New-AzPrivateLinkService' cmdlet의 '-EnableProxyProtocol' 매개 변수에 대한 하나의 추가 매개 변수 메모가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1654">Added one extra parameter note for parameter '-EnableProxyProtocol' for 'New-AzPrivateLinkService' cmdlet.</span></span>
* <span data-ttu-id="76011-1655">Start-AzVirtualNetworkGatewayConnectionPacketCapture.md 및 Start-AzVirtualnetworkGatewayPacketCapture.md의 FilterData 예제가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1655">Fixed FilterData example in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="76011-1656">Start-AzVirtualNetworkGatewayConnectionPacketCapture.md 및 Start-AzVirtualnetworkGatewayPacketCapture.md의 모든 내부 및 외부 패킷을 캡처하는 패킷 캡처 예제가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1656">Added Packet Capture example for capture all inner and outer packets in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="76011-1657">VNet 방화벽에서 Azure Firewall 정책이 지원됩니다</span><span class="sxs-lookup"><span data-stu-id="76011-1657">Supported Azure Firewall Policy on VNet Firewalls</span></span>
    - <span data-ttu-id="76011-1658">새로 추가된 cmdlet이 없습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1658">No new cmdlets are added.</span></span> <span data-ttu-id="76011-1659">VNet 방화벽에서 방화벽 정책 제한이 완화되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1659">Relaxing the restriction for firewall policy on VNet firewalls</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="76011-1660">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="76011-1660">Az.RecoveryServices</span></span>
* <span data-ttu-id="76011-1661">SQL Database에 대한 파일로 복원 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1661">Added Support for Restore-as-files for SQL Databases.</span></span>

#### <a name="azresources"></a><span data-ttu-id="76011-1662">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="76011-1662">Az.Resources</span></span>
* <span data-ttu-id="76011-1663">템플릿 배포 cmdlet이 리팩터링되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1663">Refactored template deployment cmdlets</span></span>
    - <span data-ttu-id="76011-1664">관리 그룹에서 배포를 관리하는 새 \*-AzManagementGroupDeployment cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1664">Added new cmdlets for managing deployments at management group: \*-AzManagementGroupDeployment</span></span>
    - <span data-ttu-id="76011-1665">테넌트 범위에서 배포를 관리하는 새 \*-AzTenantDeployment cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1665">Added new cmdlets for managing deployments at tenant scope: \*-AzTenantDeployment</span></span>
    - <span data-ttu-id="76011-1666">구독 범위에서 구체적으로 작동하도록 \*-AzDeployment cmdlet이 리팩터링되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1666">Refactored \*-AzDeployment cmdlets to work specifically at subscription scope</span></span>
    - <span data-ttu-id="76011-1667">\*-AzDeployment cmdlet에 대한 \*-AzSubscriptionDeployment 별칭이 만들어졌습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1667">Created aliases \*-AzSubscriptionDeployment for \*-AzDeployment cmdlets</span></span>
* <span data-ttu-id="76011-1668">'AvailableToOtherTenants' 매개 변수가 설정되지 않는 'Update-AzADApplication'이 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1668">Fixed 'Update-AzADApplication' when parameter 'AvailableToOtherTenants' is not set</span></span>
* <span data-ttu-id="76011-1669">AmbiguousParameterSetException을 방지하기 위해 ApplicationObjectWithoutCredentialParameterSet이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1669">Removed ApplicationObjectWithoutCredentialParameterSet to avoid AmbiguousParameterSetException.</span></span>
* <span data-ttu-id="76011-1670">도움말 파일이 다시 생성되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1670">Regenerated help files</span></span>

#### <a name="azsql"></a><span data-ttu-id="76011-1671">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="76011-1671">Az.Sql</span></span>
* <span data-ttu-id="76011-1672">Managed Instance에서 구독 간 특정 시점 복원에 대한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1672">Added support for cross subscription point in time restore on Managed Instances.</span></span>
* <span data-ttu-id="76011-1673">기존 SQL Managed Instance 하드웨어 생성 변경에 대한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1673">Added support for changing existing Sql Managed Instance hardware generation</span></span>
* <span data-ttu-id="76011-1674">'Update-AzSqlServerVulnerabilityAssessmentSetting' 도움말 예제(매개 변수/속성 출력 -EmailAdmins)가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1674">Fixed 'Update-AzSqlServerVulnerabilityAssessmentSetting' help examples: parameter/property output - EmailAdmins</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="76011-1675">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="76011-1675">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="76011-1676">가용성 그룹 수신기에 대한 cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1676">Added cmdlets for Availability Group Listener</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="76011-1677">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="76011-1677">Az.StorageSync</span></span>
* <span data-ttu-id="76011-1678">'Invoke-AzStorageSyncCompatibilityCheck'에서 지원되는 문자 세트가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1678">Updated supported character sets in 'Invoke-AzStorageSyncCompatibilityCheck'.</span></span>

## <a name="340---february-2020"></a><span data-ttu-id="76011-1679">3.4.0 - 2020년 2월</span><span class="sxs-lookup"><span data-stu-id="76011-1679">3.4.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="76011-1680">마지막 주 릴리스 이후의 주요 사항</span><span class="sxs-lookup"><span data-stu-id="76011-1680">Highlights since the last major release</span></span>
* <span data-ttu-id="76011-1681">Az. CosmosDB 초기 버전 0.1.0 출시</span><span class="sxs-lookup"><span data-stu-id="76011-1681">Az.CosmosDB initial version 0.1.0 released</span></span>
* <span data-ttu-id="76011-1682">Az.Network ConnectionMonitor V2 지원 추가</span><span class="sxs-lookup"><span data-stu-id="76011-1682">Az.Network ConnectionMonitor V2 support added</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="76011-1683">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="76011-1683">Az.Accounts</span></span>
* <span data-ttu-id="76011-1684">AzureRmContext.json을 사용할 수 없을 때 컨텍스트 자동 저장 사용 안 함</span><span class="sxs-lookup"><span data-stu-id="76011-1684">Disable context auto saving when AzureRmContext.json not available</span></span>
* <span data-ttu-id="76011-1685">Azure Powershell Common 참조를 1.3.5-preview로 업데이트</span><span class="sxs-lookup"><span data-stu-id="76011-1685">Update the reference to Azure Powershell Common to 1.3.5-preview</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="76011-1686">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="76011-1686">Az.ApiManagement</span></span>
* <span data-ttu-id="76011-1687">**Get-AzApiManagementApiSchema** API와 연결된 Open-Api 스키마 가져오기 수정   https://github.com/Azure/azure-powershell/issues/10626</span><span class="sxs-lookup"><span data-stu-id="76011-1687">**Get-AzApiManagementApiSchema** Fixed getting Open-Api Schema associated with an API   https://github.com/Azure/azure-powershell/issues/10626</span></span>
* <span data-ttu-id="76011-1688">**New-AzApiManagementProduct** _ 및 _ *Set-AzApiManagementProduct*\*</span><span class="sxs-lookup"><span data-stu-id="76011-1688">**New-AzApiManagementProduct** _ and _ *Set-AzApiManagementProduct*\*</span></span>
  - <span data-ttu-id="76011-1689"> https://github.com/Azure/azure-powershell/issues/10472 설명서 수정</span><span class="sxs-lookup"><span data-stu-id="76011-1689">Fix documentation for https://github.com/Azure/azure-powershell/issues/10472</span></span>
* <span data-ttu-id="76011-1690">**Set-AzApiManagementApi** cmdlet을 사용하여 ServiceUrl을 업데이트하는 방법을 보여주는 예제 추가</span><span class="sxs-lookup"><span data-stu-id="76011-1690">**Set-AzApiManagementApi** Added example to show how to update the ServiceUrl using the cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="76011-1691">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="76011-1691">Az.Compute</span></span>
* <span data-ttu-id="76011-1692">VM 이름을 사용하지 않고 Get-AzVM -Status를 수행할 때 제한을 피하기 위해 VM 상태 수를 100개로 제한</span><span class="sxs-lookup"><span data-stu-id="76011-1692">Limit the number of VM status to 100 to avoid throttling when Get-AzVM -Status is performed without VM name.</span></span>
* <span data-ttu-id="76011-1693">Update-AzDiskEncryptionSet cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="76011-1693">Add Update-AzDiskEncryptionSet cmdlet</span></span>
* <span data-ttu-id="76011-1694">다음 cmdlet에 EncryptionType 및 DiskEncryptionSetId 매개 변수 추가:</span><span class="sxs-lookup"><span data-stu-id="76011-1694">Add EncryptionType and DiskEncryptionSetId parameters to the following cmdlets:</span></span>
    - <span data-ttu-id="76011-1695">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="76011-1695">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span></span>
* <span data-ttu-id="76011-1696">Get-AzProximityPlacementGroup cmdlet에 ColocationStatus 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="76011-1696">Add ColocationStatus parameter to Get-AzProximityPlacementGroup cmdlet.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="76011-1697">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="76011-1697">Az.DataFactory</span></span>
* <span data-ttu-id="76011-1698">ADF .Net SDK 버전을 4.7.0으로 업데이트</span><span class="sxs-lookup"><span data-stu-id="76011-1698">Update ADF .Net SDK version to 4.7.0</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="76011-1699">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="76011-1699">Az.DeploymentManager</span></span>
* <span data-ttu-id="76011-1700">리소스에 대한 LIST 작업 추가</span><span class="sxs-lookup"><span data-stu-id="76011-1700">Adds LIST operations for resources</span></span>
* <span data-ttu-id="76011-1701">상태 검사 단계에 대한 작업을 수행하는 기능 추가</span><span class="sxs-lookup"><span data-stu-id="76011-1701">Adds capability for performing operations on Health Check steps</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="76011-1702">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="76011-1702">Az.HDInsight</span></span>
* <span data-ttu-id="76011-1703">AzHDInsightCluster의 문서 오류 수정</span><span class="sxs-lookup"><span data-stu-id="76011-1703">Fix document error of New-AzHDInsightCluster.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="76011-1704">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="76011-1704">Az.KeyVault</span></span>
* <span data-ttu-id="76011-1705">Remove-AzureKeyVault가 새 New-AzureKeyVault와 일관성을 유지하도록 VaultName 특성에 이름 별칭 추가</span><span class="sxs-lookup"><span data-stu-id="76011-1705">Add Name alias to VaultName attribute to make Remove-AzureKeyVault consistent with New-AzureKeyVault.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="76011-1706">Az.Network</span><span class="sxs-lookup"><span data-stu-id="76011-1706">Az.Network</span></span>
* <span data-ttu-id="76011-1707">Set-AzNetworkWatcherConfigFlowLog.md에 트래픽 분석 사용 안 함 시나리오를 보여주는 새 예제 추가</span><span class="sxs-lookup"><span data-stu-id="76011-1707">New example added to Set-AzNetworkWatcherConfigFlowLog.md to demonstrate Traffic Analytics disable scenario.</span></span>
* <span data-ttu-id="76011-1708">Azure Firewall에 관리 IP 구성을 할당하는 지원 추가 - 방화벽에서 관리 트래픽에 사용할 전용 서브넷 및 공용 IP</span><span class="sxs-lookup"><span data-stu-id="76011-1708">Add support for assigning management IP configuration to Azure Firewall - a dedicated subnet and Public IP that the firewall will use for its management traffic</span></span>
    - <span data-ttu-id="76011-1709">New-AzFirewall cmdlet이 업데이트됨:</span><span class="sxs-lookup"><span data-stu-id="76011-1709">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="76011-1710">공용 IP 주소 개체를 허용하는 -ManagementPublicIpAddress 매개 변수(필수 아님) 추가</span><span class="sxs-lookup"><span data-stu-id="76011-1710">Added parameter -ManagementPublicIpAddress (not mandatory) which accepts a Public IP Address object</span></span>
        - <span data-ttu-id="76011-1711">방화벽 개체에 SetManagementIpConfiguration 메서드 추가 - 입력으로 서브넷 및 공용 IP 주소 필요 - 서브넷 이름은 'AzureFirewallManagementSubnet'이어야 함</span><span class="sxs-lookup"><span data-stu-id="76011-1711">Added method SetManagementIpConfiguration on firewall object - requires a subnet and a Public IP address as input - subnet name must be 'AzureFirewallManagementSubnet'</span></span>
* <span data-ttu-id="76011-1712">네트워크 인터페이스 대신 NSG 예제를 보여주도록 AzNetworkSecurityGroup 예제 수정</span><span class="sxs-lookup"><span data-stu-id="76011-1712">Corrected Get-AzNetworkSecurityGroup examples to show examples for NSG's instead of network interfaces.</span></span>
* <span data-ttu-id="76011-1713">리소스 id 완성자가 매개 변수를 완성하지 못하게 방해하던 New-AzVpnSite 명령의 오타 수정</span><span class="sxs-lookup"><span data-stu-id="76011-1713">Fixed typo in New-AzVpnSite command that was preventing resource id completer from completing a parameter.</span></span>
* <span data-ttu-id="76011-1714">Application Gateway의 다시 쓰기 규칙 작업 세트에서 Url 구성에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="76011-1714">Added support for Url Confiugration in Rewrite Rules Action Set in the Application Gateway</span></span>
    - <span data-ttu-id="76011-1715">추가된 새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1715">New cmdlets added:</span></span>
        - <span data-ttu-id="76011-1716">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="76011-1716">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span></span>
    - <span data-ttu-id="76011-1717">선택적 매개 변수를 사용하도록 Cmdlet 업데이트 - UrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="76011-1717">Cmdlets updated with optional parameter - UrlConfiguration</span></span>
        - <span data-ttu-id="76011-1718">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="76011-1718">New-AzApplicationGatewayRewriteRuleActionSet</span></span>
* <span data-ttu-id="76011-1719">NetworkWatcher ConnectionMonitor 버전 2 리소스에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="76011-1719">Add suppport for NetworkWatcher ConnectionMonitor version 2 resources</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="76011-1720">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="76011-1720">Az.PolicyInsights</span></span>
* <span data-ttu-id="76011-1721">수정할 리소스를 결정하기 전에 규정 준수 평가 지원</span><span class="sxs-lookup"><span data-stu-id="76011-1721">Support evaluating compliance prior to determining what resource to remediate</span></span>
    - <span data-ttu-id="76011-1722">Start-AzPolicyRemediation에 '-ResourceDiscoverMode' 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="76011-1722">Add '-ResourceDiscoverMode' parameter to Start-AzPolicyRemediation</span></span>
* <span data-ttu-id="76011-1723">정책 메타데이터 리소스를 가져오는 Get-AzPolicyMetadata cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="76011-1723">Add Get-AzPolicyMetadata cmdlet for getting policy metadata resources</span></span>
* <span data-ttu-id="76011-1724">API 버전 2019-10-01의 Get-AzPolicyState 및 Get-AzPolicyStateSummary 업데이트</span><span class="sxs-lookup"><span data-stu-id="76011-1724">Updated Get-AzPolicyState and Get-AzPolicyStateSummary for API version 2019-10-01</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="76011-1725">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="76011-1725">Az.RecoveryServices</span></span>
* <span data-ttu-id="76011-1726">복제된 디스크를 제거할 수 있도록 Azure Site Recovery에 지원 추가</span><span class="sxs-lookup"><span data-stu-id="76011-1726">Azure Site Recovery support for removing a replicated disk.</span></span>
* <span data-ttu-id="76011-1727">Recovery Services 자격 증명 모음을 만드는 동안 태그를 추가할 수 있도록 Azure Backup에 지원 추가</span><span class="sxs-lookup"><span data-stu-id="76011-1727">Azure Backup added support for adding tags while creating a Recovery Services Vault.</span></span>

#### <a name="azresources"></a><span data-ttu-id="76011-1728">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="76011-1728">Az.Resources</span></span>
* <span data-ttu-id="76011-1729">컨텍스트 구독을 기본값으로 하는 \*-AzPolicyAssignment cmdlet에서 -Scope를 선택 사항으로 설정</span><span class="sxs-lookup"><span data-stu-id="76011-1729">Make -Scope optional in \*-AzPolicyAssignment cmdlets with default to context subscription</span></span>
* <span data-ttu-id="76011-1730">암호 및 키 자격 증명을 사용하여 ADServicePrincipal을 만드는 예제 추가</span><span class="sxs-lookup"><span data-stu-id="76011-1730">Add examples of creating ADServicePrincipal with password and key credential</span></span>

#### <a name="azsql"></a><span data-ttu-id="76011-1731">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="76011-1731">Az.Sql</span></span>
<span data-ttu-id="76011-1732">DatabaseName 대신 PartnerDatabaseName이 있는지 확인하도록 New-AzSqlDatabaseSecondary cmdlet 수정</span><span class="sxs-lookup"><span data-stu-id="76011-1732">Fix New-AzSqlDatabaseSecondary cmdlet to check for PartnerDatabaseName existence instead of DatabaseName existence.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="76011-1733">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="76011-1733">Az.Storage</span></span>
* <span data-ttu-id="76011-1734">스토리지 계정 만들기에서 테이블/큐 암호화 Keytype 설정 지원</span><span class="sxs-lookup"><span data-stu-id="76011-1734">Support set Table/Queue Encryption Keytype in Create Storage Account</span></span>
    - <span data-ttu-id="76011-1735">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="76011-1735">New-AzStorageAccount</span></span>
* <span data-ttu-id="76011-1736">StorageException에 ExtendedErrorInformation이 없으면 RequestId 표시</span><span class="sxs-lookup"><span data-stu-id="76011-1736">Show RequestId when StorageException don't have ExtendedErrorInformation</span></span>
* <span data-ttu-id="76011-1737">cmdlet Start-AzStorageBlobCopy의 예제 6 수정</span><span class="sxs-lookup"><span data-stu-id="76011-1737">Fix the Example 6 of cmdlet Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="76011-1738">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="76011-1738">Az.Websites</span></span>
* <span data-ttu-id="76011-1739">Set-AzWebapp 및 Set-AzWebappSlot이 AlwaysOn, MinTls 및 FtpsState 속성 지원</span><span class="sxs-lookup"><span data-stu-id="76011-1739">Set-AzWebapp and Set-AzWebappSlot supports AlwaysOn, MinTls and FtpsState properties</span></span>
* <span data-ttu-id="76011-1740">단일 Set-AzWebApp 명령을 사용하여 AppservicePlan을 변경하는 동시에 HttpsOnly를 설정하면 HttpsOnly가 기본값으로 다시 설정되는 문제 수정</span><span class="sxs-lookup"><span data-stu-id="76011-1740">Fixing issue where setting HttpsOnly along with changing AppservicePlan at the same time using the single Set-AzWebApp Command, was resetting HttpsOnly to default value</span></span>

## <a name="330---january-2020"></a><span data-ttu-id="76011-1741">3.3.0 - 2020년 1월</span><span class="sxs-lookup"><span data-stu-id="76011-1741">3.3.0 - January 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="76011-1742">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="76011-1742">Az.Accounts</span></span>
* <span data-ttu-id="76011-1743">AzureAttestationServiceEndpointResourceId 및 AzureAttestationServiceEndpointSuffix 매개 변수를 허용하도록 Add-AzEnvironment 및 Set-AzEnvironment가 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="76011-1743">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameters AzureAttestationServiceEndpointResourceId and AzureAttestationServiceEndpointSuffix</span></span>

#### <a name="azcdn"></a><span data-ttu-id="76011-1744">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="76011-1744">Az.Cdn</span></span>
* <span data-ttu-id="76011-1745">New-AzCdnEndpoint cmdlet에서 오류 응답 세부 정보 표시</span><span class="sxs-lookup"><span data-stu-id="76011-1745">Display error response detail in New-AzCdnEndpoint cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="76011-1746">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="76011-1746">Az.Compute</span></span>
* <span data-ttu-id="76011-1747">OS 프로필이 없는 관리 OD 디스크가 있는 VM의 Set-AzVMCustomScriptExtension cmdlet을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1747">Fix Set-AzVMCustomScriptExtension cmdlet for a VM with managed OD disk which does not have OS profile.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="76011-1748">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="76011-1748">Az.ContainerInstance</span></span>
* <span data-ttu-id="76011-1749">New-AzContainerGroup의 예에서 사용되는 고정 매개 변수 이름</span><span class="sxs-lookup"><span data-stu-id="76011-1749">Fixed parameter names used by example of New-AzContainerGroup</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="76011-1750">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="76011-1750">Az.DataBoxEdge</span></span>
* <span data-ttu-id="76011-1751">'Get-AzDataBoxEdgeStorageContainer' cmdlet 추가됨</span><span class="sxs-lookup"><span data-stu-id="76011-1751">Added cmdlet 'Get-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="76011-1752">Edge 스토리지 컨테이너 가져오기</span><span class="sxs-lookup"><span data-stu-id="76011-1752">Get the Edge Storage Container</span></span>
* <span data-ttu-id="76011-1753">'New-AzDataBoxEdgeStorageContainer' cmdlet 추가됨</span><span class="sxs-lookup"><span data-stu-id="76011-1753">Added cmdlet 'New-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="76011-1754">새 Edge 스토리지 컨테이너 만들기</span><span class="sxs-lookup"><span data-stu-id="76011-1754">Create new Edge Strorage Container</span></span>
* <span data-ttu-id="76011-1755">'Remove-AzDataBoxEdgeStorageContainer' cmdlet 추가됨</span><span class="sxs-lookup"><span data-stu-id="76011-1755">Added cmdlet 'Remove-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="76011-1756">Edge 스토리지 컨테이너 제거</span><span class="sxs-lookup"><span data-stu-id="76011-1756">Remove the Edge Storage Container</span></span>
* <span data-ttu-id="76011-1757">'Invoke-AzDataBoxEdgeStorageContainer' cmdlet 추가됨</span><span class="sxs-lookup"><span data-stu-id="76011-1757">Added cmdlet 'Invoke-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="76011-1758">Edge 스토리지 컨테이너에서 데이터를 새로 고치는 작업 호출</span><span class="sxs-lookup"><span data-stu-id="76011-1758">Invoke action to refresh data on Edge Storage Container</span></span>
* <span data-ttu-id="76011-1759">'Get-AzDataBoxEdgeStorageAccount' cmdlet 추가됨</span><span class="sxs-lookup"><span data-stu-id="76011-1759">Added cmdlet 'Get-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="76011-1760">Edge 스토리지 계정 가져오기</span><span class="sxs-lookup"><span data-stu-id="76011-1760">Get the Edge Storage Account</span></span>
* <span data-ttu-id="76011-1761">'New-AzDataBoxEdgeStorageAccount' cmdlet 추가됨</span><span class="sxs-lookup"><span data-stu-id="76011-1761">Added cmdlet 'New-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="76011-1762">새 Edge 스토리지 계정 만들기</span><span class="sxs-lookup"><span data-stu-id="76011-1762">Create new Edge Storage Account</span></span>
* <span data-ttu-id="76011-1763">'Remove-AzDataBoxEdgeStorageAccount' cmdlet 추가됨</span><span class="sxs-lookup"><span data-stu-id="76011-1763">Added cmdlet 'Remove-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="76011-1764">Edge 스토리지 계정 제거</span><span class="sxs-lookup"><span data-stu-id="76011-1764">Remove the Edge Storage Account</span></span>
* <span data-ttu-id="76011-1765">'Invoke-AzDataBoxEdgeShare' cmdlet 호출</span><span class="sxs-lookup"><span data-stu-id="76011-1765">Invoke cmdlet 'Invoke-AzDataBoxEdgeShare'</span></span>
  - <span data-ttu-id="76011-1766">공유에서 데이터를 새로 고치는 작업 호출</span><span class="sxs-lookup"><span data-stu-id="76011-1766">Invoke action to refresh data on share</span></span>
* <span data-ttu-id="76011-1767">'Set-AzDataBoxEdgeStorageAccountCredential' cmdlet 추가됨</span><span class="sxs-lookup"><span data-stu-id="76011-1767">Added cmdlet 'Set-AzDataBoxEdgeStorageAccountCredential'</span></span>
  - <span data-ttu-id="76011-1768">az databoxedge 스토리지 계정 자격 증명 설정</span><span class="sxs-lookup"><span data-stu-id="76011-1768">Set the az databoxedge storage account credential</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="76011-1769">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="76011-1769">Az.DataFactory</span></span>
* <span data-ttu-id="76011-1770">Get-AzDataFactoryV2IntegrationRuntime cmd에 AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId 및 VersionStatus 속성 추가</span><span class="sxs-lookup"><span data-stu-id="76011-1770">Add AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId and VersionStatus properties for Get-AzDataFactoryV2IntegrationRuntime cmd</span></span>
* <span data-ttu-id="76011-1771">ADF .Net SDK 버전을 4.6.0으로 업데이트</span><span class="sxs-lookup"><span data-stu-id="76011-1771">Update ADF .Net SDK version to 4.6.0</span></span>
* <span data-ttu-id="76011-1772">고정 공용 IP 주소로 Azure-SSIS IR을 만들 수 있도록 'Set-AzureRmDataFactoryV2IntegrationRuntime'cmd에 대해 'PublicIPs' 매개 변수를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1772">Add parameter 'PublicIPs' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable create Azure-SSIS IR with static public IP addresses.</span></span>

#### <a name="azdevtestlabs"></a><span data-ttu-id="76011-1773">Az.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="76011-1773">Az.DevTestLabs</span></span>
* <span data-ttu-id="76011-1774">Get-AzDtlAllowedVMSizesPolicy.md에서 끊어진 링크 제거</span><span class="sxs-lookup"><span data-stu-id="76011-1774">Remove the broken link in Get-AzDtlAllowedVMSizesPolicy.md</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="76011-1775">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="76011-1775">Az.EventHub</span></span>
* <span data-ttu-id="76011-1776">10634 문제 해결: eventhubnamespace 제거에 대한 null 개체 참조 수정</span><span class="sxs-lookup"><span data-stu-id="76011-1776">Fix for issue 10634 : Fix the null Object reference for remove eventhubnamespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="76011-1777">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="76011-1777">Az.HDInsight</span></span>
* <span data-ttu-id="76011-1778">Invoke-AzHDInsightHiveJob.md 오류를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1778">Fix Invoke-AzHDInsightHiveJob.md error.</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="76011-1779">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="76011-1779">Az.MachineLearning</span></span>
* <span data-ttu-id="76011-1780">MachineLearningCompute를 더 이상 사용할 수 없게 되어 아래 cmdlet이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1780">Removed below cmdlets because MachineLearningCompute is not available any longer</span></span>
  - <span data-ttu-id="76011-1781">Get-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="76011-1781">Get-AzMlOpCluster</span></span>
  - <span data-ttu-id="76011-1782">Get-AzMlOpClusterKey</span><span class="sxs-lookup"><span data-stu-id="76011-1782">Get-AzMlOpClusterKey</span></span>
  - <span data-ttu-id="76011-1783">New-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="76011-1783">New-AzMlOpCluster</span></span>
  - <span data-ttu-id="76011-1784">Remove-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="76011-1784">Remove-AzMlOpCluster</span></span>
  - <span data-ttu-id="76011-1785">Set-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="76011-1785">Set-AzMlOpCluster</span></span>
  - <span data-ttu-id="76011-1786">Test-AzMlOpClusterSystemServicesUpdateAvailability</span><span class="sxs-lookup"><span data-stu-id="76011-1786">Test-AzMlOpClusterSystemServicesUpdateAvailability</span></span>
  - <span data-ttu-id="76011-1787">Update-AzMlOpClusterSystemService</span><span class="sxs-lookup"><span data-stu-id="76011-1787">Update-AzMlOpClusterSystemService</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="76011-1788">Az.Network</span><span class="sxs-lookup"><span data-stu-id="76011-1788">Az.Network</span></span>
* <span data-ttu-id="76011-1789">Microsoft.Azure.Management.Sql의 종속성을 1.36-preview에서 1.37-preview로 업그레이드</span><span class="sxs-lookup"><span data-stu-id="76011-1789">Upgrade dependency of Microsoft.Azure.Management.Sql from 1.36-preview to 1.37-preview</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="76011-1790">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="76011-1790">Az.RecoveryServices</span></span>
* <span data-ttu-id="76011-1791">Azure Site Recovery는 Azure 간 공급자를 위해 고객 관리 키와 함께 유휴 상태에서 암호화된 관리 디스크 vms의 변경을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1791">Azure Site Recovery change support for managed disk vms encrypted at rest with customer managed keys for Azure to Azure provider.</span></span>
* <span data-ttu-id="76011-1792">Azure Site Recovery는 VMware에서 Azure로를 위해 보호를 사용할 때 선택적 입력으로서 디스크 암호화 집합 ID를 입력하도록 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1792">Azure Site Recovery support to input disk encryption Set Id as optional input at enabling protection for Vmware to Azure.</span></span>
* <span data-ttu-id="76011-1793">Azure Site Recovery는 VMware에서 Azure로를 위해 보호를 사용하기 위해 디스크 수준의 선택적 입력으로서 디스크 암호화 집합 ID를 입력하도록 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1793">Azure Site Recovery support to input disk encryption Set Id as optional input at disk level to enable protection for Vmware to Azure.</span></span>
* <span data-ttu-id="76011-1794">Azure Site Recovery는 HyperV에서 Azure로를 위해 디스크 암호화 집합 맵을 사용하여 복제 보호된 항목을 업데이트하도록 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1794">Azure Site Recovery support to update replication protected item with disk encryption set Map for HyperV to Azure.</span></span>

#### <a name="azresources"></a><span data-ttu-id="76011-1795">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="76011-1795">Az.Resources</span></span>
* <span data-ttu-id="76011-1796">'Remove-AzTag'의 도움말 문서에서 오류를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1796">Fix an error in help document of 'Remove-AzTag'.</span></span>

#### <a name="azsql"></a><span data-ttu-id="76011-1797">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="76011-1797">Az.Sql</span></span>
* <span data-ttu-id="76011-1798">Azure Database의 마스터 DB에서 작동하도록 취약성 평가 세트 기준 cmdlet 기능을 수정하고 관리형 인스턴스 시스템 데이터베이스에서 이를 제한합니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1798">Fix vulnerability assessment set baseline cmdlets functionality to work on master db for azure database and limit it on managed instance system databases.</span></span>
* <span data-ttu-id="76011-1799">SQL 인스턴스 장애 조치(failover) 그룹을 만들 때 오류 수정</span><span class="sxs-lookup"><span data-stu-id="76011-1799">Fix an error when creating SQL instance failover group</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="76011-1800">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="76011-1800">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="76011-1801">올바른 새 라이선스 형식으로 DR 추가</span><span class="sxs-lookup"><span data-stu-id="76011-1801">Add DR as a new valid License type</span></span>

#### <a name="azstorage"></a><span data-ttu-id="76011-1802">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="76011-1802">Az.Storage</span></span>
* <span data-ttu-id="76011-1803">다음 릴리스에서 DefaultAction Value 변경에 대해 호환성이 손상되는 변경 경고 메시지 추가</span><span class="sxs-lookup"><span data-stu-id="76011-1803">Add breaking change warning message for DefaultAction Value change in a future release</span></span>
    - <span data-ttu-id="76011-1804">Update-AzStorageAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="76011-1804">Update-AzStorageAccountNetworkRuleSet</span></span>
* <span data-ttu-id="76011-1805">-IncludeGeoReplicationStats 매개 변수와 함께 get-AzureRMStorageAccount를 실행하여 스토리지 계정의 마지막 동기화 시간 가져오기 지원</span><span class="sxs-lookup"><span data-stu-id="76011-1805">Support Get last sync time of Storage account by run get-AzureRMStorageAccount with parameter -IncludeGeoReplicationStats</span></span>
    - <span data-ttu-id="76011-1806">Get-AzureRMStorageAccount</span><span class="sxs-lookup"><span data-stu-id="76011-1806">Get-AzureRMStorageAccount</span></span>

## <a name="320---december-2019"></a><span data-ttu-id="76011-1807">3.2.0 - 2019년 12월</span><span class="sxs-lookup"><span data-stu-id="76011-1807">3.2.0 - December 2019</span></span>

### <a name="general"></a><span data-ttu-id="76011-1808">일반</span><span class="sxs-lookup"><span data-stu-id="76011-1808">General</span></span>
* <span data-ttu-id="76011-1809">모든 모듈의 상대 경로를 사용하기 위해 .psd1의 참조 업데이트</span><span class="sxs-lookup"><span data-stu-id="76011-1809">Update references in .psd1 to use relative path for all modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="76011-1810">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="76011-1810">Az.Accounts</span></span>
* <span data-ttu-id="76011-1811">Az 4.0 미리 보기를 위해 클라이언트 측 원격 분석에 대해 UserAgent를 올바르게 설정</span><span class="sxs-lookup"><span data-stu-id="76011-1811">Set correct UserAgent for client-side telemetry for Az 4.0 preview</span></span>
* <span data-ttu-id="76011-1812">Az 4.0 미리 보기에서 컨텍스트가 null인 경우 사용자에게 친숙한 오류 메시지로 표시</span><span class="sxs-lookup"><span data-stu-id="76011-1812">Display user friendly error message when context is null in Az 4.0 preview</span></span>

#### <a name="azbatch"></a><span data-ttu-id="76011-1813">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="76011-1813">Az.Batch</span></span>
* <span data-ttu-id="76011-1814">**New-AzBatchPool** 이 'VirtualMachineConfiguration.ContainerConfiguration' 또는 'VirtualMachineConfiguration.DataDisks'를 서버로 제대로 보내지 않는 [#10602](https://github.com/Azure/azure-powershell/issues/10602) 문제 수정</span><span class="sxs-lookup"><span data-stu-id="76011-1814">Fix issue [#10602](https://github.com/Azure/azure-powershell/issues/10602), where **New-AzBatchPool** did not properly send 'VirtualMachineConfiguration.ContainerConfiguration' or 'VirtualMachineConfiguration.DataDisks' to the server.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="76011-1815">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="76011-1815">Az.DataFactory</span></span>
* <span data-ttu-id="76011-1816">ADF .Net SDK 버전을 4.5.0으로 업데이트</span><span class="sxs-lookup"><span data-stu-id="76011-1816">Update ADF .Net SDK version to 4.5.0</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="76011-1817">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="76011-1817">Az.FrontDoor</span></span>
* <span data-ttu-id="76011-1818">WAF 관리 규칙 제외 지원 추가됨</span><span class="sxs-lookup"><span data-stu-id="76011-1818">Added WAF managed rules exclusion support</span></span>
* <span data-ttu-id="76011-1819">자동 완성에 SocketAddr 추가</span><span class="sxs-lookup"><span data-stu-id="76011-1819">Add SocketAddr to auto-complete</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="76011-1820">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="76011-1820">Az.HealthcareApis</span></span>
* <span data-ttu-id="76011-1821">예외 처리</span><span class="sxs-lookup"><span data-stu-id="76011-1821">Exception Handling</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="76011-1822">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="76011-1822">Az.KeyVault</span></span>
* <span data-ttu-id="76011-1823">잠재적으로 설정되지 않은 오류 액세스 값 수정</span><span class="sxs-lookup"><span data-stu-id="76011-1823">Fixed error accessing value that is potentially not set</span></span>
* <span data-ttu-id="76011-1824">타원 곡선 암호화 인증서 관리</span><span class="sxs-lookup"><span data-stu-id="76011-1824">Elliptic Curve Cryptography Certificate Managment</span></span>
    - <span data-ttu-id="76011-1825">인증서 정책에 대한 곡선 지정을 위한 지원 추가됨</span><span class="sxs-lookup"><span data-stu-id="76011-1825">Added support to specify the Curve for Certificate Policies</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="76011-1826">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="76011-1826">Az.Monitor</span></span>
* <span data-ttu-id="76011-1827">진단 설정 추가 명령에 선택적 인수 추가</span><span class="sxs-lookup"><span data-stu-id="76011-1827">Adding optional argument to the Add Diagnostic Settings command.</span></span> <span data-ttu-id="76011-1828">스위치 인수(있는 경우)는 Log Analytics로 내보내기가 고정 스키마(전용 데이터 유형)가 되어야 함을</span><span class="sxs-lookup"><span data-stu-id="76011-1828">A switch argument that if present indicates that the export to Log Analytics must be to a fixed schema (a.k.a.</span></span> <span data-ttu-id="76011-1829">나타냄</span><span class="sxs-lookup"><span data-stu-id="76011-1829">dedicated, data type)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="76011-1830">Az.Network</span><span class="sxs-lookup"><span data-stu-id="76011-1830">Az.Network</span></span>
* <span data-ttu-id="76011-1831">AzureFirewall 애플리케이션, NAT 및 네트워크 규칙에서 IpGroups 지원.</span><span class="sxs-lookup"><span data-stu-id="76011-1831">Support for IpGroups in AzureFirewall Application,Nat & Network Rules.</span></span>

#### <a name="azresources"></a><span data-ttu-id="76011-1832">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="76011-1832">Az.Resources</span></span>
* <span data-ttu-id="76011-1833">이름이 일부 내장 매개 변수 이름과 충돌하는 경우 템플릿 배포가 템플릿 매개 변수를 읽지 못하는 문제 수정.</span><span class="sxs-lookup"><span data-stu-id="76011-1833">Fix an issue where template deployment fails to read a template parameter if its name conflicts with some built-in parameter name.</span></span>
* <span data-ttu-id="76011-1834">정책 세트 정의 내에 그룹화 지원을 도입하는 새로운 API 버전 2019-09-01을 사용하도록 정책 cmdlet 업데이트.</span><span class="sxs-lookup"><span data-stu-id="76011-1834">Updated policy cmdlets to use new api version 2019-09-01 that introduces grouping support within policy set definitions.</span></span>

#### <a name="azsql"></a><span data-ttu-id="76011-1835">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="76011-1835">Az.Sql</span></span>
* <span data-ttu-id="76011-1836">취약성 평가 자동 활성화에서 스토리지 생성을 StorageV2로 업그레이드</span><span class="sxs-lookup"><span data-stu-id="76011-1836">Upgraded storage creation in Vulnerability Assessment auto enablement to StorageV2</span></span>

#### <a name="azstorage"></a><span data-ttu-id="76011-1837">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="76011-1837">Az.Storage</span></span>
* <span data-ttu-id="76011-1838">Oauth 인증을 기반으로 스토리지 컨텍스트를 사용하여 Blob/컨테이너 ID 기반 SAS 토큰 생성 지원</span><span class="sxs-lookup"><span data-stu-id="76011-1838">Support generate Blob/Constainer Idenity based SAS token with Storage Context based on Oauth authentication</span></span>
    - <span data-ttu-id="76011-1839">New-AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="76011-1839">New-AzStorageContainerSASToken</span></span>
    - <span data-ttu-id="76011-1840">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="76011-1840">New-AzStorageBlobSASToken</span></span>
* <span data-ttu-id="76011-1841">모든 Idenity SAS 토큰을 해지할 수 있도록 스토리지 계정 사용자 위임 키 해지 지원</span><span class="sxs-lookup"><span data-stu-id="76011-1841">Support revoke Storage Account User Delegation Keys, so all Idenity SAS tokens are revoked</span></span>
    - <span data-ttu-id="76011-1842">Revoke-AzStorageAccountUserDelegationKeys</span><span class="sxs-lookup"><span data-stu-id="76011-1842">Revoke-AzStorageAccountUserDelegationKeys</span></span>
* <span data-ttu-id="76011-1843">새로운 API 버전 2019-06-01을 지원하기 위해 Microsoft.Azure.Management.Storage 14.2.0으로 업그레이드.</span><span class="sxs-lookup"><span data-stu-id="76011-1843">Upgrade to Microsoft.Azure.Management.Storage 14.2.0, to support new API version 2019-06-01.</span></span>
* <span data-ttu-id="76011-1844">File Share cmdlet의 관리 평면에서 5120을 초과하는 값에 대해 QuotaGiB(Gibyby의 공유 할당량)를 지원하고 'Quota' 매개 변수 별칭을 'QuotaGiB' 매개 변수에 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1844">Support of QuotaGiB (Share Quota in Gibibye) for values of more than 5120 in the Management plane of File Share cmdlets and added the 'Quota' parameter alias to the 'QuotaGiB' parameter.</span></span>
    - <span data-ttu-id="76011-1845">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="76011-1845">New-AzRmStorageShare</span></span>
    - <span data-ttu-id="76011-1846">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="76011-1846">Update-AzRmStorageShare</span></span>
* <span data-ttu-id="76011-1847">매개 변수 'Quota'에 매개 변수 별칭 'QuotaGiB' 추가</span><span class="sxs-lookup"><span data-stu-id="76011-1847">Add parameter alias 'QuotaGiB' to parameter 'Quota'</span></span>
    - <span data-ttu-id="76011-1848">Set-AzStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="76011-1848">Set-AzStorageShareQuota</span></span>
* <span data-ttu-id="76011-1849">Set-AzStorageContainerAcl가 저장된 액세스 정책을 정리할 수 있는 문제 수정</span><span class="sxs-lookup"><span data-stu-id="76011-1849">Fix the issue that Set-AzStorageContainerAcl can clean up the stored Access Policy</span></span>
    - <span data-ttu-id="76011-1850">Set-AzStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="76011-1850">Set-AzStorageContainerAcl</span></span>

## <a name="310---november-2019"></a><span data-ttu-id="76011-1851">3.1.0 - 2019년 11월</span><span class="sxs-lookup"><span data-stu-id="76011-1851">3.1.0 - November 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="76011-1852">마지막 주 릴리스 이후의 주요 사항</span><span class="sxs-lookup"><span data-stu-id="76011-1852">Highlights since the last major release</span></span>
* <span data-ttu-id="76011-1853">Az.DataBoxEdge 1.0.0 릴리스됨</span><span class="sxs-lookup"><span data-stu-id="76011-1853">Az.DataBoxEdge 1.0.0 released</span></span>
* <span data-ttu-id="76011-1854">Az.SqlVirtualMachine 1.0.0 릴리스됨</span><span class="sxs-lookup"><span data-stu-id="76011-1854">Az.SqlVirtualMachine 1.0.0 released</span></span>

#### <a name="azcompute"></a><span data-ttu-id="76011-1855">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="76011-1855">Az.Compute</span></span>
* <span data-ttu-id="76011-1856">VM Reapply 기능</span><span class="sxs-lookup"><span data-stu-id="76011-1856">VM Reapply feature</span></span>
    - <span data-ttu-id="76011-1857">Set-AzVM cmdlet에 Reapply 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="76011-1857">Add Reapply parameter to Set-AzVM cmdlet</span></span>
* <span data-ttu-id="76011-1858">VM 확장 집합 AutomaticRepairs 기능:</span><span class="sxs-lookup"><span data-stu-id="76011-1858">VM Scale Set AutomaticRepairs feature:</span></span>
    - <span data-ttu-id="76011-1859">다음 cmdlet에 EnableAutomaticRepair, AutomaticRepairGracePeriod 및 AutomaticRepairMaxInstanceRepairsPercent 매개 변수를 추가합니다.   New-AzVmssConfig   Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="76011-1859">Add EnableAutomaticRepair, AutomaticRepairGracePeriod, and AutomaticRepairMaxInstanceRepairsPercent parameters to the following cmdlets:   New-AzVmssConfig   Update-AzVmss</span></span>
* <span data-ttu-id="76011-1860">New-AzVM에 대한 교차 테넌트 갤러리 이미지 지원</span><span class="sxs-lookup"><span data-stu-id="76011-1860">Cross tenant gallery image support for New-AzVM</span></span>
* <span data-ttu-id="76011-1861">New-AzVM, New-AzVMConfig 및 New-AzVmss cmdlet의 Priority 매개 변수의 인수 완성자에 'Spot' 추가</span><span class="sxs-lookup"><span data-stu-id="76011-1861">Add 'Spot' to the argument completer of Priority parameter in New-AzVM, New-AzVMConfig and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="76011-1862">Add-AzVmssDataDisk cmdlet에 DiskIOPSReadWrite 및 DiskMBpsReadWrite 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="76011-1862">Add DiskIOPSReadWrite and DiskMBpsReadWrite parameters to Add-AzVmssDataDisk cmdlet</span></span>
* <span data-ttu-id="76011-1863">New-AzGalleryImageVersion cmdlet의 SourceImageId 매개 변수를 선택 사항으로 변경</span><span class="sxs-lookup"><span data-stu-id="76011-1863">Change SourceImageId parameter of New-AzGalleryImageVersion cmdlet to optional</span></span>
* <span data-ttu-id="76011-1864">New-AzGalleryImageVersion cmdlet에 OSDiskImage 및 DataDiskImage 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="76011-1864">Add OSDiskImage and DataDiskImage parameters to New-AzGalleryImageVersion cmdlet</span></span>
* <span data-ttu-id="76011-1865">New-AzGalleryImageDefinition cmdlet에 HyperVGeneration 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="76011-1865">Add HyperVGeneration parameter to New-AzGalleryImageDefinition cmdlet</span></span>
* <span data-ttu-id="76011-1866">New-AzVmss, New-AzVmssConfig 및 Update-AzVmss cmdlet에 SkipExtensionsOnOverprovisionedVMs 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="76011-1866">Add SkipExtensionsOnOverprovisionedVMs parameters to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="76011-1867">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="76011-1867">Az.DataBoxEdge</span></span>
* <span data-ttu-id="76011-1868">cmdlet `Get-AzDataBoxEdgeOrder` 추가됨</span><span class="sxs-lookup"><span data-stu-id="76011-1868">Added cmdlet `Get-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="76011-1869">주문 가져오기</span><span class="sxs-lookup"><span data-stu-id="76011-1869">Get the Order</span></span>
* <span data-ttu-id="76011-1870">cmdlet `New-AzDataBoxEdgeOrder` 추가됨</span><span class="sxs-lookup"><span data-stu-id="76011-1870">Added cmdlet `New-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="76011-1871">새 주문 만들기</span><span class="sxs-lookup"><span data-stu-id="76011-1871">Create new Order</span></span>
* <span data-ttu-id="76011-1872">cmdlet `Remove-AzDataBoxEdgeOrder` 추가됨</span><span class="sxs-lookup"><span data-stu-id="76011-1872">Added cmdlet `Remove-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="76011-1873">주문 제거</span><span class="sxs-lookup"><span data-stu-id="76011-1873">Remove the Order</span></span>
* <span data-ttu-id="76011-1874">cmdlet `New-AzDataBoxEdgeShare` 변경</span><span class="sxs-lookup"><span data-stu-id="76011-1874">Change in cmdlet `New-AzDataBoxEdgeShare`</span></span>
    - <span data-ttu-id="76011-1875">이제 로컬 공유를 만듬</span><span class="sxs-lookup"><span data-stu-id="76011-1875">Now creates Local Share</span></span>
* <span data-ttu-id="76011-1876">cmdlet `Set-AzDataBoxEdgeRole` 추가됨</span><span class="sxs-lookup"><span data-stu-id="76011-1876">Added cmdlet `Set-AzDataBoxEdgeRole`</span></span>
    - <span data-ttu-id="76011-1877">이제 IotRole을 공유에 매핑할 수 있음</span><span class="sxs-lookup"><span data-stu-id="76011-1877">Now IotRole can be mapped to Share</span></span>
* <span data-ttu-id="76011-1878">cmdlet `Invoke-AzDataBoxEdgeDevice` 추가됨</span><span class="sxs-lookup"><span data-stu-id="76011-1878">Added cmdlet `Invoke-AzDataBoxEdgeDevice`</span></span>
    - <span data-ttu-id="76011-1879">스캔 업데이트 호출, 업데이트 다운로드, 디바이스에 업데이트 설치</span><span class="sxs-lookup"><span data-stu-id="76011-1879">Invoke scan update, download update, install updates on the device</span></span>
* <span data-ttu-id="76011-1880">cmdlet `Get-AzDataBoxEdgeTrigger` 추가됨</span><span class="sxs-lookup"><span data-stu-id="76011-1880">Added cmdlet `Get-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="76011-1881">트리거에 대한 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="76011-1881">Gets the information about Triggers</span></span>
* <span data-ttu-id="76011-1882">cmdlet `New-AzDataBoxEdgeTrigger` 추가됨</span><span class="sxs-lookup"><span data-stu-id="76011-1882">Added cmdlet `New-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="76011-1883">새 트리거 만들기</span><span class="sxs-lookup"><span data-stu-id="76011-1883">Create new Triggers</span></span>
* <span data-ttu-id="76011-1884">cmdlet `Remove-AzDataBoxEdgeTrigger` 추가됨</span><span class="sxs-lookup"><span data-stu-id="76011-1884">Added cmdlet `Remove-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="76011-1885">트리거 제거</span><span class="sxs-lookup"><span data-stu-id="76011-1885">Remove the Triggers</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="76011-1886">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="76011-1886">Az.DataFactory</span></span>
* <span data-ttu-id="76011-1887">ADF .Net SDK 버전을 4.4.0으로 업데이트</span><span class="sxs-lookup"><span data-stu-id="76011-1887">Update ADF .Net SDK version to 4.4.0</span></span>
* <span data-ttu-id="76011-1888">'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd에 'ExpressCustomSetup' 매개 변수를 추가하여 사용자 지정 설치 스크립트 없이 설치 구성 및 타사 구성 요소를 사용하도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1888">Add parameter 'ExpressCustomSetup' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable setup configurations and 3rd party components without custom setup script.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="76011-1889">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="76011-1889">Az.DataLakeStore</span></span>
* <span data-ttu-id="76011-1890">Get-AzDataLakeStoreDeletedItem 및 Restore-AzDataLakeStoreDeletedItem의 설명서 업데이트</span><span class="sxs-lookup"><span data-stu-id="76011-1890">Update documentation of Get-AzDataLakeStoreDeletedItem and Restore-AzDataLakeStoreDeletedItem</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="76011-1891">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="76011-1891">Az.EventHub</span></span>
* <span data-ttu-id="76011-1892">10301 문제 해결: SAS 토큰 날짜 형식 수정</span><span class="sxs-lookup"><span data-stu-id="76011-1892">Fix for issue 10301 : Fix the SAS Token date format</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="76011-1893">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="76011-1893">Az.FrontDoor</span></span>
* <span data-ttu-id="76011-1894">Enable-AzFrontDoorCustomDomainHttps 및 New-AzFrontDoorFrontendEndpointObject에 MinimumTlsVersion 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="76011-1894">Add MinimumTlsVersion parameter to Enable-AzFrontDoorCustomDomainHttps and New-AzFrontDoorFrontendEndpointObject</span></span>
* <span data-ttu-id="76011-1895">New-AzFrontDoorHealthProbeSettingObject에 HealthProbeMethod 및 EnabledState 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="76011-1895">Add HealthProbeMethod and EnabledState parameters to New-AzFrontDoorHealthProbeSettingObject</span></span>
* <span data-ttu-id="76011-1896">BackendPoolsSettings 개체를 생성하여 Front Door 생성/업데이트에 전달하는 새 cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="76011-1896">Add new cmdlet to create BackendPoolsSettings objec to pass into creation/update of Front Door</span></span>
    - <span data-ttu-id="76011-1897">New-AzFrontDoorBackendPoolsSettingObject</span><span class="sxs-lookup"><span data-stu-id="76011-1897">New-AzFrontDoorBackendPoolsSettingObject</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="76011-1898">Az.Network</span><span class="sxs-lookup"><span data-stu-id="76011-1898">Az.Network</span></span>
* <span data-ttu-id="76011-1899">'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' 및 'Start-AzVirtualnetworkGatewayPacketCapture.md' FilterData 옵션 예제를 변경합니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1899">Change 'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' and 'Start-AzVirtualnetworkGatewayPacketCapture.md' FilterData option examples.</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="76011-1900">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="76011-1900">Az.PrivateDns</span></span>
* <span data-ttu-id="76011-1901">PrivateDns .net sdk를 버전 1.0.0으로 업데이트함</span><span class="sxs-lookup"><span data-stu-id="76011-1901">Updated PrivateDns .net sdk to version 1.0.0</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="76011-1902">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="76011-1902">Az.RecoveryServices</span></span>
* <span data-ttu-id="76011-1903">보호를 사용하도록 설정할 때 디스크 유형을 선택하도록 Azure Site Recovery 지원</span><span class="sxs-lookup"><span data-stu-id="76011-1903">Azure Site Recovery support to select disk type at enabling protection.</span></span>
* <span data-ttu-id="76011-1904">복구 계획 동작 편집을 위한 Azure Site Recovery 버그 수정</span><span class="sxs-lookup"><span data-stu-id="76011-1904">Azure Site Recovery bug fix for recovery plan action edit.</span></span>
* <span data-ttu-id="76011-1905">파일 스트림 DB를 허용하도록 Azure Backup SQL 복원 지원</span><span class="sxs-lookup"><span data-stu-id="76011-1905">Azure Backup SQL Restore support to accept filestream DBs.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="76011-1906">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="76011-1906">Az.RedisCache</span></span>
* <span data-ttu-id="76011-1907">'New-AzRedisCache' 및 'Set-AzRedisCache' cmdlet에 'MinimumTlsVersion' 매개 변수가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1907">Added 'MinimumTlsVersion' parameter in 'New-AzRedisCache' and 'Set-AzRedisCache' cmdlets.</span></span> <span data-ttu-id="76011-1908">'Get-AzRedisCache' cmdlet 출력에 'MinimumTlsVersion'도 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1908">Also, added 'MinimumTlsVersion' in the output of 'Get-AzRedisCache' cmdlet.</span></span>
* <span data-ttu-id="76011-1909">'Set-AzRedisCache' 및 'New-AzRedisCache' cmdlet의 '-Size' 매개 변수에 대한 유효성 검사가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1909">Added validation on '-Size' parameter for 'Set-AzRedisCache' and 'New-AzRedisCache' cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="76011-1910">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="76011-1910">Az.Resources</span></span>
- <span data-ttu-id="76011-1911">정책 할당에 새로운 EnforcementMode 속성이 있는 새 api 버전 2019-06-01을 사용하도록 정책 cmdlet이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1911">Updated policy cmdlets to use new api version 2019-06-01 that has new EnforcementMode property in policy assignment.</span></span>
- <span data-ttu-id="76011-1912">정책 정의 만들기 도움말 예제가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1912">Updated create policy definition help example</span></span>
- <span data-ttu-id="76011-1913">Remove-AZADServicePrincipal -ServicePrincipalName 버그를 수정하고, 서비스 사용자 이름을 찾을 수 없으면 null 참조를 throw합니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1913">Fix bug Remove-AZADServicePrincipal -ServicePrincipalName, throw null reference when service principal name not found.</span></span>
- <span data-ttu-id="76011-1914">New-AZADServicePrincipal 버그를 수정하고, 테넌트에 구독이 없으면 null 참조를 throw합니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1914">Fix bug New-AZADServicePrincipal, throw null reference when tenant doesn't have any subscription.</span></span>
- <span data-ttu-id="76011-1915">연결된 애플리케이션에만 자격 증명을 추가하도록 New-AzAdServicePrincipal을 변경합니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1915">Change New-AzAdServicePrincipal to add credentials only to associated application.</span></span>

#### <a name="azsql"></a><span data-ttu-id="76011-1916">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="76011-1916">Az.Sql</span></span>
* <span data-ttu-id="76011-1917">데이터베이스 ReadReplicaCount에 대한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1917">Added support for database ReadReplicaCount.</span></span>
* <span data-ttu-id="76011-1918">영역 중복이 설정되지 않은 경우 Set-AzSqlDatabase가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1918">Fixed Set-AzSqlDatabase when zone redundancy not set</span></span>

## <a name="300---november-2019"></a><span data-ttu-id="76011-1919">3.0.0 - 2019년 11월</span><span class="sxs-lookup"><span data-stu-id="76011-1919">3.0.0 - November 2019</span></span>
### <a name="general"></a><span data-ttu-id="76011-1920">일반</span><span class="sxs-lookup"><span data-stu-id="76011-1920">General</span></span>
* <span data-ttu-id="76011-1921">Az.PrivateDns 1.0.0 릴리스</span><span class="sxs-lookup"><span data-stu-id="76011-1921">Az.PrivateDns 1.0.0 released</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="76011-1922">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="76011-1922">Az.Accounts</span></span>
* <span data-ttu-id="76011-1923">'Resolve-Error' 별칭에 사용 중단 메시지를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1923">Add a deprecation message for 'Resolve-Error' alias.</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="76011-1924">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="76011-1924">Az.Advisor</span></span>
* <span data-ttu-id="76011-1925">Get-AzAdvisorRecommendation cmdlet에 새로운 '운영 효율성' 범주가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1925">Added new category 'Operational Excellence' to Get-AzAdvisorRecommendation cmdlet.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="76011-1926">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="76011-1926">Az.Batch</span></span>
* <span data-ttu-id="76011-1927">`BatchAccountContext`의 `CoreQuota` 이름이 `DedicatedCoreQuota`로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1927">Renamed `CoreQuota` on `BatchAccountContext` to `DedicatedCoreQuota`.</span></span> <span data-ttu-id="76011-1928">또한 `LowPriorityCoreQuota`가 새로 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1928">There is also a new `LowPriorityCoreQuota`.</span></span>
  - <span data-ttu-id="76011-1929">이 변경 사항은 **Get-AzBatchAccount** 에 영향을 줍니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1929">This impacts **Get-AzBatchAccount**.</span></span>
* <span data-ttu-id="76011-1930">이제 **New-AzBatchTask** `-ResourceFile` 매개 변수는 새로운 **New-AzBatchResourceFile** cmdlet을 사용하여 구성할 수 있는 `PSResourceFile` 개체의 컬렉션을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1930">**New-AzBatchTask** `-ResourceFile` parameter now takes a collection of `PSResourceFile` objects, which can be constructed using the new **New-AzBatchResourceFile** cmdlet.</span></span>
* <span data-ttu-id="76011-1931">새로운 **New-AzBatchResourceFile** cmdlet을 통해 `PSResourceFile` 개체를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1931">New **New-AzBatchResourceFile** cmdlet to help create `PSResourceFile` objects.</span></span> <span data-ttu-id="76011-1932">이들은 `-ResourceFile` 매개 변수의 **New-AzBatchTask** 에 제공될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1932">These can be supplied to **New-AzBatchTask** on the `-ResourceFile` parameter.</span></span>
  - <span data-ttu-id="76011-1933">그에 따라 기존 `HttpUrl` 방법 외에도 두 가지 종류의 리소스 파일이 새롭게 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1933">This supports two new kinds of resource file in addition to the existing `HttpUrl` way:</span></span>
    - <span data-ttu-id="76011-1934">`AutoStorageContainerName` 기반 리소스 파일은 전체 자동 스토리지 컨테이너를 일괄 처리 노드에 다운로드합니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1934">`AutoStorageContainerName` based resource files download an entire auto-storage container to the Batch node.</span></span>
    - <span data-ttu-id="76011-1935">`StorageContainerUrl` 기반 리소스 파일은 URL에 지정된 컨테이너를 일괄 처리 노드에 다운로드합니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1935">`StorageContainerUrl` based resource files download the container specified in the URL to the Batch node.</span></span>
* <span data-ttu-id="76011-1936">**Get-AzBatchApplication** 으로 반환되는 `PSApplication`의 `ApplicationPackages` 속성이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1936">Removed `ApplicationPackages` property of `PSApplication` returned by **Get-AzBatchApplication**.</span></span>
  - <span data-ttu-id="76011-1937">이제 **Get-AzBatchApplicationPackage** 를 사용하여 애플리케이션 내부의 특정 패키지를 검색할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1937">The specific packages inside of an application now can be retrieved using **Get-AzBatchApplicationPackage**.</span></span> <span data-ttu-id="76011-1938">예: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`</span><span class="sxs-lookup"><span data-stu-id="76011-1938">For example: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span></span>
* <span data-ttu-id="76011-1939">**Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication** 및 **Set-AzBatchApplication** 에서 `ApplicationId` 이름이 `ApplicationName`으로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1939">Renamed `ApplicationId` to `ApplicationName` on **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication**, and **Set-AzBatchApplication**.</span></span>
  - <span data-ttu-id="76011-1940">이제 `ApplicationId`는 `ApplicationName`의 별칭입니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1940">`ApplicationId` now is an alias of `ApplicationName`.</span></span>
* <span data-ttu-id="76011-1941">새로운 `PSWindowsUserConfiguration` 속성이 `PSUserAccount`에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1941">Added new `PSWindowsUserConfiguration` property to `PSUserAccount`.</span></span>
* <span data-ttu-id="76011-1942">`PSApplicationPackage`에서 `Version` 이름이 `Name`으로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1942">Renamed `Version` to `Name` on `PSApplicationPackage`.</span></span>
* <span data-ttu-id="76011-1943">`PSResourceFile`에서 `BlobSource` 이름이 `HttpUrl`으로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1943">Renamed `BlobSource` to `HttpUrl` on `PSResourceFile`.</span></span>
* <span data-ttu-id="76011-1944">`PSVirtualMachineConfiguration`에서 `OSDisk` 속성이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1944">Removed `OSDisk` property from `PSVirtualMachineConfiguration`.</span></span>
* <span data-ttu-id="76011-1945">**Set-AzBatchPoolOSVersion** 이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1945">Removed **Set-AzBatchPoolOSVersion**.</span></span> <span data-ttu-id="76011-1946">이 작업은 더 이상 지원되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1946">This operation is no longer supported.</span></span>
* <span data-ttu-id="76011-1947">`PSCloudServiceConfiguration`에서 `TargetOSVersion`이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1947">Removed `TargetOSVersion` from `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="76011-1948">`PSCloudServiceConfiguration`에서 `CurrentOSVersion` 이름이 `OSVersion`으로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1948">Renamed `CurrentOSVersion` to `OSVersion` on `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="76011-1949">`PSPoolUsageMetrics`에서 `DataEgressGiB` 및 `DataIngressGiB`가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1949">Removed `DataEgressGiB` and `DataIngressGiB` from `PSPoolUsageMetrics`.</span></span>
* <span data-ttu-id="76011-1950">**Get-AzBatchNodeAgentSku** 가 제거되고 **Get-AzBatchSupportedImage** 로 대체되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1950">Removed **Get-AzBatchNodeAgentSku** and replaced it with  **Get-AzBatchSupportedImage**.</span></span>
  - <span data-ttu-id="76011-1951">**Get-AzBatchSupportedImage** 가 **Get-AzBatchNodeAgentSku** 와 동일한 데이터를 반환하지만 더 친숙한 형식이 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1951">**Get-AzBatchSupportedImage** returns the same data as **Get-AzBatchNodeAgentSku** but in a more friendly format.</span></span>
  - <span data-ttu-id="76011-1952">이제 확인되지 않은 이미지도 새롭게 반환됩니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1952">New non-verified images are also now returned.</span></span> <span data-ttu-id="76011-1953">각 이미지의 `Capabilities` 및 `BatchSupportEndOfLife`에 대한 추가 정보도 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1953">Additional information about `Capabilities` and `BatchSupportEndOfLife` for each image is also included.</span></span>
* <span data-ttu-id="76011-1954">**New-AzBatchPool** 의 새로운 `MountConfiguration` 매개 변수를 통해 풀의 각 노드에서 원격 파일 시스템을 마운트할 수 있는 기능이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1954">Added ability to mount remote file-systems on each node of a pool via the new `MountConfiguration` parameter of **New-AzBatchPool**.</span></span>
* <span data-ttu-id="76011-1955">이제 트래픽의 소스 포트를 기준으로 풀에 대한 네트워크 액세스를 차단하는 네트워크 보안 규칙이 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1955">Now support network security rules blocking network access to a pool based on the source port of the traffic.</span></span> <span data-ttu-id="76011-1956">이 작업은 `PSNetworkSecurityGroupRule`에서 `SourcePortRanges` 속성을 통해 수행됩니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1956">This is done via the `SourcePortRanges` property on `PSNetworkSecurityGroupRule`.</span></span>
* <span data-ttu-id="76011-1957">컨테이너를 실행할 때 Batch는 이제 컨테이너 작업 디렉터리 또는 일괄 처리 태스크 작업 디렉터리에서 작업 실행을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1957">When running a container, Batch now supports executing the task in the container working directory or in the Batch task working directory.</span></span> <span data-ttu-id="76011-1958">이 작업은 `PSTaskContainerSettings`에서 `WorkingDirectory` 속성에 의해 제어됩니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1958">This is controlled by the `WorkingDirectory` property on `PSTaskContainerSettings`.</span></span>
* <span data-ttu-id="76011-1959">새로운 `PublicIPs` 속성을 통해 `PSNetworkConfiguration`에서 공용 IP의 컬렉션을 지정할 수 있는 기능이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1959">Added ability to specify a collection of public IPs on `PSNetworkConfiguration` via the new `PublicIPs` property.</span></span> <span data-ttu-id="76011-1960">그 결과 사용자 제공 IP 목록의 IP가 풀에 있는 노드에 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1960">This guarantees nodes in the Pool will have an IP from the list user provided IPs.</span></span>
* <span data-ttu-id="76011-1961">지정하지 않은 경우 이제 `PSSTartTask`에서 `WaitForSuccess`의 기본값은 `$True`입니다(이전에는 `$False`).</span><span class="sxs-lookup"><span data-stu-id="76011-1961">When not specified, the default value of `WaitForSuccess` on `PSSTartTask` is now `$True` (was `$False`).</span></span>
* <span data-ttu-id="76011-1962">지정하지 않은 경우 이제 `PSAutoUserSpecification`에서 `Scope`의 기본값은 `Pool`입니다(이전에는 Windows의 경우 `Task`, Linux의 경우에는 `Pool`).</span><span class="sxs-lookup"><span data-stu-id="76011-1962">When not specified, the default value of `Scope` on `PSAutoUserSpecification` is now `Pool` (was `Task` on Windows and `Pool` on Linux).</span></span>

#### <a name="azcdn"></a><span data-ttu-id="76011-1963">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="76011-1963">Az.Cdn</span></span>
* <span data-ttu-id="76011-1964">RulesEngine에 UrlRewriteAction 및 CacheKeyQueryStringAction이 도입되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1964">Introduced UrlRewriteAction and CacheKeyQueryStringAction to RulesEngine.</span></span>
* <span data-ttu-id="76011-1965">New-AzDeliveryRuleCondition cmdlet에서 'Selector' 입력 누락과 같은 여러 버그가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1965">Fixed several bugs like missing 'Selector' Input in New-AzDeliveryRuleCondition cmdlet.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="76011-1966">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="76011-1966">Az.Compute</span></span>
* <span data-ttu-id="76011-1967">디스크 암호화 집합 기능</span><span class="sxs-lookup"><span data-stu-id="76011-1967">Disk Encryption Set feature</span></span>
    - <span data-ttu-id="76011-1968">새 cmdlet:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="76011-1968">New cmdlets:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span></span>
    - <span data-ttu-id="76011-1969">DiskEncryptionSetId 매개 변수가 다음 cmdlet에 추가되었습니다.   Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="76011-1969">DiskEncryptionSetId parameter is added to the following cmdlets:   Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span></span>
    - <span data-ttu-id="76011-1970">DiskEncryptionSetId 및 EncryptionType 매개 변수가 다음 cmdlet에 추가되었습니다.   New-AzDiskConfig   New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="76011-1970">DiskEncryptionSetId and EncryptionType parameters are added to the following cmdlets:   New-AzDiskConfig   New-AzSnapshotConfig</span></span>
* <span data-ttu-id="76011-1971">New-AzVmssIPConfig에 PublicIPAddressVersion 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="76011-1971">Add PublicIPAddressVersion parameter to New-AzVmssIPConfig</span></span>
* <span data-ttu-id="76011-1972">사용자 지정 스크립트 확장의 FileUris를 공용 설정에서 보호된 설정으로 이동</span><span class="sxs-lookup"><span data-stu-id="76011-1972">Move FileUris of custom script extension from public setting to protected setting</span></span>
* <span data-ttu-id="76011-1973">New-AzVmss, New-AzVmssConfig 및 Update-AzVmss cmdlet에 ScaleInPolicy 추가</span><span class="sxs-lookup"><span data-stu-id="76011-1973">Add ScaleInPolicy to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>
* <span data-ttu-id="76011-1974">주요 변경 내용</span><span class="sxs-lookup"><span data-stu-id="76011-1974">Breaking changes</span></span>
    - <span data-ttu-id="76011-1975">CreateOption이 업로드일 때 UploadSizeInBytes 매개 변수가 New-AzDiskConfig에 대해 DiskSizeGB 대신 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1975">UploadSizeInBytes parameter is used instead of DiskSizeGB for New-AzDiskConfig when CreateOption is Upload</span></span>
    - <span data-ttu-id="76011-1976">GalleryImageVersion 개체에서 PublishingProfile.Source.ManagedImage.Id가 StorageProfile.Source.Id로 바뀝니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1976">PublishingProfile.Source.ManagedImage.Id is replaced with StorageProfile.Source.Id in GalleryImageVersion object</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="76011-1977">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="76011-1977">Az.DataFactory</span></span>
* <span data-ttu-id="76011-1978">ADF .Net SDK 버전을 4.3.0으로 업데이트</span><span class="sxs-lookup"><span data-stu-id="76011-1978">Update ADF .Net SDK version to 4.3.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="76011-1979">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="76011-1979">Az.DataLakeStore</span></span>
* <span data-ttu-id="76011-1980">ADLS SDK 버전 업데이트(https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha) , 다음 수정 사항 제공</span><span class="sxs-lookup"><span data-stu-id="76011-1980">Update ADLS SDK version (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), brings following fixes</span></span>
* <span data-ttu-id="76011-1981">휴지통 또는 디렉터리 항목의 creationtime을 역직렬화할 수 없을 때 예외가 발생하지 않도록 방지합니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1981">Avoid throwing exception while unable to deserialize the creationtime of the trash or directory entry.</span></span>
* <span data-ttu-id="76011-1982">adlsclient에서 요청별 시간 제한 설정 노출</span><span class="sxs-lookup"><span data-stu-id="76011-1982">Expose setting per request timeout in adlsclient</span></span>
* <span data-ttu-id="76011-1983">badoffset 복구를 위한 원본 syncflag 전달 수정</span><span class="sxs-lookup"><span data-stu-id="76011-1983">Fix passing the original syncflag for badoffset recovery</span></span>
* <span data-ttu-id="76011-1984">응답이 확인된 후 연속 토큰을 검색하기 위한 EnumerateDirectory 수정</span><span class="sxs-lookup"><span data-stu-id="76011-1984">Fix EnumerateDirectory to retrieve continuation token once response is checked</span></span>
* <span data-ttu-id="76011-1985">Concat 버그 수정</span><span class="sxs-lookup"><span data-stu-id="76011-1985">Fix Concat Bug</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="76011-1986">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="76011-1986">Az.FrontDoor</span></span>
* <span data-ttu-id="76011-1987">모듈 간 기타 오타가 수정됨</span><span class="sxs-lookup"><span data-stu-id="76011-1987">Fixed miscellaneous typos across module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="76011-1988">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="76011-1988">Az.HDInsight</span></span>
* <span data-ttu-id="76011-1989">ADLSGen1 스토리지가 포함된 클러스터를 가져오기 위해 Get-AzHDInsightCluster를 사용할 때 고객에게 '올바른 Base-64 문자열이 아닙니다' 오류가 표시되는 버그가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1989">Fixed the bug that customer will get 'Not a valid Base-64 string' error when using Get-AzHDInsightCluster to get the cluster with ADLSGen1 storage.</span></span>
* <span data-ttu-id="76011-1990">고객이 Azure Data Lake에 액세스하기 위해 서비스 주체 애플리케이션 ID를 제공할 수 있도록 세 가지 cmdlet Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig 및 New-AzHDInsightCluster에 이름이 'ApplicationId'인 매개 변수를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1990">Add a parameter named 'ApplicationId' to three cmdlets Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig and New-AzHDInsightCluster so that customer can provide the service principal application id for accessing Azure Data Lake.</span></span>
* <span data-ttu-id="76011-1991">Microsoft.Azure.Management.HDInsight가 2.1.0에서 5.1.0으로 변경됨</span><span class="sxs-lookup"><span data-stu-id="76011-1991">Changed Microsoft.Azure.Management.HDInsight from 2.1.0 to 5.1.0</span></span>
* <span data-ttu-id="76011-1992">다음 5가지 cmdlet이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1992">Removed five cmdlets:</span></span>
    - <span data-ttu-id="76011-1993">Get-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="76011-1993">Get-AzHDInsightOMS</span></span>
    - <span data-ttu-id="76011-1994">Enable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="76011-1994">Enable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="76011-1995">Disable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="76011-1995">Disable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="76011-1996">Grant-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="76011-1996">Grant-AzHDInsightRdpServicesAccess</span></span>
    - <span data-ttu-id="76011-1997">Revoke-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="76011-1997">Revoke-AzHDInsightRdpServicesAccess</span></span>
* <span data-ttu-id="76011-1998">다음 3가지 cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-1998">Added three cmdlets:</span></span>
    - <span data-ttu-id="76011-1999">Get-AzHDInsightOMS 대신 Get-AzHDInsightMonitoring</span><span class="sxs-lookup"><span data-stu-id="76011-1999">Get-AzHDInsightMonitoring to replace Get-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="76011-2000">Get-AzHDInsightOMS 대신 Get-AzHDInsightMonitoring</span><span class="sxs-lookup"><span data-stu-id="76011-2000">Enable-AzHDInsightMonitoring to replace Enable-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="76011-2001">Disable-AzHDInsightOMS 대신 Disable-AzHDInsightMonitoring</span><span class="sxs-lookup"><span data-stu-id="76011-2001">Disable-AzHDInsightMonitoring to replace Disable-AzHDInsightOMS.</span></span>
* <span data-ttu-id="76011-2002">특정 위치의 기능 정보 가져오기를 지원하도록 cmdlet Get-AzHDInsightProperties가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2002">Fixed cmdlet Get-AzHDInsightProperties to support get capabilities information from a specific location.</span></span>
* <span data-ttu-id="76011-2003">Add-AzHDInsightConfigValue에서 매개 변수 집합('Spark1', 'Spark2')이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2003">Removed parameter sets('Spark1', 'Spark2') from Add-AzHDInsightConfigValue.</span></span>
* <span data-ttu-id="76011-2004">cmdlet Add-AzHDInsightSecurityProfile의 도움말 문서에 예제를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2004">Add examples to the help documents of cmdlet Add-AzHDInsightSecurityProfile.</span></span>
* <span data-ttu-id="76011-2005">다음 cmdlet의 출력 유형이 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2005">Changed output type of the following cmdlets:</span></span>
*  - <span data-ttu-id="76011-2006">Get-AzHDInsightProperties의 출력 유형이 CapabilitiesResponse에서 AzureHDInsightCapabilities로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2006">Changed the output type of Get-AzHDInsightProperties from  CapabilitiesResponse to AzureHDInsightCapabilities.</span></span>
*  - <span data-ttu-id="76011-2007">Remove-AzHDInsightCluster의 출력 유형이 ClusterGetResponse에서 bool로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2007">Changed the output type of Remove-AzHDInsightCluster from ClusterGetResponse to bool.</span></span>
*  - <span data-ttu-id="76011-2008">Set-AzHDInsightGatewaySettings의 출력 유형이 HttpConnectivitySettings에서 GatewaySettings로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2008">Changed the output type of Set-AzHDInsightGatewaySettings HttpConnectivitySettings to GatewaySettings.</span></span>
* <span data-ttu-id="76011-2009">몇 가지 시나리오 테스트 사례가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2009">Added some scenario test cases.</span></span>
* <span data-ttu-id="76011-2010">일부 별칭 제거: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span><span class="sxs-lookup"><span data-stu-id="76011-2010">Remove some alias: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="76011-2011">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="76011-2011">Az.IotHub</span></span>
* <span data-ttu-id="76011-2012">주요 변경 내용:</span><span class="sxs-lookup"><span data-stu-id="76011-2012">Breaking changes:</span></span>
    - <span data-ttu-id="76011-2013">'Add-AzIotHubEventHubConsumerGroup' cmdlet이 'EventHubEndpointName' 매개 변수를 더 이상 지원하지 않으며 원래 매개 변수 이름에 대해 별칭을 찾을 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2013">The cmdlet 'Add-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="76011-2014">'Add-AzIotHubEventHubConsumerGroup' cmdlet에 대한 매개 변수 집합 '__AllParameterSets'가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2014">The parameter set '__AllParameterSets' for cmdlet 'Add-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="76011-2015">'Get-AzIotHubEventHubConsumerGroup' cmdlet이 'EventHubEndpointName' 매개 변수를 더 이상 지원하지 않으며 원래 매개 변수 이름에 대해 별칭을 찾을 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2015">The cmdlet 'Get-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="76011-2016">'Get-AzIotHubEventHubConsumerGroup' cmdlet에 대한 매개 변수 집합 '__AllParameterSets'가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2016">The parameter set '__AllParameterSets' for cmdlet 'Get-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="76011-2017">'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' 유형의 'OperationsMonitoringProperties' 속성이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2017">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' has been removed.</span></span>
    - <span data-ttu-id="76011-2018">'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' 유형의 'OperationsMonitoringProperties' 속성이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2018">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' has been removed.</span></span>
    - <span data-ttu-id="76011-2019">'New-AzIotHubExportDevice' cmdlet이 더 이상 'New-AzIotHubExportDevices' 별칭을 지원하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2019">The cmdlet 'New-AzIotHubExportDevice' no longer supports the alias 'New-AzIotHubExportDevices'.</span></span>
    - <span data-ttu-id="76011-2020">'New-AzIotHubImportDevice' cmdlet이 더 이상 'New-AzIotHubImportDevices' 별칭을 지원하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2020">The cmdlet 'New-AzIotHubImportDevice' no longer supports the alias 'New-AzIotHubImportDevices'.</span></span>
    - <span data-ttu-id="76011-2021">'Remove-AzIotHubEventHubConsumerGroup' cmdlet이 'EventHubEndpointName' 매개 변수를 더 이상 지원하지 않으며 원래 매개 변수 이름에 대해 별칭을 찾을 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2021">The cmdlet 'Remove-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="76011-2022">'Remove-AzIotHubEventHubConsumerGroup' cmdlet에 대한 매개 변수 집합 '__AllParameterSets'가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2022">The parameter set '__AllParameterSets' for cmdlet 'Remove-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="76011-2023">'Set-AzIotHub' cmdlet이 'OperationsMonitoringProperties' 매개 변수를 더 이상 지원하지 않으며 원래 매개 변수 이름에 대해 별칭을 찾을 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2023">The cmdlet 'Set-AzIotHub' no longer supports the parameter 'OperationsMonitoringProperties' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="76011-2024">'Set-AzIotHub' cmdlet에 대한 매개 변수 집합 'UpdateOperationsMonitoringProperties'가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2024">The parameter set 'UpdateOperationsMonitoringProperties' for cmdlet 'Set-AzIotHub' has been removed.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="76011-2025">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="76011-2025">Az.RecoveryServices</span></span>
* <span data-ttu-id="76011-2026">Azure Site Recovery가 Azure-Azure를 위한 NSG, 공용 IP 및 내부 부하 분산 장치와 같은 네트워킹 리소스 구성을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2026">Azure Site Recovery support to configure networking resources like NSG, public IP and internal load balancers for Azure to Azure.</span></span>
* <span data-ttu-id="76011-2027">Azure Site Recovery가 vMWare-Azure를 위한 관리 디스크에 쓰기를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2027">Azure Site Recovery Support to write to managed disk for vMWare to Azure.</span></span>
* <span data-ttu-id="76011-2028">Azure Site Recovery가 vMWare-Azure를 위한 NIC 감소를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2028">Azure Site Recovery Support to NIC reduction for vMWare to Azure.</span></span>
* <span data-ttu-id="76011-2029">Azure Site Recovery가 Azure-Azure를 위한 가속 네트워킹을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2029">Azure Site Recovery Support to accelerated networking for Azure to Azure.</span></span>
* <span data-ttu-id="76011-2030">Azure Site Recovery가 Azure-Azure를 위한 에이전트 자동 업데이트를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2030">Azure Site Recovery Support to agent auto update for Azure to Azure.</span></span>
* <span data-ttu-id="76011-2031">Azure Site Recovery가 Azure-Azure를 위한 표준 SSD를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2031">Azure Site Recovery Support to Standard SSD for Azure to Azure.</span></span>
* <span data-ttu-id="76011-2032">Azure Site Recovery가 Azure-Azure를 위한 두 가지 Azure 디스크 암호화 전달을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2032">Azure Site Recovery Support to Azure Disk Encryption two pass for Azure to Azure.</span></span>
* <span data-ttu-id="76011-2033">Azure Site Recovery가 Azure-Azure를 위한 새로 추가된 디스크 보호를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2033">Azure Site Recovery Support to protect newly added disk for Azure to Azure.</span></span>
* <span data-ttu-id="76011-2034">VM을 위한 SoftDelete 기능 및 softdelete를 위한 테스트가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2034">Added SoftDelete feature for VM and added tests for softdelete</span></span>

#### <a name="azresources"></a><span data-ttu-id="76011-2035">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="76011-2035">Az.Resources</span></span>
* <span data-ttu-id="76011-2036">종속성 어셈블리 Microsoft.Extensions.Caching.Memory가 1.1.1에서 2.2로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2036">Update dependency assembly Microsoft.Extensions.Caching.Memory from 1.1.1 to 2.2</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="76011-2037">Az.Network</span><span class="sxs-lookup"><span data-stu-id="76011-2037">Az.Network</span></span>
* <span data-ttu-id="76011-2038">일반 서비스 공급자 지원을 위해 PrivateEndpointConnection에 대한 모든 cmdlet이 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2038">Change all cmdlets for PrivateEndpointConnection to support generic service provider.</span></span>
    - <span data-ttu-id="76011-2039">업데이트된 cmdlet:</span><span class="sxs-lookup"><span data-stu-id="76011-2039">Updated cmdlet:</span></span>
        - <span data-ttu-id="76011-2040">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="76011-2040">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="76011-2041">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="76011-2041">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="76011-2042">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="76011-2042">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="76011-2043">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="76011-2043">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="76011-2044">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="76011-2044">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="76011-2045">PrivateLinkResource에 대한 새 cmdlet이 추가되었고 일반 서비스 공급자도 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2045">Add new cmdlet for PrivateLinkResource and it also support generic service provider.</span></span>
    - <span data-ttu-id="76011-2046">새 cmdlet:</span><span class="sxs-lookup"><span data-stu-id="76011-2046">New cmdlet:</span></span>
        - <span data-ttu-id="76011-2047">Get-AzPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="76011-2047">Get-AzPrivateLinkResource</span></span>
* <span data-ttu-id="76011-2048">Proxy Protocol V2 기능에 대한 새 필드 및 매개 변수가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2048">Add new fields and parameter for the feature Proxy Protocol V2.</span></span>
    - <span data-ttu-id="76011-2049">PrivateLinkService에서 EnableProxyProtocol 속성 추가</span><span class="sxs-lookup"><span data-stu-id="76011-2049">Add property EnableProxyProtocol in PrivateLinkService</span></span>
    - <span data-ttu-id="76011-2050">PrivateEndpointConnection에서 LinkIdentifier 속성 추가</span><span class="sxs-lookup"><span data-stu-id="76011-2050">Add property LinkIdentifier in PrivateEndpointConnection</span></span>
    - <span data-ttu-id="76011-2051">새로운 선택적인 매개 변수인 EnableProxyProtocol을 추가하도록 New-AzPrivateLinkService가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2051">Updated New-AzPrivateLinkService to add a new optional parameter EnableProxyProtocol.</span></span>
* <span data-ttu-id="76011-2052">'New-AzApplicationGatewaySku' 참조 설명서의 잘못된 매개 변수 설명 수정</span><span class="sxs-lookup"><span data-stu-id="76011-2052">Fix incorrect parameter description in 'New-AzApplicationGatewaySku' reference documentation</span></span>
* <span data-ttu-id="76011-2053">Azure 방화벽 정책을 지원하는 새로운 cmdlet</span><span class="sxs-lookup"><span data-stu-id="76011-2053">New cmdlets to support the azure firewall policy</span></span>
* <span data-ttu-id="76011-2054">VirtualHub의 자식 리소스 RouteTables에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="76011-2054">Add support for child resource RouteTables of VirtualHub</span></span>
    - <span data-ttu-id="76011-2055">추가된 새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2055">New cmdlets added:</span></span>
        - <span data-ttu-id="76011-2056">Add-AzVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="76011-2056">Add-AzVirtualHubRoute</span></span>
        - <span data-ttu-id="76011-2057">Add-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="76011-2057">Add-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="76011-2058">Get-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="76011-2058">Get-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="76011-2059">Remove-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="76011-2059">Remove-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="76011-2060">Set-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="76011-2060">Set-AzVirtualHub</span></span>
* <span data-ttu-id="76011-2061">VirtualHub의 새로운 속성 Sku 및 VirtualWan의 VirtualWANType에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="76011-2061">Add support for new properties Sku of VirtualHub and VirtualWANType of VirtualWan</span></span>
    - <span data-ttu-id="76011-2062">선택적 매개 변수로 다음 cmdlet이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2062">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="76011-2063">New-AzVirtualHub: 추가된 매개 변수 Sku</span><span class="sxs-lookup"><span data-stu-id="76011-2063">New-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="76011-2064">Update-AzVirtualHub: 추가된 매개 변수 Sku</span><span class="sxs-lookup"><span data-stu-id="76011-2064">Update-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="76011-2065">New-AzVirtualWan: 추가된 매개 변수 VirtualWANType</span><span class="sxs-lookup"><span data-stu-id="76011-2065">New-AzVirtualWan : added parameter VirtualWANType</span></span>
        - <span data-ttu-id="76011-2066">Update-AzVirtualWan: 추가된 매개 변수 VirtualWANType</span><span class="sxs-lookup"><span data-stu-id="76011-2066">Update-AzVirtualWan : added parameter VirtualWANType</span></span>
* <span data-ttu-id="76011-2067">HubVnetConnection, VpnConnection 및 ExpressRouteConnection에 대한 EnableInternetSecurity 속성 지원 추가</span><span class="sxs-lookup"><span data-stu-id="76011-2067">Add support for EnableInternetSecurity property for HubVnetConnection, VpnConnection and ExpressRouteConnection</span></span>
    - <span data-ttu-id="76011-2068">추가된 새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2068">New cmdlets added:</span></span>
        - <span data-ttu-id="76011-2069">Update-AzureRmVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="76011-2069">Update-AzureRmVirtualHubVnetConnection</span></span>
    - <span data-ttu-id="76011-2070">선택적 매개 변수로 다음 cmdlet이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2070">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="76011-2071">New-AzureRmVirtualHubVnetConnection: 추가된 매개 변수 EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="76011-2071">New-AzureRmVirtualHubVnetConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="76011-2072">New-AzureRmVpnConnection: 추가된 매개 변수 EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="76011-2072">New-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="76011-2073">Update-AzureRmVpnConnection: 추가된 매개 변수 EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="76011-2073">Update-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="76011-2074">New-AzureRmExpressRouteConnection: 추가된 매개 변수 EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="76011-2074">New-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="76011-2075">Set-AzureRmExpressRouteConnection: 추가된 매개 변수 EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="76011-2075">Set-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
* <span data-ttu-id="76011-2076">TopLevel WebApplicationFirewall 정책 구성을 위한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="76011-2076">Add support for Configuring TopLevel WebApplicationFirewall Policy</span></span>
    - <span data-ttu-id="76011-2077">추가된 새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2077">New cmdlets added:</span></span>
        - <span data-ttu-id="76011-2078">New-AzApplicationGatewayFirewallPolicySetting</span><span class="sxs-lookup"><span data-stu-id="76011-2078">New-AzApplicationGatewayFirewallPolicySetting</span></span>
        - <span data-ttu-id="76011-2079">New-AzApplicationGatewayFirewallPolicyExclusion</span><span class="sxs-lookup"><span data-stu-id="76011-2079">New-AzApplicationGatewayFirewallPolicyExclusion</span></span>
        - <span data-ttu-id="76011-2080">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="76011-2080">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span></span>
        - <span data-ttu-id="76011-2081">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="76011-2081">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span></span>
        - <span data-ttu-id="76011-2082">New-AzApplicationGatewayFirewallPolicyManagedRule</span><span class="sxs-lookup"><span data-stu-id="76011-2082">New-AzApplicationGatewayFirewallPolicyManagedRule</span></span>
        - <span data-ttu-id="76011-2083">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="76011-2083">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span></span>
    - <span data-ttu-id="76011-2084">선택적 매개 변수로 다음 cmdlet이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2084">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="76011-2085">New-AzApplicationGatewayFirewallPolicy: 추가된 매개 변수 PolicySetting, ManagedRule</span><span class="sxs-lookup"><span data-stu-id="76011-2085">New-AzApplicationGatewayFirewallPolicy : added parameter PolicySetting, ManagedRule</span></span>
* <span data-ttu-id="76011-2086">CustomRule에서 Geo-Match 연산자를 위한 지원 추가됨</span><span class="sxs-lookup"><span data-stu-id="76011-2086">Added support for Geo-Match operator on CustomRule</span></span>
    - <span data-ttu-id="76011-2087">FirewallCondition에서 연산자에 GeoMatch 추가됨</span><span class="sxs-lookup"><span data-stu-id="76011-2087">Added GeoMatch to the operator on the FirewallCondition</span></span>
* <span data-ttu-id="76011-2088">perListener 및 perSite 방화벽 규칙에 대한 지원 추가됨</span><span class="sxs-lookup"><span data-stu-id="76011-2088">Added support for perListener and perSite Firewall policy</span></span>
    - <span data-ttu-id="76011-2089">선택적 매개 변수로 다음 cmdlet이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2089">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="76011-2090">New-AzApplicationGatewayHttpListener: 추가된 매개 변수 FirewallPolicy, FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="76011-2090">New-AzApplicationGatewayHttpListener : added parameter FirewallPolicy, FirewallPolicyId</span></span>
        - <span data-ttu-id="76011-2091">New-AzApplicationGatewayPathRuleConfig: 추가된 매개 변수 FirewallPolicy, FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="76011-2091">New-AzApplicationGatewayPathRuleConfig : added parameter FirewallPolicy, FirewallPolicyId</span></span>
* <span data-ttu-id="76011-2092">'PSBastion'에서 이름이 AzureBastionSubnet인 필수 서브넷의 수정은 대소문자를 구분하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2092">Fix required subnet with name AzureBastionSubnet in 'PSBastion' can be case insensitive</span></span>
* <span data-ttu-id="76011-2093">Azure Firewall을 위한 네트워크 규칙의 대상 FQDN 및 NAT 규칙의 번역된 FQDN 지원</span><span class="sxs-lookup"><span data-stu-id="76011-2093">Support for Destination FQDNs in Network Rules and Translated FQDN in NAT Rules for Azure Firewall</span></span>
* <span data-ttu-id="76011-2094">IpGroup의 최상위 리소스 RouteTables에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="76011-2094">Add support for top level resource RouteTables of IpGroup</span></span>
    - <span data-ttu-id="76011-2095">추가된 새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2095">New cmdlets added:</span></span>
        - <span data-ttu-id="76011-2096">New-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="76011-2096">New-AzIpGroup</span></span>
        - <span data-ttu-id="76011-2097">Remove-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="76011-2097">Remove-AzIpGroup</span></span>
        - <span data-ttu-id="76011-2098">Get-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="76011-2098">Get-AzIpGroup</span></span>
        - <span data-ttu-id="76011-2099">Set-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="76011-2099">Set-AzIpGroup</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="76011-2100">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="76011-2100">Az.ServiceFabric</span></span>
* <span data-ttu-id="76011-2101">Add-AzVmssSecret에서 지원되기 때문에 Add-AzServiceFabricApplicationCertificate cmdlet이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2101">Remove Add-AzServiceFabricApplicationCertificate cmdlet as this scenario is covered by Add-AzVmssSecret.</span></span>

#### <a name="azsql"></a><span data-ttu-id="76011-2102">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="76011-2102">Az.Sql</span></span>
* <span data-ttu-id="76011-2103">Managed Instances에서 삭제된 데이터베이스의 복원을 위한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2103">Added support for restore of dropped databases on Managed Instances.</span></span>
* <span data-ttu-id="76011-2104">이전의 감사 cmdlet 코드가 사용되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2104">Deprecated from code old auditing cmdlets.</span></span>
* <span data-ttu-id="76011-2105">사용되지 않는 별칭이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2105">Removed deprecated aliases:</span></span>
* <span data-ttu-id="76011-2106">Get-AzSqlDatabaseIndexRecommendations(대신 Get-AzSqlDatabaseIndexRecommendation 사용)</span><span class="sxs-lookup"><span data-stu-id="76011-2106">Get-AzSqlDatabaseIndexRecommendations (use Get-AzSqlDatabaseIndexRecommendation instead)</span></span>
* <span data-ttu-id="76011-2107">Get-AzSqlDatabaseRestorePoints(대신 Get-AzSqlDatabaseRestorePoint 사용)</span><span class="sxs-lookup"><span data-stu-id="76011-2107">Get-AzSqlDatabaseRestorePoints (use Get-AzSqlDatabaseRestorePoint instead)</span></span>
* <span data-ttu-id="76011-2108">Get-AzSqlDatabaseSecureConnectionPolicy cmdlet 제거</span><span class="sxs-lookup"><span data-stu-id="76011-2108">Remove Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="76011-2109">사용되지 않는 취약성 평가 설정 cmdlet에 대한 별칭 제거</span><span class="sxs-lookup"><span data-stu-id="76011-2109">Remove aliases for deprecated Vulnerability Assessment Settings cmdlets</span></span>
* <span data-ttu-id="76011-2110">지능형 위협 탐지 설정 cmdlet 사용 중단</span><span class="sxs-lookup"><span data-stu-id="76011-2110">Deprecate Advanced Threat Detection Settings cmdlets</span></span>
* <span data-ttu-id="76011-2111">데이터베이스의 열에 대한 민감도 권장 사항의 사용 여부를 제어하는 cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2111">Adding cmdlets to Disable and enable sensitivity recommendations on columns in a database.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="76011-2112">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="76011-2112">Az.Storage</span></span>
* <span data-ttu-id="76011-2113">스토리지 계정을 만들거나 업데이트할 때 큰 파일 공유 사용 지원</span><span class="sxs-lookup"><span data-stu-id="76011-2113">Support enable Large File share when create or update Storage account</span></span>
    -  <span data-ttu-id="76011-2114">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="76011-2114">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="76011-2115">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="76011-2115">Set-AzStorageAccount</span></span>
* <span data-ttu-id="76011-2116">파일 핸들을 닫거나/가져올 때, DeletePending 상태의 개체로 인한 오류를 방지하기 위해 입력 경로가 파일 디렉터리인지 또는 파일인지를 확인하는 과정을 건너뜁니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2116">When close/get File handle, skip check the input path is File directory or File, to avoid failure with object in DeletePending status</span></span>
    -  <span data-ttu-id="76011-2117">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="76011-2117">Get-AzStorageFileHandle</span></span>
    -  <span data-ttu-id="76011-2118">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="76011-2118">Close-AzStorageFileHandle</span></span>

## <a name="280---october-2019"></a><span data-ttu-id="76011-2119">2.8.0 - 2019년 10월</span><span class="sxs-lookup"><span data-stu-id="76011-2119">2.8.0 - October 2019</span></span>
### <a name="general"></a><span data-ttu-id="76011-2120">일반</span><span class="sxs-lookup"><span data-stu-id="76011-2120">General</span></span>
* <span data-ttu-id="76011-2121">Az.HealthcareApis 1.0.0 릴리스</span><span class="sxs-lookup"><span data-stu-id="76011-2121">Az.HealthcareApis 1.0.0 release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="76011-2122">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="76011-2122">Az.Accounts</span></span>
* <span data-ttu-id="76011-2123">생성된 모듈에 대한 원격 분석 및 URL 다시 작성이 업데이트되고, Windows 단위 테스트가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2123">Update telemetry and url rewriting for generated modules, fix windows unit tests.</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="76011-2124">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="76011-2124">Az.ApiManagement</span></span>
* <span data-ttu-id="76011-2125">**Set-AzApiManagementApi** - API 업데이트 지원이 ApiVersionSet에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2125">**Set-AzApiManagementApi** - Added support for Updating Api into ApiVersionSet</span></span>
    - <span data-ttu-id="76011-2126">문제 https://github.com/Azure/azure-powershell/issues/10068 수정</span><span class="sxs-lookup"><span data-stu-id="76011-2126">Fix for issue https://github.com/Azure/azure-powershell/issues/10068</span></span>

#### <a name="azautomation"></a><span data-ttu-id="76011-2127">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="76011-2127">Az.Automation</span></span>
* <span data-ttu-id="76011-2128">Linux 다시 부팅 설정 매개 변수에 대한 New-AzureAutomationSoftwareUpdateConfiguration cmdlet이 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2128">Fixed New-AzureAutomationSoftwareUpdateConfiguration cmdlet for Linux reboot setting parameter.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="76011-2129">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="76011-2129">Az.Batch</span></span>
* <span data-ttu-id="76011-2130">**Get-AzBatchNodeAgentSku** 가 더 이상 사용되지 않으며, 2.0.0 버전의 **Get-AzBatchSupportImage** 로 대체되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2130">**Get-AzBatchNodeAgentSku** is deprecated and will be replaced by **Get-AzBatchSupportImage** in version 2.0.0.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="76011-2131">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="76011-2131">Az.Compute</span></span>
* <span data-ttu-id="76011-2132">Priority, EvictionPolicy 및 MaxPrice 매개 변수가 New-AzVM 및 New-AzVmss cmdlet에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2132">Add Priority, EvictionPolicy, and MaxPrice parameters to New-AzVM and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="76011-2133">Add-AzVMAdditionalUnattendContent 및 Add-AzVMSshPublicKey cmdlet에 대한 경고 메시지와 도움말 문서가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2133">Fix warning message and help document for Add-AzVMAdditionalUnattendContent and Add-AzVMSshPublicKey cmdlets</span></span>
* <span data-ttu-id="76011-2134">Set-AzVMDiskEncryptionExtension의 관리 디스크가 있는 Linux VM에 대한 -skipVmBackup 예외가 해결되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2134">Fix -skipVmBackup exception for Linux VMs with managed disks for Set-AzVMDiskEncryptionExtension.</span></span>
* <span data-ttu-id="76011-2135">Set-AzVMDiskEncryptionExtension의 두 가지 패스 시나리오에서 발생하는 암호화 설정 업데이트의 버그가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2135">Fix bug in update encryption settings in Set-AzVMDiskEncryptionExtension, two pass scenario.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="76011-2136">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="76011-2136">Az.DataFactory</span></span>
* <span data-ttu-id="76011-2137">ADF V2 데이터 흐름에 대한 CRUD 명령으로 Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow 및 Get-AzDataFactoryV2DataFlow가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2137">Adding CRUD commands for ADF V2 data flow: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow, and Get-AzDataFactoryV2DataFlow.</span></span>
* <span data-ttu-id="76011-2138">ADF V2 데이터 흐름 디버그 세션에 대한 작업 명령으로 Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand 및 Stop-AzDataFactoryV2DataFlowDebugSession이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2138">Adding action commands for ADF V2 data flow debug Session: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand and Stop-AzDataFactoryV2DataFlowDebugSession.</span></span>
* <span data-ttu-id="76011-2139">ADF .Net SDK 버전이 4.2.0으로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2139">Update ADF .Net SDK version to 4.2.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="76011-2140">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="76011-2140">Az.DataLakeStore</span></span>
* <span data-ttu-id="76011-2141">도메인 없이 '-'가 있는 계정을 전달할 수 있도록 계정 유효성 검사가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2141">Fix account validation so that accounts with '-' can be passed without domain</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="76011-2142">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="76011-2142">Az.HealthcareApis</span></span>
* <span data-ttu-id="76011-2143">PowerShell 버전이 1.0.0으로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2143">Updated the powershell version to 1.0.0</span></span>
* <span data-ttu-id="76011-2144">SDK 버전이 1.0.2로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2144">Updated the SDK version to 1.0.2</span></span>
* <span data-ttu-id="76011-2145">새 SDK 버전을 참조하도록 테스트가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2145">Update in tests to refer to new SDK version</span></span>
* <span data-ttu-id="76011-2146">출력이 중첩 구조에서 평면화 구조로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2146">Updated the output structure from nested to flattened.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="76011-2147">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="76011-2147">Az.IotHub</span></span>
* <span data-ttu-id="76011-2148">새 라우팅 원본 추가: DigitalTwinChangeEvents</span><span class="sxs-lookup"><span data-stu-id="76011-2148">Add new routing source: DigitalTwinChangeEvents</span></span>
* <span data-ttu-id="76011-2149">사소한 버그 수정: Get-AzIothub에서 subscriptionId를 반환하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2149">Minor bug fix: Get-AzIothub not returning subscriptionId</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="76011-2150">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="76011-2150">Az.Monitor</span></span>
* <span data-ttu-id="76011-2151">작업 그룹에 대한 새 작업 그룹 수신기로 -ItsmReceiver, -VoiceReceiver, -ArmRoleReceiver, -AzureFunctionReceiver, -LogicAppReceiver, -AutomationRunbookReceiver, -AzureAppPushReceiver가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2151">New action group receivers added for action group   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span></span>
* <span data-ttu-id="76011-2152">수신기에 사용하도록 설정된 일반 경고 스키마가 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2152">Use common alert schema enabled for the receivers.</span></span> <span data-ttu-id="76011-2153">SMS, Azure 앱 푸시, ITSM 및 음성 수신기에는 적용되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2153">This is not applicable for SMS, Azure App push , ITSM and Voice recievers</span></span>
* <span data-ttu-id="76011-2154">웹후크에서 이제 Azure Active Directory 인증을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2154">Webhooks now supports Azure active directory authentication .</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="76011-2155">Az.Network</span><span class="sxs-lookup"><span data-stu-id="76011-2155">Az.Network</span></span>
* <span data-ttu-id="76011-2156">서비스 엔드포인트 정책에 사용할 수 있는 별칭을 가져오기 위해 호출할 수 있는 새 Get-AzAvailableServiceAlias cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2156">Add new cmdlet Get-AzAvailableServiceAlias which can be called to get the aliases that can be used for Service Endpoint Policies.</span></span>
* <span data-ttu-id="76011-2157">트래픽 선택기를 Virtual Network 게이트웨이 연결에 추가할 수 있는 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2157">Added support for the adding traffic selectors to Virtual Network Gateway Connections</span></span>
    - <span data-ttu-id="76011-2158">추가된 새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2158">New cmdlets added:</span></span>
        - <span data-ttu-id="76011-2159">New-AzureRmTrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="76011-2159">New-AzureRmTrafficSelectorPolicy</span></span>
    - <span data-ttu-id="76011-2160">cmdlet이 선택적인 -TrafficSelectorPolicies, -New-AzureRmVirtualNetworkGatewayConnection, -Set-AzureRmVirtualNetworkGatewayConnection 매개 변수로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2160">Cmdlets updated with optional parameter -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="76011-2161">ESP 및 AH 프로토콜 지원이 네트워크 보안 규칙 구성에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2161">Add support for ESP and AH protocols in network security rule configurations</span></span>
    - <span data-ttu-id="76011-2162">다음 Cmdlet이 업데이트 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2162">Updated cmdlets:</span></span>
        - <span data-ttu-id="76011-2163">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="76011-2163">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="76011-2164">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="76011-2164">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="76011-2165">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="76011-2165">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="76011-2166">Cortex cmdlet의 예외 처리가 향상되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2166">Improve handling of exceptions in Cortex cmdlets</span></span>
* <span data-ttu-id="76011-2167">새 VirtualNetworkGateways 세대 및 SKU</span><span class="sxs-lookup"><span data-stu-id="76011-2167">New Generations and SKUs for VirtualNetworkGateways</span></span>
  - <span data-ttu-id="76011-2168">새 VirtualNetworkGateways 세대가 도입되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2168">Introduce new Generations for VirtualNetworkGateways.</span></span>
  - <span data-ttu-id="76011-2169">높은 처리량의 새 VirtualNetworkGateways SKU가 도입되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2169">Introduce new high throughput SKUs for VirtualNetworkGateways.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="76011-2170">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="76011-2170">Az.RedisCache</span></span>
* <span data-ttu-id="76011-2171">'-Size' 매개 변수에 대한 누락 값을 포함하도록 'Set-AzRedisCache' 참조 설명서가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2171">Updated 'Set-AzRedisCache' reference documentation to include missing values for '-Size' parameter</span></span>

#### <a name="azsql"></a><span data-ttu-id="76011-2172">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="76011-2172">Az.Sql</span></span>
* <span data-ttu-id="76011-2173">Managed Instance에서 Active Directory 관리자를 설정할 수 있는 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2173">Add support for setting Active Directory Administrator on Managed Instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="76011-2174">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="76011-2174">Az.Storage</span></span>
* <span data-ttu-id="76011-2175">스토리지 클라이언트 라이브러리가 11.1.0으로 업그레이드되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2175">Upgrade Storage Client Library to 11.1.0</span></span>
* <span data-ttu-id="76011-2176">관리 평면 API를 사용하여 컨테이너를 나열하면 NextPageLink를 통해 나열됩니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2176">List containers with Management plane API, will list with NextPageLink</span></span>
    -  <span data-ttu-id="76011-2177">Get-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="76011-2177">Get-AzRmStorageContainer</span></span>
* <span data-ttu-id="76011-2178">구독에서 스토리지 계정을 나열하면 NextPageLink를 통해 나열됩니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2178">List Storage accounts from subscription, will list with NextPageLink</span></span>
    -  <span data-ttu-id="76011-2179">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="76011-2179">Get-AzStorageAccount</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="76011-2180">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="76011-2180">Az.StorageSync</span></span>
* <span data-ttu-id="76011-2181">Reset-AzStorageSyncServerCertificate의 9810 문제가 해결되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2181">Fix Issue 9810 in Reset-AzStorageSyncServerCertificate.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="76011-2182">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="76011-2182">Az.Websites</span></span>
* <span data-ttu-id="76011-2183">앱의 ASP를 업데이트하는 Set-AzWebApp이 실패했습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2183">Set-AzWebApp updating ASP of an app was failing</span></span>

## <a name="270---september-2019"></a><span data-ttu-id="76011-2184">2.7.0 - 2019년 9월</span><span class="sxs-lookup"><span data-stu-id="76011-2184">2.7.0 - September 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="76011-2185">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="76011-2185">Az.ApiManagement</span></span>
* <span data-ttu-id="76011-2186">'Set-AzApiManagementPolicy' 참조 설명서에서 '-Format' 매개 변수 설명이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2186">Update '-Format' parameter description in 'Set-AzApiManagementPolicy' reference documentation</span></span>
* <span data-ttu-id="76011-2187">참조 설명서에서 사용되지 않는 cmdlet 'Update-AzApiManagementDeployment'의 참조를 제거했습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2187">Removed references of deprecated cmdlet 'Update-AzApiManagementDeployment' from reference documentation.</span></span> <span data-ttu-id="76011-2188">그 대신 'Set-AzApiManagement'를 사용하세요.</span><span class="sxs-lookup"><span data-stu-id="76011-2188">Use 'Set-AzApiManagement' instead.</span></span>

#### <a name="azautomation"></a><span data-ttu-id="76011-2189">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="76011-2189">Az.Automation</span></span>
* <span data-ttu-id="76011-2190">'Register-AzAutomationDscNode'에 대한 참조 설명서의 예제 오타가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2190">Fixed example typo in reference documentation for 'Register-AzAutomationDscNode'</span></span>
* <span data-ttu-id="76011-2191">Register-AzAutomationDSCNode에 OS 제한에 대한 설명이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2191">Added clarification on OS restriction to Register-AzAutomationDSCNode</span></span>
* <span data-ttu-id="76011-2192">-Wait 옵션에 대한 Start-AzAutomationRunbook cmdlet Null 참조 예외가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2192">Fixed Start-AzAutomationRunbook cmdlet Null reference exception for -Wait option.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="76011-2193">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="76011-2193">Az.Compute</span></span>
* <span data-ttu-id="76011-2194">New-AzDiskConfig에 UploadSizeInBytes 매개 변수가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2194">Add UploadSizeInBytes parameter tp New-AzDiskConfig</span></span>
* <span data-ttu-id="76011-2195">New-AzSnapshotConfig에 증분 매개 변수가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2195">Add Incremental parameter to New-AzSnapshotConfig</span></span>
* <span data-ttu-id="76011-2196">다음과 같은 낮은 우선 순위의 가상 머신 기능이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2196">Add a low priority virtual machine feature:</span></span>
    - <span data-ttu-id="76011-2197">MaxPrice, EvictionPolicy 및 Priority 매개 변수가 New-AzVMConfig에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2197">MaxPrice, EvictionPolicy and Priority parameters are added to New-AzVMConfig.</span></span>
    - <span data-ttu-id="76011-2198">MaxPrice 매개 변수는 New-AzVmssConfig, Update-AzVM 및 Update-AzVmss cmdlet에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2198">MaxPrice parameter is added to New-AzVmssConfig, Update-AzVM and Update-AzVmss cmdlets.</span></span>
* <span data-ttu-id="76011-2199">구독의 모든 가용성 세트를 나열할 때 발생하는 Get-AzAvailabilitySet cmdlet에 대한 VM 참조 이슈가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2199">Fix VM reference issue for Get-AzAvailabilitySet cmdlet when it lists all availability sets in the subscription.</span></span>
* <span data-ttu-id="76011-2200">Get-AzRemoteDesktopFile에 대한 null 예외가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2200">Fix the null exception for Get-AzRemoteDesktopFile.</span></span>
* <span data-ttu-id="76011-2201">종료 상대 위치에 대한 VHD 검색 메서드가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2201">Fix VHD Seek method for end-relative position.</span></span>
* <span data-ttu-id="76011-2202">New-AzVM 및 Update-AzVM에 대한 UltraSSD 이슈가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2202">Fix UltraSSD issue for New-AzVM and Update-AzVM.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="76011-2203">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="76011-2203">Az.DataFactory</span></span>
* <span data-ttu-id="76011-2204">ADF V2에 대한 3가지 새 명령 Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription 및 Get-AzDataFactoryV2TriggerSubscriptionStatus가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2204">Adding 3 new commands for ADF V2 - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription, and Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>
* <span data-ttu-id="76011-2205">ADF .Net SDK 버전이 4.1.3으로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2205">Updated ADF .Net SDK version to 4.1.3</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="76011-2206">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="76011-2206">Az.HDInsight</span></span>
* <span data-ttu-id="76011-2207">호출 주요 변경 내용</span><span class="sxs-lookup"><span data-stu-id="76011-2207">Call out breaking changes</span></span>

#### <a name="aziothub"></a><span data-ttu-id="76011-2208">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="76011-2208">Az.IotHub</span></span>
* <span data-ttu-id="76011-2209">지역 쌍 재해 복구 지역에 IotHub에 대한 장애 조치(failover) 호출 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2209">Add support to invoke failover for an IotHub to the geo-paired disaster recovery region.</span></span>
* <span data-ttu-id="76011-2210">IotHub에 대한 메시지 보강 관리 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2210">Add support to manage message enrichment for an IotHub.</span></span> <span data-ttu-id="76011-2211">새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2211">New cmdlets are:</span></span>
    - <span data-ttu-id="76011-2212">Add-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="76011-2212">Add-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="76011-2213">Get-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="76011-2213">Get-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="76011-2214">Remove-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="76011-2214">Remove-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="76011-2215">Set-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="76011-2215">Set-AzIotHubMessageEnrichment</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="76011-2216">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="76011-2216">Az.Monitor</span></span>
* <span data-ttu-id="76011-2217">최신 모니터링 SDK, 즉, 0.24.1-preview를 가리킵니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2217">Pointing to the most recent Monitor SDK, i.e. 0.24.1-preview</span></span>
   - <span data-ttu-id="76011-2218">메트릭 cmdlet에 줄 바꿈하지 않는 변경 내용을 추가합니다. 즉, 단위 열거형은 여러 새 값을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2218">Adds non-braking changes to the Metrics cmdlets, i.e. the Unit enumeration supports several new values.</span></span> <span data-ttu-id="76011-2219">이러한 cmdlet은 읽기 전용이므로 cmdlet 입력이 변경되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2219">These are read-only cmdlets, so there would be no change in the input of the cmdlets.</span></span>
   - <span data-ttu-id="76011-2220">이제 **ActionGroups** 요청의 api 버전은 **2019-06-01** 이고, 이전에는 **2018-03-01** 였습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2220">The api-version of the **ActionGroups** requests is now **2019-06-01**, before it was **2018-03-01**.</span></span> <span data-ttu-id="76011-2221">시나리오 테스트가 이 변경 내용에 맞게 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2221">The scenario tests have been updated to accommodate for this change.</span></span>
   - <span data-ttu-id="76011-2222">**EmailReceiver** 및 **WebhookReceiver** 클래스에 대한 생성자가 새 필수 인수, 즉, **useCommonAlertSchema** 라는 부울 값을 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2222">The constructors for the classes **EmailReceiver** and **WebhookReceiver** added one new mandatory argument, i.e. a Boolean value called **useCommonAlertSchema**.</span></span> <span data-ttu-id="76011-2223">현재 이 값은 cmdlet의 주요 변경 사항을 숨기도록 **false** 로 고정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2223">Currently, the value is fixed to **false** to hide this breaking change from the cmdlets.</span></span> <span data-ttu-id="76011-2224">**참고**: 이 변경 사항은 경고 팀에서 유효성을 검사해야 하는 임시 변경 내용입니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2224">**NOTE**: this is a temporary change that must be validated by the Alerts team.</span></span>
   - <span data-ttu-id="76011-2225">이전 SDK에서 변경된 **Source** 클래스(**ScheduledQueryRuleSource** 클래스와 관련됨)의 생성자에 대한 인수 순서입니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2225">The order of the arguments for the constructor of the class **Source** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="76011-2226">이번 변화로 인해 두 개의 단위 테스트를 수정해야 했습니다. 즉, 두 단위 테스트가 컴파일되었지만 테스트를 통과하지 못했습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2226">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
   - <span data-ttu-id="76011-2227">이전 SDK에서 변경된 **AlertingAction** 클래스(**ScheduledQueryRuleSource** 클래스와 관련됨)의 생성자에 대한 인수 순서입니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2227">The order of the arguments for the constructor of the class **AlertingAction** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="76011-2228">이번 변화로 인해 두 개의 단위 테스트를 수정해야 했습니다. 즉, 두 단위 테스트가 컴파일되었지만 테스트를 통과하지 못했습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2228">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
* <span data-ttu-id="76011-2229">메트릭 경고 V2에 대한 동적 임계값 기준 지원</span><span class="sxs-lookup"><span data-stu-id="76011-2229">Support Dynamic Threshold criteria for metric alert V2</span></span>
    - <span data-ttu-id="76011-2230">AzMetricAlertRuleV2Criteria: 이제 동적 임계값 조건도 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2230">New-AzMetricAlertRuleV2Criteria: now creats dynamic threshold criteria also</span></span>
    - <span data-ttu-id="76011-2231">Add-AzMetricAlertRuleV2: 이제 동적 임계값 조건도 수락합니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2231">Add-AzMetricAlertRuleV2: now accept dynamic threshold criteria also</span></span>
* <span data-ttu-id="76011-2232">SQR(예약된 쿼리 규칙)의 향상된 기능</span><span class="sxs-lookup"><span data-stu-id="76011-2232">Improvements in Scheduled Query Rule cmdlets (SQR)</span></span>
 - <span data-ttu-id="76011-2233">Cmdlet이 'Location' 매개 변수를 두 가지 형식(eastus 같은 위치 또는 미국 동부 같은 위치 표시 이름)으로 모두 허용합니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2233">Cmdlets will accept 'Location' paramater in both formats, either the location (e.g. eastus) or the location display name (e.g. East US)</span></span>
 - <span data-ttu-id="76011-2234">도움말 파일에 적절하게 표시된 'Enabled' 매개 변수</span><span class="sxs-lookup"><span data-stu-id="76011-2234">Illustrated 'Enabled' parameter in help files properly</span></span>
 - <span data-ttu-id="76011-2235">선택적 매개 변수 'ActionGroup'에 대한 예제가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2235">Added examples for 'ActionGroup' optional parameter</span></span>
 - <span data-ttu-id="76011-2236">도움말 파일이 전체적으로 개선되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2236">Overall improved help files</span></span>
* <span data-ttu-id="76011-2237">'Set-AzActionRule'의 범위 유형 결정 버그를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2237">Fix bug in determining scope type for 'Set-AzActionRule'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="76011-2238">Az.Network</span><span class="sxs-lookup"><span data-stu-id="76011-2238">Az.Network</span></span>
* <span data-ttu-id="76011-2239">'New-AzApplicationGateway' 참조 설명서의 잘못된 예제가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2239">Fix incorrect example in 'New-AzApplicationGateway' reference documentation</span></span>
* <span data-ttu-id="76011-2240">'Get-AzNetworkWatcherPacketCapture' 참조 설명서에 패킷 캡처를 위한 모든 속성 검색과 관련된 메모가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2240">Add note in 'Get-AzNetworkWatcherPacketCapture' reference documentation about retrieving all properties for a packet capture</span></span>
* <span data-ttu-id="76011-2241">NIC를 올바르게 열거하도록 'Test-AzNetworkWatcherIPFlow' 참조 설명서의 예제가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2241">Fixed example in 'Test-AzNetworkWatcherIPFlow' reference documentation to correctly enumerate NICs</span></span>
* <span data-ttu-id="76011-2242">추가 세부 정보가 있는 경우 추가 세부 정보를 표시하도록 클라우드 예외 구문 분석이 향상되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2242">Improved cloud exception parsing to display additional details if they are present</span></span>
* <span data-ttu-id="76011-2243">더 많은 형식의 SDK 예외를 처리하도록 클라우드 예외 구문 분석이 향상되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2243">Improved cloud exception parsing to handle additional type of SDK exception</span></span>
* <span data-ttu-id="76011-2244">보안 규칙 모델의 잘못된 매핑이 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2244">Fixed incorrect mapping of Security Rule models</span></span>
* <span data-ttu-id="76011-2245">네트워크 인터페이스에 개인 IP 기능을 위한 속성이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2245">Added properties to network interface for private ip feature</span></span>
    - <span data-ttu-id="76011-2246">PSNetworkInterface에 'PrivateEndpoint' 속성이 PSResourceId 형식으로 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2246">Added property 'PrivateEndpoint' as type of PSResourceId to PSNetworkInterface</span></span>
    - <span data-ttu-id="76011-2247">PSNetworkInterfaceIPConfiguration에 'PrivateLinkConnectionProperties' 속성이 PSIpConfigurationConnectivityInformation 형식으로 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2247">Added property 'PrivateLinkConnectionProperties' as type of PSIpConfigurationConnectivityInformation to PSNetworkInterfaceIPConfiguration</span></span>
    - <span data-ttu-id="76011-2248">새 모델 클래스 PSIpConfigurationConnectivityInformation이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2248">Added new model class PSIpConfigurationConnectivityInformation</span></span>
* <span data-ttu-id="76011-2249">Azure Firewall 리소스에 대한 새 ApplicationRuleProtocolType 'mssql'이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2249">Added new ApplicationRuleProtocolType 'mssql' for Azure Firewall resource</span></span>
* <span data-ttu-id="76011-2250">Virtual WAN에서 멀티 링크를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2250">MultiLink support in Virtual WAN</span></span>
    - <span data-ttu-id="76011-2251">새로운 cmdlet</span><span class="sxs-lookup"><span data-stu-id="76011-2251">New cmdlets</span></span>
        - <span data-ttu-id="76011-2252">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="76011-2252">New-AzVpnSiteLink</span></span>
        - <span data-ttu-id="76011-2253">New-AzVpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="76011-2253">New-AzVpnSiteLinkConnection</span></span>
    - <span data-ttu-id="76011-2254">업데이트된 cmdlet:</span><span class="sxs-lookup"><span data-stu-id="76011-2254">Updated cmdlet:</span></span>
        - <span data-ttu-id="76011-2255">New-VpnSite</span><span class="sxs-lookup"><span data-stu-id="76011-2255">New-VpnSite</span></span>
        - <span data-ttu-id="76011-2256">Update-VpnSite</span><span class="sxs-lookup"><span data-stu-id="76011-2256">Update-VpnSite</span></span>
        - <span data-ttu-id="76011-2257">New-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="76011-2257">New-VpnConnection</span></span>
        - <span data-ttu-id="76011-2258">Update-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="76011-2258">Update-VpnConnection</span></span>
* <span data-ttu-id="76011-2259">AzureRM cmdlet 대신 Az cmdlet을 사용하도록 일부 PowerShell 예제의 문서가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2259">Fixed documents for some PowerShell examples to use Az cmdlets instead of AzureRM cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="76011-2260">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="76011-2260">Az.RecoveryServices</span></span>
* <span data-ttu-id="76011-2261">AzureVMpolicy 개체가 ProtectedItemsCount 특성으로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2261">Update AzureVMpolicy Object with ProtectedItemsCount Attribute</span></span>
* <span data-ttu-id="76011-2262">VM 정책 및 원래 스토리지 계정 복원에 대한 테스트가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2262">Added Tests for VM policy and Original Storage Account Restore</span></span>

#### <a name="azresources"></a><span data-ttu-id="76011-2263">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="76011-2263">Az.Resources</span></span>
* <span data-ttu-id="76011-2264">매개 변수 범위 없이 AzRoleAssignment를 호출할 수 없는 버그가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2264">Fix bug where New-AzRoleAssignment could not be called without parameter Scope.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="76011-2265">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="76011-2265">Az.ServiceFabric</span></span>
* <span data-ttu-id="76011-2266">'AzServiceFabricReliability' 참조 설명서에 대한 예제의 오타가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2266">Fixed typo in example for 'Update-AzServiceFabricReliability' reference documentation</span></span>
* <span data-ttu-id="76011-2267">애플리케이션 및 서비스를 관리하는 다음과 같은 새 cmdlet이 추가됩니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2267">Adding new cmdlets to manage appliaction and services:</span></span>
    - <span data-ttu-id="76011-2268">New-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="76011-2268">New-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="76011-2269">New-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="76011-2269">New-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="76011-2270">New-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="76011-2270">New-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="76011-2271">New-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="76011-2271">New-AzServiceFabricService</span></span>
    - <span data-ttu-id="76011-2272">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="76011-2272">Update-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="76011-2273">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="76011-2273">Get-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="76011-2274">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="76011-2274">Get-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="76011-2275">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="76011-2275">Get-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="76011-2276">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="76011-2276">Get-AzServiceFabricService</span></span>
    - <span data-ttu-id="76011-2277">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="76011-2277">Remove-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="76011-2278">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="76011-2278">Remove-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="76011-2279">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="76011-2279">Remove-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="76011-2280">Remove-AzServiceFabricServic</span><span class="sxs-lookup"><span data-stu-id="76011-2280">Remove-AzServiceFabricServic</span></span>
* <span data-ttu-id="76011-2281">Service Fabric SDK가 Service Fabric 리소스 공급자 api 버전 2019-03-01을 사용하는 1.2.0 버전으로 업그레이드되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2281">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2019-03-01.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="76011-2282">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="76011-2282">Az.SignalR</span></span>
* <span data-ttu-id="76011-2283">Update, Restart, CheckNameAvailability, GetUsage Cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2283">Add Update, Restart, CheckNameAvailability, GetUsage Cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="76011-2284">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="76011-2284">Az.Sql</span></span>
* <span data-ttu-id="76011-2285">'Get-AzSqlElasticPool'에 대한 참조 설명서의 예제가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2285">Update example in reference documentation for 'Get-AzSqlElasticPool'</span></span>
* <span data-ttu-id="76011-2286">탄력적 풀을 만드는 vCore 예제가 추가되었습니다(AzSqlElasticPool).</span><span class="sxs-lookup"><span data-stu-id="76011-2286">Added vCore example to creating an elastic pool (New-AzSqlElasticPool).</span></span>
* <span data-ttu-id="76011-2287">Set-AzSqlServerAdvancedThreatProtectionPolicy 및 Set-AzSqlDatabaseAdvancedThreatProtectionPolicy에서 EmailAddresses가 비어 있는 경우 EmailAddresses의 유효성을 검사하고 EmailAdmins가 false가 아닌지 확인하는 기능이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2287">Remove the validation of EmailAddresses and the check that EmailAdmins is not false in case EmailAddresses is empty in Set-AzSqlServerAdvancedThreatProtectionPolicy and Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="76011-2288">감사 범주를 사용하는 여러 진단 설정이 있는 경우 서버/데이터베이스 감사 설정을 제거하도록 설정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2288">Enabled removal of server/database auditing settings when multiple diagnostic settings that enable audit category exist.</span></span>
* <span data-ttu-id="76011-2289">여러 Sql 취약성 평가 cmdlet에서 이메일 주소 유효성 검사가 수정되었습니다(Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting 및 Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span><span class="sxs-lookup"><span data-stu-id="76011-2289">Fix email addresses validation in multiple Sql Vulnerability Assessment cmdlets (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting and Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span></span>

#### <a name="azstorage"></a><span data-ttu-id="76011-2290">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="76011-2290">Az.Storage</span></span>
* <span data-ttu-id="76011-2291">'Get-AzStorageAccountKey'에 대한 참조 설명서의 예제가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2291">Updated example in reference documentation for 'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="76011-2292">Azure 파일 업로드/다운에서, 원본 파일 SMB 속성(파일 특성, 파일 생성 시간, 파일을 마지막으로 쓴 시간)을 대상 파일에 보존하는 기능이 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2292">In upload/Downalod Azure File,support perserve the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the destination file</span></span>
    -  <span data-ttu-id="76011-2293">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="76011-2293">Set-AzStorageFileContent</span></span>
    -  <span data-ttu-id="76011-2294">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="76011-2294">Get-AzStorageFileContent</span></span>
* <span data-ttu-id="76011-2295">컨테이너가 사용되는 ImmutabilityPolicy에서 properties/metadate fail을 사용하여 블록 Blob 업로드가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2295">Fix Upload block blob with properties/metadate fail on container enabled ImmutabilityPolicy.</span></span>
    -  <span data-ttu-id="76011-2296">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="76011-2296">Set-AzStorageBlobContent</span></span>
* <span data-ttu-id="76011-2297">관리 평면 API를 사용하여 Azure 파일 공유 관리를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2297">Support manage Azure File shares with Management plane API</span></span>
    -  <span data-ttu-id="76011-2298">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="76011-2298">New-AzRmStorageShare</span></span>
    -  <span data-ttu-id="76011-2299">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="76011-2299">Get-AzRmStorageShare</span></span>
    -  <span data-ttu-id="76011-2300">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="76011-2300">Update-AzRmStorageShare</span></span>
    -  <span data-ttu-id="76011-2301">Remove-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="76011-2301">Remove-AzRmStorageShare</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="76011-2302">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="76011-2302">Az.Websites</span></span>
* <span data-ttu-id="76011-2303">앱을 새 ASP로 마이그레이션할 때 웹앱 태그가 삭제되는 이슈가 해결되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2303">Fixing issue where webapp Tags were getting deleted when migrating App to new ASPwhere webapp Tags were getting deleted when migrating App to new ASP</span></span>
* <span data-ttu-id="76011-2304">Linux와 Windows에서 모두 작동하도록 Publish-AzureWebapp이 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2304">Fixing the Publish-AzureWebapp to work across Linux and windows</span></span>
* <span data-ttu-id="76011-2305">'Get-AzWebAppPublishingProfile' 참조 설명서의 예제가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2305">Update example in 'Get-AzWebAppPublishingProfile' reference documentation</span></span>

## <a name="260---august-2019"></a><span data-ttu-id="76011-2306">2.6.0 - 2019년 8월</span><span class="sxs-lookup"><span data-stu-id="76011-2306">2.6.0 - August 2019</span></span>
#### <a name="general"></a><span data-ttu-id="76011-2307">일반</span><span class="sxs-lookup"><span data-stu-id="76011-2307">General</span></span>
* <span data-ttu-id="76011-2308">여러 모듈에서 기타 오타가 수정됨</span><span class="sxs-lookup"><span data-stu-id="76011-2308">Fixed miscellaneous typos across numerous modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="76011-2309">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="76011-2309">Az.Accounts</span></span>
* <span data-ttu-id="76011-2310">Azure Functions 인증에서 사용자가 할당한 MSI가 지원됨(# 9479)</span><span class="sxs-lookup"><span data-stu-id="76011-2310">Support user-assigned MSI in Azure Functiosn Authentication (#9479)</span></span>

#### <a name="azaks"></a><span data-ttu-id="76011-2311">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="76011-2311">Az.Aks</span></span>
* <span data-ttu-id="76011-2312">'Get-AzAks' 출력 관련 문제가 해결됨</span><span class="sxs-lookup"><span data-stu-id="76011-2312">Fix issue with output for 'Get-AzAks'</span></span>
    * <span data-ttu-id="76011-2313">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/9847 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="76011-2313">More information here: https://github.com/Azure/azure-powershell/issues/9847</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="76011-2314">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="76011-2314">Az.ApiManagement</span></span>
* <span data-ttu-id="76011-2315">문제 https://github.com/Azure/azure-powershell/issues/9351 수정</span><span class="sxs-lookup"><span data-stu-id="76011-2315">Fix for issue https://github.com/Azure/azure-powershell/issues/9351</span></span>
    - <span data-ttu-id="76011-2316">productId, apiId, groupId 및 userId에 대한 제한을 적용하지 않는 .Net NuGet 버전이 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="76011-2316">Update .net nuget version, which does not enforce restrictions on productId, apiId, groupId and userId</span></span>
* <span data-ttu-id="76011-2317">**Get-AzApiManagementProduct** - API를 사용하는 제품에 대한 쿼리 지원이 추가됨</span><span class="sxs-lookup"><span data-stu-id="76011-2317">**Get-AzApiManagementProduct** - Added support for querying products using Api.</span></span>
  https://github.com/Azure/azure-powershell/issues/9482
* <span data-ttu-id="76011-2318">**New-AzApiManagementApiRevision** - 새 API 수정(https://github.com/Azure/azure-powershell/issues/9752 )을 만들 때 ApiRevisionDescription이 설정되지 않은 문제가 해결됨</span><span class="sxs-lookup"><span data-stu-id="76011-2318">**New-AzApiManagementApiRevision** - Fix for issue where ApiRevisionDescription was not being set when creating new api revision https://github.com/Azure/azure-powershell/issues/9752</span></span>
* <span data-ttu-id="76011-2319">'PsApiManagementOAuth2AuthrozationServer' 모델의 오타가 'PsApiManagementOAuth2AuthorizationServer'로 수정됨</span><span class="sxs-lookup"><span data-stu-id="76011-2319">Fixed typo in model 'PsApiManagementOAuth2AuthrozationServer' to 'PsApiManagementOAuth2AuthorizationServer'</span></span>

#### <a name="azbatch"></a><span data-ttu-id="76011-2320">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="76011-2320">Az.Batch</span></span>
* <span data-ttu-id="76011-2321">도움말 메시지 및 설명서에서 Windows를 대문자로 시작하도록 오타가 수정됨</span><span class="sxs-lookup"><span data-stu-id="76011-2321">Fixed typo in help message and documentation to capitalize Windows</span></span>

#### <a name="azcdn"></a><span data-ttu-id="76011-2322">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="76011-2322">Az.Cdn</span></span>
* <span data-ttu-id="76011-2323">CDN 모듈 변환 도우미의 오타가 수정됨</span><span class="sxs-lookup"><span data-stu-id="76011-2323">Fixed a typo in CDN module conversion helper</span></span>

#### <a name="azcompute"></a><span data-ttu-id="76011-2324">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="76011-2324">Az.Compute</span></span>
* <span data-ttu-id="76011-2325">VmssId가 New-AzVMConfig cmdlet에 추가됨</span><span class="sxs-lookup"><span data-stu-id="76011-2325">Add VmssId to New-AzVMConfig cmdlet</span></span>
* <span data-ttu-id="76011-2326">TerminateScheduledEvents 및 TerminateScheduledEventNotBeforeTimeoutInMinutes 매개 변수가 New-AzVmssConfig 및 Update-AzVmss에 추가됨</span><span class="sxs-lookup"><span data-stu-id="76011-2326">Add TerminateScheduledEvents and TerminateScheduledEventNotBeforeTimeoutInMinutes parameters to New-AzVmssConfig and Update-AzVmss</span></span>
* <span data-ttu-id="76011-2327">HyperVGeneration 속성이 VM 이미지 개체에 추가됨</span><span class="sxs-lookup"><span data-stu-id="76011-2327">Add HyperVGeneration property to VM image object</span></span>
* <span data-ttu-id="76011-2328">Host 및 HostGroup 기능이 추가됨</span><span class="sxs-lookup"><span data-stu-id="76011-2328">Add Host and HostGroup features</span></span>
    - <span data-ttu-id="76011-2329">새 cmdlet:   New-AzHostGroup, New-AzHost, Get-AzHostGroup, Get-AzHost, Remove-AzHostGroup, Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="76011-2329">New cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span></span>
    - <span data-ttu-id="76011-2330">HostId 매개 변수가 New-AzVMConfig 및 New-AzVM 추가됨</span><span class="sxs-lookup"><span data-stu-id="76011-2330">HostId parameter is added to New-AzVMConfig and New-AzVM</span></span>
* <span data-ttu-id="76011-2331">'Invoke-AzVMRunCommand' 설명서의 예제에서 올바른 매개 변수 이름을 사용하도록 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="76011-2331">Update example in 'Invoke-AzVMRunCommand' documentation to use correct parameter name</span></span>
* <span data-ttu-id="76011-2332">'Set-AzVMDiskEncryptionExtension' 및 'Set-AzVmssDiskEncryptionExtension' 참조 설명서의 '-VolumeType' 설명이 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="76011-2332">Update '-VolumeType' description in 'Set-AzVMDiskEncryptionExtension' and 'Set-AzVmssDiskEncryptionExtension' reference documentation</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="76011-2333">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="76011-2333">Az.DataFactory</span></span>
* <span data-ttu-id="76011-2334">'New-AzDataFactoryEncryptValue' 설명서에서 'Windows'를 대문자로 시작하도록 오타가 수정됨</span><span class="sxs-lookup"><span data-stu-id="76011-2334">Fix typo to capitalize 'Windows' in 'New-AzDataFactoryEncryptValue' documentation</span></span>
* <span data-ttu-id="76011-2335">ADF .Net SDK 버전이 4.1.2로 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="76011-2335">Updated ADF .Net SDK version to 4.1.2</span></span>
* <span data-ttu-id="76011-2336">자체 호스팅 통합 런타임을 SSIS Integration Runtime의 프록시로 설정할 수 있도록 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' 및 'DataProxyStagingPath' 매개 변수가 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd에 추가됨</span><span class="sxs-lookup"><span data-stu-id="76011-2336">Add parameter 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' and 'DataProxyStagingPath' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable set up Self-Hosted Integration Runtime as a proxy for SSIS Integration Runtime</span></span>
* <span data-ttu-id="76011-2337">PSTriggerRun에서 트리거된 파이프라인, 메시지 및 속성을 표시하고, PSActivityRun에서 작업 유형을 표시하도록 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="76011-2337">Updated PSTriggerRun to show the triggered pipelines, message and properties, and PSActivityRun to show the activity type</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="76011-2338">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="76011-2338">Az.DataLakeStore</span></span>
* <span data-ttu-id="76011-2339">오류 또는 원격 예외에 대한 Get-DataLakeStoreDeletedItem 중단이 수정됨</span><span class="sxs-lookup"><span data-stu-id="76011-2339">Fix hanging of Get-DataLakeStoreDeletedItem for any errors or remote exceptions.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="76011-2340">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="76011-2340">Az.EventHub</span></span>
* <span data-ttu-id="76011-2341">#9658 문제 해결: Set-AzEventHubNetworkRuleSet의 VirtualNteworkRule 매개 변수에 대한 오타</span><span class="sxs-lookup"><span data-stu-id="76011-2341">Fix for issue #9658 : Typo VirtualNteworkRule parameter in Set-AzEventHubNetworkRuleSet</span></span>
* <span data-ttu-id="76011-2342">#9558 문제 해결: Set-AzEventHubNamespace에서 PUT 대신 PATCH가 사용됨</span><span class="sxs-lookup"><span data-stu-id="76011-2342">Fix for issue #9558 : Set-AzEventHubNamespace is using PATCH instead of PUT</span></span>
* <span data-ttu-id="76011-2343">EnableKafka 매개 변수가 Set-AzEventHubNamespace cmdlet에 추가됨</span><span class="sxs-lookup"><span data-stu-id="76011-2343">added EnableKafka parameter to Set-AzEventHubNamespace cmdlet</span></span>
* <span data-ttu-id="76011-2344">#9786 문제 해결: Listen(수신 대기) 전용 권한이 있는 규칙을 만들 수 없음</span><span class="sxs-lookup"><span data-stu-id="76011-2344">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>

#### <a name="azmarketplaceordering"></a><span data-ttu-id="76011-2345">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="76011-2345">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="76011-2346">'Azure'가 모두 소문자인 설명서의 오타가 수정됨</span><span class="sxs-lookup"><span data-stu-id="76011-2346">Fixed documentation typo where 'Azure' was all lowercase letters</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="76011-2347">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="76011-2347">Az.Monitor</span></span>
* <span data-ttu-id="76011-2348">도움말 설명서에서 잘못된 매개 변수 이름이 수정됨</span><span class="sxs-lookup"><span data-stu-id="76011-2348">Fixed incorrect parameter name in help documentation</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="76011-2349">Az.Network</span><span class="sxs-lookup"><span data-stu-id="76011-2349">Az.Network</span></span>
* <span data-ttu-id="76011-2350">New-AzPrivateLinkServiceIpConfig가 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="76011-2350">Updated New-AzPrivateLinkServiceIpConfig</span></span>
    - <span data-ttu-id="76011-2351">서버 쪽에서 사용되지 않으므로 'PublicIpAddress' 매개 변수가 사용되지 않음</span><span class="sxs-lookup"><span data-stu-id="76011-2351">Deprecated the paramster 'PublicIpAddress' since this is never used in the server side.</span></span>
    - <span data-ttu-id="76011-2352">현재 IP 구성이 기본 구성인지 여부를 나타내는 하나의 선택적 'Primary' 매개 변수가 추가됨</span><span class="sxs-lookup"><span data-stu-id="76011-2352">Added one optional parameter 'Primary' that indicate the current ip configuration is primary one or not.</span></span>
* <span data-ttu-id="76011-2353">SDK의 요청 오류 예외 처리가 향상됨 - 이전의 SDK 예외가 올바르게 처리되지 않아 주요 오류 세부 정보가 표시되지 않은 문제가 해결됨</span><span class="sxs-lookup"><span data-stu-id="76011-2353">Improved handling of request error exception from SDK   -Fixes the issue that previously SDK exceptions aren't handled correctly which results in key error details not being displayed</span></span>
* <span data-ttu-id="76011-2354">올바른 IPv6 접두사 길이를 확인하기 위해 Ipv6 IP 접두사에 대한 유효성 검사 논리가 조정됨</span><span class="sxs-lookup"><span data-stu-id="76011-2354">Adjusted validation logic for Ipv6 IP Prefix to check for correct IPv6 prefix length.</span></span>
* <span data-ttu-id="76011-2355">Get-AzVirtualNetworkSubnetConfig가 업데이트됨: 서브넷 리소스 ID별로 가져오도록 설정되는 매개 변수 세트가 추가됨</span><span class="sxs-lookup"><span data-stu-id="76011-2355">Updated Get-AzVirtualNetworkSubnetConfig: Added parameter set to get by subnet resource id.</span></span>
* <span data-ttu-id="76011-2356">AzNetworkServiceTag의 Location(위치) 매개 변수에 대한 설명이 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="76011-2356">Updated description of Location parameter for AzNetworkServiceTag</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="76011-2357">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="76011-2357">Az.OperationalInsights</span></span>
* <span data-ttu-id="76011-2358">'New-AzOperationalInsightsLinuxSyslogDataSource'에 대한 설명서가 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="76011-2358">Updated documentation for 'New-AzOperationalInsightsLinuxSyslogDataSource'</span></span>
    - <span data-ttu-id="76011-2359">예제가 추가됨</span><span class="sxs-lookup"><span data-stu-id="76011-2359">Added example</span></span>
    - <span data-ttu-id="76011-2360">'-Name' 매개 변수에 대한 설명이 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="76011-2360">Updated description for '-Name' parameter</span></span>
* <span data-ttu-id="76011-2361">New-AzOperationalInsightsWindowsEventDataSource에 대한 예제가 추가됨</span><span class="sxs-lookup"><span data-stu-id="76011-2361">Added an example for New-AzOperationalInsightsWindowsEventDataSource</span></span>
* <span data-ttu-id="76011-2362">New-AzOperationalInsightsWindowsEventDataSource의 -Name 매개 변수에 대한 설명이 변경됨</span><span class="sxs-lookup"><span data-stu-id="76011-2362">Changed the description of the -Name parameter for New-AzOperationalInsightsWindowsEventDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="76011-2363">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="76011-2363">Az.RecoveryServices</span></span>
* <span data-ttu-id="76011-2364">'Get-AzRecoveryServicesBackupJobDetail.md'가 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="76011-2364">Update 'Get-AzRecoveryServicesBackupJobDetail.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="76011-2365">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="76011-2365">Az.Resources</span></span>
* <span data-ttu-id="76011-2366">Microsoft 리소스에 대한 새 2019-05-10 API 버전 지원이 추가됨</span><span class="sxs-lookup"><span data-stu-id="76011-2366">Add support for new api version 2019-05-10 for Microsoft.Resource</span></span>
    - <span data-ttu-id="76011-2367">변수, 리소스 및 속성에 대한 'copy.count = 0' 지원이 추가됨</span><span class="sxs-lookup"><span data-stu-id="76011-2367">Add support for 'copy.count = 0' for variables, resources and properties</span></span>
    - <span data-ttu-id="76011-2368">'condition = false' 또는 'copy.count = 0'인 리소스가 완료 모드에서 삭제됨</span><span class="sxs-lookup"><span data-stu-id="76011-2368">Resources with 'condition = false' or 'copy.count = 0' will be deleted in complete mode</span></span>
* <span data-ttu-id="76011-2369">정책을 구독 수준에서 도움말 문서에 할당하는 예제가 추가됨</span><span class="sxs-lookup"><span data-stu-id="76011-2369">Add an example of assigning policy at subscription level to help doc</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="76011-2370">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="76011-2370">Az.ServiceBus</span></span>
* <span data-ttu-id="76011-2371">#9658 문제 해결: Set-AzServiceBusNetworkRuleSet의 VirtualNetworkRule 매개 변수에 대한 오타</span><span class="sxs-lookup"><span data-stu-id="76011-2371">Fix for issue #9658 : Typo VirtualNetworkRule parameter in Set-AzServiceBusNetworkRuleSet</span></span>
* <span data-ttu-id="76011-2372">#9786 문제 해결: Listen(수신 대기) 전용 권한이 있는 규칙을 만들 수 없음</span><span class="sxs-lookup"><span data-stu-id="76011-2372">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>
* <span data-ttu-id="76011-2373">큐 및 토픽에 대한 이름 가용성을 확인하는 새 'Test-AzServiceBusNameAvailability' 명령이 추가됨</span><span class="sxs-lookup"><span data-stu-id="76011-2373">Added new command 'Test-AzServiceBusNameAvailability' to check the name availability for queue and topic</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="76011-2374">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="76011-2374">Az.ServiceFabric</span></span>
* <span data-ttu-id="76011-2375">노드 유형 추가 cmdlet 버그 수정:</span><span class="sxs-lookup"><span data-stu-id="76011-2375">Fix add node type cmdlet bugs:</span></span>
    - <span data-ttu-id="76011-2376">서비스 패브릭 클러스터와 관련이 없는 다른 vmss가 리소스 그룹에 있을 때 발생하는 NullReferenceException 버그</span><span class="sxs-lookup"><span data-stu-id="76011-2376">NullReferenceException bug when resource group had other vmss not related to the service fabric cluster.</span></span> <span data-ttu-id="76011-2377">문제 해결: https://github.com/Azure/azure-powershell/issues/8681</span><span class="sxs-lookup"><span data-stu-id="76011-2377">Fixes issue: https://github.com/Azure/azure-powershell/issues/8681</span></span>
    - <span data-ttu-id="76011-2378">virtualNetwork가 클러스터의 다른 리소스 그룹에 있을 때 cmdlet이 실패하는 버그가 수정됨</span><span class="sxs-lookup"><span data-stu-id="76011-2378">Fix bug where cmdlet failed if virtualNetwork was in a different resource group that the cluster.</span></span> <span data-ttu-id="76011-2379">문제 해결: https://github.com/Azure/azure-powershell/issues/8407</span><span class="sxs-lookup"><span data-stu-id="76011-2379">fixes issue: https://github.com/Azure/azure-powershell/issues/8407</span></span>
    - <span data-ttu-id="76011-2380">Add-AzServiceFabricApplicationCertificate cmdlet이 사용되지 않음</span><span class="sxs-lookup"><span data-stu-id="76011-2380">Deprecating Add-AzServiceFabricApplicationCertificate cmdlet</span></span>

#### <a name="azsql"></a><span data-ttu-id="76011-2381">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="76011-2381">Az.Sql</span></span>
* <span data-ttu-id="76011-2382">이전의 Auditing(감사) cmdlet에 대한 설명서가 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="76011-2382">Update documentation of old Auditing cmdlets.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="76011-2383">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="76011-2383">Az.Storage</span></span>
* <span data-ttu-id="76011-2384">더 많은 시나리오를 cmdlet 예제에 추가하고 매개 변수 설명을 업데이트하여 Get/Close-AzStorageFileHandle에 대한 도움말이 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="76011-2384">Update help for Get/Close-AzStorageFileHandle, by add more scenarios to cmdlet examples and update parameter descriptions</span></span>
* <span data-ttu-id="76011-2385">Blob 업로드 및 Blob 복사에서 StandardBlobTier가 지원됨</span><span class="sxs-lookup"><span data-stu-id="76011-2385">Support StandardBlobTier in upload blob and copy blob</span></span>
    -  <span data-ttu-id="76011-2386">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="76011-2386">Set-AzStorageBlobContent</span></span>
    -  <span data-ttu-id="76011-2387">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="76011-2387">Start-AzStorageBlobCopy</span></span>
* <span data-ttu-id="76011-2388">Blob 복사에서 우선 순위 리하이드레이션이 지원됨</span><span class="sxs-lookup"><span data-stu-id="76011-2388">Support Rehydrate Priority in copy blob</span></span>
    -  <span data-ttu-id="76011-2389">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="76011-2389">Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="76011-2390">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="76011-2390">Az.Websites</span></span>
* <span data-ttu-id="76011-2391">Set-AzWebApp 및 Set-AzWebAppSlot에서 -AppSettings 매개 변수에 대한 설명이 추가됨</span><span class="sxs-lookup"><span data-stu-id="76011-2391">Add clarification around -AppSettings parameter in Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <a name="250---july-2019"></a><span data-ttu-id="76011-2392">2.5.0 - 2019년 7월</span><span class="sxs-lookup"><span data-stu-id="76011-2392">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="76011-2393">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="76011-2393">Az.Accounts</span></span>
* <span data-ttu-id="76011-2394">ClientRuntime의 최신 버전을 사용하도록 일반적인 코드를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2394">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="76011-2395">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="76011-2395">Az.ApplicationInsights</span></span>
* <span data-ttu-id="76011-2396">'Remove-AzApplicationInsightsApiKey' 설명서의 예제 오타 수정</span><span class="sxs-lookup"><span data-stu-id="76011-2396">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span>

#### <a name="azautomation"></a><span data-ttu-id="76011-2397">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="76011-2397">Az.Automation</span></span>
* <span data-ttu-id="76011-2398">리소스 문자열의 오타 수정</span><span class="sxs-lookup"><span data-stu-id="76011-2398">Fix typo in resource string</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="76011-2399">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="76011-2399">Az.CognitiveServices</span></span>
* <span data-ttu-id="76011-2400">NetworkRuleSet 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2400">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="76011-2401">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="76011-2401">Az.Compute</span></span>
* <span data-ttu-id="76011-2402">VM 인스턴스 보기 개체의 누락된 속성(ComputerName, OsName, OsVersion 및 HyperVGeneration)을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2402">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="76011-2403">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="76011-2403">Az.ContainerRegistry</span></span>
* <span data-ttu-id="76011-2404">복제 매개 변수의 Remove-AzContainerRegistryReplication에서 오타 수정</span><span class="sxs-lookup"><span data-stu-id="76011-2404">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="76011-2405">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/9633 을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="76011-2405">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="76011-2406">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="76011-2406">Az.DataFactory</span></span>
* <span data-ttu-id="76011-2407">ADF .Net SDK 버전을 4.1.0으로 업데이트</span><span class="sxs-lookup"><span data-stu-id="76011-2407">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="76011-2408">'Get-AzDataFactoryV2PipelineRun' 설명서의 오타 수정</span><span class="sxs-lookup"><span data-stu-id="76011-2408">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="76011-2409">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="76011-2409">Az.EventHub</span></span>
* <span data-ttu-id="76011-2410">SAS 토큰을 생성하기 위해 추가된 새로운 cmmdlet 추가: New-AzEventHubAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="76011-2410">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="76011-2411">'관리'만 지정된 경우 authorizationrules 권한에 대한 확인 및 오류 메시지 추가</span><span class="sxs-lookup"><span data-stu-id="76011-2411">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="76011-2412">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="76011-2412">Az.KeyVault</span></span>
* <span data-ttu-id="76011-2413">인증서 정책에 대한 KeySize 지정을 위한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="76011-2413">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="76011-2414">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="76011-2414">Az.LogicApp</span></span>
* <span data-ttu-id="76011-2415">모든 맵 유형을 나열하도록 Get-AzIntegrationAccountMap 수정</span><span class="sxs-lookup"><span data-stu-id="76011-2415">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="76011-2416">필터링을 위해 새 MapType 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="76011-2416">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="76011-2417">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="76011-2417">Az.ManagedServices</span></span>
* <span data-ttu-id="76011-2418">API 버전 2019-06-01(GA)에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="76011-2418">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="76011-2419">Az.Network</span><span class="sxs-lookup"><span data-stu-id="76011-2419">Az.Network</span></span>
* <span data-ttu-id="76011-2420">프라이빗 엔드포인트 및 프라이빗 링크 서비스에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="76011-2420">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="76011-2421">새로운 cmdlet</span><span class="sxs-lookup"><span data-stu-id="76011-2421">New cmdlets</span></span>
        - <span data-ttu-id="76011-2422">Set-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="76011-2422">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="76011-2423">Set-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="76011-2423">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="76011-2424">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="76011-2424">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="76011-2425">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="76011-2425">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="76011-2426">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="76011-2426">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="76011-2427">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="76011-2427">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="76011-2428">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="76011-2428">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="76011-2429">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="76011-2429">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="76011-2430">기능에 대한 새로운 명령이 업데이트됨: Virtualnetwork의 서브넷에 있는 PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies 플래그</span><span class="sxs-lookup"><span data-stu-id="76011-2430">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="76011-2431">업데이트된 New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="76011-2431">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="76011-2432">이 서브넷의 프라이빗 엔드포인트에 네트워크 정책을 적용할지 여부를 나타내는 선택적 매개 변수 -PrivateEndpointNetworkPoliciesFlag가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2432">Added optional parameter -PrivateEndpointNetworkPoliciesFlag that configures whether to apply network policies on private endpoint in this subnet.</span></span>
        - <span data-ttu-id="76011-2433">이 서브넷의 프라이빗 연결 서비스에 네트워크 정책을 적용할지 여부를 나타내는 선택적 매개 변수 -PrivateLinkServiceNetworkPoliciesFlag가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2433">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag that configures whether to apply network policies network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="76011-2434">AzPrivateLinkService의 cmdlet 매개 변수 'ServiceName'이 이전 버전과의 호환성을 위해 별칭 'ServiceName'을 사용한 'Name'으로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2434">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="76011-2435">네트워크 보안 규칙 구성에 ICMP 프로토콜 사용</span><span class="sxs-lookup"><span data-stu-id="76011-2435">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="76011-2436">다음 Cmdlet이 업데이트 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2436">Updated cmdlets</span></span>
        - <span data-ttu-id="76011-2437">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="76011-2437">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="76011-2438">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="76011-2438">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="76011-2439">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="76011-2439">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="76011-2440">New-AzVirtualNetworkGatewayConnection에 대한 구성 가능한 매개 변수로 ConnectionProtocolType (Ikev1/Ikev2) 추가</span><span class="sxs-lookup"><span data-stu-id="76011-2440">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="76011-2441">LoadBalancerFrontendIpConfiguration에 PrivateIpAddressVersion 추가</span><span class="sxs-lookup"><span data-stu-id="76011-2441">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="76011-2442">업데이트된 cmdlet:</span><span class="sxs-lookup"><span data-stu-id="76011-2442">Updated cmdlet:</span></span>
        - <span data-ttu-id="76011-2443">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="76011-2443">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="76011-2444">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="76011-2444">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="76011-2445">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="76011-2445">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="76011-2446">프로브에서 사용자 지정 포트를 지원하기 위한 Application Gateway New-AzApplicationGatewayProbeConfig 명령 업데이트</span><span class="sxs-lookup"><span data-stu-id="76011-2446">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="76011-2447">업데이트된 New-AzApplicationGatewayProbeConfig: 백 엔드 서버 검색에 사용되는 선택적 매개 변수 포트가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2447">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="76011-2448">이 매개 변수는 Standard_V2 및 WAF_V2 SKU에 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2448">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="76011-2449">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="76011-2449">Az.OperationalInsights</span></span>
* <span data-ttu-id="76011-2450">저장된 검색의 기본 버전이 1로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2450">Updated default version for saved searches to be 1.</span></span>
* <span data-ttu-id="76011-2451">사용자 지정 로그 null regex 처리가 수정됨</span><span class="sxs-lookup"><span data-stu-id="76011-2451">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="76011-2452">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="76011-2452">Az.RecoveryServices</span></span>
* <span data-ttu-id="76011-2453">'Get-AzRecoveryServicesBackupJob.md' 업데이트</span><span class="sxs-lookup"><span data-stu-id="76011-2453">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="76011-2454">'Get-AzRecoveryServicesBackupContainer.md' 업데이트</span><span class="sxs-lookup"><span data-stu-id="76011-2454">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="76011-2455">'Get-AzRecoveryServicesVault.md' 업데이트</span><span class="sxs-lookup"><span data-stu-id="76011-2455">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="76011-2456">'Wait-AzRecoveryServicesBackupJob.md' 업데이트</span><span class="sxs-lookup"><span data-stu-id="76011-2456">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="76011-2457">'Set-AzRecoveryServicesVaultContext.md' 업데이트</span><span class="sxs-lookup"><span data-stu-id="76011-2457">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="76011-2458">'Get-AzRecoveryServicesBackupItem.md' 업데이트</span><span class="sxs-lookup"><span data-stu-id="76011-2458">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="76011-2459">'Get-AzRecoveryServicesBackupRecoveryPoint.md' 업데이트</span><span class="sxs-lookup"><span data-stu-id="76011-2459">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="76011-2460">'Restore-AzRecoveryServicesBackupItem.md' 업데이트</span><span class="sxs-lookup"><span data-stu-id="76011-2460">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="76011-2461">Azure 파일 공유용 컨테이너를 등록 취소하기 위해 서비스 요청 업데이트</span><span class="sxs-lookup"><span data-stu-id="76011-2461">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="76011-2462">'Set-AzRecoveryServicesAsrAlertSetting.md' 업데이트</span><span class="sxs-lookup"><span data-stu-id="76011-2462">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="76011-2463">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="76011-2463">Az.Resources</span></span>
- <span data-ttu-id="76011-2464">'New-AzResourceGroupDeployment' 설명서에서 참조된 누락 cmdlet 제거</span><span class="sxs-lookup"><span data-stu-id="76011-2464">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="76011-2465">새 API 버전 2019-01-01을 사용하도록 정책 cmdlet 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="76011-2465">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="76011-2466">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="76011-2466">Az.ServiceBus</span></span>
* <span data-ttu-id="76011-2467">SAS 토큰을 생성하기 위해 추가된 새로운 cmmdlet 추가: New-AzServiceBusAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="76011-2467">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="76011-2468">'관리'만 지정된 경우 authorizationrules 권한에 대한 확인 및 오류 메시지 추가</span><span class="sxs-lookup"><span data-stu-id="76011-2468">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="76011-2469">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="76011-2469">Az.Sql</span></span>
* <span data-ttu-id="76011-2470">Set-AzSqlDatabaseSecondary cmdlet에 대한 누락된 예제 수정</span><span class="sxs-lookup"><span data-stu-id="76011-2470">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="76011-2471">이메일 주소를 제공하지 않고 설정된 취약성 평가 반복 검색 수정</span><span class="sxs-lookup"><span data-stu-id="76011-2471">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="76011-2472">경고 메시지의 작은 오타를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2472">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="76011-2473">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="76011-2473">Az.Storage</span></span>
* <span data-ttu-id="76011-2474">'Get-AzStorageAccount'에 대한 참조 설명서의 예제를 업데이트하여 올바른 매개 변수 이름 사용</span><span class="sxs-lookup"><span data-stu-id="76011-2474">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="76011-2475">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="76011-2475">Az.StorageSync</span></span>
* <span data-ttu-id="76011-2476">Invoke-AzStorageSyncChangeDetection cmdlet을 추가하는 중입니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2476">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="76011-2477">TierFilesOlderThanDays를 기념하는 문제 9551 수정</span><span class="sxs-lookup"><span data-stu-id="76011-2477">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="76011-2478">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="76011-2478">Az.Websites</span></span>
* <span data-ttu-id="76011-2479">Get-AzWebApp 및 Set-AzWebApp에서 일부 SiteConfig 속성을 반환하지 않은 버그 수정</span><span class="sxs-lookup"><span data-stu-id="76011-2479">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="76011-2480">Get-AzDeletedWebApp 및 Restore-AzDeletedWebApp에 새 위치 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="76011-2480">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="76011-2481">AzWebApp-IncludeSourceWebAppSlots을 사용하여 웹앱 슬롯을 복제하는 버그를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2481">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="76011-2482">2.4.0 - 2019년 7월</span><span class="sxs-lookup"><span data-stu-id="76011-2482">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="76011-2483">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="76011-2483">Az.Accounts</span></span>
* <span data-ttu-id="76011-2484">프로필 cmdlet에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="76011-2484">Add support for profile cmdlets</span></span>
* <span data-ttu-id="76011-2485">생성된 cmdlet에서 환경 및 데이터 평면에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="76011-2485">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="76011-2486">Windows PowerShell의 데이터 평면 cmdlet에대해 일부 경우 잘못된 엔드포인트가 사용되는 버그 수정</span><span class="sxs-lookup"><span data-stu-id="76011-2486">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="76011-2487">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="76011-2487">Az.Advisor</span></span>
* <span data-ttu-id="76011-2488">Az.Advisor의 GA 릴리스</span><span class="sxs-lookup"><span data-stu-id="76011-2488">GA release of Az.Advisor</span></span>
* <span data-ttu-id="76011-2489">이 모듈은 이제 롤업 `Az` 모듈의 일부로 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2489">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="76011-2490">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="76011-2490">Az.ApiManagement</span></span>
* <span data-ttu-id="76011-2491">문제 https://github.com/Azure/azure-powershell/issues/8671 수정</span><span class="sxs-lookup"><span data-stu-id="76011-2491">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="76011-2492">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="76011-2492">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="76011-2493">사용자 및 제품별 구독을 쿼리하기 위한 지원이 추가됨</span><span class="sxs-lookup"><span data-stu-id="76011-2493">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="76011-2494">범위 '/', '/ api, '/ api/echo api'를 사용하여 쿼리하기 위한 지원이 추가됨</span><span class="sxs-lookup"><span data-stu-id="76011-2494">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="76011-2495">[https://github.com/Azure/azure-powershell/issues/9307](https://github.com/Azure/azure-powershell/issues/9307 ) 및 https://github.com/Azure/azure-powershell/issues/8432 문제 수정</span><span class="sxs-lookup"><span data-stu-id="76011-2495">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="76011-2496">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="76011-2496">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="76011-2497">Apis를 가져올 때 'ApiVersion' 및 'ApiVersionSetId'를 지정하기 위한 지원이 추가됨</span><span class="sxs-lookup"><span data-stu-id="76011-2497">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="76011-2498">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="76011-2498">Az.Automation</span></span>
* <span data-ttu-id="76011-2499">문자열 값을 처리하기 위해 Set-AzAutomationConnectionFieldValue cmdlet 버그를 수정했습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2499">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="76011-2500">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="76011-2500">Az.Compute</span></span>
* <span data-ttu-id="76011-2501">New-AzImageConfig에 HyperVGeneration 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="76011-2501">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="76011-2502">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="76011-2502">Az.DataFactory</span></span>
* <span data-ttu-id="76011-2503">get activity runs, get pipeline runs, get trigger runs ADF cmdlet의 출력을 업데이트하여 Select-Object pipe를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2503">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="76011-2504">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="76011-2504">Az.EventGrid</span></span>
* <span data-ttu-id="76011-2505">'New-AzEventGridSubcription' 설명서의 오타 수정</span><span class="sxs-lookup"><span data-stu-id="76011-2505">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="76011-2506">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="76011-2506">Az.IotHub</span></span>
* <span data-ttu-id="76011-2507">권한 부여 정책 키를 다시 생성하기 위한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="76011-2507">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="76011-2508">Az.Network</span><span class="sxs-lookup"><span data-stu-id="76011-2508">Az.Network</span></span>
* <span data-ttu-id="76011-2509">'RoutingPreference'를 공용 IP 태그에 추가함</span><span class="sxs-lookup"><span data-stu-id="76011-2509">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="76011-2510">'Get-AzNetworkServiceTag' 참조 설명서의 예제 개선</span><span class="sxs-lookup"><span data-stu-id="76011-2510">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="76011-2511">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="76011-2511">Az.PolicyInsights</span></span>
* <span data-ttu-id="76011-2512">Get-AzPolicyState의 null 참조 문제 해결</span><span class="sxs-lookup"><span data-stu-id="76011-2512">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="76011-2513">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/9446 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="76011-2513">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="76011-2514">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="76011-2514">Az.OperationalInsights</span></span>
* <span data-ttu-id="76011-2515">Get-AzOperationalInsightsDataSource에 반환된 CustomLog datasource 모델 수정됨</span><span class="sxs-lookup"><span data-stu-id="76011-2515">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="76011-2516">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="76011-2516">Az.RecoveryServices</span></span>
* <span data-ttu-id="76011-2517">IaaSVMs에 대한 get-policy 명령 수정</span><span class="sxs-lookup"><span data-stu-id="76011-2517">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="76011-2518">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="76011-2518">Az.Resources</span></span>
    - <span data-ttu-id="76011-2519">Get-AzPolicyState -Top 매개 변수에 대한 도움말 텍스트 수정</span><span class="sxs-lookup"><span data-stu-id="76011-2519">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="76011-2520">Get-AzPolicyAlias에 대한 클라이언트 쪽 페이징 지원 추가</span><span class="sxs-lookup"><span data-stu-id="76011-2520">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="76011-2521">Set-AzPolicyAssignment, -PolicyParameters 및 -PolicyParametersObject에 대한 새 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="76011-2521">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="76011-2522">Policy cmdlet에 대한 몇 가지 문서 및 예제 업데이트</span><span class="sxs-lookup"><span data-stu-id="76011-2522">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="76011-2523">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="76011-2523">Az.ServiceBus</span></span>
* <span data-ttu-id="76011-2524">문제 #4938 수정 - MaxSizeInMegabytes를 설정할 때 New-AzureRmServiceBusQueue가 BadRequest 반환</span><span class="sxs-lookup"><span data-stu-id="76011-2524">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="76011-2525">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="76011-2525">Az.Sql</span></span>
* <span data-ttu-id="76011-2526">미리 보기 릴리스에서 공개 릴리스로 인스턴스 장애 조치(Failover) 그룹 cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="76011-2526">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="76011-2527">새 cmdlet으로 Azure SQL Server\Database Auditing을 지원하세요.</span><span class="sxs-lookup"><span data-stu-id="76011-2527">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="76011-2528">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="76011-2528">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="76011-2529">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="76011-2529">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="76011-2530">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="76011-2530">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="76011-2531">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="76011-2531">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="76011-2532">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="76011-2532">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="76011-2533">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="76011-2533">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="76011-2534">취약성 평가 설정에서 이메일 제약 조건 제거</span><span class="sxs-lookup"><span data-stu-id="76011-2534">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="76011-2535">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="76011-2535">Az.Storage</span></span>
* <span data-ttu-id="76011-2536">다음 cmdlet에서 2개의 매개 변수 '-IndexDocument' 및 '-ErrorDocument404Path'를 필수에서 선택으로 변경하세요.</span><span class="sxs-lookup"><span data-stu-id="76011-2536">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="76011-2537">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="76011-2537">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="76011-2538">예제를 추가하여 Get-AzStorageBlobContent의 도움말 업데이트</span><span class="sxs-lookup"><span data-stu-id="76011-2538">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="76011-2539">StorageException으로 cmdlet이 실패한 경우 자세한 오류 정보 표시</span><span class="sxs-lookup"><span data-stu-id="76011-2539">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="76011-2540">Azure Files AAD DS 인증으로 스토리지 계정 생성 또는 업데이트 지원</span><span class="sxs-lookup"><span data-stu-id="76011-2540">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="76011-2541">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="76011-2541">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="76011-2542">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="76011-2542">Set-AzStorageAccount</span></span>
* <span data-ttu-id="76011-2543">파일 공유, 파일 디렉터리 또는 파일의 목록 지원 또는 파일 핸들 닫기</span><span class="sxs-lookup"><span data-stu-id="76011-2543">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="76011-2544">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="76011-2544">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="76011-2545">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="76011-2545">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="76011-2546">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="76011-2546">Az.StorageSync</span></span>
* <span data-ttu-id="76011-2547">이 모듈은 이제 롤업 `Az` 모듈의 일부로 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2547">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="76011-2548">2.3.2 - 2019년 6월</span><span class="sxs-lookup"><span data-stu-id="76011-2548">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="76011-2549">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="76011-2549">Az.Accounts</span></span>
* <span data-ttu-id="76011-2550">함수 호출에 대해 일부 경우 잘못된 URL이 사용되는 버그 수정</span><span class="sxs-lookup"><span data-stu-id="76011-2550">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="76011-2551">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/8983 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="76011-2551">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="76011-2552">AzureRM에서 Az cmdlet으로의 별칭 문제 해결</span><span class="sxs-lookup"><span data-stu-id="76011-2552">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="76011-2553">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="76011-2553">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="76011-2554">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="76011-2554">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="76011-2555">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="76011-2555">Az.Compute</span></span>
* <span data-ttu-id="76011-2556">New-AzVm 및 New-AzVmss 단순 매개 변수 집합은 이제 'ProximityPlacementGroup'매개 변수를 허용합니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2556">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="76011-2557">'New-AzVM' 참조 설명서에서 오타 수정</span><span class="sxs-lookup"><span data-stu-id="76011-2557">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="76011-2558">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="76011-2558">Az.Dns</span></span>
* <span data-ttu-id="76011-2559">'Set-AzDnsZone' 도움말 예제의 오타가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2559">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="76011-2560">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="76011-2560">Az.EventGrid</span></span>
* <span data-ttu-id="76011-2561">2019-06-01 API 버전을 사용하도록 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2561">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="76011-2562">새 cmdlet:</span><span class="sxs-lookup"><span data-stu-id="76011-2562">New cmdlets:</span></span>
    - <span data-ttu-id="76011-2563">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="76011-2563">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="76011-2564">새 Azure Event Grid 도메인을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2564">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="76011-2565">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="76011-2565">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="76011-2566">Event Grid 도메인의 세부 정보를 가져오거나 현재 Azure 구독의 모든 Event Grid 도메인 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2566">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="76011-2567">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="76011-2567">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="76011-2568">Azure Event Grid 도메인을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2568">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="76011-2569">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="76011-2569">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="76011-2570">Azure Event Grid 도메인에 대한 공유 액세스 키를 다시 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2570">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="76011-2571">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="76011-2571">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="76011-2572">Event Grid 도메인 이벤트를 게시하는 데 사용되는 공유 액세스 키를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2572">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="76011-2573">New-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="76011-2573">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="76011-2574">새 Azure Event Grid 도메인 토픽을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2574">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="76011-2575">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="76011-2575">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="76011-2576">Event Grid 도메인 토픽의 세부 사항을 가져오거나, 현재 Azure의 특정 Event Grid 도메인 아래의 모든 Event Grid 도메인 토픽 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2576">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span>
    - <span data-ttu-id="76011-2577">Remove-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="76011-2577">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="76011-2578">기존 Azure Event Grid 도메인 토픽을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2578">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="76011-2579">다음 Cmdlet이 업데이트 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2579">Updated cmdlets:</span></span>
    - <span data-ttu-id="76011-2580">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="76011-2580">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="76011-2581">새로운 Event Grid 도메인 및 Event Grid 도메인 토픽에 대한 파이핑을 지원하기 위해 새로운 필수 매개 변수를 추가하여 이러한 리소스 아래에 새 이벤트 구독을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2581">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="76011-2582">새로운 Event Grid 도메인 이름 및 Event Grid 도메인 토픽 이름을 지정하기 위해 새로운 필수 매개 변수를 추가하여 이러한 리소스 아래에 새 이벤트 구독을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2582">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="76011-2583">기존 매개 변수(예: EndPointType, SubjectBeginsWith 등)를 재사용할 수 있도록 도메인 및 도메인 토픽에 대한 새로운 매개 변수 집합을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2583">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="76011-2584">지정을 위한 새로운 선택적 매개 변수를 추가</span><span class="sxs-lookup"><span data-stu-id="76011-2584">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="76011-2585">이벤트 구독 만료 날짜,</span><span class="sxs-lookup"><span data-stu-id="76011-2585">Event subscription expiration date,</span></span>
            - <span data-ttu-id="76011-2586">고급 필터링 매개 변수.</span><span class="sxs-lookup"><span data-stu-id="76011-2586">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="76011-2587">대상으로 servicebusqueue에 대한 새 열거형을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2587">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="76011-2588">-IncludedEventType 옵션에서 'All' 사용을 허용하지 않고 다음으로 대체함</span><span class="sxs-lookup"><span data-stu-id="76011-2588">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span>
    - <span data-ttu-id="76011-2589">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="76011-2589">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="76011-2590">결과 페이지 매김 및 필터링을 지원하는 새로운 선택적 매개 변수(Top, ODataQuery 및 NextLink)를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2590">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="76011-2591">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="76011-2591">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="76011-2592">Event Grid 도메인 및 Event Grid 도메인 토픽에 대한 파이핑을 지원하기 위해 새로운 필수 매개 변수를 추가하여 이러한 리소스 아래에 기존 이벤트 구독을 제거할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2592">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="76011-2593">Event Grid 도메인 이름 및 Event Grid 도메인 토픽 이름을 지정하기 위해 새로운 필수 매개 변수를 추가하여 이러한 리소스 아래에 기존 이벤트 구독을 제거할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2593">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="76011-2594">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="76011-2594">Az.FrontDoor</span></span>
* <span data-ttu-id="76011-2595">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="76011-2595">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="76011-2596">변환 지원 및 새 연산자 자동 완성 값(RegEx)을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2596">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="76011-2597">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="76011-2597">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="76011-2598">새 자동 완성 값 추가</span><span class="sxs-lookup"><span data-stu-id="76011-2598">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="76011-2599">Az.Network</span><span class="sxs-lookup"><span data-stu-id="76011-2599">Az.Network</span></span>
* <span data-ttu-id="76011-2600">Microsoft Azure Virtual Network 게이트웨이 리소스에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="76011-2600">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="76011-2601">새로운 cmdlet</span><span class="sxs-lookup"><span data-stu-id="76011-2601">New cmdlets</span></span>
        - <span data-ttu-id="76011-2602">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="76011-2602">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="76011-2603">AvailablePrivateEndpointType 추가</span><span class="sxs-lookup"><span data-stu-id="76011-2603">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="76011-2604">새로운 cmdlet</span><span class="sxs-lookup"><span data-stu-id="76011-2604">New cmdlets</span></span>
        - <span data-ttu-id="76011-2605">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="76011-2605">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="76011-2606">PrivatePrivateLinkService 추가</span><span class="sxs-lookup"><span data-stu-id="76011-2606">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="76011-2607">새로운 cmdlet</span><span class="sxs-lookup"><span data-stu-id="76011-2607">New cmdlets</span></span>
        - <span data-ttu-id="76011-2608">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="76011-2608">Get-AzPrivateLinkService</span></span>
        - <span data-ttu-id="76011-2609">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="76011-2609">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="76011-2610">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="76011-2610">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="76011-2611">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="76011-2611">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="76011-2612">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="76011-2612">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="76011-2613">PrivateEndpoint 추가</span><span class="sxs-lookup"><span data-stu-id="76011-2613">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="76011-2614">새로운 cmdlet</span><span class="sxs-lookup"><span data-stu-id="76011-2614">New cmdlets</span></span>
        - <span data-ttu-id="76011-2615">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="76011-2615">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="76011-2616">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="76011-2616">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="76011-2617">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="76011-2617">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="76011-2618">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="76011-2618">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="76011-2619">기능에 대한 새로운 명령이 업데이트됨: VpnConnection 상의 UseLocalAzureIpAddress 플래그</span><span class="sxs-lookup"><span data-stu-id="76011-2619">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="76011-2620">New-AzVpnConnection이 업데이트됨: 선택적 매개 변수 -UseLocalAzureIpAddress를 추가하여 로컬 Azure IP 주소가 연결을 시작하는 동안 소스 주소로 사용되어야 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2620">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="76011-2621">Set-AzVpnConnection이 업데이트됨: 선택적 매개 변수 -UseLocalAzureIpAddress를 추가하여 로컬 Azure IP 주소가 연결을 시작하는 동안 소스 주소로 사용되어야 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2621">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="76011-2622">ExpressRoute 피어링에 읽기 전용 필드 PeeredConnections가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2622">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="76011-2623">ExpressRoute에 읽기 전용 필드 GlobalReachEnabled가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2623">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="76011-2624">ExpressRouteCircuit 모델에서 AllowGlobalReach 필드의 사용 중단을 부르는 호환성이 손상되는 변경 속성이 추가됨</span><span class="sxs-lookup"><span data-stu-id="76011-2624">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="76011-2625">AzApplicationGatewayRedirectConfiguration cmdlet에서 TargetListenerID를 사용하는 중의 8756 오류 문제가 해결됨</span><span class="sxs-lookup"><span data-stu-id="76011-2625">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="76011-2626">다시 쓰기 규칙 세트가 설정되지 못하게 하는 New-AzApplicationGatewayPathRuleConfig의 버그를 수정했습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2626">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="76011-2627">NetworkInterfaceIpConfiguration에 VirtualNetworkTaps가 표시되는 방식이 수정됨</span><span class="sxs-lookup"><span data-stu-id="76011-2627">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="76011-2628">모든 파트를 나열하도록 Cortex Get cmdlet이 수정됨</span><span class="sxs-lookup"><span data-stu-id="76011-2628">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="76011-2629">ExpressRouteGateways, VpnGateway에 대한 VirtualHub 참조 생성 수정됨</span><span class="sxs-lookup"><span data-stu-id="76011-2629">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="76011-2630">AzureFirewall 및 NatGateway의 가용성 영역에 대한 지원 추가됨</span><span class="sxs-lookup"><span data-stu-id="76011-2630">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="76011-2631">Get-AzNetworkServiceTag cmdlet 추가됨</span><span class="sxs-lookup"><span data-stu-id="76011-2631">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="76011-2632">Azure Firewall에 대한 여러 공용 IP 주소에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="76011-2632">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="76011-2633">New-AzFirewall cmdlet이 업데이트됨:</span><span class="sxs-lookup"><span data-stu-id="76011-2633">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="76011-2634">하나 이상의 공용 IP 주소 개체를 허용하는 매개 변수 -PublicIpAddress 추가됨</span><span class="sxs-lookup"><span data-stu-id="76011-2634">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="76011-2635">Virtual Network 개체를 허용하는 매개 변수 -VirtualNetwork 추가됨</span><span class="sxs-lookup"><span data-stu-id="76011-2635">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="76011-2636">방화벽 개체에 AddPublicIpAddress 및 RemovePublicIpAddress 메서드 추가됨 - 공용 IP 주소 개체를 입력으로 허용</span><span class="sxs-lookup"><span data-stu-id="76011-2636">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="76011-2637">매개 변수 -PublicIpName 및 -VirtualNetworkName이 더 이상 사용되지 않음</span><span class="sxs-lookup"><span data-stu-id="76011-2637">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span>
* <span data-ttu-id="76011-2638">기능에 대한 새로운 명령이 업데이트됨: VpnClient AAD 인증 옵션을 가상 네트워크 게이트웨이 리소스로 설정했습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2638">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span>
    - <span data-ttu-id="76011-2639">New-AzVirtualNetworkGateway가 업데이트됨: 게이트웨이에서 VpnClient AAD 인증 옵션을 설정할 수 있도록 선택적 매개 변수 AadTenantUri, AadAudienceId, AadIssuerUri가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2639">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="76011-2640">Set-AzVirtualNetworkGateway가 업데이트됨: 게이트웨이에서 VpnClient AAD 인증 옵션을 설정할 수 있도록 선택적 매개 변수 AadTenantUri, AadAudienceId, AadIssuerUri가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2640">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="76011-2641">Set-AzVirtualNetworkGateway가 업데이트됨: 게이트웨이에서 VpnClient AAD 인증 옵션을 제거할 수 있도록 선택적인 스위치 매개 변수 RemoveAadAuthentication이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2641">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="76011-2642">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="76011-2642">Az.OperationalInsights</span></span>
* <span data-ttu-id="76011-2643">'New-AzureRmOperationalInsightsWorkspace' 명령에서 **pergb2018** 가격 책정 계층 사용</span><span class="sxs-lookup"><span data-stu-id="76011-2643">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="76011-2644">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="76011-2644">Az.Resources</span></span>
* <span data-ttu-id="76011-2645">추가 템플릿 내보내기 옵션 지원</span><span class="sxs-lookup"><span data-stu-id="76011-2645">Support for additional Template Export options</span></span>
    - <span data-ttu-id="76011-2646">Export-AzResourceGroup에 '-SkipResourceNameParameterization' 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="76011-2646">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="76011-2647">Export-AzResourceGroup에 '-SkipAllParameterization' 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="76011-2647">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="76011-2648">내보낸 리소스 필터링을 위해 Export-AzResourceGroup에 '-Resource' 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="76011-2648">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="76011-2649">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="76011-2649">Az.ServiceFabric</span></span>
* <span data-ttu-id="76011-2650">일부 경우 잘못된 지문을 가져오는 추가 인증서 ByExistingKeyVault 수정</span><span class="sxs-lookup"><span data-stu-id="76011-2650">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="76011-2651">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="76011-2651">Az.Sql</span></span>
* <span data-ttu-id="76011-2652">Advanced Threat Protection 스토리지 엔드포인트 접미사 수정</span><span class="sxs-lookup"><span data-stu-id="76011-2652">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="76011-2653">Advanced Data Security가 Advanced Threat Protection 정책을 재정의하는 것을 수정</span><span class="sxs-lookup"><span data-stu-id="76011-2653">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="76011-2654">고객이 TDE 키를 추가하고 관리되는 인스턴스에 TDE 보호기를 설정할 수 있도록 Management.Sql용 새 Cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="76011-2654">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="76011-2655">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="76011-2655">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="76011-2656">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="76011-2656">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="76011-2657">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="76011-2657">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="76011-2658">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="76011-2658">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="76011-2659">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="76011-2659">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="76011-2660">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="76011-2660">Az.Storage</span></span>
* <span data-ttu-id="76011-2661">스토리지 계정 생성 시 종류 FileStorage 및 SkuName Premium_ZRS 지원</span><span class="sxs-lookup"><span data-stu-id="76011-2661">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="76011-2662">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="76011-2662">New-AzStorageAccount</span></span>
* <span data-ttu-id="76011-2663">BLOB immutability cmdlet의 설명 명확화</span><span class="sxs-lookup"><span data-stu-id="76011-2663">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="76011-2664">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="76011-2664">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="76011-2665">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="76011-2665">Az.Websites</span></span>
* <span data-ttu-id="76011-2666">Get-AzWebAppCertificate를 클라이언트 대신 서버의 리소스 그룹별로 필터링하도록 최적화</span><span class="sxs-lookup"><span data-stu-id="76011-2666">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="76011-2667">Get-AzWebAppSnapshot에 -UseDisasterRecovery 스위치 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="76011-2667">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="76011-2668">2.2.0 - 2019년 6월</span><span class="sxs-lookup"><span data-stu-id="76011-2668">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="76011-2669">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="76011-2669">Az.Cdn</span></span>
* <span data-ttu-id="76011-2670">cmdlet에서 2019-04-15 API 버전 기반의 rulesEngine 기능을 지원하도록 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2670">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="76011-2671">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="76011-2671">Az.Compute</span></span>
* <span data-ttu-id="76011-2672">작업을 시작하여 완료되기 전에 즉시 반환하는 `NoWait` 매개 변수가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2672">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="76011-2673">다음 Cmdlet이 업데이트 되었습니다.   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="76011-2673">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="76011-2674">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="76011-2674">Az.EventHub</span></span>
* <span data-ttu-id="76011-2675">#9231 수정 - Get-AzEventHubNamespace에서 태그를 반환하지 않음</span><span class="sxs-lookup"><span data-stu-id="76011-2675">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="76011-2676">#9230 수정 - Get-AzEventHubNamespace에서 ResourceGroupName 대신 ResourceGroup을 반환함</span><span class="sxs-lookup"><span data-stu-id="76011-2676">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="76011-2677">Az.Network</span><span class="sxs-lookup"><span data-stu-id="76011-2677">Az.Network</span></span>
* <span data-ttu-id="76011-2678">Nat Gateway에 대한 ResourceId 및 InputObject 업데이트</span><span class="sxs-lookup"><span data-stu-id="76011-2678">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="76011-2679">ResourceId 및 InputObject에 대한 별칭 추가</span><span class="sxs-lookup"><span data-stu-id="76011-2679">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="76011-2680">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="76011-2680">Az.PolicyInsights</span></span>
* <span data-ttu-id="76011-2681">Get-AzPolicyEvent에서 Null 참조 문제 해결</span><span class="sxs-lookup"><span data-stu-id="76011-2681">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="76011-2682">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="76011-2682">Az.RecoveryServices</span></span>
* <span data-ttu-id="76011-2683">IaaSVM 정책 최소 보존 기간(일)이 1에서 7로 변경됨</span><span class="sxs-lookup"><span data-stu-id="76011-2683">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="76011-2684">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="76011-2684">Az.ServiceBus</span></span>
* <span data-ttu-id="76011-2685">#9182 문제 해결 - Get-AzServiceBusNamespace에서 ResourceGroupName 대신 ResourceGroup을 반환</span><span class="sxs-lookup"><span data-stu-id="76011-2685">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="76011-2686">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="76011-2686">Az.ServiceFabric</span></span>
* <span data-ttu-id="76011-2687">'Update-AzServiceFabricReliability' 오류 메시지의 오타 수정</span><span class="sxs-lookup"><span data-stu-id="76011-2687">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="76011-2688">Service Fabric 명령줄에서 누락된 문자 수정</span><span class="sxs-lookup"><span data-stu-id="76011-2688">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="76011-2689">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="76011-2689">Az.Sql</span></span>
* <span data-ttu-id="76011-2690">Managed Instance에 대한 AutoDr을 지원하기 위해 New-AzureSqlInstance cmdlet에 대한 DnsZonePartner 매개 변수를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2690">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="76011-2691">Get-AzSqlDatabaseSecureConnectionPolicy cmdlet 사용 중단</span><span class="sxs-lookup"><span data-stu-id="76011-2691">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="76011-2692">Threat Detection(위협 탐지) cmdlet 이름을 Advanced Threat Protection으로 변경함</span><span class="sxs-lookup"><span data-stu-id="76011-2692">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="76011-2693">새 AzSqlInstance -StorageSizeInGB 및 -LicenseType 매개 변수는 이제 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2693">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="76011-2694">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="76011-2694">Az.Websites</span></span>
* <span data-ttu-id="76011-2695">-WebApp 속성에서 Set-AzWebApp 및 Set-AzWebAppSlot을 사용하면 태그가 제거되는 문제를 해결함</span><span class="sxs-lookup"><span data-stu-id="76011-2695">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="76011-2696">2.1.0 - 2019년 5월</span><span class="sxs-lookup"><span data-stu-id="76011-2696">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="76011-2697">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="76011-2697">Az.ApiManagement</span></span>
* <span data-ttu-id="76011-2698">글로벌 및 API 범위에서 진단을 관리하기 위한 새 cmdlet을 만들었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2698">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="76011-2699">**Get-AzApiManagementDiagnostic** - 글로벌 또는 API 범위가 구성된 진단 가져오기</span><span class="sxs-lookup"><span data-stu-id="76011-2699">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="76011-2700">**New-AzApiManagementDiagnostic** - 글로벌 범위 또는 API 범위에서 새 진단 만들기</span><span class="sxs-lookup"><span data-stu-id="76011-2700">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="76011-2701">**New-AzApiManagementHttpMessageDiagnostic** - 기록할 Headers(헤더) 및 Body Bytes(본문 바이트 수) 크기에 대한 진단 설정 만들기</span><span class="sxs-lookup"><span data-stu-id="76011-2701">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="76011-2702">**New-AzApiManagementPipelineDiagnosticSetting** - 게이트웨이로 들어오고 나가는 HTTP 메시지에 대한 진단 설정 만들기</span><span class="sxs-lookup"><span data-stu-id="76011-2702">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="76011-2703">**New-AzApiManagementSamplingSetting** - 진단 요청/응답에 대한 샘플링 설정 만들기</span><span class="sxs-lookup"><span data-stu-id="76011-2703">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="76011-2704">**Remove-AzApiManagementDiagnostic** - 글로벌 또는 API 범위에서 진단 엔터티 제거</span><span class="sxs-lookup"><span data-stu-id="76011-2704">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="76011-2705">**Set-AzApiManagementDiagnostic** - 글로벌 또는 API 범위에서 진단 엔터티 업데이트</span><span class="sxs-lookup"><span data-stu-id="76011-2705">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="76011-2706">ApiManagement 서비스에서 캐시를 관리하기 위한 새 cmdlet을 만들었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2706">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="76011-2707">**Get-AzApiManagementCache** - 식별자 또는 모든 캐시로 지정된 캐시의 세부 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="76011-2707">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="76011-2708">**New-AzApiManagementCache** - 특정 Azure 'region'(지역)에 새 'default'(기본) 캐시 만들기</span><span class="sxs-lookup"><span data-stu-id="76011-2708">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="76011-2709">**Remove-AzApiManagementCache** - 캐시 제거</span><span class="sxs-lookup"><span data-stu-id="76011-2709">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="76011-2710">**Update-AzApiManagementCache** - 캐시 업데이트</span><span class="sxs-lookup"><span data-stu-id="76011-2710">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="76011-2711">API 스키마 관리하기 위한 새 cmdlet을 만들었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2711">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="76011-2712">**New-AzApiManagementSchema** - API에 대한 새 스키마 만들기</span><span class="sxs-lookup"><span data-stu-id="76011-2712">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="76011-2713">**Get-AzApiManagementSchema** - API에 구성된 스키마 가져오기</span><span class="sxs-lookup"><span data-stu-id="76011-2713">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="76011-2714">**Remove-AzApiManagementSchema** - API에 구성된 스키마 제거</span><span class="sxs-lookup"><span data-stu-id="76011-2714">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="76011-2715">**Set-AzApiManagementSchema** - API에 구성된 스키마 업데이트</span><span class="sxs-lookup"><span data-stu-id="76011-2715">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="76011-2716">사용자 토큰을 생성하기 위한 새 cmdlet을 만들었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2716">Created new Cmdlet for generating a User Token.</span></span>
    - <span data-ttu-id="76011-2717">**New-AzApiManagementUserToken** - 기본적으로 8시간 동안 유효한 새 사용자 토큰을 생성합니다. 'GIT' 사용자에 대한 토큰은 이 cmdlet을 사용하여 생성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2717">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="76011-2718">네트워크 상태를 검색하기 위한 새 cmdlet을 만들었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2718">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="76011-2719">**Get-AzApiManagementNetworkStatus** - API Management 서비스에서 사용하는 리소스의 네트워크 상태 연결을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2719">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="76011-2720">ApiManagement 서비스를 가상 네트워크에 배포하고 종속성이 손상되었는지 여부를 확인할 때 유용합니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2720">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="76011-2721">**New-AzApiManagement** cmdlet에서 ApiManagement 서비스를 관리하도록 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2721">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span>
    - <span data-ttu-id="76011-2722">새 '소비' SKU 지원이 추가됨</span><span class="sxs-lookup"><span data-stu-id="76011-2722">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="76011-2723">'소비' SKU에 대해 'EnableClientCertificate' 플래그를 설정하기 위한 지원이 추가됨</span><span class="sxs-lookup"><span data-stu-id="76011-2723">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="76011-2724">새 **New-AzApiManagementSslSetting** cmdlet을 사용하면 'Backend(백 엔드)' 및 'Frontend'(프런트 엔드)에서 'TLS/SSL' 설정을 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2724">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="76011-2725">또한 ApiManagement 서비스의 'Frontend'에서 '3DES'와 같은 'Ciphers'와 'Http2'와 같은 'ServerProtocols'를 구성하는 데 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2725">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="76011-2726">ApiManagement 서비스에서 'DeveloperPortal' 호스트 이름을 구성하기 위한 지원이 추가됨</span><span class="sxs-lookup"><span data-stu-id="76011-2726">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="76011-2727">**Get-AzApiManagementSsoToken** cmdlet에서 'PsApiManagement' 개체를 입력으로 사용하도록 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2727">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="76011-2728">cmdlet에서 오류 메시지를 인라인으로 표시하도록 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2728">Updated the cmdlet to display Error Messages inline</span></span>
     > <span data-ttu-id="76011-2729">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : 오류 코드: ValidationError 오류 메시지: 하나 이상의 필드에 잘못된 값이 있습니다. 오류 세부 정보:    [Code=ValidationError, Message=줄 3, 열 10의 'log-to-eventhub' 요소에 오류가 있습니다.: 로거를 찾지 못함, Target=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="76011-2729">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="76011-2730">**Export-AzApiManagementApi** cmdlet에서 API를 'OpenApi 3.0' 형식으로 내보내도록 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2730">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="76011-2731">**Import-AzApiManagementApi** cmdlet을 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2731">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="76011-2732">'OpenApi 3.0' 문서 사양에서 API 가져오기</span><span class="sxs-lookup"><span data-stu-id="76011-2732">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="76011-2733">문서('Swagger', 'Wadl', 'Wsdl', 'OpenApi')에 지정된 'PsApiManagementSchema' 속성 재정의</span><span class="sxs-lookup"><span data-stu-id="76011-2733">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="76011-2734">문서에 지정된 'ServiceUrl' 속성 재정의</span><span class="sxs-lookup"><span data-stu-id="76011-2734">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="76011-2735">**Get-AzApiManagementPolicy** cmdlet에서 'rawxml'을 사용하여 이스케이프된 비 Xml 'format'(형식)의 정책을 반환하도록 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2735">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="76011-2736">**Set-AzApiManagementPolicy** cmdlet에서 'rawxml'을 사용하여 이스케이프된 비 Xml 'format'의 정책을 수락하고, 'xml'을 사용하여 이스케이프된 Xml 'format'의 정책을 수락하도록 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2736">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="76011-2737">**New-AzApiManagementApi** cmdlet을 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2737">Updated cmdlet **New-AzApiManagementApi**</span></span>
    - <span data-ttu-id="76011-2738">'OpenId' 권한 부여 서버를 사용하여 API 구성</span><span class="sxs-lookup"><span data-stu-id="76011-2738">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="76011-2739">'ApiVersionSet'에서 API 만들기</span><span class="sxs-lookup"><span data-stu-id="76011-2739">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="76011-2740">'SourceApiId' 및 'SourceApiRevision'을 사용하여 API 복제</span><span class="sxs-lookup"><span data-stu-id="76011-2740">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="76011-2741">API 범위에서 'SubscriptionRequired' 구성 가능</span><span class="sxs-lookup"><span data-stu-id="76011-2741">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="76011-2742">**Set-AzApiManagementApi** cmdlet을 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2742">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="76011-2743">'OpenId' 권한 부여 서버를 사용하여 API 구성</span><span class="sxs-lookup"><span data-stu-id="76011-2743">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="76011-2744">API를 'ApiVersionSet'으로 업데이트</span><span class="sxs-lookup"><span data-stu-id="76011-2744">To updated an API into an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="76011-2745">API 범위에서 'SubscriptionRequired' 구성 가능</span><span class="sxs-lookup"><span data-stu-id="76011-2745">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="76011-2746">**New-AzApiManagementRevision** cmdlet을 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2746">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="76011-2747">'SourceApiRevision'을 사용하여 기존 수정 버전 복제(태그, 제품, 작업 및 정책 복사).</span><span class="sxs-lookup"><span data-stu-id="76011-2747">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="76011-2748">새 수정 버전은 부모의 'ApiId'를 가정합니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2748">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="76011-2749">'ApiRevisionDescription' 제공</span><span class="sxs-lookup"><span data-stu-id="76011-2749">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="76011-2750">API 복제 시 'ServiceUrl' 재정의</span><span class="sxs-lookup"><span data-stu-id="76011-2750">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="76011-2751">**New-AzApiManagementIdentityProvider** cmdlet을 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2751">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="76011-2752">'Authority'를 사용하여 'AAD' 또는 'AADB2C' 구성</span><span class="sxs-lookup"><span data-stu-id="76011-2752">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="76011-2753">'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' 및 'PasswordResetPolicy' 설정</span><span class="sxs-lookup"><span data-stu-id="76011-2753">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="76011-2754">**New-AzApiManagementSubscription** cmdlet을 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2754">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="76011-2755">'Scope' 및 'UserId'를 사용하여 새 SubscriptonModel 설명</span><span class="sxs-lookup"><span data-stu-id="76011-2755">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="76011-2756">'ProductId' 및 'UserId'를 사용하여 이전 구독 모델 설명</span><span class="sxs-lookup"><span data-stu-id="76011-2756">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="76011-2757">구독 수준에서 'AllowTracing'을 사용하도록 설정하는 지원 추가</span><span class="sxs-lookup"><span data-stu-id="76011-2757">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="76011-2758">**Set-AzApiManagementSubscription** cmdlet을 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2758">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="76011-2759">'Scope' 및 'UserId'를 사용하여 새 SubscriptonModel 설명</span><span class="sxs-lookup"><span data-stu-id="76011-2759">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="76011-2760">'ProductId' 및 'UserId'를 사용하여 이전 구독 모델 설명</span><span class="sxs-lookup"><span data-stu-id="76011-2760">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="76011-2761">구독 수준에서 'AllowTracing'을 사용하도록 설정하는 지원 추가</span><span class="sxs-lookup"><span data-stu-id="76011-2761">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="76011-2762">다음 cmdlet에서 'ResourceId'를 입력으로 수락하도록 업데이트했습니다</span><span class="sxs-lookup"><span data-stu-id="76011-2762">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="76011-2763">'New-AzApiManagementContext'</span><span class="sxs-lookup"><span data-stu-id="76011-2763">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="76011-2764">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="76011-2764">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="76011-2765">'Get-AzApiManagementApiRelease'</span><span class="sxs-lookup"><span data-stu-id="76011-2765">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="76011-2766">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="76011-2766">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="76011-2767">'Get-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="76011-2767">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="76011-2768">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="76011-2768">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="76011-2769">'Get-AzApiManagementAuthorizationServer'</span><span class="sxs-lookup"><span data-stu-id="76011-2769">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="76011-2770">'Get-AzApiManagementBackend'</span><span class="sxs-lookup"><span data-stu-id="76011-2770">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="76011-2771">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="76011-2771">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="76011-2772">'Get-AzApiManagementCertificate'</span><span class="sxs-lookup"><span data-stu-id="76011-2772">'Get-AzApiManagementCertificate'</span></span>
    - <span data-ttu-id="76011-2773">'Remove-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="76011-2773">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="76011-2774">'Remove-AzApiManagementSubscription'</span><span class="sxs-lookup"><span data-stu-id="76011-2774">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="76011-2775">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="76011-2775">Az.Automation</span></span>
* <span data-ttu-id="76011-2776">Get-AzAutomationJobOutputRecord에서 JSON 및 Text 레코드 값을 처리하도록 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2776">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="76011-2777">문제 https://github.com/Azure/azure-powershell/issues/7977 수정</span><span class="sxs-lookup"><span data-stu-id="76011-2777">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="76011-2778">문제 https://github.com/Azure/azure-powershell/issues/8600 수정</span><span class="sxs-lookup"><span data-stu-id="76011-2778">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="76011-2779">Start-AzAutomationDscCompilationJob에서 완료될 때까지 기다리지 않고 작업을 바로 시작하도록 변경했습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2779">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="76011-2780">문제 https://github.com/Azure/azure-powershell/issues/8347 수정</span><span class="sxs-lookup"><span data-stu-id="76011-2780">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="76011-2781">-Name을 사용하면 모든 노드를 반환하는 Get-AzAutomationDscNode 수정.</span><span class="sxs-lookup"><span data-stu-id="76011-2781">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="76011-2782">이제 일치하는 노드만 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2782">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="76011-2783">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="76011-2783">Az.Compute</span></span>
* <span data-ttu-id="76011-2784">ProtectFromScaleIn 및 ProtectFromScaleSetAction 매개 변수를 Update-AzVmssVM cmdlet에 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2784">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="76011-2785">'East US'(미국 동부)가 지원되지 않는 경우 이제 New-AzVM wimple 매개 변수 집합에서 기본적으로 사용 가능한 위치를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2785">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="76011-2786">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="76011-2786">Az.DataLakeStore</span></span>
* <span data-ttu-id="76011-2787">ADLS SDK에서 httpclient를 사용하도록 업데이트하고, 데이터 평면 테스트를 Azure 프레임워크와 통합합니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2787">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="76011-2788">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="76011-2788">Az.Monitor</span></span>
* <span data-ttu-id="76011-2789">도움말 예제에서 잘못된 매개 변수 이름을 수정했습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2789">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="76011-2790">Az.Network</span><span class="sxs-lookup"><span data-stu-id="76011-2790">Az.Network</span></span>
* <span data-ttu-id="76011-2791">DisableBgpRoutePropagation 플래그를 유효 경로 테이블 출력에 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2791">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="76011-2792">업데이트된 cmdlet:</span><span class="sxs-lookup"><span data-stu-id="76011-2792">Updated cmdlet:</span></span>
        - <span data-ttu-id="76011-2793">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="76011-2793">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="76011-2794">New-AzApplicationGatewayTrustedRootCertificate 설명서에서 이중 파선을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2794">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="76011-2795">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="76011-2795">Az.Resources</span></span>
* <span data-ttu-id="76011-2796">할당 거부를 검색하기 위한 새 Get-AzureRmDenyAssignment cmdlet을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2796">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="76011-2797">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="76011-2797">Az.Sql</span></span>
* <span data-ttu-id="76011-2798">Advanced Threat Protection cmdlet의 이름을 Advanced Data Security로 변경하고, 취약성 평가를 기본적으로 사용하도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2798">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="76011-2799">2.0.0 - 2019년 5월</span><span class="sxs-lookup"><span data-stu-id="76011-2799">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="76011-2800">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="76011-2800">Az.Accounts</span></span>
* <span data-ttu-id="76011-2801">사용자 이름/비밀번호 인증을 사용하여 ADFS 문제를 해결하도록 인증 라이브러리 업데이트</span><span class="sxs-lookup"><span data-stu-id="76011-2801">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="76011-2802">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="76011-2802">Az.CognitiveServices</span></span>
* <span data-ttu-id="76011-2803">Bing Search 서비스에 대해서만 Bing 면책 조항을 표시하세요.</span><span class="sxs-lookup"><span data-stu-id="76011-2803">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="76011-2804">계정 생성 실패 시 오류 개선.</span><span class="sxs-lookup"><span data-stu-id="76011-2804">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="76011-2805">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="76011-2805">Az.Compute</span></span>
* <span data-ttu-id="76011-2806">근접 배치 그룹 기능</span><span class="sxs-lookup"><span data-stu-id="76011-2806">Proximity placement group feature.</span></span>
    - <span data-ttu-id="76011-2807">다음과 같은 새 cmdlet을 추가했습니다.   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="76011-2807">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="76011-2808">새 매개 변수 ProximityPlacementGroupId가 다음 cmdlet에 추가됩니다.   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="76011-2808">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="76011-2809">New-AzGalleryImageVersion에 StorageAccountType 매개 변수가 추가됩니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2809">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="76011-2810">New-AzGalleryImageVersion의 TargetRegion이 StorageAccountType를 포함할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2810">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="76011-2811">SkipShutdown 스위치 매개 변수가 Stop-AzVM 및 Stop-AzVmss에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2811">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>
* <span data-ttu-id="76011-2812">주요 변경 내용</span><span class="sxs-lookup"><span data-stu-id="76011-2812">Breaking changes</span></span>
    - <span data-ttu-id="76011-2813">Set-AzVMBootDiagnostics이 Set-AzVMBootDiagnostic으로 변경됩니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2813">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="76011-2814">Export-AzLogAnalyticThrottledRequests이 Export-AzLogAnalyticThrottledRequests로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2814">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="76011-2815">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="76011-2815">Az.DeploymentManager</span></span>
* <span data-ttu-id="76011-2816">Azure 배포 관리자 cmdlet의 일반적으로 사용 가능한 첫 번째 릴리스</span><span class="sxs-lookup"><span data-stu-id="76011-2816">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="76011-2817">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="76011-2817">Az.Dns</span></span>
* <span data-ttu-id="76011-2818">자동 DNS 이름 서버 위임</span><span class="sxs-lookup"><span data-stu-id="76011-2818">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="76011-2819">DNS 영역 만들기 cmdlet은 추가 선택적 매개 변수로 부모 영역 이름을 허용합니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2819">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="76011-2820">새로 생성 된 자식 영역의 부모 영역에 NS 레코드를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2820">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="76011-2821">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="76011-2821">Az.FrontDoor</span></span>
* <span data-ttu-id="76011-2822">Azure FrontDoor cmdlet의 일반적으로 사용 가능한 첫 번째 릴리스</span><span class="sxs-lookup"><span data-stu-id="76011-2822">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="76011-2823">'Waf'를 포함하도록 WAF cmdlet의 이름 바꾸기</span><span class="sxs-lookup"><span data-stu-id="76011-2823">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="76011-2824">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="76011-2824">Az.HDInsight</span></span>
* <span data-ttu-id="76011-2825">두 개의 cmdlet을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2825">Removed two cmdlets:</span></span>
    - <span data-ttu-id="76011-2826">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="76011-2826">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="76011-2827">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="76011-2827">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="76011-2828">Grant-AzHDInsightHttpServicesAccess를 대체할 새 cmdlet Set-AzHDInsightGatewayCredential을 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2828">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="76011-2829">reader 역할과 HDInsight 운영자 역할을 구분하도록 cmdlet Get-AzHDInsightJobOutput 업데이트:</span><span class="sxs-lookup"><span data-stu-id="76011-2829">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="76011-2830">reader 역할을 가진 사용자는 'DefaultStorageAccountKey'매개 변수를 명시적으로 지정해야 합니다. 그렇지 않으면 오류가 발생합니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2830">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="76011-2831">Hdinsight 운영자 역할을 가진 사용자를 영향을 받지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2831">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="76011-2832">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="76011-2832">Az.Monitor</span></span>
* <span data-ttu-id="76011-2833">SQR API(예약 쿼리 규칙)용 새 cmdlet</span><span class="sxs-lookup"><span data-stu-id="76011-2833">New cmdlets for SQR API (Scheduled Query Rule)</span></span>
    - <span data-ttu-id="76011-2834">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="76011-2834">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="76011-2835">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="76011-2835">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="76011-2836">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="76011-2836">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="76011-2837">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="76011-2837">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="76011-2838">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="76011-2838">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="76011-2839">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="76011-2839">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="76011-2840">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="76011-2840">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="76011-2841">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="76011-2841">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="76011-2842">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="76011-2842">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="76011-2843">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="76011-2843">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="76011-2844">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="76011-2844">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="76011-2845">SQR API에 대한 [자세한 내용](/rest/api/monitor/scheduledqueryrules)</span><span class="sxs-lookup"><span data-stu-id="76011-2845">[More](/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="76011-2846">GenV2(비 클래식) 메트릭 기반 경고 규칙에 대한 cmdlet을 포함하도록 Az.Monitor.md가 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="76011-2846">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="76011-2847">Az.Network</span><span class="sxs-lookup"><span data-stu-id="76011-2847">Az.Network</span></span>
* <span data-ttu-id="76011-2848">Nat 게이트웨이 리소스에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="76011-2848">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="76011-2849">새로운 cmdlet</span><span class="sxs-lookup"><span data-stu-id="76011-2849">New cmdlets</span></span>
        - <span data-ttu-id="76011-2850">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="76011-2850">New-AzNatGateway</span></span>
        - <span data-ttu-id="76011-2851">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="76011-2851">Get-AzNatGateway</span></span>
        - <span data-ttu-id="76011-2852">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="76011-2852">Set-AzNatGateway</span></span>
        - <span data-ttu-id="76011-2853">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="76011-2853">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="76011-2854">다음 Cmdlet이 업데이트 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2854">Updated cmdlets</span></span>
        - <span data-ttu-id="76011-2855">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="76011-2855">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="76011-2856">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="76011-2856">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="76011-2857">기능에 대한 새로운 명령이 업데이트됨: Brooklyn Gateway에서 사용자 지정 경로 설정/제거.</span><span class="sxs-lookup"><span data-stu-id="76011-2857">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="76011-2858">New-AzVirtualNetworkGateway가 업데이트됨: 선택적 매개 변수 -CustomRoute를 추가하여 게이트웨이에서 설정할 사용자 지정 경로로 주소 접두사를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2858">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="76011-2859">Set-AzVirtualNetworkGateway가 업데이트됨: 선택적 매개 변수 -CustomRoute를 추가하여 게이트웨이에서 설정할 사용자 지정 경로로 주소 접두사를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2859">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="76011-2860">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="76011-2860">Az.PolicyInsights</span></span>
* <span data-ttu-id="76011-2861">정책 평가 세부 정보 쿼리 지원</span><span class="sxs-lookup"><span data-stu-id="76011-2861">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="76011-2862">Get-AzPolicyState에 '-Expand'매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="76011-2862">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="76011-2863">'-Expand PolicyEvaluationDetails' 지원</span><span class="sxs-lookup"><span data-stu-id="76011-2863">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="76011-2864">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="76011-2864">Az.RecoveryServices</span></span>
* <span data-ttu-id="76011-2865">크로스 구독 Azure에서 Azure 사이트 복구 지원</span><span class="sxs-lookup"><span data-stu-id="76011-2865">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="76011-2866">Azure Site Recovery에 대한 호환성이 손상되는 변경 표시</span><span class="sxs-lookup"><span data-stu-id="76011-2866">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="76011-2867">Azure Site Recovery 복구 계획 최종 실행 계획에 대한 수정</span><span class="sxs-lookup"><span data-stu-id="76011-2867">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="76011-2868">Azure에서 Azure에 대한 Azure Site Recovery 업데이트 네트워크 매핑 수정</span><span class="sxs-lookup"><span data-stu-id="76011-2868">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="76011-2869">관리 디스크에 대한 Azure에서 Azure에 대한 Azure Site Recovery 업데이트 보호 방향 수정</span><span class="sxs-lookup"><span data-stu-id="76011-2869">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="76011-2870">기타 사소한 수정.</span><span class="sxs-lookup"><span data-stu-id="76011-2870">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="76011-2871">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="76011-2871">Az.Relay</span></span>
* <span data-ttu-id="76011-2872">고객 관련 메시지의 철자 오류 수정</span><span class="sxs-lookup"><span data-stu-id="76011-2872">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="76011-2873">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="76011-2873">Az.ServiceBus</span></span>
* <span data-ttu-id="76011-2874">네임스페이스의 NetworkRuleSet에 대한 새 cmdlet가 추가되었습니다</span><span class="sxs-lookup"><span data-stu-id="76011-2874">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="76011-2875">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="76011-2875">Az.Storage</span></span>
* <span data-ttu-id="76011-2876">저장소 클라이언트 라이브러리 10.0.1로 업그레이드(이 SDK의 모든 개체의 네임스페이스가 'Microsoft.WindowsAzure.Storage. *'에서 'Microsoft.Azure.Storage.* '로 변경됨)</span><span class="sxs-lookup"><span data-stu-id="76011-2876">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="76011-2877">새로운 API 버전 2019-04-01을 지원하기 위해 Microsoft.Azure.Management.Storage 11.0.0으로 업그레이드합니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2877">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="76011-2878">스토리지 생성 계정의 기본 스토리지 계정 종류가 'Storage'에서 'StorageV2'로 변경됩니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2878">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="76011-2879">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="76011-2879">New-AzStorageAccount</span></span>
* <span data-ttu-id="76011-2880">'StandardLRS'가 'Standard_LRS'로 변경되는 것과 같이 '-'을 추가하여 입력 SkuName과 정렬되도록 스토리지 계정 cmdlet 출력 Sku.Name을 변경합니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2880">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="76011-2881">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="76011-2881">New-AzStorageAccount</span></span>
    - <span data-ttu-id="76011-2882">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="76011-2882">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="76011-2883">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="76011-2883">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="76011-2884">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="76011-2884">Az.Websites</span></span>
* <span data-ttu-id="76011-2885">Get-AzWebApp에서 반환한 PSSite 개체에 대해 'Kind'속성이 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2885">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="76011-2886">Get-AzWebApp\* 메트릭 및 Get-AzAppServicePlanMetrics가 사용되지 않음으로 표시되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2886">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="76011-2887">1.8.0 - 2019년 4월</span><span class="sxs-lookup"><span data-stu-id="76011-2887">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="76011-2888">마지막 주 릴리스 이후의 주요 사항</span><span class="sxs-lookup"><span data-stu-id="76011-2888">Highlights since the last major release</span></span>
* <span data-ttu-id="76011-2889">`Az` 모듈 일반 공급</span><span class="sxs-lookup"><span data-stu-id="76011-2889">General availability of `Az` module</span></span>
* <span data-ttu-id="76011-2890">`Az` 모듈에 대한 자세한 내용은 https://aka.ms/azps-announce 를 방문하세요.</span><span class="sxs-lookup"><span data-stu-id="76011-2890">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="76011-2891">Location, ResourceGroup 및 ResourceName 완성자가 추가되었습니다(https://azure.microsoft.com/blog/completers-in-azure-powershell/ ).</span><span class="sxs-lookup"><span data-stu-id="76011-2891">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="76011-2892">와일드카드 지원이 Az.Compute 및 Az.Network에 대한 Get cmdlet에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2892">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="76011-2893">Windows PowerShell 5.1 전용 대화형 사용자 이름/암호 인증이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2893">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="76011-2894">Python 2 Runbook 지원이 Az.Automation에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2894">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="76011-2895">Az.LogicApp: 통합 계정 어셈블리 및 일괄 처리 구성을 위한 새로운 cmdlet입니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2895">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="76011-2896">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="76011-2896">Az.Accounts</span></span>
* <span data-ttu-id="76011-2897">Mac에서 모듈을 올바르게 삭제하기 위해 Uninstall-AzureRm을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2897">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="76011-2898">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="76011-2898">Az.Batch</span></span>
* <span data-ttu-id="76011-2899">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2899">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="76011-2900">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="76011-2900">Az.Cdn</span></span>
* <span data-ttu-id="76011-2901">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2901">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="76011-2902">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="76011-2902">Az.CognitiveServices</span></span>
* <span data-ttu-id="76011-2903">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2903">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="76011-2904">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="76011-2904">Az.Compute</span></span>
* <span data-ttu-id="76011-2905">디스크의 리소스 ID에 리소스 ID의 소문자 resourcegroups가 있는 경우 AEM 설치 문제 수정</span><span class="sxs-lookup"><span data-stu-id="76011-2905">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="76011-2906">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2906">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="76011-2907">와일드 카드에 대한 설명서 수정</span><span class="sxs-lookup"><span data-stu-id="76011-2907">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="76011-2908">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="76011-2908">Az.DataFactory</span></span>
* <span data-ttu-id="76011-2909">NodeCount가 관리형 통합 런타임에 대해 Null이 아닌 경우 SsisProperties를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2909">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="76011-2910">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="76011-2910">Az.DataLakeStore</span></span>
* <span data-ttu-id="76011-2911">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2911">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="76011-2912">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="76011-2912">Az.EventGrid</span></span>
* <span data-ttu-id="76011-2913">이벤트 구독 cmdlet 만들기/업데이트를 사용하기 전에 리소스를 만들어야 함을 나타내기 위해 엔드포인트의 도움말 텍스트가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2913">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="76011-2914">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="76011-2914">Az.EventHub</span></span>
* <span data-ttu-id="76011-2915">네임스페이스의 NetworkRuleSet에 대한 새 cmdlet가 추가되었습니다</span><span class="sxs-lookup"><span data-stu-id="76011-2915">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="76011-2916">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="76011-2916">Az.HDInsight</span></span>
* <span data-ttu-id="76011-2917">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2917">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="76011-2918">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="76011-2918">Az.IotHub</span></span>
* <span data-ttu-id="76011-2919">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2919">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="76011-2920">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="76011-2920">Az.KeyVault</span></span>
* <span data-ttu-id="76011-2921">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2921">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="76011-2922">와일드 카드에 대한 설명서 수정</span><span class="sxs-lookup"><span data-stu-id="76011-2922">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="76011-2923">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="76011-2923">Az.MachineLearning</span></span>
* <span data-ttu-id="76011-2924">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2924">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="76011-2925">Az.Media</span><span class="sxs-lookup"><span data-stu-id="76011-2925">Az.Media</span></span>
* <span data-ttu-id="76011-2926">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2926">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="76011-2927">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="76011-2927">Az.Monitor</span></span>
  * <span data-ttu-id="76011-2928">GenV2(비 클래식) 메트릭 기반 경고 규칙에 대한 새 cmdlet</span><span class="sxs-lookup"><span data-stu-id="76011-2928">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="76011-2929">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="76011-2929">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="76011-2930">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="76011-2930">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="76011-2931">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="76011-2931">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="76011-2932">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="76011-2932">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="76011-2933">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="76011-2933">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="76011-2934">모니터 SDK가 버전 0.22.0-preview로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2934">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="76011-2935">Az.Network</span><span class="sxs-lookup"><span data-stu-id="76011-2935">Az.Network</span></span>
* <span data-ttu-id="76011-2936">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2936">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="76011-2937">와일드 카드에 대한 설명서 수정</span><span class="sxs-lookup"><span data-stu-id="76011-2937">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="76011-2938">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="76011-2938">Az.NotificationHubs</span></span>
* <span data-ttu-id="76011-2939">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2939">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="76011-2940">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="76011-2940">Az.OperationalInsights</span></span>
* <span data-ttu-id="76011-2941">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2941">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="76011-2942">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="76011-2942">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="76011-2943">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2943">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="76011-2944">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="76011-2944">Az.RecoveryServices</span></span>
* <span data-ttu-id="76011-2945">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2945">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="76011-2946">Azure VM의 SQL용 테이블 형식이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2946">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="76011-2947">AzureFileShare에서 위치를 가져오는 대체 메서드가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2947">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="76011-2948">시간대에 따라 SchedulePolicy 개체의 ScheduleRunDays가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2948">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="76011-2949">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="76011-2949">Az.RedisCache</span></span>
* <span data-ttu-id="76011-2950">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2950">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="76011-2951">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="76011-2951">Az.Resources</span></span>
* <span data-ttu-id="76011-2952">와일드 카드에 대한 설명서 수정</span><span class="sxs-lookup"><span data-stu-id="76011-2952">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="76011-2953">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="76011-2953">Az.Sql</span></span>
* <span data-ttu-id="76011-2954">Monitor SDK의 종속성을 공용 코드로 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2954">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="76011-2955">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2955">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="76011-2956">다중 열 분류 프로세스가 향상되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2956">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="76011-2957">기본적으로 Get-AzSqlServerServiceObjective의 응답으로 SKU 속성(SKU 이름, 제품군, 용량)과 테이블 형식을 포함합니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2957">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="76011-2958">해당 지역에 기존 서버 없이 위치별로 Get-AzSqlServerServiceObjective를 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2958">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="76011-2959">관리형 인스턴스 생성 시 표준 시간대 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2959">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="76011-2960">와일드 카드에 대한 설명서 수정</span><span class="sxs-lookup"><span data-stu-id="76011-2960">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="76011-2961">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="76011-2961">Az.Websites</span></span>
* <span data-ttu-id="76011-2962">실행 시 태그를 제거하지 않도록 Set-AzWebApp 및 Set-AzWebAppSlot를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2962">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="76011-2963">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2963">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="76011-2964">WebSites SDK가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2964">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="76011-2965">PSAppServicePlan에서 AdminSiteName 속성을 제거했습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2965">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="76011-2966">1.7.0 - 2019년 4월</span><span class="sxs-lookup"><span data-stu-id="76011-2966">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="76011-2967">마지막 주 릴리스 이후의 주요 사항</span><span class="sxs-lookup"><span data-stu-id="76011-2967">Highlights since the last major release</span></span>
* <span data-ttu-id="76011-2968">`Az` 모듈 일반 공급</span><span class="sxs-lookup"><span data-stu-id="76011-2968">General availability of `Az` module</span></span>
* <span data-ttu-id="76011-2969">`Az` 모듈에 대한 자세한 내용은 https://aka.ms/azps-announce 를 방문하세요.</span><span class="sxs-lookup"><span data-stu-id="76011-2969">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="76011-2970">Location, ResourceGroup 및 ResourceName 완성자가 추가되었습니다(https://azure.microsoft.com/blog/completers-in-azure-powershell/ ).</span><span class="sxs-lookup"><span data-stu-id="76011-2970">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="76011-2971">와일드카드 지원이 Az.Compute 및 Az.Network에 대한 Get cmdlet에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2971">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="76011-2972">Windows PowerShell 5.1 전용 대화형 사용자 이름/암호 인증이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2972">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="76011-2973">Python 2 Runbook 지원이 Az.Automation에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2973">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="76011-2974">Az.LogicApp: 통합 계정 어셈블리 및 일괄 처리 구성을 위한 새로운 cmdlet입니다.</span><span class="sxs-lookup"><span data-stu-id="76011-2974">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="76011-2975">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="76011-2975">Az.Accounts</span></span>
* <span data-ttu-id="76011-2976">매개 변수 AzureAnalysisServicesEndpointResourceId를 허용하도록 Add-AzEnvironment 및 Set-AzEnvironment 업데이트</span><span class="sxs-lookup"><span data-stu-id="76011-2976">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="76011-2977">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="76011-2977">Az.AnalysisServices</span></span>
* <span data-ttu-id="76011-2978">데이터 평면 cmdlet에서 ServiceClient 사용 및 원본 인증 논리 제거</span><span class="sxs-lookup"><span data-stu-id="76011-2978">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="76011-2979">호환성이 손상되는 변경을 방지하기 위해 Add-AzureASAccount를 Connect-AzAccount의 래퍼로 만듦</span><span class="sxs-lookup"><span data-stu-id="76011-2979">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="76011-2980">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="76011-2980">Az.Automation</span></span>
* <span data-ttu-id="76011-2981">포함에 대한 New-AzAutomationSoftwareUpdateConfiguration cmdlet 버그 수정</span><span class="sxs-lookup"><span data-stu-id="76011-2981">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="76011-2982">이제 매개 변수 IncludedKbNumber 및 IncludedPackageNameMask가 작동함</span><span class="sxs-lookup"><span data-stu-id="76011-2982">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="76011-2983">Azure 자동화 업데이트 관리 동적 그룹에 대한 버그 수정</span><span class="sxs-lookup"><span data-stu-id="76011-2983">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="76011-2984">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="76011-2984">Az.Compute</span></span>
* <span data-ttu-id="76011-2985">New-AzDiskConfig 및 New-AzSnapshotConfig에 HyperVGeneration 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="76011-2985">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="76011-2986">다른 테넌트의 갤러리 이미지를 사용하여 VM을 만들 수 있음</span><span class="sxs-lookup"><span data-stu-id="76011-2986">Allow VM creation with galley image from other tenants.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="76011-2987">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="76011-2987">Az.ContainerInstance</span></span>
* <span data-ttu-id="76011-2988">후행 빈 인수를 추가한 New-AzContainerGroup의 -Command 매개 변수의 문제 수정</span><span class="sxs-lookup"><span data-stu-id="76011-2988">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="76011-2989">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="76011-2989">Az.DataFactory</span></span>
* <span data-ttu-id="76011-2990">ADF .Net SDK 버전을 3.0.2로 업데이트</span><span class="sxs-lookup"><span data-stu-id="76011-2990">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="76011-2991">RepoConfiguration 관련 설정에 대한 추가 매개 변수로 Set-AzDataFactoryV2 cmdlet을 업데이트</span><span class="sxs-lookup"><span data-stu-id="76011-2991">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="76011-2992">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="76011-2992">Az.Resources</span></span>
* <span data-ttu-id="76011-2993">'-ResourceId' 또는 '-ResourceGroupName', '-Name' 및 '-ResourceType' 매개 변수를 제공할 때 'Get-AzResource'에 대한 공급자 처리 개선</span><span class="sxs-lookup"><span data-stu-id="76011-2993">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="76011-2994">'Test-AzDeployment' 및 'Test-AzResourceGroupDeployment'에 대한 오류 처리 개선</span><span class="sxs-lookup"><span data-stu-id="76011-2994">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="76011-2995">배포 유효성 검사 외부에서 발생한 오류를 처리하고 그 대신 명령의 출력에 포함</span><span class="sxs-lookup"><span data-stu-id="76011-2995">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="76011-2996">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/6856 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="76011-2996">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="76011-2997">배포 cmdlet 세트에 스크립트 및 작업 시나리오에서 프롬프트를 건너뛰는 '-IgnoreDynamicParameters' 스위치 추가</span><span class="sxs-lookup"><span data-stu-id="76011-2997">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="76011-2998">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/6856 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="76011-2998">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="76011-2999">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="76011-2999">Az.Sql</span></span>
* <span data-ttu-id="76011-3000">데이터베이스 데이터 분류 지원</span><span class="sxs-lookup"><span data-stu-id="76011-3000">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="76011-3001">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="76011-3001">Az.Storage</span></span>
* <span data-ttu-id="76011-3002">매개 변수 -UseConnectedAccount를 사용하여 스토리지 컨텍스트를 만들 때 자세한 오류 보고(단, 로그인 Azure 계정 없이)</span><span class="sxs-lookup"><span data-stu-id="76011-3002">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="76011-3003">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="76011-3003">New-AzStorageContext</span></span>
* <span data-ttu-id="76011-3004">관리 평면 API를 사용하여 지정한 스토리지 계정의 BLOB 서비스 속성 관리 지원</span><span class="sxs-lookup"><span data-stu-id="76011-3004">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="76011-3005">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="76011-3005">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="76011-3006">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="76011-3006">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="76011-3007">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="76011-3007">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="76011-3008">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="76011-3008">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="76011-3009">BLOB 및 파일 업로드/다운로드 cmdlet에 대한 -AsJob 지원</span><span class="sxs-lookup"><span data-stu-id="76011-3009">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="76011-3010">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="76011-3010">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="76011-3011">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="76011-3011">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="76011-3012">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="76011-3012">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="76011-3013">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="76011-3013">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="76011-3014">1.6.0 - 2019년 3월</span><span class="sxs-lookup"><span data-stu-id="76011-3014">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="76011-3015">마지막 주 릴리스 이후의 주요 사항</span><span class="sxs-lookup"><span data-stu-id="76011-3015">Highlights since the last major release</span></span>
* <span data-ttu-id="76011-3016">`Az` 모듈 일반 공급</span><span class="sxs-lookup"><span data-stu-id="76011-3016">General availability of `Az` module</span></span>
* <span data-ttu-id="76011-3017">`Az` 모듈에 대한 자세한 내용은 https://aka.ms/azps-announce 를 방문하세요.</span><span class="sxs-lookup"><span data-stu-id="76011-3017">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="76011-3018">Location, ResourceGroup 및 ResourceName 완성자가 추가되었습니다(https://azure.microsoft.com/blog/completers-in-azure-powershell/ ).</span><span class="sxs-lookup"><span data-stu-id="76011-3018">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="76011-3019">와일드카드 지원이 Az.Compute 및 Az.Network에 대한 Get cmdlet에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-3019">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="76011-3020">Windows PowerShell 5.1 전용 대화형 사용자 이름/암호 인증이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-3020">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="76011-3021">Python 2 Runbook 지원이 Az.Automation에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-3021">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="76011-3022">Az.LogicApp: 통합 계정 어셈블리 및 일괄 처리 구성을 위한 새로운 cmdlet입니다.</span><span class="sxs-lookup"><span data-stu-id="76011-3022">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="76011-3023">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="76011-3023">Az.Automation</span></span>
* <span data-ttu-id="76011-3024">Azure 자동화 업데이트 관리에서 변경된 지원 기능은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-3024">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="76011-3025">동적 그룹화</span><span class="sxs-lookup"><span data-stu-id="76011-3025">Dynamic grouping</span></span>
    * <span data-ttu-id="76011-3026">사전 스크립트</span><span class="sxs-lookup"><span data-stu-id="76011-3026">Pre-Post script</span></span>
    * <span data-ttu-id="76011-3027">다시 부팅 설정</span><span class="sxs-lookup"><span data-stu-id="76011-3027">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="76011-3028">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="76011-3028">Az.Compute</span></span>
* <span data-ttu-id="76011-3029">Get-AzVmBootDiagnosticsData의 경로 확인 문제가 해결되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-3029">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="76011-3030">Compute 클라이언트 라이브러리가 25.0.0으로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-3030">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="76011-3031">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="76011-3031">Az.KeyVault</span></span>
* <span data-ttu-id="76011-3032">와일드카드 지원이 KeyVault cmdlet에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-3032">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="76011-3033">Az.Network</span><span class="sxs-lookup"><span data-stu-id="76011-3033">Az.Network</span></span>
* <span data-ttu-id="76011-3034">Azure Firewall에 대한 위협 인텔리전스 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-3034">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="76011-3035">Application Gateway 방화벽 정책의 최상위 수준 리소스 및 사용자 지정 규칙이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-3035">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="76011-3036">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="76011-3036">Az.RecoveryServices</span></span>
* <span data-ttu-id="76011-3037">인스턴트 RP를 지원하기 위해 SnapshotRetentionInDays가 Azure VM 정책에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-3037">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="76011-3038">컨테이너 등록을 취소하는 파이프 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-3038">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="76011-3039">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="76011-3039">Az.Resources</span></span>
* <span data-ttu-id="76011-3040">Get-AzResource 및 Get-AzResourceGroup에 대한 와일드카드 지원을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="76011-3040">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="76011-3041">ARM에 대한 일반 호출을 수행할 때 사용되는 자격 증명을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="76011-3041">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="76011-3042">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="76011-3042">Az.Sql</span></span>
* <span data-ttu-id="76011-3043">위협 탐지의 cmdlet 매개 변수(ExcludeDetectionType)가 DetectionType에서 string[]으로 변경되어 새 DetectionType이 추가되면 이후의 증명이 되고 자동 완성도 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="76011-3043">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="76011-3044">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="76011-3044">Az.Storage</span></span>
* <span data-ttu-id="76011-3045">스토리지 계정에 대한 관리 정책 가져오기/설정/제거를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="76011-3045">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="76011-3046">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="76011-3046">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="76011-3047">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="76011-3047">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="76011-3048">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="76011-3048">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="76011-3049">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="76011-3049">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="76011-3050">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="76011-3050">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="76011-3051">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="76011-3051">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="76011-3052">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="76011-3052">Az.Websites</span></span>
* <span data-ttu-id="76011-3053">'New-AzWebApp -IncludeSourceWebAppSlots'를 사용하여 모든 슬롯의 복제를 중단하는 ARM 템플릿 버그가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-3053">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span>

## <a name="150---march-2019"></a><span data-ttu-id="76011-3054">1.5.0 - 2019년 3월</span><span class="sxs-lookup"><span data-stu-id="76011-3054">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="76011-3055">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="76011-3055">Az.Accounts</span></span>
* <span data-ttu-id="76011-3056">'Register-AzModule' 명령을 추가하여 AutoRest 생성 cmdlet을 지원</span><span class="sxs-lookup"><span data-stu-id="76011-3056">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="76011-3057">Connect-AzAccount 예제 업데이트</span><span class="sxs-lookup"><span data-stu-id="76011-3057">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="76011-3058">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="76011-3058">Az.Automation</span></span>
* <span data-ttu-id="76011-3059">몇몇 Azure Automation cmdlet에서 특정 월별 일정을 검색할 때 발생하는 문제 수정</span><span class="sxs-lookup"><span data-stu-id="76011-3059">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="76011-3060">상위 20개 노드를 반환하도록 Get-AzAutomationDscNode를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="76011-3060">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="76011-3061">이제 모든 노드 반환</span><span class="sxs-lookup"><span data-stu-id="76011-3061">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="76011-3062">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="76011-3062">Az.Cdn</span></span>
* <span data-ttu-id="76011-3063">사용자 지정 도메인 Https 사용/사용 안 함에 대한 새 Powershell cmdlet이 추가되었으며 기존의 것은 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-3063">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="76011-3064">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="76011-3064">Az.Compute</span></span>
* <span data-ttu-id="76011-3065">Get cmdlet에 와일드 카드 지원 추가</span><span class="sxs-lookup"><span data-stu-id="76011-3065">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="76011-3066">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="76011-3066">Az.DataFactory</span></span>
* <span data-ttu-id="76011-3067">ADF.Net SDK 버전이 3.0.1로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-3067">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="76011-3068">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="76011-3068">Az.LogicApp</span></span>
* <span data-ttu-id="76011-3069">첫 결과 페이지 검색 시에만 ListWorkflows 수정</span><span class="sxs-lookup"><span data-stu-id="76011-3069">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="76011-3070">Az.Network</span><span class="sxs-lookup"><span data-stu-id="76011-3070">Az.Network</span></span>
* <span data-ttu-id="76011-3071">Network cmdlet에 와일드 카드 지원 추가</span><span class="sxs-lookup"><span data-stu-id="76011-3071">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="76011-3072">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="76011-3072">Az.RecoveryServices</span></span>
* <span data-ttu-id="76011-3073">Azure VM 지원에 SQL 서버가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-3073">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="76011-3074">SDK 업데이트</span><span class="sxs-lookup"><span data-stu-id="76011-3074">SDK Update</span></span>
* <span data-ttu-id="76011-3075">VMappContainer 체크 인 Get-ProtectableItem 제거</span><span class="sxs-lookup"><span data-stu-id="76011-3075">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="76011-3076">Get ProtectableItem의 매개 변수로 Name과 ServerName이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-3076">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="76011-3077">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="76011-3077">Az.Resources</span></span>
* <span data-ttu-id="76011-3078">`-TemplateObject` 매개 변수를 추가하여 cmdlet을 배포</span><span class="sxs-lookup"><span data-stu-id="76011-3078">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="76011-3079">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/2933 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="76011-3079">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="76011-3080">`Get-AzResource`의 결과를 `Set-AzResource`(으)로 파이프할 때 발생하는 문제 수정</span><span class="sxs-lookup"><span data-stu-id="76011-3080">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="76011-3081">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/8240 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="76011-3081">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="76011-3082">실행 시 JSON 데이터 형식 문제 해결 `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="76011-3082">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="76011-3083">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/7930 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="76011-3083">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="76011-3084">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="76011-3084">Az.Sql</span></span>
* <span data-ttu-id="76011-3085">AuditingEndpointsCommunicator를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="76011-3085">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="76011-3086">새 진단 설정을 생성할 때 에지 사례의 동작을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="76011-3086">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="76011-3087">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="76011-3087">Az.Storage</span></span>
* <span data-ttu-id="76011-3088">스토리지 계정      - New-AzStorageAccount를 생성할 때 종류 BlockBlobStorage를 지원</span><span class="sxs-lookup"><span data-stu-id="76011-3088">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="76011-3089">1.4.0 - 2019년 2월</span><span class="sxs-lookup"><span data-stu-id="76011-3089">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="76011-3090">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="76011-3090">Az.AnalysisServices</span></span>
* <span data-ttu-id="76011-3091">사용되지 않는 AddAzureASAccount cmdlet</span><span class="sxs-lookup"><span data-stu-id="76011-3091">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="76011-3092">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="76011-3092">Az.Automation</span></span>
* <span data-ttu-id="76011-3093">Import-AzAutomationDscNodeConfiguration 도움말 업데이트</span><span class="sxs-lookup"><span data-stu-id="76011-3093">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="76011-3094">Import-AzAutomationDscConfiguration cmdlet 구성 이름 유효성 검사 추가</span><span class="sxs-lookup"><span data-stu-id="76011-3094">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="76011-3095">Import-AzAutomationDscConfiguration cmdlet 오류 처리 개선</span><span class="sxs-lookup"><span data-stu-id="76011-3095">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="76011-3096">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="76011-3096">Az.CognitiveServices</span></span>
* <span data-ttu-id="76011-3097">리소스의 하위 도메인을 지정하는 데 사용되는 New-AzCognitiveServicesAccount에 대한 새 선택적 매개 변수로 CustomSubdomainName이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-3097">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="76011-3098">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="76011-3098">Az.Compute</span></span>
* <span data-ttu-id="76011-3099">ID 매개 변수 집합 문제 해결</span><span class="sxs-lookup"><span data-stu-id="76011-3099">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="76011-3100">Name 매개 변수를 제공하지 않으면 Get-AzVMExtension이 설치된 모든 확장을 열거하도록 업데이트</span><span class="sxs-lookup"><span data-stu-id="76011-3100">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="76011-3101">Update-AzImage cmdlet에 태그 및 ResourceId 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="76011-3101">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="76011-3102">인스턴스 ID가 없는 Get-AzVmssVM과 InstanceView를 사용하면 인스턴스 보기가 있는 VMSS VM을 나열할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-3102">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="76011-3103">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="76011-3103">Az.DataLakeStore</span></span>
* <span data-ttu-id="76011-3104">ADL 삭제된 항목 열거 및 복원에 대한 cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="76011-3104">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="76011-3105">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="76011-3105">Az.EventHub</span></span>
* <span data-ttu-id="76011-3106">Eventhub의 CaptureDescription 클래스에서 빈 보관을 건너뛰는 새 부울 속성 SkipEmptyArchives가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-3106">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="76011-3107">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="76011-3107">Az.KeyVault</span></span>
* <span data-ttu-id="76011-3108">Set-AzKeyVaultSecret 태그 지정 수정</span><span class="sxs-lookup"><span data-stu-id="76011-3108">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="76011-3109">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="76011-3109">Az.LogicApp</span></span>
* <span data-ttu-id="76011-3110">통합 계정에 대한 기본 sku 추가</span><span class="sxs-lookup"><span data-stu-id="76011-3110">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="76011-3111">XSLT 2.0, XSLT 3.0, Liquid 맵 형식 추가</span><span class="sxs-lookup"><span data-stu-id="76011-3111">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="76011-3112">통합 계정 어셈블리에 대한 새 cmdlet</span><span class="sxs-lookup"><span data-stu-id="76011-3112">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="76011-3113">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="76011-3113">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="76011-3114">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="76011-3114">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="76011-3115">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="76011-3115">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="76011-3116">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="76011-3116">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="76011-3117">통합 계정 일괄 처리 구성에 대한 새 cmdlet</span><span class="sxs-lookup"><span data-stu-id="76011-3117">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="76011-3118">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="76011-3118">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="76011-3119">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="76011-3119">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="76011-3120">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="76011-3120">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="76011-3121">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="76011-3121">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="76011-3122">논리 앱 SDK를 버전 4.1.0으로 업데이트</span><span class="sxs-lookup"><span data-stu-id="76011-3122">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="76011-3123">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="76011-3123">Az.Monitor</span></span>
* <span data-ttu-id="76011-3124">Get-AzMetric에 대한 도움말 업데이트</span><span class="sxs-lookup"><span data-stu-id="76011-3124">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="76011-3125">Az.Network</span><span class="sxs-lookup"><span data-stu-id="76011-3125">Az.Network</span></span>
* <span data-ttu-id="76011-3126">Add-AzApplicationGatewayCustomError에 대한 도움말 예제 업데이트</span><span class="sxs-lookup"><span data-stu-id="76011-3126">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="76011-3127">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="76011-3127">Az.OperationalInsights</span></span>
* <span data-ttu-id="76011-3128">New 및 Get ApplicationInsights 데이터 소스에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="76011-3128">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="76011-3129">지정된 작업 영역에 대한 특정 또는 전체 ApplicationInsights 데이터 원본 가져오기를 지원하기 위한 새로운 'ApplicationInsights' 종류가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-3129">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span>
    - <span data-ttu-id="76011-3130">지정된 Application-Insights 리소스 매개 변수(구독 ID, resourceGroupName 및 이름)별로 데이터 원본을 만들기 위한 New-AzOperationalInsightsApplicationInsightsDataSource cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-3130">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span>

#### <a name="azresources"></a><span data-ttu-id="76011-3131">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="76011-3131">Az.Resources</span></span>
* <span data-ttu-id="76011-3132">문제 https://github.com/Azure/azure-powershell/issues/8166 수정</span><span class="sxs-lookup"><span data-stu-id="76011-3132">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="76011-3133">문제 https://github.com/Azure/azure-powershell/issues/8235 수정</span><span class="sxs-lookup"><span data-stu-id="76011-3133">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="76011-3134">문제 https://github.com/Azure/azure-powershell/issues/6219 수정</span><span class="sxs-lookup"><span data-stu-id="76011-3134">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="76011-3135">KeyCredentials 반복 만들기를 방지하기 위해 버그 수정</span><span class="sxs-lookup"><span data-stu-id="76011-3135">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="76011-3136">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="76011-3136">Az.Sql</span></span>
* <span data-ttu-id="76011-3137">SQL DB 하이퍼스케일에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="76011-3137">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="76011-3138">복원 요청에서 불필요한 속성을 설정하여 복원이 실패할 수 있는 버그 수정</span><span class="sxs-lookup"><span data-stu-id="76011-3138">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="76011-3139">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="76011-3139">Az.Websites</span></span>
* <span data-ttu-id="76011-3140">Get-AzWebAppSlotMetrics 내 올바른 예제</span><span class="sxs-lookup"><span data-stu-id="76011-3140">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="76011-3141">1.3.0 - 2019년 2월</span><span class="sxs-lookup"><span data-stu-id="76011-3141">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="76011-3142">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="76011-3142">Az.Accounts</span></span>
* <span data-ttu-id="76011-3143">ClientRuntime 최신 버전 업데이트</span><span class="sxs-lookup"><span data-stu-id="76011-3143">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="76011-3144">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="76011-3144">Az.AnalysisServices</span></span>
<span data-ttu-id="76011-3145">Az.AnalysisServices 모듈의 전반적인 가용성.</span><span class="sxs-lookup"><span data-stu-id="76011-3145">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="76011-3146">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="76011-3146">Az.Compute</span></span>
* <span data-ttu-id="76011-3147">AEM 확장: UltraSSD 및 P60, P70, P80 디스크에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="76011-3147">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="76011-3148">Set-AzVMBootDiagnostics에 대한 도움말 업데이트</span><span class="sxs-lookup"><span data-stu-id="76011-3148">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="76011-3149">Update-AzImage에 대한 도움말 및 예제 업데이트</span><span class="sxs-lookup"><span data-stu-id="76011-3149">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="76011-3150">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="76011-3150">Az.RecoveryServices</span></span>
<span data-ttu-id="76011-3151">Az.RecoveryServices 모듈의 전반적인 가용성.</span><span class="sxs-lookup"><span data-stu-id="76011-3151">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="76011-3152">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="76011-3152">Az.Resources</span></span>
* <span data-ttu-id="76011-3153">리소스 그룹 관련 태그 수정</span><span class="sxs-lookup"><span data-stu-id="76011-3153">Fix tagging for resource groups</span></span>
    - <span data-ttu-id="76011-3154">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/8166 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="76011-3154">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="76011-3155">`Get-AzureRmRoleAssignment`이(가) -ErrorAction을 준수하지 않는 문제 수정</span><span class="sxs-lookup"><span data-stu-id="76011-3155">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span>
    - <span data-ttu-id="76011-3156">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/8235 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="76011-3156">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="76011-3157">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="76011-3157">Az.Sql</span></span>
* <span data-ttu-id="76011-3158">AzSqlDatabaseBackupShortTermRetentionPolicy 가져오기/설정하기 추가</span><span class="sxs-lookup"><span data-stu-id="76011-3158">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="76011-3159">SQL cmdlet을 실행할 경우 Azure 계정에 로그인되어 있지 않은 것이 nullref 예외를 초래하는 문제 수정</span><span class="sxs-lookup"><span data-stu-id="76011-3159">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="76011-3160">Get-AzSqlCapability의 nullref 예외 수정</span><span class="sxs-lookup"><span data-stu-id="76011-3160">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="76011-3161">1.2.1 - 2019년 1월</span><span class="sxs-lookup"><span data-stu-id="76011-3161">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="76011-3162">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="76011-3162">Az.Accounts</span></span>
* <span data-ttu-id="76011-3163">올바른 인증 버전을 사용하여 릴리스</span><span class="sxs-lookup"><span data-stu-id="76011-3163">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="76011-3164">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="76011-3164">Az.AnalysisServices</span></span>
* <span data-ttu-id="76011-3165">업데이트된 인증 종속성을 사용하여 릴리스</span><span class="sxs-lookup"><span data-stu-id="76011-3165">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="76011-3166">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="76011-3166">Az.RecoveryServices</span></span>
* <span data-ttu-id="76011-3167">업데이트된 인증 종속성을 사용하여 릴리스</span><span class="sxs-lookup"><span data-stu-id="76011-3167">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="76011-3168">1.2.0 - 2019년 1월</span><span class="sxs-lookup"><span data-stu-id="76011-3168">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="76011-3169">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="76011-3169">Az.Accounts</span></span>
* <span data-ttu-id="76011-3170">Windows PowerShell 5.1 전용 대화형 사용자 이름/암호 인증 추가</span><span class="sxs-lookup"><span data-stu-id="76011-3170">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="76011-3171">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="76011-3171">Update incorrect online help URLs</span></span>
* <span data-ttu-id="76011-3172">Uninstall-AzureRm 관련 PS Core에 경고 메시지 추가</span><span class="sxs-lookup"><span data-stu-id="76011-3172">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="76011-3173">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="76011-3173">Az.Aks</span></span>
* <span data-ttu-id="76011-3174">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="76011-3174">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="76011-3175">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="76011-3175">Az.Automation</span></span>
* <span data-ttu-id="76011-3176">Python 2 Runbook에 대한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-3176">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="76011-3177">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="76011-3177">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="76011-3178">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="76011-3178">Az.Cdn</span></span>
* <span data-ttu-id="76011-3179">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="76011-3179">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="76011-3180">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="76011-3180">Az.Compute</span></span>
* <span data-ttu-id="76011-3181">Invoke-AzVMReimage cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="76011-3181">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="76011-3182">Set-AzVmss에 TempDisk 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="76011-3182">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="76011-3183">New-AzVM 경고 메시지 수정</span><span class="sxs-lookup"><span data-stu-id="76011-3183">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="76011-3184">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="76011-3184">Az.ContainerRegistry</span></span>
* <span data-ttu-id="76011-3185">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="76011-3185">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="76011-3186">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="76011-3186">Az.DataFactory</span></span>
* <span data-ttu-id="76011-3187">ADF.Net SDK 버전이 3.0.0으로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-3187">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="76011-3188">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="76011-3188">Az.DataLakeStore</span></span>
* <span data-ttu-id="76011-3189">MSI를 사용할 때 ADLS 엔드포인트 문제 수정</span><span class="sxs-lookup"><span data-stu-id="76011-3189">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="76011-3190">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/7462 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="76011-3190">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="76011-3191">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="76011-3191">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="76011-3192">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="76011-3192">Az.IotHub</span></span>
* <span data-ttu-id="76011-3193">Add-IotHubRoutingEndpoint cmdlet에 인코딩 형식을 추가하세요.</span><span class="sxs-lookup"><span data-stu-id="76011-3193">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="76011-3194">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="76011-3194">Az.KeyVault</span></span>
* <span data-ttu-id="76011-3195">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="76011-3195">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="76011-3196">Az.Network</span><span class="sxs-lookup"><span data-stu-id="76011-3196">Az.Network</span></span>
* <span data-ttu-id="76011-3197">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="76011-3197">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="76011-3198">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="76011-3198">Az.Resources</span></span>
* <span data-ttu-id="76011-3199">'New-AzADAppCredential' 및 'New-AzADSpCredential' 참조 설명서의 잘못된 예제 수정</span><span class="sxs-lookup"><span data-stu-id="76011-3199">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="76011-3200">리소스 그룹 배포 cmdlet 실행 전 '-TemplateFile' 매개 변수 경로가 확인되지 않는 문제 수정</span><span class="sxs-lookup"><span data-stu-id="76011-3200">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="76011-3201">Az.Resources: New-AzureRmPolicyDefinition -Mode 기본값에 대한 올바른 설명서</span><span class="sxs-lookup"><span data-stu-id="76011-3201">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="76011-3202">Az.Resources: 문제 https://github.com/Azure/azure-powershell/issues/7522 수정</span><span class="sxs-lookup"><span data-stu-id="76011-3202">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="76011-3203">Az.Resources: 문제 https://github.com/Azure/azure-powershell/issues/5747 수정</span><span class="sxs-lookup"><span data-stu-id="76011-3203">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="76011-3204">'PSResourceGroupDeployment' 개체의 서식 문제 수정</span><span class="sxs-lookup"><span data-stu-id="76011-3204">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="76011-3205">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/2123 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="76011-3205">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="76011-3206">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="76011-3206">Az.ServiceFabric</span></span>
* <span data-ttu-id="76011-3207">인증서가 VMSS 모델에 추가되었는데도 예외가 발생할 경우 롤백합니다. 이는 버그 https://github.com/Azure/service-fabric-issues/issues/932 를 수정하기 위함입니다.</span><span class="sxs-lookup"><span data-stu-id="76011-3207">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="76011-3208">일부 오류 메시지를 수정하세요.</span><span class="sxs-lookup"><span data-stu-id="76011-3208">Fix some error messages.</span></span>
* <span data-ttu-id="76011-3209">Az로의 마이그레이션을 통해서는 작동하지 않는 New-AzServiceFabriCluster를 위해 기본값 ARM 템플릿을 가진 클러스터 만들기를 수정하세요.</span><span class="sxs-lookup"><span data-stu-id="76011-3209">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="76011-3210">확장에서 클러스터 id를 확인하여 클러스터에 해당하는 VMSS에만 추가되도록 클러스터/애플리케이션 인증서 추가를 수정하세요.</span><span class="sxs-lookup"><span data-stu-id="76011-3210">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="76011-3211">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="76011-3211">Az.SignalR</span></span>
* <span data-ttu-id="76011-3212">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="76011-3212">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="76011-3213">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="76011-3213">Az.Sql</span></span>
* <span data-ttu-id="76011-3214">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="76011-3214">Update incorrect online help URLs</span></span>
* <span data-ttu-id="76011-3215">가능한 값을 가진 LicenseType 매개 변수에 대한 매개 변수 설명이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-3215">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="76011-3216">유일하게 업데이트된 속성인데 작동하지 않는 관리되는 인스턴스 ID의 업데이트 수정</span><span class="sxs-lookup"><span data-stu-id="76011-3216">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="76011-3217">관리되는 인스턴스에서의 사용자 지정 데이터 정렬에 대한 지원</span><span class="sxs-lookup"><span data-stu-id="76011-3217">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="76011-3218">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="76011-3218">Az.Storage</span></span>
* <span data-ttu-id="76011-3219">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="76011-3219">Update incorrect online help URLs</span></span>
* <span data-ttu-id="76011-3220">Premium Storage 계정이 클래식 로깅/메트릭을 지원하지 않기 때문에, Premium Storage 계정의 클래식 로깅/메트릭을 가져올/설정할 때 상세한 오류 메시지를 제공해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="76011-3220">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="76011-3221">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="76011-3221">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="76011-3222">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="76011-3222">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="76011-3223">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="76011-3223">Az.TrafficManager</span></span>
* <span data-ttu-id="76011-3224">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="76011-3224">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="76011-3225">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="76011-3225">Az.Websites</span></span>
* <span data-ttu-id="76011-3226">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="76011-3226">Update incorrect online help URLs</span></span>
* <span data-ttu-id="76011-3227">앱이 ASE에 호스팅되면 'New-AzWebAppSSLBinding'을 수정하여 올바른 resourcegroup+location에 인증서를 업로드합니다.</span><span class="sxs-lookup"><span data-stu-id="76011-3227">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="76011-3228">'New-AzWebAppSSLBinding'을 수정하여 SSL 인증서를 앱에 바인딩하는 데 붙는 태그를 덮어쓰지 않도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="76011-3228">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="76011-3229">1.1.0 - 2019년 1월</span><span class="sxs-lookup"><span data-stu-id="76011-3229">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="76011-3230">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="76011-3230">Az.Accounts</span></span>
* <span data-ttu-id="76011-3231">Enable-AzureRmAlias에 'Local' 범위 추가</span><span class="sxs-lookup"><span data-stu-id="76011-3231">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="76011-3232">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="76011-3232">Az.Compute</span></span>
* <span data-ttu-id="76011-3233">이름이 Restart/Start/Stop/Remove/Set-AzVM과 Save-AzVMImage에 설정된 ID 매개 변수에서 선택 사항이 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-3233">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="76011-3234">도움말 파일의 ID에 대한 설명이 업데이트 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-3234">Updated the description of ID in help files</span></span>
* <span data-ttu-id="76011-3235">Az.Accounts 모듈을 사용할 때의 이전 버전과의 호환성 문제를 해결합니다.</span><span class="sxs-lookup"><span data-stu-id="76011-3235">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="76011-3236">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="76011-3236">Az.DataLakeStore</span></span>
* <span data-ttu-id="76011-3237">SDK 수정을 위해 데이터 평면의 SDK 버전을 1.1.14로 업데이트하세요.</span><span class="sxs-lookup"><span data-stu-id="76011-3237">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="76011-3238">getfilestatus 및 liststatus에 대한 음수 acesstime 및 modificationtime 수정, 비동기 취소 토큰 수정</span><span class="sxs-lookup"><span data-stu-id="76011-3238">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="76011-3239">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="76011-3239">Az.EventGrid</span></span>
* <span data-ttu-id="76011-3240">2019-01-01 API 버전을 사용하도록 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-3240">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="76011-3241">2019-01-01 API 버전에서 새 시나리오를 지원하도록 다음 cmdlet을 업데이트</span><span class="sxs-lookup"><span data-stu-id="76011-3241">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="76011-3242">New-AzureRmEventGridSubscription: 지정을 위한 새로운 선택적 매개 변수를 추가</span><span class="sxs-lookup"><span data-stu-id="76011-3242">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="76011-3243">이벤트 Time-to-Live</span><span class="sxs-lookup"><span data-stu-id="76011-3243">Event Time-To-Live,</span></span>
        - <span data-ttu-id="76011-3244">이벤트에 대한 최대 배달 시도</span><span class="sxs-lookup"><span data-stu-id="76011-3244">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="76011-3245">배달 못한 편지의 엔드포인트입니다.</span><span class="sxs-lookup"><span data-stu-id="76011-3245">Dead letter endpoint.</span></span>
    - <span data-ttu-id="76011-3246">Update-AzureRmEventGridSubscription: 지정을 위한 새로운 선택적 매개 변수를 추가</span><span class="sxs-lookup"><span data-stu-id="76011-3246">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="76011-3247">이벤트 Time-to-Live</span><span class="sxs-lookup"><span data-stu-id="76011-3247">Event Time-To-Live,</span></span>
        - <span data-ttu-id="76011-3248">이벤트에 대한 최대 배달 시도</span><span class="sxs-lookup"><span data-stu-id="76011-3248">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="76011-3249">배달 못한 편지의 엔드포인트입니다.</span><span class="sxs-lookup"><span data-stu-id="76011-3249">Dead letter endpoint.</span></span>
* <span data-ttu-id="76011-3250">New-AzureRmEventGridSubscription 및 Update-AzureRmEventGridSubscription cmdlet의 EndpointType 옵션에 새 열거형 값(즉, storageQueue 및 hybridConnection)을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="76011-3250">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="76011-3251">이벤트 구독을 생성 또는 업데이트할 때 사용자가 직접 조치를 취해야 할 경우 경고 메시지를 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="76011-3251">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="76011-3252">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="76011-3252">Az.IotHub</span></span>
* <span data-ttu-id="76011-3253">최신 버전의 Azure IotHub SDK로 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="76011-3253">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="76011-3254">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="76011-3254">Az.LogicApp</span></span>
* <span data-ttu-id="76011-3255">지정된 이름이 없는 모든 Get-AzLogicApp 목록</span><span class="sxs-lookup"><span data-stu-id="76011-3255">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="76011-3256">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="76011-3256">Az.Resources</span></span>
* <span data-ttu-id="76011-3257">'Get-AzResource'에 '-ODataQuery'및 '-ResourceId' 매개 변수를 제공할 때 매개 변수 집합 문제 수정</span><span class="sxs-lookup"><span data-stu-id="76011-3257">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="76011-3258">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/7875 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="76011-3258">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="76011-3259">New/Set-AzPolicyDefinition에서 -Custom 매개 변수 처리 문제 수정</span><span class="sxs-lookup"><span data-stu-id="76011-3259">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="76011-3260">New-AzDeployment 설명서에서 오타 수정</span><span class="sxs-lookup"><span data-stu-id="76011-3260">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="76011-3261">'New-AzADUser'에 '-MailNickname'매개 변수가 필수 항목으로 지정됨</span><span class="sxs-lookup"><span data-stu-id="76011-3261">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="76011-3262">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/8220 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="76011-3262">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="76011-3263">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="76011-3263">Az.SignalR</span></span>
* <span data-ttu-id="76011-3264">Az.Accounts 모듈을 사용할 때의 이전 버전과의 호환성 문제를 해결합니다.</span><span class="sxs-lookup"><span data-stu-id="76011-3264">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="76011-3265">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="76011-3265">Az.Sql</span></span>
* <span data-ttu-id="76011-3266">Storage 관리 클라이언트 종속성을 일반적인 SDK 구현으로 변환했습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-3266">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="76011-3267">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="76011-3267">Az.Storage</span></span>
* <span data-ttu-id="76011-3268">Sas Token, OAuth 또는 Anonymous를 사용하여 스토리지 컨텍스트의 StorageAccountName을 실제 스토리지 계정 이름으로 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="76011-3268">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="76011-3269">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="76011-3269">New-AzStorageContext</span></span>
* <span data-ttu-id="76011-3270">'-FullUri' 매개 변수를 사용하여 Blob 스냅샷 개체의 Sas Token을 생성하고 반환된 Uri를 스냅샷 Uri로 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="76011-3270">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="76011-3271">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="76011-3271">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="76011-3272">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="76011-3272">Az.Websites</span></span>
* <span data-ttu-id="76011-3273">'Get-AzDeletedWebApp'의 날짜 구문 분석 버그를 수정했습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-3273">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="76011-3274">Az.Accounts 모듈을 사용할 때의 이전 버전과의 호환성 문제를 해결합니다.</span><span class="sxs-lookup"><span data-stu-id="76011-3274">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="76011-3275">1.0.0 - 2018년 12월</span><span class="sxs-lookup"><span data-stu-id="76011-3275">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="76011-3276">일반</span><span class="sxs-lookup"><span data-stu-id="76011-3276">General</span></span>

- <span data-ttu-id="76011-3277">Az 모듈 일반 공급</span><span class="sxs-lookup"><span data-stu-id="76011-3277">General Availability of Az Module</span></span>
- <span data-ttu-id="76011-3278">각 모듈에 대 한 온라인 도움말</span><span class="sxs-lookup"><span data-stu-id="76011-3278">Online help for each module</span></span>
- <span data-ttu-id="76011-3279">자세한 내용과 로드맵은 [Az 알림 페이지](https://aka.ms/azps-announce)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="76011-3279">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="76011-3280">AzureRM에서 마이그레이션하는 것에 대한 정보는 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="76011-3280">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="76011-3281">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="76011-3281">Az.Accounts</span></span>
- <span data-ttu-id="76011-3282">Az.Profile에서 변경</span><span class="sxs-lookup"><span data-stu-id="76011-3282">Changed from Az.Profile</span></span>
- <span data-ttu-id="76011-3283">프로필 및 컨텍스트 형식에 대한 표 형식 수정</span><span class="sxs-lookup"><span data-stu-id="76011-3283">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="76011-3284">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="76011-3284">Az.ApiManagement</span></span>
- <span data-ttu-id="76011-3285">#7002에 대한 수정</span><span class="sxs-lookup"><span data-stu-id="76011-3285">Fixes for #7002</span></span>
- <span data-ttu-id="76011-3286">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="76011-3286">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="76011-3287">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="76011-3287">Az.Batch</span></span>
- <span data-ttu-id="76011-3288">`PSComputeNode`의 새로운 `NodeAgentInformation` 속성을 통해 풀의 각 VM에서 실행 중인 Azure Batch 노드 에이전트의 버전을 확인하는 기능이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-3288">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="76011-3289">`PSDataDisk`에 대한 `Caching` 기본 값은 이제 `None` 대신 `ReadWrite`입니다.</span><span class="sxs-lookup"><span data-stu-id="76011-3289">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="76011-3290">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="76011-3290">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="76011-3291">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="76011-3291">Az.Billing</span></span>
- <span data-ttu-id="76011-3292">청구, 소비 및 UsageAggregates cmdlet 결합 cmdlet에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="76011-3292">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="76011-3293">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="76011-3293">Az.CognitivServices</span></span>
- <span data-ttu-id="76011-3294">New-AzureRmCognitiveServicesAccount 작업에서 사용 가능한 SkuName 및 Typem에 대한 완성자 추가</span><span class="sxs-lookup"><span data-stu-id="76011-3294">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="76011-3295">Get-AzCognitiveServicesAccountSkus에서 GetSkusWithAccountParamSetName 매개 변수 집합을 제거</span><span class="sxs-lookup"><span data-stu-id="76011-3295">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="76011-3296">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="76011-3296">Az.ContainerInstance</span></span>
- <span data-ttu-id="76011-3297">ManagedIdentity 지원이 추가됨</span><span class="sxs-lookup"><span data-stu-id="76011-3297">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="76011-3298">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="76011-3298">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="76011-3299">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="76011-3299">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="76011-3300">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="76011-3300">Az.DataLakeStore</span></span>
- <span data-ttu-id="76011-3301">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="76011-3301">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="76011-3302">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="76011-3302">Az.Monitor</span></span>
- <span data-ttu-id="76011-3303">Az.Monitor 이름 변경 및 기타 사소한 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="76011-3303">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="76011-3304">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="76011-3304">Az.KeyVault</span></span>
- <span data-ttu-id="76011-3305">출력 형식에서 사용되지 않는 'PurgeDisabled' 속성 제거</span><span class="sxs-lookup"><span data-stu-id="76011-3305">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="76011-3306">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="76011-3306">Az.MachineLearning</span></span>
- <span data-ttu-id="76011-3307">Az.MachineLearningCompute 모듈의 cmdlet 포함</span><span class="sxs-lookup"><span data-stu-id="76011-3307">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="76011-3308">Az.Media</span><span class="sxs-lookup"><span data-stu-id="76011-3308">Az.Media</span></span>
- <span data-ttu-id="76011-3309">New-AzMediaService에서 사용되지 않는 -Tags 별칭이 제거됨</span><span class="sxs-lookup"><span data-stu-id="76011-3309">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="76011-3310">Az.Network</span><span class="sxs-lookup"><span data-stu-id="76011-3310">Az.Network</span></span>
<span data-ttu-id="76011-3311">Application Gateway에서 RewriteRuleSets를 구성하는 것에 대한 지원이 추가됨</span><span class="sxs-lookup"><span data-stu-id="76011-3311">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="76011-3312">추가된 새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-3312">New cmdlets added:</span></span>
        - <span data-ttu-id="76011-3313">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="76011-3313">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="76011-3314">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="76011-3314">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="76011-3315">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="76011-3315">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="76011-3316">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="76011-3316">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="76011-3317">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="76011-3317">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="76011-3318">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="76011-3318">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="76011-3319">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="76011-3319">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="76011-3320">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="76011-3320">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="76011-3321">선택적 매개 변수를 사용하도록 cmdlet이 업데이트됨 -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="76011-3321">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="76011-3322">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="76011-3322">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="76011-3323">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="76011-3323">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="76011-3324">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="76011-3324">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="76011-3325">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="76011-3325">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="76011-3326">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="76011-3326">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="76011-3327">New-AzureRmApplicationGatewayUrlPathMapConfig로 ID를 사용하여 Application Gateway에 KeyVault 지원을 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-3327">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="76011-3328">선택적 매개 변수를 사용하도록 cmdlet이 업데이트됨 -KeyVaultSecretId, -KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="76011-3328">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="76011-3329">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="76011-3329">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="76011-3330">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="76011-3330">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="76011-3331">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="76011-3331">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="76011-3332">New-AzApplicationGateway cmdlet이 선택적 매개 변수를 사용하도록 업데이트됨 -UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="76011-3332">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="76011-3333">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="76011-3333">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="76011-3334">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="76011-3334">Az.OperationalInsights</span></span>
- <span data-ttu-id="76011-3335">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="76011-3335">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="76011-3336">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="76011-3336">Az.Profile</span></span>
- <span data-ttu-id="76011-3337">Az.Accounts에 모듈 이름이 변경됨</span><span class="sxs-lookup"><span data-stu-id="76011-3337">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="76011-3338">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="76011-3338">Az.RecoveryServices</span></span>
- <span data-ttu-id="76011-3339">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="76011-3339">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="76011-3340">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="76011-3340">Az.Resources</span></span>
- <span data-ttu-id="76011-3341">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="76011-3341">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="76011-3342">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="76011-3342">Az.ServiceFabric</span></span>
- <span data-ttu-id="76011-3343">일반 이름과 지문으로 지정 인증서 지원</span><span class="sxs-lookup"><span data-stu-id="76011-3343">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="76011-3344">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="76011-3344">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="76011-3345">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="76011-3345">Az.SIgnalR</span></span>
- <span data-ttu-id="76011-3346">SIgnalR에 대한 PowerShell cmdlet에 대한 일반 공급</span><span class="sxs-lookup"><span data-stu-id="76011-3346">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="76011-3347">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="76011-3347">Az.Sql</span></span>
- <span data-ttu-id="76011-3348">위협 탐지의 cmdlet에 새로운 Data_Exfiltration 및 Unsafe_Action 검색 유형 추가</span><span class="sxs-lookup"><span data-stu-id="76011-3348">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="76011-3349">Sql 감사 cmdlet에 대한 설명서 예제 업데이트</span><span class="sxs-lookup"><span data-stu-id="76011-3349">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="76011-3350">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="76011-3350">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="76011-3351">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="76011-3351">Az.Storage</span></span>
- <span data-ttu-id="76011-3352">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="76011-3352">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="76011-3353">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="76011-3353">Az.Websites</span></span>
- <span data-ttu-id="76011-3354">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="76011-3354">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="76011-3355">0.7.0 - 2018년 12월</span><span class="sxs-lookup"><span data-stu-id="76011-3355">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="76011-3356">일반</span><span class="sxs-lookup"><span data-stu-id="76011-3356">General</span></span>

* <span data-ttu-id="76011-3357">AzureRM에서 Az 전환 예정에 대한 사소한 변경</span><span class="sxs-lookup"><span data-stu-id="76011-3357">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="76011-3358">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="76011-3358">Az.Compute</span></span>

* <span data-ttu-id="76011-3359">`New-AzVm(ss)` cmdlet에 대한 간단한 매개 변수 집합에 UltraSSD 및 갤러리 이미지에 대한 지원을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="76011-3359">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="76011-3360">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="76011-3360">Az.DataLakeStore</span></span>

* <span data-ttu-id="76011-3361">ADLS 계정의 도메인의 후행 슬래시를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="76011-3361">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="76011-3362">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="76011-3362">Az.FrontDoor</span></span>

* <span data-ttu-id="76011-3363">일부 끊어진 링크 수정</span><span class="sxs-lookup"><span data-stu-id="76011-3363">Fixed some broken links</span></span>
    - <span data-ttu-id="76011-3364">New-AzureRmFrontDoor 및 Set-AzureRmFrontDoor 아티클에서 New-AzureRmFrontDoorHealthProbeSettingObject cmdlet 아티클에 대한 링크가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-3364">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="76011-3365">New-AzureRmFrontDoorManagedRuleObject 아티클에서 New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet 아티클에 대한 링크가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-3365">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="76011-3366">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="76011-3366">Az.RecoveryServices</span></span>

* <span data-ttu-id="76011-3367">Azure File Share 복원 작업에 클라이언트 측 유효성 검사가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-3367">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="76011-3368">afs 복원의 경우 storageAccountName 및 storageAccountResourceGroupName을 선택적으로 만들었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-3368">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="76011-3369">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="76011-3369">Az.Resources</span></span>

* <span data-ttu-id="76011-3370"> https://github.com/Azure/azure-powershell/issues/7679 에 대한 수정</span><span class="sxs-lookup"><span data-stu-id="76011-3370">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="76011-3371">기본 관리자를 요청할 때 구독 범위가 제공되는 경우 Get-AzureRmRoleAssignment를 업데이트하여 구독 범위를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="76011-3371">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="76011-3372">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="76011-3372">Az.Sql</span></span>

* <span data-ttu-id="76011-3373">AzureRM에서 Az 전환 예정에 대한 사소한 변경</span><span class="sxs-lookup"><span data-stu-id="76011-3373">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="76011-3374">DotNet 코어에서 Get-AzureRmSqlDatabaseVulnerabilityAssessment를 사용하는 문제 해결</span><span class="sxs-lookup"><span data-stu-id="76011-3374">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="76011-3375">SQL 감사 cmdlet과 관련된 도움말 메시지의 설명서가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-3375">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="76011-3376">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="76011-3376">Az.Storage</span></span>

* <span data-ttu-id="76011-3377">New-AzureRmStorageAccount에 -EnableHierarchicalNamespace 추가</span><span class="sxs-lookup"><span data-stu-id="76011-3377">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="76011-3378">파일 복사 cmdlet이 -DestContext 입력이 없을 때 대상의 원본 컨텍스트를 다시 사용할 수 없는 문제 수정</span><span class="sxs-lookup"><span data-stu-id="76011-3378">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="76011-3379">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="76011-3379">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="76011-3380">고정적인 웹 사이트 구성 지원</span><span class="sxs-lookup"><span data-stu-id="76011-3380">Support Static Website configuration</span></span>
    - <span data-ttu-id="76011-3381">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="76011-3381">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="76011-3382">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="76011-3382">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="76011-3383">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="76011-3383">Az.Websites</span></span>

* <span data-ttu-id="76011-3384">Set-AzureRmWebApp 및 Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="76011-3384">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span>
    - <span data-ttu-id="76011-3385">Windows 및 Linux 컨테이너 응용 프로그램에 탑재할 Azure Storage 경로를 지정하기 위해 새 매개 변수(-AzureStoragePath)가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-3385">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="76011-3386">새 cmdlet New-AzureRmWebAppAzureStoragePath의 출력을 매개 변수로 사용하여 Azure Storage 경로를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="76011-3386">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="76011-3387">0.6.1 - 2018년 11월</span><span class="sxs-lookup"><span data-stu-id="76011-3387">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="76011-3388">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="76011-3388">Az.ApiManagement</span></span>
* <span data-ttu-id="76011-3389">형식 매핑 문제에 대한 종속성 업데이트</span><span class="sxs-lookup"><span data-stu-id="76011-3389">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="76011-3390">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="76011-3390">Az.Automation</span></span>
* <span data-ttu-id="76011-3391">Azure Automation cmdlet 기반 Swagger</span><span class="sxs-lookup"><span data-stu-id="76011-3391">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="76011-3392">업데이트 관리 cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="76011-3392">Added Update Management cmdlets</span></span>
* <span data-ttu-id="76011-3393">소스 제어 cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="76011-3393">Added Source Control cmdlets</span></span>
* <span data-ttu-id="76011-3394">Remove-AzureRmAutomationHybridWorkerGroup cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="76011-3394">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="76011-3395">DSC 노드 등록 명령 수정</span><span class="sxs-lookup"><span data-stu-id="76011-3395">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="76011-3396">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="76011-3396">Az.Compute</span></span>
* <span data-ttu-id="76011-3397">SystemAssigned ID에 대한 ID 문제 수정</span><span class="sxs-lookup"><span data-stu-id="76011-3397">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="76011-3398">형식 매핑 문제에 대한 종속성 업데이트</span><span class="sxs-lookup"><span data-stu-id="76011-3398">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="76011-3399">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="76011-3399">Az.ContainerInstance</span></span>
* <span data-ttu-id="76011-3400">형식 매핑 문제에 대한 종속성 업데이트</span><span class="sxs-lookup"><span data-stu-id="76011-3400">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="76011-3401">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="76011-3401">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="76011-3402">마켓플레이스 cmdlet에 대한 예제 설명 업데이트</span><span class="sxs-lookup"><span data-stu-id="76011-3402">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="76011-3403">Az.Network</span><span class="sxs-lookup"><span data-stu-id="76011-3403">Az.Network</span></span>
* <span data-ttu-id="76011-3404">New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="76011-3404">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="76011-3405">지원되는 AzureFirewall 네트워크 프로토콜에 ICMP 다시 추가</span><span class="sxs-lookup"><span data-stu-id="76011-3405">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="76011-3406">Test-AzureRmNetworkWatcherConnectivity cmdlet을 업데이트하여 대상 ID, 주소 및 포트 유효성 검사를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="76011-3406">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span>
* <span data-ttu-id="76011-3407">VirtualNetwork 맵의 메모리 사용 문제 해결</span><span class="sxs-lookup"><span data-stu-id="76011-3407">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="76011-3408">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="76011-3408">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="76011-3409">보호된 파일 공유에 대한 정책을 수정하는 것에 대해 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="76011-3409">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="76011-3410">정책 표준 시간대를 대문자로 변환했습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-3410">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="76011-3411">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="76011-3411">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="76011-3412">New-AzureRmRecoveryServicesAsrProtectableItem의 예제 정정</span><span class="sxs-lookup"><span data-stu-id="76011-3412">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="76011-3413">형식 매핑 문제에 대한 종속성 업데이트</span><span class="sxs-lookup"><span data-stu-id="76011-3413">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="76011-3414">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="76011-3414">Az.Relay</span></span>
* <span data-ttu-id="76011-3415">선택적 매개 변수 -KeyValue를 New-AzureRmRelayKey cmdlet에 추가하여 사용자가 KeyValue를 제공할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-3415">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="76011-3416">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="76011-3416">Az.Resources</span></span>
* <span data-ttu-id="76011-3417">`New-AzureRmPolicyAssignment` 및 `Set-AzureRmPolicyAssignment`의 자원 ID 관련 매개 변수에 대한 도움말 문서를 업데이트함</span><span class="sxs-lookup"><span data-stu-id="76011-3417">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="76011-3418">-Metadata를 사용하는 New-AzureRmPolicyDefinition에 대한 예제 추가</span><span class="sxs-lookup"><span data-stu-id="76011-3418">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="76011-3419">NetStandard의 태그 키에서 대소문자 보존을 허용하도록 수정: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="76011-3419">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="76011-3420">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="76011-3420">Az.ServiceFabric</span></span>
* <span data-ttu-id="76011-3421">향후 호환성이 손상되는 변경에 대한 사용 중단 메시지 추가</span><span class="sxs-lookup"><span data-stu-id="76011-3421">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="76011-3422">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="76011-3422">Az.Sql</span></span>
* <span data-ttu-id="76011-3423">Azure Sql Database Managed Instance 및 Azure Sql Managed Database에 CRUD 작업을 위한 새 cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="76011-3423">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="76011-3424">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="76011-3424">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="76011-3425">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="76011-3425">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="76011-3426">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="76011-3426">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="76011-3427">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="76011-3427">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="76011-3428">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="76011-3428">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="76011-3429">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="76011-3429">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="76011-3430">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="76011-3430">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="76011-3431">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="76011-3431">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="76011-3432">서버 또는 데이터베이스에서 확장 감사 정책 관리를 활성화했습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-3432">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="76011-3433">새 매개 변수(PredicateExpression)가 감사 로그 필터링을 사용하도록 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-3433">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="76011-3434">Cmdlet이 레거시 클라이언트 대신 SQL 클라이언트를 사용하도록 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-3434">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="76011-3435">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="76011-3435">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="76011-3436">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="76011-3436">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="76011-3437">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="76011-3437">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="76011-3438">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="76011-3438">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="76011-3439">스토리지 계정 이름 매개 변수가 설정된 Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings를 사용할 때의 문제 해결</span><span class="sxs-lookup"><span data-stu-id="76011-3439">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="76011-3440">0.5.0 - 2018년 11월</span><span class="sxs-lookup"><span data-stu-id="76011-3440">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="76011-3441">일반</span><span class="sxs-lookup"><span data-stu-id="76011-3441">General</span></span>
* <span data-ttu-id="76011-3442">많은 핵심 cmdlet에 Resource Completers를 추가하여 대화형으로 cmdlet을 호출할 때 기존 리소스 이름을 탭으로 이동할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-3442">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="76011-3443">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="76011-3443">Az.Profile</span></span>
* <span data-ttu-id="76011-3444">ClientRuntime의 최신 버전을 사용하도록 일반적인 코드를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="76011-3444">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="76011-3445">Connect-AzAccount cmdlet의 매개 변수 TenantId 이름을 Tenant로 바꾸고 TenantId의 별칭을 추가합니다</span><span class="sxs-lookup"><span data-stu-id="76011-3445">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="76011-3446">Connect-AzAccount의 업데이트된 TenantId 설명</span><span class="sxs-lookup"><span data-stu-id="76011-3446">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="76011-3447">테넌트 도메인을 제공할 때 실패한 로그인에 대한 오류 메시지 수정</span><span class="sxs-lookup"><span data-stu-id="76011-3447">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="76011-3448">테넌트에 구독이 없는 계정의 컨텍스트 이름 충돌 문제 수정</span><span class="sxs-lookup"><span data-stu-id="76011-3448">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="76011-3449">MSI를 사용할 때 DataLake 엔드포인트 문제 수정</span><span class="sxs-lookup"><span data-stu-id="76011-3449">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="76011-3450">연결되지 않은 경우 'Disconnect-AzAccount'가 throw하는 문제 수정</span><span class="sxs-lookup"><span data-stu-id="76011-3450">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="76011-3451">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="76011-3451">Az.CognitiveServices</span></span>
* <span data-ttu-id="76011-3452">Get-AzCognitiveServicesAccountSkus 작업을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="76011-3452">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="76011-3453">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="76011-3453">Az.Compute</span></span>
* <span data-ttu-id="76011-3454">Add-AzVmssVMDataDisk 및 Remove-AzVmssVMDataDisk cmdlet를 추가합니다</span><span class="sxs-lookup"><span data-stu-id="76011-3454">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="76011-3455">Get-AzVMImage는 AutomaticOSUpgradeProperties를 표시합니다</span><span class="sxs-lookup"><span data-stu-id="76011-3455">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="76011-3456">수정된 SetAzVMChefExtension -BootstrapOptions 및 -JsonAttribute option 값이 json 형식으로 설정하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-3456">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="76011-3457">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="76011-3457">Az.DataLakeStore</span></span>
* <span data-ttu-id="76011-3458">DataLake 패키지를 1.1.10으로 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="76011-3458">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="76011-3459">기본 동시성을 다중 스레드 작업에 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="76011-3459">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="76011-3460">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="76011-3460">Az.Insights</span></span>
* <span data-ttu-id="76011-3461">해결된 문제 #7267(자동 크기 조정 영역)</span><span class="sxs-lookup"><span data-stu-id="76011-3461">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="76011-3462">열거된 매개 변수를 제대로 설정하지 않은 새 자동 크기 조정 규칙을 만드는 데 문제가 있습니다(이를 항상 기본값으로 설정함).</span><span class="sxs-lookup"><span data-stu-id="76011-3462">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="76011-3463">해결된 문제 # 7513[자세한 정보] Set-AzDiagnosticSetting은 설정을 생성하는 동안 범주를 명시적으로 지정해야 합니다</span><span class="sxs-lookup"><span data-stu-id="76011-3463">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="76011-3464">이제 cmdlet은 생성 중에 사용할 범주를 명시적으로 표시할 필요가 없습니다. 즉, 문서화된대로 작동합니다</span><span class="sxs-lookup"><span data-stu-id="76011-3464">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="76011-3465">Az.Network</span><span class="sxs-lookup"><span data-stu-id="76011-3465">Az.Network</span></span>
* <span data-ttu-id="76011-3466">다음 cmdlet에 대해 PeeringType을 필수 매개 변수로 변경했습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-3466">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="76011-3467">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="76011-3467">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="76011-3468">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="76011-3468">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="76011-3469">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="76011-3469">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="76011-3470">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="76011-3470">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="76011-3471">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="76011-3471">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="76011-3472">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="76011-3472">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="76011-3473">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="76011-3473">Az.PolicyInsights</span></span>
* <span data-ttu-id="76011-3474">추가된 정책 재구성 cmdlet</span><span class="sxs-lookup"><span data-stu-id="76011-3474">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="76011-3475">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="76011-3475">Az.Resources</span></span>
* <span data-ttu-id="76011-3476"> https://github.com/Azure/azure-powershell/issues/7402 에 대한 수정</span><span class="sxs-lookup"><span data-stu-id="76011-3476">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="76011-3477">'Get-AzResource'에 대해 '-ResourceId' 매개 변수를 사용하여 리소스 나열 허용</span><span class="sxs-lookup"><span data-stu-id="76011-3477">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="76011-3478">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="76011-3478">Az.ServiceBus</span></span>
* <span data-ttu-id="76011-3479">마이그레이션 상태를 알 수 있도록 PSServiceBusMigrationConfigurationAttributes에 MigrationState 읽기 전용 속성 추가.</span><span class="sxs-lookup"><span data-stu-id="76011-3479">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="76011-3480">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="76011-3480">Az.ServiceFabric</span></span>
* <span data-ttu-id="76011-3481">Linux Vmss에 인증서 추가 수정.</span><span class="sxs-lookup"><span data-stu-id="76011-3481">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="76011-3482">Add-AzServiceFabricClusterCertificate 수정</span><span class="sxs-lookup"><span data-stu-id="76011-3482">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="76011-3483">새 인증서(Azure/service-fabric-issues#932)에서 올바른 지문을 사용.</span><span class="sxs-lookup"><span data-stu-id="76011-3483">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="76011-3484">올바르게 예외 표시(Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="76011-3484">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="76011-3485">Vmss CreateOrUpdate 작업을 시작하기 전에 'Update-AzServiceFabricDurability'를 수정하여 클러스터 구성 업데이트.</span><span class="sxs-lookup"><span data-stu-id="76011-3485">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="76011-3486">0.4.0 - 2018년 10월</span><span class="sxs-lookup"><span data-stu-id="76011-3486">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="76011-3487">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="76011-3487">Az.Profile</span></span>
* <span data-ttu-id="76011-3488">CloudShell에서 Get-AzSubscription을 사용하여 문제를 해결합니다.</span><span class="sxs-lookup"><span data-stu-id="76011-3488">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="76011-3489">ClientRuntime의 최신 버전을 사용하도록 일반적인 코드를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="76011-3489">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="76011-3490">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="76011-3490">Az.Compute</span></span>
* <span data-ttu-id="76011-3491">'New-AzVm'에 대해 간단한 매개 변수를 사용하는 경우 가속화된 네트워킹을 설정하기 위해 새 크기가 VM 크기의 허용 목록에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-3491">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="76011-3492">모든 cmdlet에 ResourceName 인수 완성자가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-3492">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="76011-3493">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="76011-3493">Az.DataLakeStore</span></span>
* <span data-ttu-id="76011-3494">Virtual Network 규칙에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="76011-3494">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="76011-3495">Get-AzDataLakeStoreVirtualNetworkRule: Azure Data Lake Store 가상 네트워크 규칙을 가져오거나 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="76011-3495">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="76011-3496">Add-AzDataLakeStoreVirtualNetworkRule: 지정된 Data Lake Store 계정에 가상 네트워크 규칙을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="76011-3496">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="76011-3497">Set-AzDataLakeStoreVirtualNetworkRule: 지정된 Data Lake Store 계정에 지정된 가상 네트워크 규칙을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="76011-3497">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="76011-3498">Remove-AzDataLakeStoreVirtualNetworkRule: Azure Data Lake Store 가상 네트워크 규칙을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="76011-3498">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="76011-3499">Az.Network</span><span class="sxs-lookup"><span data-stu-id="76011-3499">Az.Network</span></span>
* <span data-ttu-id="76011-3500">Test-AzNetworkWatcherConnectivity cmdlet을 업데이트하고, 백 엔드에 프로토콜 값을 전달합니다.</span><span class="sxs-lookup"><span data-stu-id="76011-3500">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="76011-3501">모든 cmdlet에 ResourceName 인수 완성자가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-3501">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="76011-3502">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="76011-3502">Az.Resources</span></span>
* <span data-ttu-id="76011-3503">(기본 프로필에 구독이 없고 범위가 지정되지 않은 경우) 시나리오에서 의미 있는 예외를 추가하여 Get-AzRoleDefinition이 인식할 수 없는 예외를 throw하는 문제를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="76011-3503">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="76011-3504">또한 기본 매개 변수 집합을 'RoleDefinitionNameParameterSet'으로 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="76011-3504">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="76011-3505">0.3.0 - 2018년 10월</span><span class="sxs-lookup"><span data-stu-id="76011-3505">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="76011-3506">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="76011-3506">Azure.Storage</span></span>
* <span data-ttu-id="76011-3507">대상에 메타데이터가 있을 때 Blob/파일이 메타 데이터를 복사하지 않는 문제 수정</span><span class="sxs-lookup"><span data-stu-id="76011-3507">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="76011-3508">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="76011-3508">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="76011-3509">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="76011-3509">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="76011-3510">특정 위치의 스토리지 리소스 사용을 지원하고 글로벌 스토리지 리소스 사용 가져오기는 더 이상 사용되지 않는다는 경고 메시지를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="76011-3510">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="76011-3511">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="76011-3511">Get-AzStorageUsage</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="76011-3512">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="76011-3512">Az.CognitiveServices</span></span>
* <span data-ttu-id="76011-3513">기존 계정이 없는 Get-AzCognitiveServicesAccountSkus를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="76011-3513">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="76011-3514">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="76011-3514">Az.Compute</span></span>
* <span data-ttu-id="76011-3515">Get-AzVM -ResourceGroupName <rg>가 필요한 경우 50개가 넘는 결과를 반환하도록 수정</span><span class="sxs-lookup"><span data-stu-id="76011-3515">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="76011-3516">'SimpleParameterSet' 예제가 New-AzVmss cmdlet 도움말에 추가됨</span><span class="sxs-lookup"><span data-stu-id="76011-3516">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="76011-3517">Azure Disk Encryption 진행률 메시지의 오타를 수정</span><span class="sxs-lookup"><span data-stu-id="76011-3517">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="76011-3518">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="76011-3518">Az.DataFactoryV2</span></span>
* <span data-ttu-id="76011-3519">ADF.Net SDK 버전을 2.3.0으로 업데이트</span><span class="sxs-lookup"><span data-stu-id="76011-3519">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="76011-3520">Az.Network</span><span class="sxs-lookup"><span data-stu-id="76011-3520">Az.Network</span></span>
* <span data-ttu-id="76011-3521">NetworkProfile 기능 추가</span><span class="sxs-lookup"><span data-stu-id="76011-3521">Added NetworkProfile functionality.</span></span> <span data-ttu-id="76011-3522">추가된 새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="76011-3522">new cmdlets added</span></span>
    - <span data-ttu-id="76011-3523">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="76011-3523">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="76011-3524">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="76011-3524">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="76011-3525">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="76011-3525">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="76011-3526">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="76011-3526">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="76011-3527">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="76011-3527">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="76011-3528">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="76011-3528">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="76011-3529">서브넷 모델에 서비스 연결 링크 추가</span><span class="sxs-lookup"><span data-stu-id="76011-3529">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="76011-3530">New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="76011-3530">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="76011-3531">Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="76011-3531">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="76011-3532">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="76011-3532">Az.RedisCache</span></span>
* <span data-ttu-id="76011-3533">모든 문자열을 Size 매개 변수로 진행되도록 허용</span><span class="sxs-lookup"><span data-stu-id="76011-3533">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="76011-3534">PSArgumentCompleter 팝업에 P5 추가</span><span class="sxs-lookup"><span data-stu-id="76011-3534">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="76011-3535">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="76011-3535">Az.Resources</span></span>
* <span data-ttu-id="76011-3536">-Mode 매개 변수를 Set-AzPolicyDefinition에 추가</span><span class="sxs-lookup"><span data-stu-id="76011-3536">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="76011-3537">사용자가 포함된 Origin 작업에서 Get-AzProviderOperation commandlet 버그 수정</span><span class="sxs-lookup"><span data-stu-id="76011-3537">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="76011-3538">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="76011-3538">Az.Sql</span></span>
* <span data-ttu-id="76011-3539">일부 백업 cmdlet이 현재 azure 구독을 인식하지 않는 문제 해결</span><span class="sxs-lookup"><span data-stu-id="76011-3539">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="76011-3540">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="76011-3540">Az.Websites</span></span>
* <span data-ttu-id="76011-3541">새 cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - 컨테이너 지속적인 배포 Webhook URL을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="76011-3541">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="76011-3542">새 cmdlet New-AzWebAppContainerPSSession 및 Enter-WebAppContainerPSSession -  windows 컨테이너 앱에 PowerShell 원격 세션을 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="76011-3542">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="76011-3543">0.2.0 - 2018년 9월</span><span class="sxs-lookup"><span data-stu-id="76011-3543">0.2.0 - September 2018</span></span>
 <span data-ttu-id="76011-3544">초기 릴리스</span><span class="sxs-lookup"><span data-stu-id="76011-3544">Initial Release</span></span>