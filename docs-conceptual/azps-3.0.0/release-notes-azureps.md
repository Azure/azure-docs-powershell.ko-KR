---
title: Azure PowerShell 릴리스 정보
description: Azure PowerShell 모듈의 모든 최신 업데이트에 대해 알아봅니다.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 10/15/2019
ms.openlocfilehash: ee3f54e6bc15dbbaeb97cad7463cb1d2e5795e3e
ms.sourcegitcommit: 05431341858d10eb9c345213275c3ccc24c83c9b
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/13/2019
ms.locfileid: "74062142"
---
## <a name="300---november-2019"></a><span data-ttu-id="7ea64-103">3.0.0 - 2019년 11월</span><span class="sxs-lookup"><span data-stu-id="7ea64-103">3.0.0 - November 2019</span></span>
### <a name="general"></a><span data-ttu-id="7ea64-104">일반</span><span class="sxs-lookup"><span data-stu-id="7ea64-104">General</span></span>
* <span data-ttu-id="7ea64-105">Az.PrivateDns 1.0.0 릴리스</span><span class="sxs-lookup"><span data-stu-id="7ea64-105">Az.PrivateDns 1.0.0 released</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="7ea64-106">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="7ea64-106">Az.Accounts</span></span>
* <span data-ttu-id="7ea64-107">'Resolve-Error' 별칭에 사용 중단 메시지를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-107">Add a deprecation message for 'Resolve-Error' alias.</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="7ea64-108">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="7ea64-108">Az.Advisor</span></span>
* <span data-ttu-id="7ea64-109">Get-AzAdvisorRecommendation cmdlet에 새로운 '운영 효율성' 범주가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-109">Added new category 'Operational Excellence' to Get-AzAdvisorRecommendation cmdlet.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="7ea64-110">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="7ea64-110">Az.Batch</span></span>
* <span data-ttu-id="7ea64-111">`BatchAccountContext`의 `CoreQuota` 이름이 `DedicatedCoreQuota`로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-111">Renamed `CoreQuota` on `BatchAccountContext` to `DedicatedCoreQuota`.</span></span> <span data-ttu-id="7ea64-112">또한 `LowPriorityCoreQuota`가 새로 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-112">There is also a new `LowPriorityCoreQuota`.</span></span>
  - <span data-ttu-id="7ea64-113">이 변경 사항은 **Get-AzBatchAccount**에 영향을 줍니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-113">This impacts **Get-AzBatchAccount**.</span></span>
* <span data-ttu-id="7ea64-114">이제 **New-AzBatchTask** `-ResourceFile` 매개 변수는 새로운 **New-AzBatchResourceFile** cmdlet을 사용하여 구성할 수 있는 `PSResourceFile` 개체의 컬렉션을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-114">**New-AzBatchTask** `-ResourceFile` parameter now takes a collection of `PSResourceFile` objects, which can be constructed using the new **New-AzBatchResourceFile** cmdlet.</span></span>
* <span data-ttu-id="7ea64-115">새로운 **New-AzBatchResourceFile** cmdlet을 통해 `PSResourceFile` 개체를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-115">New **New-AzBatchResourceFile** cmdlet to help create `PSResourceFile` objects.</span></span> <span data-ttu-id="7ea64-116">이들은 `-ResourceFile` 매개 변수의 **New-AzBatchTask**에 제공될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-116">These can be supplied to **New-AzBatchTask** on the `-ResourceFile` parameter.</span></span>
  - <span data-ttu-id="7ea64-117">그에 따라 기존 `HttpUrl` 방법 외에도 두 가지 종류의 리소스 파일이 새롭게 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-117">This supports two new kinds of resource file in addition to the existing `HttpUrl` way:</span></span>
    - <span data-ttu-id="7ea64-118">`AutoStorageContainerName` 기반 리소스 파일은 전체 자동 스토리지 컨테이너를 일괄 처리 노드에 다운로드합니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-118">`AutoStorageContainerName` based resource files download an entire auto-storage container to the Batch node.</span></span>
    - <span data-ttu-id="7ea64-119">`StorageContainerUrl` 기반 리소스 파일은 URL에 지정된 컨테이너를 일괄 처리 노드에 다운로드합니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-119">`StorageContainerUrl` based resource files download the container specified in the URL to the Batch node.</span></span>
* <span data-ttu-id="7ea64-120">**Get-AzBatchApplication**으로 반환되는 `PSApplication`의 `ApplicationPackages` 속성이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-120">Removed `ApplicationPackages` property of `PSApplication` returned by **Get-AzBatchApplication**.</span></span>
  - <span data-ttu-id="7ea64-121">이제 **Get-AzBatchApplicationPackage**를 사용하여 애플리케이션 내부의 특정 패키지를 검색할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-121">The specific packages inside of an application now can be retrieved using **Get-AzBatchApplicationPackage**.</span></span> <span data-ttu-id="7ea64-122">예: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`</span><span class="sxs-lookup"><span data-stu-id="7ea64-122">For example: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span></span>
* <span data-ttu-id="7ea64-123">**Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication** 및 **Set-AzBatchApplication**에서 `ApplicationId` 이름이 `ApplicationName`으로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-123">Renamed `ApplicationId` to `ApplicationName` on **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication**, and **Set-AzBatchApplication**.</span></span>
  - <span data-ttu-id="7ea64-124">이제 `ApplicationId`는 `ApplicationName`의 별칭입니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-124">`ApplicationId` now is an alias of `ApplicationName`.</span></span>
