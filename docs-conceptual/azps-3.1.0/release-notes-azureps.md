---
title: Azure PowerShell 릴리스 정보
description: Azure PowerShell 모듈의 모든 최신 업데이트에 대해 알아봅니다.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 10/15/2019
ms.openlocfilehash: 2280b594ee9f525b2fa3175c917f6365cea354ba
ms.sourcegitcommit: 45e1823aa1a792840aa4829831b5f67a9d5d24a0
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2019
ms.locfileid: "74537118"
---
## <a name="310---november-2019"></a><span data-ttu-id="5b408-103">3.1.0 - 2019년 11월</span><span class="sxs-lookup"><span data-stu-id="5b408-103">3.1.0 - November 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="5b408-104">마지막 주 릴리스 이후의 주요 사항</span><span class="sxs-lookup"><span data-stu-id="5b408-104">Highlights since the last major release</span></span>
* <span data-ttu-id="5b408-105">Az.DataBoxEdge 1.0.0 릴리스됨</span><span class="sxs-lookup"><span data-stu-id="5b408-105">Az.DataBoxEdge 1.0.0 released</span></span>
* <span data-ttu-id="5b408-106">Az.SqlVirtualMachine 1.0.0 릴리스됨</span><span class="sxs-lookup"><span data-stu-id="5b408-106">Az.SqlVirtualMachine 1.0.0 released</span></span>

#### <a name="azcompute"></a><span data-ttu-id="5b408-107">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="5b408-107">Az.Compute</span></span>
* <span data-ttu-id="5b408-108">VM Reapply 기능</span><span class="sxs-lookup"><span data-stu-id="5b408-108">VM Reapply feature</span></span>
    - <span data-ttu-id="5b408-109">Set-AzVM cmdlet에 Reapply 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="5b408-109">Add Reapply parameter to Set-AzVM cmdlet</span></span>
* <span data-ttu-id="5b408-110">VM 확장 집합 AutomaticRepairs 기능:</span><span class="sxs-lookup"><span data-stu-id="5b408-110">VM Scale Set AutomaticRepairs feature:</span></span>
    - <span data-ttu-id="5b408-111">다음 cmdlet에 EnableAutomaticRepair, AutomaticRepairGracePeriod 및 AutomaticRepairMaxInstanceRepairsPercent 매개 변수를 추가합니다.   New-AzVmssConfig   Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="5b408-111">Add EnableAutomaticRepair, AutomaticRepairGracePeriod, and AutomaticRepairMaxInstanceRepairsPercent parameters to the following cmdlets:   New-AzVmssConfig   Update-AzVmss</span></span>
* <span data-ttu-id="5b408-112">New-AzVM에 대한 교차 테넌트 갤러리 이미지 지원</span><span class="sxs-lookup"><span data-stu-id="5b408-112">Cross tenant gallery image support for New-AzVM</span></span>
* <span data-ttu-id="5b408-113">New-AzVM, New-AzVMConfig 및 New-AzVmss cmdlet의 Priority 매개 변수의 인수 완성자에 'Spot' 추가</span><span class="sxs-lookup"><span data-stu-id="5b408-113">Add 'Spot' to the argument completer of Priority parameter in New-AzVM, New-AzVMConfig and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="5b408-114">Add-AzVmssDataDisk cmdlet에 DiskIOPSReadWrite 및 DiskMBpsReadWrite 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="5b408-114">Add DiskIOPSReadWrite and DiskMBpsReadWrite parameters to Add-AzVmssDataDisk cmdlet</span></span>
* <span data-ttu-id="5b408-115">New-AzGalleryImageVersion cmdlet의 SourceImageId 매개 변수를 선택 사항으로 변경</span><span class="sxs-lookup"><span data-stu-id="5b408-115">Change SourceImageId parameter of New-AzGalleryImageVersion cmdlet to optional</span></span>
* <span data-ttu-id="5b408-116">New-AzGalleryImageVersion cmdlet에 OSDiskImage 및 DataDiskImage 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="5b408-116">Add OSDiskImage and DataDiskImage parameters to New-AzGalleryImageVersion cmdlet</span></span>
* <span data-ttu-id="5b408-117">New-AzGalleryImageDefinition cmdlet에 HyperVGeneration 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="5b408-117">Add HyperVGeneration parameter to New-AzGalleryImageDefinition cmdlet</span></span>
* <span data-ttu-id="5b408-118">New-AzVmss, New-AzVmssConfig 및 Update-AzVmss cmdlet에 SkipExtensionsOnOverprovisionedVMs 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="5b408-118">Add SkipExtensionsOnOverprovisionedVMs parameters to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="5b408-119">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="5b408-119">Az.DataBoxEdge</span></span>
* <span data-ttu-id="5b408-120">cmdlet `Get-AzDataBoxEdgeOrder` 추가됨</span><span class="sxs-lookup"><span data-stu-id="5b408-120">Added cmdlet `Get-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="5b408-121">주문 가져오기</span><span class="sxs-lookup"><span data-stu-id="5b408-121">Get the Order</span></span>
* <span data-ttu-id="5b408-122">cmdlet `New-AzDataBoxEdgeOrder` 추가됨</span><span class="sxs-lookup"><span data-stu-id="5b408-122">Added cmdlet `New-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="5b408-123">새 주문 만들기</span><span class="sxs-lookup"><span data-stu-id="5b408-123">Create new Order</span></span>
* <span data-ttu-id="5b408-124">cmdlet `Remove-AzDataBoxEdgeOrder` 추가됨</span><span class="sxs-lookup"><span data-stu-id="5b408-124">Added cmdlet `Remove-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="5b408-125">주문 제거</span><span class="sxs-lookup"><span data-stu-id="5b408-125">Remove the Order</span></span>
* <span data-ttu-id="5b408-126">cmdlet `New-AzDataBoxEdgeShare` 변경</span><span class="sxs-lookup"><span data-stu-id="5b408-126">Change in cmdlet `New-AzDataBoxEdgeShare`</span></span>
    - <span data-ttu-id="5b408-127">이제 로컬 공유를 만듬</span><span class="sxs-lookup"><span data-stu-id="5b408-127">Now creates Local Share</span></span>
* <span data-ttu-id="5b408-128">cmdlet `Set-AzDataBoxEdgeRole` 추가됨</span><span class="sxs-lookup"><span data-stu-id="5b408-128">Added cmdlet `Set-AzDataBoxEdgeRole`</span></span>
    - <span data-ttu-id="5b408-129">이제 IotRole을 공유에 매핑할 수 있음</span><span class="sxs-lookup"><span data-stu-id="5b408-129">Now IotRole can be mapped to Share</span></span>
* <span data-ttu-id="5b408-130">cmdlet `Invoke-AzDataBoxEdgeDevice` 추가됨</span><span class="sxs-lookup"><span data-stu-id="5b408-130">Added cmdlet `Invoke-AzDataBoxEdgeDevice`</span></span>
    - <span data-ttu-id="5b408-131">스캔 업데이트 호출, 업데이트 다운로드, 디바이스에 업데이트 설치</span><span class="sxs-lookup"><span data-stu-id="5b408-131">Invoke scan update, download update, install updates on the device</span></span>
* <span data-ttu-id="5b408-132">cmdlet `Get-AzDataBoxEdgeTrigger` 추가됨</span><span class="sxs-lookup"><span data-stu-id="5b408-132">Added cmdlet `Get-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="5b408-133">트리거에 대한 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="5b408-133">Gets the information about Triggers</span></span>
* <span data-ttu-id="5b408-134">cmdlet `New-AzDataBoxEdgeTrigger` 추가됨</span><span class="sxs-lookup"><span data-stu-id="5b408-134">Added cmdlet `New-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="5b408-135">새 트리거 만들기</span><span class="sxs-lookup"><span data-stu-id="5b408-135">Create new Triggers</span></span>
* <span data-ttu-id="5b408-136">cmdlet `Remove-AzDataBoxEdgeTrigger` 추가됨</span><span class="sxs-lookup"><span data-stu-id="5b408-136">Added cmdlet `Remove-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="5b408-137">트리거 제거</span><span class="sxs-lookup"><span data-stu-id="5b408-137">Remove the Triggers</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="5b408-138">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="5b408-138">Az.DataFactory</span></span>
* <span data-ttu-id="5b408-139">ADF .Net SDK 버전을 4.4.0으로 업데이트</span><span class="sxs-lookup"><span data-stu-id="5b408-139">Update ADF .Net SDK version to 4.4.0</span></span>
* <span data-ttu-id="5b408-140">'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd에 'ExpressCustomSetup' 매개 변수를 추가하여 사용자 지정 설치 스크립트 없이 설치 구성 및 타사 구성 요소를 사용하도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-140">Add parameter 'ExpressCustomSetup' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable setup configurations and 3rd party components without custom setup script.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="5b408-141">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="5b408-141">Az.DataLakeStore</span></span>
* <span data-ttu-id="5b408-142">Get-AzDataLakeStoreDeletedItem 및 Restore-AzDataLakeStoreDeletedItem의 설명서 업데이트</span><span class="sxs-lookup"><span data-stu-id="5b408-142">Update documentation of Get-AzDataLakeStoreDeletedItem and Restore-AzDataLakeStoreDeletedItem</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="5b408-143">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="5b408-143">Az.EventHub</span></span>
* <span data-ttu-id="5b408-144">10301 문제 해결: SAS 토큰 날짜 형식 수정</span><span class="sxs-lookup"><span data-stu-id="5b408-144">Fix for issue 10301 : Fix the SAS Token date format</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="5b408-145">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="5b408-145">Az.FrontDoor</span></span>
* <span data-ttu-id="5b408-146">Enable-AzFrontDoorCustomDomainHttps 및 New-AzFrontDoorFrontendEndpointObject에 MinimumTlsVersion 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="5b408-146">Add MinimumTlsVersion parameter to Enable-AzFrontDoorCustomDomainHttps and New-AzFrontDoorFrontendEndpointObject</span></span>
* <span data-ttu-id="5b408-147">New-AzFrontDoorHealthProbeSettingObject에 HealthProbeMethod 및 EnabledState 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="5b408-147">Add HealthProbeMethod and EnabledState parameters to New-AzFrontDoorHealthProbeSettingObject</span></span>
* <span data-ttu-id="5b408-148">BackendPoolsSettings 개체를 생성하여 Front Door 생성/업데이트에 전달하는 새 cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="5b408-148">Add new cmdlet to create BackendPoolsSettings objec to pass into creation/update of Front Door</span></span>
    - <span data-ttu-id="5b408-149">New-AzFrontDoorBackendPoolsSettingObject</span><span class="sxs-lookup"><span data-stu-id="5b408-149">New-AzFrontDoorBackendPoolsSettingObject</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="5b408-150">Az.Network</span><span class="sxs-lookup"><span data-stu-id="5b408-150">Az.Network</span></span>
* <span data-ttu-id="5b408-151">'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' 및 'Start-AzVirtualnetworkGatewayPacketCapture.md' FilterData 옵션 예제를 변경합니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-151">Change 'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' and 'Start-AzVirtualnetworkGatewayPacketCapture.md' FilterData option examples.</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="5b408-152">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="5b408-152">Az.PrivateDns</span></span>
* <span data-ttu-id="5b408-153">PrivateDns .net sdk를 버전 1.0.0으로 업데이트함</span><span class="sxs-lookup"><span data-stu-id="5b408-153">Updated PrivateDns .net sdk to version 1.0.0</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="5b408-154">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="5b408-154">Az.RecoveryServices</span></span>
* <span data-ttu-id="5b408-155">보호를 사용하도록 설정할 때 디스크 유형을 선택하도록 Azure Site Recovery 지원</span><span class="sxs-lookup"><span data-stu-id="5b408-155">Azure Site Recovery support to select disk type at enabling protection.</span></span>
* <span data-ttu-id="5b408-156">복구 계획 동작 편집을 위한 Azure Site Recovery 버그 수정</span><span class="sxs-lookup"><span data-stu-id="5b408-156">Azure Site Recovery bug fix for recovery plan action edit.</span></span>
* <span data-ttu-id="5b408-157">파일 스트림 DB를 허용하도록 Azure Backup SQL 복원 지원</span><span class="sxs-lookup"><span data-stu-id="5b408-157">Azure Backup SQL Restore support to accept filestream DBs.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="5b408-158">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="5b408-158">Az.RedisCache</span></span>
* <span data-ttu-id="5b408-159">'New-AzRedisCache' 및 'Set-AzRedisCache' cmdlet에 'MinimumTlsVersion' 매개 변수가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-159">Added 'MinimumTlsVersion' parameter in 'New-AzRedisCache' and 'Set-AzRedisCache' cmdlets.</span></span> <span data-ttu-id="5b408-160">'Get-AzRedisCache' cmdlet 출력에 'MinimumTlsVersion'도 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-160">Also, added 'MinimumTlsVersion' in the output of 'Get-AzRedisCache' cmdlet.</span></span>
* <span data-ttu-id="5b408-161">'Set-AzRedisCache' 및 'New-AzRedisCache' cmdlet의 '-Size' 매개 변수에 대한 유효성 검사가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-161">Added validation on '-Size' parameter for 'Set-AzRedisCache' and 'New-AzRedisCache' cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="5b408-162">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="5b408-162">Az.Resources</span></span>
- <span data-ttu-id="5b408-163">정책 할당에 새로운 EnforcementMode 속성이 있는 새 api 버전 2019-06-01을 사용하도록 정책 cmdlet이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-163">Updated policy cmdlets to use new api version 2019-06-01 that has new EnforcementMode property in policy assignment.</span></span>
- <span data-ttu-id="5b408-164">정책 정의 만들기 도움말 예제가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-164">Updated create policy definition help example</span></span>
- <span data-ttu-id="5b408-165">Remove-AZADServicePrincipal -ServicePrincipalName 버그를 수정하고, 서비스 사용자 이름을 찾을 수 없으면 null 참조를 throw합니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-165">Fix bug Remove-AZADServicePrincipal -ServicePrincipalName, throw null reference when service principal name not found.</span></span>
- <span data-ttu-id="5b408-166">New-AZADServicePrincipal 버그를 수정하고, 테넌트에 구독이 없으면 null 참조를 throw합니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-166">Fix bug New-AZADServicePrincipal, throw null reference when tenant doesn't have any subscription.</span></span>
- <span data-ttu-id="5b408-167">연결된 애플리케이션에만 자격 증명을 추가하도록 New-AzAdServicePrincipal을 변경합니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-167">Change New-AzAdServicePrincipal to add credentials only to associated application.</span></span>

#### <a name="azsql"></a><span data-ttu-id="5b408-168">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="5b408-168">Az.Sql</span></span>
* <span data-ttu-id="5b408-169">데이터베이스 ReadReplicaCount에 대한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-169">Added support for database ReadReplicaCount.</span></span>
* <span data-ttu-id="5b408-170">영역 중복이 설정되지 않은 경우 Set-AzSqlDatabase가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-170">Fixed Set-AzSqlDatabase when zone redundancy not set</span></span>

## <a name="300---november-2019"></a><span data-ttu-id="5b408-171">3.0.0 - 2019년 11월</span><span class="sxs-lookup"><span data-stu-id="5b408-171">3.0.0 - November 2019</span></span>
### <a name="general"></a><span data-ttu-id="5b408-172">일반</span><span class="sxs-lookup"><span data-stu-id="5b408-172">General</span></span>
* <span data-ttu-id="5b408-173">Az.PrivateDns 1.0.0 릴리스</span><span class="sxs-lookup"><span data-stu-id="5b408-173">Az.PrivateDns 1.0.0 released</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="5b408-174">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="5b408-174">Az.Accounts</span></span>
* <span data-ttu-id="5b408-175">'Resolve-Error' 별칭에 사용 중단 메시지를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-175">Add a deprecation message for 'Resolve-Error' alias.</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="5b408-176">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="5b408-176">Az.Advisor</span></span>
* <span data-ttu-id="5b408-177">Get-AzAdvisorRecommendation cmdlet에 새로운 '운영 효율성' 범주가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-177">Added new category 'Operational Excellence' to Get-AzAdvisorRecommendation cmdlet.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="5b408-178">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="5b408-178">Az.Batch</span></span>
* <span data-ttu-id="5b408-179">`BatchAccountContext`의 `CoreQuota` 이름이 `DedicatedCoreQuota`로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-179">Renamed `CoreQuota` on `BatchAccountContext` to `DedicatedCoreQuota`.</span></span> <span data-ttu-id="5b408-180">또한 `LowPriorityCoreQuota`가 새로 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-180">There is also a new `LowPriorityCoreQuota`.</span></span>
  - <span data-ttu-id="5b408-181">이 변경 사항은 **Get-AzBatchAccount**에 영향을 줍니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-181">This impacts **Get-AzBatchAccount**.</span></span>
* <span data-ttu-id="5b408-182">이제 **New-AzBatchTask** `-ResourceFile` 매개 변수는 새로운 **New-AzBatchResourceFile** cmdlet을 사용하여 구성할 수 있는 `PSResourceFile` 개체의 컬렉션을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-182">**New-AzBatchTask** `-ResourceFile` parameter now takes a collection of `PSResourceFile` objects, which can be constructed using the new **New-AzBatchResourceFile** cmdlet.</span></span>
* <span data-ttu-id="5b408-183">새로운 **New-AzBatchResourceFile** cmdlet을 통해 `PSResourceFile` 개체를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-183">New **New-AzBatchResourceFile** cmdlet to help create `PSResourceFile` objects.</span></span> <span data-ttu-id="5b408-184">이들은 `-ResourceFile` 매개 변수의 **New-AzBatchTask**에 제공될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-184">These can be supplied to **New-AzBatchTask** on the `-ResourceFile` parameter.</span></span>
  - <span data-ttu-id="5b408-185">그에 따라 기존 `HttpUrl` 방법 외에도 두 가지 종류의 리소스 파일이 새롭게 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-185">This supports two new kinds of resource file in addition to the existing `HttpUrl` way:</span></span>
    - <span data-ttu-id="5b408-186">`AutoStorageContainerName` 기반 리소스 파일은 전체 자동 스토리지 컨테이너를 일괄 처리 노드에 다운로드합니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-186">`AutoStorageContainerName` based resource files download an entire auto-storage container to the Batch node.</span></span>
    - <span data-ttu-id="5b408-187">`StorageContainerUrl` 기반 리소스 파일은 URL에 지정된 컨테이너를 일괄 처리 노드에 다운로드합니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-187">`StorageContainerUrl` based resource files download the container specified in the URL to the Batch node.</span></span>
* <span data-ttu-id="5b408-188">**Get-AzBatchApplication**으로 반환되는 `PSApplication`의 `ApplicationPackages` 속성이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-188">Removed `ApplicationPackages` property of `PSApplication` returned by **Get-AzBatchApplication**.</span></span>
  - <span data-ttu-id="5b408-189">이제 **Get-AzBatchApplicationPackage**를 사용하여 애플리케이션 내부의 특정 패키지를 검색할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-189">The specific packages inside of an application now can be retrieved using **Get-AzBatchApplicationPackage**.</span></span> <span data-ttu-id="5b408-190">예: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`</span><span class="sxs-lookup"><span data-stu-id="5b408-190">For example: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span></span>
* <span data-ttu-id="5b408-191">**Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication** 및 **Set-AzBatchApplication**에서 `ApplicationId` 이름이 `ApplicationName`으로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-191">Renamed `ApplicationId` to `ApplicationName` on **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication**, and **Set-AzBatchApplication**.</span></span>
  - <span data-ttu-id="5b408-192">이제 `ApplicationId`는 `ApplicationName`의 별칭입니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-192">`ApplicationId` now is an alias of `ApplicationName`.</span></span>
