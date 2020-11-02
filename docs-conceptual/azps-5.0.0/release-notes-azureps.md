---
title: Azure PowerShell 릴리스 정보
description: Azure PowerShell 모듈의 모든 최신 업데이트에 대해 알아봅니다.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/10/2020
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: 913532fa5a8937f7ba4cc1ce21c5879f3920fc7f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92753591"
---
# <a name="azure-powershell-release-notes"></a><span data-ttu-id="6783d-103">Azure PowerShell 릴리스 정보</span><span class="sxs-lookup"><span data-stu-id="6783d-103">Azure PowerShell release notes</span></span>

## <a name="500---october-2020"></a><span data-ttu-id="6783d-104">5.0.0 - 2020년 10월</span><span class="sxs-lookup"><span data-stu-id="6783d-104">5.0.0 - October 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="6783d-105">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6783d-105">Az.Accounts</span></span>
* <span data-ttu-id="6783d-106">[호환성이 손상되는 변경] 'Get-AzProfile' 및 'Select-AzProfile'이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-106">[Breaking Change] Removed 'Get-AzProfile' and 'Select-AzProfile'</span></span>
* <span data-ttu-id="6783d-107">Azure Directory 인증 라이브러리가 MSAL(Microsoft 인증 라이브러리)로 대체되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-107">Replaced Azure Directory Authentication Library with Microsoft Authentication Library(MSAL)</span></span>

#### <a name="azaks"></a><span data-ttu-id="6783d-108">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="6783d-108">Az.Aks</span></span>
* <span data-ttu-id="6783d-109">[호환성이 손상되는 변경] 'New-AzAksCluster' 및 'Set-AzAksCluster'에서 매개 변수 별칭 'ClientIdAndSecret'이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-109">[Breaking Change] Removed parameter alias 'ClientIdAndSecret' in 'New-AzAksCluster' and 'Set-AzAksCluster'.</span></span>
* <span data-ttu-id="6783d-110">[호환성이 손상되는 변경] 'New-AzAksCluster'의 'NodeVmSetType' 기본값이 'AvailabilitySet'에서 'VirtualMachineScaleSets'로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-110">[Breaking Change] Changed the default value of 'NodeVmSetType' in 'New-AzAksCluster' from 'AvailabilitySet' to 'VirtualMachineScaleSets'.</span></span>
* <span data-ttu-id="6783d-111">[호환성이 손상되는 변경] 'New-AzAksCluster'의 'NetworkPlugin' 기본값이 'None'에서 'azure'로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-111">[Breaking Change] Changed the default value of 'NetworkPlugin' in 'New-AzAksCluster' from 'None' to 'azure'.</span></span>
* <span data-ttu-id="6783d-112">[호환성이 손상되는 변경] 'New-AzAksCluster'의 'NodeOsType' 매개 변수는 Linux라는 하나의 값만 지원하므로 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-112">[Breaking Change] Removed parameter 'NodeOsType' in 'New-AzAksCluster' as it supports only one value Linux.</span></span>

#### <a name="azbilling"></a><span data-ttu-id="6783d-113">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="6783d-113">Az.Billing</span></span>
* <span data-ttu-id="6783d-114">'Get-AzBillingAccount' cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-114">Added 'Get-AzBillingAccount' cmdlet</span></span>
* <span data-ttu-id="6783d-115">'Get-AzBillingProfile' cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-115">Added 'Get-AzBillingProfile' cmdlet</span></span>
* <span data-ttu-id="6783d-116">'Get-AzInvoiceSection' cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-116">Added 'Get-AzInvoiceSection' cmdlet</span></span>
* <span data-ttu-id="6783d-117">'Get-AzBillingInvoice' cmdlet에 새 매개 변수가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-117">Added new parameters in 'Get-AzBillingInvoice' cmdlet</span></span>
* <span data-ttu-id="6783d-118">Get-AzBillingInvoice cmdlet의 응답에서 DownloadUrlExpiry, Type, BillingPeriodNames 속성이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-118">Removed properties DownloadUrlExpiry, Type, BillingPeriodNames from the response of Get-AzBillingInvoice cmdlet</span></span>

#### <a name="azcdn"></a><span data-ttu-id="6783d-119">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="6783d-119">Az.Cdn</span></span>
* <span data-ttu-id="6783d-120">다중 원본 및 프라이빗 링크 기능을 지원하는 cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-120">Added cmdlets to support multi-origin and private link functionality</span></span> 

#### <a name="azcognitiveservices"></a><span data-ttu-id="6783d-121">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="6783d-121">Az.CognitiveServices</span></span>
* <span data-ttu-id="6783d-122">SDK가 7.4.0-preview로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-122">Updated SDK to 7.4.0-preview.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6783d-123">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6783d-123">Az.Compute</span></span>
* <span data-ttu-id="6783d-124">'New-AzVm'에 '-VmssId' 매개 변수가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-124">Added '-VmssId' parameter to 'New-AzVm'</span></span>
* <span data-ttu-id="6783d-125">'New-AzVmss' cmdlet에 'PlatformFaultDomainCount' 매개 변수가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-125">Added 'PlatformFaultDomainCount' parameter to the 'New-AzVmss' cmdlet.</span></span>
* <span data-ttu-id="6783d-126">새 cmdlet 'Get-AzDiskEncryptionSetAssociatedResource'</span><span class="sxs-lookup"><span data-stu-id="6783d-126">New cmdlet 'Get-AzDiskEncryptionSetAssociatedResource'</span></span>
* <span data-ttu-id="6783d-127">New-AzDiskConfig cmdlet에 선택적 매개 변수 'Tier' 및 'LogicalSectorSize'가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-127">Added 'Tier' and 'LogicalSectorSize' optional parameters to the New-AzDiskConfig cmdlet.</span></span> 
* <span data-ttu-id="6783d-128">'New-AzDiskUpdateConfig' cmdlet에 선택적 매개 변수 'Tier', 'MaxSharesCount', 'DiskIOPSReadOnly' 및 'DiskMBpsReadOnly'가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-128">Added 'Tier', 'MaxSharesCount', 'DiskIOPSReadOnly', and 'DiskMBpsReadOnly' optional parameters to the 'New-AzDiskUpdateConfig' cmdlet.</span></span> 

#### <a name="azcontainerregistry"></a><span data-ttu-id="6783d-129">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="6783d-129">Az.ContainerRegistry</span></span>
* <span data-ttu-id="6783d-130">[호환성이 손상되는 변경] API 버전이 2020-05-01로 업데이트됩니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-130">[Breaking Change] Updates API version to 2020-05-01</span></span>
* <span data-ttu-id="6783d-131">[호환성이 손상되는 변경] 'New-AzContainerRegistry'에서 SKU 'Classic' 및 'StorageAccountName' 매개 변수가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-131">[Breaking Change] Removed SKU 'Classic' and parameter 'StorageAccountName' from 'New-AzContainerRegistry'</span></span>
* <span data-ttu-id="6783d-132">새 cmdlet이 추가되었습니다. 'Connect-AzContainerRegistry', 'Import-AzContainerRegistry', 'Get-AzContainerRegistryUsage', 'New-AzContainerRegistryNetworkRule', 'Set-AzContainerRegistryNetworkRule'</span><span class="sxs-lookup"><span data-stu-id="6783d-132">Added New cmdlets: 'Connect-AzContainerRegistry', 'Import-AzContainerRegistry', 'Get-AzContainerRegistryUsage', 'New-AzContainerRegistryNetworkRule', 'Set-AzContainerRegistryNetworkRule'</span></span>
* <span data-ttu-id="6783d-133">'Update-AzContainerRegistry'에 새 매개 변수 'NetworkRuleSet'가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-133">Added new parameter 'NetworkRuleSet' to 'Update-AzContainerRegistry'</span></span>

#### <a name="azdatabricks"></a><span data-ttu-id="6783d-134">Az.Databricks</span><span class="sxs-lookup"><span data-stu-id="6783d-134">Az.Databricks</span></span>
* <span data-ttu-id="6783d-135">`-EncryptionKeyVersion`이 없으면 databricks 작업 영역 업데이트가 실패하는 버그가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-135">Fixed a bug that may cause updating databricks workspace without `-EncryptionKeyVersion` to fail.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="6783d-136">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="6783d-136">Az.DataFactory</span></span>
* <span data-ttu-id="6783d-137">ADF .Net SDK 버전이 4.12.0으로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-137">Updated ADF .Net SDK version to 4.12.0</span></span>
* <span data-ttu-id="6783d-138">ADF 암호화 클라이언트 SDK 버전이 4.14.7587.7로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-138">Updated ADF encryption client SDK version to 4.14.7587.7</span></span>
* <span data-ttu-id="6783d-139">'Stop-AzDataFactoryV2TriggerRun' 및 'Invoke-AzDataFactoryV2TriggerRun' 명령이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-139">Added 'Stop-AzDataFactoryV2TriggerRun' and 'Invoke-AzDataFactoryV2TriggerRun' commands</span></span>

#### <a name="azdesktopvirtualization"></a><span data-ttu-id="6783d-140">Az.DesktopVirtualization</span><span class="sxs-lookup"><span data-stu-id="6783d-140">Az.DesktopVirtualization</span></span>
* <span data-ttu-id="6783d-141">최상위 arm 개체를 만들려면 Location 속성이 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-141">Require Location property for creating top level arm objects.</span></span>
        <span data-ttu-id="6783d-142">\* `New-AzWvdApplicationGroup`에 `ApplicationGroupType`이 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-142">\* Made `ApplicationGroupType` required for `New-AzWvdApplicationGroup`.</span></span>
        <span data-ttu-id="6783d-143">\* `New-AzWvdApplicationGroup`에 `HostPoolArmPath`가 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-143">\* Made `HostPoolArmPath` required for `New-AzWvdApplicationGroup`.</span></span>
        <span data-ttu-id="6783d-144">\* `New-AzWvdHostPool`에 `PreferredAppGroupType`이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-144">\* Added `PreferredAppGroupType` for `New-AzWvdHostPool`.</span></span>

#### <a name="azfunctions"></a><span data-ttu-id="6783d-145">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="6783d-145">Az.Functions</span></span>
* <span data-ttu-id="6783d-146">[호환성이 손상되는 변경] 'Get-AzFunctionApp' 매개 변수 세트 하나를 제외한 모든 매개 변수 세트에서 'IncludeSlot' 스위치 매개 변수가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-146">[Breaking Change] Removed 'IncludeSlot' switch parameter from all but one parameter set of 'Get-AzFunctionApp'.</span></span> <span data-ttu-id="6783d-147">이제 이 cmdlet은 '-IncludeSlot'이 지정된 경우 결과에서 배포 슬롯 검색을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-147">The cmdlet now supports retrieving deployment slots in the results when '-IncludeSlot' is specified.</span></span> 
* <span data-ttu-id="6783d-148">'New-AzFunctionApp'이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-148">Updated 'New-AzFunctionApp':</span></span>
  - <span data-ttu-id="6783d-149">이 옵션을 지정할 경우 application insights 프로젝트가 생성되지 않도록 -DisableApplicationInsights가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-149">Fixed -DisableApplicationInsights so that no application insights project is created when this option is specified.</span></span> <span data-ttu-id="6783d-150">[#12728]</span><span class="sxs-lookup"><span data-stu-id="6783d-150">[#12728]</span></span>
  - <span data-ttu-id="6783d-151">[호환성이 손상되는 변경] PowerShell 6.2 함수 앱을 만드는 지원 기능이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-151">[Breaking Change] Removed support to create PowerShell 6.2 function apps.</span></span>
  - <span data-ttu-id="6783d-152">[호환성이 손상되는 변경] RuntimeVersion 매개 변수가 지정되지 않은 경우 PowerShell 함수 앱에 대한 Windows의 Functions 버전 3 기본 런타임 버전이 6.2에서 7.0으로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-152">[Breaking Change] Changed the default runtime version in Functions version 3 on Windows for PowerShell function apps from 6.2 to 7.0 when the RuntimeVersion parameter is not specified.</span></span>
  - <span data-ttu-id="6783d-153">[호환성이 손상되는 변경] RuntimeVersion 매개 변수가 지정되지 않은 경우 Node 함수 앱에 대한 Windows 및 Linux의 Functions 버전 3 기본 런타임 버전이 10에서 12로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-153">[Breaking Change] Changed the default runtime version in Functions version 3 on Windows and Linux for Node function apps from 10 to 12 when the RuntimeVersion parameter is not specified.</span></span>
  - <span data-ttu-id="6783d-154">[호환성이 손상되는 변경] RuntimeVersion 매개 변수가 지정되지 않은 경우 Python 함수 앱에 대한 Linux의 Functions 버전 3 기본 런타임 버전이 3.7에서 3.8로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-154">[Breaking Change] Changed the default runtime version in Functions version 3 on Linux for Python function apps from 3.7 to 3.8 when the RuntimeVersion parameter is not specified.</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="6783d-155">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="6783d-155">Az.HDInsight</span></span>
 * <span data-ttu-id="6783d-156">AzHDInsightCluster cmdlet의 경우:</span><span class="sxs-lookup"><span data-stu-id="6783d-156">For New-AzHDInsightCluster cmdlet:</span></span>
     - <span data-ttu-id="6783d-157">'DefaultStorageAccountName' 매개 변수가 'StorageAccountResourceId'로 대체되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-157">Replaced parameter 'DefaultStorageAccountName' with 'StorageAccountResourceId'</span></span>
     - <span data-ttu-id="6783d-158">'DefaultStorageAccountKey' 매개 변수가 'StorageAccountKey'로 대체되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-158">Replaced parameter 'DefaultStorageAccountKey' with 'StorageAccountKey'</span></span>
     - <span data-ttu-id="6783d-159">'DefaultStorageAccountType' 매개 변수가 'StorageAccountType'으로 대체되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-159">Replaced parameter 'DefaultStorageAccountType' with 'StorageAccountType'</span></span>
     - <span data-ttu-id="6783d-160">'PublicNetworkAccessType' 매개 변수가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-160">Removed parameter 'PublicNetworkAccessType'</span></span>
     - <span data-ttu-id="6783d-161">'OutboundPublicNetworkAccessType' 매개 변수가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-161">Removed parameter 'OutboundPublicNetworkAccessType'</span></span>
     - <span data-ttu-id="6783d-162">새 매개 변수가 추가되었습니다. ADLSGen2를 지원하기 위한 'StorageFileSystem' 및 'StorageAccountManagedIdentity'</span><span class="sxs-lookup"><span data-stu-id="6783d-162">Added new parameters: 'StorageFileSystem' and 'StorageAccountManagedIdentity' to support ADLSGen2</span></span>
     - <span data-ttu-id="6783d-163">HDInsight ID Broker를 지원하기 위해 새 매개 변수 'EnableIDBroker'가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-163">Added new parameter 'EnableIDBroker' to Support HDInsight ID Broker</span></span>
     - <span data-ttu-id="6783d-164">새 매개 변수가 추가되었습니다. Kafka Rest Proxy를 지원하기 위한 'KafkaClientGroupId', 'KafkaClientGroupName' 및 'KafkaManagementNodeSize'</span><span class="sxs-lookup"><span data-stu-id="6783d-164">Added new parameters: 'KafkaClientGroupId', 'KafkaClientGroupName' and 'KafkaManagementNodeSize' to support Kafka Rest Proxy</span></span>
 * <span data-ttu-id="6783d-165">New-AzHDInsightClusterConfig cmdlet의 경우:</span><span class="sxs-lookup"><span data-stu-id="6783d-165">For New-AzHDInsightClusterConfig cmdlet:</span></span>
     - <span data-ttu-id="6783d-166">'DefaultStorageAccountName' 매개 변수가 'StorageAccountResourceId'로 대체되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-166">Replaced parameter 'DefaultStorageAccountName' with 'StorageAccountResourceId'</span></span>
     - <span data-ttu-id="6783d-167">'DefaultStorageAccountKey' 매개 변수가 'StorageAccountKey'로 대체되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-167">Replaced parameter 'DefaultStorageAccountKey' with 'StorageAccountKey'</span></span>
     - <span data-ttu-id="6783d-168">'DefaultStorageAccountType' 매개 변수가 'StorageAccountType'으로 대체되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-168">Replaced parameter 'DefaultStorageAccountType' with 'StorageAccountType'</span></span>
     - <span data-ttu-id="6783d-169">'PublicNetworkAccessType' 매개 변수가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-169">Removed parameter 'PublicNetworkAccessType'</span></span>
     - <span data-ttu-id="6783d-170">'OutboundPublicNetworkAccessType' 매개 변수가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-170">Removed parameter 'OutboundPublicNetworkAccessType'</span></span>
* <span data-ttu-id="6783d-171">Set-AzHDInsightDefaultStorage cmdlet의 경우:</span><span class="sxs-lookup"><span data-stu-id="6783d-171">For Set-AzHDInsightDefaultStorage cmdlet:</span></span>
    - <span data-ttu-id="6783d-172">'StorageAccountName' 매개 변수가 'StorageAccountResourceId'로 대체되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-172">Replaced parameter 'StorageAccountName' with 'StorageAccountResourceId'</span></span>
* <span data-ttu-id="6783d-173">Add-AzHDInsightSecurityProfile cmdlet의 경우:</span><span class="sxs-lookup"><span data-stu-id="6783d-173">For Add-AzHDInsightSecurityProfile cmdlet:</span></span>
    - <span data-ttu-id="6783d-174">'Domain' 매개 변수가 'DomainResourceId'로 대체되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-174">Replaced parameter 'Domain' with 'DomainResourceId'</span></span>
    - <span data-ttu-id="6783d-175">'OrganizationalUnitDN' 매개 변수에 대한 필수 요구 사항이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-175">Removed the mandatory requirement for parameter 'OrganizationalUnitDN'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="6783d-176">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="6783d-176">Az.KeyVault</span></span>
* <span data-ttu-id="6783d-177">[호환성이 손상되는 변경] 'New-AzKeyVault'의 DisableSoftDelete 매개 변수와 'Update-AzKeyVault'의 EnableSoftDelete 매개 변수가 더 이상 사용되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-177">[Breaking Change] Deprecated parameter DisableSoftDelete in 'New-AzKeyVault' and EnableSoftDelete in 'Update-AzKeyVault'</span></span>
* <span data-ttu-id="6783d-178">[호환성이 손상되는 변경] SecretValue를 직접 표시하지 않도록 SecretValueText 특성이 제거되었습니다. [#12266]</span><span class="sxs-lookup"><span data-stu-id="6783d-178">[Breaking Change] Removed attribute SecretValueText to avoid displaying SecretValue directly [#12266]</span></span>
* <span data-ttu-id="6783d-179">새 리소스 유형 지원: 관리형 HSM</span><span class="sxs-lookup"><span data-stu-id="6783d-179">Supported new resource type: managed HSM</span></span>
    - <span data-ttu-id="6783d-180">관리형 HSM의 CRUD와 관리형 HSM에서 키를 작동하는 cmdlet</span><span class="sxs-lookup"><span data-stu-id="6783d-180">CRUD of managed HSM and cmdlets to operate keys on managed HSM</span></span>
    - <span data-ttu-id="6783d-181">전체 HSM 백업/복원, AES 키 생성, 보안 도메인 백업/복원, RBAC</span><span class="sxs-lookup"><span data-stu-id="6783d-181">Full HSM backup/restore, AES key creation, security domain backup/restore, RBAC</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="6783d-182">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="6783d-182">Az.ManagedServices</span></span>
* <span data-ttu-id="6783d-183">[호환성이 손상되는 변경] 업데이트된 매개 변수 명명 규칙 및 관련 예제</span><span class="sxs-lookup"><span data-stu-id="6783d-183">[Breaking Change] Updated parameters naming conventions and associated examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6783d-184">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6783d-184">Az.Network</span></span>
* <span data-ttu-id="6783d-185">[호환성이 손상되는 변경] 'HostedSubnet' 매개 변수가 제거되고 'Subnet'이 대신 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-185">[Breaking Change] Removed parameter 'HostedSubnet' and added 'Subnet' instead</span></span>
* <span data-ttu-id="6783d-186">가상 라우터 피어 경로에 대한 새 cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-186">Added new cmdlets for Virtual Router Peer Routes</span></span>
    - <span data-ttu-id="6783d-187">'Get-AzVirtualRouterPeerLearnedRoute'</span><span class="sxs-lookup"><span data-stu-id="6783d-187">'Get-AzVirtualRouterPeerLearnedRoute'</span></span>
    - <span data-ttu-id="6783d-188">'Get-AzVirtualRouterPeerAdvertisedRoute'</span><span class="sxs-lookup"><span data-stu-id="6783d-188">'Get-AzVirtualRouterPeerAdvertisedRoute'</span></span>
* <span data-ttu-id="6783d-189">New-AzFirewall cmdlet이 업데이트됨:</span><span class="sxs-lookup"><span data-stu-id="6783d-189">Updated New-AzFirewall cmdlet:</span></span>
    - <span data-ttu-id="6783d-190">'-SkuTier' 매개 변수가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-190">Added parameter '-SkuTier'</span></span>
    - <span data-ttu-id="6783d-191">'-SkuName' 매개 변수가 추가되었으며 Sku가 이 매개 변수의 별칭이 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-191">Added parameter '-SkuName' and made Sku as Alias for this</span></span>
    - <span data-ttu-id="6783d-192">'-Sku' 매개 변수가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-192">Removed parameter '-Sku'</span></span>
* <span data-ttu-id="6783d-193">[호환성이 손상되는 변경] 'Start-AzVpnConnectionPacketCapture' 및 'Stop-AzVpnConnectionPacketCapture'에서 'Connectionlink' 인수가 필수가 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-193">[Breaking Change] Made 'Connectionlink' argument mandatory in 'Start-AzVpnConnectionPacketCapture' and 'Stop-AzVpnConnectionPacketCapture'</span></span>
* <span data-ttu-id="6783d-194">[호환성이 손상되는 변경] '-Filter' 매개 변수를 제거하도록 'New-AzNetworkWatcherConnectionMonitorEndPointObject'가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-194">[Breaking Change] Updated 'New-AzNetworkWatcherConnectionMonitorEndPointObject' to remove parameter '-Filter'</span></span>
* <span data-ttu-id="6783d-195">[호환성이 손상되는 변경] 'New-AzNetworkWatcherConnectionMonitorEndpointFilterItemObject' cmdlet이 'New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject'로 대체되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-195">[Breaking Change] Replaced 'New-AzNetworkWatcherConnectionMonitorEndpointFilterItemObject' cmdlet with 'New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject'</span></span>
* <span data-ttu-id="6783d-196">'New-AzNetworkWatcherConnectionMonitorEndPointObject' cmdlet이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-196">Updated 'New-AzNetworkWatcherConnectionMonitorEndPointObject' cmdlet:</span></span>
    - <span data-ttu-id="6783d-197">'-Type' 매개 변수가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-197">Added parameter '-Type'</span></span>
    - <span data-ttu-id="6783d-198">'-CoverageLevel' 매개 변수가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-198">Added parameter '-CoverageLevel'</span></span>
    - <span data-ttu-id="6783d-199">'-Scope' 매개 변수가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-199">Added parameter '-Scope'</span></span>
* <span data-ttu-id="6783d-200">'New-AzNetworkWatcherConnectionMonitorProtocolConfigurationObject' cmdlet이 새 매개 변수 '-DestinationPortBehavior'로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-200">Updated 'New-AzNetworkWatcherConnectionMonitorProtocolConfigurationObject' cmdlet with new parameter '-DestinationPortBehavior'</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="6783d-201">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="6783d-201">Az.RecoveryServices</span></span>
* <span data-ttu-id="6783d-202">기여자 권한을 위해 워크로드 복원을 수정하는 중입니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-202">Fixing Workload Restore for contributor permissions.</span></span>
* <span data-ttu-id="6783d-203">Restore-AzRecoveryServicesBackupItem cmdlet에 대한 새 매개 변수 집합 및 유효성 검사가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-203">Added new parameter sets and validations for Restore-AzRecoveryServicesBackupItem cmdlet.</span></span>

#### <a name="azresources"></a><span data-ttu-id="6783d-204">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6783d-204">Az.Resources</span></span>
* <span data-ttu-id="6783d-205">구문 분석 버그가 해결되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-205">Fixed parsing bug</span></span>
* <span data-ttu-id="6783d-206">결과에서 미리 보기 메시지를 제거하도록 ARM 템플릿 What-If cmdlet이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-206">Updated ARM template What-If cmdlets to remove preview message from results</span></span>
* <span data-ttu-id="6783d-207">'-WhatIf'가 상위 범위에서 설정된 경우 템플릿 배포 cmdlet의 작동이 중단되는 문제가 해결되었습니다. [#13038]</span><span class="sxs-lookup"><span data-stu-id="6783d-207">Fixed an issue where template deployment cmdlets crash if '-WhatIf' is set at a higher scope [#13038]</span></span>
* <span data-ttu-id="6783d-208">템플릿 배포 cmdlet이 템플릿 매개 변수에서 대/소문자를 구분하지 않는 문제가 해결되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-208">Fixed an issue where template deployment cmdlets does not preserve case for template parameters</span></span>
* <span data-ttu-id="6783d-209">'Export-AzResourceGroup' cmdlet에 사용되는 기본 API 버전이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-209">Added a default API version to be used in 'Export-AzResourceGroup' cmdlet</span></span>
* <span data-ttu-id="6783d-210">템플릿 사양에 대한 cmdlet이 추가되었습니다('Get-AzTemplateSpec', 'Set-AzTemplateSpec', 'New-AzTemplateSpec', 'Remove-AzTemplateSpec', 'Export-AzTemplateSpec').</span><span class="sxs-lookup"><span data-stu-id="6783d-210">Added cmdlets for Template Specs ('Get-AzTemplateSpec', 'Set-AzTemplateSpec', 'New-AzTemplateSpec', 'Remove-AzTemplateSpec', 'Export-AzTemplateSpec')</span></span>
* <span data-ttu-id="6783d-211">새 -TemplateSpecId 매개 변수를 통해 기존 배포 cmdlet을 사용하여 템플릿 사양을 배포하도록 지원하는 기능이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-211">Added support for deploying Template Specs using existing deployment cmdlets (via the new -TemplateSpecId parameter)</span></span> 
* <span data-ttu-id="6783d-212">SDK를 사용하도록 'Get-AzResourceGroupDeploymentOperation'이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-212">Updated 'Get-AzResourceGroupDeploymentOperation' to use the SDK.</span></span>
* <span data-ttu-id="6783d-213">'\*-AzDeployment' cmdlet에서 '-ApiVersion' 매개 변수가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-213">Removed '-ApiVersion' parameter from '\*-AzDeployment' cmdlets.</span></span>

#### <a name="azsql"></a><span data-ttu-id="6783d-214">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6783d-214">Az.Sql</span></span>
* <span data-ttu-id="6783d-215">'Set-AzSqlDatabaseBackupShortTermRetentionPolicy'에 DiffBackupIntervalInHours가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-215">Added DiffBackupIntervalInHours to 'Set-AzSqlDatabaseBackupShortTermRetentionPolicy'</span></span> 
* <span data-ttu-id="6783d-216">networkIsolation이 지정되지 않은 경우 New-AzSqlDatabaseExport가 실패하는 문제가 해결되었습니다. [#13097]</span><span class="sxs-lookup"><span data-stu-id="6783d-216">Fixed issue where New-AzSqlDatabaseExport fails if networkIsolation not specified [#13097]</span></span>
* <span data-ttu-id="6783d-217">New-AzSqlDatabaseExport 및 New-AzSqlDatabaseImport가 결과 개체에 OperationStatusLink를 반환하지 않는 문제가 해결되었습니다. [#13097]</span><span class="sxs-lookup"><span data-stu-id="6783d-217">Fixed issue where New-AzSqlDatabaseExport and New-AzSqlDatabaseImport were not returning OperationStatusLink in the result object [#13097]</span></span>
* <span data-ttu-id="6783d-218">백업 스토리지 중복성 경고에서 Azure 쌍을 이루는 지역 URL이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-218">Update Azure Paired Regions URL in Backup Storage Redundancy Warnings</span></span> 

#### <a name="azstorage"></a><span data-ttu-id="6783d-219">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="6783d-219">Az.Storage</span></span>
* <span data-ttu-id="6783d-220">더 이상 사용되지 않는 RestorePolicy.LastEnabledTime 속성이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-220">Removed obsolete property RestorePolicy.LastEnabledTime</span></span>
    - <span data-ttu-id="6783d-221">'Enable-AzStorageBlobRestorePolicy'</span><span class="sxs-lookup"><span data-stu-id="6783d-221">'Enable-AzStorageBlobRestorePolicy'</span></span>
    - <span data-ttu-id="6783d-222">'Disable-AzStorageBlobRestorePolicy'</span><span class="sxs-lookup"><span data-stu-id="6783d-222">'Disable-AzStorageBlobRestorePolicy'</span></span>
    - <span data-ttu-id="6783d-223">'Get-AzStorageBlobServiceProperty'</span><span class="sxs-lookup"><span data-stu-id="6783d-223">'Get-AzStorageBlobServiceProperty'</span></span>
    - <span data-ttu-id="6783d-224">'Update-AzStorageBlobServiceProperty'</span><span class="sxs-lookup"><span data-stu-id="6783d-224">'Update-AzStorageBlobServiceProperty'</span></span>
* <span data-ttu-id="6783d-225">DaysAfterModificationGreaterThan의 Type이 int에서 int?로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-225">Change Type of DaysAfterModificationGreaterThan from int to int?</span></span>
    - <span data-ttu-id="6783d-226">'Set-AzStorageAccountManagementPolicy'</span><span class="sxs-lookup"><span data-stu-id="6783d-226">'Set-AzStorageAccountManagementPolicy'</span></span>
    - <span data-ttu-id="6783d-227">'Get-AzStorageAccountManagementPolicy'</span><span class="sxs-lookup"><span data-stu-id="6783d-227">'Get-AzStorageAccountManagementPolicy'</span></span>
    - <span data-ttu-id="6783d-228">'Add-AzStorageAccountManagementPolicyAction'</span><span class="sxs-lookup"><span data-stu-id="6783d-228">'Add-AzStorageAccountManagementPolicyAction'</span></span>
    - <span data-ttu-id="6783d-229">'New-AzStorageAccountManagementPolicyRule'</span><span class="sxs-lookup"><span data-stu-id="6783d-229">'New-AzStorageAccountManagementPolicyRule'</span></span>
* <span data-ttu-id="6783d-230">액세스 계층을 사용한 파일 공유 생성/업데이트가 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-230">Supported create/update file share with access tier</span></span>
    - <span data-ttu-id="6783d-231">'New-AzRmStorageShare'</span><span class="sxs-lookup"><span data-stu-id="6783d-231">'New-AzRmStorageShare'</span></span>
    - <span data-ttu-id="6783d-232">'Update-AzRmStorageShare'</span><span class="sxs-lookup"><span data-stu-id="6783d-232">'Update-AzRmStorageShare'</span></span>
* <span data-ttu-id="6783d-233">Datalake Gen2 항목에서 Acl의 재귀적 설정/업데이트/제거가 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-233">Supported set/update/remove Acl recursively on Datalake Gen2 item</span></span> 
    -  <span data-ttu-id="6783d-234">'Set-AzDataLakeGen2AclRecursive'</span><span class="sxs-lookup"><span data-stu-id="6783d-234">'Set-AzDataLakeGen2AclRecursive'</span></span> 
    -  <span data-ttu-id="6783d-235">'Update-AzDataLakeGen2AclRecursive'</span><span class="sxs-lookup"><span data-stu-id="6783d-235">'Update-AzDataLakeGen2AclRecursive'</span></span> 
    -  <span data-ttu-id="6783d-236">'Remove-AzDataLakeGen2AclRecursive'</span><span class="sxs-lookup"><span data-stu-id="6783d-236">'Remove-AzDataLakeGen2AclRecursive'</span></span>
* <span data-ttu-id="6783d-237">새 권한 x,t를 사용하여 컨테이너 액세스 정책 지원</span><span class="sxs-lookup"><span data-stu-id="6783d-237">Supported Container access policy with new permission x,t</span></span>
    -  <span data-ttu-id="6783d-238">'New-AzStorageContainerStoredAccessPolicy'</span><span class="sxs-lookup"><span data-stu-id="6783d-238">'New-AzStorageContainerStoredAccessPolicy'</span></span>
    -  <span data-ttu-id="6783d-239">'Set-AzStorageContainerStoredAccessPolicy'</span><span class="sxs-lookup"><span data-stu-id="6783d-239">'Set-AzStorageContainerStoredAccessPolicy'</span></span>
* <span data-ttu-id="6783d-240">자식 속성 권한 유형을 열거형에서 문자열로 변경하여 컨테이너 액세스 정책 가져오기/설정 cmdlet의 출력을 변경했습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-240">Changed the output of get/set Container access policy cmdlet, by change the child property Permission type from enum to String</span></span>
    -  <span data-ttu-id="6783d-241">'Get-AzStorageContainerStoredAccessPolicy'</span><span class="sxs-lookup"><span data-stu-id="6783d-241">'Get-AzStorageContainerStoredAccessPolicy'</span></span>
    -  <span data-ttu-id="6783d-242">'Set-AzStorageContainerStoredAccessPolicy'</span><span class="sxs-lookup"><span data-stu-id="6783d-242">'Set-AzStorageContainerStoredAccessPolicy'</span></span>
* <span data-ttu-id="6783d-243">json을 사용한 관리 정책 설정의 샘플 스크립트 문제가 해결되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-243">Fixed a sample script issue of set management policy with json</span></span>
    -  <span data-ttu-id="6783d-244">'Set-AzStorageAccountManagementPolicy'</span><span class="sxs-lookup"><span data-stu-id="6783d-244">'Set-AzStorageAccountManagementPolicy'</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="6783d-245">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="6783d-245">Az.Websites</span></span>
* <span data-ttu-id="6783d-246">Premium V3 가격 책정 계층에 대한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-246">Added support for Premium V3 pricing tier</span></span>
* <span data-ttu-id="6783d-247">WebSites SDK가 3.1.0으로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-247">Updated the WebSites SDK to 3.1.0</span></span>

### <a name="thanks-to-our-community-contributors"></a><span data-ttu-id="6783d-248">커뮤니티 기여자에게 감사드립니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-248">Thanks to our community contributors</span></span>
* <span data-ttu-id="6783d-249">@atul-ram, Get-AzDelegation.md 업데이트(#13176)</span><span class="sxs-lookup"><span data-stu-id="6783d-249">@atul-ram, Update Get-AzDelegation.md (#13176)</span></span>
* <span data-ttu-id="6783d-250">@dineshreddy007, WAC 토큰을 사용하여 Stack HCI를 등록하는 경우 올바르게 할당된 앱 역할을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-250">@dineshreddy007, Get the App Roles assigned correctly in case of Stack HCI registration using WAC token.</span></span> <span data-ttu-id="6783d-251">(#13249)</span><span class="sxs-lookup"><span data-stu-id="6783d-251">(#13249)</span></span>
* <span data-ttu-id="6783d-252">@kongou-ae, New-AzOffice365PolicyProperty.md 업데이트(#13217)</span><span class="sxs-lookup"><span data-stu-id="6783d-252">@kongou-ae, Update New-AzOffice365PolicyProperty.md (#13217)</span></span>
* <span data-ttu-id="6783d-253">Lohith Chowdary Chilukuri(@Lochiluk), Set-AzApplicationGateway.md 업데이트(#13150)</span><span class="sxs-lookup"><span data-stu-id="6783d-253">Lohith Chowdary Chilukuri (@Lochiluk), Update Set-AzApplicationGateway.md (#13150)</span></span>
* <span data-ttu-id="6783d-254">Matthew Burleigh(@mburleigh)</span><span class="sxs-lookup"><span data-stu-id="6783d-254">Matthew Burleigh (@mburleigh)</span></span>
  * <span data-ttu-id="6783d-255">문서에서 참조된 PowerShell cmdlet에 대한 링크 추가(#13203)</span><span class="sxs-lookup"><span data-stu-id="6783d-255">Add links to PowerShell cmdlets referenced in the document (#13203)</span></span>
  * <span data-ttu-id="6783d-256">문서에서 참조된 PowerShell cmdlet에 대한 링크 추가(#13190)</span><span class="sxs-lookup"><span data-stu-id="6783d-256">Add links to PowerShell cmdlets referenced in the document (#13190)</span></span>
  * <span data-ttu-id="6783d-257">문서에서 참조된 PowerShell cmdlet에 대한 링크 추가(#13189)</span><span class="sxs-lookup"><span data-stu-id="6783d-257">Add links to PowerShell cmdlets referenced in the document (#13189)</span></span>
  * <span data-ttu-id="6783d-258">참조된 cmdlet에 대한 링크 추가(#13137)</span><span class="sxs-lookup"><span data-stu-id="6783d-258">add links to referenced cmdlets (#13137)</span></span>
  * <span data-ttu-id="6783d-259">문서에서 참조된 PowerShell cmdlet에 대한 링크 추가(#13204)</span><span class="sxs-lookup"><span data-stu-id="6783d-259">Add links to PowerShell cmdlets referenced in the document (#13204)</span></span>
  * <span data-ttu-id="6783d-260">문서에서 참조된 PowerShell cmdlet에 대한 링크 추가(#13205)</span><span class="sxs-lookup"><span data-stu-id="6783d-260">Add links to PowerShell cmdlets referenced in the document (#13205)</span></span>

## <a name="480---october-2020"></a><span data-ttu-id="6783d-261">4.8.0 - 2020년 10월</span><span class="sxs-lookup"><span data-stu-id="6783d-261">4.8.0 - October 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="6783d-262">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6783d-262">Az.Accounts</span></span>
* <span data-ttu-id="6783d-263">공용 라이브러리의 DateTime 구문 분석 문제 해결[#13045]</span><span class="sxs-lookup"><span data-stu-id="6783d-263">Fixed DateTime parse issue in common libraries [#13045]</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="6783d-264">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="6783d-264">Az.CognitiveServices</span></span>
* <span data-ttu-id="6783d-265">'New-AzCognitiveServicesAccountApiProperty' cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-265">Added 'New-AzCognitiveServicesAccountApiProperty' cmdlet.</span></span>
* <span data-ttu-id="6783d-266">'New-AzCognitiveServicesAccount' 및 'Set-AzCognitiveServicesAccount'에 대해 'ApiProperty' 매개 변수 지원됨</span><span class="sxs-lookup"><span data-stu-id="6783d-266">Supported 'ApiProperty' parameter for 'New-AzCognitiveServicesAccount' and 'Set-AzCognitiveServicesAccount'</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6783d-267">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6783d-267">Az.Compute</span></span>
* <span data-ttu-id="6783d-268">FailoverTypes를 채워서 'Update-ASRRecoveryPlan'의 문제 해결</span><span class="sxs-lookup"><span data-stu-id="6783d-268">Fixed issue in 'Update-ASRRecoveryPlan' by populating FailoverTypes</span></span>
* <span data-ttu-id="6783d-269">'Get-AzVmImage' cmdlet에 '-Top' 및 '-OrderBy' 선택적 매개 변수를 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-269">Added the '-Top' and '-OrderBy' optional parameters to the 'Get-AzVmImage' cmdlet.</span></span> 

#### <a name="azdatabricks"></a><span data-ttu-id="6783d-270">Az.Databricks</span><span class="sxs-lookup"><span data-stu-id="6783d-270">Az.Databricks</span></span>
* <span data-ttu-id="6783d-271">'Az.Databricks' 모듈의 일반 공급</span><span class="sxs-lookup"><span data-stu-id="6783d-271">General availability of 'Az.Databricks' module</span></span>
* <span data-ttu-id="6783d-272">가상 네트워크 피어링에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="6783d-272">Added support for virtual network peering</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="6783d-273">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="6783d-273">Az.DataFactory</span></span>
* <span data-ttu-id="6783d-274">출력 메시지의 오타 수정</span><span class="sxs-lookup"><span data-stu-id="6783d-274">Fixed typo in output messages</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="6783d-275">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="6783d-275">Az.EventHub</span></span>
* <span data-ttu-id="6783d-276">선택적 스위치 매개 변수 'TrustedServiceAccessEnabled'를 'Set-AzEventHubNetworkRuleSet' cmdlet에 추가</span><span class="sxs-lookup"><span data-stu-id="6783d-276">Added optional switch parameter 'TrustedServiceAccessEnabled' to 'Set-AzEventHubNetworkRuleSet' cmdlet</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="6783d-277">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="6783d-277">Az.HDInsight</span></span>
* <span data-ttu-id="6783d-278">'PublicNetworkAccessType' 및 'OutboundPublicNetworkAccessType' 매개 변수 사용 중단 계획에 대한 경고 메시지 추가</span><span class="sxs-lookup"><span data-stu-id="6783d-278">Added warning message for planning to deprecate the parameters 'PublicNetworkAccessType' and 'OutboundPublicNetworkAccessType'</span></span>
* <span data-ttu-id="6783d-279">'DefaultStorageAccountName' 매개 변수를 'StorageAccountResourceId'로 바꾸려는 계획에 대한 경고 메시지 추가</span><span class="sxs-lookup"><span data-stu-id="6783d-279">Added warning message for planning to replace the parameter 'DefaultStorageAccountName' with 'StorageAccountResourceId'</span></span>
* <span data-ttu-id="6783d-280">'DefaultStorageAccountKey' 매개 변수를 'StorageAccountKey'로 바꾸려는 계획에 대한 경고 메시지 추가</span><span class="sxs-lookup"><span data-stu-id="6783d-280">Added warning message for planning to replace the parameter 'DefaultStorageAccountKey' with 'StorageAccountKey'</span></span>
* <span data-ttu-id="6783d-281">'DefaultStorageAccountType' 매개 변수를 'StorageAccountType'으로 바꾸려는 계획에 대한 경고 메시지 추가</span><span class="sxs-lookup"><span data-stu-id="6783d-281">Added warning message for planning to replace the parameter 'DefaultStorageAccountType' with 'StorageAccountType'</span></span>
* <span data-ttu-id="6783d-282">'DefaultStorageContainer' 매개 변수를 'StorageContainer'로 바꾸려는 계획에 대한 경고 메시지 추가</span><span class="sxs-lookup"><span data-stu-id="6783d-282">Added warning message for planning to replace the parameter 'DefaultStorageContainer' with 'StorageContainer'</span></span>
* <span data-ttu-id="6783d-283">'DefaultStorageRootPath' 매개 변수를 'StorageRootPath'로 바꾸려는 계획에 대한 경고 메시지 추가</span><span class="sxs-lookup"><span data-stu-id="6783d-283">Added warning message for planning to replace the parameter 'DefaultStorageRootPath' with 'StorageRootPath'</span></span>

#### <a name="aziothub"></a><span data-ttu-id="6783d-284">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="6783d-284">Az.IotHub</span></span>
* <span data-ttu-id="6783d-285">업데이트된 디바이스 SDK.</span><span class="sxs-lookup"><span data-stu-id="6783d-285">Updated devices sdk.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="6783d-286">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="6783d-286">Az.KeyVault</span></span>
* <span data-ttu-id="6783d-287">SecretValueText 속성 제거 세부 날짜 제공</span><span class="sxs-lookup"><span data-stu-id="6783d-287">Provided the detailed date of removing property SecretValueText</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="6783d-288">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="6783d-288">Az.ManagedServices</span></span>
* <span data-ttu-id="6783d-289">관리되는 서비스 할당 및 정의의 cmdlet에 대한 호환성이 손상되는 변경 경고가 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="6783d-289">Updated breaking change warnings on cmdlets of managed services assignment and definition</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="6783d-290">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="6783d-290">Az.Monitor</span></span>
* <span data-ttu-id="6783d-291">경고 메시지를 숨길 수 없는 버그를 수정했습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-291">Fixed the bug that warning message cannot be suppressed.</span></span> <span data-ttu-id="6783d-292">[#12889]</span><span class="sxs-lookup"><span data-stu-id="6783d-292">[#12889]</span></span>
* <span data-ttu-id="6783d-293">경고 규칙 기준에서 'SkipMetricValidation' 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-293">Supported 'SkipMetricValidation' parameter in alert rule criteria.</span></span> <span data-ttu-id="6783d-294">메트릭 유효성 검사를 건너뛰도록 하여 아직 생성되지 않은 사용자 지정 메트릭에 대한 경고 규칙을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-294">Allows creating an alert rule on a custom metric that isn't yet emitted, by causing the metric validation to be skipped.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6783d-295">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6783d-295">Az.Network</span></span>
* <span data-ttu-id="6783d-296">VPNSite 리소스에 Office365 정책 추가</span><span class="sxs-lookup"><span data-stu-id="6783d-296">Added Office365 Policy to VPNSite Resource</span></span>
    - <span data-ttu-id="6783d-297">'New-AzO365PolicyProperty'</span><span class="sxs-lookup"><span data-stu-id="6783d-297">'New-AzO365PolicyProperty'</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="6783d-298">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="6783d-298">Az.RecoveryServices</span></span>
* <span data-ttu-id="6783d-299">워크로드 백업에 대한 컨테이너 이름 유효성 검사가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-299">Added container name validation for workload backup.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="6783d-300">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="6783d-300">Az.RedisCache</span></span>
* <span data-ttu-id="6783d-301">Microsoft.Cache RP 등록과 관련된 권한 문제로 인해 'New-AzRedisCache' 및 'Set-AzRedisCache' cmdlet이 실패하지 않도록 함</span><span class="sxs-lookup"><span data-stu-id="6783d-301">Made 'New-AzRedisCache' and 'Set-AzRedisCache' cmdlets not fail because of permission issue related to registering Microsoft.Cache RP</span></span>

#### <a name="azsql"></a><span data-ttu-id="6783d-302">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6783d-302">Az.Sql</span></span>
* <span data-ttu-id="6783d-303">BackupStorageRedundancy가 다음에 추가됨</span><span class="sxs-lookup"><span data-stu-id="6783d-303">Added BackupStorageRedundancy to the following:</span></span> 
    - <span data-ttu-id="6783d-304">'Restore-AzureRmSqlDatabase'</span><span class="sxs-lookup"><span data-stu-id="6783d-304">'Restore-AzureRmSqlDatabase'</span></span>
    - <span data-ttu-id="6783d-305">'New-AzSqlDatabaseCopy'</span><span class="sxs-lookup"><span data-stu-id="6783d-305">'New-AzSqlDatabaseCopy'</span></span>
    - <span data-ttu-id="6783d-306">'New-AzSqlDatabaseSecondary'</span><span class="sxs-lookup"><span data-stu-id="6783d-306">'New-AzSqlDatabaseSecondary'</span></span>
* <span data-ttu-id="6783d-307">모든 SQL DB 참조에 대한 BackupStorageRedundancy 매개 변수의 대소문자 구분 제거</span><span class="sxs-lookup"><span data-stu-id="6783d-307">Removed case sensitivity for BackupStorageRedundancy parameter for all SQL DB references</span></span> 
* <span data-ttu-id="6783d-308">BackupStorageRedundancy 경고 메시지 이름 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="6783d-308">Updated BackupStorageRedundancy warning message names</span></span>

#### <a name="azstorage"></a><span data-ttu-id="6783d-309">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="6783d-309">Az.Storage</span></span>
* <span data-ttu-id="6783d-310">스토리지 계정의 파일 서비스에서 사용/사용하지 않음/공유 일시 삭제 속성 지원</span><span class="sxs-lookup"><span data-stu-id="6783d-310">Supported enable/disable/get share soft delete properties on file Service of a Storage account</span></span>
    - <span data-ttu-id="6783d-311">'Update-AzStorageFileServiceProperty'</span><span class="sxs-lookup"><span data-stu-id="6783d-311">'Update-AzStorageFileServiceProperty'</span></span>
    - <span data-ttu-id="6783d-312">'Get-AzStorageFileServiceProperty'</span><span class="sxs-lookup"><span data-stu-id="6783d-312">'Get-AzStorageFileServiceProperty'</span></span>
* <span data-ttu-id="6783d-313">지원되는 목록 파일 공유에는 스토리지 계정의 삭제된 공유와 단일 파일 공유 사용량 가져오기가 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-313">Supported list file shares include the deleted ones of a Storage account, and Get single file share usage</span></span>
    - <span data-ttu-id="6783d-314">'Get-AzRmStorageShare'</span><span class="sxs-lookup"><span data-stu-id="6783d-314">'Get-AzRmStorageShare'</span></span>
* <span data-ttu-id="6783d-315">삭제된 파일 공유 복원 지원</span><span class="sxs-lookup"><span data-stu-id="6783d-315">Supported restore a deleted file share</span></span>
    - <span data-ttu-id="6783d-316">'Restore-AzRmStorageShare'</span><span class="sxs-lookup"><span data-stu-id="6783d-316">'Restore-AzRmStorageShare'</span></span>
* <span data-ttu-id="6783d-317">Blob 서비스 속성을 수정하기 위한 cmdlet을 변경하여, 서버에서 원래 속성을 가져오지 않으며 수정된 속성만 서버로 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-317">Changed the cmdlets for modify blob service properties, won't get the original properties from server, but only set the modified properties to server.</span></span>
    - <span data-ttu-id="6783d-318">'Enable-AzStorageBlobDeleteRetentionPolicy'</span><span class="sxs-lookup"><span data-stu-id="6783d-318">'Enable-AzStorageBlobDeleteRetentionPolicy'</span></span>
    - <span data-ttu-id="6783d-319">'Disable-AzStorageBlobDeleteRetentionPolicy'</span><span class="sxs-lookup"><span data-stu-id="6783d-319">'Disable-AzStorageBlobDeleteRetentionPolicy'</span></span>  
    - <span data-ttu-id="6783d-320">'Enable-AzStorageBlobRestorePolicy'</span><span class="sxs-lookup"><span data-stu-id="6783d-320">'Enable-AzStorageBlobRestorePolicy'</span></span>
    - <span data-ttu-id="6783d-321">'Disable-AzStorageBlobRestorePolicy'</span><span class="sxs-lookup"><span data-stu-id="6783d-321">'Disable-AzStorageBlobRestorePolicy'</span></span>
    - <span data-ttu-id="6783d-322">'Update-AzStorageBlobServiceProperty'</span><span class="sxs-lookup"><span data-stu-id="6783d-322">'Update-AzStorageBlobServiceProperty'</span></span>
* <span data-ttu-id="6783d-323">New-AzStorageAccount 매개 변수 -Kind 기본값에 대한 도움말 문제 해결[#12189]</span><span class="sxs-lookup"><span data-stu-id="6783d-323">Fixed help issue for New-AzStorageAccount parameter -Kind default value [#12189]</span></span>
* <span data-ttu-id="6783d-324">Blob 업로드에서 올바른 ContentType을 설정하는 방법을 보여주는 예제를 추가하여 문제 해결[#12989]</span><span class="sxs-lookup"><span data-stu-id="6783d-324">Fixed issue by add example to show how to set correct ContentType in blob upload [#12989]</span></span>

## <a name="470---september-2020"></a><span data-ttu-id="6783d-325">4.7.0 - 2020년 9월</span><span class="sxs-lookup"><span data-stu-id="6783d-325">4.7.0 - September 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="6783d-326">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6783d-326">Az.Accounts</span></span>
* <span data-ttu-id="6783d-327">예정된 호환성이 손상되는 변경 메시지의 형식이 지정됨</span><span class="sxs-lookup"><span data-stu-id="6783d-327">Formatted the upcoming breaking change messages</span></span>
* <span data-ttu-id="6783d-328">Azure.Core가 1.4.1로 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="6783d-328">Updated Azure.Core to 1.4.1</span></span>

#### <a name="azaks"></a><span data-ttu-id="6783d-329">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="6783d-329">Az.Aks</span></span>
* <span data-ttu-id="6783d-330">'New-AzAksCluster', 'Set-AzAksCluster' 및 'New-AzAksNodePool'에 대한 클라이언트 쪽 매개 변수 유효성 검사 논리가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-330">Added client side parameter validation logic for 'New-AzAksCluster', 'Set-AzAksCluster' and 'New-AzAksNodePool'.</span></span> <span data-ttu-id="6783d-331">[#12372]</span><span class="sxs-lookup"><span data-stu-id="6783d-331">[#12372]</span></span>
* <span data-ttu-id="6783d-332">'New-AzAksCluster'에서 추가 항목에 대한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-332">Added support for add-ons in 'New-AzAksCluster'.</span></span> <span data-ttu-id="6783d-333">[#11239]</span><span class="sxs-lookup"><span data-stu-id="6783d-333">[#11239]</span></span>
* <span data-ttu-id="6783d-334">추가 항목에 대한 'Enable-AzAksAddOn' 및 'Disable-AzAksAddOn' cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-334">Added cmdlets 'Enable-AzAksAddOn' and 'Disable-AzAksAddOn' for add-ons.</span></span> <span data-ttu-id="6783d-335">[#11239]</span><span class="sxs-lookup"><span data-stu-id="6783d-335">[#11239]</span></span>
* <span data-ttu-id="6783d-336">'New-AzAksCluster'에 대한 매개 변수 'GenerateSshKey'가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-336">Added parameter 'GenerateSshKey' for 'New-AzAksCluster'.</span></span> <span data-ttu-id="6783d-337">[#12371]</span><span class="sxs-lookup"><span data-stu-id="6783d-337">[#12371]</span></span>
* <span data-ttu-id="6783d-338">API 버전이 2020-06-01로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-338">Updated api version to 2020-06-01.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="6783d-339">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="6783d-339">Az.CognitiveServices</span></span>
* <span data-ttu-id="6783d-340">특정 API에 대한 추가 법률 용어를 표시했습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-340">Showed additional legal terms for certain APIs.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6783d-341">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6783d-341">Az.Compute</span></span>
* <span data-ttu-id="6783d-342">'New-AzVmDiskEncryptionSetConfig'에 '-EncryptionType' 선택적 매개 변수가 추가됨</span><span class="sxs-lookup"><span data-stu-id="6783d-342">Added the '-EncryptionType' optional parameter to 'New-AzVmDiskEncryptionSetConfig'</span></span>
* <span data-ttu-id="6783d-343">새 리소스 종류에 대한 새 cmdlet: DiskAccess 'Get-AzDiskAccess', 'New-AzDiskAccess', 'Get-AzDiskAccess'</span><span class="sxs-lookup"><span data-stu-id="6783d-343">New cmdlets for new resource type: DiskAccess 'Get-AzDiskAccess', 'New-AzDiskAccess', 'Get-AzDiskAccess'</span></span>
* <span data-ttu-id="6783d-344">'New-AzSnapshotConfig'에 선택적 매개 변수 '-DiskAccessId' 및 '-NetworkAccessPolicy'가 추가됨</span><span class="sxs-lookup"><span data-stu-id="6783d-344">Added optional parameters '-DiskAccessId' and '-NetworkAccessPolicy' to 'New-AzSnapshotConfig'</span></span>
* <span data-ttu-id="6783d-345">'New-AzDiskConfig'에 선택적 매개 변수 '-DiskAccessId' 및 '-NetworkAccessPolicy'가 추가됨</span><span class="sxs-lookup"><span data-stu-id="6783d-345">Added optional parameters '-DiskAccessId' and '-NetworkAccessPolicy' to 'New-AzDiskConfig'</span></span>
* <span data-ttu-id="6783d-346">VirtualMachine 인스턴스 보기에 'PatchStatus' 속성이 추가됨</span><span class="sxs-lookup"><span data-stu-id="6783d-346">Added 'PatchStatus' property to VirtualMachine Instance View</span></span>
* <span data-ttu-id="6783d-347">가상 머신의 인스턴스 보기에 'VMHealth' 속성이 추가됨. 이 속성은 'Get-AzVm'이 '-Status'로 호출될 때 반환되는 개체</span><span class="sxs-lookup"><span data-stu-id="6783d-347">Added 'VMHealth' property to the virtual machine's instance view, which is the returned object when 'Get-AzVm' is invoked with '-Status'</span></span>
* <span data-ttu-id="6783d-348">'Get-AzVM' 및 'Get-AzVmss' 인스턴스 보기에 'AssignedHost' 필드가 추가됨</span><span class="sxs-lookup"><span data-stu-id="6783d-348">Added 'AssignedHost' field to 'Get-AzVM' and 'Get-AzVmss' instance views.</span></span> <span data-ttu-id="6783d-349">필드는 가상 머신 인스턴스의 리소스 ID를 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-349">The field shows the resource id of the virtual machine instance</span></span>
* <span data-ttu-id="6783d-350">선택적 매개 변수 '-SupportAutomaticPlacement'가 'New-AzHostGroup'에 추가됨</span><span class="sxs-lookup"><span data-stu-id="6783d-350">Added optional parameter '-SupportAutomaticPlacement' to 'New-AzHostGroup'</span></span> 
* <span data-ttu-id="6783d-351">'-HostGroupId' 매개 변수가 'New-AzVm' 및 'New-AzVmss'에 추가됨</span><span class="sxs-lookup"><span data-stu-id="6783d-351">Added the '-HostGroupId' parameter to 'New-AzVm' and 'New-AzVmss'</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="6783d-352">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="6783d-352">Az.DataFactory</span></span>
* <span data-ttu-id="6783d-353">ADF .Net SDK 버전이 4.11.0으로 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="6783d-353">Updated ADF .Net SDK version to 4.11.0</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="6783d-354">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="6783d-354">Az.EventHub</span></span>
* <span data-ttu-id="6783d-355">새 클러스터 cmdlet 추가됨 - 'New-AzEventHubCluster', 'Set-AzEventHubCluster', 'Get-AzEventHubCluster', 'Remove-AzEventHubCluster', 'Get-AzEventHubClustersAvailableRegions'</span><span class="sxs-lookup"><span data-stu-id="6783d-355">Added new Cluster cmdlets - 'New-AzEventHubCluster', 'Set-AzEventHubCluster', 'Get-AzEventHubCluster', 'Remove-AzEventHubCluster', 'Get-AzEventHubClustersAvailableRegions'.</span></span>
* <span data-ttu-id="6783d-356">#10722 문제 해결됨: AuthorizationRule 권한에 'Listen'만 할당하는 문제가 해결되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-356">Fixed for issue #10722 : Fix for assigning only 'Listen' to AuthorizationRule rights.</span></span>

#### <a name="azfunctions"></a><span data-ttu-id="6783d-357">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="6783d-357">Az.Functions</span></span>
* <span data-ttu-id="6783d-358">v2 Functions를 지원하지 않는 지역에서 생성하는 기능이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-358">Removed the ability to create v2 Functions in regions that do not support it.</span></span>
* <span data-ttu-id="6783d-359">PowerShell 6.2가 사용되지 않음</span><span class="sxs-lookup"><span data-stu-id="6783d-359">Deprecated PowerShell 6.2.</span></span> <span data-ttu-id="6783d-360">사용자가 PowerShell 6.2 함수 앱을 만들 때 PowerShell 7.0 함수 앱을 만들도록 권장하는 경고가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-360">Added a warning for when a user creates a PowerShell 6.2 function app that advises them to create a PowerShell 7.0 function app instead.</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="6783d-361">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="6783d-361">Az.HDInsight</span></span>
* <span data-ttu-id="6783d-362">자동 크기 조정 구성을 사용하여 클러스터 만들기 지원</span><span class="sxs-lookup"><span data-stu-id="6783d-362">Supported creating cluster with Autoscale configuration</span></span>
    - <span data-ttu-id="6783d-363">cmdlet 'New-AzHDInsightCluster'에 새 매개 변수 'AutoscaleConfiguration' 추가</span><span class="sxs-lookup"><span data-stu-id="6783d-363">Add new parameter 'AutoscaleConfiguration' to the cmdlet 'New-AzHDInsightCluster'</span></span>
* <span data-ttu-id="6783d-364">운영 클러스터의 자동 크기 조정 구성 지원됨</span><span class="sxs-lookup"><span data-stu-id="6783d-364">Supported operating cluster's Autoscale configuration</span></span>
    - <span data-ttu-id="6783d-365">새 cmdlet 'Get-AzHDInsihgtClusterAutoscaleConfiguration' 추가</span><span class="sxs-lookup"><span data-stu-id="6783d-365">Add new cmdlet 'Get-AzHDInsihgtClusterAutoscaleConfiguration'</span></span>
    - <span data-ttu-id="6783d-366">새 cmdlet 'New-AzHDInsihgtClusterAutoscaleConfiguration' 추가</span><span class="sxs-lookup"><span data-stu-id="6783d-366">Add new cmdlet 'New-AzHDInsihgtClusterAutoscaleConfiguration'</span></span>
    - <span data-ttu-id="6783d-367">새 cmdlet 'Set-AzHDInsihgtClusterAutoscaleConfiguration' 추가</span><span class="sxs-lookup"><span data-stu-id="6783d-367">Add new cmdlet 'Set-AzHDInsihgtClusterAutoscaleConfiguration'</span></span>
    - <span data-ttu-id="6783d-368">새 cmdlet 'Remove-AzHDInsihgtClusterAutoscaleConfiguration' 추가</span><span class="sxs-lookup"><span data-stu-id="6783d-368">Add new cmdlet 'Remove-AzHDInsihgtClusterAutoscaleConfiguration'</span></span>
    - <span data-ttu-id="6783d-369">새 cmdlet 'New-AzHDInsihgtClusterAutoscaleScheduleCondition' 추가</span><span class="sxs-lookup"><span data-stu-id="6783d-369">Add new cmdlet 'New-AzHDInsihgtClusterAutoscaleScheduleCondition'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="6783d-370">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="6783d-370">Az.KeyVault</span></span>
* <span data-ttu-id="6783d-371">RBAC 권한 부여에 대한 지원 추가됨 [#10557]</span><span class="sxs-lookup"><span data-stu-id="6783d-371">Added support for RBAC authorization [#10557]</span></span>
* <span data-ttu-id="6783d-372">'Set-AzKeyVaultAccessPolicy'에서 향상된 오류 처리 [#4007]</span><span class="sxs-lookup"><span data-stu-id="6783d-372">Enhanced error handling in 'Set-AzKeyVaultAccessPolicy' [#4007]</span></span>

#### <a name="azkusto"></a><span data-ttu-id="6783d-373">Az.Kusto</span><span class="sxs-lookup"><span data-stu-id="6783d-373">Az.Kusto</span></span>
* <span data-ttu-id="6783d-374">'Az.Kusto' 모듈의 일반 공급</span><span class="sxs-lookup"><span data-stu-id="6783d-374">General availability of 'Az.Kusto' module</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6783d-375">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6783d-375">Az.Network</span></span>
* <span data-ttu-id="6783d-376">[호환성이 손상되는 변경] 리소스 가상 라우터 및 가상 허브에 맞게 아래 cmdlet이 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="6783d-376">[Breaking Change] Updated below cmdlets to align resource virtual router and virtual hub</span></span>
    - <span data-ttu-id="6783d-377">'New-AzVirtualRouter':</span><span class="sxs-lookup"><span data-stu-id="6783d-377">'New-AzVirtualRouter':</span></span> 
        - <span data-ttu-id="6783d-378">IP 구성 자식 리소스를 지원하는 -HostedSubnet 매개 변수가 추가됨</span><span class="sxs-lookup"><span data-stu-id="6783d-378">Added -HostedSubnet parameter to support IP configuration child resource</span></span>
        - <span data-ttu-id="6783d-379">-HostedGateway 및 -HostedGatewayId 삭제됨</span><span class="sxs-lookup"><span data-stu-id="6783d-379">deleted -HostedGateway and -HostedGatewayId</span></span>
    - <span data-ttu-id="6783d-380">'Get-AzVirtualRouter':</span><span class="sxs-lookup"><span data-stu-id="6783d-380">'Get-AzVirtualRouter':</span></span>
        - <span data-ttu-id="6783d-381">구독 수준 매개 변수 집합이 추가됨</span><span class="sxs-lookup"><span data-stu-id="6783d-381">Added subscription level parameter set</span></span>
    - <span data-ttu-id="6783d-382">'Remove-AzVirtualRouter'</span><span class="sxs-lookup"><span data-stu-id="6783d-382">'Remove-AzVirtualRouter'</span></span>
    - <span data-ttu-id="6783d-383">'Add-AzVirtualRouterPeer'</span><span class="sxs-lookup"><span data-stu-id="6783d-383">'Add-AzVirtualRouterPeer'</span></span>
    - <span data-ttu-id="6783d-384">'Get-AzVirtualRouterPeer'</span><span class="sxs-lookup"><span data-stu-id="6783d-384">'Get-AzVirtualRouterPeer'</span></span>
    - <span data-ttu-id="6783d-385">'Remove-AzVirtualRouterPeer'</span><span class="sxs-lookup"><span data-stu-id="6783d-385">'Remove-AzVirtualRouterPeer'</span></span>
* <span data-ttu-id="6783d-386">Azure Express 경로 포트에 대해 새 cmdlet이 추가됨</span><span class="sxs-lookup"><span data-stu-id="6783d-386">Added new cmdlet for Azure Express Route Port</span></span>
    - <span data-ttu-id="6783d-387">'New-AzExpressRoutePortLOA'</span><span class="sxs-lookup"><span data-stu-id="6783d-387">'New-AzExpressRoutePortLOA'</span></span>
* <span data-ttu-id="6783d-388">VirtualNetwork 피어링 리소스에 RemoteBgpCommunities 속성이 추가됨</span><span class="sxs-lookup"><span data-stu-id="6783d-388">Added RemoteBgpCommunities property to the VirtualNetwork Peering Resource</span></span>
* <span data-ttu-id="6783d-389">'New-AzLoadBalancerFrontendIpConfig', 'New-AzPublicIpAddress' 및 'New-AzPublicIpPrefix'에 대한 경고 메시지를 수정했습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-389">Modified the warning message for 'New-AzLoadBalancerFrontendIpConfig', 'New-AzPublicIpAddress' and 'New-AzPublicIpPrefix'.</span></span>
* <span data-ttu-id="6783d-390">'Get-AzVpnGateway' 출력에 VpnGatewayIpConfigurations가 추가됨</span><span class="sxs-lookup"><span data-stu-id="6783d-390">Added VpnGatewayIpConfigurations to 'Get-AzVpnGateway' output</span></span>
* <span data-ttu-id="6783d-391">'Set-AzApplicationGatewaySslCertificate'의 버그 수정됨 [#9488]</span><span class="sxs-lookup"><span data-stu-id="6783d-391">Fixed bug for 'Set-AzApplicationGatewaySslCertificate' [#9488]</span></span>
* <span data-ttu-id="6783d-392">'AzureFirewall'에 'AllowActiveFTP' 매개 변수가 추가됨</span><span class="sxs-lookup"><span data-stu-id="6783d-392">Added 'AllowActiveFTP' parameter to 'AzureFirewall'</span></span>
* <span data-ttu-id="6783d-393">기능에 대한 새로운 명령이 업데이트됨: VirtualWan P2SVpnGateway에서 인터넷 보안 설정 사용/제거</span><span class="sxs-lookup"><span data-stu-id="6783d-393">Updated below commands for feature: Enable internet security set/remove on VirtualWan P2SVpnGateway.</span></span>
- <span data-ttu-id="6783d-394">'New-AzP2sVpnGateway' 업데이트됨: 고객이 P2SVpnGateway에서 인터넷 보안을 사용하도록 true를 설정할 수 있는 선택적 스위치 매개 변수 'EnableInternetSecurityFlag'가 추가되었으며, 이는 지점 및 사이트 간 클라이언트에 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-394">Updated 'New-AzP2sVpnGateway': Added optional switch parameter 'EnableInternetSecurityFlag' for customers to set true to enable internet security on P2SVpnGateway, which will be applied for Point to site clients.</span></span>
- <span data-ttu-id="6783d-395">'Update-AzP2sVpnGateway' 업데이트됨: 고객이 P2SVpnGateway에서 인터넷 보안을 활성화/비활성화하도록 true/false를 설정할 수 있는 선택적 스위치 매개 변수 'EnableInternetSecurityFlag' 또는 'DisableInternetSecurityFlag'가 추가되었으며, 이는 지점 및 사이트 간 클라이언트에 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-395">Updated 'Update-AzP2sVpnGateway': Added optional switch parameters 'EnableInternetSecurityFlag' or 'DisableInternetSecurityFlag' for customers to set true/false to enable/disable internet security on P2SVpnGateway, which will be applied for Point to site clients.</span></span>
* <span data-ttu-id="6783d-396">문제 해결을 위해 VirtualWan P2SVPNGateway를 재설정/재부팅할 수 있도록 새 cmdlet 'Reset-AzP2sVpnGateway'를 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-396">Added new cmdlet 'Reset-AzP2sVpnGateway' for customers to reset/reboot their VirtualWan P2SVpnGateway for troubleshooting.</span></span>
* <span data-ttu-id="6783d-397">문제 해결을 위해 VirtualWan VpnGateway를 재설정/재부팅할 수 있도록 새 cmdlet 'Reset-AzVpnGateway'를 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-397">Added new cmdlet 'Reset-AzVpnGateway' for customers to reset/reboot their VirtualWan VpnGateway for troubleshooting.</span></span>
* <span data-ttu-id="6783d-398">'Set-AzVirtualNetworkSubnetConfig' 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="6783d-398">Updated 'Set-AzVirtualNetworkSubnetConfig'</span></span>
    - <span data-ttu-id="6783d-399">매개 변수에 명시적으로 설정된 경우 서브넷의 NSG 및 라우팅 테이블 속성을 null로 설정 [# 1548][# 9718]</span><span class="sxs-lookup"><span data-stu-id="6783d-399">Set NSG and Route Table properties of subnet to null if explicitly set in parameters [#1548][#9718]</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="6783d-400">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="6783d-400">Az.RecoveryServices</span></span>
* <span data-ttu-id="6783d-401">워크로드 백업 항목에 대한 삭제 상태가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-401">Fixed the Delete State for workload Backup Items.</span></span>

#### <a name="azresources"></a><span data-ttu-id="6783d-402">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6783d-402">Az.Resources</span></span>
* <span data-ttu-id="6783d-403">Set-AzRoleAssignment에 대한 누락된 검사 추가됨</span><span class="sxs-lookup"><span data-stu-id="6783d-403">Added missing check for Set-AzRoleAssignment</span></span>
* <span data-ttu-id="6783d-404">'Get-AzResourceGroupDeploymentOperation'의 'SubscriptionId' 매개 변수에 호환성이 손상되는 변경 특성이 추가됨</span><span class="sxs-lookup"><span data-stu-id="6783d-404">Added breaking change attribute to 'SubscriptionId' parameter of 'Get-AzResourceGroupDeploymentOperation'</span></span>
* <span data-ttu-id="6783d-405">마지막으로 'Ignore' 리소스 변경을 표시하도록 ARM 템플릿 What-If cmdlet이 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="6783d-405">Updated ARM template What-If cmdlets to show 'Ignore' resource changes last</span></span>
* <span data-ttu-id="6783d-406">배포 cmdlet에 대한 보안 및 배열 매개 변수 직렬화 문제가 해결됨 [#12773]</span><span class="sxs-lookup"><span data-stu-id="6783d-406">Fixed secure and array parameter serialization issues for deployment cmdlets [#12773]</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="6783d-407">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="6783d-407">Az.ServiceFabric</span></span>
* <span data-ttu-id="6783d-408">관리형 클러스터 및 노드 유형에 대해 다음과 같은 새 cmdlet가 추가됨</span><span class="sxs-lookup"><span data-stu-id="6783d-408">Added new cmdlets for managed clusters and node types:</span></span>
    - <span data-ttu-id="6783d-409">'New-AzServiceFabricManagedCluster'</span><span class="sxs-lookup"><span data-stu-id="6783d-409">'New-AzServiceFabricManagedCluster'</span></span>
    - <span data-ttu-id="6783d-410">'Get-AzServiceFabricManagedCluster'</span><span class="sxs-lookup"><span data-stu-id="6783d-410">'Get-AzServiceFabricManagedCluster'</span></span>
    - <span data-ttu-id="6783d-411">'Set-AzServiceFabricManagedCluster'</span><span class="sxs-lookup"><span data-stu-id="6783d-411">'Set-AzServiceFabricManagedCluster'</span></span>
    - <span data-ttu-id="6783d-412">'Remove-AzServiceFabricManagedCluster'</span><span class="sxs-lookup"><span data-stu-id="6783d-412">'Remove-AzServiceFabricManagedCluster'</span></span>
    - <span data-ttu-id="6783d-413">'Add-AzServiceFabricManagedClusterClientCertificate'</span><span class="sxs-lookup"><span data-stu-id="6783d-413">'Add-AzServiceFabricManagedClusterClientCertificate'</span></span>
    - <span data-ttu-id="6783d-414">'Remove-AzServiceFabricManagedClusterClientCertificate'</span><span class="sxs-lookup"><span data-stu-id="6783d-414">'Remove-AzServiceFabricManagedClusterClientCertificate'</span></span>
    - <span data-ttu-id="6783d-415">'New-AzServiceFabricManagedNodeType'</span><span class="sxs-lookup"><span data-stu-id="6783d-415">'New-AzServiceFabricManagedNodeType'</span></span>
    - <span data-ttu-id="6783d-416">'Get-AzServiceFabricManagedNodeType'</span><span class="sxs-lookup"><span data-stu-id="6783d-416">'Get-AzServiceFabricManagedNodeType'</span></span>
    - <span data-ttu-id="6783d-417">'Set-AzServiceFabricManagedNodeType'</span><span class="sxs-lookup"><span data-stu-id="6783d-417">'Set-AzServiceFabricManagedNodeType'</span></span>
    - <span data-ttu-id="6783d-418">'Remove-AzServiceFabricManagedNodeType'</span><span class="sxs-lookup"><span data-stu-id="6783d-418">'Remove-AzServiceFabricManagedNodeType'</span></span>
    - <span data-ttu-id="6783d-419">'Add-AzServiceFabricManagedNodeTypeVMExtension'</span><span class="sxs-lookup"><span data-stu-id="6783d-419">'Add-AzServiceFabricManagedNodeTypeVMExtension'</span></span>
    - <span data-ttu-id="6783d-420">'Add-AzServiceFabricManagedNodeTypeVMSecret'</span><span class="sxs-lookup"><span data-stu-id="6783d-420">'Add-AzServiceFabricManagedNodeTypeVMSecret'</span></span>
    - <span data-ttu-id="6783d-421">'Remove-AzServiceFabricManagedNodeTypeVMExtension'</span><span class="sxs-lookup"><span data-stu-id="6783d-421">'Remove-AzServiceFabricManagedNodeTypeVMExtension'</span></span>
    - <span data-ttu-id="6783d-422">'Restart-AzServiceFabricManagedNodeTyp'</span><span class="sxs-lookup"><span data-stu-id="6783d-422">'Restart-AzServiceFabricManagedNodeTyp'</span></span>
* <span data-ttu-id="6783d-423">Service Fabric SDK를 버전 1.2.0으로 업그레이드했으며, 현재 모델에서는 서비스 패브릭 리소스 제공자 api-version 2020-03-01을, 관리형 클러스터에서는 2020-01-01-preview를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-423">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2020-03-01 for the current model and 2020-01-01-preview for managed clusters.</span></span>

#### <a name="azsql"></a><span data-ttu-id="6783d-424">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6783d-424">Az.Sql</span></span>
* <span data-ttu-id="6783d-425">BackupStorageRedundancy가 'New-AzSqlInstance' 및 'Get-AzSqlInstance'에 추가됨</span><span class="sxs-lookup"><span data-stu-id="6783d-425">Added BackupStorageRedundancy to 'New-AzSqlInstance' and 'Get-AzSqlInstance'</span></span>
* <span data-ttu-id="6783d-426">'Get-AzSqlServerActiveDirectoryOnlyAuthentication' cmdlet이 추가됨</span><span class="sxs-lookup"><span data-stu-id="6783d-426">Added cmdlet 'Get-AzSqlServerActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="6783d-427">'Enable-AzSqlServerActiveDirectoryOnlyAuthentication' cmdlet이 추가됨</span><span class="sxs-lookup"><span data-stu-id="6783d-427">Added cmdlet 'Enable-AzSqlServerActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="6783d-428">Force 매개 변수가 'New-AzSqlInstance'에 추가됨</span><span class="sxs-lookup"><span data-stu-id="6783d-428">Added Force parameter to 'New-AzSqlInstance'</span></span>
* <span data-ttu-id="6783d-429">관리되는 데이터베이스 로그 재생 서비스용 cmdlet이 추가됨</span><span class="sxs-lookup"><span data-stu-id="6783d-429">Added cmdlets for Managed Database Log Replay service</span></span>
    - <span data-ttu-id="6783d-430">'Start-AzSqlInstanceDatabaseLogReplay'</span><span class="sxs-lookup"><span data-stu-id="6783d-430">'Start-AzSqlInstanceDatabaseLogReplay'</span></span>
    - <span data-ttu-id="6783d-431">'Get-AzSqlInstanceDatabaseLogReplay'</span><span class="sxs-lookup"><span data-stu-id="6783d-431">'Get-AzSqlInstanceDatabaseLogReplay'</span></span>
    - <span data-ttu-id="6783d-432">'Complete-AzSqlInstanceDatabaseLogReplay'</span><span class="sxs-lookup"><span data-stu-id="6783d-432">'Complete-AzSqlInstanceDatabaseLogReplay'</span></span>
    - <span data-ttu-id="6783d-433">'Stop-AzSqlInstanceDatabaseLogReplay'</span><span class="sxs-lookup"><span data-stu-id="6783d-433">'Stop-AzSqlInstanceDatabaseLogReplay'</span></span>
* <span data-ttu-id="6783d-434">'Get-AzSqlInstanceActiveDirectoryOnlyAuthentication' cmdlet이 추가됨</span><span class="sxs-lookup"><span data-stu-id="6783d-434">Added cmdlet 'Get-AzSqlInstanceActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="6783d-435">'Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication' cmdlet이 추가됨</span><span class="sxs-lookup"><span data-stu-id="6783d-435">Added cmdlet 'Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="6783d-436">'Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication' cmdlet이 추가됨</span><span class="sxs-lookup"><span data-stu-id="6783d-436">Added cmdlet 'Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="6783d-437">네트워크 격리 기능을 지원하기 위해 'New-AzSqlDatabaseImport' 및 'New-AzSqlDatabaseExport' cmdlet이 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="6783d-437">Updated cmdlets 'New-AzSqlDatabaseImport' and 'New-AzSqlDatabaseExport' to support network isolation functionality</span></span>
* <span data-ttu-id="6783d-438">'New-AzSqlDatabaseImportExisting' cmdlet이 추가됨</span><span class="sxs-lookup"><span data-stu-id="6783d-438">Added cmdlet 'New-AzSqlDatabaseImportExisting'</span></span>
* <span data-ttu-id="6783d-439">백업 스토리지 유형 사양을 지원하도록 데이터베이스 cmdlet이 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="6783d-439">Updated Databases cmdlets to support backup storage type specification</span></span>
* <span data-ttu-id="6783d-440">Force 매개 변수가 'New-AzSqlDatabase'에 추가됨</span><span class="sxs-lookup"><span data-stu-id="6783d-440">Added Force parameter to 'New-AzSqlDatabase'</span></span>
* <span data-ttu-id="6783d-441">'New-AzSqlDatabase'의 영역 선택에서 BackupStorageRedundancy 구성에 대한 경고가 추가됨</span><span class="sxs-lookup"><span data-stu-id="6783d-441">Added warning for BackupStorageRedundancy configuration in select regions in 'New-AzSqlDatabase'</span></span>
* <span data-ttu-id="6783d-442">ResourceId 및 InputObject를 포함하도록 서버 및 인스턴스에 대한 ActiveDirectoryOnlyAuthentication cmdlet이 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="6783d-442">Updated ActiveDirectoryOnlyAuthentication cmdlets for server and instance to include ResourceId and InputObject</span></span>

#### <a name="azstorage"></a><span data-ttu-id="6783d-443">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="6783d-443">Az.Storage</span></span>
* <span data-ttu-id="6783d-444">Microsoft.Azure.Storage.DataMovement 2.0.0로 업그레이드하여 blob 업로드 실패 수정됨 [#12220]</span><span class="sxs-lookup"><span data-stu-id="6783d-444">Fixed upload blob fail by upgrade to Microsoft.Azure.Storage.DataMovement 2.0.0 [#12220]</span></span>
* <span data-ttu-id="6783d-445">지정 시간 복원 지원</span><span class="sxs-lookup"><span data-stu-id="6783d-445">Supported Point In Time Restore</span></span>
    - <span data-ttu-id="6783d-446">'Enable-AzStorageBlobRestorePolicy'</span><span class="sxs-lookup"><span data-stu-id="6783d-446">'Enable-AzStorageBlobRestorePolicy'</span></span>
    - <span data-ttu-id="6783d-447">'Disable-AzStorageBlobRestorePolicy'</span><span class="sxs-lookup"><span data-stu-id="6783d-447">'Disable-AzStorageBlobRestorePolicy'</span></span>
    - <span data-ttu-id="6783d-448">'New-AzStorageBlobRangeToRestore'</span><span class="sxs-lookup"><span data-stu-id="6783d-448">'New-AzStorageBlobRangeToRestore'</span></span>
    - <span data-ttu-id="6783d-449">'Restore-AzStorageBlobRange'</span><span class="sxs-lookup"><span data-stu-id="6783d-449">'Restore-AzStorageBlobRange'</span></span>
* <span data-ttu-id="6783d-450">-IncludeBlobRestoreStatus 매개 변수와 함께 get-AzureRMStorageAccount를 실행하여 스토리지 계정의 blob 복원 상태 가져오기 지원</span><span class="sxs-lookup"><span data-stu-id="6783d-450">Supported get blob restore status of Storage account by run get-AzureRMStorageAccount with parameter -IncludeBlobRestoreStatus</span></span> 
    - <span data-ttu-id="6783d-451">'Get-AzureRMStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="6783d-451">'Get-AzureRMStorageAccount'</span></span>
* <span data-ttu-id="6783d-452">예정된 cmdlet 출력 변경에 대해 호환성이 손상되는 변경 경고 메시지가 추가됨</span><span class="sxs-lookup"><span data-stu-id="6783d-452">Added breaking change warning message for upcoming cmdlet output change</span></span>
    - <span data-ttu-id="6783d-453">'Get-AzStorageContainerStoredAccessPolicy'</span><span class="sxs-lookup"><span data-stu-id="6783d-453">'Get-AzStorageContainerStoredAccessPolicy'</span></span>
    - <span data-ttu-id="6783d-454">'Set-AzStorageContainerStoredAccessPolicy'</span><span class="sxs-lookup"><span data-stu-id="6783d-454">'Set-AzStorageContainerStoredAccessPolicy'</span></span>
    - <span data-ttu-id="6783d-455">'Set-AzStorageAccountManagementPolicy'</span><span class="sxs-lookup"><span data-stu-id="6783d-455">'Set-AzStorageAccountManagementPolicy'</span></span>
    - <span data-ttu-id="6783d-456">'Get-AzStorageAccountManagementPolicy'</span><span class="sxs-lookup"><span data-stu-id="6783d-456">'Get-AzStorageAccountManagementPolicy'</span></span>
    - <span data-ttu-id="6783d-457">'Add-AzStorageAccountManagementPolicyAction'</span><span class="sxs-lookup"><span data-stu-id="6783d-457">'Add-AzStorageAccountManagementPolicyAction'</span></span>
    - <span data-ttu-id="6783d-458">'New-AzStorageAccountManagementPolicyRule'</span><span class="sxs-lookup"><span data-stu-id="6783d-458">'New-AzStorageAccountManagementPolicyRule'</span></span>
* <span data-ttu-id="6783d-459">Microsoft.Azure.Cosmos.Table SDK를 1.0.8로 업그레이드</span><span class="sxs-lookup"><span data-stu-id="6783d-459">Upgraded Microsoft.Azure.Cosmos.Table SDK to 1.0.8</span></span>

### <a name="thanks-to-our-community-contributors"></a><span data-ttu-id="6783d-460">커뮤니티 기여자에게 감사드립니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-460">Thanks to our community contributors</span></span>
* <span data-ttu-id="6783d-461">Thomas Van Laere(@ThomVanL), Dockerfile-alpine-3.10 추가(#12911)</span><span class="sxs-lookup"><span data-stu-id="6783d-461">Thomas Van Laere (@ThomVanL), Add Dockerfile-alpine-3.10 (#12911)</span></span> 
* <span data-ttu-id="6783d-462">Lohith Chowdary Chilukuri(@Lochiluk), Remove-AzNetworkInterfaceIpConfig.md 업데이트(#12807)</span><span class="sxs-lookup"><span data-stu-id="6783d-462">Lohith Chowdary Chilukuri (@Lochiluk), Update Remove-AzNetworkInterfaceIpConfig.md (#12807)</span></span> 
* <span data-ttu-id="6783d-463">Roberth Strand(@roberthstrand), Get-AzResourceGroup - 새로운 예제 및 정리(#12828)</span><span class="sxs-lookup"><span data-stu-id="6783d-463">Roberth Strand (@roberthstrand), Get-AzResourceGroup - New example, and cleanup (#12828)</span></span> 
* <span data-ttu-id="6783d-464">Ravi Mishra(@inmishrar), Azure 웹앱 런타임 스택을 DOTNETCORE로 업데이트(#12833)</span><span class="sxs-lookup"><span data-stu-id="6783d-464">Ravi Mishra (@inmishrar), update Azure Web App runtime stack to DOTNETCORE (#12833)</span></span> 
* <span data-ttu-id="6783d-465">@jack-education, NSG 및 라우팅 테이블을 서브넷에서 제거할 수 있도록 Set-AzVirtualNetworkSubnetConfig를 업데이트(# 12351)</span><span class="sxs-lookup"><span data-stu-id="6783d-465">@jack-education, Updated Set-AzVirtualNetworkSubnetConfig to allow NSG and Route Table to be removed from subnet (#12351)</span></span> 
* <span data-ttu-id="6783d-466">@hagop-globanet, Add-AzApplicationGatewayCustomError.md 업데이트(#12784)</span><span class="sxs-lookup"><span data-stu-id="6783d-466">@hagop-globanet, Update Add-AzApplicationGatewayCustomError.md (#12784)</span></span> 
* <span data-ttu-id="6783d-467">Joshua Van Daalen(@greenSacrifice)</span><span class="sxs-lookup"><span data-stu-id="6783d-467">Joshua Van Daalen (@greenSacrifice)</span></span>
  * <span data-ttu-id="6783d-468">속성(Property) 철자를 속성(Property)으로 업데이트(#12821)</span><span class="sxs-lookup"><span data-stu-id="6783d-468">Update spelling of Property to Property (#12821)</span></span> 
  * <span data-ttu-id="6783d-469">New-AzResourceLock.md 예제 업데이트(#12806)</span><span class="sxs-lookup"><span data-stu-id="6783d-469">Update New-AzResourceLock.md examples (#12806)</span></span>
* <span data-ttu-id="6783d-470">Eragon Riddle(@eragonriddle), 예제에서 매개 변수 필드 이름 수정(#12825)</span><span class="sxs-lookup"><span data-stu-id="6783d-470">Eragon Riddle (@eragonriddle), Corrected parameter field name in the example (#12825)</span></span> 
* <span data-ttu-id="6783d-471">@rossifumax, New-AzConfigurationAssignment.md의 오타 수정(#12701)</span><span class="sxs-lookup"><span data-stu-id="6783d-471">@rossifumax, Fix typo in New-AzConfigurationAssignment.md (#12701)</span></span>

## <a name="461---august-2020"></a><span data-ttu-id="6783d-472">4.6.1 - 2020년 8월</span><span class="sxs-lookup"><span data-stu-id="6783d-472">4.6.1 - August 2020</span></span>
#### <a name="azcompute"></a><span data-ttu-id="6783d-473">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6783d-473">Az.Compute</span></span>
* <span data-ttu-id="6783d-474">'New-AzVm'에서 '-EncryptionAtHost' 매개 변수를 패치하여 기본값인 false가 제거됨[#12776]</span><span class="sxs-lookup"><span data-stu-id="6783d-474">Patched '-EncryptionAtHost' parameter in 'New-AzVm' to remove default value of false [#12776]</span></span>

## <a name="460---august-2020"></a><span data-ttu-id="6783d-475">4.6.0 - 2020년 8월</span><span class="sxs-lookup"><span data-stu-id="6783d-475">4.6.0 - August 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="6783d-476">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6783d-476">Az.Accounts</span></span>
* <span data-ttu-id="6783d-477">검색 엔드포인트가 기본 AzureCloud나 기타 공용 환경을 반환하지 않는 경우 모든 퍼블릭 클라우드 환경이 로드됨 [#12633]</span><span class="sxs-lookup"><span data-stu-id="6783d-477">Loaded all public cloud environments when discovery endpoint doesn't return default AzureCloud or other public environments [#12633]</span></span>
* <span data-ttu-id="6783d-478">'Get-AzSubscription'에서 SubscriptionPolicies가 노출됨 [#12551]</span><span class="sxs-lookup"><span data-stu-id="6783d-478">Exposed SubscriptionPolicies in 'Get-AzSubscription' [#12551]</span></span>

#### <a name="azautomation"></a><span data-ttu-id="6783d-479">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="6783d-479">Az.Automation</span></span>
* <span data-ttu-id="6783d-480">Hybrid Worker 그룹을 지정하기 위해 'Set-AzAutomationWebhook'에 '-RunOn' 매개 변수가 추가됨</span><span class="sxs-lookup"><span data-stu-id="6783d-480">Added '-RunOn' parameters to 'Set-AzAutomationWebhook' to specify a Hybrid Worker Group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6783d-481">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6783d-481">Az.Compute</span></span>
* <span data-ttu-id="6783d-482">'New-AzVm', 'New-AzVmss', 'New-AzVMConfig', 'New-AzVmssConfig', 'Update-AzVM', 'Update-AzVmss'에 '-EncryptionAtHost' 매개 변수가 추가됨</span><span class="sxs-lookup"><span data-stu-id="6783d-482">Added '-EncryptionAtHost' parameter to 'New-AzVm', 'New-AzVmss', 'New-AzVMConfig', 'New-AzVmssConfig', 'Update-AzVM', and 'Update-AzVmss'</span></span>
* <span data-ttu-id="6783d-483">'Get-AzVM' 및 'Get-AzVmss' 반환 개체에 'SecurityProfile'이 추가됨</span><span class="sxs-lookup"><span data-stu-id="6783d-483">Added 'SecurityProfile' to 'Get-AzVM' and 'Get-AzVmss' return object</span></span>
* <span data-ttu-id="6783d-484">'-InstanceView' 스위치가 'Get-AzHostGroup'에 선택적 매개 변수로 추가됨</span><span class="sxs-lookup"><span data-stu-id="6783d-484">Added '-InstanceView' switch as optional parameter to 'Get-AzHostGroup'</span></span>
* <span data-ttu-id="6783d-485">새 cmdlet 'Invoke-AzVmPatchAssessment'가 추가됨</span><span class="sxs-lookup"><span data-stu-id="6783d-485">Added new cmdlet 'Invoke-AzVmPatchAssessment'</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="6783d-486">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="6783d-486">Az.DataFactory</span></span>
* <span data-ttu-id="6783d-487">PSPipelineRun 클래스에 누락된 속성이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-487">Added missing properties to PSPipelineRun class.</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="6783d-488">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="6783d-488">Az.HDInsight</span></span>
* <span data-ttu-id="6783d-489">호스트 기능에서 암호화를 사용하여 클러스터를 만드는 것이 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-489">Supported creating cluster with encryption at host feature.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="6783d-490">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="6783d-490">Az.KeyVault</span></span>
* <span data-ttu-id="6783d-491">일시 삭제 사용 안 함 계획에 대한 경고 메시지가 추가됨</span><span class="sxs-lookup"><span data-stu-id="6783d-491">Added warning messages for planning to disable soft delete</span></span>
* <span data-ttu-id="6783d-492">특성 SecretValueText 제거 계획에 대한 경고 메시지가 추가됨</span><span class="sxs-lookup"><span data-stu-id="6783d-492">Added warning messages for planning to remove attribute SecretValueText</span></span>

#### <a name="azmaintenance"></a><span data-ttu-id="6783d-493">Az.Maintenance</span><span class="sxs-lookup"><span data-stu-id="6783d-493">Az.Maintenance</span></span>
* <span data-ttu-id="6783d-494">'New-AzMaintenanceConfiguration'에 선택적 일정 관련 필드가 추가됨</span><span class="sxs-lookup"><span data-stu-id="6783d-494">Added optional schedule related fields to 'New-AzMaintenanceConfiguration'</span></span>
* <span data-ttu-id="6783d-495">'Get-AzMaintenancePublicConfiguration'에 대한 새 cmdlet이 추가됨</span><span class="sxs-lookup"><span data-stu-id="6783d-495">Added new cmdlet for 'Get-AzMaintenancePublicConfiguration'</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="6783d-496">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="6783d-496">Az.ManagedServices</span></span>
* <span data-ttu-id="6783d-497">관리되는 서비스 할당 및 정의의 cmdlet에 대한 호환성이 손상되는 변경 경고가 추가됨</span><span class="sxs-lookup"><span data-stu-id="6783d-497">Added breaking change warnings on cmdlets of managed services assignment and definition</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="6783d-498">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="6783d-498">Az.Monitor</span></span>
* <span data-ttu-id="6783d-499">로그 및 메트릭 사용을 분리하기 위해 'Set-AzDiagnosticSetting'에 설정된 매개 변수가 확장됨 [#12482]</span><span class="sxs-lookup"><span data-stu-id="6783d-499">Extended the parameter set in 'Set-AzDiagnosticSetting' for separation of Logs and Metrics enablement [#12482]</span></span>
* <span data-ttu-id="6783d-500">파이프라인에서 메트릭 경고를 가져오는 경우 'Add-AzMetricAlertRuleV2'에 대한 버그가 수정됨</span><span class="sxs-lookup"><span data-stu-id="6783d-500">Fixed bug for 'Add-AzMetricAlertRuleV2' when getting metric alert from pipeline</span></span>

#### <a name="azresources"></a><span data-ttu-id="6783d-501">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6783d-501">Az.Resources</span></span>
* <span data-ttu-id="6783d-502">Azure Policy를 통해 별칭을 수정할 수 있는지 여부를 나타내는 정보를 포함하도록 'Get-AzPolicyAlias' 응답이 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="6783d-502">Updated 'Get-AzPolicyAlias' response to include information indicating whether the alias is modifiable by Azure Policy.</span></span>
* <span data-ttu-id="6783d-503">새 cmdlet 'Set-AzRoleAssignment'가 생성됨</span><span class="sxs-lookup"><span data-stu-id="6783d-503">Created new cmdlet 'Set-AzRoleAssignment'</span></span>
* <span data-ttu-id="6783d-504">관리 그룹 범위에서 ARM 템플릿 What-If 결과를 가져오는 'Get-AzDeploymentManagementGroupWhatIfResult'가 추가됨</span><span class="sxs-lookup"><span data-stu-id="6783d-504">Added 'Get-AzDeploymentManagementGroupWhatIfResult' for getting ARM template What-If results at management Group scope</span></span>
* <span data-ttu-id="6783d-505">테넌트 범위에서 ARM 템플릿 What-If 결과를 가져오는 'Get-AzTenantWhatIfResult' 새 cmdlet이 추가됨</span><span class="sxs-lookup"><span data-stu-id="6783d-505">Added 'Get-AzTenantWhatIfResult' new cmdlet for getting ARM template What-If results at tenant scope</span></span>
* <span data-ttu-id="6783d-506">ARM 템플릿 What-If 결과를 사용하도록 'New-AzManagementGroupDeployment' 및 'New-AzTenantDeployment'에 대한 '-WhatIf' 및 '-Confirm'이 재정의됨</span><span class="sxs-lookup"><span data-stu-id="6783d-506">Overrode '-WhatIf' and '-Confirm' for 'New-AzManagementGroupDeployment' and 'New-AzTenantDeployment' to use ARM template What-If results</span></span>
* <span data-ttu-id="6783d-507">새 배포 cmdlet에 대한 '-WhatIf' 및 '-Confirm' 동작이 False를 준수하도록 수정됨</span><span class="sxs-lookup"><span data-stu-id="6783d-507">Fixed the behaviors of '-WhatIf' and '-Confirm' for new deployment cmdlets so they comply with False and</span></span> 
* <span data-ttu-id="6783d-508">'-TemplateObject' 및 'TemplateParameterObject'에 대한 직렬화 오류가 수정됨 [#1528] [#6292]</span><span class="sxs-lookup"><span data-stu-id="6783d-508">Fixed serialization error for '-TemplateObject' and 'TemplateParameterObject' [#1528] [#6292]</span></span>
* <span data-ttu-id="6783d-509">예정된 출력 형식 변경을 위해 'Get-AzResourceGroupDeploymentOperation'에 호환성이 손상되는 변경 특성이 추가됨</span><span class="sxs-lookup"><span data-stu-id="6783d-509">Added breaking change attribute to 'Get-AzResourceGroupDeploymentOperation' for the upcoming output type change</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="6783d-510">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="6783d-510">Az.SignalR</span></span>
* <span data-ttu-id="6783d-511">'Restart-AzSignalR' 및 'Update-AzSignalR' 도움말 파일 오류가 수정됨</span><span class="sxs-lookup"><span data-stu-id="6783d-511">Fixed 'Restart-AzSignalR' and 'Update-AzSignalR' help files errors</span></span>
* <span data-ttu-id="6783d-512">'Update-AzSignalRNetworkAcl', 'Set-AzSignalRUpstream' cmdlet이 추가됨</span><span class="sxs-lookup"><span data-stu-id="6783d-512">Added cmdlets 'Update-AzSignalRNetworkAcl', 'Set-AzSignalRUpstream'</span></span>

#### <a name="azstorage"></a><span data-ttu-id="6783d-513">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="6783d-513">Az.Storage</span></span>
* <span data-ttu-id="6783d-514">지원되는 Blob 쿼리 가속</span><span class="sxs-lookup"><span data-stu-id="6783d-514">Supported blob query acceleration</span></span>
    -  <span data-ttu-id="6783d-515">'Get-AzStorageBlobQueryResult'</span><span class="sxs-lookup"><span data-stu-id="6783d-515">'Get-AzStorageBlobQueryResult'</span></span>
    -  <span data-ttu-id="6783d-516">'New-AzStorageBlobQueryConfig'</span><span class="sxs-lookup"><span data-stu-id="6783d-516">'New-AzStorageBlobQueryConfig'</span></span>
* <span data-ttu-id="6783d-517">도움말 파일 업데이트, 자세한 설명 추가 및 오타 수정</span><span class="sxs-lookup"><span data-stu-id="6783d-517">Updated help file, added more description, and fixed typo</span></span>
    -  <span data-ttu-id="6783d-518">'Start-AzStorageBlobCopy'</span><span class="sxs-lookup"><span data-stu-id="6783d-518">'Start-AzStorageBlobCopy'</span></span>
    -  <span data-ttu-id="6783d-519">'Get-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="6783d-519">'Get-AzDataLakeGen2Item'</span></span>
* <span data-ttu-id="6783d-520">관련 하위 디렉터리가 없는 경우 Blob 다운로드 실패가 수정됨 [#12592]</span><span class="sxs-lookup"><span data-stu-id="6783d-520">Fixed download blob fail when related sub directory not exist [#12592]</span></span>
    -  <span data-ttu-id="6783d-521">'Get-AzStorageBlobContent'</span><span class="sxs-lookup"><span data-stu-id="6783d-521">'Get-AzStorageBlobContent'</span></span>
* <span data-ttu-id="6783d-522">스토리지 계정에 대해 개체 복제 정책 설정/가져오기/제거가 지원됨</span><span class="sxs-lookup"><span data-stu-id="6783d-522">Supported Set/Get/Remove Object Replication Policy on Storage accounts</span></span>
    - <span data-ttu-id="6783d-523">'New-AzStorageObjectReplicationPolicyRule'</span><span class="sxs-lookup"><span data-stu-id="6783d-523">'New-AzStorageObjectReplicationPolicyRule'</span></span>
    - <span data-ttu-id="6783d-524">'Set-AzStorageObjectReplicationPolicy'</span><span class="sxs-lookup"><span data-stu-id="6783d-524">'Set-AzStorageObjectReplicationPolicy'</span></span>
    - <span data-ttu-id="6783d-525">'Get-AzStorageObjectReplicationPolicy'</span><span class="sxs-lookup"><span data-stu-id="6783d-525">'Get-AzStorageObjectReplicationPolicy'</span></span>
    - <span data-ttu-id="6783d-526">'Remove-AzStorageObjectReplicationPolicy'</span><span class="sxs-lookup"><span data-stu-id="6783d-526">'Remove-AzStorageObjectReplicationPolicy'</span></span>
* <span data-ttu-id="6783d-527">스토리지 계정의 Blob Service에서 ChangeFeed 사용/사용 안 함이 지원됨</span><span class="sxs-lookup"><span data-stu-id="6783d-527">Supported enable/disable ChangeFeed on Blob Service of a Storage account</span></span>
    - <span data-ttu-id="6783d-528">'Update-AzStorageBlobServiceProperty'</span><span class="sxs-lookup"><span data-stu-id="6783d-528">'Update-AzStorageBlobServiceProperty'</span></span>

## <a name="450---august-2020"></a><span data-ttu-id="6783d-529">4.5.0 - 2020년 8월</span><span class="sxs-lookup"><span data-stu-id="6783d-529">4.5.0 - August 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="6783d-530">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6783d-530">Az.Accounts</span></span>
* <span data-ttu-id="6783d-531">매개 변수 'MaxContextPopulation'을 허용하도록 'Connect-AzAccount' 업데이트됨 [# 9865]</span><span class="sxs-lookup"><span data-stu-id="6783d-531">Updated 'Connect-AzAccount' to accept parameter 'MaxContextPopulation' [#9865]</span></span>
* <span data-ttu-id="6783d-532">SubscriptionClient 버전이 2019-06-01로 업데이트되고 테넌트 도메인을 표시 [#9838]</span><span class="sxs-lookup"><span data-stu-id="6783d-532">Updated SubscriptionClient version to 2019-06-01 and display tenant domains [#9838]</span></span>
* <span data-ttu-id="6783d-533">구독의 managedBy 테넌트 정보 및 홈 테넌트 지원</span><span class="sxs-lookup"><span data-stu-id="6783d-533">Supported home tenant and managedBy tenant information of subscription</span></span>
* <span data-ttu-id="6783d-534">원격 분석 데이터의 모듈 이름, 버전 정보 수정</span><span class="sxs-lookup"><span data-stu-id="6783d-534">Corrected module name, version info in telemetry data</span></span>
* <span data-ttu-id="6783d-535">환경 메타데이터 엔드포인트가 호환되지 않는 값을 반환하는 경우 SqlDatabaseDnsSuffix 및 ServiceManagementUrl이 조정됨</span><span class="sxs-lookup"><span data-stu-id="6783d-535">Adjusted SqlDatabaseDnsSuffix and ServiceManagementUrl if environment metadata endpoint returns incompatible value</span></span>

#### <a name="azaks"></a><span data-ttu-id="6783d-536">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="6783d-536">Az.Aks</span></span>
* <span data-ttu-id="6783d-537">'ClientIdAndSecret'을 'ServicePrincipalIdAndSecret'으로 제거하고 'ClientIdAndSecret'을 별칭으로 설정함 [#12381]</span><span class="sxs-lookup"><span data-stu-id="6783d-537">Removed 'ClientIdAndSecret' to 'ServicePrincipalIdAndSecret' and set 'ClientIdAndSecret' as an alias [#12381].</span></span>
* <span data-ttu-id="6783d-538">'Get-AzAks'/'New-AzAks'/'Remove-AzAks'/'Set-AzAks'를 'Get-AzAksCluster'/'New-AzAksCluster'/'Remove-AzAksCluster'/'Set-AzAksCluster'로 제거하고 원본을 별칭으로 설정함 [#12373].</span><span class="sxs-lookup"><span data-stu-id="6783d-538">Removed 'Get-AzAks'/'New-AzAks'/'Remove-AzAks'/'Set-AzAks' to 'Get-AzAksCluster'/'New-AzAksCluster'/'Remove-AzAksCluster'/'Set-AzAksCluster' and set the original ones as alias [#12373].</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="6783d-539">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="6783d-539">Az.ApiManagement</span></span>
* <span data-ttu-id="6783d-540">새 'Add-AzApiManagementApiToGateway' cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-540">Added new 'Add-AzApiManagementApiToGateway' cmdlet.</span></span>
* <span data-ttu-id="6783d-541">새 'Get-AzApiManagementGateway' cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-541">Added new 'Get-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="6783d-542">새 'Get-AzApiManagementGatewayHostnameConfiguration' cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-542">Added new 'Get-AzApiManagementGatewayHostnameConfiguration' cmdlet.</span></span>
* <span data-ttu-id="6783d-543">새 'Get-AzApiManagementGatewayKey' cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-543">Added new 'Get-AzApiManagementGatewayKey' cmdlet.</span></span>
* <span data-ttu-id="6783d-544">새 'New-AzApiManagementGateway' cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-544">Added new 'New-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="6783d-545">새 'New-AzApiManagementGatewayHostnameConfiguration' cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-545">Added new 'New-AzApiManagementGatewayHostnameConfiguration' cmdlet.</span></span>
* <span data-ttu-id="6783d-546">새 'New-AzApiManagementResourceLocationObject' cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-546">Added new 'New-AzApiManagementResourceLocationObject' cmdlet.</span></span>
* <span data-ttu-id="6783d-547">새 'Remove-AzApiManagementApiFromGateway' cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-547">Added new 'Remove-AzApiManagementApiFromGateway' cmdlet.</span></span>
* <span data-ttu-id="6783d-548">새 'Remove-AzApiManagementGateway' cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-548">Added new 'Remove-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="6783d-549">새 'Remove-AzApiManagementGatewayHostnameConfiguration' cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-549">Added new 'Remove-AzApiManagementGatewayHostnameConfiguration' cmdlet.</span></span>
* <span data-ttu-id="6783d-550">새 'Update-AzApiManagementGateway' cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-550">Added new 'Update-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="6783d-551">'Get-AzApiManagementApi' cmdlet에 선택적 [-GatewayId] 매개 변수가 새로 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-551">Added new optional [-GatewayId] parameter to the 'Get-AzApiManagementApi' cmdlet.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="6783d-552">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="6783d-552">Az.CognitiveServices</span></span>
* <span data-ttu-id="6783d-553">'Deny'가 특히 NetworkRules 기본 작업으로 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-553">Used 'Deny' specifically as NetworkRules default action.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="6783d-554">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="6783d-554">Az.FrontDoor</span></span>
* <span data-ttu-id="6783d-555">Enum.Parse가 null 값을 Enabled 또는 Disabled 열거형 값으로 강제 변환하려는 경우 예외가 throw되는 문제를 수정했습니다. [#12344]</span><span class="sxs-lookup"><span data-stu-id="6783d-555">Fixed an issue where an exception is being thrown when Enum.Parse tries to coerce a null value to an Enabled or Disabled enum values [#12344]</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="6783d-556">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="6783d-556">Az.HDInsight</span></span>
* <span data-ttu-id="6783d-557">전송 중 암호화 기능을 사용하여 클러스터를 만드는 것이 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-557">Supported creating cluster with encryption in transit feature.</span></span>
    - <span data-ttu-id="6783d-558">cmdlet 'New-AzHDInsightCluster'에 새 매개 변수 'EncryptionInTransit' 추가</span><span class="sxs-lookup"><span data-stu-id="6783d-558">Add new parameter 'EncryptionInTransit' to the cmdlet 'New-AzHDInsightCluster'</span></span>
    - <span data-ttu-id="6783d-559">cmdlet 'New-AzHDInsightClusterConfig'에 새 매개 변수 'EncryptionInTransit' 추가</span><span class="sxs-lookup"><span data-stu-id="6783d-559">Add new parameter 'EncryptionInTransit' to the cmdlet 'New-AzHDInsightClusterConfig'</span></span>
* <span data-ttu-id="6783d-560">프라이빗 링크 기능을 사용하여 클러스터를 만드는 것이 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-560">Supported creating cluster with private link feature:</span></span>
    - <span data-ttu-id="6783d-561">cmdlet 'New-AzHDInsightCluster'에 새 매개 변수 'PublicNetworkAccessType' 및 'OutboundPublicNetworkAccessType' 추가</span><span class="sxs-lookup"><span data-stu-id="6783d-561">Add new parameter 'PublicNetworkAccessType' and 'OutboundPublicNetworkAccessType' to the cmdlet 'New-AzHDInsightCluster'</span></span>
    - <span data-ttu-id="6783d-562">cmdlet 'New-AzHDInsightClusterConfig'에 새 매개 변수 'PublicNetworkAccessType' 및 'OutboundPublicNetworkAccessType' 추가</span><span class="sxs-lookup"><span data-stu-id="6783d-562">Add new parameter 'PublicNetworkAccessType' and 'OutboundPublicNetworkAccessType' to the cmdlet 'New-AzHDInsightClusterConfig'</span></span>
* <span data-ttu-id="6783d-563">'New-AzHDInsightCluster' 또는 'Get-AzHDInsightCluster'를 호출하는 경우 가상 네트워크 정보가 반환됨</span><span class="sxs-lookup"><span data-stu-id="6783d-563">Returned virtual network information when calling 'New-AzHDInsightCluster' or 'Get-AzHDInsightCluster'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6783d-564">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6783d-564">Az.Network</span></span>
* <span data-ttu-id="6783d-565">'Remove-AzExpressRouteCircuitConnectionConfig'에 AddressPrefixType 매개 변수 지원 추가</span><span class="sxs-lookup"><span data-stu-id="6783d-565">Added support for AddressPrefixType parameter to 'Remove-AzExpressRouteCircuitConnectionConfig'</span></span>
* <span data-ttu-id="6783d-566">작업을 중단하지 않는 변경이 추가됨: 'Remove-AzExpressRouteCircutPeeringConfig'의 프라이빗 피어링을 위한 PeerAddressType 기능</span><span class="sxs-lookup"><span data-stu-id="6783d-566">Added non-breaking changes: PeerAddressType functionality for Private Peering in 'Remove-AzExpressRouteCircutPeeringConfig'.</span></span>
* <span data-ttu-id="6783d-567">AddressPrefixType 및 PeerAddressType 매개 변수의 대/소문자를 무시하도록 코드가 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-567">Code changed to ignore case for AddressPrefixType and PeerAddressType parameter.</span></span>
* <span data-ttu-id="6783d-568">'New-AzLoadBalancerFrontendIpConfig', 'New-AzPublicIpAddress' 및 'New-AzPublicIpPrefix'에 대한 경고 메시지를 수정했습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-568">Modified the warning message for 'New-AzLoadBalancerFrontendIpConfig', 'New-AzPublicIpAddress' and 'New-AzPublicIpPrefix'.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="6783d-569">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="6783d-569">Az.OperationalInsights</span></span>
* <span data-ttu-id="6783d-570">'Remove-AzOperationalInsightsworkspace'에 대한 '-ForceDelete' 옵션이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-570">Added '-ForceDelete' option for 'Remove-AzOperationalInsightsworkspace'</span></span>
* <span data-ttu-id="6783d-571">새 cmdlet 'Get-AzOperationalInsightsDeletedWorkspace'가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-571">Added new cmdlet 'Get-AzOperationalInsightsDeletedWorkspace'</span></span>
* <span data-ttu-id="6783d-572">새 cmdlet 'Restore-AzOperationalInsightsWorkspace'가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-572">Added new cmdlet 'Restore-AzOperationalInsightsWorkspace'</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="6783d-573">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="6783d-573">Az.RecoveryServices</span></span>
* <span data-ttu-id="6783d-574">Azure Backup 컨테이너/항목 검색 환경이 개선되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-574">Improved the Azure Backup container/item discovery experience.</span></span>

#### <a name="azresources"></a><span data-ttu-id="6783d-575">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6783d-575">Az.Resources</span></span>
* <span data-ttu-id="6783d-576">'New-AzRoleAssignment'에 'Condition', 'ConditionVersion' 및 'Description' 속성을 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-576">Added properties 'Condition', 'ConditionVersion' and 'Description' to 'New-AzRoleAssignment'</span></span>
    - <span data-ttu-id="6783d-577">여기에는 데이터 모델과 관련된 모든 변경 사항이 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-577">This included all the relevant changes to the data models</span></span>

#### <a name="azsql"></a><span data-ttu-id="6783d-578">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6783d-578">Az.Sql</span></span>
* <span data-ttu-id="6783d-579">'New-AzSqlServer' 'Set-AzSqlServer'에서 서버 이름 대/소문자를 구분하지 않는 잠재적인 오류를 수정했습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-579">Fixed potential server name case insensitive error in 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>
* <span data-ttu-id="6783d-580">'New-AzSqlDatabaseSecondary'의 기존 데이터베이스 오류에서 반환되는 잘못된 데이터베이스 이름을 수정했습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-580">Fixed wrong database name returned on existing database error in 'New-AzSqlDatabaseSecondary'</span></span>

#### <a name="azstorage"></a><span data-ttu-id="6783d-581">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="6783d-581">Az.Storage</span></span>
* <span data-ttu-id="6783d-582">새 권한 x,t를 사용하여 컨테이너/blob Sas 토큰 만들기 지원</span><span class="sxs-lookup"><span data-stu-id="6783d-582">Supported create container/blob Sas token with new permission x,t</span></span>
    -  <span data-ttu-id="6783d-583">'New-AzStorageBlobSASToken'</span><span class="sxs-lookup"><span data-stu-id="6783d-583">'New-AzStorageBlobSASToken'</span></span>
    -  <span data-ttu-id="6783d-584">'New-AzStorageContainerSASToken'</span><span class="sxs-lookup"><span data-stu-id="6783d-584">'New-AzStorageContainerSASToken'</span></span>
* <span data-ttu-id="6783d-585">새 권한 x,t,f를 사용하여 계정 Sas 토큰 만들기 지원</span><span class="sxs-lookup"><span data-stu-id="6783d-585">Supported create account Sas token with new permission x,t,f</span></span>
    -  <span data-ttu-id="6783d-586">'New-AzStorageAccountSASToken'</span><span class="sxs-lookup"><span data-stu-id="6783d-586">'New-AzStorageAccountSASToken'</span></span>
* <span data-ttu-id="6783d-587">단일 파일 사용량 공유 가져오기 지원</span><span class="sxs-lookup"><span data-stu-id="6783d-587">Supported get single file share usage</span></span>
    - <span data-ttu-id="6783d-588">'Get-AzRmStorageShare'</span><span class="sxs-lookup"><span data-stu-id="6783d-588">'Get-AzRmStorageShare'</span></span>

## <a name="440---july-2020"></a><span data-ttu-id="6783d-589">4.4.0 - 2020년 7월</span><span class="sxs-lookup"><span data-stu-id="6783d-589">4.4.0 - July 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="6783d-590">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6783d-590">Az.Accounts</span></span>
* <span data-ttu-id="6783d-591">새 cmdlet 'Invoke-AzRestMethod' 추가</span><span class="sxs-lookup"><span data-stu-id="6783d-591">Added new cmdlet 'Invoke-AzRestMethod'</span></span>
* <span data-ttu-id="6783d-592">'Start-Job'을 사용하여 여러 Azure PowerShell cmdlet을 실행하는 등 다중 프로세스 시나리오에서 인증 오류를 발생시킬 수 있는 문제 해결 [#9448]</span><span class="sxs-lookup"><span data-stu-id="6783d-592">Fixed an issue that may cause authentication errors in multi-process scenarios such as running multiple Azure PowerShell cmdlets using 'Start-Job' [#9448]</span></span>

#### <a name="azaks"></a><span data-ttu-id="6783d-593">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="6783d-593">Az.Aks</span></span>
* <span data-ttu-id="6783d-594">'Get-AzAks'가 모든 클러스터를 가져오지 않는 버그 수정 [#12296]</span><span class="sxs-lookup"><span data-stu-id="6783d-594">Fixed bug 'Get-AzAks' doesn't get all clusters [#12296]</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="6783d-595">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="6783d-595">Az.AnalysisServices</span></span>
* <span data-ttu-id="6783d-596">인증에 대한 프로젝트 참조 제거</span><span class="sxs-lookup"><span data-stu-id="6783d-596">Removed project reference to Authentication</span></span>

#### <a name="azautomation"></a><span data-ttu-id="6783d-597">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="6783d-597">Az.Automation</span></span>
* <span data-ttu-id="6783d-598">이스케이프 문자를 포함하는 문자열을 json 개체로 변환할 수 없는 문제 해결</span><span class="sxs-lookup"><span data-stu-id="6783d-598">Fixed the issue that string with escape chars cannot be converted into json object.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6783d-599">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6783d-599">Az.Compute</span></span>
* <span data-ttu-id="6783d-600">'latest' 이미지 버전이 없는 'New-AzVmss'를 사용하는 경우 경고 추가</span><span class="sxs-lookup"><span data-stu-id="6783d-600">Added warning when using 'New-AzVmss' without 'latest' image version</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="6783d-601">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="6783d-601">Az.DataFactory</span></span>
* <span data-ttu-id="6783d-602">Data Factory에 대한 전역 매개 변수를 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-602">Added global parameters to Data Factory.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="6783d-603">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="6783d-603">Az.EventGrid</span></span>
* <span data-ttu-id="6783d-604">2020-06-01 API 버전을 사용하도록 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-604">Updated to use the 2020-06-01 API version.</span></span>
* <span data-ttu-id="6783d-605">추가된 새로운 기능:</span><span class="sxs-lookup"><span data-stu-id="6783d-605">Added new features:</span></span>
    - <span data-ttu-id="6783d-606">입력 매핑</span><span class="sxs-lookup"><span data-stu-id="6783d-606">Input mapping</span></span>
    - <span data-ttu-id="6783d-607">이벤트 배달 스키마</span><span class="sxs-lookup"><span data-stu-id="6783d-607">Event Delivery Schema</span></span>
    - <span data-ttu-id="6783d-608">Private Link</span><span class="sxs-lookup"><span data-stu-id="6783d-608">Private Link</span></span>
    - <span data-ttu-id="6783d-609">클라우드 이벤트 V10 스키마</span><span class="sxs-lookup"><span data-stu-id="6783d-609">Cloud Event V10 Schema</span></span>
    - <span data-ttu-id="6783d-610">대상으로 Service Bus 항목</span><span class="sxs-lookup"><span data-stu-id="6783d-610">Service Bus Topic As Destination</span></span>
    - <span data-ttu-id="6783d-611">대상으로 Azure 함수</span><span class="sxs-lookup"><span data-stu-id="6783d-611">Azure Function As Destination</span></span>
    - <span data-ttu-id="6783d-612">WebHook 일괄 처리</span><span class="sxs-lookup"><span data-stu-id="6783d-612">WebHook Batching</span></span>
    - <span data-ttu-id="6783d-613">보안 웹후크(AAD 지원)</span><span class="sxs-lookup"><span data-stu-id="6783d-613">Secure webhook (AAD support)</span></span>
    - <span data-ttu-id="6783d-614">IpFiltering</span><span class="sxs-lookup"><span data-stu-id="6783d-614">IpFiltering</span></span>
* <span data-ttu-id="6783d-615">다음 Cmdlet이 업데이트 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-615">Updated cmdlets:</span></span>
    - <span data-ttu-id="6783d-616">'New-AzEventGridSubscription'/'Update-AzEventGridSubscription':</span><span class="sxs-lookup"><span data-stu-id="6783d-616">'New-AzEventGridSubscription'/'Update-AzEventGridSubscription':</span></span>
        - <span data-ttu-id="6783d-617">웹후크 일괄 처리를 지원하기 위해 새로운 선택적 매개 변수를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-617">Add new optional parameters to support webhook batching.</span></span>
        - <span data-ttu-id="6783d-618">AAD를 사용하여 보안 웹후크를 지원하는 새로운 선택적 매개 변수를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-618">Add new optional parameters to support secured webhook using AAD.</span></span>
        - <span data-ttu-id="6783d-619">Azure 함수 및 Service Bus 항목을 새 대상으로 지원하기 위해 EndpointType 매개 변수에 대한 새 열거형을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-619">Add new enum for EndpointType parameter to support azure function and service bus topic as new destinations.</span></span>
        - <span data-ttu-id="6783d-620">배달 스키마에 대한 새로운 선택적 매개 변수를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-620">Add new optional parameter for delivery schema.</span></span>
    - <span data-ttu-id="6783d-621">'New-AzEventGridTopic'/'Update-AzEventGridTopic' 및 'New-AzEventGridDomain'/'Update-AzEventGridDomain':</span><span class="sxs-lookup"><span data-stu-id="6783d-621">'New-AzEventGridTopic'/'Update-AzEventGridTopic' and 'New-AzEventGridDomain'/'Update-AzEventGridDomain':</span></span>
        - <span data-ttu-id="6783d-622">IpFiltering을 지원하기 위해 새로운 선택적 매개 변수를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-622">Add new optional parameters to support IpFiltering.</span></span>
    - <span data-ttu-id="6783d-623">'New-AzEventGridTopic'/'New-AzEventGridDomain':</span><span class="sxs-lookup"><span data-stu-id="6783d-623">'New-AzEventGridTopic'/'New-AzEventGridDomain':</span></span>
        - <span data-ttu-id="6783d-624">입력 매핑을 지원하기 위해 새로운 선택적 매개 변수를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-624">Add new optional parameters to support Input mapping.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="6783d-625">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="6783d-625">Az.FrontDoor</span></span>
* <span data-ttu-id="6783d-626">API 2020-05-01을 사용하도록 업데이트된 모듈</span><span class="sxs-lookup"><span data-stu-id="6783d-626">Updated module to use API 2020-05-01</span></span>
* <span data-ttu-id="6783d-627">Storage, Keyvault 및 Web App Service 리소스에 대한 프라이빗 링크 지원을 추가함</span><span class="sxs-lookup"><span data-stu-id="6783d-627">Added Private link support for Storage, Keyvault and Web App Service resources</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="6783d-628">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="6783d-628">Az.HDInsight</span></span>
* <span data-ttu-id="6783d-629">국가 클라우드에서 ADLSGen1/2 스토리지로 클러스터를 만드는 것이 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-629">Supported creating cluster with ADLSGen1/2 storage in national clouds.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="6783d-630">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="6783d-630">Az.Monitor</span></span>
* <span data-ttu-id="6783d-631">메트릭 또는 로그가 null인 경우 'Get-AzDiagnosticSetting'에 대한 버그 수정 [#12272]</span><span class="sxs-lookup"><span data-stu-id="6783d-631">Fixed bug for 'Get-AzDiagnosticSetting' when metrics or logs are null [#12272]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6783d-632">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6783d-632">Az.Network</span></span>
* <span data-ttu-id="6783d-633">VWan HubVnet 연결의 매개 변수 교환 수정</span><span class="sxs-lookup"><span data-stu-id="6783d-633">Fixed parameters swap in VWan HubVnet connection</span></span>
* <span data-ttu-id="6783d-634">Azure Network Virtual Appliance 사이트에 대한 새 cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="6783d-634">Added new cmdlets for Azure Network Virtual Appliance Sites</span></span>
    - <span data-ttu-id="6783d-635">'Get-AzVirtualApplianceSite'</span><span class="sxs-lookup"><span data-stu-id="6783d-635">'Get-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="6783d-636">'New-AzVirtualApplianceSite'</span><span class="sxs-lookup"><span data-stu-id="6783d-636">'New-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="6783d-637">'Remove-AzVirtualApplianceSite'</span><span class="sxs-lookup"><span data-stu-id="6783d-637">'Remove-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="6783d-638">'Update-AzVirtualApplianceSite'</span><span class="sxs-lookup"><span data-stu-id="6783d-638">'Update-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="6783d-639">'New-AzOffice365PolicyProperty'</span><span class="sxs-lookup"><span data-stu-id="6783d-639">'New-AzOffice365PolicyProperty'</span></span>
* <span data-ttu-id="6783d-640">Azure Network Virtual Appliance에 대한 새 cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="6783d-640">Added new cmdlets for Azure Network Virtual Appliance</span></span>
    - <span data-ttu-id="6783d-641">'Get-AzNetworkVirtualAppliance'</span><span class="sxs-lookup"><span data-stu-id="6783d-641">'Get-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="6783d-642">'New-AzNetworkVirtualAppliance'</span><span class="sxs-lookup"><span data-stu-id="6783d-642">'New-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="6783d-643">'Remove-AzNetworkVirtualAppliance'</span><span class="sxs-lookup"><span data-stu-id="6783d-643">'Remove-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="6783d-644">'Update-AzNetworkVirtualAppliance'</span><span class="sxs-lookup"><span data-stu-id="6783d-644">'Update-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="6783d-645">'Get-AzNetworkVirtualApplianceSku'</span><span class="sxs-lookup"><span data-stu-id="6783d-645">'Get-AzNetworkVirtualApplianceSku'</span></span>
    - <span data-ttu-id="6783d-646">'New-AzVirtualApplianceSkuProperty'</span><span class="sxs-lookup"><span data-stu-id="6783d-646">'New-AzVirtualApplianceSkuProperty'</span></span>
* <span data-ttu-id="6783d-647">Application Gateway를 Private Link 공통 cmdlet에 온보딩</span><span class="sxs-lookup"><span data-stu-id="6783d-647">Onboarded Application Gateway to Private Link Common Cmdlets</span></span>
* <span data-ttu-id="6783d-648">StorageSync를 Private Link 공통 cmdlet에 온보딩</span><span class="sxs-lookup"><span data-stu-id="6783d-648">Onboarded StorageSync to Private Link Common Cmdlets</span></span>
* <span data-ttu-id="6783d-649">SignalR을 Private Link 공통 cmdlet에 온보딩</span><span class="sxs-lookup"><span data-stu-id="6783d-649">Onboarded SignalR to Private Link Common Cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="6783d-650">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="6783d-650">Az.RecoveryServices</span></span>
* <span data-ttu-id="6783d-651">인증에 대한 프로젝트 참조 제거</span><span class="sxs-lookup"><span data-stu-id="6783d-651">Removed project reference to Authentication</span></span>
* <span data-ttu-id="6783d-652">Azure Backup 튜닝 cmdlet은 텍스트를 보다 정확하게 작성하는 데 도움이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-652">Azure Backup tuned cmdlets help text to be more accurate.</span></span>
* <span data-ttu-id="6783d-653">Azure Backup은 'Get-AzRecoveryServicesBackupJob' cmdlet을 사용하여 MAB 에이전트 작업을 가져오는 지원을 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-653">Azure Backup added support for fetching MAB agent jobs using 'Get-AzRecoveryServicesBackupJob' cmdlet.</span></span>

#### <a name="azresources"></a><span data-ttu-id="6783d-654">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6783d-654">Az.Resources</span></span>
* <span data-ttu-id="6783d-655">SDK를 사용하도록 'Save-AzResourceGroupDeploymentTemplate'을 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-655">Updated 'Save-AzResourceGroupDeploymentTemplate' to use the SDK.</span></span>
* <span data-ttu-id="6783d-656">'Unregister-AzResourceProvider' cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-656">Added 'Unregister-AzResourceProvider' cmdlet.</span></span>

#### <a name="azsql"></a><span data-ttu-id="6783d-657">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6783d-657">Az.Sql</span></span>
* <span data-ttu-id="6783d-658">Set-AzSqlInstanceActiveDirectoryAdministrator cmdlet에서 서비스 주체 및 게스트 사용자에 대한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-658">Added support for Service principal and guest users in Set-AzSqlInstanceActiveDirectoryAdministrator cmdlet'</span></span>
* <span data-ttu-id="6783d-659">데이터 분류 cmdlet의 버그를 수정했습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-659">Fixed a bug in Data Classification cmdlets.'</span></span>
* <span data-ttu-id="6783d-660">다음의 Azure SQL Managed Instance 장애 조치에 대한 지원 추가: 'Invoke-AzSqlInstanceFailover'</span><span class="sxs-lookup"><span data-stu-id="6783d-660">Added support for Azure SQL Managed Instance failover: 'Invoke-AzSqlInstanceFailover'</span></span>

#### <a name="azstorage"></a><span data-ttu-id="6783d-661">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="6783d-661">Az.Storage</span></span>
* <span data-ttu-id="6783d-662">일부 데이터 평면 cmdlet에 대해 UserAgent가 추가되지 않는 문제를 해결했습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-662">Fixed the issue that UserAgent is not added for some data plane cmdlets.</span></span>
* <span data-ttu-id="6783d-663">MinimumTlsVersion 및 AllowBlobPublicAccess로 스토리지 계정 만들기/업데이트 지원</span><span class="sxs-lookup"><span data-stu-id="6783d-663">Supported create/update Storage account with MinimumTlsVersion and AllowBlobPublicAccess</span></span>
    -  <span data-ttu-id="6783d-664">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="6783d-664">'New-AzStorageAccount'</span></span>
    -  <span data-ttu-id="6783d-665">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="6783d-665">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="6783d-666">스토리지 계정의 Blob Service에서 버전 관리 사용/사용 안 함 지원</span><span class="sxs-lookup"><span data-stu-id="6783d-666">Support enable/disable versioning on Blob Service of a Storage account</span></span>
    - <span data-ttu-id="6783d-667">'Update-AzStorageBlobServiceProperty'</span><span class="sxs-lookup"><span data-stu-id="6783d-667">'Update-AzStorageBlobServiceProperty'</span></span>
* <span data-ttu-id="6783d-668">Blob 버전 관리로 Blob 나열 지원</span><span class="sxs-lookup"><span data-stu-id="6783d-668">Support list blobs with blob versions</span></span>
    - <span data-ttu-id="6783d-669">'Get-AzStorageBlob'</span><span class="sxs-lookup"><span data-stu-id="6783d-669">'Get-AzStorageBlob'</span></span>
* <span data-ttu-id="6783d-670">단일 Blob 스냅샷 또는 Blob 버전 가져오기/제거 지원</span><span class="sxs-lookup"><span data-stu-id="6783d-670">Support get/remove single blob snapshot or blob version</span></span>
    - <span data-ttu-id="6783d-671">'Get-AzStorageBlob'</span><span class="sxs-lookup"><span data-stu-id="6783d-671">'Get-AzStorageBlob'</span></span>
    - <span data-ttu-id="6783d-672">'Remove-AzStorageBlob'</span><span class="sxs-lookup"><span data-stu-id="6783d-672">'Remove-AzStorageBlob'</span></span>
* <span data-ttu-id="6783d-673">Azure.Storage.Blobs V12에서 생성된 Blob 개체의 파이프라인 지원</span><span class="sxs-lookup"><span data-stu-id="6783d-673">Support pipeline from blob object generated from Azure.Storage.Blobs V12</span></span>
    - <span data-ttu-id="6783d-674">'Get-AzStorageBlobContent'</span><span class="sxs-lookup"><span data-stu-id="6783d-674">'Get-AzStorageBlobContent'</span></span>
    - <span data-ttu-id="6783d-675">'New-AzStorageBlobSASToken'</span><span class="sxs-lookup"><span data-stu-id="6783d-675">'New-AzStorageBlobSASToken'</span></span>
    - <span data-ttu-id="6783d-676">'Remove-AzStorageBlob'</span><span class="sxs-lookup"><span data-stu-id="6783d-676">'Remove-AzStorageBlob'</span></span>
    - <span data-ttu-id="6783d-677">'Set-AzStorageBlobContent'</span><span class="sxs-lookup"><span data-stu-id="6783d-677">'Set-AzStorageBlobContent'</span></span>
    - <span data-ttu-id="6783d-678">'Start-AzStorageBlobCopy'</span><span class="sxs-lookup"><span data-stu-id="6783d-678">'Start-AzStorageBlobCopy'</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="6783d-679">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="6783d-679">Az.StorageSync</span></span>
* <span data-ttu-id="6783d-680">ApiVersion 2020-03-01을 대상으로 하는 새 버전의 StorageSync SDK 추가</span><span class="sxs-lookup"><span data-stu-id="6783d-680">Added a new version StorageSync SDK targeting ApiVersion 2020-03-01</span></span>
* <span data-ttu-id="6783d-681">스토리지 동기화 서비스 업데이트 cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="6783d-681">Added Update Storage Sync Service cmdlet</span></span>
    - <span data-ttu-id="6783d-682">'Set-AzStorageSyncService'</span><span class="sxs-lookup"><span data-stu-id="6783d-682">'Set-AzStorageSyncService'</span></span>
* <span data-ttu-id="6783d-683">IncomingTrafficPolicy 및 PrivateEndpointConnections가 StorageSyncService cmdlet에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-683">Added IncomingTrafficPolicy and PrivateEndpointConnections to StorageSyncService cmdlets.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="6783d-684">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="6783d-684">Az.Websites</span></span>
* <span data-ttu-id="6783d-685">App Service 계획과 동일한 리소스 그룹에 속하지 않는 슬롯에 대한 작업을 수행하기 위한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="6783d-685">Added support to perform operations for Slots not in the same resource group as the App Service Plan</span></span>

## <a name="430---june-2020"></a><span data-ttu-id="6783d-686">4.3.0 - 2020년 6월</span><span class="sxs-lookup"><span data-stu-id="6783d-686">4.3.0 - June 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="6783d-687">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6783d-687">Az.Accounts</span></span>
* <span data-ttu-id="6783d-688">기본적으로 환경 검색 설정이 지원되며 'Add-AzEnvironment'를 통해 환경을 추가할 수 있음</span><span class="sxs-lookup"><span data-stu-id="6783d-688">Supported discovering environment setting by default and adding environment via 'Add-AzEnvironment'</span></span>
* <span data-ttu-id="6783d-689">미리 로드된 어셈블리 업데이트 [#12024], [#11976]</span><span class="sxs-lookup"><span data-stu-id="6783d-689">Update preloaded assemblies [#12024], [#11976]</span></span>
* <span data-ttu-id="6783d-690">Azure.Core 어셈블리 업데이트</span><span class="sxs-lookup"><span data-stu-id="6783d-690">Updated Azure.Core assembly</span></span>
* <span data-ttu-id="6783d-691">다중 스레드 실행에서 'Connect-AzAccount'가 실패할 수 있는 문제 해결 [#11201]</span><span class="sxs-lookup"><span data-stu-id="6783d-691">Fixed an issue that may cause 'Connect-AzAccount' to fail in multi-threaded execution [#11201]</span></span>

#### <a name="azaks"></a><span data-ttu-id="6783d-692">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="6783d-692">Az.Aks</span></span>
* <span data-ttu-id="6783d-693">이전에 사용하던 [AccessProfile API](https://docs.microsoft.com/rest/api/aks/managedclusters/getaccessprofile)를 [ListClusterAdmin](https://docs.microsoft.com/rest/api/aks/managedclusters/listclusteradmincredentials) 및 [ListClusterUser](https://docs.microsoft.com/rest/api/aks/managedclusters/listclusterusercredentials) API 호출로 대체</span><span class="sxs-lookup"><span data-stu-id="6783d-693">Replaced usage of old [AccessProfile API](https://docs.microsoft.com/rest/api/aks/managedclusters/getaccessprofile) with calls to [ListClusterAdmin](https://docs.microsoft.com/rest/api/aks/managedclusters/listclusteradmincredentials) and [ListClusterUser](https://docs.microsoft.com/rest/api/aks/managedclusters/listclusterusercredentials) APIs</span></span>

#### <a name="azbatch"></a><span data-ttu-id="6783d-694">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="6783d-694">Az.Batch</span></span>
* <span data-ttu-id="6783d-695">'Microsoft.Azure.Management.Batch' SDK 버전 11.0.0을 사용하도록 Az.Batch 업데이트</span><span class="sxs-lookup"><span data-stu-id="6783d-695">Updated Az.Batch to use 'Microsoft.Azure.Management.Batch' SDK version to 11.0.0</span></span>
* <span data-ttu-id="6783d-696">'New-AzBatchAccount' cmdlet에서 BatchAccount ID를 설정하는 기능 추가</span><span class="sxs-lookup"><span data-stu-id="6783d-696">Added the ability to set the BatchAccount Identity in the 'New-AzBatchAccount' cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="6783d-697">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="6783d-697">Az.CognitiveServices</span></span>
* <span data-ttu-id="6783d-698">계정 기능 표시 지원</span><span class="sxs-lookup"><span data-stu-id="6783d-698">Supported displaying account capabilities.</span></span>
* <span data-ttu-id="6783d-699">PublicNetworkAccess 수정 지원</span><span class="sxs-lookup"><span data-stu-id="6783d-699">Supported modifying PublicNetworkAccess.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6783d-700">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6783d-700">Az.Compute</span></span>
* <span data-ttu-id="6783d-701">Set-AzVM 및 Set-AzVmssVM cmdlet에 SimulateEviction 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="6783d-701">Added SimulateEviction parameter to Set-AzVM and Set-AzVmssVM cmdlets.</span></span>
* <span data-ttu-id="6783d-702">AzGalleryImageVersion cmdlet에 대한 StorageAccountType 매개 변수의 인수 완성자에 'Premium_LRS' 추가</span><span class="sxs-lookup"><span data-stu-id="6783d-702">Added 'Premium_LRS' to the argument completer of StorageAccountType parameter for New-AzGalleryImageVersion cmdlet.</span></span>
* <span data-ttu-id="6783d-703">VMCustomScriptExtension에 Substatuses 추가 [#11297]</span><span class="sxs-lookup"><span data-stu-id="6783d-703">Added Substatuses to VMCustomScriptExtension [#11297]</span></span>
* <span data-ttu-id="6783d-704">New-AzVM 및 New-AzVMConfig cmdlet에 대한 EvictionPolicy 매개 변수의 인수 완성자에 'Delete' 추가</span><span class="sxs-lookup"><span data-stu-id="6783d-704">Added 'Delete' to the argument completer of EvictionPolicy parameter for New-AzVM and New-AzVMConfig cmdlets.</span></span>
* <span data-ttu-id="6783d-705">새 SAP용 VM 확장의 이름 수정</span><span class="sxs-lookup"><span data-stu-id="6783d-705">Fixed name of new VM Extension for SAP</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="6783d-706">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="6783d-706">Az.DataFactory</span></span>
* <span data-ttu-id="6783d-707">ADF .Net SDK 버전을 4.9.0으로 업데이트</span><span class="sxs-lookup"><span data-stu-id="6783d-707">Updated ADF .Net SDK version to 4.9.0</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="6783d-708">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="6783d-708">Az.EventHub</span></span>
* <span data-ttu-id="6783d-709">'New-AzEventHubNamespace' 및 'Set-AzEventHubNamespace' cmdlet에 관리 ID 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="6783d-709">Added Managed Identity parameters to 'New-AzEventHubNamespace' and 'Set-AzEventHubNamespace' cmdlets</span></span>

#### <a name="azfunctions"></a><span data-ttu-id="6783d-710">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="6783d-710">Az.Functions</span></span>
* <span data-ttu-id="6783d-711">PowerShell 7.0 및 Java 11 함수 앱을 만드는 지원 추가</span><span class="sxs-lookup"><span data-stu-id="6783d-711">Added support to create PowerShell 7.0 and Java 11 function apps</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="6783d-712">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="6783d-712">Az.HDInsight</span></span>
* <span data-ttu-id="6783d-713">호스트를 나열하고 HDInsight 클러스터의 특정 호스트를 다시 시작하는 기능 지원</span><span class="sxs-lookup"><span data-stu-id="6783d-713">Supported listing hosts and restart specific hosts of the HDInsight cluster.</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="6783d-714">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="6783d-714">Az.HealthcareApis</span></span>
* <span data-ttu-id="6783d-715">SDK 버전을 1.1.0으로 업데이트</span><span class="sxs-lookup"><span data-stu-id="6783d-715">Updated the SDK version to 1.1.0</span></span>
* <span data-ttu-id="6783d-716">설정 및 관리 ID 내보내기에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="6783d-716">Added support for Export settings and Managed Identity</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="6783d-717">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="6783d-717">Az.Monitor</span></span>
* <span data-ttu-id="6783d-718">'Set-AzActivityLogAlert'에 대한 입력 개체 매개 변수 수정</span><span class="sxs-lookup"><span data-stu-id="6783d-718">Fixed input object parameter for 'Set-AzActivityLogAlert'</span></span>
* <span data-ttu-id="6783d-719">'Set-AzActionGroup'에 대한 'InputObject' 매개 변수 수정 [#10868]</span><span class="sxs-lookup"><span data-stu-id="6783d-719">Fixed 'InputObject' parameter for 'Set-AzActionGroup' [#10868]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6783d-720">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6783d-720">Az.Network</span></span>
* <span data-ttu-id="6783d-721">'Remove-AzExpressRouteCircuitConnectionConfig'에 AddressPrefixType 매개 변수 지원 추가</span><span class="sxs-lookup"><span data-stu-id="6783d-721">Added support for AddressPrefixType parameter to 'Remove-AzExpressRouteCircuitConnectionConfig'</span></span>
* <span data-ttu-id="6783d-722">Azure FirewallPolicy에 대한 새 cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="6783d-722">Added new cmdlets for Azure FirewallPolicy</span></span>
    - <span data-ttu-id="6783d-723">'New-AzFirewallPolicyDnsSetting'</span><span class="sxs-lookup"><span data-stu-id="6783d-723">'New-AzFirewallPolicyDnsSetting'</span></span>
    - <span data-ttu-id="6783d-724">방화벽 정책에 대한 네트워크 규칙에서 대상 FQDN 지원</span><span class="sxs-lookup"><span data-stu-id="6783d-724">Support for Destination FQDN in Network Rules for Firewall Policy</span></span>
* <span data-ttu-id="6783d-725">백 엔드 주소 풀 작업에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="6783d-725">Added support for backend address pool operations</span></span>
    - <span data-ttu-id="6783d-726">'New-AzLoadBalancerBackendAddressConfig'</span><span class="sxs-lookup"><span data-stu-id="6783d-726">'New-AzLoadBalancerBackendAddressConfig'</span></span>
    - <span data-ttu-id="6783d-727">'New-AzLoadBalancerBackendAddressPool'</span><span class="sxs-lookup"><span data-stu-id="6783d-727">'New-AzLoadBalancerBackendAddressPool'</span></span>
    - <span data-ttu-id="6783d-728">'Set-AzLoadBalancerBackendAddressPool'</span><span class="sxs-lookup"><span data-stu-id="6783d-728">'Set-AzLoadBalancerBackendAddressPool'</span></span>
    - <span data-ttu-id="6783d-729">'Remove-AzLoadBalancerBackendAddressPool'</span><span class="sxs-lookup"><span data-stu-id="6783d-729">'Remove-AzLoadBalancerBackendAddressPool'</span></span>
    - <span data-ttu-id="6783d-730">'Get-AzLoadBalancerBackendAddressPool'</span><span class="sxs-lookup"><span data-stu-id="6783d-730">'Get-AzLoadBalancerBackendAddressPool'</span></span>
* <span data-ttu-id="6783d-731">'New-AzIpGroup'에 대한 이름 유효성 검사 추가</span><span class="sxs-lookup"><span data-stu-id="6783d-731">Added name validation for 'New-AzIpGroup'</span></span>
* <span data-ttu-id="6783d-732">Azure FirewallPolicy에 대한 새 cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="6783d-732">Added new cmdlets for Azure FirewallPolicy</span></span>
    - <span data-ttu-id="6783d-733">'New-AzFirewallPolicyThreatIntelWhitelist'</span><span class="sxs-lookup"><span data-stu-id="6783d-733">'New-AzFirewallPolicyThreatIntelWhitelist'</span></span>
* <span data-ttu-id="6783d-734">기능에 대한 새로운 명령이 업데이트됨: VirtualWan P2SVpnGateway에서 사용자 지정 dns 서버 설정/제거</span><span class="sxs-lookup"><span data-stu-id="6783d-734">Updated below commands for feature: Custom dns servers set/remove on VirtualWan P2SVpnGateway.</span></span>
    - <span data-ttu-id="6783d-735">New-AzP2sVpnGateway 업데이트됨: 고객이 P2SVpnGateway에 설정할 dns 서버를 지정할 수 있는 선택적 매개 변수 '-CustomDnsServer'가 추가되었으며, 이 매개 변수는 지점 및 사이트 간 클라이언트에서 사용 가능</span><span class="sxs-lookup"><span data-stu-id="6783d-735">Updated New-AzP2sVpnGateway: Added optional parameter '-CustomDnsServer' for customers to specify their dns servers to set on P2SVpnGateway, which can be used by Point to site clients.</span></span>
    - <span data-ttu-id="6783d-736">Update-AzP2sVpnGateway 업데이트됨: 고객이 P2SVpnGateway에 설정할 dns 서버를 지정할 수 있는 선택적 매개 변수 '-CustomDnsServer'가 추가되었으며, 이 매개 변수는 지점 및 사이트 간 클라이언트에서 사용 가능</span><span class="sxs-lookup"><span data-stu-id="6783d-736">Updated Update-AzP2sVpnGateway: Added optional parameter '-CustomDnsServer' for customers to specify their dns servers to set on P2SVpnGateway, which can be used by Point to site clients.</span></span>
* <span data-ttu-id="6783d-737">'Update-AzVpnGateway' 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="6783d-737">Updated 'Update-AzVpnGateway'</span></span>
    - <span data-ttu-id="6783d-738">고객이 VpnGateway에 설정할 사용자 지정 bgps를 지정할 수 있도록 선택적 매개 변수 '-BgpPeeringAddress' 추가</span><span class="sxs-lookup"><span data-stu-id="6783d-738">Added optional parameter '-BgpPeeringAddress' for customers to specify their custom bgps to set on VpnGateway.</span></span>
* <span data-ttu-id="6783d-739">VirtualHub 리소스의 라우팅 상태 초기화를 지원하는 새 cmdlet 추가:</span><span class="sxs-lookup"><span data-stu-id="6783d-739">Added new cmdlet to support resetting the routing state of a VirtualHub resource:</span></span>
    - <span data-ttu-id="6783d-740">'Reset-AzHubRouter'</span><span class="sxs-lookup"><span data-stu-id="6783d-740">'Reset-AzHubRouter'</span></span>
* <span data-ttu-id="6783d-741">방화벽 정책에 대한 최근 Swagger 변화에 따라 아래 항목 업데이트</span><span class="sxs-lookup"><span data-stu-id="6783d-741">Updated below things based on recent swagger change for Firewall Policy</span></span>
    - <span data-ttu-id="6783d-742">RuleGroup, RuleCollectionGroup 및 RuleType의 이름 변경</span><span class="sxs-lookup"><span data-stu-id="6783d-742">Changes names for RuleGroup, RuleCollectionGroup and RuleType</span></span>
    - <span data-ttu-id="6783d-743">여러 NAT 규칙 컬렉션을 지원하도록 방화벽 정책 NAT 규칙 컬렉션에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="6783d-743">Added support for Firewall Policy NAT Rule Collections to support multiple NAT Rule Collection</span></span>
* <span data-ttu-id="6783d-744">[호환성이 손상되는 변경] 'New-AzFirewallPolicyApplicationRule' 및 'New-AzFirewallPolicyNetworkRule'에 대한 필수 매개 변수 'SourceIpGroup' 추가</span><span class="sxs-lookup"><span data-stu-id="6783d-744">[Breaking Change] Added mandatory parameter 'SourceIpGroup' for 'New-AzFirewallPolicyApplicationRule' and 'New-AzFirewallPolicyNetworkRule'.</span></span>
* <span data-ttu-id="6783d-745">[호환성이 손상되는 변경] 'New-AzFirewallPolicyApplicationRule' 수정, 'SourceAddress' 매개 변수를 필수로 변경</span><span class="sxs-lookup"><span data-stu-id="6783d-745">[Breaking Change] Fixed 'New-AzFirewallPolicyApplicationRule', parameter 'SourceAddress' to be mandatory.</span></span>
* <span data-ttu-id="6783d-746">[호환성이 손상되는 변경] 'New-AzFirewallPolicyApplicationRule' 수정, 'SourceAddress' 매개 변수를 필수로 변경</span><span class="sxs-lookup"><span data-stu-id="6783d-746">[Breaking Change] Fixed 'New-AzFirewallPolicyApplicationRule', parameter 'SourceAddress' to be mandatory.</span></span>
* <span data-ttu-id="6783d-747">[호환성이 손상되는 변경] 다음 필수 매개 변수 제거: 'New-AzFirewallPolicyNatRuleCollection'의 'TranslatedAddress', 'TranslatedPort'</span><span class="sxs-lookup"><span data-stu-id="6783d-747">[Breaking Change] Removed mandatory parameters: 'TranslatedAddress', 'TranslatedPort' for 'New-AzFirewallPolicyNatRuleCollection'.</span></span>
* <span data-ttu-id="6783d-748">PrivateLink On Application Gateway를 지원하는 새 cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="6783d-748">Added new cmdlets to support PrivateLink On Application Gateway</span></span>
    - <span data-ttu-id="6783d-749">'New-AzApplicationGatewayPrivateLinkConfiguration'</span><span class="sxs-lookup"><span data-stu-id="6783d-749">'New-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="6783d-750">'Get-AzApplicationGatewayPrivateLinkConfiguration'</span><span class="sxs-lookup"><span data-stu-id="6783d-750">'Get-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="6783d-751">'New-AzApplicationGatewayPrivateLinkConfiguration'</span><span class="sxs-lookup"><span data-stu-id="6783d-751">'New-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="6783d-752">'Set-AzApplicationGatewayPrivateLinkConfiguration'</span><span class="sxs-lookup"><span data-stu-id="6783d-752">'Set-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="6783d-753">'Remove-AzApplicationGatewayPrivateLinkConfiguration'</span><span class="sxs-lookup"><span data-stu-id="6783d-753">'Remove-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="6783d-754">'New-AzApplicationGatewayPrivateLinkIpConfiguration'</span><span class="sxs-lookup"><span data-stu-id="6783d-754">'New-AzApplicationGatewayPrivateLinkIpConfiguration'</span></span>
* <span data-ttu-id="6783d-755">VirtualHub의 HubRouteTables 자식 리소스에 대한 새 cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="6783d-755">Added new cmdlets for HubRouteTables child resource of VirtualHub.</span></span>
    - <span data-ttu-id="6783d-756">'New-AzVHubRoute'</span><span class="sxs-lookup"><span data-stu-id="6783d-756">'New-AzVHubRoute'</span></span>
    - <span data-ttu-id="6783d-757">'New-AzVHubRouteTable'</span><span class="sxs-lookup"><span data-stu-id="6783d-757">'New-AzVHubRouteTable'</span></span>
    - <span data-ttu-id="6783d-758">'Get-AzVHubRouteTable'</span><span class="sxs-lookup"><span data-stu-id="6783d-758">'Get-AzVHubRouteTable'</span></span>
    - <span data-ttu-id="6783d-759">'Update-AzVHubRouteTable'</span><span class="sxs-lookup"><span data-stu-id="6783d-759">'Update-AzVHubRouteTable'</span></span>
    - <span data-ttu-id="6783d-760">'Remove-AzVHubRouteTable'</span><span class="sxs-lookup"><span data-stu-id="6783d-760">'Remove-AzVHubRouteTable'</span></span>
* <span data-ttu-id="6783d-761">VirtualWan의 사용자 지정 라우팅에 대한 선택적 RoutingConfiguration 입력 매개 변수를 지원하도록 기존 cmdlet 업데이트</span><span class="sxs-lookup"><span data-stu-id="6783d-761">Updated existing cmdlets to support optional RoutingConfiguration input parameter for custom routing in VirtualWan.</span></span>
    - <span data-ttu-id="6783d-762">'New-AzExpressRouteConnection'</span><span class="sxs-lookup"><span data-stu-id="6783d-762">'New-AzExpressRouteConnection'</span></span>
    - <span data-ttu-id="6783d-763">'Set-AzExpressRouteConnection'</span><span class="sxs-lookup"><span data-stu-id="6783d-763">'Set-AzExpressRouteConnection'</span></span>
    - <span data-ttu-id="6783d-764">'New-AzVirtualHubVnetConnection'</span><span class="sxs-lookup"><span data-stu-id="6783d-764">'New-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="6783d-765">'Update-AzVirtualHubVnetConnection'</span><span class="sxs-lookup"><span data-stu-id="6783d-765">'Update-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="6783d-766">'New-AzVpnConnection'</span><span class="sxs-lookup"><span data-stu-id="6783d-766">'New-AzVpnConnection'</span></span>
    - <span data-ttu-id="6783d-767">'Update-AzVpnConnection'</span><span class="sxs-lookup"><span data-stu-id="6783d-767">'Update-AzVpnConnection'</span></span>
    - <span data-ttu-id="6783d-768">'New-AzP2sVpnGateway'</span><span class="sxs-lookup"><span data-stu-id="6783d-768">'New-AzP2sVpnGateway'</span></span>
    - <span data-ttu-id="6783d-769">'Update-AzP2sVpnGateway'</span><span class="sxs-lookup"><span data-stu-id="6783d-769">'Update-AzP2sVpnGateway'</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="6783d-770">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="6783d-770">Az.OperationalInsights</span></span>
* <span data-ttu-id="6783d-771">PSWorkspace가 IOperationalInsightsWorkspace를 구현하지 않는 버그 수정 [#12135]</span><span class="sxs-lookup"><span data-stu-id="6783d-771">Fixed bug PSWorkspace doesn't implement IOperationalInsightsWorkspace [#12135]</span></span>
* <span data-ttu-id="6783d-772">'Set-AzOperationalInsightsWorkspace'에서 'Sku' 매개 변수의 올바른 값 세트에 'pergb2018' 추가</span><span class="sxs-lookup"><span data-stu-id="6783d-772">Added 'pergb2018' to valid value set of parameter 'Sku' in 'Set-AzOperationalInsightsWorkspace'</span></span> 
* <span data-ttu-id="6783d-773">매개 변수 'FunctionParameter'에 대한 별칭 'FunctionParameters' 추가</span><span class="sxs-lookup"><span data-stu-id="6783d-773">Added alias 'FunctionParameters' for parameter 'FunctionParameter' to</span></span>
    - <span data-ttu-id="6783d-774">'New-AzOperationalInsightsSavedSearch'</span><span class="sxs-lookup"><span data-stu-id="6783d-774">'New-AzOperationalInsightsSavedSearch'</span></span>
    - <span data-ttu-id="6783d-775">'Set-AzOperationalInsightsSavedSearch'</span><span class="sxs-lookup"><span data-stu-id="6783d-775">'Set-AzOperationalInsightsSavedSearch'</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="6783d-776">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="6783d-776">Az.RecoveryServices</span></span>
* <span data-ttu-id="6783d-777">Azure Backup에서 MAB 항목을 가져오기 위한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="6783d-777">Azure Backup added support for fetching MAB items.</span></span>
* <span data-ttu-id="6783d-778">Azure Site Recovery에서 'StandardSSD_LRS' 디스크 형식 지원</span><span class="sxs-lookup"><span data-stu-id="6783d-778">Azure Site Recovery supports disk type 'StandardSSD_LRS'</span></span>

#### <a name="azresources"></a><span data-ttu-id="6783d-779">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6783d-779">Az.Resources</span></span>
* <span data-ttu-id="6783d-780">'PSADUser'에서 'UsageLocation', 'GivenName', 'Surname', 'AccountEnabled', 'MailNickname', 'Mail' 추가 [#10526] [#10497]</span><span class="sxs-lookup"><span data-stu-id="6783d-780">Added 'UsageLocation', 'GivenName', 'Surname', 'AccountEnabled', 'MailNickname', 'Mail' on 'PSADUser' [#10526] [#10497]</span></span>
* <span data-ttu-id="6783d-781">'Get-AzADUser'에서 '-Mail'이 작동하지 않는 문제 해결 [#11981]</span><span class="sxs-lookup"><span data-stu-id="6783d-781">Fixed issue that '-Mail' doesn't work on 'Get-AzADUser' [#11981]</span></span>
* <span data-ttu-id="6783d-782">'Get-AzDeploymentWhatIfResult' 및 'Get-AzResourceGroupDeploymentWhatIfResult'에 '-ExcludeChangeType' 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="6783d-782">Added '-ExcludeChangeType' parameter to 'Get-AzDeploymentWhatIfResult' and 'Get-AzResourceGroupDeploymentWhatIfResult'</span></span>
* <span data-ttu-id="6783d-783">'New-AzDeployment' 및 'New-AzResourceGroupDeployment'에 '-WhatIfExcludeChangeType' 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="6783d-783">Added '-WhatIfExcludeChangeType' parameter to 'New-AzDeployment' and 'New-AzResourceGroupDeployment'</span></span>
* <span data-ttu-id="6783d-784">보다 나은 오류 메시지를 표시하도록 'Test-Az\*Deployment' cmdlet 업데이트</span><span class="sxs-lookup"><span data-stu-id="6783d-784">Updated 'Test-Az\*Deployment' cmdlets to show better error messages</span></span>
* <span data-ttu-id="6783d-785">deployment create 및 What-If cmdlet의 '-Name' 매개 변수에 대한 도움말 메시지 수정</span><span class="sxs-lookup"><span data-stu-id="6783d-785">Fixed help message for '-Name' parameter of deployment create and What-If cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="6783d-786">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6783d-786">Az.Sql</span></span>
* <span data-ttu-id="6783d-787">Set SQL Server Azure Active Directory Admin cmdlet의 서비스 주체에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="6783d-787">Added support for service principal for Set SQL Server Azure Active Directory Admin cmdlet</span></span>
* <span data-ttu-id="6783d-788">데이터 분류 cmdlet의 동기화 문제 해결</span><span class="sxs-lookup"><span data-stu-id="6783d-788">Fixed sync issue in Data Classification cmdlets.</span></span>
* <span data-ttu-id="6783d-789">'Set-AzSqlServerActiveDirectoryAdministrator'에서 메일로 사용자 검색 지원 [#12192]</span><span class="sxs-lookup"><span data-stu-id="6783d-789">Supported searching user by mail on 'Set-AzSqlServerActiveDirectoryAdministrator' [#12192]</span></span>

#### <a name="azstorage"></a><span data-ttu-id="6783d-790">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="6783d-790">Az.Storage</span></span>
* <span data-ttu-id="6783d-791">RequireInfrastructureEncryption을 사용하여 스토리지 계정 만들기 지원</span><span class="sxs-lookup"><span data-stu-id="6783d-791">Supported create Storage account with RequireInfrastructureEncryption</span></span>
    -  <span data-ttu-id="6783d-792">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="6783d-792">'New-AzStorageAccount'</span></span>
* <span data-ttu-id="6783d-793">Azure.Core 로딩 논리를 Az.Accounts로 이동</span><span class="sxs-lookup"><span data-stu-id="6783d-793">Moved the logic of loading Azure.Core to Az.Accounts</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="6783d-794">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="6783d-794">Az.Websites</span></span>
* <span data-ttu-id="6783d-795">'Restore-AzDeletedWebApp'에서 복원이 실패할 경우 생성된 웹앱을 삭제하는 보호 기능 추가</span><span class="sxs-lookup"><span data-stu-id="6783d-795">Added safeguard to delete created webapp if restore failed in 'Restore-AzDeletedWebApp'</span></span>
* <span data-ttu-id="6783d-796">'New-AzWebApp' 및 'New-AzWebAppSlot'에 대한 'SourceWebApp.Location' 추가</span><span class="sxs-lookup"><span data-stu-id="6783d-796">Added 'SourceWebApp.Location' for 'New-AzWebApp' and 'New-AzWebAppSlot'</span></span>
* <span data-ttu-id="6783d-797">'Set-AzWebApp' 및 'Set-AzWebAppSlot'에서 컨테이너 설정을 변경할 수 없는 버그 수정</span><span class="sxs-lookup"><span data-stu-id="6783d-797">Fixed bug that prevented changing Container settings in 'Set-AzWebApp' and 'Set-AzWebAppSlot'</span></span>
* <span data-ttu-id="6783d-798">Get-AzWebApp에 대한 -Name을 제공하지 않으면 SiteConfig를 가져오는 버그 수정</span><span class="sxs-lookup"><span data-stu-id="6783d-798">Fixed bug to get SiteConfig when -Name is not given for Get-AzWebApp</span></span>
* <span data-ttu-id="6783d-799">Linux 앱용 ASP를 만드는 지원 추가</span><span class="sxs-lookup"><span data-stu-id="6783d-799">Added a support to create ASP for Linux Apps</span></span>
* <span data-ttu-id="6783d-800">리소스 그룹 간 복제에 대한 예외 추가</span><span class="sxs-lookup"><span data-stu-id="6783d-800">Added exceptions for clone across resource groups</span></span>

## <a name="420---june-2020"></a><span data-ttu-id="6783d-801">4.2.0 - 2020년 6월</span><span class="sxs-lookup"><span data-stu-id="6783d-801">4.2.0 - June 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="6783d-802">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6783d-802">Az.Accounts</span></span>
* <span data-ttu-id="6783d-803">Azure Automation 또는 PowerShell 작업에서 Az가 로그를 건너뛸 수 있는 문제 수정[#11492]</span><span class="sxs-lookup"><span data-stu-id="6783d-803">Fixed an issue that may cause Az to skip logs in Azure Automation or PowerShell jobs [#11492]</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="6783d-804">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="6783d-804">Az.AnalysisServices</span></span>
* <span data-ttu-id="6783d-805">데이터 평면 cmdlet의 어셈블리 버전 업데이트</span><span class="sxs-lookup"><span data-stu-id="6783d-805">Updated assembly version of data plane cmdlets</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="6783d-806">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="6783d-806">Az.ApiManagement</span></span>
* <span data-ttu-id="6783d-807">서비스 관리 cmdlet의 어셈블리 버전 업데이트</span><span class="sxs-lookup"><span data-stu-id="6783d-807">Updated assembly version of service management cmdlets</span></span>

#### <a name="azbilling"></a><span data-ttu-id="6783d-808">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="6783d-808">Az.Billing</span></span>
* <span data-ttu-id="6783d-809">소비 cmdlet의 어셈블리 버전 업데이트</span><span class="sxs-lookup"><span data-stu-id="6783d-809">Updated assembly version of consumption cmdlets</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="6783d-810">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="6783d-810">Az.CognitiveServices</span></span>
* <span data-ttu-id="6783d-811">PrivateEndpoint 및 PublicNetworkAccess control을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-811">Support PrivateEndpoint and PublicNetworkAccess control.</span></span> 

#### <a name="azdatafactory"></a><span data-ttu-id="6783d-812">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="6783d-812">Az.DataFactory</span></span>
* <span data-ttu-id="6783d-813">데이터 팩터리 V2 cmdlet의 어셈블리 버전 업데이트</span><span class="sxs-lookup"><span data-stu-id="6783d-813">Updated assembly version of data factory V2 cmdlets</span></span>

#### <a name="azdatashare"></a><span data-ttu-id="6783d-814">Az.DataShare</span><span class="sxs-lookup"><span data-stu-id="6783d-814">Az.DataShare</span></span>
* <span data-ttu-id="6783d-815">''Az.DataShare'' 모듈의 일반 공급</span><span class="sxs-lookup"><span data-stu-id="6783d-815">General availability of ''Az.DataShare'' module</span></span>

#### <a name="azdesktopvirtualization"></a><span data-ttu-id="6783d-816">Az.DesktopVirtualization</span><span class="sxs-lookup"><span data-stu-id="6783d-816">Az.DesktopVirtualization</span></span>
* <span data-ttu-id="6783d-817">''Az.DesktopVirtualization'' 모듈의 일반 공급</span><span class="sxs-lookup"><span data-stu-id="6783d-817">General availability of ''Az.DesktopVirtualization'' module</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="6783d-818">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="6783d-818">Az.OperationalInsights</span></span>
* <span data-ttu-id="6783d-819">SDK를 0.21.0으로 업그레이드</span><span class="sxs-lookup"><span data-stu-id="6783d-819">Upgraded SDK to 0.21.0</span></span>
* <span data-ttu-id="6783d-820">다음에 선택적 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="6783d-820">Added optional parameters to</span></span> 
    - <span data-ttu-id="6783d-821">'New-AzOperationalInsightsSavedSearch'</span><span class="sxs-lookup"><span data-stu-id="6783d-821">'New-AzOperationalInsightsSavedSearch'</span></span>
    - <span data-ttu-id="6783d-822">'Set-AzOperationalInsightsSavedSearch'</span><span class="sxs-lookup"><span data-stu-id="6783d-822">'Set-AzOperationalInsightsSavedSearch'</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="6783d-823">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="6783d-823">Az.PolicyInsights</span></span>
* <span data-ttu-id="6783d-824">'Start-AzPolicyComplianceScan'의 예제 3 수정</span><span class="sxs-lookup"><span data-stu-id="6783d-824">Corrected example 3 for 'Start-AzPolicyComplianceScan'</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="6783d-825">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="6783d-825">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="6783d-826">PowerBI cmdlet의 어셈블리 버전 업데이트</span><span class="sxs-lookup"><span data-stu-id="6783d-826">Updated assembly version of PowerBI cmdlets</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="6783d-827">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="6783d-827">Az.PrivateDns</span></span>
* <span data-ttu-id="6783d-828">Remove-AzPrivateDnsRecordSet에 대한 자세한 정보 출력 문자열 형식 수정</span><span class="sxs-lookup"><span data-stu-id="6783d-828">Corrected verbose output string formatting for Remove-AzPrivateDnsRecordSet</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="6783d-829">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="6783d-829">Az.RecoveryServices</span></span>
* <span data-ttu-id="6783d-830">xml 입력에서 영역 간 복제를 위한 복구 계획을 세우기 위한 Azure Site Recovery 지원.</span><span class="sxs-lookup"><span data-stu-id="6783d-830">Azure Site Recovery support for creating recovery plan for zone to zone replication from xml input.</span></span>
* <span data-ttu-id="6783d-831">SiteRecovery 및 Backup cmdlet의 어셈블리 버전 업데이트</span><span class="sxs-lookup"><span data-stu-id="6783d-831">Updated assembly version of SiteRecovery and Backup cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="6783d-832">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6783d-832">Az.Resources</span></span>
* <span data-ttu-id="6783d-833">Get-AzDeploymentScriptLog 및 Save-AzDeploymentScriptLog cmdlet에 Tail 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="6783d-833">Added Tail parameter to Get-AzDeploymentScriptLog and Save-AzDeploymentScriptLog cmdlets</span></span>
* <span data-ttu-id="6783d-834">형식이 지정된 출력 속성을 Get-AzDeploymentScript cmdlet 출력에 표시</span><span class="sxs-lookup"><span data-stu-id="6783d-834">Formatted Output property and show it on the Get-AzDeploymentScript cmdlet output</span></span>
* <span data-ttu-id="6783d-835">-DeploymentScriptInputObject 매개 변수의 이름이 -DeploymentScriptObject로 변경</span><span class="sxs-lookup"><span data-stu-id="6783d-835">Renamed -DeploymentScriptInputObject parameter to -DeploymentScriptObject</span></span>
* <span data-ttu-id="6783d-836">cmdlet 메시지에서 누락된 파일/대상 이름이 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-836">Fixed missing file/target name in cmdlet messages.</span></span>
* <span data-ttu-id="6783d-837">리소스 관리자 및 태그 cmdlet의 어셈블리 버전 업데이트</span><span class="sxs-lookup"><span data-stu-id="6783d-837">Updated assembly version of resource manager and tags cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="6783d-838">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6783d-838">Az.Sql</span></span>
* <span data-ttu-id="6783d-839">UsePrivateLinkConnection을 'New-AzSqlSyncGroup', 'Update-AzSqlSyncGroup', 'New-AzSqlSyncMember' 및 'Update-AzSqlSyncMember'에 추가</span><span class="sxs-lookup"><span data-stu-id="6783d-839">Added UsePrivateLinkConnection to 'New-AzSqlSyncGroup', 'Update-AzSqlSyncGroup', 'New-AzSqlSyncMember' and 'Update-AzSqlSyncMember'</span></span>
* <span data-ttu-id="6783d-840">SyncMemberAzureDatabaseResourceId를 'New-AzSqlSyncMember' 및 'Update-AzSqlSyncMember'에 추가</span><span class="sxs-lookup"><span data-stu-id="6783d-840">Added SyncMemberAzureDatabaseResourceId to 'New-AzSqlSyncMember' and 'Update-AzSqlSyncMember'</span></span>
* <span data-ttu-id="6783d-841">SQL Server Azure Active Directory Admin cmdlet을 설정하는 게스트 사용자 조회 지원 추가</span><span class="sxs-lookup"><span data-stu-id="6783d-841">Added Guest user lookup support to Set SQL Server Azure Active Directory Admin cmdlet</span></span>

#### <a name="azstorage"></a><span data-ttu-id="6783d-842">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="6783d-842">Az.Storage</span></span>
* <span data-ttu-id="6783d-843">데이터 평면 cmdlet의 어셈블리 버전 업데이트</span><span class="sxs-lookup"><span data-stu-id="6783d-843">Updated assembly version of data plane cmdlets</span></span>

## <a name="410---may-2020"></a><span data-ttu-id="6783d-844">4.1.0 - 2020년 5월</span><span class="sxs-lookup"><span data-stu-id="6783d-844">4.1.0 - May 2020</span></span>
### <a name="highlights-since-the-last-release"></a><span data-ttu-id="6783d-845">마지막 릴리스 이후의 주요 사항</span><span class="sxs-lookup"><span data-stu-id="6783d-845">Highlights since the last release</span></span>
* <span data-ttu-id="6783d-846">지원되는 PowerShell 버전: Windows PowerShell 5.1, PowerShell Core 6.2.4 이상, PowerShell 7</span><span class="sxs-lookup"><span data-stu-id="6783d-846">Supported PowerShell versions: Windows PowerShell 5.1, PowerShell Core 6.2.4+, PowerShell 7</span></span>
* <span data-ttu-id="6783d-847">Az.Functions 일반 공급</span><span class="sxs-lookup"><span data-stu-id="6783d-847">General availability of Az.Functions</span></span> 
* <span data-ttu-id="6783d-848">Az.ApiManagement, Az.Batch, Az.Compute, Az.KeyVault, Az.Monitor, Az.Network, Az.OperationalInsights, Az.Resources 및 Az.Storage의 주요 릴리스 출시</span><span class="sxs-lookup"><span data-stu-id="6783d-848">Az.ApiManagement, Az.Batch, Az.Compute, Az.KeyVault, Az.Monitor, Az.Network, Az.OperationalInsights, Az.Resources, and Az.Storage have major release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="6783d-849">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6783d-849">Az.Accounts</span></span>
* <span data-ttu-id="6783d-850">'AzureSynapseAnalyticsEndpointResourceId' 및 'AzureSynapseAnalyticsEndpointSuffix' 매개 변수를 허용하도록 'Add-AzEnvironment' 및 'Set-AzEnvironment' 업데이트</span><span class="sxs-lookup"><span data-stu-id="6783d-850">Updated 'Add-AzEnvironment' and 'Set-AzEnvironment' to accept parameters 'AzureSynapseAnalyticsEndpointResourceId' and 'AzureSynapseAnalyticsEndpointSuffix'</span></span>
* <span data-ttu-id="6783d-851">Az.Accounts에 Azure.Core 관련 어셈블리가 추가되었으며 지원되는 PowerShell 플랫폼은 Windows PowerShell 5.1, PowerShell Core 6.2.4, PowerShell 7+입니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-851">Added Azure.Core related assemblies into Az.Accounts, supported PowerShell platforms include Windows PowerShell 5.1, PowerShell Core 6.2.4, PowerShell 7+</span></span>

#### <a name="azaks"></a><span data-ttu-id="6783d-852">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="6783d-852">Az.Aks</span></span>
* <span data-ttu-id="6783d-853">API 버전을 2019-10-01로 업그레이드</span><span class="sxs-lookup"><span data-stu-id="6783d-853">Upgraded API Version to 2019-10-01</span></span>
* <span data-ttu-id="6783d-854">Windows 컨테이너를 사용하여 AKS 만들기 지원</span><span class="sxs-lookup"><span data-stu-id="6783d-854">Supported to create AKS using Windows container</span></span>
* <span data-ttu-id="6783d-855">새 cmdlet 추가: 'New-AzAksNodePool', 'Update-AzAksNodePool', 'Remove-AzAksNodePool', 'Get-AzAksNodePool', 'Install-AzAksKubectl', 'Get-AzAksVersion'</span><span class="sxs-lookup"><span data-stu-id="6783d-855">Provided new cmdlets: 'New-AzAksNodePool', 'Update-AzAksNodePool', 'Remove-AzAksNodePool',        'Get-AzAksNodePool', 'Install-AzAksKubectl', 'Get-AzAksVersion'</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="6783d-856">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="6783d-856">Az.ApiManagement</span></span>
* <span data-ttu-id="6783d-857">'New-AzApiManagement' 및 'Set-AzApiManagement': [-AssignIdentity] 매개 변수 이름을 [-SystemAssignedIdentity]로 변경</span><span class="sxs-lookup"><span data-stu-id="6783d-857">'New-AzApiManagement' and 'Set-AzApiManagement': [-AssignIdentity] parameter renamed as [-SystemAssignedIdentity]</span></span>
* <span data-ttu-id="6783d-858">'New-AzApiManagement' 및 'Set-AzApiManagement': 새 매개 변수 추가: [-UserAssignedIdentity <String[]>]</span><span class="sxs-lookup"><span data-stu-id="6783d-858">'New-AzApiManagement' and 'Set-AzApiManagement': New parameter added: [-UserAssignedIdentity <String[]>]</span></span>
* <span data-ttu-id="6783d-859">'Get-AzApiManagementProperty': 'Get-AzApiManagementNamedValue'로 이름 변경.</span><span class="sxs-lookup"><span data-stu-id="6783d-859">'Get-AzApiManagementProperty': renamed as 'Get-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="6783d-860">PropertyId 매개 변수 이름을 NamedValueId로 변경.</span><span class="sxs-lookup"><span data-stu-id="6783d-860">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="6783d-861">'New-AzApiManagementProperty': 'New-AzApiManagementNamedValue'로 이름 변경.</span><span class="sxs-lookup"><span data-stu-id="6783d-861">'New-AzApiManagementProperty': renamed as 'New-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="6783d-862">PropertyId 매개 변수 이름을 NamedValueId로 변경.</span><span class="sxs-lookup"><span data-stu-id="6783d-862">PropertyId parameter renamed as NamedValueId.</span></span> 
* <span data-ttu-id="6783d-863">'Set-AzApiManagementProperty': 'Set-AzApiManagementNamedValue'로 이름 변경.</span><span class="sxs-lookup"><span data-stu-id="6783d-863">'Set-AzApiManagementProperty': renamed as 'Set-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="6783d-864">PropertyId 매개 변수 이름을 NamedValueId로 변경.</span><span class="sxs-lookup"><span data-stu-id="6783d-864">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="6783d-865">'Remove-AzApiManagementProperty': 'Remove-AzApiManagementNamedValue'로 이름 변경.</span><span class="sxs-lookup"><span data-stu-id="6783d-865">'Remove-AzApiManagementProperty': renamed as 'Remove-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="6783d-866">PropertyId 매개 변수 이름을 NamedValueId로 변경.</span><span class="sxs-lookup"><span data-stu-id="6783d-866">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="6783d-867">새 'Get-AzApiManagementAuthorizationServerClientSecret' cmdlet이 추가되었으며 'Get-AzApiManagementAuthorizationServer'는 더 이상 클라이언트 암호를 반환하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-867">Added new 'Get-AzApiManagementAuthorizationServerClientSecret' cmdlet and 'Get-AzApiManagementAuthorizationServer' will not return client secret anymore.</span></span>
* <span data-ttu-id="6783d-868">새 'Get-AzApiManagementNamedValueSecretValue' cmdlet이 추가되었으며 'Get-AzApiManagementNamedValue'는 더 이상 비밀 값을 반환하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-868">Added new 'Get-AzApiManagementNamedValueSecretValue' cmdlet and 'Get-AzApiManagementNamedValue' will not return secret value.</span></span>
* <span data-ttu-id="6783d-869">새 'Get-AzApiManagementOpenIdConnectProviderClientSecret' cmdlet이 추가되었으며 'Get-AzApiManagementOpenIdConnectProvider'는 더 이상 클라이언트 암호를 반환하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-869">Added new 'Get-AzApiManagementOpenIdConnectProviderClientSecret' cmdlet and 'Get-AzApiManagementOpenIdConnectProvider' will not return client secret anymore.</span></span>
* <span data-ttu-id="6783d-870">새 'Get-AzApiManagementSubscriptionKey' cmdlet이 추가되었으며 'Get-AzApiManagementSubscription'은 더 이상 구독 키를 반환하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-870">Added new 'Get-AzApiManagementSubscriptionKey' cmdlet and 'Get-AzApiManagementSubscription' will not return subscription keys anymore.</span></span>
* <span data-ttu-id="6783d-871">새 'Get-AzApiManagementTenantAccessSecret' cmdlet이 추가되었으며 'Get-AzApiManagementTenantAccess'는 더 이상 키를 반환하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-871">Added new 'Get-AzApiManagementTenantAccessSecret' cmdlet and 'Get-AzApiManagementTenantAccess' will not return keys anymore.</span></span>
* <span data-ttu-id="6783d-872">새 'Get-AzApiManagementTenantGitAccessSecret' cmdlet이 추가되었으며 'Get-AzApiManagementTenantGitAccess'는 더 이상 키를 반환하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-872">Added new 'Get-AzApiManagementTenantGitAccessSecret' cmdlet and 'Get-AzApiManagementTenantGitAccess' will not return keys anymore.</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="6783d-873">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="6783d-873">Az.ApplicationInsights</span></span>
* <span data-ttu-id="6783d-874">매개 변수 추가: 'New-AzApplicationInsights'에 대한 'RetentionInDays' 'PublicNetworkAccessForIngestion' 'PublicNetworkAccessForQuery'</span><span class="sxs-lookup"><span data-stu-id="6783d-874">Added Parameters: 'RetentionInDays' 'PublicNetworkAccessForIngestion' 'PublicNetworkAccessForQuery' for 'New-AzApplicationInsights'</span></span>
* <span data-ttu-id="6783d-875">'Update-AzApplicationInsights' cmdlet 작성</span><span class="sxs-lookup"><span data-stu-id="6783d-875">Created cmdlet 'Update-AzApplicationInsights'</span></span>
* <span data-ttu-id="6783d-876">연결된 스토리지 계정에 대한 cmdlet 작성</span><span class="sxs-lookup"><span data-stu-id="6783d-876">Created cmdlets for Linked Storage Account</span></span>

#### <a name="azbatch"></a><span data-ttu-id="6783d-877">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="6783d-877">Az.Batch</span></span>
* <span data-ttu-id="6783d-878">'Microsoft.Azure.Batch' SDK 버전 13.0.0 및 'Microsoft.Azure.Management.Batch' SDK 버전 9.0.0을 사용하도록 Az.Batch가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-878">Updated Az.Batch to use 'Microsoft.Azure.Batch' SDK version 13.0.0 and 'Microsoft.Azure.Management.Batch' SDK version 9.0.0.</span></span>
* <span data-ttu-id="6783d-879">새 '-CertificateKind' 매개 변수를 사용하여 'AzBatchCertificate'에 추가할 인증서 종류를 선택하는 기능이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-879">Added the ability to select the kind of certificate being added using the new '-CertificateKind' parameter to 'New-AzBatchCertificate'.</span></span>
* <span data-ttu-id="6783d-880">이전에 항상 ''였던 'ApplicationPackages' 속성이 'PSApplication'에서 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-880">Removed 'ApplicationPackages' property from 'PSApplication' which was previously always ''.</span></span>
  - <span data-ttu-id="6783d-881">이제 'Get-AzBatchApplicationPackage'를 사용하여 애플리케이션 내부의 특정 패키지를 검색할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-881">The specific packages inside of an application now can be retrieved using 'Get-AzBatchApplicationPackage'.</span></span> <span data-ttu-id="6783d-882">예를 들면 다음과 같습니다. 'Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication'.</span><span class="sxs-lookup"><span data-stu-id="6783d-882">For example: 'Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication'.</span></span>
* <span data-ttu-id="6783d-883">'New-AzBatchPool'을 사용하여 풀을 만들 때 'PSImageReference'의 'VirtualMachineImageId' 속성은 이제 Shared Image Gallery 이미지만 참조할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-883">When creating a pool using 'New-AzBatchPool', the 'VirtualMachineImageId' property of 'PSImageReference' can now only refer to a Shared Image Gallery image.</span></span>
* <span data-ttu-id="6783d-884">'New-AzBatchPool'을 사용하여 풀을 만들 때 공용 IP 없이 'PSNetworkConfiguration'의 새 'PublicIPAddressConfiguration'을 사용하여 풀을 프로비저닝할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-884">When creating a pool using 'New-AzBatchPool', the pool can be provisioned without a public IP using the new 'PublicIPAddressConfiguration' property of 'PSNetworkConfiguration'.</span></span>
  - <span data-ttu-id="6783d-885">'PSNetworkConfiguration'의 'PublicIPs' 속성도 'PSPublicIPAddressConfiguration'으로 이동되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-885">The 'PublicIPs' property of 'PSNetworkConfiguration' has moved in to 'PSPublicIPAddressConfiguration' as well.</span></span> <span data-ttu-id="6783d-886">이 속성은 'IPAddressProvisioningType'이 'UserManaged'인 경우에만 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-886">This property can only be specified if 'IPAddressProvisioningType' is 'UserManaged'.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6783d-887">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6783d-887">Az.Compute</span></span>
* <span data-ttu-id="6783d-888">'Update-AzVM' cmdlet에 HostId 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="6783d-888">Added HostId parameter to 'Update-AzVM' cmdlet</span></span>
* <span data-ttu-id="6783d-889">'New-AzVMConfig', 'New-AzVmssConfig', 'Update-AzVmss', 'Set-AzVMOperatingSystem' 및 'Set-AzVmssOsProfile' cmdlet의 도움말 문서가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-889">Updated Help documents for 'New-AzVMConfig', 'New-AzVmssConfig', 'Update-AzVmss', 'Set-AzVMOperatingSystem' and 'Set-AzVmssOsProfile' cmdlets.</span></span>
* <span data-ttu-id="6783d-890">주요 변경 내용</span><span class="sxs-lookup"><span data-stu-id="6783d-890">Breaking changes</span></span>
    - <span data-ttu-id="6783d-891">'Get-AzVMImage' cmdlet에서 FilterExpression 매개 변수가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-891">FilterExpression parameter is removed from 'Get-AzVMImage' cmdlet.</span></span>
    - <span data-ttu-id="6783d-892">'New-AzVmssConfig', 'New-AzVMConfig' 및 'Update-AzVM' cmdlet에서 AssignIdentity 매개 변수가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-892">AssignIdentity parameter is removed from 'New-AzVmssConfig', 'New-AzVMConfig' and 'Update-AzVM' cmdlets.</span></span>
    - <span data-ttu-id="6783d-893">'New-AzVmssConfig' 및 'Update-AzVmss' cmdlet에서 AutomaticRepairMaxInstanceRepairsPercent가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-893">AutomaticRepairMaxInstanceRepairsPercent is removed from 'New-AzVmssConfig' and 'Update-AzVmss' cmdlets.</span></span>
    - <span data-ttu-id="6783d-894">ProximityPlacementGroup에서 AvailabilitySetsColocationStatus, VirtualMachinesColocationStatus 및 VirtualMachineScaleSetsColocationStatus 속성이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-894">AvailabilitySetsColocationStatus, VirtualMachinesColocationStatus and VirtualMachineScaleSetsColocationStatus properties are removed from ProximityPlacementGroup.</span></span>
    - <span data-ttu-id="6783d-895">AutomaticRepairsPolicy에서 MaxInstanceRepairsPercent 속성이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-895">MaxInstanceRepairsPercent property is removed from AutomaticRepairsPolicy.</span></span>
    - <span data-ttu-id="6783d-896">AvailabilitySets, VirtualMachines 및 VirtualMachineScaleSets 형식이 IList<SubResource>에서 IList<SubResourceWithColocationStatus>로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-896">The types of AvailabilitySets, VirtualMachines and VirtualMachineScaleSets are changed from IList<SubResource> to IList<SubResourceWithColocationStatus>.</span></span>
* <span data-ttu-id="6783d-897">'Get-AzVM' cmdlet에 대한 설명이 보다 정확하게 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-897">Description for 'Get-AzVM' cmdlet has been updated to better describe it.</span></span> 

#### <a name="azdatafactory"></a><span data-ttu-id="6783d-898">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="6783d-898">Az.DataFactory</span></span>
* <span data-ttu-id="6783d-899">Managed IR에서 데이터 흐름 런타임 속성의 CRUD를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-899">Supported CRUD of data flow runtime properties in Managed IR.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="6783d-900">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="6783d-900">Az.FrontDoor</span></span>
* <span data-ttu-id="6783d-901">Front Door 규칙 엔진 개체를 생성, 업데이트, 검색 및 삭제할 수 있는 새 cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="6783d-901">Added new cmdlets for creation, update, retreival, and deletion of Front Door Rules Engine object</span></span>
* <span data-ttu-id="6783d-902">Front Door 규칙 엔진 개체를 작성할 수 있는 도우미 cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="6783d-902">Added helper cmdlets for construction of Front Door Rules Engine object</span></span>
* <span data-ttu-id="6783d-903">Front Door 회람 규칙 개체에 대한 규칙 엔진 참조 추가</span><span class="sxs-lookup"><span data-stu-id="6783d-903">Added Rules Engine reference to Front Door Routing Rule object.</span></span>
* <span data-ttu-id="6783d-904">Front Door 백 엔드 개체에 Private Link 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="6783d-904">Added Private Link parameters to Front Door Backend object</span></span>

#### <a name="azfunctions"></a><span data-ttu-id="6783d-905">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="6783d-905">Az.Functions</span></span>
* <span data-ttu-id="6783d-906">''Az.Functions'' 모듈의 일반 공급</span><span class="sxs-lookup"><span data-stu-id="6783d-906">General availability of ''Az.Functions'' module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="6783d-907">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="6783d-907">Az.HDInsight</span></span>
* <span data-ttu-id="6783d-908">고객 관리형 키 디스크 암호화 지원</span><span class="sxs-lookup"><span data-stu-id="6783d-908">Supported Customer-managed key disk encryption.</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="6783d-909">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="6783d-909">Az.HealthcareApis</span></span>
* <span data-ttu-id="6783d-910">더 이상 액세스 정책이 기본적으로 현재 보안 주체로 설정되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-910">Access policies are no longer defaulted to the current principal</span></span>

#### <a name="aziothub"></a><span data-ttu-id="6783d-911">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="6783d-911">Az.IotHub</span></span>
* <span data-ttu-id="6783d-912">SQL과 비슷한 언어를 사용하여 정보를 검색하기 위해 IoT 허브에서 쿼리를 호출하는 cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-912">Added cmdlet to invoke a query in an IoT hub to retrieve information using a SQL-like language.</span></span>
* <span data-ttu-id="6783d-913">'Add-AzIotHubDevice'가 자식 디바이스 없는 에지 지원 디바이스를 만들 수 없는 문제 해결 [#11597]</span><span class="sxs-lookup"><span data-stu-id="6783d-913">Fix issue that 'Add-AzIotHubDevice' fails to create Edge Enabled Device without child devices [#11597]</span></span>
* <span data-ttu-id="6783d-914">IoT Hub, 디바이스 또는 모듈에 대한 SAS 토큰을 생성하는 cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-914">Added cmdlet to generate SAS token for Iot Hub, device or module.</span></span>
* <span data-ttu-id="6783d-915">구성 메트릭 쿼리를 호출하는 cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-915">Added cmdlet to invoke configuration metrics query.</span></span>
* <span data-ttu-id="6783d-916">IoT Edge 자동 배포를 대규모로 관리합니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-916">Manage IoT Edge automatic deployment at scale.</span></span> <span data-ttu-id="6783d-917">새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-917">New cmdlets are:</span></span>
    - <span data-ttu-id="6783d-918">'Add-AzIotHubDeployment'</span><span class="sxs-lookup"><span data-stu-id="6783d-918">'Add-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="6783d-919">'Get-AzIotHubDeployment'</span><span class="sxs-lookup"><span data-stu-id="6783d-919">'Get-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="6783d-920">'Remove-AzIotHubDeployment'</span><span class="sxs-lookup"><span data-stu-id="6783d-920">'Remove-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="6783d-921">'Set-AzIotHubDeployment'</span><span class="sxs-lookup"><span data-stu-id="6783d-921">'Set-AzIotHubDeployment'</span></span>
* <span data-ttu-id="6783d-922">IoT Edge 배포 메트릭 쿼리를 호출하는 cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-922">Added cmdlet to invoke an IoT Edge deployment metrics query.</span></span>
* <span data-ttu-id="6783d-923">지정된 에지 디바이스에 구성 콘텐츠를 적용하는 cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-923">Added cmdlet to apply the configuration content to the specified edge device.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="6783d-924">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="6783d-924">Az.KeyVault</span></span>
* <span data-ttu-id="6783d-925">다음 별칭 제거: 'New-AzKeyVaultCertificateAdministratorDetails' 및 'New-AzKeyVaultCertificateOrganizationDetails'</span><span class="sxs-lookup"><span data-stu-id="6783d-925">Removed two aliases: 'New-AzKeyVaultCertificateAdministratorDetails' and 'New-AzKeyVaultCertificateOrganizationDetails'</span></span>
* <span data-ttu-id="6783d-926">키 자격 증명 모음을 만들 때 기본적으로 일시 삭제 사용</span><span class="sxs-lookup"><span data-stu-id="6783d-926">Enabled soft delete by default when creating a key vault</span></span>
* <span data-ttu-id="6783d-927">키 자격 증명 모음을 만들 때 특정 네트워크 위치의 액세스를 제어하도록 네트워크 규칙을 설정할 수 있음</span><span class="sxs-lookup"><span data-stu-id="6783d-927">Network rules can be set to govern the accessibility from specific network locations when creating a key vault</span></span>
* <span data-ttu-id="6783d-928">BYOK(Bring Your Own Key) 지원 추가</span><span class="sxs-lookup"><span data-stu-id="6783d-928">Added support to bring your own key (BYOK)</span></span>
    - <span data-ttu-id="6783d-929">'Add-AzKeyVaultKey'가 키 교환 키 생성 지원</span><span class="sxs-lookup"><span data-stu-id="6783d-929">'Add-AzKeyVaultKey' supports generating a key exchange key</span></span>
    - <span data-ttu-id="6783d-930">'Get-AzKeyVaultKey'가 PEM 형식의 공개 키 다운로드 지원</span><span class="sxs-lookup"><span data-stu-id="6783d-930">'Get-AzKeyVaultKey' supports downloading a public key in PEM format</span></span>
* <span data-ttu-id="6783d-931">'AzKeyVaultKey' 도움말 문서의 'KeyOps' 부분 업데이트</span><span class="sxs-lookup"><span data-stu-id="6783d-931">Updated the 'KeyOps' part of the help document of 'Add-AzKeyVaultKey'</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="6783d-932">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="6783d-932">Az.Monitor</span></span>
* <span data-ttu-id="6783d-933">'Set-AzDiagnosticSettings'의 버그 수정, 일부 범주에는 보존 정책이 적용되지 않음 [#11589]</span><span class="sxs-lookup"><span data-stu-id="6783d-933">Fixed bug for 'Set-AzDiagnosticSettings', retention policy won't apply to all categories [#11589]</span></span>
* <span data-ttu-id="6783d-934">메트릭 경고 V2에 WebTest를 사용하기 위한 조건 지원</span><span class="sxs-lookup"><span data-stu-id="6783d-934">Supported WebTest availability criteria for metric alert V2</span></span>
    - <span data-ttu-id="6783d-935">'New-AzMetricAlertRuleV2Criteria': webtest 사용 조건을 만드는 옵션 추가</span><span class="sxs-lookup"><span data-stu-id="6783d-935">'New-AzMetricAlertRuleV2Criteria': an option to create webtest availability criteria was added</span></span>
    - <span data-ttu-id="6783d-936">'Add-AzMetricAlertRuleV2': 새 webtest 사용 조건 지원</span><span class="sxs-lookup"><span data-stu-id="6783d-936">'Add-AzMetricAlertRuleV2': supports the new webtest availability criteria</span></span>
* <span data-ttu-id="6783d-937">PSLogProfile에서 RetentionPolicy에 대한 중복 정의 제거 [#7608]</span><span class="sxs-lookup"><span data-stu-id="6783d-937">Removed redundant definition for RetentionPolicy in PSLogProfile [#7608]</span></span>
* <span data-ttu-id="6783d-938">PSEventData에 정의된 중복 속성 제거 [#11353]</span><span class="sxs-lookup"><span data-stu-id="6783d-938">Removed redundant properties difined in PSEventData [#11353]</span></span>
* <span data-ttu-id="6783d-939">'Get-AzLog'를 'Get-AzActivityLog'로 이름 변경</span><span class="sxs-lookup"><span data-stu-id="6783d-939">Renamed 'Get-AzLog' to 'Get-AzActivityLog'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6783d-940">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6783d-940">Az.Network</span></span>
* <span data-ttu-id="6783d-941">영역 기본 동작이 변경된다는 것을 알리기 위해 주요 변경 특성을 추가</span><span class="sxs-lookup"><span data-stu-id="6783d-941">Added breaking change attribute to notify that Zone default behaviour will be changed</span></span>
    - <span data-ttu-id="6783d-942">'New-AzPublicIpAddress'</span><span class="sxs-lookup"><span data-stu-id="6783d-942">'New-AzPublicIpAddress'</span></span>
    - <span data-ttu-id="6783d-943">'New-AzPublicIpPrefix'</span><span class="sxs-lookup"><span data-stu-id="6783d-943">'New-AzPublicIpPrefix'</span></span>
    - <span data-ttu-id="6783d-944">'New-AzLoadBalancerFrontendIpConfig'</span><span class="sxs-lookup"><span data-stu-id="6783d-944">'New-AzLoadBalancerFrontendIpConfig'</span></span>
* <span data-ttu-id="6783d-945">새로운 최상위 리소스 SecurityPartnerProvider에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="6783d-945">Added support for a new top level resource SecurityPartnerProvider</span></span>
    - <span data-ttu-id="6783d-946">추가된 새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-946">New cmdlets added:</span></span>
        - <span data-ttu-id="6783d-947">New-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="6783d-947">New-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="6783d-948">Remove-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="6783d-948">Remove-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="6783d-949">Get-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="6783d-949">Get-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="6783d-950">Set-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="6783d-950">Set-AzSecurityPartnerProvider</span></span>
* <span data-ttu-id="6783d-951">'PSPrivateEndpointConnection'의 'PSPrivateLinkResource' 및 'GroupId'에서 'RequiredZoneNames' 추가</span><span class="sxs-lookup"><span data-stu-id="6783d-951">Added 'RequiredZoneNames' on 'PSPrivateLinkResource' and 'GroupId' on 'PSPrivateEndpointConnection'</span></span>
* <span data-ttu-id="6783d-952">New-AzNetworkWatcherConnectionMonitorTestConfigurationObject에 대한 잘못된 형식의 SuccessThresholdRoundTripTimeMs 매개 변수 수정</span><span class="sxs-lookup"><span data-stu-id="6783d-952">Fixed incorrect type of SuccessThresholdRoundTripTimeMs parameter for New-AzNetworkWatcherConnectionMonitorTestConfigurationObject</span></span>
* <span data-ttu-id="6783d-953">AllowVnetToVnetTraffic 인수의 기본값을 True로 설정하도록 VirtualWan cmdlet 업데이트</span><span class="sxs-lookup"><span data-stu-id="6783d-953">Updated VirtualWan cmdlets to set default value of AllowVnetToVnetTraffic argument to True.</span></span>
    - <span data-ttu-id="6783d-954">'New-AzVirtualWan'</span><span class="sxs-lookup"><span data-stu-id="6783d-954">'New-AzVirtualWan'</span></span>
    - <span data-ttu-id="6783d-955">'Update-AzVirtualWan'</span><span class="sxs-lookup"><span data-stu-id="6783d-955">'Update-AzVirtualWan'</span></span>
* <span data-ttu-id="6783d-956">프라이빗 엔드포인트에 대한 DNS 영역 그룹을 지원하는 새 cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="6783d-956">Added new cmdlets to support DNS zone group for private endpoint</span></span>
    - <span data-ttu-id="6783d-957">'New-AzPrivateDnsZoneConfig'</span><span class="sxs-lookup"><span data-stu-id="6783d-957">'New-AzPrivateDnsZoneConfig'</span></span>
    - <span data-ttu-id="6783d-958">'Get-AzPrivateDnsZoneGroup'</span><span class="sxs-lookup"><span data-stu-id="6783d-958">'Get-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="6783d-959">'New-AzPrivateDnsZoneGroup'</span><span class="sxs-lookup"><span data-stu-id="6783d-959">'New-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="6783d-960">'Set-AzPrivateDnsZoneGroup'</span><span class="sxs-lookup"><span data-stu-id="6783d-960">'Set-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="6783d-961">'Remove-AzPrivateDnsZoneGroup'</span><span class="sxs-lookup"><span data-stu-id="6783d-961">'Remove-AzPrivateDnsZoneGroup'</span></span>
* <span data-ttu-id="6783d-962">'AzureFirewall'에 'DNSEnableProxy', 'DNSRequireProxyForNetworkRules' 및 'DNSServers' 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="6783d-962">Added 'DNSEnableProxy', 'DNSRequireProxyForNetworkRules' and 'DNSServers' parameters to 'AzureFirewall'</span></span>
* <span data-ttu-id="6783d-963">'AzureFirewall'에 'EnableDnsProxy', 'DnsProxyNotRequiredForNetworkRule' 및 'DnsServer' 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="6783d-963">Added 'EnableDnsProxy', 'DnsProxyNotRequiredForNetworkRule' and 'DnsServer' parameters to 'AzureFirewall'</span></span>
    - <span data-ttu-id="6783d-964">업데이트된 cmdlet:</span><span class="sxs-lookup"><span data-stu-id="6783d-964">Updated cmdlet:</span></span>
        - <span data-ttu-id="6783d-965">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="6783d-965">New-AzFirewall</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="6783d-966">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="6783d-966">Az.OperationalInsights</span></span>
* <span data-ttu-id="6783d-967">새로 생성된 SDK를 적용하도록 레거시 코드 업데이트</span><span class="sxs-lookup"><span data-stu-id="6783d-967">Updated legacy code to apply new generated SDK</span></span>
* <span data-ttu-id="6783d-968">사용되지 않는 API 때문에 cmdlet 삭제</span><span class="sxs-lookup"><span data-stu-id="6783d-968">Deleted cmdlets due to deprecated APIs</span></span>
    - <span data-ttu-id="6783d-969">'Get-AzOperationalInsightsSavedSearchResult'(별칭 'Get-AzOperationalInsightsSavedSearchResults')</span><span class="sxs-lookup"><span data-stu-id="6783d-969">'Get-AzOperationalInsightsSavedSearchResult' (alias 'Get-AzOperationalInsightsSavedSearchResults')</span></span>
    - <span data-ttu-id="6783d-970">'Get-AzOperationalInsightsSearchResult'(별칭 'Get-AzOperationalInsightsSearchResults')</span><span class="sxs-lookup"><span data-stu-id="6783d-970">'Get-AzOperationalInsightsSearchResult' (alias 'Get-AzOperationalInsightsSearchResults')</span></span>
    - <span data-ttu-id="6783d-971">'Get-AzOperationalInsightsLinkTarget'(별칭 'Get-AzOperationalInsightsLinkTargets')</span><span class="sxs-lookup"><span data-stu-id="6783d-971">'Get-AzOperationalInsightsLinkTarget' (alias 'Get-AzOperationalInsightsLinkTargets')</span></span>
* <span data-ttu-id="6783d-972">'Set-AzOperationalInsightsWorkspace' 및 'New-AzOperationalInsightsWorkspace'에 대한 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="6783d-972">Added parameters for 'Set-AzOperationalInsightsWorkspace' and 'New-AzOperationalInsightsWorkspace'</span></span>
* <span data-ttu-id="6783d-973">연결된 스토리지 계정에 대한 cmdlet 작성</span><span class="sxs-lookup"><span data-stu-id="6783d-973">Created cmdlets for Linked Stoarge Account</span></span>
* <span data-ttu-id="6783d-974">클러스터 및 연결된 서비스에 대한 cmdlet 작성</span><span class="sxs-lookup"><span data-stu-id="6783d-974">Created cmdlets for Clusters and Linked Service</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="6783d-975">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="6783d-975">Az.RecoveryServices</span></span>
* <span data-ttu-id="6783d-976">Azure Site Recovery - Azure와 Azure 공급자 간 근접 배치 그룹 가상 머신을 보호하기 위한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-976">Azure Site Recovery added support for protecting proximity placement group virtual machines for Azure to Azure provider.</span></span>
* <span data-ttu-id="6783d-977">Azure Site Recovery - 영역 간 복제에 대한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-977">Azure Site Recovery added support for zone to zone replication.</span></span>
* <span data-ttu-id="6783d-978">Azure Backup - Azure 파일 공유 복구 지점의 장기 보존 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-978">Azure Backup Added Long term retention support for Azure FileShare Recovery Points.</span></span>
* <span data-ttu-id="6783d-979">Azure Backup - 'Get-AzRecoveryServicesBackupItem' cmdlet 출력에 디스크 제외 속성이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-979">Azure Backup Added disk exclusion properties to 'Get-AzRecoveryServicesBackupItem' cmdlet output.</span></span>
* <span data-ttu-id="6783d-980">사이트 복구 서비스용 Vault 자격 증명 파일에 대한 프라이빗 엔드포인트가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-980">Added private endpoint for Vault credential file for site recovery service.</span></span>

#### <a name="azresources"></a><span data-ttu-id="6783d-981">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6783d-981">Az.Resources</span></span>
* <span data-ttu-id="6783d-982">새 역할 정의를 만들 때 보기 지연에 대한 메시지 경고 추가</span><span class="sxs-lookup"><span data-stu-id="6783d-982">Added message warning about view delay when creating a new Role Definition</span></span>
* <span data-ttu-id="6783d-983">강력한 형식의 개체를 출력하도록 정책 cmdlet 변경</span><span class="sxs-lookup"><span data-stu-id="6783d-983">Changed policy cmdlets to output strongly-typed objects</span></span>
* <span data-ttu-id="6783d-984">'Get-AzResourceLock' cmdlet에 사용되는 '-TenantLevel' 매개 변수 제거 [#11335]</span><span class="sxs-lookup"><span data-stu-id="6783d-984">Removed '-TenantLevel' parameter used for on the 'Get-AzResourceLock' cmdlet [#11335]</span></span>
* <span data-ttu-id="6783d-985">'Remove-AzResourceGroup -Id ResourceId' 수정[#9882]</span><span class="sxs-lookup"><span data-stu-id="6783d-985">Fixed 'Remove-AzResourceGroup -Id ResourceId'[#9882]</span></span>
* <span data-ttu-id="6783d-986">리소스 그룹 범위에서 ARM 템플릿 가상 시나리오 결과를 가져오는 새 cmdlet 추가: 'Get-AzDeploymentResourceGroupWhatIfResult'</span><span class="sxs-lookup"><span data-stu-id="6783d-986">Added new cmdlet for getting ARM template What-If results at resource group scope: 'Get-AzDeploymentResourceGroupWhatIfResult'</span></span>
* <span data-ttu-id="6783d-987">구독 범위에서 ARM 템플릿 가상 시나리오 결과를 가져오는 새 cmdlet 추가: 'Get-AzDeploymentWhatIfResult'</span><span class="sxs-lookup"><span data-stu-id="6783d-987">Added new cmdlet for getting ARM template What-If results at subscription scope: 'Get-AzDeploymentWhatIfResult'</span></span>
   - <span data-ttu-id="6783d-988">별칭: 'Get-AzSubscriptionDeploymentWhatIf'</span><span class="sxs-lookup"><span data-stu-id="6783d-988">Alias: 'Get-AzSubscriptionDeploymentWhatIf'</span></span>
* <span data-ttu-id="6783d-989">ARM 템플릿 가상 시나리오 결과를 사용하도록 'New-AzDeployment' 및 'New-AzResourceGroupDeployment'에 대한 '-WhatIf' 및 '-Confirm' 매개 변수 재정의</span><span class="sxs-lookup"><span data-stu-id="6783d-989">Overrode '-WhatIf' and '-Confirm' parameters for 'New-AzDeployment' and 'New-AzResourceGroupDeployment' to use ARM template What-If results</span></span>
* <span data-ttu-id="6783d-990">배포 cmdlet에서 'ApiVersion' 매개 변수의 사용 중단 메시지 추가</span><span class="sxs-lookup"><span data-stu-id="6783d-990">Added deprecation message for 'ApiVersion' parameter in deployment cmdlets</span></span>
* <span data-ttu-id="6783d-991">배포 오류에 대한 향상된 오류 메시지를 표시하는 기능 추가</span><span class="sxs-lookup"><span data-stu-id="6783d-991">Added capability to show improved error messages for deployment failures</span></span>
* <span data-ttu-id="6783d-992">배포 오류에 대한 correlationId 로깅 추가</span><span class="sxs-lookup"><span data-stu-id="6783d-992">Added correlationId logging for deployment failures</span></span>
* <span data-ttu-id="6783d-993">배포 스크립트 출력에 'error' 속성 추가</span><span class="sxs-lookup"><span data-stu-id="6783d-993">Added 'error' property to the deployment script output</span></span>
* <span data-ttu-id="6783d-994">nuget Microsoft.Azure.Management.ResourceManager를 '3.7.1-preview'로 업데이트</span><span class="sxs-lookup"><span data-stu-id="6783d-994">Updated nuget Microsoft.Azure.Management.ResourceManager to '3.7.1-preview'</span></span>
* <span data-ttu-id="6783d-995">nuget 3.7.1-preview에서 DeploymentValidateResult의 Error 속성이 readonly로 변경되어 특정 테스트 사례를 제거</span><span class="sxs-lookup"><span data-stu-id="6783d-995">Removed specific test cases as Error property in DeploymentValidateResult has changed to readonly from nuget 3.7.1-preview</span></span>
* <span data-ttu-id="6783d-996">SDK ResourceManager 3.7.1-preview의 GenericResourceExpanded 도입</span><span class="sxs-lookup"><span data-stu-id="6783d-996">Brought GenericResourceExpanded from SDK ResourceManager 3.7.1-preview</span></span>
* <span data-ttu-id="6783d-997">모든 배포용 Get cmdlet에 대한 태그 지원 추가</span><span class="sxs-lookup"><span data-stu-id="6783d-997">Added tag support for all Get cmdlets for deployment, as well as</span></span>
    - <span data-ttu-id="6783d-998">'New-AzDeployment'</span><span class="sxs-lookup"><span data-stu-id="6783d-998">'New-AzDeployment'</span></span>
    - <span data-ttu-id="6783d-999">'New-AzManagementGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="6783d-999">'New-AzManagementGroupDeployment'</span></span>
    - <span data-ttu-id="6783d-1000">'New-AzResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="6783d-1000">'New-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="6783d-1001">'New-AzTenantDeployment'</span><span class="sxs-lookup"><span data-stu-id="6783d-1001">'New-AzTenantDeployment'</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="6783d-1002">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="6783d-1002">Az.ServiceFabric</span></span>
* <span data-ttu-id="6783d-1003">잘못된 인증서 지문을 가져오는 --SecretIdentifier를 사용한 인증서 추가의 버그 수정</span><span class="sxs-lookup"><span data-stu-id="6783d-1003">Fixed bug in add certificate using --SecretIdentifier that was getting the wrong certificate thumbprint</span></span>

#### <a name="azsql"></a><span data-ttu-id="6783d-1004">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6783d-1004">Az.Sql</span></span>
* <span data-ttu-id="6783d-1005">성능 강화:</span><span class="sxs-lookup"><span data-stu-id="6783d-1005">Enhance performance of:</span></span>
    - <span data-ttu-id="6783d-1006">'Set-AzSqlDatabaseSensitivityClassification'</span><span class="sxs-lookup"><span data-stu-id="6783d-1006">'Set-AzSqlDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="6783d-1007">'Set-AzSqlInstanceDatabaseSensitivityClassification'</span><span class="sxs-lookup"><span data-stu-id="6783d-1007">'Set-AzSqlInstanceDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="6783d-1008">'Remove-AzSqlDatabaseSensitivityClassification'</span><span class="sxs-lookup"><span data-stu-id="6783d-1008">'Remove-AzSqlDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="6783d-1009">'Remove-AzSqlInstanceDatabaseSensitivityClassification'</span><span class="sxs-lookup"><span data-stu-id="6783d-1009">'Remove-AzSqlInstanceDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="6783d-1010">'Enable-AzSqlDatabaseSensitivityRecommendation'</span><span class="sxs-lookup"><span data-stu-id="6783d-1010">'Enable-AzSqlDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="6783d-1011">'Enable-AzSqlInstanceDatabaseSensitivityRecommendation'</span><span class="sxs-lookup"><span data-stu-id="6783d-1011">'Enable-AzSqlInstanceDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="6783d-1012">'Disable-AzSqlDatabaseSensitivityRecommendation'</span><span class="sxs-lookup"><span data-stu-id="6783d-1012">'Disable-AzSqlDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="6783d-1013">'Disable-AzSqlInstanceDatabaseSensitivityRecommendation'</span><span class="sxs-lookup"><span data-stu-id="6783d-1013">'Disable-AzSqlInstanceDatabaseSensitivityRecommendation'</span></span>
* <span data-ttu-id="6783d-1014">'Set-AzSqlDatabaseBackupShortTermRetentionPolicy' cmdlet에서 'RetentionDays' 매개 변수의 클라이언트 쪽 유효성 검사 제거</span><span class="sxs-lookup"><span data-stu-id="6783d-1014">Removed client-side validation of 'RetentionDays' parameter from cmdlet 'Set-AzSqlDatabaseBackupShortTermRetentionPolicy'</span></span>
* <span data-ttu-id="6783d-1015">Vnet에서 스토리지 계정을 감사하고, Storage Blob 데이터 기여자 역할을 만들 때 발생하는 버그 수정</span><span class="sxs-lookup"><span data-stu-id="6783d-1015">Auditing to a storage account in Vnet, fixing a bug when creating a Storage Blob Data Contributor role.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="6783d-1016">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="6783d-1016">Az.Storage</span></span>
* <span data-ttu-id="6783d-1017">get/list account cmdlet 'Get-AzStorageAccount'에 '-AsJob' 추가</span><span class="sxs-lookup"><span data-stu-id="6783d-1017">Added '-AsJob' to get/list account cmdlet 'Get-AzStorageAccount'</span></span>
* <span data-ttu-id="6783d-1018">키 자동 회전을 지원하기 위해 스토리지 계정을 KeyvaultEncryption으로 업데이트할 때 KeyVersion을 선택 사항으로 지정</span><span class="sxs-lookup"><span data-stu-id="6783d-1018">Make KeyVersion to optional when update Storage account with KeyvaultEncryption, to support key auto-rotation</span></span>
    - <span data-ttu-id="6783d-1019">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="6783d-1019">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="6783d-1020">파이프라인을 사용하여 Azure 파일 디렉터리 제거 오류 수정</span><span class="sxs-lookup"><span data-stu-id="6783d-1020">Fixed remove Azure File Directory fail with pipeline</span></span>
    - <span data-ttu-id="6783d-1021">'Remove-AzStorageDirectory'</span><span class="sxs-lookup"><span data-stu-id="6783d-1021">'Remove-AzStorageDirectory'</span></span>
* <span data-ttu-id="6783d-1022">수정 [#9880]: Swagger에 맞게 NetWorkRule DefaultAction 값 정의 변경</span><span class="sxs-lookup"><span data-stu-id="6783d-1022">Fixed [#9880]: Change NetWorkRule DefaultAction value defination to align with swagger.</span></span>
    - <span data-ttu-id="6783d-1023">'Update-AzStorageAccountNetworkRuleSet'</span><span class="sxs-lookup"><span data-stu-id="6783d-1023">'Update-AzStorageAccountNetworkRuleSet'</span></span>
    - <span data-ttu-id="6783d-1024">'Get-AzStorageAccountNetworkRuleSet'</span><span class="sxs-lookup"><span data-stu-id="6783d-1024">'Get-AzStorageAccountNetworkRuleSet'</span></span>
* <span data-ttu-id="6783d-1025">수정 [#11624]: 서버 오류를 방지하기 위해 NetworkRules를 추가할 때 중복 규칙 건너뛰기</span><span class="sxs-lookup"><span data-stu-id="6783d-1025">Fixed [#11624]: Skip duplicated rules when add NetworkRules, to avoid server failure</span></span>
    - <span data-ttu-id="6783d-1026">'Add-AzStorageAccountNetworkRule'</span><span class="sxs-lookup"><span data-stu-id="6783d-1026">'Add-AzStorageAccountNetworkRule'</span></span>
* <span data-ttu-id="6783d-1027">Microsoft.Azure.Cosmos.Table SDK를 1.0.7로 업그레이드</span><span class="sxs-lookup"><span data-stu-id="6783d-1027">Upgraded Microsoft.Azure.Cosmos.Table SDK to 1.0.7</span></span>
* <span data-ttu-id="6783d-1028">DataLake Gen2 항목 목록에 부품 항목만 반환되는 경우 ContinuationToken을 사용하여 다시 나열하라고 사용자에게 알리는 경고 메시지 추가</span><span class="sxs-lookup"><span data-stu-id="6783d-1028">Added a warning message to remind user to list again with ContinuationToken when only part items are returned in list DataLake Gen2 Items,</span></span>
    - <span data-ttu-id="6783d-1029">'Get-AzDataLakeGen2ChildItem'</span><span class="sxs-lookup"><span data-stu-id="6783d-1029">'Get-AzDataLakeGen2ChildItem'</span></span>
* <span data-ttu-id="6783d-1030">Azure Files Active Directory 도메인 서비스 인증을 사용하여 스토리지 계정을 만들거나 업데이트하는 기능 지원</span><span class="sxs-lookup"><span data-stu-id="6783d-1030">Supported to create or update Storage account with Azure Files Active Directory Domain Service Authentication</span></span>
    -  <span data-ttu-id="6783d-1031">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="6783d-1031">'New-AzStorageAccount'</span></span>
    -  <span data-ttu-id="6783d-1032">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="6783d-1032">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="6783d-1033">스토리지 계정의 Kerberos 키 새로 만들기 또는 나열 지원</span><span class="sxs-lookup"><span data-stu-id="6783d-1033">Supported to new or list Kerberos keys of Storage account</span></span>
    -  <span data-ttu-id="6783d-1034">'New-AzStorageAccountKey'</span><span class="sxs-lookup"><span data-stu-id="6783d-1034">'New-AzStorageAccountKey'</span></span>
    -  <span data-ttu-id="6783d-1035">'Get-AzStorageAccountKey'</span><span class="sxs-lookup"><span data-stu-id="6783d-1035">'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="6783d-1036">스토리지 계정 장애 조치(failover) 지원</span><span class="sxs-lookup"><span data-stu-id="6783d-1036">Supported failover Storage account</span></span>
    - <span data-ttu-id="6783d-1037">'Invoke-AzStorageAccountFailover'</span><span class="sxs-lookup"><span data-stu-id="6783d-1037">'Invoke-AzStorageAccountFailover'</span></span>
* <span data-ttu-id="6783d-1038">'Get-AzStorageBlobCopyState'의 도움말 업데이트</span><span class="sxs-lookup"><span data-stu-id="6783d-1038">Updated help of 'Get-AzStorageBlobCopyState'</span></span>
* <span data-ttu-id="6783d-1039">'Get-AzStorageFileCopyState' 및 'Start-AzStorageBlobCopy'의 도움말 업데이트</span><span class="sxs-lookup"><span data-stu-id="6783d-1039">Updated help of 'Get-AzStorageFileCopyState' and 'Start-AzStorageBlobCopy'</span></span>
* <span data-ttu-id="6783d-1040">스토리지 클라이언트 라이브러리 v12를 큐 및 파일 cmdlet에 통합</span><span class="sxs-lookup"><span data-stu-id="6783d-1040">Integrated Storage client library v12 to Queue and File cmdlets</span></span>
* <span data-ttu-id="6783d-1041">출력 형식을 CloudFile에서 AzureStorageFile로 변경했으며, 원래 출력은 새 출력의 자식 속성이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1041">Changed output type from CloudFile to AzureStorageFile, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="6783d-1042">'Get-AzStorageFile'</span><span class="sxs-lookup"><span data-stu-id="6783d-1042">'Get-AzStorageFile'</span></span>
    - <span data-ttu-id="6783d-1043">'Remove-AzStorageFile'</span><span class="sxs-lookup"><span data-stu-id="6783d-1043">'Remove-AzStorageFile'</span></span>
    - <span data-ttu-id="6783d-1044">'Get-AzStorageFileContent'</span><span class="sxs-lookup"><span data-stu-id="6783d-1044">'Get-AzStorageFileContent'</span></span>
    - <span data-ttu-id="6783d-1045">'Set-AzStorageFileContent'</span><span class="sxs-lookup"><span data-stu-id="6783d-1045">'Set-AzStorageFileContent'</span></span>
    - <span data-ttu-id="6783d-1046">'Start-AzStorageFileCopy'</span><span class="sxs-lookup"><span data-stu-id="6783d-1046">'Start-AzStorageFileCopy'</span></span>
* <span data-ttu-id="6783d-1047">출력 형식을 CloudFileDirectory에서 AzureStorageFileDirectory로 변경했으며, 원래 출력은 새 출력의 자식 속성이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1047">Changed output type from CloudFileDirectory to AzureStorageFileDirectory, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="6783d-1048">'New-AzStorageDirectory'</span><span class="sxs-lookup"><span data-stu-id="6783d-1048">'New-AzStorageDirectory'</span></span>
    - <span data-ttu-id="6783d-1049">'Remove-AzStorageDirectory'</span><span class="sxs-lookup"><span data-stu-id="6783d-1049">'Remove-AzStorageDirectory'</span></span>
* <span data-ttu-id="6783d-1050">출력 형식을 CloudFileShare에서 AzureStorageFileShare로 변경했으며, 원래 출력은 새 출력의 자식 속성이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1050">Changed output type from CloudFileShare to AzureStorageFileShare, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="6783d-1051">'Get-AzStorageShare'</span><span class="sxs-lookup"><span data-stu-id="6783d-1051">'Get-AzStorageShare'</span></span>
    - <span data-ttu-id="6783d-1052">'New-AzStorageShare'</span><span class="sxs-lookup"><span data-stu-id="6783d-1052">'New-AzStorageShare'</span></span>
    - <span data-ttu-id="6783d-1053">'Remove-AzStorageShare'</span><span class="sxs-lookup"><span data-stu-id="6783d-1053">'Remove-AzStorageShare'</span></span>
* <span data-ttu-id="6783d-1054">출력 형식을 FileShareProperties에서 AzureStorageFileShare로 변경했으며, 원래 출력은 새 출력의 하위 자식 속성이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1054">Changed output type from FileShareProperties to AzureStorageFileShare, the original output will become a sub child property of the new output</span></span>
    - <span data-ttu-id="6783d-1055">'Set-AzStorageShareQuota'</span><span class="sxs-lookup"><span data-stu-id="6783d-1055">'Set-AzStorageShareQuota'</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="6783d-1056">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="6783d-1056">Az.TrafficManager</span></span>
* <span data-ttu-id="6783d-1057">'DisableAzureTrafficManagerEndpoint' 자세한 정보 출력에서 잘못된 프로필 이름 수정</span><span class="sxs-lookup"><span data-stu-id="6783d-1057">Fixed incorrect profile name in 'DisableAzureTrafficManagerEndpoint' verbose output</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="6783d-1058">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="6783d-1058">Az.Websites</span></span>
* <span data-ttu-id="6783d-1059">'Update-AzWebAppAccessRestrictionConfig'의 도움말에서 철자 오류 수정</span><span class="sxs-lookup"><span data-stu-id="6783d-1059">Fixed typo on help of 'Update-AzWebAppAccessRestrictionConfig'.</span></span>

## <a name="380---april-2020"></a><span data-ttu-id="6783d-1060">3.8.0 - 2020년 4월</span><span class="sxs-lookup"><span data-stu-id="6783d-1060">3.8.0 - April 2020</span></span>
### <a name="highlights-since-the-last-release"></a><span data-ttu-id="6783d-1061">마지막 릴리스 이후의 주요 사항</span><span class="sxs-lookup"><span data-stu-id="6783d-1061">Highlights since the last release</span></span>
* <span data-ttu-id="6783d-1062">Az.Storage에서 지원하는 PowerShell 버전: Windows PowerShell 5.1, PowerShell Core 6.2.4 이상, PowerShell 7</span><span class="sxs-lookup"><span data-stu-id="6783d-1062">PowerShell versions that Az.Storage supports: Windows PowerShell 5.1, PowerShell Core 6.2.4+, PowerShell 7</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="6783d-1063">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6783d-1063">Az.Accounts</span></span>
* <span data-ttu-id="6783d-1064">'Resolve-AzError'에서 Azure PowerShell 설문 조사 URL이 업데이트되었습니다. [#11507]</span><span class="sxs-lookup"><span data-stu-id="6783d-1064">Updated Azure PowerShell survey URL in 'Resolve-AzError' [#11507]</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="6783d-1065">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="6783d-1065">Az.ApiManagement</span></span>
* <span data-ttu-id="6783d-1066">향후 릴리스의 Azure File cmdlet 출력 변경에 대한 호환성이 손상되는 변경 공지가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1066">Added breaking change notice for Azure File cmdlets output change in a future release</span></span>
* <span data-ttu-id="6783d-1067">'Set-AzApiManagementGroup' - GroupId 매개 변수를 지정하도록 설명서가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1067">'Set-AzApiManagementGroup' Updated documentation to specify the GroupId parameter</span></span>

#### <a name="azcdn"></a><span data-ttu-id="6783d-1068">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="6783d-1068">Az.Cdn</span></span>
* <span data-ttu-id="6783d-1069">ChinaCDN 관련 가격 책정 SKU 표시가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1069">Fixed ChinaCDN related pricing SKU display</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="6783d-1070">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="6783d-1070">Az.CognitiveServices</span></span>
* <span data-ttu-id="6783d-1071">Identity, Encryption, UserOwnedStorage가 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1071">Supported Identity, Encryption, UserOwnedStorage</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6783d-1072">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6783d-1072">Az.Compute</span></span>
* <span data-ttu-id="6783d-1073">'Set-AzVmssOrchestrationServiceState' cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1073">Added 'Set-AzVmssOrchestrationServiceState' cmdlet.</span></span>
* <span data-ttu-id="6783d-1074">-InstanceView가 있는 'Get-AzVmss'는 OrchestrationService 상태를 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1074">'Get-AzVmss' with -InstanceView shows OrchestrationService states.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="6783d-1075">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="6783d-1075">Az.IotHub</span></span>
* <span data-ttu-id="6783d-1076">IoT 디바이스 쌍 구성을 관리합니다. 새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1076">Manage IoT device twin configuration, New cmdlets are:</span></span>
    - <span data-ttu-id="6783d-1077">'Get-AzIotHubDeviceTwin'</span><span class="sxs-lookup"><span data-stu-id="6783d-1077">'Get-AzIotHubDeviceTwin'</span></span>
    - <span data-ttu-id="6783d-1078">'Update-AzIotHubDeviceTwin'</span><span class="sxs-lookup"><span data-stu-id="6783d-1078">'Update-AzIotHubDeviceTwin'</span></span>
* <span data-ttu-id="6783d-1079">IoT Hub에서 디바이스에 대한 직접 메서드를 호출하는 cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1079">Added cmdlet to invoke direct method on a device in an Iot Hub.</span></span>
* <span data-ttu-id="6783d-1080">IoT 디바이스 모듈 쌍 구성을 관리합니다. 새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1080">Manage IoT device module twin configuration, New cmdlets are:</span></span>
    - <span data-ttu-id="6783d-1081">'Get-AzIotHubModuleTwin'</span><span class="sxs-lookup"><span data-stu-id="6783d-1081">'Get-AzIotHubModuleTwin'</span></span>
    - <span data-ttu-id="6783d-1082">'Update-AzIotHubModuleTwin'</span><span class="sxs-lookup"><span data-stu-id="6783d-1082">'Update-AzIotHubModuleTwin'</span></span>
* <span data-ttu-id="6783d-1083">IoT 자동 디바이스 관리 구성을 대규모로 관리합니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1083">Manage IoT automatic device management configuration at scale.</span></span> <span data-ttu-id="6783d-1084">새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1084">New cmdlets are:</span></span>
    - <span data-ttu-id="6783d-1085">'Add-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="6783d-1085">'Add-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="6783d-1086">'Get-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="6783d-1086">'Get-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="6783d-1087">'Remove-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="6783d-1087">'Remove-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="6783d-1088">'Set-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="6783d-1088">'Set-AzIotHubConfiguration'</span></span>
* <span data-ttu-id="6783d-1089">Iot Hub에서 에지 모듈 메서드를 호출하는 cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1089">Added cmdlet to invoke an edge module method in an Iot Hub.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="6783d-1090">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="6783d-1090">Az.KeyVault</span></span>
* <span data-ttu-id="6783d-1091">자격 증명 모음에서 일시 삭제 및 제거 보호를 사용하도록 설정할 수 있는 새 cmdlet 'Update-AzKeyVault'가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1091">Added a new cmdlet 'Update-AzKeyVault' that can enable soft delete and purge protection on a vault</span></span>
* <span data-ttu-id="6783d-1092">Microsoft.PowerShell.SecretManagement에 대한 지원이 추가되었습니다. [#11178]</span><span class="sxs-lookup"><span data-stu-id="6783d-1092">Added support to Microsoft.PowerShell.SecretManagement [#11178]</span></span>
* <span data-ttu-id="6783d-1093">'Remove-AzKeyVaultManagedStorageSasDefinition' 예제의 오류가 해결되었습니다. [#11479]</span><span class="sxs-lookup"><span data-stu-id="6783d-1093">Fixed error in the examples of 'Remove-AzKeyVaultManagedStorageSasDefinition' [#11479]</span></span>
* <span data-ttu-id="6783d-1094">프라이빗 엔드포인트에 대한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1094">Added support to private endpoint</span></span>

#### <a name="azmaintenance"></a><span data-ttu-id="6783d-1095">Az.Maintenance</span><span class="sxs-lookup"><span data-stu-id="6783d-1095">Az.Maintenance</span></span>
* <span data-ttu-id="6783d-1096">GA용 유지 관리 cmdlet의 릴리스 버전 게시</span><span class="sxs-lookup"><span data-stu-id="6783d-1096">Publishing release version of Maintenance cmdlets for GA</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="6783d-1097">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="6783d-1097">Az.Monitor</span></span>
* <span data-ttu-id="6783d-1098">프라이빗 링크 범위용 cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1098">Added cmdlets for private link scope</span></span>
    - <span data-ttu-id="6783d-1099">'Get-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="6783d-1099">'Get-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="6783d-1100">'Remove-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="6783d-1100">'Remove-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="6783d-1101">'New-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="6783d-1101">'New-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="6783d-1102">'Update-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="6783d-1102">'Update-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="6783d-1103">'Get-AzInsightsPrivateLinkScopedResource'</span><span class="sxs-lookup"><span data-stu-id="6783d-1103">'Get-AzInsightsPrivateLinkScopedResource'</span></span>
    - <span data-ttu-id="6783d-1104">'New-AzInsightsPrivateLinkScopedResource'</span><span class="sxs-lookup"><span data-stu-id="6783d-1104">'New-AzInsightsPrivateLinkScopedResource'</span></span>
    - <span data-ttu-id="6783d-1105">'Remove-AzInsightsPrivateLinkScopedResource'</span><span class="sxs-lookup"><span data-stu-id="6783d-1105">'Remove-AzInsightsPrivateLinkScopedResource'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6783d-1106">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6783d-1106">Az.Network</span></span>
* <span data-ttu-id="6783d-1107">Virtual Network 게이트웨이의 개인 IP에 대한 연결을 사용하도록 설정하는 cmdlet이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1107">Updated cmdlets to enable connection on private IP for Virtual Network Gateway.</span></span>
    - <span data-ttu-id="6783d-1108">'New-AzVirtualNetworkGateway'</span><span class="sxs-lookup"><span data-stu-id="6783d-1108">'New-AzVirtualNetworkGateway'</span></span>
    - <span data-ttu-id="6783d-1109">'Set-AzVirtualNetworkGateway'</span><span class="sxs-lookup"><span data-stu-id="6783d-1109">'Set-AzVirtualNetworkGateway'</span></span>
    - <span data-ttu-id="6783d-1110">'New-AzVirtualNetworkGatewayConnection'</span><span class="sxs-lookup"><span data-stu-id="6783d-1110">'New-AzVirtualNetworkGatewayConnection'</span></span>
    - <span data-ttu-id="6783d-1111">'Set-AzVirtualNetworkGatewayConnection'</span><span class="sxs-lookup"><span data-stu-id="6783d-1111">'Set-AzVirtualNetworkGatewayConnection'</span></span>
* <span data-ttu-id="6783d-1112">FQDN 기반 LocalNetworkGateways 및 VpnSites를 사용하도록 설정하는 cmdlet이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1112">Updated cmdlets to enable FQDN based LocalNetworkGateways and VpnSites</span></span>
    - <span data-ttu-id="6783d-1113">'New-AzLocalNetworkGateway'</span><span class="sxs-lookup"><span data-stu-id="6783d-1113">'New-AzLocalNetworkGateway'</span></span>
    - <span data-ttu-id="6783d-1114">'New-AzVpnSiteLink'</span><span class="sxs-lookup"><span data-stu-id="6783d-1114">'New-AzVpnSiteLink'</span></span>
* <span data-ttu-id="6783d-1115">ExpressRouteCircuitConnectionConfig(Global Reach)의 IPv6 주소 패밀리에 대한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1115">Added support for IPv6 address family in ExpressRouteCircuitConnectionConfig (Global Reach)</span></span>
    - <span data-ttu-id="6783d-1116">'Set-AzExpressRouteCircuitConnectionConfig'가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1116">Added 'Set-AzExpressRouteCircuitConnectionConfig'</span></span>
        - <span data-ttu-id="6783d-1117">IPv6CircuitConnectionProperties를 포함한 모든 기존 속성을 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1117">allows setting of all the existing properties including the IPv6CircuitConnectionProperties</span></span>
    - <span data-ttu-id="6783d-1118">'Add-AzExpressRouteCircuitConnectionConfig'가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1118">Updated 'Add-AzExpressRouteCircuitConnectionConfig'</span></span>
        - <span data-ttu-id="6783d-1119">주소 접두사의 주소 패밀리를 지정하는 또 다른 선택적 매개 변수 AddressPrefixType이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1119">Added another optional parameter AddressPrefixType to specify the address family of address prefix</span></span>
* <span data-ttu-id="6783d-1120">Virtual Network 게이트웨이 연결에서 DPD 시간 제한 설정을 사용하도록 cmdlet이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1120">Updated cmdlets to enable setting of DPD Timeout on Virtual Network Gateway Connections.</span></span>
    - <span data-ttu-id="6783d-1121">New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="6783d-1121">New-AzVirtualNetworkGatewayConnection</span></span>
    - <span data-ttu-id="6783d-1122">Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="6783d-1122">Set-AzVirtualNetworkGatewayConnection</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="6783d-1123">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="6783d-1123">Az.PolicyInsights</span></span>
* <span data-ttu-id="6783d-1124">정책 준수 검사를 트리거하기 위한 'Start-AzPolicyComplianceScan' cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1124">Added 'Start-AzPolicyComplianceScan' cmdlet for triggering policy compliance scans</span></span>
* <span data-ttu-id="6783d-1125">'Get-AzPolicyState' 출력에 정책 정의, 집합 정의 및 할당 버전이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1125">Added policy definition, set definition, and assignment versions to 'Get-AzPolicyState' output</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="6783d-1126">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="6783d-1126">Az.ServiceFabric</span></span>
* <span data-ttu-id="6783d-1127">'New-AzServiceFabricCluster' 예제의 코드 서식 및 사용 편의성이 개선되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1127">Improved code formatting and usability of 'New-AzServiceFabricCluster' examples</span></span>

#### <a name="azsql"></a><span data-ttu-id="6783d-1128">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6783d-1128">Az.Sql</span></span>
* <span data-ttu-id="6783d-1129">'Get-AzSqlInstanceOperation' 및 'Stop-AzSqlInstanceOperation' cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1129">Added cmdlets 'Get-AzSqlInstanceOperation' and 'Stop-AzSqlInstanceOperation'</span></span>
* <span data-ttu-id="6783d-1130">VNet에서 스토리지 계정에 대한 감사가 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1130">Supported auditing to a storage account in VNet.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="6783d-1131">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="6783d-1131">Az.Storage</span></span>
* <span data-ttu-id="6783d-1132">향후 릴리스의 Azure File cmdlet 출력 변경에 대한 호환성이 손상되는 변경 공지가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1132">Added breaking change notice for Azure File cmdlets output change in a future release</span></span>
* <span data-ttu-id="6783d-1133">스토리지 계정 생성/업데이트 시 새로운 SkuName StandardGZRS, StandardRAGZRS가 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1133">Supported new SkuName StandardGZRS, StandardRAGZRS when create/update Storage account</span></span>
    - <span data-ttu-id="6783d-1134">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="6783d-1134">'New-AzStorageAccount'</span></span>
    - <span data-ttu-id="6783d-1135">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="6783d-1135">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="6783d-1136">DataLake Gen2가 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1136">Supported DataLake Gen2</span></span>
    - <span data-ttu-id="6783d-1137">'New-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="6783d-1137">'New-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="6783d-1138">'Get-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="6783d-1138">'Get-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="6783d-1139">'Get-AzDataLakeGen2ChildItem'</span><span class="sxs-lookup"><span data-stu-id="6783d-1139">'Get-AzDataLakeGen2ChildItem'</span></span>
    - <span data-ttu-id="6783d-1140">'Move-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="6783d-1140">'Move-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="6783d-1141">'Set-AzDataLakeGen2ItemAclObject'</span><span class="sxs-lookup"><span data-stu-id="6783d-1141">'Set-AzDataLakeGen2ItemAclObject'</span></span>
    - <span data-ttu-id="6783d-1142">'Update-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="6783d-1142">'Update-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="6783d-1143">'Get-AzDataLakeGen2ItemContent'</span><span class="sxs-lookup"><span data-stu-id="6783d-1143">'Get-AzDataLakeGen2ItemContent'</span></span>
    - <span data-ttu-id="6783d-1144">'Remove-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="6783d-1144">'Remove-AzDataLakeGen2Item'</span></span>

## <a name="0100-preview---april-2020"></a><span data-ttu-id="6783d-1145">0.10.0-preview - 2020년 4월</span><span class="sxs-lookup"><span data-stu-id="6783d-1145">0.10.0-preview - April 2020</span></span>
### <a name="general"></a><span data-ttu-id="6783d-1146">일반</span><span class="sxs-lookup"><span data-stu-id="6783d-1146">General</span></span>
* <span data-ttu-id="6783d-1147">이제 Az 모듈이 Azure Stack Hub에서 미리 보기로 제공됩니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1147">Az modules is now available in preview on Azure Stack Hub.</span></span> <span data-ttu-id="6783d-1148">따라서 Linux 및 macOS와의 플랫폼 간 호환성이 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1148">This allows for cross-platform compatibility with Linux and macOs.</span></span> <span data-ttu-id="6783d-1149">Azure Stack Hub는 이제 Az 모듈을 사용하여 PowerShell Core를 지원합니다. 자세한 내용은 [여기](https://aka.ms/az4AzureStack)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="6783d-1149">Azure Stack Hub now supports PowerShell core with the Az modules, more information [here](https://aka.ms/az4AzureStack)</span></span>
* <span data-ttu-id="6783d-1150">Az 모듈은 2019-03-01-hybrid 프로필을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1150">Az modules support profile 2019-03-01-hybrid:</span></span>
  - <span data-ttu-id="6783d-1151">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="6783d-1151">Az.Billing</span></span>
  - <span data-ttu-id="6783d-1152">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6783d-1152">Az.Compute</span></span>
  - <span data-ttu-id="6783d-1153">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="6783d-1153">Az.DataBoxEdge</span></span>
  - <span data-ttu-id="6783d-1154">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="6783d-1154">Az.EventHub</span></span>
  - <span data-ttu-id="6783d-1155">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="6783d-1155">Az.IotHub</span></span>
  - <span data-ttu-id="6783d-1156">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="6783d-1156">Az.KeyVault</span></span>
  - <span data-ttu-id="6783d-1157">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="6783d-1157">Az.Monitor</span></span>
  - <span data-ttu-id="6783d-1158">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6783d-1158">Az.Network</span></span>
  - <span data-ttu-id="6783d-1159">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6783d-1159">Az.Resources</span></span>
  - <span data-ttu-id="6783d-1160">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="6783d-1160">Az.Storage</span></span>
  - <span data-ttu-id="6783d-1161">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="6783d-1161">Az.Websites</span></span>
* <span data-ttu-id="6783d-1162">Azure Stack Hub와 함께 작동하는 az용 새 PowerShell 모듈 3개(Az.Databox, Az.IotHub 및 Az.EventHub)가 도입되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1162">Three new PowerShell modules for az have been introduced that work with Azure Stack Hub, which are Az.Databox, Az.IotHub, and Az.EventHub</span></span>
* <span data-ttu-id="6783d-1163">AzureRM을 Az로 변경하는 것과 같은 사소한 변경을 수행하면 명령이 비교적 동일하게 유지됩니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1163">Commands remain relatively the same, with minor changes such as changing AzureRM to Az</span></span>
* <span data-ttu-id="6783d-1164">Azure Stack Hub에 대한 PowerShell 설명서의 업데이트된 링크는 [여기](https://aka.ms/InstallASHPowerShell)에서 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1164">Updated link to PowerShell documentation for Azure Stack Hub can be found [here](https://aka.ms/InstallASHPowerShell)</span></span>

## <a name="370---march-2020"></a><span data-ttu-id="6783d-1165">3.7.0 - 2020년 3월</span><span class="sxs-lookup"><span data-stu-id="6783d-1165">3.7.0 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="6783d-1166">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6783d-1166">Az.Accounts</span></span>
* <span data-ttu-id="6783d-1167">로그인하지 않을 때 'Get-AzTenant'/'Get-AzDefault'/'Set-AzDefault'에서 NullReferenceException이 발생하는 문제가 해결되었습니다. [# 10292]</span><span class="sxs-lookup"><span data-stu-id="6783d-1167">Fixed 'Get-AzTenant'/'Get-AzDefault'/'Set-AzDefault' throw NullReferenceException when not login [#10292]</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6783d-1168">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6783d-1168">Az.Compute</span></span>
* <span data-ttu-id="6783d-1169">'New-AzDiskConfig' cmdlet에 다음 매개 변수를 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1169">Added the following parameters to 'New-AzDiskConfig' cmdlet:</span></span>
    - <span data-ttu-id="6783d-1170">DiskIOPSReadOnly, DiskMBpsReadOnly, MaxSharesCount, GalleryImageReference</span><span class="sxs-lookup"><span data-stu-id="6783d-1170">DiskIOPSReadOnly, DiskMBpsReadOnly, MaxSharesCount, GalleryImageReference</span></span>
* <span data-ttu-id="6783d-1171">암호화 속성이 'New-AzGalleryImageVersion'cmdlet의 대상 매개 변수에 허용되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1171">Allowed Encryption property to Target parameter of 'New-AzGalleryImageVersion' cmdlet.</span></span>
* <span data-ttu-id="6783d-1172">'Set-AzVmss'-Reimage 및 'Invoke-AzVMReimage'cmdlet에 대한 tempDisk 이슈가 해결되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1172">Fixed tempDisk issue for 'Set-AzVmss' -Reimage and 'Invoke-AzVMReimage' cmdlets.</span></span> <span data-ttu-id="6783d-1173">[#11354]</span><span class="sxs-lookup"><span data-stu-id="6783d-1173">[#11354]</span></span>
* <span data-ttu-id="6783d-1174">새로운 SAP 확장을 위해 아래 cmdlet에 대한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1174">Added support to below cmdlets for new SAP Extension</span></span>
    - <span data-ttu-id="6783d-1175">'Set-AzVMAEMExtension'</span><span class="sxs-lookup"><span data-stu-id="6783d-1175">'Set-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="6783d-1176">'Get-AzVMAEMExtension'</span><span class="sxs-lookup"><span data-stu-id="6783d-1176">'Get-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="6783d-1177">'Remove-AzVMAEMExtension'</span><span class="sxs-lookup"><span data-stu-id="6783d-1177">'Remove-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="6783d-1178">'Update-AzVMAEMExtension'</span><span class="sxs-lookup"><span data-stu-id="6783d-1178">'Update-AzVMAEMExtension'</span></span>
* <span data-ttu-id="6783d-1179">도움말 문서의 예제에서 오류가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1179">Fixed errors in examples of help document</span></span>
* <span data-ttu-id="6783d-1180">VM PowerState의 정확한 문자열 값을 테이블 형식으로 표시했습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1180">Showed the exact string value for VM PowerState in the table format.</span></span>
* <span data-ttu-id="6783d-1181">'New-AzVmssConfig': SinglePlacementGroup이 비활성화된 경우 AutomaticRepairs 속성의 직렬화가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1181">'New-AzVmssConfig': fixed serialization of AutomaticRepairs property when SinglePlacementGroup is disabled.</span></span> <span data-ttu-id="6783d-1182">[#11257]</span><span class="sxs-lookup"><span data-stu-id="6783d-1182">[#11257]</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="6783d-1183">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="6783d-1183">Az.DataFactory</span></span>
* <span data-ttu-id="6783d-1184">ADF .Net SDK 버전이 4.8.0으로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1184">Updated ADF .Net SDK version to 4.8.0</span></span>
* <span data-ttu-id="6783d-1185">재실행을 지원하기 위해 'Invoke-AzDataFactoryV2Pipeline' 명령에 선택적 매개 변수를 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1185">Added optional parameters to 'Invoke-AzDataFactoryV2Pipeline' command to support rerun</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="6783d-1186">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="6783d-1186">Az.DataLakeStore</span></span>
* <span data-ttu-id="6783d-1187">'Export-AzDataLakeStoreItem' 및 'Import-AzDataLakeStoreItem'에 대해 호환성이 손상되는 변경 설명을 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1187">Added breaking change description for 'Export-AzDataLakeStoreItem' and 'Import-AzDataLakeStoreItem'</span></span>
* <span data-ttu-id="6783d-1188">'New-AzDataLakeStoreItem', 'Add-AzDAtaLakeStoreItemContent' 및 'Get-AzDAtaLakeStoreItemContent'에 대한 바이트 인코딩 옵션이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1188">Added option of Byte encoding for 'New-AzDataLakeStoreItem', 'Add-AzDAtaLakeStoreItemContent', and 'Get-AzDAtaLakeStoreItemContent'</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="6783d-1189">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="6783d-1189">Az.HDInsight</span></span>
* <span data-ttu-id="6783d-1190">클러스터 생성 시 최소 지원 TLS 버전 지정이 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1190">Supported specifying minimal supported TLS version when creating cluster.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="6783d-1191">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="6783d-1191">Az.IotHub</span></span>
* <span data-ttu-id="6783d-1192">디바이스별 분산 설정을 관리하기 위한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1192">Added support to manage distributed settings per-device.</span></span> <span data-ttu-id="6783d-1193">새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1193">New Cmdlets are:</span></span>
    - <span data-ttu-id="6783d-1194">'Get-AzIotHubDistributedTracing'</span><span class="sxs-lookup"><span data-stu-id="6783d-1194">'Get-AzIotHubDistributedTracing'</span></span>
    - <span data-ttu-id="6783d-1195">'Set-AzIotHubDistributedTracing'</span><span class="sxs-lookup"><span data-stu-id="6783d-1195">'Set-AzIotHubDistributedTracing'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="6783d-1196">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="6783d-1196">Az.KeyVault</span></span>
* <span data-ttu-id="6783d-1197">'New-AzKeyVault'에 대해 호환성이 손상되는 변경 속성이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1197">Added breaking change attributes to 'New-AzKeyVault'</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="6783d-1198">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="6783d-1198">Az.Monitor</span></span>
* <span data-ttu-id="6783d-1199">'New-AzScheduledQueryRuleLogMetricTrigger'에 대한 설명서가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1199">Updated documentation for 'New-AzScheduledQueryRuleLogMetricTrigger'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6783d-1200">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6783d-1200">Az.Network</span></span>
* <span data-ttu-id="6783d-1201">교차 테넌트 VirtualHubVnetConnections를 허용하도록 cmdlet이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1201">Updated cmdlets to allow cross-tenant VirtualHubVnetConnections</span></span>
    - <span data-ttu-id="6783d-1202">'New-AzVirtualHubVnetConnection'</span><span class="sxs-lookup"><span data-stu-id="6783d-1202">'New-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="6783d-1203">'Update-AzVirtualHubVnetConnection'</span><span class="sxs-lookup"><span data-stu-id="6783d-1203">'Update-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="6783d-1204">'New-AzVirtualHub'</span><span class="sxs-lookup"><span data-stu-id="6783d-1204">'New-AzVirtualHub'</span></span>
    - <span data-ttu-id="6783d-1205">'Update-AzVirtualHub'</span><span class="sxs-lookup"><span data-stu-id="6783d-1205">'Update-AzVirtualHub'</span></span>
* <span data-ttu-id="6783d-1206">SQL Management SDK 종속성이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1206">Removed Sql Management SDK dependency</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="6783d-1207">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="6783d-1207">Az.PolicyInsights</span></span>
* <span data-ttu-id="6783d-1208">오류 메시지가 향상되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1208">Improved error messages</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="6783d-1209">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="6783d-1209">Az.RecoveryServices</span></span>
* <span data-ttu-id="6783d-1210">Azure Site Recovery는 Azure 디스크 암호화 Virtual Machines에 대한 VM 속성을 다시 보호하고 업데이트하는 기능을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1210">Azure Site Recovery added support for doing reprotect and updated vm properties for Azure disk encrypted Virtual Machines.</span></span>
* <span data-ttu-id="6783d-1211">Azure Site Recovery VmwareToAzure 속성 DR 모니터링이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1211">Added Azure Site Recovery VmwareToAzure properties DR monitoring</span></span>
* <span data-ttu-id="6783d-1212">Azure Backup은 실패한 항목에 대한 정책 업데이트 재시도 지원을 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1212">Azure Backup added support for retrying policy update for failed items.</span></span>
* <span data-ttu-id="6783d-1213">Azure Backup은 백업 및 복원 중에 디스크 제외 설정에 대한 지원을 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1213">Azure Backup Added support for disk exclusion settings during backup and restore.</span></span>
* <span data-ttu-id="6783d-1214">Azure Backup은 AzureFileShare에서 여러 파일/폴더 복원을 위한 지원을 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1214">Azure Backup Added Support for Restoring Multiple files/folders in AzureFileShare</span></span>
* <span data-ttu-id="6783d-1215">Azure Backup은 IaasVM 정책을 업데이트하는 동안 사용자 지정 리소스 그룹 지원에 대한 지원을 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1215">Azure Backup Added support for User-specified Resourcegroup support while updating IaasVM Policy</span></span>

#### <a name="azresources"></a><span data-ttu-id="6783d-1216">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6783d-1216">Az.Resources</span></span>
* <span data-ttu-id="6783d-1217">'Get-AzResource -ResourceGroupName -Name -ExpandProperties -ResourceType'이 기본 apiVersion 대신 실제 apiVersion 리소스를 사용하도록 수정했습니다. [# 11267]</span><span class="sxs-lookup"><span data-stu-id="6783d-1217">Fixed 'Get-AzResource -ResourceGroupName -Name -ExpandProperties -ResourceType' to use actual apiVersion of resources instead of default apiVersion [#11267]</span></span>
* <span data-ttu-id="6783d-1218">오류 시나리오에 대해 correlationId 로깅이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1218">Added correlationId logging for error scenarios</span></span>
* <span data-ttu-id="6783d-1219">작은 설명서가 'Get-AzResourceLock'으로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1219">Small documentation change to 'Get-AzResourceLock'.</span></span> <span data-ttu-id="6783d-1220">예제가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1220">Added example.</span></span>
* <span data-ttu-id="6783d-1221">'Get-AzADUser'의 매개 변수 값에서 작은 따옴표를 이스케이프 처리하였습니다. [# 11317]</span><span class="sxs-lookup"><span data-stu-id="6783d-1221">Escaped single quote in parameter value of 'Get-AzADUser' [#11317]</span></span>
* <span data-ttu-id="6783d-1222">배포 스크립트('Get-AzDeploymentScript', 'Get-AzDeploymentScriptLog', 'Save-AzDeploymentScriptLog', 'Remove-AzDeploymentScript')에 대한 새로운 cmdlet 추가가 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1222">Added new cmdlets for Deployment Scripts ('Get-AzDeploymentScript', 'Get-AzDeploymentScriptLog', 'Save-AzDeploymentScriptLog', 'Remove-AzDeploymentScript')</span></span>

#### <a name="azsql"></a><span data-ttu-id="6783d-1223">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6783d-1223">Az.Sql</span></span>
* <span data-ttu-id="6783d-1224">'Invoke-AzSqlDatabaseFailover'에 읽기 가능한 보조 매개 변수를 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1224">Added readable secondary parameter to 'Invoke-AzSqlDatabaseFailover'</span></span>
* <span data-ttu-id="6783d-1225">'Disable-AzSqlServerActiveDirectoryOnlyAuthentication' cmdlet을 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1225">Added cmdlet 'Disable-AzSqlServerActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="6783d-1226">데이터베이스에서 열을 분류할 때 저장된 민감도 순위입니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1226">Saved sensitivity rank when classifying columns in the database.</span></span>

#### <a name="azsupport"></a><span data-ttu-id="6783d-1227">Az.Support</span><span class="sxs-lookup"><span data-stu-id="6783d-1227">Az.Support</span></span>
* <span data-ttu-id="6783d-1228">'Az.Support' 모듈의 일반 공급</span><span class="sxs-lookup"><span data-stu-id="6783d-1228">General availability of 'Az.Support' module</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="6783d-1229">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="6783d-1229">Az.Websites</span></span>
* <span data-ttu-id="6783d-1230">아래의 새로운 cmdlet을 통해 webapp 트래픽 라우팅 규칙을 사용하는 작업에 대한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1230">Added support for working with webapp Traffic Routing Rules via below new cmdlets</span></span>
    - <span data-ttu-id="6783d-1231">'Get-AzWebAppTrafficRouting'</span><span class="sxs-lookup"><span data-stu-id="6783d-1231">'Get-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="6783d-1232">'Update-AzWebAppTrafficRouting'</span><span class="sxs-lookup"><span data-stu-id="6783d-1232">'Update-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="6783d-1233">'Add-AzWebAppTrafficRouting'</span><span class="sxs-lookup"><span data-stu-id="6783d-1233">'Add-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="6783d-1234">'Remove-AzWebAppTrafficRouting'</span><span class="sxs-lookup"><span data-stu-id="6783d-1234">'Remove-AzWebAppTrafficRouting'</span></span>

## <a name="361---march-2020"></a><span data-ttu-id="6783d-1235">3.6.1 - 2020년 3월</span><span class="sxs-lookup"><span data-stu-id="6783d-1235">3.6.1 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="6783d-1236">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6783d-1236">Az.Accounts</span></span>
* <span data-ttu-id="6783d-1237">'피드백 보내기'에서 Azure PowerShell 설문 조사 페이지가 열립니다[#11020].</span><span class="sxs-lookup"><span data-stu-id="6783d-1237">Open Azure PowerShell survey page in 'Send-Feedback' [#11020]</span></span>
* <span data-ttu-id="6783d-1238">'오류 해결'에서 Azure PowerShell 설문 조사 URL이 표시됩니다[#11021].</span><span class="sxs-lookup"><span data-stu-id="6783d-1238">Display Azure PowerShell survey URL in 'Resolve-Error' [#11021]</span></span>
* <span data-ttu-id="6783d-1239">UserAgent에서 Az 버전이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1239">Added Az version in UserAgent</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="6783d-1240">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="6783d-1240">Az.ApiManagement</span></span>
* <span data-ttu-id="6783d-1241">DeveloperPortal 엔드포인트에서 사용자 지정 도메인을 검색하고 구성하기 위한 지원이 추가되었습니다[#11007].</span><span class="sxs-lookup"><span data-stu-id="6783d-1241">Added support for retrieving and configuring Custom Domain on the DeveloperPortal Endpoint [#11007]</span></span>
* <span data-ttu-id="6783d-1242">Json 형식의 API 정의를 다운로드하기 위한 'Export-AzApiManagementApi' 지원이 추가되었습니다[#9987].</span><span class="sxs-lookup"><span data-stu-id="6783d-1242">'Export-AzApiManagementApi' Added support for downloading Api Definition in Json format [#9987]</span></span>
* <span data-ttu-id="6783d-1243">Json 문서에서 OpenApi 3.0 정의를 가져오기 위한 'Import-AzApiManagementApi' 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1243">'Import-AzApiManagementApi' Added support for importing OpenApi 3.0 definition from Json document</span></span>
* <span data-ttu-id="6783d-1244">AAD B2C 공급자에 대한 '로그인 테넌트'를 구성하기 위한 'New-AzApiManagementIdentityProvider' 및 'Set-AzApiManagementIdentityProvider' 지원이 추가되었습니다[#9784].</span><span class="sxs-lookup"><span data-stu-id="6783d-1244">'New-AzApiManagementIdentityProvider' and 'Set-AzApiManagementIdentityProvider' Added support for configuring 'Signin Tenant' for AAD B2C Provider [#9784]</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="6783d-1245">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="6783d-1245">Az.DataLakeStore</span></span>
* <span data-ttu-id="6783d-1246">csproj 및 psd1에서 System.Buffers에 대한 참조가 명시적으로 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1246">Added reference to System.Buffers explicitly in csproj and psd1.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="6783d-1247">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="6783d-1247">Az.IotHub</span></span>
* <span data-ttu-id="6783d-1248">Iot Hub에서 디바이스를 관리하기 위한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1248">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="6783d-1249">새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1249">New Cmdlets are:</span></span>
    - <span data-ttu-id="6783d-1250">'Add-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="6783d-1250">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="6783d-1251">'Get-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="6783d-1251">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="6783d-1252">'Remove-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="6783d-1252">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="6783d-1253">'Set-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="6783d-1253">'Set-AzIotHubDevice'</span></span>
* <span data-ttu-id="6783d-1254">Iot Hub의 대상 IoT 디바이스에서 모듈을 관리하기 위한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1254">Added support to manage modules on a target Iot device in an Iot Hub.</span></span> <span data-ttu-id="6783d-1255">새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1255">New Cmdlets are:</span></span>
    - <span data-ttu-id="6783d-1256">'Add-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="6783d-1256">'Add-AzIotHubModule'</span></span>
    - <span data-ttu-id="6783d-1257">'Get-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="6783d-1257">'Get-AzIotHubModule'</span></span>
    - <span data-ttu-id="6783d-1258">'Remove-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="6783d-1258">'Remove-AzIotHubModule'</span></span>
    - <span data-ttu-id="6783d-1259">'Set-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="6783d-1259">'Set-AzIotHubModule'</span></span>
* <span data-ttu-id="6783d-1260">Iot Hub에서 대상 IoT 디바이스에 대한 연결 문자열을 가져오는 cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1260">Added cmdlet to get the connection string of a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="6783d-1261">Iot Hub에서 대상 IoT 디바이스의 모듈에 대한 연결 문자열을 가져오는 cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1261">Added cmdlet to get the connection string of a module on a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="6783d-1262">IoT 디바이스의 부모 디바이스를 가져오거나 설정하기 위한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1262">Added support to get/set parent device of an IoT device.</span></span> <span data-ttu-id="6783d-1263">새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1263">New Cmdlets are:</span></span>
    - <span data-ttu-id="6783d-1264">'Get-AzIotHubDeviceParent'</span><span class="sxs-lookup"><span data-stu-id="6783d-1264">'Get-AzIotHubDeviceParent'</span></span>
    - <span data-ttu-id="6783d-1265">'Set-AzIotHubDeviceParent'</span><span class="sxs-lookup"><span data-stu-id="6783d-1265">'Set-AzIotHubDeviceParent'</span></span>
* <span data-ttu-id="6783d-1266">디바이스 부모-자식 관계를 관리하기 위한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1266">Added support to manage device parent-child relationship.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="6783d-1267">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="6783d-1267">Az.Monitor</span></span>
* <span data-ttu-id="6783d-1268">'Get-AzMetricDefinition'에 대한 출력 값이 수정되었습니다[#9714].</span><span class="sxs-lookup"><span data-stu-id="6783d-1268">Fixed output value for 'Get-AzMetricDefinition' [#9714]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6783d-1269">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6783d-1269">Az.Network</span></span>
* <span data-ttu-id="6783d-1270">SQL Management SDK가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1270">Updated Sql Management SDK.</span></span>
* <span data-ttu-id="6783d-1271">PrivateLinkServiceConnectionState 클래스의 명명 차이 문제가 해결되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1271">Fixed a naming-difference issue in PrivateLinkServiceConnectionState class.</span></span>
    - <span data-ttu-id="6783d-1272">ActionsRequired 필드가 ActionRequired에 매핑됩니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1272">Mapping the field ActionsRequired to ActionRequired.</span></span>
* <span data-ttu-id="6783d-1273">PublicNetworkAccess가 'New-AzSqlServer' 및 'Set-AzSqlServer'에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1273">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>

#### <a name="azresources"></a><span data-ttu-id="6783d-1274">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6783d-1274">Az.Resources</span></span>
* <span data-ttu-id="6783d-1275">Get-AzRoleAssignment'의 null 참조 버그가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1275">Fixed for null reference bug in 'Get-AzRoleAssignment'</span></span>
* <span data-ttu-id="6783d-1276">'Remove-AzADGroup'에서 '-Force' 및 '-PassThru' 스위치가 선택적으로 표시됩니다[#10849].</span><span class="sxs-lookup"><span data-stu-id="6783d-1276">Marked switch '-Force' and '-PassThru' optional in 'Remove-AzADGroup' [#10849]</span></span>
* <span data-ttu-id="6783d-1277">'Remove-AzADGroup'에서 'MailNickname'이 반환되지 않는 문제가 해결되었습니다[#11167].</span><span class="sxs-lookup"><span data-stu-id="6783d-1277">Fixed issue that 'MailNickname' doesn't return in 'Remove-AzADGroup' [#11167]</span></span>
* <span data-ttu-id="6783d-1278">'Remove-AzADGroup' 파이프 작업이 작동하지 않는 문제가 해결되었습니다[#11171].</span><span class="sxs-lookup"><span data-stu-id="6783d-1278">Fixed issue that 'Remove-AzADGroup' pipe operation doesn't work [#11171]</span></span>
* <span data-ttu-id="6783d-1279">GetAzureRoleAssignmentCommand의 null 참조 버그가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1279">Fixed for null reference bug in GetAzureRoleAssignmentCommand</span></span>
* <span data-ttu-id="6783d-1280">예정된 정책 cmdlet 변경에 대한 호환성이 손상되는 변경 특성이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1280">Added breaking change attributes for upcoming changes to policy cmdlets</span></span>
* <span data-ttu-id="6783d-1281">서버 쪽에서 리소스 그룹 태그 필터링을 수행하도록 'Get-AzResourceGroup'이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1281">Updated 'Get-AzResourceGroup' to perform resource group tag filtering on server-side</span></span>
* <span data-ttu-id="6783d-1282">-ResourceId를 허용하도록 Tag cmdlet이 확장되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1282">Extended Tag cmdlets to accept -ResourceId</span></span>
    - <span data-ttu-id="6783d-1283">Get-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="6783d-1283">Get-AzTag -ResourceId</span></span>
    - <span data-ttu-id="6783d-1284">New-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="6783d-1284">New-AzTag -ResourceId</span></span>
    - <span data-ttu-id="6783d-1285">Remove-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="6783d-1285">Remove-AzTag -ResourceId</span></span>
* <span data-ttu-id="6783d-1286">새 Tag cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1286">Added new Tag cmdlet</span></span>
    - <span data-ttu-id="6783d-1287">Update-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="6783d-1287">Update-AzTag -ResourceId</span></span>
* <span data-ttu-id="6783d-1288">SDK 3.3.0에서 ScopedDeployment를 가져왔습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1288">Brought ScopedDeployment from SDK 3.3.0</span></span>

#### <a name="azsql"></a><span data-ttu-id="6783d-1289">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6783d-1289">Az.Sql</span></span>
* <span data-ttu-id="6783d-1290">PublicNetworkAccess가 'New-AzSqlServer' 및 'Set-AzSqlServer'에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1290">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>
* <span data-ttu-id="6783d-1291">관리형 데이터베이스에 대한 장기 보존 백업 구성에 대한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1291">Added support for Long Term Retention backup configuration for Managed Databases</span></span>
    - <span data-ttu-id="6783d-1292">관리형 데이터베이스에서 LTR 정책을 가져오거나 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1292">Get/Set LTR policy on a managed database</span></span>
    - <span data-ttu-id="6783d-1293">관리형 데이터베이스, 관리형 인스턴스 또는 위치를 기준으로 LTR 백업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1293">Get LTR backup(s) by managed database, managed instance, or by location</span></span>
    - <span data-ttu-id="6783d-1294">LTR 백업을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1294">Remove an LTR backup</span></span>
    - <span data-ttu-id="6783d-1295">LTR 백업을 복원하여 새 관리형 데이터베이스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1295">Restore an LTR backup to create a new managed database</span></span>
* <span data-ttu-id="6783d-1296">MinimalTlsVersion이 New-AzSqlServer 및 Set-AzSqlServer에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1296">Added MinimalTlsVersion to New-AzSqlServer and Set-AzSqlServer</span></span>
* <span data-ttu-id="6783d-1297">MinimalTlsVersion을 New-AzSqlInstance 및 Set-AzSqlInstance에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1297">Added MinimalTlsVersion to New-AzSqlInstance and Set-AzSqlInstance</span></span>
* <span data-ttu-id="6783d-1298">Az.Network에 대한 SQL SDK 버전이 높아졌습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1298">Bumped SQL SDK version for Az.Network</span></span>

#### <a name="azstorage"></a><span data-ttu-id="6783d-1299">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="6783d-1299">Az.Storage</span></span>
* <span data-ttu-id="6783d-1300">ImmutabilityPolicy에서 AllowProtectedAppendWrite가 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1300">Supported AllowProtectedAppendWrite in ImmutabilityPolicy</span></span>
    - <span data-ttu-id="6783d-1301">'Set-AzRmStorageContainerImmutabilityPolicy'</span><span class="sxs-lookup"><span data-stu-id="6783d-1301">'Set-AzRmStorageContainerImmutabilityPolicy'</span></span>
* <span data-ttu-id="6783d-1302">이후 릴리스에서 AzureStorageTable 형식 변경에 대한 호환성이 손상되는 변경 경고 메시지가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1302">Added breaking change warning message for AzureStorageTable type change in a future release</span></span>
    - <span data-ttu-id="6783d-1303">'New-AzStorageTable'</span><span class="sxs-lookup"><span data-stu-id="6783d-1303">'New-AzStorageTable'</span></span>
    - <span data-ttu-id="6783d-1304">'Get-AzStorageTable'</span><span class="sxs-lookup"><span data-stu-id="6783d-1304">'Get-AzStorageTable'</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="6783d-1305">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="6783d-1305">Az.Websites</span></span>
* <span data-ttu-id="6783d-1306">'New-AzAppServicePlan' 및 'Set-AzAppServicePlan'에 대한 Tag 매개 변수가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1306">Added Tag parameter for 'New-AzAppServicePlan' and 'Set-AzAppServicePlan'</span></span>
* <span data-ttu-id="6783d-1307">웹 사이트에 사용자 지정 도메인을 추가할 때 예외가 throw되면 cmdlet 실행을 중지합니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1307">Stop cmdlet execution if an exception is thrown when adding a custom domain to a website</span></span>
* <span data-ttu-id="6783d-1308">App Service 계획과 동일한 리소스 그룹에 속하지 않는 App Services에 대한 작업을 수행하기 위한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1308">Added support to perform operations for App Services not in the same resource group as the App Service Plan</span></span>
* <span data-ttu-id="6783d-1309">다른 리소스 그룹의 WebApp/Function에 대한 액세스 제한이 적용되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1309">Applied access restriction to WebApp/Function in different resource groups</span></span>
* <span data-ttu-id="6783d-1310">WebAppSlot에 대한 사용자 지정 호스트 이름을 설정하는 문제가 해결되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1310">Fixed issue to set custom hostnames for WebAppSlots</span></span>

## <a name="350---february-2020"></a><span data-ttu-id="6783d-1311">3.5.0 - 2020년 2월</span><span class="sxs-lookup"><span data-stu-id="6783d-1311">3.5.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="6783d-1312">마지막 주 릴리스 이후의 주요 사항</span><span class="sxs-lookup"><span data-stu-id="6783d-1312">Highlights since the last major release</span></span>
* <span data-ttu-id="6783d-1313">클라이언트 쪽 원격 분석이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1313">Updated client side telemetry.</span></span>
* <span data-ttu-id="6783d-1314">디바이스 관리를 지원하는 cmdlet이 Az.IotHub에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1314">Az.IotHub added cmdlets to support to manage devices.</span></span>
* <span data-ttu-id="6783d-1315">가용성 그룹 수신기에 대한 cmdlet이 Az.SqlVirtualMachine에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1315">Az.SqlVirtualMachine added cmdlets for Availability Group Listener.</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="6783d-1316">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6783d-1316">Az.Accounts</span></span>
* <span data-ttu-id="6783d-1317">SubscriptionId, TenantId 및 실행 시간이 클라이언트 쪽 원격 분석에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1317">Added SubscriptionId, TenantId, and execution time into data of client side telemetry</span></span>

#### <a name="azautomation"></a><span data-ttu-id="6783d-1318">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="6783d-1318">Az.Automation</span></span>
* <span data-ttu-id="6783d-1319">'New-AzAutomationSoftwareUpdateConfiguration' 참조 설명서의 예제 1에 있는 오타가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1319">Fixed typo in Example 1 in reference documentation for 'New-AzAutomationSoftwareUpdateConfiguration'</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="6783d-1320">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="6783d-1320">Az.CognitiveServices</span></span>
* <span data-ttu-id="6783d-1321">SDK가 7.0으로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1321">Updated SDK to 7.0</span></span>
* <span data-ttu-id="6783d-1322">서버 응답 본문이 비어 있는 경우 표시되는 오류 메시지가 향상되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1322">Improved error message when server responses empty body</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6783d-1323">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6783d-1323">Az.Compute</span></span>
* <span data-ttu-id="6783d-1324">업데이트하는 동안 빈 값이 ProximityPlacementGroupId에 허용되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1324">Allowed empty value for ProximityPlacementGroupId during update</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="6783d-1325">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="6783d-1325">Az.FrontDoor</span></span>
* <span data-ttu-id="6783d-1326">WAF에서 사용할 수 있는 관리형 규칙 정의를 가져오는 cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1326">Added cmdlet to get managed rule definitions that can be used in WAF</span></span>

#### <a name="aziothub"></a><span data-ttu-id="6783d-1327">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="6783d-1327">Az.IotHub</span></span>
* <span data-ttu-id="6783d-1328">Iot Hub에서 디바이스를 관리하기 위한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1328">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="6783d-1329">새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1329">New Cmdlets are:</span></span>
    - <span data-ttu-id="6783d-1330">'Add-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="6783d-1330">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="6783d-1331">'Get-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="6783d-1331">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="6783d-1332">'Remove-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="6783d-1332">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="6783d-1333">'Set-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="6783d-1333">'Set-AzIotHubDevice'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="6783d-1334">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="6783d-1334">Az.KeyVault</span></span>
* <span data-ttu-id="6783d-1335">Add-AzKeyVaultKey.md에 대해 중복된 텍스트가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1335">Fixed duplicated text for Add-AzKeyVaultKey.md</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="6783d-1336">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="6783d-1336">Az.Monitor</span></span>
* <span data-ttu-id="6783d-1337">Get-AzLog cmdlet에 대한 설명이 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1337">Fixed description of the Get-AzLog cmdlet.</span></span>
* <span data-ttu-id="6783d-1338">ActionGroupId라는 새 매개 변수가 'New-AzMetricAlertRuleV2' 명령에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1338">A new parameter called ActionGroupId was added to 'New-AzMetricAlertRuleV2' command.</span></span>
    - <span data-ttu-id="6783d-1339">사용자는 ActionGroupId(string) 또는 ActionGorup(ActivityLogAlertActionGroup) 중 하나를 제공할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1339">The user can provide either ActionGroupId(string) or ActionGorup(ActivityLogAlertActionGroup).</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6783d-1340">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6783d-1340">Az.Network</span></span>
* <span data-ttu-id="6783d-1341">'New-AzPrivateLinkService' cmdlet의 '-EnableProxyProtocol' 매개 변수에 대한 하나의 추가 매개 변수 메모가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1341">Added one extra parameter note for parameter '-EnableProxyProtocol' for 'New-AzPrivateLinkService' cmdlet.</span></span>
* <span data-ttu-id="6783d-1342">Start-AzVirtualNetworkGatewayConnectionPacketCapture.md 및 Start-AzVirtualnetworkGatewayPacketCapture.md의 FilterData 예제가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1342">Fixed FilterData example in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="6783d-1343">Start-AzVirtualNetworkGatewayConnectionPacketCapture.md 및 Start-AzVirtualnetworkGatewayPacketCapture.md의 모든 내부 및 외부 패킷을 캡처하는 패킷 캡처 예제가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1343">Added Packet Capture example for capture all inner and outer packets in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="6783d-1344">VNet 방화벽에서 Azure Firewall 정책이 지원됩니다</span><span class="sxs-lookup"><span data-stu-id="6783d-1344">Supported Azure Firewall Policy on VNet Firewalls</span></span>
    - <span data-ttu-id="6783d-1345">새로 추가된 cmdlet이 없습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1345">No new cmdlets are added.</span></span> <span data-ttu-id="6783d-1346">VNet 방화벽에서 방화벽 정책 제한이 완화되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1346">Relaxing the restriction for firewall policy on VNet firewalls</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="6783d-1347">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="6783d-1347">Az.RecoveryServices</span></span>
* <span data-ttu-id="6783d-1348">SQL Database에 대한 파일로 복원 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1348">Added Support for Restore-as-files for SQL Databases.</span></span>

#### <a name="azresources"></a><span data-ttu-id="6783d-1349">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6783d-1349">Az.Resources</span></span>
* <span data-ttu-id="6783d-1350">템플릿 배포 cmdlet이 리팩터링되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1350">Refactored template deployment cmdlets</span></span>
    - <span data-ttu-id="6783d-1351">관리 그룹에서 배포를 관리하는 새 \*-AzManagementGroupDeployment cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1351">Added new cmdlets for managing deployments at management group: \*-AzManagementGroupDeployment</span></span>
    - <span data-ttu-id="6783d-1352">테넌트 범위에서 배포를 관리하는 새 \*-AzTenantDeployment cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1352">Added new cmdlets for managing deployments at tenant scope: \*-AzTenantDeployment</span></span>
    - <span data-ttu-id="6783d-1353">구독 범위에서 구체적으로 작동하도록 \*-AzDeployment cmdlet이 리팩터링되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1353">Refactored \*-AzDeployment cmdlets to work specifically at subscription scope</span></span>
    - <span data-ttu-id="6783d-1354">\*-AzDeployment cmdlet에 대한 \*-AzSubscriptionDeployment 별칭이 만들어졌습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1354">Created aliases \*-AzSubscriptionDeployment for \*-AzDeployment cmdlets</span></span>
* <span data-ttu-id="6783d-1355">'AvailableToOtherTenants' 매개 변수가 설정되지 않는 'Update-AzADApplication'이 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1355">Fixed 'Update-AzADApplication' when parameter 'AvailableToOtherTenants' is not set</span></span>
* <span data-ttu-id="6783d-1356">AmbiguousParameterSetException을 방지하기 위해 ApplicationObjectWithoutCredentialParameterSet이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1356">Removed ApplicationObjectWithoutCredentialParameterSet to avoid AmbiguousParameterSetException.</span></span>
* <span data-ttu-id="6783d-1357">도움말 파일이 다시 생성되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1357">Regenerated help files</span></span>

#### <a name="azsql"></a><span data-ttu-id="6783d-1358">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6783d-1358">Az.Sql</span></span>
* <span data-ttu-id="6783d-1359">Managed Instance에서 구독 간 특정 시점 복원에 대한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1359">Added support for cross subscription point in time restore on Managed Instances.</span></span>
* <span data-ttu-id="6783d-1360">기존 SQL Managed Instance 하드웨어 생성 변경에 대한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1360">Added support for changing existing Sql Managed Instance hardware generation</span></span>
* <span data-ttu-id="6783d-1361">'Update-AzSqlServerVulnerabilityAssessmentSetting' 도움말 예제(매개 변수/속성 출력 -EmailAdmins)가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1361">Fixed 'Update-AzSqlServerVulnerabilityAssessmentSetting' help examples: parameter/property output - EmailAdmins</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="6783d-1362">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="6783d-1362">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="6783d-1363">가용성 그룹 수신기에 대한 cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1363">Added cmdlets for Availability Group Listener</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="6783d-1364">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="6783d-1364">Az.StorageSync</span></span>
* <span data-ttu-id="6783d-1365">'Invoke-AzStorageSyncCompatibilityCheck'에서 지원되는 문자 세트가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1365">Updated supported character sets in 'Invoke-AzStorageSyncCompatibilityCheck'.</span></span>

## <a name="340---february-2020"></a><span data-ttu-id="6783d-1366">3.4.0 - 2020년 2월</span><span class="sxs-lookup"><span data-stu-id="6783d-1366">3.4.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="6783d-1367">마지막 주 릴리스 이후의 주요 사항</span><span class="sxs-lookup"><span data-stu-id="6783d-1367">Highlights since the last major release</span></span>
* <span data-ttu-id="6783d-1368">Az. CosmosDB 초기 버전 0.1.0 출시</span><span class="sxs-lookup"><span data-stu-id="6783d-1368">Az.CosmosDB initial version 0.1.0 released</span></span>
* <span data-ttu-id="6783d-1369">Az.Network ConnectionMonitor V2 지원 추가</span><span class="sxs-lookup"><span data-stu-id="6783d-1369">Az.Network ConnectionMonitor V2 support added</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="6783d-1370">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6783d-1370">Az.Accounts</span></span>
* <span data-ttu-id="6783d-1371">AzureRmContext.json을 사용할 수 없을 때 컨텍스트 자동 저장 사용 안 함</span><span class="sxs-lookup"><span data-stu-id="6783d-1371">Disable context auto saving when AzureRmContext.json not available</span></span>
* <span data-ttu-id="6783d-1372">Azure Powershell Common 참조를 1.3.5-preview로 업데이트</span><span class="sxs-lookup"><span data-stu-id="6783d-1372">Update the reference to Azure Powershell Common to 1.3.5-preview</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="6783d-1373">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="6783d-1373">Az.ApiManagement</span></span>
* <span data-ttu-id="6783d-1374">**Get-AzApiManagementApiSchema** API와 연결된 Open-Api 스키마 가져오기 수정   https://github.com/Azure/azure-powershell/issues/10626</span><span class="sxs-lookup"><span data-stu-id="6783d-1374">**Get-AzApiManagementApiSchema** Fixed getting Open-Api Schema associated with an API   https://github.com/Azure/azure-powershell/issues/10626</span></span>
* <span data-ttu-id="6783d-1375">**New-AzApiManagementProduct** _ 및 _ *Set-AzApiManagementProduct*\*</span><span class="sxs-lookup"><span data-stu-id="6783d-1375">**New-AzApiManagementProduct** _ and _ *Set-AzApiManagementProduct*\*</span></span>
  - <span data-ttu-id="6783d-1376"> https://github.com/Azure/azure-powershell/issues/10472 설명서 수정</span><span class="sxs-lookup"><span data-stu-id="6783d-1376">Fix documentation for https://github.com/Azure/azure-powershell/issues/10472</span></span>
* <span data-ttu-id="6783d-1377">**Set-AzApiManagementApi** cmdlet을 사용하여 ServiceUrl을 업데이트하는 방법을 보여주는 예제 추가</span><span class="sxs-lookup"><span data-stu-id="6783d-1377">**Set-AzApiManagementApi** Added example to show how to update the ServiceUrl using the cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6783d-1378">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6783d-1378">Az.Compute</span></span>
* <span data-ttu-id="6783d-1379">VM 이름을 사용하지 않고 Get-AzVM -Status를 수행할 때 제한을 피하기 위해 VM 상태 수를 100개로 제한</span><span class="sxs-lookup"><span data-stu-id="6783d-1379">Limit the number of VM status to 100 to avoid throttling when Get-AzVM -Status is performed without VM name.</span></span>
* <span data-ttu-id="6783d-1380">Update-AzDiskEncryptionSet cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="6783d-1380">Add Update-AzDiskEncryptionSet cmdlet</span></span>
* <span data-ttu-id="6783d-1381">다음 cmdlet에 EncryptionType 및 DiskEncryptionSetId 매개 변수 추가:</span><span class="sxs-lookup"><span data-stu-id="6783d-1381">Add EncryptionType and DiskEncryptionSetId parameters to the following cmdlets:</span></span>
    - <span data-ttu-id="6783d-1382">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="6783d-1382">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span></span>
* <span data-ttu-id="6783d-1383">Get-AzProximityPlacementGroup cmdlet에 ColocationStatus 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="6783d-1383">Add ColocationStatus parameter to Get-AzProximityPlacementGroup cmdlet.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="6783d-1384">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="6783d-1384">Az.DataFactory</span></span>
* <span data-ttu-id="6783d-1385">ADF .Net SDK 버전을 4.7.0으로 업데이트</span><span class="sxs-lookup"><span data-stu-id="6783d-1385">Update ADF .Net SDK version to 4.7.0</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="6783d-1386">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="6783d-1386">Az.DeploymentManager</span></span>
* <span data-ttu-id="6783d-1387">리소스에 대한 LIST 작업 추가</span><span class="sxs-lookup"><span data-stu-id="6783d-1387">Adds LIST operations for resources</span></span>
* <span data-ttu-id="6783d-1388">상태 검사 단계에 대한 작업을 수행하는 기능 추가</span><span class="sxs-lookup"><span data-stu-id="6783d-1388">Adds capability for performing operations on Health Check steps</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="6783d-1389">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="6783d-1389">Az.HDInsight</span></span>
* <span data-ttu-id="6783d-1390">AzHDInsightCluster의 문서 오류 수정</span><span class="sxs-lookup"><span data-stu-id="6783d-1390">Fix document error of New-AzHDInsightCluster.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="6783d-1391">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="6783d-1391">Az.KeyVault</span></span>
* <span data-ttu-id="6783d-1392">Remove-AzureKeyVault가 새 New-AzureKeyVault와 일관성을 유지하도록 VaultName 특성에 이름 별칭 추가</span><span class="sxs-lookup"><span data-stu-id="6783d-1392">Add Name alias to VaultName attribute to make Remove-AzureKeyVault consistent with New-AzureKeyVault.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6783d-1393">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6783d-1393">Az.Network</span></span>
* <span data-ttu-id="6783d-1394">Set-AzNetworkWatcherConfigFlowLog.md에 트래픽 분석 사용 안 함 시나리오를 보여주는 새 예제 추가</span><span class="sxs-lookup"><span data-stu-id="6783d-1394">New example added to Set-AzNetworkWatcherConfigFlowLog.md to demonstrate Traffic Analytics disable scenario.</span></span>
* <span data-ttu-id="6783d-1395">Azure Firewall에 관리 IP 구성을 할당하는 지원 추가 - 방화벽에서 관리 트래픽에 사용할 전용 서브넷 및 공용 IP</span><span class="sxs-lookup"><span data-stu-id="6783d-1395">Add support for assigning management IP configuration to Azure Firewall - a dedicated subnet and Public IP that the firewall will use for its management traffic</span></span>
    - <span data-ttu-id="6783d-1396">New-AzFirewall cmdlet이 업데이트됨:</span><span class="sxs-lookup"><span data-stu-id="6783d-1396">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="6783d-1397">공용 IP 주소 개체를 허용하는 -ManagementPublicIpAddress 매개 변수(필수 아님) 추가</span><span class="sxs-lookup"><span data-stu-id="6783d-1397">Added parameter -ManagementPublicIpAddress (not mandatory) which accepts a Public IP Address object</span></span>
        - <span data-ttu-id="6783d-1398">방화벽 개체에 SetManagementIpConfiguration 메서드 추가 - 입력으로 서브넷 및 공용 IP 주소 필요 - 서브넷 이름은 'AzureFirewallManagementSubnet'이어야 함</span><span class="sxs-lookup"><span data-stu-id="6783d-1398">Added method SetManagementIpConfiguration on firewall object - requires a subnet and a Public IP address as input - subnet name must be 'AzureFirewallManagementSubnet'</span></span>
* <span data-ttu-id="6783d-1399">네트워크 인터페이스 대신 NSG 예제를 보여주도록 AzNetworkSecurityGroup 예제 수정</span><span class="sxs-lookup"><span data-stu-id="6783d-1399">Corrected Get-AzNetworkSecurityGroup examples to show examples for NSG's instead of network interfaces.</span></span>
* <span data-ttu-id="6783d-1400">리소스 id 완성자가 매개 변수를 완성하지 못하게 방해하던 New-AzVpnSite 명령의 오타 수정</span><span class="sxs-lookup"><span data-stu-id="6783d-1400">Fixed typo in New-AzVpnSite command that was preventing resource id completer from completing a parameter.</span></span>
* <span data-ttu-id="6783d-1401">Application Gateway의 다시 쓰기 규칙 작업 세트에서 Url 구성에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="6783d-1401">Added support for Url Confiugration in Rewrite Rules Action Set in the Application Gateway</span></span>
    - <span data-ttu-id="6783d-1402">추가된 새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1402">New cmdlets added:</span></span>
        - <span data-ttu-id="6783d-1403">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="6783d-1403">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span></span>
    - <span data-ttu-id="6783d-1404">선택적 매개 변수를 사용하도록 Cmdlet 업데이트 - UrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="6783d-1404">Cmdlets updated with optional parameter - UrlConfiguration</span></span>
        - <span data-ttu-id="6783d-1405">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="6783d-1405">New-AzApplicationGatewayRewriteRuleActionSet</span></span>
* <span data-ttu-id="6783d-1406">NetworkWatcher ConnectionMonitor 버전 2 리소스에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="6783d-1406">Add suppport for NetworkWatcher ConnectionMonitor version 2 resources</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="6783d-1407">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="6783d-1407">Az.PolicyInsights</span></span>
* <span data-ttu-id="6783d-1408">수정할 리소스를 결정하기 전에 규정 준수 평가 지원</span><span class="sxs-lookup"><span data-stu-id="6783d-1408">Support evaluating compliance prior to determining what resource to remediate</span></span>
    - <span data-ttu-id="6783d-1409">Start-AzPolicyRemediation에 '-ResourceDiscoverMode' 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="6783d-1409">Add '-ResourceDiscoverMode' parameter to Start-AzPolicyRemediation</span></span>
* <span data-ttu-id="6783d-1410">정책 메타데이터 리소스를 가져오는 Get-AzPolicyMetadata cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="6783d-1410">Add Get-AzPolicyMetadata cmdlet for getting policy metadata resources</span></span>
* <span data-ttu-id="6783d-1411">API 버전 2019-10-01의 Get-AzPolicyState 및 Get-AzPolicyStateSummary 업데이트</span><span class="sxs-lookup"><span data-stu-id="6783d-1411">Updated Get-AzPolicyState and Get-AzPolicyStateSummary for API version 2019-10-01</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="6783d-1412">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="6783d-1412">Az.RecoveryServices</span></span>
* <span data-ttu-id="6783d-1413">복제된 디스크를 제거할 수 있도록 Azure Site Recovery에 지원 추가</span><span class="sxs-lookup"><span data-stu-id="6783d-1413">Azure Site Recovery support for removing a replicated disk.</span></span>
* <span data-ttu-id="6783d-1414">Recovery Services 자격 증명 모음을 만드는 동안 태그를 추가할 수 있도록 Azure Backup에 지원 추가</span><span class="sxs-lookup"><span data-stu-id="6783d-1414">Azure Backup added support for adding tags while creating a Recovery Services Vault.</span></span>

#### <a name="azresources"></a><span data-ttu-id="6783d-1415">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6783d-1415">Az.Resources</span></span>
* <span data-ttu-id="6783d-1416">컨텍스트 구독을 기본값으로 하는 \*-AzPolicyAssignment cmdlet에서 -Scope를 선택 사항으로 설정</span><span class="sxs-lookup"><span data-stu-id="6783d-1416">Make -Scope optional in \*-AzPolicyAssignment cmdlets with default to context subscription</span></span>
* <span data-ttu-id="6783d-1417">암호 및 키 자격 증명을 사용하여 ADServicePrincipal을 만드는 예제 추가</span><span class="sxs-lookup"><span data-stu-id="6783d-1417">Add examples of creating ADServicePrincipal with password and key credential</span></span>

#### <a name="azsql"></a><span data-ttu-id="6783d-1418">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6783d-1418">Az.Sql</span></span>
<span data-ttu-id="6783d-1419">DatabaseName 대신 PartnerDatabaseName이 있는지 확인하도록 New-AzSqlDatabaseSecondary cmdlet 수정</span><span class="sxs-lookup"><span data-stu-id="6783d-1419">Fix New-AzSqlDatabaseSecondary cmdlet to check for PartnerDatabaseName existence instead of DatabaseName existence.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="6783d-1420">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="6783d-1420">Az.Storage</span></span>
* <span data-ttu-id="6783d-1421">스토리지 계정 만들기에서 테이블/큐 암호화 Keytype 설정 지원</span><span class="sxs-lookup"><span data-stu-id="6783d-1421">Support set Table/Queue Encryption Keytype in Create Storage Account</span></span>
    - <span data-ttu-id="6783d-1422">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6783d-1422">New-AzStorageAccount</span></span>
* <span data-ttu-id="6783d-1423">StorageException에 ExtendedErrorInformation이 없으면 RequestId 표시</span><span class="sxs-lookup"><span data-stu-id="6783d-1423">Show RequestId when StorageException don't have ExtendedErrorInformation</span></span>
* <span data-ttu-id="6783d-1424">cmdlet Start-AzStorageBlobCopy의 예제 6 수정</span><span class="sxs-lookup"><span data-stu-id="6783d-1424">Fix the Example 6 of cmdlet Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="6783d-1425">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="6783d-1425">Az.Websites</span></span>
* <span data-ttu-id="6783d-1426">Set-AzWebapp 및 Set-AzWebappSlot이 AlwaysOn, MinTls 및 FtpsState 속성 지원</span><span class="sxs-lookup"><span data-stu-id="6783d-1426">Set-AzWebapp and Set-AzWebappSlot supports AlwaysOn, MinTls and FtpsState properties</span></span>
* <span data-ttu-id="6783d-1427">단일 Set-AzWebApp 명령을 사용하여 AppservicePlan을 변경하는 동시에 HttpsOnly를 설정하면 HttpsOnly가 기본값으로 다시 설정되는 문제 수정</span><span class="sxs-lookup"><span data-stu-id="6783d-1427">Fixing issue where setting HttpsOnly along with changing AppservicePlan at the same time using the single Set-AzWebApp Command, was resetting HttpsOnly to default value</span></span>

## <a name="330---january-2020"></a><span data-ttu-id="6783d-1428">3.3.0 - 2020년 1월</span><span class="sxs-lookup"><span data-stu-id="6783d-1428">3.3.0 - January 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="6783d-1429">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6783d-1429">Az.Accounts</span></span>
* <span data-ttu-id="6783d-1430">AzureAttestationServiceEndpointResourceId 및 AzureAttestationServiceEndpointSuffix 매개 변수를 허용하도록 Add-AzEnvironment 및 Set-AzEnvironment가 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="6783d-1430">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameters AzureAttestationServiceEndpointResourceId and AzureAttestationServiceEndpointSuffix</span></span>

#### <a name="azcdn"></a><span data-ttu-id="6783d-1431">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="6783d-1431">Az.Cdn</span></span>
* <span data-ttu-id="6783d-1432">New-AzCdnEndpoint cmdlet에서 오류 응답 세부 정보 표시</span><span class="sxs-lookup"><span data-stu-id="6783d-1432">Display error response detail in New-AzCdnEndpoint cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6783d-1433">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6783d-1433">Az.Compute</span></span>
* <span data-ttu-id="6783d-1434">OS 프로필이 없는 관리 OD 디스크가 있는 VM의 Set-AzVMCustomScriptExtension cmdlet을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1434">Fix Set-AzVMCustomScriptExtension cmdlet for a VM with managed OD disk which does not have OS profile.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="6783d-1435">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="6783d-1435">Az.ContainerInstance</span></span>
* <span data-ttu-id="6783d-1436">New-AzContainerGroup의 예에서 사용되는 고정 매개 변수 이름</span><span class="sxs-lookup"><span data-stu-id="6783d-1436">Fixed parameter names used by example of New-AzContainerGroup</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="6783d-1437">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="6783d-1437">Az.DataBoxEdge</span></span>
* <span data-ttu-id="6783d-1438">'Get-AzDataBoxEdgeStorageContainer' cmdlet 추가됨</span><span class="sxs-lookup"><span data-stu-id="6783d-1438">Added cmdlet 'Get-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="6783d-1439">Edge 스토리지 컨테이너 가져오기</span><span class="sxs-lookup"><span data-stu-id="6783d-1439">Get the Edge Storage Container</span></span>
* <span data-ttu-id="6783d-1440">'New-AzDataBoxEdgeStorageContainer' cmdlet 추가됨</span><span class="sxs-lookup"><span data-stu-id="6783d-1440">Added cmdlet 'New-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="6783d-1441">새 Edge 스토리지 컨테이너 만들기</span><span class="sxs-lookup"><span data-stu-id="6783d-1441">Create new Edge Strorage Container</span></span>
* <span data-ttu-id="6783d-1442">'Remove-AzDataBoxEdgeStorageContainer' cmdlet 추가됨</span><span class="sxs-lookup"><span data-stu-id="6783d-1442">Added cmdlet 'Remove-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="6783d-1443">Edge 스토리지 컨테이너 제거</span><span class="sxs-lookup"><span data-stu-id="6783d-1443">Remove the Edge Storage Container</span></span>
* <span data-ttu-id="6783d-1444">'Invoke-AzDataBoxEdgeStorageContainer' cmdlet 추가됨</span><span class="sxs-lookup"><span data-stu-id="6783d-1444">Added cmdlet 'Invoke-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="6783d-1445">Edge 스토리지 컨테이너에서 데이터를 새로 고치는 작업 호출</span><span class="sxs-lookup"><span data-stu-id="6783d-1445">Invoke action to refresh data on Edge Storage Container</span></span>
* <span data-ttu-id="6783d-1446">'Get-AzDataBoxEdgeStorageAccount' cmdlet 추가됨</span><span class="sxs-lookup"><span data-stu-id="6783d-1446">Added cmdlet 'Get-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="6783d-1447">Edge 스토리지 계정 가져오기</span><span class="sxs-lookup"><span data-stu-id="6783d-1447">Get the Edge Storage Account</span></span>
* <span data-ttu-id="6783d-1448">'New-AzDataBoxEdgeStorageAccount' cmdlet 추가됨</span><span class="sxs-lookup"><span data-stu-id="6783d-1448">Added cmdlet 'New-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="6783d-1449">새 Edge 스토리지 계정 만들기</span><span class="sxs-lookup"><span data-stu-id="6783d-1449">Create new Edge Storage Account</span></span>
* <span data-ttu-id="6783d-1450">'Remove-AzDataBoxEdgeStorageAccount' cmdlet 추가됨</span><span class="sxs-lookup"><span data-stu-id="6783d-1450">Added cmdlet 'Remove-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="6783d-1451">Edge 스토리지 계정 제거</span><span class="sxs-lookup"><span data-stu-id="6783d-1451">Remove the Edge Storage Account</span></span>
* <span data-ttu-id="6783d-1452">'Invoke-AzDataBoxEdgeShare' cmdlet 호출</span><span class="sxs-lookup"><span data-stu-id="6783d-1452">Invoke cmdlet 'Invoke-AzDataBoxEdgeShare'</span></span>
  - <span data-ttu-id="6783d-1453">공유에서 데이터를 새로 고치는 작업 호출</span><span class="sxs-lookup"><span data-stu-id="6783d-1453">Invoke action to refresh data on share</span></span>
* <span data-ttu-id="6783d-1454">'Set-AzDataBoxEdgeStorageAccountCredential' cmdlet 추가됨</span><span class="sxs-lookup"><span data-stu-id="6783d-1454">Added cmdlet 'Set-AzDataBoxEdgeStorageAccountCredential'</span></span>
  - <span data-ttu-id="6783d-1455">az databoxedge 스토리지 계정 자격 증명 설정</span><span class="sxs-lookup"><span data-stu-id="6783d-1455">Set the az databoxedge storage account credential</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="6783d-1456">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="6783d-1456">Az.DataFactory</span></span>
* <span data-ttu-id="6783d-1457">Get-AzDataFactoryV2IntegrationRuntime cmd에 AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId 및 VersionStatus 속성 추가</span><span class="sxs-lookup"><span data-stu-id="6783d-1457">Add AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId and VersionStatus properties for Get-AzDataFactoryV2IntegrationRuntime cmd</span></span>
* <span data-ttu-id="6783d-1458">ADF .Net SDK 버전을 4.6.0으로 업데이트</span><span class="sxs-lookup"><span data-stu-id="6783d-1458">Update ADF .Net SDK version to 4.6.0</span></span>
* <span data-ttu-id="6783d-1459">고정 공용 IP 주소로 Azure-SSIS IR을 만들 수 있도록 'Set-AzureRmDataFactoryV2IntegrationRuntime'cmd에 대해 'PublicIPs' 매개 변수를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1459">Add parameter 'PublicIPs' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable create Azure-SSIS IR with static public IP addresses.</span></span>

#### <a name="azdevtestlabs"></a><span data-ttu-id="6783d-1460">Az.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="6783d-1460">Az.DevTestLabs</span></span>
* <span data-ttu-id="6783d-1461">Get-AzDtlAllowedVMSizesPolicy.md에서 끊어진 링크 제거</span><span class="sxs-lookup"><span data-stu-id="6783d-1461">Remove the broken link in Get-AzDtlAllowedVMSizesPolicy.md</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="6783d-1462">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="6783d-1462">Az.EventHub</span></span>
* <span data-ttu-id="6783d-1463">10634 문제 해결: eventhubnamespace 제거에 대한 null 개체 참조 수정</span><span class="sxs-lookup"><span data-stu-id="6783d-1463">Fix for issue 10634 : Fix the null Object reference for remove eventhubnamespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="6783d-1464">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="6783d-1464">Az.HDInsight</span></span>
* <span data-ttu-id="6783d-1465">Invoke-AzHDInsightHiveJob.md 오류를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1465">Fix Invoke-AzHDInsightHiveJob.md error.</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="6783d-1466">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="6783d-1466">Az.MachineLearning</span></span>
* <span data-ttu-id="6783d-1467">MachineLearningCompute를 더 이상 사용할 수 없게 되어 아래 cmdlet이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1467">Removed below cmdlets because MachineLearningCompute is not available any longer</span></span>
  - <span data-ttu-id="6783d-1468">Get-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="6783d-1468">Get-AzMlOpCluster</span></span>
  - <span data-ttu-id="6783d-1469">Get-AzMlOpClusterKey</span><span class="sxs-lookup"><span data-stu-id="6783d-1469">Get-AzMlOpClusterKey</span></span>
  - <span data-ttu-id="6783d-1470">New-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="6783d-1470">New-AzMlOpCluster</span></span>
  - <span data-ttu-id="6783d-1471">Remove-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="6783d-1471">Remove-AzMlOpCluster</span></span>
  - <span data-ttu-id="6783d-1472">Set-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="6783d-1472">Set-AzMlOpCluster</span></span>
  - <span data-ttu-id="6783d-1473">Test-AzMlOpClusterSystemServicesUpdateAvailability</span><span class="sxs-lookup"><span data-stu-id="6783d-1473">Test-AzMlOpClusterSystemServicesUpdateAvailability</span></span>
  - <span data-ttu-id="6783d-1474">Update-AzMlOpClusterSystemService</span><span class="sxs-lookup"><span data-stu-id="6783d-1474">Update-AzMlOpClusterSystemService</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6783d-1475">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6783d-1475">Az.Network</span></span>
* <span data-ttu-id="6783d-1476">Microsoft.Azure.Management.Sql의 종속성을 1.36-preview에서 1.37-preview로 업그레이드</span><span class="sxs-lookup"><span data-stu-id="6783d-1476">Upgrade dependency of Microsoft.Azure.Management.Sql from 1.36-preview to 1.37-preview</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="6783d-1477">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="6783d-1477">Az.RecoveryServices</span></span>
* <span data-ttu-id="6783d-1478">Azure Site Recovery는 Azure 간 공급자를 위해 고객 관리 키와 함께 유휴 상태에서 암호화된 관리 디스크 vms의 변경을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1478">Azure Site Recovery change support for managed disk vms encrypted at rest with customer managed keys for Azure to Azure provider.</span></span>
* <span data-ttu-id="6783d-1479">Azure Site Recovery는 VMware에서 Azure로를 위해 보호를 사용할 때 선택적 입력으로서 디스크 암호화 집합 ID를 입력하도록 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1479">Azure Site Recovery support to input disk encryption Set Id as optional input at enabling protection for Vmware to Azure.</span></span>
* <span data-ttu-id="6783d-1480">Azure Site Recovery는 VMware에서 Azure로를 위해 보호를 사용하기 위해 디스크 수준의 선택적 입력으로서 디스크 암호화 집합 ID를 입력하도록 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1480">Azure Site Recovery support to input disk encryption Set Id as optional input at disk level to enable protection for Vmware to Azure.</span></span>
* <span data-ttu-id="6783d-1481">Azure Site Recovery는 HyperV에서 Azure로를 위해 디스크 암호화 집합 맵을 사용하여 복제 보호된 항목을 업데이트하도록 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1481">Azure Site Recovery support to update replication protected item with disk encryption set Map for HyperV to Azure.</span></span>

#### <a name="azresources"></a><span data-ttu-id="6783d-1482">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6783d-1482">Az.Resources</span></span>
* <span data-ttu-id="6783d-1483">'Remove-AzTag'의 도움말 문서에서 오류를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1483">Fix an error in help document of 'Remove-AzTag'.</span></span>

#### <a name="azsql"></a><span data-ttu-id="6783d-1484">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6783d-1484">Az.Sql</span></span>
* <span data-ttu-id="6783d-1485">Azure Database의 마스터 DB에서 작동하도록 취약성 평가 세트 기준 cmdlet 기능을 수정하고 관리형 인스턴스 시스템 데이터베이스에서 이를 제한합니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1485">Fix vulnerability assessment set baseline cmdlets functionality to work on master db for azure database and limit it on managed instance system databases.</span></span>
* <span data-ttu-id="6783d-1486">SQL 인스턴스 장애 조치(failover) 그룹을 만들 때 오류 수정</span><span class="sxs-lookup"><span data-stu-id="6783d-1486">Fix an error when creating SQL instance failover group</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="6783d-1487">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="6783d-1487">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="6783d-1488">올바른 새 라이선스 형식으로 DR 추가</span><span class="sxs-lookup"><span data-stu-id="6783d-1488">Add DR as a new valid License type</span></span>

#### <a name="azstorage"></a><span data-ttu-id="6783d-1489">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="6783d-1489">Az.Storage</span></span>
* <span data-ttu-id="6783d-1490">다음 릴리스에서 DefaultAction Value 변경에 대해 호환성이 손상되는 변경 경고 메시지 추가</span><span class="sxs-lookup"><span data-stu-id="6783d-1490">Add breaking change warning message for DefaultAction Value change in a future release</span></span>
    - <span data-ttu-id="6783d-1491">Update-AzStorageAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="6783d-1491">Update-AzStorageAccountNetworkRuleSet</span></span>
* <span data-ttu-id="6783d-1492">-IncludeGeoReplicationStats 매개 변수와 함께 get-AzureRMStorageAccount를 실행하여 스토리지 계정의 마지막 동기화 시간 가져오기 지원</span><span class="sxs-lookup"><span data-stu-id="6783d-1492">Support Get last sync time of Storage account by run get-AzureRMStorageAccount with parameter -IncludeGeoReplicationStats</span></span>
    - <span data-ttu-id="6783d-1493">Get-AzureRMStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6783d-1493">Get-AzureRMStorageAccount</span></span>

## <a name="320---december-2019"></a><span data-ttu-id="6783d-1494">3.2.0 - 2019년 12월</span><span class="sxs-lookup"><span data-stu-id="6783d-1494">3.2.0 - December 2019</span></span>

### <a name="general"></a><span data-ttu-id="6783d-1495">일반</span><span class="sxs-lookup"><span data-stu-id="6783d-1495">General</span></span>
* <span data-ttu-id="6783d-1496">모든 모듈의 상대 경로를 사용하기 위해 .psd1의 참조 업데이트</span><span class="sxs-lookup"><span data-stu-id="6783d-1496">Update references in .psd1 to use relative path for all modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="6783d-1497">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6783d-1497">Az.Accounts</span></span>
* <span data-ttu-id="6783d-1498">Az 4.0 미리 보기를 위해 클라이언트 측 원격 분석에 대해 UserAgent를 올바르게 설정</span><span class="sxs-lookup"><span data-stu-id="6783d-1498">Set correct UserAgent for client-side telemetry for Az 4.0 preview</span></span>
* <span data-ttu-id="6783d-1499">Az 4.0 미리 보기에서 컨텍스트가 null인 경우 사용자에게 친숙한 오류 메시지로 표시</span><span class="sxs-lookup"><span data-stu-id="6783d-1499">Display user friendly error message when context is null in Az 4.0 preview</span></span>

#### <a name="azbatch"></a><span data-ttu-id="6783d-1500">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="6783d-1500">Az.Batch</span></span>
* <span data-ttu-id="6783d-1501">**New-AzBatchPool** 이 'VirtualMachineConfiguration.ContainerConfiguration' 또는 'VirtualMachineConfiguration.DataDisks'를 서버로 제대로 보내지 않는 [#10602](https://github.com/Azure/azure-powershell/issues/10602) 문제 수정</span><span class="sxs-lookup"><span data-stu-id="6783d-1501">Fix issue [#10602](https://github.com/Azure/azure-powershell/issues/10602), where **New-AzBatchPool** did not properly send 'VirtualMachineConfiguration.ContainerConfiguration' or 'VirtualMachineConfiguration.DataDisks' to the server.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="6783d-1502">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="6783d-1502">Az.DataFactory</span></span>
* <span data-ttu-id="6783d-1503">ADF .Net SDK 버전을 4.5.0으로 업데이트</span><span class="sxs-lookup"><span data-stu-id="6783d-1503">Update ADF .Net SDK version to 4.5.0</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="6783d-1504">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="6783d-1504">Az.FrontDoor</span></span>
* <span data-ttu-id="6783d-1505">WAF 관리 규칙 제외 지원 추가됨</span><span class="sxs-lookup"><span data-stu-id="6783d-1505">Added WAF managed rules exclusion support</span></span>
* <span data-ttu-id="6783d-1506">자동 완성에 SocketAddr 추가</span><span class="sxs-lookup"><span data-stu-id="6783d-1506">Add SocketAddr to auto-complete</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="6783d-1507">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="6783d-1507">Az.HealthcareApis</span></span>
* <span data-ttu-id="6783d-1508">예외 처리</span><span class="sxs-lookup"><span data-stu-id="6783d-1508">Exception Handling</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="6783d-1509">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="6783d-1509">Az.KeyVault</span></span>
* <span data-ttu-id="6783d-1510">잠재적으로 설정되지 않은 오류 액세스 값 수정</span><span class="sxs-lookup"><span data-stu-id="6783d-1510">Fixed error accessing value that is potentially not set</span></span>
* <span data-ttu-id="6783d-1511">타원 곡선 암호화 인증서 관리</span><span class="sxs-lookup"><span data-stu-id="6783d-1511">Elliptic Curve Cryptography Certificate Managment</span></span>
    - <span data-ttu-id="6783d-1512">인증서 정책에 대한 곡선 지정을 위한 지원 추가됨</span><span class="sxs-lookup"><span data-stu-id="6783d-1512">Added support to specify the Curve for Certificate Policies</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="6783d-1513">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="6783d-1513">Az.Monitor</span></span>
* <span data-ttu-id="6783d-1514">진단 설정 추가 명령에 선택적 인수 추가</span><span class="sxs-lookup"><span data-stu-id="6783d-1514">Adding optional argument to the Add Diagnostic Settings command.</span></span> <span data-ttu-id="6783d-1515">스위치 인수(있는 경우)는 Log Analytics로 내보내기가 고정 스키마(전용 데이터 유형)가 되어야 함을</span><span class="sxs-lookup"><span data-stu-id="6783d-1515">A switch argument that if present indicates that the export to Log Analytics must be to a fixed schema (a.k.a.</span></span> <span data-ttu-id="6783d-1516">나타냄</span><span class="sxs-lookup"><span data-stu-id="6783d-1516">dedicated, data type)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6783d-1517">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6783d-1517">Az.Network</span></span>
* <span data-ttu-id="6783d-1518">AzureFirewall 애플리케이션, NAT 및 네트워크 규칙에서 IpGroups 지원.</span><span class="sxs-lookup"><span data-stu-id="6783d-1518">Support for IpGroups in AzureFirewall Application,Nat & Network Rules.</span></span>

#### <a name="azresources"></a><span data-ttu-id="6783d-1519">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6783d-1519">Az.Resources</span></span>
* <span data-ttu-id="6783d-1520">이름이 일부 내장 매개 변수 이름과 충돌하는 경우 템플릿 배포가 템플릿 매개 변수를 읽지 못하는 문제 수정.</span><span class="sxs-lookup"><span data-stu-id="6783d-1520">Fix an issue where template deployment fails to read a template parameter if its name conflicts with some built-in parameter name.</span></span>
* <span data-ttu-id="6783d-1521">정책 세트 정의 내에 그룹화 지원을 도입하는 새로운 API 버전 2019-09-01을 사용하도록 정책 cmdlet 업데이트.</span><span class="sxs-lookup"><span data-stu-id="6783d-1521">Updated policy cmdlets to use new api version 2019-09-01 that introduces grouping support within policy set definitions.</span></span>

#### <a name="azsql"></a><span data-ttu-id="6783d-1522">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6783d-1522">Az.Sql</span></span>
* <span data-ttu-id="6783d-1523">취약성 평가 자동 활성화에서 스토리지 생성을 StorageV2로 업그레이드</span><span class="sxs-lookup"><span data-stu-id="6783d-1523">Upgraded storage creation in Vulnerability Assessment auto enablement to StorageV2</span></span>

#### <a name="azstorage"></a><span data-ttu-id="6783d-1524">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="6783d-1524">Az.Storage</span></span>
* <span data-ttu-id="6783d-1525">Oauth 인증을 기반으로 스토리지 컨텍스트를 사용하여 Blob/컨테이너 ID 기반 SAS 토큰 생성 지원</span><span class="sxs-lookup"><span data-stu-id="6783d-1525">Support generate Blob/Constainer Idenity based SAS token with Storage Context based on Oauth authentication</span></span>
    - <span data-ttu-id="6783d-1526">New-AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="6783d-1526">New-AzStorageContainerSASToken</span></span>
    - <span data-ttu-id="6783d-1527">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="6783d-1527">New-AzStorageBlobSASToken</span></span>
* <span data-ttu-id="6783d-1528">모든 Idenity SAS 토큰을 해지할 수 있도록 스토리지 계정 사용자 위임 키 해지 지원</span><span class="sxs-lookup"><span data-stu-id="6783d-1528">Support revoke Storage Account User Delegation Keys, so all Idenity SAS tokens are revoked</span></span>
    - <span data-ttu-id="6783d-1529">Revoke-AzStorageAccountUserDelegationKeys</span><span class="sxs-lookup"><span data-stu-id="6783d-1529">Revoke-AzStorageAccountUserDelegationKeys</span></span>
* <span data-ttu-id="6783d-1530">새로운 API 버전 2019-06-01을 지원하기 위해 Microsoft.Azure.Management.Storage 14.2.0으로 업그레이드.</span><span class="sxs-lookup"><span data-stu-id="6783d-1530">Upgrade to Microsoft.Azure.Management.Storage 14.2.0, to support new API version 2019-06-01.</span></span>
* <span data-ttu-id="6783d-1531">File Share cmdlet의 관리 평면에서 5120을 초과하는 값에 대해 QuotaGiB(Gibyby의 공유 할당량)를 지원하고 'Quota' 매개 변수 별칭을 'QuotaGiB' 매개 변수에 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1531">Support of QuotaGiB (Share Quota in Gibibye) for values of more than 5120 in the Management plane of File Share cmdlets and added the 'Quota' parameter alias to the 'QuotaGiB' parameter.</span></span>
    - <span data-ttu-id="6783d-1532">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="6783d-1532">New-AzRmStorageShare</span></span>
    - <span data-ttu-id="6783d-1533">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="6783d-1533">Update-AzRmStorageShare</span></span>
* <span data-ttu-id="6783d-1534">매개 변수 'Quota'에 매개 변수 별칭 'QuotaGiB' 추가</span><span class="sxs-lookup"><span data-stu-id="6783d-1534">Add parameter alias 'QuotaGiB' to parameter 'Quota'</span></span>
    - <span data-ttu-id="6783d-1535">Set-AzStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="6783d-1535">Set-AzStorageShareQuota</span></span>
* <span data-ttu-id="6783d-1536">Set-AzStorageContainerAcl가 저장된 액세스 정책을 정리할 수 있는 문제 수정</span><span class="sxs-lookup"><span data-stu-id="6783d-1536">Fix the issue that Set-AzStorageContainerAcl can clean up the stored Access Policy</span></span>
    - <span data-ttu-id="6783d-1537">Set-AzStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="6783d-1537">Set-AzStorageContainerAcl</span></span>

## <a name="310---november-2019"></a><span data-ttu-id="6783d-1538">3.1.0 - 2019년 11월</span><span class="sxs-lookup"><span data-stu-id="6783d-1538">3.1.0 - November 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="6783d-1539">마지막 주 릴리스 이후의 주요 사항</span><span class="sxs-lookup"><span data-stu-id="6783d-1539">Highlights since the last major release</span></span>
* <span data-ttu-id="6783d-1540">Az.DataBoxEdge 1.0.0 릴리스됨</span><span class="sxs-lookup"><span data-stu-id="6783d-1540">Az.DataBoxEdge 1.0.0 released</span></span>
* <span data-ttu-id="6783d-1541">Az.SqlVirtualMachine 1.0.0 릴리스됨</span><span class="sxs-lookup"><span data-stu-id="6783d-1541">Az.SqlVirtualMachine 1.0.0 released</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6783d-1542">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6783d-1542">Az.Compute</span></span>
* <span data-ttu-id="6783d-1543">VM Reapply 기능</span><span class="sxs-lookup"><span data-stu-id="6783d-1543">VM Reapply feature</span></span>
    - <span data-ttu-id="6783d-1544">Set-AzVM cmdlet에 Reapply 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="6783d-1544">Add Reapply parameter to Set-AzVM cmdlet</span></span>
* <span data-ttu-id="6783d-1545">VM 확장 집합 AutomaticRepairs 기능:</span><span class="sxs-lookup"><span data-stu-id="6783d-1545">VM Scale Set AutomaticRepairs feature:</span></span>
    - <span data-ttu-id="6783d-1546">다음 cmdlet에 EnableAutomaticRepair, AutomaticRepairGracePeriod 및 AutomaticRepairMaxInstanceRepairsPercent 매개 변수를 추가합니다.   New-AzVmssConfig   Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="6783d-1546">Add EnableAutomaticRepair, AutomaticRepairGracePeriod, and AutomaticRepairMaxInstanceRepairsPercent parameters to the following cmdlets:   New-AzVmssConfig   Update-AzVmss</span></span>
* <span data-ttu-id="6783d-1547">New-AzVM에 대한 교차 테넌트 갤러리 이미지 지원</span><span class="sxs-lookup"><span data-stu-id="6783d-1547">Cross tenant gallery image support for New-AzVM</span></span>
* <span data-ttu-id="6783d-1548">New-AzVM, New-AzVMConfig 및 New-AzVmss cmdlet의 Priority 매개 변수의 인수 완성자에 'Spot' 추가</span><span class="sxs-lookup"><span data-stu-id="6783d-1548">Add 'Spot' to the argument completer of Priority parameter in New-AzVM, New-AzVMConfig and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="6783d-1549">Add-AzVmssDataDisk cmdlet에 DiskIOPSReadWrite 및 DiskMBpsReadWrite 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="6783d-1549">Add DiskIOPSReadWrite and DiskMBpsReadWrite parameters to Add-AzVmssDataDisk cmdlet</span></span>
* <span data-ttu-id="6783d-1550">New-AzGalleryImageVersion cmdlet의 SourceImageId 매개 변수를 선택 사항으로 변경</span><span class="sxs-lookup"><span data-stu-id="6783d-1550">Change SourceImageId parameter of New-AzGalleryImageVersion cmdlet to optional</span></span>
* <span data-ttu-id="6783d-1551">New-AzGalleryImageVersion cmdlet에 OSDiskImage 및 DataDiskImage 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="6783d-1551">Add OSDiskImage and DataDiskImage parameters to New-AzGalleryImageVersion cmdlet</span></span>
* <span data-ttu-id="6783d-1552">New-AzGalleryImageDefinition cmdlet에 HyperVGeneration 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="6783d-1552">Add HyperVGeneration parameter to New-AzGalleryImageDefinition cmdlet</span></span>
* <span data-ttu-id="6783d-1553">New-AzVmss, New-AzVmssConfig 및 Update-AzVmss cmdlet에 SkipExtensionsOnOverprovisionedVMs 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="6783d-1553">Add SkipExtensionsOnOverprovisionedVMs parameters to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="6783d-1554">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="6783d-1554">Az.DataBoxEdge</span></span>
* <span data-ttu-id="6783d-1555">cmdlet `Get-AzDataBoxEdgeOrder` 추가됨</span><span class="sxs-lookup"><span data-stu-id="6783d-1555">Added cmdlet `Get-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="6783d-1556">주문 가져오기</span><span class="sxs-lookup"><span data-stu-id="6783d-1556">Get the Order</span></span>
* <span data-ttu-id="6783d-1557">cmdlet `New-AzDataBoxEdgeOrder` 추가됨</span><span class="sxs-lookup"><span data-stu-id="6783d-1557">Added cmdlet `New-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="6783d-1558">새 주문 만들기</span><span class="sxs-lookup"><span data-stu-id="6783d-1558">Create new Order</span></span>
* <span data-ttu-id="6783d-1559">cmdlet `Remove-AzDataBoxEdgeOrder` 추가됨</span><span class="sxs-lookup"><span data-stu-id="6783d-1559">Added cmdlet `Remove-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="6783d-1560">주문 제거</span><span class="sxs-lookup"><span data-stu-id="6783d-1560">Remove the Order</span></span>
* <span data-ttu-id="6783d-1561">cmdlet `New-AzDataBoxEdgeShare` 변경</span><span class="sxs-lookup"><span data-stu-id="6783d-1561">Change in cmdlet `New-AzDataBoxEdgeShare`</span></span>
    - <span data-ttu-id="6783d-1562">이제 로컬 공유를 만듬</span><span class="sxs-lookup"><span data-stu-id="6783d-1562">Now creates Local Share</span></span>
* <span data-ttu-id="6783d-1563">cmdlet `Set-AzDataBoxEdgeRole` 추가됨</span><span class="sxs-lookup"><span data-stu-id="6783d-1563">Added cmdlet `Set-AzDataBoxEdgeRole`</span></span>
    - <span data-ttu-id="6783d-1564">이제 IotRole을 공유에 매핑할 수 있음</span><span class="sxs-lookup"><span data-stu-id="6783d-1564">Now IotRole can be mapped to Share</span></span>
* <span data-ttu-id="6783d-1565">cmdlet `Invoke-AzDataBoxEdgeDevice` 추가됨</span><span class="sxs-lookup"><span data-stu-id="6783d-1565">Added cmdlet `Invoke-AzDataBoxEdgeDevice`</span></span>
    - <span data-ttu-id="6783d-1566">스캔 업데이트 호출, 업데이트 다운로드, 디바이스에 업데이트 설치</span><span class="sxs-lookup"><span data-stu-id="6783d-1566">Invoke scan update, download update, install updates on the device</span></span>
* <span data-ttu-id="6783d-1567">cmdlet `Get-AzDataBoxEdgeTrigger` 추가됨</span><span class="sxs-lookup"><span data-stu-id="6783d-1567">Added cmdlet `Get-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="6783d-1568">트리거에 대한 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="6783d-1568">Gets the information about Triggers</span></span>
* <span data-ttu-id="6783d-1569">cmdlet `New-AzDataBoxEdgeTrigger` 추가됨</span><span class="sxs-lookup"><span data-stu-id="6783d-1569">Added cmdlet `New-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="6783d-1570">새 트리거 만들기</span><span class="sxs-lookup"><span data-stu-id="6783d-1570">Create new Triggers</span></span>
* <span data-ttu-id="6783d-1571">cmdlet `Remove-AzDataBoxEdgeTrigger` 추가됨</span><span class="sxs-lookup"><span data-stu-id="6783d-1571">Added cmdlet `Remove-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="6783d-1572">트리거 제거</span><span class="sxs-lookup"><span data-stu-id="6783d-1572">Remove the Triggers</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="6783d-1573">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="6783d-1573">Az.DataFactory</span></span>
* <span data-ttu-id="6783d-1574">ADF .Net SDK 버전을 4.4.0으로 업데이트</span><span class="sxs-lookup"><span data-stu-id="6783d-1574">Update ADF .Net SDK version to 4.4.0</span></span>
* <span data-ttu-id="6783d-1575">'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd에 'ExpressCustomSetup' 매개 변수를 추가하여 사용자 지정 설치 스크립트 없이 설치 구성 및 타사 구성 요소를 사용하도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1575">Add parameter 'ExpressCustomSetup' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable setup configurations and 3rd party components without custom setup script.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="6783d-1576">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="6783d-1576">Az.DataLakeStore</span></span>
* <span data-ttu-id="6783d-1577">Get-AzDataLakeStoreDeletedItem 및 Restore-AzDataLakeStoreDeletedItem의 설명서 업데이트</span><span class="sxs-lookup"><span data-stu-id="6783d-1577">Update documentation of Get-AzDataLakeStoreDeletedItem and Restore-AzDataLakeStoreDeletedItem</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="6783d-1578">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="6783d-1578">Az.EventHub</span></span>
* <span data-ttu-id="6783d-1579">10301 문제 해결: SAS 토큰 날짜 형식 수정</span><span class="sxs-lookup"><span data-stu-id="6783d-1579">Fix for issue 10301 : Fix the SAS Token date format</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="6783d-1580">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="6783d-1580">Az.FrontDoor</span></span>
* <span data-ttu-id="6783d-1581">Enable-AzFrontDoorCustomDomainHttps 및 New-AzFrontDoorFrontendEndpointObject에 MinimumTlsVersion 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="6783d-1581">Add MinimumTlsVersion parameter to Enable-AzFrontDoorCustomDomainHttps and New-AzFrontDoorFrontendEndpointObject</span></span>
* <span data-ttu-id="6783d-1582">New-AzFrontDoorHealthProbeSettingObject에 HealthProbeMethod 및 EnabledState 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="6783d-1582">Add HealthProbeMethod and EnabledState parameters to New-AzFrontDoorHealthProbeSettingObject</span></span>
* <span data-ttu-id="6783d-1583">BackendPoolsSettings 개체를 생성하여 Front Door 생성/업데이트에 전달하는 새 cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="6783d-1583">Add new cmdlet to create BackendPoolsSettings objec to pass into creation/update of Front Door</span></span>
    - <span data-ttu-id="6783d-1584">New-AzFrontDoorBackendPoolsSettingObject</span><span class="sxs-lookup"><span data-stu-id="6783d-1584">New-AzFrontDoorBackendPoolsSettingObject</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6783d-1585">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6783d-1585">Az.Network</span></span>
* <span data-ttu-id="6783d-1586">'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' 및 'Start-AzVirtualnetworkGatewayPacketCapture.md' FilterData 옵션 예제를 변경합니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1586">Change 'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' and 'Start-AzVirtualnetworkGatewayPacketCapture.md' FilterData option examples.</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="6783d-1587">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="6783d-1587">Az.PrivateDns</span></span>
* <span data-ttu-id="6783d-1588">PrivateDns .net sdk를 버전 1.0.0으로 업데이트함</span><span class="sxs-lookup"><span data-stu-id="6783d-1588">Updated PrivateDns .net sdk to version 1.0.0</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="6783d-1589">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="6783d-1589">Az.RecoveryServices</span></span>
* <span data-ttu-id="6783d-1590">보호를 사용하도록 설정할 때 디스크 유형을 선택하도록 Azure Site Recovery 지원</span><span class="sxs-lookup"><span data-stu-id="6783d-1590">Azure Site Recovery support to select disk type at enabling protection.</span></span>
* <span data-ttu-id="6783d-1591">복구 계획 동작 편집을 위한 Azure Site Recovery 버그 수정</span><span class="sxs-lookup"><span data-stu-id="6783d-1591">Azure Site Recovery bug fix for recovery plan action edit.</span></span>
* <span data-ttu-id="6783d-1592">파일 스트림 DB를 허용하도록 Azure Backup SQL 복원 지원</span><span class="sxs-lookup"><span data-stu-id="6783d-1592">Azure Backup SQL Restore support to accept filestream DBs.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="6783d-1593">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="6783d-1593">Az.RedisCache</span></span>
* <span data-ttu-id="6783d-1594">'New-AzRedisCache' 및 'Set-AzRedisCache' cmdlet에 'MinimumTlsVersion' 매개 변수가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1594">Added 'MinimumTlsVersion' parameter in 'New-AzRedisCache' and 'Set-AzRedisCache' cmdlets.</span></span> <span data-ttu-id="6783d-1595">'Get-AzRedisCache' cmdlet 출력에 'MinimumTlsVersion'도 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1595">Also, added 'MinimumTlsVersion' in the output of 'Get-AzRedisCache' cmdlet.</span></span>
* <span data-ttu-id="6783d-1596">'Set-AzRedisCache' 및 'New-AzRedisCache' cmdlet의 '-Size' 매개 변수에 대한 유효성 검사가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1596">Added validation on '-Size' parameter for 'Set-AzRedisCache' and 'New-AzRedisCache' cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="6783d-1597">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6783d-1597">Az.Resources</span></span>
- <span data-ttu-id="6783d-1598">정책 할당에 새로운 EnforcementMode 속성이 있는 새 api 버전 2019-06-01을 사용하도록 정책 cmdlet이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1598">Updated policy cmdlets to use new api version 2019-06-01 that has new EnforcementMode property in policy assignment.</span></span>
- <span data-ttu-id="6783d-1599">정책 정의 만들기 도움말 예제가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1599">Updated create policy definition help example</span></span>
- <span data-ttu-id="6783d-1600">Remove-AZADServicePrincipal -ServicePrincipalName 버그를 수정하고, 서비스 사용자 이름을 찾을 수 없으면 null 참조를 throw합니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1600">Fix bug Remove-AZADServicePrincipal -ServicePrincipalName, throw null reference when service principal name not found.</span></span>
- <span data-ttu-id="6783d-1601">New-AZADServicePrincipal 버그를 수정하고, 테넌트에 구독이 없으면 null 참조를 throw합니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1601">Fix bug New-AZADServicePrincipal, throw null reference when tenant doesn't have any subscription.</span></span>
- <span data-ttu-id="6783d-1602">연결된 애플리케이션에만 자격 증명을 추가하도록 New-AzAdServicePrincipal을 변경합니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1602">Change New-AzAdServicePrincipal to add credentials only to associated application.</span></span>

#### <a name="azsql"></a><span data-ttu-id="6783d-1603">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6783d-1603">Az.Sql</span></span>
* <span data-ttu-id="6783d-1604">데이터베이스 ReadReplicaCount에 대한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1604">Added support for database ReadReplicaCount.</span></span>
* <span data-ttu-id="6783d-1605">영역 중복이 설정되지 않은 경우 Set-AzSqlDatabase가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1605">Fixed Set-AzSqlDatabase when zone redundancy not set</span></span>

## <a name="300---november-2019"></a><span data-ttu-id="6783d-1606">3.0.0 - 2019년 11월</span><span class="sxs-lookup"><span data-stu-id="6783d-1606">3.0.0 - November 2019</span></span>
### <a name="general"></a><span data-ttu-id="6783d-1607">일반</span><span class="sxs-lookup"><span data-stu-id="6783d-1607">General</span></span>
* <span data-ttu-id="6783d-1608">Az.PrivateDns 1.0.0 릴리스</span><span class="sxs-lookup"><span data-stu-id="6783d-1608">Az.PrivateDns 1.0.0 released</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="6783d-1609">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6783d-1609">Az.Accounts</span></span>
* <span data-ttu-id="6783d-1610">'Resolve-Error' 별칭에 사용 중단 메시지를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1610">Add a deprecation message for 'Resolve-Error' alias.</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="6783d-1611">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="6783d-1611">Az.Advisor</span></span>
* <span data-ttu-id="6783d-1612">Get-AzAdvisorRecommendation cmdlet에 새로운 '운영 효율성' 범주가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1612">Added new category 'Operational Excellence' to Get-AzAdvisorRecommendation cmdlet.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="6783d-1613">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="6783d-1613">Az.Batch</span></span>
* <span data-ttu-id="6783d-1614">`BatchAccountContext`의 `CoreQuota` 이름이 `DedicatedCoreQuota`로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1614">Renamed `CoreQuota` on `BatchAccountContext` to `DedicatedCoreQuota`.</span></span> <span data-ttu-id="6783d-1615">또한 `LowPriorityCoreQuota`가 새로 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1615">There is also a new `LowPriorityCoreQuota`.</span></span>
  - <span data-ttu-id="6783d-1616">이 변경 사항은 **Get-AzBatchAccount** 에 영향을 줍니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1616">This impacts **Get-AzBatchAccount** .</span></span>
* <span data-ttu-id="6783d-1617">이제 **New-AzBatchTask** `-ResourceFile` 매개 변수는 새로운 **New-AzBatchResourceFile** cmdlet을 사용하여 구성할 수 있는 `PSResourceFile` 개체의 컬렉션을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1617">**New-AzBatchTask** `-ResourceFile` parameter now takes a collection of `PSResourceFile` objects, which can be constructed using the new **New-AzBatchResourceFile** cmdlet.</span></span>
* <span data-ttu-id="6783d-1618">새로운 **New-AzBatchResourceFile** cmdlet을 통해 `PSResourceFile` 개체를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1618">New **New-AzBatchResourceFile** cmdlet to help create `PSResourceFile` objects.</span></span> <span data-ttu-id="6783d-1619">이들은 `-ResourceFile` 매개 변수의 **New-AzBatchTask** 에 제공될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1619">These can be supplied to **New-AzBatchTask** on the `-ResourceFile` parameter.</span></span>
  - <span data-ttu-id="6783d-1620">그에 따라 기존 `HttpUrl` 방법 외에도 두 가지 종류의 리소스 파일이 새롭게 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1620">This supports two new kinds of resource file in addition to the existing `HttpUrl` way:</span></span>
    - <span data-ttu-id="6783d-1621">`AutoStorageContainerName` 기반 리소스 파일은 전체 자동 스토리지 컨테이너를 일괄 처리 노드에 다운로드합니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1621">`AutoStorageContainerName` based resource files download an entire auto-storage container to the Batch node.</span></span>
    - <span data-ttu-id="6783d-1622">`StorageContainerUrl` 기반 리소스 파일은 URL에 지정된 컨테이너를 일괄 처리 노드에 다운로드합니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1622">`StorageContainerUrl` based resource files download the container specified in the URL to the Batch node.</span></span>
* <span data-ttu-id="6783d-1623">**Get-AzBatchApplication** 으로 반환되는 `PSApplication`의 `ApplicationPackages` 속성이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1623">Removed `ApplicationPackages` property of `PSApplication` returned by **Get-AzBatchApplication** .</span></span>
  - <span data-ttu-id="6783d-1624">이제 **Get-AzBatchApplicationPackage** 를 사용하여 애플리케이션 내부의 특정 패키지를 검색할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1624">The specific packages inside of an application now can be retrieved using **Get-AzBatchApplicationPackage** .</span></span> <span data-ttu-id="6783d-1625">예: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`</span><span class="sxs-lookup"><span data-stu-id="6783d-1625">For example: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span></span>
* <span data-ttu-id="6783d-1626">**Get-AzBatchApplicationPackage** , **New-AzBatchApplicationPackage** , **Remove-AzBatchApplicationPackage** , **Get-AzBatchApplication** , **New-AzBatchApplication** , **Remove-AzBatchApplication** 및 **Set-AzBatchApplication** 에서 `ApplicationId` 이름이 `ApplicationName`으로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1626">Renamed `ApplicationId` to `ApplicationName` on **Get-AzBatchApplicationPackage** , **New-AzBatchApplicationPackage** , **Remove-AzBatchApplicationPackage** , **Get-AzBatchApplication** , **New-AzBatchApplication** , **Remove-AzBatchApplication** , and **Set-AzBatchApplication** .</span></span>
  - <span data-ttu-id="6783d-1627">이제 `ApplicationId`는 `ApplicationName`의 별칭입니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1627">`ApplicationId` now is an alias of `ApplicationName`.</span></span>
* <span data-ttu-id="6783d-1628">새로운 `PSWindowsUserConfiguration` 속성이 `PSUserAccount`에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1628">Added new `PSWindowsUserConfiguration` property to `PSUserAccount`.</span></span>
* <span data-ttu-id="6783d-1629">`PSApplicationPackage`에서 `Version` 이름이 `Name`으로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1629">Renamed `Version` to `Name` on `PSApplicationPackage`.</span></span>
* <span data-ttu-id="6783d-1630">`PSResourceFile`에서 `BlobSource` 이름이 `HttpUrl`으로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1630">Renamed `BlobSource` to `HttpUrl` on `PSResourceFile`.</span></span>
* <span data-ttu-id="6783d-1631">`PSVirtualMachineConfiguration`에서 `OSDisk` 속성이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1631">Removed `OSDisk` property from `PSVirtualMachineConfiguration`.</span></span>
* <span data-ttu-id="6783d-1632">**Set-AzBatchPoolOSVersion** 이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1632">Removed **Set-AzBatchPoolOSVersion** .</span></span> <span data-ttu-id="6783d-1633">이 작업은 더 이상 지원되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1633">This operation is no longer supported.</span></span>
* <span data-ttu-id="6783d-1634">`PSCloudServiceConfiguration`에서 `TargetOSVersion`이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1634">Removed `TargetOSVersion` from `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="6783d-1635">`PSCloudServiceConfiguration`에서 `CurrentOSVersion` 이름이 `OSVersion`으로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1635">Renamed `CurrentOSVersion` to `OSVersion` on `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="6783d-1636">`PSPoolUsageMetrics`에서 `DataEgressGiB` 및 `DataIngressGiB`가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1636">Removed `DataEgressGiB` and `DataIngressGiB` from `PSPoolUsageMetrics`.</span></span>
* <span data-ttu-id="6783d-1637">**Get-AzBatchNodeAgentSku** 가 제거되고 **Get-AzBatchSupportedImage** 로 대체되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1637">Removed **Get-AzBatchNodeAgentSku** and replaced it with  **Get-AzBatchSupportedImage** .</span></span>
  - <span data-ttu-id="6783d-1638">**Get-AzBatchSupportedImage** 가 **Get-AzBatchNodeAgentSku** 와 동일한 데이터를 반환하지만 더 친숙한 형식이 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1638">**Get-AzBatchSupportedImage** returns the same data as **Get-AzBatchNodeAgentSku** but in a more friendly format.</span></span>
  - <span data-ttu-id="6783d-1639">이제 확인되지 않은 이미지도 새롭게 반환됩니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1639">New non-verified images are also now returned.</span></span> <span data-ttu-id="6783d-1640">각 이미지의 `Capabilities` 및 `BatchSupportEndOfLife`에 대한 추가 정보도 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1640">Additional information about `Capabilities` and `BatchSupportEndOfLife` for each image is also included.</span></span>
* <span data-ttu-id="6783d-1641">**New-AzBatchPool** 의 새로운 `MountConfiguration` 매개 변수를 통해 풀의 각 노드에서 원격 파일 시스템을 마운트할 수 있는 기능이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1641">Added ability to mount remote file-systems on each node of a pool via the new `MountConfiguration` parameter of **New-AzBatchPool** .</span></span>
* <span data-ttu-id="6783d-1642">이제 트래픽의 소스 포트를 기준으로 풀에 대한 네트워크 액세스를 차단하는 네트워크 보안 규칙이 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1642">Now support network security rules blocking network access to a pool based on the source port of the traffic.</span></span> <span data-ttu-id="6783d-1643">이 작업은 `PSNetworkSecurityGroupRule`에서 `SourcePortRanges` 속성을 통해 수행됩니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1643">This is done via the `SourcePortRanges` property on `PSNetworkSecurityGroupRule`.</span></span>
* <span data-ttu-id="6783d-1644">컨테이너를 실행할 때 Batch는 이제 컨테이너 작업 디렉터리 또는 일괄 처리 태스크 작업 디렉터리에서 작업 실행을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1644">When running a container, Batch now supports executing the task in the container working directory or in the Batch task working directory.</span></span> <span data-ttu-id="6783d-1645">이 작업은 `PSTaskContainerSettings`에서 `WorkingDirectory` 속성에 의해 제어됩니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1645">This is controlled by the `WorkingDirectory` property on `PSTaskContainerSettings`.</span></span>
* <span data-ttu-id="6783d-1646">새로운 `PublicIPs` 속성을 통해 `PSNetworkConfiguration`에서 공용 IP의 컬렉션을 지정할 수 있는 기능이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1646">Added ability to specify a collection of public IPs on `PSNetworkConfiguration` via the new `PublicIPs` property.</span></span> <span data-ttu-id="6783d-1647">그 결과 사용자 제공 IP 목록의 IP가 풀에 있는 노드에 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1647">This guarantees nodes in the Pool will have an IP from the list user provided IPs.</span></span>
* <span data-ttu-id="6783d-1648">지정하지 않은 경우 이제 `PSSTartTask`에서 `WaitForSuccess`의 기본값은 `$True`입니다(이전에는 `$False`).</span><span class="sxs-lookup"><span data-stu-id="6783d-1648">When not specified, the default value of `WaitForSuccess` on `PSSTartTask` is now `$True` (was `$False`).</span></span>
* <span data-ttu-id="6783d-1649">지정하지 않은 경우 이제 `PSAutoUserSpecification`에서 `Scope`의 기본값은 `Pool`입니다(이전에는 Windows의 경우 `Task`, Linux의 경우에는 `Pool`).</span><span class="sxs-lookup"><span data-stu-id="6783d-1649">When not specified, the default value of `Scope` on `PSAutoUserSpecification` is now `Pool` (was `Task` on Windows and `Pool` on Linux).</span></span>

#### <a name="azcdn"></a><span data-ttu-id="6783d-1650">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="6783d-1650">Az.Cdn</span></span>
* <span data-ttu-id="6783d-1651">RulesEngine에 UrlRewriteAction 및 CacheKeyQueryStringAction이 도입되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1651">Introduced UrlRewriteAction and CacheKeyQueryStringAction to RulesEngine.</span></span>
* <span data-ttu-id="6783d-1652">New-AzDeliveryRuleCondition cmdlet에서 'Selector' 입력 누락과 같은 여러 버그가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1652">Fixed several bugs like missing 'Selector' Input in New-AzDeliveryRuleCondition cmdlet.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6783d-1653">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6783d-1653">Az.Compute</span></span>
* <span data-ttu-id="6783d-1654">디스크 암호화 집합 기능</span><span class="sxs-lookup"><span data-stu-id="6783d-1654">Disk Encryption Set feature</span></span>
    - <span data-ttu-id="6783d-1655">새 cmdlet:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="6783d-1655">New cmdlets:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span></span>
    - <span data-ttu-id="6783d-1656">DiskEncryptionSetId 매개 변수가 다음 cmdlet에 추가되었습니다.   Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="6783d-1656">DiskEncryptionSetId parameter is added to the following cmdlets:   Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span></span>
    - <span data-ttu-id="6783d-1657">DiskEncryptionSetId 및 EncryptionType 매개 변수가 다음 cmdlet에 추가되었습니다.   New-AzDiskConfig   New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="6783d-1657">DiskEncryptionSetId and EncryptionType parameters are added to the following cmdlets:   New-AzDiskConfig   New-AzSnapshotConfig</span></span>
* <span data-ttu-id="6783d-1658">New-AzVmssIPConfig에 PublicIPAddressVersion 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="6783d-1658">Add PublicIPAddressVersion parameter to New-AzVmssIPConfig</span></span>
* <span data-ttu-id="6783d-1659">사용자 지정 스크립트 확장의 FileUris를 공용 설정에서 보호된 설정으로 이동</span><span class="sxs-lookup"><span data-stu-id="6783d-1659">Move FileUris of custom script extension from public setting to protected setting</span></span>
* <span data-ttu-id="6783d-1660">New-AzVmss, New-AzVmssConfig 및 Update-AzVmss cmdlet에 ScaleInPolicy 추가</span><span class="sxs-lookup"><span data-stu-id="6783d-1660">Add ScaleInPolicy to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>
* <span data-ttu-id="6783d-1661">주요 변경 내용</span><span class="sxs-lookup"><span data-stu-id="6783d-1661">Breaking changes</span></span>
    - <span data-ttu-id="6783d-1662">CreateOption이 업로드일 때 UploadSizeInBytes 매개 변수가 New-AzDiskConfig에 대해 DiskSizeGB 대신 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1662">UploadSizeInBytes parameter is used instead of DiskSizeGB for New-AzDiskConfig when CreateOption is Upload</span></span>
    - <span data-ttu-id="6783d-1663">GalleryImageVersion 개체에서 PublishingProfile.Source.ManagedImage.Id가 StorageProfile.Source.Id로 바뀝니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1663">PublishingProfile.Source.ManagedImage.Id is replaced with StorageProfile.Source.Id in GalleryImageVersion object</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="6783d-1664">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="6783d-1664">Az.DataFactory</span></span>
* <span data-ttu-id="6783d-1665">ADF .Net SDK 버전을 4.3.0으로 업데이트</span><span class="sxs-lookup"><span data-stu-id="6783d-1665">Update ADF .Net SDK version to 4.3.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="6783d-1666">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="6783d-1666">Az.DataLakeStore</span></span>
* <span data-ttu-id="6783d-1667">ADLS SDK 버전 업데이트(https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha) , 다음 수정 사항 제공</span><span class="sxs-lookup"><span data-stu-id="6783d-1667">Update ADLS SDK version (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), brings following fixes</span></span>
* <span data-ttu-id="6783d-1668">휴지통 또는 디렉터리 항목의 creationtime을 역직렬화할 수 없을 때 예외가 발생하지 않도록 방지합니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1668">Avoid throwing exception while unable to deserialize the creationtime of the trash or directory entry.</span></span>
* <span data-ttu-id="6783d-1669">adlsclient에서 요청별 시간 제한 설정 노출</span><span class="sxs-lookup"><span data-stu-id="6783d-1669">Expose setting per request timeout in adlsclient</span></span>
* <span data-ttu-id="6783d-1670">badoffset 복구를 위한 원본 syncflag 전달 수정</span><span class="sxs-lookup"><span data-stu-id="6783d-1670">Fix passing the original syncflag for badoffset recovery</span></span>
* <span data-ttu-id="6783d-1671">응답이 확인된 후 연속 토큰을 검색하기 위한 EnumerateDirectory 수정</span><span class="sxs-lookup"><span data-stu-id="6783d-1671">Fix EnumerateDirectory to retrieve continuation token once response is checked</span></span>
* <span data-ttu-id="6783d-1672">Concat 버그 수정</span><span class="sxs-lookup"><span data-stu-id="6783d-1672">Fix Concat Bug</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="6783d-1673">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="6783d-1673">Az.FrontDoor</span></span>
* <span data-ttu-id="6783d-1674">모듈 간 기타 오타가 수정됨</span><span class="sxs-lookup"><span data-stu-id="6783d-1674">Fixed miscellaneous typos across module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="6783d-1675">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="6783d-1675">Az.HDInsight</span></span>
* <span data-ttu-id="6783d-1676">ADLSGen1 스토리지가 포함된 클러스터를 가져오기 위해 Get-AzHDInsightCluster를 사용할 때 고객에게 '올바른 Base-64 문자열이 아닙니다' 오류가 표시되는 버그가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1676">Fixed the bug that customer will get 'Not a valid Base-64 string' error when using Get-AzHDInsightCluster to get the cluster with ADLSGen1 storage.</span></span>
* <span data-ttu-id="6783d-1677">고객이 Azure Data Lake에 액세스하기 위해 서비스 주체 애플리케이션 ID를 제공할 수 있도록 세 가지 cmdlet Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig 및 New-AzHDInsightCluster에 이름이 'ApplicationId'인 매개 변수를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1677">Add a parameter named 'ApplicationId' to three cmdlets Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig and New-AzHDInsightCluster so that customer can provide the service principal application id for accessing Azure Data Lake.</span></span>
* <span data-ttu-id="6783d-1678">Microsoft.Azure.Management.HDInsight가 2.1.0에서 5.1.0으로 변경됨</span><span class="sxs-lookup"><span data-stu-id="6783d-1678">Changed Microsoft.Azure.Management.HDInsight from 2.1.0 to 5.1.0</span></span>
* <span data-ttu-id="6783d-1679">다음 5가지 cmdlet이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1679">Removed five cmdlets:</span></span>
    - <span data-ttu-id="6783d-1680">Get-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="6783d-1680">Get-AzHDInsightOMS</span></span>
    - <span data-ttu-id="6783d-1681">Enable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="6783d-1681">Enable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="6783d-1682">Disable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="6783d-1682">Disable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="6783d-1683">Grant-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="6783d-1683">Grant-AzHDInsightRdpServicesAccess</span></span>
    - <span data-ttu-id="6783d-1684">Revoke-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="6783d-1684">Revoke-AzHDInsightRdpServicesAccess</span></span>
* <span data-ttu-id="6783d-1685">다음 3가지 cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1685">Added three cmdlets:</span></span>
    - <span data-ttu-id="6783d-1686">Get-AzHDInsightOMS 대신 Get-AzHDInsightMonitoring</span><span class="sxs-lookup"><span data-stu-id="6783d-1686">Get-AzHDInsightMonitoring to replace Get-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="6783d-1687">Get-AzHDInsightOMS 대신 Get-AzHDInsightMonitoring</span><span class="sxs-lookup"><span data-stu-id="6783d-1687">Enable-AzHDInsightMonitoring to replace Enable-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="6783d-1688">Disable-AzHDInsightOMS 대신 Disable-AzHDInsightMonitoring</span><span class="sxs-lookup"><span data-stu-id="6783d-1688">Disable-AzHDInsightMonitoring to replace Disable-AzHDInsightOMS.</span></span>
* <span data-ttu-id="6783d-1689">특정 위치의 기능 정보 가져오기를 지원하도록 cmdlet Get-AzHDInsightProperties가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1689">Fixed cmdlet Get-AzHDInsightProperties to support get capabilities information from a specific location.</span></span>
* <span data-ttu-id="6783d-1690">Add-AzHDInsightConfigValue에서 매개 변수 집합('Spark1', 'Spark2')이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1690">Removed parameter sets('Spark1', 'Spark2') from Add-AzHDInsightConfigValue.</span></span>
* <span data-ttu-id="6783d-1691">cmdlet Add-AzHDInsightSecurityProfile의 도움말 문서에 예제를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1691">Add examples to the help documents of cmdlet Add-AzHDInsightSecurityProfile.</span></span>
* <span data-ttu-id="6783d-1692">다음 cmdlet의 출력 유형이 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1692">Changed output type of the following cmdlets:</span></span>
*  - <span data-ttu-id="6783d-1693">Get-AzHDInsightProperties의 출력 유형이 CapabilitiesResponse에서 AzureHDInsightCapabilities로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1693">Changed the output type of Get-AzHDInsightProperties from  CapabilitiesResponse to AzureHDInsightCapabilities.</span></span>
*  - <span data-ttu-id="6783d-1694">Remove-AzHDInsightCluster의 출력 유형이 ClusterGetResponse에서 bool로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1694">Changed the output type of Remove-AzHDInsightCluster from ClusterGetResponse to bool.</span></span>
*  - <span data-ttu-id="6783d-1695">Set-AzHDInsightGatewaySettings의 출력 유형이 HttpConnectivitySettings에서 GatewaySettings로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1695">Changed the output type of Set-AzHDInsightGatewaySettings HttpConnectivitySettings to GatewaySettings.</span></span>
* <span data-ttu-id="6783d-1696">몇 가지 시나리오 테스트 사례가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1696">Added some scenario test cases.</span></span>
* <span data-ttu-id="6783d-1697">일부 별칭 제거: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span><span class="sxs-lookup"><span data-stu-id="6783d-1697">Remove some alias: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="6783d-1698">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="6783d-1698">Az.IotHub</span></span>
* <span data-ttu-id="6783d-1699">주요 변경 내용:</span><span class="sxs-lookup"><span data-stu-id="6783d-1699">Breaking changes:</span></span>
    - <span data-ttu-id="6783d-1700">'Add-AzIotHubEventHubConsumerGroup' cmdlet이 'EventHubEndpointName' 매개 변수를 더 이상 지원하지 않으며 원래 매개 변수 이름에 대해 별칭을 찾을 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1700">The cmdlet 'Add-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="6783d-1701">'Add-AzIotHubEventHubConsumerGroup' cmdlet에 대한 매개 변수 집합 '__AllParameterSets'가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1701">The parameter set '__AllParameterSets' for cmdlet 'Add-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="6783d-1702">'Get-AzIotHubEventHubConsumerGroup' cmdlet이 'EventHubEndpointName' 매개 변수를 더 이상 지원하지 않으며 원래 매개 변수 이름에 대해 별칭을 찾을 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1702">The cmdlet 'Get-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="6783d-1703">'Get-AzIotHubEventHubConsumerGroup' cmdlet에 대한 매개 변수 집합 '__AllParameterSets'가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1703">The parameter set '__AllParameterSets' for cmdlet 'Get-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="6783d-1704">'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' 유형의 'OperationsMonitoringProperties' 속성이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1704">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' has been removed.</span></span>
    - <span data-ttu-id="6783d-1705">'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' 유형의 'OperationsMonitoringProperties' 속성이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1705">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' has been removed.</span></span>
    - <span data-ttu-id="6783d-1706">'New-AzIotHubExportDevice' cmdlet이 더 이상 'New-AzIotHubExportDevices' 별칭을 지원하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1706">The cmdlet 'New-AzIotHubExportDevice' no longer supports the alias 'New-AzIotHubExportDevices'.</span></span>
    - <span data-ttu-id="6783d-1707">'New-AzIotHubImportDevice' cmdlet이 더 이상 'New-AzIotHubImportDevices' 별칭을 지원하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1707">The cmdlet 'New-AzIotHubImportDevice' no longer supports the alias 'New-AzIotHubImportDevices'.</span></span>
    - <span data-ttu-id="6783d-1708">'Remove-AzIotHubEventHubConsumerGroup' cmdlet이 'EventHubEndpointName' 매개 변수를 더 이상 지원하지 않으며 원래 매개 변수 이름에 대해 별칭을 찾을 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1708">The cmdlet 'Remove-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="6783d-1709">'Remove-AzIotHubEventHubConsumerGroup' cmdlet에 대한 매개 변수 집합 '__AllParameterSets'가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1709">The parameter set '__AllParameterSets' for cmdlet 'Remove-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="6783d-1710">'Set-AzIotHub' cmdlet이 'OperationsMonitoringProperties' 매개 변수를 더 이상 지원하지 않으며 원래 매개 변수 이름에 대해 별칭을 찾을 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1710">The cmdlet 'Set-AzIotHub' no longer supports the parameter 'OperationsMonitoringProperties' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="6783d-1711">'Set-AzIotHub' cmdlet에 대한 매개 변수 집합 'UpdateOperationsMonitoringProperties'가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1711">The parameter set 'UpdateOperationsMonitoringProperties' for cmdlet 'Set-AzIotHub' has been removed.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="6783d-1712">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="6783d-1712">Az.RecoveryServices</span></span>
* <span data-ttu-id="6783d-1713">Azure Site Recovery가 Azure-Azure를 위한 NSG, 공용 IP 및 내부 부하 분산 장치와 같은 네트워킹 리소스 구성을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1713">Azure Site Recovery support to configure networking resources like NSG, public IP and internal load balancers for Azure to Azure.</span></span>
* <span data-ttu-id="6783d-1714">Azure Site Recovery가 vMWare-Azure를 위한 관리 디스크에 쓰기를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1714">Azure Site Recovery Support to write to managed disk for vMWare to Azure.</span></span>
* <span data-ttu-id="6783d-1715">Azure Site Recovery가 vMWare-Azure를 위한 NIC 감소를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1715">Azure Site Recovery Support to NIC reduction for vMWare to Azure.</span></span>
* <span data-ttu-id="6783d-1716">Azure Site Recovery가 Azure-Azure를 위한 가속 네트워킹을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1716">Azure Site Recovery Support to accelerated networking for Azure to Azure.</span></span>
* <span data-ttu-id="6783d-1717">Azure Site Recovery가 Azure-Azure를 위한 에이전트 자동 업데이트를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1717">Azure Site Recovery Support to agent auto update for Azure to Azure.</span></span>
* <span data-ttu-id="6783d-1718">Azure Site Recovery가 Azure-Azure를 위한 표준 SSD를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1718">Azure Site Recovery Support to Standard SSD for Azure to Azure.</span></span>
* <span data-ttu-id="6783d-1719">Azure Site Recovery가 Azure-Azure를 위한 두 가지 Azure 디스크 암호화 전달을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1719">Azure Site Recovery Support to Azure Disk Encryption two pass for Azure to Azure.</span></span>
* <span data-ttu-id="6783d-1720">Azure Site Recovery가 Azure-Azure를 위한 새로 추가된 디스크 보호를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1720">Azure Site Recovery Support to protect newly added disk for Azure to Azure.</span></span>
* <span data-ttu-id="6783d-1721">VM을 위한 SoftDelete 기능 및 softdelete를 위한 테스트가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1721">Added SoftDelete feature for VM and added tests for softdelete</span></span>

#### <a name="azresources"></a><span data-ttu-id="6783d-1722">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6783d-1722">Az.Resources</span></span>
* <span data-ttu-id="6783d-1723">종속성 어셈블리 Microsoft.Extensions.Caching.Memory가 1.1.1에서 2.2로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1723">Update dependency assembly Microsoft.Extensions.Caching.Memory from 1.1.1 to 2.2</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6783d-1724">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6783d-1724">Az.Network</span></span>
* <span data-ttu-id="6783d-1725">일반 서비스 공급자 지원을 위해 PrivateEndpointConnection에 대한 모든 cmdlet이 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1725">Change all cmdlets for PrivateEndpointConnection to support generic service provider.</span></span>
    - <span data-ttu-id="6783d-1726">업데이트된 cmdlet:</span><span class="sxs-lookup"><span data-stu-id="6783d-1726">Updated cmdlet:</span></span>
        - <span data-ttu-id="6783d-1727">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="6783d-1727">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="6783d-1728">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="6783d-1728">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="6783d-1729">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="6783d-1729">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="6783d-1730">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="6783d-1730">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="6783d-1731">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="6783d-1731">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="6783d-1732">PrivateLinkResource에 대한 새 cmdlet이 추가되었고 일반 서비스 공급자도 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1732">Add new cmdlet for PrivateLinkResource and it also support generic service provider.</span></span>
    - <span data-ttu-id="6783d-1733">새 cmdlet:</span><span class="sxs-lookup"><span data-stu-id="6783d-1733">New cmdlet:</span></span>
        - <span data-ttu-id="6783d-1734">Get-AzPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="6783d-1734">Get-AzPrivateLinkResource</span></span>
* <span data-ttu-id="6783d-1735">Proxy Protocol V2 기능에 대한 새 필드 및 매개 변수가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1735">Add new fields and parameter for the feature Proxy Protocol V2.</span></span>
    - <span data-ttu-id="6783d-1736">PrivateLinkService에서 EnableProxyProtocol 속성 추가</span><span class="sxs-lookup"><span data-stu-id="6783d-1736">Add property EnableProxyProtocol in PrivateLinkService</span></span>
    - <span data-ttu-id="6783d-1737">PrivateEndpointConnection에서 LinkIdentifier 속성 추가</span><span class="sxs-lookup"><span data-stu-id="6783d-1737">Add property LinkIdentifier in PrivateEndpointConnection</span></span>
    - <span data-ttu-id="6783d-1738">새로운 선택적인 매개 변수인 EnableProxyProtocol을 추가하도록 New-AzPrivateLinkService가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1738">Updated New-AzPrivateLinkService to add a new optional parameter EnableProxyProtocol.</span></span>
* <span data-ttu-id="6783d-1739">'New-AzApplicationGatewaySku' 참조 설명서의 잘못된 매개 변수 설명 수정</span><span class="sxs-lookup"><span data-stu-id="6783d-1739">Fix incorrect parameter description in 'New-AzApplicationGatewaySku' reference documentation</span></span>
* <span data-ttu-id="6783d-1740">Azure 방화벽 정책을 지원하는 새로운 cmdlet</span><span class="sxs-lookup"><span data-stu-id="6783d-1740">New cmdlets to support the azure firewall policy</span></span>
* <span data-ttu-id="6783d-1741">VirtualHub의 자식 리소스 RouteTables에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="6783d-1741">Add support for child resource RouteTables of VirtualHub</span></span>
    - <span data-ttu-id="6783d-1742">추가된 새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1742">New cmdlets added:</span></span>
        - <span data-ttu-id="6783d-1743">Add-AzVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="6783d-1743">Add-AzVirtualHubRoute</span></span>
        - <span data-ttu-id="6783d-1744">Add-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="6783d-1744">Add-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="6783d-1745">Get-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="6783d-1745">Get-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="6783d-1746">Remove-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="6783d-1746">Remove-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="6783d-1747">Set-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="6783d-1747">Set-AzVirtualHub</span></span>
* <span data-ttu-id="6783d-1748">VirtualHub의 새로운 속성 Sku 및 VirtualWan의 VirtualWANType에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="6783d-1748">Add support for new properties Sku of VirtualHub and VirtualWANType of VirtualWan</span></span>
    - <span data-ttu-id="6783d-1749">선택적 매개 변수로 다음 cmdlet이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1749">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="6783d-1750">New-AzVirtualHub: 추가된 매개 변수 Sku</span><span class="sxs-lookup"><span data-stu-id="6783d-1750">New-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="6783d-1751">Update-AzVirtualHub: 추가된 매개 변수 Sku</span><span class="sxs-lookup"><span data-stu-id="6783d-1751">Update-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="6783d-1752">New-AzVirtualWan: 추가된 매개 변수 VirtualWANType</span><span class="sxs-lookup"><span data-stu-id="6783d-1752">New-AzVirtualWan : added parameter VirtualWANType</span></span>
        - <span data-ttu-id="6783d-1753">Update-AzVirtualWan: 추가된 매개 변수 VirtualWANType</span><span class="sxs-lookup"><span data-stu-id="6783d-1753">Update-AzVirtualWan : added parameter VirtualWANType</span></span>
* <span data-ttu-id="6783d-1754">HubVnetConnection, VpnConnection 및 ExpressRouteConnection에 대한 EnableInternetSecurity 속성 지원 추가</span><span class="sxs-lookup"><span data-stu-id="6783d-1754">Add support for EnableInternetSecurity property for HubVnetConnection, VpnConnection and ExpressRouteConnection</span></span>
    - <span data-ttu-id="6783d-1755">추가된 새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1755">New cmdlets added:</span></span>
        - <span data-ttu-id="6783d-1756">Update-AzureRmVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="6783d-1756">Update-AzureRmVirtualHubVnetConnection</span></span>
    - <span data-ttu-id="6783d-1757">선택적 매개 변수로 다음 cmdlet이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1757">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="6783d-1758">New-AzureRmVirtualHubVnetConnection: 추가된 매개 변수 EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="6783d-1758">New-AzureRmVirtualHubVnetConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="6783d-1759">New-AzureRmVpnConnection: 추가된 매개 변수 EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="6783d-1759">New-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="6783d-1760">Update-AzureRmVpnConnection: 추가된 매개 변수 EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="6783d-1760">Update-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="6783d-1761">New-AzureRmExpressRouteConnection: 추가된 매개 변수 EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="6783d-1761">New-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="6783d-1762">Set-AzureRmExpressRouteConnection: 추가된 매개 변수 EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="6783d-1762">Set-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
* <span data-ttu-id="6783d-1763">TopLevel WebApplicationFirewall 정책 구성을 위한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="6783d-1763">Add support for Configuring TopLevel WebApplicationFirewall Policy</span></span>
    - <span data-ttu-id="6783d-1764">추가된 새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1764">New cmdlets added:</span></span>
        - <span data-ttu-id="6783d-1765">New-AzApplicationGatewayFirewallPolicySetting</span><span class="sxs-lookup"><span data-stu-id="6783d-1765">New-AzApplicationGatewayFirewallPolicySetting</span></span>
        - <span data-ttu-id="6783d-1766">New-AzApplicationGatewayFirewallPolicyExclusion</span><span class="sxs-lookup"><span data-stu-id="6783d-1766">New-AzApplicationGatewayFirewallPolicyExclusion</span></span>
        - <span data-ttu-id="6783d-1767">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="6783d-1767">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span></span>
        - <span data-ttu-id="6783d-1768">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="6783d-1768">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span></span>
        - <span data-ttu-id="6783d-1769">New-AzApplicationGatewayFirewallPolicyManagedRule</span><span class="sxs-lookup"><span data-stu-id="6783d-1769">New-AzApplicationGatewayFirewallPolicyManagedRule</span></span>
        - <span data-ttu-id="6783d-1770">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="6783d-1770">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span></span>
    - <span data-ttu-id="6783d-1771">선택적 매개 변수로 다음 cmdlet이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1771">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="6783d-1772">New-AzApplicationGatewayFirewallPolicy: 추가된 매개 변수 PolicySetting, ManagedRule</span><span class="sxs-lookup"><span data-stu-id="6783d-1772">New-AzApplicationGatewayFirewallPolicy : added parameter PolicySetting, ManagedRule</span></span>
* <span data-ttu-id="6783d-1773">CustomRule에서 Geo-Match 연산자를 위한 지원 추가됨</span><span class="sxs-lookup"><span data-stu-id="6783d-1773">Added support for Geo-Match operator on CustomRule</span></span>
    - <span data-ttu-id="6783d-1774">FirewallCondition에서 연산자에 GeoMatch 추가됨</span><span class="sxs-lookup"><span data-stu-id="6783d-1774">Added GeoMatch to the operator on the FirewallCondition</span></span>
* <span data-ttu-id="6783d-1775">perListener 및 perSite 방화벽 규칙에 대한 지원 추가됨</span><span class="sxs-lookup"><span data-stu-id="6783d-1775">Added support for perListener and perSite Firewall policy</span></span>
    - <span data-ttu-id="6783d-1776">선택적 매개 변수로 다음 cmdlet이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1776">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="6783d-1777">New-AzApplicationGatewayHttpListener: 추가된 매개 변수 FirewallPolicy, FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="6783d-1777">New-AzApplicationGatewayHttpListener : added parameter FirewallPolicy, FirewallPolicyId</span></span>
        - <span data-ttu-id="6783d-1778">New-AzApplicationGatewayPathRuleConfig: 추가된 매개 변수 FirewallPolicy, FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="6783d-1778">New-AzApplicationGatewayPathRuleConfig : added parameter FirewallPolicy, FirewallPolicyId</span></span>
* <span data-ttu-id="6783d-1779">'PSBastion'에서 이름이 AzureBastionSubnet인 필수 서브넷의 수정은 대소문자를 구분하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1779">Fix required subnet with name AzureBastionSubnet in 'PSBastion' can be case insensitive</span></span>
* <span data-ttu-id="6783d-1780">Azure Firewall을 위한 네트워크 규칙의 대상 FQDN 및 NAT 규칙의 번역된 FQDN 지원</span><span class="sxs-lookup"><span data-stu-id="6783d-1780">Support for Destination FQDNs in Network Rules and Translated FQDN in NAT Rules for Azure Firewall</span></span>
* <span data-ttu-id="6783d-1781">IpGroup의 최상위 리소스 RouteTables에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="6783d-1781">Add support for top level resource RouteTables of IpGroup</span></span>
    - <span data-ttu-id="6783d-1782">추가된 새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1782">New cmdlets added:</span></span>
        - <span data-ttu-id="6783d-1783">New-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="6783d-1783">New-AzIpGroup</span></span>
        - <span data-ttu-id="6783d-1784">Remove-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="6783d-1784">Remove-AzIpGroup</span></span>
        - <span data-ttu-id="6783d-1785">Get-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="6783d-1785">Get-AzIpGroup</span></span>
        - <span data-ttu-id="6783d-1786">Set-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="6783d-1786">Set-AzIpGroup</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="6783d-1787">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="6783d-1787">Az.ServiceFabric</span></span>
* <span data-ttu-id="6783d-1788">Add-AzVmssSecret에서 지원되기 때문에 Add-AzServiceFabricApplicationCertificate cmdlet이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1788">Remove Add-AzServiceFabricApplicationCertificate cmdlet as this scenario is covered by Add-AzVmssSecret.</span></span>

#### <a name="azsql"></a><span data-ttu-id="6783d-1789">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6783d-1789">Az.Sql</span></span>
* <span data-ttu-id="6783d-1790">Managed Instances에서 삭제된 데이터베이스의 복원을 위한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1790">Added support for restore of dropped databases on Managed Instances.</span></span>
* <span data-ttu-id="6783d-1791">이전의 감사 cmdlet 코드가 사용되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1791">Deprecated from code old auditing cmdlets.</span></span>
* <span data-ttu-id="6783d-1792">사용되지 않는 별칭이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1792">Removed deprecated aliases:</span></span>
* <span data-ttu-id="6783d-1793">Get-AzSqlDatabaseIndexRecommendations(대신 Get-AzSqlDatabaseIndexRecommendation 사용)</span><span class="sxs-lookup"><span data-stu-id="6783d-1793">Get-AzSqlDatabaseIndexRecommendations (use Get-AzSqlDatabaseIndexRecommendation instead)</span></span>
* <span data-ttu-id="6783d-1794">Get-AzSqlDatabaseRestorePoints(대신 Get-AzSqlDatabaseRestorePoint 사용)</span><span class="sxs-lookup"><span data-stu-id="6783d-1794">Get-AzSqlDatabaseRestorePoints (use Get-AzSqlDatabaseRestorePoint instead)</span></span>
* <span data-ttu-id="6783d-1795">Get-AzSqlDatabaseSecureConnectionPolicy cmdlet 제거</span><span class="sxs-lookup"><span data-stu-id="6783d-1795">Remove Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="6783d-1796">사용되지 않는 취약성 평가 설정 cmdlet에 대한 별칭 제거</span><span class="sxs-lookup"><span data-stu-id="6783d-1796">Remove aliases for deprecated Vulnerability Assessment Settings cmdlets</span></span>
* <span data-ttu-id="6783d-1797">지능형 위협 탐지 설정 cmdlet 사용 중단</span><span class="sxs-lookup"><span data-stu-id="6783d-1797">Deprecate Advanced Threat Detection Settings cmdlets</span></span>
* <span data-ttu-id="6783d-1798">데이터베이스의 열에 대한 민감도 권장 사항의 사용 여부를 제어하는 cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1798">Adding cmdlets to Disable and enable sensitivity recommendations on columns in a database.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="6783d-1799">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="6783d-1799">Az.Storage</span></span>
* <span data-ttu-id="6783d-1800">스토리지 계정을 만들거나 업데이트할 때 큰 파일 공유 사용 지원</span><span class="sxs-lookup"><span data-stu-id="6783d-1800">Support enable Large File share when create or update Storage account</span></span>
    -  <span data-ttu-id="6783d-1801">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6783d-1801">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="6783d-1802">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6783d-1802">Set-AzStorageAccount</span></span>
* <span data-ttu-id="6783d-1803">파일 핸들을 닫거나/가져올 때, DeletePending 상태의 개체로 인한 오류를 방지하기 위해 입력 경로가 파일 디렉터리인지 또는 파일인지를 확인하는 과정을 건너뜁니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1803">When close/get File handle, skip check the input path is File directory or File, to avoid failure with object in DeletePending status</span></span>
    -  <span data-ttu-id="6783d-1804">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="6783d-1804">Get-AzStorageFileHandle</span></span>
    -  <span data-ttu-id="6783d-1805">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="6783d-1805">Close-AzStorageFileHandle</span></span>

## <a name="280---october-2019"></a><span data-ttu-id="6783d-1806">2.8.0 - 2019년 10월</span><span class="sxs-lookup"><span data-stu-id="6783d-1806">2.8.0 - October 2019</span></span>
### <a name="general"></a><span data-ttu-id="6783d-1807">일반</span><span class="sxs-lookup"><span data-stu-id="6783d-1807">General</span></span>
* <span data-ttu-id="6783d-1808">Az.HealthcareApis 1.0.0 릴리스</span><span class="sxs-lookup"><span data-stu-id="6783d-1808">Az.HealthcareApis 1.0.0 release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="6783d-1809">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6783d-1809">Az.Accounts</span></span>
* <span data-ttu-id="6783d-1810">생성된 모듈에 대한 원격 분석 및 URL 다시 작성이 업데이트되고, Windows 단위 테스트가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1810">Update telemetry and url rewriting for generated modules, fix windows unit tests.</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="6783d-1811">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="6783d-1811">Az.ApiManagement</span></span>
* <span data-ttu-id="6783d-1812">**Set-AzApiManagementApi** - API 업데이트 지원이 ApiVersionSet에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1812">**Set-AzApiManagementApi** - Added support for Updating Api into ApiVersionSet</span></span>
    - <span data-ttu-id="6783d-1813">문제 https://github.com/Azure/azure-powershell/issues/10068 수정</span><span class="sxs-lookup"><span data-stu-id="6783d-1813">Fix for issue https://github.com/Azure/azure-powershell/issues/10068</span></span>

#### <a name="azautomation"></a><span data-ttu-id="6783d-1814">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="6783d-1814">Az.Automation</span></span>
* <span data-ttu-id="6783d-1815">Linux 다시 부팅 설정 매개 변수에 대한 New-AzureAutomationSoftwareUpdateConfiguration cmdlet이 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1815">Fixed New-AzureAutomationSoftwareUpdateConfiguration cmdlet for Linux reboot setting parameter.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="6783d-1816">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="6783d-1816">Az.Batch</span></span>
* <span data-ttu-id="6783d-1817">**Get-AzBatchNodeAgentSku** 가 더 이상 사용되지 않으며, 2.0.0 버전의 **Get-AzBatchSupportImage** 로 대체되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1817">**Get-AzBatchNodeAgentSku** is deprecated and will be replaced by **Get-AzBatchSupportImage** in version 2.0.0.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6783d-1818">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6783d-1818">Az.Compute</span></span>
* <span data-ttu-id="6783d-1819">Priority, EvictionPolicy 및 MaxPrice 매개 변수가 New-AzVM 및 New-AzVmss cmdlet에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1819">Add Priority, EvictionPolicy, and MaxPrice parameters to New-AzVM and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="6783d-1820">Add-AzVMAdditionalUnattendContent 및 Add-AzVMSshPublicKey cmdlet에 대한 경고 메시지와 도움말 문서가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1820">Fix warning message and help document for Add-AzVMAdditionalUnattendContent and Add-AzVMSshPublicKey cmdlets</span></span>
* <span data-ttu-id="6783d-1821">Set-AzVMDiskEncryptionExtension의 관리 디스크가 있는 Linux VM에 대한 -skipVmBackup 예외가 해결되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1821">Fix -skipVmBackup exception for Linux VMs with managed disks for Set-AzVMDiskEncryptionExtension.</span></span>
* <span data-ttu-id="6783d-1822">Set-AzVMDiskEncryptionExtension의 두 가지 패스 시나리오에서 발생하는 암호화 설정 업데이트의 버그가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1822">Fix bug in update encryption settings in Set-AzVMDiskEncryptionExtension, two pass scenario.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="6783d-1823">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="6783d-1823">Az.DataFactory</span></span>
* <span data-ttu-id="6783d-1824">ADF V2 데이터 흐름에 대한 CRUD 명령으로 Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow 및 Get-AzDataFactoryV2DataFlow가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1824">Adding CRUD commands for ADF V2 data flow: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow, and Get-AzDataFactoryV2DataFlow.</span></span>
* <span data-ttu-id="6783d-1825">ADF V2 데이터 흐름 디버그 세션에 대한 작업 명령으로 Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand 및 Stop-AzDataFactoryV2DataFlowDebugSession이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1825">Adding action commands for ADF V2 data flow debug Session: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand and Stop-AzDataFactoryV2DataFlowDebugSession.</span></span>
* <span data-ttu-id="6783d-1826">ADF .Net SDK 버전이 4.2.0으로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1826">Update ADF .Net SDK version to 4.2.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="6783d-1827">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="6783d-1827">Az.DataLakeStore</span></span>
* <span data-ttu-id="6783d-1828">도메인 없이 '-'가 있는 계정을 전달할 수 있도록 계정 유효성 검사가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1828">Fix account validation so that accounts with '-' can be passed without domain</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="6783d-1829">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="6783d-1829">Az.HealthcareApis</span></span>
* <span data-ttu-id="6783d-1830">PowerShell 버전이 1.0.0으로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1830">Updated the powershell version to 1.0.0</span></span>
* <span data-ttu-id="6783d-1831">SDK 버전이 1.0.2로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1831">Updated the SDK version to 1.0.2</span></span>
* <span data-ttu-id="6783d-1832">새 SDK 버전을 참조하도록 테스트가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1832">Update in tests to refer to new SDK version</span></span>
* <span data-ttu-id="6783d-1833">출력이 중첩 구조에서 평면화 구조로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1833">Updated the output structure from nested to flattened.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="6783d-1834">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="6783d-1834">Az.IotHub</span></span>
* <span data-ttu-id="6783d-1835">새 라우팅 원본 추가: DigitalTwinChangeEvents</span><span class="sxs-lookup"><span data-stu-id="6783d-1835">Add new routing source: DigitalTwinChangeEvents</span></span>
* <span data-ttu-id="6783d-1836">사소한 버그 수정: Get-AzIothub에서 subscriptionId를 반환하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1836">Minor bug fix: Get-AzIothub not returning subscriptionId</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="6783d-1837">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="6783d-1837">Az.Monitor</span></span>
* <span data-ttu-id="6783d-1838">작업 그룹에 대한 새 작업 그룹 수신기로 -ItsmReceiver, -VoiceReceiver, -ArmRoleReceiver, -AzureFunctionReceiver, -LogicAppReceiver, -AutomationRunbookReceiver, -AzureAppPushReceiver가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1838">New action group receivers added for action group   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span></span>
* <span data-ttu-id="6783d-1839">수신기에 사용하도록 설정된 일반 경고 스키마가 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1839">Use common alert schema enabled for the receivers.</span></span> <span data-ttu-id="6783d-1840">SMS, Azure 앱 푸시, ITSM 및 음성 수신기에는 적용되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1840">This is not applicable for SMS, Azure App push , ITSM and Voice recievers</span></span>
* <span data-ttu-id="6783d-1841">웹후크에서 이제 Azure Active Directory 인증을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1841">Webhooks now supports Azure active directory authentication .</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6783d-1842">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6783d-1842">Az.Network</span></span>
* <span data-ttu-id="6783d-1843">서비스 엔드포인트 정책에 사용할 수 있는 별칭을 가져오기 위해 호출할 수 있는 새 Get-AzAvailableServiceAlias cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1843">Add new cmdlet Get-AzAvailableServiceAlias which can be called to get the aliases that can be used for Service Endpoint Policies.</span></span>
* <span data-ttu-id="6783d-1844">트래픽 선택기를 Virtual Network 게이트웨이 연결에 추가할 수 있는 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1844">Added support for the adding traffic selectors to Virtual Network Gateway Connections</span></span>
    - <span data-ttu-id="6783d-1845">추가된 새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1845">New cmdlets added:</span></span>
        - <span data-ttu-id="6783d-1846">New-AzureRmTrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="6783d-1846">New-AzureRmTrafficSelectorPolicy</span></span>
    - <span data-ttu-id="6783d-1847">cmdlet이 선택적인 -TrafficSelectorPolicies, -New-AzureRmVirtualNetworkGatewayConnection, -Set-AzureRmVirtualNetworkGatewayConnection 매개 변수로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1847">Cmdlets updated with optional parameter -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="6783d-1848">ESP 및 AH 프로토콜 지원이 네트워크 보안 규칙 구성에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1848">Add support for ESP and AH protocols in network security rule configurations</span></span>
    - <span data-ttu-id="6783d-1849">다음 Cmdlet이 업데이트 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1849">Updated cmdlets:</span></span>
        - <span data-ttu-id="6783d-1850">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="6783d-1850">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="6783d-1851">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="6783d-1851">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="6783d-1852">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="6783d-1852">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="6783d-1853">Cortex cmdlet의 예외 처리가 향상되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1853">Improve handling of exceptions in Cortex cmdlets</span></span>
* <span data-ttu-id="6783d-1854">새 VirtualNetworkGateways 세대 및 SKU</span><span class="sxs-lookup"><span data-stu-id="6783d-1854">New Generations and SKUs for VirtualNetworkGateways</span></span>
  - <span data-ttu-id="6783d-1855">새 VirtualNetworkGateways 세대가 도입되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1855">Introduce new Generations for VirtualNetworkGateways.</span></span>
  - <span data-ttu-id="6783d-1856">높은 처리량의 새 VirtualNetworkGateways SKU가 도입되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1856">Introduce new high throughput SKUs for VirtualNetworkGateways.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="6783d-1857">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="6783d-1857">Az.RedisCache</span></span>
* <span data-ttu-id="6783d-1858">'-Size' 매개 변수에 대한 누락 값을 포함하도록 'Set-AzRedisCache' 참조 설명서가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1858">Updated 'Set-AzRedisCache' reference documentation to include missing values for '-Size' parameter</span></span>

#### <a name="azsql"></a><span data-ttu-id="6783d-1859">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6783d-1859">Az.Sql</span></span>
* <span data-ttu-id="6783d-1860">Managed Instance에서 Active Directory 관리자를 설정할 수 있는 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1860">Add support for setting Active Directory Administrator on Managed Instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="6783d-1861">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="6783d-1861">Az.Storage</span></span>
* <span data-ttu-id="6783d-1862">스토리지 클라이언트 라이브러리가 11.1.0으로 업그레이드되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1862">Upgrade Storage Client Library to 11.1.0</span></span>
* <span data-ttu-id="6783d-1863">관리 평면 API를 사용하여 컨테이너를 나열하면 NextPageLink를 통해 나열됩니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1863">List containers with Management plane API, will list with NextPageLink</span></span>
    -  <span data-ttu-id="6783d-1864">Get-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="6783d-1864">Get-AzRmStorageContainer</span></span>
* <span data-ttu-id="6783d-1865">구독에서 스토리지 계정을 나열하면 NextPageLink를 통해 나열됩니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1865">List Storage accounts from subscription, will list with NextPageLink</span></span>
    -  <span data-ttu-id="6783d-1866">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6783d-1866">Get-AzStorageAccount</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="6783d-1867">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="6783d-1867">Az.StorageSync</span></span>
* <span data-ttu-id="6783d-1868">Reset-AzStorageSyncServerCertificate의 9810 문제가 해결되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1868">Fix Issue 9810 in Reset-AzStorageSyncServerCertificate.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="6783d-1869">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="6783d-1869">Az.Websites</span></span>
* <span data-ttu-id="6783d-1870">앱의 ASP를 업데이트하는 Set-AzWebApp이 실패했습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1870">Set-AzWebApp updating ASP of an app was failing</span></span>

## <a name="270---september-2019"></a><span data-ttu-id="6783d-1871">2.7.0 - 2019년 9월</span><span class="sxs-lookup"><span data-stu-id="6783d-1871">2.7.0 - September 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="6783d-1872">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="6783d-1872">Az.ApiManagement</span></span>
* <span data-ttu-id="6783d-1873">'Set-AzApiManagementPolicy' 참조 설명서에서 '-Format' 매개 변수 설명이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1873">Update '-Format' parameter description in 'Set-AzApiManagementPolicy' reference documentation</span></span>
* <span data-ttu-id="6783d-1874">참조 설명서에서 사용되지 않는 cmdlet 'Update-AzApiManagementDeployment'의 참조를 제거했습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1874">Removed references of deprecated cmdlet 'Update-AzApiManagementDeployment' from reference documentation.</span></span> <span data-ttu-id="6783d-1875">그 대신 'Set-AzApiManagement'를 사용하세요.</span><span class="sxs-lookup"><span data-stu-id="6783d-1875">Use 'Set-AzApiManagement' instead.</span></span>

#### <a name="azautomation"></a><span data-ttu-id="6783d-1876">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="6783d-1876">Az.Automation</span></span>
* <span data-ttu-id="6783d-1877">'Register-AzAutomationDscNode'에 대한 참조 설명서의 예제 오타가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1877">Fixed example typo in reference documentation for 'Register-AzAutomationDscNode'</span></span>
* <span data-ttu-id="6783d-1878">Register-AzAutomationDSCNode에 OS 제한에 대한 설명이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1878">Added clarification on OS restriction to Register-AzAutomationDSCNode</span></span>
* <span data-ttu-id="6783d-1879">-Wait 옵션에 대한 Start-AzAutomationRunbook cmdlet Null 참조 예외가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1879">Fixed Start-AzAutomationRunbook cmdlet Null reference exception for -Wait option.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6783d-1880">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6783d-1880">Az.Compute</span></span>
* <span data-ttu-id="6783d-1881">New-AzDiskConfig에 UploadSizeInBytes 매개 변수가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1881">Add UploadSizeInBytes parameter tp New-AzDiskConfig</span></span>
* <span data-ttu-id="6783d-1882">New-AzSnapshotConfig에 증분 매개 변수가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1882">Add Incremental parameter to New-AzSnapshotConfig</span></span>
* <span data-ttu-id="6783d-1883">다음과 같은 낮은 우선 순위의 가상 머신 기능이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1883">Add a low priority virtual machine feature:</span></span>
    - <span data-ttu-id="6783d-1884">MaxPrice, EvictionPolicy 및 Priority 매개 변수가 New-AzVMConfig에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1884">MaxPrice, EvictionPolicy and Priority parameters are added to New-AzVMConfig.</span></span>
    - <span data-ttu-id="6783d-1885">MaxPrice 매개 변수는 New-AzVmssConfig, Update-AzVM 및 Update-AzVmss cmdlet에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1885">MaxPrice parameter is added to New-AzVmssConfig, Update-AzVM and Update-AzVmss cmdlets.</span></span>
* <span data-ttu-id="6783d-1886">구독의 모든 가용성 세트를 나열할 때 발생하는 Get-AzAvailabilitySet cmdlet에 대한 VM 참조 이슈가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1886">Fix VM reference issue for Get-AzAvailabilitySet cmdlet when it lists all availability sets in the subscription.</span></span>
* <span data-ttu-id="6783d-1887">Get-AzRemoteDesktopFile에 대한 null 예외가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1887">Fix the null exception for Get-AzRemoteDesktopFile.</span></span>
* <span data-ttu-id="6783d-1888">종료 상대 위치에 대한 VHD 검색 메서드가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1888">Fix VHD Seek method for end-relative position.</span></span>
* <span data-ttu-id="6783d-1889">New-AzVM 및 Update-AzVM에 대한 UltraSSD 이슈가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1889">Fix UltraSSD issue for New-AzVM and Update-AzVM.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="6783d-1890">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="6783d-1890">Az.DataFactory</span></span>
* <span data-ttu-id="6783d-1891">ADF V2에 대한 3가지 새 명령 Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription 및 Get-AzDataFactoryV2TriggerSubscriptionStatus가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1891">Adding 3 new commands for ADF V2 - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription, and Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>
* <span data-ttu-id="6783d-1892">ADF .Net SDK 버전이 4.1.3으로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1892">Updated ADF .Net SDK version to 4.1.3</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="6783d-1893">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="6783d-1893">Az.HDInsight</span></span>
* <span data-ttu-id="6783d-1894">호출 주요 변경 내용</span><span class="sxs-lookup"><span data-stu-id="6783d-1894">Call out breaking changes</span></span>

#### <a name="aziothub"></a><span data-ttu-id="6783d-1895">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="6783d-1895">Az.IotHub</span></span>
* <span data-ttu-id="6783d-1896">지역 쌍 재해 복구 지역에 IotHub에 대한 장애 조치(failover) 호출 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1896">Add support to invoke failover for an IotHub to the geo-paired disaster recovery region.</span></span>
* <span data-ttu-id="6783d-1897">IotHub에 대한 메시지 보강 관리 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1897">Add support to manage message enrichment for an IotHub.</span></span> <span data-ttu-id="6783d-1898">새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1898">New cmdlets are:</span></span>
    - <span data-ttu-id="6783d-1899">Add-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="6783d-1899">Add-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="6783d-1900">Get-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="6783d-1900">Get-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="6783d-1901">Remove-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="6783d-1901">Remove-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="6783d-1902">Set-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="6783d-1902">Set-AzIotHubMessageEnrichment</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="6783d-1903">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="6783d-1903">Az.Monitor</span></span>
* <span data-ttu-id="6783d-1904">최신 모니터링 SDK, 즉, 0.24.1-preview를 가리킵니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1904">Pointing to the most recent Monitor SDK, i.e. 0.24.1-preview</span></span>
   - <span data-ttu-id="6783d-1905">메트릭 cmdlet에 줄 바꿈하지 않는 변경 내용을 추가합니다. 즉, 단위 열거형은 여러 새 값을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1905">Adds non-braking changes to the Metrics cmdlets, i.e. the Unit enumeration supports several new values.</span></span> <span data-ttu-id="6783d-1906">이러한 cmdlet은 읽기 전용이므로 cmdlet 입력이 변경되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1906">These are read-only cmdlets, so there would be no change in the input of the cmdlets.</span></span>
   - <span data-ttu-id="6783d-1907">이제 **ActionGroups** 요청의 api 버전은 **2019-06-01** 이고, 이전에는 **2018-03-01** 였습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1907">The api-version of the **ActionGroups** requests is now **2019-06-01** , before it was **2018-03-01** .</span></span> <span data-ttu-id="6783d-1908">시나리오 테스트가 이 변경 내용에 맞게 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1908">The scenario tests have been updated to accommodate for this change.</span></span>
   - <span data-ttu-id="6783d-1909">**EmailReceiver** 및 **WebhookReceiver** 클래스에 대한 생성자가 새 필수 인수, 즉, **useCommonAlertSchema** 라는 부울 값을 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1909">The constructors for the classes **EmailReceiver** and **WebhookReceiver** added one new mandatory argument, i.e. a Boolean value called **useCommonAlertSchema** .</span></span> <span data-ttu-id="6783d-1910">현재 이 값은 cmdlet의 주요 변경 사항을 숨기도록 **false** 로 고정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1910">Currently, the value is fixed to **false** to hide this breaking change from the cmdlets.</span></span> <span data-ttu-id="6783d-1911">**참고** : 이 변경 사항은 경고 팀에서 유효성을 검사해야 하는 임시 변경 내용입니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1911">**NOTE** : this is a temporary change that must be validated by the Alerts team.</span></span>
   - <span data-ttu-id="6783d-1912">이전 SDK에서 변경된 **Source** 클래스( **ScheduledQueryRuleSource** 클래스와 관련됨)의 생성자에 대한 인수 순서입니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1912">The order of the arguments for the constructor of the class **Source** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="6783d-1913">이번 변화로 인해 두 개의 단위 테스트를 수정해야 했습니다. 즉, 두 단위 테스트가 컴파일되었지만 테스트를 통과하지 못했습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1913">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
   - <span data-ttu-id="6783d-1914">이전 SDK에서 변경된 **AlertingAction** 클래스( **ScheduledQueryRuleSource** 클래스와 관련됨)의 생성자에 대한 인수 순서입니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1914">The order of the arguments for the constructor of the class **AlertingAction** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="6783d-1915">이번 변화로 인해 두 개의 단위 테스트를 수정해야 했습니다. 즉, 두 단위 테스트가 컴파일되었지만 테스트를 통과하지 못했습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1915">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
* <span data-ttu-id="6783d-1916">메트릭 경고 V2에 대한 동적 임계값 기준 지원</span><span class="sxs-lookup"><span data-stu-id="6783d-1916">Support Dynamic Threshold criteria for metric alert V2</span></span>
    - <span data-ttu-id="6783d-1917">AzMetricAlertRuleV2Criteria: 이제 동적 임계값 조건도 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1917">New-AzMetricAlertRuleV2Criteria: now creats dynamic threshold criteria also</span></span>
    - <span data-ttu-id="6783d-1918">Add-AzMetricAlertRuleV2: 이제 동적 임계값 조건도 수락합니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1918">Add-AzMetricAlertRuleV2: now accept dynamic threshold criteria also</span></span>
* <span data-ttu-id="6783d-1919">SQR(예약된 쿼리 규칙)의 향상된 기능</span><span class="sxs-lookup"><span data-stu-id="6783d-1919">Improvements in Scheduled Query Rule cmdlets (SQR)</span></span>
 - <span data-ttu-id="6783d-1920">Cmdlet이 'Location' 매개 변수를 두 가지 형식(eastus 같은 위치 또는 미국 동부 같은 위치 표시 이름)으로 모두 허용합니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1920">Cmdlets will accept 'Location' paramater in both formats, either the location (e.g. eastus) or the location display name (e.g. East US)</span></span>
 - <span data-ttu-id="6783d-1921">도움말 파일에 적절하게 표시된 'Enabled' 매개 변수</span><span class="sxs-lookup"><span data-stu-id="6783d-1921">Illustrated 'Enabled' parameter in help files properly</span></span>
 - <span data-ttu-id="6783d-1922">선택적 매개 변수 'ActionGroup'에 대한 예제가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1922">Added examples for 'ActionGroup' optional parameter</span></span>
 - <span data-ttu-id="6783d-1923">도움말 파일이 전체적으로 개선되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1923">Overall improved help files</span></span>
* <span data-ttu-id="6783d-1924">'Set-AzActionRule'의 범위 유형 결정 버그를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1924">Fix bug in determining scope type for 'Set-AzActionRule'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6783d-1925">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6783d-1925">Az.Network</span></span>
* <span data-ttu-id="6783d-1926">'New-AzApplicationGateway' 참조 설명서의 잘못된 예제가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1926">Fix incorrect example in 'New-AzApplicationGateway' reference documentation</span></span>
* <span data-ttu-id="6783d-1927">'Get-AzNetworkWatcherPacketCapture' 참조 설명서에 패킷 캡처를 위한 모든 속성 검색과 관련된 메모가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1927">Add note in 'Get-AzNetworkWatcherPacketCapture' reference documentation about retrieving all properties for a packet capture</span></span>
* <span data-ttu-id="6783d-1928">NIC를 올바르게 열거하도록 'Test-AzNetworkWatcherIPFlow' 참조 설명서의 예제가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1928">Fixed example in 'Test-AzNetworkWatcherIPFlow' reference documentation to correctly enumerate NICs</span></span>
* <span data-ttu-id="6783d-1929">추가 세부 정보가 있는 경우 추가 세부 정보를 표시하도록 클라우드 예외 구문 분석이 향상되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1929">Improved cloud exception parsing to display additional details if they are present</span></span>
* <span data-ttu-id="6783d-1930">더 많은 형식의 SDK 예외를 처리하도록 클라우드 예외 구문 분석이 향상되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1930">Improved cloud exception parsing to handle additional type of SDK exception</span></span>
* <span data-ttu-id="6783d-1931">보안 규칙 모델의 잘못된 매핑이 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1931">Fixed incorrect mapping of Security Rule models</span></span>
* <span data-ttu-id="6783d-1932">네트워크 인터페이스에 개인 IP 기능을 위한 속성이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1932">Added properties to network interface for private ip feature</span></span>
    - <span data-ttu-id="6783d-1933">PSNetworkInterface에 'PrivateEndpoint' 속성이 PSResourceId 형식으로 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1933">Added property 'PrivateEndpoint' as type of PSResourceId to PSNetworkInterface</span></span>
    - <span data-ttu-id="6783d-1934">PSNetworkInterfaceIPConfiguration에 'PrivateLinkConnectionProperties' 속성이 PSIpConfigurationConnectivityInformation 형식으로 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1934">Added property 'PrivateLinkConnectionProperties' as type of PSIpConfigurationConnectivityInformation to PSNetworkInterfaceIPConfiguration</span></span>
    - <span data-ttu-id="6783d-1935">새 모델 클래스 PSIpConfigurationConnectivityInformation이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1935">Added new model class PSIpConfigurationConnectivityInformation</span></span>
* <span data-ttu-id="6783d-1936">Azure Firewall 리소스에 대한 새 ApplicationRuleProtocolType 'mssql'이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1936">Added new ApplicationRuleProtocolType 'mssql' for Azure Firewall resource</span></span>
* <span data-ttu-id="6783d-1937">Virtual WAN에서 멀티 링크를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1937">MultiLink support in Virtual WAN</span></span>
    - <span data-ttu-id="6783d-1938">새로운 cmdlet</span><span class="sxs-lookup"><span data-stu-id="6783d-1938">New cmdlets</span></span>
        - <span data-ttu-id="6783d-1939">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="6783d-1939">New-AzVpnSiteLink</span></span>
        - <span data-ttu-id="6783d-1940">New-AzVpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="6783d-1940">New-AzVpnSiteLinkConnection</span></span>
    - <span data-ttu-id="6783d-1941">업데이트된 cmdlet:</span><span class="sxs-lookup"><span data-stu-id="6783d-1941">Updated cmdlet:</span></span>
        - <span data-ttu-id="6783d-1942">New-VpnSite</span><span class="sxs-lookup"><span data-stu-id="6783d-1942">New-VpnSite</span></span>
        - <span data-ttu-id="6783d-1943">Update-VpnSite</span><span class="sxs-lookup"><span data-stu-id="6783d-1943">Update-VpnSite</span></span>
        - <span data-ttu-id="6783d-1944">New-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="6783d-1944">New-VpnConnection</span></span>
        - <span data-ttu-id="6783d-1945">Update-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="6783d-1945">Update-VpnConnection</span></span>
* <span data-ttu-id="6783d-1946">AzureRM cmdlet 대신 Az cmdlet을 사용하도록 일부 PowerShell 예제의 문서가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1946">Fixed documents for some PowerShell examples to use Az cmdlets instead of AzureRM cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="6783d-1947">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="6783d-1947">Az.RecoveryServices</span></span>
* <span data-ttu-id="6783d-1948">AzureVMpolicy 개체가 ProtectedItemsCount 특성으로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1948">Update AzureVMpolicy Object with ProtectedItemsCount Attribute</span></span>
* <span data-ttu-id="6783d-1949">VM 정책 및 원래 스토리지 계정 복원에 대한 테스트가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1949">Added Tests for VM policy and Original Storage Account Restore</span></span>

#### <a name="azresources"></a><span data-ttu-id="6783d-1950">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6783d-1950">Az.Resources</span></span>
* <span data-ttu-id="6783d-1951">매개 변수 범위 없이 AzRoleAssignment를 호출할 수 없는 버그가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1951">Fix bug where New-AzRoleAssignment could not be called without parameter Scope.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="6783d-1952">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="6783d-1952">Az.ServiceFabric</span></span>
* <span data-ttu-id="6783d-1953">'AzServiceFabricReliability' 참조 설명서에 대한 예제의 오타가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1953">Fixed typo in example for 'Update-AzServiceFabricReliability' reference documentation</span></span>
* <span data-ttu-id="6783d-1954">애플리케이션 및 서비스를 관리하는 다음과 같은 새 cmdlet이 추가됩니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1954">Adding new cmdlets to manage appliaction and services:</span></span>
    - <span data-ttu-id="6783d-1955">New-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="6783d-1955">New-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="6783d-1956">New-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="6783d-1956">New-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="6783d-1957">New-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="6783d-1957">New-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="6783d-1958">New-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="6783d-1958">New-AzServiceFabricService</span></span>
    - <span data-ttu-id="6783d-1959">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="6783d-1959">Update-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="6783d-1960">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="6783d-1960">Get-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="6783d-1961">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="6783d-1961">Get-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="6783d-1962">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="6783d-1962">Get-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="6783d-1963">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="6783d-1963">Get-AzServiceFabricService</span></span>
    - <span data-ttu-id="6783d-1964">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="6783d-1964">Remove-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="6783d-1965">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="6783d-1965">Remove-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="6783d-1966">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="6783d-1966">Remove-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="6783d-1967">Remove-AzServiceFabricServic</span><span class="sxs-lookup"><span data-stu-id="6783d-1967">Remove-AzServiceFabricServic</span></span>
* <span data-ttu-id="6783d-1968">Service Fabric SDK가 Service Fabric 리소스 공급자 api 버전 2019-03-01을 사용하는 1.2.0 버전으로 업그레이드되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1968">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2019-03-01.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="6783d-1969">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="6783d-1969">Az.SignalR</span></span>
* <span data-ttu-id="6783d-1970">Update, Restart, CheckNameAvailability, GetUsage Cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1970">Add Update, Restart, CheckNameAvailability, GetUsage Cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="6783d-1971">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6783d-1971">Az.Sql</span></span>
* <span data-ttu-id="6783d-1972">'Get-AzSqlElasticPool'에 대한 참조 설명서의 예제가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1972">Update example in reference documentation for 'Get-AzSqlElasticPool'</span></span>
* <span data-ttu-id="6783d-1973">탄력적 풀을 만드는 vCore 예제가 추가되었습니다(AzSqlElasticPool).</span><span class="sxs-lookup"><span data-stu-id="6783d-1973">Added vCore example to creating an elastic pool (New-AzSqlElasticPool).</span></span>
* <span data-ttu-id="6783d-1974">Set-AzSqlServerAdvancedThreatProtectionPolicy 및 Set-AzSqlDatabaseAdvancedThreatProtectionPolicy에서 EmailAddresses가 비어 있는 경우 EmailAddresses의 유효성을 검사하고 EmailAdmins가 false가 아닌지 확인하는 기능이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1974">Remove the validation of EmailAddresses and the check that EmailAdmins is not false in case EmailAddresses is empty in Set-AzSqlServerAdvancedThreatProtectionPolicy and Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="6783d-1975">감사 범주를 사용하는 여러 진단 설정이 있는 경우 서버/데이터베이스 감사 설정을 제거하도록 설정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1975">Enabled removal of server/database auditing settings when multiple diagnostic settings that enable audit category exist.</span></span>
* <span data-ttu-id="6783d-1976">여러 Sql 취약성 평가 cmdlet에서 이메일 주소 유효성 검사가 수정되었습니다(Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting 및 Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span><span class="sxs-lookup"><span data-stu-id="6783d-1976">Fix email addresses validation in multiple Sql Vulnerability Assessment cmdlets (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting and Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span></span>

#### <a name="azstorage"></a><span data-ttu-id="6783d-1977">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="6783d-1977">Az.Storage</span></span>
* <span data-ttu-id="6783d-1978">'Get-AzStorageAccountKey'에 대한 참조 설명서의 예제가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1978">Updated example in reference documentation for 'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="6783d-1979">Azure 파일 업로드/다운에서, 원본 파일 SMB 속성(파일 특성, 파일 생성 시간, 파일을 마지막으로 쓴 시간)을 대상 파일에 보존하는 기능이 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1979">In upload/Downalod Azure File,support perserve the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the destination file</span></span>
    -  <span data-ttu-id="6783d-1980">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="6783d-1980">Set-AzStorageFileContent</span></span>
    -  <span data-ttu-id="6783d-1981">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="6783d-1981">Get-AzStorageFileContent</span></span>
* <span data-ttu-id="6783d-1982">컨테이너가 사용되는 ImmutabilityPolicy에서 properties/metadate fail을 사용하여 블록 Blob 업로드가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1982">Fix Upload block blob with properties/metadate fail on container enabled ImmutabilityPolicy.</span></span>
    -  <span data-ttu-id="6783d-1983">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="6783d-1983">Set-AzStorageBlobContent</span></span>
* <span data-ttu-id="6783d-1984">관리 평면 API를 사용하여 Azure 파일 공유 관리를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1984">Support manage Azure File shares with Management plane API</span></span>
    -  <span data-ttu-id="6783d-1985">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="6783d-1985">New-AzRmStorageShare</span></span>
    -  <span data-ttu-id="6783d-1986">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="6783d-1986">Get-AzRmStorageShare</span></span>
    -  <span data-ttu-id="6783d-1987">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="6783d-1987">Update-AzRmStorageShare</span></span>
    -  <span data-ttu-id="6783d-1988">Remove-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="6783d-1988">Remove-AzRmStorageShare</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="6783d-1989">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="6783d-1989">Az.Websites</span></span>
* <span data-ttu-id="6783d-1990">앱을 새 ASP로 마이그레이션할 때 웹앱 태그가 삭제되는 이슈가 해결되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1990">Fixing issue where webapp Tags were getting deleted when migrating App to new ASPwhere webapp Tags were getting deleted when migrating App to new ASP</span></span>
* <span data-ttu-id="6783d-1991">Linux와 Windows에서 모두 작동하도록 Publish-AzureWebapp이 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1991">Fixing the Publish-AzureWebapp to work across Linux and windows</span></span>
* <span data-ttu-id="6783d-1992">'Get-AzWebAppPublishingProfile' 참조 설명서의 예제가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-1992">Update example in 'Get-AzWebAppPublishingProfile' reference documentation</span></span>

## <a name="260---august-2019"></a><span data-ttu-id="6783d-1993">2.6.0 - 2019년 8월</span><span class="sxs-lookup"><span data-stu-id="6783d-1993">2.6.0 - August 2019</span></span>
#### <a name="general"></a><span data-ttu-id="6783d-1994">일반</span><span class="sxs-lookup"><span data-stu-id="6783d-1994">General</span></span>
* <span data-ttu-id="6783d-1995">여러 모듈에서 기타 오타가 수정됨</span><span class="sxs-lookup"><span data-stu-id="6783d-1995">Fixed miscellaneous typos across numerous modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="6783d-1996">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6783d-1996">Az.Accounts</span></span>
* <span data-ttu-id="6783d-1997">Azure Functions 인증에서 사용자가 할당한 MSI가 지원됨(# 9479)</span><span class="sxs-lookup"><span data-stu-id="6783d-1997">Support user-assigned MSI in Azure Functiosn Authentication (#9479)</span></span>

#### <a name="azaks"></a><span data-ttu-id="6783d-1998">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="6783d-1998">Az.Aks</span></span>
* <span data-ttu-id="6783d-1999">'Get-AzAks' 출력 관련 문제가 해결됨</span><span class="sxs-lookup"><span data-stu-id="6783d-1999">Fix issue with output for 'Get-AzAks'</span></span>
    * <span data-ttu-id="6783d-2000">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/9847 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="6783d-2000">More information here: https://github.com/Azure/azure-powershell/issues/9847</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="6783d-2001">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="6783d-2001">Az.ApiManagement</span></span>
* <span data-ttu-id="6783d-2002">문제 https://github.com/Azure/azure-powershell/issues/9351 수정</span><span class="sxs-lookup"><span data-stu-id="6783d-2002">Fix for issue https://github.com/Azure/azure-powershell/issues/9351</span></span>
    - <span data-ttu-id="6783d-2003">productId, apiId, groupId 및 userId에 대한 제한을 적용하지 않는 .Net NuGet 버전이 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="6783d-2003">Update .net nuget version, which does not enforce restrictions on productId, apiId, groupId and userId</span></span>
* <span data-ttu-id="6783d-2004">**Get-AzApiManagementProduct** - API를 사용하는 제품에 대한 쿼리 지원이 추가됨</span><span class="sxs-lookup"><span data-stu-id="6783d-2004">**Get-AzApiManagementProduct** - Added support for querying products using Api.</span></span>
  https://github.com/Azure/azure-powershell/issues/9482
* <span data-ttu-id="6783d-2005">**New-AzApiManagementApiRevision** - 새 API 수정(https://github.com/Azure/azure-powershell/issues/9752 )을 만들 때 ApiRevisionDescription이 설정되지 않은 문제가 해결됨</span><span class="sxs-lookup"><span data-stu-id="6783d-2005">**New-AzApiManagementApiRevision** - Fix for issue where ApiRevisionDescription was not being set when creating new api revision https://github.com/Azure/azure-powershell/issues/9752</span></span>
* <span data-ttu-id="6783d-2006">'PsApiManagementOAuth2AuthrozationServer' 모델의 오타가 'PsApiManagementOAuth2AuthorizationServer'로 수정됨</span><span class="sxs-lookup"><span data-stu-id="6783d-2006">Fixed typo in model 'PsApiManagementOAuth2AuthrozationServer' to 'PsApiManagementOAuth2AuthorizationServer'</span></span>

#### <a name="azbatch"></a><span data-ttu-id="6783d-2007">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="6783d-2007">Az.Batch</span></span>
* <span data-ttu-id="6783d-2008">도움말 메시지 및 설명서에서 Windows를 대문자로 시작하도록 오타가 수정됨</span><span class="sxs-lookup"><span data-stu-id="6783d-2008">Fixed typo in help message and documentation to capitalize Windows</span></span>

#### <a name="azcdn"></a><span data-ttu-id="6783d-2009">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="6783d-2009">Az.Cdn</span></span>
* <span data-ttu-id="6783d-2010">CDN 모듈 변환 도우미의 오타가 수정됨</span><span class="sxs-lookup"><span data-stu-id="6783d-2010">Fixed a typo in CDN module conversion helper</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6783d-2011">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6783d-2011">Az.Compute</span></span>
* <span data-ttu-id="6783d-2012">VmssId가 New-AzVMConfig cmdlet에 추가됨</span><span class="sxs-lookup"><span data-stu-id="6783d-2012">Add VmssId to New-AzVMConfig cmdlet</span></span>
* <span data-ttu-id="6783d-2013">TerminateScheduledEvents 및 TerminateScheduledEventNotBeforeTimeoutInMinutes 매개 변수가 New-AzVmssConfig 및 Update-AzVmss에 추가됨</span><span class="sxs-lookup"><span data-stu-id="6783d-2013">Add TerminateScheduledEvents and TerminateScheduledEventNotBeforeTimeoutInMinutes parameters to New-AzVmssConfig and Update-AzVmss</span></span>
* <span data-ttu-id="6783d-2014">HyperVGeneration 속성이 VM 이미지 개체에 추가됨</span><span class="sxs-lookup"><span data-stu-id="6783d-2014">Add HyperVGeneration property to VM image object</span></span>
* <span data-ttu-id="6783d-2015">Host 및 HostGroup 기능이 추가됨</span><span class="sxs-lookup"><span data-stu-id="6783d-2015">Add Host and HostGroup features</span></span>
    - <span data-ttu-id="6783d-2016">새 cmdlet:   New-AzHostGroup, New-AzHost, Get-AzHostGroup, Get-AzHost, Remove-AzHostGroup, Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="6783d-2016">New cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span></span>
    - <span data-ttu-id="6783d-2017">HostId 매개 변수가 New-AzVMConfig 및 New-AzVM 추가됨</span><span class="sxs-lookup"><span data-stu-id="6783d-2017">HostId parameter is added to New-AzVMConfig and New-AzVM</span></span>
* <span data-ttu-id="6783d-2018">'Invoke-AzVMRunCommand' 설명서의 예제에서 올바른 매개 변수 이름을 사용하도록 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="6783d-2018">Update example in 'Invoke-AzVMRunCommand' documentation to use correct parameter name</span></span>
* <span data-ttu-id="6783d-2019">'Set-AzVMDiskEncryptionExtension' 및 'Set-AzVmssDiskEncryptionExtension' 참조 설명서의 '-VolumeType' 설명이 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="6783d-2019">Update '-VolumeType' description in 'Set-AzVMDiskEncryptionExtension' and 'Set-AzVmssDiskEncryptionExtension' reference documentation</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="6783d-2020">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="6783d-2020">Az.DataFactory</span></span>
* <span data-ttu-id="6783d-2021">'New-AzDataFactoryEncryptValue' 설명서에서 'Windows'를 대문자로 시작하도록 오타가 수정됨</span><span class="sxs-lookup"><span data-stu-id="6783d-2021">Fix typo to capitalize 'Windows' in 'New-AzDataFactoryEncryptValue' documentation</span></span>
* <span data-ttu-id="6783d-2022">ADF .Net SDK 버전이 4.1.2로 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="6783d-2022">Updated ADF .Net SDK version to 4.1.2</span></span>
* <span data-ttu-id="6783d-2023">자체 호스팅 통합 런타임을 SSIS Integration Runtime의 프록시로 설정할 수 있도록 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' 및 'DataProxyStagingPath' 매개 변수가 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd에 추가됨</span><span class="sxs-lookup"><span data-stu-id="6783d-2023">Add parameter 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' and 'DataProxyStagingPath' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable set up Self-Hosted Integration Runtime as a proxy for SSIS Integration Runtime</span></span>
* <span data-ttu-id="6783d-2024">PSTriggerRun에서 트리거된 파이프라인, 메시지 및 속성을 표시하고, PSActivityRun에서 작업 유형을 표시하도록 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="6783d-2024">Updated PSTriggerRun to show the triggered pipelines, message and properties, and PSActivityRun to show the activity type</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="6783d-2025">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="6783d-2025">Az.DataLakeStore</span></span>
* <span data-ttu-id="6783d-2026">오류 또는 원격 예외에 대한 Get-DataLakeStoreDeletedItem 중단이 수정됨</span><span class="sxs-lookup"><span data-stu-id="6783d-2026">Fix hanging of Get-DataLakeStoreDeletedItem for any errors or remote exceptions.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="6783d-2027">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="6783d-2027">Az.EventHub</span></span>
* <span data-ttu-id="6783d-2028">#9658 문제 해결: Set-AzEventHubNetworkRuleSet의 VirtualNteworkRule 매개 변수에 대한 오타</span><span class="sxs-lookup"><span data-stu-id="6783d-2028">Fix for issue #9658 : Typo VirtualNteworkRule parameter in Set-AzEventHubNetworkRuleSet</span></span>
* <span data-ttu-id="6783d-2029">#9558 문제 해결: Set-AzEventHubNamespace에서 PUT 대신 PATCH가 사용됨</span><span class="sxs-lookup"><span data-stu-id="6783d-2029">Fix for issue #9558 : Set-AzEventHubNamespace is using PATCH instead of PUT</span></span>
* <span data-ttu-id="6783d-2030">EnableKafka 매개 변수가 Set-AzEventHubNamespace cmdlet에 추가됨</span><span class="sxs-lookup"><span data-stu-id="6783d-2030">added EnableKafka parameter to Set-AzEventHubNamespace cmdlet</span></span>
* <span data-ttu-id="6783d-2031">#9786 문제 해결: Listen(수신 대기) 전용 권한이 있는 규칙을 만들 수 없음</span><span class="sxs-lookup"><span data-stu-id="6783d-2031">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>

#### <a name="azmarketplaceordering"></a><span data-ttu-id="6783d-2032">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="6783d-2032">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="6783d-2033">'Azure'가 모두 소문자인 설명서의 오타가 수정됨</span><span class="sxs-lookup"><span data-stu-id="6783d-2033">Fixed documentation typo where 'Azure' was all lowercase letters</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="6783d-2034">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="6783d-2034">Az.Monitor</span></span>
* <span data-ttu-id="6783d-2035">도움말 설명서에서 잘못된 매개 변수 이름이 수정됨</span><span class="sxs-lookup"><span data-stu-id="6783d-2035">Fixed incorrect parameter name in help documentation</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6783d-2036">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6783d-2036">Az.Network</span></span>
* <span data-ttu-id="6783d-2037">New-AzPrivateLinkServiceIpConfig가 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="6783d-2037">Updated New-AzPrivateLinkServiceIpConfig</span></span>
    - <span data-ttu-id="6783d-2038">서버 쪽에서 사용되지 않으므로 'PublicIpAddress' 매개 변수가 사용되지 않음</span><span class="sxs-lookup"><span data-stu-id="6783d-2038">Deprecated the paramster 'PublicIpAddress' since this is never used in the server side.</span></span>
    - <span data-ttu-id="6783d-2039">현재 IP 구성이 기본 구성인지 여부를 나타내는 하나의 선택적 'Primary' 매개 변수가 추가됨</span><span class="sxs-lookup"><span data-stu-id="6783d-2039">Added one optional parameter 'Primary' that indicate the current ip configuration is primary one or not.</span></span>
* <span data-ttu-id="6783d-2040">SDK의 요청 오류 예외 처리가 향상됨 - 이전의 SDK 예외가 올바르게 처리되지 않아 주요 오류 세부 정보가 표시되지 않은 문제가 해결됨</span><span class="sxs-lookup"><span data-stu-id="6783d-2040">Improved handling of request error exception from SDK   -Fixes the issue that previously SDK exceptions aren't handled correctly which results in key error details not being displayed</span></span>
* <span data-ttu-id="6783d-2041">올바른 IPv6 접두사 길이를 확인하기 위해 Ipv6 IP 접두사에 대한 유효성 검사 논리가 조정됨</span><span class="sxs-lookup"><span data-stu-id="6783d-2041">Adjusted validation logic for Ipv6 IP Prefix to check for correct IPv6 prefix length.</span></span>
* <span data-ttu-id="6783d-2042">Get-AzVirtualNetworkSubnetConfig가 업데이트됨: 서브넷 리소스 ID별로 가져오도록 설정되는 매개 변수 세트가 추가됨</span><span class="sxs-lookup"><span data-stu-id="6783d-2042">Updated Get-AzVirtualNetworkSubnetConfig: Added parameter set to get by subnet resource id.</span></span>
* <span data-ttu-id="6783d-2043">AzNetworkServiceTag의 Location(위치) 매개 변수에 대한 설명이 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="6783d-2043">Updated description of Location parameter for AzNetworkServiceTag</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="6783d-2044">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="6783d-2044">Az.OperationalInsights</span></span>
* <span data-ttu-id="6783d-2045">'New-AzOperationalInsightsLinuxSyslogDataSource'에 대한 설명서가 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="6783d-2045">Updated documentation for 'New-AzOperationalInsightsLinuxSyslogDataSource'</span></span>
    - <span data-ttu-id="6783d-2046">예제가 추가됨</span><span class="sxs-lookup"><span data-stu-id="6783d-2046">Added example</span></span>
    - <span data-ttu-id="6783d-2047">'-Name' 매개 변수에 대한 설명이 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="6783d-2047">Updated description for '-Name' parameter</span></span>
* <span data-ttu-id="6783d-2048">New-AzOperationalInsightsWindowsEventDataSource에 대한 예제가 추가됨</span><span class="sxs-lookup"><span data-stu-id="6783d-2048">Added an example for New-AzOperationalInsightsWindowsEventDataSource</span></span>
* <span data-ttu-id="6783d-2049">New-AzOperationalInsightsWindowsEventDataSource의 -Name 매개 변수에 대한 설명이 변경됨</span><span class="sxs-lookup"><span data-stu-id="6783d-2049">Changed the description of the -Name parameter for New-AzOperationalInsightsWindowsEventDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="6783d-2050">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="6783d-2050">Az.RecoveryServices</span></span>
* <span data-ttu-id="6783d-2051">'Get-AzRecoveryServicesBackupJobDetail.md'가 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="6783d-2051">Update 'Get-AzRecoveryServicesBackupJobDetail.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="6783d-2052">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6783d-2052">Az.Resources</span></span>
* <span data-ttu-id="6783d-2053">Microsoft 리소스에 대한 새 2019-05-10 API 버전 지원이 추가됨</span><span class="sxs-lookup"><span data-stu-id="6783d-2053">Add support for new api version 2019-05-10 for Microsoft.Resource</span></span>
    - <span data-ttu-id="6783d-2054">변수, 리소스 및 속성에 대한 'copy.count = 0' 지원이 추가됨</span><span class="sxs-lookup"><span data-stu-id="6783d-2054">Add support for 'copy.count = 0' for variables, resources and properties</span></span>
    - <span data-ttu-id="6783d-2055">'condition = false' 또는 'copy.count = 0'인 리소스가 완료 모드에서 삭제됨</span><span class="sxs-lookup"><span data-stu-id="6783d-2055">Resources with 'condition = false' or 'copy.count = 0' will be deleted in complete mode</span></span>
* <span data-ttu-id="6783d-2056">정책을 구독 수준에서 도움말 문서에 할당하는 예제가 추가됨</span><span class="sxs-lookup"><span data-stu-id="6783d-2056">Add an example of assigning policy at subscription level to help doc</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="6783d-2057">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="6783d-2057">Az.ServiceBus</span></span>
* <span data-ttu-id="6783d-2058">#9658 문제 해결: Set-AzServiceBusNetworkRuleSet의 VirtualNetworkRule 매개 변수에 대한 오타</span><span class="sxs-lookup"><span data-stu-id="6783d-2058">Fix for issue #9658 : Typo VirtualNetworkRule parameter in Set-AzServiceBusNetworkRuleSet</span></span>
* <span data-ttu-id="6783d-2059">#9786 문제 해결: Listen(수신 대기) 전용 권한이 있는 규칙을 만들 수 없음</span><span class="sxs-lookup"><span data-stu-id="6783d-2059">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>
* <span data-ttu-id="6783d-2060">큐 및 토픽에 대한 이름 가용성을 확인하는 새 'Test-AzServiceBusNameAvailability' 명령이 추가됨</span><span class="sxs-lookup"><span data-stu-id="6783d-2060">Added new command 'Test-AzServiceBusNameAvailability' to check the name availability for queue and topic</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="6783d-2061">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="6783d-2061">Az.ServiceFabric</span></span>
* <span data-ttu-id="6783d-2062">노드 유형 추가 cmdlet 버그 수정:</span><span class="sxs-lookup"><span data-stu-id="6783d-2062">Fix add node type cmdlet bugs:</span></span>
    - <span data-ttu-id="6783d-2063">서비스 패브릭 클러스터와 관련이 없는 다른 vmss가 리소스 그룹에 있을 때 발생하는 NullReferenceException 버그</span><span class="sxs-lookup"><span data-stu-id="6783d-2063">NullReferenceException bug when resource group had other vmss not related to the service fabric cluster.</span></span> <span data-ttu-id="6783d-2064">문제 해결: https://github.com/Azure/azure-powershell/issues/8681</span><span class="sxs-lookup"><span data-stu-id="6783d-2064">Fixes issue: https://github.com/Azure/azure-powershell/issues/8681</span></span>
    - <span data-ttu-id="6783d-2065">virtualNetwork가 클러스터의 다른 리소스 그룹에 있을 때 cmdlet이 실패하는 버그가 수정됨</span><span class="sxs-lookup"><span data-stu-id="6783d-2065">Fix bug where cmdlet failed if virtualNetwork was in a different resource group that the cluster.</span></span> <span data-ttu-id="6783d-2066">문제 해결: https://github.com/Azure/azure-powershell/issues/8407</span><span class="sxs-lookup"><span data-stu-id="6783d-2066">fixes issue: https://github.com/Azure/azure-powershell/issues/8407</span></span>
    - <span data-ttu-id="6783d-2067">Add-AzServiceFabricApplicationCertificate cmdlet이 사용되지 않음</span><span class="sxs-lookup"><span data-stu-id="6783d-2067">Deprecating Add-AzServiceFabricApplicationCertificate cmdlet</span></span>

#### <a name="azsql"></a><span data-ttu-id="6783d-2068">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6783d-2068">Az.Sql</span></span>
* <span data-ttu-id="6783d-2069">이전의 Auditing(감사) cmdlet에 대한 설명서가 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="6783d-2069">Update documentation of old Auditing cmdlets.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="6783d-2070">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="6783d-2070">Az.Storage</span></span>
* <span data-ttu-id="6783d-2071">더 많은 시나리오를 cmdlet 예제에 추가하고 매개 변수 설명을 업데이트하여 Get/Close-AzStorageFileHandle에 대한 도움말이 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="6783d-2071">Update help for Get/Close-AzStorageFileHandle, by add more scenarios to cmdlet examples and update parameter descriptions</span></span>
* <span data-ttu-id="6783d-2072">Blob 업로드 및 Blob 복사에서 StandardBlobTier가 지원됨</span><span class="sxs-lookup"><span data-stu-id="6783d-2072">Support StandardBlobTier in upload blob and copy blob</span></span>
    -  <span data-ttu-id="6783d-2073">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="6783d-2073">Set-AzStorageBlobContent</span></span>
    -  <span data-ttu-id="6783d-2074">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="6783d-2074">Start-AzStorageBlobCopy</span></span>
* <span data-ttu-id="6783d-2075">Blob 복사에서 우선 순위 리하이드레이션이 지원됨</span><span class="sxs-lookup"><span data-stu-id="6783d-2075">Support Rehydrate Priority in copy blob</span></span>
    -  <span data-ttu-id="6783d-2076">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="6783d-2076">Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="6783d-2077">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="6783d-2077">Az.Websites</span></span>
* <span data-ttu-id="6783d-2078">Set-AzWebApp 및 Set-AzWebAppSlot에서 -AppSettings 매개 변수에 대한 설명이 추가됨</span><span class="sxs-lookup"><span data-stu-id="6783d-2078">Add clarification around -AppSettings parameter in Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <a name="250---july-2019"></a><span data-ttu-id="6783d-2079">2.5.0 - 2019년 7월</span><span class="sxs-lookup"><span data-stu-id="6783d-2079">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="6783d-2080">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6783d-2080">Az.Accounts</span></span>
* <span data-ttu-id="6783d-2081">ClientRuntime의 최신 버전을 사용하도록 일반적인 코드를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-2081">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="6783d-2082">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="6783d-2082">Az.ApplicationInsights</span></span>
* <span data-ttu-id="6783d-2083">'Remove-AzApplicationInsightsApiKey' 설명서의 예제 오타 수정</span><span class="sxs-lookup"><span data-stu-id="6783d-2083">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span>

#### <a name="azautomation"></a><span data-ttu-id="6783d-2084">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="6783d-2084">Az.Automation</span></span>
* <span data-ttu-id="6783d-2085">리소스 문자열의 오타 수정</span><span class="sxs-lookup"><span data-stu-id="6783d-2085">Fix typo in resource string</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="6783d-2086">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="6783d-2086">Az.CognitiveServices</span></span>
* <span data-ttu-id="6783d-2087">NetworkRuleSet 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-2087">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6783d-2088">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6783d-2088">Az.Compute</span></span>
* <span data-ttu-id="6783d-2089">VM 인스턴스 보기 개체의 누락된 속성(ComputerName, OsName, OsVersion 및 HyperVGeneration)을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-2089">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="6783d-2090">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="6783d-2090">Az.ContainerRegistry</span></span>
* <span data-ttu-id="6783d-2091">복제 매개 변수의 Remove-AzContainerRegistryReplication에서 오타 수정</span><span class="sxs-lookup"><span data-stu-id="6783d-2091">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="6783d-2092">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/9633 을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="6783d-2092">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="6783d-2093">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="6783d-2093">Az.DataFactory</span></span>
* <span data-ttu-id="6783d-2094">ADF .Net SDK 버전을 4.1.0으로 업데이트</span><span class="sxs-lookup"><span data-stu-id="6783d-2094">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="6783d-2095">'Get-AzDataFactoryV2PipelineRun' 설명서의 오타 수정</span><span class="sxs-lookup"><span data-stu-id="6783d-2095">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="6783d-2096">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="6783d-2096">Az.EventHub</span></span>
* <span data-ttu-id="6783d-2097">SAS 토큰을 생성하기 위해 추가된 새로운 cmmdlet 추가: New-AzEventHubAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="6783d-2097">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="6783d-2098">'관리'만 지정된 경우 authorizationrules 권한에 대한 확인 및 오류 메시지 추가</span><span class="sxs-lookup"><span data-stu-id="6783d-2098">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="6783d-2099">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="6783d-2099">Az.KeyVault</span></span>
* <span data-ttu-id="6783d-2100">인증서 정책에 대한 KeySize 지정을 위한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="6783d-2100">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="6783d-2101">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="6783d-2101">Az.LogicApp</span></span>
* <span data-ttu-id="6783d-2102">모든 맵 유형을 나열하도록 Get-AzIntegrationAccountMap 수정</span><span class="sxs-lookup"><span data-stu-id="6783d-2102">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="6783d-2103">필터링을 위해 새 MapType 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="6783d-2103">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="6783d-2104">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="6783d-2104">Az.ManagedServices</span></span>
* <span data-ttu-id="6783d-2105">API 버전 2019-06-01(GA)에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="6783d-2105">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6783d-2106">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6783d-2106">Az.Network</span></span>
* <span data-ttu-id="6783d-2107">프라이빗 엔드포인트 및 프라이빗 링크 서비스에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="6783d-2107">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="6783d-2108">새로운 cmdlet</span><span class="sxs-lookup"><span data-stu-id="6783d-2108">New cmdlets</span></span>
        - <span data-ttu-id="6783d-2109">Set-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="6783d-2109">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="6783d-2110">Set-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="6783d-2110">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="6783d-2111">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="6783d-2111">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="6783d-2112">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="6783d-2112">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="6783d-2113">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="6783d-2113">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="6783d-2114">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="6783d-2114">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="6783d-2115">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="6783d-2115">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="6783d-2116">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="6783d-2116">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="6783d-2117">기능에 대한 새로운 명령이 업데이트됨: Virtualnetwork의 서브넷에 있는 PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies 플래그</span><span class="sxs-lookup"><span data-stu-id="6783d-2117">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="6783d-2118">업데이트된 New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="6783d-2118">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="6783d-2119">이 서브넷의 프라이빗 엔드포인트에 네트워크 정책을 적용할지 여부를 나타내는 선택적 매개 변수 -PrivateEndpointNetworkPoliciesFlag가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-2119">Added optional parameter -PrivateEndpointNetworkPoliciesFlag that configures whether to apply network policies on private endpoint in this subnet.</span></span>
        - <span data-ttu-id="6783d-2120">이 서브넷의 프라이빗 연결 서비스에 네트워크 정책을 적용할지 여부를 나타내는 선택적 매개 변수 -PrivateLinkServiceNetworkPoliciesFlag가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-2120">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag that configures whether to apply network policies network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="6783d-2121">AzPrivateLinkService의 cmdlet 매개 변수 'ServiceName'이 이전 버전과의 호환성을 위해 별칭 'ServiceName'을 사용한 'Name'으로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-2121">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="6783d-2122">네트워크 보안 규칙 구성에 ICMP 프로토콜 사용</span><span class="sxs-lookup"><span data-stu-id="6783d-2122">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="6783d-2123">다음 Cmdlet이 업데이트 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-2123">Updated cmdlets</span></span>
        - <span data-ttu-id="6783d-2124">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="6783d-2124">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="6783d-2125">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="6783d-2125">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="6783d-2126">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="6783d-2126">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="6783d-2127">New-AzVirtualNetworkGatewayConnection에 대한 구성 가능한 매개 변수로 ConnectionProtocolType (Ikev1/Ikev2) 추가</span><span class="sxs-lookup"><span data-stu-id="6783d-2127">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="6783d-2128">LoadBalancerFrontendIpConfiguration에 PrivateIpAddressVersion 추가</span><span class="sxs-lookup"><span data-stu-id="6783d-2128">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="6783d-2129">업데이트된 cmdlet:</span><span class="sxs-lookup"><span data-stu-id="6783d-2129">Updated cmdlet:</span></span>
        - <span data-ttu-id="6783d-2130">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="6783d-2130">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="6783d-2131">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="6783d-2131">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="6783d-2132">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="6783d-2132">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="6783d-2133">프로브에서 사용자 지정 포트를 지원하기 위한 Application Gateway New-AzApplicationGatewayProbeConfig 명령 업데이트</span><span class="sxs-lookup"><span data-stu-id="6783d-2133">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="6783d-2134">업데이트된 New-AzApplicationGatewayProbeConfig: 백 엔드 서버 검색에 사용되는 선택적 매개 변수 포트가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-2134">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="6783d-2135">이 매개 변수는 Standard_V2 및 WAF_V2 SKU에 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-2135">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="6783d-2136">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="6783d-2136">Az.OperationalInsights</span></span>
* <span data-ttu-id="6783d-2137">저장된 검색의 기본 버전이 1로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-2137">Updated default version for saved searches to be 1.</span></span>
* <span data-ttu-id="6783d-2138">사용자 지정 로그 null regex 처리가 수정됨</span><span class="sxs-lookup"><span data-stu-id="6783d-2138">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="6783d-2139">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="6783d-2139">Az.RecoveryServices</span></span>
* <span data-ttu-id="6783d-2140">'Get-AzRecoveryServicesBackupJob.md' 업데이트</span><span class="sxs-lookup"><span data-stu-id="6783d-2140">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="6783d-2141">'Get-AzRecoveryServicesBackupContainer.md' 업데이트</span><span class="sxs-lookup"><span data-stu-id="6783d-2141">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="6783d-2142">'Get-AzRecoveryServicesVault.md' 업데이트</span><span class="sxs-lookup"><span data-stu-id="6783d-2142">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="6783d-2143">'Wait-AzRecoveryServicesBackupJob.md' 업데이트</span><span class="sxs-lookup"><span data-stu-id="6783d-2143">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="6783d-2144">'Set-AzRecoveryServicesVaultContext.md' 업데이트</span><span class="sxs-lookup"><span data-stu-id="6783d-2144">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="6783d-2145">'Get-AzRecoveryServicesBackupItem.md' 업데이트</span><span class="sxs-lookup"><span data-stu-id="6783d-2145">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="6783d-2146">'Get-AzRecoveryServicesBackupRecoveryPoint.md' 업데이트</span><span class="sxs-lookup"><span data-stu-id="6783d-2146">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="6783d-2147">'Restore-AzRecoveryServicesBackupItem.md' 업데이트</span><span class="sxs-lookup"><span data-stu-id="6783d-2147">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="6783d-2148">Azure 파일 공유용 컨테이너를 등록 취소하기 위해 서비스 요청 업데이트</span><span class="sxs-lookup"><span data-stu-id="6783d-2148">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="6783d-2149">'Set-AzRecoveryServicesAsrAlertSetting.md' 업데이트</span><span class="sxs-lookup"><span data-stu-id="6783d-2149">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="6783d-2150">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6783d-2150">Az.Resources</span></span>
- <span data-ttu-id="6783d-2151">'New-AzResourceGroupDeployment' 설명서에서 참조된 누락 cmdlet 제거</span><span class="sxs-lookup"><span data-stu-id="6783d-2151">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="6783d-2152">새 API 버전 2019-01-01을 사용하도록 정책 cmdlet 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="6783d-2152">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="6783d-2153">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="6783d-2153">Az.ServiceBus</span></span>
* <span data-ttu-id="6783d-2154">SAS 토큰을 생성하기 위해 추가된 새로운 cmmdlet 추가: New-AzServiceBusAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="6783d-2154">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="6783d-2155">'관리'만 지정된 경우 authorizationrules 권한에 대한 확인 및 오류 메시지 추가</span><span class="sxs-lookup"><span data-stu-id="6783d-2155">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="6783d-2156">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6783d-2156">Az.Sql</span></span>
* <span data-ttu-id="6783d-2157">Set-AzSqlDatabaseSecondary cmdlet에 대한 누락된 예제 수정</span><span class="sxs-lookup"><span data-stu-id="6783d-2157">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="6783d-2158">이메일 주소를 제공하지 않고 설정된 취약성 평가 반복 검색 수정</span><span class="sxs-lookup"><span data-stu-id="6783d-2158">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="6783d-2159">경고 메시지의 작은 오타를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-2159">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="6783d-2160">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="6783d-2160">Az.Storage</span></span>
* <span data-ttu-id="6783d-2161">'Get-AzStorageAccount'에 대한 참조 설명서의 예제를 업데이트하여 올바른 매개 변수 이름 사용</span><span class="sxs-lookup"><span data-stu-id="6783d-2161">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="6783d-2162">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="6783d-2162">Az.StorageSync</span></span>
* <span data-ttu-id="6783d-2163">Invoke-AzStorageSyncChangeDetection cmdlet을 추가하는 중입니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-2163">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="6783d-2164">TierFilesOlderThanDays를 기념하는 문제 9551 수정</span><span class="sxs-lookup"><span data-stu-id="6783d-2164">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="6783d-2165">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="6783d-2165">Az.Websites</span></span>
* <span data-ttu-id="6783d-2166">Get-AzWebApp 및 Set-AzWebApp에서 일부 SiteConfig 속성을 반환하지 않은 버그 수정</span><span class="sxs-lookup"><span data-stu-id="6783d-2166">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="6783d-2167">Get-AzDeletedWebApp 및 Restore-AzDeletedWebApp에 새 위치 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="6783d-2167">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="6783d-2168">AzWebApp-IncludeSourceWebAppSlots을 사용하여 웹앱 슬롯을 복제하는 버그를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-2168">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="6783d-2169">2.4.0 - 2019년 7월</span><span class="sxs-lookup"><span data-stu-id="6783d-2169">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="6783d-2170">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6783d-2170">Az.Accounts</span></span>
* <span data-ttu-id="6783d-2171">프로필 cmdlet에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="6783d-2171">Add support for profile cmdlets</span></span>
* <span data-ttu-id="6783d-2172">생성된 cmdlet에서 환경 및 데이터 평면에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="6783d-2172">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="6783d-2173">Windows PowerShell의 데이터 평면 cmdlet에대해 일부 경우 잘못된 엔드포인트가 사용되는 버그 수정</span><span class="sxs-lookup"><span data-stu-id="6783d-2173">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="6783d-2174">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="6783d-2174">Az.Advisor</span></span>
* <span data-ttu-id="6783d-2175">Az.Advisor의 GA 릴리스</span><span class="sxs-lookup"><span data-stu-id="6783d-2175">GA release of Az.Advisor</span></span>
* <span data-ttu-id="6783d-2176">이 모듈은 이제 롤업 `Az` 모듈의 일부로 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-2176">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="6783d-2177">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="6783d-2177">Az.ApiManagement</span></span>
* <span data-ttu-id="6783d-2178">문제 https://github.com/Azure/azure-powershell/issues/8671 수정</span><span class="sxs-lookup"><span data-stu-id="6783d-2178">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="6783d-2179">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="6783d-2179">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="6783d-2180">사용자 및 제품별 구독을 쿼리하기 위한 지원이 추가됨</span><span class="sxs-lookup"><span data-stu-id="6783d-2180">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="6783d-2181">범위 '/', '/ api, '/ api/echo api'를 사용하여 쿼리하기 위한 지원이 추가됨</span><span class="sxs-lookup"><span data-stu-id="6783d-2181">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="6783d-2182">[https://github.com/Azure/azure-powershell/issues/9307](https://github.com/Azure/azure-powershell/issues/9307 ) 및 https://github.com/Azure/azure-powershell/issues/8432 문제 수정</span><span class="sxs-lookup"><span data-stu-id="6783d-2182">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="6783d-2183">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="6783d-2183">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="6783d-2184">Apis를 가져올 때 'ApiVersion' 및 'ApiVersionSetId'를 지정하기 위한 지원이 추가됨</span><span class="sxs-lookup"><span data-stu-id="6783d-2184">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="6783d-2185">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="6783d-2185">Az.Automation</span></span>
* <span data-ttu-id="6783d-2186">문자열 값을 처리하기 위해 Set-AzAutomationConnectionFieldValue cmdlet 버그를 수정했습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-2186">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6783d-2187">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6783d-2187">Az.Compute</span></span>
* <span data-ttu-id="6783d-2188">New-AzImageConfig에 HyperVGeneration 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="6783d-2188">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="6783d-2189">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="6783d-2189">Az.DataFactory</span></span>
* <span data-ttu-id="6783d-2190">get activity runs, get pipeline runs, get trigger runs ADF cmdlet의 출력을 업데이트하여 Select-Object pipe를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-2190">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="6783d-2191">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="6783d-2191">Az.EventGrid</span></span>
* <span data-ttu-id="6783d-2192">'New-AzEventGridSubcription' 설명서의 오타 수정</span><span class="sxs-lookup"><span data-stu-id="6783d-2192">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="6783d-2193">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="6783d-2193">Az.IotHub</span></span>
* <span data-ttu-id="6783d-2194">권한 부여 정책 키를 다시 생성하기 위한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="6783d-2194">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6783d-2195">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6783d-2195">Az.Network</span></span>
* <span data-ttu-id="6783d-2196">'RoutingPreference'를 공용 IP 태그에 추가함</span><span class="sxs-lookup"><span data-stu-id="6783d-2196">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="6783d-2197">'Get-AzNetworkServiceTag' 참조 설명서의 예제 개선</span><span class="sxs-lookup"><span data-stu-id="6783d-2197">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="6783d-2198">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="6783d-2198">Az.PolicyInsights</span></span>
* <span data-ttu-id="6783d-2199">Get-AzPolicyState의 null 참조 문제 해결</span><span class="sxs-lookup"><span data-stu-id="6783d-2199">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="6783d-2200">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/9446 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="6783d-2200">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="6783d-2201">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="6783d-2201">Az.OperationalInsights</span></span>
* <span data-ttu-id="6783d-2202">Get-AzOperationalInsightsDataSource에 반환된 CustomLog datasource 모델 수정됨</span><span class="sxs-lookup"><span data-stu-id="6783d-2202">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="6783d-2203">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="6783d-2203">Az.RecoveryServices</span></span>
* <span data-ttu-id="6783d-2204">IaaSVMs에 대한 get-policy 명령 수정</span><span class="sxs-lookup"><span data-stu-id="6783d-2204">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="6783d-2205">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6783d-2205">Az.Resources</span></span>
    - <span data-ttu-id="6783d-2206">Get-AzPolicyState -Top 매개 변수에 대한 도움말 텍스트 수정</span><span class="sxs-lookup"><span data-stu-id="6783d-2206">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="6783d-2207">Get-AzPolicyAlias에 대한 클라이언트 쪽 페이징 지원 추가</span><span class="sxs-lookup"><span data-stu-id="6783d-2207">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="6783d-2208">Set-AzPolicyAssignment, -PolicyParameters 및 -PolicyParametersObject에 대한 새 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="6783d-2208">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="6783d-2209">Policy cmdlet에 대한 몇 가지 문서 및 예제 업데이트</span><span class="sxs-lookup"><span data-stu-id="6783d-2209">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="6783d-2210">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="6783d-2210">Az.ServiceBus</span></span>
* <span data-ttu-id="6783d-2211">문제 #4938 수정 - MaxSizeInMegabytes를 설정할 때 New-AzureRmServiceBusQueue가 BadRequest 반환</span><span class="sxs-lookup"><span data-stu-id="6783d-2211">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="6783d-2212">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6783d-2212">Az.Sql</span></span>
* <span data-ttu-id="6783d-2213">미리 보기 릴리스에서 공개 릴리스로 인스턴스 장애 조치(Failover) 그룹 cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="6783d-2213">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="6783d-2214">새 cmdlet으로 Azure SQL Server\Database Auditing을 지원하세요.</span><span class="sxs-lookup"><span data-stu-id="6783d-2214">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="6783d-2215">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="6783d-2215">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="6783d-2216">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="6783d-2216">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="6783d-2217">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="6783d-2217">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="6783d-2218">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="6783d-2218">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="6783d-2219">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="6783d-2219">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="6783d-2220">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="6783d-2220">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="6783d-2221">취약성 평가 설정에서 이메일 제약 조건 제거</span><span class="sxs-lookup"><span data-stu-id="6783d-2221">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="6783d-2222">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="6783d-2222">Az.Storage</span></span>
* <span data-ttu-id="6783d-2223">다음 cmdlet에서 2개의 매개 변수 '-IndexDocument' 및 '-ErrorDocument404Path'를 필수에서 선택으로 변경하세요.</span><span class="sxs-lookup"><span data-stu-id="6783d-2223">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="6783d-2224">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="6783d-2224">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="6783d-2225">예제를 추가하여 Get-AzStorageBlobContent의 도움말 업데이트</span><span class="sxs-lookup"><span data-stu-id="6783d-2225">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="6783d-2226">StorageException으로 cmdlet이 실패한 경우 자세한 오류 정보 표시</span><span class="sxs-lookup"><span data-stu-id="6783d-2226">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="6783d-2227">Azure Files AAD DS 인증으로 스토리지 계정 생성 또는 업데이트 지원</span><span class="sxs-lookup"><span data-stu-id="6783d-2227">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="6783d-2228">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6783d-2228">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="6783d-2229">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6783d-2229">Set-AzStorageAccount</span></span>
* <span data-ttu-id="6783d-2230">파일 공유, 파일 디렉터리 또는 파일의 목록 지원 또는 파일 핸들 닫기</span><span class="sxs-lookup"><span data-stu-id="6783d-2230">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="6783d-2231">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="6783d-2231">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="6783d-2232">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="6783d-2232">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="6783d-2233">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="6783d-2233">Az.StorageSync</span></span>
* <span data-ttu-id="6783d-2234">이 모듈은 이제 롤업 `Az` 모듈의 일부로 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-2234">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="6783d-2235">2.3.2 - 2019년 6월</span><span class="sxs-lookup"><span data-stu-id="6783d-2235">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="6783d-2236">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6783d-2236">Az.Accounts</span></span>
* <span data-ttu-id="6783d-2237">함수 호출에 대해 일부 경우 잘못된 URL이 사용되는 버그 수정</span><span class="sxs-lookup"><span data-stu-id="6783d-2237">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="6783d-2238">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/8983 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="6783d-2238">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="6783d-2239">AzureRM에서 Az cmdlet으로의 별칭 문제 해결</span><span class="sxs-lookup"><span data-stu-id="6783d-2239">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="6783d-2240">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="6783d-2240">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="6783d-2241">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="6783d-2241">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6783d-2242">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6783d-2242">Az.Compute</span></span>
* <span data-ttu-id="6783d-2243">New-AzVm 및 New-AzVmss 단순 매개 변수 집합은 이제 'ProximityPlacementGroup'매개 변수를 허용합니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-2243">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="6783d-2244">'New-AzVM' 참조 설명서에서 오타 수정</span><span class="sxs-lookup"><span data-stu-id="6783d-2244">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="6783d-2245">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="6783d-2245">Az.Dns</span></span>
* <span data-ttu-id="6783d-2246">'Set-AzDnsZone' 도움말 예제의 오타가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-2246">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="6783d-2247">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="6783d-2247">Az.EventGrid</span></span>
* <span data-ttu-id="6783d-2248">2019-06-01 API 버전을 사용하도록 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-2248">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="6783d-2249">새 cmdlet:</span><span class="sxs-lookup"><span data-stu-id="6783d-2249">New cmdlets:</span></span>
    - <span data-ttu-id="6783d-2250">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="6783d-2250">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="6783d-2251">새 Azure Event Grid 도메인을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-2251">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="6783d-2252">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="6783d-2252">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="6783d-2253">Event Grid 도메인의 세부 정보를 가져오거나 현재 Azure 구독의 모든 Event Grid 도메인 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-2253">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="6783d-2254">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="6783d-2254">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="6783d-2255">Azure Event Grid 도메인을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-2255">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="6783d-2256">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="6783d-2256">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="6783d-2257">Azure Event Grid 도메인에 대한 공유 액세스 키를 다시 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-2257">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="6783d-2258">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="6783d-2258">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="6783d-2259">Event Grid 도메인 이벤트를 게시하는 데 사용되는 공유 액세스 키를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-2259">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="6783d-2260">New-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="6783d-2260">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="6783d-2261">새 Azure Event Grid 도메인 토픽을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-2261">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="6783d-2262">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="6783d-2262">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="6783d-2263">Event Grid 도메인 토픽의 세부 사항을 가져오거나, 현재 Azure의 특정 Event Grid 도메인 아래의 모든 Event Grid 도메인 토픽 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-2263">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span>
    - <span data-ttu-id="6783d-2264">Remove-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="6783d-2264">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="6783d-2265">기존 Azure Event Grid 도메인 토픽을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-2265">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="6783d-2266">다음 Cmdlet이 업데이트 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-2266">Updated cmdlets:</span></span>
    - <span data-ttu-id="6783d-2267">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="6783d-2267">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="6783d-2268">새로운 Event Grid 도메인 및 Event Grid 도메인 토픽에 대한 파이핑을 지원하기 위해 새로운 필수 매개 변수를 추가하여 이러한 리소스 아래에 새 이벤트 구독을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-2268">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="6783d-2269">새로운 Event Grid 도메인 이름 및 Event Grid 도메인 토픽 이름을 지정하기 위해 새로운 필수 매개 변수를 추가하여 이러한 리소스 아래에 새 이벤트 구독을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-2269">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="6783d-2270">기존 매개 변수(예: EndPointType, SubjectBeginsWith 등)를 재사용할 수 있도록 도메인 및 도메인 토픽에 대한 새로운 매개 변수 집합을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-2270">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="6783d-2271">지정을 위한 새로운 선택적 매개 변수를 추가</span><span class="sxs-lookup"><span data-stu-id="6783d-2271">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="6783d-2272">이벤트 구독 만료 날짜,</span><span class="sxs-lookup"><span data-stu-id="6783d-2272">Event subscription expiration date,</span></span>
            - <span data-ttu-id="6783d-2273">고급 필터링 매개 변수.</span><span class="sxs-lookup"><span data-stu-id="6783d-2273">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="6783d-2274">대상으로 servicebusqueue에 대한 새 열거형을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-2274">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="6783d-2275">-IncludedEventType 옵션에서 'All' 사용을 허용하지 않고 다음으로 대체함</span><span class="sxs-lookup"><span data-stu-id="6783d-2275">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span>
    - <span data-ttu-id="6783d-2276">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="6783d-2276">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="6783d-2277">결과 페이지 매김 및 필터링을 지원하는 새로운 선택적 매개 변수(Top, ODataQuery 및 NextLink)를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-2277">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="6783d-2278">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="6783d-2278">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="6783d-2279">Event Grid 도메인 및 Event Grid 도메인 토픽에 대한 파이핑을 지원하기 위해 새로운 필수 매개 변수를 추가하여 이러한 리소스 아래에 기존 이벤트 구독을 제거할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-2279">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="6783d-2280">Event Grid 도메인 이름 및 Event Grid 도메인 토픽 이름을 지정하기 위해 새로운 필수 매개 변수를 추가하여 이러한 리소스 아래에 기존 이벤트 구독을 제거할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-2280">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="6783d-2281">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="6783d-2281">Az.FrontDoor</span></span>
* <span data-ttu-id="6783d-2282">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="6783d-2282">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="6783d-2283">변환 지원 및 새 연산자 자동 완성 값(RegEx)을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-2283">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="6783d-2284">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="6783d-2284">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="6783d-2285">새 자동 완성 값 추가</span><span class="sxs-lookup"><span data-stu-id="6783d-2285">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6783d-2286">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6783d-2286">Az.Network</span></span>
* <span data-ttu-id="6783d-2287">Microsoft Azure Virtual Network 게이트웨이 리소스에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="6783d-2287">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="6783d-2288">새로운 cmdlet</span><span class="sxs-lookup"><span data-stu-id="6783d-2288">New cmdlets</span></span>
        - <span data-ttu-id="6783d-2289">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="6783d-2289">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="6783d-2290">AvailablePrivateEndpointType 추가</span><span class="sxs-lookup"><span data-stu-id="6783d-2290">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="6783d-2291">새로운 cmdlet</span><span class="sxs-lookup"><span data-stu-id="6783d-2291">New cmdlets</span></span>
        - <span data-ttu-id="6783d-2292">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="6783d-2292">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="6783d-2293">PrivatePrivateLinkService 추가</span><span class="sxs-lookup"><span data-stu-id="6783d-2293">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="6783d-2294">새로운 cmdlet</span><span class="sxs-lookup"><span data-stu-id="6783d-2294">New cmdlets</span></span>
        - <span data-ttu-id="6783d-2295">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="6783d-2295">Get-AzPrivateLinkService</span></span>
        - <span data-ttu-id="6783d-2296">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="6783d-2296">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="6783d-2297">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="6783d-2297">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="6783d-2298">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="6783d-2298">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="6783d-2299">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="6783d-2299">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="6783d-2300">PrivateEndpoint 추가</span><span class="sxs-lookup"><span data-stu-id="6783d-2300">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="6783d-2301">새로운 cmdlet</span><span class="sxs-lookup"><span data-stu-id="6783d-2301">New cmdlets</span></span>
        - <span data-ttu-id="6783d-2302">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="6783d-2302">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="6783d-2303">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="6783d-2303">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="6783d-2304">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="6783d-2304">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="6783d-2305">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="6783d-2305">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="6783d-2306">기능에 대한 새로운 명령이 업데이트됨: VpnConnection 상의 UseLocalAzureIpAddress 플래그</span><span class="sxs-lookup"><span data-stu-id="6783d-2306">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="6783d-2307">New-AzVpnConnection이 업데이트됨: 선택적 매개 변수 -UseLocalAzureIpAddress를 추가하여 로컬 Azure IP 주소가 연결을 시작하는 동안 소스 주소로 사용되어야 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-2307">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="6783d-2308">Set-AzVpnConnection이 업데이트됨: 선택적 매개 변수 -UseLocalAzureIpAddress를 추가하여 로컬 Azure IP 주소가 연결을 시작하는 동안 소스 주소로 사용되어야 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-2308">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="6783d-2309">ExpressRoute 피어링에 읽기 전용 필드 PeeredConnections가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-2309">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="6783d-2310">ExpressRoute에 읽기 전용 필드 GlobalReachEnabled가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-2310">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="6783d-2311">ExpressRouteCircuit 모델에서 AllowGlobalReach 필드의 사용 중단을 부르는 호환성이 손상되는 변경 속성이 추가됨</span><span class="sxs-lookup"><span data-stu-id="6783d-2311">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="6783d-2312">AzApplicationGatewayRedirectConfiguration cmdlet에서 TargetListenerID를 사용하는 중의 8756 오류 문제가 해결됨</span><span class="sxs-lookup"><span data-stu-id="6783d-2312">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="6783d-2313">다시 쓰기 규칙 세트가 설정되지 못하게 하는 New-AzApplicationGatewayPathRuleConfig의 버그를 수정했습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-2313">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="6783d-2314">NetworkInterfaceIpConfiguration에 VirtualNetworkTaps가 표시되는 방식이 수정됨</span><span class="sxs-lookup"><span data-stu-id="6783d-2314">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="6783d-2315">모든 파트를 나열하도록 Cortex Get cmdlet이 수정됨</span><span class="sxs-lookup"><span data-stu-id="6783d-2315">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="6783d-2316">ExpressRouteGateways, VpnGateway에 대한 VirtualHub 참조 생성 수정됨</span><span class="sxs-lookup"><span data-stu-id="6783d-2316">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="6783d-2317">AzureFirewall 및 NatGateway의 가용성 영역에 대한 지원 추가됨</span><span class="sxs-lookup"><span data-stu-id="6783d-2317">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="6783d-2318">Get-AzNetworkServiceTag cmdlet 추가됨</span><span class="sxs-lookup"><span data-stu-id="6783d-2318">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="6783d-2319">Azure Firewall에 대한 여러 공용 IP 주소에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="6783d-2319">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="6783d-2320">New-AzFirewall cmdlet이 업데이트됨:</span><span class="sxs-lookup"><span data-stu-id="6783d-2320">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="6783d-2321">하나 이상의 공용 IP 주소 개체를 허용하는 매개 변수 -PublicIpAddress 추가됨</span><span class="sxs-lookup"><span data-stu-id="6783d-2321">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="6783d-2322">Virtual Network 개체를 허용하는 매개 변수 -VirtualNetwork 추가됨</span><span class="sxs-lookup"><span data-stu-id="6783d-2322">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="6783d-2323">방화벽 개체에 AddPublicIpAddress 및 RemovePublicIpAddress 메서드 추가됨 - 공용 IP 주소 개체를 입력으로 허용</span><span class="sxs-lookup"><span data-stu-id="6783d-2323">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="6783d-2324">매개 변수 -PublicIpName 및 -VirtualNetworkName이 더 이상 사용되지 않음</span><span class="sxs-lookup"><span data-stu-id="6783d-2324">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span>
* <span data-ttu-id="6783d-2325">기능에 대한 새로운 명령이 업데이트됨: VpnClient AAD 인증 옵션을 가상 네트워크 게이트웨이 리소스로 설정했습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-2325">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span>
    - <span data-ttu-id="6783d-2326">New-AzVirtualNetworkGateway가 업데이트됨: 게이트웨이에서 VpnClient AAD 인증 옵션을 설정할 수 있도록 선택적 매개 변수 AadTenantUri, AadAudienceId, AadIssuerUri가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-2326">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="6783d-2327">Set-AzVirtualNetworkGateway가 업데이트됨: 게이트웨이에서 VpnClient AAD 인증 옵션을 설정할 수 있도록 선택적 매개 변수 AadTenantUri, AadAudienceId, AadIssuerUri가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-2327">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="6783d-2328">Set-AzVirtualNetworkGateway가 업데이트됨: 게이트웨이에서 VpnClient AAD 인증 옵션을 제거할 수 있도록 선택적인 스위치 매개 변수 RemoveAadAuthentication이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-2328">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="6783d-2329">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="6783d-2329">Az.OperationalInsights</span></span>
* <span data-ttu-id="6783d-2330">'New-AzureRmOperationalInsightsWorkspace' 명령에서 **pergb2018** 가격 책정 계층 사용</span><span class="sxs-lookup"><span data-stu-id="6783d-2330">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="6783d-2331">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6783d-2331">Az.Resources</span></span>
* <span data-ttu-id="6783d-2332">추가 템플릿 내보내기 옵션 지원</span><span class="sxs-lookup"><span data-stu-id="6783d-2332">Support for additional Template Export options</span></span>
    - <span data-ttu-id="6783d-2333">Export-AzResourceGroup에 '-SkipResourceNameParameterization' 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="6783d-2333">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="6783d-2334">Export-AzResourceGroup에 '-SkipAllParameterization' 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="6783d-2334">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="6783d-2335">내보낸 리소스 필터링을 위해 Export-AzResourceGroup에 '-Resource' 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="6783d-2335">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="6783d-2336">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="6783d-2336">Az.ServiceFabric</span></span>
* <span data-ttu-id="6783d-2337">일부 경우 잘못된 지문을 가져오는 추가 인증서 ByExistingKeyVault 수정</span><span class="sxs-lookup"><span data-stu-id="6783d-2337">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="6783d-2338">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6783d-2338">Az.Sql</span></span>
* <span data-ttu-id="6783d-2339">Advanced Threat Protection 스토리지 엔드포인트 접미사 수정</span><span class="sxs-lookup"><span data-stu-id="6783d-2339">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="6783d-2340">Advanced Data Security가 Advanced Threat Protection 정책을 재정의하는 것을 수정</span><span class="sxs-lookup"><span data-stu-id="6783d-2340">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="6783d-2341">고객이 TDE 키를 추가하고 관리되는 인스턴스에 TDE 보호기를 설정할 수 있도록 Management.Sql용 새 Cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="6783d-2341">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="6783d-2342">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="6783d-2342">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="6783d-2343">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="6783d-2343">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="6783d-2344">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="6783d-2344">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="6783d-2345">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="6783d-2345">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="6783d-2346">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="6783d-2346">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="6783d-2347">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="6783d-2347">Az.Storage</span></span>
* <span data-ttu-id="6783d-2348">스토리지 계정 생성 시 종류 FileStorage 및 SkuName Premium_ZRS 지원</span><span class="sxs-lookup"><span data-stu-id="6783d-2348">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="6783d-2349">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6783d-2349">New-AzStorageAccount</span></span>
* <span data-ttu-id="6783d-2350">BLOB immutability cmdlet의 설명 명확화</span><span class="sxs-lookup"><span data-stu-id="6783d-2350">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="6783d-2351">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="6783d-2351">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="6783d-2352">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="6783d-2352">Az.Websites</span></span>
* <span data-ttu-id="6783d-2353">Get-AzWebAppCertificate를 클라이언트 대신 서버의 리소스 그룹별로 필터링하도록 최적화</span><span class="sxs-lookup"><span data-stu-id="6783d-2353">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="6783d-2354">Get-AzWebAppSnapshot에 -UseDisasterRecovery 스위치 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="6783d-2354">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="6783d-2355">2.2.0 - 2019년 6월</span><span class="sxs-lookup"><span data-stu-id="6783d-2355">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="6783d-2356">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="6783d-2356">Az.Cdn</span></span>
* <span data-ttu-id="6783d-2357">cmdlet에서 2019-04-15 API 버전 기반의 rulesEngine 기능을 지원하도록 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-2357">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6783d-2358">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6783d-2358">Az.Compute</span></span>
* <span data-ttu-id="6783d-2359">작업을 시작하여 완료되기 전에 즉시 반환하는 `NoWait` 매개 변수가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-2359">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="6783d-2360">다음 Cmdlet이 업데이트 되었습니다.   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="6783d-2360">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="6783d-2361">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="6783d-2361">Az.EventHub</span></span>
* <span data-ttu-id="6783d-2362">#9231 수정 - Get-AzEventHubNamespace에서 태그를 반환하지 않음</span><span class="sxs-lookup"><span data-stu-id="6783d-2362">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="6783d-2363">#9230 수정 - Get-AzEventHubNamespace에서 ResourceGroupName 대신 ResourceGroup을 반환함</span><span class="sxs-lookup"><span data-stu-id="6783d-2363">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6783d-2364">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6783d-2364">Az.Network</span></span>
* <span data-ttu-id="6783d-2365">Nat Gateway에 대한 ResourceId 및 InputObject 업데이트</span><span class="sxs-lookup"><span data-stu-id="6783d-2365">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="6783d-2366">ResourceId 및 InputObject에 대한 별칭 추가</span><span class="sxs-lookup"><span data-stu-id="6783d-2366">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="6783d-2367">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="6783d-2367">Az.PolicyInsights</span></span>
* <span data-ttu-id="6783d-2368">Get-AzPolicyEvent에서 Null 참조 문제 해결</span><span class="sxs-lookup"><span data-stu-id="6783d-2368">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="6783d-2369">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="6783d-2369">Az.RecoveryServices</span></span>
* <span data-ttu-id="6783d-2370">IaaSVM 정책 최소 보존 기간(일)이 1에서 7로 변경됨</span><span class="sxs-lookup"><span data-stu-id="6783d-2370">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="6783d-2371">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="6783d-2371">Az.ServiceBus</span></span>
* <span data-ttu-id="6783d-2372">#9182 문제 해결 - Get-AzServiceBusNamespace에서 ResourceGroupName 대신 ResourceGroup을 반환</span><span class="sxs-lookup"><span data-stu-id="6783d-2372">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="6783d-2373">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="6783d-2373">Az.ServiceFabric</span></span>
* <span data-ttu-id="6783d-2374">'Update-AzServiceFabricReliability' 오류 메시지의 오타 수정</span><span class="sxs-lookup"><span data-stu-id="6783d-2374">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="6783d-2375">Service Fabric 명령줄에서 누락된 문자 수정</span><span class="sxs-lookup"><span data-stu-id="6783d-2375">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="6783d-2376">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6783d-2376">Az.Sql</span></span>
* <span data-ttu-id="6783d-2377">Managed Instance에 대한 AutoDr을 지원하기 위해 New-AzureSqlInstance cmdlet에 대한 DnsZonePartner 매개 변수를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-2377">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="6783d-2378">Get-AzSqlDatabaseSecureConnectionPolicy cmdlet 사용 중단</span><span class="sxs-lookup"><span data-stu-id="6783d-2378">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="6783d-2379">Threat Detection(위협 탐지) cmdlet 이름을 Advanced Threat Protection으로 변경함</span><span class="sxs-lookup"><span data-stu-id="6783d-2379">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="6783d-2380">새 AzSqlInstance -StorageSizeInGB 및 -LicenseType 매개 변수는 이제 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-2380">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="6783d-2381">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="6783d-2381">Az.Websites</span></span>
* <span data-ttu-id="6783d-2382">-WebApp 속성에서 Set-AzWebApp 및 Set-AzWebAppSlot을 사용하면 태그가 제거되는 문제를 해결함</span><span class="sxs-lookup"><span data-stu-id="6783d-2382">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="6783d-2383">2.1.0 - 2019년 5월</span><span class="sxs-lookup"><span data-stu-id="6783d-2383">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="6783d-2384">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="6783d-2384">Az.ApiManagement</span></span>
* <span data-ttu-id="6783d-2385">글로벌 및 API 범위에서 진단을 관리하기 위한 새 cmdlet을 만들었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-2385">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="6783d-2386">**Get-AzApiManagementDiagnostic** - 글로벌 또는 API 범위가 구성된 진단 가져오기</span><span class="sxs-lookup"><span data-stu-id="6783d-2386">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="6783d-2387">**New-AzApiManagementDiagnostic** - 글로벌 범위 또는 API 범위에서 새 진단 만들기</span><span class="sxs-lookup"><span data-stu-id="6783d-2387">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="6783d-2388">**New-AzApiManagementHttpMessageDiagnostic** - 기록할 Headers(헤더) 및 Body Bytes(본문 바이트 수) 크기에 대한 진단 설정 만들기</span><span class="sxs-lookup"><span data-stu-id="6783d-2388">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="6783d-2389">**New-AzApiManagementPipelineDiagnosticSetting** - 게이트웨이로 들어오고 나가는 HTTP 메시지에 대한 진단 설정 만들기</span><span class="sxs-lookup"><span data-stu-id="6783d-2389">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="6783d-2390">**New-AzApiManagementSamplingSetting** - 진단 요청/응답에 대한 샘플링 설정 만들기</span><span class="sxs-lookup"><span data-stu-id="6783d-2390">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="6783d-2391">**Remove-AzApiManagementDiagnostic** - 글로벌 또는 API 범위에서 진단 엔터티 제거</span><span class="sxs-lookup"><span data-stu-id="6783d-2391">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="6783d-2392">**Set-AzApiManagementDiagnostic** - 글로벌 또는 API 범위에서 진단 엔터티 업데이트</span><span class="sxs-lookup"><span data-stu-id="6783d-2392">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="6783d-2393">ApiManagement 서비스에서 캐시를 관리하기 위한 새 cmdlet을 만들었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-2393">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="6783d-2394">**Get-AzApiManagementCache** - 식별자 또는 모든 캐시로 지정된 캐시의 세부 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="6783d-2394">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="6783d-2395">**New-AzApiManagementCache** - 특정 Azure 'region'(지역)에 새 'default'(기본) 캐시 만들기</span><span class="sxs-lookup"><span data-stu-id="6783d-2395">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="6783d-2396">**Remove-AzApiManagementCache** - 캐시 제거</span><span class="sxs-lookup"><span data-stu-id="6783d-2396">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="6783d-2397">**Update-AzApiManagementCache** - 캐시 업데이트</span><span class="sxs-lookup"><span data-stu-id="6783d-2397">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="6783d-2398">API 스키마 관리하기 위한 새 cmdlet을 만들었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-2398">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="6783d-2399">**New-AzApiManagementSchema** - API에 대한 새 스키마 만들기</span><span class="sxs-lookup"><span data-stu-id="6783d-2399">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="6783d-2400">**Get-AzApiManagementSchema** - API에 구성된 스키마 가져오기</span><span class="sxs-lookup"><span data-stu-id="6783d-2400">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="6783d-2401">**Remove-AzApiManagementSchema** - API에 구성된 스키마 제거</span><span class="sxs-lookup"><span data-stu-id="6783d-2401">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="6783d-2402">**Set-AzApiManagementSchema** - API에 구성된 스키마 업데이트</span><span class="sxs-lookup"><span data-stu-id="6783d-2402">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="6783d-2403">사용자 토큰을 생성하기 위한 새 cmdlet을 만들었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-2403">Created new Cmdlet for generating a User Token.</span></span>
    - <span data-ttu-id="6783d-2404">**New-AzApiManagementUserToken** - 기본적으로 8시간 동안 유효한 새 사용자 토큰을 생성합니다. 'GIT' 사용자에 대한 토큰은 이 cmdlet을 사용하여 생성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-2404">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="6783d-2405">네트워크 상태를 검색하기 위한 새 cmdlet을 만들었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-2405">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="6783d-2406">**Get-AzApiManagementNetworkStatus** - API Management 서비스에서 사용하는 리소스의 네트워크 상태 연결을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-2406">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="6783d-2407">ApiManagement 서비스를 가상 네트워크에 배포하고 종속성이 손상되었는지 여부를 확인할 때 유용합니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-2407">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="6783d-2408">**New-AzApiManagement** cmdlet에서 ApiManagement 서비스를 관리하도록 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-2408">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span>
    - <span data-ttu-id="6783d-2409">새 '소비' SKU 지원이 추가됨</span><span class="sxs-lookup"><span data-stu-id="6783d-2409">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="6783d-2410">'소비' SKU에 대해 'EnableClientCertificate' 플래그를 설정하기 위한 지원이 추가됨</span><span class="sxs-lookup"><span data-stu-id="6783d-2410">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="6783d-2411">새 **New-AzApiManagementSslSetting** cmdlet을 사용하면 'Backend(백 엔드)' 및 'Frontend'(프런트 엔드)에서 'TLS/SSL' 설정을 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-2411">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="6783d-2412">또한 ApiManagement 서비스의 'Frontend'에서 '3DES'와 같은 'Ciphers'와 'Http2'와 같은 'ServerProtocols'를 구성하는 데 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-2412">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="6783d-2413">ApiManagement 서비스에서 'DeveloperPortal' 호스트 이름을 구성하기 위한 지원이 추가됨</span><span class="sxs-lookup"><span data-stu-id="6783d-2413">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="6783d-2414">**Get-AzApiManagementSsoToken** cmdlet에서 'PsApiManagement' 개체를 입력으로 사용하도록 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-2414">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="6783d-2415">cmdlet에서 오류 메시지를 인라인으로 표시하도록 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-2415">Updated the cmdlet to display Error Messages inline</span></span>
     > <span data-ttu-id="6783d-2416">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : 오류 코드: ValidationError 오류 메시지: 하나 이상의 필드에 잘못된 값이 있습니다. 오류 세부 정보:    [Code=ValidationError, Message=줄 3, 열 10의 'log-to-eventhub' 요소에 오류가 있습니다.: 로거를 찾지 못함, Target=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="6783d-2416">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="6783d-2417">**Export-AzApiManagementApi** cmdlet에서 API를 'OpenApi 3.0' 형식으로 내보내도록 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-2417">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="6783d-2418">**Import-AzApiManagementApi** cmdlet을 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-2418">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="6783d-2419">'OpenApi 3.0' 문서 사양에서 API 가져오기</span><span class="sxs-lookup"><span data-stu-id="6783d-2419">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="6783d-2420">문서('Swagger', 'Wadl', 'Wsdl', 'OpenApi')에 지정된 'PsApiManagementSchema' 속성 재정의</span><span class="sxs-lookup"><span data-stu-id="6783d-2420">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="6783d-2421">문서에 지정된 'ServiceUrl' 속성 재정의</span><span class="sxs-lookup"><span data-stu-id="6783d-2421">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="6783d-2422">**Get-AzApiManagementPolicy** cmdlet에서 'rawxml'을 사용하여 이스케이프된 비 Xml 'format'(형식)의 정책을 반환하도록 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-2422">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="6783d-2423">**Set-AzApiManagementPolicy** cmdlet에서 'rawxml'을 사용하여 이스케이프된 비 Xml 'format'의 정책을 수락하고, 'xml'을 사용하여 이스케이프된 Xml 'format'의 정책을 수락하도록 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-2423">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="6783d-2424">**New-AzApiManagementApi** cmdlet을 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-2424">Updated cmdlet **New-AzApiManagementApi**</span></span>
    - <span data-ttu-id="6783d-2425">'OpenId' 권한 부여 서버를 사용하여 API 구성</span><span class="sxs-lookup"><span data-stu-id="6783d-2425">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="6783d-2426">'ApiVersionSet'에서 API 만들기</span><span class="sxs-lookup"><span data-stu-id="6783d-2426">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="6783d-2427">'SourceApiId' 및 'SourceApiRevision'을 사용하여 API 복제</span><span class="sxs-lookup"><span data-stu-id="6783d-2427">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="6783d-2428">API 범위에서 'SubscriptionRequired' 구성 가능</span><span class="sxs-lookup"><span data-stu-id="6783d-2428">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="6783d-2429">**Set-AzApiManagementApi** cmdlet을 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-2429">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="6783d-2430">'OpenId' 권한 부여 서버를 사용하여 API 구성</span><span class="sxs-lookup"><span data-stu-id="6783d-2430">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="6783d-2431">API를 'ApiVersionSet'으로 업데이트</span><span class="sxs-lookup"><span data-stu-id="6783d-2431">To updated an API into an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="6783d-2432">API 범위에서 'SubscriptionRequired' 구성 가능</span><span class="sxs-lookup"><span data-stu-id="6783d-2432">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="6783d-2433">**New-AzApiManagementRevision** cmdlet을 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-2433">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="6783d-2434">'SourceApiRevision'을 사용하여 기존 수정 버전 복제(태그, 제품, 작업 및 정책 복사).</span><span class="sxs-lookup"><span data-stu-id="6783d-2434">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="6783d-2435">새 수정 버전은 부모의 'ApiId'를 가정합니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-2435">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="6783d-2436">'ApiRevisionDescription' 제공</span><span class="sxs-lookup"><span data-stu-id="6783d-2436">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="6783d-2437">API 복제 시 'ServiceUrl' 재정의</span><span class="sxs-lookup"><span data-stu-id="6783d-2437">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="6783d-2438">**New-AzApiManagementIdentityProvider** cmdlet을 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-2438">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="6783d-2439">'Authority'를 사용하여 'AAD' 또는 'AADB2C' 구성</span><span class="sxs-lookup"><span data-stu-id="6783d-2439">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="6783d-2440">'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' 및 'PasswordResetPolicy' 설정</span><span class="sxs-lookup"><span data-stu-id="6783d-2440">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="6783d-2441">**New-AzApiManagementSubscription** cmdlet을 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-2441">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="6783d-2442">'Scope' 및 'UserId'를 사용하여 새 SubscriptonModel 설명</span><span class="sxs-lookup"><span data-stu-id="6783d-2442">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="6783d-2443">'ProductId' 및 'UserId'를 사용하여 이전 구독 모델 설명</span><span class="sxs-lookup"><span data-stu-id="6783d-2443">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="6783d-2444">구독 수준에서 'AllowTracing'을 사용하도록 설정하는 지원 추가</span><span class="sxs-lookup"><span data-stu-id="6783d-2444">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="6783d-2445">**Set-AzApiManagementSubscription** cmdlet을 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-2445">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="6783d-2446">'Scope' 및 'UserId'를 사용하여 새 SubscriptonModel 설명</span><span class="sxs-lookup"><span data-stu-id="6783d-2446">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="6783d-2447">'ProductId' 및 'UserId'를 사용하여 이전 구독 모델 설명</span><span class="sxs-lookup"><span data-stu-id="6783d-2447">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="6783d-2448">구독 수준에서 'AllowTracing'을 사용하도록 설정하는 지원 추가</span><span class="sxs-lookup"><span data-stu-id="6783d-2448">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="6783d-2449">다음 cmdlet에서 'ResourceId'를 입력으로 수락하도록 업데이트했습니다</span><span class="sxs-lookup"><span data-stu-id="6783d-2449">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="6783d-2450">'New-AzApiManagementContext'</span><span class="sxs-lookup"><span data-stu-id="6783d-2450">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="6783d-2451">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="6783d-2451">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="6783d-2452">'Get-AzApiManagementApiRelease'</span><span class="sxs-lookup"><span data-stu-id="6783d-2452">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="6783d-2453">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="6783d-2453">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="6783d-2454">'Get-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="6783d-2454">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="6783d-2455">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="6783d-2455">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="6783d-2456">'Get-AzApiManagementAuthorizationServer'</span><span class="sxs-lookup"><span data-stu-id="6783d-2456">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="6783d-2457">'Get-AzApiManagementBackend'</span><span class="sxs-lookup"><span data-stu-id="6783d-2457">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="6783d-2458">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="6783d-2458">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="6783d-2459">'Get-AzApiManagementCertificate'</span><span class="sxs-lookup"><span data-stu-id="6783d-2459">'Get-AzApiManagementCertificate'</span></span>
    - <span data-ttu-id="6783d-2460">'Remove-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="6783d-2460">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="6783d-2461">'Remove-AzApiManagementSubscription'</span><span class="sxs-lookup"><span data-stu-id="6783d-2461">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="6783d-2462">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="6783d-2462">Az.Automation</span></span>
* <span data-ttu-id="6783d-2463">Get-AzAutomationJobOutputRecord에서 JSON 및 Text 레코드 값을 처리하도록 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-2463">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="6783d-2464">문제 https://github.com/Azure/azure-powershell/issues/7977 수정</span><span class="sxs-lookup"><span data-stu-id="6783d-2464">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="6783d-2465">문제 https://github.com/Azure/azure-powershell/issues/8600 수정</span><span class="sxs-lookup"><span data-stu-id="6783d-2465">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="6783d-2466">Start-AzAutomationDscCompilationJob에서 완료될 때까지 기다리지 않고 작업을 바로 시작하도록 변경했습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-2466">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="6783d-2467">문제 https://github.com/Azure/azure-powershell/issues/8347 수정</span><span class="sxs-lookup"><span data-stu-id="6783d-2467">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="6783d-2468">-Name을 사용하면 모든 노드를 반환하는 Get-AzAutomationDscNode 수정.</span><span class="sxs-lookup"><span data-stu-id="6783d-2468">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="6783d-2469">이제 일치하는 노드만 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-2469">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6783d-2470">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6783d-2470">Az.Compute</span></span>
* <span data-ttu-id="6783d-2471">ProtectFromScaleIn 및 ProtectFromScaleSetAction 매개 변수를 Update-AzVmssVM cmdlet에 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-2471">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="6783d-2472">'East US'(미국 동부)가 지원되지 않는 경우 이제 New-AzVM wimple 매개 변수 집합에서 기본적으로 사용 가능한 위치를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-2472">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="6783d-2473">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="6783d-2473">Az.DataLakeStore</span></span>
* <span data-ttu-id="6783d-2474">ADLS SDK에서 httpclient를 사용하도록 업데이트하고, 데이터 평면 테스트를 Azure 프레임워크와 통합합니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-2474">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="6783d-2475">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="6783d-2475">Az.Monitor</span></span>
* <span data-ttu-id="6783d-2476">도움말 예제에서 잘못된 매개 변수 이름을 수정했습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-2476">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6783d-2477">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6783d-2477">Az.Network</span></span>
* <span data-ttu-id="6783d-2478">DisableBgpRoutePropagation 플래그를 유효 경로 테이블 출력에 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-2478">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="6783d-2479">업데이트된 cmdlet:</span><span class="sxs-lookup"><span data-stu-id="6783d-2479">Updated cmdlet:</span></span>
        - <span data-ttu-id="6783d-2480">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="6783d-2480">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="6783d-2481">New-AzApplicationGatewayTrustedRootCertificate 설명서에서 이중 파선을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-2481">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="6783d-2482">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6783d-2482">Az.Resources</span></span>
* <span data-ttu-id="6783d-2483">할당 거부를 검색하기 위한 새 Get-AzureRmDenyAssignment cmdlet을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-2483">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="6783d-2484">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6783d-2484">Az.Sql</span></span>
* <span data-ttu-id="6783d-2485">Advanced Threat Protection cmdlet의 이름을 Advanced Data Security로 변경하고, 취약성 평가를 기본적으로 사용하도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-2485">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="6783d-2486">2.0.0 - 2019년 5월</span><span class="sxs-lookup"><span data-stu-id="6783d-2486">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="6783d-2487">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6783d-2487">Az.Accounts</span></span>
* <span data-ttu-id="6783d-2488">사용자 이름/비밀번호 인증을 사용하여 ADFS 문제를 해결하도록 인증 라이브러리 업데이트</span><span class="sxs-lookup"><span data-stu-id="6783d-2488">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="6783d-2489">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="6783d-2489">Az.CognitiveServices</span></span>
* <span data-ttu-id="6783d-2490">Bing Search 서비스에 대해서만 Bing 면책 조항을 표시하세요.</span><span class="sxs-lookup"><span data-stu-id="6783d-2490">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="6783d-2491">계정 생성 실패 시 오류 개선.</span><span class="sxs-lookup"><span data-stu-id="6783d-2491">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6783d-2492">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6783d-2492">Az.Compute</span></span>
* <span data-ttu-id="6783d-2493">근접 배치 그룹 기능</span><span class="sxs-lookup"><span data-stu-id="6783d-2493">Proximity placement group feature.</span></span>
    - <span data-ttu-id="6783d-2494">다음과 같은 새 cmdlet을 추가했습니다.   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="6783d-2494">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="6783d-2495">새 매개 변수 ProximityPlacementGroupId가 다음 cmdlet에 추가됩니다.   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="6783d-2495">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="6783d-2496">New-AzGalleryImageVersion에 StorageAccountType 매개 변수가 추가됩니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-2496">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="6783d-2497">New-AzGalleryImageVersion의 TargetRegion이 StorageAccountType를 포함할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-2497">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="6783d-2498">SkipShutdown 스위치 매개 변수가 Stop-AzVM 및 Stop-AzVmss에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-2498">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>
* <span data-ttu-id="6783d-2499">주요 변경 내용</span><span class="sxs-lookup"><span data-stu-id="6783d-2499">Breaking changes</span></span>
    - <span data-ttu-id="6783d-2500">Set-AzVMBootDiagnostics이 Set-AzVMBootDiagnostic으로 변경됩니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-2500">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="6783d-2501">Export-AzLogAnalyticThrottledRequests이 Export-AzLogAnalyticThrottledRequests로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-2501">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="6783d-2502">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="6783d-2502">Az.DeploymentManager</span></span>
* <span data-ttu-id="6783d-2503">Azure 배포 관리자 cmdlet의 일반적으로 사용 가능한 첫 번째 릴리스</span><span class="sxs-lookup"><span data-stu-id="6783d-2503">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="6783d-2504">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="6783d-2504">Az.Dns</span></span>
* <span data-ttu-id="6783d-2505">자동 DNS 이름 서버 위임</span><span class="sxs-lookup"><span data-stu-id="6783d-2505">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="6783d-2506">DNS 영역 만들기 cmdlet은 추가 선택적 매개 변수로 부모 영역 이름을 허용합니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-2506">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="6783d-2507">새로 생성 된 자식 영역의 부모 영역에 NS 레코드를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-2507">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="6783d-2508">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="6783d-2508">Az.FrontDoor</span></span>
* <span data-ttu-id="6783d-2509">Azure FrontDoor cmdlet의 일반적으로 사용 가능한 첫 번째 릴리스</span><span class="sxs-lookup"><span data-stu-id="6783d-2509">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="6783d-2510">'Waf'를 포함하도록 WAF cmdlet의 이름 바꾸기</span><span class="sxs-lookup"><span data-stu-id="6783d-2510">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="6783d-2511">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="6783d-2511">Az.HDInsight</span></span>
* <span data-ttu-id="6783d-2512">두 개의 cmdlet을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-2512">Removed two cmdlets:</span></span>
    - <span data-ttu-id="6783d-2513">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="6783d-2513">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="6783d-2514">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="6783d-2514">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="6783d-2515">Grant-AzHDInsightHttpServicesAccess를 대체할 새 cmdlet Set-AzHDInsightGatewayCredential을 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-2515">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="6783d-2516">reader 역할과 HDInsight 운영자 역할을 구분하도록 cmdlet Get-AzHDInsightJobOutput 업데이트:</span><span class="sxs-lookup"><span data-stu-id="6783d-2516">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="6783d-2517">reader 역할을 가진 사용자는 'DefaultStorageAccountKey'매개 변수를 명시적으로 지정해야 합니다. 그렇지 않으면 오류가 발생합니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-2517">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="6783d-2518">Hdinsight 운영자 역할을 가진 사용자를 영향을 받지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-2518">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="6783d-2519">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="6783d-2519">Az.Monitor</span></span>
* <span data-ttu-id="6783d-2520">SQR API(예약 쿼리 규칙)용 새 cmdlet</span><span class="sxs-lookup"><span data-stu-id="6783d-2520">New cmdlets for SQR API (Scheduled Query Rule)</span></span>
    - <span data-ttu-id="6783d-2521">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="6783d-2521">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="6783d-2522">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="6783d-2522">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="6783d-2523">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="6783d-2523">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="6783d-2524">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="6783d-2524">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="6783d-2525">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="6783d-2525">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="6783d-2526">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="6783d-2526">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="6783d-2527">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="6783d-2527">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="6783d-2528">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="6783d-2528">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="6783d-2529">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="6783d-2529">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="6783d-2530">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="6783d-2530">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="6783d-2531">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="6783d-2531">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="6783d-2532">SQR API에 대한 [자세한 내용](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules)</span><span class="sxs-lookup"><span data-stu-id="6783d-2532">[More](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="6783d-2533">GenV2(비 클래식) 메트릭 기반 경고 규칙에 대한 cmdlet을 포함하도록 Az.Monitor.md가 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="6783d-2533">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6783d-2534">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6783d-2534">Az.Network</span></span>
* <span data-ttu-id="6783d-2535">Nat 게이트웨이 리소스에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="6783d-2535">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="6783d-2536">새로운 cmdlet</span><span class="sxs-lookup"><span data-stu-id="6783d-2536">New cmdlets</span></span>
        - <span data-ttu-id="6783d-2537">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="6783d-2537">New-AzNatGateway</span></span>
        - <span data-ttu-id="6783d-2538">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="6783d-2538">Get-AzNatGateway</span></span>
        - <span data-ttu-id="6783d-2539">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="6783d-2539">Set-AzNatGateway</span></span>
        - <span data-ttu-id="6783d-2540">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="6783d-2540">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="6783d-2541">다음 Cmdlet이 업데이트 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-2541">Updated cmdlets</span></span>
        - <span data-ttu-id="6783d-2542">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="6783d-2542">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="6783d-2543">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="6783d-2543">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="6783d-2544">기능에 대한 새로운 명령이 업데이트됨: Brooklyn Gateway에서 사용자 지정 경로 설정/제거.</span><span class="sxs-lookup"><span data-stu-id="6783d-2544">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="6783d-2545">New-AzVirtualNetworkGateway가 업데이트됨: 선택적 매개 변수 -CustomRoute를 추가하여 게이트웨이에서 설정할 사용자 지정 경로로 주소 접두사를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-2545">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="6783d-2546">Set-AzVirtualNetworkGateway가 업데이트됨: 선택적 매개 변수 -CustomRoute를 추가하여 게이트웨이에서 설정할 사용자 지정 경로로 주소 접두사를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-2546">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="6783d-2547">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="6783d-2547">Az.PolicyInsights</span></span>
* <span data-ttu-id="6783d-2548">정책 평가 세부 정보 쿼리 지원</span><span class="sxs-lookup"><span data-stu-id="6783d-2548">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="6783d-2549">Get-AzPolicyState에 '-Expand'매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="6783d-2549">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="6783d-2550">'-Expand PolicyEvaluationDetails' 지원</span><span class="sxs-lookup"><span data-stu-id="6783d-2550">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="6783d-2551">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="6783d-2551">Az.RecoveryServices</span></span>
* <span data-ttu-id="6783d-2552">크로스 구독 Azure에서 Azure 사이트 복구 지원</span><span class="sxs-lookup"><span data-stu-id="6783d-2552">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="6783d-2553">Azure Site Recovery에 대한 호환성이 손상되는 변경 표시</span><span class="sxs-lookup"><span data-stu-id="6783d-2553">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="6783d-2554">Azure Site Recovery 복구 계획 최종 실행 계획에 대한 수정</span><span class="sxs-lookup"><span data-stu-id="6783d-2554">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="6783d-2555">Azure에서 Azure에 대한 Azure Site Recovery 업데이트 네트워크 매핑 수정</span><span class="sxs-lookup"><span data-stu-id="6783d-2555">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="6783d-2556">관리 디스크에 대한 Azure에서 Azure에 대한 Azure Site Recovery 업데이트 보호 방향 수정</span><span class="sxs-lookup"><span data-stu-id="6783d-2556">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="6783d-2557">기타 사소한 수정.</span><span class="sxs-lookup"><span data-stu-id="6783d-2557">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="6783d-2558">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="6783d-2558">Az.Relay</span></span>
* <span data-ttu-id="6783d-2559">고객 관련 메시지의 철자 오류 수정</span><span class="sxs-lookup"><span data-stu-id="6783d-2559">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="6783d-2560">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="6783d-2560">Az.ServiceBus</span></span>
* <span data-ttu-id="6783d-2561">네임스페이스의 NetworkRuleSet에 대한 새 cmdlet가 추가되었습니다</span><span class="sxs-lookup"><span data-stu-id="6783d-2561">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="6783d-2562">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="6783d-2562">Az.Storage</span></span>
* <span data-ttu-id="6783d-2563">저장소 클라이언트 라이브러리 10.0.1로 업그레이드(이 SDK의 모든 개체의 네임스페이스가 'Microsoft.WindowsAzure.Storage. *'에서 'Microsoft.Azure.Storage.* '로 변경됨)</span><span class="sxs-lookup"><span data-stu-id="6783d-2563">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage. *' to 'Microsoft.Azure.Storage.* ')</span></span>
* <span data-ttu-id="6783d-2564">새로운 API 버전 2019-04-01을 지원하기 위해 Microsoft.Azure.Management.Storage 11.0.0으로 업그레이드합니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-2564">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="6783d-2565">스토리지 생성 계정의 기본 스토리지 계정 종류가 'Storage'에서 'StorageV2'로 변경됩니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-2565">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="6783d-2566">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6783d-2566">New-AzStorageAccount</span></span>
* <span data-ttu-id="6783d-2567">'StandardLRS'가 'Standard_LRS'로 변경되는 것과 같이 '-'을 추가하여 입력 SkuName과 정렬되도록 스토리지 계정 cmdlet 출력 Sku.Name을 변경합니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-2567">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="6783d-2568">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6783d-2568">New-AzStorageAccount</span></span>
    - <span data-ttu-id="6783d-2569">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6783d-2569">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="6783d-2570">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6783d-2570">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="6783d-2571">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="6783d-2571">Az.Websites</span></span>
* <span data-ttu-id="6783d-2572">Get-AzWebApp에서 반환한 PSSite 개체에 대해 'Kind'속성이 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-2572">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="6783d-2573">Get-AzWebApp\* 메트릭 및 Get-AzAppServicePlanMetrics가 사용되지 않음으로 표시되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-2573">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="6783d-2574">1.8.0 - 2019년 4월</span><span class="sxs-lookup"><span data-stu-id="6783d-2574">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="6783d-2575">마지막 주 릴리스 이후의 주요 사항</span><span class="sxs-lookup"><span data-stu-id="6783d-2575">Highlights since the last major release</span></span>
* <span data-ttu-id="6783d-2576">`Az` 모듈 일반 공급</span><span class="sxs-lookup"><span data-stu-id="6783d-2576">General availability of `Az` module</span></span>
* <span data-ttu-id="6783d-2577">`Az` 모듈에 대한 자세한 내용은 https://aka.ms/azps-announce 를 방문하세요.</span><span class="sxs-lookup"><span data-stu-id="6783d-2577">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="6783d-2578">Location, ResourceGroup 및 ResourceName 완성자가 추가되었습니다(https://azure.microsoft.com/blog/completers-in-azure-powershell/ ).</span><span class="sxs-lookup"><span data-stu-id="6783d-2578">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="6783d-2579">와일드카드 지원이 Az.Compute 및 Az.Network에 대한 Get cmdlet에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-2579">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="6783d-2580">Windows PowerShell 5.1 전용 대화형 사용자 이름/암호 인증이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-2580">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="6783d-2581">Python 2 Runbook 지원이 Az.Automation에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-2581">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="6783d-2582">Az.LogicApp: 통합 계정 어셈블리 및 일괄 처리 구성을 위한 새로운 cmdlet입니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-2582">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="6783d-2583">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6783d-2583">Az.Accounts</span></span>
* <span data-ttu-id="6783d-2584">Mac에서 모듈을 올바르게 삭제하기 위해 Uninstall-AzureRm을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-2584">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="6783d-2585">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="6783d-2585">Az.Batch</span></span>
* <span data-ttu-id="6783d-2586">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-2586">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="6783d-2587">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="6783d-2587">Az.Cdn</span></span>
* <span data-ttu-id="6783d-2588">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-2588">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="6783d-2589">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="6783d-2589">Az.CognitiveServices</span></span>
* <span data-ttu-id="6783d-2590">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-2590">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6783d-2591">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6783d-2591">Az.Compute</span></span>
* <span data-ttu-id="6783d-2592">디스크의 리소스 ID에 리소스 ID의 소문자 resourcegroups가 있는 경우 AEM 설치 문제 수정</span><span class="sxs-lookup"><span data-stu-id="6783d-2592">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="6783d-2593">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-2593">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="6783d-2594">와일드 카드에 대한 설명서 수정</span><span class="sxs-lookup"><span data-stu-id="6783d-2594">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="6783d-2595">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="6783d-2595">Az.DataFactory</span></span>
* <span data-ttu-id="6783d-2596">NodeCount가 관리형 통합 런타임에 대해 Null이 아닌 경우 SsisProperties를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-2596">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="6783d-2597">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="6783d-2597">Az.DataLakeStore</span></span>
* <span data-ttu-id="6783d-2598">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-2598">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="6783d-2599">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="6783d-2599">Az.EventGrid</span></span>
* <span data-ttu-id="6783d-2600">이벤트 구독 cmdlet 만들기/업데이트를 사용하기 전에 리소스를 만들어야 함을 나타내기 위해 엔드포인트의 도움말 텍스트가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-2600">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="6783d-2601">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="6783d-2601">Az.EventHub</span></span>
* <span data-ttu-id="6783d-2602">네임스페이스의 NetworkRuleSet에 대한 새 cmdlet가 추가되었습니다</span><span class="sxs-lookup"><span data-stu-id="6783d-2602">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="6783d-2603">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="6783d-2603">Az.HDInsight</span></span>
* <span data-ttu-id="6783d-2604">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-2604">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="6783d-2605">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="6783d-2605">Az.IotHub</span></span>
* <span data-ttu-id="6783d-2606">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-2606">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="6783d-2607">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="6783d-2607">Az.KeyVault</span></span>
* <span data-ttu-id="6783d-2608">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-2608">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="6783d-2609">와일드 카드에 대한 설명서 수정</span><span class="sxs-lookup"><span data-stu-id="6783d-2609">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="6783d-2610">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="6783d-2610">Az.MachineLearning</span></span>
* <span data-ttu-id="6783d-2611">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-2611">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="6783d-2612">Az.Media</span><span class="sxs-lookup"><span data-stu-id="6783d-2612">Az.Media</span></span>
* <span data-ttu-id="6783d-2613">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-2613">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="6783d-2614">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="6783d-2614">Az.Monitor</span></span>
  * <span data-ttu-id="6783d-2615">GenV2(비 클래식) 메트릭 기반 경고 규칙에 대한 새 cmdlet</span><span class="sxs-lookup"><span data-stu-id="6783d-2615">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="6783d-2616">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="6783d-2616">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="6783d-2617">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="6783d-2617">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="6783d-2618">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="6783d-2618">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="6783d-2619">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="6783d-2619">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="6783d-2620">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="6783d-2620">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="6783d-2621">모니터 SDK가 버전 0.22.0-preview로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-2621">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6783d-2622">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6783d-2622">Az.Network</span></span>
* <span data-ttu-id="6783d-2623">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-2623">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="6783d-2624">와일드 카드에 대한 설명서 수정</span><span class="sxs-lookup"><span data-stu-id="6783d-2624">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="6783d-2625">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="6783d-2625">Az.NotificationHubs</span></span>
* <span data-ttu-id="6783d-2626">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-2626">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="6783d-2627">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="6783d-2627">Az.OperationalInsights</span></span>
* <span data-ttu-id="6783d-2628">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-2628">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="6783d-2629">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="6783d-2629">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="6783d-2630">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-2630">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="6783d-2631">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="6783d-2631">Az.RecoveryServices</span></span>
* <span data-ttu-id="6783d-2632">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-2632">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="6783d-2633">Azure VM의 SQL용 테이블 형식이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-2633">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="6783d-2634">AzureFileShare에서 위치를 가져오는 대체 메서드가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-2634">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="6783d-2635">시간대에 따라 SchedulePolicy 개체의 ScheduleRunDays가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-2635">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="6783d-2636">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="6783d-2636">Az.RedisCache</span></span>
* <span data-ttu-id="6783d-2637">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-2637">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="6783d-2638">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6783d-2638">Az.Resources</span></span>
* <span data-ttu-id="6783d-2639">와일드 카드에 대한 설명서 수정</span><span class="sxs-lookup"><span data-stu-id="6783d-2639">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="6783d-2640">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6783d-2640">Az.Sql</span></span>
* <span data-ttu-id="6783d-2641">Monitor SDK의 종속성을 공용 코드로 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-2641">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="6783d-2642">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-2642">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="6783d-2643">다중 열 분류 프로세스가 향상되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-2643">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="6783d-2644">기본적으로 Get-AzSqlServerServiceObjective의 응답으로 SKU 속성(SKU 이름, 제품군, 용량)과 테이블 형식을 포함합니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-2644">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="6783d-2645">해당 지역에 기존 서버 없이 위치별로 Get-AzSqlServerServiceObjective를 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-2645">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="6783d-2646">관리형 인스턴스 생성 시 표준 시간대 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-2646">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="6783d-2647">와일드 카드에 대한 설명서 수정</span><span class="sxs-lookup"><span data-stu-id="6783d-2647">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="6783d-2648">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="6783d-2648">Az.Websites</span></span>
* <span data-ttu-id="6783d-2649">실행 시 태그를 제거하지 않도록 Set-AzWebApp 및 Set-AzWebAppSlot를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-2649">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="6783d-2650">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-2650">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="6783d-2651">WebSites SDK가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-2651">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="6783d-2652">PSAppServicePlan에서 AdminSiteName 속성을 제거했습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-2652">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="6783d-2653">1.7.0 - 2019년 4월</span><span class="sxs-lookup"><span data-stu-id="6783d-2653">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="6783d-2654">마지막 주 릴리스 이후의 주요 사항</span><span class="sxs-lookup"><span data-stu-id="6783d-2654">Highlights since the last major release</span></span>
* <span data-ttu-id="6783d-2655">`Az` 모듈 일반 공급</span><span class="sxs-lookup"><span data-stu-id="6783d-2655">General availability of `Az` module</span></span>
* <span data-ttu-id="6783d-2656">`Az` 모듈에 대한 자세한 내용은 https://aka.ms/azps-announce 를 방문하세요.</span><span class="sxs-lookup"><span data-stu-id="6783d-2656">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="6783d-2657">Location, ResourceGroup 및 ResourceName 완성자가 추가되었습니다(https://azure.microsoft.com/blog/completers-in-azure-powershell/ ).</span><span class="sxs-lookup"><span data-stu-id="6783d-2657">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="6783d-2658">와일드카드 지원이 Az.Compute 및 Az.Network에 대한 Get cmdlet에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-2658">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="6783d-2659">Windows PowerShell 5.1 전용 대화형 사용자 이름/암호 인증이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-2659">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="6783d-2660">Python 2 Runbook 지원이 Az.Automation에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-2660">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="6783d-2661">Az.LogicApp: 통합 계정 어셈블리 및 일괄 처리 구성을 위한 새로운 cmdlet입니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-2661">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="6783d-2662">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6783d-2662">Az.Accounts</span></span>
* <span data-ttu-id="6783d-2663">매개 변수 AzureAnalysisServicesEndpointResourceId를 허용하도록 Add-AzEnvironment 및 Set-AzEnvironment 업데이트</span><span class="sxs-lookup"><span data-stu-id="6783d-2663">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="6783d-2664">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="6783d-2664">Az.AnalysisServices</span></span>
* <span data-ttu-id="6783d-2665">데이터 평면 cmdlet에서 ServiceClient 사용 및 원본 인증 논리 제거</span><span class="sxs-lookup"><span data-stu-id="6783d-2665">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="6783d-2666">호환성이 손상되는 변경을 방지하기 위해 Add-AzureASAccount를 Connect-AzAccount의 래퍼로 만듦</span><span class="sxs-lookup"><span data-stu-id="6783d-2666">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="6783d-2667">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="6783d-2667">Az.Automation</span></span>
* <span data-ttu-id="6783d-2668">포함에 대한 New-AzAutomationSoftwareUpdateConfiguration cmdlet 버그 수정</span><span class="sxs-lookup"><span data-stu-id="6783d-2668">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="6783d-2669">이제 매개 변수 IncludedKbNumber 및 IncludedPackageNameMask가 작동함</span><span class="sxs-lookup"><span data-stu-id="6783d-2669">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="6783d-2670">Azure 자동화 업데이트 관리 동적 그룹에 대한 버그 수정</span><span class="sxs-lookup"><span data-stu-id="6783d-2670">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6783d-2671">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6783d-2671">Az.Compute</span></span>
* <span data-ttu-id="6783d-2672">New-AzDiskConfig 및 New-AzSnapshotConfig에 HyperVGeneration 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="6783d-2672">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="6783d-2673">다른 테넌트의 갤러리 이미지를 사용하여 VM을 만들 수 있음</span><span class="sxs-lookup"><span data-stu-id="6783d-2673">Allow VM creation with galley image from other tenants.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="6783d-2674">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="6783d-2674">Az.ContainerInstance</span></span>
* <span data-ttu-id="6783d-2675">후행 빈 인수를 추가한 New-AzContainerGroup의 -Command 매개 변수의 문제 수정</span><span class="sxs-lookup"><span data-stu-id="6783d-2675">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="6783d-2676">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="6783d-2676">Az.DataFactory</span></span>
* <span data-ttu-id="6783d-2677">ADF .Net SDK 버전을 3.0.2로 업데이트</span><span class="sxs-lookup"><span data-stu-id="6783d-2677">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="6783d-2678">RepoConfiguration 관련 설정에 대한 추가 매개 변수로 Set-AzDataFactoryV2 cmdlet을 업데이트</span><span class="sxs-lookup"><span data-stu-id="6783d-2678">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="6783d-2679">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6783d-2679">Az.Resources</span></span>
* <span data-ttu-id="6783d-2680">'-ResourceId' 또는 '-ResourceGroupName', '-Name' 및 '-ResourceType' 매개 변수를 제공할 때 'Get-AzResource'에 대한 공급자 처리 개선</span><span class="sxs-lookup"><span data-stu-id="6783d-2680">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="6783d-2681">'Test-AzDeployment' 및 'Test-AzResourceGroupDeployment'에 대한 오류 처리 개선</span><span class="sxs-lookup"><span data-stu-id="6783d-2681">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="6783d-2682">배포 유효성 검사 외부에서 발생한 오류를 처리하고 그 대신 명령의 출력에 포함</span><span class="sxs-lookup"><span data-stu-id="6783d-2682">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="6783d-2683">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/6856 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="6783d-2683">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="6783d-2684">배포 cmdlet 세트에 스크립트 및 작업 시나리오에서 프롬프트를 건너뛰는 '-IgnoreDynamicParameters' 스위치 추가</span><span class="sxs-lookup"><span data-stu-id="6783d-2684">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="6783d-2685">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/6856 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="6783d-2685">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="6783d-2686">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6783d-2686">Az.Sql</span></span>
* <span data-ttu-id="6783d-2687">데이터베이스 데이터 분류 지원</span><span class="sxs-lookup"><span data-stu-id="6783d-2687">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="6783d-2688">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="6783d-2688">Az.Storage</span></span>
* <span data-ttu-id="6783d-2689">매개 변수 -UseConnectedAccount를 사용하여 스토리지 컨텍스트를 만들 때 자세한 오류 보고(단, 로그인 Azure 계정 없이)</span><span class="sxs-lookup"><span data-stu-id="6783d-2689">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="6783d-2690">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="6783d-2690">New-AzStorageContext</span></span>
* <span data-ttu-id="6783d-2691">관리 평면 API를 사용하여 지정한 스토리지 계정의 BLOB 서비스 속성 관리 지원</span><span class="sxs-lookup"><span data-stu-id="6783d-2691">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="6783d-2692">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="6783d-2692">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="6783d-2693">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="6783d-2693">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="6783d-2694">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="6783d-2694">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="6783d-2695">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="6783d-2695">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="6783d-2696">BLOB 및 파일 업로드/다운로드 cmdlet에 대한 -AsJob 지원</span><span class="sxs-lookup"><span data-stu-id="6783d-2696">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="6783d-2697">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="6783d-2697">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="6783d-2698">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="6783d-2698">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="6783d-2699">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="6783d-2699">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="6783d-2700">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="6783d-2700">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="6783d-2701">1.6.0 - 2019년 3월</span><span class="sxs-lookup"><span data-stu-id="6783d-2701">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="6783d-2702">마지막 주 릴리스 이후의 주요 사항</span><span class="sxs-lookup"><span data-stu-id="6783d-2702">Highlights since the last major release</span></span>
* <span data-ttu-id="6783d-2703">`Az` 모듈 일반 공급</span><span class="sxs-lookup"><span data-stu-id="6783d-2703">General availability of `Az` module</span></span>
* <span data-ttu-id="6783d-2704">`Az` 모듈에 대한 자세한 내용은 https://aka.ms/azps-announce 를 방문하세요.</span><span class="sxs-lookup"><span data-stu-id="6783d-2704">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="6783d-2705">Location, ResourceGroup 및 ResourceName 완성자가 추가되었습니다(https://azure.microsoft.com/blog/completers-in-azure-powershell/ ).</span><span class="sxs-lookup"><span data-stu-id="6783d-2705">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="6783d-2706">와일드카드 지원이 Az.Compute 및 Az.Network에 대한 Get cmdlet에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-2706">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="6783d-2707">Windows PowerShell 5.1 전용 대화형 사용자 이름/암호 인증이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-2707">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="6783d-2708">Python 2 Runbook 지원이 Az.Automation에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-2708">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="6783d-2709">Az.LogicApp: 통합 계정 어셈블리 및 일괄 처리 구성을 위한 새로운 cmdlet입니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-2709">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="6783d-2710">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="6783d-2710">Az.Automation</span></span>
* <span data-ttu-id="6783d-2711">Azure 자동화 업데이트 관리에서 변경된 지원 기능은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-2711">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="6783d-2712">동적 그룹화</span><span class="sxs-lookup"><span data-stu-id="6783d-2712">Dynamic grouping</span></span>
    * <span data-ttu-id="6783d-2713">사전 스크립트</span><span class="sxs-lookup"><span data-stu-id="6783d-2713">Pre-Post script</span></span>
    * <span data-ttu-id="6783d-2714">다시 부팅 설정</span><span class="sxs-lookup"><span data-stu-id="6783d-2714">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6783d-2715">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6783d-2715">Az.Compute</span></span>
* <span data-ttu-id="6783d-2716">Get-AzVmBootDiagnosticsData의 경로 확인 문제가 해결되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-2716">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="6783d-2717">Compute 클라이언트 라이브러리가 25.0.0으로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-2717">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="6783d-2718">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="6783d-2718">Az.KeyVault</span></span>
* <span data-ttu-id="6783d-2719">와일드카드 지원이 KeyVault cmdlet에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-2719">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6783d-2720">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6783d-2720">Az.Network</span></span>
* <span data-ttu-id="6783d-2721">Azure Firewall에 대한 위협 인텔리전스 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-2721">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="6783d-2722">Application Gateway 방화벽 정책의 최상위 수준 리소스 및 사용자 지정 규칙이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-2722">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="6783d-2723">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="6783d-2723">Az.RecoveryServices</span></span>
* <span data-ttu-id="6783d-2724">인스턴트 RP를 지원하기 위해 SnapshotRetentionInDays가 Azure VM 정책에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-2724">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="6783d-2725">컨테이너 등록을 취소하는 파이프 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-2725">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="6783d-2726">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6783d-2726">Az.Resources</span></span>
* <span data-ttu-id="6783d-2727">Get-AzResource 및 Get-AzResourceGroup에 대한 와일드카드 지원을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-2727">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="6783d-2728">ARM에 대한 일반 호출을 수행할 때 사용되는 자격 증명을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-2728">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="6783d-2729">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6783d-2729">Az.Sql</span></span>
* <span data-ttu-id="6783d-2730">위협 탐지의 cmdlet 매개 변수(ExcludeDetectionType)가 DetectionType에서 string[]으로 변경되어 새 DetectionType이 추가되면 이후의 증명이 되고 자동 완성도 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-2730">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="6783d-2731">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="6783d-2731">Az.Storage</span></span>
* <span data-ttu-id="6783d-2732">스토리지 계정에 대한 관리 정책 가져오기/설정/제거를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-2732">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="6783d-2733">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="6783d-2733">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="6783d-2734">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="6783d-2734">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="6783d-2735">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="6783d-2735">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="6783d-2736">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="6783d-2736">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="6783d-2737">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="6783d-2737">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="6783d-2738">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="6783d-2738">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="6783d-2739">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="6783d-2739">Az.Websites</span></span>
* <span data-ttu-id="6783d-2740">'New-AzWebApp -IncludeSourceWebAppSlots'를 사용하여 모든 슬롯의 복제를 중단하는 ARM 템플릿 버그가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-2740">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span>

## <a name="150---march-2019"></a><span data-ttu-id="6783d-2741">1.5.0 - 2019년 3월</span><span class="sxs-lookup"><span data-stu-id="6783d-2741">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="6783d-2742">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6783d-2742">Az.Accounts</span></span>
* <span data-ttu-id="6783d-2743">'Register-AzModule' 명령을 추가하여 AutoRest 생성 cmdlet을 지원</span><span class="sxs-lookup"><span data-stu-id="6783d-2743">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="6783d-2744">Connect-AzAccount 예제 업데이트</span><span class="sxs-lookup"><span data-stu-id="6783d-2744">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="6783d-2745">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="6783d-2745">Az.Automation</span></span>
* <span data-ttu-id="6783d-2746">몇몇 Azure Automation cmdlet에서 특정 월별 일정을 검색할 때 발생하는 문제 수정</span><span class="sxs-lookup"><span data-stu-id="6783d-2746">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="6783d-2747">상위 20개 노드를 반환하도록 Get-AzAutomationDscNode를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-2747">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="6783d-2748">이제 모든 노드 반환</span><span class="sxs-lookup"><span data-stu-id="6783d-2748">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="6783d-2749">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="6783d-2749">Az.Cdn</span></span>
* <span data-ttu-id="6783d-2750">사용자 지정 도메인 Https 사용/사용 안 함에 대한 새 Powershell cmdlet이 추가되었으며 기존의 것은 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-2750">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6783d-2751">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6783d-2751">Az.Compute</span></span>
* <span data-ttu-id="6783d-2752">Get cmdlet에 와일드 카드 지원 추가</span><span class="sxs-lookup"><span data-stu-id="6783d-2752">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="6783d-2753">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="6783d-2753">Az.DataFactory</span></span>
* <span data-ttu-id="6783d-2754">ADF.Net SDK 버전이 3.0.1로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-2754">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="6783d-2755">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="6783d-2755">Az.LogicApp</span></span>
* <span data-ttu-id="6783d-2756">첫 결과 페이지 검색 시에만 ListWorkflows 수정</span><span class="sxs-lookup"><span data-stu-id="6783d-2756">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6783d-2757">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6783d-2757">Az.Network</span></span>
* <span data-ttu-id="6783d-2758">Network cmdlet에 와일드 카드 지원 추가</span><span class="sxs-lookup"><span data-stu-id="6783d-2758">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="6783d-2759">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="6783d-2759">Az.RecoveryServices</span></span>
* <span data-ttu-id="6783d-2760">Azure VM 지원에 SQL 서버가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-2760">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="6783d-2761">SDK 업데이트</span><span class="sxs-lookup"><span data-stu-id="6783d-2761">SDK Update</span></span>
* <span data-ttu-id="6783d-2762">VMappContainer 체크 인 Get-ProtectableItem 제거</span><span class="sxs-lookup"><span data-stu-id="6783d-2762">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="6783d-2763">Get ProtectableItem의 매개 변수로 Name과 ServerName이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-2763">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="6783d-2764">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6783d-2764">Az.Resources</span></span>
* <span data-ttu-id="6783d-2765">`-TemplateObject` 매개 변수를 추가하여 cmdlet을 배포</span><span class="sxs-lookup"><span data-stu-id="6783d-2765">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="6783d-2766">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/2933 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="6783d-2766">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="6783d-2767">`Get-AzResource`의 결과를 `Set-AzResource`(으)로 파이프할 때 발생하는 문제 수정</span><span class="sxs-lookup"><span data-stu-id="6783d-2767">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="6783d-2768">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/8240 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="6783d-2768">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="6783d-2769">실행 시 JSON 데이터 형식 문제 해결 `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="6783d-2769">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="6783d-2770">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/7930 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="6783d-2770">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="6783d-2771">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6783d-2771">Az.Sql</span></span>
* <span data-ttu-id="6783d-2772">AuditingEndpointsCommunicator를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-2772">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="6783d-2773">새 진단 설정을 생성할 때 에지 사례의 동작을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-2773">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="6783d-2774">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="6783d-2774">Az.Storage</span></span>
* <span data-ttu-id="6783d-2775">스토리지 계정      - New-AzStorageAccount를 생성할 때 종류 BlockBlobStorage를 지원</span><span class="sxs-lookup"><span data-stu-id="6783d-2775">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="6783d-2776">1.4.0 - 2019년 2월</span><span class="sxs-lookup"><span data-stu-id="6783d-2776">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="6783d-2777">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="6783d-2777">Az.AnalysisServices</span></span>
* <span data-ttu-id="6783d-2778">사용되지 않는 AddAzureASAccount cmdlet</span><span class="sxs-lookup"><span data-stu-id="6783d-2778">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="6783d-2779">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="6783d-2779">Az.Automation</span></span>
* <span data-ttu-id="6783d-2780">Import-AzAutomationDscNodeConfiguration 도움말 업데이트</span><span class="sxs-lookup"><span data-stu-id="6783d-2780">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="6783d-2781">Import-AzAutomationDscConfiguration cmdlet 구성 이름 유효성 검사 추가</span><span class="sxs-lookup"><span data-stu-id="6783d-2781">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="6783d-2782">Import-AzAutomationDscConfiguration cmdlet 오류 처리 개선</span><span class="sxs-lookup"><span data-stu-id="6783d-2782">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="6783d-2783">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="6783d-2783">Az.CognitiveServices</span></span>
* <span data-ttu-id="6783d-2784">리소스의 하위 도메인을 지정하는 데 사용되는 New-AzCognitiveServicesAccount에 대한 새 선택적 매개 변수로 CustomSubdomainName이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-2784">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6783d-2785">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6783d-2785">Az.Compute</span></span>
* <span data-ttu-id="6783d-2786">ID 매개 변수 집합 문제 해결</span><span class="sxs-lookup"><span data-stu-id="6783d-2786">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="6783d-2787">Name 매개 변수를 제공하지 않으면 Get-AzVMExtension이 설치된 모든 확장을 열거하도록 업데이트</span><span class="sxs-lookup"><span data-stu-id="6783d-2787">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="6783d-2788">Update-AzImage cmdlet에 태그 및 ResourceId 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="6783d-2788">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="6783d-2789">인스턴스 ID가 없는 Get-AzVmssVM과 InstanceView를 사용하면 인스턴스 보기가 있는 VMSS VM을 나열할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-2789">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="6783d-2790">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="6783d-2790">Az.DataLakeStore</span></span>
* <span data-ttu-id="6783d-2791">ADL 삭제된 항목 열거 및 복원에 대한 cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="6783d-2791">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="6783d-2792">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="6783d-2792">Az.EventHub</span></span>
* <span data-ttu-id="6783d-2793">Eventhub의 CaptureDescription 클래스에서 빈 보관을 건너뛰는 새 부울 속성 SkipEmptyArchives가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-2793">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="6783d-2794">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="6783d-2794">Az.KeyVault</span></span>
* <span data-ttu-id="6783d-2795">Set-AzKeyVaultSecret 태그 지정 수정</span><span class="sxs-lookup"><span data-stu-id="6783d-2795">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="6783d-2796">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="6783d-2796">Az.LogicApp</span></span>
* <span data-ttu-id="6783d-2797">통합 계정에 대한 기본 sku 추가</span><span class="sxs-lookup"><span data-stu-id="6783d-2797">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="6783d-2798">XSLT 2.0, XSLT 3.0, Liquid 맵 형식 추가</span><span class="sxs-lookup"><span data-stu-id="6783d-2798">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="6783d-2799">통합 계정 어셈블리에 대한 새 cmdlet</span><span class="sxs-lookup"><span data-stu-id="6783d-2799">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="6783d-2800">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="6783d-2800">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="6783d-2801">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="6783d-2801">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="6783d-2802">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="6783d-2802">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="6783d-2803">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="6783d-2803">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="6783d-2804">통합 계정 일괄 처리 구성에 대한 새 cmdlet</span><span class="sxs-lookup"><span data-stu-id="6783d-2804">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="6783d-2805">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="6783d-2805">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="6783d-2806">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="6783d-2806">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="6783d-2807">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="6783d-2807">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="6783d-2808">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="6783d-2808">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="6783d-2809">논리 앱 SDK를 버전 4.1.0으로 업데이트</span><span class="sxs-lookup"><span data-stu-id="6783d-2809">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="6783d-2810">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="6783d-2810">Az.Monitor</span></span>
* <span data-ttu-id="6783d-2811">Get-AzMetric에 대한 도움말 업데이트</span><span class="sxs-lookup"><span data-stu-id="6783d-2811">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6783d-2812">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6783d-2812">Az.Network</span></span>
* <span data-ttu-id="6783d-2813">Add-AzApplicationGatewayCustomError에 대한 도움말 예제 업데이트</span><span class="sxs-lookup"><span data-stu-id="6783d-2813">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="6783d-2814">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="6783d-2814">Az.OperationalInsights</span></span>
* <span data-ttu-id="6783d-2815">New 및 Get ApplicationInsights 데이터 소스에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="6783d-2815">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="6783d-2816">지정된 작업 영역에 대한 특정 또는 전체 ApplicationInsights 데이터 원본 가져오기를 지원하기 위한 새로운 'ApplicationInsights' 종류가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-2816">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span>
    - <span data-ttu-id="6783d-2817">지정된 Application-Insights 리소스 매개 변수(구독 ID, resourceGroupName 및 이름)별로 데이터 원본을 만들기 위한 New-AzOperationalInsightsApplicationInsightsDataSource cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-2817">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span>

#### <a name="azresources"></a><span data-ttu-id="6783d-2818">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6783d-2818">Az.Resources</span></span>
* <span data-ttu-id="6783d-2819">문제 https://github.com/Azure/azure-powershell/issues/8166 수정</span><span class="sxs-lookup"><span data-stu-id="6783d-2819">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="6783d-2820">문제 https://github.com/Azure/azure-powershell/issues/8235 수정</span><span class="sxs-lookup"><span data-stu-id="6783d-2820">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="6783d-2821">문제 https://github.com/Azure/azure-powershell/issues/6219 수정</span><span class="sxs-lookup"><span data-stu-id="6783d-2821">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="6783d-2822">KeyCredentials 반복 만들기를 방지하기 위해 버그 수정</span><span class="sxs-lookup"><span data-stu-id="6783d-2822">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="6783d-2823">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6783d-2823">Az.Sql</span></span>
* <span data-ttu-id="6783d-2824">SQL DB 하이퍼스케일에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="6783d-2824">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="6783d-2825">복원 요청에서 불필요한 속성을 설정하여 복원이 실패할 수 있는 버그 수정</span><span class="sxs-lookup"><span data-stu-id="6783d-2825">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="6783d-2826">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="6783d-2826">Az.Websites</span></span>
* <span data-ttu-id="6783d-2827">Get-AzWebAppSlotMetrics 내 올바른 예제</span><span class="sxs-lookup"><span data-stu-id="6783d-2827">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="6783d-2828">1.3.0 - 2019년 2월</span><span class="sxs-lookup"><span data-stu-id="6783d-2828">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="6783d-2829">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6783d-2829">Az.Accounts</span></span>
* <span data-ttu-id="6783d-2830">ClientRuntime 최신 버전 업데이트</span><span class="sxs-lookup"><span data-stu-id="6783d-2830">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="6783d-2831">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="6783d-2831">Az.AnalysisServices</span></span>
<span data-ttu-id="6783d-2832">Az.AnalysisServices 모듈의 전반적인 가용성.</span><span class="sxs-lookup"><span data-stu-id="6783d-2832">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6783d-2833">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6783d-2833">Az.Compute</span></span>
* <span data-ttu-id="6783d-2834">AEM 확장: UltraSSD 및 P60, P70, P80 디스크에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="6783d-2834">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="6783d-2835">Set-AzVMBootDiagnostics에 대한 도움말 업데이트</span><span class="sxs-lookup"><span data-stu-id="6783d-2835">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="6783d-2836">Update-AzImage에 대한 도움말 및 예제 업데이트</span><span class="sxs-lookup"><span data-stu-id="6783d-2836">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="6783d-2837">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="6783d-2837">Az.RecoveryServices</span></span>
<span data-ttu-id="6783d-2838">Az.RecoveryServices 모듈의 전반적인 가용성.</span><span class="sxs-lookup"><span data-stu-id="6783d-2838">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="6783d-2839">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6783d-2839">Az.Resources</span></span>
* <span data-ttu-id="6783d-2840">리소스 그룹 관련 태그 수정</span><span class="sxs-lookup"><span data-stu-id="6783d-2840">Fix tagging for resource groups</span></span>
    - <span data-ttu-id="6783d-2841">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/8166 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="6783d-2841">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="6783d-2842">`Get-AzureRmRoleAssignment`이(가) -ErrorAction을 준수하지 않는 문제 수정</span><span class="sxs-lookup"><span data-stu-id="6783d-2842">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span>
    - <span data-ttu-id="6783d-2843">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/8235 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="6783d-2843">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="6783d-2844">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6783d-2844">Az.Sql</span></span>
* <span data-ttu-id="6783d-2845">AzSqlDatabaseBackupShortTermRetentionPolicy 가져오기/설정하기 추가</span><span class="sxs-lookup"><span data-stu-id="6783d-2845">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="6783d-2846">SQL cmdlet을 실행할 경우 Azure 계정에 로그인되어 있지 않은 것이 nullref 예외를 초래하는 문제 수정</span><span class="sxs-lookup"><span data-stu-id="6783d-2846">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="6783d-2847">Get-AzSqlCapability의 nullref 예외 수정</span><span class="sxs-lookup"><span data-stu-id="6783d-2847">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="6783d-2848">1.2.1 - 2019년 1월</span><span class="sxs-lookup"><span data-stu-id="6783d-2848">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="6783d-2849">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6783d-2849">Az.Accounts</span></span>
* <span data-ttu-id="6783d-2850">올바른 인증 버전을 사용하여 릴리스</span><span class="sxs-lookup"><span data-stu-id="6783d-2850">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="6783d-2851">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="6783d-2851">Az.AnalysisServices</span></span>
* <span data-ttu-id="6783d-2852">업데이트된 인증 종속성을 사용하여 릴리스</span><span class="sxs-lookup"><span data-stu-id="6783d-2852">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="6783d-2853">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="6783d-2853">Az.RecoveryServices</span></span>
* <span data-ttu-id="6783d-2854">업데이트된 인증 종속성을 사용하여 릴리스</span><span class="sxs-lookup"><span data-stu-id="6783d-2854">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="6783d-2855">1.2.0 - 2019년 1월</span><span class="sxs-lookup"><span data-stu-id="6783d-2855">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="6783d-2856">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6783d-2856">Az.Accounts</span></span>
* <span data-ttu-id="6783d-2857">Windows PowerShell 5.1 전용 대화형 사용자 이름/암호 인증 추가</span><span class="sxs-lookup"><span data-stu-id="6783d-2857">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="6783d-2858">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="6783d-2858">Update incorrect online help URLs</span></span>
* <span data-ttu-id="6783d-2859">Uninstall-AzureRm 관련 PS Core에 경고 메시지 추가</span><span class="sxs-lookup"><span data-stu-id="6783d-2859">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="6783d-2860">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="6783d-2860">Az.Aks</span></span>
* <span data-ttu-id="6783d-2861">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="6783d-2861">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="6783d-2862">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="6783d-2862">Az.Automation</span></span>
* <span data-ttu-id="6783d-2863">Python 2 Runbook에 대한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-2863">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="6783d-2864">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="6783d-2864">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="6783d-2865">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="6783d-2865">Az.Cdn</span></span>
* <span data-ttu-id="6783d-2866">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="6783d-2866">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6783d-2867">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6783d-2867">Az.Compute</span></span>
* <span data-ttu-id="6783d-2868">Invoke-AzVMReimage cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="6783d-2868">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="6783d-2869">Set-AzVmss에 TempDisk 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="6783d-2869">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="6783d-2870">New-AzVM 경고 메시지 수정</span><span class="sxs-lookup"><span data-stu-id="6783d-2870">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="6783d-2871">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="6783d-2871">Az.ContainerRegistry</span></span>
* <span data-ttu-id="6783d-2872">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="6783d-2872">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="6783d-2873">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="6783d-2873">Az.DataFactory</span></span>
* <span data-ttu-id="6783d-2874">ADF.Net SDK 버전이 3.0.0으로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-2874">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="6783d-2875">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="6783d-2875">Az.DataLakeStore</span></span>
* <span data-ttu-id="6783d-2876">MSI를 사용할 때 ADLS 엔드포인트 문제 수정</span><span class="sxs-lookup"><span data-stu-id="6783d-2876">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="6783d-2877">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/7462 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="6783d-2877">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="6783d-2878">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="6783d-2878">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="6783d-2879">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="6783d-2879">Az.IotHub</span></span>
* <span data-ttu-id="6783d-2880">Add-IotHubRoutingEndpoint cmdlet에 인코딩 형식을 추가하세요.</span><span class="sxs-lookup"><span data-stu-id="6783d-2880">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="6783d-2881">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="6783d-2881">Az.KeyVault</span></span>
* <span data-ttu-id="6783d-2882">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="6783d-2882">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6783d-2883">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6783d-2883">Az.Network</span></span>
* <span data-ttu-id="6783d-2884">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="6783d-2884">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="6783d-2885">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6783d-2885">Az.Resources</span></span>
* <span data-ttu-id="6783d-2886">'New-AzADAppCredential' 및 'New-AzADSpCredential' 참조 설명서의 잘못된 예제 수정</span><span class="sxs-lookup"><span data-stu-id="6783d-2886">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="6783d-2887">리소스 그룹 배포 cmdlet 실행 전 '-TemplateFile' 매개 변수 경로가 확인되지 않는 문제 수정</span><span class="sxs-lookup"><span data-stu-id="6783d-2887">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="6783d-2888">Az.Resources: New-AzureRmPolicyDefinition -Mode 기본값에 대한 올바른 설명서</span><span class="sxs-lookup"><span data-stu-id="6783d-2888">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="6783d-2889">Az.Resources: 문제 https://github.com/Azure/azure-powershell/issues/7522 수정</span><span class="sxs-lookup"><span data-stu-id="6783d-2889">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="6783d-2890">Az.Resources: 문제 https://github.com/Azure/azure-powershell/issues/5747 수정</span><span class="sxs-lookup"><span data-stu-id="6783d-2890">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="6783d-2891">'PSResourceGroupDeployment' 개체의 서식 문제 수정</span><span class="sxs-lookup"><span data-stu-id="6783d-2891">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="6783d-2892">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/2123 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="6783d-2892">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="6783d-2893">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="6783d-2893">Az.ServiceFabric</span></span>
* <span data-ttu-id="6783d-2894">인증서가 VMSS 모델에 추가되었는데도 예외가 발생할 경우 롤백합니다. 이는 버그 https://github.com/Azure/service-fabric-issues/issues/932 를 수정하기 위함입니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-2894">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="6783d-2895">일부 오류 메시지를 수정하세요.</span><span class="sxs-lookup"><span data-stu-id="6783d-2895">Fix some error messages.</span></span>
* <span data-ttu-id="6783d-2896">Az로의 마이그레이션을 통해서는 작동하지 않는 New-AzServiceFabriCluster를 위해 기본값 ARM 템플릿을 가진 클러스터 만들기를 수정하세요.</span><span class="sxs-lookup"><span data-stu-id="6783d-2896">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="6783d-2897">확장에서 클러스터 id를 확인하여 클러스터에 해당하는 VMSS에만 추가되도록 클러스터/애플리케이션 인증서 추가를 수정하세요.</span><span class="sxs-lookup"><span data-stu-id="6783d-2897">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="6783d-2898">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="6783d-2898">Az.SignalR</span></span>
* <span data-ttu-id="6783d-2899">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="6783d-2899">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="6783d-2900">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6783d-2900">Az.Sql</span></span>
* <span data-ttu-id="6783d-2901">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="6783d-2901">Update incorrect online help URLs</span></span>
* <span data-ttu-id="6783d-2902">가능한 값을 가진 LicenseType 매개 변수에 대한 매개 변수 설명이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-2902">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="6783d-2903">유일하게 업데이트된 속성인데 작동하지 않는 관리되는 인스턴스 ID의 업데이트 수정</span><span class="sxs-lookup"><span data-stu-id="6783d-2903">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="6783d-2904">관리되는 인스턴스에서의 사용자 지정 데이터 정렬에 대한 지원</span><span class="sxs-lookup"><span data-stu-id="6783d-2904">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="6783d-2905">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="6783d-2905">Az.Storage</span></span>
* <span data-ttu-id="6783d-2906">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="6783d-2906">Update incorrect online help URLs</span></span>
* <span data-ttu-id="6783d-2907">Premium Storage 계정이 클래식 로깅/메트릭을 지원하지 않기 때문에, Premium Storage 계정의 클래식 로깅/메트릭을 가져올/설정할 때 상세한 오류 메시지를 제공해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-2907">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="6783d-2908">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="6783d-2908">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="6783d-2909">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="6783d-2909">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="6783d-2910">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="6783d-2910">Az.TrafficManager</span></span>
* <span data-ttu-id="6783d-2911">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="6783d-2911">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="6783d-2912">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="6783d-2912">Az.Websites</span></span>
* <span data-ttu-id="6783d-2913">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="6783d-2913">Update incorrect online help URLs</span></span>
* <span data-ttu-id="6783d-2914">앱이 ASE에 호스팅되면 'New-AzWebAppSSLBinding'을 수정하여 올바른 resourcegroup+location에 인증서를 업로드합니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-2914">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="6783d-2915">'New-AzWebAppSSLBinding'을 수정하여 SSL 인증서를 앱에 바인딩하는 데 붙는 태그를 덮어쓰지 않도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-2915">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="6783d-2916">1.1.0 - 2019년 1월</span><span class="sxs-lookup"><span data-stu-id="6783d-2916">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="6783d-2917">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6783d-2917">Az.Accounts</span></span>
* <span data-ttu-id="6783d-2918">Enable-AzureRmAlias에 'Local' 범위 추가</span><span class="sxs-lookup"><span data-stu-id="6783d-2918">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6783d-2919">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6783d-2919">Az.Compute</span></span>
* <span data-ttu-id="6783d-2920">이름이 Restart/Start/Stop/Remove/Set-AzVM과 Save-AzVMImage에 설정된 ID 매개 변수에서 선택 사항이 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-2920">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="6783d-2921">도움말 파일의 ID에 대한 설명이 업데이트 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-2921">Updated the description of ID in help files</span></span>
* <span data-ttu-id="6783d-2922">Az.Accounts 모듈을 사용할 때의 이전 버전과의 호환성 문제를 해결합니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-2922">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="6783d-2923">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="6783d-2923">Az.DataLakeStore</span></span>
* <span data-ttu-id="6783d-2924">SDK 수정을 위해 데이터 평면의 SDK 버전을 1.1.14로 업데이트하세요.</span><span class="sxs-lookup"><span data-stu-id="6783d-2924">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="6783d-2925">getfilestatus 및 liststatus에 대한 음수 acesstime 및 modificationtime 수정, 비동기 취소 토큰 수정</span><span class="sxs-lookup"><span data-stu-id="6783d-2925">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="6783d-2926">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="6783d-2926">Az.EventGrid</span></span>
* <span data-ttu-id="6783d-2927">2019-01-01 API 버전을 사용하도록 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-2927">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="6783d-2928">2019-01-01 API 버전에서 새 시나리오를 지원하도록 다음 cmdlet을 업데이트</span><span class="sxs-lookup"><span data-stu-id="6783d-2928">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="6783d-2929">New-AzureRmEventGridSubscription: 지정을 위한 새로운 선택적 매개 변수를 추가</span><span class="sxs-lookup"><span data-stu-id="6783d-2929">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="6783d-2930">이벤트 Time-to-Live</span><span class="sxs-lookup"><span data-stu-id="6783d-2930">Event Time-To-Live,</span></span>
        - <span data-ttu-id="6783d-2931">이벤트에 대한 최대 배달 시도</span><span class="sxs-lookup"><span data-stu-id="6783d-2931">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="6783d-2932">배달 못한 편지의 엔드포인트입니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-2932">Dead letter endpoint.</span></span>
    - <span data-ttu-id="6783d-2933">Update-AzureRmEventGridSubscription: 지정을 위한 새로운 선택적 매개 변수를 추가</span><span class="sxs-lookup"><span data-stu-id="6783d-2933">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="6783d-2934">이벤트 Time-to-Live</span><span class="sxs-lookup"><span data-stu-id="6783d-2934">Event Time-To-Live,</span></span>
        - <span data-ttu-id="6783d-2935">이벤트에 대한 최대 배달 시도</span><span class="sxs-lookup"><span data-stu-id="6783d-2935">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="6783d-2936">배달 못한 편지의 엔드포인트입니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-2936">Dead letter endpoint.</span></span>
* <span data-ttu-id="6783d-2937">New-AzureRmEventGridSubscription 및 Update-AzureRmEventGridSubscription cmdlet의 EndpointType 옵션에 새 열거형 값(즉, storageQueue 및 hybridConnection)을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-2937">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="6783d-2938">이벤트 구독을 생성 또는 업데이트할 때 사용자가 직접 조치를 취해야 할 경우 경고 메시지를 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-2938">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="6783d-2939">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="6783d-2939">Az.IotHub</span></span>
* <span data-ttu-id="6783d-2940">최신 버전의 Azure IotHub SDK로 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="6783d-2940">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="6783d-2941">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="6783d-2941">Az.LogicApp</span></span>
* <span data-ttu-id="6783d-2942">지정된 이름이 없는 모든 Get-AzLogicApp 목록</span><span class="sxs-lookup"><span data-stu-id="6783d-2942">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="6783d-2943">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6783d-2943">Az.Resources</span></span>
* <span data-ttu-id="6783d-2944">'Get-AzResource'에 '-ODataQuery'및 '-ResourceId' 매개 변수를 제공할 때 매개 변수 집합 문제 수정</span><span class="sxs-lookup"><span data-stu-id="6783d-2944">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="6783d-2945">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/7875 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="6783d-2945">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="6783d-2946">New/Set-AzPolicyDefinition에서 -Custom 매개 변수 처리 문제 수정</span><span class="sxs-lookup"><span data-stu-id="6783d-2946">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="6783d-2947">New-AzDeployment 설명서에서 오타 수정</span><span class="sxs-lookup"><span data-stu-id="6783d-2947">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="6783d-2948">'New-AzADUser'에 '-MailNickname'매개 변수가 필수 항목으로 지정됨</span><span class="sxs-lookup"><span data-stu-id="6783d-2948">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="6783d-2949">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/8220 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="6783d-2949">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="6783d-2950">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="6783d-2950">Az.SignalR</span></span>
* <span data-ttu-id="6783d-2951">Az.Accounts 모듈을 사용할 때의 이전 버전과의 호환성 문제를 해결합니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-2951">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="6783d-2952">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6783d-2952">Az.Sql</span></span>
* <span data-ttu-id="6783d-2953">Storage 관리 클라이언트 종속성을 일반적인 SDK 구현으로 변환했습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-2953">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="6783d-2954">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="6783d-2954">Az.Storage</span></span>
* <span data-ttu-id="6783d-2955">Sas Token, OAuth 또는 Anonymous를 사용하여 스토리지 컨텍스트의 StorageAccountName을 실제 스토리지 계정 이름으로 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-2955">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="6783d-2956">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="6783d-2956">New-AzStorageContext</span></span>
* <span data-ttu-id="6783d-2957">'-FullUri' 매개 변수를 사용하여 Blob 스냅샷 개체의 Sas Token을 생성하고 반환된 Uri를 스냅샷 Uri로 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-2957">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="6783d-2958">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="6783d-2958">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="6783d-2959">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="6783d-2959">Az.Websites</span></span>
* <span data-ttu-id="6783d-2960">'Get-AzDeletedWebApp'의 날짜 구문 분석 버그를 수정했습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-2960">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="6783d-2961">Az.Accounts 모듈을 사용할 때의 이전 버전과의 호환성 문제를 해결합니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-2961">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="6783d-2962">1.0.0 - 2018년 12월</span><span class="sxs-lookup"><span data-stu-id="6783d-2962">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="6783d-2963">일반</span><span class="sxs-lookup"><span data-stu-id="6783d-2963">General</span></span>

- <span data-ttu-id="6783d-2964">Az 모듈 일반 공급</span><span class="sxs-lookup"><span data-stu-id="6783d-2964">General Availability of Az Module</span></span>
- <span data-ttu-id="6783d-2965">각 모듈에 대 한 온라인 도움말</span><span class="sxs-lookup"><span data-stu-id="6783d-2965">Online help for each module</span></span>
- <span data-ttu-id="6783d-2966">자세한 내용과 로드맵은 [Az 알림 페이지](https://aka.ms/azps-announce)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="6783d-2966">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="6783d-2967">AzureRM에서 마이그레이션하는 것에 대한 정보는 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="6783d-2967">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="6783d-2968">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6783d-2968">Az.Accounts</span></span>
- <span data-ttu-id="6783d-2969">Az.Profile에서 변경</span><span class="sxs-lookup"><span data-stu-id="6783d-2969">Changed from Az.Profile</span></span>
- <span data-ttu-id="6783d-2970">프로필 및 컨텍스트 형식에 대한 표 형식 수정</span><span class="sxs-lookup"><span data-stu-id="6783d-2970">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="6783d-2971">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="6783d-2971">Az.ApiManagement</span></span>
- <span data-ttu-id="6783d-2972">#7002에 대한 수정</span><span class="sxs-lookup"><span data-stu-id="6783d-2972">Fixes for #7002</span></span>
- <span data-ttu-id="6783d-2973">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="6783d-2973">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="6783d-2974">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="6783d-2974">Az.Batch</span></span>
- <span data-ttu-id="6783d-2975">`PSComputeNode`의 새로운 `NodeAgentInformation` 속성을 통해 풀의 각 VM에서 실행 중인 Azure Batch 노드 에이전트의 버전을 확인하는 기능이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-2975">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="6783d-2976">`PSDataDisk`에 대한 `Caching` 기본 값은 이제 `None` 대신 `ReadWrite`입니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-2976">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="6783d-2977">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="6783d-2977">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="6783d-2978">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="6783d-2978">Az.Billing</span></span>
- <span data-ttu-id="6783d-2979">청구, 소비 및 UsageAggregates cmdlet 결합 cmdlet에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="6783d-2979">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="6783d-2980">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="6783d-2980">Az.CognitivServices</span></span>
- <span data-ttu-id="6783d-2981">New-AzureRmCognitiveServicesAccount 작업에서 사용 가능한 SkuName 및 Typem에 대한 완성자 추가</span><span class="sxs-lookup"><span data-stu-id="6783d-2981">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="6783d-2982">Get-AzCognitiveServicesAccountSkus에서 GetSkusWithAccountParamSetName 매개 변수 집합을 제거</span><span class="sxs-lookup"><span data-stu-id="6783d-2982">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="6783d-2983">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="6783d-2983">Az.ContainerInstance</span></span>
- <span data-ttu-id="6783d-2984">ManagedIdentity 지원이 추가됨</span><span class="sxs-lookup"><span data-stu-id="6783d-2984">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="6783d-2985">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="6783d-2985">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="6783d-2986">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="6783d-2986">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="6783d-2987">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="6783d-2987">Az.DataLakeStore</span></span>
- <span data-ttu-id="6783d-2988">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="6783d-2988">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="6783d-2989">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="6783d-2989">Az.Monitor</span></span>
- <span data-ttu-id="6783d-2990">Az.Monitor 이름 변경 및 기타 사소한 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="6783d-2990">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="6783d-2991">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="6783d-2991">Az.KeyVault</span></span>
- <span data-ttu-id="6783d-2992">출력 형식에서 사용되지 않는 'PurgeDisabled' 속성 제거</span><span class="sxs-lookup"><span data-stu-id="6783d-2992">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="6783d-2993">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="6783d-2993">Az.MachineLearning</span></span>
- <span data-ttu-id="6783d-2994">Az.MachineLearningCompute 모듈의 cmdlet 포함</span><span class="sxs-lookup"><span data-stu-id="6783d-2994">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="6783d-2995">Az.Media</span><span class="sxs-lookup"><span data-stu-id="6783d-2995">Az.Media</span></span>
- <span data-ttu-id="6783d-2996">New-AzMediaService에서 사용되지 않는 -Tags 별칭이 제거됨</span><span class="sxs-lookup"><span data-stu-id="6783d-2996">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="6783d-2997">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6783d-2997">Az.Network</span></span>
<span data-ttu-id="6783d-2998">Application Gateway에서 RewriteRuleSets를 구성하는 것에 대한 지원이 추가됨</span><span class="sxs-lookup"><span data-stu-id="6783d-2998">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="6783d-2999">추가된 새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-2999">New cmdlets added:</span></span>
        - <span data-ttu-id="6783d-3000">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="6783d-3000">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="6783d-3001">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="6783d-3001">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="6783d-3002">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="6783d-3002">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="6783d-3003">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="6783d-3003">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="6783d-3004">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="6783d-3004">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="6783d-3005">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="6783d-3005">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="6783d-3006">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="6783d-3006">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="6783d-3007">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="6783d-3007">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="6783d-3008">선택적 매개 변수를 사용하도록 cmdlet이 업데이트됨 -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="6783d-3008">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="6783d-3009">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6783d-3009">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="6783d-3010">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="6783d-3010">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="6783d-3011">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="6783d-3011">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="6783d-3012">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="6783d-3012">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="6783d-3013">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="6783d-3013">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="6783d-3014">New-AzureRmApplicationGatewayUrlPathMapConfig로 ID를 사용하여 Application Gateway에 KeyVault 지원을 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-3014">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="6783d-3015">선택적 매개 변수를 사용하도록 cmdlet이 업데이트됨 -KeyVaultSecretId, -KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="6783d-3015">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="6783d-3016">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="6783d-3016">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="6783d-3017">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="6783d-3017">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="6783d-3018">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="6783d-3018">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="6783d-3019">New-AzApplicationGateway cmdlet이 선택적 매개 변수를 사용하도록 업데이트됨 -UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="6783d-3019">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="6783d-3020">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="6783d-3020">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="6783d-3021">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="6783d-3021">Az.OperationalInsights</span></span>
- <span data-ttu-id="6783d-3022">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="6783d-3022">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="6783d-3023">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="6783d-3023">Az.Profile</span></span>
- <span data-ttu-id="6783d-3024">Az.Accounts에 모듈 이름이 변경됨</span><span class="sxs-lookup"><span data-stu-id="6783d-3024">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="6783d-3025">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="6783d-3025">Az.RecoveryServices</span></span>
- <span data-ttu-id="6783d-3026">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="6783d-3026">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="6783d-3027">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6783d-3027">Az.Resources</span></span>
- <span data-ttu-id="6783d-3028">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="6783d-3028">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="6783d-3029">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="6783d-3029">Az.ServiceFabric</span></span>
- <span data-ttu-id="6783d-3030">일반 이름과 지문으로 지정 인증서 지원</span><span class="sxs-lookup"><span data-stu-id="6783d-3030">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="6783d-3031">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="6783d-3031">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="6783d-3032">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="6783d-3032">Az.SIgnalR</span></span>
- <span data-ttu-id="6783d-3033">SIgnalR에 대한 PowerShell cmdlet에 대한 일반 공급</span><span class="sxs-lookup"><span data-stu-id="6783d-3033">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="6783d-3034">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6783d-3034">Az.Sql</span></span>
- <span data-ttu-id="6783d-3035">위협 탐지의 cmdlet에 새로운 Data_Exfiltration 및 Unsafe_Action 검색 유형 추가</span><span class="sxs-lookup"><span data-stu-id="6783d-3035">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="6783d-3036">Sql 감사 cmdlet에 대한 설명서 예제 업데이트</span><span class="sxs-lookup"><span data-stu-id="6783d-3036">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="6783d-3037">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="6783d-3037">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="6783d-3038">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="6783d-3038">Az.Storage</span></span>
- <span data-ttu-id="6783d-3039">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="6783d-3039">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="6783d-3040">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="6783d-3040">Az.Websites</span></span>
- <span data-ttu-id="6783d-3041">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="6783d-3041">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="6783d-3042">0.7.0 - 2018년 12월</span><span class="sxs-lookup"><span data-stu-id="6783d-3042">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="6783d-3043">일반</span><span class="sxs-lookup"><span data-stu-id="6783d-3043">General</span></span>

* <span data-ttu-id="6783d-3044">AzureRM에서 Az 전환 예정에 대한 사소한 변경</span><span class="sxs-lookup"><span data-stu-id="6783d-3044">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="6783d-3045">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6783d-3045">Az.Compute</span></span>

* <span data-ttu-id="6783d-3046">`New-AzVm(ss)` cmdlet에 대한 간단한 매개 변수 집합에 UltraSSD 및 갤러리 이미지에 대한 지원을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-3046">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="6783d-3047">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="6783d-3047">Az.DataLakeStore</span></span>

* <span data-ttu-id="6783d-3048">ADLS 계정의 도메인의 후행 슬래시를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-3048">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="6783d-3049">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="6783d-3049">Az.FrontDoor</span></span>

* <span data-ttu-id="6783d-3050">일부 끊어진 링크 수정</span><span class="sxs-lookup"><span data-stu-id="6783d-3050">Fixed some broken links</span></span>
    - <span data-ttu-id="6783d-3051">New-AzureRmFrontDoor 및 Set-AzureRmFrontDoor 아티클에서 New-AzureRmFrontDoorHealthProbeSettingObject cmdlet 아티클에 대한 링크가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-3051">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="6783d-3052">New-AzureRmFrontDoorManagedRuleObject 아티클에서 New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet 아티클에 대한 링크가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-3052">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="6783d-3053">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="6783d-3053">Az.RecoveryServices</span></span>

* <span data-ttu-id="6783d-3054">Azure File Share 복원 작업에 클라이언트 측 유효성 검사가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-3054">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="6783d-3055">afs 복원의 경우 storageAccountName 및 storageAccountResourceGroupName을 선택적으로 만들었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-3055">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="6783d-3056">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6783d-3056">Az.Resources</span></span>

* <span data-ttu-id="6783d-3057"> https://github.com/Azure/azure-powershell/issues/7679 에 대한 수정</span><span class="sxs-lookup"><span data-stu-id="6783d-3057">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="6783d-3058">기본 관리자를 요청할 때 구독 범위가 제공되는 경우 Get-AzureRmRoleAssignment를 업데이트하여 구독 범위를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-3058">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="6783d-3059">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6783d-3059">Az.Sql</span></span>

* <span data-ttu-id="6783d-3060">AzureRM에서 Az 전환 예정에 대한 사소한 변경</span><span class="sxs-lookup"><span data-stu-id="6783d-3060">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="6783d-3061">DotNet 코어에서 Get-AzureRmSqlDatabaseVulnerabilityAssessment를 사용하는 문제 해결</span><span class="sxs-lookup"><span data-stu-id="6783d-3061">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="6783d-3062">SQL 감사 cmdlet과 관련된 도움말 메시지의 설명서가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-3062">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="6783d-3063">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="6783d-3063">Az.Storage</span></span>

* <span data-ttu-id="6783d-3064">New-AzureRmStorageAccount에 -EnableHierarchicalNamespace 추가</span><span class="sxs-lookup"><span data-stu-id="6783d-3064">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="6783d-3065">파일 복사 cmdlet이 -DestContext 입력이 없을 때 대상의 원본 컨텍스트를 다시 사용할 수 없는 문제 수정</span><span class="sxs-lookup"><span data-stu-id="6783d-3065">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="6783d-3066">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="6783d-3066">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="6783d-3067">고정적인 웹 사이트 구성 지원</span><span class="sxs-lookup"><span data-stu-id="6783d-3067">Support Static Website configuration</span></span>
    - <span data-ttu-id="6783d-3068">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="6783d-3068">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="6783d-3069">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="6783d-3069">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="6783d-3070">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="6783d-3070">Az.Websites</span></span>

* <span data-ttu-id="6783d-3071">Set-AzureRmWebApp 및 Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="6783d-3071">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span>
    - <span data-ttu-id="6783d-3072">Windows 및 Linux 컨테이너 응용 프로그램에 탑재할 Azure Storage 경로를 지정하기 위해 새 매개 변수(-AzureStoragePath)가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-3072">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="6783d-3073">새 cmdlet New-AzureRmWebAppAzureStoragePath의 출력을 매개 변수로 사용하여 Azure Storage 경로를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-3073">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="6783d-3074">0.6.1 - 2018년 11월</span><span class="sxs-lookup"><span data-stu-id="6783d-3074">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="6783d-3075">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="6783d-3075">Az.ApiManagement</span></span>
* <span data-ttu-id="6783d-3076">형식 매핑 문제에 대한 종속성 업데이트</span><span class="sxs-lookup"><span data-stu-id="6783d-3076">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="6783d-3077">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="6783d-3077">Az.Automation</span></span>
* <span data-ttu-id="6783d-3078">Azure Automation cmdlet 기반 Swagger</span><span class="sxs-lookup"><span data-stu-id="6783d-3078">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="6783d-3079">업데이트 관리 cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="6783d-3079">Added Update Management cmdlets</span></span>
* <span data-ttu-id="6783d-3080">소스 제어 cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="6783d-3080">Added Source Control cmdlets</span></span>
* <span data-ttu-id="6783d-3081">Remove-AzureRmAutomationHybridWorkerGroup cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="6783d-3081">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="6783d-3082">DSC 노드 등록 명령 수정</span><span class="sxs-lookup"><span data-stu-id="6783d-3082">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="6783d-3083">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6783d-3083">Az.Compute</span></span>
* <span data-ttu-id="6783d-3084">SystemAssigned ID에 대한 ID 문제 수정</span><span class="sxs-lookup"><span data-stu-id="6783d-3084">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="6783d-3085">형식 매핑 문제에 대한 종속성 업데이트</span><span class="sxs-lookup"><span data-stu-id="6783d-3085">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="6783d-3086">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="6783d-3086">Az.ContainerInstance</span></span>
* <span data-ttu-id="6783d-3087">형식 매핑 문제에 대한 종속성 업데이트</span><span class="sxs-lookup"><span data-stu-id="6783d-3087">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="6783d-3088">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="6783d-3088">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="6783d-3089">마켓플레이스 cmdlet에 대한 예제 설명 업데이트</span><span class="sxs-lookup"><span data-stu-id="6783d-3089">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="6783d-3090">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6783d-3090">Az.Network</span></span>
* <span data-ttu-id="6783d-3091">New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="6783d-3091">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="6783d-3092">지원되는 AzureFirewall 네트워크 프로토콜에 ICMP 다시 추가</span><span class="sxs-lookup"><span data-stu-id="6783d-3092">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="6783d-3093">Test-AzureRmNetworkWatcherConnectivity cmdlet을 업데이트하여 대상 ID, 주소 및 포트 유효성 검사를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-3093">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span>
* <span data-ttu-id="6783d-3094">VirtualNetwork 맵의 메모리 사용 문제 해결</span><span class="sxs-lookup"><span data-stu-id="6783d-3094">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="6783d-3095">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="6783d-3095">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="6783d-3096">보호된 파일 공유에 대한 정책을 수정하는 것에 대해 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-3096">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="6783d-3097">정책 표준 시간대를 대문자로 변환했습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-3097">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="6783d-3098">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="6783d-3098">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="6783d-3099">New-AzureRmRecoveryServicesAsrProtectableItem의 예제 정정</span><span class="sxs-lookup"><span data-stu-id="6783d-3099">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="6783d-3100">형식 매핑 문제에 대한 종속성 업데이트</span><span class="sxs-lookup"><span data-stu-id="6783d-3100">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="6783d-3101">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="6783d-3101">Az.Relay</span></span>
* <span data-ttu-id="6783d-3102">선택적 매개 변수 -KeyValue를 New-AzureRmRelayKey cmdlet에 추가하여 사용자가 KeyValue를 제공할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-3102">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="6783d-3103">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6783d-3103">Az.Resources</span></span>
* <span data-ttu-id="6783d-3104">`New-AzureRmPolicyAssignment` 및 `Set-AzureRmPolicyAssignment`의 자원 ID 관련 매개 변수에 대한 도움말 문서를 업데이트함</span><span class="sxs-lookup"><span data-stu-id="6783d-3104">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="6783d-3105">-Metadata를 사용하는 New-AzureRmPolicyDefinition에 대한 예제 추가</span><span class="sxs-lookup"><span data-stu-id="6783d-3105">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="6783d-3106">NetStandard의 태그 키에서 대소문자 보존을 허용하도록 수정: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="6783d-3106">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="6783d-3107">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="6783d-3107">Az.ServiceFabric</span></span>
* <span data-ttu-id="6783d-3108">향후 호환성이 손상되는 변경에 대한 사용 중단 메시지 추가</span><span class="sxs-lookup"><span data-stu-id="6783d-3108">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="6783d-3109">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6783d-3109">Az.Sql</span></span>
* <span data-ttu-id="6783d-3110">Azure Sql Database Managed Instance 및 Azure Sql Managed Database에 CRUD 작업을 위한 새 cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="6783d-3110">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="6783d-3111">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="6783d-3111">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="6783d-3112">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="6783d-3112">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="6783d-3113">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="6783d-3113">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="6783d-3114">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="6783d-3114">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="6783d-3115">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="6783d-3115">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="6783d-3116">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="6783d-3116">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="6783d-3117">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="6783d-3117">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="6783d-3118">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="6783d-3118">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="6783d-3119">서버 또는 데이터베이스에서 확장 감사 정책 관리를 활성화했습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-3119">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="6783d-3120">새 매개 변수(PredicateExpression)가 감사 로그 필터링을 사용하도록 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-3120">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="6783d-3121">Cmdlet이 레거시 클라이언트 대신 SQL 클라이언트를 사용하도록 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-3121">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="6783d-3122">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="6783d-3122">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="6783d-3123">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="6783d-3123">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="6783d-3124">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="6783d-3124">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="6783d-3125">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="6783d-3125">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="6783d-3126">스토리지 계정 이름 매개 변수가 설정된 Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings를 사용할 때의 문제 해결</span><span class="sxs-lookup"><span data-stu-id="6783d-3126">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="6783d-3127">0.5.0 - 2018년 11월</span><span class="sxs-lookup"><span data-stu-id="6783d-3127">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="6783d-3128">일반</span><span class="sxs-lookup"><span data-stu-id="6783d-3128">General</span></span>
* <span data-ttu-id="6783d-3129">많은 핵심 cmdlet에 Resource Completers를 추가하여 대화형으로 cmdlet을 호출할 때 기존 리소스 이름을 탭으로 이동할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-3129">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="6783d-3130">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="6783d-3130">Az.Profile</span></span>
* <span data-ttu-id="6783d-3131">ClientRuntime의 최신 버전을 사용하도록 일반적인 코드를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-3131">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="6783d-3132">Connect-AzAccount cmdlet의 매개 변수 TenantId 이름을 Tenant로 바꾸고 TenantId의 별칭을 추가합니다</span><span class="sxs-lookup"><span data-stu-id="6783d-3132">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="6783d-3133">Connect-AzAccount의 업데이트된 TenantId 설명</span><span class="sxs-lookup"><span data-stu-id="6783d-3133">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="6783d-3134">테넌트 도메인을 제공할 때 실패한 로그인에 대한 오류 메시지 수정</span><span class="sxs-lookup"><span data-stu-id="6783d-3134">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="6783d-3135">테넌트에 구독이 없는 계정의 컨텍스트 이름 충돌 문제 수정</span><span class="sxs-lookup"><span data-stu-id="6783d-3135">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="6783d-3136">MSI를 사용할 때 DataLake 엔드포인트 문제 수정</span><span class="sxs-lookup"><span data-stu-id="6783d-3136">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="6783d-3137">연결되지 않은 경우 'Disconnect-AzAccount'가 throw하는 문제 수정</span><span class="sxs-lookup"><span data-stu-id="6783d-3137">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="6783d-3138">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="6783d-3138">Az.CognitiveServices</span></span>
* <span data-ttu-id="6783d-3139">Get-AzCognitiveServicesAccountSkus 작업을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-3139">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6783d-3140">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6783d-3140">Az.Compute</span></span>
* <span data-ttu-id="6783d-3141">Add-AzVmssVMDataDisk 및 Remove-AzVmssVMDataDisk cmdlet를 추가합니다</span><span class="sxs-lookup"><span data-stu-id="6783d-3141">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="6783d-3142">Get-AzVMImage는 AutomaticOSUpgradeProperties를 표시합니다</span><span class="sxs-lookup"><span data-stu-id="6783d-3142">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="6783d-3143">수정된 SetAzVMChefExtension -BootstrapOptions 및 -JsonAttribute option 값이 json 형식으로 설정하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-3143">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="6783d-3144">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="6783d-3144">Az.DataLakeStore</span></span>
* <span data-ttu-id="6783d-3145">DataLake 패키지를 1.1.10으로 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-3145">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="6783d-3146">기본 동시성을 다중 스레드 작업에 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-3146">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="6783d-3147">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="6783d-3147">Az.Insights</span></span>
* <span data-ttu-id="6783d-3148">해결된 문제 #7267(자동 크기 조정 영역)</span><span class="sxs-lookup"><span data-stu-id="6783d-3148">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="6783d-3149">열거된 매개 변수를 제대로 설정하지 않은 새 자동 크기 조정 규칙을 만드는 데 문제가 있습니다(이를 항상 기본값으로 설정함).</span><span class="sxs-lookup"><span data-stu-id="6783d-3149">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="6783d-3150">해결된 문제 # 7513[자세한 정보] Set-AzDiagnosticSetting은 설정을 생성하는 동안 범주를 명시적으로 지정해야 합니다</span><span class="sxs-lookup"><span data-stu-id="6783d-3150">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="6783d-3151">이제 cmdlet은 생성 중에 사용할 범주를 명시적으로 표시할 필요가 없습니다. 즉, 문서화된대로 작동합니다</span><span class="sxs-lookup"><span data-stu-id="6783d-3151">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6783d-3152">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6783d-3152">Az.Network</span></span>
* <span data-ttu-id="6783d-3153">다음 cmdlet에 대해 PeeringType을 필수 매개 변수로 변경했습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-3153">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="6783d-3154">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="6783d-3154">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="6783d-3155">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="6783d-3155">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="6783d-3156">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="6783d-3156">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="6783d-3157">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="6783d-3157">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="6783d-3158">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="6783d-3158">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="6783d-3159">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="6783d-3159">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="6783d-3160">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="6783d-3160">Az.PolicyInsights</span></span>
* <span data-ttu-id="6783d-3161">추가된 정책 재구성 cmdlet</span><span class="sxs-lookup"><span data-stu-id="6783d-3161">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="6783d-3162">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6783d-3162">Az.Resources</span></span>
* <span data-ttu-id="6783d-3163"> https://github.com/Azure/azure-powershell/issues/7402 에 대한 수정</span><span class="sxs-lookup"><span data-stu-id="6783d-3163">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="6783d-3164">'Get-AzResource'에 대해 '-ResourceId' 매개 변수를 사용하여 리소스 나열 허용</span><span class="sxs-lookup"><span data-stu-id="6783d-3164">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="6783d-3165">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="6783d-3165">Az.ServiceBus</span></span>
* <span data-ttu-id="6783d-3166">마이그레이션 상태를 알 수 있도록 PSServiceBusMigrationConfigurationAttributes에 MigrationState 읽기 전용 속성 추가.</span><span class="sxs-lookup"><span data-stu-id="6783d-3166">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="6783d-3167">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="6783d-3167">Az.ServiceFabric</span></span>
* <span data-ttu-id="6783d-3168">Linux Vmss에 인증서 추가 수정.</span><span class="sxs-lookup"><span data-stu-id="6783d-3168">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="6783d-3169">Add-AzServiceFabricClusterCertificate 수정</span><span class="sxs-lookup"><span data-stu-id="6783d-3169">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="6783d-3170">새 인증서(Azure/service-fabric-issues#932)에서 올바른 지문을 사용.</span><span class="sxs-lookup"><span data-stu-id="6783d-3170">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="6783d-3171">올바르게 예외 표시(Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="6783d-3171">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="6783d-3172">Vmss CreateOrUpdate 작업을 시작하기 전에 'Update-AzServiceFabricDurability'를 수정하여 클러스터 구성 업데이트.</span><span class="sxs-lookup"><span data-stu-id="6783d-3172">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="6783d-3173">0.4.0 - 2018년 10월</span><span class="sxs-lookup"><span data-stu-id="6783d-3173">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="6783d-3174">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="6783d-3174">Az.Profile</span></span>
* <span data-ttu-id="6783d-3175">CloudShell에서 Get-AzSubscription을 사용하여 문제를 해결합니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-3175">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="6783d-3176">ClientRuntime의 최신 버전을 사용하도록 일반적인 코드를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-3176">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6783d-3177">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6783d-3177">Az.Compute</span></span>
* <span data-ttu-id="6783d-3178">'New-AzVm'에 대해 간단한 매개 변수를 사용하는 경우 가속화된 네트워킹을 설정하기 위해 새 크기가 VM 크기의 허용 목록에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-3178">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="6783d-3179">모든 cmdlet에 ResourceName 인수 완성자가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-3179">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="6783d-3180">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="6783d-3180">Az.DataLakeStore</span></span>
* <span data-ttu-id="6783d-3181">Virtual Network 규칙에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="6783d-3181">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="6783d-3182">Get-AzDataLakeStoreVirtualNetworkRule: Azure Data Lake Store 가상 네트워크 규칙을 가져오거나 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-3182">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="6783d-3183">Add-AzDataLakeStoreVirtualNetworkRule: 지정된 Data Lake Store 계정에 가상 네트워크 규칙을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-3183">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="6783d-3184">Set-AzDataLakeStoreVirtualNetworkRule: 지정된 Data Lake Store 계정에 지정된 가상 네트워크 규칙을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-3184">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="6783d-3185">Remove-AzDataLakeStoreVirtualNetworkRule: Azure Data Lake Store 가상 네트워크 규칙을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-3185">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6783d-3186">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6783d-3186">Az.Network</span></span>
* <span data-ttu-id="6783d-3187">Test-AzNetworkWatcherConnectivity cmdlet을 업데이트하고, 백 엔드에 프로토콜 값을 전달합니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-3187">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="6783d-3188">모든 cmdlet에 ResourceName 인수 완성자가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-3188">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="6783d-3189">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6783d-3189">Az.Resources</span></span>
* <span data-ttu-id="6783d-3190">(기본 프로필에 구독이 없고 범위가 지정되지 않은 경우) 시나리오에서 의미 있는 예외를 추가하여 Get-AzRoleDefinition이 인식할 수 없는 예외를 throw하는 문제를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-3190">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="6783d-3191">또한 기본 매개 변수 집합을 'RoleDefinitionNameParameterSet'으로 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-3191">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="6783d-3192">0.3.0 - 2018년 10월</span><span class="sxs-lookup"><span data-stu-id="6783d-3192">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="6783d-3193">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="6783d-3193">Azure.Storage</span></span>
* <span data-ttu-id="6783d-3194">대상에 메타데이터가 있을 때 Blob/파일이 메타 데이터를 복사하지 않는 문제 수정</span><span class="sxs-lookup"><span data-stu-id="6783d-3194">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="6783d-3195">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="6783d-3195">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="6783d-3196">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="6783d-3196">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="6783d-3197">특정 위치의 스토리지 리소스 사용을 지원하고 글로벌 스토리지 리소스 사용 가져오기는 더 이상 사용되지 않는다는 경고 메시지를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-3197">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="6783d-3198">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="6783d-3198">Get-AzStorageUsage</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="6783d-3199">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="6783d-3199">Az.CognitiveServices</span></span>
* <span data-ttu-id="6783d-3200">기존 계정이 없는 Get-AzCognitiveServicesAccountSkus를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-3200">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6783d-3201">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6783d-3201">Az.Compute</span></span>
* <span data-ttu-id="6783d-3202">Get-AzVM -ResourceGroupName <rg>가 필요한 경우 50개가 넘는 결과를 반환하도록 수정</span><span class="sxs-lookup"><span data-stu-id="6783d-3202">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="6783d-3203">'SimpleParameterSet' 예제가 New-AzVmss cmdlet 도움말에 추가됨</span><span class="sxs-lookup"><span data-stu-id="6783d-3203">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="6783d-3204">Azure Disk Encryption 진행률 메시지의 오타를 수정</span><span class="sxs-lookup"><span data-stu-id="6783d-3204">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="6783d-3205">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="6783d-3205">Az.DataFactoryV2</span></span>
* <span data-ttu-id="6783d-3206">ADF.Net SDK 버전을 2.3.0으로 업데이트</span><span class="sxs-lookup"><span data-stu-id="6783d-3206">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6783d-3207">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6783d-3207">Az.Network</span></span>
* <span data-ttu-id="6783d-3208">NetworkProfile 기능 추가</span><span class="sxs-lookup"><span data-stu-id="6783d-3208">Added NetworkProfile functionality.</span></span> <span data-ttu-id="6783d-3209">추가된 새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-3209">new cmdlets added</span></span>
    - <span data-ttu-id="6783d-3210">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="6783d-3210">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="6783d-3211">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="6783d-3211">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="6783d-3212">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="6783d-3212">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="6783d-3213">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="6783d-3213">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="6783d-3214">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="6783d-3214">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="6783d-3215">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="6783d-3215">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="6783d-3216">서브넷 모델에 서비스 연결 링크 추가</span><span class="sxs-lookup"><span data-stu-id="6783d-3216">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="6783d-3217">New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="6783d-3217">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="6783d-3218">Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="6783d-3218">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="6783d-3219">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="6783d-3219">Az.RedisCache</span></span>
* <span data-ttu-id="6783d-3220">모든 문자열을 Size 매개 변수로 진행되도록 허용</span><span class="sxs-lookup"><span data-stu-id="6783d-3220">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="6783d-3221">PSArgumentCompleter 팝업에 P5 추가</span><span class="sxs-lookup"><span data-stu-id="6783d-3221">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="6783d-3222">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6783d-3222">Az.Resources</span></span>
* <span data-ttu-id="6783d-3223">-Mode 매개 변수를 Set-AzPolicyDefinition에 추가</span><span class="sxs-lookup"><span data-stu-id="6783d-3223">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="6783d-3224">사용자가 포함된 Origin 작업에서 Get-AzProviderOperation commandlet 버그 수정</span><span class="sxs-lookup"><span data-stu-id="6783d-3224">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="6783d-3225">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6783d-3225">Az.Sql</span></span>
* <span data-ttu-id="6783d-3226">일부 백업 cmdlet이 현재 azure 구독을 인식하지 않는 문제 해결</span><span class="sxs-lookup"><span data-stu-id="6783d-3226">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="6783d-3227">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="6783d-3227">Az.Websites</span></span>
* <span data-ttu-id="6783d-3228">새 cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - 컨테이너 지속적인 배포 Webhook URL을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-3228">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="6783d-3229">새 cmdlet New-AzWebAppContainerPSSession 및 Enter-WebAppContainerPSSession -  windows 컨테이너 앱에 PowerShell 원격 세션을 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="6783d-3229">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="6783d-3230">0.2.0 - 2018년 9월</span><span class="sxs-lookup"><span data-stu-id="6783d-3230">0.2.0 - September 2018</span></span>
 <span data-ttu-id="6783d-3231">초기 릴리스</span><span class="sxs-lookup"><span data-stu-id="6783d-3231">Initial Release</span></span>