* <span data-ttu-id="7ea64-125">새로운 `PSWindowsUserConfiguration` 속성이 `PSUserAccount`에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-125">Added new `PSWindowsUserConfiguration` property to `PSUserAccount`.</span></span>
* <span data-ttu-id="7ea64-126">`PSApplicationPackage`에서 `Version` 이름이 `Name`으로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-126">Renamed `Version` to `Name` on `PSApplicationPackage`.</span></span>
* <span data-ttu-id="7ea64-127">`PSResourceFile`에서 `BlobSource` 이름이 `HttpUrl`로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-127">Renamed `BlobSource` to `HttpUrl` on `PSResourceFile`.</span></span>
* <span data-ttu-id="7ea64-128">`PSVirtualMachineConfiguration`에서 `OSDisk` 속성이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-128">Removed `OSDisk` property from `PSVirtualMachineConfiguration`.</span></span>
* <span data-ttu-id="7ea64-129">**Set-AzBatchPoolOSVersion**이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-129">Removed **Set-AzBatchPoolOSVersion**.</span></span> <span data-ttu-id="7ea64-130">이 작업은 더 이상 지원되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-130">This operation is no longer supported.</span></span>
* <span data-ttu-id="7ea64-131">`PSCloudServiceConfiguration`에서 `TargetOSVersion`이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-131">Removed `TargetOSVersion` from `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="7ea64-132">`PSCloudServiceConfiguration`에서 `CurrentOSVersion` 이름이 `OSVersion`으로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-132">Renamed `CurrentOSVersion` to `OSVersion` on `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="7ea64-133">`PSPoolUsageMetrics`에서 `DataEgressGiB` 및 `DataIngressGiB`가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-133">Removed `DataEgressGiB` and `DataIngressGiB` from `PSPoolUsageMetrics`.</span></span>
* <span data-ttu-id="7ea64-134">**Get-AzBatchNodeAgentSku**가 제거되고 **Get-AzBatchSupportedImage**로 대체되었습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-134">Removed **Get-AzBatchNodeAgentSku** and replaced it with  **Get-AzBatchSupportedImage**.</span></span> 
  - <span data-ttu-id="7ea64-135">**Get-AzBatchSupportedImage**가 **Get-AzBatchNodeAgentSku**와 동일한 데이터를 반환하지만 더 친숙한 형식이 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-135">**Get-AzBatchSupportedImage** returns the same data as **Get-AzBatchNodeAgentSku** but in a more friendly format.</span></span>
  - <span data-ttu-id="7ea64-136">이제 확인되지 않은 이미지도 새롭게 반환됩니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-136">New non-verified images are also now returned.</span></span> <span data-ttu-id="7ea64-137">각 이미지의 `Capabilities` 및 `BatchSupportEndOfLife`에 대한 추가 정보도 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-137">Additional information about `Capabilities` and `BatchSupportEndOfLife` for each image is also included.</span></span>
* <span data-ttu-id="7ea64-138">**New-AzBatchPool**의 새로운 `MountConfiguration` 매개 변수를 통해 풀의 각 노드에서 원격 파일 시스템을 마운트할 수 있는 기능이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-138">Added ability to mount remote file-systems on each node of a pool via the new `MountConfiguration` parameter of **New-AzBatchPool**.</span></span>
* <span data-ttu-id="7ea64-139">이제 트래픽의 소스 포트를 기준으로 풀에 대한 네트워크 액세스를 차단하는 네트워크 보안 규칙이 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-139">Now support network security rules blocking network access to a pool based on the source port of the traffic.</span></span> <span data-ttu-id="7ea64-140">이 작업은 `PSNetworkSecurityGroupRule`에서 `SourcePortRanges` 속성을 통해 수행됩니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-140">This is done via the `SourcePortRanges` property on `PSNetworkSecurityGroupRule`.</span></span>
* <span data-ttu-id="7ea64-141">컨테이너를 실행할 때 Batch는 이제 컨테이너 작업 디렉터리 또는 일괄 처리 태스크 작업 디렉터리에서 작업 실행을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-141">When running a container, Batch now supports executing the task in the container working directory or in the Batch task working directory.</span></span> <span data-ttu-id="7ea64-142">이 작업은 `PSTaskContainerSettings`에서 `WorkingDirectory` 속성에 의해 제어됩니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-142">This is controlled by the `WorkingDirectory` property on `PSTaskContainerSettings`.</span></span>
* <span data-ttu-id="7ea64-143">새로운 `PublicIPs` 속성을 통해 `PSNetworkConfiguration`에서 공용 IP의 컬렉션을 지정할 수 있는 기능이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-143">Added ability to specify a collection of public IPs on `PSNetworkConfiguration` via the new `PublicIPs` property.</span></span> <span data-ttu-id="7ea64-144">그 결과 사용자 제공 IP 목록의 IP가 풀에 있는 노드에 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-144">This guarantees nodes in the Pool will have an IP from the list user provided IPs.</span></span>
* <span data-ttu-id="7ea64-145">지정하지 않은 경우 이제 `PSSTartTask`에서 `WaitForSuccess`의 기본값은 `$True`입니다(이전에는 `$False`).</span><span class="sxs-lookup"><span data-stu-id="7ea64-145">When not specified, the default value of `WaitForSuccess` on `PSSTartTask` is now `$True` (was `$False`).</span></span>
* <span data-ttu-id="7ea64-146">지정하지 않은 경우 이제 `PSAutoUserSpecification`에서 `Scope`의 기본값은 `Pool`입니다(이전에는 Windows의 경우 `Task`, Linux의 경우에는 `Pool`).</span><span class="sxs-lookup"><span data-stu-id="7ea64-146">When not specified, the default value of `Scope` on `PSAutoUserSpecification` is now `Pool` (was `Task` on Windows and `Pool` on Linux).</span></span>

#### <a name="azcdn"></a><span data-ttu-id="7ea64-147">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="7ea64-147">Az.Cdn</span></span>
* <span data-ttu-id="7ea64-148">RulesEngine에 UrlRewriteAction 및 CacheKeyQueryStringAction이 도입되었습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-148">Introduced UrlRewriteAction and CacheKeyQueryStringAction to RulesEngine.</span></span>
* <span data-ttu-id="7ea64-149">New-AzDeliveryRuleCondition cmdlet에서 'Selector' 입력 누락과 같은 여러 버그가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-149">Fixed several bugs like missing 'Selector' Input in New-AzDeliveryRuleCondition cmdlet.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7ea64-150">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7ea64-150">Az.Compute</span></span>
* <span data-ttu-id="7ea64-151">디스크 암호화 집합 기능</span><span class="sxs-lookup"><span data-stu-id="7ea64-151">Disk Encryption Set feature</span></span>
    - <span data-ttu-id="7ea64-152">새 cmdlet:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="7ea64-152">New cmdlets:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span></span>
    - <span data-ttu-id="7ea64-153">DiskEncryptionSetId 매개 변수가 다음 cmdlet에 추가되었습니다. Set-AzImageOSDisk Set-AzVMOSDisk Set-AzVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="7ea64-153">DiskEncryptionSetId parameter is added to the following cmdlets: Set-AzImageOSDisk Set-AzVMOSDisk Set-AzVmssStorageProfile</span></span>        
        <span data-ttu-id="7ea64-154">Add-AzImageDataDisk New-AzVMDataDisk Set-AzVMDataDisk Add-AzVMDataDisk Add-AzVmssDataDisk Add-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="7ea64-154">Add-AzImageDataDisk New-AzVMDataDisk Set-AzVMDataDisk Add-AzVMDataDisk Add-AzVmssDataDisk Add-AzVmssVMDataDisk</span></span>
    - <span data-ttu-id="7ea64-155">DiskEncryptionSetId 및 EncryptionType 매개 변수가 다음 cmdlet에 추가되었습니다.   New-AzDiskConfig   New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="7ea64-155">DiskEncryptionSetId and EncryptionType parameters are added to the following cmdlets:   New-AzDiskConfig   New-AzSnapshotConfig</span></span>
* <span data-ttu-id="7ea64-156">New-AzVmssIPConfig에 PublicIPAddressVersion 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="7ea64-156">Add PublicIPAddressVersion parameter to New-AzVmssIPConfig</span></span>
* <span data-ttu-id="7ea64-157">사용자 지정 스크립트 확장의 FileUris를 공용 설정에서 보호된 설정으로 이동</span><span class="sxs-lookup"><span data-stu-id="7ea64-157">Move FileUris of custom script extension from public setting to protected setting</span></span>
* <span data-ttu-id="7ea64-158">New-AzVmss, New-AzVmssConfig 및 Update-AzVmss cmdlet에 ScaleInPolicy 추가</span><span class="sxs-lookup"><span data-stu-id="7ea64-158">Add ScaleInPolicy to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>
* <span data-ttu-id="7ea64-159">주요 변경 내용</span><span class="sxs-lookup"><span data-stu-id="7ea64-159">Breaking changes</span></span>
    - <span data-ttu-id="7ea64-160">CreateOption이 업로드일 때 UploadSizeInBytes 매개 변수가 New-AzDiskConfig에 대해 DiskSizeGB 대신 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-160">UploadSizeInBytes parameter is used instead of DiskSizeGB for New-AzDiskConfig when CreateOption is Upload</span></span>
    - <span data-ttu-id="7ea64-161">GalleryImageVersion 개체에서 PublishingProfile.Source.ManagedImage.Id가 StorageProfile.Source.Id로 바뀝니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-161">PublishingProfile.Source.ManagedImage.Id is replaced with StorageProfile.Source.Id in GalleryImageVersion object</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="7ea64-162">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="7ea64-162">Az.DataFactory</span></span>
* <span data-ttu-id="7ea64-163">ADF .Net SDK 버전을 4.3.0으로 업데이트</span><span class="sxs-lookup"><span data-stu-id="7ea64-163">Update ADF .Net SDK version to 4.3.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="7ea64-164">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="7ea64-164">Az.DataLakeStore</span></span>
* <span data-ttu-id="7ea64-165">ADLS SDK 버전 업데이트(https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha) , 다음 수정 사항 제공</span><span class="sxs-lookup"><span data-stu-id="7ea64-165">Update ADLS SDK version (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), brings following fixes</span></span>
* <span data-ttu-id="7ea64-166">휴지통 또는 디렉터리 항목의 creationtime을 역직렬화할 수 없을 때 예외가 발생하지 않도록 방지합니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-166">Avoid throwing exception while unable to deserialize the creationtime of the trash or directory entry.</span></span>
* <span data-ttu-id="7ea64-167">adlsclient에서 요청별 시간 제한 설정 노출</span><span class="sxs-lookup"><span data-stu-id="7ea64-167">Expose setting per request timeout in adlsclient</span></span>
* <span data-ttu-id="7ea64-168">badoffset 복구를 위한 원본 syncflag 전달 수정</span><span class="sxs-lookup"><span data-stu-id="7ea64-168">Fix passing the original syncflag for badoffset recovery</span></span>
* <span data-ttu-id="7ea64-169">응답이 확인된 후 연속 토큰을 검색하기 위한 EnumerateDirectory 수정</span><span class="sxs-lookup"><span data-stu-id="7ea64-169">Fix EnumerateDirectory to retrieve continuation token once response is checked</span></span>
* <span data-ttu-id="7ea64-170">Concat 버그 수정</span><span class="sxs-lookup"><span data-stu-id="7ea64-170">Fix Concat Bug</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="7ea64-171">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="7ea64-171">Az.FrontDoor</span></span>
* <span data-ttu-id="7ea64-172">모듈 간 기타 오타가 수정됨</span><span class="sxs-lookup"><span data-stu-id="7ea64-172">Fixed miscellaneous typos across module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="7ea64-173">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="7ea64-173">Az.HDInsight</span></span>
* <span data-ttu-id="7ea64-174">ADLSGen1 스토리지가 포함된 클러스터를 가져오기 위해 Get-AzHDInsightCluster를 사용할 때 고객에게 '올바른 Base-64 문자열이 아닙니다' 오류가 표시되는 버그가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-174">Fixed the bug that customer will get 'Not a valid Base-64 string' error when using Get-AzHDInsightCluster to get the cluster with ADLSGen1 storage.</span></span>
* <span data-ttu-id="7ea64-175">고객이 Azure Data Lake에 액세스하기 위해 서비스 주체 애플리케이션 ID를 제공할 수 있도록 세 가지 cmdlet Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig 및 New-AzHDInsightCluster에 이름이 'ApplicationId'인 매개 변수를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-175">Add a parameter named 'ApplicationId' to three cmdlets Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig and New-AzHDInsightCluster so that customer can provide the service principal application id for accessing Azure Data Lake.</span></span>
* <span data-ttu-id="7ea64-176">Microsoft.Azure.Management.HDInsight가 2.1.0에서 5.1.0으로 변경됨</span><span class="sxs-lookup"><span data-stu-id="7ea64-176">Changed Microsoft.Azure.Management.HDInsight from 2.1.0 to 5.1.0</span></span>
* <span data-ttu-id="7ea64-177">다음 5가지 cmdlet이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-177">Removed five cmdlets:</span></span>
    - <span data-ttu-id="7ea64-178">Get-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="7ea64-178">Get-AzHDInsightOMS</span></span>
    - <span data-ttu-id="7ea64-179">Enable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="7ea64-179">Enable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="7ea64-180">Disable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="7ea64-180">Disable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="7ea64-181">Grant-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="7ea64-181">Grant-AzHDInsightRdpServicesAccess</span></span>
    - <span data-ttu-id="7ea64-182">Revoke-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="7ea64-182">Revoke-AzHDInsightRdpServicesAccess</span></span>
* <span data-ttu-id="7ea64-183">다음 3가지 cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-183">Added three cmdlets:</span></span>
    - <span data-ttu-id="7ea64-184">Get-AzHDInsightOMS 대신 Get-AzHDInsightMonitoring</span><span class="sxs-lookup"><span data-stu-id="7ea64-184">Get-AzHDInsightMonitoring to replace Get-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="7ea64-185">Get-AzHDInsightOMS 대신 Get-AzHDInsightMonitoring</span><span class="sxs-lookup"><span data-stu-id="7ea64-185">Enable-AzHDInsightMonitoring to replace Enable-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="7ea64-186">Disable-AzHDInsightOMS 대신 Disable-AzHDInsightMonitoring</span><span class="sxs-lookup"><span data-stu-id="7ea64-186">Disable-AzHDInsightMonitoring to replace Disable-AzHDInsightOMS.</span></span>
* <span data-ttu-id="7ea64-187">특정 위치의 기능 정보 가져오기를 지원하도록 cmdlet Get-AzHDInsightProperties가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-187">Fixed cmdlet Get-AzHDInsightProperties to support get capabilities information from a specific location.</span></span>
* <span data-ttu-id="7ea64-188">Add-AzHDInsightConfigValue에서 매개 변수 집합('Spark1', 'Spark2')이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-188">Removed parameter sets('Spark1', 'Spark2') from Add-AzHDInsightConfigValue.</span></span>
* <span data-ttu-id="7ea64-189">cmdlet Add-AzHDInsightSecurityProfile의 도움말 문서에 예제를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-189">Add examples to the help documents of cmdlet Add-AzHDInsightSecurityProfile.</span></span>
* <span data-ttu-id="7ea64-190">다음 cmdlet의 출력 유형이 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-190">Changed output type of the following cmdlets:</span></span>
*  - <span data-ttu-id="7ea64-191">Get-AzHDInsightProperties의 출력 유형이 CapabilitiesResponse에서 AzureHDInsightCapabilities로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-191">Changed the output type of Get-AzHDInsightProperties from  CapabilitiesResponse to AzureHDInsightCapabilities.</span></span>
*  - <span data-ttu-id="7ea64-192">Remove-AzHDInsightCluster의 출력 유형이 ClusterGetResponse에서 bool로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-192">Changed the output type of Remove-AzHDInsightCluster from ClusterGetResponse to bool.</span></span>
*  - <span data-ttu-id="7ea64-193">Set-AzHDInsightGatewaySettings의 출력 유형이 HttpConnectivitySettings에서 GatewaySettings로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-193">Changed the output type of Set-AzHDInsightGatewaySettings HttpConnectivitySettings to GatewaySettings.</span></span>
* <span data-ttu-id="7ea64-194">몇 가지 시나리오 테스트 사례가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-194">Added some scenario test cases.</span></span>
* <span data-ttu-id="7ea64-195">일부 별칭 제거: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span><span class="sxs-lookup"><span data-stu-id="7ea64-195">Remove some alias: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="7ea64-196">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="7ea64-196">Az.IotHub</span></span>
* <span data-ttu-id="7ea64-197">주요 변경 내용:</span><span class="sxs-lookup"><span data-stu-id="7ea64-197">Breaking changes:</span></span>
    - <span data-ttu-id="7ea64-198">'Add-AzIotHubEventHubConsumerGroup' cmdlet이 'EventHubEndpointName' 매개 변수를 더 이상 지원하지 않으며 원래 매개 변수 이름에 대해 별칭을 찾을 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-198">The cmdlet 'Add-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="7ea64-199">'Add-AzIotHubEventHubConsumerGroup' cmdlet에 대한 매개 변수 집합 '__AllParameterSets'가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-199">The parameter set '__AllParameterSets' for cmdlet 'Add-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="7ea64-200">'Get-AzIotHubEventHubConsumerGroup' cmdlet이 'EventHubEndpointName' 매개 변수를 더 이상 지원하지 않으며 원래 매개 변수 이름에 대해 별칭을 찾을 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-200">The cmdlet 'Get-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="7ea64-201">'Get-AzIotHubEventHubConsumerGroup' cmdlet에 대한 매개 변수 집합 '__AllParameterSets'가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-201">The parameter set '__AllParameterSets' for cmdlet 'Get-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="7ea64-202">'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' 유형의 'OperationsMonitoringProperties' 속성이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-202">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' has been removed.</span></span>
    - <span data-ttu-id="7ea64-203">'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' 유형의 'OperationsMonitoringProperties' 속성이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-203">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' has been removed.</span></span>
    - <span data-ttu-id="7ea64-204">'New-AzIotHubExportDevice' cmdlet이 더 이상 'New-AzIotHubExportDevices' 별칭을 지원하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-204">The cmdlet 'New-AzIotHubExportDevice' no longer supports the alias 'New-AzIotHubExportDevices'.</span></span>
    - <span data-ttu-id="7ea64-205">'New-AzIotHubImportDevice' cmdlet이 더 이상 'New-AzIotHubImportDevices' 별칭을 지원하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-205">The cmdlet 'New-AzIotHubImportDevice' no longer supports the alias 'New-AzIotHubImportDevices'.</span></span>
    - <span data-ttu-id="7ea64-206">'Remove-AzIotHubEventHubConsumerGroup' cmdlet이 'EventHubEndpointName' 매개 변수를 더 이상 지원하지 않으며 원래 매개 변수 이름에 대해 별칭을 찾을 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-206">The cmdlet 'Remove-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="7ea64-207">'Remove-AzIotHubEventHubConsumerGroup' cmdlet에 대한 매개 변수 집합 '__AllParameterSets'가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-207">The parameter set '__AllParameterSets' for cmdlet 'Remove-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="7ea64-208">'Set-AzIotHub' cmdlet이 'OperationsMonitoringProperties' 매개 변수를 더 이상 지원하지 않으며 원래 매개 변수 이름에 대해 별칭을 찾을 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-208">The cmdlet 'Set-AzIotHub' no longer supports the parameter 'OperationsMonitoringProperties' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="7ea64-209">'Set-AzIotHub' cmdlet에 대한 매개 변수 집합 'UpdateOperationsMonitoringProperties'가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-209">The parameter set 'UpdateOperationsMonitoringProperties' for cmdlet 'Set-AzIotHub' has been removed.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="7ea64-210">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="7ea64-210">Az.RecoveryServices</span></span>
* <span data-ttu-id="7ea64-211">Azure Site Recovery가 Azure-Azure를 위한 NSG, 공용 IP 및 내부 부하 분산 장치와 같은 네트워킹 리소스 구성을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-211">Azure Site Recovery support to configure networking resources like NSG, public IP and internal load balancers for Azure to Azure.</span></span>
* <span data-ttu-id="7ea64-212">Azure Site Recovery가 vMWare-Azure를 위한 관리 디스크에 쓰기를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-212">Azure Site Recovery Support to write to managed disk for vMWare to Azure.</span></span>
* <span data-ttu-id="7ea64-213">Azure Site Recovery가 vMWare-Azure를 위한 NIC 감소를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-213">Azure Site Recovery Support to NIC reduction for vMWare to Azure.</span></span>
* <span data-ttu-id="7ea64-214">Azure Site Recovery가 Azure-Azure를 위한 가속 네트워킹을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-214">Azure Site Recovery Support to accelerated networking for Azure to Azure.</span></span>
* <span data-ttu-id="7ea64-215">Azure Site Recovery가 Azure-Azure를 위한 에이전트 자동 업데이트를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-215">Azure Site Recovery Support to agent auto update for Azure to Azure.</span></span>
* <span data-ttu-id="7ea64-216">Azure Site Recovery가 Azure-Azure를 위한 표준 SSD를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-216">Azure Site Recovery Support to Standard SSD for Azure to Azure.</span></span>
* <span data-ttu-id="7ea64-217">Azure Site Recovery가 Azure-Azure를 위한 두 가지 Azure 디스크 암호화 전달을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-217">Azure Site Recovery Support to Azure Disk Encryption two pass for Azure to Azure.</span></span>
* <span data-ttu-id="7ea64-218">Azure Site Recovery가 Azure-Azure를 위한 새로 추가된 디스크 보호를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-218">Azure Site Recovery Support to protect newly added disk for Azure to Azure.</span></span>
* <span data-ttu-id="7ea64-219">VM을 위한 SoftDelete 기능 및 softdelete를 위한 테스트가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-219">Added SoftDelete feature for VM and added tests for softdelete</span></span>

#### <a name="azresources"></a><span data-ttu-id="7ea64-220">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7ea64-220">Az.Resources</span></span>
* <span data-ttu-id="7ea64-221">종속성 어셈블리 Microsoft.Extensions.Caching.Memory가 1.1.1에서 2.2로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-221">Update dependency assembly Microsoft.Extensions.Caching.Memory from 1.1.1 to 2.2</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7ea64-222">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7ea64-222">Az.Network</span></span>
* <span data-ttu-id="7ea64-223">일반 서비스 공급자 지원을 위해 PrivateEndpointConnection에 대한 모든 cmdlet이 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-223">Change all cmdlets for PrivateEndpointConnection to support generic service provider.</span></span>
    - <span data-ttu-id="7ea64-224">업데이트된 cmdlet:</span><span class="sxs-lookup"><span data-stu-id="7ea64-224">Updated cmdlet:</span></span>
        - <span data-ttu-id="7ea64-225">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="7ea64-225">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="7ea64-226">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="7ea64-226">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="7ea64-227">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="7ea64-227">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="7ea64-228">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="7ea64-228">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="7ea64-229">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="7ea64-229">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="7ea64-230">PrivateLinkResource에 대한 새 cmdlet이 추가되었고 일반 서비스 공급자도 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-230">Add new cmdlet for PrivateLinkResource and it also support generic service provider.</span></span>
    - <span data-ttu-id="7ea64-231">새 cmdlet:</span><span class="sxs-lookup"><span data-stu-id="7ea64-231">New cmdlet:</span></span>
        - <span data-ttu-id="7ea64-232">Get-AzPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="7ea64-232">Get-AzPrivateLinkResource</span></span>
* <span data-ttu-id="7ea64-233">Proxy Protocol V2 기능에 대한 새 필드 및 매개 변수가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-233">Add new fields and parameter for the feature Proxy Protocol V2.</span></span>
    - <span data-ttu-id="7ea64-234">PrivateLinkService에서 EnableProxyProtocol 속성 추가</span><span class="sxs-lookup"><span data-stu-id="7ea64-234">Add property EnableProxyProtocol in PrivateLinkService</span></span>
    - <span data-ttu-id="7ea64-235">PrivateEndpointConnection에서 LinkIdentifier 속성 추가</span><span class="sxs-lookup"><span data-stu-id="7ea64-235">Add property LinkIdentifier in PrivateEndpointConnection</span></span>
    - <span data-ttu-id="7ea64-236">새로운 선택적인 매개 변수인 EnableProxyProtocol을 추가하도록 New-AzPrivateLinkService가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-236">Updated New-AzPrivateLinkService to add a new optional parameter EnableProxyProtocol.</span></span>
* <span data-ttu-id="7ea64-237">'New-AzApplicationGatewaySku' 참조 설명서의 잘못된 매개 변수 설명 수정</span><span class="sxs-lookup"><span data-stu-id="7ea64-237">Fix incorrect parameter description in 'New-AzApplicationGatewaySku' reference documentation</span></span>
* <span data-ttu-id="7ea64-238">Azure 방화벽 정책을 지원하는 새로운 cmdlet</span><span class="sxs-lookup"><span data-stu-id="7ea64-238">New cmdlets to support the azure firewall policy</span></span>
* <span data-ttu-id="7ea64-239">VirtualHub의 자식 리소스 RouteTables에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="7ea64-239">Add support for child resource RouteTables of VirtualHub</span></span>
    - <span data-ttu-id="7ea64-240">추가된 새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-240">New cmdlets added:</span></span>
        - <span data-ttu-id="7ea64-241">Add-AzVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="7ea64-241">Add-AzVirtualHubRoute</span></span>
        - <span data-ttu-id="7ea64-242">Add-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="7ea64-242">Add-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="7ea64-243">Get-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="7ea64-243">Get-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="7ea64-244">Remove-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="7ea64-244">Remove-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="7ea64-245">Set-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="7ea64-245">Set-AzVirtualHub</span></span>
* <span data-ttu-id="7ea64-246">VirtualHub의 새로운 속성 Sku 및 VirtualWan의 VirtualWANType에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="7ea64-246">Add support for new properties Sku of VirtualHub and VirtualWANType of VirtualWan</span></span>
    - <span data-ttu-id="7ea64-247">선택적 매개 변수로 다음 cmdlet이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-247">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="7ea64-248">New-AzVirtualHub: 추가된 매개 변수 Sku</span><span class="sxs-lookup"><span data-stu-id="7ea64-248">New-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="7ea64-249">Update-AzVirtualHub: 추가된 매개 변수 Sku</span><span class="sxs-lookup"><span data-stu-id="7ea64-249">Update-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="7ea64-250">New-AzVirtualWan: 추가된 매개 변수 VirtualWANType</span><span class="sxs-lookup"><span data-stu-id="7ea64-250">New-AzVirtualWan : added parameter VirtualWANType</span></span>
        - <span data-ttu-id="7ea64-251">Update-AzVirtualWan: 추가된 매개 변수 VirtualWANType</span><span class="sxs-lookup"><span data-stu-id="7ea64-251">Update-AzVirtualWan : added parameter VirtualWANType</span></span>
* <span data-ttu-id="7ea64-252">HubVnetConnection, VpnConnection 및 ExpressRouteConnection에 대한 EnableInternetSecurity 속성 지원 추가</span><span class="sxs-lookup"><span data-stu-id="7ea64-252">Add support for EnableInternetSecurity property for HubVnetConnection, VpnConnection and ExpressRouteConnection</span></span>
    - <span data-ttu-id="7ea64-253">추가된 새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-253">New cmdlets added:</span></span>
        - <span data-ttu-id="7ea64-254">Update-AzureRmVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="7ea64-254">Update-AzureRmVirtualHubVnetConnection</span></span>
    - <span data-ttu-id="7ea64-255">선택적 매개 변수로 다음 cmdlet이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-255">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="7ea64-256">New-AzureRmVirtualHubVnetConnection: 추가된 매개 변수 EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="7ea64-256">New-AzureRmVirtualHubVnetConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="7ea64-257">New-AzureRmVpnConnection: 추가된 매개 변수 EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="7ea64-257">New-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="7ea64-258">Update-AzureRmVpnConnection: 추가된 매개 변수 EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="7ea64-258">Update-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="7ea64-259">New-AzureRmExpressRouteConnection: 추가된 매개 변수 EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="7ea64-259">New-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="7ea64-260">Set-AzureRmExpressRouteConnection: 추가된 매개 변수 EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="7ea64-260">Set-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
* <span data-ttu-id="7ea64-261">TopLevel WebApplicationFirewall 정책 구성을 위한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="7ea64-261">Add support for Configuring TopLevel WebApplicationFirewall Policy</span></span>
    - <span data-ttu-id="7ea64-262">추가된 새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-262">New cmdlets added:</span></span>
        - <span data-ttu-id="7ea64-263">New-AzApplicationGatewayFirewallPolicySetting</span><span class="sxs-lookup"><span data-stu-id="7ea64-263">New-AzApplicationGatewayFirewallPolicySetting</span></span>
        - <span data-ttu-id="7ea64-264">New-AzApplicationGatewayFirewallPolicyExclusion</span><span class="sxs-lookup"><span data-stu-id="7ea64-264">New-AzApplicationGatewayFirewallPolicyExclusion</span></span>
        - <span data-ttu-id="7ea64-265">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="7ea64-265">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span></span>
        - <span data-ttu-id="7ea64-266">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="7ea64-266">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span></span>
        - <span data-ttu-id="7ea64-267">New-AzApplicationGatewayFirewallPolicyManagedRule</span><span class="sxs-lookup"><span data-stu-id="7ea64-267">New-AzApplicationGatewayFirewallPolicyManagedRule</span></span>
        - <span data-ttu-id="7ea64-268">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="7ea64-268">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span></span>
    - <span data-ttu-id="7ea64-269">선택적 매개 변수로 다음 cmdlet이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-269">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="7ea64-270">New-AzApplicationGatewayFirewallPolicy: 추가된 매개 변수 PolicySetting, ManagedRule</span><span class="sxs-lookup"><span data-stu-id="7ea64-270">New-AzApplicationGatewayFirewallPolicy : added parameter PolicySetting, ManagedRule</span></span>
* <span data-ttu-id="7ea64-271">CustomRule에서 Geo-Match 연산자를 위한 지원 추가됨</span><span class="sxs-lookup"><span data-stu-id="7ea64-271">Added support for Geo-Match operator on CustomRule</span></span>
    - <span data-ttu-id="7ea64-272">FirewallCondition에서 연산자에 GeoMatch 추가됨</span><span class="sxs-lookup"><span data-stu-id="7ea64-272">Added GeoMatch to the operator on the FirewallCondition</span></span>
* <span data-ttu-id="7ea64-273">perListener 및 perSite 방화벽 규칙에 대한 지원 추가됨</span><span class="sxs-lookup"><span data-stu-id="7ea64-273">Added support for perListener and perSite Firewall policy</span></span>
    - <span data-ttu-id="7ea64-274">선택적 매개 변수로 다음 cmdlet이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-274">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="7ea64-275">New-AzApplicationGatewayHttpListener: 추가된 매개 변수 FirewallPolicy, FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="7ea64-275">New-AzApplicationGatewayHttpListener : added parameter FirewallPolicy, FirewallPolicyId</span></span>
        - <span data-ttu-id="7ea64-276">New-AzApplicationGatewayPathRuleConfig: 추가된 매개 변수 FirewallPolicy, FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="7ea64-276">New-AzApplicationGatewayPathRuleConfig : added parameter FirewallPolicy, FirewallPolicyId</span></span>
* <span data-ttu-id="7ea64-277">'PSBastion'에서 이름이 AzureBastionSubnet인 필수 서브넷의 수정은 대소문자를 구분하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-277">Fix required subnet with name AzureBastionSubnet in 'PSBastion' can be case insensitive</span></span>
* <span data-ttu-id="7ea64-278">Azure Firewall을 위한 네트워크 규칙의 대상 FQDN 및 NAT 규칙의 번역된 FQDN 지원</span><span class="sxs-lookup"><span data-stu-id="7ea64-278">Support for Destination FQDNs in Network Rules and Translated FQDN in NAT Rules for Azure Firewall</span></span>
* <span data-ttu-id="7ea64-279">IpGroup의 최상위 리소스 RouteTables에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="7ea64-279">Add support for top level resource RouteTables of IpGroup</span></span>
    - <span data-ttu-id="7ea64-280">추가된 새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-280">New cmdlets added:</span></span>
        - <span data-ttu-id="7ea64-281">New-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="7ea64-281">New-AzIpGroup</span></span>
        - <span data-ttu-id="7ea64-282">Remove-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="7ea64-282">Remove-AzIpGroup</span></span>
        - <span data-ttu-id="7ea64-283">Get-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="7ea64-283">Get-AzIpGroup</span></span>
        - <span data-ttu-id="7ea64-284">Set-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="7ea64-284">Set-AzIpGroup</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="7ea64-285">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="7ea64-285">Az.ServiceFabric</span></span>
* <span data-ttu-id="7ea64-286">Add-AzVmssSecret에서 지원되기 때문에 Add-AzServiceFabricApplicationCertificate cmdlet이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-286">Remove Add-AzServiceFabricApplicationCertificate cmdlet as this scenario is covered by Add-AzVmssSecret.</span></span>

#### <a name="azsql"></a><span data-ttu-id="7ea64-287">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7ea64-287">Az.Sql</span></span>
* <span data-ttu-id="7ea64-288">Managed Instances에서 삭제된 데이터베이스의 복원을 위한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-288">Added support for restore of dropped databases on Managed Instances.</span></span>
* <span data-ttu-id="7ea64-289">이전의 감사 cmdlet 코드가 사용되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-289">Deprecated from code old auditing cmdlets.</span></span>
* <span data-ttu-id="7ea64-290">사용되지 않는 별칭이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-290">Removed deprecated aliases:</span></span>
* <span data-ttu-id="7ea64-291">Get-AzSqlDatabaseIndexRecommendations(대신 Get-AzSqlDatabaseIndexRecommendation 사용)</span><span class="sxs-lookup"><span data-stu-id="7ea64-291">Get-AzSqlDatabaseIndexRecommendations (use Get-AzSqlDatabaseIndexRecommendation instead)</span></span>
* <span data-ttu-id="7ea64-292">Get-AzSqlDatabaseRestorePoints(대신 Get-AzSqlDatabaseRestorePoint 사용)</span><span class="sxs-lookup"><span data-stu-id="7ea64-292">Get-AzSqlDatabaseRestorePoints (use Get-AzSqlDatabaseRestorePoint instead)</span></span>
* <span data-ttu-id="7ea64-293">Get-AzSqlDatabaseSecureConnectionPolicy cmdlet 제거</span><span class="sxs-lookup"><span data-stu-id="7ea64-293">Remove Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="7ea64-294">사용되지 않는 취약성 평가 설정 cmdlet에 대한 별칭 제거</span><span class="sxs-lookup"><span data-stu-id="7ea64-294">Remove aliases for deprecated Vulnerability Assessment Settings cmdlets</span></span>
* <span data-ttu-id="7ea64-295">지능형 위협 탐지 설정 cmdlet 사용 중단</span><span class="sxs-lookup"><span data-stu-id="7ea64-295">Deprecate Advanced Threat Detection Settings cmdlets</span></span> 
* <span data-ttu-id="7ea64-296">데이터베이스의 열에 대한 민감도 권장 사항의 사용 여부를 제어하는 cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-296">Adding cmdlets to Disable and enable sensitivity recommendations on columns in a database.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="7ea64-297">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="7ea64-297">Az.Storage</span></span>
* <span data-ttu-id="7ea64-298">스토리지 계정을 만들거나 업데이트할 때 큰 파일 공유 사용 지원</span><span class="sxs-lookup"><span data-stu-id="7ea64-298">Support enable Large File share when create or update Storage account</span></span>
    -  <span data-ttu-id="7ea64-299">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="7ea64-299">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="7ea64-300">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="7ea64-300">Set-AzStorageAccount</span></span>
* <span data-ttu-id="7ea64-301">파일 핸들을 닫거나/가져올 때, DeletePending 상태의 개체로 인한 오류를 방지하기 위해 입력 경로가 파일 디렉터리인지 또는 파일인지를 확인하는 과정을 건너뜁니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-301">When close/get File handle, skip check the input path is File directory or File, to avoid failure with object in DeletePending status</span></span>
    -  <span data-ttu-id="7ea64-302">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="7ea64-302">Get-AzStorageFileHandle</span></span>
    -  <span data-ttu-id="7ea64-303">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="7ea64-303">Close-AzStorageFileHandle</span></span>
    
## <a name="280---october-2019"></a><span data-ttu-id="7ea64-304">2.8.0 - 2019년 10월</span><span class="sxs-lookup"><span data-stu-id="7ea64-304">2.8.0 - October 2019</span></span>
### <a name="general"></a><span data-ttu-id="7ea64-305">일반</span><span class="sxs-lookup"><span data-stu-id="7ea64-305">General</span></span>
* <span data-ttu-id="7ea64-306">Az.HealthcareApis 1.0.0 릴리스</span><span class="sxs-lookup"><span data-stu-id="7ea64-306">Az.HealthcareApis 1.0.0 release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="7ea64-307">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="7ea64-307">Az.Accounts</span></span>
* <span data-ttu-id="7ea64-308">생성된 모듈에 대한 원격 분석 및 URL 다시 작성이 업데이트되고, Windows 단위 테스트가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-308">Update telemetry and url rewriting for generated modules, fix windows unit tests.</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="7ea64-309">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="7ea64-309">Az.ApiManagement</span></span>
* <span data-ttu-id="7ea64-310">**Set-AzApiManagementApi** - API 업데이트 지원이 ApiVersionSet에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-310">**Set-AzApiManagementApi** - Added support for Updating Api into ApiVersionSet</span></span>
    - <span data-ttu-id="7ea64-311">문제 https://github.com/Azure/azure-powershell/issues/10068 수정</span><span class="sxs-lookup"><span data-stu-id="7ea64-311">Fix for issue https://github.com/Azure/azure-powershell/issues/10068</span></span>

#### <a name="azautomation"></a><span data-ttu-id="7ea64-312">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="7ea64-312">Az.Automation</span></span>
* <span data-ttu-id="7ea64-313">Linux 다시 부팅 설정 매개 변수에 대한 New-AzureAutomationSoftwareUpdateConfiguration cmdlet이 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-313">Fixed New-AzureAutomationSoftwareUpdateConfiguration cmdlet for Linux reboot setting parameter.</span></span> 

#### <a name="azbatch"></a><span data-ttu-id="7ea64-314">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="7ea64-314">Az.Batch</span></span>
* <span data-ttu-id="7ea64-315">**Get-AzBatchNodeAgentSku**가 더 이상 사용되지 않으며, 2.0.0 버전의 **Get-AzBatchSupportImage**로 대체되었습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-315">**Get-AzBatchNodeAgentSku** is deprecated and will be replaced by **Get-AzBatchSupportImage** in version 2.0.0.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7ea64-316">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7ea64-316">Az.Compute</span></span>
* <span data-ttu-id="7ea64-317">Priority, EvictionPolicy 및 MaxPrice 매개 변수가 New-AzVM 및 New-AzVmss cmdlet에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-317">Add Priority, EvictionPolicy, and MaxPrice parameters to New-AzVM and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="7ea64-318">Add-AzVMAdditionalUnattendContent 및 Add-AzVMSshPublicKey cmdlet에 대한 경고 메시지와 도움말 문서가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-318">Fix warning message and help document for Add-AzVMAdditionalUnattendContent and Add-AzVMSshPublicKey cmdlets</span></span>
* <span data-ttu-id="7ea64-319">Set-AzVMDiskEncryptionExtension의 관리 디스크가 있는 Linux VM에 대한 -skipVmBackup 예외가 해결되었습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-319">Fix -skipVmBackup exception for Linux VMs with managed disks for Set-AzVMDiskEncryptionExtension.</span></span> 
* <span data-ttu-id="7ea64-320">Set-AzVMDiskEncryptionExtension의 두 가지 패스 시나리오에서 발생하는 암호화 설정 업데이트의 버그가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-320">Fix bug in update encryption settings in Set-AzVMDiskEncryptionExtension, two pass scenario.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="7ea64-321">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="7ea64-321">Az.DataFactory</span></span>
* <span data-ttu-id="7ea64-322">ADF V2 데이터 흐름에 대한 CRUD 명령으로 Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow 및 Get-AzDataFactoryV2DataFlow가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-322">Adding CRUD commands for ADF V2 data flow: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow, and Get-AzDataFactoryV2DataFlow.</span></span>
* <span data-ttu-id="7ea64-323">ADF V2 데이터 흐름 디버그 세션에 대한 작업 명령으로 Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand 및 Stop-AzDataFactoryV2DataFlowDebugSession이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-323">Adding action commands for ADF V2 data flow debug Session: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand and Stop-AzDataFactoryV2DataFlowDebugSession.</span></span>
* <span data-ttu-id="7ea64-324">ADF .Net SDK 버전이 4.2.0으로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-324">Update ADF .Net SDK version to 4.2.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="7ea64-325">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="7ea64-325">Az.DataLakeStore</span></span>
* <span data-ttu-id="7ea64-326">도메인 없이 '-'가 있는 계정을 전달할 수 있도록 계정 유효성 검사가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-326">Fix account validation so that accounts with '-' can be passed without domain</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="7ea64-327">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="7ea64-327">Az.HealthcareApis</span></span>
* <span data-ttu-id="7ea64-328">PowerShell 버전이 1.0.0으로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-328">Updated the powershell version to 1.0.0</span></span>
* <span data-ttu-id="7ea64-329">SDK 버전이 1.0.2로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-329">Updated the SDK version to 1.0.2</span></span>
* <span data-ttu-id="7ea64-330">새 SDK 버전을 참조하도록 테스트가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-330">Update in tests to refer to new SDK version</span></span>
* <span data-ttu-id="7ea64-331">출력이 중첩 구조에서 평면화 구조로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-331">Updated the output structure from nested to flattened.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="7ea64-332">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="7ea64-332">Az.IotHub</span></span>
* <span data-ttu-id="7ea64-333">새 라우팅 원본 추가: DigitalTwinChangeEvents</span><span class="sxs-lookup"><span data-stu-id="7ea64-333">Add new routing source: DigitalTwinChangeEvents</span></span>
* <span data-ttu-id="7ea64-334">사소한 버그 수정: Get-AzIothub에서 subscriptionId를 반환하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-334">Minor bug fix: Get-AzIothub not returning subscriptionId</span></span> 

#### <a name="azmonitor"></a><span data-ttu-id="7ea64-335">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="7ea64-335">Az.Monitor</span></span>
* <span data-ttu-id="7ea64-336">작업 그룹에 대한 새 작업 그룹 수신기로 -ItsmReceiver, -VoiceReceiver, -ArmRoleReceiver, -AzureFunctionReceiver, -LogicAppReceiver, -AutomationRunbookReceiver, -AzureAppPushReceiver가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-336">New action group receivers added for action group   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span></span>
* <span data-ttu-id="7ea64-337">수신기에 사용하도록 설정된 일반 경고 스키마가 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-337">Use common alert schema enabled for the receivers.</span></span> <span data-ttu-id="7ea64-338">SMS, Azure 앱 푸시, ITSM 및 음성 수신기에는 적용되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-338">This is not applicable for SMS, Azure App push , ITSM and Voice recievers</span></span>
* <span data-ttu-id="7ea64-339">웹후크에서 이제 Azure Active Directory 인증을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-339">Webhooks now supports Azure active directory authentication .</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7ea64-340">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7ea64-340">Az.Network</span></span>
* <span data-ttu-id="7ea64-341">서비스 엔드포인트 정책에 사용할 수 있는 별칭을 가져오기 위해 호출할 수 있는 새 Get-AzAvailableServiceAlias cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-341">Add new cmdlet Get-AzAvailableServiceAlias which can be called to get the aliases that can be used for Service Endpoint Policies.</span></span>
* <span data-ttu-id="7ea64-342">트래픽 선택기를 Virtual Network 게이트웨이 연결에 추가할 수 있는 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-342">Added support for the adding traffic selectors to Virtual Network Gateway Connections</span></span>
    - <span data-ttu-id="7ea64-343">추가된 새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-343">New cmdlets added:</span></span>
        - <span data-ttu-id="7ea64-344">New-AzureRmTrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="7ea64-344">New-AzureRmTrafficSelectorPolicy</span></span>
    - <span data-ttu-id="7ea64-345">cmdlet이 선택적인 -TrafficSelectorPolicies, -New-AzureRmVirtualNetworkGatewayConnection, -Set-AzureRmVirtualNetworkGatewayConnection 매개 변수로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-345">Cmdlets updated with optional parameter -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="7ea64-346">ESP 및 AH 프로토콜 지원이 네트워크 보안 규칙 구성에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-346">Add support for ESP and AH protocols in network security rule configurations</span></span>
    - <span data-ttu-id="7ea64-347">다음 Cmdlet이 업데이트 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-347">Updated cmdlets:</span></span>
        - <span data-ttu-id="7ea64-348">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="7ea64-348">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="7ea64-349">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="7ea64-349">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="7ea64-350">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="7ea64-350">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="7ea64-351">Cortex cmdlet의 예외 처리가 향상되었습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-351">Improve handling of exceptions in Cortex cmdlets</span></span>
* <span data-ttu-id="7ea64-352">새 VirtualNetworkGateways 세대 및 SKU</span><span class="sxs-lookup"><span data-stu-id="7ea64-352">New Generations and SKUs for VirtualNetworkGateways</span></span>
  - <span data-ttu-id="7ea64-353">새 VirtualNetworkGateways 세대가 도입되었습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-353">Introduce new Generations for VirtualNetworkGateways.</span></span>
  - <span data-ttu-id="7ea64-354">높은 처리량의 새 VirtualNetworkGateways SKU가 도입되었습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-354">Introduce new high throughput SKUs for VirtualNetworkGateways.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="7ea64-355">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="7ea64-355">Az.RedisCache</span></span>
* <span data-ttu-id="7ea64-356">'-Size' 매개 변수에 대한 누락 값을 포함하도록 'Set-AzRedisCache' 참조 설명서가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-356">Updated 'Set-AzRedisCache' reference documentation to include missing values for '-Size' parameter</span></span>

#### <a name="azsql"></a><span data-ttu-id="7ea64-357">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7ea64-357">Az.Sql</span></span>
* <span data-ttu-id="7ea64-358">Managed Instance에서 Active Directory 관리자를 설정할 수 있는 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-358">Add support for setting Active Directory Administrator on Managed Instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="7ea64-359">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="7ea64-359">Az.Storage</span></span>
* <span data-ttu-id="7ea64-360">스토리지 클라이언트 라이브러리가 11.1.0으로 업그레이드되었습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-360">Upgrade Storage Client Library to 11.1.0</span></span>
* <span data-ttu-id="7ea64-361">관리 평면 API를 사용하여 컨테이너를 나열하면 NextPageLink를 통해 나열됩니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-361">List containers with Management plane API, will list with NextPageLink</span></span>
    -  <span data-ttu-id="7ea64-362">Get-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="7ea64-362">Get-AzRmStorageContainer</span></span>
* <span data-ttu-id="7ea64-363">구독에서 스토리지 계정을 나열하면 NextPageLink를 통해 나열됩니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-363">List Storage accounts from subscription, will list with NextPageLink</span></span>
    -  <span data-ttu-id="7ea64-364">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="7ea64-364">Get-AzStorageAccount</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="7ea64-365">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="7ea64-365">Az.StorageSync</span></span>
* <span data-ttu-id="7ea64-366">Reset-AzStorageSyncServerCertificate의 9810 문제가 해결되었습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-366">Fix Issue 9810 in Reset-AzStorageSyncServerCertificate.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="7ea64-367">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="7ea64-367">Az.Websites</span></span>
* <span data-ttu-id="7ea64-368">앱의 ASP를 업데이트하는 Set-AzWebApp이 실패했습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-368">Set-AzWebApp updating ASP of an app was failing</span></span>

## <a name="270---september-2019"></a><span data-ttu-id="7ea64-369">2.7.0 - 2019년 9월</span><span class="sxs-lookup"><span data-stu-id="7ea64-369">2.7.0 - September 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="7ea64-370">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="7ea64-370">Az.ApiManagement</span></span>
* <span data-ttu-id="7ea64-371">'Set-AzApiManagementPolicy' 참조 설명서에서 '-Format' 매개 변수 설명이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-371">Update '-Format' parameter description in 'Set-AzApiManagementPolicy' reference documentation</span></span>
* <span data-ttu-id="7ea64-372">참조 설명서에서 사용되지 않는 cmdlet 'Update-AzApiManagementDeployment'의 참조를 제거했습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-372">Removed references of deprecated cmdlet 'Update-AzApiManagementDeployment' from reference documentation.</span></span> <span data-ttu-id="7ea64-373">그 대신 'Set-AzApiManagement'를 사용하세요.</span><span class="sxs-lookup"><span data-stu-id="7ea64-373">Use 'Set-AzApiManagement' instead.</span></span>

#### <a name="azautomation"></a><span data-ttu-id="7ea64-374">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="7ea64-374">Az.Automation</span></span>
* <span data-ttu-id="7ea64-375">'Register-AzAutomationDscNode'에 대한 참조 설명서의 예제 오타가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-375">Fixed example typo in reference documentation for 'Register-AzAutomationDscNode'</span></span>
* <span data-ttu-id="7ea64-376">Register-AzAutomationDSCNode에 OS 제한에 대한 설명이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-376">Added clarification on OS restriction to Register-AzAutomationDSCNode</span></span>
* <span data-ttu-id="7ea64-377">-Wait 옵션에 대한 Start-AzAutomationRunbook cmdlet Null 참조 예외가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-377">Fixed Start-AzAutomationRunbook cmdlet Null reference exception for -Wait option.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7ea64-378">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7ea64-378">Az.Compute</span></span>
* <span data-ttu-id="7ea64-379">New-AzDiskConfig에 UploadSizeInBytes 매개 변수가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-379">Add UploadSizeInBytes parameter tp New-AzDiskConfig</span></span>
* <span data-ttu-id="7ea64-380">New-AzSnapshotConfig에 증분 매개 변수가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-380">Add Incremental parameter to New-AzSnapshotConfig</span></span>
* <span data-ttu-id="7ea64-381">다음과 같은 낮은 우선 순위의 가상 머신 기능이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-381">Add a low priority virtual machine feature:</span></span>
    - <span data-ttu-id="7ea64-382">MaxPrice, EvictionPolicy 및 Priority 매개 변수가 New-AzVMConfig에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-382">MaxPrice, EvictionPolicy and Priority parameters are added to New-AzVMConfig.</span></span>
    - <span data-ttu-id="7ea64-383">MaxPrice 매개 변수는 New-AzVmssConfig, Update-AzVM 및 Update-AzVmss cmdlet에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-383">MaxPrice parameter is added to New-AzVmssConfig, Update-AzVM and Update-AzVmss cmdlets.</span></span>
* <span data-ttu-id="7ea64-384">구독의 모든 가용성 세트를 나열할 때 발생하는 Get-AzAvailabilitySet cmdlet에 대한 VM 참조 이슈가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-384">Fix VM reference issue for Get-AzAvailabilitySet cmdlet when it lists all availability sets in the subscription.</span></span>
* <span data-ttu-id="7ea64-385">Get-AzRemoteDesktopFile에 대한 null 예외가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-385">Fix the null exception for Get-AzRemoteDesktopFile.</span></span>
* <span data-ttu-id="7ea64-386">종료 상대 위치에 대한 VHD 검색 메서드가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-386">Fix VHD Seek method for end-relative position.</span></span>
* <span data-ttu-id="7ea64-387">New-AzVM 및 Update-AzVM에 대한 UltraSSD 이슈가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-387">Fix UltraSSD issue for New-AzVM and Update-AzVM.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="7ea64-388">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="7ea64-388">Az.DataFactory</span></span>
* <span data-ttu-id="7ea64-389">ADF V2에 대한 3가지 새 명령 Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription 및 Get-AzDataFactoryV2TriggerSubscriptionStatus가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-389">Adding 3 new commands for ADF V2 - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription, and Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>
* <span data-ttu-id="7ea64-390">ADF .Net SDK 버전이 4.1.3으로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-390">Updated ADF .Net SDK version to 4.1.3</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="7ea64-391">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="7ea64-391">Az.HDInsight</span></span>
* <span data-ttu-id="7ea64-392">호출 주요 변경 내용</span><span class="sxs-lookup"><span data-stu-id="7ea64-392">Call out breaking changes</span></span>

#### <a name="aziothub"></a><span data-ttu-id="7ea64-393">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="7ea64-393">Az.IotHub</span></span>
* <span data-ttu-id="7ea64-394">지역 쌍 재해 복구 지역에 IotHub에 대한 장애 조치(failover) 호출 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-394">Add support to invoke failover for an IotHub to the geo-paired disaster recovery region.</span></span>
* <span data-ttu-id="7ea64-395">IotHub에 대한 메시지 보강 관리 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-395">Add support to manage message enrichment for an IotHub.</span></span> <span data-ttu-id="7ea64-396">새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-396">New cmdlets are:</span></span>
    - <span data-ttu-id="7ea64-397">Add-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="7ea64-397">Add-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="7ea64-398">Get-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="7ea64-398">Get-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="7ea64-399">Remove-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="7ea64-399">Remove-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="7ea64-400">Set-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="7ea64-400">Set-AzIotHubMessageEnrichment</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="7ea64-401">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="7ea64-401">Az.Monitor</span></span>
* <span data-ttu-id="7ea64-402">최신 모니터링 SDK, 즉, 0.24.1-preview를 가리킵니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-402">Pointing to the most recent Monitor SDK, i.e. 0.24.1-preview</span></span>
   - <span data-ttu-id="7ea64-403">메트릭 cmdlet에 줄 바꿈하지 않는 변경 내용을 추가합니다. 즉, 단위 열거형은 여러 새 값을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-403">Adds non-braking changes to the Metrics cmdlets, i.e. the Unit enumeration supports several new values.</span></span> <span data-ttu-id="7ea64-404">이러한 cmdlet은 읽기 전용이므로 cmdlet 입력이 변경되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-404">These are read-only cmdlets, so there would be no change in the input of the cmdlets.</span></span>
   - <span data-ttu-id="7ea64-405">이제 **ActionGroups** 요청의 api 버전은 **2019-06-01**이고, 이전에는 **2018-03-01**였습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-405">The api-version of the **ActionGroups** requests is now **2019-06-01**, before it was **2018-03-01**.</span></span> <span data-ttu-id="7ea64-406">시나리오 테스트가 이 변경 내용에 맞게 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-406">The scenario tests have been updated to accommodate for this change.</span></span>
   - <span data-ttu-id="7ea64-407">**EmailReceiver** 및 **WebhookReceiver** 클래스에 대한 생성자가 새 필수 인수, 즉, **useCommonAlertSchema**라는 부울 값을 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-407">The constructors for the classes **EmailReceiver** and **WebhookReceiver** added one new mandatory argument, i.e. a Boolean value called **useCommonAlertSchema**.</span></span> <span data-ttu-id="7ea64-408">현재 이 값은 cmdlet의 주요 변경 사항을 숨기도록 **false**로 고정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-408">Currently, the value is fixed to **false** to hide this breaking change from the cmdlets.</span></span> <span data-ttu-id="7ea64-409">**참고**: 이 변경 사항은 경고 팀에서 유효성을 검사해야 하는 임시 변경 내용입니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-409">**NOTE**: this is a temporary change that must be validated by the Alerts team.</span></span>
   - <span data-ttu-id="7ea64-410">이전 SDK에서 변경된 **Source** 클래스(**ScheduledQueryRuleSource** 클래스와 관련됨)의 생성자에 대한 인수 순서입니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-410">The order of the arguments for the constructor of the class **Source** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="7ea64-411">이번 변화로 인해 두 개의 단위 테스트를 수정해야 했습니다. 즉, 두 단위 테스트가 컴파일되었지만 테스트를 통과하지 못했습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-411">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
   - <span data-ttu-id="7ea64-412">이전 SDK에서 변경된 **AlertingAction** 클래스(**ScheduledQueryRuleSource** 클래스와 관련됨)의 생성자에 대한 인수 순서입니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-412">The order of the arguments for the constructor of the class **AlertingAction** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="7ea64-413">이번 변화로 인해 두 개의 단위 테스트를 수정해야 했습니다. 즉, 두 단위 테스트가 컴파일되었지만 테스트를 통과하지 못했습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-413">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
* <span data-ttu-id="7ea64-414">메트릭 경고 V2에 대한 동적 임계값 기준 지원</span><span class="sxs-lookup"><span data-stu-id="7ea64-414">Support Dynamic Threshold criteria for metric alert V2</span></span>
    - <span data-ttu-id="7ea64-415">AzMetricAlertRuleV2Criteria: 이제 동적 임계값 조건도 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-415">New-AzMetricAlertRuleV2Criteria: now creats dynamic threshold criteria also</span></span>
    - <span data-ttu-id="7ea64-416">Add-AzMetricAlertRuleV2: 이제 동적 임계값 조건도 수락합니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-416">Add-AzMetricAlertRuleV2: now accept dynamic threshold criteria also</span></span>
* <span data-ttu-id="7ea64-417">SQR(예약된 쿼리 규칙)의 향상된 기능</span><span class="sxs-lookup"><span data-stu-id="7ea64-417">Improvements in Scheduled Query Rule cmdlets (SQR)</span></span>
 - <span data-ttu-id="7ea64-418">Cmdlet이 'Location' 매개 변수를 두 가지 형식(eastus 같은 위치 또는 미국 동부 같은 위치 표시 이름)으로 모두 허용합니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-418">Cmdlets will accept 'Location' paramater in both formats, either the location (e.g. eastus) or the location display name (e.g. East US)</span></span>
 - <span data-ttu-id="7ea64-419">도움말 파일에 적절하게 표시된 'Enabled' 매개 변수</span><span class="sxs-lookup"><span data-stu-id="7ea64-419">Illustrated 'Enabled' parameter in help files properly</span></span>
 - <span data-ttu-id="7ea64-420">선택적 매개 변수 'ActionGroup'에 대한 예제가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-420">Added examples for 'ActionGroup' optional parameter</span></span>
 - <span data-ttu-id="7ea64-421">도움말 파일이 전체적으로 개선되었습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-421">Overall improved help files</span></span>
* <span data-ttu-id="7ea64-422">'Set-AzActionRule'의 범위 유형 결정 버그를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-422">Fix bug in determining scope type for 'Set-AzActionRule'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7ea64-423">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7ea64-423">Az.Network</span></span>
* <span data-ttu-id="7ea64-424">'New-AzApplicationGateway' 참조 설명서의 잘못된 예제가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-424">Fix incorrect example in 'New-AzApplicationGateway' reference documentation</span></span> 
* <span data-ttu-id="7ea64-425">'Get-AzNetworkWatcherPacketCapture' 참조 설명서에 패킷 캡처를 위한 모든 속성 검색과 관련된 메모가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-425">Add note in 'Get-AzNetworkWatcherPacketCapture' reference documentation about retrieving all properties for a packet capture</span></span>
* <span data-ttu-id="7ea64-426">NIC를 올바르게 열거하도록 'Test-AzNetworkWatcherIPFlow' 참조 설명서의 예제가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-426">Fixed example in 'Test-AzNetworkWatcherIPFlow' reference documentation to correctly enumerate NICs</span></span>
* <span data-ttu-id="7ea64-427">추가 세부 정보가 있는 경우 추가 세부 정보를 표시하도록 클라우드 예외 구문 분석이 향상되었습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-427">Improved cloud exception parsing to display additional details if they are present</span></span>
* <span data-ttu-id="7ea64-428">더 많은 형식의 SDK 예외를 처리하도록 클라우드 예외 구문 분석이 향상되었습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-428">Improved cloud exception parsing to handle additional type of SDK exception</span></span>
* <span data-ttu-id="7ea64-429">보안 규칙 모델의 잘못된 매핑이 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-429">Fixed incorrect mapping of Security Rule models</span></span>
* <span data-ttu-id="7ea64-430">네트워크 인터페이스에 개인 IP 기능을 위한 속성이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-430">Added properties to network interface for private ip feature</span></span>
    - <span data-ttu-id="7ea64-431">PSNetworkInterface에 'PrivateEndpoint' 속성이 PSResourceId 형식으로 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-431">Added property 'PrivateEndpoint' as type of PSResourceId to PSNetworkInterface</span></span>
    - <span data-ttu-id="7ea64-432">PSNetworkInterfaceIPConfiguration에 'PrivateLinkConnectionProperties' 속성이 PSIpConfigurationConnectivityInformation 형식으로 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-432">Added property 'PrivateLinkConnectionProperties' as type of PSIpConfigurationConnectivityInformation to PSNetworkInterfaceIPConfiguration</span></span>
    - <span data-ttu-id="7ea64-433">새 모델 클래스 PSIpConfigurationConnectivityInformation이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-433">Added new model class PSIpConfigurationConnectivityInformation</span></span>
* <span data-ttu-id="7ea64-434">Azure Firewall 리소스에 대한 새 ApplicationRuleProtocolType 'mssql'이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-434">Added new ApplicationRuleProtocolType 'mssql' for Azure Firewall resource</span></span>
* <span data-ttu-id="7ea64-435">Virtual WAN에서 멀티 링크를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-435">MultiLink support in Virtual WAN</span></span>
    - <span data-ttu-id="7ea64-436">새 cmdlet</span><span class="sxs-lookup"><span data-stu-id="7ea64-436">New cmdlets</span></span>
        - <span data-ttu-id="7ea64-437">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="7ea64-437">New-AzVpnSiteLink</span></span>
        - <span data-ttu-id="7ea64-438">New-AzVpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="7ea64-438">New-AzVpnSiteLinkConnection</span></span>
    - <span data-ttu-id="7ea64-439">업데이트된 cmdlet:</span><span class="sxs-lookup"><span data-stu-id="7ea64-439">Updated cmdlet:</span></span>
        - <span data-ttu-id="7ea64-440">New-VpnSite</span><span class="sxs-lookup"><span data-stu-id="7ea64-440">New-VpnSite</span></span>
        - <span data-ttu-id="7ea64-441">Update-VpnSite</span><span class="sxs-lookup"><span data-stu-id="7ea64-441">Update-VpnSite</span></span>
        - <span data-ttu-id="7ea64-442">New-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="7ea64-442">New-VpnConnection</span></span>
        - <span data-ttu-id="7ea64-443">Update-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="7ea64-443">Update-VpnConnection</span></span>
* <span data-ttu-id="7ea64-444">AzureRM cmdlet 대신 Az cmdlet을 사용하도록 일부 PowerShell 예제의 문서가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-444">Fixed documents for some PowerShell examples to use Az cmdlets instead of AzureRM cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="7ea64-445">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="7ea64-445">Az.RecoveryServices</span></span>
* <span data-ttu-id="7ea64-446">AzureVMpolicy 개체가 ProtectedItemsCount 특성으로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-446">Update AzureVMpolicy Object with ProtectedItemsCount Attribute</span></span>
* <span data-ttu-id="7ea64-447">VM 정책 및 원래 스토리지 계정 복원에 대한 테스트가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-447">Added Tests for VM policy and Original Storage Account Restore</span></span>

#### <a name="azresources"></a><span data-ttu-id="7ea64-448">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7ea64-448">Az.Resources</span></span>
* <span data-ttu-id="7ea64-449">매개 변수 범위 없이 AzRoleAssignment를 호출할 수 없는 버그가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-449">Fix bug where New-AzRoleAssignment could not be called without parameter Scope.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="7ea64-450">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="7ea64-450">Az.ServiceFabric</span></span>
* <span data-ttu-id="7ea64-451">'AzServiceFabricReliability' 참조 설명서에 대한 예제의 오타가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-451">Fixed typo in example for 'Update-AzServiceFabricReliability' reference documentation</span></span>
* <span data-ttu-id="7ea64-452">애플리케이션 및 서비스를 관리하는 다음과 같은 새 cmdlet이 추가됩니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-452">Adding new cmdlets to manage appliaction and services:</span></span>
    - <span data-ttu-id="7ea64-453">New-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="7ea64-453">New-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="7ea64-454">New-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="7ea64-454">New-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="7ea64-455">New-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="7ea64-455">New-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="7ea64-456">New-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="7ea64-456">New-AzServiceFabricService</span></span>
    - <span data-ttu-id="7ea64-457">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="7ea64-457">Update-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="7ea64-458">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="7ea64-458">Get-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="7ea64-459">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="7ea64-459">Get-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="7ea64-460">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="7ea64-460">Get-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="7ea64-461">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="7ea64-461">Get-AzServiceFabricService</span></span>
    - <span data-ttu-id="7ea64-462">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="7ea64-462">Remove-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="7ea64-463">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="7ea64-463">Remove-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="7ea64-464">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="7ea64-464">Remove-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="7ea64-465">Remove-AzServiceFabricServic</span><span class="sxs-lookup"><span data-stu-id="7ea64-465">Remove-AzServiceFabricServic</span></span>
* <span data-ttu-id="7ea64-466">Service Fabric SDK가 Service Fabric 리소스 공급자 api 버전 2019-03-01을 사용하는 1.2.0 버전으로 업그레이드되었습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-466">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2019-03-01.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="7ea64-467">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="7ea64-467">Az.SignalR</span></span>
* <span data-ttu-id="7ea64-468">Update, Restart, CheckNameAvailability, GetUsage Cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-468">Add Update, Restart, CheckNameAvailability, GetUsage Cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="7ea64-469">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7ea64-469">Az.Sql</span></span>
* <span data-ttu-id="7ea64-470">'Get-AzSqlElasticPool'에 대한 참조 설명서의 예제가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-470">Update example in reference documentation for 'Get-AzSqlElasticPool'</span></span>
* <span data-ttu-id="7ea64-471">탄력적 풀을 만드는 vCore 예제가 추가되었습니다(AzSqlElasticPool).</span><span class="sxs-lookup"><span data-stu-id="7ea64-471">Added vCore example to creating an elastic pool (New-AzSqlElasticPool).</span></span>
* <span data-ttu-id="7ea64-472">Set-AzSqlServerAdvancedThreatProtectionPolicy 및 Set-AzSqlDatabaseAdvancedThreatProtectionPolicy에서 EmailAddresses가 비어 있는 경우 EmailAddresses의 유효성을 검사하고 EmailAdmins가 false가 아닌지 확인하는 기능이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-472">Remove the validation of EmailAddresses and the check that EmailAdmins is not false in case EmailAddresses is empty in Set-AzSqlServerAdvancedThreatProtectionPolicy and Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="7ea64-473">감사 범주를 사용하는 여러 진단 설정이 있는 경우 서버/데이터베이스 감사 설정을 제거하도록 설정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-473">Enabled removal of server/database auditing settings when multiple diagnostic settings that enable audit category exist.</span></span>
* <span data-ttu-id="7ea64-474">여러 Sql 취약성 평가 cmdlet에서 이메일 주소 유효성 검사가 수정되었습니다(Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting 및 Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span><span class="sxs-lookup"><span data-stu-id="7ea64-474">Fix email addresses validation in multiple Sql Vulnerability Assessment cmdlets (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting and Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span></span>

#### <a name="azstorage"></a><span data-ttu-id="7ea64-475">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="7ea64-475">Az.Storage</span></span>
* <span data-ttu-id="7ea64-476">'Get-AzStorageAccountKey'에 대한 참조 설명서의 예제가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-476">Updated example in reference documentation for 'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="7ea64-477">Azure 파일 업로드/다운에서, 원본 파일 SMB 속성(파일 특성, 파일 생성 시간, 파일을 마지막으로 쓴 시간)을 대상 파일에 보존하는 기능이 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-477">In upload/Downalod Azure File,support perserve the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the destination file</span></span>
    -  <span data-ttu-id="7ea64-478">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="7ea64-478">Set-AzStorageFileContent</span></span>
    -  <span data-ttu-id="7ea64-479">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="7ea64-479">Get-AzStorageFileContent</span></span>
* <span data-ttu-id="7ea64-480">컨테이너가 사용되는 ImmutabilityPolicy에서 properties/metadate fail을 사용하여 블록 Blob 업로드가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-480">Fix Upload block blob with properties/metadate fail on container enabled ImmutabilityPolicy.</span></span>
    -  <span data-ttu-id="7ea64-481">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="7ea64-481">Set-AzStorageBlobContent</span></span>
* <span data-ttu-id="7ea64-482">관리 평면 API를 사용하여 Azure 파일 공유 관리를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-482">Support manage Azure File shares with Management plane API</span></span>
    -  <span data-ttu-id="7ea64-483">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="7ea64-483">New-AzRmStorageShare</span></span>
    -  <span data-ttu-id="7ea64-484">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="7ea64-484">Get-AzRmStorageShare</span></span>
    -  <span data-ttu-id="7ea64-485">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="7ea64-485">Update-AzRmStorageShare</span></span>
    -  <span data-ttu-id="7ea64-486">Remove-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="7ea64-486">Remove-AzRmStorageShare</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="7ea64-487">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="7ea64-487">Az.Websites</span></span>
* <span data-ttu-id="7ea64-488">앱을 새 ASP로 마이그레이션할 때 웹앱 태그가 삭제되는 이슈가 해결되었습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-488">Fixing issue where webapp Tags were getting deleted when migrating App to new ASPwhere webapp Tags were getting deleted when migrating App to new ASP</span></span>
* <span data-ttu-id="7ea64-489">Linux와 Windows에서 모두 작동하도록 Publish-AzureWebapp이 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-489">Fixing the Publish-AzureWebapp to work across Linux and windows</span></span>
* <span data-ttu-id="7ea64-490">'Get-AzWebAppPublishingProfile' 참조 설명서의 예제가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-490">Update example in 'Get-AzWebAppPublishingProfile' reference documentation</span></span>

## <a name="260---august-2019"></a><span data-ttu-id="7ea64-491">2.6.0 - 2019년 8월</span><span class="sxs-lookup"><span data-stu-id="7ea64-491">2.6.0 - August 2019</span></span>
#### <a name="general"></a><span data-ttu-id="7ea64-492">일반</span><span class="sxs-lookup"><span data-stu-id="7ea64-492">General</span></span>
* <span data-ttu-id="7ea64-493">여러 모듈에서 기타 오타가 수정됨</span><span class="sxs-lookup"><span data-stu-id="7ea64-493">Fixed miscellaneous typos across numerous modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="7ea64-494">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="7ea64-494">Az.Accounts</span></span>
* <span data-ttu-id="7ea64-495">Azure Functions 인증에서 사용자가 할당한 MSI가 지원됨(# 9479)</span><span class="sxs-lookup"><span data-stu-id="7ea64-495">Support user-assigned MSI in Azure Functiosn Authentication (#9479)</span></span>

#### <a name="azaks"></a><span data-ttu-id="7ea64-496">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="7ea64-496">Az.Aks</span></span>
* <span data-ttu-id="7ea64-497">'Get-AzAks' 출력 관련 문제가 해결됨</span><span class="sxs-lookup"><span data-stu-id="7ea64-497">Fix issue with output for 'Get-AzAks'</span></span>
    * <span data-ttu-id="7ea64-498">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/9847 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="7ea64-498">More information here: https://github.com/Azure/azure-powershell/issues/9847</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="7ea64-499">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="7ea64-499">Az.ApiManagement</span></span>
* <span data-ttu-id="7ea64-500">문제 https://github.com/Azure/azure-powershell/issues/9351 수정</span><span class="sxs-lookup"><span data-stu-id="7ea64-500">Fix for issue https://github.com/Azure/azure-powershell/issues/9351</span></span>
    - <span data-ttu-id="7ea64-501">productId, apiId, groupId 및 userId에 대한 제한을 적용하지 않는 .Net NuGet 버전이 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="7ea64-501">Update .net nuget version, which does not enforce restrictions on productId, apiId, groupId and userId</span></span>
* <span data-ttu-id="7ea64-502">**Get-AzApiManagementProduct** - API를 사용하는 제품에 대한 쿼리 지원이 추가됨</span><span class="sxs-lookup"><span data-stu-id="7ea64-502">**Get-AzApiManagementProduct** - Added support for querying products using Api.</span></span>
  https://github.com/Azure/azure-powershell/issues/9482
* <span data-ttu-id="7ea64-503">**New-AzApiManagementApiRevision** - 새 API 수정(https://github.com/Azure/azure-powershell/issues/9752 )을 만들 때 ApiRevisionDescription이 설정되지 않은 문제가 해결됨</span><span class="sxs-lookup"><span data-stu-id="7ea64-503">**New-AzApiManagementApiRevision** - Fix for issue where ApiRevisionDescription was not being set when creating new api revision https://github.com/Azure/azure-powershell/issues/9752</span></span>
* <span data-ttu-id="7ea64-504">'PsApiManagementOAuth2AuthrozationServer' 모델의 오타가 'PsApiManagementOAuth2AuthorizationServer'로 수정됨</span><span class="sxs-lookup"><span data-stu-id="7ea64-504">Fixed typo in model 'PsApiManagementOAuth2AuthrozationServer' to 'PsApiManagementOAuth2AuthorizationServer'</span></span>

#### <a name="azbatch"></a><span data-ttu-id="7ea64-505">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="7ea64-505">Az.Batch</span></span>
* <span data-ttu-id="7ea64-506">도움말 메시지 및 설명서에서 Windows를 대문자로 시작하도록 오타가 수정됨</span><span class="sxs-lookup"><span data-stu-id="7ea64-506">Fixed typo in help message and documentation to capitalize Windows</span></span>

#### <a name="azcdn"></a><span data-ttu-id="7ea64-507">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="7ea64-507">Az.Cdn</span></span>
* <span data-ttu-id="7ea64-508">CDN 모듈 변환 도우미의 오타가 수정됨</span><span class="sxs-lookup"><span data-stu-id="7ea64-508">Fixed a typo in CDN module conversion helper</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7ea64-509">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7ea64-509">Az.Compute</span></span>
* <span data-ttu-id="7ea64-510">VmssId가 New-AzVMConfig cmdlet에 추가됨</span><span class="sxs-lookup"><span data-stu-id="7ea64-510">Add VmssId to New-AzVMConfig cmdlet</span></span>
* <span data-ttu-id="7ea64-511">TerminateScheduledEvents 및 TerminateScheduledEventNotBeforeTimeoutInMinutes 매개 변수가 New-AzVmssConfig 및 Update-AzVmss에 추가됨</span><span class="sxs-lookup"><span data-stu-id="7ea64-511">Add TerminateScheduledEvents and TerminateScheduledEventNotBeforeTimeoutInMinutes parameters to New-AzVmssConfig and Update-AzVmss</span></span>
* <span data-ttu-id="7ea64-512">HyperVGeneration 속성이 VM 이미지 개체에 추가됨</span><span class="sxs-lookup"><span data-stu-id="7ea64-512">Add HyperVGeneration property to VM image object</span></span>
* <span data-ttu-id="7ea64-513">Host 및 HostGroup 기능이 추가됨</span><span class="sxs-lookup"><span data-stu-id="7ea64-513">Add Host and HostGroup features</span></span>
    - <span data-ttu-id="7ea64-514">새 cmdlet:   New-AzHostGroup, New-AzHost, Get-AzHostGroup, Get-AzHost, Remove-AzHostGroup, Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="7ea64-514">New cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span></span>
    - <span data-ttu-id="7ea64-515">HostId 매개 변수가 New-AzVMConfig 및 New-AzVM 추가됨</span><span class="sxs-lookup"><span data-stu-id="7ea64-515">HostId parameter is added to New-AzVMConfig and New-AzVM</span></span>
* <span data-ttu-id="7ea64-516">'Invoke-AzVMRunCommand' 설명서의 예제에서 올바른 매개 변수 이름을 사용하도록 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="7ea64-516">Update example in 'Invoke-AzVMRunCommand' documentation to use correct parameter name</span></span>
* <span data-ttu-id="7ea64-517">'Set-AzVMDiskEncryptionExtension' 및 'Set-AzVmssDiskEncryptionExtension' 참조 설명서의 '-VolumeType' 설명이 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="7ea64-517">Update '-VolumeType' description in 'Set-AzVMDiskEncryptionExtension' and 'Set-AzVmssDiskEncryptionExtension' reference documentation</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="7ea64-518">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="7ea64-518">Az.DataFactory</span></span>
* <span data-ttu-id="7ea64-519">'New-AzDataFactoryEncryptValue' 설명서에서 'Windows'를 대문자로 시작하도록 오타가 수정됨</span><span class="sxs-lookup"><span data-stu-id="7ea64-519">Fix typo to capitalize 'Windows' in 'New-AzDataFactoryEncryptValue' documentation</span></span>
* <span data-ttu-id="7ea64-520">ADF .Net SDK 버전이 4.1.2로 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="7ea64-520">Updated ADF .Net SDK version to 4.1.2</span></span>
* <span data-ttu-id="7ea64-521">자체 호스팅 통합 런타임을 SSIS Integration Runtime의 프록시로 설정할 수 있도록 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' 및 'DataProxyStagingPath' 매개 변수가 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd에 추가됨</span><span class="sxs-lookup"><span data-stu-id="7ea64-521">Add parameter 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' and 'DataProxyStagingPath' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable set up Self-Hosted Integration Runtime as a proxy for SSIS Integration Runtime</span></span>
* <span data-ttu-id="7ea64-522">PSTriggerRun에서 트리거된 파이프라인, 메시지 및 속성을 표시하고, PSActivityRun에서 작업 유형을 표시하도록 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="7ea64-522">Updated PSTriggerRun to show the triggered pipelines, message and properties, and PSActivityRun to show the activity type</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="7ea64-523">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="7ea64-523">Az.DataLakeStore</span></span>
* <span data-ttu-id="7ea64-524">오류 또는 원격 예외에 대한 Get-DataLakeStoreDeletedItem 중단이 수정됨</span><span class="sxs-lookup"><span data-stu-id="7ea64-524">Fix hanging of Get-DataLakeStoreDeletedItem for any errors or remote exceptions.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="7ea64-525">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="7ea64-525">Az.EventHub</span></span>
* <span data-ttu-id="7ea64-526">#9658 문제 해결: Set-AzEventHubNetworkRuleSet의 VirtualNteworkRule 매개 변수에 대한 오타</span><span class="sxs-lookup"><span data-stu-id="7ea64-526">Fix for issue #9658 : Typo VirtualNteworkRule parameter in Set-AzEventHubNetworkRuleSet</span></span>
* <span data-ttu-id="7ea64-527">#9558 문제 해결: Set-AzEventHubNamespace에서 PUT 대신 PATCH가 사용됨</span><span class="sxs-lookup"><span data-stu-id="7ea64-527">Fix for issue #9558 : Set-AzEventHubNamespace is using PATCH instead of PUT</span></span>
* <span data-ttu-id="7ea64-528">EnableKafka 매개 변수가 Set-AzEventHubNamespace cmdlet에 추가됨</span><span class="sxs-lookup"><span data-stu-id="7ea64-528">added EnableKafka parameter to Set-AzEventHubNamespace cmdlet</span></span>
* <span data-ttu-id="7ea64-529">#9786 문제 해결: Listen(수신 대기) 전용 권한이 있는 규칙을 만들 수 없음</span><span class="sxs-lookup"><span data-stu-id="7ea64-529">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>

#### <a name="azmarketplaceordering"></a><span data-ttu-id="7ea64-530">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="7ea64-530">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="7ea64-531">'Azure'가 모두 소문자인 설명서의 오타가 수정됨</span><span class="sxs-lookup"><span data-stu-id="7ea64-531">Fixed documentation typo where 'Azure' was all lowercase letters</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="7ea64-532">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="7ea64-532">Az.Monitor</span></span>
* <span data-ttu-id="7ea64-533">도움말 설명서에서 잘못된 매개 변수 이름이 수정됨</span><span class="sxs-lookup"><span data-stu-id="7ea64-533">Fixed incorrect parameter name in help documentation</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7ea64-534">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7ea64-534">Az.Network</span></span>
* <span data-ttu-id="7ea64-535">New-AzPrivateLinkServiceIpConfig가 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="7ea64-535">Updated New-AzPrivateLinkServiceIpConfig</span></span>
    - <span data-ttu-id="7ea64-536">서버 쪽에서 사용되지 않으므로 'PublicIpAddress' 매개 변수가 사용되지 않음</span><span class="sxs-lookup"><span data-stu-id="7ea64-536">Deprecated the paramster 'PublicIpAddress' since this is never used in the server side.</span></span>
    - <span data-ttu-id="7ea64-537">현재 IP 구성이 기본 구성인지 여부를 나타내는 하나의 선택적 'Primary' 매개 변수가 추가됨</span><span class="sxs-lookup"><span data-stu-id="7ea64-537">Added one optional parameter 'Primary' that indicate the current ip configuration is primary one or not.</span></span>
* <span data-ttu-id="7ea64-538">SDK의 요청 오류 예외 처리가 향상됨 - 이전의 SDK 예외가 올바르게 처리되지 않아 주요 오류 세부 정보가 표시되지 않은 문제가 해결됨</span><span class="sxs-lookup"><span data-stu-id="7ea64-538">Improved handling of request error exception from SDK   -Fixes the issue that previously SDK exceptions aren't handled correctly which results in key error details not being displayed</span></span>
* <span data-ttu-id="7ea64-539">올바른 IPv6 접두사 길이를 확인하기 위해 Ipv6 IP 접두사에 대한 유효성 검사 논리가 조정됨</span><span class="sxs-lookup"><span data-stu-id="7ea64-539">Adjusted validation logic for Ipv6 IP Prefix to check for correct IPv6 prefix length.</span></span> 
* <span data-ttu-id="7ea64-540">Get-AzVirtualNetworkSubnetConfig가 업데이트됨: 서브넷 리소스 ID별로 가져오도록 설정되는 매개 변수 세트가 추가됨</span><span class="sxs-lookup"><span data-stu-id="7ea64-540">Updated Get-AzVirtualNetworkSubnetConfig: Added parameter set to get by subnet resource id.</span></span>
* <span data-ttu-id="7ea64-541">AzNetworkServiceTag의 Location(위치) 매개 변수에 대한 설명이 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="7ea64-541">Updated description of Location parameter for AzNetworkServiceTag</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="7ea64-542">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="7ea64-542">Az.OperationalInsights</span></span>
* <span data-ttu-id="7ea64-543">'New-AzOperationalInsightsLinuxSyslogDataSource'에 대한 설명서가 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="7ea64-543">Updated documentation for 'New-AzOperationalInsightsLinuxSyslogDataSource'</span></span>
    - <span data-ttu-id="7ea64-544">예제가 추가됨</span><span class="sxs-lookup"><span data-stu-id="7ea64-544">Added example</span></span>
    - <span data-ttu-id="7ea64-545">'-Name' 매개 변수에 대한 설명이 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="7ea64-545">Updated description for '-Name' parameter</span></span>
* <span data-ttu-id="7ea64-546">New-AzOperationalInsightsWindowsEventDataSource에 대한 예제가 추가됨</span><span class="sxs-lookup"><span data-stu-id="7ea64-546">Added an example for New-AzOperationalInsightsWindowsEventDataSource</span></span>
* <span data-ttu-id="7ea64-547">New-AzOperationalInsightsWindowsEventDataSource의 -Name 매개 변수에 대한 설명이 변경됨</span><span class="sxs-lookup"><span data-stu-id="7ea64-547">Changed the description of the -Name parameter for New-AzOperationalInsightsWindowsEventDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="7ea64-548">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="7ea64-548">Az.RecoveryServices</span></span>
* <span data-ttu-id="7ea64-549">'Get-AzRecoveryServicesBackupJobDetail.md'가 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="7ea64-549">Update 'Get-AzRecoveryServicesBackupJobDetail.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="7ea64-550">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7ea64-550">Az.Resources</span></span>
* <span data-ttu-id="7ea64-551">Microsoft 리소스에 대한 새 2019-05-10 API 버전 지원이 추가됨</span><span class="sxs-lookup"><span data-stu-id="7ea64-551">Add support for new api version 2019-05-10 for Microsoft.Resource</span></span>
    - <span data-ttu-id="7ea64-552">변수, 리소스 및 속성에 대한 'copy.count = 0' 지원이 추가됨</span><span class="sxs-lookup"><span data-stu-id="7ea64-552">Add support for 'copy.count = 0' for variables, resources and properties</span></span>
    - <span data-ttu-id="7ea64-553">'condition = false' 또는 'copy.count = 0'인 리소스가 완료 모드에서 삭제됨</span><span class="sxs-lookup"><span data-stu-id="7ea64-553">Resources with 'condition = false' or 'copy.count = 0' will be deleted in complete mode</span></span>
* <span data-ttu-id="7ea64-554">정책을 구독 수준에서 도움말 문서에 할당하는 예제가 추가됨</span><span class="sxs-lookup"><span data-stu-id="7ea64-554">Add an example of assigning policy at subscription level to help doc</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="7ea64-555">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="7ea64-555">Az.ServiceBus</span></span>
* <span data-ttu-id="7ea64-556">#9658 문제 해결: Set-AzServiceBusNetworkRuleSet의 VirtualNetworkRule 매개 변수에 대한 오타</span><span class="sxs-lookup"><span data-stu-id="7ea64-556">Fix for issue #9658 : Typo VirtualNetworkRule parameter in Set-AzServiceBusNetworkRuleSet</span></span>
* <span data-ttu-id="7ea64-557">#9786 문제 해결: Listen(수신 대기) 전용 권한이 있는 규칙을 만들 수 없음</span><span class="sxs-lookup"><span data-stu-id="7ea64-557">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>
* <span data-ttu-id="7ea64-558">큐 및 토픽에 대한 이름 가용성을 확인하는 새 'Test-AzServiceBusNameAvailability' 명령이 추가됨</span><span class="sxs-lookup"><span data-stu-id="7ea64-558">Added new command 'Test-AzServiceBusNameAvailability' to check the name availability for queue and topic</span></span> 

#### <a name="azservicefabric"></a><span data-ttu-id="7ea64-559">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="7ea64-559">Az.ServiceFabric</span></span>
* <span data-ttu-id="7ea64-560">노드 유형 추가 cmdlet 버그 수정:</span><span class="sxs-lookup"><span data-stu-id="7ea64-560">Fix add node type cmdlet bugs:</span></span>
    - <span data-ttu-id="7ea64-561">서비스 패브릭 클러스터와 관련이 없는 다른 vmss가 리소스 그룹에 있을 때 발생하는 NullReferenceException 버그</span><span class="sxs-lookup"><span data-stu-id="7ea64-561">NullReferenceException bug when resource group had other vmss not related to the service fabric cluster.</span></span> <span data-ttu-id="7ea64-562">문제 해결: https://github.com/Azure/azure-powershell/issues/8681</span><span class="sxs-lookup"><span data-stu-id="7ea64-562">Fixes issue: https://github.com/Azure/azure-powershell/issues/8681</span></span>
    - <span data-ttu-id="7ea64-563">virtualNetwork가 클러스터의 다른 리소스 그룹에 있을 때 cmdlet이 실패하는 버그가 수정됨</span><span class="sxs-lookup"><span data-stu-id="7ea64-563">Fix bug where cmdlet failed if virtualNetwork was in a different resource group that the cluster.</span></span> <span data-ttu-id="7ea64-564">문제 해결: https://github.com/Azure/azure-powershell/issues/8407</span><span class="sxs-lookup"><span data-stu-id="7ea64-564">fixes issue: https://github.com/Azure/azure-powershell/issues/8407</span></span>
    - <span data-ttu-id="7ea64-565">Add-AzServiceFabricApplicationCertificate cmdlet이 사용되지 않음</span><span class="sxs-lookup"><span data-stu-id="7ea64-565">Deprecating Add-AzServiceFabricApplicationCertificate cmdlet</span></span>

#### <a name="azsql"></a><span data-ttu-id="7ea64-566">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7ea64-566">Az.Sql</span></span>
* <span data-ttu-id="7ea64-567">이전의 Auditing(감사) cmdlet에 대한 설명서가 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="7ea64-567">Update documentation of old Auditing cmdlets.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="7ea64-568">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="7ea64-568">Az.Storage</span></span>
* <span data-ttu-id="7ea64-569">더 많은 시나리오를 cmdlet 예제에 추가하고 매개 변수 설명을 업데이트하여 Get/Close-AzStorageFileHandle에 대한 도움말이 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="7ea64-569">Update help for Get/Close-AzStorageFileHandle, by add more scenarios to cmdlet examples and update parameter descriptions</span></span>
* <span data-ttu-id="7ea64-570">Blob 업로드 및 Blob 복사에서 StandardBlobTier가 지원됨</span><span class="sxs-lookup"><span data-stu-id="7ea64-570">Support StandardBlobTier in upload blob and copy blob</span></span>
    -  <span data-ttu-id="7ea64-571">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="7ea64-571">Set-AzStorageBlobContent</span></span>
    -  <span data-ttu-id="7ea64-572">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="7ea64-572">Start-AzStorageBlobCopy</span></span>
* <span data-ttu-id="7ea64-573">Blob 복사에서 우선 순위 리하이드레이션이 지원됨</span><span class="sxs-lookup"><span data-stu-id="7ea64-573">Support Rehydrate Priority in copy blob</span></span>
    -  <span data-ttu-id="7ea64-574">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="7ea64-574">Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="7ea64-575">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="7ea64-575">Az.Websites</span></span>
* <span data-ttu-id="7ea64-576">Set-AzWebApp 및 Set-AzWebAppSlot에서 -AppSettings 매개 변수에 대한 설명이 추가됨</span><span class="sxs-lookup"><span data-stu-id="7ea64-576">Add clarification around -AppSettings parameter in Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <a name="250---july-2019"></a><span data-ttu-id="7ea64-577">2.5.0 - 2019년 7월</span><span class="sxs-lookup"><span data-stu-id="7ea64-577">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="7ea64-578">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="7ea64-578">Az.Accounts</span></span>
* <span data-ttu-id="7ea64-579">ClientRuntime의 최신 버전을 사용하도록 일반적인 코드를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-579">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="7ea64-580">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="7ea64-580">Az.ApplicationInsights</span></span>
* <span data-ttu-id="7ea64-581">'Remove-AzApplicationInsightsApiKey' 설명서의 예제 오타 수정</span><span class="sxs-lookup"><span data-stu-id="7ea64-581">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span> 

#### <a name="azautomation"></a><span data-ttu-id="7ea64-582">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="7ea64-582">Az.Automation</span></span>
* <span data-ttu-id="7ea64-583">리소스 문자열의 오타 수정</span><span class="sxs-lookup"><span data-stu-id="7ea64-583">Fix typo in resource string</span></span> 

#### <a name="azcognitiveservices"></a><span data-ttu-id="7ea64-584">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="7ea64-584">Az.CognitiveServices</span></span>
* <span data-ttu-id="7ea64-585">NetworkRuleSet 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-585">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7ea64-586">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7ea64-586">Az.Compute</span></span>
* <span data-ttu-id="7ea64-587">VM 인스턴스 보기 개체의 누락된 속성(ComputerName, OsName, OsVersion 및 HyperVGeneration)을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-587">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="7ea64-588">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="7ea64-588">Az.ContainerRegistry</span></span>
* <span data-ttu-id="7ea64-589">복제 매개 변수의 Remove-AzContainerRegistryReplication에서 오타 수정</span><span class="sxs-lookup"><span data-stu-id="7ea64-589">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="7ea64-590">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/9633 을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="7ea64-590">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="7ea64-591">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="7ea64-591">Az.DataFactory</span></span>
* <span data-ttu-id="7ea64-592">ADF .Net SDK 버전을 4.1.0으로 업데이트</span><span class="sxs-lookup"><span data-stu-id="7ea64-592">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="7ea64-593">'Get-AzDataFactoryV2PipelineRun' 설명서의 오타 수정</span><span class="sxs-lookup"><span data-stu-id="7ea64-593">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="7ea64-594">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="7ea64-594">Az.EventHub</span></span>
* <span data-ttu-id="7ea64-595">SAS 토큰을 생성하기 위해 추가된 새로운 cmmdlet 추가: New-AzEventHubAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="7ea64-595">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="7ea64-596">'관리'만 지정된 경우 authorizationrules 권한에 대한 확인 및 오류 메시지 추가</span><span class="sxs-lookup"><span data-stu-id="7ea64-596">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="7ea64-597">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="7ea64-597">Az.KeyVault</span></span>
* <span data-ttu-id="7ea64-598">인증서 정책에 대한 KeySize 지정을 위한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="7ea64-598">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="7ea64-599">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="7ea64-599">Az.LogicApp</span></span>
* <span data-ttu-id="7ea64-600">모든 맵 유형을 나열하도록 Get-AzIntegrationAccountMap 수정</span><span class="sxs-lookup"><span data-stu-id="7ea64-600">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="7ea64-601">필터링을 위해 새 MapType 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="7ea64-601">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="7ea64-602">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="7ea64-602">Az.ManagedServices</span></span>
* <span data-ttu-id="7ea64-603">API 버전 2019-06-01(GA)에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="7ea64-603">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7ea64-604">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7ea64-604">Az.Network</span></span>
* <span data-ttu-id="7ea64-605">프라이빗 엔드포인트 및 프라이빗 링크 서비스에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="7ea64-605">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="7ea64-606">새 cmdlet</span><span class="sxs-lookup"><span data-stu-id="7ea64-606">New cmdlets</span></span>
        - <span data-ttu-id="7ea64-607">Set-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="7ea64-607">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="7ea64-608">Set-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="7ea64-608">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="7ea64-609">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="7ea64-609">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="7ea64-610">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="7ea64-610">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="7ea64-611">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="7ea64-611">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="7ea64-612">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="7ea64-612">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="7ea64-613">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="7ea64-613">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="7ea64-614">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="7ea64-614">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="7ea64-615">기능에 대한 새로운 명령이 업데이트됨: Virtualnetwork의 서브넷에 있는 PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies 플래그</span><span class="sxs-lookup"><span data-stu-id="7ea64-615">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="7ea64-616">업데이트된 New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="7ea64-616">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="7ea64-617">이 서브넷의 프라이빗 엔드포인트에 네트워크 정책을 적용할지 여부를 나타내는 선택적 매개 변수 -PrivateEndpointNetworkPoliciesFlag가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-617">Added optional parameter -PrivateEndpointNetworkPoliciesFlag that configures whether to apply network policies on private endpoint in this subnet.</span></span>
        - <span data-ttu-id="7ea64-618">이 서브넷의 프라이빗 연결 서비스에 네트워크 정책을 적용할지 여부를 나타내는 선택적 매개 변수 -PrivateLinkServiceNetworkPoliciesFlag가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-618">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag that configures whether to apply network policies network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="7ea64-619">AzPrivateLinkService의 cmdlet 매개 변수 'ServiceName'이 이전 버전과의 호환성을 위해 별칭 'ServiceName'을 사용한 'Name'으로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-619">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="7ea64-620">네트워크 보안 규칙 구성에 ICMP 프로토콜 사용</span><span class="sxs-lookup"><span data-stu-id="7ea64-620">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="7ea64-621">다음 Cmdlet이 업데이트 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-621">Updated cmdlets</span></span>
        - <span data-ttu-id="7ea64-622">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="7ea64-622">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="7ea64-623">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="7ea64-623">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="7ea64-624">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="7ea64-624">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="7ea64-625">New-AzVirtualNetworkGatewayConnection에 대한 구성 가능한 매개 변수로 ConnectionProtocolType (Ikev1/Ikev2) 추가</span><span class="sxs-lookup"><span data-stu-id="7ea64-625">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="7ea64-626">LoadBalancerFrontendIpConfiguration에 PrivateIpAddressVersion 추가</span><span class="sxs-lookup"><span data-stu-id="7ea64-626">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="7ea64-627">업데이트된 cmdlet:</span><span class="sxs-lookup"><span data-stu-id="7ea64-627">Updated cmdlet:</span></span>
        - <span data-ttu-id="7ea64-628">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="7ea64-628">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="7ea64-629">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="7ea64-629">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="7ea64-630">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="7ea64-630">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="7ea64-631">프로브에서 사용자 지정 포트를 지원하기 위한 Application Gateway New-AzApplicationGatewayProbeConfig 명령 업데이트</span><span class="sxs-lookup"><span data-stu-id="7ea64-631">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="7ea64-632">업데이트된 New-AzApplicationGatewayProbeConfig: 백 엔드 서버 검색에 사용되는 선택적 매개 변수 포트가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-632">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="7ea64-633">이 매개 변수는 Standard_V2 및 WAF_V2 SKU에 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-633">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="7ea64-634">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="7ea64-634">Az.OperationalInsights</span></span>
* <span data-ttu-id="7ea64-635">저장된 검색의 기본 버전이 1로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-635">Updated default version for saved searches to be 1.</span></span> 
* <span data-ttu-id="7ea64-636">사용자 지정 로그 null regex 처리가 수정됨</span><span class="sxs-lookup"><span data-stu-id="7ea64-636">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="7ea64-637">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="7ea64-637">Az.RecoveryServices</span></span>
* <span data-ttu-id="7ea64-638">'Get-AzRecoveryServicesBackupJob.md' 업데이트</span><span class="sxs-lookup"><span data-stu-id="7ea64-638">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="7ea64-639">'Get-AzRecoveryServicesBackupContainer.md' 업데이트</span><span class="sxs-lookup"><span data-stu-id="7ea64-639">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="7ea64-640">'Get-AzRecoveryServicesVault.md' 업데이트</span><span class="sxs-lookup"><span data-stu-id="7ea64-640">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="7ea64-641">'Wait-AzRecoveryServicesBackupJob.md' 업데이트</span><span class="sxs-lookup"><span data-stu-id="7ea64-641">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="7ea64-642">'Set-AzRecoveryServicesVaultContext.md' 업데이트</span><span class="sxs-lookup"><span data-stu-id="7ea64-642">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="7ea64-643">'Get-AzRecoveryServicesBackupItem.md' 업데이트</span><span class="sxs-lookup"><span data-stu-id="7ea64-643">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="7ea64-644">'Get-AzRecoveryServicesBackupRecoveryPoint.md' 업데이트</span><span class="sxs-lookup"><span data-stu-id="7ea64-644">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="7ea64-645">'Restore-AzRecoveryServicesBackupItem.md' 업데이트</span><span class="sxs-lookup"><span data-stu-id="7ea64-645">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="7ea64-646">Azure 파일 공유용 컨테이너를 등록 취소하기 위해 서비스 요청 업데이트</span><span class="sxs-lookup"><span data-stu-id="7ea64-646">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="7ea64-647">'Set-AzRecoveryServicesAsrAlertSetting.md' 업데이트</span><span class="sxs-lookup"><span data-stu-id="7ea64-647">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="7ea64-648">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7ea64-648">Az.Resources</span></span>
- <span data-ttu-id="7ea64-649">'New-AzResourceGroupDeployment' 설명서에서 참조된 누락 cmdlet 제거</span><span class="sxs-lookup"><span data-stu-id="7ea64-649">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="7ea64-650">새 API 버전 2019-01-01을 사용하도록 정책 cmdlet 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="7ea64-650">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="7ea64-651">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="7ea64-651">Az.ServiceBus</span></span>
* <span data-ttu-id="7ea64-652">SAS 토큰을 생성하기 위해 추가된 새로운 cmmdlet 추가: New-AzServiceBusAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="7ea64-652">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="7ea64-653">'관리'만 지정된 경우 authorizationrules 권한에 대한 확인 및 오류 메시지 추가</span><span class="sxs-lookup"><span data-stu-id="7ea64-653">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="7ea64-654">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7ea64-654">Az.Sql</span></span>
* <span data-ttu-id="7ea64-655">Set-AzSqlDatabaseSecondary cmdlet에 대한 누락된 예제 수정</span><span class="sxs-lookup"><span data-stu-id="7ea64-655">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="7ea64-656">이메일 주소를 제공하지 않고 설정된 취약성 평가 반복 검색 수정</span><span class="sxs-lookup"><span data-stu-id="7ea64-656">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="7ea64-657">경고 메시지의 작은 오타를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-657">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="7ea64-658">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="7ea64-658">Az.Storage</span></span>
* <span data-ttu-id="7ea64-659">'Get-AzStorageAccount'에 대한 참조 설명서의 예제를 업데이트하여 올바른 매개 변수 이름 사용</span><span class="sxs-lookup"><span data-stu-id="7ea64-659">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="7ea64-660">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="7ea64-660">Az.StorageSync</span></span>
* <span data-ttu-id="7ea64-661">Invoke-AzStorageSyncChangeDetection cmdlet을 추가하는 중입니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-661">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="7ea64-662">TierFilesOlderThanDays를 기념하는 문제 9551 수정</span><span class="sxs-lookup"><span data-stu-id="7ea64-662">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="7ea64-663">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="7ea64-663">Az.Websites</span></span>
* <span data-ttu-id="7ea64-664">Get-AzWebApp 및 Set-AzWebApp에서 일부 SiteConfig 속성을 반환하지 않은 버그 수정</span><span class="sxs-lookup"><span data-stu-id="7ea64-664">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="7ea64-665">Get-AzDeletedWebApp 및 Restore-AzDeletedWebApp에 새 위치 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="7ea64-665">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="7ea64-666">AzWebApp-IncludeSourceWebAppSlots을 사용하여 웹앱 슬롯을 복제하는 버그를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-666">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="7ea64-667">2.4.0 - 2019년 7월</span><span class="sxs-lookup"><span data-stu-id="7ea64-667">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="7ea64-668">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="7ea64-668">Az.Accounts</span></span>
* <span data-ttu-id="7ea64-669">프로필 cmdlet에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="7ea64-669">Add support for profile cmdlets</span></span>
* <span data-ttu-id="7ea64-670">생성된 cmdlet에서 환경 및 데이터 평면에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="7ea64-670">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="7ea64-671">Windows PowerShell의 데이터 평면 cmdlet에대해 일부 경우 잘못된 엔드포인트가 사용되는 버그 수정</span><span class="sxs-lookup"><span data-stu-id="7ea64-671">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="7ea64-672">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="7ea64-672">Az.Advisor</span></span>
* <span data-ttu-id="7ea64-673">Az.Advisor의 GA 릴리스</span><span class="sxs-lookup"><span data-stu-id="7ea64-673">GA release of Az.Advisor</span></span>
* <span data-ttu-id="7ea64-674">이 모듈은 이제 롤업 `Az` 모듈의 일부로 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-674">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="7ea64-675">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="7ea64-675">Az.ApiManagement</span></span>
* <span data-ttu-id="7ea64-676">문제 https://github.com/Azure/azure-powershell/issues/8671 수정</span><span class="sxs-lookup"><span data-stu-id="7ea64-676">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="7ea64-677">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="7ea64-677">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="7ea64-678">사용자 및 제품별 구독을 쿼리하기 위한 지원이 추가됨</span><span class="sxs-lookup"><span data-stu-id="7ea64-678">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="7ea64-679">범위 '/', '/ api, '/ api/echo api'를 사용하여 쿼리하기 위한 지원이 추가됨</span><span class="sxs-lookup"><span data-stu-id="7ea64-679">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="7ea64-680">[https://github.com/Azure/azure-powershell/issues/9307](https://github.com/Azure/azure-powershell/issues/9307 ) 및 https://github.com/Azure/azure-powershell/issues/8432 문제 수정</span><span class="sxs-lookup"><span data-stu-id="7ea64-680">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="7ea64-681">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="7ea64-681">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="7ea64-682">Apis를 가져올 때 'ApiVersion' 및 'ApiVersionSetId'를 지정하기 위한 지원이 추가됨</span><span class="sxs-lookup"><span data-stu-id="7ea64-682">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="7ea64-683">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="7ea64-683">Az.Automation</span></span>
* <span data-ttu-id="7ea64-684">문자열 값을 처리하기 위해 Set-AzAutomationConnectionFieldValue cmdlet 버그를 수정했습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-684">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7ea64-685">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7ea64-685">Az.Compute</span></span>
* <span data-ttu-id="7ea64-686">New-AzImageConfig에 HyperVGeneration 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="7ea64-686">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="7ea64-687">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="7ea64-687">Az.DataFactory</span></span>
* <span data-ttu-id="7ea64-688">get activity runs, get pipeline runs, get trigger runs ADF cmdlet의 출력을 업데이트하여 Select-Object pipe를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-688">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="7ea64-689">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="7ea64-689">Az.EventGrid</span></span>
* <span data-ttu-id="7ea64-690">'New-AzEventGridSubcription' 설명서의 오타 수정</span><span class="sxs-lookup"><span data-stu-id="7ea64-690">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="7ea64-691">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="7ea64-691">Az.IotHub</span></span>
* <span data-ttu-id="7ea64-692">권한 부여 정책 키를 다시 생성하기 위한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="7ea64-692">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7ea64-693">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7ea64-693">Az.Network</span></span>
* <span data-ttu-id="7ea64-694">'RoutingPreference'를 공용 IP 태그에 추가함</span><span class="sxs-lookup"><span data-stu-id="7ea64-694">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="7ea64-695">'Get-AzNetworkServiceTag' 참조 설명서의 예제 개선</span><span class="sxs-lookup"><span data-stu-id="7ea64-695">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="7ea64-696">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="7ea64-696">Az.PolicyInsights</span></span>
* <span data-ttu-id="7ea64-697">Get-AzPolicyState의 null 참조 문제 해결</span><span class="sxs-lookup"><span data-stu-id="7ea64-697">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="7ea64-698">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/9446 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="7ea64-698">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="7ea64-699">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="7ea64-699">Az.OperationalInsights</span></span>
* <span data-ttu-id="7ea64-700">Get-AzOperationalInsightsDataSource에 반환된 CustomLog datasource 모델 수정됨</span><span class="sxs-lookup"><span data-stu-id="7ea64-700">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="7ea64-701">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="7ea64-701">Az.RecoveryServices</span></span>
* <span data-ttu-id="7ea64-702">IaaSVMs에 대한 get-policy 명령 수정</span><span class="sxs-lookup"><span data-stu-id="7ea64-702">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="7ea64-703">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7ea64-703">Az.Resources</span></span>
    - <span data-ttu-id="7ea64-704">Get-AzPolicyState -Top 매개 변수에 대한 도움말 텍스트 수정</span><span class="sxs-lookup"><span data-stu-id="7ea64-704">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="7ea64-705">Get-AzPolicyAlias에 대한 클라이언트 쪽 페이징 지원 추가</span><span class="sxs-lookup"><span data-stu-id="7ea64-705">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="7ea64-706">Set-AzPolicyAssignment, -PolicyParameters 및 -PolicyParametersObject에 대한 새 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="7ea64-706">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="7ea64-707">Policy cmdlet에 대한 몇 가지 문서 및 예제 업데이트</span><span class="sxs-lookup"><span data-stu-id="7ea64-707">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="7ea64-708">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="7ea64-708">Az.ServiceBus</span></span>
* <span data-ttu-id="7ea64-709">문제 #4938 수정 - MaxSizeInMegabytes를 설정할 때 New-AzureRmServiceBusQueue가 BadRequest 반환</span><span class="sxs-lookup"><span data-stu-id="7ea64-709">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="7ea64-710">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7ea64-710">Az.Sql</span></span>
* <span data-ttu-id="7ea64-711">미리 보기 릴리스에서 공개 릴리스로 인스턴스 장애 조치(Failover) 그룹 cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="7ea64-711">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="7ea64-712">새 cmdlet으로 Azure SQL Server\Database Auditing을 지원하세요.</span><span class="sxs-lookup"><span data-stu-id="7ea64-712">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="7ea64-713">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="7ea64-713">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="7ea64-714">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="7ea64-714">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="7ea64-715">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="7ea64-715">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="7ea64-716">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="7ea64-716">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="7ea64-717">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="7ea64-717">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="7ea64-718">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="7ea64-718">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="7ea64-719">취약성 평가 설정에서 이메일 제약 조건 제거</span><span class="sxs-lookup"><span data-stu-id="7ea64-719">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="7ea64-720">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="7ea64-720">Az.Storage</span></span>
* <span data-ttu-id="7ea64-721">다음 cmdlet에서 2개의 매개 변수 '-IndexDocument' 및 '-ErrorDocument404Path'를 필수에서 선택으로 변경하세요.</span><span class="sxs-lookup"><span data-stu-id="7ea64-721">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="7ea64-722">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="7ea64-722">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="7ea64-723">예제를 추가하여 Get-AzStorageBlobContent의 도움말 업데이트</span><span class="sxs-lookup"><span data-stu-id="7ea64-723">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="7ea64-724">StorageException으로 cmdlet이 실패한 경우 자세한 오류 정보 표시</span><span class="sxs-lookup"><span data-stu-id="7ea64-724">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="7ea64-725">Azure Files AAD DS 인증으로 스토리지 계정 생성 또는 업데이트 지원</span><span class="sxs-lookup"><span data-stu-id="7ea64-725">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="7ea64-726">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="7ea64-726">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="7ea64-727">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="7ea64-727">Set-AzStorageAccount</span></span>
* <span data-ttu-id="7ea64-728">파일 공유, 파일 디렉터리 또는 파일의 목록 지원 또는 파일 핸들 닫기</span><span class="sxs-lookup"><span data-stu-id="7ea64-728">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="7ea64-729">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="7ea64-729">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="7ea64-730">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="7ea64-730">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="7ea64-731">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="7ea64-731">Az.StorageSync</span></span>
* <span data-ttu-id="7ea64-732">이 모듈은 이제 롤업 `Az` 모듈의 일부로 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-732">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="7ea64-733">2.3.2 - 2019년 6월</span><span class="sxs-lookup"><span data-stu-id="7ea64-733">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="7ea64-734">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="7ea64-734">Az.Accounts</span></span>
* <span data-ttu-id="7ea64-735">함수 호출에 대해 일부 경우 잘못된 URL이 사용되는 버그 수정</span><span class="sxs-lookup"><span data-stu-id="7ea64-735">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="7ea64-736">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/8983 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="7ea64-736">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="7ea64-737">AzureRM에서 Az cmdlet으로의 별칭 문제 해결</span><span class="sxs-lookup"><span data-stu-id="7ea64-737">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="7ea64-738">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="7ea64-738">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="7ea64-739">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="7ea64-739">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7ea64-740">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7ea64-740">Az.Compute</span></span>
* <span data-ttu-id="7ea64-741">New-AzVm 및 New-AzVmss 단순 매개 변수 집합은 이제 'ProximityPlacementGroup'매개 변수를 허용합니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-741">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="7ea64-742">'New-AzVM' 참조 설명서에서 오타 수정</span><span class="sxs-lookup"><span data-stu-id="7ea64-742">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="7ea64-743">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="7ea64-743">Az.Dns</span></span>
* <span data-ttu-id="7ea64-744">'Set-AzDnsZone' 도움말 예제의 오타가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-744">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="7ea64-745">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="7ea64-745">Az.EventGrid</span></span>
* <span data-ttu-id="7ea64-746">2019-06-01 API 버전을 사용하도록 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-746">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="7ea64-747">새 cmdlet:</span><span class="sxs-lookup"><span data-stu-id="7ea64-747">New cmdlets:</span></span>
    - <span data-ttu-id="7ea64-748">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="7ea64-748">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="7ea64-749">새 Azure Event Grid 도메인을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-749">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="7ea64-750">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="7ea64-750">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="7ea64-751">Event Grid 도메인의 세부 정보를 가져오거나 현재 Azure 구독의 모든 Event Grid 도메인 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-751">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="7ea64-752">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="7ea64-752">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="7ea64-753">Azure Event Grid 도메인을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-753">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="7ea64-754">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="7ea64-754">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="7ea64-755">Azure Event Grid 도메인에 대한 공유 액세스 키를 다시 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-755">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="7ea64-756">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="7ea64-756">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="7ea64-757">Event Grid 도메인 이벤트를 게시하는 데 사용되는 공유 액세스 키를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-757">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="7ea64-758">New-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="7ea64-758">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="7ea64-759">새 Azure Event Grid 도메인 토픽을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-759">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="7ea64-760">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="7ea64-760">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="7ea64-761">Event Grid 도메인 토픽의 세부 사항을 가져오거나, 현재 Azure의 특정 Event Grid 도메인 아래의 모든 Event Grid 도메인 토픽 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-761">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span> 
    - <span data-ttu-id="7ea64-762">Remove-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="7ea64-762">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="7ea64-763">기존 Azure Event Grid 도메인 토픽을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-763">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="7ea64-764">다음 Cmdlet이 업데이트 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-764">Updated cmdlets:</span></span>
    - <span data-ttu-id="7ea64-765">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="7ea64-765">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="7ea64-766">새로운 Event Grid 도메인 및 Event Grid 도메인 토픽에 대한 파이핑을 지원하기 위해 새로운 필수 매개 변수를 추가하여 이러한 리소스 아래에 새 이벤트 구독을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-766">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="7ea64-767">새로운 Event Grid 도메인 이름 및 Event Grid 도메인 토픽 이름을 지정하기 위해 새로운 필수 매개 변수를 추가하여 이러한 리소스 아래에 새 이벤트 구독을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-767">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="7ea64-768">기존 매개 변수(예: EndPointType, SubjectBeginsWith 등)를 재사용할 수 있도록 도메인 및 도메인 토픽에 대한 새로운 매개 변수 집합을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-768">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="7ea64-769">지정을 위한 새로운 선택적 매개 변수를 추가</span><span class="sxs-lookup"><span data-stu-id="7ea64-769">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="7ea64-770">이벤트 구독 만료 날짜,</span><span class="sxs-lookup"><span data-stu-id="7ea64-770">Event subscription expiration date,</span></span>
            - <span data-ttu-id="7ea64-771">고급 필터링 매개 변수.</span><span class="sxs-lookup"><span data-stu-id="7ea64-771">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="7ea64-772">대상으로 servicebusqueue에 대한 새 열거형을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-772">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="7ea64-773">-IncludedEventType 옵션에서 'All' 사용을 허용하지 않고 다음으로 대체함</span><span class="sxs-lookup"><span data-stu-id="7ea64-773">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span> 
    - <span data-ttu-id="7ea64-774">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="7ea64-774">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="7ea64-775">결과 페이지 매김 및 필터링을 지원하는 새로운 선택적 매개 변수(Top, ODataQuery 및 NextLink)를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-775">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="7ea64-776">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="7ea64-776">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="7ea64-777">Event Grid 도메인 및 Event Grid 도메인 토픽에 대한 파이핑을 지원하기 위해 새로운 필수 매개 변수를 추가하여 이러한 리소스 아래에 기존 이벤트 구독을 제거할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-777">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="7ea64-778">Event Grid 도메인 이름 및 Event Grid 도메인 토픽 이름을 지정하기 위해 새로운 필수 매개 변수를 추가하여 이러한 리소스 아래에 기존 이벤트 구독을 제거할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-778">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="7ea64-779">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="7ea64-779">Az.FrontDoor</span></span>
* <span data-ttu-id="7ea64-780">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="7ea64-780">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="7ea64-781">변환 지원 및 새 연산자 자동 완성 값(RegEx)을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-781">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="7ea64-782">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="7ea64-782">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="7ea64-783">새 자동 완성 값 추가</span><span class="sxs-lookup"><span data-stu-id="7ea64-783">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7ea64-784">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7ea64-784">Az.Network</span></span>
* <span data-ttu-id="7ea64-785">Microsoft Azure Virtual Network 게이트웨이 리소스에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="7ea64-785">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="7ea64-786">새 cmdlet</span><span class="sxs-lookup"><span data-stu-id="7ea64-786">New cmdlets</span></span>
        - <span data-ttu-id="7ea64-787">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="7ea64-787">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="7ea64-788">AvailablePrivateEndpointType 추가</span><span class="sxs-lookup"><span data-stu-id="7ea64-788">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="7ea64-789">새 cmdlet</span><span class="sxs-lookup"><span data-stu-id="7ea64-789">New cmdlets</span></span> 
        - <span data-ttu-id="7ea64-790">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="7ea64-790">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="7ea64-791">PrivatePrivateLinkService 추가</span><span class="sxs-lookup"><span data-stu-id="7ea64-791">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="7ea64-792">새 cmdlet</span><span class="sxs-lookup"><span data-stu-id="7ea64-792">New cmdlets</span></span> 
        - <span data-ttu-id="7ea64-793">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="7ea64-793">Get-AzPrivateLinkService</span></span> 
        - <span data-ttu-id="7ea64-794">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="7ea64-794">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="7ea64-795">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="7ea64-795">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="7ea64-796">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="7ea64-796">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="7ea64-797">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="7ea64-797">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="7ea64-798">PrivateEndpoint 추가</span><span class="sxs-lookup"><span data-stu-id="7ea64-798">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="7ea64-799">새 cmdlet</span><span class="sxs-lookup"><span data-stu-id="7ea64-799">New cmdlets</span></span>
        - <span data-ttu-id="7ea64-800">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="7ea64-800">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="7ea64-801">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="7ea64-801">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="7ea64-802">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="7ea64-802">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="7ea64-803">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="7ea64-803">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="7ea64-804">기능에 대한 새로운 명령이 업데이트됨: VpnConnection 상의 UseLocalAzureIpAddress 플래그</span><span class="sxs-lookup"><span data-stu-id="7ea64-804">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="7ea64-805">New-AzVpnConnection이 업데이트됨: 선택적 매개 변수 -UseLocalAzureIpAddress를 추가하여 로컬 Azure IP 주소가 연결을 시작하는 동안 소스 주소로 사용되어야 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-805">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="7ea64-806">Set-AzVpnConnection이 업데이트됨: 선택적 매개 변수 -UseLocalAzureIpAddress를 추가하여 로컬 Azure IP 주소가 연결을 시작하는 동안 소스 주소로 사용되어야 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-806">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="7ea64-807">ExpressRoute 피어링에 읽기 전용 필드 PeeredConnections가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-807">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="7ea64-808">ExpressRoute에 읽기 전용 필드 GlobalReachEnabled가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-808">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="7ea64-809">ExpressRouteCircuit 모델에서 AllowGlobalReach 필드의 사용 중단을 부르는 호환성이 손상되는 변경 속성이 추가됨</span><span class="sxs-lookup"><span data-stu-id="7ea64-809">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="7ea64-810">AzApplicationGatewayRedirectConfiguration cmdlet에서 TargetListenerID를 사용하는 중의 8756 오류 문제가 해결됨</span><span class="sxs-lookup"><span data-stu-id="7ea64-810">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="7ea64-811">다시 쓰기 규칙 세트가 설정되지 못하게 하는 New-AzApplicationGatewayPathRuleConfig의 버그를 수정했습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-811">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="7ea64-812">NetworkInterfaceIpConfiguration에 VirtualNetworkTaps가 표시되는 방식이 수정됨</span><span class="sxs-lookup"><span data-stu-id="7ea64-812">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="7ea64-813">모든 파트를 나열하도록 Cortex Get cmdlet이 수정됨</span><span class="sxs-lookup"><span data-stu-id="7ea64-813">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="7ea64-814">ExpressRouteGateways, VpnGateway에 대한 VirtualHub 참조 생성 수정됨</span><span class="sxs-lookup"><span data-stu-id="7ea64-814">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="7ea64-815">AzureFirewall 및 NatGateway의 가용성 영역에 대한 지원 추가됨</span><span class="sxs-lookup"><span data-stu-id="7ea64-815">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="7ea64-816">Get-AzNetworkServiceTag cmdlet 추가됨</span><span class="sxs-lookup"><span data-stu-id="7ea64-816">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="7ea64-817">Azure Firewall에 대한 여러 공용 IP 주소에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="7ea64-817">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="7ea64-818">New-AzFirewall cmdlet이 업데이트됨:</span><span class="sxs-lookup"><span data-stu-id="7ea64-818">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="7ea64-819">하나 이상의 공용 IP 주소 개체를 허용하는 매개 변수 -PublicIpAddress 추가됨</span><span class="sxs-lookup"><span data-stu-id="7ea64-819">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="7ea64-820">Virtual Network 개체를 허용하는 매개 변수 -VirtualNetwork 추가됨</span><span class="sxs-lookup"><span data-stu-id="7ea64-820">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="7ea64-821">방화벽 개체에 AddPublicIpAddress 및 RemovePublicIpAddress 메서드 추가됨 - 공용 IP 주소 개체를 입력으로 허용</span><span class="sxs-lookup"><span data-stu-id="7ea64-821">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="7ea64-822">매개 변수 -PublicIpName 및 -VirtualNetworkName이 더 이상 사용되지 않음</span><span class="sxs-lookup"><span data-stu-id="7ea64-822">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span> 
* <span data-ttu-id="7ea64-823">기능에 대한 새로운 명령이 업데이트됨: VpnClient AAD 인증 옵션을 가상 네트워크 게이트웨이 리소스로 설정했습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-823">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span> 
    - <span data-ttu-id="7ea64-824">New-AzVirtualNetworkGateway가 업데이트됨: 게이트웨이에서 VpnClient AAD 인증 옵션을 설정할 수 있도록 선택적 매개 변수 AadTenantUri, AadAudienceId, AadIssuerUri가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-824">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="7ea64-825">Set-AzVirtualNetworkGateway가 업데이트됨: 게이트웨이에서 VpnClient AAD 인증 옵션을 설정할 수 있도록 선택적 매개 변수 AadTenantUri, AadAudienceId, AadIssuerUri가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-825">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="7ea64-826">Set-AzVirtualNetworkGateway가 업데이트됨: 게이트웨이에서 VpnClient AAD 인증 옵션을 제거할 수 있도록 선택적인 스위치 매개 변수 RemoveAadAuthentication이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-826">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="7ea64-827">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="7ea64-827">Az.OperationalInsights</span></span>
* <span data-ttu-id="7ea64-828">'New-AzureRmOperationalInsightsWorkspace' 명령에서 **pergb2018** 가격 책정 계층 사용</span><span class="sxs-lookup"><span data-stu-id="7ea64-828">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="7ea64-829">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7ea64-829">Az.Resources</span></span>
* <span data-ttu-id="7ea64-830">추가 템플릿 내보내기 옵션 지원</span><span class="sxs-lookup"><span data-stu-id="7ea64-830">Support for additional Template Export options</span></span>
    - <span data-ttu-id="7ea64-831">Export-AzResourceGroup에 '-SkipResourceNameParameterization' 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="7ea64-831">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="7ea64-832">Export-AzResourceGroup에 '-SkipAllParameterization' 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="7ea64-832">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="7ea64-833">내보낸 리소스 필터링을 위해 Export-AzResourceGroup에 '-Resource' 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="7ea64-833">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="7ea64-834">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="7ea64-834">Az.ServiceFabric</span></span>
* <span data-ttu-id="7ea64-835">일부 경우 잘못된 지문을 가져오는 추가 인증서 ByExistingKeyVault 수정</span><span class="sxs-lookup"><span data-stu-id="7ea64-835">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="7ea64-836">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7ea64-836">Az.Sql</span></span>
* <span data-ttu-id="7ea64-837">Advanced Threat Protection 스토리지 엔드포인트 접미사 수정</span><span class="sxs-lookup"><span data-stu-id="7ea64-837">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="7ea64-838">Advanced Data Security가 Advanced Threat Protection 정책을 재정의하는 것을 수정</span><span class="sxs-lookup"><span data-stu-id="7ea64-838">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="7ea64-839">고객이 TDE 키를 추가하고 관리되는 인스턴스에 TDE 보호기를 설정할 수 있도록 Management.Sql용 새 Cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="7ea64-839">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="7ea64-840">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="7ea64-840">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="7ea64-841">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="7ea64-841">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="7ea64-842">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="7ea64-842">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="7ea64-843">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="7ea64-843">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="7ea64-844">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="7ea64-844">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="7ea64-845">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="7ea64-845">Az.Storage</span></span>
* <span data-ttu-id="7ea64-846">스토리지 계정 생성 시 종류 FileStorage 및 SkuName Premium_ZRS 지원</span><span class="sxs-lookup"><span data-stu-id="7ea64-846">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="7ea64-847">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="7ea64-847">New-AzStorageAccount</span></span>
* <span data-ttu-id="7ea64-848">BLOB immutability cmdlet의 설명 명확화</span><span class="sxs-lookup"><span data-stu-id="7ea64-848">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="7ea64-849">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="7ea64-849">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="7ea64-850">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="7ea64-850">Az.Websites</span></span>
* <span data-ttu-id="7ea64-851">Get-AzWebAppCertificate를 클라이언트 대신 서버의 리소스 그룹별로 필터링하도록 최적화</span><span class="sxs-lookup"><span data-stu-id="7ea64-851">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="7ea64-852">Get-AzWebAppSnapshot에 -UseDisasterRecovery 스위치 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="7ea64-852">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="7ea64-853">2.2.0 - 2019년 6월</span><span class="sxs-lookup"><span data-stu-id="7ea64-853">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="7ea64-854">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="7ea64-854">Az.Cdn</span></span>
* <span data-ttu-id="7ea64-855">cmdlet에서 2019-04-15 API 버전 기반의 rulesEngine 기능을 지원하도록 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-855">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7ea64-856">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7ea64-856">Az.Compute</span></span>
* <span data-ttu-id="7ea64-857">작업을 시작하여 완료되기 전에 즉시 반환하는 `NoWait` 매개 변수가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-857">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="7ea64-858">다음 Cmdlet이 업데이트 되었습니다.   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="7ea64-858">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="7ea64-859">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="7ea64-859">Az.EventHub</span></span>
* <span data-ttu-id="7ea64-860">#9231 수정 - Get-AzEventHubNamespace에서 태그를 반환하지 않음</span><span class="sxs-lookup"><span data-stu-id="7ea64-860">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="7ea64-861">#9230 수정 - Get-AzEventHubNamespace에서 ResourceGroupName 대신 ResourceGroup을 반환함</span><span class="sxs-lookup"><span data-stu-id="7ea64-861">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7ea64-862">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7ea64-862">Az.Network</span></span>
* <span data-ttu-id="7ea64-863">Nat Gateway에 대한 ResourceId 및 InputObject 업데이트</span><span class="sxs-lookup"><span data-stu-id="7ea64-863">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="7ea64-864">ResourceId 및 InputObject에 대한 별칭 추가</span><span class="sxs-lookup"><span data-stu-id="7ea64-864">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="7ea64-865">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="7ea64-865">Az.PolicyInsights</span></span>
* <span data-ttu-id="7ea64-866">Get-AzPolicyEvent에서 Null 참조 문제 해결</span><span class="sxs-lookup"><span data-stu-id="7ea64-866">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="7ea64-867">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="7ea64-867">Az.RecoveryServices</span></span>
* <span data-ttu-id="7ea64-868">IaaSVM 정책 최소 보존 기간(일)이 1에서 7로 변경됨</span><span class="sxs-lookup"><span data-stu-id="7ea64-868">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="7ea64-869">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="7ea64-869">Az.ServiceBus</span></span>
* <span data-ttu-id="7ea64-870">#9182 문제 해결 - Get-AzServiceBusNamespace에서 ResourceGroupName 대신 ResourceGroup을 반환</span><span class="sxs-lookup"><span data-stu-id="7ea64-870">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="7ea64-871">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="7ea64-871">Az.ServiceFabric</span></span>
* <span data-ttu-id="7ea64-872">'Update-AzServiceFabricReliability' 오류 메시지의 오타 수정</span><span class="sxs-lookup"><span data-stu-id="7ea64-872">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="7ea64-873">Service Fabric 명령줄에서 누락된 문자 수정</span><span class="sxs-lookup"><span data-stu-id="7ea64-873">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="7ea64-874">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7ea64-874">Az.Sql</span></span>
* <span data-ttu-id="7ea64-875">Managed Instance에 대한 AutoDr을 지원하기 위해 New-AzureSqlInstance cmdlet에 대한 DnsZonePartner 매개 변수를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-875">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="7ea64-876">Get-AzSqlDatabaseSecureConnectionPolicy cmdlet 사용 중단</span><span class="sxs-lookup"><span data-stu-id="7ea64-876">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="7ea64-877">Threat Detection(위협 탐지) cmdlet 이름을 Advanced Threat Protection으로 변경함</span><span class="sxs-lookup"><span data-stu-id="7ea64-877">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="7ea64-878">새 AzSqlInstance -StorageSizeInGB 및 -LicenseType 매개 변수는 이제 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-878">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="7ea64-879">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="7ea64-879">Az.Websites</span></span>
* <span data-ttu-id="7ea64-880">-WebApp 속성에서 Set-AzWebApp 및 Set-AzWebAppSlot을 사용하면 태그가 제거되는 문제를 해결함</span><span class="sxs-lookup"><span data-stu-id="7ea64-880">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="7ea64-881">2.1.0 - 2019년 5월</span><span class="sxs-lookup"><span data-stu-id="7ea64-881">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="7ea64-882">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="7ea64-882">Az.ApiManagement</span></span>
* <span data-ttu-id="7ea64-883">글로벌 및 API 범위에서 진단을 관리하기 위한 새 cmdlet을 만들었습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-883">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="7ea64-884">**Get-AzApiManagementDiagnostic** - 글로벌 또는 API 범위가 구성된 진단 가져오기</span><span class="sxs-lookup"><span data-stu-id="7ea64-884">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="7ea64-885">**New-AzApiManagementDiagnostic** - 글로벌 범위 또는 API 범위에서 새 진단 만들기</span><span class="sxs-lookup"><span data-stu-id="7ea64-885">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="7ea64-886">**New-AzApiManagementHttpMessageDiagnostic** - 기록할 Headers(헤더) 및 Body Bytes(본문 바이트 수) 크기에 대한 진단 설정 만들기</span><span class="sxs-lookup"><span data-stu-id="7ea64-886">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="7ea64-887">**New-AzApiManagementPipelineDiagnosticSetting** - 게이트웨이로 들어오고 나가는 HTTP 메시지에 대한 진단 설정 만들기</span><span class="sxs-lookup"><span data-stu-id="7ea64-887">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="7ea64-888">**New-AzApiManagementSamplingSetting** - 진단 요청/응답에 대한 샘플링 설정 만들기</span><span class="sxs-lookup"><span data-stu-id="7ea64-888">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="7ea64-889">**Remove-AzApiManagementDiagnostic** - 글로벌 또는 API 범위에서 진단 엔터티 제거</span><span class="sxs-lookup"><span data-stu-id="7ea64-889">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="7ea64-890">**Set-AzApiManagementDiagnostic** - 글로벌 또는 API 범위에서 진단 엔터티 업데이트</span><span class="sxs-lookup"><span data-stu-id="7ea64-890">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="7ea64-891">ApiManagement 서비스에서 캐시를 관리하기 위한 새 cmdlet을 만들었습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-891">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="7ea64-892">**Get-AzApiManagementCache** - 식별자 또는 모든 캐시로 지정된 캐시의 세부 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="7ea64-892">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="7ea64-893">**New-AzApiManagementCache** - 특정 Azure 'region'(지역)에 새 'default'(기본) 캐시 만들기</span><span class="sxs-lookup"><span data-stu-id="7ea64-893">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="7ea64-894">**Remove-AzApiManagementCache** - 캐시 제거</span><span class="sxs-lookup"><span data-stu-id="7ea64-894">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="7ea64-895">**Update-AzApiManagementCache** - 캐시 업데이트</span><span class="sxs-lookup"><span data-stu-id="7ea64-895">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="7ea64-896">API 스키마 관리하기 위한 새 cmdlet을 만들었습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-896">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="7ea64-897">**New-AzApiManagementSchema** - API에 대한 새 스키마 만들기</span><span class="sxs-lookup"><span data-stu-id="7ea64-897">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="7ea64-898">**Get-AzApiManagementSchema** - API에 구성된 스키마 가져오기</span><span class="sxs-lookup"><span data-stu-id="7ea64-898">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="7ea64-899">**Remove-AzApiManagementSchema** - API에 구성된 스키마 제거</span><span class="sxs-lookup"><span data-stu-id="7ea64-899">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="7ea64-900">**Set-AzApiManagementSchema** - API에 구성된 스키마 업데이트</span><span class="sxs-lookup"><span data-stu-id="7ea64-900">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="7ea64-901">사용자 토큰을 생성하기 위한 새 cmdlet을 만들었습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-901">Created new Cmdlet for generating a User Token.</span></span> 
    - <span data-ttu-id="7ea64-902">**New-AzApiManagementUserToken** - 기본적으로 8시간 동안 유효한 새 사용자 토큰을 생성합니다. 'GIT' 사용자에 대한 토큰은 이 cmdlet을 사용하여 생성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-902">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="7ea64-903">네트워크 상태를 검색하기 위한 새 cmdlet을 만들었습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-903">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="7ea64-904">**Get-AzApiManagementNetworkStatus** - API Management 서비스에서 사용하는 리소스의 네트워크 상태 연결을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-904">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="7ea64-905">ApiManagement 서비스를 가상 네트워크에 배포하고 종속성이 손상되었는지 여부를 확인할 때 유용합니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-905">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="7ea64-906">**New-AzApiManagement** cmdlet에서 ApiManagement 서비스를 관리하도록 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-906">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span> 
    - <span data-ttu-id="7ea64-907">새 '소비' SKU 지원이 추가됨</span><span class="sxs-lookup"><span data-stu-id="7ea64-907">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="7ea64-908">'소비' SKU에 대해 'EnableClientCertificate' 플래그를 설정하기 위한 지원이 추가됨</span><span class="sxs-lookup"><span data-stu-id="7ea64-908">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="7ea64-909">새 **New-AzApiManagementSslSetting** cmdlet을 사용하면 'Backend(백 엔드)' 및 'Frontend'(프런트 엔드)에서 'TLS/SSL' 설정을 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-909">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="7ea64-910">또한 ApiManagement 서비스의 'Frontend'에서 '3DES'와 같은 'Ciphers'와 'Http2'와 같은 'ServerProtocols'를 구성하는 데 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-910">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="7ea64-911">ApiManagement 서비스에서 'DeveloperPortal' 호스트 이름을 구성하기 위한 지원이 추가됨</span><span class="sxs-lookup"><span data-stu-id="7ea64-911">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="7ea64-912">**Get-AzApiManagementSsoToken** cmdlet에서 'PsApiManagement' 개체를 입력으로 사용하도록 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-912">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="7ea64-913">cmdlet에서 오류 메시지를 인라인으로 표시하도록 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-913">Updated the cmdlet to display Error Messages inline</span></span> 
     > <span data-ttu-id="7ea64-914">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : 오류 코드: ValidationError 오류 메시지: 하나 이상의 필드에 잘못된 값이 있습니다. 오류 세부 정보:    [Code=ValidationError, Message=줄 3, 열 10의 'log-to-eventhub' 요소에 오류가 있습니다.: 로거를 찾지 못함, Target=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="7ea64-914">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="7ea64-915">**Export-AzApiManagementApi** cmdlet에서 API를 'OpenApi 3.0' 형식으로 내보내도록 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-915">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="7ea64-916">**Import-AzApiManagementApi** cmdlet을 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-916">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="7ea64-917">'OpenApi 3.0' 문서 사양에서 API 가져오기</span><span class="sxs-lookup"><span data-stu-id="7ea64-917">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="7ea64-918">문서('Swagger', 'Wadl', 'Wsdl', 'OpenApi')에 지정된 'PsApiManagementSchema' 속성 재정의</span><span class="sxs-lookup"><span data-stu-id="7ea64-918">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="7ea64-919">문서에 지정된 'ServiceUrl' 속성 재정의</span><span class="sxs-lookup"><span data-stu-id="7ea64-919">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="7ea64-920">**Get-AzApiManagementPolicy** cmdlet에서 'rawxml'을 사용하여 이스케이프된 비 Xml 'format'(형식)의 정책을 반환하도록 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-920">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="7ea64-921">**Set-AzApiManagementPolicy** cmdlet에서 'rawxml'을 사용하여 이스케이프된 비 Xml 'format'의 정책을 수락하고, 'xml'을 사용하여 이스케이프된 Xml 'format'의 정책을 수락하도록 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-921">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="7ea64-922">**New-AzApiManagementApi** cmdlet을 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-922">Updated cmdlet **New-AzApiManagementApi**</span></span> 
    - <span data-ttu-id="7ea64-923">'OpenId' 권한 부여 서버를 사용하여 API 구성</span><span class="sxs-lookup"><span data-stu-id="7ea64-923">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="7ea64-924">'ApiVersionSet'에서 API 만들기</span><span class="sxs-lookup"><span data-stu-id="7ea64-924">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="7ea64-925">'SourceApiId' 및 'SourceApiRevision'을 사용하여 API 복제</span><span class="sxs-lookup"><span data-stu-id="7ea64-925">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="7ea64-926">API 범위에서 'SubscriptionRequired' 구성 가능</span><span class="sxs-lookup"><span data-stu-id="7ea64-926">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="7ea64-927">**Set-AzApiManagementApi** cmdlet을 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-927">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="7ea64-928">'OpenId' 권한 부여 서버를 사용하여 API 구성</span><span class="sxs-lookup"><span data-stu-id="7ea64-928">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="7ea64-929">API를 'ApiVersionSet'으로 업데이트</span><span class="sxs-lookup"><span data-stu-id="7ea64-929">To updated an API into an 'ApiVersionSet'</span></span>    
    - <span data-ttu-id="7ea64-930">API 범위에서 'SubscriptionRequired' 구성 가능</span><span class="sxs-lookup"><span data-stu-id="7ea64-930">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="7ea64-931">**New-AzApiManagementRevision** cmdlet을 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-931">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="7ea64-932">'SourceApiRevision'을 사용하여 기존 수정 버전 복제(태그, 제품, 작업 및 정책 복사).</span><span class="sxs-lookup"><span data-stu-id="7ea64-932">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="7ea64-933">새 수정 버전은 부모의 'ApiId'를 가정합니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-933">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="7ea64-934">'ApiRevisionDescription' 제공</span><span class="sxs-lookup"><span data-stu-id="7ea64-934">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="7ea64-935">API 복제 시 'ServiceUrl' 재정의</span><span class="sxs-lookup"><span data-stu-id="7ea64-935">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="7ea64-936">**New-AzApiManagementIdentityProvider** cmdlet을 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-936">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="7ea64-937">'Authority'를 사용하여 'AAD' 또는 'AADB2C' 구성</span><span class="sxs-lookup"><span data-stu-id="7ea64-937">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="7ea64-938">'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' 및 'PasswordResetPolicy' 설정</span><span class="sxs-lookup"><span data-stu-id="7ea64-938">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="7ea64-939">**New-AzApiManagementSubscription** cmdlet을 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-939">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="7ea64-940">'Scope' 및 'UserId'를 사용하여 새 SubscriptonModel 설명</span><span class="sxs-lookup"><span data-stu-id="7ea64-940">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="7ea64-941">'ProductId' 및 'UserId'를 사용하여 이전 구독 모델 설명</span><span class="sxs-lookup"><span data-stu-id="7ea64-941">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="7ea64-942">구독 수준에서 'AllowTracing'을 사용하도록 설정하는 지원 추가</span><span class="sxs-lookup"><span data-stu-id="7ea64-942">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="7ea64-943">**Set-AzApiManagementSubscription** cmdlet을 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-943">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="7ea64-944">'Scope' 및 'UserId'를 사용하여 새 SubscriptonModel 설명</span><span class="sxs-lookup"><span data-stu-id="7ea64-944">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="7ea64-945">'ProductId' 및 'UserId'를 사용하여 이전 구독 모델 설명</span><span class="sxs-lookup"><span data-stu-id="7ea64-945">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="7ea64-946">구독 수준에서 'AllowTracing'을 사용하도록 설정하는 지원 추가</span><span class="sxs-lookup"><span data-stu-id="7ea64-946">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="7ea64-947">다음 cmdlet에서 'ResourceId'를 입력으로 수락하도록 업데이트했습니다</span><span class="sxs-lookup"><span data-stu-id="7ea64-947">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="7ea64-948">'New-AzApiManagementContext'</span><span class="sxs-lookup"><span data-stu-id="7ea64-948">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="7ea64-949">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="7ea64-949">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="7ea64-950">'Get-AzApiManagementApiRelease'</span><span class="sxs-lookup"><span data-stu-id="7ea64-950">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="7ea64-951">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="7ea64-951">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="7ea64-952">'Get-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="7ea64-952">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="7ea64-953">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="7ea64-953">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="7ea64-954">'Get-AzApiManagementAuthorizationServer'</span><span class="sxs-lookup"><span data-stu-id="7ea64-954">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="7ea64-955">'Get-AzApiManagementBackend'</span><span class="sxs-lookup"><span data-stu-id="7ea64-955">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="7ea64-956">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="7ea64-956">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="7ea64-957">'Get-AzApiManagementCertificate'</span><span class="sxs-lookup"><span data-stu-id="7ea64-957">'Get-AzApiManagementCertificate'</span></span> 
    - <span data-ttu-id="7ea64-958">'Remove-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="7ea64-958">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="7ea64-959">'Remove-AzApiManagementSubscription'</span><span class="sxs-lookup"><span data-stu-id="7ea64-959">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="7ea64-960">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="7ea64-960">Az.Automation</span></span>
* <span data-ttu-id="7ea64-961">Get-AzAutomationJobOutputRecord에서 JSON 및 Text 레코드 값을 처리하도록 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-961">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="7ea64-962">문제 https://github.com/Azure/azure-powershell/issues/7977 수정</span><span class="sxs-lookup"><span data-stu-id="7ea64-962">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="7ea64-963">문제 https://github.com/Azure/azure-powershell/issues/8600 수정</span><span class="sxs-lookup"><span data-stu-id="7ea64-963">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="7ea64-964">Start-AzAutomationDscCompilationJob에서 완료될 때까지 기다리지 않고 작업을 바로 시작하도록 변경했습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-964">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="7ea64-965">문제 https://github.com/Azure/azure-powershell/issues/8347 수정</span><span class="sxs-lookup"><span data-stu-id="7ea64-965">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="7ea64-966">-Name을 사용하면 모든 노드를 반환하는 Get-AzAutomationDscNode 수정.</span><span class="sxs-lookup"><span data-stu-id="7ea64-966">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="7ea64-967">이제 일치하는 노드만 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-967">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7ea64-968">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7ea64-968">Az.Compute</span></span>
* <span data-ttu-id="7ea64-969">ProtectFromScaleIn 및 ProtectFromScaleSetAction 매개 변수를 Update-AzVmssVM cmdlet에 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-969">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="7ea64-970">'East US'(미국 동부)가 지원되지 않는 경우 이제 New-AzVM wimple 매개 변수 집합에서 기본적으로 사용 가능한 위치를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-970">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="7ea64-971">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="7ea64-971">Az.DataLakeStore</span></span>
* <span data-ttu-id="7ea64-972">ADLS SDK에서 httpclient를 사용하도록 업데이트하고, 데이터 평면 테스트를 Azure 프레임워크와 통합합니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-972">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="7ea64-973">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="7ea64-973">Az.Monitor</span></span>
* <span data-ttu-id="7ea64-974">도움말 예제에서 잘못된 매개 변수 이름을 수정했습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-974">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7ea64-975">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7ea64-975">Az.Network</span></span>
* <span data-ttu-id="7ea64-976">DisableBgpRoutePropagation 플래그를 유효 경로 테이블 출력에 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-976">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="7ea64-977">업데이트된 cmdlet:</span><span class="sxs-lookup"><span data-stu-id="7ea64-977">Updated cmdlet:</span></span>
        - <span data-ttu-id="7ea64-978">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="7ea64-978">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="7ea64-979">New-AzApplicationGatewayTrustedRootCertificate 설명서에서 이중 파선을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-979">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="7ea64-980">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7ea64-980">Az.Resources</span></span>
* <span data-ttu-id="7ea64-981">할당 거부를 검색하기 위한 새 Get-AzureRmDenyAssignment cmdlet을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-981">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="7ea64-982">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7ea64-982">Az.Sql</span></span>
* <span data-ttu-id="7ea64-983">Advanced Threat Protection cmdlet의 이름을 Advanced Data Security로 변경하고, 취약성 평가를 기본적으로 사용하도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-983">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="7ea64-984">2.0.0 - 2019년 5월</span><span class="sxs-lookup"><span data-stu-id="7ea64-984">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="7ea64-985">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="7ea64-985">Az.Accounts</span></span>
* <span data-ttu-id="7ea64-986">사용자 이름/비밀번호 인증을 사용하여 ADFS 문제를 해결하도록 인증 라이브러리 업데이트</span><span class="sxs-lookup"><span data-stu-id="7ea64-986">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="7ea64-987">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="7ea64-987">Az.CognitiveServices</span></span>
* <span data-ttu-id="7ea64-988">Bing Search 서비스에 대해서만 Bing 면책 조항을 표시하세요.</span><span class="sxs-lookup"><span data-stu-id="7ea64-988">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="7ea64-989">계정 생성 실패 시 오류 개선.</span><span class="sxs-lookup"><span data-stu-id="7ea64-989">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7ea64-990">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7ea64-990">Az.Compute</span></span>
* <span data-ttu-id="7ea64-991">근접 배치 그룹 기능</span><span class="sxs-lookup"><span data-stu-id="7ea64-991">Proximity placement group feature.</span></span>
    - <span data-ttu-id="7ea64-992">다음과 같은 새 cmdlet을 추가했습니다.   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="7ea64-992">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="7ea64-993">새 매개 변수 ProximityPlacementGroupId가 다음 cmdlet에 추가됩니다.   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="7ea64-993">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="7ea64-994">New-AzGalleryImageVersion에 StorageAccountType 매개 변수가 추가됩니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-994">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="7ea64-995">New-AzGalleryImageVersion의 TargetRegion이 StorageAccountType를 포함할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-995">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="7ea64-996">SkipShutdown 스위치 매개 변수가 Stop-AzVM 및 Stop-AzVmss에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-996">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>       
* <span data-ttu-id="7ea64-997">주요 변경 내용</span><span class="sxs-lookup"><span data-stu-id="7ea64-997">Breaking changes</span></span>
    - <span data-ttu-id="7ea64-998">Set-AzVMBootDiagnostics이 Set-AzVMBootDiagnostic으로 변경됩니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-998">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="7ea64-999">Export-AzLogAnalyticThrottledRequests이 Export-AzLogAnalyticThrottledRequests로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-999">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="7ea64-1000">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="7ea64-1000">Az.DeploymentManager</span></span>
* <span data-ttu-id="7ea64-1001">Azure 배포 관리자 cmdlet의 일반적으로 사용 가능한 첫 번째 릴리스</span><span class="sxs-lookup"><span data-stu-id="7ea64-1001">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="7ea64-1002">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="7ea64-1002">Az.Dns</span></span>
* <span data-ttu-id="7ea64-1003">자동 DNS 이름 서버 위임</span><span class="sxs-lookup"><span data-stu-id="7ea64-1003">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="7ea64-1004">DNS 영역 만들기 cmdlet은 추가 선택적 매개 변수로 부모 영역 이름을 허용합니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-1004">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="7ea64-1005">새로 생성 된 자식 영역의 부모 영역에 NS 레코드를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-1005">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="7ea64-1006">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="7ea64-1006">Az.FrontDoor</span></span>
* <span data-ttu-id="7ea64-1007">Azure FrontDoor cmdlet의 일반적으로 사용 가능한 첫 번째 릴리스</span><span class="sxs-lookup"><span data-stu-id="7ea64-1007">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="7ea64-1008">'Waf'를 포함하도록 WAF cmdlet의 이름 바꾸기</span><span class="sxs-lookup"><span data-stu-id="7ea64-1008">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="7ea64-1009">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="7ea64-1009">Az.HDInsight</span></span>
* <span data-ttu-id="7ea64-1010">두 개의 cmdlet을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-1010">Removed two cmdlets:</span></span>
    - <span data-ttu-id="7ea64-1011">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="7ea64-1011">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="7ea64-1012">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="7ea64-1012">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="7ea64-1013">Grant-AzHDInsightHttpServicesAccess를 대체할 새 cmdlet Set-AzHDInsightGatewayCredential을 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-1013">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="7ea64-1014">reader 역할과 HDInsight 운영자 역할을 구분하도록 cmdlet Get-AzHDInsightJobOutput 업데이트:</span><span class="sxs-lookup"><span data-stu-id="7ea64-1014">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="7ea64-1015">reader 역할을 가진 사용자는 'DefaultStorageAccountKey'매개 변수를 명시적으로 지정해야 합니다. 그렇지 않으면 오류가 발생합니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-1015">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="7ea64-1016">Hdinsight 운영자 역할을 가진 사용자를 영향을 받지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-1016">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="7ea64-1017">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="7ea64-1017">Az.Monitor</span></span>
* <span data-ttu-id="7ea64-1018">SQR API(예약 쿼리 규칙)용 새 cmdlet</span><span class="sxs-lookup"><span data-stu-id="7ea64-1018">New cmdlets for SQR API (Scheduled Query Rule)</span></span>  
    - <span data-ttu-id="7ea64-1019">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="7ea64-1019">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="7ea64-1020">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="7ea64-1020">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="7ea64-1021">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="7ea64-1021">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="7ea64-1022">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="7ea64-1022">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="7ea64-1023">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="7ea64-1023">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="7ea64-1024">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="7ea64-1024">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="7ea64-1025">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="7ea64-1025">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="7ea64-1026">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="7ea64-1026">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="7ea64-1027">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="7ea64-1027">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="7ea64-1028">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="7ea64-1028">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="7ea64-1029">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="7ea64-1029">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="7ea64-1030">SQR API에 대한 [자세한 내용](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules)</span><span class="sxs-lookup"><span data-stu-id="7ea64-1030">[More](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="7ea64-1031">GenV2(비 클래식) 메트릭 기반 경고 규칙에 대한 cmdlet을 포함하도록 Az.Monitor.md가 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="7ea64-1031">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7ea64-1032">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7ea64-1032">Az.Network</span></span>
* <span data-ttu-id="7ea64-1033">Nat 게이트웨이 리소스에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="7ea64-1033">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="7ea64-1034">새 cmdlet</span><span class="sxs-lookup"><span data-stu-id="7ea64-1034">New cmdlets</span></span>
        - <span data-ttu-id="7ea64-1035">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="7ea64-1035">New-AzNatGateway</span></span>
        - <span data-ttu-id="7ea64-1036">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="7ea64-1036">Get-AzNatGateway</span></span>
        - <span data-ttu-id="7ea64-1037">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="7ea64-1037">Set-AzNatGateway</span></span>
        - <span data-ttu-id="7ea64-1038">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="7ea64-1038">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="7ea64-1039">다음 Cmdlet이 업데이트 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-1039">Updated cmdlets</span></span>
        - <span data-ttu-id="7ea64-1040">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="7ea64-1040">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="7ea64-1041">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="7ea64-1041">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="7ea64-1042">기능에 대한 새로운 명령이 업데이트됨: Brooklyn Gateway에서 사용자 지정 경로 설정/제거.</span><span class="sxs-lookup"><span data-stu-id="7ea64-1042">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="7ea64-1043">New-AzVirtualNetworkGateway가 업데이트됨: 선택적 매개 변수 -CustomRoute를 추가하여 게이트웨이에서 설정할 사용자 지정 경로로 주소 접두사를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-1043">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="7ea64-1044">Set-AzVirtualNetworkGateway가 업데이트됨: 선택적 매개 변수 -CustomRoute를 추가하여 게이트웨이에서 설정할 사용자 지정 경로로 주소 접두사를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-1044">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="7ea64-1045">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="7ea64-1045">Az.PolicyInsights</span></span>
* <span data-ttu-id="7ea64-1046">정책 평가 세부 정보 쿼리 지원</span><span class="sxs-lookup"><span data-stu-id="7ea64-1046">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="7ea64-1047">Get-AzPolicyState에 '-Expand'매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="7ea64-1047">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="7ea64-1048">'-Expand PolicyEvaluationDetails' 지원</span><span class="sxs-lookup"><span data-stu-id="7ea64-1048">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="7ea64-1049">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="7ea64-1049">Az.RecoveryServices</span></span>
* <span data-ttu-id="7ea64-1050">크로스 구독 Azure에서 Azure 사이트 복구 지원</span><span class="sxs-lookup"><span data-stu-id="7ea64-1050">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="7ea64-1051">Azure Site Recovery에 대한 호환성이 손상되는 변경 표시</span><span class="sxs-lookup"><span data-stu-id="7ea64-1051">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="7ea64-1052">Azure Site Recovery 복구 계획 최종 실행 계획에 대한 수정</span><span class="sxs-lookup"><span data-stu-id="7ea64-1052">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="7ea64-1053">Azure에서 Azure에 대한 Azure Site Recovery 업데이트 네트워크 매핑 수정</span><span class="sxs-lookup"><span data-stu-id="7ea64-1053">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="7ea64-1054">관리 디스크에 대한 Azure에서 Azure에 대한 Azure Site Recovery 업데이트 보호 방향 수정</span><span class="sxs-lookup"><span data-stu-id="7ea64-1054">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="7ea64-1055">기타 사소한 수정.</span><span class="sxs-lookup"><span data-stu-id="7ea64-1055">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="7ea64-1056">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="7ea64-1056">Az.Relay</span></span>
* <span data-ttu-id="7ea64-1057">고객 관련 메시지의 철자 오류 수정</span><span class="sxs-lookup"><span data-stu-id="7ea64-1057">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="7ea64-1058">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="7ea64-1058">Az.ServiceBus</span></span>
* <span data-ttu-id="7ea64-1059">네임스페이스의 NetworkRuleSet에 대한 새 cmdlet가 추가되었습니다</span><span class="sxs-lookup"><span data-stu-id="7ea64-1059">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="7ea64-1060">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="7ea64-1060">Az.Storage</span></span>
* <span data-ttu-id="7ea64-1061">저장소 클라이언트 라이브러리 10.0.1로 업그레이드(이 SDK의 모든 개체의 네임스페이스가 'Microsoft.WindowsAzure.Storage. *'에서 'Microsoft.Azure.Storage.* '로 변경됨)</span><span class="sxs-lookup"><span data-stu-id="7ea64-1061">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="7ea64-1062">새로운 API 버전 2019-04-01을 지원하기 위해 Microsoft.Azure.Management.Storage 11.0.0으로 업그레이드합니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-1062">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="7ea64-1063">스토리지 생성 계정의 기본 스토리지 계정 종류가 'Storage'에서 'StorageV2'로 변경됩니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-1063">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="7ea64-1064">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="7ea64-1064">New-AzStorageAccount</span></span>
* <span data-ttu-id="7ea64-1065">'StandardLRS'가 'Standard_LRS'로 변경되는 것과 같이 '-'을 추가하여 입력 SkuName과 정렬되도록 스토리지 계정 cmdlet 출력 Sku.Name을 변경합니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-1065">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="7ea64-1066">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="7ea64-1066">New-AzStorageAccount</span></span>
    - <span data-ttu-id="7ea64-1067">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="7ea64-1067">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="7ea64-1068">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="7ea64-1068">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="7ea64-1069">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="7ea64-1069">Az.Websites</span></span>
* <span data-ttu-id="7ea64-1070">Get-AzWebApp에서 반환한 PSSite 개체에 대해 'Kind'속성이 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-1070">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="7ea64-1071">Get-AzWebApp\* 메트릭 및 Get-AzAppServicePlanMetrics가 사용되지 않음으로 표시되었습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-1071">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="7ea64-1072">1.8.0 - 2019년 4월</span><span class="sxs-lookup"><span data-stu-id="7ea64-1072">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="7ea64-1073">마지막 주 릴리스 이후의 주요 사항</span><span class="sxs-lookup"><span data-stu-id="7ea64-1073">Highlights since the last major release</span></span>
* <span data-ttu-id="7ea64-1074">`Az` 모듈 일반 공급</span><span class="sxs-lookup"><span data-stu-id="7ea64-1074">General availability of `Az` module</span></span>
* <span data-ttu-id="7ea64-1075">`Az` 모듈에 대한 자세한 내용은 https://aka.ms/azps-announce 를 방문하세요.</span><span class="sxs-lookup"><span data-stu-id="7ea64-1075">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="7ea64-1076">Location, ResourceGroup 및 ResourceName 완성자가 추가되었습니다(https://azure.microsoft.com/blog/completers-in-azure-powershell/ ).</span><span class="sxs-lookup"><span data-stu-id="7ea64-1076">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="7ea64-1077">와일드카드 지원이 Az.Compute 및 Az.Network에 대한 Get cmdlet에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-1077">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="7ea64-1078">Windows PowerShell 5.1 전용 대화형 사용자 이름/암호 인증이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-1078">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="7ea64-1079">Python 2 Runbook 지원이 Az.Automation에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-1079">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="7ea64-1080">Az.LogicApp: 통합 계정 어셈블리 및 일괄 처리 구성을 위한 새로운 cmdlet입니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-1080">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="7ea64-1081">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="7ea64-1081">Az.Accounts</span></span>
* <span data-ttu-id="7ea64-1082">Mac에서 모듈을 올바르게 삭제하기 위해 Uninstall-AzureRm을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-1082">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="7ea64-1083">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="7ea64-1083">Az.Batch</span></span>
* <span data-ttu-id="7ea64-1084">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-1084">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="7ea64-1085">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="7ea64-1085">Az.Cdn</span></span>
* <span data-ttu-id="7ea64-1086">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-1086">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="7ea64-1087">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="7ea64-1087">Az.CognitiveServices</span></span>
* <span data-ttu-id="7ea64-1088">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-1088">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7ea64-1089">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7ea64-1089">Az.Compute</span></span>
* <span data-ttu-id="7ea64-1090">디스크의 리소스 ID에 리소스 ID의 소문자 resourcegroups가 있는 경우 AEM 설치 문제 수정</span><span class="sxs-lookup"><span data-stu-id="7ea64-1090">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="7ea64-1091">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-1091">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="7ea64-1092">와일드 카드에 대한 설명서 수정</span><span class="sxs-lookup"><span data-stu-id="7ea64-1092">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="7ea64-1093">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="7ea64-1093">Az.DataFactory</span></span>
* <span data-ttu-id="7ea64-1094">NodeCount가 관리형 통합 런타임에 대해 Null이 아닌 경우 SsisProperties를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-1094">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="7ea64-1095">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="7ea64-1095">Az.DataLakeStore</span></span>
* <span data-ttu-id="7ea64-1096">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-1096">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="7ea64-1097">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="7ea64-1097">Az.EventGrid</span></span>
* <span data-ttu-id="7ea64-1098">이벤트 구독 cmdlet 만들기/업데이트를 사용하기 전에 리소스를 만들어야 함을 나타내기 위해 엔드포인트의 도움말 텍스트가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-1098">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="7ea64-1099">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="7ea64-1099">Az.EventHub</span></span>
* <span data-ttu-id="7ea64-1100">네임스페이스의 NetworkRuleSet에 대한 새 cmdlet가 추가되었습니다</span><span class="sxs-lookup"><span data-stu-id="7ea64-1100">Added new cmdlets for NetworkRuleSet of Namespace</span></span> 

#### <a name="azhdinsight"></a><span data-ttu-id="7ea64-1101">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="7ea64-1101">Az.HDInsight</span></span>
* <span data-ttu-id="7ea64-1102">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-1102">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="7ea64-1103">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="7ea64-1103">Az.IotHub</span></span>
* <span data-ttu-id="7ea64-1104">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-1104">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="7ea64-1105">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="7ea64-1105">Az.KeyVault</span></span>
* <span data-ttu-id="7ea64-1106">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-1106">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="7ea64-1107">와일드 카드에 대한 설명서 수정</span><span class="sxs-lookup"><span data-stu-id="7ea64-1107">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="7ea64-1108">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="7ea64-1108">Az.MachineLearning</span></span>
* <span data-ttu-id="7ea64-1109">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-1109">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="7ea64-1110">Az.Media</span><span class="sxs-lookup"><span data-stu-id="7ea64-1110">Az.Media</span></span>
* <span data-ttu-id="7ea64-1111">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-1111">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="7ea64-1112">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="7ea64-1112">Az.Monitor</span></span>
  * <span data-ttu-id="7ea64-1113">GenV2(비 클래식) 메트릭 기반 경고 규칙에 대한 새 cmdlet</span><span class="sxs-lookup"><span data-stu-id="7ea64-1113">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="7ea64-1114">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="7ea64-1114">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="7ea64-1115">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="7ea64-1115">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="7ea64-1116">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="7ea64-1116">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="7ea64-1117">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="7ea64-1117">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="7ea64-1118">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="7ea64-1118">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="7ea64-1119">모니터 SDK가 버전 0.22.0-preview로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-1119">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7ea64-1120">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7ea64-1120">Az.Network</span></span>
* <span data-ttu-id="7ea64-1121">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-1121">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="7ea64-1122">와일드 카드에 대한 설명서 수정</span><span class="sxs-lookup"><span data-stu-id="7ea64-1122">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="7ea64-1123">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="7ea64-1123">Az.NotificationHubs</span></span>
* <span data-ttu-id="7ea64-1124">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-1124">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="7ea64-1125">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="7ea64-1125">Az.OperationalInsights</span></span>
* <span data-ttu-id="7ea64-1126">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-1126">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="7ea64-1127">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="7ea64-1127">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="7ea64-1128">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-1128">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="7ea64-1129">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="7ea64-1129">Az.RecoveryServices</span></span>
* <span data-ttu-id="7ea64-1130">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-1130">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="7ea64-1131">Azure VM의 SQL용 테이블 형식이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-1131">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="7ea64-1132">AzureFileShare에서 위치를 가져오는 대체 메서드가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-1132">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="7ea64-1133">시간대에 따라 SchedulePolicy 개체의 ScheduleRunDays가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-1133">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="7ea64-1134">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="7ea64-1134">Az.RedisCache</span></span>
* <span data-ttu-id="7ea64-1135">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-1135">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="7ea64-1136">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7ea64-1136">Az.Resources</span></span>
* <span data-ttu-id="7ea64-1137">와일드 카드에 대한 설명서 수정</span><span class="sxs-lookup"><span data-stu-id="7ea64-1137">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="7ea64-1138">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7ea64-1138">Az.Sql</span></span>
* <span data-ttu-id="7ea64-1139">Monitor SDK의 종속성을 공용 코드로 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-1139">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="7ea64-1140">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-1140">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="7ea64-1141">다중 열 분류 프로세스가 향상되었습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-1141">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="7ea64-1142">기본적으로 Get-AzSqlServerServiceObjective의 응답으로 SKU 속성(SKU 이름, 제품군, 용량)과 테이블 형식을 포함합니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-1142">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="7ea64-1143">해당 지역에 기존 서버 없이 위치별로 Get-AzSqlServerServiceObjective를 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-1143">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="7ea64-1144">관리형 인스턴스 생성 시 표준 시간대 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-1144">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="7ea64-1145">와일드 카드에 대한 설명서 수정</span><span class="sxs-lookup"><span data-stu-id="7ea64-1145">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="7ea64-1146">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="7ea64-1146">Az.Websites</span></span>
* <span data-ttu-id="7ea64-1147">실행 시 태그를 제거하지 않도록 Set-AzWebApp 및 Set-AzWebAppSlot를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-1147">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="7ea64-1148">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-1148">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="7ea64-1149">WebSites SDK가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-1149">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="7ea64-1150">PSAppServicePlan에서 AdminSiteName 속성을 제거했습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-1150">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="7ea64-1151">1.7.0 - 2019년 4월</span><span class="sxs-lookup"><span data-stu-id="7ea64-1151">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="7ea64-1152">마지막 주 릴리스 이후의 주요 사항</span><span class="sxs-lookup"><span data-stu-id="7ea64-1152">Highlights since the last major release</span></span>
* <span data-ttu-id="7ea64-1153">`Az` 모듈 일반 공급</span><span class="sxs-lookup"><span data-stu-id="7ea64-1153">General availability of `Az` module</span></span>
* <span data-ttu-id="7ea64-1154">`Az` 모듈에 대한 자세한 내용은 https://aka.ms/azps-announce 를 방문하세요.</span><span class="sxs-lookup"><span data-stu-id="7ea64-1154">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="7ea64-1155">Location, ResourceGroup 및 ResourceName 완성자가 추가되었습니다(https://azure.microsoft.com/blog/completers-in-azure-powershell/ ).</span><span class="sxs-lookup"><span data-stu-id="7ea64-1155">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="7ea64-1156">와일드카드 지원이 Az.Compute 및 Az.Network에 대한 Get cmdlet에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-1156">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="7ea64-1157">Windows PowerShell 5.1 전용 대화형 사용자 이름/암호 인증이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-1157">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="7ea64-1158">Python 2 Runbook 지원이 Az.Automation에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-1158">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="7ea64-1159">Az.LogicApp: 통합 계정 어셈블리 및 일괄 처리 구성을 위한 새로운 cmdlet입니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-1159">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="7ea64-1160">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="7ea64-1160">Az.Accounts</span></span>
* <span data-ttu-id="7ea64-1161">매개 변수 AzureAnalysisServicesEndpointResourceId를 허용하도록 Add-AzEnvironment 및 Set-AzEnvironment 업데이트</span><span class="sxs-lookup"><span data-stu-id="7ea64-1161">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="7ea64-1162">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="7ea64-1162">Az.AnalysisServices</span></span>
* <span data-ttu-id="7ea64-1163">데이터 평면 cmdlet에서 ServiceClient 사용 및 원본 인증 논리 제거</span><span class="sxs-lookup"><span data-stu-id="7ea64-1163">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="7ea64-1164">호환성이 손상되는 변경을 방지하기 위해 Add-AzureASAccount를 Connect-AzAccount의 래퍼로 만듦</span><span class="sxs-lookup"><span data-stu-id="7ea64-1164">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="7ea64-1165">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="7ea64-1165">Az.Automation</span></span>
* <span data-ttu-id="7ea64-1166">포함에 대한 New-AzAutomationSoftwareUpdateConfiguration cmdlet 버그 수정</span><span class="sxs-lookup"><span data-stu-id="7ea64-1166">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="7ea64-1167">이제 매개 변수 IncludedKbNumber 및 IncludedPackageNameMask가 작동함</span><span class="sxs-lookup"><span data-stu-id="7ea64-1167">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="7ea64-1168">Azure 자동화 업데이트 관리 동적 그룹에 대한 버그 수정</span><span class="sxs-lookup"><span data-stu-id="7ea64-1168">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7ea64-1169">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7ea64-1169">Az.Compute</span></span>
* <span data-ttu-id="7ea64-1170">New-AzDiskConfig 및 New-AzSnapshotConfig에 HyperVGeneration 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="7ea64-1170">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="7ea64-1171">다른 테넌트의 갤러리 이미지를 사용하여 VM을 만들 수 있음</span><span class="sxs-lookup"><span data-stu-id="7ea64-1171">Allow VM creation with galley image from other tenants.</span></span> 

#### <a name="azcontainerinstance"></a><span data-ttu-id="7ea64-1172">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="7ea64-1172">Az.ContainerInstance</span></span>
* <span data-ttu-id="7ea64-1173">후행 빈 인수를 추가한 New-AzContainerGroup의 -Command 매개 변수의 문제 수정</span><span class="sxs-lookup"><span data-stu-id="7ea64-1173">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="7ea64-1174">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="7ea64-1174">Az.DataFactory</span></span>
* <span data-ttu-id="7ea64-1175">ADF .Net SDK 버전을 3.0.2로 업데이트</span><span class="sxs-lookup"><span data-stu-id="7ea64-1175">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="7ea64-1176">RepoConfiguration 관련 설정에 대한 추가 매개 변수로 Set-AzDataFactoryV2 cmdlet을 업데이트</span><span class="sxs-lookup"><span data-stu-id="7ea64-1176">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="7ea64-1177">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7ea64-1177">Az.Resources</span></span>
* <span data-ttu-id="7ea64-1178">'-ResourceId' 또는 '-ResourceGroupName', '-Name' 및 '-ResourceType' 매개 변수를 제공할 때 'Get-AzResource'에 대한 공급자 처리 개선</span><span class="sxs-lookup"><span data-stu-id="7ea64-1178">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="7ea64-1179">'Test-AzDeployment' 및 'Test-AzResourceGroupDeployment'에 대한 오류 처리 개선</span><span class="sxs-lookup"><span data-stu-id="7ea64-1179">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="7ea64-1180">배포 유효성 검사 외부에서 발생한 오류를 처리하고 그 대신 명령의 출력에 포함</span><span class="sxs-lookup"><span data-stu-id="7ea64-1180">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="7ea64-1181">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/6856 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="7ea64-1181">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="7ea64-1182">배포 cmdlet 세트에 스크립트 및 작업 시나리오에서 프롬프트를 건너뛰는 '-IgnoreDynamicParameters' 스위치 추가</span><span class="sxs-lookup"><span data-stu-id="7ea64-1182">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="7ea64-1183">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/6856 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="7ea64-1183">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="7ea64-1184">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7ea64-1184">Az.Sql</span></span>
* <span data-ttu-id="7ea64-1185">데이터베이스 데이터 분류 지원</span><span class="sxs-lookup"><span data-stu-id="7ea64-1185">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="7ea64-1186">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="7ea64-1186">Az.Storage</span></span>
* <span data-ttu-id="7ea64-1187">매개 변수 -UseConnectedAccount를 사용하여 스토리지 컨텍스트를 만들 때 자세한 오류 보고(단, 로그인 Azure 계정 없이)</span><span class="sxs-lookup"><span data-stu-id="7ea64-1187">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="7ea64-1188">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="7ea64-1188">New-AzStorageContext</span></span>
* <span data-ttu-id="7ea64-1189">관리 평면 API를 사용하여 지정한 스토리지 계정의 BLOB 서비스 속성 관리 지원</span><span class="sxs-lookup"><span data-stu-id="7ea64-1189">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="7ea64-1190">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="7ea64-1190">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="7ea64-1191">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="7ea64-1191">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="7ea64-1192">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="7ea64-1192">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="7ea64-1193">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="7ea64-1193">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="7ea64-1194">BLOB 및 파일 업로드/다운로드 cmdlet에 대한 -AsJob 지원</span><span class="sxs-lookup"><span data-stu-id="7ea64-1194">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="7ea64-1195">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="7ea64-1195">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="7ea64-1196">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="7ea64-1196">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="7ea64-1197">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="7ea64-1197">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="7ea64-1198">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="7ea64-1198">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="7ea64-1199">1.6.0 - 2019년 3월</span><span class="sxs-lookup"><span data-stu-id="7ea64-1199">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="7ea64-1200">마지막 주 릴리스 이후의 주요 사항</span><span class="sxs-lookup"><span data-stu-id="7ea64-1200">Highlights since the last major release</span></span>
* <span data-ttu-id="7ea64-1201">`Az` 모듈 일반 공급</span><span class="sxs-lookup"><span data-stu-id="7ea64-1201">General availability of `Az` module</span></span>
* <span data-ttu-id="7ea64-1202">`Az` 모듈에 대한 자세한 내용은 https://aka.ms/azps-announce 를 방문하세요.</span><span class="sxs-lookup"><span data-stu-id="7ea64-1202">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="7ea64-1203">Location, ResourceGroup 및 ResourceName 완성자가 추가되었습니다(https://azure.microsoft.com/blog/completers-in-azure-powershell/ ).</span><span class="sxs-lookup"><span data-stu-id="7ea64-1203">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="7ea64-1204">와일드카드 지원이 Az.Compute 및 Az.Network에 대한 Get cmdlet에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-1204">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="7ea64-1205">Windows PowerShell 5.1 전용 대화형 사용자 이름/암호 인증이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-1205">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="7ea64-1206">Python 2 Runbook 지원이 Az.Automation에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-1206">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="7ea64-1207">Az.LogicApp: 통합 계정 어셈블리 및 일괄 처리 구성을 위한 새로운 cmdlet입니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-1207">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="7ea64-1208">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="7ea64-1208">Az.Automation</span></span>
* <span data-ttu-id="7ea64-1209">Azure 자동화 업데이트 관리에서 변경된 지원 기능은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-1209">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="7ea64-1210">동적 그룹화</span><span class="sxs-lookup"><span data-stu-id="7ea64-1210">Dynamic grouping</span></span>
    * <span data-ttu-id="7ea64-1211">사전 스크립트</span><span class="sxs-lookup"><span data-stu-id="7ea64-1211">Pre-Post script</span></span>
    * <span data-ttu-id="7ea64-1212">다시 부팅 설정</span><span class="sxs-lookup"><span data-stu-id="7ea64-1212">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7ea64-1213">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7ea64-1213">Az.Compute</span></span>
* <span data-ttu-id="7ea64-1214">Get-AzVmBootDiagnosticsData의 경로 확인 문제가 해결되었습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-1214">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="7ea64-1215">Compute 클라이언트 라이브러리가 25.0.0으로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-1215">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="7ea64-1216">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="7ea64-1216">Az.KeyVault</span></span>
* <span data-ttu-id="7ea64-1217">와일드카드 지원이 KeyVault cmdlet에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-1217">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7ea64-1218">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7ea64-1218">Az.Network</span></span>
* <span data-ttu-id="7ea64-1219">Azure Firewall에 대한 위협 인텔리전스 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-1219">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="7ea64-1220">Application Gateway 방화벽 정책의 최상위 수준 리소스 및 사용자 지정 규칙이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-1220">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="7ea64-1221">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="7ea64-1221">Az.RecoveryServices</span></span>
* <span data-ttu-id="7ea64-1222">인스턴트 RP를 지원하기 위해 SnapshotRetentionInDays가 Azure VM 정책에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-1222">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="7ea64-1223">컨테이너 등록을 취소하는 파이프 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-1223">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="7ea64-1224">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7ea64-1224">Az.Resources</span></span>
* <span data-ttu-id="7ea64-1225">Get-AzResource 및 Get-AzResourceGroup에 대한 와일드카드 지원을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-1225">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="7ea64-1226">ARM에 대한 일반 호출을 수행할 때 사용되는 자격 증명을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-1226">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="7ea64-1227">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7ea64-1227">Az.Sql</span></span>
* <span data-ttu-id="7ea64-1228">위협 탐지의 cmdlet 매개 변수(ExcludeDetectionType)가 DetectionType에서 string[]으로 변경되어 새 DetectionType이 추가되면 이후의 증명이 되고 자동 완성도 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-1228">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="7ea64-1229">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="7ea64-1229">Az.Storage</span></span>
* <span data-ttu-id="7ea64-1230">스토리지 계정에 대한 관리 정책 가져오기/설정/제거를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-1230">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="7ea64-1231">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="7ea64-1231">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="7ea64-1232">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="7ea64-1232">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="7ea64-1233">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="7ea64-1233">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="7ea64-1234">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="7ea64-1234">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="7ea64-1235">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="7ea64-1235">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="7ea64-1236">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="7ea64-1236">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="7ea64-1237">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="7ea64-1237">Az.Websites</span></span>
* <span data-ttu-id="7ea64-1238">'New-AzWebApp -IncludeSourceWebAppSlots'를 사용하여 모든 슬롯의 복제를 중단하는 ARM 템플릿 버그가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-1238">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span> 

## <a name="150---march-2019"></a><span data-ttu-id="7ea64-1239">1.5.0 - 2019년 3월</span><span class="sxs-lookup"><span data-stu-id="7ea64-1239">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="7ea64-1240">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="7ea64-1240">Az.Accounts</span></span>
* <span data-ttu-id="7ea64-1241">'Register-AzModule' 명령을 추가하여 AutoRest 생성 cmdlet을 지원</span><span class="sxs-lookup"><span data-stu-id="7ea64-1241">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="7ea64-1242">Connect-AzAccount 예제 업데이트</span><span class="sxs-lookup"><span data-stu-id="7ea64-1242">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="7ea64-1243">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="7ea64-1243">Az.Automation</span></span>
* <span data-ttu-id="7ea64-1244">몇몇 Azure Automation cmdlet에서 특정 월별 일정을 검색할 때 발생하는 문제 수정</span><span class="sxs-lookup"><span data-stu-id="7ea64-1244">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="7ea64-1245">상위 20개 노드를 반환하도록 Get-AzAutomationDscNode를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-1245">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="7ea64-1246">이제 모든 노드 반환</span><span class="sxs-lookup"><span data-stu-id="7ea64-1246">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="7ea64-1247">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="7ea64-1247">Az.Cdn</span></span>
* <span data-ttu-id="7ea64-1248">사용자 지정 도메인 Https 사용/사용 안 함에 대한 새 Powershell cmdlet이 추가되었으며 기존의 것은 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-1248">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7ea64-1249">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7ea64-1249">Az.Compute</span></span>
* <span data-ttu-id="7ea64-1250">Get cmdlet에 와일드 카드 지원 추가</span><span class="sxs-lookup"><span data-stu-id="7ea64-1250">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="7ea64-1251">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="7ea64-1251">Az.DataFactory</span></span>
* <span data-ttu-id="7ea64-1252">ADF.Net SDK 버전이 3.0.1로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-1252">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="7ea64-1253">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="7ea64-1253">Az.LogicApp</span></span>
* <span data-ttu-id="7ea64-1254">첫 결과 페이지 검색 시에만 ListWorkflows 수정</span><span class="sxs-lookup"><span data-stu-id="7ea64-1254">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7ea64-1255">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7ea64-1255">Az.Network</span></span>
* <span data-ttu-id="7ea64-1256">Network cmdlet에 와일드 카드 지원 추가</span><span class="sxs-lookup"><span data-stu-id="7ea64-1256">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="7ea64-1257">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="7ea64-1257">Az.RecoveryServices</span></span>
* <span data-ttu-id="7ea64-1258">Azure VM 지원에 SQL 서버가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-1258">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="7ea64-1259">SDK 업데이트</span><span class="sxs-lookup"><span data-stu-id="7ea64-1259">SDK Update</span></span>
* <span data-ttu-id="7ea64-1260">VMappContainer 체크 인 Get-ProtectableItem 제거</span><span class="sxs-lookup"><span data-stu-id="7ea64-1260">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="7ea64-1261">Get ProtectableItem의 매개 변수로 Name과 ServerName이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-1261">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="7ea64-1262">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7ea64-1262">Az.Resources</span></span>
* <span data-ttu-id="7ea64-1263">`-TemplateObject` 매개 변수를 추가하여 cmdlet을 배포</span><span class="sxs-lookup"><span data-stu-id="7ea64-1263">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="7ea64-1264">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/2933 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="7ea64-1264">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="7ea64-1265">`Get-AzResource`의 결과를 `Set-AzResource`(으)로 파이프할 때 발생하는 문제 수정</span><span class="sxs-lookup"><span data-stu-id="7ea64-1265">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="7ea64-1266">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/8240 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="7ea64-1266">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="7ea64-1267">실행 시 JSON 데이터 형식 문제 해결 `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="7ea64-1267">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="7ea64-1268">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/7930 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="7ea64-1268">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="7ea64-1269">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7ea64-1269">Az.Sql</span></span>
* <span data-ttu-id="7ea64-1270">AuditingEndpointsCommunicator를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-1270">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="7ea64-1271">새 진단 설정을 생성할 때 에지 사례의 동작을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-1271">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="7ea64-1272">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="7ea64-1272">Az.Storage</span></span>
* <span data-ttu-id="7ea64-1273">스토리지 계정      - New-AzStorageAccount를 생성할 때 종류 BlockBlobStorage를 지원</span><span class="sxs-lookup"><span data-stu-id="7ea64-1273">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="7ea64-1274">1.4.0 - 2019년 2월</span><span class="sxs-lookup"><span data-stu-id="7ea64-1274">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="7ea64-1275">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="7ea64-1275">Az.AnalysisServices</span></span>
* <span data-ttu-id="7ea64-1276">사용되지 않는 AddAzureASAccount cmdlet</span><span class="sxs-lookup"><span data-stu-id="7ea64-1276">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="7ea64-1277">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="7ea64-1277">Az.Automation</span></span>
* <span data-ttu-id="7ea64-1278">Import-AzAutomationDscNodeConfiguration 도움말 업데이트</span><span class="sxs-lookup"><span data-stu-id="7ea64-1278">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="7ea64-1279">Import-AzAutomationDscConfiguration cmdlet 구성 이름 유효성 검사 추가</span><span class="sxs-lookup"><span data-stu-id="7ea64-1279">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="7ea64-1280">Import-AzAutomationDscConfiguration cmdlet 오류 처리 개선</span><span class="sxs-lookup"><span data-stu-id="7ea64-1280">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="7ea64-1281">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="7ea64-1281">Az.CognitiveServices</span></span>
* <span data-ttu-id="7ea64-1282">리소스의 하위 도메인을 지정하는 데 사용되는 New-AzCognitiveServicesAccount에 대한 새 선택적 매개 변수로 CustomSubdomainName이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-1282">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7ea64-1283">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7ea64-1283">Az.Compute</span></span>
* <span data-ttu-id="7ea64-1284">ID 매개 변수 집합 문제 해결</span><span class="sxs-lookup"><span data-stu-id="7ea64-1284">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="7ea64-1285">Name 매개 변수를 제공하지 않으면 Get-AzVMExtension이 설치된 모든 확장을 열거하도록 업데이트</span><span class="sxs-lookup"><span data-stu-id="7ea64-1285">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="7ea64-1286">Update-AzImage cmdlet에 태그 및 ResourceId 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="7ea64-1286">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="7ea64-1287">인스턴스 ID가 없는 Get-AzVmssVM과 InstanceView를 사용하면 인스턴스 보기가 있는 VMSS VM을 나열할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-1287">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="7ea64-1288">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="7ea64-1288">Az.DataLakeStore</span></span>
* <span data-ttu-id="7ea64-1289">ADL 삭제된 항목 열거 및 복원에 대한 cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="7ea64-1289">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="7ea64-1290">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="7ea64-1290">Az.EventHub</span></span>
* <span data-ttu-id="7ea64-1291">Eventhub의 CaptureDescription 클래스에서 빈 보관을 건너뛰는 새 부울 속성 SkipEmptyArchives가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-1291">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span> 

