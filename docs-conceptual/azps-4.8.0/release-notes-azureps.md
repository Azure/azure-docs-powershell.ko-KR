---
title: Azure PowerShell 릴리스 정보
description: Azure PowerShell 모듈의 모든 최신 업데이트에 대해 알아봅니다.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/10/2020
ms.custom: devx-track-azurepowershell
ms.service: azure-powershell
ms.openlocfilehash: ea374b23e85c16393e5de16b043ae0c28545cb61
ms.sourcegitcommit: 2036538797dd088728aee5ac5021472454d82eb2
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/06/2020
ms.locfileid: "93408074"
---
# <a name="azure-powershell-release-notes"></a><span data-ttu-id="1d1eb-103">Azure PowerShell 릴리스 정보</span><span class="sxs-lookup"><span data-stu-id="1d1eb-103">Azure PowerShell release notes</span></span>

## <a name="480---october-2020"></a><span data-ttu-id="1d1eb-104">4.8.0 - 2020년 10월</span><span class="sxs-lookup"><span data-stu-id="1d1eb-104">4.8.0 - October 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="1d1eb-105">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="1d1eb-105">Az.Accounts</span></span>
* <span data-ttu-id="1d1eb-106">공용 라이브러리의 DateTime 구문 분석 문제 해결[#13045]</span><span class="sxs-lookup"><span data-stu-id="1d1eb-106">Fixed DateTime parse issue in common libraries [#13045]</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="1d1eb-107">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="1d1eb-107">Az.CognitiveServices</span></span>
* <span data-ttu-id="1d1eb-108">'New-AzCognitiveServicesAccountApiProperty' cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-108">Added 'New-AzCognitiveServicesAccountApiProperty' cmdlet.</span></span>
* <span data-ttu-id="1d1eb-109">'New-AzCognitiveServicesAccount' 및 'Set-AzCognitiveServicesAccount'에 대해 'ApiProperty' 매개 변수 지원됨</span><span class="sxs-lookup"><span data-stu-id="1d1eb-109">Supported 'ApiProperty' parameter for 'New-AzCognitiveServicesAccount' and 'Set-AzCognitiveServicesAccount'</span></span>

#### <a name="azcompute"></a><span data-ttu-id="1d1eb-110">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="1d1eb-110">Az.Compute</span></span>
* <span data-ttu-id="1d1eb-111">FailoverTypes를 채워서 'Update-ASRRecoveryPlan'의 문제 해결</span><span class="sxs-lookup"><span data-stu-id="1d1eb-111">Fixed issue in 'Update-ASRRecoveryPlan' by populating FailoverTypes</span></span>
* <span data-ttu-id="1d1eb-112">'Get-AzVmImage' cmdlet에 '-Top' 및 '-OrderBy' 선택적 매개 변수를 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-112">Added the '-Top' and '-OrderBy' optional parameters to the 'Get-AzVmImage' cmdlet.</span></span> 

#### <a name="azdatabricks"></a><span data-ttu-id="1d1eb-113">Az.Databricks</span><span class="sxs-lookup"><span data-stu-id="1d1eb-113">Az.Databricks</span></span>
* <span data-ttu-id="1d1eb-114">'Az.Databricks' 모듈의 일반 공급</span><span class="sxs-lookup"><span data-stu-id="1d1eb-114">General availability of 'Az.Databricks' module</span></span>
* <span data-ttu-id="1d1eb-115">가상 네트워크 피어링에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="1d1eb-115">Added support for virtual network peering</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="1d1eb-116">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="1d1eb-116">Az.DataFactory</span></span>
* <span data-ttu-id="1d1eb-117">출력 메시지의 오타 수정</span><span class="sxs-lookup"><span data-stu-id="1d1eb-117">Fixed typo in output messages</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="1d1eb-118">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="1d1eb-118">Az.EventHub</span></span>
* <span data-ttu-id="1d1eb-119">선택적 스위치 매개 변수 'TrustedServiceAccessEnabled'를 'Set-AzEventHubNetworkRuleSet' cmdlet에 추가</span><span class="sxs-lookup"><span data-stu-id="1d1eb-119">Added optional switch parameter 'TrustedServiceAccessEnabled' to 'Set-AzEventHubNetworkRuleSet' cmdlet</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="1d1eb-120">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="1d1eb-120">Az.HDInsight</span></span>
* <span data-ttu-id="1d1eb-121">'PublicNetworkAccessType' 및 'OutboundPublicNetworkAccessType' 매개 변수 사용 중단 계획에 대한 경고 메시지 추가</span><span class="sxs-lookup"><span data-stu-id="1d1eb-121">Added warning message for planning to deprecate the parameters 'PublicNetworkAccessType' and 'OutboundPublicNetworkAccessType'</span></span>
* <span data-ttu-id="1d1eb-122">'DefaultStorageAccountName' 매개 변수를 'StorageAccountResourceId'로 바꾸려는 계획에 대한 경고 메시지 추가</span><span class="sxs-lookup"><span data-stu-id="1d1eb-122">Added warning message for planning to replace the parameter 'DefaultStorageAccountName' with 'StorageAccountResourceId'</span></span>
* <span data-ttu-id="1d1eb-123">'DefaultStorageAccountKey' 매개 변수를 'StorageAccountKey'로 바꾸려는 계획에 대한 경고 메시지 추가</span><span class="sxs-lookup"><span data-stu-id="1d1eb-123">Added warning message for planning to replace the parameter 'DefaultStorageAccountKey' with 'StorageAccountKey'</span></span>
* <span data-ttu-id="1d1eb-124">'DefaultStorageAccountType' 매개 변수를 'StorageAccountType'으로 바꾸려는 계획에 대한 경고 메시지 추가</span><span class="sxs-lookup"><span data-stu-id="1d1eb-124">Added warning message for planning to replace the parameter 'DefaultStorageAccountType' with 'StorageAccountType'</span></span>
* <span data-ttu-id="1d1eb-125">'DefaultStorageContainer' 매개 변수를 'StorageContainer'로 바꾸려는 계획에 대한 경고 메시지 추가</span><span class="sxs-lookup"><span data-stu-id="1d1eb-125">Added warning message for planning to replace the parameter 'DefaultStorageContainer' with 'StorageContainer'</span></span>
* <span data-ttu-id="1d1eb-126">'DefaultStorageRootPath' 매개 변수를 'StorageRootPath'로 바꾸려는 계획에 대한 경고 메시지 추가</span><span class="sxs-lookup"><span data-stu-id="1d1eb-126">Added warning message for planning to replace the parameter 'DefaultStorageRootPath' with 'StorageRootPath'</span></span>

#### <a name="aziothub"></a><span data-ttu-id="1d1eb-127">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="1d1eb-127">Az.IotHub</span></span>
* <span data-ttu-id="1d1eb-128">업데이트된 디바이스 SDK.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-128">Updated devices sdk.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="1d1eb-129">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="1d1eb-129">Az.KeyVault</span></span>
* <span data-ttu-id="1d1eb-130">SecretValueText 속성 제거 세부 날짜 제공</span><span class="sxs-lookup"><span data-stu-id="1d1eb-130">Provided the detailed date of removing property SecretValueText</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="1d1eb-131">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="1d1eb-131">Az.ManagedServices</span></span>
* <span data-ttu-id="1d1eb-132">관리되는 서비스 할당 및 정의의 cmdlet에 대한 호환성이 손상되는 변경 경고가 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="1d1eb-132">Updated breaking change warnings on cmdlets of managed services assignment and definition</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="1d1eb-133">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="1d1eb-133">Az.Monitor</span></span>
* <span data-ttu-id="1d1eb-134">경고 메시지를 숨길 수 없는 버그를 수정했습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-134">Fixed the bug that warning message cannot be suppressed.</span></span> <span data-ttu-id="1d1eb-135">[#12889]</span><span class="sxs-lookup"><span data-stu-id="1d1eb-135">[#12889]</span></span>
* <span data-ttu-id="1d1eb-136">경고 규칙 기준에서 'SkipMetricValidation' 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-136">Supported 'SkipMetricValidation' parameter in alert rule criteria.</span></span> <span data-ttu-id="1d1eb-137">메트릭 유효성 검사를 건너뛰도록 하여 아직 생성되지 않은 사용자 지정 메트릭에 대한 경고 규칙을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-137">Allows creating an alert rule on a custom metric that isn't yet emitted, by causing the metric validation to be skipped.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="1d1eb-138">Az.Network</span><span class="sxs-lookup"><span data-stu-id="1d1eb-138">Az.Network</span></span>
* <span data-ttu-id="1d1eb-139">VPNSite 리소스에 Office365 정책 추가</span><span class="sxs-lookup"><span data-stu-id="1d1eb-139">Added Office365 Policy to VPNSite Resource</span></span>
    - <span data-ttu-id="1d1eb-140">'New-AzO365PolicyProperty'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-140">'New-AzO365PolicyProperty'</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="1d1eb-141">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="1d1eb-141">Az.RecoveryServices</span></span>
* <span data-ttu-id="1d1eb-142">워크로드 백업에 대한 컨테이너 이름 유효성 검사가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-142">Added container name validation for workload backup.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="1d1eb-143">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="1d1eb-143">Az.RedisCache</span></span>
* <span data-ttu-id="1d1eb-144">Microsoft.Cache RP 등록과 관련된 권한 문제로 인해 'New-AzRedisCache' 및 'Set-AzRedisCache' cmdlet이 실패하지 않도록 함</span><span class="sxs-lookup"><span data-stu-id="1d1eb-144">Made 'New-AzRedisCache' and 'Set-AzRedisCache' cmdlets not fail because of permission issue related to registering Microsoft.Cache RP</span></span>

#### <a name="azsql"></a><span data-ttu-id="1d1eb-145">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="1d1eb-145">Az.Sql</span></span>
* <span data-ttu-id="1d1eb-146">BackupStorageRedundancy가 다음에 추가됨</span><span class="sxs-lookup"><span data-stu-id="1d1eb-146">Added BackupStorageRedundancy to the following:</span></span> 
    - <span data-ttu-id="1d1eb-147">'Restore-AzureRmSqlDatabase'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-147">'Restore-AzureRmSqlDatabase'</span></span>
    - <span data-ttu-id="1d1eb-148">'New-AzSqlDatabaseCopy'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-148">'New-AzSqlDatabaseCopy'</span></span>
    - <span data-ttu-id="1d1eb-149">'New-AzSqlDatabaseSecondary'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-149">'New-AzSqlDatabaseSecondary'</span></span>
* <span data-ttu-id="1d1eb-150">모든 SQL DB 참조에 대한 BackupStorageRedundancy 매개 변수의 대소문자 구분 제거</span><span class="sxs-lookup"><span data-stu-id="1d1eb-150">Removed case sensitivity for BackupStorageRedundancy parameter for all SQL DB references</span></span> 
* <span data-ttu-id="1d1eb-151">BackupStorageRedundancy 경고 메시지 이름 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="1d1eb-151">Updated BackupStorageRedundancy warning message names</span></span>

#### <a name="azstorage"></a><span data-ttu-id="1d1eb-152">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="1d1eb-152">Az.Storage</span></span>
* <span data-ttu-id="1d1eb-153">스토리지 계정의 파일 서비스에서 사용/사용하지 않음/공유 일시 삭제 속성 지원</span><span class="sxs-lookup"><span data-stu-id="1d1eb-153">Supported enable/disable/get share soft delete properties on file Service of a Storage account</span></span>
    - <span data-ttu-id="1d1eb-154">'Update-AzStorageFileServiceProperty'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-154">'Update-AzStorageFileServiceProperty'</span></span>
    - <span data-ttu-id="1d1eb-155">'Get-AzStorageFileServiceProperty'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-155">'Get-AzStorageFileServiceProperty'</span></span>
* <span data-ttu-id="1d1eb-156">지원되는 목록 파일 공유에는 스토리지 계정의 삭제된 공유와 단일 파일 공유 사용량 가져오기가 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-156">Supported list file shares include the deleted ones of a Storage account, and Get single file share usage</span></span>
    - <span data-ttu-id="1d1eb-157">'Get-AzRmStorageShare'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-157">'Get-AzRmStorageShare'</span></span>
* <span data-ttu-id="1d1eb-158">삭제된 파일 공유 복원 지원</span><span class="sxs-lookup"><span data-stu-id="1d1eb-158">Supported restore a deleted file share</span></span>
    - <span data-ttu-id="1d1eb-159">'Restore-AzRmStorageShare'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-159">'Restore-AzRmStorageShare'</span></span>
* <span data-ttu-id="1d1eb-160">Blob 서비스 속성을 수정하기 위한 cmdlet을 변경하여, 서버에서 원래 속성을 가져오지 않으며 수정된 속성만 서버로 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-160">Changed the cmdlets for modify blob service properties, won't get the original properties from server, but only set the modified properties to server.</span></span>
    - <span data-ttu-id="1d1eb-161">'Enable-AzStorageBlobDeleteRetentionPolicy'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-161">'Enable-AzStorageBlobDeleteRetentionPolicy'</span></span>
    - <span data-ttu-id="1d1eb-162">'Disable-AzStorageBlobDeleteRetentionPolicy'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-162">'Disable-AzStorageBlobDeleteRetentionPolicy'</span></span>  
    - <span data-ttu-id="1d1eb-163">'Enable-AzStorageBlobRestorePolicy'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-163">'Enable-AzStorageBlobRestorePolicy'</span></span>
    - <span data-ttu-id="1d1eb-164">'Disable-AzStorageBlobRestorePolicy'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-164">'Disable-AzStorageBlobRestorePolicy'</span></span>
    - <span data-ttu-id="1d1eb-165">'Update-AzStorageBlobServiceProperty'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-165">'Update-AzStorageBlobServiceProperty'</span></span>
* <span data-ttu-id="1d1eb-166">New-AzStorageAccount 매개 변수 -Kind 기본값에 대한 도움말 문제 해결[#12189]</span><span class="sxs-lookup"><span data-stu-id="1d1eb-166">Fixed help issue for New-AzStorageAccount parameter -Kind default value [#12189]</span></span>
* <span data-ttu-id="1d1eb-167">Blob 업로드에서 올바른 ContentType을 설정하는 방법을 보여주는 예제를 추가하여 문제 해결[#12989]</span><span class="sxs-lookup"><span data-stu-id="1d1eb-167">Fixed issue by add example to show how to set correct ContentType in blob upload [#12989]</span></span>

## <a name="470---september-2020"></a><span data-ttu-id="1d1eb-168">4.7.0 - 2020년 9월</span><span class="sxs-lookup"><span data-stu-id="1d1eb-168">4.7.0 - September 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="1d1eb-169">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="1d1eb-169">Az.Accounts</span></span>
* <span data-ttu-id="1d1eb-170">예정된 호환성이 손상되는 변경 메시지의 형식이 지정됨</span><span class="sxs-lookup"><span data-stu-id="1d1eb-170">Formatted the upcoming breaking change messages</span></span>
* <span data-ttu-id="1d1eb-171">Azure.Core가 1.4.1로 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="1d1eb-171">Updated Azure.Core to 1.4.1</span></span>

#### <a name="azaks"></a><span data-ttu-id="1d1eb-172">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="1d1eb-172">Az.Aks</span></span>
* <span data-ttu-id="1d1eb-173">'New-AzAksCluster', 'Set-AzAksCluster' 및 'New-AzAksNodePool'에 대한 클라이언트 쪽 매개 변수 유효성 검사 논리가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-173">Added client side parameter validation logic for 'New-AzAksCluster', 'Set-AzAksCluster' and 'New-AzAksNodePool'.</span></span> <span data-ttu-id="1d1eb-174">[#12372]</span><span class="sxs-lookup"><span data-stu-id="1d1eb-174">[#12372]</span></span>
* <span data-ttu-id="1d1eb-175">'New-AzAksCluster'에서 추가 항목에 대한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-175">Added support for add-ons in 'New-AzAksCluster'.</span></span> <span data-ttu-id="1d1eb-176">[#11239]</span><span class="sxs-lookup"><span data-stu-id="1d1eb-176">[#11239]</span></span>
* <span data-ttu-id="1d1eb-177">추가 항목에 대한 'Enable-AzAksAddOn' 및 'Disable-AzAksAddOn' cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-177">Added cmdlets 'Enable-AzAksAddOn' and 'Disable-AzAksAddOn' for add-ons.</span></span> <span data-ttu-id="1d1eb-178">[#11239]</span><span class="sxs-lookup"><span data-stu-id="1d1eb-178">[#11239]</span></span>
* <span data-ttu-id="1d1eb-179">'New-AzAksCluster'에 대한 매개 변수 'GenerateSshKey'가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-179">Added parameter 'GenerateSshKey' for 'New-AzAksCluster'.</span></span> <span data-ttu-id="1d1eb-180">[#12371]</span><span class="sxs-lookup"><span data-stu-id="1d1eb-180">[#12371]</span></span>
* <span data-ttu-id="1d1eb-181">API 버전이 2020-06-01로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-181">Updated api version to 2020-06-01.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="1d1eb-182">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="1d1eb-182">Az.CognitiveServices</span></span>
* <span data-ttu-id="1d1eb-183">특정 API에 대한 추가 법률 용어를 표시했습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-183">Showed additional legal terms for certain APIs.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="1d1eb-184">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="1d1eb-184">Az.Compute</span></span>
* <span data-ttu-id="1d1eb-185">'New-AzVmDiskEncryptionSetConfig'에 '-EncryptionType' 선택적 매개 변수가 추가됨</span><span class="sxs-lookup"><span data-stu-id="1d1eb-185">Added the '-EncryptionType' optional parameter to 'New-AzVmDiskEncryptionSetConfig'</span></span>
* <span data-ttu-id="1d1eb-186">새 리소스 종류에 대한 새 cmdlet: DiskAccess 'Get-AzDiskAccess', 'New-AzDiskAccess', 'Get-AzDiskAccess'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-186">New cmdlets for new resource type: DiskAccess 'Get-AzDiskAccess', 'New-AzDiskAccess', 'Get-AzDiskAccess'</span></span>
* <span data-ttu-id="1d1eb-187">'New-AzSnapshotConfig'에 선택적 매개 변수 '-DiskAccessId' 및 '-NetworkAccessPolicy'가 추가됨</span><span class="sxs-lookup"><span data-stu-id="1d1eb-187">Added optional parameters '-DiskAccessId' and '-NetworkAccessPolicy' to 'New-AzSnapshotConfig'</span></span>
* <span data-ttu-id="1d1eb-188">'New-AzDiskConfig'에 선택적 매개 변수 '-DiskAccessId' 및 '-NetworkAccessPolicy'가 추가됨</span><span class="sxs-lookup"><span data-stu-id="1d1eb-188">Added optional parameters '-DiskAccessId' and '-NetworkAccessPolicy' to 'New-AzDiskConfig'</span></span>
* <span data-ttu-id="1d1eb-189">VirtualMachine 인스턴스 보기에 'PatchStatus' 속성이 추가됨</span><span class="sxs-lookup"><span data-stu-id="1d1eb-189">Added 'PatchStatus' property to VirtualMachine Instance View</span></span>
* <span data-ttu-id="1d1eb-190">가상 머신의 인스턴스 보기에 'VMHealth' 속성이 추가됨. 이 속성은 'Get-AzVm'이 '-Status'로 호출될 때 반환되는 개체</span><span class="sxs-lookup"><span data-stu-id="1d1eb-190">Added 'VMHealth' property to the virtual machine's instance view, which is the returned object when 'Get-AzVm' is invoked with '-Status'</span></span>
* <span data-ttu-id="1d1eb-191">'Get-AzVM' 및 'Get-AzVmss' 인스턴스 보기에 'AssignedHost' 필드가 추가됨</span><span class="sxs-lookup"><span data-stu-id="1d1eb-191">Added 'AssignedHost' field to 'Get-AzVM' and 'Get-AzVmss' instance views.</span></span> <span data-ttu-id="1d1eb-192">필드는 가상 머신 인스턴스의 리소스 ID를 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-192">The field shows the resource id of the virtual machine instance</span></span>
* <span data-ttu-id="1d1eb-193">선택적 매개 변수 '-SupportAutomaticPlacement'가 'New-AzHostGroup'에 추가됨</span><span class="sxs-lookup"><span data-stu-id="1d1eb-193">Added optional parameter '-SupportAutomaticPlacement' to 'New-AzHostGroup'</span></span> 
* <span data-ttu-id="1d1eb-194">'-HostGroupId' 매개 변수가 'New-AzVm' 및 'New-AzVmss'에 추가됨</span><span class="sxs-lookup"><span data-stu-id="1d1eb-194">Added the '-HostGroupId' parameter to 'New-AzVm' and 'New-AzVmss'</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="1d1eb-195">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="1d1eb-195">Az.DataFactory</span></span>
* <span data-ttu-id="1d1eb-196">ADF .Net SDK 버전이 4.11.0으로 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="1d1eb-196">Updated ADF .Net SDK version to 4.11.0</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="1d1eb-197">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="1d1eb-197">Az.EventHub</span></span>
* <span data-ttu-id="1d1eb-198">새 클러스터 cmdlet 추가됨 - 'New-AzEventHubCluster', 'Set-AzEventHubCluster', 'Get-AzEventHubCluster', 'Remove-AzEventHubCluster', 'Get-AzEventHubClustersAvailableRegions'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-198">Added new Cluster cmdlets - 'New-AzEventHubCluster', 'Set-AzEventHubCluster', 'Get-AzEventHubCluster', 'Remove-AzEventHubCluster', 'Get-AzEventHubClustersAvailableRegions'.</span></span>
* <span data-ttu-id="1d1eb-199">#10722 문제 해결됨: AuthorizationRule 권한에 'Listen'만 할당하는 문제가 해결되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-199">Fixed for issue #10722 : Fix for assigning only 'Listen' to AuthorizationRule rights.</span></span>

#### <a name="azfunctions"></a><span data-ttu-id="1d1eb-200">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="1d1eb-200">Az.Functions</span></span>
* <span data-ttu-id="1d1eb-201">v2 Functions를 지원하지 않는 지역에서 생성하는 기능이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-201">Removed the ability to create v2 Functions in regions that do not support it.</span></span>
* <span data-ttu-id="1d1eb-202">PowerShell 6.2가 사용되지 않음</span><span class="sxs-lookup"><span data-stu-id="1d1eb-202">Deprecated PowerShell 6.2.</span></span> <span data-ttu-id="1d1eb-203">사용자가 PowerShell 6.2 함수 앱을 만들 때 PowerShell 7.0 함수 앱을 만들도록 권장하는 경고가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-203">Added a warning for when a user creates a PowerShell 6.2 function app that advises them to create a PowerShell 7.0 function app instead.</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="1d1eb-204">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="1d1eb-204">Az.HDInsight</span></span>
* <span data-ttu-id="1d1eb-205">자동 크기 조정 구성을 사용하여 클러스터 만들기 지원</span><span class="sxs-lookup"><span data-stu-id="1d1eb-205">Supported creating cluster with Autoscale configuration</span></span>
    - <span data-ttu-id="1d1eb-206">cmdlet 'New-AzHDInsightCluster'에 새 매개 변수 'AutoscaleConfiguration' 추가</span><span class="sxs-lookup"><span data-stu-id="1d1eb-206">Add new parameter 'AutoscaleConfiguration' to the cmdlet 'New-AzHDInsightCluster'</span></span>
* <span data-ttu-id="1d1eb-207">운영 클러스터의 자동 크기 조정 구성 지원됨</span><span class="sxs-lookup"><span data-stu-id="1d1eb-207">Supported operating cluster's Autoscale configuration</span></span>
    - <span data-ttu-id="1d1eb-208">새 cmdlet 'Get-AzHDInsihgtClusterAutoscaleConfiguration' 추가</span><span class="sxs-lookup"><span data-stu-id="1d1eb-208">Add new cmdlet 'Get-AzHDInsihgtClusterAutoscaleConfiguration'</span></span>
    - <span data-ttu-id="1d1eb-209">새 cmdlet 'New-AzHDInsihgtClusterAutoscaleConfiguration' 추가</span><span class="sxs-lookup"><span data-stu-id="1d1eb-209">Add new cmdlet 'New-AzHDInsihgtClusterAutoscaleConfiguration'</span></span>
    - <span data-ttu-id="1d1eb-210">새 cmdlet 'Set-AzHDInsihgtClusterAutoscaleConfiguration' 추가</span><span class="sxs-lookup"><span data-stu-id="1d1eb-210">Add new cmdlet 'Set-AzHDInsihgtClusterAutoscaleConfiguration'</span></span>
    - <span data-ttu-id="1d1eb-211">새 cmdlet 'Remove-AzHDInsihgtClusterAutoscaleConfiguration' 추가</span><span class="sxs-lookup"><span data-stu-id="1d1eb-211">Add new cmdlet 'Remove-AzHDInsihgtClusterAutoscaleConfiguration'</span></span>
    - <span data-ttu-id="1d1eb-212">새 cmdlet 'New-AzHDInsihgtClusterAutoscaleScheduleCondition' 추가</span><span class="sxs-lookup"><span data-stu-id="1d1eb-212">Add new cmdlet 'New-AzHDInsihgtClusterAutoscaleScheduleCondition'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="1d1eb-213">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="1d1eb-213">Az.KeyVault</span></span>
* <span data-ttu-id="1d1eb-214">RBAC 권한 부여에 대한 지원 추가됨 [#10557]</span><span class="sxs-lookup"><span data-stu-id="1d1eb-214">Added support for RBAC authorization [#10557]</span></span>
* <span data-ttu-id="1d1eb-215">'Set-AzKeyVaultAccessPolicy'에서 향상된 오류 처리 [#4007]</span><span class="sxs-lookup"><span data-stu-id="1d1eb-215">Enhanced error handling in 'Set-AzKeyVaultAccessPolicy' [#4007]</span></span>

#### <a name="azkusto"></a><span data-ttu-id="1d1eb-216">Az.Kusto</span><span class="sxs-lookup"><span data-stu-id="1d1eb-216">Az.Kusto</span></span>
* <span data-ttu-id="1d1eb-217">'Az.Kusto' 모듈의 일반 공급</span><span class="sxs-lookup"><span data-stu-id="1d1eb-217">General availability of 'Az.Kusto' module</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="1d1eb-218">Az.Network</span><span class="sxs-lookup"><span data-stu-id="1d1eb-218">Az.Network</span></span>
* <span data-ttu-id="1d1eb-219">[호환성이 손상되는 변경] 리소스 가상 라우터 및 가상 허브에 맞게 아래 cmdlet이 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="1d1eb-219">[Breaking Change] Updated below cmdlets to align resource virtual router and virtual hub</span></span>
    - <span data-ttu-id="1d1eb-220">'New-AzVirtualRouter':</span><span class="sxs-lookup"><span data-stu-id="1d1eb-220">'New-AzVirtualRouter':</span></span> 
        - <span data-ttu-id="1d1eb-221">IP 구성 자식 리소스를 지원하는 -HostedSubnet 매개 변수가 추가됨</span><span class="sxs-lookup"><span data-stu-id="1d1eb-221">Added -HostedSubnet parameter to support IP configuration child resource</span></span>
        - <span data-ttu-id="1d1eb-222">-HostedGateway 및 -HostedGatewayId 삭제됨</span><span class="sxs-lookup"><span data-stu-id="1d1eb-222">deleted -HostedGateway and -HostedGatewayId</span></span>
    - <span data-ttu-id="1d1eb-223">'Get-AzVirtualRouter':</span><span class="sxs-lookup"><span data-stu-id="1d1eb-223">'Get-AzVirtualRouter':</span></span>
        - <span data-ttu-id="1d1eb-224">구독 수준 매개 변수 집합이 추가됨</span><span class="sxs-lookup"><span data-stu-id="1d1eb-224">Added subscription level parameter set</span></span>
    - <span data-ttu-id="1d1eb-225">'Remove-AzVirtualRouter'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-225">'Remove-AzVirtualRouter'</span></span>
    - <span data-ttu-id="1d1eb-226">'Add-AzVirtualRouterPeer'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-226">'Add-AzVirtualRouterPeer'</span></span>
    - <span data-ttu-id="1d1eb-227">'Get-AzVirtualRouterPeer'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-227">'Get-AzVirtualRouterPeer'</span></span>
    - <span data-ttu-id="1d1eb-228">'Remove-AzVirtualRouterPeer'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-228">'Remove-AzVirtualRouterPeer'</span></span>
* <span data-ttu-id="1d1eb-229">Azure Express 경로 포트에 대해 새 cmdlet이 추가됨</span><span class="sxs-lookup"><span data-stu-id="1d1eb-229">Added new cmdlet for Azure Express Route Port</span></span>
    - <span data-ttu-id="1d1eb-230">'New-AzExpressRoutePortLOA'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-230">'New-AzExpressRoutePortLOA'</span></span>
* <span data-ttu-id="1d1eb-231">VirtualNetwork 피어링 리소스에 RemoteBgpCommunities 속성이 추가됨</span><span class="sxs-lookup"><span data-stu-id="1d1eb-231">Added RemoteBgpCommunities property to the VirtualNetwork Peering Resource</span></span>
* <span data-ttu-id="1d1eb-232">'New-AzLoadBalancerFrontendIpConfig', 'New-AzPublicIpAddress' 및 'New-AzPublicIpPrefix'에 대한 경고 메시지를 수정했습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-232">Modified the warning message for 'New-AzLoadBalancerFrontendIpConfig', 'New-AzPublicIpAddress' and 'New-AzPublicIpPrefix'.</span></span>
* <span data-ttu-id="1d1eb-233">'Get-AzVpnGateway' 출력에 VpnGatewayIpConfigurations가 추가됨</span><span class="sxs-lookup"><span data-stu-id="1d1eb-233">Added VpnGatewayIpConfigurations to 'Get-AzVpnGateway' output</span></span>
* <span data-ttu-id="1d1eb-234">'Set-AzApplicationGatewaySslCertificate'의 버그 수정됨 [#9488]</span><span class="sxs-lookup"><span data-stu-id="1d1eb-234">Fixed bug for 'Set-AzApplicationGatewaySslCertificate' [#9488]</span></span>
* <span data-ttu-id="1d1eb-235">'AzureFirewall'에 'AllowActiveFTP' 매개 변수가 추가됨</span><span class="sxs-lookup"><span data-stu-id="1d1eb-235">Added 'AllowActiveFTP' parameter to 'AzureFirewall'</span></span>
* <span data-ttu-id="1d1eb-236">기능에 대한 새로운 명령이 업데이트됨: VirtualWan P2SVpnGateway에서 인터넷 보안 설정 사용/제거</span><span class="sxs-lookup"><span data-stu-id="1d1eb-236">Updated below commands for feature: Enable internet security set/remove on VirtualWan P2SVpnGateway.</span></span>
- <span data-ttu-id="1d1eb-237">'New-AzP2sVpnGateway' 업데이트됨: 고객이 P2SVpnGateway에서 인터넷 보안을 사용하도록 true를 설정할 수 있는 선택적 스위치 매개 변수 'EnableInternetSecurityFlag'가 추가되었으며, 이는 지점 및 사이트 간 클라이언트에 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-237">Updated 'New-AzP2sVpnGateway': Added optional switch parameter 'EnableInternetSecurityFlag' for customers to set true to enable internet security on P2SVpnGateway, which will be applied for Point to site clients.</span></span>
- <span data-ttu-id="1d1eb-238">'Update-AzP2sVpnGateway' 업데이트됨: 고객이 P2SVpnGateway에서 인터넷 보안을 활성화/비활성화하도록 true/false를 설정할 수 있는 선택적 스위치 매개 변수 'EnableInternetSecurityFlag' 또는 'DisableInternetSecurityFlag'가 추가되었으며, 이는 지점 및 사이트 간 클라이언트에 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-238">Updated 'Update-AzP2sVpnGateway': Added optional switch parameters 'EnableInternetSecurityFlag' or 'DisableInternetSecurityFlag' for customers to set true/false to enable/disable internet security on P2SVpnGateway, which will be applied for Point to site clients.</span></span>
* <span data-ttu-id="1d1eb-239">문제 해결을 위해 VirtualWan P2SVPNGateway를 재설정/재부팅할 수 있도록 새 cmdlet 'Reset-AzP2sVpnGateway'를 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-239">Added new cmdlet 'Reset-AzP2sVpnGateway' for customers to reset/reboot their VirtualWan P2SVpnGateway for troubleshooting.</span></span>
* <span data-ttu-id="1d1eb-240">문제 해결을 위해 VirtualWan VpnGateway를 재설정/재부팅할 수 있도록 새 cmdlet 'Reset-AzVpnGateway'를 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-240">Added new cmdlet 'Reset-AzVpnGateway' for customers to reset/reboot their VirtualWan VpnGateway for troubleshooting.</span></span>
* <span data-ttu-id="1d1eb-241">'Set-AzVirtualNetworkSubnetConfig' 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="1d1eb-241">Updated 'Set-AzVirtualNetworkSubnetConfig'</span></span>
    - <span data-ttu-id="1d1eb-242">매개 변수에 명시적으로 설정된 경우 서브넷의 NSG 및 라우팅 테이블 속성을 null로 설정 [# 1548][# 9718]</span><span class="sxs-lookup"><span data-stu-id="1d1eb-242">Set NSG and Route Table properties of subnet to null if explicitly set in parameters [#1548][#9718]</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="1d1eb-243">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="1d1eb-243">Az.RecoveryServices</span></span>
* <span data-ttu-id="1d1eb-244">워크로드 백업 항목에 대한 삭제 상태가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-244">Fixed the Delete State for workload Backup Items.</span></span>

#### <a name="azresources"></a><span data-ttu-id="1d1eb-245">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="1d1eb-245">Az.Resources</span></span>
* <span data-ttu-id="1d1eb-246">Set-AzRoleAssignment에 대한 누락된 검사 추가됨</span><span class="sxs-lookup"><span data-stu-id="1d1eb-246">Added missing check for Set-AzRoleAssignment</span></span>
* <span data-ttu-id="1d1eb-247">'Get-AzResourceGroupDeploymentOperation'의 'SubscriptionId' 매개 변수에 호환성이 손상되는 변경 특성이 추가됨</span><span class="sxs-lookup"><span data-stu-id="1d1eb-247">Added breaking change attribute to 'SubscriptionId' parameter of 'Get-AzResourceGroupDeploymentOperation'</span></span>
* <span data-ttu-id="1d1eb-248">마지막으로 'Ignore' 리소스 변경을 표시하도록 ARM 템플릿 What-If cmdlet이 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="1d1eb-248">Updated ARM template What-If cmdlets to show 'Ignore' resource changes last</span></span>
* <span data-ttu-id="1d1eb-249">배포 cmdlet에 대한 보안 및 배열 매개 변수 직렬화 문제가 해결됨 [#12773]</span><span class="sxs-lookup"><span data-stu-id="1d1eb-249">Fixed secure and array parameter serialization issues for deployment cmdlets [#12773]</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="1d1eb-250">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="1d1eb-250">Az.ServiceFabric</span></span>
* <span data-ttu-id="1d1eb-251">관리형 클러스터 및 노드 유형에 대해 다음과 같은 새 cmdlet가 추가됨</span><span class="sxs-lookup"><span data-stu-id="1d1eb-251">Added new cmdlets for managed clusters and node types:</span></span>
    - <span data-ttu-id="1d1eb-252">'New-AzServiceFabricManagedCluster'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-252">'New-AzServiceFabricManagedCluster'</span></span>
    - <span data-ttu-id="1d1eb-253">'Get-AzServiceFabricManagedCluster'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-253">'Get-AzServiceFabricManagedCluster'</span></span>
    - <span data-ttu-id="1d1eb-254">'Set-AzServiceFabricManagedCluster'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-254">'Set-AzServiceFabricManagedCluster'</span></span>
    - <span data-ttu-id="1d1eb-255">'Remove-AzServiceFabricManagedCluster'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-255">'Remove-AzServiceFabricManagedCluster'</span></span>
    - <span data-ttu-id="1d1eb-256">'Add-AzServiceFabricManagedClusterClientCertificate'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-256">'Add-AzServiceFabricManagedClusterClientCertificate'</span></span>
    - <span data-ttu-id="1d1eb-257">'Remove-AzServiceFabricManagedClusterClientCertificate'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-257">'Remove-AzServiceFabricManagedClusterClientCertificate'</span></span>
    - <span data-ttu-id="1d1eb-258">'New-AzServiceFabricManagedNodeType'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-258">'New-AzServiceFabricManagedNodeType'</span></span>
    - <span data-ttu-id="1d1eb-259">'Get-AzServiceFabricManagedNodeType'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-259">'Get-AzServiceFabricManagedNodeType'</span></span>
    - <span data-ttu-id="1d1eb-260">'Set-AzServiceFabricManagedNodeType'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-260">'Set-AzServiceFabricManagedNodeType'</span></span>
    - <span data-ttu-id="1d1eb-261">'Remove-AzServiceFabricManagedNodeType'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-261">'Remove-AzServiceFabricManagedNodeType'</span></span>
    - <span data-ttu-id="1d1eb-262">'Add-AzServiceFabricManagedNodeTypeVMExtension'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-262">'Add-AzServiceFabricManagedNodeTypeVMExtension'</span></span>
    - <span data-ttu-id="1d1eb-263">'Add-AzServiceFabricManagedNodeTypeVMSecret'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-263">'Add-AzServiceFabricManagedNodeTypeVMSecret'</span></span>
    - <span data-ttu-id="1d1eb-264">'Remove-AzServiceFabricManagedNodeTypeVMExtension'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-264">'Remove-AzServiceFabricManagedNodeTypeVMExtension'</span></span>
    - <span data-ttu-id="1d1eb-265">'Restart-AzServiceFabricManagedNodeTyp'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-265">'Restart-AzServiceFabricManagedNodeTyp'</span></span>
* <span data-ttu-id="1d1eb-266">Service Fabric SDK를 버전 1.2.0으로 업그레이드했으며, 현재 모델에서는 서비스 패브릭 리소스 제공자 api-version 2020-03-01을, 관리형 클러스터에서는 2020-01-01-preview를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-266">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2020-03-01 for the current model and 2020-01-01-preview for managed clusters.</span></span>

#### <a name="azsql"></a><span data-ttu-id="1d1eb-267">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="1d1eb-267">Az.Sql</span></span>
* <span data-ttu-id="1d1eb-268">BackupStorageRedundancy가 'New-AzSqlInstance' 및 'Get-AzSqlInstance'에 추가됨</span><span class="sxs-lookup"><span data-stu-id="1d1eb-268">Added BackupStorageRedundancy to 'New-AzSqlInstance' and 'Get-AzSqlInstance'</span></span>
* <span data-ttu-id="1d1eb-269">'Get-AzSqlServerActiveDirectoryOnlyAuthentication' cmdlet이 추가됨</span><span class="sxs-lookup"><span data-stu-id="1d1eb-269">Added cmdlet 'Get-AzSqlServerActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="1d1eb-270">'Enable-AzSqlServerActiveDirectoryOnlyAuthentication' cmdlet이 추가됨</span><span class="sxs-lookup"><span data-stu-id="1d1eb-270">Added cmdlet 'Enable-AzSqlServerActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="1d1eb-271">Force 매개 변수가 'New-AzSqlInstance'에 추가됨</span><span class="sxs-lookup"><span data-stu-id="1d1eb-271">Added Force parameter to 'New-AzSqlInstance'</span></span>
* <span data-ttu-id="1d1eb-272">관리되는 데이터베이스 로그 재생 서비스용 cmdlet이 추가됨</span><span class="sxs-lookup"><span data-stu-id="1d1eb-272">Added cmdlets for Managed Database Log Replay service</span></span>
    - <span data-ttu-id="1d1eb-273">'Start-AzSqlInstanceDatabaseLogReplay'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-273">'Start-AzSqlInstanceDatabaseLogReplay'</span></span>
    - <span data-ttu-id="1d1eb-274">'Get-AzSqlInstanceDatabaseLogReplay'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-274">'Get-AzSqlInstanceDatabaseLogReplay'</span></span>
    - <span data-ttu-id="1d1eb-275">'Complete-AzSqlInstanceDatabaseLogReplay'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-275">'Complete-AzSqlInstanceDatabaseLogReplay'</span></span>
    - <span data-ttu-id="1d1eb-276">'Stop-AzSqlInstanceDatabaseLogReplay'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-276">'Stop-AzSqlInstanceDatabaseLogReplay'</span></span>
* <span data-ttu-id="1d1eb-277">'Get-AzSqlInstanceActiveDirectoryOnlyAuthentication' cmdlet이 추가됨</span><span class="sxs-lookup"><span data-stu-id="1d1eb-277">Added cmdlet 'Get-AzSqlInstanceActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="1d1eb-278">'Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication' cmdlet이 추가됨</span><span class="sxs-lookup"><span data-stu-id="1d1eb-278">Added cmdlet 'Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="1d1eb-279">'Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication' cmdlet이 추가됨</span><span class="sxs-lookup"><span data-stu-id="1d1eb-279">Added cmdlet 'Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="1d1eb-280">네트워크 격리 기능을 지원하기 위해 'New-AzSqlDatabaseImport' 및 'New-AzSqlDatabaseExport' cmdlet이 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="1d1eb-280">Updated cmdlets 'New-AzSqlDatabaseImport' and 'New-AzSqlDatabaseExport' to support network isolation functionality</span></span>
* <span data-ttu-id="1d1eb-281">'New-AzSqlDatabaseImportExisting' cmdlet이 추가됨</span><span class="sxs-lookup"><span data-stu-id="1d1eb-281">Added cmdlet 'New-AzSqlDatabaseImportExisting'</span></span>
* <span data-ttu-id="1d1eb-282">백업 스토리지 유형 사양을 지원하도록 데이터베이스 cmdlet이 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="1d1eb-282">Updated Databases cmdlets to support backup storage type specification</span></span>
* <span data-ttu-id="1d1eb-283">Force 매개 변수가 'New-AzSqlDatabase'에 추가됨</span><span class="sxs-lookup"><span data-stu-id="1d1eb-283">Added Force parameter to 'New-AzSqlDatabase'</span></span>
* <span data-ttu-id="1d1eb-284">'New-AzSqlDatabase'의 영역 선택에서 BackupStorageRedundancy 구성에 대한 경고가 추가됨</span><span class="sxs-lookup"><span data-stu-id="1d1eb-284">Added warning for BackupStorageRedundancy configuration in select regions in 'New-AzSqlDatabase'</span></span>
* <span data-ttu-id="1d1eb-285">ResourceId 및 InputObject를 포함하도록 서버 및 인스턴스에 대한 ActiveDirectoryOnlyAuthentication cmdlet이 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="1d1eb-285">Updated ActiveDirectoryOnlyAuthentication cmdlets for server and instance to include ResourceId and InputObject</span></span>

#### <a name="azstorage"></a><span data-ttu-id="1d1eb-286">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="1d1eb-286">Az.Storage</span></span>
* <span data-ttu-id="1d1eb-287">Microsoft.Azure.Storage.DataMovement 2.0.0로 업그레이드하여 blob 업로드 실패 수정됨 [#12220]</span><span class="sxs-lookup"><span data-stu-id="1d1eb-287">Fixed upload blob fail by upgrade to Microsoft.Azure.Storage.DataMovement 2.0.0 [#12220]</span></span>
* <span data-ttu-id="1d1eb-288">지정 시간 복원 지원</span><span class="sxs-lookup"><span data-stu-id="1d1eb-288">Supported Point In Time Restore</span></span>
    - <span data-ttu-id="1d1eb-289">'Enable-AzStorageBlobRestorePolicy'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-289">'Enable-AzStorageBlobRestorePolicy'</span></span>
    - <span data-ttu-id="1d1eb-290">'Disable-AzStorageBlobRestorePolicy'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-290">'Disable-AzStorageBlobRestorePolicy'</span></span>
    - <span data-ttu-id="1d1eb-291">'New-AzStorageBlobRangeToRestore'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-291">'New-AzStorageBlobRangeToRestore'</span></span>
    - <span data-ttu-id="1d1eb-292">'Restore-AzStorageBlobRange'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-292">'Restore-AzStorageBlobRange'</span></span>
* <span data-ttu-id="1d1eb-293">-IncludeBlobRestoreStatus 매개 변수와 함께 get-AzureRMStorageAccount를 실행하여 스토리지 계정의 blob 복원 상태 가져오기 지원</span><span class="sxs-lookup"><span data-stu-id="1d1eb-293">Supported get blob restore status of Storage account by run get-AzureRMStorageAccount with parameter -IncludeBlobRestoreStatus</span></span> 
    - <span data-ttu-id="1d1eb-294">'Get-AzureRMStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-294">'Get-AzureRMStorageAccount'</span></span>
* <span data-ttu-id="1d1eb-295">예정된 cmdlet 출력 변경에 대해 호환성이 손상되는 변경 경고 메시지가 추가됨</span><span class="sxs-lookup"><span data-stu-id="1d1eb-295">Added breaking change warning message for upcoming cmdlet output change</span></span>
    - <span data-ttu-id="1d1eb-296">'Get-AzStorageContainerStoredAccessPolicy'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-296">'Get-AzStorageContainerStoredAccessPolicy'</span></span>
    - <span data-ttu-id="1d1eb-297">'Set-AzStorageContainerStoredAccessPolicy'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-297">'Set-AzStorageContainerStoredAccessPolicy'</span></span>
    - <span data-ttu-id="1d1eb-298">'Set-AzStorageAccountManagementPolicy'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-298">'Set-AzStorageAccountManagementPolicy'</span></span>
    - <span data-ttu-id="1d1eb-299">'Get-AzStorageAccountManagementPolicy'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-299">'Get-AzStorageAccountManagementPolicy'</span></span>
    - <span data-ttu-id="1d1eb-300">'Add-AzStorageAccountManagementPolicyAction'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-300">'Add-AzStorageAccountManagementPolicyAction'</span></span>
    - <span data-ttu-id="1d1eb-301">'New-AzStorageAccountManagementPolicyRule'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-301">'New-AzStorageAccountManagementPolicyRule'</span></span>
* <span data-ttu-id="1d1eb-302">Microsoft.Azure.Cosmos.Table SDK를 1.0.8로 업그레이드</span><span class="sxs-lookup"><span data-stu-id="1d1eb-302">Upgraded Microsoft.Azure.Cosmos.Table SDK to 1.0.8</span></span>

### <a name="thanks-to-our-community-contributors"></a><span data-ttu-id="1d1eb-303">커뮤니티 기여자에게 감사드립니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-303">Thanks to our community contributors</span></span>
* <span data-ttu-id="1d1eb-304">Thomas Van Laere(@ThomVanL), Dockerfile-alpine-3.10 추가(#12911)</span><span class="sxs-lookup"><span data-stu-id="1d1eb-304">Thomas Van Laere (@ThomVanL), Add Dockerfile-alpine-3.10 (#12911)</span></span> 
* <span data-ttu-id="1d1eb-305">Lohith Chowdary Chilukuri(@Lochiluk), Remove-AzNetworkInterfaceIpConfig.md 업데이트(#12807)</span><span class="sxs-lookup"><span data-stu-id="1d1eb-305">Lohith Chowdary Chilukuri (@Lochiluk), Update Remove-AzNetworkInterfaceIpConfig.md (#12807)</span></span> 
* <span data-ttu-id="1d1eb-306">Roberth Strand(@roberthstrand), Get-AzResourceGroup - 새로운 예제 및 정리(#12828)</span><span class="sxs-lookup"><span data-stu-id="1d1eb-306">Roberth Strand (@roberthstrand), Get-AzResourceGroup - New example, and cleanup (#12828)</span></span> 
* <span data-ttu-id="1d1eb-307">Ravi Mishra(@inmishrar), Azure 웹앱 런타임 스택을 DOTNETCORE로 업데이트(#12833)</span><span class="sxs-lookup"><span data-stu-id="1d1eb-307">Ravi Mishra (@inmishrar), update Azure Web App runtime stack to DOTNETCORE (#12833)</span></span> 
* <span data-ttu-id="1d1eb-308">@jack-education, NSG 및 라우팅 테이블을 서브넷에서 제거할 수 있도록 Set-AzVirtualNetworkSubnetConfig를 업데이트(# 12351)</span><span class="sxs-lookup"><span data-stu-id="1d1eb-308">@jack-education, Updated Set-AzVirtualNetworkSubnetConfig to allow NSG and Route Table to be removed from subnet (#12351)</span></span> 
* <span data-ttu-id="1d1eb-309">@hagop-globanet, Add-AzApplicationGatewayCustomError.md 업데이트(#12784)</span><span class="sxs-lookup"><span data-stu-id="1d1eb-309">@hagop-globanet, Update Add-AzApplicationGatewayCustomError.md (#12784)</span></span> 
* <span data-ttu-id="1d1eb-310">Joshua Van Daalen(@greenSacrifice)</span><span class="sxs-lookup"><span data-stu-id="1d1eb-310">Joshua Van Daalen (@greenSacrifice)</span></span>
  * <span data-ttu-id="1d1eb-311">속성(Property) 철자를 속성(Property)으로 업데이트(#12821)</span><span class="sxs-lookup"><span data-stu-id="1d1eb-311">Update spelling of Property to Property (#12821)</span></span> 
  * <span data-ttu-id="1d1eb-312">New-AzResourceLock.md 예제 업데이트(#12806)</span><span class="sxs-lookup"><span data-stu-id="1d1eb-312">Update New-AzResourceLock.md examples (#12806)</span></span>
* <span data-ttu-id="1d1eb-313">Eragon Riddle(@eragonriddle), 예제에서 매개 변수 필드 이름 수정(#12825)</span><span class="sxs-lookup"><span data-stu-id="1d1eb-313">Eragon Riddle (@eragonriddle), Corrected parameter field name in the example (#12825)</span></span> 
* <span data-ttu-id="1d1eb-314">@rossifumax, New-AzConfigurationAssignment.md의 오타 수정(#12701)</span><span class="sxs-lookup"><span data-stu-id="1d1eb-314">@rossifumax, Fix typo in New-AzConfigurationAssignment.md (#12701)</span></span>

## <a name="461---august-2020"></a><span data-ttu-id="1d1eb-315">4.6.1 - 2020년 8월</span><span class="sxs-lookup"><span data-stu-id="1d1eb-315">4.6.1 - August 2020</span></span>
#### <a name="azcompute"></a><span data-ttu-id="1d1eb-316">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="1d1eb-316">Az.Compute</span></span>
* <span data-ttu-id="1d1eb-317">'New-AzVm'에서 '-EncryptionAtHost' 매개 변수를 패치하여 기본값인 false가 제거됨[#12776]</span><span class="sxs-lookup"><span data-stu-id="1d1eb-317">Patched '-EncryptionAtHost' parameter in 'New-AzVm' to remove default value of false [#12776]</span></span>

## <a name="460---august-2020"></a><span data-ttu-id="1d1eb-318">4.6.0 - 2020년 8월</span><span class="sxs-lookup"><span data-stu-id="1d1eb-318">4.6.0 - August 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="1d1eb-319">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="1d1eb-319">Az.Accounts</span></span>
* <span data-ttu-id="1d1eb-320">검색 엔드포인트가 기본 AzureCloud나 기타 공용 환경을 반환하지 않는 경우 모든 퍼블릭 클라우드 환경이 로드됨 [#12633]</span><span class="sxs-lookup"><span data-stu-id="1d1eb-320">Loaded all public cloud environments when discovery endpoint doesn't return default AzureCloud or other public environments [#12633]</span></span>
* <span data-ttu-id="1d1eb-321">'Get-AzSubscription'에서 SubscriptionPolicies가 노출됨 [#12551]</span><span class="sxs-lookup"><span data-stu-id="1d1eb-321">Exposed SubscriptionPolicies in 'Get-AzSubscription' [#12551]</span></span>

#### <a name="azautomation"></a><span data-ttu-id="1d1eb-322">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="1d1eb-322">Az.Automation</span></span>
* <span data-ttu-id="1d1eb-323">Hybrid Worker 그룹을 지정하기 위해 'Set-AzAutomationWebhook'에 '-RunOn' 매개 변수가 추가됨</span><span class="sxs-lookup"><span data-stu-id="1d1eb-323">Added '-RunOn' parameters to 'Set-AzAutomationWebhook' to specify a Hybrid Worker Group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="1d1eb-324">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="1d1eb-324">Az.Compute</span></span>
* <span data-ttu-id="1d1eb-325">'New-AzVm', 'New-AzVmss', 'New-AzVMConfig', 'New-AzVmssConfig', 'Update-AzVM', 'Update-AzVmss'에 '-EncryptionAtHost' 매개 변수가 추가됨</span><span class="sxs-lookup"><span data-stu-id="1d1eb-325">Added '-EncryptionAtHost' parameter to 'New-AzVm', 'New-AzVmss', 'New-AzVMConfig', 'New-AzVmssConfig', 'Update-AzVM', and 'Update-AzVmss'</span></span>
* <span data-ttu-id="1d1eb-326">'Get-AzVM' 및 'Get-AzVmss' 반환 개체에 'SecurityProfile'이 추가됨</span><span class="sxs-lookup"><span data-stu-id="1d1eb-326">Added 'SecurityProfile' to 'Get-AzVM' and 'Get-AzVmss' return object</span></span>
* <span data-ttu-id="1d1eb-327">'-InstanceView' 스위치가 'Get-AzHostGroup'에 선택적 매개 변수로 추가됨</span><span class="sxs-lookup"><span data-stu-id="1d1eb-327">Added '-InstanceView' switch as optional parameter to 'Get-AzHostGroup'</span></span>
* <span data-ttu-id="1d1eb-328">새 cmdlet 'Invoke-AzVmPatchAssessment'가 추가됨</span><span class="sxs-lookup"><span data-stu-id="1d1eb-328">Added new cmdlet 'Invoke-AzVmPatchAssessment'</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="1d1eb-329">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="1d1eb-329">Az.DataFactory</span></span>
* <span data-ttu-id="1d1eb-330">PSPipelineRun 클래스에 누락된 속성이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-330">Added missing properties to PSPipelineRun class.</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="1d1eb-331">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="1d1eb-331">Az.HDInsight</span></span>
* <span data-ttu-id="1d1eb-332">호스트 기능에서 암호화를 사용하여 클러스터를 만드는 것이 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-332">Supported creating cluster with encryption at host feature.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="1d1eb-333">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="1d1eb-333">Az.KeyVault</span></span>
* <span data-ttu-id="1d1eb-334">일시 삭제 사용 안 함 계획에 대한 경고 메시지가 추가됨</span><span class="sxs-lookup"><span data-stu-id="1d1eb-334">Added warning messages for planning to disable soft delete</span></span>
* <span data-ttu-id="1d1eb-335">특성 SecretValueText 제거 계획에 대한 경고 메시지가 추가됨</span><span class="sxs-lookup"><span data-stu-id="1d1eb-335">Added warning messages for planning to remove attribute SecretValueText</span></span>

#### <a name="azmaintenance"></a><span data-ttu-id="1d1eb-336">Az.Maintenance</span><span class="sxs-lookup"><span data-stu-id="1d1eb-336">Az.Maintenance</span></span>
* <span data-ttu-id="1d1eb-337">'New-AzMaintenanceConfiguration'에 선택적 일정 관련 필드가 추가됨</span><span class="sxs-lookup"><span data-stu-id="1d1eb-337">Added optional schedule related fields to 'New-AzMaintenanceConfiguration'</span></span>
* <span data-ttu-id="1d1eb-338">'Get-AzMaintenancePublicConfiguration'에 대한 새 cmdlet이 추가됨</span><span class="sxs-lookup"><span data-stu-id="1d1eb-338">Added new cmdlet for 'Get-AzMaintenancePublicConfiguration'</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="1d1eb-339">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="1d1eb-339">Az.ManagedServices</span></span>
* <span data-ttu-id="1d1eb-340">관리되는 서비스 할당 및 정의의 cmdlet에 대한 호환성이 손상되는 변경 경고가 추가됨</span><span class="sxs-lookup"><span data-stu-id="1d1eb-340">Added breaking change warnings on cmdlets of managed services assignment and definition</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="1d1eb-341">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="1d1eb-341">Az.Monitor</span></span>
* <span data-ttu-id="1d1eb-342">로그 및 메트릭 사용을 분리하기 위해 'Set-AzDiagnosticSetting'에 설정된 매개 변수가 확장됨 [#12482]</span><span class="sxs-lookup"><span data-stu-id="1d1eb-342">Extended the parameter set in 'Set-AzDiagnosticSetting' for separation of Logs and Metrics enablement [#12482]</span></span>
* <span data-ttu-id="1d1eb-343">파이프라인에서 메트릭 경고를 가져오는 경우 'Add-AzMetricAlertRuleV2'에 대한 버그가 수정됨</span><span class="sxs-lookup"><span data-stu-id="1d1eb-343">Fixed bug for 'Add-AzMetricAlertRuleV2' when getting metric alert from pipeline</span></span>

#### <a name="azresources"></a><span data-ttu-id="1d1eb-344">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="1d1eb-344">Az.Resources</span></span>
* <span data-ttu-id="1d1eb-345">Azure Policy를 통해 별칭을 수정할 수 있는지 여부를 나타내는 정보를 포함하도록 'Get-AzPolicyAlias' 응답이 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="1d1eb-345">Updated 'Get-AzPolicyAlias' response to include information indicating whether the alias is modifiable by Azure Policy.</span></span>
* <span data-ttu-id="1d1eb-346">새 cmdlet 'Set-AzRoleAssignment'가 생성됨</span><span class="sxs-lookup"><span data-stu-id="1d1eb-346">Created new cmdlet 'Set-AzRoleAssignment'</span></span>
* <span data-ttu-id="1d1eb-347">관리 그룹 범위에서 ARM 템플릿 What-If 결과를 가져오는 'Get-AzDeploymentManagementGroupWhatIfResult'가 추가됨</span><span class="sxs-lookup"><span data-stu-id="1d1eb-347">Added 'Get-AzDeploymentManagementGroupWhatIfResult' for getting ARM template What-If results at management Group scope</span></span>
* <span data-ttu-id="1d1eb-348">테넌트 범위에서 ARM 템플릿 What-If 결과를 가져오는 'Get-AzTenantWhatIfResult' 새 cmdlet이 추가됨</span><span class="sxs-lookup"><span data-stu-id="1d1eb-348">Added 'Get-AzTenantWhatIfResult' new cmdlet for getting ARM template What-If results at tenant scope</span></span>
* <span data-ttu-id="1d1eb-349">ARM 템플릿 What-If 결과를 사용하도록 'New-AzManagementGroupDeployment' 및 'New-AzTenantDeployment'에 대한 '-WhatIf' 및 '-Confirm'이 재정의됨</span><span class="sxs-lookup"><span data-stu-id="1d1eb-349">Overrode '-WhatIf' and '-Confirm' for 'New-AzManagementGroupDeployment' and 'New-AzTenantDeployment' to use ARM template What-If results</span></span>
* <span data-ttu-id="1d1eb-350">새 배포 cmdlet에 대한 '-WhatIf' 및 '-Confirm' 동작이 False를 준수하도록 수정됨</span><span class="sxs-lookup"><span data-stu-id="1d1eb-350">Fixed the behaviors of '-WhatIf' and '-Confirm' for new deployment cmdlets so they comply with False and</span></span> 
* <span data-ttu-id="1d1eb-351">'-TemplateObject' 및 'TemplateParameterObject'에 대한 직렬화 오류가 수정됨 [#1528] [#6292]</span><span class="sxs-lookup"><span data-stu-id="1d1eb-351">Fixed serialization error for '-TemplateObject' and 'TemplateParameterObject' [#1528] [#6292]</span></span>
* <span data-ttu-id="1d1eb-352">예정된 출력 형식 변경을 위해 'Get-AzResourceGroupDeploymentOperation'에 호환성이 손상되는 변경 특성이 추가됨</span><span class="sxs-lookup"><span data-stu-id="1d1eb-352">Added breaking change attribute to 'Get-AzResourceGroupDeploymentOperation' for the upcoming output type change</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="1d1eb-353">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="1d1eb-353">Az.SignalR</span></span>
* <span data-ttu-id="1d1eb-354">'Restart-AzSignalR' 및 'Update-AzSignalR' 도움말 파일 오류가 수정됨</span><span class="sxs-lookup"><span data-stu-id="1d1eb-354">Fixed 'Restart-AzSignalR' and 'Update-AzSignalR' help files errors</span></span>
* <span data-ttu-id="1d1eb-355">'Update-AzSignalRNetworkAcl', 'Set-AzSignalRUpstream' cmdlet이 추가됨</span><span class="sxs-lookup"><span data-stu-id="1d1eb-355">Added cmdlets 'Update-AzSignalRNetworkAcl', 'Set-AzSignalRUpstream'</span></span>

#### <a name="azstorage"></a><span data-ttu-id="1d1eb-356">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="1d1eb-356">Az.Storage</span></span>
* <span data-ttu-id="1d1eb-357">지원되는 Blob 쿼리 가속</span><span class="sxs-lookup"><span data-stu-id="1d1eb-357">Supported blob query acceleration</span></span>
    -  <span data-ttu-id="1d1eb-358">'Get-AzStorageBlobQueryResult'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-358">'Get-AzStorageBlobQueryResult'</span></span>
    -  <span data-ttu-id="1d1eb-359">'New-AzStorageBlobQueryConfig'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-359">'New-AzStorageBlobQueryConfig'</span></span>
* <span data-ttu-id="1d1eb-360">도움말 파일 업데이트, 자세한 설명 추가 및 오타 수정</span><span class="sxs-lookup"><span data-stu-id="1d1eb-360">Updated help file, added more description, and fixed typo</span></span>
    -  <span data-ttu-id="1d1eb-361">'Start-AzStorageBlobCopy'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-361">'Start-AzStorageBlobCopy'</span></span>
    -  <span data-ttu-id="1d1eb-362">'Get-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-362">'Get-AzDataLakeGen2Item'</span></span>
* <span data-ttu-id="1d1eb-363">관련 하위 디렉터리가 없는 경우 Blob 다운로드 실패가 수정됨 [#12592]</span><span class="sxs-lookup"><span data-stu-id="1d1eb-363">Fixed download blob fail when related sub directory not exist [#12592]</span></span>
    -  <span data-ttu-id="1d1eb-364">'Get-AzStorageBlobContent'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-364">'Get-AzStorageBlobContent'</span></span>
* <span data-ttu-id="1d1eb-365">스토리지 계정에 대해 개체 복제 정책 설정/가져오기/제거가 지원됨</span><span class="sxs-lookup"><span data-stu-id="1d1eb-365">Supported Set/Get/Remove Object Replication Policy on Storage accounts</span></span>
    - <span data-ttu-id="1d1eb-366">'New-AzStorageObjectReplicationPolicyRule'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-366">'New-AzStorageObjectReplicationPolicyRule'</span></span>
    - <span data-ttu-id="1d1eb-367">'Set-AzStorageObjectReplicationPolicy'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-367">'Set-AzStorageObjectReplicationPolicy'</span></span>
    - <span data-ttu-id="1d1eb-368">'Get-AzStorageObjectReplicationPolicy'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-368">'Get-AzStorageObjectReplicationPolicy'</span></span>
    - <span data-ttu-id="1d1eb-369">'Remove-AzStorageObjectReplicationPolicy'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-369">'Remove-AzStorageObjectReplicationPolicy'</span></span>
* <span data-ttu-id="1d1eb-370">스토리지 계정의 Blob Service에서 ChangeFeed 사용/사용 안 함이 지원됨</span><span class="sxs-lookup"><span data-stu-id="1d1eb-370">Supported enable/disable ChangeFeed on Blob Service of a Storage account</span></span>
    - <span data-ttu-id="1d1eb-371">'Update-AzStorageBlobServiceProperty'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-371">'Update-AzStorageBlobServiceProperty'</span></span>

## <a name="450---august-2020"></a><span data-ttu-id="1d1eb-372">4.5.0 - 2020년 8월</span><span class="sxs-lookup"><span data-stu-id="1d1eb-372">4.5.0 - August 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="1d1eb-373">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="1d1eb-373">Az.Accounts</span></span>
* <span data-ttu-id="1d1eb-374">매개 변수 'MaxContextPopulation'을 허용하도록 'Connect-AzAccount' 업데이트됨 [# 9865]</span><span class="sxs-lookup"><span data-stu-id="1d1eb-374">Updated 'Connect-AzAccount' to accept parameter 'MaxContextPopulation' [#9865]</span></span>
* <span data-ttu-id="1d1eb-375">SubscriptionClient 버전이 2019-06-01로 업데이트되고 테넌트 도메인을 표시 [#9838]</span><span class="sxs-lookup"><span data-stu-id="1d1eb-375">Updated SubscriptionClient version to 2019-06-01 and display tenant domains [#9838]</span></span>
* <span data-ttu-id="1d1eb-376">구독의 managedBy 테넌트 정보 및 홈 테넌트 지원</span><span class="sxs-lookup"><span data-stu-id="1d1eb-376">Supported home tenant and managedBy tenant information of subscription</span></span>
* <span data-ttu-id="1d1eb-377">원격 분석 데이터의 모듈 이름, 버전 정보 수정</span><span class="sxs-lookup"><span data-stu-id="1d1eb-377">Corrected module name, version info in telemetry data</span></span>
* <span data-ttu-id="1d1eb-378">환경 메타데이터 엔드포인트가 호환되지 않는 값을 반환하는 경우 SqlDatabaseDnsSuffix 및 ServiceManagementUrl이 조정됨</span><span class="sxs-lookup"><span data-stu-id="1d1eb-378">Adjusted SqlDatabaseDnsSuffix and ServiceManagementUrl if environment metadata endpoint returns incompatible value</span></span>

#### <a name="azaks"></a><span data-ttu-id="1d1eb-379">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="1d1eb-379">Az.Aks</span></span>
* <span data-ttu-id="1d1eb-380">'ClientIdAndSecret'을 'ServicePrincipalIdAndSecret'으로 제거하고 'ClientIdAndSecret'을 별칭으로 설정함 [#12381]</span><span class="sxs-lookup"><span data-stu-id="1d1eb-380">Removed 'ClientIdAndSecret' to 'ServicePrincipalIdAndSecret' and set 'ClientIdAndSecret' as an alias [#12381].</span></span>
* <span data-ttu-id="1d1eb-381">'Get-AzAks'/'New-AzAks'/'Remove-AzAks'/'Set-AzAks'를 'Get-AzAksCluster'/'New-AzAksCluster'/'Remove-AzAksCluster'/'Set-AzAksCluster'로 제거하고 원본을 별칭으로 설정함 [#12373].</span><span class="sxs-lookup"><span data-stu-id="1d1eb-381">Removed 'Get-AzAks'/'New-AzAks'/'Remove-AzAks'/'Set-AzAks' to 'Get-AzAksCluster'/'New-AzAksCluster'/'Remove-AzAksCluster'/'Set-AzAksCluster' and set the original ones as alias [#12373].</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="1d1eb-382">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="1d1eb-382">Az.ApiManagement</span></span>
* <span data-ttu-id="1d1eb-383">새 'Add-AzApiManagementApiToGateway' cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-383">Added new 'Add-AzApiManagementApiToGateway' cmdlet.</span></span>
* <span data-ttu-id="1d1eb-384">새 'Get-AzApiManagementGateway' cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-384">Added new 'Get-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="1d1eb-385">새 'Get-AzApiManagementGatewayHostnameConfiguration' cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-385">Added new 'Get-AzApiManagementGatewayHostnameConfiguration' cmdlet.</span></span>
* <span data-ttu-id="1d1eb-386">새 'Get-AzApiManagementGatewayKey' cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-386">Added new 'Get-AzApiManagementGatewayKey' cmdlet.</span></span>
* <span data-ttu-id="1d1eb-387">새 'New-AzApiManagementGateway' cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-387">Added new 'New-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="1d1eb-388">새 'New-AzApiManagementGatewayHostnameConfiguration' cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-388">Added new 'New-AzApiManagementGatewayHostnameConfiguration' cmdlet.</span></span>
* <span data-ttu-id="1d1eb-389">새 'New-AzApiManagementResourceLocationObject' cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-389">Added new 'New-AzApiManagementResourceLocationObject' cmdlet.</span></span>
* <span data-ttu-id="1d1eb-390">새 'Remove-AzApiManagementApiFromGateway' cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-390">Added new 'Remove-AzApiManagementApiFromGateway' cmdlet.</span></span>
* <span data-ttu-id="1d1eb-391">새 'Remove-AzApiManagementGateway' cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-391">Added new 'Remove-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="1d1eb-392">새 'Remove-AzApiManagementGatewayHostnameConfiguration' cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-392">Added new 'Remove-AzApiManagementGatewayHostnameConfiguration' cmdlet.</span></span>
* <span data-ttu-id="1d1eb-393">새 'Update-AzApiManagementGateway' cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-393">Added new 'Update-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="1d1eb-394">'Get-AzApiManagementApi' cmdlet에 선택적 [-GatewayId] 매개 변수가 새로 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-394">Added new optional [-GatewayId] parameter to the 'Get-AzApiManagementApi' cmdlet.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="1d1eb-395">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="1d1eb-395">Az.CognitiveServices</span></span>
* <span data-ttu-id="1d1eb-396">'Deny'가 특히 NetworkRules 기본 작업으로 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-396">Used 'Deny' specifically as NetworkRules default action.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="1d1eb-397">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="1d1eb-397">Az.FrontDoor</span></span>
* <span data-ttu-id="1d1eb-398">Enum.Parse가 null 값을 Enabled 또는 Disabled 열거형 값으로 강제 변환하려는 경우 예외가 throw되는 문제를 수정했습니다. [#12344]</span><span class="sxs-lookup"><span data-stu-id="1d1eb-398">Fixed an issue where an exception is being thrown when Enum.Parse tries to coerce a null value to an Enabled or Disabled enum values [#12344]</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="1d1eb-399">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="1d1eb-399">Az.HDInsight</span></span>
* <span data-ttu-id="1d1eb-400">전송 중 암호화 기능을 사용하여 클러스터를 만드는 것이 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-400">Supported creating cluster with encryption in transit feature.</span></span>
    - <span data-ttu-id="1d1eb-401">cmdlet 'New-AzHDInsightCluster'에 새 매개 변수 'EncryptionInTransit' 추가</span><span class="sxs-lookup"><span data-stu-id="1d1eb-401">Add new parameter 'EncryptionInTransit' to the cmdlet 'New-AzHDInsightCluster'</span></span>
    - <span data-ttu-id="1d1eb-402">cmdlet 'New-AzHDInsightClusterConfig'에 새 매개 변수 'EncryptionInTransit' 추가</span><span class="sxs-lookup"><span data-stu-id="1d1eb-402">Add new parameter 'EncryptionInTransit' to the cmdlet 'New-AzHDInsightClusterConfig'</span></span>
* <span data-ttu-id="1d1eb-403">프라이빗 링크 기능을 사용하여 클러스터를 만드는 것이 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-403">Supported creating cluster with private link feature:</span></span>
    - <span data-ttu-id="1d1eb-404">cmdlet 'New-AzHDInsightCluster'에 새 매개 변수 'PublicNetworkAccessType' 및 'OutboundPublicNetworkAccessType' 추가</span><span class="sxs-lookup"><span data-stu-id="1d1eb-404">Add new parameter 'PublicNetworkAccessType' and 'OutboundPublicNetworkAccessType' to the cmdlet 'New-AzHDInsightCluster'</span></span>
    - <span data-ttu-id="1d1eb-405">cmdlet 'New-AzHDInsightClusterConfig'에 새 매개 변수 'PublicNetworkAccessType' 및 'OutboundPublicNetworkAccessType' 추가</span><span class="sxs-lookup"><span data-stu-id="1d1eb-405">Add new parameter 'PublicNetworkAccessType' and 'OutboundPublicNetworkAccessType' to the cmdlet 'New-AzHDInsightClusterConfig'</span></span>
* <span data-ttu-id="1d1eb-406">'New-AzHDInsightCluster' 또는 'Get-AzHDInsightCluster'를 호출하는 경우 가상 네트워크 정보가 반환됨</span><span class="sxs-lookup"><span data-stu-id="1d1eb-406">Returned virtual network information when calling 'New-AzHDInsightCluster' or 'Get-AzHDInsightCluster'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="1d1eb-407">Az.Network</span><span class="sxs-lookup"><span data-stu-id="1d1eb-407">Az.Network</span></span>
* <span data-ttu-id="1d1eb-408">'Remove-AzExpressRouteCircuitConnectionConfig'에 AddressPrefixType 매개 변수 지원 추가</span><span class="sxs-lookup"><span data-stu-id="1d1eb-408">Added support for AddressPrefixType parameter to 'Remove-AzExpressRouteCircuitConnectionConfig'</span></span>
* <span data-ttu-id="1d1eb-409">작업을 중단하지 않는 변경이 추가됨: 'Remove-AzExpressRouteCircutPeeringConfig'의 프라이빗 피어링을 위한 PeerAddressType 기능</span><span class="sxs-lookup"><span data-stu-id="1d1eb-409">Added non-breaking changes: PeerAddressType functionality for Private Peering in 'Remove-AzExpressRouteCircutPeeringConfig'.</span></span>
* <span data-ttu-id="1d1eb-410">AddressPrefixType 및 PeerAddressType 매개 변수의 대/소문자를 무시하도록 코드가 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-410">Code changed to ignore case for AddressPrefixType and PeerAddressType parameter.</span></span>
* <span data-ttu-id="1d1eb-411">'New-AzLoadBalancerFrontendIpConfig', 'New-AzPublicIpAddress' 및 'New-AzPublicIpPrefix'에 대한 경고 메시지를 수정했습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-411">Modified the warning message for 'New-AzLoadBalancerFrontendIpConfig', 'New-AzPublicIpAddress' and 'New-AzPublicIpPrefix'.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="1d1eb-412">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="1d1eb-412">Az.OperationalInsights</span></span>
* <span data-ttu-id="1d1eb-413">'Remove-AzOperationalInsightsworkspace'에 대한 '-ForceDelete' 옵션이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-413">Added '-ForceDelete' option for 'Remove-AzOperationalInsightsworkspace'</span></span>
* <span data-ttu-id="1d1eb-414">새 cmdlet 'Get-AzOperationalInsightsDeletedWorkspace'가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-414">Added new cmdlet 'Get-AzOperationalInsightsDeletedWorkspace'</span></span>
* <span data-ttu-id="1d1eb-415">새 cmdlet 'Restore-AzOperationalInsightsWorkspace'가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-415">Added new cmdlet 'Restore-AzOperationalInsightsWorkspace'</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="1d1eb-416">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="1d1eb-416">Az.RecoveryServices</span></span>
* <span data-ttu-id="1d1eb-417">Azure Backup 컨테이너/항목 검색 환경이 개선되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-417">Improved the Azure Backup container/item discovery experience.</span></span>

#### <a name="azresources"></a><span data-ttu-id="1d1eb-418">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="1d1eb-418">Az.Resources</span></span>
* <span data-ttu-id="1d1eb-419">'New-AzRoleAssignment'에 'Condition', 'ConditionVersion' 및 'Description' 속성을 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-419">Added properties 'Condition', 'ConditionVersion' and 'Description' to 'New-AzRoleAssignment'</span></span>
    - <span data-ttu-id="1d1eb-420">여기에는 데이터 모델과 관련된 모든 변경 사항이 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-420">This included all the relevant changes to the data models</span></span>

#### <a name="azsql"></a><span data-ttu-id="1d1eb-421">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="1d1eb-421">Az.Sql</span></span>
* <span data-ttu-id="1d1eb-422">'New-AzSqlServer' 'Set-AzSqlServer'에서 서버 이름 대/소문자를 구분하지 않는 잠재적인 오류를 수정했습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-422">Fixed potential server name case insensitive error in 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>
* <span data-ttu-id="1d1eb-423">'New-AzSqlDatabaseSecondary'의 기존 데이터베이스 오류에서 반환되는 잘못된 데이터베이스 이름을 수정했습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-423">Fixed wrong database name returned on existing database error in 'New-AzSqlDatabaseSecondary'</span></span>

#### <a name="azstorage"></a><span data-ttu-id="1d1eb-424">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="1d1eb-424">Az.Storage</span></span>
* <span data-ttu-id="1d1eb-425">새 권한 x,t를 사용하여 컨테이너/blob Sas 토큰 만들기 지원</span><span class="sxs-lookup"><span data-stu-id="1d1eb-425">Supported create container/blob Sas token with new permission x,t</span></span>
    -  <span data-ttu-id="1d1eb-426">'New-AzStorageBlobSASToken'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-426">'New-AzStorageBlobSASToken'</span></span>
    -  <span data-ttu-id="1d1eb-427">'New-AzStorageContainerSASToken'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-427">'New-AzStorageContainerSASToken'</span></span>
* <span data-ttu-id="1d1eb-428">새 권한 x,t,f를 사용하여 계정 Sas 토큰 만들기 지원</span><span class="sxs-lookup"><span data-stu-id="1d1eb-428">Supported create account Sas token with new permission x,t,f</span></span>
    -  <span data-ttu-id="1d1eb-429">'New-AzStorageAccountSASToken'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-429">'New-AzStorageAccountSASToken'</span></span>
* <span data-ttu-id="1d1eb-430">단일 파일 사용량 공유 가져오기 지원</span><span class="sxs-lookup"><span data-stu-id="1d1eb-430">Supported get single file share usage</span></span>
    - <span data-ttu-id="1d1eb-431">'Get-AzRmStorageShare'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-431">'Get-AzRmStorageShare'</span></span>

## <a name="440---july-2020"></a><span data-ttu-id="1d1eb-432">4.4.0 - 2020년 7월</span><span class="sxs-lookup"><span data-stu-id="1d1eb-432">4.4.0 - July 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="1d1eb-433">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="1d1eb-433">Az.Accounts</span></span>
* <span data-ttu-id="1d1eb-434">새 cmdlet 'Invoke-AzRestMethod' 추가</span><span class="sxs-lookup"><span data-stu-id="1d1eb-434">Added new cmdlet 'Invoke-AzRestMethod'</span></span>
* <span data-ttu-id="1d1eb-435">'Start-Job'을 사용하여 여러 Azure PowerShell cmdlet을 실행하는 등 다중 프로세스 시나리오에서 인증 오류를 발생시킬 수 있는 문제 해결 [#9448]</span><span class="sxs-lookup"><span data-stu-id="1d1eb-435">Fixed an issue that may cause authentication errors in multi-process scenarios such as running multiple Azure PowerShell cmdlets using 'Start-Job' [#9448]</span></span>

#### <a name="azaks"></a><span data-ttu-id="1d1eb-436">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="1d1eb-436">Az.Aks</span></span>
* <span data-ttu-id="1d1eb-437">'Get-AzAks'가 모든 클러스터를 가져오지 않는 버그 수정 [#12296]</span><span class="sxs-lookup"><span data-stu-id="1d1eb-437">Fixed bug 'Get-AzAks' doesn't get all clusters [#12296]</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="1d1eb-438">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="1d1eb-438">Az.AnalysisServices</span></span>
* <span data-ttu-id="1d1eb-439">인증에 대한 프로젝트 참조 제거</span><span class="sxs-lookup"><span data-stu-id="1d1eb-439">Removed project reference to Authentication</span></span>

#### <a name="azautomation"></a><span data-ttu-id="1d1eb-440">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="1d1eb-440">Az.Automation</span></span>
* <span data-ttu-id="1d1eb-441">이스케이프 문자를 포함하는 문자열을 json 개체로 변환할 수 없는 문제 해결</span><span class="sxs-lookup"><span data-stu-id="1d1eb-441">Fixed the issue that string with escape chars cannot be converted into json object.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="1d1eb-442">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="1d1eb-442">Az.Compute</span></span>
* <span data-ttu-id="1d1eb-443">'latest' 이미지 버전이 없는 'New-AzVmss'를 사용하는 경우 경고 추가</span><span class="sxs-lookup"><span data-stu-id="1d1eb-443">Added warning when using 'New-AzVmss' without 'latest' image version</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="1d1eb-444">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="1d1eb-444">Az.DataFactory</span></span>
* <span data-ttu-id="1d1eb-445">Data Factory에 대한 전역 매개 변수를 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-445">Added global parameters to Data Factory.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="1d1eb-446">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="1d1eb-446">Az.EventGrid</span></span>
* <span data-ttu-id="1d1eb-447">2020-06-01 API 버전을 사용하도록 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-447">Updated to use the 2020-06-01 API version.</span></span>
* <span data-ttu-id="1d1eb-448">추가된 새로운 기능:</span><span class="sxs-lookup"><span data-stu-id="1d1eb-448">Added new features:</span></span>
    - <span data-ttu-id="1d1eb-449">입력 매핑</span><span class="sxs-lookup"><span data-stu-id="1d1eb-449">Input mapping</span></span>
    - <span data-ttu-id="1d1eb-450">이벤트 배달 스키마</span><span class="sxs-lookup"><span data-stu-id="1d1eb-450">Event Delivery Schema</span></span>
    - <span data-ttu-id="1d1eb-451">Private Link</span><span class="sxs-lookup"><span data-stu-id="1d1eb-451">Private Link</span></span>
    - <span data-ttu-id="1d1eb-452">클라우드 이벤트 V10 스키마</span><span class="sxs-lookup"><span data-stu-id="1d1eb-452">Cloud Event V10 Schema</span></span>
    - <span data-ttu-id="1d1eb-453">대상으로 Service Bus 항목</span><span class="sxs-lookup"><span data-stu-id="1d1eb-453">Service Bus Topic As Destination</span></span>
    - <span data-ttu-id="1d1eb-454">대상으로 Azure 함수</span><span class="sxs-lookup"><span data-stu-id="1d1eb-454">Azure Function As Destination</span></span>
    - <span data-ttu-id="1d1eb-455">WebHook 일괄 처리</span><span class="sxs-lookup"><span data-stu-id="1d1eb-455">WebHook Batching</span></span>
    - <span data-ttu-id="1d1eb-456">보안 웹후크(AAD 지원)</span><span class="sxs-lookup"><span data-stu-id="1d1eb-456">Secure webhook (AAD support)</span></span>
    - <span data-ttu-id="1d1eb-457">IpFiltering</span><span class="sxs-lookup"><span data-stu-id="1d1eb-457">IpFiltering</span></span>
* <span data-ttu-id="1d1eb-458">다음 Cmdlet이 업데이트 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-458">Updated cmdlets:</span></span>
    - <span data-ttu-id="1d1eb-459">'New-AzEventGridSubscription'/'Update-AzEventGridSubscription':</span><span class="sxs-lookup"><span data-stu-id="1d1eb-459">'New-AzEventGridSubscription'/'Update-AzEventGridSubscription':</span></span>
        - <span data-ttu-id="1d1eb-460">웹후크 일괄 처리를 지원하기 위해 새로운 선택적 매개 변수를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-460">Add new optional parameters to support webhook batching.</span></span>
        - <span data-ttu-id="1d1eb-461">AAD를 사용하여 보안 웹후크를 지원하는 새로운 선택적 매개 변수를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-461">Add new optional parameters to support secured webhook using AAD.</span></span>
        - <span data-ttu-id="1d1eb-462">Azure 함수 및 Service Bus 항목을 새 대상으로 지원하기 위해 EndpointType 매개 변수에 대한 새 열거형을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-462">Add new enum for EndpointType parameter to support azure function and service bus topic as new destinations.</span></span>
        - <span data-ttu-id="1d1eb-463">배달 스키마에 대한 새로운 선택적 매개 변수를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-463">Add new optional parameter for delivery schema.</span></span>
    - <span data-ttu-id="1d1eb-464">'New-AzEventGridTopic'/'Update-AzEventGridTopic' 및 'New-AzEventGridDomain'/'Update-AzEventGridDomain':</span><span class="sxs-lookup"><span data-stu-id="1d1eb-464">'New-AzEventGridTopic'/'Update-AzEventGridTopic' and 'New-AzEventGridDomain'/'Update-AzEventGridDomain':</span></span>
        - <span data-ttu-id="1d1eb-465">IpFiltering을 지원하기 위해 새로운 선택적 매개 변수를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-465">Add new optional parameters to support IpFiltering.</span></span>
    - <span data-ttu-id="1d1eb-466">'New-AzEventGridTopic'/'New-AzEventGridDomain':</span><span class="sxs-lookup"><span data-stu-id="1d1eb-466">'New-AzEventGridTopic'/'New-AzEventGridDomain':</span></span>
        - <span data-ttu-id="1d1eb-467">입력 매핑을 지원하기 위해 새로운 선택적 매개 변수를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-467">Add new optional parameters to support Input mapping.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="1d1eb-468">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="1d1eb-468">Az.FrontDoor</span></span>
* <span data-ttu-id="1d1eb-469">API 2020-05-01을 사용하도록 업데이트된 모듈</span><span class="sxs-lookup"><span data-stu-id="1d1eb-469">Updated module to use API 2020-05-01</span></span>
* <span data-ttu-id="1d1eb-470">Storage, Keyvault 및 Web App Service 리소스에 대한 프라이빗 링크 지원을 추가함</span><span class="sxs-lookup"><span data-stu-id="1d1eb-470">Added Private link support for Storage, Keyvault and Web App Service resources</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="1d1eb-471">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="1d1eb-471">Az.HDInsight</span></span>
* <span data-ttu-id="1d1eb-472">국가 클라우드에서 ADLSGen1/2 스토리지로 클러스터를 만드는 것이 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-472">Supported creating cluster with ADLSGen1/2 storage in national clouds.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="1d1eb-473">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="1d1eb-473">Az.Monitor</span></span>
* <span data-ttu-id="1d1eb-474">메트릭 또는 로그가 null인 경우 'Get-AzDiagnosticSetting'에 대한 버그 수정 [#12272]</span><span class="sxs-lookup"><span data-stu-id="1d1eb-474">Fixed bug for 'Get-AzDiagnosticSetting' when metrics or logs are null [#12272]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="1d1eb-475">Az.Network</span><span class="sxs-lookup"><span data-stu-id="1d1eb-475">Az.Network</span></span>
* <span data-ttu-id="1d1eb-476">VWan HubVnet 연결의 매개 변수 교환 수정</span><span class="sxs-lookup"><span data-stu-id="1d1eb-476">Fixed parameters swap in VWan HubVnet connection</span></span>
* <span data-ttu-id="1d1eb-477">Azure Network Virtual Appliance 사이트에 대한 새 cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="1d1eb-477">Added new cmdlets for Azure Network Virtual Appliance Sites</span></span>
    - <span data-ttu-id="1d1eb-478">'Get-AzVirtualApplianceSite'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-478">'Get-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="1d1eb-479">'New-AzVirtualApplianceSite'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-479">'New-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="1d1eb-480">'Remove-AzVirtualApplianceSite'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-480">'Remove-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="1d1eb-481">'Update-AzVirtualApplianceSite'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-481">'Update-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="1d1eb-482">'New-AzOffice365PolicyProperty'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-482">'New-AzOffice365PolicyProperty'</span></span>
* <span data-ttu-id="1d1eb-483">Azure Network Virtual Appliance에 대한 새 cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="1d1eb-483">Added new cmdlets for Azure Network Virtual Appliance</span></span>
    - <span data-ttu-id="1d1eb-484">'Get-AzNetworkVirtualAppliance'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-484">'Get-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="1d1eb-485">'New-AzNetworkVirtualAppliance'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-485">'New-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="1d1eb-486">'Remove-AzNetworkVirtualAppliance'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-486">'Remove-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="1d1eb-487">'Update-AzNetworkVirtualAppliance'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-487">'Update-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="1d1eb-488">'Get-AzNetworkVirtualApplianceSku'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-488">'Get-AzNetworkVirtualApplianceSku'</span></span>
    - <span data-ttu-id="1d1eb-489">'New-AzVirtualApplianceSkuProperty'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-489">'New-AzVirtualApplianceSkuProperty'</span></span>
* <span data-ttu-id="1d1eb-490">Application Gateway를 Private Link 공통 cmdlet에 온보딩</span><span class="sxs-lookup"><span data-stu-id="1d1eb-490">Onboarded Application Gateway to Private Link Common Cmdlets</span></span>
* <span data-ttu-id="1d1eb-491">StorageSync를 Private Link 공통 cmdlet에 온보딩</span><span class="sxs-lookup"><span data-stu-id="1d1eb-491">Onboarded StorageSync to Private Link Common Cmdlets</span></span>
* <span data-ttu-id="1d1eb-492">SignalR을 Private Link 공통 cmdlet에 온보딩</span><span class="sxs-lookup"><span data-stu-id="1d1eb-492">Onboarded SignalR to Private Link Common Cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="1d1eb-493">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="1d1eb-493">Az.RecoveryServices</span></span>
* <span data-ttu-id="1d1eb-494">인증에 대한 프로젝트 참조 제거</span><span class="sxs-lookup"><span data-stu-id="1d1eb-494">Removed project reference to Authentication</span></span>
* <span data-ttu-id="1d1eb-495">Azure Backup 튜닝 cmdlet은 텍스트를 보다 정확하게 작성하는 데 도움이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-495">Azure Backup tuned cmdlets help text to be more accurate.</span></span>
* <span data-ttu-id="1d1eb-496">Azure Backup은 'Get-AzRecoveryServicesBackupJob' cmdlet을 사용하여 MAB 에이전트 작업을 가져오는 지원을 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-496">Azure Backup added support for fetching MAB agent jobs using 'Get-AzRecoveryServicesBackupJob' cmdlet.</span></span>

#### <a name="azresources"></a><span data-ttu-id="1d1eb-497">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="1d1eb-497">Az.Resources</span></span>
* <span data-ttu-id="1d1eb-498">SDK를 사용하도록 'Save-AzResourceGroupDeploymentTemplate'을 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-498">Updated 'Save-AzResourceGroupDeploymentTemplate' to use the SDK.</span></span>
* <span data-ttu-id="1d1eb-499">'Unregister-AzResourceProvider' cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-499">Added 'Unregister-AzResourceProvider' cmdlet.</span></span>

#### <a name="azsql"></a><span data-ttu-id="1d1eb-500">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="1d1eb-500">Az.Sql</span></span>
* <span data-ttu-id="1d1eb-501">Set-AzSqlInstanceActiveDirectoryAdministrator cmdlet에서 서비스 주체 및 게스트 사용자에 대한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-501">Added support for Service principal and guest users in Set-AzSqlInstanceActiveDirectoryAdministrator cmdlet'</span></span>
* <span data-ttu-id="1d1eb-502">데이터 분류 cmdlet의 버그를 수정했습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-502">Fixed a bug in Data Classification cmdlets.'</span></span>
* <span data-ttu-id="1d1eb-503">다음의 Azure SQL Managed Instance 장애 조치에 대한 지원 추가: 'Invoke-AzSqlInstanceFailover'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-503">Added support for Azure SQL Managed Instance failover: 'Invoke-AzSqlInstanceFailover'</span></span>

#### <a name="azstorage"></a><span data-ttu-id="1d1eb-504">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="1d1eb-504">Az.Storage</span></span>
* <span data-ttu-id="1d1eb-505">일부 데이터 평면 cmdlet에 대해 UserAgent가 추가되지 않는 문제를 해결했습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-505">Fixed the issue that UserAgent is not added for some data plane cmdlets.</span></span>
* <span data-ttu-id="1d1eb-506">MinimumTlsVersion 및 AllowBlobPublicAccess로 스토리지 계정 만들기/업데이트 지원</span><span class="sxs-lookup"><span data-stu-id="1d1eb-506">Supported create/update Storage account with MinimumTlsVersion and AllowBlobPublicAccess</span></span>
    -  <span data-ttu-id="1d1eb-507">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-507">'New-AzStorageAccount'</span></span>
    -  <span data-ttu-id="1d1eb-508">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-508">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="1d1eb-509">스토리지 계정의 Blob Service에서 버전 관리 사용/사용 안 함 지원</span><span class="sxs-lookup"><span data-stu-id="1d1eb-509">Support enable/disable versioning on Blob Service of a Storage account</span></span>
    - <span data-ttu-id="1d1eb-510">'Update-AzStorageBlobServiceProperty'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-510">'Update-AzStorageBlobServiceProperty'</span></span>
* <span data-ttu-id="1d1eb-511">Blob 버전 관리로 Blob 나열 지원</span><span class="sxs-lookup"><span data-stu-id="1d1eb-511">Support list blobs with blob versions</span></span>
    - <span data-ttu-id="1d1eb-512">'Get-AzStorageBlob'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-512">'Get-AzStorageBlob'</span></span>
* <span data-ttu-id="1d1eb-513">단일 Blob 스냅샷 또는 Blob 버전 가져오기/제거 지원</span><span class="sxs-lookup"><span data-stu-id="1d1eb-513">Support get/remove single blob snapshot or blob version</span></span>
    - <span data-ttu-id="1d1eb-514">'Get-AzStorageBlob'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-514">'Get-AzStorageBlob'</span></span>
    - <span data-ttu-id="1d1eb-515">'Remove-AzStorageBlob'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-515">'Remove-AzStorageBlob'</span></span>
* <span data-ttu-id="1d1eb-516">Azure.Storage.Blobs V12에서 생성된 Blob 개체의 파이프라인 지원</span><span class="sxs-lookup"><span data-stu-id="1d1eb-516">Support pipeline from blob object generated from Azure.Storage.Blobs V12</span></span>
    - <span data-ttu-id="1d1eb-517">'Get-AzStorageBlobContent'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-517">'Get-AzStorageBlobContent'</span></span>
    - <span data-ttu-id="1d1eb-518">'New-AzStorageBlobSASToken'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-518">'New-AzStorageBlobSASToken'</span></span>
    - <span data-ttu-id="1d1eb-519">'Remove-AzStorageBlob'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-519">'Remove-AzStorageBlob'</span></span>
    - <span data-ttu-id="1d1eb-520">'Set-AzStorageBlobContent'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-520">'Set-AzStorageBlobContent'</span></span>
    - <span data-ttu-id="1d1eb-521">'Start-AzStorageBlobCopy'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-521">'Start-AzStorageBlobCopy'</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="1d1eb-522">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="1d1eb-522">Az.StorageSync</span></span>
* <span data-ttu-id="1d1eb-523">ApiVersion 2020-03-01을 대상으로 하는 새 버전의 StorageSync SDK 추가</span><span class="sxs-lookup"><span data-stu-id="1d1eb-523">Added a new version StorageSync SDK targeting ApiVersion 2020-03-01</span></span>
* <span data-ttu-id="1d1eb-524">스토리지 동기화 서비스 업데이트 cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="1d1eb-524">Added Update Storage Sync Service cmdlet</span></span>
    - <span data-ttu-id="1d1eb-525">'Set-AzStorageSyncService'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-525">'Set-AzStorageSyncService'</span></span>
* <span data-ttu-id="1d1eb-526">IncomingTrafficPolicy 및 PrivateEndpointConnections가 StorageSyncService cmdlet에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-526">Added IncomingTrafficPolicy and PrivateEndpointConnections to StorageSyncService cmdlets.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="1d1eb-527">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="1d1eb-527">Az.Websites</span></span>
* <span data-ttu-id="1d1eb-528">App Service 계획과 동일한 리소스 그룹에 속하지 않는 슬롯에 대한 작업을 수행하기 위한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="1d1eb-528">Added support to perform operations for Slots not in the same resource group as the App Service Plan</span></span>

## <a name="430---june-2020"></a><span data-ttu-id="1d1eb-529">4.3.0 - 2020년 6월</span><span class="sxs-lookup"><span data-stu-id="1d1eb-529">4.3.0 - June 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="1d1eb-530">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="1d1eb-530">Az.Accounts</span></span>
* <span data-ttu-id="1d1eb-531">기본적으로 환경 검색 설정이 지원되며 'Add-AzEnvironment'를 통해 환경을 추가할 수 있음</span><span class="sxs-lookup"><span data-stu-id="1d1eb-531">Supported discovering environment setting by default and adding environment via 'Add-AzEnvironment'</span></span>
* <span data-ttu-id="1d1eb-532">미리 로드된 어셈블리 업데이트 [#12024], [#11976]</span><span class="sxs-lookup"><span data-stu-id="1d1eb-532">Update preloaded assemblies [#12024], [#11976]</span></span>
* <span data-ttu-id="1d1eb-533">Azure.Core 어셈블리 업데이트</span><span class="sxs-lookup"><span data-stu-id="1d1eb-533">Updated Azure.Core assembly</span></span>
* <span data-ttu-id="1d1eb-534">다중 스레드 실행에서 'Connect-AzAccount'가 실패할 수 있는 문제 해결 [#11201]</span><span class="sxs-lookup"><span data-stu-id="1d1eb-534">Fixed an issue that may cause 'Connect-AzAccount' to fail in multi-threaded execution [#11201]</span></span>

#### <a name="azaks"></a><span data-ttu-id="1d1eb-535">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="1d1eb-535">Az.Aks</span></span>
* <span data-ttu-id="1d1eb-536">이전에 사용하던 [AccessProfile API](https://docs.microsoft.com/rest/api/aks/managedclusters/getaccessprofile)를 [ListClusterAdmin](https://docs.microsoft.com/rest/api/aks/managedclusters/listclusteradmincredentials) 및 [ListClusterUser](https://docs.microsoft.com/rest/api/aks/managedclusters/listclusterusercredentials) API 호출로 대체</span><span class="sxs-lookup"><span data-stu-id="1d1eb-536">Replaced usage of old [AccessProfile API](https://docs.microsoft.com/rest/api/aks/managedclusters/getaccessprofile) with calls to [ListClusterAdmin](https://docs.microsoft.com/rest/api/aks/managedclusters/listclusteradmincredentials) and [ListClusterUser](https://docs.microsoft.com/rest/api/aks/managedclusters/listclusterusercredentials) APIs</span></span>

#### <a name="azbatch"></a><span data-ttu-id="1d1eb-537">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="1d1eb-537">Az.Batch</span></span>
* <span data-ttu-id="1d1eb-538">'Microsoft.Azure.Management.Batch' SDK 버전 11.0.0을 사용하도록 Az.Batch 업데이트</span><span class="sxs-lookup"><span data-stu-id="1d1eb-538">Updated Az.Batch to use 'Microsoft.Azure.Management.Batch' SDK version to 11.0.0</span></span>
* <span data-ttu-id="1d1eb-539">'New-AzBatchAccount' cmdlet에서 BatchAccount ID를 설정하는 기능 추가</span><span class="sxs-lookup"><span data-stu-id="1d1eb-539">Added the ability to set the BatchAccount Identity in the 'New-AzBatchAccount' cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="1d1eb-540">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="1d1eb-540">Az.CognitiveServices</span></span>
* <span data-ttu-id="1d1eb-541">계정 기능 표시 지원</span><span class="sxs-lookup"><span data-stu-id="1d1eb-541">Supported displaying account capabilities.</span></span>
* <span data-ttu-id="1d1eb-542">PublicNetworkAccess 수정 지원</span><span class="sxs-lookup"><span data-stu-id="1d1eb-542">Supported modifying PublicNetworkAccess.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="1d1eb-543">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="1d1eb-543">Az.Compute</span></span>
* <span data-ttu-id="1d1eb-544">Set-AzVM 및 Set-AzVmssVM cmdlet에 SimulateEviction 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="1d1eb-544">Added SimulateEviction parameter to Set-AzVM and Set-AzVmssVM cmdlets.</span></span>
* <span data-ttu-id="1d1eb-545">AzGalleryImageVersion cmdlet에 대한 StorageAccountType 매개 변수의 인수 완성자에 'Premium_LRS' 추가</span><span class="sxs-lookup"><span data-stu-id="1d1eb-545">Added 'Premium_LRS' to the argument completer of StorageAccountType parameter for New-AzGalleryImageVersion cmdlet.</span></span>
* <span data-ttu-id="1d1eb-546">VMCustomScriptExtension에 Substatuses 추가 [#11297]</span><span class="sxs-lookup"><span data-stu-id="1d1eb-546">Added Substatuses to VMCustomScriptExtension [#11297]</span></span>
* <span data-ttu-id="1d1eb-547">New-AzVM 및 New-AzVMConfig cmdlet에 대한 EvictionPolicy 매개 변수의 인수 완성자에 'Delete' 추가</span><span class="sxs-lookup"><span data-stu-id="1d1eb-547">Added 'Delete' to the argument completer of EvictionPolicy parameter for New-AzVM and New-AzVMConfig cmdlets.</span></span>
* <span data-ttu-id="1d1eb-548">새 SAP용 VM 확장의 이름 수정</span><span class="sxs-lookup"><span data-stu-id="1d1eb-548">Fixed name of new VM Extension for SAP</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="1d1eb-549">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="1d1eb-549">Az.DataFactory</span></span>
* <span data-ttu-id="1d1eb-550">ADF .Net SDK 버전을 4.9.0으로 업데이트</span><span class="sxs-lookup"><span data-stu-id="1d1eb-550">Updated ADF .Net SDK version to 4.9.0</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="1d1eb-551">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="1d1eb-551">Az.EventHub</span></span>
* <span data-ttu-id="1d1eb-552">'New-AzEventHubNamespace' 및 'Set-AzEventHubNamespace' cmdlet에 관리 ID 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="1d1eb-552">Added Managed Identity parameters to 'New-AzEventHubNamespace' and 'Set-AzEventHubNamespace' cmdlets</span></span>

#### <a name="azfunctions"></a><span data-ttu-id="1d1eb-553">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="1d1eb-553">Az.Functions</span></span>
* <span data-ttu-id="1d1eb-554">PowerShell 7.0 및 Java 11 함수 앱을 만드는 지원 추가</span><span class="sxs-lookup"><span data-stu-id="1d1eb-554">Added support to create PowerShell 7.0 and Java 11 function apps</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="1d1eb-555">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="1d1eb-555">Az.HDInsight</span></span>
* <span data-ttu-id="1d1eb-556">호스트를 나열하고 HDInsight 클러스터의 특정 호스트를 다시 시작하는 기능 지원</span><span class="sxs-lookup"><span data-stu-id="1d1eb-556">Supported listing hosts and restart specific hosts of the HDInsight cluster.</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="1d1eb-557">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="1d1eb-557">Az.HealthcareApis</span></span>
* <span data-ttu-id="1d1eb-558">SDK 버전을 1.1.0으로 업데이트</span><span class="sxs-lookup"><span data-stu-id="1d1eb-558">Updated the SDK version to 1.1.0</span></span>
* <span data-ttu-id="1d1eb-559">설정 및 관리 ID 내보내기에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="1d1eb-559">Added support for Export settings and Managed Identity</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="1d1eb-560">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="1d1eb-560">Az.Monitor</span></span>
* <span data-ttu-id="1d1eb-561">'Set-AzActivityLogAlert'에 대한 입력 개체 매개 변수 수정</span><span class="sxs-lookup"><span data-stu-id="1d1eb-561">Fixed input object parameter for 'Set-AzActivityLogAlert'</span></span>
* <span data-ttu-id="1d1eb-562">'Set-AzActionGroup'에 대한 'InputObject' 매개 변수 수정 [#10868]</span><span class="sxs-lookup"><span data-stu-id="1d1eb-562">Fixed 'InputObject' parameter for 'Set-AzActionGroup' [#10868]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="1d1eb-563">Az.Network</span><span class="sxs-lookup"><span data-stu-id="1d1eb-563">Az.Network</span></span>
* <span data-ttu-id="1d1eb-564">'Remove-AzExpressRouteCircuitConnectionConfig'에 AddressPrefixType 매개 변수 지원 추가</span><span class="sxs-lookup"><span data-stu-id="1d1eb-564">Added support for AddressPrefixType parameter to 'Remove-AzExpressRouteCircuitConnectionConfig'</span></span>
* <span data-ttu-id="1d1eb-565">Azure FirewallPolicy에 대한 새 cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="1d1eb-565">Added new cmdlets for Azure FirewallPolicy</span></span>
    - <span data-ttu-id="1d1eb-566">'New-AzFirewallPolicyDnsSetting'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-566">'New-AzFirewallPolicyDnsSetting'</span></span>
    - <span data-ttu-id="1d1eb-567">방화벽 정책에 대한 네트워크 규칙에서 대상 FQDN 지원</span><span class="sxs-lookup"><span data-stu-id="1d1eb-567">Support for Destination FQDN in Network Rules for Firewall Policy</span></span>
* <span data-ttu-id="1d1eb-568">백 엔드 주소 풀 작업에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="1d1eb-568">Added support for backend address pool operations</span></span>
    - <span data-ttu-id="1d1eb-569">'New-AzLoadBalancerBackendAddressConfig'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-569">'New-AzLoadBalancerBackendAddressConfig'</span></span>
    - <span data-ttu-id="1d1eb-570">'New-AzLoadBalancerBackendAddressPool'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-570">'New-AzLoadBalancerBackendAddressPool'</span></span>
    - <span data-ttu-id="1d1eb-571">'Set-AzLoadBalancerBackendAddressPool'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-571">'Set-AzLoadBalancerBackendAddressPool'</span></span>
    - <span data-ttu-id="1d1eb-572">'Remove-AzLoadBalancerBackendAddressPool'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-572">'Remove-AzLoadBalancerBackendAddressPool'</span></span>
    - <span data-ttu-id="1d1eb-573">'Get-AzLoadBalancerBackendAddressPool'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-573">'Get-AzLoadBalancerBackendAddressPool'</span></span>
* <span data-ttu-id="1d1eb-574">'New-AzIpGroup'에 대한 이름 유효성 검사 추가</span><span class="sxs-lookup"><span data-stu-id="1d1eb-574">Added name validation for 'New-AzIpGroup'</span></span>
* <span data-ttu-id="1d1eb-575">Azure FirewallPolicy에 대한 새 cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="1d1eb-575">Added new cmdlets for Azure FirewallPolicy</span></span>
    - <span data-ttu-id="1d1eb-576">'New-AzFirewallPolicyThreatIntelWhitelist'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-576">'New-AzFirewallPolicyThreatIntelWhitelist'</span></span>
* <span data-ttu-id="1d1eb-577">기능에 대한 새로운 명령이 업데이트됨: VirtualWan P2SVpnGateway에서 사용자 지정 dns 서버 설정/제거</span><span class="sxs-lookup"><span data-stu-id="1d1eb-577">Updated below commands for feature: Custom dns servers set/remove on VirtualWan P2SVpnGateway.</span></span>
    - <span data-ttu-id="1d1eb-578">New-AzP2sVpnGateway 업데이트됨: 고객이 P2SVpnGateway에 설정할 dns 서버를 지정할 수 있는 선택적 매개 변수 '-CustomDnsServer'가 추가되었으며, 이 매개 변수는 지점 및 사이트 간 클라이언트에서 사용 가능</span><span class="sxs-lookup"><span data-stu-id="1d1eb-578">Updated New-AzP2sVpnGateway: Added optional parameter '-CustomDnsServer' for customers to specify their dns servers to set on P2SVpnGateway, which can be used by Point to site clients.</span></span>
    - <span data-ttu-id="1d1eb-579">Update-AzP2sVpnGateway 업데이트됨: 고객이 P2SVpnGateway에 설정할 dns 서버를 지정할 수 있는 선택적 매개 변수 '-CustomDnsServer'가 추가되었으며, 이 매개 변수는 지점 및 사이트 간 클라이언트에서 사용 가능</span><span class="sxs-lookup"><span data-stu-id="1d1eb-579">Updated Update-AzP2sVpnGateway: Added optional parameter '-CustomDnsServer' for customers to specify their dns servers to set on P2SVpnGateway, which can be used by Point to site clients.</span></span>
* <span data-ttu-id="1d1eb-580">'Update-AzVpnGateway' 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="1d1eb-580">Updated 'Update-AzVpnGateway'</span></span>
    - <span data-ttu-id="1d1eb-581">고객이 VpnGateway에 설정할 사용자 지정 bgps를 지정할 수 있도록 선택적 매개 변수 '-BgpPeeringAddress' 추가</span><span class="sxs-lookup"><span data-stu-id="1d1eb-581">Added optional parameter '-BgpPeeringAddress' for customers to specify their custom bgps to set on VpnGateway.</span></span>
* <span data-ttu-id="1d1eb-582">VirtualHub 리소스의 라우팅 상태 초기화를 지원하는 새 cmdlet 추가:</span><span class="sxs-lookup"><span data-stu-id="1d1eb-582">Added new cmdlet to support resetting the routing state of a VirtualHub resource:</span></span>
    - <span data-ttu-id="1d1eb-583">'Reset-AzHubRouter'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-583">'Reset-AzHubRouter'</span></span>
* <span data-ttu-id="1d1eb-584">방화벽 정책에 대한 최근 Swagger 변화에 따라 아래 항목 업데이트</span><span class="sxs-lookup"><span data-stu-id="1d1eb-584">Updated below things based on recent swagger change for Firewall Policy</span></span>
    - <span data-ttu-id="1d1eb-585">RuleGroup, RuleCollectionGroup 및 RuleType의 이름 변경</span><span class="sxs-lookup"><span data-stu-id="1d1eb-585">Changes names for RuleGroup, RuleCollectionGroup and RuleType</span></span>
    - <span data-ttu-id="1d1eb-586">여러 NAT 규칙 컬렉션을 지원하도록 방화벽 정책 NAT 규칙 컬렉션에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="1d1eb-586">Added support for Firewall Policy NAT Rule Collections to support multiple NAT Rule Collection</span></span>
* <span data-ttu-id="1d1eb-587">[호환성이 손상되는 변경] 'New-AzFirewallPolicyApplicationRule' 및 'New-AzFirewallPolicyNetworkRule'에 대한 필수 매개 변수 'SourceIpGroup' 추가</span><span class="sxs-lookup"><span data-stu-id="1d1eb-587">[Breaking Change] Added mandatory parameter 'SourceIpGroup' for 'New-AzFirewallPolicyApplicationRule' and 'New-AzFirewallPolicyNetworkRule'.</span></span>
* <span data-ttu-id="1d1eb-588">[호환성이 손상되는 변경] 'New-AzFirewallPolicyApplicationRule' 수정, 'SourceAddress' 매개 변수를 필수로 변경</span><span class="sxs-lookup"><span data-stu-id="1d1eb-588">[Breaking Change] Fixed 'New-AzFirewallPolicyApplicationRule', parameter 'SourceAddress' to be mandatory.</span></span>
* <span data-ttu-id="1d1eb-589">[호환성이 손상되는 변경] 'New-AzFirewallPolicyApplicationRule' 수정, 'SourceAddress' 매개 변수를 필수로 변경</span><span class="sxs-lookup"><span data-stu-id="1d1eb-589">[Breaking Change] Fixed 'New-AzFirewallPolicyApplicationRule', parameter 'SourceAddress' to be mandatory.</span></span>
* <span data-ttu-id="1d1eb-590">[호환성이 손상되는 변경] 다음 필수 매개 변수 제거: 'New-AzFirewallPolicyNatRuleCollection'의 'TranslatedAddress', 'TranslatedPort'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-590">[Breaking Change] Removed mandatory parameters: 'TranslatedAddress', 'TranslatedPort' for 'New-AzFirewallPolicyNatRuleCollection'.</span></span>
* <span data-ttu-id="1d1eb-591">PrivateLink On Application Gateway를 지원하는 새 cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="1d1eb-591">Added new cmdlets to support PrivateLink On Application Gateway</span></span>
    - <span data-ttu-id="1d1eb-592">'New-AzApplicationGatewayPrivateLinkConfiguration'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-592">'New-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="1d1eb-593">'Get-AzApplicationGatewayPrivateLinkConfiguration'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-593">'Get-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="1d1eb-594">'New-AzApplicationGatewayPrivateLinkConfiguration'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-594">'New-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="1d1eb-595">'Set-AzApplicationGatewayPrivateLinkConfiguration'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-595">'Set-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="1d1eb-596">'Remove-AzApplicationGatewayPrivateLinkConfiguration'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-596">'Remove-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="1d1eb-597">'New-AzApplicationGatewayPrivateLinkIpConfiguration'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-597">'New-AzApplicationGatewayPrivateLinkIpConfiguration'</span></span>
* <span data-ttu-id="1d1eb-598">VirtualHub의 HubRouteTables 자식 리소스에 대한 새 cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="1d1eb-598">Added new cmdlets for HubRouteTables child resource of VirtualHub.</span></span>
    - <span data-ttu-id="1d1eb-599">'New-AzVHubRoute'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-599">'New-AzVHubRoute'</span></span>
    - <span data-ttu-id="1d1eb-600">'New-AzVHubRouteTable'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-600">'New-AzVHubRouteTable'</span></span>
    - <span data-ttu-id="1d1eb-601">'Get-AzVHubRouteTable'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-601">'Get-AzVHubRouteTable'</span></span>
    - <span data-ttu-id="1d1eb-602">'Update-AzVHubRouteTable'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-602">'Update-AzVHubRouteTable'</span></span>
    - <span data-ttu-id="1d1eb-603">'Remove-AzVHubRouteTable'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-603">'Remove-AzVHubRouteTable'</span></span>
* <span data-ttu-id="1d1eb-604">VirtualWan의 사용자 지정 라우팅에 대한 선택적 RoutingConfiguration 입력 매개 변수를 지원하도록 기존 cmdlet 업데이트</span><span class="sxs-lookup"><span data-stu-id="1d1eb-604">Updated existing cmdlets to support optional RoutingConfiguration input parameter for custom routing in VirtualWan.</span></span>
    - <span data-ttu-id="1d1eb-605">'New-AzExpressRouteConnection'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-605">'New-AzExpressRouteConnection'</span></span>
    - <span data-ttu-id="1d1eb-606">'Set-AzExpressRouteConnection'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-606">'Set-AzExpressRouteConnection'</span></span>
    - <span data-ttu-id="1d1eb-607">'New-AzVirtualHubVnetConnection'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-607">'New-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="1d1eb-608">'Update-AzVirtualHubVnetConnection'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-608">'Update-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="1d1eb-609">'New-AzVpnConnection'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-609">'New-AzVpnConnection'</span></span>
    - <span data-ttu-id="1d1eb-610">'Update-AzVpnConnection'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-610">'Update-AzVpnConnection'</span></span>
    - <span data-ttu-id="1d1eb-611">'New-AzP2sVpnGateway'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-611">'New-AzP2sVpnGateway'</span></span>
    - <span data-ttu-id="1d1eb-612">'Update-AzP2sVpnGateway'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-612">'Update-AzP2sVpnGateway'</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="1d1eb-613">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="1d1eb-613">Az.OperationalInsights</span></span>
* <span data-ttu-id="1d1eb-614">PSWorkspace가 IOperationalInsightsWorkspace를 구현하지 않는 버그 수정 [#12135]</span><span class="sxs-lookup"><span data-stu-id="1d1eb-614">Fixed bug PSWorkspace doesn't implement IOperationalInsightsWorkspace [#12135]</span></span>
* <span data-ttu-id="1d1eb-615">'Set-AzOperationalInsightsWorkspace'에서 'Sku' 매개 변수의 올바른 값 세트에 'pergb2018' 추가</span><span class="sxs-lookup"><span data-stu-id="1d1eb-615">Added 'pergb2018' to valid value set of parameter 'Sku' in 'Set-AzOperationalInsightsWorkspace'</span></span> 
* <span data-ttu-id="1d1eb-616">매개 변수 'FunctionParameter'에 대한 별칭 'FunctionParameters' 추가</span><span class="sxs-lookup"><span data-stu-id="1d1eb-616">Added alias 'FunctionParameters' for parameter 'FunctionParameter' to</span></span>
    - <span data-ttu-id="1d1eb-617">'New-AzOperationalInsightsSavedSearch'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-617">'New-AzOperationalInsightsSavedSearch'</span></span>
    - <span data-ttu-id="1d1eb-618">'Set-AzOperationalInsightsSavedSearch'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-618">'Set-AzOperationalInsightsSavedSearch'</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="1d1eb-619">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="1d1eb-619">Az.RecoveryServices</span></span>
* <span data-ttu-id="1d1eb-620">Azure Backup에서 MAB 항목을 가져오기 위한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="1d1eb-620">Azure Backup added support for fetching MAB items.</span></span>
* <span data-ttu-id="1d1eb-621">Azure Site Recovery에서 'StandardSSD_LRS' 디스크 형식 지원</span><span class="sxs-lookup"><span data-stu-id="1d1eb-621">Azure Site Recovery supports disk type 'StandardSSD_LRS'</span></span>

#### <a name="azresources"></a><span data-ttu-id="1d1eb-622">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="1d1eb-622">Az.Resources</span></span>
* <span data-ttu-id="1d1eb-623">'PSADUser'에서 'UsageLocation', 'GivenName', 'Surname', 'AccountEnabled', 'MailNickname', 'Mail' 추가 [#10526] [#10497]</span><span class="sxs-lookup"><span data-stu-id="1d1eb-623">Added 'UsageLocation', 'GivenName', 'Surname', 'AccountEnabled', 'MailNickname', 'Mail' on 'PSADUser' [#10526] [#10497]</span></span>
* <span data-ttu-id="1d1eb-624">'Get-AzADUser'에서 '-Mail'이 작동하지 않는 문제 해결 [#11981]</span><span class="sxs-lookup"><span data-stu-id="1d1eb-624">Fixed issue that '-Mail' doesn't work on 'Get-AzADUser' [#11981]</span></span>
* <span data-ttu-id="1d1eb-625">'Get-AzDeploymentWhatIfResult' 및 'Get-AzResourceGroupDeploymentWhatIfResult'에 '-ExcludeChangeType' 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="1d1eb-625">Added '-ExcludeChangeType' parameter to 'Get-AzDeploymentWhatIfResult' and 'Get-AzResourceGroupDeploymentWhatIfResult'</span></span>
* <span data-ttu-id="1d1eb-626">'New-AzDeployment' 및 'New-AzResourceGroupDeployment'에 '-WhatIfExcludeChangeType' 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="1d1eb-626">Added '-WhatIfExcludeChangeType' parameter to 'New-AzDeployment' and 'New-AzResourceGroupDeployment'</span></span>
* <span data-ttu-id="1d1eb-627">보다 나은 오류 메시지를 표시하도록 'Test-Az\*Deployment' cmdlet 업데이트</span><span class="sxs-lookup"><span data-stu-id="1d1eb-627">Updated 'Test-Az\*Deployment' cmdlets to show better error messages</span></span>
* <span data-ttu-id="1d1eb-628">deployment create 및 What-If cmdlet의 '-Name' 매개 변수에 대한 도움말 메시지 수정</span><span class="sxs-lookup"><span data-stu-id="1d1eb-628">Fixed help message for '-Name' parameter of deployment create and What-If cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="1d1eb-629">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="1d1eb-629">Az.Sql</span></span>
* <span data-ttu-id="1d1eb-630">Set SQL Server Azure Active Directory Admin cmdlet의 서비스 주체에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="1d1eb-630">Added support for service principal for Set SQL Server Azure Active Directory Admin cmdlet</span></span>
* <span data-ttu-id="1d1eb-631">데이터 분류 cmdlet의 동기화 문제 해결</span><span class="sxs-lookup"><span data-stu-id="1d1eb-631">Fixed sync issue in Data Classification cmdlets.</span></span>
* <span data-ttu-id="1d1eb-632">'Set-AzSqlServerActiveDirectoryAdministrator'에서 메일로 사용자 검색 지원 [#12192]</span><span class="sxs-lookup"><span data-stu-id="1d1eb-632">Supported searching user by mail on 'Set-AzSqlServerActiveDirectoryAdministrator' [#12192]</span></span>

#### <a name="azstorage"></a><span data-ttu-id="1d1eb-633">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="1d1eb-633">Az.Storage</span></span>
* <span data-ttu-id="1d1eb-634">RequireInfrastructureEncryption을 사용하여 스토리지 계정 만들기 지원</span><span class="sxs-lookup"><span data-stu-id="1d1eb-634">Supported create Storage account with RequireInfrastructureEncryption</span></span>
    -  <span data-ttu-id="1d1eb-635">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-635">'New-AzStorageAccount'</span></span>
* <span data-ttu-id="1d1eb-636">Azure.Core 로딩 논리를 Az.Accounts로 이동</span><span class="sxs-lookup"><span data-stu-id="1d1eb-636">Moved the logic of loading Azure.Core to Az.Accounts</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="1d1eb-637">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="1d1eb-637">Az.Websites</span></span>
* <span data-ttu-id="1d1eb-638">'Restore-AzDeletedWebApp'에서 복원이 실패할 경우 생성된 웹앱을 삭제하는 보호 기능 추가</span><span class="sxs-lookup"><span data-stu-id="1d1eb-638">Added safeguard to delete created webapp if restore failed in 'Restore-AzDeletedWebApp'</span></span>
* <span data-ttu-id="1d1eb-639">'New-AzWebApp' 및 'New-AzWebAppSlot'에 대한 'SourceWebApp.Location' 추가</span><span class="sxs-lookup"><span data-stu-id="1d1eb-639">Added 'SourceWebApp.Location' for 'New-AzWebApp' and 'New-AzWebAppSlot'</span></span>
* <span data-ttu-id="1d1eb-640">'Set-AzWebApp' 및 'Set-AzWebAppSlot'에서 컨테이너 설정을 변경할 수 없는 버그 수정</span><span class="sxs-lookup"><span data-stu-id="1d1eb-640">Fixed bug that prevented changing Container settings in 'Set-AzWebApp' and 'Set-AzWebAppSlot'</span></span>
* <span data-ttu-id="1d1eb-641">Get-AzWebApp에 대한 -Name을 제공하지 않으면 SiteConfig를 가져오는 버그 수정</span><span class="sxs-lookup"><span data-stu-id="1d1eb-641">Fixed bug to get SiteConfig when -Name is not given for Get-AzWebApp</span></span>
* <span data-ttu-id="1d1eb-642">Linux 앱용 ASP를 만드는 지원 추가</span><span class="sxs-lookup"><span data-stu-id="1d1eb-642">Added a support to create ASP for Linux Apps</span></span>
* <span data-ttu-id="1d1eb-643">리소스 그룹 간 복제에 대한 예외 추가</span><span class="sxs-lookup"><span data-stu-id="1d1eb-643">Added exceptions for clone across resource groups</span></span>

## <a name="420---june-2020"></a><span data-ttu-id="1d1eb-644">4.2.0 - 2020년 6월</span><span class="sxs-lookup"><span data-stu-id="1d1eb-644">4.2.0 - June 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="1d1eb-645">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="1d1eb-645">Az.Accounts</span></span>
* <span data-ttu-id="1d1eb-646">Azure Automation 또는 PowerShell 작업에서 Az가 로그를 건너뛸 수 있는 문제 수정[#11492]</span><span class="sxs-lookup"><span data-stu-id="1d1eb-646">Fixed an issue that may cause Az to skip logs in Azure Automation or PowerShell jobs [#11492]</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="1d1eb-647">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="1d1eb-647">Az.AnalysisServices</span></span>
* <span data-ttu-id="1d1eb-648">데이터 평면 cmdlet의 어셈블리 버전 업데이트</span><span class="sxs-lookup"><span data-stu-id="1d1eb-648">Updated assembly version of data plane cmdlets</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="1d1eb-649">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="1d1eb-649">Az.ApiManagement</span></span>
* <span data-ttu-id="1d1eb-650">서비스 관리 cmdlet의 어셈블리 버전 업데이트</span><span class="sxs-lookup"><span data-stu-id="1d1eb-650">Updated assembly version of service management cmdlets</span></span>

#### <a name="azbilling"></a><span data-ttu-id="1d1eb-651">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="1d1eb-651">Az.Billing</span></span>
* <span data-ttu-id="1d1eb-652">소비 cmdlet의 어셈블리 버전 업데이트</span><span class="sxs-lookup"><span data-stu-id="1d1eb-652">Updated assembly version of consumption cmdlets</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="1d1eb-653">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="1d1eb-653">Az.CognitiveServices</span></span>
* <span data-ttu-id="1d1eb-654">PrivateEndpoint 및 PublicNetworkAccess control을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-654">Support PrivateEndpoint and PublicNetworkAccess control.</span></span> 

#### <a name="azdatafactory"></a><span data-ttu-id="1d1eb-655">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="1d1eb-655">Az.DataFactory</span></span>
* <span data-ttu-id="1d1eb-656">데이터 팩터리 V2 cmdlet의 어셈블리 버전 업데이트</span><span class="sxs-lookup"><span data-stu-id="1d1eb-656">Updated assembly version of data factory V2 cmdlets</span></span>

#### <a name="azdatashare"></a><span data-ttu-id="1d1eb-657">Az.DataShare</span><span class="sxs-lookup"><span data-stu-id="1d1eb-657">Az.DataShare</span></span>
* <span data-ttu-id="1d1eb-658">''Az.DataShare'' 모듈의 일반 공급</span><span class="sxs-lookup"><span data-stu-id="1d1eb-658">General availability of ''Az.DataShare'' module</span></span>

#### <a name="azdesktopvirtualization"></a><span data-ttu-id="1d1eb-659">Az.DesktopVirtualization</span><span class="sxs-lookup"><span data-stu-id="1d1eb-659">Az.DesktopVirtualization</span></span>
* <span data-ttu-id="1d1eb-660">''Az.DesktopVirtualization'' 모듈의 일반 공급</span><span class="sxs-lookup"><span data-stu-id="1d1eb-660">General availability of ''Az.DesktopVirtualization'' module</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="1d1eb-661">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="1d1eb-661">Az.OperationalInsights</span></span>
* <span data-ttu-id="1d1eb-662">SDK를 0.21.0으로 업그레이드</span><span class="sxs-lookup"><span data-stu-id="1d1eb-662">Upgraded SDK to 0.21.0</span></span>
* <span data-ttu-id="1d1eb-663">다음에 선택적 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="1d1eb-663">Added optional parameters to</span></span> 
    - <span data-ttu-id="1d1eb-664">'New-AzOperationalInsightsSavedSearch'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-664">'New-AzOperationalInsightsSavedSearch'</span></span>
    - <span data-ttu-id="1d1eb-665">'Set-AzOperationalInsightsSavedSearch'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-665">'Set-AzOperationalInsightsSavedSearch'</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="1d1eb-666">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="1d1eb-666">Az.PolicyInsights</span></span>
* <span data-ttu-id="1d1eb-667">'Start-AzPolicyComplianceScan'의 예제 3 수정</span><span class="sxs-lookup"><span data-stu-id="1d1eb-667">Corrected example 3 for 'Start-AzPolicyComplianceScan'</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="1d1eb-668">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="1d1eb-668">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="1d1eb-669">PowerBI cmdlet의 어셈블리 버전 업데이트</span><span class="sxs-lookup"><span data-stu-id="1d1eb-669">Updated assembly version of PowerBI cmdlets</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="1d1eb-670">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="1d1eb-670">Az.PrivateDns</span></span>
* <span data-ttu-id="1d1eb-671">Remove-AzPrivateDnsRecordSet에 대한 자세한 정보 출력 문자열 형식 수정</span><span class="sxs-lookup"><span data-stu-id="1d1eb-671">Corrected verbose output string formatting for Remove-AzPrivateDnsRecordSet</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="1d1eb-672">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="1d1eb-672">Az.RecoveryServices</span></span>
* <span data-ttu-id="1d1eb-673">xml 입력에서 영역 간 복제를 위한 복구 계획을 세우기 위한 Azure Site Recovery 지원.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-673">Azure Site Recovery support for creating recovery plan for zone to zone replication from xml input.</span></span>
* <span data-ttu-id="1d1eb-674">SiteRecovery 및 Backup cmdlet의 어셈블리 버전 업데이트</span><span class="sxs-lookup"><span data-stu-id="1d1eb-674">Updated assembly version of SiteRecovery and Backup cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="1d1eb-675">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="1d1eb-675">Az.Resources</span></span>
* <span data-ttu-id="1d1eb-676">Get-AzDeploymentScriptLog 및 Save-AzDeploymentScriptLog cmdlet에 Tail 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="1d1eb-676">Added Tail parameter to Get-AzDeploymentScriptLog and Save-AzDeploymentScriptLog cmdlets</span></span>
* <span data-ttu-id="1d1eb-677">형식이 지정된 출력 속성을 Get-AzDeploymentScript cmdlet 출력에 표시</span><span class="sxs-lookup"><span data-stu-id="1d1eb-677">Formatted Output property and show it on the Get-AzDeploymentScript cmdlet output</span></span>
* <span data-ttu-id="1d1eb-678">-DeploymentScriptInputObject 매개 변수의 이름이 -DeploymentScriptObject로 변경</span><span class="sxs-lookup"><span data-stu-id="1d1eb-678">Renamed -DeploymentScriptInputObject parameter to -DeploymentScriptObject</span></span>
* <span data-ttu-id="1d1eb-679">cmdlet 메시지에서 누락된 파일/대상 이름이 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-679">Fixed missing file/target name in cmdlet messages.</span></span>
* <span data-ttu-id="1d1eb-680">리소스 관리자 및 태그 cmdlet의 어셈블리 버전 업데이트</span><span class="sxs-lookup"><span data-stu-id="1d1eb-680">Updated assembly version of resource manager and tags cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="1d1eb-681">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="1d1eb-681">Az.Sql</span></span>
* <span data-ttu-id="1d1eb-682">UsePrivateLinkConnection을 'New-AzSqlSyncGroup', 'Update-AzSqlSyncGroup', 'New-AzSqlSyncMember' 및 'Update-AzSqlSyncMember'에 추가</span><span class="sxs-lookup"><span data-stu-id="1d1eb-682">Added UsePrivateLinkConnection to 'New-AzSqlSyncGroup', 'Update-AzSqlSyncGroup', 'New-AzSqlSyncMember' and 'Update-AzSqlSyncMember'</span></span>
* <span data-ttu-id="1d1eb-683">SyncMemberAzureDatabaseResourceId를 'New-AzSqlSyncMember' 및 'Update-AzSqlSyncMember'에 추가</span><span class="sxs-lookup"><span data-stu-id="1d1eb-683">Added SyncMemberAzureDatabaseResourceId to 'New-AzSqlSyncMember' and 'Update-AzSqlSyncMember'</span></span>
* <span data-ttu-id="1d1eb-684">SQL Server Azure Active Directory Admin cmdlet을 설정하는 게스트 사용자 조회 지원 추가</span><span class="sxs-lookup"><span data-stu-id="1d1eb-684">Added Guest user lookup support to Set SQL Server Azure Active Directory Admin cmdlet</span></span>

#### <a name="azstorage"></a><span data-ttu-id="1d1eb-685">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="1d1eb-685">Az.Storage</span></span>
* <span data-ttu-id="1d1eb-686">데이터 평면 cmdlet의 어셈블리 버전 업데이트</span><span class="sxs-lookup"><span data-stu-id="1d1eb-686">Updated assembly version of data plane cmdlets</span></span>

## <a name="410---may-2020"></a><span data-ttu-id="1d1eb-687">4.1.0 - 2020년 5월</span><span class="sxs-lookup"><span data-stu-id="1d1eb-687">4.1.0 - May 2020</span></span>
### <a name="highlights-since-the-last-release"></a><span data-ttu-id="1d1eb-688">마지막 릴리스 이후의 주요 사항</span><span class="sxs-lookup"><span data-stu-id="1d1eb-688">Highlights since the last release</span></span>
* <span data-ttu-id="1d1eb-689">지원되는 PowerShell 버전: Windows PowerShell 5.1, PowerShell Core 6.2.4 이상, PowerShell 7</span><span class="sxs-lookup"><span data-stu-id="1d1eb-689">Supported PowerShell versions: Windows PowerShell 5.1, PowerShell Core 6.2.4+, PowerShell 7</span></span>
* <span data-ttu-id="1d1eb-690">Az.Functions 일반 공급</span><span class="sxs-lookup"><span data-stu-id="1d1eb-690">General availability of Az.Functions</span></span> 
* <span data-ttu-id="1d1eb-691">Az.ApiManagement, Az.Batch, Az.Compute, Az.KeyVault, Az.Monitor, Az.Network, Az.OperationalInsights, Az.Resources 및 Az.Storage의 주요 릴리스 출시</span><span class="sxs-lookup"><span data-stu-id="1d1eb-691">Az.ApiManagement, Az.Batch, Az.Compute, Az.KeyVault, Az.Monitor, Az.Network, Az.OperationalInsights, Az.Resources, and Az.Storage have major release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="1d1eb-692">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="1d1eb-692">Az.Accounts</span></span>
* <span data-ttu-id="1d1eb-693">'AzureSynapseAnalyticsEndpointResourceId' 및 'AzureSynapseAnalyticsEndpointSuffix' 매개 변수를 허용하도록 'Add-AzEnvironment' 및 'Set-AzEnvironment' 업데이트</span><span class="sxs-lookup"><span data-stu-id="1d1eb-693">Updated 'Add-AzEnvironment' and 'Set-AzEnvironment' to accept parameters 'AzureSynapseAnalyticsEndpointResourceId' and 'AzureSynapseAnalyticsEndpointSuffix'</span></span>
* <span data-ttu-id="1d1eb-694">Az.Accounts에 Azure.Core 관련 어셈블리가 추가되었으며 지원되는 PowerShell 플랫폼은 Windows PowerShell 5.1, PowerShell Core 6.2.4, PowerShell 7+입니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-694">Added Azure.Core related assemblies into Az.Accounts, supported PowerShell platforms include Windows PowerShell 5.1, PowerShell Core 6.2.4, PowerShell 7+</span></span>

#### <a name="azaks"></a><span data-ttu-id="1d1eb-695">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="1d1eb-695">Az.Aks</span></span>
* <span data-ttu-id="1d1eb-696">API 버전을 2019-10-01로 업그레이드</span><span class="sxs-lookup"><span data-stu-id="1d1eb-696">Upgraded API Version to 2019-10-01</span></span>
* <span data-ttu-id="1d1eb-697">Windows 컨테이너를 사용하여 AKS 만들기 지원</span><span class="sxs-lookup"><span data-stu-id="1d1eb-697">Supported to create AKS using Windows container</span></span>
* <span data-ttu-id="1d1eb-698">새 cmdlet 추가: 'New-AzAksNodePool', 'Update-AzAksNodePool', 'Remove-AzAksNodePool', 'Get-AzAksNodePool', 'Install-AzAksKubectl', 'Get-AzAksVersion'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-698">Provided new cmdlets: 'New-AzAksNodePool', 'Update-AzAksNodePool', 'Remove-AzAksNodePool',        'Get-AzAksNodePool', 'Install-AzAksKubectl', 'Get-AzAksVersion'</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="1d1eb-699">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="1d1eb-699">Az.ApiManagement</span></span>
* <span data-ttu-id="1d1eb-700">'New-AzApiManagement' 및 'Set-AzApiManagement': [-AssignIdentity] 매개 변수 이름을 [-SystemAssignedIdentity]로 변경</span><span class="sxs-lookup"><span data-stu-id="1d1eb-700">'New-AzApiManagement' and 'Set-AzApiManagement': [-AssignIdentity] parameter renamed as [-SystemAssignedIdentity]</span></span>
* <span data-ttu-id="1d1eb-701">'New-AzApiManagement' 및 'Set-AzApiManagement': 새 매개 변수 추가: [-UserAssignedIdentity <String[]>]</span><span class="sxs-lookup"><span data-stu-id="1d1eb-701">'New-AzApiManagement' and 'Set-AzApiManagement': New parameter added: [-UserAssignedIdentity <String[]>]</span></span>
* <span data-ttu-id="1d1eb-702">'Get-AzApiManagementProperty': 'Get-AzApiManagementNamedValue'로 이름 변경.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-702">'Get-AzApiManagementProperty': renamed as 'Get-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="1d1eb-703">PropertyId 매개 변수 이름을 NamedValueId로 변경.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-703">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="1d1eb-704">'New-AzApiManagementProperty': 'New-AzApiManagementNamedValue'로 이름 변경.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-704">'New-AzApiManagementProperty': renamed as 'New-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="1d1eb-705">PropertyId 매개 변수 이름을 NamedValueId로 변경.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-705">PropertyId parameter renamed as NamedValueId.</span></span> 
* <span data-ttu-id="1d1eb-706">'Set-AzApiManagementProperty': 'Set-AzApiManagementNamedValue'로 이름 변경.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-706">'Set-AzApiManagementProperty': renamed as 'Set-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="1d1eb-707">PropertyId 매개 변수 이름을 NamedValueId로 변경.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-707">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="1d1eb-708">'Remove-AzApiManagementProperty': 'Remove-AzApiManagementNamedValue'로 이름 변경.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-708">'Remove-AzApiManagementProperty': renamed as 'Remove-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="1d1eb-709">PropertyId 매개 변수 이름을 NamedValueId로 변경.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-709">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="1d1eb-710">새 'Get-AzApiManagementAuthorizationServerClientSecret' cmdlet이 추가되었으며 'Get-AzApiManagementAuthorizationServer'는 더 이상 클라이언트 암호를 반환하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-710">Added new 'Get-AzApiManagementAuthorizationServerClientSecret' cmdlet and 'Get-AzApiManagementAuthorizationServer' will not return client secret anymore.</span></span>
* <span data-ttu-id="1d1eb-711">새 'Get-AzApiManagementNamedValueSecretValue' cmdlet이 추가되었으며 'Get-AzApiManagementNamedValue'는 더 이상 비밀 값을 반환하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-711">Added new 'Get-AzApiManagementNamedValueSecretValue' cmdlet and 'Get-AzApiManagementNamedValue' will not return secret value.</span></span>
* <span data-ttu-id="1d1eb-712">새 'Get-AzApiManagementOpenIdConnectProviderClientSecret' cmdlet이 추가되었으며 'Get-AzApiManagementOpenIdConnectProvider'는 더 이상 클라이언트 암호를 반환하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-712">Added new 'Get-AzApiManagementOpenIdConnectProviderClientSecret' cmdlet and 'Get-AzApiManagementOpenIdConnectProvider' will not return client secret anymore.</span></span>
* <span data-ttu-id="1d1eb-713">새 'Get-AzApiManagementSubscriptionKey' cmdlet이 추가되었으며 'Get-AzApiManagementSubscription'은 더 이상 구독 키를 반환하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-713">Added new 'Get-AzApiManagementSubscriptionKey' cmdlet and 'Get-AzApiManagementSubscription' will not return subscription keys anymore.</span></span>
* <span data-ttu-id="1d1eb-714">새 'Get-AzApiManagementTenantAccessSecret' cmdlet이 추가되었으며 'Get-AzApiManagementTenantAccess'는 더 이상 키를 반환하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-714">Added new 'Get-AzApiManagementTenantAccessSecret' cmdlet and 'Get-AzApiManagementTenantAccess' will not return keys anymore.</span></span>
* <span data-ttu-id="1d1eb-715">새 'Get-AzApiManagementTenantGitAccessSecret' cmdlet이 추가되었으며 'Get-AzApiManagementTenantGitAccess'는 더 이상 키를 반환하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-715">Added new 'Get-AzApiManagementTenantGitAccessSecret' cmdlet and 'Get-AzApiManagementTenantGitAccess' will not return keys anymore.</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="1d1eb-716">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="1d1eb-716">Az.ApplicationInsights</span></span>
* <span data-ttu-id="1d1eb-717">매개 변수 추가: 'New-AzApplicationInsights'에 대한 'RetentionInDays' 'PublicNetworkAccessForIngestion' 'PublicNetworkAccessForQuery'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-717">Added Parameters: 'RetentionInDays' 'PublicNetworkAccessForIngestion' 'PublicNetworkAccessForQuery' for 'New-AzApplicationInsights'</span></span>
* <span data-ttu-id="1d1eb-718">'Update-AzApplicationInsights' cmdlet 작성</span><span class="sxs-lookup"><span data-stu-id="1d1eb-718">Created cmdlet 'Update-AzApplicationInsights'</span></span>
* <span data-ttu-id="1d1eb-719">연결된 스토리지 계정에 대한 cmdlet 작성</span><span class="sxs-lookup"><span data-stu-id="1d1eb-719">Created cmdlets for Linked Storage Account</span></span>

#### <a name="azbatch"></a><span data-ttu-id="1d1eb-720">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="1d1eb-720">Az.Batch</span></span>
* <span data-ttu-id="1d1eb-721">'Microsoft.Azure.Batch' SDK 버전 13.0.0 및 'Microsoft.Azure.Management.Batch' SDK 버전 9.0.0을 사용하도록 Az.Batch가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-721">Updated Az.Batch to use 'Microsoft.Azure.Batch' SDK version 13.0.0 and 'Microsoft.Azure.Management.Batch' SDK version 9.0.0.</span></span>
* <span data-ttu-id="1d1eb-722">새 '-CertificateKind' 매개 변수를 사용하여 'AzBatchCertificate'에 추가할 인증서 종류를 선택하는 기능이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-722">Added the ability to select the kind of certificate being added using the new '-CertificateKind' parameter to 'New-AzBatchCertificate'.</span></span>
* <span data-ttu-id="1d1eb-723">이전에 항상 ''였던 'ApplicationPackages' 속성이 'PSApplication'에서 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-723">Removed 'ApplicationPackages' property from 'PSApplication' which was previously always ''.</span></span>
  - <span data-ttu-id="1d1eb-724">이제 'Get-AzBatchApplicationPackage'를 사용하여 애플리케이션 내부의 특정 패키지를 검색할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-724">The specific packages inside of an application now can be retrieved using 'Get-AzBatchApplicationPackage'.</span></span> <span data-ttu-id="1d1eb-725">예를 들면 다음과 같습니다. 'Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication'.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-725">For example: 'Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication'.</span></span>
* <span data-ttu-id="1d1eb-726">'New-AzBatchPool'을 사용하여 풀을 만들 때 'PSImageReference'의 'VirtualMachineImageId' 속성은 이제 Shared Image Gallery 이미지만 참조할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-726">When creating a pool using 'New-AzBatchPool', the 'VirtualMachineImageId' property of 'PSImageReference' can now only refer to a Shared Image Gallery image.</span></span>
* <span data-ttu-id="1d1eb-727">'New-AzBatchPool'을 사용하여 풀을 만들 때 공용 IP 없이 'PSNetworkConfiguration'의 새 'PublicIPAddressConfiguration'을 사용하여 풀을 프로비저닝할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-727">When creating a pool using 'New-AzBatchPool', the pool can be provisioned without a public IP using the new 'PublicIPAddressConfiguration' property of 'PSNetworkConfiguration'.</span></span>
  - <span data-ttu-id="1d1eb-728">'PSNetworkConfiguration'의 'PublicIPs' 속성도 'PSPublicIPAddressConfiguration'으로 이동되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-728">The 'PublicIPs' property of 'PSNetworkConfiguration' has moved in to 'PSPublicIPAddressConfiguration' as well.</span></span> <span data-ttu-id="1d1eb-729">이 속성은 'IPAddressProvisioningType'이 'UserManaged'인 경우에만 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-729">This property can only be specified if 'IPAddressProvisioningType' is 'UserManaged'.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="1d1eb-730">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="1d1eb-730">Az.Compute</span></span>
* <span data-ttu-id="1d1eb-731">'Update-AzVM' cmdlet에 HostId 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="1d1eb-731">Added HostId parameter to 'Update-AzVM' cmdlet</span></span>
* <span data-ttu-id="1d1eb-732">'New-AzVMConfig', 'New-AzVmssConfig', 'Update-AzVmss', 'Set-AzVMOperatingSystem' 및 'Set-AzVmssOsProfile' cmdlet의 도움말 문서가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-732">Updated Help documents for 'New-AzVMConfig', 'New-AzVmssConfig', 'Update-AzVmss', 'Set-AzVMOperatingSystem' and 'Set-AzVmssOsProfile' cmdlets.</span></span>
* <span data-ttu-id="1d1eb-733">주요 변경 내용</span><span class="sxs-lookup"><span data-stu-id="1d1eb-733">Breaking changes</span></span>
    - <span data-ttu-id="1d1eb-734">'Get-AzVMImage' cmdlet에서 FilterExpression 매개 변수가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-734">FilterExpression parameter is removed from 'Get-AzVMImage' cmdlet.</span></span>
    - <span data-ttu-id="1d1eb-735">'New-AzVmssConfig', 'New-AzVMConfig' 및 'Update-AzVM' cmdlet에서 AssignIdentity 매개 변수가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-735">AssignIdentity parameter is removed from 'New-AzVmssConfig', 'New-AzVMConfig' and 'Update-AzVM' cmdlets.</span></span>
    - <span data-ttu-id="1d1eb-736">'New-AzVmssConfig' 및 'Update-AzVmss' cmdlet에서 AutomaticRepairMaxInstanceRepairsPercent가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-736">AutomaticRepairMaxInstanceRepairsPercent is removed from 'New-AzVmssConfig' and 'Update-AzVmss' cmdlets.</span></span>
    - <span data-ttu-id="1d1eb-737">ProximityPlacementGroup에서 AvailabilitySetsColocationStatus, VirtualMachinesColocationStatus 및 VirtualMachineScaleSetsColocationStatus 속성이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-737">AvailabilitySetsColocationStatus, VirtualMachinesColocationStatus and VirtualMachineScaleSetsColocationStatus properties are removed from ProximityPlacementGroup.</span></span>
    - <span data-ttu-id="1d1eb-738">AutomaticRepairsPolicy에서 MaxInstanceRepairsPercent 속성이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-738">MaxInstanceRepairsPercent property is removed from AutomaticRepairsPolicy.</span></span>
    - <span data-ttu-id="1d1eb-739">AvailabilitySets, VirtualMachines 및 VirtualMachineScaleSets 형식이 IList<SubResource>에서 IList<SubResourceWithColocationStatus>로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-739">The types of AvailabilitySets, VirtualMachines and VirtualMachineScaleSets are changed from IList<SubResource> to IList<SubResourceWithColocationStatus>.</span></span>
* <span data-ttu-id="1d1eb-740">'Get-AzVM' cmdlet에 대한 설명이 보다 정확하게 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-740">Description for 'Get-AzVM' cmdlet has been updated to better describe it.</span></span> 

#### <a name="azdatafactory"></a><span data-ttu-id="1d1eb-741">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="1d1eb-741">Az.DataFactory</span></span>
* <span data-ttu-id="1d1eb-742">Managed IR에서 데이터 흐름 런타임 속성의 CRUD를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-742">Supported CRUD of data flow runtime properties in Managed IR.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="1d1eb-743">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="1d1eb-743">Az.FrontDoor</span></span>
* <span data-ttu-id="1d1eb-744">Front Door 규칙 엔진 개체를 생성, 업데이트, 검색 및 삭제할 수 있는 새 cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="1d1eb-744">Added new cmdlets for creation, update, retreival, and deletion of Front Door Rules Engine object</span></span>
* <span data-ttu-id="1d1eb-745">Front Door 규칙 엔진 개체를 작성할 수 있는 도우미 cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="1d1eb-745">Added helper cmdlets for construction of Front Door Rules Engine object</span></span>
* <span data-ttu-id="1d1eb-746">Front Door 회람 규칙 개체에 대한 규칙 엔진 참조 추가</span><span class="sxs-lookup"><span data-stu-id="1d1eb-746">Added Rules Engine reference to Front Door Routing Rule object.</span></span>
* <span data-ttu-id="1d1eb-747">Front Door 백 엔드 개체에 Private Link 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="1d1eb-747">Added Private Link parameters to Front Door Backend object</span></span>

#### <a name="azfunctions"></a><span data-ttu-id="1d1eb-748">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="1d1eb-748">Az.Functions</span></span>
* <span data-ttu-id="1d1eb-749">''Az.Functions'' 모듈의 일반 공급</span><span class="sxs-lookup"><span data-stu-id="1d1eb-749">General availability of ''Az.Functions'' module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="1d1eb-750">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="1d1eb-750">Az.HDInsight</span></span>
* <span data-ttu-id="1d1eb-751">고객 관리형 키 디스크 암호화 지원</span><span class="sxs-lookup"><span data-stu-id="1d1eb-751">Supported Customer-managed key disk encryption.</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="1d1eb-752">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="1d1eb-752">Az.HealthcareApis</span></span>
* <span data-ttu-id="1d1eb-753">더 이상 액세스 정책이 기본적으로 현재 보안 주체로 설정되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-753">Access policies are no longer defaulted to the current principal</span></span>

#### <a name="aziothub"></a><span data-ttu-id="1d1eb-754">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="1d1eb-754">Az.IotHub</span></span>
* <span data-ttu-id="1d1eb-755">SQL과 비슷한 언어를 사용하여 정보를 검색하기 위해 IoT 허브에서 쿼리를 호출하는 cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-755">Added cmdlet to invoke a query in an IoT hub to retrieve information using a SQL-like language.</span></span>
* <span data-ttu-id="1d1eb-756">'Add-AzIotHubDevice'가 자식 디바이스 없는 에지 지원 디바이스를 만들 수 없는 문제 해결 [#11597]</span><span class="sxs-lookup"><span data-stu-id="1d1eb-756">Fix issue that 'Add-AzIotHubDevice' fails to create Edge Enabled Device without child devices [#11597]</span></span>
* <span data-ttu-id="1d1eb-757">IoT Hub, 디바이스 또는 모듈에 대한 SAS 토큰을 생성하는 cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-757">Added cmdlet to generate SAS token for Iot Hub, device or module.</span></span>
* <span data-ttu-id="1d1eb-758">구성 메트릭 쿼리를 호출하는 cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-758">Added cmdlet to invoke configuration metrics query.</span></span>
* <span data-ttu-id="1d1eb-759">IoT Edge 자동 배포를 대규모로 관리합니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-759">Manage IoT Edge automatic deployment at scale.</span></span> <span data-ttu-id="1d1eb-760">새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-760">New cmdlets are:</span></span>
    - <span data-ttu-id="1d1eb-761">'Add-AzIotHubDeployment'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-761">'Add-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="1d1eb-762">'Get-AzIotHubDeployment'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-762">'Get-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="1d1eb-763">'Remove-AzIotHubDeployment'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-763">'Remove-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="1d1eb-764">'Set-AzIotHubDeployment'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-764">'Set-AzIotHubDeployment'</span></span>
* <span data-ttu-id="1d1eb-765">IoT Edge 배포 메트릭 쿼리를 호출하는 cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-765">Added cmdlet to invoke an IoT Edge deployment metrics query.</span></span>
* <span data-ttu-id="1d1eb-766">지정된 에지 디바이스에 구성 콘텐츠를 적용하는 cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-766">Added cmdlet to apply the configuration content to the specified edge device.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="1d1eb-767">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="1d1eb-767">Az.KeyVault</span></span>
* <span data-ttu-id="1d1eb-768">다음 별칭 제거: 'New-AzKeyVaultCertificateAdministratorDetails' 및 'New-AzKeyVaultCertificateOrganizationDetails'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-768">Removed two aliases: 'New-AzKeyVaultCertificateAdministratorDetails' and 'New-AzKeyVaultCertificateOrganizationDetails'</span></span>
* <span data-ttu-id="1d1eb-769">키 자격 증명 모음을 만들 때 기본적으로 일시 삭제 사용</span><span class="sxs-lookup"><span data-stu-id="1d1eb-769">Enabled soft delete by default when creating a key vault</span></span>
* <span data-ttu-id="1d1eb-770">키 자격 증명 모음을 만들 때 특정 네트워크 위치의 액세스를 제어하도록 네트워크 규칙을 설정할 수 있음</span><span class="sxs-lookup"><span data-stu-id="1d1eb-770">Network rules can be set to govern the accessibility from specific network locations when creating a key vault</span></span>
* <span data-ttu-id="1d1eb-771">BYOK(Bring Your Own Key) 지원 추가</span><span class="sxs-lookup"><span data-stu-id="1d1eb-771">Added support to bring your own key (BYOK)</span></span>
    - <span data-ttu-id="1d1eb-772">'Add-AzKeyVaultKey'가 키 교환 키 생성 지원</span><span class="sxs-lookup"><span data-stu-id="1d1eb-772">'Add-AzKeyVaultKey' supports generating a key exchange key</span></span>
    - <span data-ttu-id="1d1eb-773">'Get-AzKeyVaultKey'가 PEM 형식의 공개 키 다운로드 지원</span><span class="sxs-lookup"><span data-stu-id="1d1eb-773">'Get-AzKeyVaultKey' supports downloading a public key in PEM format</span></span>
* <span data-ttu-id="1d1eb-774">'AzKeyVaultKey' 도움말 문서의 'KeyOps' 부분 업데이트</span><span class="sxs-lookup"><span data-stu-id="1d1eb-774">Updated the 'KeyOps' part of the help document of 'Add-AzKeyVaultKey'</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="1d1eb-775">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="1d1eb-775">Az.Monitor</span></span>
* <span data-ttu-id="1d1eb-776">'Set-AzDiagnosticSettings'의 버그 수정, 일부 범주에는 보존 정책이 적용되지 않음 [#11589]</span><span class="sxs-lookup"><span data-stu-id="1d1eb-776">Fixed bug for 'Set-AzDiagnosticSettings', retention policy won't apply to all categories [#11589]</span></span>
* <span data-ttu-id="1d1eb-777">메트릭 경고 V2에 WebTest를 사용하기 위한 조건 지원</span><span class="sxs-lookup"><span data-stu-id="1d1eb-777">Supported WebTest availability criteria for metric alert V2</span></span>
    - <span data-ttu-id="1d1eb-778">'New-AzMetricAlertRuleV2Criteria': webtest 사용 조건을 만드는 옵션 추가</span><span class="sxs-lookup"><span data-stu-id="1d1eb-778">'New-AzMetricAlertRuleV2Criteria': an option to create webtest availability criteria was added</span></span>
    - <span data-ttu-id="1d1eb-779">'Add-AzMetricAlertRuleV2': 새 webtest 사용 조건 지원</span><span class="sxs-lookup"><span data-stu-id="1d1eb-779">'Add-AzMetricAlertRuleV2': supports the new webtest availability criteria</span></span>
* <span data-ttu-id="1d1eb-780">PSLogProfile에서 RetentionPolicy에 대한 중복 정의 제거 [#7608]</span><span class="sxs-lookup"><span data-stu-id="1d1eb-780">Removed redundant definition for RetentionPolicy in PSLogProfile [#7608]</span></span>
* <span data-ttu-id="1d1eb-781">PSEventData에 정의된 중복 속성 제거 [#11353]</span><span class="sxs-lookup"><span data-stu-id="1d1eb-781">Removed redundant properties difined in PSEventData [#11353]</span></span>
* <span data-ttu-id="1d1eb-782">'Get-AzLog'를 'Get-AzActivityLog'로 이름 변경</span><span class="sxs-lookup"><span data-stu-id="1d1eb-782">Renamed 'Get-AzLog' to 'Get-AzActivityLog'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="1d1eb-783">Az.Network</span><span class="sxs-lookup"><span data-stu-id="1d1eb-783">Az.Network</span></span>
* <span data-ttu-id="1d1eb-784">영역 기본 동작이 변경된다는 것을 알리기 위해 주요 변경 특성을 추가</span><span class="sxs-lookup"><span data-stu-id="1d1eb-784">Added breaking change attribute to notify that Zone default behaviour will be changed</span></span>
    - <span data-ttu-id="1d1eb-785">'New-AzPublicIpAddress'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-785">'New-AzPublicIpAddress'</span></span>
    - <span data-ttu-id="1d1eb-786">'New-AzPublicIpPrefix'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-786">'New-AzPublicIpPrefix'</span></span>
    - <span data-ttu-id="1d1eb-787">'New-AzLoadBalancerFrontendIpConfig'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-787">'New-AzLoadBalancerFrontendIpConfig'</span></span>
* <span data-ttu-id="1d1eb-788">새로운 최상위 리소스 SecurityPartnerProvider에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="1d1eb-788">Added support for a new top level resource SecurityPartnerProvider</span></span>
    - <span data-ttu-id="1d1eb-789">추가된 새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-789">New cmdlets added:</span></span>
        - <span data-ttu-id="1d1eb-790">New-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="1d1eb-790">New-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="1d1eb-791">Remove-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="1d1eb-791">Remove-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="1d1eb-792">Get-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="1d1eb-792">Get-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="1d1eb-793">Set-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="1d1eb-793">Set-AzSecurityPartnerProvider</span></span>
* <span data-ttu-id="1d1eb-794">'PSPrivateEndpointConnection'의 'PSPrivateLinkResource' 및 'GroupId'에서 'RequiredZoneNames' 추가</span><span class="sxs-lookup"><span data-stu-id="1d1eb-794">Added 'RequiredZoneNames' on 'PSPrivateLinkResource' and 'GroupId' on 'PSPrivateEndpointConnection'</span></span>
* <span data-ttu-id="1d1eb-795">New-AzNetworkWatcherConnectionMonitorTestConfigurationObject에 대한 잘못된 형식의 SuccessThresholdRoundTripTimeMs 매개 변수 수정</span><span class="sxs-lookup"><span data-stu-id="1d1eb-795">Fixed incorrect type of SuccessThresholdRoundTripTimeMs parameter for New-AzNetworkWatcherConnectionMonitorTestConfigurationObject</span></span>
* <span data-ttu-id="1d1eb-796">AllowVnetToVnetTraffic 인수의 기본값을 True로 설정하도록 VirtualWan cmdlet 업데이트</span><span class="sxs-lookup"><span data-stu-id="1d1eb-796">Updated VirtualWan cmdlets to set default value of AllowVnetToVnetTraffic argument to True.</span></span>
    - <span data-ttu-id="1d1eb-797">'New-AzVirtualWan'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-797">'New-AzVirtualWan'</span></span>
    - <span data-ttu-id="1d1eb-798">'Update-AzVirtualWan'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-798">'Update-AzVirtualWan'</span></span>
* <span data-ttu-id="1d1eb-799">프라이빗 엔드포인트에 대한 DNS 영역 그룹을 지원하는 새 cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="1d1eb-799">Added new cmdlets to support DNS zone group for private endpoint</span></span>
    - <span data-ttu-id="1d1eb-800">'New-AzPrivateDnsZoneConfig'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-800">'New-AzPrivateDnsZoneConfig'</span></span>
    - <span data-ttu-id="1d1eb-801">'Get-AzPrivateDnsZoneGroup'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-801">'Get-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="1d1eb-802">'New-AzPrivateDnsZoneGroup'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-802">'New-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="1d1eb-803">'Set-AzPrivateDnsZoneGroup'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-803">'Set-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="1d1eb-804">'Remove-AzPrivateDnsZoneGroup'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-804">'Remove-AzPrivateDnsZoneGroup'</span></span>
* <span data-ttu-id="1d1eb-805">'AzureFirewall'에 'DNSEnableProxy', 'DNSRequireProxyForNetworkRules' 및 'DNSServers' 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="1d1eb-805">Added 'DNSEnableProxy', 'DNSRequireProxyForNetworkRules' and 'DNSServers' parameters to 'AzureFirewall'</span></span>
* <span data-ttu-id="1d1eb-806">'AzureFirewall'에 'EnableDnsProxy', 'DnsProxyNotRequiredForNetworkRule' 및 'DnsServer' 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="1d1eb-806">Added 'EnableDnsProxy', 'DnsProxyNotRequiredForNetworkRule' and 'DnsServer' parameters to 'AzureFirewall'</span></span>
    - <span data-ttu-id="1d1eb-807">업데이트된 cmdlet:</span><span class="sxs-lookup"><span data-stu-id="1d1eb-807">Updated cmdlet:</span></span>
        - <span data-ttu-id="1d1eb-808">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="1d1eb-808">New-AzFirewall</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="1d1eb-809">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="1d1eb-809">Az.OperationalInsights</span></span>
* <span data-ttu-id="1d1eb-810">새로 생성된 SDK를 적용하도록 레거시 코드 업데이트</span><span class="sxs-lookup"><span data-stu-id="1d1eb-810">Updated legacy code to apply new generated SDK</span></span>
* <span data-ttu-id="1d1eb-811">사용되지 않는 API 때문에 cmdlet 삭제</span><span class="sxs-lookup"><span data-stu-id="1d1eb-811">Deleted cmdlets due to deprecated APIs</span></span>
    - <span data-ttu-id="1d1eb-812">'Get-AzOperationalInsightsSavedSearchResult'(별칭 'Get-AzOperationalInsightsSavedSearchResults')</span><span class="sxs-lookup"><span data-stu-id="1d1eb-812">'Get-AzOperationalInsightsSavedSearchResult' (alias 'Get-AzOperationalInsightsSavedSearchResults')</span></span>
    - <span data-ttu-id="1d1eb-813">'Get-AzOperationalInsightsSearchResult'(별칭 'Get-AzOperationalInsightsSearchResults')</span><span class="sxs-lookup"><span data-stu-id="1d1eb-813">'Get-AzOperationalInsightsSearchResult' (alias 'Get-AzOperationalInsightsSearchResults')</span></span>
    - <span data-ttu-id="1d1eb-814">'Get-AzOperationalInsightsLinkTarget'(별칭 'Get-AzOperationalInsightsLinkTargets')</span><span class="sxs-lookup"><span data-stu-id="1d1eb-814">'Get-AzOperationalInsightsLinkTarget' (alias 'Get-AzOperationalInsightsLinkTargets')</span></span>
* <span data-ttu-id="1d1eb-815">'Set-AzOperationalInsightsWorkspace' 및 'New-AzOperationalInsightsWorkspace'에 대한 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="1d1eb-815">Added parameters for 'Set-AzOperationalInsightsWorkspace' and 'New-AzOperationalInsightsWorkspace'</span></span>
* <span data-ttu-id="1d1eb-816">연결된 스토리지 계정에 대한 cmdlet 작성</span><span class="sxs-lookup"><span data-stu-id="1d1eb-816">Created cmdlets for Linked Stoarge Account</span></span>
* <span data-ttu-id="1d1eb-817">클러스터 및 연결된 서비스에 대한 cmdlet 작성</span><span class="sxs-lookup"><span data-stu-id="1d1eb-817">Created cmdlets for Clusters and Linked Service</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="1d1eb-818">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="1d1eb-818">Az.RecoveryServices</span></span>
* <span data-ttu-id="1d1eb-819">Azure Site Recovery - Azure와 Azure 공급자 간 근접 배치 그룹 가상 머신을 보호하기 위한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-819">Azure Site Recovery added support for protecting proximity placement group virtual machines for Azure to Azure provider.</span></span>
* <span data-ttu-id="1d1eb-820">Azure Site Recovery - 영역 간 복제에 대한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-820">Azure Site Recovery added support for zone to zone replication.</span></span>
* <span data-ttu-id="1d1eb-821">Azure Backup - Azure 파일 공유 복구 지점의 장기 보존 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-821">Azure Backup Added Long term retention support for Azure FileShare Recovery Points.</span></span>
* <span data-ttu-id="1d1eb-822">Azure Backup - 'Get-AzRecoveryServicesBackupItem' cmdlet 출력에 디스크 제외 속성이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-822">Azure Backup Added disk exclusion properties to 'Get-AzRecoveryServicesBackupItem' cmdlet output.</span></span>
* <span data-ttu-id="1d1eb-823">사이트 복구 서비스용 Vault 자격 증명 파일에 대한 프라이빗 엔드포인트가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-823">Added private endpoint for Vault credential file for site recovery service.</span></span>

#### <a name="azresources"></a><span data-ttu-id="1d1eb-824">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="1d1eb-824">Az.Resources</span></span>
* <span data-ttu-id="1d1eb-825">새 역할 정의를 만들 때 보기 지연에 대한 메시지 경고 추가</span><span class="sxs-lookup"><span data-stu-id="1d1eb-825">Added message warning about view delay when creating a new Role Definition</span></span>
* <span data-ttu-id="1d1eb-826">강력한 형식의 개체를 출력하도록 정책 cmdlet 변경</span><span class="sxs-lookup"><span data-stu-id="1d1eb-826">Changed policy cmdlets to output strongly-typed objects</span></span>
* <span data-ttu-id="1d1eb-827">'Get-AzResourceLock' cmdlet에 사용되는 '-TenantLevel' 매개 변수 제거 [#11335]</span><span class="sxs-lookup"><span data-stu-id="1d1eb-827">Removed '-TenantLevel' parameter used for on the 'Get-AzResourceLock' cmdlet [#11335]</span></span>
* <span data-ttu-id="1d1eb-828">'Remove-AzResourceGroup -Id ResourceId' 수정[#9882]</span><span class="sxs-lookup"><span data-stu-id="1d1eb-828">Fixed 'Remove-AzResourceGroup -Id ResourceId'[#9882]</span></span>
* <span data-ttu-id="1d1eb-829">리소스 그룹 범위에서 ARM 템플릿 가상 시나리오 결과를 가져오는 새 cmdlet 추가: 'Get-AzDeploymentResourceGroupWhatIfResult'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-829">Added new cmdlet for getting ARM template What-If results at resource group scope: 'Get-AzDeploymentResourceGroupWhatIfResult'</span></span>
* <span data-ttu-id="1d1eb-830">구독 범위에서 ARM 템플릿 가상 시나리오 결과를 가져오는 새 cmdlet 추가: 'Get-AzDeploymentWhatIfResult'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-830">Added new cmdlet for getting ARM template What-If results at subscription scope: 'Get-AzDeploymentWhatIfResult'</span></span>
   - <span data-ttu-id="1d1eb-831">별칭: 'Get-AzSubscriptionDeploymentWhatIf'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-831">Alias: 'Get-AzSubscriptionDeploymentWhatIf'</span></span>
* <span data-ttu-id="1d1eb-832">ARM 템플릿 가상 시나리오 결과를 사용하도록 'New-AzDeployment' 및 'New-AzResourceGroupDeployment'에 대한 '-WhatIf' 및 '-Confirm' 매개 변수 재정의</span><span class="sxs-lookup"><span data-stu-id="1d1eb-832">Overrode '-WhatIf' and '-Confirm' parameters for 'New-AzDeployment' and 'New-AzResourceGroupDeployment' to use ARM template What-If results</span></span>
* <span data-ttu-id="1d1eb-833">배포 cmdlet에서 'ApiVersion' 매개 변수의 사용 중단 메시지 추가</span><span class="sxs-lookup"><span data-stu-id="1d1eb-833">Added deprecation message for 'ApiVersion' parameter in deployment cmdlets</span></span>
* <span data-ttu-id="1d1eb-834">배포 오류에 대한 향상된 오류 메시지를 표시하는 기능 추가</span><span class="sxs-lookup"><span data-stu-id="1d1eb-834">Added capability to show improved error messages for deployment failures</span></span>
* <span data-ttu-id="1d1eb-835">배포 오류에 대한 correlationId 로깅 추가</span><span class="sxs-lookup"><span data-stu-id="1d1eb-835">Added correlationId logging for deployment failures</span></span>
* <span data-ttu-id="1d1eb-836">배포 스크립트 출력에 'error' 속성 추가</span><span class="sxs-lookup"><span data-stu-id="1d1eb-836">Added 'error' property to the deployment script output</span></span>
* <span data-ttu-id="1d1eb-837">nuget Microsoft.Azure.Management.ResourceManager를 '3.7.1-preview'로 업데이트</span><span class="sxs-lookup"><span data-stu-id="1d1eb-837">Updated nuget Microsoft.Azure.Management.ResourceManager to '3.7.1-preview'</span></span>
* <span data-ttu-id="1d1eb-838">nuget 3.7.1-preview에서 DeploymentValidateResult의 Error 속성이 readonly로 변경되어 특정 테스트 사례를 제거</span><span class="sxs-lookup"><span data-stu-id="1d1eb-838">Removed specific test cases as Error property in DeploymentValidateResult has changed to readonly from nuget 3.7.1-preview</span></span>
* <span data-ttu-id="1d1eb-839">SDK ResourceManager 3.7.1-preview의 GenericResourceExpanded 도입</span><span class="sxs-lookup"><span data-stu-id="1d1eb-839">Brought GenericResourceExpanded from SDK ResourceManager 3.7.1-preview</span></span>
* <span data-ttu-id="1d1eb-840">모든 배포용 Get cmdlet에 대한 태그 지원 추가</span><span class="sxs-lookup"><span data-stu-id="1d1eb-840">Added tag support for all Get cmdlets for deployment, as well as</span></span>
    - <span data-ttu-id="1d1eb-841">'New-AzDeployment'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-841">'New-AzDeployment'</span></span>
    - <span data-ttu-id="1d1eb-842">'New-AzManagementGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-842">'New-AzManagementGroupDeployment'</span></span>
    - <span data-ttu-id="1d1eb-843">'New-AzResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-843">'New-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="1d1eb-844">'New-AzTenantDeployment'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-844">'New-AzTenantDeployment'</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="1d1eb-845">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="1d1eb-845">Az.ServiceFabric</span></span>
* <span data-ttu-id="1d1eb-846">잘못된 인증서 지문을 가져오는 --SecretIdentifier를 사용한 인증서 추가의 버그 수정</span><span class="sxs-lookup"><span data-stu-id="1d1eb-846">Fixed bug in add certificate using --SecretIdentifier that was getting the wrong certificate thumbprint</span></span>

#### <a name="azsql"></a><span data-ttu-id="1d1eb-847">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="1d1eb-847">Az.Sql</span></span>
* <span data-ttu-id="1d1eb-848">성능 강화:</span><span class="sxs-lookup"><span data-stu-id="1d1eb-848">Enhance performance of:</span></span>
    - <span data-ttu-id="1d1eb-849">'Set-AzSqlDatabaseSensitivityClassification'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-849">'Set-AzSqlDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="1d1eb-850">'Set-AzSqlInstanceDatabaseSensitivityClassification'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-850">'Set-AzSqlInstanceDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="1d1eb-851">'Remove-AzSqlDatabaseSensitivityClassification'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-851">'Remove-AzSqlDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="1d1eb-852">'Remove-AzSqlInstanceDatabaseSensitivityClassification'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-852">'Remove-AzSqlInstanceDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="1d1eb-853">'Enable-AzSqlDatabaseSensitivityRecommendation'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-853">'Enable-AzSqlDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="1d1eb-854">'Enable-AzSqlInstanceDatabaseSensitivityRecommendation'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-854">'Enable-AzSqlInstanceDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="1d1eb-855">'Disable-AzSqlDatabaseSensitivityRecommendation'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-855">'Disable-AzSqlDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="1d1eb-856">'Disable-AzSqlInstanceDatabaseSensitivityRecommendation'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-856">'Disable-AzSqlInstanceDatabaseSensitivityRecommendation'</span></span>
* <span data-ttu-id="1d1eb-857">'Set-AzSqlDatabaseBackupShortTermRetentionPolicy' cmdlet에서 'RetentionDays' 매개 변수의 클라이언트 쪽 유효성 검사 제거</span><span class="sxs-lookup"><span data-stu-id="1d1eb-857">Removed client-side validation of 'RetentionDays' parameter from cmdlet 'Set-AzSqlDatabaseBackupShortTermRetentionPolicy'</span></span>
* <span data-ttu-id="1d1eb-858">Vnet에서 스토리지 계정을 감사하고, Storage Blob 데이터 기여자 역할을 만들 때 발생하는 버그 수정</span><span class="sxs-lookup"><span data-stu-id="1d1eb-858">Auditing to a storage account in Vnet, fixing a bug when creating a Storage Blob Data Contributor role.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="1d1eb-859">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="1d1eb-859">Az.Storage</span></span>
* <span data-ttu-id="1d1eb-860">get/list account cmdlet 'Get-AzStorageAccount'에 '-AsJob' 추가</span><span class="sxs-lookup"><span data-stu-id="1d1eb-860">Added '-AsJob' to get/list account cmdlet 'Get-AzStorageAccount'</span></span>
* <span data-ttu-id="1d1eb-861">키 자동 회전을 지원하기 위해 스토리지 계정을 KeyvaultEncryption으로 업데이트할 때 KeyVersion을 선택 사항으로 지정</span><span class="sxs-lookup"><span data-stu-id="1d1eb-861">Make KeyVersion to optional when update Storage account with KeyvaultEncryption, to support key auto-rotation</span></span>
    - <span data-ttu-id="1d1eb-862">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-862">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="1d1eb-863">파이프라인을 사용하여 Azure 파일 디렉터리 제거 오류 수정</span><span class="sxs-lookup"><span data-stu-id="1d1eb-863">Fixed remove Azure File Directory fail with pipeline</span></span>
    - <span data-ttu-id="1d1eb-864">'Remove-AzStorageDirectory'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-864">'Remove-AzStorageDirectory'</span></span>
* <span data-ttu-id="1d1eb-865">수정 [#9880]: Swagger에 맞게 NetWorkRule DefaultAction 값 정의 변경</span><span class="sxs-lookup"><span data-stu-id="1d1eb-865">Fixed [#9880]: Change NetWorkRule DefaultAction value defination to align with swagger.</span></span>
    - <span data-ttu-id="1d1eb-866">'Update-AzStorageAccountNetworkRuleSet'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-866">'Update-AzStorageAccountNetworkRuleSet'</span></span>
    - <span data-ttu-id="1d1eb-867">'Get-AzStorageAccountNetworkRuleSet'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-867">'Get-AzStorageAccountNetworkRuleSet'</span></span>
* <span data-ttu-id="1d1eb-868">수정 [#11624]: 서버 오류를 방지하기 위해 NetworkRules를 추가할 때 중복 규칙 건너뛰기</span><span class="sxs-lookup"><span data-stu-id="1d1eb-868">Fixed [#11624]: Skip duplicated rules when add NetworkRules, to avoid server failure</span></span>
    - <span data-ttu-id="1d1eb-869">'Add-AzStorageAccountNetworkRule'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-869">'Add-AzStorageAccountNetworkRule'</span></span>
* <span data-ttu-id="1d1eb-870">Microsoft.Azure.Cosmos.Table SDK를 1.0.7로 업그레이드</span><span class="sxs-lookup"><span data-stu-id="1d1eb-870">Upgraded Microsoft.Azure.Cosmos.Table SDK to 1.0.7</span></span>
* <span data-ttu-id="1d1eb-871">DataLake Gen2 항목 목록에 부품 항목만 반환되는 경우 ContinuationToken을 사용하여 다시 나열하라고 사용자에게 알리는 경고 메시지 추가</span><span class="sxs-lookup"><span data-stu-id="1d1eb-871">Added a warning message to remind user to list again with ContinuationToken when only part items are returned in list DataLake Gen2 Items,</span></span>
    - <span data-ttu-id="1d1eb-872">'Get-AzDataLakeGen2ChildItem'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-872">'Get-AzDataLakeGen2ChildItem'</span></span>
* <span data-ttu-id="1d1eb-873">Azure Files Active Directory 도메인 서비스 인증을 사용하여 스토리지 계정을 만들거나 업데이트하는 기능 지원</span><span class="sxs-lookup"><span data-stu-id="1d1eb-873">Supported to create or update Storage account with Azure Files Active Directory Domain Service Authentication</span></span>
    -  <span data-ttu-id="1d1eb-874">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-874">'New-AzStorageAccount'</span></span>
    -  <span data-ttu-id="1d1eb-875">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-875">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="1d1eb-876">스토리지 계정의 Kerberos 키 새로 만들기 또는 나열 지원</span><span class="sxs-lookup"><span data-stu-id="1d1eb-876">Supported to new or list Kerberos keys of Storage account</span></span>
    -  <span data-ttu-id="1d1eb-877">'New-AzStorageAccountKey'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-877">'New-AzStorageAccountKey'</span></span>
    -  <span data-ttu-id="1d1eb-878">'Get-AzStorageAccountKey'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-878">'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="1d1eb-879">스토리지 계정 장애 조치(failover) 지원</span><span class="sxs-lookup"><span data-stu-id="1d1eb-879">Supported failover Storage account</span></span>
    - <span data-ttu-id="1d1eb-880">'Invoke-AzStorageAccountFailover'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-880">'Invoke-AzStorageAccountFailover'</span></span>
* <span data-ttu-id="1d1eb-881">'Get-AzStorageBlobCopyState'의 도움말 업데이트</span><span class="sxs-lookup"><span data-stu-id="1d1eb-881">Updated help of 'Get-AzStorageBlobCopyState'</span></span>
* <span data-ttu-id="1d1eb-882">'Get-AzStorageFileCopyState' 및 'Start-AzStorageBlobCopy'의 도움말 업데이트</span><span class="sxs-lookup"><span data-stu-id="1d1eb-882">Updated help of 'Get-AzStorageFileCopyState' and 'Start-AzStorageBlobCopy'</span></span>
* <span data-ttu-id="1d1eb-883">스토리지 클라이언트 라이브러리 v12를 큐 및 파일 cmdlet에 통합</span><span class="sxs-lookup"><span data-stu-id="1d1eb-883">Integrated Storage client library v12 to Queue and File cmdlets</span></span>
* <span data-ttu-id="1d1eb-884">출력 형식을 CloudFile에서 AzureStorageFile로 변경했으며, 원래 출력은 새 출력의 자식 속성이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-884">Changed output type from CloudFile to AzureStorageFile, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="1d1eb-885">'Get-AzStorageFile'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-885">'Get-AzStorageFile'</span></span>
    - <span data-ttu-id="1d1eb-886">'Remove-AzStorageFile'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-886">'Remove-AzStorageFile'</span></span>
    - <span data-ttu-id="1d1eb-887">'Get-AzStorageFileContent'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-887">'Get-AzStorageFileContent'</span></span>
    - <span data-ttu-id="1d1eb-888">'Set-AzStorageFileContent'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-888">'Set-AzStorageFileContent'</span></span>
    - <span data-ttu-id="1d1eb-889">'Start-AzStorageFileCopy'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-889">'Start-AzStorageFileCopy'</span></span>
* <span data-ttu-id="1d1eb-890">출력 형식을 CloudFileDirectory에서 AzureStorageFileDirectory로 변경했으며, 원래 출력은 새 출력의 자식 속성이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-890">Changed output type from CloudFileDirectory to AzureStorageFileDirectory, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="1d1eb-891">'New-AzStorageDirectory'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-891">'New-AzStorageDirectory'</span></span>
    - <span data-ttu-id="1d1eb-892">'Remove-AzStorageDirectory'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-892">'Remove-AzStorageDirectory'</span></span>
* <span data-ttu-id="1d1eb-893">출력 형식을 CloudFileShare에서 AzureStorageFileShare로 변경했으며, 원래 출력은 새 출력의 자식 속성이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-893">Changed output type from CloudFileShare to AzureStorageFileShare, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="1d1eb-894">'Get-AzStorageShare'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-894">'Get-AzStorageShare'</span></span>
    - <span data-ttu-id="1d1eb-895">'New-AzStorageShare'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-895">'New-AzStorageShare'</span></span>
    - <span data-ttu-id="1d1eb-896">'Remove-AzStorageShare'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-896">'Remove-AzStorageShare'</span></span>
* <span data-ttu-id="1d1eb-897">출력 형식을 FileShareProperties에서 AzureStorageFileShare로 변경했으며, 원래 출력은 새 출력의 하위 자식 속성이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-897">Changed output type from FileShareProperties to AzureStorageFileShare, the original output will become a sub child property of the new output</span></span>
    - <span data-ttu-id="1d1eb-898">'Set-AzStorageShareQuota'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-898">'Set-AzStorageShareQuota'</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="1d1eb-899">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="1d1eb-899">Az.TrafficManager</span></span>
* <span data-ttu-id="1d1eb-900">'DisableAzureTrafficManagerEndpoint' 자세한 정보 출력에서 잘못된 프로필 이름 수정</span><span class="sxs-lookup"><span data-stu-id="1d1eb-900">Fixed incorrect profile name in 'DisableAzureTrafficManagerEndpoint' verbose output</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="1d1eb-901">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="1d1eb-901">Az.Websites</span></span>
* <span data-ttu-id="1d1eb-902">'Update-AzWebAppAccessRestrictionConfig'의 도움말에서 철자 오류 수정</span><span class="sxs-lookup"><span data-stu-id="1d1eb-902">Fixed typo on help of 'Update-AzWebAppAccessRestrictionConfig'.</span></span>

## <a name="380---april-2020"></a><span data-ttu-id="1d1eb-903">3.8.0 - 2020년 4월</span><span class="sxs-lookup"><span data-stu-id="1d1eb-903">3.8.0 - April 2020</span></span>
### <a name="highlights-since-the-last-release"></a><span data-ttu-id="1d1eb-904">마지막 릴리스 이후의 주요 사항</span><span class="sxs-lookup"><span data-stu-id="1d1eb-904">Highlights since the last release</span></span>
* <span data-ttu-id="1d1eb-905">Az.Storage에서 지원하는 PowerShell 버전: Windows PowerShell 5.1, PowerShell Core 6.2.4 이상, PowerShell 7</span><span class="sxs-lookup"><span data-stu-id="1d1eb-905">PowerShell versions that Az.Storage supports: Windows PowerShell 5.1, PowerShell Core 6.2.4+, PowerShell 7</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="1d1eb-906">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="1d1eb-906">Az.Accounts</span></span>
* <span data-ttu-id="1d1eb-907">'Resolve-AzError'에서 Azure PowerShell 설문 조사 URL이 업데이트되었습니다. [#11507]</span><span class="sxs-lookup"><span data-stu-id="1d1eb-907">Updated Azure PowerShell survey URL in 'Resolve-AzError' [#11507]</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="1d1eb-908">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="1d1eb-908">Az.ApiManagement</span></span>
* <span data-ttu-id="1d1eb-909">향후 릴리스의 Azure File cmdlet 출력 변경에 대한 호환성이 손상되는 변경 공지가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-909">Added breaking change notice for Azure File cmdlets output change in a future release</span></span>
* <span data-ttu-id="1d1eb-910">'Set-AzApiManagementGroup' - GroupId 매개 변수를 지정하도록 설명서가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-910">'Set-AzApiManagementGroup' Updated documentation to specify the GroupId parameter</span></span>

#### <a name="azcdn"></a><span data-ttu-id="1d1eb-911">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="1d1eb-911">Az.Cdn</span></span>
* <span data-ttu-id="1d1eb-912">ChinaCDN 관련 가격 책정 SKU 표시가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-912">Fixed ChinaCDN related pricing SKU display</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="1d1eb-913">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="1d1eb-913">Az.CognitiveServices</span></span>
* <span data-ttu-id="1d1eb-914">Identity, Encryption, UserOwnedStorage가 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-914">Supported Identity, Encryption, UserOwnedStorage</span></span>

#### <a name="azcompute"></a><span data-ttu-id="1d1eb-915">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="1d1eb-915">Az.Compute</span></span>
* <span data-ttu-id="1d1eb-916">'Set-AzVmssOrchestrationServiceState' cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-916">Added 'Set-AzVmssOrchestrationServiceState' cmdlet.</span></span>
* <span data-ttu-id="1d1eb-917">-InstanceView가 있는 'Get-AzVmss'는 OrchestrationService 상태를 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-917">'Get-AzVmss' with -InstanceView shows OrchestrationService states.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="1d1eb-918">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="1d1eb-918">Az.IotHub</span></span>
* <span data-ttu-id="1d1eb-919">IoT 디바이스 쌍 구성을 관리합니다. 새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-919">Manage IoT device twin configuration, New cmdlets are:</span></span>
    - <span data-ttu-id="1d1eb-920">'Get-AzIotHubDeviceTwin'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-920">'Get-AzIotHubDeviceTwin'</span></span>
    - <span data-ttu-id="1d1eb-921">'Update-AzIotHubDeviceTwin'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-921">'Update-AzIotHubDeviceTwin'</span></span>
* <span data-ttu-id="1d1eb-922">IoT Hub에서 디바이스에 대한 직접 메서드를 호출하는 cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-922">Added cmdlet to invoke direct method on a device in an Iot Hub.</span></span>
* <span data-ttu-id="1d1eb-923">IoT 디바이스 모듈 쌍 구성을 관리합니다. 새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-923">Manage IoT device module twin configuration, New cmdlets are:</span></span>
    - <span data-ttu-id="1d1eb-924">'Get-AzIotHubModuleTwin'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-924">'Get-AzIotHubModuleTwin'</span></span>
    - <span data-ttu-id="1d1eb-925">'Update-AzIotHubModuleTwin'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-925">'Update-AzIotHubModuleTwin'</span></span>
* <span data-ttu-id="1d1eb-926">IoT 자동 디바이스 관리 구성을 대규모로 관리합니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-926">Manage IoT automatic device management configuration at scale.</span></span> <span data-ttu-id="1d1eb-927">새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-927">New cmdlets are:</span></span>
    - <span data-ttu-id="1d1eb-928">'Add-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-928">'Add-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="1d1eb-929">'Get-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-929">'Get-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="1d1eb-930">'Remove-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-930">'Remove-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="1d1eb-931">'Set-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-931">'Set-AzIotHubConfiguration'</span></span>
* <span data-ttu-id="1d1eb-932">Iot Hub에서 에지 모듈 메서드를 호출하는 cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-932">Added cmdlet to invoke an edge module method in an Iot Hub.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="1d1eb-933">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="1d1eb-933">Az.KeyVault</span></span>
* <span data-ttu-id="1d1eb-934">자격 증명 모음에서 일시 삭제 및 제거 보호를 사용하도록 설정할 수 있는 새 cmdlet 'Update-AzKeyVault'가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-934">Added a new cmdlet 'Update-AzKeyVault' that can enable soft delete and purge protection on a vault</span></span>
* <span data-ttu-id="1d1eb-935">Microsoft.PowerShell.SecretManagement에 대한 지원이 추가되었습니다. [#11178]</span><span class="sxs-lookup"><span data-stu-id="1d1eb-935">Added support to Microsoft.PowerShell.SecretManagement [#11178]</span></span>
* <span data-ttu-id="1d1eb-936">'Remove-AzKeyVaultManagedStorageSasDefinition' 예제의 오류가 해결되었습니다. [#11479]</span><span class="sxs-lookup"><span data-stu-id="1d1eb-936">Fixed error in the examples of 'Remove-AzKeyVaultManagedStorageSasDefinition' [#11479]</span></span>
* <span data-ttu-id="1d1eb-937">프라이빗 엔드포인트에 대한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-937">Added support to private endpoint</span></span>

#### <a name="azmaintenance"></a><span data-ttu-id="1d1eb-938">Az.Maintenance</span><span class="sxs-lookup"><span data-stu-id="1d1eb-938">Az.Maintenance</span></span>
* <span data-ttu-id="1d1eb-939">GA용 유지 관리 cmdlet의 릴리스 버전 게시</span><span class="sxs-lookup"><span data-stu-id="1d1eb-939">Publishing release version of Maintenance cmdlets for GA</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="1d1eb-940">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="1d1eb-940">Az.Monitor</span></span>
* <span data-ttu-id="1d1eb-941">프라이빗 링크 범위용 cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-941">Added cmdlets for private link scope</span></span>
    - <span data-ttu-id="1d1eb-942">'Get-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-942">'Get-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="1d1eb-943">'Remove-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-943">'Remove-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="1d1eb-944">'New-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-944">'New-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="1d1eb-945">'Update-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-945">'Update-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="1d1eb-946">'Get-AzInsightsPrivateLinkScopedResource'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-946">'Get-AzInsightsPrivateLinkScopedResource'</span></span>
    - <span data-ttu-id="1d1eb-947">'New-AzInsightsPrivateLinkScopedResource'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-947">'New-AzInsightsPrivateLinkScopedResource'</span></span>
    - <span data-ttu-id="1d1eb-948">'Remove-AzInsightsPrivateLinkScopedResource'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-948">'Remove-AzInsightsPrivateLinkScopedResource'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="1d1eb-949">Az.Network</span><span class="sxs-lookup"><span data-stu-id="1d1eb-949">Az.Network</span></span>
* <span data-ttu-id="1d1eb-950">Virtual Network 게이트웨이의 개인 IP에 대한 연결을 사용하도록 설정하는 cmdlet이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-950">Updated cmdlets to enable connection on private IP for Virtual Network Gateway.</span></span>
    - <span data-ttu-id="1d1eb-951">'New-AzVirtualNetworkGateway'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-951">'New-AzVirtualNetworkGateway'</span></span>
    - <span data-ttu-id="1d1eb-952">'Set-AzVirtualNetworkGateway'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-952">'Set-AzVirtualNetworkGateway'</span></span>
    - <span data-ttu-id="1d1eb-953">'New-AzVirtualNetworkGatewayConnection'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-953">'New-AzVirtualNetworkGatewayConnection'</span></span>
    - <span data-ttu-id="1d1eb-954">'Set-AzVirtualNetworkGatewayConnection'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-954">'Set-AzVirtualNetworkGatewayConnection'</span></span>
* <span data-ttu-id="1d1eb-955">FQDN 기반 LocalNetworkGateways 및 VpnSites를 사용하도록 설정하는 cmdlet이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-955">Updated cmdlets to enable FQDN based LocalNetworkGateways and VpnSites</span></span>
    - <span data-ttu-id="1d1eb-956">'New-AzLocalNetworkGateway'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-956">'New-AzLocalNetworkGateway'</span></span>
    - <span data-ttu-id="1d1eb-957">'New-AzVpnSiteLink'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-957">'New-AzVpnSiteLink'</span></span>
* <span data-ttu-id="1d1eb-958">ExpressRouteCircuitConnectionConfig(Global Reach)의 IPv6 주소 패밀리에 대한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-958">Added support for IPv6 address family in ExpressRouteCircuitConnectionConfig (Global Reach)</span></span>
    - <span data-ttu-id="1d1eb-959">'Set-AzExpressRouteCircuitConnectionConfig'가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-959">Added 'Set-AzExpressRouteCircuitConnectionConfig'</span></span>
        - <span data-ttu-id="1d1eb-960">IPv6CircuitConnectionProperties를 포함한 모든 기존 속성을 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-960">allows setting of all the existing properties including the IPv6CircuitConnectionProperties</span></span>
    - <span data-ttu-id="1d1eb-961">'Add-AzExpressRouteCircuitConnectionConfig'가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-961">Updated 'Add-AzExpressRouteCircuitConnectionConfig'</span></span>
        - <span data-ttu-id="1d1eb-962">주소 접두사의 주소 패밀리를 지정하는 또 다른 선택적 매개 변수 AddressPrefixType이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-962">Added another optional parameter AddressPrefixType to specify the address family of address prefix</span></span>
* <span data-ttu-id="1d1eb-963">Virtual Network 게이트웨이 연결에서 DPD 시간 제한 설정을 사용하도록 cmdlet이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-963">Updated cmdlets to enable setting of DPD Timeout on Virtual Network Gateway Connections.</span></span>
    - <span data-ttu-id="1d1eb-964">New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="1d1eb-964">New-AzVirtualNetworkGatewayConnection</span></span>
    - <span data-ttu-id="1d1eb-965">Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="1d1eb-965">Set-AzVirtualNetworkGatewayConnection</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="1d1eb-966">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="1d1eb-966">Az.PolicyInsights</span></span>
* <span data-ttu-id="1d1eb-967">정책 준수 검사를 트리거하기 위한 'Start-AzPolicyComplianceScan' cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-967">Added 'Start-AzPolicyComplianceScan' cmdlet for triggering policy compliance scans</span></span>
* <span data-ttu-id="1d1eb-968">'Get-AzPolicyState' 출력에 정책 정의, 집합 정의 및 할당 버전이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-968">Added policy definition, set definition, and assignment versions to 'Get-AzPolicyState' output</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="1d1eb-969">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="1d1eb-969">Az.ServiceFabric</span></span>
* <span data-ttu-id="1d1eb-970">'New-AzServiceFabricCluster' 예제의 코드 서식 및 사용 편의성이 개선되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-970">Improved code formatting and usability of 'New-AzServiceFabricCluster' examples</span></span>

#### <a name="azsql"></a><span data-ttu-id="1d1eb-971">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="1d1eb-971">Az.Sql</span></span>
* <span data-ttu-id="1d1eb-972">'Get-AzSqlInstanceOperation' 및 'Stop-AzSqlInstanceOperation' cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-972">Added cmdlets 'Get-AzSqlInstanceOperation' and 'Stop-AzSqlInstanceOperation'</span></span>
* <span data-ttu-id="1d1eb-973">VNet에서 스토리지 계정에 대한 감사가 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-973">Supported auditing to a storage account in VNet.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="1d1eb-974">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="1d1eb-974">Az.Storage</span></span>
* <span data-ttu-id="1d1eb-975">향후 릴리스의 Azure File cmdlet 출력 변경에 대한 호환성이 손상되는 변경 공지가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-975">Added breaking change notice for Azure File cmdlets output change in a future release</span></span>
* <span data-ttu-id="1d1eb-976">스토리지 계정 생성/업데이트 시 새로운 SkuName StandardGZRS, StandardRAGZRS가 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-976">Supported new SkuName StandardGZRS, StandardRAGZRS when create/update Storage account</span></span>
    - <span data-ttu-id="1d1eb-977">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-977">'New-AzStorageAccount'</span></span>
    - <span data-ttu-id="1d1eb-978">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-978">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="1d1eb-979">DataLake Gen2가 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-979">Supported DataLake Gen2</span></span>
    - <span data-ttu-id="1d1eb-980">'New-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-980">'New-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="1d1eb-981">'Get-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-981">'Get-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="1d1eb-982">'Get-AzDataLakeGen2ChildItem'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-982">'Get-AzDataLakeGen2ChildItem'</span></span>
    - <span data-ttu-id="1d1eb-983">'Move-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-983">'Move-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="1d1eb-984">'Set-AzDataLakeGen2ItemAclObject'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-984">'Set-AzDataLakeGen2ItemAclObject'</span></span>
    - <span data-ttu-id="1d1eb-985">'Update-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-985">'Update-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="1d1eb-986">'Get-AzDataLakeGen2ItemContent'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-986">'Get-AzDataLakeGen2ItemContent'</span></span>
    - <span data-ttu-id="1d1eb-987">'Remove-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-987">'Remove-AzDataLakeGen2Item'</span></span>

## <a name="0100-preview---april-2020"></a><span data-ttu-id="1d1eb-988">0.10.0-preview - 2020년 4월</span><span class="sxs-lookup"><span data-stu-id="1d1eb-988">0.10.0-preview - April 2020</span></span>
### <a name="general"></a><span data-ttu-id="1d1eb-989">일반</span><span class="sxs-lookup"><span data-stu-id="1d1eb-989">General</span></span>
* <span data-ttu-id="1d1eb-990">이제 Az 모듈이 Azure Stack Hub에서 미리 보기로 제공됩니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-990">Az modules is now available in preview on Azure Stack Hub.</span></span> <span data-ttu-id="1d1eb-991">따라서 Linux 및 macOS와의 플랫폼 간 호환성이 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-991">This allows for cross-platform compatibility with Linux and macOs.</span></span> <span data-ttu-id="1d1eb-992">Azure Stack Hub는 이제 Az 모듈을 사용하여 PowerShell Core를 지원합니다. 자세한 내용은 [여기](https://aka.ms/az4AzureStack)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-992">Azure Stack Hub now supports PowerShell core with the Az modules, more information [here](https://aka.ms/az4AzureStack)</span></span>
* <span data-ttu-id="1d1eb-993">Az 모듈은 2019-03-01-hybrid 프로필을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-993">Az modules support profile 2019-03-01-hybrid:</span></span>
  - <span data-ttu-id="1d1eb-994">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="1d1eb-994">Az.Billing</span></span>
  - <span data-ttu-id="1d1eb-995">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="1d1eb-995">Az.Compute</span></span>
  - <span data-ttu-id="1d1eb-996">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="1d1eb-996">Az.DataBoxEdge</span></span>
  - <span data-ttu-id="1d1eb-997">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="1d1eb-997">Az.EventHub</span></span>
  - <span data-ttu-id="1d1eb-998">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="1d1eb-998">Az.IotHub</span></span>
  - <span data-ttu-id="1d1eb-999">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="1d1eb-999">Az.KeyVault</span></span>
  - <span data-ttu-id="1d1eb-1000">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1000">Az.Monitor</span></span>
  - <span data-ttu-id="1d1eb-1001">Az.Network</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1001">Az.Network</span></span>
  - <span data-ttu-id="1d1eb-1002">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1002">Az.Resources</span></span>
  - <span data-ttu-id="1d1eb-1003">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1003">Az.Storage</span></span>
  - <span data-ttu-id="1d1eb-1004">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1004">Az.Websites</span></span>
* <span data-ttu-id="1d1eb-1005">Azure Stack Hub와 함께 작동하는 az용 새 PowerShell 모듈 3개(Az.Databox, Az.IotHub 및 Az.EventHub)가 도입되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1005">Three new PowerShell modules for az have been introduced that work with Azure Stack Hub, which are Az.Databox, Az.IotHub, and Az.EventHub</span></span>
* <span data-ttu-id="1d1eb-1006">AzureRM을 Az로 변경하는 것과 같은 사소한 변경을 수행하면 명령이 비교적 동일하게 유지됩니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1006">Commands remain relatively the same, with minor changes such as changing AzureRM to Az</span></span>
* <span data-ttu-id="1d1eb-1007">Azure Stack Hub에 대한 PowerShell 설명서의 업데이트된 링크는 [여기](https://aka.ms/InstallASHPowerShell)에서 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1007">Updated link to PowerShell documentation for Azure Stack Hub can be found [here](https://aka.ms/InstallASHPowerShell)</span></span>

## <a name="370---march-2020"></a><span data-ttu-id="1d1eb-1008">3.7.0 - 2020년 3월</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1008">3.7.0 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="1d1eb-1009">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1009">Az.Accounts</span></span>
* <span data-ttu-id="1d1eb-1010">로그인하지 않을 때 'Get-AzTenant'/'Get-AzDefault'/'Set-AzDefault'에서 NullReferenceException이 발생하는 문제가 해결되었습니다. [# 10292]</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1010">Fixed 'Get-AzTenant'/'Get-AzDefault'/'Set-AzDefault' throw NullReferenceException when not login [#10292]</span></span>

#### <a name="azcompute"></a><span data-ttu-id="1d1eb-1011">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1011">Az.Compute</span></span>
* <span data-ttu-id="1d1eb-1012">'New-AzDiskConfig' cmdlet에 다음 매개 변수를 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1012">Added the following parameters to 'New-AzDiskConfig' cmdlet:</span></span>
    - <span data-ttu-id="1d1eb-1013">DiskIOPSReadOnly, DiskMBpsReadOnly, MaxSharesCount, GalleryImageReference</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1013">DiskIOPSReadOnly, DiskMBpsReadOnly, MaxSharesCount, GalleryImageReference</span></span>
* <span data-ttu-id="1d1eb-1014">암호화 속성이 'New-AzGalleryImageVersion'cmdlet의 대상 매개 변수에 허용되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1014">Allowed Encryption property to Target parameter of 'New-AzGalleryImageVersion' cmdlet.</span></span>
* <span data-ttu-id="1d1eb-1015">'Set-AzVmss'-Reimage 및 'Invoke-AzVMReimage'cmdlet에 대한 tempDisk 이슈가 해결되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1015">Fixed tempDisk issue for 'Set-AzVmss' -Reimage and 'Invoke-AzVMReimage' cmdlets.</span></span> <span data-ttu-id="1d1eb-1016">[#11354]</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1016">[#11354]</span></span>
* <span data-ttu-id="1d1eb-1017">새로운 SAP 확장을 위해 아래 cmdlet에 대한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1017">Added support to below cmdlets for new SAP Extension</span></span>
    - <span data-ttu-id="1d1eb-1018">'Set-AzVMAEMExtension'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1018">'Set-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="1d1eb-1019">'Get-AzVMAEMExtension'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1019">'Get-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="1d1eb-1020">'Remove-AzVMAEMExtension'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1020">'Remove-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="1d1eb-1021">'Update-AzVMAEMExtension'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1021">'Update-AzVMAEMExtension'</span></span>
* <span data-ttu-id="1d1eb-1022">도움말 문서의 예제에서 오류가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1022">Fixed errors in examples of help document</span></span>
* <span data-ttu-id="1d1eb-1023">VM PowerState의 정확한 문자열 값을 테이블 형식으로 표시했습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1023">Showed the exact string value for VM PowerState in the table format.</span></span>
* <span data-ttu-id="1d1eb-1024">'New-AzVmssConfig': SinglePlacementGroup이 비활성화된 경우 AutomaticRepairs 속성의 직렬화가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1024">'New-AzVmssConfig': fixed serialization of AutomaticRepairs property when SinglePlacementGroup is disabled.</span></span> <span data-ttu-id="1d1eb-1025">[#11257]</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1025">[#11257]</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="1d1eb-1026">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1026">Az.DataFactory</span></span>
* <span data-ttu-id="1d1eb-1027">ADF .Net SDK 버전이 4.8.0으로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1027">Updated ADF .Net SDK version to 4.8.0</span></span>
* <span data-ttu-id="1d1eb-1028">재실행을 지원하기 위해 'Invoke-AzDataFactoryV2Pipeline' 명령에 선택적 매개 변수를 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1028">Added optional parameters to 'Invoke-AzDataFactoryV2Pipeline' command to support rerun</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="1d1eb-1029">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1029">Az.DataLakeStore</span></span>
* <span data-ttu-id="1d1eb-1030">'Export-AzDataLakeStoreItem' 및 'Import-AzDataLakeStoreItem'에 대해 호환성이 손상되는 변경 설명을 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1030">Added breaking change description for 'Export-AzDataLakeStoreItem' and 'Import-AzDataLakeStoreItem'</span></span>
* <span data-ttu-id="1d1eb-1031">'New-AzDataLakeStoreItem', 'Add-AzDAtaLakeStoreItemContent' 및 'Get-AzDAtaLakeStoreItemContent'에 대한 바이트 인코딩 옵션이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1031">Added option of Byte encoding for 'New-AzDataLakeStoreItem', 'Add-AzDAtaLakeStoreItemContent', and 'Get-AzDAtaLakeStoreItemContent'</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="1d1eb-1032">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1032">Az.HDInsight</span></span>
* <span data-ttu-id="1d1eb-1033">클러스터 생성 시 최소 지원 TLS 버전 지정이 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1033">Supported specifying minimal supported TLS version when creating cluster.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="1d1eb-1034">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1034">Az.IotHub</span></span>
* <span data-ttu-id="1d1eb-1035">디바이스별 분산 설정을 관리하기 위한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1035">Added support to manage distributed settings per-device.</span></span> <span data-ttu-id="1d1eb-1036">새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1036">New Cmdlets are:</span></span>
    - <span data-ttu-id="1d1eb-1037">'Get-AzIotHubDistributedTracing'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1037">'Get-AzIotHubDistributedTracing'</span></span>
    - <span data-ttu-id="1d1eb-1038">'Set-AzIotHubDistributedTracing'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1038">'Set-AzIotHubDistributedTracing'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="1d1eb-1039">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1039">Az.KeyVault</span></span>
* <span data-ttu-id="1d1eb-1040">'New-AzKeyVault'에 대해 호환성이 손상되는 변경 속성이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1040">Added breaking change attributes to 'New-AzKeyVault'</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="1d1eb-1041">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1041">Az.Monitor</span></span>
* <span data-ttu-id="1d1eb-1042">'New-AzScheduledQueryRuleLogMetricTrigger'에 대한 설명서가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1042">Updated documentation for 'New-AzScheduledQueryRuleLogMetricTrigger'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="1d1eb-1043">Az.Network</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1043">Az.Network</span></span>
* <span data-ttu-id="1d1eb-1044">교차 테넌트 VirtualHubVnetConnections를 허용하도록 cmdlet이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1044">Updated cmdlets to allow cross-tenant VirtualHubVnetConnections</span></span>
    - <span data-ttu-id="1d1eb-1045">'New-AzVirtualHubVnetConnection'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1045">'New-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="1d1eb-1046">'Update-AzVirtualHubVnetConnection'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1046">'Update-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="1d1eb-1047">'New-AzVirtualHub'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1047">'New-AzVirtualHub'</span></span>
    - <span data-ttu-id="1d1eb-1048">'Update-AzVirtualHub'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1048">'Update-AzVirtualHub'</span></span>
* <span data-ttu-id="1d1eb-1049">SQL Management SDK 종속성이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1049">Removed Sql Management SDK dependency</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="1d1eb-1050">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1050">Az.PolicyInsights</span></span>
* <span data-ttu-id="1d1eb-1051">오류 메시지가 향상되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1051">Improved error messages</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="1d1eb-1052">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1052">Az.RecoveryServices</span></span>
* <span data-ttu-id="1d1eb-1053">Azure Site Recovery는 Azure 디스크 암호화 Virtual Machines에 대한 VM 속성을 다시 보호하고 업데이트하는 기능을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1053">Azure Site Recovery added support for doing reprotect and updated vm properties for Azure disk encrypted Virtual Machines.</span></span>
* <span data-ttu-id="1d1eb-1054">Azure Site Recovery VmwareToAzure 속성 DR 모니터링이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1054">Added Azure Site Recovery VmwareToAzure properties DR monitoring</span></span>
* <span data-ttu-id="1d1eb-1055">Azure Backup은 실패한 항목에 대한 정책 업데이트 재시도 지원을 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1055">Azure Backup added support for retrying policy update for failed items.</span></span>
* <span data-ttu-id="1d1eb-1056">Azure Backup은 백업 및 복원 중에 디스크 제외 설정에 대한 지원을 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1056">Azure Backup Added support for disk exclusion settings during backup and restore.</span></span>
* <span data-ttu-id="1d1eb-1057">Azure Backup은 AzureFileShare에서 여러 파일/폴더 복원을 위한 지원을 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1057">Azure Backup Added Support for Restoring Multiple files/folders in AzureFileShare</span></span>
* <span data-ttu-id="1d1eb-1058">Azure Backup은 IaasVM 정책을 업데이트하는 동안 사용자 지정 리소스 그룹 지원에 대한 지원을 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1058">Azure Backup Added support for User-specified Resourcegroup support while updating IaasVM Policy</span></span>

#### <a name="azresources"></a><span data-ttu-id="1d1eb-1059">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1059">Az.Resources</span></span>
* <span data-ttu-id="1d1eb-1060">'Get-AzResource -ResourceGroupName -Name -ExpandProperties -ResourceType'이 기본 apiVersion 대신 실제 apiVersion 리소스를 사용하도록 수정했습니다. [# 11267]</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1060">Fixed 'Get-AzResource -ResourceGroupName -Name -ExpandProperties -ResourceType' to use actual apiVersion of resources instead of default apiVersion [#11267]</span></span>
* <span data-ttu-id="1d1eb-1061">오류 시나리오에 대해 correlationId 로깅이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1061">Added correlationId logging for error scenarios</span></span>
* <span data-ttu-id="1d1eb-1062">작은 설명서가 'Get-AzResourceLock'으로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1062">Small documentation change to 'Get-AzResourceLock'.</span></span> <span data-ttu-id="1d1eb-1063">예제가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1063">Added example.</span></span>
* <span data-ttu-id="1d1eb-1064">'Get-AzADUser'의 매개 변수 값에서 작은 따옴표를 이스케이프 처리하였습니다. [# 11317]</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1064">Escaped single quote in parameter value of 'Get-AzADUser' [#11317]</span></span>
* <span data-ttu-id="1d1eb-1065">배포 스크립트('Get-AzDeploymentScript', 'Get-AzDeploymentScriptLog', 'Save-AzDeploymentScriptLog', 'Remove-AzDeploymentScript')에 대한 새로운 cmdlet 추가가 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1065">Added new cmdlets for Deployment Scripts ('Get-AzDeploymentScript', 'Get-AzDeploymentScriptLog', 'Save-AzDeploymentScriptLog', 'Remove-AzDeploymentScript')</span></span>

#### <a name="azsql"></a><span data-ttu-id="1d1eb-1066">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1066">Az.Sql</span></span>
* <span data-ttu-id="1d1eb-1067">'Invoke-AzSqlDatabaseFailover'에 읽기 가능한 보조 매개 변수를 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1067">Added readable secondary parameter to 'Invoke-AzSqlDatabaseFailover'</span></span>
* <span data-ttu-id="1d1eb-1068">'Disable-AzSqlServerActiveDirectoryOnlyAuthentication' cmdlet을 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1068">Added cmdlet 'Disable-AzSqlServerActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="1d1eb-1069">데이터베이스에서 열을 분류할 때 저장된 민감도 순위입니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1069">Saved sensitivity rank when classifying columns in the database.</span></span>

#### <a name="azsupport"></a><span data-ttu-id="1d1eb-1070">Az.Support</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1070">Az.Support</span></span>
* <span data-ttu-id="1d1eb-1071">'Az.Support' 모듈의 일반 공급</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1071">General availability of 'Az.Support' module</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="1d1eb-1072">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1072">Az.Websites</span></span>
* <span data-ttu-id="1d1eb-1073">아래의 새로운 cmdlet을 통해 webapp 트래픽 라우팅 규칙을 사용하는 작업에 대한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1073">Added support for working with webapp Traffic Routing Rules via below new cmdlets</span></span>
    - <span data-ttu-id="1d1eb-1074">'Get-AzWebAppTrafficRouting'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1074">'Get-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="1d1eb-1075">'Update-AzWebAppTrafficRouting'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1075">'Update-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="1d1eb-1076">'Add-AzWebAppTrafficRouting'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1076">'Add-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="1d1eb-1077">'Remove-AzWebAppTrafficRouting'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1077">'Remove-AzWebAppTrafficRouting'</span></span>

## <a name="361---march-2020"></a><span data-ttu-id="1d1eb-1078">3.6.1 - 2020년 3월</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1078">3.6.1 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="1d1eb-1079">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1079">Az.Accounts</span></span>
* <span data-ttu-id="1d1eb-1080">'피드백 보내기'에서 Azure PowerShell 설문 조사 페이지가 열립니다[#11020].</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1080">Open Azure PowerShell survey page in 'Send-Feedback' [#11020]</span></span>
* <span data-ttu-id="1d1eb-1081">'오류 해결'에서 Azure PowerShell 설문 조사 URL이 표시됩니다[#11021].</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1081">Display Azure PowerShell survey URL in 'Resolve-Error' [#11021]</span></span>
* <span data-ttu-id="1d1eb-1082">UserAgent에서 Az 버전이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1082">Added Az version in UserAgent</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="1d1eb-1083">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1083">Az.ApiManagement</span></span>
* <span data-ttu-id="1d1eb-1084">DeveloperPortal 엔드포인트에서 사용자 지정 도메인을 검색하고 구성하기 위한 지원이 추가되었습니다[#11007].</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1084">Added support for retrieving and configuring Custom Domain on the DeveloperPortal Endpoint [#11007]</span></span>
* <span data-ttu-id="1d1eb-1085">Json 형식의 API 정의를 다운로드하기 위한 'Export-AzApiManagementApi' 지원이 추가되었습니다[#9987].</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1085">'Export-AzApiManagementApi' Added support for downloading Api Definition in Json format [#9987]</span></span>
* <span data-ttu-id="1d1eb-1086">Json 문서에서 OpenApi 3.0 정의를 가져오기 위한 'Import-AzApiManagementApi' 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1086">'Import-AzApiManagementApi' Added support for importing OpenApi 3.0 definition from Json document</span></span>
* <span data-ttu-id="1d1eb-1087">AAD B2C 공급자에 대한 '로그인 테넌트'를 구성하기 위한 'New-AzApiManagementIdentityProvider' 및 'Set-AzApiManagementIdentityProvider' 지원이 추가되었습니다[#9784].</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1087">'New-AzApiManagementIdentityProvider' and 'Set-AzApiManagementIdentityProvider' Added support for configuring 'Signin Tenant' for AAD B2C Provider [#9784]</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="1d1eb-1088">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1088">Az.DataLakeStore</span></span>
* <span data-ttu-id="1d1eb-1089">csproj 및 psd1에서 System.Buffers에 대한 참조가 명시적으로 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1089">Added reference to System.Buffers explicitly in csproj and psd1.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="1d1eb-1090">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1090">Az.IotHub</span></span>
* <span data-ttu-id="1d1eb-1091">Iot Hub에서 디바이스를 관리하기 위한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1091">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="1d1eb-1092">새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1092">New Cmdlets are:</span></span>
    - <span data-ttu-id="1d1eb-1093">'Add-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1093">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="1d1eb-1094">'Get-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1094">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="1d1eb-1095">'Remove-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1095">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="1d1eb-1096">'Set-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1096">'Set-AzIotHubDevice'</span></span>
* <span data-ttu-id="1d1eb-1097">Iot Hub의 대상 IoT 디바이스에서 모듈을 관리하기 위한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1097">Added support to manage modules on a target Iot device in an Iot Hub.</span></span> <span data-ttu-id="1d1eb-1098">새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1098">New Cmdlets are:</span></span>
    - <span data-ttu-id="1d1eb-1099">'Add-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1099">'Add-AzIotHubModule'</span></span>
    - <span data-ttu-id="1d1eb-1100">'Get-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1100">'Get-AzIotHubModule'</span></span>
    - <span data-ttu-id="1d1eb-1101">'Remove-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1101">'Remove-AzIotHubModule'</span></span>
    - <span data-ttu-id="1d1eb-1102">'Set-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1102">'Set-AzIotHubModule'</span></span>
* <span data-ttu-id="1d1eb-1103">Iot Hub에서 대상 IoT 디바이스에 대한 연결 문자열을 가져오는 cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1103">Added cmdlet to get the connection string of a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="1d1eb-1104">Iot Hub에서 대상 IoT 디바이스의 모듈에 대한 연결 문자열을 가져오는 cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1104">Added cmdlet to get the connection string of a module on a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="1d1eb-1105">IoT 디바이스의 부모 디바이스를 가져오거나 설정하기 위한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1105">Added support to get/set parent device of an IoT device.</span></span> <span data-ttu-id="1d1eb-1106">새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1106">New Cmdlets are:</span></span>
    - <span data-ttu-id="1d1eb-1107">'Get-AzIotHubDeviceParent'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1107">'Get-AzIotHubDeviceParent'</span></span>
    - <span data-ttu-id="1d1eb-1108">'Set-AzIotHubDeviceParent'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1108">'Set-AzIotHubDeviceParent'</span></span>
* <span data-ttu-id="1d1eb-1109">디바이스 부모-자식 관계를 관리하기 위한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1109">Added support to manage device parent-child relationship.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="1d1eb-1110">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1110">Az.Monitor</span></span>
* <span data-ttu-id="1d1eb-1111">'Get-AzMetricDefinition'에 대한 출력 값이 수정되었습니다[#9714].</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1111">Fixed output value for 'Get-AzMetricDefinition' [#9714]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="1d1eb-1112">Az.Network</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1112">Az.Network</span></span>
* <span data-ttu-id="1d1eb-1113">SQL Management SDK가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1113">Updated Sql Management SDK.</span></span>
* <span data-ttu-id="1d1eb-1114">PrivateLinkServiceConnectionState 클래스의 명명 차이 문제가 해결되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1114">Fixed a naming-difference issue in PrivateLinkServiceConnectionState class.</span></span>
    - <span data-ttu-id="1d1eb-1115">ActionsRequired 필드가 ActionRequired에 매핑됩니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1115">Mapping the field ActionsRequired to ActionRequired.</span></span>
* <span data-ttu-id="1d1eb-1116">PublicNetworkAccess가 'New-AzSqlServer' 및 'Set-AzSqlServer'에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1116">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>

#### <a name="azresources"></a><span data-ttu-id="1d1eb-1117">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1117">Az.Resources</span></span>
* <span data-ttu-id="1d1eb-1118">Get-AzRoleAssignment'의 null 참조 버그가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1118">Fixed for null reference bug in 'Get-AzRoleAssignment'</span></span>
* <span data-ttu-id="1d1eb-1119">'Remove-AzADGroup'에서 '-Force' 및 '-PassThru' 스위치가 선택적으로 표시됩니다[#10849].</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1119">Marked switch '-Force' and '-PassThru' optional in 'Remove-AzADGroup' [#10849]</span></span>
* <span data-ttu-id="1d1eb-1120">'Remove-AzADGroup'에서 'MailNickname'이 반환되지 않는 문제가 해결되었습니다[#11167].</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1120">Fixed issue that 'MailNickname' doesn't return in 'Remove-AzADGroup' [#11167]</span></span>
* <span data-ttu-id="1d1eb-1121">'Remove-AzADGroup' 파이프 작업이 작동하지 않는 문제가 해결되었습니다[#11171].</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1121">Fixed issue that 'Remove-AzADGroup' pipe operation doesn't work [#11171]</span></span>
* <span data-ttu-id="1d1eb-1122">GetAzureRoleAssignmentCommand의 null 참조 버그가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1122">Fixed for null reference bug in GetAzureRoleAssignmentCommand</span></span>
* <span data-ttu-id="1d1eb-1123">예정된 정책 cmdlet 변경에 대한 호환성이 손상되는 변경 특성이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1123">Added breaking change attributes for upcoming changes to policy cmdlets</span></span>
* <span data-ttu-id="1d1eb-1124">서버 쪽에서 리소스 그룹 태그 필터링을 수행하도록 'Get-AzResourceGroup'이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1124">Updated 'Get-AzResourceGroup' to perform resource group tag filtering on server-side</span></span>
* <span data-ttu-id="1d1eb-1125">-ResourceId를 허용하도록 Tag cmdlet이 확장되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1125">Extended Tag cmdlets to accept -ResourceId</span></span>
    - <span data-ttu-id="1d1eb-1126">Get-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1126">Get-AzTag -ResourceId</span></span>
    - <span data-ttu-id="1d1eb-1127">New-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1127">New-AzTag -ResourceId</span></span>
    - <span data-ttu-id="1d1eb-1128">Remove-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1128">Remove-AzTag -ResourceId</span></span>
* <span data-ttu-id="1d1eb-1129">새 Tag cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1129">Added new Tag cmdlet</span></span>
    - <span data-ttu-id="1d1eb-1130">Update-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1130">Update-AzTag -ResourceId</span></span>
* <span data-ttu-id="1d1eb-1131">SDK 3.3.0에서 ScopedDeployment를 가져왔습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1131">Brought ScopedDeployment from SDK 3.3.0</span></span>

#### <a name="azsql"></a><span data-ttu-id="1d1eb-1132">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1132">Az.Sql</span></span>
* <span data-ttu-id="1d1eb-1133">PublicNetworkAccess가 'New-AzSqlServer' 및 'Set-AzSqlServer'에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1133">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>
* <span data-ttu-id="1d1eb-1134">관리형 데이터베이스에 대한 장기 보존 백업 구성에 대한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1134">Added support for Long Term Retention backup configuration for Managed Databases</span></span>
    - <span data-ttu-id="1d1eb-1135">관리형 데이터베이스에서 LTR 정책을 가져오거나 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1135">Get/Set LTR policy on a managed database</span></span>
    - <span data-ttu-id="1d1eb-1136">관리형 데이터베이스, 관리형 인스턴스 또는 위치를 기준으로 LTR 백업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1136">Get LTR backup(s) by managed database, managed instance, or by location</span></span>
    - <span data-ttu-id="1d1eb-1137">LTR 백업을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1137">Remove an LTR backup</span></span>
    - <span data-ttu-id="1d1eb-1138">LTR 백업을 복원하여 새 관리형 데이터베이스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1138">Restore an LTR backup to create a new managed database</span></span>
* <span data-ttu-id="1d1eb-1139">MinimalTlsVersion이 New-AzSqlServer 및 Set-AzSqlServer에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1139">Added MinimalTlsVersion to New-AzSqlServer and Set-AzSqlServer</span></span>
* <span data-ttu-id="1d1eb-1140">MinimalTlsVersion을 New-AzSqlInstance 및 Set-AzSqlInstance에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1140">Added MinimalTlsVersion to New-AzSqlInstance and Set-AzSqlInstance</span></span>
* <span data-ttu-id="1d1eb-1141">Az.Network에 대한 SQL SDK 버전이 높아졌습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1141">Bumped SQL SDK version for Az.Network</span></span>

#### <a name="azstorage"></a><span data-ttu-id="1d1eb-1142">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1142">Az.Storage</span></span>
* <span data-ttu-id="1d1eb-1143">ImmutabilityPolicy에서 AllowProtectedAppendWrite가 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1143">Supported AllowProtectedAppendWrite in ImmutabilityPolicy</span></span>
    - <span data-ttu-id="1d1eb-1144">'Set-AzRmStorageContainerImmutabilityPolicy'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1144">'Set-AzRmStorageContainerImmutabilityPolicy'</span></span>
* <span data-ttu-id="1d1eb-1145">이후 릴리스에서 AzureStorageTable 형식 변경에 대한 호환성이 손상되는 변경 경고 메시지가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1145">Added breaking change warning message for AzureStorageTable type change in a future release</span></span>
    - <span data-ttu-id="1d1eb-1146">'New-AzStorageTable'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1146">'New-AzStorageTable'</span></span>
    - <span data-ttu-id="1d1eb-1147">'Get-AzStorageTable'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1147">'Get-AzStorageTable'</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="1d1eb-1148">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1148">Az.Websites</span></span>
* <span data-ttu-id="1d1eb-1149">'New-AzAppServicePlan' 및 'Set-AzAppServicePlan'에 대한 Tag 매개 변수가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1149">Added Tag parameter for 'New-AzAppServicePlan' and 'Set-AzAppServicePlan'</span></span>
* <span data-ttu-id="1d1eb-1150">웹 사이트에 사용자 지정 도메인을 추가할 때 예외가 throw되면 cmdlet 실행을 중지합니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1150">Stop cmdlet execution if an exception is thrown when adding a custom domain to a website</span></span>
* <span data-ttu-id="1d1eb-1151">App Service 계획과 동일한 리소스 그룹에 속하지 않는 App Services에 대한 작업을 수행하기 위한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1151">Added support to perform operations for App Services not in the same resource group as the App Service Plan</span></span>
* <span data-ttu-id="1d1eb-1152">다른 리소스 그룹의 WebApp/Function에 대한 액세스 제한이 적용되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1152">Applied access restriction to WebApp/Function in different resource groups</span></span>
* <span data-ttu-id="1d1eb-1153">WebAppSlot에 대한 사용자 지정 호스트 이름을 설정하는 문제가 해결되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1153">Fixed issue to set custom hostnames for WebAppSlots</span></span>

## <a name="350---february-2020"></a><span data-ttu-id="1d1eb-1154">3.5.0 - 2020년 2월</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1154">3.5.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="1d1eb-1155">마지막 주 릴리스 이후의 주요 사항</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1155">Highlights since the last major release</span></span>
* <span data-ttu-id="1d1eb-1156">클라이언트 쪽 원격 분석이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1156">Updated client side telemetry.</span></span>
* <span data-ttu-id="1d1eb-1157">디바이스 관리를 지원하는 cmdlet이 Az.IotHub에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1157">Az.IotHub added cmdlets to support to manage devices.</span></span>
* <span data-ttu-id="1d1eb-1158">가용성 그룹 수신기에 대한 cmdlet이 Az.SqlVirtualMachine에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1158">Az.SqlVirtualMachine added cmdlets for Availability Group Listener.</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="1d1eb-1159">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1159">Az.Accounts</span></span>
* <span data-ttu-id="1d1eb-1160">SubscriptionId, TenantId 및 실행 시간이 클라이언트 쪽 원격 분석에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1160">Added SubscriptionId, TenantId, and execution time into data of client side telemetry</span></span>

#### <a name="azautomation"></a><span data-ttu-id="1d1eb-1161">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1161">Az.Automation</span></span>
* <span data-ttu-id="1d1eb-1162">'New-AzAutomationSoftwareUpdateConfiguration' 참조 설명서의 예제 1에 있는 오타가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1162">Fixed typo in Example 1 in reference documentation for 'New-AzAutomationSoftwareUpdateConfiguration'</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="1d1eb-1163">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1163">Az.CognitiveServices</span></span>
* <span data-ttu-id="1d1eb-1164">SDK가 7.0으로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1164">Updated SDK to 7.0</span></span>
* <span data-ttu-id="1d1eb-1165">서버 응답 본문이 비어 있는 경우 표시되는 오류 메시지가 향상되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1165">Improved error message when server responses empty body</span></span>

#### <a name="azcompute"></a><span data-ttu-id="1d1eb-1166">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1166">Az.Compute</span></span>
* <span data-ttu-id="1d1eb-1167">업데이트하는 동안 빈 값이 ProximityPlacementGroupId에 허용되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1167">Allowed empty value for ProximityPlacementGroupId during update</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="1d1eb-1168">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1168">Az.FrontDoor</span></span>
* <span data-ttu-id="1d1eb-1169">WAF에서 사용할 수 있는 관리형 규칙 정의를 가져오는 cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1169">Added cmdlet to get managed rule definitions that can be used in WAF</span></span>

#### <a name="aziothub"></a><span data-ttu-id="1d1eb-1170">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1170">Az.IotHub</span></span>
* <span data-ttu-id="1d1eb-1171">Iot Hub에서 디바이스를 관리하기 위한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1171">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="1d1eb-1172">새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1172">New Cmdlets are:</span></span>
    - <span data-ttu-id="1d1eb-1173">'Add-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1173">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="1d1eb-1174">'Get-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1174">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="1d1eb-1175">'Remove-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1175">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="1d1eb-1176">'Set-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1176">'Set-AzIotHubDevice'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="1d1eb-1177">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1177">Az.KeyVault</span></span>
* <span data-ttu-id="1d1eb-1178">Add-AzKeyVaultKey.md에 대해 중복된 텍스트가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1178">Fixed duplicated text for Add-AzKeyVaultKey.md</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="1d1eb-1179">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1179">Az.Monitor</span></span>
* <span data-ttu-id="1d1eb-1180">Get-AzLog cmdlet에 대한 설명이 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1180">Fixed description of the Get-AzLog cmdlet.</span></span>
* <span data-ttu-id="1d1eb-1181">ActionGroupId라는 새 매개 변수가 'New-AzMetricAlertRuleV2' 명령에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1181">A new parameter called ActionGroupId was added to 'New-AzMetricAlertRuleV2' command.</span></span>
    - <span data-ttu-id="1d1eb-1182">사용자는 ActionGroupId(string) 또는 ActionGorup(ActivityLogAlertActionGroup) 중 하나를 제공할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1182">The user can provide either ActionGroupId(string) or ActionGorup(ActivityLogAlertActionGroup).</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="1d1eb-1183">Az.Network</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1183">Az.Network</span></span>
* <span data-ttu-id="1d1eb-1184">'New-AzPrivateLinkService' cmdlet의 '-EnableProxyProtocol' 매개 변수에 대한 하나의 추가 매개 변수 메모가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1184">Added one extra parameter note for parameter '-EnableProxyProtocol' for 'New-AzPrivateLinkService' cmdlet.</span></span>
* <span data-ttu-id="1d1eb-1185">Start-AzVirtualNetworkGatewayConnectionPacketCapture.md 및 Start-AzVirtualnetworkGatewayPacketCapture.md의 FilterData 예제가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1185">Fixed FilterData example in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="1d1eb-1186">Start-AzVirtualNetworkGatewayConnectionPacketCapture.md 및 Start-AzVirtualnetworkGatewayPacketCapture.md의 모든 내부 및 외부 패킷을 캡처하는 패킷 캡처 예제가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1186">Added Packet Capture example for capture all inner and outer packets in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="1d1eb-1187">VNet 방화벽에서 Azure Firewall 정책이 지원됩니다</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1187">Supported Azure Firewall Policy on VNet Firewalls</span></span>
    - <span data-ttu-id="1d1eb-1188">새로 추가된 cmdlet이 없습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1188">No new cmdlets are added.</span></span> <span data-ttu-id="1d1eb-1189">VNet 방화벽에서 방화벽 정책 제한이 완화되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1189">Relaxing the restriction for firewall policy on VNet firewalls</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="1d1eb-1190">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1190">Az.RecoveryServices</span></span>
* <span data-ttu-id="1d1eb-1191">SQL Database에 대한 파일로 복원 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1191">Added Support for Restore-as-files for SQL Databases.</span></span>

#### <a name="azresources"></a><span data-ttu-id="1d1eb-1192">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1192">Az.Resources</span></span>
* <span data-ttu-id="1d1eb-1193">템플릿 배포 cmdlet이 리팩터링되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1193">Refactored template deployment cmdlets</span></span>
    - <span data-ttu-id="1d1eb-1194">관리 그룹에서 배포를 관리하는 새 \*-AzManagementGroupDeployment cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1194">Added new cmdlets for managing deployments at management group: \*-AzManagementGroupDeployment</span></span>
    - <span data-ttu-id="1d1eb-1195">테넌트 범위에서 배포를 관리하는 새 \*-AzTenantDeployment cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1195">Added new cmdlets for managing deployments at tenant scope: \*-AzTenantDeployment</span></span>
    - <span data-ttu-id="1d1eb-1196">구독 범위에서 구체적으로 작동하도록 \*-AzDeployment cmdlet이 리팩터링되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1196">Refactored \*-AzDeployment cmdlets to work specifically at subscription scope</span></span>
    - <span data-ttu-id="1d1eb-1197">\*-AzDeployment cmdlet에 대한 \*-AzSubscriptionDeployment 별칭이 만들어졌습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1197">Created aliases \*-AzSubscriptionDeployment for \*-AzDeployment cmdlets</span></span>
* <span data-ttu-id="1d1eb-1198">'AvailableToOtherTenants' 매개 변수가 설정되지 않는 'Update-AzADApplication'이 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1198">Fixed 'Update-AzADApplication' when parameter 'AvailableToOtherTenants' is not set</span></span>
* <span data-ttu-id="1d1eb-1199">AmbiguousParameterSetException을 방지하기 위해 ApplicationObjectWithoutCredentialParameterSet이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1199">Removed ApplicationObjectWithoutCredentialParameterSet to avoid AmbiguousParameterSetException.</span></span>
* <span data-ttu-id="1d1eb-1200">도움말 파일이 다시 생성되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1200">Regenerated help files</span></span>

#### <a name="azsql"></a><span data-ttu-id="1d1eb-1201">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1201">Az.Sql</span></span>
* <span data-ttu-id="1d1eb-1202">Managed Instance에서 구독 간 특정 시점 복원에 대한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1202">Added support for cross subscription point in time restore on Managed Instances.</span></span>
* <span data-ttu-id="1d1eb-1203">기존 SQL Managed Instance 하드웨어 생성 변경에 대한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1203">Added support for changing existing Sql Managed Instance hardware generation</span></span>
* <span data-ttu-id="1d1eb-1204">'Update-AzSqlServerVulnerabilityAssessmentSetting' 도움말 예제(매개 변수/속성 출력 -EmailAdmins)가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1204">Fixed 'Update-AzSqlServerVulnerabilityAssessmentSetting' help examples: parameter/property output - EmailAdmins</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="1d1eb-1205">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1205">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="1d1eb-1206">가용성 그룹 수신기에 대한 cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1206">Added cmdlets for Availability Group Listener</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="1d1eb-1207">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1207">Az.StorageSync</span></span>
* <span data-ttu-id="1d1eb-1208">'Invoke-AzStorageSyncCompatibilityCheck'에서 지원되는 문자 세트가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1208">Updated supported character sets in 'Invoke-AzStorageSyncCompatibilityCheck'.</span></span>

## <a name="340---february-2020"></a><span data-ttu-id="1d1eb-1209">3.4.0 - 2020년 2월</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1209">3.4.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="1d1eb-1210">마지막 주 릴리스 이후의 주요 사항</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1210">Highlights since the last major release</span></span>
* <span data-ttu-id="1d1eb-1211">Az. CosmosDB 초기 버전 0.1.0 출시</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1211">Az.CosmosDB initial version 0.1.0 released</span></span>
* <span data-ttu-id="1d1eb-1212">Az.Network ConnectionMonitor V2 지원 추가</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1212">Az.Network ConnectionMonitor V2 support added</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="1d1eb-1213">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1213">Az.Accounts</span></span>
* <span data-ttu-id="1d1eb-1214">AzureRmContext.json을 사용할 수 없을 때 컨텍스트 자동 저장 사용 안 함</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1214">Disable context auto saving when AzureRmContext.json not available</span></span>
* <span data-ttu-id="1d1eb-1215">Azure Powershell Common 참조를 1.3.5-preview로 업데이트</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1215">Update the reference to Azure Powershell Common to 1.3.5-preview</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="1d1eb-1216">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1216">Az.ApiManagement</span></span>
* <span data-ttu-id="1d1eb-1217">**Get-AzApiManagementApiSchema** API와 연결된 Open-Api 스키마 가져오기 수정   https://github.com/Azure/azure-powershell/issues/10626</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1217">**Get-AzApiManagementApiSchema** Fixed getting Open-Api Schema associated with an API   https://github.com/Azure/azure-powershell/issues/10626</span></span>
* <span data-ttu-id="1d1eb-1218">**New-AzApiManagementProduct** _ 및 _ *Set-AzApiManagementProduct*\*</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1218">**New-AzApiManagementProduct** _ and _ *Set-AzApiManagementProduct*\*</span></span>
  - <span data-ttu-id="1d1eb-1219"> https://github.com/Azure/azure-powershell/issues/10472 설명서 수정</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1219">Fix documentation for https://github.com/Azure/azure-powershell/issues/10472</span></span>
* <span data-ttu-id="1d1eb-1220">**Set-AzApiManagementApi** cmdlet을 사용하여 ServiceUrl을 업데이트하는 방법을 보여주는 예제 추가</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1220">**Set-AzApiManagementApi** Added example to show how to update the ServiceUrl using the cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="1d1eb-1221">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1221">Az.Compute</span></span>
* <span data-ttu-id="1d1eb-1222">VM 이름을 사용하지 않고 Get-AzVM -Status를 수행할 때 제한을 피하기 위해 VM 상태 수를 100개로 제한</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1222">Limit the number of VM status to 100 to avoid throttling when Get-AzVM -Status is performed without VM name.</span></span>
* <span data-ttu-id="1d1eb-1223">Update-AzDiskEncryptionSet cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1223">Add Update-AzDiskEncryptionSet cmdlet</span></span>
* <span data-ttu-id="1d1eb-1224">다음 cmdlet에 EncryptionType 및 DiskEncryptionSetId 매개 변수 추가:</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1224">Add EncryptionType and DiskEncryptionSetId parameters to the following cmdlets:</span></span>
    - <span data-ttu-id="1d1eb-1225">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1225">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span></span>
* <span data-ttu-id="1d1eb-1226">Get-AzProximityPlacementGroup cmdlet에 ColocationStatus 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1226">Add ColocationStatus parameter to Get-AzProximityPlacementGroup cmdlet.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="1d1eb-1227">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1227">Az.DataFactory</span></span>
* <span data-ttu-id="1d1eb-1228">ADF .Net SDK 버전을 4.7.0으로 업데이트</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1228">Update ADF .Net SDK version to 4.7.0</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="1d1eb-1229">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1229">Az.DeploymentManager</span></span>
* <span data-ttu-id="1d1eb-1230">리소스에 대한 LIST 작업 추가</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1230">Adds LIST operations for resources</span></span>
* <span data-ttu-id="1d1eb-1231">상태 검사 단계에 대한 작업을 수행하는 기능 추가</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1231">Adds capability for performing operations on Health Check steps</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="1d1eb-1232">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1232">Az.HDInsight</span></span>
* <span data-ttu-id="1d1eb-1233">AzHDInsightCluster의 문서 오류 수정</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1233">Fix document error of New-AzHDInsightCluster.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="1d1eb-1234">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1234">Az.KeyVault</span></span>
* <span data-ttu-id="1d1eb-1235">Remove-AzureKeyVault가 새 New-AzureKeyVault와 일관성을 유지하도록 VaultName 특성에 이름 별칭 추가</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1235">Add Name alias to VaultName attribute to make Remove-AzureKeyVault consistent with New-AzureKeyVault.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="1d1eb-1236">Az.Network</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1236">Az.Network</span></span>
* <span data-ttu-id="1d1eb-1237">Set-AzNetworkWatcherConfigFlowLog.md에 트래픽 분석 사용 안 함 시나리오를 보여주는 새 예제 추가</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1237">New example added to Set-AzNetworkWatcherConfigFlowLog.md to demonstrate Traffic Analytics disable scenario.</span></span>
* <span data-ttu-id="1d1eb-1238">Azure Firewall에 관리 IP 구성을 할당하는 지원 추가 - 방화벽에서 관리 트래픽에 사용할 전용 서브넷 및 공용 IP</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1238">Add support for assigning management IP configuration to Azure Firewall - a dedicated subnet and Public IP that the firewall will use for its management traffic</span></span>
    - <span data-ttu-id="1d1eb-1239">New-AzFirewall cmdlet이 업데이트됨:</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1239">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="1d1eb-1240">공용 IP 주소 개체를 허용하는 -ManagementPublicIpAddress 매개 변수(필수 아님) 추가</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1240">Added parameter -ManagementPublicIpAddress (not mandatory) which accepts a Public IP Address object</span></span>
        - <span data-ttu-id="1d1eb-1241">방화벽 개체에 SetManagementIpConfiguration 메서드 추가 - 입력으로 서브넷 및 공용 IP 주소 필요 - 서브넷 이름은 'AzureFirewallManagementSubnet'이어야 함</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1241">Added method SetManagementIpConfiguration on firewall object - requires a subnet and a Public IP address as input - subnet name must be 'AzureFirewallManagementSubnet'</span></span>
* <span data-ttu-id="1d1eb-1242">네트워크 인터페이스 대신 NSG 예제를 보여주도록 AzNetworkSecurityGroup 예제 수정</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1242">Corrected Get-AzNetworkSecurityGroup examples to show examples for NSG's instead of network interfaces.</span></span>
* <span data-ttu-id="1d1eb-1243">리소스 id 완성자가 매개 변수를 완성하지 못하게 방해하던 New-AzVpnSite 명령의 오타 수정</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1243">Fixed typo in New-AzVpnSite command that was preventing resource id completer from completing a parameter.</span></span>
* <span data-ttu-id="1d1eb-1244">Application Gateway의 다시 쓰기 규칙 작업 세트에서 Url 구성에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1244">Added support for Url Confiugration in Rewrite Rules Action Set in the Application Gateway</span></span>
    - <span data-ttu-id="1d1eb-1245">추가된 새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1245">New cmdlets added:</span></span>
        - <span data-ttu-id="1d1eb-1246">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1246">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span></span>
    - <span data-ttu-id="1d1eb-1247">선택적 매개 변수를 사용하도록 Cmdlet 업데이트 - UrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1247">Cmdlets updated with optional parameter - UrlConfiguration</span></span>
        - <span data-ttu-id="1d1eb-1248">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1248">New-AzApplicationGatewayRewriteRuleActionSet</span></span>
* <span data-ttu-id="1d1eb-1249">NetworkWatcher ConnectionMonitor 버전 2 리소스에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1249">Add suppport for NetworkWatcher ConnectionMonitor version 2 resources</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="1d1eb-1250">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1250">Az.PolicyInsights</span></span>
* <span data-ttu-id="1d1eb-1251">수정할 리소스를 결정하기 전에 규정 준수 평가 지원</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1251">Support evaluating compliance prior to determining what resource to remediate</span></span>
    - <span data-ttu-id="1d1eb-1252">Start-AzPolicyRemediation에 '-ResourceDiscoverMode' 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1252">Add '-ResourceDiscoverMode' parameter to Start-AzPolicyRemediation</span></span>
* <span data-ttu-id="1d1eb-1253">정책 메타데이터 리소스를 가져오는 Get-AzPolicyMetadata cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1253">Add Get-AzPolicyMetadata cmdlet for getting policy metadata resources</span></span>
* <span data-ttu-id="1d1eb-1254">API 버전 2019-10-01의 Get-AzPolicyState 및 Get-AzPolicyStateSummary 업데이트</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1254">Updated Get-AzPolicyState and Get-AzPolicyStateSummary for API version 2019-10-01</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="1d1eb-1255">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1255">Az.RecoveryServices</span></span>
* <span data-ttu-id="1d1eb-1256">복제된 디스크를 제거할 수 있도록 Azure Site Recovery에 지원 추가</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1256">Azure Site Recovery support for removing a replicated disk.</span></span>
* <span data-ttu-id="1d1eb-1257">Recovery Services 자격 증명 모음을 만드는 동안 태그를 추가할 수 있도록 Azure Backup에 지원 추가</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1257">Azure Backup added support for adding tags while creating a Recovery Services Vault.</span></span>

#### <a name="azresources"></a><span data-ttu-id="1d1eb-1258">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1258">Az.Resources</span></span>
* <span data-ttu-id="1d1eb-1259">컨텍스트 구독을 기본값으로 하는 \*-AzPolicyAssignment cmdlet에서 -Scope를 선택 사항으로 설정</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1259">Make -Scope optional in \*-AzPolicyAssignment cmdlets with default to context subscription</span></span>
* <span data-ttu-id="1d1eb-1260">암호 및 키 자격 증명을 사용하여 ADServicePrincipal을 만드는 예제 추가</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1260">Add examples of creating ADServicePrincipal with password and key credential</span></span>

#### <a name="azsql"></a><span data-ttu-id="1d1eb-1261">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1261">Az.Sql</span></span>
<span data-ttu-id="1d1eb-1262">DatabaseName 대신 PartnerDatabaseName이 있는지 확인하도록 New-AzSqlDatabaseSecondary cmdlet 수정</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1262">Fix New-AzSqlDatabaseSecondary cmdlet to check for PartnerDatabaseName existence instead of DatabaseName existence.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="1d1eb-1263">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1263">Az.Storage</span></span>
* <span data-ttu-id="1d1eb-1264">스토리지 계정 만들기에서 테이블/큐 암호화 Keytype 설정 지원</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1264">Support set Table/Queue Encryption Keytype in Create Storage Account</span></span>
    - <span data-ttu-id="1d1eb-1265">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1265">New-AzStorageAccount</span></span>
* <span data-ttu-id="1d1eb-1266">StorageException에 ExtendedErrorInformation이 없으면 RequestId 표시</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1266">Show RequestId when StorageException don't have ExtendedErrorInformation</span></span>
* <span data-ttu-id="1d1eb-1267">cmdlet Start-AzStorageBlobCopy의 예제 6 수정</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1267">Fix the Example 6 of cmdlet Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="1d1eb-1268">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1268">Az.Websites</span></span>
* <span data-ttu-id="1d1eb-1269">Set-AzWebapp 및 Set-AzWebappSlot이 AlwaysOn, MinTls 및 FtpsState 속성 지원</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1269">Set-AzWebapp and Set-AzWebappSlot supports AlwaysOn, MinTls and FtpsState properties</span></span>
* <span data-ttu-id="1d1eb-1270">단일 Set-AzWebApp 명령을 사용하여 AppservicePlan을 변경하는 동시에 HttpsOnly를 설정하면 HttpsOnly가 기본값으로 다시 설정되는 문제 수정</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1270">Fixing issue where setting HttpsOnly along with changing AppservicePlan at the same time using the single Set-AzWebApp Command, was resetting HttpsOnly to default value</span></span>

## <a name="330---january-2020"></a><span data-ttu-id="1d1eb-1271">3.3.0 - 2020년 1월</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1271">3.3.0 - January 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="1d1eb-1272">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1272">Az.Accounts</span></span>
* <span data-ttu-id="1d1eb-1273">AzureAttestationServiceEndpointResourceId 및 AzureAttestationServiceEndpointSuffix 매개 변수를 허용하도록 Add-AzEnvironment 및 Set-AzEnvironment가 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1273">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameters AzureAttestationServiceEndpointResourceId and AzureAttestationServiceEndpointSuffix</span></span>

#### <a name="azcdn"></a><span data-ttu-id="1d1eb-1274">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1274">Az.Cdn</span></span>
* <span data-ttu-id="1d1eb-1275">New-AzCdnEndpoint cmdlet에서 오류 응답 세부 정보 표시</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1275">Display error response detail in New-AzCdnEndpoint cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="1d1eb-1276">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1276">Az.Compute</span></span>
* <span data-ttu-id="1d1eb-1277">OS 프로필이 없는 관리 OD 디스크가 있는 VM의 Set-AzVMCustomScriptExtension cmdlet을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1277">Fix Set-AzVMCustomScriptExtension cmdlet for a VM with managed OD disk which does not have OS profile.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="1d1eb-1278">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1278">Az.ContainerInstance</span></span>
* <span data-ttu-id="1d1eb-1279">New-AzContainerGroup의 예에서 사용되는 고정 매개 변수 이름</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1279">Fixed parameter names used by example of New-AzContainerGroup</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="1d1eb-1280">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1280">Az.DataBoxEdge</span></span>
* <span data-ttu-id="1d1eb-1281">'Get-AzDataBoxEdgeStorageContainer' cmdlet 추가됨</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1281">Added cmdlet 'Get-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="1d1eb-1282">Edge 스토리지 컨테이너 가져오기</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1282">Get the Edge Storage Container</span></span>
* <span data-ttu-id="1d1eb-1283">'New-AzDataBoxEdgeStorageContainer' cmdlet 추가됨</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1283">Added cmdlet 'New-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="1d1eb-1284">새 Edge 스토리지 컨테이너 만들기</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1284">Create new Edge Strorage Container</span></span>
* <span data-ttu-id="1d1eb-1285">'Remove-AzDataBoxEdgeStorageContainer' cmdlet 추가됨</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1285">Added cmdlet 'Remove-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="1d1eb-1286">Edge 스토리지 컨테이너 제거</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1286">Remove the Edge Storage Container</span></span>
* <span data-ttu-id="1d1eb-1287">'Invoke-AzDataBoxEdgeStorageContainer' cmdlet 추가됨</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1287">Added cmdlet 'Invoke-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="1d1eb-1288">Edge 스토리지 컨테이너에서 데이터를 새로 고치는 작업 호출</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1288">Invoke action to refresh data on Edge Storage Container</span></span>
* <span data-ttu-id="1d1eb-1289">'Get-AzDataBoxEdgeStorageAccount' cmdlet 추가됨</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1289">Added cmdlet 'Get-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="1d1eb-1290">Edge 스토리지 계정 가져오기</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1290">Get the Edge Storage Account</span></span>
* <span data-ttu-id="1d1eb-1291">'New-AzDataBoxEdgeStorageAccount' cmdlet 추가됨</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1291">Added cmdlet 'New-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="1d1eb-1292">새 Edge 스토리지 계정 만들기</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1292">Create new Edge Storage Account</span></span>
* <span data-ttu-id="1d1eb-1293">'Remove-AzDataBoxEdgeStorageAccount' cmdlet 추가됨</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1293">Added cmdlet 'Remove-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="1d1eb-1294">Edge 스토리지 계정 제거</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1294">Remove the Edge Storage Account</span></span>
* <span data-ttu-id="1d1eb-1295">'Invoke-AzDataBoxEdgeShare' cmdlet 호출</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1295">Invoke cmdlet 'Invoke-AzDataBoxEdgeShare'</span></span>
  - <span data-ttu-id="1d1eb-1296">공유에서 데이터를 새로 고치는 작업 호출</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1296">Invoke action to refresh data on share</span></span>
* <span data-ttu-id="1d1eb-1297">'Set-AzDataBoxEdgeStorageAccountCredential' cmdlet 추가됨</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1297">Added cmdlet 'Set-AzDataBoxEdgeStorageAccountCredential'</span></span>
  - <span data-ttu-id="1d1eb-1298">az databoxedge 스토리지 계정 자격 증명 설정</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1298">Set the az databoxedge storage account credential</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="1d1eb-1299">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1299">Az.DataFactory</span></span>
* <span data-ttu-id="1d1eb-1300">Get-AzDataFactoryV2IntegrationRuntime cmd에 AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId 및 VersionStatus 속성 추가</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1300">Add AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId and VersionStatus properties for Get-AzDataFactoryV2IntegrationRuntime cmd</span></span>
* <span data-ttu-id="1d1eb-1301">ADF .Net SDK 버전을 4.6.0으로 업데이트</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1301">Update ADF .Net SDK version to 4.6.0</span></span>
* <span data-ttu-id="1d1eb-1302">고정 공용 IP 주소로 Azure-SSIS IR을 만들 수 있도록 'Set-AzureRmDataFactoryV2IntegrationRuntime'cmd에 대해 'PublicIPs' 매개 변수를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1302">Add parameter 'PublicIPs' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable create Azure-SSIS IR with static public IP addresses.</span></span>

#### <a name="azdevtestlabs"></a><span data-ttu-id="1d1eb-1303">Az.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1303">Az.DevTestLabs</span></span>
* <span data-ttu-id="1d1eb-1304">Get-AzDtlAllowedVMSizesPolicy.md에서 끊어진 링크 제거</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1304">Remove the broken link in Get-AzDtlAllowedVMSizesPolicy.md</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="1d1eb-1305">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1305">Az.EventHub</span></span>
* <span data-ttu-id="1d1eb-1306">10634 문제 해결: eventhubnamespace 제거에 대한 null 개체 참조 수정</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1306">Fix for issue 10634 : Fix the null Object reference for remove eventhubnamespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="1d1eb-1307">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1307">Az.HDInsight</span></span>
* <span data-ttu-id="1d1eb-1308">Invoke-AzHDInsightHiveJob.md 오류를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1308">Fix Invoke-AzHDInsightHiveJob.md error.</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="1d1eb-1309">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1309">Az.MachineLearning</span></span>
* <span data-ttu-id="1d1eb-1310">MachineLearningCompute를 더 이상 사용할 수 없게 되어 아래 cmdlet이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1310">Removed below cmdlets because MachineLearningCompute is not available any longer</span></span>
  - <span data-ttu-id="1d1eb-1311">Get-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1311">Get-AzMlOpCluster</span></span>
  - <span data-ttu-id="1d1eb-1312">Get-AzMlOpClusterKey</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1312">Get-AzMlOpClusterKey</span></span>
  - <span data-ttu-id="1d1eb-1313">New-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1313">New-AzMlOpCluster</span></span>
  - <span data-ttu-id="1d1eb-1314">Remove-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1314">Remove-AzMlOpCluster</span></span>
  - <span data-ttu-id="1d1eb-1315">Set-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1315">Set-AzMlOpCluster</span></span>
  - <span data-ttu-id="1d1eb-1316">Test-AzMlOpClusterSystemServicesUpdateAvailability</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1316">Test-AzMlOpClusterSystemServicesUpdateAvailability</span></span>
  - <span data-ttu-id="1d1eb-1317">Update-AzMlOpClusterSystemService</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1317">Update-AzMlOpClusterSystemService</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="1d1eb-1318">Az.Network</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1318">Az.Network</span></span>
* <span data-ttu-id="1d1eb-1319">Microsoft.Azure.Management.Sql의 종속성을 1.36-preview에서 1.37-preview로 업그레이드</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1319">Upgrade dependency of Microsoft.Azure.Management.Sql from 1.36-preview to 1.37-preview</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="1d1eb-1320">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1320">Az.RecoveryServices</span></span>
* <span data-ttu-id="1d1eb-1321">Azure Site Recovery는 Azure 간 공급자를 위해 고객 관리 키와 함께 유휴 상태에서 암호화된 관리 디스크 vms의 변경을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1321">Azure Site Recovery change support for managed disk vms encrypted at rest with customer managed keys for Azure to Azure provider.</span></span>
* <span data-ttu-id="1d1eb-1322">Azure Site Recovery는 VMware에서 Azure로를 위해 보호를 사용할 때 선택적 입력으로서 디스크 암호화 집합 ID를 입력하도록 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1322">Azure Site Recovery support to input disk encryption Set Id as optional input at enabling protection for Vmware to Azure.</span></span>
* <span data-ttu-id="1d1eb-1323">Azure Site Recovery는 VMware에서 Azure로를 위해 보호를 사용하기 위해 디스크 수준의 선택적 입력으로서 디스크 암호화 집합 ID를 입력하도록 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1323">Azure Site Recovery support to input disk encryption Set Id as optional input at disk level to enable protection for Vmware to Azure.</span></span>
* <span data-ttu-id="1d1eb-1324">Azure Site Recovery는 HyperV에서 Azure로를 위해 디스크 암호화 집합 맵을 사용하여 복제 보호된 항목을 업데이트하도록 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1324">Azure Site Recovery support to update replication protected item with disk encryption set Map for HyperV to Azure.</span></span>

#### <a name="azresources"></a><span data-ttu-id="1d1eb-1325">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1325">Az.Resources</span></span>
* <span data-ttu-id="1d1eb-1326">'Remove-AzTag'의 도움말 문서에서 오류를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1326">Fix an error in help document of 'Remove-AzTag'.</span></span>

#### <a name="azsql"></a><span data-ttu-id="1d1eb-1327">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1327">Az.Sql</span></span>
* <span data-ttu-id="1d1eb-1328">Azure Database의 마스터 DB에서 작동하도록 취약성 평가 세트 기준 cmdlet 기능을 수정하고 관리형 인스턴스 시스템 데이터베이스에서 이를 제한합니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1328">Fix vulnerability assessment set baseline cmdlets functionality to work on master db for azure database and limit it on managed instance system databases.</span></span>
* <span data-ttu-id="1d1eb-1329">SQL 인스턴스 장애 조치(failover) 그룹을 만들 때 오류 수정</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1329">Fix an error when creating SQL instance failover group</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="1d1eb-1330">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1330">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="1d1eb-1331">올바른 새 라이선스 형식으로 DR 추가</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1331">Add DR as a new valid License type</span></span>

#### <a name="azstorage"></a><span data-ttu-id="1d1eb-1332">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1332">Az.Storage</span></span>
* <span data-ttu-id="1d1eb-1333">다음 릴리스에서 DefaultAction Value 변경에 대해 호환성이 손상되는 변경 경고 메시지 추가</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1333">Add breaking change warning message for DefaultAction Value change in a future release</span></span>
    - <span data-ttu-id="1d1eb-1334">Update-AzStorageAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1334">Update-AzStorageAccountNetworkRuleSet</span></span>
* <span data-ttu-id="1d1eb-1335">-IncludeGeoReplicationStats 매개 변수와 함께 get-AzureRMStorageAccount를 실행하여 스토리지 계정의 마지막 동기화 시간 가져오기 지원</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1335">Support Get last sync time of Storage account by run get-AzureRMStorageAccount with parameter -IncludeGeoReplicationStats</span></span>
    - <span data-ttu-id="1d1eb-1336">Get-AzureRMStorageAccount</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1336">Get-AzureRMStorageAccount</span></span>

## <a name="320---december-2019"></a><span data-ttu-id="1d1eb-1337">3.2.0 - 2019년 12월</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1337">3.2.0 - December 2019</span></span>

### <a name="general"></a><span data-ttu-id="1d1eb-1338">일반</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1338">General</span></span>
* <span data-ttu-id="1d1eb-1339">모든 모듈의 상대 경로를 사용하기 위해 .psd1의 참조 업데이트</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1339">Update references in .psd1 to use relative path for all modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="1d1eb-1340">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1340">Az.Accounts</span></span>
* <span data-ttu-id="1d1eb-1341">Az 4.0 미리 보기를 위해 클라이언트 측 원격 분석에 대해 UserAgent를 올바르게 설정</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1341">Set correct UserAgent for client-side telemetry for Az 4.0 preview</span></span>
* <span data-ttu-id="1d1eb-1342">Az 4.0 미리 보기에서 컨텍스트가 null인 경우 사용자에게 친숙한 오류 메시지로 표시</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1342">Display user friendly error message when context is null in Az 4.0 preview</span></span>

#### <a name="azbatch"></a><span data-ttu-id="1d1eb-1343">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1343">Az.Batch</span></span>
* <span data-ttu-id="1d1eb-1344">**New-AzBatchPool** 이 'VirtualMachineConfiguration.ContainerConfiguration' 또는 'VirtualMachineConfiguration.DataDisks'를 서버로 제대로 보내지 않는 [#10602](https://github.com/Azure/azure-powershell/issues/10602) 문제 수정</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1344">Fix issue [#10602](https://github.com/Azure/azure-powershell/issues/10602), where **New-AzBatchPool** did not properly send 'VirtualMachineConfiguration.ContainerConfiguration' or 'VirtualMachineConfiguration.DataDisks' to the server.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="1d1eb-1345">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1345">Az.DataFactory</span></span>
* <span data-ttu-id="1d1eb-1346">ADF .Net SDK 버전을 4.5.0으로 업데이트</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1346">Update ADF .Net SDK version to 4.5.0</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="1d1eb-1347">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1347">Az.FrontDoor</span></span>
* <span data-ttu-id="1d1eb-1348">WAF 관리 규칙 제외 지원 추가됨</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1348">Added WAF managed rules exclusion support</span></span>
* <span data-ttu-id="1d1eb-1349">자동 완성에 SocketAddr 추가</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1349">Add SocketAddr to auto-complete</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="1d1eb-1350">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1350">Az.HealthcareApis</span></span>
* <span data-ttu-id="1d1eb-1351">예외 처리</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1351">Exception Handling</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="1d1eb-1352">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1352">Az.KeyVault</span></span>
* <span data-ttu-id="1d1eb-1353">잠재적으로 설정되지 않은 오류 액세스 값 수정</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1353">Fixed error accessing value that is potentially not set</span></span>
* <span data-ttu-id="1d1eb-1354">타원 곡선 암호화 인증서 관리</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1354">Elliptic Curve Cryptography Certificate Managment</span></span>
    - <span data-ttu-id="1d1eb-1355">인증서 정책에 대한 곡선 지정을 위한 지원 추가됨</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1355">Added support to specify the Curve for Certificate Policies</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="1d1eb-1356">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1356">Az.Monitor</span></span>
* <span data-ttu-id="1d1eb-1357">진단 설정 추가 명령에 선택적 인수 추가</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1357">Adding optional argument to the Add Diagnostic Settings command.</span></span> <span data-ttu-id="1d1eb-1358">스위치 인수(있는 경우)는 Log Analytics로 내보내기가 고정 스키마(전용 데이터 유형)가 되어야 함을</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1358">A switch argument that if present indicates that the export to Log Analytics must be to a fixed schema (a.k.a.</span></span> <span data-ttu-id="1d1eb-1359">나타냄</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1359">dedicated, data type)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="1d1eb-1360">Az.Network</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1360">Az.Network</span></span>
* <span data-ttu-id="1d1eb-1361">AzureFirewall 애플리케이션, NAT 및 네트워크 규칙에서 IpGroups 지원.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1361">Support for IpGroups in AzureFirewall Application,Nat & Network Rules.</span></span>

#### <a name="azresources"></a><span data-ttu-id="1d1eb-1362">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1362">Az.Resources</span></span>
* <span data-ttu-id="1d1eb-1363">이름이 일부 내장 매개 변수 이름과 충돌하는 경우 템플릿 배포가 템플릿 매개 변수를 읽지 못하는 문제 수정.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1363">Fix an issue where template deployment fails to read a template parameter if its name conflicts with some built-in parameter name.</span></span>
* <span data-ttu-id="1d1eb-1364">정책 세트 정의 내에 그룹화 지원을 도입하는 새로운 API 버전 2019-09-01을 사용하도록 정책 cmdlet 업데이트.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1364">Updated policy cmdlets to use new api version 2019-09-01 that introduces grouping support within policy set definitions.</span></span>

#### <a name="azsql"></a><span data-ttu-id="1d1eb-1365">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1365">Az.Sql</span></span>
* <span data-ttu-id="1d1eb-1366">취약성 평가 자동 활성화에서 스토리지 생성을 StorageV2로 업그레이드</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1366">Upgraded storage creation in Vulnerability Assessment auto enablement to StorageV2</span></span>

#### <a name="azstorage"></a><span data-ttu-id="1d1eb-1367">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1367">Az.Storage</span></span>
* <span data-ttu-id="1d1eb-1368">Oauth 인증을 기반으로 스토리지 컨텍스트를 사용하여 Blob/컨테이너 ID 기반 SAS 토큰 생성 지원</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1368">Support generate Blob/Constainer Idenity based SAS token with Storage Context based on Oauth authentication</span></span>
    - <span data-ttu-id="1d1eb-1369">New-AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1369">New-AzStorageContainerSASToken</span></span>
    - <span data-ttu-id="1d1eb-1370">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1370">New-AzStorageBlobSASToken</span></span>
* <span data-ttu-id="1d1eb-1371">모든 Idenity SAS 토큰을 해지할 수 있도록 스토리지 계정 사용자 위임 키 해지 지원</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1371">Support revoke Storage Account User Delegation Keys, so all Idenity SAS tokens are revoked</span></span>
    - <span data-ttu-id="1d1eb-1372">Revoke-AzStorageAccountUserDelegationKeys</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1372">Revoke-AzStorageAccountUserDelegationKeys</span></span>
* <span data-ttu-id="1d1eb-1373">새로운 API 버전 2019-06-01을 지원하기 위해 Microsoft.Azure.Management.Storage 14.2.0으로 업그레이드.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1373">Upgrade to Microsoft.Azure.Management.Storage 14.2.0, to support new API version 2019-06-01.</span></span>
* <span data-ttu-id="1d1eb-1374">File Share cmdlet의 관리 평면에서 5120을 초과하는 값에 대해 QuotaGiB(Gibyby의 공유 할당량)를 지원하고 'Quota' 매개 변수 별칭을 'QuotaGiB' 매개 변수에 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1374">Support of QuotaGiB (Share Quota in Gibibye) for values of more than 5120 in the Management plane of File Share cmdlets and added the 'Quota' parameter alias to the 'QuotaGiB' parameter.</span></span>
    - <span data-ttu-id="1d1eb-1375">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1375">New-AzRmStorageShare</span></span>
    - <span data-ttu-id="1d1eb-1376">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1376">Update-AzRmStorageShare</span></span>
* <span data-ttu-id="1d1eb-1377">매개 변수 'Quota'에 매개 변수 별칭 'QuotaGiB' 추가</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1377">Add parameter alias 'QuotaGiB' to parameter 'Quota'</span></span>
    - <span data-ttu-id="1d1eb-1378">Set-AzStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1378">Set-AzStorageShareQuota</span></span>
* <span data-ttu-id="1d1eb-1379">Set-AzStorageContainerAcl가 저장된 액세스 정책을 정리할 수 있는 문제 수정</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1379">Fix the issue that Set-AzStorageContainerAcl can clean up the stored Access Policy</span></span>
    - <span data-ttu-id="1d1eb-1380">Set-AzStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1380">Set-AzStorageContainerAcl</span></span>

## <a name="310---november-2019"></a><span data-ttu-id="1d1eb-1381">3.1.0 - 2019년 11월</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1381">3.1.0 - November 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="1d1eb-1382">마지막 주 릴리스 이후의 주요 사항</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1382">Highlights since the last major release</span></span>
* <span data-ttu-id="1d1eb-1383">Az.DataBoxEdge 1.0.0 릴리스됨</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1383">Az.DataBoxEdge 1.0.0 released</span></span>
* <span data-ttu-id="1d1eb-1384">Az.SqlVirtualMachine 1.0.0 릴리스됨</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1384">Az.SqlVirtualMachine 1.0.0 released</span></span>

#### <a name="azcompute"></a><span data-ttu-id="1d1eb-1385">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1385">Az.Compute</span></span>
* <span data-ttu-id="1d1eb-1386">VM Reapply 기능</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1386">VM Reapply feature</span></span>
    - <span data-ttu-id="1d1eb-1387">Set-AzVM cmdlet에 Reapply 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1387">Add Reapply parameter to Set-AzVM cmdlet</span></span>
* <span data-ttu-id="1d1eb-1388">VM 확장 집합 AutomaticRepairs 기능:</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1388">VM Scale Set AutomaticRepairs feature:</span></span>
    - <span data-ttu-id="1d1eb-1389">다음 cmdlet에 EnableAutomaticRepair, AutomaticRepairGracePeriod 및 AutomaticRepairMaxInstanceRepairsPercent 매개 변수를 추가합니다.   New-AzVmssConfig   Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1389">Add EnableAutomaticRepair, AutomaticRepairGracePeriod, and AutomaticRepairMaxInstanceRepairsPercent parameters to the following cmdlets:   New-AzVmssConfig   Update-AzVmss</span></span>
* <span data-ttu-id="1d1eb-1390">New-AzVM에 대한 교차 테넌트 갤러리 이미지 지원</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1390">Cross tenant gallery image support for New-AzVM</span></span>
* <span data-ttu-id="1d1eb-1391">New-AzVM, New-AzVMConfig 및 New-AzVmss cmdlet의 Priority 매개 변수의 인수 완성자에 'Spot' 추가</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1391">Add 'Spot' to the argument completer of Priority parameter in New-AzVM, New-AzVMConfig and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="1d1eb-1392">Add-AzVmssDataDisk cmdlet에 DiskIOPSReadWrite 및 DiskMBpsReadWrite 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1392">Add DiskIOPSReadWrite and DiskMBpsReadWrite parameters to Add-AzVmssDataDisk cmdlet</span></span>
* <span data-ttu-id="1d1eb-1393">New-AzGalleryImageVersion cmdlet의 SourceImageId 매개 변수를 선택 사항으로 변경</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1393">Change SourceImageId parameter of New-AzGalleryImageVersion cmdlet to optional</span></span>
* <span data-ttu-id="1d1eb-1394">New-AzGalleryImageVersion cmdlet에 OSDiskImage 및 DataDiskImage 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1394">Add OSDiskImage and DataDiskImage parameters to New-AzGalleryImageVersion cmdlet</span></span>
* <span data-ttu-id="1d1eb-1395">New-AzGalleryImageDefinition cmdlet에 HyperVGeneration 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1395">Add HyperVGeneration parameter to New-AzGalleryImageDefinition cmdlet</span></span>
* <span data-ttu-id="1d1eb-1396">New-AzVmss, New-AzVmssConfig 및 Update-AzVmss cmdlet에 SkipExtensionsOnOverprovisionedVMs 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1396">Add SkipExtensionsOnOverprovisionedVMs parameters to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="1d1eb-1397">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1397">Az.DataBoxEdge</span></span>
* <span data-ttu-id="1d1eb-1398">cmdlet `Get-AzDataBoxEdgeOrder` 추가됨</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1398">Added cmdlet `Get-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="1d1eb-1399">주문 가져오기</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1399">Get the Order</span></span>
* <span data-ttu-id="1d1eb-1400">cmdlet `New-AzDataBoxEdgeOrder` 추가됨</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1400">Added cmdlet `New-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="1d1eb-1401">새 주문 만들기</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1401">Create new Order</span></span>
* <span data-ttu-id="1d1eb-1402">cmdlet `Remove-AzDataBoxEdgeOrder` 추가됨</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1402">Added cmdlet `Remove-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="1d1eb-1403">주문 제거</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1403">Remove the Order</span></span>
* <span data-ttu-id="1d1eb-1404">cmdlet `New-AzDataBoxEdgeShare` 변경</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1404">Change in cmdlet `New-AzDataBoxEdgeShare`</span></span>
    - <span data-ttu-id="1d1eb-1405">이제 로컬 공유를 만듬</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1405">Now creates Local Share</span></span>
* <span data-ttu-id="1d1eb-1406">cmdlet `Set-AzDataBoxEdgeRole` 추가됨</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1406">Added cmdlet `Set-AzDataBoxEdgeRole`</span></span>
    - <span data-ttu-id="1d1eb-1407">이제 IotRole을 공유에 매핑할 수 있음</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1407">Now IotRole can be mapped to Share</span></span>
* <span data-ttu-id="1d1eb-1408">cmdlet `Invoke-AzDataBoxEdgeDevice` 추가됨</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1408">Added cmdlet `Invoke-AzDataBoxEdgeDevice`</span></span>
    - <span data-ttu-id="1d1eb-1409">스캔 업데이트 호출, 업데이트 다운로드, 디바이스에 업데이트 설치</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1409">Invoke scan update, download update, install updates on the device</span></span>
* <span data-ttu-id="1d1eb-1410">cmdlet `Get-AzDataBoxEdgeTrigger` 추가됨</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1410">Added cmdlet `Get-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="1d1eb-1411">트리거에 대한 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1411">Gets the information about Triggers</span></span>
* <span data-ttu-id="1d1eb-1412">cmdlet `New-AzDataBoxEdgeTrigger` 추가됨</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1412">Added cmdlet `New-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="1d1eb-1413">새 트리거 만들기</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1413">Create new Triggers</span></span>
* <span data-ttu-id="1d1eb-1414">cmdlet `Remove-AzDataBoxEdgeTrigger` 추가됨</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1414">Added cmdlet `Remove-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="1d1eb-1415">트리거 제거</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1415">Remove the Triggers</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="1d1eb-1416">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1416">Az.DataFactory</span></span>
* <span data-ttu-id="1d1eb-1417">ADF .Net SDK 버전을 4.4.0으로 업데이트</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1417">Update ADF .Net SDK version to 4.4.0</span></span>
* <span data-ttu-id="1d1eb-1418">'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd에 'ExpressCustomSetup' 매개 변수를 추가하여 사용자 지정 설치 스크립트 없이 설치 구성 및 타사 구성 요소를 사용하도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1418">Add parameter 'ExpressCustomSetup' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable setup configurations and 3rd party components without custom setup script.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="1d1eb-1419">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1419">Az.DataLakeStore</span></span>
* <span data-ttu-id="1d1eb-1420">Get-AzDataLakeStoreDeletedItem 및 Restore-AzDataLakeStoreDeletedItem의 설명서 업데이트</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1420">Update documentation of Get-AzDataLakeStoreDeletedItem and Restore-AzDataLakeStoreDeletedItem</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="1d1eb-1421">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1421">Az.EventHub</span></span>
* <span data-ttu-id="1d1eb-1422">10301 문제 해결: SAS 토큰 날짜 형식 수정</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1422">Fix for issue 10301 : Fix the SAS Token date format</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="1d1eb-1423">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1423">Az.FrontDoor</span></span>
* <span data-ttu-id="1d1eb-1424">Enable-AzFrontDoorCustomDomainHttps 및 New-AzFrontDoorFrontendEndpointObject에 MinimumTlsVersion 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1424">Add MinimumTlsVersion parameter to Enable-AzFrontDoorCustomDomainHttps and New-AzFrontDoorFrontendEndpointObject</span></span>
* <span data-ttu-id="1d1eb-1425">New-AzFrontDoorHealthProbeSettingObject에 HealthProbeMethod 및 EnabledState 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1425">Add HealthProbeMethod and EnabledState parameters to New-AzFrontDoorHealthProbeSettingObject</span></span>
* <span data-ttu-id="1d1eb-1426">BackendPoolsSettings 개체를 생성하여 Front Door 생성/업데이트에 전달하는 새 cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1426">Add new cmdlet to create BackendPoolsSettings objec to pass into creation/update of Front Door</span></span>
    - <span data-ttu-id="1d1eb-1427">New-AzFrontDoorBackendPoolsSettingObject</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1427">New-AzFrontDoorBackendPoolsSettingObject</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="1d1eb-1428">Az.Network</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1428">Az.Network</span></span>
* <span data-ttu-id="1d1eb-1429">'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' 및 'Start-AzVirtualnetworkGatewayPacketCapture.md' FilterData 옵션 예제를 변경합니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1429">Change 'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' and 'Start-AzVirtualnetworkGatewayPacketCapture.md' FilterData option examples.</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="1d1eb-1430">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1430">Az.PrivateDns</span></span>
* <span data-ttu-id="1d1eb-1431">PrivateDns .net sdk를 버전 1.0.0으로 업데이트함</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1431">Updated PrivateDns .net sdk to version 1.0.0</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="1d1eb-1432">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1432">Az.RecoveryServices</span></span>
* <span data-ttu-id="1d1eb-1433">보호를 사용하도록 설정할 때 디스크 유형을 선택하도록 Azure Site Recovery 지원</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1433">Azure Site Recovery support to select disk type at enabling protection.</span></span>
* <span data-ttu-id="1d1eb-1434">복구 계획 동작 편집을 위한 Azure Site Recovery 버그 수정</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1434">Azure Site Recovery bug fix for recovery plan action edit.</span></span>
* <span data-ttu-id="1d1eb-1435">파일 스트림 DB를 허용하도록 Azure Backup SQL 복원 지원</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1435">Azure Backup SQL Restore support to accept filestream DBs.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="1d1eb-1436">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1436">Az.RedisCache</span></span>
* <span data-ttu-id="1d1eb-1437">'New-AzRedisCache' 및 'Set-AzRedisCache' cmdlet에 'MinimumTlsVersion' 매개 변수가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1437">Added 'MinimumTlsVersion' parameter in 'New-AzRedisCache' and 'Set-AzRedisCache' cmdlets.</span></span> <span data-ttu-id="1d1eb-1438">'Get-AzRedisCache' cmdlet 출력에 'MinimumTlsVersion'도 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1438">Also, added 'MinimumTlsVersion' in the output of 'Get-AzRedisCache' cmdlet.</span></span>
* <span data-ttu-id="1d1eb-1439">'Set-AzRedisCache' 및 'New-AzRedisCache' cmdlet의 '-Size' 매개 변수에 대한 유효성 검사가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1439">Added validation on '-Size' parameter for 'Set-AzRedisCache' and 'New-AzRedisCache' cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="1d1eb-1440">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1440">Az.Resources</span></span>
- <span data-ttu-id="1d1eb-1441">정책 할당에 새로운 EnforcementMode 속성이 있는 새 api 버전 2019-06-01을 사용하도록 정책 cmdlet이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1441">Updated policy cmdlets to use new api version 2019-06-01 that has new EnforcementMode property in policy assignment.</span></span>
- <span data-ttu-id="1d1eb-1442">정책 정의 만들기 도움말 예제가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1442">Updated create policy definition help example</span></span>
- <span data-ttu-id="1d1eb-1443">Remove-AZADServicePrincipal -ServicePrincipalName 버그를 수정하고, 서비스 사용자 이름을 찾을 수 없으면 null 참조를 throw합니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1443">Fix bug Remove-AZADServicePrincipal -ServicePrincipalName, throw null reference when service principal name not found.</span></span>
- <span data-ttu-id="1d1eb-1444">New-AZADServicePrincipal 버그를 수정하고, 테넌트에 구독이 없으면 null 참조를 throw합니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1444">Fix bug New-AZADServicePrincipal, throw null reference when tenant doesn't have any subscription.</span></span>
- <span data-ttu-id="1d1eb-1445">연결된 애플리케이션에만 자격 증명을 추가하도록 New-AzAdServicePrincipal을 변경합니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1445">Change New-AzAdServicePrincipal to add credentials only to associated application.</span></span>

#### <a name="azsql"></a><span data-ttu-id="1d1eb-1446">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1446">Az.Sql</span></span>
* <span data-ttu-id="1d1eb-1447">데이터베이스 ReadReplicaCount에 대한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1447">Added support for database ReadReplicaCount.</span></span>
* <span data-ttu-id="1d1eb-1448">영역 중복이 설정되지 않은 경우 Set-AzSqlDatabase가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1448">Fixed Set-AzSqlDatabase when zone redundancy not set</span></span>

## <a name="300---november-2019"></a><span data-ttu-id="1d1eb-1449">3.0.0 - 2019년 11월</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1449">3.0.0 - November 2019</span></span>
### <a name="general"></a><span data-ttu-id="1d1eb-1450">일반</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1450">General</span></span>
* <span data-ttu-id="1d1eb-1451">Az.PrivateDns 1.0.0 릴리스</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1451">Az.PrivateDns 1.0.0 released</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="1d1eb-1452">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1452">Az.Accounts</span></span>
* <span data-ttu-id="1d1eb-1453">'Resolve-Error' 별칭에 사용 중단 메시지를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1453">Add a deprecation message for 'Resolve-Error' alias.</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="1d1eb-1454">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1454">Az.Advisor</span></span>
* <span data-ttu-id="1d1eb-1455">Get-AzAdvisorRecommendation cmdlet에 새로운 '운영 효율성' 범주가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1455">Added new category 'Operational Excellence' to Get-AzAdvisorRecommendation cmdlet.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="1d1eb-1456">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1456">Az.Batch</span></span>
* <span data-ttu-id="1d1eb-1457">`BatchAccountContext`의 `CoreQuota` 이름이 `DedicatedCoreQuota`로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1457">Renamed `CoreQuota` on `BatchAccountContext` to `DedicatedCoreQuota`.</span></span> <span data-ttu-id="1d1eb-1458">또한 `LowPriorityCoreQuota`가 새로 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1458">There is also a new `LowPriorityCoreQuota`.</span></span>
  - <span data-ttu-id="1d1eb-1459">이 변경 사항은 **Get-AzBatchAccount** 에 영향을 줍니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1459">This impacts **Get-AzBatchAccount**.</span></span>
* <span data-ttu-id="1d1eb-1460">이제 **New-AzBatchTask** `-ResourceFile` 매개 변수는 새로운 **New-AzBatchResourceFile** cmdlet을 사용하여 구성할 수 있는 `PSResourceFile` 개체의 컬렉션을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1460">**New-AzBatchTask** `-ResourceFile` parameter now takes a collection of `PSResourceFile` objects, which can be constructed using the new **New-AzBatchResourceFile** cmdlet.</span></span>
* <span data-ttu-id="1d1eb-1461">새로운 **New-AzBatchResourceFile** cmdlet을 통해 `PSResourceFile` 개체를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1461">New **New-AzBatchResourceFile** cmdlet to help create `PSResourceFile` objects.</span></span> <span data-ttu-id="1d1eb-1462">이들은 `-ResourceFile` 매개 변수의 **New-AzBatchTask** 에 제공될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1462">These can be supplied to **New-AzBatchTask** on the `-ResourceFile` parameter.</span></span>
  - <span data-ttu-id="1d1eb-1463">그에 따라 기존 `HttpUrl` 방법 외에도 두 가지 종류의 리소스 파일이 새롭게 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1463">This supports two new kinds of resource file in addition to the existing `HttpUrl` way:</span></span>
    - <span data-ttu-id="1d1eb-1464">`AutoStorageContainerName` 기반 리소스 파일은 전체 자동 스토리지 컨테이너를 일괄 처리 노드에 다운로드합니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1464">`AutoStorageContainerName` based resource files download an entire auto-storage container to the Batch node.</span></span>
    - <span data-ttu-id="1d1eb-1465">`StorageContainerUrl` 기반 리소스 파일은 URL에 지정된 컨테이너를 일괄 처리 노드에 다운로드합니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1465">`StorageContainerUrl` based resource files download the container specified in the URL to the Batch node.</span></span>
* <span data-ttu-id="1d1eb-1466">**Get-AzBatchApplication** 으로 반환되는 `PSApplication`의 `ApplicationPackages` 속성이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1466">Removed `ApplicationPackages` property of `PSApplication` returned by **Get-AzBatchApplication**.</span></span>
  - <span data-ttu-id="1d1eb-1467">이제 **Get-AzBatchApplicationPackage** 를 사용하여 애플리케이션 내부의 특정 패키지를 검색할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1467">The specific packages inside of an application now can be retrieved using **Get-AzBatchApplicationPackage**.</span></span> <span data-ttu-id="1d1eb-1468">예: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1468">For example: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span></span>
* <span data-ttu-id="1d1eb-1469">**Get-AzBatchApplicationPackage** , **New-AzBatchApplicationPackage** , **Remove-AzBatchApplicationPackage** , **Get-AzBatchApplication** , **New-AzBatchApplication** , **Remove-AzBatchApplication** 및 **Set-AzBatchApplication** 에서 `ApplicationId` 이름이 `ApplicationName`으로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1469">Renamed `ApplicationId` to `ApplicationName` on **Get-AzBatchApplicationPackage** , **New-AzBatchApplicationPackage** , **Remove-AzBatchApplicationPackage** , **Get-AzBatchApplication** , **New-AzBatchApplication** , **Remove-AzBatchApplication** , and **Set-AzBatchApplication**.</span></span>
  - <span data-ttu-id="1d1eb-1470">이제 `ApplicationId`는 `ApplicationName`의 별칭입니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1470">`ApplicationId` now is an alias of `ApplicationName`.</span></span>
* <span data-ttu-id="1d1eb-1471">새로운 `PSWindowsUserConfiguration` 속성이 `PSUserAccount`에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1471">Added new `PSWindowsUserConfiguration` property to `PSUserAccount`.</span></span>
* <span data-ttu-id="1d1eb-1472">`PSApplicationPackage`에서 `Version` 이름이 `Name`으로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1472">Renamed `Version` to `Name` on `PSApplicationPackage`.</span></span>
* <span data-ttu-id="1d1eb-1473">`PSResourceFile`에서 `BlobSource` 이름이 `HttpUrl`으로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1473">Renamed `BlobSource` to `HttpUrl` on `PSResourceFile`.</span></span>
* <span data-ttu-id="1d1eb-1474">`PSVirtualMachineConfiguration`에서 `OSDisk` 속성이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1474">Removed `OSDisk` property from `PSVirtualMachineConfiguration`.</span></span>
* <span data-ttu-id="1d1eb-1475">**Set-AzBatchPoolOSVersion** 이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1475">Removed **Set-AzBatchPoolOSVersion**.</span></span> <span data-ttu-id="1d1eb-1476">이 작업은 더 이상 지원되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1476">This operation is no longer supported.</span></span>
* <span data-ttu-id="1d1eb-1477">`PSCloudServiceConfiguration`에서 `TargetOSVersion`이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1477">Removed `TargetOSVersion` from `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="1d1eb-1478">`PSCloudServiceConfiguration`에서 `CurrentOSVersion` 이름이 `OSVersion`으로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1478">Renamed `CurrentOSVersion` to `OSVersion` on `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="1d1eb-1479">`PSPoolUsageMetrics`에서 `DataEgressGiB` 및 `DataIngressGiB`가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1479">Removed `DataEgressGiB` and `DataIngressGiB` from `PSPoolUsageMetrics`.</span></span>
* <span data-ttu-id="1d1eb-1480">**Get-AzBatchNodeAgentSku** 가 제거되고 **Get-AzBatchSupportedImage** 로 대체되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1480">Removed **Get-AzBatchNodeAgentSku** and replaced it with  **Get-AzBatchSupportedImage**.</span></span>
  - <span data-ttu-id="1d1eb-1481">**Get-AzBatchSupportedImage** 가 **Get-AzBatchNodeAgentSku** 와 동일한 데이터를 반환하지만 더 친숙한 형식이 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1481">**Get-AzBatchSupportedImage** returns the same data as **Get-AzBatchNodeAgentSku** but in a more friendly format.</span></span>
  - <span data-ttu-id="1d1eb-1482">이제 확인되지 않은 이미지도 새롭게 반환됩니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1482">New non-verified images are also now returned.</span></span> <span data-ttu-id="1d1eb-1483">각 이미지의 `Capabilities` 및 `BatchSupportEndOfLife`에 대한 추가 정보도 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1483">Additional information about `Capabilities` and `BatchSupportEndOfLife` for each image is also included.</span></span>
* <span data-ttu-id="1d1eb-1484">**New-AzBatchPool** 의 새로운 `MountConfiguration` 매개 변수를 통해 풀의 각 노드에서 원격 파일 시스템을 마운트할 수 있는 기능이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1484">Added ability to mount remote file-systems on each node of a pool via the new `MountConfiguration` parameter of **New-AzBatchPool**.</span></span>
* <span data-ttu-id="1d1eb-1485">이제 트래픽의 소스 포트를 기준으로 풀에 대한 네트워크 액세스를 차단하는 네트워크 보안 규칙이 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1485">Now support network security rules blocking network access to a pool based on the source port of the traffic.</span></span> <span data-ttu-id="1d1eb-1486">이 작업은 `PSNetworkSecurityGroupRule`에서 `SourcePortRanges` 속성을 통해 수행됩니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1486">This is done via the `SourcePortRanges` property on `PSNetworkSecurityGroupRule`.</span></span>
* <span data-ttu-id="1d1eb-1487">컨테이너를 실행할 때 Batch는 이제 컨테이너 작업 디렉터리 또는 일괄 처리 태스크 작업 디렉터리에서 작업 실행을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1487">When running a container, Batch now supports executing the task in the container working directory or in the Batch task working directory.</span></span> <span data-ttu-id="1d1eb-1488">이 작업은 `PSTaskContainerSettings`에서 `WorkingDirectory` 속성에 의해 제어됩니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1488">This is controlled by the `WorkingDirectory` property on `PSTaskContainerSettings`.</span></span>
* <span data-ttu-id="1d1eb-1489">새로운 `PublicIPs` 속성을 통해 `PSNetworkConfiguration`에서 공용 IP의 컬렉션을 지정할 수 있는 기능이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1489">Added ability to specify a collection of public IPs on `PSNetworkConfiguration` via the new `PublicIPs` property.</span></span> <span data-ttu-id="1d1eb-1490">그 결과 사용자 제공 IP 목록의 IP가 풀에 있는 노드에 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1490">This guarantees nodes in the Pool will have an IP from the list user provided IPs.</span></span>
* <span data-ttu-id="1d1eb-1491">지정하지 않은 경우 이제 `PSSTartTask`에서 `WaitForSuccess`의 기본값은 `$True`입니다(이전에는 `$False`).</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1491">When not specified, the default value of `WaitForSuccess` on `PSSTartTask` is now `$True` (was `$False`).</span></span>
* <span data-ttu-id="1d1eb-1492">지정하지 않은 경우 이제 `PSAutoUserSpecification`에서 `Scope`의 기본값은 `Pool`입니다(이전에는 Windows의 경우 `Task`, Linux의 경우에는 `Pool`).</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1492">When not specified, the default value of `Scope` on `PSAutoUserSpecification` is now `Pool` (was `Task` on Windows and `Pool` on Linux).</span></span>

#### <a name="azcdn"></a><span data-ttu-id="1d1eb-1493">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1493">Az.Cdn</span></span>
* <span data-ttu-id="1d1eb-1494">RulesEngine에 UrlRewriteAction 및 CacheKeyQueryStringAction이 도입되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1494">Introduced UrlRewriteAction and CacheKeyQueryStringAction to RulesEngine.</span></span>
* <span data-ttu-id="1d1eb-1495">New-AzDeliveryRuleCondition cmdlet에서 'Selector' 입력 누락과 같은 여러 버그가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1495">Fixed several bugs like missing 'Selector' Input in New-AzDeliveryRuleCondition cmdlet.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="1d1eb-1496">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1496">Az.Compute</span></span>
* <span data-ttu-id="1d1eb-1497">디스크 암호화 집합 기능</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1497">Disk Encryption Set feature</span></span>
    - <span data-ttu-id="1d1eb-1498">새 cmdlet:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1498">New cmdlets:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span></span>
    - <span data-ttu-id="1d1eb-1499">DiskEncryptionSetId 매개 변수가 다음 cmdlet에 추가되었습니다.   Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1499">DiskEncryptionSetId parameter is added to the following cmdlets:   Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span></span>
    - <span data-ttu-id="1d1eb-1500">DiskEncryptionSetId 및 EncryptionType 매개 변수가 다음 cmdlet에 추가되었습니다.   New-AzDiskConfig   New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1500">DiskEncryptionSetId and EncryptionType parameters are added to the following cmdlets:   New-AzDiskConfig   New-AzSnapshotConfig</span></span>
* <span data-ttu-id="1d1eb-1501">New-AzVmssIPConfig에 PublicIPAddressVersion 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1501">Add PublicIPAddressVersion parameter to New-AzVmssIPConfig</span></span>
* <span data-ttu-id="1d1eb-1502">사용자 지정 스크립트 확장의 FileUris를 공용 설정에서 보호된 설정으로 이동</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1502">Move FileUris of custom script extension from public setting to protected setting</span></span>
* <span data-ttu-id="1d1eb-1503">New-AzVmss, New-AzVmssConfig 및 Update-AzVmss cmdlet에 ScaleInPolicy 추가</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1503">Add ScaleInPolicy to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>
* <span data-ttu-id="1d1eb-1504">주요 변경 내용</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1504">Breaking changes</span></span>
    - <span data-ttu-id="1d1eb-1505">CreateOption이 업로드일 때 UploadSizeInBytes 매개 변수가 New-AzDiskConfig에 대해 DiskSizeGB 대신 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1505">UploadSizeInBytes parameter is used instead of DiskSizeGB for New-AzDiskConfig when CreateOption is Upload</span></span>
    - <span data-ttu-id="1d1eb-1506">GalleryImageVersion 개체에서 PublishingProfile.Source.ManagedImage.Id가 StorageProfile.Source.Id로 바뀝니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1506">PublishingProfile.Source.ManagedImage.Id is replaced with StorageProfile.Source.Id in GalleryImageVersion object</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="1d1eb-1507">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1507">Az.DataFactory</span></span>
* <span data-ttu-id="1d1eb-1508">ADF .Net SDK 버전을 4.3.0으로 업데이트</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1508">Update ADF .Net SDK version to 4.3.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="1d1eb-1509">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1509">Az.DataLakeStore</span></span>
* <span data-ttu-id="1d1eb-1510">ADLS SDK 버전 업데이트(https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha) , 다음 수정 사항 제공</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1510">Update ADLS SDK version (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), brings following fixes</span></span>
* <span data-ttu-id="1d1eb-1511">휴지통 또는 디렉터리 항목의 creationtime을 역직렬화할 수 없을 때 예외가 발생하지 않도록 방지합니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1511">Avoid throwing exception while unable to deserialize the creationtime of the trash or directory entry.</span></span>
* <span data-ttu-id="1d1eb-1512">adlsclient에서 요청별 시간 제한 설정 노출</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1512">Expose setting per request timeout in adlsclient</span></span>
* <span data-ttu-id="1d1eb-1513">badoffset 복구를 위한 원본 syncflag 전달 수정</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1513">Fix passing the original syncflag for badoffset recovery</span></span>
* <span data-ttu-id="1d1eb-1514">응답이 확인된 후 연속 토큰을 검색하기 위한 EnumerateDirectory 수정</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1514">Fix EnumerateDirectory to retrieve continuation token once response is checked</span></span>
* <span data-ttu-id="1d1eb-1515">Concat 버그 수정</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1515">Fix Concat Bug</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="1d1eb-1516">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1516">Az.FrontDoor</span></span>
* <span data-ttu-id="1d1eb-1517">모듈 간 기타 오타가 수정됨</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1517">Fixed miscellaneous typos across module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="1d1eb-1518">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1518">Az.HDInsight</span></span>
* <span data-ttu-id="1d1eb-1519">ADLSGen1 스토리지가 포함된 클러스터를 가져오기 위해 Get-AzHDInsightCluster를 사용할 때 고객에게 '올바른 Base-64 문자열이 아닙니다' 오류가 표시되는 버그가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1519">Fixed the bug that customer will get 'Not a valid Base-64 string' error when using Get-AzHDInsightCluster to get the cluster with ADLSGen1 storage.</span></span>
* <span data-ttu-id="1d1eb-1520">고객이 Azure Data Lake에 액세스하기 위해 서비스 주체 애플리케이션 ID를 제공할 수 있도록 세 가지 cmdlet Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig 및 New-AzHDInsightCluster에 이름이 'ApplicationId'인 매개 변수를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1520">Add a parameter named 'ApplicationId' to three cmdlets Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig and New-AzHDInsightCluster so that customer can provide the service principal application id for accessing Azure Data Lake.</span></span>
* <span data-ttu-id="1d1eb-1521">Microsoft.Azure.Management.HDInsight가 2.1.0에서 5.1.0으로 변경됨</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1521">Changed Microsoft.Azure.Management.HDInsight from 2.1.0 to 5.1.0</span></span>
* <span data-ttu-id="1d1eb-1522">다음 5가지 cmdlet이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1522">Removed five cmdlets:</span></span>
    - <span data-ttu-id="1d1eb-1523">Get-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1523">Get-AzHDInsightOMS</span></span>
    - <span data-ttu-id="1d1eb-1524">Enable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1524">Enable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="1d1eb-1525">Disable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1525">Disable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="1d1eb-1526">Grant-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1526">Grant-AzHDInsightRdpServicesAccess</span></span>
    - <span data-ttu-id="1d1eb-1527">Revoke-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1527">Revoke-AzHDInsightRdpServicesAccess</span></span>
* <span data-ttu-id="1d1eb-1528">다음 3가지 cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1528">Added three cmdlets:</span></span>
    - <span data-ttu-id="1d1eb-1529">Get-AzHDInsightOMS 대신 Get-AzHDInsightMonitoring</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1529">Get-AzHDInsightMonitoring to replace Get-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="1d1eb-1530">Get-AzHDInsightOMS 대신 Get-AzHDInsightMonitoring</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1530">Enable-AzHDInsightMonitoring to replace Enable-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="1d1eb-1531">Disable-AzHDInsightOMS 대신 Disable-AzHDInsightMonitoring</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1531">Disable-AzHDInsightMonitoring to replace Disable-AzHDInsightOMS.</span></span>
* <span data-ttu-id="1d1eb-1532">특정 위치의 기능 정보 가져오기를 지원하도록 cmdlet Get-AzHDInsightProperties가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1532">Fixed cmdlet Get-AzHDInsightProperties to support get capabilities information from a specific location.</span></span>
* <span data-ttu-id="1d1eb-1533">Add-AzHDInsightConfigValue에서 매개 변수 집합('Spark1', 'Spark2')이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1533">Removed parameter sets('Spark1', 'Spark2') from Add-AzHDInsightConfigValue.</span></span>
* <span data-ttu-id="1d1eb-1534">cmdlet Add-AzHDInsightSecurityProfile의 도움말 문서에 예제를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1534">Add examples to the help documents of cmdlet Add-AzHDInsightSecurityProfile.</span></span>
* <span data-ttu-id="1d1eb-1535">다음 cmdlet의 출력 유형이 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1535">Changed output type of the following cmdlets:</span></span>
*  - <span data-ttu-id="1d1eb-1536">Get-AzHDInsightProperties의 출력 유형이 CapabilitiesResponse에서 AzureHDInsightCapabilities로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1536">Changed the output type of Get-AzHDInsightProperties from  CapabilitiesResponse to AzureHDInsightCapabilities.</span></span>
*  - <span data-ttu-id="1d1eb-1537">Remove-AzHDInsightCluster의 출력 유형이 ClusterGetResponse에서 bool로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1537">Changed the output type of Remove-AzHDInsightCluster from ClusterGetResponse to bool.</span></span>
*  - <span data-ttu-id="1d1eb-1538">Set-AzHDInsightGatewaySettings의 출력 유형이 HttpConnectivitySettings에서 GatewaySettings로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1538">Changed the output type of Set-AzHDInsightGatewaySettings HttpConnectivitySettings to GatewaySettings.</span></span>
* <span data-ttu-id="1d1eb-1539">몇 가지 시나리오 테스트 사례가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1539">Added some scenario test cases.</span></span>
* <span data-ttu-id="1d1eb-1540">일부 별칭 제거: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1540">Remove some alias: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="1d1eb-1541">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1541">Az.IotHub</span></span>
* <span data-ttu-id="1d1eb-1542">주요 변경 내용:</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1542">Breaking changes:</span></span>
    - <span data-ttu-id="1d1eb-1543">'Add-AzIotHubEventHubConsumerGroup' cmdlet이 'EventHubEndpointName' 매개 변수를 더 이상 지원하지 않으며 원래 매개 변수 이름에 대해 별칭을 찾을 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1543">The cmdlet 'Add-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="1d1eb-1544">'Add-AzIotHubEventHubConsumerGroup' cmdlet에 대한 매개 변수 집합 '__AllParameterSets'가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1544">The parameter set '__AllParameterSets' for cmdlet 'Add-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="1d1eb-1545">'Get-AzIotHubEventHubConsumerGroup' cmdlet이 'EventHubEndpointName' 매개 변수를 더 이상 지원하지 않으며 원래 매개 변수 이름에 대해 별칭을 찾을 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1545">The cmdlet 'Get-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="1d1eb-1546">'Get-AzIotHubEventHubConsumerGroup' cmdlet에 대한 매개 변수 집합 '__AllParameterSets'가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1546">The parameter set '__AllParameterSets' for cmdlet 'Get-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="1d1eb-1547">'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' 유형의 'OperationsMonitoringProperties' 속성이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1547">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' has been removed.</span></span>
    - <span data-ttu-id="1d1eb-1548">'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' 유형의 'OperationsMonitoringProperties' 속성이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1548">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' has been removed.</span></span>
    - <span data-ttu-id="1d1eb-1549">'New-AzIotHubExportDevice' cmdlet이 더 이상 'New-AzIotHubExportDevices' 별칭을 지원하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1549">The cmdlet 'New-AzIotHubExportDevice' no longer supports the alias 'New-AzIotHubExportDevices'.</span></span>
    - <span data-ttu-id="1d1eb-1550">'New-AzIotHubImportDevice' cmdlet이 더 이상 'New-AzIotHubImportDevices' 별칭을 지원하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1550">The cmdlet 'New-AzIotHubImportDevice' no longer supports the alias 'New-AzIotHubImportDevices'.</span></span>
    - <span data-ttu-id="1d1eb-1551">'Remove-AzIotHubEventHubConsumerGroup' cmdlet이 'EventHubEndpointName' 매개 변수를 더 이상 지원하지 않으며 원래 매개 변수 이름에 대해 별칭을 찾을 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1551">The cmdlet 'Remove-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="1d1eb-1552">'Remove-AzIotHubEventHubConsumerGroup' cmdlet에 대한 매개 변수 집합 '__AllParameterSets'가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1552">The parameter set '__AllParameterSets' for cmdlet 'Remove-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="1d1eb-1553">'Set-AzIotHub' cmdlet이 'OperationsMonitoringProperties' 매개 변수를 더 이상 지원하지 않으며 원래 매개 변수 이름에 대해 별칭을 찾을 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1553">The cmdlet 'Set-AzIotHub' no longer supports the parameter 'OperationsMonitoringProperties' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="1d1eb-1554">'Set-AzIotHub' cmdlet에 대한 매개 변수 집합 'UpdateOperationsMonitoringProperties'가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1554">The parameter set 'UpdateOperationsMonitoringProperties' for cmdlet 'Set-AzIotHub' has been removed.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="1d1eb-1555">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1555">Az.RecoveryServices</span></span>
* <span data-ttu-id="1d1eb-1556">Azure Site Recovery가 Azure-Azure를 위한 NSG, 공용 IP 및 내부 부하 분산 장치와 같은 네트워킹 리소스 구성을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1556">Azure Site Recovery support to configure networking resources like NSG, public IP and internal load balancers for Azure to Azure.</span></span>
* <span data-ttu-id="1d1eb-1557">Azure Site Recovery가 vMWare-Azure를 위한 관리 디스크에 쓰기를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1557">Azure Site Recovery Support to write to managed disk for vMWare to Azure.</span></span>
* <span data-ttu-id="1d1eb-1558">Azure Site Recovery가 vMWare-Azure를 위한 NIC 감소를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1558">Azure Site Recovery Support to NIC reduction for vMWare to Azure.</span></span>
* <span data-ttu-id="1d1eb-1559">Azure Site Recovery가 Azure-Azure를 위한 가속 네트워킹을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1559">Azure Site Recovery Support to accelerated networking for Azure to Azure.</span></span>
* <span data-ttu-id="1d1eb-1560">Azure Site Recovery가 Azure-Azure를 위한 에이전트 자동 업데이트를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1560">Azure Site Recovery Support to agent auto update for Azure to Azure.</span></span>
* <span data-ttu-id="1d1eb-1561">Azure Site Recovery가 Azure-Azure를 위한 표준 SSD를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1561">Azure Site Recovery Support to Standard SSD for Azure to Azure.</span></span>
* <span data-ttu-id="1d1eb-1562">Azure Site Recovery가 Azure-Azure를 위한 두 가지 Azure 디스크 암호화 전달을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1562">Azure Site Recovery Support to Azure Disk Encryption two pass for Azure to Azure.</span></span>
* <span data-ttu-id="1d1eb-1563">Azure Site Recovery가 Azure-Azure를 위한 새로 추가된 디스크 보호를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1563">Azure Site Recovery Support to protect newly added disk for Azure to Azure.</span></span>
* <span data-ttu-id="1d1eb-1564">VM을 위한 SoftDelete 기능 및 softdelete를 위한 테스트가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1564">Added SoftDelete feature for VM and added tests for softdelete</span></span>

#### <a name="azresources"></a><span data-ttu-id="1d1eb-1565">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1565">Az.Resources</span></span>
* <span data-ttu-id="1d1eb-1566">종속성 어셈블리 Microsoft.Extensions.Caching.Memory가 1.1.1에서 2.2로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1566">Update dependency assembly Microsoft.Extensions.Caching.Memory from 1.1.1 to 2.2</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="1d1eb-1567">Az.Network</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1567">Az.Network</span></span>
* <span data-ttu-id="1d1eb-1568">일반 서비스 공급자 지원을 위해 PrivateEndpointConnection에 대한 모든 cmdlet이 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1568">Change all cmdlets for PrivateEndpointConnection to support generic service provider.</span></span>
    - <span data-ttu-id="1d1eb-1569">업데이트된 cmdlet:</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1569">Updated cmdlet:</span></span>
        - <span data-ttu-id="1d1eb-1570">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1570">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="1d1eb-1571">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1571">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="1d1eb-1572">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1572">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="1d1eb-1573">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1573">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="1d1eb-1574">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1574">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="1d1eb-1575">PrivateLinkResource에 대한 새 cmdlet이 추가되었고 일반 서비스 공급자도 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1575">Add new cmdlet for PrivateLinkResource and it also support generic service provider.</span></span>
    - <span data-ttu-id="1d1eb-1576">새 cmdlet:</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1576">New cmdlet:</span></span>
        - <span data-ttu-id="1d1eb-1577">Get-AzPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1577">Get-AzPrivateLinkResource</span></span>
* <span data-ttu-id="1d1eb-1578">Proxy Protocol V2 기능에 대한 새 필드 및 매개 변수가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1578">Add new fields and parameter for the feature Proxy Protocol V2.</span></span>
    - <span data-ttu-id="1d1eb-1579">PrivateLinkService에서 EnableProxyProtocol 속성 추가</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1579">Add property EnableProxyProtocol in PrivateLinkService</span></span>
    - <span data-ttu-id="1d1eb-1580">PrivateEndpointConnection에서 LinkIdentifier 속성 추가</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1580">Add property LinkIdentifier in PrivateEndpointConnection</span></span>
    - <span data-ttu-id="1d1eb-1581">새로운 선택적인 매개 변수인 EnableProxyProtocol을 추가하도록 New-AzPrivateLinkService가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1581">Updated New-AzPrivateLinkService to add a new optional parameter EnableProxyProtocol.</span></span>
* <span data-ttu-id="1d1eb-1582">'New-AzApplicationGatewaySku' 참조 설명서의 잘못된 매개 변수 설명 수정</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1582">Fix incorrect parameter description in 'New-AzApplicationGatewaySku' reference documentation</span></span>
* <span data-ttu-id="1d1eb-1583">Azure 방화벽 정책을 지원하는 새로운 cmdlet</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1583">New cmdlets to support the azure firewall policy</span></span>
* <span data-ttu-id="1d1eb-1584">VirtualHub의 자식 리소스 RouteTables에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1584">Add support for child resource RouteTables of VirtualHub</span></span>
    - <span data-ttu-id="1d1eb-1585">추가된 새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1585">New cmdlets added:</span></span>
        - <span data-ttu-id="1d1eb-1586">Add-AzVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1586">Add-AzVirtualHubRoute</span></span>
        - <span data-ttu-id="1d1eb-1587">Add-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1587">Add-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="1d1eb-1588">Get-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1588">Get-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="1d1eb-1589">Remove-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1589">Remove-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="1d1eb-1590">Set-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1590">Set-AzVirtualHub</span></span>
* <span data-ttu-id="1d1eb-1591">VirtualHub의 새로운 속성 Sku 및 VirtualWan의 VirtualWANType에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1591">Add support for new properties Sku of VirtualHub and VirtualWANType of VirtualWan</span></span>
    - <span data-ttu-id="1d1eb-1592">선택적 매개 변수로 다음 cmdlet이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1592">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="1d1eb-1593">New-AzVirtualHub: 추가된 매개 변수 Sku</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1593">New-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="1d1eb-1594">Update-AzVirtualHub: 추가된 매개 변수 Sku</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1594">Update-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="1d1eb-1595">New-AzVirtualWan: 추가된 매개 변수 VirtualWANType</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1595">New-AzVirtualWan : added parameter VirtualWANType</span></span>
        - <span data-ttu-id="1d1eb-1596">Update-AzVirtualWan: 추가된 매개 변수 VirtualWANType</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1596">Update-AzVirtualWan : added parameter VirtualWANType</span></span>
* <span data-ttu-id="1d1eb-1597">HubVnetConnection, VpnConnection 및 ExpressRouteConnection에 대한 EnableInternetSecurity 속성 지원 추가</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1597">Add support for EnableInternetSecurity property for HubVnetConnection, VpnConnection and ExpressRouteConnection</span></span>
    - <span data-ttu-id="1d1eb-1598">추가된 새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1598">New cmdlets added:</span></span>
        - <span data-ttu-id="1d1eb-1599">Update-AzureRmVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1599">Update-AzureRmVirtualHubVnetConnection</span></span>
    - <span data-ttu-id="1d1eb-1600">선택적 매개 변수로 다음 cmdlet이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1600">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="1d1eb-1601">New-AzureRmVirtualHubVnetConnection: 추가된 매개 변수 EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1601">New-AzureRmVirtualHubVnetConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="1d1eb-1602">New-AzureRmVpnConnection: 추가된 매개 변수 EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1602">New-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="1d1eb-1603">Update-AzureRmVpnConnection: 추가된 매개 변수 EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1603">Update-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="1d1eb-1604">New-AzureRmExpressRouteConnection: 추가된 매개 변수 EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1604">New-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="1d1eb-1605">Set-AzureRmExpressRouteConnection: 추가된 매개 변수 EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1605">Set-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
* <span data-ttu-id="1d1eb-1606">TopLevel WebApplicationFirewall 정책 구성을 위한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1606">Add support for Configuring TopLevel WebApplicationFirewall Policy</span></span>
    - <span data-ttu-id="1d1eb-1607">추가된 새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1607">New cmdlets added:</span></span>
        - <span data-ttu-id="1d1eb-1608">New-AzApplicationGatewayFirewallPolicySetting</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1608">New-AzApplicationGatewayFirewallPolicySetting</span></span>
        - <span data-ttu-id="1d1eb-1609">New-AzApplicationGatewayFirewallPolicyExclusion</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1609">New-AzApplicationGatewayFirewallPolicyExclusion</span></span>
        - <span data-ttu-id="1d1eb-1610">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1610">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span></span>
        - <span data-ttu-id="1d1eb-1611">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1611">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span></span>
        - <span data-ttu-id="1d1eb-1612">New-AzApplicationGatewayFirewallPolicyManagedRule</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1612">New-AzApplicationGatewayFirewallPolicyManagedRule</span></span>
        - <span data-ttu-id="1d1eb-1613">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1613">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span></span>
    - <span data-ttu-id="1d1eb-1614">선택적 매개 변수로 다음 cmdlet이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1614">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="1d1eb-1615">New-AzApplicationGatewayFirewallPolicy: 추가된 매개 변수 PolicySetting, ManagedRule</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1615">New-AzApplicationGatewayFirewallPolicy : added parameter PolicySetting, ManagedRule</span></span>
* <span data-ttu-id="1d1eb-1616">CustomRule에서 Geo-Match 연산자를 위한 지원 추가됨</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1616">Added support for Geo-Match operator on CustomRule</span></span>
    - <span data-ttu-id="1d1eb-1617">FirewallCondition에서 연산자에 GeoMatch 추가됨</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1617">Added GeoMatch to the operator on the FirewallCondition</span></span>
* <span data-ttu-id="1d1eb-1618">perListener 및 perSite 방화벽 규칙에 대한 지원 추가됨</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1618">Added support for perListener and perSite Firewall policy</span></span>
    - <span data-ttu-id="1d1eb-1619">선택적 매개 변수로 다음 cmdlet이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1619">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="1d1eb-1620">New-AzApplicationGatewayHttpListener: 추가된 매개 변수 FirewallPolicy, FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1620">New-AzApplicationGatewayHttpListener : added parameter FirewallPolicy, FirewallPolicyId</span></span>
        - <span data-ttu-id="1d1eb-1621">New-AzApplicationGatewayPathRuleConfig: 추가된 매개 변수 FirewallPolicy, FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1621">New-AzApplicationGatewayPathRuleConfig : added parameter FirewallPolicy, FirewallPolicyId</span></span>
* <span data-ttu-id="1d1eb-1622">'PSBastion'에서 이름이 AzureBastionSubnet인 필수 서브넷의 수정은 대소문자를 구분하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1622">Fix required subnet with name AzureBastionSubnet in 'PSBastion' can be case insensitive</span></span>
* <span data-ttu-id="1d1eb-1623">Azure Firewall을 위한 네트워크 규칙의 대상 FQDN 및 NAT 규칙의 번역된 FQDN 지원</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1623">Support for Destination FQDNs in Network Rules and Translated FQDN in NAT Rules for Azure Firewall</span></span>
* <span data-ttu-id="1d1eb-1624">IpGroup의 최상위 리소스 RouteTables에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1624">Add support for top level resource RouteTables of IpGroup</span></span>
    - <span data-ttu-id="1d1eb-1625">추가된 새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1625">New cmdlets added:</span></span>
        - <span data-ttu-id="1d1eb-1626">New-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1626">New-AzIpGroup</span></span>
        - <span data-ttu-id="1d1eb-1627">Remove-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1627">Remove-AzIpGroup</span></span>
        - <span data-ttu-id="1d1eb-1628">Get-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1628">Get-AzIpGroup</span></span>
        - <span data-ttu-id="1d1eb-1629">Set-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1629">Set-AzIpGroup</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="1d1eb-1630">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1630">Az.ServiceFabric</span></span>
* <span data-ttu-id="1d1eb-1631">Add-AzVmssSecret에서 지원되기 때문에 Add-AzServiceFabricApplicationCertificate cmdlet이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1631">Remove Add-AzServiceFabricApplicationCertificate cmdlet as this scenario is covered by Add-AzVmssSecret.</span></span>

#### <a name="azsql"></a><span data-ttu-id="1d1eb-1632">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1632">Az.Sql</span></span>
* <span data-ttu-id="1d1eb-1633">Managed Instances에서 삭제된 데이터베이스의 복원을 위한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1633">Added support for restore of dropped databases on Managed Instances.</span></span>
* <span data-ttu-id="1d1eb-1634">이전의 감사 cmdlet 코드가 사용되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1634">Deprecated from code old auditing cmdlets.</span></span>
* <span data-ttu-id="1d1eb-1635">사용되지 않는 별칭이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1635">Removed deprecated aliases:</span></span>
* <span data-ttu-id="1d1eb-1636">Get-AzSqlDatabaseIndexRecommendations(대신 Get-AzSqlDatabaseIndexRecommendation 사용)</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1636">Get-AzSqlDatabaseIndexRecommendations (use Get-AzSqlDatabaseIndexRecommendation instead)</span></span>
* <span data-ttu-id="1d1eb-1637">Get-AzSqlDatabaseRestorePoints(대신 Get-AzSqlDatabaseRestorePoint 사용)</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1637">Get-AzSqlDatabaseRestorePoints (use Get-AzSqlDatabaseRestorePoint instead)</span></span>
* <span data-ttu-id="1d1eb-1638">Get-AzSqlDatabaseSecureConnectionPolicy cmdlet 제거</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1638">Remove Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="1d1eb-1639">사용되지 않는 취약성 평가 설정 cmdlet에 대한 별칭 제거</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1639">Remove aliases for deprecated Vulnerability Assessment Settings cmdlets</span></span>
* <span data-ttu-id="1d1eb-1640">지능형 위협 탐지 설정 cmdlet 사용 중단</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1640">Deprecate Advanced Threat Detection Settings cmdlets</span></span>
* <span data-ttu-id="1d1eb-1641">데이터베이스의 열에 대한 민감도 권장 사항의 사용 여부를 제어하는 cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1641">Adding cmdlets to Disable and enable sensitivity recommendations on columns in a database.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="1d1eb-1642">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1642">Az.Storage</span></span>
* <span data-ttu-id="1d1eb-1643">스토리지 계정을 만들거나 업데이트할 때 큰 파일 공유 사용 지원</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1643">Support enable Large File share when create or update Storage account</span></span>
    -  <span data-ttu-id="1d1eb-1644">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1644">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="1d1eb-1645">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1645">Set-AzStorageAccount</span></span>
* <span data-ttu-id="1d1eb-1646">파일 핸들을 닫거나/가져올 때, DeletePending 상태의 개체로 인한 오류를 방지하기 위해 입력 경로가 파일 디렉터리인지 또는 파일인지를 확인하는 과정을 건너뜁니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1646">When close/get File handle, skip check the input path is File directory or File, to avoid failure with object in DeletePending status</span></span>
    -  <span data-ttu-id="1d1eb-1647">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1647">Get-AzStorageFileHandle</span></span>
    -  <span data-ttu-id="1d1eb-1648">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1648">Close-AzStorageFileHandle</span></span>

## <a name="280---october-2019"></a><span data-ttu-id="1d1eb-1649">2.8.0 - 2019년 10월</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1649">2.8.0 - October 2019</span></span>
### <a name="general"></a><span data-ttu-id="1d1eb-1650">일반</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1650">General</span></span>
* <span data-ttu-id="1d1eb-1651">Az.HealthcareApis 1.0.0 릴리스</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1651">Az.HealthcareApis 1.0.0 release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="1d1eb-1652">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1652">Az.Accounts</span></span>
* <span data-ttu-id="1d1eb-1653">생성된 모듈에 대한 원격 분석 및 URL 다시 작성이 업데이트되고, Windows 단위 테스트가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1653">Update telemetry and url rewriting for generated modules, fix windows unit tests.</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="1d1eb-1654">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1654">Az.ApiManagement</span></span>
* <span data-ttu-id="1d1eb-1655">**Set-AzApiManagementApi** - API 업데이트 지원이 ApiVersionSet에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1655">**Set-AzApiManagementApi** - Added support for Updating Api into ApiVersionSet</span></span>
    - <span data-ttu-id="1d1eb-1656">문제 https://github.com/Azure/azure-powershell/issues/10068 수정</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1656">Fix for issue https://github.com/Azure/azure-powershell/issues/10068</span></span>

#### <a name="azautomation"></a><span data-ttu-id="1d1eb-1657">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1657">Az.Automation</span></span>
* <span data-ttu-id="1d1eb-1658">Linux 다시 부팅 설정 매개 변수에 대한 New-AzureAutomationSoftwareUpdateConfiguration cmdlet이 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1658">Fixed New-AzureAutomationSoftwareUpdateConfiguration cmdlet for Linux reboot setting parameter.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="1d1eb-1659">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1659">Az.Batch</span></span>
* <span data-ttu-id="1d1eb-1660">**Get-AzBatchNodeAgentSku** 가 더 이상 사용되지 않으며, 2.0.0 버전의 **Get-AzBatchSupportImage** 로 대체되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1660">**Get-AzBatchNodeAgentSku** is deprecated and will be replaced by **Get-AzBatchSupportImage** in version 2.0.0.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="1d1eb-1661">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1661">Az.Compute</span></span>
* <span data-ttu-id="1d1eb-1662">Priority, EvictionPolicy 및 MaxPrice 매개 변수가 New-AzVM 및 New-AzVmss cmdlet에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1662">Add Priority, EvictionPolicy, and MaxPrice parameters to New-AzVM and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="1d1eb-1663">Add-AzVMAdditionalUnattendContent 및 Add-AzVMSshPublicKey cmdlet에 대한 경고 메시지와 도움말 문서가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1663">Fix warning message and help document for Add-AzVMAdditionalUnattendContent and Add-AzVMSshPublicKey cmdlets</span></span>
* <span data-ttu-id="1d1eb-1664">Set-AzVMDiskEncryptionExtension의 관리 디스크가 있는 Linux VM에 대한 -skipVmBackup 예외가 해결되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1664">Fix -skipVmBackup exception for Linux VMs with managed disks for Set-AzVMDiskEncryptionExtension.</span></span>
* <span data-ttu-id="1d1eb-1665">Set-AzVMDiskEncryptionExtension의 두 가지 패스 시나리오에서 발생하는 암호화 설정 업데이트의 버그가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1665">Fix bug in update encryption settings in Set-AzVMDiskEncryptionExtension, two pass scenario.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="1d1eb-1666">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1666">Az.DataFactory</span></span>
* <span data-ttu-id="1d1eb-1667">ADF V2 데이터 흐름에 대한 CRUD 명령으로 Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow 및 Get-AzDataFactoryV2DataFlow가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1667">Adding CRUD commands for ADF V2 data flow: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow, and Get-AzDataFactoryV2DataFlow.</span></span>
* <span data-ttu-id="1d1eb-1668">ADF V2 데이터 흐름 디버그 세션에 대한 작업 명령으로 Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand 및 Stop-AzDataFactoryV2DataFlowDebugSession이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1668">Adding action commands for ADF V2 data flow debug Session: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand and Stop-AzDataFactoryV2DataFlowDebugSession.</span></span>
* <span data-ttu-id="1d1eb-1669">ADF .Net SDK 버전이 4.2.0으로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1669">Update ADF .Net SDK version to 4.2.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="1d1eb-1670">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1670">Az.DataLakeStore</span></span>
* <span data-ttu-id="1d1eb-1671">도메인 없이 '-'가 있는 계정을 전달할 수 있도록 계정 유효성 검사가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1671">Fix account validation so that accounts with '-' can be passed without domain</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="1d1eb-1672">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1672">Az.HealthcareApis</span></span>
* <span data-ttu-id="1d1eb-1673">PowerShell 버전이 1.0.0으로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1673">Updated the powershell version to 1.0.0</span></span>
* <span data-ttu-id="1d1eb-1674">SDK 버전이 1.0.2로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1674">Updated the SDK version to 1.0.2</span></span>
* <span data-ttu-id="1d1eb-1675">새 SDK 버전을 참조하도록 테스트가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1675">Update in tests to refer to new SDK version</span></span>
* <span data-ttu-id="1d1eb-1676">출력이 중첩 구조에서 평면화 구조로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1676">Updated the output structure from nested to flattened.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="1d1eb-1677">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1677">Az.IotHub</span></span>
* <span data-ttu-id="1d1eb-1678">새 라우팅 원본 추가: DigitalTwinChangeEvents</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1678">Add new routing source: DigitalTwinChangeEvents</span></span>
* <span data-ttu-id="1d1eb-1679">사소한 버그 수정: Get-AzIothub에서 subscriptionId를 반환하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1679">Minor bug fix: Get-AzIothub not returning subscriptionId</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="1d1eb-1680">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1680">Az.Monitor</span></span>
* <span data-ttu-id="1d1eb-1681">작업 그룹에 대한 새 작업 그룹 수신기로 -ItsmReceiver, -VoiceReceiver, -ArmRoleReceiver, -AzureFunctionReceiver, -LogicAppReceiver, -AutomationRunbookReceiver, -AzureAppPushReceiver가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1681">New action group receivers added for action group   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span></span>
* <span data-ttu-id="1d1eb-1682">수신기에 사용하도록 설정된 일반 경고 스키마가 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1682">Use common alert schema enabled for the receivers.</span></span> <span data-ttu-id="1d1eb-1683">SMS, Azure 앱 푸시, ITSM 및 음성 수신기에는 적용되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1683">This is not applicable for SMS, Azure App push , ITSM and Voice recievers</span></span>
* <span data-ttu-id="1d1eb-1684">웹후크에서 이제 Azure Active Directory 인증을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1684">Webhooks now supports Azure active directory authentication .</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="1d1eb-1685">Az.Network</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1685">Az.Network</span></span>
* <span data-ttu-id="1d1eb-1686">서비스 엔드포인트 정책에 사용할 수 있는 별칭을 가져오기 위해 호출할 수 있는 새 Get-AzAvailableServiceAlias cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1686">Add new cmdlet Get-AzAvailableServiceAlias which can be called to get the aliases that can be used for Service Endpoint Policies.</span></span>
* <span data-ttu-id="1d1eb-1687">트래픽 선택기를 Virtual Network 게이트웨이 연결에 추가할 수 있는 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1687">Added support for the adding traffic selectors to Virtual Network Gateway Connections</span></span>
    - <span data-ttu-id="1d1eb-1688">추가된 새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1688">New cmdlets added:</span></span>
        - <span data-ttu-id="1d1eb-1689">New-AzureRmTrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1689">New-AzureRmTrafficSelectorPolicy</span></span>
    - <span data-ttu-id="1d1eb-1690">cmdlet이 선택적인 -TrafficSelectorPolicies, -New-AzureRmVirtualNetworkGatewayConnection, -Set-AzureRmVirtualNetworkGatewayConnection 매개 변수로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1690">Cmdlets updated with optional parameter -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="1d1eb-1691">ESP 및 AH 프로토콜 지원이 네트워크 보안 규칙 구성에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1691">Add support for ESP and AH protocols in network security rule configurations</span></span>
    - <span data-ttu-id="1d1eb-1692">다음 Cmdlet이 업데이트 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1692">Updated cmdlets:</span></span>
        - <span data-ttu-id="1d1eb-1693">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1693">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="1d1eb-1694">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1694">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="1d1eb-1695">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1695">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="1d1eb-1696">Cortex cmdlet의 예외 처리가 향상되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1696">Improve handling of exceptions in Cortex cmdlets</span></span>
* <span data-ttu-id="1d1eb-1697">새 VirtualNetworkGateways 세대 및 SKU</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1697">New Generations and SKUs for VirtualNetworkGateways</span></span>
  - <span data-ttu-id="1d1eb-1698">새 VirtualNetworkGateways 세대가 도입되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1698">Introduce new Generations for VirtualNetworkGateways.</span></span>
  - <span data-ttu-id="1d1eb-1699">높은 처리량의 새 VirtualNetworkGateways SKU가 도입되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1699">Introduce new high throughput SKUs for VirtualNetworkGateways.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="1d1eb-1700">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1700">Az.RedisCache</span></span>
* <span data-ttu-id="1d1eb-1701">'-Size' 매개 변수에 대한 누락 값을 포함하도록 'Set-AzRedisCache' 참조 설명서가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1701">Updated 'Set-AzRedisCache' reference documentation to include missing values for '-Size' parameter</span></span>

#### <a name="azsql"></a><span data-ttu-id="1d1eb-1702">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1702">Az.Sql</span></span>
* <span data-ttu-id="1d1eb-1703">Managed Instance에서 Active Directory 관리자를 설정할 수 있는 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1703">Add support for setting Active Directory Administrator on Managed Instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="1d1eb-1704">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1704">Az.Storage</span></span>
* <span data-ttu-id="1d1eb-1705">스토리지 클라이언트 라이브러리가 11.1.0으로 업그레이드되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1705">Upgrade Storage Client Library to 11.1.0</span></span>
* <span data-ttu-id="1d1eb-1706">관리 평면 API를 사용하여 컨테이너를 나열하면 NextPageLink를 통해 나열됩니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1706">List containers with Management plane API, will list with NextPageLink</span></span>
    -  <span data-ttu-id="1d1eb-1707">Get-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1707">Get-AzRmStorageContainer</span></span>
* <span data-ttu-id="1d1eb-1708">구독에서 스토리지 계정을 나열하면 NextPageLink를 통해 나열됩니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1708">List Storage accounts from subscription, will list with NextPageLink</span></span>
    -  <span data-ttu-id="1d1eb-1709">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1709">Get-AzStorageAccount</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="1d1eb-1710">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1710">Az.StorageSync</span></span>
* <span data-ttu-id="1d1eb-1711">Reset-AzStorageSyncServerCertificate의 9810 문제가 해결되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1711">Fix Issue 9810 in Reset-AzStorageSyncServerCertificate.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="1d1eb-1712">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1712">Az.Websites</span></span>
* <span data-ttu-id="1d1eb-1713">앱의 ASP를 업데이트하는 Set-AzWebApp이 실패했습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1713">Set-AzWebApp updating ASP of an app was failing</span></span>

## <a name="270---september-2019"></a><span data-ttu-id="1d1eb-1714">2.7.0 - 2019년 9월</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1714">2.7.0 - September 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="1d1eb-1715">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1715">Az.ApiManagement</span></span>
* <span data-ttu-id="1d1eb-1716">'Set-AzApiManagementPolicy' 참조 설명서에서 '-Format' 매개 변수 설명이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1716">Update '-Format' parameter description in 'Set-AzApiManagementPolicy' reference documentation</span></span>
* <span data-ttu-id="1d1eb-1717">참조 설명서에서 사용되지 않는 cmdlet 'Update-AzApiManagementDeployment'의 참조를 제거했습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1717">Removed references of deprecated cmdlet 'Update-AzApiManagementDeployment' from reference documentation.</span></span> <span data-ttu-id="1d1eb-1718">그 대신 'Set-AzApiManagement'를 사용하세요.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1718">Use 'Set-AzApiManagement' instead.</span></span>

#### <a name="azautomation"></a><span data-ttu-id="1d1eb-1719">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1719">Az.Automation</span></span>
* <span data-ttu-id="1d1eb-1720">'Register-AzAutomationDscNode'에 대한 참조 설명서의 예제 오타가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1720">Fixed example typo in reference documentation for 'Register-AzAutomationDscNode'</span></span>
* <span data-ttu-id="1d1eb-1721">Register-AzAutomationDSCNode에 OS 제한에 대한 설명이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1721">Added clarification on OS restriction to Register-AzAutomationDSCNode</span></span>
* <span data-ttu-id="1d1eb-1722">-Wait 옵션에 대한 Start-AzAutomationRunbook cmdlet Null 참조 예외가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1722">Fixed Start-AzAutomationRunbook cmdlet Null reference exception for -Wait option.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="1d1eb-1723">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1723">Az.Compute</span></span>
* <span data-ttu-id="1d1eb-1724">New-AzDiskConfig에 UploadSizeInBytes 매개 변수가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1724">Add UploadSizeInBytes parameter tp New-AzDiskConfig</span></span>
* <span data-ttu-id="1d1eb-1725">New-AzSnapshotConfig에 증분 매개 변수가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1725">Add Incremental parameter to New-AzSnapshotConfig</span></span>
* <span data-ttu-id="1d1eb-1726">다음과 같은 낮은 우선 순위의 가상 머신 기능이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1726">Add a low priority virtual machine feature:</span></span>
    - <span data-ttu-id="1d1eb-1727">MaxPrice, EvictionPolicy 및 Priority 매개 변수가 New-AzVMConfig에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1727">MaxPrice, EvictionPolicy and Priority parameters are added to New-AzVMConfig.</span></span>
    - <span data-ttu-id="1d1eb-1728">MaxPrice 매개 변수는 New-AzVmssConfig, Update-AzVM 및 Update-AzVmss cmdlet에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1728">MaxPrice parameter is added to New-AzVmssConfig, Update-AzVM and Update-AzVmss cmdlets.</span></span>
* <span data-ttu-id="1d1eb-1729">구독의 모든 가용성 세트를 나열할 때 발생하는 Get-AzAvailabilitySet cmdlet에 대한 VM 참조 이슈가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1729">Fix VM reference issue for Get-AzAvailabilitySet cmdlet when it lists all availability sets in the subscription.</span></span>
* <span data-ttu-id="1d1eb-1730">Get-AzRemoteDesktopFile에 대한 null 예외가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1730">Fix the null exception for Get-AzRemoteDesktopFile.</span></span>
* <span data-ttu-id="1d1eb-1731">종료 상대 위치에 대한 VHD 검색 메서드가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1731">Fix VHD Seek method for end-relative position.</span></span>
* <span data-ttu-id="1d1eb-1732">New-AzVM 및 Update-AzVM에 대한 UltraSSD 이슈가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1732">Fix UltraSSD issue for New-AzVM and Update-AzVM.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="1d1eb-1733">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1733">Az.DataFactory</span></span>
* <span data-ttu-id="1d1eb-1734">ADF V2에 대한 3가지 새 명령 Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription 및 Get-AzDataFactoryV2TriggerSubscriptionStatus가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1734">Adding 3 new commands for ADF V2 - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription, and Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>
* <span data-ttu-id="1d1eb-1735">ADF .Net SDK 버전이 4.1.3으로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1735">Updated ADF .Net SDK version to 4.1.3</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="1d1eb-1736">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1736">Az.HDInsight</span></span>
* <span data-ttu-id="1d1eb-1737">호출 주요 변경 내용</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1737">Call out breaking changes</span></span>

#### <a name="aziothub"></a><span data-ttu-id="1d1eb-1738">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1738">Az.IotHub</span></span>
* <span data-ttu-id="1d1eb-1739">지역 쌍 재해 복구 지역에 IotHub에 대한 장애 조치(failover) 호출 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1739">Add support to invoke failover for an IotHub to the geo-paired disaster recovery region.</span></span>
* <span data-ttu-id="1d1eb-1740">IotHub에 대한 메시지 보강 관리 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1740">Add support to manage message enrichment for an IotHub.</span></span> <span data-ttu-id="1d1eb-1741">새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1741">New cmdlets are:</span></span>
    - <span data-ttu-id="1d1eb-1742">Add-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1742">Add-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="1d1eb-1743">Get-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1743">Get-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="1d1eb-1744">Remove-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1744">Remove-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="1d1eb-1745">Set-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1745">Set-AzIotHubMessageEnrichment</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="1d1eb-1746">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1746">Az.Monitor</span></span>
* <span data-ttu-id="1d1eb-1747">최신 모니터링 SDK, 즉, 0.24.1-preview를 가리킵니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1747">Pointing to the most recent Monitor SDK, i.e. 0.24.1-preview</span></span>
   - <span data-ttu-id="1d1eb-1748">메트릭 cmdlet에 줄 바꿈하지 않는 변경 내용을 추가합니다. 즉, 단위 열거형은 여러 새 값을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1748">Adds non-braking changes to the Metrics cmdlets, i.e. the Unit enumeration supports several new values.</span></span> <span data-ttu-id="1d1eb-1749">이러한 cmdlet은 읽기 전용이므로 cmdlet 입력이 변경되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1749">These are read-only cmdlets, so there would be no change in the input of the cmdlets.</span></span>
   - <span data-ttu-id="1d1eb-1750">이제 **ActionGroups** 요청의 api 버전은 **2019-06-01** 이고, 이전에는 **2018-03-01** 였습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1750">The api-version of the **ActionGroups** requests is now **2019-06-01** , before it was **2018-03-01**.</span></span> <span data-ttu-id="1d1eb-1751">시나리오 테스트가 이 변경 내용에 맞게 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1751">The scenario tests have been updated to accommodate for this change.</span></span>
   - <span data-ttu-id="1d1eb-1752">**EmailReceiver** 및 **WebhookReceiver** 클래스에 대한 생성자가 새 필수 인수, 즉, **useCommonAlertSchema** 라는 부울 값을 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1752">The constructors for the classes **EmailReceiver** and **WebhookReceiver** added one new mandatory argument, i.e. a Boolean value called **useCommonAlertSchema**.</span></span> <span data-ttu-id="1d1eb-1753">현재 이 값은 cmdlet의 주요 변경 사항을 숨기도록 **false** 로 고정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1753">Currently, the value is fixed to **false** to hide this breaking change from the cmdlets.</span></span> <span data-ttu-id="1d1eb-1754">**참고** : 이 변경 사항은 경고 팀에서 유효성을 검사해야 하는 임시 변경 내용입니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1754">**NOTE** : this is a temporary change that must be validated by the Alerts team.</span></span>
   - <span data-ttu-id="1d1eb-1755">이전 SDK에서 변경된 **Source** 클래스( **ScheduledQueryRuleSource** 클래스와 관련됨)의 생성자에 대한 인수 순서입니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1755">The order of the arguments for the constructor of the class **Source** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="1d1eb-1756">이번 변화로 인해 두 개의 단위 테스트를 수정해야 했습니다. 즉, 두 단위 테스트가 컴파일되었지만 테스트를 통과하지 못했습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1756">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
   - <span data-ttu-id="1d1eb-1757">이전 SDK에서 변경된 **AlertingAction** 클래스( **ScheduledQueryRuleSource** 클래스와 관련됨)의 생성자에 대한 인수 순서입니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1757">The order of the arguments for the constructor of the class **AlertingAction** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="1d1eb-1758">이번 변화로 인해 두 개의 단위 테스트를 수정해야 했습니다. 즉, 두 단위 테스트가 컴파일되었지만 테스트를 통과하지 못했습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1758">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
* <span data-ttu-id="1d1eb-1759">메트릭 경고 V2에 대한 동적 임계값 기준 지원</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1759">Support Dynamic Threshold criteria for metric alert V2</span></span>
    - <span data-ttu-id="1d1eb-1760">AzMetricAlertRuleV2Criteria: 이제 동적 임계값 조건도 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1760">New-AzMetricAlertRuleV2Criteria: now creats dynamic threshold criteria also</span></span>
    - <span data-ttu-id="1d1eb-1761">Add-AzMetricAlertRuleV2: 이제 동적 임계값 조건도 수락합니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1761">Add-AzMetricAlertRuleV2: now accept dynamic threshold criteria also</span></span>
* <span data-ttu-id="1d1eb-1762">SQR(예약된 쿼리 규칙)의 향상된 기능</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1762">Improvements in Scheduled Query Rule cmdlets (SQR)</span></span>
 - <span data-ttu-id="1d1eb-1763">Cmdlet이 'Location' 매개 변수를 두 가지 형식(eastus 같은 위치 또는 미국 동부 같은 위치 표시 이름)으로 모두 허용합니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1763">Cmdlets will accept 'Location' paramater in both formats, either the location (e.g. eastus) or the location display name (e.g. East US)</span></span>
 - <span data-ttu-id="1d1eb-1764">도움말 파일에 적절하게 표시된 'Enabled' 매개 변수</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1764">Illustrated 'Enabled' parameter in help files properly</span></span>
 - <span data-ttu-id="1d1eb-1765">선택적 매개 변수 'ActionGroup'에 대한 예제가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1765">Added examples for 'ActionGroup' optional parameter</span></span>
 - <span data-ttu-id="1d1eb-1766">도움말 파일이 전체적으로 개선되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1766">Overall improved help files</span></span>
* <span data-ttu-id="1d1eb-1767">'Set-AzActionRule'의 범위 유형 결정 버그를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1767">Fix bug in determining scope type for 'Set-AzActionRule'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="1d1eb-1768">Az.Network</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1768">Az.Network</span></span>
* <span data-ttu-id="1d1eb-1769">'New-AzApplicationGateway' 참조 설명서의 잘못된 예제가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1769">Fix incorrect example in 'New-AzApplicationGateway' reference documentation</span></span>
* <span data-ttu-id="1d1eb-1770">'Get-AzNetworkWatcherPacketCapture' 참조 설명서에 패킷 캡처를 위한 모든 속성 검색과 관련된 메모가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1770">Add note in 'Get-AzNetworkWatcherPacketCapture' reference documentation about retrieving all properties for a packet capture</span></span>
* <span data-ttu-id="1d1eb-1771">NIC를 올바르게 열거하도록 'Test-AzNetworkWatcherIPFlow' 참조 설명서의 예제가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1771">Fixed example in 'Test-AzNetworkWatcherIPFlow' reference documentation to correctly enumerate NICs</span></span>
* <span data-ttu-id="1d1eb-1772">추가 세부 정보가 있는 경우 추가 세부 정보를 표시하도록 클라우드 예외 구문 분석이 향상되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1772">Improved cloud exception parsing to display additional details if they are present</span></span>
* <span data-ttu-id="1d1eb-1773">더 많은 형식의 SDK 예외를 처리하도록 클라우드 예외 구문 분석이 향상되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1773">Improved cloud exception parsing to handle additional type of SDK exception</span></span>
* <span data-ttu-id="1d1eb-1774">보안 규칙 모델의 잘못된 매핑이 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1774">Fixed incorrect mapping of Security Rule models</span></span>
* <span data-ttu-id="1d1eb-1775">네트워크 인터페이스에 개인 IP 기능을 위한 속성이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1775">Added properties to network interface for private ip feature</span></span>
    - <span data-ttu-id="1d1eb-1776">PSNetworkInterface에 'PrivateEndpoint' 속성이 PSResourceId 형식으로 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1776">Added property 'PrivateEndpoint' as type of PSResourceId to PSNetworkInterface</span></span>
    - <span data-ttu-id="1d1eb-1777">PSNetworkInterfaceIPConfiguration에 'PrivateLinkConnectionProperties' 속성이 PSIpConfigurationConnectivityInformation 형식으로 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1777">Added property 'PrivateLinkConnectionProperties' as type of PSIpConfigurationConnectivityInformation to PSNetworkInterfaceIPConfiguration</span></span>
    - <span data-ttu-id="1d1eb-1778">새 모델 클래스 PSIpConfigurationConnectivityInformation이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1778">Added new model class PSIpConfigurationConnectivityInformation</span></span>
* <span data-ttu-id="1d1eb-1779">Azure Firewall 리소스에 대한 새 ApplicationRuleProtocolType 'mssql'이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1779">Added new ApplicationRuleProtocolType 'mssql' for Azure Firewall resource</span></span>
* <span data-ttu-id="1d1eb-1780">Virtual WAN에서 멀티 링크를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1780">MultiLink support in Virtual WAN</span></span>
    - <span data-ttu-id="1d1eb-1781">새로운 cmdlet</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1781">New cmdlets</span></span>
        - <span data-ttu-id="1d1eb-1782">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1782">New-AzVpnSiteLink</span></span>
        - <span data-ttu-id="1d1eb-1783">New-AzVpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1783">New-AzVpnSiteLinkConnection</span></span>
    - <span data-ttu-id="1d1eb-1784">업데이트된 cmdlet:</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1784">Updated cmdlet:</span></span>
        - <span data-ttu-id="1d1eb-1785">New-VpnSite</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1785">New-VpnSite</span></span>
        - <span data-ttu-id="1d1eb-1786">Update-VpnSite</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1786">Update-VpnSite</span></span>
        - <span data-ttu-id="1d1eb-1787">New-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1787">New-VpnConnection</span></span>
        - <span data-ttu-id="1d1eb-1788">Update-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1788">Update-VpnConnection</span></span>
* <span data-ttu-id="1d1eb-1789">AzureRM cmdlet 대신 Az cmdlet을 사용하도록 일부 PowerShell 예제의 문서가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1789">Fixed documents for some PowerShell examples to use Az cmdlets instead of AzureRM cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="1d1eb-1790">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1790">Az.RecoveryServices</span></span>
* <span data-ttu-id="1d1eb-1791">AzureVMpolicy 개체가 ProtectedItemsCount 특성으로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1791">Update AzureVMpolicy Object with ProtectedItemsCount Attribute</span></span>
* <span data-ttu-id="1d1eb-1792">VM 정책 및 원래 스토리지 계정 복원에 대한 테스트가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1792">Added Tests for VM policy and Original Storage Account Restore</span></span>

#### <a name="azresources"></a><span data-ttu-id="1d1eb-1793">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1793">Az.Resources</span></span>
* <span data-ttu-id="1d1eb-1794">매개 변수 범위 없이 AzRoleAssignment를 호출할 수 없는 버그가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1794">Fix bug where New-AzRoleAssignment could not be called without parameter Scope.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="1d1eb-1795">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1795">Az.ServiceFabric</span></span>
* <span data-ttu-id="1d1eb-1796">'AzServiceFabricReliability' 참조 설명서에 대한 예제의 오타가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1796">Fixed typo in example for 'Update-AzServiceFabricReliability' reference documentation</span></span>
* <span data-ttu-id="1d1eb-1797">애플리케이션 및 서비스를 관리하는 다음과 같은 새 cmdlet이 추가됩니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1797">Adding new cmdlets to manage appliaction and services:</span></span>
    - <span data-ttu-id="1d1eb-1798">New-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1798">New-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="1d1eb-1799">New-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1799">New-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="1d1eb-1800">New-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1800">New-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="1d1eb-1801">New-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1801">New-AzServiceFabricService</span></span>
    - <span data-ttu-id="1d1eb-1802">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1802">Update-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="1d1eb-1803">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1803">Get-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="1d1eb-1804">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1804">Get-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="1d1eb-1805">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1805">Get-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="1d1eb-1806">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1806">Get-AzServiceFabricService</span></span>
    - <span data-ttu-id="1d1eb-1807">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1807">Remove-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="1d1eb-1808">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1808">Remove-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="1d1eb-1809">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1809">Remove-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="1d1eb-1810">Remove-AzServiceFabricServic</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1810">Remove-AzServiceFabricServic</span></span>
* <span data-ttu-id="1d1eb-1811">Service Fabric SDK가 Service Fabric 리소스 공급자 api 버전 2019-03-01을 사용하는 1.2.0 버전으로 업그레이드되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1811">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2019-03-01.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="1d1eb-1812">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1812">Az.SignalR</span></span>
* <span data-ttu-id="1d1eb-1813">Update, Restart, CheckNameAvailability, GetUsage Cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1813">Add Update, Restart, CheckNameAvailability, GetUsage Cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="1d1eb-1814">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1814">Az.Sql</span></span>
* <span data-ttu-id="1d1eb-1815">'Get-AzSqlElasticPool'에 대한 참조 설명서의 예제가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1815">Update example in reference documentation for 'Get-AzSqlElasticPool'</span></span>
* <span data-ttu-id="1d1eb-1816">탄력적 풀을 만드는 vCore 예제가 추가되었습니다(AzSqlElasticPool).</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1816">Added vCore example to creating an elastic pool (New-AzSqlElasticPool).</span></span>
* <span data-ttu-id="1d1eb-1817">Set-AzSqlServerAdvancedThreatProtectionPolicy 및 Set-AzSqlDatabaseAdvancedThreatProtectionPolicy에서 EmailAddresses가 비어 있는 경우 EmailAddresses의 유효성을 검사하고 EmailAdmins가 false가 아닌지 확인하는 기능이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1817">Remove the validation of EmailAddresses and the check that EmailAdmins is not false in case EmailAddresses is empty in Set-AzSqlServerAdvancedThreatProtectionPolicy and Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="1d1eb-1818">감사 범주를 사용하는 여러 진단 설정이 있는 경우 서버/데이터베이스 감사 설정을 제거하도록 설정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1818">Enabled removal of server/database auditing settings when multiple diagnostic settings that enable audit category exist.</span></span>
* <span data-ttu-id="1d1eb-1819">여러 Sql 취약성 평가 cmdlet에서 이메일 주소 유효성 검사가 수정되었습니다(Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting 및 Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1819">Fix email addresses validation in multiple Sql Vulnerability Assessment cmdlets (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting and Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span></span>

#### <a name="azstorage"></a><span data-ttu-id="1d1eb-1820">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1820">Az.Storage</span></span>
* <span data-ttu-id="1d1eb-1821">'Get-AzStorageAccountKey'에 대한 참조 설명서의 예제가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1821">Updated example in reference documentation for 'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="1d1eb-1822">Azure 파일 업로드/다운에서, 원본 파일 SMB 속성(파일 특성, 파일 생성 시간, 파일을 마지막으로 쓴 시간)을 대상 파일에 보존하는 기능이 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1822">In upload/Downalod Azure File,support perserve the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the destination file</span></span>
    -  <span data-ttu-id="1d1eb-1823">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1823">Set-AzStorageFileContent</span></span>
    -  <span data-ttu-id="1d1eb-1824">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1824">Get-AzStorageFileContent</span></span>
* <span data-ttu-id="1d1eb-1825">컨테이너가 사용되는 ImmutabilityPolicy에서 properties/metadate fail을 사용하여 블록 Blob 업로드가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1825">Fix Upload block blob with properties/metadate fail on container enabled ImmutabilityPolicy.</span></span>
    -  <span data-ttu-id="1d1eb-1826">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1826">Set-AzStorageBlobContent</span></span>
* <span data-ttu-id="1d1eb-1827">관리 평면 API를 사용하여 Azure 파일 공유 관리를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1827">Support manage Azure File shares with Management plane API</span></span>
    -  <span data-ttu-id="1d1eb-1828">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1828">New-AzRmStorageShare</span></span>
    -  <span data-ttu-id="1d1eb-1829">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1829">Get-AzRmStorageShare</span></span>
    -  <span data-ttu-id="1d1eb-1830">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1830">Update-AzRmStorageShare</span></span>
    -  <span data-ttu-id="1d1eb-1831">Remove-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1831">Remove-AzRmStorageShare</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="1d1eb-1832">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1832">Az.Websites</span></span>
* <span data-ttu-id="1d1eb-1833">앱을 새 ASP로 마이그레이션할 때 웹앱 태그가 삭제되는 이슈가 해결되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1833">Fixing issue where webapp Tags were getting deleted when migrating App to new ASPwhere webapp Tags were getting deleted when migrating App to new ASP</span></span>
* <span data-ttu-id="1d1eb-1834">Linux와 Windows에서 모두 작동하도록 Publish-AzureWebapp이 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1834">Fixing the Publish-AzureWebapp to work across Linux and windows</span></span>
* <span data-ttu-id="1d1eb-1835">'Get-AzWebAppPublishingProfile' 참조 설명서의 예제가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1835">Update example in 'Get-AzWebAppPublishingProfile' reference documentation</span></span>

## <a name="260---august-2019"></a><span data-ttu-id="1d1eb-1836">2.6.0 - 2019년 8월</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1836">2.6.0 - August 2019</span></span>
#### <a name="general"></a><span data-ttu-id="1d1eb-1837">일반</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1837">General</span></span>
* <span data-ttu-id="1d1eb-1838">여러 모듈에서 기타 오타가 수정됨</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1838">Fixed miscellaneous typos across numerous modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="1d1eb-1839">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1839">Az.Accounts</span></span>
* <span data-ttu-id="1d1eb-1840">Azure Functions 인증에서 사용자가 할당한 MSI가 지원됨(# 9479)</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1840">Support user-assigned MSI in Azure Functiosn Authentication (#9479)</span></span>

#### <a name="azaks"></a><span data-ttu-id="1d1eb-1841">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1841">Az.Aks</span></span>
* <span data-ttu-id="1d1eb-1842">'Get-AzAks' 출력 관련 문제가 해결됨</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1842">Fix issue with output for 'Get-AzAks'</span></span>
    * <span data-ttu-id="1d1eb-1843">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/9847 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1843">More information here: https://github.com/Azure/azure-powershell/issues/9847</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="1d1eb-1844">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1844">Az.ApiManagement</span></span>
* <span data-ttu-id="1d1eb-1845">문제 https://github.com/Azure/azure-powershell/issues/9351 수정</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1845">Fix for issue https://github.com/Azure/azure-powershell/issues/9351</span></span>
    - <span data-ttu-id="1d1eb-1846">productId, apiId, groupId 및 userId에 대한 제한을 적용하지 않는 .Net NuGet 버전이 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1846">Update .net nuget version, which does not enforce restrictions on productId, apiId, groupId and userId</span></span>
* <span data-ttu-id="1d1eb-1847">**Get-AzApiManagementProduct** - API를 사용하는 제품에 대한 쿼리 지원이 추가됨</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1847">**Get-AzApiManagementProduct** - Added support for querying products using Api.</span></span>
  https://github.com/Azure/azure-powershell/issues/9482
* <span data-ttu-id="1d1eb-1848">**New-AzApiManagementApiRevision** - 새 API 수정(https://github.com/Azure/azure-powershell/issues/9752 )을 만들 때 ApiRevisionDescription이 설정되지 않은 문제가 해결됨</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1848">**New-AzApiManagementApiRevision** - Fix for issue where ApiRevisionDescription was not being set when creating new api revision https://github.com/Azure/azure-powershell/issues/9752</span></span>
* <span data-ttu-id="1d1eb-1849">'PsApiManagementOAuth2AuthrozationServer' 모델의 오타가 'PsApiManagementOAuth2AuthorizationServer'로 수정됨</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1849">Fixed typo in model 'PsApiManagementOAuth2AuthrozationServer' to 'PsApiManagementOAuth2AuthorizationServer'</span></span>

#### <a name="azbatch"></a><span data-ttu-id="1d1eb-1850">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1850">Az.Batch</span></span>
* <span data-ttu-id="1d1eb-1851">도움말 메시지 및 설명서에서 Windows를 대문자로 시작하도록 오타가 수정됨</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1851">Fixed typo in help message and documentation to capitalize Windows</span></span>

#### <a name="azcdn"></a><span data-ttu-id="1d1eb-1852">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1852">Az.Cdn</span></span>
* <span data-ttu-id="1d1eb-1853">CDN 모듈 변환 도우미의 오타가 수정됨</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1853">Fixed a typo in CDN module conversion helper</span></span>

#### <a name="azcompute"></a><span data-ttu-id="1d1eb-1854">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1854">Az.Compute</span></span>
* <span data-ttu-id="1d1eb-1855">VmssId가 New-AzVMConfig cmdlet에 추가됨</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1855">Add VmssId to New-AzVMConfig cmdlet</span></span>
* <span data-ttu-id="1d1eb-1856">TerminateScheduledEvents 및 TerminateScheduledEventNotBeforeTimeoutInMinutes 매개 변수가 New-AzVmssConfig 및 Update-AzVmss에 추가됨</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1856">Add TerminateScheduledEvents and TerminateScheduledEventNotBeforeTimeoutInMinutes parameters to New-AzVmssConfig and Update-AzVmss</span></span>
* <span data-ttu-id="1d1eb-1857">HyperVGeneration 속성이 VM 이미지 개체에 추가됨</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1857">Add HyperVGeneration property to VM image object</span></span>
* <span data-ttu-id="1d1eb-1858">Host 및 HostGroup 기능이 추가됨</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1858">Add Host and HostGroup features</span></span>
    - <span data-ttu-id="1d1eb-1859">새 cmdlet:   New-AzHostGroup, New-AzHost, Get-AzHostGroup, Get-AzHost, Remove-AzHostGroup, Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1859">New cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span></span>
    - <span data-ttu-id="1d1eb-1860">HostId 매개 변수가 New-AzVMConfig 및 New-AzVM 추가됨</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1860">HostId parameter is added to New-AzVMConfig and New-AzVM</span></span>
* <span data-ttu-id="1d1eb-1861">'Invoke-AzVMRunCommand' 설명서의 예제에서 올바른 매개 변수 이름을 사용하도록 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1861">Update example in 'Invoke-AzVMRunCommand' documentation to use correct parameter name</span></span>
* <span data-ttu-id="1d1eb-1862">'Set-AzVMDiskEncryptionExtension' 및 'Set-AzVmssDiskEncryptionExtension' 참조 설명서의 '-VolumeType' 설명이 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1862">Update '-VolumeType' description in 'Set-AzVMDiskEncryptionExtension' and 'Set-AzVmssDiskEncryptionExtension' reference documentation</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="1d1eb-1863">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1863">Az.DataFactory</span></span>
* <span data-ttu-id="1d1eb-1864">'New-AzDataFactoryEncryptValue' 설명서에서 'Windows'를 대문자로 시작하도록 오타가 수정됨</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1864">Fix typo to capitalize 'Windows' in 'New-AzDataFactoryEncryptValue' documentation</span></span>
* <span data-ttu-id="1d1eb-1865">ADF .Net SDK 버전이 4.1.2로 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1865">Updated ADF .Net SDK version to 4.1.2</span></span>
* <span data-ttu-id="1d1eb-1866">자체 호스팅 통합 런타임을 SSIS Integration Runtime의 프록시로 설정할 수 있도록 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' 및 'DataProxyStagingPath' 매개 변수가 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd에 추가됨</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1866">Add parameter 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' and 'DataProxyStagingPath' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable set up Self-Hosted Integration Runtime as a proxy for SSIS Integration Runtime</span></span>
* <span data-ttu-id="1d1eb-1867">PSTriggerRun에서 트리거된 파이프라인, 메시지 및 속성을 표시하고, PSActivityRun에서 작업 유형을 표시하도록 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1867">Updated PSTriggerRun to show the triggered pipelines, message and properties, and PSActivityRun to show the activity type</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="1d1eb-1868">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1868">Az.DataLakeStore</span></span>
* <span data-ttu-id="1d1eb-1869">오류 또는 원격 예외에 대한 Get-DataLakeStoreDeletedItem 중단이 수정됨</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1869">Fix hanging of Get-DataLakeStoreDeletedItem for any errors or remote exceptions.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="1d1eb-1870">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1870">Az.EventHub</span></span>
* <span data-ttu-id="1d1eb-1871">#9658 문제 해결: Set-AzEventHubNetworkRuleSet의 VirtualNteworkRule 매개 변수에 대한 오타</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1871">Fix for issue #9658 : Typo VirtualNteworkRule parameter in Set-AzEventHubNetworkRuleSet</span></span>
* <span data-ttu-id="1d1eb-1872">#9558 문제 해결: Set-AzEventHubNamespace에서 PUT 대신 PATCH가 사용됨</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1872">Fix for issue #9558 : Set-AzEventHubNamespace is using PATCH instead of PUT</span></span>
* <span data-ttu-id="1d1eb-1873">EnableKafka 매개 변수가 Set-AzEventHubNamespace cmdlet에 추가됨</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1873">added EnableKafka parameter to Set-AzEventHubNamespace cmdlet</span></span>
* <span data-ttu-id="1d1eb-1874">#9786 문제 해결: Listen(수신 대기) 전용 권한이 있는 규칙을 만들 수 없음</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1874">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>

#### <a name="azmarketplaceordering"></a><span data-ttu-id="1d1eb-1875">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1875">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="1d1eb-1876">'Azure'가 모두 소문자인 설명서의 오타가 수정됨</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1876">Fixed documentation typo where 'Azure' was all lowercase letters</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="1d1eb-1877">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1877">Az.Monitor</span></span>
* <span data-ttu-id="1d1eb-1878">도움말 설명서에서 잘못된 매개 변수 이름이 수정됨</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1878">Fixed incorrect parameter name in help documentation</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="1d1eb-1879">Az.Network</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1879">Az.Network</span></span>
* <span data-ttu-id="1d1eb-1880">New-AzPrivateLinkServiceIpConfig가 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1880">Updated New-AzPrivateLinkServiceIpConfig</span></span>
    - <span data-ttu-id="1d1eb-1881">서버 쪽에서 사용되지 않으므로 'PublicIpAddress' 매개 변수가 사용되지 않음</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1881">Deprecated the paramster 'PublicIpAddress' since this is never used in the server side.</span></span>
    - <span data-ttu-id="1d1eb-1882">현재 IP 구성이 기본 구성인지 여부를 나타내는 하나의 선택적 'Primary' 매개 변수가 추가됨</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1882">Added one optional parameter 'Primary' that indicate the current ip configuration is primary one or not.</span></span>
* <span data-ttu-id="1d1eb-1883">SDK의 요청 오류 예외 처리가 향상됨 - 이전의 SDK 예외가 올바르게 처리되지 않아 주요 오류 세부 정보가 표시되지 않은 문제가 해결됨</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1883">Improved handling of request error exception from SDK   -Fixes the issue that previously SDK exceptions aren't handled correctly which results in key error details not being displayed</span></span>
* <span data-ttu-id="1d1eb-1884">올바른 IPv6 접두사 길이를 확인하기 위해 Ipv6 IP 접두사에 대한 유효성 검사 논리가 조정됨</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1884">Adjusted validation logic for Ipv6 IP Prefix to check for correct IPv6 prefix length.</span></span>
* <span data-ttu-id="1d1eb-1885">Get-AzVirtualNetworkSubnetConfig가 업데이트됨: 서브넷 리소스 ID별로 가져오도록 설정되는 매개 변수 세트가 추가됨</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1885">Updated Get-AzVirtualNetworkSubnetConfig: Added parameter set to get by subnet resource id.</span></span>
* <span data-ttu-id="1d1eb-1886">AzNetworkServiceTag의 Location(위치) 매개 변수에 대한 설명이 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1886">Updated description of Location parameter for AzNetworkServiceTag</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="1d1eb-1887">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1887">Az.OperationalInsights</span></span>
* <span data-ttu-id="1d1eb-1888">'New-AzOperationalInsightsLinuxSyslogDataSource'에 대한 설명서가 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1888">Updated documentation for 'New-AzOperationalInsightsLinuxSyslogDataSource'</span></span>
    - <span data-ttu-id="1d1eb-1889">예제가 추가됨</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1889">Added example</span></span>
    - <span data-ttu-id="1d1eb-1890">'-Name' 매개 변수에 대한 설명이 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1890">Updated description for '-Name' parameter</span></span>
* <span data-ttu-id="1d1eb-1891">New-AzOperationalInsightsWindowsEventDataSource에 대한 예제가 추가됨</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1891">Added an example for New-AzOperationalInsightsWindowsEventDataSource</span></span>
* <span data-ttu-id="1d1eb-1892">New-AzOperationalInsightsWindowsEventDataSource의 -Name 매개 변수에 대한 설명이 변경됨</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1892">Changed the description of the -Name parameter for New-AzOperationalInsightsWindowsEventDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="1d1eb-1893">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1893">Az.RecoveryServices</span></span>
* <span data-ttu-id="1d1eb-1894">'Get-AzRecoveryServicesBackupJobDetail.md'가 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1894">Update 'Get-AzRecoveryServicesBackupJobDetail.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="1d1eb-1895">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1895">Az.Resources</span></span>
* <span data-ttu-id="1d1eb-1896">Microsoft 리소스에 대한 새 2019-05-10 API 버전 지원이 추가됨</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1896">Add support for new api version 2019-05-10 for Microsoft.Resource</span></span>
    - <span data-ttu-id="1d1eb-1897">변수, 리소스 및 속성에 대한 'copy.count = 0' 지원이 추가됨</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1897">Add support for 'copy.count = 0' for variables, resources and properties</span></span>
    - <span data-ttu-id="1d1eb-1898">'condition = false' 또는 'copy.count = 0'인 리소스가 완료 모드에서 삭제됨</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1898">Resources with 'condition = false' or 'copy.count = 0' will be deleted in complete mode</span></span>
* <span data-ttu-id="1d1eb-1899">정책을 구독 수준에서 도움말 문서에 할당하는 예제가 추가됨</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1899">Add an example of assigning policy at subscription level to help doc</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="1d1eb-1900">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1900">Az.ServiceBus</span></span>
* <span data-ttu-id="1d1eb-1901">#9658 문제 해결: Set-AzServiceBusNetworkRuleSet의 VirtualNetworkRule 매개 변수에 대한 오타</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1901">Fix for issue #9658 : Typo VirtualNetworkRule parameter in Set-AzServiceBusNetworkRuleSet</span></span>
* <span data-ttu-id="1d1eb-1902">#9786 문제 해결: Listen(수신 대기) 전용 권한이 있는 규칙을 만들 수 없음</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1902">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>
* <span data-ttu-id="1d1eb-1903">큐 및 토픽에 대한 이름 가용성을 확인하는 새 'Test-AzServiceBusNameAvailability' 명령이 추가됨</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1903">Added new command 'Test-AzServiceBusNameAvailability' to check the name availability for queue and topic</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="1d1eb-1904">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1904">Az.ServiceFabric</span></span>
* <span data-ttu-id="1d1eb-1905">노드 유형 추가 cmdlet 버그 수정:</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1905">Fix add node type cmdlet bugs:</span></span>
    - <span data-ttu-id="1d1eb-1906">서비스 패브릭 클러스터와 관련이 없는 다른 vmss가 리소스 그룹에 있을 때 발생하는 NullReferenceException 버그</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1906">NullReferenceException bug when resource group had other vmss not related to the service fabric cluster.</span></span> <span data-ttu-id="1d1eb-1907">문제 해결: https://github.com/Azure/azure-powershell/issues/8681</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1907">Fixes issue: https://github.com/Azure/azure-powershell/issues/8681</span></span>
    - <span data-ttu-id="1d1eb-1908">virtualNetwork가 클러스터의 다른 리소스 그룹에 있을 때 cmdlet이 실패하는 버그가 수정됨</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1908">Fix bug where cmdlet failed if virtualNetwork was in a different resource group that the cluster.</span></span> <span data-ttu-id="1d1eb-1909">문제 해결: https://github.com/Azure/azure-powershell/issues/8407</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1909">fixes issue: https://github.com/Azure/azure-powershell/issues/8407</span></span>
    - <span data-ttu-id="1d1eb-1910">Add-AzServiceFabricApplicationCertificate cmdlet이 사용되지 않음</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1910">Deprecating Add-AzServiceFabricApplicationCertificate cmdlet</span></span>

#### <a name="azsql"></a><span data-ttu-id="1d1eb-1911">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1911">Az.Sql</span></span>
* <span data-ttu-id="1d1eb-1912">이전의 Auditing(감사) cmdlet에 대한 설명서가 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1912">Update documentation of old Auditing cmdlets.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="1d1eb-1913">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1913">Az.Storage</span></span>
* <span data-ttu-id="1d1eb-1914">더 많은 시나리오를 cmdlet 예제에 추가하고 매개 변수 설명을 업데이트하여 Get/Close-AzStorageFileHandle에 대한 도움말이 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1914">Update help for Get/Close-AzStorageFileHandle, by add more scenarios to cmdlet examples and update parameter descriptions</span></span>
* <span data-ttu-id="1d1eb-1915">Blob 업로드 및 Blob 복사에서 StandardBlobTier가 지원됨</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1915">Support StandardBlobTier in upload blob and copy blob</span></span>
    -  <span data-ttu-id="1d1eb-1916">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1916">Set-AzStorageBlobContent</span></span>
    -  <span data-ttu-id="1d1eb-1917">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1917">Start-AzStorageBlobCopy</span></span>
* <span data-ttu-id="1d1eb-1918">Blob 복사에서 우선 순위 리하이드레이션이 지원됨</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1918">Support Rehydrate Priority in copy blob</span></span>
    -  <span data-ttu-id="1d1eb-1919">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1919">Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="1d1eb-1920">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1920">Az.Websites</span></span>
* <span data-ttu-id="1d1eb-1921">Set-AzWebApp 및 Set-AzWebAppSlot에서 -AppSettings 매개 변수에 대한 설명이 추가됨</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1921">Add clarification around -AppSettings parameter in Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <a name="250---july-2019"></a><span data-ttu-id="1d1eb-1922">2.5.0 - 2019년 7월</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1922">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="1d1eb-1923">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1923">Az.Accounts</span></span>
* <span data-ttu-id="1d1eb-1924">ClientRuntime의 최신 버전을 사용하도록 일반적인 코드를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1924">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="1d1eb-1925">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1925">Az.ApplicationInsights</span></span>
* <span data-ttu-id="1d1eb-1926">'Remove-AzApplicationInsightsApiKey' 설명서의 예제 오타 수정</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1926">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span>

#### <a name="azautomation"></a><span data-ttu-id="1d1eb-1927">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1927">Az.Automation</span></span>
* <span data-ttu-id="1d1eb-1928">리소스 문자열의 오타 수정</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1928">Fix typo in resource string</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="1d1eb-1929">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1929">Az.CognitiveServices</span></span>
* <span data-ttu-id="1d1eb-1930">NetworkRuleSet 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1930">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="1d1eb-1931">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1931">Az.Compute</span></span>
* <span data-ttu-id="1d1eb-1932">VM 인스턴스 보기 개체의 누락된 속성(ComputerName, OsName, OsVersion 및 HyperVGeneration)을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1932">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="1d1eb-1933">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1933">Az.ContainerRegistry</span></span>
* <span data-ttu-id="1d1eb-1934">복제 매개 변수의 Remove-AzContainerRegistryReplication에서 오타 수정</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1934">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="1d1eb-1935">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/9633 을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1935">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="1d1eb-1936">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1936">Az.DataFactory</span></span>
* <span data-ttu-id="1d1eb-1937">ADF .Net SDK 버전을 4.1.0으로 업데이트</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1937">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="1d1eb-1938">'Get-AzDataFactoryV2PipelineRun' 설명서의 오타 수정</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1938">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="1d1eb-1939">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1939">Az.EventHub</span></span>
* <span data-ttu-id="1d1eb-1940">SAS 토큰을 생성하기 위해 추가된 새로운 cmmdlet 추가: New-AzEventHubAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1940">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="1d1eb-1941">'관리'만 지정된 경우 authorizationrules 권한에 대한 확인 및 오류 메시지 추가</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1941">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="1d1eb-1942">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1942">Az.KeyVault</span></span>
* <span data-ttu-id="1d1eb-1943">인증서 정책에 대한 KeySize 지정을 위한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1943">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="1d1eb-1944">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1944">Az.LogicApp</span></span>
* <span data-ttu-id="1d1eb-1945">모든 맵 유형을 나열하도록 Get-AzIntegrationAccountMap 수정</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1945">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="1d1eb-1946">필터링을 위해 새 MapType 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1946">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="1d1eb-1947">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1947">Az.ManagedServices</span></span>
* <span data-ttu-id="1d1eb-1948">API 버전 2019-06-01(GA)에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1948">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="1d1eb-1949">Az.Network</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1949">Az.Network</span></span>
* <span data-ttu-id="1d1eb-1950">프라이빗 엔드포인트 및 프라이빗 링크 서비스에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1950">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="1d1eb-1951">새로운 cmdlet</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1951">New cmdlets</span></span>
        - <span data-ttu-id="1d1eb-1952">Set-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1952">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="1d1eb-1953">Set-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1953">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="1d1eb-1954">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1954">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="1d1eb-1955">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1955">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="1d1eb-1956">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1956">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="1d1eb-1957">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1957">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="1d1eb-1958">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1958">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="1d1eb-1959">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1959">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="1d1eb-1960">기능에 대한 새로운 명령이 업데이트됨: Virtualnetwork의 서브넷에 있는 PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies 플래그</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1960">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="1d1eb-1961">업데이트된 New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1961">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="1d1eb-1962">이 서브넷의 프라이빗 엔드포인트에 네트워크 정책을 적용할지 여부를 나타내는 선택적 매개 변수 -PrivateEndpointNetworkPoliciesFlag가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1962">Added optional parameter -PrivateEndpointNetworkPoliciesFlag that configures whether to apply network policies on private endpoint in this subnet.</span></span>
        - <span data-ttu-id="1d1eb-1963">이 서브넷의 프라이빗 연결 서비스에 네트워크 정책을 적용할지 여부를 나타내는 선택적 매개 변수 -PrivateLinkServiceNetworkPoliciesFlag가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1963">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag that configures whether to apply network policies network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="1d1eb-1964">AzPrivateLinkService의 cmdlet 매개 변수 'ServiceName'이 이전 버전과의 호환성을 위해 별칭 'ServiceName'을 사용한 'Name'으로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1964">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="1d1eb-1965">네트워크 보안 규칙 구성에 ICMP 프로토콜 사용</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1965">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="1d1eb-1966">다음 Cmdlet이 업데이트 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1966">Updated cmdlets</span></span>
        - <span data-ttu-id="1d1eb-1967">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1967">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="1d1eb-1968">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1968">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="1d1eb-1969">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1969">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="1d1eb-1970">New-AzVirtualNetworkGatewayConnection에 대한 구성 가능한 매개 변수로 ConnectionProtocolType (Ikev1/Ikev2) 추가</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1970">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="1d1eb-1971">LoadBalancerFrontendIpConfiguration에 PrivateIpAddressVersion 추가</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1971">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="1d1eb-1972">업데이트된 cmdlet:</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1972">Updated cmdlet:</span></span>
        - <span data-ttu-id="1d1eb-1973">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1973">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="1d1eb-1974">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1974">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="1d1eb-1975">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1975">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="1d1eb-1976">프로브에서 사용자 지정 포트를 지원하기 위한 Application Gateway New-AzApplicationGatewayProbeConfig 명령 업데이트</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1976">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="1d1eb-1977">업데이트된 New-AzApplicationGatewayProbeConfig: 백 엔드 서버 검색에 사용되는 선택적 매개 변수 포트가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1977">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="1d1eb-1978">이 매개 변수는 Standard_V2 및 WAF_V2 SKU에 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1978">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="1d1eb-1979">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1979">Az.OperationalInsights</span></span>
* <span data-ttu-id="1d1eb-1980">저장된 검색의 기본 버전이 1로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1980">Updated default version for saved searches to be 1.</span></span>
* <span data-ttu-id="1d1eb-1981">사용자 지정 로그 null regex 처리가 수정됨</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1981">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="1d1eb-1982">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1982">Az.RecoveryServices</span></span>
* <span data-ttu-id="1d1eb-1983">'Get-AzRecoveryServicesBackupJob.md' 업데이트</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1983">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="1d1eb-1984">'Get-AzRecoveryServicesBackupContainer.md' 업데이트</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1984">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="1d1eb-1985">'Get-AzRecoveryServicesVault.md' 업데이트</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1985">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="1d1eb-1986">'Wait-AzRecoveryServicesBackupJob.md' 업데이트</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1986">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="1d1eb-1987">'Set-AzRecoveryServicesVaultContext.md' 업데이트</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1987">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="1d1eb-1988">'Get-AzRecoveryServicesBackupItem.md' 업데이트</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1988">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="1d1eb-1989">'Get-AzRecoveryServicesBackupRecoveryPoint.md' 업데이트</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1989">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="1d1eb-1990">'Restore-AzRecoveryServicesBackupItem.md' 업데이트</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1990">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="1d1eb-1991">Azure 파일 공유용 컨테이너를 등록 취소하기 위해 서비스 요청 업데이트</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1991">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="1d1eb-1992">'Set-AzRecoveryServicesAsrAlertSetting.md' 업데이트</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1992">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="1d1eb-1993">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1993">Az.Resources</span></span>
- <span data-ttu-id="1d1eb-1994">'New-AzResourceGroupDeployment' 설명서에서 참조된 누락 cmdlet 제거</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1994">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="1d1eb-1995">새 API 버전 2019-01-01을 사용하도록 정책 cmdlet 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1995">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="1d1eb-1996">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1996">Az.ServiceBus</span></span>
* <span data-ttu-id="1d1eb-1997">SAS 토큰을 생성하기 위해 추가된 새로운 cmmdlet 추가: New-AzServiceBusAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1997">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="1d1eb-1998">'관리'만 지정된 경우 authorizationrules 권한에 대한 확인 및 오류 메시지 추가</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1998">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="1d1eb-1999">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="1d1eb-1999">Az.Sql</span></span>
* <span data-ttu-id="1d1eb-2000">Set-AzSqlDatabaseSecondary cmdlet에 대한 누락된 예제 수정</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2000">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="1d1eb-2001">이메일 주소를 제공하지 않고 설정된 취약성 평가 반복 검색 수정</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2001">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="1d1eb-2002">경고 메시지의 작은 오타를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2002">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="1d1eb-2003">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2003">Az.Storage</span></span>
* <span data-ttu-id="1d1eb-2004">'Get-AzStorageAccount'에 대한 참조 설명서의 예제를 업데이트하여 올바른 매개 변수 이름 사용</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2004">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="1d1eb-2005">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2005">Az.StorageSync</span></span>
* <span data-ttu-id="1d1eb-2006">Invoke-AzStorageSyncChangeDetection cmdlet을 추가하는 중입니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2006">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="1d1eb-2007">TierFilesOlderThanDays를 기념하는 문제 9551 수정</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2007">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="1d1eb-2008">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2008">Az.Websites</span></span>
* <span data-ttu-id="1d1eb-2009">Get-AzWebApp 및 Set-AzWebApp에서 일부 SiteConfig 속성을 반환하지 않은 버그 수정</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2009">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="1d1eb-2010">Get-AzDeletedWebApp 및 Restore-AzDeletedWebApp에 새 위치 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2010">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="1d1eb-2011">AzWebApp-IncludeSourceWebAppSlots을 사용하여 웹앱 슬롯을 복제하는 버그를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2011">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="1d1eb-2012">2.4.0 - 2019년 7월</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2012">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="1d1eb-2013">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2013">Az.Accounts</span></span>
* <span data-ttu-id="1d1eb-2014">프로필 cmdlet에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2014">Add support for profile cmdlets</span></span>
* <span data-ttu-id="1d1eb-2015">생성된 cmdlet에서 환경 및 데이터 평면에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2015">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="1d1eb-2016">Windows PowerShell의 데이터 평면 cmdlet에대해 일부 경우 잘못된 엔드포인트가 사용되는 버그 수정</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2016">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="1d1eb-2017">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2017">Az.Advisor</span></span>
* <span data-ttu-id="1d1eb-2018">Az.Advisor의 GA 릴리스</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2018">GA release of Az.Advisor</span></span>
* <span data-ttu-id="1d1eb-2019">이 모듈은 이제 롤업 `Az` 모듈의 일부로 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2019">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="1d1eb-2020">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2020">Az.ApiManagement</span></span>
* <span data-ttu-id="1d1eb-2021">문제 https://github.com/Azure/azure-powershell/issues/8671 수정</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2021">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="1d1eb-2022">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2022">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="1d1eb-2023">사용자 및 제품별 구독을 쿼리하기 위한 지원이 추가됨</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2023">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="1d1eb-2024">범위 '/', '/ api, '/ api/echo api'를 사용하여 쿼리하기 위한 지원이 추가됨</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2024">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="1d1eb-2025">[https://github.com/Azure/azure-powershell/issues/9307](https://github.com/Azure/azure-powershell/issues/9307 ) 및 https://github.com/Azure/azure-powershell/issues/8432 문제 수정</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2025">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="1d1eb-2026">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2026">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="1d1eb-2027">Apis를 가져올 때 'ApiVersion' 및 'ApiVersionSetId'를 지정하기 위한 지원이 추가됨</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2027">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="1d1eb-2028">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2028">Az.Automation</span></span>
* <span data-ttu-id="1d1eb-2029">문자열 값을 처리하기 위해 Set-AzAutomationConnectionFieldValue cmdlet 버그를 수정했습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2029">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="1d1eb-2030">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2030">Az.Compute</span></span>
* <span data-ttu-id="1d1eb-2031">New-AzImageConfig에 HyperVGeneration 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2031">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="1d1eb-2032">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2032">Az.DataFactory</span></span>
* <span data-ttu-id="1d1eb-2033">get activity runs, get pipeline runs, get trigger runs ADF cmdlet의 출력을 업데이트하여 Select-Object pipe를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2033">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="1d1eb-2034">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2034">Az.EventGrid</span></span>
* <span data-ttu-id="1d1eb-2035">'New-AzEventGridSubcription' 설명서의 오타 수정</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2035">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="1d1eb-2036">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2036">Az.IotHub</span></span>
* <span data-ttu-id="1d1eb-2037">권한 부여 정책 키를 다시 생성하기 위한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2037">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="1d1eb-2038">Az.Network</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2038">Az.Network</span></span>
* <span data-ttu-id="1d1eb-2039">'RoutingPreference'를 공용 IP 태그에 추가함</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2039">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="1d1eb-2040">'Get-AzNetworkServiceTag' 참조 설명서의 예제 개선</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2040">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="1d1eb-2041">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2041">Az.PolicyInsights</span></span>
* <span data-ttu-id="1d1eb-2042">Get-AzPolicyState의 null 참조 문제 해결</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2042">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="1d1eb-2043">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/9446 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2043">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="1d1eb-2044">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2044">Az.OperationalInsights</span></span>
* <span data-ttu-id="1d1eb-2045">Get-AzOperationalInsightsDataSource에 반환된 CustomLog datasource 모델 수정됨</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2045">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="1d1eb-2046">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2046">Az.RecoveryServices</span></span>
* <span data-ttu-id="1d1eb-2047">IaaSVMs에 대한 get-policy 명령 수정</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2047">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="1d1eb-2048">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2048">Az.Resources</span></span>
    - <span data-ttu-id="1d1eb-2049">Get-AzPolicyState -Top 매개 변수에 대한 도움말 텍스트 수정</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2049">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="1d1eb-2050">Get-AzPolicyAlias에 대한 클라이언트 쪽 페이징 지원 추가</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2050">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="1d1eb-2051">Set-AzPolicyAssignment, -PolicyParameters 및 -PolicyParametersObject에 대한 새 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2051">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="1d1eb-2052">Policy cmdlet에 대한 몇 가지 문서 및 예제 업데이트</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2052">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="1d1eb-2053">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2053">Az.ServiceBus</span></span>
* <span data-ttu-id="1d1eb-2054">문제 #4938 수정 - MaxSizeInMegabytes를 설정할 때 New-AzureRmServiceBusQueue가 BadRequest 반환</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2054">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="1d1eb-2055">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2055">Az.Sql</span></span>
* <span data-ttu-id="1d1eb-2056">미리 보기 릴리스에서 공개 릴리스로 인스턴스 장애 조치(Failover) 그룹 cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2056">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="1d1eb-2057">새 cmdlet으로 Azure SQL Server\Database Auditing을 지원하세요.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2057">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="1d1eb-2058">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2058">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="1d1eb-2059">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2059">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="1d1eb-2060">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2060">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="1d1eb-2061">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2061">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="1d1eb-2062">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2062">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="1d1eb-2063">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2063">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="1d1eb-2064">취약성 평가 설정에서 이메일 제약 조건 제거</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2064">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="1d1eb-2065">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2065">Az.Storage</span></span>
* <span data-ttu-id="1d1eb-2066">다음 cmdlet에서 2개의 매개 변수 '-IndexDocument' 및 '-ErrorDocument404Path'를 필수에서 선택으로 변경하세요.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2066">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="1d1eb-2067">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2067">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="1d1eb-2068">예제를 추가하여 Get-AzStorageBlobContent의 도움말 업데이트</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2068">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="1d1eb-2069">StorageException으로 cmdlet이 실패한 경우 자세한 오류 정보 표시</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2069">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="1d1eb-2070">Azure Files AAD DS 인증으로 스토리지 계정 생성 또는 업데이트 지원</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2070">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="1d1eb-2071">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2071">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="1d1eb-2072">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2072">Set-AzStorageAccount</span></span>
* <span data-ttu-id="1d1eb-2073">파일 공유, 파일 디렉터리 또는 파일의 목록 지원 또는 파일 핸들 닫기</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2073">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="1d1eb-2074">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2074">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="1d1eb-2075">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2075">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="1d1eb-2076">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2076">Az.StorageSync</span></span>
* <span data-ttu-id="1d1eb-2077">이 모듈은 이제 롤업 `Az` 모듈의 일부로 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2077">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="1d1eb-2078">2.3.2 - 2019년 6월</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2078">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="1d1eb-2079">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2079">Az.Accounts</span></span>
* <span data-ttu-id="1d1eb-2080">함수 호출에 대해 일부 경우 잘못된 URL이 사용되는 버그 수정</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2080">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="1d1eb-2081">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/8983 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2081">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="1d1eb-2082">AzureRM에서 Az cmdlet으로의 별칭 문제 해결</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2082">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="1d1eb-2083">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2083">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="1d1eb-2084">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2084">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="1d1eb-2085">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2085">Az.Compute</span></span>
* <span data-ttu-id="1d1eb-2086">New-AzVm 및 New-AzVmss 단순 매개 변수 집합은 이제 'ProximityPlacementGroup'매개 변수를 허용합니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2086">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="1d1eb-2087">'New-AzVM' 참조 설명서에서 오타 수정</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2087">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="1d1eb-2088">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2088">Az.Dns</span></span>
* <span data-ttu-id="1d1eb-2089">'Set-AzDnsZone' 도움말 예제의 오타가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2089">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="1d1eb-2090">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2090">Az.EventGrid</span></span>
* <span data-ttu-id="1d1eb-2091">2019-06-01 API 버전을 사용하도록 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2091">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="1d1eb-2092">새 cmdlet:</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2092">New cmdlets:</span></span>
    - <span data-ttu-id="1d1eb-2093">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2093">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="1d1eb-2094">새 Azure Event Grid 도메인을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2094">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="1d1eb-2095">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2095">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="1d1eb-2096">Event Grid 도메인의 세부 정보를 가져오거나 현재 Azure 구독의 모든 Event Grid 도메인 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2096">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="1d1eb-2097">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2097">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="1d1eb-2098">Azure Event Grid 도메인을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2098">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="1d1eb-2099">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2099">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="1d1eb-2100">Azure Event Grid 도메인에 대한 공유 액세스 키를 다시 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2100">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="1d1eb-2101">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2101">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="1d1eb-2102">Event Grid 도메인 이벤트를 게시하는 데 사용되는 공유 액세스 키를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2102">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="1d1eb-2103">New-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2103">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="1d1eb-2104">새 Azure Event Grid 도메인 토픽을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2104">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="1d1eb-2105">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2105">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="1d1eb-2106">Event Grid 도메인 토픽의 세부 사항을 가져오거나, 현재 Azure의 특정 Event Grid 도메인 아래의 모든 Event Grid 도메인 토픽 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2106">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span>
    - <span data-ttu-id="1d1eb-2107">Remove-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2107">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="1d1eb-2108">기존 Azure Event Grid 도메인 토픽을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2108">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="1d1eb-2109">다음 Cmdlet이 업데이트 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2109">Updated cmdlets:</span></span>
    - <span data-ttu-id="1d1eb-2110">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2110">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="1d1eb-2111">새로운 Event Grid 도메인 및 Event Grid 도메인 토픽에 대한 파이핑을 지원하기 위해 새로운 필수 매개 변수를 추가하여 이러한 리소스 아래에 새 이벤트 구독을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2111">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="1d1eb-2112">새로운 Event Grid 도메인 이름 및 Event Grid 도메인 토픽 이름을 지정하기 위해 새로운 필수 매개 변수를 추가하여 이러한 리소스 아래에 새 이벤트 구독을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2112">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="1d1eb-2113">기존 매개 변수(예: EndPointType, SubjectBeginsWith 등)를 재사용할 수 있도록 도메인 및 도메인 토픽에 대한 새로운 매개 변수 집합을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2113">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="1d1eb-2114">지정을 위한 새로운 선택적 매개 변수를 추가</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2114">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="1d1eb-2115">이벤트 구독 만료 날짜,</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2115">Event subscription expiration date,</span></span>
            - <span data-ttu-id="1d1eb-2116">고급 필터링 매개 변수.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2116">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="1d1eb-2117">대상으로 servicebusqueue에 대한 새 열거형을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2117">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="1d1eb-2118">-IncludedEventType 옵션에서 'All' 사용을 허용하지 않고 다음으로 대체함</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2118">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span>
    - <span data-ttu-id="1d1eb-2119">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2119">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="1d1eb-2120">결과 페이지 매김 및 필터링을 지원하는 새로운 선택적 매개 변수(Top, ODataQuery 및 NextLink)를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2120">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="1d1eb-2121">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2121">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="1d1eb-2122">Event Grid 도메인 및 Event Grid 도메인 토픽에 대한 파이핑을 지원하기 위해 새로운 필수 매개 변수를 추가하여 이러한 리소스 아래에 기존 이벤트 구독을 제거할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2122">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="1d1eb-2123">Event Grid 도메인 이름 및 Event Grid 도메인 토픽 이름을 지정하기 위해 새로운 필수 매개 변수를 추가하여 이러한 리소스 아래에 기존 이벤트 구독을 제거할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2123">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="1d1eb-2124">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2124">Az.FrontDoor</span></span>
* <span data-ttu-id="1d1eb-2125">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2125">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="1d1eb-2126">변환 지원 및 새 연산자 자동 완성 값(RegEx)을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2126">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="1d1eb-2127">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2127">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="1d1eb-2128">새 자동 완성 값 추가</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2128">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="1d1eb-2129">Az.Network</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2129">Az.Network</span></span>
* <span data-ttu-id="1d1eb-2130">Microsoft Azure Virtual Network 게이트웨이 리소스에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2130">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="1d1eb-2131">새로운 cmdlet</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2131">New cmdlets</span></span>
        - <span data-ttu-id="1d1eb-2132">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2132">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="1d1eb-2133">AvailablePrivateEndpointType 추가</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2133">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="1d1eb-2134">새로운 cmdlet</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2134">New cmdlets</span></span>
        - <span data-ttu-id="1d1eb-2135">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2135">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="1d1eb-2136">PrivatePrivateLinkService 추가</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2136">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="1d1eb-2137">새로운 cmdlet</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2137">New cmdlets</span></span>
        - <span data-ttu-id="1d1eb-2138">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2138">Get-AzPrivateLinkService</span></span>
        - <span data-ttu-id="1d1eb-2139">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2139">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="1d1eb-2140">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2140">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="1d1eb-2141">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2141">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="1d1eb-2142">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2142">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="1d1eb-2143">PrivateEndpoint 추가</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2143">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="1d1eb-2144">새로운 cmdlet</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2144">New cmdlets</span></span>
        - <span data-ttu-id="1d1eb-2145">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2145">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="1d1eb-2146">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2146">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="1d1eb-2147">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2147">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="1d1eb-2148">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2148">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="1d1eb-2149">기능에 대한 새로운 명령이 업데이트됨: VpnConnection 상의 UseLocalAzureIpAddress 플래그</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2149">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="1d1eb-2150">New-AzVpnConnection이 업데이트됨: 선택적 매개 변수 -UseLocalAzureIpAddress를 추가하여 로컬 Azure IP 주소가 연결을 시작하는 동안 소스 주소로 사용되어야 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2150">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="1d1eb-2151">Set-AzVpnConnection이 업데이트됨: 선택적 매개 변수 -UseLocalAzureIpAddress를 추가하여 로컬 Azure IP 주소가 연결을 시작하는 동안 소스 주소로 사용되어야 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2151">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="1d1eb-2152">ExpressRoute 피어링에 읽기 전용 필드 PeeredConnections가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2152">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="1d1eb-2153">ExpressRoute에 읽기 전용 필드 GlobalReachEnabled가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2153">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="1d1eb-2154">ExpressRouteCircuit 모델에서 AllowGlobalReach 필드의 사용 중단을 부르는 호환성이 손상되는 변경 속성이 추가됨</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2154">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="1d1eb-2155">AzApplicationGatewayRedirectConfiguration cmdlet에서 TargetListenerID를 사용하는 중의 8756 오류 문제가 해결됨</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2155">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="1d1eb-2156">다시 쓰기 규칙 세트가 설정되지 못하게 하는 New-AzApplicationGatewayPathRuleConfig의 버그를 수정했습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2156">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="1d1eb-2157">NetworkInterfaceIpConfiguration에 VirtualNetworkTaps가 표시되는 방식이 수정됨</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2157">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="1d1eb-2158">모든 파트를 나열하도록 Cortex Get cmdlet이 수정됨</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2158">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="1d1eb-2159">ExpressRouteGateways, VpnGateway에 대한 VirtualHub 참조 생성 수정됨</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2159">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="1d1eb-2160">AzureFirewall 및 NatGateway의 가용성 영역에 대한 지원 추가됨</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2160">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="1d1eb-2161">Get-AzNetworkServiceTag cmdlet 추가됨</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2161">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="1d1eb-2162">Azure Firewall에 대한 여러 공용 IP 주소에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2162">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="1d1eb-2163">New-AzFirewall cmdlet이 업데이트됨:</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2163">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="1d1eb-2164">하나 이상의 공용 IP 주소 개체를 허용하는 매개 변수 -PublicIpAddress 추가됨</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2164">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="1d1eb-2165">Virtual Network 개체를 허용하는 매개 변수 -VirtualNetwork 추가됨</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2165">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="1d1eb-2166">방화벽 개체에 AddPublicIpAddress 및 RemovePublicIpAddress 메서드 추가됨 - 공용 IP 주소 개체를 입력으로 허용</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2166">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="1d1eb-2167">매개 변수 -PublicIpName 및 -VirtualNetworkName이 더 이상 사용되지 않음</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2167">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span>
* <span data-ttu-id="1d1eb-2168">기능에 대한 새로운 명령이 업데이트됨: VpnClient AAD 인증 옵션을 가상 네트워크 게이트웨이 리소스로 설정했습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2168">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span>
    - <span data-ttu-id="1d1eb-2169">New-AzVirtualNetworkGateway가 업데이트됨: 게이트웨이에서 VpnClient AAD 인증 옵션을 설정할 수 있도록 선택적 매개 변수 AadTenantUri, AadAudienceId, AadIssuerUri가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2169">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="1d1eb-2170">Set-AzVirtualNetworkGateway가 업데이트됨: 게이트웨이에서 VpnClient AAD 인증 옵션을 설정할 수 있도록 선택적 매개 변수 AadTenantUri, AadAudienceId, AadIssuerUri가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2170">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="1d1eb-2171">Set-AzVirtualNetworkGateway가 업데이트됨: 게이트웨이에서 VpnClient AAD 인증 옵션을 제거할 수 있도록 선택적인 스위치 매개 변수 RemoveAadAuthentication이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2171">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="1d1eb-2172">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2172">Az.OperationalInsights</span></span>
* <span data-ttu-id="1d1eb-2173">'New-AzureRmOperationalInsightsWorkspace' 명령에서 **pergb2018** 가격 책정 계층 사용</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2173">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="1d1eb-2174">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2174">Az.Resources</span></span>
* <span data-ttu-id="1d1eb-2175">추가 템플릿 내보내기 옵션 지원</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2175">Support for additional Template Export options</span></span>
    - <span data-ttu-id="1d1eb-2176">Export-AzResourceGroup에 '-SkipResourceNameParameterization' 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2176">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="1d1eb-2177">Export-AzResourceGroup에 '-SkipAllParameterization' 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2177">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="1d1eb-2178">내보낸 리소스 필터링을 위해 Export-AzResourceGroup에 '-Resource' 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2178">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="1d1eb-2179">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2179">Az.ServiceFabric</span></span>
* <span data-ttu-id="1d1eb-2180">일부 경우 잘못된 지문을 가져오는 추가 인증서 ByExistingKeyVault 수정</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2180">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="1d1eb-2181">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2181">Az.Sql</span></span>
* <span data-ttu-id="1d1eb-2182">Advanced Threat Protection 스토리지 엔드포인트 접미사 수정</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2182">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="1d1eb-2183">Advanced Data Security가 Advanced Threat Protection 정책을 재정의하는 것을 수정</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2183">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="1d1eb-2184">고객이 TDE 키를 추가하고 관리되는 인스턴스에 TDE 보호기를 설정할 수 있도록 Management.Sql용 새 Cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2184">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="1d1eb-2185">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2185">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="1d1eb-2186">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2186">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="1d1eb-2187">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2187">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="1d1eb-2188">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2188">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="1d1eb-2189">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2189">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="1d1eb-2190">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2190">Az.Storage</span></span>
* <span data-ttu-id="1d1eb-2191">스토리지 계정 생성 시 종류 FileStorage 및 SkuName Premium_ZRS 지원</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2191">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="1d1eb-2192">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2192">New-AzStorageAccount</span></span>
* <span data-ttu-id="1d1eb-2193">BLOB immutability cmdlet의 설명 명확화</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2193">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="1d1eb-2194">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2194">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="1d1eb-2195">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2195">Az.Websites</span></span>
* <span data-ttu-id="1d1eb-2196">Get-AzWebAppCertificate를 클라이언트 대신 서버의 리소스 그룹별로 필터링하도록 최적화</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2196">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="1d1eb-2197">Get-AzWebAppSnapshot에 -UseDisasterRecovery 스위치 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2197">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="1d1eb-2198">2.2.0 - 2019년 6월</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2198">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="1d1eb-2199">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2199">Az.Cdn</span></span>
* <span data-ttu-id="1d1eb-2200">cmdlet에서 2019-04-15 API 버전 기반의 rulesEngine 기능을 지원하도록 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2200">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="1d1eb-2201">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2201">Az.Compute</span></span>
* <span data-ttu-id="1d1eb-2202">작업을 시작하여 완료되기 전에 즉시 반환하는 `NoWait` 매개 변수가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2202">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="1d1eb-2203">다음 Cmdlet이 업데이트 되었습니다.   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2203">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="1d1eb-2204">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2204">Az.EventHub</span></span>
* <span data-ttu-id="1d1eb-2205">#9231 수정 - Get-AzEventHubNamespace에서 태그를 반환하지 않음</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2205">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="1d1eb-2206">#9230 수정 - Get-AzEventHubNamespace에서 ResourceGroupName 대신 ResourceGroup을 반환함</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2206">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="1d1eb-2207">Az.Network</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2207">Az.Network</span></span>
* <span data-ttu-id="1d1eb-2208">Nat Gateway에 대한 ResourceId 및 InputObject 업데이트</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2208">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="1d1eb-2209">ResourceId 및 InputObject에 대한 별칭 추가</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2209">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="1d1eb-2210">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2210">Az.PolicyInsights</span></span>
* <span data-ttu-id="1d1eb-2211">Get-AzPolicyEvent에서 Null 참조 문제 해결</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2211">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="1d1eb-2212">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2212">Az.RecoveryServices</span></span>
* <span data-ttu-id="1d1eb-2213">IaaSVM 정책 최소 보존 기간(일)이 1에서 7로 변경됨</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2213">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="1d1eb-2214">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2214">Az.ServiceBus</span></span>
* <span data-ttu-id="1d1eb-2215">#9182 문제 해결 - Get-AzServiceBusNamespace에서 ResourceGroupName 대신 ResourceGroup을 반환</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2215">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="1d1eb-2216">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2216">Az.ServiceFabric</span></span>
* <span data-ttu-id="1d1eb-2217">'Update-AzServiceFabricReliability' 오류 메시지의 오타 수정</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2217">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="1d1eb-2218">Service Fabric 명령줄에서 누락된 문자 수정</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2218">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="1d1eb-2219">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2219">Az.Sql</span></span>
* <span data-ttu-id="1d1eb-2220">Managed Instance에 대한 AutoDr을 지원하기 위해 New-AzureSqlInstance cmdlet에 대한 DnsZonePartner 매개 변수를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2220">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="1d1eb-2221">Get-AzSqlDatabaseSecureConnectionPolicy cmdlet 사용 중단</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2221">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="1d1eb-2222">Threat Detection(위협 탐지) cmdlet 이름을 Advanced Threat Protection으로 변경함</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2222">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="1d1eb-2223">새 AzSqlInstance -StorageSizeInGB 및 -LicenseType 매개 변수는 이제 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2223">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="1d1eb-2224">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2224">Az.Websites</span></span>
* <span data-ttu-id="1d1eb-2225">-WebApp 속성에서 Set-AzWebApp 및 Set-AzWebAppSlot을 사용하면 태그가 제거되는 문제를 해결함</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2225">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="1d1eb-2226">2.1.0 - 2019년 5월</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2226">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="1d1eb-2227">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2227">Az.ApiManagement</span></span>
* <span data-ttu-id="1d1eb-2228">글로벌 및 API 범위에서 진단을 관리하기 위한 새 cmdlet을 만들었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2228">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="1d1eb-2229">**Get-AzApiManagementDiagnostic** - 글로벌 또는 API 범위가 구성된 진단 가져오기</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2229">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="1d1eb-2230">**New-AzApiManagementDiagnostic** - 글로벌 범위 또는 API 범위에서 새 진단 만들기</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2230">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="1d1eb-2231">**New-AzApiManagementHttpMessageDiagnostic** - 기록할 Headers(헤더) 및 Body Bytes(본문 바이트 수) 크기에 대한 진단 설정 만들기</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2231">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="1d1eb-2232">**New-AzApiManagementPipelineDiagnosticSetting** - 게이트웨이로 들어오고 나가는 HTTP 메시지에 대한 진단 설정 만들기</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2232">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="1d1eb-2233">**New-AzApiManagementSamplingSetting** - 진단 요청/응답에 대한 샘플링 설정 만들기</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2233">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="1d1eb-2234">**Remove-AzApiManagementDiagnostic** - 글로벌 또는 API 범위에서 진단 엔터티 제거</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2234">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="1d1eb-2235">**Set-AzApiManagementDiagnostic** - 글로벌 또는 API 범위에서 진단 엔터티 업데이트</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2235">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="1d1eb-2236">ApiManagement 서비스에서 캐시를 관리하기 위한 새 cmdlet을 만들었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2236">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="1d1eb-2237">**Get-AzApiManagementCache** - 식별자 또는 모든 캐시로 지정된 캐시의 세부 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2237">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="1d1eb-2238">**New-AzApiManagementCache** - 특정 Azure 'region'(지역)에 새 'default'(기본) 캐시 만들기</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2238">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="1d1eb-2239">**Remove-AzApiManagementCache** - 캐시 제거</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2239">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="1d1eb-2240">**Update-AzApiManagementCache** - 캐시 업데이트</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2240">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="1d1eb-2241">API 스키마 관리하기 위한 새 cmdlet을 만들었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2241">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="1d1eb-2242">**New-AzApiManagementSchema** - API에 대한 새 스키마 만들기</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2242">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="1d1eb-2243">**Get-AzApiManagementSchema** - API에 구성된 스키마 가져오기</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2243">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="1d1eb-2244">**Remove-AzApiManagementSchema** - API에 구성된 스키마 제거</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2244">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="1d1eb-2245">**Set-AzApiManagementSchema** - API에 구성된 스키마 업데이트</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2245">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="1d1eb-2246">사용자 토큰을 생성하기 위한 새 cmdlet을 만들었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2246">Created new Cmdlet for generating a User Token.</span></span>
    - <span data-ttu-id="1d1eb-2247">**New-AzApiManagementUserToken** - 기본적으로 8시간 동안 유효한 새 사용자 토큰을 생성합니다. 'GIT' 사용자에 대한 토큰은 이 cmdlet을 사용하여 생성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2247">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="1d1eb-2248">네트워크 상태를 검색하기 위한 새 cmdlet을 만들었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2248">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="1d1eb-2249">**Get-AzApiManagementNetworkStatus** - API Management 서비스에서 사용하는 리소스의 네트워크 상태 연결을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2249">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="1d1eb-2250">ApiManagement 서비스를 가상 네트워크에 배포하고 종속성이 손상되었는지 여부를 확인할 때 유용합니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2250">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="1d1eb-2251">**New-AzApiManagement** cmdlet에서 ApiManagement 서비스를 관리하도록 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2251">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span>
    - <span data-ttu-id="1d1eb-2252">새 '소비' SKU 지원이 추가됨</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2252">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="1d1eb-2253">'소비' SKU에 대해 'EnableClientCertificate' 플래그를 설정하기 위한 지원이 추가됨</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2253">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="1d1eb-2254">새 **New-AzApiManagementSslSetting** cmdlet을 사용하면 'Backend(백 엔드)' 및 'Frontend'(프런트 엔드)에서 'TLS/SSL' 설정을 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2254">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="1d1eb-2255">또한 ApiManagement 서비스의 'Frontend'에서 '3DES'와 같은 'Ciphers'와 'Http2'와 같은 'ServerProtocols'를 구성하는 데 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2255">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="1d1eb-2256">ApiManagement 서비스에서 'DeveloperPortal' 호스트 이름을 구성하기 위한 지원이 추가됨</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2256">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="1d1eb-2257">**Get-AzApiManagementSsoToken** cmdlet에서 'PsApiManagement' 개체를 입력으로 사용하도록 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2257">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="1d1eb-2258">cmdlet에서 오류 메시지를 인라인으로 표시하도록 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2258">Updated the cmdlet to display Error Messages inline</span></span>
     > <span data-ttu-id="1d1eb-2259">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : 오류 코드: ValidationError 오류 메시지: 하나 이상의 필드에 잘못된 값이 있습니다. 오류 세부 정보:    [Code=ValidationError, Message=줄 3, 열 10의 'log-to-eventhub' 요소에 오류가 있습니다.: 로거를 찾지 못함, Target=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2259">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="1d1eb-2260">**Export-AzApiManagementApi** cmdlet에서 API를 'OpenApi 3.0' 형식으로 내보내도록 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2260">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="1d1eb-2261">**Import-AzApiManagementApi** cmdlet을 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2261">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="1d1eb-2262">'OpenApi 3.0' 문서 사양에서 API 가져오기</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2262">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="1d1eb-2263">문서('Swagger', 'Wadl', 'Wsdl', 'OpenApi')에 지정된 'PsApiManagementSchema' 속성 재정의</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2263">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="1d1eb-2264">문서에 지정된 'ServiceUrl' 속성 재정의</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2264">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="1d1eb-2265">**Get-AzApiManagementPolicy** cmdlet에서 'rawxml'을 사용하여 이스케이프된 비 Xml 'format'(형식)의 정책을 반환하도록 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2265">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="1d1eb-2266">**Set-AzApiManagementPolicy** cmdlet에서 'rawxml'을 사용하여 이스케이프된 비 Xml 'format'의 정책을 수락하고, 'xml'을 사용하여 이스케이프된 Xml 'format'의 정책을 수락하도록 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2266">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="1d1eb-2267">**New-AzApiManagementApi** cmdlet을 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2267">Updated cmdlet **New-AzApiManagementApi**</span></span>
    - <span data-ttu-id="1d1eb-2268">'OpenId' 권한 부여 서버를 사용하여 API 구성</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2268">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="1d1eb-2269">'ApiVersionSet'에서 API 만들기</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2269">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="1d1eb-2270">'SourceApiId' 및 'SourceApiRevision'을 사용하여 API 복제</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2270">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="1d1eb-2271">API 범위에서 'SubscriptionRequired' 구성 가능</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2271">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="1d1eb-2272">**Set-AzApiManagementApi** cmdlet을 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2272">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="1d1eb-2273">'OpenId' 권한 부여 서버를 사용하여 API 구성</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2273">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="1d1eb-2274">API를 'ApiVersionSet'으로 업데이트</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2274">To updated an API into an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="1d1eb-2275">API 범위에서 'SubscriptionRequired' 구성 가능</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2275">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="1d1eb-2276">**New-AzApiManagementRevision** cmdlet을 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2276">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="1d1eb-2277">'SourceApiRevision'을 사용하여 기존 수정 버전 복제(태그, 제품, 작업 및 정책 복사).</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2277">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="1d1eb-2278">새 수정 버전은 부모의 'ApiId'를 가정합니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2278">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="1d1eb-2279">'ApiRevisionDescription' 제공</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2279">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="1d1eb-2280">API 복제 시 'ServiceUrl' 재정의</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2280">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="1d1eb-2281">**New-AzApiManagementIdentityProvider** cmdlet을 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2281">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="1d1eb-2282">'Authority'를 사용하여 'AAD' 또는 'AADB2C' 구성</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2282">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="1d1eb-2283">'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' 및 'PasswordResetPolicy' 설정</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2283">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="1d1eb-2284">**New-AzApiManagementSubscription** cmdlet을 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2284">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="1d1eb-2285">'Scope' 및 'UserId'를 사용하여 새 SubscriptonModel 설명</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2285">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="1d1eb-2286">'ProductId' 및 'UserId'를 사용하여 이전 구독 모델 설명</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2286">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="1d1eb-2287">구독 수준에서 'AllowTracing'을 사용하도록 설정하는 지원 추가</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2287">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="1d1eb-2288">**Set-AzApiManagementSubscription** cmdlet을 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2288">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="1d1eb-2289">'Scope' 및 'UserId'를 사용하여 새 SubscriptonModel 설명</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2289">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="1d1eb-2290">'ProductId' 및 'UserId'를 사용하여 이전 구독 모델 설명</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2290">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="1d1eb-2291">구독 수준에서 'AllowTracing'을 사용하도록 설정하는 지원 추가</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2291">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="1d1eb-2292">다음 cmdlet에서 'ResourceId'를 입력으로 수락하도록 업데이트했습니다</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2292">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="1d1eb-2293">'New-AzApiManagementContext'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2293">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="1d1eb-2294">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2294">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="1d1eb-2295">'Get-AzApiManagementApiRelease'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2295">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="1d1eb-2296">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2296">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="1d1eb-2297">'Get-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2297">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="1d1eb-2298">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2298">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="1d1eb-2299">'Get-AzApiManagementAuthorizationServer'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2299">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="1d1eb-2300">'Get-AzApiManagementBackend'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2300">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="1d1eb-2301">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2301">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="1d1eb-2302">'Get-AzApiManagementCertificate'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2302">'Get-AzApiManagementCertificate'</span></span>
    - <span data-ttu-id="1d1eb-2303">'Remove-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2303">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="1d1eb-2304">'Remove-AzApiManagementSubscription'</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2304">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="1d1eb-2305">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2305">Az.Automation</span></span>
* <span data-ttu-id="1d1eb-2306">Get-AzAutomationJobOutputRecord에서 JSON 및 Text 레코드 값을 처리하도록 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2306">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="1d1eb-2307">문제 https://github.com/Azure/azure-powershell/issues/7977 수정</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2307">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="1d1eb-2308">문제 https://github.com/Azure/azure-powershell/issues/8600 수정</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2308">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="1d1eb-2309">Start-AzAutomationDscCompilationJob에서 완료될 때까지 기다리지 않고 작업을 바로 시작하도록 변경했습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2309">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="1d1eb-2310">문제 https://github.com/Azure/azure-powershell/issues/8347 수정</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2310">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="1d1eb-2311">-Name을 사용하면 모든 노드를 반환하는 Get-AzAutomationDscNode 수정.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2311">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="1d1eb-2312">이제 일치하는 노드만 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2312">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="1d1eb-2313">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2313">Az.Compute</span></span>
* <span data-ttu-id="1d1eb-2314">ProtectFromScaleIn 및 ProtectFromScaleSetAction 매개 변수를 Update-AzVmssVM cmdlet에 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2314">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="1d1eb-2315">'East US'(미국 동부)가 지원되지 않는 경우 이제 New-AzVM wimple 매개 변수 집합에서 기본적으로 사용 가능한 위치를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2315">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="1d1eb-2316">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2316">Az.DataLakeStore</span></span>
* <span data-ttu-id="1d1eb-2317">ADLS SDK에서 httpclient를 사용하도록 업데이트하고, 데이터 평면 테스트를 Azure 프레임워크와 통합합니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2317">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="1d1eb-2318">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2318">Az.Monitor</span></span>
* <span data-ttu-id="1d1eb-2319">도움말 예제에서 잘못된 매개 변수 이름을 수정했습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2319">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="1d1eb-2320">Az.Network</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2320">Az.Network</span></span>
* <span data-ttu-id="1d1eb-2321">DisableBgpRoutePropagation 플래그를 유효 경로 테이블 출력에 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2321">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="1d1eb-2322">업데이트된 cmdlet:</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2322">Updated cmdlet:</span></span>
        - <span data-ttu-id="1d1eb-2323">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2323">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="1d1eb-2324">New-AzApplicationGatewayTrustedRootCertificate 설명서에서 이중 파선을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2324">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="1d1eb-2325">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2325">Az.Resources</span></span>
* <span data-ttu-id="1d1eb-2326">할당 거부를 검색하기 위한 새 Get-AzureRmDenyAssignment cmdlet을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2326">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="1d1eb-2327">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2327">Az.Sql</span></span>
* <span data-ttu-id="1d1eb-2328">Advanced Threat Protection cmdlet의 이름을 Advanced Data Security로 변경하고, 취약성 평가를 기본적으로 사용하도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2328">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="1d1eb-2329">2.0.0 - 2019년 5월</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2329">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="1d1eb-2330">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2330">Az.Accounts</span></span>
* <span data-ttu-id="1d1eb-2331">사용자 이름/비밀번호 인증을 사용하여 ADFS 문제를 해결하도록 인증 라이브러리 업데이트</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2331">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="1d1eb-2332">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2332">Az.CognitiveServices</span></span>
* <span data-ttu-id="1d1eb-2333">Bing Search 서비스에 대해서만 Bing 면책 조항을 표시하세요.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2333">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="1d1eb-2334">계정 생성 실패 시 오류 개선.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2334">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="1d1eb-2335">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2335">Az.Compute</span></span>
* <span data-ttu-id="1d1eb-2336">근접 배치 그룹 기능</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2336">Proximity placement group feature.</span></span>
    - <span data-ttu-id="1d1eb-2337">다음과 같은 새 cmdlet을 추가했습니다.   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2337">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="1d1eb-2338">새 매개 변수 ProximityPlacementGroupId가 다음 cmdlet에 추가됩니다.   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2338">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="1d1eb-2339">New-AzGalleryImageVersion에 StorageAccountType 매개 변수가 추가됩니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2339">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="1d1eb-2340">New-AzGalleryImageVersion의 TargetRegion이 StorageAccountType를 포함할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2340">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="1d1eb-2341">SkipShutdown 스위치 매개 변수가 Stop-AzVM 및 Stop-AzVmss에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2341">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>
* <span data-ttu-id="1d1eb-2342">주요 변경 내용</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2342">Breaking changes</span></span>
    - <span data-ttu-id="1d1eb-2343">Set-AzVMBootDiagnostics이 Set-AzVMBootDiagnostic으로 변경됩니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2343">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="1d1eb-2344">Export-AzLogAnalyticThrottledRequests이 Export-AzLogAnalyticThrottledRequests로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2344">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="1d1eb-2345">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2345">Az.DeploymentManager</span></span>
* <span data-ttu-id="1d1eb-2346">Azure 배포 관리자 cmdlet의 일반적으로 사용 가능한 첫 번째 릴리스</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2346">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="1d1eb-2347">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2347">Az.Dns</span></span>
* <span data-ttu-id="1d1eb-2348">자동 DNS 이름 서버 위임</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2348">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="1d1eb-2349">DNS 영역 만들기 cmdlet은 추가 선택적 매개 변수로 부모 영역 이름을 허용합니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2349">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="1d1eb-2350">새로 생성 된 자식 영역의 부모 영역에 NS 레코드를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2350">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="1d1eb-2351">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2351">Az.FrontDoor</span></span>
* <span data-ttu-id="1d1eb-2352">Azure FrontDoor cmdlet의 일반적으로 사용 가능한 첫 번째 릴리스</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2352">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="1d1eb-2353">'Waf'를 포함하도록 WAF cmdlet의 이름 바꾸기</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2353">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="1d1eb-2354">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2354">Az.HDInsight</span></span>
* <span data-ttu-id="1d1eb-2355">두 개의 cmdlet을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2355">Removed two cmdlets:</span></span>
    - <span data-ttu-id="1d1eb-2356">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2356">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="1d1eb-2357">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2357">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="1d1eb-2358">Grant-AzHDInsightHttpServicesAccess를 대체할 새 cmdlet Set-AzHDInsightGatewayCredential을 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2358">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="1d1eb-2359">reader 역할과 HDInsight 운영자 역할을 구분하도록 cmdlet Get-AzHDInsightJobOutput 업데이트:</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2359">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="1d1eb-2360">reader 역할을 가진 사용자는 'DefaultStorageAccountKey'매개 변수를 명시적으로 지정해야 합니다. 그렇지 않으면 오류가 발생합니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2360">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="1d1eb-2361">Hdinsight 운영자 역할을 가진 사용자를 영향을 받지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2361">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="1d1eb-2362">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2362">Az.Monitor</span></span>
* <span data-ttu-id="1d1eb-2363">SQR API(예약 쿼리 규칙)용 새 cmdlet</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2363">New cmdlets for SQR API (Scheduled Query Rule)</span></span>
    - <span data-ttu-id="1d1eb-2364">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2364">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="1d1eb-2365">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2365">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="1d1eb-2366">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2366">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="1d1eb-2367">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2367">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="1d1eb-2368">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2368">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="1d1eb-2369">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2369">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="1d1eb-2370">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2370">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="1d1eb-2371">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2371">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="1d1eb-2372">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2372">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="1d1eb-2373">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2373">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="1d1eb-2374">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2374">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="1d1eb-2375">SQR API에 대한 [자세한 내용](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules)</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2375">[More](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="1d1eb-2376">GenV2(비 클래식) 메트릭 기반 경고 규칙에 대한 cmdlet을 포함하도록 Az.Monitor.md가 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2376">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="1d1eb-2377">Az.Network</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2377">Az.Network</span></span>
* <span data-ttu-id="1d1eb-2378">Nat 게이트웨이 리소스에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2378">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="1d1eb-2379">새로운 cmdlet</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2379">New cmdlets</span></span>
        - <span data-ttu-id="1d1eb-2380">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2380">New-AzNatGateway</span></span>
        - <span data-ttu-id="1d1eb-2381">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2381">Get-AzNatGateway</span></span>
        - <span data-ttu-id="1d1eb-2382">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2382">Set-AzNatGateway</span></span>
        - <span data-ttu-id="1d1eb-2383">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2383">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="1d1eb-2384">다음 Cmdlet이 업데이트 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2384">Updated cmdlets</span></span>
        - <span data-ttu-id="1d1eb-2385">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2385">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="1d1eb-2386">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2386">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="1d1eb-2387">기능에 대한 새로운 명령이 업데이트됨: Brooklyn Gateway에서 사용자 지정 경로 설정/제거.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2387">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="1d1eb-2388">New-AzVirtualNetworkGateway가 업데이트됨: 선택적 매개 변수 -CustomRoute를 추가하여 게이트웨이에서 설정할 사용자 지정 경로로 주소 접두사를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2388">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="1d1eb-2389">Set-AzVirtualNetworkGateway가 업데이트됨: 선택적 매개 변수 -CustomRoute를 추가하여 게이트웨이에서 설정할 사용자 지정 경로로 주소 접두사를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2389">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="1d1eb-2390">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2390">Az.PolicyInsights</span></span>
* <span data-ttu-id="1d1eb-2391">정책 평가 세부 정보 쿼리 지원</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2391">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="1d1eb-2392">Get-AzPolicyState에 '-Expand'매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2392">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="1d1eb-2393">'-Expand PolicyEvaluationDetails' 지원</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2393">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="1d1eb-2394">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2394">Az.RecoveryServices</span></span>
* <span data-ttu-id="1d1eb-2395">크로스 구독 Azure에서 Azure 사이트 복구 지원</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2395">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="1d1eb-2396">Azure Site Recovery에 대한 호환성이 손상되는 변경 표시</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2396">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="1d1eb-2397">Azure Site Recovery 복구 계획 최종 실행 계획에 대한 수정</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2397">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="1d1eb-2398">Azure에서 Azure에 대한 Azure Site Recovery 업데이트 네트워크 매핑 수정</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2398">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="1d1eb-2399">관리 디스크에 대한 Azure에서 Azure에 대한 Azure Site Recovery 업데이트 보호 방향 수정</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2399">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="1d1eb-2400">기타 사소한 수정.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2400">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="1d1eb-2401">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2401">Az.Relay</span></span>
* <span data-ttu-id="1d1eb-2402">고객 관련 메시지의 철자 오류 수정</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2402">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="1d1eb-2403">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2403">Az.ServiceBus</span></span>
* <span data-ttu-id="1d1eb-2404">네임스페이스의 NetworkRuleSet에 대한 새 cmdlet가 추가되었습니다</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2404">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="1d1eb-2405">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2405">Az.Storage</span></span>
* <span data-ttu-id="1d1eb-2406">저장소 클라이언트 라이브러리 10.0.1로 업그레이드(이 SDK의 모든 개체의 네임스페이스가 'Microsoft.WindowsAzure.Storage. *'에서 'Microsoft.Azure.Storage.* '로 변경됨)</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2406">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage. *' to 'Microsoft.Azure.Storage.* ')</span></span>
* <span data-ttu-id="1d1eb-2407">새로운 API 버전 2019-04-01을 지원하기 위해 Microsoft.Azure.Management.Storage 11.0.0으로 업그레이드합니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2407">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="1d1eb-2408">스토리지 생성 계정의 기본 스토리지 계정 종류가 'Storage'에서 'StorageV2'로 변경됩니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2408">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="1d1eb-2409">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2409">New-AzStorageAccount</span></span>
* <span data-ttu-id="1d1eb-2410">'StandardLRS'가 'Standard_LRS'로 변경되는 것과 같이 '-'을 추가하여 입력 SkuName과 정렬되도록 스토리지 계정 cmdlet 출력 Sku.Name을 변경합니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2410">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="1d1eb-2411">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2411">New-AzStorageAccount</span></span>
    - <span data-ttu-id="1d1eb-2412">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2412">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="1d1eb-2413">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2413">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="1d1eb-2414">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2414">Az.Websites</span></span>
* <span data-ttu-id="1d1eb-2415">Get-AzWebApp에서 반환한 PSSite 개체에 대해 'Kind'속성이 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2415">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="1d1eb-2416">Get-AzWebApp\* 메트릭 및 Get-AzAppServicePlanMetrics가 사용되지 않음으로 표시되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2416">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="1d1eb-2417">1.8.0 - 2019년 4월</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2417">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="1d1eb-2418">마지막 주 릴리스 이후의 주요 사항</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2418">Highlights since the last major release</span></span>
* <span data-ttu-id="1d1eb-2419">`Az` 모듈 일반 공급</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2419">General availability of `Az` module</span></span>
* <span data-ttu-id="1d1eb-2420">`Az` 모듈에 대한 자세한 내용은 https://aka.ms/azps-announce 를 방문하세요.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2420">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="1d1eb-2421">Location, ResourceGroup 및 ResourceName 완성자가 추가되었습니다(https://azure.microsoft.com/blog/completers-in-azure-powershell/ ).</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2421">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="1d1eb-2422">와일드카드 지원이 Az.Compute 및 Az.Network에 대한 Get cmdlet에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2422">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="1d1eb-2423">Windows PowerShell 5.1 전용 대화형 사용자 이름/암호 인증이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2423">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="1d1eb-2424">Python 2 Runbook 지원이 Az.Automation에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2424">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="1d1eb-2425">Az.LogicApp: 통합 계정 어셈블리 및 일괄 처리 구성을 위한 새로운 cmdlet입니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2425">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="1d1eb-2426">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2426">Az.Accounts</span></span>
* <span data-ttu-id="1d1eb-2427">Mac에서 모듈을 올바르게 삭제하기 위해 Uninstall-AzureRm을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2427">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="1d1eb-2428">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2428">Az.Batch</span></span>
* <span data-ttu-id="1d1eb-2429">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2429">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="1d1eb-2430">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2430">Az.Cdn</span></span>
* <span data-ttu-id="1d1eb-2431">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2431">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="1d1eb-2432">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2432">Az.CognitiveServices</span></span>
* <span data-ttu-id="1d1eb-2433">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2433">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="1d1eb-2434">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2434">Az.Compute</span></span>
* <span data-ttu-id="1d1eb-2435">디스크의 리소스 ID에 리소스 ID의 소문자 resourcegroups가 있는 경우 AEM 설치 문제 수정</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2435">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="1d1eb-2436">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2436">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="1d1eb-2437">와일드 카드에 대한 설명서 수정</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2437">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="1d1eb-2438">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2438">Az.DataFactory</span></span>
* <span data-ttu-id="1d1eb-2439">NodeCount가 관리형 통합 런타임에 대해 Null이 아닌 경우 SsisProperties를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2439">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="1d1eb-2440">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2440">Az.DataLakeStore</span></span>
* <span data-ttu-id="1d1eb-2441">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2441">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="1d1eb-2442">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2442">Az.EventGrid</span></span>
* <span data-ttu-id="1d1eb-2443">이벤트 구독 cmdlet 만들기/업데이트를 사용하기 전에 리소스를 만들어야 함을 나타내기 위해 엔드포인트의 도움말 텍스트가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2443">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="1d1eb-2444">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2444">Az.EventHub</span></span>
* <span data-ttu-id="1d1eb-2445">네임스페이스의 NetworkRuleSet에 대한 새 cmdlet가 추가되었습니다</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2445">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="1d1eb-2446">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2446">Az.HDInsight</span></span>
* <span data-ttu-id="1d1eb-2447">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2447">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="1d1eb-2448">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2448">Az.IotHub</span></span>
* <span data-ttu-id="1d1eb-2449">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2449">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="1d1eb-2450">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2450">Az.KeyVault</span></span>
* <span data-ttu-id="1d1eb-2451">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2451">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="1d1eb-2452">와일드 카드에 대한 설명서 수정</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2452">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="1d1eb-2453">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2453">Az.MachineLearning</span></span>
* <span data-ttu-id="1d1eb-2454">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2454">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="1d1eb-2455">Az.Media</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2455">Az.Media</span></span>
* <span data-ttu-id="1d1eb-2456">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2456">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="1d1eb-2457">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2457">Az.Monitor</span></span>
  * <span data-ttu-id="1d1eb-2458">GenV2(비 클래식) 메트릭 기반 경고 규칙에 대한 새 cmdlet</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2458">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="1d1eb-2459">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2459">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="1d1eb-2460">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2460">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="1d1eb-2461">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2461">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="1d1eb-2462">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2462">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="1d1eb-2463">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2463">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="1d1eb-2464">모니터 SDK가 버전 0.22.0-preview로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2464">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="1d1eb-2465">Az.Network</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2465">Az.Network</span></span>
* <span data-ttu-id="1d1eb-2466">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2466">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="1d1eb-2467">와일드 카드에 대한 설명서 수정</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2467">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="1d1eb-2468">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2468">Az.NotificationHubs</span></span>
* <span data-ttu-id="1d1eb-2469">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2469">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="1d1eb-2470">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2470">Az.OperationalInsights</span></span>
* <span data-ttu-id="1d1eb-2471">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2471">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="1d1eb-2472">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2472">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="1d1eb-2473">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2473">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="1d1eb-2474">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2474">Az.RecoveryServices</span></span>
* <span data-ttu-id="1d1eb-2475">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2475">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="1d1eb-2476">Azure VM의 SQL용 테이블 형식이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2476">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="1d1eb-2477">AzureFileShare에서 위치를 가져오는 대체 메서드가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2477">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="1d1eb-2478">시간대에 따라 SchedulePolicy 개체의 ScheduleRunDays가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2478">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="1d1eb-2479">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2479">Az.RedisCache</span></span>
* <span data-ttu-id="1d1eb-2480">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2480">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="1d1eb-2481">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2481">Az.Resources</span></span>
* <span data-ttu-id="1d1eb-2482">와일드 카드에 대한 설명서 수정</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2482">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="1d1eb-2483">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2483">Az.Sql</span></span>
* <span data-ttu-id="1d1eb-2484">Monitor SDK의 종속성을 공용 코드로 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2484">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="1d1eb-2485">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2485">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="1d1eb-2486">다중 열 분류 프로세스가 향상되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2486">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="1d1eb-2487">기본적으로 Get-AzSqlServerServiceObjective의 응답으로 SKU 속성(SKU 이름, 제품군, 용량)과 테이블 형식을 포함합니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2487">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="1d1eb-2488">해당 지역에 기존 서버 없이 위치별로 Get-AzSqlServerServiceObjective를 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2488">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="1d1eb-2489">관리형 인스턴스 생성 시 표준 시간대 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2489">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="1d1eb-2490">와일드 카드에 대한 설명서 수정</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2490">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="1d1eb-2491">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2491">Az.Websites</span></span>
* <span data-ttu-id="1d1eb-2492">실행 시 태그를 제거하지 않도록 Set-AzWebApp 및 Set-AzWebAppSlot를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2492">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="1d1eb-2493">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2493">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="1d1eb-2494">WebSites SDK가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2494">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="1d1eb-2495">PSAppServicePlan에서 AdminSiteName 속성을 제거했습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2495">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="1d1eb-2496">1.7.0 - 2019년 4월</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2496">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="1d1eb-2497">마지막 주 릴리스 이후의 주요 사항</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2497">Highlights since the last major release</span></span>
* <span data-ttu-id="1d1eb-2498">`Az` 모듈 일반 공급</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2498">General availability of `Az` module</span></span>
* <span data-ttu-id="1d1eb-2499">`Az` 모듈에 대한 자세한 내용은 https://aka.ms/azps-announce 를 방문하세요.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2499">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="1d1eb-2500">Location, ResourceGroup 및 ResourceName 완성자가 추가되었습니다(https://azure.microsoft.com/blog/completers-in-azure-powershell/ ).</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2500">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="1d1eb-2501">와일드카드 지원이 Az.Compute 및 Az.Network에 대한 Get cmdlet에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2501">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="1d1eb-2502">Windows PowerShell 5.1 전용 대화형 사용자 이름/암호 인증이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2502">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="1d1eb-2503">Python 2 Runbook 지원이 Az.Automation에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2503">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="1d1eb-2504">Az.LogicApp: 통합 계정 어셈블리 및 일괄 처리 구성을 위한 새로운 cmdlet입니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2504">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="1d1eb-2505">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2505">Az.Accounts</span></span>
* <span data-ttu-id="1d1eb-2506">매개 변수 AzureAnalysisServicesEndpointResourceId를 허용하도록 Add-AzEnvironment 및 Set-AzEnvironment 업데이트</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2506">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="1d1eb-2507">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2507">Az.AnalysisServices</span></span>
* <span data-ttu-id="1d1eb-2508">데이터 평면 cmdlet에서 ServiceClient 사용 및 원본 인증 논리 제거</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2508">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="1d1eb-2509">호환성이 손상되는 변경을 방지하기 위해 Add-AzureASAccount를 Connect-AzAccount의 래퍼로 만듦</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2509">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="1d1eb-2510">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2510">Az.Automation</span></span>
* <span data-ttu-id="1d1eb-2511">포함에 대한 New-AzAutomationSoftwareUpdateConfiguration cmdlet 버그 수정</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2511">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="1d1eb-2512">이제 매개 변수 IncludedKbNumber 및 IncludedPackageNameMask가 작동함</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2512">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="1d1eb-2513">Azure 자동화 업데이트 관리 동적 그룹에 대한 버그 수정</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2513">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="1d1eb-2514">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2514">Az.Compute</span></span>
* <span data-ttu-id="1d1eb-2515">New-AzDiskConfig 및 New-AzSnapshotConfig에 HyperVGeneration 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2515">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="1d1eb-2516">다른 테넌트의 갤러리 이미지를 사용하여 VM을 만들 수 있음</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2516">Allow VM creation with galley image from other tenants.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="1d1eb-2517">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2517">Az.ContainerInstance</span></span>
* <span data-ttu-id="1d1eb-2518">후행 빈 인수를 추가한 New-AzContainerGroup의 -Command 매개 변수의 문제 수정</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2518">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="1d1eb-2519">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2519">Az.DataFactory</span></span>
* <span data-ttu-id="1d1eb-2520">ADF .Net SDK 버전을 3.0.2로 업데이트</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2520">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="1d1eb-2521">RepoConfiguration 관련 설정에 대한 추가 매개 변수로 Set-AzDataFactoryV2 cmdlet을 업데이트</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2521">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="1d1eb-2522">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2522">Az.Resources</span></span>
* <span data-ttu-id="1d1eb-2523">'-ResourceId' 또는 '-ResourceGroupName', '-Name' 및 '-ResourceType' 매개 변수를 제공할 때 'Get-AzResource'에 대한 공급자 처리 개선</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2523">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="1d1eb-2524">'Test-AzDeployment' 및 'Test-AzResourceGroupDeployment'에 대한 오류 처리 개선</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2524">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="1d1eb-2525">배포 유효성 검사 외부에서 발생한 오류를 처리하고 그 대신 명령의 출력에 포함</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2525">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="1d1eb-2526">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/6856 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2526">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="1d1eb-2527">배포 cmdlet 세트에 스크립트 및 작업 시나리오에서 프롬프트를 건너뛰는 '-IgnoreDynamicParameters' 스위치 추가</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2527">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="1d1eb-2528">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/6856 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2528">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="1d1eb-2529">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2529">Az.Sql</span></span>
* <span data-ttu-id="1d1eb-2530">데이터베이스 데이터 분류 지원</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2530">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="1d1eb-2531">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2531">Az.Storage</span></span>
* <span data-ttu-id="1d1eb-2532">매개 변수 -UseConnectedAccount를 사용하여 스토리지 컨텍스트를 만들 때 자세한 오류 보고(단, 로그인 Azure 계정 없이)</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2532">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="1d1eb-2533">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2533">New-AzStorageContext</span></span>
* <span data-ttu-id="1d1eb-2534">관리 평면 API를 사용하여 지정한 스토리지 계정의 BLOB 서비스 속성 관리 지원</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2534">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="1d1eb-2535">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2535">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="1d1eb-2536">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2536">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="1d1eb-2537">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2537">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="1d1eb-2538">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2538">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="1d1eb-2539">BLOB 및 파일 업로드/다운로드 cmdlet에 대한 -AsJob 지원</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2539">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="1d1eb-2540">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2540">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="1d1eb-2541">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2541">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="1d1eb-2542">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2542">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="1d1eb-2543">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2543">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="1d1eb-2544">1.6.0 - 2019년 3월</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2544">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="1d1eb-2545">마지막 주 릴리스 이후의 주요 사항</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2545">Highlights since the last major release</span></span>
* <span data-ttu-id="1d1eb-2546">`Az` 모듈 일반 공급</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2546">General availability of `Az` module</span></span>
* <span data-ttu-id="1d1eb-2547">`Az` 모듈에 대한 자세한 내용은 https://aka.ms/azps-announce 를 방문하세요.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2547">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="1d1eb-2548">Location, ResourceGroup 및 ResourceName 완성자가 추가되었습니다(https://azure.microsoft.com/blog/completers-in-azure-powershell/ ).</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2548">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="1d1eb-2549">와일드카드 지원이 Az.Compute 및 Az.Network에 대한 Get cmdlet에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2549">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="1d1eb-2550">Windows PowerShell 5.1 전용 대화형 사용자 이름/암호 인증이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2550">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="1d1eb-2551">Python 2 Runbook 지원이 Az.Automation에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2551">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="1d1eb-2552">Az.LogicApp: 통합 계정 어셈블리 및 일괄 처리 구성을 위한 새로운 cmdlet입니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2552">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="1d1eb-2553">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2553">Az.Automation</span></span>
* <span data-ttu-id="1d1eb-2554">Azure 자동화 업데이트 관리에서 변경된 지원 기능은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2554">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="1d1eb-2555">동적 그룹화</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2555">Dynamic grouping</span></span>
    * <span data-ttu-id="1d1eb-2556">사전 스크립트</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2556">Pre-Post script</span></span>
    * <span data-ttu-id="1d1eb-2557">다시 부팅 설정</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2557">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="1d1eb-2558">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2558">Az.Compute</span></span>
* <span data-ttu-id="1d1eb-2559">Get-AzVmBootDiagnosticsData의 경로 확인 문제가 해결되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2559">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="1d1eb-2560">Compute 클라이언트 라이브러리가 25.0.0으로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2560">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="1d1eb-2561">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2561">Az.KeyVault</span></span>
* <span data-ttu-id="1d1eb-2562">와일드카드 지원이 KeyVault cmdlet에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2562">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="1d1eb-2563">Az.Network</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2563">Az.Network</span></span>
* <span data-ttu-id="1d1eb-2564">Azure Firewall에 대한 위협 인텔리전스 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2564">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="1d1eb-2565">Application Gateway 방화벽 정책의 최상위 수준 리소스 및 사용자 지정 규칙이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2565">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="1d1eb-2566">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2566">Az.RecoveryServices</span></span>
* <span data-ttu-id="1d1eb-2567">인스턴트 RP를 지원하기 위해 SnapshotRetentionInDays가 Azure VM 정책에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2567">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="1d1eb-2568">컨테이너 등록을 취소하는 파이프 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2568">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="1d1eb-2569">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2569">Az.Resources</span></span>
* <span data-ttu-id="1d1eb-2570">Get-AzResource 및 Get-AzResourceGroup에 대한 와일드카드 지원을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2570">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="1d1eb-2571">ARM에 대한 일반 호출을 수행할 때 사용되는 자격 증명을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2571">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="1d1eb-2572">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2572">Az.Sql</span></span>
* <span data-ttu-id="1d1eb-2573">위협 탐지의 cmdlet 매개 변수(ExcludeDetectionType)가 DetectionType에서 string[]으로 변경되어 새 DetectionType이 추가되면 이후의 증명이 되고 자동 완성도 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2573">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="1d1eb-2574">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2574">Az.Storage</span></span>
* <span data-ttu-id="1d1eb-2575">스토리지 계정에 대한 관리 정책 가져오기/설정/제거를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2575">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="1d1eb-2576">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2576">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="1d1eb-2577">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2577">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="1d1eb-2578">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2578">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="1d1eb-2579">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2579">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="1d1eb-2580">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2580">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="1d1eb-2581">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2581">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="1d1eb-2582">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2582">Az.Websites</span></span>
* <span data-ttu-id="1d1eb-2583">'New-AzWebApp -IncludeSourceWebAppSlots'를 사용하여 모든 슬롯의 복제를 중단하는 ARM 템플릿 버그가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2583">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span>

## <a name="150---march-2019"></a><span data-ttu-id="1d1eb-2584">1.5.0 - 2019년 3월</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2584">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="1d1eb-2585">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2585">Az.Accounts</span></span>
* <span data-ttu-id="1d1eb-2586">'Register-AzModule' 명령을 추가하여 AutoRest 생성 cmdlet을 지원</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2586">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="1d1eb-2587">Connect-AzAccount 예제 업데이트</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2587">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="1d1eb-2588">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2588">Az.Automation</span></span>
* <span data-ttu-id="1d1eb-2589">몇몇 Azure Automation cmdlet에서 특정 월별 일정을 검색할 때 발생하는 문제 수정</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2589">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="1d1eb-2590">상위 20개 노드를 반환하도록 Get-AzAutomationDscNode를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2590">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="1d1eb-2591">이제 모든 노드 반환</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2591">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="1d1eb-2592">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2592">Az.Cdn</span></span>
* <span data-ttu-id="1d1eb-2593">사용자 지정 도메인 Https 사용/사용 안 함에 대한 새 Powershell cmdlet이 추가되었으며 기존의 것은 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2593">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="1d1eb-2594">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2594">Az.Compute</span></span>
* <span data-ttu-id="1d1eb-2595">Get cmdlet에 와일드 카드 지원 추가</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2595">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="1d1eb-2596">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2596">Az.DataFactory</span></span>
* <span data-ttu-id="1d1eb-2597">ADF.Net SDK 버전이 3.0.1로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2597">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="1d1eb-2598">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2598">Az.LogicApp</span></span>
* <span data-ttu-id="1d1eb-2599">첫 결과 페이지 검색 시에만 ListWorkflows 수정</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2599">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="1d1eb-2600">Az.Network</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2600">Az.Network</span></span>
* <span data-ttu-id="1d1eb-2601">Network cmdlet에 와일드 카드 지원 추가</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2601">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="1d1eb-2602">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2602">Az.RecoveryServices</span></span>
* <span data-ttu-id="1d1eb-2603">Azure VM 지원에 SQL 서버가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2603">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="1d1eb-2604">SDK 업데이트</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2604">SDK Update</span></span>
* <span data-ttu-id="1d1eb-2605">VMappContainer 체크 인 Get-ProtectableItem 제거</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2605">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="1d1eb-2606">Get ProtectableItem의 매개 변수로 Name과 ServerName이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2606">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="1d1eb-2607">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2607">Az.Resources</span></span>
* <span data-ttu-id="1d1eb-2608">`-TemplateObject` 매개 변수를 추가하여 cmdlet을 배포</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2608">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="1d1eb-2609">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/2933 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2609">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="1d1eb-2610">`Get-AzResource`의 결과를 `Set-AzResource`(으)로 파이프할 때 발생하는 문제 수정</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2610">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="1d1eb-2611">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/8240 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2611">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="1d1eb-2612">실행 시 JSON 데이터 형식 문제 해결 `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2612">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="1d1eb-2613">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/7930 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2613">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="1d1eb-2614">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2614">Az.Sql</span></span>
* <span data-ttu-id="1d1eb-2615">AuditingEndpointsCommunicator를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2615">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="1d1eb-2616">새 진단 설정을 생성할 때 에지 사례의 동작을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2616">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="1d1eb-2617">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2617">Az.Storage</span></span>
* <span data-ttu-id="1d1eb-2618">스토리지 계정      - New-AzStorageAccount를 생성할 때 종류 BlockBlobStorage를 지원</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2618">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="1d1eb-2619">1.4.0 - 2019년 2월</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2619">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="1d1eb-2620">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2620">Az.AnalysisServices</span></span>
* <span data-ttu-id="1d1eb-2621">사용되지 않는 AddAzureASAccount cmdlet</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2621">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="1d1eb-2622">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2622">Az.Automation</span></span>
* <span data-ttu-id="1d1eb-2623">Import-AzAutomationDscNodeConfiguration 도움말 업데이트</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2623">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="1d1eb-2624">Import-AzAutomationDscConfiguration cmdlet 구성 이름 유효성 검사 추가</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2624">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="1d1eb-2625">Import-AzAutomationDscConfiguration cmdlet 오류 처리 개선</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2625">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="1d1eb-2626">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2626">Az.CognitiveServices</span></span>
* <span data-ttu-id="1d1eb-2627">리소스의 하위 도메인을 지정하는 데 사용되는 New-AzCognitiveServicesAccount에 대한 새 선택적 매개 변수로 CustomSubdomainName이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2627">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="1d1eb-2628">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2628">Az.Compute</span></span>
* <span data-ttu-id="1d1eb-2629">ID 매개 변수 집합 문제 해결</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2629">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="1d1eb-2630">Name 매개 변수를 제공하지 않으면 Get-AzVMExtension이 설치된 모든 확장을 열거하도록 업데이트</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2630">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="1d1eb-2631">Update-AzImage cmdlet에 태그 및 ResourceId 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2631">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="1d1eb-2632">인스턴스 ID가 없는 Get-AzVmssVM과 InstanceView를 사용하면 인스턴스 보기가 있는 VMSS VM을 나열할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2632">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="1d1eb-2633">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2633">Az.DataLakeStore</span></span>
* <span data-ttu-id="1d1eb-2634">ADL 삭제된 항목 열거 및 복원에 대한 cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2634">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="1d1eb-2635">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2635">Az.EventHub</span></span>
* <span data-ttu-id="1d1eb-2636">Eventhub의 CaptureDescription 클래스에서 빈 보관을 건너뛰는 새 부울 속성 SkipEmptyArchives가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2636">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="1d1eb-2637">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2637">Az.KeyVault</span></span>
* <span data-ttu-id="1d1eb-2638">Set-AzKeyVaultSecret 태그 지정 수정</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2638">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="1d1eb-2639">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2639">Az.LogicApp</span></span>
* <span data-ttu-id="1d1eb-2640">통합 계정에 대한 기본 sku 추가</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2640">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="1d1eb-2641">XSLT 2.0, XSLT 3.0, Liquid 맵 형식 추가</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2641">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="1d1eb-2642">통합 계정 어셈블리에 대한 새 cmdlet</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2642">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="1d1eb-2643">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2643">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="1d1eb-2644">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2644">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="1d1eb-2645">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2645">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="1d1eb-2646">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2646">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="1d1eb-2647">통합 계정 일괄 처리 구성에 대한 새 cmdlet</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2647">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="1d1eb-2648">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2648">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="1d1eb-2649">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2649">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="1d1eb-2650">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2650">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="1d1eb-2651">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2651">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="1d1eb-2652">논리 앱 SDK를 버전 4.1.0으로 업데이트</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2652">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="1d1eb-2653">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2653">Az.Monitor</span></span>
* <span data-ttu-id="1d1eb-2654">Get-AzMetric에 대한 도움말 업데이트</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2654">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="1d1eb-2655">Az.Network</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2655">Az.Network</span></span>
* <span data-ttu-id="1d1eb-2656">Add-AzApplicationGatewayCustomError에 대한 도움말 예제 업데이트</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2656">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="1d1eb-2657">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2657">Az.OperationalInsights</span></span>
* <span data-ttu-id="1d1eb-2658">New 및 Get ApplicationInsights 데이터 소스에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2658">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="1d1eb-2659">지정된 작업 영역에 대한 특정 또는 전체 ApplicationInsights 데이터 원본 가져오기를 지원하기 위한 새로운 'ApplicationInsights' 종류가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2659">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span>
    - <span data-ttu-id="1d1eb-2660">지정된 Application-Insights 리소스 매개 변수(구독 ID, resourceGroupName 및 이름)별로 데이터 원본을 만들기 위한 New-AzOperationalInsightsApplicationInsightsDataSource cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2660">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span>

#### <a name="azresources"></a><span data-ttu-id="1d1eb-2661">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2661">Az.Resources</span></span>
* <span data-ttu-id="1d1eb-2662">문제 https://github.com/Azure/azure-powershell/issues/8166 수정</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2662">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="1d1eb-2663">문제 https://github.com/Azure/azure-powershell/issues/8235 수정</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2663">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="1d1eb-2664">문제 https://github.com/Azure/azure-powershell/issues/6219 수정</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2664">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="1d1eb-2665">KeyCredentials 반복 만들기를 방지하기 위해 버그 수정</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2665">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="1d1eb-2666">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2666">Az.Sql</span></span>
* <span data-ttu-id="1d1eb-2667">SQL DB 하이퍼스케일에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2667">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="1d1eb-2668">복원 요청에서 불필요한 속성을 설정하여 복원이 실패할 수 있는 버그 수정</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2668">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="1d1eb-2669">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2669">Az.Websites</span></span>
* <span data-ttu-id="1d1eb-2670">Get-AzWebAppSlotMetrics 내 올바른 예제</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2670">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="1d1eb-2671">1.3.0 - 2019년 2월</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2671">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="1d1eb-2672">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2672">Az.Accounts</span></span>
* <span data-ttu-id="1d1eb-2673">ClientRuntime 최신 버전 업데이트</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2673">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="1d1eb-2674">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2674">Az.AnalysisServices</span></span>
<span data-ttu-id="1d1eb-2675">Az.AnalysisServices 모듈의 전반적인 가용성.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2675">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="1d1eb-2676">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2676">Az.Compute</span></span>
* <span data-ttu-id="1d1eb-2677">AEM 확장: UltraSSD 및 P60, P70, P80 디스크에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2677">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="1d1eb-2678">Set-AzVMBootDiagnostics에 대한 도움말 업데이트</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2678">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="1d1eb-2679">Update-AzImage에 대한 도움말 및 예제 업데이트</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2679">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="1d1eb-2680">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2680">Az.RecoveryServices</span></span>
<span data-ttu-id="1d1eb-2681">Az.RecoveryServices 모듈의 전반적인 가용성.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2681">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="1d1eb-2682">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2682">Az.Resources</span></span>
* <span data-ttu-id="1d1eb-2683">리소스 그룹 관련 태그 수정</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2683">Fix tagging for resource groups</span></span>
    - <span data-ttu-id="1d1eb-2684">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/8166 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2684">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="1d1eb-2685">`Get-AzureRmRoleAssignment`이(가) -ErrorAction을 준수하지 않는 문제 수정</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2685">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span>
    - <span data-ttu-id="1d1eb-2686">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/8235 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2686">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="1d1eb-2687">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2687">Az.Sql</span></span>
* <span data-ttu-id="1d1eb-2688">AzSqlDatabaseBackupShortTermRetentionPolicy 가져오기/설정하기 추가</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2688">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="1d1eb-2689">SQL cmdlet을 실행할 경우 Azure 계정에 로그인되어 있지 않은 것이 nullref 예외를 초래하는 문제 수정</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2689">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="1d1eb-2690">Get-AzSqlCapability의 nullref 예외 수정</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2690">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="1d1eb-2691">1.2.1 - 2019년 1월</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2691">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="1d1eb-2692">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2692">Az.Accounts</span></span>
* <span data-ttu-id="1d1eb-2693">올바른 인증 버전을 사용하여 릴리스</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2693">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="1d1eb-2694">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2694">Az.AnalysisServices</span></span>
* <span data-ttu-id="1d1eb-2695">업데이트된 인증 종속성을 사용하여 릴리스</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2695">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="1d1eb-2696">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2696">Az.RecoveryServices</span></span>
* <span data-ttu-id="1d1eb-2697">업데이트된 인증 종속성을 사용하여 릴리스</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2697">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="1d1eb-2698">1.2.0 - 2019년 1월</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2698">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="1d1eb-2699">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2699">Az.Accounts</span></span>
* <span data-ttu-id="1d1eb-2700">Windows PowerShell 5.1 전용 대화형 사용자 이름/암호 인증 추가</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2700">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="1d1eb-2701">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2701">Update incorrect online help URLs</span></span>
* <span data-ttu-id="1d1eb-2702">Uninstall-AzureRm 관련 PS Core에 경고 메시지 추가</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2702">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="1d1eb-2703">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2703">Az.Aks</span></span>
* <span data-ttu-id="1d1eb-2704">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2704">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="1d1eb-2705">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2705">Az.Automation</span></span>
* <span data-ttu-id="1d1eb-2706">Python 2 Runbook에 대한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2706">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="1d1eb-2707">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2707">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="1d1eb-2708">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2708">Az.Cdn</span></span>
* <span data-ttu-id="1d1eb-2709">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2709">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="1d1eb-2710">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2710">Az.Compute</span></span>
* <span data-ttu-id="1d1eb-2711">Invoke-AzVMReimage cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2711">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="1d1eb-2712">Set-AzVmss에 TempDisk 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2712">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="1d1eb-2713">New-AzVM 경고 메시지 수정</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2713">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="1d1eb-2714">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2714">Az.ContainerRegistry</span></span>
* <span data-ttu-id="1d1eb-2715">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2715">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="1d1eb-2716">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2716">Az.DataFactory</span></span>
* <span data-ttu-id="1d1eb-2717">ADF.Net SDK 버전이 3.0.0으로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2717">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="1d1eb-2718">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2718">Az.DataLakeStore</span></span>
* <span data-ttu-id="1d1eb-2719">MSI를 사용할 때 ADLS 엔드포인트 문제 수정</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2719">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="1d1eb-2720">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/7462 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2720">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="1d1eb-2721">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2721">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="1d1eb-2722">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2722">Az.IotHub</span></span>
* <span data-ttu-id="1d1eb-2723">Add-IotHubRoutingEndpoint cmdlet에 인코딩 형식을 추가하세요.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2723">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="1d1eb-2724">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2724">Az.KeyVault</span></span>
* <span data-ttu-id="1d1eb-2725">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2725">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="1d1eb-2726">Az.Network</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2726">Az.Network</span></span>
* <span data-ttu-id="1d1eb-2727">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2727">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="1d1eb-2728">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2728">Az.Resources</span></span>
* <span data-ttu-id="1d1eb-2729">'New-AzADAppCredential' 및 'New-AzADSpCredential' 참조 설명서의 잘못된 예제 수정</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2729">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="1d1eb-2730">리소스 그룹 배포 cmdlet 실행 전 '-TemplateFile' 매개 변수 경로가 확인되지 않는 문제 수정</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2730">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="1d1eb-2731">Az.Resources: New-AzureRmPolicyDefinition -Mode 기본값에 대한 올바른 설명서</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2731">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="1d1eb-2732">Az.Resources: 문제 https://github.com/Azure/azure-powershell/issues/7522 수정</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2732">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="1d1eb-2733">Az.Resources: 문제 https://github.com/Azure/azure-powershell/issues/5747 수정</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2733">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="1d1eb-2734">'PSResourceGroupDeployment' 개체의 서식 문제 수정</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2734">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="1d1eb-2735">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/2123 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2735">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="1d1eb-2736">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2736">Az.ServiceFabric</span></span>
* <span data-ttu-id="1d1eb-2737">인증서가 VMSS 모델에 추가되었는데도 예외가 발생할 경우 롤백합니다. 이는 버그 https://github.com/Azure/service-fabric-issues/issues/932 를 수정하기 위함입니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2737">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="1d1eb-2738">일부 오류 메시지를 수정하세요.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2738">Fix some error messages.</span></span>
* <span data-ttu-id="1d1eb-2739">Az로의 마이그레이션을 통해서는 작동하지 않는 New-AzServiceFabriCluster를 위해 기본값 ARM 템플릿을 가진 클러스터 만들기를 수정하세요.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2739">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="1d1eb-2740">확장에서 클러스터 id를 확인하여 클러스터에 해당하는 VMSS에만 추가되도록 클러스터/애플리케이션 인증서 추가를 수정하세요.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2740">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="1d1eb-2741">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2741">Az.SignalR</span></span>
* <span data-ttu-id="1d1eb-2742">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2742">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="1d1eb-2743">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2743">Az.Sql</span></span>
* <span data-ttu-id="1d1eb-2744">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2744">Update incorrect online help URLs</span></span>
* <span data-ttu-id="1d1eb-2745">가능한 값을 가진 LicenseType 매개 변수에 대한 매개 변수 설명이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2745">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="1d1eb-2746">유일하게 업데이트된 속성인데 작동하지 않는 관리되는 인스턴스 ID의 업데이트 수정</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2746">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="1d1eb-2747">관리되는 인스턴스에서의 사용자 지정 데이터 정렬에 대한 지원</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2747">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="1d1eb-2748">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2748">Az.Storage</span></span>
* <span data-ttu-id="1d1eb-2749">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2749">Update incorrect online help URLs</span></span>
* <span data-ttu-id="1d1eb-2750">Premium Storage 계정이 클래식 로깅/메트릭을 지원하지 않기 때문에, Premium Storage 계정의 클래식 로깅/메트릭을 가져올/설정할 때 상세한 오류 메시지를 제공해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2750">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="1d1eb-2751">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2751">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="1d1eb-2752">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2752">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="1d1eb-2753">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2753">Az.TrafficManager</span></span>
* <span data-ttu-id="1d1eb-2754">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2754">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="1d1eb-2755">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2755">Az.Websites</span></span>
* <span data-ttu-id="1d1eb-2756">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2756">Update incorrect online help URLs</span></span>
* <span data-ttu-id="1d1eb-2757">앱이 ASE에 호스팅되면 'New-AzWebAppSSLBinding'을 수정하여 올바른 resourcegroup+location에 인증서를 업로드합니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2757">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="1d1eb-2758">'New-AzWebAppSSLBinding'을 수정하여 SSL 인증서를 앱에 바인딩하는 데 붙는 태그를 덮어쓰지 않도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2758">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="1d1eb-2759">1.1.0 - 2019년 1월</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2759">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="1d1eb-2760">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2760">Az.Accounts</span></span>
* <span data-ttu-id="1d1eb-2761">Enable-AzureRmAlias에 'Local' 범위 추가</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2761">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="1d1eb-2762">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2762">Az.Compute</span></span>
* <span data-ttu-id="1d1eb-2763">이름이 Restart/Start/Stop/Remove/Set-AzVM과 Save-AzVMImage에 설정된 ID 매개 변수에서 선택 사항이 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2763">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="1d1eb-2764">도움말 파일의 ID에 대한 설명이 업데이트 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2764">Updated the description of ID in help files</span></span>
* <span data-ttu-id="1d1eb-2765">Az.Accounts 모듈을 사용할 때의 이전 버전과의 호환성 문제를 해결합니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2765">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="1d1eb-2766">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2766">Az.DataLakeStore</span></span>
* <span data-ttu-id="1d1eb-2767">SDK 수정을 위해 데이터 평면의 SDK 버전을 1.1.14로 업데이트하세요.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2767">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="1d1eb-2768">getfilestatus 및 liststatus에 대한 음수 acesstime 및 modificationtime 수정, 비동기 취소 토큰 수정</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2768">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="1d1eb-2769">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2769">Az.EventGrid</span></span>
* <span data-ttu-id="1d1eb-2770">2019-01-01 API 버전을 사용하도록 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2770">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="1d1eb-2771">2019-01-01 API 버전에서 새 시나리오를 지원하도록 다음 cmdlet을 업데이트</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2771">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="1d1eb-2772">New-AzureRmEventGridSubscription: 지정을 위한 새로운 선택적 매개 변수를 추가</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2772">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="1d1eb-2773">이벤트 Time-to-Live</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2773">Event Time-To-Live,</span></span>
        - <span data-ttu-id="1d1eb-2774">이벤트에 대한 최대 배달 시도</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2774">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="1d1eb-2775">배달 못한 편지의 엔드포인트입니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2775">Dead letter endpoint.</span></span>
    - <span data-ttu-id="1d1eb-2776">Update-AzureRmEventGridSubscription: 지정을 위한 새로운 선택적 매개 변수를 추가</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2776">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="1d1eb-2777">이벤트 Time-to-Live</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2777">Event Time-To-Live,</span></span>
        - <span data-ttu-id="1d1eb-2778">이벤트에 대한 최대 배달 시도</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2778">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="1d1eb-2779">배달 못한 편지의 엔드포인트입니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2779">Dead letter endpoint.</span></span>
* <span data-ttu-id="1d1eb-2780">New-AzureRmEventGridSubscription 및 Update-AzureRmEventGridSubscription cmdlet의 EndpointType 옵션에 새 열거형 값(즉, storageQueue 및 hybridConnection)을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2780">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="1d1eb-2781">이벤트 구독을 생성 또는 업데이트할 때 사용자가 직접 조치를 취해야 할 경우 경고 메시지를 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2781">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="1d1eb-2782">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2782">Az.IotHub</span></span>
* <span data-ttu-id="1d1eb-2783">최신 버전의 Azure IotHub SDK로 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2783">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="1d1eb-2784">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2784">Az.LogicApp</span></span>
* <span data-ttu-id="1d1eb-2785">지정된 이름이 없는 모든 Get-AzLogicApp 목록</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2785">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="1d1eb-2786">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2786">Az.Resources</span></span>
* <span data-ttu-id="1d1eb-2787">'Get-AzResource'에 '-ODataQuery'및 '-ResourceId' 매개 변수를 제공할 때 매개 변수 집합 문제 수정</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2787">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="1d1eb-2788">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/7875 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2788">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="1d1eb-2789">New/Set-AzPolicyDefinition에서 -Custom 매개 변수 처리 문제 수정</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2789">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="1d1eb-2790">New-AzDeployment 설명서에서 오타 수정</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2790">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="1d1eb-2791">'New-AzADUser'에 '-MailNickname'매개 변수가 필수 항목으로 지정됨</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2791">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="1d1eb-2792">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/8220 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2792">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="1d1eb-2793">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2793">Az.SignalR</span></span>
* <span data-ttu-id="1d1eb-2794">Az.Accounts 모듈을 사용할 때의 이전 버전과의 호환성 문제를 해결합니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2794">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="1d1eb-2795">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2795">Az.Sql</span></span>
* <span data-ttu-id="1d1eb-2796">Storage 관리 클라이언트 종속성을 일반적인 SDK 구현으로 변환했습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2796">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="1d1eb-2797">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2797">Az.Storage</span></span>
* <span data-ttu-id="1d1eb-2798">Sas Token, OAuth 또는 Anonymous를 사용하여 스토리지 컨텍스트의 StorageAccountName을 실제 스토리지 계정 이름으로 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2798">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="1d1eb-2799">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2799">New-AzStorageContext</span></span>
* <span data-ttu-id="1d1eb-2800">'-FullUri' 매개 변수를 사용하여 Blob 스냅샷 개체의 Sas Token을 생성하고 반환된 Uri를 스냅샷 Uri로 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2800">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="1d1eb-2801">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2801">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="1d1eb-2802">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2802">Az.Websites</span></span>
* <span data-ttu-id="1d1eb-2803">'Get-AzDeletedWebApp'의 날짜 구문 분석 버그를 수정했습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2803">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="1d1eb-2804">Az.Accounts 모듈을 사용할 때의 이전 버전과의 호환성 문제를 해결합니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2804">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="1d1eb-2805">1.0.0 - 2018년 12월</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2805">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="1d1eb-2806">일반</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2806">General</span></span>

- <span data-ttu-id="1d1eb-2807">Az 모듈 일반 공급</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2807">General Availability of Az Module</span></span>
- <span data-ttu-id="1d1eb-2808">각 모듈에 대 한 온라인 도움말</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2808">Online help for each module</span></span>
- <span data-ttu-id="1d1eb-2809">자세한 내용과 로드맵은 [Az 알림 페이지](https://aka.ms/azps-announce)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2809">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="1d1eb-2810">AzureRM에서 마이그레이션하는 것에 대한 정보는 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2810">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="1d1eb-2811">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2811">Az.Accounts</span></span>
- <span data-ttu-id="1d1eb-2812">Az.Profile에서 변경</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2812">Changed from Az.Profile</span></span>
- <span data-ttu-id="1d1eb-2813">프로필 및 컨텍스트 형식에 대한 표 형식 수정</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2813">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="1d1eb-2814">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2814">Az.ApiManagement</span></span>
- <span data-ttu-id="1d1eb-2815">#7002에 대한 수정</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2815">Fixes for #7002</span></span>
- <span data-ttu-id="1d1eb-2816">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2816">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="1d1eb-2817">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2817">Az.Batch</span></span>
- <span data-ttu-id="1d1eb-2818">`PSComputeNode`의 새로운 `NodeAgentInformation` 속성을 통해 풀의 각 VM에서 실행 중인 Azure Batch 노드 에이전트의 버전을 확인하는 기능이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2818">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="1d1eb-2819">`PSDataDisk`에 대한 `Caching` 기본 값은 이제 `None` 대신 `ReadWrite`입니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2819">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="1d1eb-2820">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2820">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="1d1eb-2821">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2821">Az.Billing</span></span>
- <span data-ttu-id="1d1eb-2822">청구, 소비 및 UsageAggregates cmdlet 결합 cmdlet에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2822">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="1d1eb-2823">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2823">Az.CognitivServices</span></span>
- <span data-ttu-id="1d1eb-2824">New-AzureRmCognitiveServicesAccount 작업에서 사용 가능한 SkuName 및 Typem에 대한 완성자 추가</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2824">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="1d1eb-2825">Get-AzCognitiveServicesAccountSkus에서 GetSkusWithAccountParamSetName 매개 변수 집합을 제거</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2825">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="1d1eb-2826">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2826">Az.ContainerInstance</span></span>
- <span data-ttu-id="1d1eb-2827">ManagedIdentity 지원이 추가됨</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2827">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="1d1eb-2828">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2828">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="1d1eb-2829">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2829">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="1d1eb-2830">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2830">Az.DataLakeStore</span></span>
- <span data-ttu-id="1d1eb-2831">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2831">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="1d1eb-2832">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2832">Az.Monitor</span></span>
- <span data-ttu-id="1d1eb-2833">Az.Monitor 이름 변경 및 기타 사소한 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2833">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="1d1eb-2834">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2834">Az.KeyVault</span></span>
- <span data-ttu-id="1d1eb-2835">출력 형식에서 사용되지 않는 'PurgeDisabled' 속성 제거</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2835">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="1d1eb-2836">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2836">Az.MachineLearning</span></span>
- <span data-ttu-id="1d1eb-2837">Az.MachineLearningCompute 모듈의 cmdlet 포함</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2837">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="1d1eb-2838">Az.Media</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2838">Az.Media</span></span>
- <span data-ttu-id="1d1eb-2839">New-AzMediaService에서 사용되지 않는 -Tags 별칭이 제거됨</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2839">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="1d1eb-2840">Az.Network</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2840">Az.Network</span></span>
<span data-ttu-id="1d1eb-2841">Application Gateway에서 RewriteRuleSets를 구성하는 것에 대한 지원이 추가됨</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2841">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="1d1eb-2842">추가된 새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2842">New cmdlets added:</span></span>
        - <span data-ttu-id="1d1eb-2843">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2843">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="1d1eb-2844">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2844">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="1d1eb-2845">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2845">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="1d1eb-2846">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2846">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="1d1eb-2847">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2847">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="1d1eb-2848">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2848">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="1d1eb-2849">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2849">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="1d1eb-2850">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2850">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="1d1eb-2851">선택적 매개 변수를 사용하도록 cmdlet이 업데이트됨 -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2851">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="1d1eb-2852">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2852">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="1d1eb-2853">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2853">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="1d1eb-2854">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2854">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="1d1eb-2855">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2855">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="1d1eb-2856">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2856">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="1d1eb-2857">New-AzureRmApplicationGatewayUrlPathMapConfig로 ID를 사용하여 Application Gateway에 KeyVault 지원을 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2857">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="1d1eb-2858">선택적 매개 변수를 사용하도록 cmdlet이 업데이트됨 -KeyVaultSecretId, -KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2858">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="1d1eb-2859">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2859">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="1d1eb-2860">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2860">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="1d1eb-2861">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2861">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="1d1eb-2862">New-AzApplicationGateway cmdlet이 선택적 매개 변수를 사용하도록 업데이트됨 -UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2862">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="1d1eb-2863">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2863">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="1d1eb-2864">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2864">Az.OperationalInsights</span></span>
- <span data-ttu-id="1d1eb-2865">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2865">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="1d1eb-2866">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2866">Az.Profile</span></span>
- <span data-ttu-id="1d1eb-2867">Az.Accounts에 모듈 이름이 변경됨</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2867">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="1d1eb-2868">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2868">Az.RecoveryServices</span></span>
- <span data-ttu-id="1d1eb-2869">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2869">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="1d1eb-2870">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2870">Az.Resources</span></span>
- <span data-ttu-id="1d1eb-2871">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2871">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="1d1eb-2872">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2872">Az.ServiceFabric</span></span>
- <span data-ttu-id="1d1eb-2873">일반 이름과 지문으로 지정 인증서 지원</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2873">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="1d1eb-2874">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2874">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="1d1eb-2875">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2875">Az.SIgnalR</span></span>
- <span data-ttu-id="1d1eb-2876">SIgnalR에 대한 PowerShell cmdlet에 대한 일반 공급</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2876">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="1d1eb-2877">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2877">Az.Sql</span></span>
- <span data-ttu-id="1d1eb-2878">위협 탐지의 cmdlet에 새로운 Data_Exfiltration 및 Unsafe_Action 검색 유형 추가</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2878">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="1d1eb-2879">Sql 감사 cmdlet에 대한 설명서 예제 업데이트</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2879">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="1d1eb-2880">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2880">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="1d1eb-2881">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2881">Az.Storage</span></span>
- <span data-ttu-id="1d1eb-2882">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2882">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="1d1eb-2883">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2883">Az.Websites</span></span>
- <span data-ttu-id="1d1eb-2884">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2884">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="1d1eb-2885">0.7.0 - 2018년 12월</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2885">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="1d1eb-2886">일반</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2886">General</span></span>

* <span data-ttu-id="1d1eb-2887">AzureRM에서 Az 전환 예정에 대한 사소한 변경</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2887">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="1d1eb-2888">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2888">Az.Compute</span></span>

* <span data-ttu-id="1d1eb-2889">`New-AzVm(ss)` cmdlet에 대한 간단한 매개 변수 집합에 UltraSSD 및 갤러리 이미지에 대한 지원을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2889">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="1d1eb-2890">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2890">Az.DataLakeStore</span></span>

* <span data-ttu-id="1d1eb-2891">ADLS 계정의 도메인의 후행 슬래시를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2891">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="1d1eb-2892">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2892">Az.FrontDoor</span></span>

* <span data-ttu-id="1d1eb-2893">일부 끊어진 링크 수정</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2893">Fixed some broken links</span></span>
    - <span data-ttu-id="1d1eb-2894">New-AzureRmFrontDoor 및 Set-AzureRmFrontDoor 아티클에서 New-AzureRmFrontDoorHealthProbeSettingObject cmdlet 아티클에 대한 링크가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2894">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="1d1eb-2895">New-AzureRmFrontDoorManagedRuleObject 아티클에서 New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet 아티클에 대한 링크가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2895">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="1d1eb-2896">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2896">Az.RecoveryServices</span></span>

* <span data-ttu-id="1d1eb-2897">Azure File Share 복원 작업에 클라이언트 측 유효성 검사가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2897">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="1d1eb-2898">afs 복원의 경우 storageAccountName 및 storageAccountResourceGroupName을 선택적으로 만들었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2898">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="1d1eb-2899">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2899">Az.Resources</span></span>

* <span data-ttu-id="1d1eb-2900"> https://github.com/Azure/azure-powershell/issues/7679 에 대한 수정</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2900">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="1d1eb-2901">기본 관리자를 요청할 때 구독 범위가 제공되는 경우 Get-AzureRmRoleAssignment를 업데이트하여 구독 범위를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2901">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="1d1eb-2902">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2902">Az.Sql</span></span>

* <span data-ttu-id="1d1eb-2903">AzureRM에서 Az 전환 예정에 대한 사소한 변경</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2903">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="1d1eb-2904">DotNet 코어에서 Get-AzureRmSqlDatabaseVulnerabilityAssessment를 사용하는 문제 해결</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2904">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="1d1eb-2905">SQL 감사 cmdlet과 관련된 도움말 메시지의 설명서가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2905">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="1d1eb-2906">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2906">Az.Storage</span></span>

* <span data-ttu-id="1d1eb-2907">New-AzureRmStorageAccount에 -EnableHierarchicalNamespace 추가</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2907">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="1d1eb-2908">파일 복사 cmdlet이 -DestContext 입력이 없을 때 대상의 원본 컨텍스트를 다시 사용할 수 없는 문제 수정</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2908">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="1d1eb-2909">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2909">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="1d1eb-2910">고정적인 웹 사이트 구성 지원</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2910">Support Static Website configuration</span></span>
    - <span data-ttu-id="1d1eb-2911">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2911">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="1d1eb-2912">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2912">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="1d1eb-2913">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2913">Az.Websites</span></span>

* <span data-ttu-id="1d1eb-2914">Set-AzureRmWebApp 및 Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2914">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span>
    - <span data-ttu-id="1d1eb-2915">Windows 및 Linux 컨테이너 응용 프로그램에 탑재할 Azure Storage 경로를 지정하기 위해 새 매개 변수(-AzureStoragePath)가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2915">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="1d1eb-2916">새 cmdlet New-AzureRmWebAppAzureStoragePath의 출력을 매개 변수로 사용하여 Azure Storage 경로를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2916">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="1d1eb-2917">0.6.1 - 2018년 11월</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2917">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="1d1eb-2918">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2918">Az.ApiManagement</span></span>
* <span data-ttu-id="1d1eb-2919">형식 매핑 문제에 대한 종속성 업데이트</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2919">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="1d1eb-2920">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2920">Az.Automation</span></span>
* <span data-ttu-id="1d1eb-2921">Azure Automation cmdlet 기반 Swagger</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2921">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="1d1eb-2922">업데이트 관리 cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2922">Added Update Management cmdlets</span></span>
* <span data-ttu-id="1d1eb-2923">소스 제어 cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2923">Added Source Control cmdlets</span></span>
* <span data-ttu-id="1d1eb-2924">Remove-AzureRmAutomationHybridWorkerGroup cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2924">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="1d1eb-2925">DSC 노드 등록 명령 수정</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2925">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="1d1eb-2926">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2926">Az.Compute</span></span>
* <span data-ttu-id="1d1eb-2927">SystemAssigned ID에 대한 ID 문제 수정</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2927">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="1d1eb-2928">형식 매핑 문제에 대한 종속성 업데이트</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2928">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="1d1eb-2929">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2929">Az.ContainerInstance</span></span>
* <span data-ttu-id="1d1eb-2930">형식 매핑 문제에 대한 종속성 업데이트</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2930">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="1d1eb-2931">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2931">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="1d1eb-2932">마켓플레이스 cmdlet에 대한 예제 설명 업데이트</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2932">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="1d1eb-2933">Az.Network</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2933">Az.Network</span></span>
* <span data-ttu-id="1d1eb-2934">New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2934">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="1d1eb-2935">지원되는 AzureFirewall 네트워크 프로토콜에 ICMP 다시 추가</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2935">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="1d1eb-2936">Test-AzureRmNetworkWatcherConnectivity cmdlet을 업데이트하여 대상 ID, 주소 및 포트 유효성 검사를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2936">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span>
* <span data-ttu-id="1d1eb-2937">VirtualNetwork 맵의 메모리 사용 문제 해결</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2937">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="1d1eb-2938">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2938">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="1d1eb-2939">보호된 파일 공유에 대한 정책을 수정하는 것에 대해 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2939">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="1d1eb-2940">정책 표준 시간대를 대문자로 변환했습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2940">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="1d1eb-2941">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2941">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="1d1eb-2942">New-AzureRmRecoveryServicesAsrProtectableItem의 예제 정정</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2942">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="1d1eb-2943">형식 매핑 문제에 대한 종속성 업데이트</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2943">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="1d1eb-2944">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2944">Az.Relay</span></span>
* <span data-ttu-id="1d1eb-2945">선택적 매개 변수 -KeyValue를 New-AzureRmRelayKey cmdlet에 추가하여 사용자가 KeyValue를 제공할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2945">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="1d1eb-2946">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2946">Az.Resources</span></span>
* <span data-ttu-id="1d1eb-2947">`New-AzureRmPolicyAssignment` 및 `Set-AzureRmPolicyAssignment`의 자원 ID 관련 매개 변수에 대한 도움말 문서를 업데이트함</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2947">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="1d1eb-2948">-Metadata를 사용하는 New-AzureRmPolicyDefinition에 대한 예제 추가</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2948">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="1d1eb-2949">NetStandard의 태그 키에서 대소문자 보존을 허용하도록 수정: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2949">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="1d1eb-2950">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2950">Az.ServiceFabric</span></span>
* <span data-ttu-id="1d1eb-2951">향후 호환성이 손상되는 변경에 대한 사용 중단 메시지 추가</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2951">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="1d1eb-2952">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2952">Az.Sql</span></span>
* <span data-ttu-id="1d1eb-2953">Azure Sql Database Managed Instance 및 Azure Sql Managed Database에 CRUD 작업을 위한 새 cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2953">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="1d1eb-2954">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2954">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="1d1eb-2955">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2955">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="1d1eb-2956">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2956">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="1d1eb-2957">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2957">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="1d1eb-2958">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2958">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="1d1eb-2959">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2959">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="1d1eb-2960">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2960">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="1d1eb-2961">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2961">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="1d1eb-2962">서버 또는 데이터베이스에서 확장 감사 정책 관리를 활성화했습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2962">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="1d1eb-2963">새 매개 변수(PredicateExpression)가 감사 로그 필터링을 사용하도록 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2963">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="1d1eb-2964">Cmdlet이 레거시 클라이언트 대신 SQL 클라이언트를 사용하도록 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2964">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="1d1eb-2965">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2965">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="1d1eb-2966">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2966">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="1d1eb-2967">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2967">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="1d1eb-2968">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2968">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="1d1eb-2969">스토리지 계정 이름 매개 변수가 설정된 Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings를 사용할 때의 문제 해결</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2969">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="1d1eb-2970">0.5.0 - 2018년 11월</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2970">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="1d1eb-2971">일반</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2971">General</span></span>
* <span data-ttu-id="1d1eb-2972">많은 핵심 cmdlet에 Resource Completers를 추가하여 대화형으로 cmdlet을 호출할 때 기존 리소스 이름을 탭으로 이동할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2972">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="1d1eb-2973">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2973">Az.Profile</span></span>
* <span data-ttu-id="1d1eb-2974">ClientRuntime의 최신 버전을 사용하도록 일반적인 코드를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2974">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="1d1eb-2975">Connect-AzAccount cmdlet의 매개 변수 TenantId 이름을 Tenant로 바꾸고 TenantId의 별칭을 추가합니다</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2975">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="1d1eb-2976">Connect-AzAccount의 업데이트된 TenantId 설명</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2976">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="1d1eb-2977">테넌트 도메인을 제공할 때 실패한 로그인에 대한 오류 메시지 수정</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2977">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="1d1eb-2978">테넌트에 구독이 없는 계정의 컨텍스트 이름 충돌 문제 수정</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2978">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="1d1eb-2979">MSI를 사용할 때 DataLake 엔드포인트 문제 수정</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2979">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="1d1eb-2980">연결되지 않은 경우 'Disconnect-AzAccount'가 throw하는 문제 수정</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2980">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="1d1eb-2981">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2981">Az.CognitiveServices</span></span>
* <span data-ttu-id="1d1eb-2982">Get-AzCognitiveServicesAccountSkus 작업을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2982">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="1d1eb-2983">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2983">Az.Compute</span></span>
* <span data-ttu-id="1d1eb-2984">Add-AzVmssVMDataDisk 및 Remove-AzVmssVMDataDisk cmdlet를 추가합니다</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2984">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="1d1eb-2985">Get-AzVMImage는 AutomaticOSUpgradeProperties를 표시합니다</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2985">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="1d1eb-2986">수정된 SetAzVMChefExtension -BootstrapOptions 및 -JsonAttribute option 값이 json 형식으로 설정하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2986">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="1d1eb-2987">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2987">Az.DataLakeStore</span></span>
* <span data-ttu-id="1d1eb-2988">DataLake 패키지를 1.1.10으로 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2988">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="1d1eb-2989">기본 동시성을 다중 스레드 작업에 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2989">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="1d1eb-2990">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2990">Az.Insights</span></span>
* <span data-ttu-id="1d1eb-2991">해결된 문제 #7267(자동 크기 조정 영역)</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2991">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="1d1eb-2992">열거된 매개 변수를 제대로 설정하지 않은 새 자동 크기 조정 규칙을 만드는 데 문제가 있습니다(이를 항상 기본값으로 설정함).</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2992">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="1d1eb-2993">해결된 문제 # 7513[자세한 정보] Set-AzDiagnosticSetting은 설정을 생성하는 동안 범주를 명시적으로 지정해야 합니다</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2993">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="1d1eb-2994">이제 cmdlet은 생성 중에 사용할 범주를 명시적으로 표시할 필요가 없습니다. 즉, 문서화된대로 작동합니다</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2994">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="1d1eb-2995">Az.Network</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2995">Az.Network</span></span>
* <span data-ttu-id="1d1eb-2996">다음 cmdlet에 대해 PeeringType을 필수 매개 변수로 변경했습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2996">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="1d1eb-2997">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2997">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="1d1eb-2998">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2998">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="1d1eb-2999">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="1d1eb-2999">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="1d1eb-3000">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="1d1eb-3000">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="1d1eb-3001">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="1d1eb-3001">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="1d1eb-3002">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="1d1eb-3002">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="1d1eb-3003">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="1d1eb-3003">Az.PolicyInsights</span></span>
* <span data-ttu-id="1d1eb-3004">추가된 정책 재구성 cmdlet</span><span class="sxs-lookup"><span data-stu-id="1d1eb-3004">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="1d1eb-3005">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="1d1eb-3005">Az.Resources</span></span>
* <span data-ttu-id="1d1eb-3006"> https://github.com/Azure/azure-powershell/issues/7402 에 대한 수정</span><span class="sxs-lookup"><span data-stu-id="1d1eb-3006">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="1d1eb-3007">'Get-AzResource'에 대해 '-ResourceId' 매개 변수를 사용하여 리소스 나열 허용</span><span class="sxs-lookup"><span data-stu-id="1d1eb-3007">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="1d1eb-3008">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="1d1eb-3008">Az.ServiceBus</span></span>
* <span data-ttu-id="1d1eb-3009">마이그레이션 상태를 알 수 있도록 PSServiceBusMigrationConfigurationAttributes에 MigrationState 읽기 전용 속성 추가.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-3009">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="1d1eb-3010">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="1d1eb-3010">Az.ServiceFabric</span></span>
* <span data-ttu-id="1d1eb-3011">Linux Vmss에 인증서 추가 수정.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-3011">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="1d1eb-3012">Add-AzServiceFabricClusterCertificate 수정</span><span class="sxs-lookup"><span data-stu-id="1d1eb-3012">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="1d1eb-3013">새 인증서(Azure/service-fabric-issues#932)에서 올바른 지문을 사용.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-3013">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="1d1eb-3014">올바르게 예외 표시(Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="1d1eb-3014">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="1d1eb-3015">Vmss CreateOrUpdate 작업을 시작하기 전에 'Update-AzServiceFabricDurability'를 수정하여 클러스터 구성 업데이트.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-3015">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="1d1eb-3016">0.4.0 - 2018년 10월</span><span class="sxs-lookup"><span data-stu-id="1d1eb-3016">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="1d1eb-3017">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="1d1eb-3017">Az.Profile</span></span>
* <span data-ttu-id="1d1eb-3018">CloudShell에서 Get-AzSubscription을 사용하여 문제를 해결합니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-3018">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="1d1eb-3019">ClientRuntime의 최신 버전을 사용하도록 일반적인 코드를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-3019">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="1d1eb-3020">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="1d1eb-3020">Az.Compute</span></span>
* <span data-ttu-id="1d1eb-3021">'New-AzVm'에 대해 간단한 매개 변수를 사용하는 경우 가속화된 네트워킹을 설정하기 위해 새 크기가 VM 크기의 허용 목록에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-3021">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="1d1eb-3022">모든 cmdlet에 ResourceName 인수 완성자가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-3022">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="1d1eb-3023">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="1d1eb-3023">Az.DataLakeStore</span></span>
* <span data-ttu-id="1d1eb-3024">Virtual Network 규칙에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="1d1eb-3024">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="1d1eb-3025">Get-AzDataLakeStoreVirtualNetworkRule: Azure Data Lake Store 가상 네트워크 규칙을 가져오거나 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-3025">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="1d1eb-3026">Add-AzDataLakeStoreVirtualNetworkRule: 지정된 Data Lake Store 계정에 가상 네트워크 규칙을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-3026">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="1d1eb-3027">Set-AzDataLakeStoreVirtualNetworkRule: 지정된 Data Lake Store 계정에 지정된 가상 네트워크 규칙을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-3027">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="1d1eb-3028">Remove-AzDataLakeStoreVirtualNetworkRule: Azure Data Lake Store 가상 네트워크 규칙을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-3028">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="1d1eb-3029">Az.Network</span><span class="sxs-lookup"><span data-stu-id="1d1eb-3029">Az.Network</span></span>
* <span data-ttu-id="1d1eb-3030">Test-AzNetworkWatcherConnectivity cmdlet을 업데이트하고, 백 엔드에 프로토콜 값을 전달합니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-3030">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="1d1eb-3031">모든 cmdlet에 ResourceName 인수 완성자가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-3031">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="1d1eb-3032">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="1d1eb-3032">Az.Resources</span></span>
* <span data-ttu-id="1d1eb-3033">(기본 프로필에 구독이 없고 범위가 지정되지 않은 경우) 시나리오에서 의미 있는 예외를 추가하여 Get-AzRoleDefinition이 인식할 수 없는 예외를 throw하는 문제를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-3033">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="1d1eb-3034">또한 기본 매개 변수 집합을 'RoleDefinitionNameParameterSet'으로 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-3034">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="1d1eb-3035">0.3.0 - 2018년 10월</span><span class="sxs-lookup"><span data-stu-id="1d1eb-3035">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="1d1eb-3036">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="1d1eb-3036">Azure.Storage</span></span>
* <span data-ttu-id="1d1eb-3037">대상에 메타데이터가 있을 때 Blob/파일이 메타 데이터를 복사하지 않는 문제 수정</span><span class="sxs-lookup"><span data-stu-id="1d1eb-3037">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="1d1eb-3038">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="1d1eb-3038">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="1d1eb-3039">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="1d1eb-3039">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="1d1eb-3040">특정 위치의 스토리지 리소스 사용을 지원하고 글로벌 스토리지 리소스 사용 가져오기는 더 이상 사용되지 않는다는 경고 메시지를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-3040">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="1d1eb-3041">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="1d1eb-3041">Get-AzStorageUsage</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="1d1eb-3042">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="1d1eb-3042">Az.CognitiveServices</span></span>
* <span data-ttu-id="1d1eb-3043">기존 계정이 없는 Get-AzCognitiveServicesAccountSkus를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-3043">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="1d1eb-3044">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="1d1eb-3044">Az.Compute</span></span>
* <span data-ttu-id="1d1eb-3045">Get-AzVM -ResourceGroupName <rg>가 필요한 경우 50개가 넘는 결과를 반환하도록 수정</span><span class="sxs-lookup"><span data-stu-id="1d1eb-3045">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="1d1eb-3046">'SimpleParameterSet' 예제가 New-AzVmss cmdlet 도움말에 추가됨</span><span class="sxs-lookup"><span data-stu-id="1d1eb-3046">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="1d1eb-3047">Azure Disk Encryption 진행률 메시지의 오타를 수정</span><span class="sxs-lookup"><span data-stu-id="1d1eb-3047">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="1d1eb-3048">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="1d1eb-3048">Az.DataFactoryV2</span></span>
* <span data-ttu-id="1d1eb-3049">ADF.Net SDK 버전을 2.3.0으로 업데이트</span><span class="sxs-lookup"><span data-stu-id="1d1eb-3049">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="1d1eb-3050">Az.Network</span><span class="sxs-lookup"><span data-stu-id="1d1eb-3050">Az.Network</span></span>
* <span data-ttu-id="1d1eb-3051">NetworkProfile 기능 추가</span><span class="sxs-lookup"><span data-stu-id="1d1eb-3051">Added NetworkProfile functionality.</span></span> <span data-ttu-id="1d1eb-3052">추가된 새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-3052">new cmdlets added</span></span>
    - <span data-ttu-id="1d1eb-3053">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="1d1eb-3053">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="1d1eb-3054">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="1d1eb-3054">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="1d1eb-3055">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="1d1eb-3055">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="1d1eb-3056">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="1d1eb-3056">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="1d1eb-3057">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="1d1eb-3057">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="1d1eb-3058">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="1d1eb-3058">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="1d1eb-3059">서브넷 모델에 서비스 연결 링크 추가</span><span class="sxs-lookup"><span data-stu-id="1d1eb-3059">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="1d1eb-3060">New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="1d1eb-3060">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="1d1eb-3061">Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="1d1eb-3061">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="1d1eb-3062">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="1d1eb-3062">Az.RedisCache</span></span>
* <span data-ttu-id="1d1eb-3063">모든 문자열을 Size 매개 변수로 진행되도록 허용</span><span class="sxs-lookup"><span data-stu-id="1d1eb-3063">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="1d1eb-3064">PSArgumentCompleter 팝업에 P5 추가</span><span class="sxs-lookup"><span data-stu-id="1d1eb-3064">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="1d1eb-3065">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="1d1eb-3065">Az.Resources</span></span>
* <span data-ttu-id="1d1eb-3066">-Mode 매개 변수를 Set-AzPolicyDefinition에 추가</span><span class="sxs-lookup"><span data-stu-id="1d1eb-3066">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="1d1eb-3067">사용자가 포함된 Origin 작업에서 Get-AzProviderOperation commandlet 버그 수정</span><span class="sxs-lookup"><span data-stu-id="1d1eb-3067">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="1d1eb-3068">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="1d1eb-3068">Az.Sql</span></span>
* <span data-ttu-id="1d1eb-3069">일부 백업 cmdlet이 현재 azure 구독을 인식하지 않는 문제 해결</span><span class="sxs-lookup"><span data-stu-id="1d1eb-3069">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="1d1eb-3070">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="1d1eb-3070">Az.Websites</span></span>
* <span data-ttu-id="1d1eb-3071">새 cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - 컨테이너 지속적인 배포 Webhook URL을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-3071">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="1d1eb-3072">새 cmdlet New-AzWebAppContainerPSSession 및 Enter-WebAppContainerPSSession -  windows 컨테이너 앱에 PowerShell 원격 세션을 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-3072">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="1d1eb-3073">0.2.0 - 2018년 9월</span><span class="sxs-lookup"><span data-stu-id="1d1eb-3073">0.2.0 - September 2018</span></span>
 <span data-ttu-id="1d1eb-3074">초기 릴리스</span><span class="sxs-lookup"><span data-stu-id="1d1eb-3074">Initial Release</span></span>