* <span data-ttu-id="5b408-193">새로운 `PSWindowsUserConfiguration` 속성이 `PSUserAccount`에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-193">Added new `PSWindowsUserConfiguration` property to `PSUserAccount`.</span></span>
* <span data-ttu-id="5b408-194">`PSApplicationPackage`에서 `Version` 이름이 `Name`으로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-194">Renamed `Version` to `Name` on `PSApplicationPackage`.</span></span>
* <span data-ttu-id="5b408-195">`PSResourceFile`에서 `BlobSource` 이름이 `HttpUrl`로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-195">Renamed `BlobSource` to `HttpUrl` on `PSResourceFile`.</span></span>
* <span data-ttu-id="5b408-196">`PSVirtualMachineConfiguration`에서 `OSDisk` 속성이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-196">Removed `OSDisk` property from `PSVirtualMachineConfiguration`.</span></span>
* <span data-ttu-id="5b408-197">**Set-AzBatchPoolOSVersion**이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-197">Removed **Set-AzBatchPoolOSVersion**.</span></span> <span data-ttu-id="5b408-198">이 작업은 더 이상 지원되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-198">This operation is no longer supported.</span></span>
* <span data-ttu-id="5b408-199">`PSCloudServiceConfiguration`에서 `TargetOSVersion`이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-199">Removed `TargetOSVersion` from `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="5b408-200">`PSCloudServiceConfiguration`에서 `CurrentOSVersion` 이름이 `OSVersion`으로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-200">Renamed `CurrentOSVersion` to `OSVersion` on `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="5b408-201">`PSPoolUsageMetrics`에서 `DataEgressGiB` 및 `DataIngressGiB`가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-201">Removed `DataEgressGiB` and `DataIngressGiB` from `PSPoolUsageMetrics`.</span></span>
* <span data-ttu-id="5b408-202">**Get-AzBatchNodeAgentSku**가 제거되고 **Get-AzBatchSupportedImage**로 대체되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-202">Removed **Get-AzBatchNodeAgentSku** and replaced it with  **Get-AzBatchSupportedImage**.</span></span> 
  - <span data-ttu-id="5b408-203">**Get-AzBatchSupportedImage**가 **Get-AzBatchNodeAgentSku**와 동일한 데이터를 반환하지만 더 친숙한 형식이 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-203">**Get-AzBatchSupportedImage** returns the same data as **Get-AzBatchNodeAgentSku** but in a more friendly format.</span></span>
  - <span data-ttu-id="5b408-204">이제 확인되지 않은 이미지도 새롭게 반환됩니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-204">New non-verified images are also now returned.</span></span> <span data-ttu-id="5b408-205">각 이미지의 `Capabilities` 및 `BatchSupportEndOfLife`에 대한 추가 정보도 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-205">Additional information about `Capabilities` and `BatchSupportEndOfLife` for each image is also included.</span></span>
* <span data-ttu-id="5b408-206">**New-AzBatchPool**의 새로운 `MountConfiguration` 매개 변수를 통해 풀의 각 노드에서 원격 파일 시스템을 마운트할 수 있는 기능이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-206">Added ability to mount remote file-systems on each node of a pool via the new `MountConfiguration` parameter of **New-AzBatchPool**.</span></span>
* <span data-ttu-id="5b408-207">이제 트래픽의 소스 포트를 기준으로 풀에 대한 네트워크 액세스를 차단하는 네트워크 보안 규칙이 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-207">Now support network security rules blocking network access to a pool based on the source port of the traffic.</span></span> <span data-ttu-id="5b408-208">이 작업은 `PSNetworkSecurityGroupRule`에서 `SourcePortRanges` 속성을 통해 수행됩니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-208">This is done via the `SourcePortRanges` property on `PSNetworkSecurityGroupRule`.</span></span>
* <span data-ttu-id="5b408-209">컨테이너를 실행할 때 Batch는 이제 컨테이너 작업 디렉터리 또는 일괄 처리 태스크 작업 디렉터리에서 작업 실행을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-209">When running a container, Batch now supports executing the task in the container working directory or in the Batch task working directory.</span></span> <span data-ttu-id="5b408-210">이 작업은 `PSTaskContainerSettings`에서 `WorkingDirectory` 속성에 의해 제어됩니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-210">This is controlled by the `WorkingDirectory` property on `PSTaskContainerSettings`.</span></span>
* <span data-ttu-id="5b408-211">새로운 `PublicIPs` 속성을 통해 `PSNetworkConfiguration`에서 공용 IP의 컬렉션을 지정할 수 있는 기능이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-211">Added ability to specify a collection of public IPs on `PSNetworkConfiguration` via the new `PublicIPs` property.</span></span> <span data-ttu-id="5b408-212">그 결과 사용자 제공 IP 목록의 IP가 풀에 있는 노드에 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-212">This guarantees nodes in the Pool will have an IP from the list user provided IPs.</span></span>
* <span data-ttu-id="5b408-213">지정하지 않은 경우 이제 `PSSTartTask`에서 `WaitForSuccess`의 기본값은 `$True`입니다(이전에는 `$False`).</span><span class="sxs-lookup"><span data-stu-id="5b408-213">When not specified, the default value of `WaitForSuccess` on `PSSTartTask` is now `$True` (was `$False`).</span></span>
* <span data-ttu-id="5b408-214">지정하지 않은 경우 이제 `PSAutoUserSpecification`에서 `Scope`의 기본값은 `Pool`입니다(이전에는 Windows의 경우 `Task`, Linux의 경우에는 `Pool`).</span><span class="sxs-lookup"><span data-stu-id="5b408-214">When not specified, the default value of `Scope` on `PSAutoUserSpecification` is now `Pool` (was `Task` on Windows and `Pool` on Linux).</span></span>

#### <a name="azcdn"></a><span data-ttu-id="5b408-215">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="5b408-215">Az.Cdn</span></span>
* <span data-ttu-id="5b408-216">RulesEngine에 UrlRewriteAction 및 CacheKeyQueryStringAction이 도입되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-216">Introduced UrlRewriteAction and CacheKeyQueryStringAction to RulesEngine.</span></span>
* <span data-ttu-id="5b408-217">New-AzDeliveryRuleCondition cmdlet에서 'Selector' 입력 누락과 같은 여러 버그가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-217">Fixed several bugs like missing 'Selector' Input in New-AzDeliveryRuleCondition cmdlet.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="5b408-218">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="5b408-218">Az.Compute</span></span>
* <span data-ttu-id="5b408-219">디스크 암호화 집합 기능</span><span class="sxs-lookup"><span data-stu-id="5b408-219">Disk Encryption Set feature</span></span>
    - <span data-ttu-id="5b408-220">새 cmdlet:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="5b408-220">New cmdlets:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span></span>
    - <span data-ttu-id="5b408-221">DiskEncryptionSetId 매개 변수가 다음 cmdlet에 추가되었습니다. Set-AzImageOSDisk Set-AzVMOSDisk Set-AzVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="5b408-221">DiskEncryptionSetId parameter is added to the following cmdlets: Set-AzImageOSDisk Set-AzVMOSDisk Set-AzVmssStorageProfile</span></span>        
        <span data-ttu-id="5b408-222">Add-AzImageDataDisk New-AzVMDataDisk Set-AzVMDataDisk Add-AzVMDataDisk Add-AzVmssDataDisk Add-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="5b408-222">Add-AzImageDataDisk New-AzVMDataDisk Set-AzVMDataDisk Add-AzVMDataDisk Add-AzVmssDataDisk Add-AzVmssVMDataDisk</span></span>
    - <span data-ttu-id="5b408-223">DiskEncryptionSetId 및 EncryptionType 매개 변수가 다음 cmdlet에 추가되었습니다.   New-AzDiskConfig   New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="5b408-223">DiskEncryptionSetId and EncryptionType parameters are added to the following cmdlets:   New-AzDiskConfig   New-AzSnapshotConfig</span></span>
* <span data-ttu-id="5b408-224">New-AzVmssIPConfig에 PublicIPAddressVersion 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="5b408-224">Add PublicIPAddressVersion parameter to New-AzVmssIPConfig</span></span>
* <span data-ttu-id="5b408-225">사용자 지정 스크립트 확장의 FileUris를 공용 설정에서 보호된 설정으로 이동</span><span class="sxs-lookup"><span data-stu-id="5b408-225">Move FileUris of custom script extension from public setting to protected setting</span></span>
* <span data-ttu-id="5b408-226">New-AzVmss, New-AzVmssConfig 및 Update-AzVmss cmdlet에 ScaleInPolicy 추가</span><span class="sxs-lookup"><span data-stu-id="5b408-226">Add ScaleInPolicy to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>
* <span data-ttu-id="5b408-227">주요 변경 내용</span><span class="sxs-lookup"><span data-stu-id="5b408-227">Breaking changes</span></span>
    - <span data-ttu-id="5b408-228">CreateOption이 업로드일 때 UploadSizeInBytes 매개 변수가 New-AzDiskConfig에 대해 DiskSizeGB 대신 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-228">UploadSizeInBytes parameter is used instead of DiskSizeGB for New-AzDiskConfig when CreateOption is Upload</span></span>
    - <span data-ttu-id="5b408-229">GalleryImageVersion 개체에서 PublishingProfile.Source.ManagedImage.Id가 StorageProfile.Source.Id로 바뀝니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-229">PublishingProfile.Source.ManagedImage.Id is replaced with StorageProfile.Source.Id in GalleryImageVersion object</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="5b408-230">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="5b408-230">Az.DataFactory</span></span>
* <span data-ttu-id="5b408-231">ADF .Net SDK 버전을 4.3.0으로 업데이트</span><span class="sxs-lookup"><span data-stu-id="5b408-231">Update ADF .Net SDK version to 4.3.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="5b408-232">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="5b408-232">Az.DataLakeStore</span></span>
* <span data-ttu-id="5b408-233">ADLS SDK 버전 업데이트(https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha) , 다음 수정 사항 제공</span><span class="sxs-lookup"><span data-stu-id="5b408-233">Update ADLS SDK version (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), brings following fixes</span></span>
* <span data-ttu-id="5b408-234">휴지통 또는 디렉터리 항목의 creationtime을 역직렬화할 수 없을 때 예외가 발생하지 않도록 방지합니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-234">Avoid throwing exception while unable to deserialize the creationtime of the trash or directory entry.</span></span>
* <span data-ttu-id="5b408-235">adlsclient에서 요청별 시간 제한 설정 노출</span><span class="sxs-lookup"><span data-stu-id="5b408-235">Expose setting per request timeout in adlsclient</span></span>
* <span data-ttu-id="5b408-236">badoffset 복구를 위한 원본 syncflag 전달 수정</span><span class="sxs-lookup"><span data-stu-id="5b408-236">Fix passing the original syncflag for badoffset recovery</span></span>
* <span data-ttu-id="5b408-237">응답이 확인된 후 연속 토큰을 검색하기 위한 EnumerateDirectory 수정</span><span class="sxs-lookup"><span data-stu-id="5b408-237">Fix EnumerateDirectory to retrieve continuation token once response is checked</span></span>
* <span data-ttu-id="5b408-238">Concat 버그 수정</span><span class="sxs-lookup"><span data-stu-id="5b408-238">Fix Concat Bug</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="5b408-239">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="5b408-239">Az.FrontDoor</span></span>
* <span data-ttu-id="5b408-240">모듈 간 기타 오타가 수정됨</span><span class="sxs-lookup"><span data-stu-id="5b408-240">Fixed miscellaneous typos across module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="5b408-241">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="5b408-241">Az.HDInsight</span></span>
* <span data-ttu-id="5b408-242">ADLSGen1 스토리지가 포함된 클러스터를 가져오기 위해 Get-AzHDInsightCluster를 사용할 때 고객에게 '올바른 Base-64 문자열이 아닙니다' 오류가 표시되는 버그가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-242">Fixed the bug that customer will get 'Not a valid Base-64 string' error when using Get-AzHDInsightCluster to get the cluster with ADLSGen1 storage.</span></span>
* <span data-ttu-id="5b408-243">고객이 Azure Data Lake에 액세스하기 위해 서비스 주체 애플리케이션 ID를 제공할 수 있도록 세 가지 cmdlet Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig 및 New-AzHDInsightCluster에 이름이 'ApplicationId'인 매개 변수를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-243">Add a parameter named 'ApplicationId' to three cmdlets Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig and New-AzHDInsightCluster so that customer can provide the service principal application id for accessing Azure Data Lake.</span></span>
* <span data-ttu-id="5b408-244">Microsoft.Azure.Management.HDInsight가 2.1.0에서 5.1.0으로 변경됨</span><span class="sxs-lookup"><span data-stu-id="5b408-244">Changed Microsoft.Azure.Management.HDInsight from 2.1.0 to 5.1.0</span></span>
* <span data-ttu-id="5b408-245">다음 5가지 cmdlet이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-245">Removed five cmdlets:</span></span>
    - <span data-ttu-id="5b408-246">Get-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="5b408-246">Get-AzHDInsightOMS</span></span>
    - <span data-ttu-id="5b408-247">Enable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="5b408-247">Enable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="5b408-248">Disable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="5b408-248">Disable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="5b408-249">Grant-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="5b408-249">Grant-AzHDInsightRdpServicesAccess</span></span>
    - <span data-ttu-id="5b408-250">Revoke-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="5b408-250">Revoke-AzHDInsightRdpServicesAccess</span></span>
* <span data-ttu-id="5b408-251">다음 3가지 cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-251">Added three cmdlets:</span></span>
    - <span data-ttu-id="5b408-252">Get-AzHDInsightOMS 대신 Get-AzHDInsightMonitoring</span><span class="sxs-lookup"><span data-stu-id="5b408-252">Get-AzHDInsightMonitoring to replace Get-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="5b408-253">Get-AzHDInsightOMS 대신 Get-AzHDInsightMonitoring</span><span class="sxs-lookup"><span data-stu-id="5b408-253">Enable-AzHDInsightMonitoring to replace Enable-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="5b408-254">Disable-AzHDInsightOMS 대신 Disable-AzHDInsightMonitoring</span><span class="sxs-lookup"><span data-stu-id="5b408-254">Disable-AzHDInsightMonitoring to replace Disable-AzHDInsightOMS.</span></span>
* <span data-ttu-id="5b408-255">특정 위치의 기능 정보 가져오기를 지원하도록 cmdlet Get-AzHDInsightProperties가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-255">Fixed cmdlet Get-AzHDInsightProperties to support get capabilities information from a specific location.</span></span>
* <span data-ttu-id="5b408-256">Add-AzHDInsightConfigValue에서 매개 변수 집합('Spark1', 'Spark2')이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-256">Removed parameter sets('Spark1', 'Spark2') from Add-AzHDInsightConfigValue.</span></span>
* <span data-ttu-id="5b408-257">cmdlet Add-AzHDInsightSecurityProfile의 도움말 문서에 예제를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-257">Add examples to the help documents of cmdlet Add-AzHDInsightSecurityProfile.</span></span>
* <span data-ttu-id="5b408-258">다음 cmdlet의 출력 유형이 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-258">Changed output type of the following cmdlets:</span></span>
*  - <span data-ttu-id="5b408-259">Get-AzHDInsightProperties의 출력 유형이 CapabilitiesResponse에서 AzureHDInsightCapabilities로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-259">Changed the output type of Get-AzHDInsightProperties from  CapabilitiesResponse to AzureHDInsightCapabilities.</span></span>
*  - <span data-ttu-id="5b408-260">Remove-AzHDInsightCluster의 출력 유형이 ClusterGetResponse에서 bool로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-260">Changed the output type of Remove-AzHDInsightCluster from ClusterGetResponse to bool.</span></span>
*  - <span data-ttu-id="5b408-261">Set-AzHDInsightGatewaySettings의 출력 유형이 HttpConnectivitySettings에서 GatewaySettings로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-261">Changed the output type of Set-AzHDInsightGatewaySettings HttpConnectivitySettings to GatewaySettings.</span></span>
* <span data-ttu-id="5b408-262">몇 가지 시나리오 테스트 사례가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-262">Added some scenario test cases.</span></span>
* <span data-ttu-id="5b408-263">일부 별칭 제거: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span><span class="sxs-lookup"><span data-stu-id="5b408-263">Remove some alias: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="5b408-264">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="5b408-264">Az.IotHub</span></span>
* <span data-ttu-id="5b408-265">주요 변경 내용:</span><span class="sxs-lookup"><span data-stu-id="5b408-265">Breaking changes:</span></span>
    - <span data-ttu-id="5b408-266">'Add-AzIotHubEventHubConsumerGroup' cmdlet이 'EventHubEndpointName' 매개 변수를 더 이상 지원하지 않으며 원래 매개 변수 이름에 대해 별칭을 찾을 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-266">The cmdlet 'Add-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="5b408-267">'Add-AzIotHubEventHubConsumerGroup' cmdlet에 대한 매개 변수 집합 '__AllParameterSets'가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-267">The parameter set '__AllParameterSets' for cmdlet 'Add-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="5b408-268">'Get-AzIotHubEventHubConsumerGroup' cmdlet이 'EventHubEndpointName' 매개 변수를 더 이상 지원하지 않으며 원래 매개 변수 이름에 대해 별칭을 찾을 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-268">The cmdlet 'Get-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="5b408-269">'Get-AzIotHubEventHubConsumerGroup' cmdlet에 대한 매개 변수 집합 '__AllParameterSets'가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-269">The parameter set '__AllParameterSets' for cmdlet 'Get-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="5b408-270">'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' 유형의 'OperationsMonitoringProperties' 속성이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-270">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' has been removed.</span></span>
    - <span data-ttu-id="5b408-271">'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' 유형의 'OperationsMonitoringProperties' 속성이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-271">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' has been removed.</span></span>
    - <span data-ttu-id="5b408-272">'New-AzIotHubExportDevice' cmdlet이 더 이상 'New-AzIotHubExportDevices' 별칭을 지원하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-272">The cmdlet 'New-AzIotHubExportDevice' no longer supports the alias 'New-AzIotHubExportDevices'.</span></span>
    - <span data-ttu-id="5b408-273">'New-AzIotHubImportDevice' cmdlet이 더 이상 'New-AzIotHubImportDevices' 별칭을 지원하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-273">The cmdlet 'New-AzIotHubImportDevice' no longer supports the alias 'New-AzIotHubImportDevices'.</span></span>
    - <span data-ttu-id="5b408-274">'Remove-AzIotHubEventHubConsumerGroup' cmdlet이 'EventHubEndpointName' 매개 변수를 더 이상 지원하지 않으며 원래 매개 변수 이름에 대해 별칭을 찾을 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-274">The cmdlet 'Remove-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="5b408-275">'Remove-AzIotHubEventHubConsumerGroup' cmdlet에 대한 매개 변수 집합 '__AllParameterSets'가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-275">The parameter set '__AllParameterSets' for cmdlet 'Remove-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="5b408-276">'Set-AzIotHub' cmdlet이 'OperationsMonitoringProperties' 매개 변수를 더 이상 지원하지 않으며 원래 매개 변수 이름에 대해 별칭을 찾을 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-276">The cmdlet 'Set-AzIotHub' no longer supports the parameter 'OperationsMonitoringProperties' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="5b408-277">'Set-AzIotHub' cmdlet에 대한 매개 변수 집합 'UpdateOperationsMonitoringProperties'가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-277">The parameter set 'UpdateOperationsMonitoringProperties' for cmdlet 'Set-AzIotHub' has been removed.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="5b408-278">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="5b408-278">Az.RecoveryServices</span></span>
* <span data-ttu-id="5b408-279">Azure Site Recovery가 Azure-Azure를 위한 NSG, 공용 IP 및 내부 부하 분산 장치와 같은 네트워킹 리소스 구성을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-279">Azure Site Recovery support to configure networking resources like NSG, public IP and internal load balancers for Azure to Azure.</span></span>
* <span data-ttu-id="5b408-280">Azure Site Recovery가 vMWare-Azure를 위한 관리 디스크에 쓰기를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-280">Azure Site Recovery Support to write to managed disk for vMWare to Azure.</span></span>
* <span data-ttu-id="5b408-281">Azure Site Recovery가 vMWare-Azure를 위한 NIC 감소를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-281">Azure Site Recovery Support to NIC reduction for vMWare to Azure.</span></span>
* <span data-ttu-id="5b408-282">Azure Site Recovery가 Azure-Azure를 위한 가속 네트워킹을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-282">Azure Site Recovery Support to accelerated networking for Azure to Azure.</span></span>
* <span data-ttu-id="5b408-283">Azure Site Recovery가 Azure-Azure를 위한 에이전트 자동 업데이트를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-283">Azure Site Recovery Support to agent auto update for Azure to Azure.</span></span>
* <span data-ttu-id="5b408-284">Azure Site Recovery가 Azure-Azure를 위한 표준 SSD를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-284">Azure Site Recovery Support to Standard SSD for Azure to Azure.</span></span>
* <span data-ttu-id="5b408-285">Azure Site Recovery가 Azure-Azure를 위한 두 가지 Azure 디스크 암호화 전달을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-285">Azure Site Recovery Support to Azure Disk Encryption two pass for Azure to Azure.</span></span>
* <span data-ttu-id="5b408-286">Azure Site Recovery가 Azure-Azure를 위한 새로 추가된 디스크 보호를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-286">Azure Site Recovery Support to protect newly added disk for Azure to Azure.</span></span>
* <span data-ttu-id="5b408-287">VM을 위한 SoftDelete 기능 및 softdelete를 위한 테스트가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-287">Added SoftDelete feature for VM and added tests for softdelete</span></span>

#### <a name="azresources"></a><span data-ttu-id="5b408-288">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="5b408-288">Az.Resources</span></span>
* <span data-ttu-id="5b408-289">종속성 어셈블리 Microsoft.Extensions.Caching.Memory가 1.1.1에서 2.2로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-289">Update dependency assembly Microsoft.Extensions.Caching.Memory from 1.1.1 to 2.2</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="5b408-290">Az.Network</span><span class="sxs-lookup"><span data-stu-id="5b408-290">Az.Network</span></span>
* <span data-ttu-id="5b408-291">일반 서비스 공급자 지원을 위해 PrivateEndpointConnection에 대한 모든 cmdlet이 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-291">Change all cmdlets for PrivateEndpointConnection to support generic service provider.</span></span>
    - <span data-ttu-id="5b408-292">업데이트된 cmdlet:</span><span class="sxs-lookup"><span data-stu-id="5b408-292">Updated cmdlet:</span></span>
        - <span data-ttu-id="5b408-293">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="5b408-293">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="5b408-294">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="5b408-294">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="5b408-295">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="5b408-295">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="5b408-296">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="5b408-296">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="5b408-297">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="5b408-297">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="5b408-298">PrivateLinkResource에 대한 새 cmdlet이 추가되었고 일반 서비스 공급자도 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-298">Add new cmdlet for PrivateLinkResource and it also support generic service provider.</span></span>
    - <span data-ttu-id="5b408-299">새 cmdlet:</span><span class="sxs-lookup"><span data-stu-id="5b408-299">New cmdlet:</span></span>
        - <span data-ttu-id="5b408-300">Get-AzPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="5b408-300">Get-AzPrivateLinkResource</span></span>
* <span data-ttu-id="5b408-301">Proxy Protocol V2 기능에 대한 새 필드 및 매개 변수가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-301">Add new fields and parameter for the feature Proxy Protocol V2.</span></span>
    - <span data-ttu-id="5b408-302">PrivateLinkService에서 EnableProxyProtocol 속성 추가</span><span class="sxs-lookup"><span data-stu-id="5b408-302">Add property EnableProxyProtocol in PrivateLinkService</span></span>
    - <span data-ttu-id="5b408-303">PrivateEndpointConnection에서 LinkIdentifier 속성 추가</span><span class="sxs-lookup"><span data-stu-id="5b408-303">Add property LinkIdentifier in PrivateEndpointConnection</span></span>
    - <span data-ttu-id="5b408-304">새로운 선택적인 매개 변수인 EnableProxyProtocol을 추가하도록 New-AzPrivateLinkService가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-304">Updated New-AzPrivateLinkService to add a new optional parameter EnableProxyProtocol.</span></span>
* <span data-ttu-id="5b408-305">'New-AzApplicationGatewaySku' 참조 설명서의 잘못된 매개 변수 설명 수정</span><span class="sxs-lookup"><span data-stu-id="5b408-305">Fix incorrect parameter description in 'New-AzApplicationGatewaySku' reference documentation</span></span>
* <span data-ttu-id="5b408-306">Azure 방화벽 정책을 지원하는 새로운 cmdlet</span><span class="sxs-lookup"><span data-stu-id="5b408-306">New cmdlets to support the azure firewall policy</span></span>
* <span data-ttu-id="5b408-307">VirtualHub의 자식 리소스 RouteTables에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="5b408-307">Add support for child resource RouteTables of VirtualHub</span></span>
    - <span data-ttu-id="5b408-308">추가된 새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-308">New cmdlets added:</span></span>
        - <span data-ttu-id="5b408-309">Add-AzVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="5b408-309">Add-AzVirtualHubRoute</span></span>
        - <span data-ttu-id="5b408-310">Add-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="5b408-310">Add-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="5b408-311">Get-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="5b408-311">Get-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="5b408-312">Remove-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="5b408-312">Remove-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="5b408-313">Set-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="5b408-313">Set-AzVirtualHub</span></span>
* <span data-ttu-id="5b408-314">VirtualHub의 새로운 속성 Sku 및 VirtualWan의 VirtualWANType에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="5b408-314">Add support for new properties Sku of VirtualHub and VirtualWANType of VirtualWan</span></span>
    - <span data-ttu-id="5b408-315">선택적 매개 변수로 다음 cmdlet이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-315">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="5b408-316">New-AzVirtualHub: 추가된 매개 변수 Sku</span><span class="sxs-lookup"><span data-stu-id="5b408-316">New-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="5b408-317">Update-AzVirtualHub: 추가된 매개 변수 Sku</span><span class="sxs-lookup"><span data-stu-id="5b408-317">Update-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="5b408-318">New-AzVirtualWan: 추가된 매개 변수 VirtualWANType</span><span class="sxs-lookup"><span data-stu-id="5b408-318">New-AzVirtualWan : added parameter VirtualWANType</span></span>
        - <span data-ttu-id="5b408-319">Update-AzVirtualWan: 추가된 매개 변수 VirtualWANType</span><span class="sxs-lookup"><span data-stu-id="5b408-319">Update-AzVirtualWan : added parameter VirtualWANType</span></span>
* <span data-ttu-id="5b408-320">HubVnetConnection, VpnConnection 및 ExpressRouteConnection에 대한 EnableInternetSecurity 속성 지원 추가</span><span class="sxs-lookup"><span data-stu-id="5b408-320">Add support for EnableInternetSecurity property for HubVnetConnection, VpnConnection and ExpressRouteConnection</span></span>
    - <span data-ttu-id="5b408-321">추가된 새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-321">New cmdlets added:</span></span>
        - <span data-ttu-id="5b408-322">Update-AzureRmVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="5b408-322">Update-AzureRmVirtualHubVnetConnection</span></span>
    - <span data-ttu-id="5b408-323">선택적 매개 변수로 다음 cmdlet이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-323">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="5b408-324">New-AzureRmVirtualHubVnetConnection: 추가된 매개 변수 EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="5b408-324">New-AzureRmVirtualHubVnetConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="5b408-325">New-AzureRmVpnConnection: 추가된 매개 변수 EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="5b408-325">New-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="5b408-326">Update-AzureRmVpnConnection: 추가된 매개 변수 EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="5b408-326">Update-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="5b408-327">New-AzureRmExpressRouteConnection: 추가된 매개 변수 EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="5b408-327">New-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="5b408-328">Set-AzureRmExpressRouteConnection: 추가된 매개 변수 EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="5b408-328">Set-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
* <span data-ttu-id="5b408-329">TopLevel WebApplicationFirewall 정책 구성을 위한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="5b408-329">Add support for Configuring TopLevel WebApplicationFirewall Policy</span></span>
    - <span data-ttu-id="5b408-330">추가된 새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-330">New cmdlets added:</span></span>
        - <span data-ttu-id="5b408-331">New-AzApplicationGatewayFirewallPolicySetting</span><span class="sxs-lookup"><span data-stu-id="5b408-331">New-AzApplicationGatewayFirewallPolicySetting</span></span>
        - <span data-ttu-id="5b408-332">New-AzApplicationGatewayFirewallPolicyExclusion</span><span class="sxs-lookup"><span data-stu-id="5b408-332">New-AzApplicationGatewayFirewallPolicyExclusion</span></span>
        - <span data-ttu-id="5b408-333">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="5b408-333">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span></span>
        - <span data-ttu-id="5b408-334">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="5b408-334">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span></span>
        - <span data-ttu-id="5b408-335">New-AzApplicationGatewayFirewallPolicyManagedRule</span><span class="sxs-lookup"><span data-stu-id="5b408-335">New-AzApplicationGatewayFirewallPolicyManagedRule</span></span>
        - <span data-ttu-id="5b408-336">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="5b408-336">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span></span>
    - <span data-ttu-id="5b408-337">선택적 매개 변수로 다음 cmdlet이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-337">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="5b408-338">New-AzApplicationGatewayFirewallPolicy: 추가된 매개 변수 PolicySetting, ManagedRule</span><span class="sxs-lookup"><span data-stu-id="5b408-338">New-AzApplicationGatewayFirewallPolicy : added parameter PolicySetting, ManagedRule</span></span>
* <span data-ttu-id="5b408-339">CustomRule에서 Geo-Match 연산자를 위한 지원 추가됨</span><span class="sxs-lookup"><span data-stu-id="5b408-339">Added support for Geo-Match operator on CustomRule</span></span>
    - <span data-ttu-id="5b408-340">FirewallCondition에서 연산자에 GeoMatch 추가됨</span><span class="sxs-lookup"><span data-stu-id="5b408-340">Added GeoMatch to the operator on the FirewallCondition</span></span>
* <span data-ttu-id="5b408-341">perListener 및 perSite 방화벽 규칙에 대한 지원 추가됨</span><span class="sxs-lookup"><span data-stu-id="5b408-341">Added support for perListener and perSite Firewall policy</span></span>
    - <span data-ttu-id="5b408-342">선택적 매개 변수로 다음 cmdlet이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-342">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="5b408-343">New-AzApplicationGatewayHttpListener: 추가된 매개 변수 FirewallPolicy, FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="5b408-343">New-AzApplicationGatewayHttpListener : added parameter FirewallPolicy, FirewallPolicyId</span></span>
        - <span data-ttu-id="5b408-344">New-AzApplicationGatewayPathRuleConfig: 추가된 매개 변수 FirewallPolicy, FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="5b408-344">New-AzApplicationGatewayPathRuleConfig : added parameter FirewallPolicy, FirewallPolicyId</span></span>
* <span data-ttu-id="5b408-345">'PSBastion'에서 이름이 AzureBastionSubnet인 필수 서브넷의 수정은 대소문자를 구분하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-345">Fix required subnet with name AzureBastionSubnet in 'PSBastion' can be case insensitive</span></span>
* <span data-ttu-id="5b408-346">Azure Firewall을 위한 네트워크 규칙의 대상 FQDN 및 NAT 규칙의 번역된 FQDN 지원</span><span class="sxs-lookup"><span data-stu-id="5b408-346">Support for Destination FQDNs in Network Rules and Translated FQDN in NAT Rules for Azure Firewall</span></span>
* <span data-ttu-id="5b408-347">IpGroup의 최상위 리소스 RouteTables에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="5b408-347">Add support for top level resource RouteTables of IpGroup</span></span>
    - <span data-ttu-id="5b408-348">추가된 새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-348">New cmdlets added:</span></span>
        - <span data-ttu-id="5b408-349">New-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="5b408-349">New-AzIpGroup</span></span>
        - <span data-ttu-id="5b408-350">Remove-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="5b408-350">Remove-AzIpGroup</span></span>
        - <span data-ttu-id="5b408-351">Get-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="5b408-351">Get-AzIpGroup</span></span>
        - <span data-ttu-id="5b408-352">Set-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="5b408-352">Set-AzIpGroup</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="5b408-353">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="5b408-353">Az.ServiceFabric</span></span>
* <span data-ttu-id="5b408-354">Add-AzVmssSecret에서 지원되기 때문에 Add-AzServiceFabricApplicationCertificate cmdlet이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-354">Remove Add-AzServiceFabricApplicationCertificate cmdlet as this scenario is covered by Add-AzVmssSecret.</span></span>

#### <a name="azsql"></a><span data-ttu-id="5b408-355">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="5b408-355">Az.Sql</span></span>
* <span data-ttu-id="5b408-356">Managed Instances에서 삭제된 데이터베이스의 복원을 위한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-356">Added support for restore of dropped databases on Managed Instances.</span></span>
* <span data-ttu-id="5b408-357">이전의 감사 cmdlet 코드가 사용되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-357">Deprecated from code old auditing cmdlets.</span></span>
* <span data-ttu-id="5b408-358">사용되지 않는 별칭이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-358">Removed deprecated aliases:</span></span>
* <span data-ttu-id="5b408-359">Get-AzSqlDatabaseIndexRecommendations(대신 Get-AzSqlDatabaseIndexRecommendation 사용)</span><span class="sxs-lookup"><span data-stu-id="5b408-359">Get-AzSqlDatabaseIndexRecommendations (use Get-AzSqlDatabaseIndexRecommendation instead)</span></span>
* <span data-ttu-id="5b408-360">Get-AzSqlDatabaseRestorePoints(대신 Get-AzSqlDatabaseRestorePoint 사용)</span><span class="sxs-lookup"><span data-stu-id="5b408-360">Get-AzSqlDatabaseRestorePoints (use Get-AzSqlDatabaseRestorePoint instead)</span></span>
* <span data-ttu-id="5b408-361">Get-AzSqlDatabaseSecureConnectionPolicy cmdlet 제거</span><span class="sxs-lookup"><span data-stu-id="5b408-361">Remove Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="5b408-362">사용되지 않는 취약성 평가 설정 cmdlet에 대한 별칭 제거</span><span class="sxs-lookup"><span data-stu-id="5b408-362">Remove aliases for deprecated Vulnerability Assessment Settings cmdlets</span></span>
* <span data-ttu-id="5b408-363">지능형 위협 탐지 설정 cmdlet 사용 중단</span><span class="sxs-lookup"><span data-stu-id="5b408-363">Deprecate Advanced Threat Detection Settings cmdlets</span></span> 
* <span data-ttu-id="5b408-364">데이터베이스의 열에 대한 민감도 권장 사항의 사용 여부를 제어하는 cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-364">Adding cmdlets to Disable and enable sensitivity recommendations on columns in a database.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="5b408-365">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="5b408-365">Az.Storage</span></span>
* <span data-ttu-id="5b408-366">스토리지 계정을 만들거나 업데이트할 때 큰 파일 공유 사용 지원</span><span class="sxs-lookup"><span data-stu-id="5b408-366">Support enable Large File share when create or update Storage account</span></span>
    -  <span data-ttu-id="5b408-367">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="5b408-367">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="5b408-368">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="5b408-368">Set-AzStorageAccount</span></span>
* <span data-ttu-id="5b408-369">파일 핸들을 닫거나/가져올 때, DeletePending 상태의 개체로 인한 오류를 방지하기 위해 입력 경로가 파일 디렉터리인지 또는 파일인지를 확인하는 과정을 건너뜁니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-369">When close/get File handle, skip check the input path is File directory or File, to avoid failure with object in DeletePending status</span></span>
    -  <span data-ttu-id="5b408-370">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="5b408-370">Get-AzStorageFileHandle</span></span>
    -  <span data-ttu-id="5b408-371">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="5b408-371">Close-AzStorageFileHandle</span></span>
    
## <a name="280---october-2019"></a><span data-ttu-id="5b408-372">2.8.0 - 2019년 10월</span><span class="sxs-lookup"><span data-stu-id="5b408-372">2.8.0 - October 2019</span></span>
### <a name="general"></a><span data-ttu-id="5b408-373">일반</span><span class="sxs-lookup"><span data-stu-id="5b408-373">General</span></span>
* <span data-ttu-id="5b408-374">Az.HealthcareApis 1.0.0 릴리스</span><span class="sxs-lookup"><span data-stu-id="5b408-374">Az.HealthcareApis 1.0.0 release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="5b408-375">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="5b408-375">Az.Accounts</span></span>
* <span data-ttu-id="5b408-376">생성된 모듈에 대한 원격 분석 및 URL 다시 작성이 업데이트되고, Windows 단위 테스트가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-376">Update telemetry and url rewriting for generated modules, fix windows unit tests.</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="5b408-377">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="5b408-377">Az.ApiManagement</span></span>
* <span data-ttu-id="5b408-378">**Set-AzApiManagementApi** - API 업데이트 지원이 ApiVersionSet에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-378">**Set-AzApiManagementApi** - Added support for Updating Api into ApiVersionSet</span></span>
    - <span data-ttu-id="5b408-379">문제 https://github.com/Azure/azure-powershell/issues/10068 수정</span><span class="sxs-lookup"><span data-stu-id="5b408-379">Fix for issue https://github.com/Azure/azure-powershell/issues/10068</span></span>

#### <a name="azautomation"></a><span data-ttu-id="5b408-380">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="5b408-380">Az.Automation</span></span>
* <span data-ttu-id="5b408-381">Linux 다시 부팅 설정 매개 변수에 대한 New-AzureAutomationSoftwareUpdateConfiguration cmdlet이 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-381">Fixed New-AzureAutomationSoftwareUpdateConfiguration cmdlet for Linux reboot setting parameter.</span></span> 

#### <a name="azbatch"></a><span data-ttu-id="5b408-382">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="5b408-382">Az.Batch</span></span>
* <span data-ttu-id="5b408-383">**Get-AzBatchNodeAgentSku**가 더 이상 사용되지 않으며, 2.0.0 버전의 **Get-AzBatchSupportImage**로 대체되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-383">**Get-AzBatchNodeAgentSku** is deprecated and will be replaced by **Get-AzBatchSupportImage** in version 2.0.0.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="5b408-384">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="5b408-384">Az.Compute</span></span>
* <span data-ttu-id="5b408-385">Priority, EvictionPolicy 및 MaxPrice 매개 변수가 New-AzVM 및 New-AzVmss cmdlet에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-385">Add Priority, EvictionPolicy, and MaxPrice parameters to New-AzVM and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="5b408-386">Add-AzVMAdditionalUnattendContent 및 Add-AzVMSshPublicKey cmdlet에 대한 경고 메시지와 도움말 문서가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-386">Fix warning message and help document for Add-AzVMAdditionalUnattendContent and Add-AzVMSshPublicKey cmdlets</span></span>
* <span data-ttu-id="5b408-387">Set-AzVMDiskEncryptionExtension의 관리 디스크가 있는 Linux VM에 대한 -skipVmBackup 예외가 해결되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-387">Fix -skipVmBackup exception for Linux VMs with managed disks for Set-AzVMDiskEncryptionExtension.</span></span> 
* <span data-ttu-id="5b408-388">Set-AzVMDiskEncryptionExtension의 두 가지 패스 시나리오에서 발생하는 암호화 설정 업데이트의 버그가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-388">Fix bug in update encryption settings in Set-AzVMDiskEncryptionExtension, two pass scenario.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="5b408-389">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="5b408-389">Az.DataFactory</span></span>
* <span data-ttu-id="5b408-390">ADF V2 데이터 흐름에 대한 CRUD 명령으로 Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow 및 Get-AzDataFactoryV2DataFlow가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-390">Adding CRUD commands for ADF V2 data flow: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow, and Get-AzDataFactoryV2DataFlow.</span></span>
* <span data-ttu-id="5b408-391">ADF V2 데이터 흐름 디버그 세션에 대한 작업 명령으로 Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand 및 Stop-AzDataFactoryV2DataFlowDebugSession이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-391">Adding action commands for ADF V2 data flow debug Session: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand and Stop-AzDataFactoryV2DataFlowDebugSession.</span></span>
* <span data-ttu-id="5b408-392">ADF .Net SDK 버전이 4.2.0으로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-392">Update ADF .Net SDK version to 4.2.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="5b408-393">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="5b408-393">Az.DataLakeStore</span></span>
* <span data-ttu-id="5b408-394">도메인 없이 '-'가 있는 계정을 전달할 수 있도록 계정 유효성 검사가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-394">Fix account validation so that accounts with '-' can be passed without domain</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="5b408-395">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="5b408-395">Az.HealthcareApis</span></span>
* <span data-ttu-id="5b408-396">PowerShell 버전이 1.0.0으로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-396">Updated the powershell version to 1.0.0</span></span>
* <span data-ttu-id="5b408-397">SDK 버전이 1.0.2로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-397">Updated the SDK version to 1.0.2</span></span>
* <span data-ttu-id="5b408-398">새 SDK 버전을 참조하도록 테스트가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-398">Update in tests to refer to new SDK version</span></span>
* <span data-ttu-id="5b408-399">출력이 중첩 구조에서 평면화 구조로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-399">Updated the output structure from nested to flattened.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="5b408-400">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="5b408-400">Az.IotHub</span></span>
* <span data-ttu-id="5b408-401">새 라우팅 원본 추가: DigitalTwinChangeEvents</span><span class="sxs-lookup"><span data-stu-id="5b408-401">Add new routing source: DigitalTwinChangeEvents</span></span>
* <span data-ttu-id="5b408-402">사소한 버그 수정: Get-AzIothub에서 subscriptionId를 반환하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-402">Minor bug fix: Get-AzIothub not returning subscriptionId</span></span> 

#### <a name="azmonitor"></a><span data-ttu-id="5b408-403">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="5b408-403">Az.Monitor</span></span>
* <span data-ttu-id="5b408-404">작업 그룹에 대한 새 작업 그룹 수신기로 -ItsmReceiver, -VoiceReceiver, -ArmRoleReceiver, -AzureFunctionReceiver, -LogicAppReceiver, -AutomationRunbookReceiver, -AzureAppPushReceiver가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-404">New action group receivers added for action group   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span></span>
* <span data-ttu-id="5b408-405">수신기에 사용하도록 설정된 일반 경고 스키마가 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-405">Use common alert schema enabled for the receivers.</span></span> <span data-ttu-id="5b408-406">SMS, Azure 앱 푸시, ITSM 및 음성 수신기에는 적용되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-406">This is not applicable for SMS, Azure App push , ITSM and Voice recievers</span></span>
* <span data-ttu-id="5b408-407">웹후크에서 이제 Azure Active Directory 인증을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-407">Webhooks now supports Azure active directory authentication .</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="5b408-408">Az.Network</span><span class="sxs-lookup"><span data-stu-id="5b408-408">Az.Network</span></span>
* <span data-ttu-id="5b408-409">서비스 엔드포인트 정책에 사용할 수 있는 별칭을 가져오기 위해 호출할 수 있는 새 Get-AzAvailableServiceAlias cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-409">Add new cmdlet Get-AzAvailableServiceAlias which can be called to get the aliases that can be used for Service Endpoint Policies.</span></span>
* <span data-ttu-id="5b408-410">트래픽 선택기를 Virtual Network 게이트웨이 연결에 추가할 수 있는 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-410">Added support for the adding traffic selectors to Virtual Network Gateway Connections</span></span>
    - <span data-ttu-id="5b408-411">추가된 새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-411">New cmdlets added:</span></span>
        - <span data-ttu-id="5b408-412">New-AzureRmTrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="5b408-412">New-AzureRmTrafficSelectorPolicy</span></span>
    - <span data-ttu-id="5b408-413">cmdlet이 선택적인 -TrafficSelectorPolicies, -New-AzureRmVirtualNetworkGatewayConnection, -Set-AzureRmVirtualNetworkGatewayConnection 매개 변수로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-413">Cmdlets updated with optional parameter -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="5b408-414">ESP 및 AH 프로토콜 지원이 네트워크 보안 규칙 구성에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-414">Add support for ESP and AH protocols in network security rule configurations</span></span>
    - <span data-ttu-id="5b408-415">다음 Cmdlet이 업데이트 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-415">Updated cmdlets:</span></span>
        - <span data-ttu-id="5b408-416">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="5b408-416">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="5b408-417">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="5b408-417">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="5b408-418">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="5b408-418">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="5b408-419">Cortex cmdlet의 예외 처리가 향상되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-419">Improve handling of exceptions in Cortex cmdlets</span></span>
* <span data-ttu-id="5b408-420">새 VirtualNetworkGateways 세대 및 SKU</span><span class="sxs-lookup"><span data-stu-id="5b408-420">New Generations and SKUs for VirtualNetworkGateways</span></span>
  - <span data-ttu-id="5b408-421">새 VirtualNetworkGateways 세대가 도입되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-421">Introduce new Generations for VirtualNetworkGateways.</span></span>
  - <span data-ttu-id="5b408-422">높은 처리량의 새 VirtualNetworkGateways SKU가 도입되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-422">Introduce new high throughput SKUs for VirtualNetworkGateways.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="5b408-423">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="5b408-423">Az.RedisCache</span></span>
* <span data-ttu-id="5b408-424">'-Size' 매개 변수에 대한 누락 값을 포함하도록 'Set-AzRedisCache' 참조 설명서가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-424">Updated 'Set-AzRedisCache' reference documentation to include missing values for '-Size' parameter</span></span>

#### <a name="azsql"></a><span data-ttu-id="5b408-425">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="5b408-425">Az.Sql</span></span>
* <span data-ttu-id="5b408-426">Managed Instance에서 Active Directory 관리자를 설정할 수 있는 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-426">Add support for setting Active Directory Administrator on Managed Instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="5b408-427">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="5b408-427">Az.Storage</span></span>
* <span data-ttu-id="5b408-428">스토리지 클라이언트 라이브러리가 11.1.0으로 업그레이드되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-428">Upgrade Storage Client Library to 11.1.0</span></span>
* <span data-ttu-id="5b408-429">관리 평면 API를 사용하여 컨테이너를 나열하면 NextPageLink를 통해 나열됩니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-429">List containers with Management plane API, will list with NextPageLink</span></span>
    -  <span data-ttu-id="5b408-430">Get-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="5b408-430">Get-AzRmStorageContainer</span></span>
* <span data-ttu-id="5b408-431">구독에서 스토리지 계정을 나열하면 NextPageLink를 통해 나열됩니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-431">List Storage accounts from subscription, will list with NextPageLink</span></span>
    -  <span data-ttu-id="5b408-432">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="5b408-432">Get-AzStorageAccount</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="5b408-433">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="5b408-433">Az.StorageSync</span></span>
* <span data-ttu-id="5b408-434">Reset-AzStorageSyncServerCertificate의 9810 문제가 해결되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-434">Fix Issue 9810 in Reset-AzStorageSyncServerCertificate.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="5b408-435">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="5b408-435">Az.Websites</span></span>
* <span data-ttu-id="5b408-436">앱의 ASP를 업데이트하는 Set-AzWebApp이 실패했습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-436">Set-AzWebApp updating ASP of an app was failing</span></span>

## <a name="270---september-2019"></a><span data-ttu-id="5b408-437">2.7.0 - 2019년 9월</span><span class="sxs-lookup"><span data-stu-id="5b408-437">2.7.0 - September 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="5b408-438">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="5b408-438">Az.ApiManagement</span></span>
* <span data-ttu-id="5b408-439">'Set-AzApiManagementPolicy' 참조 설명서에서 '-Format' 매개 변수 설명이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-439">Update '-Format' parameter description in 'Set-AzApiManagementPolicy' reference documentation</span></span>
* <span data-ttu-id="5b408-440">참조 설명서에서 사용되지 않는 cmdlet 'Update-AzApiManagementDeployment'의 참조를 제거했습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-440">Removed references of deprecated cmdlet 'Update-AzApiManagementDeployment' from reference documentation.</span></span> <span data-ttu-id="5b408-441">그 대신 'Set-AzApiManagement'를 사용하세요.</span><span class="sxs-lookup"><span data-stu-id="5b408-441">Use 'Set-AzApiManagement' instead.</span></span>

#### <a name="azautomation"></a><span data-ttu-id="5b408-442">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="5b408-442">Az.Automation</span></span>
* <span data-ttu-id="5b408-443">'Register-AzAutomationDscNode'에 대한 참조 설명서의 예제 오타가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-443">Fixed example typo in reference documentation for 'Register-AzAutomationDscNode'</span></span>
* <span data-ttu-id="5b408-444">Register-AzAutomationDSCNode에 OS 제한에 대한 설명이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-444">Added clarification on OS restriction to Register-AzAutomationDSCNode</span></span>
* <span data-ttu-id="5b408-445">-Wait 옵션에 대한 Start-AzAutomationRunbook cmdlet Null 참조 예외가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-445">Fixed Start-AzAutomationRunbook cmdlet Null reference exception for -Wait option.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="5b408-446">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="5b408-446">Az.Compute</span></span>
* <span data-ttu-id="5b408-447">New-AzDiskConfig에 UploadSizeInBytes 매개 변수가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-447">Add UploadSizeInBytes parameter tp New-AzDiskConfig</span></span>
* <span data-ttu-id="5b408-448">New-AzSnapshotConfig에 증분 매개 변수가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-448">Add Incremental parameter to New-AzSnapshotConfig</span></span>
* <span data-ttu-id="5b408-449">다음과 같은 낮은 우선 순위의 가상 머신 기능이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-449">Add a low priority virtual machine feature:</span></span>
    - <span data-ttu-id="5b408-450">MaxPrice, EvictionPolicy 및 Priority 매개 변수가 New-AzVMConfig에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-450">MaxPrice, EvictionPolicy and Priority parameters are added to New-AzVMConfig.</span></span>
    - <span data-ttu-id="5b408-451">MaxPrice 매개 변수는 New-AzVmssConfig, Update-AzVM 및 Update-AzVmss cmdlet에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-451">MaxPrice parameter is added to New-AzVmssConfig, Update-AzVM and Update-AzVmss cmdlets.</span></span>
* <span data-ttu-id="5b408-452">구독의 모든 가용성 세트를 나열할 때 발생하는 Get-AzAvailabilitySet cmdlet에 대한 VM 참조 이슈가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-452">Fix VM reference issue for Get-AzAvailabilitySet cmdlet when it lists all availability sets in the subscription.</span></span>
* <span data-ttu-id="5b408-453">Get-AzRemoteDesktopFile에 대한 null 예외가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-453">Fix the null exception for Get-AzRemoteDesktopFile.</span></span>
* <span data-ttu-id="5b408-454">종료 상대 위치에 대한 VHD 검색 메서드가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-454">Fix VHD Seek method for end-relative position.</span></span>
* <span data-ttu-id="5b408-455">New-AzVM 및 Update-AzVM에 대한 UltraSSD 이슈가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-455">Fix UltraSSD issue for New-AzVM and Update-AzVM.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="5b408-456">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="5b408-456">Az.DataFactory</span></span>
* <span data-ttu-id="5b408-457">ADF V2에 대한 3가지 새 명령 Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription 및 Get-AzDataFactoryV2TriggerSubscriptionStatus가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-457">Adding 3 new commands for ADF V2 - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription, and Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>
* <span data-ttu-id="5b408-458">ADF .Net SDK 버전이 4.1.3으로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-458">Updated ADF .Net SDK version to 4.1.3</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="5b408-459">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="5b408-459">Az.HDInsight</span></span>
* <span data-ttu-id="5b408-460">호출 주요 변경 내용</span><span class="sxs-lookup"><span data-stu-id="5b408-460">Call out breaking changes</span></span>

#### <a name="aziothub"></a><span data-ttu-id="5b408-461">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="5b408-461">Az.IotHub</span></span>
* <span data-ttu-id="5b408-462">지역 쌍 재해 복구 지역에 IotHub에 대한 장애 조치(failover) 호출 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-462">Add support to invoke failover for an IotHub to the geo-paired disaster recovery region.</span></span>
* <span data-ttu-id="5b408-463">IotHub에 대한 메시지 보강 관리 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-463">Add support to manage message enrichment for an IotHub.</span></span> <span data-ttu-id="5b408-464">새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-464">New cmdlets are:</span></span>
    - <span data-ttu-id="5b408-465">Add-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="5b408-465">Add-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="5b408-466">Get-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="5b408-466">Get-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="5b408-467">Remove-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="5b408-467">Remove-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="5b408-468">Set-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="5b408-468">Set-AzIotHubMessageEnrichment</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="5b408-469">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="5b408-469">Az.Monitor</span></span>
* <span data-ttu-id="5b408-470">최신 모니터링 SDK, 즉, 0.24.1-preview를 가리킵니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-470">Pointing to the most recent Monitor SDK, i.e. 0.24.1-preview</span></span>
   - <span data-ttu-id="5b408-471">메트릭 cmdlet에 줄 바꿈하지 않는 변경 내용을 추가합니다. 즉, 단위 열거형은 여러 새 값을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-471">Adds non-braking changes to the Metrics cmdlets, i.e. the Unit enumeration supports several new values.</span></span> <span data-ttu-id="5b408-472">이러한 cmdlet은 읽기 전용이므로 cmdlet 입력이 변경되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-472">These are read-only cmdlets, so there would be no change in the input of the cmdlets.</span></span>
   - <span data-ttu-id="5b408-473">이제 **ActionGroups** 요청의 api 버전은 **2019-06-01**이고, 이전에는 **2018-03-01**였습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-473">The api-version of the **ActionGroups** requests is now **2019-06-01**, before it was **2018-03-01**.</span></span> <span data-ttu-id="5b408-474">시나리오 테스트가 이 변경 내용에 맞게 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-474">The scenario tests have been updated to accommodate for this change.</span></span>
   - <span data-ttu-id="5b408-475">**EmailReceiver** 및 **WebhookReceiver** 클래스에 대한 생성자가 새 필수 인수, 즉, **useCommonAlertSchema**라는 부울 값을 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-475">The constructors for the classes **EmailReceiver** and **WebhookReceiver** added one new mandatory argument, i.e. a Boolean value called **useCommonAlertSchema**.</span></span> <span data-ttu-id="5b408-476">현재 이 값은 cmdlet의 주요 변경 사항을 숨기도록 **false**로 고정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-476">Currently, the value is fixed to **false** to hide this breaking change from the cmdlets.</span></span> <span data-ttu-id="5b408-477">**참고**: 이 변경 사항은 경고 팀에서 유효성을 검사해야 하는 임시 변경 내용입니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-477">**NOTE**: this is a temporary change that must be validated by the Alerts team.</span></span>
   - <span data-ttu-id="5b408-478">이전 SDK에서 변경된 **Source** 클래스(**ScheduledQueryRuleSource** 클래스와 관련됨)의 생성자에 대한 인수 순서입니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-478">The order of the arguments for the constructor of the class **Source** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="5b408-479">이번 변화로 인해 두 개의 단위 테스트를 수정해야 했습니다. 즉, 두 단위 테스트가 컴파일되었지만 테스트를 통과하지 못했습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-479">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
   - <span data-ttu-id="5b408-480">이전 SDK에서 변경된 **AlertingAction** 클래스(**ScheduledQueryRuleSource** 클래스와 관련됨)의 생성자에 대한 인수 순서입니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-480">The order of the arguments for the constructor of the class **AlertingAction** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="5b408-481">이번 변화로 인해 두 개의 단위 테스트를 수정해야 했습니다. 즉, 두 단위 테스트가 컴파일되었지만 테스트를 통과하지 못했습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-481">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
* <span data-ttu-id="5b408-482">메트릭 경고 V2에 대한 동적 임계값 기준 지원</span><span class="sxs-lookup"><span data-stu-id="5b408-482">Support Dynamic Threshold criteria for metric alert V2</span></span>
    - <span data-ttu-id="5b408-483">AzMetricAlertRuleV2Criteria: 이제 동적 임계값 조건도 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-483">New-AzMetricAlertRuleV2Criteria: now creats dynamic threshold criteria also</span></span>
    - <span data-ttu-id="5b408-484">Add-AzMetricAlertRuleV2: 이제 동적 임계값 조건도 수락합니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-484">Add-AzMetricAlertRuleV2: now accept dynamic threshold criteria also</span></span>
* <span data-ttu-id="5b408-485">SQR(예약된 쿼리 규칙)의 향상된 기능</span><span class="sxs-lookup"><span data-stu-id="5b408-485">Improvements in Scheduled Query Rule cmdlets (SQR)</span></span>
 - <span data-ttu-id="5b408-486">Cmdlet이 'Location' 매개 변수를 두 가지 형식(eastus 같은 위치 또는 미국 동부 같은 위치 표시 이름)으로 모두 허용합니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-486">Cmdlets will accept 'Location' paramater in both formats, either the location (e.g. eastus) or the location display name (e.g. East US)</span></span>
 - <span data-ttu-id="5b408-487">도움말 파일에 적절하게 표시된 'Enabled' 매개 변수</span><span class="sxs-lookup"><span data-stu-id="5b408-487">Illustrated 'Enabled' parameter in help files properly</span></span>
 - <span data-ttu-id="5b408-488">선택적 매개 변수 'ActionGroup'에 대한 예제가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-488">Added examples for 'ActionGroup' optional parameter</span></span>
 - <span data-ttu-id="5b408-489">도움말 파일이 전체적으로 개선되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-489">Overall improved help files</span></span>
* <span data-ttu-id="5b408-490">'Set-AzActionRule'의 범위 유형 결정 버그를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-490">Fix bug in determining scope type for 'Set-AzActionRule'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="5b408-491">Az.Network</span><span class="sxs-lookup"><span data-stu-id="5b408-491">Az.Network</span></span>
* <span data-ttu-id="5b408-492">'New-AzApplicationGateway' 참조 설명서의 잘못된 예제가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-492">Fix incorrect example in 'New-AzApplicationGateway' reference documentation</span></span> 
* <span data-ttu-id="5b408-493">'Get-AzNetworkWatcherPacketCapture' 참조 설명서에 패킷 캡처를 위한 모든 속성 검색과 관련된 메모가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-493">Add note in 'Get-AzNetworkWatcherPacketCapture' reference documentation about retrieving all properties for a packet capture</span></span>
* <span data-ttu-id="5b408-494">NIC를 올바르게 열거하도록 'Test-AzNetworkWatcherIPFlow' 참조 설명서의 예제가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-494">Fixed example in 'Test-AzNetworkWatcherIPFlow' reference documentation to correctly enumerate NICs</span></span>
* <span data-ttu-id="5b408-495">추가 세부 정보가 있는 경우 추가 세부 정보를 표시하도록 클라우드 예외 구문 분석이 향상되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-495">Improved cloud exception parsing to display additional details if they are present</span></span>
* <span data-ttu-id="5b408-496">더 많은 형식의 SDK 예외를 처리하도록 클라우드 예외 구문 분석이 향상되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-496">Improved cloud exception parsing to handle additional type of SDK exception</span></span>
* <span data-ttu-id="5b408-497">보안 규칙 모델의 잘못된 매핑이 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-497">Fixed incorrect mapping of Security Rule models</span></span>
* <span data-ttu-id="5b408-498">네트워크 인터페이스에 개인 IP 기능을 위한 속성이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-498">Added properties to network interface for private ip feature</span></span>
    - <span data-ttu-id="5b408-499">PSNetworkInterface에 'PrivateEndpoint' 속성이 PSResourceId 형식으로 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-499">Added property 'PrivateEndpoint' as type of PSResourceId to PSNetworkInterface</span></span>
    - <span data-ttu-id="5b408-500">PSNetworkInterfaceIPConfiguration에 'PrivateLinkConnectionProperties' 속성이 PSIpConfigurationConnectivityInformation 형식으로 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-500">Added property 'PrivateLinkConnectionProperties' as type of PSIpConfigurationConnectivityInformation to PSNetworkInterfaceIPConfiguration</span></span>
    - <span data-ttu-id="5b408-501">새 모델 클래스 PSIpConfigurationConnectivityInformation이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-501">Added new model class PSIpConfigurationConnectivityInformation</span></span>
* <span data-ttu-id="5b408-502">Azure Firewall 리소스에 대한 새 ApplicationRuleProtocolType 'mssql'이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-502">Added new ApplicationRuleProtocolType 'mssql' for Azure Firewall resource</span></span>
* <span data-ttu-id="5b408-503">Virtual WAN에서 멀티 링크를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-503">MultiLink support in Virtual WAN</span></span>
    - <span data-ttu-id="5b408-504">새 cmdlet</span><span class="sxs-lookup"><span data-stu-id="5b408-504">New cmdlets</span></span>
        - <span data-ttu-id="5b408-505">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="5b408-505">New-AzVpnSiteLink</span></span>
        - <span data-ttu-id="5b408-506">New-AzVpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="5b408-506">New-AzVpnSiteLinkConnection</span></span>
    - <span data-ttu-id="5b408-507">업데이트된 cmdlet:</span><span class="sxs-lookup"><span data-stu-id="5b408-507">Updated cmdlet:</span></span>
        - <span data-ttu-id="5b408-508">New-VpnSite</span><span class="sxs-lookup"><span data-stu-id="5b408-508">New-VpnSite</span></span>
        - <span data-ttu-id="5b408-509">Update-VpnSite</span><span class="sxs-lookup"><span data-stu-id="5b408-509">Update-VpnSite</span></span>
        - <span data-ttu-id="5b408-510">New-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="5b408-510">New-VpnConnection</span></span>
        - <span data-ttu-id="5b408-511">Update-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="5b408-511">Update-VpnConnection</span></span>
* <span data-ttu-id="5b408-512">AzureRM cmdlet 대신 Az cmdlet을 사용하도록 일부 PowerShell 예제의 문서가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-512">Fixed documents for some PowerShell examples to use Az cmdlets instead of AzureRM cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="5b408-513">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="5b408-513">Az.RecoveryServices</span></span>
* <span data-ttu-id="5b408-514">AzureVMpolicy 개체가 ProtectedItemsCount 특성으로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-514">Update AzureVMpolicy Object with ProtectedItemsCount Attribute</span></span>
* <span data-ttu-id="5b408-515">VM 정책 및 원래 스토리지 계정 복원에 대한 테스트가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-515">Added Tests for VM policy and Original Storage Account Restore</span></span>

#### <a name="azresources"></a><span data-ttu-id="5b408-516">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="5b408-516">Az.Resources</span></span>
* <span data-ttu-id="5b408-517">매개 변수 범위 없이 AzRoleAssignment를 호출할 수 없는 버그가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-517">Fix bug where New-AzRoleAssignment could not be called without parameter Scope.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="5b408-518">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="5b408-518">Az.ServiceFabric</span></span>
* <span data-ttu-id="5b408-519">'AzServiceFabricReliability' 참조 설명서에 대한 예제의 오타가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-519">Fixed typo in example for 'Update-AzServiceFabricReliability' reference documentation</span></span>
* <span data-ttu-id="5b408-520">애플리케이션 및 서비스를 관리하는 다음과 같은 새 cmdlet이 추가됩니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-520">Adding new cmdlets to manage appliaction and services:</span></span>
    - <span data-ttu-id="5b408-521">New-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="5b408-521">New-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="5b408-522">New-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="5b408-522">New-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="5b408-523">New-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="5b408-523">New-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="5b408-524">New-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="5b408-524">New-AzServiceFabricService</span></span>
    - <span data-ttu-id="5b408-525">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="5b408-525">Update-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="5b408-526">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="5b408-526">Get-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="5b408-527">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="5b408-527">Get-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="5b408-528">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="5b408-528">Get-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="5b408-529">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="5b408-529">Get-AzServiceFabricService</span></span>
    - <span data-ttu-id="5b408-530">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="5b408-530">Remove-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="5b408-531">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="5b408-531">Remove-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="5b408-532">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="5b408-532">Remove-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="5b408-533">Remove-AzServiceFabricServic</span><span class="sxs-lookup"><span data-stu-id="5b408-533">Remove-AzServiceFabricServic</span></span>
* <span data-ttu-id="5b408-534">Service Fabric SDK가 Service Fabric 리소스 공급자 api 버전 2019-03-01을 사용하는 1.2.0 버전으로 업그레이드되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-534">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2019-03-01.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="5b408-535">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="5b408-535">Az.SignalR</span></span>
* <span data-ttu-id="5b408-536">Update, Restart, CheckNameAvailability, GetUsage Cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-536">Add Update, Restart, CheckNameAvailability, GetUsage Cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="5b408-537">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="5b408-537">Az.Sql</span></span>
* <span data-ttu-id="5b408-538">'Get-AzSqlElasticPool'에 대한 참조 설명서의 예제가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-538">Update example in reference documentation for 'Get-AzSqlElasticPool'</span></span>
* <span data-ttu-id="5b408-539">탄력적 풀을 만드는 vCore 예제가 추가되었습니다(AzSqlElasticPool).</span><span class="sxs-lookup"><span data-stu-id="5b408-539">Added vCore example to creating an elastic pool (New-AzSqlElasticPool).</span></span>
* <span data-ttu-id="5b408-540">Set-AzSqlServerAdvancedThreatProtectionPolicy 및 Set-AzSqlDatabaseAdvancedThreatProtectionPolicy에서 EmailAddresses가 비어 있는 경우 EmailAddresses의 유효성을 검사하고 EmailAdmins가 false가 아닌지 확인하는 기능이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-540">Remove the validation of EmailAddresses and the check that EmailAdmins is not false in case EmailAddresses is empty in Set-AzSqlServerAdvancedThreatProtectionPolicy and Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="5b408-541">감사 범주를 사용하는 여러 진단 설정이 있는 경우 서버/데이터베이스 감사 설정을 제거하도록 설정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-541">Enabled removal of server/database auditing settings when multiple diagnostic settings that enable audit category exist.</span></span>
* <span data-ttu-id="5b408-542">여러 Sql 취약성 평가 cmdlet에서 이메일 주소 유효성 검사가 수정되었습니다(Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting 및 Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span><span class="sxs-lookup"><span data-stu-id="5b408-542">Fix email addresses validation in multiple Sql Vulnerability Assessment cmdlets (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting and Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span></span>

#### <a name="azstorage"></a><span data-ttu-id="5b408-543">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="5b408-543">Az.Storage</span></span>
* <span data-ttu-id="5b408-544">'Get-AzStorageAccountKey'에 대한 참조 설명서의 예제가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-544">Updated example in reference documentation for 'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="5b408-545">Azure 파일 업로드/다운에서, 원본 파일 SMB 속성(파일 특성, 파일 생성 시간, 파일을 마지막으로 쓴 시간)을 대상 파일에 보존하는 기능이 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-545">In upload/Downalod Azure File,support perserve the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the destination file</span></span>
    -  <span data-ttu-id="5b408-546">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="5b408-546">Set-AzStorageFileContent</span></span>
    -  <span data-ttu-id="5b408-547">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="5b408-547">Get-AzStorageFileContent</span></span>
* <span data-ttu-id="5b408-548">컨테이너가 사용되는 ImmutabilityPolicy에서 properties/metadate fail을 사용하여 블록 Blob 업로드가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-548">Fix Upload block blob with properties/metadate fail on container enabled ImmutabilityPolicy.</span></span>
    -  <span data-ttu-id="5b408-549">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="5b408-549">Set-AzStorageBlobContent</span></span>
* <span data-ttu-id="5b408-550">관리 평면 API를 사용하여 Azure 파일 공유 관리를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-550">Support manage Azure File shares with Management plane API</span></span>
    -  <span data-ttu-id="5b408-551">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="5b408-551">New-AzRmStorageShare</span></span>
    -  <span data-ttu-id="5b408-552">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="5b408-552">Get-AzRmStorageShare</span></span>
    -  <span data-ttu-id="5b408-553">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="5b408-553">Update-AzRmStorageShare</span></span>
    -  <span data-ttu-id="5b408-554">Remove-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="5b408-554">Remove-AzRmStorageShare</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="5b408-555">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="5b408-555">Az.Websites</span></span>
* <span data-ttu-id="5b408-556">앱을 새 ASP로 마이그레이션할 때 웹앱 태그가 삭제되는 이슈가 해결되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-556">Fixing issue where webapp Tags were getting deleted when migrating App to new ASPwhere webapp Tags were getting deleted when migrating App to new ASP</span></span>
* <span data-ttu-id="5b408-557">Linux와 Windows에서 모두 작동하도록 Publish-AzureWebapp이 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-557">Fixing the Publish-AzureWebapp to work across Linux and windows</span></span>
* <span data-ttu-id="5b408-558">'Get-AzWebAppPublishingProfile' 참조 설명서의 예제가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-558">Update example in 'Get-AzWebAppPublishingProfile' reference documentation</span></span>

## <a name="260---august-2019"></a><span data-ttu-id="5b408-559">2.6.0 - 2019년 8월</span><span class="sxs-lookup"><span data-stu-id="5b408-559">2.6.0 - August 2019</span></span>
#### <a name="general"></a><span data-ttu-id="5b408-560">일반</span><span class="sxs-lookup"><span data-stu-id="5b408-560">General</span></span>
* <span data-ttu-id="5b408-561">여러 모듈에서 기타 오타가 수정됨</span><span class="sxs-lookup"><span data-stu-id="5b408-561">Fixed miscellaneous typos across numerous modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="5b408-562">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="5b408-562">Az.Accounts</span></span>
* <span data-ttu-id="5b408-563">Azure Functions 인증에서 사용자가 할당한 MSI가 지원됨(# 9479)</span><span class="sxs-lookup"><span data-stu-id="5b408-563">Support user-assigned MSI in Azure Functiosn Authentication (#9479)</span></span>

#### <a name="azaks"></a><span data-ttu-id="5b408-564">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="5b408-564">Az.Aks</span></span>
* <span data-ttu-id="5b408-565">'Get-AzAks' 출력 관련 문제가 해결됨</span><span class="sxs-lookup"><span data-stu-id="5b408-565">Fix issue with output for 'Get-AzAks'</span></span>
    * <span data-ttu-id="5b408-566">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/9847 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5b408-566">More information here: https://github.com/Azure/azure-powershell/issues/9847</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="5b408-567">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="5b408-567">Az.ApiManagement</span></span>
* <span data-ttu-id="5b408-568">문제 https://github.com/Azure/azure-powershell/issues/9351 수정</span><span class="sxs-lookup"><span data-stu-id="5b408-568">Fix for issue https://github.com/Azure/azure-powershell/issues/9351</span></span>
    - <span data-ttu-id="5b408-569">productId, apiId, groupId 및 userId에 대한 제한을 적용하지 않는 .Net NuGet 버전이 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="5b408-569">Update .net nuget version, which does not enforce restrictions on productId, apiId, groupId and userId</span></span>
* <span data-ttu-id="5b408-570">**Get-AzApiManagementProduct** - API를 사용하는 제품에 대한 쿼리 지원이 추가됨</span><span class="sxs-lookup"><span data-stu-id="5b408-570">**Get-AzApiManagementProduct** - Added support for querying products using Api.</span></span>
  https://github.com/Azure/azure-powershell/issues/9482
* <span data-ttu-id="5b408-571">**New-AzApiManagementApiRevision** - 새 API 수정(https://github.com/Azure/azure-powershell/issues/9752 )을 만들 때 ApiRevisionDescription이 설정되지 않은 문제가 해결됨</span><span class="sxs-lookup"><span data-stu-id="5b408-571">**New-AzApiManagementApiRevision** - Fix for issue where ApiRevisionDescription was not being set when creating new api revision https://github.com/Azure/azure-powershell/issues/9752</span></span>
* <span data-ttu-id="5b408-572">'PsApiManagementOAuth2AuthrozationServer' 모델의 오타가 'PsApiManagementOAuth2AuthorizationServer'로 수정됨</span><span class="sxs-lookup"><span data-stu-id="5b408-572">Fixed typo in model 'PsApiManagementOAuth2AuthrozationServer' to 'PsApiManagementOAuth2AuthorizationServer'</span></span>

#### <a name="azbatch"></a><span data-ttu-id="5b408-573">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="5b408-573">Az.Batch</span></span>
* <span data-ttu-id="5b408-574">도움말 메시지 및 설명서에서 Windows를 대문자로 시작하도록 오타가 수정됨</span><span class="sxs-lookup"><span data-stu-id="5b408-574">Fixed typo in help message and documentation to capitalize Windows</span></span>

#### <a name="azcdn"></a><span data-ttu-id="5b408-575">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="5b408-575">Az.Cdn</span></span>
* <span data-ttu-id="5b408-576">CDN 모듈 변환 도우미의 오타가 수정됨</span><span class="sxs-lookup"><span data-stu-id="5b408-576">Fixed a typo in CDN module conversion helper</span></span>

#### <a name="azcompute"></a><span data-ttu-id="5b408-577">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="5b408-577">Az.Compute</span></span>
* <span data-ttu-id="5b408-578">VmssId가 New-AzVMConfig cmdlet에 추가됨</span><span class="sxs-lookup"><span data-stu-id="5b408-578">Add VmssId to New-AzVMConfig cmdlet</span></span>
* <span data-ttu-id="5b408-579">TerminateScheduledEvents 및 TerminateScheduledEventNotBeforeTimeoutInMinutes 매개 변수가 New-AzVmssConfig 및 Update-AzVmss에 추가됨</span><span class="sxs-lookup"><span data-stu-id="5b408-579">Add TerminateScheduledEvents and TerminateScheduledEventNotBeforeTimeoutInMinutes parameters to New-AzVmssConfig and Update-AzVmss</span></span>
* <span data-ttu-id="5b408-580">HyperVGeneration 속성이 VM 이미지 개체에 추가됨</span><span class="sxs-lookup"><span data-stu-id="5b408-580">Add HyperVGeneration property to VM image object</span></span>
* <span data-ttu-id="5b408-581">Host 및 HostGroup 기능이 추가됨</span><span class="sxs-lookup"><span data-stu-id="5b408-581">Add Host and HostGroup features</span></span>
    - <span data-ttu-id="5b408-582">새 cmdlet:   New-AzHostGroup, New-AzHost, Get-AzHostGroup, Get-AzHost, Remove-AzHostGroup, Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="5b408-582">New cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span></span>
    - <span data-ttu-id="5b408-583">HostId 매개 변수가 New-AzVMConfig 및 New-AzVM 추가됨</span><span class="sxs-lookup"><span data-stu-id="5b408-583">HostId parameter is added to New-AzVMConfig and New-AzVM</span></span>
* <span data-ttu-id="5b408-584">'Invoke-AzVMRunCommand' 설명서의 예제에서 올바른 매개 변수 이름을 사용하도록 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="5b408-584">Update example in 'Invoke-AzVMRunCommand' documentation to use correct parameter name</span></span>
* <span data-ttu-id="5b408-585">'Set-AzVMDiskEncryptionExtension' 및 'Set-AzVmssDiskEncryptionExtension' 참조 설명서의 '-VolumeType' 설명이 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="5b408-585">Update '-VolumeType' description in 'Set-AzVMDiskEncryptionExtension' and 'Set-AzVmssDiskEncryptionExtension' reference documentation</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="5b408-586">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="5b408-586">Az.DataFactory</span></span>
* <span data-ttu-id="5b408-587">'New-AzDataFactoryEncryptValue' 설명서에서 'Windows'를 대문자로 시작하도록 오타가 수정됨</span><span class="sxs-lookup"><span data-stu-id="5b408-587">Fix typo to capitalize 'Windows' in 'New-AzDataFactoryEncryptValue' documentation</span></span>
* <span data-ttu-id="5b408-588">ADF .Net SDK 버전이 4.1.2로 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="5b408-588">Updated ADF .Net SDK version to 4.1.2</span></span>
* <span data-ttu-id="5b408-589">자체 호스팅 통합 런타임을 SSIS Integration Runtime의 프록시로 설정할 수 있도록 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' 및 'DataProxyStagingPath' 매개 변수가 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd에 추가됨</span><span class="sxs-lookup"><span data-stu-id="5b408-589">Add parameter 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' and 'DataProxyStagingPath' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable set up Self-Hosted Integration Runtime as a proxy for SSIS Integration Runtime</span></span>
* <span data-ttu-id="5b408-590">PSTriggerRun에서 트리거된 파이프라인, 메시지 및 속성을 표시하고, PSActivityRun에서 작업 유형을 표시하도록 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="5b408-590">Updated PSTriggerRun to show the triggered pipelines, message and properties, and PSActivityRun to show the activity type</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="5b408-591">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="5b408-591">Az.DataLakeStore</span></span>
* <span data-ttu-id="5b408-592">오류 또는 원격 예외에 대한 Get-DataLakeStoreDeletedItem 중단이 수정됨</span><span class="sxs-lookup"><span data-stu-id="5b408-592">Fix hanging of Get-DataLakeStoreDeletedItem for any errors or remote exceptions.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="5b408-593">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="5b408-593">Az.EventHub</span></span>
* <span data-ttu-id="5b408-594">#9658 문제 해결: Set-AzEventHubNetworkRuleSet의 VirtualNteworkRule 매개 변수에 대한 오타</span><span class="sxs-lookup"><span data-stu-id="5b408-594">Fix for issue #9658 : Typo VirtualNteworkRule parameter in Set-AzEventHubNetworkRuleSet</span></span>
* <span data-ttu-id="5b408-595">#9558 문제 해결: Set-AzEventHubNamespace에서 PUT 대신 PATCH가 사용됨</span><span class="sxs-lookup"><span data-stu-id="5b408-595">Fix for issue #9558 : Set-AzEventHubNamespace is using PATCH instead of PUT</span></span>
* <span data-ttu-id="5b408-596">EnableKafka 매개 변수가 Set-AzEventHubNamespace cmdlet에 추가됨</span><span class="sxs-lookup"><span data-stu-id="5b408-596">added EnableKafka parameter to Set-AzEventHubNamespace cmdlet</span></span>
* <span data-ttu-id="5b408-597">#9786 문제 해결: Listen(수신 대기) 전용 권한이 있는 규칙을 만들 수 없음</span><span class="sxs-lookup"><span data-stu-id="5b408-597">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>

#### <a name="azmarketplaceordering"></a><span data-ttu-id="5b408-598">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="5b408-598">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="5b408-599">'Azure'가 모두 소문자인 설명서의 오타가 수정됨</span><span class="sxs-lookup"><span data-stu-id="5b408-599">Fixed documentation typo where 'Azure' was all lowercase letters</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="5b408-600">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="5b408-600">Az.Monitor</span></span>
* <span data-ttu-id="5b408-601">도움말 설명서에서 잘못된 매개 변수 이름이 수정됨</span><span class="sxs-lookup"><span data-stu-id="5b408-601">Fixed incorrect parameter name in help documentation</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="5b408-602">Az.Network</span><span class="sxs-lookup"><span data-stu-id="5b408-602">Az.Network</span></span>
* <span data-ttu-id="5b408-603">New-AzPrivateLinkServiceIpConfig가 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="5b408-603">Updated New-AzPrivateLinkServiceIpConfig</span></span>
    - <span data-ttu-id="5b408-604">서버 쪽에서 사용되지 않으므로 'PublicIpAddress' 매개 변수가 사용되지 않음</span><span class="sxs-lookup"><span data-stu-id="5b408-604">Deprecated the paramster 'PublicIpAddress' since this is never used in the server side.</span></span>
    - <span data-ttu-id="5b408-605">현재 IP 구성이 기본 구성인지 여부를 나타내는 하나의 선택적 'Primary' 매개 변수가 추가됨</span><span class="sxs-lookup"><span data-stu-id="5b408-605">Added one optional parameter 'Primary' that indicate the current ip configuration is primary one or not.</span></span>
* <span data-ttu-id="5b408-606">SDK의 요청 오류 예외 처리가 향상됨 - 이전의 SDK 예외가 올바르게 처리되지 않아 주요 오류 세부 정보가 표시되지 않은 문제가 해결됨</span><span class="sxs-lookup"><span data-stu-id="5b408-606">Improved handling of request error exception from SDK   -Fixes the issue that previously SDK exceptions aren't handled correctly which results in key error details not being displayed</span></span>
* <span data-ttu-id="5b408-607">올바른 IPv6 접두사 길이를 확인하기 위해 Ipv6 IP 접두사에 대한 유효성 검사 논리가 조정됨</span><span class="sxs-lookup"><span data-stu-id="5b408-607">Adjusted validation logic for Ipv6 IP Prefix to check for correct IPv6 prefix length.</span></span> 
* <span data-ttu-id="5b408-608">Get-AzVirtualNetworkSubnetConfig가 업데이트됨: 서브넷 리소스 ID별로 가져오도록 설정되는 매개 변수 세트가 추가됨</span><span class="sxs-lookup"><span data-stu-id="5b408-608">Updated Get-AzVirtualNetworkSubnetConfig: Added parameter set to get by subnet resource id.</span></span>
* <span data-ttu-id="5b408-609">AzNetworkServiceTag의 Location(위치) 매개 변수에 대한 설명이 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="5b408-609">Updated description of Location parameter for AzNetworkServiceTag</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="5b408-610">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="5b408-610">Az.OperationalInsights</span></span>
* <span data-ttu-id="5b408-611">'New-AzOperationalInsightsLinuxSyslogDataSource'에 대한 설명서가 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="5b408-611">Updated documentation for 'New-AzOperationalInsightsLinuxSyslogDataSource'</span></span>
    - <span data-ttu-id="5b408-612">예제가 추가됨</span><span class="sxs-lookup"><span data-stu-id="5b408-612">Added example</span></span>
    - <span data-ttu-id="5b408-613">'-Name' 매개 변수에 대한 설명이 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="5b408-613">Updated description for '-Name' parameter</span></span>
* <span data-ttu-id="5b408-614">New-AzOperationalInsightsWindowsEventDataSource에 대한 예제가 추가됨</span><span class="sxs-lookup"><span data-stu-id="5b408-614">Added an example for New-AzOperationalInsightsWindowsEventDataSource</span></span>
* <span data-ttu-id="5b408-615">New-AzOperationalInsightsWindowsEventDataSource의 -Name 매개 변수에 대한 설명이 변경됨</span><span class="sxs-lookup"><span data-stu-id="5b408-615">Changed the description of the -Name parameter for New-AzOperationalInsightsWindowsEventDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="5b408-616">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="5b408-616">Az.RecoveryServices</span></span>
* <span data-ttu-id="5b408-617">'Get-AzRecoveryServicesBackupJobDetail.md'가 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="5b408-617">Update 'Get-AzRecoveryServicesBackupJobDetail.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="5b408-618">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="5b408-618">Az.Resources</span></span>
* <span data-ttu-id="5b408-619">Microsoft 리소스에 대한 새 2019-05-10 API 버전 지원이 추가됨</span><span class="sxs-lookup"><span data-stu-id="5b408-619">Add support for new api version 2019-05-10 for Microsoft.Resource</span></span>
    - <span data-ttu-id="5b408-620">변수, 리소스 및 속성에 대한 'copy.count = 0' 지원이 추가됨</span><span class="sxs-lookup"><span data-stu-id="5b408-620">Add support for 'copy.count = 0' for variables, resources and properties</span></span>
    - <span data-ttu-id="5b408-621">'condition = false' 또는 'copy.count = 0'인 리소스가 완료 모드에서 삭제됨</span><span class="sxs-lookup"><span data-stu-id="5b408-621">Resources with 'condition = false' or 'copy.count = 0' will be deleted in complete mode</span></span>
* <span data-ttu-id="5b408-622">정책을 구독 수준에서 도움말 문서에 할당하는 예제가 추가됨</span><span class="sxs-lookup"><span data-stu-id="5b408-622">Add an example of assigning policy at subscription level to help doc</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="5b408-623">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="5b408-623">Az.ServiceBus</span></span>
* <span data-ttu-id="5b408-624">#9658 문제 해결: Set-AzServiceBusNetworkRuleSet의 VirtualNetworkRule 매개 변수에 대한 오타</span><span class="sxs-lookup"><span data-stu-id="5b408-624">Fix for issue #9658 : Typo VirtualNetworkRule parameter in Set-AzServiceBusNetworkRuleSet</span></span>
* <span data-ttu-id="5b408-625">#9786 문제 해결: Listen(수신 대기) 전용 권한이 있는 규칙을 만들 수 없음</span><span class="sxs-lookup"><span data-stu-id="5b408-625">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>
* <span data-ttu-id="5b408-626">큐 및 토픽에 대한 이름 가용성을 확인하는 새 'Test-AzServiceBusNameAvailability' 명령이 추가됨</span><span class="sxs-lookup"><span data-stu-id="5b408-626">Added new command 'Test-AzServiceBusNameAvailability' to check the name availability for queue and topic</span></span> 

#### <a name="azservicefabric"></a><span data-ttu-id="5b408-627">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="5b408-627">Az.ServiceFabric</span></span>
* <span data-ttu-id="5b408-628">노드 유형 추가 cmdlet 버그 수정:</span><span class="sxs-lookup"><span data-stu-id="5b408-628">Fix add node type cmdlet bugs:</span></span>
    - <span data-ttu-id="5b408-629">서비스 패브릭 클러스터와 관련이 없는 다른 vmss가 리소스 그룹에 있을 때 발생하는 NullReferenceException 버그</span><span class="sxs-lookup"><span data-stu-id="5b408-629">NullReferenceException bug when resource group had other vmss not related to the service fabric cluster.</span></span> <span data-ttu-id="5b408-630">문제 해결: https://github.com/Azure/azure-powershell/issues/8681</span><span class="sxs-lookup"><span data-stu-id="5b408-630">Fixes issue: https://github.com/Azure/azure-powershell/issues/8681</span></span>
    - <span data-ttu-id="5b408-631">virtualNetwork가 클러스터의 다른 리소스 그룹에 있을 때 cmdlet이 실패하는 버그가 수정됨</span><span class="sxs-lookup"><span data-stu-id="5b408-631">Fix bug where cmdlet failed if virtualNetwork was in a different resource group that the cluster.</span></span> <span data-ttu-id="5b408-632">문제 해결: https://github.com/Azure/azure-powershell/issues/8407</span><span class="sxs-lookup"><span data-stu-id="5b408-632">fixes issue: https://github.com/Azure/azure-powershell/issues/8407</span></span>
    - <span data-ttu-id="5b408-633">Add-AzServiceFabricApplicationCertificate cmdlet이 사용되지 않음</span><span class="sxs-lookup"><span data-stu-id="5b408-633">Deprecating Add-AzServiceFabricApplicationCertificate cmdlet</span></span>

#### <a name="azsql"></a><span data-ttu-id="5b408-634">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="5b408-634">Az.Sql</span></span>
* <span data-ttu-id="5b408-635">이전의 Auditing(감사) cmdlet에 대한 설명서가 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="5b408-635">Update documentation of old Auditing cmdlets.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="5b408-636">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="5b408-636">Az.Storage</span></span>
* <span data-ttu-id="5b408-637">더 많은 시나리오를 cmdlet 예제에 추가하고 매개 변수 설명을 업데이트하여 Get/Close-AzStorageFileHandle에 대한 도움말이 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="5b408-637">Update help for Get/Close-AzStorageFileHandle, by add more scenarios to cmdlet examples and update parameter descriptions</span></span>
* <span data-ttu-id="5b408-638">Blob 업로드 및 Blob 복사에서 StandardBlobTier가 지원됨</span><span class="sxs-lookup"><span data-stu-id="5b408-638">Support StandardBlobTier in upload blob and copy blob</span></span>
    -  <span data-ttu-id="5b408-639">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="5b408-639">Set-AzStorageBlobContent</span></span>
    -  <span data-ttu-id="5b408-640">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="5b408-640">Start-AzStorageBlobCopy</span></span>
* <span data-ttu-id="5b408-641">Blob 복사에서 우선 순위 리하이드레이션이 지원됨</span><span class="sxs-lookup"><span data-stu-id="5b408-641">Support Rehydrate Priority in copy blob</span></span>
    -  <span data-ttu-id="5b408-642">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="5b408-642">Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="5b408-643">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="5b408-643">Az.Websites</span></span>
* <span data-ttu-id="5b408-644">Set-AzWebApp 및 Set-AzWebAppSlot에서 -AppSettings 매개 변수에 대한 설명이 추가됨</span><span class="sxs-lookup"><span data-stu-id="5b408-644">Add clarification around -AppSettings parameter in Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <a name="250---july-2019"></a><span data-ttu-id="5b408-645">2.5.0 - 2019년 7월</span><span class="sxs-lookup"><span data-stu-id="5b408-645">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="5b408-646">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="5b408-646">Az.Accounts</span></span>
* <span data-ttu-id="5b408-647">ClientRuntime의 최신 버전을 사용하도록 일반적인 코드를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-647">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="5b408-648">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="5b408-648">Az.ApplicationInsights</span></span>
* <span data-ttu-id="5b408-649">'Remove-AzApplicationInsightsApiKey' 설명서의 예제 오타 수정</span><span class="sxs-lookup"><span data-stu-id="5b408-649">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span> 

#### <a name="azautomation"></a><span data-ttu-id="5b408-650">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="5b408-650">Az.Automation</span></span>
* <span data-ttu-id="5b408-651">리소스 문자열의 오타 수정</span><span class="sxs-lookup"><span data-stu-id="5b408-651">Fix typo in resource string</span></span> 

#### <a name="azcognitiveservices"></a><span data-ttu-id="5b408-652">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="5b408-652">Az.CognitiveServices</span></span>
* <span data-ttu-id="5b408-653">NetworkRuleSet 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-653">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="5b408-654">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="5b408-654">Az.Compute</span></span>
* <span data-ttu-id="5b408-655">VM 인스턴스 보기 개체의 누락된 속성(ComputerName, OsName, OsVersion 및 HyperVGeneration)을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-655">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="5b408-656">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="5b408-656">Az.ContainerRegistry</span></span>
* <span data-ttu-id="5b408-657">복제 매개 변수의 Remove-AzContainerRegistryReplication에서 오타 수정</span><span class="sxs-lookup"><span data-stu-id="5b408-657">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="5b408-658">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/9633 을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5b408-658">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="5b408-659">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="5b408-659">Az.DataFactory</span></span>
* <span data-ttu-id="5b408-660">ADF .Net SDK 버전을 4.1.0으로 업데이트</span><span class="sxs-lookup"><span data-stu-id="5b408-660">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="5b408-661">'Get-AzDataFactoryV2PipelineRun' 설명서의 오타 수정</span><span class="sxs-lookup"><span data-stu-id="5b408-661">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="5b408-662">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="5b408-662">Az.EventHub</span></span>
* <span data-ttu-id="5b408-663">SAS 토큰을 생성하기 위해 추가된 새로운 cmmdlet 추가: New-AzEventHubAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="5b408-663">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="5b408-664">'관리'만 지정된 경우 authorizationrules 권한에 대한 확인 및 오류 메시지 추가</span><span class="sxs-lookup"><span data-stu-id="5b408-664">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="5b408-665">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="5b408-665">Az.KeyVault</span></span>
* <span data-ttu-id="5b408-666">인증서 정책에 대한 KeySize 지정을 위한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="5b408-666">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="5b408-667">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="5b408-667">Az.LogicApp</span></span>
* <span data-ttu-id="5b408-668">모든 맵 유형을 나열하도록 Get-AzIntegrationAccountMap 수정</span><span class="sxs-lookup"><span data-stu-id="5b408-668">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="5b408-669">필터링을 위해 새 MapType 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="5b408-669">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="5b408-670">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="5b408-670">Az.ManagedServices</span></span>
* <span data-ttu-id="5b408-671">API 버전 2019-06-01(GA)에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="5b408-671">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="5b408-672">Az.Network</span><span class="sxs-lookup"><span data-stu-id="5b408-672">Az.Network</span></span>
* <span data-ttu-id="5b408-673">프라이빗 엔드포인트 및 프라이빗 링크 서비스에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="5b408-673">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="5b408-674">새 cmdlet</span><span class="sxs-lookup"><span data-stu-id="5b408-674">New cmdlets</span></span>
        - <span data-ttu-id="5b408-675">Set-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="5b408-675">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="5b408-676">Set-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="5b408-676">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="5b408-677">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="5b408-677">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="5b408-678">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="5b408-678">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="5b408-679">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="5b408-679">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="5b408-680">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="5b408-680">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="5b408-681">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="5b408-681">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="5b408-682">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="5b408-682">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="5b408-683">기능에 대한 새로운 명령이 업데이트됨: Virtualnetwork의 서브넷에 있는 PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies 플래그</span><span class="sxs-lookup"><span data-stu-id="5b408-683">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="5b408-684">업데이트된 New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="5b408-684">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="5b408-685">이 서브넷의 프라이빗 엔드포인트에 네트워크 정책을 적용할지 여부를 나타내는 선택적 매개 변수 -PrivateEndpointNetworkPoliciesFlag가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-685">Added optional parameter -PrivateEndpointNetworkPoliciesFlag that configures whether to apply network policies on private endpoint in this subnet.</span></span>
        - <span data-ttu-id="5b408-686">이 서브넷의 프라이빗 연결 서비스에 네트워크 정책을 적용할지 여부를 나타내는 선택적 매개 변수 -PrivateLinkServiceNetworkPoliciesFlag가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-686">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag that configures whether to apply network policies network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="5b408-687">AzPrivateLinkService의 cmdlet 매개 변수 'ServiceName'이 이전 버전과의 호환성을 위해 별칭 'ServiceName'을 사용한 'Name'으로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-687">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="5b408-688">네트워크 보안 규칙 구성에 ICMP 프로토콜 사용</span><span class="sxs-lookup"><span data-stu-id="5b408-688">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="5b408-689">다음 Cmdlet이 업데이트 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-689">Updated cmdlets</span></span>
        - <span data-ttu-id="5b408-690">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="5b408-690">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="5b408-691">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="5b408-691">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="5b408-692">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="5b408-692">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="5b408-693">New-AzVirtualNetworkGatewayConnection에 대한 구성 가능한 매개 변수로 ConnectionProtocolType (Ikev1/Ikev2) 추가</span><span class="sxs-lookup"><span data-stu-id="5b408-693">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="5b408-694">LoadBalancerFrontendIpConfiguration에 PrivateIpAddressVersion 추가</span><span class="sxs-lookup"><span data-stu-id="5b408-694">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="5b408-695">업데이트된 cmdlet:</span><span class="sxs-lookup"><span data-stu-id="5b408-695">Updated cmdlet:</span></span>
        - <span data-ttu-id="5b408-696">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="5b408-696">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="5b408-697">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="5b408-697">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="5b408-698">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="5b408-698">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="5b408-699">프로브에서 사용자 지정 포트를 지원하기 위한 Application Gateway New-AzApplicationGatewayProbeConfig 명령 업데이트</span><span class="sxs-lookup"><span data-stu-id="5b408-699">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="5b408-700">업데이트된 New-AzApplicationGatewayProbeConfig: 백 엔드 서버 검색에 사용되는 선택적 매개 변수 포트가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-700">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="5b408-701">이 매개 변수는 Standard_V2 및 WAF_V2 SKU에 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-701">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="5b408-702">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="5b408-702">Az.OperationalInsights</span></span>
* <span data-ttu-id="5b408-703">저장된 검색의 기본 버전이 1로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-703">Updated default version for saved searches to be 1.</span></span> 
* <span data-ttu-id="5b408-704">사용자 지정 로그 null regex 처리가 수정됨</span><span class="sxs-lookup"><span data-stu-id="5b408-704">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="5b408-705">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="5b408-705">Az.RecoveryServices</span></span>
* <span data-ttu-id="5b408-706">'Get-AzRecoveryServicesBackupJob.md' 업데이트</span><span class="sxs-lookup"><span data-stu-id="5b408-706">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="5b408-707">'Get-AzRecoveryServicesBackupContainer.md' 업데이트</span><span class="sxs-lookup"><span data-stu-id="5b408-707">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="5b408-708">'Get-AzRecoveryServicesVault.md' 업데이트</span><span class="sxs-lookup"><span data-stu-id="5b408-708">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="5b408-709">'Wait-AzRecoveryServicesBackupJob.md' 업데이트</span><span class="sxs-lookup"><span data-stu-id="5b408-709">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="5b408-710">'Set-AzRecoveryServicesVaultContext.md' 업데이트</span><span class="sxs-lookup"><span data-stu-id="5b408-710">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="5b408-711">'Get-AzRecoveryServicesBackupItem.md' 업데이트</span><span class="sxs-lookup"><span data-stu-id="5b408-711">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="5b408-712">'Get-AzRecoveryServicesBackupRecoveryPoint.md' 업데이트</span><span class="sxs-lookup"><span data-stu-id="5b408-712">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="5b408-713">'Restore-AzRecoveryServicesBackupItem.md' 업데이트</span><span class="sxs-lookup"><span data-stu-id="5b408-713">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="5b408-714">Azure 파일 공유용 컨테이너를 등록 취소하기 위해 서비스 요청 업데이트</span><span class="sxs-lookup"><span data-stu-id="5b408-714">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="5b408-715">'Set-AzRecoveryServicesAsrAlertSetting.md' 업데이트</span><span class="sxs-lookup"><span data-stu-id="5b408-715">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="5b408-716">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="5b408-716">Az.Resources</span></span>
- <span data-ttu-id="5b408-717">'New-AzResourceGroupDeployment' 설명서에서 참조된 누락 cmdlet 제거</span><span class="sxs-lookup"><span data-stu-id="5b408-717">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="5b408-718">새 API 버전 2019-01-01을 사용하도록 정책 cmdlet 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="5b408-718">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="5b408-719">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="5b408-719">Az.ServiceBus</span></span>
* <span data-ttu-id="5b408-720">SAS 토큰을 생성하기 위해 추가된 새로운 cmmdlet 추가: New-AzServiceBusAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="5b408-720">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="5b408-721">'관리'만 지정된 경우 authorizationrules 권한에 대한 확인 및 오류 메시지 추가</span><span class="sxs-lookup"><span data-stu-id="5b408-721">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="5b408-722">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="5b408-722">Az.Sql</span></span>
* <span data-ttu-id="5b408-723">Set-AzSqlDatabaseSecondary cmdlet에 대한 누락된 예제 수정</span><span class="sxs-lookup"><span data-stu-id="5b408-723">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="5b408-724">이메일 주소를 제공하지 않고 설정된 취약성 평가 반복 검색 수정</span><span class="sxs-lookup"><span data-stu-id="5b408-724">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="5b408-725">경고 메시지의 작은 오타를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-725">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="5b408-726">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="5b408-726">Az.Storage</span></span>
* <span data-ttu-id="5b408-727">'Get-AzStorageAccount'에 대한 참조 설명서의 예제를 업데이트하여 올바른 매개 변수 이름 사용</span><span class="sxs-lookup"><span data-stu-id="5b408-727">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="5b408-728">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="5b408-728">Az.StorageSync</span></span>
* <span data-ttu-id="5b408-729">Invoke-AzStorageSyncChangeDetection cmdlet을 추가하는 중입니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-729">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="5b408-730">TierFilesOlderThanDays를 기념하는 문제 9551 수정</span><span class="sxs-lookup"><span data-stu-id="5b408-730">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="5b408-731">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="5b408-731">Az.Websites</span></span>
* <span data-ttu-id="5b408-732">Get-AzWebApp 및 Set-AzWebApp에서 일부 SiteConfig 속성을 반환하지 않은 버그 수정</span><span class="sxs-lookup"><span data-stu-id="5b408-732">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="5b408-733">Get-AzDeletedWebApp 및 Restore-AzDeletedWebApp에 새 위치 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="5b408-733">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="5b408-734">AzWebApp-IncludeSourceWebAppSlots을 사용하여 웹앱 슬롯을 복제하는 버그를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-734">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="5b408-735">2.4.0 - 2019년 7월</span><span class="sxs-lookup"><span data-stu-id="5b408-735">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="5b408-736">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="5b408-736">Az.Accounts</span></span>
* <span data-ttu-id="5b408-737">프로필 cmdlet에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="5b408-737">Add support for profile cmdlets</span></span>
* <span data-ttu-id="5b408-738">생성된 cmdlet에서 환경 및 데이터 평면에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="5b408-738">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="5b408-739">Windows PowerShell의 데이터 평면 cmdlet에대해 일부 경우 잘못된 엔드포인트가 사용되는 버그 수정</span><span class="sxs-lookup"><span data-stu-id="5b408-739">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="5b408-740">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="5b408-740">Az.Advisor</span></span>
* <span data-ttu-id="5b408-741">Az.Advisor의 GA 릴리스</span><span class="sxs-lookup"><span data-stu-id="5b408-741">GA release of Az.Advisor</span></span>
* <span data-ttu-id="5b408-742">이 모듈은 이제 롤업 `Az` 모듈의 일부로 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-742">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="5b408-743">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="5b408-743">Az.ApiManagement</span></span>
* <span data-ttu-id="5b408-744">문제 https://github.com/Azure/azure-powershell/issues/8671 수정</span><span class="sxs-lookup"><span data-stu-id="5b408-744">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="5b408-745">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="5b408-745">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="5b408-746">사용자 및 제품별 구독을 쿼리하기 위한 지원이 추가됨</span><span class="sxs-lookup"><span data-stu-id="5b408-746">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="5b408-747">범위 '/', '/ api, '/ api/echo api'를 사용하여 쿼리하기 위한 지원이 추가됨</span><span class="sxs-lookup"><span data-stu-id="5b408-747">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="5b408-748">[https://github.com/Azure/azure-powershell/issues/9307](https://github.com/Azure/azure-powershell/issues/9307 ) 및 https://github.com/Azure/azure-powershell/issues/8432 문제 수정</span><span class="sxs-lookup"><span data-stu-id="5b408-748">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="5b408-749">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="5b408-749">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="5b408-750">Apis를 가져올 때 'ApiVersion' 및 'ApiVersionSetId'를 지정하기 위한 지원이 추가됨</span><span class="sxs-lookup"><span data-stu-id="5b408-750">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="5b408-751">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="5b408-751">Az.Automation</span></span>
* <span data-ttu-id="5b408-752">문자열 값을 처리하기 위해 Set-AzAutomationConnectionFieldValue cmdlet 버그를 수정했습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-752">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="5b408-753">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="5b408-753">Az.Compute</span></span>
* <span data-ttu-id="5b408-754">New-AzImageConfig에 HyperVGeneration 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="5b408-754">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="5b408-755">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="5b408-755">Az.DataFactory</span></span>
* <span data-ttu-id="5b408-756">get activity runs, get pipeline runs, get trigger runs ADF cmdlet의 출력을 업데이트하여 Select-Object pipe를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-756">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="5b408-757">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="5b408-757">Az.EventGrid</span></span>
* <span data-ttu-id="5b408-758">'New-AzEventGridSubcription' 설명서의 오타 수정</span><span class="sxs-lookup"><span data-stu-id="5b408-758">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="5b408-759">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="5b408-759">Az.IotHub</span></span>
* <span data-ttu-id="5b408-760">권한 부여 정책 키를 다시 생성하기 위한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="5b408-760">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="5b408-761">Az.Network</span><span class="sxs-lookup"><span data-stu-id="5b408-761">Az.Network</span></span>
* <span data-ttu-id="5b408-762">'RoutingPreference'를 공용 IP 태그에 추가함</span><span class="sxs-lookup"><span data-stu-id="5b408-762">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="5b408-763">'Get-AzNetworkServiceTag' 참조 설명서의 예제 개선</span><span class="sxs-lookup"><span data-stu-id="5b408-763">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="5b408-764">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="5b408-764">Az.PolicyInsights</span></span>
* <span data-ttu-id="5b408-765">Get-AzPolicyState의 null 참조 문제 해결</span><span class="sxs-lookup"><span data-stu-id="5b408-765">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="5b408-766">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/9446 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5b408-766">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="5b408-767">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="5b408-767">Az.OperationalInsights</span></span>
* <span data-ttu-id="5b408-768">Get-AzOperationalInsightsDataSource에 반환된 CustomLog datasource 모델 수정됨</span><span class="sxs-lookup"><span data-stu-id="5b408-768">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="5b408-769">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="5b408-769">Az.RecoveryServices</span></span>
* <span data-ttu-id="5b408-770">IaaSVMs에 대한 get-policy 명령 수정</span><span class="sxs-lookup"><span data-stu-id="5b408-770">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="5b408-771">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="5b408-771">Az.Resources</span></span>
    - <span data-ttu-id="5b408-772">Get-AzPolicyState -Top 매개 변수에 대한 도움말 텍스트 수정</span><span class="sxs-lookup"><span data-stu-id="5b408-772">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="5b408-773">Get-AzPolicyAlias에 대한 클라이언트 쪽 페이징 지원 추가</span><span class="sxs-lookup"><span data-stu-id="5b408-773">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="5b408-774">Set-AzPolicyAssignment, -PolicyParameters 및 -PolicyParametersObject에 대한 새 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="5b408-774">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="5b408-775">Policy cmdlet에 대한 몇 가지 문서 및 예제 업데이트</span><span class="sxs-lookup"><span data-stu-id="5b408-775">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="5b408-776">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="5b408-776">Az.ServiceBus</span></span>
* <span data-ttu-id="5b408-777">문제 #4938 수정 - MaxSizeInMegabytes를 설정할 때 New-AzureRmServiceBusQueue가 BadRequest 반환</span><span class="sxs-lookup"><span data-stu-id="5b408-777">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="5b408-778">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="5b408-778">Az.Sql</span></span>
* <span data-ttu-id="5b408-779">미리 보기 릴리스에서 공개 릴리스로 인스턴스 장애 조치(Failover) 그룹 cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="5b408-779">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="5b408-780">새 cmdlet으로 Azure SQL Server\Database Auditing을 지원하세요.</span><span class="sxs-lookup"><span data-stu-id="5b408-780">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="5b408-781">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="5b408-781">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="5b408-782">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="5b408-782">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="5b408-783">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="5b408-783">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="5b408-784">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="5b408-784">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="5b408-785">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="5b408-785">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="5b408-786">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="5b408-786">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="5b408-787">취약성 평가 설정에서 이메일 제약 조건 제거</span><span class="sxs-lookup"><span data-stu-id="5b408-787">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="5b408-788">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="5b408-788">Az.Storage</span></span>
* <span data-ttu-id="5b408-789">다음 cmdlet에서 2개의 매개 변수 '-IndexDocument' 및 '-ErrorDocument404Path'를 필수에서 선택으로 변경하세요.</span><span class="sxs-lookup"><span data-stu-id="5b408-789">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="5b408-790">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="5b408-790">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="5b408-791">예제를 추가하여 Get-AzStorageBlobContent의 도움말 업데이트</span><span class="sxs-lookup"><span data-stu-id="5b408-791">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="5b408-792">StorageException으로 cmdlet이 실패한 경우 자세한 오류 정보 표시</span><span class="sxs-lookup"><span data-stu-id="5b408-792">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="5b408-793">Azure Files AAD DS 인증으로 스토리지 계정 생성 또는 업데이트 지원</span><span class="sxs-lookup"><span data-stu-id="5b408-793">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="5b408-794">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="5b408-794">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="5b408-795">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="5b408-795">Set-AzStorageAccount</span></span>
* <span data-ttu-id="5b408-796">파일 공유, 파일 디렉터리 또는 파일의 목록 지원 또는 파일 핸들 닫기</span><span class="sxs-lookup"><span data-stu-id="5b408-796">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="5b408-797">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="5b408-797">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="5b408-798">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="5b408-798">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="5b408-799">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="5b408-799">Az.StorageSync</span></span>
* <span data-ttu-id="5b408-800">이 모듈은 이제 롤업 `Az` 모듈의 일부로 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-800">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="5b408-801">2.3.2 - 2019년 6월</span><span class="sxs-lookup"><span data-stu-id="5b408-801">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="5b408-802">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="5b408-802">Az.Accounts</span></span>
* <span data-ttu-id="5b408-803">함수 호출에 대해 일부 경우 잘못된 URL이 사용되는 버그 수정</span><span class="sxs-lookup"><span data-stu-id="5b408-803">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="5b408-804">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/8983 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5b408-804">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="5b408-805">AzureRM에서 Az cmdlet으로의 별칭 문제 해결</span><span class="sxs-lookup"><span data-stu-id="5b408-805">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="5b408-806">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="5b408-806">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="5b408-807">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="5b408-807">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="5b408-808">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="5b408-808">Az.Compute</span></span>
* <span data-ttu-id="5b408-809">New-AzVm 및 New-AzVmss 단순 매개 변수 집합은 이제 'ProximityPlacementGroup'매개 변수를 허용합니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-809">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="5b408-810">'New-AzVM' 참조 설명서에서 오타 수정</span><span class="sxs-lookup"><span data-stu-id="5b408-810">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="5b408-811">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="5b408-811">Az.Dns</span></span>
* <span data-ttu-id="5b408-812">'Set-AzDnsZone' 도움말 예제의 오타가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-812">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="5b408-813">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="5b408-813">Az.EventGrid</span></span>
* <span data-ttu-id="5b408-814">2019-06-01 API 버전을 사용하도록 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-814">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="5b408-815">새 cmdlet:</span><span class="sxs-lookup"><span data-stu-id="5b408-815">New cmdlets:</span></span>
    - <span data-ttu-id="5b408-816">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="5b408-816">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="5b408-817">새 Azure Event Grid 도메인을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-817">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="5b408-818">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="5b408-818">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="5b408-819">Event Grid 도메인의 세부 정보를 가져오거나 현재 Azure 구독의 모든 Event Grid 도메인 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-819">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="5b408-820">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="5b408-820">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="5b408-821">Azure Event Grid 도메인을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-821">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="5b408-822">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="5b408-822">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="5b408-823">Azure Event Grid 도메인에 대한 공유 액세스 키를 다시 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-823">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="5b408-824">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="5b408-824">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="5b408-825">Event Grid 도메인 이벤트를 게시하는 데 사용되는 공유 액세스 키를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-825">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="5b408-826">New-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="5b408-826">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="5b408-827">새 Azure Event Grid 도메인 토픽을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-827">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="5b408-828">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="5b408-828">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="5b408-829">Event Grid 도메인 토픽의 세부 사항을 가져오거나, 현재 Azure의 특정 Event Grid 도메인 아래의 모든 Event Grid 도메인 토픽 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-829">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span> 
    - <span data-ttu-id="5b408-830">Remove-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="5b408-830">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="5b408-831">기존 Azure Event Grid 도메인 토픽을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-831">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="5b408-832">다음 Cmdlet이 업데이트 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-832">Updated cmdlets:</span></span>
    - <span data-ttu-id="5b408-833">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="5b408-833">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="5b408-834">새로운 Event Grid 도메인 및 Event Grid 도메인 토픽에 대한 파이핑을 지원하기 위해 새로운 필수 매개 변수를 추가하여 이러한 리소스 아래에 새 이벤트 구독을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-834">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="5b408-835">새로운 Event Grid 도메인 이름 및 Event Grid 도메인 토픽 이름을 지정하기 위해 새로운 필수 매개 변수를 추가하여 이러한 리소스 아래에 새 이벤트 구독을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-835">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="5b408-836">기존 매개 변수(예: EndPointType, SubjectBeginsWith 등)를 재사용할 수 있도록 도메인 및 도메인 토픽에 대한 새로운 매개 변수 집합을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-836">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="5b408-837">지정을 위한 새로운 선택적 매개 변수를 추가</span><span class="sxs-lookup"><span data-stu-id="5b408-837">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="5b408-838">이벤트 구독 만료 날짜,</span><span class="sxs-lookup"><span data-stu-id="5b408-838">Event subscription expiration date,</span></span>
            - <span data-ttu-id="5b408-839">고급 필터링 매개 변수.</span><span class="sxs-lookup"><span data-stu-id="5b408-839">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="5b408-840">대상으로 servicebusqueue에 대한 새 열거형을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-840">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="5b408-841">-IncludedEventType 옵션에서 'All' 사용을 허용하지 않고 다음으로 대체함</span><span class="sxs-lookup"><span data-stu-id="5b408-841">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span> 
    - <span data-ttu-id="5b408-842">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="5b408-842">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="5b408-843">결과 페이지 매김 및 필터링을 지원하는 새로운 선택적 매개 변수(Top, ODataQuery 및 NextLink)를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-843">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="5b408-844">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="5b408-844">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="5b408-845">Event Grid 도메인 및 Event Grid 도메인 토픽에 대한 파이핑을 지원하기 위해 새로운 필수 매개 변수를 추가하여 이러한 리소스 아래에 기존 이벤트 구독을 제거할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-845">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="5b408-846">Event Grid 도메인 이름 및 Event Grid 도메인 토픽 이름을 지정하기 위해 새로운 필수 매개 변수를 추가하여 이러한 리소스 아래에 기존 이벤트 구독을 제거할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-846">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="5b408-847">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="5b408-847">Az.FrontDoor</span></span>
* <span data-ttu-id="5b408-848">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="5b408-848">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="5b408-849">변환 지원 및 새 연산자 자동 완성 값(RegEx)을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-849">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="5b408-850">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="5b408-850">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="5b408-851">새 자동 완성 값 추가</span><span class="sxs-lookup"><span data-stu-id="5b408-851">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="5b408-852">Az.Network</span><span class="sxs-lookup"><span data-stu-id="5b408-852">Az.Network</span></span>
* <span data-ttu-id="5b408-853">Microsoft Azure Virtual Network 게이트웨이 리소스에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="5b408-853">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="5b408-854">새 cmdlet</span><span class="sxs-lookup"><span data-stu-id="5b408-854">New cmdlets</span></span>
        - <span data-ttu-id="5b408-855">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="5b408-855">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="5b408-856">AvailablePrivateEndpointType 추가</span><span class="sxs-lookup"><span data-stu-id="5b408-856">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="5b408-857">새 cmdlet</span><span class="sxs-lookup"><span data-stu-id="5b408-857">New cmdlets</span></span> 
        - <span data-ttu-id="5b408-858">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="5b408-858">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="5b408-859">PrivatePrivateLinkService 추가</span><span class="sxs-lookup"><span data-stu-id="5b408-859">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="5b408-860">새 cmdlet</span><span class="sxs-lookup"><span data-stu-id="5b408-860">New cmdlets</span></span> 
        - <span data-ttu-id="5b408-861">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="5b408-861">Get-AzPrivateLinkService</span></span> 
        - <span data-ttu-id="5b408-862">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="5b408-862">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="5b408-863">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="5b408-863">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="5b408-864">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="5b408-864">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="5b408-865">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="5b408-865">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="5b408-866">PrivateEndpoint 추가</span><span class="sxs-lookup"><span data-stu-id="5b408-866">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="5b408-867">새 cmdlet</span><span class="sxs-lookup"><span data-stu-id="5b408-867">New cmdlets</span></span>
        - <span data-ttu-id="5b408-868">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="5b408-868">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="5b408-869">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="5b408-869">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="5b408-870">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="5b408-870">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="5b408-871">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="5b408-871">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="5b408-872">기능에 대한 새로운 명령이 업데이트됨: VpnConnection 상의 UseLocalAzureIpAddress 플래그</span><span class="sxs-lookup"><span data-stu-id="5b408-872">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="5b408-873">New-AzVpnConnection이 업데이트됨: 선택적 매개 변수 -UseLocalAzureIpAddress를 추가하여 로컬 Azure IP 주소가 연결을 시작하는 동안 소스 주소로 사용되어야 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-873">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="5b408-874">Set-AzVpnConnection이 업데이트됨: 선택적 매개 변수 -UseLocalAzureIpAddress를 추가하여 로컬 Azure IP 주소가 연결을 시작하는 동안 소스 주소로 사용되어야 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-874">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="5b408-875">ExpressRoute 피어링에 읽기 전용 필드 PeeredConnections가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-875">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="5b408-876">ExpressRoute에 읽기 전용 필드 GlobalReachEnabled가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-876">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="5b408-877">ExpressRouteCircuit 모델에서 AllowGlobalReach 필드의 사용 중단을 부르는 호환성이 손상되는 변경 속성이 추가됨</span><span class="sxs-lookup"><span data-stu-id="5b408-877">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="5b408-878">AzApplicationGatewayRedirectConfiguration cmdlet에서 TargetListenerID를 사용하는 중의 8756 오류 문제가 해결됨</span><span class="sxs-lookup"><span data-stu-id="5b408-878">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="5b408-879">다시 쓰기 규칙 세트가 설정되지 못하게 하는 New-AzApplicationGatewayPathRuleConfig의 버그를 수정했습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-879">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="5b408-880">NetworkInterfaceIpConfiguration에 VirtualNetworkTaps가 표시되는 방식이 수정됨</span><span class="sxs-lookup"><span data-stu-id="5b408-880">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="5b408-881">모든 파트를 나열하도록 Cortex Get cmdlet이 수정됨</span><span class="sxs-lookup"><span data-stu-id="5b408-881">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="5b408-882">ExpressRouteGateways, VpnGateway에 대한 VirtualHub 참조 생성 수정됨</span><span class="sxs-lookup"><span data-stu-id="5b408-882">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="5b408-883">AzureFirewall 및 NatGateway의 가용성 영역에 대한 지원 추가됨</span><span class="sxs-lookup"><span data-stu-id="5b408-883">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="5b408-884">Get-AzNetworkServiceTag cmdlet 추가됨</span><span class="sxs-lookup"><span data-stu-id="5b408-884">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="5b408-885">Azure Firewall에 대한 여러 공용 IP 주소에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="5b408-885">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="5b408-886">New-AzFirewall cmdlet이 업데이트됨:</span><span class="sxs-lookup"><span data-stu-id="5b408-886">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="5b408-887">하나 이상의 공용 IP 주소 개체를 허용하는 매개 변수 -PublicIpAddress 추가됨</span><span class="sxs-lookup"><span data-stu-id="5b408-887">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="5b408-888">Virtual Network 개체를 허용하는 매개 변수 -VirtualNetwork 추가됨</span><span class="sxs-lookup"><span data-stu-id="5b408-888">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="5b408-889">방화벽 개체에 AddPublicIpAddress 및 RemovePublicIpAddress 메서드 추가됨 - 공용 IP 주소 개체를 입력으로 허용</span><span class="sxs-lookup"><span data-stu-id="5b408-889">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="5b408-890">매개 변수 -PublicIpName 및 -VirtualNetworkName이 더 이상 사용되지 않음</span><span class="sxs-lookup"><span data-stu-id="5b408-890">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span> 
* <span data-ttu-id="5b408-891">기능에 대한 새로운 명령이 업데이트됨: VpnClient AAD 인증 옵션을 가상 네트워크 게이트웨이 리소스로 설정했습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-891">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span> 
    - <span data-ttu-id="5b408-892">New-AzVirtualNetworkGateway가 업데이트됨: 게이트웨이에서 VpnClient AAD 인증 옵션을 설정할 수 있도록 선택적 매개 변수 AadTenantUri, AadAudienceId, AadIssuerUri가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-892">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="5b408-893">Set-AzVirtualNetworkGateway가 업데이트됨: 게이트웨이에서 VpnClient AAD 인증 옵션을 설정할 수 있도록 선택적 매개 변수 AadTenantUri, AadAudienceId, AadIssuerUri가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-893">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="5b408-894">Set-AzVirtualNetworkGateway가 업데이트됨: 게이트웨이에서 VpnClient AAD 인증 옵션을 제거할 수 있도록 선택적인 스위치 매개 변수 RemoveAadAuthentication이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-894">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="5b408-895">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="5b408-895">Az.OperationalInsights</span></span>
* <span data-ttu-id="5b408-896">'New-AzureRmOperationalInsightsWorkspace' 명령에서 **pergb2018** 가격 책정 계층 사용</span><span class="sxs-lookup"><span data-stu-id="5b408-896">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="5b408-897">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="5b408-897">Az.Resources</span></span>
* <span data-ttu-id="5b408-898">추가 템플릿 내보내기 옵션 지원</span><span class="sxs-lookup"><span data-stu-id="5b408-898">Support for additional Template Export options</span></span>
    - <span data-ttu-id="5b408-899">Export-AzResourceGroup에 '-SkipResourceNameParameterization' 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="5b408-899">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="5b408-900">Export-AzResourceGroup에 '-SkipAllParameterization' 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="5b408-900">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="5b408-901">내보낸 리소스 필터링을 위해 Export-AzResourceGroup에 '-Resource' 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="5b408-901">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="5b408-902">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="5b408-902">Az.ServiceFabric</span></span>
* <span data-ttu-id="5b408-903">일부 경우 잘못된 지문을 가져오는 추가 인증서 ByExistingKeyVault 수정</span><span class="sxs-lookup"><span data-stu-id="5b408-903">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="5b408-904">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="5b408-904">Az.Sql</span></span>
* <span data-ttu-id="5b408-905">Advanced Threat Protection 스토리지 엔드포인트 접미사 수정</span><span class="sxs-lookup"><span data-stu-id="5b408-905">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="5b408-906">Advanced Data Security가 Advanced Threat Protection 정책을 재정의하는 것을 수정</span><span class="sxs-lookup"><span data-stu-id="5b408-906">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="5b408-907">고객이 TDE 키를 추가하고 관리되는 인스턴스에 TDE 보호기를 설정할 수 있도록 Management.Sql용 새 Cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="5b408-907">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="5b408-908">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="5b408-908">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="5b408-909">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="5b408-909">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="5b408-910">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="5b408-910">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="5b408-911">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="5b408-911">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="5b408-912">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="5b408-912">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="5b408-913">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="5b408-913">Az.Storage</span></span>
* <span data-ttu-id="5b408-914">스토리지 계정 생성 시 종류 FileStorage 및 SkuName Premium_ZRS 지원</span><span class="sxs-lookup"><span data-stu-id="5b408-914">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="5b408-915">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="5b408-915">New-AzStorageAccount</span></span>
* <span data-ttu-id="5b408-916">BLOB immutability cmdlet의 설명 명확화</span><span class="sxs-lookup"><span data-stu-id="5b408-916">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="5b408-917">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="5b408-917">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="5b408-918">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="5b408-918">Az.Websites</span></span>
* <span data-ttu-id="5b408-919">Get-AzWebAppCertificate를 클라이언트 대신 서버의 리소스 그룹별로 필터링하도록 최적화</span><span class="sxs-lookup"><span data-stu-id="5b408-919">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="5b408-920">Get-AzWebAppSnapshot에 -UseDisasterRecovery 스위치 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="5b408-920">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="5b408-921">2.2.0 - 2019년 6월</span><span class="sxs-lookup"><span data-stu-id="5b408-921">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="5b408-922">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="5b408-922">Az.Cdn</span></span>
* <span data-ttu-id="5b408-923">cmdlet에서 2019-04-15 API 버전 기반의 rulesEngine 기능을 지원하도록 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-923">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="5b408-924">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="5b408-924">Az.Compute</span></span>
* <span data-ttu-id="5b408-925">작업을 시작하여 완료되기 전에 즉시 반환하는 `NoWait` 매개 변수가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-925">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="5b408-926">다음 Cmdlet이 업데이트 되었습니다.   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="5b408-926">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="5b408-927">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="5b408-927">Az.EventHub</span></span>
* <span data-ttu-id="5b408-928">#9231 수정 - Get-AzEventHubNamespace에서 태그를 반환하지 않음</span><span class="sxs-lookup"><span data-stu-id="5b408-928">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="5b408-929">#9230 수정 - Get-AzEventHubNamespace에서 ResourceGroupName 대신 ResourceGroup을 반환함</span><span class="sxs-lookup"><span data-stu-id="5b408-929">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="5b408-930">Az.Network</span><span class="sxs-lookup"><span data-stu-id="5b408-930">Az.Network</span></span>
* <span data-ttu-id="5b408-931">Nat Gateway에 대한 ResourceId 및 InputObject 업데이트</span><span class="sxs-lookup"><span data-stu-id="5b408-931">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="5b408-932">ResourceId 및 InputObject에 대한 별칭 추가</span><span class="sxs-lookup"><span data-stu-id="5b408-932">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="5b408-933">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="5b408-933">Az.PolicyInsights</span></span>
* <span data-ttu-id="5b408-934">Get-AzPolicyEvent에서 Null 참조 문제 해결</span><span class="sxs-lookup"><span data-stu-id="5b408-934">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="5b408-935">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="5b408-935">Az.RecoveryServices</span></span>
* <span data-ttu-id="5b408-936">IaaSVM 정책 최소 보존 기간(일)이 1에서 7로 변경됨</span><span class="sxs-lookup"><span data-stu-id="5b408-936">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="5b408-937">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="5b408-937">Az.ServiceBus</span></span>
* <span data-ttu-id="5b408-938">#9182 문제 해결 - Get-AzServiceBusNamespace에서 ResourceGroupName 대신 ResourceGroup을 반환</span><span class="sxs-lookup"><span data-stu-id="5b408-938">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="5b408-939">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="5b408-939">Az.ServiceFabric</span></span>
* <span data-ttu-id="5b408-940">'Update-AzServiceFabricReliability' 오류 메시지의 오타 수정</span><span class="sxs-lookup"><span data-stu-id="5b408-940">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="5b408-941">Service Fabric 명령줄에서 누락된 문자 수정</span><span class="sxs-lookup"><span data-stu-id="5b408-941">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="5b408-942">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="5b408-942">Az.Sql</span></span>
* <span data-ttu-id="5b408-943">Managed Instance에 대한 AutoDr을 지원하기 위해 New-AzureSqlInstance cmdlet에 대한 DnsZonePartner 매개 변수를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-943">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="5b408-944">Get-AzSqlDatabaseSecureConnectionPolicy cmdlet 사용 중단</span><span class="sxs-lookup"><span data-stu-id="5b408-944">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="5b408-945">Threat Detection(위협 탐지) cmdlet 이름을 Advanced Threat Protection으로 변경함</span><span class="sxs-lookup"><span data-stu-id="5b408-945">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="5b408-946">새 AzSqlInstance -StorageSizeInGB 및 -LicenseType 매개 변수는 이제 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-946">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="5b408-947">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="5b408-947">Az.Websites</span></span>
* <span data-ttu-id="5b408-948">-WebApp 속성에서 Set-AzWebApp 및 Set-AzWebAppSlot을 사용하면 태그가 제거되는 문제를 해결함</span><span class="sxs-lookup"><span data-stu-id="5b408-948">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="5b408-949">2.1.0 - 2019년 5월</span><span class="sxs-lookup"><span data-stu-id="5b408-949">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="5b408-950">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="5b408-950">Az.ApiManagement</span></span>
* <span data-ttu-id="5b408-951">글로벌 및 API 범위에서 진단을 관리하기 위한 새 cmdlet을 만들었습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-951">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="5b408-952">**Get-AzApiManagementDiagnostic** - 글로벌 또는 API 범위가 구성된 진단 가져오기</span><span class="sxs-lookup"><span data-stu-id="5b408-952">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="5b408-953">**New-AzApiManagementDiagnostic** - 글로벌 범위 또는 API 범위에서 새 진단 만들기</span><span class="sxs-lookup"><span data-stu-id="5b408-953">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="5b408-954">**New-AzApiManagementHttpMessageDiagnostic** - 기록할 Headers(헤더) 및 Body Bytes(본문 바이트 수) 크기에 대한 진단 설정 만들기</span><span class="sxs-lookup"><span data-stu-id="5b408-954">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="5b408-955">**New-AzApiManagementPipelineDiagnosticSetting** - 게이트웨이로 들어오고 나가는 HTTP 메시지에 대한 진단 설정 만들기</span><span class="sxs-lookup"><span data-stu-id="5b408-955">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="5b408-956">**New-AzApiManagementSamplingSetting** - 진단 요청/응답에 대한 샘플링 설정 만들기</span><span class="sxs-lookup"><span data-stu-id="5b408-956">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="5b408-957">**Remove-AzApiManagementDiagnostic** - 글로벌 또는 API 범위에서 진단 엔터티 제거</span><span class="sxs-lookup"><span data-stu-id="5b408-957">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="5b408-958">**Set-AzApiManagementDiagnostic** - 글로벌 또는 API 범위에서 진단 엔터티 업데이트</span><span class="sxs-lookup"><span data-stu-id="5b408-958">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="5b408-959">ApiManagement 서비스에서 캐시를 관리하기 위한 새 cmdlet을 만들었습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-959">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="5b408-960">**Get-AzApiManagementCache** - 식별자 또는 모든 캐시로 지정된 캐시의 세부 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="5b408-960">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="5b408-961">**New-AzApiManagementCache** - 특정 Azure 'region'(지역)에 새 'default'(기본) 캐시 만들기</span><span class="sxs-lookup"><span data-stu-id="5b408-961">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="5b408-962">**Remove-AzApiManagementCache** - 캐시 제거</span><span class="sxs-lookup"><span data-stu-id="5b408-962">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="5b408-963">**Update-AzApiManagementCache** - 캐시 업데이트</span><span class="sxs-lookup"><span data-stu-id="5b408-963">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="5b408-964">API 스키마 관리하기 위한 새 cmdlet을 만들었습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-964">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="5b408-965">**New-AzApiManagementSchema** - API에 대한 새 스키마 만들기</span><span class="sxs-lookup"><span data-stu-id="5b408-965">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="5b408-966">**Get-AzApiManagementSchema** - API에 구성된 스키마 가져오기</span><span class="sxs-lookup"><span data-stu-id="5b408-966">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="5b408-967">**Remove-AzApiManagementSchema** - API에 구성된 스키마 제거</span><span class="sxs-lookup"><span data-stu-id="5b408-967">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="5b408-968">**Set-AzApiManagementSchema** - API에 구성된 스키마 업데이트</span><span class="sxs-lookup"><span data-stu-id="5b408-968">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="5b408-969">사용자 토큰을 생성하기 위한 새 cmdlet을 만들었습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-969">Created new Cmdlet for generating a User Token.</span></span> 
    - <span data-ttu-id="5b408-970">**New-AzApiManagementUserToken** - 기본적으로 8시간 동안 유효한 새 사용자 토큰을 생성합니다. 'GIT' 사용자에 대한 토큰은 이 cmdlet을 사용하여 생성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-970">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="5b408-971">네트워크 상태를 검색하기 위한 새 cmdlet을 만들었습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-971">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="5b408-972">**Get-AzApiManagementNetworkStatus** - API Management 서비스에서 사용하는 리소스의 네트워크 상태 연결을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-972">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="5b408-973">ApiManagement 서비스를 가상 네트워크에 배포하고 종속성이 손상되었는지 여부를 확인할 때 유용합니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-973">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="5b408-974">**New-AzApiManagement** cmdlet에서 ApiManagement 서비스를 관리하도록 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-974">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span> 
    - <span data-ttu-id="5b408-975">새 '소비' SKU 지원이 추가됨</span><span class="sxs-lookup"><span data-stu-id="5b408-975">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="5b408-976">'소비' SKU에 대해 'EnableClientCertificate' 플래그를 설정하기 위한 지원이 추가됨</span><span class="sxs-lookup"><span data-stu-id="5b408-976">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="5b408-977">새 **New-AzApiManagementSslSetting** cmdlet을 사용하면 'Backend(백 엔드)' 및 'Frontend'(프런트 엔드)에서 'TLS/SSL' 설정을 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-977">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="5b408-978">또한 ApiManagement 서비스의 'Frontend'에서 '3DES'와 같은 'Ciphers'와 'Http2'와 같은 'ServerProtocols'를 구성하는 데 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-978">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="5b408-979">ApiManagement 서비스에서 'DeveloperPortal' 호스트 이름을 구성하기 위한 지원이 추가됨</span><span class="sxs-lookup"><span data-stu-id="5b408-979">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="5b408-980">**Get-AzApiManagementSsoToken** cmdlet에서 'PsApiManagement' 개체를 입력으로 사용하도록 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-980">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="5b408-981">cmdlet에서 오류 메시지를 인라인으로 표시하도록 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-981">Updated the cmdlet to display Error Messages inline</span></span> 
     > <span data-ttu-id="5b408-982">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : 오류 코드: ValidationError 오류 메시지: 하나 이상의 필드에 잘못된 값이 있습니다. 오류 세부 정보:    [Code=ValidationError, Message=줄 3, 열 10의 'log-to-eventhub' 요소에 오류가 있습니다.: 로거를 찾지 못함, Target=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="5b408-982">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="5b408-983">**Export-AzApiManagementApi** cmdlet에서 API를 'OpenApi 3.0' 형식으로 내보내도록 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-983">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="5b408-984">**Import-AzApiManagementApi** cmdlet을 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-984">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="5b408-985">'OpenApi 3.0' 문서 사양에서 API 가져오기</span><span class="sxs-lookup"><span data-stu-id="5b408-985">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="5b408-986">문서('Swagger', 'Wadl', 'Wsdl', 'OpenApi')에 지정된 'PsApiManagementSchema' 속성 재정의</span><span class="sxs-lookup"><span data-stu-id="5b408-986">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="5b408-987">문서에 지정된 'ServiceUrl' 속성 재정의</span><span class="sxs-lookup"><span data-stu-id="5b408-987">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="5b408-988">**Get-AzApiManagementPolicy** cmdlet에서 'rawxml'을 사용하여 이스케이프된 비 Xml 'format'(형식)의 정책을 반환하도록 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-988">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="5b408-989">**Set-AzApiManagementPolicy** cmdlet에서 'rawxml'을 사용하여 이스케이프된 비 Xml 'format'의 정책을 수락하고, 'xml'을 사용하여 이스케이프된 Xml 'format'의 정책을 수락하도록 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-989">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="5b408-990">**New-AzApiManagementApi** cmdlet을 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-990">Updated cmdlet **New-AzApiManagementApi**</span></span> 
    - <span data-ttu-id="5b408-991">'OpenId' 권한 부여 서버를 사용하여 API 구성</span><span class="sxs-lookup"><span data-stu-id="5b408-991">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="5b408-992">'ApiVersionSet'에서 API 만들기</span><span class="sxs-lookup"><span data-stu-id="5b408-992">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="5b408-993">'SourceApiId' 및 'SourceApiRevision'을 사용하여 API 복제</span><span class="sxs-lookup"><span data-stu-id="5b408-993">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="5b408-994">API 범위에서 'SubscriptionRequired' 구성 가능</span><span class="sxs-lookup"><span data-stu-id="5b408-994">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="5b408-995">**Set-AzApiManagementApi** cmdlet을 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-995">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="5b408-996">'OpenId' 권한 부여 서버를 사용하여 API 구성</span><span class="sxs-lookup"><span data-stu-id="5b408-996">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="5b408-997">API를 'ApiVersionSet'으로 업데이트</span><span class="sxs-lookup"><span data-stu-id="5b408-997">To updated an API into an 'ApiVersionSet'</span></span>    
    - <span data-ttu-id="5b408-998">API 범위에서 'SubscriptionRequired' 구성 가능</span><span class="sxs-lookup"><span data-stu-id="5b408-998">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="5b408-999">**New-AzApiManagementRevision** cmdlet을 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-999">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="5b408-1000">'SourceApiRevision'을 사용하여 기존 수정 버전 복제(태그, 제품, 작업 및 정책 복사).</span><span class="sxs-lookup"><span data-stu-id="5b408-1000">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="5b408-1001">새 수정 버전은 부모의 'ApiId'를 가정합니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-1001">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="5b408-1002">'ApiRevisionDescription' 제공</span><span class="sxs-lookup"><span data-stu-id="5b408-1002">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="5b408-1003">API 복제 시 'ServiceUrl' 재정의</span><span class="sxs-lookup"><span data-stu-id="5b408-1003">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="5b408-1004">**New-AzApiManagementIdentityProvider** cmdlet을 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-1004">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="5b408-1005">'Authority'를 사용하여 'AAD' 또는 'AADB2C' 구성</span><span class="sxs-lookup"><span data-stu-id="5b408-1005">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="5b408-1006">'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' 및 'PasswordResetPolicy' 설정</span><span class="sxs-lookup"><span data-stu-id="5b408-1006">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="5b408-1007">**New-AzApiManagementSubscription** cmdlet을 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-1007">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="5b408-1008">'Scope' 및 'UserId'를 사용하여 새 SubscriptonModel 설명</span><span class="sxs-lookup"><span data-stu-id="5b408-1008">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="5b408-1009">'ProductId' 및 'UserId'를 사용하여 이전 구독 모델 설명</span><span class="sxs-lookup"><span data-stu-id="5b408-1009">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="5b408-1010">구독 수준에서 'AllowTracing'을 사용하도록 설정하는 지원 추가</span><span class="sxs-lookup"><span data-stu-id="5b408-1010">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="5b408-1011">**Set-AzApiManagementSubscription** cmdlet을 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-1011">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="5b408-1012">'Scope' 및 'UserId'를 사용하여 새 SubscriptonModel 설명</span><span class="sxs-lookup"><span data-stu-id="5b408-1012">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="5b408-1013">'ProductId' 및 'UserId'를 사용하여 이전 구독 모델 설명</span><span class="sxs-lookup"><span data-stu-id="5b408-1013">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="5b408-1014">구독 수준에서 'AllowTracing'을 사용하도록 설정하는 지원 추가</span><span class="sxs-lookup"><span data-stu-id="5b408-1014">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="5b408-1015">다음 cmdlet에서 'ResourceId'를 입력으로 수락하도록 업데이트했습니다</span><span class="sxs-lookup"><span data-stu-id="5b408-1015">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="5b408-1016">'New-AzApiManagementContext'</span><span class="sxs-lookup"><span data-stu-id="5b408-1016">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="5b408-1017">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="5b408-1017">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="5b408-1018">'Get-AzApiManagementApiRelease'</span><span class="sxs-lookup"><span data-stu-id="5b408-1018">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="5b408-1019">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="5b408-1019">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="5b408-1020">'Get-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="5b408-1020">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="5b408-1021">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="5b408-1021">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="5b408-1022">'Get-AzApiManagementAuthorizationServer'</span><span class="sxs-lookup"><span data-stu-id="5b408-1022">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="5b408-1023">'Get-AzApiManagementBackend'</span><span class="sxs-lookup"><span data-stu-id="5b408-1023">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="5b408-1024">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="5b408-1024">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="5b408-1025">'Get-AzApiManagementCertificate'</span><span class="sxs-lookup"><span data-stu-id="5b408-1025">'Get-AzApiManagementCertificate'</span></span> 
    - <span data-ttu-id="5b408-1026">'Remove-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="5b408-1026">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="5b408-1027">'Remove-AzApiManagementSubscription'</span><span class="sxs-lookup"><span data-stu-id="5b408-1027">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="5b408-1028">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="5b408-1028">Az.Automation</span></span>
* <span data-ttu-id="5b408-1029">Get-AzAutomationJobOutputRecord에서 JSON 및 Text 레코드 값을 처리하도록 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-1029">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="5b408-1030">문제 https://github.com/Azure/azure-powershell/issues/7977 수정</span><span class="sxs-lookup"><span data-stu-id="5b408-1030">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="5b408-1031">문제 https://github.com/Azure/azure-powershell/issues/8600 수정</span><span class="sxs-lookup"><span data-stu-id="5b408-1031">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="5b408-1032">Start-AzAutomationDscCompilationJob에서 완료될 때까지 기다리지 않고 작업을 바로 시작하도록 변경했습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-1032">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="5b408-1033">문제 https://github.com/Azure/azure-powershell/issues/8347 수정</span><span class="sxs-lookup"><span data-stu-id="5b408-1033">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="5b408-1034">-Name을 사용하면 모든 노드를 반환하는 Get-AzAutomationDscNode 수정.</span><span class="sxs-lookup"><span data-stu-id="5b408-1034">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="5b408-1035">이제 일치하는 노드만 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-1035">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="5b408-1036">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="5b408-1036">Az.Compute</span></span>
* <span data-ttu-id="5b408-1037">ProtectFromScaleIn 및 ProtectFromScaleSetAction 매개 변수를 Update-AzVmssVM cmdlet에 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-1037">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="5b408-1038">'East US'(미국 동부)가 지원되지 않는 경우 이제 New-AzVM wimple 매개 변수 집합에서 기본적으로 사용 가능한 위치를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-1038">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="5b408-1039">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="5b408-1039">Az.DataLakeStore</span></span>
* <span data-ttu-id="5b408-1040">ADLS SDK에서 httpclient를 사용하도록 업데이트하고, 데이터 평면 테스트를 Azure 프레임워크와 통합합니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-1040">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="5b408-1041">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="5b408-1041">Az.Monitor</span></span>
* <span data-ttu-id="5b408-1042">도움말 예제에서 잘못된 매개 변수 이름을 수정했습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-1042">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="5b408-1043">Az.Network</span><span class="sxs-lookup"><span data-stu-id="5b408-1043">Az.Network</span></span>
* <span data-ttu-id="5b408-1044">DisableBgpRoutePropagation 플래그를 유효 경로 테이블 출력에 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-1044">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="5b408-1045">업데이트된 cmdlet:</span><span class="sxs-lookup"><span data-stu-id="5b408-1045">Updated cmdlet:</span></span>
        - <span data-ttu-id="5b408-1046">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="5b408-1046">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="5b408-1047">New-AzApplicationGatewayTrustedRootCertificate 설명서에서 이중 파선을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-1047">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="5b408-1048">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="5b408-1048">Az.Resources</span></span>
* <span data-ttu-id="5b408-1049">할당 거부를 검색하기 위한 새 Get-AzureRmDenyAssignment cmdlet을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-1049">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="5b408-1050">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="5b408-1050">Az.Sql</span></span>
* <span data-ttu-id="5b408-1051">Advanced Threat Protection cmdlet의 이름을 Advanced Data Security로 변경하고, 취약성 평가를 기본적으로 사용하도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-1051">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="5b408-1052">2.0.0 - 2019년 5월</span><span class="sxs-lookup"><span data-stu-id="5b408-1052">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="5b408-1053">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="5b408-1053">Az.Accounts</span></span>
* <span data-ttu-id="5b408-1054">사용자 이름/비밀번호 인증을 사용하여 ADFS 문제를 해결하도록 인증 라이브러리 업데이트</span><span class="sxs-lookup"><span data-stu-id="5b408-1054">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="5b408-1055">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="5b408-1055">Az.CognitiveServices</span></span>
* <span data-ttu-id="5b408-1056">Bing Search 서비스에 대해서만 Bing 면책 조항을 표시하세요.</span><span class="sxs-lookup"><span data-stu-id="5b408-1056">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="5b408-1057">계정 생성 실패 시 오류 개선.</span><span class="sxs-lookup"><span data-stu-id="5b408-1057">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="5b408-1058">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="5b408-1058">Az.Compute</span></span>
* <span data-ttu-id="5b408-1059">근접 배치 그룹 기능</span><span class="sxs-lookup"><span data-stu-id="5b408-1059">Proximity placement group feature.</span></span>
    - <span data-ttu-id="5b408-1060">다음과 같은 새 cmdlet을 추가했습니다.   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="5b408-1060">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="5b408-1061">새 매개 변수 ProximityPlacementGroupId가 다음 cmdlet에 추가됩니다.   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="5b408-1061">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="5b408-1062">New-AzGalleryImageVersion에 StorageAccountType 매개 변수가 추가됩니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-1062">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="5b408-1063">New-AzGalleryImageVersion의 TargetRegion이 StorageAccountType를 포함할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-1063">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="5b408-1064">SkipShutdown 스위치 매개 변수가 Stop-AzVM 및 Stop-AzVmss에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-1064">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>       
* <span data-ttu-id="5b408-1065">주요 변경 내용</span><span class="sxs-lookup"><span data-stu-id="5b408-1065">Breaking changes</span></span>
    - <span data-ttu-id="5b408-1066">Set-AzVMBootDiagnostics이 Set-AzVMBootDiagnostic으로 변경됩니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-1066">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="5b408-1067">Export-AzLogAnalyticThrottledRequests이 Export-AzLogAnalyticThrottledRequests로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-1067">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="5b408-1068">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="5b408-1068">Az.DeploymentManager</span></span>
* <span data-ttu-id="5b408-1069">Azure 배포 관리자 cmdlet의 일반적으로 사용 가능한 첫 번째 릴리스</span><span class="sxs-lookup"><span data-stu-id="5b408-1069">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="5b408-1070">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="5b408-1070">Az.Dns</span></span>
* <span data-ttu-id="5b408-1071">자동 DNS 이름 서버 위임</span><span class="sxs-lookup"><span data-stu-id="5b408-1071">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="5b408-1072">DNS 영역 만들기 cmdlet은 추가 선택적 매개 변수로 부모 영역 이름을 허용합니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-1072">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="5b408-1073">새로 생성 된 자식 영역의 부모 영역에 NS 레코드를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-1073">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="5b408-1074">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="5b408-1074">Az.FrontDoor</span></span>
* <span data-ttu-id="5b408-1075">Azure FrontDoor cmdlet의 일반적으로 사용 가능한 첫 번째 릴리스</span><span class="sxs-lookup"><span data-stu-id="5b408-1075">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="5b408-1076">'Waf'를 포함하도록 WAF cmdlet의 이름 바꾸기</span><span class="sxs-lookup"><span data-stu-id="5b408-1076">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="5b408-1077">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="5b408-1077">Az.HDInsight</span></span>
* <span data-ttu-id="5b408-1078">두 개의 cmdlet을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-1078">Removed two cmdlets:</span></span>
    - <span data-ttu-id="5b408-1079">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="5b408-1079">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="5b408-1080">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="5b408-1080">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="5b408-1081">Grant-AzHDInsightHttpServicesAccess를 대체할 새 cmdlet Set-AzHDInsightGatewayCredential을 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-1081">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="5b408-1082">reader 역할과 HDInsight 운영자 역할을 구분하도록 cmdlet Get-AzHDInsightJobOutput 업데이트:</span><span class="sxs-lookup"><span data-stu-id="5b408-1082">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="5b408-1083">reader 역할을 가진 사용자는 'DefaultStorageAccountKey'매개 변수를 명시적으로 지정해야 합니다. 그렇지 않으면 오류가 발생합니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-1083">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="5b408-1084">Hdinsight 운영자 역할을 가진 사용자를 영향을 받지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-1084">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="5b408-1085">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="5b408-1085">Az.Monitor</span></span>
* <span data-ttu-id="5b408-1086">SQR API(예약 쿼리 규칙)용 새 cmdlet</span><span class="sxs-lookup"><span data-stu-id="5b408-1086">New cmdlets for SQR API (Scheduled Query Rule)</span></span>  
    - <span data-ttu-id="5b408-1087">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="5b408-1087">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="5b408-1088">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="5b408-1088">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="5b408-1089">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="5b408-1089">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="5b408-1090">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="5b408-1090">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="5b408-1091">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="5b408-1091">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="5b408-1092">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="5b408-1092">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="5b408-1093">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="5b408-1093">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="5b408-1094">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="5b408-1094">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="5b408-1095">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="5b408-1095">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="5b408-1096">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="5b408-1096">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="5b408-1097">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="5b408-1097">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="5b408-1098">SQR API에 대한 [자세한 내용](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules)</span><span class="sxs-lookup"><span data-stu-id="5b408-1098">[More](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="5b408-1099">GenV2(비 클래식) 메트릭 기반 경고 규칙에 대한 cmdlet을 포함하도록 Az.Monitor.md가 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="5b408-1099">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="5b408-1100">Az.Network</span><span class="sxs-lookup"><span data-stu-id="5b408-1100">Az.Network</span></span>
* <span data-ttu-id="5b408-1101">Nat 게이트웨이 리소스에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="5b408-1101">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="5b408-1102">새 cmdlet</span><span class="sxs-lookup"><span data-stu-id="5b408-1102">New cmdlets</span></span>
        - <span data-ttu-id="5b408-1103">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="5b408-1103">New-AzNatGateway</span></span>
        - <span data-ttu-id="5b408-1104">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="5b408-1104">Get-AzNatGateway</span></span>
        - <span data-ttu-id="5b408-1105">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="5b408-1105">Set-AzNatGateway</span></span>
        - <span data-ttu-id="5b408-1106">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="5b408-1106">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="5b408-1107">다음 Cmdlet이 업데이트 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-1107">Updated cmdlets</span></span>
        - <span data-ttu-id="5b408-1108">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="5b408-1108">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="5b408-1109">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="5b408-1109">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="5b408-1110">기능에 대한 새로운 명령이 업데이트됨: Brooklyn Gateway에서 사용자 지정 경로 설정/제거.</span><span class="sxs-lookup"><span data-stu-id="5b408-1110">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="5b408-1111">New-AzVirtualNetworkGateway가 업데이트됨: 선택적 매개 변수 -CustomRoute를 추가하여 게이트웨이에서 설정할 사용자 지정 경로로 주소 접두사를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-1111">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="5b408-1112">Set-AzVirtualNetworkGateway가 업데이트됨: 선택적 매개 변수 -CustomRoute를 추가하여 게이트웨이에서 설정할 사용자 지정 경로로 주소 접두사를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-1112">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="5b408-1113">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="5b408-1113">Az.PolicyInsights</span></span>
* <span data-ttu-id="5b408-1114">정책 평가 세부 정보 쿼리 지원</span><span class="sxs-lookup"><span data-stu-id="5b408-1114">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="5b408-1115">Get-AzPolicyState에 '-Expand'매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="5b408-1115">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="5b408-1116">'-Expand PolicyEvaluationDetails' 지원</span><span class="sxs-lookup"><span data-stu-id="5b408-1116">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="5b408-1117">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="5b408-1117">Az.RecoveryServices</span></span>
* <span data-ttu-id="5b408-1118">크로스 구독 Azure에서 Azure 사이트 복구 지원</span><span class="sxs-lookup"><span data-stu-id="5b408-1118">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="5b408-1119">Azure Site Recovery에 대한 호환성이 손상되는 변경 표시</span><span class="sxs-lookup"><span data-stu-id="5b408-1119">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="5b408-1120">Azure Site Recovery 복구 계획 최종 실행 계획에 대한 수정</span><span class="sxs-lookup"><span data-stu-id="5b408-1120">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="5b408-1121">Azure에서 Azure에 대한 Azure Site Recovery 업데이트 네트워크 매핑 수정</span><span class="sxs-lookup"><span data-stu-id="5b408-1121">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="5b408-1122">관리 디스크에 대한 Azure에서 Azure에 대한 Azure Site Recovery 업데이트 보호 방향 수정</span><span class="sxs-lookup"><span data-stu-id="5b408-1122">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="5b408-1123">기타 사소한 수정.</span><span class="sxs-lookup"><span data-stu-id="5b408-1123">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="5b408-1124">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="5b408-1124">Az.Relay</span></span>
* <span data-ttu-id="5b408-1125">고객 관련 메시지의 철자 오류 수정</span><span class="sxs-lookup"><span data-stu-id="5b408-1125">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="5b408-1126">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="5b408-1126">Az.ServiceBus</span></span>
* <span data-ttu-id="5b408-1127">네임스페이스의 NetworkRuleSet에 대한 새 cmdlet가 추가되었습니다</span><span class="sxs-lookup"><span data-stu-id="5b408-1127">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="5b408-1128">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="5b408-1128">Az.Storage</span></span>
* <span data-ttu-id="5b408-1129">저장소 클라이언트 라이브러리 10.0.1로 업그레이드(이 SDK의 모든 개체의 네임스페이스가 'Microsoft.WindowsAzure.Storage. *'에서 'Microsoft.Azure.Storage.* '로 변경됨)</span><span class="sxs-lookup"><span data-stu-id="5b408-1129">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="5b408-1130">새로운 API 버전 2019-04-01을 지원하기 위해 Microsoft.Azure.Management.Storage 11.0.0으로 업그레이드합니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-1130">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="5b408-1131">스토리지 생성 계정의 기본 스토리지 계정 종류가 'Storage'에서 'StorageV2'로 변경됩니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-1131">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="5b408-1132">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="5b408-1132">New-AzStorageAccount</span></span>
* <span data-ttu-id="5b408-1133">'StandardLRS'가 'Standard_LRS'로 변경되는 것과 같이 '-'을 추가하여 입력 SkuName과 정렬되도록 스토리지 계정 cmdlet 출력 Sku.Name을 변경합니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-1133">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="5b408-1134">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="5b408-1134">New-AzStorageAccount</span></span>
    - <span data-ttu-id="5b408-1135">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="5b408-1135">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="5b408-1136">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="5b408-1136">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="5b408-1137">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="5b408-1137">Az.Websites</span></span>
* <span data-ttu-id="5b408-1138">Get-AzWebApp에서 반환한 PSSite 개체에 대해 'Kind'속성이 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-1138">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="5b408-1139">Get-AzWebApp\* 메트릭 및 Get-AzAppServicePlanMetrics가 사용되지 않음으로 표시되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-1139">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="5b408-1140">1.8.0 - 2019년 4월</span><span class="sxs-lookup"><span data-stu-id="5b408-1140">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="5b408-1141">마지막 주 릴리스 이후의 주요 사항</span><span class="sxs-lookup"><span data-stu-id="5b408-1141">Highlights since the last major release</span></span>
* <span data-ttu-id="5b408-1142">`Az` 모듈 일반 공급</span><span class="sxs-lookup"><span data-stu-id="5b408-1142">General availability of `Az` module</span></span>
* <span data-ttu-id="5b408-1143">`Az` 모듈에 대한 자세한 내용은 https://aka.ms/azps-announce 를 방문하세요.</span><span class="sxs-lookup"><span data-stu-id="5b408-1143">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="5b408-1144">Location, ResourceGroup 및 ResourceName 완성자가 추가되었습니다(https://azure.microsoft.com/blog/completers-in-azure-powershell/ ).</span><span class="sxs-lookup"><span data-stu-id="5b408-1144">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="5b408-1145">와일드카드 지원이 Az.Compute 및 Az.Network에 대한 Get cmdlet에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-1145">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="5b408-1146">Windows PowerShell 5.1 전용 대화형 사용자 이름/암호 인증이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-1146">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="5b408-1147">Python 2 Runbook 지원이 Az.Automation에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-1147">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="5b408-1148">Az.LogicApp: 통합 계정 어셈블리 및 일괄 처리 구성을 위한 새로운 cmdlet입니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-1148">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="5b408-1149">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="5b408-1149">Az.Accounts</span></span>
* <span data-ttu-id="5b408-1150">Mac에서 모듈을 올바르게 삭제하기 위해 Uninstall-AzureRm을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-1150">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="5b408-1151">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="5b408-1151">Az.Batch</span></span>
* <span data-ttu-id="5b408-1152">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-1152">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="5b408-1153">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="5b408-1153">Az.Cdn</span></span>
* <span data-ttu-id="5b408-1154">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-1154">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="5b408-1155">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="5b408-1155">Az.CognitiveServices</span></span>
* <span data-ttu-id="5b408-1156">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-1156">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="5b408-1157">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="5b408-1157">Az.Compute</span></span>
* <span data-ttu-id="5b408-1158">디스크의 리소스 ID에 리소스 ID의 소문자 resourcegroups가 있는 경우 AEM 설치 문제 수정</span><span class="sxs-lookup"><span data-stu-id="5b408-1158">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="5b408-1159">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-1159">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="5b408-1160">와일드 카드에 대한 설명서 수정</span><span class="sxs-lookup"><span data-stu-id="5b408-1160">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="5b408-1161">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="5b408-1161">Az.DataFactory</span></span>
* <span data-ttu-id="5b408-1162">NodeCount가 관리형 통합 런타임에 대해 Null이 아닌 경우 SsisProperties를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-1162">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="5b408-1163">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="5b408-1163">Az.DataLakeStore</span></span>
* <span data-ttu-id="5b408-1164">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-1164">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="5b408-1165">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="5b408-1165">Az.EventGrid</span></span>
* <span data-ttu-id="5b408-1166">이벤트 구독 cmdlet 만들기/업데이트를 사용하기 전에 리소스를 만들어야 함을 나타내기 위해 엔드포인트의 도움말 텍스트가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-1166">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="5b408-1167">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="5b408-1167">Az.EventHub</span></span>
* <span data-ttu-id="5b408-1168">네임스페이스의 NetworkRuleSet에 대한 새 cmdlet가 추가되었습니다</span><span class="sxs-lookup"><span data-stu-id="5b408-1168">Added new cmdlets for NetworkRuleSet of Namespace</span></span> 

#### <a name="azhdinsight"></a><span data-ttu-id="5b408-1169">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="5b408-1169">Az.HDInsight</span></span>
* <span data-ttu-id="5b408-1170">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-1170">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="5b408-1171">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="5b408-1171">Az.IotHub</span></span>
* <span data-ttu-id="5b408-1172">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-1172">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="5b408-1173">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="5b408-1173">Az.KeyVault</span></span>
* <span data-ttu-id="5b408-1174">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-1174">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="5b408-1175">와일드 카드에 대한 설명서 수정</span><span class="sxs-lookup"><span data-stu-id="5b408-1175">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="5b408-1176">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="5b408-1176">Az.MachineLearning</span></span>
* <span data-ttu-id="5b408-1177">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-1177">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="5b408-1178">Az.Media</span><span class="sxs-lookup"><span data-stu-id="5b408-1178">Az.Media</span></span>
* <span data-ttu-id="5b408-1179">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-1179">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="5b408-1180">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="5b408-1180">Az.Monitor</span></span>
  * <span data-ttu-id="5b408-1181">GenV2(비 클래식) 메트릭 기반 경고 규칙에 대한 새 cmdlet</span><span class="sxs-lookup"><span data-stu-id="5b408-1181">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="5b408-1182">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="5b408-1182">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="5b408-1183">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="5b408-1183">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="5b408-1184">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="5b408-1184">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="5b408-1185">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="5b408-1185">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="5b408-1186">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="5b408-1186">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="5b408-1187">모니터 SDK가 버전 0.22.0-preview로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-1187">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="5b408-1188">Az.Network</span><span class="sxs-lookup"><span data-stu-id="5b408-1188">Az.Network</span></span>
* <span data-ttu-id="5b408-1189">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-1189">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="5b408-1190">와일드 카드에 대한 설명서 수정</span><span class="sxs-lookup"><span data-stu-id="5b408-1190">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="5b408-1191">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="5b408-1191">Az.NotificationHubs</span></span>
* <span data-ttu-id="5b408-1192">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-1192">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="5b408-1193">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="5b408-1193">Az.OperationalInsights</span></span>
* <span data-ttu-id="5b408-1194">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-1194">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="5b408-1195">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="5b408-1195">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="5b408-1196">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-1196">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="5b408-1197">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="5b408-1197">Az.RecoveryServices</span></span>
* <span data-ttu-id="5b408-1198">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-1198">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="5b408-1199">Azure VM의 SQL용 테이블 형식이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-1199">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="5b408-1200">AzureFileShare에서 위치를 가져오는 대체 메서드가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-1200">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="5b408-1201">시간대에 따라 SchedulePolicy 개체의 ScheduleRunDays가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-1201">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="5b408-1202">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="5b408-1202">Az.RedisCache</span></span>
* <span data-ttu-id="5b408-1203">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-1203">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="5b408-1204">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="5b408-1204">Az.Resources</span></span>
* <span data-ttu-id="5b408-1205">와일드 카드에 대한 설명서 수정</span><span class="sxs-lookup"><span data-stu-id="5b408-1205">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="5b408-1206">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="5b408-1206">Az.Sql</span></span>
* <span data-ttu-id="5b408-1207">Monitor SDK의 종속성을 공용 코드로 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-1207">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="5b408-1208">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-1208">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="5b408-1209">다중 열 분류 프로세스가 향상되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-1209">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="5b408-1210">기본적으로 Get-AzSqlServerServiceObjective의 응답으로 SKU 속성(SKU 이름, 제품군, 용량)과 테이블 형식을 포함합니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-1210">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="5b408-1211">해당 지역에 기존 서버 없이 위치별로 Get-AzSqlServerServiceObjective를 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-1211">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="5b408-1212">관리형 인스턴스 생성 시 표준 시간대 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-1212">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="5b408-1213">와일드 카드에 대한 설명서 수정</span><span class="sxs-lookup"><span data-stu-id="5b408-1213">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="5b408-1214">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="5b408-1214">Az.Websites</span></span>
* <span data-ttu-id="5b408-1215">실행 시 태그를 제거하지 않도록 Set-AzWebApp 및 Set-AzWebAppSlot를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-1215">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="5b408-1216">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-1216">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="5b408-1217">WebSites SDK가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-1217">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="5b408-1218">PSAppServicePlan에서 AdminSiteName 속성을 제거했습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-1218">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="5b408-1219">1.7.0 - 2019년 4월</span><span class="sxs-lookup"><span data-stu-id="5b408-1219">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="5b408-1220">마지막 주 릴리스 이후의 주요 사항</span><span class="sxs-lookup"><span data-stu-id="5b408-1220">Highlights since the last major release</span></span>
* <span data-ttu-id="5b408-1221">`Az` 모듈 일반 공급</span><span class="sxs-lookup"><span data-stu-id="5b408-1221">General availability of `Az` module</span></span>
* <span data-ttu-id="5b408-1222">`Az` 모듈에 대한 자세한 내용은 https://aka.ms/azps-announce 를 방문하세요.</span><span class="sxs-lookup"><span data-stu-id="5b408-1222">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="5b408-1223">Location, ResourceGroup 및 ResourceName 완성자가 추가되었습니다(https://azure.microsoft.com/blog/completers-in-azure-powershell/ ).</span><span class="sxs-lookup"><span data-stu-id="5b408-1223">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="5b408-1224">와일드카드 지원이 Az.Compute 및 Az.Network에 대한 Get cmdlet에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-1224">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="5b408-1225">Windows PowerShell 5.1 전용 대화형 사용자 이름/암호 인증이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-1225">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="5b408-1226">Python 2 Runbook 지원이 Az.Automation에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-1226">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="5b408-1227">Az.LogicApp: 통합 계정 어셈블리 및 일괄 처리 구성을 위한 새로운 cmdlet입니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-1227">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="5b408-1228">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="5b408-1228">Az.Accounts</span></span>
* <span data-ttu-id="5b408-1229">매개 변수 AzureAnalysisServicesEndpointResourceId를 허용하도록 Add-AzEnvironment 및 Set-AzEnvironment 업데이트</span><span class="sxs-lookup"><span data-stu-id="5b408-1229">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="5b408-1230">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="5b408-1230">Az.AnalysisServices</span></span>
* <span data-ttu-id="5b408-1231">데이터 평면 cmdlet에서 ServiceClient 사용 및 원본 인증 논리 제거</span><span class="sxs-lookup"><span data-stu-id="5b408-1231">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="5b408-1232">호환성이 손상되는 변경을 방지하기 위해 Add-AzureASAccount를 Connect-AzAccount의 래퍼로 만듦</span><span class="sxs-lookup"><span data-stu-id="5b408-1232">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="5b408-1233">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="5b408-1233">Az.Automation</span></span>
* <span data-ttu-id="5b408-1234">포함에 대한 New-AzAutomationSoftwareUpdateConfiguration cmdlet 버그 수정</span><span class="sxs-lookup"><span data-stu-id="5b408-1234">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="5b408-1235">이제 매개 변수 IncludedKbNumber 및 IncludedPackageNameMask가 작동함</span><span class="sxs-lookup"><span data-stu-id="5b408-1235">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="5b408-1236">Azure 자동화 업데이트 관리 동적 그룹에 대한 버그 수정</span><span class="sxs-lookup"><span data-stu-id="5b408-1236">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="5b408-1237">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="5b408-1237">Az.Compute</span></span>
* <span data-ttu-id="5b408-1238">New-AzDiskConfig 및 New-AzSnapshotConfig에 HyperVGeneration 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="5b408-1238">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="5b408-1239">다른 테넌트의 갤러리 이미지를 사용하여 VM을 만들 수 있음</span><span class="sxs-lookup"><span data-stu-id="5b408-1239">Allow VM creation with galley image from other tenants.</span></span> 

#### <a name="azcontainerinstance"></a><span data-ttu-id="5b408-1240">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="5b408-1240">Az.ContainerInstance</span></span>
* <span data-ttu-id="5b408-1241">후행 빈 인수를 추가한 New-AzContainerGroup의 -Command 매개 변수의 문제 수정</span><span class="sxs-lookup"><span data-stu-id="5b408-1241">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="5b408-1242">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="5b408-1242">Az.DataFactory</span></span>
* <span data-ttu-id="5b408-1243">ADF .Net SDK 버전을 3.0.2로 업데이트</span><span class="sxs-lookup"><span data-stu-id="5b408-1243">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="5b408-1244">RepoConfiguration 관련 설정에 대한 추가 매개 변수로 Set-AzDataFactoryV2 cmdlet을 업데이트</span><span class="sxs-lookup"><span data-stu-id="5b408-1244">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="5b408-1245">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="5b408-1245">Az.Resources</span></span>
* <span data-ttu-id="5b408-1246">'-ResourceId' 또는 '-ResourceGroupName', '-Name' 및 '-ResourceType' 매개 변수를 제공할 때 'Get-AzResource'에 대한 공급자 처리 개선</span><span class="sxs-lookup"><span data-stu-id="5b408-1246">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="5b408-1247">'Test-AzDeployment' 및 'Test-AzResourceGroupDeployment'에 대한 오류 처리 개선</span><span class="sxs-lookup"><span data-stu-id="5b408-1247">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="5b408-1248">배포 유효성 검사 외부에서 발생한 오류를 처리하고 그 대신 명령의 출력에 포함</span><span class="sxs-lookup"><span data-stu-id="5b408-1248">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="5b408-1249">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/6856 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5b408-1249">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="5b408-1250">배포 cmdlet 세트에 스크립트 및 작업 시나리오에서 프롬프트를 건너뛰는 '-IgnoreDynamicParameters' 스위치 추가</span><span class="sxs-lookup"><span data-stu-id="5b408-1250">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="5b408-1251">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/6856 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5b408-1251">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="5b408-1252">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="5b408-1252">Az.Sql</span></span>
* <span data-ttu-id="5b408-1253">데이터베이스 데이터 분류 지원</span><span class="sxs-lookup"><span data-stu-id="5b408-1253">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="5b408-1254">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="5b408-1254">Az.Storage</span></span>
* <span data-ttu-id="5b408-1255">매개 변수 -UseConnectedAccount를 사용하여 스토리지 컨텍스트를 만들 때 자세한 오류 보고(단, 로그인 Azure 계정 없이)</span><span class="sxs-lookup"><span data-stu-id="5b408-1255">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="5b408-1256">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="5b408-1256">New-AzStorageContext</span></span>
* <span data-ttu-id="5b408-1257">관리 평면 API를 사용하여 지정한 스토리지 계정의 BLOB 서비스 속성 관리 지원</span><span class="sxs-lookup"><span data-stu-id="5b408-1257">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="5b408-1258">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="5b408-1258">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="5b408-1259">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="5b408-1259">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="5b408-1260">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="5b408-1260">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="5b408-1261">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="5b408-1261">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="5b408-1262">BLOB 및 파일 업로드/다운로드 cmdlet에 대한 -AsJob 지원</span><span class="sxs-lookup"><span data-stu-id="5b408-1262">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="5b408-1263">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="5b408-1263">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="5b408-1264">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="5b408-1264">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="5b408-1265">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="5b408-1265">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="5b408-1266">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="5b408-1266">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="5b408-1267">1.6.0 - 2019년 3월</span><span class="sxs-lookup"><span data-stu-id="5b408-1267">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="5b408-1268">마지막 주 릴리스 이후의 주요 사항</span><span class="sxs-lookup"><span data-stu-id="5b408-1268">Highlights since the last major release</span></span>
* <span data-ttu-id="5b408-1269">`Az` 모듈 일반 공급</span><span class="sxs-lookup"><span data-stu-id="5b408-1269">General availability of `Az` module</span></span>
* <span data-ttu-id="5b408-1270">`Az` 모듈에 대한 자세한 내용은 https://aka.ms/azps-announce 를 방문하세요.</span><span class="sxs-lookup"><span data-stu-id="5b408-1270">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="5b408-1271">Location, ResourceGroup 및 ResourceName 완성자가 추가되었습니다(https://azure.microsoft.com/blog/completers-in-azure-powershell/ ).</span><span class="sxs-lookup"><span data-stu-id="5b408-1271">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="5b408-1272">와일드카드 지원이 Az.Compute 및 Az.Network에 대한 Get cmdlet에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-1272">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="5b408-1273">Windows PowerShell 5.1 전용 대화형 사용자 이름/암호 인증이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-1273">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="5b408-1274">Python 2 Runbook 지원이 Az.Automation에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-1274">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="5b408-1275">Az.LogicApp: 통합 계정 어셈블리 및 일괄 처리 구성을 위한 새로운 cmdlet입니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-1275">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="5b408-1276">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="5b408-1276">Az.Automation</span></span>
* <span data-ttu-id="5b408-1277">Azure 자동화 업데이트 관리에서 변경된 지원 기능은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-1277">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="5b408-1278">동적 그룹화</span><span class="sxs-lookup"><span data-stu-id="5b408-1278">Dynamic grouping</span></span>
    * <span data-ttu-id="5b408-1279">사전 스크립트</span><span class="sxs-lookup"><span data-stu-id="5b408-1279">Pre-Post script</span></span>
    * <span data-ttu-id="5b408-1280">다시 부팅 설정</span><span class="sxs-lookup"><span data-stu-id="5b408-1280">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="5b408-1281">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="5b408-1281">Az.Compute</span></span>
* <span data-ttu-id="5b408-1282">Get-AzVmBootDiagnosticsData의 경로 확인 문제가 해결되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-1282">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="5b408-1283">Compute 클라이언트 라이브러리가 25.0.0으로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-1283">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="5b408-1284">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="5b408-1284">Az.KeyVault</span></span>
* <span data-ttu-id="5b408-1285">와일드카드 지원이 KeyVault cmdlet에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-1285">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="5b408-1286">Az.Network</span><span class="sxs-lookup"><span data-stu-id="5b408-1286">Az.Network</span></span>
* <span data-ttu-id="5b408-1287">Azure Firewall에 대한 위협 인텔리전스 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-1287">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="5b408-1288">Application Gateway 방화벽 정책의 최상위 수준 리소스 및 사용자 지정 규칙이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-1288">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="5b408-1289">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="5b408-1289">Az.RecoveryServices</span></span>
* <span data-ttu-id="5b408-1290">인스턴트 RP를 지원하기 위해 SnapshotRetentionInDays가 Azure VM 정책에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-1290">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="5b408-1291">컨테이너 등록을 취소하는 파이프 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-1291">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="5b408-1292">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="5b408-1292">Az.Resources</span></span>
* <span data-ttu-id="5b408-1293">Get-AzResource 및 Get-AzResourceGroup에 대한 와일드카드 지원을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-1293">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="5b408-1294">ARM에 대한 일반 호출을 수행할 때 사용되는 자격 증명을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-1294">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="5b408-1295">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="5b408-1295">Az.Sql</span></span>
* <span data-ttu-id="5b408-1296">위협 탐지의 cmdlet 매개 변수(ExcludeDetectionType)가 DetectionType에서 string[]으로 변경되어 새 DetectionType이 추가되면 이후의 증명이 되고 자동 완성도 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-1296">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="5b408-1297">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="5b408-1297">Az.Storage</span></span>
* <span data-ttu-id="5b408-1298">스토리지 계정에 대한 관리 정책 가져오기/설정/제거를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-1298">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="5b408-1299">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="5b408-1299">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="5b408-1300">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="5b408-1300">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="5b408-1301">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="5b408-1301">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="5b408-1302">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="5b408-1302">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="5b408-1303">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="5b408-1303">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="5b408-1304">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="5b408-1304">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="5b408-1305">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="5b408-1305">Az.Websites</span></span>
* <span data-ttu-id="5b408-1306">'New-AzWebApp -IncludeSourceWebAppSlots'를 사용하여 모든 슬롯의 복제를 중단하는 ARM 템플릿 버그가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-1306">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span> 

## <a name="150---march-2019"></a><span data-ttu-id="5b408-1307">1.5.0 - 2019년 3월</span><span class="sxs-lookup"><span data-stu-id="5b408-1307">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="5b408-1308">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="5b408-1308">Az.Accounts</span></span>
* <span data-ttu-id="5b408-1309">'Register-AzModule' 명령을 추가하여 AutoRest 생성 cmdlet을 지원</span><span class="sxs-lookup"><span data-stu-id="5b408-1309">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="5b408-1310">Connect-AzAccount 예제 업데이트</span><span class="sxs-lookup"><span data-stu-id="5b408-1310">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="5b408-1311">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="5b408-1311">Az.Automation</span></span>
* <span data-ttu-id="5b408-1312">몇몇 Azure Automation cmdlet에서 특정 월별 일정을 검색할 때 발생하는 문제 수정</span><span class="sxs-lookup"><span data-stu-id="5b408-1312">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="5b408-1313">상위 20개 노드를 반환하도록 Get-AzAutomationDscNode를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-1313">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="5b408-1314">이제 모든 노드 반환</span><span class="sxs-lookup"><span data-stu-id="5b408-1314">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="5b408-1315">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="5b408-1315">Az.Cdn</span></span>
* <span data-ttu-id="5b408-1316">사용자 지정 도메인 Https 사용/사용 안 함에 대한 새 Powershell cmdlet이 추가되었으며 기존의 것은 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-1316">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="5b408-1317">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="5b408-1317">Az.Compute</span></span>
* <span data-ttu-id="5b408-1318">Get cmdlet에 와일드 카드 지원 추가</span><span class="sxs-lookup"><span data-stu-id="5b408-1318">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="5b408-1319">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="5b408-1319">Az.DataFactory</span></span>
* <span data-ttu-id="5b408-1320">ADF.Net SDK 버전이 3.0.1로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-1320">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="5b408-1321">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="5b408-1321">Az.LogicApp</span></span>
* <span data-ttu-id="5b408-1322">첫 결과 페이지 검색 시에만 ListWorkflows 수정</span><span class="sxs-lookup"><span data-stu-id="5b408-1322">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="5b408-1323">Az.Network</span><span class="sxs-lookup"><span data-stu-id="5b408-1323">Az.Network</span></span>
* <span data-ttu-id="5b408-1324">Network cmdlet에 와일드 카드 지원 추가</span><span class="sxs-lookup"><span data-stu-id="5b408-1324">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="5b408-1325">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="5b408-1325">Az.RecoveryServices</span></span>
* <span data-ttu-id="5b408-1326">Azure VM 지원에 SQL 서버가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-1326">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="5b408-1327">SDK 업데이트</span><span class="sxs-lookup"><span data-stu-id="5b408-1327">SDK Update</span></span>
* <span data-ttu-id="5b408-1328">VMappContainer 체크 인 Get-ProtectableItem 제거</span><span class="sxs-lookup"><span data-stu-id="5b408-1328">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="5b408-1329">Get ProtectableItem의 매개 변수로 Name과 ServerName이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-1329">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="5b408-1330">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="5b408-1330">Az.Resources</span></span>
* <span data-ttu-id="5b408-1331">`-TemplateObject` 매개 변수를 추가하여 cmdlet을 배포</span><span class="sxs-lookup"><span data-stu-id="5b408-1331">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="5b408-1332">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/2933 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5b408-1332">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="5b408-1333">`Get-AzResource`의 결과를 `Set-AzResource`(으)로 파이프할 때 발생하는 문제 수정</span><span class="sxs-lookup"><span data-stu-id="5b408-1333">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="5b408-1334">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/8240 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5b408-1334">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="5b408-1335">실행 시 JSON 데이터 형식 문제 해결 `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="5b408-1335">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="5b408-1336">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/7930 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5b408-1336">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="5b408-1337">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="5b408-1337">Az.Sql</span></span>
* <span data-ttu-id="5b408-1338">AuditingEndpointsCommunicator를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-1338">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="5b408-1339">새 진단 설정을 생성할 때 에지 사례의 동작을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-1339">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="5b408-1340">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="5b408-1340">Az.Storage</span></span>
* <span data-ttu-id="5b408-1341">스토리지 계정      - New-AzStorageAccount를 생성할 때 종류 BlockBlobStorage를 지원</span><span class="sxs-lookup"><span data-stu-id="5b408-1341">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="5b408-1342">1.4.0 - 2019년 2월</span><span class="sxs-lookup"><span data-stu-id="5b408-1342">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="5b408-1343">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="5b408-1343">Az.AnalysisServices</span></span>
* <span data-ttu-id="5b408-1344">사용되지 않는 AddAzureASAccount cmdlet</span><span class="sxs-lookup"><span data-stu-id="5b408-1344">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="5b408-1345">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="5b408-1345">Az.Automation</span></span>
* <span data-ttu-id="5b408-1346">Import-AzAutomationDscNodeConfiguration 도움말 업데이트</span><span class="sxs-lookup"><span data-stu-id="5b408-1346">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="5b408-1347">Import-AzAutomationDscConfiguration cmdlet 구성 이름 유효성 검사 추가</span><span class="sxs-lookup"><span data-stu-id="5b408-1347">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="5b408-1348">Import-AzAutomationDscConfiguration cmdlet 오류 처리 개선</span><span class="sxs-lookup"><span data-stu-id="5b408-1348">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="5b408-1349">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="5b408-1349">Az.CognitiveServices</span></span>
* <span data-ttu-id="5b408-1350">리소스의 하위 도메인을 지정하는 데 사용되는 New-AzCognitiveServicesAccount에 대한 새 선택적 매개 변수로 CustomSubdomainName이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-1350">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="5b408-1351">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="5b408-1351">Az.Compute</span></span>
* <span data-ttu-id="5b408-1352">ID 매개 변수 집합 문제 해결</span><span class="sxs-lookup"><span data-stu-id="5b408-1352">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="5b408-1353">Name 매개 변수를 제공하지 않으면 Get-AzVMExtension이 설치된 모든 확장을 열거하도록 업데이트</span><span class="sxs-lookup"><span data-stu-id="5b408-1353">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="5b408-1354">Update-AzImage cmdlet에 태그 및 ResourceId 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="5b408-1354">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="5b408-1355">인스턴스 ID가 없는 Get-AzVmssVM과 InstanceView를 사용하면 인스턴스 보기가 있는 VMSS VM을 나열할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-1355">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="5b408-1356">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="5b408-1356">Az.DataLakeStore</span></span>
* <span data-ttu-id="5b408-1357">ADL 삭제된 항목 열거 및 복원에 대한 cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="5b408-1357">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="5b408-1358">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="5b408-1358">Az.EventHub</span></span>
* <span data-ttu-id="5b408-1359">Eventhub의 CaptureDescription 클래스에서 빈 보관을 건너뛰는 새 부울 속성 SkipEmptyArchives가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-1359">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span> 