#### <a name="azkeyvault"></a><span data-ttu-id="7ea64-1292">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="7ea64-1292">Az.KeyVault</span></span>
* <span data-ttu-id="7ea64-1293">Set-AzKeyVaultSecret 태그 지정 수정</span><span class="sxs-lookup"><span data-stu-id="7ea64-1293">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="7ea64-1294">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="7ea64-1294">Az.LogicApp</span></span>
* <span data-ttu-id="7ea64-1295">통합 계정에 대한 기본 sku 추가</span><span class="sxs-lookup"><span data-stu-id="7ea64-1295">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="7ea64-1296">XSLT 2.0, XSLT 3.0, Liquid 맵 형식 추가</span><span class="sxs-lookup"><span data-stu-id="7ea64-1296">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="7ea64-1297">통합 계정 어셈블리에 대한 새 cmdlet</span><span class="sxs-lookup"><span data-stu-id="7ea64-1297">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="7ea64-1298">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="7ea64-1298">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="7ea64-1299">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="7ea64-1299">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="7ea64-1300">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="7ea64-1300">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="7ea64-1301">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="7ea64-1301">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="7ea64-1302">통합 계정 일괄 처리 구성에 대한 새 cmdlet</span><span class="sxs-lookup"><span data-stu-id="7ea64-1302">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="7ea64-1303">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="7ea64-1303">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="7ea64-1304">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="7ea64-1304">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="7ea64-1305">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="7ea64-1305">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="7ea64-1306">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="7ea64-1306">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="7ea64-1307">논리 앱 SDK를 버전 4.1.0으로 업데이트</span><span class="sxs-lookup"><span data-stu-id="7ea64-1307">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="7ea64-1308">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="7ea64-1308">Az.Monitor</span></span>
* <span data-ttu-id="7ea64-1309">Get-AzMetric에 대한 도움말 업데이트</span><span class="sxs-lookup"><span data-stu-id="7ea64-1309">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7ea64-1310">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7ea64-1310">Az.Network</span></span>
* <span data-ttu-id="7ea64-1311">Add-AzApplicationGatewayCustomError에 대한 도움말 예제 업데이트</span><span class="sxs-lookup"><span data-stu-id="7ea64-1311">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="7ea64-1312">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="7ea64-1312">Az.OperationalInsights</span></span>
* <span data-ttu-id="7ea64-1313">New 및 Get ApplicationInsights 데이터 소스에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="7ea64-1313">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="7ea64-1314">지정된 작업 영역에 대한 특정 또는 전체 ApplicationInsights 데이터 원본 가져오기를 지원하기 위한 새로운 'ApplicationInsights' 종류가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-1314">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span> 
    - <span data-ttu-id="7ea64-1315">지정된 Application-Insights 리소스 매개 변수(구독 ID, resourceGroupName 및 이름)별로 데이터 원본을 만들기 위한 New-AzOperationalInsightsApplicationInsightsDataSource cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-1315">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span> 

