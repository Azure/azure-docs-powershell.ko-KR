---
title: Azure PowerShell 릴리스 정보
description: Azure PowerShell 모듈의 모든 최신 업데이트에 대해 알아봅니다.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/10/2020
ms.openlocfilehash: a9ec7589ab155553da29612096a607d82a078321
ms.sourcegitcommit: 747769a143ddebff39e78c2cc62a182401adddb9
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/23/2020
ms.locfileid: "85268148"
---
# <a name="azure-powershell-release-notes"></a><span data-ttu-id="5d3f2-103">Azure PowerShell 릴리스 정보</span><span class="sxs-lookup"><span data-stu-id="5d3f2-103">Azure PowerShell release notes</span></span>

## <a name="430---june-2020"></a><span data-ttu-id="5d3f2-104">4.3.0 - 2020년 6월</span><span class="sxs-lookup"><span data-stu-id="5d3f2-104">4.3.0 - June 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="5d3f2-105">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="5d3f2-105">Az.Accounts</span></span>
* <span data-ttu-id="5d3f2-106">기본적으로 환경 검색 설정이 지원되며 'Add-AzEnvironment'를 통해 환경을 추가할 수 있음</span><span class="sxs-lookup"><span data-stu-id="5d3f2-106">Supported discovering environment setting by default and adding environment via 'Add-AzEnvironment'</span></span>
* <span data-ttu-id="5d3f2-107">미리 로드된 어셈블리 업데이트 [#12024], [#11976]</span><span class="sxs-lookup"><span data-stu-id="5d3f2-107">Update preloaded assemblies [#12024], [#11976]</span></span>
* <span data-ttu-id="5d3f2-108">Azure.Core 어셈블리 업데이트</span><span class="sxs-lookup"><span data-stu-id="5d3f2-108">Updated Azure.Core assembly</span></span>
* <span data-ttu-id="5d3f2-109">다중 스레드 실행에서 'Connect-AzAccount'가 실패할 수 있는 문제 해결 [#11201]</span><span class="sxs-lookup"><span data-stu-id="5d3f2-109">Fixed an issue that may cause 'Connect-AzAccount' to fail in multi-threaded execution [#11201]</span></span>

#### <a name="azaks"></a><span data-ttu-id="5d3f2-110">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="5d3f2-110">Az.Aks</span></span>
* <span data-ttu-id="5d3f2-111">이전에 사용하던 [AccessProfile API](https://docs.microsoft.com/rest/api/aks/managedclusters/getaccessprofile)를 [ListClusterAdmin](https://docs.microsoft.com/rest/api/aks/managedclusters/listclusteradmincredentials) 및 [ListClusterUser](https://docs.microsoft.com/rest/api/aks/managedclusters/listclusterusercredentials) API 호출로 대체</span><span class="sxs-lookup"><span data-stu-id="5d3f2-111">Replaced usage of old [AccessProfile API](https://docs.microsoft.com/rest/api/aks/managedclusters/getaccessprofile) with calls to [ListClusterAdmin](https://docs.microsoft.com/rest/api/aks/managedclusters/listclusteradmincredentials) and [ListClusterUser](https://docs.microsoft.com/rest/api/aks/managedclusters/listclusterusercredentials) APIs</span></span>

#### <a name="azbatch"></a><span data-ttu-id="5d3f2-112">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="5d3f2-112">Az.Batch</span></span>
* <span data-ttu-id="5d3f2-113">'Microsoft.Azure.Management.Batch' SDK 버전 11.0.0을 사용하도록 Az.Batch 업데이트</span><span class="sxs-lookup"><span data-stu-id="5d3f2-113">Updated Az.Batch to use 'Microsoft.Azure.Management.Batch' SDK version to 11.0.0</span></span>
* <span data-ttu-id="5d3f2-114">'New-AzBatchAccount' cmdlet에서 BatchAccount ID를 설정하는 기능 추가</span><span class="sxs-lookup"><span data-stu-id="5d3f2-114">Added the ability to set the BatchAccount Identity in the 'New-AzBatchAccount' cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="5d3f2-115">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="5d3f2-115">Az.CognitiveServices</span></span>
* <span data-ttu-id="5d3f2-116">계정 기능 표시 지원</span><span class="sxs-lookup"><span data-stu-id="5d3f2-116">Supported displaying account capabilities.</span></span>
* <span data-ttu-id="5d3f2-117">PublicNetworkAccess 수정 지원</span><span class="sxs-lookup"><span data-stu-id="5d3f2-117">Supported modifying PublicNetworkAccess.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="5d3f2-118">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="5d3f2-118">Az.Compute</span></span>
* <span data-ttu-id="5d3f2-119">Set-AzVM 및 Set-AzVmssVM cmdlet에 SimulateEviction 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="5d3f2-119">Added SimulateEviction parameter to Set-AzVM and Set-AzVmssVM cmdlets.</span></span>
* <span data-ttu-id="5d3f2-120">AzGalleryImageVersion cmdlet에 대한 StorageAccountType 매개 변수의 인수 완성자에 'Premium_LRS' 추가</span><span class="sxs-lookup"><span data-stu-id="5d3f2-120">Added 'Premium_LRS' to the argument completer of StorageAccountType parameter for New-AzGalleryImageVersion cmdlet.</span></span>
* <span data-ttu-id="5d3f2-121">VMCustomScriptExtension에 Substatuses 추가 [#11297]</span><span class="sxs-lookup"><span data-stu-id="5d3f2-121">Added Substatuses to VMCustomScriptExtension [#11297]</span></span>
* <span data-ttu-id="5d3f2-122">New-AzVM 및 New-AzVMConfig cmdlet에 대한 EvictionPolicy 매개 변수의 인수 완성자에 'Delete' 추가</span><span class="sxs-lookup"><span data-stu-id="5d3f2-122">Added 'Delete' to the argument completer of EvictionPolicy parameter for New-AzVM and New-AzVMConfig cmdlets.</span></span>
* <span data-ttu-id="5d3f2-123">새 SAP용 VM 확장의 이름 수정</span><span class="sxs-lookup"><span data-stu-id="5d3f2-123">Fixed name of new VM Extension for SAP</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="5d3f2-124">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="5d3f2-124">Az.DataFactory</span></span>
* <span data-ttu-id="5d3f2-125">ADF .Net SDK 버전을 4.9.0으로 업데이트</span><span class="sxs-lookup"><span data-stu-id="5d3f2-125">Updated ADF .Net SDK version to 4.9.0</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="5d3f2-126">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="5d3f2-126">Az.EventHub</span></span>
* <span data-ttu-id="5d3f2-127">'New-AzEventHubNamespace' 및 'Set-AzEventHubNamespace' cmdlet에 관리 ID 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="5d3f2-127">Added Managed Identity parameters to 'New-AzEventHubNamespace' and 'Set-AzEventHubNamespace' cmdlets</span></span>

#### <a name="azfunctions"></a><span data-ttu-id="5d3f2-128">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="5d3f2-128">Az.Functions</span></span>
* <span data-ttu-id="5d3f2-129">PowerShell 7.0 및 Java 11 함수 앱을 만드는 지원 추가</span><span class="sxs-lookup"><span data-stu-id="5d3f2-129">Added support to create PowerShell 7.0 and Java 11 function apps</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="5d3f2-130">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="5d3f2-130">Az.HDInsight</span></span>
* <span data-ttu-id="5d3f2-131">호스트를 나열하고 HDInsight 클러스터의 특정 호스트를 다시 시작하는 기능 지원</span><span class="sxs-lookup"><span data-stu-id="5d3f2-131">Supported listing hosts and restart specific hosts of the HDInsight cluster.</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="5d3f2-132">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="5d3f2-132">Az.HealthcareApis</span></span>
* <span data-ttu-id="5d3f2-133">SDK 버전을 1.1.0으로 업데이트</span><span class="sxs-lookup"><span data-stu-id="5d3f2-133">Updated the SDK version to 1.1.0</span></span>
* <span data-ttu-id="5d3f2-134">설정 및 관리 ID 내보내기에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="5d3f2-134">Added support for Export settings and Managed Identity</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="5d3f2-135">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="5d3f2-135">Az.Monitor</span></span>
* <span data-ttu-id="5d3f2-136">'Set-AzActivityLogAlert'에 대한 입력 개체 매개 변수 수정</span><span class="sxs-lookup"><span data-stu-id="5d3f2-136">Fixed input object parameter for 'Set-AzActivityLogAlert'</span></span>
* <span data-ttu-id="5d3f2-137">'Set-AzActionGroup'에 대한 'InputObject' 매개 변수 수정 [#10868]</span><span class="sxs-lookup"><span data-stu-id="5d3f2-137">Fixed 'InputObject' parameter for 'Set-AzActionGroup' [#10868]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="5d3f2-138">Az.Network</span><span class="sxs-lookup"><span data-stu-id="5d3f2-138">Az.Network</span></span>
* <span data-ttu-id="5d3f2-139">'Remove-AzExpressRouteCircuitConnectionConfig'에 AddressPrefixType 매개 변수 지원 추가</span><span class="sxs-lookup"><span data-stu-id="5d3f2-139">Added support for AddressPrefixType parameter to 'Remove-AzExpressRouteCircuitConnectionConfig'</span></span>
* <span data-ttu-id="5d3f2-140">Azure FirewallPolicy에 대한 새 cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="5d3f2-140">Added new cmdlets for Azure FirewallPolicy</span></span>
    - <span data-ttu-id="5d3f2-141">'New-AzFirewallPolicyDnsSetting'</span><span class="sxs-lookup"><span data-stu-id="5d3f2-141">'New-AzFirewallPolicyDnsSetting'</span></span>
    - <span data-ttu-id="5d3f2-142">방화벽 정책에 대한 네트워크 규칙에서 대상 FQDN 지원</span><span class="sxs-lookup"><span data-stu-id="5d3f2-142">Support for Destination FQDN in Network Rules for Firewall Policy</span></span>
* <span data-ttu-id="5d3f2-143">백 엔드 주소 풀 작업에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="5d3f2-143">Added support for backend address pool operations</span></span>
    - <span data-ttu-id="5d3f2-144">'New-AzLoadBalancerBackendAddressConfig'</span><span class="sxs-lookup"><span data-stu-id="5d3f2-144">'New-AzLoadBalancerBackendAddressConfig'</span></span>
    - <span data-ttu-id="5d3f2-145">'New-AzLoadBalancerBackendAddressPool'</span><span class="sxs-lookup"><span data-stu-id="5d3f2-145">'New-AzLoadBalancerBackendAddressPool'</span></span>
    - <span data-ttu-id="5d3f2-146">'Set-AzLoadBalancerBackendAddressPool'</span><span class="sxs-lookup"><span data-stu-id="5d3f2-146">'Set-AzLoadBalancerBackendAddressPool'</span></span>
    - <span data-ttu-id="5d3f2-147">'Remove-AzLoadBalancerBackendAddressPool'</span><span class="sxs-lookup"><span data-stu-id="5d3f2-147">'Remove-AzLoadBalancerBackendAddressPool'</span></span>
    - <span data-ttu-id="5d3f2-148">'Get-AzLoadBalancerBackendAddressPool'</span><span class="sxs-lookup"><span data-stu-id="5d3f2-148">'Get-AzLoadBalancerBackendAddressPool'</span></span>
* <span data-ttu-id="5d3f2-149">'New-AzIpGroup'에 대한 이름 유효성 검사 추가</span><span class="sxs-lookup"><span data-stu-id="5d3f2-149">Added name validation for 'New-AzIpGroup'</span></span>
* <span data-ttu-id="5d3f2-150">Azure FirewallPolicy에 대한 새 cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="5d3f2-150">Added new cmdlets for Azure FirewallPolicy</span></span>
    - <span data-ttu-id="5d3f2-151">'New-AzFirewallPolicyThreatIntelWhitelist'</span><span class="sxs-lookup"><span data-stu-id="5d3f2-151">'New-AzFirewallPolicyThreatIntelWhitelist'</span></span>
* <span data-ttu-id="5d3f2-152">기능에 대한 새로운 명령이 업데이트됨: VirtualWan P2SVpnGateway에서 사용자 지정 dns 서버 설정/제거</span><span class="sxs-lookup"><span data-stu-id="5d3f2-152">Updated below commands for feature: Custom dns servers set/remove on VirtualWan P2SVpnGateway.</span></span>
    - <span data-ttu-id="5d3f2-153">New-AzP2sVpnGateway 업데이트됨: 고객이 P2SVpnGateway에 설정할 dns 서버를 지정할 수 있는 선택적 매개 변수 '-CustomDnsServer'가 추가되었으며, 이 매개 변수는 지점 및 사이트 간 클라이언트에서 사용 가능</span><span class="sxs-lookup"><span data-stu-id="5d3f2-153">Updated New-AzP2sVpnGateway: Added optional parameter '-CustomDnsServer' for customers to specify their dns servers to set on P2SVpnGateway, which can be used by Point to site clients.</span></span>
    - <span data-ttu-id="5d3f2-154">Update-AzP2sVpnGateway 업데이트됨: 고객이 P2SVpnGateway에 설정할 dns 서버를 지정할 수 있는 선택적 매개 변수 '-CustomDnsServer'가 추가되었으며, 이 매개 변수는 지점 및 사이트 간 클라이언트에서 사용 가능</span><span class="sxs-lookup"><span data-stu-id="5d3f2-154">Updated Update-AzP2sVpnGateway: Added optional parameter '-CustomDnsServer' for customers to specify their dns servers to set on P2SVpnGateway, which can be used by Point to site clients.</span></span>
* <span data-ttu-id="5d3f2-155">'Update-AzVpnGateway' 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="5d3f2-155">Updated 'Update-AzVpnGateway'</span></span>
    - <span data-ttu-id="5d3f2-156">고객이 VpnGateway에 설정할 사용자 지정 bgps를 지정할 수 있도록 선택적 매개 변수 '-BgpPeeringAddress' 추가</span><span class="sxs-lookup"><span data-stu-id="5d3f2-156">Added optional parameter '-BgpPeeringAddress' for customers to specify their custom bgps to set on VpnGateway.</span></span>
* <span data-ttu-id="5d3f2-157">VirtualHub 리소스의 라우팅 상태 초기화를 지원하는 새 cmdlet 추가:</span><span class="sxs-lookup"><span data-stu-id="5d3f2-157">Added new cmdlet to support resetting the routing state of a VirtualHub resource:</span></span>
    - <span data-ttu-id="5d3f2-158">'Reset-AzHubRouter'</span><span class="sxs-lookup"><span data-stu-id="5d3f2-158">'Reset-AzHubRouter'</span></span>
* <span data-ttu-id="5d3f2-159">방화벽 정책에 대한 최근 Swagger 변화에 따라 아래 항목 업데이트</span><span class="sxs-lookup"><span data-stu-id="5d3f2-159">Updated below things based on recent swagger change for Firewall Policy</span></span>
    - <span data-ttu-id="5d3f2-160">RuleGroup, RuleCollectionGroup 및 RuleType의 이름 변경</span><span class="sxs-lookup"><span data-stu-id="5d3f2-160">Changes names for RuleGroup, RuleCollectionGroup and RuleType</span></span>
    - <span data-ttu-id="5d3f2-161">여러 NAT 규칙 컬렉션을 지원하도록 방화벽 정책 NAT 규칙 컬렉션에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="5d3f2-161">Added support for Firewall Policy NAT Rule Collections to support multiple NAT Rule Collection</span></span>
* <span data-ttu-id="5d3f2-162">[호환성이 손상되는 변경] 'New-AzFirewallPolicyApplicationRule' 및 'New-AzFirewallPolicyNetworkRule'에 대한 필수 매개 변수 'SourceIpGroup' 추가</span><span class="sxs-lookup"><span data-stu-id="5d3f2-162">[Breaking Change] Added mandatory parameter 'SourceIpGroup' for 'New-AzFirewallPolicyApplicationRule' and 'New-AzFirewallPolicyNetworkRule'.</span></span>
* <span data-ttu-id="5d3f2-163">[호환성이 손상되는 변경] 'New-AzFirewallPolicyApplicationRule' 수정, 'SourceAddress' 매개 변수를 필수로 변경</span><span class="sxs-lookup"><span data-stu-id="5d3f2-163">[Breaking Change] Fixed 'New-AzFirewallPolicyApplicationRule', parameter 'SourceAddress' to be mandatory.</span></span>
* <span data-ttu-id="5d3f2-164">[호환성이 손상되는 변경] 'New-AzFirewallPolicyApplicationRule' 수정, 'SourceAddress' 매개 변수를 필수로 변경</span><span class="sxs-lookup"><span data-stu-id="5d3f2-164">[Breaking Change] Fixed 'New-AzFirewallPolicyApplicationRule', parameter 'SourceAddress' to be mandatory.</span></span>
* <span data-ttu-id="5d3f2-165">[호환성이 손상되는 변경] 다음 필수 매개 변수 제거: 'New-AzFirewallPolicyNatRuleCollection'의 'TranslatedAddress', 'TranslatedPort'</span><span class="sxs-lookup"><span data-stu-id="5d3f2-165">[Breaking Change] Removed mandatory parameters: 'TranslatedAddress', 'TranslatedPort' for 'New-AzFirewallPolicyNatRuleCollection'.</span></span>
* <span data-ttu-id="5d3f2-166">PrivateLink On Application Gateway를 지원하는 새 cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="5d3f2-166">Added new cmdlets to support PrivateLink On Application Gateway</span></span>
    - <span data-ttu-id="5d3f2-167">'New-AzApplicationGatewayPrivateLinkConfiguration'</span><span class="sxs-lookup"><span data-stu-id="5d3f2-167">'New-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="5d3f2-168">'Get-AzApplicationGatewayPrivateLinkConfiguration'</span><span class="sxs-lookup"><span data-stu-id="5d3f2-168">'Get-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="5d3f2-169">'New-AzApplicationGatewayPrivateLinkConfiguration'</span><span class="sxs-lookup"><span data-stu-id="5d3f2-169">'New-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="5d3f2-170">'Set-AzApplicationGatewayPrivateLinkConfiguration'</span><span class="sxs-lookup"><span data-stu-id="5d3f2-170">'Set-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="5d3f2-171">'Remove-AzApplicationGatewayPrivateLinkConfiguration'</span><span class="sxs-lookup"><span data-stu-id="5d3f2-171">'Remove-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="5d3f2-172">'New-AzApplicationGatewayPrivateLinkIpConfiguration'</span><span class="sxs-lookup"><span data-stu-id="5d3f2-172">'New-AzApplicationGatewayPrivateLinkIpConfiguration'</span></span>
* <span data-ttu-id="5d3f2-173">VirtualHub의 HubRouteTables 자식 리소스에 대한 새 cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="5d3f2-173">Added new cmdlets for HubRouteTables child resource of VirtualHub.</span></span>
    - <span data-ttu-id="5d3f2-174">'New-AzVHubRoute'</span><span class="sxs-lookup"><span data-stu-id="5d3f2-174">'New-AzVHubRoute'</span></span>
    - <span data-ttu-id="5d3f2-175">'New-AzVHubRouteTable'</span><span class="sxs-lookup"><span data-stu-id="5d3f2-175">'New-AzVHubRouteTable'</span></span>
    - <span data-ttu-id="5d3f2-176">'Get-AzVHubRouteTable'</span><span class="sxs-lookup"><span data-stu-id="5d3f2-176">'Get-AzVHubRouteTable'</span></span>
    - <span data-ttu-id="5d3f2-177">'Update-AzVHubRouteTable'</span><span class="sxs-lookup"><span data-stu-id="5d3f2-177">'Update-AzVHubRouteTable'</span></span>
    - <span data-ttu-id="5d3f2-178">'Remove-AzVHubRouteTable'</span><span class="sxs-lookup"><span data-stu-id="5d3f2-178">'Remove-AzVHubRouteTable'</span></span>
* <span data-ttu-id="5d3f2-179">VirtualWan의 사용자 지정 라우팅에 대한 선택적 RoutingConfiguration 입력 매개 변수를 지원하도록 기존 cmdlet 업데이트</span><span class="sxs-lookup"><span data-stu-id="5d3f2-179">Updated existing cmdlets to support optional RoutingConfiguration input parameter for custom routing in VirtualWan.</span></span>
    - <span data-ttu-id="5d3f2-180">'New-AzExpressRouteConnection'</span><span class="sxs-lookup"><span data-stu-id="5d3f2-180">'New-AzExpressRouteConnection'</span></span>
    - <span data-ttu-id="5d3f2-181">'Set-AzExpressRouteConnection'</span><span class="sxs-lookup"><span data-stu-id="5d3f2-181">'Set-AzExpressRouteConnection'</span></span>
    - <span data-ttu-id="5d3f2-182">'New-AzVirtualHubVnetConnection'</span><span class="sxs-lookup"><span data-stu-id="5d3f2-182">'New-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="5d3f2-183">'Update-AzVirtualHubVnetConnection'</span><span class="sxs-lookup"><span data-stu-id="5d3f2-183">'Update-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="5d3f2-184">'New-AzVpnConnection'</span><span class="sxs-lookup"><span data-stu-id="5d3f2-184">'New-AzVpnConnection'</span></span>
    - <span data-ttu-id="5d3f2-185">'Update-AzVpnConnection'</span><span class="sxs-lookup"><span data-stu-id="5d3f2-185">'Update-AzVpnConnection'</span></span>
    - <span data-ttu-id="5d3f2-186">'New-AzP2sVpnGateway'</span><span class="sxs-lookup"><span data-stu-id="5d3f2-186">'New-AzP2sVpnGateway'</span></span>
    - <span data-ttu-id="5d3f2-187">'Update-AzP2sVpnGateway'</span><span class="sxs-lookup"><span data-stu-id="5d3f2-187">'Update-AzP2sVpnGateway'</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="5d3f2-188">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="5d3f2-188">Az.OperationalInsights</span></span>
* <span data-ttu-id="5d3f2-189">PSWorkspace가 IOperationalInsightsWorkspace를 구현하지 않는 버그 수정 [#12135]</span><span class="sxs-lookup"><span data-stu-id="5d3f2-189">Fixed bug PSWorkspace doesn't implement IOperationalInsightsWorkspace [#12135]</span></span>
* <span data-ttu-id="5d3f2-190">'Set-AzOperationalInsightsWorkspace'에서 'Sku' 매개 변수의 올바른 값 세트에 'pergb2018' 추가</span><span class="sxs-lookup"><span data-stu-id="5d3f2-190">Added 'pergb2018' to valid value set of parameter 'Sku' in 'Set-AzOperationalInsightsWorkspace'</span></span> 
* <span data-ttu-id="5d3f2-191">매개 변수 'FunctionParameter'에 대한 별칭 'FunctionParameters' 추가</span><span class="sxs-lookup"><span data-stu-id="5d3f2-191">Added alias 'FunctionParameters' for parameter 'FunctionParameter' to</span></span>
    - <span data-ttu-id="5d3f2-192">'New-AzOperationalInsightsSavedSearch'</span><span class="sxs-lookup"><span data-stu-id="5d3f2-192">'New-AzOperationalInsightsSavedSearch'</span></span>
    - <span data-ttu-id="5d3f2-193">'Set-AzOperationalInsightsSavedSearch'</span><span class="sxs-lookup"><span data-stu-id="5d3f2-193">'Set-AzOperationalInsightsSavedSearch'</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="5d3f2-194">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="5d3f2-194">Az.RecoveryServices</span></span>
* <span data-ttu-id="5d3f2-195">Azure Backup에서 MAB 항목을 가져오기 위한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="5d3f2-195">Azure Backup added support for fetching MAB items.</span></span>
* <span data-ttu-id="5d3f2-196">Azure Site Recovery에서 'StandardSSD_LRS' 디스크 형식 지원</span><span class="sxs-lookup"><span data-stu-id="5d3f2-196">Azure Site Recovery supports disk type 'StandardSSD_LRS'</span></span>

#### <a name="azresources"></a><span data-ttu-id="5d3f2-197">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="5d3f2-197">Az.Resources</span></span>
* <span data-ttu-id="5d3f2-198">'PSADUser'에서 'UsageLocation', 'GivenName', 'Surname', 'AccountEnabled', 'MailNickname', 'Mail' 추가 [#10526] [#10497]</span><span class="sxs-lookup"><span data-stu-id="5d3f2-198">Added 'UsageLocation', 'GivenName', 'Surname', 'AccountEnabled', 'MailNickname', 'Mail' on 'PSADUser' [#10526] [#10497]</span></span>
* <span data-ttu-id="5d3f2-199">'Get-AzADUser'에서 '-Mail'이 작동하지 않는 문제 해결 [#11981]</span><span class="sxs-lookup"><span data-stu-id="5d3f2-199">Fixed issue that '-Mail' doesn't work on 'Get-AzADUser' [#11981]</span></span>
* <span data-ttu-id="5d3f2-200">'Get-AzDeploymentWhatIfResult' 및 'Get-AzResourceGroupDeploymentWhatIfResult'에 '-ExcludeChangeType' 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="5d3f2-200">Added '-ExcludeChangeType' parameter to 'Get-AzDeploymentWhatIfResult' and 'Get-AzResourceGroupDeploymentWhatIfResult'</span></span>
* <span data-ttu-id="5d3f2-201">'New-AzDeployment' 및 'New-AzResourceGroupDeployment'에 '-WhatIfExcludeChangeType' 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="5d3f2-201">Added '-WhatIfExcludeChangeType' parameter to 'New-AzDeployment' and 'New-AzResourceGroupDeployment'</span></span>
* <span data-ttu-id="5d3f2-202">보다 나은 오류 메시지를 표시하도록 'Test-Az\*Deployment' cmdlet 업데이트</span><span class="sxs-lookup"><span data-stu-id="5d3f2-202">Updated 'Test-Az\*Deployment' cmdlets to show better error messages</span></span>
* <span data-ttu-id="5d3f2-203">deployment create 및 What-If cmdlet의 '-Name' 매개 변수에 대한 도움말 메시지 수정</span><span class="sxs-lookup"><span data-stu-id="5d3f2-203">Fixed help message for '-Name' parameter of deployment create and What-If cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="5d3f2-204">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="5d3f2-204">Az.Sql</span></span>
* <span data-ttu-id="5d3f2-205">Set SQL Server Azure Active Directory Admin cmdlet의 서비스 주체에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="5d3f2-205">Added support for service principal for Set SQL Server Azure Active Directory Admin cmdlet</span></span>
* <span data-ttu-id="5d3f2-206">데이터 분류 cmdlet의 동기화 문제 해결</span><span class="sxs-lookup"><span data-stu-id="5d3f2-206">Fixed sync issue in Data Classification cmdlets.</span></span>
* <span data-ttu-id="5d3f2-207">'Set-AzSqlServerActiveDirectoryAdministrator'에서 메일로 사용자 검색 지원 [#12192]</span><span class="sxs-lookup"><span data-stu-id="5d3f2-207">Supported searching user by mail on 'Set-AzSqlServerActiveDirectoryAdministrator' [#12192]</span></span>

#### <a name="azstorage"></a><span data-ttu-id="5d3f2-208">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="5d3f2-208">Az.Storage</span></span>
* <span data-ttu-id="5d3f2-209">RequireInfrastructureEncryption을 사용하여 스토리지 계정 만들기 지원</span><span class="sxs-lookup"><span data-stu-id="5d3f2-209">Supported create Storage account with RequireInfrastructureEncryption</span></span>
    -  <span data-ttu-id="5d3f2-210">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="5d3f2-210">'New-AzStorageAccount'</span></span>
* <span data-ttu-id="5d3f2-211">Azure.Core 로딩 논리를 Az.Accounts로 이동</span><span class="sxs-lookup"><span data-stu-id="5d3f2-211">Moved the logic of loading Azure.Core to Az.Accounts</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="5d3f2-212">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="5d3f2-212">Az.Websites</span></span>
* <span data-ttu-id="5d3f2-213">'Restore-AzDeletedWebApp'에서 복원이 실패할 경우 생성된 웹앱을 삭제하는 보호 기능 추가</span><span class="sxs-lookup"><span data-stu-id="5d3f2-213">Added safeguard to delete created webapp if restore failed in 'Restore-AzDeletedWebApp'</span></span>
* <span data-ttu-id="5d3f2-214">'New-AzWebApp' 및 'New-AzWebAppSlot'에 대한 'SourceWebApp.Location' 추가</span><span class="sxs-lookup"><span data-stu-id="5d3f2-214">Added 'SourceWebApp.Location' for 'New-AzWebApp' and 'New-AzWebAppSlot'</span></span>
* <span data-ttu-id="5d3f2-215">'Set-AzWebApp' 및 'Set-AzWebAppSlot'에서 컨테이너 설정을 변경할 수 없는 버그 수정</span><span class="sxs-lookup"><span data-stu-id="5d3f2-215">Fixed bug that prevented changing Container settings in 'Set-AzWebApp' and 'Set-AzWebAppSlot'</span></span>
* <span data-ttu-id="5d3f2-216">Get-AzWebApp에 대한 -Name을 제공하지 않으면 SiteConfig를 가져오는 버그 수정</span><span class="sxs-lookup"><span data-stu-id="5d3f2-216">Fixed bug to get SiteConfig when -Name is not given for Get-AzWebApp</span></span>
* <span data-ttu-id="5d3f2-217">Linux 앱용 ASP를 만드는 지원 추가</span><span class="sxs-lookup"><span data-stu-id="5d3f2-217">Added a support to create ASP for Linux Apps</span></span>
* <span data-ttu-id="5d3f2-218">리소스 그룹 간 복제에 대한 예외 추가</span><span class="sxs-lookup"><span data-stu-id="5d3f2-218">Added exceptions for clone across resource groups</span></span>

## <a name="420---june-2020"></a><span data-ttu-id="5d3f2-219">4.2.0 - 2020년 6월</span><span class="sxs-lookup"><span data-stu-id="5d3f2-219">4.2.0 - June 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="5d3f2-220">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="5d3f2-220">Az.Accounts</span></span>
* <span data-ttu-id="5d3f2-221">Azure Automation 또는 PowerShell 작업에서 Az가 로그를 건너뛸 수 있는 문제 수정[#11492]</span><span class="sxs-lookup"><span data-stu-id="5d3f2-221">Fixed an issue that may cause Az to skip logs in Azure Automation or PowerShell jobs [#11492]</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="5d3f2-222">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="5d3f2-222">Az.AnalysisServices</span></span>
* <span data-ttu-id="5d3f2-223">데이터 평면 cmdlet의 어셈블리 버전 업데이트</span><span class="sxs-lookup"><span data-stu-id="5d3f2-223">Updated assembly version of data plane cmdlets</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="5d3f2-224">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="5d3f2-224">Az.ApiManagement</span></span>
* <span data-ttu-id="5d3f2-225">서비스 관리 cmdlet의 어셈블리 버전 업데이트</span><span class="sxs-lookup"><span data-stu-id="5d3f2-225">Updated assembly version of service management cmdlets</span></span>

#### <a name="azbilling"></a><span data-ttu-id="5d3f2-226">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="5d3f2-226">Az.Billing</span></span>
* <span data-ttu-id="5d3f2-227">소비 cmdlet의 어셈블리 버전 업데이트</span><span class="sxs-lookup"><span data-stu-id="5d3f2-227">Updated assembly version of consumption cmdlets</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="5d3f2-228">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="5d3f2-228">Az.CognitiveServices</span></span>
* <span data-ttu-id="5d3f2-229">PrivateEndpoint 및 PublicNetworkAccess control을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-229">Support PrivateEndpoint and PublicNetworkAccess control.</span></span> 

#### <a name="azdatafactory"></a><span data-ttu-id="5d3f2-230">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="5d3f2-230">Az.DataFactory</span></span>
* <span data-ttu-id="5d3f2-231">데이터 팩터리 V2 cmdlet의 어셈블리 버전 업데이트</span><span class="sxs-lookup"><span data-stu-id="5d3f2-231">Updated assembly version of data factory V2 cmdlets</span></span>

#### <a name="azdatashare"></a><span data-ttu-id="5d3f2-232">Az.DataShare</span><span class="sxs-lookup"><span data-stu-id="5d3f2-232">Az.DataShare</span></span>
* <span data-ttu-id="5d3f2-233">''Az.DataShare'' 모듈의 일반 공급</span><span class="sxs-lookup"><span data-stu-id="5d3f2-233">General availability of ''Az.DataShare'' module</span></span>

#### <a name="azdesktopvirtualization"></a><span data-ttu-id="5d3f2-234">Az.DesktopVirtualization</span><span class="sxs-lookup"><span data-stu-id="5d3f2-234">Az.DesktopVirtualization</span></span>
* <span data-ttu-id="5d3f2-235">''Az.DesktopVirtualization'' 모듈의 일반 공급</span><span class="sxs-lookup"><span data-stu-id="5d3f2-235">General availability of ''Az.DesktopVirtualization'' module</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="5d3f2-236">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="5d3f2-236">Az.OperationalInsights</span></span>
* <span data-ttu-id="5d3f2-237">SDK를 0.21.0으로 업그레이드</span><span class="sxs-lookup"><span data-stu-id="5d3f2-237">Upgraded SDK to 0.21.0</span></span>
* <span data-ttu-id="5d3f2-238">다음에 선택적 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="5d3f2-238">Added optional parameters to</span></span> 
    - <span data-ttu-id="5d3f2-239">'New-AzOperationalInsightsSavedSearch'</span><span class="sxs-lookup"><span data-stu-id="5d3f2-239">'New-AzOperationalInsightsSavedSearch'</span></span>
    - <span data-ttu-id="5d3f2-240">'Set-AzOperationalInsightsSavedSearch'</span><span class="sxs-lookup"><span data-stu-id="5d3f2-240">'Set-AzOperationalInsightsSavedSearch'</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="5d3f2-241">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="5d3f2-241">Az.PolicyInsights</span></span>
* <span data-ttu-id="5d3f2-242">'Start-AzPolicyComplianceScan'의 예제 3 수정</span><span class="sxs-lookup"><span data-stu-id="5d3f2-242">Corrected example 3 for 'Start-AzPolicyComplianceScan'</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="5d3f2-243">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="5d3f2-243">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="5d3f2-244">PowerBI cmdlet의 어셈블리 버전 업데이트</span><span class="sxs-lookup"><span data-stu-id="5d3f2-244">Updated assembly version of PowerBI cmdlets</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="5d3f2-245">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="5d3f2-245">Az.PrivateDns</span></span>
* <span data-ttu-id="5d3f2-246">Remove-AzPrivateDnsRecordSet에 대한 자세한 정보 출력 문자열 형식 수정</span><span class="sxs-lookup"><span data-stu-id="5d3f2-246">Corrected verbose output string formatting for Remove-AzPrivateDnsRecordSet</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="5d3f2-247">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="5d3f2-247">Az.RecoveryServices</span></span>
* <span data-ttu-id="5d3f2-248">xml 입력에서 영역 간 복제를 위한 복구 계획을 세우기 위한 Azure Site Recovery 지원.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-248">Azure Site Recovery support for creating recovery plan for zone to zone replication from xml input.</span></span>
* <span data-ttu-id="5d3f2-249">SiteRecovery 및 Backup cmdlet의 어셈블리 버전 업데이트</span><span class="sxs-lookup"><span data-stu-id="5d3f2-249">Updated assembly version of SiteRecovery and Backup cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="5d3f2-250">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="5d3f2-250">Az.Resources</span></span>
* <span data-ttu-id="5d3f2-251">Get-AzDeploymentScriptLog 및 Save-AzDeploymentScriptLog cmdlet에 Tail 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="5d3f2-251">Added Tail parameter to Get-AzDeploymentScriptLog and Save-AzDeploymentScriptLog cmdlets</span></span>
* <span data-ttu-id="5d3f2-252">형식이 지정된 출력 속성을 Get-AzDeploymentScript cmdlet 출력에 표시</span><span class="sxs-lookup"><span data-stu-id="5d3f2-252">Formatted Output property and show it on the Get-AzDeploymentScript cmdlet output</span></span>
* <span data-ttu-id="5d3f2-253">-DeploymentScriptInputObject 매개 변수의 이름이 -DeploymentScriptObject로 변경</span><span class="sxs-lookup"><span data-stu-id="5d3f2-253">Renamed -DeploymentScriptInputObject parameter to -DeploymentScriptObject</span></span>
* <span data-ttu-id="5d3f2-254">cmdlet 메시지에서 누락된 파일/대상 이름이 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-254">Fixed missing file/target name in cmdlet messages.</span></span>
* <span data-ttu-id="5d3f2-255">리소스 관리자 및 태그 cmdlet의 어셈블리 버전 업데이트</span><span class="sxs-lookup"><span data-stu-id="5d3f2-255">Updated assembly version of resource manager and tags cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="5d3f2-256">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="5d3f2-256">Az.Sql</span></span>
* <span data-ttu-id="5d3f2-257">UsePrivateLinkConnection을 'New-AzSqlSyncGroup', 'Update-AzSqlSyncGroup', 'New-AzSqlSyncMember' 및 'Update-AzSqlSyncMember'에 추가</span><span class="sxs-lookup"><span data-stu-id="5d3f2-257">Added UsePrivateLinkConnection to 'New-AzSqlSyncGroup', 'Update-AzSqlSyncGroup', 'New-AzSqlSyncMember' and 'Update-AzSqlSyncMember'</span></span>
* <span data-ttu-id="5d3f2-258">SyncMemberAzureDatabaseResourceId를 'New-AzSqlSyncMember' 및 'Update-AzSqlSyncMember'에 추가</span><span class="sxs-lookup"><span data-stu-id="5d3f2-258">Added SyncMemberAzureDatabaseResourceId to 'New-AzSqlSyncMember' and 'Update-AzSqlSyncMember'</span></span>
* <span data-ttu-id="5d3f2-259">SQL Server Azure Active Directory Admin cmdlet을 설정하는 게스트 사용자 조회 지원 추가</span><span class="sxs-lookup"><span data-stu-id="5d3f2-259">Added Guest user lookup support to Set SQL Server Azure Active Directory Admin cmdlet</span></span>

#### <a name="azstorage"></a><span data-ttu-id="5d3f2-260">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="5d3f2-260">Az.Storage</span></span>
* <span data-ttu-id="5d3f2-261">데이터 평면 cmdlet의 어셈블리 버전 업데이트</span><span class="sxs-lookup"><span data-stu-id="5d3f2-261">Updated assembly version of data plane cmdlets</span></span>

## <a name="410---may-2020"></a><span data-ttu-id="5d3f2-262">4.1.0 - 2020년 5월</span><span class="sxs-lookup"><span data-stu-id="5d3f2-262">4.1.0 - May 2020</span></span>
### <a name="highlights-since-the-last-release"></a><span data-ttu-id="5d3f2-263">마지막 릴리스 이후의 주요 사항</span><span class="sxs-lookup"><span data-stu-id="5d3f2-263">Highlights since the last release</span></span>
* <span data-ttu-id="5d3f2-264">지원되는 PowerShell 버전: Windows PowerShell 5.1, PowerShell Core 6.2.4 이상, PowerShell 7</span><span class="sxs-lookup"><span data-stu-id="5d3f2-264">Supported PowerShell versions: Windows PowerShell 5.1, PowerShell Core 6.2.4+, PowerShell 7</span></span>
* <span data-ttu-id="5d3f2-265">Az.Functions 일반 공급</span><span class="sxs-lookup"><span data-stu-id="5d3f2-265">General availability of Az.Functions</span></span> 
* <span data-ttu-id="5d3f2-266">Az.ApiManagement, Az.Batch, Az.Compute, Az.KeyVault, Az.Monitor, Az.Network, Az.OperationalInsights, Az.Resources 및 Az.Storage의 주요 릴리스 출시</span><span class="sxs-lookup"><span data-stu-id="5d3f2-266">Az.ApiManagement, Az.Batch, Az.Compute, Az.KeyVault, Az.Monitor, Az.Network, Az.OperationalInsights, Az.Resources, and Az.Storage have major release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="5d3f2-267">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="5d3f2-267">Az.Accounts</span></span>
* <span data-ttu-id="5d3f2-268">'AzureSynapseAnalyticsEndpointResourceId' 및 'AzureSynapseAnalyticsEndpointSuffix' 매개 변수를 허용하도록 'Add-AzEnvironment' 및 'Set-AzEnvironment' 업데이트</span><span class="sxs-lookup"><span data-stu-id="5d3f2-268">Updated 'Add-AzEnvironment' and 'Set-AzEnvironment' to accept parameters 'AzureSynapseAnalyticsEndpointResourceId' and 'AzureSynapseAnalyticsEndpointSuffix'</span></span>
* <span data-ttu-id="5d3f2-269">Az.Accounts에 Azure.Core 관련 어셈블리가 추가되었으며 지원되는 PowerShell 플랫폼은 Windows PowerShell 5.1, PowerShell Core 6.2.4, PowerShell 7+입니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-269">Added Azure.Core related assemblies into Az.Accounts, supported PowerShell platforms include Windows PowerShell 5.1, PowerShell Core 6.2.4, PowerShell 7+</span></span>

#### <a name="azaks"></a><span data-ttu-id="5d3f2-270">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="5d3f2-270">Az.Aks</span></span>
* <span data-ttu-id="5d3f2-271">API 버전을 2019-10-01로 업그레이드</span><span class="sxs-lookup"><span data-stu-id="5d3f2-271">Upgraded API Version to 2019-10-01</span></span>
* <span data-ttu-id="5d3f2-272">Windows 컨테이너를 사용하여 AKS 만들기 지원</span><span class="sxs-lookup"><span data-stu-id="5d3f2-272">Supported to create AKS using Windows container</span></span>
* <span data-ttu-id="5d3f2-273">새 cmdlet 추가: 'New-AzAksNodePool', 'Update-AzAksNodePool', 'Remove-AzAksNodePool', 'Get-AzAksNodePool', 'Install-AzAksKubectl', 'Get-AzAksVersion'</span><span class="sxs-lookup"><span data-stu-id="5d3f2-273">Provided new cmdlets: 'New-AzAksNodePool', 'Update-AzAksNodePool', 'Remove-AzAksNodePool',        'Get-AzAksNodePool', 'Install-AzAksKubectl', 'Get-AzAksVersion'</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="5d3f2-274">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="5d3f2-274">Az.ApiManagement</span></span>
* <span data-ttu-id="5d3f2-275">'New-AzApiManagement' 및 'Set-AzApiManagement': [-AssignIdentity] 매개 변수 이름을 [-SystemAssignedIdentity]로 변경</span><span class="sxs-lookup"><span data-stu-id="5d3f2-275">'New-AzApiManagement' and 'Set-AzApiManagement': [-AssignIdentity] parameter renamed as [-SystemAssignedIdentity]</span></span>
* <span data-ttu-id="5d3f2-276">'New-AzApiManagement' 및 'Set-AzApiManagement': 새 매개 변수 추가: [-UserAssignedIdentity <String[]>]</span><span class="sxs-lookup"><span data-stu-id="5d3f2-276">'New-AzApiManagement' and 'Set-AzApiManagement': New parameter added: [-UserAssignedIdentity <String[]>]</span></span>
* <span data-ttu-id="5d3f2-277">'Get-AzApiManagementProperty': 'Get-AzApiManagementNamedValue'로 이름 변경.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-277">'Get-AzApiManagementProperty': renamed as 'Get-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="5d3f2-278">PropertyId 매개 변수 이름을 NamedValueId로 변경.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-278">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="5d3f2-279">'New-AzApiManagementProperty': 'New-AzApiManagementNamedValue'로 이름 변경.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-279">'New-AzApiManagementProperty': renamed as 'New-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="5d3f2-280">PropertyId 매개 변수 이름을 NamedValueId로 변경.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-280">PropertyId parameter renamed as NamedValueId.</span></span> 
* <span data-ttu-id="5d3f2-281">'Set-AzApiManagementProperty': 'Set-AzApiManagementNamedValue'로 이름 변경.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-281">'Set-AzApiManagementProperty': renamed as 'Set-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="5d3f2-282">PropertyId 매개 변수 이름을 NamedValueId로 변경.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-282">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="5d3f2-283">'Remove-AzApiManagementProperty': 'Remove-AzApiManagementNamedValue'로 이름 변경.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-283">'Remove-AzApiManagementProperty': renamed as 'Remove-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="5d3f2-284">PropertyId 매개 변수 이름을 NamedValueId로 변경.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-284">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="5d3f2-285">새 'Get-AzApiManagementAuthorizationServerClientSecret' cmdlet이 추가되었으며 'Get-AzApiManagementAuthorizationServer'는 더 이상 클라이언트 암호를 반환하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-285">Added new 'Get-AzApiManagementAuthorizationServerClientSecret' cmdlet and 'Get-AzApiManagementAuthorizationServer' will not return client secret anymore.</span></span>
* <span data-ttu-id="5d3f2-286">새 'Get-AzApiManagementNamedValueSecretValue' cmdlet이 추가되었으며 'Get-AzApiManagementNamedValue'는 더 이상 비밀 값을 반환하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-286">Added new 'Get-AzApiManagementNamedValueSecretValue' cmdlet and 'Get-AzApiManagementNamedValue' will not return secret value.</span></span>
* <span data-ttu-id="5d3f2-287">새 'Get-AzApiManagementOpenIdConnectProviderClientSecret' cmdlet이 추가되었으며 'Get-AzApiManagementOpenIdConnectProvider'는 더 이상 클라이언트 암호를 반환하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-287">Added new 'Get-AzApiManagementOpenIdConnectProviderClientSecret' cmdlet and 'Get-AzApiManagementOpenIdConnectProvider' will not return client secret anymore.</span></span>
* <span data-ttu-id="5d3f2-288">새 'Get-AzApiManagementSubscriptionKey' cmdlet이 추가되었으며 'Get-AzApiManagementSubscription'은 더 이상 구독 키를 반환하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-288">Added new 'Get-AzApiManagementSubscriptionKey' cmdlet and 'Get-AzApiManagementSubscription' will not return subscription keys anymore.</span></span>
* <span data-ttu-id="5d3f2-289">새 'Get-AzApiManagementTenantAccessSecret' cmdlet이 추가되었으며 'Get-AzApiManagementTenantAccess'는 더 이상 키를 반환하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-289">Added new 'Get-AzApiManagementTenantAccessSecret' cmdlet and 'Get-AzApiManagementTenantAccess' will not return keys anymore.</span></span>
* <span data-ttu-id="5d3f2-290">새 'Get-AzApiManagementTenantGitAccessSecret' cmdlet이 추가되었으며 'Get-AzApiManagementTenantGitAccess'는 더 이상 키를 반환하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-290">Added new 'Get-AzApiManagementTenantGitAccessSecret' cmdlet and 'Get-AzApiManagementTenantGitAccess' will not return keys anymore.</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="5d3f2-291">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="5d3f2-291">Az.ApplicationInsights</span></span>
* <span data-ttu-id="5d3f2-292">매개 변수 추가: 'New-AzApplicationInsights'에 대한 'RetentionInDays' 'PublicNetworkAccessForIngestion' 'PublicNetworkAccessForQuery'</span><span class="sxs-lookup"><span data-stu-id="5d3f2-292">Added Parameters: 'RetentionInDays' 'PublicNetworkAccessForIngestion' 'PublicNetworkAccessForQuery' for 'New-AzApplicationInsights'</span></span>
* <span data-ttu-id="5d3f2-293">'Update-AzApplicationInsights' cmdlet 작성</span><span class="sxs-lookup"><span data-stu-id="5d3f2-293">Created cmdlet 'Update-AzApplicationInsights'</span></span>
* <span data-ttu-id="5d3f2-294">연결된 스토리지 계정에 대한 cmdlet 작성</span><span class="sxs-lookup"><span data-stu-id="5d3f2-294">Created cmdlets for Linked Storage Account</span></span>

#### <a name="azbatch"></a><span data-ttu-id="5d3f2-295">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="5d3f2-295">Az.Batch</span></span>
* <span data-ttu-id="5d3f2-296">'Microsoft.Azure.Batch' SDK 버전 13.0.0 및 'Microsoft.Azure.Management.Batch' SDK 버전 9.0.0을 사용하도록 Az.Batch가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-296">Updated Az.Batch to use 'Microsoft.Azure.Batch' SDK version 13.0.0 and 'Microsoft.Azure.Management.Batch' SDK version 9.0.0.</span></span>
* <span data-ttu-id="5d3f2-297">새 '-CertificateKind' 매개 변수를 사용하여 'AzBatchCertificate'에 추가할 인증서 종류를 선택하는 기능이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-297">Added the ability to select the kind of certificate being added using the new '-CertificateKind' parameter to 'New-AzBatchCertificate'.</span></span>
* <span data-ttu-id="5d3f2-298">이전에 항상 ''였던 'ApplicationPackages' 속성이 'PSApplication'에서 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-298">Removed 'ApplicationPackages' property from 'PSApplication' which was previously always ''.</span></span>
  - <span data-ttu-id="5d3f2-299">이제 'Get-AzBatchApplicationPackage'를 사용하여 애플리케이션 내부의 특정 패키지를 검색할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-299">The specific packages inside of an application now can be retrieved using 'Get-AzBatchApplicationPackage'.</span></span> <span data-ttu-id="5d3f2-300">예를 들면 다음과 같습니다. 'Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication'.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-300">For example: 'Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication'.</span></span>
* <span data-ttu-id="5d3f2-301">'New-AzBatchPool'을 사용하여 풀을 만들 때 'PSImageReference'의 'VirtualMachineImageId' 속성은 이제 Shared Image Gallery 이미지만 참조할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-301">When creating a pool using 'New-AzBatchPool', the 'VirtualMachineImageId' property of 'PSImageReference' can now only refer to a Shared Image Gallery image.</span></span>
* <span data-ttu-id="5d3f2-302">'New-AzBatchPool'을 사용하여 풀을 만들 때 공용 IP 없이 'PSNetworkConfiguration'의 새 'PublicIPAddressConfiguration'을 사용하여 풀을 프로비저닝할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-302">When creating a pool using 'New-AzBatchPool', the pool can be provisioned without a public IP using the new 'PublicIPAddressConfiguration' property of 'PSNetworkConfiguration'.</span></span>
  - <span data-ttu-id="5d3f2-303">'PSNetworkConfiguration'의 'PublicIPs' 속성도 'PSPublicIPAddressConfiguration'으로 이동되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-303">The 'PublicIPs' property of 'PSNetworkConfiguration' has moved in to 'PSPublicIPAddressConfiguration' as well.</span></span> <span data-ttu-id="5d3f2-304">이 속성은 'IPAddressProvisioningType'이 'UserManaged'인 경우에만 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-304">This property can only be specified if 'IPAddressProvisioningType' is 'UserManaged'.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="5d3f2-305">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="5d3f2-305">Az.Compute</span></span>
* <span data-ttu-id="5d3f2-306">'Update-AzVM' cmdlet에 HostId 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="5d3f2-306">Added HostId parameter to 'Update-AzVM' cmdlet</span></span>
* <span data-ttu-id="5d3f2-307">'New-AzVMConfig', 'New-AzVmssConfig', 'Update-AzVmss', 'Set-AzVMOperatingSystem' 및 'Set-AzVmssOsProfile' cmdlet의 도움말 문서가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-307">Updated Help documents for 'New-AzVMConfig', 'New-AzVmssConfig', 'Update-AzVmss', 'Set-AzVMOperatingSystem' and 'Set-AzVmssOsProfile' cmdlets.</span></span>
* <span data-ttu-id="5d3f2-308">주요 변경 내용</span><span class="sxs-lookup"><span data-stu-id="5d3f2-308">Breaking changes</span></span>
    - <span data-ttu-id="5d3f2-309">'Get-AzVMImage' cmdlet에서 FilterExpression 매개 변수가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-309">FilterExpression parameter is removed from 'Get-AzVMImage' cmdlet.</span></span>
    - <span data-ttu-id="5d3f2-310">'New-AzVmssConfig', 'New-AzVMConfig' 및 'Update-AzVM' cmdlet에서 AssignIdentity 매개 변수가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-310">AssignIdentity parameter is removed from 'New-AzVmssConfig', 'New-AzVMConfig' and 'Update-AzVM' cmdlets.</span></span>
    - <span data-ttu-id="5d3f2-311">'New-AzVmssConfig' 및 'Update-AzVmss' cmdlet에서 AutomaticRepairMaxInstanceRepairsPercent가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-311">AutomaticRepairMaxInstanceRepairsPercent is removed from 'New-AzVmssConfig' and 'Update-AzVmss' cmdlets.</span></span>
    - <span data-ttu-id="5d3f2-312">ProximityPlacementGroup에서 AvailabilitySetsColocationStatus, VirtualMachinesColocationStatus 및 VirtualMachineScaleSetsColocationStatus 속성이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-312">AvailabilitySetsColocationStatus, VirtualMachinesColocationStatus and VirtualMachineScaleSetsColocationStatus properties are removed from ProximityPlacementGroup.</span></span>
    - <span data-ttu-id="5d3f2-313">AutomaticRepairsPolicy에서 MaxInstanceRepairsPercent 속성이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-313">MaxInstanceRepairsPercent property is removed from AutomaticRepairsPolicy.</span></span>
    - <span data-ttu-id="5d3f2-314">AvailabilitySets, VirtualMachines 및 VirtualMachineScaleSets 형식이 IList<SubResource>에서 IList<SubResourceWithColocationStatus>로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-314">The types of AvailabilitySets, VirtualMachines and VirtualMachineScaleSets are changed from IList<SubResource> to IList<SubResourceWithColocationStatus>.</span></span>
* <span data-ttu-id="5d3f2-315">'Get-AzVM' cmdlet에 대한 설명이 보다 정확하게 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-315">Description for 'Get-AzVM' cmdlet has been updated to better describe it.</span></span> 

#### <a name="azdatafactory"></a><span data-ttu-id="5d3f2-316">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="5d3f2-316">Az.DataFactory</span></span>
* <span data-ttu-id="5d3f2-317">Managed IR에서 데이터 흐름 런타임 속성의 CRUD를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-317">Supported CRUD of data flow runtime properties in Managed IR.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="5d3f2-318">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="5d3f2-318">Az.FrontDoor</span></span>
* <span data-ttu-id="5d3f2-319">Front Door 규칙 엔진 개체를 생성, 업데이트, 검색 및 삭제할 수 있는 새 cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="5d3f2-319">Added new cmdlets for creation, update, retreival, and deletion of Front Door Rules Engine object</span></span>
* <span data-ttu-id="5d3f2-320">Front Door 규칙 엔진 개체를 작성할 수 있는 도우미 cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="5d3f2-320">Added helper cmdlets for construction of Front Door Rules Engine object</span></span>
* <span data-ttu-id="5d3f2-321">Front Door 회람 규칙 개체에 대한 규칙 엔진 참조 추가</span><span class="sxs-lookup"><span data-stu-id="5d3f2-321">Added Rules Engine reference to Front Door Routing Rule object.</span></span>
* <span data-ttu-id="5d3f2-322">Front Door 백 엔드 개체에 Private Link 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="5d3f2-322">Added Private Link parameters to Front Door Backend object</span></span>

#### <a name="azfunctions"></a><span data-ttu-id="5d3f2-323">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="5d3f2-323">Az.Functions</span></span>
* <span data-ttu-id="5d3f2-324">''Az.Functions'' 모듈의 일반 공급</span><span class="sxs-lookup"><span data-stu-id="5d3f2-324">General availability of ''Az.Functions'' module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="5d3f2-325">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="5d3f2-325">Az.HDInsight</span></span>
* <span data-ttu-id="5d3f2-326">고객 관리형 키 디스크 암호화 지원</span><span class="sxs-lookup"><span data-stu-id="5d3f2-326">Supported Customer-managed key disk encryption.</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="5d3f2-327">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="5d3f2-327">Az.HealthcareApis</span></span>
* <span data-ttu-id="5d3f2-328">더 이상 액세스 정책이 기본적으로 현재 보안 주체로 설정되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-328">Access policies are no longer defaulted to the current principal</span></span>

#### <a name="aziothub"></a><span data-ttu-id="5d3f2-329">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="5d3f2-329">Az.IotHub</span></span>
* <span data-ttu-id="5d3f2-330">SQL과 비슷한 언어를 사용하여 정보를 검색하기 위해 IoT 허브에서 쿼리를 호출하는 cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-330">Added cmdlet to invoke a query in an IoT hub to retrieve information using a SQL-like language.</span></span>
* <span data-ttu-id="5d3f2-331">'Add-AzIotHubDevice'가 자식 디바이스 없는 에지 지원 디바이스를 만들 수 없는 문제 해결 [#11597]</span><span class="sxs-lookup"><span data-stu-id="5d3f2-331">Fix issue that 'Add-AzIotHubDevice' fails to create Edge Enabled Device without child devices [#11597]</span></span>
* <span data-ttu-id="5d3f2-332">IoT Hub, 디바이스 또는 모듈에 대한 SAS 토큰을 생성하는 cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-332">Added cmdlet to generate SAS token for Iot Hub, device or module.</span></span>
* <span data-ttu-id="5d3f2-333">구성 메트릭 쿼리를 호출하는 cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-333">Added cmdlet to invoke configuration metrics query.</span></span>
* <span data-ttu-id="5d3f2-334">IoT Edge 자동 배포를 대규모로 관리합니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-334">Manage IoT Edge automatic deployment at scale.</span></span> <span data-ttu-id="5d3f2-335">새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-335">New cmdlets are:</span></span>
    - <span data-ttu-id="5d3f2-336">'Add-AzIotHubDeployment'</span><span class="sxs-lookup"><span data-stu-id="5d3f2-336">'Add-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="5d3f2-337">'Get-AzIotHubDeployment'</span><span class="sxs-lookup"><span data-stu-id="5d3f2-337">'Get-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="5d3f2-338">'Remove-AzIotHubDeployment'</span><span class="sxs-lookup"><span data-stu-id="5d3f2-338">'Remove-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="5d3f2-339">'Set-AzIotHubDeployment'</span><span class="sxs-lookup"><span data-stu-id="5d3f2-339">'Set-AzIotHubDeployment'</span></span>
* <span data-ttu-id="5d3f2-340">IoT Edge 배포 메트릭 쿼리를 호출하는 cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-340">Added cmdlet to invoke an IoT Edge deployment metrics query.</span></span>
* <span data-ttu-id="5d3f2-341">지정된 에지 디바이스에 구성 콘텐츠를 적용하는 cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-341">Added cmdlet to apply the configuration content to the specified edge device.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="5d3f2-342">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="5d3f2-342">Az.KeyVault</span></span>
* <span data-ttu-id="5d3f2-343">다음 별칭 제거: 'New-AzKeyVaultCertificateAdministratorDetails' 및 'New-AzKeyVaultCertificateOrganizationDetails'</span><span class="sxs-lookup"><span data-stu-id="5d3f2-343">Removed two aliases: 'New-AzKeyVaultCertificateAdministratorDetails' and 'New-AzKeyVaultCertificateOrganizationDetails'</span></span>
* <span data-ttu-id="5d3f2-344">키 자격 증명 모음을 만들 때 기본적으로 일시 삭제 사용</span><span class="sxs-lookup"><span data-stu-id="5d3f2-344">Enabled soft delete by default when creating a key vault</span></span>
* <span data-ttu-id="5d3f2-345">키 자격 증명 모음을 만들 때 특정 네트워크 위치의 액세스를 제어하도록 네트워크 규칙을 설정할 수 있음</span><span class="sxs-lookup"><span data-stu-id="5d3f2-345">Network rules can be set to govern the accessibility from specific network locations when creating a key vault</span></span>
* <span data-ttu-id="5d3f2-346">BYOK(Bring Your Own Key) 지원 추가</span><span class="sxs-lookup"><span data-stu-id="5d3f2-346">Added support to bring your own key (BYOK)</span></span>
    - <span data-ttu-id="5d3f2-347">'Add-AzKeyVaultKey'가 키 교환 키 생성 지원</span><span class="sxs-lookup"><span data-stu-id="5d3f2-347">'Add-AzKeyVaultKey' supports generating a key exchange key</span></span>
    - <span data-ttu-id="5d3f2-348">'Get-AzKeyVaultKey'가 PEM 형식의 공개 키 다운로드 지원</span><span class="sxs-lookup"><span data-stu-id="5d3f2-348">'Get-AzKeyVaultKey' supports downloading a public key in PEM format</span></span>
* <span data-ttu-id="5d3f2-349">'AzKeyVaultKey' 도움말 문서의 'KeyOps' 부분 업데이트</span><span class="sxs-lookup"><span data-stu-id="5d3f2-349">Updated the 'KeyOps' part of the help document of 'Add-AzKeyVaultKey'</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="5d3f2-350">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="5d3f2-350">Az.Monitor</span></span>
* <span data-ttu-id="5d3f2-351">'Set-AzDiagnosticSettings'의 버그 수정, 일부 범주에는 보존 정책이 적용되지 않음 [#11589]</span><span class="sxs-lookup"><span data-stu-id="5d3f2-351">Fixed bug for 'Set-AzDiagnosticSettings', retention policy won't apply to all categories [#11589]</span></span>
* <span data-ttu-id="5d3f2-352">메트릭 경고 V2에 WebTest를 사용하기 위한 조건 지원</span><span class="sxs-lookup"><span data-stu-id="5d3f2-352">Supported WebTest availability criteria for metric alert V2</span></span>
    - <span data-ttu-id="5d3f2-353">'New-AzMetricAlertRuleV2Criteria': webtest 사용 조건을 만드는 옵션 추가</span><span class="sxs-lookup"><span data-stu-id="5d3f2-353">'New-AzMetricAlertRuleV2Criteria': an option to create webtest availability criteria was added</span></span>
    - <span data-ttu-id="5d3f2-354">'Add-AzMetricAlertRuleV2': 새 webtest 사용 조건 지원</span><span class="sxs-lookup"><span data-stu-id="5d3f2-354">'Add-AzMetricAlertRuleV2': supports the new webtest availability criteria</span></span>
* <span data-ttu-id="5d3f2-355">PSLogProfile에서 RetentionPolicy에 대한 중복 정의 제거 [#7608]</span><span class="sxs-lookup"><span data-stu-id="5d3f2-355">Removed redundant definition for RetentionPolicy in PSLogProfile [#7608]</span></span>
* <span data-ttu-id="5d3f2-356">PSEventData에 정의된 중복 속성 제거 [#11353]</span><span class="sxs-lookup"><span data-stu-id="5d3f2-356">Removed redundant properties difined in PSEventData [#11353]</span></span>
* <span data-ttu-id="5d3f2-357">'Get-AzLog'를 'Get-AzActivityLog'로 이름 변경</span><span class="sxs-lookup"><span data-stu-id="5d3f2-357">Renamed 'Get-AzLog' to 'Get-AzActivityLog'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="5d3f2-358">Az.Network</span><span class="sxs-lookup"><span data-stu-id="5d3f2-358">Az.Network</span></span>
* <span data-ttu-id="5d3f2-359">영역 기본 동작이 변경된다는 것을 알리기 위해 주요 변경 특성을 추가</span><span class="sxs-lookup"><span data-stu-id="5d3f2-359">Added breaking change attribute to notify that Zone default behaviour will be changed</span></span>
    - <span data-ttu-id="5d3f2-360">'New-AzPublicIpAddress'</span><span class="sxs-lookup"><span data-stu-id="5d3f2-360">'New-AzPublicIpAddress'</span></span>
    - <span data-ttu-id="5d3f2-361">'New-AzPublicIpPrefix'</span><span class="sxs-lookup"><span data-stu-id="5d3f2-361">'New-AzPublicIpPrefix'</span></span>
    - <span data-ttu-id="5d3f2-362">'New-AzLoadBalancerFrontendIpConfig'</span><span class="sxs-lookup"><span data-stu-id="5d3f2-362">'New-AzLoadBalancerFrontendIpConfig'</span></span>
* <span data-ttu-id="5d3f2-363">새로운 최상위 리소스 SecurityPartnerProvider에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="5d3f2-363">Added support for a new top level resource SecurityPartnerProvider</span></span>
    - <span data-ttu-id="5d3f2-364">추가된 새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-364">New cmdlets added:</span></span>
        - <span data-ttu-id="5d3f2-365">New-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="5d3f2-365">New-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="5d3f2-366">Remove-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="5d3f2-366">Remove-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="5d3f2-367">Get-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="5d3f2-367">Get-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="5d3f2-368">Set-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="5d3f2-368">Set-AzSecurityPartnerProvider</span></span>
* <span data-ttu-id="5d3f2-369">'PSPrivateEndpointConnection'의 'PSPrivateLinkResource' 및 'GroupId'에서 'RequiredZoneNames' 추가</span><span class="sxs-lookup"><span data-stu-id="5d3f2-369">Added 'RequiredZoneNames' on 'PSPrivateLinkResource' and 'GroupId' on 'PSPrivateEndpointConnection'</span></span>
* <span data-ttu-id="5d3f2-370">New-AzNetworkWatcherConnectionMonitorTestConfigurationObject에 대한 잘못된 형식의 SuccessThresholdRoundTripTimeMs 매개 변수 수정</span><span class="sxs-lookup"><span data-stu-id="5d3f2-370">Fixed incorrect type of SuccessThresholdRoundTripTimeMs parameter for New-AzNetworkWatcherConnectionMonitorTestConfigurationObject</span></span>
* <span data-ttu-id="5d3f2-371">AllowVnetToVnetTraffic 인수의 기본값을 True로 설정하도록 VirtualWan cmdlet 업데이트</span><span class="sxs-lookup"><span data-stu-id="5d3f2-371">Updated VirtualWan cmdlets to set default value of AllowVnetToVnetTraffic argument to True.</span></span>
    - <span data-ttu-id="5d3f2-372">'New-AzVirtualWan'</span><span class="sxs-lookup"><span data-stu-id="5d3f2-372">'New-AzVirtualWan'</span></span>
    - <span data-ttu-id="5d3f2-373">'Update-AzVirtualWan'</span><span class="sxs-lookup"><span data-stu-id="5d3f2-373">'Update-AzVirtualWan'</span></span>
* <span data-ttu-id="5d3f2-374">프라이빗 엔드포인트에 대한 DNS 영역 그룹을 지원하는 새 cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="5d3f2-374">Added new cmdlets to support DNS zone group for private endpoint</span></span>
    - <span data-ttu-id="5d3f2-375">'New-AzPrivateDnsZoneConfig'</span><span class="sxs-lookup"><span data-stu-id="5d3f2-375">'New-AzPrivateDnsZoneConfig'</span></span>
    - <span data-ttu-id="5d3f2-376">'Get-AzPrivateDnsZoneGroup'</span><span class="sxs-lookup"><span data-stu-id="5d3f2-376">'Get-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="5d3f2-377">'New-AzPrivateDnsZoneGroup'</span><span class="sxs-lookup"><span data-stu-id="5d3f2-377">'New-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="5d3f2-378">'Set-AzPrivateDnsZoneGroup'</span><span class="sxs-lookup"><span data-stu-id="5d3f2-378">'Set-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="5d3f2-379">'Remove-AzPrivateDnsZoneGroup'</span><span class="sxs-lookup"><span data-stu-id="5d3f2-379">'Remove-AzPrivateDnsZoneGroup'</span></span>
* <span data-ttu-id="5d3f2-380">'AzureFirewall'에 'DNSEnableProxy', 'DNSRequireProxyForNetworkRules' 및 'DNSServers' 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="5d3f2-380">Added 'DNSEnableProxy', 'DNSRequireProxyForNetworkRules' and 'DNSServers' parameters to 'AzureFirewall'</span></span>
* <span data-ttu-id="5d3f2-381">'AzureFirewall'에 'EnableDnsProxy', 'DnsProxyNotRequiredForNetworkRule' 및 'DnsServer' 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="5d3f2-381">Added 'EnableDnsProxy', 'DnsProxyNotRequiredForNetworkRule' and 'DnsServer' parameters to 'AzureFirewall'</span></span>
    - <span data-ttu-id="5d3f2-382">업데이트된 cmdlet:</span><span class="sxs-lookup"><span data-stu-id="5d3f2-382">Updated cmdlet:</span></span>
        - <span data-ttu-id="5d3f2-383">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="5d3f2-383">New-AzFirewall</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="5d3f2-384">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="5d3f2-384">Az.OperationalInsights</span></span>
* <span data-ttu-id="5d3f2-385">새로 생성된 SDK를 적용하도록 레거시 코드 업데이트</span><span class="sxs-lookup"><span data-stu-id="5d3f2-385">Updated legacy code to apply new generated SDK</span></span>
* <span data-ttu-id="5d3f2-386">사용되지 않는 API 때문에 cmdlet 삭제</span><span class="sxs-lookup"><span data-stu-id="5d3f2-386">Deleted cmdlets due to deprecated APIs</span></span>
    - <span data-ttu-id="5d3f2-387">'Get-AzOperationalInsightsSavedSearchResult'(별칭 'Get-AzOperationalInsightsSavedSearchResults')</span><span class="sxs-lookup"><span data-stu-id="5d3f2-387">'Get-AzOperationalInsightsSavedSearchResult' (alias 'Get-AzOperationalInsightsSavedSearchResults')</span></span>
    - <span data-ttu-id="5d3f2-388">'Get-AzOperationalInsightsSearchResult'(별칭 'Get-AzOperationalInsightsSearchResults')</span><span class="sxs-lookup"><span data-stu-id="5d3f2-388">'Get-AzOperationalInsightsSearchResult' (alias 'Get-AzOperationalInsightsSearchResults')</span></span>
    - <span data-ttu-id="5d3f2-389">'Get-AzOperationalInsightsLinkTarget'(별칭 'Get-AzOperationalInsightsLinkTargets')</span><span class="sxs-lookup"><span data-stu-id="5d3f2-389">'Get-AzOperationalInsightsLinkTarget' (alias 'Get-AzOperationalInsightsLinkTargets')</span></span>
* <span data-ttu-id="5d3f2-390">'Set-AzOperationalInsightsWorkspace' 및 'New-AzOperationalInsightsWorkspace'에 대한 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="5d3f2-390">Added parameters for 'Set-AzOperationalInsightsWorkspace' and 'New-AzOperationalInsightsWorkspace'</span></span>
* <span data-ttu-id="5d3f2-391">연결된 스토리지 계정에 대한 cmdlet 작성</span><span class="sxs-lookup"><span data-stu-id="5d3f2-391">Created cmdlets for Linked Stoarge Account</span></span>
* <span data-ttu-id="5d3f2-392">클러스터 및 연결된 서비스에 대한 cmdlet 작성</span><span class="sxs-lookup"><span data-stu-id="5d3f2-392">Created cmdlets for Clusters and Linked Service</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="5d3f2-393">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="5d3f2-393">Az.RecoveryServices</span></span>
* <span data-ttu-id="5d3f2-394">Azure Site Recovery - Azure와 Azure 공급자 간 근접 배치 그룹 가상 머신을 보호하기 위한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-394">Azure Site Recovery added support for protecting proximity placement group virtual machines for Azure to Azure provider.</span></span>
* <span data-ttu-id="5d3f2-395">Azure Site Recovery - 영역 간 복제에 대한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-395">Azure Site Recovery added support for zone to zone replication.</span></span>
* <span data-ttu-id="5d3f2-396">Azure Backup - Azure 파일 공유 복구 지점의 장기 보존 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-396">Azure Backup Added Long term retention support for Azure FileShare Recovery Points.</span></span>
* <span data-ttu-id="5d3f2-397">Azure Backup - 'Get-AzRecoveryServicesBackupItem' cmdlet 출력에 디스크 제외 속성이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-397">Azure Backup Added disk exclusion properties to 'Get-AzRecoveryServicesBackupItem' cmdlet output.</span></span>
* <span data-ttu-id="5d3f2-398">사이트 복구 서비스용 Vault 자격 증명 파일에 대한 프라이빗 엔드포인트가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-398">Added private endpoint for Vault credential file for site recovery service.</span></span>

#### <a name="azresources"></a><span data-ttu-id="5d3f2-399">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="5d3f2-399">Az.Resources</span></span>
* <span data-ttu-id="5d3f2-400">새 역할 정의를 만들 때 보기 지연에 대한 메시지 경고 추가</span><span class="sxs-lookup"><span data-stu-id="5d3f2-400">Added message warning about view delay when creating a new Role Definition</span></span>
* <span data-ttu-id="5d3f2-401">강력한 형식의 개체를 출력하도록 정책 cmdlet 변경</span><span class="sxs-lookup"><span data-stu-id="5d3f2-401">Changed policy cmdlets to output strongly-typed objects</span></span>
* <span data-ttu-id="5d3f2-402">'Get-AzResourceLock' cmdlet에 사용되는 '-TenantLevel' 매개 변수 제거 [#11335]</span><span class="sxs-lookup"><span data-stu-id="5d3f2-402">Removed '-TenantLevel' parameter used for on the 'Get-AzResourceLock' cmdlet [#11335]</span></span>
* <span data-ttu-id="5d3f2-403">'Remove-AzResourceGroup -Id ResourceId' 수정[#9882]</span><span class="sxs-lookup"><span data-stu-id="5d3f2-403">Fixed 'Remove-AzResourceGroup -Id ResourceId'[#9882]</span></span>
* <span data-ttu-id="5d3f2-404">리소스 그룹 범위에서 ARM 템플릿 가상 시나리오 결과를 가져오는 새 cmdlet 추가: 'Get-AzDeploymentResourceGroupWhatIfResult'</span><span class="sxs-lookup"><span data-stu-id="5d3f2-404">Added new cmdlet for getting ARM template What-If results at resource group scope: 'Get-AzDeploymentResourceGroupWhatIfResult'</span></span>
* <span data-ttu-id="5d3f2-405">구독 범위에서 ARM 템플릿 가상 시나리오 결과를 가져오는 새 cmdlet 추가: 'Get-AzDeploymentWhatIfResult'</span><span class="sxs-lookup"><span data-stu-id="5d3f2-405">Added new cmdlet for getting ARM template What-If results at subscription scope: 'Get-AzDeploymentWhatIfResult'</span></span>
   - <span data-ttu-id="5d3f2-406">별칭: 'Get-AzSubscriptionDeploymentWhatIf'</span><span class="sxs-lookup"><span data-stu-id="5d3f2-406">Alias: 'Get-AzSubscriptionDeploymentWhatIf'</span></span>
* <span data-ttu-id="5d3f2-407">ARM 템플릿 가상 시나리오 결과를 사용하도록 'New-AzDeployment' 및 'New-AzResourceGroupDeployment'에 대한 '-WhatIf' 및 '-Confirm' 매개 변수 재정의</span><span class="sxs-lookup"><span data-stu-id="5d3f2-407">Overrode '-WhatIf' and '-Confirm' parameters for 'New-AzDeployment' and 'New-AzResourceGroupDeployment' to use ARM template What-If results</span></span>
* <span data-ttu-id="5d3f2-408">배포 cmdlet에서 'ApiVersion' 매개 변수의 사용 중단 메시지 추가</span><span class="sxs-lookup"><span data-stu-id="5d3f2-408">Added deprecation message for 'ApiVersion' parameter in deployment cmdlets</span></span>
* <span data-ttu-id="5d3f2-409">배포 오류에 대한 향상된 오류 메시지를 표시하는 기능 추가</span><span class="sxs-lookup"><span data-stu-id="5d3f2-409">Added capability to show improved error messages for deployment failures</span></span>
* <span data-ttu-id="5d3f2-410">배포 오류에 대한 correlationId 로깅 추가</span><span class="sxs-lookup"><span data-stu-id="5d3f2-410">Added correlationId logging for deployment failures</span></span>
* <span data-ttu-id="5d3f2-411">배포 스크립트 출력에 'error' 속성 추가</span><span class="sxs-lookup"><span data-stu-id="5d3f2-411">Added 'error' property to the deployment script output</span></span>
* <span data-ttu-id="5d3f2-412">nuget Microsoft.Azure.Management.ResourceManager를 '3.7.1-preview'로 업데이트</span><span class="sxs-lookup"><span data-stu-id="5d3f2-412">Updated nuget Microsoft.Azure.Management.ResourceManager to '3.7.1-preview'</span></span>
* <span data-ttu-id="5d3f2-413">nuget 3.7.1-preview에서 DeploymentValidateResult의 Error 속성이 readonly로 변경되어 특정 테스트 사례를 제거</span><span class="sxs-lookup"><span data-stu-id="5d3f2-413">Removed specific test cases as Error property in DeploymentValidateResult has changed to readonly from nuget 3.7.1-preview</span></span>
* <span data-ttu-id="5d3f2-414">SDK ResourceManager 3.7.1-preview의 GenericResourceExpanded 도입</span><span class="sxs-lookup"><span data-stu-id="5d3f2-414">Brought GenericResourceExpanded from SDK ResourceManager 3.7.1-preview</span></span>
* <span data-ttu-id="5d3f2-415">모든 배포용 Get cmdlet에 대한 태그 지원 추가</span><span class="sxs-lookup"><span data-stu-id="5d3f2-415">Added tag support for all Get cmdlets for deployment, as well as</span></span>
    - <span data-ttu-id="5d3f2-416">'New-AzDeployment'</span><span class="sxs-lookup"><span data-stu-id="5d3f2-416">'New-AzDeployment'</span></span>
    - <span data-ttu-id="5d3f2-417">'New-AzManagementGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="5d3f2-417">'New-AzManagementGroupDeployment'</span></span>
    - <span data-ttu-id="5d3f2-418">'New-AzResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="5d3f2-418">'New-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="5d3f2-419">'New-AzTenantDeployment'</span><span class="sxs-lookup"><span data-stu-id="5d3f2-419">'New-AzTenantDeployment'</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="5d3f2-420">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="5d3f2-420">Az.ServiceFabric</span></span>
* <span data-ttu-id="5d3f2-421">잘못된 인증서 지문을 가져오는 --SecretIdentifier를 사용한 인증서 추가의 버그 수정</span><span class="sxs-lookup"><span data-stu-id="5d3f2-421">Fixed bug in add certificate using --SecretIdentifier that was getting the wrong certificate thumbprint</span></span>

#### <a name="azsql"></a><span data-ttu-id="5d3f2-422">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="5d3f2-422">Az.Sql</span></span>
* <span data-ttu-id="5d3f2-423">성능 강화:</span><span class="sxs-lookup"><span data-stu-id="5d3f2-423">Enhance performance of:</span></span>
    - <span data-ttu-id="5d3f2-424">'Set-AzSqlDatabaseSensitivityClassification'</span><span class="sxs-lookup"><span data-stu-id="5d3f2-424">'Set-AzSqlDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="5d3f2-425">'Set-AzSqlInstanceDatabaseSensitivityClassification'</span><span class="sxs-lookup"><span data-stu-id="5d3f2-425">'Set-AzSqlInstanceDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="5d3f2-426">'Remove-AzSqlDatabaseSensitivityClassification'</span><span class="sxs-lookup"><span data-stu-id="5d3f2-426">'Remove-AzSqlDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="5d3f2-427">'Remove-AzSqlInstanceDatabaseSensitivityClassification'</span><span class="sxs-lookup"><span data-stu-id="5d3f2-427">'Remove-AzSqlInstanceDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="5d3f2-428">'Enable-AzSqlDatabaseSensitivityRecommendation'</span><span class="sxs-lookup"><span data-stu-id="5d3f2-428">'Enable-AzSqlDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="5d3f2-429">'Enable-AzSqlInstanceDatabaseSensitivityRecommendation'</span><span class="sxs-lookup"><span data-stu-id="5d3f2-429">'Enable-AzSqlInstanceDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="5d3f2-430">'Disable-AzSqlDatabaseSensitivityRecommendation'</span><span class="sxs-lookup"><span data-stu-id="5d3f2-430">'Disable-AzSqlDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="5d3f2-431">'Disable-AzSqlInstanceDatabaseSensitivityRecommendation'</span><span class="sxs-lookup"><span data-stu-id="5d3f2-431">'Disable-AzSqlInstanceDatabaseSensitivityRecommendation'</span></span>
* <span data-ttu-id="5d3f2-432">'Set-AzSqlDatabaseBackupShortTermRetentionPolicy' cmdlet에서 'RetentionDays' 매개 변수의 클라이언트 쪽 유효성 검사 제거</span><span class="sxs-lookup"><span data-stu-id="5d3f2-432">Removed client-side validation of 'RetentionDays' parameter from cmdlet 'Set-AzSqlDatabaseBackupShortTermRetentionPolicy'</span></span>
* <span data-ttu-id="5d3f2-433">Vnet에서 스토리지 계정을 감사하고, Storage Blob 데이터 기여자 역할을 만들 때 발생하는 버그 수정</span><span class="sxs-lookup"><span data-stu-id="5d3f2-433">Auditing to a storage account in Vnet, fixing a bug when creating a Storage Blob Data Contributor role.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="5d3f2-434">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="5d3f2-434">Az.Storage</span></span>
* <span data-ttu-id="5d3f2-435">get/list account cmdlet 'Get-AzStorageAccount'에 '-AsJob' 추가</span><span class="sxs-lookup"><span data-stu-id="5d3f2-435">Added '-AsJob' to get/list account cmdlet 'Get-AzStorageAccount'</span></span>
* <span data-ttu-id="5d3f2-436">키 자동 회전을 지원하기 위해 스토리지 계정을 KeyvaultEncryption으로 업데이트할 때 KeyVersion을 선택 사항으로 지정</span><span class="sxs-lookup"><span data-stu-id="5d3f2-436">Make KeyVersion to optional when update Storage account with KeyvaultEncryption, to support key auto-rotation</span></span>
    - <span data-ttu-id="5d3f2-437">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="5d3f2-437">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="5d3f2-438">파이프라인을 사용하여 Azure 파일 디렉터리 제거 오류 수정</span><span class="sxs-lookup"><span data-stu-id="5d3f2-438">Fixed remove Azure File Directory fail with pipeline</span></span>
    - <span data-ttu-id="5d3f2-439">'Remove-AzStorageDirectory'</span><span class="sxs-lookup"><span data-stu-id="5d3f2-439">'Remove-AzStorageDirectory'</span></span>
* <span data-ttu-id="5d3f2-440">수정 [#9880]: Swagger에 맞게 NetWorkRule DefaultAction 값 정의 변경</span><span class="sxs-lookup"><span data-stu-id="5d3f2-440">Fixed [#9880]: Change NetWorkRule DefaultAction value defination to align with swagger.</span></span>
    - <span data-ttu-id="5d3f2-441">'Update-AzStorageAccountNetworkRuleSet'</span><span class="sxs-lookup"><span data-stu-id="5d3f2-441">'Update-AzStorageAccountNetworkRuleSet'</span></span>
    - <span data-ttu-id="5d3f2-442">'Get-AzStorageAccountNetworkRuleSet'</span><span class="sxs-lookup"><span data-stu-id="5d3f2-442">'Get-AzStorageAccountNetworkRuleSet'</span></span>
* <span data-ttu-id="5d3f2-443">수정 [#11624]: 서버 오류를 방지하기 위해 NetworkRules를 추가할 때 중복 규칙 건너뛰기</span><span class="sxs-lookup"><span data-stu-id="5d3f2-443">Fixed [#11624]: Skip duplicated rules when add NetworkRules, to avoid server failure</span></span>
    - <span data-ttu-id="5d3f2-444">'Add-AzStorageAccountNetworkRule'</span><span class="sxs-lookup"><span data-stu-id="5d3f2-444">'Add-AzStorageAccountNetworkRule'</span></span>
* <span data-ttu-id="5d3f2-445">Microsoft.Azure.Cosmos.Table SDK를 1.0.7로 업그레이드</span><span class="sxs-lookup"><span data-stu-id="5d3f2-445">Upgraded Microsoft.Azure.Cosmos.Table SDK to 1.0.7</span></span>
* <span data-ttu-id="5d3f2-446">DataLake Gen2 항목 목록에 부품 항목만 반환되는 경우 ContinuationToken을 사용하여 다시 나열하라고 사용자에게 알리는 경고 메시지 추가</span><span class="sxs-lookup"><span data-stu-id="5d3f2-446">Added a warning message to remind user to list again with ContinuationToken when only part items are returned in list DataLake Gen2 Items,</span></span>
    - <span data-ttu-id="5d3f2-447">'Get-AzDataLakeGen2ChildItem'</span><span class="sxs-lookup"><span data-stu-id="5d3f2-447">'Get-AzDataLakeGen2ChildItem'</span></span>
* <span data-ttu-id="5d3f2-448">Azure Files Active Directory 도메인 서비스 인증을 사용하여 스토리지 계정을 만들거나 업데이트하는 기능 지원</span><span class="sxs-lookup"><span data-stu-id="5d3f2-448">Supported to create or update Storage account with Azure Files Active Directory Domain Service Authentication</span></span>
    -  <span data-ttu-id="5d3f2-449">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="5d3f2-449">'New-AzStorageAccount'</span></span>
    -  <span data-ttu-id="5d3f2-450">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="5d3f2-450">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="5d3f2-451">스토리지 계정의 Kerberos 키 새로 만들기 또는 나열 지원</span><span class="sxs-lookup"><span data-stu-id="5d3f2-451">Supported to new or list Kerberos keys of Storage account</span></span>
    -  <span data-ttu-id="5d3f2-452">'New-AzStorageAccountKey'</span><span class="sxs-lookup"><span data-stu-id="5d3f2-452">'New-AzStorageAccountKey'</span></span>
    -  <span data-ttu-id="5d3f2-453">'Get-AzStorageAccountKey'</span><span class="sxs-lookup"><span data-stu-id="5d3f2-453">'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="5d3f2-454">스토리지 계정 장애 조치(failover) 지원</span><span class="sxs-lookup"><span data-stu-id="5d3f2-454">Supported failover Storage account</span></span>
    - <span data-ttu-id="5d3f2-455">'Invoke-AzStorageAccountFailover'</span><span class="sxs-lookup"><span data-stu-id="5d3f2-455">'Invoke-AzStorageAccountFailover'</span></span>
* <span data-ttu-id="5d3f2-456">'Get-AzStorageBlobCopyState'의 도움말 업데이트</span><span class="sxs-lookup"><span data-stu-id="5d3f2-456">Updated help of 'Get-AzStorageBlobCopyState'</span></span>
* <span data-ttu-id="5d3f2-457">'Get-AzStorageFileCopyState' 및 'Start-AzStorageBlobCopy'의 도움말 업데이트</span><span class="sxs-lookup"><span data-stu-id="5d3f2-457">Updated help of 'Get-AzStorageFileCopyState' and 'Start-AzStorageBlobCopy'</span></span>
* <span data-ttu-id="5d3f2-458">스토리지 클라이언트 라이브러리 v12를 큐 및 파일 cmdlet에 통합</span><span class="sxs-lookup"><span data-stu-id="5d3f2-458">Integrated Storage client library v12 to Queue and File cmdlets</span></span>
* <span data-ttu-id="5d3f2-459">출력 형식을 CloudFile에서 AzureStorageFile로 변경했으며, 원래 출력은 새 출력의 자식 속성이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-459">Changed output type from CloudFile to AzureStorageFile, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="5d3f2-460">'Get-AzStorageFile'</span><span class="sxs-lookup"><span data-stu-id="5d3f2-460">'Get-AzStorageFile'</span></span>
    - <span data-ttu-id="5d3f2-461">'Remove-AzStorageFile'</span><span class="sxs-lookup"><span data-stu-id="5d3f2-461">'Remove-AzStorageFile'</span></span>
    - <span data-ttu-id="5d3f2-462">'Get-AzStorageFileContent'</span><span class="sxs-lookup"><span data-stu-id="5d3f2-462">'Get-AzStorageFileContent'</span></span>
    - <span data-ttu-id="5d3f2-463">'Set-AzStorageFileContent'</span><span class="sxs-lookup"><span data-stu-id="5d3f2-463">'Set-AzStorageFileContent'</span></span>
    - <span data-ttu-id="5d3f2-464">'Start-AzStorageFileCopy'</span><span class="sxs-lookup"><span data-stu-id="5d3f2-464">'Start-AzStorageFileCopy'</span></span>
* <span data-ttu-id="5d3f2-465">출력 형식을 CloudFileDirectory에서 AzureStorageFileDirectory로 변경했으며, 원래 출력은 새 출력의 자식 속성이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-465">Changed output type from CloudFileDirectory to AzureStorageFileDirectory, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="5d3f2-466">'New-AzStorageDirectory'</span><span class="sxs-lookup"><span data-stu-id="5d3f2-466">'New-AzStorageDirectory'</span></span>
    - <span data-ttu-id="5d3f2-467">'Remove-AzStorageDirectory'</span><span class="sxs-lookup"><span data-stu-id="5d3f2-467">'Remove-AzStorageDirectory'</span></span>
* <span data-ttu-id="5d3f2-468">출력 형식을 CloudFileShare에서 AzureStorageFileShare로 변경했으며, 원래 출력은 새 출력의 자식 속성이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-468">Changed output type from CloudFileShare to AzureStorageFileShare, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="5d3f2-469">'Get-AzStorageShare'</span><span class="sxs-lookup"><span data-stu-id="5d3f2-469">'Get-AzStorageShare'</span></span>
    - <span data-ttu-id="5d3f2-470">'New-AzStorageShare'</span><span class="sxs-lookup"><span data-stu-id="5d3f2-470">'New-AzStorageShare'</span></span>
    - <span data-ttu-id="5d3f2-471">'Remove-AzStorageShare'</span><span class="sxs-lookup"><span data-stu-id="5d3f2-471">'Remove-AzStorageShare'</span></span>
* <span data-ttu-id="5d3f2-472">출력 형식을 FileShareProperties에서 AzureStorageFileShare로 변경했으며, 원래 출력은 새 출력의 하위 자식 속성이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-472">Changed output type from FileShareProperties to AzureStorageFileShare, the original output will become a sub child property of the new output</span></span>
    - <span data-ttu-id="5d3f2-473">'Set-AzStorageShareQuota'</span><span class="sxs-lookup"><span data-stu-id="5d3f2-473">'Set-AzStorageShareQuota'</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="5d3f2-474">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="5d3f2-474">Az.TrafficManager</span></span>
* <span data-ttu-id="5d3f2-475">'DisableAzureTrafficManagerEndpoint' 자세한 정보 출력에서 잘못된 프로필 이름 수정</span><span class="sxs-lookup"><span data-stu-id="5d3f2-475">Fixed incorrect profile name in 'DisableAzureTrafficManagerEndpoint' verbose output</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="5d3f2-476">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="5d3f2-476">Az.Websites</span></span>
* <span data-ttu-id="5d3f2-477">'Update-AzWebAppAccessRestrictionConfig'의 도움말에서 철자 오류 수정</span><span class="sxs-lookup"><span data-stu-id="5d3f2-477">Fixed typo on help of 'Update-AzWebAppAccessRestrictionConfig'.</span></span>

## <a name="380---april-2020"></a><span data-ttu-id="5d3f2-478">3.8.0 - 2020년 4월</span><span class="sxs-lookup"><span data-stu-id="5d3f2-478">3.8.0 - April 2020</span></span>
### <a name="highlights-since-the-last-release"></a><span data-ttu-id="5d3f2-479">마지막 릴리스 이후의 주요 사항</span><span class="sxs-lookup"><span data-stu-id="5d3f2-479">Highlights since the last release</span></span>
* <span data-ttu-id="5d3f2-480">Az.Storage에서 지원하는 PowerShell 버전: Windows PowerShell 5.1, PowerShell Core 6.2.4 이상, PowerShell 7</span><span class="sxs-lookup"><span data-stu-id="5d3f2-480">PowerShell versions that Az.Storage supports: Windows PowerShell 5.1, PowerShell Core 6.2.4+, PowerShell 7</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="5d3f2-481">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="5d3f2-481">Az.Accounts</span></span>
* <span data-ttu-id="5d3f2-482">'Resolve-AzError'에서 Azure PowerShell 설문 조사 URL이 업데이트되었습니다. [#11507]</span><span class="sxs-lookup"><span data-stu-id="5d3f2-482">Updated Azure PowerShell survey URL in 'Resolve-AzError' [#11507]</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="5d3f2-483">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="5d3f2-483">Az.ApiManagement</span></span>
* <span data-ttu-id="5d3f2-484">향후 릴리스의 Azure File cmdlet 출력 변경에 대한 호환성이 손상되는 변경 공지가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-484">Added breaking change notice for Azure File cmdlets output change in a future release</span></span>
* <span data-ttu-id="5d3f2-485">'Set-AzApiManagementGroup' - GroupId 매개 변수를 지정하도록 설명서가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-485">'Set-AzApiManagementGroup' Updated documentation to specify the GroupId parameter</span></span>

#### <a name="azcdn"></a><span data-ttu-id="5d3f2-486">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="5d3f2-486">Az.Cdn</span></span>
* <span data-ttu-id="5d3f2-487">ChinaCDN 관련 가격 책정 SKU 표시가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-487">Fixed ChinaCDN related pricing SKU display</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="5d3f2-488">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="5d3f2-488">Az.CognitiveServices</span></span>
* <span data-ttu-id="5d3f2-489">Identity, Encryption, UserOwnedStorage가 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-489">Supported Identity, Encryption, UserOwnedStorage</span></span>

#### <a name="azcompute"></a><span data-ttu-id="5d3f2-490">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="5d3f2-490">Az.Compute</span></span>
* <span data-ttu-id="5d3f2-491">'Set-AzVmssOrchestrationServiceState' cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-491">Added 'Set-AzVmssOrchestrationServiceState' cmdlet.</span></span>
* <span data-ttu-id="5d3f2-492">-InstanceView가 있는 'Get-AzVmss'는 OrchestrationService 상태를 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-492">'Get-AzVmss' with -InstanceView shows OrchestrationService states.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="5d3f2-493">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="5d3f2-493">Az.IotHub</span></span>
* <span data-ttu-id="5d3f2-494">IoT 디바이스 쌍 구성을 관리합니다. 새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-494">Manage IoT device twin configuration, New cmdlets are:</span></span>
    - <span data-ttu-id="5d3f2-495">'Get-AzIotHubDeviceTwin'</span><span class="sxs-lookup"><span data-stu-id="5d3f2-495">'Get-AzIotHubDeviceTwin'</span></span>
    - <span data-ttu-id="5d3f2-496">'Update-AzIotHubDeviceTwin'</span><span class="sxs-lookup"><span data-stu-id="5d3f2-496">'Update-AzIotHubDeviceTwin'</span></span>
* <span data-ttu-id="5d3f2-497">IoT Hub에서 디바이스에 대한 직접 메서드를 호출하는 cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-497">Added cmdlet to invoke direct method on a device in an Iot Hub.</span></span>
* <span data-ttu-id="5d3f2-498">IoT 디바이스 모듈 쌍 구성을 관리합니다. 새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-498">Manage IoT device module twin configuration, New cmdlets are:</span></span>
    - <span data-ttu-id="5d3f2-499">'Get-AzIotHubModuleTwin'</span><span class="sxs-lookup"><span data-stu-id="5d3f2-499">'Get-AzIotHubModuleTwin'</span></span>
    - <span data-ttu-id="5d3f2-500">'Update-AzIotHubModuleTwin'</span><span class="sxs-lookup"><span data-stu-id="5d3f2-500">'Update-AzIotHubModuleTwin'</span></span>
* <span data-ttu-id="5d3f2-501">IoT 자동 디바이스 관리 구성을 대규모로 관리합니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-501">Manage IoT automatic device management configuration at scale.</span></span> <span data-ttu-id="5d3f2-502">새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-502">New cmdlets are:</span></span>
    - <span data-ttu-id="5d3f2-503">'Add-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="5d3f2-503">'Add-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="5d3f2-504">'Get-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="5d3f2-504">'Get-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="5d3f2-505">'Remove-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="5d3f2-505">'Remove-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="5d3f2-506">'Set-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="5d3f2-506">'Set-AzIotHubConfiguration'</span></span>
* <span data-ttu-id="5d3f2-507">Iot Hub에서 에지 모듈 메서드를 호출하는 cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-507">Added cmdlet to invoke an edge module method in an Iot Hub.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="5d3f2-508">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="5d3f2-508">Az.KeyVault</span></span>
* <span data-ttu-id="5d3f2-509">자격 증명 모음에서 일시 삭제 및 제거 보호를 사용하도록 설정할 수 있는 새 cmdlet 'Update-AzKeyVault'가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-509">Added a new cmdlet 'Update-AzKeyVault' that can enable soft delete and purge protection on a vault</span></span>
* <span data-ttu-id="5d3f2-510">Microsoft.PowerShell.SecretManagement에 대한 지원이 추가되었습니다. [#11178]</span><span class="sxs-lookup"><span data-stu-id="5d3f2-510">Added support to Microsoft.PowerShell.SecretManagement [#11178]</span></span>
* <span data-ttu-id="5d3f2-511">'Remove-AzKeyVaultManagedStorageSasDefinition' 예제의 오류가 해결되었습니다. [#11479]</span><span class="sxs-lookup"><span data-stu-id="5d3f2-511">Fixed error in the examples of 'Remove-AzKeyVaultManagedStorageSasDefinition' [#11479]</span></span>
* <span data-ttu-id="5d3f2-512">프라이빗 엔드포인트에 대한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-512">Added support to private endpoint</span></span>

#### <a name="azmaintenance"></a><span data-ttu-id="5d3f2-513">Az.Maintenance</span><span class="sxs-lookup"><span data-stu-id="5d3f2-513">Az.Maintenance</span></span>
* <span data-ttu-id="5d3f2-514">GA용 유지 관리 cmdlet의 릴리스 버전 게시</span><span class="sxs-lookup"><span data-stu-id="5d3f2-514">Publishing release version of Maintenance cmdlets for GA</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="5d3f2-515">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="5d3f2-515">Az.Monitor</span></span>
* <span data-ttu-id="5d3f2-516">프라이빗 링크 범위용 cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-516">Added cmdlets for private link scope</span></span>
    - <span data-ttu-id="5d3f2-517">'Get-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="5d3f2-517">'Get-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="5d3f2-518">'Remove-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="5d3f2-518">'Remove-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="5d3f2-519">'New-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="5d3f2-519">'New-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="5d3f2-520">'Update-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="5d3f2-520">'Update-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="5d3f2-521">'Get-AzInsightsPrivateLinkScopedResource'</span><span class="sxs-lookup"><span data-stu-id="5d3f2-521">'Get-AzInsightsPrivateLinkScopedResource'</span></span>
    - <span data-ttu-id="5d3f2-522">'New-AzInsightsPrivateLinkScopedResource'</span><span class="sxs-lookup"><span data-stu-id="5d3f2-522">'New-AzInsightsPrivateLinkScopedResource'</span></span>
    - <span data-ttu-id="5d3f2-523">'Remove-AzInsightsPrivateLinkScopedResource'</span><span class="sxs-lookup"><span data-stu-id="5d3f2-523">'Remove-AzInsightsPrivateLinkScopedResource'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="5d3f2-524">Az.Network</span><span class="sxs-lookup"><span data-stu-id="5d3f2-524">Az.Network</span></span>
* <span data-ttu-id="5d3f2-525">Virtual Network 게이트웨이의 개인 IP에 대한 연결을 사용하도록 설정하는 cmdlet이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-525">Updated cmdlets to enable connection on private IP for Virtual Network Gateway.</span></span>
    - <span data-ttu-id="5d3f2-526">'New-AzVirtualNetworkGateway'</span><span class="sxs-lookup"><span data-stu-id="5d3f2-526">'New-AzVirtualNetworkGateway'</span></span>
    - <span data-ttu-id="5d3f2-527">'Set-AzVirtualNetworkGateway'</span><span class="sxs-lookup"><span data-stu-id="5d3f2-527">'Set-AzVirtualNetworkGateway'</span></span>
    - <span data-ttu-id="5d3f2-528">'New-AzVirtualNetworkGatewayConnection'</span><span class="sxs-lookup"><span data-stu-id="5d3f2-528">'New-AzVirtualNetworkGatewayConnection'</span></span>
    - <span data-ttu-id="5d3f2-529">'Set-AzVirtualNetworkGatewayConnection'</span><span class="sxs-lookup"><span data-stu-id="5d3f2-529">'Set-AzVirtualNetworkGatewayConnection'</span></span>
* <span data-ttu-id="5d3f2-530">FQDN 기반 LocalNetworkGateways 및 VpnSites를 사용하도록 설정하는 cmdlet이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-530">Updated cmdlets to enable FQDN based LocalNetworkGateways and VpnSites</span></span>
    - <span data-ttu-id="5d3f2-531">'New-AzLocalNetworkGateway'</span><span class="sxs-lookup"><span data-stu-id="5d3f2-531">'New-AzLocalNetworkGateway'</span></span>
    - <span data-ttu-id="5d3f2-532">'New-AzVpnSiteLink'</span><span class="sxs-lookup"><span data-stu-id="5d3f2-532">'New-AzVpnSiteLink'</span></span>
* <span data-ttu-id="5d3f2-533">ExpressRouteCircuitConnectionConfig(Global Reach)의 IPv6 주소 패밀리에 대한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-533">Added support for IPv6 address family in ExpressRouteCircuitConnectionConfig (Global Reach)</span></span>
    - <span data-ttu-id="5d3f2-534">'Set-AzExpressRouteCircuitConnectionConfig'가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-534">Added 'Set-AzExpressRouteCircuitConnectionConfig'</span></span>
        - <span data-ttu-id="5d3f2-535">IPv6CircuitConnectionProperties를 포함한 모든 기존 속성을 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-535">allows setting of all the existing properties including the IPv6CircuitConnectionProperties</span></span>
    - <span data-ttu-id="5d3f2-536">'Add-AzExpressRouteCircuitConnectionConfig'가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-536">Updated 'Add-AzExpressRouteCircuitConnectionConfig'</span></span>
        - <span data-ttu-id="5d3f2-537">주소 접두사의 주소 패밀리를 지정하는 또 다른 선택적 매개 변수 AddressPrefixType이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-537">Added another optional parameter AddressPrefixType to specify the address family of address prefix</span></span>
* <span data-ttu-id="5d3f2-538">Virtual Network 게이트웨이 연결에서 DPD 시간 제한 설정을 사용하도록 cmdlet이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-538">Updated cmdlets to enable setting of DPD Timeout on Virtual Network Gateway Connections.</span></span>
    - <span data-ttu-id="5d3f2-539">New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="5d3f2-539">New-AzVirtualNetworkGatewayConnection</span></span>
    - <span data-ttu-id="5d3f2-540">Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="5d3f2-540">Set-AzVirtualNetworkGatewayConnection</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="5d3f2-541">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="5d3f2-541">Az.PolicyInsights</span></span>
* <span data-ttu-id="5d3f2-542">정책 준수 검사를 트리거하기 위한 'Start-AzPolicyComplianceScan' cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-542">Added 'Start-AzPolicyComplianceScan' cmdlet for triggering policy compliance scans</span></span>
* <span data-ttu-id="5d3f2-543">'Get-AzPolicyState' 출력에 정책 정의, 집합 정의 및 할당 버전이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-543">Added policy definition, set definition, and assignment versions to 'Get-AzPolicyState' output</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="5d3f2-544">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="5d3f2-544">Az.ServiceFabric</span></span>
* <span data-ttu-id="5d3f2-545">'New-AzServiceFabricCluster' 예제의 코드 서식 및 사용 편의성이 개선되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-545">Improved code formatting and usability of 'New-AzServiceFabricCluster' examples</span></span>

#### <a name="azsql"></a><span data-ttu-id="5d3f2-546">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="5d3f2-546">Az.Sql</span></span>
* <span data-ttu-id="5d3f2-547">'Get-AzSqlInstanceOperation' 및 'Stop-AzSqlInstanceOperation' cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-547">Added cmdlets 'Get-AzSqlInstanceOperation' and 'Stop-AzSqlInstanceOperation'</span></span>
* <span data-ttu-id="5d3f2-548">VNet에서 스토리지 계정에 대한 감사가 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-548">Supported auditing to a storage account in VNet.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="5d3f2-549">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="5d3f2-549">Az.Storage</span></span>
* <span data-ttu-id="5d3f2-550">향후 릴리스의 Azure File cmdlet 출력 변경에 대한 호환성이 손상되는 변경 공지가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-550">Added breaking change notice for Azure File cmdlets output change in a future release</span></span>
* <span data-ttu-id="5d3f2-551">스토리지 계정 생성/업데이트 시 새로운 SkuName StandardGZRS, StandardRAGZRS가 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-551">Supported new SkuName StandardGZRS, StandardRAGZRS when create/update Storage account</span></span>
    - <span data-ttu-id="5d3f2-552">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="5d3f2-552">'New-AzStorageAccount'</span></span>
    - <span data-ttu-id="5d3f2-553">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="5d3f2-553">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="5d3f2-554">DataLake Gen2가 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-554">Supported DataLake Gen2</span></span>
    - <span data-ttu-id="5d3f2-555">'New-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="5d3f2-555">'New-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="5d3f2-556">'Get-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="5d3f2-556">'Get-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="5d3f2-557">'Get-AzDataLakeGen2ChildItem'</span><span class="sxs-lookup"><span data-stu-id="5d3f2-557">'Get-AzDataLakeGen2ChildItem'</span></span>
    - <span data-ttu-id="5d3f2-558">'Move-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="5d3f2-558">'Move-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="5d3f2-559">'Set-AzDataLakeGen2ItemAclObject'</span><span class="sxs-lookup"><span data-stu-id="5d3f2-559">'Set-AzDataLakeGen2ItemAclObject'</span></span>
    - <span data-ttu-id="5d3f2-560">'Update-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="5d3f2-560">'Update-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="5d3f2-561">'Get-AzDataLakeGen2ItemContent'</span><span class="sxs-lookup"><span data-stu-id="5d3f2-561">'Get-AzDataLakeGen2ItemContent'</span></span>
    - <span data-ttu-id="5d3f2-562">'Remove-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="5d3f2-562">'Remove-AzDataLakeGen2Item'</span></span>

## <a name="0100-preview---april-2020"></a><span data-ttu-id="5d3f2-563">0.10.0-preview - 2020년 4월</span><span class="sxs-lookup"><span data-stu-id="5d3f2-563">0.10.0-preview - April 2020</span></span>
### <a name="general"></a><span data-ttu-id="5d3f2-564">일반</span><span class="sxs-lookup"><span data-stu-id="5d3f2-564">General</span></span>
* <span data-ttu-id="5d3f2-565">이제 Az 모듈이 Azure Stack Hub에서 미리 보기로 제공됩니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-565">Az modules is now available in preview on Azure Stack Hub.</span></span> <span data-ttu-id="5d3f2-566">따라서 Linux 및 macOS와의 플랫폼 간 호환성이 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-566">This allows for cross-platform compatibility with Linux and macOs.</span></span> <span data-ttu-id="5d3f2-567">Azure Stack Hub는 이제 Az 모듈을 사용하여 PowerShell Core를 지원합니다. 자세한 내용은 [여기](https://aka.ms/az4AzureStack)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-567">Azure Stack Hub now supports PowerShell core with the Az modules, more information [here](https://aka.ms/az4AzureStack)</span></span>
* <span data-ttu-id="5d3f2-568">Az 모듈은 2019-03-01-hybrid 프로필을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-568">Az modules support profile 2019-03-01-hybrid:</span></span>
  - <span data-ttu-id="5d3f2-569">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="5d3f2-569">Az.Billing</span></span>
  - <span data-ttu-id="5d3f2-570">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="5d3f2-570">Az.Compute</span></span>
  - <span data-ttu-id="5d3f2-571">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="5d3f2-571">Az.DataBoxEdge</span></span>
  - <span data-ttu-id="5d3f2-572">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="5d3f2-572">Az.EventHub</span></span>
  - <span data-ttu-id="5d3f2-573">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="5d3f2-573">Az.IotHub</span></span>
  - <span data-ttu-id="5d3f2-574">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="5d3f2-574">Az.KeyVault</span></span>
  - <span data-ttu-id="5d3f2-575">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="5d3f2-575">Az.Monitor</span></span>
  - <span data-ttu-id="5d3f2-576">Az.Network</span><span class="sxs-lookup"><span data-stu-id="5d3f2-576">Az.Network</span></span>
  - <span data-ttu-id="5d3f2-577">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="5d3f2-577">Az.Resources</span></span>
  - <span data-ttu-id="5d3f2-578">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="5d3f2-578">Az.Storage</span></span>
  - <span data-ttu-id="5d3f2-579">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="5d3f2-579">Az.Websites</span></span>
* <span data-ttu-id="5d3f2-580">Azure Stack Hub와 함께 작동하는 az용 새 PowerShell 모듈 3개(Az.Databox, Az.IotHub 및 Az.EventHub)가 도입되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-580">Three new PowerShell modules for az have been introduced that work with Azure Stack Hub, which are Az.Databox, Az.IotHub, and Az.EventHub</span></span>
* <span data-ttu-id="5d3f2-581">AzureRM을 Az로 변경하는 것과 같은 사소한 변경을 수행하면 명령이 비교적 동일하게 유지됩니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-581">Commands remain relatively the same, with minor changes such as changing AzureRM to Az</span></span>
* <span data-ttu-id="5d3f2-582">Azure Stack Hub에 대한 PowerShell 설명서의 업데이트된 링크는 [여기](https://aka.ms/InstallASHPowerShell)에서 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-582">Updated link to PowerShell documentation for Azure Stack Hub can be found [here](https://aka.ms/InstallASHPowerShell)</span></span>

## <a name="370---march-2020"></a><span data-ttu-id="5d3f2-583">3.7.0 - 2020년 3월</span><span class="sxs-lookup"><span data-stu-id="5d3f2-583">3.7.0 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="5d3f2-584">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="5d3f2-584">Az.Accounts</span></span>
* <span data-ttu-id="5d3f2-585">로그인하지 않을 때 'Get-AzTenant'/'Get-AzDefault'/'Set-AzDefault'에서 NullReferenceException이 발생하는 문제가 해결되었습니다. [# 10292]</span><span class="sxs-lookup"><span data-stu-id="5d3f2-585">Fixed 'Get-AzTenant'/'Get-AzDefault'/'Set-AzDefault' throw NullReferenceException when not login [#10292]</span></span>

#### <a name="azcompute"></a><span data-ttu-id="5d3f2-586">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="5d3f2-586">Az.Compute</span></span>
* <span data-ttu-id="5d3f2-587">'New-AzDiskConfig' cmdlet에 다음 매개 변수를 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-587">Added the following parameters to 'New-AzDiskConfig' cmdlet:</span></span>
    - <span data-ttu-id="5d3f2-588">DiskIOPSReadOnly, DiskMBpsReadOnly, MaxSharesCount, GalleryImageReference</span><span class="sxs-lookup"><span data-stu-id="5d3f2-588">DiskIOPSReadOnly, DiskMBpsReadOnly, MaxSharesCount, GalleryImageReference</span></span>
* <span data-ttu-id="5d3f2-589">암호화 속성이 'New-AzGalleryImageVersion'cmdlet의 대상 매개 변수에 허용되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-589">Allowed Encryption property to Target parameter of 'New-AzGalleryImageVersion' cmdlet.</span></span>
* <span data-ttu-id="5d3f2-590">'Set-AzVmss'-Reimage 및 'Invoke-AzVMReimage'cmdlet에 대한 tempDisk 이슈가 해결되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-590">Fixed tempDisk issue for 'Set-AzVmss' -Reimage and 'Invoke-AzVMReimage' cmdlets.</span></span> <span data-ttu-id="5d3f2-591">[#11354]</span><span class="sxs-lookup"><span data-stu-id="5d3f2-591">[#11354]</span></span>
* <span data-ttu-id="5d3f2-592">새로운 SAP 확장을 위해 아래 cmdlet에 대한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-592">Added support to below cmdlets for new SAP Extension</span></span>
    - <span data-ttu-id="5d3f2-593">'Set-AzVMAEMExtension'</span><span class="sxs-lookup"><span data-stu-id="5d3f2-593">'Set-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="5d3f2-594">'Get-AzVMAEMExtension'</span><span class="sxs-lookup"><span data-stu-id="5d3f2-594">'Get-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="5d3f2-595">'Remove-AzVMAEMExtension'</span><span class="sxs-lookup"><span data-stu-id="5d3f2-595">'Remove-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="5d3f2-596">'Update-AzVMAEMExtension'</span><span class="sxs-lookup"><span data-stu-id="5d3f2-596">'Update-AzVMAEMExtension'</span></span>
* <span data-ttu-id="5d3f2-597">도움말 문서의 예제에서 오류가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-597">Fixed errors in examples of help document</span></span>
* <span data-ttu-id="5d3f2-598">VM PowerState의 정확한 문자열 값을 테이블 형식으로 표시했습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-598">Showed the exact string value for VM PowerState in the table format.</span></span>
* <span data-ttu-id="5d3f2-599">'New-AzVmssConfig': SinglePlacementGroup이 비활성화된 경우 AutomaticRepairs 속성의 직렬화가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-599">'New-AzVmssConfig': fixed serialization of AutomaticRepairs property when SinglePlacementGroup is disabled.</span></span> <span data-ttu-id="5d3f2-600">[#11257]</span><span class="sxs-lookup"><span data-stu-id="5d3f2-600">[#11257]</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="5d3f2-601">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="5d3f2-601">Az.DataFactory</span></span>
* <span data-ttu-id="5d3f2-602">ADF .Net SDK 버전이 4.8.0으로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-602">Updated ADF .Net SDK version to 4.8.0</span></span>
* <span data-ttu-id="5d3f2-603">재실행을 지원하기 위해 'Invoke-AzDataFactoryV2Pipeline' 명령에 선택적 매개 변수를 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-603">Added optional parameters to 'Invoke-AzDataFactoryV2Pipeline' command to support rerun</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="5d3f2-604">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="5d3f2-604">Az.DataLakeStore</span></span>
* <span data-ttu-id="5d3f2-605">'Export-AzDataLakeStoreItem' 및 'Import-AzDataLakeStoreItem'에 대해 호환성이 손상되는 변경 설명을 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-605">Added breaking change description for 'Export-AzDataLakeStoreItem' and 'Import-AzDataLakeStoreItem'</span></span>
* <span data-ttu-id="5d3f2-606">'New-AzDataLakeStoreItem', 'Add-AzDAtaLakeStoreItemContent' 및 'Get-AzDAtaLakeStoreItemContent'에 대한 바이트 인코딩 옵션이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-606">Added option of Byte encoding for 'New-AzDataLakeStoreItem', 'Add-AzDAtaLakeStoreItemContent', and 'Get-AzDAtaLakeStoreItemContent'</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="5d3f2-607">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="5d3f2-607">Az.HDInsight</span></span>
* <span data-ttu-id="5d3f2-608">클러스터 생성 시 최소 지원 TLS 버전 지정이 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-608">Supported specifying minimal supported TLS version when creating cluster.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="5d3f2-609">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="5d3f2-609">Az.IotHub</span></span>
* <span data-ttu-id="5d3f2-610">디바이스별 분산 설정을 관리하기 위한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-610">Added support to manage distributed settings per-device.</span></span> <span data-ttu-id="5d3f2-611">새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-611">New Cmdlets are:</span></span>
    - <span data-ttu-id="5d3f2-612">'Get-AzIotHubDistributedTracing'</span><span class="sxs-lookup"><span data-stu-id="5d3f2-612">'Get-AzIotHubDistributedTracing'</span></span>
    - <span data-ttu-id="5d3f2-613">'Set-AzIotHubDistributedTracing'</span><span class="sxs-lookup"><span data-stu-id="5d3f2-613">'Set-AzIotHubDistributedTracing'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="5d3f2-614">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="5d3f2-614">Az.KeyVault</span></span>
* <span data-ttu-id="5d3f2-615">'New-AzKeyVault'에 대해 호환성이 손상되는 변경 속성이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-615">Added breaking change attributes to 'New-AzKeyVault'</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="5d3f2-616">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="5d3f2-616">Az.Monitor</span></span>
* <span data-ttu-id="5d3f2-617">'New-AzScheduledQueryRuleLogMetricTrigger'에 대한 설명서가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-617">Updated documentation for 'New-AzScheduledQueryRuleLogMetricTrigger'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="5d3f2-618">Az.Network</span><span class="sxs-lookup"><span data-stu-id="5d3f2-618">Az.Network</span></span>
* <span data-ttu-id="5d3f2-619">교차 테넌트 VirtualHubVnetConnections를 허용하도록 cmdlet이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-619">Updated cmdlets to allow cross-tenant VirtualHubVnetConnections</span></span>
    - <span data-ttu-id="5d3f2-620">'New-AzVirtualHubVnetConnection'</span><span class="sxs-lookup"><span data-stu-id="5d3f2-620">'New-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="5d3f2-621">'Update-AzVirtualHubVnetConnection'</span><span class="sxs-lookup"><span data-stu-id="5d3f2-621">'Update-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="5d3f2-622">'New-AzVirtualHub'</span><span class="sxs-lookup"><span data-stu-id="5d3f2-622">'New-AzVirtualHub'</span></span>
    - <span data-ttu-id="5d3f2-623">'Update-AzVirtualHub'</span><span class="sxs-lookup"><span data-stu-id="5d3f2-623">'Update-AzVirtualHub'</span></span>
* <span data-ttu-id="5d3f2-624">SQL Management SDK 종속성이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-624">Removed Sql Management SDK dependency</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="5d3f2-625">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="5d3f2-625">Az.PolicyInsights</span></span>
* <span data-ttu-id="5d3f2-626">오류 메시지가 향상되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-626">Improved error messages</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="5d3f2-627">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="5d3f2-627">Az.RecoveryServices</span></span>
* <span data-ttu-id="5d3f2-628">Azure Site Recovery는 Azure 디스크 암호화 Virtual Machines에 대한 VM 속성을 다시 보호하고 업데이트하는 기능을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-628">Azure Site Recovery added support for doing reprotect and updated vm properties for Azure disk encrypted Virtual Machines.</span></span>
* <span data-ttu-id="5d3f2-629">Azure Site Recovery VmwareToAzure 속성 DR 모니터링이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-629">Added Azure Site Recovery VmwareToAzure properties DR monitoring</span></span>
* <span data-ttu-id="5d3f2-630">Azure Backup은 실패한 항목에 대한 정책 업데이트 재시도 지원을 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-630">Azure Backup added support for retrying policy update for failed items.</span></span>
* <span data-ttu-id="5d3f2-631">Azure Backup은 백업 및 복원 중에 디스크 제외 설정에 대한 지원을 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-631">Azure Backup Added support for disk exclusion settings during backup and restore.</span></span>
* <span data-ttu-id="5d3f2-632">Azure Backup은 AzureFileShare에서 여러 파일/폴더 복원을 위한 지원을 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-632">Azure Backup Added Support for Restoring Multiple files/folders in AzureFileShare</span></span>
* <span data-ttu-id="5d3f2-633">Azure Backup은 IaasVM 정책을 업데이트하는 동안 사용자 지정 리소스 그룹 지원에 대한 지원을 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-633">Azure Backup Added support for User-specified Resourcegroup support while updating IaasVM Policy</span></span>

#### <a name="azresources"></a><span data-ttu-id="5d3f2-634">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="5d3f2-634">Az.Resources</span></span>
* <span data-ttu-id="5d3f2-635">'Get-AzResource -ResourceGroupName -Name -ExpandProperties -ResourceType'이 기본 apiVersion 대신 실제 apiVersion 리소스를 사용하도록 수정했습니다. [# 11267]</span><span class="sxs-lookup"><span data-stu-id="5d3f2-635">Fixed 'Get-AzResource -ResourceGroupName -Name -ExpandProperties -ResourceType' to use actual apiVersion of resources instead of default apiVersion [#11267]</span></span>
* <span data-ttu-id="5d3f2-636">오류 시나리오에 대해 correlationId 로깅이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-636">Added correlationId logging for error scenarios</span></span>
* <span data-ttu-id="5d3f2-637">작은 설명서가 'Get-AzResourceLock'으로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-637">Small documentation change to 'Get-AzResourceLock'.</span></span> <span data-ttu-id="5d3f2-638">예제가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-638">Added example.</span></span>
* <span data-ttu-id="5d3f2-639">'Get-AzADUser'의 매개 변수 값에서 작은 따옴표를 이스케이프 처리하였습니다. [# 11317]</span><span class="sxs-lookup"><span data-stu-id="5d3f2-639">Escaped single quote in parameter value of 'Get-AzADUser' [#11317]</span></span>
* <span data-ttu-id="5d3f2-640">배포 스크립트('Get-AzDeploymentScript', 'Get-AzDeploymentScriptLog', 'Save-AzDeploymentScriptLog', 'Remove-AzDeploymentScript')에 대한 새로운 cmdlet 추가가 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-640">Added new cmdlets for Deployment Scripts ('Get-AzDeploymentScript', 'Get-AzDeploymentScriptLog', 'Save-AzDeploymentScriptLog', 'Remove-AzDeploymentScript')</span></span>

#### <a name="azsql"></a><span data-ttu-id="5d3f2-641">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="5d3f2-641">Az.Sql</span></span>
* <span data-ttu-id="5d3f2-642">'Invoke-AzSqlDatabaseFailover'에 읽기 가능한 보조 매개 변수를 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-642">Added readable secondary parameter to 'Invoke-AzSqlDatabaseFailover'</span></span>
* <span data-ttu-id="5d3f2-643">'Disable-AzSqlServerActiveDirectoryOnlyAuthentication' cmdlet을 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-643">Added cmdlet 'Disable-AzSqlServerActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="5d3f2-644">데이터베이스에서 열을 분류할 때 저장된 민감도 순위입니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-644">Saved sensitivity rank when classifying columns in the database.</span></span>

#### <a name="azsupport"></a><span data-ttu-id="5d3f2-645">Az.Support</span><span class="sxs-lookup"><span data-stu-id="5d3f2-645">Az.Support</span></span>
* <span data-ttu-id="5d3f2-646">'Az.Support' 모듈의 일반 공급</span><span class="sxs-lookup"><span data-stu-id="5d3f2-646">General availability of 'Az.Support' module</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="5d3f2-647">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="5d3f2-647">Az.Websites</span></span>
* <span data-ttu-id="5d3f2-648">아래의 새로운 cmdlet을 통해 webapp 트래픽 라우팅 규칙을 사용하는 작업에 대한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-648">Added support for working with webapp Traffic Routing Rules via below new cmdlets</span></span>
    - <span data-ttu-id="5d3f2-649">'Get-AzWebAppTrafficRouting'</span><span class="sxs-lookup"><span data-stu-id="5d3f2-649">'Get-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="5d3f2-650">'Update-AzWebAppTrafficRouting'</span><span class="sxs-lookup"><span data-stu-id="5d3f2-650">'Update-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="5d3f2-651">'Add-AzWebAppTrafficRouting'</span><span class="sxs-lookup"><span data-stu-id="5d3f2-651">'Add-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="5d3f2-652">'Remove-AzWebAppTrafficRouting'</span><span class="sxs-lookup"><span data-stu-id="5d3f2-652">'Remove-AzWebAppTrafficRouting'</span></span>

## <a name="361---march-2020"></a><span data-ttu-id="5d3f2-653">3.6.1 - 2020년 3월</span><span class="sxs-lookup"><span data-stu-id="5d3f2-653">3.6.1 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="5d3f2-654">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="5d3f2-654">Az.Accounts</span></span>
* <span data-ttu-id="5d3f2-655">'피드백 보내기'에서 Azure PowerShell 설문 조사 페이지가 열립니다[#11020].</span><span class="sxs-lookup"><span data-stu-id="5d3f2-655">Open Azure PowerShell survey page in 'Send-Feedback' [#11020]</span></span>
* <span data-ttu-id="5d3f2-656">'오류 해결'에서 Azure PowerShell 설문 조사 URL이 표시됩니다[#11021].</span><span class="sxs-lookup"><span data-stu-id="5d3f2-656">Display Azure PowerShell survey URL in 'Resolve-Error' [#11021]</span></span>
* <span data-ttu-id="5d3f2-657">UserAgent에서 Az 버전이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-657">Added Az version in UserAgent</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="5d3f2-658">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="5d3f2-658">Az.ApiManagement</span></span>
* <span data-ttu-id="5d3f2-659">DeveloperPortal 엔드포인트에서 사용자 지정 도메인을 검색하고 구성하기 위한 지원이 추가되었습니다[#11007].</span><span class="sxs-lookup"><span data-stu-id="5d3f2-659">Added support for retrieving and configuring Custom Domain on the DeveloperPortal Endpoint [#11007]</span></span>
* <span data-ttu-id="5d3f2-660">Json 형식의 API 정의를 다운로드하기 위한 'Export-AzApiManagementApi' 지원이 추가되었습니다[#9987].</span><span class="sxs-lookup"><span data-stu-id="5d3f2-660">'Export-AzApiManagementApi' Added support for downloading Api Definition in Json format [#9987]</span></span>
* <span data-ttu-id="5d3f2-661">Json 문서에서 OpenApi 3.0 정의를 가져오기 위한 'Import-AzApiManagementApi' 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-661">'Import-AzApiManagementApi' Added support for importing OpenApi 3.0 definition from Json document</span></span>
* <span data-ttu-id="5d3f2-662">AAD B2C 공급자에 대한 '로그인 테넌트'를 구성하기 위한 'New-AzApiManagementIdentityProvider' 및 'Set-AzApiManagementIdentityProvider' 지원이 추가되었습니다[#9784].</span><span class="sxs-lookup"><span data-stu-id="5d3f2-662">'New-AzApiManagementIdentityProvider' and 'Set-AzApiManagementIdentityProvider' Added support for configuring 'Signin Tenant' for AAD B2C Provider [#9784]</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="5d3f2-663">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="5d3f2-663">Az.DataLakeStore</span></span>
* <span data-ttu-id="5d3f2-664">csproj 및 psd1에서 System.Buffers에 대한 참조가 명시적으로 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-664">Added reference to System.Buffers explicitly in csproj and psd1.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="5d3f2-665">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="5d3f2-665">Az.IotHub</span></span>
* <span data-ttu-id="5d3f2-666">Iot Hub에서 디바이스를 관리하기 위한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-666">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="5d3f2-667">새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-667">New Cmdlets are:</span></span>
    - <span data-ttu-id="5d3f2-668">'Add-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="5d3f2-668">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="5d3f2-669">'Get-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="5d3f2-669">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="5d3f2-670">'Remove-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="5d3f2-670">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="5d3f2-671">'Set-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="5d3f2-671">'Set-AzIotHubDevice'</span></span>
* <span data-ttu-id="5d3f2-672">Iot Hub의 대상 IoT 디바이스에서 모듈을 관리하기 위한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-672">Added support to manage modules on a target Iot device in an Iot Hub.</span></span> <span data-ttu-id="5d3f2-673">새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-673">New Cmdlets are:</span></span>
    - <span data-ttu-id="5d3f2-674">'Add-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="5d3f2-674">'Add-AzIotHubModule'</span></span>
    - <span data-ttu-id="5d3f2-675">'Get-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="5d3f2-675">'Get-AzIotHubModule'</span></span>
    - <span data-ttu-id="5d3f2-676">'Remove-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="5d3f2-676">'Remove-AzIotHubModule'</span></span>
    - <span data-ttu-id="5d3f2-677">'Set-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="5d3f2-677">'Set-AzIotHubModule'</span></span>
* <span data-ttu-id="5d3f2-678">Iot Hub에서 대상 IoT 디바이스에 대한 연결 문자열을 가져오는 cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-678">Added cmdlet to get the connection string of a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="5d3f2-679">Iot Hub에서 대상 IoT 디바이스의 모듈에 대한 연결 문자열을 가져오는 cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-679">Added cmdlet to get the connection string of a module on a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="5d3f2-680">IoT 디바이스의 부모 디바이스를 가져오거나 설정하기 위한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-680">Added support to get/set parent device of an IoT device.</span></span> <span data-ttu-id="5d3f2-681">새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-681">New Cmdlets are:</span></span>
    - <span data-ttu-id="5d3f2-682">'Get-AzIotHubDeviceParent'</span><span class="sxs-lookup"><span data-stu-id="5d3f2-682">'Get-AzIotHubDeviceParent'</span></span>
    - <span data-ttu-id="5d3f2-683">'Set-AzIotHubDeviceParent'</span><span class="sxs-lookup"><span data-stu-id="5d3f2-683">'Set-AzIotHubDeviceParent'</span></span>
* <span data-ttu-id="5d3f2-684">디바이스 부모-자식 관계를 관리하기 위한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-684">Added support to manage device parent-child relationship.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="5d3f2-685">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="5d3f2-685">Az.Monitor</span></span>
* <span data-ttu-id="5d3f2-686">'Get-AzMetricDefinition'에 대한 출력 값이 수정되었습니다[#9714].</span><span class="sxs-lookup"><span data-stu-id="5d3f2-686">Fixed output value for 'Get-AzMetricDefinition' [#9714]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="5d3f2-687">Az.Network</span><span class="sxs-lookup"><span data-stu-id="5d3f2-687">Az.Network</span></span>
* <span data-ttu-id="5d3f2-688">SQL Management SDK가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-688">Updated Sql Management SDK.</span></span>
* <span data-ttu-id="5d3f2-689">PrivateLinkServiceConnectionState 클래스의 명명 차이 문제가 해결되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-689">Fixed a naming-difference issue in PrivateLinkServiceConnectionState class.</span></span>
    - <span data-ttu-id="5d3f2-690">ActionsRequired 필드가 ActionRequired에 매핑됩니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-690">Mapping the field ActionsRequired to ActionRequired.</span></span>
* <span data-ttu-id="5d3f2-691">PublicNetworkAccess가 'New-AzSqlServer' 및 'Set-AzSqlServer'에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-691">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>

#### <a name="azresources"></a><span data-ttu-id="5d3f2-692">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="5d3f2-692">Az.Resources</span></span>
* <span data-ttu-id="5d3f2-693">Get-AzRoleAssignment'의 null 참조 버그가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-693">Fixed for null reference bug in 'Get-AzRoleAssignment'</span></span>
* <span data-ttu-id="5d3f2-694">'Remove-AzADGroup'에서 '-Force' 및 '-PassThru' 스위치가 선택적으로 표시됩니다[#10849].</span><span class="sxs-lookup"><span data-stu-id="5d3f2-694">Marked switch '-Force' and '-PassThru' optional in 'Remove-AzADGroup' [#10849]</span></span>
* <span data-ttu-id="5d3f2-695">'Remove-AzADGroup'에서 'MailNickname'이 반환되지 않는 문제가 해결되었습니다[#11167].</span><span class="sxs-lookup"><span data-stu-id="5d3f2-695">Fixed issue that 'MailNickname' doesn't return in 'Remove-AzADGroup' [#11167]</span></span>
* <span data-ttu-id="5d3f2-696">'Remove-AzADGroup' 파이프 작업이 작동하지 않는 문제가 해결되었습니다[#11171].</span><span class="sxs-lookup"><span data-stu-id="5d3f2-696">Fixed issue that 'Remove-AzADGroup' pipe operation doesn't work [#11171]</span></span>
* <span data-ttu-id="5d3f2-697">GetAzureRoleAssignmentCommand의 null 참조 버그가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-697">Fixed for null reference bug in GetAzureRoleAssignmentCommand</span></span>
* <span data-ttu-id="5d3f2-698">예정된 정책 cmdlet 변경에 대한 호환성이 손상되는 변경 특성이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-698">Added breaking change attributes for upcoming changes to policy cmdlets</span></span>
* <span data-ttu-id="5d3f2-699">서버 쪽에서 리소스 그룹 태그 필터링을 수행하도록 'Get-AzResourceGroup'이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-699">Updated 'Get-AzResourceGroup' to perform resource group tag filtering on server-side</span></span>
* <span data-ttu-id="5d3f2-700">-ResourceId를 허용하도록 Tag cmdlet이 확장되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-700">Extended Tag cmdlets to accept -ResourceId</span></span>
    - <span data-ttu-id="5d3f2-701">Get-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="5d3f2-701">Get-AzTag -ResourceId</span></span>
    - <span data-ttu-id="5d3f2-702">New-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="5d3f2-702">New-AzTag -ResourceId</span></span>
    - <span data-ttu-id="5d3f2-703">Remove-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="5d3f2-703">Remove-AzTag -ResourceId</span></span>
* <span data-ttu-id="5d3f2-704">새 Tag cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-704">Added new Tag cmdlet</span></span>
    - <span data-ttu-id="5d3f2-705">Update-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="5d3f2-705">Update-AzTag -ResourceId</span></span>
* <span data-ttu-id="5d3f2-706">SDK 3.3.0에서 ScopedDeployment를 가져왔습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-706">Brought ScopedDeployment from SDK 3.3.0</span></span>

#### <a name="azsql"></a><span data-ttu-id="5d3f2-707">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="5d3f2-707">Az.Sql</span></span>
* <span data-ttu-id="5d3f2-708">PublicNetworkAccess가 'New-AzSqlServer' 및 'Set-AzSqlServer'에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-708">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>
* <span data-ttu-id="5d3f2-709">관리형 데이터베이스에 대한 장기 보존 백업 구성에 대한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-709">Added support for Long Term Retention backup configuration for Managed Databases</span></span>
    - <span data-ttu-id="5d3f2-710">관리형 데이터베이스에서 LTR 정책을 가져오거나 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-710">Get/Set LTR policy on a managed database</span></span>
    - <span data-ttu-id="5d3f2-711">관리형 데이터베이스, 관리형 인스턴스 또는 위치를 기준으로 LTR 백업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-711">Get LTR backup(s) by managed database, managed instance, or by location</span></span>
    - <span data-ttu-id="5d3f2-712">LTR 백업을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-712">Remove an LTR backup</span></span>
    - <span data-ttu-id="5d3f2-713">LTR 백업을 복원하여 새 관리형 데이터베이스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-713">Restore an LTR backup to create a new managed database</span></span>
* <span data-ttu-id="5d3f2-714">MinimalTlsVersion이 New-AzSqlServer 및 Set-AzSqlServer에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-714">Added MinimalTlsVersion to New-AzSqlServer and Set-AzSqlServer</span></span>
* <span data-ttu-id="5d3f2-715">MinimalTlsVersion을 New-AzSqlInstance 및 Set-AzSqlInstance에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-715">Added MinimalTlsVersion to New-AzSqlInstance and Set-AzSqlInstance</span></span>
* <span data-ttu-id="5d3f2-716">Az.Network에 대한 SQL SDK 버전이 높아졌습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-716">Bumped SQL SDK version for Az.Network</span></span>

#### <a name="azstorage"></a><span data-ttu-id="5d3f2-717">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="5d3f2-717">Az.Storage</span></span>
* <span data-ttu-id="5d3f2-718">ImmutabilityPolicy에서 AllowProtectedAppendWrite가 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-718">Supported AllowProtectedAppendWrite in ImmutabilityPolicy</span></span>
    - <span data-ttu-id="5d3f2-719">'Set-AzRmStorageContainerImmutabilityPolicy'</span><span class="sxs-lookup"><span data-stu-id="5d3f2-719">'Set-AzRmStorageContainerImmutabilityPolicy'</span></span>
* <span data-ttu-id="5d3f2-720">이후 릴리스에서 AzureStorageTable 형식 변경에 대한 호환성이 손상되는 변경 경고 메시지가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-720">Added breaking change warning message for AzureStorageTable type change in a future release</span></span>
    - <span data-ttu-id="5d3f2-721">'New-AzStorageTable'</span><span class="sxs-lookup"><span data-stu-id="5d3f2-721">'New-AzStorageTable'</span></span>
    - <span data-ttu-id="5d3f2-722">'Get-AzStorageTable'</span><span class="sxs-lookup"><span data-stu-id="5d3f2-722">'Get-AzStorageTable'</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="5d3f2-723">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="5d3f2-723">Az.Websites</span></span>
* <span data-ttu-id="5d3f2-724">'New-AzAppServicePlan' 및 'Set-AzAppServicePlan'에 대한 Tag 매개 변수가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-724">Added Tag parameter for 'New-AzAppServicePlan' and 'Set-AzAppServicePlan'</span></span>
* <span data-ttu-id="5d3f2-725">웹 사이트에 사용자 지정 도메인을 추가할 때 예외가 throw되면 cmdlet 실행을 중지합니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-725">Stop cmdlet execution if an exception is thrown when adding a custom domain to a website</span></span>
* <span data-ttu-id="5d3f2-726">App Service 계획과 동일한 리소스 그룹에 속하지 않는 App Services에 대한 작업을 수행하기 위한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-726">Added support to perform operations for App Services not in the same resource group as the App Service Plan</span></span>
* <span data-ttu-id="5d3f2-727">다른 리소스 그룹의 WebApp/Function에 대한 액세스 제한이 적용되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-727">Applied access restriction to WebApp/Function in different resource groups</span></span>
* <span data-ttu-id="5d3f2-728">WebAppSlot에 대한 사용자 지정 호스트 이름을 설정하는 문제가 해결되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-728">Fixed issue to set custom hostnames for WebAppSlots</span></span>

## <a name="350---february-2020"></a><span data-ttu-id="5d3f2-729">3.5.0 - 2020년 2월</span><span class="sxs-lookup"><span data-stu-id="5d3f2-729">3.5.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="5d3f2-730">마지막 주 릴리스 이후의 주요 사항</span><span class="sxs-lookup"><span data-stu-id="5d3f2-730">Highlights since the last major release</span></span>
* <span data-ttu-id="5d3f2-731">클라이언트 쪽 원격 분석이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-731">Updated client side telemetry.</span></span>
* <span data-ttu-id="5d3f2-732">디바이스 관리를 지원하는 cmdlet이 Az.IotHub에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-732">Az.IotHub added cmdlets to support to manage devices.</span></span>
* <span data-ttu-id="5d3f2-733">가용성 그룹 수신기에 대한 cmdlet이 Az.SqlVirtualMachine에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-733">Az.SqlVirtualMachine added cmdlets for Availability Group Listener.</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="5d3f2-734">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="5d3f2-734">Az.Accounts</span></span>
* <span data-ttu-id="5d3f2-735">SubscriptionId, TenantId 및 실행 시간이 클라이언트 쪽 원격 분석에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-735">Added SubscriptionId, TenantId, and execution time into data of client side telemetry</span></span>

#### <a name="azautomation"></a><span data-ttu-id="5d3f2-736">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="5d3f2-736">Az.Automation</span></span>
* <span data-ttu-id="5d3f2-737">'New-AzAutomationSoftwareUpdateConfiguration' 참조 설명서의 예제 1에 있는 오타가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-737">Fixed typo in Example 1 in reference documentation for 'New-AzAutomationSoftwareUpdateConfiguration'</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="5d3f2-738">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="5d3f2-738">Az.CognitiveServices</span></span>
* <span data-ttu-id="5d3f2-739">SDK가 7.0으로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-739">Updated SDK to 7.0</span></span>
* <span data-ttu-id="5d3f2-740">서버 응답 본문이 비어 있는 경우 표시되는 오류 메시지가 향상되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-740">Improved error message when server responses empty body</span></span>

#### <a name="azcompute"></a><span data-ttu-id="5d3f2-741">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="5d3f2-741">Az.Compute</span></span>
* <span data-ttu-id="5d3f2-742">업데이트하는 동안 빈 값이 ProximityPlacementGroupId에 허용되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-742">Allowed empty value for ProximityPlacementGroupId during update</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="5d3f2-743">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="5d3f2-743">Az.FrontDoor</span></span>
* <span data-ttu-id="5d3f2-744">WAF에서 사용할 수 있는 관리형 규칙 정의를 가져오는 cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-744">Added cmdlet to get managed rule definitions that can be used in WAF</span></span>

#### <a name="aziothub"></a><span data-ttu-id="5d3f2-745">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="5d3f2-745">Az.IotHub</span></span>
* <span data-ttu-id="5d3f2-746">Iot Hub에서 디바이스를 관리하기 위한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-746">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="5d3f2-747">새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-747">New Cmdlets are:</span></span>
    - <span data-ttu-id="5d3f2-748">'Add-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="5d3f2-748">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="5d3f2-749">'Get-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="5d3f2-749">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="5d3f2-750">'Remove-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="5d3f2-750">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="5d3f2-751">'Set-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="5d3f2-751">'Set-AzIotHubDevice'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="5d3f2-752">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="5d3f2-752">Az.KeyVault</span></span>
* <span data-ttu-id="5d3f2-753">Add-AzKeyVaultKey.md에 대해 중복된 텍스트가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-753">Fixed duplicated text for Add-AzKeyVaultKey.md</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="5d3f2-754">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="5d3f2-754">Az.Monitor</span></span>
* <span data-ttu-id="5d3f2-755">Get-AzLog cmdlet에 대한 설명이 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-755">Fixed description of the Get-AzLog cmdlet.</span></span>
* <span data-ttu-id="5d3f2-756">ActionGroupId라는 새 매개 변수가 'New-AzMetricAlertRuleV2' 명령에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-756">A new parameter called ActionGroupId was added to 'New-AzMetricAlertRuleV2' command.</span></span>
    - <span data-ttu-id="5d3f2-757">사용자는 ActionGroupId(string) 또는 ActionGorup(ActivityLogAlertActionGroup) 중 하나를 제공할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-757">The user can provide either ActionGroupId(string) or ActionGorup(ActivityLogAlertActionGroup).</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="5d3f2-758">Az.Network</span><span class="sxs-lookup"><span data-stu-id="5d3f2-758">Az.Network</span></span>
* <span data-ttu-id="5d3f2-759">'New-AzPrivateLinkService' cmdlet의 '-EnableProxyProtocol' 매개 변수에 대한 하나의 추가 매개 변수 메모가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-759">Added one extra parameter note for parameter '-EnableProxyProtocol' for 'New-AzPrivateLinkService' cmdlet.</span></span>
* <span data-ttu-id="5d3f2-760">Start-AzVirtualNetworkGatewayConnectionPacketCapture.md 및 Start-AzVirtualnetworkGatewayPacketCapture.md의 FilterData 예제가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-760">Fixed FilterData example in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="5d3f2-761">Start-AzVirtualNetworkGatewayConnectionPacketCapture.md 및 Start-AzVirtualnetworkGatewayPacketCapture.md의 모든 내부 및 외부 패킷을 캡처하는 패킷 캡처 예제가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-761">Added Packet Capture example for capture all inner and outer packets in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="5d3f2-762">VNet 방화벽에서 Azure Firewall 정책이 지원됩니다</span><span class="sxs-lookup"><span data-stu-id="5d3f2-762">Supported Azure Firewall Policy on VNet Firewalls</span></span>
    - <span data-ttu-id="5d3f2-763">새로 추가된 cmdlet이 없습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-763">No new cmdlets are added.</span></span> <span data-ttu-id="5d3f2-764">VNet 방화벽에서 방화벽 정책 제한이 완화되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-764">Relaxing the restriction for firewall policy on VNet firewalls</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="5d3f2-765">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="5d3f2-765">Az.RecoveryServices</span></span>
* <span data-ttu-id="5d3f2-766">SQL Database에 대한 파일로 복원 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-766">Added Support for Restore-as-files for SQL Databases.</span></span>

#### <a name="azresources"></a><span data-ttu-id="5d3f2-767">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="5d3f2-767">Az.Resources</span></span>
* <span data-ttu-id="5d3f2-768">템플릿 배포 cmdlet이 리팩터링되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-768">Refactored template deployment cmdlets</span></span>
    - <span data-ttu-id="5d3f2-769">관리 그룹에서 배포를 관리하는 새 \*-AzManagementGroupDeployment cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-769">Added new cmdlets for managing deployments at management group: \*-AzManagementGroupDeployment</span></span>
    - <span data-ttu-id="5d3f2-770">테넌트 범위에서 배포를 관리하는 새 \*-AzTenantDeployment cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-770">Added new cmdlets for managing deployments at tenant scope: \*-AzTenantDeployment</span></span>
    - <span data-ttu-id="5d3f2-771">구독 범위에서 구체적으로 작동하도록 \*-AzDeployment cmdlet이 리팩터링되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-771">Refactored \*-AzDeployment cmdlets to work specifically at subscription scope</span></span>
    - <span data-ttu-id="5d3f2-772">\*-AzDeployment cmdlet에 대한 \*-AzSubscriptionDeployment 별칭이 만들어졌습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-772">Created aliases \*-AzSubscriptionDeployment for \*-AzDeployment cmdlets</span></span>
* <span data-ttu-id="5d3f2-773">'AvailableToOtherTenants' 매개 변수가 설정되지 않는 'Update-AzADApplication'이 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-773">Fixed 'Update-AzADApplication' when parameter 'AvailableToOtherTenants' is not set</span></span>
* <span data-ttu-id="5d3f2-774">AmbiguousParameterSetException을 방지하기 위해 ApplicationObjectWithoutCredentialParameterSet이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-774">Removed ApplicationObjectWithoutCredentialParameterSet to avoid AmbiguousParameterSetException.</span></span>
* <span data-ttu-id="5d3f2-775">도움말 파일이 다시 생성되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-775">Regenerated help files</span></span>

#### <a name="azsql"></a><span data-ttu-id="5d3f2-776">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="5d3f2-776">Az.Sql</span></span>
* <span data-ttu-id="5d3f2-777">Managed Instance에서 구독 간 특정 시점 복원에 대한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-777">Added support for cross subscription point in time restore on Managed Instances.</span></span>
* <span data-ttu-id="5d3f2-778">기존 SQL Managed Instance 하드웨어 생성 변경에 대한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-778">Added support for changing existing Sql Managed Instance hardware generation</span></span>
* <span data-ttu-id="5d3f2-779">'Update-AzSqlServerVulnerabilityAssessmentSetting' 도움말 예제(매개 변수/속성 출력 -EmailAdmins)가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-779">Fixed 'Update-AzSqlServerVulnerabilityAssessmentSetting' help examples: parameter/property output - EmailAdmins</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="5d3f2-780">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="5d3f2-780">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="5d3f2-781">가용성 그룹 수신기에 대한 cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-781">Added cmdlets for Availability Group Listener</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="5d3f2-782">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="5d3f2-782">Az.StorageSync</span></span>
* <span data-ttu-id="5d3f2-783">'Invoke-AzStorageSyncCompatibilityCheck'에서 지원되는 문자 세트가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-783">Updated supported character sets in 'Invoke-AzStorageSyncCompatibilityCheck'.</span></span>

## <a name="340---february-2020"></a><span data-ttu-id="5d3f2-784">3.4.0 - 2020년 2월</span><span class="sxs-lookup"><span data-stu-id="5d3f2-784">3.4.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="5d3f2-785">마지막 주 릴리스 이후의 주요 사항</span><span class="sxs-lookup"><span data-stu-id="5d3f2-785">Highlights since the last major release</span></span>
* <span data-ttu-id="5d3f2-786">Az. CosmosDB 초기 버전 0.1.0 출시</span><span class="sxs-lookup"><span data-stu-id="5d3f2-786">Az.CosmosDB initial version 0.1.0 released</span></span>
* <span data-ttu-id="5d3f2-787">Az.Network ConnectionMonitor V2 지원 추가</span><span class="sxs-lookup"><span data-stu-id="5d3f2-787">Az.Network ConnectionMonitor V2 support added</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="5d3f2-788">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="5d3f2-788">Az.Accounts</span></span>
* <span data-ttu-id="5d3f2-789">AzureRmContext.json을 사용할 수 없을 때 컨텍스트 자동 저장 사용 안 함</span><span class="sxs-lookup"><span data-stu-id="5d3f2-789">Disable context auto saving when AzureRmContext.json not available</span></span>
* <span data-ttu-id="5d3f2-790">Azure Powershell Common 참조를 1.3.5-preview로 업데이트</span><span class="sxs-lookup"><span data-stu-id="5d3f2-790">Update the reference to Azure Powershell Common to 1.3.5-preview</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="5d3f2-791">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="5d3f2-791">Az.ApiManagement</span></span>
* <span data-ttu-id="5d3f2-792">**Get-AzApiManagementApiSchema** API와 연결된 Open-Api 스키마 가져오기 수정   https://github.com/Azure/azure-powershell/issues/10626</span><span class="sxs-lookup"><span data-stu-id="5d3f2-792">**Get-AzApiManagementApiSchema** Fixed getting Open-Api Schema associated with an API   https://github.com/Azure/azure-powershell/issues/10626</span></span>
* <span data-ttu-id="5d3f2-793">**New-AzApiManagementProduct**\* 및 **Set-AzApiManagementProduct**</span><span class="sxs-lookup"><span data-stu-id="5d3f2-793">**New-AzApiManagementProduct**\* and **Set-AzApiManagementProduct**</span></span>
  - <span data-ttu-id="5d3f2-794">https://github.com/Azure/azure-powershell/issues/10472 설명서 수정</span><span class="sxs-lookup"><span data-stu-id="5d3f2-794">Fix documentation for https://github.com/Azure/azure-powershell/issues/10472</span></span>
* <span data-ttu-id="5d3f2-795">**Set-AzApiManagementApi** cmdlet을 사용하여 ServiceUrl을 업데이트하는 방법을 보여주는 예제 추가</span><span class="sxs-lookup"><span data-stu-id="5d3f2-795">**Set-AzApiManagementApi** Added example to show how to update the ServiceUrl using the cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="5d3f2-796">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="5d3f2-796">Az.Compute</span></span>
* <span data-ttu-id="5d3f2-797">VM 이름을 사용하지 않고 Get-AzVM -Status를 수행할 때 제한을 피하기 위해 VM 상태 수를 100개로 제한</span><span class="sxs-lookup"><span data-stu-id="5d3f2-797">Limit the number of VM status to 100 to avoid throttling when Get-AzVM -Status is performed without VM name.</span></span>
* <span data-ttu-id="5d3f2-798">Update-AzDiskEncryptionSet cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="5d3f2-798">Add Update-AzDiskEncryptionSet cmdlet</span></span>
* <span data-ttu-id="5d3f2-799">다음 cmdlet에 EncryptionType 및 DiskEncryptionSetId 매개 변수 추가:</span><span class="sxs-lookup"><span data-stu-id="5d3f2-799">Add EncryptionType and DiskEncryptionSetId parameters to the following cmdlets:</span></span>
    - <span data-ttu-id="5d3f2-800">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="5d3f2-800">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span></span>
* <span data-ttu-id="5d3f2-801">Get-AzProximityPlacementGroup cmdlet에 ColocationStatus 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="5d3f2-801">Add ColocationStatus parameter to Get-AzProximityPlacementGroup cmdlet.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="5d3f2-802">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="5d3f2-802">Az.DataFactory</span></span>
* <span data-ttu-id="5d3f2-803">ADF .Net SDK 버전을 4.7.0으로 업데이트</span><span class="sxs-lookup"><span data-stu-id="5d3f2-803">Update ADF .Net SDK version to 4.7.0</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="5d3f2-804">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="5d3f2-804">Az.DeploymentManager</span></span>
* <span data-ttu-id="5d3f2-805">리소스에 대한 LIST 작업 추가</span><span class="sxs-lookup"><span data-stu-id="5d3f2-805">Adds LIST operations for resources</span></span>
* <span data-ttu-id="5d3f2-806">상태 검사 단계에 대한 작업을 수행하는 기능 추가</span><span class="sxs-lookup"><span data-stu-id="5d3f2-806">Adds capability for performing operations on Health Check steps</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="5d3f2-807">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="5d3f2-807">Az.HDInsight</span></span>
* <span data-ttu-id="5d3f2-808">AzHDInsightCluster의 문서 오류 수정</span><span class="sxs-lookup"><span data-stu-id="5d3f2-808">Fix document error of New-AzHDInsightCluster.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="5d3f2-809">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="5d3f2-809">Az.KeyVault</span></span>
* <span data-ttu-id="5d3f2-810">Remove-AzureKeyVault가 새 New-AzureKeyVault와 일관성을 유지하도록 VaultName 특성에 이름 별칭 추가</span><span class="sxs-lookup"><span data-stu-id="5d3f2-810">Add Name alias to VaultName attribute to make Remove-AzureKeyVault consistent with New-AzureKeyVault.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="5d3f2-811">Az.Network</span><span class="sxs-lookup"><span data-stu-id="5d3f2-811">Az.Network</span></span>
* <span data-ttu-id="5d3f2-812">Set-AzNetworkWatcherConfigFlowLog.md에 트래픽 분석 사용 안 함 시나리오를 보여주는 새 예제 추가</span><span class="sxs-lookup"><span data-stu-id="5d3f2-812">New example added to Set-AzNetworkWatcherConfigFlowLog.md to demonstrate Traffic Analytics disable scenario.</span></span>
* <span data-ttu-id="5d3f2-813">Azure Firewall에 관리 IP 구성을 할당하는 지원 추가 - 방화벽에서 관리 트래픽에 사용할 전용 서브넷 및 공용 IP</span><span class="sxs-lookup"><span data-stu-id="5d3f2-813">Add support for assigning management IP configuration to Azure Firewall - a dedicated subnet and Public IP that the firewall will use for its management traffic</span></span>
    - <span data-ttu-id="5d3f2-814">New-AzFirewall cmdlet이 업데이트됨:</span><span class="sxs-lookup"><span data-stu-id="5d3f2-814">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="5d3f2-815">공용 IP 주소 개체를 허용하는 -ManagementPublicIpAddress 매개 변수(필수 아님) 추가</span><span class="sxs-lookup"><span data-stu-id="5d3f2-815">Added parameter -ManagementPublicIpAddress (not mandatory) which accepts a Public IP Address object</span></span>
        - <span data-ttu-id="5d3f2-816">방화벽 개체에 SetManagementIpConfiguration 메서드 추가 - 입력으로 서브넷 및 공용 IP 주소 필요 - 서브넷 이름은 'AzureFirewallManagementSubnet'이어야 함</span><span class="sxs-lookup"><span data-stu-id="5d3f2-816">Added method SetManagementIpConfiguration on firewall object - requires a subnet and a Public IP address as input - subnet name must be 'AzureFirewallManagementSubnet'</span></span>
* <span data-ttu-id="5d3f2-817">네트워크 인터페이스 대신 NSG 예제를 보여주도록 AzNetworkSecurityGroup 예제 수정</span><span class="sxs-lookup"><span data-stu-id="5d3f2-817">Corrected Get-AzNetworkSecurityGroup examples to show examples for NSG's instead of network interfaces.</span></span>
* <span data-ttu-id="5d3f2-818">리소스 id 완성자가 매개 변수를 완성하지 못하게 방해하던 New-AzVpnSite 명령의 오타 수정</span><span class="sxs-lookup"><span data-stu-id="5d3f2-818">Fixed typo in New-AzVpnSite command that was preventing resource id completer from completing a parameter.</span></span>
* <span data-ttu-id="5d3f2-819">Application Gateway의 다시 쓰기 규칙 작업 세트에서 Url 구성에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="5d3f2-819">Added support for Url Confiugration in Rewrite Rules Action Set in the Application Gateway</span></span>
    - <span data-ttu-id="5d3f2-820">추가된 새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-820">New cmdlets added:</span></span>
        - <span data-ttu-id="5d3f2-821">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="5d3f2-821">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span></span>
    - <span data-ttu-id="5d3f2-822">선택적 매개 변수를 사용하도록 Cmdlet 업데이트 - UrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="5d3f2-822">Cmdlets updated with optional parameter - UrlConfiguration</span></span>
        - <span data-ttu-id="5d3f2-823">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="5d3f2-823">New-AzApplicationGatewayRewriteRuleActionSet</span></span>
* <span data-ttu-id="5d3f2-824">NetworkWatcher ConnectionMonitor 버전 2 리소스에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="5d3f2-824">Add suppport for NetworkWatcher ConnectionMonitor version 2 resources</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="5d3f2-825">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="5d3f2-825">Az.PolicyInsights</span></span>
* <span data-ttu-id="5d3f2-826">수정할 리소스를 결정하기 전에 규정 준수 평가 지원</span><span class="sxs-lookup"><span data-stu-id="5d3f2-826">Support evaluating compliance prior to determining what resource to remediate</span></span>
    - <span data-ttu-id="5d3f2-827">Start-AzPolicyRemediation에 '-ResourceDiscoverMode' 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="5d3f2-827">Add '-ResourceDiscoverMode' parameter to Start-AzPolicyRemediation</span></span>
* <span data-ttu-id="5d3f2-828">정책 메타데이터 리소스를 가져오는 Get-AzPolicyMetadata cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="5d3f2-828">Add Get-AzPolicyMetadata cmdlet for getting policy metadata resources</span></span>
* <span data-ttu-id="5d3f2-829">API 버전 2019-10-01의 Get-AzPolicyState 및 Get-AzPolicyStateSummary 업데이트</span><span class="sxs-lookup"><span data-stu-id="5d3f2-829">Updated Get-AzPolicyState and Get-AzPolicyStateSummary for API version 2019-10-01</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="5d3f2-830">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="5d3f2-830">Az.RecoveryServices</span></span>
* <span data-ttu-id="5d3f2-831">복제된 디스크를 제거할 수 있도록 Azure Site Recovery에 지원 추가</span><span class="sxs-lookup"><span data-stu-id="5d3f2-831">Azure Site Recovery support for removing a replicated disk.</span></span>
* <span data-ttu-id="5d3f2-832">Recovery Services 자격 증명 모음을 만드는 동안 태그를 추가할 수 있도록 Azure Backup에 지원 추가</span><span class="sxs-lookup"><span data-stu-id="5d3f2-832">Azure Backup added support for adding tags while creating a Recovery Services Vault.</span></span>

#### <a name="azresources"></a><span data-ttu-id="5d3f2-833">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="5d3f2-833">Az.Resources</span></span>
* <span data-ttu-id="5d3f2-834">컨텍스트 구독을 기본값으로 하는 \*-AzPolicyAssignment cmdlet에서 -Scope를 선택 사항으로 설정</span><span class="sxs-lookup"><span data-stu-id="5d3f2-834">Make -Scope optional in \*-AzPolicyAssignment cmdlets with default to context subscription</span></span>
* <span data-ttu-id="5d3f2-835">암호 및 키 자격 증명을 사용하여 ADServicePrincipal을 만드는 예제 추가</span><span class="sxs-lookup"><span data-stu-id="5d3f2-835">Add examples of creating ADServicePrincipal with password and key credential</span></span>

#### <a name="azsql"></a><span data-ttu-id="5d3f2-836">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="5d3f2-836">Az.Sql</span></span>
<span data-ttu-id="5d3f2-837">DatabaseName 대신 PartnerDatabaseName이 있는지 확인하도록 New-AzSqlDatabaseSecondary cmdlet 수정</span><span class="sxs-lookup"><span data-stu-id="5d3f2-837">Fix New-AzSqlDatabaseSecondary cmdlet to check for PartnerDatabaseName existence instead of DatabaseName existence.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="5d3f2-838">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="5d3f2-838">Az.Storage</span></span>
* <span data-ttu-id="5d3f2-839">스토리지 계정 만들기에서 테이블/큐 암호화 Keytype 설정 지원</span><span class="sxs-lookup"><span data-stu-id="5d3f2-839">Support set Table/Queue Encryption Keytype in Create Storage Account</span></span>
    - <span data-ttu-id="5d3f2-840">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="5d3f2-840">New-AzStorageAccount</span></span>
* <span data-ttu-id="5d3f2-841">StorageException에 ExtendedErrorInformation이 없으면 RequestId 표시</span><span class="sxs-lookup"><span data-stu-id="5d3f2-841">Show RequestId when StorageException don't have ExtendedErrorInformation</span></span>
* <span data-ttu-id="5d3f2-842">cmdlet Start-AzStorageBlobCopy의 예제 6 수정</span><span class="sxs-lookup"><span data-stu-id="5d3f2-842">Fix the Example 6 of cmdlet Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="5d3f2-843">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="5d3f2-843">Az.Websites</span></span>
* <span data-ttu-id="5d3f2-844">Set-AzWebapp 및 Set-AzWebappSlot이 AlwaysOn, MinTls 및 FtpsState 속성 지원</span><span class="sxs-lookup"><span data-stu-id="5d3f2-844">Set-AzWebapp and Set-AzWebappSlot supports AlwaysOn, MinTls and FtpsState properties</span></span>
* <span data-ttu-id="5d3f2-845">단일 Set-AzWebApp 명령을 사용하여 AppservicePlan을 변경하는 동시에 HttpsOnly를 설정하면 HttpsOnly가 기본값으로 다시 설정되는 문제 수정</span><span class="sxs-lookup"><span data-stu-id="5d3f2-845">Fixing issue where setting HttpsOnly along with changing AppservicePlan at the same time using the single Set-AzWebApp Command, was resetting HttpsOnly to default value</span></span>

## <a name="330---january-2020"></a><span data-ttu-id="5d3f2-846">3.3.0 - 2020년 1월</span><span class="sxs-lookup"><span data-stu-id="5d3f2-846">3.3.0 - January 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="5d3f2-847">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="5d3f2-847">Az.Accounts</span></span>
* <span data-ttu-id="5d3f2-848">AzureAttestationServiceEndpointResourceId 및 AzureAttestationServiceEndpointSuffix 매개 변수를 허용하도록 Add-AzEnvironment 및 Set-AzEnvironment가 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="5d3f2-848">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameters AzureAttestationServiceEndpointResourceId and AzureAttestationServiceEndpointSuffix</span></span>

#### <a name="azcdn"></a><span data-ttu-id="5d3f2-849">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="5d3f2-849">Az.Cdn</span></span>
* <span data-ttu-id="5d3f2-850">New-AzCdnEndpoint cmdlet에서 오류 응답 세부 정보 표시</span><span class="sxs-lookup"><span data-stu-id="5d3f2-850">Display error response detail in New-AzCdnEndpoint cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="5d3f2-851">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="5d3f2-851">Az.Compute</span></span>
* <span data-ttu-id="5d3f2-852">OS 프로필이 없는 관리 OD 디스크가 있는 VM의 Set-AzVMCustomScriptExtension cmdlet을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-852">Fix Set-AzVMCustomScriptExtension cmdlet for a VM with managed OD disk which does not have OS profile.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="5d3f2-853">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="5d3f2-853">Az.ContainerInstance</span></span>
* <span data-ttu-id="5d3f2-854">New-AzContainerGroup의 예에서 사용되는 고정 매개 변수 이름</span><span class="sxs-lookup"><span data-stu-id="5d3f2-854">Fixed parameter names used by example of New-AzContainerGroup</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="5d3f2-855">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="5d3f2-855">Az.DataBoxEdge</span></span>
* <span data-ttu-id="5d3f2-856">'Get-AzDataBoxEdgeStorageContainer' cmdlet 추가됨</span><span class="sxs-lookup"><span data-stu-id="5d3f2-856">Added cmdlet 'Get-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="5d3f2-857">Edge 스토리지 컨테이너 가져오기</span><span class="sxs-lookup"><span data-stu-id="5d3f2-857">Get the Edge Storage Container</span></span>
* <span data-ttu-id="5d3f2-858">'New-AzDataBoxEdgeStorageContainer' cmdlet 추가됨</span><span class="sxs-lookup"><span data-stu-id="5d3f2-858">Added cmdlet 'New-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="5d3f2-859">새 Edge 스토리지 컨테이너 만들기</span><span class="sxs-lookup"><span data-stu-id="5d3f2-859">Create new Edge Strorage Container</span></span>
* <span data-ttu-id="5d3f2-860">'Remove-AzDataBoxEdgeStorageContainer' cmdlet 추가됨</span><span class="sxs-lookup"><span data-stu-id="5d3f2-860">Added cmdlet 'Remove-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="5d3f2-861">Edge 스토리지 컨테이너 제거</span><span class="sxs-lookup"><span data-stu-id="5d3f2-861">Remove the Edge Storage Container</span></span>
* <span data-ttu-id="5d3f2-862">'Invoke-AzDataBoxEdgeStorageContainer' cmdlet 추가됨</span><span class="sxs-lookup"><span data-stu-id="5d3f2-862">Added cmdlet 'Invoke-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="5d3f2-863">Edge 스토리지 컨테이너에서 데이터를 새로 고치는 작업 호출</span><span class="sxs-lookup"><span data-stu-id="5d3f2-863">Invoke action to refresh data on Edge Storage Container</span></span>
* <span data-ttu-id="5d3f2-864">'Get-AzDataBoxEdgeStorageAccount' cmdlet 추가됨</span><span class="sxs-lookup"><span data-stu-id="5d3f2-864">Added cmdlet 'Get-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="5d3f2-865">Edge 스토리지 계정 가져오기</span><span class="sxs-lookup"><span data-stu-id="5d3f2-865">Get the Edge Storage Account</span></span>
* <span data-ttu-id="5d3f2-866">'New-AzDataBoxEdgeStorageAccount' cmdlet 추가됨</span><span class="sxs-lookup"><span data-stu-id="5d3f2-866">Added cmdlet 'New-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="5d3f2-867">새 Edge 스토리지 계정 만들기</span><span class="sxs-lookup"><span data-stu-id="5d3f2-867">Create new Edge Storage Account</span></span>
* <span data-ttu-id="5d3f2-868">'Remove-AzDataBoxEdgeStorageAccount' cmdlet 추가됨</span><span class="sxs-lookup"><span data-stu-id="5d3f2-868">Added cmdlet 'Remove-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="5d3f2-869">Edge 스토리지 계정 제거</span><span class="sxs-lookup"><span data-stu-id="5d3f2-869">Remove the Edge Storage Account</span></span>
* <span data-ttu-id="5d3f2-870">'Invoke-AzDataBoxEdgeShare' cmdlet 호출</span><span class="sxs-lookup"><span data-stu-id="5d3f2-870">Invoke cmdlet 'Invoke-AzDataBoxEdgeShare'</span></span>
  - <span data-ttu-id="5d3f2-871">공유에서 데이터를 새로 고치는 작업 호출</span><span class="sxs-lookup"><span data-stu-id="5d3f2-871">Invoke action to refresh data on share</span></span>
* <span data-ttu-id="5d3f2-872">'Set-AzDataBoxEdgeStorageAccountCredential' cmdlet 추가됨</span><span class="sxs-lookup"><span data-stu-id="5d3f2-872">Added cmdlet 'Set-AzDataBoxEdgeStorageAccountCredential'</span></span>
  - <span data-ttu-id="5d3f2-873">az databoxedge 스토리지 계정 자격 증명 설정</span><span class="sxs-lookup"><span data-stu-id="5d3f2-873">Set the az databoxedge storage account credential</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="5d3f2-874">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="5d3f2-874">Az.DataFactory</span></span>
* <span data-ttu-id="5d3f2-875">Get-AzDataFactoryV2IntegrationRuntime cmd에 AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId 및 VersionStatus 속성 추가</span><span class="sxs-lookup"><span data-stu-id="5d3f2-875">Add AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId and VersionStatus properties for Get-AzDataFactoryV2IntegrationRuntime cmd</span></span>
* <span data-ttu-id="5d3f2-876">ADF .Net SDK 버전을 4.6.0으로 업데이트</span><span class="sxs-lookup"><span data-stu-id="5d3f2-876">Update ADF .Net SDK version to 4.6.0</span></span>
* <span data-ttu-id="5d3f2-877">고정 공용 IP 주소로 Azure-SSIS IR을 만들 수 있도록 'Set-AzureRmDataFactoryV2IntegrationRuntime'cmd에 대해 'PublicIPs' 매개 변수를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-877">Add parameter 'PublicIPs' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable create Azure-SSIS IR with static public IP addresses.</span></span>

#### <a name="azdevtestlabs"></a><span data-ttu-id="5d3f2-878">Az.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="5d3f2-878">Az.DevTestLabs</span></span>
* <span data-ttu-id="5d3f2-879">Get-AzDtlAllowedVMSizesPolicy.md에서 끊어진 링크 제거</span><span class="sxs-lookup"><span data-stu-id="5d3f2-879">Remove the broken link in Get-AzDtlAllowedVMSizesPolicy.md</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="5d3f2-880">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="5d3f2-880">Az.EventHub</span></span>
* <span data-ttu-id="5d3f2-881">10634 문제 해결: eventhubnamespace 제거에 대한 null 개체 참조 수정</span><span class="sxs-lookup"><span data-stu-id="5d3f2-881">Fix for issue 10634 : Fix the null Object reference for remove eventhubnamespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="5d3f2-882">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="5d3f2-882">Az.HDInsight</span></span>
* <span data-ttu-id="5d3f2-883">Invoke-AzHDInsightHiveJob.md 오류를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-883">Fix Invoke-AzHDInsightHiveJob.md error.</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="5d3f2-884">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="5d3f2-884">Az.MachineLearning</span></span>
* <span data-ttu-id="5d3f2-885">MachineLearningCompute를 더 이상 사용할 수 없게 되어 아래 cmdlet이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-885">Removed below cmdlets because MachineLearningCompute is not available any longer</span></span>
  - <span data-ttu-id="5d3f2-886">Get-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="5d3f2-886">Get-AzMlOpCluster</span></span>
  - <span data-ttu-id="5d3f2-887">Get-AzMlOpClusterKey</span><span class="sxs-lookup"><span data-stu-id="5d3f2-887">Get-AzMlOpClusterKey</span></span>
  - <span data-ttu-id="5d3f2-888">New-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="5d3f2-888">New-AzMlOpCluster</span></span>
  - <span data-ttu-id="5d3f2-889">Remove-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="5d3f2-889">Remove-AzMlOpCluster</span></span>
  - <span data-ttu-id="5d3f2-890">Set-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="5d3f2-890">Set-AzMlOpCluster</span></span>
  - <span data-ttu-id="5d3f2-891">Test-AzMlOpClusterSystemServicesUpdateAvailability</span><span class="sxs-lookup"><span data-stu-id="5d3f2-891">Test-AzMlOpClusterSystemServicesUpdateAvailability</span></span>
  - <span data-ttu-id="5d3f2-892">Update-AzMlOpClusterSystemService</span><span class="sxs-lookup"><span data-stu-id="5d3f2-892">Update-AzMlOpClusterSystemService</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="5d3f2-893">Az.Network</span><span class="sxs-lookup"><span data-stu-id="5d3f2-893">Az.Network</span></span>
* <span data-ttu-id="5d3f2-894">Microsoft.Azure.Management.Sql의 종속성을 1.36-preview에서 1.37-preview로 업그레이드</span><span class="sxs-lookup"><span data-stu-id="5d3f2-894">Upgrade dependency of Microsoft.Azure.Management.Sql from 1.36-preview to 1.37-preview</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="5d3f2-895">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="5d3f2-895">Az.RecoveryServices</span></span>
* <span data-ttu-id="5d3f2-896">Azure Site Recovery는 Azure 간 공급자를 위해 고객 관리 키와 함께 유휴 상태에서 암호화된 관리 디스크 vms의 변경을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-896">Azure Site Recovery change support for managed disk vms encrypted at rest with customer managed keys for Azure to Azure provider.</span></span>
* <span data-ttu-id="5d3f2-897">Azure Site Recovery는 VMware에서 Azure로를 위해 보호를 사용할 때 선택적 입력으로서 디스크 암호화 집합 ID를 입력하도록 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-897">Azure Site Recovery support to input disk encryption Set Id as optional input at enabling protection for Vmware to Azure.</span></span>
* <span data-ttu-id="5d3f2-898">Azure Site Recovery는 VMware에서 Azure로를 위해 보호를 사용하기 위해 디스크 수준의 선택적 입력으로서 디스크 암호화 집합 ID를 입력하도록 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-898">Azure Site Recovery support to input disk encryption Set Id as optional input at disk level to enable protection for Vmware to Azure.</span></span>
* <span data-ttu-id="5d3f2-899">Azure Site Recovery는 HyperV에서 Azure로를 위해 디스크 암호화 집합 맵을 사용하여 복제 보호된 항목을 업데이트하도록 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-899">Azure Site Recovery support to update replication protected item with disk encryption set Map for HyperV to Azure.</span></span>

#### <a name="azresources"></a><span data-ttu-id="5d3f2-900">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="5d3f2-900">Az.Resources</span></span>
* <span data-ttu-id="5d3f2-901">'Remove-AzTag'의 도움말 문서에서 오류를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-901">Fix an error in help document of 'Remove-AzTag'.</span></span>

#### <a name="azsql"></a><span data-ttu-id="5d3f2-902">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="5d3f2-902">Az.Sql</span></span>
* <span data-ttu-id="5d3f2-903">Azure Database의 마스터 DB에서 작동하도록 취약성 평가 세트 기준 cmdlet 기능을 수정하고 관리형 인스턴스 시스템 데이터베이스에서 이를 제한합니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-903">Fix vulnerability assessment set baseline cmdlets functionality to work on master db for azure database and limit it on managed instance system databases.</span></span>
* <span data-ttu-id="5d3f2-904">SQL 인스턴스 장애 조치(failover) 그룹을 만들 때 오류 수정</span><span class="sxs-lookup"><span data-stu-id="5d3f2-904">Fix an error when creating SQL instance failover group</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="5d3f2-905">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="5d3f2-905">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="5d3f2-906">올바른 새 라이선스 형식으로 DR 추가</span><span class="sxs-lookup"><span data-stu-id="5d3f2-906">Add DR as a new valid License type</span></span>

#### <a name="azstorage"></a><span data-ttu-id="5d3f2-907">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="5d3f2-907">Az.Storage</span></span>
* <span data-ttu-id="5d3f2-908">다음 릴리스에서 DefaultAction Value 변경에 대해 호환성이 손상되는 변경 경고 메시지 추가</span><span class="sxs-lookup"><span data-stu-id="5d3f2-908">Add breaking change warning message for DefaultAction Value change in a future release</span></span>
    - <span data-ttu-id="5d3f2-909">Update-AzStorageAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="5d3f2-909">Update-AzStorageAccountNetworkRuleSet</span></span>
* <span data-ttu-id="5d3f2-910">-IncludeGeoReplicationStats 매개 변수와 함께 get-AzureRMStorageAccount를 실행하여 스토리지 계정의 마지막 동기화 시간 가져오기 지원</span><span class="sxs-lookup"><span data-stu-id="5d3f2-910">Support Get last sync time of Storage account by run get-AzureRMStorageAccount with parameter -IncludeGeoReplicationStats</span></span>
    - <span data-ttu-id="5d3f2-911">Get-AzureRMStorageAccount</span><span class="sxs-lookup"><span data-stu-id="5d3f2-911">Get-AzureRMStorageAccount</span></span>

## <a name="320---december-2019"></a><span data-ttu-id="5d3f2-912">3.2.0 - 2019년 12월</span><span class="sxs-lookup"><span data-stu-id="5d3f2-912">3.2.0 - December 2019</span></span>

### <a name="general"></a><span data-ttu-id="5d3f2-913">일반</span><span class="sxs-lookup"><span data-stu-id="5d3f2-913">General</span></span>
* <span data-ttu-id="5d3f2-914">모든 모듈의 상대 경로를 사용하기 위해 .psd1의 참조 업데이트</span><span class="sxs-lookup"><span data-stu-id="5d3f2-914">Update references in .psd1 to use relative path for all modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="5d3f2-915">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="5d3f2-915">Az.Accounts</span></span>
* <span data-ttu-id="5d3f2-916">Az 4.0 미리 보기를 위해 클라이언트 측 원격 분석에 대해 UserAgent를 올바르게 설정</span><span class="sxs-lookup"><span data-stu-id="5d3f2-916">Set correct UserAgent for client-side telemetry for Az 4.0 preview</span></span>
* <span data-ttu-id="5d3f2-917">Az 4.0 미리 보기에서 컨텍스트가 null인 경우 사용자에게 친숙한 오류 메시지로 표시</span><span class="sxs-lookup"><span data-stu-id="5d3f2-917">Display user friendly error message when context is null in Az 4.0 preview</span></span>

#### <a name="azbatch"></a><span data-ttu-id="5d3f2-918">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="5d3f2-918">Az.Batch</span></span>
* <span data-ttu-id="5d3f2-919">**New-AzBatchPool**이 'VirtualMachineConfiguration.ContainerConfiguration' 또는 'VirtualMachineConfiguration.DataDisks'를 서버로 제대로 보내지 않는 [#10602](https://github.com/Azure/azure-powershell/issues/10602) 문제 수정</span><span class="sxs-lookup"><span data-stu-id="5d3f2-919">Fix issue [#10602](https://github.com/Azure/azure-powershell/issues/10602), where **New-AzBatchPool** did not properly send 'VirtualMachineConfiguration.ContainerConfiguration' or 'VirtualMachineConfiguration.DataDisks' to the server.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="5d3f2-920">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="5d3f2-920">Az.DataFactory</span></span>
* <span data-ttu-id="5d3f2-921">ADF .Net SDK 버전을 4.5.0으로 업데이트</span><span class="sxs-lookup"><span data-stu-id="5d3f2-921">Update ADF .Net SDK version to 4.5.0</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="5d3f2-922">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="5d3f2-922">Az.FrontDoor</span></span>
* <span data-ttu-id="5d3f2-923">WAF 관리 규칙 제외 지원 추가됨</span><span class="sxs-lookup"><span data-stu-id="5d3f2-923">Added WAF managed rules exclusion support</span></span>
* <span data-ttu-id="5d3f2-924">자동 완성에 SocketAddr 추가</span><span class="sxs-lookup"><span data-stu-id="5d3f2-924">Add SocketAddr to auto-complete</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="5d3f2-925">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="5d3f2-925">Az.HealthcareApis</span></span>
* <span data-ttu-id="5d3f2-926">예외 처리</span><span class="sxs-lookup"><span data-stu-id="5d3f2-926">Exception Handling</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="5d3f2-927">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="5d3f2-927">Az.KeyVault</span></span>
* <span data-ttu-id="5d3f2-928">잠재적으로 설정되지 않은 오류 액세스 값 수정</span><span class="sxs-lookup"><span data-stu-id="5d3f2-928">Fixed error accessing value that is potentially not set</span></span>
* <span data-ttu-id="5d3f2-929">타원 곡선 암호화 인증서 관리</span><span class="sxs-lookup"><span data-stu-id="5d3f2-929">Elliptic Curve Cryptography Certificate Managment</span></span>
    - <span data-ttu-id="5d3f2-930">인증서 정책에 대한 곡선 지정을 위한 지원 추가됨</span><span class="sxs-lookup"><span data-stu-id="5d3f2-930">Added support to specify the Curve for Certificate Policies</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="5d3f2-931">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="5d3f2-931">Az.Monitor</span></span>
* <span data-ttu-id="5d3f2-932">진단 설정 추가 명령에 선택적 인수 추가</span><span class="sxs-lookup"><span data-stu-id="5d3f2-932">Adding optional argument to the Add Diagnostic Settings command.</span></span> <span data-ttu-id="5d3f2-933">스위치 인수(있는 경우)는 Log Analytics로 내보내기가 고정 스키마(전용 데이터 유형)가 되어야 함을</span><span class="sxs-lookup"><span data-stu-id="5d3f2-933">A switch argument that if present indicates that the export to Log Analytics must be to a fixed schema (a.k.a.</span></span> <span data-ttu-id="5d3f2-934">나타냄</span><span class="sxs-lookup"><span data-stu-id="5d3f2-934">dedicated, data type)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="5d3f2-935">Az.Network</span><span class="sxs-lookup"><span data-stu-id="5d3f2-935">Az.Network</span></span>
* <span data-ttu-id="5d3f2-936">AzureFirewall 애플리케이션, NAT 및 네트워크 규칙에서 IpGroups 지원.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-936">Support for IpGroups in AzureFirewall Application,Nat & Network Rules.</span></span>

#### <a name="azresources"></a><span data-ttu-id="5d3f2-937">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="5d3f2-937">Az.Resources</span></span>
* <span data-ttu-id="5d3f2-938">이름이 일부 내장 매개 변수 이름과 충돌하는 경우 템플릿 배포가 템플릿 매개 변수를 읽지 못하는 문제 수정.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-938">Fix an issue where template deployment fails to read a template parameter if its name conflicts with some built-in parameter name.</span></span>
* <span data-ttu-id="5d3f2-939">정책 세트 정의 내에 그룹화 지원을 도입하는 새로운 API 버전 2019-09-01을 사용하도록 정책 cmdlet 업데이트.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-939">Updated policy cmdlets to use new api version 2019-09-01 that introduces grouping support within policy set definitions.</span></span>

#### <a name="azsql"></a><span data-ttu-id="5d3f2-940">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="5d3f2-940">Az.Sql</span></span>
* <span data-ttu-id="5d3f2-941">취약성 평가 자동 활성화에서 스토리지 생성을 StorageV2로 업그레이드</span><span class="sxs-lookup"><span data-stu-id="5d3f2-941">Upgraded storage creation in Vulnerability Assessment auto enablement to StorageV2</span></span>

#### <a name="azstorage"></a><span data-ttu-id="5d3f2-942">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="5d3f2-942">Az.Storage</span></span>
* <span data-ttu-id="5d3f2-943">Oauth 인증을 기반으로 스토리지 컨텍스트를 사용하여 Blob/컨테이너 ID 기반 SAS 토큰 생성 지원</span><span class="sxs-lookup"><span data-stu-id="5d3f2-943">Support generate Blob/Constainer Idenity based SAS token with Storage Context based on Oauth authentication</span></span>
    - <span data-ttu-id="5d3f2-944">New-AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="5d3f2-944">New-AzStorageContainerSASToken</span></span>
    - <span data-ttu-id="5d3f2-945">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="5d3f2-945">New-AzStorageBlobSASToken</span></span>
* <span data-ttu-id="5d3f2-946">모든 Idenity SAS 토큰을 해지할 수 있도록 스토리지 계정 사용자 위임 키 해지 지원</span><span class="sxs-lookup"><span data-stu-id="5d3f2-946">Support revoke Storage Account User Delegation Keys, so all Idenity SAS tokens are revoked</span></span>
    - <span data-ttu-id="5d3f2-947">Revoke-AzStorageAccountUserDelegationKeys</span><span class="sxs-lookup"><span data-stu-id="5d3f2-947">Revoke-AzStorageAccountUserDelegationKeys</span></span>
* <span data-ttu-id="5d3f2-948">새로운 API 버전 2019-06-01을 지원하기 위해 Microsoft.Azure.Management.Storage 14.2.0으로 업그레이드.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-948">Upgrade to Microsoft.Azure.Management.Storage 14.2.0, to support new API version 2019-06-01.</span></span>
* <span data-ttu-id="5d3f2-949">File Share cmdlet의 관리 평면에서 5120을 초과하는 값에 대해 QuotaGiB(Gibyby의 공유 할당량)를 지원하고 'Quota' 매개 변수 별칭을 'QuotaGiB' 매개 변수에 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-949">Support of QuotaGiB (Share Quota in Gibibye) for values of more than 5120 in the Management plane of File Share cmdlets and added the 'Quota' parameter alias to the 'QuotaGiB' parameter.</span></span>
    - <span data-ttu-id="5d3f2-950">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="5d3f2-950">New-AzRmStorageShare</span></span>
    - <span data-ttu-id="5d3f2-951">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="5d3f2-951">Update-AzRmStorageShare</span></span>
* <span data-ttu-id="5d3f2-952">매개 변수 'Quota'에 매개 변수 별칭 'QuotaGiB' 추가</span><span class="sxs-lookup"><span data-stu-id="5d3f2-952">Add parameter alias 'QuotaGiB' to parameter 'Quota'</span></span>
    - <span data-ttu-id="5d3f2-953">Set-AzStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="5d3f2-953">Set-AzStorageShareQuota</span></span>
* <span data-ttu-id="5d3f2-954">Set-AzStorageContainerAcl가 저장된 액세스 정책을 정리할 수 있는 문제 수정</span><span class="sxs-lookup"><span data-stu-id="5d3f2-954">Fix the issue that Set-AzStorageContainerAcl can clean up the stored Access Policy</span></span>
    - <span data-ttu-id="5d3f2-955">Set-AzStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="5d3f2-955">Set-AzStorageContainerAcl</span></span>

## <a name="310---november-2019"></a><span data-ttu-id="5d3f2-956">3.1.0 - 2019년 11월</span><span class="sxs-lookup"><span data-stu-id="5d3f2-956">3.1.0 - November 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="5d3f2-957">마지막 주 릴리스 이후의 주요 사항</span><span class="sxs-lookup"><span data-stu-id="5d3f2-957">Highlights since the last major release</span></span>
* <span data-ttu-id="5d3f2-958">Az.DataBoxEdge 1.0.0 릴리스됨</span><span class="sxs-lookup"><span data-stu-id="5d3f2-958">Az.DataBoxEdge 1.0.0 released</span></span>
* <span data-ttu-id="5d3f2-959">Az.SqlVirtualMachine 1.0.0 릴리스됨</span><span class="sxs-lookup"><span data-stu-id="5d3f2-959">Az.SqlVirtualMachine 1.0.0 released</span></span>

#### <a name="azcompute"></a><span data-ttu-id="5d3f2-960">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="5d3f2-960">Az.Compute</span></span>
* <span data-ttu-id="5d3f2-961">VM Reapply 기능</span><span class="sxs-lookup"><span data-stu-id="5d3f2-961">VM Reapply feature</span></span>
    - <span data-ttu-id="5d3f2-962">Set-AzVM cmdlet에 Reapply 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="5d3f2-962">Add Reapply parameter to Set-AzVM cmdlet</span></span>
* <span data-ttu-id="5d3f2-963">VM 확장 집합 AutomaticRepairs 기능:</span><span class="sxs-lookup"><span data-stu-id="5d3f2-963">VM Scale Set AutomaticRepairs feature:</span></span>
    - <span data-ttu-id="5d3f2-964">다음 cmdlet에 EnableAutomaticRepair, AutomaticRepairGracePeriod 및 AutomaticRepairMaxInstanceRepairsPercent 매개 변수를 추가합니다.   New-AzVmssConfig   Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="5d3f2-964">Add EnableAutomaticRepair, AutomaticRepairGracePeriod, and AutomaticRepairMaxInstanceRepairsPercent parameters to the following cmdlets:   New-AzVmssConfig   Update-AzVmss</span></span>
* <span data-ttu-id="5d3f2-965">New-AzVM에 대한 교차 테넌트 갤러리 이미지 지원</span><span class="sxs-lookup"><span data-stu-id="5d3f2-965">Cross tenant gallery image support for New-AzVM</span></span>
* <span data-ttu-id="5d3f2-966">New-AzVM, New-AzVMConfig 및 New-AzVmss cmdlet의 Priority 매개 변수의 인수 완성자에 'Spot' 추가</span><span class="sxs-lookup"><span data-stu-id="5d3f2-966">Add 'Spot' to the argument completer of Priority parameter in New-AzVM, New-AzVMConfig and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="5d3f2-967">Add-AzVmssDataDisk cmdlet에 DiskIOPSReadWrite 및 DiskMBpsReadWrite 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="5d3f2-967">Add DiskIOPSReadWrite and DiskMBpsReadWrite parameters to Add-AzVmssDataDisk cmdlet</span></span>
* <span data-ttu-id="5d3f2-968">New-AzGalleryImageVersion cmdlet의 SourceImageId 매개 변수를 선택 사항으로 변경</span><span class="sxs-lookup"><span data-stu-id="5d3f2-968">Change SourceImageId parameter of New-AzGalleryImageVersion cmdlet to optional</span></span>
* <span data-ttu-id="5d3f2-969">New-AzGalleryImageVersion cmdlet에 OSDiskImage 및 DataDiskImage 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="5d3f2-969">Add OSDiskImage and DataDiskImage parameters to New-AzGalleryImageVersion cmdlet</span></span>
* <span data-ttu-id="5d3f2-970">New-AzGalleryImageDefinition cmdlet에 HyperVGeneration 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="5d3f2-970">Add HyperVGeneration parameter to New-AzGalleryImageDefinition cmdlet</span></span>
* <span data-ttu-id="5d3f2-971">New-AzVmss, New-AzVmssConfig 및 Update-AzVmss cmdlet에 SkipExtensionsOnOverprovisionedVMs 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="5d3f2-971">Add SkipExtensionsOnOverprovisionedVMs parameters to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="5d3f2-972">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="5d3f2-972">Az.DataBoxEdge</span></span>
* <span data-ttu-id="5d3f2-973">cmdlet `Get-AzDataBoxEdgeOrder` 추가됨</span><span class="sxs-lookup"><span data-stu-id="5d3f2-973">Added cmdlet `Get-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="5d3f2-974">주문 가져오기</span><span class="sxs-lookup"><span data-stu-id="5d3f2-974">Get the Order</span></span>
* <span data-ttu-id="5d3f2-975">cmdlet `New-AzDataBoxEdgeOrder` 추가됨</span><span class="sxs-lookup"><span data-stu-id="5d3f2-975">Added cmdlet `New-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="5d3f2-976">새 주문 만들기</span><span class="sxs-lookup"><span data-stu-id="5d3f2-976">Create new Order</span></span>
* <span data-ttu-id="5d3f2-977">cmdlet `Remove-AzDataBoxEdgeOrder` 추가됨</span><span class="sxs-lookup"><span data-stu-id="5d3f2-977">Added cmdlet `Remove-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="5d3f2-978">주문 제거</span><span class="sxs-lookup"><span data-stu-id="5d3f2-978">Remove the Order</span></span>
* <span data-ttu-id="5d3f2-979">cmdlet `New-AzDataBoxEdgeShare` 변경</span><span class="sxs-lookup"><span data-stu-id="5d3f2-979">Change in cmdlet `New-AzDataBoxEdgeShare`</span></span>
    - <span data-ttu-id="5d3f2-980">이제 로컬 공유를 만듬</span><span class="sxs-lookup"><span data-stu-id="5d3f2-980">Now creates Local Share</span></span>
* <span data-ttu-id="5d3f2-981">cmdlet `Set-AzDataBoxEdgeRole` 추가됨</span><span class="sxs-lookup"><span data-stu-id="5d3f2-981">Added cmdlet `Set-AzDataBoxEdgeRole`</span></span>
    - <span data-ttu-id="5d3f2-982">이제 IotRole을 공유에 매핑할 수 있음</span><span class="sxs-lookup"><span data-stu-id="5d3f2-982">Now IotRole can be mapped to Share</span></span>
* <span data-ttu-id="5d3f2-983">cmdlet `Invoke-AzDataBoxEdgeDevice` 추가됨</span><span class="sxs-lookup"><span data-stu-id="5d3f2-983">Added cmdlet `Invoke-AzDataBoxEdgeDevice`</span></span>
    - <span data-ttu-id="5d3f2-984">스캔 업데이트 호출, 업데이트 다운로드, 디바이스에 업데이트 설치</span><span class="sxs-lookup"><span data-stu-id="5d3f2-984">Invoke scan update, download update, install updates on the device</span></span>
* <span data-ttu-id="5d3f2-985">cmdlet `Get-AzDataBoxEdgeTrigger` 추가됨</span><span class="sxs-lookup"><span data-stu-id="5d3f2-985">Added cmdlet `Get-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="5d3f2-986">트리거에 대한 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="5d3f2-986">Gets the information about Triggers</span></span>
* <span data-ttu-id="5d3f2-987">cmdlet `New-AzDataBoxEdgeTrigger` 추가됨</span><span class="sxs-lookup"><span data-stu-id="5d3f2-987">Added cmdlet `New-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="5d3f2-988">새 트리거 만들기</span><span class="sxs-lookup"><span data-stu-id="5d3f2-988">Create new Triggers</span></span>
* <span data-ttu-id="5d3f2-989">cmdlet `Remove-AzDataBoxEdgeTrigger` 추가됨</span><span class="sxs-lookup"><span data-stu-id="5d3f2-989">Added cmdlet `Remove-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="5d3f2-990">트리거 제거</span><span class="sxs-lookup"><span data-stu-id="5d3f2-990">Remove the Triggers</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="5d3f2-991">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="5d3f2-991">Az.DataFactory</span></span>
* <span data-ttu-id="5d3f2-992">ADF .Net SDK 버전을 4.4.0으로 업데이트</span><span class="sxs-lookup"><span data-stu-id="5d3f2-992">Update ADF .Net SDK version to 4.4.0</span></span>
* <span data-ttu-id="5d3f2-993">'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd에 'ExpressCustomSetup' 매개 변수를 추가하여 사용자 지정 설치 스크립트 없이 설치 구성 및 타사 구성 요소를 사용하도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-993">Add parameter 'ExpressCustomSetup' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable setup configurations and 3rd party components without custom setup script.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="5d3f2-994">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="5d3f2-994">Az.DataLakeStore</span></span>
* <span data-ttu-id="5d3f2-995">Get-AzDataLakeStoreDeletedItem 및 Restore-AzDataLakeStoreDeletedItem의 설명서 업데이트</span><span class="sxs-lookup"><span data-stu-id="5d3f2-995">Update documentation of Get-AzDataLakeStoreDeletedItem and Restore-AzDataLakeStoreDeletedItem</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="5d3f2-996">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="5d3f2-996">Az.EventHub</span></span>
* <span data-ttu-id="5d3f2-997">10301 문제 해결: SAS 토큰 날짜 형식 수정</span><span class="sxs-lookup"><span data-stu-id="5d3f2-997">Fix for issue 10301 : Fix the SAS Token date format</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="5d3f2-998">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="5d3f2-998">Az.FrontDoor</span></span>
* <span data-ttu-id="5d3f2-999">Enable-AzFrontDoorCustomDomainHttps 및 New-AzFrontDoorFrontendEndpointObject에 MinimumTlsVersion 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="5d3f2-999">Add MinimumTlsVersion parameter to Enable-AzFrontDoorCustomDomainHttps and New-AzFrontDoorFrontendEndpointObject</span></span>
* <span data-ttu-id="5d3f2-1000">New-AzFrontDoorHealthProbeSettingObject에 HealthProbeMethod 및 EnabledState 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1000">Add HealthProbeMethod and EnabledState parameters to New-AzFrontDoorHealthProbeSettingObject</span></span>
* <span data-ttu-id="5d3f2-1001">BackendPoolsSettings 개체를 생성하여 Front Door 생성/업데이트에 전달하는 새 cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1001">Add new cmdlet to create BackendPoolsSettings objec to pass into creation/update of Front Door</span></span>
    - <span data-ttu-id="5d3f2-1002">New-AzFrontDoorBackendPoolsSettingObject</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1002">New-AzFrontDoorBackendPoolsSettingObject</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="5d3f2-1003">Az.Network</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1003">Az.Network</span></span>
* <span data-ttu-id="5d3f2-1004">'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' 및 'Start-AzVirtualnetworkGatewayPacketCapture.md' FilterData 옵션 예제를 변경합니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1004">Change 'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' and 'Start-AzVirtualnetworkGatewayPacketCapture.md' FilterData option examples.</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="5d3f2-1005">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1005">Az.PrivateDns</span></span>
* <span data-ttu-id="5d3f2-1006">PrivateDns .net sdk를 버전 1.0.0으로 업데이트함</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1006">Updated PrivateDns .net sdk to version 1.0.0</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="5d3f2-1007">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1007">Az.RecoveryServices</span></span>
* <span data-ttu-id="5d3f2-1008">보호를 사용하도록 설정할 때 디스크 유형을 선택하도록 Azure Site Recovery 지원</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1008">Azure Site Recovery support to select disk type at enabling protection.</span></span>
* <span data-ttu-id="5d3f2-1009">복구 계획 동작 편집을 위한 Azure Site Recovery 버그 수정</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1009">Azure Site Recovery bug fix for recovery plan action edit.</span></span>
* <span data-ttu-id="5d3f2-1010">파일 스트림 DB를 허용하도록 Azure Backup SQL 복원 지원</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1010">Azure Backup SQL Restore support to accept filestream DBs.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="5d3f2-1011">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1011">Az.RedisCache</span></span>
* <span data-ttu-id="5d3f2-1012">'New-AzRedisCache' 및 'Set-AzRedisCache' cmdlet에 'MinimumTlsVersion' 매개 변수가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1012">Added 'MinimumTlsVersion' parameter in 'New-AzRedisCache' and 'Set-AzRedisCache' cmdlets.</span></span> <span data-ttu-id="5d3f2-1013">'Get-AzRedisCache' cmdlet 출력에 'MinimumTlsVersion'도 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1013">Also, added 'MinimumTlsVersion' in the output of 'Get-AzRedisCache' cmdlet.</span></span>
* <span data-ttu-id="5d3f2-1014">'Set-AzRedisCache' 및 'New-AzRedisCache' cmdlet의 '-Size' 매개 변수에 대한 유효성 검사가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1014">Added validation on '-Size' parameter for 'Set-AzRedisCache' and 'New-AzRedisCache' cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="5d3f2-1015">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1015">Az.Resources</span></span>
- <span data-ttu-id="5d3f2-1016">정책 할당에 새로운 EnforcementMode 속성이 있는 새 api 버전 2019-06-01을 사용하도록 정책 cmdlet이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1016">Updated policy cmdlets to use new api version 2019-06-01 that has new EnforcementMode property in policy assignment.</span></span>
- <span data-ttu-id="5d3f2-1017">정책 정의 만들기 도움말 예제가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1017">Updated create policy definition help example</span></span>
- <span data-ttu-id="5d3f2-1018">Remove-AZADServicePrincipal -ServicePrincipalName 버그를 수정하고, 서비스 사용자 이름을 찾을 수 없으면 null 참조를 throw합니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1018">Fix bug Remove-AZADServicePrincipal -ServicePrincipalName, throw null reference when service principal name not found.</span></span>
- <span data-ttu-id="5d3f2-1019">New-AZADServicePrincipal 버그를 수정하고, 테넌트에 구독이 없으면 null 참조를 throw합니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1019">Fix bug New-AZADServicePrincipal, throw null reference when tenant doesn't have any subscription.</span></span>
- <span data-ttu-id="5d3f2-1020">연결된 애플리케이션에만 자격 증명을 추가하도록 New-AzAdServicePrincipal을 변경합니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1020">Change New-AzAdServicePrincipal to add credentials only to associated application.</span></span>

#### <a name="azsql"></a><span data-ttu-id="5d3f2-1021">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1021">Az.Sql</span></span>
* <span data-ttu-id="5d3f2-1022">데이터베이스 ReadReplicaCount에 대한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1022">Added support for database ReadReplicaCount.</span></span>
* <span data-ttu-id="5d3f2-1023">영역 중복이 설정되지 않은 경우 Set-AzSqlDatabase가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1023">Fixed Set-AzSqlDatabase when zone redundancy not set</span></span>

## <a name="300---november-2019"></a><span data-ttu-id="5d3f2-1024">3.0.0 - 2019년 11월</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1024">3.0.0 - November 2019</span></span>
### <a name="general"></a><span data-ttu-id="5d3f2-1025">일반</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1025">General</span></span>
* <span data-ttu-id="5d3f2-1026">Az.PrivateDns 1.0.0 릴리스</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1026">Az.PrivateDns 1.0.0 released</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="5d3f2-1027">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1027">Az.Accounts</span></span>
* <span data-ttu-id="5d3f2-1028">'Resolve-Error' 별칭에 사용 중단 메시지를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1028">Add a deprecation message for 'Resolve-Error' alias.</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="5d3f2-1029">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1029">Az.Advisor</span></span>
* <span data-ttu-id="5d3f2-1030">Get-AzAdvisorRecommendation cmdlet에 새로운 '운영 효율성' 범주가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1030">Added new category 'Operational Excellence' to Get-AzAdvisorRecommendation cmdlet.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="5d3f2-1031">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1031">Az.Batch</span></span>
* <span data-ttu-id="5d3f2-1032">`BatchAccountContext`의 `CoreQuota` 이름이 `DedicatedCoreQuota`로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1032">Renamed `CoreQuota` on `BatchAccountContext` to `DedicatedCoreQuota`.</span></span> <span data-ttu-id="5d3f2-1033">또한 `LowPriorityCoreQuota`가 새로 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1033">There is also a new `LowPriorityCoreQuota`.</span></span>
  - <span data-ttu-id="5d3f2-1034">이 변경 사항은 **Get-AzBatchAccount**에 영향을 줍니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1034">This impacts **Get-AzBatchAccount**.</span></span>
* <span data-ttu-id="5d3f2-1035">이제 **New-AzBatchTask** `-ResourceFile` 매개 변수는 새로운 **New-AzBatchResourceFile** cmdlet을 사용하여 구성할 수 있는 `PSResourceFile` 개체의 컬렉션을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1035">**New-AzBatchTask** `-ResourceFile` parameter now takes a collection of `PSResourceFile` objects, which can be constructed using the new **New-AzBatchResourceFile** cmdlet.</span></span>
* <span data-ttu-id="5d3f2-1036">새로운 **New-AzBatchResourceFile** cmdlet을 통해 `PSResourceFile` 개체를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1036">New **New-AzBatchResourceFile** cmdlet to help create `PSResourceFile` objects.</span></span> <span data-ttu-id="5d3f2-1037">이들은 `-ResourceFile` 매개 변수의 **New-AzBatchTask**에 제공될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1037">These can be supplied to **New-AzBatchTask** on the `-ResourceFile` parameter.</span></span>
  - <span data-ttu-id="5d3f2-1038">그에 따라 기존 `HttpUrl` 방법 외에도 두 가지 종류의 리소스 파일이 새롭게 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1038">This supports two new kinds of resource file in addition to the existing `HttpUrl` way:</span></span>
    - <span data-ttu-id="5d3f2-1039">`AutoStorageContainerName` 기반 리소스 파일은 전체 자동 스토리지 컨테이너를 일괄 처리 노드에 다운로드합니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1039">`AutoStorageContainerName` based resource files download an entire auto-storage container to the Batch node.</span></span>
    - <span data-ttu-id="5d3f2-1040">`StorageContainerUrl` 기반 리소스 파일은 URL에 지정된 컨테이너를 일괄 처리 노드에 다운로드합니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1040">`StorageContainerUrl` based resource files download the container specified in the URL to the Batch node.</span></span>
* <span data-ttu-id="5d3f2-1041">**Get-AzBatchApplication**으로 반환되는 `PSApplication`의 `ApplicationPackages` 속성이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1041">Removed `ApplicationPackages` property of `PSApplication` returned by **Get-AzBatchApplication**.</span></span>
  - <span data-ttu-id="5d3f2-1042">이제 **Get-AzBatchApplicationPackage**를 사용하여 애플리케이션 내부의 특정 패키지를 검색할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1042">The specific packages inside of an application now can be retrieved using **Get-AzBatchApplicationPackage**.</span></span> <span data-ttu-id="5d3f2-1043">예: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1043">For example: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span></span>
* <span data-ttu-id="5d3f2-1044">**Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication** 및 **Set-AzBatchApplication**에서 `ApplicationId` 이름이 `ApplicationName`으로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1044">Renamed `ApplicationId` to `ApplicationName` on **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication**, and **Set-AzBatchApplication**.</span></span>
  - <span data-ttu-id="5d3f2-1045">이제 `ApplicationId`는 `ApplicationName`의 별칭입니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1045">`ApplicationId` now is an alias of `ApplicationName`.</span></span>
* <span data-ttu-id="5d3f2-1046">새로운 `PSWindowsUserConfiguration` 속성이 `PSUserAccount`에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1046">Added new `PSWindowsUserConfiguration` property to `PSUserAccount`.</span></span>
* <span data-ttu-id="5d3f2-1047">`PSApplicationPackage`에서 `Version` 이름이 `Name`으로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1047">Renamed `Version` to `Name` on `PSApplicationPackage`.</span></span>
* <span data-ttu-id="5d3f2-1048">`PSResourceFile`에서 `BlobSource` 이름이 `HttpUrl`으로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1048">Renamed `BlobSource` to `HttpUrl` on `PSResourceFile`.</span></span>
* <span data-ttu-id="5d3f2-1049">`PSVirtualMachineConfiguration`에서 `OSDisk` 속성이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1049">Removed `OSDisk` property from `PSVirtualMachineConfiguration`.</span></span>
* <span data-ttu-id="5d3f2-1050">**Set-AzBatchPoolOSVersion**이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1050">Removed **Set-AzBatchPoolOSVersion**.</span></span> <span data-ttu-id="5d3f2-1051">이 작업은 더 이상 지원되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1051">This operation is no longer supported.</span></span>
* <span data-ttu-id="5d3f2-1052">`PSCloudServiceConfiguration`에서 `TargetOSVersion`이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1052">Removed `TargetOSVersion` from `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="5d3f2-1053">`PSCloudServiceConfiguration`에서 `CurrentOSVersion` 이름이 `OSVersion`으로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1053">Renamed `CurrentOSVersion` to `OSVersion` on `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="5d3f2-1054">`PSPoolUsageMetrics`에서 `DataEgressGiB` 및 `DataIngressGiB`가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1054">Removed `DataEgressGiB` and `DataIngressGiB` from `PSPoolUsageMetrics`.</span></span>
* <span data-ttu-id="5d3f2-1055">**Get-AzBatchNodeAgentSku**가 제거되고 **Get-AzBatchSupportedImage**로 대체되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1055">Removed **Get-AzBatchNodeAgentSku** and replaced it with  **Get-AzBatchSupportedImage**.</span></span>
  - <span data-ttu-id="5d3f2-1056">**Get-AzBatchSupportedImage**가 **Get-AzBatchNodeAgentSku**와 동일한 데이터를 반환하지만 더 친숙한 형식이 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1056">**Get-AzBatchSupportedImage** returns the same data as **Get-AzBatchNodeAgentSku** but in a more friendly format.</span></span>
  - <span data-ttu-id="5d3f2-1057">이제 확인되지 않은 이미지도 새롭게 반환됩니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1057">New non-verified images are also now returned.</span></span> <span data-ttu-id="5d3f2-1058">각 이미지의 `Capabilities` 및 `BatchSupportEndOfLife`에 대한 추가 정보도 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1058">Additional information about `Capabilities` and `BatchSupportEndOfLife` for each image is also included.</span></span>
* <span data-ttu-id="5d3f2-1059">**New-AzBatchPool**의 새로운 `MountConfiguration` 매개 변수를 통해 풀의 각 노드에서 원격 파일 시스템을 마운트할 수 있는 기능이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1059">Added ability to mount remote file-systems on each node of a pool via the new `MountConfiguration` parameter of **New-AzBatchPool**.</span></span>
* <span data-ttu-id="5d3f2-1060">이제 트래픽의 소스 포트를 기준으로 풀에 대한 네트워크 액세스를 차단하는 네트워크 보안 규칙이 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1060">Now support network security rules blocking network access to a pool based on the source port of the traffic.</span></span> <span data-ttu-id="5d3f2-1061">이 작업은 `PSNetworkSecurityGroupRule`에서 `SourcePortRanges` 속성을 통해 수행됩니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1061">This is done via the `SourcePortRanges` property on `PSNetworkSecurityGroupRule`.</span></span>
* <span data-ttu-id="5d3f2-1062">컨테이너를 실행할 때 Batch는 이제 컨테이너 작업 디렉터리 또는 일괄 처리 태스크 작업 디렉터리에서 작업 실행을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1062">When running a container, Batch now supports executing the task in the container working directory or in the Batch task working directory.</span></span> <span data-ttu-id="5d3f2-1063">이 작업은 `PSTaskContainerSettings`에서 `WorkingDirectory` 속성에 의해 제어됩니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1063">This is controlled by the `WorkingDirectory` property on `PSTaskContainerSettings`.</span></span>
* <span data-ttu-id="5d3f2-1064">새로운 `PublicIPs` 속성을 통해 `PSNetworkConfiguration`에서 공용 IP의 컬렉션을 지정할 수 있는 기능이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1064">Added ability to specify a collection of public IPs on `PSNetworkConfiguration` via the new `PublicIPs` property.</span></span> <span data-ttu-id="5d3f2-1065">그 결과 사용자 제공 IP 목록의 IP가 풀에 있는 노드에 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1065">This guarantees nodes in the Pool will have an IP from the list user provided IPs.</span></span>
* <span data-ttu-id="5d3f2-1066">지정하지 않은 경우 이제 `PSSTartTask`에서 `WaitForSuccess`의 기본값은 `$True`입니다(이전에는 `$False`).</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1066">When not specified, the default value of `WaitForSuccess` on `PSSTartTask` is now `$True` (was `$False`).</span></span>
* <span data-ttu-id="5d3f2-1067">지정하지 않은 경우 이제 `PSAutoUserSpecification`에서 `Scope`의 기본값은 `Pool`입니다(이전에는 Windows의 경우 `Task`, Linux의 경우에는 `Pool`).</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1067">When not specified, the default value of `Scope` on `PSAutoUserSpecification` is now `Pool` (was `Task` on Windows and `Pool` on Linux).</span></span>

#### <a name="azcdn"></a><span data-ttu-id="5d3f2-1068">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1068">Az.Cdn</span></span>
* <span data-ttu-id="5d3f2-1069">RulesEngine에 UrlRewriteAction 및 CacheKeyQueryStringAction이 도입되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1069">Introduced UrlRewriteAction and CacheKeyQueryStringAction to RulesEngine.</span></span>
* <span data-ttu-id="5d3f2-1070">New-AzDeliveryRuleCondition cmdlet에서 'Selector' 입력 누락과 같은 여러 버그가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1070">Fixed several bugs like missing 'Selector' Input in New-AzDeliveryRuleCondition cmdlet.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="5d3f2-1071">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1071">Az.Compute</span></span>
* <span data-ttu-id="5d3f2-1072">디스크 암호화 집합 기능</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1072">Disk Encryption Set feature</span></span>
    - <span data-ttu-id="5d3f2-1073">새 cmdlet:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1073">New cmdlets:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span></span>
    - <span data-ttu-id="5d3f2-1074">DiskEncryptionSetId 매개 변수가 다음 cmdlet에 추가되었습니다.   Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1074">DiskEncryptionSetId parameter is added to the following cmdlets:   Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span></span>
    - <span data-ttu-id="5d3f2-1075">DiskEncryptionSetId 및 EncryptionType 매개 변수가 다음 cmdlet에 추가되었습니다.   New-AzDiskConfig   New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1075">DiskEncryptionSetId and EncryptionType parameters are added to the following cmdlets:   New-AzDiskConfig   New-AzSnapshotConfig</span></span>
* <span data-ttu-id="5d3f2-1076">New-AzVmssIPConfig에 PublicIPAddressVersion 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1076">Add PublicIPAddressVersion parameter to New-AzVmssIPConfig</span></span>
* <span data-ttu-id="5d3f2-1077">사용자 지정 스크립트 확장의 FileUris를 공용 설정에서 보호된 설정으로 이동</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1077">Move FileUris of custom script extension from public setting to protected setting</span></span>
* <span data-ttu-id="5d3f2-1078">New-AzVmss, New-AzVmssConfig 및 Update-AzVmss cmdlet에 ScaleInPolicy 추가</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1078">Add ScaleInPolicy to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>
* <span data-ttu-id="5d3f2-1079">주요 변경 내용</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1079">Breaking changes</span></span>
    - <span data-ttu-id="5d3f2-1080">CreateOption이 업로드일 때 UploadSizeInBytes 매개 변수가 New-AzDiskConfig에 대해 DiskSizeGB 대신 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1080">UploadSizeInBytes parameter is used instead of DiskSizeGB for New-AzDiskConfig when CreateOption is Upload</span></span>
    - <span data-ttu-id="5d3f2-1081">GalleryImageVersion 개체에서 PublishingProfile.Source.ManagedImage.Id가 StorageProfile.Source.Id로 바뀝니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1081">PublishingProfile.Source.ManagedImage.Id is replaced with StorageProfile.Source.Id in GalleryImageVersion object</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="5d3f2-1082">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1082">Az.DataFactory</span></span>
* <span data-ttu-id="5d3f2-1083">ADF .Net SDK 버전을 4.3.0으로 업데이트</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1083">Update ADF .Net SDK version to 4.3.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="5d3f2-1084">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1084">Az.DataLakeStore</span></span>
* <span data-ttu-id="5d3f2-1085">ADLS SDK 버전 업데이트(https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha) , 다음 수정 사항 제공</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1085">Update ADLS SDK version (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), brings following fixes</span></span>
* <span data-ttu-id="5d3f2-1086">휴지통 또는 디렉터리 항목의 creationtime을 역직렬화할 수 없을 때 예외가 발생하지 않도록 방지합니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1086">Avoid throwing exception while unable to deserialize the creationtime of the trash or directory entry.</span></span>
* <span data-ttu-id="5d3f2-1087">adlsclient에서 요청별 시간 제한 설정 노출</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1087">Expose setting per request timeout in adlsclient</span></span>
* <span data-ttu-id="5d3f2-1088">badoffset 복구를 위한 원본 syncflag 전달 수정</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1088">Fix passing the original syncflag for badoffset recovery</span></span>
* <span data-ttu-id="5d3f2-1089">응답이 확인된 후 연속 토큰을 검색하기 위한 EnumerateDirectory 수정</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1089">Fix EnumerateDirectory to retrieve continuation token once response is checked</span></span>
* <span data-ttu-id="5d3f2-1090">Concat 버그 수정</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1090">Fix Concat Bug</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="5d3f2-1091">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1091">Az.FrontDoor</span></span>
* <span data-ttu-id="5d3f2-1092">모듈 간 기타 오타가 수정됨</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1092">Fixed miscellaneous typos across module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="5d3f2-1093">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1093">Az.HDInsight</span></span>
* <span data-ttu-id="5d3f2-1094">ADLSGen1 스토리지가 포함된 클러스터를 가져오기 위해 Get-AzHDInsightCluster를 사용할 때 고객에게 '올바른 Base-64 문자열이 아닙니다' 오류가 표시되는 버그가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1094">Fixed the bug that customer will get 'Not a valid Base-64 string' error when using Get-AzHDInsightCluster to get the cluster with ADLSGen1 storage.</span></span>
* <span data-ttu-id="5d3f2-1095">고객이 Azure Data Lake에 액세스하기 위해 서비스 주체 애플리케이션 ID를 제공할 수 있도록 세 가지 cmdlet Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig 및 New-AzHDInsightCluster에 이름이 'ApplicationId'인 매개 변수를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1095">Add a parameter named 'ApplicationId' to three cmdlets Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig and New-AzHDInsightCluster so that customer can provide the service principal application id for accessing Azure Data Lake.</span></span>
* <span data-ttu-id="5d3f2-1096">Microsoft.Azure.Management.HDInsight가 2.1.0에서 5.1.0으로 변경됨</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1096">Changed Microsoft.Azure.Management.HDInsight from 2.1.0 to 5.1.0</span></span>
* <span data-ttu-id="5d3f2-1097">다음 5가지 cmdlet이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1097">Removed five cmdlets:</span></span>
    - <span data-ttu-id="5d3f2-1098">Get-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1098">Get-AzHDInsightOMS</span></span>
    - <span data-ttu-id="5d3f2-1099">Enable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1099">Enable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="5d3f2-1100">Disable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1100">Disable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="5d3f2-1101">Grant-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1101">Grant-AzHDInsightRdpServicesAccess</span></span>
    - <span data-ttu-id="5d3f2-1102">Revoke-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1102">Revoke-AzHDInsightRdpServicesAccess</span></span>
* <span data-ttu-id="5d3f2-1103">다음 3가지 cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1103">Added three cmdlets:</span></span>
    - <span data-ttu-id="5d3f2-1104">Get-AzHDInsightOMS 대신 Get-AzHDInsightMonitoring</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1104">Get-AzHDInsightMonitoring to replace Get-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="5d3f2-1105">Get-AzHDInsightOMS 대신 Get-AzHDInsightMonitoring</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1105">Enable-AzHDInsightMonitoring to replace Enable-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="5d3f2-1106">Disable-AzHDInsightOMS 대신 Disable-AzHDInsightMonitoring</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1106">Disable-AzHDInsightMonitoring to replace Disable-AzHDInsightOMS.</span></span>
* <span data-ttu-id="5d3f2-1107">특정 위치의 기능 정보 가져오기를 지원하도록 cmdlet Get-AzHDInsightProperties가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1107">Fixed cmdlet Get-AzHDInsightProperties to support get capabilities information from a specific location.</span></span>
* <span data-ttu-id="5d3f2-1108">Add-AzHDInsightConfigValue에서 매개 변수 집합('Spark1', 'Spark2')이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1108">Removed parameter sets('Spark1', 'Spark2') from Add-AzHDInsightConfigValue.</span></span>
* <span data-ttu-id="5d3f2-1109">cmdlet Add-AzHDInsightSecurityProfile의 도움말 문서에 예제를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1109">Add examples to the help documents of cmdlet Add-AzHDInsightSecurityProfile.</span></span>
* <span data-ttu-id="5d3f2-1110">다음 cmdlet의 출력 유형이 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1110">Changed output type of the following cmdlets:</span></span>
*  - <span data-ttu-id="5d3f2-1111">Get-AzHDInsightProperties의 출력 유형이 CapabilitiesResponse에서 AzureHDInsightCapabilities로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1111">Changed the output type of Get-AzHDInsightProperties from  CapabilitiesResponse to AzureHDInsightCapabilities.</span></span>
*  - <span data-ttu-id="5d3f2-1112">Remove-AzHDInsightCluster의 출력 유형이 ClusterGetResponse에서 bool로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1112">Changed the output type of Remove-AzHDInsightCluster from ClusterGetResponse to bool.</span></span>
*  - <span data-ttu-id="5d3f2-1113">Set-AzHDInsightGatewaySettings의 출력 유형이 HttpConnectivitySettings에서 GatewaySettings로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1113">Changed the output type of Set-AzHDInsightGatewaySettings HttpConnectivitySettings to GatewaySettings.</span></span>
* <span data-ttu-id="5d3f2-1114">몇 가지 시나리오 테스트 사례가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1114">Added some scenario test cases.</span></span>
* <span data-ttu-id="5d3f2-1115">일부 별칭 제거: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1115">Remove some alias: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="5d3f2-1116">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1116">Az.IotHub</span></span>
* <span data-ttu-id="5d3f2-1117">주요 변경 내용:</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1117">Breaking changes:</span></span>
    - <span data-ttu-id="5d3f2-1118">'Add-AzIotHubEventHubConsumerGroup' cmdlet이 'EventHubEndpointName' 매개 변수를 더 이상 지원하지 않으며 원래 매개 변수 이름에 대해 별칭을 찾을 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1118">The cmdlet 'Add-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="5d3f2-1119">'Add-AzIotHubEventHubConsumerGroup' cmdlet에 대한 매개 변수 집합 '__AllParameterSets'가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1119">The parameter set '__AllParameterSets' for cmdlet 'Add-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="5d3f2-1120">'Get-AzIotHubEventHubConsumerGroup' cmdlet이 'EventHubEndpointName' 매개 변수를 더 이상 지원하지 않으며 원래 매개 변수 이름에 대해 별칭을 찾을 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1120">The cmdlet 'Get-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="5d3f2-1121">'Get-AzIotHubEventHubConsumerGroup' cmdlet에 대한 매개 변수 집합 '__AllParameterSets'가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1121">The parameter set '__AllParameterSets' for cmdlet 'Get-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="5d3f2-1122">'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' 유형의 'OperationsMonitoringProperties' 속성이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1122">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' has been removed.</span></span>
    - <span data-ttu-id="5d3f2-1123">'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' 유형의 'OperationsMonitoringProperties' 속성이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1123">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' has been removed.</span></span>
    - <span data-ttu-id="5d3f2-1124">'New-AzIotHubExportDevice' cmdlet이 더 이상 'New-AzIotHubExportDevices' 별칭을 지원하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1124">The cmdlet 'New-AzIotHubExportDevice' no longer supports the alias 'New-AzIotHubExportDevices'.</span></span>
    - <span data-ttu-id="5d3f2-1125">'New-AzIotHubImportDevice' cmdlet이 더 이상 'New-AzIotHubImportDevices' 별칭을 지원하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1125">The cmdlet 'New-AzIotHubImportDevice' no longer supports the alias 'New-AzIotHubImportDevices'.</span></span>
    - <span data-ttu-id="5d3f2-1126">'Remove-AzIotHubEventHubConsumerGroup' cmdlet이 'EventHubEndpointName' 매개 변수를 더 이상 지원하지 않으며 원래 매개 변수 이름에 대해 별칭을 찾을 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1126">The cmdlet 'Remove-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="5d3f2-1127">'Remove-AzIotHubEventHubConsumerGroup' cmdlet에 대한 매개 변수 집합 '__AllParameterSets'가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1127">The parameter set '__AllParameterSets' for cmdlet 'Remove-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="5d3f2-1128">'Set-AzIotHub' cmdlet이 'OperationsMonitoringProperties' 매개 변수를 더 이상 지원하지 않으며 원래 매개 변수 이름에 대해 별칭을 찾을 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1128">The cmdlet 'Set-AzIotHub' no longer supports the parameter 'OperationsMonitoringProperties' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="5d3f2-1129">'Set-AzIotHub' cmdlet에 대한 매개 변수 집합 'UpdateOperationsMonitoringProperties'가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1129">The parameter set 'UpdateOperationsMonitoringProperties' for cmdlet 'Set-AzIotHub' has been removed.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="5d3f2-1130">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1130">Az.RecoveryServices</span></span>
* <span data-ttu-id="5d3f2-1131">Azure Site Recovery가 Azure-Azure를 위한 NSG, 공용 IP 및 내부 부하 분산 장치와 같은 네트워킹 리소스 구성을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1131">Azure Site Recovery support to configure networking resources like NSG, public IP and internal load balancers for Azure to Azure.</span></span>
* <span data-ttu-id="5d3f2-1132">Azure Site Recovery가 vMWare-Azure를 위한 관리 디스크에 쓰기를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1132">Azure Site Recovery Support to write to managed disk for vMWare to Azure.</span></span>
* <span data-ttu-id="5d3f2-1133">Azure Site Recovery가 vMWare-Azure를 위한 NIC 감소를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1133">Azure Site Recovery Support to NIC reduction for vMWare to Azure.</span></span>
* <span data-ttu-id="5d3f2-1134">Azure Site Recovery가 Azure-Azure를 위한 가속 네트워킹을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1134">Azure Site Recovery Support to accelerated networking for Azure to Azure.</span></span>
* <span data-ttu-id="5d3f2-1135">Azure Site Recovery가 Azure-Azure를 위한 에이전트 자동 업데이트를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1135">Azure Site Recovery Support to agent auto update for Azure to Azure.</span></span>
* <span data-ttu-id="5d3f2-1136">Azure Site Recovery가 Azure-Azure를 위한 표준 SSD를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1136">Azure Site Recovery Support to Standard SSD for Azure to Azure.</span></span>
* <span data-ttu-id="5d3f2-1137">Azure Site Recovery가 Azure-Azure를 위한 두 가지 Azure 디스크 암호화 전달을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1137">Azure Site Recovery Support to Azure Disk Encryption two pass for Azure to Azure.</span></span>
* <span data-ttu-id="5d3f2-1138">Azure Site Recovery가 Azure-Azure를 위한 새로 추가된 디스크 보호를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1138">Azure Site Recovery Support to protect newly added disk for Azure to Azure.</span></span>
* <span data-ttu-id="5d3f2-1139">VM을 위한 SoftDelete 기능 및 softdelete를 위한 테스트가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1139">Added SoftDelete feature for VM and added tests for softdelete</span></span>

#### <a name="azresources"></a><span data-ttu-id="5d3f2-1140">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1140">Az.Resources</span></span>
* <span data-ttu-id="5d3f2-1141">종속성 어셈블리 Microsoft.Extensions.Caching.Memory가 1.1.1에서 2.2로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1141">Update dependency assembly Microsoft.Extensions.Caching.Memory from 1.1.1 to 2.2</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="5d3f2-1142">Az.Network</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1142">Az.Network</span></span>
* <span data-ttu-id="5d3f2-1143">일반 서비스 공급자 지원을 위해 PrivateEndpointConnection에 대한 모든 cmdlet이 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1143">Change all cmdlets for PrivateEndpointConnection to support generic service provider.</span></span>
    - <span data-ttu-id="5d3f2-1144">업데이트된 cmdlet:</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1144">Updated cmdlet:</span></span>
        - <span data-ttu-id="5d3f2-1145">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1145">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="5d3f2-1146">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1146">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="5d3f2-1147">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1147">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="5d3f2-1148">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1148">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="5d3f2-1149">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1149">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="5d3f2-1150">PrivateLinkResource에 대한 새 cmdlet이 추가되었고 일반 서비스 공급자도 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1150">Add new cmdlet for PrivateLinkResource and it also support generic service provider.</span></span>
    - <span data-ttu-id="5d3f2-1151">새 cmdlet:</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1151">New cmdlet:</span></span>
        - <span data-ttu-id="5d3f2-1152">Get-AzPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1152">Get-AzPrivateLinkResource</span></span>
* <span data-ttu-id="5d3f2-1153">Proxy Protocol V2 기능에 대한 새 필드 및 매개 변수가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1153">Add new fields and parameter for the feature Proxy Protocol V2.</span></span>
    - <span data-ttu-id="5d3f2-1154">PrivateLinkService에서 EnableProxyProtocol 속성 추가</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1154">Add property EnableProxyProtocol in PrivateLinkService</span></span>
    - <span data-ttu-id="5d3f2-1155">PrivateEndpointConnection에서 LinkIdentifier 속성 추가</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1155">Add property LinkIdentifier in PrivateEndpointConnection</span></span>
    - <span data-ttu-id="5d3f2-1156">새로운 선택적인 매개 변수인 EnableProxyProtocol을 추가하도록 New-AzPrivateLinkService가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1156">Updated New-AzPrivateLinkService to add a new optional parameter EnableProxyProtocol.</span></span>
* <span data-ttu-id="5d3f2-1157">'New-AzApplicationGatewaySku' 참조 설명서의 잘못된 매개 변수 설명 수정</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1157">Fix incorrect parameter description in 'New-AzApplicationGatewaySku' reference documentation</span></span>
* <span data-ttu-id="5d3f2-1158">Azure 방화벽 정책을 지원하는 새로운 cmdlet</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1158">New cmdlets to support the azure firewall policy</span></span>
* <span data-ttu-id="5d3f2-1159">VirtualHub의 자식 리소스 RouteTables에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1159">Add support for child resource RouteTables of VirtualHub</span></span>
    - <span data-ttu-id="5d3f2-1160">추가된 새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1160">New cmdlets added:</span></span>
        - <span data-ttu-id="5d3f2-1161">Add-AzVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1161">Add-AzVirtualHubRoute</span></span>
        - <span data-ttu-id="5d3f2-1162">Add-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1162">Add-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="5d3f2-1163">Get-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1163">Get-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="5d3f2-1164">Remove-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1164">Remove-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="5d3f2-1165">Set-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1165">Set-AzVirtualHub</span></span>
* <span data-ttu-id="5d3f2-1166">VirtualHub의 새로운 속성 Sku 및 VirtualWan의 VirtualWANType에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1166">Add support for new properties Sku of VirtualHub and VirtualWANType of VirtualWan</span></span>
    - <span data-ttu-id="5d3f2-1167">선택적 매개 변수로 다음 cmdlet이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1167">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="5d3f2-1168">New-AzVirtualHub: 추가된 매개 변수 Sku</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1168">New-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="5d3f2-1169">Update-AzVirtualHub: 추가된 매개 변수 Sku</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1169">Update-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="5d3f2-1170">New-AzVirtualWan: 추가된 매개 변수 VirtualWANType</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1170">New-AzVirtualWan : added parameter VirtualWANType</span></span>
        - <span data-ttu-id="5d3f2-1171">Update-AzVirtualWan: 추가된 매개 변수 VirtualWANType</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1171">Update-AzVirtualWan : added parameter VirtualWANType</span></span>
* <span data-ttu-id="5d3f2-1172">HubVnetConnection, VpnConnection 및 ExpressRouteConnection에 대한 EnableInternetSecurity 속성 지원 추가</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1172">Add support for EnableInternetSecurity property for HubVnetConnection, VpnConnection and ExpressRouteConnection</span></span>
    - <span data-ttu-id="5d3f2-1173">추가된 새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1173">New cmdlets added:</span></span>
        - <span data-ttu-id="5d3f2-1174">Update-AzureRmVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1174">Update-AzureRmVirtualHubVnetConnection</span></span>
    - <span data-ttu-id="5d3f2-1175">선택적 매개 변수로 다음 cmdlet이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1175">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="5d3f2-1176">New-AzureRmVirtualHubVnetConnection: 추가된 매개 변수 EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1176">New-AzureRmVirtualHubVnetConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="5d3f2-1177">New-AzureRmVpnConnection: 추가된 매개 변수 EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1177">New-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="5d3f2-1178">Update-AzureRmVpnConnection: 추가된 매개 변수 EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1178">Update-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="5d3f2-1179">New-AzureRmExpressRouteConnection: 추가된 매개 변수 EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1179">New-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="5d3f2-1180">Set-AzureRmExpressRouteConnection: 추가된 매개 변수 EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1180">Set-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
* <span data-ttu-id="5d3f2-1181">TopLevel WebApplicationFirewall 정책 구성을 위한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1181">Add support for Configuring TopLevel WebApplicationFirewall Policy</span></span>
    - <span data-ttu-id="5d3f2-1182">추가된 새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1182">New cmdlets added:</span></span>
        - <span data-ttu-id="5d3f2-1183">New-AzApplicationGatewayFirewallPolicySetting</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1183">New-AzApplicationGatewayFirewallPolicySetting</span></span>
        - <span data-ttu-id="5d3f2-1184">New-AzApplicationGatewayFirewallPolicyExclusion</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1184">New-AzApplicationGatewayFirewallPolicyExclusion</span></span>
        - <span data-ttu-id="5d3f2-1185">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1185">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span></span>
        - <span data-ttu-id="5d3f2-1186">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1186">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span></span>
        - <span data-ttu-id="5d3f2-1187">New-AzApplicationGatewayFirewallPolicyManagedRule</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1187">New-AzApplicationGatewayFirewallPolicyManagedRule</span></span>
        - <span data-ttu-id="5d3f2-1188">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1188">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span></span>
    - <span data-ttu-id="5d3f2-1189">선택적 매개 변수로 다음 cmdlet이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1189">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="5d3f2-1190">New-AzApplicationGatewayFirewallPolicy: 추가된 매개 변수 PolicySetting, ManagedRule</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1190">New-AzApplicationGatewayFirewallPolicy : added parameter PolicySetting, ManagedRule</span></span>
* <span data-ttu-id="5d3f2-1191">CustomRule에서 Geo-Match 연산자를 위한 지원 추가됨</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1191">Added support for Geo-Match operator on CustomRule</span></span>
    - <span data-ttu-id="5d3f2-1192">FirewallCondition에서 연산자에 GeoMatch 추가됨</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1192">Added GeoMatch to the operator on the FirewallCondition</span></span>
* <span data-ttu-id="5d3f2-1193">perListener 및 perSite 방화벽 규칙에 대한 지원 추가됨</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1193">Added support for perListener and perSite Firewall policy</span></span>
    - <span data-ttu-id="5d3f2-1194">선택적 매개 변수로 다음 cmdlet이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1194">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="5d3f2-1195">New-AzApplicationGatewayHttpListener: 추가된 매개 변수 FirewallPolicy, FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1195">New-AzApplicationGatewayHttpListener : added parameter FirewallPolicy, FirewallPolicyId</span></span>
        - <span data-ttu-id="5d3f2-1196">New-AzApplicationGatewayPathRuleConfig: 추가된 매개 변수 FirewallPolicy, FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1196">New-AzApplicationGatewayPathRuleConfig : added parameter FirewallPolicy, FirewallPolicyId</span></span>
* <span data-ttu-id="5d3f2-1197">'PSBastion'에서 이름이 AzureBastionSubnet인 필수 서브넷의 수정은 대소문자를 구분하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1197">Fix required subnet with name AzureBastionSubnet in 'PSBastion' can be case insensitive</span></span>
* <span data-ttu-id="5d3f2-1198">Azure Firewall을 위한 네트워크 규칙의 대상 FQDN 및 NAT 규칙의 번역된 FQDN 지원</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1198">Support for Destination FQDNs in Network Rules and Translated FQDN in NAT Rules for Azure Firewall</span></span>
* <span data-ttu-id="5d3f2-1199">IpGroup의 최상위 리소스 RouteTables에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1199">Add support for top level resource RouteTables of IpGroup</span></span>
    - <span data-ttu-id="5d3f2-1200">추가된 새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1200">New cmdlets added:</span></span>
        - <span data-ttu-id="5d3f2-1201">New-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1201">New-AzIpGroup</span></span>
        - <span data-ttu-id="5d3f2-1202">Remove-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1202">Remove-AzIpGroup</span></span>
        - <span data-ttu-id="5d3f2-1203">Get-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1203">Get-AzIpGroup</span></span>
        - <span data-ttu-id="5d3f2-1204">Set-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1204">Set-AzIpGroup</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="5d3f2-1205">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1205">Az.ServiceFabric</span></span>
* <span data-ttu-id="5d3f2-1206">Add-AzVmssSecret에서 지원되기 때문에 Add-AzServiceFabricApplicationCertificate cmdlet이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1206">Remove Add-AzServiceFabricApplicationCertificate cmdlet as this scenario is covered by Add-AzVmssSecret.</span></span>

#### <a name="azsql"></a><span data-ttu-id="5d3f2-1207">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1207">Az.Sql</span></span>
* <span data-ttu-id="5d3f2-1208">Managed Instances에서 삭제된 데이터베이스의 복원을 위한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1208">Added support for restore of dropped databases on Managed Instances.</span></span>
* <span data-ttu-id="5d3f2-1209">이전의 감사 cmdlet 코드가 사용되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1209">Deprecated from code old auditing cmdlets.</span></span>
* <span data-ttu-id="5d3f2-1210">사용되지 않는 별칭이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1210">Removed deprecated aliases:</span></span>
* <span data-ttu-id="5d3f2-1211">Get-AzSqlDatabaseIndexRecommendations(대신 Get-AzSqlDatabaseIndexRecommendation 사용)</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1211">Get-AzSqlDatabaseIndexRecommendations (use Get-AzSqlDatabaseIndexRecommendation instead)</span></span>
* <span data-ttu-id="5d3f2-1212">Get-AzSqlDatabaseRestorePoints(대신 Get-AzSqlDatabaseRestorePoint 사용)</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1212">Get-AzSqlDatabaseRestorePoints (use Get-AzSqlDatabaseRestorePoint instead)</span></span>
* <span data-ttu-id="5d3f2-1213">Get-AzSqlDatabaseSecureConnectionPolicy cmdlet 제거</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1213">Remove Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="5d3f2-1214">사용되지 않는 취약성 평가 설정 cmdlet에 대한 별칭 제거</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1214">Remove aliases for deprecated Vulnerability Assessment Settings cmdlets</span></span>
* <span data-ttu-id="5d3f2-1215">지능형 위협 탐지 설정 cmdlet 사용 중단</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1215">Deprecate Advanced Threat Detection Settings cmdlets</span></span>
* <span data-ttu-id="5d3f2-1216">데이터베이스의 열에 대한 민감도 권장 사항의 사용 여부를 제어하는 cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1216">Adding cmdlets to Disable and enable sensitivity recommendations on columns in a database.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="5d3f2-1217">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1217">Az.Storage</span></span>
* <span data-ttu-id="5d3f2-1218">스토리지 계정을 만들거나 업데이트할 때 큰 파일 공유 사용 지원</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1218">Support enable Large File share when create or update Storage account</span></span>
    -  <span data-ttu-id="5d3f2-1219">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1219">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="5d3f2-1220">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1220">Set-AzStorageAccount</span></span>
* <span data-ttu-id="5d3f2-1221">파일 핸들을 닫거나/가져올 때, DeletePending 상태의 개체로 인한 오류를 방지하기 위해 입력 경로가 파일 디렉터리인지 또는 파일인지를 확인하는 과정을 건너뜁니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1221">When close/get File handle, skip check the input path is File directory or File, to avoid failure with object in DeletePending status</span></span>
    -  <span data-ttu-id="5d3f2-1222">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1222">Get-AzStorageFileHandle</span></span>
    -  <span data-ttu-id="5d3f2-1223">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1223">Close-AzStorageFileHandle</span></span>

## <a name="280---october-2019"></a><span data-ttu-id="5d3f2-1224">2.8.0 - 2019년 10월</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1224">2.8.0 - October 2019</span></span>
### <a name="general"></a><span data-ttu-id="5d3f2-1225">일반</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1225">General</span></span>
* <span data-ttu-id="5d3f2-1226">Az.HealthcareApis 1.0.0 릴리스</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1226">Az.HealthcareApis 1.0.0 release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="5d3f2-1227">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1227">Az.Accounts</span></span>
* <span data-ttu-id="5d3f2-1228">생성된 모듈에 대한 원격 분석 및 URL 다시 작성이 업데이트되고, Windows 단위 테스트가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1228">Update telemetry and url rewriting for generated modules, fix windows unit tests.</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="5d3f2-1229">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1229">Az.ApiManagement</span></span>
* <span data-ttu-id="5d3f2-1230">**Set-AzApiManagementApi** - API 업데이트 지원이 ApiVersionSet에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1230">**Set-AzApiManagementApi** - Added support for Updating Api into ApiVersionSet</span></span>
    - <span data-ttu-id="5d3f2-1231">문제 https://github.com/Azure/azure-powershell/issues/10068 수정</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1231">Fix for issue https://github.com/Azure/azure-powershell/issues/10068</span></span>

#### <a name="azautomation"></a><span data-ttu-id="5d3f2-1232">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1232">Az.Automation</span></span>
* <span data-ttu-id="5d3f2-1233">Linux 다시 부팅 설정 매개 변수에 대한 New-AzureAutomationSoftwareUpdateConfiguration cmdlet이 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1233">Fixed New-AzureAutomationSoftwareUpdateConfiguration cmdlet for Linux reboot setting parameter.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="5d3f2-1234">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1234">Az.Batch</span></span>
* <span data-ttu-id="5d3f2-1235">**Get-AzBatchNodeAgentSku**가 더 이상 사용되지 않으며, 2.0.0 버전의 **Get-AzBatchSupportImage**로 대체되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1235">**Get-AzBatchNodeAgentSku** is deprecated and will be replaced by **Get-AzBatchSupportImage** in version 2.0.0.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="5d3f2-1236">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1236">Az.Compute</span></span>
* <span data-ttu-id="5d3f2-1237">Priority, EvictionPolicy 및 MaxPrice 매개 변수가 New-AzVM 및 New-AzVmss cmdlet에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1237">Add Priority, EvictionPolicy, and MaxPrice parameters to New-AzVM and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="5d3f2-1238">Add-AzVMAdditionalUnattendContent 및 Add-AzVMSshPublicKey cmdlet에 대한 경고 메시지와 도움말 문서가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1238">Fix warning message and help document for Add-AzVMAdditionalUnattendContent and Add-AzVMSshPublicKey cmdlets</span></span>
* <span data-ttu-id="5d3f2-1239">Set-AzVMDiskEncryptionExtension의 관리 디스크가 있는 Linux VM에 대한 -skipVmBackup 예외가 해결되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1239">Fix -skipVmBackup exception for Linux VMs with managed disks for Set-AzVMDiskEncryptionExtension.</span></span>
* <span data-ttu-id="5d3f2-1240">Set-AzVMDiskEncryptionExtension의 두 가지 패스 시나리오에서 발생하는 암호화 설정 업데이트의 버그가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1240">Fix bug in update encryption settings in Set-AzVMDiskEncryptionExtension, two pass scenario.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="5d3f2-1241">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1241">Az.DataFactory</span></span>
* <span data-ttu-id="5d3f2-1242">ADF V2 데이터 흐름에 대한 CRUD 명령으로 Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow 및 Get-AzDataFactoryV2DataFlow가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1242">Adding CRUD commands for ADF V2 data flow: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow, and Get-AzDataFactoryV2DataFlow.</span></span>
* <span data-ttu-id="5d3f2-1243">ADF V2 데이터 흐름 디버그 세션에 대한 작업 명령으로 Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand 및 Stop-AzDataFactoryV2DataFlowDebugSession이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1243">Adding action commands for ADF V2 data flow debug Session: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand and Stop-AzDataFactoryV2DataFlowDebugSession.</span></span>
* <span data-ttu-id="5d3f2-1244">ADF .Net SDK 버전이 4.2.0으로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1244">Update ADF .Net SDK version to 4.2.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="5d3f2-1245">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1245">Az.DataLakeStore</span></span>
* <span data-ttu-id="5d3f2-1246">도메인 없이 '-'가 있는 계정을 전달할 수 있도록 계정 유효성 검사가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1246">Fix account validation so that accounts with '-' can be passed without domain</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="5d3f2-1247">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1247">Az.HealthcareApis</span></span>
* <span data-ttu-id="5d3f2-1248">PowerShell 버전이 1.0.0으로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1248">Updated the powershell version to 1.0.0</span></span>
* <span data-ttu-id="5d3f2-1249">SDK 버전이 1.0.2로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1249">Updated the SDK version to 1.0.2</span></span>
* <span data-ttu-id="5d3f2-1250">새 SDK 버전을 참조하도록 테스트가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1250">Update in tests to refer to new SDK version</span></span>
* <span data-ttu-id="5d3f2-1251">출력이 중첩 구조에서 평면화 구조로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1251">Updated the output structure from nested to flattened.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="5d3f2-1252">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1252">Az.IotHub</span></span>
* <span data-ttu-id="5d3f2-1253">새 라우팅 원본 추가: DigitalTwinChangeEvents</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1253">Add new routing source: DigitalTwinChangeEvents</span></span>
* <span data-ttu-id="5d3f2-1254">사소한 버그 수정: Get-AzIothub에서 subscriptionId를 반환하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1254">Minor bug fix: Get-AzIothub not returning subscriptionId</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="5d3f2-1255">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1255">Az.Monitor</span></span>
* <span data-ttu-id="5d3f2-1256">작업 그룹에 대한 새 작업 그룹 수신기로 -ItsmReceiver, -VoiceReceiver, -ArmRoleReceiver, -AzureFunctionReceiver, -LogicAppReceiver, -AutomationRunbookReceiver, -AzureAppPushReceiver가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1256">New action group receivers added for action group   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span></span>
* <span data-ttu-id="5d3f2-1257">수신기에 사용하도록 설정된 일반 경고 스키마가 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1257">Use common alert schema enabled for the receivers.</span></span> <span data-ttu-id="5d3f2-1258">SMS, Azure 앱 푸시, ITSM 및 음성 수신기에는 적용되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1258">This is not applicable for SMS, Azure App push , ITSM and Voice recievers</span></span>
* <span data-ttu-id="5d3f2-1259">웹후크에서 이제 Azure Active Directory 인증을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1259">Webhooks now supports Azure active directory authentication .</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="5d3f2-1260">Az.Network</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1260">Az.Network</span></span>
* <span data-ttu-id="5d3f2-1261">서비스 엔드포인트 정책에 사용할 수 있는 별칭을 가져오기 위해 호출할 수 있는 새 Get-AzAvailableServiceAlias cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1261">Add new cmdlet Get-AzAvailableServiceAlias which can be called to get the aliases that can be used for Service Endpoint Policies.</span></span>
* <span data-ttu-id="5d3f2-1262">트래픽 선택기를 Virtual Network 게이트웨이 연결에 추가할 수 있는 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1262">Added support for the adding traffic selectors to Virtual Network Gateway Connections</span></span>
    - <span data-ttu-id="5d3f2-1263">추가된 새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1263">New cmdlets added:</span></span>
        - <span data-ttu-id="5d3f2-1264">New-AzureRmTrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1264">New-AzureRmTrafficSelectorPolicy</span></span>
    - <span data-ttu-id="5d3f2-1265">cmdlet이 선택적인 -TrafficSelectorPolicies, -New-AzureRmVirtualNetworkGatewayConnection, -Set-AzureRmVirtualNetworkGatewayConnection 매개 변수로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1265">Cmdlets updated with optional parameter -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="5d3f2-1266">ESP 및 AH 프로토콜 지원이 네트워크 보안 규칙 구성에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1266">Add support for ESP and AH protocols in network security rule configurations</span></span>
    - <span data-ttu-id="5d3f2-1267">다음 Cmdlet이 업데이트 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1267">Updated cmdlets:</span></span>
        - <span data-ttu-id="5d3f2-1268">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1268">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="5d3f2-1269">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1269">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="5d3f2-1270">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1270">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="5d3f2-1271">Cortex cmdlet의 예외 처리가 향상되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1271">Improve handling of exceptions in Cortex cmdlets</span></span>
* <span data-ttu-id="5d3f2-1272">새 VirtualNetworkGateways 세대 및 SKU</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1272">New Generations and SKUs for VirtualNetworkGateways</span></span>
  - <span data-ttu-id="5d3f2-1273">새 VirtualNetworkGateways 세대가 도입되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1273">Introduce new Generations for VirtualNetworkGateways.</span></span>
  - <span data-ttu-id="5d3f2-1274">높은 처리량의 새 VirtualNetworkGateways SKU가 도입되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1274">Introduce new high throughput SKUs for VirtualNetworkGateways.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="5d3f2-1275">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1275">Az.RedisCache</span></span>
* <span data-ttu-id="5d3f2-1276">'-Size' 매개 변수에 대한 누락 값을 포함하도록 'Set-AzRedisCache' 참조 설명서가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1276">Updated 'Set-AzRedisCache' reference documentation to include missing values for '-Size' parameter</span></span>

#### <a name="azsql"></a><span data-ttu-id="5d3f2-1277">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1277">Az.Sql</span></span>
* <span data-ttu-id="5d3f2-1278">Managed Instance에서 Active Directory 관리자를 설정할 수 있는 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1278">Add support for setting Active Directory Administrator on Managed Instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="5d3f2-1279">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1279">Az.Storage</span></span>
* <span data-ttu-id="5d3f2-1280">스토리지 클라이언트 라이브러리가 11.1.0으로 업그레이드되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1280">Upgrade Storage Client Library to 11.1.0</span></span>
* <span data-ttu-id="5d3f2-1281">관리 평면 API를 사용하여 컨테이너를 나열하면 NextPageLink를 통해 나열됩니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1281">List containers with Management plane API, will list with NextPageLink</span></span>
    -  <span data-ttu-id="5d3f2-1282">Get-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1282">Get-AzRmStorageContainer</span></span>
* <span data-ttu-id="5d3f2-1283">구독에서 스토리지 계정을 나열하면 NextPageLink를 통해 나열됩니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1283">List Storage accounts from subscription, will list with NextPageLink</span></span>
    -  <span data-ttu-id="5d3f2-1284">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1284">Get-AzStorageAccount</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="5d3f2-1285">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1285">Az.StorageSync</span></span>
* <span data-ttu-id="5d3f2-1286">Reset-AzStorageSyncServerCertificate의 9810 문제가 해결되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1286">Fix Issue 9810 in Reset-AzStorageSyncServerCertificate.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="5d3f2-1287">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1287">Az.Websites</span></span>
* <span data-ttu-id="5d3f2-1288">앱의 ASP를 업데이트하는 Set-AzWebApp이 실패했습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1288">Set-AzWebApp updating ASP of an app was failing</span></span>

## <a name="270---september-2019"></a><span data-ttu-id="5d3f2-1289">2.7.0 - 2019년 9월</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1289">2.7.0 - September 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="5d3f2-1290">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1290">Az.ApiManagement</span></span>
* <span data-ttu-id="5d3f2-1291">'Set-AzApiManagementPolicy' 참조 설명서에서 '-Format' 매개 변수 설명이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1291">Update '-Format' parameter description in 'Set-AzApiManagementPolicy' reference documentation</span></span>
* <span data-ttu-id="5d3f2-1292">참조 설명서에서 사용되지 않는 cmdlet 'Update-AzApiManagementDeployment'의 참조를 제거했습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1292">Removed references of deprecated cmdlet 'Update-AzApiManagementDeployment' from reference documentation.</span></span> <span data-ttu-id="5d3f2-1293">그 대신 'Set-AzApiManagement'를 사용하세요.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1293">Use 'Set-AzApiManagement' instead.</span></span>

#### <a name="azautomation"></a><span data-ttu-id="5d3f2-1294">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1294">Az.Automation</span></span>
* <span data-ttu-id="5d3f2-1295">'Register-AzAutomationDscNode'에 대한 참조 설명서의 예제 오타가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1295">Fixed example typo in reference documentation for 'Register-AzAutomationDscNode'</span></span>
* <span data-ttu-id="5d3f2-1296">Register-AzAutomationDSCNode에 OS 제한에 대한 설명이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1296">Added clarification on OS restriction to Register-AzAutomationDSCNode</span></span>
* <span data-ttu-id="5d3f2-1297">-Wait 옵션에 대한 Start-AzAutomationRunbook cmdlet Null 참조 예외가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1297">Fixed Start-AzAutomationRunbook cmdlet Null reference exception for -Wait option.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="5d3f2-1298">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1298">Az.Compute</span></span>
* <span data-ttu-id="5d3f2-1299">New-AzDiskConfig에 UploadSizeInBytes 매개 변수가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1299">Add UploadSizeInBytes parameter tp New-AzDiskConfig</span></span>
* <span data-ttu-id="5d3f2-1300">New-AzSnapshotConfig에 증분 매개 변수가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1300">Add Incremental parameter to New-AzSnapshotConfig</span></span>
* <span data-ttu-id="5d3f2-1301">다음과 같은 낮은 우선 순위의 가상 머신 기능이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1301">Add a low priority virtual machine feature:</span></span>
    - <span data-ttu-id="5d3f2-1302">MaxPrice, EvictionPolicy 및 Priority 매개 변수가 New-AzVMConfig에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1302">MaxPrice, EvictionPolicy and Priority parameters are added to New-AzVMConfig.</span></span>
    - <span data-ttu-id="5d3f2-1303">MaxPrice 매개 변수는 New-AzVmssConfig, Update-AzVM 및 Update-AzVmss cmdlet에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1303">MaxPrice parameter is added to New-AzVmssConfig, Update-AzVM and Update-AzVmss cmdlets.</span></span>
* <span data-ttu-id="5d3f2-1304">구독의 모든 가용성 세트를 나열할 때 발생하는 Get-AzAvailabilitySet cmdlet에 대한 VM 참조 이슈가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1304">Fix VM reference issue for Get-AzAvailabilitySet cmdlet when it lists all availability sets in the subscription.</span></span>
* <span data-ttu-id="5d3f2-1305">Get-AzRemoteDesktopFile에 대한 null 예외가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1305">Fix the null exception for Get-AzRemoteDesktopFile.</span></span>
* <span data-ttu-id="5d3f2-1306">종료 상대 위치에 대한 VHD 검색 메서드가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1306">Fix VHD Seek method for end-relative position.</span></span>
* <span data-ttu-id="5d3f2-1307">New-AzVM 및 Update-AzVM에 대한 UltraSSD 이슈가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1307">Fix UltraSSD issue for New-AzVM and Update-AzVM.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="5d3f2-1308">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1308">Az.DataFactory</span></span>
* <span data-ttu-id="5d3f2-1309">ADF V2에 대한 3가지 새 명령 Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription 및 Get-AzDataFactoryV2TriggerSubscriptionStatus가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1309">Adding 3 new commands for ADF V2 - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription, and Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>
* <span data-ttu-id="5d3f2-1310">ADF .Net SDK 버전이 4.1.3으로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1310">Updated ADF .Net SDK version to 4.1.3</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="5d3f2-1311">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1311">Az.HDInsight</span></span>
* <span data-ttu-id="5d3f2-1312">호출 주요 변경 내용</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1312">Call out breaking changes</span></span>

#### <a name="aziothub"></a><span data-ttu-id="5d3f2-1313">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1313">Az.IotHub</span></span>
* <span data-ttu-id="5d3f2-1314">지역 쌍 재해 복구 지역에 IotHub에 대한 장애 조치(failover) 호출 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1314">Add support to invoke failover for an IotHub to the geo-paired disaster recovery region.</span></span>
* <span data-ttu-id="5d3f2-1315">IotHub에 대한 메시지 보강 관리 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1315">Add support to manage message enrichment for an IotHub.</span></span> <span data-ttu-id="5d3f2-1316">새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1316">New cmdlets are:</span></span>
    - <span data-ttu-id="5d3f2-1317">Add-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1317">Add-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="5d3f2-1318">Get-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1318">Get-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="5d3f2-1319">Remove-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1319">Remove-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="5d3f2-1320">Set-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1320">Set-AzIotHubMessageEnrichment</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="5d3f2-1321">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1321">Az.Monitor</span></span>
* <span data-ttu-id="5d3f2-1322">최신 모니터링 SDK, 즉, 0.24.1-preview를 가리킵니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1322">Pointing to the most recent Monitor SDK, i.e. 0.24.1-preview</span></span>
   - <span data-ttu-id="5d3f2-1323">메트릭 cmdlet에 줄 바꿈하지 않는 변경 내용을 추가합니다. 즉, 단위 열거형은 여러 새 값을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1323">Adds non-braking changes to the Metrics cmdlets, i.e. the Unit enumeration supports several new values.</span></span> <span data-ttu-id="5d3f2-1324">이러한 cmdlet은 읽기 전용이므로 cmdlet 입력이 변경되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1324">These are read-only cmdlets, so there would be no change in the input of the cmdlets.</span></span>
   - <span data-ttu-id="5d3f2-1325">이제 **ActionGroups** 요청의 api 버전은 **2019-06-01**이고, 이전에는 **2018-03-01**였습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1325">The api-version of the **ActionGroups** requests is now **2019-06-01**, before it was **2018-03-01**.</span></span> <span data-ttu-id="5d3f2-1326">시나리오 테스트가 이 변경 내용에 맞게 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1326">The scenario tests have been updated to accommodate for this change.</span></span>
   - <span data-ttu-id="5d3f2-1327">**EmailReceiver** 및 **WebhookReceiver** 클래스에 대한 생성자가 새 필수 인수, 즉, **useCommonAlertSchema**라는 부울 값을 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1327">The constructors for the classes **EmailReceiver** and **WebhookReceiver** added one new mandatory argument, i.e. a Boolean value called **useCommonAlertSchema**.</span></span> <span data-ttu-id="5d3f2-1328">현재 이 값은 cmdlet의 주요 변경 사항을 숨기도록 **false**로 고정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1328">Currently, the value is fixed to **false** to hide this breaking change from the cmdlets.</span></span> <span data-ttu-id="5d3f2-1329">**참고**: 이 변경 사항은 경고 팀에서 유효성을 검사해야 하는 임시 변경 내용입니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1329">**NOTE**: this is a temporary change that must be validated by the Alerts team.</span></span>
   - <span data-ttu-id="5d3f2-1330">이전 SDK에서 변경된 **Source** 클래스(**ScheduledQueryRuleSource** 클래스와 관련됨)의 생성자에 대한 인수 순서입니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1330">The order of the arguments for the constructor of the class **Source** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="5d3f2-1331">이번 변화로 인해 두 개의 단위 테스트를 수정해야 했습니다. 즉, 두 단위 테스트가 컴파일되었지만 테스트를 통과하지 못했습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1331">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
   - <span data-ttu-id="5d3f2-1332">이전 SDK에서 변경된 **AlertingAction** 클래스(**ScheduledQueryRuleSource** 클래스와 관련됨)의 생성자에 대한 인수 순서입니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1332">The order of the arguments for the constructor of the class **AlertingAction** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="5d3f2-1333">이번 변화로 인해 두 개의 단위 테스트를 수정해야 했습니다. 즉, 두 단위 테스트가 컴파일되었지만 테스트를 통과하지 못했습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1333">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
* <span data-ttu-id="5d3f2-1334">메트릭 경고 V2에 대한 동적 임계값 기준 지원</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1334">Support Dynamic Threshold criteria for metric alert V2</span></span>
    - <span data-ttu-id="5d3f2-1335">AzMetricAlertRuleV2Criteria: 이제 동적 임계값 조건도 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1335">New-AzMetricAlertRuleV2Criteria: now creats dynamic threshold criteria also</span></span>
    - <span data-ttu-id="5d3f2-1336">Add-AzMetricAlertRuleV2: 이제 동적 임계값 조건도 수락합니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1336">Add-AzMetricAlertRuleV2: now accept dynamic threshold criteria also</span></span>
* <span data-ttu-id="5d3f2-1337">SQR(예약된 쿼리 규칙)의 향상된 기능</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1337">Improvements in Scheduled Query Rule cmdlets (SQR)</span></span>
 - <span data-ttu-id="5d3f2-1338">Cmdlet이 'Location' 매개 변수를 두 가지 형식(eastus 같은 위치 또는 미국 동부 같은 위치 표시 이름)으로 모두 허용합니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1338">Cmdlets will accept 'Location' paramater in both formats, either the location (e.g. eastus) or the location display name (e.g. East US)</span></span>
 - <span data-ttu-id="5d3f2-1339">도움말 파일에 적절하게 표시된 'Enabled' 매개 변수</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1339">Illustrated 'Enabled' parameter in help files properly</span></span>
 - <span data-ttu-id="5d3f2-1340">선택적 매개 변수 'ActionGroup'에 대한 예제가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1340">Added examples for 'ActionGroup' optional parameter</span></span>
 - <span data-ttu-id="5d3f2-1341">도움말 파일이 전체적으로 개선되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1341">Overall improved help files</span></span>
* <span data-ttu-id="5d3f2-1342">'Set-AzActionRule'의 범위 유형 결정 버그를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1342">Fix bug in determining scope type for 'Set-AzActionRule'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="5d3f2-1343">Az.Network</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1343">Az.Network</span></span>
* <span data-ttu-id="5d3f2-1344">'New-AzApplicationGateway' 참조 설명서의 잘못된 예제가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1344">Fix incorrect example in 'New-AzApplicationGateway' reference documentation</span></span>
* <span data-ttu-id="5d3f2-1345">'Get-AzNetworkWatcherPacketCapture' 참조 설명서에 패킷 캡처를 위한 모든 속성 검색과 관련된 메모가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1345">Add note in 'Get-AzNetworkWatcherPacketCapture' reference documentation about retrieving all properties for a packet capture</span></span>
* <span data-ttu-id="5d3f2-1346">NIC를 올바르게 열거하도록 'Test-AzNetworkWatcherIPFlow' 참조 설명서의 예제가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1346">Fixed example in 'Test-AzNetworkWatcherIPFlow' reference documentation to correctly enumerate NICs</span></span>
* <span data-ttu-id="5d3f2-1347">추가 세부 정보가 있는 경우 추가 세부 정보를 표시하도록 클라우드 예외 구문 분석이 향상되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1347">Improved cloud exception parsing to display additional details if they are present</span></span>
* <span data-ttu-id="5d3f2-1348">더 많은 형식의 SDK 예외를 처리하도록 클라우드 예외 구문 분석이 향상되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1348">Improved cloud exception parsing to handle additional type of SDK exception</span></span>
* <span data-ttu-id="5d3f2-1349">보안 규칙 모델의 잘못된 매핑이 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1349">Fixed incorrect mapping of Security Rule models</span></span>
* <span data-ttu-id="5d3f2-1350">네트워크 인터페이스에 개인 IP 기능을 위한 속성이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1350">Added properties to network interface for private ip feature</span></span>
    - <span data-ttu-id="5d3f2-1351">PSNetworkInterface에 'PrivateEndpoint' 속성이 PSResourceId 형식으로 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1351">Added property 'PrivateEndpoint' as type of PSResourceId to PSNetworkInterface</span></span>
    - <span data-ttu-id="5d3f2-1352">PSNetworkInterfaceIPConfiguration에 'PrivateLinkConnectionProperties' 속성이 PSIpConfigurationConnectivityInformation 형식으로 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1352">Added property 'PrivateLinkConnectionProperties' as type of PSIpConfigurationConnectivityInformation to PSNetworkInterfaceIPConfiguration</span></span>
    - <span data-ttu-id="5d3f2-1353">새 모델 클래스 PSIpConfigurationConnectivityInformation이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1353">Added new model class PSIpConfigurationConnectivityInformation</span></span>
* <span data-ttu-id="5d3f2-1354">Azure Firewall 리소스에 대한 새 ApplicationRuleProtocolType 'mssql'이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1354">Added new ApplicationRuleProtocolType 'mssql' for Azure Firewall resource</span></span>
* <span data-ttu-id="5d3f2-1355">Virtual WAN에서 멀티 링크를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1355">MultiLink support in Virtual WAN</span></span>
    - <span data-ttu-id="5d3f2-1356">새로운 cmdlet</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1356">New cmdlets</span></span>
        - <span data-ttu-id="5d3f2-1357">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1357">New-AzVpnSiteLink</span></span>
        - <span data-ttu-id="5d3f2-1358">New-AzVpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1358">New-AzVpnSiteLinkConnection</span></span>
    - <span data-ttu-id="5d3f2-1359">업데이트된 cmdlet:</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1359">Updated cmdlet:</span></span>
        - <span data-ttu-id="5d3f2-1360">New-VpnSite</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1360">New-VpnSite</span></span>
        - <span data-ttu-id="5d3f2-1361">Update-VpnSite</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1361">Update-VpnSite</span></span>
        - <span data-ttu-id="5d3f2-1362">New-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1362">New-VpnConnection</span></span>
        - <span data-ttu-id="5d3f2-1363">Update-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1363">Update-VpnConnection</span></span>
* <span data-ttu-id="5d3f2-1364">AzureRM cmdlet 대신 Az cmdlet을 사용하도록 일부 PowerShell 예제의 문서가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1364">Fixed documents for some PowerShell examples to use Az cmdlets instead of AzureRM cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="5d3f2-1365">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1365">Az.RecoveryServices</span></span>
* <span data-ttu-id="5d3f2-1366">AzureVMpolicy 개체가 ProtectedItemsCount 특성으로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1366">Update AzureVMpolicy Object with ProtectedItemsCount Attribute</span></span>
* <span data-ttu-id="5d3f2-1367">VM 정책 및 원래 스토리지 계정 복원에 대한 테스트가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1367">Added Tests for VM policy and Original Storage Account Restore</span></span>

#### <a name="azresources"></a><span data-ttu-id="5d3f2-1368">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1368">Az.Resources</span></span>
* <span data-ttu-id="5d3f2-1369">매개 변수 범위 없이 AzRoleAssignment를 호출할 수 없는 버그가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1369">Fix bug where New-AzRoleAssignment could not be called without parameter Scope.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="5d3f2-1370">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1370">Az.ServiceFabric</span></span>
* <span data-ttu-id="5d3f2-1371">'AzServiceFabricReliability' 참조 설명서에 대한 예제의 오타가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1371">Fixed typo in example for 'Update-AzServiceFabricReliability' reference documentation</span></span>
* <span data-ttu-id="5d3f2-1372">애플리케이션 및 서비스를 관리하는 다음과 같은 새 cmdlet이 추가됩니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1372">Adding new cmdlets to manage appliaction and services:</span></span>
    - <span data-ttu-id="5d3f2-1373">New-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1373">New-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="5d3f2-1374">New-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1374">New-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="5d3f2-1375">New-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1375">New-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="5d3f2-1376">New-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1376">New-AzServiceFabricService</span></span>
    - <span data-ttu-id="5d3f2-1377">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1377">Update-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="5d3f2-1378">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1378">Get-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="5d3f2-1379">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1379">Get-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="5d3f2-1380">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1380">Get-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="5d3f2-1381">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1381">Get-AzServiceFabricService</span></span>
    - <span data-ttu-id="5d3f2-1382">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1382">Remove-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="5d3f2-1383">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1383">Remove-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="5d3f2-1384">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1384">Remove-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="5d3f2-1385">Remove-AzServiceFabricServic</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1385">Remove-AzServiceFabricServic</span></span>
* <span data-ttu-id="5d3f2-1386">Service Fabric SDK가 Service Fabric 리소스 공급자 api 버전 2019-03-01을 사용하는 1.2.0 버전으로 업그레이드되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1386">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2019-03-01.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="5d3f2-1387">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1387">Az.SignalR</span></span>
* <span data-ttu-id="5d3f2-1388">Update, Restart, CheckNameAvailability, GetUsage Cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1388">Add Update, Restart, CheckNameAvailability, GetUsage Cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="5d3f2-1389">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1389">Az.Sql</span></span>
* <span data-ttu-id="5d3f2-1390">'Get-AzSqlElasticPool'에 대한 참조 설명서의 예제가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1390">Update example in reference documentation for 'Get-AzSqlElasticPool'</span></span>
* <span data-ttu-id="5d3f2-1391">탄력적 풀을 만드는 vCore 예제가 추가되었습니다(AzSqlElasticPool).</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1391">Added vCore example to creating an elastic pool (New-AzSqlElasticPool).</span></span>
* <span data-ttu-id="5d3f2-1392">Set-AzSqlServerAdvancedThreatProtectionPolicy 및 Set-AzSqlDatabaseAdvancedThreatProtectionPolicy에서 EmailAddresses가 비어 있는 경우 EmailAddresses의 유효성을 검사하고 EmailAdmins가 false가 아닌지 확인하는 기능이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1392">Remove the validation of EmailAddresses and the check that EmailAdmins is not false in case EmailAddresses is empty in Set-AzSqlServerAdvancedThreatProtectionPolicy and Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="5d3f2-1393">감사 범주를 사용하는 여러 진단 설정이 있는 경우 서버/데이터베이스 감사 설정을 제거하도록 설정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1393">Enabled removal of server/database auditing settings when multiple diagnostic settings that enable audit category exist.</span></span>
* <span data-ttu-id="5d3f2-1394">여러 Sql 취약성 평가 cmdlet에서 이메일 주소 유효성 검사가 수정되었습니다(Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting 및 Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1394">Fix email addresses validation in multiple Sql Vulnerability Assessment cmdlets (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting and Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span></span>

#### <a name="azstorage"></a><span data-ttu-id="5d3f2-1395">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1395">Az.Storage</span></span>
* <span data-ttu-id="5d3f2-1396">'Get-AzStorageAccountKey'에 대한 참조 설명서의 예제가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1396">Updated example in reference documentation for 'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="5d3f2-1397">Azure 파일 업로드/다운에서, 원본 파일 SMB 속성(파일 특성, 파일 생성 시간, 파일을 마지막으로 쓴 시간)을 대상 파일에 보존하는 기능이 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1397">In upload/Downalod Azure File,support perserve the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the destination file</span></span>
    -  <span data-ttu-id="5d3f2-1398">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1398">Set-AzStorageFileContent</span></span>
    -  <span data-ttu-id="5d3f2-1399">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1399">Get-AzStorageFileContent</span></span>
* <span data-ttu-id="5d3f2-1400">컨테이너가 사용되는 ImmutabilityPolicy에서 properties/metadate fail을 사용하여 블록 Blob 업로드가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1400">Fix Upload block blob with properties/metadate fail on container enabled ImmutabilityPolicy.</span></span>
    -  <span data-ttu-id="5d3f2-1401">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1401">Set-AzStorageBlobContent</span></span>
* <span data-ttu-id="5d3f2-1402">관리 평면 API를 사용하여 Azure 파일 공유 관리를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1402">Support manage Azure File shares with Management plane API</span></span>
    -  <span data-ttu-id="5d3f2-1403">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1403">New-AzRmStorageShare</span></span>
    -  <span data-ttu-id="5d3f2-1404">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1404">Get-AzRmStorageShare</span></span>
    -  <span data-ttu-id="5d3f2-1405">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1405">Update-AzRmStorageShare</span></span>
    -  <span data-ttu-id="5d3f2-1406">Remove-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1406">Remove-AzRmStorageShare</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="5d3f2-1407">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1407">Az.Websites</span></span>
* <span data-ttu-id="5d3f2-1408">앱을 새 ASP로 마이그레이션할 때 웹앱 태그가 삭제되는 이슈가 해결되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1408">Fixing issue where webapp Tags were getting deleted when migrating App to new ASPwhere webapp Tags were getting deleted when migrating App to new ASP</span></span>
* <span data-ttu-id="5d3f2-1409">Linux와 Windows에서 모두 작동하도록 Publish-AzureWebapp이 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1409">Fixing the Publish-AzureWebapp to work across Linux and windows</span></span>
* <span data-ttu-id="5d3f2-1410">'Get-AzWebAppPublishingProfile' 참조 설명서의 예제가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1410">Update example in 'Get-AzWebAppPublishingProfile' reference documentation</span></span>

## <a name="260---august-2019"></a><span data-ttu-id="5d3f2-1411">2.6.0 - 2019년 8월</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1411">2.6.0 - August 2019</span></span>
#### <a name="general"></a><span data-ttu-id="5d3f2-1412">일반</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1412">General</span></span>
* <span data-ttu-id="5d3f2-1413">여러 모듈에서 기타 오타가 수정됨</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1413">Fixed miscellaneous typos across numerous modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="5d3f2-1414">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1414">Az.Accounts</span></span>
* <span data-ttu-id="5d3f2-1415">Azure Functions 인증에서 사용자가 할당한 MSI가 지원됨(# 9479)</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1415">Support user-assigned MSI in Azure Functiosn Authentication (#9479)</span></span>

#### <a name="azaks"></a><span data-ttu-id="5d3f2-1416">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1416">Az.Aks</span></span>
* <span data-ttu-id="5d3f2-1417">'Get-AzAks' 출력 관련 문제가 해결됨</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1417">Fix issue with output for 'Get-AzAks'</span></span>
    * <span data-ttu-id="5d3f2-1418">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/9847 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1418">More information here: https://github.com/Azure/azure-powershell/issues/9847</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="5d3f2-1419">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1419">Az.ApiManagement</span></span>
* <span data-ttu-id="5d3f2-1420">문제 https://github.com/Azure/azure-powershell/issues/9351 수정</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1420">Fix for issue https://github.com/Azure/azure-powershell/issues/9351</span></span>
    - <span data-ttu-id="5d3f2-1421">productId, apiId, groupId 및 userId에 대한 제한을 적용하지 않는 .Net NuGet 버전이 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1421">Update .net nuget version, which does not enforce restrictions on productId, apiId, groupId and userId</span></span>
* <span data-ttu-id="5d3f2-1422">**Get-AzApiManagementProduct** - API를 사용하는 제품에 대한 쿼리 지원이 추가됨</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1422">**Get-AzApiManagementProduct** - Added support for querying products using Api.</span></span>
  https://github.com/Azure/azure-powershell/issues/9482
* <span data-ttu-id="5d3f2-1423">**New-AzApiManagementApiRevision** - 새 API 수정(https://github.com/Azure/azure-powershell/issues/9752 )을 만들 때 ApiRevisionDescription이 설정되지 않은 문제가 해결됨</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1423">**New-AzApiManagementApiRevision** - Fix for issue where ApiRevisionDescription was not being set when creating new api revision https://github.com/Azure/azure-powershell/issues/9752</span></span>
* <span data-ttu-id="5d3f2-1424">'PsApiManagementOAuth2AuthrozationServer' 모델의 오타가 'PsApiManagementOAuth2AuthorizationServer'로 수정됨</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1424">Fixed typo in model 'PsApiManagementOAuth2AuthrozationServer' to 'PsApiManagementOAuth2AuthorizationServer'</span></span>

#### <a name="azbatch"></a><span data-ttu-id="5d3f2-1425">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1425">Az.Batch</span></span>
* <span data-ttu-id="5d3f2-1426">도움말 메시지 및 설명서에서 Windows를 대문자로 시작하도록 오타가 수정됨</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1426">Fixed typo in help message and documentation to capitalize Windows</span></span>

#### <a name="azcdn"></a><span data-ttu-id="5d3f2-1427">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1427">Az.Cdn</span></span>
* <span data-ttu-id="5d3f2-1428">CDN 모듈 변환 도우미의 오타가 수정됨</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1428">Fixed a typo in CDN module conversion helper</span></span>

#### <a name="azcompute"></a><span data-ttu-id="5d3f2-1429">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1429">Az.Compute</span></span>
* <span data-ttu-id="5d3f2-1430">VmssId가 New-AzVMConfig cmdlet에 추가됨</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1430">Add VmssId to New-AzVMConfig cmdlet</span></span>
* <span data-ttu-id="5d3f2-1431">TerminateScheduledEvents 및 TerminateScheduledEventNotBeforeTimeoutInMinutes 매개 변수가 New-AzVmssConfig 및 Update-AzVmss에 추가됨</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1431">Add TerminateScheduledEvents and TerminateScheduledEventNotBeforeTimeoutInMinutes parameters to New-AzVmssConfig and Update-AzVmss</span></span>
* <span data-ttu-id="5d3f2-1432">HyperVGeneration 속성이 VM 이미지 개체에 추가됨</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1432">Add HyperVGeneration property to VM image object</span></span>
* <span data-ttu-id="5d3f2-1433">Host 및 HostGroup 기능이 추가됨</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1433">Add Host and HostGroup features</span></span>
    - <span data-ttu-id="5d3f2-1434">새 cmdlet:   New-AzHostGroup, New-AzHost, Get-AzHostGroup, Get-AzHost, Remove-AzHostGroup, Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1434">New cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span></span>
    - <span data-ttu-id="5d3f2-1435">HostId 매개 변수가 New-AzVMConfig 및 New-AzVM 추가됨</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1435">HostId parameter is added to New-AzVMConfig and New-AzVM</span></span>
* <span data-ttu-id="5d3f2-1436">'Invoke-AzVMRunCommand' 설명서의 예제에서 올바른 매개 변수 이름을 사용하도록 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1436">Update example in 'Invoke-AzVMRunCommand' documentation to use correct parameter name</span></span>
* <span data-ttu-id="5d3f2-1437">'Set-AzVMDiskEncryptionExtension' 및 'Set-AzVmssDiskEncryptionExtension' 참조 설명서의 '-VolumeType' 설명이 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1437">Update '-VolumeType' description in 'Set-AzVMDiskEncryptionExtension' and 'Set-AzVmssDiskEncryptionExtension' reference documentation</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="5d3f2-1438">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1438">Az.DataFactory</span></span>
* <span data-ttu-id="5d3f2-1439">'New-AzDataFactoryEncryptValue' 설명서에서 'Windows'를 대문자로 시작하도록 오타가 수정됨</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1439">Fix typo to capitalize 'Windows' in 'New-AzDataFactoryEncryptValue' documentation</span></span>
* <span data-ttu-id="5d3f2-1440">ADF .Net SDK 버전이 4.1.2로 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1440">Updated ADF .Net SDK version to 4.1.2</span></span>
* <span data-ttu-id="5d3f2-1441">자체 호스팅 통합 런타임을 SSIS Integration Runtime의 프록시로 설정할 수 있도록 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' 및 'DataProxyStagingPath' 매개 변수가 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd에 추가됨</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1441">Add parameter 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' and 'DataProxyStagingPath' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable set up Self-Hosted Integration Runtime as a proxy for SSIS Integration Runtime</span></span>
* <span data-ttu-id="5d3f2-1442">PSTriggerRun에서 트리거된 파이프라인, 메시지 및 속성을 표시하고, PSActivityRun에서 작업 유형을 표시하도록 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1442">Updated PSTriggerRun to show the triggered pipelines, message and properties, and PSActivityRun to show the activity type</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="5d3f2-1443">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1443">Az.DataLakeStore</span></span>
* <span data-ttu-id="5d3f2-1444">오류 또는 원격 예외에 대한 Get-DataLakeStoreDeletedItem 중단이 수정됨</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1444">Fix hanging of Get-DataLakeStoreDeletedItem for any errors or remote exceptions.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="5d3f2-1445">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1445">Az.EventHub</span></span>
* <span data-ttu-id="5d3f2-1446">#9658 문제 해결: Set-AzEventHubNetworkRuleSet의 VirtualNteworkRule 매개 변수에 대한 오타</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1446">Fix for issue #9658 : Typo VirtualNteworkRule parameter in Set-AzEventHubNetworkRuleSet</span></span>
* <span data-ttu-id="5d3f2-1447">#9558 문제 해결: Set-AzEventHubNamespace에서 PUT 대신 PATCH가 사용됨</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1447">Fix for issue #9558 : Set-AzEventHubNamespace is using PATCH instead of PUT</span></span>
* <span data-ttu-id="5d3f2-1448">EnableKafka 매개 변수가 Set-AzEventHubNamespace cmdlet에 추가됨</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1448">added EnableKafka parameter to Set-AzEventHubNamespace cmdlet</span></span>
* <span data-ttu-id="5d3f2-1449">#9786 문제 해결: Listen(수신 대기) 전용 권한이 있는 규칙을 만들 수 없음</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1449">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>

#### <a name="azmarketplaceordering"></a><span data-ttu-id="5d3f2-1450">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1450">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="5d3f2-1451">'Azure'가 모두 소문자인 설명서의 오타가 수정됨</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1451">Fixed documentation typo where 'Azure' was all lowercase letters</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="5d3f2-1452">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1452">Az.Monitor</span></span>
* <span data-ttu-id="5d3f2-1453">도움말 설명서에서 잘못된 매개 변수 이름이 수정됨</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1453">Fixed incorrect parameter name in help documentation</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="5d3f2-1454">Az.Network</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1454">Az.Network</span></span>
* <span data-ttu-id="5d3f2-1455">New-AzPrivateLinkServiceIpConfig가 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1455">Updated New-AzPrivateLinkServiceIpConfig</span></span>
    - <span data-ttu-id="5d3f2-1456">서버 쪽에서 사용되지 않으므로 'PublicIpAddress' 매개 변수가 사용되지 않음</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1456">Deprecated the paramster 'PublicIpAddress' since this is never used in the server side.</span></span>
    - <span data-ttu-id="5d3f2-1457">현재 IP 구성이 기본 구성인지 여부를 나타내는 하나의 선택적 'Primary' 매개 변수가 추가됨</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1457">Added one optional parameter 'Primary' that indicate the current ip configuration is primary one or not.</span></span>
* <span data-ttu-id="5d3f2-1458">SDK의 요청 오류 예외 처리가 향상됨 - 이전의 SDK 예외가 올바르게 처리되지 않아 주요 오류 세부 정보가 표시되지 않은 문제가 해결됨</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1458">Improved handling of request error exception from SDK   -Fixes the issue that previously SDK exceptions aren't handled correctly which results in key error details not being displayed</span></span>
* <span data-ttu-id="5d3f2-1459">올바른 IPv6 접두사 길이를 확인하기 위해 Ipv6 IP 접두사에 대한 유효성 검사 논리가 조정됨</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1459">Adjusted validation logic for Ipv6 IP Prefix to check for correct IPv6 prefix length.</span></span>
* <span data-ttu-id="5d3f2-1460">Get-AzVirtualNetworkSubnetConfig가 업데이트됨: 서브넷 리소스 ID별로 가져오도록 설정되는 매개 변수 세트가 추가됨</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1460">Updated Get-AzVirtualNetworkSubnetConfig: Added parameter set to get by subnet resource id.</span></span>
* <span data-ttu-id="5d3f2-1461">AzNetworkServiceTag의 Location(위치) 매개 변수에 대한 설명이 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1461">Updated description of Location parameter for AzNetworkServiceTag</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="5d3f2-1462">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1462">Az.OperationalInsights</span></span>
* <span data-ttu-id="5d3f2-1463">'New-AzOperationalInsightsLinuxSyslogDataSource'에 대한 설명서가 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1463">Updated documentation for 'New-AzOperationalInsightsLinuxSyslogDataSource'</span></span>
    - <span data-ttu-id="5d3f2-1464">예제가 추가됨</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1464">Added example</span></span>
    - <span data-ttu-id="5d3f2-1465">'-Name' 매개 변수에 대한 설명이 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1465">Updated description for '-Name' parameter</span></span>
* <span data-ttu-id="5d3f2-1466">New-AzOperationalInsightsWindowsEventDataSource에 대한 예제가 추가됨</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1466">Added an example for New-AzOperationalInsightsWindowsEventDataSource</span></span>
* <span data-ttu-id="5d3f2-1467">New-AzOperationalInsightsWindowsEventDataSource의 -Name 매개 변수에 대한 설명이 변경됨</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1467">Changed the description of the -Name parameter for New-AzOperationalInsightsWindowsEventDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="5d3f2-1468">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1468">Az.RecoveryServices</span></span>
* <span data-ttu-id="5d3f2-1469">'Get-AzRecoveryServicesBackupJobDetail.md'가 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1469">Update 'Get-AzRecoveryServicesBackupJobDetail.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="5d3f2-1470">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1470">Az.Resources</span></span>
* <span data-ttu-id="5d3f2-1471">Microsoft 리소스에 대한 새 2019-05-10 API 버전 지원이 추가됨</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1471">Add support for new api version 2019-05-10 for Microsoft.Resource</span></span>
    - <span data-ttu-id="5d3f2-1472">변수, 리소스 및 속성에 대한 'copy.count = 0' 지원이 추가됨</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1472">Add support for 'copy.count = 0' for variables, resources and properties</span></span>
    - <span data-ttu-id="5d3f2-1473">'condition = false' 또는 'copy.count = 0'인 리소스가 완료 모드에서 삭제됨</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1473">Resources with 'condition = false' or 'copy.count = 0' will be deleted in complete mode</span></span>
* <span data-ttu-id="5d3f2-1474">정책을 구독 수준에서 도움말 문서에 할당하는 예제가 추가됨</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1474">Add an example of assigning policy at subscription level to help doc</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="5d3f2-1475">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1475">Az.ServiceBus</span></span>
* <span data-ttu-id="5d3f2-1476">#9658 문제 해결: Set-AzServiceBusNetworkRuleSet의 VirtualNetworkRule 매개 변수에 대한 오타</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1476">Fix for issue #9658 : Typo VirtualNetworkRule parameter in Set-AzServiceBusNetworkRuleSet</span></span>
* <span data-ttu-id="5d3f2-1477">#9786 문제 해결: Listen(수신 대기) 전용 권한이 있는 규칙을 만들 수 없음</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1477">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>
* <span data-ttu-id="5d3f2-1478">큐 및 토픽에 대한 이름 가용성을 확인하는 새 'Test-AzServiceBusNameAvailability' 명령이 추가됨</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1478">Added new command 'Test-AzServiceBusNameAvailability' to check the name availability for queue and topic</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="5d3f2-1479">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1479">Az.ServiceFabric</span></span>
* <span data-ttu-id="5d3f2-1480">노드 유형 추가 cmdlet 버그 수정:</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1480">Fix add node type cmdlet bugs:</span></span>
    - <span data-ttu-id="5d3f2-1481">서비스 패브릭 클러스터와 관련이 없는 다른 vmss가 리소스 그룹에 있을 때 발생하는 NullReferenceException 버그</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1481">NullReferenceException bug when resource group had other vmss not related to the service fabric cluster.</span></span> <span data-ttu-id="5d3f2-1482">문제 해결: https://github.com/Azure/azure-powershell/issues/8681</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1482">Fixes issue: https://github.com/Azure/azure-powershell/issues/8681</span></span>
    - <span data-ttu-id="5d3f2-1483">virtualNetwork가 클러스터의 다른 리소스 그룹에 있을 때 cmdlet이 실패하는 버그가 수정됨</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1483">Fix bug where cmdlet failed if virtualNetwork was in a different resource group that the cluster.</span></span> <span data-ttu-id="5d3f2-1484">문제 해결: https://github.com/Azure/azure-powershell/issues/8407</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1484">fixes issue: https://github.com/Azure/azure-powershell/issues/8407</span></span>
    - <span data-ttu-id="5d3f2-1485">Add-AzServiceFabricApplicationCertificate cmdlet이 사용되지 않음</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1485">Deprecating Add-AzServiceFabricApplicationCertificate cmdlet</span></span>

#### <a name="azsql"></a><span data-ttu-id="5d3f2-1486">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1486">Az.Sql</span></span>
* <span data-ttu-id="5d3f2-1487">이전의 Auditing(감사) cmdlet에 대한 설명서가 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1487">Update documentation of old Auditing cmdlets.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="5d3f2-1488">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1488">Az.Storage</span></span>
* <span data-ttu-id="5d3f2-1489">더 많은 시나리오를 cmdlet 예제에 추가하고 매개 변수 설명을 업데이트하여 Get/Close-AzStorageFileHandle에 대한 도움말이 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1489">Update help for Get/Close-AzStorageFileHandle, by add more scenarios to cmdlet examples and update parameter descriptions</span></span>
* <span data-ttu-id="5d3f2-1490">Blob 업로드 및 Blob 복사에서 StandardBlobTier가 지원됨</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1490">Support StandardBlobTier in upload blob and copy blob</span></span>
    -  <span data-ttu-id="5d3f2-1491">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1491">Set-AzStorageBlobContent</span></span>
    -  <span data-ttu-id="5d3f2-1492">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1492">Start-AzStorageBlobCopy</span></span>
* <span data-ttu-id="5d3f2-1493">Blob 복사에서 우선 순위 리하이드레이션이 지원됨</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1493">Support Rehydrate Priority in copy blob</span></span>
    -  <span data-ttu-id="5d3f2-1494">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1494">Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="5d3f2-1495">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1495">Az.Websites</span></span>
* <span data-ttu-id="5d3f2-1496">Set-AzWebApp 및 Set-AzWebAppSlot에서 -AppSettings 매개 변수에 대한 설명이 추가됨</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1496">Add clarification around -AppSettings parameter in Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <a name="250---july-2019"></a><span data-ttu-id="5d3f2-1497">2.5.0 - 2019년 7월</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1497">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="5d3f2-1498">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1498">Az.Accounts</span></span>
* <span data-ttu-id="5d3f2-1499">ClientRuntime의 최신 버전을 사용하도록 일반적인 코드를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1499">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="5d3f2-1500">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1500">Az.ApplicationInsights</span></span>
* <span data-ttu-id="5d3f2-1501">'Remove-AzApplicationInsightsApiKey' 설명서의 예제 오타 수정</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1501">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span>

#### <a name="azautomation"></a><span data-ttu-id="5d3f2-1502">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1502">Az.Automation</span></span>
* <span data-ttu-id="5d3f2-1503">리소스 문자열의 오타 수정</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1503">Fix typo in resource string</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="5d3f2-1504">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1504">Az.CognitiveServices</span></span>
* <span data-ttu-id="5d3f2-1505">NetworkRuleSet 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1505">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="5d3f2-1506">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1506">Az.Compute</span></span>
* <span data-ttu-id="5d3f2-1507">VM 인스턴스 보기 개체의 누락된 속성(ComputerName, OsName, OsVersion 및 HyperVGeneration)을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1507">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="5d3f2-1508">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1508">Az.ContainerRegistry</span></span>
* <span data-ttu-id="5d3f2-1509">복제 매개 변수의 Remove-AzContainerRegistryReplication에서 오타 수정</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1509">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="5d3f2-1510">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/9633 을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1510">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="5d3f2-1511">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1511">Az.DataFactory</span></span>
* <span data-ttu-id="5d3f2-1512">ADF .Net SDK 버전을 4.1.0으로 업데이트</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1512">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="5d3f2-1513">'Get-AzDataFactoryV2PipelineRun' 설명서의 오타 수정</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1513">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="5d3f2-1514">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1514">Az.EventHub</span></span>
* <span data-ttu-id="5d3f2-1515">SAS 토큰을 생성하기 위해 추가된 새로운 cmmdlet 추가: New-AzEventHubAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1515">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="5d3f2-1516">'관리'만 지정된 경우 authorizationrules 권한에 대한 확인 및 오류 메시지 추가</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1516">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="5d3f2-1517">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1517">Az.KeyVault</span></span>
* <span data-ttu-id="5d3f2-1518">인증서 정책에 대한 KeySize 지정을 위한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1518">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="5d3f2-1519">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1519">Az.LogicApp</span></span>
* <span data-ttu-id="5d3f2-1520">모든 맵 유형을 나열하도록 Get-AzIntegrationAccountMap 수정</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1520">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="5d3f2-1521">필터링을 위해 새 MapType 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1521">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="5d3f2-1522">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1522">Az.ManagedServices</span></span>
* <span data-ttu-id="5d3f2-1523">API 버전 2019-06-01(GA)에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1523">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="5d3f2-1524">Az.Network</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1524">Az.Network</span></span>
* <span data-ttu-id="5d3f2-1525">프라이빗 엔드포인트 및 프라이빗 링크 서비스에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1525">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="5d3f2-1526">새로운 cmdlet</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1526">New cmdlets</span></span>
        - <span data-ttu-id="5d3f2-1527">Set-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1527">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="5d3f2-1528">Set-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1528">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="5d3f2-1529">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1529">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="5d3f2-1530">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1530">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="5d3f2-1531">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1531">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="5d3f2-1532">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1532">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="5d3f2-1533">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1533">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="5d3f2-1534">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1534">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="5d3f2-1535">기능에 대한 새로운 명령이 업데이트됨: Virtualnetwork의 서브넷에 있는 PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies 플래그</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1535">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="5d3f2-1536">업데이트된 New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1536">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="5d3f2-1537">이 서브넷의 프라이빗 엔드포인트에 네트워크 정책을 적용할지 여부를 나타내는 선택적 매개 변수 -PrivateEndpointNetworkPoliciesFlag가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1537">Added optional parameter -PrivateEndpointNetworkPoliciesFlag that configures whether to apply network policies on private endpoint in this subnet.</span></span>
        - <span data-ttu-id="5d3f2-1538">이 서브넷의 프라이빗 연결 서비스에 네트워크 정책을 적용할지 여부를 나타내는 선택적 매개 변수 -PrivateLinkServiceNetworkPoliciesFlag가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1538">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag that configures whether to apply network policies network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="5d3f2-1539">AzPrivateLinkService의 cmdlet 매개 변수 'ServiceName'이 이전 버전과의 호환성을 위해 별칭 'ServiceName'을 사용한 'Name'으로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1539">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="5d3f2-1540">네트워크 보안 규칙 구성에 ICMP 프로토콜 사용</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1540">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="5d3f2-1541">다음 Cmdlet이 업데이트 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1541">Updated cmdlets</span></span>
        - <span data-ttu-id="5d3f2-1542">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1542">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="5d3f2-1543">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1543">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="5d3f2-1544">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1544">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="5d3f2-1545">New-AzVirtualNetworkGatewayConnection에 대한 구성 가능한 매개 변수로 ConnectionProtocolType (Ikev1/Ikev2) 추가</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1545">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="5d3f2-1546">LoadBalancerFrontendIpConfiguration에 PrivateIpAddressVersion 추가</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1546">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="5d3f2-1547">업데이트된 cmdlet:</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1547">Updated cmdlet:</span></span>
        - <span data-ttu-id="5d3f2-1548">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1548">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="5d3f2-1549">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1549">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="5d3f2-1550">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1550">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="5d3f2-1551">프로브에서 사용자 지정 포트를 지원하기 위한 Application Gateway New-AzApplicationGatewayProbeConfig 명령 업데이트</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1551">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="5d3f2-1552">업데이트된 New-AzApplicationGatewayProbeConfig: 백 엔드 서버 검색에 사용되는 선택적 매개 변수 포트가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1552">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="5d3f2-1553">이 매개 변수는 Standard_V2 및 WAF_V2 SKU에 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1553">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="5d3f2-1554">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1554">Az.OperationalInsights</span></span>
* <span data-ttu-id="5d3f2-1555">저장된 검색의 기본 버전이 1로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1555">Updated default version for saved searches to be 1.</span></span>
* <span data-ttu-id="5d3f2-1556">사용자 지정 로그 null regex 처리가 수정됨</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1556">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="5d3f2-1557">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1557">Az.RecoveryServices</span></span>
* <span data-ttu-id="5d3f2-1558">'Get-AzRecoveryServicesBackupJob.md' 업데이트</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1558">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="5d3f2-1559">'Get-AzRecoveryServicesBackupContainer.md' 업데이트</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1559">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="5d3f2-1560">'Get-AzRecoveryServicesVault.md' 업데이트</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1560">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="5d3f2-1561">'Wait-AzRecoveryServicesBackupJob.md' 업데이트</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1561">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="5d3f2-1562">'Set-AzRecoveryServicesVaultContext.md' 업데이트</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1562">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="5d3f2-1563">'Get-AzRecoveryServicesBackupItem.md' 업데이트</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1563">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="5d3f2-1564">'Get-AzRecoveryServicesBackupRecoveryPoint.md' 업데이트</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1564">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="5d3f2-1565">'Restore-AzRecoveryServicesBackupItem.md' 업데이트</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1565">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="5d3f2-1566">Azure 파일 공유용 컨테이너를 등록 취소하기 위해 서비스 요청 업데이트</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1566">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="5d3f2-1567">'Set-AzRecoveryServicesAsrAlertSetting.md' 업데이트</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1567">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="5d3f2-1568">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1568">Az.Resources</span></span>
- <span data-ttu-id="5d3f2-1569">'New-AzResourceGroupDeployment' 설명서에서 참조된 누락 cmdlet 제거</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1569">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="5d3f2-1570">새 API 버전 2019-01-01을 사용하도록 정책 cmdlet 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1570">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="5d3f2-1571">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1571">Az.ServiceBus</span></span>
* <span data-ttu-id="5d3f2-1572">SAS 토큰을 생성하기 위해 추가된 새로운 cmmdlet 추가: New-AzServiceBusAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1572">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="5d3f2-1573">'관리'만 지정된 경우 authorizationrules 권한에 대한 확인 및 오류 메시지 추가</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1573">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="5d3f2-1574">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1574">Az.Sql</span></span>
* <span data-ttu-id="5d3f2-1575">Set-AzSqlDatabaseSecondary cmdlet에 대한 누락된 예제 수정</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1575">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="5d3f2-1576">이메일 주소를 제공하지 않고 설정된 취약성 평가 반복 검색 수정</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1576">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="5d3f2-1577">경고 메시지의 작은 오타를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1577">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="5d3f2-1578">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1578">Az.Storage</span></span>
* <span data-ttu-id="5d3f2-1579">'Get-AzStorageAccount'에 대한 참조 설명서의 예제를 업데이트하여 올바른 매개 변수 이름 사용</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1579">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="5d3f2-1580">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1580">Az.StorageSync</span></span>
* <span data-ttu-id="5d3f2-1581">Invoke-AzStorageSyncChangeDetection cmdlet을 추가하는 중입니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1581">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="5d3f2-1582">TierFilesOlderThanDays를 기념하는 문제 9551 수정</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1582">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="5d3f2-1583">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1583">Az.Websites</span></span>
* <span data-ttu-id="5d3f2-1584">Get-AzWebApp 및 Set-AzWebApp에서 일부 SiteConfig 속성을 반환하지 않은 버그 수정</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1584">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="5d3f2-1585">Get-AzDeletedWebApp 및 Restore-AzDeletedWebApp에 새 위치 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1585">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="5d3f2-1586">AzWebApp-IncludeSourceWebAppSlots을 사용하여 웹앱 슬롯을 복제하는 버그를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1586">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="5d3f2-1587">2.4.0 - 2019년 7월</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1587">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="5d3f2-1588">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1588">Az.Accounts</span></span>
* <span data-ttu-id="5d3f2-1589">프로필 cmdlet에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1589">Add support for profile cmdlets</span></span>
* <span data-ttu-id="5d3f2-1590">생성된 cmdlet에서 환경 및 데이터 평면에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1590">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="5d3f2-1591">Windows PowerShell의 데이터 평면 cmdlet에대해 일부 경우 잘못된 엔드포인트가 사용되는 버그 수정</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1591">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="5d3f2-1592">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1592">Az.Advisor</span></span>
* <span data-ttu-id="5d3f2-1593">Az.Advisor의 GA 릴리스</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1593">GA release of Az.Advisor</span></span>
* <span data-ttu-id="5d3f2-1594">이 모듈은 이제 롤업 `Az` 모듈의 일부로 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1594">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="5d3f2-1595">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1595">Az.ApiManagement</span></span>
* <span data-ttu-id="5d3f2-1596">문제 https://github.com/Azure/azure-powershell/issues/8671 수정</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1596">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="5d3f2-1597">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1597">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="5d3f2-1598">사용자 및 제품별 구독을 쿼리하기 위한 지원이 추가됨</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1598">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="5d3f2-1599">범위 '/', '/ api, '/ api/echo api'를 사용하여 쿼리하기 위한 지원이 추가됨</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1599">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="5d3f2-1600">[https://github.com/Azure/azure-powershell/issues/9307](https://github.com/Azure/azure-powershell/issues/9307 ) 및 https://github.com/Azure/azure-powershell/issues/8432 문제 수정</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1600">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="5d3f2-1601">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1601">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="5d3f2-1602">Apis를 가져올 때 'ApiVersion' 및 'ApiVersionSetId'를 지정하기 위한 지원이 추가됨</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1602">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="5d3f2-1603">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1603">Az.Automation</span></span>
* <span data-ttu-id="5d3f2-1604">문자열 값을 처리하기 위해 Set-AzAutomationConnectionFieldValue cmdlet 버그를 수정했습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1604">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="5d3f2-1605">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1605">Az.Compute</span></span>
* <span data-ttu-id="5d3f2-1606">New-AzImageConfig에 HyperVGeneration 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1606">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="5d3f2-1607">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1607">Az.DataFactory</span></span>
* <span data-ttu-id="5d3f2-1608">get activity runs, get pipeline runs, get trigger runs ADF cmdlet의 출력을 업데이트하여 Select-Object pipe를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1608">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="5d3f2-1609">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1609">Az.EventGrid</span></span>
* <span data-ttu-id="5d3f2-1610">'New-AzEventGridSubcription' 설명서의 오타 수정</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1610">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="5d3f2-1611">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1611">Az.IotHub</span></span>
* <span data-ttu-id="5d3f2-1612">권한 부여 정책 키를 다시 생성하기 위한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1612">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="5d3f2-1613">Az.Network</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1613">Az.Network</span></span>
* <span data-ttu-id="5d3f2-1614">'RoutingPreference'를 공용 IP 태그에 추가함</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1614">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="5d3f2-1615">'Get-AzNetworkServiceTag' 참조 설명서의 예제 개선</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1615">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="5d3f2-1616">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1616">Az.PolicyInsights</span></span>
* <span data-ttu-id="5d3f2-1617">Get-AzPolicyState의 null 참조 문제 해결</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1617">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="5d3f2-1618">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/9446 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1618">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="5d3f2-1619">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1619">Az.OperationalInsights</span></span>
* <span data-ttu-id="5d3f2-1620">Get-AzOperationalInsightsDataSource에 반환된 CustomLog datasource 모델 수정됨</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1620">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="5d3f2-1621">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1621">Az.RecoveryServices</span></span>
* <span data-ttu-id="5d3f2-1622">IaaSVMs에 대한 get-policy 명령 수정</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1622">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="5d3f2-1623">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1623">Az.Resources</span></span>
    - <span data-ttu-id="5d3f2-1624">Get-AzPolicyState -Top 매개 변수에 대한 도움말 텍스트 수정</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1624">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="5d3f2-1625">Get-AzPolicyAlias에 대한 클라이언트 쪽 페이징 지원 추가</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1625">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="5d3f2-1626">Set-AzPolicyAssignment, -PolicyParameters 및 -PolicyParametersObject에 대한 새 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1626">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="5d3f2-1627">Policy cmdlet에 대한 몇 가지 문서 및 예제 업데이트</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1627">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="5d3f2-1628">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1628">Az.ServiceBus</span></span>
* <span data-ttu-id="5d3f2-1629">문제 #4938 수정 - MaxSizeInMegabytes를 설정할 때 New-AzureRmServiceBusQueue가 BadRequest 반환</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1629">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="5d3f2-1630">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1630">Az.Sql</span></span>
* <span data-ttu-id="5d3f2-1631">미리 보기 릴리스에서 공개 릴리스로 인스턴스 장애 조치(Failover) 그룹 cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1631">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="5d3f2-1632">새 cmdlet으로 Azure SQL Server\Database Auditing을 지원하세요.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1632">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="5d3f2-1633">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1633">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="5d3f2-1634">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1634">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="5d3f2-1635">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1635">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="5d3f2-1636">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1636">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="5d3f2-1637">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1637">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="5d3f2-1638">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1638">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="5d3f2-1639">취약성 평가 설정에서 이메일 제약 조건 제거</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1639">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="5d3f2-1640">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1640">Az.Storage</span></span>
* <span data-ttu-id="5d3f2-1641">다음 cmdlet에서 2개의 매개 변수 '-IndexDocument' 및 '-ErrorDocument404Path'를 필수에서 선택으로 변경하세요.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1641">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="5d3f2-1642">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1642">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="5d3f2-1643">예제를 추가하여 Get-AzStorageBlobContent의 도움말 업데이트</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1643">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="5d3f2-1644">StorageException으로 cmdlet이 실패한 경우 자세한 오류 정보 표시</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1644">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="5d3f2-1645">Azure Files AAD DS 인증으로 스토리지 계정 생성 또는 업데이트 지원</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1645">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="5d3f2-1646">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1646">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="5d3f2-1647">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1647">Set-AzStorageAccount</span></span>
* <span data-ttu-id="5d3f2-1648">파일 공유, 파일 디렉터리 또는 파일의 목록 지원 또는 파일 핸들 닫기</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1648">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="5d3f2-1649">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1649">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="5d3f2-1650">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1650">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="5d3f2-1651">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1651">Az.StorageSync</span></span>
* <span data-ttu-id="5d3f2-1652">이 모듈은 이제 롤업 `Az` 모듈의 일부로 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1652">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="5d3f2-1653">2.3.2 - 2019년 6월</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1653">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="5d3f2-1654">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1654">Az.Accounts</span></span>
* <span data-ttu-id="5d3f2-1655">함수 호출에 대해 일부 경우 잘못된 URL이 사용되는 버그 수정</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1655">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="5d3f2-1656">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/8983 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1656">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="5d3f2-1657">AzureRM에서 Az cmdlet으로의 별칭 문제 해결</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1657">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="5d3f2-1658">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1658">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="5d3f2-1659">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1659">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="5d3f2-1660">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1660">Az.Compute</span></span>
* <span data-ttu-id="5d3f2-1661">New-AzVm 및 New-AzVmss 단순 매개 변수 집합은 이제 'ProximityPlacementGroup'매개 변수를 허용합니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1661">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="5d3f2-1662">'New-AzVM' 참조 설명서에서 오타 수정</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1662">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="5d3f2-1663">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1663">Az.Dns</span></span>
* <span data-ttu-id="5d3f2-1664">'Set-AzDnsZone' 도움말 예제의 오타가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1664">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="5d3f2-1665">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1665">Az.EventGrid</span></span>
* <span data-ttu-id="5d3f2-1666">2019-06-01 API 버전을 사용하도록 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1666">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="5d3f2-1667">새 cmdlet:</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1667">New cmdlets:</span></span>
    - <span data-ttu-id="5d3f2-1668">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1668">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="5d3f2-1669">새 Azure Event Grid 도메인을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1669">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="5d3f2-1670">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1670">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="5d3f2-1671">Event Grid 도메인의 세부 정보를 가져오거나 현재 Azure 구독의 모든 Event Grid 도메인 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1671">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="5d3f2-1672">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1672">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="5d3f2-1673">Azure Event Grid 도메인을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1673">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="5d3f2-1674">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1674">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="5d3f2-1675">Azure Event Grid 도메인에 대한 공유 액세스 키를 다시 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1675">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="5d3f2-1676">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1676">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="5d3f2-1677">Event Grid 도메인 이벤트를 게시하는 데 사용되는 공유 액세스 키를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1677">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="5d3f2-1678">New-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1678">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="5d3f2-1679">새 Azure Event Grid 도메인 토픽을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1679">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="5d3f2-1680">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1680">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="5d3f2-1681">Event Grid 도메인 토픽의 세부 사항을 가져오거나, 현재 Azure의 특정 Event Grid 도메인 아래의 모든 Event Grid 도메인 토픽 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1681">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span>
    - <span data-ttu-id="5d3f2-1682">Remove-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1682">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="5d3f2-1683">기존 Azure Event Grid 도메인 토픽을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1683">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="5d3f2-1684">다음 Cmdlet이 업데이트 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1684">Updated cmdlets:</span></span>
    - <span data-ttu-id="5d3f2-1685">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1685">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="5d3f2-1686">새로운 Event Grid 도메인 및 Event Grid 도메인 토픽에 대한 파이핑을 지원하기 위해 새로운 필수 매개 변수를 추가하여 이러한 리소스 아래에 새 이벤트 구독을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1686">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="5d3f2-1687">새로운 Event Grid 도메인 이름 및 Event Grid 도메인 토픽 이름을 지정하기 위해 새로운 필수 매개 변수를 추가하여 이러한 리소스 아래에 새 이벤트 구독을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1687">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="5d3f2-1688">기존 매개 변수(예: EndPointType, SubjectBeginsWith 등)를 재사용할 수 있도록 도메인 및 도메인 토픽에 대한 새로운 매개 변수 집합을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1688">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="5d3f2-1689">지정을 위한 새로운 선택적 매개 변수를 추가</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1689">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="5d3f2-1690">이벤트 구독 만료 날짜,</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1690">Event subscription expiration date,</span></span>
            - <span data-ttu-id="5d3f2-1691">고급 필터링 매개 변수.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1691">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="5d3f2-1692">대상으로 servicebusqueue에 대한 새 열거형을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1692">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="5d3f2-1693">-IncludedEventType 옵션에서 'All' 사용을 허용하지 않고 다음으로 대체함</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1693">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span>
    - <span data-ttu-id="5d3f2-1694">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1694">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="5d3f2-1695">결과 페이지 매김 및 필터링을 지원하는 새로운 선택적 매개 변수(Top, ODataQuery 및 NextLink)를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1695">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="5d3f2-1696">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1696">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="5d3f2-1697">Event Grid 도메인 및 Event Grid 도메인 토픽에 대한 파이핑을 지원하기 위해 새로운 필수 매개 변수를 추가하여 이러한 리소스 아래에 기존 이벤트 구독을 제거할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1697">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="5d3f2-1698">Event Grid 도메인 이름 및 Event Grid 도메인 토픽 이름을 지정하기 위해 새로운 필수 매개 변수를 추가하여 이러한 리소스 아래에 기존 이벤트 구독을 제거할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1698">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="5d3f2-1699">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1699">Az.FrontDoor</span></span>
* <span data-ttu-id="5d3f2-1700">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1700">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="5d3f2-1701">변환 지원 및 새 연산자 자동 완성 값(RegEx)을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1701">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="5d3f2-1702">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1702">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="5d3f2-1703">새 자동 완성 값 추가</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1703">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="5d3f2-1704">Az.Network</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1704">Az.Network</span></span>
* <span data-ttu-id="5d3f2-1705">Microsoft Azure Virtual Network 게이트웨이 리소스에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1705">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="5d3f2-1706">새로운 cmdlet</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1706">New cmdlets</span></span>
        - <span data-ttu-id="5d3f2-1707">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1707">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="5d3f2-1708">AvailablePrivateEndpointType 추가</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1708">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="5d3f2-1709">새로운 cmdlet</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1709">New cmdlets</span></span>
        - <span data-ttu-id="5d3f2-1710">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1710">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="5d3f2-1711">PrivatePrivateLinkService 추가</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1711">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="5d3f2-1712">새로운 cmdlet</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1712">New cmdlets</span></span>
        - <span data-ttu-id="5d3f2-1713">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1713">Get-AzPrivateLinkService</span></span>
        - <span data-ttu-id="5d3f2-1714">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1714">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="5d3f2-1715">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1715">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="5d3f2-1716">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1716">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="5d3f2-1717">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1717">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="5d3f2-1718">PrivateEndpoint 추가</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1718">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="5d3f2-1719">새로운 cmdlet</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1719">New cmdlets</span></span>
        - <span data-ttu-id="5d3f2-1720">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1720">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="5d3f2-1721">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1721">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="5d3f2-1722">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1722">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="5d3f2-1723">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1723">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="5d3f2-1724">기능에 대한 새로운 명령이 업데이트됨: VpnConnection 상의 UseLocalAzureIpAddress 플래그</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1724">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="5d3f2-1725">New-AzVpnConnection이 업데이트됨: 선택적 매개 변수 -UseLocalAzureIpAddress를 추가하여 로컬 Azure IP 주소가 연결을 시작하는 동안 소스 주소로 사용되어야 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1725">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="5d3f2-1726">Set-AzVpnConnection이 업데이트됨: 선택적 매개 변수 -UseLocalAzureIpAddress를 추가하여 로컬 Azure IP 주소가 연결을 시작하는 동안 소스 주소로 사용되어야 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1726">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="5d3f2-1727">ExpressRoute 피어링에 읽기 전용 필드 PeeredConnections가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1727">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="5d3f2-1728">ExpressRoute에 읽기 전용 필드 GlobalReachEnabled가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1728">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="5d3f2-1729">ExpressRouteCircuit 모델에서 AllowGlobalReach 필드의 사용 중단을 부르는 호환성이 손상되는 변경 속성이 추가됨</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1729">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="5d3f2-1730">AzApplicationGatewayRedirectConfiguration cmdlet에서 TargetListenerID를 사용하는 중의 8756 오류 문제가 해결됨</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1730">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="5d3f2-1731">다시 쓰기 규칙 세트가 설정되지 못하게 하는 New-AzApplicationGatewayPathRuleConfig의 버그를 수정했습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1731">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="5d3f2-1732">NetworkInterfaceIpConfiguration에 VirtualNetworkTaps가 표시되는 방식이 수정됨</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1732">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="5d3f2-1733">모든 파트를 나열하도록 Cortex Get cmdlet이 수정됨</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1733">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="5d3f2-1734">ExpressRouteGateways, VpnGateway에 대한 VirtualHub 참조 생성 수정됨</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1734">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="5d3f2-1735">AzureFirewall 및 NatGateway의 가용성 영역에 대한 지원 추가됨</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1735">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="5d3f2-1736">Get-AzNetworkServiceTag cmdlet 추가됨</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1736">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="5d3f2-1737">Azure Firewall에 대한 여러 공용 IP 주소에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1737">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="5d3f2-1738">New-AzFirewall cmdlet이 업데이트됨:</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1738">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="5d3f2-1739">하나 이상의 공용 IP 주소 개체를 허용하는 매개 변수 -PublicIpAddress 추가됨</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1739">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="5d3f2-1740">Virtual Network 개체를 허용하는 매개 변수 -VirtualNetwork 추가됨</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1740">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="5d3f2-1741">방화벽 개체에 AddPublicIpAddress 및 RemovePublicIpAddress 메서드 추가됨 - 공용 IP 주소 개체를 입력으로 허용</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1741">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="5d3f2-1742">매개 변수 -PublicIpName 및 -VirtualNetworkName이 더 이상 사용되지 않음</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1742">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span>
* <span data-ttu-id="5d3f2-1743">기능에 대한 새로운 명령이 업데이트됨: VpnClient AAD 인증 옵션을 가상 네트워크 게이트웨이 리소스로 설정했습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1743">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span>
    - <span data-ttu-id="5d3f2-1744">New-AzVirtualNetworkGateway가 업데이트됨: 게이트웨이에서 VpnClient AAD 인증 옵션을 설정할 수 있도록 선택적 매개 변수 AadTenantUri, AadAudienceId, AadIssuerUri가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1744">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="5d3f2-1745">Set-AzVirtualNetworkGateway가 업데이트됨: 게이트웨이에서 VpnClient AAD 인증 옵션을 설정할 수 있도록 선택적 매개 변수 AadTenantUri, AadAudienceId, AadIssuerUri가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1745">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="5d3f2-1746">Set-AzVirtualNetworkGateway가 업데이트됨: 게이트웨이에서 VpnClient AAD 인증 옵션을 제거할 수 있도록 선택적인 스위치 매개 변수 RemoveAadAuthentication이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1746">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="5d3f2-1747">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1747">Az.OperationalInsights</span></span>
* <span data-ttu-id="5d3f2-1748">'New-AzureRmOperationalInsightsWorkspace' 명령에서 **pergb2018** 가격 책정 계층 사용</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1748">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="5d3f2-1749">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1749">Az.Resources</span></span>
* <span data-ttu-id="5d3f2-1750">추가 템플릿 내보내기 옵션 지원</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1750">Support for additional Template Export options</span></span>
    - <span data-ttu-id="5d3f2-1751">Export-AzResourceGroup에 '-SkipResourceNameParameterization' 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1751">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="5d3f2-1752">Export-AzResourceGroup에 '-SkipAllParameterization' 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1752">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="5d3f2-1753">내보낸 리소스 필터링을 위해 Export-AzResourceGroup에 '-Resource' 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1753">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="5d3f2-1754">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1754">Az.ServiceFabric</span></span>
* <span data-ttu-id="5d3f2-1755">일부 경우 잘못된 지문을 가져오는 추가 인증서 ByExistingKeyVault 수정</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1755">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="5d3f2-1756">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1756">Az.Sql</span></span>
* <span data-ttu-id="5d3f2-1757">Advanced Threat Protection 스토리지 엔드포인트 접미사 수정</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1757">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="5d3f2-1758">Advanced Data Security가 Advanced Threat Protection 정책을 재정의하는 것을 수정</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1758">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="5d3f2-1759">고객이 TDE 키를 추가하고 관리되는 인스턴스에 TDE 보호기를 설정할 수 있도록 Management.Sql용 새 Cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1759">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="5d3f2-1760">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1760">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="5d3f2-1761">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1761">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="5d3f2-1762">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1762">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="5d3f2-1763">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1763">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="5d3f2-1764">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1764">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="5d3f2-1765">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1765">Az.Storage</span></span>
* <span data-ttu-id="5d3f2-1766">스토리지 계정 생성 시 종류 FileStorage 및 SkuName Premium_ZRS 지원</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1766">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="5d3f2-1767">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1767">New-AzStorageAccount</span></span>
* <span data-ttu-id="5d3f2-1768">BLOB immutability cmdlet의 설명 명확화</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1768">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="5d3f2-1769">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1769">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="5d3f2-1770">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1770">Az.Websites</span></span>
* <span data-ttu-id="5d3f2-1771">Get-AzWebAppCertificate를 클라이언트 대신 서버의 리소스 그룹별로 필터링하도록 최적화</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1771">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="5d3f2-1772">Get-AzWebAppSnapshot에 -UseDisasterRecovery 스위치 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1772">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="5d3f2-1773">2.2.0 - 2019년 6월</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1773">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="5d3f2-1774">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1774">Az.Cdn</span></span>
* <span data-ttu-id="5d3f2-1775">cmdlet에서 2019-04-15 API 버전 기반의 rulesEngine 기능을 지원하도록 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1775">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="5d3f2-1776">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1776">Az.Compute</span></span>
* <span data-ttu-id="5d3f2-1777">작업을 시작하여 완료되기 전에 즉시 반환하는 `NoWait` 매개 변수가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1777">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="5d3f2-1778">다음 Cmdlet이 업데이트 되었습니다.   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1778">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="5d3f2-1779">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1779">Az.EventHub</span></span>
* <span data-ttu-id="5d3f2-1780">#9231 수정 - Get-AzEventHubNamespace에서 태그를 반환하지 않음</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1780">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="5d3f2-1781">#9230 수정 - Get-AzEventHubNamespace에서 ResourceGroupName 대신 ResourceGroup을 반환함</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1781">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="5d3f2-1782">Az.Network</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1782">Az.Network</span></span>
* <span data-ttu-id="5d3f2-1783">Nat Gateway에 대한 ResourceId 및 InputObject 업데이트</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1783">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="5d3f2-1784">ResourceId 및 InputObject에 대한 별칭 추가</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1784">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="5d3f2-1785">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1785">Az.PolicyInsights</span></span>
* <span data-ttu-id="5d3f2-1786">Get-AzPolicyEvent에서 Null 참조 문제 해결</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1786">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="5d3f2-1787">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1787">Az.RecoveryServices</span></span>
* <span data-ttu-id="5d3f2-1788">IaaSVM 정책 최소 보존 기간(일)이 1에서 7로 변경됨</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1788">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="5d3f2-1789">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1789">Az.ServiceBus</span></span>
* <span data-ttu-id="5d3f2-1790">#9182 문제 해결 - Get-AzServiceBusNamespace에서 ResourceGroupName 대신 ResourceGroup을 반환</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1790">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="5d3f2-1791">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1791">Az.ServiceFabric</span></span>
* <span data-ttu-id="5d3f2-1792">'Update-AzServiceFabricReliability' 오류 메시지의 오타 수정</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1792">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="5d3f2-1793">Service Fabric 명령줄에서 누락된 문자 수정</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1793">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="5d3f2-1794">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1794">Az.Sql</span></span>
* <span data-ttu-id="5d3f2-1795">Managed Instance에 대한 AutoDr을 지원하기 위해 New-AzureSqlInstance cmdlet에 대한 DnsZonePartner 매개 변수를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1795">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="5d3f2-1796">Get-AzSqlDatabaseSecureConnectionPolicy cmdlet 사용 중단</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1796">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="5d3f2-1797">Threat Detection(위협 탐지) cmdlet 이름을 Advanced Threat Protection으로 변경함</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1797">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="5d3f2-1798">새 AzSqlInstance -StorageSizeInGB 및 -LicenseType 매개 변수는 이제 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1798">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="5d3f2-1799">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1799">Az.Websites</span></span>
* <span data-ttu-id="5d3f2-1800">-WebApp 속성에서 Set-AzWebApp 및 Set-AzWebAppSlot을 사용하면 태그가 제거되는 문제를 해결함</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1800">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="5d3f2-1801">2.1.0 - 2019년 5월</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1801">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="5d3f2-1802">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1802">Az.ApiManagement</span></span>
* <span data-ttu-id="5d3f2-1803">글로벌 및 API 범위에서 진단을 관리하기 위한 새 cmdlet을 만들었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1803">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="5d3f2-1804">**Get-AzApiManagementDiagnostic** - 글로벌 또는 API 범위가 구성된 진단 가져오기</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1804">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="5d3f2-1805">**New-AzApiManagementDiagnostic** - 글로벌 범위 또는 API 범위에서 새 진단 만들기</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1805">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="5d3f2-1806">**New-AzApiManagementHttpMessageDiagnostic** - 기록할 Headers(헤더) 및 Body Bytes(본문 바이트 수) 크기에 대한 진단 설정 만들기</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1806">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="5d3f2-1807">**New-AzApiManagementPipelineDiagnosticSetting** - 게이트웨이로 들어오고 나가는 HTTP 메시지에 대한 진단 설정 만들기</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1807">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="5d3f2-1808">**New-AzApiManagementSamplingSetting** - 진단 요청/응답에 대한 샘플링 설정 만들기</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1808">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="5d3f2-1809">**Remove-AzApiManagementDiagnostic** - 글로벌 또는 API 범위에서 진단 엔터티 제거</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1809">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="5d3f2-1810">**Set-AzApiManagementDiagnostic** - 글로벌 또는 API 범위에서 진단 엔터티 업데이트</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1810">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="5d3f2-1811">ApiManagement 서비스에서 캐시를 관리하기 위한 새 cmdlet을 만들었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1811">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="5d3f2-1812">**Get-AzApiManagementCache** - 식별자 또는 모든 캐시로 지정된 캐시의 세부 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1812">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="5d3f2-1813">**New-AzApiManagementCache** - 특정 Azure 'region'(지역)에 새 'default'(기본) 캐시 만들기</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1813">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="5d3f2-1814">**Remove-AzApiManagementCache** - 캐시 제거</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1814">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="5d3f2-1815">**Update-AzApiManagementCache** - 캐시 업데이트</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1815">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="5d3f2-1816">API 스키마 관리하기 위한 새 cmdlet을 만들었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1816">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="5d3f2-1817">**New-AzApiManagementSchema** - API에 대한 새 스키마 만들기</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1817">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="5d3f2-1818">**Get-AzApiManagementSchema** - API에 구성된 스키마 가져오기</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1818">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="5d3f2-1819">**Remove-AzApiManagementSchema** - API에 구성된 스키마 제거</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1819">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="5d3f2-1820">**Set-AzApiManagementSchema** - API에 구성된 스키마 업데이트</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1820">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="5d3f2-1821">사용자 토큰을 생성하기 위한 새 cmdlet을 만들었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1821">Created new Cmdlet for generating a User Token.</span></span>
    - <span data-ttu-id="5d3f2-1822">**New-AzApiManagementUserToken** - 기본적으로 8시간 동안 유효한 새 사용자 토큰을 생성합니다. 'GIT' 사용자에 대한 토큰은 이 cmdlet을 사용하여 생성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1822">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="5d3f2-1823">네트워크 상태를 검색하기 위한 새 cmdlet을 만들었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1823">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="5d3f2-1824">**Get-AzApiManagementNetworkStatus** - API Management 서비스에서 사용하는 리소스의 네트워크 상태 연결을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1824">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="5d3f2-1825">ApiManagement 서비스를 가상 네트워크에 배포하고 종속성이 손상되었는지 여부를 확인할 때 유용합니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1825">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="5d3f2-1826">**New-AzApiManagement** cmdlet에서 ApiManagement 서비스를 관리하도록 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1826">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span>
    - <span data-ttu-id="5d3f2-1827">새 '소비' SKU 지원이 추가됨</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1827">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="5d3f2-1828">'소비' SKU에 대해 'EnableClientCertificate' 플래그를 설정하기 위한 지원이 추가됨</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1828">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="5d3f2-1829">새 **New-AzApiManagementSslSetting** cmdlet을 사용하면 'Backend(백 엔드)' 및 'Frontend'(프런트 엔드)에서 'TLS/SSL' 설정을 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1829">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="5d3f2-1830">또한 ApiManagement 서비스의 'Frontend'에서 '3DES'와 같은 'Ciphers'와 'Http2'와 같은 'ServerProtocols'를 구성하는 데 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1830">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="5d3f2-1831">ApiManagement 서비스에서 'DeveloperPortal' 호스트 이름을 구성하기 위한 지원이 추가됨</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1831">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="5d3f2-1832">**Get-AzApiManagementSsoToken** cmdlet에서 'PsApiManagement' 개체를 입력으로 사용하도록 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1832">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="5d3f2-1833">cmdlet에서 오류 메시지를 인라인으로 표시하도록 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1833">Updated the cmdlet to display Error Messages inline</span></span>
     > <span data-ttu-id="5d3f2-1834">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : 오류 코드: ValidationError 오류 메시지: 하나 이상의 필드에 잘못된 값이 있습니다. 오류 세부 정보:    [Code=ValidationError, Message=줄 3, 열 10의 'log-to-eventhub' 요소에 오류가 있습니다.: 로거를 찾지 못함, Target=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1834">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="5d3f2-1835">**Export-AzApiManagementApi** cmdlet에서 API를 'OpenApi 3.0' 형식으로 내보내도록 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1835">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="5d3f2-1836">**Import-AzApiManagementApi** cmdlet을 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1836">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="5d3f2-1837">'OpenApi 3.0' 문서 사양에서 API 가져오기</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1837">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="5d3f2-1838">문서('Swagger', 'Wadl', 'Wsdl', 'OpenApi')에 지정된 'PsApiManagementSchema' 속성 재정의</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1838">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="5d3f2-1839">문서에 지정된 'ServiceUrl' 속성 재정의</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1839">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="5d3f2-1840">**Get-AzApiManagementPolicy** cmdlet에서 'rawxml'을 사용하여 이스케이프된 비 Xml 'format'(형식)의 정책을 반환하도록 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1840">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="5d3f2-1841">**Set-AzApiManagementPolicy** cmdlet에서 'rawxml'을 사용하여 이스케이프된 비 Xml 'format'의 정책을 수락하고, 'xml'을 사용하여 이스케이프된 Xml 'format'의 정책을 수락하도록 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1841">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="5d3f2-1842">**New-AzApiManagementApi** cmdlet을 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1842">Updated cmdlet **New-AzApiManagementApi**</span></span>
    - <span data-ttu-id="5d3f2-1843">'OpenId' 권한 부여 서버를 사용하여 API 구성</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1843">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="5d3f2-1844">'ApiVersionSet'에서 API 만들기</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1844">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="5d3f2-1845">'SourceApiId' 및 'SourceApiRevision'을 사용하여 API 복제</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1845">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="5d3f2-1846">API 범위에서 'SubscriptionRequired' 구성 가능</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1846">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="5d3f2-1847">**Set-AzApiManagementApi** cmdlet을 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1847">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="5d3f2-1848">'OpenId' 권한 부여 서버를 사용하여 API 구성</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1848">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="5d3f2-1849">API를 'ApiVersionSet'으로 업데이트</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1849">To updated an API into an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="5d3f2-1850">API 범위에서 'SubscriptionRequired' 구성 가능</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1850">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="5d3f2-1851">**New-AzApiManagementRevision** cmdlet을 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1851">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="5d3f2-1852">'SourceApiRevision'을 사용하여 기존 수정 버전 복제(태그, 제품, 작업 및 정책 복사).</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1852">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="5d3f2-1853">새 수정 버전은 부모의 'ApiId'를 가정합니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1853">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="5d3f2-1854">'ApiRevisionDescription' 제공</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1854">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="5d3f2-1855">API 복제 시 'ServiceUrl' 재정의</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1855">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="5d3f2-1856">**New-AzApiManagementIdentityProvider** cmdlet을 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1856">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="5d3f2-1857">'Authority'를 사용하여 'AAD' 또는 'AADB2C' 구성</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1857">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="5d3f2-1858">'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' 및 'PasswordResetPolicy' 설정</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1858">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="5d3f2-1859">**New-AzApiManagementSubscription** cmdlet을 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1859">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="5d3f2-1860">'Scope' 및 'UserId'를 사용하여 새 SubscriptonModel 설명</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1860">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="5d3f2-1861">'ProductId' 및 'UserId'를 사용하여 이전 구독 모델 설명</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1861">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="5d3f2-1862">구독 수준에서 'AllowTracing'을 사용하도록 설정하는 지원 추가</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1862">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="5d3f2-1863">**Set-AzApiManagementSubscription** cmdlet을 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1863">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="5d3f2-1864">'Scope' 및 'UserId'를 사용하여 새 SubscriptonModel 설명</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1864">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="5d3f2-1865">'ProductId' 및 'UserId'를 사용하여 이전 구독 모델 설명</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1865">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="5d3f2-1866">구독 수준에서 'AllowTracing'을 사용하도록 설정하는 지원 추가</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1866">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="5d3f2-1867">다음 cmdlet에서 'ResourceId'를 입력으로 수락하도록 업데이트했습니다</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1867">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="5d3f2-1868">'New-AzApiManagementContext'</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1868">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="5d3f2-1869">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1869">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="5d3f2-1870">'Get-AzApiManagementApiRelease'</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1870">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="5d3f2-1871">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1871">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="5d3f2-1872">'Get-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1872">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="5d3f2-1873">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1873">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="5d3f2-1874">'Get-AzApiManagementAuthorizationServer'</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1874">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="5d3f2-1875">'Get-AzApiManagementBackend'</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1875">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="5d3f2-1876">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1876">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="5d3f2-1877">'Get-AzApiManagementCertificate'</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1877">'Get-AzApiManagementCertificate'</span></span>
    - <span data-ttu-id="5d3f2-1878">'Remove-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1878">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="5d3f2-1879">'Remove-AzApiManagementSubscription'</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1879">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="5d3f2-1880">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1880">Az.Automation</span></span>
* <span data-ttu-id="5d3f2-1881">Get-AzAutomationJobOutputRecord에서 JSON 및 Text 레코드 값을 처리하도록 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1881">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="5d3f2-1882">문제 https://github.com/Azure/azure-powershell/issues/7977 수정</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1882">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="5d3f2-1883">문제 https://github.com/Azure/azure-powershell/issues/8600 수정</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1883">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="5d3f2-1884">Start-AzAutomationDscCompilationJob에서 완료될 때까지 기다리지 않고 작업을 바로 시작하도록 변경했습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1884">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="5d3f2-1885">문제 https://github.com/Azure/azure-powershell/issues/8347 수정</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1885">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="5d3f2-1886">-Name을 사용하면 모든 노드를 반환하는 Get-AzAutomationDscNode 수정.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1886">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="5d3f2-1887">이제 일치하는 노드만 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1887">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="5d3f2-1888">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1888">Az.Compute</span></span>
* <span data-ttu-id="5d3f2-1889">ProtectFromScaleIn 및 ProtectFromScaleSetAction 매개 변수를 Update-AzVmssVM cmdlet에 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1889">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="5d3f2-1890">'East US'(미국 동부)가 지원되지 않는 경우 이제 New-AzVM wimple 매개 변수 집합에서 기본적으로 사용 가능한 위치를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1890">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="5d3f2-1891">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1891">Az.DataLakeStore</span></span>
* <span data-ttu-id="5d3f2-1892">ADLS SDK에서 httpclient를 사용하도록 업데이트하고, 데이터 평면 테스트를 Azure 프레임워크와 통합합니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1892">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="5d3f2-1893">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1893">Az.Monitor</span></span>
* <span data-ttu-id="5d3f2-1894">도움말 예제에서 잘못된 매개 변수 이름을 수정했습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1894">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="5d3f2-1895">Az.Network</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1895">Az.Network</span></span>
* <span data-ttu-id="5d3f2-1896">DisableBgpRoutePropagation 플래그를 유효 경로 테이블 출력에 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1896">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="5d3f2-1897">업데이트된 cmdlet:</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1897">Updated cmdlet:</span></span>
        - <span data-ttu-id="5d3f2-1898">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1898">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="5d3f2-1899">New-AzApplicationGatewayTrustedRootCertificate 설명서에서 이중 파선을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1899">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="5d3f2-1900">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1900">Az.Resources</span></span>
* <span data-ttu-id="5d3f2-1901">할당 거부를 검색하기 위한 새 Get-AzureRmDenyAssignment cmdlet을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1901">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="5d3f2-1902">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1902">Az.Sql</span></span>
* <span data-ttu-id="5d3f2-1903">Advanced Threat Protection cmdlet의 이름을 Advanced Data Security로 변경하고, 취약성 평가를 기본적으로 사용하도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1903">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="5d3f2-1904">2.0.0 - 2019년 5월</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1904">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="5d3f2-1905">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1905">Az.Accounts</span></span>
* <span data-ttu-id="5d3f2-1906">사용자 이름/비밀번호 인증을 사용하여 ADFS 문제를 해결하도록 인증 라이브러리 업데이트</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1906">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="5d3f2-1907">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1907">Az.CognitiveServices</span></span>
* <span data-ttu-id="5d3f2-1908">Bing Search 서비스에 대해서만 Bing 면책 조항을 표시하세요.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1908">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="5d3f2-1909">계정 생성 실패 시 오류 개선.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1909">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="5d3f2-1910">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1910">Az.Compute</span></span>
* <span data-ttu-id="5d3f2-1911">근접 배치 그룹 기능</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1911">Proximity placement group feature.</span></span>
    - <span data-ttu-id="5d3f2-1912">다음과 같은 새 cmdlet을 추가했습니다.   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1912">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="5d3f2-1913">새 매개 변수 ProximityPlacementGroupId가 다음 cmdlet에 추가됩니다.   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1913">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="5d3f2-1914">New-AzGalleryImageVersion에 StorageAccountType 매개 변수가 추가됩니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1914">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="5d3f2-1915">New-AzGalleryImageVersion의 TargetRegion이 StorageAccountType를 포함할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1915">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="5d3f2-1916">SkipShutdown 스위치 매개 변수가 Stop-AzVM 및 Stop-AzVmss에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1916">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>
* <span data-ttu-id="5d3f2-1917">주요 변경 내용</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1917">Breaking changes</span></span>
    - <span data-ttu-id="5d3f2-1918">Set-AzVMBootDiagnostics이 Set-AzVMBootDiagnostic으로 변경됩니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1918">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="5d3f2-1919">Export-AzLogAnalyticThrottledRequests이 Export-AzLogAnalyticThrottledRequests로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1919">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="5d3f2-1920">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1920">Az.DeploymentManager</span></span>
* <span data-ttu-id="5d3f2-1921">Azure 배포 관리자 cmdlet의 일반적으로 사용 가능한 첫 번째 릴리스</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1921">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="5d3f2-1922">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1922">Az.Dns</span></span>
* <span data-ttu-id="5d3f2-1923">자동 DNS 이름 서버 위임</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1923">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="5d3f2-1924">DNS 영역 만들기 cmdlet은 추가 선택적 매개 변수로 부모 영역 이름을 허용합니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1924">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="5d3f2-1925">새로 생성 된 자식 영역의 부모 영역에 NS 레코드를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1925">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="5d3f2-1926">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1926">Az.FrontDoor</span></span>
* <span data-ttu-id="5d3f2-1927">Azure FrontDoor cmdlet의 일반적으로 사용 가능한 첫 번째 릴리스</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1927">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="5d3f2-1928">'Waf'를 포함하도록 WAF cmdlet의 이름 바꾸기</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1928">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="5d3f2-1929">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1929">Az.HDInsight</span></span>
* <span data-ttu-id="5d3f2-1930">두 개의 cmdlet을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1930">Removed two cmdlets:</span></span>
    - <span data-ttu-id="5d3f2-1931">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1931">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="5d3f2-1932">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1932">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="5d3f2-1933">Grant-AzHDInsightHttpServicesAccess를 대체할 새 cmdlet Set-AzHDInsightGatewayCredential을 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1933">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="5d3f2-1934">reader 역할과 HDInsight 운영자 역할을 구분하도록 cmdlet Get-AzHDInsightJobOutput 업데이트:</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1934">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="5d3f2-1935">reader 역할을 가진 사용자는 'DefaultStorageAccountKey'매개 변수를 명시적으로 지정해야 합니다. 그렇지 않으면 오류가 발생합니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1935">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="5d3f2-1936">Hdinsight 운영자 역할을 가진 사용자를 영향을 받지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1936">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="5d3f2-1937">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1937">Az.Monitor</span></span>
* <span data-ttu-id="5d3f2-1938">SQR API(예약 쿼리 규칙)용 새 cmdlet</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1938">New cmdlets for SQR API (Scheduled Query Rule)</span></span>
    - <span data-ttu-id="5d3f2-1939">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1939">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="5d3f2-1940">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1940">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="5d3f2-1941">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1941">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="5d3f2-1942">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1942">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="5d3f2-1943">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1943">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="5d3f2-1944">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1944">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="5d3f2-1945">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1945">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="5d3f2-1946">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1946">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="5d3f2-1947">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1947">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="5d3f2-1948">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1948">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="5d3f2-1949">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1949">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="5d3f2-1950">SQR API에 대한 [자세한 내용](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules)</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1950">[More](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="5d3f2-1951">GenV2(비 클래식) 메트릭 기반 경고 규칙에 대한 cmdlet을 포함하도록 Az.Monitor.md가 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1951">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="5d3f2-1952">Az.Network</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1952">Az.Network</span></span>
* <span data-ttu-id="5d3f2-1953">Nat 게이트웨이 리소스에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1953">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="5d3f2-1954">새로운 cmdlet</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1954">New cmdlets</span></span>
        - <span data-ttu-id="5d3f2-1955">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1955">New-AzNatGateway</span></span>
        - <span data-ttu-id="5d3f2-1956">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1956">Get-AzNatGateway</span></span>
        - <span data-ttu-id="5d3f2-1957">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1957">Set-AzNatGateway</span></span>
        - <span data-ttu-id="5d3f2-1958">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1958">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="5d3f2-1959">다음 Cmdlet이 업데이트 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1959">Updated cmdlets</span></span>
        - <span data-ttu-id="5d3f2-1960">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1960">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="5d3f2-1961">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1961">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="5d3f2-1962">기능에 대한 새로운 명령이 업데이트됨: Brooklyn Gateway에서 사용자 지정 경로 설정/제거.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1962">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="5d3f2-1963">New-AzVirtualNetworkGateway가 업데이트됨: 선택적 매개 변수 -CustomRoute를 추가하여 게이트웨이에서 설정할 사용자 지정 경로로 주소 접두사를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1963">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="5d3f2-1964">Set-AzVirtualNetworkGateway가 업데이트됨: 선택적 매개 변수 -CustomRoute를 추가하여 게이트웨이에서 설정할 사용자 지정 경로로 주소 접두사를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1964">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="5d3f2-1965">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1965">Az.PolicyInsights</span></span>
* <span data-ttu-id="5d3f2-1966">정책 평가 세부 정보 쿼리 지원</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1966">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="5d3f2-1967">Get-AzPolicyState에 '-Expand'매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1967">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="5d3f2-1968">'-Expand PolicyEvaluationDetails' 지원</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1968">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="5d3f2-1969">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1969">Az.RecoveryServices</span></span>
* <span data-ttu-id="5d3f2-1970">크로스 구독 Azure에서 Azure 사이트 복구 지원</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1970">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="5d3f2-1971">Azure Site Recovery에 대한 호환성이 손상되는 변경 표시</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1971">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="5d3f2-1972">Azure Site Recovery 복구 계획 최종 실행 계획에 대한 수정</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1972">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="5d3f2-1973">Azure에서 Azure에 대한 Azure Site Recovery 업데이트 네트워크 매핑 수정</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1973">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="5d3f2-1974">관리 디스크에 대한 Azure에서 Azure에 대한 Azure Site Recovery 업데이트 보호 방향 수정</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1974">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="5d3f2-1975">기타 사소한 수정.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1975">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="5d3f2-1976">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1976">Az.Relay</span></span>
* <span data-ttu-id="5d3f2-1977">고객 관련 메시지의 철자 오류 수정</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1977">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="5d3f2-1978">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1978">Az.ServiceBus</span></span>
* <span data-ttu-id="5d3f2-1979">네임스페이스의 NetworkRuleSet에 대한 새 cmdlet가 추가되었습니다</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1979">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="5d3f2-1980">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1980">Az.Storage</span></span>
* <span data-ttu-id="5d3f2-1981">저장소 클라이언트 라이브러리 10.0.1로 업그레이드(이 SDK의 모든 개체의 네임스페이스가 'Microsoft.WindowsAzure.Storage. *'에서 'Microsoft.Azure.Storage.* '로 변경됨)</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1981">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="5d3f2-1982">새로운 API 버전 2019-04-01을 지원하기 위해 Microsoft.Azure.Management.Storage 11.0.0으로 업그레이드합니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1982">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="5d3f2-1983">스토리지 생성 계정의 기본 스토리지 계정 종류가 'Storage'에서 'StorageV2'로 변경됩니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1983">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="5d3f2-1984">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1984">New-AzStorageAccount</span></span>
* <span data-ttu-id="5d3f2-1985">'StandardLRS'가 'Standard_LRS'로 변경되는 것과 같이 '-'을 추가하여 입력 SkuName과 정렬되도록 스토리지 계정 cmdlet 출력 Sku.Name을 변경합니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1985">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="5d3f2-1986">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1986">New-AzStorageAccount</span></span>
    - <span data-ttu-id="5d3f2-1987">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1987">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="5d3f2-1988">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1988">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="5d3f2-1989">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1989">Az.Websites</span></span>
* <span data-ttu-id="5d3f2-1990">Get-AzWebApp에서 반환한 PSSite 개체에 대해 'Kind'속성이 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1990">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="5d3f2-1991">Get-AzWebApp\* 메트릭 및 Get-AzAppServicePlanMetrics가 사용되지 않음으로 표시되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1991">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="5d3f2-1992">1.8.0 - 2019년 4월</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1992">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="5d3f2-1993">마지막 주 릴리스 이후의 주요 사항</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1993">Highlights since the last major release</span></span>
* <span data-ttu-id="5d3f2-1994">`Az` 모듈 일반 공급</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1994">General availability of `Az` module</span></span>
* <span data-ttu-id="5d3f2-1995">`Az` 모듈에 대한 자세한 내용은 https://aka.ms/azps-announce 를 방문하세요.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1995">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="5d3f2-1996">Location, ResourceGroup 및 ResourceName 완성자가 추가되었습니다(https://azure.microsoft.com/blog/completers-in-azure-powershell/ ).</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1996">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="5d3f2-1997">와일드카드 지원이 Az.Compute 및 Az.Network에 대한 Get cmdlet에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1997">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="5d3f2-1998">Windows PowerShell 5.1 전용 대화형 사용자 이름/암호 인증이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1998">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="5d3f2-1999">Python 2 Runbook 지원이 Az.Automation에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-1999">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="5d3f2-2000">Az.LogicApp: 통합 계정 어셈블리 및 일괄 처리 구성을 위한 새로운 cmdlet입니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2000">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="5d3f2-2001">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2001">Az.Accounts</span></span>
* <span data-ttu-id="5d3f2-2002">Mac에서 모듈을 올바르게 삭제하기 위해 Uninstall-AzureRm을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2002">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="5d3f2-2003">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2003">Az.Batch</span></span>
* <span data-ttu-id="5d3f2-2004">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2004">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="5d3f2-2005">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2005">Az.Cdn</span></span>
* <span data-ttu-id="5d3f2-2006">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2006">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="5d3f2-2007">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2007">Az.CognitiveServices</span></span>
* <span data-ttu-id="5d3f2-2008">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2008">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="5d3f2-2009">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2009">Az.Compute</span></span>
* <span data-ttu-id="5d3f2-2010">디스크의 리소스 ID에 리소스 ID의 소문자 resourcegroups가 있는 경우 AEM 설치 문제 수정</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2010">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="5d3f2-2011">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2011">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="5d3f2-2012">와일드 카드에 대한 설명서 수정</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2012">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="5d3f2-2013">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2013">Az.DataFactory</span></span>
* <span data-ttu-id="5d3f2-2014">NodeCount가 관리형 통합 런타임에 대해 Null이 아닌 경우 SsisProperties를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2014">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="5d3f2-2015">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2015">Az.DataLakeStore</span></span>
* <span data-ttu-id="5d3f2-2016">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2016">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="5d3f2-2017">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2017">Az.EventGrid</span></span>
* <span data-ttu-id="5d3f2-2018">이벤트 구독 cmdlet 만들기/업데이트를 사용하기 전에 리소스를 만들어야 함을 나타내기 위해 엔드포인트의 도움말 텍스트가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2018">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="5d3f2-2019">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2019">Az.EventHub</span></span>
* <span data-ttu-id="5d3f2-2020">네임스페이스의 NetworkRuleSet에 대한 새 cmdlet가 추가되었습니다</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2020">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="5d3f2-2021">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2021">Az.HDInsight</span></span>
* <span data-ttu-id="5d3f2-2022">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2022">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="5d3f2-2023">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2023">Az.IotHub</span></span>
* <span data-ttu-id="5d3f2-2024">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2024">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="5d3f2-2025">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2025">Az.KeyVault</span></span>
* <span data-ttu-id="5d3f2-2026">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2026">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="5d3f2-2027">와일드 카드에 대한 설명서 수정</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2027">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="5d3f2-2028">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2028">Az.MachineLearning</span></span>
* <span data-ttu-id="5d3f2-2029">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2029">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="5d3f2-2030">Az.Media</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2030">Az.Media</span></span>
* <span data-ttu-id="5d3f2-2031">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2031">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="5d3f2-2032">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2032">Az.Monitor</span></span>
  * <span data-ttu-id="5d3f2-2033">GenV2(비 클래식) 메트릭 기반 경고 규칙에 대한 새 cmdlet</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2033">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="5d3f2-2034">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2034">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="5d3f2-2035">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2035">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="5d3f2-2036">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2036">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="5d3f2-2037">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2037">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="5d3f2-2038">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2038">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="5d3f2-2039">모니터 SDK가 버전 0.22.0-preview로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2039">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="5d3f2-2040">Az.Network</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2040">Az.Network</span></span>
* <span data-ttu-id="5d3f2-2041">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2041">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="5d3f2-2042">와일드 카드에 대한 설명서 수정</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2042">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="5d3f2-2043">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2043">Az.NotificationHubs</span></span>
* <span data-ttu-id="5d3f2-2044">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2044">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="5d3f2-2045">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2045">Az.OperationalInsights</span></span>
* <span data-ttu-id="5d3f2-2046">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2046">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="5d3f2-2047">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2047">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="5d3f2-2048">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2048">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="5d3f2-2049">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2049">Az.RecoveryServices</span></span>
* <span data-ttu-id="5d3f2-2050">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2050">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="5d3f2-2051">Azure VM의 SQL용 테이블 형식이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2051">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="5d3f2-2052">AzureFileShare에서 위치를 가져오는 대체 메서드가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2052">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="5d3f2-2053">시간대에 따라 SchedulePolicy 개체의 ScheduleRunDays가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2053">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="5d3f2-2054">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2054">Az.RedisCache</span></span>
* <span data-ttu-id="5d3f2-2055">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2055">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="5d3f2-2056">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2056">Az.Resources</span></span>
* <span data-ttu-id="5d3f2-2057">와일드 카드에 대한 설명서 수정</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2057">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="5d3f2-2058">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2058">Az.Sql</span></span>
* <span data-ttu-id="5d3f2-2059">Monitor SDK의 종속성을 공용 코드로 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2059">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="5d3f2-2060">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2060">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="5d3f2-2061">다중 열 분류 프로세스가 향상되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2061">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="5d3f2-2062">기본적으로 Get-AzSqlServerServiceObjective의 응답으로 SKU 속성(SKU 이름, 제품군, 용량)과 테이블 형식을 포함합니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2062">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="5d3f2-2063">해당 지역에 기존 서버 없이 위치별로 Get-AzSqlServerServiceObjective를 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2063">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="5d3f2-2064">관리형 인스턴스 생성 시 표준 시간대 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2064">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="5d3f2-2065">와일드 카드에 대한 설명서 수정</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2065">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="5d3f2-2066">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2066">Az.Websites</span></span>
* <span data-ttu-id="5d3f2-2067">실행 시 태그를 제거하지 않도록 Set-AzWebApp 및 Set-AzWebAppSlot를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2067">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="5d3f2-2068">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2068">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="5d3f2-2069">WebSites SDK가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2069">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="5d3f2-2070">PSAppServicePlan에서 AdminSiteName 속성을 제거했습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2070">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="5d3f2-2071">1.7.0 - 2019년 4월</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2071">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="5d3f2-2072">마지막 주 릴리스 이후의 주요 사항</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2072">Highlights since the last major release</span></span>
* <span data-ttu-id="5d3f2-2073">`Az` 모듈 일반 공급</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2073">General availability of `Az` module</span></span>
* <span data-ttu-id="5d3f2-2074">`Az` 모듈에 대한 자세한 내용은 https://aka.ms/azps-announce 를 방문하세요.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2074">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="5d3f2-2075">Location, ResourceGroup 및 ResourceName 완성자가 추가되었습니다(https://azure.microsoft.com/blog/completers-in-azure-powershell/ ).</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2075">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="5d3f2-2076">와일드카드 지원이 Az.Compute 및 Az.Network에 대한 Get cmdlet에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2076">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="5d3f2-2077">Windows PowerShell 5.1 전용 대화형 사용자 이름/암호 인증이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2077">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="5d3f2-2078">Python 2 Runbook 지원이 Az.Automation에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2078">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="5d3f2-2079">Az.LogicApp: 통합 계정 어셈블리 및 일괄 처리 구성을 위한 새로운 cmdlet입니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2079">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="5d3f2-2080">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2080">Az.Accounts</span></span>
* <span data-ttu-id="5d3f2-2081">매개 변수 AzureAnalysisServicesEndpointResourceId를 허용하도록 Add-AzEnvironment 및 Set-AzEnvironment 업데이트</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2081">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="5d3f2-2082">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2082">Az.AnalysisServices</span></span>
* <span data-ttu-id="5d3f2-2083">데이터 평면 cmdlet에서 ServiceClient 사용 및 원본 인증 논리 제거</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2083">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="5d3f2-2084">호환성이 손상되는 변경을 방지하기 위해 Add-AzureASAccount를 Connect-AzAccount의 래퍼로 만듦</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2084">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="5d3f2-2085">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2085">Az.Automation</span></span>
* <span data-ttu-id="5d3f2-2086">포함에 대한 New-AzAutomationSoftwareUpdateConfiguration cmdlet 버그 수정</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2086">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="5d3f2-2087">이제 매개 변수 IncludedKbNumber 및 IncludedPackageNameMask가 작동함</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2087">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="5d3f2-2088">Azure 자동화 업데이트 관리 동적 그룹에 대한 버그 수정</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2088">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="5d3f2-2089">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2089">Az.Compute</span></span>
* <span data-ttu-id="5d3f2-2090">New-AzDiskConfig 및 New-AzSnapshotConfig에 HyperVGeneration 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2090">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="5d3f2-2091">다른 테넌트의 갤러리 이미지를 사용하여 VM을 만들 수 있음</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2091">Allow VM creation with galley image from other tenants.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="5d3f2-2092">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2092">Az.ContainerInstance</span></span>
* <span data-ttu-id="5d3f2-2093">후행 빈 인수를 추가한 New-AzContainerGroup의 -Command 매개 변수의 문제 수정</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2093">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="5d3f2-2094">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2094">Az.DataFactory</span></span>
* <span data-ttu-id="5d3f2-2095">ADF .Net SDK 버전을 3.0.2로 업데이트</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2095">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="5d3f2-2096">RepoConfiguration 관련 설정에 대한 추가 매개 변수로 Set-AzDataFactoryV2 cmdlet을 업데이트</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2096">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="5d3f2-2097">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2097">Az.Resources</span></span>
* <span data-ttu-id="5d3f2-2098">'-ResourceId' 또는 '-ResourceGroupName', '-Name' 및 '-ResourceType' 매개 변수를 제공할 때 'Get-AzResource'에 대한 공급자 처리 개선</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2098">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="5d3f2-2099">'Test-AzDeployment' 및 'Test-AzResourceGroupDeployment'에 대한 오류 처리 개선</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2099">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="5d3f2-2100">배포 유효성 검사 외부에서 발생한 오류를 처리하고 그 대신 명령의 출력에 포함</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2100">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="5d3f2-2101">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/6856 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2101">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="5d3f2-2102">배포 cmdlet 세트에 스크립트 및 작업 시나리오에서 프롬프트를 건너뛰는 '-IgnoreDynamicParameters' 스위치 추가</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2102">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="5d3f2-2103">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/6856 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2103">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="5d3f2-2104">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2104">Az.Sql</span></span>
* <span data-ttu-id="5d3f2-2105">데이터베이스 데이터 분류 지원</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2105">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="5d3f2-2106">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2106">Az.Storage</span></span>
* <span data-ttu-id="5d3f2-2107">매개 변수 -UseConnectedAccount를 사용하여 스토리지 컨텍스트를 만들 때 자세한 오류 보고(단, 로그인 Azure 계정 없이)</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2107">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="5d3f2-2108">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2108">New-AzStorageContext</span></span>
* <span data-ttu-id="5d3f2-2109">관리 평면 API를 사용하여 지정한 스토리지 계정의 BLOB 서비스 속성 관리 지원</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2109">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="5d3f2-2110">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2110">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="5d3f2-2111">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2111">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="5d3f2-2112">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2112">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="5d3f2-2113">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2113">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="5d3f2-2114">BLOB 및 파일 업로드/다운로드 cmdlet에 대한 -AsJob 지원</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2114">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="5d3f2-2115">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2115">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="5d3f2-2116">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2116">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="5d3f2-2117">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2117">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="5d3f2-2118">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2118">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="5d3f2-2119">1.6.0 - 2019년 3월</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2119">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="5d3f2-2120">마지막 주 릴리스 이후의 주요 사항</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2120">Highlights since the last major release</span></span>
* <span data-ttu-id="5d3f2-2121">`Az` 모듈 일반 공급</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2121">General availability of `Az` module</span></span>
* <span data-ttu-id="5d3f2-2122">`Az` 모듈에 대한 자세한 내용은 https://aka.ms/azps-announce 를 방문하세요.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2122">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="5d3f2-2123">Location, ResourceGroup 및 ResourceName 완성자가 추가되었습니다(https://azure.microsoft.com/blog/completers-in-azure-powershell/ ).</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2123">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="5d3f2-2124">와일드카드 지원이 Az.Compute 및 Az.Network에 대한 Get cmdlet에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2124">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="5d3f2-2125">Windows PowerShell 5.1 전용 대화형 사용자 이름/암호 인증이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2125">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="5d3f2-2126">Python 2 Runbook 지원이 Az.Automation에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2126">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="5d3f2-2127">Az.LogicApp: 통합 계정 어셈블리 및 일괄 처리 구성을 위한 새로운 cmdlet입니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2127">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="5d3f2-2128">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2128">Az.Automation</span></span>
* <span data-ttu-id="5d3f2-2129">Azure 자동화 업데이트 관리에서 변경된 지원 기능은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2129">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="5d3f2-2130">동적 그룹화</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2130">Dynamic grouping</span></span>
    * <span data-ttu-id="5d3f2-2131">사전 스크립트</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2131">Pre-Post script</span></span>
    * <span data-ttu-id="5d3f2-2132">다시 부팅 설정</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2132">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="5d3f2-2133">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2133">Az.Compute</span></span>
* <span data-ttu-id="5d3f2-2134">Get-AzVmBootDiagnosticsData의 경로 확인 문제가 해결되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2134">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="5d3f2-2135">Compute 클라이언트 라이브러리가 25.0.0으로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2135">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="5d3f2-2136">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2136">Az.KeyVault</span></span>
* <span data-ttu-id="5d3f2-2137">와일드카드 지원이 KeyVault cmdlet에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2137">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="5d3f2-2138">Az.Network</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2138">Az.Network</span></span>
* <span data-ttu-id="5d3f2-2139">Azure Firewall에 대한 위협 인텔리전스 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2139">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="5d3f2-2140">Application Gateway 방화벽 정책의 최상위 수준 리소스 및 사용자 지정 규칙이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2140">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="5d3f2-2141">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2141">Az.RecoveryServices</span></span>
* <span data-ttu-id="5d3f2-2142">인스턴트 RP를 지원하기 위해 SnapshotRetentionInDays가 Azure VM 정책에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2142">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="5d3f2-2143">컨테이너 등록을 취소하는 파이프 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2143">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="5d3f2-2144">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2144">Az.Resources</span></span>
* <span data-ttu-id="5d3f2-2145">Get-AzResource 및 Get-AzResourceGroup에 대한 와일드카드 지원을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2145">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="5d3f2-2146">ARM에 대한 일반 호출을 수행할 때 사용되는 자격 증명을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2146">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="5d3f2-2147">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2147">Az.Sql</span></span>
* <span data-ttu-id="5d3f2-2148">위협 탐지의 cmdlet 매개 변수(ExcludeDetectionType)가 DetectionType에서 string[]으로 변경되어 새 DetectionType이 추가되면 이후의 증명이 되고 자동 완성도 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2148">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="5d3f2-2149">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2149">Az.Storage</span></span>
* <span data-ttu-id="5d3f2-2150">스토리지 계정에 대한 관리 정책 가져오기/설정/제거를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2150">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="5d3f2-2151">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2151">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="5d3f2-2152">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2152">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="5d3f2-2153">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2153">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="5d3f2-2154">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2154">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="5d3f2-2155">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2155">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="5d3f2-2156">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2156">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="5d3f2-2157">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2157">Az.Websites</span></span>
* <span data-ttu-id="5d3f2-2158">'New-AzWebApp -IncludeSourceWebAppSlots'를 사용하여 모든 슬롯의 복제를 중단하는 ARM 템플릿 버그가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2158">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span>

## <a name="150---march-2019"></a><span data-ttu-id="5d3f2-2159">1.5.0 - 2019년 3월</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2159">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="5d3f2-2160">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2160">Az.Accounts</span></span>
* <span data-ttu-id="5d3f2-2161">'Register-AzModule' 명령을 추가하여 AutoRest 생성 cmdlet을 지원</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2161">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="5d3f2-2162">Connect-AzAccount 예제 업데이트</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2162">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="5d3f2-2163">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2163">Az.Automation</span></span>
* <span data-ttu-id="5d3f2-2164">몇몇 Azure Automation cmdlet에서 특정 월별 일정을 검색할 때 발생하는 문제 수정</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2164">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="5d3f2-2165">상위 20개 노드를 반환하도록 Get-AzAutomationDscNode를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2165">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="5d3f2-2166">이제 모든 노드 반환</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2166">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="5d3f2-2167">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2167">Az.Cdn</span></span>
* <span data-ttu-id="5d3f2-2168">사용자 지정 도메인 Https 사용/사용 안 함에 대한 새 Powershell cmdlet이 추가되었으며 기존의 것은 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2168">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="5d3f2-2169">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2169">Az.Compute</span></span>
* <span data-ttu-id="5d3f2-2170">Get cmdlet에 와일드 카드 지원 추가</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2170">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="5d3f2-2171">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2171">Az.DataFactory</span></span>
* <span data-ttu-id="5d3f2-2172">ADF.Net SDK 버전이 3.0.1로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2172">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="5d3f2-2173">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2173">Az.LogicApp</span></span>
* <span data-ttu-id="5d3f2-2174">첫 결과 페이지 검색 시에만 ListWorkflows 수정</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2174">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="5d3f2-2175">Az.Network</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2175">Az.Network</span></span>
* <span data-ttu-id="5d3f2-2176">Network cmdlet에 와일드 카드 지원 추가</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2176">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="5d3f2-2177">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2177">Az.RecoveryServices</span></span>
* <span data-ttu-id="5d3f2-2178">Azure VM 지원에 SQL 서버가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2178">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="5d3f2-2179">SDK 업데이트</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2179">SDK Update</span></span>
* <span data-ttu-id="5d3f2-2180">VMappContainer 체크 인 Get-ProtectableItem 제거</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2180">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="5d3f2-2181">Get ProtectableItem의 매개 변수로 Name과 ServerName이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2181">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="5d3f2-2182">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2182">Az.Resources</span></span>
* <span data-ttu-id="5d3f2-2183">`-TemplateObject` 매개 변수를 추가하여 cmdlet을 배포</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2183">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="5d3f2-2184">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/2933 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2184">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="5d3f2-2185">`Get-AzResource`의 결과를 `Set-AzResource`(으)로 파이프할 때 발생하는 문제 수정</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2185">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="5d3f2-2186">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/8240 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2186">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="5d3f2-2187">실행 시 JSON 데이터 형식 문제 해결 `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2187">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="5d3f2-2188">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/7930 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2188">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="5d3f2-2189">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2189">Az.Sql</span></span>
* <span data-ttu-id="5d3f2-2190">AuditingEndpointsCommunicator를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2190">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="5d3f2-2191">새 진단 설정을 생성할 때 에지 사례의 동작을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2191">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="5d3f2-2192">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2192">Az.Storage</span></span>
* <span data-ttu-id="5d3f2-2193">스토리지 계정      - New-AzStorageAccount를 생성할 때 종류 BlockBlobStorage를 지원</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2193">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="5d3f2-2194">1.4.0 - 2019년 2월</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2194">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="5d3f2-2195">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2195">Az.AnalysisServices</span></span>
* <span data-ttu-id="5d3f2-2196">사용되지 않는 AddAzureASAccount cmdlet</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2196">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="5d3f2-2197">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2197">Az.Automation</span></span>
* <span data-ttu-id="5d3f2-2198">Import-AzAutomationDscNodeConfiguration 도움말 업데이트</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2198">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="5d3f2-2199">Import-AzAutomationDscConfiguration cmdlet 구성 이름 유효성 검사 추가</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2199">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="5d3f2-2200">Import-AzAutomationDscConfiguration cmdlet 오류 처리 개선</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2200">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="5d3f2-2201">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2201">Az.CognitiveServices</span></span>
* <span data-ttu-id="5d3f2-2202">리소스의 하위 도메인을 지정하는 데 사용되는 New-AzCognitiveServicesAccount에 대한 새 선택적 매개 변수로 CustomSubdomainName이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2202">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="5d3f2-2203">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2203">Az.Compute</span></span>
* <span data-ttu-id="5d3f2-2204">ID 매개 변수 집합 문제 해결</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2204">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="5d3f2-2205">Name 매개 변수를 제공하지 않으면 Get-AzVMExtension이 설치된 모든 확장을 열거하도록 업데이트</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2205">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="5d3f2-2206">Update-AzImage cmdlet에 태그 및 ResourceId 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2206">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="5d3f2-2207">인스턴스 ID가 없는 Get-AzVmssVM과 InstanceView를 사용하면 인스턴스 보기가 있는 VMSS VM을 나열할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2207">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="5d3f2-2208">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2208">Az.DataLakeStore</span></span>
* <span data-ttu-id="5d3f2-2209">ADL 삭제된 항목 열거 및 복원에 대한 cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2209">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="5d3f2-2210">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2210">Az.EventHub</span></span>
* <span data-ttu-id="5d3f2-2211">Eventhub의 CaptureDescription 클래스에서 빈 보관을 건너뛰는 새 부울 속성 SkipEmptyArchives가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2211">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="5d3f2-2212">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2212">Az.KeyVault</span></span>
* <span data-ttu-id="5d3f2-2213">Set-AzKeyVaultSecret 태그 지정 수정</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2213">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="5d3f2-2214">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2214">Az.LogicApp</span></span>
* <span data-ttu-id="5d3f2-2215">통합 계정에 대한 기본 sku 추가</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2215">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="5d3f2-2216">XSLT 2.0, XSLT 3.0, Liquid 맵 형식 추가</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2216">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="5d3f2-2217">통합 계정 어셈블리에 대한 새 cmdlet</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2217">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="5d3f2-2218">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2218">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="5d3f2-2219">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2219">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="5d3f2-2220">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2220">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="5d3f2-2221">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2221">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="5d3f2-2222">통합 계정 일괄 처리 구성에 대한 새 cmdlet</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2222">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="5d3f2-2223">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2223">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="5d3f2-2224">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2224">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="5d3f2-2225">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2225">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="5d3f2-2226">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2226">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="5d3f2-2227">논리 앱 SDK를 버전 4.1.0으로 업데이트</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2227">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="5d3f2-2228">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2228">Az.Monitor</span></span>
* <span data-ttu-id="5d3f2-2229">Get-AzMetric에 대한 도움말 업데이트</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2229">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="5d3f2-2230">Az.Network</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2230">Az.Network</span></span>
* <span data-ttu-id="5d3f2-2231">Add-AzApplicationGatewayCustomError에 대한 도움말 예제 업데이트</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2231">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="5d3f2-2232">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2232">Az.OperationalInsights</span></span>
* <span data-ttu-id="5d3f2-2233">New 및 Get ApplicationInsights 데이터 소스에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2233">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="5d3f2-2234">지정된 작업 영역에 대한 특정 또는 전체 ApplicationInsights 데이터 원본 가져오기를 지원하기 위한 새로운 'ApplicationInsights' 종류가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2234">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span>
    - <span data-ttu-id="5d3f2-2235">지정된 Application-Insights 리소스 매개 변수(구독 ID, resourceGroupName 및 이름)별로 데이터 원본을 만들기 위한 New-AzOperationalInsightsApplicationInsightsDataSource cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2235">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span>

#### <a name="azresources"></a><span data-ttu-id="5d3f2-2236">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2236">Az.Resources</span></span>
* <span data-ttu-id="5d3f2-2237">문제 https://github.com/Azure/azure-powershell/issues/8166 수정</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2237">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="5d3f2-2238">문제 https://github.com/Azure/azure-powershell/issues/8235 수정</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2238">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="5d3f2-2239">문제 https://github.com/Azure/azure-powershell/issues/6219 수정</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2239">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="5d3f2-2240">KeyCredentials 반복 만들기를 방지하기 위해 버그 수정</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2240">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="5d3f2-2241">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2241">Az.Sql</span></span>
* <span data-ttu-id="5d3f2-2242">SQL DB 하이퍼스케일에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2242">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="5d3f2-2243">복원 요청에서 불필요한 속성을 설정하여 복원이 실패할 수 있는 버그 수정</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2243">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="5d3f2-2244">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2244">Az.Websites</span></span>
* <span data-ttu-id="5d3f2-2245">Get-AzWebAppSlotMetrics 내 올바른 예제</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2245">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="5d3f2-2246">1.3.0 - 2019년 2월</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2246">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="5d3f2-2247">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2247">Az.Accounts</span></span>
* <span data-ttu-id="5d3f2-2248">ClientRuntime 최신 버전 업데이트</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2248">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="5d3f2-2249">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2249">Az.AnalysisServices</span></span>
<span data-ttu-id="5d3f2-2250">Az.AnalysisServices 모듈의 전반적인 가용성.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2250">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="5d3f2-2251">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2251">Az.Compute</span></span>
* <span data-ttu-id="5d3f2-2252">AEM 확장: UltraSSD 및 P60, P70, P80 디스크에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2252">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="5d3f2-2253">Set-AzVMBootDiagnostics에 대한 도움말 업데이트</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2253">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="5d3f2-2254">Update-AzImage에 대한 도움말 및 예제 업데이트</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2254">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="5d3f2-2255">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2255">Az.RecoveryServices</span></span>
<span data-ttu-id="5d3f2-2256">Az.RecoveryServices 모듈의 전반적인 가용성.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2256">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="5d3f2-2257">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2257">Az.Resources</span></span>
* <span data-ttu-id="5d3f2-2258">리소스 그룹 관련 태그 수정</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2258">Fix tagging for resource groups</span></span>
    - <span data-ttu-id="5d3f2-2259">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/8166 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2259">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="5d3f2-2260">`Get-AzureRmRoleAssignment`이(가) -ErrorAction을 준수하지 않는 문제 수정</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2260">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span>
    - <span data-ttu-id="5d3f2-2261">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/8235 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2261">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="5d3f2-2262">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2262">Az.Sql</span></span>
* <span data-ttu-id="5d3f2-2263">AzSqlDatabaseBackupShortTermRetentionPolicy 가져오기/설정하기 추가</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2263">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="5d3f2-2264">SQL cmdlet을 실행할 경우 Azure 계정에 로그인되어 있지 않은 것이 nullref 예외를 초래하는 문제 수정</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2264">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="5d3f2-2265">Get-AzSqlCapability의 nullref 예외 수정</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2265">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="5d3f2-2266">1.2.1 - 2019년 1월</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2266">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="5d3f2-2267">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2267">Az.Accounts</span></span>
* <span data-ttu-id="5d3f2-2268">올바른 인증 버전을 사용하여 릴리스</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2268">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="5d3f2-2269">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2269">Az.AnalysisServices</span></span>
* <span data-ttu-id="5d3f2-2270">업데이트된 인증 종속성을 사용하여 릴리스</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2270">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="5d3f2-2271">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2271">Az.RecoveryServices</span></span>
* <span data-ttu-id="5d3f2-2272">업데이트된 인증 종속성을 사용하여 릴리스</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2272">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="5d3f2-2273">1.2.0 - 2019년 1월</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2273">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="5d3f2-2274">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2274">Az.Accounts</span></span>
* <span data-ttu-id="5d3f2-2275">Windows PowerShell 5.1 전용 대화형 사용자 이름/암호 인증 추가</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2275">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="5d3f2-2276">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2276">Update incorrect online help URLs</span></span>
* <span data-ttu-id="5d3f2-2277">Uninstall-AzureRm 관련 PS Core에 경고 메시지 추가</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2277">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="5d3f2-2278">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2278">Az.Aks</span></span>
* <span data-ttu-id="5d3f2-2279">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2279">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="5d3f2-2280">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2280">Az.Automation</span></span>
* <span data-ttu-id="5d3f2-2281">Python 2 Runbook에 대한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2281">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="5d3f2-2282">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2282">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="5d3f2-2283">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2283">Az.Cdn</span></span>
* <span data-ttu-id="5d3f2-2284">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2284">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="5d3f2-2285">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2285">Az.Compute</span></span>
* <span data-ttu-id="5d3f2-2286">Invoke-AzVMReimage cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2286">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="5d3f2-2287">Set-AzVmss에 TempDisk 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2287">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="5d3f2-2288">New-AzVM 경고 메시지 수정</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2288">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="5d3f2-2289">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2289">Az.ContainerRegistry</span></span>
* <span data-ttu-id="5d3f2-2290">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2290">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="5d3f2-2291">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2291">Az.DataFactory</span></span>
* <span data-ttu-id="5d3f2-2292">ADF.Net SDK 버전이 3.0.0으로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2292">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="5d3f2-2293">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2293">Az.DataLakeStore</span></span>
* <span data-ttu-id="5d3f2-2294">MSI를 사용할 때 ADLS 엔드포인트 문제 수정</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2294">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="5d3f2-2295">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/7462 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2295">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="5d3f2-2296">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2296">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="5d3f2-2297">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2297">Az.IotHub</span></span>
* <span data-ttu-id="5d3f2-2298">Add-IotHubRoutingEndpoint cmdlet에 인코딩 형식을 추가하세요.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2298">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="5d3f2-2299">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2299">Az.KeyVault</span></span>
* <span data-ttu-id="5d3f2-2300">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2300">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="5d3f2-2301">Az.Network</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2301">Az.Network</span></span>
* <span data-ttu-id="5d3f2-2302">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2302">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="5d3f2-2303">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2303">Az.Resources</span></span>
* <span data-ttu-id="5d3f2-2304">'New-AzADAppCredential' 및 'New-AzADSpCredential' 참조 설명서의 잘못된 예제 수정</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2304">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="5d3f2-2305">리소스 그룹 배포 cmdlet 실행 전 '-TemplateFile' 매개 변수 경로가 확인되지 않는 문제 수정</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2305">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="5d3f2-2306">Az.Resources: New-AzureRmPolicyDefinition -Mode 기본값에 대한 올바른 설명서</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2306">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="5d3f2-2307">Az.Resources: 문제 https://github.com/Azure/azure-powershell/issues/7522 수정</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2307">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="5d3f2-2308">Az.Resources: 문제 https://github.com/Azure/azure-powershell/issues/5747 수정</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2308">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="5d3f2-2309">'PSResourceGroupDeployment' 개체의 서식 문제 수정</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2309">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="5d3f2-2310">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/2123 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2310">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="5d3f2-2311">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2311">Az.ServiceFabric</span></span>
* <span data-ttu-id="5d3f2-2312">인증서가 VMSS 모델에 추가되었는데도 예외가 발생할 경우 롤백합니다. 이는 버그 https://github.com/Azure/service-fabric-issues/issues/932 를 수정하기 위함입니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2312">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="5d3f2-2313">일부 오류 메시지를 수정하세요.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2313">Fix some error messages.</span></span>
* <span data-ttu-id="5d3f2-2314">Az로의 마이그레이션을 통해서는 작동하지 않는 New-AzServiceFabriCluster를 위해 기본값 ARM 템플릿을 가진 클러스터 만들기를 수정하세요.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2314">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="5d3f2-2315">확장에서 클러스터 id를 확인하여 클러스터에 해당하는 VMSS에만 추가되도록 클러스터/애플리케이션 인증서 추가를 수정하세요.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2315">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="5d3f2-2316">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2316">Az.SignalR</span></span>
* <span data-ttu-id="5d3f2-2317">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2317">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="5d3f2-2318">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2318">Az.Sql</span></span>
* <span data-ttu-id="5d3f2-2319">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2319">Update incorrect online help URLs</span></span>
* <span data-ttu-id="5d3f2-2320">가능한 값을 가진 LicenseType 매개 변수에 대한 매개 변수 설명이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2320">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="5d3f2-2321">유일하게 업데이트된 속성인데 작동하지 않는 관리되는 인스턴스 ID의 업데이트 수정</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2321">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="5d3f2-2322">관리되는 인스턴스에서의 사용자 지정 데이터 정렬에 대한 지원</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2322">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="5d3f2-2323">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2323">Az.Storage</span></span>
* <span data-ttu-id="5d3f2-2324">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2324">Update incorrect online help URLs</span></span>
* <span data-ttu-id="5d3f2-2325">Premium Storage 계정이 클래식 로깅/메트릭을 지원하지 않기 때문에, Premium Storage 계정의 클래식 로깅/메트릭을 가져올/설정할 때 상세한 오류 메시지를 제공해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2325">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="5d3f2-2326">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2326">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="5d3f2-2327">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2327">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="5d3f2-2328">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2328">Az.TrafficManager</span></span>
* <span data-ttu-id="5d3f2-2329">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2329">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="5d3f2-2330">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2330">Az.Websites</span></span>
* <span data-ttu-id="5d3f2-2331">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2331">Update incorrect online help URLs</span></span>
* <span data-ttu-id="5d3f2-2332">앱이 ASE에 호스팅되면 'New-AzWebAppSSLBinding'을 수정하여 올바른 resourcegroup+location에 인증서를 업로드합니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2332">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="5d3f2-2333">'New-AzWebAppSSLBinding'을 수정하여 SSL 인증서를 앱에 바인딩하는 데 붙는 태그를 덮어쓰지 않도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2333">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="5d3f2-2334">1.1.0 - 2019년 1월</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2334">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="5d3f2-2335">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2335">Az.Accounts</span></span>
* <span data-ttu-id="5d3f2-2336">Enable-AzureRmAlias에 'Local' 범위 추가</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2336">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="5d3f2-2337">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2337">Az.Compute</span></span>
* <span data-ttu-id="5d3f2-2338">이름이 Restart/Start/Stop/Remove/Set-AzVM과 Save-AzVMImage에 설정된 ID 매개 변수에서 선택 사항이 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2338">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="5d3f2-2339">도움말 파일의 ID에 대한 설명이 업데이트 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2339">Updated the description of ID in help files</span></span>
* <span data-ttu-id="5d3f2-2340">Az.Accounts 모듈을 사용할 때의 이전 버전과의 호환성 문제를 해결합니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2340">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="5d3f2-2341">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2341">Az.DataLakeStore</span></span>
* <span data-ttu-id="5d3f2-2342">SDK 수정을 위해 데이터 평면의 SDK 버전을 1.1.14로 업데이트하세요.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2342">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="5d3f2-2343">getfilestatus 및 liststatus에 대한 음수 acesstime 및 modificationtime 수정, 비동기 취소 토큰 수정</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2343">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="5d3f2-2344">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2344">Az.EventGrid</span></span>
* <span data-ttu-id="5d3f2-2345">2019-01-01 API 버전을 사용하도록 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2345">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="5d3f2-2346">2019-01-01 API 버전에서 새 시나리오를 지원하도록 다음 cmdlet을 업데이트</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2346">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="5d3f2-2347">New-AzureRmEventGridSubscription: 지정을 위한 새로운 선택적 매개 변수를 추가</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2347">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="5d3f2-2348">이벤트 Time-to-Live</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2348">Event Time-To-Live,</span></span>
        - <span data-ttu-id="5d3f2-2349">이벤트에 대한 최대 배달 시도</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2349">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="5d3f2-2350">배달 못한 편지의 엔드포인트입니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2350">Dead letter endpoint.</span></span>
    - <span data-ttu-id="5d3f2-2351">Update-AzureRmEventGridSubscription: 지정을 위한 새로운 선택적 매개 변수를 추가</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2351">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="5d3f2-2352">이벤트 Time-to-Live</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2352">Event Time-To-Live,</span></span>
        - <span data-ttu-id="5d3f2-2353">이벤트에 대한 최대 배달 시도</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2353">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="5d3f2-2354">배달 못한 편지의 엔드포인트입니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2354">Dead letter endpoint.</span></span>
* <span data-ttu-id="5d3f2-2355">New-AzureRmEventGridSubscription 및 Update-AzureRmEventGridSubscription cmdlet의 EndpointType 옵션에 새 열거형 값(즉, storageQueue 및 hybridConnection)을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2355">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="5d3f2-2356">이벤트 구독을 생성 또는 업데이트할 때 사용자가 직접 조치를 취해야 할 경우 경고 메시지를 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2356">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="5d3f2-2357">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2357">Az.IotHub</span></span>
* <span data-ttu-id="5d3f2-2358">최신 버전의 Azure IotHub SDK로 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2358">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="5d3f2-2359">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2359">Az.LogicApp</span></span>
* <span data-ttu-id="5d3f2-2360">지정된 이름이 없는 모든 Get-AzLogicApp 목록</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2360">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="5d3f2-2361">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2361">Az.Resources</span></span>
* <span data-ttu-id="5d3f2-2362">'Get-AzResource'에 '-ODataQuery'및 '-ResourceId' 매개 변수를 제공할 때 매개 변수 집합 문제 수정</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2362">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="5d3f2-2363">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/7875 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2363">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="5d3f2-2364">New/Set-AzPolicyDefinition에서 -Custom 매개 변수 처리 문제 수정</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2364">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="5d3f2-2365">New-AzDeployment 설명서에서 오타 수정</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2365">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="5d3f2-2366">'New-AzADUser'에 '-MailNickname'매개 변수가 필수 항목으로 지정됨</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2366">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="5d3f2-2367">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/8220 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2367">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="5d3f2-2368">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2368">Az.SignalR</span></span>
* <span data-ttu-id="5d3f2-2369">Az.Accounts 모듈을 사용할 때의 이전 버전과의 호환성 문제를 해결합니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2369">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="5d3f2-2370">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2370">Az.Sql</span></span>
* <span data-ttu-id="5d3f2-2371">Storage 관리 클라이언트 종속성을 일반적인 SDK 구현으로 변환했습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2371">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="5d3f2-2372">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2372">Az.Storage</span></span>
* <span data-ttu-id="5d3f2-2373">Sas Token, OAuth 또는 Anonymous를 사용하여 스토리지 컨텍스트의 StorageAccountName을 실제 스토리지 계정 이름으로 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2373">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="5d3f2-2374">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2374">New-AzStorageContext</span></span>
* <span data-ttu-id="5d3f2-2375">'-FullUri' 매개 변수를 사용하여 Blob 스냅샷 개체의 Sas Token을 생성하고 반환된 Uri를 스냅샷 Uri로 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2375">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="5d3f2-2376">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2376">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="5d3f2-2377">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2377">Az.Websites</span></span>
* <span data-ttu-id="5d3f2-2378">'Get-AzDeletedWebApp'의 날짜 구문 분석 버그를 수정했습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2378">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="5d3f2-2379">Az.Accounts 모듈을 사용할 때의 이전 버전과의 호환성 문제를 해결합니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2379">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="5d3f2-2380">1.0.0 - 2018년 12월</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2380">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="5d3f2-2381">일반</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2381">General</span></span>

- <span data-ttu-id="5d3f2-2382">Az 모듈 일반 공급</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2382">General Availability of Az Module</span></span>
- <span data-ttu-id="5d3f2-2383">각 모듈에 대 한 온라인 도움말</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2383">Online help for each module</span></span>
- <span data-ttu-id="5d3f2-2384">자세한 내용과 로드맵은 [Az 알림 페이지](https://aka.ms/azps-announce)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2384">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="5d3f2-2385">AzureRM에서 마이그레이션하는 것에 대한 정보는 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2385">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="5d3f2-2386">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2386">Az.Accounts</span></span>
- <span data-ttu-id="5d3f2-2387">Az.Profile에서 변경</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2387">Changed from Az.Profile</span></span>
- <span data-ttu-id="5d3f2-2388">프로필 및 컨텍스트 형식에 대한 표 형식 수정</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2388">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="5d3f2-2389">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2389">Az.ApiManagement</span></span>
- <span data-ttu-id="5d3f2-2390">#7002에 대한 수정</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2390">Fixes for #7002</span></span>
- <span data-ttu-id="5d3f2-2391">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2391">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="5d3f2-2392">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2392">Az.Batch</span></span>
- <span data-ttu-id="5d3f2-2393">`PSComputeNode`의 새로운 `NodeAgentInformation` 속성을 통해 풀의 각 VM에서 실행 중인 Azure Batch 노드 에이전트의 버전을 확인하는 기능이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2393">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="5d3f2-2394">`PSDataDisk`에 대한 `Caching` 기본 값은 이제 `None` 대신 `ReadWrite`입니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2394">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="5d3f2-2395">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2395">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="5d3f2-2396">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2396">Az.Billing</span></span>
- <span data-ttu-id="5d3f2-2397">청구, 소비 및 UsageAggregates cmdlet 결합 cmdlet에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2397">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="5d3f2-2398">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2398">Az.CognitivServices</span></span>
- <span data-ttu-id="5d3f2-2399">New-AzureRmCognitiveServicesAccount 작업에서 사용 가능한 SkuName 및 Typem에 대한 완성자 추가</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2399">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="5d3f2-2400">Get-AzCognitiveServicesAccountSkus에서 GetSkusWithAccountParamSetName 매개 변수 집합을 제거</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2400">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="5d3f2-2401">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2401">Az.ContainerInstance</span></span>
- <span data-ttu-id="5d3f2-2402">ManagedIdentity 지원이 추가됨</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2402">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="5d3f2-2403">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2403">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="5d3f2-2404">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2404">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="5d3f2-2405">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2405">Az.DataLakeStore</span></span>
- <span data-ttu-id="5d3f2-2406">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2406">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="5d3f2-2407">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2407">Az.Monitor</span></span>
- <span data-ttu-id="5d3f2-2408">Az.Monitor 이름 변경 및 기타 사소한 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2408">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="5d3f2-2409">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2409">Az.KeyVault</span></span>
- <span data-ttu-id="5d3f2-2410">출력 형식에서 사용되지 않는 'PurgeDisabled' 속성 제거</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2410">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="5d3f2-2411">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2411">Az.MachineLearning</span></span>
- <span data-ttu-id="5d3f2-2412">Az.MachineLearningCompute 모듈의 cmdlet 포함</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2412">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="5d3f2-2413">Az.Media</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2413">Az.Media</span></span>
- <span data-ttu-id="5d3f2-2414">New-AzMediaService에서 사용되지 않는 -Tags 별칭이 제거됨</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2414">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="5d3f2-2415">Az.Network</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2415">Az.Network</span></span>
<span data-ttu-id="5d3f2-2416">Application Gateway에서 RewriteRuleSets를 구성하는 것에 대한 지원이 추가됨</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2416">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="5d3f2-2417">추가된 새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2417">New cmdlets added:</span></span>
        - <span data-ttu-id="5d3f2-2418">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2418">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="5d3f2-2419">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2419">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="5d3f2-2420">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2420">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="5d3f2-2421">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2421">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="5d3f2-2422">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2422">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="5d3f2-2423">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2423">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="5d3f2-2424">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2424">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="5d3f2-2425">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2425">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="5d3f2-2426">선택적 매개 변수를 사용하도록 cmdlet이 업데이트됨 -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2426">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="5d3f2-2427">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2427">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="5d3f2-2428">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2428">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="5d3f2-2429">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2429">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="5d3f2-2430">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2430">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="5d3f2-2431">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2431">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="5d3f2-2432">New-AzureRmApplicationGatewayUrlPathMapConfig로 ID를 사용하여 Application Gateway에 KeyVault 지원을 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2432">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="5d3f2-2433">선택적 매개 변수를 사용하도록 cmdlet이 업데이트됨 -KeyVaultSecretId, -KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2433">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="5d3f2-2434">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2434">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="5d3f2-2435">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2435">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="5d3f2-2436">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2436">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="5d3f2-2437">New-AzApplicationGateway cmdlet이 선택적 매개 변수를 사용하도록 업데이트됨 -UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2437">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="5d3f2-2438">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2438">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="5d3f2-2439">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2439">Az.OperationalInsights</span></span>
- <span data-ttu-id="5d3f2-2440">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2440">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="5d3f2-2441">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2441">Az.Profile</span></span>
- <span data-ttu-id="5d3f2-2442">Az.Accounts에 모듈 이름이 변경됨</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2442">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="5d3f2-2443">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2443">Az.RecoveryServices</span></span>
- <span data-ttu-id="5d3f2-2444">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2444">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="5d3f2-2445">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2445">Az.Resources</span></span>
- <span data-ttu-id="5d3f2-2446">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2446">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="5d3f2-2447">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2447">Az.ServiceFabric</span></span>
- <span data-ttu-id="5d3f2-2448">일반 이름과 지문으로 지정 인증서 지원</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2448">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="5d3f2-2449">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2449">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="5d3f2-2450">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2450">Az.SIgnalR</span></span>
- <span data-ttu-id="5d3f2-2451">SIgnalR에 대한 PowerShell cmdlet에 대한 일반 공급</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2451">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="5d3f2-2452">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2452">Az.Sql</span></span>
- <span data-ttu-id="5d3f2-2453">위협 탐지의 cmdlet에 새로운 Data_Exfiltration 및 Unsafe_Action 검색 유형 추가</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2453">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="5d3f2-2454">Sql 감사 cmdlet에 대한 설명서 예제 업데이트</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2454">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="5d3f2-2455">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2455">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="5d3f2-2456">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2456">Az.Storage</span></span>
- <span data-ttu-id="5d3f2-2457">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2457">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="5d3f2-2458">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2458">Az.Websites</span></span>
- <span data-ttu-id="5d3f2-2459">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2459">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="5d3f2-2460">0.7.0 - 2018년 12월</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2460">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="5d3f2-2461">일반</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2461">General</span></span>

* <span data-ttu-id="5d3f2-2462">AzureRM에서 Az 전환 예정에 대한 사소한 변경</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2462">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="5d3f2-2463">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2463">Az.Compute</span></span>

* <span data-ttu-id="5d3f2-2464">`New-AzVm(ss)` cmdlet에 대한 간단한 매개 변수 집합에 UltraSSD 및 갤러리 이미지에 대한 지원을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2464">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="5d3f2-2465">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2465">Az.DataLakeStore</span></span>

* <span data-ttu-id="5d3f2-2466">ADLS 계정의 도메인의 후행 슬래시를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2466">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="5d3f2-2467">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2467">Az.FrontDoor</span></span>

* <span data-ttu-id="5d3f2-2468">일부 끊어진 링크 수정</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2468">Fixed some broken links</span></span>
    - <span data-ttu-id="5d3f2-2469">New-AzureRmFrontDoor 및 Set-AzureRmFrontDoor 아티클에서 New-AzureRmFrontDoorHealthProbeSettingObject cmdlet 아티클에 대한 링크가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2469">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="5d3f2-2470">New-AzureRmFrontDoorManagedRuleObject 아티클에서 New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet 아티클에 대한 링크가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2470">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="5d3f2-2471">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2471">Az.RecoveryServices</span></span>

* <span data-ttu-id="5d3f2-2472">Azure File Share 복원 작업에 클라이언트 측 유효성 검사가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2472">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="5d3f2-2473">afs 복원의 경우 storageAccountName 및 storageAccountResourceGroupName을 선택적으로 만들었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2473">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="5d3f2-2474">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2474">Az.Resources</span></span>

* <span data-ttu-id="5d3f2-2475">https://github.com/Azure/azure-powershell/issues/7679 에 대한 수정</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2475">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="5d3f2-2476">기본 관리자를 요청할 때 구독 범위가 제공되는 경우 Get-AzureRmRoleAssignment를 업데이트하여 구독 범위를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2476">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="5d3f2-2477">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2477">Az.Sql</span></span>

* <span data-ttu-id="5d3f2-2478">AzureRM에서 Az 전환 예정에 대한 사소한 변경</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2478">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="5d3f2-2479">DotNet 코어에서 Get-AzureRmSqlDatabaseVulnerabilityAssessment를 사용하는 문제 해결</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2479">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="5d3f2-2480">SQL 감사 cmdlet과 관련된 도움말 메시지의 설명서가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2480">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="5d3f2-2481">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2481">Az.Storage</span></span>

* <span data-ttu-id="5d3f2-2482">New-AzureRmStorageAccount에 -EnableHierarchicalNamespace 추가</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2482">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="5d3f2-2483">파일 복사 cmdlet이 -DestContext 입력이 없을 때 대상의 원본 컨텍스트를 다시 사용할 수 없는 문제 수정</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2483">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="5d3f2-2484">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2484">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="5d3f2-2485">고정적인 웹 사이트 구성 지원</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2485">Support Static Website configuration</span></span>
    - <span data-ttu-id="5d3f2-2486">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2486">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="5d3f2-2487">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2487">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="5d3f2-2488">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2488">Az.Websites</span></span>

* <span data-ttu-id="5d3f2-2489">Set-AzureRmWebApp 및 Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2489">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span>
    - <span data-ttu-id="5d3f2-2490">Windows 및 Linux 컨테이너 응용 프로그램에 탑재할 Azure Storage 경로를 지정하기 위해 새 매개 변수(-AzureStoragePath)가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2490">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="5d3f2-2491">새 cmdlet New-AzureRmWebAppAzureStoragePath의 출력을 매개 변수로 사용하여 Azure Storage 경로를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2491">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="5d3f2-2492">0.6.1 - 2018년 11월</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2492">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="5d3f2-2493">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2493">Az.ApiManagement</span></span>
* <span data-ttu-id="5d3f2-2494">형식 매핑 문제에 대한 종속성 업데이트</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2494">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="5d3f2-2495">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2495">Az.Automation</span></span>
* <span data-ttu-id="5d3f2-2496">Azure Automation cmdlet 기반 Swagger</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2496">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="5d3f2-2497">업데이트 관리 cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2497">Added Update Management cmdlets</span></span>
* <span data-ttu-id="5d3f2-2498">소스 제어 cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2498">Added Source Control cmdlets</span></span>
* <span data-ttu-id="5d3f2-2499">Remove-AzureRmAutomationHybridWorkerGroup cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2499">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="5d3f2-2500">DSC 노드 등록 명령 수정</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2500">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="5d3f2-2501">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2501">Az.Compute</span></span>
* <span data-ttu-id="5d3f2-2502">SystemAssigned ID에 대한 ID 문제 수정</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2502">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="5d3f2-2503">형식 매핑 문제에 대한 종속성 업데이트</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2503">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="5d3f2-2504">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2504">Az.ContainerInstance</span></span>
* <span data-ttu-id="5d3f2-2505">형식 매핑 문제에 대한 종속성 업데이트</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2505">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="5d3f2-2506">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2506">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="5d3f2-2507">마켓플레이스 cmdlet에 대한 예제 설명 업데이트</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2507">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="5d3f2-2508">Az.Network</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2508">Az.Network</span></span>
* <span data-ttu-id="5d3f2-2509">New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2509">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="5d3f2-2510">지원되는 AzureFirewall 네트워크 프로토콜에 ICMP 다시 추가</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2510">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="5d3f2-2511">Test-AzureRmNetworkWatcherConnectivity cmdlet을 업데이트하여 대상 ID, 주소 및 포트 유효성 검사를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2511">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span>
* <span data-ttu-id="5d3f2-2512">VirtualNetwork 맵의 메모리 사용 문제 해결</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2512">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="5d3f2-2513">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2513">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="5d3f2-2514">보호된 파일 공유에 대한 정책을 수정하는 것에 대해 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2514">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="5d3f2-2515">정책 표준 시간대를 대문자로 변환했습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2515">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="5d3f2-2516">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2516">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="5d3f2-2517">New-AzureRmRecoveryServicesAsrProtectableItem의 예제 정정</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2517">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="5d3f2-2518">형식 매핑 문제에 대한 종속성 업데이트</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2518">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="5d3f2-2519">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2519">Az.Relay</span></span>
* <span data-ttu-id="5d3f2-2520">선택적 매개 변수 -KeyValue를 New-AzureRmRelayKey cmdlet에 추가하여 사용자가 KeyValue를 제공할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2520">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="5d3f2-2521">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2521">Az.Resources</span></span>
* <span data-ttu-id="5d3f2-2522">`New-AzureRmPolicyAssignment` 및 `Set-AzureRmPolicyAssignment`의 자원 ID 관련 매개 변수에 대한 도움말 문서를 업데이트함</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2522">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="5d3f2-2523">-Metadata를 사용하는 New-AzureRmPolicyDefinition에 대한 예제 추가</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2523">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="5d3f2-2524">NetStandard의 태그 키에서 대소문자 보존을 허용하도록 수정: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2524">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="5d3f2-2525">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2525">Az.ServiceFabric</span></span>
* <span data-ttu-id="5d3f2-2526">향후 호환성이 손상되는 변경에 대한 사용 중단 메시지 추가</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2526">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="5d3f2-2527">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2527">Az.Sql</span></span>
* <span data-ttu-id="5d3f2-2528">Azure Sql Database Managed Instance 및 Azure Sql Managed Database에 CRUD 작업을 위한 새 cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2528">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="5d3f2-2529">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2529">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="5d3f2-2530">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2530">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="5d3f2-2531">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2531">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="5d3f2-2532">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2532">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="5d3f2-2533">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2533">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="5d3f2-2534">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2534">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="5d3f2-2535">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2535">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="5d3f2-2536">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2536">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="5d3f2-2537">서버 또는 데이터베이스에서 확장 감사 정책 관리를 활성화했습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2537">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="5d3f2-2538">새 매개 변수(PredicateExpression)가 감사 로그 필터링을 사용하도록 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2538">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="5d3f2-2539">Cmdlet이 레거시 클라이언트 대신 SQL 클라이언트를 사용하도록 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2539">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="5d3f2-2540">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2540">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="5d3f2-2541">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2541">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="5d3f2-2542">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2542">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="5d3f2-2543">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2543">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="5d3f2-2544">스토리지 계정 이름 매개 변수가 설정된 Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings를 사용할 때의 문제 해결</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2544">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="5d3f2-2545">0.5.0 - 2018년 11월</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2545">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="5d3f2-2546">일반</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2546">General</span></span>
* <span data-ttu-id="5d3f2-2547">많은 핵심 cmdlet에 Resource Completers를 추가하여 대화형으로 cmdlet을 호출할 때 기존 리소스 이름을 탭으로 이동할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2547">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="5d3f2-2548">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2548">Az.Profile</span></span>
* <span data-ttu-id="5d3f2-2549">ClientRuntime의 최신 버전을 사용하도록 일반적인 코드를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2549">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="5d3f2-2550">Connect-AzAccount cmdlet의 매개 변수 TenantId 이름을 Tenant로 바꾸고 TenantId의 별칭을 추가합니다</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2550">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="5d3f2-2551">Connect-AzAccount의 업데이트된 TenantId 설명</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2551">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="5d3f2-2552">테넌트 도메인을 제공할 때 실패한 로그인에 대한 오류 메시지 수정</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2552">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="5d3f2-2553">테넌트에 구독이 없는 계정의 컨텍스트 이름 충돌 문제 수정</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2553">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="5d3f2-2554">MSI를 사용할 때 DataLake 엔드포인트 문제 수정</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2554">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="5d3f2-2555">연결되지 않은 경우 'Disconnect-AzAccount'가 throw하는 문제 수정</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2555">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="5d3f2-2556">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2556">Az.CognitiveServices</span></span>
* <span data-ttu-id="5d3f2-2557">Get-AzCognitiveServicesAccountSkus 작업을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2557">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="5d3f2-2558">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2558">Az.Compute</span></span>
* <span data-ttu-id="5d3f2-2559">Add-AzVmssVMDataDisk 및 Remove-AzVmssVMDataDisk cmdlet를 추가합니다</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2559">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="5d3f2-2560">Get-AzVMImage는 AutomaticOSUpgradeProperties를 표시합니다</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2560">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="5d3f2-2561">수정된 SetAzVMChefExtension -BootstrapOptions 및 -JsonAttribute option 값이 json 형식으로 설정하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2561">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="5d3f2-2562">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2562">Az.DataLakeStore</span></span>
* <span data-ttu-id="5d3f2-2563">DataLake 패키지를 1.1.10으로 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2563">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="5d3f2-2564">기본 동시성을 다중 스레드 작업에 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2564">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="5d3f2-2565">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2565">Az.Insights</span></span>
* <span data-ttu-id="5d3f2-2566">해결된 문제 #7267(자동 크기 조정 영역)</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2566">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="5d3f2-2567">열거된 매개 변수를 제대로 설정하지 않은 새 자동 크기 조정 규칙을 만드는 데 문제가 있습니다(이를 항상 기본값으로 설정함).</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2567">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="5d3f2-2568">해결된 문제 # 7513[자세한 정보] Set-AzDiagnosticSetting은 설정을 생성하는 동안 범주를 명시적으로 지정해야 합니다</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2568">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="5d3f2-2569">이제 cmdlet은 생성 중에 사용할 범주를 명시적으로 표시할 필요가 없습니다. 즉, 문서화된대로 작동합니다</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2569">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="5d3f2-2570">Az.Network</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2570">Az.Network</span></span>
* <span data-ttu-id="5d3f2-2571">다음 cmdlet에 대해 PeeringType을 필수 매개 변수로 변경했습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2571">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="5d3f2-2572">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2572">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="5d3f2-2573">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2573">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="5d3f2-2574">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2574">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="5d3f2-2575">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2575">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="5d3f2-2576">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2576">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="5d3f2-2577">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2577">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="5d3f2-2578">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2578">Az.PolicyInsights</span></span>
* <span data-ttu-id="5d3f2-2579">추가된 정책 재구성 cmdlet</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2579">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="5d3f2-2580">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2580">Az.Resources</span></span>
* <span data-ttu-id="5d3f2-2581">https://github.com/Azure/azure-powershell/issues/7402 에 대한 수정</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2581">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="5d3f2-2582">'Get-AzResource'에 대해 '-ResourceId' 매개 변수를 사용하여 리소스 나열 허용</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2582">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="5d3f2-2583">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2583">Az.ServiceBus</span></span>
* <span data-ttu-id="5d3f2-2584">마이그레이션 상태를 알 수 있도록 PSServiceBusMigrationConfigurationAttributes에 MigrationState 읽기 전용 속성 추가.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2584">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="5d3f2-2585">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2585">Az.ServiceFabric</span></span>
* <span data-ttu-id="5d3f2-2586">Linux Vmss에 인증서 추가 수정.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2586">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="5d3f2-2587">Add-AzServiceFabricClusterCertificate 수정</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2587">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="5d3f2-2588">새 인증서(Azure/service-fabric-issues#932)에서 올바른 지문을 사용.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2588">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="5d3f2-2589">올바르게 예외 표시(Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2589">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="5d3f2-2590">Vmss CreateOrUpdate 작업을 시작하기 전에 'Update-AzServiceFabricDurability'를 수정하여 클러스터 구성 업데이트.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2590">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="5d3f2-2591">0.4.0 - 2018년 10월</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2591">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="5d3f2-2592">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2592">Az.Profile</span></span>
* <span data-ttu-id="5d3f2-2593">CloudShell에서 Get-AzSubscription을 사용하여 문제를 해결합니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2593">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="5d3f2-2594">ClientRuntime의 최신 버전을 사용하도록 일반적인 코드를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2594">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="5d3f2-2595">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2595">Az.Compute</span></span>
* <span data-ttu-id="5d3f2-2596">'New-AzVm'에 대해 간단한 매개 변수를 사용하는 경우 가속화된 네트워킹을 설정하기 위해 새 크기가 VM 크기의 허용 목록에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2596">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="5d3f2-2597">모든 cmdlet에 ResourceName 인수 완성자가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2597">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="5d3f2-2598">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2598">Az.DataLakeStore</span></span>
* <span data-ttu-id="5d3f2-2599">Virtual Network 규칙에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2599">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="5d3f2-2600">Get-AzDataLakeStoreVirtualNetworkRule: Azure Data Lake Store 가상 네트워크 규칙을 가져오거나 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2600">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="5d3f2-2601">Add-AzDataLakeStoreVirtualNetworkRule: 지정된 Data Lake Store 계정에 가상 네트워크 규칙을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2601">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="5d3f2-2602">Set-AzDataLakeStoreVirtualNetworkRule: 지정된 Data Lake Store 계정에 지정된 가상 네트워크 규칙을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2602">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="5d3f2-2603">Remove-AzDataLakeStoreVirtualNetworkRule: Azure Data Lake Store 가상 네트워크 규칙을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2603">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="5d3f2-2604">Az.Network</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2604">Az.Network</span></span>
* <span data-ttu-id="5d3f2-2605">Test-AzNetworkWatcherConnectivity cmdlet을 업데이트하고, 백 엔드에 프로토콜 값을 전달합니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2605">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="5d3f2-2606">모든 cmdlet에 ResourceName 인수 완성자가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2606">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="5d3f2-2607">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2607">Az.Resources</span></span>
* <span data-ttu-id="5d3f2-2608">(기본 프로필에 구독이 없고 범위가 지정되지 않은 경우) 시나리오에서 의미 있는 예외를 추가하여 Get-AzRoleDefinition이 인식할 수 없는 예외를 throw하는 문제를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2608">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="5d3f2-2609">또한 기본 매개 변수 집합을 'RoleDefinitionNameParameterSet'으로 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2609">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="5d3f2-2610">0.3.0 - 2018년 10월</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2610">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="5d3f2-2611">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2611">Azure.Storage</span></span>
* <span data-ttu-id="5d3f2-2612">대상에 메타데이터가 있을 때 Blob/파일이 메타 데이터를 복사하지 않는 문제 수정</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2612">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="5d3f2-2613">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2613">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="5d3f2-2614">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2614">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="5d3f2-2615">특정 위치의 스토리지 리소스 사용을 지원하고 글로벌 스토리지 리소스 사용 가져오기는 더 이상 사용되지 않는다는 경고 메시지를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2615">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="5d3f2-2616">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2616">Get-AzStorageUsage</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="5d3f2-2617">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2617">Az.CognitiveServices</span></span>
* <span data-ttu-id="5d3f2-2618">기존 계정이 없는 Get-AzCognitiveServicesAccountSkus를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2618">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="5d3f2-2619">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2619">Az.Compute</span></span>
* <span data-ttu-id="5d3f2-2620">Get-AzVM -ResourceGroupName <rg>가 필요한 경우 50개가 넘는 결과를 반환하도록 수정</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2620">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="5d3f2-2621">'SimpleParameterSet' 예제가 New-AzVmss cmdlet 도움말에 추가됨</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2621">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="5d3f2-2622">Azure Disk Encryption 진행률 메시지의 오타를 수정</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2622">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="5d3f2-2623">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2623">Az.DataFactoryV2</span></span>
* <span data-ttu-id="5d3f2-2624">ADF.Net SDK 버전을 2.3.0으로 업데이트</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2624">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="5d3f2-2625">Az.Network</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2625">Az.Network</span></span>
* <span data-ttu-id="5d3f2-2626">NetworkProfile 기능 추가</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2626">Added NetworkProfile functionality.</span></span> <span data-ttu-id="5d3f2-2627">추가된 새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2627">new cmdlets added</span></span>
    - <span data-ttu-id="5d3f2-2628">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2628">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="5d3f2-2629">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2629">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="5d3f2-2630">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2630">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="5d3f2-2631">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2631">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="5d3f2-2632">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2632">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="5d3f2-2633">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2633">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="5d3f2-2634">서브넷 모델에 서비스 연결 링크 추가</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2634">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="5d3f2-2635">New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2635">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="5d3f2-2636">Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2636">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="5d3f2-2637">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2637">Az.RedisCache</span></span>
* <span data-ttu-id="5d3f2-2638">모든 문자열을 Size 매개 변수로 진행되도록 허용</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2638">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="5d3f2-2639">PSArgumentCompleter 팝업에 P5 추가</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2639">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="5d3f2-2640">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2640">Az.Resources</span></span>
* <span data-ttu-id="5d3f2-2641">-Mode 매개 변수를 Set-AzPolicyDefinition에 추가</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2641">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="5d3f2-2642">사용자가 포함된 Origin 작업에서 Get-AzProviderOperation commandlet 버그 수정</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2642">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="5d3f2-2643">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2643">Az.Sql</span></span>
* <span data-ttu-id="5d3f2-2644">일부 백업 cmdlet이 현재 azure 구독을 인식하지 않는 문제 해결</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2644">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="5d3f2-2645">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2645">Az.Websites</span></span>
* <span data-ttu-id="5d3f2-2646">새 cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - 컨테이너 지속적인 배포 Webhook URL을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2646">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="5d3f2-2647">새 cmdlet New-AzWebAppContainerPSSession 및 Enter-WebAppContainerPSSession -  windows 컨테이너 앱에 PowerShell 원격 세션을 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2647">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="5d3f2-2648">0.2.0 - 2018년 9월</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2648">0.2.0 - September 2018</span></span>
 <span data-ttu-id="5d3f2-2649">초기 릴리스</span><span class="sxs-lookup"><span data-stu-id="5d3f2-2649">Initial Release</span></span>