#### <a name="azkeyvault"></a><span data-ttu-id="5b408-1360">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="5b408-1360">Az.KeyVault</span></span>
* <span data-ttu-id="5b408-1361">Set-AzKeyVaultSecret 태그 지정 수정</span><span class="sxs-lookup"><span data-stu-id="5b408-1361">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="5b408-1362">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="5b408-1362">Az.LogicApp</span></span>
* <span data-ttu-id="5b408-1363">통합 계정에 대한 기본 sku 추가</span><span class="sxs-lookup"><span data-stu-id="5b408-1363">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="5b408-1364">XSLT 2.0, XSLT 3.0, Liquid 맵 형식 추가</span><span class="sxs-lookup"><span data-stu-id="5b408-1364">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="5b408-1365">통합 계정 어셈블리에 대한 새 cmdlet</span><span class="sxs-lookup"><span data-stu-id="5b408-1365">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="5b408-1366">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="5b408-1366">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="5b408-1367">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="5b408-1367">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="5b408-1368">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="5b408-1368">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="5b408-1369">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="5b408-1369">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="5b408-1370">통합 계정 일괄 처리 구성에 대한 새 cmdlet</span><span class="sxs-lookup"><span data-stu-id="5b408-1370">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="5b408-1371">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="5b408-1371">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="5b408-1372">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="5b408-1372">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="5b408-1373">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="5b408-1373">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="5b408-1374">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="5b408-1374">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="5b408-1375">논리 앱 SDK를 버전 4.1.0으로 업데이트</span><span class="sxs-lookup"><span data-stu-id="5b408-1375">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="5b408-1376">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="5b408-1376">Az.Monitor</span></span>
* <span data-ttu-id="5b408-1377">Get-AzMetric에 대한 도움말 업데이트</span><span class="sxs-lookup"><span data-stu-id="5b408-1377">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="5b408-1378">Az.Network</span><span class="sxs-lookup"><span data-stu-id="5b408-1378">Az.Network</span></span>
* <span data-ttu-id="5b408-1379">Add-AzApplicationGatewayCustomError에 대한 도움말 예제 업데이트</span><span class="sxs-lookup"><span data-stu-id="5b408-1379">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="5b408-1380">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="5b408-1380">Az.OperationalInsights</span></span>
* <span data-ttu-id="5b408-1381">New 및 Get ApplicationInsights 데이터 소스에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="5b408-1381">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="5b408-1382">지정된 작업 영역에 대한 특정 또는 전체 ApplicationInsights 데이터 원본 가져오기를 지원하기 위한 새로운 'ApplicationInsights' 종류가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-1382">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span> 
    - <span data-ttu-id="5b408-1383">지정된 Application-Insights 리소스 매개 변수(구독 ID, resourceGroupName 및 이름)별로 데이터 원본을 만들기 위한 New-AzOperationalInsightsApplicationInsightsDataSource cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-1383">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span> 