#### <a name="azresources"></a><span data-ttu-id="7ea64-1316">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7ea64-1316">Az.Resources</span></span>
* <span data-ttu-id="7ea64-1317">문제 https://github.com/Azure/azure-powershell/issues/8166 수정</span><span class="sxs-lookup"><span data-stu-id="7ea64-1317">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="7ea64-1318">문제 https://github.com/Azure/azure-powershell/issues/8235 수정</span><span class="sxs-lookup"><span data-stu-id="7ea64-1318">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="7ea64-1319">문제 https://github.com/Azure/azure-powershell/issues/6219 수정</span><span class="sxs-lookup"><span data-stu-id="7ea64-1319">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="7ea64-1320">KeyCredentials 반복 만들기를 방지하기 위해 버그 수정</span><span class="sxs-lookup"><span data-stu-id="7ea64-1320">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="7ea64-1321">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7ea64-1321">Az.Sql</span></span>
* <span data-ttu-id="7ea64-1322">SQL DB 하이퍼스케일에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="7ea64-1322">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="7ea64-1323">복원 요청에서 불필요한 속성을 설정하여 복원이 실패할 수 있는 버그 수정</span><span class="sxs-lookup"><span data-stu-id="7ea64-1323">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="7ea64-1324">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="7ea64-1324">Az.Websites</span></span>
* <span data-ttu-id="7ea64-1325">Get-AzWebAppSlotMetrics 내 올바른 예제</span><span class="sxs-lookup"><span data-stu-id="7ea64-1325">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="7ea64-1326">1.3.0 - 2019년 2월</span><span class="sxs-lookup"><span data-stu-id="7ea64-1326">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="7ea64-1327">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="7ea64-1327">Az.Accounts</span></span>
* <span data-ttu-id="7ea64-1328">ClientRuntime 최신 버전 업데이트</span><span class="sxs-lookup"><span data-stu-id="7ea64-1328">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="7ea64-1329">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="7ea64-1329">Az.AnalysisServices</span></span>
<span data-ttu-id="7ea64-1330">Az.AnalysisServices 모듈의 전반적인 가용성.</span><span class="sxs-lookup"><span data-stu-id="7ea64-1330">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7ea64-1331">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7ea64-1331">Az.Compute</span></span>
* <span data-ttu-id="7ea64-1332">AEM 확장: UltraSSD 및 P60, P70, P80 디스크에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="7ea64-1332">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="7ea64-1333">Set-AzVMBootDiagnostics에 대한 도움말 업데이트</span><span class="sxs-lookup"><span data-stu-id="7ea64-1333">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="7ea64-1334">Update-AzImage에 대한 도움말 및 예제 업데이트</span><span class="sxs-lookup"><span data-stu-id="7ea64-1334">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="7ea64-1335">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="7ea64-1335">Az.RecoveryServices</span></span>
<span data-ttu-id="7ea64-1336">Az.RecoveryServices 모듈의 전반적인 가용성.</span><span class="sxs-lookup"><span data-stu-id="7ea64-1336">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="7ea64-1337">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7ea64-1337">Az.Resources</span></span>
* <span data-ttu-id="7ea64-1338">리소스 그룹 관련 태그 수정</span><span class="sxs-lookup"><span data-stu-id="7ea64-1338">Fix tagging for resource groups</span></span> 
    - <span data-ttu-id="7ea64-1339">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/8166 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="7ea64-1339">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="7ea64-1340">`Get-AzureRmRoleAssignment`이(가) -ErrorAction을 준수하지 않는 문제 수정</span><span class="sxs-lookup"><span data-stu-id="7ea64-1340">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span> 
    - <span data-ttu-id="7ea64-1341">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/8235 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="7ea64-1341">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="7ea64-1342">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7ea64-1342">Az.Sql</span></span>
