---
title: Azure PowerShell 릴리스 정보
description: Azure PowerShell 모듈의 모든 최신 업데이트에 대해 알아봅니다.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/10/2020
ms.openlocfilehash: a9c5394a5fac8a8a3de96925b3563776783ea9fe
ms.sourcegitcommit: d661f38bec34e65bf73913db59028e11fd78b131
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/05/2020
ms.locfileid: "82080201"
---
# <a name="azure-powershell-release-notes"></a><span data-ttu-id="852cd-103">Azure PowerShell 릴리스 정보</span><span class="sxs-lookup"><span data-stu-id="852cd-103">Azure PowerShell release notes</span></span>

## <a name="380---april-2020"></a><span data-ttu-id="852cd-104">3.8.0 - 2020년 4월</span><span class="sxs-lookup"><span data-stu-id="852cd-104">3.8.0 - April 2020</span></span>
### <a name="highlights-since-the-last-release"></a><span data-ttu-id="852cd-105">마지막 릴리스 이후의 주요 사항</span><span class="sxs-lookup"><span data-stu-id="852cd-105">Highlights since the last release</span></span>
* <span data-ttu-id="852cd-106">Az.Storage에서 지원하는 PowerShell 버전: Windows PowerShell 5.1, PowerShell Core 6.2.4 이상, PowerShell 7</span><span class="sxs-lookup"><span data-stu-id="852cd-106">PowerShell versions that Az.Storage supports: Windows PowerShell 5.1, PowerShell Core 6.2.4+, PowerShell 7</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="852cd-107">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="852cd-107">Az.Accounts</span></span>
* <span data-ttu-id="852cd-108">'Resolve-AzError'에서 Azure PowerShell 설문 조사 URL이 업데이트되었습니다. [#11507]</span><span class="sxs-lookup"><span data-stu-id="852cd-108">Updated Azure PowerShell survey URL in 'Resolve-AzError' [#11507]</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="852cd-109">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="852cd-109">Az.ApiManagement</span></span>
* <span data-ttu-id="852cd-110">향후 릴리스의 Azure File cmdlet 출력 변경에 대한 호환성이 손상되는 변경 공지가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-110">Added breaking change notice for Azure File cmdlets output change in a future release</span></span>
* <span data-ttu-id="852cd-111">'Set-AzApiManagementGroup' - GroupId 매개 변수를 지정하도록 설명서가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-111">'Set-AzApiManagementGroup' Updated documentation to specify the GroupId parameter</span></span>

#### <a name="azcdn"></a><span data-ttu-id="852cd-112">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="852cd-112">Az.Cdn</span></span>
* <span data-ttu-id="852cd-113">ChinaCDN 관련 가격 책정 SKU 표시가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-113">Fixed ChinaCDN related pricing SKU display</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="852cd-114">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="852cd-114">Az.CognitiveServices</span></span>
* <span data-ttu-id="852cd-115">Identity, Encryption, UserOwnedStorage가 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-115">Supported Identity, Encryption, UserOwnedStorage</span></span>

#### <a name="azcompute"></a><span data-ttu-id="852cd-116">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="852cd-116">Az.Compute</span></span>
* <span data-ttu-id="852cd-117">'Set-AzVmssOrchestrationServiceState' cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-117">Added 'Set-AzVmssOrchestrationServiceState' cmdlet.</span></span>
* <span data-ttu-id="852cd-118">-InstanceView가 있는 'Get-AzVmss'는 OrchestrationService 상태를 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-118">'Get-AzVmss' with -InstanceView shows OrchestrationService states.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="852cd-119">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="852cd-119">Az.IotHub</span></span>
* <span data-ttu-id="852cd-120">IoT 디바이스 쌍 구성을 관리합니다. 새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-120">Manage IoT device twin configuration, New cmdlets are:</span></span>
    - <span data-ttu-id="852cd-121">'Get-AzIotHubDeviceTwin'</span><span class="sxs-lookup"><span data-stu-id="852cd-121">'Get-AzIotHubDeviceTwin'</span></span>
    - <span data-ttu-id="852cd-122">'Update-AzIotHubDeviceTwin'</span><span class="sxs-lookup"><span data-stu-id="852cd-122">'Update-AzIotHubDeviceTwin'</span></span>
* <span data-ttu-id="852cd-123">IoT Hub에서 디바이스에 대한 직접 메서드를 호출하는 cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-123">Added cmdlet to invoke direct method on a device in an Iot Hub.</span></span>
* <span data-ttu-id="852cd-124">IoT 디바이스 모듈 쌍 구성을 관리합니다. 새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-124">Manage IoT device module twin configuration, New cmdlets are:</span></span>
    - <span data-ttu-id="852cd-125">'Get-AzIotHubModuleTwin'</span><span class="sxs-lookup"><span data-stu-id="852cd-125">'Get-AzIotHubModuleTwin'</span></span>
    - <span data-ttu-id="852cd-126">'Update-AzIotHubModuleTwin'</span><span class="sxs-lookup"><span data-stu-id="852cd-126">'Update-AzIotHubModuleTwin'</span></span>
* <span data-ttu-id="852cd-127">IoT 자동 디바이스 관리 구성을 대규모로 관리합니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-127">Manage IoT automatic device management configuration at scale.</span></span> <span data-ttu-id="852cd-128">새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-128">New cmdlets are:</span></span>
    - <span data-ttu-id="852cd-129">'Add-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="852cd-129">'Add-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="852cd-130">'Get-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="852cd-130">'Get-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="852cd-131">'Remove-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="852cd-131">'Remove-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="852cd-132">'Set-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="852cd-132">'Set-AzIotHubConfiguration'</span></span>
* <span data-ttu-id="852cd-133">Iot Hub에서 에지 모듈 메서드를 호출하는 cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-133">Added cmdlet to invoke an edge module method in an Iot Hub.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="852cd-134">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="852cd-134">Az.KeyVault</span></span>
* <span data-ttu-id="852cd-135">자격 증명 모음에서 일시 삭제 및 제거 보호를 사용하도록 설정할 수 있는 새 cmdlet 'Update-AzKeyVault'가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-135">Added a new cmdlet 'Update-AzKeyVault' that can enable soft delete and purge protection on a vault</span></span>
* <span data-ttu-id="852cd-136">Microsoft.PowerShell.SecretManagement에 대한 지원이 추가되었습니다. [#11178]</span><span class="sxs-lookup"><span data-stu-id="852cd-136">Added support to Microsoft.PowerShell.SecretManagement [#11178]</span></span>
* <span data-ttu-id="852cd-137">'Remove-AzKeyVaultManagedStorageSasDefinition' 예제의 오류가 해결되었습니다. [#11479]</span><span class="sxs-lookup"><span data-stu-id="852cd-137">Fixed error in the examples of 'Remove-AzKeyVaultManagedStorageSasDefinition' [#11479]</span></span>
* <span data-ttu-id="852cd-138">프라이빗 엔드포인트에 대한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-138">Added support to private endpoint</span></span>

#### <a name="azmaintenance"></a><span data-ttu-id="852cd-139">Az.Maintenance</span><span class="sxs-lookup"><span data-stu-id="852cd-139">Az.Maintenance</span></span>
* <span data-ttu-id="852cd-140">GA용 유지 관리 cmdlet의 릴리스 버전 게시</span><span class="sxs-lookup"><span data-stu-id="852cd-140">Publishing release version of Maintenance cmdlets for GA</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="852cd-141">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="852cd-141">Az.Monitor</span></span>
* <span data-ttu-id="852cd-142">프라이빗 링크 범위용 cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-142">Added cmdlets for private link scope</span></span>
    - <span data-ttu-id="852cd-143">'Get-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="852cd-143">'Get-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="852cd-144">'Remove-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="852cd-144">'Remove-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="852cd-145">'New-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="852cd-145">'New-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="852cd-146">'Update-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="852cd-146">'Update-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="852cd-147">'Get-AzInsightsPrivateLinkScopedResource'</span><span class="sxs-lookup"><span data-stu-id="852cd-147">'Get-AzInsightsPrivateLinkScopedResource'</span></span>
    - <span data-ttu-id="852cd-148">'New-AzInsightsPrivateLinkScopedResource'</span><span class="sxs-lookup"><span data-stu-id="852cd-148">'New-AzInsightsPrivateLinkScopedResource'</span></span>
    - <span data-ttu-id="852cd-149">'Remove-AzInsightsPrivateLinkScopedResource'</span><span class="sxs-lookup"><span data-stu-id="852cd-149">'Remove-AzInsightsPrivateLinkScopedResource'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="852cd-150">Az.Network</span><span class="sxs-lookup"><span data-stu-id="852cd-150">Az.Network</span></span>
* <span data-ttu-id="852cd-151">Virtual Network 게이트웨이의 개인 IP에 대한 연결을 사용하도록 설정하는 cmdlet이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-151">Updated cmdlets to enable connection on private IP for Virtual Network Gateway.</span></span>
    - <span data-ttu-id="852cd-152">'New-AzVirtualNetworkGateway'</span><span class="sxs-lookup"><span data-stu-id="852cd-152">'New-AzVirtualNetworkGateway'</span></span>
    - <span data-ttu-id="852cd-153">'Set-AzVirtualNetworkGateway'</span><span class="sxs-lookup"><span data-stu-id="852cd-153">'Set-AzVirtualNetworkGateway'</span></span>
    - <span data-ttu-id="852cd-154">'New-AzVirtualNetworkGatewayConnection'</span><span class="sxs-lookup"><span data-stu-id="852cd-154">'New-AzVirtualNetworkGatewayConnection'</span></span>
    - <span data-ttu-id="852cd-155">'Set-AzVirtualNetworkGatewayConnection'</span><span class="sxs-lookup"><span data-stu-id="852cd-155">'Set-AzVirtualNetworkGatewayConnection'</span></span>
* <span data-ttu-id="852cd-156">FQDN 기반 LocalNetworkGateways 및 VpnSites를 사용하도록 설정하는 cmdlet이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-156">Updated cmdlets to enable FQDN based LocalNetworkGateways and VpnSites</span></span>
    - <span data-ttu-id="852cd-157">'New-AzLocalNetworkGateway'</span><span class="sxs-lookup"><span data-stu-id="852cd-157">'New-AzLocalNetworkGateway'</span></span>
    - <span data-ttu-id="852cd-158">'New-AzVpnSiteLink'</span><span class="sxs-lookup"><span data-stu-id="852cd-158">'New-AzVpnSiteLink'</span></span>
* <span data-ttu-id="852cd-159">ExpressRouteCircuitConnectionConfig(Global Reach)의 IPv6 주소 패밀리에 대한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-159">Added support for IPv6 address family in ExpressRouteCircuitConnectionConfig (Global Reach)</span></span>
    - <span data-ttu-id="852cd-160">'Set-AzExpressRouteCircuitConnectionConfig'가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-160">Added 'Set-AzExpressRouteCircuitConnectionConfig'</span></span>
        - <span data-ttu-id="852cd-161">IPv6CircuitConnectionProperties를 포함한 모든 기존 속성을 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-161">allows setting of all the existing properties including the IPv6CircuitConnectionProperties</span></span>
    - <span data-ttu-id="852cd-162">'Add-AzExpressRouteCircuitConnectionConfig'가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-162">Updated 'Add-AzExpressRouteCircuitConnectionConfig'</span></span>
        - <span data-ttu-id="852cd-163">주소 접두사의 주소 패밀리를 지정하는 또 다른 선택적 매개 변수 AddressPrefixType이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-163">Added another optional parameter AddressPrefixType to specify the address family of address prefix</span></span>
* <span data-ttu-id="852cd-164">Virtual Network 게이트웨이 연결에서 DPD 시간 제한 설정을 사용하도록 cmdlet이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-164">Updated cmdlets to enable setting of DPD Timeout on Virtual Network Gateway Connections.</span></span>
    - <span data-ttu-id="852cd-165">New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="852cd-165">New-AzVirtualNetworkGatewayConnection</span></span>
    - <span data-ttu-id="852cd-166">Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="852cd-166">Set-AzVirtualNetworkGatewayConnection</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="852cd-167">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="852cd-167">Az.PolicyInsights</span></span>
* <span data-ttu-id="852cd-168">정책 준수 검사를 트리거하기 위한 'Start-AzPolicyComplianceScan' cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-168">Added 'Start-AzPolicyComplianceScan' cmdlet for triggering policy compliance scans</span></span>
* <span data-ttu-id="852cd-169">'Get-AzPolicyState' 출력에 정책 정의, 집합 정의 및 할당 버전이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-169">Added policy definition, set definition, and assignment versions to 'Get-AzPolicyState' output</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="852cd-170">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="852cd-170">Az.ServiceFabric</span></span>
* <span data-ttu-id="852cd-171">'New-AzServiceFabricCluster' 예제의 코드 서식 및 사용 편의성이 개선되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-171">Improved code formatting and usability of 'New-AzServiceFabricCluster' examples</span></span>

#### <a name="azsql"></a><span data-ttu-id="852cd-172">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="852cd-172">Az.Sql</span></span>
* <span data-ttu-id="852cd-173">'Get-AzSqlInstanceOperation' 및 'Stop-AzSqlInstanceOperation' cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-173">Added cmdlets 'Get-AzSqlInstanceOperation' and 'Stop-AzSqlInstanceOperation'</span></span>
* <span data-ttu-id="852cd-174">VNet에서 스토리지 계정에 대한 감사가 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-174">Supported auditing to a storage account in VNet.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="852cd-175">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="852cd-175">Az.Storage</span></span>
* <span data-ttu-id="852cd-176">향후 릴리스의 Azure File cmdlet 출력 변경에 대한 호환성이 손상되는 변경 공지가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-176">Added breaking change notice for Azure File cmdlets output change in a future release</span></span>
* <span data-ttu-id="852cd-177">스토리지 계정 생성/업데이트 시 새로운 SkuName StandardGZRS, StandardRAGZRS가 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-177">Supported new SkuName StandardGZRS, StandardRAGZRS when create/update Storage account</span></span>
    - <span data-ttu-id="852cd-178">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="852cd-178">'New-AzStorageAccount'</span></span>
    - <span data-ttu-id="852cd-179">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="852cd-179">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="852cd-180">DataLake Gen2가 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-180">Supported DataLake Gen2</span></span>
    - <span data-ttu-id="852cd-181">'New-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="852cd-181">'New-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="852cd-182">'Get-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="852cd-182">'Get-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="852cd-183">'Get-AzDataLakeGen2ChildItem'</span><span class="sxs-lookup"><span data-stu-id="852cd-183">'Get-AzDataLakeGen2ChildItem'</span></span>
    - <span data-ttu-id="852cd-184">'Move-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="852cd-184">'Move-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="852cd-185">'Set-AzDataLakeGen2ItemAclObject'</span><span class="sxs-lookup"><span data-stu-id="852cd-185">'Set-AzDataLakeGen2ItemAclObject'</span></span>
    - <span data-ttu-id="852cd-186">'Update-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="852cd-186">'Update-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="852cd-187">'Get-AzDataLakeGen2ItemContent'</span><span class="sxs-lookup"><span data-stu-id="852cd-187">'Get-AzDataLakeGen2ItemContent'</span></span>
    - <span data-ttu-id="852cd-188">'Remove-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="852cd-188">'Remove-AzDataLakeGen2Item'</span></span>

## <a name="0100-preview---april-2020"></a><span data-ttu-id="852cd-189">0.10.0-preview - 2020년 4월</span><span class="sxs-lookup"><span data-stu-id="852cd-189">0.10.0-preview - April 2020</span></span>
### <a name="general"></a><span data-ttu-id="852cd-190">일반</span><span class="sxs-lookup"><span data-stu-id="852cd-190">General</span></span>
* <span data-ttu-id="852cd-191">이제 Az 모듈이 Azure Stack Hub에서 미리 보기로 제공됩니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-191">Az modules is now available in preview on Azure Stack Hub.</span></span> <span data-ttu-id="852cd-192">따라서 Linux 및 macOS와의 플랫폼 간 호환성이 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-192">This allows for cross-platform compatibility with Linux and macOs.</span></span> <span data-ttu-id="852cd-193">Azure Stack Hub는 이제 Az 모듈을 사용하여 PowerShell Core를 지원합니다. 자세한 내용은 [여기](https://aka.ms/az4AzureStack)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="852cd-193">Azure Stack Hub now supports PowerShell core with the Az modules, more information [here](https://aka.ms/az4AzureStack)</span></span>
* <span data-ttu-id="852cd-194">Az 모듈은 2019-03-01-hybrid 프로필을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-194">Az modules support profile 2019-03-01-hybrid:</span></span>
  - <span data-ttu-id="852cd-195">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="852cd-195">Az.Billing</span></span>
  - <span data-ttu-id="852cd-196">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="852cd-196">Az.Compute</span></span>
  - <span data-ttu-id="852cd-197">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="852cd-197">Az.DataBoxEdge</span></span>
  - <span data-ttu-id="852cd-198">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="852cd-198">Az.EventHub</span></span>
  - <span data-ttu-id="852cd-199">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="852cd-199">Az.IotHub</span></span>
  - <span data-ttu-id="852cd-200">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="852cd-200">Az.KeyVault</span></span>
  - <span data-ttu-id="852cd-201">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="852cd-201">Az.Monitor</span></span>
  - <span data-ttu-id="852cd-202">Az.Network</span><span class="sxs-lookup"><span data-stu-id="852cd-202">Az.Network</span></span>
  - <span data-ttu-id="852cd-203">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="852cd-203">Az.Resources</span></span>
  - <span data-ttu-id="852cd-204">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="852cd-204">Az.Storage</span></span>
  - <span data-ttu-id="852cd-205">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="852cd-205">Az.Websites</span></span>
* <span data-ttu-id="852cd-206">Azure Stack Hub와 함께 작동하는 az용 새 PowerShell 모듈 3개(Az.Databox, Az.IotHub 및 Az.EventHub)가 도입되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-206">Three new PowerShell modules for az have been introduced that work with Azure Stack Hub, which are Az.Databox, Az.IotHub, and Az.EventHub</span></span>
* <span data-ttu-id="852cd-207">AzureRM을 Az로 변경하는 것과 같은 사소한 변경을 수행하면 명령이 비교적 동일하게 유지됩니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-207">Commands remain relatively the same, with minor changes such as changing AzureRM to Az</span></span>
* <span data-ttu-id="852cd-208">Azure Stack Hub에 대한 PowerShell 설명서의 업데이트된 링크는 [여기](https://aka.ms/InstallASHPowerShell)에서 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-208">Updated link to PowerShell documentation for Azure Stack Hub can be found [here](https://aka.ms/InstallASHPowerShell)</span></span>

## <a name="370---march-2020"></a><span data-ttu-id="852cd-209">3.7.0 - 2020년 3월</span><span class="sxs-lookup"><span data-stu-id="852cd-209">3.7.0 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="852cd-210">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="852cd-210">Az.Accounts</span></span>
* <span data-ttu-id="852cd-211">로그인하지 않을 때 'Get-AzTenant'/'Get-AzDefault'/'Set-AzDefault'에서 NullReferenceException이 발생하는 문제가 해결되었습니다. [# 10292]</span><span class="sxs-lookup"><span data-stu-id="852cd-211">Fixed 'Get-AzTenant'/'Get-AzDefault'/'Set-AzDefault' throw NullReferenceException when not login [#10292]</span></span>

#### <a name="azcompute"></a><span data-ttu-id="852cd-212">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="852cd-212">Az.Compute</span></span>
* <span data-ttu-id="852cd-213">'New-AzDiskConfig' cmdlet에 다음 매개 변수를 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-213">Added the following parameters to 'New-AzDiskConfig' cmdlet:</span></span>
    - <span data-ttu-id="852cd-214">DiskIOPSReadOnly, DiskMBpsReadOnly, MaxSharesCount, GalleryImageReference</span><span class="sxs-lookup"><span data-stu-id="852cd-214">DiskIOPSReadOnly, DiskMBpsReadOnly, MaxSharesCount, GalleryImageReference</span></span>
* <span data-ttu-id="852cd-215">암호화 속성이 'New-AzGalleryImageVersion'cmdlet의 대상 매개 변수에 허용되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-215">Allowed Encryption property to Target parameter of 'New-AzGalleryImageVersion' cmdlet.</span></span>
* <span data-ttu-id="852cd-216">'Set-AzVmss'-Reimage 및 'Invoke-AzVMReimage'cmdlet에 대한 tempDisk 이슈가 해결되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-216">Fixed tempDisk issue for 'Set-AzVmss' -Reimage and 'Invoke-AzVMReimage' cmdlets.</span></span> <span data-ttu-id="852cd-217">[#11354]</span><span class="sxs-lookup"><span data-stu-id="852cd-217">[#11354]</span></span>
* <span data-ttu-id="852cd-218">새로운 SAP 확장을 위해 아래 cmdlet에 대한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-218">Added support to below cmdlets for new SAP Extension</span></span>
    - <span data-ttu-id="852cd-219">'Set-AzVMAEMExtension'</span><span class="sxs-lookup"><span data-stu-id="852cd-219">'Set-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="852cd-220">'Get-AzVMAEMExtension'</span><span class="sxs-lookup"><span data-stu-id="852cd-220">'Get-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="852cd-221">'Remove-AzVMAEMExtension'</span><span class="sxs-lookup"><span data-stu-id="852cd-221">'Remove-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="852cd-222">'Update-AzVMAEMExtension'</span><span class="sxs-lookup"><span data-stu-id="852cd-222">'Update-AzVMAEMExtension'</span></span>
* <span data-ttu-id="852cd-223">도움말 문서의 예제에서 오류가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-223">Fixed errors in examples of help document</span></span>
* <span data-ttu-id="852cd-224">VM PowerState의 정확한 문자열 값을 테이블 형식으로 표시했습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-224">Showed the exact string value for VM PowerState in the table format.</span></span>
* <span data-ttu-id="852cd-225">'New-AzVmssConfig': SinglePlacementGroup이 비활성화된 경우 AutomaticRepairs 속성의 직렬화가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-225">'New-AzVmssConfig': fixed serialization of AutomaticRepairs property when SinglePlacementGroup is disabled.</span></span> <span data-ttu-id="852cd-226">[#11257]</span><span class="sxs-lookup"><span data-stu-id="852cd-226">[#11257]</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="852cd-227">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="852cd-227">Az.DataFactory</span></span>
* <span data-ttu-id="852cd-228">ADF .Net SDK 버전이 4.8.0으로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-228">Updated ADF .Net SDK version to 4.8.0</span></span>
* <span data-ttu-id="852cd-229">재실행을 지원하기 위해 'Invoke-AzDataFactoryV2Pipeline' 명령에 선택적 매개 변수를 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-229">Added optional parameters to 'Invoke-AzDataFactoryV2Pipeline' command to support rerun</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="852cd-230">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="852cd-230">Az.DataLakeStore</span></span>
* <span data-ttu-id="852cd-231">'Export-AzDataLakeStoreItem' 및 'Import-AzDataLakeStoreItem'에 대해 호환성이 손상되는 변경 설명을 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-231">Added breaking change description for 'Export-AzDataLakeStoreItem' and 'Import-AzDataLakeStoreItem'</span></span>
* <span data-ttu-id="852cd-232">'New-AzDataLakeStoreItem', 'Add-AzDAtaLakeStoreItemContent' 및 'Get-AzDAtaLakeStoreItemContent'에 대한 바이트 인코딩 옵션이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-232">Added option of Byte encoding for 'New-AzDataLakeStoreItem', 'Add-AzDAtaLakeStoreItemContent', and 'Get-AzDAtaLakeStoreItemContent'</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="852cd-233">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="852cd-233">Az.HDInsight</span></span>
* <span data-ttu-id="852cd-234">클러스터 생성 시 최소 지원 TLS 버전 지정이 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-234">Supported specifying minimal supported TLS version when creating cluster.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="852cd-235">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="852cd-235">Az.IotHub</span></span>
* <span data-ttu-id="852cd-236">디바이스별 분산 설정을 관리하기 위한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-236">Added support to manage distributed settings per-device.</span></span> <span data-ttu-id="852cd-237">새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-237">New Cmdlets are:</span></span>
    - <span data-ttu-id="852cd-238">'Get-AzIotHubDistributedTracing'</span><span class="sxs-lookup"><span data-stu-id="852cd-238">'Get-AzIotHubDistributedTracing'</span></span>
    - <span data-ttu-id="852cd-239">'Set-AzIotHubDistributedTracing'</span><span class="sxs-lookup"><span data-stu-id="852cd-239">'Set-AzIotHubDistributedTracing'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="852cd-240">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="852cd-240">Az.KeyVault</span></span>
* <span data-ttu-id="852cd-241">'New-AzKeyVault'에 대해 호환성이 손상되는 변경 속성이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-241">Added breaking change attributes to 'New-AzKeyVault'</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="852cd-242">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="852cd-242">Az.Monitor</span></span>
* <span data-ttu-id="852cd-243">'New-AzScheduledQueryRuleLogMetricTrigger'에 대한 설명서가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-243">Updated documentation for 'New-AzScheduledQueryRuleLogMetricTrigger'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="852cd-244">Az.Network</span><span class="sxs-lookup"><span data-stu-id="852cd-244">Az.Network</span></span>
* <span data-ttu-id="852cd-245">교차 테넌트 VirtualHubVnetConnections를 허용하도록 cmdlet이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-245">Updated cmdlets to allow cross-tenant VirtualHubVnetConnections</span></span>
    - <span data-ttu-id="852cd-246">'New-AzVirtualHubVnetConnection'</span><span class="sxs-lookup"><span data-stu-id="852cd-246">'New-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="852cd-247">'Update-AzVirtualHubVnetConnection'</span><span class="sxs-lookup"><span data-stu-id="852cd-247">'Update-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="852cd-248">'New-AzVirtualHub'</span><span class="sxs-lookup"><span data-stu-id="852cd-248">'New-AzVirtualHub'</span></span>
    - <span data-ttu-id="852cd-249">'Update-AzVirtualHub'</span><span class="sxs-lookup"><span data-stu-id="852cd-249">'Update-AzVirtualHub'</span></span>
* <span data-ttu-id="852cd-250">SQL Management SDK 종속성이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-250">Removed Sql Management SDK dependency</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="852cd-251">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="852cd-251">Az.PolicyInsights</span></span>
* <span data-ttu-id="852cd-252">오류 메시지가 향상되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-252">Improved error messages</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="852cd-253">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="852cd-253">Az.RecoveryServices</span></span>
* <span data-ttu-id="852cd-254">Azure Site Recovery는 Azure 디스크 암호화 Virtual Machines에 대한 VM 속성을 다시 보호하고 업데이트하는 기능을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-254">Azure Site Recovery added support for doing reprotect and updated vm properties for Azure disk encrypted Virtual Machines.</span></span>
* <span data-ttu-id="852cd-255">Azure Site Recovery VmwareToAzure 속성 DR 모니터링이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-255">Added Azure Site Recovery VmwareToAzure properties DR monitoring</span></span>
* <span data-ttu-id="852cd-256">Azure Backup은 실패한 항목에 대한 정책 업데이트 재시도 지원을 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-256">Azure Backup added support for retrying policy update for failed items.</span></span>
* <span data-ttu-id="852cd-257">Azure Backup은 백업 및 복원 중에 디스크 제외 설정에 대한 지원을 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-257">Azure Backup Added support for disk exclusion settings during backup and restore.</span></span>
* <span data-ttu-id="852cd-258">Azure Backup은 AzureFileShare에서 여러 파일/폴더 복원을 위한 지원을 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-258">Azure Backup Added Support for Restoring Multiple files/folders in AzureFileShare</span></span>
* <span data-ttu-id="852cd-259">Azure Backup은 IaasVM 정책을 업데이트하는 동안 사용자 지정 리소스 그룹 지원에 대한 지원을 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-259">Azure Backup Added support for User-specified Resourcegroup support while updating IaasVM Policy</span></span>

#### <a name="azresources"></a><span data-ttu-id="852cd-260">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="852cd-260">Az.Resources</span></span>
* <span data-ttu-id="852cd-261">'Get-AzResource -ResourceGroupName -Name -ExpandProperties -ResourceType'이 기본 apiVersion 대신 실제 apiVersion 리소스를 사용하도록 수정했습니다. [# 11267]</span><span class="sxs-lookup"><span data-stu-id="852cd-261">Fixed 'Get-AzResource -ResourceGroupName -Name -ExpandProperties -ResourceType' to use actual apiVersion of resources instead of default apiVersion [#11267]</span></span>
* <span data-ttu-id="852cd-262">오류 시나리오에 대해 correlationId 로깅이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-262">Added correlationId logging for error scenarios</span></span>
* <span data-ttu-id="852cd-263">작은 설명서가 'Get-AzResourceLock'으로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-263">Small documentation change to 'Get-AzResourceLock'.</span></span> <span data-ttu-id="852cd-264">예제가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-264">Added example.</span></span>
* <span data-ttu-id="852cd-265">'Get-AzADUser'의 매개 변수 값에서 작은 따옴표를 이스케이프 처리하였습니다. [# 11317]</span><span class="sxs-lookup"><span data-stu-id="852cd-265">Escaped single quote in parameter value of 'Get-AzADUser' [#11317]</span></span>
* <span data-ttu-id="852cd-266">배포 스크립트('Get-AzDeploymentScript', 'Get-AzDeploymentScriptLog', 'Save-AzDeploymentScriptLog', 'Remove-AzDeploymentScript')에 대한 새로운 cmdlet 추가가 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-266">Added new cmdlets for Deployment Scripts ('Get-AzDeploymentScript', 'Get-AzDeploymentScriptLog', 'Save-AzDeploymentScriptLog', 'Remove-AzDeploymentScript')</span></span>

#### <a name="azsql"></a><span data-ttu-id="852cd-267">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="852cd-267">Az.Sql</span></span>
* <span data-ttu-id="852cd-268">'Invoke-AzSqlDatabaseFailover'에 읽기 가능한 보조 매개 변수를 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-268">Added readable secondary parameter to 'Invoke-AzSqlDatabaseFailover'</span></span>
* <span data-ttu-id="852cd-269">'Disable-AzSqlServerActiveDirectoryOnlyAuthentication' cmdlet을 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-269">Added cmdlet 'Disable-AzSqlServerActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="852cd-270">데이터베이스에서 열을 분류할 때 저장된 민감도 순위입니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-270">Saved sensitivity rank when classifying columns in the database.</span></span>

#### <a name="azsupport"></a><span data-ttu-id="852cd-271">Az.Support</span><span class="sxs-lookup"><span data-stu-id="852cd-271">Az.Support</span></span>
* <span data-ttu-id="852cd-272">'Az.Support' 모듈의 일반 공급</span><span class="sxs-lookup"><span data-stu-id="852cd-272">General availability of 'Az.Support' module</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="852cd-273">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="852cd-273">Az.Websites</span></span>
* <span data-ttu-id="852cd-274">아래의 새로운 cmdlet을 통해 webapp 트래픽 라우팅 규칙을 사용하는 작업에 대한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-274">Added support for working with webapp Traffic Routing Rules via below new cmdlets</span></span>
    - <span data-ttu-id="852cd-275">'Get-AzWebAppTrafficRouting'</span><span class="sxs-lookup"><span data-stu-id="852cd-275">'Get-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="852cd-276">'Update-AzWebAppTrafficRouting'</span><span class="sxs-lookup"><span data-stu-id="852cd-276">'Update-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="852cd-277">'Add-AzWebAppTrafficRouting'</span><span class="sxs-lookup"><span data-stu-id="852cd-277">'Add-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="852cd-278">'Remove-AzWebAppTrafficRouting'</span><span class="sxs-lookup"><span data-stu-id="852cd-278">'Remove-AzWebAppTrafficRouting'</span></span>

## <a name="361---march-2020"></a><span data-ttu-id="852cd-279">3.6.1 - 2020년 3월</span><span class="sxs-lookup"><span data-stu-id="852cd-279">3.6.1 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="852cd-280">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="852cd-280">Az.Accounts</span></span>
* <span data-ttu-id="852cd-281">'피드백 보내기'에서 Azure PowerShell 설문 조사 페이지가 열립니다[#11020].</span><span class="sxs-lookup"><span data-stu-id="852cd-281">Open Azure PowerShell survey page in 'Send-Feedback' [#11020]</span></span>
* <span data-ttu-id="852cd-282">'오류 해결'에서 Azure PowerShell 설문 조사 URL이 표시됩니다[#11021].</span><span class="sxs-lookup"><span data-stu-id="852cd-282">Display Azure PowerShell survey URL in 'Resolve-Error' [#11021]</span></span>
* <span data-ttu-id="852cd-283">UserAgent에서 Az 버전이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-283">Added Az version in UserAgent</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="852cd-284">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="852cd-284">Az.ApiManagement</span></span>
* <span data-ttu-id="852cd-285">DeveloperPortal 엔드포인트에서 사용자 지정 도메인을 검색하고 구성하기 위한 지원이 추가되었습니다[#11007].</span><span class="sxs-lookup"><span data-stu-id="852cd-285">Added support for retrieving and configuring Custom Domain on the DeveloperPortal Endpoint [#11007]</span></span>
* <span data-ttu-id="852cd-286">Json 형식의 API 정의를 다운로드하기 위한 'Export-AzApiManagementApi' 지원이 추가되었습니다[#9987].</span><span class="sxs-lookup"><span data-stu-id="852cd-286">'Export-AzApiManagementApi' Added support for downloading Api Definition in Json format [#9987]</span></span>
* <span data-ttu-id="852cd-287">Json 문서에서 OpenApi 3.0 정의를 가져오기 위한 'Import-AzApiManagementApi' 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-287">'Import-AzApiManagementApi' Added support for importing OpenApi 3.0 definition from Json document</span></span>
* <span data-ttu-id="852cd-288">AAD B2C 공급자에 대한 '로그인 테넌트'를 구성하기 위한 'New-AzApiManagementIdentityProvider' 및 'Set-AzApiManagementIdentityProvider' 지원이 추가되었습니다[#9784].</span><span class="sxs-lookup"><span data-stu-id="852cd-288">'New-AzApiManagementIdentityProvider' and 'Set-AzApiManagementIdentityProvider' Added support for configuring 'Signin Tenant' for AAD B2C Provider [#9784]</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="852cd-289">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="852cd-289">Az.DataLakeStore</span></span>
* <span data-ttu-id="852cd-290">csproj 및 psd1에서 System.Buffers에 대한 참조가 명시적으로 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-290">Added reference to System.Buffers explicitly in csproj and psd1.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="852cd-291">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="852cd-291">Az.IotHub</span></span>
* <span data-ttu-id="852cd-292">Iot Hub에서 디바이스를 관리하기 위한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-292">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="852cd-293">새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-293">New Cmdlets are:</span></span>
    - <span data-ttu-id="852cd-294">'Add-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="852cd-294">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="852cd-295">'Get-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="852cd-295">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="852cd-296">'Remove-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="852cd-296">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="852cd-297">'Set-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="852cd-297">'Set-AzIotHubDevice'</span></span>
* <span data-ttu-id="852cd-298">Iot Hub의 대상 IoT 디바이스에서 모듈을 관리하기 위한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-298">Added support to manage modules on a target Iot device in an Iot Hub.</span></span> <span data-ttu-id="852cd-299">새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-299">New Cmdlets are:</span></span>
    - <span data-ttu-id="852cd-300">'Add-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="852cd-300">'Add-AzIotHubModule'</span></span>
    - <span data-ttu-id="852cd-301">'Get-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="852cd-301">'Get-AzIotHubModule'</span></span>
    - <span data-ttu-id="852cd-302">'Remove-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="852cd-302">'Remove-AzIotHubModule'</span></span>
    - <span data-ttu-id="852cd-303">'Set-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="852cd-303">'Set-AzIotHubModule'</span></span>
* <span data-ttu-id="852cd-304">Iot Hub에서 대상 IoT 디바이스에 대한 연결 문자열을 가져오는 cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-304">Added cmdlet to get the connection string of a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="852cd-305">Iot Hub에서 대상 IoT 디바이스의 모듈에 대한 연결 문자열을 가져오는 cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-305">Added cmdlet to get the connection string of a module on a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="852cd-306">IoT 디바이스의 부모 디바이스를 가져오거나 설정하기 위한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-306">Added support to get/set parent device of an IoT device.</span></span> <span data-ttu-id="852cd-307">새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-307">New Cmdlets are:</span></span>
    - <span data-ttu-id="852cd-308">'Get-AzIotHubDeviceParent'</span><span class="sxs-lookup"><span data-stu-id="852cd-308">'Get-AzIotHubDeviceParent'</span></span>
    - <span data-ttu-id="852cd-309">'Set-AzIotHubDeviceParent'</span><span class="sxs-lookup"><span data-stu-id="852cd-309">'Set-AzIotHubDeviceParent'</span></span>
* <span data-ttu-id="852cd-310">디바이스 부모-자식 관계를 관리하기 위한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-310">Added support to manage device parent-child relationship.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="852cd-311">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="852cd-311">Az.Monitor</span></span>
* <span data-ttu-id="852cd-312">'Get-AzMetricDefinition'에 대한 출력 값이 수정되었습니다[#9714].</span><span class="sxs-lookup"><span data-stu-id="852cd-312">Fixed output value for 'Get-AzMetricDefinition' [#9714]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="852cd-313">Az.Network</span><span class="sxs-lookup"><span data-stu-id="852cd-313">Az.Network</span></span>
* <span data-ttu-id="852cd-314">SQL Management SDK가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-314">Updated Sql Management SDK.</span></span>
* <span data-ttu-id="852cd-315">PrivateLinkServiceConnectionState 클래스의 명명 차이 문제가 해결되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-315">Fixed a naming-difference issue in PrivateLinkServiceConnectionState class.</span></span>
    - <span data-ttu-id="852cd-316">ActionsRequired 필드가 ActionRequired에 매핑됩니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-316">Mapping the field ActionsRequired to ActionRequired.</span></span>
* <span data-ttu-id="852cd-317">PublicNetworkAccess가 'New-AzSqlServer' 및 'Set-AzSqlServer'에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-317">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>

#### <a name="azresources"></a><span data-ttu-id="852cd-318">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="852cd-318">Az.Resources</span></span>
* <span data-ttu-id="852cd-319">Get-AzRoleAssignment'의 null 참조 버그가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-319">Fixed for null reference bug in 'Get-AzRoleAssignment'</span></span>
* <span data-ttu-id="852cd-320">'Remove-AzADGroup'에서 '-Force' 및 '-PassThru' 스위치가 선택적으로 표시됩니다[#10849].</span><span class="sxs-lookup"><span data-stu-id="852cd-320">Marked switch '-Force' and '-PassThru' optional in 'Remove-AzADGroup' [#10849]</span></span>
* <span data-ttu-id="852cd-321">'Remove-AzADGroup'에서 'MailNickname'이 반환되지 않는 문제가 해결되었습니다[#11167].</span><span class="sxs-lookup"><span data-stu-id="852cd-321">Fixed issue that 'MailNickname' doesn't return in 'Remove-AzADGroup' [#11167]</span></span>
* <span data-ttu-id="852cd-322">'Remove-AzADGroup' 파이프 작업이 작동하지 않는 문제가 해결되었습니다[#11171].</span><span class="sxs-lookup"><span data-stu-id="852cd-322">Fixed issue that 'Remove-AzADGroup' pipe operation doesn't work [#11171]</span></span>
* <span data-ttu-id="852cd-323">GetAzureRoleAssignmentCommand의 null 참조 버그가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-323">Fixed for null reference bug in GetAzureRoleAssignmentCommand</span></span>
* <span data-ttu-id="852cd-324">예정된 정책 cmdlet 변경에 대한 호환성이 손상되는 변경 특성이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-324">Added breaking change attributes for upcoming changes to policy cmdlets</span></span>
* <span data-ttu-id="852cd-325">서버 쪽에서 리소스 그룹 태그 필터링을 수행하도록 'Get-AzResourceGroup'이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-325">Updated 'Get-AzResourceGroup' to perform resource group tag filtering on server-side</span></span>
* <span data-ttu-id="852cd-326">-ResourceId를 허용하도록 Tag cmdlet이 확장되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-326">Extended Tag cmdlets to accept -ResourceId</span></span>
    - <span data-ttu-id="852cd-327">Get-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="852cd-327">Get-AzTag -ResourceId</span></span>
    - <span data-ttu-id="852cd-328">New-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="852cd-328">New-AzTag -ResourceId</span></span>
    - <span data-ttu-id="852cd-329">Remove-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="852cd-329">Remove-AzTag -ResourceId</span></span>
* <span data-ttu-id="852cd-330">새 Tag cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-330">Added new Tag cmdlet</span></span>
    - <span data-ttu-id="852cd-331">Update-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="852cd-331">Update-AzTag -ResourceId</span></span>
* <span data-ttu-id="852cd-332">SDK 3.3.0에서 ScopedDeployment를 가져왔습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-332">Brought ScopedDeployment from SDK 3.3.0</span></span>

#### <a name="azsql"></a><span data-ttu-id="852cd-333">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="852cd-333">Az.Sql</span></span>
* <span data-ttu-id="852cd-334">PublicNetworkAccess가 'New-AzSqlServer' 및 'Set-AzSqlServer'에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-334">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>
* <span data-ttu-id="852cd-335">관리형 데이터베이스에 대한 장기 보존 백업 구성에 대한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-335">Added support for Long Term Retention backup configuration for Managed Databases</span></span>
    - <span data-ttu-id="852cd-336">관리형 데이터베이스에서 LTR 정책을 가져오거나 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-336">Get/Set LTR policy on a managed database</span></span>
    - <span data-ttu-id="852cd-337">관리형 데이터베이스, 관리형 인스턴스 또는 위치를 기준으로 LTR 백업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-337">Get LTR backup(s) by managed database, managed instance, or by location</span></span>
    - <span data-ttu-id="852cd-338">LTR 백업을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-338">Remove an LTR backup</span></span>
    - <span data-ttu-id="852cd-339">LTR 백업을 복원하여 새 관리형 데이터베이스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-339">Restore an LTR backup to create a new managed database</span></span>
* <span data-ttu-id="852cd-340">MinimalTlsVersion이 New-AzSqlServer 및 Set-AzSqlServer에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-340">Added MinimalTlsVersion to New-AzSqlServer and Set-AzSqlServer</span></span>
* <span data-ttu-id="852cd-341">MinimalTlsVersion을 New-AzSqlInstance 및 Set-AzSqlInstance에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-341">Added MinimalTlsVersion to New-AzSqlInstance and Set-AzSqlInstance</span></span>
* <span data-ttu-id="852cd-342">Az.Network에 대한 SQL SDK 버전이 높아졌습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-342">Bumped SQL SDK version for Az.Network</span></span>

#### <a name="azstorage"></a><span data-ttu-id="852cd-343">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="852cd-343">Az.Storage</span></span>
* <span data-ttu-id="852cd-344">ImmutabilityPolicy에서 AllowProtectedAppendWrite가 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-344">Supported AllowProtectedAppendWrite in ImmutabilityPolicy</span></span>
    - <span data-ttu-id="852cd-345">'Set-AzRmStorageContainerImmutabilityPolicy'</span><span class="sxs-lookup"><span data-stu-id="852cd-345">'Set-AzRmStorageContainerImmutabilityPolicy'</span></span>
* <span data-ttu-id="852cd-346">이후 릴리스에서 AzureStorageTable 형식 변경에 대한 호환성이 손상되는 변경 경고 메시지가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-346">Added breaking change warning message for AzureStorageTable type change in a future release</span></span>
    - <span data-ttu-id="852cd-347">'New-AzStorageTable'</span><span class="sxs-lookup"><span data-stu-id="852cd-347">'New-AzStorageTable'</span></span>
    - <span data-ttu-id="852cd-348">'Get-AzStorageTable'</span><span class="sxs-lookup"><span data-stu-id="852cd-348">'Get-AzStorageTable'</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="852cd-349">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="852cd-349">Az.Websites</span></span>
* <span data-ttu-id="852cd-350">'New-AzAppServicePlan' 및 'Set-AzAppServicePlan'에 대한 Tag 매개 변수가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-350">Added Tag parameter for 'New-AzAppServicePlan' and 'Set-AzAppServicePlan'</span></span>
* <span data-ttu-id="852cd-351">웹 사이트에 사용자 지정 도메인을 추가할 때 예외가 throw되면 cmdlet 실행을 중지합니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-351">Stop cmdlet execution if an exception is thrown when adding a custom domain to a website</span></span>
* <span data-ttu-id="852cd-352">App Service 계획과 동일한 리소스 그룹에 속하지 않는 App Services에 대한 작업을 수행하기 위한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-352">Added support to perform operations for App Services not in the same resource group as the App Service Plan</span></span>
* <span data-ttu-id="852cd-353">다른 리소스 그룹의 WebApp/Function에 대한 액세스 제한이 적용되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-353">Applied access restriction to WebApp/Function in different resource groups</span></span>
* <span data-ttu-id="852cd-354">WebAppSlot에 대한 사용자 지정 호스트 이름을 설정하는 문제가 해결되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-354">Fixed issue to set custom hostnames for WebAppSlots</span></span>

## <a name="350---february-2020"></a><span data-ttu-id="852cd-355">3.5.0 - 2020년 2월</span><span class="sxs-lookup"><span data-stu-id="852cd-355">3.5.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="852cd-356">마지막 주 릴리스 이후의 주요 사항</span><span class="sxs-lookup"><span data-stu-id="852cd-356">Highlights since the last major release</span></span>
* <span data-ttu-id="852cd-357">클라이언트 쪽 원격 분석이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-357">Updated client side telemetry.</span></span>
* <span data-ttu-id="852cd-358">디바이스 관리를 지원하는 cmdlet이 Az.IotHub에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-358">Az.IotHub added cmdlets to support to manage devices.</span></span>
* <span data-ttu-id="852cd-359">가용성 그룹 수신기에 대한 cmdlet이 Az.SqlVirtualMachine에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-359">Az.SqlVirtualMachine added cmdlets for Availability Group Listener.</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="852cd-360">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="852cd-360">Az.Accounts</span></span>
* <span data-ttu-id="852cd-361">SubscriptionId, TenantId 및 실행 시간이 클라이언트 쪽 원격 분석에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-361">Added SubscriptionId, TenantId, and execution time into data of client side telemetry</span></span>

#### <a name="azautomation"></a><span data-ttu-id="852cd-362">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="852cd-362">Az.Automation</span></span>
* <span data-ttu-id="852cd-363">'New-AzAutomationSoftwareUpdateConfiguration' 참조 설명서의 예제 1에 있는 오타가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-363">Fixed typo in Example 1 in reference documentation for 'New-AzAutomationSoftwareUpdateConfiguration'</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="852cd-364">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="852cd-364">Az.CognitiveServices</span></span>
* <span data-ttu-id="852cd-365">SDK가 7.0으로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-365">Updated SDK to 7.0</span></span>
* <span data-ttu-id="852cd-366">서버 응답 본문이 비어 있는 경우 표시되는 오류 메시지가 향상되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-366">Improved error message when server responses empty body</span></span>

#### <a name="azcompute"></a><span data-ttu-id="852cd-367">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="852cd-367">Az.Compute</span></span>
* <span data-ttu-id="852cd-368">업데이트하는 동안 빈 값이 ProximityPlacementGroupId에 허용되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-368">Allowed empty value for ProximityPlacementGroupId during update</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="852cd-369">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="852cd-369">Az.FrontDoor</span></span>
* <span data-ttu-id="852cd-370">WAF에서 사용할 수 있는 관리형 규칙 정의를 가져오는 cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-370">Added cmdlet to get managed rule definitions that can be used in WAF</span></span>

#### <a name="aziothub"></a><span data-ttu-id="852cd-371">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="852cd-371">Az.IotHub</span></span>
* <span data-ttu-id="852cd-372">Iot Hub에서 디바이스를 관리하기 위한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-372">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="852cd-373">새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-373">New Cmdlets are:</span></span>
    - <span data-ttu-id="852cd-374">'Add-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="852cd-374">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="852cd-375">'Get-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="852cd-375">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="852cd-376">'Remove-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="852cd-376">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="852cd-377">'Set-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="852cd-377">'Set-AzIotHubDevice'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="852cd-378">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="852cd-378">Az.KeyVault</span></span>
* <span data-ttu-id="852cd-379">Add-AzKeyVaultKey.md에 대해 중복된 텍스트가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-379">Fixed duplicated text for Add-AzKeyVaultKey.md</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="852cd-380">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="852cd-380">Az.Monitor</span></span>
* <span data-ttu-id="852cd-381">Get-AzLog cmdlet에 대한 설명이 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-381">Fixed description of the Get-AzLog cmdlet.</span></span>
* <span data-ttu-id="852cd-382">ActionGroupId라는 새 매개 변수가 'New-AzMetricAlertRuleV2' 명령에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-382">A new parameter called ActionGroupId was added to 'New-AzMetricAlertRuleV2' command.</span></span>
    - <span data-ttu-id="852cd-383">사용자는 ActionGroupId(string) 또는 ActionGorup(ActivityLogAlertActionGroup) 중 하나를 제공할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-383">The user can provide either ActionGroupId(string) or ActionGorup(ActivityLogAlertActionGroup).</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="852cd-384">Az.Network</span><span class="sxs-lookup"><span data-stu-id="852cd-384">Az.Network</span></span>
* <span data-ttu-id="852cd-385">'New-AzPrivateLinkService' cmdlet의 '-EnableProxyProtocol' 매개 변수에 대한 하나의 추가 매개 변수 메모가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-385">Added one extra parameter note for parameter '-EnableProxyProtocol' for 'New-AzPrivateLinkService' cmdlet.</span></span>
* <span data-ttu-id="852cd-386">Start-AzVirtualNetworkGatewayConnectionPacketCapture.md 및 Start-AzVirtualnetworkGatewayPacketCapture.md의 FilterData 예제가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-386">Fixed FilterData example in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="852cd-387">Start-AzVirtualNetworkGatewayConnectionPacketCapture.md 및 Start-AzVirtualnetworkGatewayPacketCapture.md의 모든 내부 및 외부 패킷을 캡처하는 패킷 캡처 예제가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-387">Added Packet Capture example for capture all inner and outer packets in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="852cd-388">VNet 방화벽에서 Azure Firewall 정책이 지원됩니다</span><span class="sxs-lookup"><span data-stu-id="852cd-388">Supported Azure Firewall Policy on VNet Firewalls</span></span>
    - <span data-ttu-id="852cd-389">새로 추가된 cmdlet이 없습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-389">No new cmdlets are added.</span></span> <span data-ttu-id="852cd-390">VNet 방화벽에서 방화벽 정책 제한이 완화되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-390">Relaxing the restriction for firewall policy on VNet firewalls</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="852cd-391">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="852cd-391">Az.RecoveryServices</span></span>
* <span data-ttu-id="852cd-392">SQL Database에 대한 파일로 복원 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-392">Added Support for Restore-as-files for SQL Databases.</span></span>

#### <a name="azresources"></a><span data-ttu-id="852cd-393">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="852cd-393">Az.Resources</span></span>
* <span data-ttu-id="852cd-394">템플릿 배포 cmdlet이 리팩터링되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-394">Refactored template deployment cmdlets</span></span>
    - <span data-ttu-id="852cd-395">관리 그룹에서 배포를 관리하는 새 \*-AzManagementGroupDeployment cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-395">Added new cmdlets for managing deployments at management group: \*-AzManagementGroupDeployment</span></span>
    - <span data-ttu-id="852cd-396">테넌트 범위에서 배포를 관리하는 새 \*-AzTenantDeployment cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-396">Added new cmdlets for managing deployments at tenant scope: \*-AzTenantDeployment</span></span>
    - <span data-ttu-id="852cd-397">구독 범위에서 구체적으로 작동하도록 \*-AzDeployment cmdlet이 리팩터링되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-397">Refactored \*-AzDeployment cmdlets to work specifically at subscription scope</span></span>
    - <span data-ttu-id="852cd-398">\*-AzDeployment cmdlet에 대한 \*-AzSubscriptionDeployment 별칭이 만들어졌습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-398">Created aliases \*-AzSubscriptionDeployment for \*-AzDeployment cmdlets</span></span>
* <span data-ttu-id="852cd-399">'AvailableToOtherTenants' 매개 변수가 설정되지 않는 'Update-AzADApplication'이 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-399">Fixed 'Update-AzADApplication' when parameter 'AvailableToOtherTenants' is not set</span></span>
* <span data-ttu-id="852cd-400">AmbiguousParameterSetException을 방지하기 위해 ApplicationObjectWithoutCredentialParameterSet이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-400">Removed ApplicationObjectWithoutCredentialParameterSet to avoid AmbiguousParameterSetException.</span></span>
* <span data-ttu-id="852cd-401">도움말 파일이 다시 생성되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-401">Regenerated help files</span></span>

#### <a name="azsql"></a><span data-ttu-id="852cd-402">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="852cd-402">Az.Sql</span></span>
* <span data-ttu-id="852cd-403">Managed Instance에서 구독 간 특정 시점 복원에 대한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-403">Added support for cross subscription point in time restore on Managed Instances.</span></span>
* <span data-ttu-id="852cd-404">기존 SQL Managed Instance 하드웨어 생성 변경에 대한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-404">Added support for changing existing Sql Managed Instance hardware generation</span></span>
* <span data-ttu-id="852cd-405">'Update-AzSqlServerVulnerabilityAssessmentSetting' 도움말 예제(매개 변수/속성 출력 -EmailAdmins)가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-405">Fixed 'Update-AzSqlServerVulnerabilityAssessmentSetting' help examples: parameter/property output - EmailAdmins</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="852cd-406">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="852cd-406">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="852cd-407">가용성 그룹 수신기에 대한 cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-407">Added cmdlets for Availability Group Listener</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="852cd-408">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="852cd-408">Az.StorageSync</span></span>
* <span data-ttu-id="852cd-409">'Invoke-AzStorageSyncCompatibilityCheck'에서 지원되는 문자 세트가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-409">Updated supported character sets in 'Invoke-AzStorageSyncCompatibilityCheck'.</span></span>

## <a name="340---february-2020"></a><span data-ttu-id="852cd-410">3.4.0 - 2020년 2월</span><span class="sxs-lookup"><span data-stu-id="852cd-410">3.4.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="852cd-411">마지막 주 릴리스 이후의 주요 사항</span><span class="sxs-lookup"><span data-stu-id="852cd-411">Highlights since the last major release</span></span>
* <span data-ttu-id="852cd-412">Az. CosmosDB 초기 버전 0.1.0 출시</span><span class="sxs-lookup"><span data-stu-id="852cd-412">Az.CosmosDB initial version 0.1.0 released</span></span>
* <span data-ttu-id="852cd-413">Az.Network ConnectionMonitor V2 지원 추가</span><span class="sxs-lookup"><span data-stu-id="852cd-413">Az.Network ConnectionMonitor V2 support added</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="852cd-414">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="852cd-414">Az.Accounts</span></span>
* <span data-ttu-id="852cd-415">AzureRmContext.json을 사용할 수 없을 때 컨텍스트 자동 저장 사용 안 함</span><span class="sxs-lookup"><span data-stu-id="852cd-415">Disable context auto saving when AzureRmContext.json not available</span></span>
* <span data-ttu-id="852cd-416">Azure Powershell Common 참조를 1.3.5-preview로 업데이트</span><span class="sxs-lookup"><span data-stu-id="852cd-416">Update the reference to Azure Powershell Common to 1.3.5-preview</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="852cd-417">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="852cd-417">Az.ApiManagement</span></span>
* <span data-ttu-id="852cd-418">**Get-AzApiManagementApiSchema** API와 연결된 Open-Api 스키마 가져오기 수정   https://github.com/Azure/azure-powershell/issues/10626</span><span class="sxs-lookup"><span data-stu-id="852cd-418">**Get-AzApiManagementApiSchema** Fixed getting Open-Api Schema associated with an API   https://github.com/Azure/azure-powershell/issues/10626</span></span>
* <span data-ttu-id="852cd-419">**New-AzApiManagementProduct**\* 및 **Set-AzApiManagementProduct**</span><span class="sxs-lookup"><span data-stu-id="852cd-419">**New-AzApiManagementProduct**\* and **Set-AzApiManagementProduct**</span></span>
  - <span data-ttu-id="852cd-420">https://github.com/Azure/azure-powershell/issues/10472 설명서 수정</span><span class="sxs-lookup"><span data-stu-id="852cd-420">Fix documentation for https://github.com/Azure/azure-powershell/issues/10472</span></span>
* <span data-ttu-id="852cd-421">**Set-AzApiManagementApi** cmdlet을 사용하여 ServiceUrl을 업데이트하는 방법을 보여주는 예제 추가</span><span class="sxs-lookup"><span data-stu-id="852cd-421">**Set-AzApiManagementApi** Added example to show how to update the ServiceUrl using the cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="852cd-422">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="852cd-422">Az.Compute</span></span>
* <span data-ttu-id="852cd-423">VM 이름을 사용하지 않고 Get-AzVM -Status를 수행할 때 제한을 피하기 위해 VM 상태 수를 100개로 제한</span><span class="sxs-lookup"><span data-stu-id="852cd-423">Limit the number of VM status to 100 to avoid throttling when Get-AzVM -Status is performed without VM name.</span></span>
* <span data-ttu-id="852cd-424">Update-AzDiskEncryptionSet cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="852cd-424">Add Update-AzDiskEncryptionSet cmdlet</span></span>
* <span data-ttu-id="852cd-425">다음 cmdlet에 EncryptionType 및 DiskEncryptionSetId 매개 변수 추가:</span><span class="sxs-lookup"><span data-stu-id="852cd-425">Add EncryptionType and DiskEncryptionSetId parameters to the following cmdlets:</span></span>
    - <span data-ttu-id="852cd-426">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="852cd-426">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span></span>
* <span data-ttu-id="852cd-427">Get-AzProximityPlacementGroup cmdlet에 ColocationStatus 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="852cd-427">Add ColocationStatus parameter to Get-AzProximityPlacementGroup cmdlet.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="852cd-428">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="852cd-428">Az.DataFactory</span></span>
* <span data-ttu-id="852cd-429">ADF .Net SDK 버전을 4.7.0으로 업데이트</span><span class="sxs-lookup"><span data-stu-id="852cd-429">Update ADF .Net SDK version to 4.7.0</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="852cd-430">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="852cd-430">Az.DeploymentManager</span></span>
* <span data-ttu-id="852cd-431">리소스에 대한 LIST 작업 추가</span><span class="sxs-lookup"><span data-stu-id="852cd-431">Adds LIST operations for resources</span></span>
* <span data-ttu-id="852cd-432">상태 검사 단계에 대한 작업을 수행하는 기능 추가</span><span class="sxs-lookup"><span data-stu-id="852cd-432">Adds capability for performing operations on Health Check steps</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="852cd-433">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="852cd-433">Az.HDInsight</span></span>
* <span data-ttu-id="852cd-434">AzHDInsightCluster의 문서 오류 수정</span><span class="sxs-lookup"><span data-stu-id="852cd-434">Fix document error of New-AzHDInsightCluster.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="852cd-435">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="852cd-435">Az.KeyVault</span></span>
* <span data-ttu-id="852cd-436">Remove-AzureKeyVault가 새 New-AzureKeyVault와 일관성을 유지하도록 VaultName 특성에 이름 별칭 추가</span><span class="sxs-lookup"><span data-stu-id="852cd-436">Add Name alias to VaultName attribute to make Remove-AzureKeyVault consistent with New-AzureKeyVault.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="852cd-437">Az.Network</span><span class="sxs-lookup"><span data-stu-id="852cd-437">Az.Network</span></span>
* <span data-ttu-id="852cd-438">Set-AzNetworkWatcherConfigFlowLog.md에 트래픽 분석 사용 안 함 시나리오를 보여주는 새 예제 추가</span><span class="sxs-lookup"><span data-stu-id="852cd-438">New example added to Set-AzNetworkWatcherConfigFlowLog.md to demonstrate Traffic Analytics disable scenario.</span></span>
* <span data-ttu-id="852cd-439">Azure Firewall에 관리 IP 구성을 할당하는 지원 추가 - 방화벽에서 관리 트래픽에 사용할 전용 서브넷 및 공용 IP</span><span class="sxs-lookup"><span data-stu-id="852cd-439">Add support for assigning management IP configuration to Azure Firewall - a dedicated subnet and Public IP that the firewall will use for its management traffic</span></span>
    - <span data-ttu-id="852cd-440">New-AzFirewall cmdlet이 업데이트됨:</span><span class="sxs-lookup"><span data-stu-id="852cd-440">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="852cd-441">공용 IP 주소 개체를 허용하는 -ManagementPublicIpAddress 매개 변수(필수 아님) 추가</span><span class="sxs-lookup"><span data-stu-id="852cd-441">Added parameter -ManagementPublicIpAddress (not mandatory) which accepts a Public IP Address object</span></span>
        - <span data-ttu-id="852cd-442">방화벽 개체에 SetManagementIpConfiguration 메서드 추가 - 입력으로 서브넷 및 공용 IP 주소 필요 - 서브넷 이름은 'AzureFirewallManagementSubnet'이어야 함</span><span class="sxs-lookup"><span data-stu-id="852cd-442">Added method SetManagementIpConfiguration on firewall object - requires a subnet and a Public IP address as input - subnet name must be 'AzureFirewallManagementSubnet'</span></span>
* <span data-ttu-id="852cd-443">네트워크 인터페이스 대신 NSG 예제를 보여주도록 AzNetworkSecurityGroup 예제 수정</span><span class="sxs-lookup"><span data-stu-id="852cd-443">Corrected Get-AzNetworkSecurityGroup examples to show examples for NSG's instead of network interfaces.</span></span>
* <span data-ttu-id="852cd-444">리소스 id 완성자가 매개 변수를 완성하지 못하게 방해하던 New-AzVpnSite 명령의 오타 수정</span><span class="sxs-lookup"><span data-stu-id="852cd-444">Fixed typo in New-AzVpnSite command that was preventing resource id completer from completing a parameter.</span></span>
* <span data-ttu-id="852cd-445">Application Gateway의 다시 쓰기 규칙 작업 세트에서 Url 구성에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="852cd-445">Added support for Url Confiugration in Rewrite Rules Action Set in the Application Gateway</span></span>
    - <span data-ttu-id="852cd-446">추가된 새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-446">New cmdlets added:</span></span>
        - <span data-ttu-id="852cd-447">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="852cd-447">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span></span>
    - <span data-ttu-id="852cd-448">선택적 매개 변수를 사용하도록 Cmdlet 업데이트 - UrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="852cd-448">Cmdlets updated with optional parameter - UrlConfiguration</span></span>
        - <span data-ttu-id="852cd-449">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="852cd-449">New-AzApplicationGatewayRewriteRuleActionSet</span></span>
* <span data-ttu-id="852cd-450">NetworkWatcher ConnectionMonitor 버전 2 리소스에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="852cd-450">Add suppport for NetworkWatcher ConnectionMonitor version 2 resources</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="852cd-451">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="852cd-451">Az.PolicyInsights</span></span>
* <span data-ttu-id="852cd-452">수정할 리소스를 결정하기 전에 규정 준수 평가 지원</span><span class="sxs-lookup"><span data-stu-id="852cd-452">Support evaluating compliance prior to determining what resource to remediate</span></span>
    - <span data-ttu-id="852cd-453">Start-AzPolicyRemediation에 '-ResourceDiscoverMode' 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="852cd-453">Add '-ResourceDiscoverMode' parameter to Start-AzPolicyRemediation</span></span>
* <span data-ttu-id="852cd-454">정책 메타데이터 리소스를 가져오는 Get-AzPolicyMetadata cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="852cd-454">Add Get-AzPolicyMetadata cmdlet for getting policy metadata resources</span></span>
* <span data-ttu-id="852cd-455">API 버전 2019-10-01의 Get-AzPolicyState 및 Get-AzPolicyStateSummary 업데이트</span><span class="sxs-lookup"><span data-stu-id="852cd-455">Updated Get-AzPolicyState and Get-AzPolicyStateSummary for API version 2019-10-01</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="852cd-456">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="852cd-456">Az.RecoveryServices</span></span>
* <span data-ttu-id="852cd-457">복제된 디스크를 제거할 수 있도록 Azure Site Recovery에 지원 추가</span><span class="sxs-lookup"><span data-stu-id="852cd-457">Azure Site Recovery support for removing a replicated disk.</span></span>
* <span data-ttu-id="852cd-458">Recovery Services 자격 증명 모음을 만드는 동안 태그를 추가할 수 있도록 Azure Backup에 지원 추가</span><span class="sxs-lookup"><span data-stu-id="852cd-458">Azure Backup added support for adding tags while creating a Recovery Services Vault.</span></span>

#### <a name="azresources"></a><span data-ttu-id="852cd-459">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="852cd-459">Az.Resources</span></span>
* <span data-ttu-id="852cd-460">컨텍스트 구독을 기본값으로 하는 \*-AzPolicyAssignment cmdlet에서 -Scope를 선택 사항으로 설정</span><span class="sxs-lookup"><span data-stu-id="852cd-460">Make -Scope optional in \*-AzPolicyAssignment cmdlets with default to context subscription</span></span>
* <span data-ttu-id="852cd-461">암호 및 키 자격 증명을 사용하여 ADServicePrincipal을 만드는 예제 추가</span><span class="sxs-lookup"><span data-stu-id="852cd-461">Add examples of creating ADServicePrincipal with password and key credential</span></span>

#### <a name="azsql"></a><span data-ttu-id="852cd-462">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="852cd-462">Az.Sql</span></span>
<span data-ttu-id="852cd-463">DatabaseName 대신 PartnerDatabaseName이 있는지 확인하도록 New-AzSqlDatabaseSecondary cmdlet 수정</span><span class="sxs-lookup"><span data-stu-id="852cd-463">Fix New-AzSqlDatabaseSecondary cmdlet to check for PartnerDatabaseName existence instead of DatabaseName existence.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="852cd-464">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="852cd-464">Az.Storage</span></span>
* <span data-ttu-id="852cd-465">스토리지 계정 만들기에서 테이블/큐 암호화 Keytype 설정 지원</span><span class="sxs-lookup"><span data-stu-id="852cd-465">Support set Table/Queue Encryption Keytype in Create Storage Account</span></span>
    - <span data-ttu-id="852cd-466">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="852cd-466">New-AzStorageAccount</span></span>
* <span data-ttu-id="852cd-467">StorageException에 ExtendedErrorInformation이 없으면 RequestId 표시</span><span class="sxs-lookup"><span data-stu-id="852cd-467">Show RequestId when StorageException don't have ExtendedErrorInformation</span></span>
* <span data-ttu-id="852cd-468">cmdlet Start-AzStorageBlobCopy의 예제 6 수정</span><span class="sxs-lookup"><span data-stu-id="852cd-468">Fix the Example 6 of cmdlet Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="852cd-469">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="852cd-469">Az.Websites</span></span>
* <span data-ttu-id="852cd-470">Set-AzWebapp 및 Set-AzWebappSlot이 AlwaysOn, MinTls 및 FtpsState 속성 지원</span><span class="sxs-lookup"><span data-stu-id="852cd-470">Set-AzWebapp and Set-AzWebappSlot supports AlwaysOn, MinTls and FtpsState properties</span></span>
* <span data-ttu-id="852cd-471">단일 Set-AzWebApp 명령을 사용하여 AppservicePlan을 변경하는 동시에 HttpsOnly를 설정하면 HttpsOnly가 기본값으로 다시 설정되는 문제 수정</span><span class="sxs-lookup"><span data-stu-id="852cd-471">Fixing issue where setting HttpsOnly along with changing AppservicePlan at the same time using the single Set-AzWebApp Command, was resetting HttpsOnly to default value</span></span>

## <a name="330---january-2020"></a><span data-ttu-id="852cd-472">3.3.0 - 2020년 1월</span><span class="sxs-lookup"><span data-stu-id="852cd-472">3.3.0 - January 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="852cd-473">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="852cd-473">Az.Accounts</span></span>
* <span data-ttu-id="852cd-474">AzureAttestationServiceEndpointResourceId 및 AzureAttestationServiceEndpointSuffix 매개 변수를 허용하도록 Add-AzEnvironment 및 Set-AzEnvironment가 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="852cd-474">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameters AzureAttestationServiceEndpointResourceId and AzureAttestationServiceEndpointSuffix</span></span>

#### <a name="azcdn"></a><span data-ttu-id="852cd-475">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="852cd-475">Az.Cdn</span></span>
* <span data-ttu-id="852cd-476">New-AzCdnEndpoint cmdlet에서 오류 응답 세부 정보 표시</span><span class="sxs-lookup"><span data-stu-id="852cd-476">Display error response detail in New-AzCdnEndpoint cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="852cd-477">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="852cd-477">Az.Compute</span></span>
* <span data-ttu-id="852cd-478">OS 프로필이 없는 관리 OD 디스크가 있는 VM의 Set-AzVMCustomScriptExtension cmdlet을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-478">Fix Set-AzVMCustomScriptExtension cmdlet for a VM with managed OD disk which does not have OS profile.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="852cd-479">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="852cd-479">Az.ContainerInstance</span></span>
* <span data-ttu-id="852cd-480">New-AzContainerGroup의 예에서 사용되는 고정 매개 변수 이름</span><span class="sxs-lookup"><span data-stu-id="852cd-480">Fixed parameter names used by example of New-AzContainerGroup</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="852cd-481">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="852cd-481">Az.DataBoxEdge</span></span>
* <span data-ttu-id="852cd-482">'Get-AzDataBoxEdgeStorageContainer' cmdlet 추가됨</span><span class="sxs-lookup"><span data-stu-id="852cd-482">Added cmdlet 'Get-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="852cd-483">Edge 스토리지 컨테이너 가져오기</span><span class="sxs-lookup"><span data-stu-id="852cd-483">Get the Edge Storage Container</span></span>
* <span data-ttu-id="852cd-484">'New-AzDataBoxEdgeStorageContainer' cmdlet 추가됨</span><span class="sxs-lookup"><span data-stu-id="852cd-484">Added cmdlet 'New-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="852cd-485">새 Edge 스토리지 컨테이너 만들기</span><span class="sxs-lookup"><span data-stu-id="852cd-485">Create new Edge Strorage Container</span></span>
* <span data-ttu-id="852cd-486">'Remove-AzDataBoxEdgeStorageContainer' cmdlet 추가됨</span><span class="sxs-lookup"><span data-stu-id="852cd-486">Added cmdlet 'Remove-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="852cd-487">Edge 스토리지 컨테이너 제거</span><span class="sxs-lookup"><span data-stu-id="852cd-487">Remove the Edge Storage Container</span></span>
* <span data-ttu-id="852cd-488">'Invoke-AzDataBoxEdgeStorageContainer' cmdlet 추가됨</span><span class="sxs-lookup"><span data-stu-id="852cd-488">Added cmdlet 'Invoke-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="852cd-489">Edge 스토리지 컨테이너에서 데이터를 새로 고치는 작업 호출</span><span class="sxs-lookup"><span data-stu-id="852cd-489">Invoke action to refresh data on Edge Storage Container</span></span>
* <span data-ttu-id="852cd-490">'Get-AzDataBoxEdgeStorageAccount' cmdlet 추가됨</span><span class="sxs-lookup"><span data-stu-id="852cd-490">Added cmdlet 'Get-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="852cd-491">Edge 스토리지 계정 가져오기</span><span class="sxs-lookup"><span data-stu-id="852cd-491">Get the Edge Storage Account</span></span>
* <span data-ttu-id="852cd-492">'New-AzDataBoxEdgeStorageAccount' cmdlet 추가됨</span><span class="sxs-lookup"><span data-stu-id="852cd-492">Added cmdlet 'New-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="852cd-493">새 Edge 스토리지 계정 만들기</span><span class="sxs-lookup"><span data-stu-id="852cd-493">Create new Edge Storage Account</span></span>
* <span data-ttu-id="852cd-494">'Remove-AzDataBoxEdgeStorageAccount' cmdlet 추가됨</span><span class="sxs-lookup"><span data-stu-id="852cd-494">Added cmdlet 'Remove-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="852cd-495">Edge 스토리지 계정 제거</span><span class="sxs-lookup"><span data-stu-id="852cd-495">Remove the Edge Storage Account</span></span>
* <span data-ttu-id="852cd-496">'Invoke-AzDataBoxEdgeShare' cmdlet 호출</span><span class="sxs-lookup"><span data-stu-id="852cd-496">Invoke cmdlet 'Invoke-AzDataBoxEdgeShare'</span></span>
  - <span data-ttu-id="852cd-497">공유에서 데이터를 새로 고치는 작업 호출</span><span class="sxs-lookup"><span data-stu-id="852cd-497">Invoke action to refresh data on share</span></span>
* <span data-ttu-id="852cd-498">'Set-AzDataBoxEdgeStorageAccountCredential' cmdlet 추가됨</span><span class="sxs-lookup"><span data-stu-id="852cd-498">Added cmdlet 'Set-AzDataBoxEdgeStorageAccountCredential'</span></span>
  - <span data-ttu-id="852cd-499">az databoxedge 스토리지 계정 자격 증명 설정</span><span class="sxs-lookup"><span data-stu-id="852cd-499">Set the az databoxedge storage account credential</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="852cd-500">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="852cd-500">Az.DataFactory</span></span>
* <span data-ttu-id="852cd-501">Get-AzDataFactoryV2IntegrationRuntime cmd에 AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId 및 VersionStatus 속성 추가</span><span class="sxs-lookup"><span data-stu-id="852cd-501">Add AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId and VersionStatus properties for Get-AzDataFactoryV2IntegrationRuntime cmd</span></span>
* <span data-ttu-id="852cd-502">ADF .Net SDK 버전을 4.6.0으로 업데이트</span><span class="sxs-lookup"><span data-stu-id="852cd-502">Update ADF .Net SDK version to 4.6.0</span></span>
* <span data-ttu-id="852cd-503">고정 공용 IP 주소로 Azure-SSIS IR을 만들 수 있도록 'Set-AzureRmDataFactoryV2IntegrationRuntime'cmd에 대해 'PublicIPs' 매개 변수를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-503">Add parameter 'PublicIPs' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable create Azure-SSIS IR with static public IP addresses.</span></span>

#### <a name="azdevtestlabs"></a><span data-ttu-id="852cd-504">Az.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="852cd-504">Az.DevTestLabs</span></span>
* <span data-ttu-id="852cd-505">Get-AzDtlAllowedVMSizesPolicy.md에서 끊어진 링크 제거</span><span class="sxs-lookup"><span data-stu-id="852cd-505">Remove the broken link in Get-AzDtlAllowedVMSizesPolicy.md</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="852cd-506">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="852cd-506">Az.EventHub</span></span>
* <span data-ttu-id="852cd-507">10634 문제 해결: eventhubnamespace 제거에 대한 null 개체 참조 수정</span><span class="sxs-lookup"><span data-stu-id="852cd-507">Fix for issue 10634 : Fix the null Object reference for remove eventhubnamespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="852cd-508">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="852cd-508">Az.HDInsight</span></span>
* <span data-ttu-id="852cd-509">Invoke-AzHDInsightHiveJob.md 오류를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-509">Fix Invoke-AzHDInsightHiveJob.md error.</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="852cd-510">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="852cd-510">Az.MachineLearning</span></span>
* <span data-ttu-id="852cd-511">MachineLearningCompute를 더 이상 사용할 수 없게 되어 아래 cmdlet이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-511">Removed below cmdlets because MachineLearningCompute is not available any longer</span></span>
  - <span data-ttu-id="852cd-512">Get-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="852cd-512">Get-AzMlOpCluster</span></span>
  - <span data-ttu-id="852cd-513">Get-AzMlOpClusterKey</span><span class="sxs-lookup"><span data-stu-id="852cd-513">Get-AzMlOpClusterKey</span></span>
  - <span data-ttu-id="852cd-514">New-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="852cd-514">New-AzMlOpCluster</span></span>
  - <span data-ttu-id="852cd-515">Remove-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="852cd-515">Remove-AzMlOpCluster</span></span>
  - <span data-ttu-id="852cd-516">Set-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="852cd-516">Set-AzMlOpCluster</span></span>
  - <span data-ttu-id="852cd-517">Test-AzMlOpClusterSystemServicesUpdateAvailability</span><span class="sxs-lookup"><span data-stu-id="852cd-517">Test-AzMlOpClusterSystemServicesUpdateAvailability</span></span>
  - <span data-ttu-id="852cd-518">Update-AzMlOpClusterSystemService</span><span class="sxs-lookup"><span data-stu-id="852cd-518">Update-AzMlOpClusterSystemService</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="852cd-519">Az.Network</span><span class="sxs-lookup"><span data-stu-id="852cd-519">Az.Network</span></span>
* <span data-ttu-id="852cd-520">Microsoft.Azure.Management.Sql의 종속성을 1.36-preview에서 1.37-preview로 업그레이드</span><span class="sxs-lookup"><span data-stu-id="852cd-520">Upgrade dependency of Microsoft.Azure.Management.Sql from 1.36-preview to 1.37-preview</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="852cd-521">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="852cd-521">Az.RecoveryServices</span></span>
* <span data-ttu-id="852cd-522">Azure Site Recovery는 Azure 간 공급자를 위해 고객 관리 키와 함께 유휴 상태에서 암호화된 관리 디스크 vms의 변경을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-522">Azure Site Recovery change support for managed disk vms encrypted at rest with customer managed keys for Azure to Azure provider.</span></span>
* <span data-ttu-id="852cd-523">Azure Site Recovery는 VMware에서 Azure로를 위해 보호를 사용할 때 선택적 입력으로서 디스크 암호화 집합 ID를 입력하도록 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-523">Azure Site Recovery support to input disk encryption Set Id as optional input at enabling protection for Vmware to Azure.</span></span>
* <span data-ttu-id="852cd-524">Azure Site Recovery는 VMware에서 Azure로를 위해 보호를 사용하기 위해 디스크 수준의 선택적 입력으로서 디스크 암호화 집합 ID를 입력하도록 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-524">Azure Site Recovery support to input disk encryption Set Id as optional input at disk level to enable protection for Vmware to Azure.</span></span>
* <span data-ttu-id="852cd-525">Azure Site Recovery는 HyperV에서 Azure로를 위해 디스크 암호화 집합 맵을 사용하여 복제 보호된 항목을 업데이트하도록 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-525">Azure Site Recovery support to update replication protected item with disk encryption set Map for HyperV to Azure.</span></span>

#### <a name="azresources"></a><span data-ttu-id="852cd-526">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="852cd-526">Az.Resources</span></span>
* <span data-ttu-id="852cd-527">'Remove-AzTag'의 도움말 문서에서 오류를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-527">Fix an error in help document of 'Remove-AzTag'.</span></span>

#### <a name="azsql"></a><span data-ttu-id="852cd-528">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="852cd-528">Az.Sql</span></span>
* <span data-ttu-id="852cd-529">Azure Database의 마스터 DB에서 작동하도록 취약성 평가 세트 기준 cmdlet 기능을 수정하고 관리형 인스턴스 시스템 데이터베이스에서 이를 제한합니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-529">Fix vulnerability assessment set baseline cmdlets functionality to work on master db for azure database and limit it on managed instance system databases.</span></span>
* <span data-ttu-id="852cd-530">SQL 인스턴스 장애 조치(failover) 그룹을 만들 때 오류 수정</span><span class="sxs-lookup"><span data-stu-id="852cd-530">Fix an error when creating SQL instance failover group</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="852cd-531">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="852cd-531">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="852cd-532">올바른 새 라이선스 형식으로 DR 추가</span><span class="sxs-lookup"><span data-stu-id="852cd-532">Add DR as a new valid License type</span></span>

#### <a name="azstorage"></a><span data-ttu-id="852cd-533">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="852cd-533">Az.Storage</span></span>
* <span data-ttu-id="852cd-534">다음 릴리스에서 DefaultAction Value 변경에 대해 호환성이 손상되는 변경 경고 메시지 추가</span><span class="sxs-lookup"><span data-stu-id="852cd-534">Add breaking change warning message for DefaultAction Value change in a future release</span></span>
    - <span data-ttu-id="852cd-535">Update-AzStorageAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="852cd-535">Update-AzStorageAccountNetworkRuleSet</span></span>
* <span data-ttu-id="852cd-536">-IncludeGeoReplicationStats 매개 변수와 함께 get-AzureRMStorageAccount를 실행하여 스토리지 계정의 마지막 동기화 시간 가져오기 지원</span><span class="sxs-lookup"><span data-stu-id="852cd-536">Support Get last sync time of Storage account by run get-AzureRMStorageAccount with parameter -IncludeGeoReplicationStats</span></span>
    - <span data-ttu-id="852cd-537">Get-AzureRMStorageAccount</span><span class="sxs-lookup"><span data-stu-id="852cd-537">Get-AzureRMStorageAccount</span></span>

## <a name="320---december-2019"></a><span data-ttu-id="852cd-538">3.2.0 - 2019년 12월</span><span class="sxs-lookup"><span data-stu-id="852cd-538">3.2.0 - December 2019</span></span>

### <a name="general"></a><span data-ttu-id="852cd-539">일반</span><span class="sxs-lookup"><span data-stu-id="852cd-539">General</span></span>
* <span data-ttu-id="852cd-540">모든 모듈의 상대 경로를 사용하기 위해 .psd1의 참조 업데이트</span><span class="sxs-lookup"><span data-stu-id="852cd-540">Update references in .psd1 to use relative path for all modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="852cd-541">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="852cd-541">Az.Accounts</span></span>
* <span data-ttu-id="852cd-542">Az 4.0 미리 보기를 위해 클라이언트 측 원격 분석에 대해 UserAgent를 올바르게 설정</span><span class="sxs-lookup"><span data-stu-id="852cd-542">Set correct UserAgent for client-side telemetry for Az 4.0 preview</span></span>
* <span data-ttu-id="852cd-543">Az 4.0 미리 보기에서 컨텍스트가 null인 경우 사용자에게 친숙한 오류 메시지로 표시</span><span class="sxs-lookup"><span data-stu-id="852cd-543">Display user friendly error message when context is null in Az 4.0 preview</span></span>

#### <a name="azbatch"></a><span data-ttu-id="852cd-544">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="852cd-544">Az.Batch</span></span>
* <span data-ttu-id="852cd-545">**New-AzBatchPool**이 'VirtualMachineConfiguration.ContainerConfiguration' 또는 'VirtualMachineConfiguration.DataDisks'를 서버로 제대로 보내지 않는 [#10602](https://github.com/Azure/azure-powershell/issues/10602) 문제 수정</span><span class="sxs-lookup"><span data-stu-id="852cd-545">Fix issue [#10602](https://github.com/Azure/azure-powershell/issues/10602), where **New-AzBatchPool** did not properly send 'VirtualMachineConfiguration.ContainerConfiguration' or 'VirtualMachineConfiguration.DataDisks' to the server.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="852cd-546">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="852cd-546">Az.DataFactory</span></span>
* <span data-ttu-id="852cd-547">ADF .Net SDK 버전을 4.5.0으로 업데이트</span><span class="sxs-lookup"><span data-stu-id="852cd-547">Update ADF .Net SDK version to 4.5.0</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="852cd-548">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="852cd-548">Az.FrontDoor</span></span>
* <span data-ttu-id="852cd-549">WAF 관리 규칙 제외 지원 추가됨</span><span class="sxs-lookup"><span data-stu-id="852cd-549">Added WAF managed rules exclusion support</span></span>
* <span data-ttu-id="852cd-550">자동 완성에 SocketAddr 추가</span><span class="sxs-lookup"><span data-stu-id="852cd-550">Add SocketAddr to auto-complete</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="852cd-551">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="852cd-551">Az.HealthcareApis</span></span>
* <span data-ttu-id="852cd-552">예외 처리</span><span class="sxs-lookup"><span data-stu-id="852cd-552">Exception Handling</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="852cd-553">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="852cd-553">Az.KeyVault</span></span>
* <span data-ttu-id="852cd-554">잠재적으로 설정되지 않은 오류 액세스 값 수정</span><span class="sxs-lookup"><span data-stu-id="852cd-554">Fixed error accessing value that is potentially not set</span></span>
* <span data-ttu-id="852cd-555">타원 곡선 암호화 인증서 관리</span><span class="sxs-lookup"><span data-stu-id="852cd-555">Elliptic Curve Cryptography Certificate Managment</span></span>
    - <span data-ttu-id="852cd-556">인증서 정책에 대한 곡선 지정을 위한 지원 추가됨</span><span class="sxs-lookup"><span data-stu-id="852cd-556">Added support to specify the Curve for Certificate Policies</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="852cd-557">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="852cd-557">Az.Monitor</span></span>
* <span data-ttu-id="852cd-558">진단 설정 추가 명령에 선택적 인수 추가</span><span class="sxs-lookup"><span data-stu-id="852cd-558">Adding optional argument to the Add Diagnostic Settings command.</span></span> <span data-ttu-id="852cd-559">스위치 인수(있는 경우)는 Log Analytics로 내보내기가 고정 스키마(전용 데이터 유형)가 되어야 함을</span><span class="sxs-lookup"><span data-stu-id="852cd-559">A switch argument that if present indicates that the export to Log Analytics must be to a fixed schema (a.k.a.</span></span> <span data-ttu-id="852cd-560">나타냄</span><span class="sxs-lookup"><span data-stu-id="852cd-560">dedicated, data type)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="852cd-561">Az.Network</span><span class="sxs-lookup"><span data-stu-id="852cd-561">Az.Network</span></span>
* <span data-ttu-id="852cd-562">AzureFirewall 애플리케이션, NAT 및 네트워크 규칙에서 IpGroups 지원.</span><span class="sxs-lookup"><span data-stu-id="852cd-562">Support for IpGroups in AzureFirewall Application,Nat & Network Rules.</span></span>

#### <a name="azresources"></a><span data-ttu-id="852cd-563">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="852cd-563">Az.Resources</span></span>
* <span data-ttu-id="852cd-564">이름이 일부 내장 매개 변수 이름과 충돌하는 경우 템플릿 배포가 템플릿 매개 변수를 읽지 못하는 문제 수정.</span><span class="sxs-lookup"><span data-stu-id="852cd-564">Fix an issue where template deployment fails to read a template parameter if its name conflicts with some built-in parameter name.</span></span>
* <span data-ttu-id="852cd-565">정책 세트 정의 내에 그룹화 지원을 도입하는 새로운 API 버전 2019-09-01을 사용하도록 정책 cmdlet 업데이트.</span><span class="sxs-lookup"><span data-stu-id="852cd-565">Updated policy cmdlets to use new api version 2019-09-01 that introduces grouping support within policy set definitions.</span></span>

#### <a name="azsql"></a><span data-ttu-id="852cd-566">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="852cd-566">Az.Sql</span></span>
* <span data-ttu-id="852cd-567">취약성 평가 자동 활성화에서 스토리지 생성을 StorageV2로 업그레이드</span><span class="sxs-lookup"><span data-stu-id="852cd-567">Upgraded storage creation in Vulnerability Assessment auto enablement to StorageV2</span></span>

#### <a name="azstorage"></a><span data-ttu-id="852cd-568">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="852cd-568">Az.Storage</span></span>
* <span data-ttu-id="852cd-569">Oauth 인증을 기반으로 스토리지 컨텍스트를 사용하여 Blob/컨테이너 ID 기반 SAS 토큰 생성 지원</span><span class="sxs-lookup"><span data-stu-id="852cd-569">Support generate Blob/Constainer Idenity based SAS token with Storage Context based on Oauth authentication</span></span>
    - <span data-ttu-id="852cd-570">New-AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="852cd-570">New-AzStorageContainerSASToken</span></span>
    - <span data-ttu-id="852cd-571">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="852cd-571">New-AzStorageBlobSASToken</span></span>
* <span data-ttu-id="852cd-572">모든 Idenity SAS 토큰을 해지할 수 있도록 스토리지 계정 사용자 위임 키 해지 지원</span><span class="sxs-lookup"><span data-stu-id="852cd-572">Support revoke Storage Account User Delegation Keys, so all Idenity SAS tokens are revoked</span></span>
    - <span data-ttu-id="852cd-573">Revoke-AzStorageAccountUserDelegationKeys</span><span class="sxs-lookup"><span data-stu-id="852cd-573">Revoke-AzStorageAccountUserDelegationKeys</span></span>
* <span data-ttu-id="852cd-574">새로운 API 버전 2019-06-01을 지원하기 위해 Microsoft.Azure.Management.Storage 14.2.0으로 업그레이드.</span><span class="sxs-lookup"><span data-stu-id="852cd-574">Upgrade to Microsoft.Azure.Management.Storage 14.2.0, to support new API version 2019-06-01.</span></span>
* <span data-ttu-id="852cd-575">File Share cmdlet의 관리 평면에서 5120을 초과하는 값에 대해 QuotaGiB(Gibyby의 공유 할당량)를 지원하고 'Quota' 매개 변수 별칭을 'QuotaGiB' 매개 변수에 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-575">Support of QuotaGiB (Share Quota in Gibibye) for values of more than 5120 in the Management plane of File Share cmdlets and added the 'Quota' parameter alias to the 'QuotaGiB' parameter.</span></span>
    - <span data-ttu-id="852cd-576">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="852cd-576">New-AzRmStorageShare</span></span>
    - <span data-ttu-id="852cd-577">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="852cd-577">Update-AzRmStorageShare</span></span>
* <span data-ttu-id="852cd-578">매개 변수 'Quota'에 매개 변수 별칭 'QuotaGiB' 추가</span><span class="sxs-lookup"><span data-stu-id="852cd-578">Add parameter alias 'QuotaGiB' to parameter 'Quota'</span></span>
    - <span data-ttu-id="852cd-579">Set-AzStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="852cd-579">Set-AzStorageShareQuota</span></span>
* <span data-ttu-id="852cd-580">Set-AzStorageContainerAcl가 저장된 액세스 정책을 정리할 수 있는 문제 수정</span><span class="sxs-lookup"><span data-stu-id="852cd-580">Fix the issue that Set-AzStorageContainerAcl can clean up the stored Access Policy</span></span>
    - <span data-ttu-id="852cd-581">Set-AzStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="852cd-581">Set-AzStorageContainerAcl</span></span>

## <a name="310---november-2019"></a><span data-ttu-id="852cd-582">3.1.0 - 2019년 11월</span><span class="sxs-lookup"><span data-stu-id="852cd-582">3.1.0 - November 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="852cd-583">마지막 주 릴리스 이후의 주요 사항</span><span class="sxs-lookup"><span data-stu-id="852cd-583">Highlights since the last major release</span></span>
* <span data-ttu-id="852cd-584">Az.DataBoxEdge 1.0.0 릴리스됨</span><span class="sxs-lookup"><span data-stu-id="852cd-584">Az.DataBoxEdge 1.0.0 released</span></span>
* <span data-ttu-id="852cd-585">Az.SqlVirtualMachine 1.0.0 릴리스됨</span><span class="sxs-lookup"><span data-stu-id="852cd-585">Az.SqlVirtualMachine 1.0.0 released</span></span>

#### <a name="azcompute"></a><span data-ttu-id="852cd-586">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="852cd-586">Az.Compute</span></span>
* <span data-ttu-id="852cd-587">VM Reapply 기능</span><span class="sxs-lookup"><span data-stu-id="852cd-587">VM Reapply feature</span></span>
    - <span data-ttu-id="852cd-588">Set-AzVM cmdlet에 Reapply 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="852cd-588">Add Reapply parameter to Set-AzVM cmdlet</span></span>
* <span data-ttu-id="852cd-589">VM 확장 집합 AutomaticRepairs 기능:</span><span class="sxs-lookup"><span data-stu-id="852cd-589">VM Scale Set AutomaticRepairs feature:</span></span>
    - <span data-ttu-id="852cd-590">다음 cmdlet에 EnableAutomaticRepair, AutomaticRepairGracePeriod 및 AutomaticRepairMaxInstanceRepairsPercent 매개 변수를 추가합니다.   New-AzVmssConfig   Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="852cd-590">Add EnableAutomaticRepair, AutomaticRepairGracePeriod, and AutomaticRepairMaxInstanceRepairsPercent parameters to the following cmdlets:   New-AzVmssConfig   Update-AzVmss</span></span>
* <span data-ttu-id="852cd-591">New-AzVM에 대한 교차 테넌트 갤러리 이미지 지원</span><span class="sxs-lookup"><span data-stu-id="852cd-591">Cross tenant gallery image support for New-AzVM</span></span>
* <span data-ttu-id="852cd-592">New-AzVM, New-AzVMConfig 및 New-AzVmss cmdlet의 Priority 매개 변수의 인수 완성자에 'Spot' 추가</span><span class="sxs-lookup"><span data-stu-id="852cd-592">Add 'Spot' to the argument completer of Priority parameter in New-AzVM, New-AzVMConfig and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="852cd-593">Add-AzVmssDataDisk cmdlet에 DiskIOPSReadWrite 및 DiskMBpsReadWrite 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="852cd-593">Add DiskIOPSReadWrite and DiskMBpsReadWrite parameters to Add-AzVmssDataDisk cmdlet</span></span>
* <span data-ttu-id="852cd-594">New-AzGalleryImageVersion cmdlet의 SourceImageId 매개 변수를 선택 사항으로 변경</span><span class="sxs-lookup"><span data-stu-id="852cd-594">Change SourceImageId parameter of New-AzGalleryImageVersion cmdlet to optional</span></span>
* <span data-ttu-id="852cd-595">New-AzGalleryImageVersion cmdlet에 OSDiskImage 및 DataDiskImage 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="852cd-595">Add OSDiskImage and DataDiskImage parameters to New-AzGalleryImageVersion cmdlet</span></span>
* <span data-ttu-id="852cd-596">New-AzGalleryImageDefinition cmdlet에 HyperVGeneration 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="852cd-596">Add HyperVGeneration parameter to New-AzGalleryImageDefinition cmdlet</span></span>
* <span data-ttu-id="852cd-597">New-AzVmss, New-AzVmssConfig 및 Update-AzVmss cmdlet에 SkipExtensionsOnOverprovisionedVMs 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="852cd-597">Add SkipExtensionsOnOverprovisionedVMs parameters to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="852cd-598">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="852cd-598">Az.DataBoxEdge</span></span>
* <span data-ttu-id="852cd-599">cmdlet `Get-AzDataBoxEdgeOrder` 추가됨</span><span class="sxs-lookup"><span data-stu-id="852cd-599">Added cmdlet `Get-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="852cd-600">주문 가져오기</span><span class="sxs-lookup"><span data-stu-id="852cd-600">Get the Order</span></span>
* <span data-ttu-id="852cd-601">cmdlet `New-AzDataBoxEdgeOrder` 추가됨</span><span class="sxs-lookup"><span data-stu-id="852cd-601">Added cmdlet `New-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="852cd-602">새 주문 만들기</span><span class="sxs-lookup"><span data-stu-id="852cd-602">Create new Order</span></span>
* <span data-ttu-id="852cd-603">cmdlet `Remove-AzDataBoxEdgeOrder` 추가됨</span><span class="sxs-lookup"><span data-stu-id="852cd-603">Added cmdlet `Remove-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="852cd-604">주문 제거</span><span class="sxs-lookup"><span data-stu-id="852cd-604">Remove the Order</span></span>
* <span data-ttu-id="852cd-605">cmdlet `New-AzDataBoxEdgeShare` 변경</span><span class="sxs-lookup"><span data-stu-id="852cd-605">Change in cmdlet `New-AzDataBoxEdgeShare`</span></span>
    - <span data-ttu-id="852cd-606">이제 로컬 공유를 만듬</span><span class="sxs-lookup"><span data-stu-id="852cd-606">Now creates Local Share</span></span>
* <span data-ttu-id="852cd-607">cmdlet `Set-AzDataBoxEdgeRole` 추가됨</span><span class="sxs-lookup"><span data-stu-id="852cd-607">Added cmdlet `Set-AzDataBoxEdgeRole`</span></span>
    - <span data-ttu-id="852cd-608">이제 IotRole을 공유에 매핑할 수 있음</span><span class="sxs-lookup"><span data-stu-id="852cd-608">Now IotRole can be mapped to Share</span></span>
* <span data-ttu-id="852cd-609">cmdlet `Invoke-AzDataBoxEdgeDevice` 추가됨</span><span class="sxs-lookup"><span data-stu-id="852cd-609">Added cmdlet `Invoke-AzDataBoxEdgeDevice`</span></span>
    - <span data-ttu-id="852cd-610">스캔 업데이트 호출, 업데이트 다운로드, 디바이스에 업데이트 설치</span><span class="sxs-lookup"><span data-stu-id="852cd-610">Invoke scan update, download update, install updates on the device</span></span>
* <span data-ttu-id="852cd-611">cmdlet `Get-AzDataBoxEdgeTrigger` 추가됨</span><span class="sxs-lookup"><span data-stu-id="852cd-611">Added cmdlet `Get-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="852cd-612">트리거에 대한 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="852cd-612">Gets the information about Triggers</span></span>
* <span data-ttu-id="852cd-613">cmdlet `New-AzDataBoxEdgeTrigger` 추가됨</span><span class="sxs-lookup"><span data-stu-id="852cd-613">Added cmdlet `New-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="852cd-614">새 트리거 만들기</span><span class="sxs-lookup"><span data-stu-id="852cd-614">Create new Triggers</span></span>
* <span data-ttu-id="852cd-615">cmdlet `Remove-AzDataBoxEdgeTrigger` 추가됨</span><span class="sxs-lookup"><span data-stu-id="852cd-615">Added cmdlet `Remove-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="852cd-616">트리거 제거</span><span class="sxs-lookup"><span data-stu-id="852cd-616">Remove the Triggers</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="852cd-617">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="852cd-617">Az.DataFactory</span></span>
* <span data-ttu-id="852cd-618">ADF .Net SDK 버전을 4.4.0으로 업데이트</span><span class="sxs-lookup"><span data-stu-id="852cd-618">Update ADF .Net SDK version to 4.4.0</span></span>
* <span data-ttu-id="852cd-619">'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd에 'ExpressCustomSetup' 매개 변수를 추가하여 사용자 지정 설치 스크립트 없이 설치 구성 및 타사 구성 요소를 사용하도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-619">Add parameter 'ExpressCustomSetup' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable setup configurations and 3rd party components without custom setup script.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="852cd-620">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="852cd-620">Az.DataLakeStore</span></span>
* <span data-ttu-id="852cd-621">Get-AzDataLakeStoreDeletedItem 및 Restore-AzDataLakeStoreDeletedItem의 설명서 업데이트</span><span class="sxs-lookup"><span data-stu-id="852cd-621">Update documentation of Get-AzDataLakeStoreDeletedItem and Restore-AzDataLakeStoreDeletedItem</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="852cd-622">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="852cd-622">Az.EventHub</span></span>
* <span data-ttu-id="852cd-623">10301 문제 해결: SAS 토큰 날짜 형식 수정</span><span class="sxs-lookup"><span data-stu-id="852cd-623">Fix for issue 10301 : Fix the SAS Token date format</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="852cd-624">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="852cd-624">Az.FrontDoor</span></span>
* <span data-ttu-id="852cd-625">Enable-AzFrontDoorCustomDomainHttps 및 New-AzFrontDoorFrontendEndpointObject에 MinimumTlsVersion 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="852cd-625">Add MinimumTlsVersion parameter to Enable-AzFrontDoorCustomDomainHttps and New-AzFrontDoorFrontendEndpointObject</span></span>
* <span data-ttu-id="852cd-626">New-AzFrontDoorHealthProbeSettingObject에 HealthProbeMethod 및 EnabledState 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="852cd-626">Add HealthProbeMethod and EnabledState parameters to New-AzFrontDoorHealthProbeSettingObject</span></span>
* <span data-ttu-id="852cd-627">BackendPoolsSettings 개체를 생성하여 Front Door 생성/업데이트에 전달하는 새 cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="852cd-627">Add new cmdlet to create BackendPoolsSettings objec to pass into creation/update of Front Door</span></span>
    - <span data-ttu-id="852cd-628">New-AzFrontDoorBackendPoolsSettingObject</span><span class="sxs-lookup"><span data-stu-id="852cd-628">New-AzFrontDoorBackendPoolsSettingObject</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="852cd-629">Az.Network</span><span class="sxs-lookup"><span data-stu-id="852cd-629">Az.Network</span></span>
* <span data-ttu-id="852cd-630">'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' 및 'Start-AzVirtualnetworkGatewayPacketCapture.md' FilterData 옵션 예제를 변경합니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-630">Change 'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' and 'Start-AzVirtualnetworkGatewayPacketCapture.md' FilterData option examples.</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="852cd-631">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="852cd-631">Az.PrivateDns</span></span>
* <span data-ttu-id="852cd-632">PrivateDns .net sdk를 버전 1.0.0으로 업데이트함</span><span class="sxs-lookup"><span data-stu-id="852cd-632">Updated PrivateDns .net sdk to version 1.0.0</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="852cd-633">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="852cd-633">Az.RecoveryServices</span></span>
* <span data-ttu-id="852cd-634">보호를 사용하도록 설정할 때 디스크 유형을 선택하도록 Azure Site Recovery 지원</span><span class="sxs-lookup"><span data-stu-id="852cd-634">Azure Site Recovery support to select disk type at enabling protection.</span></span>
* <span data-ttu-id="852cd-635">복구 계획 동작 편집을 위한 Azure Site Recovery 버그 수정</span><span class="sxs-lookup"><span data-stu-id="852cd-635">Azure Site Recovery bug fix for recovery plan action edit.</span></span>
* <span data-ttu-id="852cd-636">파일 스트림 DB를 허용하도록 Azure Backup SQL 복원 지원</span><span class="sxs-lookup"><span data-stu-id="852cd-636">Azure Backup SQL Restore support to accept filestream DBs.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="852cd-637">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="852cd-637">Az.RedisCache</span></span>
* <span data-ttu-id="852cd-638">'New-AzRedisCache' 및 'Set-AzRedisCache' cmdlet에 'MinimumTlsVersion' 매개 변수가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-638">Added 'MinimumTlsVersion' parameter in 'New-AzRedisCache' and 'Set-AzRedisCache' cmdlets.</span></span> <span data-ttu-id="852cd-639">'Get-AzRedisCache' cmdlet 출력에 'MinimumTlsVersion'도 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-639">Also, added 'MinimumTlsVersion' in the output of 'Get-AzRedisCache' cmdlet.</span></span>
* <span data-ttu-id="852cd-640">'Set-AzRedisCache' 및 'New-AzRedisCache' cmdlet의 '-Size' 매개 변수에 대한 유효성 검사가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-640">Added validation on '-Size' parameter for 'Set-AzRedisCache' and 'New-AzRedisCache' cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="852cd-641">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="852cd-641">Az.Resources</span></span>
- <span data-ttu-id="852cd-642">정책 할당에 새로운 EnforcementMode 속성이 있는 새 api 버전 2019-06-01을 사용하도록 정책 cmdlet이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-642">Updated policy cmdlets to use new api version 2019-06-01 that has new EnforcementMode property in policy assignment.</span></span>
- <span data-ttu-id="852cd-643">정책 정의 만들기 도움말 예제가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-643">Updated create policy definition help example</span></span>
- <span data-ttu-id="852cd-644">Remove-AZADServicePrincipal -ServicePrincipalName 버그를 수정하고, 서비스 사용자 이름을 찾을 수 없으면 null 참조를 throw합니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-644">Fix bug Remove-AZADServicePrincipal -ServicePrincipalName, throw null reference when service principal name not found.</span></span>
- <span data-ttu-id="852cd-645">New-AZADServicePrincipal 버그를 수정하고, 테넌트에 구독이 없으면 null 참조를 throw합니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-645">Fix bug New-AZADServicePrincipal, throw null reference when tenant doesn't have any subscription.</span></span>
- <span data-ttu-id="852cd-646">연결된 애플리케이션에만 자격 증명을 추가하도록 New-AzAdServicePrincipal을 변경합니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-646">Change New-AzAdServicePrincipal to add credentials only to associated application.</span></span>

#### <a name="azsql"></a><span data-ttu-id="852cd-647">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="852cd-647">Az.Sql</span></span>
* <span data-ttu-id="852cd-648">데이터베이스 ReadReplicaCount에 대한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-648">Added support for database ReadReplicaCount.</span></span>
* <span data-ttu-id="852cd-649">영역 중복이 설정되지 않은 경우 Set-AzSqlDatabase가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-649">Fixed Set-AzSqlDatabase when zone redundancy not set</span></span>

## <a name="300---november-2019"></a><span data-ttu-id="852cd-650">3.0.0 - 2019년 11월</span><span class="sxs-lookup"><span data-stu-id="852cd-650">3.0.0 - November 2019</span></span>
### <a name="general"></a><span data-ttu-id="852cd-651">일반</span><span class="sxs-lookup"><span data-stu-id="852cd-651">General</span></span>
* <span data-ttu-id="852cd-652">Az.PrivateDns 1.0.0 릴리스</span><span class="sxs-lookup"><span data-stu-id="852cd-652">Az.PrivateDns 1.0.0 released</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="852cd-653">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="852cd-653">Az.Accounts</span></span>
* <span data-ttu-id="852cd-654">'Resolve-Error' 별칭에 사용 중단 메시지를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-654">Add a deprecation message for 'Resolve-Error' alias.</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="852cd-655">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="852cd-655">Az.Advisor</span></span>
* <span data-ttu-id="852cd-656">Get-AzAdvisorRecommendation cmdlet에 새로운 '운영 효율성' 범주가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-656">Added new category 'Operational Excellence' to Get-AzAdvisorRecommendation cmdlet.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="852cd-657">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="852cd-657">Az.Batch</span></span>
* <span data-ttu-id="852cd-658">`BatchAccountContext`의 `CoreQuota` 이름이 `DedicatedCoreQuota`로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-658">Renamed `CoreQuota` on `BatchAccountContext` to `DedicatedCoreQuota`.</span></span> <span data-ttu-id="852cd-659">또한 `LowPriorityCoreQuota`가 새로 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-659">There is also a new `LowPriorityCoreQuota`.</span></span>
  - <span data-ttu-id="852cd-660">이 변경 사항은 **Get-AzBatchAccount**에 영향을 줍니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-660">This impacts **Get-AzBatchAccount**.</span></span>
* <span data-ttu-id="852cd-661">이제 **New-AzBatchTask** `-ResourceFile` 매개 변수는 새로운 **New-AzBatchResourceFile** cmdlet을 사용하여 구성할 수 있는 `PSResourceFile` 개체의 컬렉션을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-661">**New-AzBatchTask** `-ResourceFile` parameter now takes a collection of `PSResourceFile` objects, which can be constructed using the new **New-AzBatchResourceFile** cmdlet.</span></span>
* <span data-ttu-id="852cd-662">새로운 **New-AzBatchResourceFile** cmdlet을 통해 `PSResourceFile` 개체를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-662">New **New-AzBatchResourceFile** cmdlet to help create `PSResourceFile` objects.</span></span> <span data-ttu-id="852cd-663">이들은 `-ResourceFile` 매개 변수의 **New-AzBatchTask**에 제공될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-663">These can be supplied to **New-AzBatchTask** on the `-ResourceFile` parameter.</span></span>
  - <span data-ttu-id="852cd-664">그에 따라 기존 `HttpUrl` 방법 외에도 두 가지 종류의 리소스 파일이 새롭게 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-664">This supports two new kinds of resource file in addition to the existing `HttpUrl` way:</span></span>
    - <span data-ttu-id="852cd-665">`AutoStorageContainerName` 기반 리소스 파일은 전체 자동 스토리지 컨테이너를 일괄 처리 노드에 다운로드합니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-665">`AutoStorageContainerName` based resource files download an entire auto-storage container to the Batch node.</span></span>
    - <span data-ttu-id="852cd-666">`StorageContainerUrl` 기반 리소스 파일은 URL에 지정된 컨테이너를 일괄 처리 노드에 다운로드합니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-666">`StorageContainerUrl` based resource files download the container specified in the URL to the Batch node.</span></span>
* <span data-ttu-id="852cd-667">**Get-AzBatchApplication**으로 반환되는 `PSApplication`의 `ApplicationPackages` 속성이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-667">Removed `ApplicationPackages` property of `PSApplication` returned by **Get-AzBatchApplication**.</span></span>
  - <span data-ttu-id="852cd-668">이제 **Get-AzBatchApplicationPackage**를 사용하여 애플리케이션 내부의 특정 패키지를 검색할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-668">The specific packages inside of an application now can be retrieved using **Get-AzBatchApplicationPackage**.</span></span> <span data-ttu-id="852cd-669">예: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`</span><span class="sxs-lookup"><span data-stu-id="852cd-669">For example: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span></span>
* <span data-ttu-id="852cd-670">**Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication** 및 **Set-AzBatchApplication**에서 `ApplicationId` 이름이 `ApplicationName`으로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-670">Renamed `ApplicationId` to `ApplicationName` on **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication**, and **Set-AzBatchApplication**.</span></span>
  - <span data-ttu-id="852cd-671">이제 `ApplicationId`는 `ApplicationName`의 별칭입니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-671">`ApplicationId` now is an alias of `ApplicationName`.</span></span>
* <span data-ttu-id="852cd-672">새로운 `PSWindowsUserConfiguration` 속성이 `PSUserAccount`에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-672">Added new `PSWindowsUserConfiguration` property to `PSUserAccount`.</span></span>
* <span data-ttu-id="852cd-673">`PSApplicationPackage`에서 `Version` 이름이 `Name`으로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-673">Renamed `Version` to `Name` on `PSApplicationPackage`.</span></span>
* <span data-ttu-id="852cd-674">`PSResourceFile`에서 `BlobSource` 이름이 `HttpUrl`으로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-674">Renamed `BlobSource` to `HttpUrl` on `PSResourceFile`.</span></span>
* <span data-ttu-id="852cd-675">`PSVirtualMachineConfiguration`에서 `OSDisk` 속성이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-675">Removed `OSDisk` property from `PSVirtualMachineConfiguration`.</span></span>
* <span data-ttu-id="852cd-676">**Set-AzBatchPoolOSVersion**이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-676">Removed **Set-AzBatchPoolOSVersion**.</span></span> <span data-ttu-id="852cd-677">이 작업은 더 이상 지원되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-677">This operation is no longer supported.</span></span>
* <span data-ttu-id="852cd-678">`PSCloudServiceConfiguration`에서 `TargetOSVersion`이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-678">Removed `TargetOSVersion` from `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="852cd-679">`PSCloudServiceConfiguration`에서 `CurrentOSVersion` 이름이 `OSVersion`으로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-679">Renamed `CurrentOSVersion` to `OSVersion` on `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="852cd-680">`PSPoolUsageMetrics`에서 `DataEgressGiB` 및 `DataIngressGiB`가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-680">Removed `DataEgressGiB` and `DataIngressGiB` from `PSPoolUsageMetrics`.</span></span>
* <span data-ttu-id="852cd-681">**Get-AzBatchNodeAgentSku**가 제거되고 **Get-AzBatchSupportedImage**로 대체되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-681">Removed **Get-AzBatchNodeAgentSku** and replaced it with  **Get-AzBatchSupportedImage**.</span></span>
  - <span data-ttu-id="852cd-682">**Get-AzBatchSupportedImage**가 **Get-AzBatchNodeAgentSku**와 동일한 데이터를 반환하지만 더 친숙한 형식이 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-682">**Get-AzBatchSupportedImage** returns the same data as **Get-AzBatchNodeAgentSku** but in a more friendly format.</span></span>
  - <span data-ttu-id="852cd-683">이제 확인되지 않은 이미지도 새롭게 반환됩니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-683">New non-verified images are also now returned.</span></span> <span data-ttu-id="852cd-684">각 이미지의 `Capabilities` 및 `BatchSupportEndOfLife`에 대한 추가 정보도 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-684">Additional information about `Capabilities` and `BatchSupportEndOfLife` for each image is also included.</span></span>
* <span data-ttu-id="852cd-685">**New-AzBatchPool**의 새로운 `MountConfiguration` 매개 변수를 통해 풀의 각 노드에서 원격 파일 시스템을 마운트할 수 있는 기능이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-685">Added ability to mount remote file-systems on each node of a pool via the new `MountConfiguration` parameter of **New-AzBatchPool**.</span></span>
* <span data-ttu-id="852cd-686">이제 트래픽의 소스 포트를 기준으로 풀에 대한 네트워크 액세스를 차단하는 네트워크 보안 규칙이 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-686">Now support network security rules blocking network access to a pool based on the source port of the traffic.</span></span> <span data-ttu-id="852cd-687">이 작업은 `PSNetworkSecurityGroupRule`에서 `SourcePortRanges` 속성을 통해 수행됩니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-687">This is done via the `SourcePortRanges` property on `PSNetworkSecurityGroupRule`.</span></span>
* <span data-ttu-id="852cd-688">컨테이너를 실행할 때 Batch는 이제 컨테이너 작업 디렉터리 또는 일괄 처리 태스크 작업 디렉터리에서 작업 실행을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-688">When running a container, Batch now supports executing the task in the container working directory or in the Batch task working directory.</span></span> <span data-ttu-id="852cd-689">이 작업은 `PSTaskContainerSettings`에서 `WorkingDirectory` 속성에 의해 제어됩니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-689">This is controlled by the `WorkingDirectory` property on `PSTaskContainerSettings`.</span></span>
* <span data-ttu-id="852cd-690">새로운 `PublicIPs` 속성을 통해 `PSNetworkConfiguration`에서 공용 IP의 컬렉션을 지정할 수 있는 기능이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-690">Added ability to specify a collection of public IPs on `PSNetworkConfiguration` via the new `PublicIPs` property.</span></span> <span data-ttu-id="852cd-691">그 결과 사용자 제공 IP 목록의 IP가 풀에 있는 노드에 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-691">This guarantees nodes in the Pool will have an IP from the list user provided IPs.</span></span>
* <span data-ttu-id="852cd-692">지정하지 않은 경우 이제 `PSSTartTask`에서 `WaitForSuccess`의 기본값은 `$True`입니다(이전에는 `$False`).</span><span class="sxs-lookup"><span data-stu-id="852cd-692">When not specified, the default value of `WaitForSuccess` on `PSSTartTask` is now `$True` (was `$False`).</span></span>
* <span data-ttu-id="852cd-693">지정하지 않은 경우 이제 `PSAutoUserSpecification`에서 `Scope`의 기본값은 `Pool`입니다(이전에는 Windows의 경우 `Task`, Linux의 경우에는 `Pool`).</span><span class="sxs-lookup"><span data-stu-id="852cd-693">When not specified, the default value of `Scope` on `PSAutoUserSpecification` is now `Pool` (was `Task` on Windows and `Pool` on Linux).</span></span>

#### <a name="azcdn"></a><span data-ttu-id="852cd-694">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="852cd-694">Az.Cdn</span></span>
* <span data-ttu-id="852cd-695">RulesEngine에 UrlRewriteAction 및 CacheKeyQueryStringAction이 도입되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-695">Introduced UrlRewriteAction and CacheKeyQueryStringAction to RulesEngine.</span></span>
* <span data-ttu-id="852cd-696">New-AzDeliveryRuleCondition cmdlet에서 'Selector' 입력 누락과 같은 여러 버그가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-696">Fixed several bugs like missing 'Selector' Input in New-AzDeliveryRuleCondition cmdlet.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="852cd-697">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="852cd-697">Az.Compute</span></span>
* <span data-ttu-id="852cd-698">디스크 암호화 집합 기능</span><span class="sxs-lookup"><span data-stu-id="852cd-698">Disk Encryption Set feature</span></span>
    - <span data-ttu-id="852cd-699">새 cmdlet:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="852cd-699">New cmdlets:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span></span>
    - <span data-ttu-id="852cd-700">DiskEncryptionSetId 매개 변수가 다음 cmdlet에 추가되었습니다.   Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="852cd-700">DiskEncryptionSetId parameter is added to the following cmdlets:   Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span></span>
    - <span data-ttu-id="852cd-701">DiskEncryptionSetId 및 EncryptionType 매개 변수가 다음 cmdlet에 추가되었습니다.   New-AzDiskConfig   New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="852cd-701">DiskEncryptionSetId and EncryptionType parameters are added to the following cmdlets:   New-AzDiskConfig   New-AzSnapshotConfig</span></span>
* <span data-ttu-id="852cd-702">New-AzVmssIPConfig에 PublicIPAddressVersion 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="852cd-702">Add PublicIPAddressVersion parameter to New-AzVmssIPConfig</span></span>
* <span data-ttu-id="852cd-703">사용자 지정 스크립트 확장의 FileUris를 공용 설정에서 보호된 설정으로 이동</span><span class="sxs-lookup"><span data-stu-id="852cd-703">Move FileUris of custom script extension from public setting to protected setting</span></span>
* <span data-ttu-id="852cd-704">New-AzVmss, New-AzVmssConfig 및 Update-AzVmss cmdlet에 ScaleInPolicy 추가</span><span class="sxs-lookup"><span data-stu-id="852cd-704">Add ScaleInPolicy to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>
* <span data-ttu-id="852cd-705">주요 변경 내용</span><span class="sxs-lookup"><span data-stu-id="852cd-705">Breaking changes</span></span>
    - <span data-ttu-id="852cd-706">CreateOption이 업로드일 때 UploadSizeInBytes 매개 변수가 New-AzDiskConfig에 대해 DiskSizeGB 대신 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-706">UploadSizeInBytes parameter is used instead of DiskSizeGB for New-AzDiskConfig when CreateOption is Upload</span></span>
    - <span data-ttu-id="852cd-707">GalleryImageVersion 개체에서 PublishingProfile.Source.ManagedImage.Id가 StorageProfile.Source.Id로 바뀝니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-707">PublishingProfile.Source.ManagedImage.Id is replaced with StorageProfile.Source.Id in GalleryImageVersion object</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="852cd-708">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="852cd-708">Az.DataFactory</span></span>
* <span data-ttu-id="852cd-709">ADF .Net SDK 버전을 4.3.0으로 업데이트</span><span class="sxs-lookup"><span data-stu-id="852cd-709">Update ADF .Net SDK version to 4.3.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="852cd-710">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="852cd-710">Az.DataLakeStore</span></span>
* <span data-ttu-id="852cd-711">ADLS SDK 버전 업데이트(https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha) , 다음 수정 사항 제공</span><span class="sxs-lookup"><span data-stu-id="852cd-711">Update ADLS SDK version (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), brings following fixes</span></span>
* <span data-ttu-id="852cd-712">휴지통 또는 디렉터리 항목의 creationtime을 역직렬화할 수 없을 때 예외가 발생하지 않도록 방지합니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-712">Avoid throwing exception while unable to deserialize the creationtime of the trash or directory entry.</span></span>
* <span data-ttu-id="852cd-713">adlsclient에서 요청별 시간 제한 설정 노출</span><span class="sxs-lookup"><span data-stu-id="852cd-713">Expose setting per request timeout in adlsclient</span></span>
* <span data-ttu-id="852cd-714">badoffset 복구를 위한 원본 syncflag 전달 수정</span><span class="sxs-lookup"><span data-stu-id="852cd-714">Fix passing the original syncflag for badoffset recovery</span></span>
* <span data-ttu-id="852cd-715">응답이 확인된 후 연속 토큰을 검색하기 위한 EnumerateDirectory 수정</span><span class="sxs-lookup"><span data-stu-id="852cd-715">Fix EnumerateDirectory to retrieve continuation token once response is checked</span></span>
* <span data-ttu-id="852cd-716">Concat 버그 수정</span><span class="sxs-lookup"><span data-stu-id="852cd-716">Fix Concat Bug</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="852cd-717">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="852cd-717">Az.FrontDoor</span></span>
* <span data-ttu-id="852cd-718">모듈 간 기타 오타가 수정됨</span><span class="sxs-lookup"><span data-stu-id="852cd-718">Fixed miscellaneous typos across module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="852cd-719">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="852cd-719">Az.HDInsight</span></span>
* <span data-ttu-id="852cd-720">ADLSGen1 스토리지가 포함된 클러스터를 가져오기 위해 Get-AzHDInsightCluster를 사용할 때 고객에게 '올바른 Base-64 문자열이 아닙니다' 오류가 표시되는 버그가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-720">Fixed the bug that customer will get 'Not a valid Base-64 string' error when using Get-AzHDInsightCluster to get the cluster with ADLSGen1 storage.</span></span>
* <span data-ttu-id="852cd-721">고객이 Azure Data Lake에 액세스하기 위해 서비스 주체 애플리케이션 ID를 제공할 수 있도록 세 가지 cmdlet Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig 및 New-AzHDInsightCluster에 이름이 'ApplicationId'인 매개 변수를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-721">Add a parameter named 'ApplicationId' to three cmdlets Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig and New-AzHDInsightCluster so that customer can provide the service principal application id for accessing Azure Data Lake.</span></span>
* <span data-ttu-id="852cd-722">Microsoft.Azure.Management.HDInsight가 2.1.0에서 5.1.0으로 변경됨</span><span class="sxs-lookup"><span data-stu-id="852cd-722">Changed Microsoft.Azure.Management.HDInsight from 2.1.0 to 5.1.0</span></span>
* <span data-ttu-id="852cd-723">다음 5가지 cmdlet이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-723">Removed five cmdlets:</span></span>
    - <span data-ttu-id="852cd-724">Get-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="852cd-724">Get-AzHDInsightOMS</span></span>
    - <span data-ttu-id="852cd-725">Enable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="852cd-725">Enable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="852cd-726">Disable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="852cd-726">Disable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="852cd-727">Grant-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="852cd-727">Grant-AzHDInsightRdpServicesAccess</span></span>
    - <span data-ttu-id="852cd-728">Revoke-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="852cd-728">Revoke-AzHDInsightRdpServicesAccess</span></span>
* <span data-ttu-id="852cd-729">다음 3가지 cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-729">Added three cmdlets:</span></span>
    - <span data-ttu-id="852cd-730">Get-AzHDInsightOMS 대신 Get-AzHDInsightMonitoring</span><span class="sxs-lookup"><span data-stu-id="852cd-730">Get-AzHDInsightMonitoring to replace Get-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="852cd-731">Get-AzHDInsightOMS 대신 Get-AzHDInsightMonitoring</span><span class="sxs-lookup"><span data-stu-id="852cd-731">Enable-AzHDInsightMonitoring to replace Enable-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="852cd-732">Disable-AzHDInsightOMS 대신 Disable-AzHDInsightMonitoring</span><span class="sxs-lookup"><span data-stu-id="852cd-732">Disable-AzHDInsightMonitoring to replace Disable-AzHDInsightOMS.</span></span>
* <span data-ttu-id="852cd-733">특정 위치의 기능 정보 가져오기를 지원하도록 cmdlet Get-AzHDInsightProperties가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-733">Fixed cmdlet Get-AzHDInsightProperties to support get capabilities information from a specific location.</span></span>
* <span data-ttu-id="852cd-734">Add-AzHDInsightConfigValue에서 매개 변수 집합('Spark1', 'Spark2')이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-734">Removed parameter sets('Spark1', 'Spark2') from Add-AzHDInsightConfigValue.</span></span>
* <span data-ttu-id="852cd-735">cmdlet Add-AzHDInsightSecurityProfile의 도움말 문서에 예제를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-735">Add examples to the help documents of cmdlet Add-AzHDInsightSecurityProfile.</span></span>
* <span data-ttu-id="852cd-736">다음 cmdlet의 출력 유형이 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-736">Changed output type of the following cmdlets:</span></span>
*  - <span data-ttu-id="852cd-737">Get-AzHDInsightProperties의 출력 유형이 CapabilitiesResponse에서 AzureHDInsightCapabilities로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-737">Changed the output type of Get-AzHDInsightProperties from  CapabilitiesResponse to AzureHDInsightCapabilities.</span></span>
*  - <span data-ttu-id="852cd-738">Remove-AzHDInsightCluster의 출력 유형이 ClusterGetResponse에서 bool로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-738">Changed the output type of Remove-AzHDInsightCluster from ClusterGetResponse to bool.</span></span>
*  - <span data-ttu-id="852cd-739">Set-AzHDInsightGatewaySettings의 출력 유형이 HttpConnectivitySettings에서 GatewaySettings로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-739">Changed the output type of Set-AzHDInsightGatewaySettings HttpConnectivitySettings to GatewaySettings.</span></span>
* <span data-ttu-id="852cd-740">몇 가지 시나리오 테스트 사례가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-740">Added some scenario test cases.</span></span>
* <span data-ttu-id="852cd-741">일부 별칭 제거: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span><span class="sxs-lookup"><span data-stu-id="852cd-741">Remove some alias: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="852cd-742">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="852cd-742">Az.IotHub</span></span>
* <span data-ttu-id="852cd-743">주요 변경 내용:</span><span class="sxs-lookup"><span data-stu-id="852cd-743">Breaking changes:</span></span>
    - <span data-ttu-id="852cd-744">'Add-AzIotHubEventHubConsumerGroup' cmdlet이 'EventHubEndpointName' 매개 변수를 더 이상 지원하지 않으며 원래 매개 변수 이름에 대해 별칭을 찾을 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-744">The cmdlet 'Add-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="852cd-745">'Add-AzIotHubEventHubConsumerGroup' cmdlet에 대한 매개 변수 집합 '__AllParameterSets'가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-745">The parameter set '__AllParameterSets' for cmdlet 'Add-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="852cd-746">'Get-AzIotHubEventHubConsumerGroup' cmdlet이 'EventHubEndpointName' 매개 변수를 더 이상 지원하지 않으며 원래 매개 변수 이름에 대해 별칭을 찾을 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-746">The cmdlet 'Get-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="852cd-747">'Get-AzIotHubEventHubConsumerGroup' cmdlet에 대한 매개 변수 집합 '__AllParameterSets'가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-747">The parameter set '__AllParameterSets' for cmdlet 'Get-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="852cd-748">'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' 유형의 'OperationsMonitoringProperties' 속성이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-748">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' has been removed.</span></span>
    - <span data-ttu-id="852cd-749">'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' 유형의 'OperationsMonitoringProperties' 속성이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-749">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' has been removed.</span></span>
    - <span data-ttu-id="852cd-750">'New-AzIotHubExportDevice' cmdlet이 더 이상 'New-AzIotHubExportDevices' 별칭을 지원하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-750">The cmdlet 'New-AzIotHubExportDevice' no longer supports the alias 'New-AzIotHubExportDevices'.</span></span>
    - <span data-ttu-id="852cd-751">'New-AzIotHubImportDevice' cmdlet이 더 이상 'New-AzIotHubImportDevices' 별칭을 지원하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-751">The cmdlet 'New-AzIotHubImportDevice' no longer supports the alias 'New-AzIotHubImportDevices'.</span></span>
    - <span data-ttu-id="852cd-752">'Remove-AzIotHubEventHubConsumerGroup' cmdlet이 'EventHubEndpointName' 매개 변수를 더 이상 지원하지 않으며 원래 매개 변수 이름에 대해 별칭을 찾을 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-752">The cmdlet 'Remove-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="852cd-753">'Remove-AzIotHubEventHubConsumerGroup' cmdlet에 대한 매개 변수 집합 '__AllParameterSets'가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-753">The parameter set '__AllParameterSets' for cmdlet 'Remove-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="852cd-754">'Set-AzIotHub' cmdlet이 'OperationsMonitoringProperties' 매개 변수를 더 이상 지원하지 않으며 원래 매개 변수 이름에 대해 별칭을 찾을 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-754">The cmdlet 'Set-AzIotHub' no longer supports the parameter 'OperationsMonitoringProperties' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="852cd-755">'Set-AzIotHub' cmdlet에 대한 매개 변수 집합 'UpdateOperationsMonitoringProperties'가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-755">The parameter set 'UpdateOperationsMonitoringProperties' for cmdlet 'Set-AzIotHub' has been removed.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="852cd-756">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="852cd-756">Az.RecoveryServices</span></span>
* <span data-ttu-id="852cd-757">Azure Site Recovery가 Azure-Azure를 위한 NSG, 공용 IP 및 내부 부하 분산 장치와 같은 네트워킹 리소스 구성을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-757">Azure Site Recovery support to configure networking resources like NSG, public IP and internal load balancers for Azure to Azure.</span></span>
* <span data-ttu-id="852cd-758">Azure Site Recovery가 vMWare-Azure를 위한 관리 디스크에 쓰기를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-758">Azure Site Recovery Support to write to managed disk for vMWare to Azure.</span></span>
* <span data-ttu-id="852cd-759">Azure Site Recovery가 vMWare-Azure를 위한 NIC 감소를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-759">Azure Site Recovery Support to NIC reduction for vMWare to Azure.</span></span>
* <span data-ttu-id="852cd-760">Azure Site Recovery가 Azure-Azure를 위한 가속 네트워킹을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-760">Azure Site Recovery Support to accelerated networking for Azure to Azure.</span></span>
* <span data-ttu-id="852cd-761">Azure Site Recovery가 Azure-Azure를 위한 에이전트 자동 업데이트를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-761">Azure Site Recovery Support to agent auto update for Azure to Azure.</span></span>
* <span data-ttu-id="852cd-762">Azure Site Recovery가 Azure-Azure를 위한 표준 SSD를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-762">Azure Site Recovery Support to Standard SSD for Azure to Azure.</span></span>
* <span data-ttu-id="852cd-763">Azure Site Recovery가 Azure-Azure를 위한 두 가지 Azure 디스크 암호화 전달을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-763">Azure Site Recovery Support to Azure Disk Encryption two pass for Azure to Azure.</span></span>
* <span data-ttu-id="852cd-764">Azure Site Recovery가 Azure-Azure를 위한 새로 추가된 디스크 보호를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-764">Azure Site Recovery Support to protect newly added disk for Azure to Azure.</span></span>
* <span data-ttu-id="852cd-765">VM을 위한 SoftDelete 기능 및 softdelete를 위한 테스트가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-765">Added SoftDelete feature for VM and added tests for softdelete</span></span>

#### <a name="azresources"></a><span data-ttu-id="852cd-766">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="852cd-766">Az.Resources</span></span>
* <span data-ttu-id="852cd-767">종속성 어셈블리 Microsoft.Extensions.Caching.Memory가 1.1.1에서 2.2로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-767">Update dependency assembly Microsoft.Extensions.Caching.Memory from 1.1.1 to 2.2</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="852cd-768">Az.Network</span><span class="sxs-lookup"><span data-stu-id="852cd-768">Az.Network</span></span>
* <span data-ttu-id="852cd-769">일반 서비스 공급자 지원을 위해 PrivateEndpointConnection에 대한 모든 cmdlet이 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-769">Change all cmdlets for PrivateEndpointConnection to support generic service provider.</span></span>
    - <span data-ttu-id="852cd-770">업데이트된 cmdlet:</span><span class="sxs-lookup"><span data-stu-id="852cd-770">Updated cmdlet:</span></span>
        - <span data-ttu-id="852cd-771">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="852cd-771">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="852cd-772">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="852cd-772">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="852cd-773">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="852cd-773">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="852cd-774">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="852cd-774">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="852cd-775">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="852cd-775">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="852cd-776">PrivateLinkResource에 대한 새 cmdlet이 추가되었고 일반 서비스 공급자도 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-776">Add new cmdlet for PrivateLinkResource and it also support generic service provider.</span></span>
    - <span data-ttu-id="852cd-777">새 cmdlet:</span><span class="sxs-lookup"><span data-stu-id="852cd-777">New cmdlet:</span></span>
        - <span data-ttu-id="852cd-778">Get-AzPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="852cd-778">Get-AzPrivateLinkResource</span></span>
* <span data-ttu-id="852cd-779">Proxy Protocol V2 기능에 대한 새 필드 및 매개 변수가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-779">Add new fields and parameter for the feature Proxy Protocol V2.</span></span>
    - <span data-ttu-id="852cd-780">PrivateLinkService에서 EnableProxyProtocol 속성 추가</span><span class="sxs-lookup"><span data-stu-id="852cd-780">Add property EnableProxyProtocol in PrivateLinkService</span></span>
    - <span data-ttu-id="852cd-781">PrivateEndpointConnection에서 LinkIdentifier 속성 추가</span><span class="sxs-lookup"><span data-stu-id="852cd-781">Add property LinkIdentifier in PrivateEndpointConnection</span></span>
    - <span data-ttu-id="852cd-782">새로운 선택적인 매개 변수인 EnableProxyProtocol을 추가하도록 New-AzPrivateLinkService가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-782">Updated New-AzPrivateLinkService to add a new optional parameter EnableProxyProtocol.</span></span>
* <span data-ttu-id="852cd-783">'New-AzApplicationGatewaySku' 참조 설명서의 잘못된 매개 변수 설명 수정</span><span class="sxs-lookup"><span data-stu-id="852cd-783">Fix incorrect parameter description in 'New-AzApplicationGatewaySku' reference documentation</span></span>
* <span data-ttu-id="852cd-784">Azure 방화벽 정책을 지원하는 새로운 cmdlet</span><span class="sxs-lookup"><span data-stu-id="852cd-784">New cmdlets to support the azure firewall policy</span></span>
* <span data-ttu-id="852cd-785">VirtualHub의 자식 리소스 RouteTables에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="852cd-785">Add support for child resource RouteTables of VirtualHub</span></span>
    - <span data-ttu-id="852cd-786">추가된 새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-786">New cmdlets added:</span></span>
        - <span data-ttu-id="852cd-787">Add-AzVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="852cd-787">Add-AzVirtualHubRoute</span></span>
        - <span data-ttu-id="852cd-788">Add-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="852cd-788">Add-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="852cd-789">Get-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="852cd-789">Get-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="852cd-790">Remove-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="852cd-790">Remove-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="852cd-791">Set-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="852cd-791">Set-AzVirtualHub</span></span>
* <span data-ttu-id="852cd-792">VirtualHub의 새로운 속성 Sku 및 VirtualWan의 VirtualWANType에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="852cd-792">Add support for new properties Sku of VirtualHub and VirtualWANType of VirtualWan</span></span>
    - <span data-ttu-id="852cd-793">선택적 매개 변수로 다음 cmdlet이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-793">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="852cd-794">New-AzVirtualHub: 추가된 매개 변수 Sku</span><span class="sxs-lookup"><span data-stu-id="852cd-794">New-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="852cd-795">Update-AzVirtualHub: 추가된 매개 변수 Sku</span><span class="sxs-lookup"><span data-stu-id="852cd-795">Update-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="852cd-796">New-AzVirtualWan: 추가된 매개 변수 VirtualWANType</span><span class="sxs-lookup"><span data-stu-id="852cd-796">New-AzVirtualWan : added parameter VirtualWANType</span></span>
        - <span data-ttu-id="852cd-797">Update-AzVirtualWan: 추가된 매개 변수 VirtualWANType</span><span class="sxs-lookup"><span data-stu-id="852cd-797">Update-AzVirtualWan : added parameter VirtualWANType</span></span>
* <span data-ttu-id="852cd-798">HubVnetConnection, VpnConnection 및 ExpressRouteConnection에 대한 EnableInternetSecurity 속성 지원 추가</span><span class="sxs-lookup"><span data-stu-id="852cd-798">Add support for EnableInternetSecurity property for HubVnetConnection, VpnConnection and ExpressRouteConnection</span></span>
    - <span data-ttu-id="852cd-799">추가된 새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-799">New cmdlets added:</span></span>
        - <span data-ttu-id="852cd-800">Update-AzureRmVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="852cd-800">Update-AzureRmVirtualHubVnetConnection</span></span>
    - <span data-ttu-id="852cd-801">선택적 매개 변수로 다음 cmdlet이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-801">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="852cd-802">New-AzureRmVirtualHubVnetConnection: 추가된 매개 변수 EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="852cd-802">New-AzureRmVirtualHubVnetConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="852cd-803">New-AzureRmVpnConnection: 추가된 매개 변수 EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="852cd-803">New-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="852cd-804">Update-AzureRmVpnConnection: 추가된 매개 변수 EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="852cd-804">Update-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="852cd-805">New-AzureRmExpressRouteConnection: 추가된 매개 변수 EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="852cd-805">New-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="852cd-806">Set-AzureRmExpressRouteConnection: 추가된 매개 변수 EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="852cd-806">Set-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
* <span data-ttu-id="852cd-807">TopLevel WebApplicationFirewall 정책 구성을 위한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="852cd-807">Add support for Configuring TopLevel WebApplicationFirewall Policy</span></span>
    - <span data-ttu-id="852cd-808">추가된 새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-808">New cmdlets added:</span></span>
        - <span data-ttu-id="852cd-809">New-AzApplicationGatewayFirewallPolicySetting</span><span class="sxs-lookup"><span data-stu-id="852cd-809">New-AzApplicationGatewayFirewallPolicySetting</span></span>
        - <span data-ttu-id="852cd-810">New-AzApplicationGatewayFirewallPolicyExclusion</span><span class="sxs-lookup"><span data-stu-id="852cd-810">New-AzApplicationGatewayFirewallPolicyExclusion</span></span>
        - <span data-ttu-id="852cd-811">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="852cd-811">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span></span>
        - <span data-ttu-id="852cd-812">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="852cd-812">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span></span>
        - <span data-ttu-id="852cd-813">New-AzApplicationGatewayFirewallPolicyManagedRule</span><span class="sxs-lookup"><span data-stu-id="852cd-813">New-AzApplicationGatewayFirewallPolicyManagedRule</span></span>
        - <span data-ttu-id="852cd-814">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="852cd-814">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span></span>
    - <span data-ttu-id="852cd-815">선택적 매개 변수로 다음 cmdlet이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-815">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="852cd-816">New-AzApplicationGatewayFirewallPolicy: 추가된 매개 변수 PolicySetting, ManagedRule</span><span class="sxs-lookup"><span data-stu-id="852cd-816">New-AzApplicationGatewayFirewallPolicy : added parameter PolicySetting, ManagedRule</span></span>
* <span data-ttu-id="852cd-817">CustomRule에서 Geo-Match 연산자를 위한 지원 추가됨</span><span class="sxs-lookup"><span data-stu-id="852cd-817">Added support for Geo-Match operator on CustomRule</span></span>
    - <span data-ttu-id="852cd-818">FirewallCondition에서 연산자에 GeoMatch 추가됨</span><span class="sxs-lookup"><span data-stu-id="852cd-818">Added GeoMatch to the operator on the FirewallCondition</span></span>
* <span data-ttu-id="852cd-819">perListener 및 perSite 방화벽 규칙에 대한 지원 추가됨</span><span class="sxs-lookup"><span data-stu-id="852cd-819">Added support for perListener and perSite Firewall policy</span></span>
    - <span data-ttu-id="852cd-820">선택적 매개 변수로 다음 cmdlet이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-820">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="852cd-821">New-AzApplicationGatewayHttpListener: 추가된 매개 변수 FirewallPolicy, FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="852cd-821">New-AzApplicationGatewayHttpListener : added parameter FirewallPolicy, FirewallPolicyId</span></span>
        - <span data-ttu-id="852cd-822">New-AzApplicationGatewayPathRuleConfig: 추가된 매개 변수 FirewallPolicy, FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="852cd-822">New-AzApplicationGatewayPathRuleConfig : added parameter FirewallPolicy, FirewallPolicyId</span></span>
* <span data-ttu-id="852cd-823">'PSBastion'에서 이름이 AzureBastionSubnet인 필수 서브넷의 수정은 대소문자를 구분하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-823">Fix required subnet with name AzureBastionSubnet in 'PSBastion' can be case insensitive</span></span>
* <span data-ttu-id="852cd-824">Azure Firewall을 위한 네트워크 규칙의 대상 FQDN 및 NAT 규칙의 번역된 FQDN 지원</span><span class="sxs-lookup"><span data-stu-id="852cd-824">Support for Destination FQDNs in Network Rules and Translated FQDN in NAT Rules for Azure Firewall</span></span>
* <span data-ttu-id="852cd-825">IpGroup의 최상위 리소스 RouteTables에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="852cd-825">Add support for top level resource RouteTables of IpGroup</span></span>
    - <span data-ttu-id="852cd-826">추가된 새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-826">New cmdlets added:</span></span>
        - <span data-ttu-id="852cd-827">New-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="852cd-827">New-AzIpGroup</span></span>
        - <span data-ttu-id="852cd-828">Remove-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="852cd-828">Remove-AzIpGroup</span></span>
        - <span data-ttu-id="852cd-829">Get-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="852cd-829">Get-AzIpGroup</span></span>
        - <span data-ttu-id="852cd-830">Set-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="852cd-830">Set-AzIpGroup</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="852cd-831">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="852cd-831">Az.ServiceFabric</span></span>
* <span data-ttu-id="852cd-832">Add-AzVmssSecret에서 지원되기 때문에 Add-AzServiceFabricApplicationCertificate cmdlet이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-832">Remove Add-AzServiceFabricApplicationCertificate cmdlet as this scenario is covered by Add-AzVmssSecret.</span></span>

#### <a name="azsql"></a><span data-ttu-id="852cd-833">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="852cd-833">Az.Sql</span></span>
* <span data-ttu-id="852cd-834">Managed Instances에서 삭제된 데이터베이스의 복원을 위한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-834">Added support for restore of dropped databases on Managed Instances.</span></span>
* <span data-ttu-id="852cd-835">이전의 감사 cmdlet 코드가 사용되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-835">Deprecated from code old auditing cmdlets.</span></span>
* <span data-ttu-id="852cd-836">사용되지 않는 별칭이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-836">Removed deprecated aliases:</span></span>
* <span data-ttu-id="852cd-837">Get-AzSqlDatabaseIndexRecommendations(대신 Get-AzSqlDatabaseIndexRecommendation 사용)</span><span class="sxs-lookup"><span data-stu-id="852cd-837">Get-AzSqlDatabaseIndexRecommendations (use Get-AzSqlDatabaseIndexRecommendation instead)</span></span>
* <span data-ttu-id="852cd-838">Get-AzSqlDatabaseRestorePoints(대신 Get-AzSqlDatabaseRestorePoint 사용)</span><span class="sxs-lookup"><span data-stu-id="852cd-838">Get-AzSqlDatabaseRestorePoints (use Get-AzSqlDatabaseRestorePoint instead)</span></span>
* <span data-ttu-id="852cd-839">Get-AzSqlDatabaseSecureConnectionPolicy cmdlet 제거</span><span class="sxs-lookup"><span data-stu-id="852cd-839">Remove Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="852cd-840">사용되지 않는 취약성 평가 설정 cmdlet에 대한 별칭 제거</span><span class="sxs-lookup"><span data-stu-id="852cd-840">Remove aliases for deprecated Vulnerability Assessment Settings cmdlets</span></span>
* <span data-ttu-id="852cd-841">지능형 위협 탐지 설정 cmdlet 사용 중단</span><span class="sxs-lookup"><span data-stu-id="852cd-841">Deprecate Advanced Threat Detection Settings cmdlets</span></span>
* <span data-ttu-id="852cd-842">데이터베이스의 열에 대한 민감도 권장 사항의 사용 여부를 제어하는 cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-842">Adding cmdlets to Disable and enable sensitivity recommendations on columns in a database.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="852cd-843">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="852cd-843">Az.Storage</span></span>
* <span data-ttu-id="852cd-844">스토리지 계정을 만들거나 업데이트할 때 큰 파일 공유 사용 지원</span><span class="sxs-lookup"><span data-stu-id="852cd-844">Support enable Large File share when create or update Storage account</span></span>
    -  <span data-ttu-id="852cd-845">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="852cd-845">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="852cd-846">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="852cd-846">Set-AzStorageAccount</span></span>
* <span data-ttu-id="852cd-847">파일 핸들을 닫거나/가져올 때, DeletePending 상태의 개체로 인한 오류를 방지하기 위해 입력 경로가 파일 디렉터리인지 또는 파일인지를 확인하는 과정을 건너뜁니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-847">When close/get File handle, skip check the input path is File directory or File, to avoid failure with object in DeletePending status</span></span>
    -  <span data-ttu-id="852cd-848">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="852cd-848">Get-AzStorageFileHandle</span></span>
    -  <span data-ttu-id="852cd-849">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="852cd-849">Close-AzStorageFileHandle</span></span>

## <a name="280---october-2019"></a><span data-ttu-id="852cd-850">2.8.0 - 2019년 10월</span><span class="sxs-lookup"><span data-stu-id="852cd-850">2.8.0 - October 2019</span></span>
### <a name="general"></a><span data-ttu-id="852cd-851">일반</span><span class="sxs-lookup"><span data-stu-id="852cd-851">General</span></span>
* <span data-ttu-id="852cd-852">Az.HealthcareApis 1.0.0 릴리스</span><span class="sxs-lookup"><span data-stu-id="852cd-852">Az.HealthcareApis 1.0.0 release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="852cd-853">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="852cd-853">Az.Accounts</span></span>
* <span data-ttu-id="852cd-854">생성된 모듈에 대한 원격 분석 및 URL 다시 작성이 업데이트되고, Windows 단위 테스트가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-854">Update telemetry and url rewriting for generated modules, fix windows unit tests.</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="852cd-855">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="852cd-855">Az.ApiManagement</span></span>
* <span data-ttu-id="852cd-856">**Set-AzApiManagementApi** - API 업데이트 지원이 ApiVersionSet에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-856">**Set-AzApiManagementApi** - Added support for Updating Api into ApiVersionSet</span></span>
    - <span data-ttu-id="852cd-857">문제 https://github.com/Azure/azure-powershell/issues/10068 수정</span><span class="sxs-lookup"><span data-stu-id="852cd-857">Fix for issue https://github.com/Azure/azure-powershell/issues/10068</span></span>

#### <a name="azautomation"></a><span data-ttu-id="852cd-858">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="852cd-858">Az.Automation</span></span>
* <span data-ttu-id="852cd-859">Linux 다시 부팅 설정 매개 변수에 대한 New-AzureAutomationSoftwareUpdateConfiguration cmdlet이 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-859">Fixed New-AzureAutomationSoftwareUpdateConfiguration cmdlet for Linux reboot setting parameter.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="852cd-860">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="852cd-860">Az.Batch</span></span>
* <span data-ttu-id="852cd-861">**Get-AzBatchNodeAgentSku**가 더 이상 사용되지 않으며, 2.0.0 버전의 **Get-AzBatchSupportImage**로 대체되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-861">**Get-AzBatchNodeAgentSku** is deprecated and will be replaced by **Get-AzBatchSupportImage** in version 2.0.0.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="852cd-862">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="852cd-862">Az.Compute</span></span>
* <span data-ttu-id="852cd-863">Priority, EvictionPolicy 및 MaxPrice 매개 변수가 New-AzVM 및 New-AzVmss cmdlet에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-863">Add Priority, EvictionPolicy, and MaxPrice parameters to New-AzVM and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="852cd-864">Add-AzVMAdditionalUnattendContent 및 Add-AzVMSshPublicKey cmdlet에 대한 경고 메시지와 도움말 문서가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-864">Fix warning message and help document for Add-AzVMAdditionalUnattendContent and Add-AzVMSshPublicKey cmdlets</span></span>
* <span data-ttu-id="852cd-865">Set-AzVMDiskEncryptionExtension의 관리 디스크가 있는 Linux VM에 대한 -skipVmBackup 예외가 해결되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-865">Fix -skipVmBackup exception for Linux VMs with managed disks for Set-AzVMDiskEncryptionExtension.</span></span>
* <span data-ttu-id="852cd-866">Set-AzVMDiskEncryptionExtension의 두 가지 패스 시나리오에서 발생하는 암호화 설정 업데이트의 버그가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-866">Fix bug in update encryption settings in Set-AzVMDiskEncryptionExtension, two pass scenario.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="852cd-867">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="852cd-867">Az.DataFactory</span></span>
* <span data-ttu-id="852cd-868">ADF V2 데이터 흐름에 대한 CRUD 명령으로 Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow 및 Get-AzDataFactoryV2DataFlow가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-868">Adding CRUD commands for ADF V2 data flow: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow, and Get-AzDataFactoryV2DataFlow.</span></span>
* <span data-ttu-id="852cd-869">ADF V2 데이터 흐름 디버그 세션에 대한 작업 명령으로 Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand 및 Stop-AzDataFactoryV2DataFlowDebugSession이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-869">Adding action commands for ADF V2 data flow debug Session: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand and Stop-AzDataFactoryV2DataFlowDebugSession.</span></span>
* <span data-ttu-id="852cd-870">ADF .Net SDK 버전이 4.2.0으로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-870">Update ADF .Net SDK version to 4.2.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="852cd-871">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="852cd-871">Az.DataLakeStore</span></span>
* <span data-ttu-id="852cd-872">도메인 없이 '-'가 있는 계정을 전달할 수 있도록 계정 유효성 검사가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-872">Fix account validation so that accounts with '-' can be passed without domain</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="852cd-873">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="852cd-873">Az.HealthcareApis</span></span>
* <span data-ttu-id="852cd-874">PowerShell 버전이 1.0.0으로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-874">Updated the powershell version to 1.0.0</span></span>
* <span data-ttu-id="852cd-875">SDK 버전이 1.0.2로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-875">Updated the SDK version to 1.0.2</span></span>
* <span data-ttu-id="852cd-876">새 SDK 버전을 참조하도록 테스트가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-876">Update in tests to refer to new SDK version</span></span>
* <span data-ttu-id="852cd-877">출력이 중첩 구조에서 평면화 구조로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-877">Updated the output structure from nested to flattened.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="852cd-878">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="852cd-878">Az.IotHub</span></span>
* <span data-ttu-id="852cd-879">새 라우팅 원본 추가: DigitalTwinChangeEvents</span><span class="sxs-lookup"><span data-stu-id="852cd-879">Add new routing source: DigitalTwinChangeEvents</span></span>
* <span data-ttu-id="852cd-880">사소한 버그 수정: Get-AzIothub에서 subscriptionId를 반환하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-880">Minor bug fix: Get-AzIothub not returning subscriptionId</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="852cd-881">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="852cd-881">Az.Monitor</span></span>
* <span data-ttu-id="852cd-882">작업 그룹에 대한 새 작업 그룹 수신기로 -ItsmReceiver, -VoiceReceiver, -ArmRoleReceiver, -AzureFunctionReceiver, -LogicAppReceiver, -AutomationRunbookReceiver, -AzureAppPushReceiver가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-882">New action group receivers added for action group   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span></span>
* <span data-ttu-id="852cd-883">수신기에 사용하도록 설정된 일반 경고 스키마가 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-883">Use common alert schema enabled for the receivers.</span></span> <span data-ttu-id="852cd-884">SMS, Azure 앱 푸시, ITSM 및 음성 수신기에는 적용되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-884">This is not applicable for SMS, Azure App push , ITSM and Voice recievers</span></span>
* <span data-ttu-id="852cd-885">웹후크에서 이제 Azure Active Directory 인증을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-885">Webhooks now supports Azure active directory authentication .</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="852cd-886">Az.Network</span><span class="sxs-lookup"><span data-stu-id="852cd-886">Az.Network</span></span>
* <span data-ttu-id="852cd-887">서비스 엔드포인트 정책에 사용할 수 있는 별칭을 가져오기 위해 호출할 수 있는 새 Get-AzAvailableServiceAlias cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-887">Add new cmdlet Get-AzAvailableServiceAlias which can be called to get the aliases that can be used for Service Endpoint Policies.</span></span>
* <span data-ttu-id="852cd-888">트래픽 선택기를 Virtual Network 게이트웨이 연결에 추가할 수 있는 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-888">Added support for the adding traffic selectors to Virtual Network Gateway Connections</span></span>
    - <span data-ttu-id="852cd-889">추가된 새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-889">New cmdlets added:</span></span>
        - <span data-ttu-id="852cd-890">New-AzureRmTrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="852cd-890">New-AzureRmTrafficSelectorPolicy</span></span>
    - <span data-ttu-id="852cd-891">cmdlet이 선택적인 -TrafficSelectorPolicies, -New-AzureRmVirtualNetworkGatewayConnection, -Set-AzureRmVirtualNetworkGatewayConnection 매개 변수로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-891">Cmdlets updated with optional parameter -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="852cd-892">ESP 및 AH 프로토콜 지원이 네트워크 보안 규칙 구성에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-892">Add support for ESP and AH protocols in network security rule configurations</span></span>
    - <span data-ttu-id="852cd-893">다음 Cmdlet이 업데이트 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-893">Updated cmdlets:</span></span>
        - <span data-ttu-id="852cd-894">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="852cd-894">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="852cd-895">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="852cd-895">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="852cd-896">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="852cd-896">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="852cd-897">Cortex cmdlet의 예외 처리가 향상되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-897">Improve handling of exceptions in Cortex cmdlets</span></span>
* <span data-ttu-id="852cd-898">새 VirtualNetworkGateways 세대 및 SKU</span><span class="sxs-lookup"><span data-stu-id="852cd-898">New Generations and SKUs for VirtualNetworkGateways</span></span>
  - <span data-ttu-id="852cd-899">새 VirtualNetworkGateways 세대가 도입되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-899">Introduce new Generations for VirtualNetworkGateways.</span></span>
  - <span data-ttu-id="852cd-900">높은 처리량의 새 VirtualNetworkGateways SKU가 도입되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-900">Introduce new high throughput SKUs for VirtualNetworkGateways.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="852cd-901">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="852cd-901">Az.RedisCache</span></span>
* <span data-ttu-id="852cd-902">'-Size' 매개 변수에 대한 누락 값을 포함하도록 'Set-AzRedisCache' 참조 설명서가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-902">Updated 'Set-AzRedisCache' reference documentation to include missing values for '-Size' parameter</span></span>

#### <a name="azsql"></a><span data-ttu-id="852cd-903">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="852cd-903">Az.Sql</span></span>
* <span data-ttu-id="852cd-904">Managed Instance에서 Active Directory 관리자를 설정할 수 있는 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-904">Add support for setting Active Directory Administrator on Managed Instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="852cd-905">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="852cd-905">Az.Storage</span></span>
* <span data-ttu-id="852cd-906">스토리지 클라이언트 라이브러리가 11.1.0으로 업그레이드되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-906">Upgrade Storage Client Library to 11.1.0</span></span>
* <span data-ttu-id="852cd-907">관리 평면 API를 사용하여 컨테이너를 나열하면 NextPageLink를 통해 나열됩니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-907">List containers with Management plane API, will list with NextPageLink</span></span>
    -  <span data-ttu-id="852cd-908">Get-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="852cd-908">Get-AzRmStorageContainer</span></span>
* <span data-ttu-id="852cd-909">구독에서 스토리지 계정을 나열하면 NextPageLink를 통해 나열됩니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-909">List Storage accounts from subscription, will list with NextPageLink</span></span>
    -  <span data-ttu-id="852cd-910">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="852cd-910">Get-AzStorageAccount</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="852cd-911">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="852cd-911">Az.StorageSync</span></span>
* <span data-ttu-id="852cd-912">Reset-AzStorageSyncServerCertificate의 9810 문제가 해결되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-912">Fix Issue 9810 in Reset-AzStorageSyncServerCertificate.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="852cd-913">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="852cd-913">Az.Websites</span></span>
* <span data-ttu-id="852cd-914">앱의 ASP를 업데이트하는 Set-AzWebApp이 실패했습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-914">Set-AzWebApp updating ASP of an app was failing</span></span>

## <a name="270---september-2019"></a><span data-ttu-id="852cd-915">2.7.0 - 2019년 9월</span><span class="sxs-lookup"><span data-stu-id="852cd-915">2.7.0 - September 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="852cd-916">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="852cd-916">Az.ApiManagement</span></span>
* <span data-ttu-id="852cd-917">'Set-AzApiManagementPolicy' 참조 설명서에서 '-Format' 매개 변수 설명이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-917">Update '-Format' parameter description in 'Set-AzApiManagementPolicy' reference documentation</span></span>
* <span data-ttu-id="852cd-918">참조 설명서에서 사용되지 않는 cmdlet 'Update-AzApiManagementDeployment'의 참조를 제거했습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-918">Removed references of deprecated cmdlet 'Update-AzApiManagementDeployment' from reference documentation.</span></span> <span data-ttu-id="852cd-919">그 대신 'Set-AzApiManagement'를 사용하세요.</span><span class="sxs-lookup"><span data-stu-id="852cd-919">Use 'Set-AzApiManagement' instead.</span></span>

#### <a name="azautomation"></a><span data-ttu-id="852cd-920">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="852cd-920">Az.Automation</span></span>
* <span data-ttu-id="852cd-921">'Register-AzAutomationDscNode'에 대한 참조 설명서의 예제 오타가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-921">Fixed example typo in reference documentation for 'Register-AzAutomationDscNode'</span></span>
* <span data-ttu-id="852cd-922">Register-AzAutomationDSCNode에 OS 제한에 대한 설명이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-922">Added clarification on OS restriction to Register-AzAutomationDSCNode</span></span>
* <span data-ttu-id="852cd-923">-Wait 옵션에 대한 Start-AzAutomationRunbook cmdlet Null 참조 예외가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-923">Fixed Start-AzAutomationRunbook cmdlet Null reference exception for -Wait option.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="852cd-924">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="852cd-924">Az.Compute</span></span>
* <span data-ttu-id="852cd-925">New-AzDiskConfig에 UploadSizeInBytes 매개 변수가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-925">Add UploadSizeInBytes parameter tp New-AzDiskConfig</span></span>
* <span data-ttu-id="852cd-926">New-AzSnapshotConfig에 증분 매개 변수가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-926">Add Incremental parameter to New-AzSnapshotConfig</span></span>
* <span data-ttu-id="852cd-927">다음과 같은 낮은 우선 순위의 가상 머신 기능이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-927">Add a low priority virtual machine feature:</span></span>
    - <span data-ttu-id="852cd-928">MaxPrice, EvictionPolicy 및 Priority 매개 변수가 New-AzVMConfig에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-928">MaxPrice, EvictionPolicy and Priority parameters are added to New-AzVMConfig.</span></span>
    - <span data-ttu-id="852cd-929">MaxPrice 매개 변수는 New-AzVmssConfig, Update-AzVM 및 Update-AzVmss cmdlet에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-929">MaxPrice parameter is added to New-AzVmssConfig, Update-AzVM and Update-AzVmss cmdlets.</span></span>
* <span data-ttu-id="852cd-930">구독의 모든 가용성 세트를 나열할 때 발생하는 Get-AzAvailabilitySet cmdlet에 대한 VM 참조 이슈가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-930">Fix VM reference issue for Get-AzAvailabilitySet cmdlet when it lists all availability sets in the subscription.</span></span>
* <span data-ttu-id="852cd-931">Get-AzRemoteDesktopFile에 대한 null 예외가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-931">Fix the null exception for Get-AzRemoteDesktopFile.</span></span>
* <span data-ttu-id="852cd-932">종료 상대 위치에 대한 VHD 검색 메서드가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-932">Fix VHD Seek method for end-relative position.</span></span>
* <span data-ttu-id="852cd-933">New-AzVM 및 Update-AzVM에 대한 UltraSSD 이슈가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-933">Fix UltraSSD issue for New-AzVM and Update-AzVM.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="852cd-934">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="852cd-934">Az.DataFactory</span></span>
* <span data-ttu-id="852cd-935">ADF V2에 대한 3가지 새 명령 Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription 및 Get-AzDataFactoryV2TriggerSubscriptionStatus가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-935">Adding 3 new commands for ADF V2 - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription, and Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>
* <span data-ttu-id="852cd-936">ADF .Net SDK 버전이 4.1.3으로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-936">Updated ADF .Net SDK version to 4.1.3</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="852cd-937">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="852cd-937">Az.HDInsight</span></span>
* <span data-ttu-id="852cd-938">호출 주요 변경 내용</span><span class="sxs-lookup"><span data-stu-id="852cd-938">Call out breaking changes</span></span>

#### <a name="aziothub"></a><span data-ttu-id="852cd-939">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="852cd-939">Az.IotHub</span></span>
* <span data-ttu-id="852cd-940">지역 쌍 재해 복구 지역에 IotHub에 대한 장애 조치(failover) 호출 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-940">Add support to invoke failover for an IotHub to the geo-paired disaster recovery region.</span></span>
* <span data-ttu-id="852cd-941">IotHub에 대한 메시지 보강 관리 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-941">Add support to manage message enrichment for an IotHub.</span></span> <span data-ttu-id="852cd-942">새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-942">New cmdlets are:</span></span>
    - <span data-ttu-id="852cd-943">Add-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="852cd-943">Add-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="852cd-944">Get-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="852cd-944">Get-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="852cd-945">Remove-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="852cd-945">Remove-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="852cd-946">Set-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="852cd-946">Set-AzIotHubMessageEnrichment</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="852cd-947">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="852cd-947">Az.Monitor</span></span>
* <span data-ttu-id="852cd-948">최신 모니터링 SDK, 즉, 0.24.1-preview를 가리킵니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-948">Pointing to the most recent Monitor SDK, i.e. 0.24.1-preview</span></span>
   - <span data-ttu-id="852cd-949">메트릭 cmdlet에 줄 바꿈하지 않는 변경 내용을 추가합니다. 즉, 단위 열거형은 여러 새 값을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-949">Adds non-braking changes to the Metrics cmdlets, i.e. the Unit enumeration supports several new values.</span></span> <span data-ttu-id="852cd-950">이러한 cmdlet은 읽기 전용이므로 cmdlet 입력이 변경되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-950">These are read-only cmdlets, so there would be no change in the input of the cmdlets.</span></span>
   - <span data-ttu-id="852cd-951">이제 **ActionGroups** 요청의 api 버전은 **2019-06-01**이고, 이전에는 **2018-03-01**였습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-951">The api-version of the **ActionGroups** requests is now **2019-06-01**, before it was **2018-03-01**.</span></span> <span data-ttu-id="852cd-952">시나리오 테스트가 이 변경 내용에 맞게 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-952">The scenario tests have been updated to accommodate for this change.</span></span>
   - <span data-ttu-id="852cd-953">**EmailReceiver** 및 **WebhookReceiver** 클래스에 대한 생성자가 새 필수 인수, 즉, **useCommonAlertSchema**라는 부울 값을 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-953">The constructors for the classes **EmailReceiver** and **WebhookReceiver** added one new mandatory argument, i.e. a Boolean value called **useCommonAlertSchema**.</span></span> <span data-ttu-id="852cd-954">현재 이 값은 cmdlet의 주요 변경 사항을 숨기도록 **false**로 고정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-954">Currently, the value is fixed to **false** to hide this breaking change from the cmdlets.</span></span> <span data-ttu-id="852cd-955">**참고**: 이 변경 사항은 경고 팀에서 유효성을 검사해야 하는 임시 변경 내용입니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-955">**NOTE**: this is a temporary change that must be validated by the Alerts team.</span></span>
   - <span data-ttu-id="852cd-956">이전 SDK에서 변경된 **Source** 클래스(**ScheduledQueryRuleSource** 클래스와 관련됨)의 생성자에 대한 인수 순서입니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-956">The order of the arguments for the constructor of the class **Source** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="852cd-957">이번 변화로 인해 두 개의 단위 테스트를 수정해야 했습니다. 즉, 두 단위 테스트가 컴파일되었지만 테스트를 통과하지 못했습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-957">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
   - <span data-ttu-id="852cd-958">이전 SDK에서 변경된 **AlertingAction** 클래스(**ScheduledQueryRuleSource** 클래스와 관련됨)의 생성자에 대한 인수 순서입니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-958">The order of the arguments for the constructor of the class **AlertingAction** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="852cd-959">이번 변화로 인해 두 개의 단위 테스트를 수정해야 했습니다. 즉, 두 단위 테스트가 컴파일되었지만 테스트를 통과하지 못했습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-959">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
* <span data-ttu-id="852cd-960">메트릭 경고 V2에 대한 동적 임계값 기준 지원</span><span class="sxs-lookup"><span data-stu-id="852cd-960">Support Dynamic Threshold criteria for metric alert V2</span></span>
    - <span data-ttu-id="852cd-961">AzMetricAlertRuleV2Criteria: 이제 동적 임계값 조건도 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-961">New-AzMetricAlertRuleV2Criteria: now creats dynamic threshold criteria also</span></span>
    - <span data-ttu-id="852cd-962">Add-AzMetricAlertRuleV2: 이제 동적 임계값 조건도 수락합니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-962">Add-AzMetricAlertRuleV2: now accept dynamic threshold criteria also</span></span>
* <span data-ttu-id="852cd-963">SQR(예약된 쿼리 규칙)의 향상된 기능</span><span class="sxs-lookup"><span data-stu-id="852cd-963">Improvements in Scheduled Query Rule cmdlets (SQR)</span></span>
 - <span data-ttu-id="852cd-964">Cmdlet이 'Location' 매개 변수를 두 가지 형식(eastus 같은 위치 또는 미국 동부 같은 위치 표시 이름)으로 모두 허용합니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-964">Cmdlets will accept 'Location' paramater in both formats, either the location (e.g. eastus) or the location display name (e.g. East US)</span></span>
 - <span data-ttu-id="852cd-965">도움말 파일에 적절하게 표시된 'Enabled' 매개 변수</span><span class="sxs-lookup"><span data-stu-id="852cd-965">Illustrated 'Enabled' parameter in help files properly</span></span>
 - <span data-ttu-id="852cd-966">선택적 매개 변수 'ActionGroup'에 대한 예제가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-966">Added examples for 'ActionGroup' optional parameter</span></span>
 - <span data-ttu-id="852cd-967">도움말 파일이 전체적으로 개선되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-967">Overall improved help files</span></span>
* <span data-ttu-id="852cd-968">'Set-AzActionRule'의 범위 유형 결정 버그를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-968">Fix bug in determining scope type for 'Set-AzActionRule'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="852cd-969">Az.Network</span><span class="sxs-lookup"><span data-stu-id="852cd-969">Az.Network</span></span>
* <span data-ttu-id="852cd-970">'New-AzApplicationGateway' 참조 설명서의 잘못된 예제가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-970">Fix incorrect example in 'New-AzApplicationGateway' reference documentation</span></span>
* <span data-ttu-id="852cd-971">'Get-AzNetworkWatcherPacketCapture' 참조 설명서에 패킷 캡처를 위한 모든 속성 검색과 관련된 메모가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-971">Add note in 'Get-AzNetworkWatcherPacketCapture' reference documentation about retrieving all properties for a packet capture</span></span>
* <span data-ttu-id="852cd-972">NIC를 올바르게 열거하도록 'Test-AzNetworkWatcherIPFlow' 참조 설명서의 예제가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-972">Fixed example in 'Test-AzNetworkWatcherIPFlow' reference documentation to correctly enumerate NICs</span></span>
* <span data-ttu-id="852cd-973">추가 세부 정보가 있는 경우 추가 세부 정보를 표시하도록 클라우드 예외 구문 분석이 향상되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-973">Improved cloud exception parsing to display additional details if they are present</span></span>
* <span data-ttu-id="852cd-974">더 많은 형식의 SDK 예외를 처리하도록 클라우드 예외 구문 분석이 향상되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-974">Improved cloud exception parsing to handle additional type of SDK exception</span></span>
* <span data-ttu-id="852cd-975">보안 규칙 모델의 잘못된 매핑이 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-975">Fixed incorrect mapping of Security Rule models</span></span>
* <span data-ttu-id="852cd-976">네트워크 인터페이스에 개인 IP 기능을 위한 속성이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-976">Added properties to network interface for private ip feature</span></span>
    - <span data-ttu-id="852cd-977">PSNetworkInterface에 'PrivateEndpoint' 속성이 PSResourceId 형식으로 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-977">Added property 'PrivateEndpoint' as type of PSResourceId to PSNetworkInterface</span></span>
    - <span data-ttu-id="852cd-978">PSNetworkInterfaceIPConfiguration에 'PrivateLinkConnectionProperties' 속성이 PSIpConfigurationConnectivityInformation 형식으로 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-978">Added property 'PrivateLinkConnectionProperties' as type of PSIpConfigurationConnectivityInformation to PSNetworkInterfaceIPConfiguration</span></span>
    - <span data-ttu-id="852cd-979">새 모델 클래스 PSIpConfigurationConnectivityInformation이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-979">Added new model class PSIpConfigurationConnectivityInformation</span></span>
* <span data-ttu-id="852cd-980">Azure Firewall 리소스에 대한 새 ApplicationRuleProtocolType 'mssql'이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-980">Added new ApplicationRuleProtocolType 'mssql' for Azure Firewall resource</span></span>
* <span data-ttu-id="852cd-981">Virtual WAN에서 멀티 링크를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-981">MultiLink support in Virtual WAN</span></span>
    - <span data-ttu-id="852cd-982">새로운 cmdlet</span><span class="sxs-lookup"><span data-stu-id="852cd-982">New cmdlets</span></span>
        - <span data-ttu-id="852cd-983">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="852cd-983">New-AzVpnSiteLink</span></span>
        - <span data-ttu-id="852cd-984">New-AzVpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="852cd-984">New-AzVpnSiteLinkConnection</span></span>
    - <span data-ttu-id="852cd-985">업데이트된 cmdlet:</span><span class="sxs-lookup"><span data-stu-id="852cd-985">Updated cmdlet:</span></span>
        - <span data-ttu-id="852cd-986">New-VpnSite</span><span class="sxs-lookup"><span data-stu-id="852cd-986">New-VpnSite</span></span>
        - <span data-ttu-id="852cd-987">Update-VpnSite</span><span class="sxs-lookup"><span data-stu-id="852cd-987">Update-VpnSite</span></span>
        - <span data-ttu-id="852cd-988">New-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="852cd-988">New-VpnConnection</span></span>
        - <span data-ttu-id="852cd-989">Update-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="852cd-989">Update-VpnConnection</span></span>
* <span data-ttu-id="852cd-990">AzureRM cmdlet 대신 Az cmdlet을 사용하도록 일부 PowerShell 예제의 문서가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-990">Fixed documents for some PowerShell examples to use Az cmdlets instead of AzureRM cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="852cd-991">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="852cd-991">Az.RecoveryServices</span></span>
* <span data-ttu-id="852cd-992">AzureVMpolicy 개체가 ProtectedItemsCount 특성으로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-992">Update AzureVMpolicy Object with ProtectedItemsCount Attribute</span></span>
* <span data-ttu-id="852cd-993">VM 정책 및 원래 스토리지 계정 복원에 대한 테스트가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-993">Added Tests for VM policy and Original Storage Account Restore</span></span>

#### <a name="azresources"></a><span data-ttu-id="852cd-994">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="852cd-994">Az.Resources</span></span>
* <span data-ttu-id="852cd-995">매개 변수 범위 없이 AzRoleAssignment를 호출할 수 없는 버그가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-995">Fix bug where New-AzRoleAssignment could not be called without parameter Scope.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="852cd-996">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="852cd-996">Az.ServiceFabric</span></span>
* <span data-ttu-id="852cd-997">'AzServiceFabricReliability' 참조 설명서에 대한 예제의 오타가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-997">Fixed typo in example for 'Update-AzServiceFabricReliability' reference documentation</span></span>
* <span data-ttu-id="852cd-998">애플리케이션 및 서비스를 관리하는 다음과 같은 새 cmdlet이 추가됩니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-998">Adding new cmdlets to manage appliaction and services:</span></span>
    - <span data-ttu-id="852cd-999">New-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="852cd-999">New-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="852cd-1000">New-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="852cd-1000">New-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="852cd-1001">New-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="852cd-1001">New-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="852cd-1002">New-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="852cd-1002">New-AzServiceFabricService</span></span>
    - <span data-ttu-id="852cd-1003">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="852cd-1003">Update-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="852cd-1004">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="852cd-1004">Get-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="852cd-1005">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="852cd-1005">Get-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="852cd-1006">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="852cd-1006">Get-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="852cd-1007">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="852cd-1007">Get-AzServiceFabricService</span></span>
    - <span data-ttu-id="852cd-1008">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="852cd-1008">Remove-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="852cd-1009">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="852cd-1009">Remove-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="852cd-1010">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="852cd-1010">Remove-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="852cd-1011">Remove-AzServiceFabricServic</span><span class="sxs-lookup"><span data-stu-id="852cd-1011">Remove-AzServiceFabricServic</span></span>
* <span data-ttu-id="852cd-1012">Service Fabric SDK가 Service Fabric 리소스 공급자 api 버전 2019-03-01을 사용하는 1.2.0 버전으로 업그레이드되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-1012">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2019-03-01.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="852cd-1013">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="852cd-1013">Az.SignalR</span></span>
* <span data-ttu-id="852cd-1014">Update, Restart, CheckNameAvailability, GetUsage Cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-1014">Add Update, Restart, CheckNameAvailability, GetUsage Cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="852cd-1015">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="852cd-1015">Az.Sql</span></span>
* <span data-ttu-id="852cd-1016">'Get-AzSqlElasticPool'에 대한 참조 설명서의 예제가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-1016">Update example in reference documentation for 'Get-AzSqlElasticPool'</span></span>
* <span data-ttu-id="852cd-1017">탄력적 풀을 만드는 vCore 예제가 추가되었습니다(AzSqlElasticPool).</span><span class="sxs-lookup"><span data-stu-id="852cd-1017">Added vCore example to creating an elastic pool (New-AzSqlElasticPool).</span></span>
* <span data-ttu-id="852cd-1018">Set-AzSqlServerAdvancedThreatProtectionPolicy 및 Set-AzSqlDatabaseAdvancedThreatProtectionPolicy에서 EmailAddresses가 비어 있는 경우 EmailAddresses의 유효성을 검사하고 EmailAdmins가 false가 아닌지 확인하는 기능이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-1018">Remove the validation of EmailAddresses and the check that EmailAdmins is not false in case EmailAddresses is empty in Set-AzSqlServerAdvancedThreatProtectionPolicy and Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="852cd-1019">감사 범주를 사용하는 여러 진단 설정이 있는 경우 서버/데이터베이스 감사 설정을 제거하도록 설정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-1019">Enabled removal of server/database auditing settings when multiple diagnostic settings that enable audit category exist.</span></span>
* <span data-ttu-id="852cd-1020">여러 Sql 취약성 평가 cmdlet에서 이메일 주소 유효성 검사가 수정되었습니다(Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting 및 Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span><span class="sxs-lookup"><span data-stu-id="852cd-1020">Fix email addresses validation in multiple Sql Vulnerability Assessment cmdlets (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting and Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span></span>

#### <a name="azstorage"></a><span data-ttu-id="852cd-1021">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="852cd-1021">Az.Storage</span></span>
* <span data-ttu-id="852cd-1022">'Get-AzStorageAccountKey'에 대한 참조 설명서의 예제가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-1022">Updated example in reference documentation for 'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="852cd-1023">Azure 파일 업로드/다운에서, 원본 파일 SMB 속성(파일 특성, 파일 생성 시간, 파일을 마지막으로 쓴 시간)을 대상 파일에 보존하는 기능이 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-1023">In upload/Downalod Azure File,support perserve the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the destination file</span></span>
    -  <span data-ttu-id="852cd-1024">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="852cd-1024">Set-AzStorageFileContent</span></span>
    -  <span data-ttu-id="852cd-1025">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="852cd-1025">Get-AzStorageFileContent</span></span>
* <span data-ttu-id="852cd-1026">컨테이너가 사용되는 ImmutabilityPolicy에서 properties/metadate fail을 사용하여 블록 Blob 업로드가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-1026">Fix Upload block blob with properties/metadate fail on container enabled ImmutabilityPolicy.</span></span>
    -  <span data-ttu-id="852cd-1027">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="852cd-1027">Set-AzStorageBlobContent</span></span>
* <span data-ttu-id="852cd-1028">관리 평면 API를 사용하여 Azure 파일 공유 관리를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-1028">Support manage Azure File shares with Management plane API</span></span>
    -  <span data-ttu-id="852cd-1029">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="852cd-1029">New-AzRmStorageShare</span></span>
    -  <span data-ttu-id="852cd-1030">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="852cd-1030">Get-AzRmStorageShare</span></span>
    -  <span data-ttu-id="852cd-1031">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="852cd-1031">Update-AzRmStorageShare</span></span>
    -  <span data-ttu-id="852cd-1032">Remove-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="852cd-1032">Remove-AzRmStorageShare</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="852cd-1033">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="852cd-1033">Az.Websites</span></span>
* <span data-ttu-id="852cd-1034">앱을 새 ASP로 마이그레이션할 때 웹앱 태그가 삭제되는 이슈가 해결되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-1034">Fixing issue where webapp Tags were getting deleted when migrating App to new ASPwhere webapp Tags were getting deleted when migrating App to new ASP</span></span>
* <span data-ttu-id="852cd-1035">Linux와 Windows에서 모두 작동하도록 Publish-AzureWebapp이 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-1035">Fixing the Publish-AzureWebapp to work across Linux and windows</span></span>
* <span data-ttu-id="852cd-1036">'Get-AzWebAppPublishingProfile' 참조 설명서의 예제가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-1036">Update example in 'Get-AzWebAppPublishingProfile' reference documentation</span></span>

## <a name="260---august-2019"></a><span data-ttu-id="852cd-1037">2.6.0 - 2019년 8월</span><span class="sxs-lookup"><span data-stu-id="852cd-1037">2.6.0 - August 2019</span></span>
#### <a name="general"></a><span data-ttu-id="852cd-1038">일반</span><span class="sxs-lookup"><span data-stu-id="852cd-1038">General</span></span>
* <span data-ttu-id="852cd-1039">여러 모듈에서 기타 오타가 수정됨</span><span class="sxs-lookup"><span data-stu-id="852cd-1039">Fixed miscellaneous typos across numerous modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="852cd-1040">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="852cd-1040">Az.Accounts</span></span>
* <span data-ttu-id="852cd-1041">Azure Functions 인증에서 사용자가 할당한 MSI가 지원됨(# 9479)</span><span class="sxs-lookup"><span data-stu-id="852cd-1041">Support user-assigned MSI in Azure Functiosn Authentication (#9479)</span></span>

#### <a name="azaks"></a><span data-ttu-id="852cd-1042">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="852cd-1042">Az.Aks</span></span>
* <span data-ttu-id="852cd-1043">'Get-AzAks' 출력 관련 문제가 해결됨</span><span class="sxs-lookup"><span data-stu-id="852cd-1043">Fix issue with output for 'Get-AzAks'</span></span>
    * <span data-ttu-id="852cd-1044">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/9847 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="852cd-1044">More information here: https://github.com/Azure/azure-powershell/issues/9847</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="852cd-1045">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="852cd-1045">Az.ApiManagement</span></span>
* <span data-ttu-id="852cd-1046">문제 https://github.com/Azure/azure-powershell/issues/9351 수정</span><span class="sxs-lookup"><span data-stu-id="852cd-1046">Fix for issue https://github.com/Azure/azure-powershell/issues/9351</span></span>
    - <span data-ttu-id="852cd-1047">productId, apiId, groupId 및 userId에 대한 제한을 적용하지 않는 .Net NuGet 버전이 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="852cd-1047">Update .net nuget version, which does not enforce restrictions on productId, apiId, groupId and userId</span></span>
* <span data-ttu-id="852cd-1048">**Get-AzApiManagementProduct** - API를 사용하는 제품에 대한 쿼리 지원이 추가됨</span><span class="sxs-lookup"><span data-stu-id="852cd-1048">**Get-AzApiManagementProduct** - Added support for querying products using Api.</span></span>
  https://github.com/Azure/azure-powershell/issues/9482
* <span data-ttu-id="852cd-1049">**New-AzApiManagementApiRevision** - 새 API 수정(https://github.com/Azure/azure-powershell/issues/9752 )을 만들 때 ApiRevisionDescription이 설정되지 않은 문제가 해결됨</span><span class="sxs-lookup"><span data-stu-id="852cd-1049">**New-AzApiManagementApiRevision** - Fix for issue where ApiRevisionDescription was not being set when creating new api revision https://github.com/Azure/azure-powershell/issues/9752</span></span>
* <span data-ttu-id="852cd-1050">'PsApiManagementOAuth2AuthrozationServer' 모델의 오타가 'PsApiManagementOAuth2AuthorizationServer'로 수정됨</span><span class="sxs-lookup"><span data-stu-id="852cd-1050">Fixed typo in model 'PsApiManagementOAuth2AuthrozationServer' to 'PsApiManagementOAuth2AuthorizationServer'</span></span>

#### <a name="azbatch"></a><span data-ttu-id="852cd-1051">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="852cd-1051">Az.Batch</span></span>
* <span data-ttu-id="852cd-1052">도움말 메시지 및 설명서에서 Windows를 대문자로 시작하도록 오타가 수정됨</span><span class="sxs-lookup"><span data-stu-id="852cd-1052">Fixed typo in help message and documentation to capitalize Windows</span></span>

#### <a name="azcdn"></a><span data-ttu-id="852cd-1053">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="852cd-1053">Az.Cdn</span></span>
* <span data-ttu-id="852cd-1054">CDN 모듈 변환 도우미의 오타가 수정됨</span><span class="sxs-lookup"><span data-stu-id="852cd-1054">Fixed a typo in CDN module conversion helper</span></span>

#### <a name="azcompute"></a><span data-ttu-id="852cd-1055">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="852cd-1055">Az.Compute</span></span>
* <span data-ttu-id="852cd-1056">VmssId가 New-AzVMConfig cmdlet에 추가됨</span><span class="sxs-lookup"><span data-stu-id="852cd-1056">Add VmssId to New-AzVMConfig cmdlet</span></span>
* <span data-ttu-id="852cd-1057">TerminateScheduledEvents 및 TerminateScheduledEventNotBeforeTimeoutInMinutes 매개 변수가 New-AzVmssConfig 및 Update-AzVmss에 추가됨</span><span class="sxs-lookup"><span data-stu-id="852cd-1057">Add TerminateScheduledEvents and TerminateScheduledEventNotBeforeTimeoutInMinutes parameters to New-AzVmssConfig and Update-AzVmss</span></span>
* <span data-ttu-id="852cd-1058">HyperVGeneration 속성이 VM 이미지 개체에 추가됨</span><span class="sxs-lookup"><span data-stu-id="852cd-1058">Add HyperVGeneration property to VM image object</span></span>
* <span data-ttu-id="852cd-1059">Host 및 HostGroup 기능이 추가됨</span><span class="sxs-lookup"><span data-stu-id="852cd-1059">Add Host and HostGroup features</span></span>
    - <span data-ttu-id="852cd-1060">새 cmdlet:   New-AzHostGroup, New-AzHost, Get-AzHostGroup, Get-AzHost, Remove-AzHostGroup, Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="852cd-1060">New cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span></span>
    - <span data-ttu-id="852cd-1061">HostId 매개 변수가 New-AzVMConfig 및 New-AzVM 추가됨</span><span class="sxs-lookup"><span data-stu-id="852cd-1061">HostId parameter is added to New-AzVMConfig and New-AzVM</span></span>
* <span data-ttu-id="852cd-1062">'Invoke-AzVMRunCommand' 설명서의 예제에서 올바른 매개 변수 이름을 사용하도록 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="852cd-1062">Update example in 'Invoke-AzVMRunCommand' documentation to use correct parameter name</span></span>
* <span data-ttu-id="852cd-1063">'Set-AzVMDiskEncryptionExtension' 및 'Set-AzVmssDiskEncryptionExtension' 참조 설명서의 '-VolumeType' 설명이 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="852cd-1063">Update '-VolumeType' description in 'Set-AzVMDiskEncryptionExtension' and 'Set-AzVmssDiskEncryptionExtension' reference documentation</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="852cd-1064">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="852cd-1064">Az.DataFactory</span></span>
* <span data-ttu-id="852cd-1065">'New-AzDataFactoryEncryptValue' 설명서에서 'Windows'를 대문자로 시작하도록 오타가 수정됨</span><span class="sxs-lookup"><span data-stu-id="852cd-1065">Fix typo to capitalize 'Windows' in 'New-AzDataFactoryEncryptValue' documentation</span></span>
* <span data-ttu-id="852cd-1066">ADF .Net SDK 버전이 4.1.2로 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="852cd-1066">Updated ADF .Net SDK version to 4.1.2</span></span>
* <span data-ttu-id="852cd-1067">자체 호스팅 통합 런타임을 SSIS Integration Runtime의 프록시로 설정할 수 있도록 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' 및 'DataProxyStagingPath' 매개 변수가 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd에 추가됨</span><span class="sxs-lookup"><span data-stu-id="852cd-1067">Add parameter 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' and 'DataProxyStagingPath' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable set up Self-Hosted Integration Runtime as a proxy for SSIS Integration Runtime</span></span>
* <span data-ttu-id="852cd-1068">PSTriggerRun에서 트리거된 파이프라인, 메시지 및 속성을 표시하고, PSActivityRun에서 작업 유형을 표시하도록 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="852cd-1068">Updated PSTriggerRun to show the triggered pipelines, message and properties, and PSActivityRun to show the activity type</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="852cd-1069">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="852cd-1069">Az.DataLakeStore</span></span>
* <span data-ttu-id="852cd-1070">오류 또는 원격 예외에 대한 Get-DataLakeStoreDeletedItem 중단이 수정됨</span><span class="sxs-lookup"><span data-stu-id="852cd-1070">Fix hanging of Get-DataLakeStoreDeletedItem for any errors or remote exceptions.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="852cd-1071">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="852cd-1071">Az.EventHub</span></span>
* <span data-ttu-id="852cd-1072">#9658 문제 해결: Set-AzEventHubNetworkRuleSet의 VirtualNteworkRule 매개 변수에 대한 오타</span><span class="sxs-lookup"><span data-stu-id="852cd-1072">Fix for issue #9658 : Typo VirtualNteworkRule parameter in Set-AzEventHubNetworkRuleSet</span></span>
* <span data-ttu-id="852cd-1073">#9558 문제 해결: Set-AzEventHubNamespace에서 PUT 대신 PATCH가 사용됨</span><span class="sxs-lookup"><span data-stu-id="852cd-1073">Fix for issue #9558 : Set-AzEventHubNamespace is using PATCH instead of PUT</span></span>
* <span data-ttu-id="852cd-1074">EnableKafka 매개 변수가 Set-AzEventHubNamespace cmdlet에 추가됨</span><span class="sxs-lookup"><span data-stu-id="852cd-1074">added EnableKafka parameter to Set-AzEventHubNamespace cmdlet</span></span>
* <span data-ttu-id="852cd-1075">#9786 문제 해결: Listen(수신 대기) 전용 권한이 있는 규칙을 만들 수 없음</span><span class="sxs-lookup"><span data-stu-id="852cd-1075">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>

#### <a name="azmarketplaceordering"></a><span data-ttu-id="852cd-1076">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="852cd-1076">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="852cd-1077">'Azure'가 모두 소문자인 설명서의 오타가 수정됨</span><span class="sxs-lookup"><span data-stu-id="852cd-1077">Fixed documentation typo where 'Azure' was all lowercase letters</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="852cd-1078">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="852cd-1078">Az.Monitor</span></span>
* <span data-ttu-id="852cd-1079">도움말 설명서에서 잘못된 매개 변수 이름이 수정됨</span><span class="sxs-lookup"><span data-stu-id="852cd-1079">Fixed incorrect parameter name in help documentation</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="852cd-1080">Az.Network</span><span class="sxs-lookup"><span data-stu-id="852cd-1080">Az.Network</span></span>
* <span data-ttu-id="852cd-1081">New-AzPrivateLinkServiceIpConfig가 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="852cd-1081">Updated New-AzPrivateLinkServiceIpConfig</span></span>
    - <span data-ttu-id="852cd-1082">서버 쪽에서 사용되지 않으므로 'PublicIpAddress' 매개 변수가 사용되지 않음</span><span class="sxs-lookup"><span data-stu-id="852cd-1082">Deprecated the paramster 'PublicIpAddress' since this is never used in the server side.</span></span>
    - <span data-ttu-id="852cd-1083">현재 IP 구성이 기본 구성인지 여부를 나타내는 하나의 선택적 'Primary' 매개 변수가 추가됨</span><span class="sxs-lookup"><span data-stu-id="852cd-1083">Added one optional parameter 'Primary' that indicate the current ip configuration is primary one or not.</span></span>
* <span data-ttu-id="852cd-1084">SDK의 요청 오류 예외 처리가 향상됨 - 이전의 SDK 예외가 올바르게 처리되지 않아 주요 오류 세부 정보가 표시되지 않은 문제가 해결됨</span><span class="sxs-lookup"><span data-stu-id="852cd-1084">Improved handling of request error exception from SDK   -Fixes the issue that previously SDK exceptions aren't handled correctly which results in key error details not being displayed</span></span>
* <span data-ttu-id="852cd-1085">올바른 IPv6 접두사 길이를 확인하기 위해 Ipv6 IP 접두사에 대한 유효성 검사 논리가 조정됨</span><span class="sxs-lookup"><span data-stu-id="852cd-1085">Adjusted validation logic for Ipv6 IP Prefix to check for correct IPv6 prefix length.</span></span>
* <span data-ttu-id="852cd-1086">Get-AzVirtualNetworkSubnetConfig가 업데이트됨: 서브넷 리소스 ID별로 가져오도록 설정되는 매개 변수 세트가 추가됨</span><span class="sxs-lookup"><span data-stu-id="852cd-1086">Updated Get-AzVirtualNetworkSubnetConfig: Added parameter set to get by subnet resource id.</span></span>
* <span data-ttu-id="852cd-1087">AzNetworkServiceTag의 Location(위치) 매개 변수에 대한 설명이 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="852cd-1087">Updated description of Location parameter for AzNetworkServiceTag</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="852cd-1088">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="852cd-1088">Az.OperationalInsights</span></span>
* <span data-ttu-id="852cd-1089">'New-AzOperationalInsightsLinuxSyslogDataSource'에 대한 설명서가 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="852cd-1089">Updated documentation for 'New-AzOperationalInsightsLinuxSyslogDataSource'</span></span>
    - <span data-ttu-id="852cd-1090">예제가 추가됨</span><span class="sxs-lookup"><span data-stu-id="852cd-1090">Added example</span></span>
    - <span data-ttu-id="852cd-1091">'-Name' 매개 변수에 대한 설명이 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="852cd-1091">Updated description for '-Name' parameter</span></span>
* <span data-ttu-id="852cd-1092">New-AzOperationalInsightsWindowsEventDataSource에 대한 예제가 추가됨</span><span class="sxs-lookup"><span data-stu-id="852cd-1092">Added an example for New-AzOperationalInsightsWindowsEventDataSource</span></span>
* <span data-ttu-id="852cd-1093">New-AzOperationalInsightsWindowsEventDataSource의 -Name 매개 변수에 대한 설명이 변경됨</span><span class="sxs-lookup"><span data-stu-id="852cd-1093">Changed the description of the -Name parameter for New-AzOperationalInsightsWindowsEventDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="852cd-1094">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="852cd-1094">Az.RecoveryServices</span></span>
* <span data-ttu-id="852cd-1095">'Get-AzRecoveryServicesBackupJobDetail.md'가 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="852cd-1095">Update 'Get-AzRecoveryServicesBackupJobDetail.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="852cd-1096">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="852cd-1096">Az.Resources</span></span>
* <span data-ttu-id="852cd-1097">Microsoft 리소스에 대한 새 2019-05-10 API 버전 지원이 추가됨</span><span class="sxs-lookup"><span data-stu-id="852cd-1097">Add support for new api version 2019-05-10 for Microsoft.Resource</span></span>
    - <span data-ttu-id="852cd-1098">변수, 리소스 및 속성에 대한 'copy.count = 0' 지원이 추가됨</span><span class="sxs-lookup"><span data-stu-id="852cd-1098">Add support for 'copy.count = 0' for variables, resources and properties</span></span>
    - <span data-ttu-id="852cd-1099">'condition = false' 또는 'copy.count = 0'인 리소스가 완료 모드에서 삭제됨</span><span class="sxs-lookup"><span data-stu-id="852cd-1099">Resources with 'condition = false' or 'copy.count = 0' will be deleted in complete mode</span></span>
* <span data-ttu-id="852cd-1100">정책을 구독 수준에서 도움말 문서에 할당하는 예제가 추가됨</span><span class="sxs-lookup"><span data-stu-id="852cd-1100">Add an example of assigning policy at subscription level to help doc</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="852cd-1101">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="852cd-1101">Az.ServiceBus</span></span>
* <span data-ttu-id="852cd-1102">#9658 문제 해결: Set-AzServiceBusNetworkRuleSet의 VirtualNetworkRule 매개 변수에 대한 오타</span><span class="sxs-lookup"><span data-stu-id="852cd-1102">Fix for issue #9658 : Typo VirtualNetworkRule parameter in Set-AzServiceBusNetworkRuleSet</span></span>
* <span data-ttu-id="852cd-1103">#9786 문제 해결: Listen(수신 대기) 전용 권한이 있는 규칙을 만들 수 없음</span><span class="sxs-lookup"><span data-stu-id="852cd-1103">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>
* <span data-ttu-id="852cd-1104">큐 및 토픽에 대한 이름 가용성을 확인하는 새 'Test-AzServiceBusNameAvailability' 명령이 추가됨</span><span class="sxs-lookup"><span data-stu-id="852cd-1104">Added new command 'Test-AzServiceBusNameAvailability' to check the name availability for queue and topic</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="852cd-1105">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="852cd-1105">Az.ServiceFabric</span></span>
* <span data-ttu-id="852cd-1106">노드 유형 추가 cmdlet 버그 수정:</span><span class="sxs-lookup"><span data-stu-id="852cd-1106">Fix add node type cmdlet bugs:</span></span>
    - <span data-ttu-id="852cd-1107">서비스 패브릭 클러스터와 관련이 없는 다른 vmss가 리소스 그룹에 있을 때 발생하는 NullReferenceException 버그</span><span class="sxs-lookup"><span data-stu-id="852cd-1107">NullReferenceException bug when resource group had other vmss not related to the service fabric cluster.</span></span> <span data-ttu-id="852cd-1108">문제 해결: https://github.com/Azure/azure-powershell/issues/8681</span><span class="sxs-lookup"><span data-stu-id="852cd-1108">Fixes issue: https://github.com/Azure/azure-powershell/issues/8681</span></span>
    - <span data-ttu-id="852cd-1109">virtualNetwork가 클러스터의 다른 리소스 그룹에 있을 때 cmdlet이 실패하는 버그가 수정됨</span><span class="sxs-lookup"><span data-stu-id="852cd-1109">Fix bug where cmdlet failed if virtualNetwork was in a different resource group that the cluster.</span></span> <span data-ttu-id="852cd-1110">문제 해결: https://github.com/Azure/azure-powershell/issues/8407</span><span class="sxs-lookup"><span data-stu-id="852cd-1110">fixes issue: https://github.com/Azure/azure-powershell/issues/8407</span></span>
    - <span data-ttu-id="852cd-1111">Add-AzServiceFabricApplicationCertificate cmdlet이 사용되지 않음</span><span class="sxs-lookup"><span data-stu-id="852cd-1111">Deprecating Add-AzServiceFabricApplicationCertificate cmdlet</span></span>

#### <a name="azsql"></a><span data-ttu-id="852cd-1112">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="852cd-1112">Az.Sql</span></span>
* <span data-ttu-id="852cd-1113">이전의 Auditing(감사) cmdlet에 대한 설명서가 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="852cd-1113">Update documentation of old Auditing cmdlets.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="852cd-1114">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="852cd-1114">Az.Storage</span></span>
* <span data-ttu-id="852cd-1115">더 많은 시나리오를 cmdlet 예제에 추가하고 매개 변수 설명을 업데이트하여 Get/Close-AzStorageFileHandle에 대한 도움말이 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="852cd-1115">Update help for Get/Close-AzStorageFileHandle, by add more scenarios to cmdlet examples and update parameter descriptions</span></span>
* <span data-ttu-id="852cd-1116">Blob 업로드 및 Blob 복사에서 StandardBlobTier가 지원됨</span><span class="sxs-lookup"><span data-stu-id="852cd-1116">Support StandardBlobTier in upload blob and copy blob</span></span>
    -  <span data-ttu-id="852cd-1117">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="852cd-1117">Set-AzStorageBlobContent</span></span>
    -  <span data-ttu-id="852cd-1118">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="852cd-1118">Start-AzStorageBlobCopy</span></span>
* <span data-ttu-id="852cd-1119">Blob 복사에서 우선 순위 리하이드레이션이 지원됨</span><span class="sxs-lookup"><span data-stu-id="852cd-1119">Support Rehydrate Priority in copy blob</span></span>
    -  <span data-ttu-id="852cd-1120">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="852cd-1120">Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="852cd-1121">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="852cd-1121">Az.Websites</span></span>
* <span data-ttu-id="852cd-1122">Set-AzWebApp 및 Set-AzWebAppSlot에서 -AppSettings 매개 변수에 대한 설명이 추가됨</span><span class="sxs-lookup"><span data-stu-id="852cd-1122">Add clarification around -AppSettings parameter in Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <a name="250---july-2019"></a><span data-ttu-id="852cd-1123">2.5.0 - 2019년 7월</span><span class="sxs-lookup"><span data-stu-id="852cd-1123">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="852cd-1124">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="852cd-1124">Az.Accounts</span></span>
* <span data-ttu-id="852cd-1125">ClientRuntime의 최신 버전을 사용하도록 일반적인 코드를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-1125">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="852cd-1126">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="852cd-1126">Az.ApplicationInsights</span></span>
* <span data-ttu-id="852cd-1127">'Remove-AzApplicationInsightsApiKey' 설명서의 예제 오타 수정</span><span class="sxs-lookup"><span data-stu-id="852cd-1127">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span>

#### <a name="azautomation"></a><span data-ttu-id="852cd-1128">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="852cd-1128">Az.Automation</span></span>
* <span data-ttu-id="852cd-1129">리소스 문자열의 오타 수정</span><span class="sxs-lookup"><span data-stu-id="852cd-1129">Fix typo in resource string</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="852cd-1130">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="852cd-1130">Az.CognitiveServices</span></span>
* <span data-ttu-id="852cd-1131">NetworkRuleSet 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-1131">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="852cd-1132">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="852cd-1132">Az.Compute</span></span>
* <span data-ttu-id="852cd-1133">VM 인스턴스 보기 개체의 누락된 속성(ComputerName, OsName, OsVersion 및 HyperVGeneration)을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-1133">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="852cd-1134">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="852cd-1134">Az.ContainerRegistry</span></span>
* <span data-ttu-id="852cd-1135">복제 매개 변수의 Remove-AzContainerRegistryReplication에서 오타 수정</span><span class="sxs-lookup"><span data-stu-id="852cd-1135">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="852cd-1136">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/9633 을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="852cd-1136">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="852cd-1137">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="852cd-1137">Az.DataFactory</span></span>
* <span data-ttu-id="852cd-1138">ADF .Net SDK 버전을 4.1.0으로 업데이트</span><span class="sxs-lookup"><span data-stu-id="852cd-1138">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="852cd-1139">'Get-AzDataFactoryV2PipelineRun' 설명서의 오타 수정</span><span class="sxs-lookup"><span data-stu-id="852cd-1139">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="852cd-1140">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="852cd-1140">Az.EventHub</span></span>
* <span data-ttu-id="852cd-1141">SAS 토큰을 생성하기 위해 추가된 새로운 cmmdlet 추가: New-AzEventHubAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="852cd-1141">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="852cd-1142">'관리'만 지정된 경우 authorizationrules 권한에 대한 확인 및 오류 메시지 추가</span><span class="sxs-lookup"><span data-stu-id="852cd-1142">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="852cd-1143">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="852cd-1143">Az.KeyVault</span></span>
* <span data-ttu-id="852cd-1144">인증서 정책에 대한 KeySize 지정을 위한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="852cd-1144">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="852cd-1145">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="852cd-1145">Az.LogicApp</span></span>
* <span data-ttu-id="852cd-1146">모든 맵 유형을 나열하도록 Get-AzIntegrationAccountMap 수정</span><span class="sxs-lookup"><span data-stu-id="852cd-1146">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="852cd-1147">필터링을 위해 새 MapType 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="852cd-1147">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="852cd-1148">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="852cd-1148">Az.ManagedServices</span></span>
* <span data-ttu-id="852cd-1149">API 버전 2019-06-01(GA)에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="852cd-1149">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="852cd-1150">Az.Network</span><span class="sxs-lookup"><span data-stu-id="852cd-1150">Az.Network</span></span>
* <span data-ttu-id="852cd-1151">프라이빗 엔드포인트 및 프라이빗 링크 서비스에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="852cd-1151">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="852cd-1152">새로운 cmdlet</span><span class="sxs-lookup"><span data-stu-id="852cd-1152">New cmdlets</span></span>
        - <span data-ttu-id="852cd-1153">Set-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="852cd-1153">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="852cd-1154">Set-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="852cd-1154">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="852cd-1155">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="852cd-1155">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="852cd-1156">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="852cd-1156">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="852cd-1157">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="852cd-1157">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="852cd-1158">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="852cd-1158">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="852cd-1159">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="852cd-1159">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="852cd-1160">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="852cd-1160">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="852cd-1161">기능에 대한 새로운 명령이 업데이트됨: Virtualnetwork의 서브넷에 있는 PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies 플래그</span><span class="sxs-lookup"><span data-stu-id="852cd-1161">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="852cd-1162">업데이트된 New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="852cd-1162">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="852cd-1163">이 서브넷의 프라이빗 엔드포인트에 네트워크 정책을 적용할지 여부를 나타내는 선택적 매개 변수 -PrivateEndpointNetworkPoliciesFlag가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-1163">Added optional parameter -PrivateEndpointNetworkPoliciesFlag that configures whether to apply network policies on private endpoint in this subnet.</span></span>
        - <span data-ttu-id="852cd-1164">이 서브넷의 프라이빗 연결 서비스에 네트워크 정책을 적용할지 여부를 나타내는 선택적 매개 변수 -PrivateLinkServiceNetworkPoliciesFlag가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-1164">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag that configures whether to apply network policies network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="852cd-1165">AzPrivateLinkService의 cmdlet 매개 변수 'ServiceName'이 이전 버전과의 호환성을 위해 별칭 'ServiceName'을 사용한 'Name'으로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-1165">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="852cd-1166">네트워크 보안 규칙 구성에 ICMP 프로토콜 사용</span><span class="sxs-lookup"><span data-stu-id="852cd-1166">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="852cd-1167">다음 Cmdlet이 업데이트 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-1167">Updated cmdlets</span></span>
        - <span data-ttu-id="852cd-1168">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="852cd-1168">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="852cd-1169">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="852cd-1169">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="852cd-1170">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="852cd-1170">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="852cd-1171">New-AzVirtualNetworkGatewayConnection에 대한 구성 가능한 매개 변수로 ConnectionProtocolType (Ikev1/Ikev2) 추가</span><span class="sxs-lookup"><span data-stu-id="852cd-1171">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="852cd-1172">LoadBalancerFrontendIpConfiguration에 PrivateIpAddressVersion 추가</span><span class="sxs-lookup"><span data-stu-id="852cd-1172">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="852cd-1173">업데이트된 cmdlet:</span><span class="sxs-lookup"><span data-stu-id="852cd-1173">Updated cmdlet:</span></span>
        - <span data-ttu-id="852cd-1174">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="852cd-1174">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="852cd-1175">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="852cd-1175">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="852cd-1176">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="852cd-1176">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="852cd-1177">프로브에서 사용자 지정 포트를 지원하기 위한 Application Gateway New-AzApplicationGatewayProbeConfig 명령 업데이트</span><span class="sxs-lookup"><span data-stu-id="852cd-1177">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="852cd-1178">업데이트된 New-AzApplicationGatewayProbeConfig: 백 엔드 서버 검색에 사용되는 선택적 매개 변수 포트가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-1178">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="852cd-1179">이 매개 변수는 Standard_V2 및 WAF_V2 SKU에 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-1179">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="852cd-1180">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="852cd-1180">Az.OperationalInsights</span></span>
* <span data-ttu-id="852cd-1181">저장된 검색의 기본 버전이 1로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-1181">Updated default version for saved searches to be 1.</span></span>
* <span data-ttu-id="852cd-1182">사용자 지정 로그 null regex 처리가 수정됨</span><span class="sxs-lookup"><span data-stu-id="852cd-1182">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="852cd-1183">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="852cd-1183">Az.RecoveryServices</span></span>
* <span data-ttu-id="852cd-1184">'Get-AzRecoveryServicesBackupJob.md' 업데이트</span><span class="sxs-lookup"><span data-stu-id="852cd-1184">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="852cd-1185">'Get-AzRecoveryServicesBackupContainer.md' 업데이트</span><span class="sxs-lookup"><span data-stu-id="852cd-1185">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="852cd-1186">'Get-AzRecoveryServicesVault.md' 업데이트</span><span class="sxs-lookup"><span data-stu-id="852cd-1186">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="852cd-1187">'Wait-AzRecoveryServicesBackupJob.md' 업데이트</span><span class="sxs-lookup"><span data-stu-id="852cd-1187">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="852cd-1188">'Set-AzRecoveryServicesVaultContext.md' 업데이트</span><span class="sxs-lookup"><span data-stu-id="852cd-1188">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="852cd-1189">'Get-AzRecoveryServicesBackupItem.md' 업데이트</span><span class="sxs-lookup"><span data-stu-id="852cd-1189">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="852cd-1190">'Get-AzRecoveryServicesBackupRecoveryPoint.md' 업데이트</span><span class="sxs-lookup"><span data-stu-id="852cd-1190">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="852cd-1191">'Restore-AzRecoveryServicesBackupItem.md' 업데이트</span><span class="sxs-lookup"><span data-stu-id="852cd-1191">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="852cd-1192">Azure 파일 공유용 컨테이너를 등록 취소하기 위해 서비스 요청 업데이트</span><span class="sxs-lookup"><span data-stu-id="852cd-1192">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="852cd-1193">'Set-AzRecoveryServicesAsrAlertSetting.md' 업데이트</span><span class="sxs-lookup"><span data-stu-id="852cd-1193">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="852cd-1194">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="852cd-1194">Az.Resources</span></span>
- <span data-ttu-id="852cd-1195">'New-AzResourceGroupDeployment' 설명서에서 참조된 누락 cmdlet 제거</span><span class="sxs-lookup"><span data-stu-id="852cd-1195">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="852cd-1196">새 API 버전 2019-01-01을 사용하도록 정책 cmdlet 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="852cd-1196">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="852cd-1197">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="852cd-1197">Az.ServiceBus</span></span>
* <span data-ttu-id="852cd-1198">SAS 토큰을 생성하기 위해 추가된 새로운 cmmdlet 추가: New-AzServiceBusAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="852cd-1198">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="852cd-1199">'관리'만 지정된 경우 authorizationrules 권한에 대한 확인 및 오류 메시지 추가</span><span class="sxs-lookup"><span data-stu-id="852cd-1199">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="852cd-1200">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="852cd-1200">Az.Sql</span></span>
* <span data-ttu-id="852cd-1201">Set-AzSqlDatabaseSecondary cmdlet에 대한 누락된 예제 수정</span><span class="sxs-lookup"><span data-stu-id="852cd-1201">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="852cd-1202">이메일 주소를 제공하지 않고 설정된 취약성 평가 반복 검색 수정</span><span class="sxs-lookup"><span data-stu-id="852cd-1202">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="852cd-1203">경고 메시지의 작은 오타를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-1203">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="852cd-1204">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="852cd-1204">Az.Storage</span></span>
* <span data-ttu-id="852cd-1205">'Get-AzStorageAccount'에 대한 참조 설명서의 예제를 업데이트하여 올바른 매개 변수 이름 사용</span><span class="sxs-lookup"><span data-stu-id="852cd-1205">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="852cd-1206">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="852cd-1206">Az.StorageSync</span></span>
* <span data-ttu-id="852cd-1207">Invoke-AzStorageSyncChangeDetection cmdlet을 추가하는 중입니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-1207">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="852cd-1208">TierFilesOlderThanDays를 기념하는 문제 9551 수정</span><span class="sxs-lookup"><span data-stu-id="852cd-1208">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="852cd-1209">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="852cd-1209">Az.Websites</span></span>
* <span data-ttu-id="852cd-1210">Get-AzWebApp 및 Set-AzWebApp에서 일부 SiteConfig 속성을 반환하지 않은 버그 수정</span><span class="sxs-lookup"><span data-stu-id="852cd-1210">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="852cd-1211">Get-AzDeletedWebApp 및 Restore-AzDeletedWebApp에 새 위치 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="852cd-1211">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="852cd-1212">AzWebApp-IncludeSourceWebAppSlots을 사용하여 웹앱 슬롯을 복제하는 버그를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-1212">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="852cd-1213">2.4.0 - 2019년 7월</span><span class="sxs-lookup"><span data-stu-id="852cd-1213">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="852cd-1214">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="852cd-1214">Az.Accounts</span></span>
* <span data-ttu-id="852cd-1215">프로필 cmdlet에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="852cd-1215">Add support for profile cmdlets</span></span>
* <span data-ttu-id="852cd-1216">생성된 cmdlet에서 환경 및 데이터 평면에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="852cd-1216">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="852cd-1217">Windows PowerShell의 데이터 평면 cmdlet에대해 일부 경우 잘못된 엔드포인트가 사용되는 버그 수정</span><span class="sxs-lookup"><span data-stu-id="852cd-1217">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="852cd-1218">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="852cd-1218">Az.Advisor</span></span>
* <span data-ttu-id="852cd-1219">Az.Advisor의 GA 릴리스</span><span class="sxs-lookup"><span data-stu-id="852cd-1219">GA release of Az.Advisor</span></span>
* <span data-ttu-id="852cd-1220">이 모듈은 이제 롤업 `Az` 모듈의 일부로 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-1220">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="852cd-1221">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="852cd-1221">Az.ApiManagement</span></span>
* <span data-ttu-id="852cd-1222">문제 https://github.com/Azure/azure-powershell/issues/8671 수정</span><span class="sxs-lookup"><span data-stu-id="852cd-1222">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="852cd-1223">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="852cd-1223">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="852cd-1224">사용자 및 제품별 구독을 쿼리하기 위한 지원이 추가됨</span><span class="sxs-lookup"><span data-stu-id="852cd-1224">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="852cd-1225">범위 '/', '/ api, '/ api/echo api'를 사용하여 쿼리하기 위한 지원이 추가됨</span><span class="sxs-lookup"><span data-stu-id="852cd-1225">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="852cd-1226">[https://github.com/Azure/azure-powershell/issues/9307](https://github.com/Azure/azure-powershell/issues/9307 ) 및 https://github.com/Azure/azure-powershell/issues/8432 문제 수정</span><span class="sxs-lookup"><span data-stu-id="852cd-1226">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="852cd-1227">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="852cd-1227">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="852cd-1228">Apis를 가져올 때 'ApiVersion' 및 'ApiVersionSetId'를 지정하기 위한 지원이 추가됨</span><span class="sxs-lookup"><span data-stu-id="852cd-1228">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="852cd-1229">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="852cd-1229">Az.Automation</span></span>
* <span data-ttu-id="852cd-1230">문자열 값을 처리하기 위해 Set-AzAutomationConnectionFieldValue cmdlet 버그를 수정했습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-1230">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="852cd-1231">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="852cd-1231">Az.Compute</span></span>
* <span data-ttu-id="852cd-1232">New-AzImageConfig에 HyperVGeneration 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="852cd-1232">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="852cd-1233">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="852cd-1233">Az.DataFactory</span></span>
* <span data-ttu-id="852cd-1234">get activity runs, get pipeline runs, get trigger runs ADF cmdlet의 출력을 업데이트하여 Select-Object pipe를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-1234">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="852cd-1235">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="852cd-1235">Az.EventGrid</span></span>
* <span data-ttu-id="852cd-1236">'New-AzEventGridSubcription' 설명서의 오타 수정</span><span class="sxs-lookup"><span data-stu-id="852cd-1236">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="852cd-1237">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="852cd-1237">Az.IotHub</span></span>
* <span data-ttu-id="852cd-1238">권한 부여 정책 키를 다시 생성하기 위한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="852cd-1238">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="852cd-1239">Az.Network</span><span class="sxs-lookup"><span data-stu-id="852cd-1239">Az.Network</span></span>
* <span data-ttu-id="852cd-1240">'RoutingPreference'를 공용 IP 태그에 추가함</span><span class="sxs-lookup"><span data-stu-id="852cd-1240">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="852cd-1241">'Get-AzNetworkServiceTag' 참조 설명서의 예제 개선</span><span class="sxs-lookup"><span data-stu-id="852cd-1241">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="852cd-1242">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="852cd-1242">Az.PolicyInsights</span></span>
* <span data-ttu-id="852cd-1243">Get-AzPolicyState의 null 참조 문제 해결</span><span class="sxs-lookup"><span data-stu-id="852cd-1243">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="852cd-1244">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/9446 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="852cd-1244">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="852cd-1245">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="852cd-1245">Az.OperationalInsights</span></span>
* <span data-ttu-id="852cd-1246">Get-AzOperationalInsightsDataSource에 반환된 CustomLog datasource 모델 수정됨</span><span class="sxs-lookup"><span data-stu-id="852cd-1246">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="852cd-1247">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="852cd-1247">Az.RecoveryServices</span></span>
* <span data-ttu-id="852cd-1248">IaaSVMs에 대한 get-policy 명령 수정</span><span class="sxs-lookup"><span data-stu-id="852cd-1248">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="852cd-1249">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="852cd-1249">Az.Resources</span></span>
    - <span data-ttu-id="852cd-1250">Get-AzPolicyState -Top 매개 변수에 대한 도움말 텍스트 수정</span><span class="sxs-lookup"><span data-stu-id="852cd-1250">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="852cd-1251">Get-AzPolicyAlias에 대한 클라이언트 쪽 페이징 지원 추가</span><span class="sxs-lookup"><span data-stu-id="852cd-1251">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="852cd-1252">Set-AzPolicyAssignment, -PolicyParameters 및 -PolicyParametersObject에 대한 새 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="852cd-1252">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="852cd-1253">Policy cmdlet에 대한 몇 가지 문서 및 예제 업데이트</span><span class="sxs-lookup"><span data-stu-id="852cd-1253">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="852cd-1254">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="852cd-1254">Az.ServiceBus</span></span>
* <span data-ttu-id="852cd-1255">문제 #4938 수정 - MaxSizeInMegabytes를 설정할 때 New-AzureRmServiceBusQueue가 BadRequest 반환</span><span class="sxs-lookup"><span data-stu-id="852cd-1255">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="852cd-1256">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="852cd-1256">Az.Sql</span></span>
* <span data-ttu-id="852cd-1257">미리 보기 릴리스에서 공개 릴리스로 인스턴스 장애 조치(Failover) 그룹 cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="852cd-1257">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="852cd-1258">새 cmdlet으로 Azure SQL Server\Database Auditing을 지원하세요.</span><span class="sxs-lookup"><span data-stu-id="852cd-1258">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="852cd-1259">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="852cd-1259">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="852cd-1260">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="852cd-1260">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="852cd-1261">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="852cd-1261">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="852cd-1262">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="852cd-1262">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="852cd-1263">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="852cd-1263">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="852cd-1264">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="852cd-1264">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="852cd-1265">취약성 평가 설정에서 이메일 제약 조건 제거</span><span class="sxs-lookup"><span data-stu-id="852cd-1265">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="852cd-1266">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="852cd-1266">Az.Storage</span></span>
* <span data-ttu-id="852cd-1267">다음 cmdlet에서 2개의 매개 변수 '-IndexDocument' 및 '-ErrorDocument404Path'를 필수에서 선택으로 변경하세요.</span><span class="sxs-lookup"><span data-stu-id="852cd-1267">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="852cd-1268">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="852cd-1268">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="852cd-1269">예제를 추가하여 Get-AzStorageBlobContent의 도움말 업데이트</span><span class="sxs-lookup"><span data-stu-id="852cd-1269">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="852cd-1270">StorageException으로 cmdlet이 실패한 경우 자세한 오류 정보 표시</span><span class="sxs-lookup"><span data-stu-id="852cd-1270">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="852cd-1271">Azure Files AAD DS 인증으로 스토리지 계정 생성 또는 업데이트 지원</span><span class="sxs-lookup"><span data-stu-id="852cd-1271">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="852cd-1272">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="852cd-1272">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="852cd-1273">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="852cd-1273">Set-AzStorageAccount</span></span>
* <span data-ttu-id="852cd-1274">파일 공유, 파일 디렉터리 또는 파일의 목록 지원 또는 파일 핸들 닫기</span><span class="sxs-lookup"><span data-stu-id="852cd-1274">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="852cd-1275">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="852cd-1275">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="852cd-1276">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="852cd-1276">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="852cd-1277">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="852cd-1277">Az.StorageSync</span></span>
* <span data-ttu-id="852cd-1278">이 모듈은 이제 롤업 `Az` 모듈의 일부로 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-1278">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="852cd-1279">2.3.2 - 2019년 6월</span><span class="sxs-lookup"><span data-stu-id="852cd-1279">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="852cd-1280">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="852cd-1280">Az.Accounts</span></span>
* <span data-ttu-id="852cd-1281">함수 호출에 대해 일부 경우 잘못된 URL이 사용되는 버그 수정</span><span class="sxs-lookup"><span data-stu-id="852cd-1281">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="852cd-1282">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/8983 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="852cd-1282">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="852cd-1283">AzureRM에서 Az cmdlet으로의 별칭 문제 해결</span><span class="sxs-lookup"><span data-stu-id="852cd-1283">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="852cd-1284">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="852cd-1284">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="852cd-1285">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="852cd-1285">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="852cd-1286">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="852cd-1286">Az.Compute</span></span>
* <span data-ttu-id="852cd-1287">New-AzVm 및 New-AzVmss 단순 매개 변수 집합은 이제 'ProximityPlacementGroup'매개 변수를 허용합니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-1287">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="852cd-1288">'New-AzVM' 참조 설명서에서 오타 수정</span><span class="sxs-lookup"><span data-stu-id="852cd-1288">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="852cd-1289">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="852cd-1289">Az.Dns</span></span>
* <span data-ttu-id="852cd-1290">'Set-AzDnsZone' 도움말 예제의 오타가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-1290">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="852cd-1291">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="852cd-1291">Az.EventGrid</span></span>
* <span data-ttu-id="852cd-1292">2019-06-01 API 버전을 사용하도록 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-1292">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="852cd-1293">새 cmdlet:</span><span class="sxs-lookup"><span data-stu-id="852cd-1293">New cmdlets:</span></span>
    - <span data-ttu-id="852cd-1294">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="852cd-1294">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="852cd-1295">새 Azure Event Grid 도메인을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-1295">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="852cd-1296">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="852cd-1296">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="852cd-1297">Event Grid 도메인의 세부 정보를 가져오거나 현재 Azure 구독의 모든 Event Grid 도메인 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-1297">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="852cd-1298">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="852cd-1298">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="852cd-1299">Azure Event Grid 도메인을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-1299">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="852cd-1300">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="852cd-1300">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="852cd-1301">Azure Event Grid 도메인에 대한 공유 액세스 키를 다시 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-1301">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="852cd-1302">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="852cd-1302">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="852cd-1303">Event Grid 도메인 이벤트를 게시하는 데 사용되는 공유 액세스 키를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-1303">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="852cd-1304">New-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="852cd-1304">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="852cd-1305">새 Azure Event Grid 도메인 토픽을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-1305">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="852cd-1306">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="852cd-1306">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="852cd-1307">Event Grid 도메인 토픽의 세부 사항을 가져오거나, 현재 Azure의 특정 Event Grid 도메인 아래의 모든 Event Grid 도메인 토픽 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-1307">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span>
    - <span data-ttu-id="852cd-1308">Remove-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="852cd-1308">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="852cd-1309">기존 Azure Event Grid 도메인 토픽을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-1309">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="852cd-1310">다음 Cmdlet이 업데이트 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-1310">Updated cmdlets:</span></span>
    - <span data-ttu-id="852cd-1311">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="852cd-1311">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="852cd-1312">새로운 Event Grid 도메인 및 Event Grid 도메인 토픽에 대한 파이핑을 지원하기 위해 새로운 필수 매개 변수를 추가하여 이러한 리소스 아래에 새 이벤트 구독을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-1312">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="852cd-1313">새로운 Event Grid 도메인 이름 및 Event Grid 도메인 토픽 이름을 지정하기 위해 새로운 필수 매개 변수를 추가하여 이러한 리소스 아래에 새 이벤트 구독을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-1313">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="852cd-1314">기존 매개 변수(예: EndPointType, SubjectBeginsWith 등)를 재사용할 수 있도록 도메인 및 도메인 토픽에 대한 새로운 매개 변수 집합을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-1314">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="852cd-1315">지정을 위한 새로운 선택적 매개 변수를 추가</span><span class="sxs-lookup"><span data-stu-id="852cd-1315">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="852cd-1316">이벤트 구독 만료 날짜,</span><span class="sxs-lookup"><span data-stu-id="852cd-1316">Event subscription expiration date,</span></span>
            - <span data-ttu-id="852cd-1317">고급 필터링 매개 변수.</span><span class="sxs-lookup"><span data-stu-id="852cd-1317">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="852cd-1318">대상으로 servicebusqueue에 대한 새 열거형을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-1318">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="852cd-1319">-IncludedEventType 옵션에서 'All' 사용을 허용하지 않고 다음으로 대체함</span><span class="sxs-lookup"><span data-stu-id="852cd-1319">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span>
    - <span data-ttu-id="852cd-1320">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="852cd-1320">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="852cd-1321">결과 페이지 매김 및 필터링을 지원하는 새로운 선택적 매개 변수(Top, ODataQuery 및 NextLink)를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-1321">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="852cd-1322">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="852cd-1322">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="852cd-1323">Event Grid 도메인 및 Event Grid 도메인 토픽에 대한 파이핑을 지원하기 위해 새로운 필수 매개 변수를 추가하여 이러한 리소스 아래에 기존 이벤트 구독을 제거할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-1323">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="852cd-1324">Event Grid 도메인 이름 및 Event Grid 도메인 토픽 이름을 지정하기 위해 새로운 필수 매개 변수를 추가하여 이러한 리소스 아래에 기존 이벤트 구독을 제거할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-1324">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="852cd-1325">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="852cd-1325">Az.FrontDoor</span></span>
* <span data-ttu-id="852cd-1326">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="852cd-1326">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="852cd-1327">변환 지원 및 새 연산자 자동 완성 값(RegEx)을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-1327">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="852cd-1328">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="852cd-1328">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="852cd-1329">새 자동 완성 값 추가</span><span class="sxs-lookup"><span data-stu-id="852cd-1329">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="852cd-1330">Az.Network</span><span class="sxs-lookup"><span data-stu-id="852cd-1330">Az.Network</span></span>
* <span data-ttu-id="852cd-1331">Microsoft Azure Virtual Network 게이트웨이 리소스에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="852cd-1331">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="852cd-1332">새로운 cmdlet</span><span class="sxs-lookup"><span data-stu-id="852cd-1332">New cmdlets</span></span>
        - <span data-ttu-id="852cd-1333">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="852cd-1333">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="852cd-1334">AvailablePrivateEndpointType 추가</span><span class="sxs-lookup"><span data-stu-id="852cd-1334">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="852cd-1335">새로운 cmdlet</span><span class="sxs-lookup"><span data-stu-id="852cd-1335">New cmdlets</span></span>
        - <span data-ttu-id="852cd-1336">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="852cd-1336">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="852cd-1337">PrivatePrivateLinkService 추가</span><span class="sxs-lookup"><span data-stu-id="852cd-1337">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="852cd-1338">새로운 cmdlet</span><span class="sxs-lookup"><span data-stu-id="852cd-1338">New cmdlets</span></span>
        - <span data-ttu-id="852cd-1339">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="852cd-1339">Get-AzPrivateLinkService</span></span>
        - <span data-ttu-id="852cd-1340">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="852cd-1340">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="852cd-1341">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="852cd-1341">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="852cd-1342">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="852cd-1342">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="852cd-1343">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="852cd-1343">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="852cd-1344">PrivateEndpoint 추가</span><span class="sxs-lookup"><span data-stu-id="852cd-1344">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="852cd-1345">새로운 cmdlet</span><span class="sxs-lookup"><span data-stu-id="852cd-1345">New cmdlets</span></span>
        - <span data-ttu-id="852cd-1346">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="852cd-1346">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="852cd-1347">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="852cd-1347">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="852cd-1348">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="852cd-1348">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="852cd-1349">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="852cd-1349">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="852cd-1350">기능에 대한 새로운 명령이 업데이트됨: VpnConnection 상의 UseLocalAzureIpAddress 플래그</span><span class="sxs-lookup"><span data-stu-id="852cd-1350">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="852cd-1351">New-AzVpnConnection이 업데이트됨: 선택적 매개 변수 -UseLocalAzureIpAddress를 추가하여 로컬 Azure IP 주소가 연결을 시작하는 동안 소스 주소로 사용되어야 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-1351">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="852cd-1352">Set-AzVpnConnection이 업데이트됨: 선택적 매개 변수 -UseLocalAzureIpAddress를 추가하여 로컬 Azure IP 주소가 연결을 시작하는 동안 소스 주소로 사용되어야 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-1352">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="852cd-1353">ExpressRoute 피어링에 읽기 전용 필드 PeeredConnections가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-1353">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="852cd-1354">ExpressRoute에 읽기 전용 필드 GlobalReachEnabled가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-1354">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="852cd-1355">ExpressRouteCircuit 모델에서 AllowGlobalReach 필드의 사용 중단을 부르는 호환성이 손상되는 변경 속성이 추가됨</span><span class="sxs-lookup"><span data-stu-id="852cd-1355">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="852cd-1356">AzApplicationGatewayRedirectConfiguration cmdlet에서 TargetListenerID를 사용하는 중의 8756 오류 문제가 해결됨</span><span class="sxs-lookup"><span data-stu-id="852cd-1356">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="852cd-1357">다시 쓰기 규칙 세트가 설정되지 못하게 하는 New-AzApplicationGatewayPathRuleConfig의 버그를 수정했습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-1357">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="852cd-1358">NetworkInterfaceIpConfiguration에 VirtualNetworkTaps가 표시되는 방식이 수정됨</span><span class="sxs-lookup"><span data-stu-id="852cd-1358">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="852cd-1359">모든 파트를 나열하도록 Cortex Get cmdlet이 수정됨</span><span class="sxs-lookup"><span data-stu-id="852cd-1359">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="852cd-1360">ExpressRouteGateways, VpnGateway에 대한 VirtualHub 참조 생성 수정됨</span><span class="sxs-lookup"><span data-stu-id="852cd-1360">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="852cd-1361">AzureFirewall 및 NatGateway의 가용성 영역에 대한 지원 추가됨</span><span class="sxs-lookup"><span data-stu-id="852cd-1361">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="852cd-1362">Get-AzNetworkServiceTag cmdlet 추가됨</span><span class="sxs-lookup"><span data-stu-id="852cd-1362">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="852cd-1363">Azure Firewall에 대한 여러 공용 IP 주소에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="852cd-1363">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="852cd-1364">New-AzFirewall cmdlet이 업데이트됨:</span><span class="sxs-lookup"><span data-stu-id="852cd-1364">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="852cd-1365">하나 이상의 공용 IP 주소 개체를 허용하는 매개 변수 -PublicIpAddress 추가됨</span><span class="sxs-lookup"><span data-stu-id="852cd-1365">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="852cd-1366">Virtual Network 개체를 허용하는 매개 변수 -VirtualNetwork 추가됨</span><span class="sxs-lookup"><span data-stu-id="852cd-1366">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="852cd-1367">방화벽 개체에 AddPublicIpAddress 및 RemovePublicIpAddress 메서드 추가됨 - 공용 IP 주소 개체를 입력으로 허용</span><span class="sxs-lookup"><span data-stu-id="852cd-1367">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="852cd-1368">매개 변수 -PublicIpName 및 -VirtualNetworkName이 더 이상 사용되지 않음</span><span class="sxs-lookup"><span data-stu-id="852cd-1368">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span>
* <span data-ttu-id="852cd-1369">기능에 대한 새로운 명령이 업데이트됨: VpnClient AAD 인증 옵션을 가상 네트워크 게이트웨이 리소스로 설정했습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-1369">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span>
    - <span data-ttu-id="852cd-1370">New-AzVirtualNetworkGateway가 업데이트됨: 게이트웨이에서 VpnClient AAD 인증 옵션을 설정할 수 있도록 선택적 매개 변수 AadTenantUri, AadAudienceId, AadIssuerUri가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-1370">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="852cd-1371">Set-AzVirtualNetworkGateway가 업데이트됨: 게이트웨이에서 VpnClient AAD 인증 옵션을 설정할 수 있도록 선택적 매개 변수 AadTenantUri, AadAudienceId, AadIssuerUri가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-1371">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="852cd-1372">Set-AzVirtualNetworkGateway가 업데이트됨: 게이트웨이에서 VpnClient AAD 인증 옵션을 제거할 수 있도록 선택적인 스위치 매개 변수 RemoveAadAuthentication이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-1372">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="852cd-1373">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="852cd-1373">Az.OperationalInsights</span></span>
* <span data-ttu-id="852cd-1374">'New-AzureRmOperationalInsightsWorkspace' 명령에서 **pergb2018** 가격 책정 계층 사용</span><span class="sxs-lookup"><span data-stu-id="852cd-1374">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="852cd-1375">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="852cd-1375">Az.Resources</span></span>
* <span data-ttu-id="852cd-1376">추가 템플릿 내보내기 옵션 지원</span><span class="sxs-lookup"><span data-stu-id="852cd-1376">Support for additional Template Export options</span></span>
    - <span data-ttu-id="852cd-1377">Export-AzResourceGroup에 '-SkipResourceNameParameterization' 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="852cd-1377">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="852cd-1378">Export-AzResourceGroup에 '-SkipAllParameterization' 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="852cd-1378">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="852cd-1379">내보낸 리소스 필터링을 위해 Export-AzResourceGroup에 '-Resource' 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="852cd-1379">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="852cd-1380">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="852cd-1380">Az.ServiceFabric</span></span>
* <span data-ttu-id="852cd-1381">일부 경우 잘못된 지문을 가져오는 추가 인증서 ByExistingKeyVault 수정</span><span class="sxs-lookup"><span data-stu-id="852cd-1381">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="852cd-1382">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="852cd-1382">Az.Sql</span></span>
* <span data-ttu-id="852cd-1383">Advanced Threat Protection 스토리지 엔드포인트 접미사 수정</span><span class="sxs-lookup"><span data-stu-id="852cd-1383">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="852cd-1384">Advanced Data Security가 Advanced Threat Protection 정책을 재정의하는 것을 수정</span><span class="sxs-lookup"><span data-stu-id="852cd-1384">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="852cd-1385">고객이 TDE 키를 추가하고 관리되는 인스턴스에 TDE 보호기를 설정할 수 있도록 Management.Sql용 새 Cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="852cd-1385">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="852cd-1386">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="852cd-1386">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="852cd-1387">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="852cd-1387">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="852cd-1388">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="852cd-1388">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="852cd-1389">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="852cd-1389">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="852cd-1390">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="852cd-1390">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="852cd-1391">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="852cd-1391">Az.Storage</span></span>
* <span data-ttu-id="852cd-1392">스토리지 계정 생성 시 종류 FileStorage 및 SkuName Premium_ZRS 지원</span><span class="sxs-lookup"><span data-stu-id="852cd-1392">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="852cd-1393">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="852cd-1393">New-AzStorageAccount</span></span>
* <span data-ttu-id="852cd-1394">BLOB immutability cmdlet의 설명 명확화</span><span class="sxs-lookup"><span data-stu-id="852cd-1394">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="852cd-1395">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="852cd-1395">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="852cd-1396">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="852cd-1396">Az.Websites</span></span>
* <span data-ttu-id="852cd-1397">Get-AzWebAppCertificate를 클라이언트 대신 서버의 리소스 그룹별로 필터링하도록 최적화</span><span class="sxs-lookup"><span data-stu-id="852cd-1397">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="852cd-1398">Get-AzWebAppSnapshot에 -UseDisasterRecovery 스위치 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="852cd-1398">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="852cd-1399">2.2.0 - 2019년 6월</span><span class="sxs-lookup"><span data-stu-id="852cd-1399">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="852cd-1400">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="852cd-1400">Az.Cdn</span></span>
* <span data-ttu-id="852cd-1401">cmdlet에서 2019-04-15 API 버전 기반의 rulesEngine 기능을 지원하도록 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-1401">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="852cd-1402">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="852cd-1402">Az.Compute</span></span>
* <span data-ttu-id="852cd-1403">작업을 시작하여 완료되기 전에 즉시 반환하는 `NoWait` 매개 변수가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-1403">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="852cd-1404">다음 Cmdlet이 업데이트 되었습니다.   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="852cd-1404">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="852cd-1405">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="852cd-1405">Az.EventHub</span></span>
* <span data-ttu-id="852cd-1406">#9231 수정 - Get-AzEventHubNamespace에서 태그를 반환하지 않음</span><span class="sxs-lookup"><span data-stu-id="852cd-1406">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="852cd-1407">#9230 수정 - Get-AzEventHubNamespace에서 ResourceGroupName 대신 ResourceGroup을 반환함</span><span class="sxs-lookup"><span data-stu-id="852cd-1407">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="852cd-1408">Az.Network</span><span class="sxs-lookup"><span data-stu-id="852cd-1408">Az.Network</span></span>
* <span data-ttu-id="852cd-1409">Nat Gateway에 대한 ResourceId 및 InputObject 업데이트</span><span class="sxs-lookup"><span data-stu-id="852cd-1409">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="852cd-1410">ResourceId 및 InputObject에 대한 별칭 추가</span><span class="sxs-lookup"><span data-stu-id="852cd-1410">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="852cd-1411">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="852cd-1411">Az.PolicyInsights</span></span>
* <span data-ttu-id="852cd-1412">Get-AzPolicyEvent에서 Null 참조 문제 해결</span><span class="sxs-lookup"><span data-stu-id="852cd-1412">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="852cd-1413">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="852cd-1413">Az.RecoveryServices</span></span>
* <span data-ttu-id="852cd-1414">IaaSVM 정책 최소 보존 기간(일)이 1에서 7로 변경됨</span><span class="sxs-lookup"><span data-stu-id="852cd-1414">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="852cd-1415">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="852cd-1415">Az.ServiceBus</span></span>
* <span data-ttu-id="852cd-1416">#9182 문제 해결 - Get-AzServiceBusNamespace에서 ResourceGroupName 대신 ResourceGroup을 반환</span><span class="sxs-lookup"><span data-stu-id="852cd-1416">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="852cd-1417">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="852cd-1417">Az.ServiceFabric</span></span>
* <span data-ttu-id="852cd-1418">'Update-AzServiceFabricReliability' 오류 메시지의 오타 수정</span><span class="sxs-lookup"><span data-stu-id="852cd-1418">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="852cd-1419">Service Fabric 명령줄에서 누락된 문자 수정</span><span class="sxs-lookup"><span data-stu-id="852cd-1419">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="852cd-1420">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="852cd-1420">Az.Sql</span></span>
* <span data-ttu-id="852cd-1421">Managed Instance에 대한 AutoDr을 지원하기 위해 New-AzureSqlInstance cmdlet에 대한 DnsZonePartner 매개 변수를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-1421">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="852cd-1422">Get-AzSqlDatabaseSecureConnectionPolicy cmdlet 사용 중단</span><span class="sxs-lookup"><span data-stu-id="852cd-1422">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="852cd-1423">Threat Detection(위협 탐지) cmdlet 이름을 Advanced Threat Protection으로 변경함</span><span class="sxs-lookup"><span data-stu-id="852cd-1423">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="852cd-1424">새 AzSqlInstance -StorageSizeInGB 및 -LicenseType 매개 변수는 이제 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-1424">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="852cd-1425">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="852cd-1425">Az.Websites</span></span>
* <span data-ttu-id="852cd-1426">-WebApp 속성에서 Set-AzWebApp 및 Set-AzWebAppSlot을 사용하면 태그가 제거되는 문제를 해결함</span><span class="sxs-lookup"><span data-stu-id="852cd-1426">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="852cd-1427">2.1.0 - 2019년 5월</span><span class="sxs-lookup"><span data-stu-id="852cd-1427">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="852cd-1428">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="852cd-1428">Az.ApiManagement</span></span>
* <span data-ttu-id="852cd-1429">글로벌 및 API 범위에서 진단을 관리하기 위한 새 cmdlet을 만들었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-1429">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="852cd-1430">**Get-AzApiManagementDiagnostic** - 글로벌 또는 API 범위가 구성된 진단 가져오기</span><span class="sxs-lookup"><span data-stu-id="852cd-1430">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="852cd-1431">**New-AzApiManagementDiagnostic** - 글로벌 범위 또는 API 범위에서 새 진단 만들기</span><span class="sxs-lookup"><span data-stu-id="852cd-1431">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="852cd-1432">**New-AzApiManagementHttpMessageDiagnostic** - 기록할 Headers(헤더) 및 Body Bytes(본문 바이트 수) 크기에 대한 진단 설정 만들기</span><span class="sxs-lookup"><span data-stu-id="852cd-1432">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="852cd-1433">**New-AzApiManagementPipelineDiagnosticSetting** - 게이트웨이로 들어오고 나가는 HTTP 메시지에 대한 진단 설정 만들기</span><span class="sxs-lookup"><span data-stu-id="852cd-1433">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="852cd-1434">**New-AzApiManagementSamplingSetting** - 진단 요청/응답에 대한 샘플링 설정 만들기</span><span class="sxs-lookup"><span data-stu-id="852cd-1434">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="852cd-1435">**Remove-AzApiManagementDiagnostic** - 글로벌 또는 API 범위에서 진단 엔터티 제거</span><span class="sxs-lookup"><span data-stu-id="852cd-1435">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="852cd-1436">**Set-AzApiManagementDiagnostic** - 글로벌 또는 API 범위에서 진단 엔터티 업데이트</span><span class="sxs-lookup"><span data-stu-id="852cd-1436">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="852cd-1437">ApiManagement 서비스에서 캐시를 관리하기 위한 새 cmdlet을 만들었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-1437">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="852cd-1438">**Get-AzApiManagementCache** - 식별자 또는 모든 캐시로 지정된 캐시의 세부 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="852cd-1438">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="852cd-1439">**New-AzApiManagementCache** - 특정 Azure 'region'(지역)에 새 'default'(기본) 캐시 만들기</span><span class="sxs-lookup"><span data-stu-id="852cd-1439">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="852cd-1440">**Remove-AzApiManagementCache** - 캐시 제거</span><span class="sxs-lookup"><span data-stu-id="852cd-1440">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="852cd-1441">**Update-AzApiManagementCache** - 캐시 업데이트</span><span class="sxs-lookup"><span data-stu-id="852cd-1441">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="852cd-1442">API 스키마 관리하기 위한 새 cmdlet을 만들었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-1442">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="852cd-1443">**New-AzApiManagementSchema** - API에 대한 새 스키마 만들기</span><span class="sxs-lookup"><span data-stu-id="852cd-1443">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="852cd-1444">**Get-AzApiManagementSchema** - API에 구성된 스키마 가져오기</span><span class="sxs-lookup"><span data-stu-id="852cd-1444">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="852cd-1445">**Remove-AzApiManagementSchema** - API에 구성된 스키마 제거</span><span class="sxs-lookup"><span data-stu-id="852cd-1445">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="852cd-1446">**Set-AzApiManagementSchema** - API에 구성된 스키마 업데이트</span><span class="sxs-lookup"><span data-stu-id="852cd-1446">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="852cd-1447">사용자 토큰을 생성하기 위한 새 cmdlet을 만들었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-1447">Created new Cmdlet for generating a User Token.</span></span>
    - <span data-ttu-id="852cd-1448">**New-AzApiManagementUserToken** - 기본적으로 8시간 동안 유효한 새 사용자 토큰을 생성합니다. 'GIT' 사용자에 대한 토큰은 이 cmdlet을 사용하여 생성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-1448">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="852cd-1449">네트워크 상태를 검색하기 위한 새 cmdlet을 만들었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-1449">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="852cd-1450">**Get-AzApiManagementNetworkStatus** - API Management 서비스에서 사용하는 리소스의 네트워크 상태 연결을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-1450">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="852cd-1451">ApiManagement 서비스를 가상 네트워크에 배포하고 종속성이 손상되었는지 여부를 확인할 때 유용합니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-1451">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="852cd-1452">**New-AzApiManagement** cmdlet에서 ApiManagement 서비스를 관리하도록 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-1452">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span>
    - <span data-ttu-id="852cd-1453">새 '소비' SKU 지원이 추가됨</span><span class="sxs-lookup"><span data-stu-id="852cd-1453">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="852cd-1454">'소비' SKU에 대해 'EnableClientCertificate' 플래그를 설정하기 위한 지원이 추가됨</span><span class="sxs-lookup"><span data-stu-id="852cd-1454">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="852cd-1455">새 **New-AzApiManagementSslSetting** cmdlet을 사용하면 'Backend(백 엔드)' 및 'Frontend'(프런트 엔드)에서 'TLS/SSL' 설정을 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-1455">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="852cd-1456">또한 ApiManagement 서비스의 'Frontend'에서 '3DES'와 같은 'Ciphers'와 'Http2'와 같은 'ServerProtocols'를 구성하는 데 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-1456">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="852cd-1457">ApiManagement 서비스에서 'DeveloperPortal' 호스트 이름을 구성하기 위한 지원이 추가됨</span><span class="sxs-lookup"><span data-stu-id="852cd-1457">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="852cd-1458">**Get-AzApiManagementSsoToken** cmdlet에서 'PsApiManagement' 개체를 입력으로 사용하도록 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-1458">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="852cd-1459">cmdlet에서 오류 메시지를 인라인으로 표시하도록 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-1459">Updated the cmdlet to display Error Messages inline</span></span>
     > <span data-ttu-id="852cd-1460">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : 오류 코드: ValidationError 오류 메시지: 하나 이상의 필드에 잘못된 값이 있습니다. 오류 세부 정보:    [Code=ValidationError, Message=줄 3, 열 10의 'log-to-eventhub' 요소에 오류가 있습니다.: 로거를 찾지 못함, Target=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="852cd-1460">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="852cd-1461">**Export-AzApiManagementApi** cmdlet에서 API를 'OpenApi 3.0' 형식으로 내보내도록 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-1461">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="852cd-1462">**Import-AzApiManagementApi** cmdlet을 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-1462">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="852cd-1463">'OpenApi 3.0' 문서 사양에서 API 가져오기</span><span class="sxs-lookup"><span data-stu-id="852cd-1463">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="852cd-1464">문서('Swagger', 'Wadl', 'Wsdl', 'OpenApi')에 지정된 'PsApiManagementSchema' 속성 재정의</span><span class="sxs-lookup"><span data-stu-id="852cd-1464">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="852cd-1465">문서에 지정된 'ServiceUrl' 속성 재정의</span><span class="sxs-lookup"><span data-stu-id="852cd-1465">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="852cd-1466">**Get-AzApiManagementPolicy** cmdlet에서 'rawxml'을 사용하여 이스케이프된 비 Xml 'format'(형식)의 정책을 반환하도록 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-1466">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="852cd-1467">**Set-AzApiManagementPolicy** cmdlet에서 'rawxml'을 사용하여 이스케이프된 비 Xml 'format'의 정책을 수락하고, 'xml'을 사용하여 이스케이프된 Xml 'format'의 정책을 수락하도록 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-1467">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="852cd-1468">**New-AzApiManagementApi** cmdlet을 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-1468">Updated cmdlet **New-AzApiManagementApi**</span></span>
    - <span data-ttu-id="852cd-1469">'OpenId' 권한 부여 서버를 사용하여 API 구성</span><span class="sxs-lookup"><span data-stu-id="852cd-1469">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="852cd-1470">'ApiVersionSet'에서 API 만들기</span><span class="sxs-lookup"><span data-stu-id="852cd-1470">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="852cd-1471">'SourceApiId' 및 'SourceApiRevision'을 사용하여 API 복제</span><span class="sxs-lookup"><span data-stu-id="852cd-1471">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="852cd-1472">API 범위에서 'SubscriptionRequired' 구성 가능</span><span class="sxs-lookup"><span data-stu-id="852cd-1472">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="852cd-1473">**Set-AzApiManagementApi** cmdlet을 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-1473">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="852cd-1474">'OpenId' 권한 부여 서버를 사용하여 API 구성</span><span class="sxs-lookup"><span data-stu-id="852cd-1474">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="852cd-1475">API를 'ApiVersionSet'으로 업데이트</span><span class="sxs-lookup"><span data-stu-id="852cd-1475">To updated an API into an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="852cd-1476">API 범위에서 'SubscriptionRequired' 구성 가능</span><span class="sxs-lookup"><span data-stu-id="852cd-1476">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="852cd-1477">**New-AzApiManagementRevision** cmdlet을 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-1477">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="852cd-1478">'SourceApiRevision'을 사용하여 기존 수정 버전 복제(태그, 제품, 작업 및 정책 복사).</span><span class="sxs-lookup"><span data-stu-id="852cd-1478">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="852cd-1479">새 수정 버전은 부모의 'ApiId'를 가정합니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-1479">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="852cd-1480">'ApiRevisionDescription' 제공</span><span class="sxs-lookup"><span data-stu-id="852cd-1480">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="852cd-1481">API 복제 시 'ServiceUrl' 재정의</span><span class="sxs-lookup"><span data-stu-id="852cd-1481">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="852cd-1482">**New-AzApiManagementIdentityProvider** cmdlet을 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-1482">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="852cd-1483">'Authority'를 사용하여 'AAD' 또는 'AADB2C' 구성</span><span class="sxs-lookup"><span data-stu-id="852cd-1483">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="852cd-1484">'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' 및 'PasswordResetPolicy' 설정</span><span class="sxs-lookup"><span data-stu-id="852cd-1484">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="852cd-1485">**New-AzApiManagementSubscription** cmdlet을 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-1485">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="852cd-1486">'Scope' 및 'UserId'를 사용하여 새 SubscriptonModel 설명</span><span class="sxs-lookup"><span data-stu-id="852cd-1486">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="852cd-1487">'ProductId' 및 'UserId'를 사용하여 이전 구독 모델 설명</span><span class="sxs-lookup"><span data-stu-id="852cd-1487">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="852cd-1488">구독 수준에서 'AllowTracing'을 사용하도록 설정하는 지원 추가</span><span class="sxs-lookup"><span data-stu-id="852cd-1488">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="852cd-1489">**Set-AzApiManagementSubscription** cmdlet을 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-1489">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="852cd-1490">'Scope' 및 'UserId'를 사용하여 새 SubscriptonModel 설명</span><span class="sxs-lookup"><span data-stu-id="852cd-1490">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="852cd-1491">'ProductId' 및 'UserId'를 사용하여 이전 구독 모델 설명</span><span class="sxs-lookup"><span data-stu-id="852cd-1491">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="852cd-1492">구독 수준에서 'AllowTracing'을 사용하도록 설정하는 지원 추가</span><span class="sxs-lookup"><span data-stu-id="852cd-1492">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="852cd-1493">다음 cmdlet에서 'ResourceId'를 입력으로 수락하도록 업데이트했습니다</span><span class="sxs-lookup"><span data-stu-id="852cd-1493">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="852cd-1494">'New-AzApiManagementContext'</span><span class="sxs-lookup"><span data-stu-id="852cd-1494">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="852cd-1495">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="852cd-1495">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="852cd-1496">'Get-AzApiManagementApiRelease'</span><span class="sxs-lookup"><span data-stu-id="852cd-1496">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="852cd-1497">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="852cd-1497">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="852cd-1498">'Get-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="852cd-1498">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="852cd-1499">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="852cd-1499">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="852cd-1500">'Get-AzApiManagementAuthorizationServer'</span><span class="sxs-lookup"><span data-stu-id="852cd-1500">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="852cd-1501">'Get-AzApiManagementBackend'</span><span class="sxs-lookup"><span data-stu-id="852cd-1501">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="852cd-1502">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="852cd-1502">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="852cd-1503">'Get-AzApiManagementCertificate'</span><span class="sxs-lookup"><span data-stu-id="852cd-1503">'Get-AzApiManagementCertificate'</span></span>
    - <span data-ttu-id="852cd-1504">'Remove-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="852cd-1504">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="852cd-1505">'Remove-AzApiManagementSubscription'</span><span class="sxs-lookup"><span data-stu-id="852cd-1505">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="852cd-1506">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="852cd-1506">Az.Automation</span></span>
* <span data-ttu-id="852cd-1507">Get-AzAutomationJobOutputRecord에서 JSON 및 Text 레코드 값을 처리하도록 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-1507">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="852cd-1508">문제 https://github.com/Azure/azure-powershell/issues/7977 수정</span><span class="sxs-lookup"><span data-stu-id="852cd-1508">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="852cd-1509">문제 https://github.com/Azure/azure-powershell/issues/8600 수정</span><span class="sxs-lookup"><span data-stu-id="852cd-1509">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="852cd-1510">Start-AzAutomationDscCompilationJob에서 완료될 때까지 기다리지 않고 작업을 바로 시작하도록 변경했습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-1510">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="852cd-1511">문제 https://github.com/Azure/azure-powershell/issues/8347 수정</span><span class="sxs-lookup"><span data-stu-id="852cd-1511">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="852cd-1512">-Name을 사용하면 모든 노드를 반환하는 Get-AzAutomationDscNode 수정.</span><span class="sxs-lookup"><span data-stu-id="852cd-1512">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="852cd-1513">이제 일치하는 노드만 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-1513">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="852cd-1514">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="852cd-1514">Az.Compute</span></span>
* <span data-ttu-id="852cd-1515">ProtectFromScaleIn 및 ProtectFromScaleSetAction 매개 변수를 Update-AzVmssVM cmdlet에 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-1515">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="852cd-1516">'East US'(미국 동부)가 지원되지 않는 경우 이제 New-AzVM wimple 매개 변수 집합에서 기본적으로 사용 가능한 위치를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-1516">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="852cd-1517">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="852cd-1517">Az.DataLakeStore</span></span>
* <span data-ttu-id="852cd-1518">ADLS SDK에서 httpclient를 사용하도록 업데이트하고, 데이터 평면 테스트를 Azure 프레임워크와 통합합니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-1518">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="852cd-1519">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="852cd-1519">Az.Monitor</span></span>
* <span data-ttu-id="852cd-1520">도움말 예제에서 잘못된 매개 변수 이름을 수정했습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-1520">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="852cd-1521">Az.Network</span><span class="sxs-lookup"><span data-stu-id="852cd-1521">Az.Network</span></span>
* <span data-ttu-id="852cd-1522">DisableBgpRoutePropagation 플래그를 유효 경로 테이블 출력에 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-1522">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="852cd-1523">업데이트된 cmdlet:</span><span class="sxs-lookup"><span data-stu-id="852cd-1523">Updated cmdlet:</span></span>
        - <span data-ttu-id="852cd-1524">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="852cd-1524">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="852cd-1525">New-AzApplicationGatewayTrustedRootCertificate 설명서에서 이중 파선을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-1525">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="852cd-1526">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="852cd-1526">Az.Resources</span></span>
* <span data-ttu-id="852cd-1527">할당 거부를 검색하기 위한 새 Get-AzureRmDenyAssignment cmdlet을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-1527">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="852cd-1528">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="852cd-1528">Az.Sql</span></span>
* <span data-ttu-id="852cd-1529">Advanced Threat Protection cmdlet의 이름을 Advanced Data Security로 변경하고, 취약성 평가를 기본적으로 사용하도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-1529">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="852cd-1530">2.0.0 - 2019년 5월</span><span class="sxs-lookup"><span data-stu-id="852cd-1530">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="852cd-1531">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="852cd-1531">Az.Accounts</span></span>
* <span data-ttu-id="852cd-1532">사용자 이름/비밀번호 인증을 사용하여 ADFS 문제를 해결하도록 인증 라이브러리 업데이트</span><span class="sxs-lookup"><span data-stu-id="852cd-1532">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="852cd-1533">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="852cd-1533">Az.CognitiveServices</span></span>
* <span data-ttu-id="852cd-1534">Bing Search 서비스에 대해서만 Bing 면책 조항을 표시하세요.</span><span class="sxs-lookup"><span data-stu-id="852cd-1534">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="852cd-1535">계정 생성 실패 시 오류 개선.</span><span class="sxs-lookup"><span data-stu-id="852cd-1535">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="852cd-1536">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="852cd-1536">Az.Compute</span></span>
* <span data-ttu-id="852cd-1537">근접 배치 그룹 기능</span><span class="sxs-lookup"><span data-stu-id="852cd-1537">Proximity placement group feature.</span></span>
    - <span data-ttu-id="852cd-1538">다음과 같은 새 cmdlet을 추가했습니다.   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="852cd-1538">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="852cd-1539">새 매개 변수 ProximityPlacementGroupId가 다음 cmdlet에 추가됩니다.   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="852cd-1539">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="852cd-1540">New-AzGalleryImageVersion에 StorageAccountType 매개 변수가 추가됩니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-1540">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="852cd-1541">New-AzGalleryImageVersion의 TargetRegion이 StorageAccountType를 포함할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-1541">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="852cd-1542">SkipShutdown 스위치 매개 변수가 Stop-AzVM 및 Stop-AzVmss에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-1542">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>
* <span data-ttu-id="852cd-1543">주요 변경 내용</span><span class="sxs-lookup"><span data-stu-id="852cd-1543">Breaking changes</span></span>
    - <span data-ttu-id="852cd-1544">Set-AzVMBootDiagnostics이 Set-AzVMBootDiagnostic으로 변경됩니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-1544">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="852cd-1545">Export-AzLogAnalyticThrottledRequests이 Export-AzLogAnalyticThrottledRequests로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-1545">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="852cd-1546">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="852cd-1546">Az.DeploymentManager</span></span>
* <span data-ttu-id="852cd-1547">Azure 배포 관리자 cmdlet의 일반적으로 사용 가능한 첫 번째 릴리스</span><span class="sxs-lookup"><span data-stu-id="852cd-1547">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="852cd-1548">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="852cd-1548">Az.Dns</span></span>
* <span data-ttu-id="852cd-1549">자동 DNS 이름 서버 위임</span><span class="sxs-lookup"><span data-stu-id="852cd-1549">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="852cd-1550">DNS 영역 만들기 cmdlet은 추가 선택적 매개 변수로 부모 영역 이름을 허용합니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-1550">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="852cd-1551">새로 생성 된 자식 영역의 부모 영역에 NS 레코드를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-1551">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="852cd-1552">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="852cd-1552">Az.FrontDoor</span></span>
* <span data-ttu-id="852cd-1553">Azure FrontDoor cmdlet의 일반적으로 사용 가능한 첫 번째 릴리스</span><span class="sxs-lookup"><span data-stu-id="852cd-1553">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="852cd-1554">'Waf'를 포함하도록 WAF cmdlet의 이름 바꾸기</span><span class="sxs-lookup"><span data-stu-id="852cd-1554">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="852cd-1555">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="852cd-1555">Az.HDInsight</span></span>
* <span data-ttu-id="852cd-1556">두 개의 cmdlet을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-1556">Removed two cmdlets:</span></span>
    - <span data-ttu-id="852cd-1557">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="852cd-1557">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="852cd-1558">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="852cd-1558">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="852cd-1559">Grant-AzHDInsightHttpServicesAccess를 대체할 새 cmdlet Set-AzHDInsightGatewayCredential을 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-1559">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="852cd-1560">reader 역할과 HDInsight 운영자 역할을 구분하도록 cmdlet Get-AzHDInsightJobOutput 업데이트:</span><span class="sxs-lookup"><span data-stu-id="852cd-1560">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="852cd-1561">reader 역할을 가진 사용자는 'DefaultStorageAccountKey'매개 변수를 명시적으로 지정해야 합니다. 그렇지 않으면 오류가 발생합니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-1561">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="852cd-1562">Hdinsight 운영자 역할을 가진 사용자를 영향을 받지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-1562">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="852cd-1563">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="852cd-1563">Az.Monitor</span></span>
* <span data-ttu-id="852cd-1564">SQR API(예약 쿼리 규칙)용 새 cmdlet</span><span class="sxs-lookup"><span data-stu-id="852cd-1564">New cmdlets for SQR API (Scheduled Query Rule)</span></span>
    - <span data-ttu-id="852cd-1565">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="852cd-1565">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="852cd-1566">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="852cd-1566">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="852cd-1567">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="852cd-1567">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="852cd-1568">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="852cd-1568">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="852cd-1569">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="852cd-1569">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="852cd-1570">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="852cd-1570">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="852cd-1571">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="852cd-1571">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="852cd-1572">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="852cd-1572">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="852cd-1573">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="852cd-1573">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="852cd-1574">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="852cd-1574">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="852cd-1575">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="852cd-1575">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="852cd-1576">SQR API에 대한 [자세한 내용](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules)</span><span class="sxs-lookup"><span data-stu-id="852cd-1576">[More](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="852cd-1577">GenV2(비 클래식) 메트릭 기반 경고 규칙에 대한 cmdlet을 포함하도록 Az.Monitor.md가 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="852cd-1577">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="852cd-1578">Az.Network</span><span class="sxs-lookup"><span data-stu-id="852cd-1578">Az.Network</span></span>
* <span data-ttu-id="852cd-1579">Nat 게이트웨이 리소스에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="852cd-1579">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="852cd-1580">새로운 cmdlet</span><span class="sxs-lookup"><span data-stu-id="852cd-1580">New cmdlets</span></span>
        - <span data-ttu-id="852cd-1581">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="852cd-1581">New-AzNatGateway</span></span>
        - <span data-ttu-id="852cd-1582">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="852cd-1582">Get-AzNatGateway</span></span>
        - <span data-ttu-id="852cd-1583">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="852cd-1583">Set-AzNatGateway</span></span>
        - <span data-ttu-id="852cd-1584">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="852cd-1584">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="852cd-1585">다음 Cmdlet이 업데이트 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-1585">Updated cmdlets</span></span>
        - <span data-ttu-id="852cd-1586">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="852cd-1586">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="852cd-1587">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="852cd-1587">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="852cd-1588">기능에 대한 새로운 명령이 업데이트됨: Brooklyn Gateway에서 사용자 지정 경로 설정/제거.</span><span class="sxs-lookup"><span data-stu-id="852cd-1588">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="852cd-1589">New-AzVirtualNetworkGateway가 업데이트됨: 선택적 매개 변수 -CustomRoute를 추가하여 게이트웨이에서 설정할 사용자 지정 경로로 주소 접두사를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-1589">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="852cd-1590">Set-AzVirtualNetworkGateway가 업데이트됨: 선택적 매개 변수 -CustomRoute를 추가하여 게이트웨이에서 설정할 사용자 지정 경로로 주소 접두사를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-1590">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="852cd-1591">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="852cd-1591">Az.PolicyInsights</span></span>
* <span data-ttu-id="852cd-1592">정책 평가 세부 정보 쿼리 지원</span><span class="sxs-lookup"><span data-stu-id="852cd-1592">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="852cd-1593">Get-AzPolicyState에 '-Expand'매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="852cd-1593">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="852cd-1594">'-Expand PolicyEvaluationDetails' 지원</span><span class="sxs-lookup"><span data-stu-id="852cd-1594">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="852cd-1595">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="852cd-1595">Az.RecoveryServices</span></span>
* <span data-ttu-id="852cd-1596">크로스 구독 Azure에서 Azure 사이트 복구 지원</span><span class="sxs-lookup"><span data-stu-id="852cd-1596">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="852cd-1597">Azure Site Recovery에 대한 호환성이 손상되는 변경 표시</span><span class="sxs-lookup"><span data-stu-id="852cd-1597">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="852cd-1598">Azure Site Recovery 복구 계획 최종 실행 계획에 대한 수정</span><span class="sxs-lookup"><span data-stu-id="852cd-1598">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="852cd-1599">Azure에서 Azure에 대한 Azure Site Recovery 업데이트 네트워크 매핑 수정</span><span class="sxs-lookup"><span data-stu-id="852cd-1599">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="852cd-1600">관리 디스크에 대한 Azure에서 Azure에 대한 Azure Site Recovery 업데이트 보호 방향 수정</span><span class="sxs-lookup"><span data-stu-id="852cd-1600">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="852cd-1601">기타 사소한 수정.</span><span class="sxs-lookup"><span data-stu-id="852cd-1601">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="852cd-1602">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="852cd-1602">Az.Relay</span></span>
* <span data-ttu-id="852cd-1603">고객 관련 메시지의 철자 오류 수정</span><span class="sxs-lookup"><span data-stu-id="852cd-1603">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="852cd-1604">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="852cd-1604">Az.ServiceBus</span></span>
* <span data-ttu-id="852cd-1605">네임스페이스의 NetworkRuleSet에 대한 새 cmdlet가 추가되었습니다</span><span class="sxs-lookup"><span data-stu-id="852cd-1605">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="852cd-1606">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="852cd-1606">Az.Storage</span></span>
* <span data-ttu-id="852cd-1607">저장소 클라이언트 라이브러리 10.0.1로 업그레이드(이 SDK의 모든 개체의 네임스페이스가 'Microsoft.WindowsAzure.Storage. *'에서 'Microsoft.Azure.Storage.* '로 변경됨)</span><span class="sxs-lookup"><span data-stu-id="852cd-1607">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="852cd-1608">새로운 API 버전 2019-04-01을 지원하기 위해 Microsoft.Azure.Management.Storage 11.0.0으로 업그레이드합니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-1608">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="852cd-1609">스토리지 생성 계정의 기본 스토리지 계정 종류가 'Storage'에서 'StorageV2'로 변경됩니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-1609">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="852cd-1610">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="852cd-1610">New-AzStorageAccount</span></span>
* <span data-ttu-id="852cd-1611">'StandardLRS'가 'Standard_LRS'로 변경되는 것과 같이 '-'을 추가하여 입력 SkuName과 정렬되도록 스토리지 계정 cmdlet 출력 Sku.Name을 변경합니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-1611">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="852cd-1612">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="852cd-1612">New-AzStorageAccount</span></span>
    - <span data-ttu-id="852cd-1613">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="852cd-1613">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="852cd-1614">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="852cd-1614">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="852cd-1615">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="852cd-1615">Az.Websites</span></span>
* <span data-ttu-id="852cd-1616">Get-AzWebApp에서 반환한 PSSite 개체에 대해 'Kind'속성이 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-1616">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="852cd-1617">Get-AzWebApp\* 메트릭 및 Get-AzAppServicePlanMetrics가 사용되지 않음으로 표시되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-1617">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="852cd-1618">1.8.0 - 2019년 4월</span><span class="sxs-lookup"><span data-stu-id="852cd-1618">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="852cd-1619">마지막 주 릴리스 이후의 주요 사항</span><span class="sxs-lookup"><span data-stu-id="852cd-1619">Highlights since the last major release</span></span>
* <span data-ttu-id="852cd-1620">`Az` 모듈 일반 공급</span><span class="sxs-lookup"><span data-stu-id="852cd-1620">General availability of `Az` module</span></span>
* <span data-ttu-id="852cd-1621">`Az` 모듈에 대한 자세한 내용은 https://aka.ms/azps-announce 를 방문하세요.</span><span class="sxs-lookup"><span data-stu-id="852cd-1621">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="852cd-1622">Location, ResourceGroup 및 ResourceName 완성자가 추가되었습니다(https://azure.microsoft.com/blog/completers-in-azure-powershell/ ).</span><span class="sxs-lookup"><span data-stu-id="852cd-1622">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="852cd-1623">와일드카드 지원이 Az.Compute 및 Az.Network에 대한 Get cmdlet에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-1623">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="852cd-1624">Windows PowerShell 5.1 전용 대화형 사용자 이름/암호 인증이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-1624">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="852cd-1625">Python 2 Runbook 지원이 Az.Automation에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-1625">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="852cd-1626">Az.LogicApp: 통합 계정 어셈블리 및 일괄 처리 구성을 위한 새로운 cmdlet입니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-1626">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="852cd-1627">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="852cd-1627">Az.Accounts</span></span>
* <span data-ttu-id="852cd-1628">Mac에서 모듈을 올바르게 삭제하기 위해 Uninstall-AzureRm을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-1628">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="852cd-1629">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="852cd-1629">Az.Batch</span></span>
* <span data-ttu-id="852cd-1630">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-1630">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="852cd-1631">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="852cd-1631">Az.Cdn</span></span>
* <span data-ttu-id="852cd-1632">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-1632">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="852cd-1633">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="852cd-1633">Az.CognitiveServices</span></span>
* <span data-ttu-id="852cd-1634">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-1634">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="852cd-1635">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="852cd-1635">Az.Compute</span></span>
* <span data-ttu-id="852cd-1636">디스크의 리소스 ID에 리소스 ID의 소문자 resourcegroups가 있는 경우 AEM 설치 문제 수정</span><span class="sxs-lookup"><span data-stu-id="852cd-1636">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="852cd-1637">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-1637">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="852cd-1638">와일드 카드에 대한 설명서 수정</span><span class="sxs-lookup"><span data-stu-id="852cd-1638">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="852cd-1639">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="852cd-1639">Az.DataFactory</span></span>
* <span data-ttu-id="852cd-1640">NodeCount가 관리형 통합 런타임에 대해 Null이 아닌 경우 SsisProperties를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-1640">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="852cd-1641">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="852cd-1641">Az.DataLakeStore</span></span>
* <span data-ttu-id="852cd-1642">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-1642">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="852cd-1643">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="852cd-1643">Az.EventGrid</span></span>
* <span data-ttu-id="852cd-1644">이벤트 구독 cmdlet 만들기/업데이트를 사용하기 전에 리소스를 만들어야 함을 나타내기 위해 엔드포인트의 도움말 텍스트가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-1644">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="852cd-1645">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="852cd-1645">Az.EventHub</span></span>
* <span data-ttu-id="852cd-1646">네임스페이스의 NetworkRuleSet에 대한 새 cmdlet가 추가되었습니다</span><span class="sxs-lookup"><span data-stu-id="852cd-1646">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="852cd-1647">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="852cd-1647">Az.HDInsight</span></span>
* <span data-ttu-id="852cd-1648">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-1648">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="852cd-1649">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="852cd-1649">Az.IotHub</span></span>
* <span data-ttu-id="852cd-1650">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-1650">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="852cd-1651">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="852cd-1651">Az.KeyVault</span></span>
* <span data-ttu-id="852cd-1652">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-1652">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="852cd-1653">와일드 카드에 대한 설명서 수정</span><span class="sxs-lookup"><span data-stu-id="852cd-1653">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="852cd-1654">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="852cd-1654">Az.MachineLearning</span></span>
* <span data-ttu-id="852cd-1655">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-1655">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="852cd-1656">Az.Media</span><span class="sxs-lookup"><span data-stu-id="852cd-1656">Az.Media</span></span>
* <span data-ttu-id="852cd-1657">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-1657">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="852cd-1658">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="852cd-1658">Az.Monitor</span></span>
  * <span data-ttu-id="852cd-1659">GenV2(비 클래식) 메트릭 기반 경고 규칙에 대한 새 cmdlet</span><span class="sxs-lookup"><span data-stu-id="852cd-1659">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="852cd-1660">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="852cd-1660">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="852cd-1661">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="852cd-1661">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="852cd-1662">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="852cd-1662">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="852cd-1663">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="852cd-1663">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="852cd-1664">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="852cd-1664">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="852cd-1665">모니터 SDK가 버전 0.22.0-preview로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-1665">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="852cd-1666">Az.Network</span><span class="sxs-lookup"><span data-stu-id="852cd-1666">Az.Network</span></span>
* <span data-ttu-id="852cd-1667">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-1667">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="852cd-1668">와일드 카드에 대한 설명서 수정</span><span class="sxs-lookup"><span data-stu-id="852cd-1668">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="852cd-1669">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="852cd-1669">Az.NotificationHubs</span></span>
* <span data-ttu-id="852cd-1670">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-1670">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="852cd-1671">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="852cd-1671">Az.OperationalInsights</span></span>
* <span data-ttu-id="852cd-1672">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-1672">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="852cd-1673">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="852cd-1673">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="852cd-1674">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-1674">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="852cd-1675">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="852cd-1675">Az.RecoveryServices</span></span>
* <span data-ttu-id="852cd-1676">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-1676">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="852cd-1677">Azure VM의 SQL용 테이블 형식이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-1677">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="852cd-1678">AzureFileShare에서 위치를 가져오는 대체 메서드가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-1678">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="852cd-1679">시간대에 따라 SchedulePolicy 개체의 ScheduleRunDays가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-1679">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="852cd-1680">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="852cd-1680">Az.RedisCache</span></span>
* <span data-ttu-id="852cd-1681">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-1681">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="852cd-1682">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="852cd-1682">Az.Resources</span></span>
* <span data-ttu-id="852cd-1683">와일드 카드에 대한 설명서 수정</span><span class="sxs-lookup"><span data-stu-id="852cd-1683">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="852cd-1684">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="852cd-1684">Az.Sql</span></span>
* <span data-ttu-id="852cd-1685">Monitor SDK의 종속성을 공용 코드로 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-1685">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="852cd-1686">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-1686">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="852cd-1687">다중 열 분류 프로세스가 향상되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-1687">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="852cd-1688">기본적으로 Get-AzSqlServerServiceObjective의 응답으로 SKU 속성(SKU 이름, 제품군, 용량)과 테이블 형식을 포함합니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-1688">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="852cd-1689">해당 지역에 기존 서버 없이 위치별로 Get-AzSqlServerServiceObjective를 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-1689">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="852cd-1690">관리형 인스턴스 생성 시 표준 시간대 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-1690">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="852cd-1691">와일드 카드에 대한 설명서 수정</span><span class="sxs-lookup"><span data-stu-id="852cd-1691">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="852cd-1692">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="852cd-1692">Az.Websites</span></span>
* <span data-ttu-id="852cd-1693">실행 시 태그를 제거하지 않도록 Set-AzWebApp 및 Set-AzWebAppSlot를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-1693">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="852cd-1694">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-1694">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="852cd-1695">WebSites SDK가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-1695">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="852cd-1696">PSAppServicePlan에서 AdminSiteName 속성을 제거했습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-1696">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="852cd-1697">1.7.0 - 2019년 4월</span><span class="sxs-lookup"><span data-stu-id="852cd-1697">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="852cd-1698">마지막 주 릴리스 이후의 주요 사항</span><span class="sxs-lookup"><span data-stu-id="852cd-1698">Highlights since the last major release</span></span>
* <span data-ttu-id="852cd-1699">`Az` 모듈 일반 공급</span><span class="sxs-lookup"><span data-stu-id="852cd-1699">General availability of `Az` module</span></span>
* <span data-ttu-id="852cd-1700">`Az` 모듈에 대한 자세한 내용은 https://aka.ms/azps-announce 를 방문하세요.</span><span class="sxs-lookup"><span data-stu-id="852cd-1700">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="852cd-1701">Location, ResourceGroup 및 ResourceName 완성자가 추가되었습니다(https://azure.microsoft.com/blog/completers-in-azure-powershell/ ).</span><span class="sxs-lookup"><span data-stu-id="852cd-1701">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="852cd-1702">와일드카드 지원이 Az.Compute 및 Az.Network에 대한 Get cmdlet에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-1702">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="852cd-1703">Windows PowerShell 5.1 전용 대화형 사용자 이름/암호 인증이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-1703">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="852cd-1704">Python 2 Runbook 지원이 Az.Automation에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-1704">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="852cd-1705">Az.LogicApp: 통합 계정 어셈블리 및 일괄 처리 구성을 위한 새로운 cmdlet입니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-1705">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="852cd-1706">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="852cd-1706">Az.Accounts</span></span>
* <span data-ttu-id="852cd-1707">매개 변수 AzureAnalysisServicesEndpointResourceId를 허용하도록 Add-AzEnvironment 및 Set-AzEnvironment 업데이트</span><span class="sxs-lookup"><span data-stu-id="852cd-1707">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="852cd-1708">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="852cd-1708">Az.AnalysisServices</span></span>
* <span data-ttu-id="852cd-1709">데이터 평면 cmdlet에서 ServiceClient 사용 및 원본 인증 논리 제거</span><span class="sxs-lookup"><span data-stu-id="852cd-1709">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="852cd-1710">호환성이 손상되는 변경을 방지하기 위해 Add-AzureASAccount를 Connect-AzAccount의 래퍼로 만듦</span><span class="sxs-lookup"><span data-stu-id="852cd-1710">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="852cd-1711">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="852cd-1711">Az.Automation</span></span>
* <span data-ttu-id="852cd-1712">포함에 대한 New-AzAutomationSoftwareUpdateConfiguration cmdlet 버그 수정</span><span class="sxs-lookup"><span data-stu-id="852cd-1712">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="852cd-1713">이제 매개 변수 IncludedKbNumber 및 IncludedPackageNameMask가 작동함</span><span class="sxs-lookup"><span data-stu-id="852cd-1713">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="852cd-1714">Azure 자동화 업데이트 관리 동적 그룹에 대한 버그 수정</span><span class="sxs-lookup"><span data-stu-id="852cd-1714">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="852cd-1715">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="852cd-1715">Az.Compute</span></span>
* <span data-ttu-id="852cd-1716">New-AzDiskConfig 및 New-AzSnapshotConfig에 HyperVGeneration 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="852cd-1716">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="852cd-1717">다른 테넌트의 갤러리 이미지를 사용하여 VM을 만들 수 있음</span><span class="sxs-lookup"><span data-stu-id="852cd-1717">Allow VM creation with galley image from other tenants.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="852cd-1718">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="852cd-1718">Az.ContainerInstance</span></span>
* <span data-ttu-id="852cd-1719">후행 빈 인수를 추가한 New-AzContainerGroup의 -Command 매개 변수의 문제 수정</span><span class="sxs-lookup"><span data-stu-id="852cd-1719">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="852cd-1720">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="852cd-1720">Az.DataFactory</span></span>
* <span data-ttu-id="852cd-1721">ADF .Net SDK 버전을 3.0.2로 업데이트</span><span class="sxs-lookup"><span data-stu-id="852cd-1721">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="852cd-1722">RepoConfiguration 관련 설정에 대한 추가 매개 변수로 Set-AzDataFactoryV2 cmdlet을 업데이트</span><span class="sxs-lookup"><span data-stu-id="852cd-1722">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="852cd-1723">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="852cd-1723">Az.Resources</span></span>
* <span data-ttu-id="852cd-1724">'-ResourceId' 또는 '-ResourceGroupName', '-Name' 및 '-ResourceType' 매개 변수를 제공할 때 'Get-AzResource'에 대한 공급자 처리 개선</span><span class="sxs-lookup"><span data-stu-id="852cd-1724">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="852cd-1725">'Test-AzDeployment' 및 'Test-AzResourceGroupDeployment'에 대한 오류 처리 개선</span><span class="sxs-lookup"><span data-stu-id="852cd-1725">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="852cd-1726">배포 유효성 검사 외부에서 발생한 오류를 처리하고 그 대신 명령의 출력에 포함</span><span class="sxs-lookup"><span data-stu-id="852cd-1726">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="852cd-1727">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/6856 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="852cd-1727">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="852cd-1728">배포 cmdlet 세트에 스크립트 및 작업 시나리오에서 프롬프트를 건너뛰는 '-IgnoreDynamicParameters' 스위치 추가</span><span class="sxs-lookup"><span data-stu-id="852cd-1728">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="852cd-1729">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/6856 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="852cd-1729">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="852cd-1730">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="852cd-1730">Az.Sql</span></span>
* <span data-ttu-id="852cd-1731">데이터베이스 데이터 분류 지원</span><span class="sxs-lookup"><span data-stu-id="852cd-1731">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="852cd-1732">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="852cd-1732">Az.Storage</span></span>
* <span data-ttu-id="852cd-1733">매개 변수 -UseConnectedAccount를 사용하여 스토리지 컨텍스트를 만들 때 자세한 오류 보고(단, 로그인 Azure 계정 없이)</span><span class="sxs-lookup"><span data-stu-id="852cd-1733">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="852cd-1734">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="852cd-1734">New-AzStorageContext</span></span>
* <span data-ttu-id="852cd-1735">관리 평면 API를 사용하여 지정한 스토리지 계정의 BLOB 서비스 속성 관리 지원</span><span class="sxs-lookup"><span data-stu-id="852cd-1735">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="852cd-1736">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="852cd-1736">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="852cd-1737">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="852cd-1737">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="852cd-1738">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="852cd-1738">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="852cd-1739">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="852cd-1739">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="852cd-1740">BLOB 및 파일 업로드/다운로드 cmdlet에 대한 -AsJob 지원</span><span class="sxs-lookup"><span data-stu-id="852cd-1740">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="852cd-1741">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="852cd-1741">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="852cd-1742">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="852cd-1742">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="852cd-1743">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="852cd-1743">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="852cd-1744">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="852cd-1744">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="852cd-1745">1.6.0 - 2019년 3월</span><span class="sxs-lookup"><span data-stu-id="852cd-1745">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="852cd-1746">마지막 주 릴리스 이후의 주요 사항</span><span class="sxs-lookup"><span data-stu-id="852cd-1746">Highlights since the last major release</span></span>
* <span data-ttu-id="852cd-1747">`Az` 모듈 일반 공급</span><span class="sxs-lookup"><span data-stu-id="852cd-1747">General availability of `Az` module</span></span>
* <span data-ttu-id="852cd-1748">`Az` 모듈에 대한 자세한 내용은 https://aka.ms/azps-announce 를 방문하세요.</span><span class="sxs-lookup"><span data-stu-id="852cd-1748">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="852cd-1749">Location, ResourceGroup 및 ResourceName 완성자가 추가되었습니다(https://azure.microsoft.com/blog/completers-in-azure-powershell/ ).</span><span class="sxs-lookup"><span data-stu-id="852cd-1749">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="852cd-1750">와일드카드 지원이 Az.Compute 및 Az.Network에 대한 Get cmdlet에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-1750">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="852cd-1751">Windows PowerShell 5.1 전용 대화형 사용자 이름/암호 인증이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-1751">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="852cd-1752">Python 2 Runbook 지원이 Az.Automation에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-1752">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="852cd-1753">Az.LogicApp: 통합 계정 어셈블리 및 일괄 처리 구성을 위한 새로운 cmdlet입니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-1753">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="852cd-1754">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="852cd-1754">Az.Automation</span></span>
* <span data-ttu-id="852cd-1755">Azure 자동화 업데이트 관리에서 변경된 지원 기능은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-1755">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="852cd-1756">동적 그룹화</span><span class="sxs-lookup"><span data-stu-id="852cd-1756">Dynamic grouping</span></span>
    * <span data-ttu-id="852cd-1757">사전 스크립트</span><span class="sxs-lookup"><span data-stu-id="852cd-1757">Pre-Post script</span></span>
    * <span data-ttu-id="852cd-1758">다시 부팅 설정</span><span class="sxs-lookup"><span data-stu-id="852cd-1758">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="852cd-1759">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="852cd-1759">Az.Compute</span></span>
* <span data-ttu-id="852cd-1760">Get-AzVmBootDiagnosticsData의 경로 확인 문제가 해결되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-1760">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="852cd-1761">Compute 클라이언트 라이브러리가 25.0.0으로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-1761">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="852cd-1762">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="852cd-1762">Az.KeyVault</span></span>
* <span data-ttu-id="852cd-1763">와일드카드 지원이 KeyVault cmdlet에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-1763">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="852cd-1764">Az.Network</span><span class="sxs-lookup"><span data-stu-id="852cd-1764">Az.Network</span></span>
* <span data-ttu-id="852cd-1765">Azure Firewall에 대한 위협 인텔리전스 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-1765">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="852cd-1766">Application Gateway 방화벽 정책의 최상위 수준 리소스 및 사용자 지정 규칙이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-1766">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="852cd-1767">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="852cd-1767">Az.RecoveryServices</span></span>
* <span data-ttu-id="852cd-1768">인스턴트 RP를 지원하기 위해 SnapshotRetentionInDays가 Azure VM 정책에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-1768">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="852cd-1769">컨테이너 등록을 취소하는 파이프 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-1769">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="852cd-1770">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="852cd-1770">Az.Resources</span></span>
* <span data-ttu-id="852cd-1771">Get-AzResource 및 Get-AzResourceGroup에 대한 와일드카드 지원을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-1771">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="852cd-1772">ARM에 대한 일반 호출을 수행할 때 사용되는 자격 증명을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-1772">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="852cd-1773">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="852cd-1773">Az.Sql</span></span>
* <span data-ttu-id="852cd-1774">위협 탐지의 cmdlet 매개 변수(ExcludeDetectionType)가 DetectionType에서 string[]으로 변경되어 새 DetectionType이 추가되면 이후의 증명이 되고 자동 완성도 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-1774">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="852cd-1775">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="852cd-1775">Az.Storage</span></span>
* <span data-ttu-id="852cd-1776">스토리지 계정에 대한 관리 정책 가져오기/설정/제거를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-1776">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="852cd-1777">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="852cd-1777">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="852cd-1778">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="852cd-1778">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="852cd-1779">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="852cd-1779">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="852cd-1780">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="852cd-1780">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="852cd-1781">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="852cd-1781">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="852cd-1782">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="852cd-1782">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="852cd-1783">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="852cd-1783">Az.Websites</span></span>
* <span data-ttu-id="852cd-1784">'New-AzWebApp -IncludeSourceWebAppSlots'를 사용하여 모든 슬롯의 복제를 중단하는 ARM 템플릿 버그가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-1784">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span>

## <a name="150---march-2019"></a><span data-ttu-id="852cd-1785">1.5.0 - 2019년 3월</span><span class="sxs-lookup"><span data-stu-id="852cd-1785">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="852cd-1786">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="852cd-1786">Az.Accounts</span></span>
* <span data-ttu-id="852cd-1787">'Register-AzModule' 명령을 추가하여 AutoRest 생성 cmdlet을 지원</span><span class="sxs-lookup"><span data-stu-id="852cd-1787">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="852cd-1788">Connect-AzAccount 예제 업데이트</span><span class="sxs-lookup"><span data-stu-id="852cd-1788">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="852cd-1789">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="852cd-1789">Az.Automation</span></span>
* <span data-ttu-id="852cd-1790">몇몇 Azure Automation cmdlet에서 특정 월별 일정을 검색할 때 발생하는 문제 수정</span><span class="sxs-lookup"><span data-stu-id="852cd-1790">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="852cd-1791">상위 20개 노드를 반환하도록 Get-AzAutomationDscNode를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-1791">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="852cd-1792">이제 모든 노드 반환</span><span class="sxs-lookup"><span data-stu-id="852cd-1792">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="852cd-1793">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="852cd-1793">Az.Cdn</span></span>
* <span data-ttu-id="852cd-1794">사용자 지정 도메인 Https 사용/사용 안 함에 대한 새 Powershell cmdlet이 추가되었으며 기존의 것은 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-1794">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="852cd-1795">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="852cd-1795">Az.Compute</span></span>
* <span data-ttu-id="852cd-1796">Get cmdlet에 와일드 카드 지원 추가</span><span class="sxs-lookup"><span data-stu-id="852cd-1796">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="852cd-1797">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="852cd-1797">Az.DataFactory</span></span>
* <span data-ttu-id="852cd-1798">ADF.Net SDK 버전이 3.0.1로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-1798">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="852cd-1799">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="852cd-1799">Az.LogicApp</span></span>
* <span data-ttu-id="852cd-1800">첫 결과 페이지 검색 시에만 ListWorkflows 수정</span><span class="sxs-lookup"><span data-stu-id="852cd-1800">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="852cd-1801">Az.Network</span><span class="sxs-lookup"><span data-stu-id="852cd-1801">Az.Network</span></span>
* <span data-ttu-id="852cd-1802">Network cmdlet에 와일드 카드 지원 추가</span><span class="sxs-lookup"><span data-stu-id="852cd-1802">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="852cd-1803">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="852cd-1803">Az.RecoveryServices</span></span>
* <span data-ttu-id="852cd-1804">Azure VM 지원에 SQL 서버가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-1804">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="852cd-1805">SDK 업데이트</span><span class="sxs-lookup"><span data-stu-id="852cd-1805">SDK Update</span></span>
* <span data-ttu-id="852cd-1806">VMappContainer 체크 인 Get-ProtectableItem 제거</span><span class="sxs-lookup"><span data-stu-id="852cd-1806">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="852cd-1807">Get ProtectableItem의 매개 변수로 Name과 ServerName이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-1807">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="852cd-1808">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="852cd-1808">Az.Resources</span></span>
* <span data-ttu-id="852cd-1809">`-TemplateObject` 매개 변수를 추가하여 cmdlet을 배포</span><span class="sxs-lookup"><span data-stu-id="852cd-1809">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="852cd-1810">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/2933 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="852cd-1810">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="852cd-1811">`Get-AzResource`의 결과를 `Set-AzResource`(으)로 파이프할 때 발생하는 문제 수정</span><span class="sxs-lookup"><span data-stu-id="852cd-1811">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="852cd-1812">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/8240 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="852cd-1812">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="852cd-1813">실행 시 JSON 데이터 형식 문제 해결 `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="852cd-1813">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="852cd-1814">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/7930 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="852cd-1814">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="852cd-1815">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="852cd-1815">Az.Sql</span></span>
* <span data-ttu-id="852cd-1816">AuditingEndpointsCommunicator를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-1816">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="852cd-1817">새 진단 설정을 생성할 때 에지 사례의 동작을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-1817">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="852cd-1818">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="852cd-1818">Az.Storage</span></span>
* <span data-ttu-id="852cd-1819">스토리지 계정      - New-AzStorageAccount를 생성할 때 종류 BlockBlobStorage를 지원</span><span class="sxs-lookup"><span data-stu-id="852cd-1819">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="852cd-1820">1.4.0 - 2019년 2월</span><span class="sxs-lookup"><span data-stu-id="852cd-1820">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="852cd-1821">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="852cd-1821">Az.AnalysisServices</span></span>
* <span data-ttu-id="852cd-1822">사용되지 않는 AddAzureASAccount cmdlet</span><span class="sxs-lookup"><span data-stu-id="852cd-1822">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="852cd-1823">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="852cd-1823">Az.Automation</span></span>
* <span data-ttu-id="852cd-1824">Import-AzAutomationDscNodeConfiguration 도움말 업데이트</span><span class="sxs-lookup"><span data-stu-id="852cd-1824">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="852cd-1825">Import-AzAutomationDscConfiguration cmdlet 구성 이름 유효성 검사 추가</span><span class="sxs-lookup"><span data-stu-id="852cd-1825">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="852cd-1826">Import-AzAutomationDscConfiguration cmdlet 오류 처리 개선</span><span class="sxs-lookup"><span data-stu-id="852cd-1826">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="852cd-1827">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="852cd-1827">Az.CognitiveServices</span></span>
* <span data-ttu-id="852cd-1828">리소스의 하위 도메인을 지정하는 데 사용되는 New-AzCognitiveServicesAccount에 대한 새 선택적 매개 변수로 CustomSubdomainName이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-1828">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="852cd-1829">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="852cd-1829">Az.Compute</span></span>
* <span data-ttu-id="852cd-1830">ID 매개 변수 집합 문제 해결</span><span class="sxs-lookup"><span data-stu-id="852cd-1830">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="852cd-1831">Name 매개 변수를 제공하지 않으면 Get-AzVMExtension이 설치된 모든 확장을 열거하도록 업데이트</span><span class="sxs-lookup"><span data-stu-id="852cd-1831">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="852cd-1832">Update-AzImage cmdlet에 태그 및 ResourceId 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="852cd-1832">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="852cd-1833">인스턴스 ID가 없는 Get-AzVmssVM과 InstanceView를 사용하면 인스턴스 보기가 있는 VMSS VM을 나열할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-1833">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="852cd-1834">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="852cd-1834">Az.DataLakeStore</span></span>
* <span data-ttu-id="852cd-1835">ADL 삭제된 항목 열거 및 복원에 대한 cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="852cd-1835">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="852cd-1836">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="852cd-1836">Az.EventHub</span></span>
* <span data-ttu-id="852cd-1837">Eventhub의 CaptureDescription 클래스에서 빈 보관을 건너뛰는 새 부울 속성 SkipEmptyArchives가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-1837">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="852cd-1838">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="852cd-1838">Az.KeyVault</span></span>
* <span data-ttu-id="852cd-1839">Set-AzKeyVaultSecret 태그 지정 수정</span><span class="sxs-lookup"><span data-stu-id="852cd-1839">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="852cd-1840">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="852cd-1840">Az.LogicApp</span></span>
* <span data-ttu-id="852cd-1841">통합 계정에 대한 기본 sku 추가</span><span class="sxs-lookup"><span data-stu-id="852cd-1841">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="852cd-1842">XSLT 2.0, XSLT 3.0, Liquid 맵 형식 추가</span><span class="sxs-lookup"><span data-stu-id="852cd-1842">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="852cd-1843">통합 계정 어셈블리에 대한 새 cmdlet</span><span class="sxs-lookup"><span data-stu-id="852cd-1843">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="852cd-1844">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="852cd-1844">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="852cd-1845">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="852cd-1845">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="852cd-1846">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="852cd-1846">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="852cd-1847">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="852cd-1847">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="852cd-1848">통합 계정 일괄 처리 구성에 대한 새 cmdlet</span><span class="sxs-lookup"><span data-stu-id="852cd-1848">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="852cd-1849">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="852cd-1849">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="852cd-1850">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="852cd-1850">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="852cd-1851">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="852cd-1851">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="852cd-1852">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="852cd-1852">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="852cd-1853">논리 앱 SDK를 버전 4.1.0으로 업데이트</span><span class="sxs-lookup"><span data-stu-id="852cd-1853">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="852cd-1854">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="852cd-1854">Az.Monitor</span></span>
* <span data-ttu-id="852cd-1855">Get-AzMetric에 대한 도움말 업데이트</span><span class="sxs-lookup"><span data-stu-id="852cd-1855">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="852cd-1856">Az.Network</span><span class="sxs-lookup"><span data-stu-id="852cd-1856">Az.Network</span></span>
* <span data-ttu-id="852cd-1857">Add-AzApplicationGatewayCustomError에 대한 도움말 예제 업데이트</span><span class="sxs-lookup"><span data-stu-id="852cd-1857">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="852cd-1858">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="852cd-1858">Az.OperationalInsights</span></span>
* <span data-ttu-id="852cd-1859">New 및 Get ApplicationInsights 데이터 소스에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="852cd-1859">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="852cd-1860">지정된 작업 영역에 대한 특정 또는 전체 ApplicationInsights 데이터 원본 가져오기를 지원하기 위한 새로운 'ApplicationInsights' 종류가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-1860">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span>
    - <span data-ttu-id="852cd-1861">지정된 Application-Insights 리소스 매개 변수(구독 ID, resourceGroupName 및 이름)별로 데이터 원본을 만들기 위한 New-AzOperationalInsightsApplicationInsightsDataSource cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-1861">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span>

#### <a name="azresources"></a><span data-ttu-id="852cd-1862">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="852cd-1862">Az.Resources</span></span>
* <span data-ttu-id="852cd-1863">문제 https://github.com/Azure/azure-powershell/issues/8166 수정</span><span class="sxs-lookup"><span data-stu-id="852cd-1863">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="852cd-1864">문제 https://github.com/Azure/azure-powershell/issues/8235 수정</span><span class="sxs-lookup"><span data-stu-id="852cd-1864">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="852cd-1865">문제 https://github.com/Azure/azure-powershell/issues/6219 수정</span><span class="sxs-lookup"><span data-stu-id="852cd-1865">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="852cd-1866">KeyCredentials 반복 만들기를 방지하기 위해 버그 수정</span><span class="sxs-lookup"><span data-stu-id="852cd-1866">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="852cd-1867">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="852cd-1867">Az.Sql</span></span>
* <span data-ttu-id="852cd-1868">SQL DB 하이퍼스케일에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="852cd-1868">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="852cd-1869">복원 요청에서 불필요한 속성을 설정하여 복원이 실패할 수 있는 버그 수정</span><span class="sxs-lookup"><span data-stu-id="852cd-1869">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="852cd-1870">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="852cd-1870">Az.Websites</span></span>
* <span data-ttu-id="852cd-1871">Get-AzWebAppSlotMetrics 내 올바른 예제</span><span class="sxs-lookup"><span data-stu-id="852cd-1871">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="852cd-1872">1.3.0 - 2019년 2월</span><span class="sxs-lookup"><span data-stu-id="852cd-1872">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="852cd-1873">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="852cd-1873">Az.Accounts</span></span>
* <span data-ttu-id="852cd-1874">ClientRuntime 최신 버전 업데이트</span><span class="sxs-lookup"><span data-stu-id="852cd-1874">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="852cd-1875">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="852cd-1875">Az.AnalysisServices</span></span>
<span data-ttu-id="852cd-1876">Az.AnalysisServices 모듈의 전반적인 가용성.</span><span class="sxs-lookup"><span data-stu-id="852cd-1876">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="852cd-1877">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="852cd-1877">Az.Compute</span></span>
* <span data-ttu-id="852cd-1878">AEM 확장: UltraSSD 및 P60, P70, P80 디스크에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="852cd-1878">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="852cd-1879">Set-AzVMBootDiagnostics에 대한 도움말 업데이트</span><span class="sxs-lookup"><span data-stu-id="852cd-1879">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="852cd-1880">Update-AzImage에 대한 도움말 및 예제 업데이트</span><span class="sxs-lookup"><span data-stu-id="852cd-1880">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="852cd-1881">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="852cd-1881">Az.RecoveryServices</span></span>
<span data-ttu-id="852cd-1882">Az.RecoveryServices 모듈의 전반적인 가용성.</span><span class="sxs-lookup"><span data-stu-id="852cd-1882">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="852cd-1883">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="852cd-1883">Az.Resources</span></span>
* <span data-ttu-id="852cd-1884">리소스 그룹 관련 태그 수정</span><span class="sxs-lookup"><span data-stu-id="852cd-1884">Fix tagging for resource groups</span></span>
    - <span data-ttu-id="852cd-1885">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/8166 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="852cd-1885">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="852cd-1886">`Get-AzureRmRoleAssignment`이(가) -ErrorAction을 준수하지 않는 문제 수정</span><span class="sxs-lookup"><span data-stu-id="852cd-1886">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span>
    - <span data-ttu-id="852cd-1887">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/8235 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="852cd-1887">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="852cd-1888">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="852cd-1888">Az.Sql</span></span>
* <span data-ttu-id="852cd-1889">AzSqlDatabaseBackupShortTermRetentionPolicy 가져오기/설정하기 추가</span><span class="sxs-lookup"><span data-stu-id="852cd-1889">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="852cd-1890">SQL cmdlet을 실행할 경우 Azure 계정에 로그인되어 있지 않은 것이 nullref 예외를 초래하는 문제 수정</span><span class="sxs-lookup"><span data-stu-id="852cd-1890">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="852cd-1891">Get-AzSqlCapability의 nullref 예외 수정</span><span class="sxs-lookup"><span data-stu-id="852cd-1891">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="852cd-1892">1.2.1 - 2019년 1월</span><span class="sxs-lookup"><span data-stu-id="852cd-1892">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="852cd-1893">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="852cd-1893">Az.Accounts</span></span>
* <span data-ttu-id="852cd-1894">올바른 인증 버전을 사용하여 릴리스</span><span class="sxs-lookup"><span data-stu-id="852cd-1894">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="852cd-1895">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="852cd-1895">Az.AnalysisServices</span></span>
* <span data-ttu-id="852cd-1896">업데이트된 인증 종속성을 사용하여 릴리스</span><span class="sxs-lookup"><span data-stu-id="852cd-1896">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="852cd-1897">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="852cd-1897">Az.RecoveryServices</span></span>
* <span data-ttu-id="852cd-1898">업데이트된 인증 종속성을 사용하여 릴리스</span><span class="sxs-lookup"><span data-stu-id="852cd-1898">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="852cd-1899">1.2.0 - 2019년 1월</span><span class="sxs-lookup"><span data-stu-id="852cd-1899">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="852cd-1900">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="852cd-1900">Az.Accounts</span></span>
* <span data-ttu-id="852cd-1901">Windows PowerShell 5.1 전용 대화형 사용자 이름/암호 인증 추가</span><span class="sxs-lookup"><span data-stu-id="852cd-1901">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="852cd-1902">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="852cd-1902">Update incorrect online help URLs</span></span>
* <span data-ttu-id="852cd-1903">Uninstall-AzureRm 관련 PS Core에 경고 메시지 추가</span><span class="sxs-lookup"><span data-stu-id="852cd-1903">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="852cd-1904">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="852cd-1904">Az.Aks</span></span>
* <span data-ttu-id="852cd-1905">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="852cd-1905">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="852cd-1906">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="852cd-1906">Az.Automation</span></span>
* <span data-ttu-id="852cd-1907">Python 2 Runbook에 대한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-1907">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="852cd-1908">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="852cd-1908">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="852cd-1909">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="852cd-1909">Az.Cdn</span></span>
* <span data-ttu-id="852cd-1910">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="852cd-1910">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="852cd-1911">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="852cd-1911">Az.Compute</span></span>
* <span data-ttu-id="852cd-1912">Invoke-AzVMReimage cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="852cd-1912">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="852cd-1913">Set-AzVmss에 TempDisk 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="852cd-1913">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="852cd-1914">New-AzVM 경고 메시지 수정</span><span class="sxs-lookup"><span data-stu-id="852cd-1914">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="852cd-1915">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="852cd-1915">Az.ContainerRegistry</span></span>
* <span data-ttu-id="852cd-1916">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="852cd-1916">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="852cd-1917">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="852cd-1917">Az.DataFactory</span></span>
* <span data-ttu-id="852cd-1918">ADF.Net SDK 버전이 3.0.0으로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-1918">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="852cd-1919">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="852cd-1919">Az.DataLakeStore</span></span>
* <span data-ttu-id="852cd-1920">MSI를 사용할 때 ADLS 엔드포인트 문제 수정</span><span class="sxs-lookup"><span data-stu-id="852cd-1920">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="852cd-1921">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/7462 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="852cd-1921">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="852cd-1922">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="852cd-1922">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="852cd-1923">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="852cd-1923">Az.IotHub</span></span>
* <span data-ttu-id="852cd-1924">Add-IotHubRoutingEndpoint cmdlet에 인코딩 형식을 추가하세요.</span><span class="sxs-lookup"><span data-stu-id="852cd-1924">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="852cd-1925">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="852cd-1925">Az.KeyVault</span></span>
* <span data-ttu-id="852cd-1926">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="852cd-1926">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="852cd-1927">Az.Network</span><span class="sxs-lookup"><span data-stu-id="852cd-1927">Az.Network</span></span>
* <span data-ttu-id="852cd-1928">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="852cd-1928">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="852cd-1929">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="852cd-1929">Az.Resources</span></span>
* <span data-ttu-id="852cd-1930">'New-AzADAppCredential' 및 'New-AzADSpCredential' 참조 설명서의 잘못된 예제 수정</span><span class="sxs-lookup"><span data-stu-id="852cd-1930">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="852cd-1931">리소스 그룹 배포 cmdlet 실행 전 '-TemplateFile' 매개 변수 경로가 확인되지 않는 문제 수정</span><span class="sxs-lookup"><span data-stu-id="852cd-1931">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="852cd-1932">Az.Resources: New-AzureRmPolicyDefinition -Mode 기본값에 대한 올바른 설명서</span><span class="sxs-lookup"><span data-stu-id="852cd-1932">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="852cd-1933">Az.Resources: 문제 https://github.com/Azure/azure-powershell/issues/7522 수정</span><span class="sxs-lookup"><span data-stu-id="852cd-1933">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="852cd-1934">Az.Resources: 문제 https://github.com/Azure/azure-powershell/issues/5747 수정</span><span class="sxs-lookup"><span data-stu-id="852cd-1934">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="852cd-1935">'PSResourceGroupDeployment' 개체의 서식 문제 수정</span><span class="sxs-lookup"><span data-stu-id="852cd-1935">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="852cd-1936">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/2123 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="852cd-1936">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="852cd-1937">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="852cd-1937">Az.ServiceFabric</span></span>
* <span data-ttu-id="852cd-1938">인증서가 VMSS 모델에 추가되었는데도 예외가 발생할 경우 롤백합니다. 이는 버그 https://github.com/Azure/service-fabric-issues/issues/932 를 수정하기 위함입니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-1938">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="852cd-1939">일부 오류 메시지를 수정하세요.</span><span class="sxs-lookup"><span data-stu-id="852cd-1939">Fix some error messages.</span></span>
* <span data-ttu-id="852cd-1940">Az로의 마이그레이션을 통해서는 작동하지 않는 New-AzServiceFabriCluster를 위해 기본값 ARM 템플릿을 가진 클러스터 만들기를 수정하세요.</span><span class="sxs-lookup"><span data-stu-id="852cd-1940">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="852cd-1941">확장에서 클러스터 id를 확인하여 클러스터에 해당하는 VMSS에만 추가되도록 클러스터/애플리케이션 인증서 추가를 수정하세요.</span><span class="sxs-lookup"><span data-stu-id="852cd-1941">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="852cd-1942">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="852cd-1942">Az.SignalR</span></span>
* <span data-ttu-id="852cd-1943">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="852cd-1943">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="852cd-1944">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="852cd-1944">Az.Sql</span></span>
* <span data-ttu-id="852cd-1945">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="852cd-1945">Update incorrect online help URLs</span></span>
* <span data-ttu-id="852cd-1946">가능한 값을 가진 LicenseType 매개 변수에 대한 매개 변수 설명이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-1946">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="852cd-1947">유일하게 업데이트된 속성인데 작동하지 않는 관리되는 인스턴스 ID의 업데이트 수정</span><span class="sxs-lookup"><span data-stu-id="852cd-1947">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="852cd-1948">관리되는 인스턴스에서의 사용자 지정 데이터 정렬에 대한 지원</span><span class="sxs-lookup"><span data-stu-id="852cd-1948">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="852cd-1949">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="852cd-1949">Az.Storage</span></span>
* <span data-ttu-id="852cd-1950">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="852cd-1950">Update incorrect online help URLs</span></span>
* <span data-ttu-id="852cd-1951">Premium Storage 계정이 클래식 로깅/메트릭을 지원하지 않기 때문에, Premium Storage 계정의 클래식 로깅/메트릭을 가져올/설정할 때 상세한 오류 메시지를 제공해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-1951">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="852cd-1952">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="852cd-1952">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="852cd-1953">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="852cd-1953">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="852cd-1954">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="852cd-1954">Az.TrafficManager</span></span>
* <span data-ttu-id="852cd-1955">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="852cd-1955">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="852cd-1956">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="852cd-1956">Az.Websites</span></span>
* <span data-ttu-id="852cd-1957">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="852cd-1957">Update incorrect online help URLs</span></span>
* <span data-ttu-id="852cd-1958">앱이 ASE에 호스팅되면 'New-AzWebAppSSLBinding'을 수정하여 올바른 resourcegroup+location에 인증서를 업로드합니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-1958">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="852cd-1959">'New-AzWebAppSSLBinding'을 수정하여 SSL 인증서를 앱에 바인딩하는 데 붙는 태그를 덮어쓰지 않도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-1959">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="852cd-1960">1.1.0 - 2019년 1월</span><span class="sxs-lookup"><span data-stu-id="852cd-1960">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="852cd-1961">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="852cd-1961">Az.Accounts</span></span>
* <span data-ttu-id="852cd-1962">Enable-AzureRmAlias에 'Local' 범위 추가</span><span class="sxs-lookup"><span data-stu-id="852cd-1962">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="852cd-1963">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="852cd-1963">Az.Compute</span></span>
* <span data-ttu-id="852cd-1964">이름이 Restart/Start/Stop/Remove/Set-AzVM과 Save-AzVMImage에 설정된 ID 매개 변수에서 선택 사항이 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-1964">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="852cd-1965">도움말 파일의 ID에 대한 설명이 업데이트 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-1965">Updated the description of ID in help files</span></span>
* <span data-ttu-id="852cd-1966">Az.Accounts 모듈을 사용할 때의 이전 버전과의 호환성 문제를 해결합니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-1966">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="852cd-1967">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="852cd-1967">Az.DataLakeStore</span></span>
* <span data-ttu-id="852cd-1968">SDK 수정을 위해 데이터 평면의 SDK 버전을 1.1.14로 업데이트하세요.</span><span class="sxs-lookup"><span data-stu-id="852cd-1968">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="852cd-1969">getfilestatus 및 liststatus에 대한 음수 acesstime 및 modificationtime 수정, 비동기 취소 토큰 수정</span><span class="sxs-lookup"><span data-stu-id="852cd-1969">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="852cd-1970">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="852cd-1970">Az.EventGrid</span></span>
* <span data-ttu-id="852cd-1971">2019-01-01 API 버전을 사용하도록 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-1971">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="852cd-1972">2019-01-01 API 버전에서 새 시나리오를 지원하도록 다음 cmdlet을 업데이트</span><span class="sxs-lookup"><span data-stu-id="852cd-1972">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="852cd-1973">New-AzureRmEventGridSubscription: 지정을 위한 새로운 선택적 매개 변수를 추가</span><span class="sxs-lookup"><span data-stu-id="852cd-1973">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="852cd-1974">이벤트 Time-to-Live</span><span class="sxs-lookup"><span data-stu-id="852cd-1974">Event Time-To-Live,</span></span>
        - <span data-ttu-id="852cd-1975">이벤트에 대한 최대 배달 시도</span><span class="sxs-lookup"><span data-stu-id="852cd-1975">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="852cd-1976">배달 못한 편지의 엔드포인트입니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-1976">Dead letter endpoint.</span></span>
    - <span data-ttu-id="852cd-1977">Update-AzureRmEventGridSubscription: 지정을 위한 새로운 선택적 매개 변수를 추가</span><span class="sxs-lookup"><span data-stu-id="852cd-1977">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="852cd-1978">이벤트 Time-to-Live</span><span class="sxs-lookup"><span data-stu-id="852cd-1978">Event Time-To-Live,</span></span>
        - <span data-ttu-id="852cd-1979">이벤트에 대한 최대 배달 시도</span><span class="sxs-lookup"><span data-stu-id="852cd-1979">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="852cd-1980">배달 못한 편지의 엔드포인트입니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-1980">Dead letter endpoint.</span></span>
* <span data-ttu-id="852cd-1981">New-AzureRmEventGridSubscription 및 Update-AzureRmEventGridSubscription cmdlet의 EndpointType 옵션에 새 열거형 값(즉, storageQueue 및 hybridConnection)을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-1981">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="852cd-1982">이벤트 구독을 생성 또는 업데이트할 때 사용자가 직접 조치를 취해야 할 경우 경고 메시지를 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-1982">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="852cd-1983">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="852cd-1983">Az.IotHub</span></span>
* <span data-ttu-id="852cd-1984">최신 버전의 Azure IotHub SDK로 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="852cd-1984">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="852cd-1985">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="852cd-1985">Az.LogicApp</span></span>
* <span data-ttu-id="852cd-1986">지정된 이름이 없는 모든 Get-AzLogicApp 목록</span><span class="sxs-lookup"><span data-stu-id="852cd-1986">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="852cd-1987">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="852cd-1987">Az.Resources</span></span>
* <span data-ttu-id="852cd-1988">'Get-AzResource'에 '-ODataQuery'및 '-ResourceId' 매개 변수를 제공할 때 매개 변수 집합 문제 수정</span><span class="sxs-lookup"><span data-stu-id="852cd-1988">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="852cd-1989">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/7875 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="852cd-1989">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="852cd-1990">New/Set-AzPolicyDefinition에서 -Custom 매개 변수 처리 문제 수정</span><span class="sxs-lookup"><span data-stu-id="852cd-1990">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="852cd-1991">New-AzDeployment 설명서에서 오타 수정</span><span class="sxs-lookup"><span data-stu-id="852cd-1991">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="852cd-1992">'New-AzADUser'에 '-MailNickname'매개 변수가 필수 항목으로 지정됨</span><span class="sxs-lookup"><span data-stu-id="852cd-1992">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="852cd-1993">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/8220 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="852cd-1993">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="852cd-1994">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="852cd-1994">Az.SignalR</span></span>
* <span data-ttu-id="852cd-1995">Az.Accounts 모듈을 사용할 때의 이전 버전과의 호환성 문제를 해결합니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-1995">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="852cd-1996">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="852cd-1996">Az.Sql</span></span>
* <span data-ttu-id="852cd-1997">Storage 관리 클라이언트 종속성을 일반적인 SDK 구현으로 변환했습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-1997">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="852cd-1998">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="852cd-1998">Az.Storage</span></span>
* <span data-ttu-id="852cd-1999">Sas Token, OAuth 또는 Anonymous를 사용하여 스토리지 컨텍스트의 StorageAccountName을 실제 스토리지 계정 이름으로 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-1999">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="852cd-2000">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="852cd-2000">New-AzStorageContext</span></span>
* <span data-ttu-id="852cd-2001">'-FullUri' 매개 변수를 사용하여 Blob 스냅샷 개체의 Sas Token을 생성하고 반환된 Uri를 스냅샷 Uri로 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-2001">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="852cd-2002">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="852cd-2002">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="852cd-2003">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="852cd-2003">Az.Websites</span></span>
* <span data-ttu-id="852cd-2004">'Get-AzDeletedWebApp'의 날짜 구문 분석 버그를 수정했습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-2004">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="852cd-2005">Az.Accounts 모듈을 사용할 때의 이전 버전과의 호환성 문제를 해결합니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-2005">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="852cd-2006">1.0.0 - 2018년 12월</span><span class="sxs-lookup"><span data-stu-id="852cd-2006">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="852cd-2007">일반</span><span class="sxs-lookup"><span data-stu-id="852cd-2007">General</span></span>

- <span data-ttu-id="852cd-2008">Az 모듈 일반 공급</span><span class="sxs-lookup"><span data-stu-id="852cd-2008">General Availability of Az Module</span></span>
- <span data-ttu-id="852cd-2009">각 모듈에 대 한 온라인 도움말</span><span class="sxs-lookup"><span data-stu-id="852cd-2009">Online help for each module</span></span>
- <span data-ttu-id="852cd-2010">자세한 내용과 로드맵은 [Az 알림 페이지](https://aka.ms/azps-announce)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="852cd-2010">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="852cd-2011">AzureRM에서 마이그레이션하는 것에 대한 정보는 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="852cd-2011">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="852cd-2012">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="852cd-2012">Az.Accounts</span></span>
- <span data-ttu-id="852cd-2013">Az.Profile에서 변경</span><span class="sxs-lookup"><span data-stu-id="852cd-2013">Changed from Az.Profile</span></span>
- <span data-ttu-id="852cd-2014">프로필 및 컨텍스트 형식에 대한 표 형식 수정</span><span class="sxs-lookup"><span data-stu-id="852cd-2014">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="852cd-2015">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="852cd-2015">Az.ApiManagement</span></span>
- <span data-ttu-id="852cd-2016">#7002에 대한 수정</span><span class="sxs-lookup"><span data-stu-id="852cd-2016">Fixes for #7002</span></span>
- <span data-ttu-id="852cd-2017">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="852cd-2017">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="852cd-2018">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="852cd-2018">Az.Batch</span></span>
- <span data-ttu-id="852cd-2019">`PSComputeNode`의 새로운 `NodeAgentInformation` 속성을 통해 풀의 각 VM에서 실행 중인 Azure Batch 노드 에이전트의 버전을 확인하는 기능이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-2019">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="852cd-2020">`PSDataDisk`에 대한 `Caching` 기본 값은 이제 `None` 대신 `ReadWrite`입니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-2020">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="852cd-2021">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="852cd-2021">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="852cd-2022">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="852cd-2022">Az.Billing</span></span>
- <span data-ttu-id="852cd-2023">청구, 소비 및 UsageAggregates cmdlet 결합 cmdlet에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="852cd-2023">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="852cd-2024">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="852cd-2024">Az.CognitivServices</span></span>
- <span data-ttu-id="852cd-2025">New-AzureRmCognitiveServicesAccount 작업에서 사용 가능한 SkuName 및 Typem에 대한 완성자 추가</span><span class="sxs-lookup"><span data-stu-id="852cd-2025">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="852cd-2026">Get-AzCognitiveServicesAccountSkus에서 GetSkusWithAccountParamSetName 매개 변수 집합을 제거</span><span class="sxs-lookup"><span data-stu-id="852cd-2026">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="852cd-2027">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="852cd-2027">Az.ContainerInstance</span></span>
- <span data-ttu-id="852cd-2028">ManagedIdentity 지원이 추가됨</span><span class="sxs-lookup"><span data-stu-id="852cd-2028">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="852cd-2029">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="852cd-2029">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="852cd-2030">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="852cd-2030">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="852cd-2031">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="852cd-2031">Az.DataLakeStore</span></span>
- <span data-ttu-id="852cd-2032">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="852cd-2032">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="852cd-2033">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="852cd-2033">Az.Monitor</span></span>
- <span data-ttu-id="852cd-2034">Az.Monitor 이름 변경 및 기타 사소한 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="852cd-2034">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="852cd-2035">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="852cd-2035">Az.KeyVault</span></span>
- <span data-ttu-id="852cd-2036">출력 형식에서 사용되지 않는 'PurgeDisabled' 속성 제거</span><span class="sxs-lookup"><span data-stu-id="852cd-2036">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="852cd-2037">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="852cd-2037">Az.MachineLearning</span></span>
- <span data-ttu-id="852cd-2038">Az.MachineLearningCompute 모듈의 cmdlet 포함</span><span class="sxs-lookup"><span data-stu-id="852cd-2038">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="852cd-2039">Az.Media</span><span class="sxs-lookup"><span data-stu-id="852cd-2039">Az.Media</span></span>
- <span data-ttu-id="852cd-2040">New-AzMediaService에서 사용되지 않는 -Tags 별칭이 제거됨</span><span class="sxs-lookup"><span data-stu-id="852cd-2040">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="852cd-2041">Az.Network</span><span class="sxs-lookup"><span data-stu-id="852cd-2041">Az.Network</span></span>
<span data-ttu-id="852cd-2042">Application Gateway에서 RewriteRuleSets를 구성하는 것에 대한 지원이 추가됨</span><span class="sxs-lookup"><span data-stu-id="852cd-2042">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="852cd-2043">추가된 새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-2043">New cmdlets added:</span></span>
        - <span data-ttu-id="852cd-2044">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="852cd-2044">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="852cd-2045">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="852cd-2045">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="852cd-2046">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="852cd-2046">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="852cd-2047">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="852cd-2047">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="852cd-2048">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="852cd-2048">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="852cd-2049">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="852cd-2049">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="852cd-2050">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="852cd-2050">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="852cd-2051">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="852cd-2051">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="852cd-2052">선택적 매개 변수를 사용하도록 cmdlet이 업데이트됨 -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="852cd-2052">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="852cd-2053">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="852cd-2053">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="852cd-2054">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="852cd-2054">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="852cd-2055">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="852cd-2055">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="852cd-2056">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="852cd-2056">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="852cd-2057">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="852cd-2057">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="852cd-2058">New-AzureRmApplicationGatewayUrlPathMapConfig로 ID를 사용하여 Application Gateway에 KeyVault 지원을 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-2058">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="852cd-2059">선택적 매개 변수를 사용하도록 cmdlet이 업데이트됨 -KeyVaultSecretId, -KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="852cd-2059">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="852cd-2060">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="852cd-2060">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="852cd-2061">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="852cd-2061">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="852cd-2062">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="852cd-2062">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="852cd-2063">New-AzApplicationGateway cmdlet이 선택적 매개 변수를 사용하도록 업데이트됨 -UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="852cd-2063">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="852cd-2064">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="852cd-2064">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="852cd-2065">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="852cd-2065">Az.OperationalInsights</span></span>
- <span data-ttu-id="852cd-2066">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="852cd-2066">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="852cd-2067">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="852cd-2067">Az.Profile</span></span>
- <span data-ttu-id="852cd-2068">Az.Accounts에 모듈 이름이 변경됨</span><span class="sxs-lookup"><span data-stu-id="852cd-2068">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="852cd-2069">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="852cd-2069">Az.RecoveryServices</span></span>
- <span data-ttu-id="852cd-2070">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="852cd-2070">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="852cd-2071">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="852cd-2071">Az.Resources</span></span>
- <span data-ttu-id="852cd-2072">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="852cd-2072">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="852cd-2073">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="852cd-2073">Az.ServiceFabric</span></span>
- <span data-ttu-id="852cd-2074">일반 이름과 지문으로 지정 인증서 지원</span><span class="sxs-lookup"><span data-stu-id="852cd-2074">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="852cd-2075">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="852cd-2075">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="852cd-2076">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="852cd-2076">Az.SIgnalR</span></span>
- <span data-ttu-id="852cd-2077">SIgnalR에 대한 PowerShell cmdlet에 대한 일반 공급</span><span class="sxs-lookup"><span data-stu-id="852cd-2077">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="852cd-2078">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="852cd-2078">Az.Sql</span></span>
- <span data-ttu-id="852cd-2079">위협 탐지의 cmdlet에 새로운 Data_Exfiltration 및 Unsafe_Action 검색 유형 추가</span><span class="sxs-lookup"><span data-stu-id="852cd-2079">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="852cd-2080">Sql 감사 cmdlet에 대한 설명서 예제 업데이트</span><span class="sxs-lookup"><span data-stu-id="852cd-2080">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="852cd-2081">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="852cd-2081">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="852cd-2082">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="852cd-2082">Az.Storage</span></span>
- <span data-ttu-id="852cd-2083">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="852cd-2083">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="852cd-2084">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="852cd-2084">Az.Websites</span></span>
- <span data-ttu-id="852cd-2085">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="852cd-2085">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="852cd-2086">0.7.0 - 2018년 12월</span><span class="sxs-lookup"><span data-stu-id="852cd-2086">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="852cd-2087">일반</span><span class="sxs-lookup"><span data-stu-id="852cd-2087">General</span></span>

* <span data-ttu-id="852cd-2088">AzureRM에서 Az 전환 예정에 대한 사소한 변경</span><span class="sxs-lookup"><span data-stu-id="852cd-2088">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="852cd-2089">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="852cd-2089">Az.Compute</span></span>

* <span data-ttu-id="852cd-2090">`New-AzVm(ss)` cmdlet에 대한 간단한 매개 변수 집합에 UltraSSD 및 갤러리 이미지에 대한 지원을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-2090">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="852cd-2091">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="852cd-2091">Az.DataLakeStore</span></span>

* <span data-ttu-id="852cd-2092">ADLS 계정의 도메인의 후행 슬래시를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-2092">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="852cd-2093">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="852cd-2093">Az.FrontDoor</span></span>

* <span data-ttu-id="852cd-2094">일부 끊어진 링크 수정</span><span class="sxs-lookup"><span data-stu-id="852cd-2094">Fixed some broken links</span></span>
    - <span data-ttu-id="852cd-2095">New-AzureRmFrontDoor 및 Set-AzureRmFrontDoor 아티클에서 New-AzureRmFrontDoorHealthProbeSettingObject cmdlet 아티클에 대한 링크가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-2095">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="852cd-2096">New-AzureRmFrontDoorManagedRuleObject 아티클에서 New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet 아티클에 대한 링크가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-2096">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="852cd-2097">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="852cd-2097">Az.RecoveryServices</span></span>

* <span data-ttu-id="852cd-2098">Azure File Share 복원 작업에 클라이언트 측 유효성 검사가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-2098">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="852cd-2099">afs 복원의 경우 storageAccountName 및 storageAccountResourceGroupName을 선택적으로 만들었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-2099">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="852cd-2100">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="852cd-2100">Az.Resources</span></span>

* <span data-ttu-id="852cd-2101">https://github.com/Azure/azure-powershell/issues/7679 에 대한 수정</span><span class="sxs-lookup"><span data-stu-id="852cd-2101">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="852cd-2102">기본 관리자를 요청할 때 구독 범위가 제공되는 경우 Get-AzureRmRoleAssignment를 업데이트하여 구독 범위를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-2102">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="852cd-2103">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="852cd-2103">Az.Sql</span></span>

* <span data-ttu-id="852cd-2104">AzureRM에서 Az 전환 예정에 대한 사소한 변경</span><span class="sxs-lookup"><span data-stu-id="852cd-2104">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="852cd-2105">DotNet 코어에서 Get-AzureRmSqlDatabaseVulnerabilityAssessment를 사용하는 문제 해결</span><span class="sxs-lookup"><span data-stu-id="852cd-2105">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="852cd-2106">SQL 감사 cmdlet과 관련된 도움말 메시지의 설명서가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-2106">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="852cd-2107">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="852cd-2107">Az.Storage</span></span>

* <span data-ttu-id="852cd-2108">New-AzureRmStorageAccount에 -EnableHierarchicalNamespace 추가</span><span class="sxs-lookup"><span data-stu-id="852cd-2108">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="852cd-2109">파일 복사 cmdlet이 -DestContext 입력이 없을 때 대상의 원본 컨텍스트를 다시 사용할 수 없는 문제 수정</span><span class="sxs-lookup"><span data-stu-id="852cd-2109">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="852cd-2110">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="852cd-2110">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="852cd-2111">고정적인 웹 사이트 구성 지원</span><span class="sxs-lookup"><span data-stu-id="852cd-2111">Support Static Website configuration</span></span>
    - <span data-ttu-id="852cd-2112">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="852cd-2112">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="852cd-2113">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="852cd-2113">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="852cd-2114">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="852cd-2114">Az.Websites</span></span>

* <span data-ttu-id="852cd-2115">Set-AzureRmWebApp 및 Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="852cd-2115">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span>
    - <span data-ttu-id="852cd-2116">Windows 및 Linux 컨테이너 응용 프로그램에 탑재할 Azure Storage 경로를 지정하기 위해 새 매개 변수(-AzureStoragePath)가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-2116">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="852cd-2117">새 cmdlet New-AzureRmWebAppAzureStoragePath의 출력을 매개 변수로 사용하여 Azure Storage 경로를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-2117">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="852cd-2118">0.6.1 - 2018년 11월</span><span class="sxs-lookup"><span data-stu-id="852cd-2118">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="852cd-2119">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="852cd-2119">Az.ApiManagement</span></span>
* <span data-ttu-id="852cd-2120">형식 매핑 문제에 대한 종속성 업데이트</span><span class="sxs-lookup"><span data-stu-id="852cd-2120">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="852cd-2121">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="852cd-2121">Az.Automation</span></span>
* <span data-ttu-id="852cd-2122">Azure Automation cmdlet 기반 Swagger</span><span class="sxs-lookup"><span data-stu-id="852cd-2122">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="852cd-2123">업데이트 관리 cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="852cd-2123">Added Update Management cmdlets</span></span>
* <span data-ttu-id="852cd-2124">소스 제어 cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="852cd-2124">Added Source Control cmdlets</span></span>
* <span data-ttu-id="852cd-2125">Remove-AzureRmAutomationHybridWorkerGroup cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="852cd-2125">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="852cd-2126">DSC 노드 등록 명령 수정</span><span class="sxs-lookup"><span data-stu-id="852cd-2126">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="852cd-2127">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="852cd-2127">Az.Compute</span></span>
* <span data-ttu-id="852cd-2128">SystemAssigned ID에 대한 ID 문제 수정</span><span class="sxs-lookup"><span data-stu-id="852cd-2128">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="852cd-2129">형식 매핑 문제에 대한 종속성 업데이트</span><span class="sxs-lookup"><span data-stu-id="852cd-2129">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="852cd-2130">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="852cd-2130">Az.ContainerInstance</span></span>
* <span data-ttu-id="852cd-2131">형식 매핑 문제에 대한 종속성 업데이트</span><span class="sxs-lookup"><span data-stu-id="852cd-2131">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="852cd-2132">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="852cd-2132">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="852cd-2133">마켓플레이스 cmdlet에 대한 예제 설명 업데이트</span><span class="sxs-lookup"><span data-stu-id="852cd-2133">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="852cd-2134">Az.Network</span><span class="sxs-lookup"><span data-stu-id="852cd-2134">Az.Network</span></span>
* <span data-ttu-id="852cd-2135">New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="852cd-2135">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="852cd-2136">지원되는 AzureFirewall 네트워크 프로토콜에 ICMP 다시 추가</span><span class="sxs-lookup"><span data-stu-id="852cd-2136">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="852cd-2137">Test-AzureRmNetworkWatcherConnectivity cmdlet을 업데이트하여 대상 ID, 주소 및 포트 유효성 검사를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-2137">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span>
* <span data-ttu-id="852cd-2138">VirtualNetwork 맵의 메모리 사용 문제 해결</span><span class="sxs-lookup"><span data-stu-id="852cd-2138">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="852cd-2139">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="852cd-2139">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="852cd-2140">보호된 파일 공유에 대한 정책을 수정하는 것에 대해 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-2140">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="852cd-2141">정책 표준 시간대를 대문자로 변환했습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-2141">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="852cd-2142">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="852cd-2142">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="852cd-2143">New-AzureRmRecoveryServicesAsrProtectableItem의 예제 정정</span><span class="sxs-lookup"><span data-stu-id="852cd-2143">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="852cd-2144">형식 매핑 문제에 대한 종속성 업데이트</span><span class="sxs-lookup"><span data-stu-id="852cd-2144">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="852cd-2145">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="852cd-2145">Az.Relay</span></span>
* <span data-ttu-id="852cd-2146">선택적 매개 변수 -KeyValue를 New-AzureRmRelayKey cmdlet에 추가하여 사용자가 KeyValue를 제공할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-2146">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="852cd-2147">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="852cd-2147">Az.Resources</span></span>
* <span data-ttu-id="852cd-2148">`New-AzureRmPolicyAssignment` 및 `Set-AzureRmPolicyAssignment`의 자원 ID 관련 매개 변수에 대한 도움말 문서를 업데이트함</span><span class="sxs-lookup"><span data-stu-id="852cd-2148">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="852cd-2149">-Metadata를 사용하는 New-AzureRmPolicyDefinition에 대한 예제 추가</span><span class="sxs-lookup"><span data-stu-id="852cd-2149">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="852cd-2150">NetStandard의 태그 키에서 대소문자 보존을 허용하도록 수정: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="852cd-2150">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="852cd-2151">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="852cd-2151">Az.ServiceFabric</span></span>
* <span data-ttu-id="852cd-2152">향후 호환성이 손상되는 변경에 대한 사용 중단 메시지 추가</span><span class="sxs-lookup"><span data-stu-id="852cd-2152">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="852cd-2153">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="852cd-2153">Az.Sql</span></span>
* <span data-ttu-id="852cd-2154">Azure Sql Database Managed Instance 및 Azure Sql Managed Database에 CRUD 작업을 위한 새 cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="852cd-2154">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="852cd-2155">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="852cd-2155">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="852cd-2156">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="852cd-2156">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="852cd-2157">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="852cd-2157">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="852cd-2158">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="852cd-2158">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="852cd-2159">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="852cd-2159">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="852cd-2160">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="852cd-2160">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="852cd-2161">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="852cd-2161">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="852cd-2162">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="852cd-2162">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="852cd-2163">서버 또는 데이터베이스에서 확장 감사 정책 관리를 활성화했습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-2163">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="852cd-2164">새 매개 변수(PredicateExpression)가 감사 로그 필터링을 사용하도록 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-2164">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="852cd-2165">Cmdlet이 레거시 클라이언트 대신 SQL 클라이언트를 사용하도록 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-2165">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="852cd-2166">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="852cd-2166">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="852cd-2167">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="852cd-2167">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="852cd-2168">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="852cd-2168">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="852cd-2169">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="852cd-2169">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="852cd-2170">스토리지 계정 이름 매개 변수가 설정된 Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings를 사용할 때의 문제 해결</span><span class="sxs-lookup"><span data-stu-id="852cd-2170">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="852cd-2171">0.5.0 - 2018년 11월</span><span class="sxs-lookup"><span data-stu-id="852cd-2171">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="852cd-2172">일반</span><span class="sxs-lookup"><span data-stu-id="852cd-2172">General</span></span>
* <span data-ttu-id="852cd-2173">많은 핵심 cmdlet에 Resource Completers를 추가하여 대화형으로 cmdlet을 호출할 때 기존 리소스 이름을 탭으로 이동할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-2173">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="852cd-2174">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="852cd-2174">Az.Profile</span></span>
* <span data-ttu-id="852cd-2175">ClientRuntime의 최신 버전을 사용하도록 일반적인 코드를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-2175">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="852cd-2176">Connect-AzAccount cmdlet의 매개 변수 TenantId 이름을 Tenant로 바꾸고 TenantId의 별칭을 추가합니다</span><span class="sxs-lookup"><span data-stu-id="852cd-2176">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="852cd-2177">Connect-AzAccount의 업데이트된 TenantId 설명</span><span class="sxs-lookup"><span data-stu-id="852cd-2177">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="852cd-2178">테넌트 도메인을 제공할 때 실패한 로그인에 대한 오류 메시지 수정</span><span class="sxs-lookup"><span data-stu-id="852cd-2178">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="852cd-2179">테넌트에 구독이 없는 계정의 컨텍스트 이름 충돌 문제 수정</span><span class="sxs-lookup"><span data-stu-id="852cd-2179">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="852cd-2180">MSI를 사용할 때 DataLake 엔드포인트 문제 수정</span><span class="sxs-lookup"><span data-stu-id="852cd-2180">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="852cd-2181">연결되지 않은 경우 'Disconnect-AzAccount'가 throw하는 문제 수정</span><span class="sxs-lookup"><span data-stu-id="852cd-2181">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="852cd-2182">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="852cd-2182">Az.CognitiveServices</span></span>
* <span data-ttu-id="852cd-2183">Get-AzCognitiveServicesAccountSkus 작업을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-2183">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="852cd-2184">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="852cd-2184">Az.Compute</span></span>
* <span data-ttu-id="852cd-2185">Add-AzVmssVMDataDisk 및 Remove-AzVmssVMDataDisk cmdlet를 추가합니다</span><span class="sxs-lookup"><span data-stu-id="852cd-2185">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="852cd-2186">Get-AzVMImage는 AutomaticOSUpgradeProperties를 표시합니다</span><span class="sxs-lookup"><span data-stu-id="852cd-2186">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="852cd-2187">수정된 SetAzVMChefExtension -BootstrapOptions 및 -JsonAttribute option 값이 json 형식으로 설정하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-2187">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="852cd-2188">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="852cd-2188">Az.DataLakeStore</span></span>
* <span data-ttu-id="852cd-2189">DataLake 패키지를 1.1.10으로 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-2189">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="852cd-2190">기본 동시성을 다중 스레드 작업에 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-2190">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="852cd-2191">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="852cd-2191">Az.Insights</span></span>
* <span data-ttu-id="852cd-2192">해결된 문제 #7267(자동 크기 조정 영역)</span><span class="sxs-lookup"><span data-stu-id="852cd-2192">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="852cd-2193">열거된 매개 변수를 제대로 설정하지 않은 새 자동 크기 조정 규칙을 만드는 데 문제가 있습니다(이를 항상 기본값으로 설정함).</span><span class="sxs-lookup"><span data-stu-id="852cd-2193">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="852cd-2194">해결된 문제 # 7513[자세한 정보] Set-AzDiagnosticSetting은 설정을 생성하는 동안 범주를 명시적으로 지정해야 합니다</span><span class="sxs-lookup"><span data-stu-id="852cd-2194">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="852cd-2195">이제 cmdlet은 생성 중에 사용할 범주를 명시적으로 표시할 필요가 없습니다. 즉, 문서화된대로 작동합니다</span><span class="sxs-lookup"><span data-stu-id="852cd-2195">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="852cd-2196">Az.Network</span><span class="sxs-lookup"><span data-stu-id="852cd-2196">Az.Network</span></span>
* <span data-ttu-id="852cd-2197">다음 cmdlet에 대해 PeeringType을 필수 매개 변수로 변경했습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-2197">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="852cd-2198">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="852cd-2198">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="852cd-2199">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="852cd-2199">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="852cd-2200">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="852cd-2200">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="852cd-2201">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="852cd-2201">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="852cd-2202">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="852cd-2202">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="852cd-2203">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="852cd-2203">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="852cd-2204">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="852cd-2204">Az.PolicyInsights</span></span>
* <span data-ttu-id="852cd-2205">추가된 정책 재구성 cmdlet</span><span class="sxs-lookup"><span data-stu-id="852cd-2205">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="852cd-2206">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="852cd-2206">Az.Resources</span></span>
* <span data-ttu-id="852cd-2207">https://github.com/Azure/azure-powershell/issues/7402 에 대한 수정</span><span class="sxs-lookup"><span data-stu-id="852cd-2207">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="852cd-2208">'Get-AzResource'에 대해 '-ResourceId' 매개 변수를 사용하여 리소스 나열 허용</span><span class="sxs-lookup"><span data-stu-id="852cd-2208">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="852cd-2209">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="852cd-2209">Az.ServiceBus</span></span>
* <span data-ttu-id="852cd-2210">마이그레이션 상태를 알 수 있도록 PSServiceBusMigrationConfigurationAttributes에 MigrationState 읽기 전용 속성 추가.</span><span class="sxs-lookup"><span data-stu-id="852cd-2210">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="852cd-2211">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="852cd-2211">Az.ServiceFabric</span></span>
* <span data-ttu-id="852cd-2212">Linux Vmss에 인증서 추가 수정.</span><span class="sxs-lookup"><span data-stu-id="852cd-2212">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="852cd-2213">Add-AzServiceFabricClusterCertificate 수정</span><span class="sxs-lookup"><span data-stu-id="852cd-2213">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="852cd-2214">새 인증서(Azure/service-fabric-issues#932)에서 올바른 지문을 사용.</span><span class="sxs-lookup"><span data-stu-id="852cd-2214">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="852cd-2215">올바르게 예외 표시(Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="852cd-2215">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="852cd-2216">Vmss CreateOrUpdate 작업을 시작하기 전에 'Update-AzServiceFabricDurability'를 수정하여 클러스터 구성 업데이트.</span><span class="sxs-lookup"><span data-stu-id="852cd-2216">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="852cd-2217">0.4.0 - 2018년 10월</span><span class="sxs-lookup"><span data-stu-id="852cd-2217">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="852cd-2218">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="852cd-2218">Az.Profile</span></span>
* <span data-ttu-id="852cd-2219">CloudShell에서 Get-AzSubscription을 사용하여 문제를 해결합니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-2219">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="852cd-2220">ClientRuntime의 최신 버전을 사용하도록 일반적인 코드를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-2220">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="852cd-2221">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="852cd-2221">Az.Compute</span></span>
* <span data-ttu-id="852cd-2222">'New-AzVm'에 대해 간단한 매개 변수를 사용하는 경우 가속화된 네트워킹을 설정하기 위해 새 크기가 VM 크기의 허용 목록에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-2222">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="852cd-2223">모든 cmdlet에 ResourceName 인수 완성자가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-2223">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="852cd-2224">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="852cd-2224">Az.DataLakeStore</span></span>
* <span data-ttu-id="852cd-2225">Virtual Network 규칙에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="852cd-2225">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="852cd-2226">Get-AzDataLakeStoreVirtualNetworkRule: Azure Data Lake Store 가상 네트워크 규칙을 가져오거나 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-2226">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="852cd-2227">Add-AzDataLakeStoreVirtualNetworkRule: 지정된 Data Lake Store 계정에 가상 네트워크 규칙을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-2227">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="852cd-2228">Set-AzDataLakeStoreVirtualNetworkRule: 지정된 Data Lake Store 계정에 지정된 가상 네트워크 규칙을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-2228">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="852cd-2229">Remove-AzDataLakeStoreVirtualNetworkRule: Azure Data Lake Store 가상 네트워크 규칙을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-2229">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="852cd-2230">Az.Network</span><span class="sxs-lookup"><span data-stu-id="852cd-2230">Az.Network</span></span>
* <span data-ttu-id="852cd-2231">Test-AzNetworkWatcherConnectivity cmdlet을 업데이트하고, 백 엔드에 프로토콜 값을 전달합니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-2231">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="852cd-2232">모든 cmdlet에 ResourceName 인수 완성자가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-2232">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="852cd-2233">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="852cd-2233">Az.Resources</span></span>
* <span data-ttu-id="852cd-2234">(기본 프로필에 구독이 없고 범위가 지정되지 않은 경우) 시나리오에서 의미 있는 예외를 추가하여 Get-AzRoleDefinition이 인식할 수 없는 예외를 throw하는 문제를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-2234">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="852cd-2235">또한 기본 매개 변수 집합을 'RoleDefinitionNameParameterSet'으로 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-2235">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="852cd-2236">0.3.0 - 2018년 10월</span><span class="sxs-lookup"><span data-stu-id="852cd-2236">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="852cd-2237">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="852cd-2237">Azure.Storage</span></span>
* <span data-ttu-id="852cd-2238">대상에 메타데이터가 있을 때 Blob/파일이 메타 데이터를 복사하지 않는 문제 수정</span><span class="sxs-lookup"><span data-stu-id="852cd-2238">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="852cd-2239">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="852cd-2239">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="852cd-2240">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="852cd-2240">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="852cd-2241">특정 위치의 스토리지 리소스 사용을 지원하고 글로벌 스토리지 리소스 사용 가져오기는 더 이상 사용되지 않는다는 경고 메시지를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-2241">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="852cd-2242">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="852cd-2242">Get-AzStorageUsage</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="852cd-2243">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="852cd-2243">Az.CognitiveServices</span></span>
* <span data-ttu-id="852cd-2244">기존 계정이 없는 Get-AzCognitiveServicesAccountSkus를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-2244">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="852cd-2245">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="852cd-2245">Az.Compute</span></span>
* <span data-ttu-id="852cd-2246">Get-AzVM -ResourceGroupName <rg>가 필요한 경우 50개가 넘는 결과를 반환하도록 수정</span><span class="sxs-lookup"><span data-stu-id="852cd-2246">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="852cd-2247">'SimpleParameterSet' 예제가 New-AzVmss cmdlet 도움말에 추가됨</span><span class="sxs-lookup"><span data-stu-id="852cd-2247">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="852cd-2248">Azure Disk Encryption 진행률 메시지의 오타를 수정</span><span class="sxs-lookup"><span data-stu-id="852cd-2248">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="852cd-2249">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="852cd-2249">Az.DataFactoryV2</span></span>
* <span data-ttu-id="852cd-2250">ADF.Net SDK 버전을 2.3.0으로 업데이트</span><span class="sxs-lookup"><span data-stu-id="852cd-2250">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="852cd-2251">Az.Network</span><span class="sxs-lookup"><span data-stu-id="852cd-2251">Az.Network</span></span>
* <span data-ttu-id="852cd-2252">NetworkProfile 기능 추가</span><span class="sxs-lookup"><span data-stu-id="852cd-2252">Added NetworkProfile functionality.</span></span> <span data-ttu-id="852cd-2253">추가된 새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-2253">new cmdlets added</span></span>
    - <span data-ttu-id="852cd-2254">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="852cd-2254">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="852cd-2255">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="852cd-2255">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="852cd-2256">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="852cd-2256">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="852cd-2257">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="852cd-2257">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="852cd-2258">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="852cd-2258">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="852cd-2259">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="852cd-2259">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="852cd-2260">서브넷 모델에 서비스 연결 링크 추가</span><span class="sxs-lookup"><span data-stu-id="852cd-2260">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="852cd-2261">New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="852cd-2261">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="852cd-2262">Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="852cd-2262">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="852cd-2263">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="852cd-2263">Az.RedisCache</span></span>
* <span data-ttu-id="852cd-2264">모든 문자열을 Size 매개 변수로 진행되도록 허용</span><span class="sxs-lookup"><span data-stu-id="852cd-2264">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="852cd-2265">PSArgumentCompleter 팝업에 P5 추가</span><span class="sxs-lookup"><span data-stu-id="852cd-2265">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="852cd-2266">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="852cd-2266">Az.Resources</span></span>
* <span data-ttu-id="852cd-2267">-Mode 매개 변수를 Set-AzPolicyDefinition에 추가</span><span class="sxs-lookup"><span data-stu-id="852cd-2267">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="852cd-2268">사용자가 포함된 Origin 작업에서 Get-AzProviderOperation commandlet 버그 수정</span><span class="sxs-lookup"><span data-stu-id="852cd-2268">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="852cd-2269">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="852cd-2269">Az.Sql</span></span>
* <span data-ttu-id="852cd-2270">일부 백업 cmdlet이 현재 azure 구독을 인식하지 않는 문제 해결</span><span class="sxs-lookup"><span data-stu-id="852cd-2270">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="852cd-2271">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="852cd-2271">Az.Websites</span></span>
* <span data-ttu-id="852cd-2272">새 cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - 컨테이너 지속적인 배포 Webhook URL을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-2272">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="852cd-2273">새 cmdlet New-AzWebAppContainerPSSession 및 Enter-WebAppContainerPSSession -  windows 컨테이너 앱에 PowerShell 원격 세션을 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="852cd-2273">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="852cd-2274">0.2.0 - 2018년 9월</span><span class="sxs-lookup"><span data-stu-id="852cd-2274">0.2.0 - September 2018</span></span>
 <span data-ttu-id="852cd-2275">초기 릴리스</span><span class="sxs-lookup"><span data-stu-id="852cd-2275">Initial Release</span></span>