#### <a name="azresources"></a><span data-ttu-id="5b408-1384">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="5b408-1384">Az.Resources</span></span>
* <span data-ttu-id="5b408-1385">문제 https://github.com/Azure/azure-powershell/issues/8166 수정</span><span class="sxs-lookup"><span data-stu-id="5b408-1385">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="5b408-1386">문제 https://github.com/Azure/azure-powershell/issues/8235 수정</span><span class="sxs-lookup"><span data-stu-id="5b408-1386">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="5b408-1387">문제 https://github.com/Azure/azure-powershell/issues/6219 수정</span><span class="sxs-lookup"><span data-stu-id="5b408-1387">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="5b408-1388">KeyCredentials 반복 만들기를 방지하기 위해 버그 수정</span><span class="sxs-lookup"><span data-stu-id="5b408-1388">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="5b408-1389">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="5b408-1389">Az.Sql</span></span>
* <span data-ttu-id="5b408-1390">SQL DB 하이퍼스케일에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="5b408-1390">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="5b408-1391">복원 요청에서 불필요한 속성을 설정하여 복원이 실패할 수 있는 버그 수정</span><span class="sxs-lookup"><span data-stu-id="5b408-1391">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="5b408-1392">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="5b408-1392">Az.Websites</span></span>
* <span data-ttu-id="5b408-1393">Get-AzWebAppSlotMetrics 내 올바른 예제</span><span class="sxs-lookup"><span data-stu-id="5b408-1393">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="5b408-1394">1.3.0 - 2019년 2월</span><span class="sxs-lookup"><span data-stu-id="5b408-1394">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="5b408-1395">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="5b408-1395">Az.Accounts</span></span>
* <span data-ttu-id="5b408-1396">ClientRuntime 최신 버전 업데이트</span><span class="sxs-lookup"><span data-stu-id="5b408-1396">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="5b408-1397">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="5b408-1397">Az.AnalysisServices</span></span>
<span data-ttu-id="5b408-1398">Az.AnalysisServices 모듈의 전반적인 가용성.</span><span class="sxs-lookup"><span data-stu-id="5b408-1398">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="5b408-1399">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="5b408-1399">Az.Compute</span></span>
* <span data-ttu-id="5b408-1400">AEM 확장: UltraSSD 및 P60, P70, P80 디스크에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="5b408-1400">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="5b408-1401">Set-AzVMBootDiagnostics에 대한 도움말 업데이트</span><span class="sxs-lookup"><span data-stu-id="5b408-1401">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="5b408-1402">Update-AzImage에 대한 도움말 및 예제 업데이트</span><span class="sxs-lookup"><span data-stu-id="5b408-1402">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="5b408-1403">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="5b408-1403">Az.RecoveryServices</span></span>
<span data-ttu-id="5b408-1404">Az.RecoveryServices 모듈의 전반적인 가용성.</span><span class="sxs-lookup"><span data-stu-id="5b408-1404">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="5b408-1405">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="5b408-1405">Az.Resources</span></span>
* <span data-ttu-id="5b408-1406">리소스 그룹 관련 태그 수정</span><span class="sxs-lookup"><span data-stu-id="5b408-1406">Fix tagging for resource groups</span></span> 
    - <span data-ttu-id="5b408-1407">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/8166 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5b408-1407">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="5b408-1408">`Get-AzureRmRoleAssignment`이(가) -ErrorAction을 준수하지 않는 문제 수정</span><span class="sxs-lookup"><span data-stu-id="5b408-1408">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span> 
    - <span data-ttu-id="5b408-1409">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/8235 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5b408-1409">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="5b408-1410">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="5b408-1410">Az.Sql</span></span>