* <span data-ttu-id="7ea64-1343">AzSqlDatabaseBackupShortTermRetentionPolicy 가져오기/설정하기 추가</span><span class="sxs-lookup"><span data-stu-id="7ea64-1343">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="7ea64-1344">SQL cmdlet을 실행할 경우 Azure 계정에 로그인되어 있지 않은 것이 nullref 예외를 초래하는 문제 수정</span><span class="sxs-lookup"><span data-stu-id="7ea64-1344">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="7ea64-1345">Get-AzSqlCapability의 nullref 예외 수정</span><span class="sxs-lookup"><span data-stu-id="7ea64-1345">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="7ea64-1346">1.2.1 - 2019년 1월</span><span class="sxs-lookup"><span data-stu-id="7ea64-1346">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="7ea64-1347">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="7ea64-1347">Az.Accounts</span></span>
* <span data-ttu-id="7ea64-1348">올바른 인증 버전을 사용하여 릴리스</span><span class="sxs-lookup"><span data-stu-id="7ea64-1348">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="7ea64-1349">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="7ea64-1349">Az.AnalysisServices</span></span>
* <span data-ttu-id="7ea64-1350">업데이트된 인증 종속성을 사용하여 릴리스</span><span class="sxs-lookup"><span data-stu-id="7ea64-1350">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="7ea64-1351">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="7ea64-1351">Az.RecoveryServices</span></span>
* <span data-ttu-id="7ea64-1352">업데이트된 인증 종속성을 사용하여 릴리스</span><span class="sxs-lookup"><span data-stu-id="7ea64-1352">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="7ea64-1353">1.2.0 - 2019년 1월</span><span class="sxs-lookup"><span data-stu-id="7ea64-1353">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="7ea64-1354">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="7ea64-1354">Az.Accounts</span></span>
* <span data-ttu-id="7ea64-1355">Windows PowerShell 5.1 전용 대화형 사용자 이름/암호 인증 추가</span><span class="sxs-lookup"><span data-stu-id="7ea64-1355">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="7ea64-1356">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="7ea64-1356">Update incorrect online help URLs</span></span>
* <span data-ttu-id="7ea64-1357">Uninstall-AzureRm 관련 PS Core에 경고 메시지 추가</span><span class="sxs-lookup"><span data-stu-id="7ea64-1357">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="7ea64-1358">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="7ea64-1358">Az.Aks</span></span>
* <span data-ttu-id="7ea64-1359">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="7ea64-1359">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="7ea64-1360">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="7ea64-1360">Az.Automation</span></span>
* <span data-ttu-id="7ea64-1361">Python 2 Runbook에 대한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-1361">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="7ea64-1362">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="7ea64-1362">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="7ea64-1363">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="7ea64-1363">Az.Cdn</span></span>
* <span data-ttu-id="7ea64-1364">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="7ea64-1364">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7ea64-1365">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7ea64-1365">Az.Compute</span></span>
* <span data-ttu-id="7ea64-1366">Invoke-AzVMReimage cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="7ea64-1366">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="7ea64-1367">Set-AzVmss에 TempDisk 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="7ea64-1367">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="7ea64-1368">New-AzVM 경고 메시지 수정</span><span class="sxs-lookup"><span data-stu-id="7ea64-1368">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="7ea64-1369">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="7ea64-1369">Az.ContainerRegistry</span></span>
* <span data-ttu-id="7ea64-1370">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="7ea64-1370">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="7ea64-1371">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="7ea64-1371">Az.DataFactory</span></span>
* <span data-ttu-id="7ea64-1372">ADF.Net SDK 버전이 3.0.0으로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-1372">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="7ea64-1373">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="7ea64-1373">Az.DataLakeStore</span></span>
* <span data-ttu-id="7ea64-1374">MSI를 사용할 때 ADLS 엔드포인트 문제 수정</span><span class="sxs-lookup"><span data-stu-id="7ea64-1374">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="7ea64-1375">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/7462 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="7ea64-1375">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="7ea64-1376">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="7ea64-1376">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="7ea64-1377">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="7ea64-1377">Az.IotHub</span></span>
* <span data-ttu-id="7ea64-1378">Add-IotHubRoutingEndpoint cmdlet에 인코딩 형식을 추가하세요.</span><span class="sxs-lookup"><span data-stu-id="7ea64-1378">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="7ea64-1379">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="7ea64-1379">Az.KeyVault</span></span>
* <span data-ttu-id="7ea64-1380">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="7ea64-1380">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7ea64-1381">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7ea64-1381">Az.Network</span></span>
* <span data-ttu-id="7ea64-1382">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="7ea64-1382">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="7ea64-1383">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7ea64-1383">Az.Resources</span></span>
* <span data-ttu-id="7ea64-1384">'New-AzADAppCredential' 및 'New-AzADSpCredential' 참조 설명서의 잘못된 예제 수정</span><span class="sxs-lookup"><span data-stu-id="7ea64-1384">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="7ea64-1385">리소스 그룹 배포 cmdlet 실행 전 '-TemplateFile' 매개 변수 경로가 확인되지 않는 문제 수정</span><span class="sxs-lookup"><span data-stu-id="7ea64-1385">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="7ea64-1386">Az.Resources: New-AzureRmPolicyDefinition -Mode 기본값에 대한 올바른 설명서</span><span class="sxs-lookup"><span data-stu-id="7ea64-1386">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="7ea64-1387">Az.Resources: 문제 https://github.com/Azure/azure-powershell/issues/7522 수정</span><span class="sxs-lookup"><span data-stu-id="7ea64-1387">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="7ea64-1388">Az.Resources: 문제 https://github.com/Azure/azure-powershell/issues/5747 수정</span><span class="sxs-lookup"><span data-stu-id="7ea64-1388">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="7ea64-1389">'PSResourceGroupDeployment' 개체의 서식 문제 수정</span><span class="sxs-lookup"><span data-stu-id="7ea64-1389">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="7ea64-1390">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/2123 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="7ea64-1390">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="7ea64-1391">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="7ea64-1391">Az.ServiceFabric</span></span>
* <span data-ttu-id="7ea64-1392">인증서가 VMSS 모델에 추가되었는데도 예외가 발생할 경우 롤백합니다. 이는 버그 https://github.com/Azure/service-fabric-issues/issues/932 를 수정하기 위함입니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-1392">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="7ea64-1393">일부 오류 메시지를 수정하세요.</span><span class="sxs-lookup"><span data-stu-id="7ea64-1393">Fix some error messages.</span></span>
* <span data-ttu-id="7ea64-1394">Az로의 마이그레이션을 통해서는 작동하지 않는 New-AzServiceFabriCluster를 위해 기본값 ARM 템플릿을 가진 클러스터 만들기를 수정하세요.</span><span class="sxs-lookup"><span data-stu-id="7ea64-1394">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="7ea64-1395">확장에서 클러스터 id를 확인하여 클러스터에 해당하는 VMSS에만 추가되도록 클러스터/애플리케이션 인증서 추가를 수정하세요.</span><span class="sxs-lookup"><span data-stu-id="7ea64-1395">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="7ea64-1396">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="7ea64-1396">Az.SignalR</span></span>
* <span data-ttu-id="7ea64-1397">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="7ea64-1397">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="7ea64-1398">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7ea64-1398">Az.Sql</span></span>
* <span data-ttu-id="7ea64-1399">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="7ea64-1399">Update incorrect online help URLs</span></span>
* <span data-ttu-id="7ea64-1400">가능한 값을 가진 LicenseType 매개 변수에 대한 매개 변수 설명이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-1400">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="7ea64-1401">유일하게 업데이트된 속성인데 작동하지 않는 관리되는 인스턴스 ID의 업데이트 수정</span><span class="sxs-lookup"><span data-stu-id="7ea64-1401">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="7ea64-1402">관리되는 인스턴스에서의 사용자 지정 데이터 정렬에 대한 지원</span><span class="sxs-lookup"><span data-stu-id="7ea64-1402">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="7ea64-1403">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="7ea64-1403">Az.Storage</span></span>
* <span data-ttu-id="7ea64-1404">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="7ea64-1404">Update incorrect online help URLs</span></span>
* <span data-ttu-id="7ea64-1405">Premium Storage 계정이 클래식 로깅/메트릭을 지원하지 않기 때문에, Premium Storage 계정의 클래식 로깅/메트릭을 가져올/설정할 때 상세한 오류 메시지를 제공해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-1405">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="7ea64-1406">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="7ea64-1406">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="7ea64-1407">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="7ea64-1407">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="7ea64-1408">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="7ea64-1408">Az.TrafficManager</span></span>
* <span data-ttu-id="7ea64-1409">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="7ea64-1409">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="7ea64-1410">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="7ea64-1410">Az.Websites</span></span>
* <span data-ttu-id="7ea64-1411">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="7ea64-1411">Update incorrect online help URLs</span></span>
* <span data-ttu-id="7ea64-1412">앱이 ASE에 호스팅되면 'New-AzWebAppSSLBinding'을 수정하여 올바른 resourcegroup+location에 인증서를 업로드합니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-1412">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="7ea64-1413">'New-AzWebAppSSLBinding'을 수정하여 SSL 인증서를 앱에 바인딩하는 데 붙는 태그를 덮어쓰지 않도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-1413">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="7ea64-1414">1.1.0 - 2019년 1월</span><span class="sxs-lookup"><span data-stu-id="7ea64-1414">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="7ea64-1415">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="7ea64-1415">Az.Accounts</span></span>
* <span data-ttu-id="7ea64-1416">Enable-AzureRmAlias에 'Local' 범위 추가</span><span class="sxs-lookup"><span data-stu-id="7ea64-1416">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7ea64-1417">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7ea64-1417">Az.Compute</span></span>
* <span data-ttu-id="7ea64-1418">이름이 Restart/Start/Stop/Remove/Set-AzVM과 Save-AzVMImage에 설정된 ID 매개 변수에서 선택 사항이 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-1418">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="7ea64-1419">도움말 파일의 ID에 대한 설명이 업데이트 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-1419">Updated the description of ID in help files</span></span>
* <span data-ttu-id="7ea64-1420">Az.Accounts 모듈을 사용할 때의 이전 버전과의 호환성 문제를 해결합니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-1420">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="7ea64-1421">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="7ea64-1421">Az.DataLakeStore</span></span>
* <span data-ttu-id="7ea64-1422">SDK 수정을 위해 데이터 평면의 SDK 버전을 1.1.14로 업데이트하세요.</span><span class="sxs-lookup"><span data-stu-id="7ea64-1422">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="7ea64-1423">getfilestatus 및 liststatus에 대한 음수 acesstime 및 modificationtime 수정, 비동기 취소 토큰 수정</span><span class="sxs-lookup"><span data-stu-id="7ea64-1423">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="7ea64-1424">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="7ea64-1424">Az.EventGrid</span></span>
* <span data-ttu-id="7ea64-1425">2019-01-01 API 버전을 사용하도록 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-1425">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="7ea64-1426">2019-01-01 API 버전에서 새 시나리오를 지원하도록 다음 cmdlet을 업데이트</span><span class="sxs-lookup"><span data-stu-id="7ea64-1426">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="7ea64-1427">New-AzureRmEventGridSubscription: 지정을 위한 새로운 선택적 매개 변수를 추가</span><span class="sxs-lookup"><span data-stu-id="7ea64-1427">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="7ea64-1428">이벤트 Time-to-Live</span><span class="sxs-lookup"><span data-stu-id="7ea64-1428">Event Time-To-Live,</span></span>
        - <span data-ttu-id="7ea64-1429">이벤트에 대한 최대 배달 시도</span><span class="sxs-lookup"><span data-stu-id="7ea64-1429">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="7ea64-1430">배달 못한 편지의 엔드포인트입니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-1430">Dead letter endpoint.</span></span>
    - <span data-ttu-id="7ea64-1431">Update-AzureRmEventGridSubscription: 지정을 위한 새로운 선택적 매개 변수를 추가</span><span class="sxs-lookup"><span data-stu-id="7ea64-1431">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="7ea64-1432">이벤트 Time-to-Live</span><span class="sxs-lookup"><span data-stu-id="7ea64-1432">Event Time-To-Live,</span></span>
        - <span data-ttu-id="7ea64-1433">이벤트에 대한 최대 배달 시도</span><span class="sxs-lookup"><span data-stu-id="7ea64-1433">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="7ea64-1434">배달 못한 편지의 엔드포인트입니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-1434">Dead letter endpoint.</span></span>
