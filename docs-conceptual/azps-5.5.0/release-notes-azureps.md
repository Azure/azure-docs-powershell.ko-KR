---
title: Azure PowerShell 릴리스 정보
description: Azure PowerShell 모듈의 모든 최신 업데이트에 대해 알아봅니다.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/10/2020
ms.custom: devx-track-azurepowershell
ms.service: azure-powershell
ms.openlocfilehash: 0fe1d2360af5a05953a08eaf3b3eaf0bf5ddcda5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100012203"
---
# <a name="azure-powershell-release-notes"></a><span data-ttu-id="184db-103">Azure PowerShell 릴리스 정보</span><span class="sxs-lookup"><span data-stu-id="184db-103">Azure PowerShell release notes</span></span>

## <a name="550---february-2021"></a><span data-ttu-id="184db-104">5.5.0 - 2021년 2월</span><span class="sxs-lookup"><span data-stu-id="184db-104">5.5.0 - February 2021</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="184db-105">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="184db-105">Az.Accounts</span></span>
* <span data-ttu-id="184db-106">예외에서 CloudError 코드가 추적되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-106">Tracked CloudError code in exception</span></span>
* <span data-ttu-id="184db-107">'Clear-AzContext'가 실행될 때 'ContextCleared' 이벤트가 발생했습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-107">Raised 'ContextCleared' event when 'Clear-AzContext' was executed</span></span>

#### <a name="azaks"></a><span data-ttu-id="184db-108">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="184db-108">Az.Aks</span></span>
* <span data-ttu-id="184db-109">cmdlet 실패에 대한 오류 메시지가 구체화되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-109">Refined error messages of cmdlet failure.</span></span>
* <span data-ttu-id="184db-110">Azure PowerShell 관련 예외를 사용하도록 예외 처리가 업그레이드되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-110">Upgraded exception handling to use Azure PowerShell related exceptions.</span></span>
* <span data-ttu-id="184db-111">사용자가 제공된 서비스 주체를 사용하여 Kubernetes 클러스터를 만들 수 없는 문제가 해결되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-111">Fixed the issue that user could not use provided service principal to create Kubernetes cluster.</span></span> <span data-ttu-id="184db-112">[#13938]</span><span class="sxs-lookup"><span data-stu-id="184db-112">[#13938]</span></span>

#### <a name="azautomation"></a><span data-ttu-id="184db-113">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="184db-113">Az.Automation</span></span>
* <span data-ttu-id="184db-114">'PSCustomObject' 및 'Array' 처리 문제가 해결되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-114">Fixed the issue of processing 'PSCustomObject' and 'Array'.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="184db-115">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="184db-115">Az.Compute</span></span>
* <span data-ttu-id="184db-116">'Set-AzVmExtension' 및 'Add-AzVmssExtension'에 '-EnableAutomaticUpgrade' 매개 변수가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-116">Added parameter '-EnableAutomaticUpgrade' to 'Set-AzVmExtension' and 'Add-AzVmssExtension'.</span></span>
* <span data-ttu-id="184db-117">'Get-AzVMImage' cmdlet 설명서에서 FilterExpression 매개 변수가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-117">Removed FilterExpression parameter from 'Get-AzVMImage' cmdlet documentation.</span></span> 
* <span data-ttu-id="184db-118">ContainerService cmdlet에 사용 중단 메시지가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-118">Added deprecation message to the ContainerService cmdlets:</span></span>
    - <span data-ttu-id="184db-119">'Add-AzureRmContainerServiceAgentPoolProfileCommand'</span><span class="sxs-lookup"><span data-stu-id="184db-119">'Add-AzureRmContainerServiceAgentPoolProfileCommand'</span></span>
    - <span data-ttu-id="184db-120">'Get-AzContainerService'</span><span class="sxs-lookup"><span data-stu-id="184db-120">'Get-AzContainerService'</span></span>
    - <span data-ttu-id="184db-121">'New-AzContainerService'</span><span class="sxs-lookup"><span data-stu-id="184db-121">'New-AzContainerService'</span></span>
    - <span data-ttu-id="184db-122">'New-AzContainerServiceConfig'</span><span class="sxs-lookup"><span data-stu-id="184db-122">'New-AzContainerServiceConfig'</span></span>
    - <span data-ttu-id="184db-123">'Remove-AzContainerService'</span><span class="sxs-lookup"><span data-stu-id="184db-123">'Remove-AzContainerService'</span></span>
    - <span data-ttu-id="184db-124">'Remove-AzContainerServiceAgentPoolProfile'</span><span class="sxs-lookup"><span data-stu-id="184db-124">'Remove-AzContainerServiceAgentPoolProfile'</span></span>
    - <span data-ttu-id="184db-125">'Update-AzContainerService'</span><span class="sxs-lookup"><span data-stu-id="184db-125">'Update-AzContainerService'</span></span>
* <span data-ttu-id="184db-126">'New-AzDiskConfig' 및 'New-AzDiskUpdateConfig'에 '-BurstingEnabled' 매개 변수가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-126">Added parameter '-BurstingEnabled' to 'New-AzDiskConfig' and 'New-AzDiskUpdateConfig'</span></span>
* <span data-ttu-id="184db-127">'Export-AzLogAnalyticThrottledRequest' 및 'Export-AzLogAnalyticRequestRateByInterval' cmdlet에 '-GroupByApplicationId' 및 '-GroupByUserAgent' 매개 변수가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-127">Added '-GroupByApplicationId' and '-GroupByUserAgent' parameters to the 'Export-AzLogAnalyticThrottledRequest' and 'Export-AzLogAnalyticRequestRateByInterval' cmdlets.</span></span>
* <span data-ttu-id="184db-128">'Get-AzVMExtension' cmdlet에 'VMParameterSet' 매개 변수 집합이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-128">Added 'VMParameterSet' parameter set to 'Get-AzVMExtension' cmdlet.</span></span> <span data-ttu-id="184db-129">이 매개 변수 집합에 새 매개 변수 '-VM'이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-129">Added new parameter '-VM' to this parameter set.</span></span> 

#### <a name="azcontainerregistry"></a><span data-ttu-id="184db-130">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="184db-130">Az.ContainerRegistry</span></span>
* <span data-ttu-id="184db-131">지원되는 리포지토리, 매니페스트 및 태그 작업에 cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-131">Added cmdlets to supported repository, manifest, and tag operations:</span></span>
    - <span data-ttu-id="184db-132">'Get-AzContainerRegistryRepository'</span><span class="sxs-lookup"><span data-stu-id="184db-132">'Get-AzContainerRegistryRepository'</span></span>
    - <span data-ttu-id="184db-133">'Update-AzContainerRegistryRepository'</span><span class="sxs-lookup"><span data-stu-id="184db-133">'Update-AzContainerRegistryRepository'</span></span>
    - <span data-ttu-id="184db-134">'Remove-AzContainerRegistryRepository'</span><span class="sxs-lookup"><span data-stu-id="184db-134">'Remove-AzContainerRegistryRepository'</span></span>
    - <span data-ttu-id="184db-135">'Get-AzContainerRegistryManifest'</span><span class="sxs-lookup"><span data-stu-id="184db-135">'Get-AzContainerRegistryManifest'</span></span>
    - <span data-ttu-id="184db-136">'Update-AzContainerRegistryManifest'</span><span class="sxs-lookup"><span data-stu-id="184db-136">'Update-AzContainerRegistryManifest'</span></span>
    - <span data-ttu-id="184db-137">'Remove-AzContainerRegistryManifest'</span><span class="sxs-lookup"><span data-stu-id="184db-137">'Remove-AzContainerRegistryManifest'</span></span>
    - <span data-ttu-id="184db-138">'Get-AzContainerRegistryTag'</span><span class="sxs-lookup"><span data-stu-id="184db-138">'Get-AzContainerRegistryTag'</span></span>
    - <span data-ttu-id="184db-139">'Update-AzContainerRegistryTag'</span><span class="sxs-lookup"><span data-stu-id="184db-139">'Update-AzContainerRegistryTag'</span></span>
    - <span data-ttu-id="184db-140">'Remove-AzContainerRegistryTag'</span><span class="sxs-lookup"><span data-stu-id="184db-140">'Remove-AzContainerRegistryTag'</span></span>

#### <a name="azdatabricks"></a><span data-ttu-id="184db-141">Az.Databricks</span><span class="sxs-lookup"><span data-stu-id="184db-141">Az.Databricks</span></span>
<span data-ttu-id="184db-142">Databricks 작업 영역을 만들 때 -EnableNoPublicIP가 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="184db-142">Supported -EnableNoPublicIP when creating a Databricks workspace</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="184db-143">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="184db-143">Az.FrontDoor</span></span>
* <span data-ttu-id="184db-144">속성에 FrontDoorId가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-144">Added FrontDoorId to properties</span></span>
* <span data-ttu-id="184db-145">관리형 규칙에 JSON 제외 및 RequestBodyCheck 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-145">Added JSON Exclusions and RequestBodyCheck support to managed rules</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="184db-146">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="184db-146">Az.HDInsight</span></span>
* <span data-ttu-id="184db-147">컴퓨팅 격리 기능을 지원하기 위해 'New-AzHDInsightCluster' cmdlet에 새 매개 변수 '-EnableComputeIsolation' 및 '-ComputeIsolationHostSku'가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-147">Added new parameter '-EnableComputeIsolation' and '-ComputeIsolationHostSku' to the cmdlet 'New-AzHDInsightCluster' to support compute isolation feature</span></span>
* <span data-ttu-id="184db-148">AzureHDInsightCluster 클래스에 'ComputeIsolationProperties' 및 'ConnectivityEndpoints' 속성이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-148">Added property 'ComputeIsolationProperties' and 'ConnectivityEndpoints' in the class AzureHDInsightCluster.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="184db-149">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="184db-149">Az.KeyVault</span></span>
* <span data-ttu-id="184db-150">BYOK 파일을 통해 키를 가져올 때 키 유형 및 곡선 이름을 지정하는 기능이 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="184db-150">Supported specifying key type and curve name when importing keys via a BYOK file</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="184db-151">Az.Network</span><span class="sxs-lookup"><span data-stu-id="184db-151">Az.Network</span></span>
* <span data-ttu-id="184db-152">'가상 라우터'라는 이전 제품 이름을 향후에 '경로 서버'라는 새 이름으로 바꾸기 위해 새 cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-152">Added new cmdlets to replace old product name 'virtual router' with new name 'route server' in the future.</span></span>
    - <span data-ttu-id="184db-153">'New-AzRouteServer'</span><span class="sxs-lookup"><span data-stu-id="184db-153">'New-AzRouteServer'</span></span>
    - <span data-ttu-id="184db-154">'Get-AzRouteServer'</span><span class="sxs-lookup"><span data-stu-id="184db-154">'Get-AzRouteServer'</span></span>
    - <span data-ttu-id="184db-155">'Remove-AzRouteServer'</span><span class="sxs-lookup"><span data-stu-id="184db-155">'Remove-AzRouteServer'</span></span>
    - <span data-ttu-id="184db-156">'Update-AzRouteServer'</span><span class="sxs-lookup"><span data-stu-id="184db-156">'Update-AzRouteServer'</span></span>
    - <span data-ttu-id="184db-157">'Get-AzRouteServerPeer'</span><span class="sxs-lookup"><span data-stu-id="184db-157">'Get-AzRouteServerPeer'</span></span>
    - <span data-ttu-id="184db-158">'Add-AzRouteServerPeer'</span><span class="sxs-lookup"><span data-stu-id="184db-158">'Add-AzRouteServerPeer'</span></span>
    - <span data-ttu-id="184db-159">'Update-AzRouteServerPeer'</span><span class="sxs-lookup"><span data-stu-id="184db-159">'Update-AzRouteServerPeer'</span></span>
    - <span data-ttu-id="184db-160">'Remove-AzRouteServerPeer'</span><span class="sxs-lookup"><span data-stu-id="184db-160">'Remove-AzRouteServerPeer'</span></span>
    - <span data-ttu-id="184db-161">이전 cmdlet에 사용 중단 특성 경고가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-161">Added deprecation attribute warning to the old cmdlets.</span></span>
* <span data-ttu-id="184db-162">ExpressRouteLink MacSecConfig의 버그가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-162">Bug fix in ExpressRouteLink MacSecConfig.</span></span> <span data-ttu-id="184db-163">'PSExpressRouteLinkMacSecConfig'에 새 속성 'SciState'가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-163">Added new property 'SciState' to 'PSExpressRouteLinkMacSecConfig'</span></span>
* <span data-ttu-id="184db-164">Get-AzVirtualNetworkGatewayConnectionIkeSa의 서식 목록 및 서식 테이블 뷰가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-164">Updated format list and format table views for Get-AzVirtualNetworkGatewayConnectionIkeSa</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="184db-165">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="184db-165">Az.PolicyInsights</span></span>
* <span data-ttu-id="184db-166">PowerShell에서 변경 내용이 취소되어 요청 행 한도가 증가했습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-166">Retracted changes made in powershell that increased request row limit.</span></span> <span data-ttu-id="184db-167">잘못된 페이징 지원 문이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-167">Removed incorrect statement of supporting paging</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="184db-168">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="184db-168">Az.RecoveryServices</span></span>
* <span data-ttu-id="184db-169">백업 서비스별 정책 유효성 검사 한도가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-169">modified policy validation limits as per backup service.</span></span>
* <span data-ttu-id="184db-170">복구 서비스 자격 증명 모음에 대한 영역 중복이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-170">Added Zone Redundancy for Recovery Service Vaults.</span></span> 
* <span data-ttu-id="184db-171">VMware-Azure 및 HyperV-Azure 공급자를 위한 근접 배치 그룹에 Azure Site Recovery가 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="184db-171">Azure Site Recovery support for Proximity placement group for VMware to Azure and HyperV to Azure providers.</span></span>
* <span data-ttu-id="184db-172">VMware-Azure 및 HyperV-Azure 공급자를 위한 가용성 영역에 Azure Site Recovery가 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="184db-172">Azure Site Recovery support for Availability zone for VMware to Azure and HyperV to Azure providers.</span></span>
* <span data-ttu-id="184db-173">HyperV-Azure 공급자를 위한 UseManagedDisk에 Azure Site Recovery가 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="184db-173">Azure Site Recovery support for UseManagedDisk for HyperV to Azure provider</span></span>

#### <a name="azresources"></a><span data-ttu-id="184db-174">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="184db-174">Az.Resources</span></span>
* <span data-ttu-id="184db-175">현재 매핑은 특정 시나리오를 중단시키므로 New-AzRoleAssignment 및 Set-AzRoleAssignment에서 보안 주체 유형이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-175">Removed principal type on New-AzRoleAssignment and Set-AzRoleAssignment because current mapping was breaking certain scenarios</span></span>

#### <a name="azsql"></a><span data-ttu-id="184db-176">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="184db-176">Az.Sql</span></span>
* <span data-ttu-id="184db-177">'New-AzSqlDatabase', 'Set-AzSqlDatabase', 'New-AzSqlElasticPool' 및 'Set-AzSqlElasticPool'에 MaintenanceConfigurationId가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-177">Added MaintenanceConfigurationId to 'New-AzSqlDatabase', 'Set-AzSqlDatabase', 'New-AzSqlElasticPool' and 'Set-AzSqlElasticPool'</span></span>
* <span data-ttu-id="184db-178">PredicateExpression 인수가 제공되는 경우에 발생하는 'Set-AzSqlServerAudit'의 회귀 문제가 해결되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-178">Fixed regression in 'Set-AzSqlServerAudit' when PredicateExpression argument is provided</span></span>

#### <a name="azstorage"></a><span data-ttu-id="184db-179">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="184db-179">Az.Storage</span></span>
* <span data-ttu-id="184db-180">Storage 계정 만들기/업데이트에서 RoutingPreference 설정이 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="184db-180">Supported RoutingPreference settings in create/update Storage account</span></span>
    - <span data-ttu-id="184db-181">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="184db-181">'New-AzStorageAccount'</span></span>
    - <span data-ttu-id="184db-182">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="184db-182">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="184db-183">Azure.Storage.Blobs가 12.8.0으로 업그레이드되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-183">Upgraded Azure.Storage.Blobs to 12.8.0</span></span>
* <span data-ttu-id="184db-184">Azure.Storage.Files.Shares가 12.6.0으로 업그레이드되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-184">Upgraded Azure.Storage.Files.Shares to 12.6.0</span></span>
* <span data-ttu-id="184db-185">Azure.Storage.Files.DataLake가 12.6.0으로 업그레이드되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-185">Upgraded Azure.Storage.Files.DataLake to 12.6.0</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="184db-186">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="184db-186">Az.Websites</span></span>
* <span data-ttu-id="184db-187">키 자격 증명 모음 인증서를 WebApp으로 가져오기 위한 지원 기능이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-187">Added support for Importing a key vault certificate to WebApp.</span></span>

### <a name="thanks-to-our-community-contributors"></a><span data-ttu-id="184db-188">커뮤니티 기여자에게 감사드립니다.</span><span class="sxs-lookup"><span data-stu-id="184db-188">Thanks to our community contributors</span></span>
* <span data-ttu-id="184db-189">@atul-ram, Set-AzEventHub.md 업데이트(#13921)</span><span class="sxs-lookup"><span data-stu-id="184db-189">@atul-ram, Update Set-AzEventHub.md (#13921)</span></span>
* <span data-ttu-id="184db-190">Christoph Bergmeister [MVP](@bergmeister), Set-AzDataLakeGen2AclRecursive.md - 오타 수정(directiry -> directory) (#14082)</span><span class="sxs-lookup"><span data-stu-id="184db-190">Christoph Bergmeister [MVP] (@bergmeister), Set-AzDataLakeGen2AclRecursive.md - Fix typo (directiry -> directory) (#14082)</span></span>
* <span data-ttu-id="184db-191">Alexander Schmidt(@devdeer-alex), 손상된 기여 지침 링크 수정(#14009)</span><span class="sxs-lookup"><span data-stu-id="184db-191">Alexander Schmidt (@devdeer-alex), Fixed broken link to contribution guidelines (#14009)</span></span>
* <span data-ttu-id="184db-192">@JiangYuchun, Get-AzApplicationGatewayAuthenticationCertificate.md 업데이트(#13972)</span><span class="sxs-lookup"><span data-stu-id="184db-192">@JiangYuchun, Update Get-AzApplicationGatewayAuthenticationCertificate.md (#13972)</span></span>
* <span data-ttu-id="184db-193">Sebastian Olsen(@Spacebjorn), 예제 명령 수정(#13901)</span><span class="sxs-lookup"><span data-stu-id="184db-193">Sebastian Olsen (@Spacebjorn), Corrected example command (#13901)</span></span>

## <a name="540---january-2021"></a><span data-ttu-id="184db-194">5.4.0 - 2021년 1월</span><span class="sxs-lookup"><span data-stu-id="184db-194">5.4.0 - January 2021</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="184db-195">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="184db-195">Az.Accounts</span></span>
* <span data-ttu-id="184db-196">디버그 메시지에 올바른 클라이언트 요청 ID 표시[#13745]</span><span class="sxs-lookup"><span data-stu-id="184db-196">Shown correct client request id on debug message [#13745]</span></span>
* <span data-ttu-id="184db-197">공용 Azure PowerShell 예외 형식 추가됨</span><span class="sxs-lookup"><span data-stu-id="184db-197">Added common Azure PowerShell exception type</span></span>
* <span data-ttu-id="184db-198">지원되는 스토리지 API 2019-06-01</span><span class="sxs-lookup"><span data-stu-id="184db-198">Supported storage API 2019-06-01</span></span>

#### <a name="azautomation"></a><span data-ttu-id="184db-199">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="184db-199">Az.Automation</span></span>
* <span data-ttu-id="184db-200">업데이트 관리 일정에 대한 설명이 채워지지 않은 문제 해결</span><span class="sxs-lookup"><span data-stu-id="184db-200">Fixed issue where description was not populated for update management schedules</span></span>

#### <a name="azcosmosdb"></a><span data-ttu-id="184db-201">Az.CosmosDB</span><span class="sxs-lookup"><span data-stu-id="184db-201">Az.CosmosDB</span></span>
* <span data-ttu-id="184db-202">'Az.CosmosDB' 모듈의 일반 공급</span><span class="sxs-lookup"><span data-stu-id="184db-202">General availability of 'Az.CosmosDB' module</span></span>
* <span data-ttu-id="184db-203">New-AzCosmosDBAccount cmdlet을 제한하여 기존 데이터베이스 계정에 대한 업데이트를 호출합니다.</span><span class="sxs-lookup"><span data-stu-id="184db-203">Restricting New-AzCosmosDBAccount cmdlet to make update calls to existing Database Accounts.</span></span>
* <span data-ttu-id="184db-204">SqlContainer에 AnalyticalStorageTTL를 소개합니다.</span><span class="sxs-lookup"><span data-stu-id="184db-204">Introducing AnalyticalStorageTTL in SqlContainer.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="184db-205">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="184db-205">Az.IotHub</span></span>
* <span data-ttu-id="184db-206">SAS 토큰 생성과 관련된 회귀 수정</span><span class="sxs-lookup"><span data-stu-id="184db-206">Fixed a regression regarding SAS token generation</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="184db-207">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="184db-207">Az.KeyVault</span></span>
* <span data-ttu-id="184db-208">비밀 관리 모듈의 문제 해결</span><span class="sxs-lookup"><span data-stu-id="184db-208">Fixed an issue in Secret Management module</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="184db-209">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="184db-209">Az.LogicApp</span></span>
* <span data-ttu-id="184db-210">'Get-AzLogicAppTriggerHistory' 및 'Get-AzLogicAppRunAction'이 결과의 첫 페이지만 검색하는 문제 해결[#9141]</span><span class="sxs-lookup"><span data-stu-id="184db-210">Fixed issue that 'Get-AzLogicAppTriggerHistory' and 'Get-AzLogicAppRunAction' only retrieving the first page of results [#9141]</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="184db-211">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="184db-211">Az.Monitor</span></span>
* <span data-ttu-id="184db-212">데이터 수집 규칙에 대한 cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-212">Added cmdlets for data collection rules:</span></span> 
    - <span data-ttu-id="184db-213">'Get-AzDataCollectionRule'</span><span class="sxs-lookup"><span data-stu-id="184db-213">'Get-AzDataCollectionRule'</span></span>
    - <span data-ttu-id="184db-214">'New-AzDataCollectionRule'</span><span class="sxs-lookup"><span data-stu-id="184db-214">'New-AzDataCollectionRule'</span></span>
    - <span data-ttu-id="184db-215">'Set-AzDataCollectionRule'</span><span class="sxs-lookup"><span data-stu-id="184db-215">'Set-AzDataCollectionRule'</span></span>
    - <span data-ttu-id="184db-216">'Update-AzDataCollectionRule'</span><span class="sxs-lookup"><span data-stu-id="184db-216">'Update-AzDataCollectionRule'</span></span>
    - <span data-ttu-id="184db-217">'Remove-AzDataCollectionRule'</span><span class="sxs-lookup"><span data-stu-id="184db-217">'Remove-AzDataCollectionRule'</span></span>
* <span data-ttu-id="184db-218">데이터 수집 규칙 연결에 대한 cmdlet이 추가됨</span><span class="sxs-lookup"><span data-stu-id="184db-218">Added cmdlets for data collection rules associations</span></span>
    - <span data-ttu-id="184db-219">'Get-AzDataCollectionRuleAssociation'</span><span class="sxs-lookup"><span data-stu-id="184db-219">'Get-AzDataCollectionRuleAssociation'</span></span>
    - <span data-ttu-id="184db-220">'New-AzDataCollectionRuleAssociation'</span><span class="sxs-lookup"><span data-stu-id="184db-220">'New-AzDataCollectionRuleAssociation'</span></span>
    - <span data-ttu-id="184db-221">'Remove-AzDataCollectionRuleAssociation'</span><span class="sxs-lookup"><span data-stu-id="184db-221">'Remove-AzDataCollectionRuleAssociation'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="184db-222">Az.Network</span><span class="sxs-lookup"><span data-stu-id="184db-222">Az.Network</span></span>
* <span data-ttu-id="184db-223">VpnGatewayNATRule의 CRUD에 대한 새 cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-223">Added new cmdlets for CRUD of VpnGatewayNATRule.</span></span>
    - <span data-ttu-id="184db-224">'New-AzVpnGatewayNatRule'</span><span class="sxs-lookup"><span data-stu-id="184db-224">'New-AzVpnGatewayNatRule'</span></span>
    - <span data-ttu-id="184db-225">'Update-AzVpnGatewayNatRule'</span><span class="sxs-lookup"><span data-stu-id="184db-225">'Update-AzVpnGatewayNatRule'</span></span>
    - <span data-ttu-id="184db-226">'Get-AzVpnGatewayNatRule'</span><span class="sxs-lookup"><span data-stu-id="184db-226">'Get-AzVpnGatewayNatRule'</span></span>
    - <span data-ttu-id="184db-227">'Remove-AzVpnGatewayNatRule'</span><span class="sxs-lookup"><span data-stu-id="184db-227">'Remove-AzVpnGatewayNatRule'</span></span>  
* <span data-ttu-id="184db-228">VpnGateway 리소스에서 NATRule을 설정하고 VpnSiteLinkConnection 리소스와 연결하도록 cmdlet이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-228">Updated cmdlets to set NATRule on VpnGateway resource and associate it with VpnSiteLinkConnection resource.</span></span>
    - <span data-ttu-id="184db-229">'New-AzVpnGateway'</span><span class="sxs-lookup"><span data-stu-id="184db-229">'New-AzVpnGateway'</span></span>
    - <span data-ttu-id="184db-230">'Update-AzVpnGateway'</span><span class="sxs-lookup"><span data-stu-id="184db-230">'Update-AzVpnGateway'</span></span> 
    - <span data-ttu-id="184db-231">'New-AzVpnSiteLinkConnection'</span><span class="sxs-lookup"><span data-stu-id="184db-231">'New-AzVpnSiteLinkConnection'</span></span>
* <span data-ttu-id="184db-232">Virtual Network 게이트웨이 연결에서 ConnectionMode 설정을 사용하도록 cmdlet이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-232">Updated cmdlets to enable setting of ConnectionMode on Virtual Network Gateway Connections.</span></span>
    - <span data-ttu-id="184db-233">'New-AzVirtualNetworkGatewayConnection'</span><span class="sxs-lookup"><span data-stu-id="184db-233">'New-AzVirtualNetworkGatewayConnection'</span></span>
    - <span data-ttu-id="184db-234">'Set-AzVirtualNetworkGatewayConnection'</span><span class="sxs-lookup"><span data-stu-id="184db-234">'Set-AzVirtualNetworkGatewayConnection'</span></span>
* <span data-ttu-id="184db-235">'New-AzFirewallPolicyApplicationRule' cmdlet 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-235">Updated 'New-AzFirewallPolicyApplicationRule' cmdlet:</span></span>
    - <span data-ttu-id="184db-236">매개 변수 TargetUrl이 추가됨</span><span class="sxs-lookup"><span data-stu-id="184db-236">Added parameter TargetUrl</span></span>
    - <span data-ttu-id="184db-237">매개 변수 TerminateTLS가 추가됨</span><span class="sxs-lookup"><span data-stu-id="184db-237">Added parameter TerminateTLS</span></span>
* <span data-ttu-id="184db-238">Azure Firewall Premium 기능에 대한 새 cmdlet이 추가됨</span><span class="sxs-lookup"><span data-stu-id="184db-238">Added new cmdlets for Azure Firewall Premium Features</span></span>
    - <span data-ttu-id="184db-239">'New-AzFirewallPolicyIntrusionDetection'</span><span class="sxs-lookup"><span data-stu-id="184db-239">'New-AzFirewallPolicyIntrusionDetection'</span></span>
    - <span data-ttu-id="184db-240">'New-AzFirewallPolicyIntrusionDetectionBypassTraffic'</span><span class="sxs-lookup"><span data-stu-id="184db-240">'New-AzFirewallPolicyIntrusionDetectionBypassTraffic'</span></span>
    - <span data-ttu-id="184db-241">'New-AzFirewallPolicyIntrusionDetectionSignatureOverride'</span><span class="sxs-lookup"><span data-stu-id="184db-241">'New-AzFirewallPolicyIntrusionDetectionSignatureOverride'</span></span>
* <span data-ttu-id="184db-242">New-AzFirewallPolicy cmdlet이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-242">Updated New-AzFirewallPolicy cmdlet:</span></span>
    - <span data-ttu-id="184db-243">매개 변수 -SkuTier 추가됨</span><span class="sxs-lookup"><span data-stu-id="184db-243">Added parameter -SkuTier</span></span>
    - <span data-ttu-id="184db-244">매개 변수 -Identity 추가됨</span><span class="sxs-lookup"><span data-stu-id="184db-244">Added parameter -Identity</span></span>
    - <span data-ttu-id="184db-245">매개 변수 -UserAssignedIdentityId 추가됨</span><span class="sxs-lookup"><span data-stu-id="184db-245">Added parameter -UserAssignedIdentityId</span></span>
    - <span data-ttu-id="184db-246">매개 변수 -IntrusionDetection 추가됨</span><span class="sxs-lookup"><span data-stu-id="184db-246">Added parameter -IntrusionDetection</span></span>
    - <span data-ttu-id="184db-247">매개 변수 -TransportSecurityName 추가됨</span><span class="sxs-lookup"><span data-stu-id="184db-247">Added parameter -TransportSecurityName</span></span>
    - <span data-ttu-id="184db-248">매개 변수 -TransportSecurityKeyVaultSecretId 추가됨</span><span class="sxs-lookup"><span data-stu-id="184db-248">Added parameter -TransportSecurityKeyVaultSecretId</span></span>
* <span data-ttu-id="184db-249">가상 네트워크 게이트웨이 연결에 대한 IKE 보안 연결을 가져오는 새 cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-249">Added new cmdlet to fetch IKE Security Associations for Virtual Network Gateway Connections.</span></span>
    - <span data-ttu-id="184db-250">'Get-AzVirtualNetworkGatewayConnectionIkeSa'</span><span class="sxs-lookup"><span data-stu-id="184db-250">'Get-AzVirtualNetworkGatewayConnectionIkeSa'</span></span>
* <span data-ttu-id="184db-251">p2sVpnGateway에 대한 여러 인증 지원이 추가됨</span><span class="sxs-lookup"><span data-stu-id="184db-251">Added multiple Authentication support for p2sVpnGateway</span></span>
    - <span data-ttu-id="184db-252">여러 인증 매개 변수를 설정할 수 있도록 New-AzVpnServerConfiguration 및 Update-AzVpnServerConfiguration이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-252">Updated New-AzVpnServerConfiguration and Update-AzVpnServerConfiguration to allow multiple authentication parameters to be set.</span></span>
* <span data-ttu-id="184db-253">'New-AzVpnGateway' 및 'New-AzP2sVpnGateway' cmdlet이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-253">Updated 'New-AzVpnGateway' and 'New-AzP2sVpnGateway' cmdlet:</span></span>
    - <span data-ttu-id="184db-254">매개 변수 EnableRoutingPreferenceInternetFlag 추가됨</span><span class="sxs-lookup"><span data-stu-id="184db-254">Added parameter EnableRoutingPreferenceInternetFlag</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="184db-255">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="184db-255">Az.RecoveryServices</span></span>
* <span data-ttu-id="184db-256">지역 간 복원 기능이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-256">Added Cross Region Restore feature.</span></span>  
* <span data-ttu-id="184db-257">대상 항목이 가용성 그룹인 경우 워크로드 구성 가져오기가 차단되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-257">Blocked getting workload config when target item is an availability group.</span></span>

#### <a name="azresources"></a><span data-ttu-id="184db-258">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="184db-258">Az.Resources</span></span>
* <span data-ttu-id="184db-259">New-Az\*Deployments cmdlet에서 -QueryString 매개 변수에 대한 지원 추가됨</span><span class="sxs-lookup"><span data-stu-id="184db-259">Added support for -QueryString parameter in New-Az\*Deployments cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="184db-260">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="184db-260">Az.Sql</span></span>
* <span data-ttu-id="184db-261">'Start-AzSqlInstanceDatabaseLogReplay'cmdlet 동기화, -AsJob 플래그 추가됨</span><span class="sxs-lookup"><span data-stu-id="184db-261">Made 'Start-AzSqlInstanceDatabaseLogReplay' cmdlet synchronous, added -AsJob flag</span></span>

#### <a name="azstorage"></a><span data-ttu-id="184db-262">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="184db-262">Az.Storage</span></span>
* <span data-ttu-id="184db-263">-IncludeVersion으로 BLOB을 나열할 때 ContinuationToken이 null이 되지 않도록 수정</span><span class="sxs-lookup"><span data-stu-id="184db-263">Fix ContinuationToken never null when list blob with -IncludeVersion</span></span>
    - <span data-ttu-id="184db-264">'Get-AzStorageBlob'</span><span class="sxs-lookup"><span data-stu-id="184db-264">'Get-AzStorageBlob'</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="184db-265">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="184db-265">Az.Websites</span></span>
* <span data-ttu-id="184db-266">App Service 관리형 인증서에 대한 지원이 추가됨</span><span class="sxs-lookup"><span data-stu-id="184db-266">Added support for App Service Managed certificates</span></span>
    - <span data-ttu-id="184db-267">'New-AzWebAppCertificate'</span><span class="sxs-lookup"><span data-stu-id="184db-267">'New-AzWebAppCertificate'</span></span>
    - <span data-ttu-id="184db-268">'Remove-AzWebAppCertificate'</span><span class="sxs-lookup"><span data-stu-id="184db-268">'Remove-AzWebAppCertificate'</span></span>
* <span data-ttu-id="184db-269">'Set-AzWebApp' 및 'Set-AzWebAppSlot'의 앱 설정에서 Docker 암호가 제거되는 문제 해결</span><span class="sxs-lookup"><span data-stu-id="184db-269">Fixed issue that causes Docker Password to be removed from appsettings in 'Set-AzWebApp' and 'Set-AzWebAppSlot'</span></span>

### <a name="thanks-to-our-community-contributors"></a><span data-ttu-id="184db-270">커뮤니티 기여자에게 감사드립니다.</span><span class="sxs-lookup"><span data-stu-id="184db-270">Thanks to our community contributors</span></span>
* <span data-ttu-id="184db-271">Ivan Akcheurov(@ivanakcheurov), Set-AzSecurityWorkspaceSetting.md 업데이트(#13877)</span><span class="sxs-lookup"><span data-stu-id="184db-271">Ivan Akcheurov (@ivanakcheurov), Update Set-AzSecurityWorkspaceSetting.md (#13877)</span></span>
* <span data-ttu-id="184db-272">@javiermarasco, 예제 업데이트(#13837)</span><span class="sxs-lookup"><span data-stu-id="184db-272">@javiermarasco, Update example (#13837)</span></span>
* <span data-ttu-id="184db-273">@jhaprakash26, Set-AzVirtualNetwork.md 업데이트(#13857)</span><span class="sxs-lookup"><span data-stu-id="184db-273">@jhaprakash26, Update Set-AzVirtualNetwork.md (#13857)</span></span>
* <span data-ttu-id="184db-274">Michael Holmes(@MichaelHolmesWP), New-AzStorageTableStoredAccessPolicy.md 업데이트(#13871)</span><span class="sxs-lookup"><span data-stu-id="184db-274">Michael Holmes (@MichaelHolmesWP), Update New-AzStorageTableStoredAccessPolicy.md (#13871)</span></span>
* <span data-ttu-id="184db-275">Michael James(@mikejwhat), Get-AzLogicAppTriggerHistory 및 Get-AzLogicAppRunAction이 30개 이상의 결과를 반환하도록 허용(#13846)</span><span class="sxs-lookup"><span data-stu-id="184db-275">Michael James (@mikejwhat), Allow Get-AzLogicAppTriggerHistory and Get-AzLogicAppRunAction to return more than 30 results (#13846)</span></span>
* <span data-ttu-id="184db-276">@Willem-J-an, Set-AzWebApp(슬롯)의 appsettings에서 Docker 암호가 제거되는 버그 수정(#13866)</span><span class="sxs-lookup"><span data-stu-id="184db-276">@Willem-J-an, Fix bug causing Docker Password to be removed from appsettings in Set-AzWebApp(Slot) (#13866)</span></span>

## <a name="530---december-2020"></a><span data-ttu-id="184db-277">5.3.0 - 2020년 12월</span><span class="sxs-lookup"><span data-stu-id="184db-277">5.3.0 - December 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="184db-278">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="184db-278">Az.Accounts</span></span>
* <span data-ttu-id="184db-279">Windows PowerShell에서 Http 프록시가 적용되지 않는 문제 해결[#13647]</span><span class="sxs-lookup"><span data-stu-id="184db-279">Fixed the issue that Http proxy is not respected in Windows PowerShell [#13647]</span></span>
* <span data-ttu-id="184db-280">생성된 모듈에서 장기 실행 작업의 디버그 로그 개선</span><span class="sxs-lookup"><span data-stu-id="184db-280">Improved debug log of long running operations in generated modules</span></span>

#### <a name="azautomation"></a><span data-ttu-id="184db-281">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="184db-281">Az.Automation</span></span>
* <span data-ttu-id="184db-282">'Start-AzAutomationRunbook'의 매개 변수가 PSObject 래핑된 문자열을 JSON 문자열로 변환할 수 없는 문제 해결[#13240]</span><span class="sxs-lookup"><span data-stu-id="184db-282">Fixed issue that parameters of 'Start-AzAutomationRunbook' cannot convert PSObject wrapped string to JSON string [#13240]</span></span>
* <span data-ttu-id="184db-283">New-AzAutomationUpdateManagementAzureQuery cmdlet에 대한 위치 완성기 수정</span><span class="sxs-lookup"><span data-stu-id="184db-283">Fixed location completer for New-AzAutomationUpdateManagementAzureQuery cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="184db-284">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="184db-284">Az.Compute</span></span>
* <span data-ttu-id="184db-285">새 매개 변수 집합 'VMParameterSet'의 새 매개 변수 'VM'이 'Get-AzVMDscExtensionStatus' 및 'Get-AzVMDscExtension' cmdlet에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-285">New parameter 'VM' in new parameter set 'VMParameterSet' added to 'Get-AzVMDscExtensionStatus' and 'Get-AzVMDscExtension' cmdlets.</span></span> 

#### <a name="azdatabricks"></a><span data-ttu-id="184db-286">Az.Databricks</span><span class="sxs-lookup"><span data-stu-id="184db-286">Az.Databricks</span></span>
* <span data-ttu-id="184db-287">'New-AzDatabricksVNetPeering'이 완전히 프로비저닝되기 전에 반환될 수 있는 문제 해결(https://github.com/Azure/autorest.powershell/issues/610)</span><span class="sxs-lookup"><span data-stu-id="184db-287">Fixed an issue that may cause 'New-AzDatabricksVNetPeering' to return before it is fully provisioned (https://github.com/Azure/autorest.powershell/issues/610)</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="184db-288">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="184db-288">Az.DataFactory</span></span>
* <span data-ttu-id="184db-289">SupportsShouldProcess 문제에 대해 'Invoke-AzDataFactoryV2Pipeline' 명령 수정</span><span class="sxs-lookup"><span data-stu-id="184db-289">Fixed the command 'Invoke-AzDataFactoryV2Pipeline' for SupportsShouldProcess issue</span></span>

#### <a name="azdesktopvirtualization"></a><span data-ttu-id="184db-290">Az.DesktopVirtualization</span><span class="sxs-lookup"><span data-stu-id="184db-290">Az.DesktopVirtualization</span></span>
* <span data-ttu-id="184db-291">호스트 풀에 StartVMOnConnect 속성을 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-291">Added StartVMOnConnect property to hostpool.</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="184db-292">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="184db-292">Az.HDInsight</span></span>
* <span data-ttu-id="184db-293">추가된 속성: AzureHDInsightHostInfo 클래스의 Fqdn 및 EffectiveDiskEncryptionKeyUrl.</span><span class="sxs-lookup"><span data-stu-id="184db-293">Added properties: Fqdn and EffectiveDiskEncryptionKeyUrl in the class AzureHDInsightHostInfo.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="184db-294">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="184db-294">Az.KeyVault</span></span>
* <span data-ttu-id="184db-295">비밀을 일반 텍스트로 직접 반환하기 위해 'Get-AzKeyVaultSecret'에 새 매개 변수 '-AsPlainText' 추가[#13630]</span><span class="sxs-lookup"><span data-stu-id="184db-295">Added a new parameter '-AsPlainText' to 'Get-AzKeyVaultSecret' to directly return the secret in plain text [#13630]</span></span>
* <span data-ttu-id="184db-296">관리되는 HSM 전체 백업에서 키 선택적 복원 지원[#13526]</span><span class="sxs-lookup"><span data-stu-id="184db-296">Supported selective restore a key from a managed HSM full backup [#13526]</span></span>
* <span data-ttu-id="184db-297">일부 사소한 문제 해결[#13583] [#13584]</span><span class="sxs-lookup"><span data-stu-id="184db-297">Fixed some minor issues [#13583] [#13584]</span></span>
* <span data-ttu-id="184db-298">SecretManagement 모듈에서 'Get-Secret'의 누락된 반환 개체 추가</span><span class="sxs-lookup"><span data-stu-id="184db-298">Added missing return objects of 'Get-Secret' in SecretManagement module</span></span>
* <span data-ttu-id="184db-299">기본 액세스 정책 없이 자격 증명 모음이 만들어질 수 있는 문제 해결[#13687]</span><span class="sxs-lookup"><span data-stu-id="184db-299">Fixed an issue that may cause vault to be created without default access policy [#13687]</span></span>

#### <a name="azkusto"></a><span data-ttu-id="184db-300">Az.Kusto</span><span class="sxs-lookup"><span data-stu-id="184db-300">Az.Kusto</span></span>
* <span data-ttu-id="184db-301">API 버전이 2020-09-18로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-301">Updated API version to 2020-09-18.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="184db-302">Az.Network</span><span class="sxs-lookup"><span data-stu-id="184db-302">Az.Network</span></span>
* <span data-ttu-id="184db-303">ExpressRouteCircuit 시나리오에서 피어링 및 연결 cmdlet 제거 문제 해결</span><span class="sxs-lookup"><span data-stu-id="184db-303">Fixed issue in remove peering and connection cmdlet for ExpressRouteCircuit scenario</span></span>
    - <span data-ttu-id="184db-304">'Remove-AzExpressRouteCircuitPeeringConfig' 및 'Remove-AzExpressRouteCircuitConnectionConfig'</span><span class="sxs-lookup"><span data-stu-id="184db-304">'Remove-AzExpressRouteCircuitPeeringConfig' and 'Remove-AzExpressRouteCircuitConnectionConfig'</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="184db-305">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="184db-305">Az.PolicyInsights</span></span>
* <span data-ttu-id="184db-306">Get-AzPolicyState에 대해 페이지를 매긴 결과를 반환하기 위한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="184db-306">Added support for returning paginated results for Get-AzPolicyState</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="184db-307">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="184db-307">Az.RecoveryServices</span></span>
* <span data-ttu-id="184db-308">SQL에 대해 일시 삭제 기능을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-308">Enabled softdelete feature for SQL.</span></span>
* <span data-ttu-id="184db-309">SQL AG 복원이 수정되었고 컨테이너 이름 확인이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-309">Fixed SQL AG restore and removed the container name check.</span></span>
* <span data-ttu-id="184db-310">Azure Files 백업 항목에 대한 컨테이너 이름 형식을 변경했습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-310">Changed container name format for Azure Files backup item.</span></span>
* <span data-ttu-id="184db-311">복구 서비스 자격 증명 모음에 대한 CMK 기능 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-311">Added CMK feature support for Recovery services vault.</span></span>

#### <a name="azresources"></a><span data-ttu-id="184db-312">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="184db-312">Az.Resources</span></span>
* <span data-ttu-id="184db-313">'New-AzureManagedApplication' 및 'Set-AzureManagedApplication'에서 NullRef 예외 문제를 해결했습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-313">Fixed a NullRef exception issue in 'New-AzureManagedApplication' and 'Set-AzureManagedApplication'.</span></span>
* <span data-ttu-id="184db-314">Azure Resource Manager SDK를 업데이트하여 최신 DeploymentScripts GA api-version: 2020-10-01을 사용하도록 했습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-314">Updated Azure Resource Manager SDK to use latest DeploymentScripts GA api-version: 2020-10-01.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="184db-315">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="184db-315">Az.ServiceFabric</span></span>
* <span data-ttu-id="184db-316">'Add-AzServiceFabricNodeType'을 수정했습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-316">Fixed 'Add-AzServiceFabricNodeType'.</span></span> <span data-ttu-id="184db-317">가상 머신 확장 집합을 만들기 전에 서비스 패브릭 클러스터에 노드 유형을 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-317">Added node type to service fabric cluster before creating virtual machine scale set.</span></span>

#### <a name="azsql"></a><span data-ttu-id="184db-318">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="184db-318">Az.Sql</span></span>
* <span data-ttu-id="184db-319">'InstanceFailoverGroup' 명령에 대한 매개 변수 설명을 수정했습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-319">Fixed parameter description for 'InstanceFailoverGroup' command.</span></span>
* <span data-ttu-id="184db-320">SQL 데이터 분류 명령의 ID에서 schemaName, tableName 및 columnName이 추출되는 논리를 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-320">Updated the logic in which schemaName, tableName and columnName are being extracted from the id of SQL Data Classification commands.</span></span>
* <span data-ttu-id="184db-321">문서를 준수하도록 'Get-AzSqlDatabaseImportExportStatus'의 Status 및 StatusMessage 필드 수정</span><span class="sxs-lookup"><span data-stu-id="184db-321">Fixed Status and StatusMessage fields in 'Get-AzSqlDatabaseImportExportStatus' to conform to documentation</span></span>
* <span data-ttu-id="184db-322">다음의 Microsoft 지원 작업(DevOps) 감사 cmdlet 추가: Get-AzSqlServerMSSupportAudit, Set-AzSqlServerMSSupportAudit, Remove-AzSqlServerMSSupportAudit</span><span class="sxs-lookup"><span data-stu-id="184db-322">Added Microsoft support operations (DevOps) auditing cmdlets: Get-AzSqlServerMSSupportAudit, Set-AzSqlServerMSSupportAudit, Remove-AzSqlServerMSSupportAudit</span></span>

#### <a name="azstorage"></a><span data-ttu-id="184db-323">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="184db-323">Az.Storage</span></span>
* <span data-ttu-id="184db-324">스토리지 계정의 EncryptionScope 생성/업데이트/가져오기/나열 지원</span><span class="sxs-lookup"><span data-stu-id="184db-324">Supported create/update/get/list EncryptionScope of a Storage account</span></span>
    - <span data-ttu-id="184db-325">'New-AzStorageEncryptionScope'</span><span class="sxs-lookup"><span data-stu-id="184db-325">'New-AzStorageEncryptionScope'</span></span>
    - <span data-ttu-id="184db-326">'Update-AzStorageEncryptionScope'</span><span class="sxs-lookup"><span data-stu-id="184db-326">'Update-AzStorageEncryptionScope'</span></span>
    - <span data-ttu-id="184db-327">'Get-AzStorageEncryptionScope'</span><span class="sxs-lookup"><span data-stu-id="184db-327">'Get-AzStorageEncryptionScope'</span></span>
* <span data-ttu-id="184db-328">암호화 범위 설정으로 컨테이너 만들기 및 Blob 업로드 지원</span><span class="sxs-lookup"><span data-stu-id="184db-328">Supported create container and upload blob with Encryption Scope setting</span></span>
    - <span data-ttu-id="184db-329">'New-AzRmStorageContainer'</span><span class="sxs-lookup"><span data-stu-id="184db-329">'New-AzRmStorageContainer'</span></span>
    - <span data-ttu-id="184db-330">'New-AzStorageContainer'</span><span class="sxs-lookup"><span data-stu-id="184db-330">'New-AzStorageContainer'</span></span>
    - <span data-ttu-id="184db-331">'Set-AzStorageBlobContent'</span><span class="sxs-lookup"><span data-stu-id="184db-331">'Set-AzStorageBlobContent'</span></span>

### <a name="thanks-to-our-community-contributors"></a><span data-ttu-id="184db-332">커뮤니티 기여자에게 감사드립니다.</span><span class="sxs-lookup"><span data-stu-id="184db-332">Thanks to our community contributors</span></span>
* <span data-ttu-id="184db-333">Andreas Wolter(@AndreasWolter), 마케팅 언어 제거, 예제 필터 개선(#13671)</span><span class="sxs-lookup"><span data-stu-id="184db-333">Andreas Wolter (@AndreasWolter), removed marketing language, better example filter (#13671)</span></span>
* <span data-ttu-id="184db-334">Tidjani Belmansour(@BelRarr), Get-AzBillingInvoice.md 업데이트(#13634)</span><span class="sxs-lookup"><span data-stu-id="184db-334">Tidjani Belmansour (@BelRarr), Update Get-AzBillingInvoice.md (#13634)</span></span>
* <span data-ttu-id="184db-335">David Klempfner(@DavidKlempfner)</span><span class="sxs-lookup"><span data-stu-id="184db-335">David Klempfner (@DavidKlempfner)</span></span>
  * <span data-ttu-id="184db-336">맞춤법 오류 수정(#13677)</span><span class="sxs-lookup"><span data-stu-id="184db-336">Fixed spelling mistake (#13677)</span></span>
  * <span data-ttu-id="184db-337">PSMetricNoDetails.cs 업데이트(#13676)</span><span class="sxs-lookup"><span data-stu-id="184db-337">Update PSMetricNoDetails.cs (#13676)</span></span>
* <span data-ttu-id="184db-338">@kilobyte97, 구성을 삭제하기 위해 cmdlet 제거에 대한 버그 수정(#13655)</span><span class="sxs-lookup"><span data-stu-id="184db-338">@kilobyte97, bugfix for remove cmdlet to delete config (#13655)</span></span>
* <span data-ttu-id="184db-339">@kongou-ae, Set-AzFirewall.md 업데이트(#13727)</span><span class="sxs-lookup"><span data-stu-id="184db-339">@kongou-ae, Update Set-AzFirewall.md (#13727)</span></span>
* <span data-ttu-id="184db-340">@MasterKuat, 설명서의 제목과 코드 간 스왑 수정(#13666)</span><span class="sxs-lookup"><span data-stu-id="184db-340">@MasterKuat, Fix swap between title and code in documentation (#13666)</span></span>
* <span data-ttu-id="184db-341">NickT(@nukeulis), Set-AzContext.md 업데이트(#13702)</span><span class="sxs-lookup"><span data-stu-id="184db-341">NickT (@nukeulis), Update Set-AzContext.md (#13702)</span></span>
* <span data-ttu-id="184db-342">@PaulHCode, Start-AzJitNetworkAccessPolicy.md 업데이트 - 시연 중인 cmdlet이 적절하게 표시되도록 예제 수정(#13713)</span><span class="sxs-lookup"><span data-stu-id="184db-342">@PaulHCode, Update Start-AzJitNetworkAccessPolicy.md - Fix the Example to display the proper cmdlet being demonstrated (#13713)</span></span>
* <span data-ttu-id="184db-343">Ryan Borstelmann (@ryanborMSFT), 구독 ID 제거(#13715)</span><span class="sxs-lookup"><span data-stu-id="184db-343">Ryan Borstelmann (@ryanborMSFT), Removed Subscription ID (#13715)</span></span>
* <span data-ttu-id="184db-344">Shashikant Shakya (@shshakya), Set-AzSqlDatabase.md 업데이트(#13674)</span><span class="sxs-lookup"><span data-stu-id="184db-344">Shashikant Shakya (@shshakya), Update Set-AzSqlDatabase.md (#13674)</span></span>
* <span data-ttu-id="184db-345">Sebastian Olsen(@Spacebjorn), Get-AzRecoveryServicesBackupItem.md 업데이트(#13719)</span><span class="sxs-lookup"><span data-stu-id="184db-345">Sebastian Olsen (@Spacebjorn), Update Get-AzRecoveryServicesBackupItem.md (#13719)</span></span>

## <a name="520---december-2020"></a><span data-ttu-id="184db-346">5.2.0 - 2020년 12월</span><span class="sxs-lookup"><span data-stu-id="184db-346">5.2.0 - December 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="184db-347">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="184db-347">Az.Accounts</span></span>
* <span data-ttu-id="184db-348">기본 라이브러리에서 가져올 수 없는 경우 원시 토큰에서 ExpiresOn 시간을 구문 분석하도록 관리됨</span><span class="sxs-lookup"><span data-stu-id="184db-348">Managed to parse ExpiresOn time from raw token if could not get from underlying library</span></span>
* <span data-ttu-id="184db-349">대화형 인증을 사용할 수 없는 경우 경고 메시지 향상됨</span><span class="sxs-lookup"><span data-stu-id="184db-349">Improved warning message if Interactive authentication is unavailable</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="184db-350">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="184db-350">Az.ApiManagement</span></span>
* <span data-ttu-id="184db-351">[호환성이 손상되는 변경] 기본적으로 'New-AzApiManagementProduct'는 구독 제한이 없습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-351">[Breaking change] 'New-AzApiManagementProduct' by default has no subscription limit.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="184db-352">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="184db-352">Az.Compute</span></span>
* <span data-ttu-id="184db-353">너무 많은 리소스로 인한 제한을 확인하기 전에 '-Name'으로 필터링하도록 Get-AzVm을 편집했습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-353">Edited Get-AzVm to filter by '-Name' prior to checking for throttling due to too many resources.</span></span> 
* <span data-ttu-id="184db-354">새 cmdlet 'Start-AzVmssRollingExtensionUpgrade'.</span><span class="sxs-lookup"><span data-stu-id="184db-354">New cmdlet 'Start-AzVmssRollingExtensionUpgrade'.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="184db-355">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="184db-355">Az.ContainerRegistry</span></span>
* <span data-ttu-id="184db-356">'Get-AzContainerRegistryUsage'에 대한 파이프라인 입력 및 값에 대해 'Name' 매개 변수 지원됨 [#13605]</span><span class="sxs-lookup"><span data-stu-id="184db-356">Supported parameter 'Name' for and value from pipeline input for 'Get-AzContainerRegistryUsage' [#13605]</span></span>
* <span data-ttu-id="184db-357">'Connect-AzContainerRegistry'에 대한 예외 수정됨</span><span class="sxs-lookup"><span data-stu-id="184db-357">Polished exceptions for 'Connect-AzContainerRegistry'</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="184db-358">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="184db-358">Az.DataFactory</span></span>
* <span data-ttu-id="184db-359">ADF .Net SDK 버전이 4.13.0으로 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="184db-359">Updated ADF .Net SDK version to 4.13.0</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="184db-360">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="184db-360">Az.HealthcareApis</span></span>
* <span data-ttu-id="184db-361">고객 관리형 키에 대한 지원 추가됨</span><span class="sxs-lookup"><span data-stu-id="184db-361">Added support for customer managed keys</span></span>

#### <a name="aziothub"></a><span data-ttu-id="184db-362">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="184db-362">Az.IotHub</span></span>
* <span data-ttu-id="184db-363">SAS 토큰의 문제가 해결되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-363">Fixed an issue of SAS token.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="184db-364">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="184db-364">Az.KeyVault</span></span>
* <span data-ttu-id="184db-365">키 자격 증명 모음 액세스 정책 설정 시 'all'이 옵션으로 지원됨</span><span class="sxs-lookup"><span data-stu-id="184db-365">Supported 'all' as an option when setting key vault access policies</span></span>
* <span data-ttu-id="184db-366">새 버전의 SecretManagement 모듈 지원됨 [#13366]</span><span class="sxs-lookup"><span data-stu-id="184db-366">Supported new version of SecretManagement module [#13366]</span></span>
* <span data-ttu-id="184db-367">SecretManagementModule의 'SecretValue'에 대해 ByteArray, String, PSCredential 및 Hashtable 지원됨 [#12190]</span><span class="sxs-lookup"><span data-stu-id="184db-367">Supported ByteArray, String, PSCredential and Hashtable for 'SecretValue' in SecretManagementModule [#12190]</span></span>
* <span data-ttu-id="184db-368">[호환성이 손상되는 변경] 관리형 HSM과 관련된 cmdlet의 API 표면을 다시 디자인했습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-368">[Breaking change] redesigned the API surface of cmdlets related to managed HSM.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="184db-369">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="184db-369">Az.Monitor</span></span>
* <span data-ttu-id="184db-370">'New-AzAutoscaleProfile'의 'Rule' 매개 변수가 빈 목록을 허용하도록 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-370">Changed parameter 'Rule' of 'New-AzAutoscaleProfile' to accept empty list.</span></span> <span data-ttu-id="184db-371">[#12903]</span><span class="sxs-lookup"><span data-stu-id="184db-371">[#12903]</span></span>
* <span data-ttu-id="184db-372">진단 설정을 보다 유연하게 만들 수 있도록 다음과 같은 새 cmdlet 추가됨</span><span class="sxs-lookup"><span data-stu-id="184db-372">Added new cmdlets to support creating diagnostic settings more flexible:</span></span>
    * <span data-ttu-id="184db-373">'Get-AzDiagnosticSettingCategory'</span><span class="sxs-lookup"><span data-stu-id="184db-373">'Get-AzDiagnosticSettingCategory'</span></span>
    * <span data-ttu-id="184db-374">'New-AzDiagnosticSetting'</span><span class="sxs-lookup"><span data-stu-id="184db-374">'New-AzDiagnosticSetting'</span></span>
    * <span data-ttu-id="184db-375">'New-AzDiagnosticDetailSetting'</span><span class="sxs-lookup"><span data-stu-id="184db-375">'New-AzDiagnosticDetailSetting'</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="184db-376">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="184db-376">Az.RecoveryServices</span></span>
* <span data-ttu-id="184db-377">도움말 텍스트 및 매개 변수 집합 이름이 'Restore-AzRecoveryServicesBackupItem' cmdlet으로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-377">Made help text and parameter set name changes to 'Restore-AzRecoveryServicesBackupItem' cmdlet.</span></span>

#### <a name="azresources"></a><span data-ttu-id="184db-378">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="184db-378">Az.Resources</span></span>
* <span data-ttu-id="184db-379">'Set-AzTemplateSpec' 및 'New-AzTemplateSpec'에 '-Tag' 매개 변수 지원 추가됨</span><span class="sxs-lookup"><span data-stu-id="184db-379">Added '-Tag' parameter support to 'Set-AzTemplateSpec' and 'New-AzTemplateSpec'</span></span>
* <span data-ttu-id="184db-380">템플릿 사양에 대한 기본 포맷터에 Tag 표시 지원 추가됨</span><span class="sxs-lookup"><span data-stu-id="184db-380">Added Tag display support to default formatter for Template Specs</span></span> 

#### <a name="azservicefabric"></a><span data-ttu-id="184db-381">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="184db-381">Az.ServiceFabric</span></span>
* <span data-ttu-id="184db-382">SettingsSectionDescription 매개 변수를 사용하여 'Set-AzServiceFabricSetting'에 예가 추가됨</span><span class="sxs-lookup"><span data-stu-id="184db-382">Added example to 'Set-AzServiceFabricSetting' with SettingsSectionDescription param</span></span>
* <span data-ttu-id="184db-383">ARM 배포 리소스에 대해서만 지원됨을 알리도록 애플리케이션 관련 cmdlet 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="184db-383">Updated application related cmdlets to call out that support is only for ARM deployed resources</span></span>
* <span data-ttu-id="184db-384">사용 중단 클러스터 인증서 cmdlet 'Add-AzureRmServiceFabricClusterCertificate' 및 'Remove-AzureRmServiceFabricClusterCertificate'로 표시됨</span><span class="sxs-lookup"><span data-stu-id="184db-384">Marked for deprecation cluster cert cmdlets 'Add-AzureRmServiceFabricClusterCertificate' and 'Remove-AzureRmServiceFabricClusterCertificate'</span></span>

#### <a name="azsql"></a><span data-ttu-id="184db-385">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="184db-385">Az.Sql</span></span>
* <span data-ttu-id="184db-386">SecondaryType이 다음에 추가됨</span><span class="sxs-lookup"><span data-stu-id="184db-386">Added SecondaryType to the following:</span></span> 
    - <span data-ttu-id="184db-387">'New-AzSqlDatabase'</span><span class="sxs-lookup"><span data-stu-id="184db-387">'New-AzSqlDatabase'</span></span>
    - <span data-ttu-id="184db-388">'Set-AzSqlDatabase'</span><span class="sxs-lookup"><span data-stu-id="184db-388">'Set-AzSqlDatabase'</span></span>
    - <span data-ttu-id="184db-389">'New-AzSqlDatabaseSecondary'</span><span class="sxs-lookup"><span data-stu-id="184db-389">'New-AzSqlDatabaseSecondary'</span></span>
* <span data-ttu-id="184db-390">HighAvailabilityReplicaCount가 다음에 추가됨</span><span class="sxs-lookup"><span data-stu-id="184db-390">Added HighAvailabilityReplicaCount to the following:</span></span> 
    - <span data-ttu-id="184db-391">'New-AzSqlDatabase'</span><span class="sxs-lookup"><span data-stu-id="184db-391">'New-AzSqlDatabase'</span></span>
    - <span data-ttu-id="184db-392">'Set-AzSqlDatabase'</span><span class="sxs-lookup"><span data-stu-id="184db-392">'Set-AzSqlDatabase'</span></span>
* <span data-ttu-id="184db-393">다음에서 HighAvailabilityReplicaCount의 별칭을 ReadReplicaCount로 지정됨</span><span class="sxs-lookup"><span data-stu-id="184db-393">Made ReadReplicaCount an alias of HighAvailabilityReplicaCount in the following:</span></span> 
    - <span data-ttu-id="184db-394">'New-AzSqlDatabase'</span><span class="sxs-lookup"><span data-stu-id="184db-394">'New-AzSqlDatabase'</span></span>
    - <span data-ttu-id="184db-395">'Set-AzSqlDatabase'</span><span class="sxs-lookup"><span data-stu-id="184db-395">'Set-AzSqlDatabase'</span></span>

#### <a name="azstorage"></a><span data-ttu-id="184db-396">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="184db-396">Az.Storage</span></span>
* <span data-ttu-id="184db-397">최대 4TiB까지 Azure 파일 업로드 지원됨</span><span class="sxs-lookup"><span data-stu-id="184db-397">Supported upload Azure File size up to 4 TiB</span></span>
    - <span data-ttu-id="184db-398">'Set-AzStorageFileContent'</span><span class="sxs-lookup"><span data-stu-id="184db-398">'Set-AzStorageFileContent'</span></span>
* <span data-ttu-id="184db-399">Azure.Storage.Blobs를 12.7.0으로 업그레이드</span><span class="sxs-lookup"><span data-stu-id="184db-399">Upgraded Azure.Storage.Blobs to 12.7.0</span></span>
* <span data-ttu-id="184db-400">Azure.Storage.Files.Shares를 12.5.0으로 업그레이드</span><span class="sxs-lookup"><span data-stu-id="184db-400">Upgraded Azure.Storage.Files.Shares to 12.5.0</span></span>
* <span data-ttu-id="184db-401">Azure.Storage.Files.DataLake를 12.5.0으로 업그레이드</span><span class="sxs-lookup"><span data-stu-id="184db-401">Upgraded Azure.Storage.Files.DataLake to 12.5.0</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="184db-402">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="184db-402">Az.StorageSync</span></span>
* <span data-ttu-id="184db-403">다운로드 정책 및 로컬 캐시 모드가 포함된 동기화 계층화 정책 기능 추가됨</span><span class="sxs-lookup"><span data-stu-id="184db-403">Added Sync tiering policy feature with download policy and local cache mode</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="184db-404">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="184db-404">Az.Websites</span></span>
* <span data-ttu-id="184db-405">중복 액세스 제한 규칙 방지</span><span class="sxs-lookup"><span data-stu-id="184db-405">Prevent duplicate access restriction rules</span></span>

### <a name="thanks-to-our-community-contributors"></a><span data-ttu-id="184db-406">커뮤니티 기여자에게 감사드립니다.</span><span class="sxs-lookup"><span data-stu-id="184db-406">Thanks to our community contributors</span></span>
* <span data-ttu-id="184db-407">Andrew Dawson(@dawsonar802), Get-AzKeyVaultCertificate.md 업데이트 - 인증서를 가져와서 PowerShell Core에서 작동하도록 pfx 섹션으로 저장(#13557)</span><span class="sxs-lookup"><span data-stu-id="184db-407">Andrew Dawson (@dawsonar802), Update Get-AzKeyVaultCertificate.md - Get cert and save it as pfx section to work with PowerShell Core (#13557)</span></span>
* <span data-ttu-id="184db-408">@iviark, 의료 API Powershell BYOK 업데이트(#13518)</span><span class="sxs-lookup"><span data-stu-id="184db-408">@iviark, Healthcare APIs Powershell BYOK Updates (#13518)</span></span>
* <span data-ttu-id="184db-409">John Duckmanton(@johnduckmanton) TagPatchOperation의 철자 수정(#13508)</span><span class="sxs-lookup"><span data-stu-id="184db-409">John Duckmanton (@johnduckmanton), Correct spelling of TagPatchOperation (#13508)</span></span>
* <span data-ttu-id="184db-410">Michael James(@mikejwhat)</span><span class="sxs-lookup"><span data-stu-id="184db-410">Michael James (@mikejwhat)</span></span>
  * <span data-ttu-id="184db-411">AzLogicAppRunHistory 도움말 정리(#13513)</span><span class="sxs-lookup"><span data-stu-id="184db-411">Get-AzLogicAppRunHistory Help Tidy (#13513)</span></span>
* <span data-ttu-id="184db-412">Richard de Zwart(@mountain65)</span><span class="sxs-lookup"><span data-stu-id="184db-412">Richard de Zwart (@mountain65)</span></span>
  * <span data-ttu-id="184db-413">Update-AzAppConfigurationStore.md 업데이트(#13485)</span><span class="sxs-lookup"><span data-stu-id="184db-413">Update Update-AzAppConfigurationStore.md (#13485)</span></span>
  * <span data-ttu-id="184db-414">New-AzCosmosDBAccount.md 업데이트(#13490)</span><span class="sxs-lookup"><span data-stu-id="184db-414">Update New-AzCosmosDBAccount.md (#13490)</span></span>
* <span data-ttu-id="184db-415">@SteppingRazor, New-AzApiManagementProduct: SubscriptionsLimit 매개 변수 기본값을 None으로 변경(#13457)</span><span class="sxs-lookup"><span data-stu-id="184db-415">@SteppingRazor, New-AzApiManagementProduct: Change SubscriptionsLimit parameter default value to None (#13457)</span></span>
* <span data-ttu-id="184db-416">Steve Burkett(@SteveBurkettNZ), 예에서 WorkspaceResourceId 매개 변수의 오타 수정(#13589).</span><span class="sxs-lookup"><span data-stu-id="184db-416">Steve Burkett (@SteveBurkettNZ), Fix Typo for WorkspaceResourceId parameter in example (#13589)</span></span>

## <a name="510---november-2020"></a><span data-ttu-id="184db-417">5.1.0 - 2020년 11월</span><span class="sxs-lookup"><span data-stu-id="184db-417">5.1.0 - November 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="184db-418">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="184db-418">Az.Accounts</span></span>
* <span data-ttu-id="184db-419">'Connect-AzAccount -DeviceCode'를 사용하는 경우 TenantId가 적용되지 않을 수 있는 문제가 해결됨 [#13477]</span><span class="sxs-lookup"><span data-stu-id="184db-419">Fixed an issue that TenantId may be not respected if using 'Connect-AzAccount -DeviceCode'[#13477]</span></span>
* <span data-ttu-id="184db-420">새 cmdlet 'Get-AzAccessToken'이 추가됨</span><span class="sxs-lookup"><span data-stu-id="184db-420">Added new cmdlet 'Get-AzAccessToken'</span></span>
* <span data-ttu-id="184db-421">사용자 프로필 경로에 액세스할 수 없는 경우 오류가 발생하는 문제가 해결됨</span><span class="sxs-lookup"><span data-stu-id="184db-421">Fixed an issue that error happens if user profile path is inaccessible</span></span>
* <span data-ttu-id="184db-422">Connect-AzAccount 중에 쓰기-개체 오류가 발생하는 문제가 해결됨 [#13419]</span><span class="sxs-lookup"><span data-stu-id="184db-422">Fixed an issue causing Write-Object error during Connect-AzAccount [#13419]</span></span>
* <span data-ttu-id="184db-423">'ContainerRegistryEndpointSuffix' 매개 변수가 'Add-AzEnvironment' 및 'Set-AzEnvironment'에 추가됨</span><span class="sxs-lookup"><span data-stu-id="184db-423">Added parameter 'ContainerRegistryEndpointSuffix' to: 'Add-AzEnvironment', 'Set-AzEnvironment'</span></span> 
* <span data-ttu-id="184db-424"><kbd>CTRL</kbd>+<kbd>C</kbd> 키를 눌러 로그인을 중단하는 기능이 지원됨</span><span class="sxs-lookup"><span data-stu-id="184db-424">Supported interrupting login by hitting <kbd>CTRL</kbd>+<kbd>C</kbd></span></span>
* <span data-ttu-id="184db-425">'Connect-AzAccount -KeyVaultAccessToken'이 작동하지 않는 문제가 해결됨 [#13127]</span><span class="sxs-lookup"><span data-stu-id="184db-425">Fixed an issue causing 'Connect-AzAccount -KeyVaultAccessToken' not working [#13127]</span></span>
* <span data-ttu-id="184db-426">'Invoke-AzRestMethod'에서 null 참조 및 메서드 대/소문자를 구분하지 않는 문제가 해결됨</span><span class="sxs-lookup"><span data-stu-id="184db-426">Fixed null reference and method case insensitive in 'Invoke-AzRestMethod'</span></span>

#### <a name="azaks"></a><span data-ttu-id="184db-427">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="184db-427">Az.Aks</span></span>
* <span data-ttu-id="184db-428">사용자가 서비스 주체를 사용하여 새 Kubernetes 클러스터를 만들 수 없는 문제가 해결됨</span><span class="sxs-lookup"><span data-stu-id="184db-428">Fixed the issue that user cannot use service principal to create a new Kubernetes cluster.</span></span> <span data-ttu-id="184db-429">[#13012]</span><span class="sxs-lookup"><span data-stu-id="184db-429">[#13012]</span></span>

#### <a name="azappconfiguration"></a><span data-ttu-id="184db-430">Az.AppConfiguration</span><span class="sxs-lookup"><span data-stu-id="184db-430">Az.AppConfiguration</span></span>
* <span data-ttu-id="184db-431">'Az.AppConfiguration' 모듈의 일반 공급</span><span class="sxs-lookup"><span data-stu-id="184db-431">General availability of 'Az.AppConfiguration' module</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="184db-432">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="184db-432">Az.DataFactory</span></span>
* <span data-ttu-id="184db-433">'New-AzDataFactoryV2LinkedServiceEncryptedCredential' 명령의 오류 메시지가 개선됨</span><span class="sxs-lookup"><span data-stu-id="184db-433">Improved error message of 'New-AzDataFactoryV2LinkedServiceEncryptedCredential' command</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="184db-434">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="184db-434">Az.DataLakeStore</span></span>
* <span data-ttu-id="184db-435">ADLS 데이터 평면 SDK가 1.2.4로 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="184db-435">Updated ADLS dataplane SDK to 1.2.4-alpha.</span></span> <span data-ttu-id="184db-436">변경 내용: https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-124-alpha</span><span class="sxs-lookup"><span data-stu-id="184db-436">Changes:https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-124-alpha</span></span>

#### <a name="azdesktopvirtualization"></a><span data-ttu-id="184db-437">Az.DesktopVirtualization</span><span class="sxs-lookup"><span data-stu-id="184db-437">Az.DesktopVirtualization</span></span>
* <span data-ttu-id="184db-438">새 MSIX 패키지 cmdlet 및 업데이트된 애플리케이션 cmdlet이 추가됨</span><span class="sxs-lookup"><span data-stu-id="184db-438">Added new MSIX Package cmdlets and updated Applications cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="184db-439">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="184db-439">Az.EventHub</span></span>
* <span data-ttu-id="184db-440">태그가 없는 EventHub 클러스터에 대한 클러스터 명령이 수정됨</span><span class="sxs-lookup"><span data-stu-id="184db-440">Fixed Cluster commands for EventHub cluster without tags</span></span>
* <span data-ttu-id="184db-441">AzEventHubGeoDRConfiguration 명령의 PartnerNamespace에 대한 도움말 텍스트가 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="184db-441">Updated help text for PartnerNamespace of AzEventHubGeoDRConfiguration commands</span></span> 

#### <a name="azhdinsight"></a><span data-ttu-id="184db-442">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="184db-442">Az.HDInsight</span></span>
* <span data-ttu-id="184db-443">릴레이 아웃바운드 및 프라이빗 링크 기능을 지원하기 위해 cmdlet 'New-AzHDInsightCluster'에 'ResourceProviderConnection' 및 'PrivateLink' 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="184db-443">Add parameters 'ResourceProviderConnection' and 'PrivateLink' to cmdlet 'New-AzHDInsightCluster' to support relay outbound and private link feature</span></span>
* <span data-ttu-id="184db-444">사용자 지정 Ambari 데이터베이스 기능을 지원하기 위해 cmdlet 'New-AzHDInsightCluster'에 'AmbariDatabase' 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="184db-444">Add parameter 'AmbariDatabase' to cmdlet 'New-AzHDInsightCluster' to support custom Ambari database feature</span></span>
* <span data-ttu-id="184db-445">cmdlet 'Add-AzHDInsightMetastore'의 'MetastoreType' 매개 변수에 accept 값 'AmbariDatabase' 추가</span><span class="sxs-lookup"><span data-stu-id="184db-445">Add accept value 'AmbariDatabase' to the parameter 'MetastoreType' of the cmdlet 'Add-AzHDInsightMetastore'</span></span>

#### <a name="aziothub"></a><span data-ttu-id="184db-446">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="184db-446">Az.IotHub</span></span>
* <span data-ttu-id="184db-447">IoT Hub create cmdlet에서 태그 허용</span><span class="sxs-lookup"><span data-stu-id="184db-447">Allowed tags in IoT Hub create cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="184db-448">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="184db-448">Az.KeyVault</span></span>
* <span data-ttu-id="184db-449">key vault 태그 업데이트 지원</span><span class="sxs-lookup"><span data-stu-id="184db-449">Supported updating key vault tag</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="184db-450">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="184db-450">Az.LogicApp</span></span>
* <span data-ttu-id="184db-451">Get-AzLogicAppRunHistory가 결과의 첫 번째 페이지만 검색하도록 수정됨</span><span class="sxs-lookup"><span data-stu-id="184db-451">Fixed for Get-AzLogicAppRunHistory only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="184db-452">Az.Network</span><span class="sxs-lookup"><span data-stu-id="184db-452">Az.Network</span></span>
* <span data-ttu-id="184db-453">아래 cmdlet이 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="184db-453">Updated below cmdlet</span></span> 
    - <span data-ttu-id="184db-454">'New-AzLoadBalancerFrontendIpConfigCommand', 'Set-AzLoadBalancerFrontendIpConfigCommand', 'Add-AzLoadBalancerFrontendIpConfigCommand':</span><span class="sxs-lookup"><span data-stu-id="184db-454">'New-AzLoadBalancerFrontendIpConfigCommand', 'Set-AzLoadBalancerFrontendIpConfigCommand', 'Add-AzLoadBalancerFrontendIpConfigCommand':</span></span>
        - <span data-ttu-id="184db-455">PublicIpAddressPrefix 속성이 추가됨</span><span class="sxs-lookup"><span data-stu-id="184db-455">Added PublicIpAddressPrefix property</span></span>
        - <span data-ttu-id="184db-456">PublicIpAddressPrefixId 속성이 추가됨</span><span class="sxs-lookup"><span data-stu-id="184db-456">Added PublicIpAddressPrefixId property</span></span>
* <span data-ttu-id="184db-457">글로벌 부하 분산을 허용하도록 다음 cmdlet에 새 속성이 추가됨</span><span class="sxs-lookup"><span data-stu-id="184db-457">Added new properties to the following cmdlets to allow for global load balancing</span></span>
    - <span data-ttu-id="184db-458">'New-AzLoadBalancer':</span><span class="sxs-lookup"><span data-stu-id="184db-458">'New-AzLoadBalancer':</span></span>
        - <span data-ttu-id="184db-459">Sku 계층 속성이 추가됨</span><span class="sxs-lookup"><span data-stu-id="184db-459">Added Sku Tier property</span></span>
    - <span data-ttu-id="184db-460">'New-AzPuplicIpAddress':</span><span class="sxs-lookup"><span data-stu-id="184db-460">'New-AzPuplicIpAddress':</span></span>
        - <span data-ttu-id="184db-461">Sku 계층 속성이 추가됨</span><span class="sxs-lookup"><span data-stu-id="184db-461">Added Sku Tier property</span></span>
    - <span data-ttu-id="184db-462">'New-AzPublicIpPrefix':</span><span class="sxs-lookup"><span data-stu-id="184db-462">'New-AzPublicIpPrefix':</span></span>
        - <span data-ttu-id="184db-463">Sku 계층 속성이 추가됨</span><span class="sxs-lookup"><span data-stu-id="184db-463">Added Sku Tier property</span></span>
    - <span data-ttu-id="184db-464">'New-AzLoadBalancerBackendAddressConfig':</span><span class="sxs-lookup"><span data-stu-id="184db-464">'New-AzLoadBalancerBackendAddressConfig':</span></span>
        - <span data-ttu-id="184db-465">LoadBalancerFrontendIPConfigurationId 속성이 추가됨</span><span class="sxs-lookup"><span data-stu-id="184db-465">Added LoadBalancerFrontendIPConfigurationId property</span></span>
* <span data-ttu-id="184db-466">cmdlet -'New-AzVirtualHubRoute', -'New-AzVirtualHubRouteTable', -'Add-AzVirtualHubRoute', -'Add-AzVirtualHubRouteTable', -'Get-AzVirtualHubRouteTable' 및 -'Remove-AzVirtualHubRouteTable'의 사용 중지 예정 경고가 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="184db-466">Updated planning to deprecate warnings for the following cmdlets   -'New-AzVirtualHubRoute'   -'New-AzVirtualHubRouteTable'   -'Add-AzVirtualHubRoute'   -'Add-AzVirtualHubRouteTable'   -'Get-AzVirtualHubRouteTable'   -'Remove-AzVirtualHubRouteTable'</span></span>
* <span data-ttu-id="184db-467">cmdlet -'New-AzVirtualHub', -'Set-AzVirtualHub' 및 -'Update-AzVirtualHub'에 대한 인수 'RouteTable'의 사용 중지 예정 경고가 추가됨</span><span class="sxs-lookup"><span data-stu-id="184db-467">Added planning to deprecate warnings on the argument 'RouteTable' for the following cmdlets   -'New-AzVirtualHub'   -'Set-AzVirtualHub'   -'Update-AzVirtualHub'</span></span>
* <span data-ttu-id="184db-468">'Set-AzExpressRouteGateway'에서 '-MinScaleUnits' 및 '-MaxScaleUnits' 인수가 선택적 인수로 변경됨</span><span class="sxs-lookup"><span data-stu-id="184db-468">Made arguments '-MinScaleUnits' and '-MaxScaleUnits' optional in 'Set-AzExpressRouteGateway'</span></span>
* <span data-ttu-id="184db-469">Application Gateway에서 상호 인증 및 SSL 프로필을 지원하기 위해 새 cmdlet이 추가됨</span><span class="sxs-lookup"><span data-stu-id="184db-469">Added new cmdlets to support Mutual Authentication and SSL Profiles on Application Gateway</span></span>
    - <span data-ttu-id="184db-470">'Get-AzApplicationGatewayClientAuthConfiguration'</span><span class="sxs-lookup"><span data-stu-id="184db-470">'Get-AzApplicationGatewayClientAuthConfiguration'</span></span>
    - <span data-ttu-id="184db-471">'New-AzApplicationGatewayClientAuthConfiguration'</span><span class="sxs-lookup"><span data-stu-id="184db-471">'New-AzApplicationGatewayClientAuthConfiguration'</span></span>
    - <span data-ttu-id="184db-472">'Remove-AzApplicationGatewayClientAuthConfiguration'</span><span class="sxs-lookup"><span data-stu-id="184db-472">'Remove-AzApplicationGatewayClientAuthConfiguration'</span></span>
    - <span data-ttu-id="184db-473">'Set-AzApplicationGatewayClientAuthConfiguration'</span><span class="sxs-lookup"><span data-stu-id="184db-473">'Set-AzApplicationGatewayClientAuthConfiguration'</span></span>
    - <span data-ttu-id="184db-474">'Add-AzApplicationGatewayTrustedClientCertificate'</span><span class="sxs-lookup"><span data-stu-id="184db-474">'Add-AzApplicationGatewayTrustedClientCertificate'</span></span> 
    - <span data-ttu-id="184db-475">'Get-AzApplicationGatewayTrustedClientCertificate'</span><span class="sxs-lookup"><span data-stu-id="184db-475">'Get-AzApplicationGatewayTrustedClientCertificate'</span></span> 
    - <span data-ttu-id="184db-476">'New-AzApplicationGatewayTrustedClientCertificate'</span><span class="sxs-lookup"><span data-stu-id="184db-476">'New-AzApplicationGatewayTrustedClientCertificate'</span></span> 
    - <span data-ttu-id="184db-477">'Remove-AzApplicationGatewayTrustedClientCertificate'</span><span class="sxs-lookup"><span data-stu-id="184db-477">'Remove-AzApplicationGatewayTrustedClientCertificate'</span></span> 
    - <span data-ttu-id="184db-478">'Set-AzApplicationGatewayTrustedClientCertificate'</span><span class="sxs-lookup"><span data-stu-id="184db-478">'Set-AzApplicationGatewayTrustedClientCertificate'</span></span>
    - <span data-ttu-id="184db-479">'Add-AzApplicationGatewaySslProfile'</span><span class="sxs-lookup"><span data-stu-id="184db-479">'Add-AzApplicationGatewaySslProfile'</span></span>
    - <span data-ttu-id="184db-480">'Get-AzApplicationGatewaySslProfile'</span><span class="sxs-lookup"><span data-stu-id="184db-480">'Get-AzApplicationGatewaySslProfile'</span></span>
    - <span data-ttu-id="184db-481">'New-AzApplicationGatewaySslProfile'</span><span class="sxs-lookup"><span data-stu-id="184db-481">'New-AzApplicationGatewaySslProfile'</span></span>
    - <span data-ttu-id="184db-482">'Remove-AzApplicationGatewaySslProfile'</span><span class="sxs-lookup"><span data-stu-id="184db-482">'Remove-AzApplicationGatewaySslProfile'</span></span>
    - <span data-ttu-id="184db-483">'Set-AzApplicationGatewaySslProfile'</span><span class="sxs-lookup"><span data-stu-id="184db-483">'Set-AzApplicationGatewaySslProfile'</span></span>
    - <span data-ttu-id="184db-484">'Get-AzApplicationGatewaySslProfilePolicy'</span><span class="sxs-lookup"><span data-stu-id="184db-484">'Get-AzApplicationGatewaySslProfilePolicy'</span></span>
    - <span data-ttu-id="184db-485">'Remove-AzApplicationGatewaySslProfilePolicy'</span><span class="sxs-lookup"><span data-stu-id="184db-485">'Remove-AzApplicationGatewaySslProfilePolicy'</span></span>
    - <span data-ttu-id="184db-486">'Set-AzApplicationGatewaySslProfilePolicy'</span><span class="sxs-lookup"><span data-stu-id="184db-486">'Set-AzApplicationGatewaySslProfilePolicy'</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="184db-487">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="184db-487">Az.RecoveryServices</span></span>
* <span data-ttu-id="184db-488">정책 BackupTime은 UTC로 지정.</span><span class="sxs-lookup"><span data-stu-id="184db-488">Specifying policy BackupTime is in UTC.</span></span>
* <span data-ttu-id="184db-489">Get-AzRecoveryServicesBackupJobDetails cmdlet에서 호환성이 손상되는 변경에 대한 경고를 수정하는 중</span><span class="sxs-lookup"><span data-stu-id="184db-489">Modifying breaking change warning in Get-AzRecoveryServicesBackupJobDetails cmdlet.</span></span>
* <span data-ttu-id="184db-490">Set-AzRecoveryServicesBackupProtectionPolicy cmdlet에 대한 샘플 스크립트 도움말 텍스트를 업데이트하는 중</span><span class="sxs-lookup"><span data-stu-id="184db-490">Updating sample script help text for Set-AzRecoveryServicesBackupProtectionPolicy cmdlet.</span></span>

#### <a name="azresources"></a><span data-ttu-id="184db-491">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="184db-491">Az.Resources</span></span>
* <span data-ttu-id="184db-492">가상 도구에서 대/소문자가 서로 다른 두 개의 리소스 그룹 범위를 표시하는 문제가 해결됨</span><span class="sxs-lookup"><span data-stu-id="184db-492">Fixed an issue where What-If shows two resource group scopes with different casing</span></span>
* <span data-ttu-id="184db-493">SDK를 사용하도록 'Export-AzResourceGroup'이 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="184db-493">Updated 'Export-AzResourceGroup' to use the SDK.</span></span>
* <span data-ttu-id="184db-494">구문 분석 메서드에 문화권 정보가 추가됨</span><span class="sxs-lookup"><span data-stu-id="184db-494">Added culture info to parse methods</span></span>

#### <a name="azsql"></a><span data-ttu-id="184db-495">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="184db-495">Az.Sql</span></span>
* <span data-ttu-id="184db-496">Set-AzSqlDatabaseAudit가 하이퍼스케일 데이터베이스를 지원하지 않아 데이터베이스 버전을 확인할 수 없는 문제가 해결됨</span><span class="sxs-lookup"><span data-stu-id="184db-496">Fixed issues where Set-AzSqlDatabaseAudit were not support Hyperscale database and database edition cannot be determined</span></span>
* <span data-ttu-id="184db-497">'New-AzSqlInstance' 및 'Set-AzSqlInstance'에 MaintenanceConfigurationId가 추가됨</span><span class="sxs-lookup"><span data-stu-id="184db-497">Added MaintenanceConfigurationId to 'New-AzSqlInstance' and 'Set-AzSqlInstance'</span></span>
* <span data-ttu-id="184db-498">PartnerServerName 매개 변수가 키가 아닌 값으로 확인되는 GetAzureSqlDatabaseReplicationLink.cs의 버그가 해결됨</span><span class="sxs-lookup"><span data-stu-id="184db-498">Fixed a bug in GetAzureSqlDatabaseReplicationLink.cs where PartnerServerName parameter was being checked for by value instead of key</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="184db-499">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="184db-499">Az.Websites</span></span>
* <span data-ttu-id="184db-500">다음과 같은 새 액세스 제한 기능에 대한 지원이 추가됨: ServiceTag, 다중 ip 및 http 헤더</span><span class="sxs-lookup"><span data-stu-id="184db-500">Added support for new access restriction features: ServiceTag, multi-ip and http-headers</span></span>

### <a name="thanks-to-our-community-contributors"></a><span data-ttu-id="184db-501">커뮤니티 기여자에게 감사드립니다.</span><span class="sxs-lookup"><span data-stu-id="184db-501">Thanks to our community contributors</span></span>
* <span data-ttu-id="184db-502">John Q. Martin(@johnmart82), 방화벽 필수 조건 정보 추가(#13385)</span><span class="sxs-lookup"><span data-stu-id="184db-502">John Q. Martin (@johnmart82), Adding firewall prerequisite information (#13385)</span></span>
* <span data-ttu-id="184db-503">Manikandan Duraisamy(@madurais-msft), PublicSubnetName 인수 수정(#13417)</span><span class="sxs-lookup"><span data-stu-id="184db-503">Manikandan Duraisamy (@madurais-msft), Corrected the PublicSubnetName argument (#13417)</span></span>
* <span data-ttu-id="184db-504">@mahortas, -HostNames 매개 변수 값 업데이트(#13349)</span><span class="sxs-lookup"><span data-stu-id="184db-504">@mahortas, Update for -HostNames parameter values (#13349)</span></span>
* <span data-ttu-id="184db-505">@MariachiForHire, 지원되는 TrafficAnalyticsInterval 값 추가(#13304)</span><span class="sxs-lookup"><span data-stu-id="184db-505">@MariachiForHire, added supported TrafficAnalyticsInterval values (#13304)</span></span>
* <span data-ttu-id="184db-506">Michael James(@mikejwhat), Get-AzLogicAppRunHistory에서 30개를 초과하는 항목을 반환할 수 있도록 허용(#13393)</span><span class="sxs-lookup"><span data-stu-id="184db-506">Michael James (@mikejwhat), Allow Get-AzLogicAppRunHistory to return more than 30 entries (#13393)</span></span>
* <span data-ttu-id="184db-507">Shashikant Shakya(@shshakya), Restore-AzSqlInstanceDatabase.md 업데이트(#13404)</span><span class="sxs-lookup"><span data-stu-id="184db-507">Shashikant Shakya (@shshakya), Update Restore-AzSqlInstanceDatabase.md (#13404)</span></span>

## <a name="500---october-2020"></a><span data-ttu-id="184db-508">5.0.0 - 2020년 10월</span><span class="sxs-lookup"><span data-stu-id="184db-508">5.0.0 - October 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="184db-509">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="184db-509">Az.Accounts</span></span>
* <span data-ttu-id="184db-510">[호환성이 손상되는 변경] 'Get-AzProfile' 및 'Select-AzProfile'이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-510">[Breaking Change] Removed 'Get-AzProfile' and 'Select-AzProfile'</span></span>
* <span data-ttu-id="184db-511">Azure Directory 인증 라이브러리가 MSAL(Microsoft 인증 라이브러리)로 대체되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-511">Replaced Azure Directory Authentication Library with Microsoft Authentication Library(MSAL)</span></span>

#### <a name="azaks"></a><span data-ttu-id="184db-512">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="184db-512">Az.Aks</span></span>
* <span data-ttu-id="184db-513">[호환성이 손상되는 변경] 'New-AzAksCluster' 및 'Set-AzAksCluster'에서 매개 변수 별칭 'ClientIdAndSecret'이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-513">[Breaking Change] Removed parameter alias 'ClientIdAndSecret' in 'New-AzAksCluster' and 'Set-AzAksCluster'.</span></span>
* <span data-ttu-id="184db-514">[호환성이 손상되는 변경] 'New-AzAksCluster'의 'NodeVmSetType' 기본값이 'AvailabilitySet'에서 'VirtualMachineScaleSets'로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-514">[Breaking Change] Changed the default value of 'NodeVmSetType' in 'New-AzAksCluster' from 'AvailabilitySet' to 'VirtualMachineScaleSets'.</span></span>
* <span data-ttu-id="184db-515">[호환성이 손상되는 변경] 'New-AzAksCluster'의 'NetworkPlugin' 기본값이 'None'에서 'azure'로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-515">[Breaking Change] Changed the default value of 'NetworkPlugin' in 'New-AzAksCluster' from 'None' to 'azure'.</span></span>
* <span data-ttu-id="184db-516">[호환성이 손상되는 변경] 'New-AzAksCluster'의 'NodeOsType' 매개 변수는 Linux라는 하나의 값만 지원하므로 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-516">[Breaking Change] Removed parameter 'NodeOsType' in 'New-AzAksCluster' as it supports only one value Linux.</span></span>

#### <a name="azbilling"></a><span data-ttu-id="184db-517">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="184db-517">Az.Billing</span></span>
* <span data-ttu-id="184db-518">'Get-AzBillingAccount' cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-518">Added 'Get-AzBillingAccount' cmdlet</span></span>
* <span data-ttu-id="184db-519">'Get-AzBillingProfile' cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-519">Added 'Get-AzBillingProfile' cmdlet</span></span>
* <span data-ttu-id="184db-520">'Get-AzInvoiceSection' cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-520">Added 'Get-AzInvoiceSection' cmdlet</span></span>
* <span data-ttu-id="184db-521">'Get-AzBillingInvoice' cmdlet에 새 매개 변수가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-521">Added new parameters in 'Get-AzBillingInvoice' cmdlet</span></span>
* <span data-ttu-id="184db-522">Get-AzBillingInvoice cmdlet의 응답에서 DownloadUrlExpiry, Type, BillingPeriodNames 속성이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-522">Removed properties DownloadUrlExpiry, Type, BillingPeriodNames from the response of Get-AzBillingInvoice cmdlet</span></span>

#### <a name="azcdn"></a><span data-ttu-id="184db-523">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="184db-523">Az.Cdn</span></span>
* <span data-ttu-id="184db-524">다중 원본 및 프라이빗 링크 기능을 지원하는 cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-524">Added cmdlets to support multi-origin and private link functionality</span></span> 

#### <a name="azcognitiveservices"></a><span data-ttu-id="184db-525">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="184db-525">Az.CognitiveServices</span></span>
* <span data-ttu-id="184db-526">SDK가 7.4.0-preview로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-526">Updated SDK to 7.4.0-preview.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="184db-527">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="184db-527">Az.Compute</span></span>
* <span data-ttu-id="184db-528">'New-AzVm'에 '-VmssId' 매개 변수가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-528">Added '-VmssId' parameter to 'New-AzVm'</span></span>
* <span data-ttu-id="184db-529">'New-AzVmss' cmdlet에 'PlatformFaultDomainCount' 매개 변수가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-529">Added 'PlatformFaultDomainCount' parameter to the 'New-AzVmss' cmdlet.</span></span>
* <span data-ttu-id="184db-530">새 cmdlet 'Get-AzDiskEncryptionSetAssociatedResource'</span><span class="sxs-lookup"><span data-stu-id="184db-530">New cmdlet 'Get-AzDiskEncryptionSetAssociatedResource'</span></span>
* <span data-ttu-id="184db-531">New-AzDiskConfig cmdlet에 선택적 매개 변수 'Tier' 및 'LogicalSectorSize'가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-531">Added 'Tier' and 'LogicalSectorSize' optional parameters to the New-AzDiskConfig cmdlet.</span></span> 
* <span data-ttu-id="184db-532">'New-AzDiskUpdateConfig' cmdlet에 선택적 매개 변수 'Tier', 'MaxSharesCount', 'DiskIOPSReadOnly' 및 'DiskMBpsReadOnly'가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-532">Added 'Tier', 'MaxSharesCount', 'DiskIOPSReadOnly', and 'DiskMBpsReadOnly' optional parameters to the 'New-AzDiskUpdateConfig' cmdlet.</span></span> 

#### <a name="azcontainerregistry"></a><span data-ttu-id="184db-533">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="184db-533">Az.ContainerRegistry</span></span>
* <span data-ttu-id="184db-534">[호환성이 손상되는 변경] API 버전이 2019-05-01로 업데이트됩니다.</span><span class="sxs-lookup"><span data-stu-id="184db-534">[Breaking Change] Updates API version to 2019-05-01</span></span>
* <span data-ttu-id="184db-535">[호환성이 손상되는 변경] 'New-AzContainerRegistry'에서 SKU 'Classic' 및 'StorageAccountName' 매개 변수가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-535">[Breaking Change] Removed SKU 'Classic' and parameter 'StorageAccountName' from 'New-AzContainerRegistry'</span></span>
* <span data-ttu-id="184db-536">새 cmdlet이 추가되었습니다. 'Connect-AzContainerRegistry', 'Import-AzContainerRegistry', 'Get-AzContainerRegistryUsage', 'New-AzContainerRegistryNetworkRule', 'Set-AzContainerRegistryNetworkRule'</span><span class="sxs-lookup"><span data-stu-id="184db-536">Added New cmdlets: 'Connect-AzContainerRegistry', 'Import-AzContainerRegistry', 'Get-AzContainerRegistryUsage', 'New-AzContainerRegistryNetworkRule', 'Set-AzContainerRegistryNetworkRule'</span></span>
* <span data-ttu-id="184db-537">'Update-AzContainerRegistry'에 새 매개 변수 'NetworkRuleSet'가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-537">Added new parameter 'NetworkRuleSet' to 'Update-AzContainerRegistry'</span></span>

#### <a name="azdatabricks"></a><span data-ttu-id="184db-538">Az.Databricks</span><span class="sxs-lookup"><span data-stu-id="184db-538">Az.Databricks</span></span>
* <span data-ttu-id="184db-539">`-EncryptionKeyVersion`이 없으면 databricks 작업 영역 업데이트가 실패하는 버그가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-539">Fixed a bug that may cause updating databricks workspace without `-EncryptionKeyVersion` to fail.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="184db-540">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="184db-540">Az.DataFactory</span></span>
* <span data-ttu-id="184db-541">ADF .Net SDK 버전이 4.12.0으로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-541">Updated ADF .Net SDK version to 4.12.0</span></span>
* <span data-ttu-id="184db-542">ADF 암호화 클라이언트 SDK 버전이 4.14.7587.7로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-542">Updated ADF encryption client SDK version to 4.14.7587.7</span></span>
* <span data-ttu-id="184db-543">'Stop-AzDataFactoryV2TriggerRun' 및 'Invoke-AzDataFactoryV2TriggerRun' 명령이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-543">Added 'Stop-AzDataFactoryV2TriggerRun' and 'Invoke-AzDataFactoryV2TriggerRun' commands</span></span>

#### <a name="azdesktopvirtualization"></a><span data-ttu-id="184db-544">Az.DesktopVirtualization</span><span class="sxs-lookup"><span data-stu-id="184db-544">Az.DesktopVirtualization</span></span>
* <span data-ttu-id="184db-545">최상위 arm 개체를 만들려면 Location 속성이 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="184db-545">Require Location property for creating top level arm objects.</span></span>
        <span data-ttu-id="184db-546">\* `New-AzWvdApplicationGroup`에 `ApplicationGroupType`이 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="184db-546">\* Made `ApplicationGroupType` required for `New-AzWvdApplicationGroup`.</span></span>
        <span data-ttu-id="184db-547">\* `New-AzWvdApplicationGroup`에 `HostPoolArmPath`가 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="184db-547">\* Made `HostPoolArmPath` required for `New-AzWvdApplicationGroup`.</span></span>
        <span data-ttu-id="184db-548">\* `New-AzWvdHostPool`에 `PreferredAppGroupType`이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-548">\* Added `PreferredAppGroupType` for `New-AzWvdHostPool`.</span></span>

#### <a name="azfunctions"></a><span data-ttu-id="184db-549">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="184db-549">Az.Functions</span></span>
* <span data-ttu-id="184db-550">[호환성이 손상되는 변경] 'Get-AzFunctionApp' 매개 변수 세트 하나를 제외한 모든 매개 변수 세트에서 'IncludeSlot' 스위치 매개 변수가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-550">[Breaking Change] Removed 'IncludeSlot' switch parameter from all but one parameter set of 'Get-AzFunctionApp'.</span></span> <span data-ttu-id="184db-551">이제 이 cmdlet은 '-IncludeSlot'이 지정된 경우 결과에서 배포 슬롯 검색을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="184db-551">The cmdlet now supports retrieving deployment slots in the results when '-IncludeSlot' is specified.</span></span> 
* <span data-ttu-id="184db-552">'New-AzFunctionApp'이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-552">Updated 'New-AzFunctionApp':</span></span>
  - <span data-ttu-id="184db-553">이 옵션을 지정할 경우 application insights 프로젝트가 생성되지 않도록 -DisableApplicationInsights가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-553">Fixed -DisableApplicationInsights so that no application insights project is created when this option is specified.</span></span> <span data-ttu-id="184db-554">[#12728]</span><span class="sxs-lookup"><span data-stu-id="184db-554">[#12728]</span></span>
  - <span data-ttu-id="184db-555">[호환성이 손상되는 변경] PowerShell 6.2 함수 앱을 만드는 지원 기능이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-555">[Breaking Change] Removed support to create PowerShell 6.2 function apps.</span></span>
  - <span data-ttu-id="184db-556">[호환성이 손상되는 변경] RuntimeVersion 매개 변수가 지정되지 않은 경우 PowerShell 함수 앱에 대한 Windows의 Functions 버전 3 기본 런타임 버전이 6.2에서 7.0으로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-556">[Breaking Change] Changed the default runtime version in Functions version 3 on Windows for PowerShell function apps from 6.2 to 7.0 when the RuntimeVersion parameter is not specified.</span></span>
  - <span data-ttu-id="184db-557">[호환성이 손상되는 변경] RuntimeVersion 매개 변수가 지정되지 않은 경우 Node 함수 앱에 대한 Windows 및 Linux의 Functions 버전 3 기본 런타임 버전이 10에서 12로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-557">[Breaking Change] Changed the default runtime version in Functions version 3 on Windows and Linux for Node function apps from 10 to 12 when the RuntimeVersion parameter is not specified.</span></span>
  - <span data-ttu-id="184db-558">[호환성이 손상되는 변경] RuntimeVersion 매개 변수가 지정되지 않은 경우 Python 함수 앱에 대한 Linux의 Functions 버전 3 기본 런타임 버전이 3.7에서 3.8로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-558">[Breaking Change] Changed the default runtime version in Functions version 3 on Linux for Python function apps from 3.7 to 3.8 when the RuntimeVersion parameter is not specified.</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="184db-559">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="184db-559">Az.HDInsight</span></span>
 * <span data-ttu-id="184db-560">AzHDInsightCluster cmdlet의 경우:</span><span class="sxs-lookup"><span data-stu-id="184db-560">For New-AzHDInsightCluster cmdlet:</span></span>
     - <span data-ttu-id="184db-561">'DefaultStorageAccountName' 매개 변수가 'StorageAccountResourceId'로 대체되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-561">Replaced parameter 'DefaultStorageAccountName' with 'StorageAccountResourceId'</span></span>
     - <span data-ttu-id="184db-562">'DefaultStorageAccountKey' 매개 변수가 'StorageAccountKey'로 대체되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-562">Replaced parameter 'DefaultStorageAccountKey' with 'StorageAccountKey'</span></span>
     - <span data-ttu-id="184db-563">'DefaultStorageAccountType' 매개 변수가 'StorageAccountType'으로 대체되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-563">Replaced parameter 'DefaultStorageAccountType' with 'StorageAccountType'</span></span>
     - <span data-ttu-id="184db-564">'PublicNetworkAccessType' 매개 변수가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-564">Removed parameter 'PublicNetworkAccessType'</span></span>
     - <span data-ttu-id="184db-565">'OutboundPublicNetworkAccessType' 매개 변수가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-565">Removed parameter 'OutboundPublicNetworkAccessType'</span></span>
     - <span data-ttu-id="184db-566">새 매개 변수가 추가되었습니다. ADLSGen2를 지원하기 위한 'StorageFileSystem' 및 'StorageAccountManagedIdentity'</span><span class="sxs-lookup"><span data-stu-id="184db-566">Added new parameters: 'StorageFileSystem' and 'StorageAccountManagedIdentity' to support ADLSGen2</span></span>
     - <span data-ttu-id="184db-567">HDInsight ID Broker를 지원하기 위해 새 매개 변수 'EnableIDBroker'가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-567">Added new parameter 'EnableIDBroker' to Support HDInsight ID Broker</span></span>
     - <span data-ttu-id="184db-568">새 매개 변수가 추가되었습니다. Kafka Rest Proxy를 지원하기 위한 'KafkaClientGroupId', 'KafkaClientGroupName' 및 'KafkaManagementNodeSize'</span><span class="sxs-lookup"><span data-stu-id="184db-568">Added new parameters: 'KafkaClientGroupId', 'KafkaClientGroupName' and 'KafkaManagementNodeSize' to support Kafka Rest Proxy</span></span>
 * <span data-ttu-id="184db-569">New-AzHDInsightClusterConfig cmdlet의 경우:</span><span class="sxs-lookup"><span data-stu-id="184db-569">For New-AzHDInsightClusterConfig cmdlet:</span></span>
     - <span data-ttu-id="184db-570">'DefaultStorageAccountName' 매개 변수가 'StorageAccountResourceId'로 대체되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-570">Replaced parameter 'DefaultStorageAccountName' with 'StorageAccountResourceId'</span></span>
     - <span data-ttu-id="184db-571">'DefaultStorageAccountKey' 매개 변수가 'StorageAccountKey'로 대체되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-571">Replaced parameter 'DefaultStorageAccountKey' with 'StorageAccountKey'</span></span>
     - <span data-ttu-id="184db-572">'DefaultStorageAccountType' 매개 변수가 'StorageAccountType'으로 대체되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-572">Replaced parameter 'DefaultStorageAccountType' with 'StorageAccountType'</span></span>
     - <span data-ttu-id="184db-573">'PublicNetworkAccessType' 매개 변수가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-573">Removed parameter 'PublicNetworkAccessType'</span></span>
     - <span data-ttu-id="184db-574">'OutboundPublicNetworkAccessType' 매개 변수가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-574">Removed parameter 'OutboundPublicNetworkAccessType'</span></span>
* <span data-ttu-id="184db-575">Set-AzHDInsightDefaultStorage cmdlet의 경우:</span><span class="sxs-lookup"><span data-stu-id="184db-575">For Set-AzHDInsightDefaultStorage cmdlet:</span></span>
    - <span data-ttu-id="184db-576">'StorageAccountName' 매개 변수가 'StorageAccountResourceId'로 대체되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-576">Replaced parameter 'StorageAccountName' with 'StorageAccountResourceId'</span></span>
* <span data-ttu-id="184db-577">Add-AzHDInsightSecurityProfile cmdlet의 경우:</span><span class="sxs-lookup"><span data-stu-id="184db-577">For Add-AzHDInsightSecurityProfile cmdlet:</span></span>
    - <span data-ttu-id="184db-578">'Domain' 매개 변수가 'DomainResourceId'로 대체되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-578">Replaced parameter 'Domain' with 'DomainResourceId'</span></span>
    - <span data-ttu-id="184db-579">'OrganizationalUnitDN' 매개 변수에 대한 필수 요구 사항이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-579">Removed the mandatory requirement for parameter 'OrganizationalUnitDN'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="184db-580">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="184db-580">Az.KeyVault</span></span>
* <span data-ttu-id="184db-581">[호환성이 손상되는 변경] 'New-AzKeyVault'의 DisableSoftDelete 매개 변수와 'Update-AzKeyVault'의 EnableSoftDelete 매개 변수가 더 이상 사용되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-581">[Breaking Change] Deprecated parameter DisableSoftDelete in 'New-AzKeyVault' and EnableSoftDelete in 'Update-AzKeyVault'</span></span>
* <span data-ttu-id="184db-582">[호환성이 손상되는 변경] SecretValue를 직접 표시하지 않도록 SecretValueText 특성이 제거되었습니다. [#12266]</span><span class="sxs-lookup"><span data-stu-id="184db-582">[Breaking Change] Removed attribute SecretValueText to avoid displaying SecretValue directly [#12266]</span></span>
* <span data-ttu-id="184db-583">새 리소스 유형 지원: 관리형 HSM</span><span class="sxs-lookup"><span data-stu-id="184db-583">Supported new resource type: managed HSM</span></span>
    - <span data-ttu-id="184db-584">관리형 HSM의 CRUD와 관리형 HSM에서 키를 작동하는 cmdlet</span><span class="sxs-lookup"><span data-stu-id="184db-584">CRUD of managed HSM and cmdlets to operate keys on managed HSM</span></span>
    - <span data-ttu-id="184db-585">전체 HSM 백업/복원, AES 키 생성, 보안 도메인 백업/복원, RBAC</span><span class="sxs-lookup"><span data-stu-id="184db-585">Full HSM backup/restore, AES key creation, security domain backup/restore, RBAC</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="184db-586">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="184db-586">Az.ManagedServices</span></span>
* <span data-ttu-id="184db-587">[호환성이 손상되는 변경] 업데이트된 매개 변수 명명 규칙 및 관련 예제</span><span class="sxs-lookup"><span data-stu-id="184db-587">[Breaking Change] Updated parameters naming conventions and associated examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="184db-588">Az.Network</span><span class="sxs-lookup"><span data-stu-id="184db-588">Az.Network</span></span>
* <span data-ttu-id="184db-589">[호환성이 손상되는 변경] 'HostedSubnet' 매개 변수가 제거되고 'Subnet'이 대신 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-589">[Breaking Change] Removed parameter 'HostedSubnet' and added 'Subnet' instead</span></span>
* <span data-ttu-id="184db-590">가상 라우터 피어 경로에 대한 새 cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-590">Added new cmdlets for Virtual Router Peer Routes</span></span>
    - <span data-ttu-id="184db-591">'Get-AzVirtualRouterPeerLearnedRoute'</span><span class="sxs-lookup"><span data-stu-id="184db-591">'Get-AzVirtualRouterPeerLearnedRoute'</span></span>
    - <span data-ttu-id="184db-592">'Get-AzVirtualRouterPeerAdvertisedRoute'</span><span class="sxs-lookup"><span data-stu-id="184db-592">'Get-AzVirtualRouterPeerAdvertisedRoute'</span></span>
* <span data-ttu-id="184db-593">New-AzFirewall cmdlet이 업데이트됨:</span><span class="sxs-lookup"><span data-stu-id="184db-593">Updated New-AzFirewall cmdlet:</span></span>
    - <span data-ttu-id="184db-594">'-SkuTier' 매개 변수가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-594">Added parameter '-SkuTier'</span></span>
    - <span data-ttu-id="184db-595">'-SkuName' 매개 변수가 추가되었으며 Sku가 이 매개 변수의 별칭이 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-595">Added parameter '-SkuName' and made Sku as Alias for this</span></span>
    - <span data-ttu-id="184db-596">'-Sku' 매개 변수가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-596">Removed parameter '-Sku'</span></span>
* <span data-ttu-id="184db-597">[호환성이 손상되는 변경] 'Start-AzVpnConnectionPacketCapture' 및 'Stop-AzVpnConnectionPacketCapture'에서 'Connectionlink' 인수가 필수가 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-597">[Breaking Change] Made 'Connectionlink' argument mandatory in 'Start-AzVpnConnectionPacketCapture' and 'Stop-AzVpnConnectionPacketCapture'</span></span>
* <span data-ttu-id="184db-598">[호환성이 손상되는 변경] '-Filter' 매개 변수를 제거하도록 'New-AzNetworkWatcherConnectionMonitorEndPointObject'가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-598">[Breaking Change] Updated 'New-AzNetworkWatcherConnectionMonitorEndPointObject' to remove parameter '-Filter'</span></span>
* <span data-ttu-id="184db-599">[호환성이 손상되는 변경] 'New-AzNetworkWatcherConnectionMonitorEndpointFilterItemObject' cmdlet이 'New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject'로 대체되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-599">[Breaking Change] Replaced 'New-AzNetworkWatcherConnectionMonitorEndpointFilterItemObject' cmdlet with 'New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject'</span></span>
* <span data-ttu-id="184db-600">'New-AzNetworkWatcherConnectionMonitorEndPointObject' cmdlet이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-600">Updated 'New-AzNetworkWatcherConnectionMonitorEndPointObject' cmdlet:</span></span>
    - <span data-ttu-id="184db-601">'-Type' 매개 변수가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-601">Added parameter '-Type'</span></span>
    - <span data-ttu-id="184db-602">'-CoverageLevel' 매개 변수가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-602">Added parameter '-CoverageLevel'</span></span>
    - <span data-ttu-id="184db-603">'-Scope' 매개 변수가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-603">Added parameter '-Scope'</span></span>
* <span data-ttu-id="184db-604">'New-AzNetworkWatcherConnectionMonitorProtocolConfigurationObject' cmdlet이 새 매개 변수 '-DestinationPortBehavior'로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-604">Updated 'New-AzNetworkWatcherConnectionMonitorProtocolConfigurationObject' cmdlet with new parameter '-DestinationPortBehavior'</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="184db-605">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="184db-605">Az.RecoveryServices</span></span>
* <span data-ttu-id="184db-606">기여자 권한을 위해 워크로드 복원을 수정하는 중입니다.</span><span class="sxs-lookup"><span data-stu-id="184db-606">Fixing Workload Restore for contributor permissions.</span></span>
* <span data-ttu-id="184db-607">Restore-AzRecoveryServicesBackupItem cmdlet에 대한 새 매개 변수 집합 및 유효성 검사가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-607">Added new parameter sets and validations for Restore-AzRecoveryServicesBackupItem cmdlet.</span></span>

#### <a name="azresources"></a><span data-ttu-id="184db-608">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="184db-608">Az.Resources</span></span>
* <span data-ttu-id="184db-609">구문 분석 버그가 해결되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-609">Fixed parsing bug</span></span>
* <span data-ttu-id="184db-610">결과에서 미리 보기 메시지를 제거하도록 ARM 템플릿 What-If cmdlet이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-610">Updated ARM template What-If cmdlets to remove preview message from results</span></span>
* <span data-ttu-id="184db-611">'-WhatIf'가 상위 범위에서 설정된 경우 템플릿 배포 cmdlet의 작동이 중단되는 문제가 해결되었습니다. [#13038]</span><span class="sxs-lookup"><span data-stu-id="184db-611">Fixed an issue where template deployment cmdlets crash if '-WhatIf' is set at a higher scope [#13038]</span></span>
* <span data-ttu-id="184db-612">템플릿 배포 cmdlet이 템플릿 매개 변수에서 대/소문자를 구분하지 않는 문제가 해결되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-612">Fixed an issue where template deployment cmdlets does not preserve case for template parameters</span></span>
* <span data-ttu-id="184db-613">'Export-AzResourceGroup' cmdlet에 사용되는 기본 API 버전이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-613">Added a default API version to be used in 'Export-AzResourceGroup' cmdlet</span></span>
* <span data-ttu-id="184db-614">템플릿 사양에 대한 cmdlet이 추가되었습니다('Get-AzTemplateSpec', 'Set-AzTemplateSpec', 'New-AzTemplateSpec', 'Remove-AzTemplateSpec', 'Export-AzTemplateSpec').</span><span class="sxs-lookup"><span data-stu-id="184db-614">Added cmdlets for Template Specs ('Get-AzTemplateSpec', 'Set-AzTemplateSpec', 'New-AzTemplateSpec', 'Remove-AzTemplateSpec', 'Export-AzTemplateSpec')</span></span>
* <span data-ttu-id="184db-615">새 -TemplateSpecId 매개 변수를 통해 기존 배포 cmdlet을 사용하여 템플릿 사양을 배포하도록 지원하는 기능이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-615">Added support for deploying Template Specs using existing deployment cmdlets (via the new -TemplateSpecId parameter)</span></span> 
* <span data-ttu-id="184db-616">SDK를 사용하도록 'Get-AzResourceGroupDeploymentOperation'이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-616">Updated 'Get-AzResourceGroupDeploymentOperation' to use the SDK.</span></span>
* <span data-ttu-id="184db-617">'\*-AzDeployment' cmdlet에서 '-ApiVersion' 매개 변수가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-617">Removed '-ApiVersion' parameter from '\*-AzDeployment' cmdlets.</span></span>

#### <a name="azsql"></a><span data-ttu-id="184db-618">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="184db-618">Az.Sql</span></span>
* <span data-ttu-id="184db-619">networkIsolation이 지정되지 않은 경우 New-AzSqlDatabaseExport가 실패하는 문제가 해결되었습니다. [#13097]</span><span class="sxs-lookup"><span data-stu-id="184db-619">Fixed issue where New-AzSqlDatabaseExport fails if networkIsolation not specified [#13097]</span></span>
* <span data-ttu-id="184db-620">New-AzSqlDatabaseExport 및 New-AzSqlDatabaseImport가 결과 개체에 OperationStatusLink를 반환하지 않는 문제가 해결되었습니다. [#13097]</span><span class="sxs-lookup"><span data-stu-id="184db-620">Fixed issue where New-AzSqlDatabaseExport and New-AzSqlDatabaseImport were not returning OperationStatusLink in the result object [#13097]</span></span>
* <span data-ttu-id="184db-621">백업 스토리지 중복성 경고에서 Azure 쌍을 이루는 지역 URL이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-621">Update Azure Paired Regions URL in Backup Storage Redundancy Warnings</span></span> 

#### <a name="azstorage"></a><span data-ttu-id="184db-622">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="184db-622">Az.Storage</span></span>
* <span data-ttu-id="184db-623">더 이상 사용되지 않는 RestorePolicy.LastEnabledTime 속성이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-623">Removed obsolete property RestorePolicy.LastEnabledTime</span></span>
    - <span data-ttu-id="184db-624">'Enable-AzStorageBlobRestorePolicy'</span><span class="sxs-lookup"><span data-stu-id="184db-624">'Enable-AzStorageBlobRestorePolicy'</span></span>
    - <span data-ttu-id="184db-625">'Disable-AzStorageBlobRestorePolicy'</span><span class="sxs-lookup"><span data-stu-id="184db-625">'Disable-AzStorageBlobRestorePolicy'</span></span>
    - <span data-ttu-id="184db-626">'Get-AzStorageBlobServiceProperty'</span><span class="sxs-lookup"><span data-stu-id="184db-626">'Get-AzStorageBlobServiceProperty'</span></span>
    - <span data-ttu-id="184db-627">'Update-AzStorageBlobServiceProperty'</span><span class="sxs-lookup"><span data-stu-id="184db-627">'Update-AzStorageBlobServiceProperty'</span></span>
* <span data-ttu-id="184db-628">DaysAfterModificationGreaterThan의 Type이 int에서 int?로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-628">Change Type of DaysAfterModificationGreaterThan from int to int?</span></span>
    - <span data-ttu-id="184db-629">'Set-AzStorageAccountManagementPolicy'</span><span class="sxs-lookup"><span data-stu-id="184db-629">'Set-AzStorageAccountManagementPolicy'</span></span>
    - <span data-ttu-id="184db-630">'Get-AzStorageAccountManagementPolicy'</span><span class="sxs-lookup"><span data-stu-id="184db-630">'Get-AzStorageAccountManagementPolicy'</span></span>
    - <span data-ttu-id="184db-631">'Add-AzStorageAccountManagementPolicyAction'</span><span class="sxs-lookup"><span data-stu-id="184db-631">'Add-AzStorageAccountManagementPolicyAction'</span></span>
    - <span data-ttu-id="184db-632">'New-AzStorageAccountManagementPolicyRule'</span><span class="sxs-lookup"><span data-stu-id="184db-632">'New-AzStorageAccountManagementPolicyRule'</span></span>
* <span data-ttu-id="184db-633">액세스 계층을 사용한 파일 공유 생성/업데이트가 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="184db-633">Supported create/update file share with access tier</span></span>
    - <span data-ttu-id="184db-634">'New-AzRmStorageShare'</span><span class="sxs-lookup"><span data-stu-id="184db-634">'New-AzRmStorageShare'</span></span>
    - <span data-ttu-id="184db-635">'Update-AzRmStorageShare'</span><span class="sxs-lookup"><span data-stu-id="184db-635">'Update-AzRmStorageShare'</span></span>
* <span data-ttu-id="184db-636">Datalake Gen2 항목에서 Acl의 재귀적 설정/업데이트/제거가 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="184db-636">Supported set/update/remove Acl recursively on Datalake Gen2 item</span></span> 
    -  <span data-ttu-id="184db-637">'Set-AzDataLakeGen2AclRecursive'</span><span class="sxs-lookup"><span data-stu-id="184db-637">'Set-AzDataLakeGen2AclRecursive'</span></span> 
    -  <span data-ttu-id="184db-638">'Update-AzDataLakeGen2AclRecursive'</span><span class="sxs-lookup"><span data-stu-id="184db-638">'Update-AzDataLakeGen2AclRecursive'</span></span> 
    -  <span data-ttu-id="184db-639">'Remove-AzDataLakeGen2AclRecursive'</span><span class="sxs-lookup"><span data-stu-id="184db-639">'Remove-AzDataLakeGen2AclRecursive'</span></span>
* <span data-ttu-id="184db-640">새 권한 x,t를 사용하여 컨테이너 액세스 정책 지원</span><span class="sxs-lookup"><span data-stu-id="184db-640">Supported Container access policy with new permission x,t</span></span>
    -  <span data-ttu-id="184db-641">'New-AzStorageContainerStoredAccessPolicy'</span><span class="sxs-lookup"><span data-stu-id="184db-641">'New-AzStorageContainerStoredAccessPolicy'</span></span>
    -  <span data-ttu-id="184db-642">'Set-AzStorageContainerStoredAccessPolicy'</span><span class="sxs-lookup"><span data-stu-id="184db-642">'Set-AzStorageContainerStoredAccessPolicy'</span></span>
* <span data-ttu-id="184db-643">자식 속성 권한 유형을 열거형에서 문자열로 변경하여 컨테이너 액세스 정책 가져오기/설정 cmdlet의 출력을 변경했습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-643">Changed the output of get/set Container access policy cmdlet, by change the child property Permission type from enum to String</span></span>
    -  <span data-ttu-id="184db-644">'Get-AzStorageContainerStoredAccessPolicy'</span><span class="sxs-lookup"><span data-stu-id="184db-644">'Get-AzStorageContainerStoredAccessPolicy'</span></span>
    -  <span data-ttu-id="184db-645">'Set-AzStorageContainerStoredAccessPolicy'</span><span class="sxs-lookup"><span data-stu-id="184db-645">'Set-AzStorageContainerStoredAccessPolicy'</span></span>
* <span data-ttu-id="184db-646">json을 사용한 관리 정책 설정의 샘플 스크립트 문제가 해결되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-646">Fixed a sample script issue of set management policy with json</span></span>
    -  <span data-ttu-id="184db-647">'Set-AzStorageAccountManagementPolicy'</span><span class="sxs-lookup"><span data-stu-id="184db-647">'Set-AzStorageAccountManagementPolicy'</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="184db-648">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="184db-648">Az.Websites</span></span>
* <span data-ttu-id="184db-649">Premium V3 가격 책정 계층에 대한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-649">Added support for Premium V3 pricing tier</span></span>
* <span data-ttu-id="184db-650">WebSites SDK가 3.1.0으로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-650">Updated the WebSites SDK to 3.1.0</span></span>

### <a name="thanks-to-our-community-contributors"></a><span data-ttu-id="184db-651">커뮤니티 기여자에게 감사드립니다.</span><span class="sxs-lookup"><span data-stu-id="184db-651">Thanks to our community contributors</span></span>
* <span data-ttu-id="184db-652">@atul-ram, Get-AzDelegation.md 업데이트(#13176)</span><span class="sxs-lookup"><span data-stu-id="184db-652">@atul-ram, Update Get-AzDelegation.md (#13176)</span></span>
* <span data-ttu-id="184db-653">@dineshreddy007, WAC 토큰을 사용하여 Stack HCI를 등록하는 경우 올바르게 할당된 앱 역할을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="184db-653">@dineshreddy007, Get the App Roles assigned correctly in case of Stack HCI registration using WAC token.</span></span> <span data-ttu-id="184db-654">(#13249)</span><span class="sxs-lookup"><span data-stu-id="184db-654">(#13249)</span></span>
* <span data-ttu-id="184db-655">@kongou-ae, New-AzOffice365PolicyProperty.md 업데이트(#13217)</span><span class="sxs-lookup"><span data-stu-id="184db-655">@kongou-ae, Update New-AzOffice365PolicyProperty.md (#13217)</span></span>
* <span data-ttu-id="184db-656">Lohith Chowdary Chilukuri(@Lochiluk), Set-AzApplicationGateway.md 업데이트(#13150)</span><span class="sxs-lookup"><span data-stu-id="184db-656">Lohith Chowdary Chilukuri (@Lochiluk), Update Set-AzApplicationGateway.md (#13150)</span></span>
* <span data-ttu-id="184db-657">Matthew Burleigh(@mburleigh)</span><span class="sxs-lookup"><span data-stu-id="184db-657">Matthew Burleigh (@mburleigh)</span></span>
  * <span data-ttu-id="184db-658">문서에서 참조된 PowerShell cmdlet에 대한 링크 추가(#13203)</span><span class="sxs-lookup"><span data-stu-id="184db-658">Add links to PowerShell cmdlets referenced in the document (#13203)</span></span>
  * <span data-ttu-id="184db-659">문서에서 참조된 PowerShell cmdlet에 대한 링크 추가(#13190)</span><span class="sxs-lookup"><span data-stu-id="184db-659">Add links to PowerShell cmdlets referenced in the document (#13190)</span></span>
  * <span data-ttu-id="184db-660">문서에서 참조된 PowerShell cmdlet에 대한 링크 추가(#13189)</span><span class="sxs-lookup"><span data-stu-id="184db-660">Add links to PowerShell cmdlets referenced in the document (#13189)</span></span>
  * <span data-ttu-id="184db-661">참조된 cmdlet에 대한 링크 추가(#13137)</span><span class="sxs-lookup"><span data-stu-id="184db-661">add links to referenced cmdlets (#13137)</span></span>
  * <span data-ttu-id="184db-662">문서에서 참조된 PowerShell cmdlet에 대한 링크 추가(#13204)</span><span class="sxs-lookup"><span data-stu-id="184db-662">Add links to PowerShell cmdlets referenced in the document (#13204)</span></span>
  * <span data-ttu-id="184db-663">문서에서 참조된 PowerShell cmdlet에 대한 링크 추가(#13205)</span><span class="sxs-lookup"><span data-stu-id="184db-663">Add links to PowerShell cmdlets referenced in the document (#13205)</span></span>

## <a name="480---october-2020"></a><span data-ttu-id="184db-664">4.8.0 - 2020년 10월</span><span class="sxs-lookup"><span data-stu-id="184db-664">4.8.0 - October 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="184db-665">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="184db-665">Az.Accounts</span></span>
* <span data-ttu-id="184db-666">공용 라이브러리의 DateTime 구문 분석 문제 해결[#13045]</span><span class="sxs-lookup"><span data-stu-id="184db-666">Fixed DateTime parse issue in common libraries [#13045]</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="184db-667">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="184db-667">Az.CognitiveServices</span></span>
* <span data-ttu-id="184db-668">'New-AzCognitiveServicesAccountApiProperty' cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-668">Added 'New-AzCognitiveServicesAccountApiProperty' cmdlet.</span></span>
* <span data-ttu-id="184db-669">'New-AzCognitiveServicesAccount' 및 'Set-AzCognitiveServicesAccount'에 대해 'ApiProperty' 매개 변수 지원됨</span><span class="sxs-lookup"><span data-stu-id="184db-669">Supported 'ApiProperty' parameter for 'New-AzCognitiveServicesAccount' and 'Set-AzCognitiveServicesAccount'</span></span>

#### <a name="azcompute"></a><span data-ttu-id="184db-670">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="184db-670">Az.Compute</span></span>
* <span data-ttu-id="184db-671">FailoverTypes를 채워서 'Update-ASRRecoveryPlan'의 문제 해결</span><span class="sxs-lookup"><span data-stu-id="184db-671">Fixed issue in 'Update-ASRRecoveryPlan' by populating FailoverTypes</span></span>
* <span data-ttu-id="184db-672">'Get-AzVmImage' cmdlet에 '-Top' 및 '-OrderBy' 선택적 매개 변수를 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-672">Added the '-Top' and '-OrderBy' optional parameters to the 'Get-AzVmImage' cmdlet.</span></span> 

#### <a name="azdatabricks"></a><span data-ttu-id="184db-673">Az.Databricks</span><span class="sxs-lookup"><span data-stu-id="184db-673">Az.Databricks</span></span>
* <span data-ttu-id="184db-674">'Az.Databricks' 모듈의 일반 공급</span><span class="sxs-lookup"><span data-stu-id="184db-674">General availability of 'Az.Databricks' module</span></span>
* <span data-ttu-id="184db-675">가상 네트워크 피어링에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="184db-675">Added support for virtual network peering</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="184db-676">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="184db-676">Az.DataFactory</span></span>
* <span data-ttu-id="184db-677">출력 메시지의 오타 수정</span><span class="sxs-lookup"><span data-stu-id="184db-677">Fixed typo in output messages</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="184db-678">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="184db-678">Az.EventHub</span></span>
* <span data-ttu-id="184db-679">선택적 스위치 매개 변수 'TrustedServiceAccessEnabled'를 'Set-AzEventHubNetworkRuleSet' cmdlet에 추가</span><span class="sxs-lookup"><span data-stu-id="184db-679">Added optional switch parameter 'TrustedServiceAccessEnabled' to 'Set-AzEventHubNetworkRuleSet' cmdlet</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="184db-680">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="184db-680">Az.HDInsight</span></span>
* <span data-ttu-id="184db-681">'PublicNetworkAccessType' 및 'OutboundPublicNetworkAccessType' 매개 변수 사용 중단 계획에 대한 경고 메시지 추가</span><span class="sxs-lookup"><span data-stu-id="184db-681">Added warning message for planning to deprecate the parameters 'PublicNetworkAccessType' and 'OutboundPublicNetworkAccessType'</span></span>
* <span data-ttu-id="184db-682">'DefaultStorageAccountName' 매개 변수를 'StorageAccountResourceId'로 바꾸려는 계획에 대한 경고 메시지 추가</span><span class="sxs-lookup"><span data-stu-id="184db-682">Added warning message for planning to replace the parameter 'DefaultStorageAccountName' with 'StorageAccountResourceId'</span></span>
* <span data-ttu-id="184db-683">'DefaultStorageAccountKey' 매개 변수를 'StorageAccountKey'로 바꾸려는 계획에 대한 경고 메시지 추가</span><span class="sxs-lookup"><span data-stu-id="184db-683">Added warning message for planning to replace the parameter 'DefaultStorageAccountKey' with 'StorageAccountKey'</span></span>
* <span data-ttu-id="184db-684">'DefaultStorageAccountType' 매개 변수를 'StorageAccountType'으로 바꾸려는 계획에 대한 경고 메시지 추가</span><span class="sxs-lookup"><span data-stu-id="184db-684">Added warning message for planning to replace the parameter 'DefaultStorageAccountType' with 'StorageAccountType'</span></span>
* <span data-ttu-id="184db-685">'DefaultStorageContainer' 매개 변수를 'StorageContainer'로 바꾸려는 계획에 대한 경고 메시지 추가</span><span class="sxs-lookup"><span data-stu-id="184db-685">Added warning message for planning to replace the parameter 'DefaultStorageContainer' with 'StorageContainer'</span></span>
* <span data-ttu-id="184db-686">'DefaultStorageRootPath' 매개 변수를 'StorageRootPath'로 바꾸려는 계획에 대한 경고 메시지 추가</span><span class="sxs-lookup"><span data-stu-id="184db-686">Added warning message for planning to replace the parameter 'DefaultStorageRootPath' with 'StorageRootPath'</span></span>

#### <a name="aziothub"></a><span data-ttu-id="184db-687">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="184db-687">Az.IotHub</span></span>
* <span data-ttu-id="184db-688">업데이트된 디바이스 SDK.</span><span class="sxs-lookup"><span data-stu-id="184db-688">Updated devices sdk.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="184db-689">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="184db-689">Az.KeyVault</span></span>
* <span data-ttu-id="184db-690">SecretValueText 속성 제거 세부 날짜 제공</span><span class="sxs-lookup"><span data-stu-id="184db-690">Provided the detailed date of removing property SecretValueText</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="184db-691">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="184db-691">Az.ManagedServices</span></span>
* <span data-ttu-id="184db-692">관리되는 서비스 할당 및 정의의 cmdlet에 대한 호환성이 손상되는 변경 경고가 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="184db-692">Updated breaking change warnings on cmdlets of managed services assignment and definition</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="184db-693">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="184db-693">Az.Monitor</span></span>
* <span data-ttu-id="184db-694">경고 메시지를 숨길 수 없는 버그를 수정했습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-694">Fixed the bug that warning message cannot be suppressed.</span></span> <span data-ttu-id="184db-695">[#12889]</span><span class="sxs-lookup"><span data-stu-id="184db-695">[#12889]</span></span>
* <span data-ttu-id="184db-696">경고 규칙 기준에서 'SkipMetricValidation' 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="184db-696">Supported 'SkipMetricValidation' parameter in alert rule criteria.</span></span> <span data-ttu-id="184db-697">메트릭 유효성 검사를 건너뛰도록 하여 아직 생성되지 않은 사용자 지정 메트릭에 대한 경고 규칙을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-697">Allows creating an alert rule on a custom metric that isn't yet emitted, by causing the metric validation to be skipped.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="184db-698">Az.Network</span><span class="sxs-lookup"><span data-stu-id="184db-698">Az.Network</span></span>
* <span data-ttu-id="184db-699">VPNSite 리소스에 Office365 정책 추가</span><span class="sxs-lookup"><span data-stu-id="184db-699">Added Office365 Policy to VPNSite Resource</span></span>
    - <span data-ttu-id="184db-700">'New-AzO365PolicyProperty'</span><span class="sxs-lookup"><span data-stu-id="184db-700">'New-AzO365PolicyProperty'</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="184db-701">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="184db-701">Az.RecoveryServices</span></span>
* <span data-ttu-id="184db-702">워크로드 백업에 대한 컨테이너 이름 유효성 검사가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-702">Added container name validation for workload backup.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="184db-703">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="184db-703">Az.RedisCache</span></span>
* <span data-ttu-id="184db-704">Microsoft.Cache RP 등록과 관련된 권한 문제로 인해 'New-AzRedisCache' 및 'Set-AzRedisCache' cmdlet이 실패하지 않도록 함</span><span class="sxs-lookup"><span data-stu-id="184db-704">Made 'New-AzRedisCache' and 'Set-AzRedisCache' cmdlets not fail because of permission issue related to registering Microsoft.Cache RP</span></span>

#### <a name="azsql"></a><span data-ttu-id="184db-705">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="184db-705">Az.Sql</span></span>
* <span data-ttu-id="184db-706">BackupStorageRedundancy가 다음에 추가됨</span><span class="sxs-lookup"><span data-stu-id="184db-706">Added BackupStorageRedundancy to the following:</span></span> 
    - <span data-ttu-id="184db-707">'Restore-AzureRmSqlDatabase'</span><span class="sxs-lookup"><span data-stu-id="184db-707">'Restore-AzureRmSqlDatabase'</span></span>
    - <span data-ttu-id="184db-708">'New-AzSqlDatabaseCopy'</span><span class="sxs-lookup"><span data-stu-id="184db-708">'New-AzSqlDatabaseCopy'</span></span>
    - <span data-ttu-id="184db-709">'New-AzSqlDatabaseSecondary'</span><span class="sxs-lookup"><span data-stu-id="184db-709">'New-AzSqlDatabaseSecondary'</span></span>
* <span data-ttu-id="184db-710">모든 SQL DB 참조에 대한 BackupStorageRedundancy 매개 변수의 대소문자 구분 제거</span><span class="sxs-lookup"><span data-stu-id="184db-710">Removed case sensitivity for BackupStorageRedundancy parameter for all SQL DB references</span></span> 
* <span data-ttu-id="184db-711">BackupStorageRedundancy 경고 메시지 이름 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="184db-711">Updated BackupStorageRedundancy warning message names</span></span>

#### <a name="azstorage"></a><span data-ttu-id="184db-712">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="184db-712">Az.Storage</span></span>
* <span data-ttu-id="184db-713">스토리지 계정의 파일 서비스에서 사용/사용하지 않음/공유 일시 삭제 속성 지원</span><span class="sxs-lookup"><span data-stu-id="184db-713">Supported enable/disable/get share soft delete properties on file Service of a Storage account</span></span>
    - <span data-ttu-id="184db-714">'Update-AzStorageFileServiceProperty'</span><span class="sxs-lookup"><span data-stu-id="184db-714">'Update-AzStorageFileServiceProperty'</span></span>
    - <span data-ttu-id="184db-715">'Get-AzStorageFileServiceProperty'</span><span class="sxs-lookup"><span data-stu-id="184db-715">'Get-AzStorageFileServiceProperty'</span></span>
* <span data-ttu-id="184db-716">지원되는 목록 파일 공유에는 스토리지 계정의 삭제된 공유와 단일 파일 공유 사용량 가져오기가 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="184db-716">Supported list file shares include the deleted ones of a Storage account, and Get single file share usage</span></span>
    - <span data-ttu-id="184db-717">'Get-AzRmStorageShare'</span><span class="sxs-lookup"><span data-stu-id="184db-717">'Get-AzRmStorageShare'</span></span>
* <span data-ttu-id="184db-718">삭제된 파일 공유 복원 지원</span><span class="sxs-lookup"><span data-stu-id="184db-718">Supported restore a deleted file share</span></span>
    - <span data-ttu-id="184db-719">'Restore-AzRmStorageShare'</span><span class="sxs-lookup"><span data-stu-id="184db-719">'Restore-AzRmStorageShare'</span></span>
* <span data-ttu-id="184db-720">Blob 서비스 속성을 수정하기 위한 cmdlet을 변경하여, 서버에서 원래 속성을 가져오지 않으며 수정된 속성만 서버로 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="184db-720">Changed the cmdlets for modify blob service properties, won't get the original properties from server, but only set the modified properties to server.</span></span>
    - <span data-ttu-id="184db-721">'Enable-AzStorageBlobDeleteRetentionPolicy'</span><span class="sxs-lookup"><span data-stu-id="184db-721">'Enable-AzStorageBlobDeleteRetentionPolicy'</span></span>
    - <span data-ttu-id="184db-722">'Disable-AzStorageBlobDeleteRetentionPolicy'</span><span class="sxs-lookup"><span data-stu-id="184db-722">'Disable-AzStorageBlobDeleteRetentionPolicy'</span></span>  
    - <span data-ttu-id="184db-723">'Enable-AzStorageBlobRestorePolicy'</span><span class="sxs-lookup"><span data-stu-id="184db-723">'Enable-AzStorageBlobRestorePolicy'</span></span>
    - <span data-ttu-id="184db-724">'Disable-AzStorageBlobRestorePolicy'</span><span class="sxs-lookup"><span data-stu-id="184db-724">'Disable-AzStorageBlobRestorePolicy'</span></span>
    - <span data-ttu-id="184db-725">'Update-AzStorageBlobServiceProperty'</span><span class="sxs-lookup"><span data-stu-id="184db-725">'Update-AzStorageBlobServiceProperty'</span></span>
* <span data-ttu-id="184db-726">New-AzStorageAccount 매개 변수 -Kind 기본값에 대한 도움말 문제 해결[#12189]</span><span class="sxs-lookup"><span data-stu-id="184db-726">Fixed help issue for New-AzStorageAccount parameter -Kind default value [#12189]</span></span>
* <span data-ttu-id="184db-727">Blob 업로드에서 올바른 ContentType을 설정하는 방법을 보여주는 예제를 추가하여 문제 해결[#12989]</span><span class="sxs-lookup"><span data-stu-id="184db-727">Fixed issue by add example to show how to set correct ContentType in blob upload [#12989]</span></span>

## <a name="470---september-2020"></a><span data-ttu-id="184db-728">4.7.0 - 2020년 9월</span><span class="sxs-lookup"><span data-stu-id="184db-728">4.7.0 - September 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="184db-729">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="184db-729">Az.Accounts</span></span>
* <span data-ttu-id="184db-730">예정된 호환성이 손상되는 변경 메시지의 형식이 지정됨</span><span class="sxs-lookup"><span data-stu-id="184db-730">Formatted the upcoming breaking change messages</span></span>
* <span data-ttu-id="184db-731">Azure.Core가 1.4.1로 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="184db-731">Updated Azure.Core to 1.4.1</span></span>

#### <a name="azaks"></a><span data-ttu-id="184db-732">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="184db-732">Az.Aks</span></span>
* <span data-ttu-id="184db-733">'New-AzAksCluster', 'Set-AzAksCluster' 및 'New-AzAksNodePool'에 대한 클라이언트 쪽 매개 변수 유효성 검사 논리가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-733">Added client side parameter validation logic for 'New-AzAksCluster', 'Set-AzAksCluster' and 'New-AzAksNodePool'.</span></span> <span data-ttu-id="184db-734">[#12372]</span><span class="sxs-lookup"><span data-stu-id="184db-734">[#12372]</span></span>
* <span data-ttu-id="184db-735">'New-AzAksCluster'에서 추가 항목에 대한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-735">Added support for add-ons in 'New-AzAksCluster'.</span></span> <span data-ttu-id="184db-736">[#11239]</span><span class="sxs-lookup"><span data-stu-id="184db-736">[#11239]</span></span>
* <span data-ttu-id="184db-737">추가 항목에 대한 'Enable-AzAksAddOn' 및 'Disable-AzAksAddOn' cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-737">Added cmdlets 'Enable-AzAksAddOn' and 'Disable-AzAksAddOn' for add-ons.</span></span> <span data-ttu-id="184db-738">[#11239]</span><span class="sxs-lookup"><span data-stu-id="184db-738">[#11239]</span></span>
* <span data-ttu-id="184db-739">'New-AzAksCluster'에 대한 매개 변수 'GenerateSshKey'가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-739">Added parameter 'GenerateSshKey' for 'New-AzAksCluster'.</span></span> <span data-ttu-id="184db-740">[#12371]</span><span class="sxs-lookup"><span data-stu-id="184db-740">[#12371]</span></span>
* <span data-ttu-id="184db-741">API 버전이 2020-06-01로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-741">Updated api version to 2020-06-01.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="184db-742">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="184db-742">Az.CognitiveServices</span></span>
* <span data-ttu-id="184db-743">특정 API에 대한 추가 법률 용어를 표시했습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-743">Showed additional legal terms for certain APIs.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="184db-744">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="184db-744">Az.Compute</span></span>
* <span data-ttu-id="184db-745">'New-AzVmDiskEncryptionSetConfig'에 '-EncryptionType' 선택적 매개 변수가 추가됨</span><span class="sxs-lookup"><span data-stu-id="184db-745">Added the '-EncryptionType' optional parameter to 'New-AzVmDiskEncryptionSetConfig'</span></span>
* <span data-ttu-id="184db-746">새 리소스 종류에 대한 새 cmdlet: DiskAccess 'Get-AzDiskAccess', 'New-AzDiskAccess', 'Get-AzDiskAccess'</span><span class="sxs-lookup"><span data-stu-id="184db-746">New cmdlets for new resource type: DiskAccess 'Get-AzDiskAccess', 'New-AzDiskAccess', 'Get-AzDiskAccess'</span></span>
* <span data-ttu-id="184db-747">'New-AzSnapshotConfig'에 선택적 매개 변수 '-DiskAccessId' 및 '-NetworkAccessPolicy'가 추가됨</span><span class="sxs-lookup"><span data-stu-id="184db-747">Added optional parameters '-DiskAccessId' and '-NetworkAccessPolicy' to 'New-AzSnapshotConfig'</span></span>
* <span data-ttu-id="184db-748">'New-AzDiskConfig'에 선택적 매개 변수 '-DiskAccessId' 및 '-NetworkAccessPolicy'가 추가됨</span><span class="sxs-lookup"><span data-stu-id="184db-748">Added optional parameters '-DiskAccessId' and '-NetworkAccessPolicy' to 'New-AzDiskConfig'</span></span>
* <span data-ttu-id="184db-749">VirtualMachine 인스턴스 보기에 'PatchStatus' 속성이 추가됨</span><span class="sxs-lookup"><span data-stu-id="184db-749">Added 'PatchStatus' property to VirtualMachine Instance View</span></span>
* <span data-ttu-id="184db-750">가상 머신의 인스턴스 보기에 'VMHealth' 속성이 추가됨. 이 속성은 'Get-AzVm'이 '-Status'로 호출될 때 반환되는 개체</span><span class="sxs-lookup"><span data-stu-id="184db-750">Added 'VMHealth' property to the virtual machine's instance view, which is the returned object when 'Get-AzVm' is invoked with '-Status'</span></span>
* <span data-ttu-id="184db-751">'Get-AzVM' 및 'Get-AzVmss' 인스턴스 보기에 'AssignedHost' 필드가 추가됨</span><span class="sxs-lookup"><span data-stu-id="184db-751">Added 'AssignedHost' field to 'Get-AzVM' and 'Get-AzVmss' instance views.</span></span> <span data-ttu-id="184db-752">필드는 가상 머신 인스턴스의 리소스 ID를 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="184db-752">The field shows the resource id of the virtual machine instance</span></span>
* <span data-ttu-id="184db-753">선택적 매개 변수 '-SupportAutomaticPlacement'가 'New-AzHostGroup'에 추가됨</span><span class="sxs-lookup"><span data-stu-id="184db-753">Added optional parameter '-SupportAutomaticPlacement' to 'New-AzHostGroup'</span></span> 
* <span data-ttu-id="184db-754">'-HostGroupId' 매개 변수가 'New-AzVm' 및 'New-AzVmss'에 추가됨</span><span class="sxs-lookup"><span data-stu-id="184db-754">Added the '-HostGroupId' parameter to 'New-AzVm' and 'New-AzVmss'</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="184db-755">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="184db-755">Az.DataFactory</span></span>
* <span data-ttu-id="184db-756">ADF .Net SDK 버전이 4.11.0으로 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="184db-756">Updated ADF .Net SDK version to 4.11.0</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="184db-757">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="184db-757">Az.EventHub</span></span>
* <span data-ttu-id="184db-758">새 클러스터 cmdlet 추가됨 - 'New-AzEventHubCluster', 'Set-AzEventHubCluster', 'Get-AzEventHubCluster', 'Remove-AzEventHubCluster', 'Get-AzEventHubClustersAvailableRegions'</span><span class="sxs-lookup"><span data-stu-id="184db-758">Added new Cluster cmdlets - 'New-AzEventHubCluster', 'Set-AzEventHubCluster', 'Get-AzEventHubCluster', 'Remove-AzEventHubCluster', 'Get-AzEventHubClustersAvailableRegions'.</span></span>
* <span data-ttu-id="184db-759">#10722 문제 해결됨: AuthorizationRule 권한에 'Listen'만 할당하는 문제가 해결되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-759">Fixed for issue #10722 : Fix for assigning only 'Listen' to AuthorizationRule rights.</span></span>

#### <a name="azfunctions"></a><span data-ttu-id="184db-760">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="184db-760">Az.Functions</span></span>
* <span data-ttu-id="184db-761">v2 Functions를 지원하지 않는 지역에서 생성하는 기능이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-761">Removed the ability to create v2 Functions in regions that do not support it.</span></span>
* <span data-ttu-id="184db-762">PowerShell 6.2가 사용되지 않음</span><span class="sxs-lookup"><span data-stu-id="184db-762">Deprecated PowerShell 6.2.</span></span> <span data-ttu-id="184db-763">사용자가 PowerShell 6.2 함수 앱을 만들 때 PowerShell 7.0 함수 앱을 만들도록 권장하는 경고가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-763">Added a warning for when a user creates a PowerShell 6.2 function app that advises them to create a PowerShell 7.0 function app instead.</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="184db-764">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="184db-764">Az.HDInsight</span></span>
* <span data-ttu-id="184db-765">자동 크기 조정 구성을 사용하여 클러스터 만들기 지원</span><span class="sxs-lookup"><span data-stu-id="184db-765">Supported creating cluster with Autoscale configuration</span></span>
    - <span data-ttu-id="184db-766">cmdlet 'New-AzHDInsightCluster'에 새 매개 변수 'AutoscaleConfiguration' 추가</span><span class="sxs-lookup"><span data-stu-id="184db-766">Add new parameter 'AutoscaleConfiguration' to the cmdlet 'New-AzHDInsightCluster'</span></span>
* <span data-ttu-id="184db-767">운영 클러스터의 자동 크기 조정 구성 지원됨</span><span class="sxs-lookup"><span data-stu-id="184db-767">Supported operating cluster's Autoscale configuration</span></span>
    - <span data-ttu-id="184db-768">새 cmdlet 'Get-AzHDInsihgtClusterAutoscaleConfiguration' 추가</span><span class="sxs-lookup"><span data-stu-id="184db-768">Add new cmdlet 'Get-AzHDInsihgtClusterAutoscaleConfiguration'</span></span>
    - <span data-ttu-id="184db-769">새 cmdlet 'New-AzHDInsihgtClusterAutoscaleConfiguration' 추가</span><span class="sxs-lookup"><span data-stu-id="184db-769">Add new cmdlet 'New-AzHDInsihgtClusterAutoscaleConfiguration'</span></span>
    - <span data-ttu-id="184db-770">새 cmdlet 'Set-AzHDInsihgtClusterAutoscaleConfiguration' 추가</span><span class="sxs-lookup"><span data-stu-id="184db-770">Add new cmdlet 'Set-AzHDInsihgtClusterAutoscaleConfiguration'</span></span>
    - <span data-ttu-id="184db-771">새 cmdlet 'Remove-AzHDInsihgtClusterAutoscaleConfiguration' 추가</span><span class="sxs-lookup"><span data-stu-id="184db-771">Add new cmdlet 'Remove-AzHDInsihgtClusterAutoscaleConfiguration'</span></span>
    - <span data-ttu-id="184db-772">새 cmdlet 'New-AzHDInsihgtClusterAutoscaleScheduleCondition' 추가</span><span class="sxs-lookup"><span data-stu-id="184db-772">Add new cmdlet 'New-AzHDInsihgtClusterAutoscaleScheduleCondition'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="184db-773">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="184db-773">Az.KeyVault</span></span>
* <span data-ttu-id="184db-774">RBAC 권한 부여에 대한 지원 추가됨 [#10557]</span><span class="sxs-lookup"><span data-stu-id="184db-774">Added support for RBAC authorization [#10557]</span></span>
* <span data-ttu-id="184db-775">'Set-AzKeyVaultAccessPolicy'에서 향상된 오류 처리 [#4007]</span><span class="sxs-lookup"><span data-stu-id="184db-775">Enhanced error handling in 'Set-AzKeyVaultAccessPolicy' [#4007]</span></span>

#### <a name="azkusto"></a><span data-ttu-id="184db-776">Az.Kusto</span><span class="sxs-lookup"><span data-stu-id="184db-776">Az.Kusto</span></span>
* <span data-ttu-id="184db-777">'Az.Kusto' 모듈의 일반 공급</span><span class="sxs-lookup"><span data-stu-id="184db-777">General availability of 'Az.Kusto' module</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="184db-778">Az.Network</span><span class="sxs-lookup"><span data-stu-id="184db-778">Az.Network</span></span>
* <span data-ttu-id="184db-779">[호환성이 손상되는 변경] 리소스 가상 라우터 및 가상 허브에 맞게 아래 cmdlet이 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="184db-779">[Breaking Change] Updated below cmdlets to align resource virtual router and virtual hub</span></span>
    - <span data-ttu-id="184db-780">'New-AzVirtualRouter':</span><span class="sxs-lookup"><span data-stu-id="184db-780">'New-AzVirtualRouter':</span></span> 
        - <span data-ttu-id="184db-781">IP 구성 자식 리소스를 지원하는 -HostedSubnet 매개 변수가 추가됨</span><span class="sxs-lookup"><span data-stu-id="184db-781">Added -HostedSubnet parameter to support IP configuration child resource</span></span>
        - <span data-ttu-id="184db-782">-HostedGateway 및 -HostedGatewayId 삭제됨</span><span class="sxs-lookup"><span data-stu-id="184db-782">deleted -HostedGateway and -HostedGatewayId</span></span>
    - <span data-ttu-id="184db-783">'Get-AzVirtualRouter':</span><span class="sxs-lookup"><span data-stu-id="184db-783">'Get-AzVirtualRouter':</span></span>
        - <span data-ttu-id="184db-784">구독 수준 매개 변수 집합이 추가됨</span><span class="sxs-lookup"><span data-stu-id="184db-784">Added subscription level parameter set</span></span>
    - <span data-ttu-id="184db-785">'Remove-AzVirtualRouter'</span><span class="sxs-lookup"><span data-stu-id="184db-785">'Remove-AzVirtualRouter'</span></span>
    - <span data-ttu-id="184db-786">'Add-AzVirtualRouterPeer'</span><span class="sxs-lookup"><span data-stu-id="184db-786">'Add-AzVirtualRouterPeer'</span></span>
    - <span data-ttu-id="184db-787">'Get-AzVirtualRouterPeer'</span><span class="sxs-lookup"><span data-stu-id="184db-787">'Get-AzVirtualRouterPeer'</span></span>
    - <span data-ttu-id="184db-788">'Remove-AzVirtualRouterPeer'</span><span class="sxs-lookup"><span data-stu-id="184db-788">'Remove-AzVirtualRouterPeer'</span></span>
* <span data-ttu-id="184db-789">Azure Express 경로 포트에 대해 새 cmdlet이 추가됨</span><span class="sxs-lookup"><span data-stu-id="184db-789">Added new cmdlet for Azure Express Route Port</span></span>
    - <span data-ttu-id="184db-790">'New-AzExpressRoutePortLOA'</span><span class="sxs-lookup"><span data-stu-id="184db-790">'New-AzExpressRoutePortLOA'</span></span>
* <span data-ttu-id="184db-791">VirtualNetwork 피어링 리소스에 RemoteBgpCommunities 속성이 추가됨</span><span class="sxs-lookup"><span data-stu-id="184db-791">Added RemoteBgpCommunities property to the VirtualNetwork Peering Resource</span></span>
* <span data-ttu-id="184db-792">'New-AzLoadBalancerFrontendIpConfig', 'New-AzPublicIpAddress' 및 'New-AzPublicIpPrefix'에 대한 경고 메시지를 수정했습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-792">Modified the warning message for 'New-AzLoadBalancerFrontendIpConfig', 'New-AzPublicIpAddress' and 'New-AzPublicIpPrefix'.</span></span>
* <span data-ttu-id="184db-793">'Get-AzVpnGateway' 출력에 VpnGatewayIpConfigurations가 추가됨</span><span class="sxs-lookup"><span data-stu-id="184db-793">Added VpnGatewayIpConfigurations to 'Get-AzVpnGateway' output</span></span>
* <span data-ttu-id="184db-794">'Set-AzApplicationGatewaySslCertificate'의 버그 수정됨 [#9488]</span><span class="sxs-lookup"><span data-stu-id="184db-794">Fixed bug for 'Set-AzApplicationGatewaySslCertificate' [#9488]</span></span>
* <span data-ttu-id="184db-795">'AzureFirewall'에 'AllowActiveFTP' 매개 변수가 추가됨</span><span class="sxs-lookup"><span data-stu-id="184db-795">Added 'AllowActiveFTP' parameter to 'AzureFirewall'</span></span>
* <span data-ttu-id="184db-796">기능에 대한 새로운 명령이 업데이트됨: VirtualWan P2SVpnGateway에서 인터넷 보안 설정 사용/제거</span><span class="sxs-lookup"><span data-stu-id="184db-796">Updated below commands for feature: Enable internet security set/remove on VirtualWan P2SVpnGateway.</span></span>
- <span data-ttu-id="184db-797">'New-AzP2sVpnGateway' 업데이트됨: 고객이 P2SVpnGateway에서 인터넷 보안을 사용하도록 true를 설정할 수 있는 선택적 스위치 매개 변수 'EnableInternetSecurityFlag'가 추가되었으며, 이는 지점 및 사이트 간 클라이언트에 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="184db-797">Updated 'New-AzP2sVpnGateway': Added optional switch parameter 'EnableInternetSecurityFlag' for customers to set true to enable internet security on P2SVpnGateway, which will be applied for Point to site clients.</span></span>
- <span data-ttu-id="184db-798">'Update-AzP2sVpnGateway' 업데이트됨: 고객이 P2SVpnGateway에서 인터넷 보안을 활성화/비활성화하도록 true/false를 설정할 수 있는 선택적 스위치 매개 변수 'EnableInternetSecurityFlag' 또는 'DisableInternetSecurityFlag'가 추가되었으며, 이는 지점 및 사이트 간 클라이언트에 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="184db-798">Updated 'Update-AzP2sVpnGateway': Added optional switch parameters 'EnableInternetSecurityFlag' or 'DisableInternetSecurityFlag' for customers to set true/false to enable/disable internet security on P2SVpnGateway, which will be applied for Point to site clients.</span></span>
* <span data-ttu-id="184db-799">문제 해결을 위해 VirtualWan P2SVPNGateway를 재설정/재부팅할 수 있도록 새 cmdlet 'Reset-AzP2sVpnGateway'를 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-799">Added new cmdlet 'Reset-AzP2sVpnGateway' for customers to reset/reboot their VirtualWan P2SVpnGateway for troubleshooting.</span></span>
* <span data-ttu-id="184db-800">문제 해결을 위해 VirtualWan VpnGateway를 재설정/재부팅할 수 있도록 새 cmdlet 'Reset-AzVpnGateway'를 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-800">Added new cmdlet 'Reset-AzVpnGateway' for customers to reset/reboot their VirtualWan VpnGateway for troubleshooting.</span></span>
* <span data-ttu-id="184db-801">'Set-AzVirtualNetworkSubnetConfig' 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="184db-801">Updated 'Set-AzVirtualNetworkSubnetConfig'</span></span>
    - <span data-ttu-id="184db-802">매개 변수에 명시적으로 설정된 경우 서브넷의 NSG 및 라우팅 테이블 속성을 null로 설정 [# 1548][# 9718]</span><span class="sxs-lookup"><span data-stu-id="184db-802">Set NSG and Route Table properties of subnet to null if explicitly set in parameters [#1548][#9718]</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="184db-803">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="184db-803">Az.RecoveryServices</span></span>
* <span data-ttu-id="184db-804">워크로드 백업 항목에 대한 삭제 상태가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-804">Fixed the Delete State for workload Backup Items.</span></span>

#### <a name="azresources"></a><span data-ttu-id="184db-805">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="184db-805">Az.Resources</span></span>
* <span data-ttu-id="184db-806">Set-AzRoleAssignment에 대한 누락된 검사 추가됨</span><span class="sxs-lookup"><span data-stu-id="184db-806">Added missing check for Set-AzRoleAssignment</span></span>
* <span data-ttu-id="184db-807">'Get-AzResourceGroupDeploymentOperation'의 'SubscriptionId' 매개 변수에 호환성이 손상되는 변경 특성이 추가됨</span><span class="sxs-lookup"><span data-stu-id="184db-807">Added breaking change attribute to 'SubscriptionId' parameter of 'Get-AzResourceGroupDeploymentOperation'</span></span>
* <span data-ttu-id="184db-808">마지막으로 'Ignore' 리소스 변경을 표시하도록 ARM 템플릿 What-If cmdlet이 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="184db-808">Updated ARM template What-If cmdlets to show 'Ignore' resource changes last</span></span>
* <span data-ttu-id="184db-809">배포 cmdlet에 대한 보안 및 배열 매개 변수 직렬화 문제가 해결됨 [#12773]</span><span class="sxs-lookup"><span data-stu-id="184db-809">Fixed secure and array parameter serialization issues for deployment cmdlets [#12773]</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="184db-810">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="184db-810">Az.ServiceFabric</span></span>
* <span data-ttu-id="184db-811">관리형 클러스터 및 노드 유형에 대해 다음과 같은 새 cmdlet가 추가됨</span><span class="sxs-lookup"><span data-stu-id="184db-811">Added new cmdlets for managed clusters and node types:</span></span>
    - <span data-ttu-id="184db-812">'New-AzServiceFabricManagedCluster'</span><span class="sxs-lookup"><span data-stu-id="184db-812">'New-AzServiceFabricManagedCluster'</span></span>
    - <span data-ttu-id="184db-813">'Get-AzServiceFabricManagedCluster'</span><span class="sxs-lookup"><span data-stu-id="184db-813">'Get-AzServiceFabricManagedCluster'</span></span>
    - <span data-ttu-id="184db-814">'Set-AzServiceFabricManagedCluster'</span><span class="sxs-lookup"><span data-stu-id="184db-814">'Set-AzServiceFabricManagedCluster'</span></span>
    - <span data-ttu-id="184db-815">'Remove-AzServiceFabricManagedCluster'</span><span class="sxs-lookup"><span data-stu-id="184db-815">'Remove-AzServiceFabricManagedCluster'</span></span>
    - <span data-ttu-id="184db-816">'Add-AzServiceFabricManagedClusterClientCertificate'</span><span class="sxs-lookup"><span data-stu-id="184db-816">'Add-AzServiceFabricManagedClusterClientCertificate'</span></span>
    - <span data-ttu-id="184db-817">'Remove-AzServiceFabricManagedClusterClientCertificate'</span><span class="sxs-lookup"><span data-stu-id="184db-817">'Remove-AzServiceFabricManagedClusterClientCertificate'</span></span>
    - <span data-ttu-id="184db-818">'New-AzServiceFabricManagedNodeType'</span><span class="sxs-lookup"><span data-stu-id="184db-818">'New-AzServiceFabricManagedNodeType'</span></span>
    - <span data-ttu-id="184db-819">'Get-AzServiceFabricManagedNodeType'</span><span class="sxs-lookup"><span data-stu-id="184db-819">'Get-AzServiceFabricManagedNodeType'</span></span>
    - <span data-ttu-id="184db-820">'Set-AzServiceFabricManagedNodeType'</span><span class="sxs-lookup"><span data-stu-id="184db-820">'Set-AzServiceFabricManagedNodeType'</span></span>
    - <span data-ttu-id="184db-821">'Remove-AzServiceFabricManagedNodeType'</span><span class="sxs-lookup"><span data-stu-id="184db-821">'Remove-AzServiceFabricManagedNodeType'</span></span>
    - <span data-ttu-id="184db-822">'Add-AzServiceFabricManagedNodeTypeVMExtension'</span><span class="sxs-lookup"><span data-stu-id="184db-822">'Add-AzServiceFabricManagedNodeTypeVMExtension'</span></span>
    - <span data-ttu-id="184db-823">'Add-AzServiceFabricManagedNodeTypeVMSecret'</span><span class="sxs-lookup"><span data-stu-id="184db-823">'Add-AzServiceFabricManagedNodeTypeVMSecret'</span></span>
    - <span data-ttu-id="184db-824">'Remove-AzServiceFabricManagedNodeTypeVMExtension'</span><span class="sxs-lookup"><span data-stu-id="184db-824">'Remove-AzServiceFabricManagedNodeTypeVMExtension'</span></span>
    - <span data-ttu-id="184db-825">'Restart-AzServiceFabricManagedNodeTyp'</span><span class="sxs-lookup"><span data-stu-id="184db-825">'Restart-AzServiceFabricManagedNodeTyp'</span></span>
* <span data-ttu-id="184db-826">Service Fabric SDK를 버전 1.2.0으로 업그레이드했으며, 현재 모델에서는 서비스 패브릭 리소스 제공자 api-version 2020-03-01을, 관리형 클러스터에서는 2020-01-01-preview를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="184db-826">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2020-03-01 for the current model and 2020-01-01-preview for managed clusters.</span></span>

#### <a name="azsql"></a><span data-ttu-id="184db-827">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="184db-827">Az.Sql</span></span>
* <span data-ttu-id="184db-828">BackupStorageRedundancy가 'New-AzSqlInstance' 및 'Get-AzSqlInstance'에 추가됨</span><span class="sxs-lookup"><span data-stu-id="184db-828">Added BackupStorageRedundancy to 'New-AzSqlInstance' and 'Get-AzSqlInstance'</span></span>
* <span data-ttu-id="184db-829">'Get-AzSqlServerActiveDirectoryOnlyAuthentication' cmdlet이 추가됨</span><span class="sxs-lookup"><span data-stu-id="184db-829">Added cmdlet 'Get-AzSqlServerActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="184db-830">'Enable-AzSqlServerActiveDirectoryOnlyAuthentication' cmdlet이 추가됨</span><span class="sxs-lookup"><span data-stu-id="184db-830">Added cmdlet 'Enable-AzSqlServerActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="184db-831">Force 매개 변수가 'New-AzSqlInstance'에 추가됨</span><span class="sxs-lookup"><span data-stu-id="184db-831">Added Force parameter to 'New-AzSqlInstance'</span></span>
* <span data-ttu-id="184db-832">관리되는 데이터베이스 로그 재생 서비스용 cmdlet이 추가됨</span><span class="sxs-lookup"><span data-stu-id="184db-832">Added cmdlets for Managed Database Log Replay service</span></span>
    - <span data-ttu-id="184db-833">'Start-AzSqlInstanceDatabaseLogReplay'</span><span class="sxs-lookup"><span data-stu-id="184db-833">'Start-AzSqlInstanceDatabaseLogReplay'</span></span>
    - <span data-ttu-id="184db-834">'Get-AzSqlInstanceDatabaseLogReplay'</span><span class="sxs-lookup"><span data-stu-id="184db-834">'Get-AzSqlInstanceDatabaseLogReplay'</span></span>
    - <span data-ttu-id="184db-835">'Complete-AzSqlInstanceDatabaseLogReplay'</span><span class="sxs-lookup"><span data-stu-id="184db-835">'Complete-AzSqlInstanceDatabaseLogReplay'</span></span>
    - <span data-ttu-id="184db-836">'Stop-AzSqlInstanceDatabaseLogReplay'</span><span class="sxs-lookup"><span data-stu-id="184db-836">'Stop-AzSqlInstanceDatabaseLogReplay'</span></span>
* <span data-ttu-id="184db-837">'Get-AzSqlInstanceActiveDirectoryOnlyAuthentication' cmdlet이 추가됨</span><span class="sxs-lookup"><span data-stu-id="184db-837">Added cmdlet 'Get-AzSqlInstanceActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="184db-838">'Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication' cmdlet이 추가됨</span><span class="sxs-lookup"><span data-stu-id="184db-838">Added cmdlet 'Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="184db-839">'Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication' cmdlet이 추가됨</span><span class="sxs-lookup"><span data-stu-id="184db-839">Added cmdlet 'Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="184db-840">네트워크 격리 기능을 지원하기 위해 'New-AzSqlDatabaseImport' 및 'New-AzSqlDatabaseExport' cmdlet이 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="184db-840">Updated cmdlets 'New-AzSqlDatabaseImport' and 'New-AzSqlDatabaseExport' to support network isolation functionality</span></span>
* <span data-ttu-id="184db-841">'New-AzSqlDatabaseImportExisting' cmdlet이 추가됨</span><span class="sxs-lookup"><span data-stu-id="184db-841">Added cmdlet 'New-AzSqlDatabaseImportExisting'</span></span>
* <span data-ttu-id="184db-842">백업 스토리지 유형 사양을 지원하도록 데이터베이스 cmdlet이 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="184db-842">Updated Databases cmdlets to support backup storage type specification</span></span>
* <span data-ttu-id="184db-843">Force 매개 변수가 'New-AzSqlDatabase'에 추가됨</span><span class="sxs-lookup"><span data-stu-id="184db-843">Added Force parameter to 'New-AzSqlDatabase'</span></span>
* <span data-ttu-id="184db-844">'New-AzSqlDatabase'의 영역 선택에서 BackupStorageRedundancy 구성에 대한 경고가 추가됨</span><span class="sxs-lookup"><span data-stu-id="184db-844">Added warning for BackupStorageRedundancy configuration in select regions in 'New-AzSqlDatabase'</span></span>
* <span data-ttu-id="184db-845">ResourceId 및 InputObject를 포함하도록 서버 및 인스턴스에 대한 ActiveDirectoryOnlyAuthentication cmdlet이 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="184db-845">Updated ActiveDirectoryOnlyAuthentication cmdlets for server and instance to include ResourceId and InputObject</span></span>

#### <a name="azstorage"></a><span data-ttu-id="184db-846">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="184db-846">Az.Storage</span></span>
* <span data-ttu-id="184db-847">Microsoft.Azure.Storage.DataMovement 2.0.0로 업그레이드하여 blob 업로드 실패 수정됨 [#12220]</span><span class="sxs-lookup"><span data-stu-id="184db-847">Fixed upload blob fail by upgrade to Microsoft.Azure.Storage.DataMovement 2.0.0 [#12220]</span></span>
* <span data-ttu-id="184db-848">지정 시간 복원 지원</span><span class="sxs-lookup"><span data-stu-id="184db-848">Supported Point In Time Restore</span></span>
    - <span data-ttu-id="184db-849">'Enable-AzStorageBlobRestorePolicy'</span><span class="sxs-lookup"><span data-stu-id="184db-849">'Enable-AzStorageBlobRestorePolicy'</span></span>
    - <span data-ttu-id="184db-850">'Disable-AzStorageBlobRestorePolicy'</span><span class="sxs-lookup"><span data-stu-id="184db-850">'Disable-AzStorageBlobRestorePolicy'</span></span>
    - <span data-ttu-id="184db-851">'New-AzStorageBlobRangeToRestore'</span><span class="sxs-lookup"><span data-stu-id="184db-851">'New-AzStorageBlobRangeToRestore'</span></span>
    - <span data-ttu-id="184db-852">'Restore-AzStorageBlobRange'</span><span class="sxs-lookup"><span data-stu-id="184db-852">'Restore-AzStorageBlobRange'</span></span>
* <span data-ttu-id="184db-853">-IncludeBlobRestoreStatus 매개 변수와 함께 get-AzureRMStorageAccount를 실행하여 스토리지 계정의 blob 복원 상태 가져오기 지원</span><span class="sxs-lookup"><span data-stu-id="184db-853">Supported get blob restore status of Storage account by run get-AzureRMStorageAccount with parameter -IncludeBlobRestoreStatus</span></span> 
    - <span data-ttu-id="184db-854">'Get-AzureRMStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="184db-854">'Get-AzureRMStorageAccount'</span></span>
* <span data-ttu-id="184db-855">예정된 cmdlet 출력 변경에 대해 호환성이 손상되는 변경 경고 메시지가 추가됨</span><span class="sxs-lookup"><span data-stu-id="184db-855">Added breaking change warning message for upcoming cmdlet output change</span></span>
    - <span data-ttu-id="184db-856">'Get-AzStorageContainerStoredAccessPolicy'</span><span class="sxs-lookup"><span data-stu-id="184db-856">'Get-AzStorageContainerStoredAccessPolicy'</span></span>
    - <span data-ttu-id="184db-857">'Set-AzStorageContainerStoredAccessPolicy'</span><span class="sxs-lookup"><span data-stu-id="184db-857">'Set-AzStorageContainerStoredAccessPolicy'</span></span>
    - <span data-ttu-id="184db-858">'Set-AzStorageAccountManagementPolicy'</span><span class="sxs-lookup"><span data-stu-id="184db-858">'Set-AzStorageAccountManagementPolicy'</span></span>
    - <span data-ttu-id="184db-859">'Get-AzStorageAccountManagementPolicy'</span><span class="sxs-lookup"><span data-stu-id="184db-859">'Get-AzStorageAccountManagementPolicy'</span></span>
    - <span data-ttu-id="184db-860">'Add-AzStorageAccountManagementPolicyAction'</span><span class="sxs-lookup"><span data-stu-id="184db-860">'Add-AzStorageAccountManagementPolicyAction'</span></span>
    - <span data-ttu-id="184db-861">'New-AzStorageAccountManagementPolicyRule'</span><span class="sxs-lookup"><span data-stu-id="184db-861">'New-AzStorageAccountManagementPolicyRule'</span></span>
* <span data-ttu-id="184db-862">Microsoft.Azure.Cosmos.Table SDK를 1.0.8로 업그레이드</span><span class="sxs-lookup"><span data-stu-id="184db-862">Upgraded Microsoft.Azure.Cosmos.Table SDK to 1.0.8</span></span>

### <a name="thanks-to-our-community-contributors"></a><span data-ttu-id="184db-863">커뮤니티 기여자에게 감사드립니다.</span><span class="sxs-lookup"><span data-stu-id="184db-863">Thanks to our community contributors</span></span>
* <span data-ttu-id="184db-864">Thomas Van Laere(@ThomVanL), Dockerfile-alpine-3.10 추가(#12911)</span><span class="sxs-lookup"><span data-stu-id="184db-864">Thomas Van Laere (@ThomVanL), Add Dockerfile-alpine-3.10 (#12911)</span></span> 
* <span data-ttu-id="184db-865">Lohith Chowdary Chilukuri(@Lochiluk), Remove-AzNetworkInterfaceIpConfig.md 업데이트(#12807)</span><span class="sxs-lookup"><span data-stu-id="184db-865">Lohith Chowdary Chilukuri (@Lochiluk), Update Remove-AzNetworkInterfaceIpConfig.md (#12807)</span></span> 
* <span data-ttu-id="184db-866">Roberth Strand(@roberthstrand), Get-AzResourceGroup - 새로운 예제 및 정리(#12828)</span><span class="sxs-lookup"><span data-stu-id="184db-866">Roberth Strand (@roberthstrand), Get-AzResourceGroup - New example, and cleanup (#12828)</span></span> 
* <span data-ttu-id="184db-867">Ravi Mishra(@inmishrar), Azure 웹앱 런타임 스택을 DOTNETCORE로 업데이트(#12833)</span><span class="sxs-lookup"><span data-stu-id="184db-867">Ravi Mishra (@inmishrar), update Azure Web App runtime stack to DOTNETCORE (#12833)</span></span> 
* <span data-ttu-id="184db-868">@jack-education, NSG 및 라우팅 테이블을 서브넷에서 제거할 수 있도록 Set-AzVirtualNetworkSubnetConfig를 업데이트(# 12351)</span><span class="sxs-lookup"><span data-stu-id="184db-868">@jack-education, Updated Set-AzVirtualNetworkSubnetConfig to allow NSG and Route Table to be removed from subnet (#12351)</span></span> 
* <span data-ttu-id="184db-869">@hagop-globanet, Add-AzApplicationGatewayCustomError.md 업데이트(#12784)</span><span class="sxs-lookup"><span data-stu-id="184db-869">@hagop-globanet, Update Add-AzApplicationGatewayCustomError.md (#12784)</span></span> 
* <span data-ttu-id="184db-870">Joshua Van Daalen(@greenSacrifice)</span><span class="sxs-lookup"><span data-stu-id="184db-870">Joshua Van Daalen (@greenSacrifice)</span></span>
  * <span data-ttu-id="184db-871">속성(Property) 철자를 속성(Property)으로 업데이트(#12821)</span><span class="sxs-lookup"><span data-stu-id="184db-871">Update spelling of Property to Property (#12821)</span></span> 
  * <span data-ttu-id="184db-872">New-AzResourceLock.md 예제 업데이트(#12806)</span><span class="sxs-lookup"><span data-stu-id="184db-872">Update New-AzResourceLock.md examples (#12806)</span></span>
* <span data-ttu-id="184db-873">Eragon Riddle(@eragonriddle), 예제에서 매개 변수 필드 이름 수정(#12825)</span><span class="sxs-lookup"><span data-stu-id="184db-873">Eragon Riddle (@eragonriddle), Corrected parameter field name in the example (#12825)</span></span> 
* <span data-ttu-id="184db-874">@rossifumax, New-AzConfigurationAssignment.md의 오타 수정(#12701)</span><span class="sxs-lookup"><span data-stu-id="184db-874">@rossifumax, Fix typo in New-AzConfigurationAssignment.md (#12701)</span></span>

## <a name="461---august-2020"></a><span data-ttu-id="184db-875">4.6.1 - 2020년 8월</span><span class="sxs-lookup"><span data-stu-id="184db-875">4.6.1 - August 2020</span></span>
#### <a name="azcompute"></a><span data-ttu-id="184db-876">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="184db-876">Az.Compute</span></span>
* <span data-ttu-id="184db-877">'New-AzVm'에서 '-EncryptionAtHost' 매개 변수를 패치하여 기본값인 false가 제거됨[#12776]</span><span class="sxs-lookup"><span data-stu-id="184db-877">Patched '-EncryptionAtHost' parameter in 'New-AzVm' to remove default value of false [#12776]</span></span>

## <a name="460---august-2020"></a><span data-ttu-id="184db-878">4.6.0 - 2020년 8월</span><span class="sxs-lookup"><span data-stu-id="184db-878">4.6.0 - August 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="184db-879">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="184db-879">Az.Accounts</span></span>
* <span data-ttu-id="184db-880">검색 엔드포인트가 기본 AzureCloud나 기타 공용 환경을 반환하지 않는 경우 모든 퍼블릭 클라우드 환경이 로드됨 [#12633]</span><span class="sxs-lookup"><span data-stu-id="184db-880">Loaded all public cloud environments when discovery endpoint doesn't return default AzureCloud or other public environments [#12633]</span></span>
* <span data-ttu-id="184db-881">'Get-AzSubscription'에서 SubscriptionPolicies가 노출됨 [#12551]</span><span class="sxs-lookup"><span data-stu-id="184db-881">Exposed SubscriptionPolicies in 'Get-AzSubscription' [#12551]</span></span>

#### <a name="azautomation"></a><span data-ttu-id="184db-882">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="184db-882">Az.Automation</span></span>
* <span data-ttu-id="184db-883">Hybrid Worker 그룹을 지정하기 위해 'Set-AzAutomationWebhook'에 '-RunOn' 매개 변수가 추가됨</span><span class="sxs-lookup"><span data-stu-id="184db-883">Added '-RunOn' parameters to 'Set-AzAutomationWebhook' to specify a Hybrid Worker Group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="184db-884">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="184db-884">Az.Compute</span></span>
* <span data-ttu-id="184db-885">'New-AzVm', 'New-AzVmss', 'New-AzVMConfig', 'New-AzVmssConfig', 'Update-AzVM', 'Update-AzVmss'에 '-EncryptionAtHost' 매개 변수가 추가됨</span><span class="sxs-lookup"><span data-stu-id="184db-885">Added '-EncryptionAtHost' parameter to 'New-AzVm', 'New-AzVmss', 'New-AzVMConfig', 'New-AzVmssConfig', 'Update-AzVM', and 'Update-AzVmss'</span></span>
* <span data-ttu-id="184db-886">'Get-AzVM' 및 'Get-AzVmss' 반환 개체에 'SecurityProfile'이 추가됨</span><span class="sxs-lookup"><span data-stu-id="184db-886">Added 'SecurityProfile' to 'Get-AzVM' and 'Get-AzVmss' return object</span></span>
* <span data-ttu-id="184db-887">'-InstanceView' 스위치가 'Get-AzHostGroup'에 선택적 매개 변수로 추가됨</span><span class="sxs-lookup"><span data-stu-id="184db-887">Added '-InstanceView' switch as optional parameter to 'Get-AzHostGroup'</span></span>
* <span data-ttu-id="184db-888">새 cmdlet 'Invoke-AzVmPatchAssessment'가 추가됨</span><span class="sxs-lookup"><span data-stu-id="184db-888">Added new cmdlet 'Invoke-AzVmPatchAssessment'</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="184db-889">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="184db-889">Az.DataFactory</span></span>
* <span data-ttu-id="184db-890">PSPipelineRun 클래스에 누락된 속성이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-890">Added missing properties to PSPipelineRun class.</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="184db-891">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="184db-891">Az.HDInsight</span></span>
* <span data-ttu-id="184db-892">호스트 기능에서 암호화를 사용하여 클러스터를 만드는 것이 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="184db-892">Supported creating cluster with encryption at host feature.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="184db-893">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="184db-893">Az.KeyVault</span></span>
* <span data-ttu-id="184db-894">일시 삭제 사용 안 함 계획에 대한 경고 메시지가 추가됨</span><span class="sxs-lookup"><span data-stu-id="184db-894">Added warning messages for planning to disable soft delete</span></span>
* <span data-ttu-id="184db-895">특성 SecretValueText 제거 계획에 대한 경고 메시지가 추가됨</span><span class="sxs-lookup"><span data-stu-id="184db-895">Added warning messages for planning to remove attribute SecretValueText</span></span>

#### <a name="azmaintenance"></a><span data-ttu-id="184db-896">Az.Maintenance</span><span class="sxs-lookup"><span data-stu-id="184db-896">Az.Maintenance</span></span>
* <span data-ttu-id="184db-897">'New-AzMaintenanceConfiguration'에 선택적 일정 관련 필드가 추가됨</span><span class="sxs-lookup"><span data-stu-id="184db-897">Added optional schedule related fields to 'New-AzMaintenanceConfiguration'</span></span>
* <span data-ttu-id="184db-898">'Get-AzMaintenancePublicConfiguration'에 대한 새 cmdlet이 추가됨</span><span class="sxs-lookup"><span data-stu-id="184db-898">Added new cmdlet for 'Get-AzMaintenancePublicConfiguration'</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="184db-899">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="184db-899">Az.ManagedServices</span></span>
* <span data-ttu-id="184db-900">관리되는 서비스 할당 및 정의의 cmdlet에 대한 호환성이 손상되는 변경 경고가 추가됨</span><span class="sxs-lookup"><span data-stu-id="184db-900">Added breaking change warnings on cmdlets of managed services assignment and definition</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="184db-901">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="184db-901">Az.Monitor</span></span>
* <span data-ttu-id="184db-902">로그 및 메트릭 사용을 분리하기 위해 'Set-AzDiagnosticSetting'에 설정된 매개 변수가 확장됨 [#12482]</span><span class="sxs-lookup"><span data-stu-id="184db-902">Extended the parameter set in 'Set-AzDiagnosticSetting' for separation of Logs and Metrics enablement [#12482]</span></span>
* <span data-ttu-id="184db-903">파이프라인에서 메트릭 경고를 가져오는 경우 'Add-AzMetricAlertRuleV2'에 대한 버그가 수정됨</span><span class="sxs-lookup"><span data-stu-id="184db-903">Fixed bug for 'Add-AzMetricAlertRuleV2' when getting metric alert from pipeline</span></span>

#### <a name="azresources"></a><span data-ttu-id="184db-904">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="184db-904">Az.Resources</span></span>
* <span data-ttu-id="184db-905">Azure Policy를 통해 별칭을 수정할 수 있는지 여부를 나타내는 정보를 포함하도록 'Get-AzPolicyAlias' 응답이 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="184db-905">Updated 'Get-AzPolicyAlias' response to include information indicating whether the alias is modifiable by Azure Policy.</span></span>
* <span data-ttu-id="184db-906">새 cmdlet 'Set-AzRoleAssignment'가 생성됨</span><span class="sxs-lookup"><span data-stu-id="184db-906">Created new cmdlet 'Set-AzRoleAssignment'</span></span>
* <span data-ttu-id="184db-907">관리 그룹 범위에서 ARM 템플릿 What-If 결과를 가져오는 'Get-AzDeploymentManagementGroupWhatIfResult'가 추가됨</span><span class="sxs-lookup"><span data-stu-id="184db-907">Added 'Get-AzDeploymentManagementGroupWhatIfResult' for getting ARM template What-If results at management Group scope</span></span>
* <span data-ttu-id="184db-908">테넌트 범위에서 ARM 템플릿 What-If 결과를 가져오는 'Get-AzTenantWhatIfResult' 새 cmdlet이 추가됨</span><span class="sxs-lookup"><span data-stu-id="184db-908">Added 'Get-AzTenantWhatIfResult' new cmdlet for getting ARM template What-If results at tenant scope</span></span>
* <span data-ttu-id="184db-909">ARM 템플릿 What-If 결과를 사용하도록 'New-AzManagementGroupDeployment' 및 'New-AzTenantDeployment'에 대한 '-WhatIf' 및 '-Confirm'이 재정의됨</span><span class="sxs-lookup"><span data-stu-id="184db-909">Overrode '-WhatIf' and '-Confirm' for 'New-AzManagementGroupDeployment' and 'New-AzTenantDeployment' to use ARM template What-If results</span></span>
* <span data-ttu-id="184db-910">새 배포 cmdlet에 대한 '-WhatIf' 및 '-Confirm' 동작이 False를 준수하도록 수정됨</span><span class="sxs-lookup"><span data-stu-id="184db-910">Fixed the behaviors of '-WhatIf' and '-Confirm' for new deployment cmdlets so they comply with False and</span></span> 
* <span data-ttu-id="184db-911">'-TemplateObject' 및 'TemplateParameterObject'에 대한 직렬화 오류가 수정됨 [#1528] [#6292]</span><span class="sxs-lookup"><span data-stu-id="184db-911">Fixed serialization error for '-TemplateObject' and 'TemplateParameterObject' [#1528] [#6292]</span></span>
* <span data-ttu-id="184db-912">예정된 출력 형식 변경을 위해 'Get-AzResourceGroupDeploymentOperation'에 호환성이 손상되는 변경 특성이 추가됨</span><span class="sxs-lookup"><span data-stu-id="184db-912">Added breaking change attribute to 'Get-AzResourceGroupDeploymentOperation' for the upcoming output type change</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="184db-913">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="184db-913">Az.SignalR</span></span>
* <span data-ttu-id="184db-914">'Restart-AzSignalR' 및 'Update-AzSignalR' 도움말 파일 오류가 수정됨</span><span class="sxs-lookup"><span data-stu-id="184db-914">Fixed 'Restart-AzSignalR' and 'Update-AzSignalR' help files errors</span></span>
* <span data-ttu-id="184db-915">'Update-AzSignalRNetworkAcl', 'Set-AzSignalRUpstream' cmdlet이 추가됨</span><span class="sxs-lookup"><span data-stu-id="184db-915">Added cmdlets 'Update-AzSignalRNetworkAcl', 'Set-AzSignalRUpstream'</span></span>

#### <a name="azstorage"></a><span data-ttu-id="184db-916">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="184db-916">Az.Storage</span></span>
* <span data-ttu-id="184db-917">지원되는 Blob 쿼리 가속</span><span class="sxs-lookup"><span data-stu-id="184db-917">Supported blob query acceleration</span></span>
    -  <span data-ttu-id="184db-918">'Get-AzStorageBlobQueryResult'</span><span class="sxs-lookup"><span data-stu-id="184db-918">'Get-AzStorageBlobQueryResult'</span></span>
    -  <span data-ttu-id="184db-919">'New-AzStorageBlobQueryConfig'</span><span class="sxs-lookup"><span data-stu-id="184db-919">'New-AzStorageBlobQueryConfig'</span></span>
* <span data-ttu-id="184db-920">도움말 파일 업데이트, 자세한 설명 추가 및 오타 수정</span><span class="sxs-lookup"><span data-stu-id="184db-920">Updated help file, added more description, and fixed typo</span></span>
    -  <span data-ttu-id="184db-921">'Start-AzStorageBlobCopy'</span><span class="sxs-lookup"><span data-stu-id="184db-921">'Start-AzStorageBlobCopy'</span></span>
    -  <span data-ttu-id="184db-922">'Get-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="184db-922">'Get-AzDataLakeGen2Item'</span></span>
* <span data-ttu-id="184db-923">관련 하위 디렉터리가 없는 경우 Blob 다운로드 실패가 수정됨 [#12592]</span><span class="sxs-lookup"><span data-stu-id="184db-923">Fixed download blob fail when related sub directory not exist [#12592]</span></span>
    -  <span data-ttu-id="184db-924">'Get-AzStorageBlobContent'</span><span class="sxs-lookup"><span data-stu-id="184db-924">'Get-AzStorageBlobContent'</span></span>
* <span data-ttu-id="184db-925">스토리지 계정에 대해 개체 복제 정책 설정/가져오기/제거가 지원됨</span><span class="sxs-lookup"><span data-stu-id="184db-925">Supported Set/Get/Remove Object Replication Policy on Storage accounts</span></span>
    - <span data-ttu-id="184db-926">'New-AzStorageObjectReplicationPolicyRule'</span><span class="sxs-lookup"><span data-stu-id="184db-926">'New-AzStorageObjectReplicationPolicyRule'</span></span>
    - <span data-ttu-id="184db-927">'Set-AzStorageObjectReplicationPolicy'</span><span class="sxs-lookup"><span data-stu-id="184db-927">'Set-AzStorageObjectReplicationPolicy'</span></span>
    - <span data-ttu-id="184db-928">'Get-AzStorageObjectReplicationPolicy'</span><span class="sxs-lookup"><span data-stu-id="184db-928">'Get-AzStorageObjectReplicationPolicy'</span></span>
    - <span data-ttu-id="184db-929">'Remove-AzStorageObjectReplicationPolicy'</span><span class="sxs-lookup"><span data-stu-id="184db-929">'Remove-AzStorageObjectReplicationPolicy'</span></span>
* <span data-ttu-id="184db-930">스토리지 계정의 Blob Service에서 ChangeFeed 사용/사용 안 함이 지원됨</span><span class="sxs-lookup"><span data-stu-id="184db-930">Supported enable/disable ChangeFeed on Blob Service of a Storage account</span></span>
    - <span data-ttu-id="184db-931">'Update-AzStorageBlobServiceProperty'</span><span class="sxs-lookup"><span data-stu-id="184db-931">'Update-AzStorageBlobServiceProperty'</span></span>

## <a name="450---august-2020"></a><span data-ttu-id="184db-932">4.5.0 - 2020년 8월</span><span class="sxs-lookup"><span data-stu-id="184db-932">4.5.0 - August 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="184db-933">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="184db-933">Az.Accounts</span></span>
* <span data-ttu-id="184db-934">매개 변수 'MaxContextPopulation'을 허용하도록 'Connect-AzAccount' 업데이트됨 [# 9865]</span><span class="sxs-lookup"><span data-stu-id="184db-934">Updated 'Connect-AzAccount' to accept parameter 'MaxContextPopulation' [#9865]</span></span>
* <span data-ttu-id="184db-935">SubscriptionClient 버전이 2019-06-01로 업데이트되고 테넌트 도메인을 표시 [#9838]</span><span class="sxs-lookup"><span data-stu-id="184db-935">Updated SubscriptionClient version to 2019-06-01 and display tenant domains [#9838]</span></span>
* <span data-ttu-id="184db-936">구독의 managedBy 테넌트 정보 및 홈 테넌트 지원</span><span class="sxs-lookup"><span data-stu-id="184db-936">Supported home tenant and managedBy tenant information of subscription</span></span>
* <span data-ttu-id="184db-937">원격 분석 데이터의 모듈 이름, 버전 정보 수정</span><span class="sxs-lookup"><span data-stu-id="184db-937">Corrected module name, version info in telemetry data</span></span>
* <span data-ttu-id="184db-938">환경 메타데이터 엔드포인트가 호환되지 않는 값을 반환하는 경우 SqlDatabaseDnsSuffix 및 ServiceManagementUrl이 조정됨</span><span class="sxs-lookup"><span data-stu-id="184db-938">Adjusted SqlDatabaseDnsSuffix and ServiceManagementUrl if environment metadata endpoint returns incompatible value</span></span>

#### <a name="azaks"></a><span data-ttu-id="184db-939">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="184db-939">Az.Aks</span></span>
* <span data-ttu-id="184db-940">'ClientIdAndSecret'을 'ServicePrincipalIdAndSecret'으로 제거하고 'ClientIdAndSecret'을 별칭으로 설정함 [#12381]</span><span class="sxs-lookup"><span data-stu-id="184db-940">Removed 'ClientIdAndSecret' to 'ServicePrincipalIdAndSecret' and set 'ClientIdAndSecret' as an alias [#12381].</span></span>
* <span data-ttu-id="184db-941">'Get-AzAks'/'New-AzAks'/'Remove-AzAks'/'Set-AzAks'를 'Get-AzAksCluster'/'New-AzAksCluster'/'Remove-AzAksCluster'/'Set-AzAksCluster'로 제거하고 원본을 별칭으로 설정함 [#12373].</span><span class="sxs-lookup"><span data-stu-id="184db-941">Removed 'Get-AzAks'/'New-AzAks'/'Remove-AzAks'/'Set-AzAks' to 'Get-AzAksCluster'/'New-AzAksCluster'/'Remove-AzAksCluster'/'Set-AzAksCluster' and set the original ones as alias [#12373].</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="184db-942">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="184db-942">Az.ApiManagement</span></span>
* <span data-ttu-id="184db-943">새 'Add-AzApiManagementApiToGateway' cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-943">Added new 'Add-AzApiManagementApiToGateway' cmdlet.</span></span>
* <span data-ttu-id="184db-944">새 'Get-AzApiManagementGateway' cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-944">Added new 'Get-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="184db-945">새 'Get-AzApiManagementGatewayHostnameConfiguration' cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-945">Added new 'Get-AzApiManagementGatewayHostnameConfiguration' cmdlet.</span></span>
* <span data-ttu-id="184db-946">새 'Get-AzApiManagementGatewayKey' cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-946">Added new 'Get-AzApiManagementGatewayKey' cmdlet.</span></span>
* <span data-ttu-id="184db-947">새 'New-AzApiManagementGateway' cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-947">Added new 'New-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="184db-948">새 'New-AzApiManagementGatewayHostnameConfiguration' cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-948">Added new 'New-AzApiManagementGatewayHostnameConfiguration' cmdlet.</span></span>
* <span data-ttu-id="184db-949">새 'New-AzApiManagementResourceLocationObject' cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-949">Added new 'New-AzApiManagementResourceLocationObject' cmdlet.</span></span>
* <span data-ttu-id="184db-950">새 'Remove-AzApiManagementApiFromGateway' cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-950">Added new 'Remove-AzApiManagementApiFromGateway' cmdlet.</span></span>
* <span data-ttu-id="184db-951">새 'Remove-AzApiManagementGateway' cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-951">Added new 'Remove-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="184db-952">새 'Remove-AzApiManagementGatewayHostnameConfiguration' cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-952">Added new 'Remove-AzApiManagementGatewayHostnameConfiguration' cmdlet.</span></span>
* <span data-ttu-id="184db-953">새 'Update-AzApiManagementGateway' cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-953">Added new 'Update-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="184db-954">'Get-AzApiManagementApi' cmdlet에 선택적 [-GatewayId] 매개 변수가 새로 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-954">Added new optional [-GatewayId] parameter to the 'Get-AzApiManagementApi' cmdlet.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="184db-955">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="184db-955">Az.CognitiveServices</span></span>
* <span data-ttu-id="184db-956">'Deny'가 특히 NetworkRules 기본 작업으로 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="184db-956">Used 'Deny' specifically as NetworkRules default action.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="184db-957">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="184db-957">Az.FrontDoor</span></span>
* <span data-ttu-id="184db-958">Enum.Parse가 null 값을 Enabled 또는 Disabled 열거형 값으로 강제 변환하려는 경우 예외가 throw되는 문제를 수정했습니다. [#12344]</span><span class="sxs-lookup"><span data-stu-id="184db-958">Fixed an issue where an exception is being thrown when Enum.Parse tries to coerce a null value to an Enabled or Disabled enum values [#12344]</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="184db-959">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="184db-959">Az.HDInsight</span></span>
* <span data-ttu-id="184db-960">전송 중 암호화 기능을 사용하여 클러스터를 만드는 것이 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="184db-960">Supported creating cluster with encryption in transit feature.</span></span>
    - <span data-ttu-id="184db-961">cmdlet 'New-AzHDInsightCluster'에 새 매개 변수 'EncryptionInTransit' 추가</span><span class="sxs-lookup"><span data-stu-id="184db-961">Add new parameter 'EncryptionInTransit' to the cmdlet 'New-AzHDInsightCluster'</span></span>
    - <span data-ttu-id="184db-962">cmdlet 'New-AzHDInsightClusterConfig'에 새 매개 변수 'EncryptionInTransit' 추가</span><span class="sxs-lookup"><span data-stu-id="184db-962">Add new parameter 'EncryptionInTransit' to the cmdlet 'New-AzHDInsightClusterConfig'</span></span>
* <span data-ttu-id="184db-963">프라이빗 링크 기능을 사용하여 클러스터를 만드는 것이 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="184db-963">Supported creating cluster with private link feature:</span></span>
    - <span data-ttu-id="184db-964">cmdlet 'New-AzHDInsightCluster'에 새 매개 변수 'PublicNetworkAccessType' 및 'OutboundPublicNetworkAccessType' 추가</span><span class="sxs-lookup"><span data-stu-id="184db-964">Add new parameter 'PublicNetworkAccessType' and 'OutboundPublicNetworkAccessType' to the cmdlet 'New-AzHDInsightCluster'</span></span>
    - <span data-ttu-id="184db-965">cmdlet 'New-AzHDInsightClusterConfig'에 새 매개 변수 'PublicNetworkAccessType' 및 'OutboundPublicNetworkAccessType' 추가</span><span class="sxs-lookup"><span data-stu-id="184db-965">Add new parameter 'PublicNetworkAccessType' and 'OutboundPublicNetworkAccessType' to the cmdlet 'New-AzHDInsightClusterConfig'</span></span>
* <span data-ttu-id="184db-966">'New-AzHDInsightCluster' 또는 'Get-AzHDInsightCluster'를 호출하는 경우 가상 네트워크 정보가 반환됨</span><span class="sxs-lookup"><span data-stu-id="184db-966">Returned virtual network information when calling 'New-AzHDInsightCluster' or 'Get-AzHDInsightCluster'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="184db-967">Az.Network</span><span class="sxs-lookup"><span data-stu-id="184db-967">Az.Network</span></span>
* <span data-ttu-id="184db-968">'Remove-AzExpressRouteCircuitConnectionConfig'에 AddressPrefixType 매개 변수 지원 추가</span><span class="sxs-lookup"><span data-stu-id="184db-968">Added support for AddressPrefixType parameter to 'Remove-AzExpressRouteCircuitConnectionConfig'</span></span>
* <span data-ttu-id="184db-969">작업을 중단하지 않는 변경이 추가됨: 'Remove-AzExpressRouteCircutPeeringConfig'의 프라이빗 피어링을 위한 PeerAddressType 기능</span><span class="sxs-lookup"><span data-stu-id="184db-969">Added non-breaking changes: PeerAddressType functionality for Private Peering in 'Remove-AzExpressRouteCircutPeeringConfig'.</span></span>
* <span data-ttu-id="184db-970">AddressPrefixType 및 PeerAddressType 매개 변수의 대/소문자를 무시하도록 코드가 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-970">Code changed to ignore case for AddressPrefixType and PeerAddressType parameter.</span></span>
* <span data-ttu-id="184db-971">'New-AzLoadBalancerFrontendIpConfig', 'New-AzPublicIpAddress' 및 'New-AzPublicIpPrefix'에 대한 경고 메시지를 수정했습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-971">Modified the warning message for 'New-AzLoadBalancerFrontendIpConfig', 'New-AzPublicIpAddress' and 'New-AzPublicIpPrefix'.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="184db-972">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="184db-972">Az.OperationalInsights</span></span>
* <span data-ttu-id="184db-973">'Remove-AzOperationalInsightsworkspace'에 대한 '-ForceDelete' 옵션이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-973">Added '-ForceDelete' option for 'Remove-AzOperationalInsightsworkspace'</span></span>
* <span data-ttu-id="184db-974">새 cmdlet 'Get-AzOperationalInsightsDeletedWorkspace'가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-974">Added new cmdlet 'Get-AzOperationalInsightsDeletedWorkspace'</span></span>
* <span data-ttu-id="184db-975">새 cmdlet 'Restore-AzOperationalInsightsWorkspace'가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-975">Added new cmdlet 'Restore-AzOperationalInsightsWorkspace'</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="184db-976">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="184db-976">Az.RecoveryServices</span></span>
* <span data-ttu-id="184db-977">Azure Backup 컨테이너/항목 검색 환경이 개선되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-977">Improved the Azure Backup container/item discovery experience.</span></span>

#### <a name="azresources"></a><span data-ttu-id="184db-978">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="184db-978">Az.Resources</span></span>
* <span data-ttu-id="184db-979">'New-AzRoleAssignment'에 'Condition', 'ConditionVersion' 및 'Description' 속성을 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-979">Added properties 'Condition', 'ConditionVersion' and 'Description' to 'New-AzRoleAssignment'</span></span>
    - <span data-ttu-id="184db-980">여기에는 데이터 모델과 관련된 모든 변경 사항이 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="184db-980">This included all the relevant changes to the data models</span></span>

#### <a name="azsql"></a><span data-ttu-id="184db-981">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="184db-981">Az.Sql</span></span>
* <span data-ttu-id="184db-982">'New-AzSqlServer' 'Set-AzSqlServer'에서 서버 이름 대/소문자를 구분하지 않는 잠재적인 오류를 수정했습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-982">Fixed potential server name case insensitive error in 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>
* <span data-ttu-id="184db-983">'New-AzSqlDatabaseSecondary'의 기존 데이터베이스 오류에서 반환되는 잘못된 데이터베이스 이름을 수정했습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-983">Fixed wrong database name returned on existing database error in 'New-AzSqlDatabaseSecondary'</span></span>

#### <a name="azstorage"></a><span data-ttu-id="184db-984">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="184db-984">Az.Storage</span></span>
* <span data-ttu-id="184db-985">새 권한 x,t를 사용하여 컨테이너/blob Sas 토큰 만들기 지원</span><span class="sxs-lookup"><span data-stu-id="184db-985">Supported create container/blob Sas token with new permission x,t</span></span>
    -  <span data-ttu-id="184db-986">'New-AzStorageBlobSASToken'</span><span class="sxs-lookup"><span data-stu-id="184db-986">'New-AzStorageBlobSASToken'</span></span>
    -  <span data-ttu-id="184db-987">'New-AzStorageContainerSASToken'</span><span class="sxs-lookup"><span data-stu-id="184db-987">'New-AzStorageContainerSASToken'</span></span>
* <span data-ttu-id="184db-988">새 권한 x,t,f를 사용하여 계정 Sas 토큰 만들기 지원</span><span class="sxs-lookup"><span data-stu-id="184db-988">Supported create account Sas token with new permission x,t,f</span></span>
    -  <span data-ttu-id="184db-989">'New-AzStorageAccountSASToken'</span><span class="sxs-lookup"><span data-stu-id="184db-989">'New-AzStorageAccountSASToken'</span></span>
* <span data-ttu-id="184db-990">단일 파일 사용량 공유 가져오기 지원</span><span class="sxs-lookup"><span data-stu-id="184db-990">Supported get single file share usage</span></span>
    - <span data-ttu-id="184db-991">'Get-AzRmStorageShare'</span><span class="sxs-lookup"><span data-stu-id="184db-991">'Get-AzRmStorageShare'</span></span>

## <a name="440---july-2020"></a><span data-ttu-id="184db-992">4.4.0 - 2020년 7월</span><span class="sxs-lookup"><span data-stu-id="184db-992">4.4.0 - July 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="184db-993">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="184db-993">Az.Accounts</span></span>
* <span data-ttu-id="184db-994">새 cmdlet 'Invoke-AzRestMethod' 추가</span><span class="sxs-lookup"><span data-stu-id="184db-994">Added new cmdlet 'Invoke-AzRestMethod'</span></span>
* <span data-ttu-id="184db-995">'Start-Job'을 사용하여 여러 Azure PowerShell cmdlet을 실행하는 등 다중 프로세스 시나리오에서 인증 오류를 발생시킬 수 있는 문제 해결 [#9448]</span><span class="sxs-lookup"><span data-stu-id="184db-995">Fixed an issue that may cause authentication errors in multi-process scenarios such as running multiple Azure PowerShell cmdlets using 'Start-Job' [#9448]</span></span>

#### <a name="azaks"></a><span data-ttu-id="184db-996">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="184db-996">Az.Aks</span></span>
* <span data-ttu-id="184db-997">'Get-AzAks'가 모든 클러스터를 가져오지 않는 버그 수정 [#12296]</span><span class="sxs-lookup"><span data-stu-id="184db-997">Fixed bug 'Get-AzAks' doesn't get all clusters [#12296]</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="184db-998">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="184db-998">Az.AnalysisServices</span></span>
* <span data-ttu-id="184db-999">인증에 대한 프로젝트 참조 제거</span><span class="sxs-lookup"><span data-stu-id="184db-999">Removed project reference to Authentication</span></span>

#### <a name="azautomation"></a><span data-ttu-id="184db-1000">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="184db-1000">Az.Automation</span></span>
* <span data-ttu-id="184db-1001">이스케이프 문자를 포함하는 문자열을 json 개체로 변환할 수 없는 문제 해결</span><span class="sxs-lookup"><span data-stu-id="184db-1001">Fixed the issue that string with escape chars cannot be converted into json object.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="184db-1002">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="184db-1002">Az.Compute</span></span>
* <span data-ttu-id="184db-1003">'latest' 이미지 버전이 없는 'New-AzVmss'를 사용하는 경우 경고 추가</span><span class="sxs-lookup"><span data-stu-id="184db-1003">Added warning when using 'New-AzVmss' without 'latest' image version</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="184db-1004">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="184db-1004">Az.DataFactory</span></span>
* <span data-ttu-id="184db-1005">Data Factory에 대한 전역 매개 변수를 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-1005">Added global parameters to Data Factory.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="184db-1006">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="184db-1006">Az.EventGrid</span></span>
* <span data-ttu-id="184db-1007">2020-06-01 API 버전을 사용하도록 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-1007">Updated to use the 2020-06-01 API version.</span></span>
* <span data-ttu-id="184db-1008">추가된 새로운 기능:</span><span class="sxs-lookup"><span data-stu-id="184db-1008">Added new features:</span></span>
    - <span data-ttu-id="184db-1009">입력 매핑</span><span class="sxs-lookup"><span data-stu-id="184db-1009">Input mapping</span></span>
    - <span data-ttu-id="184db-1010">이벤트 배달 스키마</span><span class="sxs-lookup"><span data-stu-id="184db-1010">Event Delivery Schema</span></span>
    - <span data-ttu-id="184db-1011">Private Link</span><span class="sxs-lookup"><span data-stu-id="184db-1011">Private Link</span></span>
    - <span data-ttu-id="184db-1012">클라우드 이벤트 V10 스키마</span><span class="sxs-lookup"><span data-stu-id="184db-1012">Cloud Event V10 Schema</span></span>
    - <span data-ttu-id="184db-1013">대상으로 Service Bus 항목</span><span class="sxs-lookup"><span data-stu-id="184db-1013">Service Bus Topic As Destination</span></span>
    - <span data-ttu-id="184db-1014">대상으로 Azure 함수</span><span class="sxs-lookup"><span data-stu-id="184db-1014">Azure Function As Destination</span></span>
    - <span data-ttu-id="184db-1015">WebHook 일괄 처리</span><span class="sxs-lookup"><span data-stu-id="184db-1015">WebHook Batching</span></span>
    - <span data-ttu-id="184db-1016">보안 웹후크(AAD 지원)</span><span class="sxs-lookup"><span data-stu-id="184db-1016">Secure webhook (AAD support)</span></span>
    - <span data-ttu-id="184db-1017">IpFiltering</span><span class="sxs-lookup"><span data-stu-id="184db-1017">IpFiltering</span></span>
* <span data-ttu-id="184db-1018">다음 Cmdlet이 업데이트 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-1018">Updated cmdlets:</span></span>
    - <span data-ttu-id="184db-1019">'New-AzEventGridSubscription'/'Update-AzEventGridSubscription':</span><span class="sxs-lookup"><span data-stu-id="184db-1019">'New-AzEventGridSubscription'/'Update-AzEventGridSubscription':</span></span>
        - <span data-ttu-id="184db-1020">웹후크 일괄 처리를 지원하기 위해 새로운 선택적 매개 변수를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="184db-1020">Add new optional parameters to support webhook batching.</span></span>
        - <span data-ttu-id="184db-1021">AAD를 사용하여 보안 웹후크를 지원하는 새로운 선택적 매개 변수를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="184db-1021">Add new optional parameters to support secured webhook using AAD.</span></span>
        - <span data-ttu-id="184db-1022">Azure 함수 및 Service Bus 항목을 새 대상으로 지원하기 위해 EndpointType 매개 변수에 대한 새 열거형을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="184db-1022">Add new enum for EndpointType parameter to support azure function and service bus topic as new destinations.</span></span>
        - <span data-ttu-id="184db-1023">배달 스키마에 대한 새로운 선택적 매개 변수를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="184db-1023">Add new optional parameter for delivery schema.</span></span>
    - <span data-ttu-id="184db-1024">'New-AzEventGridTopic'/'Update-AzEventGridTopic' 및 'New-AzEventGridDomain'/'Update-AzEventGridDomain':</span><span class="sxs-lookup"><span data-stu-id="184db-1024">'New-AzEventGridTopic'/'Update-AzEventGridTopic' and 'New-AzEventGridDomain'/'Update-AzEventGridDomain':</span></span>
        - <span data-ttu-id="184db-1025">IpFiltering을 지원하기 위해 새로운 선택적 매개 변수를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="184db-1025">Add new optional parameters to support IpFiltering.</span></span>
    - <span data-ttu-id="184db-1026">'New-AzEventGridTopic'/'New-AzEventGridDomain':</span><span class="sxs-lookup"><span data-stu-id="184db-1026">'New-AzEventGridTopic'/'New-AzEventGridDomain':</span></span>
        - <span data-ttu-id="184db-1027">입력 매핑을 지원하기 위해 새로운 선택적 매개 변수를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="184db-1027">Add new optional parameters to support Input mapping.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="184db-1028">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="184db-1028">Az.FrontDoor</span></span>
* <span data-ttu-id="184db-1029">API 2020-05-01을 사용하도록 업데이트된 모듈</span><span class="sxs-lookup"><span data-stu-id="184db-1029">Updated module to use API 2020-05-01</span></span>
* <span data-ttu-id="184db-1030">Storage, Keyvault 및 Web App Service 리소스에 대한 프라이빗 링크 지원을 추가함</span><span class="sxs-lookup"><span data-stu-id="184db-1030">Added Private link support for Storage, Keyvault and Web App Service resources</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="184db-1031">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="184db-1031">Az.HDInsight</span></span>
* <span data-ttu-id="184db-1032">국가 클라우드에서 ADLSGen1/2 스토리지로 클러스터를 만드는 것이 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="184db-1032">Supported creating cluster with ADLSGen1/2 storage in national clouds.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="184db-1033">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="184db-1033">Az.Monitor</span></span>
* <span data-ttu-id="184db-1034">메트릭 또는 로그가 null인 경우 'Get-AzDiagnosticSetting'에 대한 버그 수정 [#12272]</span><span class="sxs-lookup"><span data-stu-id="184db-1034">Fixed bug for 'Get-AzDiagnosticSetting' when metrics or logs are null [#12272]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="184db-1035">Az.Network</span><span class="sxs-lookup"><span data-stu-id="184db-1035">Az.Network</span></span>
* <span data-ttu-id="184db-1036">VWan HubVnet 연결의 매개 변수 교환 수정</span><span class="sxs-lookup"><span data-stu-id="184db-1036">Fixed parameters swap in VWan HubVnet connection</span></span>
* <span data-ttu-id="184db-1037">Azure Network Virtual Appliance 사이트에 대한 새 cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="184db-1037">Added new cmdlets for Azure Network Virtual Appliance Sites</span></span>
    - <span data-ttu-id="184db-1038">'Get-AzVirtualApplianceSite'</span><span class="sxs-lookup"><span data-stu-id="184db-1038">'Get-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="184db-1039">'New-AzVirtualApplianceSite'</span><span class="sxs-lookup"><span data-stu-id="184db-1039">'New-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="184db-1040">'Remove-AzVirtualApplianceSite'</span><span class="sxs-lookup"><span data-stu-id="184db-1040">'Remove-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="184db-1041">'Update-AzVirtualApplianceSite'</span><span class="sxs-lookup"><span data-stu-id="184db-1041">'Update-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="184db-1042">'New-AzOffice365PolicyProperty'</span><span class="sxs-lookup"><span data-stu-id="184db-1042">'New-AzOffice365PolicyProperty'</span></span>
* <span data-ttu-id="184db-1043">Azure Network Virtual Appliance에 대한 새 cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="184db-1043">Added new cmdlets for Azure Network Virtual Appliance</span></span>
    - <span data-ttu-id="184db-1044">'Get-AzNetworkVirtualAppliance'</span><span class="sxs-lookup"><span data-stu-id="184db-1044">'Get-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="184db-1045">'New-AzNetworkVirtualAppliance'</span><span class="sxs-lookup"><span data-stu-id="184db-1045">'New-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="184db-1046">'Remove-AzNetworkVirtualAppliance'</span><span class="sxs-lookup"><span data-stu-id="184db-1046">'Remove-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="184db-1047">'Update-AzNetworkVirtualAppliance'</span><span class="sxs-lookup"><span data-stu-id="184db-1047">'Update-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="184db-1048">'Get-AzNetworkVirtualApplianceSku'</span><span class="sxs-lookup"><span data-stu-id="184db-1048">'Get-AzNetworkVirtualApplianceSku'</span></span>
    - <span data-ttu-id="184db-1049">'New-AzVirtualApplianceSkuProperty'</span><span class="sxs-lookup"><span data-stu-id="184db-1049">'New-AzVirtualApplianceSkuProperty'</span></span>
* <span data-ttu-id="184db-1050">Application Gateway를 Private Link 공통 cmdlet에 온보딩</span><span class="sxs-lookup"><span data-stu-id="184db-1050">Onboarded Application Gateway to Private Link Common Cmdlets</span></span>
* <span data-ttu-id="184db-1051">StorageSync를 Private Link 공통 cmdlet에 온보딩</span><span class="sxs-lookup"><span data-stu-id="184db-1051">Onboarded StorageSync to Private Link Common Cmdlets</span></span>
* <span data-ttu-id="184db-1052">SignalR을 Private Link 공통 cmdlet에 온보딩</span><span class="sxs-lookup"><span data-stu-id="184db-1052">Onboarded SignalR to Private Link Common Cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="184db-1053">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="184db-1053">Az.RecoveryServices</span></span>
* <span data-ttu-id="184db-1054">인증에 대한 프로젝트 참조 제거</span><span class="sxs-lookup"><span data-stu-id="184db-1054">Removed project reference to Authentication</span></span>
* <span data-ttu-id="184db-1055">Azure Backup 튜닝 cmdlet은 텍스트를 보다 정확하게 작성하는 데 도움이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="184db-1055">Azure Backup tuned cmdlets help text to be more accurate.</span></span>
* <span data-ttu-id="184db-1056">Azure Backup은 'Get-AzRecoveryServicesBackupJob' cmdlet을 사용하여 MAB 에이전트 작업을 가져오는 지원을 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-1056">Azure Backup added support for fetching MAB agent jobs using 'Get-AzRecoveryServicesBackupJob' cmdlet.</span></span>

#### <a name="azresources"></a><span data-ttu-id="184db-1057">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="184db-1057">Az.Resources</span></span>
* <span data-ttu-id="184db-1058">SDK를 사용하도록 'Save-AzResourceGroupDeploymentTemplate'을 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-1058">Updated 'Save-AzResourceGroupDeploymentTemplate' to use the SDK.</span></span>
* <span data-ttu-id="184db-1059">'Unregister-AzResourceProvider' cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-1059">Added 'Unregister-AzResourceProvider' cmdlet.</span></span>

#### <a name="azsql"></a><span data-ttu-id="184db-1060">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="184db-1060">Az.Sql</span></span>
* <span data-ttu-id="184db-1061">Set-AzSqlInstanceActiveDirectoryAdministrator cmdlet에서 서비스 주체 및 게스트 사용자에 대한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-1061">Added support for Service principal and guest users in Set-AzSqlInstanceActiveDirectoryAdministrator cmdlet'</span></span>
* <span data-ttu-id="184db-1062">데이터 분류 cmdlet의 버그를 수정했습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-1062">Fixed a bug in Data Classification cmdlets.'</span></span>
* <span data-ttu-id="184db-1063">다음의 Azure SQL Managed Instance 장애 조치에 대한 지원 추가: 'Invoke-AzSqlInstanceFailover'</span><span class="sxs-lookup"><span data-stu-id="184db-1063">Added support for Azure SQL Managed Instance failover: 'Invoke-AzSqlInstanceFailover'</span></span>

#### <a name="azstorage"></a><span data-ttu-id="184db-1064">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="184db-1064">Az.Storage</span></span>
* <span data-ttu-id="184db-1065">일부 데이터 평면 cmdlet에 대해 UserAgent가 추가되지 않는 문제를 해결했습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-1065">Fixed the issue that UserAgent is not added for some data plane cmdlets.</span></span>
* <span data-ttu-id="184db-1066">MinimumTlsVersion 및 AllowBlobPublicAccess로 스토리지 계정 만들기/업데이트 지원</span><span class="sxs-lookup"><span data-stu-id="184db-1066">Supported create/update Storage account with MinimumTlsVersion and AllowBlobPublicAccess</span></span>
    -  <span data-ttu-id="184db-1067">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="184db-1067">'New-AzStorageAccount'</span></span>
    -  <span data-ttu-id="184db-1068">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="184db-1068">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="184db-1069">스토리지 계정의 Blob Service에서 버전 관리 사용/사용 안 함 지원</span><span class="sxs-lookup"><span data-stu-id="184db-1069">Support enable/disable versioning on Blob Service of a Storage account</span></span>
    - <span data-ttu-id="184db-1070">'Update-AzStorageBlobServiceProperty'</span><span class="sxs-lookup"><span data-stu-id="184db-1070">'Update-AzStorageBlobServiceProperty'</span></span>
* <span data-ttu-id="184db-1071">Blob 버전 관리로 Blob 나열 지원</span><span class="sxs-lookup"><span data-stu-id="184db-1071">Support list blobs with blob versions</span></span>
    - <span data-ttu-id="184db-1072">'Get-AzStorageBlob'</span><span class="sxs-lookup"><span data-stu-id="184db-1072">'Get-AzStorageBlob'</span></span>
* <span data-ttu-id="184db-1073">단일 Blob 스냅샷 또는 Blob 버전 가져오기/제거 지원</span><span class="sxs-lookup"><span data-stu-id="184db-1073">Support get/remove single blob snapshot or blob version</span></span>
    - <span data-ttu-id="184db-1074">'Get-AzStorageBlob'</span><span class="sxs-lookup"><span data-stu-id="184db-1074">'Get-AzStorageBlob'</span></span>
    - <span data-ttu-id="184db-1075">'Remove-AzStorageBlob'</span><span class="sxs-lookup"><span data-stu-id="184db-1075">'Remove-AzStorageBlob'</span></span>
* <span data-ttu-id="184db-1076">Azure.Storage.Blobs V12에서 생성된 Blob 개체의 파이프라인 지원</span><span class="sxs-lookup"><span data-stu-id="184db-1076">Support pipeline from blob object generated from Azure.Storage.Blobs V12</span></span>
    - <span data-ttu-id="184db-1077">'Get-AzStorageBlobContent'</span><span class="sxs-lookup"><span data-stu-id="184db-1077">'Get-AzStorageBlobContent'</span></span>
    - <span data-ttu-id="184db-1078">'New-AzStorageBlobSASToken'</span><span class="sxs-lookup"><span data-stu-id="184db-1078">'New-AzStorageBlobSASToken'</span></span>
    - <span data-ttu-id="184db-1079">'Remove-AzStorageBlob'</span><span class="sxs-lookup"><span data-stu-id="184db-1079">'Remove-AzStorageBlob'</span></span>
    - <span data-ttu-id="184db-1080">'Set-AzStorageBlobContent'</span><span class="sxs-lookup"><span data-stu-id="184db-1080">'Set-AzStorageBlobContent'</span></span>
    - <span data-ttu-id="184db-1081">'Start-AzStorageBlobCopy'</span><span class="sxs-lookup"><span data-stu-id="184db-1081">'Start-AzStorageBlobCopy'</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="184db-1082">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="184db-1082">Az.StorageSync</span></span>
* <span data-ttu-id="184db-1083">ApiVersion 2020-03-01을 대상으로 하는 새 버전의 StorageSync SDK 추가</span><span class="sxs-lookup"><span data-stu-id="184db-1083">Added a new version StorageSync SDK targeting ApiVersion 2020-03-01</span></span>
* <span data-ttu-id="184db-1084">스토리지 동기화 서비스 업데이트 cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="184db-1084">Added Update Storage Sync Service cmdlet</span></span>
    - <span data-ttu-id="184db-1085">'Set-AzStorageSyncService'</span><span class="sxs-lookup"><span data-stu-id="184db-1085">'Set-AzStorageSyncService'</span></span>
* <span data-ttu-id="184db-1086">IncomingTrafficPolicy 및 PrivateEndpointConnections가 StorageSyncService cmdlet에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-1086">Added IncomingTrafficPolicy and PrivateEndpointConnections to StorageSyncService cmdlets.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="184db-1087">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="184db-1087">Az.Websites</span></span>
* <span data-ttu-id="184db-1088">App Service 계획과 동일한 리소스 그룹에 속하지 않는 슬롯에 대한 작업을 수행하기 위한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="184db-1088">Added support to perform operations for Slots not in the same resource group as the App Service Plan</span></span>

## <a name="430---june-2020"></a><span data-ttu-id="184db-1089">4.3.0 - 2020년 6월</span><span class="sxs-lookup"><span data-stu-id="184db-1089">4.3.0 - June 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="184db-1090">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="184db-1090">Az.Accounts</span></span>
* <span data-ttu-id="184db-1091">기본적으로 환경 검색 설정이 지원되며 'Add-AzEnvironment'를 통해 환경을 추가할 수 있음</span><span class="sxs-lookup"><span data-stu-id="184db-1091">Supported discovering environment setting by default and adding environment via 'Add-AzEnvironment'</span></span>
* <span data-ttu-id="184db-1092">미리 로드된 어셈블리 업데이트 [#12024], [#11976]</span><span class="sxs-lookup"><span data-stu-id="184db-1092">Update preloaded assemblies [#12024], [#11976]</span></span>
* <span data-ttu-id="184db-1093">Azure.Core 어셈블리 업데이트</span><span class="sxs-lookup"><span data-stu-id="184db-1093">Updated Azure.Core assembly</span></span>
* <span data-ttu-id="184db-1094">다중 스레드 실행에서 'Connect-AzAccount'가 실패할 수 있는 문제 해결 [#11201]</span><span class="sxs-lookup"><span data-stu-id="184db-1094">Fixed an issue that may cause 'Connect-AzAccount' to fail in multi-threaded execution [#11201]</span></span>

#### <a name="azaks"></a><span data-ttu-id="184db-1095">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="184db-1095">Az.Aks</span></span>
* <span data-ttu-id="184db-1096">이전에 사용하던 [AccessProfile API](/rest/api/aks/managedclusters/getaccessprofile)를 [ListClusterAdmin](/rest/api/aks/managedclusters/listclusteradmincredentials) 및 [ListClusterUser](/rest/api/aks/managedclusters/listclusterusercredentials) API 호출로 대체</span><span class="sxs-lookup"><span data-stu-id="184db-1096">Replaced usage of old [AccessProfile API](/rest/api/aks/managedclusters/getaccessprofile) with calls to [ListClusterAdmin](/rest/api/aks/managedclusters/listclusteradmincredentials) and [ListClusterUser](/rest/api/aks/managedclusters/listclusterusercredentials) APIs</span></span>

#### <a name="azbatch"></a><span data-ttu-id="184db-1097">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="184db-1097">Az.Batch</span></span>
* <span data-ttu-id="184db-1098">'Microsoft.Azure.Management.Batch' SDK 버전 11.0.0을 사용하도록 Az.Batch 업데이트</span><span class="sxs-lookup"><span data-stu-id="184db-1098">Updated Az.Batch to use 'Microsoft.Azure.Management.Batch' SDK version to 11.0.0</span></span>
* <span data-ttu-id="184db-1099">'New-AzBatchAccount' cmdlet에서 BatchAccount ID를 설정하는 기능 추가</span><span class="sxs-lookup"><span data-stu-id="184db-1099">Added the ability to set the BatchAccount Identity in the 'New-AzBatchAccount' cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="184db-1100">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="184db-1100">Az.CognitiveServices</span></span>
* <span data-ttu-id="184db-1101">계정 기능 표시 지원</span><span class="sxs-lookup"><span data-stu-id="184db-1101">Supported displaying account capabilities.</span></span>
* <span data-ttu-id="184db-1102">PublicNetworkAccess 수정 지원</span><span class="sxs-lookup"><span data-stu-id="184db-1102">Supported modifying PublicNetworkAccess.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="184db-1103">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="184db-1103">Az.Compute</span></span>
* <span data-ttu-id="184db-1104">Set-AzVM 및 Set-AzVmssVM cmdlet에 SimulateEviction 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="184db-1104">Added SimulateEviction parameter to Set-AzVM and Set-AzVmssVM cmdlets.</span></span>
* <span data-ttu-id="184db-1105">AzGalleryImageVersion cmdlet에 대한 StorageAccountType 매개 변수의 인수 완성자에 'Premium_LRS' 추가</span><span class="sxs-lookup"><span data-stu-id="184db-1105">Added 'Premium_LRS' to the argument completer of StorageAccountType parameter for New-AzGalleryImageVersion cmdlet.</span></span>
* <span data-ttu-id="184db-1106">VMCustomScriptExtension에 Substatuses 추가 [#11297]</span><span class="sxs-lookup"><span data-stu-id="184db-1106">Added Substatuses to VMCustomScriptExtension [#11297]</span></span>
* <span data-ttu-id="184db-1107">New-AzVM 및 New-AzVMConfig cmdlet에 대한 EvictionPolicy 매개 변수의 인수 완성자에 'Delete' 추가</span><span class="sxs-lookup"><span data-stu-id="184db-1107">Added 'Delete' to the argument completer of EvictionPolicy parameter for New-AzVM and New-AzVMConfig cmdlets.</span></span>
* <span data-ttu-id="184db-1108">새 SAP용 VM 확장의 이름 수정</span><span class="sxs-lookup"><span data-stu-id="184db-1108">Fixed name of new VM Extension for SAP</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="184db-1109">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="184db-1109">Az.DataFactory</span></span>
* <span data-ttu-id="184db-1110">ADF .Net SDK 버전을 4.9.0으로 업데이트</span><span class="sxs-lookup"><span data-stu-id="184db-1110">Updated ADF .Net SDK version to 4.9.0</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="184db-1111">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="184db-1111">Az.EventHub</span></span>
* <span data-ttu-id="184db-1112">'New-AzEventHubNamespace' 및 'Set-AzEventHubNamespace' cmdlet에 관리 ID 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="184db-1112">Added Managed Identity parameters to 'New-AzEventHubNamespace' and 'Set-AzEventHubNamespace' cmdlets</span></span>

#### <a name="azfunctions"></a><span data-ttu-id="184db-1113">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="184db-1113">Az.Functions</span></span>
* <span data-ttu-id="184db-1114">PowerShell 7.0 및 Java 11 함수 앱을 만드는 지원 추가</span><span class="sxs-lookup"><span data-stu-id="184db-1114">Added support to create PowerShell 7.0 and Java 11 function apps</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="184db-1115">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="184db-1115">Az.HDInsight</span></span>
* <span data-ttu-id="184db-1116">호스트를 나열하고 HDInsight 클러스터의 특정 호스트를 다시 시작하는 기능 지원</span><span class="sxs-lookup"><span data-stu-id="184db-1116">Supported listing hosts and restart specific hosts of the HDInsight cluster.</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="184db-1117">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="184db-1117">Az.HealthcareApis</span></span>
* <span data-ttu-id="184db-1118">SDK 버전을 1.1.0으로 업데이트</span><span class="sxs-lookup"><span data-stu-id="184db-1118">Updated the SDK version to 1.1.0</span></span>
* <span data-ttu-id="184db-1119">설정 및 관리 ID 내보내기에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="184db-1119">Added support for Export settings and Managed Identity</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="184db-1120">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="184db-1120">Az.Monitor</span></span>
* <span data-ttu-id="184db-1121">'Set-AzActivityLogAlert'에 대한 입력 개체 매개 변수 수정</span><span class="sxs-lookup"><span data-stu-id="184db-1121">Fixed input object parameter for 'Set-AzActivityLogAlert'</span></span>
* <span data-ttu-id="184db-1122">'Set-AzActionGroup'에 대한 'InputObject' 매개 변수 수정 [#10868]</span><span class="sxs-lookup"><span data-stu-id="184db-1122">Fixed 'InputObject' parameter for 'Set-AzActionGroup' [#10868]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="184db-1123">Az.Network</span><span class="sxs-lookup"><span data-stu-id="184db-1123">Az.Network</span></span>
* <span data-ttu-id="184db-1124">'Remove-AzExpressRouteCircuitConnectionConfig'에 AddressPrefixType 매개 변수 지원 추가</span><span class="sxs-lookup"><span data-stu-id="184db-1124">Added support for AddressPrefixType parameter to 'Remove-AzExpressRouteCircuitConnectionConfig'</span></span>
* <span data-ttu-id="184db-1125">Azure FirewallPolicy에 대한 새 cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="184db-1125">Added new cmdlets for Azure FirewallPolicy</span></span>
    - <span data-ttu-id="184db-1126">'New-AzFirewallPolicyDnsSetting'</span><span class="sxs-lookup"><span data-stu-id="184db-1126">'New-AzFirewallPolicyDnsSetting'</span></span>
    - <span data-ttu-id="184db-1127">방화벽 정책에 대한 네트워크 규칙에서 대상 FQDN 지원</span><span class="sxs-lookup"><span data-stu-id="184db-1127">Support for Destination FQDN in Network Rules for Firewall Policy</span></span>
* <span data-ttu-id="184db-1128">백 엔드 주소 풀 작업에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="184db-1128">Added support for backend address pool operations</span></span>
    - <span data-ttu-id="184db-1129">'New-AzLoadBalancerBackendAddressConfig'</span><span class="sxs-lookup"><span data-stu-id="184db-1129">'New-AzLoadBalancerBackendAddressConfig'</span></span>
    - <span data-ttu-id="184db-1130">'New-AzLoadBalancerBackendAddressPool'</span><span class="sxs-lookup"><span data-stu-id="184db-1130">'New-AzLoadBalancerBackendAddressPool'</span></span>
    - <span data-ttu-id="184db-1131">'Set-AzLoadBalancerBackendAddressPool'</span><span class="sxs-lookup"><span data-stu-id="184db-1131">'Set-AzLoadBalancerBackendAddressPool'</span></span>
    - <span data-ttu-id="184db-1132">'Remove-AzLoadBalancerBackendAddressPool'</span><span class="sxs-lookup"><span data-stu-id="184db-1132">'Remove-AzLoadBalancerBackendAddressPool'</span></span>
    - <span data-ttu-id="184db-1133">'Get-AzLoadBalancerBackendAddressPool'</span><span class="sxs-lookup"><span data-stu-id="184db-1133">'Get-AzLoadBalancerBackendAddressPool'</span></span>
* <span data-ttu-id="184db-1134">'New-AzIpGroup'에 대한 이름 유효성 검사 추가</span><span class="sxs-lookup"><span data-stu-id="184db-1134">Added name validation for 'New-AzIpGroup'</span></span>
* <span data-ttu-id="184db-1135">Azure FirewallPolicy에 대한 새 cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="184db-1135">Added new cmdlets for Azure FirewallPolicy</span></span>
    - <span data-ttu-id="184db-1136">'New-AzFirewallPolicyThreatIntelWhitelist'</span><span class="sxs-lookup"><span data-stu-id="184db-1136">'New-AzFirewallPolicyThreatIntelWhitelist'</span></span>
* <span data-ttu-id="184db-1137">기능에 대한 새로운 명령이 업데이트됨: VirtualWan P2SVpnGateway에서 사용자 지정 dns 서버 설정/제거</span><span class="sxs-lookup"><span data-stu-id="184db-1137">Updated below commands for feature: Custom dns servers set/remove on VirtualWan P2SVpnGateway.</span></span>
    - <span data-ttu-id="184db-1138">New-AzP2sVpnGateway 업데이트됨: 고객이 P2SVpnGateway에 설정할 dns 서버를 지정할 수 있는 선택적 매개 변수 '-CustomDnsServer'가 추가되었으며, 이 매개 변수는 지점 및 사이트 간 클라이언트에서 사용 가능</span><span class="sxs-lookup"><span data-stu-id="184db-1138">Updated New-AzP2sVpnGateway: Added optional parameter '-CustomDnsServer' for customers to specify their dns servers to set on P2SVpnGateway, which can be used by Point to site clients.</span></span>
    - <span data-ttu-id="184db-1139">Update-AzP2sVpnGateway 업데이트됨: 고객이 P2SVpnGateway에 설정할 dns 서버를 지정할 수 있는 선택적 매개 변수 '-CustomDnsServer'가 추가되었으며, 이 매개 변수는 지점 및 사이트 간 클라이언트에서 사용 가능</span><span class="sxs-lookup"><span data-stu-id="184db-1139">Updated Update-AzP2sVpnGateway: Added optional parameter '-CustomDnsServer' for customers to specify their dns servers to set on P2SVpnGateway, which can be used by Point to site clients.</span></span>
* <span data-ttu-id="184db-1140">'Update-AzVpnGateway' 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="184db-1140">Updated 'Update-AzVpnGateway'</span></span>
    - <span data-ttu-id="184db-1141">고객이 VpnGateway에 설정할 사용자 지정 bgps를 지정할 수 있도록 선택적 매개 변수 '-BgpPeeringAddress' 추가</span><span class="sxs-lookup"><span data-stu-id="184db-1141">Added optional parameter '-BgpPeeringAddress' for customers to specify their custom bgps to set on VpnGateway.</span></span>
* <span data-ttu-id="184db-1142">VirtualHub 리소스의 라우팅 상태 초기화를 지원하는 새 cmdlet 추가:</span><span class="sxs-lookup"><span data-stu-id="184db-1142">Added new cmdlet to support resetting the routing state of a VirtualHub resource:</span></span>
    - <span data-ttu-id="184db-1143">'Reset-AzHubRouter'</span><span class="sxs-lookup"><span data-stu-id="184db-1143">'Reset-AzHubRouter'</span></span>
* <span data-ttu-id="184db-1144">방화벽 정책에 대한 최근 Swagger 변화에 따라 아래 항목 업데이트</span><span class="sxs-lookup"><span data-stu-id="184db-1144">Updated below things based on recent swagger change for Firewall Policy</span></span>
    - <span data-ttu-id="184db-1145">RuleGroup, RuleCollectionGroup 및 RuleType의 이름 변경</span><span class="sxs-lookup"><span data-stu-id="184db-1145">Changes names for RuleGroup, RuleCollectionGroup and RuleType</span></span>
    - <span data-ttu-id="184db-1146">여러 NAT 규칙 컬렉션을 지원하도록 방화벽 정책 NAT 규칙 컬렉션에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="184db-1146">Added support for Firewall Policy NAT Rule Collections to support multiple NAT Rule Collection</span></span>
* <span data-ttu-id="184db-1147">[호환성이 손상되는 변경] 'New-AzFirewallPolicyApplicationRule' 및 'New-AzFirewallPolicyNetworkRule'에 대한 필수 매개 변수 'SourceIpGroup' 추가</span><span class="sxs-lookup"><span data-stu-id="184db-1147">[Breaking Change] Added mandatory parameter 'SourceIpGroup' for 'New-AzFirewallPolicyApplicationRule' and 'New-AzFirewallPolicyNetworkRule'.</span></span>
* <span data-ttu-id="184db-1148">[호환성이 손상되는 변경] 'New-AzFirewallPolicyApplicationRule' 수정, 'SourceAddress' 매개 변수를 필수로 변경</span><span class="sxs-lookup"><span data-stu-id="184db-1148">[Breaking Change] Fixed 'New-AzFirewallPolicyApplicationRule', parameter 'SourceAddress' to be mandatory.</span></span>
* <span data-ttu-id="184db-1149">[호환성이 손상되는 변경] 'New-AzFirewallPolicyApplicationRule' 수정, 'SourceAddress' 매개 변수를 필수로 변경</span><span class="sxs-lookup"><span data-stu-id="184db-1149">[Breaking Change] Fixed 'New-AzFirewallPolicyApplicationRule', parameter 'SourceAddress' to be mandatory.</span></span>
* <span data-ttu-id="184db-1150">[호환성이 손상되는 변경] 다음 필수 매개 변수 제거: 'New-AzFirewallPolicyNatRuleCollection'의 'TranslatedAddress', 'TranslatedPort'</span><span class="sxs-lookup"><span data-stu-id="184db-1150">[Breaking Change] Removed mandatory parameters: 'TranslatedAddress', 'TranslatedPort' for 'New-AzFirewallPolicyNatRuleCollection'.</span></span>
* <span data-ttu-id="184db-1151">PrivateLink On Application Gateway를 지원하는 새 cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="184db-1151">Added new cmdlets to support PrivateLink On Application Gateway</span></span>
    - <span data-ttu-id="184db-1152">'New-AzApplicationGatewayPrivateLinkConfiguration'</span><span class="sxs-lookup"><span data-stu-id="184db-1152">'New-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="184db-1153">'Get-AzApplicationGatewayPrivateLinkConfiguration'</span><span class="sxs-lookup"><span data-stu-id="184db-1153">'Get-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="184db-1154">'New-AzApplicationGatewayPrivateLinkConfiguration'</span><span class="sxs-lookup"><span data-stu-id="184db-1154">'New-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="184db-1155">'Set-AzApplicationGatewayPrivateLinkConfiguration'</span><span class="sxs-lookup"><span data-stu-id="184db-1155">'Set-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="184db-1156">'Remove-AzApplicationGatewayPrivateLinkConfiguration'</span><span class="sxs-lookup"><span data-stu-id="184db-1156">'Remove-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="184db-1157">'New-AzApplicationGatewayPrivateLinkIpConfiguration'</span><span class="sxs-lookup"><span data-stu-id="184db-1157">'New-AzApplicationGatewayPrivateLinkIpConfiguration'</span></span>
* <span data-ttu-id="184db-1158">VirtualHub의 HubRouteTables 자식 리소스에 대한 새 cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="184db-1158">Added new cmdlets for HubRouteTables child resource of VirtualHub.</span></span>
    - <span data-ttu-id="184db-1159">'New-AzVHubRoute'</span><span class="sxs-lookup"><span data-stu-id="184db-1159">'New-AzVHubRoute'</span></span>
    - <span data-ttu-id="184db-1160">'New-AzVHubRouteTable'</span><span class="sxs-lookup"><span data-stu-id="184db-1160">'New-AzVHubRouteTable'</span></span>
    - <span data-ttu-id="184db-1161">'Get-AzVHubRouteTable'</span><span class="sxs-lookup"><span data-stu-id="184db-1161">'Get-AzVHubRouteTable'</span></span>
    - <span data-ttu-id="184db-1162">'Update-AzVHubRouteTable'</span><span class="sxs-lookup"><span data-stu-id="184db-1162">'Update-AzVHubRouteTable'</span></span>
    - <span data-ttu-id="184db-1163">'Remove-AzVHubRouteTable'</span><span class="sxs-lookup"><span data-stu-id="184db-1163">'Remove-AzVHubRouteTable'</span></span>
* <span data-ttu-id="184db-1164">VirtualWan의 사용자 지정 라우팅에 대한 선택적 RoutingConfiguration 입력 매개 변수를 지원하도록 기존 cmdlet 업데이트</span><span class="sxs-lookup"><span data-stu-id="184db-1164">Updated existing cmdlets to support optional RoutingConfiguration input parameter for custom routing in VirtualWan.</span></span>
    - <span data-ttu-id="184db-1165">'New-AzExpressRouteConnection'</span><span class="sxs-lookup"><span data-stu-id="184db-1165">'New-AzExpressRouteConnection'</span></span>
    - <span data-ttu-id="184db-1166">'Set-AzExpressRouteConnection'</span><span class="sxs-lookup"><span data-stu-id="184db-1166">'Set-AzExpressRouteConnection'</span></span>
    - <span data-ttu-id="184db-1167">'New-AzVirtualHubVnetConnection'</span><span class="sxs-lookup"><span data-stu-id="184db-1167">'New-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="184db-1168">'Update-AzVirtualHubVnetConnection'</span><span class="sxs-lookup"><span data-stu-id="184db-1168">'Update-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="184db-1169">'New-AzVpnConnection'</span><span class="sxs-lookup"><span data-stu-id="184db-1169">'New-AzVpnConnection'</span></span>
    - <span data-ttu-id="184db-1170">'Update-AzVpnConnection'</span><span class="sxs-lookup"><span data-stu-id="184db-1170">'Update-AzVpnConnection'</span></span>
    - <span data-ttu-id="184db-1171">'New-AzP2sVpnGateway'</span><span class="sxs-lookup"><span data-stu-id="184db-1171">'New-AzP2sVpnGateway'</span></span>
    - <span data-ttu-id="184db-1172">'Update-AzP2sVpnGateway'</span><span class="sxs-lookup"><span data-stu-id="184db-1172">'Update-AzP2sVpnGateway'</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="184db-1173">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="184db-1173">Az.OperationalInsights</span></span>
* <span data-ttu-id="184db-1174">PSWorkspace가 IOperationalInsightsWorkspace를 구현하지 않는 버그 수정 [#12135]</span><span class="sxs-lookup"><span data-stu-id="184db-1174">Fixed bug PSWorkspace doesn't implement IOperationalInsightsWorkspace [#12135]</span></span>
* <span data-ttu-id="184db-1175">'Set-AzOperationalInsightsWorkspace'에서 'Sku' 매개 변수의 올바른 값 세트에 'pergb2018' 추가</span><span class="sxs-lookup"><span data-stu-id="184db-1175">Added 'pergb2018' to valid value set of parameter 'Sku' in 'Set-AzOperationalInsightsWorkspace'</span></span> 
* <span data-ttu-id="184db-1176">매개 변수 'FunctionParameter'에 대한 별칭 'FunctionParameters' 추가</span><span class="sxs-lookup"><span data-stu-id="184db-1176">Added alias 'FunctionParameters' for parameter 'FunctionParameter' to</span></span>
    - <span data-ttu-id="184db-1177">'New-AzOperationalInsightsSavedSearch'</span><span class="sxs-lookup"><span data-stu-id="184db-1177">'New-AzOperationalInsightsSavedSearch'</span></span>
    - <span data-ttu-id="184db-1178">'Set-AzOperationalInsightsSavedSearch'</span><span class="sxs-lookup"><span data-stu-id="184db-1178">'Set-AzOperationalInsightsSavedSearch'</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="184db-1179">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="184db-1179">Az.RecoveryServices</span></span>
* <span data-ttu-id="184db-1180">Azure Backup에서 MAB 항목을 가져오기 위한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="184db-1180">Azure Backup added support for fetching MAB items.</span></span>
* <span data-ttu-id="184db-1181">Azure Site Recovery에서 'StandardSSD_LRS' 디스크 형식 지원</span><span class="sxs-lookup"><span data-stu-id="184db-1181">Azure Site Recovery supports disk type 'StandardSSD_LRS'</span></span>

#### <a name="azresources"></a><span data-ttu-id="184db-1182">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="184db-1182">Az.Resources</span></span>
* <span data-ttu-id="184db-1183">'PSADUser'에서 'UsageLocation', 'GivenName', 'Surname', 'AccountEnabled', 'MailNickname', 'Mail' 추가 [#10526] [#10497]</span><span class="sxs-lookup"><span data-stu-id="184db-1183">Added 'UsageLocation', 'GivenName', 'Surname', 'AccountEnabled', 'MailNickname', 'Mail' on 'PSADUser' [#10526] [#10497]</span></span>
* <span data-ttu-id="184db-1184">'Get-AzADUser'에서 '-Mail'이 작동하지 않는 문제 해결 [#11981]</span><span class="sxs-lookup"><span data-stu-id="184db-1184">Fixed issue that '-Mail' doesn't work on 'Get-AzADUser' [#11981]</span></span>
* <span data-ttu-id="184db-1185">'Get-AzDeploymentWhatIfResult' 및 'Get-AzResourceGroupDeploymentWhatIfResult'에 '-ExcludeChangeType' 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="184db-1185">Added '-ExcludeChangeType' parameter to 'Get-AzDeploymentWhatIfResult' and 'Get-AzResourceGroupDeploymentWhatIfResult'</span></span>
* <span data-ttu-id="184db-1186">'New-AzDeployment' 및 'New-AzResourceGroupDeployment'에 '-WhatIfExcludeChangeType' 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="184db-1186">Added '-WhatIfExcludeChangeType' parameter to 'New-AzDeployment' and 'New-AzResourceGroupDeployment'</span></span>
* <span data-ttu-id="184db-1187">보다 나은 오류 메시지를 표시하도록 'Test-Az\*Deployment' cmdlet 업데이트</span><span class="sxs-lookup"><span data-stu-id="184db-1187">Updated 'Test-Az\*Deployment' cmdlets to show better error messages</span></span>
* <span data-ttu-id="184db-1188">deployment create 및 What-If cmdlet의 '-Name' 매개 변수에 대한 도움말 메시지 수정</span><span class="sxs-lookup"><span data-stu-id="184db-1188">Fixed help message for '-Name' parameter of deployment create and What-If cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="184db-1189">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="184db-1189">Az.Sql</span></span>
* <span data-ttu-id="184db-1190">Set SQL Server Azure Active Directory Admin cmdlet의 서비스 주체에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="184db-1190">Added support for service principal for Set SQL Server Azure Active Directory Admin cmdlet</span></span>
* <span data-ttu-id="184db-1191">데이터 분류 cmdlet의 동기화 문제 해결</span><span class="sxs-lookup"><span data-stu-id="184db-1191">Fixed sync issue in Data Classification cmdlets.</span></span>
* <span data-ttu-id="184db-1192">'Set-AzSqlServerActiveDirectoryAdministrator'에서 메일로 사용자 검색 지원 [#12192]</span><span class="sxs-lookup"><span data-stu-id="184db-1192">Supported searching user by mail on 'Set-AzSqlServerActiveDirectoryAdministrator' [#12192]</span></span>

#### <a name="azstorage"></a><span data-ttu-id="184db-1193">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="184db-1193">Az.Storage</span></span>
* <span data-ttu-id="184db-1194">RequireInfrastructureEncryption을 사용하여 스토리지 계정 만들기 지원</span><span class="sxs-lookup"><span data-stu-id="184db-1194">Supported create Storage account with RequireInfrastructureEncryption</span></span>
    -  <span data-ttu-id="184db-1195">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="184db-1195">'New-AzStorageAccount'</span></span>
* <span data-ttu-id="184db-1196">Azure.Core 로딩 논리를 Az.Accounts로 이동</span><span class="sxs-lookup"><span data-stu-id="184db-1196">Moved the logic of loading Azure.Core to Az.Accounts</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="184db-1197">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="184db-1197">Az.Websites</span></span>
* <span data-ttu-id="184db-1198">'Restore-AzDeletedWebApp'에서 복원이 실패할 경우 생성된 웹앱을 삭제하는 보호 기능 추가</span><span class="sxs-lookup"><span data-stu-id="184db-1198">Added safeguard to delete created webapp if restore failed in 'Restore-AzDeletedWebApp'</span></span>
* <span data-ttu-id="184db-1199">'New-AzWebApp' 및 'New-AzWebAppSlot'에 대한 'SourceWebApp.Location' 추가</span><span class="sxs-lookup"><span data-stu-id="184db-1199">Added 'SourceWebApp.Location' for 'New-AzWebApp' and 'New-AzWebAppSlot'</span></span>
* <span data-ttu-id="184db-1200">'Set-AzWebApp' 및 'Set-AzWebAppSlot'에서 컨테이너 설정을 변경할 수 없는 버그 수정</span><span class="sxs-lookup"><span data-stu-id="184db-1200">Fixed bug that prevented changing Container settings in 'Set-AzWebApp' and 'Set-AzWebAppSlot'</span></span>
* <span data-ttu-id="184db-1201">Get-AzWebApp에 대한 -Name을 제공하지 않으면 SiteConfig를 가져오는 버그 수정</span><span class="sxs-lookup"><span data-stu-id="184db-1201">Fixed bug to get SiteConfig when -Name is not given for Get-AzWebApp</span></span>
* <span data-ttu-id="184db-1202">Linux 앱용 ASP를 만드는 지원 추가</span><span class="sxs-lookup"><span data-stu-id="184db-1202">Added a support to create ASP for Linux Apps</span></span>
* <span data-ttu-id="184db-1203">리소스 그룹 간 복제에 대한 예외 추가</span><span class="sxs-lookup"><span data-stu-id="184db-1203">Added exceptions for clone across resource groups</span></span>

## <a name="420---june-2020"></a><span data-ttu-id="184db-1204">4.2.0 - 2020년 6월</span><span class="sxs-lookup"><span data-stu-id="184db-1204">4.2.0 - June 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="184db-1205">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="184db-1205">Az.Accounts</span></span>
* <span data-ttu-id="184db-1206">Azure Automation 또는 PowerShell 작업에서 Az가 로그를 건너뛸 수 있는 문제 수정[#11492]</span><span class="sxs-lookup"><span data-stu-id="184db-1206">Fixed an issue that may cause Az to skip logs in Azure Automation or PowerShell jobs [#11492]</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="184db-1207">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="184db-1207">Az.AnalysisServices</span></span>
* <span data-ttu-id="184db-1208">데이터 평면 cmdlet의 어셈블리 버전 업데이트</span><span class="sxs-lookup"><span data-stu-id="184db-1208">Updated assembly version of data plane cmdlets</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="184db-1209">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="184db-1209">Az.ApiManagement</span></span>
* <span data-ttu-id="184db-1210">서비스 관리 cmdlet의 어셈블리 버전 업데이트</span><span class="sxs-lookup"><span data-stu-id="184db-1210">Updated assembly version of service management cmdlets</span></span>

#### <a name="azbilling"></a><span data-ttu-id="184db-1211">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="184db-1211">Az.Billing</span></span>
* <span data-ttu-id="184db-1212">소비 cmdlet의 어셈블리 버전 업데이트</span><span class="sxs-lookup"><span data-stu-id="184db-1212">Updated assembly version of consumption cmdlets</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="184db-1213">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="184db-1213">Az.CognitiveServices</span></span>
* <span data-ttu-id="184db-1214">PrivateEndpoint 및 PublicNetworkAccess control을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="184db-1214">Support PrivateEndpoint and PublicNetworkAccess control.</span></span> 

#### <a name="azdatafactory"></a><span data-ttu-id="184db-1215">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="184db-1215">Az.DataFactory</span></span>
* <span data-ttu-id="184db-1216">데이터 팩터리 V2 cmdlet의 어셈블리 버전 업데이트</span><span class="sxs-lookup"><span data-stu-id="184db-1216">Updated assembly version of data factory V2 cmdlets</span></span>

#### <a name="azdatashare"></a><span data-ttu-id="184db-1217">Az.DataShare</span><span class="sxs-lookup"><span data-stu-id="184db-1217">Az.DataShare</span></span>
* <span data-ttu-id="184db-1218">''Az.DataShare'' 모듈의 일반 공급</span><span class="sxs-lookup"><span data-stu-id="184db-1218">General availability of ''Az.DataShare'' module</span></span>

#### <a name="azdesktopvirtualization"></a><span data-ttu-id="184db-1219">Az.DesktopVirtualization</span><span class="sxs-lookup"><span data-stu-id="184db-1219">Az.DesktopVirtualization</span></span>
* <span data-ttu-id="184db-1220">''Az.DesktopVirtualization'' 모듈의 일반 공급</span><span class="sxs-lookup"><span data-stu-id="184db-1220">General availability of ''Az.DesktopVirtualization'' module</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="184db-1221">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="184db-1221">Az.OperationalInsights</span></span>
* <span data-ttu-id="184db-1222">SDK를 0.21.0으로 업그레이드</span><span class="sxs-lookup"><span data-stu-id="184db-1222">Upgraded SDK to 0.21.0</span></span>
* <span data-ttu-id="184db-1223">다음에 선택적 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="184db-1223">Added optional parameters to</span></span> 
    - <span data-ttu-id="184db-1224">'New-AzOperationalInsightsSavedSearch'</span><span class="sxs-lookup"><span data-stu-id="184db-1224">'New-AzOperationalInsightsSavedSearch'</span></span>
    - <span data-ttu-id="184db-1225">'Set-AzOperationalInsightsSavedSearch'</span><span class="sxs-lookup"><span data-stu-id="184db-1225">'Set-AzOperationalInsightsSavedSearch'</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="184db-1226">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="184db-1226">Az.PolicyInsights</span></span>
* <span data-ttu-id="184db-1227">'Start-AzPolicyComplianceScan'의 예제 3 수정</span><span class="sxs-lookup"><span data-stu-id="184db-1227">Corrected example 3 for 'Start-AzPolicyComplianceScan'</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="184db-1228">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="184db-1228">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="184db-1229">PowerBI cmdlet의 어셈블리 버전 업데이트</span><span class="sxs-lookup"><span data-stu-id="184db-1229">Updated assembly version of PowerBI cmdlets</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="184db-1230">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="184db-1230">Az.PrivateDns</span></span>
* <span data-ttu-id="184db-1231">Remove-AzPrivateDnsRecordSet에 대한 자세한 정보 출력 문자열 형식 수정</span><span class="sxs-lookup"><span data-stu-id="184db-1231">Corrected verbose output string formatting for Remove-AzPrivateDnsRecordSet</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="184db-1232">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="184db-1232">Az.RecoveryServices</span></span>
* <span data-ttu-id="184db-1233">xml 입력에서 영역 간 복제를 위한 복구 계획을 세우기 위한 Azure Site Recovery 지원.</span><span class="sxs-lookup"><span data-stu-id="184db-1233">Azure Site Recovery support for creating recovery plan for zone to zone replication from xml input.</span></span>
* <span data-ttu-id="184db-1234">SiteRecovery 및 Backup cmdlet의 어셈블리 버전 업데이트</span><span class="sxs-lookup"><span data-stu-id="184db-1234">Updated assembly version of SiteRecovery and Backup cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="184db-1235">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="184db-1235">Az.Resources</span></span>
* <span data-ttu-id="184db-1236">Get-AzDeploymentScriptLog 및 Save-AzDeploymentScriptLog cmdlet에 Tail 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="184db-1236">Added Tail parameter to Get-AzDeploymentScriptLog and Save-AzDeploymentScriptLog cmdlets</span></span>
* <span data-ttu-id="184db-1237">형식이 지정된 출력 속성을 Get-AzDeploymentScript cmdlet 출력에 표시</span><span class="sxs-lookup"><span data-stu-id="184db-1237">Formatted Output property and show it on the Get-AzDeploymentScript cmdlet output</span></span>
* <span data-ttu-id="184db-1238">-DeploymentScriptInputObject 매개 변수의 이름이 -DeploymentScriptObject로 변경</span><span class="sxs-lookup"><span data-stu-id="184db-1238">Renamed -DeploymentScriptInputObject parameter to -DeploymentScriptObject</span></span>
* <span data-ttu-id="184db-1239">cmdlet 메시지에서 누락된 파일/대상 이름이 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-1239">Fixed missing file/target name in cmdlet messages.</span></span>
* <span data-ttu-id="184db-1240">리소스 관리자 및 태그 cmdlet의 어셈블리 버전 업데이트</span><span class="sxs-lookup"><span data-stu-id="184db-1240">Updated assembly version of resource manager and tags cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="184db-1241">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="184db-1241">Az.Sql</span></span>
* <span data-ttu-id="184db-1242">UsePrivateLinkConnection을 'New-AzSqlSyncGroup', 'Update-AzSqlSyncGroup', 'New-AzSqlSyncMember' 및 'Update-AzSqlSyncMember'에 추가</span><span class="sxs-lookup"><span data-stu-id="184db-1242">Added UsePrivateLinkConnection to 'New-AzSqlSyncGroup', 'Update-AzSqlSyncGroup', 'New-AzSqlSyncMember' and 'Update-AzSqlSyncMember'</span></span>
* <span data-ttu-id="184db-1243">SyncMemberAzureDatabaseResourceId를 'New-AzSqlSyncMember' 및 'Update-AzSqlSyncMember'에 추가</span><span class="sxs-lookup"><span data-stu-id="184db-1243">Added SyncMemberAzureDatabaseResourceId to 'New-AzSqlSyncMember' and 'Update-AzSqlSyncMember'</span></span>
* <span data-ttu-id="184db-1244">SQL Server Azure Active Directory Admin cmdlet을 설정하는 게스트 사용자 조회 지원 추가</span><span class="sxs-lookup"><span data-stu-id="184db-1244">Added Guest user lookup support to Set SQL Server Azure Active Directory Admin cmdlet</span></span>

#### <a name="azstorage"></a><span data-ttu-id="184db-1245">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="184db-1245">Az.Storage</span></span>
* <span data-ttu-id="184db-1246">데이터 평면 cmdlet의 어셈블리 버전 업데이트</span><span class="sxs-lookup"><span data-stu-id="184db-1246">Updated assembly version of data plane cmdlets</span></span>

## <a name="410---may-2020"></a><span data-ttu-id="184db-1247">4.1.0 - 2020년 5월</span><span class="sxs-lookup"><span data-stu-id="184db-1247">4.1.0 - May 2020</span></span>
### <a name="highlights-since-the-last-release"></a><span data-ttu-id="184db-1248">마지막 릴리스 이후의 주요 사항</span><span class="sxs-lookup"><span data-stu-id="184db-1248">Highlights since the last release</span></span>
* <span data-ttu-id="184db-1249">지원되는 PowerShell 버전: Windows PowerShell 5.1, PowerShell Core 6.2.4 이상, PowerShell 7</span><span class="sxs-lookup"><span data-stu-id="184db-1249">Supported PowerShell versions: Windows PowerShell 5.1, PowerShell Core 6.2.4+, PowerShell 7</span></span>
* <span data-ttu-id="184db-1250">Az.Functions 일반 공급</span><span class="sxs-lookup"><span data-stu-id="184db-1250">General availability of Az.Functions</span></span> 
* <span data-ttu-id="184db-1251">Az.ApiManagement, Az.Batch, Az.Compute, Az.KeyVault, Az.Monitor, Az.Network, Az.OperationalInsights, Az.Resources 및 Az.Storage의 주요 릴리스 출시</span><span class="sxs-lookup"><span data-stu-id="184db-1251">Az.ApiManagement, Az.Batch, Az.Compute, Az.KeyVault, Az.Monitor, Az.Network, Az.OperationalInsights, Az.Resources, and Az.Storage have major release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="184db-1252">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="184db-1252">Az.Accounts</span></span>
* <span data-ttu-id="184db-1253">'AzureSynapseAnalyticsEndpointResourceId' 및 'AzureSynapseAnalyticsEndpointSuffix' 매개 변수를 허용하도록 'Add-AzEnvironment' 및 'Set-AzEnvironment' 업데이트</span><span class="sxs-lookup"><span data-stu-id="184db-1253">Updated 'Add-AzEnvironment' and 'Set-AzEnvironment' to accept parameters 'AzureSynapseAnalyticsEndpointResourceId' and 'AzureSynapseAnalyticsEndpointSuffix'</span></span>
* <span data-ttu-id="184db-1254">Az.Accounts에 Azure.Core 관련 어셈블리가 추가되었으며 지원되는 PowerShell 플랫폼은 Windows PowerShell 5.1, PowerShell Core 6.2.4, PowerShell 7+입니다.</span><span class="sxs-lookup"><span data-stu-id="184db-1254">Added Azure.Core related assemblies into Az.Accounts, supported PowerShell platforms include Windows PowerShell 5.1, PowerShell Core 6.2.4, PowerShell 7+</span></span>

#### <a name="azaks"></a><span data-ttu-id="184db-1255">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="184db-1255">Az.Aks</span></span>
* <span data-ttu-id="184db-1256">API 버전을 2019-10-01로 업그레이드</span><span class="sxs-lookup"><span data-stu-id="184db-1256">Upgraded API Version to 2019-10-01</span></span>
* <span data-ttu-id="184db-1257">Windows 컨테이너를 사용하여 AKS 만들기 지원</span><span class="sxs-lookup"><span data-stu-id="184db-1257">Supported to create AKS using Windows container</span></span>
* <span data-ttu-id="184db-1258">새 cmdlet 추가: 'New-AzAksNodePool', 'Update-AzAksNodePool', 'Remove-AzAksNodePool', 'Get-AzAksNodePool', 'Install-AzAksKubectl', 'Get-AzAksVersion'</span><span class="sxs-lookup"><span data-stu-id="184db-1258">Provided new cmdlets: 'New-AzAksNodePool', 'Update-AzAksNodePool', 'Remove-AzAksNodePool',        'Get-AzAksNodePool', 'Install-AzAksKubectl', 'Get-AzAksVersion'</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="184db-1259">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="184db-1259">Az.ApiManagement</span></span>
* <span data-ttu-id="184db-1260">'New-AzApiManagement' 및 'Set-AzApiManagement': [-AssignIdentity] 매개 변수 이름을 [-SystemAssignedIdentity]로 변경</span><span class="sxs-lookup"><span data-stu-id="184db-1260">'New-AzApiManagement' and 'Set-AzApiManagement': [-AssignIdentity] parameter renamed as [-SystemAssignedIdentity]</span></span>
* <span data-ttu-id="184db-1261">'New-AzApiManagement' 및 'Set-AzApiManagement': 새 매개 변수 추가: [-UserAssignedIdentity <String[]>]</span><span class="sxs-lookup"><span data-stu-id="184db-1261">'New-AzApiManagement' and 'Set-AzApiManagement': New parameter added: [-UserAssignedIdentity <String[]>]</span></span>
* <span data-ttu-id="184db-1262">'Get-AzApiManagementProperty': 'Get-AzApiManagementNamedValue'로 이름 변경.</span><span class="sxs-lookup"><span data-stu-id="184db-1262">'Get-AzApiManagementProperty': renamed as 'Get-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="184db-1263">PropertyId 매개 변수 이름을 NamedValueId로 변경.</span><span class="sxs-lookup"><span data-stu-id="184db-1263">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="184db-1264">'New-AzApiManagementProperty': 'New-AzApiManagementNamedValue'로 이름 변경.</span><span class="sxs-lookup"><span data-stu-id="184db-1264">'New-AzApiManagementProperty': renamed as 'New-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="184db-1265">PropertyId 매개 변수 이름을 NamedValueId로 변경.</span><span class="sxs-lookup"><span data-stu-id="184db-1265">PropertyId parameter renamed as NamedValueId.</span></span> 
* <span data-ttu-id="184db-1266">'Set-AzApiManagementProperty': 'Set-AzApiManagementNamedValue'로 이름 변경.</span><span class="sxs-lookup"><span data-stu-id="184db-1266">'Set-AzApiManagementProperty': renamed as 'Set-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="184db-1267">PropertyId 매개 변수 이름을 NamedValueId로 변경.</span><span class="sxs-lookup"><span data-stu-id="184db-1267">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="184db-1268">'Remove-AzApiManagementProperty': 'Remove-AzApiManagementNamedValue'로 이름 변경.</span><span class="sxs-lookup"><span data-stu-id="184db-1268">'Remove-AzApiManagementProperty': renamed as 'Remove-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="184db-1269">PropertyId 매개 변수 이름을 NamedValueId로 변경.</span><span class="sxs-lookup"><span data-stu-id="184db-1269">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="184db-1270">새 'Get-AzApiManagementAuthorizationServerClientSecret' cmdlet이 추가되었으며 'Get-AzApiManagementAuthorizationServer'는 더 이상 클라이언트 암호를 반환하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-1270">Added new 'Get-AzApiManagementAuthorizationServerClientSecret' cmdlet and 'Get-AzApiManagementAuthorizationServer' will not return client secret anymore.</span></span>
* <span data-ttu-id="184db-1271">새 'Get-AzApiManagementNamedValueSecretValue' cmdlet이 추가되었으며 'Get-AzApiManagementNamedValue'는 더 이상 비밀 값을 반환하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-1271">Added new 'Get-AzApiManagementNamedValueSecretValue' cmdlet and 'Get-AzApiManagementNamedValue' will not return secret value.</span></span>
* <span data-ttu-id="184db-1272">새 'Get-AzApiManagementOpenIdConnectProviderClientSecret' cmdlet이 추가되었으며 'Get-AzApiManagementOpenIdConnectProvider'는 더 이상 클라이언트 암호를 반환하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-1272">Added new 'Get-AzApiManagementOpenIdConnectProviderClientSecret' cmdlet and 'Get-AzApiManagementOpenIdConnectProvider' will not return client secret anymore.</span></span>
* <span data-ttu-id="184db-1273">새 'Get-AzApiManagementSubscriptionKey' cmdlet이 추가되었으며 'Get-AzApiManagementSubscription'은 더 이상 구독 키를 반환하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-1273">Added new 'Get-AzApiManagementSubscriptionKey' cmdlet and 'Get-AzApiManagementSubscription' will not return subscription keys anymore.</span></span>
* <span data-ttu-id="184db-1274">새 'Get-AzApiManagementTenantAccessSecret' cmdlet이 추가되었으며 'Get-AzApiManagementTenantAccess'는 더 이상 키를 반환하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-1274">Added new 'Get-AzApiManagementTenantAccessSecret' cmdlet and 'Get-AzApiManagementTenantAccess' will not return keys anymore.</span></span>
* <span data-ttu-id="184db-1275">새 'Get-AzApiManagementTenantGitAccessSecret' cmdlet이 추가되었으며 'Get-AzApiManagementTenantGitAccess'는 더 이상 키를 반환하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-1275">Added new 'Get-AzApiManagementTenantGitAccessSecret' cmdlet and 'Get-AzApiManagementTenantGitAccess' will not return keys anymore.</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="184db-1276">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="184db-1276">Az.ApplicationInsights</span></span>
* <span data-ttu-id="184db-1277">매개 변수 추가: 'New-AzApplicationInsights'에 대한 'RetentionInDays' 'PublicNetworkAccessForIngestion' 'PublicNetworkAccessForQuery'</span><span class="sxs-lookup"><span data-stu-id="184db-1277">Added Parameters: 'RetentionInDays' 'PublicNetworkAccessForIngestion' 'PublicNetworkAccessForQuery' for 'New-AzApplicationInsights'</span></span>
* <span data-ttu-id="184db-1278">'Update-AzApplicationInsights' cmdlet 작성</span><span class="sxs-lookup"><span data-stu-id="184db-1278">Created cmdlet 'Update-AzApplicationInsights'</span></span>
* <span data-ttu-id="184db-1279">연결된 스토리지 계정에 대한 cmdlet 작성</span><span class="sxs-lookup"><span data-stu-id="184db-1279">Created cmdlets for Linked Storage Account</span></span>

#### <a name="azbatch"></a><span data-ttu-id="184db-1280">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="184db-1280">Az.Batch</span></span>
* <span data-ttu-id="184db-1281">'Microsoft.Azure.Batch' SDK 버전 13.0.0 및 'Microsoft.Azure.Management.Batch' SDK 버전 9.0.0을 사용하도록 Az.Batch가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-1281">Updated Az.Batch to use 'Microsoft.Azure.Batch' SDK version 13.0.0 and 'Microsoft.Azure.Management.Batch' SDK version 9.0.0.</span></span>
* <span data-ttu-id="184db-1282">새 '-CertificateKind' 매개 변수를 사용하여 'AzBatchCertificate'에 추가할 인증서 종류를 선택하는 기능이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-1282">Added the ability to select the kind of certificate being added using the new '-CertificateKind' parameter to 'New-AzBatchCertificate'.</span></span>
* <span data-ttu-id="184db-1283">이전에 항상 ''였던 'ApplicationPackages' 속성이 'PSApplication'에서 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-1283">Removed 'ApplicationPackages' property from 'PSApplication' which was previously always ''.</span></span>
  - <span data-ttu-id="184db-1284">이제 'Get-AzBatchApplicationPackage'를 사용하여 애플리케이션 내부의 특정 패키지를 검색할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-1284">The specific packages inside of an application now can be retrieved using 'Get-AzBatchApplicationPackage'.</span></span> <span data-ttu-id="184db-1285">예를 들면 다음과 같습니다. 'Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication'.</span><span class="sxs-lookup"><span data-stu-id="184db-1285">For example: 'Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication'.</span></span>
* <span data-ttu-id="184db-1286">'New-AzBatchPool'을 사용하여 풀을 만들 때 'PSImageReference'의 'VirtualMachineImageId' 속성은 이제 Shared Image Gallery 이미지만 참조할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-1286">When creating a pool using 'New-AzBatchPool', the 'VirtualMachineImageId' property of 'PSImageReference' can now only refer to a Shared Image Gallery image.</span></span>
* <span data-ttu-id="184db-1287">'New-AzBatchPool'을 사용하여 풀을 만들 때 공용 IP 없이 'PSNetworkConfiguration'의 새 'PublicIPAddressConfiguration'을 사용하여 풀을 프로비저닝할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-1287">When creating a pool using 'New-AzBatchPool', the pool can be provisioned without a public IP using the new 'PublicIPAddressConfiguration' property of 'PSNetworkConfiguration'.</span></span>
  - <span data-ttu-id="184db-1288">'PSNetworkConfiguration'의 'PublicIPs' 속성도 'PSPublicIPAddressConfiguration'으로 이동되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-1288">The 'PublicIPs' property of 'PSNetworkConfiguration' has moved in to 'PSPublicIPAddressConfiguration' as well.</span></span> <span data-ttu-id="184db-1289">이 속성은 'IPAddressProvisioningType'이 'UserManaged'인 경우에만 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-1289">This property can only be specified if 'IPAddressProvisioningType' is 'UserManaged'.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="184db-1290">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="184db-1290">Az.Compute</span></span>
* <span data-ttu-id="184db-1291">'Update-AzVM' cmdlet에 HostId 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="184db-1291">Added HostId parameter to 'Update-AzVM' cmdlet</span></span>
* <span data-ttu-id="184db-1292">'New-AzVMConfig', 'New-AzVmssConfig', 'Update-AzVmss', 'Set-AzVMOperatingSystem' 및 'Set-AzVmssOsProfile' cmdlet의 도움말 문서가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-1292">Updated Help documents for 'New-AzVMConfig', 'New-AzVmssConfig', 'Update-AzVmss', 'Set-AzVMOperatingSystem' and 'Set-AzVmssOsProfile' cmdlets.</span></span>
* <span data-ttu-id="184db-1293">주요 변경 내용</span><span class="sxs-lookup"><span data-stu-id="184db-1293">Breaking changes</span></span>
    - <span data-ttu-id="184db-1294">'Get-AzVMImage' cmdlet에서 FilterExpression 매개 변수가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-1294">FilterExpression parameter is removed from 'Get-AzVMImage' cmdlet.</span></span>
    - <span data-ttu-id="184db-1295">'New-AzVmssConfig', 'New-AzVMConfig' 및 'Update-AzVM' cmdlet에서 AssignIdentity 매개 변수가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-1295">AssignIdentity parameter is removed from 'New-AzVmssConfig', 'New-AzVMConfig' and 'Update-AzVM' cmdlets.</span></span>
    - <span data-ttu-id="184db-1296">'New-AzVmssConfig' 및 'Update-AzVmss' cmdlet에서 AutomaticRepairMaxInstanceRepairsPercent가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-1296">AutomaticRepairMaxInstanceRepairsPercent is removed from 'New-AzVmssConfig' and 'Update-AzVmss' cmdlets.</span></span>
    - <span data-ttu-id="184db-1297">ProximityPlacementGroup에서 AvailabilitySetsColocationStatus, VirtualMachinesColocationStatus 및 VirtualMachineScaleSetsColocationStatus 속성이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-1297">AvailabilitySetsColocationStatus, VirtualMachinesColocationStatus and VirtualMachineScaleSetsColocationStatus properties are removed from ProximityPlacementGroup.</span></span>
    - <span data-ttu-id="184db-1298">AutomaticRepairsPolicy에서 MaxInstanceRepairsPercent 속성이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-1298">MaxInstanceRepairsPercent property is removed from AutomaticRepairsPolicy.</span></span>
    - <span data-ttu-id="184db-1299">AvailabilitySets, VirtualMachines 및 VirtualMachineScaleSets 형식이 IList<SubResource>에서 IList<SubResourceWithColocationStatus>로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-1299">The types of AvailabilitySets, VirtualMachines and VirtualMachineScaleSets are changed from IList<SubResource> to IList<SubResourceWithColocationStatus>.</span></span>
* <span data-ttu-id="184db-1300">'Get-AzVM' cmdlet에 대한 설명이 보다 정확하게 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-1300">Description for 'Get-AzVM' cmdlet has been updated to better describe it.</span></span> 

#### <a name="azdatafactory"></a><span data-ttu-id="184db-1301">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="184db-1301">Az.DataFactory</span></span>
* <span data-ttu-id="184db-1302">Managed IR에서 데이터 흐름 런타임 속성의 CRUD를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="184db-1302">Supported CRUD of data flow runtime properties in Managed IR.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="184db-1303">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="184db-1303">Az.FrontDoor</span></span>
* <span data-ttu-id="184db-1304">Front Door 규칙 엔진 개체를 생성, 업데이트, 검색 및 삭제할 수 있는 새 cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="184db-1304">Added new cmdlets for creation, update, retreival, and deletion of Front Door Rules Engine object</span></span>
* <span data-ttu-id="184db-1305">Front Door 규칙 엔진 개체를 작성할 수 있는 도우미 cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="184db-1305">Added helper cmdlets for construction of Front Door Rules Engine object</span></span>
* <span data-ttu-id="184db-1306">Front Door 회람 규칙 개체에 대한 규칙 엔진 참조 추가</span><span class="sxs-lookup"><span data-stu-id="184db-1306">Added Rules Engine reference to Front Door Routing Rule object.</span></span>
* <span data-ttu-id="184db-1307">Front Door 백 엔드 개체에 Private Link 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="184db-1307">Added Private Link parameters to Front Door Backend object</span></span>

#### <a name="azfunctions"></a><span data-ttu-id="184db-1308">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="184db-1308">Az.Functions</span></span>
* <span data-ttu-id="184db-1309">''Az.Functions'' 모듈의 일반 공급</span><span class="sxs-lookup"><span data-stu-id="184db-1309">General availability of ''Az.Functions'' module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="184db-1310">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="184db-1310">Az.HDInsight</span></span>
* <span data-ttu-id="184db-1311">고객 관리형 키 디스크 암호화 지원</span><span class="sxs-lookup"><span data-stu-id="184db-1311">Supported Customer-managed key disk encryption.</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="184db-1312">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="184db-1312">Az.HealthcareApis</span></span>
* <span data-ttu-id="184db-1313">더 이상 액세스 정책이 기본적으로 현재 보안 주체로 설정되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-1313">Access policies are no longer defaulted to the current principal</span></span>

#### <a name="aziothub"></a><span data-ttu-id="184db-1314">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="184db-1314">Az.IotHub</span></span>
* <span data-ttu-id="184db-1315">SQL과 비슷한 언어를 사용하여 정보를 검색하기 위해 IoT 허브에서 쿼리를 호출하는 cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-1315">Added cmdlet to invoke a query in an IoT hub to retrieve information using a SQL-like language.</span></span>
* <span data-ttu-id="184db-1316">'Add-AzIotHubDevice'가 자식 디바이스 없는 에지 지원 디바이스를 만들 수 없는 문제 해결 [#11597]</span><span class="sxs-lookup"><span data-stu-id="184db-1316">Fix issue that 'Add-AzIotHubDevice' fails to create Edge Enabled Device without child devices [#11597]</span></span>
* <span data-ttu-id="184db-1317">IoT Hub, 디바이스 또는 모듈에 대한 SAS 토큰을 생성하는 cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-1317">Added cmdlet to generate SAS token for Iot Hub, device or module.</span></span>
* <span data-ttu-id="184db-1318">구성 메트릭 쿼리를 호출하는 cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-1318">Added cmdlet to invoke configuration metrics query.</span></span>
* <span data-ttu-id="184db-1319">IoT Edge 자동 배포를 대규모로 관리합니다.</span><span class="sxs-lookup"><span data-stu-id="184db-1319">Manage IoT Edge automatic deployment at scale.</span></span> <span data-ttu-id="184db-1320">새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-1320">New cmdlets are:</span></span>
    - <span data-ttu-id="184db-1321">'Add-AzIotHubDeployment'</span><span class="sxs-lookup"><span data-stu-id="184db-1321">'Add-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="184db-1322">'Get-AzIotHubDeployment'</span><span class="sxs-lookup"><span data-stu-id="184db-1322">'Get-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="184db-1323">'Remove-AzIotHubDeployment'</span><span class="sxs-lookup"><span data-stu-id="184db-1323">'Remove-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="184db-1324">'Set-AzIotHubDeployment'</span><span class="sxs-lookup"><span data-stu-id="184db-1324">'Set-AzIotHubDeployment'</span></span>
* <span data-ttu-id="184db-1325">IoT Edge 배포 메트릭 쿼리를 호출하는 cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-1325">Added cmdlet to invoke an IoT Edge deployment metrics query.</span></span>
* <span data-ttu-id="184db-1326">지정된 에지 디바이스에 구성 콘텐츠를 적용하는 cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-1326">Added cmdlet to apply the configuration content to the specified edge device.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="184db-1327">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="184db-1327">Az.KeyVault</span></span>
* <span data-ttu-id="184db-1328">다음 별칭 제거: 'New-AzKeyVaultCertificateAdministratorDetails' 및 'New-AzKeyVaultCertificateOrganizationDetails'</span><span class="sxs-lookup"><span data-stu-id="184db-1328">Removed two aliases: 'New-AzKeyVaultCertificateAdministratorDetails' and 'New-AzKeyVaultCertificateOrganizationDetails'</span></span>
* <span data-ttu-id="184db-1329">키 자격 증명 모음을 만들 때 기본적으로 일시 삭제 사용</span><span class="sxs-lookup"><span data-stu-id="184db-1329">Enabled soft delete by default when creating a key vault</span></span>
* <span data-ttu-id="184db-1330">키 자격 증명 모음을 만들 때 특정 네트워크 위치의 액세스를 제어하도록 네트워크 규칙을 설정할 수 있음</span><span class="sxs-lookup"><span data-stu-id="184db-1330">Network rules can be set to govern the accessibility from specific network locations when creating a key vault</span></span>
* <span data-ttu-id="184db-1331">BYOK(Bring Your Own Key) 지원 추가</span><span class="sxs-lookup"><span data-stu-id="184db-1331">Added support to bring your own key (BYOK)</span></span>
    - <span data-ttu-id="184db-1332">'Add-AzKeyVaultKey'가 키 교환 키 생성 지원</span><span class="sxs-lookup"><span data-stu-id="184db-1332">'Add-AzKeyVaultKey' supports generating a key exchange key</span></span>
    - <span data-ttu-id="184db-1333">'Get-AzKeyVaultKey'가 PEM 형식의 공개 키 다운로드 지원</span><span class="sxs-lookup"><span data-stu-id="184db-1333">'Get-AzKeyVaultKey' supports downloading a public key in PEM format</span></span>
* <span data-ttu-id="184db-1334">'AzKeyVaultKey' 도움말 문서의 'KeyOps' 부분 업데이트</span><span class="sxs-lookup"><span data-stu-id="184db-1334">Updated the 'KeyOps' part of the help document of 'Add-AzKeyVaultKey'</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="184db-1335">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="184db-1335">Az.Monitor</span></span>
* <span data-ttu-id="184db-1336">'Set-AzDiagnosticSettings'의 버그 수정, 일부 범주에는 보존 정책이 적용되지 않음 [#11589]</span><span class="sxs-lookup"><span data-stu-id="184db-1336">Fixed bug for 'Set-AzDiagnosticSettings', retention policy won't apply to all categories [#11589]</span></span>
* <span data-ttu-id="184db-1337">메트릭 경고 V2에 WebTest를 사용하기 위한 조건 지원</span><span class="sxs-lookup"><span data-stu-id="184db-1337">Supported WebTest availability criteria for metric alert V2</span></span>
    - <span data-ttu-id="184db-1338">'New-AzMetricAlertRuleV2Criteria': webtest 사용 조건을 만드는 옵션 추가</span><span class="sxs-lookup"><span data-stu-id="184db-1338">'New-AzMetricAlertRuleV2Criteria': an option to create webtest availability criteria was added</span></span>
    - <span data-ttu-id="184db-1339">'Add-AzMetricAlertRuleV2': 새 webtest 사용 조건 지원</span><span class="sxs-lookup"><span data-stu-id="184db-1339">'Add-AzMetricAlertRuleV2': supports the new webtest availability criteria</span></span>
* <span data-ttu-id="184db-1340">PSLogProfile에서 RetentionPolicy에 대한 중복 정의 제거 [#7608]</span><span class="sxs-lookup"><span data-stu-id="184db-1340">Removed redundant definition for RetentionPolicy in PSLogProfile [#7608]</span></span>
* <span data-ttu-id="184db-1341">PSEventData에 정의된 중복 속성 제거 [#11353]</span><span class="sxs-lookup"><span data-stu-id="184db-1341">Removed redundant properties difined in PSEventData [#11353]</span></span>
* <span data-ttu-id="184db-1342">'Get-AzLog'를 'Get-AzActivityLog'로 이름 변경</span><span class="sxs-lookup"><span data-stu-id="184db-1342">Renamed 'Get-AzLog' to 'Get-AzActivityLog'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="184db-1343">Az.Network</span><span class="sxs-lookup"><span data-stu-id="184db-1343">Az.Network</span></span>
* <span data-ttu-id="184db-1344">영역 기본 동작이 변경된다는 것을 알리기 위해 주요 변경 특성을 추가</span><span class="sxs-lookup"><span data-stu-id="184db-1344">Added breaking change attribute to notify that Zone default behaviour will be changed</span></span>
    - <span data-ttu-id="184db-1345">'New-AzPublicIpAddress'</span><span class="sxs-lookup"><span data-stu-id="184db-1345">'New-AzPublicIpAddress'</span></span>
    - <span data-ttu-id="184db-1346">'New-AzPublicIpPrefix'</span><span class="sxs-lookup"><span data-stu-id="184db-1346">'New-AzPublicIpPrefix'</span></span>
    - <span data-ttu-id="184db-1347">'New-AzLoadBalancerFrontendIpConfig'</span><span class="sxs-lookup"><span data-stu-id="184db-1347">'New-AzLoadBalancerFrontendIpConfig'</span></span>
* <span data-ttu-id="184db-1348">새로운 최상위 리소스 SecurityPartnerProvider에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="184db-1348">Added support for a new top level resource SecurityPartnerProvider</span></span>
    - <span data-ttu-id="184db-1349">추가된 새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-1349">New cmdlets added:</span></span>
        - <span data-ttu-id="184db-1350">New-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="184db-1350">New-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="184db-1351">Remove-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="184db-1351">Remove-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="184db-1352">Get-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="184db-1352">Get-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="184db-1353">Set-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="184db-1353">Set-AzSecurityPartnerProvider</span></span>
* <span data-ttu-id="184db-1354">'PSPrivateEndpointConnection'의 'PSPrivateLinkResource' 및 'GroupId'에서 'RequiredZoneNames' 추가</span><span class="sxs-lookup"><span data-stu-id="184db-1354">Added 'RequiredZoneNames' on 'PSPrivateLinkResource' and 'GroupId' on 'PSPrivateEndpointConnection'</span></span>
* <span data-ttu-id="184db-1355">New-AzNetworkWatcherConnectionMonitorTestConfigurationObject에 대한 잘못된 형식의 SuccessThresholdRoundTripTimeMs 매개 변수 수정</span><span class="sxs-lookup"><span data-stu-id="184db-1355">Fixed incorrect type of SuccessThresholdRoundTripTimeMs parameter for New-AzNetworkWatcherConnectionMonitorTestConfigurationObject</span></span>
* <span data-ttu-id="184db-1356">AllowVnetToVnetTraffic 인수의 기본값을 True로 설정하도록 VirtualWan cmdlet 업데이트</span><span class="sxs-lookup"><span data-stu-id="184db-1356">Updated VirtualWan cmdlets to set default value of AllowVnetToVnetTraffic argument to True.</span></span>
    - <span data-ttu-id="184db-1357">'New-AzVirtualWan'</span><span class="sxs-lookup"><span data-stu-id="184db-1357">'New-AzVirtualWan'</span></span>
    - <span data-ttu-id="184db-1358">'Update-AzVirtualWan'</span><span class="sxs-lookup"><span data-stu-id="184db-1358">'Update-AzVirtualWan'</span></span>
* <span data-ttu-id="184db-1359">프라이빗 엔드포인트에 대한 DNS 영역 그룹을 지원하는 새 cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="184db-1359">Added new cmdlets to support DNS zone group for private endpoint</span></span>
    - <span data-ttu-id="184db-1360">'New-AzPrivateDnsZoneConfig'</span><span class="sxs-lookup"><span data-stu-id="184db-1360">'New-AzPrivateDnsZoneConfig'</span></span>
    - <span data-ttu-id="184db-1361">'Get-AzPrivateDnsZoneGroup'</span><span class="sxs-lookup"><span data-stu-id="184db-1361">'Get-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="184db-1362">'New-AzPrivateDnsZoneGroup'</span><span class="sxs-lookup"><span data-stu-id="184db-1362">'New-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="184db-1363">'Set-AzPrivateDnsZoneGroup'</span><span class="sxs-lookup"><span data-stu-id="184db-1363">'Set-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="184db-1364">'Remove-AzPrivateDnsZoneGroup'</span><span class="sxs-lookup"><span data-stu-id="184db-1364">'Remove-AzPrivateDnsZoneGroup'</span></span>
* <span data-ttu-id="184db-1365">'AzureFirewall'에 'DNSEnableProxy', 'DNSRequireProxyForNetworkRules' 및 'DNSServers' 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="184db-1365">Added 'DNSEnableProxy', 'DNSRequireProxyForNetworkRules' and 'DNSServers' parameters to 'AzureFirewall'</span></span>
* <span data-ttu-id="184db-1366">'AzureFirewall'에 'EnableDnsProxy', 'DnsProxyNotRequiredForNetworkRule' 및 'DnsServer' 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="184db-1366">Added 'EnableDnsProxy', 'DnsProxyNotRequiredForNetworkRule' and 'DnsServer' parameters to 'AzureFirewall'</span></span>
    - <span data-ttu-id="184db-1367">업데이트된 cmdlet:</span><span class="sxs-lookup"><span data-stu-id="184db-1367">Updated cmdlet:</span></span>
        - <span data-ttu-id="184db-1368">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="184db-1368">New-AzFirewall</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="184db-1369">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="184db-1369">Az.OperationalInsights</span></span>
* <span data-ttu-id="184db-1370">새로 생성된 SDK를 적용하도록 레거시 코드 업데이트</span><span class="sxs-lookup"><span data-stu-id="184db-1370">Updated legacy code to apply new generated SDK</span></span>
* <span data-ttu-id="184db-1371">사용되지 않는 API 때문에 cmdlet 삭제</span><span class="sxs-lookup"><span data-stu-id="184db-1371">Deleted cmdlets due to deprecated APIs</span></span>
    - <span data-ttu-id="184db-1372">'Get-AzOperationalInsightsSavedSearchResult'(별칭 'Get-AzOperationalInsightsSavedSearchResults')</span><span class="sxs-lookup"><span data-stu-id="184db-1372">'Get-AzOperationalInsightsSavedSearchResult' (alias 'Get-AzOperationalInsightsSavedSearchResults')</span></span>
    - <span data-ttu-id="184db-1373">'Get-AzOperationalInsightsSearchResult'(별칭 'Get-AzOperationalInsightsSearchResults')</span><span class="sxs-lookup"><span data-stu-id="184db-1373">'Get-AzOperationalInsightsSearchResult' (alias 'Get-AzOperationalInsightsSearchResults')</span></span>
    - <span data-ttu-id="184db-1374">'Get-AzOperationalInsightsLinkTarget'(별칭 'Get-AzOperationalInsightsLinkTargets')</span><span class="sxs-lookup"><span data-stu-id="184db-1374">'Get-AzOperationalInsightsLinkTarget' (alias 'Get-AzOperationalInsightsLinkTargets')</span></span>
* <span data-ttu-id="184db-1375">'Set-AzOperationalInsightsWorkspace' 및 'New-AzOperationalInsightsWorkspace'에 대한 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="184db-1375">Added parameters for 'Set-AzOperationalInsightsWorkspace' and 'New-AzOperationalInsightsWorkspace'</span></span>
* <span data-ttu-id="184db-1376">연결된 스토리지 계정에 대한 cmdlet 작성</span><span class="sxs-lookup"><span data-stu-id="184db-1376">Created cmdlets for Linked Stoarge Account</span></span>
* <span data-ttu-id="184db-1377">클러스터 및 연결된 서비스에 대한 cmdlet 작성</span><span class="sxs-lookup"><span data-stu-id="184db-1377">Created cmdlets for Clusters and Linked Service</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="184db-1378">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="184db-1378">Az.RecoveryServices</span></span>
* <span data-ttu-id="184db-1379">Azure Site Recovery - Azure와 Azure 공급자 간 근접 배치 그룹 가상 머신을 보호하기 위한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-1379">Azure Site Recovery added support for protecting proximity placement group virtual machines for Azure to Azure provider.</span></span>
* <span data-ttu-id="184db-1380">Azure Site Recovery - 영역 간 복제에 대한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-1380">Azure Site Recovery added support for zone to zone replication.</span></span>
* <span data-ttu-id="184db-1381">Azure Backup - Azure 파일 공유 복구 지점의 장기 보존 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-1381">Azure Backup Added Long term retention support for Azure FileShare Recovery Points.</span></span>
* <span data-ttu-id="184db-1382">Azure Backup - 'Get-AzRecoveryServicesBackupItem' cmdlet 출력에 디스크 제외 속성이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-1382">Azure Backup Added disk exclusion properties to 'Get-AzRecoveryServicesBackupItem' cmdlet output.</span></span>
* <span data-ttu-id="184db-1383">사이트 복구 서비스용 Vault 자격 증명 파일에 대한 프라이빗 엔드포인트가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-1383">Added private endpoint for Vault credential file for site recovery service.</span></span>

#### <a name="azresources"></a><span data-ttu-id="184db-1384">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="184db-1384">Az.Resources</span></span>
* <span data-ttu-id="184db-1385">새 역할 정의를 만들 때 보기 지연에 대한 메시지 경고 추가</span><span class="sxs-lookup"><span data-stu-id="184db-1385">Added message warning about view delay when creating a new Role Definition</span></span>
* <span data-ttu-id="184db-1386">강력한 형식의 개체를 출력하도록 정책 cmdlet 변경</span><span class="sxs-lookup"><span data-stu-id="184db-1386">Changed policy cmdlets to output strongly-typed objects</span></span>
* <span data-ttu-id="184db-1387">'Get-AzResourceLock' cmdlet에 사용되는 '-TenantLevel' 매개 변수 제거 [#11335]</span><span class="sxs-lookup"><span data-stu-id="184db-1387">Removed '-TenantLevel' parameter used for on the 'Get-AzResourceLock' cmdlet [#11335]</span></span>
* <span data-ttu-id="184db-1388">'Remove-AzResourceGroup -Id ResourceId' 수정[#9882]</span><span class="sxs-lookup"><span data-stu-id="184db-1388">Fixed 'Remove-AzResourceGroup -Id ResourceId'[#9882]</span></span>
* <span data-ttu-id="184db-1389">리소스 그룹 범위에서 ARM 템플릿 가상 시나리오 결과를 가져오는 새 cmdlet 추가: 'Get-AzDeploymentResourceGroupWhatIfResult'</span><span class="sxs-lookup"><span data-stu-id="184db-1389">Added new cmdlet for getting ARM template What-If results at resource group scope: 'Get-AzDeploymentResourceGroupWhatIfResult'</span></span>
* <span data-ttu-id="184db-1390">구독 범위에서 ARM 템플릿 가상 시나리오 결과를 가져오는 새 cmdlet 추가: 'Get-AzDeploymentWhatIfResult'</span><span class="sxs-lookup"><span data-stu-id="184db-1390">Added new cmdlet for getting ARM template What-If results at subscription scope: 'Get-AzDeploymentWhatIfResult'</span></span>
   - <span data-ttu-id="184db-1391">별칭: 'Get-AzSubscriptionDeploymentWhatIf'</span><span class="sxs-lookup"><span data-stu-id="184db-1391">Alias: 'Get-AzSubscriptionDeploymentWhatIf'</span></span>
* <span data-ttu-id="184db-1392">ARM 템플릿 가상 시나리오 결과를 사용하도록 'New-AzDeployment' 및 'New-AzResourceGroupDeployment'에 대한 '-WhatIf' 및 '-Confirm' 매개 변수 재정의</span><span class="sxs-lookup"><span data-stu-id="184db-1392">Overrode '-WhatIf' and '-Confirm' parameters for 'New-AzDeployment' and 'New-AzResourceGroupDeployment' to use ARM template What-If results</span></span>
* <span data-ttu-id="184db-1393">배포 cmdlet에서 'ApiVersion' 매개 변수의 사용 중단 메시지 추가</span><span class="sxs-lookup"><span data-stu-id="184db-1393">Added deprecation message for 'ApiVersion' parameter in deployment cmdlets</span></span>
* <span data-ttu-id="184db-1394">배포 오류에 대한 향상된 오류 메시지를 표시하는 기능 추가</span><span class="sxs-lookup"><span data-stu-id="184db-1394">Added capability to show improved error messages for deployment failures</span></span>
* <span data-ttu-id="184db-1395">배포 오류에 대한 correlationId 로깅 추가</span><span class="sxs-lookup"><span data-stu-id="184db-1395">Added correlationId logging for deployment failures</span></span>
* <span data-ttu-id="184db-1396">배포 스크립트 출력에 'error' 속성 추가</span><span class="sxs-lookup"><span data-stu-id="184db-1396">Added 'error' property to the deployment script output</span></span>
* <span data-ttu-id="184db-1397">nuget Microsoft.Azure.Management.ResourceManager를 '3.7.1-preview'로 업데이트</span><span class="sxs-lookup"><span data-stu-id="184db-1397">Updated nuget Microsoft.Azure.Management.ResourceManager to '3.7.1-preview'</span></span>
* <span data-ttu-id="184db-1398">nuget 3.7.1-preview에서 DeploymentValidateResult의 Error 속성이 readonly로 변경되어 특정 테스트 사례를 제거</span><span class="sxs-lookup"><span data-stu-id="184db-1398">Removed specific test cases as Error property in DeploymentValidateResult has changed to readonly from nuget 3.7.1-preview</span></span>
* <span data-ttu-id="184db-1399">SDK ResourceManager 3.7.1-preview의 GenericResourceExpanded 도입</span><span class="sxs-lookup"><span data-stu-id="184db-1399">Brought GenericResourceExpanded from SDK ResourceManager 3.7.1-preview</span></span>
* <span data-ttu-id="184db-1400">모든 배포용 Get cmdlet에 대한 태그 지원 추가</span><span class="sxs-lookup"><span data-stu-id="184db-1400">Added tag support for all Get cmdlets for deployment, as well as</span></span>
    - <span data-ttu-id="184db-1401">'New-AzDeployment'</span><span class="sxs-lookup"><span data-stu-id="184db-1401">'New-AzDeployment'</span></span>
    - <span data-ttu-id="184db-1402">'New-AzManagementGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="184db-1402">'New-AzManagementGroupDeployment'</span></span>
    - <span data-ttu-id="184db-1403">'New-AzResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="184db-1403">'New-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="184db-1404">'New-AzTenantDeployment'</span><span class="sxs-lookup"><span data-stu-id="184db-1404">'New-AzTenantDeployment'</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="184db-1405">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="184db-1405">Az.ServiceFabric</span></span>
* <span data-ttu-id="184db-1406">잘못된 인증서 지문을 가져오는 --SecretIdentifier를 사용한 인증서 추가의 버그 수정</span><span class="sxs-lookup"><span data-stu-id="184db-1406">Fixed bug in add certificate using --SecretIdentifier that was getting the wrong certificate thumbprint</span></span>

#### <a name="azsql"></a><span data-ttu-id="184db-1407">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="184db-1407">Az.Sql</span></span>
* <span data-ttu-id="184db-1408">성능 강화:</span><span class="sxs-lookup"><span data-stu-id="184db-1408">Enhance performance of:</span></span>
    - <span data-ttu-id="184db-1409">'Set-AzSqlDatabaseSensitivityClassification'</span><span class="sxs-lookup"><span data-stu-id="184db-1409">'Set-AzSqlDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="184db-1410">'Set-AzSqlInstanceDatabaseSensitivityClassification'</span><span class="sxs-lookup"><span data-stu-id="184db-1410">'Set-AzSqlInstanceDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="184db-1411">'Remove-AzSqlDatabaseSensitivityClassification'</span><span class="sxs-lookup"><span data-stu-id="184db-1411">'Remove-AzSqlDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="184db-1412">'Remove-AzSqlInstanceDatabaseSensitivityClassification'</span><span class="sxs-lookup"><span data-stu-id="184db-1412">'Remove-AzSqlInstanceDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="184db-1413">'Enable-AzSqlDatabaseSensitivityRecommendation'</span><span class="sxs-lookup"><span data-stu-id="184db-1413">'Enable-AzSqlDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="184db-1414">'Enable-AzSqlInstanceDatabaseSensitivityRecommendation'</span><span class="sxs-lookup"><span data-stu-id="184db-1414">'Enable-AzSqlInstanceDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="184db-1415">'Disable-AzSqlDatabaseSensitivityRecommendation'</span><span class="sxs-lookup"><span data-stu-id="184db-1415">'Disable-AzSqlDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="184db-1416">'Disable-AzSqlInstanceDatabaseSensitivityRecommendation'</span><span class="sxs-lookup"><span data-stu-id="184db-1416">'Disable-AzSqlInstanceDatabaseSensitivityRecommendation'</span></span>
* <span data-ttu-id="184db-1417">'Set-AzSqlDatabaseBackupShortTermRetentionPolicy' cmdlet에서 'RetentionDays' 매개 변수의 클라이언트 쪽 유효성 검사 제거</span><span class="sxs-lookup"><span data-stu-id="184db-1417">Removed client-side validation of 'RetentionDays' parameter from cmdlet 'Set-AzSqlDatabaseBackupShortTermRetentionPolicy'</span></span>
* <span data-ttu-id="184db-1418">Vnet에서 스토리지 계정을 감사하고, Storage Blob 데이터 기여자 역할을 만들 때 발생하는 버그 수정</span><span class="sxs-lookup"><span data-stu-id="184db-1418">Auditing to a storage account in Vnet, fixing a bug when creating a Storage Blob Data Contributor role.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="184db-1419">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="184db-1419">Az.Storage</span></span>
* <span data-ttu-id="184db-1420">get/list account cmdlet 'Get-AzStorageAccount'에 '-AsJob' 추가</span><span class="sxs-lookup"><span data-stu-id="184db-1420">Added '-AsJob' to get/list account cmdlet 'Get-AzStorageAccount'</span></span>
* <span data-ttu-id="184db-1421">키 자동 회전을 지원하기 위해 스토리지 계정을 KeyvaultEncryption으로 업데이트할 때 KeyVersion을 선택 사항으로 지정</span><span class="sxs-lookup"><span data-stu-id="184db-1421">Make KeyVersion to optional when update Storage account with KeyvaultEncryption, to support key auto-rotation</span></span>
    - <span data-ttu-id="184db-1422">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="184db-1422">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="184db-1423">파이프라인을 사용하여 Azure 파일 디렉터리 제거 오류 수정</span><span class="sxs-lookup"><span data-stu-id="184db-1423">Fixed remove Azure File Directory fail with pipeline</span></span>
    - <span data-ttu-id="184db-1424">'Remove-AzStorageDirectory'</span><span class="sxs-lookup"><span data-stu-id="184db-1424">'Remove-AzStorageDirectory'</span></span>
* <span data-ttu-id="184db-1425">수정 [#9880]: Swagger에 맞게 NetWorkRule DefaultAction 값 정의 변경</span><span class="sxs-lookup"><span data-stu-id="184db-1425">Fixed [#9880]: Change NetWorkRule DefaultAction value defination to align with swagger.</span></span>
    - <span data-ttu-id="184db-1426">'Update-AzStorageAccountNetworkRuleSet'</span><span class="sxs-lookup"><span data-stu-id="184db-1426">'Update-AzStorageAccountNetworkRuleSet'</span></span>
    - <span data-ttu-id="184db-1427">'Get-AzStorageAccountNetworkRuleSet'</span><span class="sxs-lookup"><span data-stu-id="184db-1427">'Get-AzStorageAccountNetworkRuleSet'</span></span>
* <span data-ttu-id="184db-1428">수정 [#11624]: 서버 오류를 방지하기 위해 NetworkRules를 추가할 때 중복 규칙 건너뛰기</span><span class="sxs-lookup"><span data-stu-id="184db-1428">Fixed [#11624]: Skip duplicated rules when add NetworkRules, to avoid server failure</span></span>
    - <span data-ttu-id="184db-1429">'Add-AzStorageAccountNetworkRule'</span><span class="sxs-lookup"><span data-stu-id="184db-1429">'Add-AzStorageAccountNetworkRule'</span></span>
* <span data-ttu-id="184db-1430">Microsoft.Azure.Cosmos.Table SDK를 1.0.7로 업그레이드</span><span class="sxs-lookup"><span data-stu-id="184db-1430">Upgraded Microsoft.Azure.Cosmos.Table SDK to 1.0.7</span></span>
* <span data-ttu-id="184db-1431">DataLake Gen2 항목 목록에 부품 항목만 반환되는 경우 ContinuationToken을 사용하여 다시 나열하라고 사용자에게 알리는 경고 메시지 추가</span><span class="sxs-lookup"><span data-stu-id="184db-1431">Added a warning message to remind user to list again with ContinuationToken when only part items are returned in list DataLake Gen2 Items,</span></span>
    - <span data-ttu-id="184db-1432">'Get-AzDataLakeGen2ChildItem'</span><span class="sxs-lookup"><span data-stu-id="184db-1432">'Get-AzDataLakeGen2ChildItem'</span></span>
* <span data-ttu-id="184db-1433">Azure Files Active Directory 도메인 서비스 인증을 사용하여 스토리지 계정을 만들거나 업데이트하는 기능 지원</span><span class="sxs-lookup"><span data-stu-id="184db-1433">Supported to create or update Storage account with Azure Files Active Directory Domain Service Authentication</span></span>
    -  <span data-ttu-id="184db-1434">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="184db-1434">'New-AzStorageAccount'</span></span>
    -  <span data-ttu-id="184db-1435">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="184db-1435">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="184db-1436">스토리지 계정의 Kerberos 키 새로 만들기 또는 나열 지원</span><span class="sxs-lookup"><span data-stu-id="184db-1436">Supported to new or list Kerberos keys of Storage account</span></span>
    -  <span data-ttu-id="184db-1437">'New-AzStorageAccountKey'</span><span class="sxs-lookup"><span data-stu-id="184db-1437">'New-AzStorageAccountKey'</span></span>
    -  <span data-ttu-id="184db-1438">'Get-AzStorageAccountKey'</span><span class="sxs-lookup"><span data-stu-id="184db-1438">'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="184db-1439">스토리지 계정 장애 조치(failover) 지원</span><span class="sxs-lookup"><span data-stu-id="184db-1439">Supported failover Storage account</span></span>
    - <span data-ttu-id="184db-1440">'Invoke-AzStorageAccountFailover'</span><span class="sxs-lookup"><span data-stu-id="184db-1440">'Invoke-AzStorageAccountFailover'</span></span>
* <span data-ttu-id="184db-1441">'Get-AzStorageBlobCopyState'의 도움말 업데이트</span><span class="sxs-lookup"><span data-stu-id="184db-1441">Updated help of 'Get-AzStorageBlobCopyState'</span></span>
* <span data-ttu-id="184db-1442">'Get-AzStorageFileCopyState' 및 'Start-AzStorageBlobCopy'의 도움말 업데이트</span><span class="sxs-lookup"><span data-stu-id="184db-1442">Updated help of 'Get-AzStorageFileCopyState' and 'Start-AzStorageBlobCopy'</span></span>
* <span data-ttu-id="184db-1443">스토리지 클라이언트 라이브러리 v12를 큐 및 파일 cmdlet에 통합</span><span class="sxs-lookup"><span data-stu-id="184db-1443">Integrated Storage client library v12 to Queue and File cmdlets</span></span>
* <span data-ttu-id="184db-1444">출력 형식을 CloudFile에서 AzureStorageFile로 변경했으며, 원래 출력은 새 출력의 자식 속성이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="184db-1444">Changed output type from CloudFile to AzureStorageFile, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="184db-1445">'Get-AzStorageFile'</span><span class="sxs-lookup"><span data-stu-id="184db-1445">'Get-AzStorageFile'</span></span>
    - <span data-ttu-id="184db-1446">'Remove-AzStorageFile'</span><span class="sxs-lookup"><span data-stu-id="184db-1446">'Remove-AzStorageFile'</span></span>
    - <span data-ttu-id="184db-1447">'Get-AzStorageFileContent'</span><span class="sxs-lookup"><span data-stu-id="184db-1447">'Get-AzStorageFileContent'</span></span>
    - <span data-ttu-id="184db-1448">'Set-AzStorageFileContent'</span><span class="sxs-lookup"><span data-stu-id="184db-1448">'Set-AzStorageFileContent'</span></span>
    - <span data-ttu-id="184db-1449">'Start-AzStorageFileCopy'</span><span class="sxs-lookup"><span data-stu-id="184db-1449">'Start-AzStorageFileCopy'</span></span>
* <span data-ttu-id="184db-1450">출력 형식을 CloudFileDirectory에서 AzureStorageFileDirectory로 변경했으며, 원래 출력은 새 출력의 자식 속성이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="184db-1450">Changed output type from CloudFileDirectory to AzureStorageFileDirectory, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="184db-1451">'New-AzStorageDirectory'</span><span class="sxs-lookup"><span data-stu-id="184db-1451">'New-AzStorageDirectory'</span></span>
    - <span data-ttu-id="184db-1452">'Remove-AzStorageDirectory'</span><span class="sxs-lookup"><span data-stu-id="184db-1452">'Remove-AzStorageDirectory'</span></span>
* <span data-ttu-id="184db-1453">출력 형식을 CloudFileShare에서 AzureStorageFileShare로 변경했으며, 원래 출력은 새 출력의 자식 속성이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="184db-1453">Changed output type from CloudFileShare to AzureStorageFileShare, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="184db-1454">'Get-AzStorageShare'</span><span class="sxs-lookup"><span data-stu-id="184db-1454">'Get-AzStorageShare'</span></span>
    - <span data-ttu-id="184db-1455">'New-AzStorageShare'</span><span class="sxs-lookup"><span data-stu-id="184db-1455">'New-AzStorageShare'</span></span>
    - <span data-ttu-id="184db-1456">'Remove-AzStorageShare'</span><span class="sxs-lookup"><span data-stu-id="184db-1456">'Remove-AzStorageShare'</span></span>
* <span data-ttu-id="184db-1457">출력 형식을 FileShareProperties에서 AzureStorageFileShare로 변경했으며, 원래 출력은 새 출력의 하위 자식 속성이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="184db-1457">Changed output type from FileShareProperties to AzureStorageFileShare, the original output will become a sub child property of the new output</span></span>
    - <span data-ttu-id="184db-1458">'Set-AzStorageShareQuota'</span><span class="sxs-lookup"><span data-stu-id="184db-1458">'Set-AzStorageShareQuota'</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="184db-1459">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="184db-1459">Az.TrafficManager</span></span>
* <span data-ttu-id="184db-1460">'DisableAzureTrafficManagerEndpoint' 자세한 정보 출력에서 잘못된 프로필 이름 수정</span><span class="sxs-lookup"><span data-stu-id="184db-1460">Fixed incorrect profile name in 'DisableAzureTrafficManagerEndpoint' verbose output</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="184db-1461">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="184db-1461">Az.Websites</span></span>
* <span data-ttu-id="184db-1462">'Update-AzWebAppAccessRestrictionConfig'의 도움말에서 철자 오류 수정</span><span class="sxs-lookup"><span data-stu-id="184db-1462">Fixed typo on help of 'Update-AzWebAppAccessRestrictionConfig'.</span></span>

## <a name="380---april-2020"></a><span data-ttu-id="184db-1463">3.8.0 - 2020년 4월</span><span class="sxs-lookup"><span data-stu-id="184db-1463">3.8.0 - April 2020</span></span>
### <a name="highlights-since-the-last-release"></a><span data-ttu-id="184db-1464">마지막 릴리스 이후의 주요 사항</span><span class="sxs-lookup"><span data-stu-id="184db-1464">Highlights since the last release</span></span>
* <span data-ttu-id="184db-1465">Az.Storage에서 지원하는 PowerShell 버전: Windows PowerShell 5.1, PowerShell Core 6.2.4 이상, PowerShell 7</span><span class="sxs-lookup"><span data-stu-id="184db-1465">PowerShell versions that Az.Storage supports: Windows PowerShell 5.1, PowerShell Core 6.2.4+, PowerShell 7</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="184db-1466">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="184db-1466">Az.Accounts</span></span>
* <span data-ttu-id="184db-1467">'Resolve-AzError'에서 Azure PowerShell 설문 조사 URL이 업데이트되었습니다. [#11507]</span><span class="sxs-lookup"><span data-stu-id="184db-1467">Updated Azure PowerShell survey URL in 'Resolve-AzError' [#11507]</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="184db-1468">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="184db-1468">Az.ApiManagement</span></span>
* <span data-ttu-id="184db-1469">향후 릴리스의 Azure File cmdlet 출력 변경에 대한 호환성이 손상되는 변경 공지가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-1469">Added breaking change notice for Azure File cmdlets output change in a future release</span></span>
* <span data-ttu-id="184db-1470">'Set-AzApiManagementGroup' - GroupId 매개 변수를 지정하도록 설명서가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-1470">'Set-AzApiManagementGroup' Updated documentation to specify the GroupId parameter</span></span>

#### <a name="azcdn"></a><span data-ttu-id="184db-1471">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="184db-1471">Az.Cdn</span></span>
* <span data-ttu-id="184db-1472">ChinaCDN 관련 가격 책정 SKU 표시가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-1472">Fixed ChinaCDN related pricing SKU display</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="184db-1473">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="184db-1473">Az.CognitiveServices</span></span>
* <span data-ttu-id="184db-1474">Identity, Encryption, UserOwnedStorage가 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="184db-1474">Supported Identity, Encryption, UserOwnedStorage</span></span>

#### <a name="azcompute"></a><span data-ttu-id="184db-1475">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="184db-1475">Az.Compute</span></span>
* <span data-ttu-id="184db-1476">'Set-AzVmssOrchestrationServiceState' cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-1476">Added 'Set-AzVmssOrchestrationServiceState' cmdlet.</span></span>
* <span data-ttu-id="184db-1477">-InstanceView가 있는 'Get-AzVmss'는 OrchestrationService 상태를 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="184db-1477">'Get-AzVmss' with -InstanceView shows OrchestrationService states.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="184db-1478">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="184db-1478">Az.IotHub</span></span>
* <span data-ttu-id="184db-1479">IoT 디바이스 쌍 구성을 관리합니다. 새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-1479">Manage IoT device twin configuration, New cmdlets are:</span></span>
    - <span data-ttu-id="184db-1480">'Get-AzIotHubDeviceTwin'</span><span class="sxs-lookup"><span data-stu-id="184db-1480">'Get-AzIotHubDeviceTwin'</span></span>
    - <span data-ttu-id="184db-1481">'Update-AzIotHubDeviceTwin'</span><span class="sxs-lookup"><span data-stu-id="184db-1481">'Update-AzIotHubDeviceTwin'</span></span>
* <span data-ttu-id="184db-1482">IoT Hub에서 디바이스에 대한 직접 메서드를 호출하는 cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-1482">Added cmdlet to invoke direct method on a device in an Iot Hub.</span></span>
* <span data-ttu-id="184db-1483">IoT 디바이스 모듈 쌍 구성을 관리합니다. 새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-1483">Manage IoT device module twin configuration, New cmdlets are:</span></span>
    - <span data-ttu-id="184db-1484">'Get-AzIotHubModuleTwin'</span><span class="sxs-lookup"><span data-stu-id="184db-1484">'Get-AzIotHubModuleTwin'</span></span>
    - <span data-ttu-id="184db-1485">'Update-AzIotHubModuleTwin'</span><span class="sxs-lookup"><span data-stu-id="184db-1485">'Update-AzIotHubModuleTwin'</span></span>
* <span data-ttu-id="184db-1486">IoT 자동 디바이스 관리 구성을 대규모로 관리합니다.</span><span class="sxs-lookup"><span data-stu-id="184db-1486">Manage IoT automatic device management configuration at scale.</span></span> <span data-ttu-id="184db-1487">새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-1487">New cmdlets are:</span></span>
    - <span data-ttu-id="184db-1488">'Add-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="184db-1488">'Add-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="184db-1489">'Get-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="184db-1489">'Get-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="184db-1490">'Remove-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="184db-1490">'Remove-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="184db-1491">'Set-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="184db-1491">'Set-AzIotHubConfiguration'</span></span>
* <span data-ttu-id="184db-1492">Iot Hub에서 에지 모듈 메서드를 호출하는 cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-1492">Added cmdlet to invoke an edge module method in an Iot Hub.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="184db-1493">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="184db-1493">Az.KeyVault</span></span>
* <span data-ttu-id="184db-1494">자격 증명 모음에서 일시 삭제 및 제거 보호를 사용하도록 설정할 수 있는 새 cmdlet 'Update-AzKeyVault'가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-1494">Added a new cmdlet 'Update-AzKeyVault' that can enable soft delete and purge protection on a vault</span></span>
* <span data-ttu-id="184db-1495">Microsoft.PowerShell.SecretManagement에 대한 지원이 추가되었습니다. [#11178]</span><span class="sxs-lookup"><span data-stu-id="184db-1495">Added support to Microsoft.PowerShell.SecretManagement [#11178]</span></span>
* <span data-ttu-id="184db-1496">'Remove-AzKeyVaultManagedStorageSasDefinition' 예제의 오류가 해결되었습니다. [#11479]</span><span class="sxs-lookup"><span data-stu-id="184db-1496">Fixed error in the examples of 'Remove-AzKeyVaultManagedStorageSasDefinition' [#11479]</span></span>
* <span data-ttu-id="184db-1497">프라이빗 엔드포인트에 대한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-1497">Added support to private endpoint</span></span>

#### <a name="azmaintenance"></a><span data-ttu-id="184db-1498">Az.Maintenance</span><span class="sxs-lookup"><span data-stu-id="184db-1498">Az.Maintenance</span></span>
* <span data-ttu-id="184db-1499">GA용 유지 관리 cmdlet의 릴리스 버전 게시</span><span class="sxs-lookup"><span data-stu-id="184db-1499">Publishing release version of Maintenance cmdlets for GA</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="184db-1500">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="184db-1500">Az.Monitor</span></span>
* <span data-ttu-id="184db-1501">프라이빗 링크 범위용 cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-1501">Added cmdlets for private link scope</span></span>
    - <span data-ttu-id="184db-1502">'Get-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="184db-1502">'Get-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="184db-1503">'Remove-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="184db-1503">'Remove-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="184db-1504">'New-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="184db-1504">'New-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="184db-1505">'Update-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="184db-1505">'Update-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="184db-1506">'Get-AzInsightsPrivateLinkScopedResource'</span><span class="sxs-lookup"><span data-stu-id="184db-1506">'Get-AzInsightsPrivateLinkScopedResource'</span></span>
    - <span data-ttu-id="184db-1507">'New-AzInsightsPrivateLinkScopedResource'</span><span class="sxs-lookup"><span data-stu-id="184db-1507">'New-AzInsightsPrivateLinkScopedResource'</span></span>
    - <span data-ttu-id="184db-1508">'Remove-AzInsightsPrivateLinkScopedResource'</span><span class="sxs-lookup"><span data-stu-id="184db-1508">'Remove-AzInsightsPrivateLinkScopedResource'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="184db-1509">Az.Network</span><span class="sxs-lookup"><span data-stu-id="184db-1509">Az.Network</span></span>
* <span data-ttu-id="184db-1510">Virtual Network 게이트웨이의 개인 IP에 대한 연결을 사용하도록 설정하는 cmdlet이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-1510">Updated cmdlets to enable connection on private IP for Virtual Network Gateway.</span></span>
    - <span data-ttu-id="184db-1511">'New-AzVirtualNetworkGateway'</span><span class="sxs-lookup"><span data-stu-id="184db-1511">'New-AzVirtualNetworkGateway'</span></span>
    - <span data-ttu-id="184db-1512">'Set-AzVirtualNetworkGateway'</span><span class="sxs-lookup"><span data-stu-id="184db-1512">'Set-AzVirtualNetworkGateway'</span></span>
    - <span data-ttu-id="184db-1513">'New-AzVirtualNetworkGatewayConnection'</span><span class="sxs-lookup"><span data-stu-id="184db-1513">'New-AzVirtualNetworkGatewayConnection'</span></span>
    - <span data-ttu-id="184db-1514">'Set-AzVirtualNetworkGatewayConnection'</span><span class="sxs-lookup"><span data-stu-id="184db-1514">'Set-AzVirtualNetworkGatewayConnection'</span></span>
* <span data-ttu-id="184db-1515">FQDN 기반 LocalNetworkGateways 및 VpnSites를 사용하도록 설정하는 cmdlet이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-1515">Updated cmdlets to enable FQDN based LocalNetworkGateways and VpnSites</span></span>
    - <span data-ttu-id="184db-1516">'New-AzLocalNetworkGateway'</span><span class="sxs-lookup"><span data-stu-id="184db-1516">'New-AzLocalNetworkGateway'</span></span>
    - <span data-ttu-id="184db-1517">'New-AzVpnSiteLink'</span><span class="sxs-lookup"><span data-stu-id="184db-1517">'New-AzVpnSiteLink'</span></span>
* <span data-ttu-id="184db-1518">ExpressRouteCircuitConnectionConfig(Global Reach)의 IPv6 주소 패밀리에 대한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-1518">Added support for IPv6 address family in ExpressRouteCircuitConnectionConfig (Global Reach)</span></span>
    - <span data-ttu-id="184db-1519">'Set-AzExpressRouteCircuitConnectionConfig'가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-1519">Added 'Set-AzExpressRouteCircuitConnectionConfig'</span></span>
        - <span data-ttu-id="184db-1520">IPv6CircuitConnectionProperties를 포함한 모든 기존 속성을 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-1520">allows setting of all the existing properties including the IPv6CircuitConnectionProperties</span></span>
    - <span data-ttu-id="184db-1521">'Add-AzExpressRouteCircuitConnectionConfig'가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-1521">Updated 'Add-AzExpressRouteCircuitConnectionConfig'</span></span>
        - <span data-ttu-id="184db-1522">주소 접두사의 주소 패밀리를 지정하는 또 다른 선택적 매개 변수 AddressPrefixType이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-1522">Added another optional parameter AddressPrefixType to specify the address family of address prefix</span></span>
* <span data-ttu-id="184db-1523">Virtual Network 게이트웨이 연결에서 DPD 시간 제한 설정을 사용하도록 cmdlet이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-1523">Updated cmdlets to enable setting of DPD Timeout on Virtual Network Gateway Connections.</span></span>
    - <span data-ttu-id="184db-1524">New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="184db-1524">New-AzVirtualNetworkGatewayConnection</span></span>
    - <span data-ttu-id="184db-1525">Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="184db-1525">Set-AzVirtualNetworkGatewayConnection</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="184db-1526">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="184db-1526">Az.PolicyInsights</span></span>
* <span data-ttu-id="184db-1527">정책 준수 검사를 트리거하기 위한 'Start-AzPolicyComplianceScan' cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-1527">Added 'Start-AzPolicyComplianceScan' cmdlet for triggering policy compliance scans</span></span>
* <span data-ttu-id="184db-1528">'Get-AzPolicyState' 출력에 정책 정의, 집합 정의 및 할당 버전이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-1528">Added policy definition, set definition, and assignment versions to 'Get-AzPolicyState' output</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="184db-1529">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="184db-1529">Az.ServiceFabric</span></span>
* <span data-ttu-id="184db-1530">'New-AzServiceFabricCluster' 예제의 코드 서식 및 사용 편의성이 개선되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-1530">Improved code formatting and usability of 'New-AzServiceFabricCluster' examples</span></span>

#### <a name="azsql"></a><span data-ttu-id="184db-1531">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="184db-1531">Az.Sql</span></span>
* <span data-ttu-id="184db-1532">'Get-AzSqlInstanceOperation' 및 'Stop-AzSqlInstanceOperation' cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-1532">Added cmdlets 'Get-AzSqlInstanceOperation' and 'Stop-AzSqlInstanceOperation'</span></span>
* <span data-ttu-id="184db-1533">VNet에서 스토리지 계정에 대한 감사가 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="184db-1533">Supported auditing to a storage account in VNet.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="184db-1534">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="184db-1534">Az.Storage</span></span>
* <span data-ttu-id="184db-1535">향후 릴리스의 Azure File cmdlet 출력 변경에 대한 호환성이 손상되는 변경 공지가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-1535">Added breaking change notice for Azure File cmdlets output change in a future release</span></span>
* <span data-ttu-id="184db-1536">스토리지 계정 생성/업데이트 시 새로운 SkuName StandardGZRS, StandardRAGZRS가 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="184db-1536">Supported new SkuName StandardGZRS, StandardRAGZRS when create/update Storage account</span></span>
    - <span data-ttu-id="184db-1537">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="184db-1537">'New-AzStorageAccount'</span></span>
    - <span data-ttu-id="184db-1538">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="184db-1538">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="184db-1539">DataLake Gen2가 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="184db-1539">Supported DataLake Gen2</span></span>
    - <span data-ttu-id="184db-1540">'New-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="184db-1540">'New-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="184db-1541">'Get-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="184db-1541">'Get-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="184db-1542">'Get-AzDataLakeGen2ChildItem'</span><span class="sxs-lookup"><span data-stu-id="184db-1542">'Get-AzDataLakeGen2ChildItem'</span></span>
    - <span data-ttu-id="184db-1543">'Move-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="184db-1543">'Move-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="184db-1544">'Set-AzDataLakeGen2ItemAclObject'</span><span class="sxs-lookup"><span data-stu-id="184db-1544">'Set-AzDataLakeGen2ItemAclObject'</span></span>
    - <span data-ttu-id="184db-1545">'Update-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="184db-1545">'Update-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="184db-1546">'Get-AzDataLakeGen2ItemContent'</span><span class="sxs-lookup"><span data-stu-id="184db-1546">'Get-AzDataLakeGen2ItemContent'</span></span>
    - <span data-ttu-id="184db-1547">'Remove-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="184db-1547">'Remove-AzDataLakeGen2Item'</span></span>

## <a name="0100-preview---april-2020"></a><span data-ttu-id="184db-1548">0.10.0-preview - 2020년 4월</span><span class="sxs-lookup"><span data-stu-id="184db-1548">0.10.0-preview - April 2020</span></span>
### <a name="general"></a><span data-ttu-id="184db-1549">일반</span><span class="sxs-lookup"><span data-stu-id="184db-1549">General</span></span>
* <span data-ttu-id="184db-1550">이제 Az 모듈이 Azure Stack Hub에서 미리 보기로 제공됩니다.</span><span class="sxs-lookup"><span data-stu-id="184db-1550">Az modules is now available in preview on Azure Stack Hub.</span></span> <span data-ttu-id="184db-1551">따라서 Linux 및 macOS와의 플랫폼 간 호환성이 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="184db-1551">This allows for cross-platform compatibility with Linux and macOs.</span></span> <span data-ttu-id="184db-1552">Azure Stack Hub는 이제 Az 모듈을 사용하여 PowerShell Core를 지원합니다. 자세한 내용은 [여기](/azure-stack/operator/powershell-install-az-module)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="184db-1552">Azure Stack Hub now supports PowerShell core with the Az modules, more information [here](/azure-stack/operator/powershell-install-az-module)</span></span>
* <span data-ttu-id="184db-1553">Az 모듈은 2019-03-01-hybrid 프로필을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="184db-1553">Az modules support profile 2019-03-01-hybrid:</span></span>
  - <span data-ttu-id="184db-1554">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="184db-1554">Az.Billing</span></span>
  - <span data-ttu-id="184db-1555">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="184db-1555">Az.Compute</span></span>
  - <span data-ttu-id="184db-1556">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="184db-1556">Az.DataBoxEdge</span></span>
  - <span data-ttu-id="184db-1557">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="184db-1557">Az.EventHub</span></span>
  - <span data-ttu-id="184db-1558">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="184db-1558">Az.IotHub</span></span>
  - <span data-ttu-id="184db-1559">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="184db-1559">Az.KeyVault</span></span>
  - <span data-ttu-id="184db-1560">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="184db-1560">Az.Monitor</span></span>
  - <span data-ttu-id="184db-1561">Az.Network</span><span class="sxs-lookup"><span data-stu-id="184db-1561">Az.Network</span></span>
  - <span data-ttu-id="184db-1562">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="184db-1562">Az.Resources</span></span>
  - <span data-ttu-id="184db-1563">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="184db-1563">Az.Storage</span></span>
  - <span data-ttu-id="184db-1564">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="184db-1564">Az.Websites</span></span>
* <span data-ttu-id="184db-1565">Azure Stack Hub와 함께 작동하는 az용 새 PowerShell 모듈 3개(Az.Databox, Az.IotHub 및 Az.EventHub)가 도입되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-1565">Three new PowerShell modules for az have been introduced that work with Azure Stack Hub, which are Az.Databox, Az.IotHub, and Az.EventHub</span></span>
* <span data-ttu-id="184db-1566">AzureRM을 Az로 변경하는 것과 같은 사소한 변경을 수행하면 명령이 비교적 동일하게 유지됩니다.</span><span class="sxs-lookup"><span data-stu-id="184db-1566">Commands remain relatively the same, with minor changes such as changing AzureRM to Az</span></span>
* <span data-ttu-id="184db-1567">Azure Stack Hub에 대한 PowerShell 설명서의 업데이트된 링크는 [여기](/azure-stack/operator/powershell-install-az-module)에서 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-1567">Updated link to PowerShell documentation for Azure Stack Hub can be found [here](/azure-stack/operator/powershell-install-az-module)</span></span>

## <a name="370---march-2020"></a><span data-ttu-id="184db-1568">3.7.0 - 2020년 3월</span><span class="sxs-lookup"><span data-stu-id="184db-1568">3.7.0 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="184db-1569">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="184db-1569">Az.Accounts</span></span>
* <span data-ttu-id="184db-1570">로그인하지 않을 때 'Get-AzTenant'/'Get-AzDefault'/'Set-AzDefault'에서 NullReferenceException이 발생하는 문제가 해결되었습니다. [# 10292]</span><span class="sxs-lookup"><span data-stu-id="184db-1570">Fixed 'Get-AzTenant'/'Get-AzDefault'/'Set-AzDefault' throw NullReferenceException when not login [#10292]</span></span>

#### <a name="azcompute"></a><span data-ttu-id="184db-1571">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="184db-1571">Az.Compute</span></span>
* <span data-ttu-id="184db-1572">'New-AzDiskConfig' cmdlet에 다음 매개 변수를 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-1572">Added the following parameters to 'New-AzDiskConfig' cmdlet:</span></span>
    - <span data-ttu-id="184db-1573">DiskIOPSReadOnly, DiskMBpsReadOnly, MaxSharesCount, GalleryImageReference</span><span class="sxs-lookup"><span data-stu-id="184db-1573">DiskIOPSReadOnly, DiskMBpsReadOnly, MaxSharesCount, GalleryImageReference</span></span>
* <span data-ttu-id="184db-1574">암호화 속성이 'New-AzGalleryImageVersion'cmdlet의 대상 매개 변수에 허용되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-1574">Allowed Encryption property to Target parameter of 'New-AzGalleryImageVersion' cmdlet.</span></span>
* <span data-ttu-id="184db-1575">'Set-AzVmss'-Reimage 및 'Invoke-AzVMReimage'cmdlet에 대한 tempDisk 이슈가 해결되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-1575">Fixed tempDisk issue for 'Set-AzVmss' -Reimage and 'Invoke-AzVMReimage' cmdlets.</span></span> <span data-ttu-id="184db-1576">[#11354]</span><span class="sxs-lookup"><span data-stu-id="184db-1576">[#11354]</span></span>
* <span data-ttu-id="184db-1577">새로운 SAP 확장을 위해 아래 cmdlet에 대한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-1577">Added support to below cmdlets for new SAP Extension</span></span>
    - <span data-ttu-id="184db-1578">'Set-AzVMAEMExtension'</span><span class="sxs-lookup"><span data-stu-id="184db-1578">'Set-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="184db-1579">'Get-AzVMAEMExtension'</span><span class="sxs-lookup"><span data-stu-id="184db-1579">'Get-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="184db-1580">'Remove-AzVMAEMExtension'</span><span class="sxs-lookup"><span data-stu-id="184db-1580">'Remove-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="184db-1581">'Update-AzVMAEMExtension'</span><span class="sxs-lookup"><span data-stu-id="184db-1581">'Update-AzVMAEMExtension'</span></span>
* <span data-ttu-id="184db-1582">도움말 문서의 예제에서 오류가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-1582">Fixed errors in examples of help document</span></span>
* <span data-ttu-id="184db-1583">VM PowerState의 정확한 문자열 값을 테이블 형식으로 표시했습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-1583">Showed the exact string value for VM PowerState in the table format.</span></span>
* <span data-ttu-id="184db-1584">'New-AzVmssConfig': SinglePlacementGroup이 비활성화된 경우 AutomaticRepairs 속성의 직렬화가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-1584">'New-AzVmssConfig': fixed serialization of AutomaticRepairs property when SinglePlacementGroup is disabled.</span></span> <span data-ttu-id="184db-1585">[#11257]</span><span class="sxs-lookup"><span data-stu-id="184db-1585">[#11257]</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="184db-1586">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="184db-1586">Az.DataFactory</span></span>
* <span data-ttu-id="184db-1587">ADF .Net SDK 버전이 4.8.0으로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-1587">Updated ADF .Net SDK version to 4.8.0</span></span>
* <span data-ttu-id="184db-1588">재실행을 지원하기 위해 'Invoke-AzDataFactoryV2Pipeline' 명령에 선택적 매개 변수를 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-1588">Added optional parameters to 'Invoke-AzDataFactoryV2Pipeline' command to support rerun</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="184db-1589">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="184db-1589">Az.DataLakeStore</span></span>
* <span data-ttu-id="184db-1590">'Export-AzDataLakeStoreItem' 및 'Import-AzDataLakeStoreItem'에 대해 호환성이 손상되는 변경 설명을 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-1590">Added breaking change description for 'Export-AzDataLakeStoreItem' and 'Import-AzDataLakeStoreItem'</span></span>
* <span data-ttu-id="184db-1591">'New-AzDataLakeStoreItem', 'Add-AzDAtaLakeStoreItemContent' 및 'Get-AzDAtaLakeStoreItemContent'에 대한 바이트 인코딩 옵션이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-1591">Added option of Byte encoding for 'New-AzDataLakeStoreItem', 'Add-AzDAtaLakeStoreItemContent', and 'Get-AzDAtaLakeStoreItemContent'</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="184db-1592">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="184db-1592">Az.HDInsight</span></span>
* <span data-ttu-id="184db-1593">클러스터 생성 시 최소 지원 TLS 버전 지정이 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="184db-1593">Supported specifying minimal supported TLS version when creating cluster.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="184db-1594">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="184db-1594">Az.IotHub</span></span>
* <span data-ttu-id="184db-1595">디바이스별 분산 설정을 관리하기 위한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-1595">Added support to manage distributed settings per-device.</span></span> <span data-ttu-id="184db-1596">새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-1596">New Cmdlets are:</span></span>
    - <span data-ttu-id="184db-1597">'Get-AzIotHubDistributedTracing'</span><span class="sxs-lookup"><span data-stu-id="184db-1597">'Get-AzIotHubDistributedTracing'</span></span>
    - <span data-ttu-id="184db-1598">'Set-AzIotHubDistributedTracing'</span><span class="sxs-lookup"><span data-stu-id="184db-1598">'Set-AzIotHubDistributedTracing'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="184db-1599">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="184db-1599">Az.KeyVault</span></span>
* <span data-ttu-id="184db-1600">'New-AzKeyVault'에 대해 호환성이 손상되는 변경 속성이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-1600">Added breaking change attributes to 'New-AzKeyVault'</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="184db-1601">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="184db-1601">Az.Monitor</span></span>
* <span data-ttu-id="184db-1602">'New-AzScheduledQueryRuleLogMetricTrigger'에 대한 설명서가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-1602">Updated documentation for 'New-AzScheduledQueryRuleLogMetricTrigger'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="184db-1603">Az.Network</span><span class="sxs-lookup"><span data-stu-id="184db-1603">Az.Network</span></span>
* <span data-ttu-id="184db-1604">교차 테넌트 VirtualHubVnetConnections를 허용하도록 cmdlet이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-1604">Updated cmdlets to allow cross-tenant VirtualHubVnetConnections</span></span>
    - <span data-ttu-id="184db-1605">'New-AzVirtualHubVnetConnection'</span><span class="sxs-lookup"><span data-stu-id="184db-1605">'New-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="184db-1606">'Update-AzVirtualHubVnetConnection'</span><span class="sxs-lookup"><span data-stu-id="184db-1606">'Update-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="184db-1607">'New-AzVirtualHub'</span><span class="sxs-lookup"><span data-stu-id="184db-1607">'New-AzVirtualHub'</span></span>
    - <span data-ttu-id="184db-1608">'Update-AzVirtualHub'</span><span class="sxs-lookup"><span data-stu-id="184db-1608">'Update-AzVirtualHub'</span></span>
* <span data-ttu-id="184db-1609">SQL Management SDK 종속성이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-1609">Removed Sql Management SDK dependency</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="184db-1610">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="184db-1610">Az.PolicyInsights</span></span>
* <span data-ttu-id="184db-1611">오류 메시지가 향상되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-1611">Improved error messages</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="184db-1612">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="184db-1612">Az.RecoveryServices</span></span>
* <span data-ttu-id="184db-1613">Azure Site Recovery는 Azure 디스크 암호화 Virtual Machines에 대한 VM 속성을 다시 보호하고 업데이트하는 기능을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="184db-1613">Azure Site Recovery added support for doing reprotect and updated vm properties for Azure disk encrypted Virtual Machines.</span></span>
* <span data-ttu-id="184db-1614">Azure Site Recovery VmwareToAzure 속성 DR 모니터링이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-1614">Added Azure Site Recovery VmwareToAzure properties DR monitoring</span></span>
* <span data-ttu-id="184db-1615">Azure Backup은 실패한 항목에 대한 정책 업데이트 재시도 지원을 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-1615">Azure Backup added support for retrying policy update for failed items.</span></span>
* <span data-ttu-id="184db-1616">Azure Backup은 백업 및 복원 중에 디스크 제외 설정에 대한 지원을 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-1616">Azure Backup Added support for disk exclusion settings during backup and restore.</span></span>
* <span data-ttu-id="184db-1617">Azure Backup은 AzureFileShare에서 여러 파일/폴더 복원을 위한 지원을 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-1617">Azure Backup Added Support for Restoring Multiple files/folders in AzureFileShare</span></span>
* <span data-ttu-id="184db-1618">Azure Backup은 IaasVM 정책을 업데이트하는 동안 사용자 지정 리소스 그룹 지원에 대한 지원을 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-1618">Azure Backup Added support for User-specified Resourcegroup support while updating IaasVM Policy</span></span>

#### <a name="azresources"></a><span data-ttu-id="184db-1619">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="184db-1619">Az.Resources</span></span>
* <span data-ttu-id="184db-1620">'Get-AzResource -ResourceGroupName -Name -ExpandProperties -ResourceType'이 기본 apiVersion 대신 실제 apiVersion 리소스를 사용하도록 수정했습니다. [# 11267]</span><span class="sxs-lookup"><span data-stu-id="184db-1620">Fixed 'Get-AzResource -ResourceGroupName -Name -ExpandProperties -ResourceType' to use actual apiVersion of resources instead of default apiVersion [#11267]</span></span>
* <span data-ttu-id="184db-1621">오류 시나리오에 대해 correlationId 로깅이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-1621">Added correlationId logging for error scenarios</span></span>
* <span data-ttu-id="184db-1622">작은 설명서가 'Get-AzResourceLock'으로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-1622">Small documentation change to 'Get-AzResourceLock'.</span></span> <span data-ttu-id="184db-1623">예제가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-1623">Added example.</span></span>
* <span data-ttu-id="184db-1624">'Get-AzADUser'의 매개 변수 값에서 작은 따옴표를 이스케이프 처리하였습니다. [# 11317]</span><span class="sxs-lookup"><span data-stu-id="184db-1624">Escaped single quote in parameter value of 'Get-AzADUser' [#11317]</span></span>
* <span data-ttu-id="184db-1625">배포 스크립트('Get-AzDeploymentScript', 'Get-AzDeploymentScriptLog', 'Save-AzDeploymentScriptLog', 'Remove-AzDeploymentScript')에 대한 새로운 cmdlet 추가가 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-1625">Added new cmdlets for Deployment Scripts ('Get-AzDeploymentScript', 'Get-AzDeploymentScriptLog', 'Save-AzDeploymentScriptLog', 'Remove-AzDeploymentScript')</span></span>

#### <a name="azsql"></a><span data-ttu-id="184db-1626">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="184db-1626">Az.Sql</span></span>
* <span data-ttu-id="184db-1627">'Invoke-AzSqlDatabaseFailover'에 읽기 가능한 보조 매개 변수를 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-1627">Added readable secondary parameter to 'Invoke-AzSqlDatabaseFailover'</span></span>
* <span data-ttu-id="184db-1628">'Disable-AzSqlServerActiveDirectoryOnlyAuthentication' cmdlet을 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-1628">Added cmdlet 'Disable-AzSqlServerActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="184db-1629">데이터베이스에서 열을 분류할 때 저장된 민감도 순위입니다.</span><span class="sxs-lookup"><span data-stu-id="184db-1629">Saved sensitivity rank when classifying columns in the database.</span></span>

#### <a name="azsupport"></a><span data-ttu-id="184db-1630">Az.Support</span><span class="sxs-lookup"><span data-stu-id="184db-1630">Az.Support</span></span>
* <span data-ttu-id="184db-1631">'Az.Support' 모듈의 일반 공급</span><span class="sxs-lookup"><span data-stu-id="184db-1631">General availability of 'Az.Support' module</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="184db-1632">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="184db-1632">Az.Websites</span></span>
* <span data-ttu-id="184db-1633">아래의 새로운 cmdlet을 통해 webapp 트래픽 라우팅 규칙을 사용하는 작업에 대한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-1633">Added support for working with webapp Traffic Routing Rules via below new cmdlets</span></span>
    - <span data-ttu-id="184db-1634">'Get-AzWebAppTrafficRouting'</span><span class="sxs-lookup"><span data-stu-id="184db-1634">'Get-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="184db-1635">'Update-AzWebAppTrafficRouting'</span><span class="sxs-lookup"><span data-stu-id="184db-1635">'Update-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="184db-1636">'Add-AzWebAppTrafficRouting'</span><span class="sxs-lookup"><span data-stu-id="184db-1636">'Add-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="184db-1637">'Remove-AzWebAppTrafficRouting'</span><span class="sxs-lookup"><span data-stu-id="184db-1637">'Remove-AzWebAppTrafficRouting'</span></span>

## <a name="361---march-2020"></a><span data-ttu-id="184db-1638">3.6.1 - 2020년 3월</span><span class="sxs-lookup"><span data-stu-id="184db-1638">3.6.1 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="184db-1639">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="184db-1639">Az.Accounts</span></span>
* <span data-ttu-id="184db-1640">'피드백 보내기'에서 Azure PowerShell 설문 조사 페이지가 열립니다[#11020].</span><span class="sxs-lookup"><span data-stu-id="184db-1640">Open Azure PowerShell survey page in 'Send-Feedback' [#11020]</span></span>
* <span data-ttu-id="184db-1641">'오류 해결'에서 Azure PowerShell 설문 조사 URL이 표시됩니다[#11021].</span><span class="sxs-lookup"><span data-stu-id="184db-1641">Display Azure PowerShell survey URL in 'Resolve-Error' [#11021]</span></span>
* <span data-ttu-id="184db-1642">UserAgent에서 Az 버전이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-1642">Added Az version in UserAgent</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="184db-1643">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="184db-1643">Az.ApiManagement</span></span>
* <span data-ttu-id="184db-1644">DeveloperPortal 엔드포인트에서 사용자 지정 도메인을 검색하고 구성하기 위한 지원이 추가되었습니다[#11007].</span><span class="sxs-lookup"><span data-stu-id="184db-1644">Added support for retrieving and configuring Custom Domain on the DeveloperPortal Endpoint [#11007]</span></span>
* <span data-ttu-id="184db-1645">Json 형식의 API 정의를 다운로드하기 위한 'Export-AzApiManagementApi' 지원이 추가되었습니다[#9987].</span><span class="sxs-lookup"><span data-stu-id="184db-1645">'Export-AzApiManagementApi' Added support for downloading Api Definition in Json format [#9987]</span></span>
* <span data-ttu-id="184db-1646">Json 문서에서 OpenApi 3.0 정의를 가져오기 위한 'Import-AzApiManagementApi' 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-1646">'Import-AzApiManagementApi' Added support for importing OpenApi 3.0 definition from Json document</span></span>
* <span data-ttu-id="184db-1647">AAD B2C 공급자에 대한 '로그인 테넌트'를 구성하기 위한 'New-AzApiManagementIdentityProvider' 및 'Set-AzApiManagementIdentityProvider' 지원이 추가되었습니다[#9784].</span><span class="sxs-lookup"><span data-stu-id="184db-1647">'New-AzApiManagementIdentityProvider' and 'Set-AzApiManagementIdentityProvider' Added support for configuring 'Signin Tenant' for AAD B2C Provider [#9784]</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="184db-1648">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="184db-1648">Az.DataLakeStore</span></span>
* <span data-ttu-id="184db-1649">csproj 및 psd1에서 System.Buffers에 대한 참조가 명시적으로 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-1649">Added reference to System.Buffers explicitly in csproj and psd1.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="184db-1650">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="184db-1650">Az.IotHub</span></span>
* <span data-ttu-id="184db-1651">Iot Hub에서 디바이스를 관리하기 위한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-1651">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="184db-1652">새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-1652">New Cmdlets are:</span></span>
    - <span data-ttu-id="184db-1653">'Add-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="184db-1653">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="184db-1654">'Get-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="184db-1654">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="184db-1655">'Remove-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="184db-1655">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="184db-1656">'Set-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="184db-1656">'Set-AzIotHubDevice'</span></span>
* <span data-ttu-id="184db-1657">Iot Hub의 대상 IoT 디바이스에서 모듈을 관리하기 위한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-1657">Added support to manage modules on a target Iot device in an Iot Hub.</span></span> <span data-ttu-id="184db-1658">새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-1658">New Cmdlets are:</span></span>
    - <span data-ttu-id="184db-1659">'Add-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="184db-1659">'Add-AzIotHubModule'</span></span>
    - <span data-ttu-id="184db-1660">'Get-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="184db-1660">'Get-AzIotHubModule'</span></span>
    - <span data-ttu-id="184db-1661">'Remove-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="184db-1661">'Remove-AzIotHubModule'</span></span>
    - <span data-ttu-id="184db-1662">'Set-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="184db-1662">'Set-AzIotHubModule'</span></span>
* <span data-ttu-id="184db-1663">Iot Hub에서 대상 IoT 디바이스에 대한 연결 문자열을 가져오는 cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-1663">Added cmdlet to get the connection string of a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="184db-1664">Iot Hub에서 대상 IoT 디바이스의 모듈에 대한 연결 문자열을 가져오는 cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-1664">Added cmdlet to get the connection string of a module on a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="184db-1665">IoT 디바이스의 부모 디바이스를 가져오거나 설정하기 위한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-1665">Added support to get/set parent device of an IoT device.</span></span> <span data-ttu-id="184db-1666">새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-1666">New Cmdlets are:</span></span>
    - <span data-ttu-id="184db-1667">'Get-AzIotHubDeviceParent'</span><span class="sxs-lookup"><span data-stu-id="184db-1667">'Get-AzIotHubDeviceParent'</span></span>
    - <span data-ttu-id="184db-1668">'Set-AzIotHubDeviceParent'</span><span class="sxs-lookup"><span data-stu-id="184db-1668">'Set-AzIotHubDeviceParent'</span></span>
* <span data-ttu-id="184db-1669">디바이스 부모-자식 관계를 관리하기 위한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-1669">Added support to manage device parent-child relationship.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="184db-1670">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="184db-1670">Az.Monitor</span></span>
* <span data-ttu-id="184db-1671">'Get-AzMetricDefinition'에 대한 출력 값이 수정되었습니다[#9714].</span><span class="sxs-lookup"><span data-stu-id="184db-1671">Fixed output value for 'Get-AzMetricDefinition' [#9714]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="184db-1672">Az.Network</span><span class="sxs-lookup"><span data-stu-id="184db-1672">Az.Network</span></span>
* <span data-ttu-id="184db-1673">SQL Management SDK가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-1673">Updated Sql Management SDK.</span></span>
* <span data-ttu-id="184db-1674">PrivateLinkServiceConnectionState 클래스의 명명 차이 문제가 해결되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-1674">Fixed a naming-difference issue in PrivateLinkServiceConnectionState class.</span></span>
    - <span data-ttu-id="184db-1675">ActionsRequired 필드가 ActionRequired에 매핑됩니다.</span><span class="sxs-lookup"><span data-stu-id="184db-1675">Mapping the field ActionsRequired to ActionRequired.</span></span>
* <span data-ttu-id="184db-1676">PublicNetworkAccess가 'New-AzSqlServer' 및 'Set-AzSqlServer'에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-1676">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>

#### <a name="azresources"></a><span data-ttu-id="184db-1677">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="184db-1677">Az.Resources</span></span>
* <span data-ttu-id="184db-1678">Get-AzRoleAssignment'의 null 참조 버그가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-1678">Fixed for null reference bug in 'Get-AzRoleAssignment'</span></span>
* <span data-ttu-id="184db-1679">'Remove-AzADGroup'에서 '-Force' 및 '-PassThru' 스위치가 선택적으로 표시됩니다[#10849].</span><span class="sxs-lookup"><span data-stu-id="184db-1679">Marked switch '-Force' and '-PassThru' optional in 'Remove-AzADGroup' [#10849]</span></span>
* <span data-ttu-id="184db-1680">'Remove-AzADGroup'에서 'MailNickname'이 반환되지 않는 문제가 해결되었습니다[#11167].</span><span class="sxs-lookup"><span data-stu-id="184db-1680">Fixed issue that 'MailNickname' doesn't return in 'Remove-AzADGroup' [#11167]</span></span>
* <span data-ttu-id="184db-1681">'Remove-AzADGroup' 파이프 작업이 작동하지 않는 문제가 해결되었습니다[#11171].</span><span class="sxs-lookup"><span data-stu-id="184db-1681">Fixed issue that 'Remove-AzADGroup' pipe operation doesn't work [#11171]</span></span>
* <span data-ttu-id="184db-1682">GetAzureRoleAssignmentCommand의 null 참조 버그가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-1682">Fixed for null reference bug in GetAzureRoleAssignmentCommand</span></span>
* <span data-ttu-id="184db-1683">예정된 정책 cmdlet 변경에 대한 호환성이 손상되는 변경 특성이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-1683">Added breaking change attributes for upcoming changes to policy cmdlets</span></span>
* <span data-ttu-id="184db-1684">서버 쪽에서 리소스 그룹 태그 필터링을 수행하도록 'Get-AzResourceGroup'이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-1684">Updated 'Get-AzResourceGroup' to perform resource group tag filtering on server-side</span></span>
* <span data-ttu-id="184db-1685">-ResourceId를 허용하도록 Tag cmdlet이 확장되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-1685">Extended Tag cmdlets to accept -ResourceId</span></span>
    - <span data-ttu-id="184db-1686">Get-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="184db-1686">Get-AzTag -ResourceId</span></span>
    - <span data-ttu-id="184db-1687">New-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="184db-1687">New-AzTag -ResourceId</span></span>
    - <span data-ttu-id="184db-1688">Remove-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="184db-1688">Remove-AzTag -ResourceId</span></span>
* <span data-ttu-id="184db-1689">새 Tag cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-1689">Added new Tag cmdlet</span></span>
    - <span data-ttu-id="184db-1690">Update-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="184db-1690">Update-AzTag -ResourceId</span></span>
* <span data-ttu-id="184db-1691">SDK 3.3.0에서 ScopedDeployment를 가져왔습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-1691">Brought ScopedDeployment from SDK 3.3.0</span></span>

#### <a name="azsql"></a><span data-ttu-id="184db-1692">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="184db-1692">Az.Sql</span></span>
* <span data-ttu-id="184db-1693">PublicNetworkAccess가 'New-AzSqlServer' 및 'Set-AzSqlServer'에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-1693">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>
* <span data-ttu-id="184db-1694">관리형 데이터베이스에 대한 장기 보존 백업 구성에 대한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-1694">Added support for Long Term Retention backup configuration for Managed Databases</span></span>
    - <span data-ttu-id="184db-1695">관리형 데이터베이스에서 LTR 정책을 가져오거나 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="184db-1695">Get/Set LTR policy on a managed database</span></span>
    - <span data-ttu-id="184db-1696">관리형 데이터베이스, 관리형 인스턴스 또는 위치를 기준으로 LTR 백업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="184db-1696">Get LTR backup(s) by managed database, managed instance, or by location</span></span>
    - <span data-ttu-id="184db-1697">LTR 백업을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="184db-1697">Remove an LTR backup</span></span>
    - <span data-ttu-id="184db-1698">LTR 백업을 복원하여 새 관리형 데이터베이스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="184db-1698">Restore an LTR backup to create a new managed database</span></span>
* <span data-ttu-id="184db-1699">MinimalTlsVersion이 New-AzSqlServer 및 Set-AzSqlServer에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-1699">Added MinimalTlsVersion to New-AzSqlServer and Set-AzSqlServer</span></span>
* <span data-ttu-id="184db-1700">MinimalTlsVersion을 New-AzSqlInstance 및 Set-AzSqlInstance에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-1700">Added MinimalTlsVersion to New-AzSqlInstance and Set-AzSqlInstance</span></span>
* <span data-ttu-id="184db-1701">Az.Network에 대한 SQL SDK 버전이 높아졌습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-1701">Bumped SQL SDK version for Az.Network</span></span>

#### <a name="azstorage"></a><span data-ttu-id="184db-1702">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="184db-1702">Az.Storage</span></span>
* <span data-ttu-id="184db-1703">ImmutabilityPolicy에서 AllowProtectedAppendWrite가 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="184db-1703">Supported AllowProtectedAppendWrite in ImmutabilityPolicy</span></span>
    - <span data-ttu-id="184db-1704">'Set-AzRmStorageContainerImmutabilityPolicy'</span><span class="sxs-lookup"><span data-stu-id="184db-1704">'Set-AzRmStorageContainerImmutabilityPolicy'</span></span>
* <span data-ttu-id="184db-1705">이후 릴리스에서 AzureStorageTable 형식 변경에 대한 호환성이 손상되는 변경 경고 메시지가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-1705">Added breaking change warning message for AzureStorageTable type change in a future release</span></span>
    - <span data-ttu-id="184db-1706">'New-AzStorageTable'</span><span class="sxs-lookup"><span data-stu-id="184db-1706">'New-AzStorageTable'</span></span>
    - <span data-ttu-id="184db-1707">'Get-AzStorageTable'</span><span class="sxs-lookup"><span data-stu-id="184db-1707">'Get-AzStorageTable'</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="184db-1708">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="184db-1708">Az.Websites</span></span>
* <span data-ttu-id="184db-1709">'New-AzAppServicePlan' 및 'Set-AzAppServicePlan'에 대한 Tag 매개 변수가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-1709">Added Tag parameter for 'New-AzAppServicePlan' and 'Set-AzAppServicePlan'</span></span>
* <span data-ttu-id="184db-1710">웹 사이트에 사용자 지정 도메인을 추가할 때 예외가 throw되면 cmdlet 실행을 중지합니다.</span><span class="sxs-lookup"><span data-stu-id="184db-1710">Stop cmdlet execution if an exception is thrown when adding a custom domain to a website</span></span>
* <span data-ttu-id="184db-1711">App Service 계획과 동일한 리소스 그룹에 속하지 않는 App Services에 대한 작업을 수행하기 위한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-1711">Added support to perform operations for App Services not in the same resource group as the App Service Plan</span></span>
* <span data-ttu-id="184db-1712">다른 리소스 그룹의 WebApp/Function에 대한 액세스 제한이 적용되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-1712">Applied access restriction to WebApp/Function in different resource groups</span></span>
* <span data-ttu-id="184db-1713">WebAppSlot에 대한 사용자 지정 호스트 이름을 설정하는 문제가 해결되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-1713">Fixed issue to set custom hostnames for WebAppSlots</span></span>

## <a name="350---february-2020"></a><span data-ttu-id="184db-1714">3.5.0 - 2020년 2월</span><span class="sxs-lookup"><span data-stu-id="184db-1714">3.5.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="184db-1715">마지막 주 릴리스 이후의 주요 사항</span><span class="sxs-lookup"><span data-stu-id="184db-1715">Highlights since the last major release</span></span>
* <span data-ttu-id="184db-1716">클라이언트 쪽 원격 분석이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-1716">Updated client side telemetry.</span></span>
* <span data-ttu-id="184db-1717">디바이스 관리를 지원하는 cmdlet이 Az.IotHub에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-1717">Az.IotHub added cmdlets to support to manage devices.</span></span>
* <span data-ttu-id="184db-1718">가용성 그룹 수신기에 대한 cmdlet이 Az.SqlVirtualMachine에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-1718">Az.SqlVirtualMachine added cmdlets for Availability Group Listener.</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="184db-1719">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="184db-1719">Az.Accounts</span></span>
* <span data-ttu-id="184db-1720">SubscriptionId, TenantId 및 실행 시간이 클라이언트 쪽 원격 분석에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-1720">Added SubscriptionId, TenantId, and execution time into data of client side telemetry</span></span>

#### <a name="azautomation"></a><span data-ttu-id="184db-1721">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="184db-1721">Az.Automation</span></span>
* <span data-ttu-id="184db-1722">'New-AzAutomationSoftwareUpdateConfiguration' 참조 설명서의 예제 1에 있는 오타가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-1722">Fixed typo in Example 1 in reference documentation for 'New-AzAutomationSoftwareUpdateConfiguration'</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="184db-1723">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="184db-1723">Az.CognitiveServices</span></span>
* <span data-ttu-id="184db-1724">SDK가 7.0으로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-1724">Updated SDK to 7.0</span></span>
* <span data-ttu-id="184db-1725">서버 응답 본문이 비어 있는 경우 표시되는 오류 메시지가 향상되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-1725">Improved error message when server responses empty body</span></span>

#### <a name="azcompute"></a><span data-ttu-id="184db-1726">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="184db-1726">Az.Compute</span></span>
* <span data-ttu-id="184db-1727">업데이트하는 동안 빈 값이 ProximityPlacementGroupId에 허용되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-1727">Allowed empty value for ProximityPlacementGroupId during update</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="184db-1728">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="184db-1728">Az.FrontDoor</span></span>
* <span data-ttu-id="184db-1729">WAF에서 사용할 수 있는 관리형 규칙 정의를 가져오는 cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-1729">Added cmdlet to get managed rule definitions that can be used in WAF</span></span>

#### <a name="aziothub"></a><span data-ttu-id="184db-1730">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="184db-1730">Az.IotHub</span></span>
* <span data-ttu-id="184db-1731">Iot Hub에서 디바이스를 관리하기 위한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-1731">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="184db-1732">새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-1732">New Cmdlets are:</span></span>
    - <span data-ttu-id="184db-1733">'Add-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="184db-1733">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="184db-1734">'Get-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="184db-1734">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="184db-1735">'Remove-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="184db-1735">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="184db-1736">'Set-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="184db-1736">'Set-AzIotHubDevice'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="184db-1737">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="184db-1737">Az.KeyVault</span></span>
* <span data-ttu-id="184db-1738">Add-AzKeyVaultKey.md에 대해 중복된 텍스트가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-1738">Fixed duplicated text for Add-AzKeyVaultKey.md</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="184db-1739">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="184db-1739">Az.Monitor</span></span>
* <span data-ttu-id="184db-1740">Get-AzLog cmdlet에 대한 설명이 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-1740">Fixed description of the Get-AzLog cmdlet.</span></span>
* <span data-ttu-id="184db-1741">ActionGroupId라는 새 매개 변수가 'New-AzMetricAlertRuleV2' 명령에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-1741">A new parameter called ActionGroupId was added to 'New-AzMetricAlertRuleV2' command.</span></span>
    - <span data-ttu-id="184db-1742">사용자는 ActionGroupId(string) 또는 ActionGorup(ActivityLogAlertActionGroup) 중 하나를 제공할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-1742">The user can provide either ActionGroupId(string) or ActionGorup(ActivityLogAlertActionGroup).</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="184db-1743">Az.Network</span><span class="sxs-lookup"><span data-stu-id="184db-1743">Az.Network</span></span>
* <span data-ttu-id="184db-1744">'New-AzPrivateLinkService' cmdlet의 '-EnableProxyProtocol' 매개 변수에 대한 하나의 추가 매개 변수 메모가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-1744">Added one extra parameter note for parameter '-EnableProxyProtocol' for 'New-AzPrivateLinkService' cmdlet.</span></span>
* <span data-ttu-id="184db-1745">Start-AzVirtualNetworkGatewayConnectionPacketCapture.md 및 Start-AzVirtualnetworkGatewayPacketCapture.md의 FilterData 예제가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-1745">Fixed FilterData example in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="184db-1746">Start-AzVirtualNetworkGatewayConnectionPacketCapture.md 및 Start-AzVirtualnetworkGatewayPacketCapture.md의 모든 내부 및 외부 패킷을 캡처하는 패킷 캡처 예제가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-1746">Added Packet Capture example for capture all inner and outer packets in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="184db-1747">VNet 방화벽에서 Azure Firewall 정책이 지원됩니다</span><span class="sxs-lookup"><span data-stu-id="184db-1747">Supported Azure Firewall Policy on VNet Firewalls</span></span>
    - <span data-ttu-id="184db-1748">새로 추가된 cmdlet이 없습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-1748">No new cmdlets are added.</span></span> <span data-ttu-id="184db-1749">VNet 방화벽에서 방화벽 정책 제한이 완화되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-1749">Relaxing the restriction for firewall policy on VNet firewalls</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="184db-1750">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="184db-1750">Az.RecoveryServices</span></span>
* <span data-ttu-id="184db-1751">SQL Database에 대한 파일로 복원 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-1751">Added Support for Restore-as-files for SQL Databases.</span></span>

#### <a name="azresources"></a><span data-ttu-id="184db-1752">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="184db-1752">Az.Resources</span></span>
* <span data-ttu-id="184db-1753">템플릿 배포 cmdlet이 리팩터링되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-1753">Refactored template deployment cmdlets</span></span>
    - <span data-ttu-id="184db-1754">관리 그룹에서 배포를 관리하는 새 \*-AzManagementGroupDeployment cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-1754">Added new cmdlets for managing deployments at management group: \*-AzManagementGroupDeployment</span></span>
    - <span data-ttu-id="184db-1755">테넌트 범위에서 배포를 관리하는 새 \*-AzTenantDeployment cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-1755">Added new cmdlets for managing deployments at tenant scope: \*-AzTenantDeployment</span></span>
    - <span data-ttu-id="184db-1756">구독 범위에서 구체적으로 작동하도록 \*-AzDeployment cmdlet이 리팩터링되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-1756">Refactored \*-AzDeployment cmdlets to work specifically at subscription scope</span></span>
    - <span data-ttu-id="184db-1757">\*-AzDeployment cmdlet에 대한 \*-AzSubscriptionDeployment 별칭이 만들어졌습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-1757">Created aliases \*-AzSubscriptionDeployment for \*-AzDeployment cmdlets</span></span>
* <span data-ttu-id="184db-1758">'AvailableToOtherTenants' 매개 변수가 설정되지 않는 'Update-AzADApplication'이 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-1758">Fixed 'Update-AzADApplication' when parameter 'AvailableToOtherTenants' is not set</span></span>
* <span data-ttu-id="184db-1759">AmbiguousParameterSetException을 방지하기 위해 ApplicationObjectWithoutCredentialParameterSet이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-1759">Removed ApplicationObjectWithoutCredentialParameterSet to avoid AmbiguousParameterSetException.</span></span>
* <span data-ttu-id="184db-1760">도움말 파일이 다시 생성되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-1760">Regenerated help files</span></span>

#### <a name="azsql"></a><span data-ttu-id="184db-1761">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="184db-1761">Az.Sql</span></span>
* <span data-ttu-id="184db-1762">Managed Instance에서 구독 간 특정 시점 복원에 대한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-1762">Added support for cross subscription point in time restore on Managed Instances.</span></span>
* <span data-ttu-id="184db-1763">기존 SQL Managed Instance 하드웨어 생성 변경에 대한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-1763">Added support for changing existing Sql Managed Instance hardware generation</span></span>
* <span data-ttu-id="184db-1764">'Update-AzSqlServerVulnerabilityAssessmentSetting' 도움말 예제(매개 변수/속성 출력 -EmailAdmins)가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-1764">Fixed 'Update-AzSqlServerVulnerabilityAssessmentSetting' help examples: parameter/property output - EmailAdmins</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="184db-1765">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="184db-1765">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="184db-1766">가용성 그룹 수신기에 대한 cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-1766">Added cmdlets for Availability Group Listener</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="184db-1767">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="184db-1767">Az.StorageSync</span></span>
* <span data-ttu-id="184db-1768">'Invoke-AzStorageSyncCompatibilityCheck'에서 지원되는 문자 세트가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-1768">Updated supported character sets in 'Invoke-AzStorageSyncCompatibilityCheck'.</span></span>

## <a name="340---february-2020"></a><span data-ttu-id="184db-1769">3.4.0 - 2020년 2월</span><span class="sxs-lookup"><span data-stu-id="184db-1769">3.4.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="184db-1770">마지막 주 릴리스 이후의 주요 사항</span><span class="sxs-lookup"><span data-stu-id="184db-1770">Highlights since the last major release</span></span>
* <span data-ttu-id="184db-1771">Az. CosmosDB 초기 버전 0.1.0 출시</span><span class="sxs-lookup"><span data-stu-id="184db-1771">Az.CosmosDB initial version 0.1.0 released</span></span>
* <span data-ttu-id="184db-1772">Az.Network ConnectionMonitor V2 지원 추가</span><span class="sxs-lookup"><span data-stu-id="184db-1772">Az.Network ConnectionMonitor V2 support added</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="184db-1773">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="184db-1773">Az.Accounts</span></span>
* <span data-ttu-id="184db-1774">AzureRmContext.json을 사용할 수 없을 때 컨텍스트 자동 저장 사용 안 함</span><span class="sxs-lookup"><span data-stu-id="184db-1774">Disable context auto saving when AzureRmContext.json not available</span></span>
* <span data-ttu-id="184db-1775">Azure Powershell Common 참조를 1.3.5-preview로 업데이트</span><span class="sxs-lookup"><span data-stu-id="184db-1775">Update the reference to Azure Powershell Common to 1.3.5-preview</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="184db-1776">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="184db-1776">Az.ApiManagement</span></span>
* <span data-ttu-id="184db-1777">**Get-AzApiManagementApiSchema** API와 연결된 Open-Api 스키마 가져오기 수정   https://github.com/Azure/azure-powershell/issues/10626</span><span class="sxs-lookup"><span data-stu-id="184db-1777">**Get-AzApiManagementApiSchema** Fixed getting Open-Api Schema associated with an API   https://github.com/Azure/azure-powershell/issues/10626</span></span>
* <span data-ttu-id="184db-1778">**New-AzApiManagementProduct** _ 및 _ *Set-AzApiManagementProduct*\*</span><span class="sxs-lookup"><span data-stu-id="184db-1778">**New-AzApiManagementProduct** _ and _ *Set-AzApiManagementProduct*\*</span></span>
  - <span data-ttu-id="184db-1779"> https://github.com/Azure/azure-powershell/issues/10472 설명서 수정</span><span class="sxs-lookup"><span data-stu-id="184db-1779">Fix documentation for https://github.com/Azure/azure-powershell/issues/10472</span></span>
* <span data-ttu-id="184db-1780">**Set-AzApiManagementApi** cmdlet을 사용하여 ServiceUrl을 업데이트하는 방법을 보여주는 예제 추가</span><span class="sxs-lookup"><span data-stu-id="184db-1780">**Set-AzApiManagementApi** Added example to show how to update the ServiceUrl using the cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="184db-1781">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="184db-1781">Az.Compute</span></span>
* <span data-ttu-id="184db-1782">VM 이름을 사용하지 않고 Get-AzVM -Status를 수행할 때 제한을 피하기 위해 VM 상태 수를 100개로 제한</span><span class="sxs-lookup"><span data-stu-id="184db-1782">Limit the number of VM status to 100 to avoid throttling when Get-AzVM -Status is performed without VM name.</span></span>
* <span data-ttu-id="184db-1783">Update-AzDiskEncryptionSet cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="184db-1783">Add Update-AzDiskEncryptionSet cmdlet</span></span>
* <span data-ttu-id="184db-1784">다음 cmdlet에 EncryptionType 및 DiskEncryptionSetId 매개 변수 추가:</span><span class="sxs-lookup"><span data-stu-id="184db-1784">Add EncryptionType and DiskEncryptionSetId parameters to the following cmdlets:</span></span>
    - <span data-ttu-id="184db-1785">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="184db-1785">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span></span>
* <span data-ttu-id="184db-1786">Get-AzProximityPlacementGroup cmdlet에 ColocationStatus 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="184db-1786">Add ColocationStatus parameter to Get-AzProximityPlacementGroup cmdlet.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="184db-1787">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="184db-1787">Az.DataFactory</span></span>
* <span data-ttu-id="184db-1788">ADF .Net SDK 버전을 4.7.0으로 업데이트</span><span class="sxs-lookup"><span data-stu-id="184db-1788">Update ADF .Net SDK version to 4.7.0</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="184db-1789">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="184db-1789">Az.DeploymentManager</span></span>
* <span data-ttu-id="184db-1790">리소스에 대한 LIST 작업 추가</span><span class="sxs-lookup"><span data-stu-id="184db-1790">Adds LIST operations for resources</span></span>
* <span data-ttu-id="184db-1791">상태 검사 단계에 대한 작업을 수행하는 기능 추가</span><span class="sxs-lookup"><span data-stu-id="184db-1791">Adds capability for performing operations on Health Check steps</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="184db-1792">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="184db-1792">Az.HDInsight</span></span>
* <span data-ttu-id="184db-1793">AzHDInsightCluster의 문서 오류 수정</span><span class="sxs-lookup"><span data-stu-id="184db-1793">Fix document error of New-AzHDInsightCluster.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="184db-1794">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="184db-1794">Az.KeyVault</span></span>
* <span data-ttu-id="184db-1795">Remove-AzureKeyVault가 새 New-AzureKeyVault와 일관성을 유지하도록 VaultName 특성에 이름 별칭 추가</span><span class="sxs-lookup"><span data-stu-id="184db-1795">Add Name alias to VaultName attribute to make Remove-AzureKeyVault consistent with New-AzureKeyVault.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="184db-1796">Az.Network</span><span class="sxs-lookup"><span data-stu-id="184db-1796">Az.Network</span></span>
* <span data-ttu-id="184db-1797">Set-AzNetworkWatcherConfigFlowLog.md에 트래픽 분석 사용 안 함 시나리오를 보여주는 새 예제 추가</span><span class="sxs-lookup"><span data-stu-id="184db-1797">New example added to Set-AzNetworkWatcherConfigFlowLog.md to demonstrate Traffic Analytics disable scenario.</span></span>
* <span data-ttu-id="184db-1798">Azure Firewall에 관리 IP 구성을 할당하는 지원 추가 - 방화벽에서 관리 트래픽에 사용할 전용 서브넷 및 공용 IP</span><span class="sxs-lookup"><span data-stu-id="184db-1798">Add support for assigning management IP configuration to Azure Firewall - a dedicated subnet and Public IP that the firewall will use for its management traffic</span></span>
    - <span data-ttu-id="184db-1799">New-AzFirewall cmdlet이 업데이트됨:</span><span class="sxs-lookup"><span data-stu-id="184db-1799">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="184db-1800">공용 IP 주소 개체를 허용하는 -ManagementPublicIpAddress 매개 변수(필수 아님) 추가</span><span class="sxs-lookup"><span data-stu-id="184db-1800">Added parameter -ManagementPublicIpAddress (not mandatory) which accepts a Public IP Address object</span></span>
        - <span data-ttu-id="184db-1801">방화벽 개체에 SetManagementIpConfiguration 메서드 추가 - 입력으로 서브넷 및 공용 IP 주소 필요 - 서브넷 이름은 'AzureFirewallManagementSubnet'이어야 함</span><span class="sxs-lookup"><span data-stu-id="184db-1801">Added method SetManagementIpConfiguration on firewall object - requires a subnet and a Public IP address as input - subnet name must be 'AzureFirewallManagementSubnet'</span></span>
* <span data-ttu-id="184db-1802">네트워크 인터페이스 대신 NSG 예제를 보여주도록 AzNetworkSecurityGroup 예제 수정</span><span class="sxs-lookup"><span data-stu-id="184db-1802">Corrected Get-AzNetworkSecurityGroup examples to show examples for NSG's instead of network interfaces.</span></span>
* <span data-ttu-id="184db-1803">리소스 id 완성자가 매개 변수를 완성하지 못하게 방해하던 New-AzVpnSite 명령의 오타 수정</span><span class="sxs-lookup"><span data-stu-id="184db-1803">Fixed typo in New-AzVpnSite command that was preventing resource id completer from completing a parameter.</span></span>
* <span data-ttu-id="184db-1804">Application Gateway의 다시 쓰기 규칙 작업 세트에서 Url 구성에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="184db-1804">Added support for Url Confiugration in Rewrite Rules Action Set in the Application Gateway</span></span>
    - <span data-ttu-id="184db-1805">추가된 새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-1805">New cmdlets added:</span></span>
        - <span data-ttu-id="184db-1806">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="184db-1806">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span></span>
    - <span data-ttu-id="184db-1807">선택적 매개 변수를 사용하도록 Cmdlet 업데이트 - UrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="184db-1807">Cmdlets updated with optional parameter - UrlConfiguration</span></span>
        - <span data-ttu-id="184db-1808">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="184db-1808">New-AzApplicationGatewayRewriteRuleActionSet</span></span>
* <span data-ttu-id="184db-1809">NetworkWatcher ConnectionMonitor 버전 2 리소스에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="184db-1809">Add suppport for NetworkWatcher ConnectionMonitor version 2 resources</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="184db-1810">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="184db-1810">Az.PolicyInsights</span></span>
* <span data-ttu-id="184db-1811">수정할 리소스를 결정하기 전에 규정 준수 평가 지원</span><span class="sxs-lookup"><span data-stu-id="184db-1811">Support evaluating compliance prior to determining what resource to remediate</span></span>
    - <span data-ttu-id="184db-1812">Start-AzPolicyRemediation에 '-ResourceDiscoverMode' 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="184db-1812">Add '-ResourceDiscoverMode' parameter to Start-AzPolicyRemediation</span></span>
* <span data-ttu-id="184db-1813">정책 메타데이터 리소스를 가져오는 Get-AzPolicyMetadata cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="184db-1813">Add Get-AzPolicyMetadata cmdlet for getting policy metadata resources</span></span>
* <span data-ttu-id="184db-1814">API 버전 2019-10-01의 Get-AzPolicyState 및 Get-AzPolicyStateSummary 업데이트</span><span class="sxs-lookup"><span data-stu-id="184db-1814">Updated Get-AzPolicyState and Get-AzPolicyStateSummary for API version 2019-10-01</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="184db-1815">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="184db-1815">Az.RecoveryServices</span></span>
* <span data-ttu-id="184db-1816">복제된 디스크를 제거할 수 있도록 Azure Site Recovery에 지원 추가</span><span class="sxs-lookup"><span data-stu-id="184db-1816">Azure Site Recovery support for removing a replicated disk.</span></span>
* <span data-ttu-id="184db-1817">Recovery Services 자격 증명 모음을 만드는 동안 태그를 추가할 수 있도록 Azure Backup에 지원 추가</span><span class="sxs-lookup"><span data-stu-id="184db-1817">Azure Backup added support for adding tags while creating a Recovery Services Vault.</span></span>

#### <a name="azresources"></a><span data-ttu-id="184db-1818">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="184db-1818">Az.Resources</span></span>
* <span data-ttu-id="184db-1819">컨텍스트 구독을 기본값으로 하는 \*-AzPolicyAssignment cmdlet에서 -Scope를 선택 사항으로 설정</span><span class="sxs-lookup"><span data-stu-id="184db-1819">Make -Scope optional in \*-AzPolicyAssignment cmdlets with default to context subscription</span></span>
* <span data-ttu-id="184db-1820">암호 및 키 자격 증명을 사용하여 ADServicePrincipal을 만드는 예제 추가</span><span class="sxs-lookup"><span data-stu-id="184db-1820">Add examples of creating ADServicePrincipal with password and key credential</span></span>

#### <a name="azsql"></a><span data-ttu-id="184db-1821">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="184db-1821">Az.Sql</span></span>
<span data-ttu-id="184db-1822">DatabaseName 대신 PartnerDatabaseName이 있는지 확인하도록 New-AzSqlDatabaseSecondary cmdlet 수정</span><span class="sxs-lookup"><span data-stu-id="184db-1822">Fix New-AzSqlDatabaseSecondary cmdlet to check for PartnerDatabaseName existence instead of DatabaseName existence.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="184db-1823">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="184db-1823">Az.Storage</span></span>
* <span data-ttu-id="184db-1824">스토리지 계정 만들기에서 테이블/큐 암호화 Keytype 설정 지원</span><span class="sxs-lookup"><span data-stu-id="184db-1824">Support set Table/Queue Encryption Keytype in Create Storage Account</span></span>
    - <span data-ttu-id="184db-1825">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="184db-1825">New-AzStorageAccount</span></span>
* <span data-ttu-id="184db-1826">StorageException에 ExtendedErrorInformation이 없으면 RequestId 표시</span><span class="sxs-lookup"><span data-stu-id="184db-1826">Show RequestId when StorageException don't have ExtendedErrorInformation</span></span>
* <span data-ttu-id="184db-1827">cmdlet Start-AzStorageBlobCopy의 예제 6 수정</span><span class="sxs-lookup"><span data-stu-id="184db-1827">Fix the Example 6 of cmdlet Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="184db-1828">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="184db-1828">Az.Websites</span></span>
* <span data-ttu-id="184db-1829">Set-AzWebapp 및 Set-AzWebappSlot이 AlwaysOn, MinTls 및 FtpsState 속성 지원</span><span class="sxs-lookup"><span data-stu-id="184db-1829">Set-AzWebapp and Set-AzWebappSlot supports AlwaysOn, MinTls and FtpsState properties</span></span>
* <span data-ttu-id="184db-1830">단일 Set-AzWebApp 명령을 사용하여 AppservicePlan을 변경하는 동시에 HttpsOnly를 설정하면 HttpsOnly가 기본값으로 다시 설정되는 문제 수정</span><span class="sxs-lookup"><span data-stu-id="184db-1830">Fixing issue where setting HttpsOnly along with changing AppservicePlan at the same time using the single Set-AzWebApp Command, was resetting HttpsOnly to default value</span></span>

## <a name="330---january-2020"></a><span data-ttu-id="184db-1831">3.3.0 - 2020년 1월</span><span class="sxs-lookup"><span data-stu-id="184db-1831">3.3.0 - January 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="184db-1832">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="184db-1832">Az.Accounts</span></span>
* <span data-ttu-id="184db-1833">AzureAttestationServiceEndpointResourceId 및 AzureAttestationServiceEndpointSuffix 매개 변수를 허용하도록 Add-AzEnvironment 및 Set-AzEnvironment가 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="184db-1833">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameters AzureAttestationServiceEndpointResourceId and AzureAttestationServiceEndpointSuffix</span></span>

#### <a name="azcdn"></a><span data-ttu-id="184db-1834">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="184db-1834">Az.Cdn</span></span>
* <span data-ttu-id="184db-1835">New-AzCdnEndpoint cmdlet에서 오류 응답 세부 정보 표시</span><span class="sxs-lookup"><span data-stu-id="184db-1835">Display error response detail in New-AzCdnEndpoint cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="184db-1836">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="184db-1836">Az.Compute</span></span>
* <span data-ttu-id="184db-1837">OS 프로필이 없는 관리 OD 디스크가 있는 VM의 Set-AzVMCustomScriptExtension cmdlet을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="184db-1837">Fix Set-AzVMCustomScriptExtension cmdlet for a VM with managed OD disk which does not have OS profile.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="184db-1838">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="184db-1838">Az.ContainerInstance</span></span>
* <span data-ttu-id="184db-1839">New-AzContainerGroup의 예에서 사용되는 고정 매개 변수 이름</span><span class="sxs-lookup"><span data-stu-id="184db-1839">Fixed parameter names used by example of New-AzContainerGroup</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="184db-1840">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="184db-1840">Az.DataBoxEdge</span></span>
* <span data-ttu-id="184db-1841">'Get-AzDataBoxEdgeStorageContainer' cmdlet 추가됨</span><span class="sxs-lookup"><span data-stu-id="184db-1841">Added cmdlet 'Get-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="184db-1842">Edge 스토리지 컨테이너 가져오기</span><span class="sxs-lookup"><span data-stu-id="184db-1842">Get the Edge Storage Container</span></span>
* <span data-ttu-id="184db-1843">'New-AzDataBoxEdgeStorageContainer' cmdlet 추가됨</span><span class="sxs-lookup"><span data-stu-id="184db-1843">Added cmdlet 'New-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="184db-1844">새 Edge 스토리지 컨테이너 만들기</span><span class="sxs-lookup"><span data-stu-id="184db-1844">Create new Edge Strorage Container</span></span>
* <span data-ttu-id="184db-1845">'Remove-AzDataBoxEdgeStorageContainer' cmdlet 추가됨</span><span class="sxs-lookup"><span data-stu-id="184db-1845">Added cmdlet 'Remove-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="184db-1846">Edge 스토리지 컨테이너 제거</span><span class="sxs-lookup"><span data-stu-id="184db-1846">Remove the Edge Storage Container</span></span>
* <span data-ttu-id="184db-1847">'Invoke-AzDataBoxEdgeStorageContainer' cmdlet 추가됨</span><span class="sxs-lookup"><span data-stu-id="184db-1847">Added cmdlet 'Invoke-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="184db-1848">Edge 스토리지 컨테이너에서 데이터를 새로 고치는 작업 호출</span><span class="sxs-lookup"><span data-stu-id="184db-1848">Invoke action to refresh data on Edge Storage Container</span></span>
* <span data-ttu-id="184db-1849">'Get-AzDataBoxEdgeStorageAccount' cmdlet 추가됨</span><span class="sxs-lookup"><span data-stu-id="184db-1849">Added cmdlet 'Get-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="184db-1850">Edge 스토리지 계정 가져오기</span><span class="sxs-lookup"><span data-stu-id="184db-1850">Get the Edge Storage Account</span></span>
* <span data-ttu-id="184db-1851">'New-AzDataBoxEdgeStorageAccount' cmdlet 추가됨</span><span class="sxs-lookup"><span data-stu-id="184db-1851">Added cmdlet 'New-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="184db-1852">새 Edge 스토리지 계정 만들기</span><span class="sxs-lookup"><span data-stu-id="184db-1852">Create new Edge Storage Account</span></span>
* <span data-ttu-id="184db-1853">'Remove-AzDataBoxEdgeStorageAccount' cmdlet 추가됨</span><span class="sxs-lookup"><span data-stu-id="184db-1853">Added cmdlet 'Remove-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="184db-1854">Edge 스토리지 계정 제거</span><span class="sxs-lookup"><span data-stu-id="184db-1854">Remove the Edge Storage Account</span></span>
* <span data-ttu-id="184db-1855">'Invoke-AzDataBoxEdgeShare' cmdlet 호출</span><span class="sxs-lookup"><span data-stu-id="184db-1855">Invoke cmdlet 'Invoke-AzDataBoxEdgeShare'</span></span>
  - <span data-ttu-id="184db-1856">공유에서 데이터를 새로 고치는 작업 호출</span><span class="sxs-lookup"><span data-stu-id="184db-1856">Invoke action to refresh data on share</span></span>
* <span data-ttu-id="184db-1857">'Set-AzDataBoxEdgeStorageAccountCredential' cmdlet 추가됨</span><span class="sxs-lookup"><span data-stu-id="184db-1857">Added cmdlet 'Set-AzDataBoxEdgeStorageAccountCredential'</span></span>
  - <span data-ttu-id="184db-1858">az databoxedge 스토리지 계정 자격 증명 설정</span><span class="sxs-lookup"><span data-stu-id="184db-1858">Set the az databoxedge storage account credential</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="184db-1859">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="184db-1859">Az.DataFactory</span></span>
* <span data-ttu-id="184db-1860">Get-AzDataFactoryV2IntegrationRuntime cmd에 AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId 및 VersionStatus 속성 추가</span><span class="sxs-lookup"><span data-stu-id="184db-1860">Add AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId and VersionStatus properties for Get-AzDataFactoryV2IntegrationRuntime cmd</span></span>
* <span data-ttu-id="184db-1861">ADF .Net SDK 버전을 4.6.0으로 업데이트</span><span class="sxs-lookup"><span data-stu-id="184db-1861">Update ADF .Net SDK version to 4.6.0</span></span>
* <span data-ttu-id="184db-1862">고정 공용 IP 주소로 Azure-SSIS IR을 만들 수 있도록 'Set-AzureRmDataFactoryV2IntegrationRuntime'cmd에 대해 'PublicIPs' 매개 변수를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="184db-1862">Add parameter 'PublicIPs' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable create Azure-SSIS IR with static public IP addresses.</span></span>

#### <a name="azdevtestlabs"></a><span data-ttu-id="184db-1863">Az.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="184db-1863">Az.DevTestLabs</span></span>
* <span data-ttu-id="184db-1864">Get-AzDtlAllowedVMSizesPolicy.md에서 끊어진 링크 제거</span><span class="sxs-lookup"><span data-stu-id="184db-1864">Remove the broken link in Get-AzDtlAllowedVMSizesPolicy.md</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="184db-1865">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="184db-1865">Az.EventHub</span></span>
* <span data-ttu-id="184db-1866">10634 문제 해결: eventhubnamespace 제거에 대한 null 개체 참조 수정</span><span class="sxs-lookup"><span data-stu-id="184db-1866">Fix for issue 10634 : Fix the null Object reference for remove eventhubnamespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="184db-1867">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="184db-1867">Az.HDInsight</span></span>
* <span data-ttu-id="184db-1868">Invoke-AzHDInsightHiveJob.md 오류를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="184db-1868">Fix Invoke-AzHDInsightHiveJob.md error.</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="184db-1869">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="184db-1869">Az.MachineLearning</span></span>
* <span data-ttu-id="184db-1870">MachineLearningCompute를 더 이상 사용할 수 없게 되어 아래 cmdlet이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-1870">Removed below cmdlets because MachineLearningCompute is not available any longer</span></span>
  - <span data-ttu-id="184db-1871">Get-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="184db-1871">Get-AzMlOpCluster</span></span>
  - <span data-ttu-id="184db-1872">Get-AzMlOpClusterKey</span><span class="sxs-lookup"><span data-stu-id="184db-1872">Get-AzMlOpClusterKey</span></span>
  - <span data-ttu-id="184db-1873">New-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="184db-1873">New-AzMlOpCluster</span></span>
  - <span data-ttu-id="184db-1874">Remove-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="184db-1874">Remove-AzMlOpCluster</span></span>
  - <span data-ttu-id="184db-1875">Set-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="184db-1875">Set-AzMlOpCluster</span></span>
  - <span data-ttu-id="184db-1876">Test-AzMlOpClusterSystemServicesUpdateAvailability</span><span class="sxs-lookup"><span data-stu-id="184db-1876">Test-AzMlOpClusterSystemServicesUpdateAvailability</span></span>
  - <span data-ttu-id="184db-1877">Update-AzMlOpClusterSystemService</span><span class="sxs-lookup"><span data-stu-id="184db-1877">Update-AzMlOpClusterSystemService</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="184db-1878">Az.Network</span><span class="sxs-lookup"><span data-stu-id="184db-1878">Az.Network</span></span>
* <span data-ttu-id="184db-1879">Microsoft.Azure.Management.Sql의 종속성을 1.36-preview에서 1.37-preview로 업그레이드</span><span class="sxs-lookup"><span data-stu-id="184db-1879">Upgrade dependency of Microsoft.Azure.Management.Sql from 1.36-preview to 1.37-preview</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="184db-1880">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="184db-1880">Az.RecoveryServices</span></span>
* <span data-ttu-id="184db-1881">Azure Site Recovery는 Azure 간 공급자를 위해 고객 관리 키와 함께 유휴 상태에서 암호화된 관리 디스크 vms의 변경을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="184db-1881">Azure Site Recovery change support for managed disk vms encrypted at rest with customer managed keys for Azure to Azure provider.</span></span>
* <span data-ttu-id="184db-1882">Azure Site Recovery는 VMware에서 Azure로를 위해 보호를 사용할 때 선택적 입력으로서 디스크 암호화 집합 ID를 입력하도록 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="184db-1882">Azure Site Recovery support to input disk encryption Set Id as optional input at enabling protection for Vmware to Azure.</span></span>
* <span data-ttu-id="184db-1883">Azure Site Recovery는 VMware에서 Azure로를 위해 보호를 사용하기 위해 디스크 수준의 선택적 입력으로서 디스크 암호화 집합 ID를 입력하도록 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="184db-1883">Azure Site Recovery support to input disk encryption Set Id as optional input at disk level to enable protection for Vmware to Azure.</span></span>
* <span data-ttu-id="184db-1884">Azure Site Recovery는 HyperV에서 Azure로를 위해 디스크 암호화 집합 맵을 사용하여 복제 보호된 항목을 업데이트하도록 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="184db-1884">Azure Site Recovery support to update replication protected item with disk encryption set Map for HyperV to Azure.</span></span>

#### <a name="azresources"></a><span data-ttu-id="184db-1885">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="184db-1885">Az.Resources</span></span>
* <span data-ttu-id="184db-1886">'Remove-AzTag'의 도움말 문서에서 오류를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="184db-1886">Fix an error in help document of 'Remove-AzTag'.</span></span>

#### <a name="azsql"></a><span data-ttu-id="184db-1887">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="184db-1887">Az.Sql</span></span>
* <span data-ttu-id="184db-1888">Azure Database의 마스터 DB에서 작동하도록 취약성 평가 세트 기준 cmdlet 기능을 수정하고 관리형 인스턴스 시스템 데이터베이스에서 이를 제한합니다.</span><span class="sxs-lookup"><span data-stu-id="184db-1888">Fix vulnerability assessment set baseline cmdlets functionality to work on master db for azure database and limit it on managed instance system databases.</span></span>
* <span data-ttu-id="184db-1889">SQL 인스턴스 장애 조치(failover) 그룹을 만들 때 오류 수정</span><span class="sxs-lookup"><span data-stu-id="184db-1889">Fix an error when creating SQL instance failover group</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="184db-1890">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="184db-1890">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="184db-1891">올바른 새 라이선스 형식으로 DR 추가</span><span class="sxs-lookup"><span data-stu-id="184db-1891">Add DR as a new valid License type</span></span>

#### <a name="azstorage"></a><span data-ttu-id="184db-1892">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="184db-1892">Az.Storage</span></span>
* <span data-ttu-id="184db-1893">다음 릴리스에서 DefaultAction Value 변경에 대해 호환성이 손상되는 변경 경고 메시지 추가</span><span class="sxs-lookup"><span data-stu-id="184db-1893">Add breaking change warning message for DefaultAction Value change in a future release</span></span>
    - <span data-ttu-id="184db-1894">Update-AzStorageAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="184db-1894">Update-AzStorageAccountNetworkRuleSet</span></span>
* <span data-ttu-id="184db-1895">-IncludeGeoReplicationStats 매개 변수와 함께 get-AzureRMStorageAccount를 실행하여 스토리지 계정의 마지막 동기화 시간 가져오기 지원</span><span class="sxs-lookup"><span data-stu-id="184db-1895">Support Get last sync time of Storage account by run get-AzureRMStorageAccount with parameter -IncludeGeoReplicationStats</span></span>
    - <span data-ttu-id="184db-1896">Get-AzureRMStorageAccount</span><span class="sxs-lookup"><span data-stu-id="184db-1896">Get-AzureRMStorageAccount</span></span>

## <a name="320---december-2019"></a><span data-ttu-id="184db-1897">3.2.0 - 2019년 12월</span><span class="sxs-lookup"><span data-stu-id="184db-1897">3.2.0 - December 2019</span></span>

### <a name="general"></a><span data-ttu-id="184db-1898">일반</span><span class="sxs-lookup"><span data-stu-id="184db-1898">General</span></span>
* <span data-ttu-id="184db-1899">모든 모듈의 상대 경로를 사용하기 위해 .psd1의 참조 업데이트</span><span class="sxs-lookup"><span data-stu-id="184db-1899">Update references in .psd1 to use relative path for all modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="184db-1900">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="184db-1900">Az.Accounts</span></span>
* <span data-ttu-id="184db-1901">Az 4.0 미리 보기를 위해 클라이언트 측 원격 분석에 대해 UserAgent를 올바르게 설정</span><span class="sxs-lookup"><span data-stu-id="184db-1901">Set correct UserAgent for client-side telemetry for Az 4.0 preview</span></span>
* <span data-ttu-id="184db-1902">Az 4.0 미리 보기에서 컨텍스트가 null인 경우 사용자에게 친숙한 오류 메시지로 표시</span><span class="sxs-lookup"><span data-stu-id="184db-1902">Display user friendly error message when context is null in Az 4.0 preview</span></span>

#### <a name="azbatch"></a><span data-ttu-id="184db-1903">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="184db-1903">Az.Batch</span></span>
* <span data-ttu-id="184db-1904">**New-AzBatchPool** 이 'VirtualMachineConfiguration.ContainerConfiguration' 또는 'VirtualMachineConfiguration.DataDisks'를 서버로 제대로 보내지 않는 [#10602](https://github.com/Azure/azure-powershell/issues/10602) 문제 수정</span><span class="sxs-lookup"><span data-stu-id="184db-1904">Fix issue [#10602](https://github.com/Azure/azure-powershell/issues/10602), where **New-AzBatchPool** did not properly send 'VirtualMachineConfiguration.ContainerConfiguration' or 'VirtualMachineConfiguration.DataDisks' to the server.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="184db-1905">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="184db-1905">Az.DataFactory</span></span>
* <span data-ttu-id="184db-1906">ADF .Net SDK 버전을 4.5.0으로 업데이트</span><span class="sxs-lookup"><span data-stu-id="184db-1906">Update ADF .Net SDK version to 4.5.0</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="184db-1907">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="184db-1907">Az.FrontDoor</span></span>
* <span data-ttu-id="184db-1908">WAF 관리 규칙 제외 지원 추가됨</span><span class="sxs-lookup"><span data-stu-id="184db-1908">Added WAF managed rules exclusion support</span></span>
* <span data-ttu-id="184db-1909">자동 완성에 SocketAddr 추가</span><span class="sxs-lookup"><span data-stu-id="184db-1909">Add SocketAddr to auto-complete</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="184db-1910">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="184db-1910">Az.HealthcareApis</span></span>
* <span data-ttu-id="184db-1911">예외 처리</span><span class="sxs-lookup"><span data-stu-id="184db-1911">Exception Handling</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="184db-1912">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="184db-1912">Az.KeyVault</span></span>
* <span data-ttu-id="184db-1913">잠재적으로 설정되지 않은 오류 액세스 값 수정</span><span class="sxs-lookup"><span data-stu-id="184db-1913">Fixed error accessing value that is potentially not set</span></span>
* <span data-ttu-id="184db-1914">타원 곡선 암호화 인증서 관리</span><span class="sxs-lookup"><span data-stu-id="184db-1914">Elliptic Curve Cryptography Certificate Managment</span></span>
    - <span data-ttu-id="184db-1915">인증서 정책에 대한 곡선 지정을 위한 지원 추가됨</span><span class="sxs-lookup"><span data-stu-id="184db-1915">Added support to specify the Curve for Certificate Policies</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="184db-1916">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="184db-1916">Az.Monitor</span></span>
* <span data-ttu-id="184db-1917">진단 설정 추가 명령에 선택적 인수 추가</span><span class="sxs-lookup"><span data-stu-id="184db-1917">Adding optional argument to the Add Diagnostic Settings command.</span></span> <span data-ttu-id="184db-1918">스위치 인수(있는 경우)는 Log Analytics로 내보내기가 고정 스키마(전용 데이터 유형)가 되어야 함을</span><span class="sxs-lookup"><span data-stu-id="184db-1918">A switch argument that if present indicates that the export to Log Analytics must be to a fixed schema (a.k.a.</span></span> <span data-ttu-id="184db-1919">나타냄</span><span class="sxs-lookup"><span data-stu-id="184db-1919">dedicated, data type)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="184db-1920">Az.Network</span><span class="sxs-lookup"><span data-stu-id="184db-1920">Az.Network</span></span>
* <span data-ttu-id="184db-1921">AzureFirewall 애플리케이션, NAT 및 네트워크 규칙에서 IpGroups 지원.</span><span class="sxs-lookup"><span data-stu-id="184db-1921">Support for IpGroups in AzureFirewall Application,Nat & Network Rules.</span></span>

#### <a name="azresources"></a><span data-ttu-id="184db-1922">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="184db-1922">Az.Resources</span></span>
* <span data-ttu-id="184db-1923">이름이 일부 내장 매개 변수 이름과 충돌하는 경우 템플릿 배포가 템플릿 매개 변수를 읽지 못하는 문제 수정.</span><span class="sxs-lookup"><span data-stu-id="184db-1923">Fix an issue where template deployment fails to read a template parameter if its name conflicts with some built-in parameter name.</span></span>
* <span data-ttu-id="184db-1924">정책 세트 정의 내에 그룹화 지원을 도입하는 새로운 API 버전 2019-09-01을 사용하도록 정책 cmdlet 업데이트.</span><span class="sxs-lookup"><span data-stu-id="184db-1924">Updated policy cmdlets to use new api version 2019-09-01 that introduces grouping support within policy set definitions.</span></span>

#### <a name="azsql"></a><span data-ttu-id="184db-1925">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="184db-1925">Az.Sql</span></span>
* <span data-ttu-id="184db-1926">취약성 평가 자동 활성화에서 스토리지 생성을 StorageV2로 업그레이드</span><span class="sxs-lookup"><span data-stu-id="184db-1926">Upgraded storage creation in Vulnerability Assessment auto enablement to StorageV2</span></span>

#### <a name="azstorage"></a><span data-ttu-id="184db-1927">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="184db-1927">Az.Storage</span></span>
* <span data-ttu-id="184db-1928">Oauth 인증을 기반으로 스토리지 컨텍스트를 사용하여 Blob/컨테이너 ID 기반 SAS 토큰 생성 지원</span><span class="sxs-lookup"><span data-stu-id="184db-1928">Support generate Blob/Constainer Idenity based SAS token with Storage Context based on Oauth authentication</span></span>
    - <span data-ttu-id="184db-1929">New-AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="184db-1929">New-AzStorageContainerSASToken</span></span>
    - <span data-ttu-id="184db-1930">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="184db-1930">New-AzStorageBlobSASToken</span></span>
* <span data-ttu-id="184db-1931">모든 Idenity SAS 토큰을 해지할 수 있도록 스토리지 계정 사용자 위임 키 해지 지원</span><span class="sxs-lookup"><span data-stu-id="184db-1931">Support revoke Storage Account User Delegation Keys, so all Idenity SAS tokens are revoked</span></span>
    - <span data-ttu-id="184db-1932">Revoke-AzStorageAccountUserDelegationKeys</span><span class="sxs-lookup"><span data-stu-id="184db-1932">Revoke-AzStorageAccountUserDelegationKeys</span></span>
* <span data-ttu-id="184db-1933">새로운 API 버전 2019-06-01을 지원하기 위해 Microsoft.Azure.Management.Storage 14.2.0으로 업그레이드.</span><span class="sxs-lookup"><span data-stu-id="184db-1933">Upgrade to Microsoft.Azure.Management.Storage 14.2.0, to support new API version 2019-06-01.</span></span>
* <span data-ttu-id="184db-1934">File Share cmdlet의 관리 평면에서 5120을 초과하는 값에 대해 QuotaGiB(Gibyby의 공유 할당량)를 지원하고 'Quota' 매개 변수 별칭을 'QuotaGiB' 매개 변수에 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-1934">Support of QuotaGiB (Share Quota in Gibibye) for values of more than 5120 in the Management plane of File Share cmdlets and added the 'Quota' parameter alias to the 'QuotaGiB' parameter.</span></span>
    - <span data-ttu-id="184db-1935">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="184db-1935">New-AzRmStorageShare</span></span>
    - <span data-ttu-id="184db-1936">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="184db-1936">Update-AzRmStorageShare</span></span>
* <span data-ttu-id="184db-1937">매개 변수 'Quota'에 매개 변수 별칭 'QuotaGiB' 추가</span><span class="sxs-lookup"><span data-stu-id="184db-1937">Add parameter alias 'QuotaGiB' to parameter 'Quota'</span></span>
    - <span data-ttu-id="184db-1938">Set-AzStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="184db-1938">Set-AzStorageShareQuota</span></span>
* <span data-ttu-id="184db-1939">Set-AzStorageContainerAcl가 저장된 액세스 정책을 정리할 수 있는 문제 수정</span><span class="sxs-lookup"><span data-stu-id="184db-1939">Fix the issue that Set-AzStorageContainerAcl can clean up the stored Access Policy</span></span>
    - <span data-ttu-id="184db-1940">Set-AzStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="184db-1940">Set-AzStorageContainerAcl</span></span>

## <a name="310---november-2019"></a><span data-ttu-id="184db-1941">3.1.0 - 2019년 11월</span><span class="sxs-lookup"><span data-stu-id="184db-1941">3.1.0 - November 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="184db-1942">마지막 주 릴리스 이후의 주요 사항</span><span class="sxs-lookup"><span data-stu-id="184db-1942">Highlights since the last major release</span></span>
* <span data-ttu-id="184db-1943">Az.DataBoxEdge 1.0.0 릴리스됨</span><span class="sxs-lookup"><span data-stu-id="184db-1943">Az.DataBoxEdge 1.0.0 released</span></span>
* <span data-ttu-id="184db-1944">Az.SqlVirtualMachine 1.0.0 릴리스됨</span><span class="sxs-lookup"><span data-stu-id="184db-1944">Az.SqlVirtualMachine 1.0.0 released</span></span>

#### <a name="azcompute"></a><span data-ttu-id="184db-1945">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="184db-1945">Az.Compute</span></span>
* <span data-ttu-id="184db-1946">VM Reapply 기능</span><span class="sxs-lookup"><span data-stu-id="184db-1946">VM Reapply feature</span></span>
    - <span data-ttu-id="184db-1947">Set-AzVM cmdlet에 Reapply 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="184db-1947">Add Reapply parameter to Set-AzVM cmdlet</span></span>
* <span data-ttu-id="184db-1948">VM 확장 집합 AutomaticRepairs 기능:</span><span class="sxs-lookup"><span data-stu-id="184db-1948">VM Scale Set AutomaticRepairs feature:</span></span>
    - <span data-ttu-id="184db-1949">다음 cmdlet에 EnableAutomaticRepair, AutomaticRepairGracePeriod 및 AutomaticRepairMaxInstanceRepairsPercent 매개 변수를 추가합니다.   New-AzVmssConfig   Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="184db-1949">Add EnableAutomaticRepair, AutomaticRepairGracePeriod, and AutomaticRepairMaxInstanceRepairsPercent parameters to the following cmdlets:   New-AzVmssConfig   Update-AzVmss</span></span>
* <span data-ttu-id="184db-1950">New-AzVM에 대한 교차 테넌트 갤러리 이미지 지원</span><span class="sxs-lookup"><span data-stu-id="184db-1950">Cross tenant gallery image support for New-AzVM</span></span>
* <span data-ttu-id="184db-1951">New-AzVM, New-AzVMConfig 및 New-AzVmss cmdlet의 Priority 매개 변수의 인수 완성자에 'Spot' 추가</span><span class="sxs-lookup"><span data-stu-id="184db-1951">Add 'Spot' to the argument completer of Priority parameter in New-AzVM, New-AzVMConfig and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="184db-1952">Add-AzVmssDataDisk cmdlet에 DiskIOPSReadWrite 및 DiskMBpsReadWrite 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="184db-1952">Add DiskIOPSReadWrite and DiskMBpsReadWrite parameters to Add-AzVmssDataDisk cmdlet</span></span>
* <span data-ttu-id="184db-1953">New-AzGalleryImageVersion cmdlet의 SourceImageId 매개 변수를 선택 사항으로 변경</span><span class="sxs-lookup"><span data-stu-id="184db-1953">Change SourceImageId parameter of New-AzGalleryImageVersion cmdlet to optional</span></span>
* <span data-ttu-id="184db-1954">New-AzGalleryImageVersion cmdlet에 OSDiskImage 및 DataDiskImage 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="184db-1954">Add OSDiskImage and DataDiskImage parameters to New-AzGalleryImageVersion cmdlet</span></span>
* <span data-ttu-id="184db-1955">New-AzGalleryImageDefinition cmdlet에 HyperVGeneration 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="184db-1955">Add HyperVGeneration parameter to New-AzGalleryImageDefinition cmdlet</span></span>
* <span data-ttu-id="184db-1956">New-AzVmss, New-AzVmssConfig 및 Update-AzVmss cmdlet에 SkipExtensionsOnOverprovisionedVMs 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="184db-1956">Add SkipExtensionsOnOverprovisionedVMs parameters to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="184db-1957">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="184db-1957">Az.DataBoxEdge</span></span>
* <span data-ttu-id="184db-1958">cmdlet `Get-AzDataBoxEdgeOrder` 추가됨</span><span class="sxs-lookup"><span data-stu-id="184db-1958">Added cmdlet `Get-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="184db-1959">주문 가져오기</span><span class="sxs-lookup"><span data-stu-id="184db-1959">Get the Order</span></span>
* <span data-ttu-id="184db-1960">cmdlet `New-AzDataBoxEdgeOrder` 추가됨</span><span class="sxs-lookup"><span data-stu-id="184db-1960">Added cmdlet `New-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="184db-1961">새 주문 만들기</span><span class="sxs-lookup"><span data-stu-id="184db-1961">Create new Order</span></span>
* <span data-ttu-id="184db-1962">cmdlet `Remove-AzDataBoxEdgeOrder` 추가됨</span><span class="sxs-lookup"><span data-stu-id="184db-1962">Added cmdlet `Remove-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="184db-1963">주문 제거</span><span class="sxs-lookup"><span data-stu-id="184db-1963">Remove the Order</span></span>
* <span data-ttu-id="184db-1964">cmdlet `New-AzDataBoxEdgeShare` 변경</span><span class="sxs-lookup"><span data-stu-id="184db-1964">Change in cmdlet `New-AzDataBoxEdgeShare`</span></span>
    - <span data-ttu-id="184db-1965">이제 로컬 공유를 만듬</span><span class="sxs-lookup"><span data-stu-id="184db-1965">Now creates Local Share</span></span>
* <span data-ttu-id="184db-1966">cmdlet `Set-AzDataBoxEdgeRole` 추가됨</span><span class="sxs-lookup"><span data-stu-id="184db-1966">Added cmdlet `Set-AzDataBoxEdgeRole`</span></span>
    - <span data-ttu-id="184db-1967">이제 IotRole을 공유에 매핑할 수 있음</span><span class="sxs-lookup"><span data-stu-id="184db-1967">Now IotRole can be mapped to Share</span></span>
* <span data-ttu-id="184db-1968">cmdlet `Invoke-AzDataBoxEdgeDevice` 추가됨</span><span class="sxs-lookup"><span data-stu-id="184db-1968">Added cmdlet `Invoke-AzDataBoxEdgeDevice`</span></span>
    - <span data-ttu-id="184db-1969">스캔 업데이트 호출, 업데이트 다운로드, 디바이스에 업데이트 설치</span><span class="sxs-lookup"><span data-stu-id="184db-1969">Invoke scan update, download update, install updates on the device</span></span>
* <span data-ttu-id="184db-1970">cmdlet `Get-AzDataBoxEdgeTrigger` 추가됨</span><span class="sxs-lookup"><span data-stu-id="184db-1970">Added cmdlet `Get-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="184db-1971">트리거에 대한 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="184db-1971">Gets the information about Triggers</span></span>
* <span data-ttu-id="184db-1972">cmdlet `New-AzDataBoxEdgeTrigger` 추가됨</span><span class="sxs-lookup"><span data-stu-id="184db-1972">Added cmdlet `New-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="184db-1973">새 트리거 만들기</span><span class="sxs-lookup"><span data-stu-id="184db-1973">Create new Triggers</span></span>
* <span data-ttu-id="184db-1974">cmdlet `Remove-AzDataBoxEdgeTrigger` 추가됨</span><span class="sxs-lookup"><span data-stu-id="184db-1974">Added cmdlet `Remove-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="184db-1975">트리거 제거</span><span class="sxs-lookup"><span data-stu-id="184db-1975">Remove the Triggers</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="184db-1976">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="184db-1976">Az.DataFactory</span></span>
* <span data-ttu-id="184db-1977">ADF .Net SDK 버전을 4.4.0으로 업데이트</span><span class="sxs-lookup"><span data-stu-id="184db-1977">Update ADF .Net SDK version to 4.4.0</span></span>
* <span data-ttu-id="184db-1978">'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd에 'ExpressCustomSetup' 매개 변수를 추가하여 사용자 지정 설치 스크립트 없이 설치 구성 및 타사 구성 요소를 사용하도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="184db-1978">Add parameter 'ExpressCustomSetup' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable setup configurations and 3rd party components without custom setup script.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="184db-1979">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="184db-1979">Az.DataLakeStore</span></span>
* <span data-ttu-id="184db-1980">Get-AzDataLakeStoreDeletedItem 및 Restore-AzDataLakeStoreDeletedItem의 설명서 업데이트</span><span class="sxs-lookup"><span data-stu-id="184db-1980">Update documentation of Get-AzDataLakeStoreDeletedItem and Restore-AzDataLakeStoreDeletedItem</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="184db-1981">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="184db-1981">Az.EventHub</span></span>
* <span data-ttu-id="184db-1982">10301 문제 해결: SAS 토큰 날짜 형식 수정</span><span class="sxs-lookup"><span data-stu-id="184db-1982">Fix for issue 10301 : Fix the SAS Token date format</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="184db-1983">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="184db-1983">Az.FrontDoor</span></span>
* <span data-ttu-id="184db-1984">Enable-AzFrontDoorCustomDomainHttps 및 New-AzFrontDoorFrontendEndpointObject에 MinimumTlsVersion 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="184db-1984">Add MinimumTlsVersion parameter to Enable-AzFrontDoorCustomDomainHttps and New-AzFrontDoorFrontendEndpointObject</span></span>
* <span data-ttu-id="184db-1985">New-AzFrontDoorHealthProbeSettingObject에 HealthProbeMethod 및 EnabledState 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="184db-1985">Add HealthProbeMethod and EnabledState parameters to New-AzFrontDoorHealthProbeSettingObject</span></span>
* <span data-ttu-id="184db-1986">BackendPoolsSettings 개체를 생성하여 Front Door 생성/업데이트에 전달하는 새 cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="184db-1986">Add new cmdlet to create BackendPoolsSettings objec to pass into creation/update of Front Door</span></span>
    - <span data-ttu-id="184db-1987">New-AzFrontDoorBackendPoolsSettingObject</span><span class="sxs-lookup"><span data-stu-id="184db-1987">New-AzFrontDoorBackendPoolsSettingObject</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="184db-1988">Az.Network</span><span class="sxs-lookup"><span data-stu-id="184db-1988">Az.Network</span></span>
* <span data-ttu-id="184db-1989">'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' 및 'Start-AzVirtualnetworkGatewayPacketCapture.md' FilterData 옵션 예제를 변경합니다.</span><span class="sxs-lookup"><span data-stu-id="184db-1989">Change 'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' and 'Start-AzVirtualnetworkGatewayPacketCapture.md' FilterData option examples.</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="184db-1990">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="184db-1990">Az.PrivateDns</span></span>
* <span data-ttu-id="184db-1991">PrivateDns .net sdk를 버전 1.0.0으로 업데이트함</span><span class="sxs-lookup"><span data-stu-id="184db-1991">Updated PrivateDns .net sdk to version 1.0.0</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="184db-1992">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="184db-1992">Az.RecoveryServices</span></span>
* <span data-ttu-id="184db-1993">보호를 사용하도록 설정할 때 디스크 유형을 선택하도록 Azure Site Recovery 지원</span><span class="sxs-lookup"><span data-stu-id="184db-1993">Azure Site Recovery support to select disk type at enabling protection.</span></span>
* <span data-ttu-id="184db-1994">복구 계획 동작 편집을 위한 Azure Site Recovery 버그 수정</span><span class="sxs-lookup"><span data-stu-id="184db-1994">Azure Site Recovery bug fix for recovery plan action edit.</span></span>
* <span data-ttu-id="184db-1995">파일 스트림 DB를 허용하도록 Azure Backup SQL 복원 지원</span><span class="sxs-lookup"><span data-stu-id="184db-1995">Azure Backup SQL Restore support to accept filestream DBs.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="184db-1996">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="184db-1996">Az.RedisCache</span></span>
* <span data-ttu-id="184db-1997">'New-AzRedisCache' 및 'Set-AzRedisCache' cmdlet에 'MinimumTlsVersion' 매개 변수가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-1997">Added 'MinimumTlsVersion' parameter in 'New-AzRedisCache' and 'Set-AzRedisCache' cmdlets.</span></span> <span data-ttu-id="184db-1998">'Get-AzRedisCache' cmdlet 출력에 'MinimumTlsVersion'도 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-1998">Also, added 'MinimumTlsVersion' in the output of 'Get-AzRedisCache' cmdlet.</span></span>
* <span data-ttu-id="184db-1999">'Set-AzRedisCache' 및 'New-AzRedisCache' cmdlet의 '-Size' 매개 변수에 대한 유효성 검사가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-1999">Added validation on '-Size' parameter for 'Set-AzRedisCache' and 'New-AzRedisCache' cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="184db-2000">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="184db-2000">Az.Resources</span></span>
- <span data-ttu-id="184db-2001">정책 할당에 새로운 EnforcementMode 속성이 있는 새 api 버전 2019-06-01을 사용하도록 정책 cmdlet이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2001">Updated policy cmdlets to use new api version 2019-06-01 that has new EnforcementMode property in policy assignment.</span></span>
- <span data-ttu-id="184db-2002">정책 정의 만들기 도움말 예제가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2002">Updated create policy definition help example</span></span>
- <span data-ttu-id="184db-2003">Remove-AZADServicePrincipal -ServicePrincipalName 버그를 수정하고, 서비스 사용자 이름을 찾을 수 없으면 null 참조를 throw합니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2003">Fix bug Remove-AZADServicePrincipal -ServicePrincipalName, throw null reference when service principal name not found.</span></span>
- <span data-ttu-id="184db-2004">New-AZADServicePrincipal 버그를 수정하고, 테넌트에 구독이 없으면 null 참조를 throw합니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2004">Fix bug New-AZADServicePrincipal, throw null reference when tenant doesn't have any subscription.</span></span>
- <span data-ttu-id="184db-2005">연결된 애플리케이션에만 자격 증명을 추가하도록 New-AzAdServicePrincipal을 변경합니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2005">Change New-AzAdServicePrincipal to add credentials only to associated application.</span></span>

#### <a name="azsql"></a><span data-ttu-id="184db-2006">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="184db-2006">Az.Sql</span></span>
* <span data-ttu-id="184db-2007">데이터베이스 ReadReplicaCount에 대한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2007">Added support for database ReadReplicaCount.</span></span>
* <span data-ttu-id="184db-2008">영역 중복이 설정되지 않은 경우 Set-AzSqlDatabase가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2008">Fixed Set-AzSqlDatabase when zone redundancy not set</span></span>

## <a name="300---november-2019"></a><span data-ttu-id="184db-2009">3.0.0 - 2019년 11월</span><span class="sxs-lookup"><span data-stu-id="184db-2009">3.0.0 - November 2019</span></span>
### <a name="general"></a><span data-ttu-id="184db-2010">일반</span><span class="sxs-lookup"><span data-stu-id="184db-2010">General</span></span>
* <span data-ttu-id="184db-2011">Az.PrivateDns 1.0.0 릴리스</span><span class="sxs-lookup"><span data-stu-id="184db-2011">Az.PrivateDns 1.0.0 released</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="184db-2012">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="184db-2012">Az.Accounts</span></span>
* <span data-ttu-id="184db-2013">'Resolve-Error' 별칭에 사용 중단 메시지를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2013">Add a deprecation message for 'Resolve-Error' alias.</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="184db-2014">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="184db-2014">Az.Advisor</span></span>
* <span data-ttu-id="184db-2015">Get-AzAdvisorRecommendation cmdlet에 새로운 '운영 효율성' 범주가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2015">Added new category 'Operational Excellence' to Get-AzAdvisorRecommendation cmdlet.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="184db-2016">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="184db-2016">Az.Batch</span></span>
* <span data-ttu-id="184db-2017">`BatchAccountContext`의 `CoreQuota` 이름이 `DedicatedCoreQuota`로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2017">Renamed `CoreQuota` on `BatchAccountContext` to `DedicatedCoreQuota`.</span></span> <span data-ttu-id="184db-2018">또한 `LowPriorityCoreQuota`가 새로 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2018">There is also a new `LowPriorityCoreQuota`.</span></span>
  - <span data-ttu-id="184db-2019">이 변경 사항은 **Get-AzBatchAccount** 에 영향을 줍니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2019">This impacts **Get-AzBatchAccount**.</span></span>
* <span data-ttu-id="184db-2020">이제 **New-AzBatchTask** `-ResourceFile` 매개 변수는 새로운 **New-AzBatchResourceFile** cmdlet을 사용하여 구성할 수 있는 `PSResourceFile` 개체의 컬렉션을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2020">**New-AzBatchTask** `-ResourceFile` parameter now takes a collection of `PSResourceFile` objects, which can be constructed using the new **New-AzBatchResourceFile** cmdlet.</span></span>
* <span data-ttu-id="184db-2021">새로운 **New-AzBatchResourceFile** cmdlet을 통해 `PSResourceFile` 개체를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2021">New **New-AzBatchResourceFile** cmdlet to help create `PSResourceFile` objects.</span></span> <span data-ttu-id="184db-2022">이들은 `-ResourceFile` 매개 변수의 **New-AzBatchTask** 에 제공될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2022">These can be supplied to **New-AzBatchTask** on the `-ResourceFile` parameter.</span></span>
  - <span data-ttu-id="184db-2023">그에 따라 기존 `HttpUrl` 방법 외에도 두 가지 종류의 리소스 파일이 새롭게 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2023">This supports two new kinds of resource file in addition to the existing `HttpUrl` way:</span></span>
    - <span data-ttu-id="184db-2024">`AutoStorageContainerName` 기반 리소스 파일은 전체 자동 스토리지 컨테이너를 일괄 처리 노드에 다운로드합니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2024">`AutoStorageContainerName` based resource files download an entire auto-storage container to the Batch node.</span></span>
    - <span data-ttu-id="184db-2025">`StorageContainerUrl` 기반 리소스 파일은 URL에 지정된 컨테이너를 일괄 처리 노드에 다운로드합니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2025">`StorageContainerUrl` based resource files download the container specified in the URL to the Batch node.</span></span>
* <span data-ttu-id="184db-2026">**Get-AzBatchApplication** 으로 반환되는 `PSApplication`의 `ApplicationPackages` 속성이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2026">Removed `ApplicationPackages` property of `PSApplication` returned by **Get-AzBatchApplication**.</span></span>
  - <span data-ttu-id="184db-2027">이제 **Get-AzBatchApplicationPackage** 를 사용하여 애플리케이션 내부의 특정 패키지를 검색할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2027">The specific packages inside of an application now can be retrieved using **Get-AzBatchApplicationPackage**.</span></span> <span data-ttu-id="184db-2028">예: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`</span><span class="sxs-lookup"><span data-stu-id="184db-2028">For example: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span></span>
* <span data-ttu-id="184db-2029">**Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication** 및 **Set-AzBatchApplication** 에서 `ApplicationId` 이름이 `ApplicationName`으로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2029">Renamed `ApplicationId` to `ApplicationName` on **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication**, and **Set-AzBatchApplication**.</span></span>
  - <span data-ttu-id="184db-2030">이제 `ApplicationId`는 `ApplicationName`의 별칭입니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2030">`ApplicationId` now is an alias of `ApplicationName`.</span></span>
* <span data-ttu-id="184db-2031">새로운 `PSWindowsUserConfiguration` 속성이 `PSUserAccount`에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2031">Added new `PSWindowsUserConfiguration` property to `PSUserAccount`.</span></span>
* <span data-ttu-id="184db-2032">`PSApplicationPackage`에서 `Version` 이름이 `Name`으로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2032">Renamed `Version` to `Name` on `PSApplicationPackage`.</span></span>
* <span data-ttu-id="184db-2033">`PSResourceFile`에서 `BlobSource` 이름이 `HttpUrl`으로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2033">Renamed `BlobSource` to `HttpUrl` on `PSResourceFile`.</span></span>
* <span data-ttu-id="184db-2034">`PSVirtualMachineConfiguration`에서 `OSDisk` 속성이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2034">Removed `OSDisk` property from `PSVirtualMachineConfiguration`.</span></span>
* <span data-ttu-id="184db-2035">**Set-AzBatchPoolOSVersion** 이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2035">Removed **Set-AzBatchPoolOSVersion**.</span></span> <span data-ttu-id="184db-2036">이 작업은 더 이상 지원되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2036">This operation is no longer supported.</span></span>
* <span data-ttu-id="184db-2037">`PSCloudServiceConfiguration`에서 `TargetOSVersion`이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2037">Removed `TargetOSVersion` from `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="184db-2038">`PSCloudServiceConfiguration`에서 `CurrentOSVersion` 이름이 `OSVersion`으로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2038">Renamed `CurrentOSVersion` to `OSVersion` on `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="184db-2039">`PSPoolUsageMetrics`에서 `DataEgressGiB` 및 `DataIngressGiB`가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2039">Removed `DataEgressGiB` and `DataIngressGiB` from `PSPoolUsageMetrics`.</span></span>
* <span data-ttu-id="184db-2040">**Get-AzBatchNodeAgentSku** 가 제거되고 **Get-AzBatchSupportedImage** 로 대체되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2040">Removed **Get-AzBatchNodeAgentSku** and replaced it with  **Get-AzBatchSupportedImage**.</span></span>
  - <span data-ttu-id="184db-2041">**Get-AzBatchSupportedImage** 가 **Get-AzBatchNodeAgentSku** 와 동일한 데이터를 반환하지만 더 친숙한 형식이 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2041">**Get-AzBatchSupportedImage** returns the same data as **Get-AzBatchNodeAgentSku** but in a more friendly format.</span></span>
  - <span data-ttu-id="184db-2042">이제 확인되지 않은 이미지도 새롭게 반환됩니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2042">New non-verified images are also now returned.</span></span> <span data-ttu-id="184db-2043">각 이미지의 `Capabilities` 및 `BatchSupportEndOfLife`에 대한 추가 정보도 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2043">Additional information about `Capabilities` and `BatchSupportEndOfLife` for each image is also included.</span></span>
* <span data-ttu-id="184db-2044">**New-AzBatchPool** 의 새로운 `MountConfiguration` 매개 변수를 통해 풀의 각 노드에서 원격 파일 시스템을 마운트할 수 있는 기능이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2044">Added ability to mount remote file-systems on each node of a pool via the new `MountConfiguration` parameter of **New-AzBatchPool**.</span></span>
* <span data-ttu-id="184db-2045">이제 트래픽의 소스 포트를 기준으로 풀에 대한 네트워크 액세스를 차단하는 네트워크 보안 규칙이 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2045">Now support network security rules blocking network access to a pool based on the source port of the traffic.</span></span> <span data-ttu-id="184db-2046">이 작업은 `PSNetworkSecurityGroupRule`에서 `SourcePortRanges` 속성을 통해 수행됩니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2046">This is done via the `SourcePortRanges` property on `PSNetworkSecurityGroupRule`.</span></span>
* <span data-ttu-id="184db-2047">컨테이너를 실행할 때 Batch는 이제 컨테이너 작업 디렉터리 또는 일괄 처리 태스크 작업 디렉터리에서 작업 실행을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2047">When running a container, Batch now supports executing the task in the container working directory or in the Batch task working directory.</span></span> <span data-ttu-id="184db-2048">이 작업은 `PSTaskContainerSettings`에서 `WorkingDirectory` 속성에 의해 제어됩니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2048">This is controlled by the `WorkingDirectory` property on `PSTaskContainerSettings`.</span></span>
* <span data-ttu-id="184db-2049">새로운 `PublicIPs` 속성을 통해 `PSNetworkConfiguration`에서 공용 IP의 컬렉션을 지정할 수 있는 기능이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2049">Added ability to specify a collection of public IPs on `PSNetworkConfiguration` via the new `PublicIPs` property.</span></span> <span data-ttu-id="184db-2050">그 결과 사용자 제공 IP 목록의 IP가 풀에 있는 노드에 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2050">This guarantees nodes in the Pool will have an IP from the list user provided IPs.</span></span>
* <span data-ttu-id="184db-2051">지정하지 않은 경우 이제 `PSSTartTask`에서 `WaitForSuccess`의 기본값은 `$True`입니다(이전에는 `$False`).</span><span class="sxs-lookup"><span data-stu-id="184db-2051">When not specified, the default value of `WaitForSuccess` on `PSSTartTask` is now `$True` (was `$False`).</span></span>
* <span data-ttu-id="184db-2052">지정하지 않은 경우 이제 `PSAutoUserSpecification`에서 `Scope`의 기본값은 `Pool`입니다(이전에는 Windows의 경우 `Task`, Linux의 경우에는 `Pool`).</span><span class="sxs-lookup"><span data-stu-id="184db-2052">When not specified, the default value of `Scope` on `PSAutoUserSpecification` is now `Pool` (was `Task` on Windows and `Pool` on Linux).</span></span>

#### <a name="azcdn"></a><span data-ttu-id="184db-2053">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="184db-2053">Az.Cdn</span></span>
* <span data-ttu-id="184db-2054">RulesEngine에 UrlRewriteAction 및 CacheKeyQueryStringAction이 도입되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2054">Introduced UrlRewriteAction and CacheKeyQueryStringAction to RulesEngine.</span></span>
* <span data-ttu-id="184db-2055">New-AzDeliveryRuleCondition cmdlet에서 'Selector' 입력 누락과 같은 여러 버그가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2055">Fixed several bugs like missing 'Selector' Input in New-AzDeliveryRuleCondition cmdlet.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="184db-2056">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="184db-2056">Az.Compute</span></span>
* <span data-ttu-id="184db-2057">디스크 암호화 집합 기능</span><span class="sxs-lookup"><span data-stu-id="184db-2057">Disk Encryption Set feature</span></span>
    - <span data-ttu-id="184db-2058">새 cmdlet:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="184db-2058">New cmdlets:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span></span>
    - <span data-ttu-id="184db-2059">DiskEncryptionSetId 매개 변수가 다음 cmdlet에 추가되었습니다.   Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="184db-2059">DiskEncryptionSetId parameter is added to the following cmdlets:   Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span></span>
    - <span data-ttu-id="184db-2060">DiskEncryptionSetId 및 EncryptionType 매개 변수가 다음 cmdlet에 추가되었습니다.   New-AzDiskConfig   New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="184db-2060">DiskEncryptionSetId and EncryptionType parameters are added to the following cmdlets:   New-AzDiskConfig   New-AzSnapshotConfig</span></span>
* <span data-ttu-id="184db-2061">New-AzVmssIPConfig에 PublicIPAddressVersion 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="184db-2061">Add PublicIPAddressVersion parameter to New-AzVmssIPConfig</span></span>
* <span data-ttu-id="184db-2062">사용자 지정 스크립트 확장의 FileUris를 공용 설정에서 보호된 설정으로 이동</span><span class="sxs-lookup"><span data-stu-id="184db-2062">Move FileUris of custom script extension from public setting to protected setting</span></span>
* <span data-ttu-id="184db-2063">New-AzVmss, New-AzVmssConfig 및 Update-AzVmss cmdlet에 ScaleInPolicy 추가</span><span class="sxs-lookup"><span data-stu-id="184db-2063">Add ScaleInPolicy to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>
* <span data-ttu-id="184db-2064">주요 변경 내용</span><span class="sxs-lookup"><span data-stu-id="184db-2064">Breaking changes</span></span>
    - <span data-ttu-id="184db-2065">CreateOption이 업로드일 때 UploadSizeInBytes 매개 변수가 New-AzDiskConfig에 대해 DiskSizeGB 대신 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2065">UploadSizeInBytes parameter is used instead of DiskSizeGB for New-AzDiskConfig when CreateOption is Upload</span></span>
    - <span data-ttu-id="184db-2066">GalleryImageVersion 개체에서 PublishingProfile.Source.ManagedImage.Id가 StorageProfile.Source.Id로 바뀝니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2066">PublishingProfile.Source.ManagedImage.Id is replaced with StorageProfile.Source.Id in GalleryImageVersion object</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="184db-2067">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="184db-2067">Az.DataFactory</span></span>
* <span data-ttu-id="184db-2068">ADF .Net SDK 버전을 4.3.0으로 업데이트</span><span class="sxs-lookup"><span data-stu-id="184db-2068">Update ADF .Net SDK version to 4.3.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="184db-2069">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="184db-2069">Az.DataLakeStore</span></span>
* <span data-ttu-id="184db-2070">ADLS SDK 버전 업데이트(https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha) , 다음 수정 사항 제공</span><span class="sxs-lookup"><span data-stu-id="184db-2070">Update ADLS SDK version (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), brings following fixes</span></span>
* <span data-ttu-id="184db-2071">휴지통 또는 디렉터리 항목의 creationtime을 역직렬화할 수 없을 때 예외가 발생하지 않도록 방지합니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2071">Avoid throwing exception while unable to deserialize the creationtime of the trash or directory entry.</span></span>
* <span data-ttu-id="184db-2072">adlsclient에서 요청별 시간 제한 설정 노출</span><span class="sxs-lookup"><span data-stu-id="184db-2072">Expose setting per request timeout in adlsclient</span></span>
* <span data-ttu-id="184db-2073">badoffset 복구를 위한 원본 syncflag 전달 수정</span><span class="sxs-lookup"><span data-stu-id="184db-2073">Fix passing the original syncflag for badoffset recovery</span></span>
* <span data-ttu-id="184db-2074">응답이 확인된 후 연속 토큰을 검색하기 위한 EnumerateDirectory 수정</span><span class="sxs-lookup"><span data-stu-id="184db-2074">Fix EnumerateDirectory to retrieve continuation token once response is checked</span></span>
* <span data-ttu-id="184db-2075">Concat 버그 수정</span><span class="sxs-lookup"><span data-stu-id="184db-2075">Fix Concat Bug</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="184db-2076">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="184db-2076">Az.FrontDoor</span></span>
* <span data-ttu-id="184db-2077">모듈 간 기타 오타가 수정됨</span><span class="sxs-lookup"><span data-stu-id="184db-2077">Fixed miscellaneous typos across module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="184db-2078">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="184db-2078">Az.HDInsight</span></span>
* <span data-ttu-id="184db-2079">ADLSGen1 스토리지가 포함된 클러스터를 가져오기 위해 Get-AzHDInsightCluster를 사용할 때 고객에게 '올바른 Base-64 문자열이 아닙니다' 오류가 표시되는 버그가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2079">Fixed the bug that customer will get 'Not a valid Base-64 string' error when using Get-AzHDInsightCluster to get the cluster with ADLSGen1 storage.</span></span>
* <span data-ttu-id="184db-2080">고객이 Azure Data Lake에 액세스하기 위해 서비스 주체 애플리케이션 ID를 제공할 수 있도록 세 가지 cmdlet Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig 및 New-AzHDInsightCluster에 이름이 'ApplicationId'인 매개 변수를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2080">Add a parameter named 'ApplicationId' to three cmdlets Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig and New-AzHDInsightCluster so that customer can provide the service principal application id for accessing Azure Data Lake.</span></span>
* <span data-ttu-id="184db-2081">Microsoft.Azure.Management.HDInsight가 2.1.0에서 5.1.0으로 변경됨</span><span class="sxs-lookup"><span data-stu-id="184db-2081">Changed Microsoft.Azure.Management.HDInsight from 2.1.0 to 5.1.0</span></span>
* <span data-ttu-id="184db-2082">다음 5가지 cmdlet이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2082">Removed five cmdlets:</span></span>
    - <span data-ttu-id="184db-2083">Get-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="184db-2083">Get-AzHDInsightOMS</span></span>
    - <span data-ttu-id="184db-2084">Enable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="184db-2084">Enable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="184db-2085">Disable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="184db-2085">Disable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="184db-2086">Grant-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="184db-2086">Grant-AzHDInsightRdpServicesAccess</span></span>
    - <span data-ttu-id="184db-2087">Revoke-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="184db-2087">Revoke-AzHDInsightRdpServicesAccess</span></span>
* <span data-ttu-id="184db-2088">다음 3가지 cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2088">Added three cmdlets:</span></span>
    - <span data-ttu-id="184db-2089">Get-AzHDInsightOMS 대신 Get-AzHDInsightMonitoring</span><span class="sxs-lookup"><span data-stu-id="184db-2089">Get-AzHDInsightMonitoring to replace Get-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="184db-2090">Get-AzHDInsightOMS 대신 Get-AzHDInsightMonitoring</span><span class="sxs-lookup"><span data-stu-id="184db-2090">Enable-AzHDInsightMonitoring to replace Enable-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="184db-2091">Disable-AzHDInsightOMS 대신 Disable-AzHDInsightMonitoring</span><span class="sxs-lookup"><span data-stu-id="184db-2091">Disable-AzHDInsightMonitoring to replace Disable-AzHDInsightOMS.</span></span>
* <span data-ttu-id="184db-2092">특정 위치의 기능 정보 가져오기를 지원하도록 cmdlet Get-AzHDInsightProperties가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2092">Fixed cmdlet Get-AzHDInsightProperties to support get capabilities information from a specific location.</span></span>
* <span data-ttu-id="184db-2093">Add-AzHDInsightConfigValue에서 매개 변수 집합('Spark1', 'Spark2')이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2093">Removed parameter sets('Spark1', 'Spark2') from Add-AzHDInsightConfigValue.</span></span>
* <span data-ttu-id="184db-2094">cmdlet Add-AzHDInsightSecurityProfile의 도움말 문서에 예제를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2094">Add examples to the help documents of cmdlet Add-AzHDInsightSecurityProfile.</span></span>
* <span data-ttu-id="184db-2095">다음 cmdlet의 출력 유형이 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2095">Changed output type of the following cmdlets:</span></span>
*  - <span data-ttu-id="184db-2096">Get-AzHDInsightProperties의 출력 유형이 CapabilitiesResponse에서 AzureHDInsightCapabilities로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2096">Changed the output type of Get-AzHDInsightProperties from  CapabilitiesResponse to AzureHDInsightCapabilities.</span></span>
*  - <span data-ttu-id="184db-2097">Remove-AzHDInsightCluster의 출력 유형이 ClusterGetResponse에서 bool로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2097">Changed the output type of Remove-AzHDInsightCluster from ClusterGetResponse to bool.</span></span>
*  - <span data-ttu-id="184db-2098">Set-AzHDInsightGatewaySettings의 출력 유형이 HttpConnectivitySettings에서 GatewaySettings로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2098">Changed the output type of Set-AzHDInsightGatewaySettings HttpConnectivitySettings to GatewaySettings.</span></span>
* <span data-ttu-id="184db-2099">몇 가지 시나리오 테스트 사례가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2099">Added some scenario test cases.</span></span>
* <span data-ttu-id="184db-2100">일부 별칭 제거: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span><span class="sxs-lookup"><span data-stu-id="184db-2100">Remove some alias: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="184db-2101">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="184db-2101">Az.IotHub</span></span>
* <span data-ttu-id="184db-2102">주요 변경 내용:</span><span class="sxs-lookup"><span data-stu-id="184db-2102">Breaking changes:</span></span>
    - <span data-ttu-id="184db-2103">'Add-AzIotHubEventHubConsumerGroup' cmdlet이 'EventHubEndpointName' 매개 변수를 더 이상 지원하지 않으며 원래 매개 변수 이름에 대해 별칭을 찾을 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2103">The cmdlet 'Add-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="184db-2104">'Add-AzIotHubEventHubConsumerGroup' cmdlet에 대한 매개 변수 집합 '__AllParameterSets'가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2104">The parameter set '__AllParameterSets' for cmdlet 'Add-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="184db-2105">'Get-AzIotHubEventHubConsumerGroup' cmdlet이 'EventHubEndpointName' 매개 변수를 더 이상 지원하지 않으며 원래 매개 변수 이름에 대해 별칭을 찾을 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2105">The cmdlet 'Get-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="184db-2106">'Get-AzIotHubEventHubConsumerGroup' cmdlet에 대한 매개 변수 집합 '__AllParameterSets'가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2106">The parameter set '__AllParameterSets' for cmdlet 'Get-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="184db-2107">'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' 유형의 'OperationsMonitoringProperties' 속성이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2107">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' has been removed.</span></span>
    - <span data-ttu-id="184db-2108">'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' 유형의 'OperationsMonitoringProperties' 속성이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2108">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' has been removed.</span></span>
    - <span data-ttu-id="184db-2109">'New-AzIotHubExportDevice' cmdlet이 더 이상 'New-AzIotHubExportDevices' 별칭을 지원하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2109">The cmdlet 'New-AzIotHubExportDevice' no longer supports the alias 'New-AzIotHubExportDevices'.</span></span>
    - <span data-ttu-id="184db-2110">'New-AzIotHubImportDevice' cmdlet이 더 이상 'New-AzIotHubImportDevices' 별칭을 지원하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2110">The cmdlet 'New-AzIotHubImportDevice' no longer supports the alias 'New-AzIotHubImportDevices'.</span></span>
    - <span data-ttu-id="184db-2111">'Remove-AzIotHubEventHubConsumerGroup' cmdlet이 'EventHubEndpointName' 매개 변수를 더 이상 지원하지 않으며 원래 매개 변수 이름에 대해 별칭을 찾을 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2111">The cmdlet 'Remove-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="184db-2112">'Remove-AzIotHubEventHubConsumerGroup' cmdlet에 대한 매개 변수 집합 '__AllParameterSets'가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2112">The parameter set '__AllParameterSets' for cmdlet 'Remove-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="184db-2113">'Set-AzIotHub' cmdlet이 'OperationsMonitoringProperties' 매개 변수를 더 이상 지원하지 않으며 원래 매개 변수 이름에 대해 별칭을 찾을 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2113">The cmdlet 'Set-AzIotHub' no longer supports the parameter 'OperationsMonitoringProperties' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="184db-2114">'Set-AzIotHub' cmdlet에 대한 매개 변수 집합 'UpdateOperationsMonitoringProperties'가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2114">The parameter set 'UpdateOperationsMonitoringProperties' for cmdlet 'Set-AzIotHub' has been removed.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="184db-2115">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="184db-2115">Az.RecoveryServices</span></span>
* <span data-ttu-id="184db-2116">Azure Site Recovery가 Azure-Azure를 위한 NSG, 공용 IP 및 내부 부하 분산 장치와 같은 네트워킹 리소스 구성을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2116">Azure Site Recovery support to configure networking resources like NSG, public IP and internal load balancers for Azure to Azure.</span></span>
* <span data-ttu-id="184db-2117">Azure Site Recovery가 vMWare-Azure를 위한 관리 디스크에 쓰기를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2117">Azure Site Recovery Support to write to managed disk for vMWare to Azure.</span></span>
* <span data-ttu-id="184db-2118">Azure Site Recovery가 vMWare-Azure를 위한 NIC 감소를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2118">Azure Site Recovery Support to NIC reduction for vMWare to Azure.</span></span>
* <span data-ttu-id="184db-2119">Azure Site Recovery가 Azure-Azure를 위한 가속 네트워킹을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2119">Azure Site Recovery Support to accelerated networking for Azure to Azure.</span></span>
* <span data-ttu-id="184db-2120">Azure Site Recovery가 Azure-Azure를 위한 에이전트 자동 업데이트를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2120">Azure Site Recovery Support to agent auto update for Azure to Azure.</span></span>
* <span data-ttu-id="184db-2121">Azure Site Recovery가 Azure-Azure를 위한 표준 SSD를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2121">Azure Site Recovery Support to Standard SSD for Azure to Azure.</span></span>
* <span data-ttu-id="184db-2122">Azure Site Recovery가 Azure-Azure를 위한 두 가지 Azure 디스크 암호화 전달을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2122">Azure Site Recovery Support to Azure Disk Encryption two pass for Azure to Azure.</span></span>
* <span data-ttu-id="184db-2123">Azure Site Recovery가 Azure-Azure를 위한 새로 추가된 디스크 보호를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2123">Azure Site Recovery Support to protect newly added disk for Azure to Azure.</span></span>
* <span data-ttu-id="184db-2124">VM을 위한 SoftDelete 기능 및 softdelete를 위한 테스트가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2124">Added SoftDelete feature for VM and added tests for softdelete</span></span>

#### <a name="azresources"></a><span data-ttu-id="184db-2125">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="184db-2125">Az.Resources</span></span>
* <span data-ttu-id="184db-2126">종속성 어셈블리 Microsoft.Extensions.Caching.Memory가 1.1.1에서 2.2로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2126">Update dependency assembly Microsoft.Extensions.Caching.Memory from 1.1.1 to 2.2</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="184db-2127">Az.Network</span><span class="sxs-lookup"><span data-stu-id="184db-2127">Az.Network</span></span>
* <span data-ttu-id="184db-2128">일반 서비스 공급자 지원을 위해 PrivateEndpointConnection에 대한 모든 cmdlet이 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2128">Change all cmdlets for PrivateEndpointConnection to support generic service provider.</span></span>
    - <span data-ttu-id="184db-2129">업데이트된 cmdlet:</span><span class="sxs-lookup"><span data-stu-id="184db-2129">Updated cmdlet:</span></span>
        - <span data-ttu-id="184db-2130">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="184db-2130">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="184db-2131">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="184db-2131">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="184db-2132">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="184db-2132">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="184db-2133">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="184db-2133">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="184db-2134">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="184db-2134">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="184db-2135">PrivateLinkResource에 대한 새 cmdlet이 추가되었고 일반 서비스 공급자도 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2135">Add new cmdlet for PrivateLinkResource and it also support generic service provider.</span></span>
    - <span data-ttu-id="184db-2136">새 cmdlet:</span><span class="sxs-lookup"><span data-stu-id="184db-2136">New cmdlet:</span></span>
        - <span data-ttu-id="184db-2137">Get-AzPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="184db-2137">Get-AzPrivateLinkResource</span></span>
* <span data-ttu-id="184db-2138">Proxy Protocol V2 기능에 대한 새 필드 및 매개 변수가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2138">Add new fields and parameter for the feature Proxy Protocol V2.</span></span>
    - <span data-ttu-id="184db-2139">PrivateLinkService에서 EnableProxyProtocol 속성 추가</span><span class="sxs-lookup"><span data-stu-id="184db-2139">Add property EnableProxyProtocol in PrivateLinkService</span></span>
    - <span data-ttu-id="184db-2140">PrivateEndpointConnection에서 LinkIdentifier 속성 추가</span><span class="sxs-lookup"><span data-stu-id="184db-2140">Add property LinkIdentifier in PrivateEndpointConnection</span></span>
    - <span data-ttu-id="184db-2141">새로운 선택적인 매개 변수인 EnableProxyProtocol을 추가하도록 New-AzPrivateLinkService가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2141">Updated New-AzPrivateLinkService to add a new optional parameter EnableProxyProtocol.</span></span>
* <span data-ttu-id="184db-2142">'New-AzApplicationGatewaySku' 참조 설명서의 잘못된 매개 변수 설명 수정</span><span class="sxs-lookup"><span data-stu-id="184db-2142">Fix incorrect parameter description in 'New-AzApplicationGatewaySku' reference documentation</span></span>
* <span data-ttu-id="184db-2143">Azure 방화벽 정책을 지원하는 새로운 cmdlet</span><span class="sxs-lookup"><span data-stu-id="184db-2143">New cmdlets to support the azure firewall policy</span></span>
* <span data-ttu-id="184db-2144">VirtualHub의 자식 리소스 RouteTables에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="184db-2144">Add support for child resource RouteTables of VirtualHub</span></span>
    - <span data-ttu-id="184db-2145">추가된 새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2145">New cmdlets added:</span></span>
        - <span data-ttu-id="184db-2146">Add-AzVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="184db-2146">Add-AzVirtualHubRoute</span></span>
        - <span data-ttu-id="184db-2147">Add-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="184db-2147">Add-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="184db-2148">Get-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="184db-2148">Get-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="184db-2149">Remove-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="184db-2149">Remove-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="184db-2150">Set-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="184db-2150">Set-AzVirtualHub</span></span>
* <span data-ttu-id="184db-2151">VirtualHub의 새로운 속성 Sku 및 VirtualWan의 VirtualWANType에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="184db-2151">Add support for new properties Sku of VirtualHub and VirtualWANType of VirtualWan</span></span>
    - <span data-ttu-id="184db-2152">선택적 매개 변수로 다음 cmdlet이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2152">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="184db-2153">New-AzVirtualHub: 추가된 매개 변수 Sku</span><span class="sxs-lookup"><span data-stu-id="184db-2153">New-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="184db-2154">Update-AzVirtualHub: 추가된 매개 변수 Sku</span><span class="sxs-lookup"><span data-stu-id="184db-2154">Update-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="184db-2155">New-AzVirtualWan: 추가된 매개 변수 VirtualWANType</span><span class="sxs-lookup"><span data-stu-id="184db-2155">New-AzVirtualWan : added parameter VirtualWANType</span></span>
        - <span data-ttu-id="184db-2156">Update-AzVirtualWan: 추가된 매개 변수 VirtualWANType</span><span class="sxs-lookup"><span data-stu-id="184db-2156">Update-AzVirtualWan : added parameter VirtualWANType</span></span>
* <span data-ttu-id="184db-2157">HubVnetConnection, VpnConnection 및 ExpressRouteConnection에 대한 EnableInternetSecurity 속성 지원 추가</span><span class="sxs-lookup"><span data-stu-id="184db-2157">Add support for EnableInternetSecurity property for HubVnetConnection, VpnConnection and ExpressRouteConnection</span></span>
    - <span data-ttu-id="184db-2158">추가된 새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2158">New cmdlets added:</span></span>
        - <span data-ttu-id="184db-2159">Update-AzureRmVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="184db-2159">Update-AzureRmVirtualHubVnetConnection</span></span>
    - <span data-ttu-id="184db-2160">선택적 매개 변수로 다음 cmdlet이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2160">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="184db-2161">New-AzureRmVirtualHubVnetConnection: 추가된 매개 변수 EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="184db-2161">New-AzureRmVirtualHubVnetConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="184db-2162">New-AzureRmVpnConnection: 추가된 매개 변수 EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="184db-2162">New-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="184db-2163">Update-AzureRmVpnConnection: 추가된 매개 변수 EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="184db-2163">Update-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="184db-2164">New-AzureRmExpressRouteConnection: 추가된 매개 변수 EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="184db-2164">New-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="184db-2165">Set-AzureRmExpressRouteConnection: 추가된 매개 변수 EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="184db-2165">Set-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
* <span data-ttu-id="184db-2166">TopLevel WebApplicationFirewall 정책 구성을 위한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="184db-2166">Add support for Configuring TopLevel WebApplicationFirewall Policy</span></span>
    - <span data-ttu-id="184db-2167">추가된 새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2167">New cmdlets added:</span></span>
        - <span data-ttu-id="184db-2168">New-AzApplicationGatewayFirewallPolicySetting</span><span class="sxs-lookup"><span data-stu-id="184db-2168">New-AzApplicationGatewayFirewallPolicySetting</span></span>
        - <span data-ttu-id="184db-2169">New-AzApplicationGatewayFirewallPolicyExclusion</span><span class="sxs-lookup"><span data-stu-id="184db-2169">New-AzApplicationGatewayFirewallPolicyExclusion</span></span>
        - <span data-ttu-id="184db-2170">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="184db-2170">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span></span>
        - <span data-ttu-id="184db-2171">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="184db-2171">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span></span>
        - <span data-ttu-id="184db-2172">New-AzApplicationGatewayFirewallPolicyManagedRule</span><span class="sxs-lookup"><span data-stu-id="184db-2172">New-AzApplicationGatewayFirewallPolicyManagedRule</span></span>
        - <span data-ttu-id="184db-2173">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="184db-2173">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span></span>
    - <span data-ttu-id="184db-2174">선택적 매개 변수로 다음 cmdlet이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2174">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="184db-2175">New-AzApplicationGatewayFirewallPolicy: 추가된 매개 변수 PolicySetting, ManagedRule</span><span class="sxs-lookup"><span data-stu-id="184db-2175">New-AzApplicationGatewayFirewallPolicy : added parameter PolicySetting, ManagedRule</span></span>
* <span data-ttu-id="184db-2176">CustomRule에서 Geo-Match 연산자를 위한 지원 추가됨</span><span class="sxs-lookup"><span data-stu-id="184db-2176">Added support for Geo-Match operator on CustomRule</span></span>
    - <span data-ttu-id="184db-2177">FirewallCondition에서 연산자에 GeoMatch 추가됨</span><span class="sxs-lookup"><span data-stu-id="184db-2177">Added GeoMatch to the operator on the FirewallCondition</span></span>
* <span data-ttu-id="184db-2178">perListener 및 perSite 방화벽 규칙에 대한 지원 추가됨</span><span class="sxs-lookup"><span data-stu-id="184db-2178">Added support for perListener and perSite Firewall policy</span></span>
    - <span data-ttu-id="184db-2179">선택적 매개 변수로 다음 cmdlet이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2179">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="184db-2180">New-AzApplicationGatewayHttpListener: 추가된 매개 변수 FirewallPolicy, FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="184db-2180">New-AzApplicationGatewayHttpListener : added parameter FirewallPolicy, FirewallPolicyId</span></span>
        - <span data-ttu-id="184db-2181">New-AzApplicationGatewayPathRuleConfig: 추가된 매개 변수 FirewallPolicy, FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="184db-2181">New-AzApplicationGatewayPathRuleConfig : added parameter FirewallPolicy, FirewallPolicyId</span></span>
* <span data-ttu-id="184db-2182">'PSBastion'에서 이름이 AzureBastionSubnet인 필수 서브넷의 수정은 대소문자를 구분하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2182">Fix required subnet with name AzureBastionSubnet in 'PSBastion' can be case insensitive</span></span>
* <span data-ttu-id="184db-2183">Azure Firewall을 위한 네트워크 규칙의 대상 FQDN 및 NAT 규칙의 번역된 FQDN 지원</span><span class="sxs-lookup"><span data-stu-id="184db-2183">Support for Destination FQDNs in Network Rules and Translated FQDN in NAT Rules for Azure Firewall</span></span>
* <span data-ttu-id="184db-2184">IpGroup의 최상위 리소스 RouteTables에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="184db-2184">Add support for top level resource RouteTables of IpGroup</span></span>
    - <span data-ttu-id="184db-2185">추가된 새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2185">New cmdlets added:</span></span>
        - <span data-ttu-id="184db-2186">New-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="184db-2186">New-AzIpGroup</span></span>
        - <span data-ttu-id="184db-2187">Remove-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="184db-2187">Remove-AzIpGroup</span></span>
        - <span data-ttu-id="184db-2188">Get-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="184db-2188">Get-AzIpGroup</span></span>
        - <span data-ttu-id="184db-2189">Set-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="184db-2189">Set-AzIpGroup</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="184db-2190">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="184db-2190">Az.ServiceFabric</span></span>
* <span data-ttu-id="184db-2191">Add-AzVmssSecret에서 지원되기 때문에 Add-AzServiceFabricApplicationCertificate cmdlet이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2191">Remove Add-AzServiceFabricApplicationCertificate cmdlet as this scenario is covered by Add-AzVmssSecret.</span></span>

#### <a name="azsql"></a><span data-ttu-id="184db-2192">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="184db-2192">Az.Sql</span></span>
* <span data-ttu-id="184db-2193">Managed Instances에서 삭제된 데이터베이스의 복원을 위한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2193">Added support for restore of dropped databases on Managed Instances.</span></span>
* <span data-ttu-id="184db-2194">이전의 감사 cmdlet 코드가 사용되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2194">Deprecated from code old auditing cmdlets.</span></span>
* <span data-ttu-id="184db-2195">사용되지 않는 별칭이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2195">Removed deprecated aliases:</span></span>
* <span data-ttu-id="184db-2196">Get-AzSqlDatabaseIndexRecommendations(대신 Get-AzSqlDatabaseIndexRecommendation 사용)</span><span class="sxs-lookup"><span data-stu-id="184db-2196">Get-AzSqlDatabaseIndexRecommendations (use Get-AzSqlDatabaseIndexRecommendation instead)</span></span>
* <span data-ttu-id="184db-2197">Get-AzSqlDatabaseRestorePoints(대신 Get-AzSqlDatabaseRestorePoint 사용)</span><span class="sxs-lookup"><span data-stu-id="184db-2197">Get-AzSqlDatabaseRestorePoints (use Get-AzSqlDatabaseRestorePoint instead)</span></span>
* <span data-ttu-id="184db-2198">Get-AzSqlDatabaseSecureConnectionPolicy cmdlet 제거</span><span class="sxs-lookup"><span data-stu-id="184db-2198">Remove Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="184db-2199">사용되지 않는 취약성 평가 설정 cmdlet에 대한 별칭 제거</span><span class="sxs-lookup"><span data-stu-id="184db-2199">Remove aliases for deprecated Vulnerability Assessment Settings cmdlets</span></span>
* <span data-ttu-id="184db-2200">지능형 위협 탐지 설정 cmdlet 사용 중단</span><span class="sxs-lookup"><span data-stu-id="184db-2200">Deprecate Advanced Threat Detection Settings cmdlets</span></span>
* <span data-ttu-id="184db-2201">데이터베이스의 열에 대한 민감도 권장 사항의 사용 여부를 제어하는 cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2201">Adding cmdlets to Disable and enable sensitivity recommendations on columns in a database.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="184db-2202">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="184db-2202">Az.Storage</span></span>
* <span data-ttu-id="184db-2203">스토리지 계정을 만들거나 업데이트할 때 큰 파일 공유 사용 지원</span><span class="sxs-lookup"><span data-stu-id="184db-2203">Support enable Large File share when create or update Storage account</span></span>
    -  <span data-ttu-id="184db-2204">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="184db-2204">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="184db-2205">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="184db-2205">Set-AzStorageAccount</span></span>
* <span data-ttu-id="184db-2206">파일 핸들을 닫거나/가져올 때, DeletePending 상태의 개체로 인한 오류를 방지하기 위해 입력 경로가 파일 디렉터리인지 또는 파일인지를 확인하는 과정을 건너뜁니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2206">When close/get File handle, skip check the input path is File directory or File, to avoid failure with object in DeletePending status</span></span>
    -  <span data-ttu-id="184db-2207">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="184db-2207">Get-AzStorageFileHandle</span></span>
    -  <span data-ttu-id="184db-2208">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="184db-2208">Close-AzStorageFileHandle</span></span>

## <a name="280---october-2019"></a><span data-ttu-id="184db-2209">2.8.0 - 2019년 10월</span><span class="sxs-lookup"><span data-stu-id="184db-2209">2.8.0 - October 2019</span></span>
### <a name="general"></a><span data-ttu-id="184db-2210">일반</span><span class="sxs-lookup"><span data-stu-id="184db-2210">General</span></span>
* <span data-ttu-id="184db-2211">Az.HealthcareApis 1.0.0 릴리스</span><span class="sxs-lookup"><span data-stu-id="184db-2211">Az.HealthcareApis 1.0.0 release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="184db-2212">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="184db-2212">Az.Accounts</span></span>
* <span data-ttu-id="184db-2213">생성된 모듈에 대한 원격 분석 및 URL 다시 작성이 업데이트되고, Windows 단위 테스트가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2213">Update telemetry and url rewriting for generated modules, fix windows unit tests.</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="184db-2214">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="184db-2214">Az.ApiManagement</span></span>
* <span data-ttu-id="184db-2215">**Set-AzApiManagementApi** - API 업데이트 지원이 ApiVersionSet에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2215">**Set-AzApiManagementApi** - Added support for Updating Api into ApiVersionSet</span></span>
    - <span data-ttu-id="184db-2216">문제 https://github.com/Azure/azure-powershell/issues/10068 수정</span><span class="sxs-lookup"><span data-stu-id="184db-2216">Fix for issue https://github.com/Azure/azure-powershell/issues/10068</span></span>

#### <a name="azautomation"></a><span data-ttu-id="184db-2217">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="184db-2217">Az.Automation</span></span>
* <span data-ttu-id="184db-2218">Linux 다시 부팅 설정 매개 변수에 대한 New-AzureAutomationSoftwareUpdateConfiguration cmdlet이 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2218">Fixed New-AzureAutomationSoftwareUpdateConfiguration cmdlet for Linux reboot setting parameter.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="184db-2219">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="184db-2219">Az.Batch</span></span>
* <span data-ttu-id="184db-2220">**Get-AzBatchNodeAgentSku** 가 더 이상 사용되지 않으며, 2.0.0 버전의 **Get-AzBatchSupportImage** 로 대체되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2220">**Get-AzBatchNodeAgentSku** is deprecated and will be replaced by **Get-AzBatchSupportImage** in version 2.0.0.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="184db-2221">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="184db-2221">Az.Compute</span></span>
* <span data-ttu-id="184db-2222">Priority, EvictionPolicy 및 MaxPrice 매개 변수가 New-AzVM 및 New-AzVmss cmdlet에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2222">Add Priority, EvictionPolicy, and MaxPrice parameters to New-AzVM and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="184db-2223">Add-AzVMAdditionalUnattendContent 및 Add-AzVMSshPublicKey cmdlet에 대한 경고 메시지와 도움말 문서가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2223">Fix warning message and help document for Add-AzVMAdditionalUnattendContent and Add-AzVMSshPublicKey cmdlets</span></span>
* <span data-ttu-id="184db-2224">Set-AzVMDiskEncryptionExtension의 관리 디스크가 있는 Linux VM에 대한 -skipVmBackup 예외가 해결되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2224">Fix -skipVmBackup exception for Linux VMs with managed disks for Set-AzVMDiskEncryptionExtension.</span></span>
* <span data-ttu-id="184db-2225">Set-AzVMDiskEncryptionExtension의 두 가지 패스 시나리오에서 발생하는 암호화 설정 업데이트의 버그가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2225">Fix bug in update encryption settings in Set-AzVMDiskEncryptionExtension, two pass scenario.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="184db-2226">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="184db-2226">Az.DataFactory</span></span>
* <span data-ttu-id="184db-2227">ADF V2 데이터 흐름에 대한 CRUD 명령으로 Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow 및 Get-AzDataFactoryV2DataFlow가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2227">Adding CRUD commands for ADF V2 data flow: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow, and Get-AzDataFactoryV2DataFlow.</span></span>
* <span data-ttu-id="184db-2228">ADF V2 데이터 흐름 디버그 세션에 대한 작업 명령으로 Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand 및 Stop-AzDataFactoryV2DataFlowDebugSession이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2228">Adding action commands for ADF V2 data flow debug Session: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand and Stop-AzDataFactoryV2DataFlowDebugSession.</span></span>
* <span data-ttu-id="184db-2229">ADF .Net SDK 버전이 4.2.0으로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2229">Update ADF .Net SDK version to 4.2.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="184db-2230">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="184db-2230">Az.DataLakeStore</span></span>
* <span data-ttu-id="184db-2231">도메인 없이 '-'가 있는 계정을 전달할 수 있도록 계정 유효성 검사가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2231">Fix account validation so that accounts with '-' can be passed without domain</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="184db-2232">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="184db-2232">Az.HealthcareApis</span></span>
* <span data-ttu-id="184db-2233">PowerShell 버전이 1.0.0으로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2233">Updated the powershell version to 1.0.0</span></span>
* <span data-ttu-id="184db-2234">SDK 버전이 1.0.2로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2234">Updated the SDK version to 1.0.2</span></span>
* <span data-ttu-id="184db-2235">새 SDK 버전을 참조하도록 테스트가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2235">Update in tests to refer to new SDK version</span></span>
* <span data-ttu-id="184db-2236">출력이 중첩 구조에서 평면화 구조로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2236">Updated the output structure from nested to flattened.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="184db-2237">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="184db-2237">Az.IotHub</span></span>
* <span data-ttu-id="184db-2238">새 라우팅 원본 추가: DigitalTwinChangeEvents</span><span class="sxs-lookup"><span data-stu-id="184db-2238">Add new routing source: DigitalTwinChangeEvents</span></span>
* <span data-ttu-id="184db-2239">사소한 버그 수정: Get-AzIothub에서 subscriptionId를 반환하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2239">Minor bug fix: Get-AzIothub not returning subscriptionId</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="184db-2240">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="184db-2240">Az.Monitor</span></span>
* <span data-ttu-id="184db-2241">작업 그룹에 대한 새 작업 그룹 수신기로 -ItsmReceiver, -VoiceReceiver, -ArmRoleReceiver, -AzureFunctionReceiver, -LogicAppReceiver, -AutomationRunbookReceiver, -AzureAppPushReceiver가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2241">New action group receivers added for action group   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span></span>
* <span data-ttu-id="184db-2242">수신기에 사용하도록 설정된 일반 경고 스키마가 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2242">Use common alert schema enabled for the receivers.</span></span> <span data-ttu-id="184db-2243">SMS, Azure 앱 푸시, ITSM 및 음성 수신기에는 적용되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2243">This is not applicable for SMS, Azure App push , ITSM and Voice recievers</span></span>
* <span data-ttu-id="184db-2244">웹후크에서 이제 Azure Active Directory 인증을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2244">Webhooks now supports Azure active directory authentication .</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="184db-2245">Az.Network</span><span class="sxs-lookup"><span data-stu-id="184db-2245">Az.Network</span></span>
* <span data-ttu-id="184db-2246">서비스 엔드포인트 정책에 사용할 수 있는 별칭을 가져오기 위해 호출할 수 있는 새 Get-AzAvailableServiceAlias cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2246">Add new cmdlet Get-AzAvailableServiceAlias which can be called to get the aliases that can be used for Service Endpoint Policies.</span></span>
* <span data-ttu-id="184db-2247">트래픽 선택기를 Virtual Network 게이트웨이 연결에 추가할 수 있는 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2247">Added support for the adding traffic selectors to Virtual Network Gateway Connections</span></span>
    - <span data-ttu-id="184db-2248">추가된 새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2248">New cmdlets added:</span></span>
        - <span data-ttu-id="184db-2249">New-AzureRmTrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="184db-2249">New-AzureRmTrafficSelectorPolicy</span></span>
    - <span data-ttu-id="184db-2250">cmdlet이 선택적인 -TrafficSelectorPolicies, -New-AzureRmVirtualNetworkGatewayConnection, -Set-AzureRmVirtualNetworkGatewayConnection 매개 변수로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2250">Cmdlets updated with optional parameter -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="184db-2251">ESP 및 AH 프로토콜 지원이 네트워크 보안 규칙 구성에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2251">Add support for ESP and AH protocols in network security rule configurations</span></span>
    - <span data-ttu-id="184db-2252">다음 Cmdlet이 업데이트 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2252">Updated cmdlets:</span></span>
        - <span data-ttu-id="184db-2253">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="184db-2253">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="184db-2254">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="184db-2254">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="184db-2255">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="184db-2255">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="184db-2256">Cortex cmdlet의 예외 처리가 향상되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2256">Improve handling of exceptions in Cortex cmdlets</span></span>
* <span data-ttu-id="184db-2257">새 VirtualNetworkGateways 세대 및 SKU</span><span class="sxs-lookup"><span data-stu-id="184db-2257">New Generations and SKUs for VirtualNetworkGateways</span></span>
  - <span data-ttu-id="184db-2258">새 VirtualNetworkGateways 세대가 도입되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2258">Introduce new Generations for VirtualNetworkGateways.</span></span>
  - <span data-ttu-id="184db-2259">높은 처리량의 새 VirtualNetworkGateways SKU가 도입되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2259">Introduce new high throughput SKUs for VirtualNetworkGateways.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="184db-2260">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="184db-2260">Az.RedisCache</span></span>
* <span data-ttu-id="184db-2261">'-Size' 매개 변수에 대한 누락 값을 포함하도록 'Set-AzRedisCache' 참조 설명서가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2261">Updated 'Set-AzRedisCache' reference documentation to include missing values for '-Size' parameter</span></span>

#### <a name="azsql"></a><span data-ttu-id="184db-2262">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="184db-2262">Az.Sql</span></span>
* <span data-ttu-id="184db-2263">Managed Instance에서 Active Directory 관리자를 설정할 수 있는 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2263">Add support for setting Active Directory Administrator on Managed Instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="184db-2264">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="184db-2264">Az.Storage</span></span>
* <span data-ttu-id="184db-2265">스토리지 클라이언트 라이브러리가 11.1.0으로 업그레이드되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2265">Upgrade Storage Client Library to 11.1.0</span></span>
* <span data-ttu-id="184db-2266">관리 평면 API를 사용하여 컨테이너를 나열하면 NextPageLink를 통해 나열됩니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2266">List containers with Management plane API, will list with NextPageLink</span></span>
    -  <span data-ttu-id="184db-2267">Get-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="184db-2267">Get-AzRmStorageContainer</span></span>
* <span data-ttu-id="184db-2268">구독에서 스토리지 계정을 나열하면 NextPageLink를 통해 나열됩니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2268">List Storage accounts from subscription, will list with NextPageLink</span></span>
    -  <span data-ttu-id="184db-2269">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="184db-2269">Get-AzStorageAccount</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="184db-2270">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="184db-2270">Az.StorageSync</span></span>
* <span data-ttu-id="184db-2271">Reset-AzStorageSyncServerCertificate의 9810 문제가 해결되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2271">Fix Issue 9810 in Reset-AzStorageSyncServerCertificate.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="184db-2272">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="184db-2272">Az.Websites</span></span>
* <span data-ttu-id="184db-2273">앱의 ASP를 업데이트하는 Set-AzWebApp이 실패했습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2273">Set-AzWebApp updating ASP of an app was failing</span></span>

## <a name="270---september-2019"></a><span data-ttu-id="184db-2274">2.7.0 - 2019년 9월</span><span class="sxs-lookup"><span data-stu-id="184db-2274">2.7.0 - September 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="184db-2275">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="184db-2275">Az.ApiManagement</span></span>
* <span data-ttu-id="184db-2276">'Set-AzApiManagementPolicy' 참조 설명서에서 '-Format' 매개 변수 설명이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2276">Update '-Format' parameter description in 'Set-AzApiManagementPolicy' reference documentation</span></span>
* <span data-ttu-id="184db-2277">참조 설명서에서 사용되지 않는 cmdlet 'Update-AzApiManagementDeployment'의 참조를 제거했습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2277">Removed references of deprecated cmdlet 'Update-AzApiManagementDeployment' from reference documentation.</span></span> <span data-ttu-id="184db-2278">그 대신 'Set-AzApiManagement'를 사용하세요.</span><span class="sxs-lookup"><span data-stu-id="184db-2278">Use 'Set-AzApiManagement' instead.</span></span>

#### <a name="azautomation"></a><span data-ttu-id="184db-2279">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="184db-2279">Az.Automation</span></span>
* <span data-ttu-id="184db-2280">'Register-AzAutomationDscNode'에 대한 참조 설명서의 예제 오타가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2280">Fixed example typo in reference documentation for 'Register-AzAutomationDscNode'</span></span>
* <span data-ttu-id="184db-2281">Register-AzAutomationDSCNode에 OS 제한에 대한 설명이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2281">Added clarification on OS restriction to Register-AzAutomationDSCNode</span></span>
* <span data-ttu-id="184db-2282">-Wait 옵션에 대한 Start-AzAutomationRunbook cmdlet Null 참조 예외가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2282">Fixed Start-AzAutomationRunbook cmdlet Null reference exception for -Wait option.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="184db-2283">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="184db-2283">Az.Compute</span></span>
* <span data-ttu-id="184db-2284">New-AzDiskConfig에 UploadSizeInBytes 매개 변수가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2284">Add UploadSizeInBytes parameter tp New-AzDiskConfig</span></span>
* <span data-ttu-id="184db-2285">New-AzSnapshotConfig에 증분 매개 변수가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2285">Add Incremental parameter to New-AzSnapshotConfig</span></span>
* <span data-ttu-id="184db-2286">다음과 같은 낮은 우선 순위의 가상 머신 기능이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2286">Add a low priority virtual machine feature:</span></span>
    - <span data-ttu-id="184db-2287">MaxPrice, EvictionPolicy 및 Priority 매개 변수가 New-AzVMConfig에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2287">MaxPrice, EvictionPolicy and Priority parameters are added to New-AzVMConfig.</span></span>
    - <span data-ttu-id="184db-2288">MaxPrice 매개 변수는 New-AzVmssConfig, Update-AzVM 및 Update-AzVmss cmdlet에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2288">MaxPrice parameter is added to New-AzVmssConfig, Update-AzVM and Update-AzVmss cmdlets.</span></span>
* <span data-ttu-id="184db-2289">구독의 모든 가용성 세트를 나열할 때 발생하는 Get-AzAvailabilitySet cmdlet에 대한 VM 참조 이슈가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2289">Fix VM reference issue for Get-AzAvailabilitySet cmdlet when it lists all availability sets in the subscription.</span></span>
* <span data-ttu-id="184db-2290">Get-AzRemoteDesktopFile에 대한 null 예외가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2290">Fix the null exception for Get-AzRemoteDesktopFile.</span></span>
* <span data-ttu-id="184db-2291">종료 상대 위치에 대한 VHD 검색 메서드가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2291">Fix VHD Seek method for end-relative position.</span></span>
* <span data-ttu-id="184db-2292">New-AzVM 및 Update-AzVM에 대한 UltraSSD 이슈가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2292">Fix UltraSSD issue for New-AzVM and Update-AzVM.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="184db-2293">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="184db-2293">Az.DataFactory</span></span>
* <span data-ttu-id="184db-2294">ADF V2에 대한 3가지 새 명령 Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription 및 Get-AzDataFactoryV2TriggerSubscriptionStatus가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2294">Adding 3 new commands for ADF V2 - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription, and Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>
* <span data-ttu-id="184db-2295">ADF .Net SDK 버전이 4.1.3으로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2295">Updated ADF .Net SDK version to 4.1.3</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="184db-2296">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="184db-2296">Az.HDInsight</span></span>
* <span data-ttu-id="184db-2297">호출 주요 변경 내용</span><span class="sxs-lookup"><span data-stu-id="184db-2297">Call out breaking changes</span></span>

#### <a name="aziothub"></a><span data-ttu-id="184db-2298">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="184db-2298">Az.IotHub</span></span>
* <span data-ttu-id="184db-2299">지역 쌍 재해 복구 지역에 IotHub에 대한 장애 조치(failover) 호출 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2299">Add support to invoke failover for an IotHub to the geo-paired disaster recovery region.</span></span>
* <span data-ttu-id="184db-2300">IotHub에 대한 메시지 보강 관리 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2300">Add support to manage message enrichment for an IotHub.</span></span> <span data-ttu-id="184db-2301">새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2301">New cmdlets are:</span></span>
    - <span data-ttu-id="184db-2302">Add-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="184db-2302">Add-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="184db-2303">Get-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="184db-2303">Get-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="184db-2304">Remove-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="184db-2304">Remove-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="184db-2305">Set-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="184db-2305">Set-AzIotHubMessageEnrichment</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="184db-2306">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="184db-2306">Az.Monitor</span></span>
* <span data-ttu-id="184db-2307">최신 모니터링 SDK, 즉, 0.24.1-preview를 가리킵니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2307">Pointing to the most recent Monitor SDK, i.e. 0.24.1-preview</span></span>
   - <span data-ttu-id="184db-2308">메트릭 cmdlet에 줄 바꿈하지 않는 변경 내용을 추가합니다. 즉, 단위 열거형은 여러 새 값을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2308">Adds non-braking changes to the Metrics cmdlets, i.e. the Unit enumeration supports several new values.</span></span> <span data-ttu-id="184db-2309">이러한 cmdlet은 읽기 전용이므로 cmdlet 입력이 변경되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2309">These are read-only cmdlets, so there would be no change in the input of the cmdlets.</span></span>
   - <span data-ttu-id="184db-2310">이제 **ActionGroups** 요청의 api 버전은 **2019-06-01** 이고, 이전에는 **2018-03-01** 였습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2310">The api-version of the **ActionGroups** requests is now **2019-06-01**, before it was **2018-03-01**.</span></span> <span data-ttu-id="184db-2311">시나리오 테스트가 이 변경 내용에 맞게 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2311">The scenario tests have been updated to accommodate for this change.</span></span>
   - <span data-ttu-id="184db-2312">**EmailReceiver** 및 **WebhookReceiver** 클래스에 대한 생성자가 새 필수 인수, 즉, **useCommonAlertSchema** 라는 부울 값을 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2312">The constructors for the classes **EmailReceiver** and **WebhookReceiver** added one new mandatory argument, i.e. a Boolean value called **useCommonAlertSchema**.</span></span> <span data-ttu-id="184db-2313">현재 이 값은 cmdlet의 주요 변경 사항을 숨기도록 **false** 로 고정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2313">Currently, the value is fixed to **false** to hide this breaking change from the cmdlets.</span></span> <span data-ttu-id="184db-2314">**참고**: 이 변경 사항은 경고 팀에서 유효성을 검사해야 하는 임시 변경 내용입니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2314">**NOTE**: this is a temporary change that must be validated by the Alerts team.</span></span>
   - <span data-ttu-id="184db-2315">이전 SDK에서 변경된 **Source** 클래스(**ScheduledQueryRuleSource** 클래스와 관련됨)의 생성자에 대한 인수 순서입니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2315">The order of the arguments for the constructor of the class **Source** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="184db-2316">이번 변화로 인해 두 개의 단위 테스트를 수정해야 했습니다. 즉, 두 단위 테스트가 컴파일되었지만 테스트를 통과하지 못했습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2316">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
   - <span data-ttu-id="184db-2317">이전 SDK에서 변경된 **AlertingAction** 클래스(**ScheduledQueryRuleSource** 클래스와 관련됨)의 생성자에 대한 인수 순서입니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2317">The order of the arguments for the constructor of the class **AlertingAction** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="184db-2318">이번 변화로 인해 두 개의 단위 테스트를 수정해야 했습니다. 즉, 두 단위 테스트가 컴파일되었지만 테스트를 통과하지 못했습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2318">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
* <span data-ttu-id="184db-2319">메트릭 경고 V2에 대한 동적 임계값 기준 지원</span><span class="sxs-lookup"><span data-stu-id="184db-2319">Support Dynamic Threshold criteria for metric alert V2</span></span>
    - <span data-ttu-id="184db-2320">AzMetricAlertRuleV2Criteria: 이제 동적 임계값 조건도 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2320">New-AzMetricAlertRuleV2Criteria: now creats dynamic threshold criteria also</span></span>
    - <span data-ttu-id="184db-2321">Add-AzMetricAlertRuleV2: 이제 동적 임계값 조건도 수락합니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2321">Add-AzMetricAlertRuleV2: now accept dynamic threshold criteria also</span></span>
* <span data-ttu-id="184db-2322">SQR(예약된 쿼리 규칙)의 향상된 기능</span><span class="sxs-lookup"><span data-stu-id="184db-2322">Improvements in Scheduled Query Rule cmdlets (SQR)</span></span>
 - <span data-ttu-id="184db-2323">Cmdlet이 'Location' 매개 변수를 두 가지 형식(eastus 같은 위치 또는 미국 동부 같은 위치 표시 이름)으로 모두 허용합니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2323">Cmdlets will accept 'Location' paramater in both formats, either the location (e.g. eastus) or the location display name (e.g. East US)</span></span>
 - <span data-ttu-id="184db-2324">도움말 파일에 적절하게 표시된 'Enabled' 매개 변수</span><span class="sxs-lookup"><span data-stu-id="184db-2324">Illustrated 'Enabled' parameter in help files properly</span></span>
 - <span data-ttu-id="184db-2325">선택적 매개 변수 'ActionGroup'에 대한 예제가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2325">Added examples for 'ActionGroup' optional parameter</span></span>
 - <span data-ttu-id="184db-2326">도움말 파일이 전체적으로 개선되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2326">Overall improved help files</span></span>
* <span data-ttu-id="184db-2327">'Set-AzActionRule'의 범위 유형 결정 버그를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2327">Fix bug in determining scope type for 'Set-AzActionRule'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="184db-2328">Az.Network</span><span class="sxs-lookup"><span data-stu-id="184db-2328">Az.Network</span></span>
* <span data-ttu-id="184db-2329">'New-AzApplicationGateway' 참조 설명서의 잘못된 예제가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2329">Fix incorrect example in 'New-AzApplicationGateway' reference documentation</span></span>
* <span data-ttu-id="184db-2330">'Get-AzNetworkWatcherPacketCapture' 참조 설명서에 패킷 캡처를 위한 모든 속성 검색과 관련된 메모가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2330">Add note in 'Get-AzNetworkWatcherPacketCapture' reference documentation about retrieving all properties for a packet capture</span></span>
* <span data-ttu-id="184db-2331">NIC를 올바르게 열거하도록 'Test-AzNetworkWatcherIPFlow' 참조 설명서의 예제가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2331">Fixed example in 'Test-AzNetworkWatcherIPFlow' reference documentation to correctly enumerate NICs</span></span>
* <span data-ttu-id="184db-2332">추가 세부 정보가 있는 경우 추가 세부 정보를 표시하도록 클라우드 예외 구문 분석이 향상되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2332">Improved cloud exception parsing to display additional details if they are present</span></span>
* <span data-ttu-id="184db-2333">더 많은 형식의 SDK 예외를 처리하도록 클라우드 예외 구문 분석이 향상되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2333">Improved cloud exception parsing to handle additional type of SDK exception</span></span>
* <span data-ttu-id="184db-2334">보안 규칙 모델의 잘못된 매핑이 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2334">Fixed incorrect mapping of Security Rule models</span></span>
* <span data-ttu-id="184db-2335">네트워크 인터페이스에 개인 IP 기능을 위한 속성이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2335">Added properties to network interface for private ip feature</span></span>
    - <span data-ttu-id="184db-2336">PSNetworkInterface에 'PrivateEndpoint' 속성이 PSResourceId 형식으로 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2336">Added property 'PrivateEndpoint' as type of PSResourceId to PSNetworkInterface</span></span>
    - <span data-ttu-id="184db-2337">PSNetworkInterfaceIPConfiguration에 'PrivateLinkConnectionProperties' 속성이 PSIpConfigurationConnectivityInformation 형식으로 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2337">Added property 'PrivateLinkConnectionProperties' as type of PSIpConfigurationConnectivityInformation to PSNetworkInterfaceIPConfiguration</span></span>
    - <span data-ttu-id="184db-2338">새 모델 클래스 PSIpConfigurationConnectivityInformation이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2338">Added new model class PSIpConfigurationConnectivityInformation</span></span>
* <span data-ttu-id="184db-2339">Azure Firewall 리소스에 대한 새 ApplicationRuleProtocolType 'mssql'이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2339">Added new ApplicationRuleProtocolType 'mssql' for Azure Firewall resource</span></span>
* <span data-ttu-id="184db-2340">Virtual WAN에서 멀티 링크를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2340">MultiLink support in Virtual WAN</span></span>
    - <span data-ttu-id="184db-2341">새로운 cmdlet</span><span class="sxs-lookup"><span data-stu-id="184db-2341">New cmdlets</span></span>
        - <span data-ttu-id="184db-2342">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="184db-2342">New-AzVpnSiteLink</span></span>
        - <span data-ttu-id="184db-2343">New-AzVpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="184db-2343">New-AzVpnSiteLinkConnection</span></span>
    - <span data-ttu-id="184db-2344">업데이트된 cmdlet:</span><span class="sxs-lookup"><span data-stu-id="184db-2344">Updated cmdlet:</span></span>
        - <span data-ttu-id="184db-2345">New-VpnSite</span><span class="sxs-lookup"><span data-stu-id="184db-2345">New-VpnSite</span></span>
        - <span data-ttu-id="184db-2346">Update-VpnSite</span><span class="sxs-lookup"><span data-stu-id="184db-2346">Update-VpnSite</span></span>
        - <span data-ttu-id="184db-2347">New-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="184db-2347">New-VpnConnection</span></span>
        - <span data-ttu-id="184db-2348">Update-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="184db-2348">Update-VpnConnection</span></span>
* <span data-ttu-id="184db-2349">AzureRM cmdlet 대신 Az cmdlet을 사용하도록 일부 PowerShell 예제의 문서가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2349">Fixed documents for some PowerShell examples to use Az cmdlets instead of AzureRM cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="184db-2350">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="184db-2350">Az.RecoveryServices</span></span>
* <span data-ttu-id="184db-2351">AzureVMpolicy 개체가 ProtectedItemsCount 특성으로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2351">Update AzureVMpolicy Object with ProtectedItemsCount Attribute</span></span>
* <span data-ttu-id="184db-2352">VM 정책 및 원래 스토리지 계정 복원에 대한 테스트가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2352">Added Tests for VM policy and Original Storage Account Restore</span></span>

#### <a name="azresources"></a><span data-ttu-id="184db-2353">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="184db-2353">Az.Resources</span></span>
* <span data-ttu-id="184db-2354">매개 변수 범위 없이 AzRoleAssignment를 호출할 수 없는 버그가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2354">Fix bug where New-AzRoleAssignment could not be called without parameter Scope.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="184db-2355">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="184db-2355">Az.ServiceFabric</span></span>
* <span data-ttu-id="184db-2356">'AzServiceFabricReliability' 참조 설명서에 대한 예제의 오타가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2356">Fixed typo in example for 'Update-AzServiceFabricReliability' reference documentation</span></span>
* <span data-ttu-id="184db-2357">애플리케이션 및 서비스를 관리하는 다음과 같은 새 cmdlet이 추가됩니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2357">Adding new cmdlets to manage appliaction and services:</span></span>
    - <span data-ttu-id="184db-2358">New-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="184db-2358">New-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="184db-2359">New-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="184db-2359">New-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="184db-2360">New-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="184db-2360">New-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="184db-2361">New-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="184db-2361">New-AzServiceFabricService</span></span>
    - <span data-ttu-id="184db-2362">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="184db-2362">Update-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="184db-2363">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="184db-2363">Get-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="184db-2364">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="184db-2364">Get-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="184db-2365">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="184db-2365">Get-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="184db-2366">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="184db-2366">Get-AzServiceFabricService</span></span>
    - <span data-ttu-id="184db-2367">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="184db-2367">Remove-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="184db-2368">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="184db-2368">Remove-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="184db-2369">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="184db-2369">Remove-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="184db-2370">Remove-AzServiceFabricServic</span><span class="sxs-lookup"><span data-stu-id="184db-2370">Remove-AzServiceFabricServic</span></span>
* <span data-ttu-id="184db-2371">Service Fabric SDK가 Service Fabric 리소스 공급자 api 버전 2019-03-01을 사용하는 1.2.0 버전으로 업그레이드되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2371">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2019-03-01.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="184db-2372">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="184db-2372">Az.SignalR</span></span>
* <span data-ttu-id="184db-2373">Update, Restart, CheckNameAvailability, GetUsage Cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2373">Add Update, Restart, CheckNameAvailability, GetUsage Cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="184db-2374">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="184db-2374">Az.Sql</span></span>
* <span data-ttu-id="184db-2375">'Get-AzSqlElasticPool'에 대한 참조 설명서의 예제가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2375">Update example in reference documentation for 'Get-AzSqlElasticPool'</span></span>
* <span data-ttu-id="184db-2376">탄력적 풀을 만드는 vCore 예제가 추가되었습니다(AzSqlElasticPool).</span><span class="sxs-lookup"><span data-stu-id="184db-2376">Added vCore example to creating an elastic pool (New-AzSqlElasticPool).</span></span>
* <span data-ttu-id="184db-2377">Set-AzSqlServerAdvancedThreatProtectionPolicy 및 Set-AzSqlDatabaseAdvancedThreatProtectionPolicy에서 EmailAddresses가 비어 있는 경우 EmailAddresses의 유효성을 검사하고 EmailAdmins가 false가 아닌지 확인하는 기능이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2377">Remove the validation of EmailAddresses and the check that EmailAdmins is not false in case EmailAddresses is empty in Set-AzSqlServerAdvancedThreatProtectionPolicy and Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="184db-2378">감사 범주를 사용하는 여러 진단 설정이 있는 경우 서버/데이터베이스 감사 설정을 제거하도록 설정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2378">Enabled removal of server/database auditing settings when multiple diagnostic settings that enable audit category exist.</span></span>
* <span data-ttu-id="184db-2379">여러 Sql 취약성 평가 cmdlet에서 이메일 주소 유효성 검사가 수정되었습니다(Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting 및 Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span><span class="sxs-lookup"><span data-stu-id="184db-2379">Fix email addresses validation in multiple Sql Vulnerability Assessment cmdlets (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting and Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span></span>

#### <a name="azstorage"></a><span data-ttu-id="184db-2380">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="184db-2380">Az.Storage</span></span>
* <span data-ttu-id="184db-2381">'Get-AzStorageAccountKey'에 대한 참조 설명서의 예제가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2381">Updated example in reference documentation for 'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="184db-2382">Azure 파일 업로드/다운에서, 원본 파일 SMB 속성(파일 특성, 파일 생성 시간, 파일을 마지막으로 쓴 시간)을 대상 파일에 보존하는 기능이 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2382">In upload/Downalod Azure File,support perserve the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the destination file</span></span>
    -  <span data-ttu-id="184db-2383">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="184db-2383">Set-AzStorageFileContent</span></span>
    -  <span data-ttu-id="184db-2384">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="184db-2384">Get-AzStorageFileContent</span></span>
* <span data-ttu-id="184db-2385">컨테이너가 사용되는 ImmutabilityPolicy에서 properties/metadate fail을 사용하여 블록 Blob 업로드가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2385">Fix Upload block blob with properties/metadate fail on container enabled ImmutabilityPolicy.</span></span>
    -  <span data-ttu-id="184db-2386">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="184db-2386">Set-AzStorageBlobContent</span></span>
* <span data-ttu-id="184db-2387">관리 평면 API를 사용하여 Azure 파일 공유 관리를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2387">Support manage Azure File shares with Management plane API</span></span>
    -  <span data-ttu-id="184db-2388">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="184db-2388">New-AzRmStorageShare</span></span>
    -  <span data-ttu-id="184db-2389">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="184db-2389">Get-AzRmStorageShare</span></span>
    -  <span data-ttu-id="184db-2390">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="184db-2390">Update-AzRmStorageShare</span></span>
    -  <span data-ttu-id="184db-2391">Remove-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="184db-2391">Remove-AzRmStorageShare</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="184db-2392">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="184db-2392">Az.Websites</span></span>
* <span data-ttu-id="184db-2393">앱을 새 ASP로 마이그레이션할 때 웹앱 태그가 삭제되는 이슈가 해결되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2393">Fixing issue where webapp Tags were getting deleted when migrating App to new ASPwhere webapp Tags were getting deleted when migrating App to new ASP</span></span>
* <span data-ttu-id="184db-2394">Linux와 Windows에서 모두 작동하도록 Publish-AzureWebapp이 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2394">Fixing the Publish-AzureWebapp to work across Linux and windows</span></span>
* <span data-ttu-id="184db-2395">'Get-AzWebAppPublishingProfile' 참조 설명서의 예제가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2395">Update example in 'Get-AzWebAppPublishingProfile' reference documentation</span></span>

## <a name="260---august-2019"></a><span data-ttu-id="184db-2396">2.6.0 - 2019년 8월</span><span class="sxs-lookup"><span data-stu-id="184db-2396">2.6.0 - August 2019</span></span>
#### <a name="general"></a><span data-ttu-id="184db-2397">일반</span><span class="sxs-lookup"><span data-stu-id="184db-2397">General</span></span>
* <span data-ttu-id="184db-2398">여러 모듈에서 기타 오타가 수정됨</span><span class="sxs-lookup"><span data-stu-id="184db-2398">Fixed miscellaneous typos across numerous modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="184db-2399">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="184db-2399">Az.Accounts</span></span>
* <span data-ttu-id="184db-2400">Azure Functions 인증에서 사용자가 할당한 MSI가 지원됨(# 9479)</span><span class="sxs-lookup"><span data-stu-id="184db-2400">Support user-assigned MSI in Azure Functiosn Authentication (#9479)</span></span>

#### <a name="azaks"></a><span data-ttu-id="184db-2401">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="184db-2401">Az.Aks</span></span>
* <span data-ttu-id="184db-2402">'Get-AzAks' 출력 관련 문제가 해결됨</span><span class="sxs-lookup"><span data-stu-id="184db-2402">Fix issue with output for 'Get-AzAks'</span></span>
    * <span data-ttu-id="184db-2403">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/9847 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="184db-2403">More information here: https://github.com/Azure/azure-powershell/issues/9847</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="184db-2404">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="184db-2404">Az.ApiManagement</span></span>
* <span data-ttu-id="184db-2405">문제 https://github.com/Azure/azure-powershell/issues/9351 수정</span><span class="sxs-lookup"><span data-stu-id="184db-2405">Fix for issue https://github.com/Azure/azure-powershell/issues/9351</span></span>
    - <span data-ttu-id="184db-2406">productId, apiId, groupId 및 userId에 대한 제한을 적용하지 않는 .Net NuGet 버전이 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="184db-2406">Update .net nuget version, which does not enforce restrictions on productId, apiId, groupId and userId</span></span>
* <span data-ttu-id="184db-2407">**Get-AzApiManagementProduct** - API를 사용하는 제품에 대한 쿼리 지원이 추가됨</span><span class="sxs-lookup"><span data-stu-id="184db-2407">**Get-AzApiManagementProduct** - Added support for querying products using Api.</span></span>
  https://github.com/Azure/azure-powershell/issues/9482
* <span data-ttu-id="184db-2408">**New-AzApiManagementApiRevision** - 새 API 수정(https://github.com/Azure/azure-powershell/issues/9752 )을 만들 때 ApiRevisionDescription이 설정되지 않은 문제가 해결됨</span><span class="sxs-lookup"><span data-stu-id="184db-2408">**New-AzApiManagementApiRevision** - Fix for issue where ApiRevisionDescription was not being set when creating new api revision https://github.com/Azure/azure-powershell/issues/9752</span></span>
* <span data-ttu-id="184db-2409">'PsApiManagementOAuth2AuthrozationServer' 모델의 오타가 'PsApiManagementOAuth2AuthorizationServer'로 수정됨</span><span class="sxs-lookup"><span data-stu-id="184db-2409">Fixed typo in model 'PsApiManagementOAuth2AuthrozationServer' to 'PsApiManagementOAuth2AuthorizationServer'</span></span>

#### <a name="azbatch"></a><span data-ttu-id="184db-2410">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="184db-2410">Az.Batch</span></span>
* <span data-ttu-id="184db-2411">도움말 메시지 및 설명서에서 Windows를 대문자로 시작하도록 오타가 수정됨</span><span class="sxs-lookup"><span data-stu-id="184db-2411">Fixed typo in help message and documentation to capitalize Windows</span></span>

#### <a name="azcdn"></a><span data-ttu-id="184db-2412">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="184db-2412">Az.Cdn</span></span>
* <span data-ttu-id="184db-2413">CDN 모듈 변환 도우미의 오타가 수정됨</span><span class="sxs-lookup"><span data-stu-id="184db-2413">Fixed a typo in CDN module conversion helper</span></span>

#### <a name="azcompute"></a><span data-ttu-id="184db-2414">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="184db-2414">Az.Compute</span></span>
* <span data-ttu-id="184db-2415">VmssId가 New-AzVMConfig cmdlet에 추가됨</span><span class="sxs-lookup"><span data-stu-id="184db-2415">Add VmssId to New-AzVMConfig cmdlet</span></span>
* <span data-ttu-id="184db-2416">TerminateScheduledEvents 및 TerminateScheduledEventNotBeforeTimeoutInMinutes 매개 변수가 New-AzVmssConfig 및 Update-AzVmss에 추가됨</span><span class="sxs-lookup"><span data-stu-id="184db-2416">Add TerminateScheduledEvents and TerminateScheduledEventNotBeforeTimeoutInMinutes parameters to New-AzVmssConfig and Update-AzVmss</span></span>
* <span data-ttu-id="184db-2417">HyperVGeneration 속성이 VM 이미지 개체에 추가됨</span><span class="sxs-lookup"><span data-stu-id="184db-2417">Add HyperVGeneration property to VM image object</span></span>
* <span data-ttu-id="184db-2418">Host 및 HostGroup 기능이 추가됨</span><span class="sxs-lookup"><span data-stu-id="184db-2418">Add Host and HostGroup features</span></span>
    - <span data-ttu-id="184db-2419">새 cmdlet:   New-AzHostGroup, New-AzHost, Get-AzHostGroup, Get-AzHost, Remove-AzHostGroup, Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="184db-2419">New cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span></span>
    - <span data-ttu-id="184db-2420">HostId 매개 변수가 New-AzVMConfig 및 New-AzVM 추가됨</span><span class="sxs-lookup"><span data-stu-id="184db-2420">HostId parameter is added to New-AzVMConfig and New-AzVM</span></span>
* <span data-ttu-id="184db-2421">'Invoke-AzVMRunCommand' 설명서의 예제에서 올바른 매개 변수 이름을 사용하도록 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="184db-2421">Update example in 'Invoke-AzVMRunCommand' documentation to use correct parameter name</span></span>
* <span data-ttu-id="184db-2422">'Set-AzVMDiskEncryptionExtension' 및 'Set-AzVmssDiskEncryptionExtension' 참조 설명서의 '-VolumeType' 설명이 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="184db-2422">Update '-VolumeType' description in 'Set-AzVMDiskEncryptionExtension' and 'Set-AzVmssDiskEncryptionExtension' reference documentation</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="184db-2423">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="184db-2423">Az.DataFactory</span></span>
* <span data-ttu-id="184db-2424">'New-AzDataFactoryEncryptValue' 설명서에서 'Windows'를 대문자로 시작하도록 오타가 수정됨</span><span class="sxs-lookup"><span data-stu-id="184db-2424">Fix typo to capitalize 'Windows' in 'New-AzDataFactoryEncryptValue' documentation</span></span>
* <span data-ttu-id="184db-2425">ADF .Net SDK 버전이 4.1.2로 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="184db-2425">Updated ADF .Net SDK version to 4.1.2</span></span>
* <span data-ttu-id="184db-2426">자체 호스팅 통합 런타임을 SSIS Integration Runtime의 프록시로 설정할 수 있도록 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' 및 'DataProxyStagingPath' 매개 변수가 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd에 추가됨</span><span class="sxs-lookup"><span data-stu-id="184db-2426">Add parameter 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' and 'DataProxyStagingPath' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable set up Self-Hosted Integration Runtime as a proxy for SSIS Integration Runtime</span></span>
* <span data-ttu-id="184db-2427">PSTriggerRun에서 트리거된 파이프라인, 메시지 및 속성을 표시하고, PSActivityRun에서 작업 유형을 표시하도록 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="184db-2427">Updated PSTriggerRun to show the triggered pipelines, message and properties, and PSActivityRun to show the activity type</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="184db-2428">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="184db-2428">Az.DataLakeStore</span></span>
* <span data-ttu-id="184db-2429">오류 또는 원격 예외에 대한 Get-DataLakeStoreDeletedItem 중단이 수정됨</span><span class="sxs-lookup"><span data-stu-id="184db-2429">Fix hanging of Get-DataLakeStoreDeletedItem for any errors or remote exceptions.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="184db-2430">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="184db-2430">Az.EventHub</span></span>
* <span data-ttu-id="184db-2431">#9658 문제 해결: Set-AzEventHubNetworkRuleSet의 VirtualNteworkRule 매개 변수에 대한 오타</span><span class="sxs-lookup"><span data-stu-id="184db-2431">Fix for issue #9658 : Typo VirtualNteworkRule parameter in Set-AzEventHubNetworkRuleSet</span></span>
* <span data-ttu-id="184db-2432">#9558 문제 해결: Set-AzEventHubNamespace에서 PUT 대신 PATCH가 사용됨</span><span class="sxs-lookup"><span data-stu-id="184db-2432">Fix for issue #9558 : Set-AzEventHubNamespace is using PATCH instead of PUT</span></span>
* <span data-ttu-id="184db-2433">EnableKafka 매개 변수가 Set-AzEventHubNamespace cmdlet에 추가됨</span><span class="sxs-lookup"><span data-stu-id="184db-2433">added EnableKafka parameter to Set-AzEventHubNamespace cmdlet</span></span>
* <span data-ttu-id="184db-2434">#9786 문제 해결: Listen(수신 대기) 전용 권한이 있는 규칙을 만들 수 없음</span><span class="sxs-lookup"><span data-stu-id="184db-2434">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>

#### <a name="azmarketplaceordering"></a><span data-ttu-id="184db-2435">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="184db-2435">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="184db-2436">'Azure'가 모두 소문자인 설명서의 오타가 수정됨</span><span class="sxs-lookup"><span data-stu-id="184db-2436">Fixed documentation typo where 'Azure' was all lowercase letters</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="184db-2437">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="184db-2437">Az.Monitor</span></span>
* <span data-ttu-id="184db-2438">도움말 설명서에서 잘못된 매개 변수 이름이 수정됨</span><span class="sxs-lookup"><span data-stu-id="184db-2438">Fixed incorrect parameter name in help documentation</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="184db-2439">Az.Network</span><span class="sxs-lookup"><span data-stu-id="184db-2439">Az.Network</span></span>
* <span data-ttu-id="184db-2440">New-AzPrivateLinkServiceIpConfig가 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="184db-2440">Updated New-AzPrivateLinkServiceIpConfig</span></span>
    - <span data-ttu-id="184db-2441">서버 쪽에서 사용되지 않으므로 'PublicIpAddress' 매개 변수가 사용되지 않음</span><span class="sxs-lookup"><span data-stu-id="184db-2441">Deprecated the paramster 'PublicIpAddress' since this is never used in the server side.</span></span>
    - <span data-ttu-id="184db-2442">현재 IP 구성이 기본 구성인지 여부를 나타내는 하나의 선택적 'Primary' 매개 변수가 추가됨</span><span class="sxs-lookup"><span data-stu-id="184db-2442">Added one optional parameter 'Primary' that indicate the current ip configuration is primary one or not.</span></span>
* <span data-ttu-id="184db-2443">SDK의 요청 오류 예외 처리가 향상됨 - 이전의 SDK 예외가 올바르게 처리되지 않아 주요 오류 세부 정보가 표시되지 않은 문제가 해결됨</span><span class="sxs-lookup"><span data-stu-id="184db-2443">Improved handling of request error exception from SDK   -Fixes the issue that previously SDK exceptions aren't handled correctly which results in key error details not being displayed</span></span>
* <span data-ttu-id="184db-2444">올바른 IPv6 접두사 길이를 확인하기 위해 Ipv6 IP 접두사에 대한 유효성 검사 논리가 조정됨</span><span class="sxs-lookup"><span data-stu-id="184db-2444">Adjusted validation logic for Ipv6 IP Prefix to check for correct IPv6 prefix length.</span></span>
* <span data-ttu-id="184db-2445">Get-AzVirtualNetworkSubnetConfig가 업데이트됨: 서브넷 리소스 ID별로 가져오도록 설정되는 매개 변수 세트가 추가됨</span><span class="sxs-lookup"><span data-stu-id="184db-2445">Updated Get-AzVirtualNetworkSubnetConfig: Added parameter set to get by subnet resource id.</span></span>
* <span data-ttu-id="184db-2446">AzNetworkServiceTag의 Location(위치) 매개 변수에 대한 설명이 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="184db-2446">Updated description of Location parameter for AzNetworkServiceTag</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="184db-2447">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="184db-2447">Az.OperationalInsights</span></span>
* <span data-ttu-id="184db-2448">'New-AzOperationalInsightsLinuxSyslogDataSource'에 대한 설명서가 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="184db-2448">Updated documentation for 'New-AzOperationalInsightsLinuxSyslogDataSource'</span></span>
    - <span data-ttu-id="184db-2449">예제가 추가됨</span><span class="sxs-lookup"><span data-stu-id="184db-2449">Added example</span></span>
    - <span data-ttu-id="184db-2450">'-Name' 매개 변수에 대한 설명이 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="184db-2450">Updated description for '-Name' parameter</span></span>
* <span data-ttu-id="184db-2451">New-AzOperationalInsightsWindowsEventDataSource에 대한 예제가 추가됨</span><span class="sxs-lookup"><span data-stu-id="184db-2451">Added an example for New-AzOperationalInsightsWindowsEventDataSource</span></span>
* <span data-ttu-id="184db-2452">New-AzOperationalInsightsWindowsEventDataSource의 -Name 매개 변수에 대한 설명이 변경됨</span><span class="sxs-lookup"><span data-stu-id="184db-2452">Changed the description of the -Name parameter for New-AzOperationalInsightsWindowsEventDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="184db-2453">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="184db-2453">Az.RecoveryServices</span></span>
* <span data-ttu-id="184db-2454">'Get-AzRecoveryServicesBackupJobDetail.md'가 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="184db-2454">Update 'Get-AzRecoveryServicesBackupJobDetail.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="184db-2455">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="184db-2455">Az.Resources</span></span>
* <span data-ttu-id="184db-2456">Microsoft 리소스에 대한 새 2019-05-10 API 버전 지원이 추가됨</span><span class="sxs-lookup"><span data-stu-id="184db-2456">Add support for new api version 2019-05-10 for Microsoft.Resource</span></span>
    - <span data-ttu-id="184db-2457">변수, 리소스 및 속성에 대한 'copy.count = 0' 지원이 추가됨</span><span class="sxs-lookup"><span data-stu-id="184db-2457">Add support for 'copy.count = 0' for variables, resources and properties</span></span>
    - <span data-ttu-id="184db-2458">'condition = false' 또는 'copy.count = 0'인 리소스가 완료 모드에서 삭제됨</span><span class="sxs-lookup"><span data-stu-id="184db-2458">Resources with 'condition = false' or 'copy.count = 0' will be deleted in complete mode</span></span>
* <span data-ttu-id="184db-2459">정책을 구독 수준에서 도움말 문서에 할당하는 예제가 추가됨</span><span class="sxs-lookup"><span data-stu-id="184db-2459">Add an example of assigning policy at subscription level to help doc</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="184db-2460">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="184db-2460">Az.ServiceBus</span></span>
* <span data-ttu-id="184db-2461">#9658 문제 해결: Set-AzServiceBusNetworkRuleSet의 VirtualNetworkRule 매개 변수에 대한 오타</span><span class="sxs-lookup"><span data-stu-id="184db-2461">Fix for issue #9658 : Typo VirtualNetworkRule parameter in Set-AzServiceBusNetworkRuleSet</span></span>
* <span data-ttu-id="184db-2462">#9786 문제 해결: Listen(수신 대기) 전용 권한이 있는 규칙을 만들 수 없음</span><span class="sxs-lookup"><span data-stu-id="184db-2462">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>
* <span data-ttu-id="184db-2463">큐 및 토픽에 대한 이름 가용성을 확인하는 새 'Test-AzServiceBusNameAvailability' 명령이 추가됨</span><span class="sxs-lookup"><span data-stu-id="184db-2463">Added new command 'Test-AzServiceBusNameAvailability' to check the name availability for queue and topic</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="184db-2464">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="184db-2464">Az.ServiceFabric</span></span>
* <span data-ttu-id="184db-2465">노드 유형 추가 cmdlet 버그 수정:</span><span class="sxs-lookup"><span data-stu-id="184db-2465">Fix add node type cmdlet bugs:</span></span>
    - <span data-ttu-id="184db-2466">서비스 패브릭 클러스터와 관련이 없는 다른 vmss가 리소스 그룹에 있을 때 발생하는 NullReferenceException 버그</span><span class="sxs-lookup"><span data-stu-id="184db-2466">NullReferenceException bug when resource group had other vmss not related to the service fabric cluster.</span></span> <span data-ttu-id="184db-2467">문제 해결: https://github.com/Azure/azure-powershell/issues/8681</span><span class="sxs-lookup"><span data-stu-id="184db-2467">Fixes issue: https://github.com/Azure/azure-powershell/issues/8681</span></span>
    - <span data-ttu-id="184db-2468">virtualNetwork가 클러스터의 다른 리소스 그룹에 있을 때 cmdlet이 실패하는 버그가 수정됨</span><span class="sxs-lookup"><span data-stu-id="184db-2468">Fix bug where cmdlet failed if virtualNetwork was in a different resource group that the cluster.</span></span> <span data-ttu-id="184db-2469">문제 해결: https://github.com/Azure/azure-powershell/issues/8407</span><span class="sxs-lookup"><span data-stu-id="184db-2469">fixes issue: https://github.com/Azure/azure-powershell/issues/8407</span></span>
    - <span data-ttu-id="184db-2470">Add-AzServiceFabricApplicationCertificate cmdlet이 사용되지 않음</span><span class="sxs-lookup"><span data-stu-id="184db-2470">Deprecating Add-AzServiceFabricApplicationCertificate cmdlet</span></span>

#### <a name="azsql"></a><span data-ttu-id="184db-2471">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="184db-2471">Az.Sql</span></span>
* <span data-ttu-id="184db-2472">이전의 Auditing(감사) cmdlet에 대한 설명서가 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="184db-2472">Update documentation of old Auditing cmdlets.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="184db-2473">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="184db-2473">Az.Storage</span></span>
* <span data-ttu-id="184db-2474">더 많은 시나리오를 cmdlet 예제에 추가하고 매개 변수 설명을 업데이트하여 Get/Close-AzStorageFileHandle에 대한 도움말이 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="184db-2474">Update help for Get/Close-AzStorageFileHandle, by add more scenarios to cmdlet examples and update parameter descriptions</span></span>
* <span data-ttu-id="184db-2475">Blob 업로드 및 Blob 복사에서 StandardBlobTier가 지원됨</span><span class="sxs-lookup"><span data-stu-id="184db-2475">Support StandardBlobTier in upload blob and copy blob</span></span>
    -  <span data-ttu-id="184db-2476">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="184db-2476">Set-AzStorageBlobContent</span></span>
    -  <span data-ttu-id="184db-2477">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="184db-2477">Start-AzStorageBlobCopy</span></span>
* <span data-ttu-id="184db-2478">Blob 복사에서 우선 순위 리하이드레이션이 지원됨</span><span class="sxs-lookup"><span data-stu-id="184db-2478">Support Rehydrate Priority in copy blob</span></span>
    -  <span data-ttu-id="184db-2479">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="184db-2479">Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="184db-2480">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="184db-2480">Az.Websites</span></span>
* <span data-ttu-id="184db-2481">Set-AzWebApp 및 Set-AzWebAppSlot에서 -AppSettings 매개 변수에 대한 설명이 추가됨</span><span class="sxs-lookup"><span data-stu-id="184db-2481">Add clarification around -AppSettings parameter in Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <a name="250---july-2019"></a><span data-ttu-id="184db-2482">2.5.0 - 2019년 7월</span><span class="sxs-lookup"><span data-stu-id="184db-2482">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="184db-2483">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="184db-2483">Az.Accounts</span></span>
* <span data-ttu-id="184db-2484">ClientRuntime의 최신 버전을 사용하도록 일반적인 코드를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2484">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="184db-2485">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="184db-2485">Az.ApplicationInsights</span></span>
* <span data-ttu-id="184db-2486">'Remove-AzApplicationInsightsApiKey' 설명서의 예제 오타 수정</span><span class="sxs-lookup"><span data-stu-id="184db-2486">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span>

#### <a name="azautomation"></a><span data-ttu-id="184db-2487">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="184db-2487">Az.Automation</span></span>
* <span data-ttu-id="184db-2488">리소스 문자열의 오타 수정</span><span class="sxs-lookup"><span data-stu-id="184db-2488">Fix typo in resource string</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="184db-2489">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="184db-2489">Az.CognitiveServices</span></span>
* <span data-ttu-id="184db-2490">NetworkRuleSet 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2490">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="184db-2491">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="184db-2491">Az.Compute</span></span>
* <span data-ttu-id="184db-2492">VM 인스턴스 보기 개체의 누락된 속성(ComputerName, OsName, OsVersion 및 HyperVGeneration)을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2492">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="184db-2493">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="184db-2493">Az.ContainerRegistry</span></span>
* <span data-ttu-id="184db-2494">복제 매개 변수의 Remove-AzContainerRegistryReplication에서 오타 수정</span><span class="sxs-lookup"><span data-stu-id="184db-2494">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="184db-2495">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/9633 을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="184db-2495">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="184db-2496">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="184db-2496">Az.DataFactory</span></span>
* <span data-ttu-id="184db-2497">ADF .Net SDK 버전을 4.1.0으로 업데이트</span><span class="sxs-lookup"><span data-stu-id="184db-2497">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="184db-2498">'Get-AzDataFactoryV2PipelineRun' 설명서의 오타 수정</span><span class="sxs-lookup"><span data-stu-id="184db-2498">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="184db-2499">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="184db-2499">Az.EventHub</span></span>
* <span data-ttu-id="184db-2500">SAS 토큰을 생성하기 위해 추가된 새로운 cmmdlet 추가: New-AzEventHubAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="184db-2500">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="184db-2501">'관리'만 지정된 경우 authorizationrules 권한에 대한 확인 및 오류 메시지 추가</span><span class="sxs-lookup"><span data-stu-id="184db-2501">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="184db-2502">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="184db-2502">Az.KeyVault</span></span>
* <span data-ttu-id="184db-2503">인증서 정책에 대한 KeySize 지정을 위한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="184db-2503">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="184db-2504">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="184db-2504">Az.LogicApp</span></span>
* <span data-ttu-id="184db-2505">모든 맵 유형을 나열하도록 Get-AzIntegrationAccountMap 수정</span><span class="sxs-lookup"><span data-stu-id="184db-2505">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="184db-2506">필터링을 위해 새 MapType 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="184db-2506">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="184db-2507">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="184db-2507">Az.ManagedServices</span></span>
* <span data-ttu-id="184db-2508">API 버전 2019-06-01(GA)에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="184db-2508">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="184db-2509">Az.Network</span><span class="sxs-lookup"><span data-stu-id="184db-2509">Az.Network</span></span>
* <span data-ttu-id="184db-2510">프라이빗 엔드포인트 및 프라이빗 링크 서비스에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="184db-2510">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="184db-2511">새로운 cmdlet</span><span class="sxs-lookup"><span data-stu-id="184db-2511">New cmdlets</span></span>
        - <span data-ttu-id="184db-2512">Set-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="184db-2512">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="184db-2513">Set-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="184db-2513">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="184db-2514">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="184db-2514">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="184db-2515">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="184db-2515">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="184db-2516">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="184db-2516">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="184db-2517">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="184db-2517">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="184db-2518">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="184db-2518">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="184db-2519">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="184db-2519">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="184db-2520">기능에 대한 새로운 명령이 업데이트됨: Virtualnetwork의 서브넷에 있는 PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies 플래그</span><span class="sxs-lookup"><span data-stu-id="184db-2520">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="184db-2521">업데이트된 New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="184db-2521">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="184db-2522">이 서브넷의 프라이빗 엔드포인트에 네트워크 정책을 적용할지 여부를 나타내는 선택적 매개 변수 -PrivateEndpointNetworkPoliciesFlag가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2522">Added optional parameter -PrivateEndpointNetworkPoliciesFlag that configures whether to apply network policies on private endpoint in this subnet.</span></span>
        - <span data-ttu-id="184db-2523">이 서브넷의 프라이빗 연결 서비스에 네트워크 정책을 적용할지 여부를 나타내는 선택적 매개 변수 -PrivateLinkServiceNetworkPoliciesFlag가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2523">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag that configures whether to apply network policies network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="184db-2524">AzPrivateLinkService의 cmdlet 매개 변수 'ServiceName'이 이전 버전과의 호환성을 위해 별칭 'ServiceName'을 사용한 'Name'으로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2524">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="184db-2525">네트워크 보안 규칙 구성에 ICMP 프로토콜 사용</span><span class="sxs-lookup"><span data-stu-id="184db-2525">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="184db-2526">다음 Cmdlet이 업데이트 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2526">Updated cmdlets</span></span>
        - <span data-ttu-id="184db-2527">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="184db-2527">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="184db-2528">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="184db-2528">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="184db-2529">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="184db-2529">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="184db-2530">New-AzVirtualNetworkGatewayConnection에 대한 구성 가능한 매개 변수로 ConnectionProtocolType (Ikev1/Ikev2) 추가</span><span class="sxs-lookup"><span data-stu-id="184db-2530">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="184db-2531">LoadBalancerFrontendIpConfiguration에 PrivateIpAddressVersion 추가</span><span class="sxs-lookup"><span data-stu-id="184db-2531">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="184db-2532">업데이트된 cmdlet:</span><span class="sxs-lookup"><span data-stu-id="184db-2532">Updated cmdlet:</span></span>
        - <span data-ttu-id="184db-2533">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="184db-2533">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="184db-2534">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="184db-2534">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="184db-2535">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="184db-2535">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="184db-2536">프로브에서 사용자 지정 포트를 지원하기 위한 Application Gateway New-AzApplicationGatewayProbeConfig 명령 업데이트</span><span class="sxs-lookup"><span data-stu-id="184db-2536">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="184db-2537">업데이트된 New-AzApplicationGatewayProbeConfig: 백 엔드 서버 검색에 사용되는 선택적 매개 변수 포트가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2537">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="184db-2538">이 매개 변수는 Standard_V2 및 WAF_V2 SKU에 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2538">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="184db-2539">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="184db-2539">Az.OperationalInsights</span></span>
* <span data-ttu-id="184db-2540">저장된 검색의 기본 버전이 1로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2540">Updated default version for saved searches to be 1.</span></span>
* <span data-ttu-id="184db-2541">사용자 지정 로그 null regex 처리가 수정됨</span><span class="sxs-lookup"><span data-stu-id="184db-2541">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="184db-2542">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="184db-2542">Az.RecoveryServices</span></span>
* <span data-ttu-id="184db-2543">'Get-AzRecoveryServicesBackupJob.md' 업데이트</span><span class="sxs-lookup"><span data-stu-id="184db-2543">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="184db-2544">'Get-AzRecoveryServicesBackupContainer.md' 업데이트</span><span class="sxs-lookup"><span data-stu-id="184db-2544">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="184db-2545">'Get-AzRecoveryServicesVault.md' 업데이트</span><span class="sxs-lookup"><span data-stu-id="184db-2545">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="184db-2546">'Wait-AzRecoveryServicesBackupJob.md' 업데이트</span><span class="sxs-lookup"><span data-stu-id="184db-2546">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="184db-2547">'Set-AzRecoveryServicesVaultContext.md' 업데이트</span><span class="sxs-lookup"><span data-stu-id="184db-2547">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="184db-2548">'Get-AzRecoveryServicesBackupItem.md' 업데이트</span><span class="sxs-lookup"><span data-stu-id="184db-2548">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="184db-2549">'Get-AzRecoveryServicesBackupRecoveryPoint.md' 업데이트</span><span class="sxs-lookup"><span data-stu-id="184db-2549">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="184db-2550">'Restore-AzRecoveryServicesBackupItem.md' 업데이트</span><span class="sxs-lookup"><span data-stu-id="184db-2550">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="184db-2551">Azure 파일 공유용 컨테이너를 등록 취소하기 위해 서비스 요청 업데이트</span><span class="sxs-lookup"><span data-stu-id="184db-2551">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="184db-2552">'Set-AzRecoveryServicesAsrAlertSetting.md' 업데이트</span><span class="sxs-lookup"><span data-stu-id="184db-2552">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="184db-2553">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="184db-2553">Az.Resources</span></span>
- <span data-ttu-id="184db-2554">'New-AzResourceGroupDeployment' 설명서에서 참조된 누락 cmdlet 제거</span><span class="sxs-lookup"><span data-stu-id="184db-2554">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="184db-2555">새 API 버전 2019-01-01을 사용하도록 정책 cmdlet 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="184db-2555">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="184db-2556">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="184db-2556">Az.ServiceBus</span></span>
* <span data-ttu-id="184db-2557">SAS 토큰을 생성하기 위해 추가된 새로운 cmmdlet 추가: New-AzServiceBusAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="184db-2557">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="184db-2558">'관리'만 지정된 경우 authorizationrules 권한에 대한 확인 및 오류 메시지 추가</span><span class="sxs-lookup"><span data-stu-id="184db-2558">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="184db-2559">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="184db-2559">Az.Sql</span></span>
* <span data-ttu-id="184db-2560">Set-AzSqlDatabaseSecondary cmdlet에 대한 누락된 예제 수정</span><span class="sxs-lookup"><span data-stu-id="184db-2560">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="184db-2561">이메일 주소를 제공하지 않고 설정된 취약성 평가 반복 검색 수정</span><span class="sxs-lookup"><span data-stu-id="184db-2561">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="184db-2562">경고 메시지의 작은 오타를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2562">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="184db-2563">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="184db-2563">Az.Storage</span></span>
* <span data-ttu-id="184db-2564">'Get-AzStorageAccount'에 대한 참조 설명서의 예제를 업데이트하여 올바른 매개 변수 이름 사용</span><span class="sxs-lookup"><span data-stu-id="184db-2564">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="184db-2565">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="184db-2565">Az.StorageSync</span></span>
* <span data-ttu-id="184db-2566">Invoke-AzStorageSyncChangeDetection cmdlet을 추가하는 중입니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2566">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="184db-2567">TierFilesOlderThanDays를 기념하는 문제 9551 수정</span><span class="sxs-lookup"><span data-stu-id="184db-2567">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="184db-2568">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="184db-2568">Az.Websites</span></span>
* <span data-ttu-id="184db-2569">Get-AzWebApp 및 Set-AzWebApp에서 일부 SiteConfig 속성을 반환하지 않은 버그 수정</span><span class="sxs-lookup"><span data-stu-id="184db-2569">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="184db-2570">Get-AzDeletedWebApp 및 Restore-AzDeletedWebApp에 새 위치 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="184db-2570">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="184db-2571">AzWebApp-IncludeSourceWebAppSlots을 사용하여 웹앱 슬롯을 복제하는 버그를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2571">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="184db-2572">2.4.0 - 2019년 7월</span><span class="sxs-lookup"><span data-stu-id="184db-2572">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="184db-2573">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="184db-2573">Az.Accounts</span></span>
* <span data-ttu-id="184db-2574">프로필 cmdlet에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="184db-2574">Add support for profile cmdlets</span></span>
* <span data-ttu-id="184db-2575">생성된 cmdlet에서 환경 및 데이터 평면에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="184db-2575">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="184db-2576">Windows PowerShell의 데이터 평면 cmdlet에대해 일부 경우 잘못된 엔드포인트가 사용되는 버그 수정</span><span class="sxs-lookup"><span data-stu-id="184db-2576">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="184db-2577">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="184db-2577">Az.Advisor</span></span>
* <span data-ttu-id="184db-2578">Az.Advisor의 GA 릴리스</span><span class="sxs-lookup"><span data-stu-id="184db-2578">GA release of Az.Advisor</span></span>
* <span data-ttu-id="184db-2579">이 모듈은 이제 롤업 `Az` 모듈의 일부로 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2579">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="184db-2580">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="184db-2580">Az.ApiManagement</span></span>
* <span data-ttu-id="184db-2581">문제 https://github.com/Azure/azure-powershell/issues/8671 수정</span><span class="sxs-lookup"><span data-stu-id="184db-2581">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="184db-2582">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="184db-2582">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="184db-2583">사용자 및 제품별 구독을 쿼리하기 위한 지원이 추가됨</span><span class="sxs-lookup"><span data-stu-id="184db-2583">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="184db-2584">범위 '/', '/ api, '/ api/echo api'를 사용하여 쿼리하기 위한 지원이 추가됨</span><span class="sxs-lookup"><span data-stu-id="184db-2584">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="184db-2585">[https://github.com/Azure/azure-powershell/issues/9307](https://github.com/Azure/azure-powershell/issues/9307 ) 및 https://github.com/Azure/azure-powershell/issues/8432 문제 수정</span><span class="sxs-lookup"><span data-stu-id="184db-2585">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="184db-2586">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="184db-2586">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="184db-2587">Apis를 가져올 때 'ApiVersion' 및 'ApiVersionSetId'를 지정하기 위한 지원이 추가됨</span><span class="sxs-lookup"><span data-stu-id="184db-2587">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="184db-2588">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="184db-2588">Az.Automation</span></span>
* <span data-ttu-id="184db-2589">문자열 값을 처리하기 위해 Set-AzAutomationConnectionFieldValue cmdlet 버그를 수정했습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2589">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="184db-2590">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="184db-2590">Az.Compute</span></span>
* <span data-ttu-id="184db-2591">New-AzImageConfig에 HyperVGeneration 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="184db-2591">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="184db-2592">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="184db-2592">Az.DataFactory</span></span>
* <span data-ttu-id="184db-2593">get activity runs, get pipeline runs, get trigger runs ADF cmdlet의 출력을 업데이트하여 Select-Object pipe를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2593">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="184db-2594">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="184db-2594">Az.EventGrid</span></span>
* <span data-ttu-id="184db-2595">'New-AzEventGridSubcription' 설명서의 오타 수정</span><span class="sxs-lookup"><span data-stu-id="184db-2595">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="184db-2596">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="184db-2596">Az.IotHub</span></span>
* <span data-ttu-id="184db-2597">권한 부여 정책 키를 다시 생성하기 위한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="184db-2597">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="184db-2598">Az.Network</span><span class="sxs-lookup"><span data-stu-id="184db-2598">Az.Network</span></span>
* <span data-ttu-id="184db-2599">'RoutingPreference'를 공용 IP 태그에 추가함</span><span class="sxs-lookup"><span data-stu-id="184db-2599">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="184db-2600">'Get-AzNetworkServiceTag' 참조 설명서의 예제 개선</span><span class="sxs-lookup"><span data-stu-id="184db-2600">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="184db-2601">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="184db-2601">Az.PolicyInsights</span></span>
* <span data-ttu-id="184db-2602">Get-AzPolicyState의 null 참조 문제 해결</span><span class="sxs-lookup"><span data-stu-id="184db-2602">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="184db-2603">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/9446 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="184db-2603">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="184db-2604">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="184db-2604">Az.OperationalInsights</span></span>
* <span data-ttu-id="184db-2605">Get-AzOperationalInsightsDataSource에 반환된 CustomLog datasource 모델 수정됨</span><span class="sxs-lookup"><span data-stu-id="184db-2605">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="184db-2606">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="184db-2606">Az.RecoveryServices</span></span>
* <span data-ttu-id="184db-2607">IaaSVMs에 대한 get-policy 명령 수정</span><span class="sxs-lookup"><span data-stu-id="184db-2607">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="184db-2608">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="184db-2608">Az.Resources</span></span>
    - <span data-ttu-id="184db-2609">Get-AzPolicyState -Top 매개 변수에 대한 도움말 텍스트 수정</span><span class="sxs-lookup"><span data-stu-id="184db-2609">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="184db-2610">Get-AzPolicyAlias에 대한 클라이언트 쪽 페이징 지원 추가</span><span class="sxs-lookup"><span data-stu-id="184db-2610">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="184db-2611">Set-AzPolicyAssignment, -PolicyParameters 및 -PolicyParametersObject에 대한 새 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="184db-2611">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="184db-2612">Policy cmdlet에 대한 몇 가지 문서 및 예제 업데이트</span><span class="sxs-lookup"><span data-stu-id="184db-2612">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="184db-2613">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="184db-2613">Az.ServiceBus</span></span>
* <span data-ttu-id="184db-2614">문제 #4938 수정 - MaxSizeInMegabytes를 설정할 때 New-AzureRmServiceBusQueue가 BadRequest 반환</span><span class="sxs-lookup"><span data-stu-id="184db-2614">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="184db-2615">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="184db-2615">Az.Sql</span></span>
* <span data-ttu-id="184db-2616">미리 보기 릴리스에서 공개 릴리스로 인스턴스 장애 조치(Failover) 그룹 cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="184db-2616">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="184db-2617">새 cmdlet으로 Azure SQL Server\Database Auditing을 지원하세요.</span><span class="sxs-lookup"><span data-stu-id="184db-2617">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="184db-2618">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="184db-2618">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="184db-2619">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="184db-2619">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="184db-2620">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="184db-2620">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="184db-2621">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="184db-2621">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="184db-2622">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="184db-2622">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="184db-2623">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="184db-2623">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="184db-2624">취약성 평가 설정에서 이메일 제약 조건 제거</span><span class="sxs-lookup"><span data-stu-id="184db-2624">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="184db-2625">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="184db-2625">Az.Storage</span></span>
* <span data-ttu-id="184db-2626">다음 cmdlet에서 2개의 매개 변수 '-IndexDocument' 및 '-ErrorDocument404Path'를 필수에서 선택으로 변경하세요.</span><span class="sxs-lookup"><span data-stu-id="184db-2626">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="184db-2627">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="184db-2627">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="184db-2628">예제를 추가하여 Get-AzStorageBlobContent의 도움말 업데이트</span><span class="sxs-lookup"><span data-stu-id="184db-2628">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="184db-2629">StorageException으로 cmdlet이 실패한 경우 자세한 오류 정보 표시</span><span class="sxs-lookup"><span data-stu-id="184db-2629">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="184db-2630">Azure Files AAD DS 인증으로 스토리지 계정 생성 또는 업데이트 지원</span><span class="sxs-lookup"><span data-stu-id="184db-2630">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="184db-2631">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="184db-2631">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="184db-2632">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="184db-2632">Set-AzStorageAccount</span></span>
* <span data-ttu-id="184db-2633">파일 공유, 파일 디렉터리 또는 파일의 목록 지원 또는 파일 핸들 닫기</span><span class="sxs-lookup"><span data-stu-id="184db-2633">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="184db-2634">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="184db-2634">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="184db-2635">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="184db-2635">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="184db-2636">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="184db-2636">Az.StorageSync</span></span>
* <span data-ttu-id="184db-2637">이 모듈은 이제 롤업 `Az` 모듈의 일부로 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2637">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="184db-2638">2.3.2 - 2019년 6월</span><span class="sxs-lookup"><span data-stu-id="184db-2638">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="184db-2639">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="184db-2639">Az.Accounts</span></span>
* <span data-ttu-id="184db-2640">함수 호출에 대해 일부 경우 잘못된 URL이 사용되는 버그 수정</span><span class="sxs-lookup"><span data-stu-id="184db-2640">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="184db-2641">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/8983 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="184db-2641">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="184db-2642">AzureRM에서 Az cmdlet으로의 별칭 문제 해결</span><span class="sxs-lookup"><span data-stu-id="184db-2642">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="184db-2643">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="184db-2643">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="184db-2644">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="184db-2644">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="184db-2645">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="184db-2645">Az.Compute</span></span>
* <span data-ttu-id="184db-2646">New-AzVm 및 New-AzVmss 단순 매개 변수 집합은 이제 'ProximityPlacementGroup'매개 변수를 허용합니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2646">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="184db-2647">'New-AzVM' 참조 설명서에서 오타 수정</span><span class="sxs-lookup"><span data-stu-id="184db-2647">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="184db-2648">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="184db-2648">Az.Dns</span></span>
* <span data-ttu-id="184db-2649">'Set-AzDnsZone' 도움말 예제의 오타가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2649">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="184db-2650">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="184db-2650">Az.EventGrid</span></span>
* <span data-ttu-id="184db-2651">2019-06-01 API 버전을 사용하도록 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2651">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="184db-2652">새 cmdlet:</span><span class="sxs-lookup"><span data-stu-id="184db-2652">New cmdlets:</span></span>
    - <span data-ttu-id="184db-2653">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="184db-2653">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="184db-2654">새 Azure Event Grid 도메인을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2654">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="184db-2655">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="184db-2655">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="184db-2656">Event Grid 도메인의 세부 정보를 가져오거나 현재 Azure 구독의 모든 Event Grid 도메인 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2656">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="184db-2657">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="184db-2657">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="184db-2658">Azure Event Grid 도메인을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2658">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="184db-2659">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="184db-2659">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="184db-2660">Azure Event Grid 도메인에 대한 공유 액세스 키를 다시 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2660">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="184db-2661">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="184db-2661">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="184db-2662">Event Grid 도메인 이벤트를 게시하는 데 사용되는 공유 액세스 키를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2662">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="184db-2663">New-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="184db-2663">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="184db-2664">새 Azure Event Grid 도메인 토픽을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2664">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="184db-2665">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="184db-2665">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="184db-2666">Event Grid 도메인 토픽의 세부 사항을 가져오거나, 현재 Azure의 특정 Event Grid 도메인 아래의 모든 Event Grid 도메인 토픽 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2666">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span>
    - <span data-ttu-id="184db-2667">Remove-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="184db-2667">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="184db-2668">기존 Azure Event Grid 도메인 토픽을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2668">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="184db-2669">다음 Cmdlet이 업데이트 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2669">Updated cmdlets:</span></span>
    - <span data-ttu-id="184db-2670">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="184db-2670">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="184db-2671">새로운 Event Grid 도메인 및 Event Grid 도메인 토픽에 대한 파이핑을 지원하기 위해 새로운 필수 매개 변수를 추가하여 이러한 리소스 아래에 새 이벤트 구독을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2671">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="184db-2672">새로운 Event Grid 도메인 이름 및 Event Grid 도메인 토픽 이름을 지정하기 위해 새로운 필수 매개 변수를 추가하여 이러한 리소스 아래에 새 이벤트 구독을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2672">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="184db-2673">기존 매개 변수(예: EndPointType, SubjectBeginsWith 등)를 재사용할 수 있도록 도메인 및 도메인 토픽에 대한 새로운 매개 변수 집합을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2673">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="184db-2674">지정을 위한 새로운 선택적 매개 변수를 추가</span><span class="sxs-lookup"><span data-stu-id="184db-2674">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="184db-2675">이벤트 구독 만료 날짜,</span><span class="sxs-lookup"><span data-stu-id="184db-2675">Event subscription expiration date,</span></span>
            - <span data-ttu-id="184db-2676">고급 필터링 매개 변수.</span><span class="sxs-lookup"><span data-stu-id="184db-2676">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="184db-2677">대상으로 servicebusqueue에 대한 새 열거형을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2677">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="184db-2678">-IncludedEventType 옵션에서 'All' 사용을 허용하지 않고 다음으로 대체함</span><span class="sxs-lookup"><span data-stu-id="184db-2678">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span>
    - <span data-ttu-id="184db-2679">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="184db-2679">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="184db-2680">결과 페이지 매김 및 필터링을 지원하는 새로운 선택적 매개 변수(Top, ODataQuery 및 NextLink)를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2680">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="184db-2681">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="184db-2681">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="184db-2682">Event Grid 도메인 및 Event Grid 도메인 토픽에 대한 파이핑을 지원하기 위해 새로운 필수 매개 변수를 추가하여 이러한 리소스 아래에 기존 이벤트 구독을 제거할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2682">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="184db-2683">Event Grid 도메인 이름 및 Event Grid 도메인 토픽 이름을 지정하기 위해 새로운 필수 매개 변수를 추가하여 이러한 리소스 아래에 기존 이벤트 구독을 제거할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2683">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="184db-2684">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="184db-2684">Az.FrontDoor</span></span>
* <span data-ttu-id="184db-2685">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="184db-2685">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="184db-2686">변환 지원 및 새 연산자 자동 완성 값(RegEx)을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2686">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="184db-2687">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="184db-2687">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="184db-2688">새 자동 완성 값 추가</span><span class="sxs-lookup"><span data-stu-id="184db-2688">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="184db-2689">Az.Network</span><span class="sxs-lookup"><span data-stu-id="184db-2689">Az.Network</span></span>
* <span data-ttu-id="184db-2690">Microsoft Azure Virtual Network 게이트웨이 리소스에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="184db-2690">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="184db-2691">새로운 cmdlet</span><span class="sxs-lookup"><span data-stu-id="184db-2691">New cmdlets</span></span>
        - <span data-ttu-id="184db-2692">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="184db-2692">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="184db-2693">AvailablePrivateEndpointType 추가</span><span class="sxs-lookup"><span data-stu-id="184db-2693">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="184db-2694">새로운 cmdlet</span><span class="sxs-lookup"><span data-stu-id="184db-2694">New cmdlets</span></span>
        - <span data-ttu-id="184db-2695">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="184db-2695">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="184db-2696">PrivatePrivateLinkService 추가</span><span class="sxs-lookup"><span data-stu-id="184db-2696">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="184db-2697">새로운 cmdlet</span><span class="sxs-lookup"><span data-stu-id="184db-2697">New cmdlets</span></span>
        - <span data-ttu-id="184db-2698">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="184db-2698">Get-AzPrivateLinkService</span></span>
        - <span data-ttu-id="184db-2699">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="184db-2699">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="184db-2700">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="184db-2700">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="184db-2701">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="184db-2701">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="184db-2702">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="184db-2702">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="184db-2703">PrivateEndpoint 추가</span><span class="sxs-lookup"><span data-stu-id="184db-2703">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="184db-2704">새로운 cmdlet</span><span class="sxs-lookup"><span data-stu-id="184db-2704">New cmdlets</span></span>
        - <span data-ttu-id="184db-2705">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="184db-2705">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="184db-2706">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="184db-2706">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="184db-2707">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="184db-2707">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="184db-2708">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="184db-2708">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="184db-2709">기능에 대한 새로운 명령이 업데이트됨: VpnConnection 상의 UseLocalAzureIpAddress 플래그</span><span class="sxs-lookup"><span data-stu-id="184db-2709">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="184db-2710">New-AzVpnConnection이 업데이트됨: 선택적 매개 변수 -UseLocalAzureIpAddress를 추가하여 로컬 Azure IP 주소가 연결을 시작하는 동안 소스 주소로 사용되어야 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2710">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="184db-2711">Set-AzVpnConnection이 업데이트됨: 선택적 매개 변수 -UseLocalAzureIpAddress를 추가하여 로컬 Azure IP 주소가 연결을 시작하는 동안 소스 주소로 사용되어야 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2711">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="184db-2712">ExpressRoute 피어링에 읽기 전용 필드 PeeredConnections가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2712">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="184db-2713">ExpressRoute에 읽기 전용 필드 GlobalReachEnabled가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2713">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="184db-2714">ExpressRouteCircuit 모델에서 AllowGlobalReach 필드의 사용 중단을 부르는 호환성이 손상되는 변경 속성이 추가됨</span><span class="sxs-lookup"><span data-stu-id="184db-2714">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="184db-2715">AzApplicationGatewayRedirectConfiguration cmdlet에서 TargetListenerID를 사용하는 중의 8756 오류 문제가 해결됨</span><span class="sxs-lookup"><span data-stu-id="184db-2715">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="184db-2716">다시 쓰기 규칙 세트가 설정되지 못하게 하는 New-AzApplicationGatewayPathRuleConfig의 버그를 수정했습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2716">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="184db-2717">NetworkInterfaceIpConfiguration에 VirtualNetworkTaps가 표시되는 방식이 수정됨</span><span class="sxs-lookup"><span data-stu-id="184db-2717">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="184db-2718">모든 파트를 나열하도록 Cortex Get cmdlet이 수정됨</span><span class="sxs-lookup"><span data-stu-id="184db-2718">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="184db-2719">ExpressRouteGateways, VpnGateway에 대한 VirtualHub 참조 생성 수정됨</span><span class="sxs-lookup"><span data-stu-id="184db-2719">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="184db-2720">AzureFirewall 및 NatGateway의 가용성 영역에 대한 지원 추가됨</span><span class="sxs-lookup"><span data-stu-id="184db-2720">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="184db-2721">Get-AzNetworkServiceTag cmdlet 추가됨</span><span class="sxs-lookup"><span data-stu-id="184db-2721">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="184db-2722">Azure Firewall에 대한 여러 공용 IP 주소에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="184db-2722">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="184db-2723">New-AzFirewall cmdlet이 업데이트됨:</span><span class="sxs-lookup"><span data-stu-id="184db-2723">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="184db-2724">하나 이상의 공용 IP 주소 개체를 허용하는 매개 변수 -PublicIpAddress 추가됨</span><span class="sxs-lookup"><span data-stu-id="184db-2724">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="184db-2725">Virtual Network 개체를 허용하는 매개 변수 -VirtualNetwork 추가됨</span><span class="sxs-lookup"><span data-stu-id="184db-2725">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="184db-2726">방화벽 개체에 AddPublicIpAddress 및 RemovePublicIpAddress 메서드 추가됨 - 공용 IP 주소 개체를 입력으로 허용</span><span class="sxs-lookup"><span data-stu-id="184db-2726">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="184db-2727">매개 변수 -PublicIpName 및 -VirtualNetworkName이 더 이상 사용되지 않음</span><span class="sxs-lookup"><span data-stu-id="184db-2727">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span>
* <span data-ttu-id="184db-2728">기능에 대한 새로운 명령이 업데이트됨: VpnClient AAD 인증 옵션을 가상 네트워크 게이트웨이 리소스로 설정했습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2728">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span>
    - <span data-ttu-id="184db-2729">New-AzVirtualNetworkGateway가 업데이트됨: 게이트웨이에서 VpnClient AAD 인증 옵션을 설정할 수 있도록 선택적 매개 변수 AadTenantUri, AadAudienceId, AadIssuerUri가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2729">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="184db-2730">Set-AzVirtualNetworkGateway가 업데이트됨: 게이트웨이에서 VpnClient AAD 인증 옵션을 설정할 수 있도록 선택적 매개 변수 AadTenantUri, AadAudienceId, AadIssuerUri가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2730">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="184db-2731">Set-AzVirtualNetworkGateway가 업데이트됨: 게이트웨이에서 VpnClient AAD 인증 옵션을 제거할 수 있도록 선택적인 스위치 매개 변수 RemoveAadAuthentication이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2731">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="184db-2732">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="184db-2732">Az.OperationalInsights</span></span>
* <span data-ttu-id="184db-2733">'New-AzureRmOperationalInsightsWorkspace' 명령에서 **pergb2018** 가격 책정 계층 사용</span><span class="sxs-lookup"><span data-stu-id="184db-2733">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="184db-2734">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="184db-2734">Az.Resources</span></span>
* <span data-ttu-id="184db-2735">추가 템플릿 내보내기 옵션 지원</span><span class="sxs-lookup"><span data-stu-id="184db-2735">Support for additional Template Export options</span></span>
    - <span data-ttu-id="184db-2736">Export-AzResourceGroup에 '-SkipResourceNameParameterization' 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="184db-2736">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="184db-2737">Export-AzResourceGroup에 '-SkipAllParameterization' 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="184db-2737">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="184db-2738">내보낸 리소스 필터링을 위해 Export-AzResourceGroup에 '-Resource' 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="184db-2738">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="184db-2739">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="184db-2739">Az.ServiceFabric</span></span>
* <span data-ttu-id="184db-2740">일부 경우 잘못된 지문을 가져오는 추가 인증서 ByExistingKeyVault 수정</span><span class="sxs-lookup"><span data-stu-id="184db-2740">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="184db-2741">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="184db-2741">Az.Sql</span></span>
* <span data-ttu-id="184db-2742">Advanced Threat Protection 스토리지 엔드포인트 접미사 수정</span><span class="sxs-lookup"><span data-stu-id="184db-2742">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="184db-2743">Advanced Data Security가 Advanced Threat Protection 정책을 재정의하는 것을 수정</span><span class="sxs-lookup"><span data-stu-id="184db-2743">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="184db-2744">고객이 TDE 키를 추가하고 관리되는 인스턴스에 TDE 보호기를 설정할 수 있도록 Management.Sql용 새 Cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="184db-2744">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="184db-2745">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="184db-2745">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="184db-2746">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="184db-2746">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="184db-2747">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="184db-2747">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="184db-2748">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="184db-2748">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="184db-2749">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="184db-2749">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="184db-2750">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="184db-2750">Az.Storage</span></span>
* <span data-ttu-id="184db-2751">스토리지 계정 생성 시 종류 FileStorage 및 SkuName Premium_ZRS 지원</span><span class="sxs-lookup"><span data-stu-id="184db-2751">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="184db-2752">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="184db-2752">New-AzStorageAccount</span></span>
* <span data-ttu-id="184db-2753">BLOB immutability cmdlet의 설명 명확화</span><span class="sxs-lookup"><span data-stu-id="184db-2753">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="184db-2754">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="184db-2754">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="184db-2755">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="184db-2755">Az.Websites</span></span>
* <span data-ttu-id="184db-2756">Get-AzWebAppCertificate를 클라이언트 대신 서버의 리소스 그룹별로 필터링하도록 최적화</span><span class="sxs-lookup"><span data-stu-id="184db-2756">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="184db-2757">Get-AzWebAppSnapshot에 -UseDisasterRecovery 스위치 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="184db-2757">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="184db-2758">2.2.0 - 2019년 6월</span><span class="sxs-lookup"><span data-stu-id="184db-2758">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="184db-2759">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="184db-2759">Az.Cdn</span></span>
* <span data-ttu-id="184db-2760">cmdlet에서 2019-04-15 API 버전 기반의 rulesEngine 기능을 지원하도록 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2760">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="184db-2761">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="184db-2761">Az.Compute</span></span>
* <span data-ttu-id="184db-2762">작업을 시작하여 완료되기 전에 즉시 반환하는 `NoWait` 매개 변수가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2762">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="184db-2763">다음 Cmdlet이 업데이트 되었습니다.   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="184db-2763">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="184db-2764">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="184db-2764">Az.EventHub</span></span>
* <span data-ttu-id="184db-2765">#9231 수정 - Get-AzEventHubNamespace에서 태그를 반환하지 않음</span><span class="sxs-lookup"><span data-stu-id="184db-2765">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="184db-2766">#9230 수정 - Get-AzEventHubNamespace에서 ResourceGroupName 대신 ResourceGroup을 반환함</span><span class="sxs-lookup"><span data-stu-id="184db-2766">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="184db-2767">Az.Network</span><span class="sxs-lookup"><span data-stu-id="184db-2767">Az.Network</span></span>
* <span data-ttu-id="184db-2768">Nat Gateway에 대한 ResourceId 및 InputObject 업데이트</span><span class="sxs-lookup"><span data-stu-id="184db-2768">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="184db-2769">ResourceId 및 InputObject에 대한 별칭 추가</span><span class="sxs-lookup"><span data-stu-id="184db-2769">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="184db-2770">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="184db-2770">Az.PolicyInsights</span></span>
* <span data-ttu-id="184db-2771">Get-AzPolicyEvent에서 Null 참조 문제 해결</span><span class="sxs-lookup"><span data-stu-id="184db-2771">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="184db-2772">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="184db-2772">Az.RecoveryServices</span></span>
* <span data-ttu-id="184db-2773">IaaSVM 정책 최소 보존 기간(일)이 1에서 7로 변경됨</span><span class="sxs-lookup"><span data-stu-id="184db-2773">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="184db-2774">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="184db-2774">Az.ServiceBus</span></span>
* <span data-ttu-id="184db-2775">#9182 문제 해결 - Get-AzServiceBusNamespace에서 ResourceGroupName 대신 ResourceGroup을 반환</span><span class="sxs-lookup"><span data-stu-id="184db-2775">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="184db-2776">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="184db-2776">Az.ServiceFabric</span></span>
* <span data-ttu-id="184db-2777">'Update-AzServiceFabricReliability' 오류 메시지의 오타 수정</span><span class="sxs-lookup"><span data-stu-id="184db-2777">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="184db-2778">Service Fabric 명령줄에서 누락된 문자 수정</span><span class="sxs-lookup"><span data-stu-id="184db-2778">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="184db-2779">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="184db-2779">Az.Sql</span></span>
* <span data-ttu-id="184db-2780">Managed Instance에 대한 AutoDr을 지원하기 위해 New-AzureSqlInstance cmdlet에 대한 DnsZonePartner 매개 변수를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2780">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="184db-2781">Get-AzSqlDatabaseSecureConnectionPolicy cmdlet 사용 중단</span><span class="sxs-lookup"><span data-stu-id="184db-2781">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="184db-2782">Threat Detection(위협 탐지) cmdlet 이름을 Advanced Threat Protection으로 변경함</span><span class="sxs-lookup"><span data-stu-id="184db-2782">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="184db-2783">새 AzSqlInstance -StorageSizeInGB 및 -LicenseType 매개 변수는 이제 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2783">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="184db-2784">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="184db-2784">Az.Websites</span></span>
* <span data-ttu-id="184db-2785">-WebApp 속성에서 Set-AzWebApp 및 Set-AzWebAppSlot을 사용하면 태그가 제거되는 문제를 해결함</span><span class="sxs-lookup"><span data-stu-id="184db-2785">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="184db-2786">2.1.0 - 2019년 5월</span><span class="sxs-lookup"><span data-stu-id="184db-2786">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="184db-2787">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="184db-2787">Az.ApiManagement</span></span>
* <span data-ttu-id="184db-2788">글로벌 및 API 범위에서 진단을 관리하기 위한 새 cmdlet을 만들었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2788">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="184db-2789">**Get-AzApiManagementDiagnostic** - 글로벌 또는 API 범위가 구성된 진단 가져오기</span><span class="sxs-lookup"><span data-stu-id="184db-2789">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="184db-2790">**New-AzApiManagementDiagnostic** - 글로벌 범위 또는 API 범위에서 새 진단 만들기</span><span class="sxs-lookup"><span data-stu-id="184db-2790">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="184db-2791">**New-AzApiManagementHttpMessageDiagnostic** - 기록할 Headers(헤더) 및 Body Bytes(본문 바이트 수) 크기에 대한 진단 설정 만들기</span><span class="sxs-lookup"><span data-stu-id="184db-2791">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="184db-2792">**New-AzApiManagementPipelineDiagnosticSetting** - 게이트웨이로 들어오고 나가는 HTTP 메시지에 대한 진단 설정 만들기</span><span class="sxs-lookup"><span data-stu-id="184db-2792">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="184db-2793">**New-AzApiManagementSamplingSetting** - 진단 요청/응답에 대한 샘플링 설정 만들기</span><span class="sxs-lookup"><span data-stu-id="184db-2793">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="184db-2794">**Remove-AzApiManagementDiagnostic** - 글로벌 또는 API 범위에서 진단 엔터티 제거</span><span class="sxs-lookup"><span data-stu-id="184db-2794">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="184db-2795">**Set-AzApiManagementDiagnostic** - 글로벌 또는 API 범위에서 진단 엔터티 업데이트</span><span class="sxs-lookup"><span data-stu-id="184db-2795">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="184db-2796">ApiManagement 서비스에서 캐시를 관리하기 위한 새 cmdlet을 만들었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2796">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="184db-2797">**Get-AzApiManagementCache** - 식별자 또는 모든 캐시로 지정된 캐시의 세부 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="184db-2797">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="184db-2798">**New-AzApiManagementCache** - 특정 Azure 'region'(지역)에 새 'default'(기본) 캐시 만들기</span><span class="sxs-lookup"><span data-stu-id="184db-2798">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="184db-2799">**Remove-AzApiManagementCache** - 캐시 제거</span><span class="sxs-lookup"><span data-stu-id="184db-2799">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="184db-2800">**Update-AzApiManagementCache** - 캐시 업데이트</span><span class="sxs-lookup"><span data-stu-id="184db-2800">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="184db-2801">API 스키마 관리하기 위한 새 cmdlet을 만들었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2801">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="184db-2802">**New-AzApiManagementSchema** - API에 대한 새 스키마 만들기</span><span class="sxs-lookup"><span data-stu-id="184db-2802">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="184db-2803">**Get-AzApiManagementSchema** - API에 구성된 스키마 가져오기</span><span class="sxs-lookup"><span data-stu-id="184db-2803">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="184db-2804">**Remove-AzApiManagementSchema** - API에 구성된 스키마 제거</span><span class="sxs-lookup"><span data-stu-id="184db-2804">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="184db-2805">**Set-AzApiManagementSchema** - API에 구성된 스키마 업데이트</span><span class="sxs-lookup"><span data-stu-id="184db-2805">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="184db-2806">사용자 토큰을 생성하기 위한 새 cmdlet을 만들었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2806">Created new Cmdlet for generating a User Token.</span></span>
    - <span data-ttu-id="184db-2807">**New-AzApiManagementUserToken** - 기본적으로 8시간 동안 유효한 새 사용자 토큰을 생성합니다. 'GIT' 사용자에 대한 토큰은 이 cmdlet을 사용하여 생성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2807">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="184db-2808">네트워크 상태를 검색하기 위한 새 cmdlet을 만들었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2808">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="184db-2809">**Get-AzApiManagementNetworkStatus** - API Management 서비스에서 사용하는 리소스의 네트워크 상태 연결을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2809">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="184db-2810">ApiManagement 서비스를 가상 네트워크에 배포하고 종속성이 손상되었는지 여부를 확인할 때 유용합니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2810">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="184db-2811">**New-AzApiManagement** cmdlet에서 ApiManagement 서비스를 관리하도록 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2811">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span>
    - <span data-ttu-id="184db-2812">새 '소비' SKU 지원이 추가됨</span><span class="sxs-lookup"><span data-stu-id="184db-2812">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="184db-2813">'소비' SKU에 대해 'EnableClientCertificate' 플래그를 설정하기 위한 지원이 추가됨</span><span class="sxs-lookup"><span data-stu-id="184db-2813">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="184db-2814">새 **New-AzApiManagementSslSetting** cmdlet을 사용하면 'Backend(백 엔드)' 및 'Frontend'(프런트 엔드)에서 'TLS/SSL' 설정을 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2814">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="184db-2815">또한 ApiManagement 서비스의 'Frontend'에서 '3DES'와 같은 'Ciphers'와 'Http2'와 같은 'ServerProtocols'를 구성하는 데 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2815">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="184db-2816">ApiManagement 서비스에서 'DeveloperPortal' 호스트 이름을 구성하기 위한 지원이 추가됨</span><span class="sxs-lookup"><span data-stu-id="184db-2816">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="184db-2817">**Get-AzApiManagementSsoToken** cmdlet에서 'PsApiManagement' 개체를 입력으로 사용하도록 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2817">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="184db-2818">cmdlet에서 오류 메시지를 인라인으로 표시하도록 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2818">Updated the cmdlet to display Error Messages inline</span></span>
     > <span data-ttu-id="184db-2819">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : 오류 코드: ValidationError 오류 메시지: 하나 이상의 필드에 잘못된 값이 있습니다. 오류 세부 정보:    [Code=ValidationError, Message=줄 3, 열 10의 'log-to-eventhub' 요소에 오류가 있습니다.: 로거를 찾지 못함, Target=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="184db-2819">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="184db-2820">**Export-AzApiManagementApi** cmdlet에서 API를 'OpenApi 3.0' 형식으로 내보내도록 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2820">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="184db-2821">**Import-AzApiManagementApi** cmdlet을 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2821">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="184db-2822">'OpenApi 3.0' 문서 사양에서 API 가져오기</span><span class="sxs-lookup"><span data-stu-id="184db-2822">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="184db-2823">문서('Swagger', 'Wadl', 'Wsdl', 'OpenApi')에 지정된 'PsApiManagementSchema' 속성 재정의</span><span class="sxs-lookup"><span data-stu-id="184db-2823">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="184db-2824">문서에 지정된 'ServiceUrl' 속성 재정의</span><span class="sxs-lookup"><span data-stu-id="184db-2824">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="184db-2825">**Get-AzApiManagementPolicy** cmdlet에서 'rawxml'을 사용하여 이스케이프된 비 Xml 'format'(형식)의 정책을 반환하도록 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2825">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="184db-2826">**Set-AzApiManagementPolicy** cmdlet에서 'rawxml'을 사용하여 이스케이프된 비 Xml 'format'의 정책을 수락하고, 'xml'을 사용하여 이스케이프된 Xml 'format'의 정책을 수락하도록 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2826">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="184db-2827">**New-AzApiManagementApi** cmdlet을 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2827">Updated cmdlet **New-AzApiManagementApi**</span></span>
    - <span data-ttu-id="184db-2828">'OpenId' 권한 부여 서버를 사용하여 API 구성</span><span class="sxs-lookup"><span data-stu-id="184db-2828">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="184db-2829">'ApiVersionSet'에서 API 만들기</span><span class="sxs-lookup"><span data-stu-id="184db-2829">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="184db-2830">'SourceApiId' 및 'SourceApiRevision'을 사용하여 API 복제</span><span class="sxs-lookup"><span data-stu-id="184db-2830">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="184db-2831">API 범위에서 'SubscriptionRequired' 구성 가능</span><span class="sxs-lookup"><span data-stu-id="184db-2831">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="184db-2832">**Set-AzApiManagementApi** cmdlet을 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2832">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="184db-2833">'OpenId' 권한 부여 서버를 사용하여 API 구성</span><span class="sxs-lookup"><span data-stu-id="184db-2833">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="184db-2834">API를 'ApiVersionSet'으로 업데이트</span><span class="sxs-lookup"><span data-stu-id="184db-2834">To updated an API into an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="184db-2835">API 범위에서 'SubscriptionRequired' 구성 가능</span><span class="sxs-lookup"><span data-stu-id="184db-2835">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="184db-2836">**New-AzApiManagementRevision** cmdlet을 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2836">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="184db-2837">'SourceApiRevision'을 사용하여 기존 수정 버전 복제(태그, 제품, 작업 및 정책 복사).</span><span class="sxs-lookup"><span data-stu-id="184db-2837">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="184db-2838">새 수정 버전은 부모의 'ApiId'를 가정합니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2838">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="184db-2839">'ApiRevisionDescription' 제공</span><span class="sxs-lookup"><span data-stu-id="184db-2839">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="184db-2840">API 복제 시 'ServiceUrl' 재정의</span><span class="sxs-lookup"><span data-stu-id="184db-2840">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="184db-2841">**New-AzApiManagementIdentityProvider** cmdlet을 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2841">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="184db-2842">'Authority'를 사용하여 'AAD' 또는 'AADB2C' 구성</span><span class="sxs-lookup"><span data-stu-id="184db-2842">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="184db-2843">'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' 및 'PasswordResetPolicy' 설정</span><span class="sxs-lookup"><span data-stu-id="184db-2843">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="184db-2844">**New-AzApiManagementSubscription** cmdlet을 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2844">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="184db-2845">'Scope' 및 'UserId'를 사용하여 새 SubscriptonModel 설명</span><span class="sxs-lookup"><span data-stu-id="184db-2845">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="184db-2846">'ProductId' 및 'UserId'를 사용하여 이전 구독 모델 설명</span><span class="sxs-lookup"><span data-stu-id="184db-2846">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="184db-2847">구독 수준에서 'AllowTracing'을 사용하도록 설정하는 지원 추가</span><span class="sxs-lookup"><span data-stu-id="184db-2847">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="184db-2848">**Set-AzApiManagementSubscription** cmdlet을 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2848">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="184db-2849">'Scope' 및 'UserId'를 사용하여 새 SubscriptonModel 설명</span><span class="sxs-lookup"><span data-stu-id="184db-2849">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="184db-2850">'ProductId' 및 'UserId'를 사용하여 이전 구독 모델 설명</span><span class="sxs-lookup"><span data-stu-id="184db-2850">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="184db-2851">구독 수준에서 'AllowTracing'을 사용하도록 설정하는 지원 추가</span><span class="sxs-lookup"><span data-stu-id="184db-2851">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="184db-2852">다음 cmdlet에서 'ResourceId'를 입력으로 수락하도록 업데이트했습니다</span><span class="sxs-lookup"><span data-stu-id="184db-2852">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="184db-2853">'New-AzApiManagementContext'</span><span class="sxs-lookup"><span data-stu-id="184db-2853">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="184db-2854">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="184db-2854">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="184db-2855">'Get-AzApiManagementApiRelease'</span><span class="sxs-lookup"><span data-stu-id="184db-2855">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="184db-2856">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="184db-2856">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="184db-2857">'Get-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="184db-2857">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="184db-2858">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="184db-2858">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="184db-2859">'Get-AzApiManagementAuthorizationServer'</span><span class="sxs-lookup"><span data-stu-id="184db-2859">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="184db-2860">'Get-AzApiManagementBackend'</span><span class="sxs-lookup"><span data-stu-id="184db-2860">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="184db-2861">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="184db-2861">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="184db-2862">'Get-AzApiManagementCertificate'</span><span class="sxs-lookup"><span data-stu-id="184db-2862">'Get-AzApiManagementCertificate'</span></span>
    - <span data-ttu-id="184db-2863">'Remove-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="184db-2863">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="184db-2864">'Remove-AzApiManagementSubscription'</span><span class="sxs-lookup"><span data-stu-id="184db-2864">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="184db-2865">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="184db-2865">Az.Automation</span></span>
* <span data-ttu-id="184db-2866">Get-AzAutomationJobOutputRecord에서 JSON 및 Text 레코드 값을 처리하도록 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2866">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="184db-2867">문제 https://github.com/Azure/azure-powershell/issues/7977 수정</span><span class="sxs-lookup"><span data-stu-id="184db-2867">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="184db-2868">문제 https://github.com/Azure/azure-powershell/issues/8600 수정</span><span class="sxs-lookup"><span data-stu-id="184db-2868">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="184db-2869">Start-AzAutomationDscCompilationJob에서 완료될 때까지 기다리지 않고 작업을 바로 시작하도록 변경했습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2869">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="184db-2870">문제 https://github.com/Azure/azure-powershell/issues/8347 수정</span><span class="sxs-lookup"><span data-stu-id="184db-2870">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="184db-2871">-Name을 사용하면 모든 노드를 반환하는 Get-AzAutomationDscNode 수정.</span><span class="sxs-lookup"><span data-stu-id="184db-2871">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="184db-2872">이제 일치하는 노드만 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2872">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="184db-2873">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="184db-2873">Az.Compute</span></span>
* <span data-ttu-id="184db-2874">ProtectFromScaleIn 및 ProtectFromScaleSetAction 매개 변수를 Update-AzVmssVM cmdlet에 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2874">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="184db-2875">'East US'(미국 동부)가 지원되지 않는 경우 이제 New-AzVM wimple 매개 변수 집합에서 기본적으로 사용 가능한 위치를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2875">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="184db-2876">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="184db-2876">Az.DataLakeStore</span></span>
* <span data-ttu-id="184db-2877">ADLS SDK에서 httpclient를 사용하도록 업데이트하고, 데이터 평면 테스트를 Azure 프레임워크와 통합합니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2877">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="184db-2878">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="184db-2878">Az.Monitor</span></span>
* <span data-ttu-id="184db-2879">도움말 예제에서 잘못된 매개 변수 이름을 수정했습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2879">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="184db-2880">Az.Network</span><span class="sxs-lookup"><span data-stu-id="184db-2880">Az.Network</span></span>
* <span data-ttu-id="184db-2881">DisableBgpRoutePropagation 플래그를 유효 경로 테이블 출력에 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2881">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="184db-2882">업데이트된 cmdlet:</span><span class="sxs-lookup"><span data-stu-id="184db-2882">Updated cmdlet:</span></span>
        - <span data-ttu-id="184db-2883">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="184db-2883">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="184db-2884">New-AzApplicationGatewayTrustedRootCertificate 설명서에서 이중 파선을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2884">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="184db-2885">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="184db-2885">Az.Resources</span></span>
* <span data-ttu-id="184db-2886">할당 거부를 검색하기 위한 새 Get-AzureRmDenyAssignment cmdlet을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2886">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="184db-2887">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="184db-2887">Az.Sql</span></span>
* <span data-ttu-id="184db-2888">Advanced Threat Protection cmdlet의 이름을 Advanced Data Security로 변경하고, 취약성 평가를 기본적으로 사용하도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2888">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="184db-2889">2.0.0 - 2019년 5월</span><span class="sxs-lookup"><span data-stu-id="184db-2889">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="184db-2890">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="184db-2890">Az.Accounts</span></span>
* <span data-ttu-id="184db-2891">사용자 이름/비밀번호 인증을 사용하여 ADFS 문제를 해결하도록 인증 라이브러리 업데이트</span><span class="sxs-lookup"><span data-stu-id="184db-2891">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="184db-2892">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="184db-2892">Az.CognitiveServices</span></span>
* <span data-ttu-id="184db-2893">Bing Search 서비스에 대해서만 Bing 면책 조항을 표시하세요.</span><span class="sxs-lookup"><span data-stu-id="184db-2893">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="184db-2894">계정 생성 실패 시 오류 개선.</span><span class="sxs-lookup"><span data-stu-id="184db-2894">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="184db-2895">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="184db-2895">Az.Compute</span></span>
* <span data-ttu-id="184db-2896">근접 배치 그룹 기능</span><span class="sxs-lookup"><span data-stu-id="184db-2896">Proximity placement group feature.</span></span>
    - <span data-ttu-id="184db-2897">다음과 같은 새 cmdlet을 추가했습니다.   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="184db-2897">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="184db-2898">새 매개 변수 ProximityPlacementGroupId가 다음 cmdlet에 추가됩니다.   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="184db-2898">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="184db-2899">New-AzGalleryImageVersion에 StorageAccountType 매개 변수가 추가됩니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2899">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="184db-2900">New-AzGalleryImageVersion의 TargetRegion이 StorageAccountType를 포함할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2900">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="184db-2901">SkipShutdown 스위치 매개 변수가 Stop-AzVM 및 Stop-AzVmss에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2901">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>
* <span data-ttu-id="184db-2902">주요 변경 내용</span><span class="sxs-lookup"><span data-stu-id="184db-2902">Breaking changes</span></span>
    - <span data-ttu-id="184db-2903">Set-AzVMBootDiagnostics이 Set-AzVMBootDiagnostic으로 변경됩니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2903">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="184db-2904">Export-AzLogAnalyticThrottledRequests이 Export-AzLogAnalyticThrottledRequests로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2904">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="184db-2905">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="184db-2905">Az.DeploymentManager</span></span>
* <span data-ttu-id="184db-2906">Azure 배포 관리자 cmdlet의 일반적으로 사용 가능한 첫 번째 릴리스</span><span class="sxs-lookup"><span data-stu-id="184db-2906">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="184db-2907">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="184db-2907">Az.Dns</span></span>
* <span data-ttu-id="184db-2908">자동 DNS 이름 서버 위임</span><span class="sxs-lookup"><span data-stu-id="184db-2908">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="184db-2909">DNS 영역 만들기 cmdlet은 추가 선택적 매개 변수로 부모 영역 이름을 허용합니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2909">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="184db-2910">새로 생성 된 자식 영역의 부모 영역에 NS 레코드를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2910">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="184db-2911">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="184db-2911">Az.FrontDoor</span></span>
* <span data-ttu-id="184db-2912">Azure FrontDoor cmdlet의 일반적으로 사용 가능한 첫 번째 릴리스</span><span class="sxs-lookup"><span data-stu-id="184db-2912">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="184db-2913">'Waf'를 포함하도록 WAF cmdlet의 이름 바꾸기</span><span class="sxs-lookup"><span data-stu-id="184db-2913">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="184db-2914">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="184db-2914">Az.HDInsight</span></span>
* <span data-ttu-id="184db-2915">두 개의 cmdlet을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2915">Removed two cmdlets:</span></span>
    - <span data-ttu-id="184db-2916">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="184db-2916">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="184db-2917">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="184db-2917">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="184db-2918">Grant-AzHDInsightHttpServicesAccess를 대체할 새 cmdlet Set-AzHDInsightGatewayCredential을 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2918">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="184db-2919">reader 역할과 HDInsight 운영자 역할을 구분하도록 cmdlet Get-AzHDInsightJobOutput 업데이트:</span><span class="sxs-lookup"><span data-stu-id="184db-2919">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="184db-2920">reader 역할을 가진 사용자는 'DefaultStorageAccountKey'매개 변수를 명시적으로 지정해야 합니다. 그렇지 않으면 오류가 발생합니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2920">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="184db-2921">Hdinsight 운영자 역할을 가진 사용자를 영향을 받지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2921">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="184db-2922">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="184db-2922">Az.Monitor</span></span>
* <span data-ttu-id="184db-2923">SQR API(예약 쿼리 규칙)용 새 cmdlet</span><span class="sxs-lookup"><span data-stu-id="184db-2923">New cmdlets for SQR API (Scheduled Query Rule)</span></span>
    - <span data-ttu-id="184db-2924">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="184db-2924">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="184db-2925">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="184db-2925">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="184db-2926">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="184db-2926">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="184db-2927">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="184db-2927">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="184db-2928">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="184db-2928">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="184db-2929">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="184db-2929">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="184db-2930">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="184db-2930">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="184db-2931">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="184db-2931">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="184db-2932">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="184db-2932">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="184db-2933">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="184db-2933">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="184db-2934">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="184db-2934">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="184db-2935">SQR API에 대한 [자세한 내용](/rest/api/monitor/scheduledqueryrules)</span><span class="sxs-lookup"><span data-stu-id="184db-2935">[More](/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="184db-2936">GenV2(비 클래식) 메트릭 기반 경고 규칙에 대한 cmdlet을 포함하도록 Az.Monitor.md가 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="184db-2936">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="184db-2937">Az.Network</span><span class="sxs-lookup"><span data-stu-id="184db-2937">Az.Network</span></span>
* <span data-ttu-id="184db-2938">Nat 게이트웨이 리소스에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="184db-2938">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="184db-2939">새로운 cmdlet</span><span class="sxs-lookup"><span data-stu-id="184db-2939">New cmdlets</span></span>
        - <span data-ttu-id="184db-2940">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="184db-2940">New-AzNatGateway</span></span>
        - <span data-ttu-id="184db-2941">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="184db-2941">Get-AzNatGateway</span></span>
        - <span data-ttu-id="184db-2942">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="184db-2942">Set-AzNatGateway</span></span>
        - <span data-ttu-id="184db-2943">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="184db-2943">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="184db-2944">다음 Cmdlet이 업데이트 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2944">Updated cmdlets</span></span>
        - <span data-ttu-id="184db-2945">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="184db-2945">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="184db-2946">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="184db-2946">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="184db-2947">기능에 대한 새로운 명령이 업데이트됨: Brooklyn Gateway에서 사용자 지정 경로 설정/제거.</span><span class="sxs-lookup"><span data-stu-id="184db-2947">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="184db-2948">New-AzVirtualNetworkGateway가 업데이트됨: 선택적 매개 변수 -CustomRoute를 추가하여 게이트웨이에서 설정할 사용자 지정 경로로 주소 접두사를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2948">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="184db-2949">Set-AzVirtualNetworkGateway가 업데이트됨: 선택적 매개 변수 -CustomRoute를 추가하여 게이트웨이에서 설정할 사용자 지정 경로로 주소 접두사를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2949">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="184db-2950">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="184db-2950">Az.PolicyInsights</span></span>
* <span data-ttu-id="184db-2951">정책 평가 세부 정보 쿼리 지원</span><span class="sxs-lookup"><span data-stu-id="184db-2951">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="184db-2952">Get-AzPolicyState에 '-Expand'매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="184db-2952">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="184db-2953">'-Expand PolicyEvaluationDetails' 지원</span><span class="sxs-lookup"><span data-stu-id="184db-2953">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="184db-2954">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="184db-2954">Az.RecoveryServices</span></span>
* <span data-ttu-id="184db-2955">크로스 구독 Azure에서 Azure 사이트 복구 지원</span><span class="sxs-lookup"><span data-stu-id="184db-2955">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="184db-2956">Azure Site Recovery에 대한 호환성이 손상되는 변경 표시</span><span class="sxs-lookup"><span data-stu-id="184db-2956">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="184db-2957">Azure Site Recovery 복구 계획 최종 실행 계획에 대한 수정</span><span class="sxs-lookup"><span data-stu-id="184db-2957">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="184db-2958">Azure에서 Azure에 대한 Azure Site Recovery 업데이트 네트워크 매핑 수정</span><span class="sxs-lookup"><span data-stu-id="184db-2958">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="184db-2959">관리 디스크에 대한 Azure에서 Azure에 대한 Azure Site Recovery 업데이트 보호 방향 수정</span><span class="sxs-lookup"><span data-stu-id="184db-2959">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="184db-2960">기타 사소한 수정.</span><span class="sxs-lookup"><span data-stu-id="184db-2960">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="184db-2961">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="184db-2961">Az.Relay</span></span>
* <span data-ttu-id="184db-2962">고객 관련 메시지의 철자 오류 수정</span><span class="sxs-lookup"><span data-stu-id="184db-2962">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="184db-2963">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="184db-2963">Az.ServiceBus</span></span>
* <span data-ttu-id="184db-2964">네임스페이스의 NetworkRuleSet에 대한 새 cmdlet가 추가되었습니다</span><span class="sxs-lookup"><span data-stu-id="184db-2964">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="184db-2965">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="184db-2965">Az.Storage</span></span>
* <span data-ttu-id="184db-2966">저장소 클라이언트 라이브러리 10.0.1로 업그레이드(이 SDK의 모든 개체의 네임스페이스가 'Microsoft.WindowsAzure.Storage. *'에서 'Microsoft.Azure.Storage.* '로 변경됨)</span><span class="sxs-lookup"><span data-stu-id="184db-2966">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="184db-2967">새로운 API 버전 2019-04-01을 지원하기 위해 Microsoft.Azure.Management.Storage 11.0.0으로 업그레이드합니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2967">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="184db-2968">스토리지 생성 계정의 기본 스토리지 계정 종류가 'Storage'에서 'StorageV2'로 변경됩니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2968">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="184db-2969">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="184db-2969">New-AzStorageAccount</span></span>
* <span data-ttu-id="184db-2970">'StandardLRS'가 'Standard_LRS'로 변경되는 것과 같이 '-'을 추가하여 입력 SkuName과 정렬되도록 스토리지 계정 cmdlet 출력 Sku.Name을 변경합니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2970">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="184db-2971">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="184db-2971">New-AzStorageAccount</span></span>
    - <span data-ttu-id="184db-2972">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="184db-2972">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="184db-2973">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="184db-2973">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="184db-2974">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="184db-2974">Az.Websites</span></span>
* <span data-ttu-id="184db-2975">Get-AzWebApp에서 반환한 PSSite 개체에 대해 'Kind'속성이 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2975">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="184db-2976">Get-AzWebApp\* 메트릭 및 Get-AzAppServicePlanMetrics가 사용되지 않음으로 표시되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2976">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="184db-2977">1.8.0 - 2019년 4월</span><span class="sxs-lookup"><span data-stu-id="184db-2977">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="184db-2978">마지막 주 릴리스 이후의 주요 사항</span><span class="sxs-lookup"><span data-stu-id="184db-2978">Highlights since the last major release</span></span>
* <span data-ttu-id="184db-2979">`Az` 모듈 일반 공급</span><span class="sxs-lookup"><span data-stu-id="184db-2979">General availability of `Az` module</span></span>
* <span data-ttu-id="184db-2980">`Az` 모듈에 대한 자세한 내용은 https://aka.ms/azps-announce 를 방문하세요.</span><span class="sxs-lookup"><span data-stu-id="184db-2980">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="184db-2981">Location, ResourceGroup 및 ResourceName 완성자가 추가되었습니다(https://azure.microsoft.com/blog/completers-in-azure-powershell/ ).</span><span class="sxs-lookup"><span data-stu-id="184db-2981">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="184db-2982">와일드카드 지원이 Az.Compute 및 Az.Network에 대한 Get cmdlet에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2982">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="184db-2983">Windows PowerShell 5.1 전용 대화형 사용자 이름/암호 인증이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2983">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="184db-2984">Python 2 Runbook 지원이 Az.Automation에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2984">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="184db-2985">Az.LogicApp: 통합 계정 어셈블리 및 일괄 처리 구성을 위한 새로운 cmdlet입니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2985">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="184db-2986">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="184db-2986">Az.Accounts</span></span>
* <span data-ttu-id="184db-2987">Mac에서 모듈을 올바르게 삭제하기 위해 Uninstall-AzureRm을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2987">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="184db-2988">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="184db-2988">Az.Batch</span></span>
* <span data-ttu-id="184db-2989">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2989">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="184db-2990">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="184db-2990">Az.Cdn</span></span>
* <span data-ttu-id="184db-2991">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2991">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="184db-2992">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="184db-2992">Az.CognitiveServices</span></span>
* <span data-ttu-id="184db-2993">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2993">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="184db-2994">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="184db-2994">Az.Compute</span></span>
* <span data-ttu-id="184db-2995">디스크의 리소스 ID에 리소스 ID의 소문자 resourcegroups가 있는 경우 AEM 설치 문제 수정</span><span class="sxs-lookup"><span data-stu-id="184db-2995">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="184db-2996">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2996">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="184db-2997">와일드 카드에 대한 설명서 수정</span><span class="sxs-lookup"><span data-stu-id="184db-2997">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="184db-2998">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="184db-2998">Az.DataFactory</span></span>
* <span data-ttu-id="184db-2999">NodeCount가 관리형 통합 런타임에 대해 Null이 아닌 경우 SsisProperties를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="184db-2999">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="184db-3000">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="184db-3000">Az.DataLakeStore</span></span>
* <span data-ttu-id="184db-3001">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-3001">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="184db-3002">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="184db-3002">Az.EventGrid</span></span>
* <span data-ttu-id="184db-3003">이벤트 구독 cmdlet 만들기/업데이트를 사용하기 전에 리소스를 만들어야 함을 나타내기 위해 엔드포인트의 도움말 텍스트가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-3003">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="184db-3004">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="184db-3004">Az.EventHub</span></span>
* <span data-ttu-id="184db-3005">네임스페이스의 NetworkRuleSet에 대한 새 cmdlet가 추가되었습니다</span><span class="sxs-lookup"><span data-stu-id="184db-3005">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="184db-3006">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="184db-3006">Az.HDInsight</span></span>
* <span data-ttu-id="184db-3007">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-3007">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="184db-3008">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="184db-3008">Az.IotHub</span></span>
* <span data-ttu-id="184db-3009">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-3009">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="184db-3010">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="184db-3010">Az.KeyVault</span></span>
* <span data-ttu-id="184db-3011">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-3011">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="184db-3012">와일드 카드에 대한 설명서 수정</span><span class="sxs-lookup"><span data-stu-id="184db-3012">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="184db-3013">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="184db-3013">Az.MachineLearning</span></span>
* <span data-ttu-id="184db-3014">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-3014">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="184db-3015">Az.Media</span><span class="sxs-lookup"><span data-stu-id="184db-3015">Az.Media</span></span>
* <span data-ttu-id="184db-3016">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-3016">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="184db-3017">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="184db-3017">Az.Monitor</span></span>
  * <span data-ttu-id="184db-3018">GenV2(비 클래식) 메트릭 기반 경고 규칙에 대한 새 cmdlet</span><span class="sxs-lookup"><span data-stu-id="184db-3018">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="184db-3019">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="184db-3019">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="184db-3020">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="184db-3020">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="184db-3021">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="184db-3021">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="184db-3022">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="184db-3022">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="184db-3023">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="184db-3023">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="184db-3024">모니터 SDK가 버전 0.22.0-preview로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-3024">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="184db-3025">Az.Network</span><span class="sxs-lookup"><span data-stu-id="184db-3025">Az.Network</span></span>
* <span data-ttu-id="184db-3026">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-3026">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="184db-3027">와일드 카드에 대한 설명서 수정</span><span class="sxs-lookup"><span data-stu-id="184db-3027">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="184db-3028">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="184db-3028">Az.NotificationHubs</span></span>
* <span data-ttu-id="184db-3029">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-3029">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="184db-3030">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="184db-3030">Az.OperationalInsights</span></span>
* <span data-ttu-id="184db-3031">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-3031">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="184db-3032">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="184db-3032">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="184db-3033">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-3033">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="184db-3034">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="184db-3034">Az.RecoveryServices</span></span>
* <span data-ttu-id="184db-3035">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-3035">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="184db-3036">Azure VM의 SQL용 테이블 형식이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-3036">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="184db-3037">AzureFileShare에서 위치를 가져오는 대체 메서드가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-3037">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="184db-3038">시간대에 따라 SchedulePolicy 개체의 ScheduleRunDays가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-3038">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="184db-3039">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="184db-3039">Az.RedisCache</span></span>
* <span data-ttu-id="184db-3040">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-3040">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="184db-3041">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="184db-3041">Az.Resources</span></span>
* <span data-ttu-id="184db-3042">와일드 카드에 대한 설명서 수정</span><span class="sxs-lookup"><span data-stu-id="184db-3042">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="184db-3043">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="184db-3043">Az.Sql</span></span>
* <span data-ttu-id="184db-3044">Monitor SDK의 종속성을 공용 코드로 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="184db-3044">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="184db-3045">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-3045">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="184db-3046">다중 열 분류 프로세스가 향상되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-3046">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="184db-3047">기본적으로 Get-AzSqlServerServiceObjective의 응답으로 SKU 속성(SKU 이름, 제품군, 용량)과 테이블 형식을 포함합니다.</span><span class="sxs-lookup"><span data-stu-id="184db-3047">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="184db-3048">해당 지역에 기존 서버 없이 위치별로 Get-AzSqlServerServiceObjective를 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-3048">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="184db-3049">관리형 인스턴스 생성 시 표준 시간대 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="184db-3049">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="184db-3050">와일드 카드에 대한 설명서 수정</span><span class="sxs-lookup"><span data-stu-id="184db-3050">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="184db-3051">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="184db-3051">Az.Websites</span></span>
* <span data-ttu-id="184db-3052">실행 시 태그를 제거하지 않도록 Set-AzWebApp 및 Set-AzWebAppSlot를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="184db-3052">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="184db-3053">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-3053">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="184db-3054">WebSites SDK가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-3054">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="184db-3055">PSAppServicePlan에서 AdminSiteName 속성을 제거했습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-3055">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="184db-3056">1.7.0 - 2019년 4월</span><span class="sxs-lookup"><span data-stu-id="184db-3056">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="184db-3057">마지막 주 릴리스 이후의 주요 사항</span><span class="sxs-lookup"><span data-stu-id="184db-3057">Highlights since the last major release</span></span>
* <span data-ttu-id="184db-3058">`Az` 모듈 일반 공급</span><span class="sxs-lookup"><span data-stu-id="184db-3058">General availability of `Az` module</span></span>
* <span data-ttu-id="184db-3059">`Az` 모듈에 대한 자세한 내용은 https://aka.ms/azps-announce 를 방문하세요.</span><span class="sxs-lookup"><span data-stu-id="184db-3059">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="184db-3060">Location, ResourceGroup 및 ResourceName 완성자가 추가되었습니다(https://azure.microsoft.com/blog/completers-in-azure-powershell/ ).</span><span class="sxs-lookup"><span data-stu-id="184db-3060">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="184db-3061">와일드카드 지원이 Az.Compute 및 Az.Network에 대한 Get cmdlet에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-3061">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="184db-3062">Windows PowerShell 5.1 전용 대화형 사용자 이름/암호 인증이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-3062">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="184db-3063">Python 2 Runbook 지원이 Az.Automation에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-3063">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="184db-3064">Az.LogicApp: 통합 계정 어셈블리 및 일괄 처리 구성을 위한 새로운 cmdlet입니다.</span><span class="sxs-lookup"><span data-stu-id="184db-3064">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="184db-3065">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="184db-3065">Az.Accounts</span></span>
* <span data-ttu-id="184db-3066">매개 변수 AzureAnalysisServicesEndpointResourceId를 허용하도록 Add-AzEnvironment 및 Set-AzEnvironment 업데이트</span><span class="sxs-lookup"><span data-stu-id="184db-3066">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="184db-3067">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="184db-3067">Az.AnalysisServices</span></span>
* <span data-ttu-id="184db-3068">데이터 평면 cmdlet에서 ServiceClient 사용 및 원본 인증 논리 제거</span><span class="sxs-lookup"><span data-stu-id="184db-3068">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="184db-3069">호환성이 손상되는 변경을 방지하기 위해 Add-AzureASAccount를 Connect-AzAccount의 래퍼로 만듦</span><span class="sxs-lookup"><span data-stu-id="184db-3069">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="184db-3070">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="184db-3070">Az.Automation</span></span>
* <span data-ttu-id="184db-3071">포함에 대한 New-AzAutomationSoftwareUpdateConfiguration cmdlet 버그 수정</span><span class="sxs-lookup"><span data-stu-id="184db-3071">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="184db-3072">이제 매개 변수 IncludedKbNumber 및 IncludedPackageNameMask가 작동함</span><span class="sxs-lookup"><span data-stu-id="184db-3072">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="184db-3073">Azure 자동화 업데이트 관리 동적 그룹에 대한 버그 수정</span><span class="sxs-lookup"><span data-stu-id="184db-3073">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="184db-3074">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="184db-3074">Az.Compute</span></span>
* <span data-ttu-id="184db-3075">New-AzDiskConfig 및 New-AzSnapshotConfig에 HyperVGeneration 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="184db-3075">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="184db-3076">다른 테넌트의 갤러리 이미지를 사용하여 VM을 만들 수 있음</span><span class="sxs-lookup"><span data-stu-id="184db-3076">Allow VM creation with galley image from other tenants.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="184db-3077">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="184db-3077">Az.ContainerInstance</span></span>
* <span data-ttu-id="184db-3078">후행 빈 인수를 추가한 New-AzContainerGroup의 -Command 매개 변수의 문제 수정</span><span class="sxs-lookup"><span data-stu-id="184db-3078">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="184db-3079">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="184db-3079">Az.DataFactory</span></span>
* <span data-ttu-id="184db-3080">ADF .Net SDK 버전을 3.0.2로 업데이트</span><span class="sxs-lookup"><span data-stu-id="184db-3080">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="184db-3081">RepoConfiguration 관련 설정에 대한 추가 매개 변수로 Set-AzDataFactoryV2 cmdlet을 업데이트</span><span class="sxs-lookup"><span data-stu-id="184db-3081">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="184db-3082">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="184db-3082">Az.Resources</span></span>
* <span data-ttu-id="184db-3083">'-ResourceId' 또는 '-ResourceGroupName', '-Name' 및 '-ResourceType' 매개 변수를 제공할 때 'Get-AzResource'에 대한 공급자 처리 개선</span><span class="sxs-lookup"><span data-stu-id="184db-3083">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="184db-3084">'Test-AzDeployment' 및 'Test-AzResourceGroupDeployment'에 대한 오류 처리 개선</span><span class="sxs-lookup"><span data-stu-id="184db-3084">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="184db-3085">배포 유효성 검사 외부에서 발생한 오류를 처리하고 그 대신 명령의 출력에 포함</span><span class="sxs-lookup"><span data-stu-id="184db-3085">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="184db-3086">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/6856 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="184db-3086">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="184db-3087">배포 cmdlet 세트에 스크립트 및 작업 시나리오에서 프롬프트를 건너뛰는 '-IgnoreDynamicParameters' 스위치 추가</span><span class="sxs-lookup"><span data-stu-id="184db-3087">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="184db-3088">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/6856 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="184db-3088">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="184db-3089">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="184db-3089">Az.Sql</span></span>
* <span data-ttu-id="184db-3090">데이터베이스 데이터 분류 지원</span><span class="sxs-lookup"><span data-stu-id="184db-3090">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="184db-3091">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="184db-3091">Az.Storage</span></span>
* <span data-ttu-id="184db-3092">매개 변수 -UseConnectedAccount를 사용하여 스토리지 컨텍스트를 만들 때 자세한 오류 보고(단, 로그인 Azure 계정 없이)</span><span class="sxs-lookup"><span data-stu-id="184db-3092">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="184db-3093">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="184db-3093">New-AzStorageContext</span></span>
* <span data-ttu-id="184db-3094">관리 평면 API를 사용하여 지정한 스토리지 계정의 BLOB 서비스 속성 관리 지원</span><span class="sxs-lookup"><span data-stu-id="184db-3094">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="184db-3095">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="184db-3095">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="184db-3096">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="184db-3096">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="184db-3097">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="184db-3097">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="184db-3098">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="184db-3098">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="184db-3099">BLOB 및 파일 업로드/다운로드 cmdlet에 대한 -AsJob 지원</span><span class="sxs-lookup"><span data-stu-id="184db-3099">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="184db-3100">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="184db-3100">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="184db-3101">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="184db-3101">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="184db-3102">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="184db-3102">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="184db-3103">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="184db-3103">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="184db-3104">1.6.0 - 2019년 3월</span><span class="sxs-lookup"><span data-stu-id="184db-3104">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="184db-3105">마지막 주 릴리스 이후의 주요 사항</span><span class="sxs-lookup"><span data-stu-id="184db-3105">Highlights since the last major release</span></span>
* <span data-ttu-id="184db-3106">`Az` 모듈 일반 공급</span><span class="sxs-lookup"><span data-stu-id="184db-3106">General availability of `Az` module</span></span>
* <span data-ttu-id="184db-3107">`Az` 모듈에 대한 자세한 내용은 https://aka.ms/azps-announce 를 방문하세요.</span><span class="sxs-lookup"><span data-stu-id="184db-3107">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="184db-3108">Location, ResourceGroup 및 ResourceName 완성자가 추가되었습니다(https://azure.microsoft.com/blog/completers-in-azure-powershell/ ).</span><span class="sxs-lookup"><span data-stu-id="184db-3108">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="184db-3109">와일드카드 지원이 Az.Compute 및 Az.Network에 대한 Get cmdlet에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-3109">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="184db-3110">Windows PowerShell 5.1 전용 대화형 사용자 이름/암호 인증이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-3110">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="184db-3111">Python 2 Runbook 지원이 Az.Automation에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-3111">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="184db-3112">Az.LogicApp: 통합 계정 어셈블리 및 일괄 처리 구성을 위한 새로운 cmdlet입니다.</span><span class="sxs-lookup"><span data-stu-id="184db-3112">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="184db-3113">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="184db-3113">Az.Automation</span></span>
* <span data-ttu-id="184db-3114">Azure 자동화 업데이트 관리에서 변경된 지원 기능은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-3114">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="184db-3115">동적 그룹화</span><span class="sxs-lookup"><span data-stu-id="184db-3115">Dynamic grouping</span></span>
    * <span data-ttu-id="184db-3116">사전 스크립트</span><span class="sxs-lookup"><span data-stu-id="184db-3116">Pre-Post script</span></span>
    * <span data-ttu-id="184db-3117">다시 부팅 설정</span><span class="sxs-lookup"><span data-stu-id="184db-3117">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="184db-3118">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="184db-3118">Az.Compute</span></span>
* <span data-ttu-id="184db-3119">Get-AzVmBootDiagnosticsData의 경로 확인 문제가 해결되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-3119">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="184db-3120">Compute 클라이언트 라이브러리가 25.0.0으로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-3120">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="184db-3121">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="184db-3121">Az.KeyVault</span></span>
* <span data-ttu-id="184db-3122">와일드카드 지원이 KeyVault cmdlet에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-3122">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="184db-3123">Az.Network</span><span class="sxs-lookup"><span data-stu-id="184db-3123">Az.Network</span></span>
* <span data-ttu-id="184db-3124">Azure Firewall에 대한 위협 인텔리전스 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-3124">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="184db-3125">Application Gateway 방화벽 정책의 최상위 수준 리소스 및 사용자 지정 규칙이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-3125">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="184db-3126">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="184db-3126">Az.RecoveryServices</span></span>
* <span data-ttu-id="184db-3127">인스턴트 RP를 지원하기 위해 SnapshotRetentionInDays가 Azure VM 정책에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-3127">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="184db-3128">컨테이너 등록을 취소하는 파이프 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-3128">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="184db-3129">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="184db-3129">Az.Resources</span></span>
* <span data-ttu-id="184db-3130">Get-AzResource 및 Get-AzResourceGroup에 대한 와일드카드 지원을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="184db-3130">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="184db-3131">ARM에 대한 일반 호출을 수행할 때 사용되는 자격 증명을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="184db-3131">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="184db-3132">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="184db-3132">Az.Sql</span></span>
* <span data-ttu-id="184db-3133">위협 탐지의 cmdlet 매개 변수(ExcludeDetectionType)가 DetectionType에서 string[]으로 변경되어 새 DetectionType이 추가되면 이후의 증명이 되고 자동 완성도 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="184db-3133">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="184db-3134">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="184db-3134">Az.Storage</span></span>
* <span data-ttu-id="184db-3135">스토리지 계정에 대한 관리 정책 가져오기/설정/제거를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="184db-3135">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="184db-3136">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="184db-3136">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="184db-3137">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="184db-3137">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="184db-3138">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="184db-3138">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="184db-3139">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="184db-3139">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="184db-3140">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="184db-3140">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="184db-3141">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="184db-3141">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="184db-3142">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="184db-3142">Az.Websites</span></span>
* <span data-ttu-id="184db-3143">'New-AzWebApp -IncludeSourceWebAppSlots'를 사용하여 모든 슬롯의 복제를 중단하는 ARM 템플릿 버그가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-3143">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span>

## <a name="150---march-2019"></a><span data-ttu-id="184db-3144">1.5.0 - 2019년 3월</span><span class="sxs-lookup"><span data-stu-id="184db-3144">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="184db-3145">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="184db-3145">Az.Accounts</span></span>
* <span data-ttu-id="184db-3146">'Register-AzModule' 명령을 추가하여 AutoRest 생성 cmdlet을 지원</span><span class="sxs-lookup"><span data-stu-id="184db-3146">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="184db-3147">Connect-AzAccount 예제 업데이트</span><span class="sxs-lookup"><span data-stu-id="184db-3147">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="184db-3148">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="184db-3148">Az.Automation</span></span>
* <span data-ttu-id="184db-3149">몇몇 Azure Automation cmdlet에서 특정 월별 일정을 검색할 때 발생하는 문제 수정</span><span class="sxs-lookup"><span data-stu-id="184db-3149">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="184db-3150">상위 20개 노드를 반환하도록 Get-AzAutomationDscNode를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="184db-3150">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="184db-3151">이제 모든 노드 반환</span><span class="sxs-lookup"><span data-stu-id="184db-3151">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="184db-3152">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="184db-3152">Az.Cdn</span></span>
* <span data-ttu-id="184db-3153">사용자 지정 도메인 Https 사용/사용 안 함에 대한 새 Powershell cmdlet이 추가되었으며 기존의 것은 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-3153">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="184db-3154">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="184db-3154">Az.Compute</span></span>
* <span data-ttu-id="184db-3155">Get cmdlet에 와일드 카드 지원 추가</span><span class="sxs-lookup"><span data-stu-id="184db-3155">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="184db-3156">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="184db-3156">Az.DataFactory</span></span>
* <span data-ttu-id="184db-3157">ADF.Net SDK 버전이 3.0.1로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-3157">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="184db-3158">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="184db-3158">Az.LogicApp</span></span>
* <span data-ttu-id="184db-3159">첫 결과 페이지 검색 시에만 ListWorkflows 수정</span><span class="sxs-lookup"><span data-stu-id="184db-3159">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="184db-3160">Az.Network</span><span class="sxs-lookup"><span data-stu-id="184db-3160">Az.Network</span></span>
* <span data-ttu-id="184db-3161">Network cmdlet에 와일드 카드 지원 추가</span><span class="sxs-lookup"><span data-stu-id="184db-3161">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="184db-3162">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="184db-3162">Az.RecoveryServices</span></span>
* <span data-ttu-id="184db-3163">Azure VM 지원에 SQL 서버가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-3163">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="184db-3164">SDK 업데이트</span><span class="sxs-lookup"><span data-stu-id="184db-3164">SDK Update</span></span>
* <span data-ttu-id="184db-3165">VMappContainer 체크 인 Get-ProtectableItem 제거</span><span class="sxs-lookup"><span data-stu-id="184db-3165">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="184db-3166">Get ProtectableItem의 매개 변수로 Name과 ServerName이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-3166">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="184db-3167">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="184db-3167">Az.Resources</span></span>
* <span data-ttu-id="184db-3168">`-TemplateObject` 매개 변수를 추가하여 cmdlet을 배포</span><span class="sxs-lookup"><span data-stu-id="184db-3168">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="184db-3169">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/2933 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="184db-3169">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="184db-3170">`Get-AzResource`의 결과를 `Set-AzResource`(으)로 파이프할 때 발생하는 문제 수정</span><span class="sxs-lookup"><span data-stu-id="184db-3170">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="184db-3171">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/8240 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="184db-3171">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="184db-3172">실행 시 JSON 데이터 형식 문제 해결 `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="184db-3172">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="184db-3173">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/7930 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="184db-3173">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="184db-3174">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="184db-3174">Az.Sql</span></span>
* <span data-ttu-id="184db-3175">AuditingEndpointsCommunicator를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="184db-3175">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="184db-3176">새 진단 설정을 생성할 때 에지 사례의 동작을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="184db-3176">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="184db-3177">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="184db-3177">Az.Storage</span></span>
* <span data-ttu-id="184db-3178">스토리지 계정      - New-AzStorageAccount를 생성할 때 종류 BlockBlobStorage를 지원</span><span class="sxs-lookup"><span data-stu-id="184db-3178">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="184db-3179">1.4.0 - 2019년 2월</span><span class="sxs-lookup"><span data-stu-id="184db-3179">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="184db-3180">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="184db-3180">Az.AnalysisServices</span></span>
* <span data-ttu-id="184db-3181">사용되지 않는 AddAzureASAccount cmdlet</span><span class="sxs-lookup"><span data-stu-id="184db-3181">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="184db-3182">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="184db-3182">Az.Automation</span></span>
* <span data-ttu-id="184db-3183">Import-AzAutomationDscNodeConfiguration 도움말 업데이트</span><span class="sxs-lookup"><span data-stu-id="184db-3183">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="184db-3184">Import-AzAutomationDscConfiguration cmdlet 구성 이름 유효성 검사 추가</span><span class="sxs-lookup"><span data-stu-id="184db-3184">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="184db-3185">Import-AzAutomationDscConfiguration cmdlet 오류 처리 개선</span><span class="sxs-lookup"><span data-stu-id="184db-3185">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="184db-3186">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="184db-3186">Az.CognitiveServices</span></span>
* <span data-ttu-id="184db-3187">리소스의 하위 도메인을 지정하는 데 사용되는 New-AzCognitiveServicesAccount에 대한 새 선택적 매개 변수로 CustomSubdomainName이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-3187">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="184db-3188">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="184db-3188">Az.Compute</span></span>
* <span data-ttu-id="184db-3189">ID 매개 변수 집합 문제 해결</span><span class="sxs-lookup"><span data-stu-id="184db-3189">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="184db-3190">Name 매개 변수를 제공하지 않으면 Get-AzVMExtension이 설치된 모든 확장을 열거하도록 업데이트</span><span class="sxs-lookup"><span data-stu-id="184db-3190">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="184db-3191">Update-AzImage cmdlet에 태그 및 ResourceId 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="184db-3191">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="184db-3192">인스턴스 ID가 없는 Get-AzVmssVM과 InstanceView를 사용하면 인스턴스 보기가 있는 VMSS VM을 나열할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-3192">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="184db-3193">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="184db-3193">Az.DataLakeStore</span></span>
* <span data-ttu-id="184db-3194">ADL 삭제된 항목 열거 및 복원에 대한 cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="184db-3194">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="184db-3195">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="184db-3195">Az.EventHub</span></span>
* <span data-ttu-id="184db-3196">Eventhub의 CaptureDescription 클래스에서 빈 보관을 건너뛰는 새 부울 속성 SkipEmptyArchives가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-3196">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="184db-3197">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="184db-3197">Az.KeyVault</span></span>
* <span data-ttu-id="184db-3198">Set-AzKeyVaultSecret 태그 지정 수정</span><span class="sxs-lookup"><span data-stu-id="184db-3198">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="184db-3199">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="184db-3199">Az.LogicApp</span></span>
* <span data-ttu-id="184db-3200">통합 계정에 대한 기본 sku 추가</span><span class="sxs-lookup"><span data-stu-id="184db-3200">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="184db-3201">XSLT 2.0, XSLT 3.0, Liquid 맵 형식 추가</span><span class="sxs-lookup"><span data-stu-id="184db-3201">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="184db-3202">통합 계정 어셈블리에 대한 새 cmdlet</span><span class="sxs-lookup"><span data-stu-id="184db-3202">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="184db-3203">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="184db-3203">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="184db-3204">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="184db-3204">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="184db-3205">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="184db-3205">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="184db-3206">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="184db-3206">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="184db-3207">통합 계정 일괄 처리 구성에 대한 새 cmdlet</span><span class="sxs-lookup"><span data-stu-id="184db-3207">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="184db-3208">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="184db-3208">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="184db-3209">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="184db-3209">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="184db-3210">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="184db-3210">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="184db-3211">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="184db-3211">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="184db-3212">논리 앱 SDK를 버전 4.1.0으로 업데이트</span><span class="sxs-lookup"><span data-stu-id="184db-3212">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="184db-3213">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="184db-3213">Az.Monitor</span></span>
* <span data-ttu-id="184db-3214">Get-AzMetric에 대한 도움말 업데이트</span><span class="sxs-lookup"><span data-stu-id="184db-3214">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="184db-3215">Az.Network</span><span class="sxs-lookup"><span data-stu-id="184db-3215">Az.Network</span></span>
* <span data-ttu-id="184db-3216">Add-AzApplicationGatewayCustomError에 대한 도움말 예제 업데이트</span><span class="sxs-lookup"><span data-stu-id="184db-3216">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="184db-3217">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="184db-3217">Az.OperationalInsights</span></span>
* <span data-ttu-id="184db-3218">New 및 Get ApplicationInsights 데이터 소스에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="184db-3218">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="184db-3219">지정된 작업 영역에 대한 특정 또는 전체 ApplicationInsights 데이터 원본 가져오기를 지원하기 위한 새로운 'ApplicationInsights' 종류가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-3219">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span>
    - <span data-ttu-id="184db-3220">지정된 Application-Insights 리소스 매개 변수(구독 ID, resourceGroupName 및 이름)별로 데이터 원본을 만들기 위한 New-AzOperationalInsightsApplicationInsightsDataSource cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-3220">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span>

#### <a name="azresources"></a><span data-ttu-id="184db-3221">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="184db-3221">Az.Resources</span></span>
* <span data-ttu-id="184db-3222">문제 https://github.com/Azure/azure-powershell/issues/8166 수정</span><span class="sxs-lookup"><span data-stu-id="184db-3222">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="184db-3223">문제 https://github.com/Azure/azure-powershell/issues/8235 수정</span><span class="sxs-lookup"><span data-stu-id="184db-3223">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="184db-3224">문제 https://github.com/Azure/azure-powershell/issues/6219 수정</span><span class="sxs-lookup"><span data-stu-id="184db-3224">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="184db-3225">KeyCredentials 반복 만들기를 방지하기 위해 버그 수정</span><span class="sxs-lookup"><span data-stu-id="184db-3225">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="184db-3226">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="184db-3226">Az.Sql</span></span>
* <span data-ttu-id="184db-3227">SQL DB 하이퍼스케일에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="184db-3227">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="184db-3228">복원 요청에서 불필요한 속성을 설정하여 복원이 실패할 수 있는 버그 수정</span><span class="sxs-lookup"><span data-stu-id="184db-3228">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="184db-3229">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="184db-3229">Az.Websites</span></span>
* <span data-ttu-id="184db-3230">Get-AzWebAppSlotMetrics 내 올바른 예제</span><span class="sxs-lookup"><span data-stu-id="184db-3230">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="184db-3231">1.3.0 - 2019년 2월</span><span class="sxs-lookup"><span data-stu-id="184db-3231">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="184db-3232">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="184db-3232">Az.Accounts</span></span>
* <span data-ttu-id="184db-3233">ClientRuntime 최신 버전 업데이트</span><span class="sxs-lookup"><span data-stu-id="184db-3233">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="184db-3234">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="184db-3234">Az.AnalysisServices</span></span>
<span data-ttu-id="184db-3235">Az.AnalysisServices 모듈의 전반적인 가용성.</span><span class="sxs-lookup"><span data-stu-id="184db-3235">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="184db-3236">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="184db-3236">Az.Compute</span></span>
* <span data-ttu-id="184db-3237">AEM 확장: UltraSSD 및 P60, P70, P80 디스크에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="184db-3237">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="184db-3238">Set-AzVMBootDiagnostics에 대한 도움말 업데이트</span><span class="sxs-lookup"><span data-stu-id="184db-3238">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="184db-3239">Update-AzImage에 대한 도움말 및 예제 업데이트</span><span class="sxs-lookup"><span data-stu-id="184db-3239">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="184db-3240">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="184db-3240">Az.RecoveryServices</span></span>
<span data-ttu-id="184db-3241">Az.RecoveryServices 모듈의 전반적인 가용성.</span><span class="sxs-lookup"><span data-stu-id="184db-3241">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="184db-3242">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="184db-3242">Az.Resources</span></span>
* <span data-ttu-id="184db-3243">리소스 그룹 관련 태그 수정</span><span class="sxs-lookup"><span data-stu-id="184db-3243">Fix tagging for resource groups</span></span>
    - <span data-ttu-id="184db-3244">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/8166 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="184db-3244">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="184db-3245">`Get-AzureRmRoleAssignment`이(가) -ErrorAction을 준수하지 않는 문제 수정</span><span class="sxs-lookup"><span data-stu-id="184db-3245">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span>
    - <span data-ttu-id="184db-3246">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/8235 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="184db-3246">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="184db-3247">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="184db-3247">Az.Sql</span></span>
* <span data-ttu-id="184db-3248">AzSqlDatabaseBackupShortTermRetentionPolicy 가져오기/설정하기 추가</span><span class="sxs-lookup"><span data-stu-id="184db-3248">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="184db-3249">SQL cmdlet을 실행할 경우 Azure 계정에 로그인되어 있지 않은 것이 nullref 예외를 초래하는 문제 수정</span><span class="sxs-lookup"><span data-stu-id="184db-3249">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="184db-3250">Get-AzSqlCapability의 nullref 예외 수정</span><span class="sxs-lookup"><span data-stu-id="184db-3250">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="184db-3251">1.2.1 - 2019년 1월</span><span class="sxs-lookup"><span data-stu-id="184db-3251">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="184db-3252">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="184db-3252">Az.Accounts</span></span>
* <span data-ttu-id="184db-3253">올바른 인증 버전을 사용하여 릴리스</span><span class="sxs-lookup"><span data-stu-id="184db-3253">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="184db-3254">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="184db-3254">Az.AnalysisServices</span></span>
* <span data-ttu-id="184db-3255">업데이트된 인증 종속성을 사용하여 릴리스</span><span class="sxs-lookup"><span data-stu-id="184db-3255">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="184db-3256">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="184db-3256">Az.RecoveryServices</span></span>
* <span data-ttu-id="184db-3257">업데이트된 인증 종속성을 사용하여 릴리스</span><span class="sxs-lookup"><span data-stu-id="184db-3257">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="184db-3258">1.2.0 - 2019년 1월</span><span class="sxs-lookup"><span data-stu-id="184db-3258">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="184db-3259">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="184db-3259">Az.Accounts</span></span>
* <span data-ttu-id="184db-3260">Windows PowerShell 5.1 전용 대화형 사용자 이름/암호 인증 추가</span><span class="sxs-lookup"><span data-stu-id="184db-3260">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="184db-3261">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="184db-3261">Update incorrect online help URLs</span></span>
* <span data-ttu-id="184db-3262">Uninstall-AzureRm 관련 PS Core에 경고 메시지 추가</span><span class="sxs-lookup"><span data-stu-id="184db-3262">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="184db-3263">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="184db-3263">Az.Aks</span></span>
* <span data-ttu-id="184db-3264">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="184db-3264">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="184db-3265">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="184db-3265">Az.Automation</span></span>
* <span data-ttu-id="184db-3266">Python 2 Runbook에 대한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-3266">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="184db-3267">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="184db-3267">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="184db-3268">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="184db-3268">Az.Cdn</span></span>
* <span data-ttu-id="184db-3269">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="184db-3269">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="184db-3270">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="184db-3270">Az.Compute</span></span>
* <span data-ttu-id="184db-3271">Invoke-AzVMReimage cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="184db-3271">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="184db-3272">Set-AzVmss에 TempDisk 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="184db-3272">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="184db-3273">New-AzVM 경고 메시지 수정</span><span class="sxs-lookup"><span data-stu-id="184db-3273">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="184db-3274">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="184db-3274">Az.ContainerRegistry</span></span>
* <span data-ttu-id="184db-3275">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="184db-3275">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="184db-3276">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="184db-3276">Az.DataFactory</span></span>
* <span data-ttu-id="184db-3277">ADF.Net SDK 버전이 3.0.0으로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-3277">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="184db-3278">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="184db-3278">Az.DataLakeStore</span></span>
* <span data-ttu-id="184db-3279">MSI를 사용할 때 ADLS 엔드포인트 문제 수정</span><span class="sxs-lookup"><span data-stu-id="184db-3279">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="184db-3280">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/7462 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="184db-3280">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="184db-3281">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="184db-3281">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="184db-3282">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="184db-3282">Az.IotHub</span></span>
* <span data-ttu-id="184db-3283">Add-IotHubRoutingEndpoint cmdlet에 인코딩 형식을 추가하세요.</span><span class="sxs-lookup"><span data-stu-id="184db-3283">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="184db-3284">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="184db-3284">Az.KeyVault</span></span>
* <span data-ttu-id="184db-3285">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="184db-3285">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="184db-3286">Az.Network</span><span class="sxs-lookup"><span data-stu-id="184db-3286">Az.Network</span></span>
* <span data-ttu-id="184db-3287">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="184db-3287">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="184db-3288">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="184db-3288">Az.Resources</span></span>
* <span data-ttu-id="184db-3289">'New-AzADAppCredential' 및 'New-AzADSpCredential' 참조 설명서의 잘못된 예제 수정</span><span class="sxs-lookup"><span data-stu-id="184db-3289">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="184db-3290">리소스 그룹 배포 cmdlet 실행 전 '-TemplateFile' 매개 변수 경로가 확인되지 않는 문제 수정</span><span class="sxs-lookup"><span data-stu-id="184db-3290">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="184db-3291">Az.Resources: New-AzureRmPolicyDefinition -Mode 기본값에 대한 올바른 설명서</span><span class="sxs-lookup"><span data-stu-id="184db-3291">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="184db-3292">Az.Resources: 문제 https://github.com/Azure/azure-powershell/issues/7522 수정</span><span class="sxs-lookup"><span data-stu-id="184db-3292">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="184db-3293">Az.Resources: 문제 https://github.com/Azure/azure-powershell/issues/5747 수정</span><span class="sxs-lookup"><span data-stu-id="184db-3293">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="184db-3294">'PSResourceGroupDeployment' 개체의 서식 문제 수정</span><span class="sxs-lookup"><span data-stu-id="184db-3294">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="184db-3295">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/2123 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="184db-3295">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="184db-3296">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="184db-3296">Az.ServiceFabric</span></span>
* <span data-ttu-id="184db-3297">인증서가 VMSS 모델에 추가되었는데도 예외가 발생할 경우 롤백합니다. 이는 버그 https://github.com/Azure/service-fabric-issues/issues/932 를 수정하기 위함입니다.</span><span class="sxs-lookup"><span data-stu-id="184db-3297">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="184db-3298">일부 오류 메시지를 수정하세요.</span><span class="sxs-lookup"><span data-stu-id="184db-3298">Fix some error messages.</span></span>
* <span data-ttu-id="184db-3299">Az로의 마이그레이션을 통해서는 작동하지 않는 New-AzServiceFabriCluster를 위해 기본값 ARM 템플릿을 가진 클러스터 만들기를 수정하세요.</span><span class="sxs-lookup"><span data-stu-id="184db-3299">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="184db-3300">확장에서 클러스터 id를 확인하여 클러스터에 해당하는 VMSS에만 추가되도록 클러스터/애플리케이션 인증서 추가를 수정하세요.</span><span class="sxs-lookup"><span data-stu-id="184db-3300">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="184db-3301">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="184db-3301">Az.SignalR</span></span>
* <span data-ttu-id="184db-3302">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="184db-3302">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="184db-3303">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="184db-3303">Az.Sql</span></span>
* <span data-ttu-id="184db-3304">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="184db-3304">Update incorrect online help URLs</span></span>
* <span data-ttu-id="184db-3305">가능한 값을 가진 LicenseType 매개 변수에 대한 매개 변수 설명이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-3305">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="184db-3306">유일하게 업데이트된 속성인데 작동하지 않는 관리되는 인스턴스 ID의 업데이트 수정</span><span class="sxs-lookup"><span data-stu-id="184db-3306">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="184db-3307">관리되는 인스턴스에서의 사용자 지정 데이터 정렬에 대한 지원</span><span class="sxs-lookup"><span data-stu-id="184db-3307">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="184db-3308">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="184db-3308">Az.Storage</span></span>
* <span data-ttu-id="184db-3309">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="184db-3309">Update incorrect online help URLs</span></span>
* <span data-ttu-id="184db-3310">Premium Storage 계정이 클래식 로깅/메트릭을 지원하지 않기 때문에, Premium Storage 계정의 클래식 로깅/메트릭을 가져올/설정할 때 상세한 오류 메시지를 제공해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="184db-3310">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="184db-3311">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="184db-3311">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="184db-3312">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="184db-3312">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="184db-3313">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="184db-3313">Az.TrafficManager</span></span>
* <span data-ttu-id="184db-3314">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="184db-3314">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="184db-3315">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="184db-3315">Az.Websites</span></span>
* <span data-ttu-id="184db-3316">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="184db-3316">Update incorrect online help URLs</span></span>
* <span data-ttu-id="184db-3317">앱이 ASE에 호스팅되면 'New-AzWebAppSSLBinding'을 수정하여 올바른 resourcegroup+location에 인증서를 업로드합니다.</span><span class="sxs-lookup"><span data-stu-id="184db-3317">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="184db-3318">'New-AzWebAppSSLBinding'을 수정하여 SSL 인증서를 앱에 바인딩하는 데 붙는 태그를 덮어쓰지 않도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="184db-3318">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="184db-3319">1.1.0 - 2019년 1월</span><span class="sxs-lookup"><span data-stu-id="184db-3319">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="184db-3320">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="184db-3320">Az.Accounts</span></span>
* <span data-ttu-id="184db-3321">Enable-AzureRmAlias에 'Local' 범위 추가</span><span class="sxs-lookup"><span data-stu-id="184db-3321">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="184db-3322">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="184db-3322">Az.Compute</span></span>
* <span data-ttu-id="184db-3323">이름이 Restart/Start/Stop/Remove/Set-AzVM과 Save-AzVMImage에 설정된 ID 매개 변수에서 선택 사항이 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-3323">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="184db-3324">도움말 파일의 ID에 대한 설명이 업데이트 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-3324">Updated the description of ID in help files</span></span>
* <span data-ttu-id="184db-3325">Az.Accounts 모듈을 사용할 때의 이전 버전과의 호환성 문제를 해결합니다.</span><span class="sxs-lookup"><span data-stu-id="184db-3325">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="184db-3326">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="184db-3326">Az.DataLakeStore</span></span>
* <span data-ttu-id="184db-3327">SDK 수정을 위해 데이터 평면의 SDK 버전을 1.1.14로 업데이트하세요.</span><span class="sxs-lookup"><span data-stu-id="184db-3327">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="184db-3328">getfilestatus 및 liststatus에 대한 음수 acesstime 및 modificationtime 수정, 비동기 취소 토큰 수정</span><span class="sxs-lookup"><span data-stu-id="184db-3328">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="184db-3329">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="184db-3329">Az.EventGrid</span></span>
* <span data-ttu-id="184db-3330">2019-01-01 API 버전을 사용하도록 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-3330">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="184db-3331">2019-01-01 API 버전에서 새 시나리오를 지원하도록 다음 cmdlet을 업데이트</span><span class="sxs-lookup"><span data-stu-id="184db-3331">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="184db-3332">New-AzureRmEventGridSubscription: 지정을 위한 새로운 선택적 매개 변수를 추가</span><span class="sxs-lookup"><span data-stu-id="184db-3332">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="184db-3333">이벤트 Time-to-Live</span><span class="sxs-lookup"><span data-stu-id="184db-3333">Event Time-To-Live,</span></span>
        - <span data-ttu-id="184db-3334">이벤트에 대한 최대 배달 시도</span><span class="sxs-lookup"><span data-stu-id="184db-3334">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="184db-3335">배달 못한 편지의 엔드포인트입니다.</span><span class="sxs-lookup"><span data-stu-id="184db-3335">Dead letter endpoint.</span></span>
    - <span data-ttu-id="184db-3336">Update-AzureRmEventGridSubscription: 지정을 위한 새로운 선택적 매개 변수를 추가</span><span class="sxs-lookup"><span data-stu-id="184db-3336">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="184db-3337">이벤트 Time-to-Live</span><span class="sxs-lookup"><span data-stu-id="184db-3337">Event Time-To-Live,</span></span>
        - <span data-ttu-id="184db-3338">이벤트에 대한 최대 배달 시도</span><span class="sxs-lookup"><span data-stu-id="184db-3338">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="184db-3339">배달 못한 편지의 엔드포인트입니다.</span><span class="sxs-lookup"><span data-stu-id="184db-3339">Dead letter endpoint.</span></span>
* <span data-ttu-id="184db-3340">New-AzureRmEventGridSubscription 및 Update-AzureRmEventGridSubscription cmdlet의 EndpointType 옵션에 새 열거형 값(즉, storageQueue 및 hybridConnection)을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="184db-3340">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="184db-3341">이벤트 구독을 생성 또는 업데이트할 때 사용자가 직접 조치를 취해야 할 경우 경고 메시지를 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="184db-3341">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="184db-3342">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="184db-3342">Az.IotHub</span></span>
* <span data-ttu-id="184db-3343">최신 버전의 Azure IotHub SDK로 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="184db-3343">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="184db-3344">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="184db-3344">Az.LogicApp</span></span>
* <span data-ttu-id="184db-3345">지정된 이름이 없는 모든 Get-AzLogicApp 목록</span><span class="sxs-lookup"><span data-stu-id="184db-3345">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="184db-3346">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="184db-3346">Az.Resources</span></span>
* <span data-ttu-id="184db-3347">'Get-AzResource'에 '-ODataQuery'및 '-ResourceId' 매개 변수를 제공할 때 매개 변수 집합 문제 수정</span><span class="sxs-lookup"><span data-stu-id="184db-3347">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="184db-3348">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/7875 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="184db-3348">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="184db-3349">New/Set-AzPolicyDefinition에서 -Custom 매개 변수 처리 문제 수정</span><span class="sxs-lookup"><span data-stu-id="184db-3349">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="184db-3350">New-AzDeployment 설명서에서 오타 수정</span><span class="sxs-lookup"><span data-stu-id="184db-3350">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="184db-3351">'New-AzADUser'에 '-MailNickname'매개 변수가 필수 항목으로 지정됨</span><span class="sxs-lookup"><span data-stu-id="184db-3351">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="184db-3352">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/8220 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="184db-3352">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="184db-3353">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="184db-3353">Az.SignalR</span></span>
* <span data-ttu-id="184db-3354">Az.Accounts 모듈을 사용할 때의 이전 버전과의 호환성 문제를 해결합니다.</span><span class="sxs-lookup"><span data-stu-id="184db-3354">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="184db-3355">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="184db-3355">Az.Sql</span></span>
* <span data-ttu-id="184db-3356">Storage 관리 클라이언트 종속성을 일반적인 SDK 구현으로 변환했습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-3356">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="184db-3357">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="184db-3357">Az.Storage</span></span>
* <span data-ttu-id="184db-3358">Sas Token, OAuth 또는 Anonymous를 사용하여 스토리지 컨텍스트의 StorageAccountName을 실제 스토리지 계정 이름으로 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="184db-3358">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="184db-3359">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="184db-3359">New-AzStorageContext</span></span>
* <span data-ttu-id="184db-3360">'-FullUri' 매개 변수를 사용하여 Blob 스냅샷 개체의 Sas Token을 생성하고 반환된 Uri를 스냅샷 Uri로 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="184db-3360">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="184db-3361">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="184db-3361">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="184db-3362">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="184db-3362">Az.Websites</span></span>
* <span data-ttu-id="184db-3363">'Get-AzDeletedWebApp'의 날짜 구문 분석 버그를 수정했습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-3363">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="184db-3364">Az.Accounts 모듈을 사용할 때의 이전 버전과의 호환성 문제를 해결합니다.</span><span class="sxs-lookup"><span data-stu-id="184db-3364">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="184db-3365">1.0.0 - 2018년 12월</span><span class="sxs-lookup"><span data-stu-id="184db-3365">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="184db-3366">일반</span><span class="sxs-lookup"><span data-stu-id="184db-3366">General</span></span>

- <span data-ttu-id="184db-3367">Az 모듈 일반 공급</span><span class="sxs-lookup"><span data-stu-id="184db-3367">General Availability of Az Module</span></span>
- <span data-ttu-id="184db-3368">각 모듈에 대 한 온라인 도움말</span><span class="sxs-lookup"><span data-stu-id="184db-3368">Online help for each module</span></span>
- <span data-ttu-id="184db-3369">자세한 내용과 로드맵은 [Az 알림 페이지](https://aka.ms/azps-announce)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="184db-3369">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="184db-3370">AzureRM에서 마이그레이션하는 것에 대한 정보는 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="184db-3370">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="184db-3371">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="184db-3371">Az.Accounts</span></span>
- <span data-ttu-id="184db-3372">Az.Profile에서 변경</span><span class="sxs-lookup"><span data-stu-id="184db-3372">Changed from Az.Profile</span></span>
- <span data-ttu-id="184db-3373">프로필 및 컨텍스트 형식에 대한 표 형식 수정</span><span class="sxs-lookup"><span data-stu-id="184db-3373">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="184db-3374">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="184db-3374">Az.ApiManagement</span></span>
- <span data-ttu-id="184db-3375">#7002에 대한 수정</span><span class="sxs-lookup"><span data-stu-id="184db-3375">Fixes for #7002</span></span>
- <span data-ttu-id="184db-3376">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="184db-3376">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="184db-3377">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="184db-3377">Az.Batch</span></span>
- <span data-ttu-id="184db-3378">`PSComputeNode`의 새로운 `NodeAgentInformation` 속성을 통해 풀의 각 VM에서 실행 중인 Azure Batch 노드 에이전트의 버전을 확인하는 기능이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-3378">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="184db-3379">`PSDataDisk`에 대한 `Caching` 기본 값은 이제 `None` 대신 `ReadWrite`입니다.</span><span class="sxs-lookup"><span data-stu-id="184db-3379">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="184db-3380">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="184db-3380">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="184db-3381">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="184db-3381">Az.Billing</span></span>
- <span data-ttu-id="184db-3382">청구, 소비 및 UsageAggregates cmdlet 결합 cmdlet에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="184db-3382">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="184db-3383">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="184db-3383">Az.CognitivServices</span></span>
- <span data-ttu-id="184db-3384">New-AzureRmCognitiveServicesAccount 작업에서 사용 가능한 SkuName 및 Typem에 대한 완성자 추가</span><span class="sxs-lookup"><span data-stu-id="184db-3384">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="184db-3385">Get-AzCognitiveServicesAccountSkus에서 GetSkusWithAccountParamSetName 매개 변수 집합을 제거</span><span class="sxs-lookup"><span data-stu-id="184db-3385">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="184db-3386">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="184db-3386">Az.ContainerInstance</span></span>
- <span data-ttu-id="184db-3387">ManagedIdentity 지원이 추가됨</span><span class="sxs-lookup"><span data-stu-id="184db-3387">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="184db-3388">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="184db-3388">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="184db-3389">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="184db-3389">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="184db-3390">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="184db-3390">Az.DataLakeStore</span></span>
- <span data-ttu-id="184db-3391">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="184db-3391">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="184db-3392">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="184db-3392">Az.Monitor</span></span>
- <span data-ttu-id="184db-3393">Az.Monitor 이름 변경 및 기타 사소한 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="184db-3393">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="184db-3394">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="184db-3394">Az.KeyVault</span></span>
- <span data-ttu-id="184db-3395">출력 형식에서 사용되지 않는 'PurgeDisabled' 속성 제거</span><span class="sxs-lookup"><span data-stu-id="184db-3395">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="184db-3396">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="184db-3396">Az.MachineLearning</span></span>
- <span data-ttu-id="184db-3397">Az.MachineLearningCompute 모듈의 cmdlet 포함</span><span class="sxs-lookup"><span data-stu-id="184db-3397">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="184db-3398">Az.Media</span><span class="sxs-lookup"><span data-stu-id="184db-3398">Az.Media</span></span>
- <span data-ttu-id="184db-3399">New-AzMediaService에서 사용되지 않는 -Tags 별칭이 제거됨</span><span class="sxs-lookup"><span data-stu-id="184db-3399">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="184db-3400">Az.Network</span><span class="sxs-lookup"><span data-stu-id="184db-3400">Az.Network</span></span>
<span data-ttu-id="184db-3401">Application Gateway에서 RewriteRuleSets를 구성하는 것에 대한 지원이 추가됨</span><span class="sxs-lookup"><span data-stu-id="184db-3401">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="184db-3402">추가된 새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-3402">New cmdlets added:</span></span>
        - <span data-ttu-id="184db-3403">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="184db-3403">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="184db-3404">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="184db-3404">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="184db-3405">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="184db-3405">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="184db-3406">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="184db-3406">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="184db-3407">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="184db-3407">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="184db-3408">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="184db-3408">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="184db-3409">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="184db-3409">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="184db-3410">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="184db-3410">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="184db-3411">선택적 매개 변수를 사용하도록 cmdlet이 업데이트됨 -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="184db-3411">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="184db-3412">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="184db-3412">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="184db-3413">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="184db-3413">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="184db-3414">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="184db-3414">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="184db-3415">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="184db-3415">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="184db-3416">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="184db-3416">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="184db-3417">New-AzureRmApplicationGatewayUrlPathMapConfig로 ID를 사용하여 Application Gateway에 KeyVault 지원을 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-3417">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="184db-3418">선택적 매개 변수를 사용하도록 cmdlet이 업데이트됨 -KeyVaultSecretId, -KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="184db-3418">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="184db-3419">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="184db-3419">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="184db-3420">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="184db-3420">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="184db-3421">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="184db-3421">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="184db-3422">New-AzApplicationGateway cmdlet이 선택적 매개 변수를 사용하도록 업데이트됨 -UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="184db-3422">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="184db-3423">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="184db-3423">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="184db-3424">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="184db-3424">Az.OperationalInsights</span></span>
- <span data-ttu-id="184db-3425">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="184db-3425">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="184db-3426">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="184db-3426">Az.Profile</span></span>
- <span data-ttu-id="184db-3427">Az.Accounts에 모듈 이름이 변경됨</span><span class="sxs-lookup"><span data-stu-id="184db-3427">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="184db-3428">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="184db-3428">Az.RecoveryServices</span></span>
- <span data-ttu-id="184db-3429">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="184db-3429">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="184db-3430">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="184db-3430">Az.Resources</span></span>
- <span data-ttu-id="184db-3431">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="184db-3431">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="184db-3432">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="184db-3432">Az.ServiceFabric</span></span>
- <span data-ttu-id="184db-3433">일반 이름과 지문으로 지정 인증서 지원</span><span class="sxs-lookup"><span data-stu-id="184db-3433">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="184db-3434">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="184db-3434">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="184db-3435">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="184db-3435">Az.SIgnalR</span></span>
- <span data-ttu-id="184db-3436">SIgnalR에 대한 PowerShell cmdlet에 대한 일반 공급</span><span class="sxs-lookup"><span data-stu-id="184db-3436">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="184db-3437">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="184db-3437">Az.Sql</span></span>
- <span data-ttu-id="184db-3438">위협 탐지의 cmdlet에 새로운 Data_Exfiltration 및 Unsafe_Action 검색 유형 추가</span><span class="sxs-lookup"><span data-stu-id="184db-3438">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="184db-3439">Sql 감사 cmdlet에 대한 설명서 예제 업데이트</span><span class="sxs-lookup"><span data-stu-id="184db-3439">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="184db-3440">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="184db-3440">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="184db-3441">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="184db-3441">Az.Storage</span></span>
- <span data-ttu-id="184db-3442">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="184db-3442">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="184db-3443">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="184db-3443">Az.Websites</span></span>
- <span data-ttu-id="184db-3444">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="184db-3444">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="184db-3445">0.7.0 - 2018년 12월</span><span class="sxs-lookup"><span data-stu-id="184db-3445">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="184db-3446">일반</span><span class="sxs-lookup"><span data-stu-id="184db-3446">General</span></span>

* <span data-ttu-id="184db-3447">AzureRM에서 Az 전환 예정에 대한 사소한 변경</span><span class="sxs-lookup"><span data-stu-id="184db-3447">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="184db-3448">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="184db-3448">Az.Compute</span></span>

* <span data-ttu-id="184db-3449">`New-AzVm(ss)` cmdlet에 대한 간단한 매개 변수 집합에 UltraSSD 및 갤러리 이미지에 대한 지원을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="184db-3449">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="184db-3450">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="184db-3450">Az.DataLakeStore</span></span>

* <span data-ttu-id="184db-3451">ADLS 계정의 도메인의 후행 슬래시를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="184db-3451">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="184db-3452">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="184db-3452">Az.FrontDoor</span></span>

* <span data-ttu-id="184db-3453">일부 끊어진 링크 수정</span><span class="sxs-lookup"><span data-stu-id="184db-3453">Fixed some broken links</span></span>
    - <span data-ttu-id="184db-3454">New-AzureRmFrontDoor 및 Set-AzureRmFrontDoor 아티클에서 New-AzureRmFrontDoorHealthProbeSettingObject cmdlet 아티클에 대한 링크가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-3454">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="184db-3455">New-AzureRmFrontDoorManagedRuleObject 아티클에서 New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet 아티클에 대한 링크가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-3455">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="184db-3456">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="184db-3456">Az.RecoveryServices</span></span>

* <span data-ttu-id="184db-3457">Azure File Share 복원 작업에 클라이언트 측 유효성 검사가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-3457">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="184db-3458">afs 복원의 경우 storageAccountName 및 storageAccountResourceGroupName을 선택적으로 만들었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-3458">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="184db-3459">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="184db-3459">Az.Resources</span></span>

* <span data-ttu-id="184db-3460"> https://github.com/Azure/azure-powershell/issues/7679 에 대한 수정</span><span class="sxs-lookup"><span data-stu-id="184db-3460">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="184db-3461">기본 관리자를 요청할 때 구독 범위가 제공되는 경우 Get-AzureRmRoleAssignment를 업데이트하여 구독 범위를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="184db-3461">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="184db-3462">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="184db-3462">Az.Sql</span></span>

* <span data-ttu-id="184db-3463">AzureRM에서 Az 전환 예정에 대한 사소한 변경</span><span class="sxs-lookup"><span data-stu-id="184db-3463">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="184db-3464">DotNet 코어에서 Get-AzureRmSqlDatabaseVulnerabilityAssessment를 사용하는 문제 해결</span><span class="sxs-lookup"><span data-stu-id="184db-3464">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="184db-3465">SQL 감사 cmdlet과 관련된 도움말 메시지의 설명서가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-3465">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="184db-3466">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="184db-3466">Az.Storage</span></span>

* <span data-ttu-id="184db-3467">New-AzureRmStorageAccount에 -EnableHierarchicalNamespace 추가</span><span class="sxs-lookup"><span data-stu-id="184db-3467">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="184db-3468">파일 복사 cmdlet이 -DestContext 입력이 없을 때 대상의 원본 컨텍스트를 다시 사용할 수 없는 문제 수정</span><span class="sxs-lookup"><span data-stu-id="184db-3468">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="184db-3469">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="184db-3469">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="184db-3470">고정적인 웹 사이트 구성 지원</span><span class="sxs-lookup"><span data-stu-id="184db-3470">Support Static Website configuration</span></span>
    - <span data-ttu-id="184db-3471">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="184db-3471">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="184db-3472">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="184db-3472">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="184db-3473">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="184db-3473">Az.Websites</span></span>

* <span data-ttu-id="184db-3474">Set-AzureRmWebApp 및 Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="184db-3474">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span>
    - <span data-ttu-id="184db-3475">Windows 및 Linux 컨테이너 응용 프로그램에 탑재할 Azure Storage 경로를 지정하기 위해 새 매개 변수(-AzureStoragePath)가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-3475">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="184db-3476">새 cmdlet New-AzureRmWebAppAzureStoragePath의 출력을 매개 변수로 사용하여 Azure Storage 경로를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="184db-3476">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="184db-3477">0.6.1 - 2018년 11월</span><span class="sxs-lookup"><span data-stu-id="184db-3477">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="184db-3478">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="184db-3478">Az.ApiManagement</span></span>
* <span data-ttu-id="184db-3479">형식 매핑 문제에 대한 종속성 업데이트</span><span class="sxs-lookup"><span data-stu-id="184db-3479">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="184db-3480">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="184db-3480">Az.Automation</span></span>
* <span data-ttu-id="184db-3481">Azure Automation cmdlet 기반 Swagger</span><span class="sxs-lookup"><span data-stu-id="184db-3481">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="184db-3482">업데이트 관리 cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="184db-3482">Added Update Management cmdlets</span></span>
* <span data-ttu-id="184db-3483">소스 제어 cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="184db-3483">Added Source Control cmdlets</span></span>
* <span data-ttu-id="184db-3484">Remove-AzureRmAutomationHybridWorkerGroup cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="184db-3484">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="184db-3485">DSC 노드 등록 명령 수정</span><span class="sxs-lookup"><span data-stu-id="184db-3485">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="184db-3486">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="184db-3486">Az.Compute</span></span>
* <span data-ttu-id="184db-3487">SystemAssigned ID에 대한 ID 문제 수정</span><span class="sxs-lookup"><span data-stu-id="184db-3487">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="184db-3488">형식 매핑 문제에 대한 종속성 업데이트</span><span class="sxs-lookup"><span data-stu-id="184db-3488">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="184db-3489">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="184db-3489">Az.ContainerInstance</span></span>
* <span data-ttu-id="184db-3490">형식 매핑 문제에 대한 종속성 업데이트</span><span class="sxs-lookup"><span data-stu-id="184db-3490">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="184db-3491">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="184db-3491">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="184db-3492">마켓플레이스 cmdlet에 대한 예제 설명 업데이트</span><span class="sxs-lookup"><span data-stu-id="184db-3492">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="184db-3493">Az.Network</span><span class="sxs-lookup"><span data-stu-id="184db-3493">Az.Network</span></span>
* <span data-ttu-id="184db-3494">New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="184db-3494">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="184db-3495">지원되는 AzureFirewall 네트워크 프로토콜에 ICMP 다시 추가</span><span class="sxs-lookup"><span data-stu-id="184db-3495">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="184db-3496">Test-AzureRmNetworkWatcherConnectivity cmdlet을 업데이트하여 대상 ID, 주소 및 포트 유효성 검사를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="184db-3496">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span>
* <span data-ttu-id="184db-3497">VirtualNetwork 맵의 메모리 사용 문제 해결</span><span class="sxs-lookup"><span data-stu-id="184db-3497">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="184db-3498">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="184db-3498">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="184db-3499">보호된 파일 공유에 대한 정책을 수정하는 것에 대해 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="184db-3499">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="184db-3500">정책 표준 시간대를 대문자로 변환했습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-3500">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="184db-3501">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="184db-3501">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="184db-3502">New-AzureRmRecoveryServicesAsrProtectableItem의 예제 정정</span><span class="sxs-lookup"><span data-stu-id="184db-3502">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="184db-3503">형식 매핑 문제에 대한 종속성 업데이트</span><span class="sxs-lookup"><span data-stu-id="184db-3503">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="184db-3504">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="184db-3504">Az.Relay</span></span>
* <span data-ttu-id="184db-3505">선택적 매개 변수 -KeyValue를 New-AzureRmRelayKey cmdlet에 추가하여 사용자가 KeyValue를 제공할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-3505">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="184db-3506">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="184db-3506">Az.Resources</span></span>
* <span data-ttu-id="184db-3507">`New-AzureRmPolicyAssignment` 및 `Set-AzureRmPolicyAssignment`의 자원 ID 관련 매개 변수에 대한 도움말 문서를 업데이트함</span><span class="sxs-lookup"><span data-stu-id="184db-3507">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="184db-3508">-Metadata를 사용하는 New-AzureRmPolicyDefinition에 대한 예제 추가</span><span class="sxs-lookup"><span data-stu-id="184db-3508">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="184db-3509">NetStandard의 태그 키에서 대소문자 보존을 허용하도록 수정: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="184db-3509">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="184db-3510">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="184db-3510">Az.ServiceFabric</span></span>
* <span data-ttu-id="184db-3511">향후 호환성이 손상되는 변경에 대한 사용 중단 메시지 추가</span><span class="sxs-lookup"><span data-stu-id="184db-3511">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="184db-3512">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="184db-3512">Az.Sql</span></span>
* <span data-ttu-id="184db-3513">Azure Sql Database Managed Instance 및 Azure Sql Managed Database에 CRUD 작업을 위한 새 cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="184db-3513">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="184db-3514">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="184db-3514">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="184db-3515">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="184db-3515">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="184db-3516">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="184db-3516">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="184db-3517">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="184db-3517">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="184db-3518">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="184db-3518">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="184db-3519">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="184db-3519">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="184db-3520">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="184db-3520">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="184db-3521">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="184db-3521">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="184db-3522">서버 또는 데이터베이스에서 확장 감사 정책 관리를 활성화했습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-3522">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="184db-3523">새 매개 변수(PredicateExpression)가 감사 로그 필터링을 사용하도록 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-3523">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="184db-3524">Cmdlet이 레거시 클라이언트 대신 SQL 클라이언트를 사용하도록 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-3524">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="184db-3525">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="184db-3525">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="184db-3526">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="184db-3526">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="184db-3527">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="184db-3527">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="184db-3528">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="184db-3528">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="184db-3529">스토리지 계정 이름 매개 변수가 설정된 Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings를 사용할 때의 문제 해결</span><span class="sxs-lookup"><span data-stu-id="184db-3529">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="184db-3530">0.5.0 - 2018년 11월</span><span class="sxs-lookup"><span data-stu-id="184db-3530">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="184db-3531">일반</span><span class="sxs-lookup"><span data-stu-id="184db-3531">General</span></span>
* <span data-ttu-id="184db-3532">많은 핵심 cmdlet에 Resource Completers를 추가하여 대화형으로 cmdlet을 호출할 때 기존 리소스 이름을 탭으로 이동할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-3532">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="184db-3533">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="184db-3533">Az.Profile</span></span>
* <span data-ttu-id="184db-3534">ClientRuntime의 최신 버전을 사용하도록 일반적인 코드를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="184db-3534">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="184db-3535">Connect-AzAccount cmdlet의 매개 변수 TenantId 이름을 Tenant로 바꾸고 TenantId의 별칭을 추가합니다</span><span class="sxs-lookup"><span data-stu-id="184db-3535">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="184db-3536">Connect-AzAccount의 업데이트된 TenantId 설명</span><span class="sxs-lookup"><span data-stu-id="184db-3536">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="184db-3537">테넌트 도메인을 제공할 때 실패한 로그인에 대한 오류 메시지 수정</span><span class="sxs-lookup"><span data-stu-id="184db-3537">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="184db-3538">테넌트에 구독이 없는 계정의 컨텍스트 이름 충돌 문제 수정</span><span class="sxs-lookup"><span data-stu-id="184db-3538">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="184db-3539">MSI를 사용할 때 DataLake 엔드포인트 문제 수정</span><span class="sxs-lookup"><span data-stu-id="184db-3539">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="184db-3540">연결되지 않은 경우 'Disconnect-AzAccount'가 throw하는 문제 수정</span><span class="sxs-lookup"><span data-stu-id="184db-3540">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="184db-3541">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="184db-3541">Az.CognitiveServices</span></span>
* <span data-ttu-id="184db-3542">Get-AzCognitiveServicesAccountSkus 작업을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="184db-3542">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="184db-3543">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="184db-3543">Az.Compute</span></span>
* <span data-ttu-id="184db-3544">Add-AzVmssVMDataDisk 및 Remove-AzVmssVMDataDisk cmdlet를 추가합니다</span><span class="sxs-lookup"><span data-stu-id="184db-3544">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="184db-3545">Get-AzVMImage는 AutomaticOSUpgradeProperties를 표시합니다</span><span class="sxs-lookup"><span data-stu-id="184db-3545">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="184db-3546">수정된 SetAzVMChefExtension -BootstrapOptions 및 -JsonAttribute option 값이 json 형식으로 설정하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-3546">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="184db-3547">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="184db-3547">Az.DataLakeStore</span></span>
* <span data-ttu-id="184db-3548">DataLake 패키지를 1.1.10으로 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="184db-3548">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="184db-3549">기본 동시성을 다중 스레드 작업에 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="184db-3549">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="184db-3550">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="184db-3550">Az.Insights</span></span>
* <span data-ttu-id="184db-3551">해결된 문제 #7267(자동 크기 조정 영역)</span><span class="sxs-lookup"><span data-stu-id="184db-3551">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="184db-3552">열거된 매개 변수를 제대로 설정하지 않은 새 자동 크기 조정 규칙을 만드는 데 문제가 있습니다(이를 항상 기본값으로 설정함).</span><span class="sxs-lookup"><span data-stu-id="184db-3552">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="184db-3553">해결된 문제 # 7513[자세한 정보] Set-AzDiagnosticSetting은 설정을 생성하는 동안 범주를 명시적으로 지정해야 합니다</span><span class="sxs-lookup"><span data-stu-id="184db-3553">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="184db-3554">이제 cmdlet은 생성 중에 사용할 범주를 명시적으로 표시할 필요가 없습니다. 즉, 문서화된대로 작동합니다</span><span class="sxs-lookup"><span data-stu-id="184db-3554">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="184db-3555">Az.Network</span><span class="sxs-lookup"><span data-stu-id="184db-3555">Az.Network</span></span>
* <span data-ttu-id="184db-3556">다음 cmdlet에 대해 PeeringType을 필수 매개 변수로 변경했습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-3556">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="184db-3557">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="184db-3557">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="184db-3558">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="184db-3558">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="184db-3559">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="184db-3559">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="184db-3560">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="184db-3560">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="184db-3561">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="184db-3561">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="184db-3562">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="184db-3562">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="184db-3563">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="184db-3563">Az.PolicyInsights</span></span>
* <span data-ttu-id="184db-3564">추가된 정책 재구성 cmdlet</span><span class="sxs-lookup"><span data-stu-id="184db-3564">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="184db-3565">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="184db-3565">Az.Resources</span></span>
* <span data-ttu-id="184db-3566"> https://github.com/Azure/azure-powershell/issues/7402 에 대한 수정</span><span class="sxs-lookup"><span data-stu-id="184db-3566">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="184db-3567">'Get-AzResource'에 대해 '-ResourceId' 매개 변수를 사용하여 리소스 나열 허용</span><span class="sxs-lookup"><span data-stu-id="184db-3567">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="184db-3568">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="184db-3568">Az.ServiceBus</span></span>
* <span data-ttu-id="184db-3569">마이그레이션 상태를 알 수 있도록 PSServiceBusMigrationConfigurationAttributes에 MigrationState 읽기 전용 속성 추가.</span><span class="sxs-lookup"><span data-stu-id="184db-3569">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="184db-3570">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="184db-3570">Az.ServiceFabric</span></span>
* <span data-ttu-id="184db-3571">Linux Vmss에 인증서 추가 수정.</span><span class="sxs-lookup"><span data-stu-id="184db-3571">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="184db-3572">Add-AzServiceFabricClusterCertificate 수정</span><span class="sxs-lookup"><span data-stu-id="184db-3572">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="184db-3573">새 인증서(Azure/service-fabric-issues#932)에서 올바른 지문을 사용.</span><span class="sxs-lookup"><span data-stu-id="184db-3573">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="184db-3574">올바르게 예외 표시(Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="184db-3574">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="184db-3575">Vmss CreateOrUpdate 작업을 시작하기 전에 'Update-AzServiceFabricDurability'를 수정하여 클러스터 구성 업데이트.</span><span class="sxs-lookup"><span data-stu-id="184db-3575">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="184db-3576">0.4.0 - 2018년 10월</span><span class="sxs-lookup"><span data-stu-id="184db-3576">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="184db-3577">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="184db-3577">Az.Profile</span></span>
* <span data-ttu-id="184db-3578">CloudShell에서 Get-AzSubscription을 사용하여 문제를 해결합니다.</span><span class="sxs-lookup"><span data-stu-id="184db-3578">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="184db-3579">ClientRuntime의 최신 버전을 사용하도록 일반적인 코드를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="184db-3579">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="184db-3580">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="184db-3580">Az.Compute</span></span>
* <span data-ttu-id="184db-3581">'New-AzVm'에 대해 간단한 매개 변수를 사용하는 경우 가속화된 네트워킹을 설정하기 위해 새 크기가 VM 크기의 허용 목록에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-3581">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="184db-3582">모든 cmdlet에 ResourceName 인수 완성자가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-3582">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="184db-3583">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="184db-3583">Az.DataLakeStore</span></span>
* <span data-ttu-id="184db-3584">Virtual Network 규칙에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="184db-3584">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="184db-3585">Get-AzDataLakeStoreVirtualNetworkRule: Azure Data Lake Store 가상 네트워크 규칙을 가져오거나 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="184db-3585">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="184db-3586">Add-AzDataLakeStoreVirtualNetworkRule: 지정된 Data Lake Store 계정에 가상 네트워크 규칙을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="184db-3586">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="184db-3587">Set-AzDataLakeStoreVirtualNetworkRule: 지정된 Data Lake Store 계정에 지정된 가상 네트워크 규칙을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="184db-3587">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="184db-3588">Remove-AzDataLakeStoreVirtualNetworkRule: Azure Data Lake Store 가상 네트워크 규칙을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="184db-3588">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="184db-3589">Az.Network</span><span class="sxs-lookup"><span data-stu-id="184db-3589">Az.Network</span></span>
* <span data-ttu-id="184db-3590">Test-AzNetworkWatcherConnectivity cmdlet을 업데이트하고, 백 엔드에 프로토콜 값을 전달합니다.</span><span class="sxs-lookup"><span data-stu-id="184db-3590">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="184db-3591">모든 cmdlet에 ResourceName 인수 완성자가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-3591">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="184db-3592">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="184db-3592">Az.Resources</span></span>
* <span data-ttu-id="184db-3593">(기본 프로필에 구독이 없고 범위가 지정되지 않은 경우) 시나리오에서 의미 있는 예외를 추가하여 Get-AzRoleDefinition이 인식할 수 없는 예외를 throw하는 문제를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="184db-3593">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="184db-3594">또한 기본 매개 변수 집합을 'RoleDefinitionNameParameterSet'으로 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="184db-3594">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="184db-3595">0.3.0 - 2018년 10월</span><span class="sxs-lookup"><span data-stu-id="184db-3595">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="184db-3596">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="184db-3596">Azure.Storage</span></span>
* <span data-ttu-id="184db-3597">대상에 메타데이터가 있을 때 Blob/파일이 메타 데이터를 복사하지 않는 문제 수정</span><span class="sxs-lookup"><span data-stu-id="184db-3597">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="184db-3598">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="184db-3598">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="184db-3599">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="184db-3599">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="184db-3600">특정 위치의 스토리지 리소스 사용을 지원하고 글로벌 스토리지 리소스 사용 가져오기는 더 이상 사용되지 않는다는 경고 메시지를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="184db-3600">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="184db-3601">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="184db-3601">Get-AzStorageUsage</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="184db-3602">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="184db-3602">Az.CognitiveServices</span></span>
* <span data-ttu-id="184db-3603">기존 계정이 없는 Get-AzCognitiveServicesAccountSkus를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="184db-3603">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="184db-3604">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="184db-3604">Az.Compute</span></span>
* <span data-ttu-id="184db-3605">Get-AzVM -ResourceGroupName <rg>가 필요한 경우 50개가 넘는 결과를 반환하도록 수정</span><span class="sxs-lookup"><span data-stu-id="184db-3605">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="184db-3606">'SimpleParameterSet' 예제가 New-AzVmss cmdlet 도움말에 추가됨</span><span class="sxs-lookup"><span data-stu-id="184db-3606">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="184db-3607">Azure Disk Encryption 진행률 메시지의 오타를 수정</span><span class="sxs-lookup"><span data-stu-id="184db-3607">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="184db-3608">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="184db-3608">Az.DataFactoryV2</span></span>
* <span data-ttu-id="184db-3609">ADF.Net SDK 버전을 2.3.0으로 업데이트</span><span class="sxs-lookup"><span data-stu-id="184db-3609">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="184db-3610">Az.Network</span><span class="sxs-lookup"><span data-stu-id="184db-3610">Az.Network</span></span>
* <span data-ttu-id="184db-3611">NetworkProfile 기능 추가</span><span class="sxs-lookup"><span data-stu-id="184db-3611">Added NetworkProfile functionality.</span></span> <span data-ttu-id="184db-3612">추가된 새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="184db-3612">new cmdlets added</span></span>
    - <span data-ttu-id="184db-3613">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="184db-3613">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="184db-3614">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="184db-3614">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="184db-3615">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="184db-3615">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="184db-3616">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="184db-3616">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="184db-3617">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="184db-3617">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="184db-3618">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="184db-3618">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="184db-3619">서브넷 모델에 서비스 연결 링크 추가</span><span class="sxs-lookup"><span data-stu-id="184db-3619">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="184db-3620">New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="184db-3620">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="184db-3621">Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="184db-3621">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="184db-3622">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="184db-3622">Az.RedisCache</span></span>
* <span data-ttu-id="184db-3623">모든 문자열을 Size 매개 변수로 진행되도록 허용</span><span class="sxs-lookup"><span data-stu-id="184db-3623">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="184db-3624">PSArgumentCompleter 팝업에 P5 추가</span><span class="sxs-lookup"><span data-stu-id="184db-3624">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="184db-3625">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="184db-3625">Az.Resources</span></span>
* <span data-ttu-id="184db-3626">-Mode 매개 변수를 Set-AzPolicyDefinition에 추가</span><span class="sxs-lookup"><span data-stu-id="184db-3626">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="184db-3627">사용자가 포함된 Origin 작업에서 Get-AzProviderOperation commandlet 버그 수정</span><span class="sxs-lookup"><span data-stu-id="184db-3627">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="184db-3628">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="184db-3628">Az.Sql</span></span>
* <span data-ttu-id="184db-3629">일부 백업 cmdlet이 현재 azure 구독을 인식하지 않는 문제 해결</span><span class="sxs-lookup"><span data-stu-id="184db-3629">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="184db-3630">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="184db-3630">Az.Websites</span></span>
* <span data-ttu-id="184db-3631">새 cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - 컨테이너 지속적인 배포 Webhook URL을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="184db-3631">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="184db-3632">새 cmdlet New-AzWebAppContainerPSSession 및 Enter-WebAppContainerPSSession -  windows 컨테이너 앱에 PowerShell 원격 세션을 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="184db-3632">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="184db-3633">0.2.0 - 2018년 9월</span><span class="sxs-lookup"><span data-stu-id="184db-3633">0.2.0 - September 2018</span></span>
 <span data-ttu-id="184db-3634">초기 릴리스</span><span class="sxs-lookup"><span data-stu-id="184db-3634">Initial Release</span></span>