* <span data-ttu-id="5b408-1411">AzSqlDatabaseBackupShortTermRetentionPolicy 가져오기/설정하기 추가</span><span class="sxs-lookup"><span data-stu-id="5b408-1411">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="5b408-1412">SQL cmdlet을 실행할 경우 Azure 계정에 로그인되어 있지 않은 것이 nullref 예외를 초래하는 문제 수정</span><span class="sxs-lookup"><span data-stu-id="5b408-1412">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="5b408-1413">Get-AzSqlCapability의 nullref 예외 수정</span><span class="sxs-lookup"><span data-stu-id="5b408-1413">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="5b408-1414">1.2.1 - 2019년 1월</span><span class="sxs-lookup"><span data-stu-id="5b408-1414">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="5b408-1415">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="5b408-1415">Az.Accounts</span></span>
* <span data-ttu-id="5b408-1416">올바른 인증 버전을 사용하여 릴리스</span><span class="sxs-lookup"><span data-stu-id="5b408-1416">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="5b408-1417">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="5b408-1417">Az.AnalysisServices</span></span>
* <span data-ttu-id="5b408-1418">업데이트된 인증 종속성을 사용하여 릴리스</span><span class="sxs-lookup"><span data-stu-id="5b408-1418">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="5b408-1419">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="5b408-1419">Az.RecoveryServices</span></span>
* <span data-ttu-id="5b408-1420">업데이트된 인증 종속성을 사용하여 릴리스</span><span class="sxs-lookup"><span data-stu-id="5b408-1420">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="5b408-1421">1.2.0 - 2019년 1월</span><span class="sxs-lookup"><span data-stu-id="5b408-1421">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="5b408-1422">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="5b408-1422">Az.Accounts</span></span>
* <span data-ttu-id="5b408-1423">Windows PowerShell 5.1 전용 대화형 사용자 이름/암호 인증 추가</span><span class="sxs-lookup"><span data-stu-id="5b408-1423">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="5b408-1424">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="5b408-1424">Update incorrect online help URLs</span></span>
* <span data-ttu-id="5b408-1425">Uninstall-AzureRm 관련 PS Core에 경고 메시지 추가</span><span class="sxs-lookup"><span data-stu-id="5b408-1425">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="5b408-1426">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="5b408-1426">Az.Aks</span></span>
* <span data-ttu-id="5b408-1427">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="5b408-1427">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="5b408-1428">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="5b408-1428">Az.Automation</span></span>
* <span data-ttu-id="5b408-1429">Python 2 Runbook에 대한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-1429">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="5b408-1430">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="5b408-1430">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="5b408-1431">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="5b408-1431">Az.Cdn</span></span>
* <span data-ttu-id="5b408-1432">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="5b408-1432">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="5b408-1433">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="5b408-1433">Az.Compute</span></span>
* <span data-ttu-id="5b408-1434">Invoke-AzVMReimage cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="5b408-1434">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="5b408-1435">Set-AzVmss에 TempDisk 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="5b408-1435">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="5b408-1436">New-AzVM 경고 메시지 수정</span><span class="sxs-lookup"><span data-stu-id="5b408-1436">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="5b408-1437">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="5b408-1437">Az.ContainerRegistry</span></span>
* <span data-ttu-id="5b408-1438">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="5b408-1438">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="5b408-1439">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="5b408-1439">Az.DataFactory</span></span>
* <span data-ttu-id="5b408-1440">ADF.Net SDK 버전이 3.0.0으로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-1440">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="5b408-1441">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="5b408-1441">Az.DataLakeStore</span></span>
* <span data-ttu-id="5b408-1442">MSI를 사용할 때 ADLS 엔드포인트 문제 수정</span><span class="sxs-lookup"><span data-stu-id="5b408-1442">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="5b408-1443">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/7462 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5b408-1443">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="5b408-1444">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="5b408-1444">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="5b408-1445">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="5b408-1445">Az.IotHub</span></span>
* <span data-ttu-id="5b408-1446">Add-IotHubRoutingEndpoint cmdlet에 인코딩 형식을 추가하세요.</span><span class="sxs-lookup"><span data-stu-id="5b408-1446">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="5b408-1447">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="5b408-1447">Az.KeyVault</span></span>
* <span data-ttu-id="5b408-1448">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="5b408-1448">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="5b408-1449">Az.Network</span><span class="sxs-lookup"><span data-stu-id="5b408-1449">Az.Network</span></span>
* <span data-ttu-id="5b408-1450">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="5b408-1450">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="5b408-1451">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="5b408-1451">Az.Resources</span></span>
* <span data-ttu-id="5b408-1452">'New-AzADAppCredential' 및 'New-AzADSpCredential' 참조 설명서의 잘못된 예제 수정</span><span class="sxs-lookup"><span data-stu-id="5b408-1452">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="5b408-1453">리소스 그룹 배포 cmdlet 실행 전 '-TemplateFile' 매개 변수 경로가 확인되지 않는 문제 수정</span><span class="sxs-lookup"><span data-stu-id="5b408-1453">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="5b408-1454">Az.Resources: New-AzureRmPolicyDefinition -Mode 기본값에 대한 올바른 설명서</span><span class="sxs-lookup"><span data-stu-id="5b408-1454">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="5b408-1455">Az.Resources: 문제 https://github.com/Azure/azure-powershell/issues/7522 수정</span><span class="sxs-lookup"><span data-stu-id="5b408-1455">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="5b408-1456">Az.Resources: 문제 https://github.com/Azure/azure-powershell/issues/5747 수정</span><span class="sxs-lookup"><span data-stu-id="5b408-1456">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="5b408-1457">'PSResourceGroupDeployment' 개체의 서식 문제 수정</span><span class="sxs-lookup"><span data-stu-id="5b408-1457">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="5b408-1458">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/2123 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5b408-1458">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="5b408-1459">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="5b408-1459">Az.ServiceFabric</span></span>
* <span data-ttu-id="5b408-1460">인증서가 VMSS 모델에 추가되었는데도 예외가 발생할 경우 롤백합니다. 이는 버그 https://github.com/Azure/service-fabric-issues/issues/932 를 수정하기 위함입니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-1460">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="5b408-1461">일부 오류 메시지를 수정하세요.</span><span class="sxs-lookup"><span data-stu-id="5b408-1461">Fix some error messages.</span></span>
* <span data-ttu-id="5b408-1462">Az로의 마이그레이션을 통해서는 작동하지 않는 New-AzServiceFabriCluster를 위해 기본값 ARM 템플릿을 가진 클러스터 만들기를 수정하세요.</span><span class="sxs-lookup"><span data-stu-id="5b408-1462">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="5b408-1463">확장에서 클러스터 id를 확인하여 클러스터에 해당하는 VMSS에만 추가되도록 클러스터/애플리케이션 인증서 추가를 수정하세요.</span><span class="sxs-lookup"><span data-stu-id="5b408-1463">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="5b408-1464">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="5b408-1464">Az.SignalR</span></span>
* <span data-ttu-id="5b408-1465">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="5b408-1465">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="5b408-1466">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="5b408-1466">Az.Sql</span></span>
* <span data-ttu-id="5b408-1467">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="5b408-1467">Update incorrect online help URLs</span></span>
* <span data-ttu-id="5b408-1468">가능한 값을 가진 LicenseType 매개 변수에 대한 매개 변수 설명이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-1468">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="5b408-1469">유일하게 업데이트된 속성인데 작동하지 않는 관리되는 인스턴스 ID의 업데이트 수정</span><span class="sxs-lookup"><span data-stu-id="5b408-1469">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="5b408-1470">관리되는 인스턴스에서의 사용자 지정 데이터 정렬에 대한 지원</span><span class="sxs-lookup"><span data-stu-id="5b408-1470">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="5b408-1471">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="5b408-1471">Az.Storage</span></span>
* <span data-ttu-id="5b408-1472">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="5b408-1472">Update incorrect online help URLs</span></span>
* <span data-ttu-id="5b408-1473">Premium Storage 계정이 클래식 로깅/메트릭을 지원하지 않기 때문에, Premium Storage 계정의 클래식 로깅/메트릭을 가져올/설정할 때 상세한 오류 메시지를 제공해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-1473">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="5b408-1474">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="5b408-1474">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="5b408-1475">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="5b408-1475">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="5b408-1476">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="5b408-1476">Az.TrafficManager</span></span>
* <span data-ttu-id="5b408-1477">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="5b408-1477">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="5b408-1478">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="5b408-1478">Az.Websites</span></span>
* <span data-ttu-id="5b408-1479">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="5b408-1479">Update incorrect online help URLs</span></span>
* <span data-ttu-id="5b408-1480">앱이 ASE에 호스팅되면 'New-AzWebAppSSLBinding'을 수정하여 올바른 resourcegroup+location에 인증서를 업로드합니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-1480">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="5b408-1481">'New-AzWebAppSSLBinding'을 수정하여 SSL 인증서를 앱에 바인딩하는 데 붙는 태그를 덮어쓰지 않도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-1481">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="5b408-1482">1.1.0 - 2019년 1월</span><span class="sxs-lookup"><span data-stu-id="5b408-1482">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="5b408-1483">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="5b408-1483">Az.Accounts</span></span>
* <span data-ttu-id="5b408-1484">Enable-AzureRmAlias에 'Local' 범위 추가</span><span class="sxs-lookup"><span data-stu-id="5b408-1484">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="5b408-1485">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="5b408-1485">Az.Compute</span></span>
* <span data-ttu-id="5b408-1486">이름이 Restart/Start/Stop/Remove/Set-AzVM과 Save-AzVMImage에 설정된 ID 매개 변수에서 선택 사항이 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-1486">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="5b408-1487">도움말 파일의 ID에 대한 설명이 업데이트 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-1487">Updated the description of ID in help files</span></span>
* <span data-ttu-id="5b408-1488">Az.Accounts 모듈을 사용할 때의 이전 버전과의 호환성 문제를 해결합니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-1488">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="5b408-1489">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="5b408-1489">Az.DataLakeStore</span></span>
* <span data-ttu-id="5b408-1490">SDK 수정을 위해 데이터 평면의 SDK 버전을 1.1.14로 업데이트하세요.</span><span class="sxs-lookup"><span data-stu-id="5b408-1490">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="5b408-1491">getfilestatus 및 liststatus에 대한 음수 acesstime 및 modificationtime 수정, 비동기 취소 토큰 수정</span><span class="sxs-lookup"><span data-stu-id="5b408-1491">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="5b408-1492">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="5b408-1492">Az.EventGrid</span></span>
* <span data-ttu-id="5b408-1493">2019-01-01 API 버전을 사용하도록 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-1493">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="5b408-1494">2019-01-01 API 버전에서 새 시나리오를 지원하도록 다음 cmdlet을 업데이트</span><span class="sxs-lookup"><span data-stu-id="5b408-1494">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="5b408-1495">New-AzureRmEventGridSubscription: 지정을 위한 새로운 선택적 매개 변수를 추가</span><span class="sxs-lookup"><span data-stu-id="5b408-1495">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="5b408-1496">이벤트 Time-to-Live</span><span class="sxs-lookup"><span data-stu-id="5b408-1496">Event Time-To-Live,</span></span>
        - <span data-ttu-id="5b408-1497">이벤트에 대한 최대 배달 시도</span><span class="sxs-lookup"><span data-stu-id="5b408-1497">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="5b408-1498">배달 못한 편지의 엔드포인트입니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-1498">Dead letter endpoint.</span></span>
    - <span data-ttu-id="5b408-1499">Update-AzureRmEventGridSubscription: 지정을 위한 새로운 선택적 매개 변수를 추가</span><span class="sxs-lookup"><span data-stu-id="5b408-1499">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="5b408-1500">이벤트 Time-to-Live</span><span class="sxs-lookup"><span data-stu-id="5b408-1500">Event Time-To-Live,</span></span>
        - <span data-ttu-id="5b408-1501">이벤트에 대한 최대 배달 시도</span><span class="sxs-lookup"><span data-stu-id="5b408-1501">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="5b408-1502">배달 못한 편지의 엔드포인트입니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-1502">Dead letter endpoint.</span></span>