* <span data-ttu-id="7ea64-1435">New-AzureRmEventGridSubscription 및 Update-AzureRmEventGridSubscription cmdlet의 EndpointType 옵션에 새 열거형 값(즉, storageQueue 및 hybridConnection)을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-1435">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="7ea64-1436">이벤트 구독을 생성 또는 업데이트할 때 사용자가 직접 조치를 취해야 할 경우 경고 메시지를 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-1436">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="7ea64-1437">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="7ea64-1437">Az.IotHub</span></span>
* <span data-ttu-id="7ea64-1438">최신 버전의 Azure IotHub SDK로 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="7ea64-1438">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="7ea64-1439">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="7ea64-1439">Az.LogicApp</span></span>
* <span data-ttu-id="7ea64-1440">지정된 이름이 없는 모든 Get-AzLogicApp 목록</span><span class="sxs-lookup"><span data-stu-id="7ea64-1440">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="7ea64-1441">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7ea64-1441">Az.Resources</span></span>
* <span data-ttu-id="7ea64-1442">'Get-AzResource'에 '-ODataQuery'및 '-ResourceId' 매개 변수를 제공할 때 매개 변수 집합 문제 수정</span><span class="sxs-lookup"><span data-stu-id="7ea64-1442">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="7ea64-1443">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/7875 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="7ea64-1443">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="7ea64-1444">New/Set-AzPolicyDefinition에서 -Custom 매개 변수 처리 문제 수정</span><span class="sxs-lookup"><span data-stu-id="7ea64-1444">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="7ea64-1445">New-AzDeployment 설명서에서 오타 수정</span><span class="sxs-lookup"><span data-stu-id="7ea64-1445">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="7ea64-1446">'New-AzADUser'에 '-MailNickname'매개 변수가 필수 항목으로 지정됨</span><span class="sxs-lookup"><span data-stu-id="7ea64-1446">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="7ea64-1447">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/8220 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="7ea64-1447">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="7ea64-1448">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="7ea64-1448">Az.SignalR</span></span>
* <span data-ttu-id="7ea64-1449">Az.Accounts 모듈을 사용할 때의 이전 버전과의 호환성 문제를 해결합니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-1449">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="7ea64-1450">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7ea64-1450">Az.Sql</span></span>
* <span data-ttu-id="7ea64-1451">Storage 관리 클라이언트 종속성을 일반적인 SDK 구현으로 변환했습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-1451">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="7ea64-1452">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="7ea64-1452">Az.Storage</span></span>
* <span data-ttu-id="7ea64-1453">Sas Token, OAuth 또는 Anonymous를 사용하여 스토리지 컨텍스트의 StorageAccountName을 실제 스토리지 계정 이름으로 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-1453">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="7ea64-1454">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="7ea64-1454">New-AzStorageContext</span></span>
* <span data-ttu-id="7ea64-1455">'-FullUri' 매개 변수를 사용하여 Blob 스냅샷 개체의 Sas Token을 생성하고 반환된 Uri를 스냅샷 Uri로 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-1455">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="7ea64-1456">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="7ea64-1456">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="7ea64-1457">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="7ea64-1457">Az.Websites</span></span>
* <span data-ttu-id="7ea64-1458">'Get-AzDeletedWebApp'의 날짜 구문 분석 버그를 수정했습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-1458">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="7ea64-1459">Az.Accounts 모듈을 사용할 때의 이전 버전과의 호환성 문제를 해결합니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-1459">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="7ea64-1460">1.0.0 - 2018년 12월</span><span class="sxs-lookup"><span data-stu-id="7ea64-1460">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="7ea64-1461">일반</span><span class="sxs-lookup"><span data-stu-id="7ea64-1461">General</span></span>