* <span data-ttu-id="5b408-1503">New-AzureRmEventGridSubscription 및 Update-AzureRmEventGridSubscription cmdlet의 EndpointType 옵션에 새 열거형 값(즉, storageQueue 및 hybridConnection)을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-1503">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="5b408-1504">이벤트 구독을 생성 또는 업데이트할 때 사용자가 직접 조치를 취해야 할 경우 경고 메시지를 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-1504">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="5b408-1505">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="5b408-1505">Az.IotHub</span></span>
* <span data-ttu-id="5b408-1506">최신 버전의 Azure IotHub SDK로 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="5b408-1506">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="5b408-1507">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="5b408-1507">Az.LogicApp</span></span>
* <span data-ttu-id="5b408-1508">지정된 이름이 없는 모든 Get-AzLogicApp 목록</span><span class="sxs-lookup"><span data-stu-id="5b408-1508">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="5b408-1509">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="5b408-1509">Az.Resources</span></span>
* <span data-ttu-id="5b408-1510">'Get-AzResource'에 '-ODataQuery'및 '-ResourceId' 매개 변수를 제공할 때 매개 변수 집합 문제 수정</span><span class="sxs-lookup"><span data-stu-id="5b408-1510">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="5b408-1511">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/7875 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5b408-1511">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="5b408-1512">New/Set-AzPolicyDefinition에서 -Custom 매개 변수 처리 문제 수정</span><span class="sxs-lookup"><span data-stu-id="5b408-1512">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="5b408-1513">New-AzDeployment 설명서에서 오타 수정</span><span class="sxs-lookup"><span data-stu-id="5b408-1513">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="5b408-1514">'New-AzADUser'에 '-MailNickname'매개 변수가 필수 항목으로 지정됨</span><span class="sxs-lookup"><span data-stu-id="5b408-1514">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="5b408-1515">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/8220 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5b408-1515">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="5b408-1516">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="5b408-1516">Az.SignalR</span></span>
* <span data-ttu-id="5b408-1517">Az.Accounts 모듈을 사용할 때의 이전 버전과의 호환성 문제를 해결합니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-1517">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="5b408-1518">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="5b408-1518">Az.Sql</span></span>
* <span data-ttu-id="5b408-1519">Storage 관리 클라이언트 종속성을 일반적인 SDK 구현으로 변환했습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-1519">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="5b408-1520">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="5b408-1520">Az.Storage</span></span>
* <span data-ttu-id="5b408-1521">Sas Token, OAuth 또는 Anonymous를 사용하여 스토리지 컨텍스트의 StorageAccountName을 실제 스토리지 계정 이름으로 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-1521">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="5b408-1522">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="5b408-1522">New-AzStorageContext</span></span>
* <span data-ttu-id="5b408-1523">'-FullUri' 매개 변수를 사용하여 Blob 스냅샷 개체의 Sas Token을 생성하고 반환된 Uri를 스냅샷 Uri로 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-1523">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="5b408-1524">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="5b408-1524">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="5b408-1525">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="5b408-1525">Az.Websites</span></span>
* <span data-ttu-id="5b408-1526">'Get-AzDeletedWebApp'의 날짜 구문 분석 버그를 수정했습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-1526">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="5b408-1527">Az.Accounts 모듈을 사용할 때의 이전 버전과의 호환성 문제를 해결합니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-1527">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="5b408-1528">1.0.0 - 2018년 12월</span><span class="sxs-lookup"><span data-stu-id="5b408-1528">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="5b408-1529">일반</span><span class="sxs-lookup"><span data-stu-id="5b408-1529">General</span></span>