- <span data-ttu-id="7ea64-1462">Az 모듈 일반 공급</span><span class="sxs-lookup"><span data-stu-id="7ea64-1462">General Availability of Az Module</span></span>
- <span data-ttu-id="7ea64-1463">각 모듈에 대 한 온라인 도움말</span><span class="sxs-lookup"><span data-stu-id="7ea64-1463">Online help for each module</span></span>
- <span data-ttu-id="7ea64-1464">자세한 내용과 로드맵은 [Az 알림 페이지](https://aka.ms/azps-announce)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="7ea64-1464">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="7ea64-1465">AzureRM에서 마이그레이션하는 것에 대한 정보는 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="7ea64-1465">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="7ea64-1466">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="7ea64-1466">Az.Accounts</span></span>
- <span data-ttu-id="7ea64-1467">Az.Profile에서 변경</span><span class="sxs-lookup"><span data-stu-id="7ea64-1467">Changed from Az.Profile</span></span>
- <span data-ttu-id="7ea64-1468">프로필 및 컨텍스트 형식에 대한 표 형식 수정</span><span class="sxs-lookup"><span data-stu-id="7ea64-1468">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="7ea64-1469">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="7ea64-1469">Az.ApiManagement</span></span>
- <span data-ttu-id="7ea64-1470">#7002에 대한 수정</span><span class="sxs-lookup"><span data-stu-id="7ea64-1470">Fixes for #7002</span></span>
- <span data-ttu-id="7ea64-1471">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="7ea64-1471">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="7ea64-1472">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="7ea64-1472">Az.Batch</span></span>
- <span data-ttu-id="7ea64-1473">`PSComputeNode`의 새로운 `NodeAgentInformation` 속성을 통해 풀의 각 VM에서 실행 중인 Azure Batch 노드 에이전트의 버전을 확인하는 기능이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-1473">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="7ea64-1474">`PSDataDisk`에 대한 `Caching` 기본 값은 이제 `None` 대신 `ReadWrite`입니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-1474">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="7ea64-1475">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="7ea64-1475">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="7ea64-1476">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="7ea64-1476">Az.Billing</span></span>
- <span data-ttu-id="7ea64-1477">청구, 소비 및 UsageAggregates cmdlet 결합 cmdlet에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="7ea64-1477">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="7ea64-1478">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="7ea64-1478">Az.CognitivServices</span></span>
- <span data-ttu-id="7ea64-1479">New-AzureRmCognitiveServicesAccount 작업에서 사용 가능한 SkuName 및 Typem에 대한 완성자 추가</span><span class="sxs-lookup"><span data-stu-id="7ea64-1479">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="7ea64-1480">Get-AzCognitiveServicesAccountSkus에서 GetSkusWithAccountParamSetName 매개 변수 집합을 제거</span><span class="sxs-lookup"><span data-stu-id="7ea64-1480">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="7ea64-1481">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="7ea64-1481">Az.ContainerInstance</span></span>
- <span data-ttu-id="7ea64-1482">ManagedIdentity 지원이 추가됨</span><span class="sxs-lookup"><span data-stu-id="7ea64-1482">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="7ea64-1483">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="7ea64-1483">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="7ea64-1484">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="7ea64-1484">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="7ea64-1485">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="7ea64-1485">Az.DataLakeStore</span></span>
- <span data-ttu-id="7ea64-1486">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="7ea64-1486">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="7ea64-1487">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="7ea64-1487">Az.Monitor</span></span>
- <span data-ttu-id="7ea64-1488">Az.Monitor 이름 변경 및 기타 사소한 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="7ea64-1488">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="7ea64-1489">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="7ea64-1489">Az.KeyVault</span></span>
- <span data-ttu-id="7ea64-1490">출력 형식에서 사용되지 않는 'PurgeDisabled' 속성 제거</span><span class="sxs-lookup"><span data-stu-id="7ea64-1490">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="7ea64-1491">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="7ea64-1491">Az.MachineLearning</span></span>
- <span data-ttu-id="7ea64-1492">Az.MachineLearningCompute 모듈의 cmdlet 포함</span><span class="sxs-lookup"><span data-stu-id="7ea64-1492">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="7ea64-1493">Az.Media</span><span class="sxs-lookup"><span data-stu-id="7ea64-1493">Az.Media</span></span>
- <span data-ttu-id="7ea64-1494">New-AzMediaService에서 사용되지 않는 -Tags 별칭이 제거됨</span><span class="sxs-lookup"><span data-stu-id="7ea64-1494">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="7ea64-1495">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7ea64-1495">Az.Network</span></span>
<span data-ttu-id="7ea64-1496">Application Gateway에서 RewriteRuleSets를 구성하는 것에 대한 지원이 추가됨</span><span class="sxs-lookup"><span data-stu-id="7ea64-1496">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="7ea64-1497">추가된 새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-1497">New cmdlets added:</span></span>
        - <span data-ttu-id="7ea64-1498">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="7ea64-1498">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="7ea64-1499">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="7ea64-1499">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="7ea64-1500">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="7ea64-1500">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="7ea64-1501">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="7ea64-1501">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="7ea64-1502">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="7ea64-1502">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="7ea64-1503">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="7ea64-1503">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="7ea64-1504">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="7ea64-1504">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="7ea64-1505">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="7ea64-1505">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="7ea64-1506">선택적 매개 변수를 사용하도록 cmdlet이 업데이트됨 -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="7ea64-1506">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="7ea64-1507">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7ea64-1507">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="7ea64-1508">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="7ea64-1508">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="7ea64-1509">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="7ea64-1509">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="7ea64-1510">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="7ea64-1510">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="7ea64-1511">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="7ea64-1511">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="7ea64-1512">New-AzureRmApplicationGatewayUrlPathMapConfig로 ID를 사용하여 Application Gateway에 KeyVault 지원을 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-1512">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="7ea64-1513">선택적 매개 변수를 사용하도록 cmdlet이 업데이트됨 -KeyVaultSecretId, -KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="7ea64-1513">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="7ea64-1514">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="7ea64-1514">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="7ea64-1515">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="7ea64-1515">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="7ea64-1516">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="7ea64-1516">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="7ea64-1517">New-AzApplicationGateway cmdlet이 선택적 매개 변수를 사용하도록 업데이트됨 -UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="7ea64-1517">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="7ea64-1518">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="7ea64-1518">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="7ea64-1519">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="7ea64-1519">Az.OperationalInsights</span></span>
- <span data-ttu-id="7ea64-1520">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="7ea64-1520">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="7ea64-1521">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="7ea64-1521">Az.Profile</span></span>
- <span data-ttu-id="7ea64-1522">Az.Accounts에 모듈 이름이 변경됨</span><span class="sxs-lookup"><span data-stu-id="7ea64-1522">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="7ea64-1523">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="7ea64-1523">Az.RecoveryServices</span></span>
- <span data-ttu-id="7ea64-1524">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="7ea64-1524">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="7ea64-1525">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7ea64-1525">Az.Resources</span></span>
- <span data-ttu-id="7ea64-1526">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="7ea64-1526">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="7ea64-1527">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="7ea64-1527">Az.ServiceFabric</span></span>
- <span data-ttu-id="7ea64-1528">일반 이름과 지문으로 지정 인증서 지원</span><span class="sxs-lookup"><span data-stu-id="7ea64-1528">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="7ea64-1529">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="7ea64-1529">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="7ea64-1530">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="7ea64-1530">Az.SIgnalR</span></span>
- <span data-ttu-id="7ea64-1531">SIgnalR에 대한 PowerShell cmdlet에 대한 일반 공급</span><span class="sxs-lookup"><span data-stu-id="7ea64-1531">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="7ea64-1532">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7ea64-1532">Az.Sql</span></span>
- <span data-ttu-id="7ea64-1533">위협 탐지의 cmdlet에 새로운 Data_Exfiltration 및 Unsafe_Action 검색 유형 추가</span><span class="sxs-lookup"><span data-stu-id="7ea64-1533">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="7ea64-1534">Sql 감사 cmdlet에 대한 설명서 예제 업데이트</span><span class="sxs-lookup"><span data-stu-id="7ea64-1534">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="7ea64-1535">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="7ea64-1535">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="7ea64-1536">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="7ea64-1536">Az.Storage</span></span>
- <span data-ttu-id="7ea64-1537">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="7ea64-1537">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="7ea64-1538">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="7ea64-1538">Az.Websites</span></span>
- <span data-ttu-id="7ea64-1539">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="7ea64-1539">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="7ea64-1540">0.7.0 - 2018년 12월</span><span class="sxs-lookup"><span data-stu-id="7ea64-1540">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="7ea64-1541">일반</span><span class="sxs-lookup"><span data-stu-id="7ea64-1541">General</span></span>

* <span data-ttu-id="7ea64-1542">AzureRM에서 Az 전환 예정에 대한 사소한 변경</span><span class="sxs-lookup"><span data-stu-id="7ea64-1542">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="7ea64-1543">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7ea64-1543">Az.Compute</span></span>

* <span data-ttu-id="7ea64-1544">`New-AzVm(ss)` cmdlet에 대한 간단한 매개 변수 집합에 UltraSSD 및 갤러리 이미지에 대한 지원을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-1544">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="7ea64-1545">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="7ea64-1545">Az.DataLakeStore</span></span>

* <span data-ttu-id="7ea64-1546">ADLS 계정의 도메인의 후행 슬래시를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-1546">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="7ea64-1547">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="7ea64-1547">Az.FrontDoor</span></span>

* <span data-ttu-id="7ea64-1548">일부 끊어진 링크 수정</span><span class="sxs-lookup"><span data-stu-id="7ea64-1548">Fixed some broken links</span></span>
    - <span data-ttu-id="7ea64-1549">New-AzureRmFrontDoor 및 Set-AzureRmFrontDoor 아티클에서 New-AzureRmFrontDoorHealthProbeSettingObject cmdlet 아티클에 대한 링크가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-1549">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="7ea64-1550">New-AzureRmFrontDoorManagedRuleObject 아티클에서 New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet 아티클에 대한 링크가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-1550">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="7ea64-1551">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="7ea64-1551">Az.RecoveryServices</span></span>

* <span data-ttu-id="7ea64-1552">Azure File Share 복원 작업에 클라이언트 측 유효성 검사가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-1552">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="7ea64-1553">afs 복원의 경우 storageAccountName 및 storageAccountResourceGroupName을 선택적으로 만들었습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-1553">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="7ea64-1554">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7ea64-1554">Az.Resources</span></span>

* <span data-ttu-id="7ea64-1555">에 대 한 수정 https://github.com/Azure/azure-powershell/issues/7679</span><span class="sxs-lookup"><span data-stu-id="7ea64-1555">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="7ea64-1556">기본 관리자를 요청할 때 구독 범위가 제공되는 경우 Get-AzureRmRoleAssignment를 업데이트하여 구독 범위를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-1556">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="7ea64-1557">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7ea64-1557">Az.Sql</span></span>

* <span data-ttu-id="7ea64-1558">AzureRM에서 Az 전환 예정에 대한 사소한 변경</span><span class="sxs-lookup"><span data-stu-id="7ea64-1558">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="7ea64-1559">DotNet 코어에서 Get-AzureRmSqlDatabaseVulnerabilityAssessment를 사용하는 문제 해결</span><span class="sxs-lookup"><span data-stu-id="7ea64-1559">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="7ea64-1560">SQL 감사 cmdlet과 관련된 도움말 메시지의 설명서가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-1560">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="7ea64-1561">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="7ea64-1561">Az.Storage</span></span>

* <span data-ttu-id="7ea64-1562">New-AzureRmStorageAccount에 -EnableHierarchicalNamespace 추가</span><span class="sxs-lookup"><span data-stu-id="7ea64-1562">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="7ea64-1563">파일 복사 cmdlet이 -DestContext 입력이 없을 때 대상의 원본 컨텍스트를 다시 사용할 수 없는 문제 수정</span><span class="sxs-lookup"><span data-stu-id="7ea64-1563">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="7ea64-1564">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="7ea64-1564">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="7ea64-1565">고정적인 웹 사이트 구성 지원</span><span class="sxs-lookup"><span data-stu-id="7ea64-1565">Support Static Website configuration</span></span>
    - <span data-ttu-id="7ea64-1566">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="7ea64-1566">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="7ea64-1567">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="7ea64-1567">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="7ea64-1568">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="7ea64-1568">Az.Websites</span></span>

* <span data-ttu-id="7ea64-1569">Set-AzureRmWebApp 및 Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="7ea64-1569">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span> 
    - <span data-ttu-id="7ea64-1570">Windows 및 Linux 컨테이너 응용 프로그램에 탑재할 Azure Storage 경로를 지정하기 위해 새 매개 변수(-AzureStoragePath)가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-1570">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="7ea64-1571">새 cmdlet New-AzureRmWebAppAzureStoragePath의 출력을 매개 변수로 사용하여 Azure Storage 경로를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-1571">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="7ea64-1572">0.6.1 - 2018년 11월</span><span class="sxs-lookup"><span data-stu-id="7ea64-1572">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="7ea64-1573">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="7ea64-1573">Az.ApiManagement</span></span>
* <span data-ttu-id="7ea64-1574">형식 매핑 문제에 대한 종속성 업데이트</span><span class="sxs-lookup"><span data-stu-id="7ea64-1574">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="7ea64-1575">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="7ea64-1575">Az.Automation</span></span>
* <span data-ttu-id="7ea64-1576">Azure Automation cmdlet 기반 Swagger</span><span class="sxs-lookup"><span data-stu-id="7ea64-1576">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="7ea64-1577">업데이트 관리 cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="7ea64-1577">Added Update Management cmdlets</span></span>
* <span data-ttu-id="7ea64-1578">소스 제어 cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="7ea64-1578">Added Source Control cmdlets</span></span>
* <span data-ttu-id="7ea64-1579">Remove-AzureRmAutomationHybridWorkerGroup cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="7ea64-1579">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="7ea64-1580">DSC 노드 등록 명령 수정</span><span class="sxs-lookup"><span data-stu-id="7ea64-1580">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="7ea64-1581">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7ea64-1581">Az.Compute</span></span>
* <span data-ttu-id="7ea64-1582">SystemAssigned ID에 대한 ID 문제 수정</span><span class="sxs-lookup"><span data-stu-id="7ea64-1582">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="7ea64-1583">형식 매핑 문제에 대한 종속성 업데이트</span><span class="sxs-lookup"><span data-stu-id="7ea64-1583">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="7ea64-1584">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="7ea64-1584">Az.ContainerInstance</span></span>
* <span data-ttu-id="7ea64-1585">형식 매핑 문제에 대한 종속성 업데이트</span><span class="sxs-lookup"><span data-stu-id="7ea64-1585">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="7ea64-1586">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="7ea64-1586">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="7ea64-1587">마켓플레이스 cmdlet에 대한 예제 설명 업데이트</span><span class="sxs-lookup"><span data-stu-id="7ea64-1587">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="7ea64-1588">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7ea64-1588">Az.Network</span></span>
* <span data-ttu-id="7ea64-1589">New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="7ea64-1589">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="7ea64-1590">지원되는 AzureFirewall 네트워크 프로토콜에 ICMP 다시 추가</span><span class="sxs-lookup"><span data-stu-id="7ea64-1590">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="7ea64-1591">Test-AzureRmNetworkWatcherConnectivity cmdlet을 업데이트하여 대상 ID, 주소 및 포트 유효성 검사를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-1591">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span> 
* <span data-ttu-id="7ea64-1592">VirtualNetwork 맵의 메모리 사용 문제 해결</span><span class="sxs-lookup"><span data-stu-id="7ea64-1592">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="7ea64-1593">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="7ea64-1593">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="7ea64-1594">보호된 파일 공유에 대한 정책을 수정하는 것에 대해 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-1594">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="7ea64-1595">정책 표준 시간대를 대문자로 변환했습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-1595">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="7ea64-1596">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="7ea64-1596">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="7ea64-1597">New-AzureRmRecoveryServicesAsrProtectableItem의 예제 정정</span><span class="sxs-lookup"><span data-stu-id="7ea64-1597">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="7ea64-1598">형식 매핑 문제에 대한 종속성 업데이트</span><span class="sxs-lookup"><span data-stu-id="7ea64-1598">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="7ea64-1599">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="7ea64-1599">Az.Relay</span></span>
* <span data-ttu-id="7ea64-1600">선택적 매개 변수 -KeyValue를 New-AzureRmRelayKey cmdlet에 추가하여 사용자가 KeyValue를 제공할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-1600">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="7ea64-1601">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7ea64-1601">Az.Resources</span></span>
* <span data-ttu-id="7ea64-1602">`New-AzureRmPolicyAssignment` 및 `Set-AzureRmPolicyAssignment`의 자원 ID 관련 매개 변수에 대한 도움말 문서를 업데이트함</span><span class="sxs-lookup"><span data-stu-id="7ea64-1602">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="7ea64-1603">-Metadata를 사용하는 New-AzureRmPolicyDefinition에 대한 예제 추가</span><span class="sxs-lookup"><span data-stu-id="7ea64-1603">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="7ea64-1604">NetStandard의 태그 키에서 대소문자 보존을 허용하도록 수정: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="7ea64-1604">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="7ea64-1605">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="7ea64-1605">Az.ServiceFabric</span></span>
* <span data-ttu-id="7ea64-1606">향후 호환성이 손상되는 변경에 대한 사용 중단 메시지 추가</span><span class="sxs-lookup"><span data-stu-id="7ea64-1606">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="7ea64-1607">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7ea64-1607">Az.Sql</span></span>
* <span data-ttu-id="7ea64-1608">Azure Sql Database Managed Instance 및 Azure Sql Managed Database에 CRUD 작업을 위한 새 cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="7ea64-1608">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="7ea64-1609">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="7ea64-1609">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="7ea64-1610">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="7ea64-1610">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="7ea64-1611">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="7ea64-1611">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="7ea64-1612">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="7ea64-1612">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="7ea64-1613">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="7ea64-1613">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="7ea64-1614">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="7ea64-1614">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="7ea64-1615">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="7ea64-1615">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="7ea64-1616">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="7ea64-1616">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="7ea64-1617">서버 또는 데이터베이스에서 확장 감사 정책 관리를 활성화했습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-1617">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="7ea64-1618">새 매개 변수(PredicateExpression)가 감사 로그 필터링을 사용하도록 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-1618">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="7ea64-1619">Cmdlet이 레거시 클라이언트 대신 SQL 클라이언트를 사용하도록 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-1619">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="7ea64-1620">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="7ea64-1620">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="7ea64-1621">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="7ea64-1621">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="7ea64-1622">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="7ea64-1622">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="7ea64-1623">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="7ea64-1623">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="7ea64-1624">스토리지 계정 이름 매개 변수가 설정된 Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings를 사용할 때의 문제 해결</span><span class="sxs-lookup"><span data-stu-id="7ea64-1624">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="7ea64-1625">0.5.0 - 2018년 11월</span><span class="sxs-lookup"><span data-stu-id="7ea64-1625">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="7ea64-1626">일반</span><span class="sxs-lookup"><span data-stu-id="7ea64-1626">General</span></span>
* <span data-ttu-id="7ea64-1627">많은 핵심 cmdlet에 Resource Completers를 추가하여 대화형으로 cmdlet을 호출할 때 기존 리소스 이름을 탭으로 이동할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-1627">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="7ea64-1628">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="7ea64-1628">Az.Profile</span></span>
* <span data-ttu-id="7ea64-1629">ClientRuntime의 최신 버전을 사용하도록 일반적인 코드를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-1629">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="7ea64-1630">Connect-AzAccount cmdlet의 매개 변수 TenantId 이름을 Tenant로 바꾸고 TenantId의 별칭을 추가합니다</span><span class="sxs-lookup"><span data-stu-id="7ea64-1630">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="7ea64-1631">Connect-AzAccount의 업데이트된 TenantId 설명</span><span class="sxs-lookup"><span data-stu-id="7ea64-1631">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="7ea64-1632">테넌트 도메인을 제공할 때 실패한 로그인에 대한 오류 메시지 수정</span><span class="sxs-lookup"><span data-stu-id="7ea64-1632">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="7ea64-1633">테넌트에 구독이 없는 계정의 컨텍스트 이름 충돌 문제 수정</span><span class="sxs-lookup"><span data-stu-id="7ea64-1633">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="7ea64-1634">MSI를 사용할 때 DataLake 엔드포인트 문제 수정</span><span class="sxs-lookup"><span data-stu-id="7ea64-1634">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="7ea64-1635">연결되지 않은 경우 'Disconnect-AzAccount'가 throw하는 문제 수정</span><span class="sxs-lookup"><span data-stu-id="7ea64-1635">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="7ea64-1636">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="7ea64-1636">Az.CognitiveServices</span></span>
* <span data-ttu-id="7ea64-1637">Get-AzCognitiveServicesAccountSkus 작업을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-1637">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7ea64-1638">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7ea64-1638">Az.Compute</span></span>
* <span data-ttu-id="7ea64-1639">Add-AzVmssVMDataDisk 및 Remove-AzVmssVMDataDisk cmdlet를 추가합니다</span><span class="sxs-lookup"><span data-stu-id="7ea64-1639">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="7ea64-1640">Get-AzVMImage는 AutomaticOSUpgradeProperties를 표시합니다</span><span class="sxs-lookup"><span data-stu-id="7ea64-1640">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="7ea64-1641">수정된 SetAzVMChefExtension -BootstrapOptions 및 -JsonAttribute option 값이 json 형식으로 설정하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-1641">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="7ea64-1642">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="7ea64-1642">Az.DataLakeStore</span></span>
* <span data-ttu-id="7ea64-1643">DataLake 패키지를 1.1.10으로 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-1643">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="7ea64-1644">기본 동시성을 다중 스레드 작업에 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-1644">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="7ea64-1645">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="7ea64-1645">Az.Insights</span></span>
* <span data-ttu-id="7ea64-1646">해결된 문제 #7267(자동 크기 조정 영역)</span><span class="sxs-lookup"><span data-stu-id="7ea64-1646">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="7ea64-1647">열거된 매개 변수를 제대로 설정하지 않은 새 자동 크기 조정 규칙을 만드는 데 문제가 있습니다(이를 항상 기본값으로 설정함).</span><span class="sxs-lookup"><span data-stu-id="7ea64-1647">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="7ea64-1648">해결된 문제 # 7513[자세한 정보] Set-AzDiagnosticSetting은 설정을 생성하는 동안 범주를 명시적으로 지정해야 합니다</span><span class="sxs-lookup"><span data-stu-id="7ea64-1648">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="7ea64-1649">이제 cmdlet은 생성 중에 사용할 범주를 명시적으로 표시할 필요가 없습니다. 즉, 문서화된대로 작동합니다</span><span class="sxs-lookup"><span data-stu-id="7ea64-1649">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7ea64-1650">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7ea64-1650">Az.Network</span></span>
* <span data-ttu-id="7ea64-1651">다음 cmdlet에 대해 PeeringType을 필수 매개 변수로 변경했습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-1651">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="7ea64-1652">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="7ea64-1652">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="7ea64-1653">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="7ea64-1653">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="7ea64-1654">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="7ea64-1654">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="7ea64-1655">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="7ea64-1655">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="7ea64-1656">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="7ea64-1656">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="7ea64-1657">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="7ea64-1657">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="7ea64-1658">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="7ea64-1658">Az.PolicyInsights</span></span>
* <span data-ttu-id="7ea64-1659">추가된 정책 재구성 cmdlet</span><span class="sxs-lookup"><span data-stu-id="7ea64-1659">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="7ea64-1660">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7ea64-1660">Az.Resources</span></span>
* <span data-ttu-id="7ea64-1661">에 대 한 수정 https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="7ea64-1661">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="7ea64-1662">'Get-AzResource'에 대해 '-ResourceId' 매개 변수를 사용하여 리소스 나열 허용</span><span class="sxs-lookup"><span data-stu-id="7ea64-1662">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="7ea64-1663">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="7ea64-1663">Az.ServiceBus</span></span>
* <span data-ttu-id="7ea64-1664">마이그레이션 상태를 알 수 있도록 PSServiceBusMigrationConfigurationAttributes에 MigrationState 읽기 전용 속성 추가.</span><span class="sxs-lookup"><span data-stu-id="7ea64-1664">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="7ea64-1665">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="7ea64-1665">Az.ServiceFabric</span></span>
* <span data-ttu-id="7ea64-1666">Linux Vmss에 인증서 추가 수정.</span><span class="sxs-lookup"><span data-stu-id="7ea64-1666">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="7ea64-1667">Add-AzServiceFabricClusterCertificate 수정</span><span class="sxs-lookup"><span data-stu-id="7ea64-1667">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="7ea64-1668">새 인증서(Azure/service-fabric-issues#932)에서 올바른 지문을 사용.</span><span class="sxs-lookup"><span data-stu-id="7ea64-1668">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="7ea64-1669">올바르게 예외 표시(Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="7ea64-1669">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="7ea64-1670">Vmss CreateOrUpdate 작업을 시작하기 전에 'Update-AzServiceFabricDurability'를 수정하여 클러스터 구성 업데이트.</span><span class="sxs-lookup"><span data-stu-id="7ea64-1670">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="7ea64-1671">0.4.0 - 2018년 10월</span><span class="sxs-lookup"><span data-stu-id="7ea64-1671">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="7ea64-1672">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="7ea64-1672">Az.Profile</span></span>
* <span data-ttu-id="7ea64-1673">CloudShell에서 Get-AzSubscription을 사용하여 문제를 해결합니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-1673">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="7ea64-1674">ClientRuntime의 최신 버전을 사용하도록 일반적인 코드를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-1674">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7ea64-1675">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7ea64-1675">Az.Compute</span></span>
* <span data-ttu-id="7ea64-1676">'New-AzVm'에 대해 간단한 매개 변수를 사용하는 경우 가속화된 네트워킹을 설정하기 위해 새 크기가 VM 크기의 허용 목록에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-1676">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="7ea64-1677">모든 cmdlet에 ResourceName 인수 완성자가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-1677">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="7ea64-1678">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="7ea64-1678">Az.DataLakeStore</span></span>
* <span data-ttu-id="7ea64-1679">Virtual Network 규칙에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="7ea64-1679">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="7ea64-1680">Get-AzDataLakeStoreVirtualNetworkRule: Azure Data Lake Store 가상 네트워크 규칙을 가져오거나 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-1680">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="7ea64-1681">Add-AzDataLakeStoreVirtualNetworkRule: 지정된 Data Lake Store 계정에 가상 네트워크 규칙을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-1681">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="7ea64-1682">Set-AzDataLakeStoreVirtualNetworkRule: 지정된 Data Lake Store 계정에 지정된 가상 네트워크 규칙을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-1682">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="7ea64-1683">Remove-AzDataLakeStoreVirtualNetworkRule: Azure Data Lake Store 가상 네트워크 규칙을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-1683">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7ea64-1684">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7ea64-1684">Az.Network</span></span>
* <span data-ttu-id="7ea64-1685">Test-AzNetworkWatcherConnectivity cmdlet을 업데이트하고, 백 엔드에 프로토콜 값을 전달합니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-1685">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="7ea64-1686">모든 cmdlet에 ResourceName 인수 완성자가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-1686">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="7ea64-1687">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7ea64-1687">Az.Resources</span></span>
* <span data-ttu-id="7ea64-1688">(기본 프로필에 구독이 없고 범위가 지정되지 않은 경우) 시나리오에서 의미 있는 예외를 추가하여 Get-AzRoleDefinition이 인식할 수 없는 예외를 throw하는 문제를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-1688">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="7ea64-1689">또한 기본 매개 변수 집합을 'RoleDefinitionNameParameterSet'으로 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-1689">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="7ea64-1690">0.3.0 - 2018년 10월</span><span class="sxs-lookup"><span data-stu-id="7ea64-1690">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="7ea64-1691">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="7ea64-1691">Azure.Storage</span></span>
* <span data-ttu-id="7ea64-1692">대상에 메타데이터가 있을 때 Blob/파일이 메타 데이터를 복사하지 않는 문제 수정</span><span class="sxs-lookup"><span data-stu-id="7ea64-1692">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="7ea64-1693">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="7ea64-1693">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="7ea64-1694">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="7ea64-1694">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="7ea64-1695">특정 위치의 스토리지 리소스 사용을 지원하고 글로벌 스토리지 리소스 사용 가져오기는 더 이상 사용되지 않는다는 경고 메시지를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-1695">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="7ea64-1696">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="7ea64-1696">Get-AzStorageUsage</span></span>
    
#### <a name="azcognitiveservices"></a><span data-ttu-id="7ea64-1697">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="7ea64-1697">Az.CognitiveServices</span></span>
* <span data-ttu-id="7ea64-1698">기존 계정이 없는 Get-AzCognitiveServicesAccountSkus를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-1698">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7ea64-1699">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7ea64-1699">Az.Compute</span></span>
* <span data-ttu-id="7ea64-1700">Get-AzVM -ResourceGroupName <rg>가 필요한 경우 50개가 넘는 결과를 반환하도록 수정</span><span class="sxs-lookup"><span data-stu-id="7ea64-1700">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="7ea64-1701">'SimpleParameterSet' 예제가 New-AzVmss cmdlet 도움말에 추가됨</span><span class="sxs-lookup"><span data-stu-id="7ea64-1701">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="7ea64-1702">Azure Disk Encryption 진행률 메시지의 오타를 수정</span><span class="sxs-lookup"><span data-stu-id="7ea64-1702">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="7ea64-1703">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="7ea64-1703">Az.DataFactoryV2</span></span>
* <span data-ttu-id="7ea64-1704">ADF.Net SDK 버전을 2.3.0으로 업데이트</span><span class="sxs-lookup"><span data-stu-id="7ea64-1704">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7ea64-1705">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7ea64-1705">Az.Network</span></span>
* <span data-ttu-id="7ea64-1706">NetworkProfile 기능 추가</span><span class="sxs-lookup"><span data-stu-id="7ea64-1706">Added NetworkProfile functionality.</span></span> <span data-ttu-id="7ea64-1707">추가된 새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-1707">new cmdlets added</span></span>
    - <span data-ttu-id="7ea64-1708">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="7ea64-1708">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="7ea64-1709">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="7ea64-1709">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="7ea64-1710">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="7ea64-1710">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="7ea64-1711">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="7ea64-1711">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="7ea64-1712">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="7ea64-1712">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="7ea64-1713">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="7ea64-1713">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="7ea64-1714">서브넷 모델에 서비스 연결 링크 추가</span><span class="sxs-lookup"><span data-stu-id="7ea64-1714">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="7ea64-1715">New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="7ea64-1715">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="7ea64-1716">Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="7ea64-1716">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="7ea64-1717">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="7ea64-1717">Az.RedisCache</span></span>
* <span data-ttu-id="7ea64-1718">모든 문자열을 Size 매개 변수로 진행되도록 허용</span><span class="sxs-lookup"><span data-stu-id="7ea64-1718">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="7ea64-1719">PSArgumentCompleter 팝업에 P5 추가</span><span class="sxs-lookup"><span data-stu-id="7ea64-1719">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="7ea64-1720">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7ea64-1720">Az.Resources</span></span>
* <span data-ttu-id="7ea64-1721">-Mode 매개 변수를 Set-AzPolicyDefinition에 추가</span><span class="sxs-lookup"><span data-stu-id="7ea64-1721">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="7ea64-1722">사용자가 포함된 Origin 작업에서 Get-AzProviderOperation commandlet 버그 수정</span><span class="sxs-lookup"><span data-stu-id="7ea64-1722">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="7ea64-1723">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7ea64-1723">Az.Sql</span></span>
* <span data-ttu-id="7ea64-1724">일부 백업 cmdlet이 현재 azure 구독을 인식하지 않는 문제 해결</span><span class="sxs-lookup"><span data-stu-id="7ea64-1724">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="7ea64-1725">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="7ea64-1725">Az.Websites</span></span>
* <span data-ttu-id="7ea64-1726">새 cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - 컨테이너 지속적인 배포 Webhook URL을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-1726">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="7ea64-1727">새 cmdlet New-AzWebAppContainerPSSession 및 Enter-WebAppContainerPSSession -  windows 컨테이너 앱에 PowerShell 원격 세션을 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="7ea64-1727">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="7ea64-1728">0.2.0 - 2018년 9월</span><span class="sxs-lookup"><span data-stu-id="7ea64-1728">0.2.0 - September 2018</span></span>
 <span data-ttu-id="7ea64-1729">최초 릴리스</span><span class="sxs-lookup"><span data-stu-id="7ea64-1729">Initial Release</span></span>