- <span data-ttu-id="5b408-1530">Az 모듈 일반 공급</span><span class="sxs-lookup"><span data-stu-id="5b408-1530">General Availability of Az Module</span></span>
- <span data-ttu-id="5b408-1531">각 모듈에 대 한 온라인 도움말</span><span class="sxs-lookup"><span data-stu-id="5b408-1531">Online help for each module</span></span>
- <span data-ttu-id="5b408-1532">자세한 내용과 로드맵은 [Az 알림 페이지](https://aka.ms/azps-announce)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5b408-1532">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="5b408-1533">AzureRM에서 마이그레이션하는 것에 대한 정보는 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5b408-1533">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="5b408-1534">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="5b408-1534">Az.Accounts</span></span>
- <span data-ttu-id="5b408-1535">Az.Profile에서 변경</span><span class="sxs-lookup"><span data-stu-id="5b408-1535">Changed from Az.Profile</span></span>
- <span data-ttu-id="5b408-1536">프로필 및 컨텍스트 형식에 대한 표 형식 수정</span><span class="sxs-lookup"><span data-stu-id="5b408-1536">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="5b408-1537">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="5b408-1537">Az.ApiManagement</span></span>
- <span data-ttu-id="5b408-1538">#7002에 대한 수정</span><span class="sxs-lookup"><span data-stu-id="5b408-1538">Fixes for #7002</span></span>
- <span data-ttu-id="5b408-1539">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5b408-1539">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="5b408-1540">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="5b408-1540">Az.Batch</span></span>
- <span data-ttu-id="5b408-1541">`PSComputeNode`의 새로운 `NodeAgentInformation` 속성을 통해 풀의 각 VM에서 실행 중인 Azure Batch 노드 에이전트의 버전을 확인하는 기능이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-1541">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="5b408-1542">`PSDataDisk`에 대한 `Caching` 기본 값은 이제 `None` 대신 `ReadWrite`입니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-1542">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="5b408-1543">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5b408-1543">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="5b408-1544">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="5b408-1544">Az.Billing</span></span>
- <span data-ttu-id="5b408-1545">청구, 소비 및 UsageAggregates cmdlet 결합 cmdlet에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5b408-1545">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="5b408-1546">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="5b408-1546">Az.CognitivServices</span></span>
- <span data-ttu-id="5b408-1547">New-AzureRmCognitiveServicesAccount 작업에서 사용 가능한 SkuName 및 Typem에 대한 완성자 추가</span><span class="sxs-lookup"><span data-stu-id="5b408-1547">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="5b408-1548">Get-AzCognitiveServicesAccountSkus에서 GetSkusWithAccountParamSetName 매개 변수 집합을 제거</span><span class="sxs-lookup"><span data-stu-id="5b408-1548">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="5b408-1549">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="5b408-1549">Az.ContainerInstance</span></span>
- <span data-ttu-id="5b408-1550">ManagedIdentity 지원이 추가됨</span><span class="sxs-lookup"><span data-stu-id="5b408-1550">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="5b408-1551">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="5b408-1551">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="5b408-1552">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5b408-1552">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="5b408-1553">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="5b408-1553">Az.DataLakeStore</span></span>
- <span data-ttu-id="5b408-1554">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5b408-1554">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="5b408-1555">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="5b408-1555">Az.Monitor</span></span>
- <span data-ttu-id="5b408-1556">Az.Monitor 이름 변경 및 기타 사소한 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5b408-1556">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="5b408-1557">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="5b408-1557">Az.KeyVault</span></span>
- <span data-ttu-id="5b408-1558">출력 형식에서 사용되지 않는 'PurgeDisabled' 속성 제거</span><span class="sxs-lookup"><span data-stu-id="5b408-1558">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="5b408-1559">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="5b408-1559">Az.MachineLearning</span></span>
- <span data-ttu-id="5b408-1560">Az.MachineLearningCompute 모듈의 cmdlet 포함</span><span class="sxs-lookup"><span data-stu-id="5b408-1560">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="5b408-1561">Az.Media</span><span class="sxs-lookup"><span data-stu-id="5b408-1561">Az.Media</span></span>
- <span data-ttu-id="5b408-1562">New-AzMediaService에서 사용되지 않는 -Tags 별칭이 제거됨</span><span class="sxs-lookup"><span data-stu-id="5b408-1562">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="5b408-1563">Az.Network</span><span class="sxs-lookup"><span data-stu-id="5b408-1563">Az.Network</span></span>
<span data-ttu-id="5b408-1564">Application Gateway에서 RewriteRuleSets를 구성하는 것에 대한 지원이 추가됨</span><span class="sxs-lookup"><span data-stu-id="5b408-1564">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="5b408-1565">추가된 새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-1565">New cmdlets added:</span></span>
        - <span data-ttu-id="5b408-1566">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="5b408-1566">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="5b408-1567">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="5b408-1567">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="5b408-1568">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="5b408-1568">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="5b408-1569">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="5b408-1569">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="5b408-1570">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="5b408-1570">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="5b408-1571">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="5b408-1571">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="5b408-1572">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="5b408-1572">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="5b408-1573">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="5b408-1573">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="5b408-1574">선택적 매개 변수를 사용하도록 cmdlet이 업데이트됨 -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="5b408-1574">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="5b408-1575">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5b408-1575">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="5b408-1576">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="5b408-1576">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="5b408-1577">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="5b408-1577">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="5b408-1578">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="5b408-1578">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="5b408-1579">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="5b408-1579">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="5b408-1580">New-AzureRmApplicationGatewayUrlPathMapConfig로 ID를 사용하여 Application Gateway에 KeyVault 지원을 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-1580">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="5b408-1581">선택적 매개 변수를 사용하도록 cmdlet이 업데이트됨 -KeyVaultSecretId, -KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="5b408-1581">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="5b408-1582">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="5b408-1582">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="5b408-1583">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="5b408-1583">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="5b408-1584">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="5b408-1584">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="5b408-1585">New-AzApplicationGateway cmdlet이 선택적 매개 변수를 사용하도록 업데이트됨 -UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="5b408-1585">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="5b408-1586">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5b408-1586">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="5b408-1587">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="5b408-1587">Az.OperationalInsights</span></span>
- <span data-ttu-id="5b408-1588">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5b408-1588">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="5b408-1589">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="5b408-1589">Az.Profile</span></span>
- <span data-ttu-id="5b408-1590">Az.Accounts에 모듈 이름이 변경됨</span><span class="sxs-lookup"><span data-stu-id="5b408-1590">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="5b408-1591">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="5b408-1591">Az.RecoveryServices</span></span>
- <span data-ttu-id="5b408-1592">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5b408-1592">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="5b408-1593">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="5b408-1593">Az.Resources</span></span>
- <span data-ttu-id="5b408-1594">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5b408-1594">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="5b408-1595">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="5b408-1595">Az.ServiceFabric</span></span>
- <span data-ttu-id="5b408-1596">일반 이름과 지문으로 지정 인증서 지원</span><span class="sxs-lookup"><span data-stu-id="5b408-1596">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="5b408-1597">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5b408-1597">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="5b408-1598">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="5b408-1598">Az.SIgnalR</span></span>
- <span data-ttu-id="5b408-1599">SIgnalR에 대한 PowerShell cmdlet에 대한 일반 공급</span><span class="sxs-lookup"><span data-stu-id="5b408-1599">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="5b408-1600">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="5b408-1600">Az.Sql</span></span>
- <span data-ttu-id="5b408-1601">위협 탐지의 cmdlet에 새로운 Data_Exfiltration 및 Unsafe_Action 검색 유형 추가</span><span class="sxs-lookup"><span data-stu-id="5b408-1601">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="5b408-1602">Sql 감사 cmdlet에 대한 설명서 예제 업데이트</span><span class="sxs-lookup"><span data-stu-id="5b408-1602">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="5b408-1603">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5b408-1603">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="5b408-1604">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="5b408-1604">Az.Storage</span></span>
- <span data-ttu-id="5b408-1605">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5b408-1605">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="5b408-1606">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="5b408-1606">Az.Websites</span></span>
- <span data-ttu-id="5b408-1607">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5b408-1607">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="5b408-1608">0.7.0 - 2018년 12월</span><span class="sxs-lookup"><span data-stu-id="5b408-1608">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="5b408-1609">일반</span><span class="sxs-lookup"><span data-stu-id="5b408-1609">General</span></span>

* <span data-ttu-id="5b408-1610">AzureRM에서 Az 전환 예정에 대한 사소한 변경</span><span class="sxs-lookup"><span data-stu-id="5b408-1610">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="5b408-1611">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="5b408-1611">Az.Compute</span></span>

* <span data-ttu-id="5b408-1612">`New-AzVm(ss)` cmdlet에 대한 간단한 매개 변수 집합에 UltraSSD 및 갤러리 이미지에 대한 지원을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-1612">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="5b408-1613">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="5b408-1613">Az.DataLakeStore</span></span>

* <span data-ttu-id="5b408-1614">ADLS 계정의 도메인의 후행 슬래시를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-1614">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="5b408-1615">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="5b408-1615">Az.FrontDoor</span></span>

* <span data-ttu-id="5b408-1616">일부 끊어진 링크 수정</span><span class="sxs-lookup"><span data-stu-id="5b408-1616">Fixed some broken links</span></span>
    - <span data-ttu-id="5b408-1617">New-AzureRmFrontDoor 및 Set-AzureRmFrontDoor 아티클에서 New-AzureRmFrontDoorHealthProbeSettingObject cmdlet 아티클에 대한 링크가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-1617">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="5b408-1618">New-AzureRmFrontDoorManagedRuleObject 아티클에서 New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet 아티클에 대한 링크가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-1618">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="5b408-1619">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="5b408-1619">Az.RecoveryServices</span></span>

* <span data-ttu-id="5b408-1620">Azure File Share 복원 작업에 클라이언트 측 유효성 검사가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-1620">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="5b408-1621">afs 복원의 경우 storageAccountName 및 storageAccountResourceGroupName을 선택적으로 만들었습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-1621">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="5b408-1622">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="5b408-1622">Az.Resources</span></span>

* <span data-ttu-id="5b408-1623">에 대 한 수정 https://github.com/Azure/azure-powershell/issues/7679</span><span class="sxs-lookup"><span data-stu-id="5b408-1623">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="5b408-1624">기본 관리자를 요청할 때 구독 범위가 제공되는 경우 Get-AzureRmRoleAssignment를 업데이트하여 구독 범위를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-1624">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="5b408-1625">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="5b408-1625">Az.Sql</span></span>

* <span data-ttu-id="5b408-1626">AzureRM에서 Az 전환 예정에 대한 사소한 변경</span><span class="sxs-lookup"><span data-stu-id="5b408-1626">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="5b408-1627">DotNet 코어에서 Get-AzureRmSqlDatabaseVulnerabilityAssessment를 사용하는 문제 해결</span><span class="sxs-lookup"><span data-stu-id="5b408-1627">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="5b408-1628">SQL 감사 cmdlet과 관련된 도움말 메시지의 설명서가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-1628">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="5b408-1629">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="5b408-1629">Az.Storage</span></span>

* <span data-ttu-id="5b408-1630">New-AzureRmStorageAccount에 -EnableHierarchicalNamespace 추가</span><span class="sxs-lookup"><span data-stu-id="5b408-1630">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="5b408-1631">파일 복사 cmdlet이 -DestContext 입력이 없을 때 대상의 원본 컨텍스트를 다시 사용할 수 없는 문제 수정</span><span class="sxs-lookup"><span data-stu-id="5b408-1631">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="5b408-1632">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="5b408-1632">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="5b408-1633">고정적인 웹 사이트 구성 지원</span><span class="sxs-lookup"><span data-stu-id="5b408-1633">Support Static Website configuration</span></span>
    - <span data-ttu-id="5b408-1634">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="5b408-1634">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="5b408-1635">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="5b408-1635">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="5b408-1636">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="5b408-1636">Az.Websites</span></span>

* <span data-ttu-id="5b408-1637">Set-AzureRmWebApp 및 Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="5b408-1637">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span> 
    - <span data-ttu-id="5b408-1638">Windows 및 Linux 컨테이너 응용 프로그램에 탑재할 Azure Storage 경로를 지정하기 위해 새 매개 변수(-AzureStoragePath)가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-1638">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="5b408-1639">새 cmdlet New-AzureRmWebAppAzureStoragePath의 출력을 매개 변수로 사용하여 Azure Storage 경로를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-1639">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="5b408-1640">0.6.1 - 2018년 11월</span><span class="sxs-lookup"><span data-stu-id="5b408-1640">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="5b408-1641">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="5b408-1641">Az.ApiManagement</span></span>
* <span data-ttu-id="5b408-1642">형식 매핑 문제에 대한 종속성 업데이트</span><span class="sxs-lookup"><span data-stu-id="5b408-1642">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="5b408-1643">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="5b408-1643">Az.Automation</span></span>
* <span data-ttu-id="5b408-1644">Azure Automation cmdlet 기반 Swagger</span><span class="sxs-lookup"><span data-stu-id="5b408-1644">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="5b408-1645">업데이트 관리 cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="5b408-1645">Added Update Management cmdlets</span></span>
* <span data-ttu-id="5b408-1646">소스 제어 cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="5b408-1646">Added Source Control cmdlets</span></span>
* <span data-ttu-id="5b408-1647">Remove-AzureRmAutomationHybridWorkerGroup cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="5b408-1647">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="5b408-1648">DSC 노드 등록 명령 수정</span><span class="sxs-lookup"><span data-stu-id="5b408-1648">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="5b408-1649">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="5b408-1649">Az.Compute</span></span>
* <span data-ttu-id="5b408-1650">SystemAssigned ID에 대한 ID 문제 수정</span><span class="sxs-lookup"><span data-stu-id="5b408-1650">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="5b408-1651">형식 매핑 문제에 대한 종속성 업데이트</span><span class="sxs-lookup"><span data-stu-id="5b408-1651">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="5b408-1652">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="5b408-1652">Az.ContainerInstance</span></span>
* <span data-ttu-id="5b408-1653">형식 매핑 문제에 대한 종속성 업데이트</span><span class="sxs-lookup"><span data-stu-id="5b408-1653">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="5b408-1654">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="5b408-1654">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="5b408-1655">마켓플레이스 cmdlet에 대한 예제 설명 업데이트</span><span class="sxs-lookup"><span data-stu-id="5b408-1655">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="5b408-1656">Az.Network</span><span class="sxs-lookup"><span data-stu-id="5b408-1656">Az.Network</span></span>
* <span data-ttu-id="5b408-1657">New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="5b408-1657">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="5b408-1658">지원되는 AzureFirewall 네트워크 프로토콜에 ICMP 다시 추가</span><span class="sxs-lookup"><span data-stu-id="5b408-1658">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="5b408-1659">Test-AzureRmNetworkWatcherConnectivity cmdlet을 업데이트하여 대상 ID, 주소 및 포트 유효성 검사를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-1659">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span> 
* <span data-ttu-id="5b408-1660">VirtualNetwork 맵의 메모리 사용 문제 해결</span><span class="sxs-lookup"><span data-stu-id="5b408-1660">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="5b408-1661">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="5b408-1661">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="5b408-1662">보호된 파일 공유에 대한 정책을 수정하는 것에 대해 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-1662">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="5b408-1663">정책 표준 시간대를 대문자로 변환했습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-1663">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="5b408-1664">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="5b408-1664">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="5b408-1665">New-AzureRmRecoveryServicesAsrProtectableItem의 예제 정정</span><span class="sxs-lookup"><span data-stu-id="5b408-1665">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="5b408-1666">형식 매핑 문제에 대한 종속성 업데이트</span><span class="sxs-lookup"><span data-stu-id="5b408-1666">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="5b408-1667">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="5b408-1667">Az.Relay</span></span>
* <span data-ttu-id="5b408-1668">선택적 매개 변수 -KeyValue를 New-AzureRmRelayKey cmdlet에 추가하여 사용자가 KeyValue를 제공할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-1668">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="5b408-1669">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="5b408-1669">Az.Resources</span></span>
* <span data-ttu-id="5b408-1670">`New-AzureRmPolicyAssignment` 및 `Set-AzureRmPolicyAssignment`의 자원 ID 관련 매개 변수에 대한 도움말 문서를 업데이트함</span><span class="sxs-lookup"><span data-stu-id="5b408-1670">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="5b408-1671">-Metadata를 사용하는 New-AzureRmPolicyDefinition에 대한 예제 추가</span><span class="sxs-lookup"><span data-stu-id="5b408-1671">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="5b408-1672">NetStandard의 태그 키에서 대소문자 보존을 허용하도록 수정: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="5b408-1672">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="5b408-1673">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="5b408-1673">Az.ServiceFabric</span></span>
* <span data-ttu-id="5b408-1674">향후 호환성이 손상되는 변경에 대한 사용 중단 메시지 추가</span><span class="sxs-lookup"><span data-stu-id="5b408-1674">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="5b408-1675">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="5b408-1675">Az.Sql</span></span>
* <span data-ttu-id="5b408-1676">Azure Sql Database Managed Instance 및 Azure Sql Managed Database에 CRUD 작업을 위한 새 cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="5b408-1676">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="5b408-1677">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="5b408-1677">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="5b408-1678">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="5b408-1678">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="5b408-1679">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="5b408-1679">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="5b408-1680">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="5b408-1680">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="5b408-1681">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="5b408-1681">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="5b408-1682">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="5b408-1682">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="5b408-1683">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="5b408-1683">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="5b408-1684">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="5b408-1684">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="5b408-1685">서버 또는 데이터베이스에서 확장 감사 정책 관리를 활성화했습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-1685">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="5b408-1686">새 매개 변수(PredicateExpression)가 감사 로그 필터링을 사용하도록 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-1686">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="5b408-1687">Cmdlet이 레거시 클라이언트 대신 SQL 클라이언트를 사용하도록 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-1687">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="5b408-1688">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="5b408-1688">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="5b408-1689">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="5b408-1689">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="5b408-1690">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="5b408-1690">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="5b408-1691">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="5b408-1691">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="5b408-1692">스토리지 계정 이름 매개 변수가 설정된 Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings를 사용할 때의 문제 해결</span><span class="sxs-lookup"><span data-stu-id="5b408-1692">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="5b408-1693">0.5.0 - 2018년 11월</span><span class="sxs-lookup"><span data-stu-id="5b408-1693">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="5b408-1694">일반</span><span class="sxs-lookup"><span data-stu-id="5b408-1694">General</span></span>
* <span data-ttu-id="5b408-1695">많은 핵심 cmdlet에 Resource Completers를 추가하여 대화형으로 cmdlet을 호출할 때 기존 리소스 이름을 탭으로 이동할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-1695">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="5b408-1696">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="5b408-1696">Az.Profile</span></span>
* <span data-ttu-id="5b408-1697">ClientRuntime의 최신 버전을 사용하도록 일반적인 코드를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-1697">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="5b408-1698">Connect-AzAccount cmdlet의 매개 변수 TenantId 이름을 Tenant로 바꾸고 TenantId의 별칭을 추가합니다</span><span class="sxs-lookup"><span data-stu-id="5b408-1698">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="5b408-1699">Connect-AzAccount의 업데이트된 TenantId 설명</span><span class="sxs-lookup"><span data-stu-id="5b408-1699">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="5b408-1700">테넌트 도메인을 제공할 때 실패한 로그인에 대한 오류 메시지 수정</span><span class="sxs-lookup"><span data-stu-id="5b408-1700">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="5b408-1701">테넌트에 구독이 없는 계정의 컨텍스트 이름 충돌 문제 수정</span><span class="sxs-lookup"><span data-stu-id="5b408-1701">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="5b408-1702">MSI를 사용할 때 DataLake 엔드포인트 문제 수정</span><span class="sxs-lookup"><span data-stu-id="5b408-1702">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="5b408-1703">연결되지 않은 경우 'Disconnect-AzAccount'가 throw하는 문제 수정</span><span class="sxs-lookup"><span data-stu-id="5b408-1703">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="5b408-1704">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="5b408-1704">Az.CognitiveServices</span></span>
* <span data-ttu-id="5b408-1705">Get-AzCognitiveServicesAccountSkus 작업을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-1705">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="5b408-1706">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="5b408-1706">Az.Compute</span></span>
* <span data-ttu-id="5b408-1707">Add-AzVmssVMDataDisk 및 Remove-AzVmssVMDataDisk cmdlet를 추가합니다</span><span class="sxs-lookup"><span data-stu-id="5b408-1707">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="5b408-1708">Get-AzVMImage는 AutomaticOSUpgradeProperties를 표시합니다</span><span class="sxs-lookup"><span data-stu-id="5b408-1708">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="5b408-1709">수정된 SetAzVMChefExtension -BootstrapOptions 및 -JsonAttribute option 값이 json 형식으로 설정하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-1709">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="5b408-1710">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="5b408-1710">Az.DataLakeStore</span></span>
* <span data-ttu-id="5b408-1711">DataLake 패키지를 1.1.10으로 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-1711">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="5b408-1712">기본 동시성을 다중 스레드 작업에 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-1712">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="5b408-1713">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="5b408-1713">Az.Insights</span></span>
* <span data-ttu-id="5b408-1714">해결된 문제 #7267(자동 크기 조정 영역)</span><span class="sxs-lookup"><span data-stu-id="5b408-1714">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="5b408-1715">열거된 매개 변수를 제대로 설정하지 않은 새 자동 크기 조정 규칙을 만드는 데 문제가 있습니다(이를 항상 기본값으로 설정함).</span><span class="sxs-lookup"><span data-stu-id="5b408-1715">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="5b408-1716">해결된 문제 # 7513[자세한 정보] Set-AzDiagnosticSetting은 설정을 생성하는 동안 범주를 명시적으로 지정해야 합니다</span><span class="sxs-lookup"><span data-stu-id="5b408-1716">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="5b408-1717">이제 cmdlet은 생성 중에 사용할 범주를 명시적으로 표시할 필요가 없습니다. 즉, 문서화된대로 작동합니다</span><span class="sxs-lookup"><span data-stu-id="5b408-1717">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="5b408-1718">Az.Network</span><span class="sxs-lookup"><span data-stu-id="5b408-1718">Az.Network</span></span>
* <span data-ttu-id="5b408-1719">다음 cmdlet에 대해 PeeringType을 필수 매개 변수로 변경했습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-1719">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="5b408-1720">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="5b408-1720">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="5b408-1721">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="5b408-1721">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="5b408-1722">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="5b408-1722">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="5b408-1723">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="5b408-1723">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="5b408-1724">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="5b408-1724">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="5b408-1725">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="5b408-1725">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="5b408-1726">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="5b408-1726">Az.PolicyInsights</span></span>
* <span data-ttu-id="5b408-1727">추가된 정책 재구성 cmdlet</span><span class="sxs-lookup"><span data-stu-id="5b408-1727">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="5b408-1728">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="5b408-1728">Az.Resources</span></span>
* <span data-ttu-id="5b408-1729">에 대 한 수정 https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="5b408-1729">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="5b408-1730">'Get-AzResource'에 대해 '-ResourceId' 매개 변수를 사용하여 리소스 나열 허용</span><span class="sxs-lookup"><span data-stu-id="5b408-1730">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="5b408-1731">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="5b408-1731">Az.ServiceBus</span></span>
* <span data-ttu-id="5b408-1732">마이그레이션 상태를 알 수 있도록 PSServiceBusMigrationConfigurationAttributes에 MigrationState 읽기 전용 속성 추가.</span><span class="sxs-lookup"><span data-stu-id="5b408-1732">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="5b408-1733">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="5b408-1733">Az.ServiceFabric</span></span>
* <span data-ttu-id="5b408-1734">Linux Vmss에 인증서 추가 수정.</span><span class="sxs-lookup"><span data-stu-id="5b408-1734">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="5b408-1735">Add-AzServiceFabricClusterCertificate 수정</span><span class="sxs-lookup"><span data-stu-id="5b408-1735">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="5b408-1736">새 인증서(Azure/service-fabric-issues#932)에서 올바른 지문을 사용.</span><span class="sxs-lookup"><span data-stu-id="5b408-1736">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="5b408-1737">올바르게 예외 표시(Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="5b408-1737">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="5b408-1738">Vmss CreateOrUpdate 작업을 시작하기 전에 'Update-AzServiceFabricDurability'를 수정하여 클러스터 구성 업데이트.</span><span class="sxs-lookup"><span data-stu-id="5b408-1738">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="5b408-1739">0.4.0 - 2018년 10월</span><span class="sxs-lookup"><span data-stu-id="5b408-1739">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="5b408-1740">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="5b408-1740">Az.Profile</span></span>
* <span data-ttu-id="5b408-1741">CloudShell에서 Get-AzSubscription을 사용하여 문제를 해결합니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-1741">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="5b408-1742">ClientRuntime의 최신 버전을 사용하도록 일반적인 코드를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-1742">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="5b408-1743">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="5b408-1743">Az.Compute</span></span>
* <span data-ttu-id="5b408-1744">'New-AzVm'에 대해 간단한 매개 변수를 사용하는 경우 가속화된 네트워킹을 설정하기 위해 새 크기가 VM 크기의 허용 목록에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-1744">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="5b408-1745">모든 cmdlet에 ResourceName 인수 완성자가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-1745">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="5b408-1746">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="5b408-1746">Az.DataLakeStore</span></span>
* <span data-ttu-id="5b408-1747">Virtual Network 규칙에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="5b408-1747">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="5b408-1748">Get-AzDataLakeStoreVirtualNetworkRule: Azure Data Lake Store 가상 네트워크 규칙을 가져오거나 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-1748">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="5b408-1749">Add-AzDataLakeStoreVirtualNetworkRule: 지정된 Data Lake Store 계정에 가상 네트워크 규칙을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-1749">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="5b408-1750">Set-AzDataLakeStoreVirtualNetworkRule: 지정된 Data Lake Store 계정에 지정된 가상 네트워크 규칙을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-1750">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="5b408-1751">Remove-AzDataLakeStoreVirtualNetworkRule: Azure Data Lake Store 가상 네트워크 규칙을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-1751">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="5b408-1752">Az.Network</span><span class="sxs-lookup"><span data-stu-id="5b408-1752">Az.Network</span></span>
* <span data-ttu-id="5b408-1753">Test-AzNetworkWatcherConnectivity cmdlet을 업데이트하고, 백 엔드에 프로토콜 값을 전달합니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-1753">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="5b408-1754">모든 cmdlet에 ResourceName 인수 완성자가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-1754">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="5b408-1755">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="5b408-1755">Az.Resources</span></span>
* <span data-ttu-id="5b408-1756">(기본 프로필에 구독이 없고 범위가 지정되지 않은 경우) 시나리오에서 의미 있는 예외를 추가하여 Get-AzRoleDefinition이 인식할 수 없는 예외를 throw하는 문제를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-1756">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="5b408-1757">또한 기본 매개 변수 집합을 'RoleDefinitionNameParameterSet'으로 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-1757">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="5b408-1758">0.3.0 - 2018년 10월</span><span class="sxs-lookup"><span data-stu-id="5b408-1758">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="5b408-1759">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="5b408-1759">Azure.Storage</span></span>
* <span data-ttu-id="5b408-1760">대상에 메타데이터가 있을 때 Blob/파일이 메타 데이터를 복사하지 않는 문제 수정</span><span class="sxs-lookup"><span data-stu-id="5b408-1760">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="5b408-1761">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="5b408-1761">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="5b408-1762">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="5b408-1762">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="5b408-1763">특정 위치의 스토리지 리소스 사용을 지원하고 글로벌 스토리지 리소스 사용 가져오기는 더 이상 사용되지 않는다는 경고 메시지를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-1763">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="5b408-1764">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="5b408-1764">Get-AzStorageUsage</span></span>
    
#### <a name="azcognitiveservices"></a><span data-ttu-id="5b408-1765">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="5b408-1765">Az.CognitiveServices</span></span>
* <span data-ttu-id="5b408-1766">기존 계정이 없는 Get-AzCognitiveServicesAccountSkus를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-1766">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="5b408-1767">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="5b408-1767">Az.Compute</span></span>
* <span data-ttu-id="5b408-1768">Get-AzVM -ResourceGroupName <rg>가 필요한 경우 50개가 넘는 결과를 반환하도록 수정</span><span class="sxs-lookup"><span data-stu-id="5b408-1768">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="5b408-1769">'SimpleParameterSet' 예제가 New-AzVmss cmdlet 도움말에 추가됨</span><span class="sxs-lookup"><span data-stu-id="5b408-1769">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="5b408-1770">Azure Disk Encryption 진행률 메시지의 오타를 수정</span><span class="sxs-lookup"><span data-stu-id="5b408-1770">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="5b408-1771">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="5b408-1771">Az.DataFactoryV2</span></span>
* <span data-ttu-id="5b408-1772">ADF.Net SDK 버전을 2.3.0으로 업데이트</span><span class="sxs-lookup"><span data-stu-id="5b408-1772">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="5b408-1773">Az.Network</span><span class="sxs-lookup"><span data-stu-id="5b408-1773">Az.Network</span></span>
* <span data-ttu-id="5b408-1774">NetworkProfile 기능 추가</span><span class="sxs-lookup"><span data-stu-id="5b408-1774">Added NetworkProfile functionality.</span></span> <span data-ttu-id="5b408-1775">추가된 새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-1775">new cmdlets added</span></span>
    - <span data-ttu-id="5b408-1776">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="5b408-1776">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="5b408-1777">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="5b408-1777">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="5b408-1778">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="5b408-1778">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="5b408-1779">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="5b408-1779">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="5b408-1780">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="5b408-1780">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="5b408-1781">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="5b408-1781">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="5b408-1782">서브넷 모델에 서비스 연결 링크 추가</span><span class="sxs-lookup"><span data-stu-id="5b408-1782">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="5b408-1783">New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="5b408-1783">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="5b408-1784">Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="5b408-1784">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="5b408-1785">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="5b408-1785">Az.RedisCache</span></span>
* <span data-ttu-id="5b408-1786">모든 문자열을 Size 매개 변수로 진행되도록 허용</span><span class="sxs-lookup"><span data-stu-id="5b408-1786">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="5b408-1787">PSArgumentCompleter 팝업에 P5 추가</span><span class="sxs-lookup"><span data-stu-id="5b408-1787">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="5b408-1788">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="5b408-1788">Az.Resources</span></span>
* <span data-ttu-id="5b408-1789">-Mode 매개 변수를 Set-AzPolicyDefinition에 추가</span><span class="sxs-lookup"><span data-stu-id="5b408-1789">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="5b408-1790">사용자가 포함된 Origin 작업에서 Get-AzProviderOperation commandlet 버그 수정</span><span class="sxs-lookup"><span data-stu-id="5b408-1790">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="5b408-1791">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="5b408-1791">Az.Sql</span></span>
* <span data-ttu-id="5b408-1792">일부 백업 cmdlet이 현재 azure 구독을 인식하지 않는 문제 해결</span><span class="sxs-lookup"><span data-stu-id="5b408-1792">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="5b408-1793">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="5b408-1793">Az.Websites</span></span>
* <span data-ttu-id="5b408-1794">새 cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - 컨테이너 지속적인 배포 Webhook URL을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-1794">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="5b408-1795">새 cmdlet New-AzWebAppContainerPSSession 및 Enter-WebAppContainerPSSession -  windows 컨테이너 앱에 PowerShell 원격 세션을 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="5b408-1795">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="5b408-1796">0.2.0 - 2018년 9월</span><span class="sxs-lookup"><span data-stu-id="5b408-1796">0.2.0 - September 2018</span></span>
 <span data-ttu-id="5b408-1797">최초 릴리스</span><span class="sxs-lookup"><span data-stu-id="5b408-1797">Initial Release</span></span>
