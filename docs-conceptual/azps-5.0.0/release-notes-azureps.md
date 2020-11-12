---
title: Azure PowerShell 릴리스 정보
description: Azure PowerShell 모듈의 모든 최신 업데이트에 대해 알아봅니다.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/10/2020
ms.custom: devx-track-azurepowershell
ms.service: azure-powershell
ms.openlocfilehash: 27073db862b83c5b95f2364355037c1ebd34a3b5
ms.sourcegitcommit: 2036538797dd088728aee5ac5021472454d82eb2
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/06/2020
ms.locfileid: "93407496"
---
# <a name="azure-powershell-release-notes"></a><span data-ttu-id="c16ab-103">Azure PowerShell 릴리스 정보</span><span class="sxs-lookup"><span data-stu-id="c16ab-103">Azure PowerShell release notes</span></span>

## <a name="500---october-2020"></a><span data-ttu-id="c16ab-104">5.0.0 - 2020년 10월</span><span class="sxs-lookup"><span data-stu-id="c16ab-104">5.0.0 - October 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="c16ab-105">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="c16ab-105">Az.Accounts</span></span>
* <span data-ttu-id="c16ab-106">[호환성이 손상되는 변경] 'Get-AzProfile' 및 'Select-AzProfile'이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-106">[Breaking Change] Removed 'Get-AzProfile' and 'Select-AzProfile'</span></span>
* <span data-ttu-id="c16ab-107">Azure Directory 인증 라이브러리가 MSAL(Microsoft 인증 라이브러리)로 대체되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-107">Replaced Azure Directory Authentication Library with Microsoft Authentication Library(MSAL)</span></span>

#### <a name="azaks"></a><span data-ttu-id="c16ab-108">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="c16ab-108">Az.Aks</span></span>
* <span data-ttu-id="c16ab-109">[호환성이 손상되는 변경] 'New-AzAksCluster' 및 'Set-AzAksCluster'에서 매개 변수 별칭 'ClientIdAndSecret'이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-109">[Breaking Change] Removed parameter alias 'ClientIdAndSecret' in 'New-AzAksCluster' and 'Set-AzAksCluster'.</span></span>
* <span data-ttu-id="c16ab-110">[호환성이 손상되는 변경] 'New-AzAksCluster'의 'NodeVmSetType' 기본값이 'AvailabilitySet'에서 'VirtualMachineScaleSets'로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-110">[Breaking Change] Changed the default value of 'NodeVmSetType' in 'New-AzAksCluster' from 'AvailabilitySet' to 'VirtualMachineScaleSets'.</span></span>
* <span data-ttu-id="c16ab-111">[호환성이 손상되는 변경] 'New-AzAksCluster'의 'NetworkPlugin' 기본값이 'None'에서 'azure'로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-111">[Breaking Change] Changed the default value of 'NetworkPlugin' in 'New-AzAksCluster' from 'None' to 'azure'.</span></span>
* <span data-ttu-id="c16ab-112">[호환성이 손상되는 변경] 'New-AzAksCluster'의 'NodeOsType' 매개 변수는 Linux라는 하나의 값만 지원하므로 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-112">[Breaking Change] Removed parameter 'NodeOsType' in 'New-AzAksCluster' as it supports only one value Linux.</span></span>

#### <a name="azbilling"></a><span data-ttu-id="c16ab-113">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="c16ab-113">Az.Billing</span></span>
* <span data-ttu-id="c16ab-114">'Get-AzBillingAccount' cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-114">Added 'Get-AzBillingAccount' cmdlet</span></span>
* <span data-ttu-id="c16ab-115">'Get-AzBillingProfile' cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-115">Added 'Get-AzBillingProfile' cmdlet</span></span>
* <span data-ttu-id="c16ab-116">'Get-AzInvoiceSection' cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-116">Added 'Get-AzInvoiceSection' cmdlet</span></span>
* <span data-ttu-id="c16ab-117">'Get-AzBillingInvoice' cmdlet에 새 매개 변수가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-117">Added new parameters in 'Get-AzBillingInvoice' cmdlet</span></span>
* <span data-ttu-id="c16ab-118">Get-AzBillingInvoice cmdlet의 응답에서 DownloadUrlExpiry, Type, BillingPeriodNames 속성이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-118">Removed properties DownloadUrlExpiry, Type, BillingPeriodNames from the response of Get-AzBillingInvoice cmdlet</span></span>

#### <a name="azcdn"></a><span data-ttu-id="c16ab-119">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="c16ab-119">Az.Cdn</span></span>
* <span data-ttu-id="c16ab-120">다중 원본 및 프라이빗 링크 기능을 지원하는 cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-120">Added cmdlets to support multi-origin and private link functionality</span></span> 

#### <a name="azcognitiveservices"></a><span data-ttu-id="c16ab-121">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="c16ab-121">Az.CognitiveServices</span></span>
* <span data-ttu-id="c16ab-122">SDK가 7.4.0-preview로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-122">Updated SDK to 7.4.0-preview.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="c16ab-123">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="c16ab-123">Az.Compute</span></span>
* <span data-ttu-id="c16ab-124">'New-AzVm'에 '-VmssId' 매개 변수가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-124">Added '-VmssId' parameter to 'New-AzVm'</span></span>
* <span data-ttu-id="c16ab-125">'New-AzVmss' cmdlet에 'PlatformFaultDomainCount' 매개 변수가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-125">Added 'PlatformFaultDomainCount' parameter to the 'New-AzVmss' cmdlet.</span></span>
* <span data-ttu-id="c16ab-126">새 cmdlet 'Get-AzDiskEncryptionSetAssociatedResource'</span><span class="sxs-lookup"><span data-stu-id="c16ab-126">New cmdlet 'Get-AzDiskEncryptionSetAssociatedResource'</span></span>
* <span data-ttu-id="c16ab-127">New-AzDiskConfig cmdlet에 선택적 매개 변수 'Tier' 및 'LogicalSectorSize'가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-127">Added 'Tier' and 'LogicalSectorSize' optional parameters to the New-AzDiskConfig cmdlet.</span></span> 
* <span data-ttu-id="c16ab-128">'New-AzDiskUpdateConfig' cmdlet에 선택적 매개 변수 'Tier', 'MaxSharesCount', 'DiskIOPSReadOnly' 및 'DiskMBpsReadOnly'가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-128">Added 'Tier', 'MaxSharesCount', 'DiskIOPSReadOnly', and 'DiskMBpsReadOnly' optional parameters to the 'New-AzDiskUpdateConfig' cmdlet.</span></span> 

#### <a name="azcontainerregistry"></a><span data-ttu-id="c16ab-129">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="c16ab-129">Az.ContainerRegistry</span></span>
* <span data-ttu-id="c16ab-130">[호환성이 손상되는 변경] API 버전이 2019-05-01로 업데이트됩니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-130">[Breaking Change] Updates API version to 2019-05-01</span></span>
* <span data-ttu-id="c16ab-131">[호환성이 손상되는 변경] 'New-AzContainerRegistry'에서 SKU 'Classic' 및 'StorageAccountName' 매개 변수가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-131">[Breaking Change] Removed SKU 'Classic' and parameter 'StorageAccountName' from 'New-AzContainerRegistry'</span></span>
* <span data-ttu-id="c16ab-132">새 cmdlet이 추가되었습니다. 'Connect-AzContainerRegistry', 'Import-AzContainerRegistry', 'Get-AzContainerRegistryUsage', 'New-AzContainerRegistryNetworkRule', 'Set-AzContainerRegistryNetworkRule'</span><span class="sxs-lookup"><span data-stu-id="c16ab-132">Added New cmdlets: 'Connect-AzContainerRegistry', 'Import-AzContainerRegistry', 'Get-AzContainerRegistryUsage', 'New-AzContainerRegistryNetworkRule', 'Set-AzContainerRegistryNetworkRule'</span></span>
* <span data-ttu-id="c16ab-133">'Update-AzContainerRegistry'에 새 매개 변수 'NetworkRuleSet'가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-133">Added new parameter 'NetworkRuleSet' to 'Update-AzContainerRegistry'</span></span>

#### <a name="azdatabricks"></a><span data-ttu-id="c16ab-134">Az.Databricks</span><span class="sxs-lookup"><span data-stu-id="c16ab-134">Az.Databricks</span></span>
* <span data-ttu-id="c16ab-135">`-EncryptionKeyVersion`이 없으면 databricks 작업 영역 업데이트가 실패하는 버그가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-135">Fixed a bug that may cause updating databricks workspace without `-EncryptionKeyVersion` to fail.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="c16ab-136">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="c16ab-136">Az.DataFactory</span></span>
* <span data-ttu-id="c16ab-137">ADF .Net SDK 버전이 4.12.0으로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-137">Updated ADF .Net SDK version to 4.12.0</span></span>
* <span data-ttu-id="c16ab-138">ADF 암호화 클라이언트 SDK 버전이 4.14.7587.7로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-138">Updated ADF encryption client SDK version to 4.14.7587.7</span></span>
* <span data-ttu-id="c16ab-139">'Stop-AzDataFactoryV2TriggerRun' 및 'Invoke-AzDataFactoryV2TriggerRun' 명령이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-139">Added 'Stop-AzDataFactoryV2TriggerRun' and 'Invoke-AzDataFactoryV2TriggerRun' commands</span></span>

#### <a name="azdesktopvirtualization"></a><span data-ttu-id="c16ab-140">Az.DesktopVirtualization</span><span class="sxs-lookup"><span data-stu-id="c16ab-140">Az.DesktopVirtualization</span></span>
* <span data-ttu-id="c16ab-141">최상위 arm 개체를 만들려면 Location 속성이 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-141">Require Location property for creating top level arm objects.</span></span>
        <span data-ttu-id="c16ab-142">\* `New-AzWvdApplicationGroup`에 `ApplicationGroupType`이 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-142">\* Made `ApplicationGroupType` required for `New-AzWvdApplicationGroup`.</span></span>
        <span data-ttu-id="c16ab-143">\* `New-AzWvdApplicationGroup`에 `HostPoolArmPath`가 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-143">\* Made `HostPoolArmPath` required for `New-AzWvdApplicationGroup`.</span></span>
        <span data-ttu-id="c16ab-144">\* `New-AzWvdHostPool`에 `PreferredAppGroupType`이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-144">\* Added `PreferredAppGroupType` for `New-AzWvdHostPool`.</span></span>

#### <a name="azfunctions"></a><span data-ttu-id="c16ab-145">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="c16ab-145">Az.Functions</span></span>
* <span data-ttu-id="c16ab-146">[호환성이 손상되는 변경] 'Get-AzFunctionApp' 매개 변수 세트 하나를 제외한 모든 매개 변수 세트에서 'IncludeSlot' 스위치 매개 변수가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-146">[Breaking Change] Removed 'IncludeSlot' switch parameter from all but one parameter set of 'Get-AzFunctionApp'.</span></span> <span data-ttu-id="c16ab-147">이제 이 cmdlet은 '-IncludeSlot'이 지정된 경우 결과에서 배포 슬롯 검색을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-147">The cmdlet now supports retrieving deployment slots in the results when '-IncludeSlot' is specified.</span></span> 
* <span data-ttu-id="c16ab-148">'New-AzFunctionApp'이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-148">Updated 'New-AzFunctionApp':</span></span>
  - <span data-ttu-id="c16ab-149">이 옵션을 지정할 경우 application insights 프로젝트가 생성되지 않도록 -DisableApplicationInsights가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-149">Fixed -DisableApplicationInsights so that no application insights project is created when this option is specified.</span></span> <span data-ttu-id="c16ab-150">[#12728]</span><span class="sxs-lookup"><span data-stu-id="c16ab-150">[#12728]</span></span>
  - <span data-ttu-id="c16ab-151">[호환성이 손상되는 변경] PowerShell 6.2 함수 앱을 만드는 지원 기능이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-151">[Breaking Change] Removed support to create PowerShell 6.2 function apps.</span></span>
  - <span data-ttu-id="c16ab-152">[호환성이 손상되는 변경] RuntimeVersion 매개 변수가 지정되지 않은 경우 PowerShell 함수 앱에 대한 Windows의 Functions 버전 3 기본 런타임 버전이 6.2에서 7.0으로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-152">[Breaking Change] Changed the default runtime version in Functions version 3 on Windows for PowerShell function apps from 6.2 to 7.0 when the RuntimeVersion parameter is not specified.</span></span>
  - <span data-ttu-id="c16ab-153">[호환성이 손상되는 변경] RuntimeVersion 매개 변수가 지정되지 않은 경우 Node 함수 앱에 대한 Windows 및 Linux의 Functions 버전 3 기본 런타임 버전이 10에서 12로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-153">[Breaking Change] Changed the default runtime version in Functions version 3 on Windows and Linux for Node function apps from 10 to 12 when the RuntimeVersion parameter is not specified.</span></span>
  - <span data-ttu-id="c16ab-154">[호환성이 손상되는 변경] RuntimeVersion 매개 변수가 지정되지 않은 경우 Python 함수 앱에 대한 Linux의 Functions 버전 3 기본 런타임 버전이 3.7에서 3.8로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-154">[Breaking Change] Changed the default runtime version in Functions version 3 on Linux for Python function apps from 3.7 to 3.8 when the RuntimeVersion parameter is not specified.</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="c16ab-155">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="c16ab-155">Az.HDInsight</span></span>
 * <span data-ttu-id="c16ab-156">AzHDInsightCluster cmdlet의 경우:</span><span class="sxs-lookup"><span data-stu-id="c16ab-156">For New-AzHDInsightCluster cmdlet:</span></span>
     - <span data-ttu-id="c16ab-157">'DefaultStorageAccountName' 매개 변수가 'StorageAccountResourceId'로 대체되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-157">Replaced parameter 'DefaultStorageAccountName' with 'StorageAccountResourceId'</span></span>
     - <span data-ttu-id="c16ab-158">'DefaultStorageAccountKey' 매개 변수가 'StorageAccountKey'로 대체되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-158">Replaced parameter 'DefaultStorageAccountKey' with 'StorageAccountKey'</span></span>
     - <span data-ttu-id="c16ab-159">'DefaultStorageAccountType' 매개 변수가 'StorageAccountType'으로 대체되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-159">Replaced parameter 'DefaultStorageAccountType' with 'StorageAccountType'</span></span>
     - <span data-ttu-id="c16ab-160">'PublicNetworkAccessType' 매개 변수가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-160">Removed parameter 'PublicNetworkAccessType'</span></span>
     - <span data-ttu-id="c16ab-161">'OutboundPublicNetworkAccessType' 매개 변수가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-161">Removed parameter 'OutboundPublicNetworkAccessType'</span></span>
     - <span data-ttu-id="c16ab-162">새 매개 변수가 추가되었습니다. ADLSGen2를 지원하기 위한 'StorageFileSystem' 및 'StorageAccountManagedIdentity'</span><span class="sxs-lookup"><span data-stu-id="c16ab-162">Added new parameters: 'StorageFileSystem' and 'StorageAccountManagedIdentity' to support ADLSGen2</span></span>
     - <span data-ttu-id="c16ab-163">HDInsight ID Broker를 지원하기 위해 새 매개 변수 'EnableIDBroker'가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-163">Added new parameter 'EnableIDBroker' to Support HDInsight ID Broker</span></span>
     - <span data-ttu-id="c16ab-164">새 매개 변수가 추가되었습니다. Kafka Rest Proxy를 지원하기 위한 'KafkaClientGroupId', 'KafkaClientGroupName' 및 'KafkaManagementNodeSize'</span><span class="sxs-lookup"><span data-stu-id="c16ab-164">Added new parameters: 'KafkaClientGroupId', 'KafkaClientGroupName' and 'KafkaManagementNodeSize' to support Kafka Rest Proxy</span></span>
 * <span data-ttu-id="c16ab-165">New-AzHDInsightClusterConfig cmdlet의 경우:</span><span class="sxs-lookup"><span data-stu-id="c16ab-165">For New-AzHDInsightClusterConfig cmdlet:</span></span>
     - <span data-ttu-id="c16ab-166">'DefaultStorageAccountName' 매개 변수가 'StorageAccountResourceId'로 대체되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-166">Replaced parameter 'DefaultStorageAccountName' with 'StorageAccountResourceId'</span></span>
     - <span data-ttu-id="c16ab-167">'DefaultStorageAccountKey' 매개 변수가 'StorageAccountKey'로 대체되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-167">Replaced parameter 'DefaultStorageAccountKey' with 'StorageAccountKey'</span></span>
     - <span data-ttu-id="c16ab-168">'DefaultStorageAccountType' 매개 변수가 'StorageAccountType'으로 대체되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-168">Replaced parameter 'DefaultStorageAccountType' with 'StorageAccountType'</span></span>
     - <span data-ttu-id="c16ab-169">'PublicNetworkAccessType' 매개 변수가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-169">Removed parameter 'PublicNetworkAccessType'</span></span>
     - <span data-ttu-id="c16ab-170">'OutboundPublicNetworkAccessType' 매개 변수가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-170">Removed parameter 'OutboundPublicNetworkAccessType'</span></span>
* <span data-ttu-id="c16ab-171">Set-AzHDInsightDefaultStorage cmdlet의 경우:</span><span class="sxs-lookup"><span data-stu-id="c16ab-171">For Set-AzHDInsightDefaultStorage cmdlet:</span></span>
    - <span data-ttu-id="c16ab-172">'StorageAccountName' 매개 변수가 'StorageAccountResourceId'로 대체되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-172">Replaced parameter 'StorageAccountName' with 'StorageAccountResourceId'</span></span>
* <span data-ttu-id="c16ab-173">Add-AzHDInsightSecurityProfile cmdlet의 경우:</span><span class="sxs-lookup"><span data-stu-id="c16ab-173">For Add-AzHDInsightSecurityProfile cmdlet:</span></span>
    - <span data-ttu-id="c16ab-174">'Domain' 매개 변수가 'DomainResourceId'로 대체되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-174">Replaced parameter 'Domain' with 'DomainResourceId'</span></span>
    - <span data-ttu-id="c16ab-175">'OrganizationalUnitDN' 매개 변수에 대한 필수 요구 사항이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-175">Removed the mandatory requirement for parameter 'OrganizationalUnitDN'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="c16ab-176">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="c16ab-176">Az.KeyVault</span></span>
* <span data-ttu-id="c16ab-177">[호환성이 손상되는 변경] 'New-AzKeyVault'의 DisableSoftDelete 매개 변수와 'Update-AzKeyVault'의 EnableSoftDelete 매개 변수가 더 이상 사용되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-177">[Breaking Change] Deprecated parameter DisableSoftDelete in 'New-AzKeyVault' and EnableSoftDelete in 'Update-AzKeyVault'</span></span>
* <span data-ttu-id="c16ab-178">[호환성이 손상되는 변경] SecretValue를 직접 표시하지 않도록 SecretValueText 특성이 제거되었습니다. [#12266]</span><span class="sxs-lookup"><span data-stu-id="c16ab-178">[Breaking Change] Removed attribute SecretValueText to avoid displaying SecretValue directly [#12266]</span></span>
* <span data-ttu-id="c16ab-179">새 리소스 유형 지원: 관리형 HSM</span><span class="sxs-lookup"><span data-stu-id="c16ab-179">Supported new resource type: managed HSM</span></span>
    - <span data-ttu-id="c16ab-180">관리형 HSM의 CRUD와 관리형 HSM에서 키를 작동하는 cmdlet</span><span class="sxs-lookup"><span data-stu-id="c16ab-180">CRUD of managed HSM and cmdlets to operate keys on managed HSM</span></span>
    - <span data-ttu-id="c16ab-181">전체 HSM 백업/복원, AES 키 생성, 보안 도메인 백업/복원, RBAC</span><span class="sxs-lookup"><span data-stu-id="c16ab-181">Full HSM backup/restore, AES key creation, security domain backup/restore, RBAC</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="c16ab-182">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="c16ab-182">Az.ManagedServices</span></span>
* <span data-ttu-id="c16ab-183">[호환성이 손상되는 변경] 업데이트된 매개 변수 명명 규칙 및 관련 예제</span><span class="sxs-lookup"><span data-stu-id="c16ab-183">[Breaking Change] Updated parameters naming conventions and associated examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="c16ab-184">Az.Network</span><span class="sxs-lookup"><span data-stu-id="c16ab-184">Az.Network</span></span>
* <span data-ttu-id="c16ab-185">[호환성이 손상되는 변경] 'HostedSubnet' 매개 변수가 제거되고 'Subnet'이 대신 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-185">[Breaking Change] Removed parameter 'HostedSubnet' and added 'Subnet' instead</span></span>
* <span data-ttu-id="c16ab-186">가상 라우터 피어 경로에 대한 새 cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-186">Added new cmdlets for Virtual Router Peer Routes</span></span>
    - <span data-ttu-id="c16ab-187">'Get-AzVirtualRouterPeerLearnedRoute'</span><span class="sxs-lookup"><span data-stu-id="c16ab-187">'Get-AzVirtualRouterPeerLearnedRoute'</span></span>
    - <span data-ttu-id="c16ab-188">'Get-AzVirtualRouterPeerAdvertisedRoute'</span><span class="sxs-lookup"><span data-stu-id="c16ab-188">'Get-AzVirtualRouterPeerAdvertisedRoute'</span></span>
* <span data-ttu-id="c16ab-189">New-AzFirewall cmdlet이 업데이트됨:</span><span class="sxs-lookup"><span data-stu-id="c16ab-189">Updated New-AzFirewall cmdlet:</span></span>
    - <span data-ttu-id="c16ab-190">'-SkuTier' 매개 변수가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-190">Added parameter '-SkuTier'</span></span>
    - <span data-ttu-id="c16ab-191">'-SkuName' 매개 변수가 추가되었으며 Sku가 이 매개 변수의 별칭이 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-191">Added parameter '-SkuName' and made Sku as Alias for this</span></span>
    - <span data-ttu-id="c16ab-192">'-Sku' 매개 변수가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-192">Removed parameter '-Sku'</span></span>
* <span data-ttu-id="c16ab-193">[호환성이 손상되는 변경] 'Start-AzVpnConnectionPacketCapture' 및 'Stop-AzVpnConnectionPacketCapture'에서 'Connectionlink' 인수가 필수가 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-193">[Breaking Change] Made 'Connectionlink' argument mandatory in 'Start-AzVpnConnectionPacketCapture' and 'Stop-AzVpnConnectionPacketCapture'</span></span>
* <span data-ttu-id="c16ab-194">[호환성이 손상되는 변경] '-Filter' 매개 변수를 제거하도록 'New-AzNetworkWatcherConnectionMonitorEndPointObject'가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-194">[Breaking Change] Updated 'New-AzNetworkWatcherConnectionMonitorEndPointObject' to remove parameter '-Filter'</span></span>
* <span data-ttu-id="c16ab-195">[호환성이 손상되는 변경] 'New-AzNetworkWatcherConnectionMonitorEndpointFilterItemObject' cmdlet이 'New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject'로 대체되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-195">[Breaking Change] Replaced 'New-AzNetworkWatcherConnectionMonitorEndpointFilterItemObject' cmdlet with 'New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject'</span></span>
* <span data-ttu-id="c16ab-196">'New-AzNetworkWatcherConnectionMonitorEndPointObject' cmdlet이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-196">Updated 'New-AzNetworkWatcherConnectionMonitorEndPointObject' cmdlet:</span></span>
    - <span data-ttu-id="c16ab-197">'-Type' 매개 변수가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-197">Added parameter '-Type'</span></span>
    - <span data-ttu-id="c16ab-198">'-CoverageLevel' 매개 변수가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-198">Added parameter '-CoverageLevel'</span></span>
    - <span data-ttu-id="c16ab-199">'-Scope' 매개 변수가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-199">Added parameter '-Scope'</span></span>
* <span data-ttu-id="c16ab-200">'New-AzNetworkWatcherConnectionMonitorProtocolConfigurationObject' cmdlet이 새 매개 변수 '-DestinationPortBehavior'로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-200">Updated 'New-AzNetworkWatcherConnectionMonitorProtocolConfigurationObject' cmdlet with new parameter '-DestinationPortBehavior'</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="c16ab-201">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="c16ab-201">Az.RecoveryServices</span></span>
* <span data-ttu-id="c16ab-202">기여자 권한을 위해 워크로드 복원을 수정하는 중입니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-202">Fixing Workload Restore for contributor permissions.</span></span>
* <span data-ttu-id="c16ab-203">Restore-AzRecoveryServicesBackupItem cmdlet에 대한 새 매개 변수 집합 및 유효성 검사가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-203">Added new parameter sets and validations for Restore-AzRecoveryServicesBackupItem cmdlet.</span></span>

#### <a name="azresources"></a><span data-ttu-id="c16ab-204">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="c16ab-204">Az.Resources</span></span>
* <span data-ttu-id="c16ab-205">구문 분석 버그가 해결되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-205">Fixed parsing bug</span></span>
* <span data-ttu-id="c16ab-206">결과에서 미리 보기 메시지를 제거하도록 ARM 템플릿 What-If cmdlet이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-206">Updated ARM template What-If cmdlets to remove preview message from results</span></span>
* <span data-ttu-id="c16ab-207">'-WhatIf'가 상위 범위에서 설정된 경우 템플릿 배포 cmdlet의 작동이 중단되는 문제가 해결되었습니다. [#13038]</span><span class="sxs-lookup"><span data-stu-id="c16ab-207">Fixed an issue where template deployment cmdlets crash if '-WhatIf' is set at a higher scope [#13038]</span></span>
* <span data-ttu-id="c16ab-208">템플릿 배포 cmdlet이 템플릿 매개 변수에서 대/소문자를 구분하지 않는 문제가 해결되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-208">Fixed an issue where template deployment cmdlets does not preserve case for template parameters</span></span>
* <span data-ttu-id="c16ab-209">'Export-AzResourceGroup' cmdlet에 사용되는 기본 API 버전이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-209">Added a default API version to be used in 'Export-AzResourceGroup' cmdlet</span></span>
* <span data-ttu-id="c16ab-210">템플릿 사양에 대한 cmdlet이 추가되었습니다('Get-AzTemplateSpec', 'Set-AzTemplateSpec', 'New-AzTemplateSpec', 'Remove-AzTemplateSpec', 'Export-AzTemplateSpec').</span><span class="sxs-lookup"><span data-stu-id="c16ab-210">Added cmdlets for Template Specs ('Get-AzTemplateSpec', 'Set-AzTemplateSpec', 'New-AzTemplateSpec', 'Remove-AzTemplateSpec', 'Export-AzTemplateSpec')</span></span>
* <span data-ttu-id="c16ab-211">새 -TemplateSpecId 매개 변수를 통해 기존 배포 cmdlet을 사용하여 템플릿 사양을 배포하도록 지원하는 기능이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-211">Added support for deploying Template Specs using existing deployment cmdlets (via the new -TemplateSpecId parameter)</span></span> 
* <span data-ttu-id="c16ab-212">SDK를 사용하도록 'Get-AzResourceGroupDeploymentOperation'이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-212">Updated 'Get-AzResourceGroupDeploymentOperation' to use the SDK.</span></span>
* <span data-ttu-id="c16ab-213">'\*-AzDeployment' cmdlet에서 '-ApiVersion' 매개 변수가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-213">Removed '-ApiVersion' parameter from '\*-AzDeployment' cmdlets.</span></span>

#### <a name="azsql"></a><span data-ttu-id="c16ab-214">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="c16ab-214">Az.Sql</span></span>
* <span data-ttu-id="c16ab-215">networkIsolation이 지정되지 않은 경우 New-AzSqlDatabaseExport가 실패하는 문제가 해결되었습니다. [#13097]</span><span class="sxs-lookup"><span data-stu-id="c16ab-215">Fixed issue where New-AzSqlDatabaseExport fails if networkIsolation not specified [#13097]</span></span>
* <span data-ttu-id="c16ab-216">New-AzSqlDatabaseExport 및 New-AzSqlDatabaseImport가 결과 개체에 OperationStatusLink를 반환하지 않는 문제가 해결되었습니다. [#13097]</span><span class="sxs-lookup"><span data-stu-id="c16ab-216">Fixed issue where New-AzSqlDatabaseExport and New-AzSqlDatabaseImport were not returning OperationStatusLink in the result object [#13097]</span></span>
* <span data-ttu-id="c16ab-217">백업 스토리지 중복성 경고에서 Azure 쌍을 이루는 지역 URL이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-217">Update Azure Paired Regions URL in Backup Storage Redundancy Warnings</span></span> 

#### <a name="azstorage"></a><span data-ttu-id="c16ab-218">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="c16ab-218">Az.Storage</span></span>
* <span data-ttu-id="c16ab-219">더 이상 사용되지 않는 RestorePolicy.LastEnabledTime 속성이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-219">Removed obsolete property RestorePolicy.LastEnabledTime</span></span>
    - <span data-ttu-id="c16ab-220">'Enable-AzStorageBlobRestorePolicy'</span><span class="sxs-lookup"><span data-stu-id="c16ab-220">'Enable-AzStorageBlobRestorePolicy'</span></span>
    - <span data-ttu-id="c16ab-221">'Disable-AzStorageBlobRestorePolicy'</span><span class="sxs-lookup"><span data-stu-id="c16ab-221">'Disable-AzStorageBlobRestorePolicy'</span></span>
    - <span data-ttu-id="c16ab-222">'Get-AzStorageBlobServiceProperty'</span><span class="sxs-lookup"><span data-stu-id="c16ab-222">'Get-AzStorageBlobServiceProperty'</span></span>
    - <span data-ttu-id="c16ab-223">'Update-AzStorageBlobServiceProperty'</span><span class="sxs-lookup"><span data-stu-id="c16ab-223">'Update-AzStorageBlobServiceProperty'</span></span>
* <span data-ttu-id="c16ab-224">DaysAfterModificationGreaterThan의 Type이 int에서 int?로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-224">Change Type of DaysAfterModificationGreaterThan from int to int?</span></span>
    - <span data-ttu-id="c16ab-225">'Set-AzStorageAccountManagementPolicy'</span><span class="sxs-lookup"><span data-stu-id="c16ab-225">'Set-AzStorageAccountManagementPolicy'</span></span>
    - <span data-ttu-id="c16ab-226">'Get-AzStorageAccountManagementPolicy'</span><span class="sxs-lookup"><span data-stu-id="c16ab-226">'Get-AzStorageAccountManagementPolicy'</span></span>
    - <span data-ttu-id="c16ab-227">'Add-AzStorageAccountManagementPolicyAction'</span><span class="sxs-lookup"><span data-stu-id="c16ab-227">'Add-AzStorageAccountManagementPolicyAction'</span></span>
    - <span data-ttu-id="c16ab-228">'New-AzStorageAccountManagementPolicyRule'</span><span class="sxs-lookup"><span data-stu-id="c16ab-228">'New-AzStorageAccountManagementPolicyRule'</span></span>
* <span data-ttu-id="c16ab-229">액세스 계층을 사용한 파일 공유 생성/업데이트가 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-229">Supported create/update file share with access tier</span></span>
    - <span data-ttu-id="c16ab-230">'New-AzRmStorageShare'</span><span class="sxs-lookup"><span data-stu-id="c16ab-230">'New-AzRmStorageShare'</span></span>
    - <span data-ttu-id="c16ab-231">'Update-AzRmStorageShare'</span><span class="sxs-lookup"><span data-stu-id="c16ab-231">'Update-AzRmStorageShare'</span></span>
* <span data-ttu-id="c16ab-232">Datalake Gen2 항목에서 Acl의 재귀적 설정/업데이트/제거가 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-232">Supported set/update/remove Acl recursively on Datalake Gen2 item</span></span> 
    -  <span data-ttu-id="c16ab-233">'Set-AzDataLakeGen2AclRecursive'</span><span class="sxs-lookup"><span data-stu-id="c16ab-233">'Set-AzDataLakeGen2AclRecursive'</span></span> 
    -  <span data-ttu-id="c16ab-234">'Update-AzDataLakeGen2AclRecursive'</span><span class="sxs-lookup"><span data-stu-id="c16ab-234">'Update-AzDataLakeGen2AclRecursive'</span></span> 
    -  <span data-ttu-id="c16ab-235">'Remove-AzDataLakeGen2AclRecursive'</span><span class="sxs-lookup"><span data-stu-id="c16ab-235">'Remove-AzDataLakeGen2AclRecursive'</span></span>
* <span data-ttu-id="c16ab-236">새 권한 x,t를 사용하여 컨테이너 액세스 정책 지원</span><span class="sxs-lookup"><span data-stu-id="c16ab-236">Supported Container access policy with new permission x,t</span></span>
    -  <span data-ttu-id="c16ab-237">'New-AzStorageContainerStoredAccessPolicy'</span><span class="sxs-lookup"><span data-stu-id="c16ab-237">'New-AzStorageContainerStoredAccessPolicy'</span></span>
    -  <span data-ttu-id="c16ab-238">'Set-AzStorageContainerStoredAccessPolicy'</span><span class="sxs-lookup"><span data-stu-id="c16ab-238">'Set-AzStorageContainerStoredAccessPolicy'</span></span>
* <span data-ttu-id="c16ab-239">자식 속성 권한 유형을 열거형에서 문자열로 변경하여 컨테이너 액세스 정책 가져오기/설정 cmdlet의 출력을 변경했습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-239">Changed the output of get/set Container access policy cmdlet, by change the child property Permission type from enum to String</span></span>
    -  <span data-ttu-id="c16ab-240">'Get-AzStorageContainerStoredAccessPolicy'</span><span class="sxs-lookup"><span data-stu-id="c16ab-240">'Get-AzStorageContainerStoredAccessPolicy'</span></span>
    -  <span data-ttu-id="c16ab-241">'Set-AzStorageContainerStoredAccessPolicy'</span><span class="sxs-lookup"><span data-stu-id="c16ab-241">'Set-AzStorageContainerStoredAccessPolicy'</span></span>
* <span data-ttu-id="c16ab-242">json을 사용한 관리 정책 설정의 샘플 스크립트 문제가 해결되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-242">Fixed a sample script issue of set management policy with json</span></span>
    -  <span data-ttu-id="c16ab-243">'Set-AzStorageAccountManagementPolicy'</span><span class="sxs-lookup"><span data-stu-id="c16ab-243">'Set-AzStorageAccountManagementPolicy'</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="c16ab-244">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="c16ab-244">Az.Websites</span></span>
* <span data-ttu-id="c16ab-245">Premium V3 가격 책정 계층에 대한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-245">Added support for Premium V3 pricing tier</span></span>
* <span data-ttu-id="c16ab-246">WebSites SDK가 3.1.0으로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-246">Updated the WebSites SDK to 3.1.0</span></span>

### <a name="thanks-to-our-community-contributors"></a><span data-ttu-id="c16ab-247">커뮤니티 기여자에게 감사드립니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-247">Thanks to our community contributors</span></span>
* <span data-ttu-id="c16ab-248">@atul-ram, Get-AzDelegation.md 업데이트(#13176)</span><span class="sxs-lookup"><span data-stu-id="c16ab-248">@atul-ram, Update Get-AzDelegation.md (#13176)</span></span>
* <span data-ttu-id="c16ab-249">@dineshreddy007, WAC 토큰을 사용하여 Stack HCI를 등록하는 경우 올바르게 할당된 앱 역할을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-249">@dineshreddy007, Get the App Roles assigned correctly in case of Stack HCI registration using WAC token.</span></span> <span data-ttu-id="c16ab-250">(#13249)</span><span class="sxs-lookup"><span data-stu-id="c16ab-250">(#13249)</span></span>
* <span data-ttu-id="c16ab-251">@kongou-ae, New-AzOffice365PolicyProperty.md 업데이트(#13217)</span><span class="sxs-lookup"><span data-stu-id="c16ab-251">@kongou-ae, Update New-AzOffice365PolicyProperty.md (#13217)</span></span>
* <span data-ttu-id="c16ab-252">Lohith Chowdary Chilukuri(@Lochiluk), Set-AzApplicationGateway.md 업데이트(#13150)</span><span class="sxs-lookup"><span data-stu-id="c16ab-252">Lohith Chowdary Chilukuri (@Lochiluk), Update Set-AzApplicationGateway.md (#13150)</span></span>
* <span data-ttu-id="c16ab-253">Matthew Burleigh(@mburleigh)</span><span class="sxs-lookup"><span data-stu-id="c16ab-253">Matthew Burleigh (@mburleigh)</span></span>
  * <span data-ttu-id="c16ab-254">문서에서 참조된 PowerShell cmdlet에 대한 링크 추가(#13203)</span><span class="sxs-lookup"><span data-stu-id="c16ab-254">Add links to PowerShell cmdlets referenced in the document (#13203)</span></span>
  * <span data-ttu-id="c16ab-255">문서에서 참조된 PowerShell cmdlet에 대한 링크 추가(#13190)</span><span class="sxs-lookup"><span data-stu-id="c16ab-255">Add links to PowerShell cmdlets referenced in the document (#13190)</span></span>
  * <span data-ttu-id="c16ab-256">문서에서 참조된 PowerShell cmdlet에 대한 링크 추가(#13189)</span><span class="sxs-lookup"><span data-stu-id="c16ab-256">Add links to PowerShell cmdlets referenced in the document (#13189)</span></span>
  * <span data-ttu-id="c16ab-257">참조된 cmdlet에 대한 링크 추가(#13137)</span><span class="sxs-lookup"><span data-stu-id="c16ab-257">add links to referenced cmdlets (#13137)</span></span>
  * <span data-ttu-id="c16ab-258">문서에서 참조된 PowerShell cmdlet에 대한 링크 추가(#13204)</span><span class="sxs-lookup"><span data-stu-id="c16ab-258">Add links to PowerShell cmdlets referenced in the document (#13204)</span></span>
  * <span data-ttu-id="c16ab-259">문서에서 참조된 PowerShell cmdlet에 대한 링크 추가(#13205)</span><span class="sxs-lookup"><span data-stu-id="c16ab-259">Add links to PowerShell cmdlets referenced in the document (#13205)</span></span>

## <a name="480---october-2020"></a><span data-ttu-id="c16ab-260">4.8.0 - 2020년 10월</span><span class="sxs-lookup"><span data-stu-id="c16ab-260">4.8.0 - October 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="c16ab-261">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="c16ab-261">Az.Accounts</span></span>
* <span data-ttu-id="c16ab-262">공용 라이브러리의 DateTime 구문 분석 문제 해결[#13045]</span><span class="sxs-lookup"><span data-stu-id="c16ab-262">Fixed DateTime parse issue in common libraries [#13045]</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="c16ab-263">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="c16ab-263">Az.CognitiveServices</span></span>
* <span data-ttu-id="c16ab-264">'New-AzCognitiveServicesAccountApiProperty' cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-264">Added 'New-AzCognitiveServicesAccountApiProperty' cmdlet.</span></span>
* <span data-ttu-id="c16ab-265">'New-AzCognitiveServicesAccount' 및 'Set-AzCognitiveServicesAccount'에 대해 'ApiProperty' 매개 변수 지원됨</span><span class="sxs-lookup"><span data-stu-id="c16ab-265">Supported 'ApiProperty' parameter for 'New-AzCognitiveServicesAccount' and 'Set-AzCognitiveServicesAccount'</span></span>

#### <a name="azcompute"></a><span data-ttu-id="c16ab-266">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="c16ab-266">Az.Compute</span></span>
* <span data-ttu-id="c16ab-267">FailoverTypes를 채워서 'Update-ASRRecoveryPlan'의 문제 해결</span><span class="sxs-lookup"><span data-stu-id="c16ab-267">Fixed issue in 'Update-ASRRecoveryPlan' by populating FailoverTypes</span></span>
* <span data-ttu-id="c16ab-268">'Get-AzVmImage' cmdlet에 '-Top' 및 '-OrderBy' 선택적 매개 변수를 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-268">Added the '-Top' and '-OrderBy' optional parameters to the 'Get-AzVmImage' cmdlet.</span></span> 

#### <a name="azdatabricks"></a><span data-ttu-id="c16ab-269">Az.Databricks</span><span class="sxs-lookup"><span data-stu-id="c16ab-269">Az.Databricks</span></span>
* <span data-ttu-id="c16ab-270">'Az.Databricks' 모듈의 일반 공급</span><span class="sxs-lookup"><span data-stu-id="c16ab-270">General availability of 'Az.Databricks' module</span></span>
* <span data-ttu-id="c16ab-271">가상 네트워크 피어링에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="c16ab-271">Added support for virtual network peering</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="c16ab-272">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="c16ab-272">Az.DataFactory</span></span>
* <span data-ttu-id="c16ab-273">출력 메시지의 오타 수정</span><span class="sxs-lookup"><span data-stu-id="c16ab-273">Fixed typo in output messages</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="c16ab-274">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="c16ab-274">Az.EventHub</span></span>
* <span data-ttu-id="c16ab-275">선택적 스위치 매개 변수 'TrustedServiceAccessEnabled'를 'Set-AzEventHubNetworkRuleSet' cmdlet에 추가</span><span class="sxs-lookup"><span data-stu-id="c16ab-275">Added optional switch parameter 'TrustedServiceAccessEnabled' to 'Set-AzEventHubNetworkRuleSet' cmdlet</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="c16ab-276">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="c16ab-276">Az.HDInsight</span></span>
* <span data-ttu-id="c16ab-277">'PublicNetworkAccessType' 및 'OutboundPublicNetworkAccessType' 매개 변수 사용 중단 계획에 대한 경고 메시지 추가</span><span class="sxs-lookup"><span data-stu-id="c16ab-277">Added warning message for planning to deprecate the parameters 'PublicNetworkAccessType' and 'OutboundPublicNetworkAccessType'</span></span>
* <span data-ttu-id="c16ab-278">'DefaultStorageAccountName' 매개 변수를 'StorageAccountResourceId'로 바꾸려는 계획에 대한 경고 메시지 추가</span><span class="sxs-lookup"><span data-stu-id="c16ab-278">Added warning message for planning to replace the parameter 'DefaultStorageAccountName' with 'StorageAccountResourceId'</span></span>
* <span data-ttu-id="c16ab-279">'DefaultStorageAccountKey' 매개 변수를 'StorageAccountKey'로 바꾸려는 계획에 대한 경고 메시지 추가</span><span class="sxs-lookup"><span data-stu-id="c16ab-279">Added warning message for planning to replace the parameter 'DefaultStorageAccountKey' with 'StorageAccountKey'</span></span>
* <span data-ttu-id="c16ab-280">'DefaultStorageAccountType' 매개 변수를 'StorageAccountType'으로 바꾸려는 계획에 대한 경고 메시지 추가</span><span class="sxs-lookup"><span data-stu-id="c16ab-280">Added warning message for planning to replace the parameter 'DefaultStorageAccountType' with 'StorageAccountType'</span></span>
* <span data-ttu-id="c16ab-281">'DefaultStorageContainer' 매개 변수를 'StorageContainer'로 바꾸려는 계획에 대한 경고 메시지 추가</span><span class="sxs-lookup"><span data-stu-id="c16ab-281">Added warning message for planning to replace the parameter 'DefaultStorageContainer' with 'StorageContainer'</span></span>
* <span data-ttu-id="c16ab-282">'DefaultStorageRootPath' 매개 변수를 'StorageRootPath'로 바꾸려는 계획에 대한 경고 메시지 추가</span><span class="sxs-lookup"><span data-stu-id="c16ab-282">Added warning message for planning to replace the parameter 'DefaultStorageRootPath' with 'StorageRootPath'</span></span>

#### <a name="aziothub"></a><span data-ttu-id="c16ab-283">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="c16ab-283">Az.IotHub</span></span>
* <span data-ttu-id="c16ab-284">업데이트된 디바이스 SDK.</span><span class="sxs-lookup"><span data-stu-id="c16ab-284">Updated devices sdk.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="c16ab-285">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="c16ab-285">Az.KeyVault</span></span>
* <span data-ttu-id="c16ab-286">SecretValueText 속성 제거 세부 날짜 제공</span><span class="sxs-lookup"><span data-stu-id="c16ab-286">Provided the detailed date of removing property SecretValueText</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="c16ab-287">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="c16ab-287">Az.ManagedServices</span></span>
* <span data-ttu-id="c16ab-288">관리되는 서비스 할당 및 정의의 cmdlet에 대한 호환성이 손상되는 변경 경고가 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="c16ab-288">Updated breaking change warnings on cmdlets of managed services assignment and definition</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="c16ab-289">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="c16ab-289">Az.Monitor</span></span>
* <span data-ttu-id="c16ab-290">경고 메시지를 숨길 수 없는 버그를 수정했습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-290">Fixed the bug that warning message cannot be suppressed.</span></span> <span data-ttu-id="c16ab-291">[#12889]</span><span class="sxs-lookup"><span data-stu-id="c16ab-291">[#12889]</span></span>
* <span data-ttu-id="c16ab-292">경고 규칙 기준에서 'SkipMetricValidation' 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-292">Supported 'SkipMetricValidation' parameter in alert rule criteria.</span></span> <span data-ttu-id="c16ab-293">메트릭 유효성 검사를 건너뛰도록 하여 아직 생성되지 않은 사용자 지정 메트릭에 대한 경고 규칙을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-293">Allows creating an alert rule on a custom metric that isn't yet emitted, by causing the metric validation to be skipped.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="c16ab-294">Az.Network</span><span class="sxs-lookup"><span data-stu-id="c16ab-294">Az.Network</span></span>
* <span data-ttu-id="c16ab-295">VPNSite 리소스에 Office365 정책 추가</span><span class="sxs-lookup"><span data-stu-id="c16ab-295">Added Office365 Policy to VPNSite Resource</span></span>
    - <span data-ttu-id="c16ab-296">'New-AzO365PolicyProperty'</span><span class="sxs-lookup"><span data-stu-id="c16ab-296">'New-AzO365PolicyProperty'</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="c16ab-297">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="c16ab-297">Az.RecoveryServices</span></span>
* <span data-ttu-id="c16ab-298">워크로드 백업에 대한 컨테이너 이름 유효성 검사가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-298">Added container name validation for workload backup.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="c16ab-299">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="c16ab-299">Az.RedisCache</span></span>
* <span data-ttu-id="c16ab-300">Microsoft.Cache RP 등록과 관련된 권한 문제로 인해 'New-AzRedisCache' 및 'Set-AzRedisCache' cmdlet이 실패하지 않도록 함</span><span class="sxs-lookup"><span data-stu-id="c16ab-300">Made 'New-AzRedisCache' and 'Set-AzRedisCache' cmdlets not fail because of permission issue related to registering Microsoft.Cache RP</span></span>

#### <a name="azsql"></a><span data-ttu-id="c16ab-301">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="c16ab-301">Az.Sql</span></span>
* <span data-ttu-id="c16ab-302">BackupStorageRedundancy가 다음에 추가됨</span><span class="sxs-lookup"><span data-stu-id="c16ab-302">Added BackupStorageRedundancy to the following:</span></span> 
    - <span data-ttu-id="c16ab-303">'Restore-AzureRmSqlDatabase'</span><span class="sxs-lookup"><span data-stu-id="c16ab-303">'Restore-AzureRmSqlDatabase'</span></span>
    - <span data-ttu-id="c16ab-304">'New-AzSqlDatabaseCopy'</span><span class="sxs-lookup"><span data-stu-id="c16ab-304">'New-AzSqlDatabaseCopy'</span></span>
    - <span data-ttu-id="c16ab-305">'New-AzSqlDatabaseSecondary'</span><span class="sxs-lookup"><span data-stu-id="c16ab-305">'New-AzSqlDatabaseSecondary'</span></span>
* <span data-ttu-id="c16ab-306">모든 SQL DB 참조에 대한 BackupStorageRedundancy 매개 변수의 대소문자 구분 제거</span><span class="sxs-lookup"><span data-stu-id="c16ab-306">Removed case sensitivity for BackupStorageRedundancy parameter for all SQL DB references</span></span> 
* <span data-ttu-id="c16ab-307">BackupStorageRedundancy 경고 메시지 이름 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="c16ab-307">Updated BackupStorageRedundancy warning message names</span></span>

#### <a name="azstorage"></a><span data-ttu-id="c16ab-308">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="c16ab-308">Az.Storage</span></span>
* <span data-ttu-id="c16ab-309">스토리지 계정의 파일 서비스에서 사용/사용하지 않음/공유 일시 삭제 속성 지원</span><span class="sxs-lookup"><span data-stu-id="c16ab-309">Supported enable/disable/get share soft delete properties on file Service of a Storage account</span></span>
    - <span data-ttu-id="c16ab-310">'Update-AzStorageFileServiceProperty'</span><span class="sxs-lookup"><span data-stu-id="c16ab-310">'Update-AzStorageFileServiceProperty'</span></span>
    - <span data-ttu-id="c16ab-311">'Get-AzStorageFileServiceProperty'</span><span class="sxs-lookup"><span data-stu-id="c16ab-311">'Get-AzStorageFileServiceProperty'</span></span>
* <span data-ttu-id="c16ab-312">지원되는 목록 파일 공유에는 스토리지 계정의 삭제된 공유와 단일 파일 공유 사용량 가져오기가 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-312">Supported list file shares include the deleted ones of a Storage account, and Get single file share usage</span></span>
    - <span data-ttu-id="c16ab-313">'Get-AzRmStorageShare'</span><span class="sxs-lookup"><span data-stu-id="c16ab-313">'Get-AzRmStorageShare'</span></span>
* <span data-ttu-id="c16ab-314">삭제된 파일 공유 복원 지원</span><span class="sxs-lookup"><span data-stu-id="c16ab-314">Supported restore a deleted file share</span></span>
    - <span data-ttu-id="c16ab-315">'Restore-AzRmStorageShare'</span><span class="sxs-lookup"><span data-stu-id="c16ab-315">'Restore-AzRmStorageShare'</span></span>
* <span data-ttu-id="c16ab-316">Blob 서비스 속성을 수정하기 위한 cmdlet을 변경하여, 서버에서 원래 속성을 가져오지 않으며 수정된 속성만 서버로 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-316">Changed the cmdlets for modify blob service properties, won't get the original properties from server, but only set the modified properties to server.</span></span>
    - <span data-ttu-id="c16ab-317">'Enable-AzStorageBlobDeleteRetentionPolicy'</span><span class="sxs-lookup"><span data-stu-id="c16ab-317">'Enable-AzStorageBlobDeleteRetentionPolicy'</span></span>
    - <span data-ttu-id="c16ab-318">'Disable-AzStorageBlobDeleteRetentionPolicy'</span><span class="sxs-lookup"><span data-stu-id="c16ab-318">'Disable-AzStorageBlobDeleteRetentionPolicy'</span></span>  
    - <span data-ttu-id="c16ab-319">'Enable-AzStorageBlobRestorePolicy'</span><span class="sxs-lookup"><span data-stu-id="c16ab-319">'Enable-AzStorageBlobRestorePolicy'</span></span>
    - <span data-ttu-id="c16ab-320">'Disable-AzStorageBlobRestorePolicy'</span><span class="sxs-lookup"><span data-stu-id="c16ab-320">'Disable-AzStorageBlobRestorePolicy'</span></span>
    - <span data-ttu-id="c16ab-321">'Update-AzStorageBlobServiceProperty'</span><span class="sxs-lookup"><span data-stu-id="c16ab-321">'Update-AzStorageBlobServiceProperty'</span></span>
* <span data-ttu-id="c16ab-322">New-AzStorageAccount 매개 변수 -Kind 기본값에 대한 도움말 문제 해결[#12189]</span><span class="sxs-lookup"><span data-stu-id="c16ab-322">Fixed help issue for New-AzStorageAccount parameter -Kind default value [#12189]</span></span>
* <span data-ttu-id="c16ab-323">Blob 업로드에서 올바른 ContentType을 설정하는 방법을 보여주는 예제를 추가하여 문제 해결[#12989]</span><span class="sxs-lookup"><span data-stu-id="c16ab-323">Fixed issue by add example to show how to set correct ContentType in blob upload [#12989]</span></span>

## <a name="470---september-2020"></a><span data-ttu-id="c16ab-324">4.7.0 - 2020년 9월</span><span class="sxs-lookup"><span data-stu-id="c16ab-324">4.7.0 - September 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="c16ab-325">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="c16ab-325">Az.Accounts</span></span>
* <span data-ttu-id="c16ab-326">예정된 호환성이 손상되는 변경 메시지의 형식이 지정됨</span><span class="sxs-lookup"><span data-stu-id="c16ab-326">Formatted the upcoming breaking change messages</span></span>
* <span data-ttu-id="c16ab-327">Azure.Core가 1.4.1로 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="c16ab-327">Updated Azure.Core to 1.4.1</span></span>

#### <a name="azaks"></a><span data-ttu-id="c16ab-328">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="c16ab-328">Az.Aks</span></span>
* <span data-ttu-id="c16ab-329">'New-AzAksCluster', 'Set-AzAksCluster' 및 'New-AzAksNodePool'에 대한 클라이언트 쪽 매개 변수 유효성 검사 논리가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-329">Added client side parameter validation logic for 'New-AzAksCluster', 'Set-AzAksCluster' and 'New-AzAksNodePool'.</span></span> <span data-ttu-id="c16ab-330">[#12372]</span><span class="sxs-lookup"><span data-stu-id="c16ab-330">[#12372]</span></span>
* <span data-ttu-id="c16ab-331">'New-AzAksCluster'에서 추가 항목에 대한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-331">Added support for add-ons in 'New-AzAksCluster'.</span></span> <span data-ttu-id="c16ab-332">[#11239]</span><span class="sxs-lookup"><span data-stu-id="c16ab-332">[#11239]</span></span>
* <span data-ttu-id="c16ab-333">추가 항목에 대한 'Enable-AzAksAddOn' 및 'Disable-AzAksAddOn' cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-333">Added cmdlets 'Enable-AzAksAddOn' and 'Disable-AzAksAddOn' for add-ons.</span></span> <span data-ttu-id="c16ab-334">[#11239]</span><span class="sxs-lookup"><span data-stu-id="c16ab-334">[#11239]</span></span>
* <span data-ttu-id="c16ab-335">'New-AzAksCluster'에 대한 매개 변수 'GenerateSshKey'가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-335">Added parameter 'GenerateSshKey' for 'New-AzAksCluster'.</span></span> <span data-ttu-id="c16ab-336">[#12371]</span><span class="sxs-lookup"><span data-stu-id="c16ab-336">[#12371]</span></span>
* <span data-ttu-id="c16ab-337">API 버전이 2020-06-01로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-337">Updated api version to 2020-06-01.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="c16ab-338">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="c16ab-338">Az.CognitiveServices</span></span>
* <span data-ttu-id="c16ab-339">특정 API에 대한 추가 법률 용어를 표시했습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-339">Showed additional legal terms for certain APIs.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="c16ab-340">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="c16ab-340">Az.Compute</span></span>
* <span data-ttu-id="c16ab-341">'New-AzVmDiskEncryptionSetConfig'에 '-EncryptionType' 선택적 매개 변수가 추가됨</span><span class="sxs-lookup"><span data-stu-id="c16ab-341">Added the '-EncryptionType' optional parameter to 'New-AzVmDiskEncryptionSetConfig'</span></span>
* <span data-ttu-id="c16ab-342">새 리소스 종류에 대한 새 cmdlet: DiskAccess 'Get-AzDiskAccess', 'New-AzDiskAccess', 'Get-AzDiskAccess'</span><span class="sxs-lookup"><span data-stu-id="c16ab-342">New cmdlets for new resource type: DiskAccess 'Get-AzDiskAccess', 'New-AzDiskAccess', 'Get-AzDiskAccess'</span></span>
* <span data-ttu-id="c16ab-343">'New-AzSnapshotConfig'에 선택적 매개 변수 '-DiskAccessId' 및 '-NetworkAccessPolicy'가 추가됨</span><span class="sxs-lookup"><span data-stu-id="c16ab-343">Added optional parameters '-DiskAccessId' and '-NetworkAccessPolicy' to 'New-AzSnapshotConfig'</span></span>
* <span data-ttu-id="c16ab-344">'New-AzDiskConfig'에 선택적 매개 변수 '-DiskAccessId' 및 '-NetworkAccessPolicy'가 추가됨</span><span class="sxs-lookup"><span data-stu-id="c16ab-344">Added optional parameters '-DiskAccessId' and '-NetworkAccessPolicy' to 'New-AzDiskConfig'</span></span>
* <span data-ttu-id="c16ab-345">VirtualMachine 인스턴스 보기에 'PatchStatus' 속성이 추가됨</span><span class="sxs-lookup"><span data-stu-id="c16ab-345">Added 'PatchStatus' property to VirtualMachine Instance View</span></span>
* <span data-ttu-id="c16ab-346">가상 머신의 인스턴스 보기에 'VMHealth' 속성이 추가됨. 이 속성은 'Get-AzVm'이 '-Status'로 호출될 때 반환되는 개체</span><span class="sxs-lookup"><span data-stu-id="c16ab-346">Added 'VMHealth' property to the virtual machine's instance view, which is the returned object when 'Get-AzVm' is invoked with '-Status'</span></span>
* <span data-ttu-id="c16ab-347">'Get-AzVM' 및 'Get-AzVmss' 인스턴스 보기에 'AssignedHost' 필드가 추가됨</span><span class="sxs-lookup"><span data-stu-id="c16ab-347">Added 'AssignedHost' field to 'Get-AzVM' and 'Get-AzVmss' instance views.</span></span> <span data-ttu-id="c16ab-348">필드는 가상 머신 인스턴스의 리소스 ID를 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-348">The field shows the resource id of the virtual machine instance</span></span>
* <span data-ttu-id="c16ab-349">선택적 매개 변수 '-SupportAutomaticPlacement'가 'New-AzHostGroup'에 추가됨</span><span class="sxs-lookup"><span data-stu-id="c16ab-349">Added optional parameter '-SupportAutomaticPlacement' to 'New-AzHostGroup'</span></span> 
* <span data-ttu-id="c16ab-350">'-HostGroupId' 매개 변수가 'New-AzVm' 및 'New-AzVmss'에 추가됨</span><span class="sxs-lookup"><span data-stu-id="c16ab-350">Added the '-HostGroupId' parameter to 'New-AzVm' and 'New-AzVmss'</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="c16ab-351">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="c16ab-351">Az.DataFactory</span></span>
* <span data-ttu-id="c16ab-352">ADF .Net SDK 버전이 4.11.0으로 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="c16ab-352">Updated ADF .Net SDK version to 4.11.0</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="c16ab-353">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="c16ab-353">Az.EventHub</span></span>
* <span data-ttu-id="c16ab-354">새 클러스터 cmdlet 추가됨 - 'New-AzEventHubCluster', 'Set-AzEventHubCluster', 'Get-AzEventHubCluster', 'Remove-AzEventHubCluster', 'Get-AzEventHubClustersAvailableRegions'</span><span class="sxs-lookup"><span data-stu-id="c16ab-354">Added new Cluster cmdlets - 'New-AzEventHubCluster', 'Set-AzEventHubCluster', 'Get-AzEventHubCluster', 'Remove-AzEventHubCluster', 'Get-AzEventHubClustersAvailableRegions'.</span></span>
* <span data-ttu-id="c16ab-355">#10722 문제 해결됨: AuthorizationRule 권한에 'Listen'만 할당하는 문제가 해결되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-355">Fixed for issue #10722 : Fix for assigning only 'Listen' to AuthorizationRule rights.</span></span>

#### <a name="azfunctions"></a><span data-ttu-id="c16ab-356">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="c16ab-356">Az.Functions</span></span>
* <span data-ttu-id="c16ab-357">v2 Functions를 지원하지 않는 지역에서 생성하는 기능이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-357">Removed the ability to create v2 Functions in regions that do not support it.</span></span>
* <span data-ttu-id="c16ab-358">PowerShell 6.2가 사용되지 않음</span><span class="sxs-lookup"><span data-stu-id="c16ab-358">Deprecated PowerShell 6.2.</span></span> <span data-ttu-id="c16ab-359">사용자가 PowerShell 6.2 함수 앱을 만들 때 PowerShell 7.0 함수 앱을 만들도록 권장하는 경고가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-359">Added a warning for when a user creates a PowerShell 6.2 function app that advises them to create a PowerShell 7.0 function app instead.</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="c16ab-360">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="c16ab-360">Az.HDInsight</span></span>
* <span data-ttu-id="c16ab-361">자동 크기 조정 구성을 사용하여 클러스터 만들기 지원</span><span class="sxs-lookup"><span data-stu-id="c16ab-361">Supported creating cluster with Autoscale configuration</span></span>
    - <span data-ttu-id="c16ab-362">cmdlet 'New-AzHDInsightCluster'에 새 매개 변수 'AutoscaleConfiguration' 추가</span><span class="sxs-lookup"><span data-stu-id="c16ab-362">Add new parameter 'AutoscaleConfiguration' to the cmdlet 'New-AzHDInsightCluster'</span></span>
* <span data-ttu-id="c16ab-363">운영 클러스터의 자동 크기 조정 구성 지원됨</span><span class="sxs-lookup"><span data-stu-id="c16ab-363">Supported operating cluster's Autoscale configuration</span></span>
    - <span data-ttu-id="c16ab-364">새 cmdlet 'Get-AzHDInsihgtClusterAutoscaleConfiguration' 추가</span><span class="sxs-lookup"><span data-stu-id="c16ab-364">Add new cmdlet 'Get-AzHDInsihgtClusterAutoscaleConfiguration'</span></span>
    - <span data-ttu-id="c16ab-365">새 cmdlet 'New-AzHDInsihgtClusterAutoscaleConfiguration' 추가</span><span class="sxs-lookup"><span data-stu-id="c16ab-365">Add new cmdlet 'New-AzHDInsihgtClusterAutoscaleConfiguration'</span></span>
    - <span data-ttu-id="c16ab-366">새 cmdlet 'Set-AzHDInsihgtClusterAutoscaleConfiguration' 추가</span><span class="sxs-lookup"><span data-stu-id="c16ab-366">Add new cmdlet 'Set-AzHDInsihgtClusterAutoscaleConfiguration'</span></span>
    - <span data-ttu-id="c16ab-367">새 cmdlet 'Remove-AzHDInsihgtClusterAutoscaleConfiguration' 추가</span><span class="sxs-lookup"><span data-stu-id="c16ab-367">Add new cmdlet 'Remove-AzHDInsihgtClusterAutoscaleConfiguration'</span></span>
    - <span data-ttu-id="c16ab-368">새 cmdlet 'New-AzHDInsihgtClusterAutoscaleScheduleCondition' 추가</span><span class="sxs-lookup"><span data-stu-id="c16ab-368">Add new cmdlet 'New-AzHDInsihgtClusterAutoscaleScheduleCondition'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="c16ab-369">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="c16ab-369">Az.KeyVault</span></span>
* <span data-ttu-id="c16ab-370">RBAC 권한 부여에 대한 지원 추가됨 [#10557]</span><span class="sxs-lookup"><span data-stu-id="c16ab-370">Added support for RBAC authorization [#10557]</span></span>
* <span data-ttu-id="c16ab-371">'Set-AzKeyVaultAccessPolicy'에서 향상된 오류 처리 [#4007]</span><span class="sxs-lookup"><span data-stu-id="c16ab-371">Enhanced error handling in 'Set-AzKeyVaultAccessPolicy' [#4007]</span></span>

#### <a name="azkusto"></a><span data-ttu-id="c16ab-372">Az.Kusto</span><span class="sxs-lookup"><span data-stu-id="c16ab-372">Az.Kusto</span></span>
* <span data-ttu-id="c16ab-373">'Az.Kusto' 모듈의 일반 공급</span><span class="sxs-lookup"><span data-stu-id="c16ab-373">General availability of 'Az.Kusto' module</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="c16ab-374">Az.Network</span><span class="sxs-lookup"><span data-stu-id="c16ab-374">Az.Network</span></span>
* <span data-ttu-id="c16ab-375">[호환성이 손상되는 변경] 리소스 가상 라우터 및 가상 허브에 맞게 아래 cmdlet이 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="c16ab-375">[Breaking Change] Updated below cmdlets to align resource virtual router and virtual hub</span></span>
    - <span data-ttu-id="c16ab-376">'New-AzVirtualRouter':</span><span class="sxs-lookup"><span data-stu-id="c16ab-376">'New-AzVirtualRouter':</span></span> 
        - <span data-ttu-id="c16ab-377">IP 구성 자식 리소스를 지원하는 -HostedSubnet 매개 변수가 추가됨</span><span class="sxs-lookup"><span data-stu-id="c16ab-377">Added -HostedSubnet parameter to support IP configuration child resource</span></span>
        - <span data-ttu-id="c16ab-378">-HostedGateway 및 -HostedGatewayId 삭제됨</span><span class="sxs-lookup"><span data-stu-id="c16ab-378">deleted -HostedGateway and -HostedGatewayId</span></span>
    - <span data-ttu-id="c16ab-379">'Get-AzVirtualRouter':</span><span class="sxs-lookup"><span data-stu-id="c16ab-379">'Get-AzVirtualRouter':</span></span>
        - <span data-ttu-id="c16ab-380">구독 수준 매개 변수 집합이 추가됨</span><span class="sxs-lookup"><span data-stu-id="c16ab-380">Added subscription level parameter set</span></span>
    - <span data-ttu-id="c16ab-381">'Remove-AzVirtualRouter'</span><span class="sxs-lookup"><span data-stu-id="c16ab-381">'Remove-AzVirtualRouter'</span></span>
    - <span data-ttu-id="c16ab-382">'Add-AzVirtualRouterPeer'</span><span class="sxs-lookup"><span data-stu-id="c16ab-382">'Add-AzVirtualRouterPeer'</span></span>
    - <span data-ttu-id="c16ab-383">'Get-AzVirtualRouterPeer'</span><span class="sxs-lookup"><span data-stu-id="c16ab-383">'Get-AzVirtualRouterPeer'</span></span>
    - <span data-ttu-id="c16ab-384">'Remove-AzVirtualRouterPeer'</span><span class="sxs-lookup"><span data-stu-id="c16ab-384">'Remove-AzVirtualRouterPeer'</span></span>
* <span data-ttu-id="c16ab-385">Azure Express 경로 포트에 대해 새 cmdlet이 추가됨</span><span class="sxs-lookup"><span data-stu-id="c16ab-385">Added new cmdlet for Azure Express Route Port</span></span>
    - <span data-ttu-id="c16ab-386">'New-AzExpressRoutePortLOA'</span><span class="sxs-lookup"><span data-stu-id="c16ab-386">'New-AzExpressRoutePortLOA'</span></span>
* <span data-ttu-id="c16ab-387">VirtualNetwork 피어링 리소스에 RemoteBgpCommunities 속성이 추가됨</span><span class="sxs-lookup"><span data-stu-id="c16ab-387">Added RemoteBgpCommunities property to the VirtualNetwork Peering Resource</span></span>
* <span data-ttu-id="c16ab-388">'New-AzLoadBalancerFrontendIpConfig', 'New-AzPublicIpAddress' 및 'New-AzPublicIpPrefix'에 대한 경고 메시지를 수정했습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-388">Modified the warning message for 'New-AzLoadBalancerFrontendIpConfig', 'New-AzPublicIpAddress' and 'New-AzPublicIpPrefix'.</span></span>
* <span data-ttu-id="c16ab-389">'Get-AzVpnGateway' 출력에 VpnGatewayIpConfigurations가 추가됨</span><span class="sxs-lookup"><span data-stu-id="c16ab-389">Added VpnGatewayIpConfigurations to 'Get-AzVpnGateway' output</span></span>
* <span data-ttu-id="c16ab-390">'Set-AzApplicationGatewaySslCertificate'의 버그 수정됨 [#9488]</span><span class="sxs-lookup"><span data-stu-id="c16ab-390">Fixed bug for 'Set-AzApplicationGatewaySslCertificate' [#9488]</span></span>
* <span data-ttu-id="c16ab-391">'AzureFirewall'에 'AllowActiveFTP' 매개 변수가 추가됨</span><span class="sxs-lookup"><span data-stu-id="c16ab-391">Added 'AllowActiveFTP' parameter to 'AzureFirewall'</span></span>
* <span data-ttu-id="c16ab-392">기능에 대한 새로운 명령이 업데이트됨: VirtualWan P2SVpnGateway에서 인터넷 보안 설정 사용/제거</span><span class="sxs-lookup"><span data-stu-id="c16ab-392">Updated below commands for feature: Enable internet security set/remove on VirtualWan P2SVpnGateway.</span></span>
- <span data-ttu-id="c16ab-393">'New-AzP2sVpnGateway' 업데이트됨: 고객이 P2SVpnGateway에서 인터넷 보안을 사용하도록 true를 설정할 수 있는 선택적 스위치 매개 변수 'EnableInternetSecurityFlag'가 추가되었으며, 이는 지점 및 사이트 간 클라이언트에 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-393">Updated 'New-AzP2sVpnGateway': Added optional switch parameter 'EnableInternetSecurityFlag' for customers to set true to enable internet security on P2SVpnGateway, which will be applied for Point to site clients.</span></span>
- <span data-ttu-id="c16ab-394">'Update-AzP2sVpnGateway' 업데이트됨: 고객이 P2SVpnGateway에서 인터넷 보안을 활성화/비활성화하도록 true/false를 설정할 수 있는 선택적 스위치 매개 변수 'EnableInternetSecurityFlag' 또는 'DisableInternetSecurityFlag'가 추가되었으며, 이는 지점 및 사이트 간 클라이언트에 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-394">Updated 'Update-AzP2sVpnGateway': Added optional switch parameters 'EnableInternetSecurityFlag' or 'DisableInternetSecurityFlag' for customers to set true/false to enable/disable internet security on P2SVpnGateway, which will be applied for Point to site clients.</span></span>
* <span data-ttu-id="c16ab-395">문제 해결을 위해 VirtualWan P2SVPNGateway를 재설정/재부팅할 수 있도록 새 cmdlet 'Reset-AzP2sVpnGateway'를 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-395">Added new cmdlet 'Reset-AzP2sVpnGateway' for customers to reset/reboot their VirtualWan P2SVpnGateway for troubleshooting.</span></span>
* <span data-ttu-id="c16ab-396">문제 해결을 위해 VirtualWan VpnGateway를 재설정/재부팅할 수 있도록 새 cmdlet 'Reset-AzVpnGateway'를 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-396">Added new cmdlet 'Reset-AzVpnGateway' for customers to reset/reboot their VirtualWan VpnGateway for troubleshooting.</span></span>
* <span data-ttu-id="c16ab-397">'Set-AzVirtualNetworkSubnetConfig' 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="c16ab-397">Updated 'Set-AzVirtualNetworkSubnetConfig'</span></span>
    - <span data-ttu-id="c16ab-398">매개 변수에 명시적으로 설정된 경우 서브넷의 NSG 및 라우팅 테이블 속성을 null로 설정 [# 1548][# 9718]</span><span class="sxs-lookup"><span data-stu-id="c16ab-398">Set NSG and Route Table properties of subnet to null if explicitly set in parameters [#1548][#9718]</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="c16ab-399">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="c16ab-399">Az.RecoveryServices</span></span>
* <span data-ttu-id="c16ab-400">워크로드 백업 항목에 대한 삭제 상태가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-400">Fixed the Delete State for workload Backup Items.</span></span>

#### <a name="azresources"></a><span data-ttu-id="c16ab-401">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="c16ab-401">Az.Resources</span></span>
* <span data-ttu-id="c16ab-402">Set-AzRoleAssignment에 대한 누락된 검사 추가됨</span><span class="sxs-lookup"><span data-stu-id="c16ab-402">Added missing check for Set-AzRoleAssignment</span></span>
* <span data-ttu-id="c16ab-403">'Get-AzResourceGroupDeploymentOperation'의 'SubscriptionId' 매개 변수에 호환성이 손상되는 변경 특성이 추가됨</span><span class="sxs-lookup"><span data-stu-id="c16ab-403">Added breaking change attribute to 'SubscriptionId' parameter of 'Get-AzResourceGroupDeploymentOperation'</span></span>
* <span data-ttu-id="c16ab-404">마지막으로 'Ignore' 리소스 변경을 표시하도록 ARM 템플릿 What-If cmdlet이 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="c16ab-404">Updated ARM template What-If cmdlets to show 'Ignore' resource changes last</span></span>
* <span data-ttu-id="c16ab-405">배포 cmdlet에 대한 보안 및 배열 매개 변수 직렬화 문제가 해결됨 [#12773]</span><span class="sxs-lookup"><span data-stu-id="c16ab-405">Fixed secure and array parameter serialization issues for deployment cmdlets [#12773]</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="c16ab-406">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="c16ab-406">Az.ServiceFabric</span></span>
* <span data-ttu-id="c16ab-407">관리형 클러스터 및 노드 유형에 대해 다음과 같은 새 cmdlet가 추가됨</span><span class="sxs-lookup"><span data-stu-id="c16ab-407">Added new cmdlets for managed clusters and node types:</span></span>
    - <span data-ttu-id="c16ab-408">'New-AzServiceFabricManagedCluster'</span><span class="sxs-lookup"><span data-stu-id="c16ab-408">'New-AzServiceFabricManagedCluster'</span></span>
    - <span data-ttu-id="c16ab-409">'Get-AzServiceFabricManagedCluster'</span><span class="sxs-lookup"><span data-stu-id="c16ab-409">'Get-AzServiceFabricManagedCluster'</span></span>
    - <span data-ttu-id="c16ab-410">'Set-AzServiceFabricManagedCluster'</span><span class="sxs-lookup"><span data-stu-id="c16ab-410">'Set-AzServiceFabricManagedCluster'</span></span>
    - <span data-ttu-id="c16ab-411">'Remove-AzServiceFabricManagedCluster'</span><span class="sxs-lookup"><span data-stu-id="c16ab-411">'Remove-AzServiceFabricManagedCluster'</span></span>
    - <span data-ttu-id="c16ab-412">'Add-AzServiceFabricManagedClusterClientCertificate'</span><span class="sxs-lookup"><span data-stu-id="c16ab-412">'Add-AzServiceFabricManagedClusterClientCertificate'</span></span>
    - <span data-ttu-id="c16ab-413">'Remove-AzServiceFabricManagedClusterClientCertificate'</span><span class="sxs-lookup"><span data-stu-id="c16ab-413">'Remove-AzServiceFabricManagedClusterClientCertificate'</span></span>
    - <span data-ttu-id="c16ab-414">'New-AzServiceFabricManagedNodeType'</span><span class="sxs-lookup"><span data-stu-id="c16ab-414">'New-AzServiceFabricManagedNodeType'</span></span>
    - <span data-ttu-id="c16ab-415">'Get-AzServiceFabricManagedNodeType'</span><span class="sxs-lookup"><span data-stu-id="c16ab-415">'Get-AzServiceFabricManagedNodeType'</span></span>
    - <span data-ttu-id="c16ab-416">'Set-AzServiceFabricManagedNodeType'</span><span class="sxs-lookup"><span data-stu-id="c16ab-416">'Set-AzServiceFabricManagedNodeType'</span></span>
    - <span data-ttu-id="c16ab-417">'Remove-AzServiceFabricManagedNodeType'</span><span class="sxs-lookup"><span data-stu-id="c16ab-417">'Remove-AzServiceFabricManagedNodeType'</span></span>
    - <span data-ttu-id="c16ab-418">'Add-AzServiceFabricManagedNodeTypeVMExtension'</span><span class="sxs-lookup"><span data-stu-id="c16ab-418">'Add-AzServiceFabricManagedNodeTypeVMExtension'</span></span>
    - <span data-ttu-id="c16ab-419">'Add-AzServiceFabricManagedNodeTypeVMSecret'</span><span class="sxs-lookup"><span data-stu-id="c16ab-419">'Add-AzServiceFabricManagedNodeTypeVMSecret'</span></span>
    - <span data-ttu-id="c16ab-420">'Remove-AzServiceFabricManagedNodeTypeVMExtension'</span><span class="sxs-lookup"><span data-stu-id="c16ab-420">'Remove-AzServiceFabricManagedNodeTypeVMExtension'</span></span>
    - <span data-ttu-id="c16ab-421">'Restart-AzServiceFabricManagedNodeTyp'</span><span class="sxs-lookup"><span data-stu-id="c16ab-421">'Restart-AzServiceFabricManagedNodeTyp'</span></span>
* <span data-ttu-id="c16ab-422">Service Fabric SDK를 버전 1.2.0으로 업그레이드했으며, 현재 모델에서는 서비스 패브릭 리소스 제공자 api-version 2020-03-01을, 관리형 클러스터에서는 2020-01-01-preview를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-422">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2020-03-01 for the current model and 2020-01-01-preview for managed clusters.</span></span>

#### <a name="azsql"></a><span data-ttu-id="c16ab-423">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="c16ab-423">Az.Sql</span></span>
* <span data-ttu-id="c16ab-424">BackupStorageRedundancy가 'New-AzSqlInstance' 및 'Get-AzSqlInstance'에 추가됨</span><span class="sxs-lookup"><span data-stu-id="c16ab-424">Added BackupStorageRedundancy to 'New-AzSqlInstance' and 'Get-AzSqlInstance'</span></span>
* <span data-ttu-id="c16ab-425">'Get-AzSqlServerActiveDirectoryOnlyAuthentication' cmdlet이 추가됨</span><span class="sxs-lookup"><span data-stu-id="c16ab-425">Added cmdlet 'Get-AzSqlServerActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="c16ab-426">'Enable-AzSqlServerActiveDirectoryOnlyAuthentication' cmdlet이 추가됨</span><span class="sxs-lookup"><span data-stu-id="c16ab-426">Added cmdlet 'Enable-AzSqlServerActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="c16ab-427">Force 매개 변수가 'New-AzSqlInstance'에 추가됨</span><span class="sxs-lookup"><span data-stu-id="c16ab-427">Added Force parameter to 'New-AzSqlInstance'</span></span>
* <span data-ttu-id="c16ab-428">관리되는 데이터베이스 로그 재생 서비스용 cmdlet이 추가됨</span><span class="sxs-lookup"><span data-stu-id="c16ab-428">Added cmdlets for Managed Database Log Replay service</span></span>
    - <span data-ttu-id="c16ab-429">'Start-AzSqlInstanceDatabaseLogReplay'</span><span class="sxs-lookup"><span data-stu-id="c16ab-429">'Start-AzSqlInstanceDatabaseLogReplay'</span></span>
    - <span data-ttu-id="c16ab-430">'Get-AzSqlInstanceDatabaseLogReplay'</span><span class="sxs-lookup"><span data-stu-id="c16ab-430">'Get-AzSqlInstanceDatabaseLogReplay'</span></span>
    - <span data-ttu-id="c16ab-431">'Complete-AzSqlInstanceDatabaseLogReplay'</span><span class="sxs-lookup"><span data-stu-id="c16ab-431">'Complete-AzSqlInstanceDatabaseLogReplay'</span></span>
    - <span data-ttu-id="c16ab-432">'Stop-AzSqlInstanceDatabaseLogReplay'</span><span class="sxs-lookup"><span data-stu-id="c16ab-432">'Stop-AzSqlInstanceDatabaseLogReplay'</span></span>
* <span data-ttu-id="c16ab-433">'Get-AzSqlInstanceActiveDirectoryOnlyAuthentication' cmdlet이 추가됨</span><span class="sxs-lookup"><span data-stu-id="c16ab-433">Added cmdlet 'Get-AzSqlInstanceActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="c16ab-434">'Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication' cmdlet이 추가됨</span><span class="sxs-lookup"><span data-stu-id="c16ab-434">Added cmdlet 'Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="c16ab-435">'Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication' cmdlet이 추가됨</span><span class="sxs-lookup"><span data-stu-id="c16ab-435">Added cmdlet 'Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="c16ab-436">네트워크 격리 기능을 지원하기 위해 'New-AzSqlDatabaseImport' 및 'New-AzSqlDatabaseExport' cmdlet이 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="c16ab-436">Updated cmdlets 'New-AzSqlDatabaseImport' and 'New-AzSqlDatabaseExport' to support network isolation functionality</span></span>
* <span data-ttu-id="c16ab-437">'New-AzSqlDatabaseImportExisting' cmdlet이 추가됨</span><span class="sxs-lookup"><span data-stu-id="c16ab-437">Added cmdlet 'New-AzSqlDatabaseImportExisting'</span></span>
* <span data-ttu-id="c16ab-438">백업 스토리지 유형 사양을 지원하도록 데이터베이스 cmdlet이 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="c16ab-438">Updated Databases cmdlets to support backup storage type specification</span></span>
* <span data-ttu-id="c16ab-439">Force 매개 변수가 'New-AzSqlDatabase'에 추가됨</span><span class="sxs-lookup"><span data-stu-id="c16ab-439">Added Force parameter to 'New-AzSqlDatabase'</span></span>
* <span data-ttu-id="c16ab-440">'New-AzSqlDatabase'의 영역 선택에서 BackupStorageRedundancy 구성에 대한 경고가 추가됨</span><span class="sxs-lookup"><span data-stu-id="c16ab-440">Added warning for BackupStorageRedundancy configuration in select regions in 'New-AzSqlDatabase'</span></span>
* <span data-ttu-id="c16ab-441">ResourceId 및 InputObject를 포함하도록 서버 및 인스턴스에 대한 ActiveDirectoryOnlyAuthentication cmdlet이 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="c16ab-441">Updated ActiveDirectoryOnlyAuthentication cmdlets for server and instance to include ResourceId and InputObject</span></span>

#### <a name="azstorage"></a><span data-ttu-id="c16ab-442">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="c16ab-442">Az.Storage</span></span>
* <span data-ttu-id="c16ab-443">Microsoft.Azure.Storage.DataMovement 2.0.0로 업그레이드하여 blob 업로드 실패 수정됨 [#12220]</span><span class="sxs-lookup"><span data-stu-id="c16ab-443">Fixed upload blob fail by upgrade to Microsoft.Azure.Storage.DataMovement 2.0.0 [#12220]</span></span>
* <span data-ttu-id="c16ab-444">지정 시간 복원 지원</span><span class="sxs-lookup"><span data-stu-id="c16ab-444">Supported Point In Time Restore</span></span>
    - <span data-ttu-id="c16ab-445">'Enable-AzStorageBlobRestorePolicy'</span><span class="sxs-lookup"><span data-stu-id="c16ab-445">'Enable-AzStorageBlobRestorePolicy'</span></span>
    - <span data-ttu-id="c16ab-446">'Disable-AzStorageBlobRestorePolicy'</span><span class="sxs-lookup"><span data-stu-id="c16ab-446">'Disable-AzStorageBlobRestorePolicy'</span></span>
    - <span data-ttu-id="c16ab-447">'New-AzStorageBlobRangeToRestore'</span><span class="sxs-lookup"><span data-stu-id="c16ab-447">'New-AzStorageBlobRangeToRestore'</span></span>
    - <span data-ttu-id="c16ab-448">'Restore-AzStorageBlobRange'</span><span class="sxs-lookup"><span data-stu-id="c16ab-448">'Restore-AzStorageBlobRange'</span></span>
* <span data-ttu-id="c16ab-449">-IncludeBlobRestoreStatus 매개 변수와 함께 get-AzureRMStorageAccount를 실행하여 스토리지 계정의 blob 복원 상태 가져오기 지원</span><span class="sxs-lookup"><span data-stu-id="c16ab-449">Supported get blob restore status of Storage account by run get-AzureRMStorageAccount with parameter -IncludeBlobRestoreStatus</span></span> 
    - <span data-ttu-id="c16ab-450">'Get-AzureRMStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="c16ab-450">'Get-AzureRMStorageAccount'</span></span>
* <span data-ttu-id="c16ab-451">예정된 cmdlet 출력 변경에 대해 호환성이 손상되는 변경 경고 메시지가 추가됨</span><span class="sxs-lookup"><span data-stu-id="c16ab-451">Added breaking change warning message for upcoming cmdlet output change</span></span>
    - <span data-ttu-id="c16ab-452">'Get-AzStorageContainerStoredAccessPolicy'</span><span class="sxs-lookup"><span data-stu-id="c16ab-452">'Get-AzStorageContainerStoredAccessPolicy'</span></span>
    - <span data-ttu-id="c16ab-453">'Set-AzStorageContainerStoredAccessPolicy'</span><span class="sxs-lookup"><span data-stu-id="c16ab-453">'Set-AzStorageContainerStoredAccessPolicy'</span></span>
    - <span data-ttu-id="c16ab-454">'Set-AzStorageAccountManagementPolicy'</span><span class="sxs-lookup"><span data-stu-id="c16ab-454">'Set-AzStorageAccountManagementPolicy'</span></span>
    - <span data-ttu-id="c16ab-455">'Get-AzStorageAccountManagementPolicy'</span><span class="sxs-lookup"><span data-stu-id="c16ab-455">'Get-AzStorageAccountManagementPolicy'</span></span>
    - <span data-ttu-id="c16ab-456">'Add-AzStorageAccountManagementPolicyAction'</span><span class="sxs-lookup"><span data-stu-id="c16ab-456">'Add-AzStorageAccountManagementPolicyAction'</span></span>
    - <span data-ttu-id="c16ab-457">'New-AzStorageAccountManagementPolicyRule'</span><span class="sxs-lookup"><span data-stu-id="c16ab-457">'New-AzStorageAccountManagementPolicyRule'</span></span>
* <span data-ttu-id="c16ab-458">Microsoft.Azure.Cosmos.Table SDK를 1.0.8로 업그레이드</span><span class="sxs-lookup"><span data-stu-id="c16ab-458">Upgraded Microsoft.Azure.Cosmos.Table SDK to 1.0.8</span></span>

### <a name="thanks-to-our-community-contributors"></a><span data-ttu-id="c16ab-459">커뮤니티 기여자에게 감사드립니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-459">Thanks to our community contributors</span></span>
* <span data-ttu-id="c16ab-460">Thomas Van Laere(@ThomVanL), Dockerfile-alpine-3.10 추가(#12911)</span><span class="sxs-lookup"><span data-stu-id="c16ab-460">Thomas Van Laere (@ThomVanL), Add Dockerfile-alpine-3.10 (#12911)</span></span> 
* <span data-ttu-id="c16ab-461">Lohith Chowdary Chilukuri(@Lochiluk), Remove-AzNetworkInterfaceIpConfig.md 업데이트(#12807)</span><span class="sxs-lookup"><span data-stu-id="c16ab-461">Lohith Chowdary Chilukuri (@Lochiluk), Update Remove-AzNetworkInterfaceIpConfig.md (#12807)</span></span> 
* <span data-ttu-id="c16ab-462">Roberth Strand(@roberthstrand), Get-AzResourceGroup - 새로운 예제 및 정리(#12828)</span><span class="sxs-lookup"><span data-stu-id="c16ab-462">Roberth Strand (@roberthstrand), Get-AzResourceGroup - New example, and cleanup (#12828)</span></span> 
* <span data-ttu-id="c16ab-463">Ravi Mishra(@inmishrar), Azure 웹앱 런타임 스택을 DOTNETCORE로 업데이트(#12833)</span><span class="sxs-lookup"><span data-stu-id="c16ab-463">Ravi Mishra (@inmishrar), update Azure Web App runtime stack to DOTNETCORE (#12833)</span></span> 
* <span data-ttu-id="c16ab-464">@jack-education, NSG 및 라우팅 테이블을 서브넷에서 제거할 수 있도록 Set-AzVirtualNetworkSubnetConfig를 업데이트(# 12351)</span><span class="sxs-lookup"><span data-stu-id="c16ab-464">@jack-education, Updated Set-AzVirtualNetworkSubnetConfig to allow NSG and Route Table to be removed from subnet (#12351)</span></span> 
* <span data-ttu-id="c16ab-465">@hagop-globanet, Add-AzApplicationGatewayCustomError.md 업데이트(#12784)</span><span class="sxs-lookup"><span data-stu-id="c16ab-465">@hagop-globanet, Update Add-AzApplicationGatewayCustomError.md (#12784)</span></span> 
* <span data-ttu-id="c16ab-466">Joshua Van Daalen(@greenSacrifice)</span><span class="sxs-lookup"><span data-stu-id="c16ab-466">Joshua Van Daalen (@greenSacrifice)</span></span>
  * <span data-ttu-id="c16ab-467">속성(Property) 철자를 속성(Property)으로 업데이트(#12821)</span><span class="sxs-lookup"><span data-stu-id="c16ab-467">Update spelling of Property to Property (#12821)</span></span> 
  * <span data-ttu-id="c16ab-468">New-AzResourceLock.md 예제 업데이트(#12806)</span><span class="sxs-lookup"><span data-stu-id="c16ab-468">Update New-AzResourceLock.md examples (#12806)</span></span>
* <span data-ttu-id="c16ab-469">Eragon Riddle(@eragonriddle), 예제에서 매개 변수 필드 이름 수정(#12825)</span><span class="sxs-lookup"><span data-stu-id="c16ab-469">Eragon Riddle (@eragonriddle), Corrected parameter field name in the example (#12825)</span></span> 
* <span data-ttu-id="c16ab-470">@rossifumax, New-AzConfigurationAssignment.md의 오타 수정(#12701)</span><span class="sxs-lookup"><span data-stu-id="c16ab-470">@rossifumax, Fix typo in New-AzConfigurationAssignment.md (#12701)</span></span>

## <a name="461---august-2020"></a><span data-ttu-id="c16ab-471">4.6.1 - 2020년 8월</span><span class="sxs-lookup"><span data-stu-id="c16ab-471">4.6.1 - August 2020</span></span>
#### <a name="azcompute"></a><span data-ttu-id="c16ab-472">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="c16ab-472">Az.Compute</span></span>
* <span data-ttu-id="c16ab-473">'New-AzVm'에서 '-EncryptionAtHost' 매개 변수를 패치하여 기본값인 false가 제거됨[#12776]</span><span class="sxs-lookup"><span data-stu-id="c16ab-473">Patched '-EncryptionAtHost' parameter in 'New-AzVm' to remove default value of false [#12776]</span></span>

## <a name="460---august-2020"></a><span data-ttu-id="c16ab-474">4.6.0 - 2020년 8월</span><span class="sxs-lookup"><span data-stu-id="c16ab-474">4.6.0 - August 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="c16ab-475">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="c16ab-475">Az.Accounts</span></span>
* <span data-ttu-id="c16ab-476">검색 엔드포인트가 기본 AzureCloud나 기타 공용 환경을 반환하지 않는 경우 모든 퍼블릭 클라우드 환경이 로드됨 [#12633]</span><span class="sxs-lookup"><span data-stu-id="c16ab-476">Loaded all public cloud environments when discovery endpoint doesn't return default AzureCloud or other public environments [#12633]</span></span>
* <span data-ttu-id="c16ab-477">'Get-AzSubscription'에서 SubscriptionPolicies가 노출됨 [#12551]</span><span class="sxs-lookup"><span data-stu-id="c16ab-477">Exposed SubscriptionPolicies in 'Get-AzSubscription' [#12551]</span></span>

#### <a name="azautomation"></a><span data-ttu-id="c16ab-478">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="c16ab-478">Az.Automation</span></span>
* <span data-ttu-id="c16ab-479">Hybrid Worker 그룹을 지정하기 위해 'Set-AzAutomationWebhook'에 '-RunOn' 매개 변수가 추가됨</span><span class="sxs-lookup"><span data-stu-id="c16ab-479">Added '-RunOn' parameters to 'Set-AzAutomationWebhook' to specify a Hybrid Worker Group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="c16ab-480">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="c16ab-480">Az.Compute</span></span>
* <span data-ttu-id="c16ab-481">'New-AzVm', 'New-AzVmss', 'New-AzVMConfig', 'New-AzVmssConfig', 'Update-AzVM', 'Update-AzVmss'에 '-EncryptionAtHost' 매개 변수가 추가됨</span><span class="sxs-lookup"><span data-stu-id="c16ab-481">Added '-EncryptionAtHost' parameter to 'New-AzVm', 'New-AzVmss', 'New-AzVMConfig', 'New-AzVmssConfig', 'Update-AzVM', and 'Update-AzVmss'</span></span>
* <span data-ttu-id="c16ab-482">'Get-AzVM' 및 'Get-AzVmss' 반환 개체에 'SecurityProfile'이 추가됨</span><span class="sxs-lookup"><span data-stu-id="c16ab-482">Added 'SecurityProfile' to 'Get-AzVM' and 'Get-AzVmss' return object</span></span>
* <span data-ttu-id="c16ab-483">'-InstanceView' 스위치가 'Get-AzHostGroup'에 선택적 매개 변수로 추가됨</span><span class="sxs-lookup"><span data-stu-id="c16ab-483">Added '-InstanceView' switch as optional parameter to 'Get-AzHostGroup'</span></span>
* <span data-ttu-id="c16ab-484">새 cmdlet 'Invoke-AzVmPatchAssessment'가 추가됨</span><span class="sxs-lookup"><span data-stu-id="c16ab-484">Added new cmdlet 'Invoke-AzVmPatchAssessment'</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="c16ab-485">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="c16ab-485">Az.DataFactory</span></span>
* <span data-ttu-id="c16ab-486">PSPipelineRun 클래스에 누락된 속성이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-486">Added missing properties to PSPipelineRun class.</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="c16ab-487">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="c16ab-487">Az.HDInsight</span></span>
* <span data-ttu-id="c16ab-488">호스트 기능에서 암호화를 사용하여 클러스터를 만드는 것이 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-488">Supported creating cluster with encryption at host feature.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="c16ab-489">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="c16ab-489">Az.KeyVault</span></span>
* <span data-ttu-id="c16ab-490">일시 삭제 사용 안 함 계획에 대한 경고 메시지가 추가됨</span><span class="sxs-lookup"><span data-stu-id="c16ab-490">Added warning messages for planning to disable soft delete</span></span>
* <span data-ttu-id="c16ab-491">특성 SecretValueText 제거 계획에 대한 경고 메시지가 추가됨</span><span class="sxs-lookup"><span data-stu-id="c16ab-491">Added warning messages for planning to remove attribute SecretValueText</span></span>

#### <a name="azmaintenance"></a><span data-ttu-id="c16ab-492">Az.Maintenance</span><span class="sxs-lookup"><span data-stu-id="c16ab-492">Az.Maintenance</span></span>
* <span data-ttu-id="c16ab-493">'New-AzMaintenanceConfiguration'에 선택적 일정 관련 필드가 추가됨</span><span class="sxs-lookup"><span data-stu-id="c16ab-493">Added optional schedule related fields to 'New-AzMaintenanceConfiguration'</span></span>
* <span data-ttu-id="c16ab-494">'Get-AzMaintenancePublicConfiguration'에 대한 새 cmdlet이 추가됨</span><span class="sxs-lookup"><span data-stu-id="c16ab-494">Added new cmdlet for 'Get-AzMaintenancePublicConfiguration'</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="c16ab-495">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="c16ab-495">Az.ManagedServices</span></span>
* <span data-ttu-id="c16ab-496">관리되는 서비스 할당 및 정의의 cmdlet에 대한 호환성이 손상되는 변경 경고가 추가됨</span><span class="sxs-lookup"><span data-stu-id="c16ab-496">Added breaking change warnings on cmdlets of managed services assignment and definition</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="c16ab-497">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="c16ab-497">Az.Monitor</span></span>
* <span data-ttu-id="c16ab-498">로그 및 메트릭 사용을 분리하기 위해 'Set-AzDiagnosticSetting'에 설정된 매개 변수가 확장됨 [#12482]</span><span class="sxs-lookup"><span data-stu-id="c16ab-498">Extended the parameter set in 'Set-AzDiagnosticSetting' for separation of Logs and Metrics enablement [#12482]</span></span>
* <span data-ttu-id="c16ab-499">파이프라인에서 메트릭 경고를 가져오는 경우 'Add-AzMetricAlertRuleV2'에 대한 버그가 수정됨</span><span class="sxs-lookup"><span data-stu-id="c16ab-499">Fixed bug for 'Add-AzMetricAlertRuleV2' when getting metric alert from pipeline</span></span>

#### <a name="azresources"></a><span data-ttu-id="c16ab-500">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="c16ab-500">Az.Resources</span></span>
* <span data-ttu-id="c16ab-501">Azure Policy를 통해 별칭을 수정할 수 있는지 여부를 나타내는 정보를 포함하도록 'Get-AzPolicyAlias' 응답이 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="c16ab-501">Updated 'Get-AzPolicyAlias' response to include information indicating whether the alias is modifiable by Azure Policy.</span></span>
* <span data-ttu-id="c16ab-502">새 cmdlet 'Set-AzRoleAssignment'가 생성됨</span><span class="sxs-lookup"><span data-stu-id="c16ab-502">Created new cmdlet 'Set-AzRoleAssignment'</span></span>
* <span data-ttu-id="c16ab-503">관리 그룹 범위에서 ARM 템플릿 What-If 결과를 가져오는 'Get-AzDeploymentManagementGroupWhatIfResult'가 추가됨</span><span class="sxs-lookup"><span data-stu-id="c16ab-503">Added 'Get-AzDeploymentManagementGroupWhatIfResult' for getting ARM template What-If results at management Group scope</span></span>
* <span data-ttu-id="c16ab-504">테넌트 범위에서 ARM 템플릿 What-If 결과를 가져오는 'Get-AzTenantWhatIfResult' 새 cmdlet이 추가됨</span><span class="sxs-lookup"><span data-stu-id="c16ab-504">Added 'Get-AzTenantWhatIfResult' new cmdlet for getting ARM template What-If results at tenant scope</span></span>
* <span data-ttu-id="c16ab-505">ARM 템플릿 What-If 결과를 사용하도록 'New-AzManagementGroupDeployment' 및 'New-AzTenantDeployment'에 대한 '-WhatIf' 및 '-Confirm'이 재정의됨</span><span class="sxs-lookup"><span data-stu-id="c16ab-505">Overrode '-WhatIf' and '-Confirm' for 'New-AzManagementGroupDeployment' and 'New-AzTenantDeployment' to use ARM template What-If results</span></span>
* <span data-ttu-id="c16ab-506">새 배포 cmdlet에 대한 '-WhatIf' 및 '-Confirm' 동작이 False를 준수하도록 수정됨</span><span class="sxs-lookup"><span data-stu-id="c16ab-506">Fixed the behaviors of '-WhatIf' and '-Confirm' for new deployment cmdlets so they comply with False and</span></span> 
* <span data-ttu-id="c16ab-507">'-TemplateObject' 및 'TemplateParameterObject'에 대한 직렬화 오류가 수정됨 [#1528] [#6292]</span><span class="sxs-lookup"><span data-stu-id="c16ab-507">Fixed serialization error for '-TemplateObject' and 'TemplateParameterObject' [#1528] [#6292]</span></span>
* <span data-ttu-id="c16ab-508">예정된 출력 형식 변경을 위해 'Get-AzResourceGroupDeploymentOperation'에 호환성이 손상되는 변경 특성이 추가됨</span><span class="sxs-lookup"><span data-stu-id="c16ab-508">Added breaking change attribute to 'Get-AzResourceGroupDeploymentOperation' for the upcoming output type change</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="c16ab-509">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="c16ab-509">Az.SignalR</span></span>
* <span data-ttu-id="c16ab-510">'Restart-AzSignalR' 및 'Update-AzSignalR' 도움말 파일 오류가 수정됨</span><span class="sxs-lookup"><span data-stu-id="c16ab-510">Fixed 'Restart-AzSignalR' and 'Update-AzSignalR' help files errors</span></span>
* <span data-ttu-id="c16ab-511">'Update-AzSignalRNetworkAcl', 'Set-AzSignalRUpstream' cmdlet이 추가됨</span><span class="sxs-lookup"><span data-stu-id="c16ab-511">Added cmdlets 'Update-AzSignalRNetworkAcl', 'Set-AzSignalRUpstream'</span></span>

#### <a name="azstorage"></a><span data-ttu-id="c16ab-512">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="c16ab-512">Az.Storage</span></span>
* <span data-ttu-id="c16ab-513">지원되는 Blob 쿼리 가속</span><span class="sxs-lookup"><span data-stu-id="c16ab-513">Supported blob query acceleration</span></span>
    -  <span data-ttu-id="c16ab-514">'Get-AzStorageBlobQueryResult'</span><span class="sxs-lookup"><span data-stu-id="c16ab-514">'Get-AzStorageBlobQueryResult'</span></span>
    -  <span data-ttu-id="c16ab-515">'New-AzStorageBlobQueryConfig'</span><span class="sxs-lookup"><span data-stu-id="c16ab-515">'New-AzStorageBlobQueryConfig'</span></span>
* <span data-ttu-id="c16ab-516">도움말 파일 업데이트, 자세한 설명 추가 및 오타 수정</span><span class="sxs-lookup"><span data-stu-id="c16ab-516">Updated help file, added more description, and fixed typo</span></span>
    -  <span data-ttu-id="c16ab-517">'Start-AzStorageBlobCopy'</span><span class="sxs-lookup"><span data-stu-id="c16ab-517">'Start-AzStorageBlobCopy'</span></span>
    -  <span data-ttu-id="c16ab-518">'Get-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="c16ab-518">'Get-AzDataLakeGen2Item'</span></span>
* <span data-ttu-id="c16ab-519">관련 하위 디렉터리가 없는 경우 Blob 다운로드 실패가 수정됨 [#12592]</span><span class="sxs-lookup"><span data-stu-id="c16ab-519">Fixed download blob fail when related sub directory not exist [#12592]</span></span>
    -  <span data-ttu-id="c16ab-520">'Get-AzStorageBlobContent'</span><span class="sxs-lookup"><span data-stu-id="c16ab-520">'Get-AzStorageBlobContent'</span></span>
* <span data-ttu-id="c16ab-521">스토리지 계정에 대해 개체 복제 정책 설정/가져오기/제거가 지원됨</span><span class="sxs-lookup"><span data-stu-id="c16ab-521">Supported Set/Get/Remove Object Replication Policy on Storage accounts</span></span>
    - <span data-ttu-id="c16ab-522">'New-AzStorageObjectReplicationPolicyRule'</span><span class="sxs-lookup"><span data-stu-id="c16ab-522">'New-AzStorageObjectReplicationPolicyRule'</span></span>
    - <span data-ttu-id="c16ab-523">'Set-AzStorageObjectReplicationPolicy'</span><span class="sxs-lookup"><span data-stu-id="c16ab-523">'Set-AzStorageObjectReplicationPolicy'</span></span>
    - <span data-ttu-id="c16ab-524">'Get-AzStorageObjectReplicationPolicy'</span><span class="sxs-lookup"><span data-stu-id="c16ab-524">'Get-AzStorageObjectReplicationPolicy'</span></span>
    - <span data-ttu-id="c16ab-525">'Remove-AzStorageObjectReplicationPolicy'</span><span class="sxs-lookup"><span data-stu-id="c16ab-525">'Remove-AzStorageObjectReplicationPolicy'</span></span>
* <span data-ttu-id="c16ab-526">스토리지 계정의 Blob Service에서 ChangeFeed 사용/사용 안 함이 지원됨</span><span class="sxs-lookup"><span data-stu-id="c16ab-526">Supported enable/disable ChangeFeed on Blob Service of a Storage account</span></span>
    - <span data-ttu-id="c16ab-527">'Update-AzStorageBlobServiceProperty'</span><span class="sxs-lookup"><span data-stu-id="c16ab-527">'Update-AzStorageBlobServiceProperty'</span></span>

## <a name="450---august-2020"></a><span data-ttu-id="c16ab-528">4.5.0 - 2020년 8월</span><span class="sxs-lookup"><span data-stu-id="c16ab-528">4.5.0 - August 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="c16ab-529">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="c16ab-529">Az.Accounts</span></span>
* <span data-ttu-id="c16ab-530">매개 변수 'MaxContextPopulation'을 허용하도록 'Connect-AzAccount' 업데이트됨 [# 9865]</span><span class="sxs-lookup"><span data-stu-id="c16ab-530">Updated 'Connect-AzAccount' to accept parameter 'MaxContextPopulation' [#9865]</span></span>
* <span data-ttu-id="c16ab-531">SubscriptionClient 버전이 2019-06-01로 업데이트되고 테넌트 도메인을 표시 [#9838]</span><span class="sxs-lookup"><span data-stu-id="c16ab-531">Updated SubscriptionClient version to 2019-06-01 and display tenant domains [#9838]</span></span>
* <span data-ttu-id="c16ab-532">구독의 managedBy 테넌트 정보 및 홈 테넌트 지원</span><span class="sxs-lookup"><span data-stu-id="c16ab-532">Supported home tenant and managedBy tenant information of subscription</span></span>
* <span data-ttu-id="c16ab-533">원격 분석 데이터의 모듈 이름, 버전 정보 수정</span><span class="sxs-lookup"><span data-stu-id="c16ab-533">Corrected module name, version info in telemetry data</span></span>
* <span data-ttu-id="c16ab-534">환경 메타데이터 엔드포인트가 호환되지 않는 값을 반환하는 경우 SqlDatabaseDnsSuffix 및 ServiceManagementUrl이 조정됨</span><span class="sxs-lookup"><span data-stu-id="c16ab-534">Adjusted SqlDatabaseDnsSuffix and ServiceManagementUrl if environment metadata endpoint returns incompatible value</span></span>

#### <a name="azaks"></a><span data-ttu-id="c16ab-535">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="c16ab-535">Az.Aks</span></span>
* <span data-ttu-id="c16ab-536">'ClientIdAndSecret'을 'ServicePrincipalIdAndSecret'으로 제거하고 'ClientIdAndSecret'을 별칭으로 설정함 [#12381]</span><span class="sxs-lookup"><span data-stu-id="c16ab-536">Removed 'ClientIdAndSecret' to 'ServicePrincipalIdAndSecret' and set 'ClientIdAndSecret' as an alias [#12381].</span></span>
* <span data-ttu-id="c16ab-537">'Get-AzAks'/'New-AzAks'/'Remove-AzAks'/'Set-AzAks'를 'Get-AzAksCluster'/'New-AzAksCluster'/'Remove-AzAksCluster'/'Set-AzAksCluster'로 제거하고 원본을 별칭으로 설정함 [#12373].</span><span class="sxs-lookup"><span data-stu-id="c16ab-537">Removed 'Get-AzAks'/'New-AzAks'/'Remove-AzAks'/'Set-AzAks' to 'Get-AzAksCluster'/'New-AzAksCluster'/'Remove-AzAksCluster'/'Set-AzAksCluster' and set the original ones as alias [#12373].</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="c16ab-538">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="c16ab-538">Az.ApiManagement</span></span>
* <span data-ttu-id="c16ab-539">새 'Add-AzApiManagementApiToGateway' cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-539">Added new 'Add-AzApiManagementApiToGateway' cmdlet.</span></span>
* <span data-ttu-id="c16ab-540">새 'Get-AzApiManagementGateway' cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-540">Added new 'Get-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="c16ab-541">새 'Get-AzApiManagementGatewayHostnameConfiguration' cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-541">Added new 'Get-AzApiManagementGatewayHostnameConfiguration' cmdlet.</span></span>
* <span data-ttu-id="c16ab-542">새 'Get-AzApiManagementGatewayKey' cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-542">Added new 'Get-AzApiManagementGatewayKey' cmdlet.</span></span>
* <span data-ttu-id="c16ab-543">새 'New-AzApiManagementGateway' cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-543">Added new 'New-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="c16ab-544">새 'New-AzApiManagementGatewayHostnameConfiguration' cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-544">Added new 'New-AzApiManagementGatewayHostnameConfiguration' cmdlet.</span></span>
* <span data-ttu-id="c16ab-545">새 'New-AzApiManagementResourceLocationObject' cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-545">Added new 'New-AzApiManagementResourceLocationObject' cmdlet.</span></span>
* <span data-ttu-id="c16ab-546">새 'Remove-AzApiManagementApiFromGateway' cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-546">Added new 'Remove-AzApiManagementApiFromGateway' cmdlet.</span></span>
* <span data-ttu-id="c16ab-547">새 'Remove-AzApiManagementGateway' cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-547">Added new 'Remove-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="c16ab-548">새 'Remove-AzApiManagementGatewayHostnameConfiguration' cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-548">Added new 'Remove-AzApiManagementGatewayHostnameConfiguration' cmdlet.</span></span>
* <span data-ttu-id="c16ab-549">새 'Update-AzApiManagementGateway' cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-549">Added new 'Update-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="c16ab-550">'Get-AzApiManagementApi' cmdlet에 선택적 [-GatewayId] 매개 변수가 새로 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-550">Added new optional [-GatewayId] parameter to the 'Get-AzApiManagementApi' cmdlet.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="c16ab-551">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="c16ab-551">Az.CognitiveServices</span></span>
* <span data-ttu-id="c16ab-552">'Deny'가 특히 NetworkRules 기본 작업으로 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-552">Used 'Deny' specifically as NetworkRules default action.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="c16ab-553">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="c16ab-553">Az.FrontDoor</span></span>
* <span data-ttu-id="c16ab-554">Enum.Parse가 null 값을 Enabled 또는 Disabled 열거형 값으로 강제 변환하려는 경우 예외가 throw되는 문제를 수정했습니다. [#12344]</span><span class="sxs-lookup"><span data-stu-id="c16ab-554">Fixed an issue where an exception is being thrown when Enum.Parse tries to coerce a null value to an Enabled or Disabled enum values [#12344]</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="c16ab-555">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="c16ab-555">Az.HDInsight</span></span>
* <span data-ttu-id="c16ab-556">전송 중 암호화 기능을 사용하여 클러스터를 만드는 것이 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-556">Supported creating cluster with encryption in transit feature.</span></span>
    - <span data-ttu-id="c16ab-557">cmdlet 'New-AzHDInsightCluster'에 새 매개 변수 'EncryptionInTransit' 추가</span><span class="sxs-lookup"><span data-stu-id="c16ab-557">Add new parameter 'EncryptionInTransit' to the cmdlet 'New-AzHDInsightCluster'</span></span>
    - <span data-ttu-id="c16ab-558">cmdlet 'New-AzHDInsightClusterConfig'에 새 매개 변수 'EncryptionInTransit' 추가</span><span class="sxs-lookup"><span data-stu-id="c16ab-558">Add new parameter 'EncryptionInTransit' to the cmdlet 'New-AzHDInsightClusterConfig'</span></span>
* <span data-ttu-id="c16ab-559">프라이빗 링크 기능을 사용하여 클러스터를 만드는 것이 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-559">Supported creating cluster with private link feature:</span></span>
    - <span data-ttu-id="c16ab-560">cmdlet 'New-AzHDInsightCluster'에 새 매개 변수 'PublicNetworkAccessType' 및 'OutboundPublicNetworkAccessType' 추가</span><span class="sxs-lookup"><span data-stu-id="c16ab-560">Add new parameter 'PublicNetworkAccessType' and 'OutboundPublicNetworkAccessType' to the cmdlet 'New-AzHDInsightCluster'</span></span>
    - <span data-ttu-id="c16ab-561">cmdlet 'New-AzHDInsightClusterConfig'에 새 매개 변수 'PublicNetworkAccessType' 및 'OutboundPublicNetworkAccessType' 추가</span><span class="sxs-lookup"><span data-stu-id="c16ab-561">Add new parameter 'PublicNetworkAccessType' and 'OutboundPublicNetworkAccessType' to the cmdlet 'New-AzHDInsightClusterConfig'</span></span>
* <span data-ttu-id="c16ab-562">'New-AzHDInsightCluster' 또는 'Get-AzHDInsightCluster'를 호출하는 경우 가상 네트워크 정보가 반환됨</span><span class="sxs-lookup"><span data-stu-id="c16ab-562">Returned virtual network information when calling 'New-AzHDInsightCluster' or 'Get-AzHDInsightCluster'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="c16ab-563">Az.Network</span><span class="sxs-lookup"><span data-stu-id="c16ab-563">Az.Network</span></span>
* <span data-ttu-id="c16ab-564">'Remove-AzExpressRouteCircuitConnectionConfig'에 AddressPrefixType 매개 변수 지원 추가</span><span class="sxs-lookup"><span data-stu-id="c16ab-564">Added support for AddressPrefixType parameter to 'Remove-AzExpressRouteCircuitConnectionConfig'</span></span>
* <span data-ttu-id="c16ab-565">작업을 중단하지 않는 변경이 추가됨: 'Remove-AzExpressRouteCircutPeeringConfig'의 프라이빗 피어링을 위한 PeerAddressType 기능</span><span class="sxs-lookup"><span data-stu-id="c16ab-565">Added non-breaking changes: PeerAddressType functionality for Private Peering in 'Remove-AzExpressRouteCircutPeeringConfig'.</span></span>
* <span data-ttu-id="c16ab-566">AddressPrefixType 및 PeerAddressType 매개 변수의 대/소문자를 무시하도록 코드가 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-566">Code changed to ignore case for AddressPrefixType and PeerAddressType parameter.</span></span>
* <span data-ttu-id="c16ab-567">'New-AzLoadBalancerFrontendIpConfig', 'New-AzPublicIpAddress' 및 'New-AzPublicIpPrefix'에 대한 경고 메시지를 수정했습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-567">Modified the warning message for 'New-AzLoadBalancerFrontendIpConfig', 'New-AzPublicIpAddress' and 'New-AzPublicIpPrefix'.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="c16ab-568">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="c16ab-568">Az.OperationalInsights</span></span>
* <span data-ttu-id="c16ab-569">'Remove-AzOperationalInsightsworkspace'에 대한 '-ForceDelete' 옵션이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-569">Added '-ForceDelete' option for 'Remove-AzOperationalInsightsworkspace'</span></span>
* <span data-ttu-id="c16ab-570">새 cmdlet 'Get-AzOperationalInsightsDeletedWorkspace'가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-570">Added new cmdlet 'Get-AzOperationalInsightsDeletedWorkspace'</span></span>
* <span data-ttu-id="c16ab-571">새 cmdlet 'Restore-AzOperationalInsightsWorkspace'가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-571">Added new cmdlet 'Restore-AzOperationalInsightsWorkspace'</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="c16ab-572">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="c16ab-572">Az.RecoveryServices</span></span>
* <span data-ttu-id="c16ab-573">Azure Backup 컨테이너/항목 검색 환경이 개선되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-573">Improved the Azure Backup container/item discovery experience.</span></span>

#### <a name="azresources"></a><span data-ttu-id="c16ab-574">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="c16ab-574">Az.Resources</span></span>
* <span data-ttu-id="c16ab-575">'New-AzRoleAssignment'에 'Condition', 'ConditionVersion' 및 'Description' 속성을 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-575">Added properties 'Condition', 'ConditionVersion' and 'Description' to 'New-AzRoleAssignment'</span></span>
    - <span data-ttu-id="c16ab-576">여기에는 데이터 모델과 관련된 모든 변경 사항이 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-576">This included all the relevant changes to the data models</span></span>

#### <a name="azsql"></a><span data-ttu-id="c16ab-577">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="c16ab-577">Az.Sql</span></span>
* <span data-ttu-id="c16ab-578">'New-AzSqlServer' 'Set-AzSqlServer'에서 서버 이름 대/소문자를 구분하지 않는 잠재적인 오류를 수정했습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-578">Fixed potential server name case insensitive error in 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>
* <span data-ttu-id="c16ab-579">'New-AzSqlDatabaseSecondary'의 기존 데이터베이스 오류에서 반환되는 잘못된 데이터베이스 이름을 수정했습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-579">Fixed wrong database name returned on existing database error in 'New-AzSqlDatabaseSecondary'</span></span>

#### <a name="azstorage"></a><span data-ttu-id="c16ab-580">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="c16ab-580">Az.Storage</span></span>
* <span data-ttu-id="c16ab-581">새 권한 x,t를 사용하여 컨테이너/blob Sas 토큰 만들기 지원</span><span class="sxs-lookup"><span data-stu-id="c16ab-581">Supported create container/blob Sas token with new permission x,t</span></span>
    -  <span data-ttu-id="c16ab-582">'New-AzStorageBlobSASToken'</span><span class="sxs-lookup"><span data-stu-id="c16ab-582">'New-AzStorageBlobSASToken'</span></span>
    -  <span data-ttu-id="c16ab-583">'New-AzStorageContainerSASToken'</span><span class="sxs-lookup"><span data-stu-id="c16ab-583">'New-AzStorageContainerSASToken'</span></span>
* <span data-ttu-id="c16ab-584">새 권한 x,t,f를 사용하여 계정 Sas 토큰 만들기 지원</span><span class="sxs-lookup"><span data-stu-id="c16ab-584">Supported create account Sas token with new permission x,t,f</span></span>
    -  <span data-ttu-id="c16ab-585">'New-AzStorageAccountSASToken'</span><span class="sxs-lookup"><span data-stu-id="c16ab-585">'New-AzStorageAccountSASToken'</span></span>
* <span data-ttu-id="c16ab-586">단일 파일 사용량 공유 가져오기 지원</span><span class="sxs-lookup"><span data-stu-id="c16ab-586">Supported get single file share usage</span></span>
    - <span data-ttu-id="c16ab-587">'Get-AzRmStorageShare'</span><span class="sxs-lookup"><span data-stu-id="c16ab-587">'Get-AzRmStorageShare'</span></span>

## <a name="440---july-2020"></a><span data-ttu-id="c16ab-588">4.4.0 - 2020년 7월</span><span class="sxs-lookup"><span data-stu-id="c16ab-588">4.4.0 - July 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="c16ab-589">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="c16ab-589">Az.Accounts</span></span>
* <span data-ttu-id="c16ab-590">새 cmdlet 'Invoke-AzRestMethod' 추가</span><span class="sxs-lookup"><span data-stu-id="c16ab-590">Added new cmdlet 'Invoke-AzRestMethod'</span></span>
* <span data-ttu-id="c16ab-591">'Start-Job'을 사용하여 여러 Azure PowerShell cmdlet을 실행하는 등 다중 프로세스 시나리오에서 인증 오류를 발생시킬 수 있는 문제 해결 [#9448]</span><span class="sxs-lookup"><span data-stu-id="c16ab-591">Fixed an issue that may cause authentication errors in multi-process scenarios such as running multiple Azure PowerShell cmdlets using 'Start-Job' [#9448]</span></span>

#### <a name="azaks"></a><span data-ttu-id="c16ab-592">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="c16ab-592">Az.Aks</span></span>
* <span data-ttu-id="c16ab-593">'Get-AzAks'가 모든 클러스터를 가져오지 않는 버그 수정 [#12296]</span><span class="sxs-lookup"><span data-stu-id="c16ab-593">Fixed bug 'Get-AzAks' doesn't get all clusters [#12296]</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="c16ab-594">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="c16ab-594">Az.AnalysisServices</span></span>
* <span data-ttu-id="c16ab-595">인증에 대한 프로젝트 참조 제거</span><span class="sxs-lookup"><span data-stu-id="c16ab-595">Removed project reference to Authentication</span></span>

#### <a name="azautomation"></a><span data-ttu-id="c16ab-596">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="c16ab-596">Az.Automation</span></span>
* <span data-ttu-id="c16ab-597">이스케이프 문자를 포함하는 문자열을 json 개체로 변환할 수 없는 문제 해결</span><span class="sxs-lookup"><span data-stu-id="c16ab-597">Fixed the issue that string with escape chars cannot be converted into json object.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="c16ab-598">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="c16ab-598">Az.Compute</span></span>
* <span data-ttu-id="c16ab-599">'latest' 이미지 버전이 없는 'New-AzVmss'를 사용하는 경우 경고 추가</span><span class="sxs-lookup"><span data-stu-id="c16ab-599">Added warning when using 'New-AzVmss' without 'latest' image version</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="c16ab-600">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="c16ab-600">Az.DataFactory</span></span>
* <span data-ttu-id="c16ab-601">Data Factory에 대한 전역 매개 변수를 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-601">Added global parameters to Data Factory.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="c16ab-602">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="c16ab-602">Az.EventGrid</span></span>
* <span data-ttu-id="c16ab-603">2020-06-01 API 버전을 사용하도록 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-603">Updated to use the 2020-06-01 API version.</span></span>
* <span data-ttu-id="c16ab-604">추가된 새로운 기능:</span><span class="sxs-lookup"><span data-stu-id="c16ab-604">Added new features:</span></span>
    - <span data-ttu-id="c16ab-605">입력 매핑</span><span class="sxs-lookup"><span data-stu-id="c16ab-605">Input mapping</span></span>
    - <span data-ttu-id="c16ab-606">이벤트 배달 스키마</span><span class="sxs-lookup"><span data-stu-id="c16ab-606">Event Delivery Schema</span></span>
    - <span data-ttu-id="c16ab-607">Private Link</span><span class="sxs-lookup"><span data-stu-id="c16ab-607">Private Link</span></span>
    - <span data-ttu-id="c16ab-608">클라우드 이벤트 V10 스키마</span><span class="sxs-lookup"><span data-stu-id="c16ab-608">Cloud Event V10 Schema</span></span>
    - <span data-ttu-id="c16ab-609">대상으로 Service Bus 항목</span><span class="sxs-lookup"><span data-stu-id="c16ab-609">Service Bus Topic As Destination</span></span>
    - <span data-ttu-id="c16ab-610">대상으로 Azure 함수</span><span class="sxs-lookup"><span data-stu-id="c16ab-610">Azure Function As Destination</span></span>
    - <span data-ttu-id="c16ab-611">WebHook 일괄 처리</span><span class="sxs-lookup"><span data-stu-id="c16ab-611">WebHook Batching</span></span>
    - <span data-ttu-id="c16ab-612">보안 웹후크(AAD 지원)</span><span class="sxs-lookup"><span data-stu-id="c16ab-612">Secure webhook (AAD support)</span></span>
    - <span data-ttu-id="c16ab-613">IpFiltering</span><span class="sxs-lookup"><span data-stu-id="c16ab-613">IpFiltering</span></span>
* <span data-ttu-id="c16ab-614">다음 Cmdlet이 업데이트 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-614">Updated cmdlets:</span></span>
    - <span data-ttu-id="c16ab-615">'New-AzEventGridSubscription'/'Update-AzEventGridSubscription':</span><span class="sxs-lookup"><span data-stu-id="c16ab-615">'New-AzEventGridSubscription'/'Update-AzEventGridSubscription':</span></span>
        - <span data-ttu-id="c16ab-616">웹후크 일괄 처리를 지원하기 위해 새로운 선택적 매개 변수를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-616">Add new optional parameters to support webhook batching.</span></span>
        - <span data-ttu-id="c16ab-617">AAD를 사용하여 보안 웹후크를 지원하는 새로운 선택적 매개 변수를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-617">Add new optional parameters to support secured webhook using AAD.</span></span>
        - <span data-ttu-id="c16ab-618">Azure 함수 및 Service Bus 항목을 새 대상으로 지원하기 위해 EndpointType 매개 변수에 대한 새 열거형을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-618">Add new enum for EndpointType parameter to support azure function and service bus topic as new destinations.</span></span>
        - <span data-ttu-id="c16ab-619">배달 스키마에 대한 새로운 선택적 매개 변수를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-619">Add new optional parameter for delivery schema.</span></span>
    - <span data-ttu-id="c16ab-620">'New-AzEventGridTopic'/'Update-AzEventGridTopic' 및 'New-AzEventGridDomain'/'Update-AzEventGridDomain':</span><span class="sxs-lookup"><span data-stu-id="c16ab-620">'New-AzEventGridTopic'/'Update-AzEventGridTopic' and 'New-AzEventGridDomain'/'Update-AzEventGridDomain':</span></span>
        - <span data-ttu-id="c16ab-621">IpFiltering을 지원하기 위해 새로운 선택적 매개 변수를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-621">Add new optional parameters to support IpFiltering.</span></span>
    - <span data-ttu-id="c16ab-622">'New-AzEventGridTopic'/'New-AzEventGridDomain':</span><span class="sxs-lookup"><span data-stu-id="c16ab-622">'New-AzEventGridTopic'/'New-AzEventGridDomain':</span></span>
        - <span data-ttu-id="c16ab-623">입력 매핑을 지원하기 위해 새로운 선택적 매개 변수를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-623">Add new optional parameters to support Input mapping.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="c16ab-624">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="c16ab-624">Az.FrontDoor</span></span>
* <span data-ttu-id="c16ab-625">API 2020-05-01을 사용하도록 업데이트된 모듈</span><span class="sxs-lookup"><span data-stu-id="c16ab-625">Updated module to use API 2020-05-01</span></span>
* <span data-ttu-id="c16ab-626">Storage, Keyvault 및 Web App Service 리소스에 대한 프라이빗 링크 지원을 추가함</span><span class="sxs-lookup"><span data-stu-id="c16ab-626">Added Private link support for Storage, Keyvault and Web App Service resources</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="c16ab-627">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="c16ab-627">Az.HDInsight</span></span>
* <span data-ttu-id="c16ab-628">국가 클라우드에서 ADLSGen1/2 스토리지로 클러스터를 만드는 것이 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-628">Supported creating cluster with ADLSGen1/2 storage in national clouds.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="c16ab-629">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="c16ab-629">Az.Monitor</span></span>
* <span data-ttu-id="c16ab-630">메트릭 또는 로그가 null인 경우 'Get-AzDiagnosticSetting'에 대한 버그 수정 [#12272]</span><span class="sxs-lookup"><span data-stu-id="c16ab-630">Fixed bug for 'Get-AzDiagnosticSetting' when metrics or logs are null [#12272]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="c16ab-631">Az.Network</span><span class="sxs-lookup"><span data-stu-id="c16ab-631">Az.Network</span></span>
* <span data-ttu-id="c16ab-632">VWan HubVnet 연결의 매개 변수 교환 수정</span><span class="sxs-lookup"><span data-stu-id="c16ab-632">Fixed parameters swap in VWan HubVnet connection</span></span>
* <span data-ttu-id="c16ab-633">Azure Network Virtual Appliance 사이트에 대한 새 cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="c16ab-633">Added new cmdlets for Azure Network Virtual Appliance Sites</span></span>
    - <span data-ttu-id="c16ab-634">'Get-AzVirtualApplianceSite'</span><span class="sxs-lookup"><span data-stu-id="c16ab-634">'Get-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="c16ab-635">'New-AzVirtualApplianceSite'</span><span class="sxs-lookup"><span data-stu-id="c16ab-635">'New-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="c16ab-636">'Remove-AzVirtualApplianceSite'</span><span class="sxs-lookup"><span data-stu-id="c16ab-636">'Remove-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="c16ab-637">'Update-AzVirtualApplianceSite'</span><span class="sxs-lookup"><span data-stu-id="c16ab-637">'Update-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="c16ab-638">'New-AzOffice365PolicyProperty'</span><span class="sxs-lookup"><span data-stu-id="c16ab-638">'New-AzOffice365PolicyProperty'</span></span>
* <span data-ttu-id="c16ab-639">Azure Network Virtual Appliance에 대한 새 cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="c16ab-639">Added new cmdlets for Azure Network Virtual Appliance</span></span>
    - <span data-ttu-id="c16ab-640">'Get-AzNetworkVirtualAppliance'</span><span class="sxs-lookup"><span data-stu-id="c16ab-640">'Get-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="c16ab-641">'New-AzNetworkVirtualAppliance'</span><span class="sxs-lookup"><span data-stu-id="c16ab-641">'New-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="c16ab-642">'Remove-AzNetworkVirtualAppliance'</span><span class="sxs-lookup"><span data-stu-id="c16ab-642">'Remove-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="c16ab-643">'Update-AzNetworkVirtualAppliance'</span><span class="sxs-lookup"><span data-stu-id="c16ab-643">'Update-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="c16ab-644">'Get-AzNetworkVirtualApplianceSku'</span><span class="sxs-lookup"><span data-stu-id="c16ab-644">'Get-AzNetworkVirtualApplianceSku'</span></span>
    - <span data-ttu-id="c16ab-645">'New-AzVirtualApplianceSkuProperty'</span><span class="sxs-lookup"><span data-stu-id="c16ab-645">'New-AzVirtualApplianceSkuProperty'</span></span>
* <span data-ttu-id="c16ab-646">Application Gateway를 Private Link 공통 cmdlet에 온보딩</span><span class="sxs-lookup"><span data-stu-id="c16ab-646">Onboarded Application Gateway to Private Link Common Cmdlets</span></span>
* <span data-ttu-id="c16ab-647">StorageSync를 Private Link 공통 cmdlet에 온보딩</span><span class="sxs-lookup"><span data-stu-id="c16ab-647">Onboarded StorageSync to Private Link Common Cmdlets</span></span>
* <span data-ttu-id="c16ab-648">SignalR을 Private Link 공통 cmdlet에 온보딩</span><span class="sxs-lookup"><span data-stu-id="c16ab-648">Onboarded SignalR to Private Link Common Cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="c16ab-649">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="c16ab-649">Az.RecoveryServices</span></span>
* <span data-ttu-id="c16ab-650">인증에 대한 프로젝트 참조 제거</span><span class="sxs-lookup"><span data-stu-id="c16ab-650">Removed project reference to Authentication</span></span>
* <span data-ttu-id="c16ab-651">Azure Backup 튜닝 cmdlet은 텍스트를 보다 정확하게 작성하는 데 도움이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-651">Azure Backup tuned cmdlets help text to be more accurate.</span></span>
* <span data-ttu-id="c16ab-652">Azure Backup은 'Get-AzRecoveryServicesBackupJob' cmdlet을 사용하여 MAB 에이전트 작업을 가져오는 지원을 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-652">Azure Backup added support for fetching MAB agent jobs using 'Get-AzRecoveryServicesBackupJob' cmdlet.</span></span>

#### <a name="azresources"></a><span data-ttu-id="c16ab-653">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="c16ab-653">Az.Resources</span></span>
* <span data-ttu-id="c16ab-654">SDK를 사용하도록 'Save-AzResourceGroupDeploymentTemplate'을 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-654">Updated 'Save-AzResourceGroupDeploymentTemplate' to use the SDK.</span></span>
* <span data-ttu-id="c16ab-655">'Unregister-AzResourceProvider' cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-655">Added 'Unregister-AzResourceProvider' cmdlet.</span></span>

#### <a name="azsql"></a><span data-ttu-id="c16ab-656">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="c16ab-656">Az.Sql</span></span>
* <span data-ttu-id="c16ab-657">Set-AzSqlInstanceActiveDirectoryAdministrator cmdlet에서 서비스 주체 및 게스트 사용자에 대한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-657">Added support for Service principal and guest users in Set-AzSqlInstanceActiveDirectoryAdministrator cmdlet'</span></span>
* <span data-ttu-id="c16ab-658">데이터 분류 cmdlet의 버그를 수정했습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-658">Fixed a bug in Data Classification cmdlets.'</span></span>
* <span data-ttu-id="c16ab-659">다음의 Azure SQL Managed Instance 장애 조치에 대한 지원 추가: 'Invoke-AzSqlInstanceFailover'</span><span class="sxs-lookup"><span data-stu-id="c16ab-659">Added support for Azure SQL Managed Instance failover: 'Invoke-AzSqlInstanceFailover'</span></span>

#### <a name="azstorage"></a><span data-ttu-id="c16ab-660">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="c16ab-660">Az.Storage</span></span>
* <span data-ttu-id="c16ab-661">일부 데이터 평면 cmdlet에 대해 UserAgent가 추가되지 않는 문제를 해결했습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-661">Fixed the issue that UserAgent is not added for some data plane cmdlets.</span></span>
* <span data-ttu-id="c16ab-662">MinimumTlsVersion 및 AllowBlobPublicAccess로 스토리지 계정 만들기/업데이트 지원</span><span class="sxs-lookup"><span data-stu-id="c16ab-662">Supported create/update Storage account with MinimumTlsVersion and AllowBlobPublicAccess</span></span>
    -  <span data-ttu-id="c16ab-663">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="c16ab-663">'New-AzStorageAccount'</span></span>
    -  <span data-ttu-id="c16ab-664">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="c16ab-664">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="c16ab-665">스토리지 계정의 Blob Service에서 버전 관리 사용/사용 안 함 지원</span><span class="sxs-lookup"><span data-stu-id="c16ab-665">Support enable/disable versioning on Blob Service of a Storage account</span></span>
    - <span data-ttu-id="c16ab-666">'Update-AzStorageBlobServiceProperty'</span><span class="sxs-lookup"><span data-stu-id="c16ab-666">'Update-AzStorageBlobServiceProperty'</span></span>
* <span data-ttu-id="c16ab-667">Blob 버전 관리로 Blob 나열 지원</span><span class="sxs-lookup"><span data-stu-id="c16ab-667">Support list blobs with blob versions</span></span>
    - <span data-ttu-id="c16ab-668">'Get-AzStorageBlob'</span><span class="sxs-lookup"><span data-stu-id="c16ab-668">'Get-AzStorageBlob'</span></span>
* <span data-ttu-id="c16ab-669">단일 Blob 스냅샷 또는 Blob 버전 가져오기/제거 지원</span><span class="sxs-lookup"><span data-stu-id="c16ab-669">Support get/remove single blob snapshot or blob version</span></span>
    - <span data-ttu-id="c16ab-670">'Get-AzStorageBlob'</span><span class="sxs-lookup"><span data-stu-id="c16ab-670">'Get-AzStorageBlob'</span></span>
    - <span data-ttu-id="c16ab-671">'Remove-AzStorageBlob'</span><span class="sxs-lookup"><span data-stu-id="c16ab-671">'Remove-AzStorageBlob'</span></span>
* <span data-ttu-id="c16ab-672">Azure.Storage.Blobs V12에서 생성된 Blob 개체의 파이프라인 지원</span><span class="sxs-lookup"><span data-stu-id="c16ab-672">Support pipeline from blob object generated from Azure.Storage.Blobs V12</span></span>
    - <span data-ttu-id="c16ab-673">'Get-AzStorageBlobContent'</span><span class="sxs-lookup"><span data-stu-id="c16ab-673">'Get-AzStorageBlobContent'</span></span>
    - <span data-ttu-id="c16ab-674">'New-AzStorageBlobSASToken'</span><span class="sxs-lookup"><span data-stu-id="c16ab-674">'New-AzStorageBlobSASToken'</span></span>
    - <span data-ttu-id="c16ab-675">'Remove-AzStorageBlob'</span><span class="sxs-lookup"><span data-stu-id="c16ab-675">'Remove-AzStorageBlob'</span></span>
    - <span data-ttu-id="c16ab-676">'Set-AzStorageBlobContent'</span><span class="sxs-lookup"><span data-stu-id="c16ab-676">'Set-AzStorageBlobContent'</span></span>
    - <span data-ttu-id="c16ab-677">'Start-AzStorageBlobCopy'</span><span class="sxs-lookup"><span data-stu-id="c16ab-677">'Start-AzStorageBlobCopy'</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="c16ab-678">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="c16ab-678">Az.StorageSync</span></span>
* <span data-ttu-id="c16ab-679">ApiVersion 2020-03-01을 대상으로 하는 새 버전의 StorageSync SDK 추가</span><span class="sxs-lookup"><span data-stu-id="c16ab-679">Added a new version StorageSync SDK targeting ApiVersion 2020-03-01</span></span>
* <span data-ttu-id="c16ab-680">스토리지 동기화 서비스 업데이트 cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="c16ab-680">Added Update Storage Sync Service cmdlet</span></span>
    - <span data-ttu-id="c16ab-681">'Set-AzStorageSyncService'</span><span class="sxs-lookup"><span data-stu-id="c16ab-681">'Set-AzStorageSyncService'</span></span>
* <span data-ttu-id="c16ab-682">IncomingTrafficPolicy 및 PrivateEndpointConnections가 StorageSyncService cmdlet에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-682">Added IncomingTrafficPolicy and PrivateEndpointConnections to StorageSyncService cmdlets.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="c16ab-683">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="c16ab-683">Az.Websites</span></span>
* <span data-ttu-id="c16ab-684">App Service 계획과 동일한 리소스 그룹에 속하지 않는 슬롯에 대한 작업을 수행하기 위한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="c16ab-684">Added support to perform operations for Slots not in the same resource group as the App Service Plan</span></span>

## <a name="430---june-2020"></a><span data-ttu-id="c16ab-685">4.3.0 - 2020년 6월</span><span class="sxs-lookup"><span data-stu-id="c16ab-685">4.3.0 - June 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="c16ab-686">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="c16ab-686">Az.Accounts</span></span>
* <span data-ttu-id="c16ab-687">기본적으로 환경 검색 설정이 지원되며 'Add-AzEnvironment'를 통해 환경을 추가할 수 있음</span><span class="sxs-lookup"><span data-stu-id="c16ab-687">Supported discovering environment setting by default and adding environment via 'Add-AzEnvironment'</span></span>
* <span data-ttu-id="c16ab-688">미리 로드된 어셈블리 업데이트 [#12024], [#11976]</span><span class="sxs-lookup"><span data-stu-id="c16ab-688">Update preloaded assemblies [#12024], [#11976]</span></span>
* <span data-ttu-id="c16ab-689">Azure.Core 어셈블리 업데이트</span><span class="sxs-lookup"><span data-stu-id="c16ab-689">Updated Azure.Core assembly</span></span>
* <span data-ttu-id="c16ab-690">다중 스레드 실행에서 'Connect-AzAccount'가 실패할 수 있는 문제 해결 [#11201]</span><span class="sxs-lookup"><span data-stu-id="c16ab-690">Fixed an issue that may cause 'Connect-AzAccount' to fail in multi-threaded execution [#11201]</span></span>

#### <a name="azaks"></a><span data-ttu-id="c16ab-691">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="c16ab-691">Az.Aks</span></span>
* <span data-ttu-id="c16ab-692">이전에 사용하던 [AccessProfile API](https://docs.microsoft.com/rest/api/aks/managedclusters/getaccessprofile)를 [ListClusterAdmin](https://docs.microsoft.com/rest/api/aks/managedclusters/listclusteradmincredentials) 및 [ListClusterUser](https://docs.microsoft.com/rest/api/aks/managedclusters/listclusterusercredentials) API 호출로 대체</span><span class="sxs-lookup"><span data-stu-id="c16ab-692">Replaced usage of old [AccessProfile API](https://docs.microsoft.com/rest/api/aks/managedclusters/getaccessprofile) with calls to [ListClusterAdmin](https://docs.microsoft.com/rest/api/aks/managedclusters/listclusteradmincredentials) and [ListClusterUser](https://docs.microsoft.com/rest/api/aks/managedclusters/listclusterusercredentials) APIs</span></span>

#### <a name="azbatch"></a><span data-ttu-id="c16ab-693">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="c16ab-693">Az.Batch</span></span>
* <span data-ttu-id="c16ab-694">'Microsoft.Azure.Management.Batch' SDK 버전 11.0.0을 사용하도록 Az.Batch 업데이트</span><span class="sxs-lookup"><span data-stu-id="c16ab-694">Updated Az.Batch to use 'Microsoft.Azure.Management.Batch' SDK version to 11.0.0</span></span>
* <span data-ttu-id="c16ab-695">'New-AzBatchAccount' cmdlet에서 BatchAccount ID를 설정하는 기능 추가</span><span class="sxs-lookup"><span data-stu-id="c16ab-695">Added the ability to set the BatchAccount Identity in the 'New-AzBatchAccount' cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="c16ab-696">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="c16ab-696">Az.CognitiveServices</span></span>
* <span data-ttu-id="c16ab-697">계정 기능 표시 지원</span><span class="sxs-lookup"><span data-stu-id="c16ab-697">Supported displaying account capabilities.</span></span>
* <span data-ttu-id="c16ab-698">PublicNetworkAccess 수정 지원</span><span class="sxs-lookup"><span data-stu-id="c16ab-698">Supported modifying PublicNetworkAccess.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="c16ab-699">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="c16ab-699">Az.Compute</span></span>
* <span data-ttu-id="c16ab-700">Set-AzVM 및 Set-AzVmssVM cmdlet에 SimulateEviction 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="c16ab-700">Added SimulateEviction parameter to Set-AzVM and Set-AzVmssVM cmdlets.</span></span>
* <span data-ttu-id="c16ab-701">AzGalleryImageVersion cmdlet에 대한 StorageAccountType 매개 변수의 인수 완성자에 'Premium_LRS' 추가</span><span class="sxs-lookup"><span data-stu-id="c16ab-701">Added 'Premium_LRS' to the argument completer of StorageAccountType parameter for New-AzGalleryImageVersion cmdlet.</span></span>
* <span data-ttu-id="c16ab-702">VMCustomScriptExtension에 Substatuses 추가 [#11297]</span><span class="sxs-lookup"><span data-stu-id="c16ab-702">Added Substatuses to VMCustomScriptExtension [#11297]</span></span>
* <span data-ttu-id="c16ab-703">New-AzVM 및 New-AzVMConfig cmdlet에 대한 EvictionPolicy 매개 변수의 인수 완성자에 'Delete' 추가</span><span class="sxs-lookup"><span data-stu-id="c16ab-703">Added 'Delete' to the argument completer of EvictionPolicy parameter for New-AzVM and New-AzVMConfig cmdlets.</span></span>
* <span data-ttu-id="c16ab-704">새 SAP용 VM 확장의 이름 수정</span><span class="sxs-lookup"><span data-stu-id="c16ab-704">Fixed name of new VM Extension for SAP</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="c16ab-705">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="c16ab-705">Az.DataFactory</span></span>
* <span data-ttu-id="c16ab-706">ADF .Net SDK 버전을 4.9.0으로 업데이트</span><span class="sxs-lookup"><span data-stu-id="c16ab-706">Updated ADF .Net SDK version to 4.9.0</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="c16ab-707">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="c16ab-707">Az.EventHub</span></span>
* <span data-ttu-id="c16ab-708">'New-AzEventHubNamespace' 및 'Set-AzEventHubNamespace' cmdlet에 관리 ID 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="c16ab-708">Added Managed Identity parameters to 'New-AzEventHubNamespace' and 'Set-AzEventHubNamespace' cmdlets</span></span>

#### <a name="azfunctions"></a><span data-ttu-id="c16ab-709">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="c16ab-709">Az.Functions</span></span>
* <span data-ttu-id="c16ab-710">PowerShell 7.0 및 Java 11 함수 앱을 만드는 지원 추가</span><span class="sxs-lookup"><span data-stu-id="c16ab-710">Added support to create PowerShell 7.0 and Java 11 function apps</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="c16ab-711">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="c16ab-711">Az.HDInsight</span></span>
* <span data-ttu-id="c16ab-712">호스트를 나열하고 HDInsight 클러스터의 특정 호스트를 다시 시작하는 기능 지원</span><span class="sxs-lookup"><span data-stu-id="c16ab-712">Supported listing hosts and restart specific hosts of the HDInsight cluster.</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="c16ab-713">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="c16ab-713">Az.HealthcareApis</span></span>
* <span data-ttu-id="c16ab-714">SDK 버전을 1.1.0으로 업데이트</span><span class="sxs-lookup"><span data-stu-id="c16ab-714">Updated the SDK version to 1.1.0</span></span>
* <span data-ttu-id="c16ab-715">설정 및 관리 ID 내보내기에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="c16ab-715">Added support for Export settings and Managed Identity</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="c16ab-716">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="c16ab-716">Az.Monitor</span></span>
* <span data-ttu-id="c16ab-717">'Set-AzActivityLogAlert'에 대한 입력 개체 매개 변수 수정</span><span class="sxs-lookup"><span data-stu-id="c16ab-717">Fixed input object parameter for 'Set-AzActivityLogAlert'</span></span>
* <span data-ttu-id="c16ab-718">'Set-AzActionGroup'에 대한 'InputObject' 매개 변수 수정 [#10868]</span><span class="sxs-lookup"><span data-stu-id="c16ab-718">Fixed 'InputObject' parameter for 'Set-AzActionGroup' [#10868]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="c16ab-719">Az.Network</span><span class="sxs-lookup"><span data-stu-id="c16ab-719">Az.Network</span></span>
* <span data-ttu-id="c16ab-720">'Remove-AzExpressRouteCircuitConnectionConfig'에 AddressPrefixType 매개 변수 지원 추가</span><span class="sxs-lookup"><span data-stu-id="c16ab-720">Added support for AddressPrefixType parameter to 'Remove-AzExpressRouteCircuitConnectionConfig'</span></span>
* <span data-ttu-id="c16ab-721">Azure FirewallPolicy에 대한 새 cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="c16ab-721">Added new cmdlets for Azure FirewallPolicy</span></span>
    - <span data-ttu-id="c16ab-722">'New-AzFirewallPolicyDnsSetting'</span><span class="sxs-lookup"><span data-stu-id="c16ab-722">'New-AzFirewallPolicyDnsSetting'</span></span>
    - <span data-ttu-id="c16ab-723">방화벽 정책에 대한 네트워크 규칙에서 대상 FQDN 지원</span><span class="sxs-lookup"><span data-stu-id="c16ab-723">Support for Destination FQDN in Network Rules for Firewall Policy</span></span>
* <span data-ttu-id="c16ab-724">백 엔드 주소 풀 작업에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="c16ab-724">Added support for backend address pool operations</span></span>
    - <span data-ttu-id="c16ab-725">'New-AzLoadBalancerBackendAddressConfig'</span><span class="sxs-lookup"><span data-stu-id="c16ab-725">'New-AzLoadBalancerBackendAddressConfig'</span></span>
    - <span data-ttu-id="c16ab-726">'New-AzLoadBalancerBackendAddressPool'</span><span class="sxs-lookup"><span data-stu-id="c16ab-726">'New-AzLoadBalancerBackendAddressPool'</span></span>
    - <span data-ttu-id="c16ab-727">'Set-AzLoadBalancerBackendAddressPool'</span><span class="sxs-lookup"><span data-stu-id="c16ab-727">'Set-AzLoadBalancerBackendAddressPool'</span></span>
    - <span data-ttu-id="c16ab-728">'Remove-AzLoadBalancerBackendAddressPool'</span><span class="sxs-lookup"><span data-stu-id="c16ab-728">'Remove-AzLoadBalancerBackendAddressPool'</span></span>
    - <span data-ttu-id="c16ab-729">'Get-AzLoadBalancerBackendAddressPool'</span><span class="sxs-lookup"><span data-stu-id="c16ab-729">'Get-AzLoadBalancerBackendAddressPool'</span></span>
* <span data-ttu-id="c16ab-730">'New-AzIpGroup'에 대한 이름 유효성 검사 추가</span><span class="sxs-lookup"><span data-stu-id="c16ab-730">Added name validation for 'New-AzIpGroup'</span></span>
* <span data-ttu-id="c16ab-731">Azure FirewallPolicy에 대한 새 cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="c16ab-731">Added new cmdlets for Azure FirewallPolicy</span></span>
    - <span data-ttu-id="c16ab-732">'New-AzFirewallPolicyThreatIntelWhitelist'</span><span class="sxs-lookup"><span data-stu-id="c16ab-732">'New-AzFirewallPolicyThreatIntelWhitelist'</span></span>
* <span data-ttu-id="c16ab-733">기능에 대한 새로운 명령이 업데이트됨: VirtualWan P2SVpnGateway에서 사용자 지정 dns 서버 설정/제거</span><span class="sxs-lookup"><span data-stu-id="c16ab-733">Updated below commands for feature: Custom dns servers set/remove on VirtualWan P2SVpnGateway.</span></span>
    - <span data-ttu-id="c16ab-734">New-AzP2sVpnGateway 업데이트됨: 고객이 P2SVpnGateway에 설정할 dns 서버를 지정할 수 있는 선택적 매개 변수 '-CustomDnsServer'가 추가되었으며, 이 매개 변수는 지점 및 사이트 간 클라이언트에서 사용 가능</span><span class="sxs-lookup"><span data-stu-id="c16ab-734">Updated New-AzP2sVpnGateway: Added optional parameter '-CustomDnsServer' for customers to specify their dns servers to set on P2SVpnGateway, which can be used by Point to site clients.</span></span>
    - <span data-ttu-id="c16ab-735">Update-AzP2sVpnGateway 업데이트됨: 고객이 P2SVpnGateway에 설정할 dns 서버를 지정할 수 있는 선택적 매개 변수 '-CustomDnsServer'가 추가되었으며, 이 매개 변수는 지점 및 사이트 간 클라이언트에서 사용 가능</span><span class="sxs-lookup"><span data-stu-id="c16ab-735">Updated Update-AzP2sVpnGateway: Added optional parameter '-CustomDnsServer' for customers to specify their dns servers to set on P2SVpnGateway, which can be used by Point to site clients.</span></span>
* <span data-ttu-id="c16ab-736">'Update-AzVpnGateway' 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="c16ab-736">Updated 'Update-AzVpnGateway'</span></span>
    - <span data-ttu-id="c16ab-737">고객이 VpnGateway에 설정할 사용자 지정 bgps를 지정할 수 있도록 선택적 매개 변수 '-BgpPeeringAddress' 추가</span><span class="sxs-lookup"><span data-stu-id="c16ab-737">Added optional parameter '-BgpPeeringAddress' for customers to specify their custom bgps to set on VpnGateway.</span></span>
* <span data-ttu-id="c16ab-738">VirtualHub 리소스의 라우팅 상태 초기화를 지원하는 새 cmdlet 추가:</span><span class="sxs-lookup"><span data-stu-id="c16ab-738">Added new cmdlet to support resetting the routing state of a VirtualHub resource:</span></span>
    - <span data-ttu-id="c16ab-739">'Reset-AzHubRouter'</span><span class="sxs-lookup"><span data-stu-id="c16ab-739">'Reset-AzHubRouter'</span></span>
* <span data-ttu-id="c16ab-740">방화벽 정책에 대한 최근 Swagger 변화에 따라 아래 항목 업데이트</span><span class="sxs-lookup"><span data-stu-id="c16ab-740">Updated below things based on recent swagger change for Firewall Policy</span></span>
    - <span data-ttu-id="c16ab-741">RuleGroup, RuleCollectionGroup 및 RuleType의 이름 변경</span><span class="sxs-lookup"><span data-stu-id="c16ab-741">Changes names for RuleGroup, RuleCollectionGroup and RuleType</span></span>
    - <span data-ttu-id="c16ab-742">여러 NAT 규칙 컬렉션을 지원하도록 방화벽 정책 NAT 규칙 컬렉션에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="c16ab-742">Added support for Firewall Policy NAT Rule Collections to support multiple NAT Rule Collection</span></span>
* <span data-ttu-id="c16ab-743">[호환성이 손상되는 변경] 'New-AzFirewallPolicyApplicationRule' 및 'New-AzFirewallPolicyNetworkRule'에 대한 필수 매개 변수 'SourceIpGroup' 추가</span><span class="sxs-lookup"><span data-stu-id="c16ab-743">[Breaking Change] Added mandatory parameter 'SourceIpGroup' for 'New-AzFirewallPolicyApplicationRule' and 'New-AzFirewallPolicyNetworkRule'.</span></span>
* <span data-ttu-id="c16ab-744">[호환성이 손상되는 변경] 'New-AzFirewallPolicyApplicationRule' 수정, 'SourceAddress' 매개 변수를 필수로 변경</span><span class="sxs-lookup"><span data-stu-id="c16ab-744">[Breaking Change] Fixed 'New-AzFirewallPolicyApplicationRule', parameter 'SourceAddress' to be mandatory.</span></span>
* <span data-ttu-id="c16ab-745">[호환성이 손상되는 변경] 'New-AzFirewallPolicyApplicationRule' 수정, 'SourceAddress' 매개 변수를 필수로 변경</span><span class="sxs-lookup"><span data-stu-id="c16ab-745">[Breaking Change] Fixed 'New-AzFirewallPolicyApplicationRule', parameter 'SourceAddress' to be mandatory.</span></span>
* <span data-ttu-id="c16ab-746">[호환성이 손상되는 변경] 다음 필수 매개 변수 제거: 'New-AzFirewallPolicyNatRuleCollection'의 'TranslatedAddress', 'TranslatedPort'</span><span class="sxs-lookup"><span data-stu-id="c16ab-746">[Breaking Change] Removed mandatory parameters: 'TranslatedAddress', 'TranslatedPort' for 'New-AzFirewallPolicyNatRuleCollection'.</span></span>
* <span data-ttu-id="c16ab-747">PrivateLink On Application Gateway를 지원하는 새 cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="c16ab-747">Added new cmdlets to support PrivateLink On Application Gateway</span></span>
    - <span data-ttu-id="c16ab-748">'New-AzApplicationGatewayPrivateLinkConfiguration'</span><span class="sxs-lookup"><span data-stu-id="c16ab-748">'New-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="c16ab-749">'Get-AzApplicationGatewayPrivateLinkConfiguration'</span><span class="sxs-lookup"><span data-stu-id="c16ab-749">'Get-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="c16ab-750">'New-AzApplicationGatewayPrivateLinkConfiguration'</span><span class="sxs-lookup"><span data-stu-id="c16ab-750">'New-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="c16ab-751">'Set-AzApplicationGatewayPrivateLinkConfiguration'</span><span class="sxs-lookup"><span data-stu-id="c16ab-751">'Set-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="c16ab-752">'Remove-AzApplicationGatewayPrivateLinkConfiguration'</span><span class="sxs-lookup"><span data-stu-id="c16ab-752">'Remove-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="c16ab-753">'New-AzApplicationGatewayPrivateLinkIpConfiguration'</span><span class="sxs-lookup"><span data-stu-id="c16ab-753">'New-AzApplicationGatewayPrivateLinkIpConfiguration'</span></span>
* <span data-ttu-id="c16ab-754">VirtualHub의 HubRouteTables 자식 리소스에 대한 새 cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="c16ab-754">Added new cmdlets for HubRouteTables child resource of VirtualHub.</span></span>
    - <span data-ttu-id="c16ab-755">'New-AzVHubRoute'</span><span class="sxs-lookup"><span data-stu-id="c16ab-755">'New-AzVHubRoute'</span></span>
    - <span data-ttu-id="c16ab-756">'New-AzVHubRouteTable'</span><span class="sxs-lookup"><span data-stu-id="c16ab-756">'New-AzVHubRouteTable'</span></span>
    - <span data-ttu-id="c16ab-757">'Get-AzVHubRouteTable'</span><span class="sxs-lookup"><span data-stu-id="c16ab-757">'Get-AzVHubRouteTable'</span></span>
    - <span data-ttu-id="c16ab-758">'Update-AzVHubRouteTable'</span><span class="sxs-lookup"><span data-stu-id="c16ab-758">'Update-AzVHubRouteTable'</span></span>
    - <span data-ttu-id="c16ab-759">'Remove-AzVHubRouteTable'</span><span class="sxs-lookup"><span data-stu-id="c16ab-759">'Remove-AzVHubRouteTable'</span></span>
* <span data-ttu-id="c16ab-760">VirtualWan의 사용자 지정 라우팅에 대한 선택적 RoutingConfiguration 입력 매개 변수를 지원하도록 기존 cmdlet 업데이트</span><span class="sxs-lookup"><span data-stu-id="c16ab-760">Updated existing cmdlets to support optional RoutingConfiguration input parameter for custom routing in VirtualWan.</span></span>
    - <span data-ttu-id="c16ab-761">'New-AzExpressRouteConnection'</span><span class="sxs-lookup"><span data-stu-id="c16ab-761">'New-AzExpressRouteConnection'</span></span>
    - <span data-ttu-id="c16ab-762">'Set-AzExpressRouteConnection'</span><span class="sxs-lookup"><span data-stu-id="c16ab-762">'Set-AzExpressRouteConnection'</span></span>
    - <span data-ttu-id="c16ab-763">'New-AzVirtualHubVnetConnection'</span><span class="sxs-lookup"><span data-stu-id="c16ab-763">'New-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="c16ab-764">'Update-AzVirtualHubVnetConnection'</span><span class="sxs-lookup"><span data-stu-id="c16ab-764">'Update-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="c16ab-765">'New-AzVpnConnection'</span><span class="sxs-lookup"><span data-stu-id="c16ab-765">'New-AzVpnConnection'</span></span>
    - <span data-ttu-id="c16ab-766">'Update-AzVpnConnection'</span><span class="sxs-lookup"><span data-stu-id="c16ab-766">'Update-AzVpnConnection'</span></span>
    - <span data-ttu-id="c16ab-767">'New-AzP2sVpnGateway'</span><span class="sxs-lookup"><span data-stu-id="c16ab-767">'New-AzP2sVpnGateway'</span></span>
    - <span data-ttu-id="c16ab-768">'Update-AzP2sVpnGateway'</span><span class="sxs-lookup"><span data-stu-id="c16ab-768">'Update-AzP2sVpnGateway'</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="c16ab-769">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="c16ab-769">Az.OperationalInsights</span></span>
* <span data-ttu-id="c16ab-770">PSWorkspace가 IOperationalInsightsWorkspace를 구현하지 않는 버그 수정 [#12135]</span><span class="sxs-lookup"><span data-stu-id="c16ab-770">Fixed bug PSWorkspace doesn't implement IOperationalInsightsWorkspace [#12135]</span></span>
* <span data-ttu-id="c16ab-771">'Set-AzOperationalInsightsWorkspace'에서 'Sku' 매개 변수의 올바른 값 세트에 'pergb2018' 추가</span><span class="sxs-lookup"><span data-stu-id="c16ab-771">Added 'pergb2018' to valid value set of parameter 'Sku' in 'Set-AzOperationalInsightsWorkspace'</span></span> 
* <span data-ttu-id="c16ab-772">매개 변수 'FunctionParameter'에 대한 별칭 'FunctionParameters' 추가</span><span class="sxs-lookup"><span data-stu-id="c16ab-772">Added alias 'FunctionParameters' for parameter 'FunctionParameter' to</span></span>
    - <span data-ttu-id="c16ab-773">'New-AzOperationalInsightsSavedSearch'</span><span class="sxs-lookup"><span data-stu-id="c16ab-773">'New-AzOperationalInsightsSavedSearch'</span></span>
    - <span data-ttu-id="c16ab-774">'Set-AzOperationalInsightsSavedSearch'</span><span class="sxs-lookup"><span data-stu-id="c16ab-774">'Set-AzOperationalInsightsSavedSearch'</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="c16ab-775">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="c16ab-775">Az.RecoveryServices</span></span>
* <span data-ttu-id="c16ab-776">Azure Backup에서 MAB 항목을 가져오기 위한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="c16ab-776">Azure Backup added support for fetching MAB items.</span></span>
* <span data-ttu-id="c16ab-777">Azure Site Recovery에서 'StandardSSD_LRS' 디스크 형식 지원</span><span class="sxs-lookup"><span data-stu-id="c16ab-777">Azure Site Recovery supports disk type 'StandardSSD_LRS'</span></span>

#### <a name="azresources"></a><span data-ttu-id="c16ab-778">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="c16ab-778">Az.Resources</span></span>
* <span data-ttu-id="c16ab-779">'PSADUser'에서 'UsageLocation', 'GivenName', 'Surname', 'AccountEnabled', 'MailNickname', 'Mail' 추가 [#10526] [#10497]</span><span class="sxs-lookup"><span data-stu-id="c16ab-779">Added 'UsageLocation', 'GivenName', 'Surname', 'AccountEnabled', 'MailNickname', 'Mail' on 'PSADUser' [#10526] [#10497]</span></span>
* <span data-ttu-id="c16ab-780">'Get-AzADUser'에서 '-Mail'이 작동하지 않는 문제 해결 [#11981]</span><span class="sxs-lookup"><span data-stu-id="c16ab-780">Fixed issue that '-Mail' doesn't work on 'Get-AzADUser' [#11981]</span></span>
* <span data-ttu-id="c16ab-781">'Get-AzDeploymentWhatIfResult' 및 'Get-AzResourceGroupDeploymentWhatIfResult'에 '-ExcludeChangeType' 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="c16ab-781">Added '-ExcludeChangeType' parameter to 'Get-AzDeploymentWhatIfResult' and 'Get-AzResourceGroupDeploymentWhatIfResult'</span></span>
* <span data-ttu-id="c16ab-782">'New-AzDeployment' 및 'New-AzResourceGroupDeployment'에 '-WhatIfExcludeChangeType' 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="c16ab-782">Added '-WhatIfExcludeChangeType' parameter to 'New-AzDeployment' and 'New-AzResourceGroupDeployment'</span></span>
* <span data-ttu-id="c16ab-783">보다 나은 오류 메시지를 표시하도록 'Test-Az\*Deployment' cmdlet 업데이트</span><span class="sxs-lookup"><span data-stu-id="c16ab-783">Updated 'Test-Az\*Deployment' cmdlets to show better error messages</span></span>
* <span data-ttu-id="c16ab-784">deployment create 및 What-If cmdlet의 '-Name' 매개 변수에 대한 도움말 메시지 수정</span><span class="sxs-lookup"><span data-stu-id="c16ab-784">Fixed help message for '-Name' parameter of deployment create and What-If cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="c16ab-785">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="c16ab-785">Az.Sql</span></span>
* <span data-ttu-id="c16ab-786">Set SQL Server Azure Active Directory Admin cmdlet의 서비스 주체에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="c16ab-786">Added support for service principal for Set SQL Server Azure Active Directory Admin cmdlet</span></span>
* <span data-ttu-id="c16ab-787">데이터 분류 cmdlet의 동기화 문제 해결</span><span class="sxs-lookup"><span data-stu-id="c16ab-787">Fixed sync issue in Data Classification cmdlets.</span></span>
* <span data-ttu-id="c16ab-788">'Set-AzSqlServerActiveDirectoryAdministrator'에서 메일로 사용자 검색 지원 [#12192]</span><span class="sxs-lookup"><span data-stu-id="c16ab-788">Supported searching user by mail on 'Set-AzSqlServerActiveDirectoryAdministrator' [#12192]</span></span>

#### <a name="azstorage"></a><span data-ttu-id="c16ab-789">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="c16ab-789">Az.Storage</span></span>
* <span data-ttu-id="c16ab-790">RequireInfrastructureEncryption을 사용하여 스토리지 계정 만들기 지원</span><span class="sxs-lookup"><span data-stu-id="c16ab-790">Supported create Storage account with RequireInfrastructureEncryption</span></span>
    -  <span data-ttu-id="c16ab-791">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="c16ab-791">'New-AzStorageAccount'</span></span>
* <span data-ttu-id="c16ab-792">Azure.Core 로딩 논리를 Az.Accounts로 이동</span><span class="sxs-lookup"><span data-stu-id="c16ab-792">Moved the logic of loading Azure.Core to Az.Accounts</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="c16ab-793">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="c16ab-793">Az.Websites</span></span>
* <span data-ttu-id="c16ab-794">'Restore-AzDeletedWebApp'에서 복원이 실패할 경우 생성된 웹앱을 삭제하는 보호 기능 추가</span><span class="sxs-lookup"><span data-stu-id="c16ab-794">Added safeguard to delete created webapp if restore failed in 'Restore-AzDeletedWebApp'</span></span>
* <span data-ttu-id="c16ab-795">'New-AzWebApp' 및 'New-AzWebAppSlot'에 대한 'SourceWebApp.Location' 추가</span><span class="sxs-lookup"><span data-stu-id="c16ab-795">Added 'SourceWebApp.Location' for 'New-AzWebApp' and 'New-AzWebAppSlot'</span></span>
* <span data-ttu-id="c16ab-796">'Set-AzWebApp' 및 'Set-AzWebAppSlot'에서 컨테이너 설정을 변경할 수 없는 버그 수정</span><span class="sxs-lookup"><span data-stu-id="c16ab-796">Fixed bug that prevented changing Container settings in 'Set-AzWebApp' and 'Set-AzWebAppSlot'</span></span>
* <span data-ttu-id="c16ab-797">Get-AzWebApp에 대한 -Name을 제공하지 않으면 SiteConfig를 가져오는 버그 수정</span><span class="sxs-lookup"><span data-stu-id="c16ab-797">Fixed bug to get SiteConfig when -Name is not given for Get-AzWebApp</span></span>
* <span data-ttu-id="c16ab-798">Linux 앱용 ASP를 만드는 지원 추가</span><span class="sxs-lookup"><span data-stu-id="c16ab-798">Added a support to create ASP for Linux Apps</span></span>
* <span data-ttu-id="c16ab-799">리소스 그룹 간 복제에 대한 예외 추가</span><span class="sxs-lookup"><span data-stu-id="c16ab-799">Added exceptions for clone across resource groups</span></span>

## <a name="420---june-2020"></a><span data-ttu-id="c16ab-800">4.2.0 - 2020년 6월</span><span class="sxs-lookup"><span data-stu-id="c16ab-800">4.2.0 - June 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="c16ab-801">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="c16ab-801">Az.Accounts</span></span>
* <span data-ttu-id="c16ab-802">Azure Automation 또는 PowerShell 작업에서 Az가 로그를 건너뛸 수 있는 문제 수정[#11492]</span><span class="sxs-lookup"><span data-stu-id="c16ab-802">Fixed an issue that may cause Az to skip logs in Azure Automation or PowerShell jobs [#11492]</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="c16ab-803">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="c16ab-803">Az.AnalysisServices</span></span>
* <span data-ttu-id="c16ab-804">데이터 평면 cmdlet의 어셈블리 버전 업데이트</span><span class="sxs-lookup"><span data-stu-id="c16ab-804">Updated assembly version of data plane cmdlets</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="c16ab-805">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="c16ab-805">Az.ApiManagement</span></span>
* <span data-ttu-id="c16ab-806">서비스 관리 cmdlet의 어셈블리 버전 업데이트</span><span class="sxs-lookup"><span data-stu-id="c16ab-806">Updated assembly version of service management cmdlets</span></span>

#### <a name="azbilling"></a><span data-ttu-id="c16ab-807">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="c16ab-807">Az.Billing</span></span>
* <span data-ttu-id="c16ab-808">소비 cmdlet의 어셈블리 버전 업데이트</span><span class="sxs-lookup"><span data-stu-id="c16ab-808">Updated assembly version of consumption cmdlets</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="c16ab-809">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="c16ab-809">Az.CognitiveServices</span></span>
* <span data-ttu-id="c16ab-810">PrivateEndpoint 및 PublicNetworkAccess control을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-810">Support PrivateEndpoint and PublicNetworkAccess control.</span></span> 

#### <a name="azdatafactory"></a><span data-ttu-id="c16ab-811">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="c16ab-811">Az.DataFactory</span></span>
* <span data-ttu-id="c16ab-812">데이터 팩터리 V2 cmdlet의 어셈블리 버전 업데이트</span><span class="sxs-lookup"><span data-stu-id="c16ab-812">Updated assembly version of data factory V2 cmdlets</span></span>

#### <a name="azdatashare"></a><span data-ttu-id="c16ab-813">Az.DataShare</span><span class="sxs-lookup"><span data-stu-id="c16ab-813">Az.DataShare</span></span>
* <span data-ttu-id="c16ab-814">''Az.DataShare'' 모듈의 일반 공급</span><span class="sxs-lookup"><span data-stu-id="c16ab-814">General availability of ''Az.DataShare'' module</span></span>

#### <a name="azdesktopvirtualization"></a><span data-ttu-id="c16ab-815">Az.DesktopVirtualization</span><span class="sxs-lookup"><span data-stu-id="c16ab-815">Az.DesktopVirtualization</span></span>
* <span data-ttu-id="c16ab-816">''Az.DesktopVirtualization'' 모듈의 일반 공급</span><span class="sxs-lookup"><span data-stu-id="c16ab-816">General availability of ''Az.DesktopVirtualization'' module</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="c16ab-817">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="c16ab-817">Az.OperationalInsights</span></span>
* <span data-ttu-id="c16ab-818">SDK를 0.21.0으로 업그레이드</span><span class="sxs-lookup"><span data-stu-id="c16ab-818">Upgraded SDK to 0.21.0</span></span>
* <span data-ttu-id="c16ab-819">다음에 선택적 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="c16ab-819">Added optional parameters to</span></span> 
    - <span data-ttu-id="c16ab-820">'New-AzOperationalInsightsSavedSearch'</span><span class="sxs-lookup"><span data-stu-id="c16ab-820">'New-AzOperationalInsightsSavedSearch'</span></span>
    - <span data-ttu-id="c16ab-821">'Set-AzOperationalInsightsSavedSearch'</span><span class="sxs-lookup"><span data-stu-id="c16ab-821">'Set-AzOperationalInsightsSavedSearch'</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="c16ab-822">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="c16ab-822">Az.PolicyInsights</span></span>
* <span data-ttu-id="c16ab-823">'Start-AzPolicyComplianceScan'의 예제 3 수정</span><span class="sxs-lookup"><span data-stu-id="c16ab-823">Corrected example 3 for 'Start-AzPolicyComplianceScan'</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="c16ab-824">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="c16ab-824">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="c16ab-825">PowerBI cmdlet의 어셈블리 버전 업데이트</span><span class="sxs-lookup"><span data-stu-id="c16ab-825">Updated assembly version of PowerBI cmdlets</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="c16ab-826">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="c16ab-826">Az.PrivateDns</span></span>
* <span data-ttu-id="c16ab-827">Remove-AzPrivateDnsRecordSet에 대한 자세한 정보 출력 문자열 형식 수정</span><span class="sxs-lookup"><span data-stu-id="c16ab-827">Corrected verbose output string formatting for Remove-AzPrivateDnsRecordSet</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="c16ab-828">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="c16ab-828">Az.RecoveryServices</span></span>
* <span data-ttu-id="c16ab-829">xml 입력에서 영역 간 복제를 위한 복구 계획을 세우기 위한 Azure Site Recovery 지원.</span><span class="sxs-lookup"><span data-stu-id="c16ab-829">Azure Site Recovery support for creating recovery plan for zone to zone replication from xml input.</span></span>
* <span data-ttu-id="c16ab-830">SiteRecovery 및 Backup cmdlet의 어셈블리 버전 업데이트</span><span class="sxs-lookup"><span data-stu-id="c16ab-830">Updated assembly version of SiteRecovery and Backup cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="c16ab-831">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="c16ab-831">Az.Resources</span></span>
* <span data-ttu-id="c16ab-832">Get-AzDeploymentScriptLog 및 Save-AzDeploymentScriptLog cmdlet에 Tail 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="c16ab-832">Added Tail parameter to Get-AzDeploymentScriptLog and Save-AzDeploymentScriptLog cmdlets</span></span>
* <span data-ttu-id="c16ab-833">형식이 지정된 출력 속성을 Get-AzDeploymentScript cmdlet 출력에 표시</span><span class="sxs-lookup"><span data-stu-id="c16ab-833">Formatted Output property and show it on the Get-AzDeploymentScript cmdlet output</span></span>
* <span data-ttu-id="c16ab-834">-DeploymentScriptInputObject 매개 변수의 이름이 -DeploymentScriptObject로 변경</span><span class="sxs-lookup"><span data-stu-id="c16ab-834">Renamed -DeploymentScriptInputObject parameter to -DeploymentScriptObject</span></span>
* <span data-ttu-id="c16ab-835">cmdlet 메시지에서 누락된 파일/대상 이름이 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-835">Fixed missing file/target name in cmdlet messages.</span></span>
* <span data-ttu-id="c16ab-836">리소스 관리자 및 태그 cmdlet의 어셈블리 버전 업데이트</span><span class="sxs-lookup"><span data-stu-id="c16ab-836">Updated assembly version of resource manager and tags cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="c16ab-837">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="c16ab-837">Az.Sql</span></span>
* <span data-ttu-id="c16ab-838">UsePrivateLinkConnection을 'New-AzSqlSyncGroup', 'Update-AzSqlSyncGroup', 'New-AzSqlSyncMember' 및 'Update-AzSqlSyncMember'에 추가</span><span class="sxs-lookup"><span data-stu-id="c16ab-838">Added UsePrivateLinkConnection to 'New-AzSqlSyncGroup', 'Update-AzSqlSyncGroup', 'New-AzSqlSyncMember' and 'Update-AzSqlSyncMember'</span></span>
* <span data-ttu-id="c16ab-839">SyncMemberAzureDatabaseResourceId를 'New-AzSqlSyncMember' 및 'Update-AzSqlSyncMember'에 추가</span><span class="sxs-lookup"><span data-stu-id="c16ab-839">Added SyncMemberAzureDatabaseResourceId to 'New-AzSqlSyncMember' and 'Update-AzSqlSyncMember'</span></span>
* <span data-ttu-id="c16ab-840">SQL Server Azure Active Directory Admin cmdlet을 설정하는 게스트 사용자 조회 지원 추가</span><span class="sxs-lookup"><span data-stu-id="c16ab-840">Added Guest user lookup support to Set SQL Server Azure Active Directory Admin cmdlet</span></span>

#### <a name="azstorage"></a><span data-ttu-id="c16ab-841">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="c16ab-841">Az.Storage</span></span>
* <span data-ttu-id="c16ab-842">데이터 평면 cmdlet의 어셈블리 버전 업데이트</span><span class="sxs-lookup"><span data-stu-id="c16ab-842">Updated assembly version of data plane cmdlets</span></span>

## <a name="410---may-2020"></a><span data-ttu-id="c16ab-843">4.1.0 - 2020년 5월</span><span class="sxs-lookup"><span data-stu-id="c16ab-843">4.1.0 - May 2020</span></span>
### <a name="highlights-since-the-last-release"></a><span data-ttu-id="c16ab-844">마지막 릴리스 이후의 주요 사항</span><span class="sxs-lookup"><span data-stu-id="c16ab-844">Highlights since the last release</span></span>
* <span data-ttu-id="c16ab-845">지원되는 PowerShell 버전: Windows PowerShell 5.1, PowerShell Core 6.2.4 이상, PowerShell 7</span><span class="sxs-lookup"><span data-stu-id="c16ab-845">Supported PowerShell versions: Windows PowerShell 5.1, PowerShell Core 6.2.4+, PowerShell 7</span></span>
* <span data-ttu-id="c16ab-846">Az.Functions 일반 공급</span><span class="sxs-lookup"><span data-stu-id="c16ab-846">General availability of Az.Functions</span></span> 
* <span data-ttu-id="c16ab-847">Az.ApiManagement, Az.Batch, Az.Compute, Az.KeyVault, Az.Monitor, Az.Network, Az.OperationalInsights, Az.Resources 및 Az.Storage의 주요 릴리스 출시</span><span class="sxs-lookup"><span data-stu-id="c16ab-847">Az.ApiManagement, Az.Batch, Az.Compute, Az.KeyVault, Az.Monitor, Az.Network, Az.OperationalInsights, Az.Resources, and Az.Storage have major release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="c16ab-848">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="c16ab-848">Az.Accounts</span></span>
* <span data-ttu-id="c16ab-849">'AzureSynapseAnalyticsEndpointResourceId' 및 'AzureSynapseAnalyticsEndpointSuffix' 매개 변수를 허용하도록 'Add-AzEnvironment' 및 'Set-AzEnvironment' 업데이트</span><span class="sxs-lookup"><span data-stu-id="c16ab-849">Updated 'Add-AzEnvironment' and 'Set-AzEnvironment' to accept parameters 'AzureSynapseAnalyticsEndpointResourceId' and 'AzureSynapseAnalyticsEndpointSuffix'</span></span>
* <span data-ttu-id="c16ab-850">Az.Accounts에 Azure.Core 관련 어셈블리가 추가되었으며 지원되는 PowerShell 플랫폼은 Windows PowerShell 5.1, PowerShell Core 6.2.4, PowerShell 7+입니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-850">Added Azure.Core related assemblies into Az.Accounts, supported PowerShell platforms include Windows PowerShell 5.1, PowerShell Core 6.2.4, PowerShell 7+</span></span>

#### <a name="azaks"></a><span data-ttu-id="c16ab-851">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="c16ab-851">Az.Aks</span></span>
* <span data-ttu-id="c16ab-852">API 버전을 2019-10-01로 업그레이드</span><span class="sxs-lookup"><span data-stu-id="c16ab-852">Upgraded API Version to 2019-10-01</span></span>
* <span data-ttu-id="c16ab-853">Windows 컨테이너를 사용하여 AKS 만들기 지원</span><span class="sxs-lookup"><span data-stu-id="c16ab-853">Supported to create AKS using Windows container</span></span>
* <span data-ttu-id="c16ab-854">새 cmdlet 추가: 'New-AzAksNodePool', 'Update-AzAksNodePool', 'Remove-AzAksNodePool', 'Get-AzAksNodePool', 'Install-AzAksKubectl', 'Get-AzAksVersion'</span><span class="sxs-lookup"><span data-stu-id="c16ab-854">Provided new cmdlets: 'New-AzAksNodePool', 'Update-AzAksNodePool', 'Remove-AzAksNodePool',        'Get-AzAksNodePool', 'Install-AzAksKubectl', 'Get-AzAksVersion'</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="c16ab-855">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="c16ab-855">Az.ApiManagement</span></span>
* <span data-ttu-id="c16ab-856">'New-AzApiManagement' 및 'Set-AzApiManagement': [-AssignIdentity] 매개 변수 이름을 [-SystemAssignedIdentity]로 변경</span><span class="sxs-lookup"><span data-stu-id="c16ab-856">'New-AzApiManagement' and 'Set-AzApiManagement': [-AssignIdentity] parameter renamed as [-SystemAssignedIdentity]</span></span>
* <span data-ttu-id="c16ab-857">'New-AzApiManagement' 및 'Set-AzApiManagement': 새 매개 변수 추가: [-UserAssignedIdentity <String[]>]</span><span class="sxs-lookup"><span data-stu-id="c16ab-857">'New-AzApiManagement' and 'Set-AzApiManagement': New parameter added: [-UserAssignedIdentity <String[]>]</span></span>
* <span data-ttu-id="c16ab-858">'Get-AzApiManagementProperty': 'Get-AzApiManagementNamedValue'로 이름 변경.</span><span class="sxs-lookup"><span data-stu-id="c16ab-858">'Get-AzApiManagementProperty': renamed as 'Get-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="c16ab-859">PropertyId 매개 변수 이름을 NamedValueId로 변경.</span><span class="sxs-lookup"><span data-stu-id="c16ab-859">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="c16ab-860">'New-AzApiManagementProperty': 'New-AzApiManagementNamedValue'로 이름 변경.</span><span class="sxs-lookup"><span data-stu-id="c16ab-860">'New-AzApiManagementProperty': renamed as 'New-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="c16ab-861">PropertyId 매개 변수 이름을 NamedValueId로 변경.</span><span class="sxs-lookup"><span data-stu-id="c16ab-861">PropertyId parameter renamed as NamedValueId.</span></span> 
* <span data-ttu-id="c16ab-862">'Set-AzApiManagementProperty': 'Set-AzApiManagementNamedValue'로 이름 변경.</span><span class="sxs-lookup"><span data-stu-id="c16ab-862">'Set-AzApiManagementProperty': renamed as 'Set-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="c16ab-863">PropertyId 매개 변수 이름을 NamedValueId로 변경.</span><span class="sxs-lookup"><span data-stu-id="c16ab-863">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="c16ab-864">'Remove-AzApiManagementProperty': 'Remove-AzApiManagementNamedValue'로 이름 변경.</span><span class="sxs-lookup"><span data-stu-id="c16ab-864">'Remove-AzApiManagementProperty': renamed as 'Remove-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="c16ab-865">PropertyId 매개 변수 이름을 NamedValueId로 변경.</span><span class="sxs-lookup"><span data-stu-id="c16ab-865">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="c16ab-866">새 'Get-AzApiManagementAuthorizationServerClientSecret' cmdlet이 추가되었으며 'Get-AzApiManagementAuthorizationServer'는 더 이상 클라이언트 암호를 반환하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-866">Added new 'Get-AzApiManagementAuthorizationServerClientSecret' cmdlet and 'Get-AzApiManagementAuthorizationServer' will not return client secret anymore.</span></span>
* <span data-ttu-id="c16ab-867">새 'Get-AzApiManagementNamedValueSecretValue' cmdlet이 추가되었으며 'Get-AzApiManagementNamedValue'는 더 이상 비밀 값을 반환하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-867">Added new 'Get-AzApiManagementNamedValueSecretValue' cmdlet and 'Get-AzApiManagementNamedValue' will not return secret value.</span></span>
* <span data-ttu-id="c16ab-868">새 'Get-AzApiManagementOpenIdConnectProviderClientSecret' cmdlet이 추가되었으며 'Get-AzApiManagementOpenIdConnectProvider'는 더 이상 클라이언트 암호를 반환하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-868">Added new 'Get-AzApiManagementOpenIdConnectProviderClientSecret' cmdlet and 'Get-AzApiManagementOpenIdConnectProvider' will not return client secret anymore.</span></span>
* <span data-ttu-id="c16ab-869">새 'Get-AzApiManagementSubscriptionKey' cmdlet이 추가되었으며 'Get-AzApiManagementSubscription'은 더 이상 구독 키를 반환하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-869">Added new 'Get-AzApiManagementSubscriptionKey' cmdlet and 'Get-AzApiManagementSubscription' will not return subscription keys anymore.</span></span>
* <span data-ttu-id="c16ab-870">새 'Get-AzApiManagementTenantAccessSecret' cmdlet이 추가되었으며 'Get-AzApiManagementTenantAccess'는 더 이상 키를 반환하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-870">Added new 'Get-AzApiManagementTenantAccessSecret' cmdlet and 'Get-AzApiManagementTenantAccess' will not return keys anymore.</span></span>
* <span data-ttu-id="c16ab-871">새 'Get-AzApiManagementTenantGitAccessSecret' cmdlet이 추가되었으며 'Get-AzApiManagementTenantGitAccess'는 더 이상 키를 반환하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-871">Added new 'Get-AzApiManagementTenantGitAccessSecret' cmdlet and 'Get-AzApiManagementTenantGitAccess' will not return keys anymore.</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="c16ab-872">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="c16ab-872">Az.ApplicationInsights</span></span>
* <span data-ttu-id="c16ab-873">매개 변수 추가: 'New-AzApplicationInsights'에 대한 'RetentionInDays' 'PublicNetworkAccessForIngestion' 'PublicNetworkAccessForQuery'</span><span class="sxs-lookup"><span data-stu-id="c16ab-873">Added Parameters: 'RetentionInDays' 'PublicNetworkAccessForIngestion' 'PublicNetworkAccessForQuery' for 'New-AzApplicationInsights'</span></span>
* <span data-ttu-id="c16ab-874">'Update-AzApplicationInsights' cmdlet 작성</span><span class="sxs-lookup"><span data-stu-id="c16ab-874">Created cmdlet 'Update-AzApplicationInsights'</span></span>
* <span data-ttu-id="c16ab-875">연결된 스토리지 계정에 대한 cmdlet 작성</span><span class="sxs-lookup"><span data-stu-id="c16ab-875">Created cmdlets for Linked Storage Account</span></span>

#### <a name="azbatch"></a><span data-ttu-id="c16ab-876">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="c16ab-876">Az.Batch</span></span>
* <span data-ttu-id="c16ab-877">'Microsoft.Azure.Batch' SDK 버전 13.0.0 및 'Microsoft.Azure.Management.Batch' SDK 버전 9.0.0을 사용하도록 Az.Batch가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-877">Updated Az.Batch to use 'Microsoft.Azure.Batch' SDK version 13.0.0 and 'Microsoft.Azure.Management.Batch' SDK version 9.0.0.</span></span>
* <span data-ttu-id="c16ab-878">새 '-CertificateKind' 매개 변수를 사용하여 'AzBatchCertificate'에 추가할 인증서 종류를 선택하는 기능이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-878">Added the ability to select the kind of certificate being added using the new '-CertificateKind' parameter to 'New-AzBatchCertificate'.</span></span>
* <span data-ttu-id="c16ab-879">이전에 항상 ''였던 'ApplicationPackages' 속성이 'PSApplication'에서 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-879">Removed 'ApplicationPackages' property from 'PSApplication' which was previously always ''.</span></span>
  - <span data-ttu-id="c16ab-880">이제 'Get-AzBatchApplicationPackage'를 사용하여 애플리케이션 내부의 특정 패키지를 검색할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-880">The specific packages inside of an application now can be retrieved using 'Get-AzBatchApplicationPackage'.</span></span> <span data-ttu-id="c16ab-881">예를 들면 다음과 같습니다. 'Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication'.</span><span class="sxs-lookup"><span data-stu-id="c16ab-881">For example: 'Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication'.</span></span>
* <span data-ttu-id="c16ab-882">'New-AzBatchPool'을 사용하여 풀을 만들 때 'PSImageReference'의 'VirtualMachineImageId' 속성은 이제 Shared Image Gallery 이미지만 참조할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-882">When creating a pool using 'New-AzBatchPool', the 'VirtualMachineImageId' property of 'PSImageReference' can now only refer to a Shared Image Gallery image.</span></span>
* <span data-ttu-id="c16ab-883">'New-AzBatchPool'을 사용하여 풀을 만들 때 공용 IP 없이 'PSNetworkConfiguration'의 새 'PublicIPAddressConfiguration'을 사용하여 풀을 프로비저닝할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-883">When creating a pool using 'New-AzBatchPool', the pool can be provisioned without a public IP using the new 'PublicIPAddressConfiguration' property of 'PSNetworkConfiguration'.</span></span>
  - <span data-ttu-id="c16ab-884">'PSNetworkConfiguration'의 'PublicIPs' 속성도 'PSPublicIPAddressConfiguration'으로 이동되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-884">The 'PublicIPs' property of 'PSNetworkConfiguration' has moved in to 'PSPublicIPAddressConfiguration' as well.</span></span> <span data-ttu-id="c16ab-885">이 속성은 'IPAddressProvisioningType'이 'UserManaged'인 경우에만 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-885">This property can only be specified if 'IPAddressProvisioningType' is 'UserManaged'.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="c16ab-886">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="c16ab-886">Az.Compute</span></span>
* <span data-ttu-id="c16ab-887">'Update-AzVM' cmdlet에 HostId 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="c16ab-887">Added HostId parameter to 'Update-AzVM' cmdlet</span></span>
* <span data-ttu-id="c16ab-888">'New-AzVMConfig', 'New-AzVmssConfig', 'Update-AzVmss', 'Set-AzVMOperatingSystem' 및 'Set-AzVmssOsProfile' cmdlet의 도움말 문서가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-888">Updated Help documents for 'New-AzVMConfig', 'New-AzVmssConfig', 'Update-AzVmss', 'Set-AzVMOperatingSystem' and 'Set-AzVmssOsProfile' cmdlets.</span></span>
* <span data-ttu-id="c16ab-889">주요 변경 내용</span><span class="sxs-lookup"><span data-stu-id="c16ab-889">Breaking changes</span></span>
    - <span data-ttu-id="c16ab-890">'Get-AzVMImage' cmdlet에서 FilterExpression 매개 변수가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-890">FilterExpression parameter is removed from 'Get-AzVMImage' cmdlet.</span></span>
    - <span data-ttu-id="c16ab-891">'New-AzVmssConfig', 'New-AzVMConfig' 및 'Update-AzVM' cmdlet에서 AssignIdentity 매개 변수가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-891">AssignIdentity parameter is removed from 'New-AzVmssConfig', 'New-AzVMConfig' and 'Update-AzVM' cmdlets.</span></span>
    - <span data-ttu-id="c16ab-892">'New-AzVmssConfig' 및 'Update-AzVmss' cmdlet에서 AutomaticRepairMaxInstanceRepairsPercent가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-892">AutomaticRepairMaxInstanceRepairsPercent is removed from 'New-AzVmssConfig' and 'Update-AzVmss' cmdlets.</span></span>
    - <span data-ttu-id="c16ab-893">ProximityPlacementGroup에서 AvailabilitySetsColocationStatus, VirtualMachinesColocationStatus 및 VirtualMachineScaleSetsColocationStatus 속성이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-893">AvailabilitySetsColocationStatus, VirtualMachinesColocationStatus and VirtualMachineScaleSetsColocationStatus properties are removed from ProximityPlacementGroup.</span></span>
    - <span data-ttu-id="c16ab-894">AutomaticRepairsPolicy에서 MaxInstanceRepairsPercent 속성이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-894">MaxInstanceRepairsPercent property is removed from AutomaticRepairsPolicy.</span></span>
    - <span data-ttu-id="c16ab-895">AvailabilitySets, VirtualMachines 및 VirtualMachineScaleSets 형식이 IList<SubResource>에서 IList<SubResourceWithColocationStatus>로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-895">The types of AvailabilitySets, VirtualMachines and VirtualMachineScaleSets are changed from IList<SubResource> to IList<SubResourceWithColocationStatus>.</span></span>
* <span data-ttu-id="c16ab-896">'Get-AzVM' cmdlet에 대한 설명이 보다 정확하게 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-896">Description for 'Get-AzVM' cmdlet has been updated to better describe it.</span></span> 

#### <a name="azdatafactory"></a><span data-ttu-id="c16ab-897">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="c16ab-897">Az.DataFactory</span></span>
* <span data-ttu-id="c16ab-898">Managed IR에서 데이터 흐름 런타임 속성의 CRUD를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-898">Supported CRUD of data flow runtime properties in Managed IR.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="c16ab-899">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="c16ab-899">Az.FrontDoor</span></span>
* <span data-ttu-id="c16ab-900">Front Door 규칙 엔진 개체를 생성, 업데이트, 검색 및 삭제할 수 있는 새 cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="c16ab-900">Added new cmdlets for creation, update, retreival, and deletion of Front Door Rules Engine object</span></span>
* <span data-ttu-id="c16ab-901">Front Door 규칙 엔진 개체를 작성할 수 있는 도우미 cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="c16ab-901">Added helper cmdlets for construction of Front Door Rules Engine object</span></span>
* <span data-ttu-id="c16ab-902">Front Door 회람 규칙 개체에 대한 규칙 엔진 참조 추가</span><span class="sxs-lookup"><span data-stu-id="c16ab-902">Added Rules Engine reference to Front Door Routing Rule object.</span></span>
* <span data-ttu-id="c16ab-903">Front Door 백 엔드 개체에 Private Link 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="c16ab-903">Added Private Link parameters to Front Door Backend object</span></span>

#### <a name="azfunctions"></a><span data-ttu-id="c16ab-904">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="c16ab-904">Az.Functions</span></span>
* <span data-ttu-id="c16ab-905">''Az.Functions'' 모듈의 일반 공급</span><span class="sxs-lookup"><span data-stu-id="c16ab-905">General availability of ''Az.Functions'' module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="c16ab-906">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="c16ab-906">Az.HDInsight</span></span>
* <span data-ttu-id="c16ab-907">고객 관리형 키 디스크 암호화 지원</span><span class="sxs-lookup"><span data-stu-id="c16ab-907">Supported Customer-managed key disk encryption.</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="c16ab-908">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="c16ab-908">Az.HealthcareApis</span></span>
* <span data-ttu-id="c16ab-909">더 이상 액세스 정책이 기본적으로 현재 보안 주체로 설정되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-909">Access policies are no longer defaulted to the current principal</span></span>

#### <a name="aziothub"></a><span data-ttu-id="c16ab-910">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="c16ab-910">Az.IotHub</span></span>
* <span data-ttu-id="c16ab-911">SQL과 비슷한 언어를 사용하여 정보를 검색하기 위해 IoT 허브에서 쿼리를 호출하는 cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-911">Added cmdlet to invoke a query in an IoT hub to retrieve information using a SQL-like language.</span></span>
* <span data-ttu-id="c16ab-912">'Add-AzIotHubDevice'가 자식 디바이스 없는 에지 지원 디바이스를 만들 수 없는 문제 해결 [#11597]</span><span class="sxs-lookup"><span data-stu-id="c16ab-912">Fix issue that 'Add-AzIotHubDevice' fails to create Edge Enabled Device without child devices [#11597]</span></span>
* <span data-ttu-id="c16ab-913">IoT Hub, 디바이스 또는 모듈에 대한 SAS 토큰을 생성하는 cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-913">Added cmdlet to generate SAS token for Iot Hub, device or module.</span></span>
* <span data-ttu-id="c16ab-914">구성 메트릭 쿼리를 호출하는 cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-914">Added cmdlet to invoke configuration metrics query.</span></span>
* <span data-ttu-id="c16ab-915">IoT Edge 자동 배포를 대규모로 관리합니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-915">Manage IoT Edge automatic deployment at scale.</span></span> <span data-ttu-id="c16ab-916">새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-916">New cmdlets are:</span></span>
    - <span data-ttu-id="c16ab-917">'Add-AzIotHubDeployment'</span><span class="sxs-lookup"><span data-stu-id="c16ab-917">'Add-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="c16ab-918">'Get-AzIotHubDeployment'</span><span class="sxs-lookup"><span data-stu-id="c16ab-918">'Get-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="c16ab-919">'Remove-AzIotHubDeployment'</span><span class="sxs-lookup"><span data-stu-id="c16ab-919">'Remove-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="c16ab-920">'Set-AzIotHubDeployment'</span><span class="sxs-lookup"><span data-stu-id="c16ab-920">'Set-AzIotHubDeployment'</span></span>
* <span data-ttu-id="c16ab-921">IoT Edge 배포 메트릭 쿼리를 호출하는 cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-921">Added cmdlet to invoke an IoT Edge deployment metrics query.</span></span>
* <span data-ttu-id="c16ab-922">지정된 에지 디바이스에 구성 콘텐츠를 적용하는 cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-922">Added cmdlet to apply the configuration content to the specified edge device.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="c16ab-923">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="c16ab-923">Az.KeyVault</span></span>
* <span data-ttu-id="c16ab-924">다음 별칭 제거: 'New-AzKeyVaultCertificateAdministratorDetails' 및 'New-AzKeyVaultCertificateOrganizationDetails'</span><span class="sxs-lookup"><span data-stu-id="c16ab-924">Removed two aliases: 'New-AzKeyVaultCertificateAdministratorDetails' and 'New-AzKeyVaultCertificateOrganizationDetails'</span></span>
* <span data-ttu-id="c16ab-925">키 자격 증명 모음을 만들 때 기본적으로 일시 삭제 사용</span><span class="sxs-lookup"><span data-stu-id="c16ab-925">Enabled soft delete by default when creating a key vault</span></span>
* <span data-ttu-id="c16ab-926">키 자격 증명 모음을 만들 때 특정 네트워크 위치의 액세스를 제어하도록 네트워크 규칙을 설정할 수 있음</span><span class="sxs-lookup"><span data-stu-id="c16ab-926">Network rules can be set to govern the accessibility from specific network locations when creating a key vault</span></span>
* <span data-ttu-id="c16ab-927">BYOK(Bring Your Own Key) 지원 추가</span><span class="sxs-lookup"><span data-stu-id="c16ab-927">Added support to bring your own key (BYOK)</span></span>
    - <span data-ttu-id="c16ab-928">'Add-AzKeyVaultKey'가 키 교환 키 생성 지원</span><span class="sxs-lookup"><span data-stu-id="c16ab-928">'Add-AzKeyVaultKey' supports generating a key exchange key</span></span>
    - <span data-ttu-id="c16ab-929">'Get-AzKeyVaultKey'가 PEM 형식의 공개 키 다운로드 지원</span><span class="sxs-lookup"><span data-stu-id="c16ab-929">'Get-AzKeyVaultKey' supports downloading a public key in PEM format</span></span>
* <span data-ttu-id="c16ab-930">'AzKeyVaultKey' 도움말 문서의 'KeyOps' 부분 업데이트</span><span class="sxs-lookup"><span data-stu-id="c16ab-930">Updated the 'KeyOps' part of the help document of 'Add-AzKeyVaultKey'</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="c16ab-931">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="c16ab-931">Az.Monitor</span></span>
* <span data-ttu-id="c16ab-932">'Set-AzDiagnosticSettings'의 버그 수정, 일부 범주에는 보존 정책이 적용되지 않음 [#11589]</span><span class="sxs-lookup"><span data-stu-id="c16ab-932">Fixed bug for 'Set-AzDiagnosticSettings', retention policy won't apply to all categories [#11589]</span></span>
* <span data-ttu-id="c16ab-933">메트릭 경고 V2에 WebTest를 사용하기 위한 조건 지원</span><span class="sxs-lookup"><span data-stu-id="c16ab-933">Supported WebTest availability criteria for metric alert V2</span></span>
    - <span data-ttu-id="c16ab-934">'New-AzMetricAlertRuleV2Criteria': webtest 사용 조건을 만드는 옵션 추가</span><span class="sxs-lookup"><span data-stu-id="c16ab-934">'New-AzMetricAlertRuleV2Criteria': an option to create webtest availability criteria was added</span></span>
    - <span data-ttu-id="c16ab-935">'Add-AzMetricAlertRuleV2': 새 webtest 사용 조건 지원</span><span class="sxs-lookup"><span data-stu-id="c16ab-935">'Add-AzMetricAlertRuleV2': supports the new webtest availability criteria</span></span>
* <span data-ttu-id="c16ab-936">PSLogProfile에서 RetentionPolicy에 대한 중복 정의 제거 [#7608]</span><span class="sxs-lookup"><span data-stu-id="c16ab-936">Removed redundant definition for RetentionPolicy in PSLogProfile [#7608]</span></span>
* <span data-ttu-id="c16ab-937">PSEventData에 정의된 중복 속성 제거 [#11353]</span><span class="sxs-lookup"><span data-stu-id="c16ab-937">Removed redundant properties difined in PSEventData [#11353]</span></span>
* <span data-ttu-id="c16ab-938">'Get-AzLog'를 'Get-AzActivityLog'로 이름 변경</span><span class="sxs-lookup"><span data-stu-id="c16ab-938">Renamed 'Get-AzLog' to 'Get-AzActivityLog'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="c16ab-939">Az.Network</span><span class="sxs-lookup"><span data-stu-id="c16ab-939">Az.Network</span></span>
* <span data-ttu-id="c16ab-940">영역 기본 동작이 변경된다는 것을 알리기 위해 주요 변경 특성을 추가</span><span class="sxs-lookup"><span data-stu-id="c16ab-940">Added breaking change attribute to notify that Zone default behaviour will be changed</span></span>
    - <span data-ttu-id="c16ab-941">'New-AzPublicIpAddress'</span><span class="sxs-lookup"><span data-stu-id="c16ab-941">'New-AzPublicIpAddress'</span></span>
    - <span data-ttu-id="c16ab-942">'New-AzPublicIpPrefix'</span><span class="sxs-lookup"><span data-stu-id="c16ab-942">'New-AzPublicIpPrefix'</span></span>
    - <span data-ttu-id="c16ab-943">'New-AzLoadBalancerFrontendIpConfig'</span><span class="sxs-lookup"><span data-stu-id="c16ab-943">'New-AzLoadBalancerFrontendIpConfig'</span></span>
* <span data-ttu-id="c16ab-944">새로운 최상위 리소스 SecurityPartnerProvider에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="c16ab-944">Added support for a new top level resource SecurityPartnerProvider</span></span>
    - <span data-ttu-id="c16ab-945">추가된 새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-945">New cmdlets added:</span></span>
        - <span data-ttu-id="c16ab-946">New-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="c16ab-946">New-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="c16ab-947">Remove-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="c16ab-947">Remove-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="c16ab-948">Get-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="c16ab-948">Get-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="c16ab-949">Set-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="c16ab-949">Set-AzSecurityPartnerProvider</span></span>
* <span data-ttu-id="c16ab-950">'PSPrivateEndpointConnection'의 'PSPrivateLinkResource' 및 'GroupId'에서 'RequiredZoneNames' 추가</span><span class="sxs-lookup"><span data-stu-id="c16ab-950">Added 'RequiredZoneNames' on 'PSPrivateLinkResource' and 'GroupId' on 'PSPrivateEndpointConnection'</span></span>
* <span data-ttu-id="c16ab-951">New-AzNetworkWatcherConnectionMonitorTestConfigurationObject에 대한 잘못된 형식의 SuccessThresholdRoundTripTimeMs 매개 변수 수정</span><span class="sxs-lookup"><span data-stu-id="c16ab-951">Fixed incorrect type of SuccessThresholdRoundTripTimeMs parameter for New-AzNetworkWatcherConnectionMonitorTestConfigurationObject</span></span>
* <span data-ttu-id="c16ab-952">AllowVnetToVnetTraffic 인수의 기본값을 True로 설정하도록 VirtualWan cmdlet 업데이트</span><span class="sxs-lookup"><span data-stu-id="c16ab-952">Updated VirtualWan cmdlets to set default value of AllowVnetToVnetTraffic argument to True.</span></span>
    - <span data-ttu-id="c16ab-953">'New-AzVirtualWan'</span><span class="sxs-lookup"><span data-stu-id="c16ab-953">'New-AzVirtualWan'</span></span>
    - <span data-ttu-id="c16ab-954">'Update-AzVirtualWan'</span><span class="sxs-lookup"><span data-stu-id="c16ab-954">'Update-AzVirtualWan'</span></span>
* <span data-ttu-id="c16ab-955">프라이빗 엔드포인트에 대한 DNS 영역 그룹을 지원하는 새 cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="c16ab-955">Added new cmdlets to support DNS zone group for private endpoint</span></span>
    - <span data-ttu-id="c16ab-956">'New-AzPrivateDnsZoneConfig'</span><span class="sxs-lookup"><span data-stu-id="c16ab-956">'New-AzPrivateDnsZoneConfig'</span></span>
    - <span data-ttu-id="c16ab-957">'Get-AzPrivateDnsZoneGroup'</span><span class="sxs-lookup"><span data-stu-id="c16ab-957">'Get-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="c16ab-958">'New-AzPrivateDnsZoneGroup'</span><span class="sxs-lookup"><span data-stu-id="c16ab-958">'New-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="c16ab-959">'Set-AzPrivateDnsZoneGroup'</span><span class="sxs-lookup"><span data-stu-id="c16ab-959">'Set-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="c16ab-960">'Remove-AzPrivateDnsZoneGroup'</span><span class="sxs-lookup"><span data-stu-id="c16ab-960">'Remove-AzPrivateDnsZoneGroup'</span></span>
* <span data-ttu-id="c16ab-961">'AzureFirewall'에 'DNSEnableProxy', 'DNSRequireProxyForNetworkRules' 및 'DNSServers' 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="c16ab-961">Added 'DNSEnableProxy', 'DNSRequireProxyForNetworkRules' and 'DNSServers' parameters to 'AzureFirewall'</span></span>
* <span data-ttu-id="c16ab-962">'AzureFirewall'에 'EnableDnsProxy', 'DnsProxyNotRequiredForNetworkRule' 및 'DnsServer' 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="c16ab-962">Added 'EnableDnsProxy', 'DnsProxyNotRequiredForNetworkRule' and 'DnsServer' parameters to 'AzureFirewall'</span></span>
    - <span data-ttu-id="c16ab-963">업데이트된 cmdlet:</span><span class="sxs-lookup"><span data-stu-id="c16ab-963">Updated cmdlet:</span></span>
        - <span data-ttu-id="c16ab-964">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="c16ab-964">New-AzFirewall</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="c16ab-965">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="c16ab-965">Az.OperationalInsights</span></span>
* <span data-ttu-id="c16ab-966">새로 생성된 SDK를 적용하도록 레거시 코드 업데이트</span><span class="sxs-lookup"><span data-stu-id="c16ab-966">Updated legacy code to apply new generated SDK</span></span>
* <span data-ttu-id="c16ab-967">사용되지 않는 API 때문에 cmdlet 삭제</span><span class="sxs-lookup"><span data-stu-id="c16ab-967">Deleted cmdlets due to deprecated APIs</span></span>
    - <span data-ttu-id="c16ab-968">'Get-AzOperationalInsightsSavedSearchResult'(별칭 'Get-AzOperationalInsightsSavedSearchResults')</span><span class="sxs-lookup"><span data-stu-id="c16ab-968">'Get-AzOperationalInsightsSavedSearchResult' (alias 'Get-AzOperationalInsightsSavedSearchResults')</span></span>
    - <span data-ttu-id="c16ab-969">'Get-AzOperationalInsightsSearchResult'(별칭 'Get-AzOperationalInsightsSearchResults')</span><span class="sxs-lookup"><span data-stu-id="c16ab-969">'Get-AzOperationalInsightsSearchResult' (alias 'Get-AzOperationalInsightsSearchResults')</span></span>
    - <span data-ttu-id="c16ab-970">'Get-AzOperationalInsightsLinkTarget'(별칭 'Get-AzOperationalInsightsLinkTargets')</span><span class="sxs-lookup"><span data-stu-id="c16ab-970">'Get-AzOperationalInsightsLinkTarget' (alias 'Get-AzOperationalInsightsLinkTargets')</span></span>
* <span data-ttu-id="c16ab-971">'Set-AzOperationalInsightsWorkspace' 및 'New-AzOperationalInsightsWorkspace'에 대한 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="c16ab-971">Added parameters for 'Set-AzOperationalInsightsWorkspace' and 'New-AzOperationalInsightsWorkspace'</span></span>
* <span data-ttu-id="c16ab-972">연결된 스토리지 계정에 대한 cmdlet 작성</span><span class="sxs-lookup"><span data-stu-id="c16ab-972">Created cmdlets for Linked Stoarge Account</span></span>
* <span data-ttu-id="c16ab-973">클러스터 및 연결된 서비스에 대한 cmdlet 작성</span><span class="sxs-lookup"><span data-stu-id="c16ab-973">Created cmdlets for Clusters and Linked Service</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="c16ab-974">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="c16ab-974">Az.RecoveryServices</span></span>
* <span data-ttu-id="c16ab-975">Azure Site Recovery - Azure와 Azure 공급자 간 근접 배치 그룹 가상 머신을 보호하기 위한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-975">Azure Site Recovery added support for protecting proximity placement group virtual machines for Azure to Azure provider.</span></span>
* <span data-ttu-id="c16ab-976">Azure Site Recovery - 영역 간 복제에 대한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-976">Azure Site Recovery added support for zone to zone replication.</span></span>
* <span data-ttu-id="c16ab-977">Azure Backup - Azure 파일 공유 복구 지점의 장기 보존 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-977">Azure Backup Added Long term retention support for Azure FileShare Recovery Points.</span></span>
* <span data-ttu-id="c16ab-978">Azure Backup - 'Get-AzRecoveryServicesBackupItem' cmdlet 출력에 디스크 제외 속성이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-978">Azure Backup Added disk exclusion properties to 'Get-AzRecoveryServicesBackupItem' cmdlet output.</span></span>
* <span data-ttu-id="c16ab-979">사이트 복구 서비스용 Vault 자격 증명 파일에 대한 프라이빗 엔드포인트가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-979">Added private endpoint for Vault credential file for site recovery service.</span></span>

#### <a name="azresources"></a><span data-ttu-id="c16ab-980">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="c16ab-980">Az.Resources</span></span>
* <span data-ttu-id="c16ab-981">새 역할 정의를 만들 때 보기 지연에 대한 메시지 경고 추가</span><span class="sxs-lookup"><span data-stu-id="c16ab-981">Added message warning about view delay when creating a new Role Definition</span></span>
* <span data-ttu-id="c16ab-982">강력한 형식의 개체를 출력하도록 정책 cmdlet 변경</span><span class="sxs-lookup"><span data-stu-id="c16ab-982">Changed policy cmdlets to output strongly-typed objects</span></span>
* <span data-ttu-id="c16ab-983">'Get-AzResourceLock' cmdlet에 사용되는 '-TenantLevel' 매개 변수 제거 [#11335]</span><span class="sxs-lookup"><span data-stu-id="c16ab-983">Removed '-TenantLevel' parameter used for on the 'Get-AzResourceLock' cmdlet [#11335]</span></span>
* <span data-ttu-id="c16ab-984">'Remove-AzResourceGroup -Id ResourceId' 수정[#9882]</span><span class="sxs-lookup"><span data-stu-id="c16ab-984">Fixed 'Remove-AzResourceGroup -Id ResourceId'[#9882]</span></span>
* <span data-ttu-id="c16ab-985">리소스 그룹 범위에서 ARM 템플릿 가상 시나리오 결과를 가져오는 새 cmdlet 추가: 'Get-AzDeploymentResourceGroupWhatIfResult'</span><span class="sxs-lookup"><span data-stu-id="c16ab-985">Added new cmdlet for getting ARM template What-If results at resource group scope: 'Get-AzDeploymentResourceGroupWhatIfResult'</span></span>
* <span data-ttu-id="c16ab-986">구독 범위에서 ARM 템플릿 가상 시나리오 결과를 가져오는 새 cmdlet 추가: 'Get-AzDeploymentWhatIfResult'</span><span class="sxs-lookup"><span data-stu-id="c16ab-986">Added new cmdlet for getting ARM template What-If results at subscription scope: 'Get-AzDeploymentWhatIfResult'</span></span>
   - <span data-ttu-id="c16ab-987">별칭: 'Get-AzSubscriptionDeploymentWhatIf'</span><span class="sxs-lookup"><span data-stu-id="c16ab-987">Alias: 'Get-AzSubscriptionDeploymentWhatIf'</span></span>
* <span data-ttu-id="c16ab-988">ARM 템플릿 가상 시나리오 결과를 사용하도록 'New-AzDeployment' 및 'New-AzResourceGroupDeployment'에 대한 '-WhatIf' 및 '-Confirm' 매개 변수 재정의</span><span class="sxs-lookup"><span data-stu-id="c16ab-988">Overrode '-WhatIf' and '-Confirm' parameters for 'New-AzDeployment' and 'New-AzResourceGroupDeployment' to use ARM template What-If results</span></span>
* <span data-ttu-id="c16ab-989">배포 cmdlet에서 'ApiVersion' 매개 변수의 사용 중단 메시지 추가</span><span class="sxs-lookup"><span data-stu-id="c16ab-989">Added deprecation message for 'ApiVersion' parameter in deployment cmdlets</span></span>
* <span data-ttu-id="c16ab-990">배포 오류에 대한 향상된 오류 메시지를 표시하는 기능 추가</span><span class="sxs-lookup"><span data-stu-id="c16ab-990">Added capability to show improved error messages for deployment failures</span></span>
* <span data-ttu-id="c16ab-991">배포 오류에 대한 correlationId 로깅 추가</span><span class="sxs-lookup"><span data-stu-id="c16ab-991">Added correlationId logging for deployment failures</span></span>
* <span data-ttu-id="c16ab-992">배포 스크립트 출력에 'error' 속성 추가</span><span class="sxs-lookup"><span data-stu-id="c16ab-992">Added 'error' property to the deployment script output</span></span>
* <span data-ttu-id="c16ab-993">nuget Microsoft.Azure.Management.ResourceManager를 '3.7.1-preview'로 업데이트</span><span class="sxs-lookup"><span data-stu-id="c16ab-993">Updated nuget Microsoft.Azure.Management.ResourceManager to '3.7.1-preview'</span></span>
* <span data-ttu-id="c16ab-994">nuget 3.7.1-preview에서 DeploymentValidateResult의 Error 속성이 readonly로 변경되어 특정 테스트 사례를 제거</span><span class="sxs-lookup"><span data-stu-id="c16ab-994">Removed specific test cases as Error property in DeploymentValidateResult has changed to readonly from nuget 3.7.1-preview</span></span>
* <span data-ttu-id="c16ab-995">SDK ResourceManager 3.7.1-preview의 GenericResourceExpanded 도입</span><span class="sxs-lookup"><span data-stu-id="c16ab-995">Brought GenericResourceExpanded from SDK ResourceManager 3.7.1-preview</span></span>
* <span data-ttu-id="c16ab-996">모든 배포용 Get cmdlet에 대한 태그 지원 추가</span><span class="sxs-lookup"><span data-stu-id="c16ab-996">Added tag support for all Get cmdlets for deployment, as well as</span></span>
    - <span data-ttu-id="c16ab-997">'New-AzDeployment'</span><span class="sxs-lookup"><span data-stu-id="c16ab-997">'New-AzDeployment'</span></span>
    - <span data-ttu-id="c16ab-998">'New-AzManagementGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="c16ab-998">'New-AzManagementGroupDeployment'</span></span>
    - <span data-ttu-id="c16ab-999">'New-AzResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="c16ab-999">'New-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="c16ab-1000">'New-AzTenantDeployment'</span><span class="sxs-lookup"><span data-stu-id="c16ab-1000">'New-AzTenantDeployment'</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="c16ab-1001">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="c16ab-1001">Az.ServiceFabric</span></span>
* <span data-ttu-id="c16ab-1002">잘못된 인증서 지문을 가져오는 --SecretIdentifier를 사용한 인증서 추가의 버그 수정</span><span class="sxs-lookup"><span data-stu-id="c16ab-1002">Fixed bug in add certificate using --SecretIdentifier that was getting the wrong certificate thumbprint</span></span>

#### <a name="azsql"></a><span data-ttu-id="c16ab-1003">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="c16ab-1003">Az.Sql</span></span>
* <span data-ttu-id="c16ab-1004">성능 강화:</span><span class="sxs-lookup"><span data-stu-id="c16ab-1004">Enhance performance of:</span></span>
    - <span data-ttu-id="c16ab-1005">'Set-AzSqlDatabaseSensitivityClassification'</span><span class="sxs-lookup"><span data-stu-id="c16ab-1005">'Set-AzSqlDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="c16ab-1006">'Set-AzSqlInstanceDatabaseSensitivityClassification'</span><span class="sxs-lookup"><span data-stu-id="c16ab-1006">'Set-AzSqlInstanceDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="c16ab-1007">'Remove-AzSqlDatabaseSensitivityClassification'</span><span class="sxs-lookup"><span data-stu-id="c16ab-1007">'Remove-AzSqlDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="c16ab-1008">'Remove-AzSqlInstanceDatabaseSensitivityClassification'</span><span class="sxs-lookup"><span data-stu-id="c16ab-1008">'Remove-AzSqlInstanceDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="c16ab-1009">'Enable-AzSqlDatabaseSensitivityRecommendation'</span><span class="sxs-lookup"><span data-stu-id="c16ab-1009">'Enable-AzSqlDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="c16ab-1010">'Enable-AzSqlInstanceDatabaseSensitivityRecommendation'</span><span class="sxs-lookup"><span data-stu-id="c16ab-1010">'Enable-AzSqlInstanceDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="c16ab-1011">'Disable-AzSqlDatabaseSensitivityRecommendation'</span><span class="sxs-lookup"><span data-stu-id="c16ab-1011">'Disable-AzSqlDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="c16ab-1012">'Disable-AzSqlInstanceDatabaseSensitivityRecommendation'</span><span class="sxs-lookup"><span data-stu-id="c16ab-1012">'Disable-AzSqlInstanceDatabaseSensitivityRecommendation'</span></span>
* <span data-ttu-id="c16ab-1013">'Set-AzSqlDatabaseBackupShortTermRetentionPolicy' cmdlet에서 'RetentionDays' 매개 변수의 클라이언트 쪽 유효성 검사 제거</span><span class="sxs-lookup"><span data-stu-id="c16ab-1013">Removed client-side validation of 'RetentionDays' parameter from cmdlet 'Set-AzSqlDatabaseBackupShortTermRetentionPolicy'</span></span>
* <span data-ttu-id="c16ab-1014">Vnet에서 스토리지 계정을 감사하고, Storage Blob 데이터 기여자 역할을 만들 때 발생하는 버그 수정</span><span class="sxs-lookup"><span data-stu-id="c16ab-1014">Auditing to a storage account in Vnet, fixing a bug when creating a Storage Blob Data Contributor role.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="c16ab-1015">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="c16ab-1015">Az.Storage</span></span>
* <span data-ttu-id="c16ab-1016">get/list account cmdlet 'Get-AzStorageAccount'에 '-AsJob' 추가</span><span class="sxs-lookup"><span data-stu-id="c16ab-1016">Added '-AsJob' to get/list account cmdlet 'Get-AzStorageAccount'</span></span>
* <span data-ttu-id="c16ab-1017">키 자동 회전을 지원하기 위해 스토리지 계정을 KeyvaultEncryption으로 업데이트할 때 KeyVersion을 선택 사항으로 지정</span><span class="sxs-lookup"><span data-stu-id="c16ab-1017">Make KeyVersion to optional when update Storage account with KeyvaultEncryption, to support key auto-rotation</span></span>
    - <span data-ttu-id="c16ab-1018">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="c16ab-1018">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="c16ab-1019">파이프라인을 사용하여 Azure 파일 디렉터리 제거 오류 수정</span><span class="sxs-lookup"><span data-stu-id="c16ab-1019">Fixed remove Azure File Directory fail with pipeline</span></span>
    - <span data-ttu-id="c16ab-1020">'Remove-AzStorageDirectory'</span><span class="sxs-lookup"><span data-stu-id="c16ab-1020">'Remove-AzStorageDirectory'</span></span>
* <span data-ttu-id="c16ab-1021">수정 [#9880]: Swagger에 맞게 NetWorkRule DefaultAction 값 정의 변경</span><span class="sxs-lookup"><span data-stu-id="c16ab-1021">Fixed [#9880]: Change NetWorkRule DefaultAction value defination to align with swagger.</span></span>
    - <span data-ttu-id="c16ab-1022">'Update-AzStorageAccountNetworkRuleSet'</span><span class="sxs-lookup"><span data-stu-id="c16ab-1022">'Update-AzStorageAccountNetworkRuleSet'</span></span>
    - <span data-ttu-id="c16ab-1023">'Get-AzStorageAccountNetworkRuleSet'</span><span class="sxs-lookup"><span data-stu-id="c16ab-1023">'Get-AzStorageAccountNetworkRuleSet'</span></span>
* <span data-ttu-id="c16ab-1024">수정 [#11624]: 서버 오류를 방지하기 위해 NetworkRules를 추가할 때 중복 규칙 건너뛰기</span><span class="sxs-lookup"><span data-stu-id="c16ab-1024">Fixed [#11624]: Skip duplicated rules when add NetworkRules, to avoid server failure</span></span>
    - <span data-ttu-id="c16ab-1025">'Add-AzStorageAccountNetworkRule'</span><span class="sxs-lookup"><span data-stu-id="c16ab-1025">'Add-AzStorageAccountNetworkRule'</span></span>
* <span data-ttu-id="c16ab-1026">Microsoft.Azure.Cosmos.Table SDK를 1.0.7로 업그레이드</span><span class="sxs-lookup"><span data-stu-id="c16ab-1026">Upgraded Microsoft.Azure.Cosmos.Table SDK to 1.0.7</span></span>
* <span data-ttu-id="c16ab-1027">DataLake Gen2 항목 목록에 부품 항목만 반환되는 경우 ContinuationToken을 사용하여 다시 나열하라고 사용자에게 알리는 경고 메시지 추가</span><span class="sxs-lookup"><span data-stu-id="c16ab-1027">Added a warning message to remind user to list again with ContinuationToken when only part items are returned in list DataLake Gen2 Items,</span></span>
    - <span data-ttu-id="c16ab-1028">'Get-AzDataLakeGen2ChildItem'</span><span class="sxs-lookup"><span data-stu-id="c16ab-1028">'Get-AzDataLakeGen2ChildItem'</span></span>
* <span data-ttu-id="c16ab-1029">Azure Files Active Directory 도메인 서비스 인증을 사용하여 스토리지 계정을 만들거나 업데이트하는 기능 지원</span><span class="sxs-lookup"><span data-stu-id="c16ab-1029">Supported to create or update Storage account with Azure Files Active Directory Domain Service Authentication</span></span>
    -  <span data-ttu-id="c16ab-1030">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="c16ab-1030">'New-AzStorageAccount'</span></span>
    -  <span data-ttu-id="c16ab-1031">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="c16ab-1031">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="c16ab-1032">스토리지 계정의 Kerberos 키 새로 만들기 또는 나열 지원</span><span class="sxs-lookup"><span data-stu-id="c16ab-1032">Supported to new or list Kerberos keys of Storage account</span></span>
    -  <span data-ttu-id="c16ab-1033">'New-AzStorageAccountKey'</span><span class="sxs-lookup"><span data-stu-id="c16ab-1033">'New-AzStorageAccountKey'</span></span>
    -  <span data-ttu-id="c16ab-1034">'Get-AzStorageAccountKey'</span><span class="sxs-lookup"><span data-stu-id="c16ab-1034">'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="c16ab-1035">스토리지 계정 장애 조치(failover) 지원</span><span class="sxs-lookup"><span data-stu-id="c16ab-1035">Supported failover Storage account</span></span>
    - <span data-ttu-id="c16ab-1036">'Invoke-AzStorageAccountFailover'</span><span class="sxs-lookup"><span data-stu-id="c16ab-1036">'Invoke-AzStorageAccountFailover'</span></span>
* <span data-ttu-id="c16ab-1037">'Get-AzStorageBlobCopyState'의 도움말 업데이트</span><span class="sxs-lookup"><span data-stu-id="c16ab-1037">Updated help of 'Get-AzStorageBlobCopyState'</span></span>
* <span data-ttu-id="c16ab-1038">'Get-AzStorageFileCopyState' 및 'Start-AzStorageBlobCopy'의 도움말 업데이트</span><span class="sxs-lookup"><span data-stu-id="c16ab-1038">Updated help of 'Get-AzStorageFileCopyState' and 'Start-AzStorageBlobCopy'</span></span>
* <span data-ttu-id="c16ab-1039">스토리지 클라이언트 라이브러리 v12를 큐 및 파일 cmdlet에 통합</span><span class="sxs-lookup"><span data-stu-id="c16ab-1039">Integrated Storage client library v12 to Queue and File cmdlets</span></span>
* <span data-ttu-id="c16ab-1040">출력 형식을 CloudFile에서 AzureStorageFile로 변경했으며, 원래 출력은 새 출력의 자식 속성이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1040">Changed output type from CloudFile to AzureStorageFile, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="c16ab-1041">'Get-AzStorageFile'</span><span class="sxs-lookup"><span data-stu-id="c16ab-1041">'Get-AzStorageFile'</span></span>
    - <span data-ttu-id="c16ab-1042">'Remove-AzStorageFile'</span><span class="sxs-lookup"><span data-stu-id="c16ab-1042">'Remove-AzStorageFile'</span></span>
    - <span data-ttu-id="c16ab-1043">'Get-AzStorageFileContent'</span><span class="sxs-lookup"><span data-stu-id="c16ab-1043">'Get-AzStorageFileContent'</span></span>
    - <span data-ttu-id="c16ab-1044">'Set-AzStorageFileContent'</span><span class="sxs-lookup"><span data-stu-id="c16ab-1044">'Set-AzStorageFileContent'</span></span>
    - <span data-ttu-id="c16ab-1045">'Start-AzStorageFileCopy'</span><span class="sxs-lookup"><span data-stu-id="c16ab-1045">'Start-AzStorageFileCopy'</span></span>
* <span data-ttu-id="c16ab-1046">출력 형식을 CloudFileDirectory에서 AzureStorageFileDirectory로 변경했으며, 원래 출력은 새 출력의 자식 속성이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1046">Changed output type from CloudFileDirectory to AzureStorageFileDirectory, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="c16ab-1047">'New-AzStorageDirectory'</span><span class="sxs-lookup"><span data-stu-id="c16ab-1047">'New-AzStorageDirectory'</span></span>
    - <span data-ttu-id="c16ab-1048">'Remove-AzStorageDirectory'</span><span class="sxs-lookup"><span data-stu-id="c16ab-1048">'Remove-AzStorageDirectory'</span></span>
* <span data-ttu-id="c16ab-1049">출력 형식을 CloudFileShare에서 AzureStorageFileShare로 변경했으며, 원래 출력은 새 출력의 자식 속성이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1049">Changed output type from CloudFileShare to AzureStorageFileShare, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="c16ab-1050">'Get-AzStorageShare'</span><span class="sxs-lookup"><span data-stu-id="c16ab-1050">'Get-AzStorageShare'</span></span>
    - <span data-ttu-id="c16ab-1051">'New-AzStorageShare'</span><span class="sxs-lookup"><span data-stu-id="c16ab-1051">'New-AzStorageShare'</span></span>
    - <span data-ttu-id="c16ab-1052">'Remove-AzStorageShare'</span><span class="sxs-lookup"><span data-stu-id="c16ab-1052">'Remove-AzStorageShare'</span></span>
* <span data-ttu-id="c16ab-1053">출력 형식을 FileShareProperties에서 AzureStorageFileShare로 변경했으며, 원래 출력은 새 출력의 하위 자식 속성이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1053">Changed output type from FileShareProperties to AzureStorageFileShare, the original output will become a sub child property of the new output</span></span>
    - <span data-ttu-id="c16ab-1054">'Set-AzStorageShareQuota'</span><span class="sxs-lookup"><span data-stu-id="c16ab-1054">'Set-AzStorageShareQuota'</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="c16ab-1055">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="c16ab-1055">Az.TrafficManager</span></span>
* <span data-ttu-id="c16ab-1056">'DisableAzureTrafficManagerEndpoint' 자세한 정보 출력에서 잘못된 프로필 이름 수정</span><span class="sxs-lookup"><span data-stu-id="c16ab-1056">Fixed incorrect profile name in 'DisableAzureTrafficManagerEndpoint' verbose output</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="c16ab-1057">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="c16ab-1057">Az.Websites</span></span>
* <span data-ttu-id="c16ab-1058">'Update-AzWebAppAccessRestrictionConfig'의 도움말에서 철자 오류 수정</span><span class="sxs-lookup"><span data-stu-id="c16ab-1058">Fixed typo on help of 'Update-AzWebAppAccessRestrictionConfig'.</span></span>

## <a name="380---april-2020"></a><span data-ttu-id="c16ab-1059">3.8.0 - 2020년 4월</span><span class="sxs-lookup"><span data-stu-id="c16ab-1059">3.8.0 - April 2020</span></span>
### <a name="highlights-since-the-last-release"></a><span data-ttu-id="c16ab-1060">마지막 릴리스 이후의 주요 사항</span><span class="sxs-lookup"><span data-stu-id="c16ab-1060">Highlights since the last release</span></span>
* <span data-ttu-id="c16ab-1061">Az.Storage에서 지원하는 PowerShell 버전: Windows PowerShell 5.1, PowerShell Core 6.2.4 이상, PowerShell 7</span><span class="sxs-lookup"><span data-stu-id="c16ab-1061">PowerShell versions that Az.Storage supports: Windows PowerShell 5.1, PowerShell Core 6.2.4+, PowerShell 7</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="c16ab-1062">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="c16ab-1062">Az.Accounts</span></span>
* <span data-ttu-id="c16ab-1063">'Resolve-AzError'에서 Azure PowerShell 설문 조사 URL이 업데이트되었습니다. [#11507]</span><span class="sxs-lookup"><span data-stu-id="c16ab-1063">Updated Azure PowerShell survey URL in 'Resolve-AzError' [#11507]</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="c16ab-1064">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="c16ab-1064">Az.ApiManagement</span></span>
* <span data-ttu-id="c16ab-1065">향후 릴리스의 Azure File cmdlet 출력 변경에 대한 호환성이 손상되는 변경 공지가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1065">Added breaking change notice for Azure File cmdlets output change in a future release</span></span>
* <span data-ttu-id="c16ab-1066">'Set-AzApiManagementGroup' - GroupId 매개 변수를 지정하도록 설명서가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1066">'Set-AzApiManagementGroup' Updated documentation to specify the GroupId parameter</span></span>

#### <a name="azcdn"></a><span data-ttu-id="c16ab-1067">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="c16ab-1067">Az.Cdn</span></span>
* <span data-ttu-id="c16ab-1068">ChinaCDN 관련 가격 책정 SKU 표시가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1068">Fixed ChinaCDN related pricing SKU display</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="c16ab-1069">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="c16ab-1069">Az.CognitiveServices</span></span>
* <span data-ttu-id="c16ab-1070">Identity, Encryption, UserOwnedStorage가 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1070">Supported Identity, Encryption, UserOwnedStorage</span></span>

#### <a name="azcompute"></a><span data-ttu-id="c16ab-1071">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="c16ab-1071">Az.Compute</span></span>
* <span data-ttu-id="c16ab-1072">'Set-AzVmssOrchestrationServiceState' cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1072">Added 'Set-AzVmssOrchestrationServiceState' cmdlet.</span></span>
* <span data-ttu-id="c16ab-1073">-InstanceView가 있는 'Get-AzVmss'는 OrchestrationService 상태를 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1073">'Get-AzVmss' with -InstanceView shows OrchestrationService states.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="c16ab-1074">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="c16ab-1074">Az.IotHub</span></span>
* <span data-ttu-id="c16ab-1075">IoT 디바이스 쌍 구성을 관리합니다. 새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1075">Manage IoT device twin configuration, New cmdlets are:</span></span>
    - <span data-ttu-id="c16ab-1076">'Get-AzIotHubDeviceTwin'</span><span class="sxs-lookup"><span data-stu-id="c16ab-1076">'Get-AzIotHubDeviceTwin'</span></span>
    - <span data-ttu-id="c16ab-1077">'Update-AzIotHubDeviceTwin'</span><span class="sxs-lookup"><span data-stu-id="c16ab-1077">'Update-AzIotHubDeviceTwin'</span></span>
* <span data-ttu-id="c16ab-1078">IoT Hub에서 디바이스에 대한 직접 메서드를 호출하는 cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1078">Added cmdlet to invoke direct method on a device in an Iot Hub.</span></span>
* <span data-ttu-id="c16ab-1079">IoT 디바이스 모듈 쌍 구성을 관리합니다. 새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1079">Manage IoT device module twin configuration, New cmdlets are:</span></span>
    - <span data-ttu-id="c16ab-1080">'Get-AzIotHubModuleTwin'</span><span class="sxs-lookup"><span data-stu-id="c16ab-1080">'Get-AzIotHubModuleTwin'</span></span>
    - <span data-ttu-id="c16ab-1081">'Update-AzIotHubModuleTwin'</span><span class="sxs-lookup"><span data-stu-id="c16ab-1081">'Update-AzIotHubModuleTwin'</span></span>
* <span data-ttu-id="c16ab-1082">IoT 자동 디바이스 관리 구성을 대규모로 관리합니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1082">Manage IoT automatic device management configuration at scale.</span></span> <span data-ttu-id="c16ab-1083">새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1083">New cmdlets are:</span></span>
    - <span data-ttu-id="c16ab-1084">'Add-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="c16ab-1084">'Add-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="c16ab-1085">'Get-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="c16ab-1085">'Get-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="c16ab-1086">'Remove-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="c16ab-1086">'Remove-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="c16ab-1087">'Set-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="c16ab-1087">'Set-AzIotHubConfiguration'</span></span>
* <span data-ttu-id="c16ab-1088">Iot Hub에서 에지 모듈 메서드를 호출하는 cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1088">Added cmdlet to invoke an edge module method in an Iot Hub.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="c16ab-1089">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="c16ab-1089">Az.KeyVault</span></span>
* <span data-ttu-id="c16ab-1090">자격 증명 모음에서 일시 삭제 및 제거 보호를 사용하도록 설정할 수 있는 새 cmdlet 'Update-AzKeyVault'가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1090">Added a new cmdlet 'Update-AzKeyVault' that can enable soft delete and purge protection on a vault</span></span>
* <span data-ttu-id="c16ab-1091">Microsoft.PowerShell.SecretManagement에 대한 지원이 추가되었습니다. [#11178]</span><span class="sxs-lookup"><span data-stu-id="c16ab-1091">Added support to Microsoft.PowerShell.SecretManagement [#11178]</span></span>
* <span data-ttu-id="c16ab-1092">'Remove-AzKeyVaultManagedStorageSasDefinition' 예제의 오류가 해결되었습니다. [#11479]</span><span class="sxs-lookup"><span data-stu-id="c16ab-1092">Fixed error in the examples of 'Remove-AzKeyVaultManagedStorageSasDefinition' [#11479]</span></span>
* <span data-ttu-id="c16ab-1093">프라이빗 엔드포인트에 대한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1093">Added support to private endpoint</span></span>

#### <a name="azmaintenance"></a><span data-ttu-id="c16ab-1094">Az.Maintenance</span><span class="sxs-lookup"><span data-stu-id="c16ab-1094">Az.Maintenance</span></span>
* <span data-ttu-id="c16ab-1095">GA용 유지 관리 cmdlet의 릴리스 버전 게시</span><span class="sxs-lookup"><span data-stu-id="c16ab-1095">Publishing release version of Maintenance cmdlets for GA</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="c16ab-1096">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="c16ab-1096">Az.Monitor</span></span>
* <span data-ttu-id="c16ab-1097">프라이빗 링크 범위용 cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1097">Added cmdlets for private link scope</span></span>
    - <span data-ttu-id="c16ab-1098">'Get-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="c16ab-1098">'Get-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="c16ab-1099">'Remove-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="c16ab-1099">'Remove-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="c16ab-1100">'New-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="c16ab-1100">'New-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="c16ab-1101">'Update-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="c16ab-1101">'Update-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="c16ab-1102">'Get-AzInsightsPrivateLinkScopedResource'</span><span class="sxs-lookup"><span data-stu-id="c16ab-1102">'Get-AzInsightsPrivateLinkScopedResource'</span></span>
    - <span data-ttu-id="c16ab-1103">'New-AzInsightsPrivateLinkScopedResource'</span><span class="sxs-lookup"><span data-stu-id="c16ab-1103">'New-AzInsightsPrivateLinkScopedResource'</span></span>
    - <span data-ttu-id="c16ab-1104">'Remove-AzInsightsPrivateLinkScopedResource'</span><span class="sxs-lookup"><span data-stu-id="c16ab-1104">'Remove-AzInsightsPrivateLinkScopedResource'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="c16ab-1105">Az.Network</span><span class="sxs-lookup"><span data-stu-id="c16ab-1105">Az.Network</span></span>
* <span data-ttu-id="c16ab-1106">Virtual Network 게이트웨이의 개인 IP에 대한 연결을 사용하도록 설정하는 cmdlet이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1106">Updated cmdlets to enable connection on private IP for Virtual Network Gateway.</span></span>
    - <span data-ttu-id="c16ab-1107">'New-AzVirtualNetworkGateway'</span><span class="sxs-lookup"><span data-stu-id="c16ab-1107">'New-AzVirtualNetworkGateway'</span></span>
    - <span data-ttu-id="c16ab-1108">'Set-AzVirtualNetworkGateway'</span><span class="sxs-lookup"><span data-stu-id="c16ab-1108">'Set-AzVirtualNetworkGateway'</span></span>
    - <span data-ttu-id="c16ab-1109">'New-AzVirtualNetworkGatewayConnection'</span><span class="sxs-lookup"><span data-stu-id="c16ab-1109">'New-AzVirtualNetworkGatewayConnection'</span></span>
    - <span data-ttu-id="c16ab-1110">'Set-AzVirtualNetworkGatewayConnection'</span><span class="sxs-lookup"><span data-stu-id="c16ab-1110">'Set-AzVirtualNetworkGatewayConnection'</span></span>
* <span data-ttu-id="c16ab-1111">FQDN 기반 LocalNetworkGateways 및 VpnSites를 사용하도록 설정하는 cmdlet이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1111">Updated cmdlets to enable FQDN based LocalNetworkGateways and VpnSites</span></span>
    - <span data-ttu-id="c16ab-1112">'New-AzLocalNetworkGateway'</span><span class="sxs-lookup"><span data-stu-id="c16ab-1112">'New-AzLocalNetworkGateway'</span></span>
    - <span data-ttu-id="c16ab-1113">'New-AzVpnSiteLink'</span><span class="sxs-lookup"><span data-stu-id="c16ab-1113">'New-AzVpnSiteLink'</span></span>
* <span data-ttu-id="c16ab-1114">ExpressRouteCircuitConnectionConfig(Global Reach)의 IPv6 주소 패밀리에 대한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1114">Added support for IPv6 address family in ExpressRouteCircuitConnectionConfig (Global Reach)</span></span>
    - <span data-ttu-id="c16ab-1115">'Set-AzExpressRouteCircuitConnectionConfig'가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1115">Added 'Set-AzExpressRouteCircuitConnectionConfig'</span></span>
        - <span data-ttu-id="c16ab-1116">IPv6CircuitConnectionProperties를 포함한 모든 기존 속성을 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1116">allows setting of all the existing properties including the IPv6CircuitConnectionProperties</span></span>
    - <span data-ttu-id="c16ab-1117">'Add-AzExpressRouteCircuitConnectionConfig'가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1117">Updated 'Add-AzExpressRouteCircuitConnectionConfig'</span></span>
        - <span data-ttu-id="c16ab-1118">주소 접두사의 주소 패밀리를 지정하는 또 다른 선택적 매개 변수 AddressPrefixType이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1118">Added another optional parameter AddressPrefixType to specify the address family of address prefix</span></span>
* <span data-ttu-id="c16ab-1119">Virtual Network 게이트웨이 연결에서 DPD 시간 제한 설정을 사용하도록 cmdlet이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1119">Updated cmdlets to enable setting of DPD Timeout on Virtual Network Gateway Connections.</span></span>
    - <span data-ttu-id="c16ab-1120">New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="c16ab-1120">New-AzVirtualNetworkGatewayConnection</span></span>
    - <span data-ttu-id="c16ab-1121">Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="c16ab-1121">Set-AzVirtualNetworkGatewayConnection</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="c16ab-1122">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="c16ab-1122">Az.PolicyInsights</span></span>
* <span data-ttu-id="c16ab-1123">정책 준수 검사를 트리거하기 위한 'Start-AzPolicyComplianceScan' cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1123">Added 'Start-AzPolicyComplianceScan' cmdlet for triggering policy compliance scans</span></span>
* <span data-ttu-id="c16ab-1124">'Get-AzPolicyState' 출력에 정책 정의, 집합 정의 및 할당 버전이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1124">Added policy definition, set definition, and assignment versions to 'Get-AzPolicyState' output</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="c16ab-1125">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="c16ab-1125">Az.ServiceFabric</span></span>
* <span data-ttu-id="c16ab-1126">'New-AzServiceFabricCluster' 예제의 코드 서식 및 사용 편의성이 개선되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1126">Improved code formatting and usability of 'New-AzServiceFabricCluster' examples</span></span>

#### <a name="azsql"></a><span data-ttu-id="c16ab-1127">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="c16ab-1127">Az.Sql</span></span>
* <span data-ttu-id="c16ab-1128">'Get-AzSqlInstanceOperation' 및 'Stop-AzSqlInstanceOperation' cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1128">Added cmdlets 'Get-AzSqlInstanceOperation' and 'Stop-AzSqlInstanceOperation'</span></span>
* <span data-ttu-id="c16ab-1129">VNet에서 스토리지 계정에 대한 감사가 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1129">Supported auditing to a storage account in VNet.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="c16ab-1130">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="c16ab-1130">Az.Storage</span></span>
* <span data-ttu-id="c16ab-1131">향후 릴리스의 Azure File cmdlet 출력 변경에 대한 호환성이 손상되는 변경 공지가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1131">Added breaking change notice for Azure File cmdlets output change in a future release</span></span>
* <span data-ttu-id="c16ab-1132">스토리지 계정 생성/업데이트 시 새로운 SkuName StandardGZRS, StandardRAGZRS가 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1132">Supported new SkuName StandardGZRS, StandardRAGZRS when create/update Storage account</span></span>
    - <span data-ttu-id="c16ab-1133">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="c16ab-1133">'New-AzStorageAccount'</span></span>
    - <span data-ttu-id="c16ab-1134">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="c16ab-1134">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="c16ab-1135">DataLake Gen2가 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1135">Supported DataLake Gen2</span></span>
    - <span data-ttu-id="c16ab-1136">'New-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="c16ab-1136">'New-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="c16ab-1137">'Get-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="c16ab-1137">'Get-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="c16ab-1138">'Get-AzDataLakeGen2ChildItem'</span><span class="sxs-lookup"><span data-stu-id="c16ab-1138">'Get-AzDataLakeGen2ChildItem'</span></span>
    - <span data-ttu-id="c16ab-1139">'Move-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="c16ab-1139">'Move-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="c16ab-1140">'Set-AzDataLakeGen2ItemAclObject'</span><span class="sxs-lookup"><span data-stu-id="c16ab-1140">'Set-AzDataLakeGen2ItemAclObject'</span></span>
    - <span data-ttu-id="c16ab-1141">'Update-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="c16ab-1141">'Update-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="c16ab-1142">'Get-AzDataLakeGen2ItemContent'</span><span class="sxs-lookup"><span data-stu-id="c16ab-1142">'Get-AzDataLakeGen2ItemContent'</span></span>
    - <span data-ttu-id="c16ab-1143">'Remove-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="c16ab-1143">'Remove-AzDataLakeGen2Item'</span></span>

## <a name="0100-preview---april-2020"></a><span data-ttu-id="c16ab-1144">0.10.0-preview - 2020년 4월</span><span class="sxs-lookup"><span data-stu-id="c16ab-1144">0.10.0-preview - April 2020</span></span>
### <a name="general"></a><span data-ttu-id="c16ab-1145">일반</span><span class="sxs-lookup"><span data-stu-id="c16ab-1145">General</span></span>
* <span data-ttu-id="c16ab-1146">이제 Az 모듈이 Azure Stack Hub에서 미리 보기로 제공됩니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1146">Az modules is now available in preview on Azure Stack Hub.</span></span> <span data-ttu-id="c16ab-1147">따라서 Linux 및 macOS와의 플랫폼 간 호환성이 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1147">This allows for cross-platform compatibility with Linux and macOs.</span></span> <span data-ttu-id="c16ab-1148">Azure Stack Hub는 이제 Az 모듈을 사용하여 PowerShell Core를 지원합니다. 자세한 내용은 [여기](https://aka.ms/az4AzureStack)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1148">Azure Stack Hub now supports PowerShell core with the Az modules, more information [here](https://aka.ms/az4AzureStack)</span></span>
* <span data-ttu-id="c16ab-1149">Az 모듈은 2019-03-01-hybrid 프로필을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1149">Az modules support profile 2019-03-01-hybrid:</span></span>
  - <span data-ttu-id="c16ab-1150">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="c16ab-1150">Az.Billing</span></span>
  - <span data-ttu-id="c16ab-1151">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="c16ab-1151">Az.Compute</span></span>
  - <span data-ttu-id="c16ab-1152">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="c16ab-1152">Az.DataBoxEdge</span></span>
  - <span data-ttu-id="c16ab-1153">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="c16ab-1153">Az.EventHub</span></span>
  - <span data-ttu-id="c16ab-1154">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="c16ab-1154">Az.IotHub</span></span>
  - <span data-ttu-id="c16ab-1155">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="c16ab-1155">Az.KeyVault</span></span>
  - <span data-ttu-id="c16ab-1156">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="c16ab-1156">Az.Monitor</span></span>
  - <span data-ttu-id="c16ab-1157">Az.Network</span><span class="sxs-lookup"><span data-stu-id="c16ab-1157">Az.Network</span></span>
  - <span data-ttu-id="c16ab-1158">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="c16ab-1158">Az.Resources</span></span>
  - <span data-ttu-id="c16ab-1159">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="c16ab-1159">Az.Storage</span></span>
  - <span data-ttu-id="c16ab-1160">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="c16ab-1160">Az.Websites</span></span>
* <span data-ttu-id="c16ab-1161">Azure Stack Hub와 함께 작동하는 az용 새 PowerShell 모듈 3개(Az.Databox, Az.IotHub 및 Az.EventHub)가 도입되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1161">Three new PowerShell modules for az have been introduced that work with Azure Stack Hub, which are Az.Databox, Az.IotHub, and Az.EventHub</span></span>
* <span data-ttu-id="c16ab-1162">AzureRM을 Az로 변경하는 것과 같은 사소한 변경을 수행하면 명령이 비교적 동일하게 유지됩니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1162">Commands remain relatively the same, with minor changes such as changing AzureRM to Az</span></span>
* <span data-ttu-id="c16ab-1163">Azure Stack Hub에 대한 PowerShell 설명서의 업데이트된 링크는 [여기](https://aka.ms/InstallASHPowerShell)에서 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1163">Updated link to PowerShell documentation for Azure Stack Hub can be found [here](https://aka.ms/InstallASHPowerShell)</span></span>

## <a name="370---march-2020"></a><span data-ttu-id="c16ab-1164">3.7.0 - 2020년 3월</span><span class="sxs-lookup"><span data-stu-id="c16ab-1164">3.7.0 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="c16ab-1165">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="c16ab-1165">Az.Accounts</span></span>
* <span data-ttu-id="c16ab-1166">로그인하지 않을 때 'Get-AzTenant'/'Get-AzDefault'/'Set-AzDefault'에서 NullReferenceException이 발생하는 문제가 해결되었습니다. [# 10292]</span><span class="sxs-lookup"><span data-stu-id="c16ab-1166">Fixed 'Get-AzTenant'/'Get-AzDefault'/'Set-AzDefault' throw NullReferenceException when not login [#10292]</span></span>

#### <a name="azcompute"></a><span data-ttu-id="c16ab-1167">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="c16ab-1167">Az.Compute</span></span>
* <span data-ttu-id="c16ab-1168">'New-AzDiskConfig' cmdlet에 다음 매개 변수를 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1168">Added the following parameters to 'New-AzDiskConfig' cmdlet:</span></span>
    - <span data-ttu-id="c16ab-1169">DiskIOPSReadOnly, DiskMBpsReadOnly, MaxSharesCount, GalleryImageReference</span><span class="sxs-lookup"><span data-stu-id="c16ab-1169">DiskIOPSReadOnly, DiskMBpsReadOnly, MaxSharesCount, GalleryImageReference</span></span>
* <span data-ttu-id="c16ab-1170">암호화 속성이 'New-AzGalleryImageVersion'cmdlet의 대상 매개 변수에 허용되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1170">Allowed Encryption property to Target parameter of 'New-AzGalleryImageVersion' cmdlet.</span></span>
* <span data-ttu-id="c16ab-1171">'Set-AzVmss'-Reimage 및 'Invoke-AzVMReimage'cmdlet에 대한 tempDisk 이슈가 해결되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1171">Fixed tempDisk issue for 'Set-AzVmss' -Reimage and 'Invoke-AzVMReimage' cmdlets.</span></span> <span data-ttu-id="c16ab-1172">[#11354]</span><span class="sxs-lookup"><span data-stu-id="c16ab-1172">[#11354]</span></span>
* <span data-ttu-id="c16ab-1173">새로운 SAP 확장을 위해 아래 cmdlet에 대한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1173">Added support to below cmdlets for new SAP Extension</span></span>
    - <span data-ttu-id="c16ab-1174">'Set-AzVMAEMExtension'</span><span class="sxs-lookup"><span data-stu-id="c16ab-1174">'Set-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="c16ab-1175">'Get-AzVMAEMExtension'</span><span class="sxs-lookup"><span data-stu-id="c16ab-1175">'Get-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="c16ab-1176">'Remove-AzVMAEMExtension'</span><span class="sxs-lookup"><span data-stu-id="c16ab-1176">'Remove-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="c16ab-1177">'Update-AzVMAEMExtension'</span><span class="sxs-lookup"><span data-stu-id="c16ab-1177">'Update-AzVMAEMExtension'</span></span>
* <span data-ttu-id="c16ab-1178">도움말 문서의 예제에서 오류가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1178">Fixed errors in examples of help document</span></span>
* <span data-ttu-id="c16ab-1179">VM PowerState의 정확한 문자열 값을 테이블 형식으로 표시했습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1179">Showed the exact string value for VM PowerState in the table format.</span></span>
* <span data-ttu-id="c16ab-1180">'New-AzVmssConfig': SinglePlacementGroup이 비활성화된 경우 AutomaticRepairs 속성의 직렬화가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1180">'New-AzVmssConfig': fixed serialization of AutomaticRepairs property when SinglePlacementGroup is disabled.</span></span> <span data-ttu-id="c16ab-1181">[#11257]</span><span class="sxs-lookup"><span data-stu-id="c16ab-1181">[#11257]</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="c16ab-1182">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="c16ab-1182">Az.DataFactory</span></span>
* <span data-ttu-id="c16ab-1183">ADF .Net SDK 버전이 4.8.0으로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1183">Updated ADF .Net SDK version to 4.8.0</span></span>
* <span data-ttu-id="c16ab-1184">재실행을 지원하기 위해 'Invoke-AzDataFactoryV2Pipeline' 명령에 선택적 매개 변수를 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1184">Added optional parameters to 'Invoke-AzDataFactoryV2Pipeline' command to support rerun</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="c16ab-1185">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="c16ab-1185">Az.DataLakeStore</span></span>
* <span data-ttu-id="c16ab-1186">'Export-AzDataLakeStoreItem' 및 'Import-AzDataLakeStoreItem'에 대해 호환성이 손상되는 변경 설명을 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1186">Added breaking change description for 'Export-AzDataLakeStoreItem' and 'Import-AzDataLakeStoreItem'</span></span>
* <span data-ttu-id="c16ab-1187">'New-AzDataLakeStoreItem', 'Add-AzDAtaLakeStoreItemContent' 및 'Get-AzDAtaLakeStoreItemContent'에 대한 바이트 인코딩 옵션이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1187">Added option of Byte encoding for 'New-AzDataLakeStoreItem', 'Add-AzDAtaLakeStoreItemContent', and 'Get-AzDAtaLakeStoreItemContent'</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="c16ab-1188">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="c16ab-1188">Az.HDInsight</span></span>
* <span data-ttu-id="c16ab-1189">클러스터 생성 시 최소 지원 TLS 버전 지정이 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1189">Supported specifying minimal supported TLS version when creating cluster.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="c16ab-1190">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="c16ab-1190">Az.IotHub</span></span>
* <span data-ttu-id="c16ab-1191">디바이스별 분산 설정을 관리하기 위한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1191">Added support to manage distributed settings per-device.</span></span> <span data-ttu-id="c16ab-1192">새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1192">New Cmdlets are:</span></span>
    - <span data-ttu-id="c16ab-1193">'Get-AzIotHubDistributedTracing'</span><span class="sxs-lookup"><span data-stu-id="c16ab-1193">'Get-AzIotHubDistributedTracing'</span></span>
    - <span data-ttu-id="c16ab-1194">'Set-AzIotHubDistributedTracing'</span><span class="sxs-lookup"><span data-stu-id="c16ab-1194">'Set-AzIotHubDistributedTracing'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="c16ab-1195">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="c16ab-1195">Az.KeyVault</span></span>
* <span data-ttu-id="c16ab-1196">'New-AzKeyVault'에 대해 호환성이 손상되는 변경 속성이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1196">Added breaking change attributes to 'New-AzKeyVault'</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="c16ab-1197">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="c16ab-1197">Az.Monitor</span></span>
* <span data-ttu-id="c16ab-1198">'New-AzScheduledQueryRuleLogMetricTrigger'에 대한 설명서가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1198">Updated documentation for 'New-AzScheduledQueryRuleLogMetricTrigger'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="c16ab-1199">Az.Network</span><span class="sxs-lookup"><span data-stu-id="c16ab-1199">Az.Network</span></span>
* <span data-ttu-id="c16ab-1200">교차 테넌트 VirtualHubVnetConnections를 허용하도록 cmdlet이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1200">Updated cmdlets to allow cross-tenant VirtualHubVnetConnections</span></span>
    - <span data-ttu-id="c16ab-1201">'New-AzVirtualHubVnetConnection'</span><span class="sxs-lookup"><span data-stu-id="c16ab-1201">'New-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="c16ab-1202">'Update-AzVirtualHubVnetConnection'</span><span class="sxs-lookup"><span data-stu-id="c16ab-1202">'Update-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="c16ab-1203">'New-AzVirtualHub'</span><span class="sxs-lookup"><span data-stu-id="c16ab-1203">'New-AzVirtualHub'</span></span>
    - <span data-ttu-id="c16ab-1204">'Update-AzVirtualHub'</span><span class="sxs-lookup"><span data-stu-id="c16ab-1204">'Update-AzVirtualHub'</span></span>
* <span data-ttu-id="c16ab-1205">SQL Management SDK 종속성이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1205">Removed Sql Management SDK dependency</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="c16ab-1206">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="c16ab-1206">Az.PolicyInsights</span></span>
* <span data-ttu-id="c16ab-1207">오류 메시지가 향상되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1207">Improved error messages</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="c16ab-1208">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="c16ab-1208">Az.RecoveryServices</span></span>
* <span data-ttu-id="c16ab-1209">Azure Site Recovery는 Azure 디스크 암호화 Virtual Machines에 대한 VM 속성을 다시 보호하고 업데이트하는 기능을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1209">Azure Site Recovery added support for doing reprotect and updated vm properties for Azure disk encrypted Virtual Machines.</span></span>
* <span data-ttu-id="c16ab-1210">Azure Site Recovery VmwareToAzure 속성 DR 모니터링이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1210">Added Azure Site Recovery VmwareToAzure properties DR monitoring</span></span>
* <span data-ttu-id="c16ab-1211">Azure Backup은 실패한 항목에 대한 정책 업데이트 재시도 지원을 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1211">Azure Backup added support for retrying policy update for failed items.</span></span>
* <span data-ttu-id="c16ab-1212">Azure Backup은 백업 및 복원 중에 디스크 제외 설정에 대한 지원을 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1212">Azure Backup Added support for disk exclusion settings during backup and restore.</span></span>
* <span data-ttu-id="c16ab-1213">Azure Backup은 AzureFileShare에서 여러 파일/폴더 복원을 위한 지원을 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1213">Azure Backup Added Support for Restoring Multiple files/folders in AzureFileShare</span></span>
* <span data-ttu-id="c16ab-1214">Azure Backup은 IaasVM 정책을 업데이트하는 동안 사용자 지정 리소스 그룹 지원에 대한 지원을 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1214">Azure Backup Added support for User-specified Resourcegroup support while updating IaasVM Policy</span></span>

#### <a name="azresources"></a><span data-ttu-id="c16ab-1215">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="c16ab-1215">Az.Resources</span></span>
* <span data-ttu-id="c16ab-1216">'Get-AzResource -ResourceGroupName -Name -ExpandProperties -ResourceType'이 기본 apiVersion 대신 실제 apiVersion 리소스를 사용하도록 수정했습니다. [# 11267]</span><span class="sxs-lookup"><span data-stu-id="c16ab-1216">Fixed 'Get-AzResource -ResourceGroupName -Name -ExpandProperties -ResourceType' to use actual apiVersion of resources instead of default apiVersion [#11267]</span></span>
* <span data-ttu-id="c16ab-1217">오류 시나리오에 대해 correlationId 로깅이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1217">Added correlationId logging for error scenarios</span></span>
* <span data-ttu-id="c16ab-1218">작은 설명서가 'Get-AzResourceLock'으로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1218">Small documentation change to 'Get-AzResourceLock'.</span></span> <span data-ttu-id="c16ab-1219">예제가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1219">Added example.</span></span>
* <span data-ttu-id="c16ab-1220">'Get-AzADUser'의 매개 변수 값에서 작은 따옴표를 이스케이프 처리하였습니다. [# 11317]</span><span class="sxs-lookup"><span data-stu-id="c16ab-1220">Escaped single quote in parameter value of 'Get-AzADUser' [#11317]</span></span>
* <span data-ttu-id="c16ab-1221">배포 스크립트('Get-AzDeploymentScript', 'Get-AzDeploymentScriptLog', 'Save-AzDeploymentScriptLog', 'Remove-AzDeploymentScript')에 대한 새로운 cmdlet 추가가 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1221">Added new cmdlets for Deployment Scripts ('Get-AzDeploymentScript', 'Get-AzDeploymentScriptLog', 'Save-AzDeploymentScriptLog', 'Remove-AzDeploymentScript')</span></span>

#### <a name="azsql"></a><span data-ttu-id="c16ab-1222">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="c16ab-1222">Az.Sql</span></span>
* <span data-ttu-id="c16ab-1223">'Invoke-AzSqlDatabaseFailover'에 읽기 가능한 보조 매개 변수를 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1223">Added readable secondary parameter to 'Invoke-AzSqlDatabaseFailover'</span></span>
* <span data-ttu-id="c16ab-1224">'Disable-AzSqlServerActiveDirectoryOnlyAuthentication' cmdlet을 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1224">Added cmdlet 'Disable-AzSqlServerActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="c16ab-1225">데이터베이스에서 열을 분류할 때 저장된 민감도 순위입니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1225">Saved sensitivity rank when classifying columns in the database.</span></span>

#### <a name="azsupport"></a><span data-ttu-id="c16ab-1226">Az.Support</span><span class="sxs-lookup"><span data-stu-id="c16ab-1226">Az.Support</span></span>
* <span data-ttu-id="c16ab-1227">'Az.Support' 모듈의 일반 공급</span><span class="sxs-lookup"><span data-stu-id="c16ab-1227">General availability of 'Az.Support' module</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="c16ab-1228">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="c16ab-1228">Az.Websites</span></span>
* <span data-ttu-id="c16ab-1229">아래의 새로운 cmdlet을 통해 webapp 트래픽 라우팅 규칙을 사용하는 작업에 대한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1229">Added support for working with webapp Traffic Routing Rules via below new cmdlets</span></span>
    - <span data-ttu-id="c16ab-1230">'Get-AzWebAppTrafficRouting'</span><span class="sxs-lookup"><span data-stu-id="c16ab-1230">'Get-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="c16ab-1231">'Update-AzWebAppTrafficRouting'</span><span class="sxs-lookup"><span data-stu-id="c16ab-1231">'Update-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="c16ab-1232">'Add-AzWebAppTrafficRouting'</span><span class="sxs-lookup"><span data-stu-id="c16ab-1232">'Add-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="c16ab-1233">'Remove-AzWebAppTrafficRouting'</span><span class="sxs-lookup"><span data-stu-id="c16ab-1233">'Remove-AzWebAppTrafficRouting'</span></span>

## <a name="361---march-2020"></a><span data-ttu-id="c16ab-1234">3.6.1 - 2020년 3월</span><span class="sxs-lookup"><span data-stu-id="c16ab-1234">3.6.1 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="c16ab-1235">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="c16ab-1235">Az.Accounts</span></span>
* <span data-ttu-id="c16ab-1236">'피드백 보내기'에서 Azure PowerShell 설문 조사 페이지가 열립니다[#11020].</span><span class="sxs-lookup"><span data-stu-id="c16ab-1236">Open Azure PowerShell survey page in 'Send-Feedback' [#11020]</span></span>
* <span data-ttu-id="c16ab-1237">'오류 해결'에서 Azure PowerShell 설문 조사 URL이 표시됩니다[#11021].</span><span class="sxs-lookup"><span data-stu-id="c16ab-1237">Display Azure PowerShell survey URL in 'Resolve-Error' [#11021]</span></span>
* <span data-ttu-id="c16ab-1238">UserAgent에서 Az 버전이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1238">Added Az version in UserAgent</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="c16ab-1239">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="c16ab-1239">Az.ApiManagement</span></span>
* <span data-ttu-id="c16ab-1240">DeveloperPortal 엔드포인트에서 사용자 지정 도메인을 검색하고 구성하기 위한 지원이 추가되었습니다[#11007].</span><span class="sxs-lookup"><span data-stu-id="c16ab-1240">Added support for retrieving and configuring Custom Domain on the DeveloperPortal Endpoint [#11007]</span></span>
* <span data-ttu-id="c16ab-1241">Json 형식의 API 정의를 다운로드하기 위한 'Export-AzApiManagementApi' 지원이 추가되었습니다[#9987].</span><span class="sxs-lookup"><span data-stu-id="c16ab-1241">'Export-AzApiManagementApi' Added support for downloading Api Definition in Json format [#9987]</span></span>
* <span data-ttu-id="c16ab-1242">Json 문서에서 OpenApi 3.0 정의를 가져오기 위한 'Import-AzApiManagementApi' 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1242">'Import-AzApiManagementApi' Added support for importing OpenApi 3.0 definition from Json document</span></span>
* <span data-ttu-id="c16ab-1243">AAD B2C 공급자에 대한 '로그인 테넌트'를 구성하기 위한 'New-AzApiManagementIdentityProvider' 및 'Set-AzApiManagementIdentityProvider' 지원이 추가되었습니다[#9784].</span><span class="sxs-lookup"><span data-stu-id="c16ab-1243">'New-AzApiManagementIdentityProvider' and 'Set-AzApiManagementIdentityProvider' Added support for configuring 'Signin Tenant' for AAD B2C Provider [#9784]</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="c16ab-1244">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="c16ab-1244">Az.DataLakeStore</span></span>
* <span data-ttu-id="c16ab-1245">csproj 및 psd1에서 System.Buffers에 대한 참조가 명시적으로 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1245">Added reference to System.Buffers explicitly in csproj and psd1.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="c16ab-1246">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="c16ab-1246">Az.IotHub</span></span>
* <span data-ttu-id="c16ab-1247">Iot Hub에서 디바이스를 관리하기 위한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1247">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="c16ab-1248">새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1248">New Cmdlets are:</span></span>
    - <span data-ttu-id="c16ab-1249">'Add-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="c16ab-1249">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="c16ab-1250">'Get-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="c16ab-1250">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="c16ab-1251">'Remove-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="c16ab-1251">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="c16ab-1252">'Set-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="c16ab-1252">'Set-AzIotHubDevice'</span></span>
* <span data-ttu-id="c16ab-1253">Iot Hub의 대상 IoT 디바이스에서 모듈을 관리하기 위한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1253">Added support to manage modules on a target Iot device in an Iot Hub.</span></span> <span data-ttu-id="c16ab-1254">새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1254">New Cmdlets are:</span></span>
    - <span data-ttu-id="c16ab-1255">'Add-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="c16ab-1255">'Add-AzIotHubModule'</span></span>
    - <span data-ttu-id="c16ab-1256">'Get-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="c16ab-1256">'Get-AzIotHubModule'</span></span>
    - <span data-ttu-id="c16ab-1257">'Remove-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="c16ab-1257">'Remove-AzIotHubModule'</span></span>
    - <span data-ttu-id="c16ab-1258">'Set-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="c16ab-1258">'Set-AzIotHubModule'</span></span>
* <span data-ttu-id="c16ab-1259">Iot Hub에서 대상 IoT 디바이스에 대한 연결 문자열을 가져오는 cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1259">Added cmdlet to get the connection string of a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="c16ab-1260">Iot Hub에서 대상 IoT 디바이스의 모듈에 대한 연결 문자열을 가져오는 cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1260">Added cmdlet to get the connection string of a module on a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="c16ab-1261">IoT 디바이스의 부모 디바이스를 가져오거나 설정하기 위한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1261">Added support to get/set parent device of an IoT device.</span></span> <span data-ttu-id="c16ab-1262">새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1262">New Cmdlets are:</span></span>
    - <span data-ttu-id="c16ab-1263">'Get-AzIotHubDeviceParent'</span><span class="sxs-lookup"><span data-stu-id="c16ab-1263">'Get-AzIotHubDeviceParent'</span></span>
    - <span data-ttu-id="c16ab-1264">'Set-AzIotHubDeviceParent'</span><span class="sxs-lookup"><span data-stu-id="c16ab-1264">'Set-AzIotHubDeviceParent'</span></span>
* <span data-ttu-id="c16ab-1265">디바이스 부모-자식 관계를 관리하기 위한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1265">Added support to manage device parent-child relationship.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="c16ab-1266">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="c16ab-1266">Az.Monitor</span></span>
* <span data-ttu-id="c16ab-1267">'Get-AzMetricDefinition'에 대한 출력 값이 수정되었습니다[#9714].</span><span class="sxs-lookup"><span data-stu-id="c16ab-1267">Fixed output value for 'Get-AzMetricDefinition' [#9714]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="c16ab-1268">Az.Network</span><span class="sxs-lookup"><span data-stu-id="c16ab-1268">Az.Network</span></span>
* <span data-ttu-id="c16ab-1269">SQL Management SDK가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1269">Updated Sql Management SDK.</span></span>
* <span data-ttu-id="c16ab-1270">PrivateLinkServiceConnectionState 클래스의 명명 차이 문제가 해결되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1270">Fixed a naming-difference issue in PrivateLinkServiceConnectionState class.</span></span>
    - <span data-ttu-id="c16ab-1271">ActionsRequired 필드가 ActionRequired에 매핑됩니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1271">Mapping the field ActionsRequired to ActionRequired.</span></span>
* <span data-ttu-id="c16ab-1272">PublicNetworkAccess가 'New-AzSqlServer' 및 'Set-AzSqlServer'에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1272">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>

#### <a name="azresources"></a><span data-ttu-id="c16ab-1273">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="c16ab-1273">Az.Resources</span></span>
* <span data-ttu-id="c16ab-1274">Get-AzRoleAssignment'의 null 참조 버그가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1274">Fixed for null reference bug in 'Get-AzRoleAssignment'</span></span>
* <span data-ttu-id="c16ab-1275">'Remove-AzADGroup'에서 '-Force' 및 '-PassThru' 스위치가 선택적으로 표시됩니다[#10849].</span><span class="sxs-lookup"><span data-stu-id="c16ab-1275">Marked switch '-Force' and '-PassThru' optional in 'Remove-AzADGroup' [#10849]</span></span>
* <span data-ttu-id="c16ab-1276">'Remove-AzADGroup'에서 'MailNickname'이 반환되지 않는 문제가 해결되었습니다[#11167].</span><span class="sxs-lookup"><span data-stu-id="c16ab-1276">Fixed issue that 'MailNickname' doesn't return in 'Remove-AzADGroup' [#11167]</span></span>
* <span data-ttu-id="c16ab-1277">'Remove-AzADGroup' 파이프 작업이 작동하지 않는 문제가 해결되었습니다[#11171].</span><span class="sxs-lookup"><span data-stu-id="c16ab-1277">Fixed issue that 'Remove-AzADGroup' pipe operation doesn't work [#11171]</span></span>
* <span data-ttu-id="c16ab-1278">GetAzureRoleAssignmentCommand의 null 참조 버그가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1278">Fixed for null reference bug in GetAzureRoleAssignmentCommand</span></span>
* <span data-ttu-id="c16ab-1279">예정된 정책 cmdlet 변경에 대한 호환성이 손상되는 변경 특성이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1279">Added breaking change attributes for upcoming changes to policy cmdlets</span></span>
* <span data-ttu-id="c16ab-1280">서버 쪽에서 리소스 그룹 태그 필터링을 수행하도록 'Get-AzResourceGroup'이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1280">Updated 'Get-AzResourceGroup' to perform resource group tag filtering on server-side</span></span>
* <span data-ttu-id="c16ab-1281">-ResourceId를 허용하도록 Tag cmdlet이 확장되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1281">Extended Tag cmdlets to accept -ResourceId</span></span>
    - <span data-ttu-id="c16ab-1282">Get-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="c16ab-1282">Get-AzTag -ResourceId</span></span>
    - <span data-ttu-id="c16ab-1283">New-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="c16ab-1283">New-AzTag -ResourceId</span></span>
    - <span data-ttu-id="c16ab-1284">Remove-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="c16ab-1284">Remove-AzTag -ResourceId</span></span>
* <span data-ttu-id="c16ab-1285">새 Tag cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1285">Added new Tag cmdlet</span></span>
    - <span data-ttu-id="c16ab-1286">Update-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="c16ab-1286">Update-AzTag -ResourceId</span></span>
* <span data-ttu-id="c16ab-1287">SDK 3.3.0에서 ScopedDeployment를 가져왔습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1287">Brought ScopedDeployment from SDK 3.3.0</span></span>

#### <a name="azsql"></a><span data-ttu-id="c16ab-1288">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="c16ab-1288">Az.Sql</span></span>
* <span data-ttu-id="c16ab-1289">PublicNetworkAccess가 'New-AzSqlServer' 및 'Set-AzSqlServer'에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1289">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>
* <span data-ttu-id="c16ab-1290">관리형 데이터베이스에 대한 장기 보존 백업 구성에 대한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1290">Added support for Long Term Retention backup configuration for Managed Databases</span></span>
    - <span data-ttu-id="c16ab-1291">관리형 데이터베이스에서 LTR 정책을 가져오거나 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1291">Get/Set LTR policy on a managed database</span></span>
    - <span data-ttu-id="c16ab-1292">관리형 데이터베이스, 관리형 인스턴스 또는 위치를 기준으로 LTR 백업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1292">Get LTR backup(s) by managed database, managed instance, or by location</span></span>
    - <span data-ttu-id="c16ab-1293">LTR 백업을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1293">Remove an LTR backup</span></span>
    - <span data-ttu-id="c16ab-1294">LTR 백업을 복원하여 새 관리형 데이터베이스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1294">Restore an LTR backup to create a new managed database</span></span>
* <span data-ttu-id="c16ab-1295">MinimalTlsVersion이 New-AzSqlServer 및 Set-AzSqlServer에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1295">Added MinimalTlsVersion to New-AzSqlServer and Set-AzSqlServer</span></span>
* <span data-ttu-id="c16ab-1296">MinimalTlsVersion을 New-AzSqlInstance 및 Set-AzSqlInstance에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1296">Added MinimalTlsVersion to New-AzSqlInstance and Set-AzSqlInstance</span></span>
* <span data-ttu-id="c16ab-1297">Az.Network에 대한 SQL SDK 버전이 높아졌습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1297">Bumped SQL SDK version for Az.Network</span></span>

#### <a name="azstorage"></a><span data-ttu-id="c16ab-1298">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="c16ab-1298">Az.Storage</span></span>
* <span data-ttu-id="c16ab-1299">ImmutabilityPolicy에서 AllowProtectedAppendWrite가 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1299">Supported AllowProtectedAppendWrite in ImmutabilityPolicy</span></span>
    - <span data-ttu-id="c16ab-1300">'Set-AzRmStorageContainerImmutabilityPolicy'</span><span class="sxs-lookup"><span data-stu-id="c16ab-1300">'Set-AzRmStorageContainerImmutabilityPolicy'</span></span>
* <span data-ttu-id="c16ab-1301">이후 릴리스에서 AzureStorageTable 형식 변경에 대한 호환성이 손상되는 변경 경고 메시지가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1301">Added breaking change warning message for AzureStorageTable type change in a future release</span></span>
    - <span data-ttu-id="c16ab-1302">'New-AzStorageTable'</span><span class="sxs-lookup"><span data-stu-id="c16ab-1302">'New-AzStorageTable'</span></span>
    - <span data-ttu-id="c16ab-1303">'Get-AzStorageTable'</span><span class="sxs-lookup"><span data-stu-id="c16ab-1303">'Get-AzStorageTable'</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="c16ab-1304">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="c16ab-1304">Az.Websites</span></span>
* <span data-ttu-id="c16ab-1305">'New-AzAppServicePlan' 및 'Set-AzAppServicePlan'에 대한 Tag 매개 변수가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1305">Added Tag parameter for 'New-AzAppServicePlan' and 'Set-AzAppServicePlan'</span></span>
* <span data-ttu-id="c16ab-1306">웹 사이트에 사용자 지정 도메인을 추가할 때 예외가 throw되면 cmdlet 실행을 중지합니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1306">Stop cmdlet execution if an exception is thrown when adding a custom domain to a website</span></span>
* <span data-ttu-id="c16ab-1307">App Service 계획과 동일한 리소스 그룹에 속하지 않는 App Services에 대한 작업을 수행하기 위한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1307">Added support to perform operations for App Services not in the same resource group as the App Service Plan</span></span>
* <span data-ttu-id="c16ab-1308">다른 리소스 그룹의 WebApp/Function에 대한 액세스 제한이 적용되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1308">Applied access restriction to WebApp/Function in different resource groups</span></span>
* <span data-ttu-id="c16ab-1309">WebAppSlot에 대한 사용자 지정 호스트 이름을 설정하는 문제가 해결되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1309">Fixed issue to set custom hostnames for WebAppSlots</span></span>

## <a name="350---february-2020"></a><span data-ttu-id="c16ab-1310">3.5.0 - 2020년 2월</span><span class="sxs-lookup"><span data-stu-id="c16ab-1310">3.5.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="c16ab-1311">마지막 주 릴리스 이후의 주요 사항</span><span class="sxs-lookup"><span data-stu-id="c16ab-1311">Highlights since the last major release</span></span>
* <span data-ttu-id="c16ab-1312">클라이언트 쪽 원격 분석이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1312">Updated client side telemetry.</span></span>
* <span data-ttu-id="c16ab-1313">디바이스 관리를 지원하는 cmdlet이 Az.IotHub에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1313">Az.IotHub added cmdlets to support to manage devices.</span></span>
* <span data-ttu-id="c16ab-1314">가용성 그룹 수신기에 대한 cmdlet이 Az.SqlVirtualMachine에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1314">Az.SqlVirtualMachine added cmdlets for Availability Group Listener.</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="c16ab-1315">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="c16ab-1315">Az.Accounts</span></span>
* <span data-ttu-id="c16ab-1316">SubscriptionId, TenantId 및 실행 시간이 클라이언트 쪽 원격 분석에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1316">Added SubscriptionId, TenantId, and execution time into data of client side telemetry</span></span>

#### <a name="azautomation"></a><span data-ttu-id="c16ab-1317">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="c16ab-1317">Az.Automation</span></span>
* <span data-ttu-id="c16ab-1318">'New-AzAutomationSoftwareUpdateConfiguration' 참조 설명서의 예제 1에 있는 오타가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1318">Fixed typo in Example 1 in reference documentation for 'New-AzAutomationSoftwareUpdateConfiguration'</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="c16ab-1319">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="c16ab-1319">Az.CognitiveServices</span></span>
* <span data-ttu-id="c16ab-1320">SDK가 7.0으로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1320">Updated SDK to 7.0</span></span>
* <span data-ttu-id="c16ab-1321">서버 응답 본문이 비어 있는 경우 표시되는 오류 메시지가 향상되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1321">Improved error message when server responses empty body</span></span>

#### <a name="azcompute"></a><span data-ttu-id="c16ab-1322">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="c16ab-1322">Az.Compute</span></span>
* <span data-ttu-id="c16ab-1323">업데이트하는 동안 빈 값이 ProximityPlacementGroupId에 허용되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1323">Allowed empty value for ProximityPlacementGroupId during update</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="c16ab-1324">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="c16ab-1324">Az.FrontDoor</span></span>
* <span data-ttu-id="c16ab-1325">WAF에서 사용할 수 있는 관리형 규칙 정의를 가져오는 cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1325">Added cmdlet to get managed rule definitions that can be used in WAF</span></span>

#### <a name="aziothub"></a><span data-ttu-id="c16ab-1326">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="c16ab-1326">Az.IotHub</span></span>
* <span data-ttu-id="c16ab-1327">Iot Hub에서 디바이스를 관리하기 위한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1327">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="c16ab-1328">새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1328">New Cmdlets are:</span></span>
    - <span data-ttu-id="c16ab-1329">'Add-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="c16ab-1329">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="c16ab-1330">'Get-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="c16ab-1330">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="c16ab-1331">'Remove-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="c16ab-1331">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="c16ab-1332">'Set-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="c16ab-1332">'Set-AzIotHubDevice'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="c16ab-1333">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="c16ab-1333">Az.KeyVault</span></span>
* <span data-ttu-id="c16ab-1334">Add-AzKeyVaultKey.md에 대해 중복된 텍스트가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1334">Fixed duplicated text for Add-AzKeyVaultKey.md</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="c16ab-1335">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="c16ab-1335">Az.Monitor</span></span>
* <span data-ttu-id="c16ab-1336">Get-AzLog cmdlet에 대한 설명이 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1336">Fixed description of the Get-AzLog cmdlet.</span></span>
* <span data-ttu-id="c16ab-1337">ActionGroupId라는 새 매개 변수가 'New-AzMetricAlertRuleV2' 명령에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1337">A new parameter called ActionGroupId was added to 'New-AzMetricAlertRuleV2' command.</span></span>
    - <span data-ttu-id="c16ab-1338">사용자는 ActionGroupId(string) 또는 ActionGorup(ActivityLogAlertActionGroup) 중 하나를 제공할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1338">The user can provide either ActionGroupId(string) or ActionGorup(ActivityLogAlertActionGroup).</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="c16ab-1339">Az.Network</span><span class="sxs-lookup"><span data-stu-id="c16ab-1339">Az.Network</span></span>
* <span data-ttu-id="c16ab-1340">'New-AzPrivateLinkService' cmdlet의 '-EnableProxyProtocol' 매개 변수에 대한 하나의 추가 매개 변수 메모가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1340">Added one extra parameter note for parameter '-EnableProxyProtocol' for 'New-AzPrivateLinkService' cmdlet.</span></span>
* <span data-ttu-id="c16ab-1341">Start-AzVirtualNetworkGatewayConnectionPacketCapture.md 및 Start-AzVirtualnetworkGatewayPacketCapture.md의 FilterData 예제가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1341">Fixed FilterData example in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="c16ab-1342">Start-AzVirtualNetworkGatewayConnectionPacketCapture.md 및 Start-AzVirtualnetworkGatewayPacketCapture.md의 모든 내부 및 외부 패킷을 캡처하는 패킷 캡처 예제가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1342">Added Packet Capture example for capture all inner and outer packets in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="c16ab-1343">VNet 방화벽에서 Azure Firewall 정책이 지원됩니다</span><span class="sxs-lookup"><span data-stu-id="c16ab-1343">Supported Azure Firewall Policy on VNet Firewalls</span></span>
    - <span data-ttu-id="c16ab-1344">새로 추가된 cmdlet이 없습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1344">No new cmdlets are added.</span></span> <span data-ttu-id="c16ab-1345">VNet 방화벽에서 방화벽 정책 제한이 완화되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1345">Relaxing the restriction for firewall policy on VNet firewalls</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="c16ab-1346">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="c16ab-1346">Az.RecoveryServices</span></span>
* <span data-ttu-id="c16ab-1347">SQL Database에 대한 파일로 복원 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1347">Added Support for Restore-as-files for SQL Databases.</span></span>

#### <a name="azresources"></a><span data-ttu-id="c16ab-1348">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="c16ab-1348">Az.Resources</span></span>
* <span data-ttu-id="c16ab-1349">템플릿 배포 cmdlet이 리팩터링되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1349">Refactored template deployment cmdlets</span></span>
    - <span data-ttu-id="c16ab-1350">관리 그룹에서 배포를 관리하는 새 \*-AzManagementGroupDeployment cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1350">Added new cmdlets for managing deployments at management group: \*-AzManagementGroupDeployment</span></span>
    - <span data-ttu-id="c16ab-1351">테넌트 범위에서 배포를 관리하는 새 \*-AzTenantDeployment cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1351">Added new cmdlets for managing deployments at tenant scope: \*-AzTenantDeployment</span></span>
    - <span data-ttu-id="c16ab-1352">구독 범위에서 구체적으로 작동하도록 \*-AzDeployment cmdlet이 리팩터링되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1352">Refactored \*-AzDeployment cmdlets to work specifically at subscription scope</span></span>
    - <span data-ttu-id="c16ab-1353">\*-AzDeployment cmdlet에 대한 \*-AzSubscriptionDeployment 별칭이 만들어졌습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1353">Created aliases \*-AzSubscriptionDeployment for \*-AzDeployment cmdlets</span></span>
* <span data-ttu-id="c16ab-1354">'AvailableToOtherTenants' 매개 변수가 설정되지 않는 'Update-AzADApplication'이 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1354">Fixed 'Update-AzADApplication' when parameter 'AvailableToOtherTenants' is not set</span></span>
* <span data-ttu-id="c16ab-1355">AmbiguousParameterSetException을 방지하기 위해 ApplicationObjectWithoutCredentialParameterSet이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1355">Removed ApplicationObjectWithoutCredentialParameterSet to avoid AmbiguousParameterSetException.</span></span>
* <span data-ttu-id="c16ab-1356">도움말 파일이 다시 생성되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1356">Regenerated help files</span></span>

#### <a name="azsql"></a><span data-ttu-id="c16ab-1357">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="c16ab-1357">Az.Sql</span></span>
* <span data-ttu-id="c16ab-1358">Managed Instance에서 구독 간 특정 시점 복원에 대한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1358">Added support for cross subscription point in time restore on Managed Instances.</span></span>
* <span data-ttu-id="c16ab-1359">기존 SQL Managed Instance 하드웨어 생성 변경에 대한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1359">Added support for changing existing Sql Managed Instance hardware generation</span></span>
* <span data-ttu-id="c16ab-1360">'Update-AzSqlServerVulnerabilityAssessmentSetting' 도움말 예제(매개 변수/속성 출력 -EmailAdmins)가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1360">Fixed 'Update-AzSqlServerVulnerabilityAssessmentSetting' help examples: parameter/property output - EmailAdmins</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="c16ab-1361">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="c16ab-1361">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="c16ab-1362">가용성 그룹 수신기에 대한 cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1362">Added cmdlets for Availability Group Listener</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="c16ab-1363">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="c16ab-1363">Az.StorageSync</span></span>
* <span data-ttu-id="c16ab-1364">'Invoke-AzStorageSyncCompatibilityCheck'에서 지원되는 문자 세트가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1364">Updated supported character sets in 'Invoke-AzStorageSyncCompatibilityCheck'.</span></span>

## <a name="340---february-2020"></a><span data-ttu-id="c16ab-1365">3.4.0 - 2020년 2월</span><span class="sxs-lookup"><span data-stu-id="c16ab-1365">3.4.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="c16ab-1366">마지막 주 릴리스 이후의 주요 사항</span><span class="sxs-lookup"><span data-stu-id="c16ab-1366">Highlights since the last major release</span></span>
* <span data-ttu-id="c16ab-1367">Az. CosmosDB 초기 버전 0.1.0 출시</span><span class="sxs-lookup"><span data-stu-id="c16ab-1367">Az.CosmosDB initial version 0.1.0 released</span></span>
* <span data-ttu-id="c16ab-1368">Az.Network ConnectionMonitor V2 지원 추가</span><span class="sxs-lookup"><span data-stu-id="c16ab-1368">Az.Network ConnectionMonitor V2 support added</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="c16ab-1369">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="c16ab-1369">Az.Accounts</span></span>
* <span data-ttu-id="c16ab-1370">AzureRmContext.json을 사용할 수 없을 때 컨텍스트 자동 저장 사용 안 함</span><span class="sxs-lookup"><span data-stu-id="c16ab-1370">Disable context auto saving when AzureRmContext.json not available</span></span>
* <span data-ttu-id="c16ab-1371">Azure Powershell Common 참조를 1.3.5-preview로 업데이트</span><span class="sxs-lookup"><span data-stu-id="c16ab-1371">Update the reference to Azure Powershell Common to 1.3.5-preview</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="c16ab-1372">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="c16ab-1372">Az.ApiManagement</span></span>
* <span data-ttu-id="c16ab-1373">**Get-AzApiManagementApiSchema** API와 연결된 Open-Api 스키마 가져오기 수정   https://github.com/Azure/azure-powershell/issues/10626</span><span class="sxs-lookup"><span data-stu-id="c16ab-1373">**Get-AzApiManagementApiSchema** Fixed getting Open-Api Schema associated with an API   https://github.com/Azure/azure-powershell/issues/10626</span></span>
* <span data-ttu-id="c16ab-1374">**New-AzApiManagementProduct** _ 및 _ *Set-AzApiManagementProduct*\*</span><span class="sxs-lookup"><span data-stu-id="c16ab-1374">**New-AzApiManagementProduct** _ and _ *Set-AzApiManagementProduct*\*</span></span>
  - <span data-ttu-id="c16ab-1375"> https://github.com/Azure/azure-powershell/issues/10472 설명서 수정</span><span class="sxs-lookup"><span data-stu-id="c16ab-1375">Fix documentation for https://github.com/Azure/azure-powershell/issues/10472</span></span>
* <span data-ttu-id="c16ab-1376">**Set-AzApiManagementApi** cmdlet을 사용하여 ServiceUrl을 업데이트하는 방법을 보여주는 예제 추가</span><span class="sxs-lookup"><span data-stu-id="c16ab-1376">**Set-AzApiManagementApi** Added example to show how to update the ServiceUrl using the cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="c16ab-1377">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="c16ab-1377">Az.Compute</span></span>
* <span data-ttu-id="c16ab-1378">VM 이름을 사용하지 않고 Get-AzVM -Status를 수행할 때 제한을 피하기 위해 VM 상태 수를 100개로 제한</span><span class="sxs-lookup"><span data-stu-id="c16ab-1378">Limit the number of VM status to 100 to avoid throttling when Get-AzVM -Status is performed without VM name.</span></span>
* <span data-ttu-id="c16ab-1379">Update-AzDiskEncryptionSet cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="c16ab-1379">Add Update-AzDiskEncryptionSet cmdlet</span></span>
* <span data-ttu-id="c16ab-1380">다음 cmdlet에 EncryptionType 및 DiskEncryptionSetId 매개 변수 추가:</span><span class="sxs-lookup"><span data-stu-id="c16ab-1380">Add EncryptionType and DiskEncryptionSetId parameters to the following cmdlets:</span></span>
    - <span data-ttu-id="c16ab-1381">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="c16ab-1381">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span></span>
* <span data-ttu-id="c16ab-1382">Get-AzProximityPlacementGroup cmdlet에 ColocationStatus 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="c16ab-1382">Add ColocationStatus parameter to Get-AzProximityPlacementGroup cmdlet.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="c16ab-1383">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="c16ab-1383">Az.DataFactory</span></span>
* <span data-ttu-id="c16ab-1384">ADF .Net SDK 버전을 4.7.0으로 업데이트</span><span class="sxs-lookup"><span data-stu-id="c16ab-1384">Update ADF .Net SDK version to 4.7.0</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="c16ab-1385">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="c16ab-1385">Az.DeploymentManager</span></span>
* <span data-ttu-id="c16ab-1386">리소스에 대한 LIST 작업 추가</span><span class="sxs-lookup"><span data-stu-id="c16ab-1386">Adds LIST operations for resources</span></span>
* <span data-ttu-id="c16ab-1387">상태 검사 단계에 대한 작업을 수행하는 기능 추가</span><span class="sxs-lookup"><span data-stu-id="c16ab-1387">Adds capability for performing operations on Health Check steps</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="c16ab-1388">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="c16ab-1388">Az.HDInsight</span></span>
* <span data-ttu-id="c16ab-1389">AzHDInsightCluster의 문서 오류 수정</span><span class="sxs-lookup"><span data-stu-id="c16ab-1389">Fix document error of New-AzHDInsightCluster.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="c16ab-1390">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="c16ab-1390">Az.KeyVault</span></span>
* <span data-ttu-id="c16ab-1391">Remove-AzureKeyVault가 새 New-AzureKeyVault와 일관성을 유지하도록 VaultName 특성에 이름 별칭 추가</span><span class="sxs-lookup"><span data-stu-id="c16ab-1391">Add Name alias to VaultName attribute to make Remove-AzureKeyVault consistent with New-AzureKeyVault.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="c16ab-1392">Az.Network</span><span class="sxs-lookup"><span data-stu-id="c16ab-1392">Az.Network</span></span>
* <span data-ttu-id="c16ab-1393">Set-AzNetworkWatcherConfigFlowLog.md에 트래픽 분석 사용 안 함 시나리오를 보여주는 새 예제 추가</span><span class="sxs-lookup"><span data-stu-id="c16ab-1393">New example added to Set-AzNetworkWatcherConfigFlowLog.md to demonstrate Traffic Analytics disable scenario.</span></span>
* <span data-ttu-id="c16ab-1394">Azure Firewall에 관리 IP 구성을 할당하는 지원 추가 - 방화벽에서 관리 트래픽에 사용할 전용 서브넷 및 공용 IP</span><span class="sxs-lookup"><span data-stu-id="c16ab-1394">Add support for assigning management IP configuration to Azure Firewall - a dedicated subnet and Public IP that the firewall will use for its management traffic</span></span>
    - <span data-ttu-id="c16ab-1395">New-AzFirewall cmdlet이 업데이트됨:</span><span class="sxs-lookup"><span data-stu-id="c16ab-1395">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="c16ab-1396">공용 IP 주소 개체를 허용하는 -ManagementPublicIpAddress 매개 변수(필수 아님) 추가</span><span class="sxs-lookup"><span data-stu-id="c16ab-1396">Added parameter -ManagementPublicIpAddress (not mandatory) which accepts a Public IP Address object</span></span>
        - <span data-ttu-id="c16ab-1397">방화벽 개체에 SetManagementIpConfiguration 메서드 추가 - 입력으로 서브넷 및 공용 IP 주소 필요 - 서브넷 이름은 'AzureFirewallManagementSubnet'이어야 함</span><span class="sxs-lookup"><span data-stu-id="c16ab-1397">Added method SetManagementIpConfiguration on firewall object - requires a subnet and a Public IP address as input - subnet name must be 'AzureFirewallManagementSubnet'</span></span>
* <span data-ttu-id="c16ab-1398">네트워크 인터페이스 대신 NSG 예제를 보여주도록 AzNetworkSecurityGroup 예제 수정</span><span class="sxs-lookup"><span data-stu-id="c16ab-1398">Corrected Get-AzNetworkSecurityGroup examples to show examples for NSG's instead of network interfaces.</span></span>
* <span data-ttu-id="c16ab-1399">리소스 id 완성자가 매개 변수를 완성하지 못하게 방해하던 New-AzVpnSite 명령의 오타 수정</span><span class="sxs-lookup"><span data-stu-id="c16ab-1399">Fixed typo in New-AzVpnSite command that was preventing resource id completer from completing a parameter.</span></span>
* <span data-ttu-id="c16ab-1400">Application Gateway의 다시 쓰기 규칙 작업 세트에서 Url 구성에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="c16ab-1400">Added support for Url Confiugration in Rewrite Rules Action Set in the Application Gateway</span></span>
    - <span data-ttu-id="c16ab-1401">추가된 새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1401">New cmdlets added:</span></span>
        - <span data-ttu-id="c16ab-1402">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="c16ab-1402">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span></span>
    - <span data-ttu-id="c16ab-1403">선택적 매개 변수를 사용하도록 Cmdlet 업데이트 - UrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="c16ab-1403">Cmdlets updated with optional parameter - UrlConfiguration</span></span>
        - <span data-ttu-id="c16ab-1404">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="c16ab-1404">New-AzApplicationGatewayRewriteRuleActionSet</span></span>
* <span data-ttu-id="c16ab-1405">NetworkWatcher ConnectionMonitor 버전 2 리소스에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="c16ab-1405">Add suppport for NetworkWatcher ConnectionMonitor version 2 resources</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="c16ab-1406">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="c16ab-1406">Az.PolicyInsights</span></span>
* <span data-ttu-id="c16ab-1407">수정할 리소스를 결정하기 전에 규정 준수 평가 지원</span><span class="sxs-lookup"><span data-stu-id="c16ab-1407">Support evaluating compliance prior to determining what resource to remediate</span></span>
    - <span data-ttu-id="c16ab-1408">Start-AzPolicyRemediation에 '-ResourceDiscoverMode' 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="c16ab-1408">Add '-ResourceDiscoverMode' parameter to Start-AzPolicyRemediation</span></span>
* <span data-ttu-id="c16ab-1409">정책 메타데이터 리소스를 가져오는 Get-AzPolicyMetadata cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="c16ab-1409">Add Get-AzPolicyMetadata cmdlet for getting policy metadata resources</span></span>
* <span data-ttu-id="c16ab-1410">API 버전 2019-10-01의 Get-AzPolicyState 및 Get-AzPolicyStateSummary 업데이트</span><span class="sxs-lookup"><span data-stu-id="c16ab-1410">Updated Get-AzPolicyState and Get-AzPolicyStateSummary for API version 2019-10-01</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="c16ab-1411">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="c16ab-1411">Az.RecoveryServices</span></span>
* <span data-ttu-id="c16ab-1412">복제된 디스크를 제거할 수 있도록 Azure Site Recovery에 지원 추가</span><span class="sxs-lookup"><span data-stu-id="c16ab-1412">Azure Site Recovery support for removing a replicated disk.</span></span>
* <span data-ttu-id="c16ab-1413">Recovery Services 자격 증명 모음을 만드는 동안 태그를 추가할 수 있도록 Azure Backup에 지원 추가</span><span class="sxs-lookup"><span data-stu-id="c16ab-1413">Azure Backup added support for adding tags while creating a Recovery Services Vault.</span></span>

#### <a name="azresources"></a><span data-ttu-id="c16ab-1414">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="c16ab-1414">Az.Resources</span></span>
* <span data-ttu-id="c16ab-1415">컨텍스트 구독을 기본값으로 하는 \*-AzPolicyAssignment cmdlet에서 -Scope를 선택 사항으로 설정</span><span class="sxs-lookup"><span data-stu-id="c16ab-1415">Make -Scope optional in \*-AzPolicyAssignment cmdlets with default to context subscription</span></span>
* <span data-ttu-id="c16ab-1416">암호 및 키 자격 증명을 사용하여 ADServicePrincipal을 만드는 예제 추가</span><span class="sxs-lookup"><span data-stu-id="c16ab-1416">Add examples of creating ADServicePrincipal with password and key credential</span></span>

#### <a name="azsql"></a><span data-ttu-id="c16ab-1417">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="c16ab-1417">Az.Sql</span></span>
<span data-ttu-id="c16ab-1418">DatabaseName 대신 PartnerDatabaseName이 있는지 확인하도록 New-AzSqlDatabaseSecondary cmdlet 수정</span><span class="sxs-lookup"><span data-stu-id="c16ab-1418">Fix New-AzSqlDatabaseSecondary cmdlet to check for PartnerDatabaseName existence instead of DatabaseName existence.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="c16ab-1419">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="c16ab-1419">Az.Storage</span></span>
* <span data-ttu-id="c16ab-1420">스토리지 계정 만들기에서 테이블/큐 암호화 Keytype 설정 지원</span><span class="sxs-lookup"><span data-stu-id="c16ab-1420">Support set Table/Queue Encryption Keytype in Create Storage Account</span></span>
    - <span data-ttu-id="c16ab-1421">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="c16ab-1421">New-AzStorageAccount</span></span>
* <span data-ttu-id="c16ab-1422">StorageException에 ExtendedErrorInformation이 없으면 RequestId 표시</span><span class="sxs-lookup"><span data-stu-id="c16ab-1422">Show RequestId when StorageException don't have ExtendedErrorInformation</span></span>
* <span data-ttu-id="c16ab-1423">cmdlet Start-AzStorageBlobCopy의 예제 6 수정</span><span class="sxs-lookup"><span data-stu-id="c16ab-1423">Fix the Example 6 of cmdlet Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="c16ab-1424">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="c16ab-1424">Az.Websites</span></span>
* <span data-ttu-id="c16ab-1425">Set-AzWebapp 및 Set-AzWebappSlot이 AlwaysOn, MinTls 및 FtpsState 속성 지원</span><span class="sxs-lookup"><span data-stu-id="c16ab-1425">Set-AzWebapp and Set-AzWebappSlot supports AlwaysOn, MinTls and FtpsState properties</span></span>
* <span data-ttu-id="c16ab-1426">단일 Set-AzWebApp 명령을 사용하여 AppservicePlan을 변경하는 동시에 HttpsOnly를 설정하면 HttpsOnly가 기본값으로 다시 설정되는 문제 수정</span><span class="sxs-lookup"><span data-stu-id="c16ab-1426">Fixing issue where setting HttpsOnly along with changing AppservicePlan at the same time using the single Set-AzWebApp Command, was resetting HttpsOnly to default value</span></span>

## <a name="330---january-2020"></a><span data-ttu-id="c16ab-1427">3.3.0 - 2020년 1월</span><span class="sxs-lookup"><span data-stu-id="c16ab-1427">3.3.0 - January 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="c16ab-1428">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="c16ab-1428">Az.Accounts</span></span>
* <span data-ttu-id="c16ab-1429">AzureAttestationServiceEndpointResourceId 및 AzureAttestationServiceEndpointSuffix 매개 변수를 허용하도록 Add-AzEnvironment 및 Set-AzEnvironment가 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="c16ab-1429">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameters AzureAttestationServiceEndpointResourceId and AzureAttestationServiceEndpointSuffix</span></span>

#### <a name="azcdn"></a><span data-ttu-id="c16ab-1430">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="c16ab-1430">Az.Cdn</span></span>
* <span data-ttu-id="c16ab-1431">New-AzCdnEndpoint cmdlet에서 오류 응답 세부 정보 표시</span><span class="sxs-lookup"><span data-stu-id="c16ab-1431">Display error response detail in New-AzCdnEndpoint cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="c16ab-1432">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="c16ab-1432">Az.Compute</span></span>
* <span data-ttu-id="c16ab-1433">OS 프로필이 없는 관리 OD 디스크가 있는 VM의 Set-AzVMCustomScriptExtension cmdlet을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1433">Fix Set-AzVMCustomScriptExtension cmdlet for a VM with managed OD disk which does not have OS profile.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="c16ab-1434">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="c16ab-1434">Az.ContainerInstance</span></span>
* <span data-ttu-id="c16ab-1435">New-AzContainerGroup의 예에서 사용되는 고정 매개 변수 이름</span><span class="sxs-lookup"><span data-stu-id="c16ab-1435">Fixed parameter names used by example of New-AzContainerGroup</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="c16ab-1436">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="c16ab-1436">Az.DataBoxEdge</span></span>
* <span data-ttu-id="c16ab-1437">'Get-AzDataBoxEdgeStorageContainer' cmdlet 추가됨</span><span class="sxs-lookup"><span data-stu-id="c16ab-1437">Added cmdlet 'Get-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="c16ab-1438">Edge 스토리지 컨테이너 가져오기</span><span class="sxs-lookup"><span data-stu-id="c16ab-1438">Get the Edge Storage Container</span></span>
* <span data-ttu-id="c16ab-1439">'New-AzDataBoxEdgeStorageContainer' cmdlet 추가됨</span><span class="sxs-lookup"><span data-stu-id="c16ab-1439">Added cmdlet 'New-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="c16ab-1440">새 Edge 스토리지 컨테이너 만들기</span><span class="sxs-lookup"><span data-stu-id="c16ab-1440">Create new Edge Strorage Container</span></span>
* <span data-ttu-id="c16ab-1441">'Remove-AzDataBoxEdgeStorageContainer' cmdlet 추가됨</span><span class="sxs-lookup"><span data-stu-id="c16ab-1441">Added cmdlet 'Remove-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="c16ab-1442">Edge 스토리지 컨테이너 제거</span><span class="sxs-lookup"><span data-stu-id="c16ab-1442">Remove the Edge Storage Container</span></span>
* <span data-ttu-id="c16ab-1443">'Invoke-AzDataBoxEdgeStorageContainer' cmdlet 추가됨</span><span class="sxs-lookup"><span data-stu-id="c16ab-1443">Added cmdlet 'Invoke-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="c16ab-1444">Edge 스토리지 컨테이너에서 데이터를 새로 고치는 작업 호출</span><span class="sxs-lookup"><span data-stu-id="c16ab-1444">Invoke action to refresh data on Edge Storage Container</span></span>
* <span data-ttu-id="c16ab-1445">'Get-AzDataBoxEdgeStorageAccount' cmdlet 추가됨</span><span class="sxs-lookup"><span data-stu-id="c16ab-1445">Added cmdlet 'Get-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="c16ab-1446">Edge 스토리지 계정 가져오기</span><span class="sxs-lookup"><span data-stu-id="c16ab-1446">Get the Edge Storage Account</span></span>
* <span data-ttu-id="c16ab-1447">'New-AzDataBoxEdgeStorageAccount' cmdlet 추가됨</span><span class="sxs-lookup"><span data-stu-id="c16ab-1447">Added cmdlet 'New-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="c16ab-1448">새 Edge 스토리지 계정 만들기</span><span class="sxs-lookup"><span data-stu-id="c16ab-1448">Create new Edge Storage Account</span></span>
* <span data-ttu-id="c16ab-1449">'Remove-AzDataBoxEdgeStorageAccount' cmdlet 추가됨</span><span class="sxs-lookup"><span data-stu-id="c16ab-1449">Added cmdlet 'Remove-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="c16ab-1450">Edge 스토리지 계정 제거</span><span class="sxs-lookup"><span data-stu-id="c16ab-1450">Remove the Edge Storage Account</span></span>
* <span data-ttu-id="c16ab-1451">'Invoke-AzDataBoxEdgeShare' cmdlet 호출</span><span class="sxs-lookup"><span data-stu-id="c16ab-1451">Invoke cmdlet 'Invoke-AzDataBoxEdgeShare'</span></span>
  - <span data-ttu-id="c16ab-1452">공유에서 데이터를 새로 고치는 작업 호출</span><span class="sxs-lookup"><span data-stu-id="c16ab-1452">Invoke action to refresh data on share</span></span>
* <span data-ttu-id="c16ab-1453">'Set-AzDataBoxEdgeStorageAccountCredential' cmdlet 추가됨</span><span class="sxs-lookup"><span data-stu-id="c16ab-1453">Added cmdlet 'Set-AzDataBoxEdgeStorageAccountCredential'</span></span>
  - <span data-ttu-id="c16ab-1454">az databoxedge 스토리지 계정 자격 증명 설정</span><span class="sxs-lookup"><span data-stu-id="c16ab-1454">Set the az databoxedge storage account credential</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="c16ab-1455">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="c16ab-1455">Az.DataFactory</span></span>
* <span data-ttu-id="c16ab-1456">Get-AzDataFactoryV2IntegrationRuntime cmd에 AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId 및 VersionStatus 속성 추가</span><span class="sxs-lookup"><span data-stu-id="c16ab-1456">Add AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId and VersionStatus properties for Get-AzDataFactoryV2IntegrationRuntime cmd</span></span>
* <span data-ttu-id="c16ab-1457">ADF .Net SDK 버전을 4.6.0으로 업데이트</span><span class="sxs-lookup"><span data-stu-id="c16ab-1457">Update ADF .Net SDK version to 4.6.0</span></span>
* <span data-ttu-id="c16ab-1458">고정 공용 IP 주소로 Azure-SSIS IR을 만들 수 있도록 'Set-AzureRmDataFactoryV2IntegrationRuntime'cmd에 대해 'PublicIPs' 매개 변수를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1458">Add parameter 'PublicIPs' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable create Azure-SSIS IR with static public IP addresses.</span></span>

#### <a name="azdevtestlabs"></a><span data-ttu-id="c16ab-1459">Az.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="c16ab-1459">Az.DevTestLabs</span></span>
* <span data-ttu-id="c16ab-1460">Get-AzDtlAllowedVMSizesPolicy.md에서 끊어진 링크 제거</span><span class="sxs-lookup"><span data-stu-id="c16ab-1460">Remove the broken link in Get-AzDtlAllowedVMSizesPolicy.md</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="c16ab-1461">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="c16ab-1461">Az.EventHub</span></span>
* <span data-ttu-id="c16ab-1462">10634 문제 해결: eventhubnamespace 제거에 대한 null 개체 참조 수정</span><span class="sxs-lookup"><span data-stu-id="c16ab-1462">Fix for issue 10634 : Fix the null Object reference for remove eventhubnamespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="c16ab-1463">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="c16ab-1463">Az.HDInsight</span></span>
* <span data-ttu-id="c16ab-1464">Invoke-AzHDInsightHiveJob.md 오류를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1464">Fix Invoke-AzHDInsightHiveJob.md error.</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="c16ab-1465">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="c16ab-1465">Az.MachineLearning</span></span>
* <span data-ttu-id="c16ab-1466">MachineLearningCompute를 더 이상 사용할 수 없게 되어 아래 cmdlet이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1466">Removed below cmdlets because MachineLearningCompute is not available any longer</span></span>
  - <span data-ttu-id="c16ab-1467">Get-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="c16ab-1467">Get-AzMlOpCluster</span></span>
  - <span data-ttu-id="c16ab-1468">Get-AzMlOpClusterKey</span><span class="sxs-lookup"><span data-stu-id="c16ab-1468">Get-AzMlOpClusterKey</span></span>
  - <span data-ttu-id="c16ab-1469">New-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="c16ab-1469">New-AzMlOpCluster</span></span>
  - <span data-ttu-id="c16ab-1470">Remove-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="c16ab-1470">Remove-AzMlOpCluster</span></span>
  - <span data-ttu-id="c16ab-1471">Set-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="c16ab-1471">Set-AzMlOpCluster</span></span>
  - <span data-ttu-id="c16ab-1472">Test-AzMlOpClusterSystemServicesUpdateAvailability</span><span class="sxs-lookup"><span data-stu-id="c16ab-1472">Test-AzMlOpClusterSystemServicesUpdateAvailability</span></span>
  - <span data-ttu-id="c16ab-1473">Update-AzMlOpClusterSystemService</span><span class="sxs-lookup"><span data-stu-id="c16ab-1473">Update-AzMlOpClusterSystemService</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="c16ab-1474">Az.Network</span><span class="sxs-lookup"><span data-stu-id="c16ab-1474">Az.Network</span></span>
* <span data-ttu-id="c16ab-1475">Microsoft.Azure.Management.Sql의 종속성을 1.36-preview에서 1.37-preview로 업그레이드</span><span class="sxs-lookup"><span data-stu-id="c16ab-1475">Upgrade dependency of Microsoft.Azure.Management.Sql from 1.36-preview to 1.37-preview</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="c16ab-1476">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="c16ab-1476">Az.RecoveryServices</span></span>
* <span data-ttu-id="c16ab-1477">Azure Site Recovery는 Azure 간 공급자를 위해 고객 관리 키와 함께 유휴 상태에서 암호화된 관리 디스크 vms의 변경을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1477">Azure Site Recovery change support for managed disk vms encrypted at rest with customer managed keys for Azure to Azure provider.</span></span>
* <span data-ttu-id="c16ab-1478">Azure Site Recovery는 VMware에서 Azure로를 위해 보호를 사용할 때 선택적 입력으로서 디스크 암호화 집합 ID를 입력하도록 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1478">Azure Site Recovery support to input disk encryption Set Id as optional input at enabling protection for Vmware to Azure.</span></span>
* <span data-ttu-id="c16ab-1479">Azure Site Recovery는 VMware에서 Azure로를 위해 보호를 사용하기 위해 디스크 수준의 선택적 입력으로서 디스크 암호화 집합 ID를 입력하도록 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1479">Azure Site Recovery support to input disk encryption Set Id as optional input at disk level to enable protection for Vmware to Azure.</span></span>
* <span data-ttu-id="c16ab-1480">Azure Site Recovery는 HyperV에서 Azure로를 위해 디스크 암호화 집합 맵을 사용하여 복제 보호된 항목을 업데이트하도록 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1480">Azure Site Recovery support to update replication protected item with disk encryption set Map for HyperV to Azure.</span></span>

#### <a name="azresources"></a><span data-ttu-id="c16ab-1481">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="c16ab-1481">Az.Resources</span></span>
* <span data-ttu-id="c16ab-1482">'Remove-AzTag'의 도움말 문서에서 오류를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1482">Fix an error in help document of 'Remove-AzTag'.</span></span>

#### <a name="azsql"></a><span data-ttu-id="c16ab-1483">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="c16ab-1483">Az.Sql</span></span>
* <span data-ttu-id="c16ab-1484">Azure Database의 마스터 DB에서 작동하도록 취약성 평가 세트 기준 cmdlet 기능을 수정하고 관리형 인스턴스 시스템 데이터베이스에서 이를 제한합니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1484">Fix vulnerability assessment set baseline cmdlets functionality to work on master db for azure database and limit it on managed instance system databases.</span></span>
* <span data-ttu-id="c16ab-1485">SQL 인스턴스 장애 조치(failover) 그룹을 만들 때 오류 수정</span><span class="sxs-lookup"><span data-stu-id="c16ab-1485">Fix an error when creating SQL instance failover group</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="c16ab-1486">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="c16ab-1486">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="c16ab-1487">올바른 새 라이선스 형식으로 DR 추가</span><span class="sxs-lookup"><span data-stu-id="c16ab-1487">Add DR as a new valid License type</span></span>

#### <a name="azstorage"></a><span data-ttu-id="c16ab-1488">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="c16ab-1488">Az.Storage</span></span>
* <span data-ttu-id="c16ab-1489">다음 릴리스에서 DefaultAction Value 변경에 대해 호환성이 손상되는 변경 경고 메시지 추가</span><span class="sxs-lookup"><span data-stu-id="c16ab-1489">Add breaking change warning message for DefaultAction Value change in a future release</span></span>
    - <span data-ttu-id="c16ab-1490">Update-AzStorageAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="c16ab-1490">Update-AzStorageAccountNetworkRuleSet</span></span>
* <span data-ttu-id="c16ab-1491">-IncludeGeoReplicationStats 매개 변수와 함께 get-AzureRMStorageAccount를 실행하여 스토리지 계정의 마지막 동기화 시간 가져오기 지원</span><span class="sxs-lookup"><span data-stu-id="c16ab-1491">Support Get last sync time of Storage account by run get-AzureRMStorageAccount with parameter -IncludeGeoReplicationStats</span></span>
    - <span data-ttu-id="c16ab-1492">Get-AzureRMStorageAccount</span><span class="sxs-lookup"><span data-stu-id="c16ab-1492">Get-AzureRMStorageAccount</span></span>

## <a name="320---december-2019"></a><span data-ttu-id="c16ab-1493">3.2.0 - 2019년 12월</span><span class="sxs-lookup"><span data-stu-id="c16ab-1493">3.2.0 - December 2019</span></span>

### <a name="general"></a><span data-ttu-id="c16ab-1494">일반</span><span class="sxs-lookup"><span data-stu-id="c16ab-1494">General</span></span>
* <span data-ttu-id="c16ab-1495">모든 모듈의 상대 경로를 사용하기 위해 .psd1의 참조 업데이트</span><span class="sxs-lookup"><span data-stu-id="c16ab-1495">Update references in .psd1 to use relative path for all modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="c16ab-1496">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="c16ab-1496">Az.Accounts</span></span>
* <span data-ttu-id="c16ab-1497">Az 4.0 미리 보기를 위해 클라이언트 측 원격 분석에 대해 UserAgent를 올바르게 설정</span><span class="sxs-lookup"><span data-stu-id="c16ab-1497">Set correct UserAgent for client-side telemetry for Az 4.0 preview</span></span>
* <span data-ttu-id="c16ab-1498">Az 4.0 미리 보기에서 컨텍스트가 null인 경우 사용자에게 친숙한 오류 메시지로 표시</span><span class="sxs-lookup"><span data-stu-id="c16ab-1498">Display user friendly error message when context is null in Az 4.0 preview</span></span>

#### <a name="azbatch"></a><span data-ttu-id="c16ab-1499">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="c16ab-1499">Az.Batch</span></span>
* <span data-ttu-id="c16ab-1500">**New-AzBatchPool** 이 'VirtualMachineConfiguration.ContainerConfiguration' 또는 'VirtualMachineConfiguration.DataDisks'를 서버로 제대로 보내지 않는 [#10602](https://github.com/Azure/azure-powershell/issues/10602) 문제 수정</span><span class="sxs-lookup"><span data-stu-id="c16ab-1500">Fix issue [#10602](https://github.com/Azure/azure-powershell/issues/10602), where **New-AzBatchPool** did not properly send 'VirtualMachineConfiguration.ContainerConfiguration' or 'VirtualMachineConfiguration.DataDisks' to the server.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="c16ab-1501">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="c16ab-1501">Az.DataFactory</span></span>
* <span data-ttu-id="c16ab-1502">ADF .Net SDK 버전을 4.5.0으로 업데이트</span><span class="sxs-lookup"><span data-stu-id="c16ab-1502">Update ADF .Net SDK version to 4.5.0</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="c16ab-1503">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="c16ab-1503">Az.FrontDoor</span></span>
* <span data-ttu-id="c16ab-1504">WAF 관리 규칙 제외 지원 추가됨</span><span class="sxs-lookup"><span data-stu-id="c16ab-1504">Added WAF managed rules exclusion support</span></span>
* <span data-ttu-id="c16ab-1505">자동 완성에 SocketAddr 추가</span><span class="sxs-lookup"><span data-stu-id="c16ab-1505">Add SocketAddr to auto-complete</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="c16ab-1506">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="c16ab-1506">Az.HealthcareApis</span></span>
* <span data-ttu-id="c16ab-1507">예외 처리</span><span class="sxs-lookup"><span data-stu-id="c16ab-1507">Exception Handling</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="c16ab-1508">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="c16ab-1508">Az.KeyVault</span></span>
* <span data-ttu-id="c16ab-1509">잠재적으로 설정되지 않은 오류 액세스 값 수정</span><span class="sxs-lookup"><span data-stu-id="c16ab-1509">Fixed error accessing value that is potentially not set</span></span>
* <span data-ttu-id="c16ab-1510">타원 곡선 암호화 인증서 관리</span><span class="sxs-lookup"><span data-stu-id="c16ab-1510">Elliptic Curve Cryptography Certificate Managment</span></span>
    - <span data-ttu-id="c16ab-1511">인증서 정책에 대한 곡선 지정을 위한 지원 추가됨</span><span class="sxs-lookup"><span data-stu-id="c16ab-1511">Added support to specify the Curve for Certificate Policies</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="c16ab-1512">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="c16ab-1512">Az.Monitor</span></span>
* <span data-ttu-id="c16ab-1513">진단 설정 추가 명령에 선택적 인수 추가</span><span class="sxs-lookup"><span data-stu-id="c16ab-1513">Adding optional argument to the Add Diagnostic Settings command.</span></span> <span data-ttu-id="c16ab-1514">스위치 인수(있는 경우)는 Log Analytics로 내보내기가 고정 스키마(전용 데이터 유형)가 되어야 함을</span><span class="sxs-lookup"><span data-stu-id="c16ab-1514">A switch argument that if present indicates that the export to Log Analytics must be to a fixed schema (a.k.a.</span></span> <span data-ttu-id="c16ab-1515">나타냄</span><span class="sxs-lookup"><span data-stu-id="c16ab-1515">dedicated, data type)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="c16ab-1516">Az.Network</span><span class="sxs-lookup"><span data-stu-id="c16ab-1516">Az.Network</span></span>
* <span data-ttu-id="c16ab-1517">AzureFirewall 애플리케이션, NAT 및 네트워크 규칙에서 IpGroups 지원.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1517">Support for IpGroups in AzureFirewall Application,Nat & Network Rules.</span></span>

#### <a name="azresources"></a><span data-ttu-id="c16ab-1518">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="c16ab-1518">Az.Resources</span></span>
* <span data-ttu-id="c16ab-1519">이름이 일부 내장 매개 변수 이름과 충돌하는 경우 템플릿 배포가 템플릿 매개 변수를 읽지 못하는 문제 수정.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1519">Fix an issue where template deployment fails to read a template parameter if its name conflicts with some built-in parameter name.</span></span>
* <span data-ttu-id="c16ab-1520">정책 세트 정의 내에 그룹화 지원을 도입하는 새로운 API 버전 2019-09-01을 사용하도록 정책 cmdlet 업데이트.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1520">Updated policy cmdlets to use new api version 2019-09-01 that introduces grouping support within policy set definitions.</span></span>

#### <a name="azsql"></a><span data-ttu-id="c16ab-1521">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="c16ab-1521">Az.Sql</span></span>
* <span data-ttu-id="c16ab-1522">취약성 평가 자동 활성화에서 스토리지 생성을 StorageV2로 업그레이드</span><span class="sxs-lookup"><span data-stu-id="c16ab-1522">Upgraded storage creation in Vulnerability Assessment auto enablement to StorageV2</span></span>

#### <a name="azstorage"></a><span data-ttu-id="c16ab-1523">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="c16ab-1523">Az.Storage</span></span>
* <span data-ttu-id="c16ab-1524">Oauth 인증을 기반으로 스토리지 컨텍스트를 사용하여 Blob/컨테이너 ID 기반 SAS 토큰 생성 지원</span><span class="sxs-lookup"><span data-stu-id="c16ab-1524">Support generate Blob/Constainer Idenity based SAS token with Storage Context based on Oauth authentication</span></span>
    - <span data-ttu-id="c16ab-1525">New-AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="c16ab-1525">New-AzStorageContainerSASToken</span></span>
    - <span data-ttu-id="c16ab-1526">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="c16ab-1526">New-AzStorageBlobSASToken</span></span>
* <span data-ttu-id="c16ab-1527">모든 Idenity SAS 토큰을 해지할 수 있도록 스토리지 계정 사용자 위임 키 해지 지원</span><span class="sxs-lookup"><span data-stu-id="c16ab-1527">Support revoke Storage Account User Delegation Keys, so all Idenity SAS tokens are revoked</span></span>
    - <span data-ttu-id="c16ab-1528">Revoke-AzStorageAccountUserDelegationKeys</span><span class="sxs-lookup"><span data-stu-id="c16ab-1528">Revoke-AzStorageAccountUserDelegationKeys</span></span>
* <span data-ttu-id="c16ab-1529">새로운 API 버전 2019-06-01을 지원하기 위해 Microsoft.Azure.Management.Storage 14.2.0으로 업그레이드.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1529">Upgrade to Microsoft.Azure.Management.Storage 14.2.0, to support new API version 2019-06-01.</span></span>
* <span data-ttu-id="c16ab-1530">File Share cmdlet의 관리 평면에서 5120을 초과하는 값에 대해 QuotaGiB(Gibyby의 공유 할당량)를 지원하고 'Quota' 매개 변수 별칭을 'QuotaGiB' 매개 변수에 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1530">Support of QuotaGiB (Share Quota in Gibibye) for values of more than 5120 in the Management plane of File Share cmdlets and added the 'Quota' parameter alias to the 'QuotaGiB' parameter.</span></span>
    - <span data-ttu-id="c16ab-1531">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="c16ab-1531">New-AzRmStorageShare</span></span>
    - <span data-ttu-id="c16ab-1532">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="c16ab-1532">Update-AzRmStorageShare</span></span>
* <span data-ttu-id="c16ab-1533">매개 변수 'Quota'에 매개 변수 별칭 'QuotaGiB' 추가</span><span class="sxs-lookup"><span data-stu-id="c16ab-1533">Add parameter alias 'QuotaGiB' to parameter 'Quota'</span></span>
    - <span data-ttu-id="c16ab-1534">Set-AzStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="c16ab-1534">Set-AzStorageShareQuota</span></span>
* <span data-ttu-id="c16ab-1535">Set-AzStorageContainerAcl가 저장된 액세스 정책을 정리할 수 있는 문제 수정</span><span class="sxs-lookup"><span data-stu-id="c16ab-1535">Fix the issue that Set-AzStorageContainerAcl can clean up the stored Access Policy</span></span>
    - <span data-ttu-id="c16ab-1536">Set-AzStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="c16ab-1536">Set-AzStorageContainerAcl</span></span>

## <a name="310---november-2019"></a><span data-ttu-id="c16ab-1537">3.1.0 - 2019년 11월</span><span class="sxs-lookup"><span data-stu-id="c16ab-1537">3.1.0 - November 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="c16ab-1538">마지막 주 릴리스 이후의 주요 사항</span><span class="sxs-lookup"><span data-stu-id="c16ab-1538">Highlights since the last major release</span></span>
* <span data-ttu-id="c16ab-1539">Az.DataBoxEdge 1.0.0 릴리스됨</span><span class="sxs-lookup"><span data-stu-id="c16ab-1539">Az.DataBoxEdge 1.0.0 released</span></span>
* <span data-ttu-id="c16ab-1540">Az.SqlVirtualMachine 1.0.0 릴리스됨</span><span class="sxs-lookup"><span data-stu-id="c16ab-1540">Az.SqlVirtualMachine 1.0.0 released</span></span>

#### <a name="azcompute"></a><span data-ttu-id="c16ab-1541">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="c16ab-1541">Az.Compute</span></span>
* <span data-ttu-id="c16ab-1542">VM Reapply 기능</span><span class="sxs-lookup"><span data-stu-id="c16ab-1542">VM Reapply feature</span></span>
    - <span data-ttu-id="c16ab-1543">Set-AzVM cmdlet에 Reapply 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="c16ab-1543">Add Reapply parameter to Set-AzVM cmdlet</span></span>
* <span data-ttu-id="c16ab-1544">VM 확장 집합 AutomaticRepairs 기능:</span><span class="sxs-lookup"><span data-stu-id="c16ab-1544">VM Scale Set AutomaticRepairs feature:</span></span>
    - <span data-ttu-id="c16ab-1545">다음 cmdlet에 EnableAutomaticRepair, AutomaticRepairGracePeriod 및 AutomaticRepairMaxInstanceRepairsPercent 매개 변수를 추가합니다.   New-AzVmssConfig   Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="c16ab-1545">Add EnableAutomaticRepair, AutomaticRepairGracePeriod, and AutomaticRepairMaxInstanceRepairsPercent parameters to the following cmdlets:   New-AzVmssConfig   Update-AzVmss</span></span>
* <span data-ttu-id="c16ab-1546">New-AzVM에 대한 교차 테넌트 갤러리 이미지 지원</span><span class="sxs-lookup"><span data-stu-id="c16ab-1546">Cross tenant gallery image support for New-AzVM</span></span>
* <span data-ttu-id="c16ab-1547">New-AzVM, New-AzVMConfig 및 New-AzVmss cmdlet의 Priority 매개 변수의 인수 완성자에 'Spot' 추가</span><span class="sxs-lookup"><span data-stu-id="c16ab-1547">Add 'Spot' to the argument completer of Priority parameter in New-AzVM, New-AzVMConfig and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="c16ab-1548">Add-AzVmssDataDisk cmdlet에 DiskIOPSReadWrite 및 DiskMBpsReadWrite 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="c16ab-1548">Add DiskIOPSReadWrite and DiskMBpsReadWrite parameters to Add-AzVmssDataDisk cmdlet</span></span>
* <span data-ttu-id="c16ab-1549">New-AzGalleryImageVersion cmdlet의 SourceImageId 매개 변수를 선택 사항으로 변경</span><span class="sxs-lookup"><span data-stu-id="c16ab-1549">Change SourceImageId parameter of New-AzGalleryImageVersion cmdlet to optional</span></span>
* <span data-ttu-id="c16ab-1550">New-AzGalleryImageVersion cmdlet에 OSDiskImage 및 DataDiskImage 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="c16ab-1550">Add OSDiskImage and DataDiskImage parameters to New-AzGalleryImageVersion cmdlet</span></span>
* <span data-ttu-id="c16ab-1551">New-AzGalleryImageDefinition cmdlet에 HyperVGeneration 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="c16ab-1551">Add HyperVGeneration parameter to New-AzGalleryImageDefinition cmdlet</span></span>
* <span data-ttu-id="c16ab-1552">New-AzVmss, New-AzVmssConfig 및 Update-AzVmss cmdlet에 SkipExtensionsOnOverprovisionedVMs 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="c16ab-1552">Add SkipExtensionsOnOverprovisionedVMs parameters to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="c16ab-1553">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="c16ab-1553">Az.DataBoxEdge</span></span>
* <span data-ttu-id="c16ab-1554">cmdlet `Get-AzDataBoxEdgeOrder` 추가됨</span><span class="sxs-lookup"><span data-stu-id="c16ab-1554">Added cmdlet `Get-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="c16ab-1555">주문 가져오기</span><span class="sxs-lookup"><span data-stu-id="c16ab-1555">Get the Order</span></span>
* <span data-ttu-id="c16ab-1556">cmdlet `New-AzDataBoxEdgeOrder` 추가됨</span><span class="sxs-lookup"><span data-stu-id="c16ab-1556">Added cmdlet `New-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="c16ab-1557">새 주문 만들기</span><span class="sxs-lookup"><span data-stu-id="c16ab-1557">Create new Order</span></span>
* <span data-ttu-id="c16ab-1558">cmdlet `Remove-AzDataBoxEdgeOrder` 추가됨</span><span class="sxs-lookup"><span data-stu-id="c16ab-1558">Added cmdlet `Remove-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="c16ab-1559">주문 제거</span><span class="sxs-lookup"><span data-stu-id="c16ab-1559">Remove the Order</span></span>
* <span data-ttu-id="c16ab-1560">cmdlet `New-AzDataBoxEdgeShare` 변경</span><span class="sxs-lookup"><span data-stu-id="c16ab-1560">Change in cmdlet `New-AzDataBoxEdgeShare`</span></span>
    - <span data-ttu-id="c16ab-1561">이제 로컬 공유를 만듬</span><span class="sxs-lookup"><span data-stu-id="c16ab-1561">Now creates Local Share</span></span>
* <span data-ttu-id="c16ab-1562">cmdlet `Set-AzDataBoxEdgeRole` 추가됨</span><span class="sxs-lookup"><span data-stu-id="c16ab-1562">Added cmdlet `Set-AzDataBoxEdgeRole`</span></span>
    - <span data-ttu-id="c16ab-1563">이제 IotRole을 공유에 매핑할 수 있음</span><span class="sxs-lookup"><span data-stu-id="c16ab-1563">Now IotRole can be mapped to Share</span></span>
* <span data-ttu-id="c16ab-1564">cmdlet `Invoke-AzDataBoxEdgeDevice` 추가됨</span><span class="sxs-lookup"><span data-stu-id="c16ab-1564">Added cmdlet `Invoke-AzDataBoxEdgeDevice`</span></span>
    - <span data-ttu-id="c16ab-1565">스캔 업데이트 호출, 업데이트 다운로드, 디바이스에 업데이트 설치</span><span class="sxs-lookup"><span data-stu-id="c16ab-1565">Invoke scan update, download update, install updates on the device</span></span>
* <span data-ttu-id="c16ab-1566">cmdlet `Get-AzDataBoxEdgeTrigger` 추가됨</span><span class="sxs-lookup"><span data-stu-id="c16ab-1566">Added cmdlet `Get-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="c16ab-1567">트리거에 대한 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="c16ab-1567">Gets the information about Triggers</span></span>
* <span data-ttu-id="c16ab-1568">cmdlet `New-AzDataBoxEdgeTrigger` 추가됨</span><span class="sxs-lookup"><span data-stu-id="c16ab-1568">Added cmdlet `New-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="c16ab-1569">새 트리거 만들기</span><span class="sxs-lookup"><span data-stu-id="c16ab-1569">Create new Triggers</span></span>
* <span data-ttu-id="c16ab-1570">cmdlet `Remove-AzDataBoxEdgeTrigger` 추가됨</span><span class="sxs-lookup"><span data-stu-id="c16ab-1570">Added cmdlet `Remove-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="c16ab-1571">트리거 제거</span><span class="sxs-lookup"><span data-stu-id="c16ab-1571">Remove the Triggers</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="c16ab-1572">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="c16ab-1572">Az.DataFactory</span></span>
* <span data-ttu-id="c16ab-1573">ADF .Net SDK 버전을 4.4.0으로 업데이트</span><span class="sxs-lookup"><span data-stu-id="c16ab-1573">Update ADF .Net SDK version to 4.4.0</span></span>
* <span data-ttu-id="c16ab-1574">'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd에 'ExpressCustomSetup' 매개 변수를 추가하여 사용자 지정 설치 스크립트 없이 설치 구성 및 타사 구성 요소를 사용하도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1574">Add parameter 'ExpressCustomSetup' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable setup configurations and 3rd party components without custom setup script.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="c16ab-1575">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="c16ab-1575">Az.DataLakeStore</span></span>
* <span data-ttu-id="c16ab-1576">Get-AzDataLakeStoreDeletedItem 및 Restore-AzDataLakeStoreDeletedItem의 설명서 업데이트</span><span class="sxs-lookup"><span data-stu-id="c16ab-1576">Update documentation of Get-AzDataLakeStoreDeletedItem and Restore-AzDataLakeStoreDeletedItem</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="c16ab-1577">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="c16ab-1577">Az.EventHub</span></span>
* <span data-ttu-id="c16ab-1578">10301 문제 해결: SAS 토큰 날짜 형식 수정</span><span class="sxs-lookup"><span data-stu-id="c16ab-1578">Fix for issue 10301 : Fix the SAS Token date format</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="c16ab-1579">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="c16ab-1579">Az.FrontDoor</span></span>
* <span data-ttu-id="c16ab-1580">Enable-AzFrontDoorCustomDomainHttps 및 New-AzFrontDoorFrontendEndpointObject에 MinimumTlsVersion 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="c16ab-1580">Add MinimumTlsVersion parameter to Enable-AzFrontDoorCustomDomainHttps and New-AzFrontDoorFrontendEndpointObject</span></span>
* <span data-ttu-id="c16ab-1581">New-AzFrontDoorHealthProbeSettingObject에 HealthProbeMethod 및 EnabledState 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="c16ab-1581">Add HealthProbeMethod and EnabledState parameters to New-AzFrontDoorHealthProbeSettingObject</span></span>
* <span data-ttu-id="c16ab-1582">BackendPoolsSettings 개체를 생성하여 Front Door 생성/업데이트에 전달하는 새 cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="c16ab-1582">Add new cmdlet to create BackendPoolsSettings objec to pass into creation/update of Front Door</span></span>
    - <span data-ttu-id="c16ab-1583">New-AzFrontDoorBackendPoolsSettingObject</span><span class="sxs-lookup"><span data-stu-id="c16ab-1583">New-AzFrontDoorBackendPoolsSettingObject</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="c16ab-1584">Az.Network</span><span class="sxs-lookup"><span data-stu-id="c16ab-1584">Az.Network</span></span>
* <span data-ttu-id="c16ab-1585">'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' 및 'Start-AzVirtualnetworkGatewayPacketCapture.md' FilterData 옵션 예제를 변경합니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1585">Change 'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' and 'Start-AzVirtualnetworkGatewayPacketCapture.md' FilterData option examples.</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="c16ab-1586">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="c16ab-1586">Az.PrivateDns</span></span>
* <span data-ttu-id="c16ab-1587">PrivateDns .net sdk를 버전 1.0.0으로 업데이트함</span><span class="sxs-lookup"><span data-stu-id="c16ab-1587">Updated PrivateDns .net sdk to version 1.0.0</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="c16ab-1588">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="c16ab-1588">Az.RecoveryServices</span></span>
* <span data-ttu-id="c16ab-1589">보호를 사용하도록 설정할 때 디스크 유형을 선택하도록 Azure Site Recovery 지원</span><span class="sxs-lookup"><span data-stu-id="c16ab-1589">Azure Site Recovery support to select disk type at enabling protection.</span></span>
* <span data-ttu-id="c16ab-1590">복구 계획 동작 편집을 위한 Azure Site Recovery 버그 수정</span><span class="sxs-lookup"><span data-stu-id="c16ab-1590">Azure Site Recovery bug fix for recovery plan action edit.</span></span>
* <span data-ttu-id="c16ab-1591">파일 스트림 DB를 허용하도록 Azure Backup SQL 복원 지원</span><span class="sxs-lookup"><span data-stu-id="c16ab-1591">Azure Backup SQL Restore support to accept filestream DBs.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="c16ab-1592">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="c16ab-1592">Az.RedisCache</span></span>
* <span data-ttu-id="c16ab-1593">'New-AzRedisCache' 및 'Set-AzRedisCache' cmdlet에 'MinimumTlsVersion' 매개 변수가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1593">Added 'MinimumTlsVersion' parameter in 'New-AzRedisCache' and 'Set-AzRedisCache' cmdlets.</span></span> <span data-ttu-id="c16ab-1594">'Get-AzRedisCache' cmdlet 출력에 'MinimumTlsVersion'도 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1594">Also, added 'MinimumTlsVersion' in the output of 'Get-AzRedisCache' cmdlet.</span></span>
* <span data-ttu-id="c16ab-1595">'Set-AzRedisCache' 및 'New-AzRedisCache' cmdlet의 '-Size' 매개 변수에 대한 유효성 검사가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1595">Added validation on '-Size' parameter for 'Set-AzRedisCache' and 'New-AzRedisCache' cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="c16ab-1596">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="c16ab-1596">Az.Resources</span></span>
- <span data-ttu-id="c16ab-1597">정책 할당에 새로운 EnforcementMode 속성이 있는 새 api 버전 2019-06-01을 사용하도록 정책 cmdlet이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1597">Updated policy cmdlets to use new api version 2019-06-01 that has new EnforcementMode property in policy assignment.</span></span>
- <span data-ttu-id="c16ab-1598">정책 정의 만들기 도움말 예제가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1598">Updated create policy definition help example</span></span>
- <span data-ttu-id="c16ab-1599">Remove-AZADServicePrincipal -ServicePrincipalName 버그를 수정하고, 서비스 사용자 이름을 찾을 수 없으면 null 참조를 throw합니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1599">Fix bug Remove-AZADServicePrincipal -ServicePrincipalName, throw null reference when service principal name not found.</span></span>
- <span data-ttu-id="c16ab-1600">New-AZADServicePrincipal 버그를 수정하고, 테넌트에 구독이 없으면 null 참조를 throw합니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1600">Fix bug New-AZADServicePrincipal, throw null reference when tenant doesn't have any subscription.</span></span>
- <span data-ttu-id="c16ab-1601">연결된 애플리케이션에만 자격 증명을 추가하도록 New-AzAdServicePrincipal을 변경합니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1601">Change New-AzAdServicePrincipal to add credentials only to associated application.</span></span>

#### <a name="azsql"></a><span data-ttu-id="c16ab-1602">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="c16ab-1602">Az.Sql</span></span>
* <span data-ttu-id="c16ab-1603">데이터베이스 ReadReplicaCount에 대한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1603">Added support for database ReadReplicaCount.</span></span>
* <span data-ttu-id="c16ab-1604">영역 중복이 설정되지 않은 경우 Set-AzSqlDatabase가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1604">Fixed Set-AzSqlDatabase when zone redundancy not set</span></span>

## <a name="300---november-2019"></a><span data-ttu-id="c16ab-1605">3.0.0 - 2019년 11월</span><span class="sxs-lookup"><span data-stu-id="c16ab-1605">3.0.0 - November 2019</span></span>
### <a name="general"></a><span data-ttu-id="c16ab-1606">일반</span><span class="sxs-lookup"><span data-stu-id="c16ab-1606">General</span></span>
* <span data-ttu-id="c16ab-1607">Az.PrivateDns 1.0.0 릴리스</span><span class="sxs-lookup"><span data-stu-id="c16ab-1607">Az.PrivateDns 1.0.0 released</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="c16ab-1608">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="c16ab-1608">Az.Accounts</span></span>
* <span data-ttu-id="c16ab-1609">'Resolve-Error' 별칭에 사용 중단 메시지를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1609">Add a deprecation message for 'Resolve-Error' alias.</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="c16ab-1610">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="c16ab-1610">Az.Advisor</span></span>
* <span data-ttu-id="c16ab-1611">Get-AzAdvisorRecommendation cmdlet에 새로운 '운영 효율성' 범주가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1611">Added new category 'Operational Excellence' to Get-AzAdvisorRecommendation cmdlet.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="c16ab-1612">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="c16ab-1612">Az.Batch</span></span>
* <span data-ttu-id="c16ab-1613">`BatchAccountContext`의 `CoreQuota` 이름이 `DedicatedCoreQuota`로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1613">Renamed `CoreQuota` on `BatchAccountContext` to `DedicatedCoreQuota`.</span></span> <span data-ttu-id="c16ab-1614">또한 `LowPriorityCoreQuota`가 새로 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1614">There is also a new `LowPriorityCoreQuota`.</span></span>
  - <span data-ttu-id="c16ab-1615">이 변경 사항은 **Get-AzBatchAccount** 에 영향을 줍니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1615">This impacts **Get-AzBatchAccount**.</span></span>
* <span data-ttu-id="c16ab-1616">이제 **New-AzBatchTask** `-ResourceFile` 매개 변수는 새로운 **New-AzBatchResourceFile** cmdlet을 사용하여 구성할 수 있는 `PSResourceFile` 개체의 컬렉션을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1616">**New-AzBatchTask** `-ResourceFile` parameter now takes a collection of `PSResourceFile` objects, which can be constructed using the new **New-AzBatchResourceFile** cmdlet.</span></span>
* <span data-ttu-id="c16ab-1617">새로운 **New-AzBatchResourceFile** cmdlet을 통해 `PSResourceFile` 개체를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1617">New **New-AzBatchResourceFile** cmdlet to help create `PSResourceFile` objects.</span></span> <span data-ttu-id="c16ab-1618">이들은 `-ResourceFile` 매개 변수의 **New-AzBatchTask** 에 제공될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1618">These can be supplied to **New-AzBatchTask** on the `-ResourceFile` parameter.</span></span>
  - <span data-ttu-id="c16ab-1619">그에 따라 기존 `HttpUrl` 방법 외에도 두 가지 종류의 리소스 파일이 새롭게 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1619">This supports two new kinds of resource file in addition to the existing `HttpUrl` way:</span></span>
    - <span data-ttu-id="c16ab-1620">`AutoStorageContainerName` 기반 리소스 파일은 전체 자동 스토리지 컨테이너를 일괄 처리 노드에 다운로드합니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1620">`AutoStorageContainerName` based resource files download an entire auto-storage container to the Batch node.</span></span>
    - <span data-ttu-id="c16ab-1621">`StorageContainerUrl` 기반 리소스 파일은 URL에 지정된 컨테이너를 일괄 처리 노드에 다운로드합니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1621">`StorageContainerUrl` based resource files download the container specified in the URL to the Batch node.</span></span>
* <span data-ttu-id="c16ab-1622">**Get-AzBatchApplication** 으로 반환되는 `PSApplication`의 `ApplicationPackages` 속성이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1622">Removed `ApplicationPackages` property of `PSApplication` returned by **Get-AzBatchApplication**.</span></span>
  - <span data-ttu-id="c16ab-1623">이제 **Get-AzBatchApplicationPackage** 를 사용하여 애플리케이션 내부의 특정 패키지를 검색할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1623">The specific packages inside of an application now can be retrieved using **Get-AzBatchApplicationPackage**.</span></span> <span data-ttu-id="c16ab-1624">예: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`</span><span class="sxs-lookup"><span data-stu-id="c16ab-1624">For example: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span></span>
* <span data-ttu-id="c16ab-1625">**Get-AzBatchApplicationPackage** , **New-AzBatchApplicationPackage** , **Remove-AzBatchApplicationPackage** , **Get-AzBatchApplication** , **New-AzBatchApplication** , **Remove-AzBatchApplication** 및 **Set-AzBatchApplication** 에서 `ApplicationId` 이름이 `ApplicationName`으로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1625">Renamed `ApplicationId` to `ApplicationName` on **Get-AzBatchApplicationPackage** , **New-AzBatchApplicationPackage** , **Remove-AzBatchApplicationPackage** , **Get-AzBatchApplication** , **New-AzBatchApplication** , **Remove-AzBatchApplication** , and **Set-AzBatchApplication**.</span></span>
  - <span data-ttu-id="c16ab-1626">이제 `ApplicationId`는 `ApplicationName`의 별칭입니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1626">`ApplicationId` now is an alias of `ApplicationName`.</span></span>
* <span data-ttu-id="c16ab-1627">새로운 `PSWindowsUserConfiguration` 속성이 `PSUserAccount`에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1627">Added new `PSWindowsUserConfiguration` property to `PSUserAccount`.</span></span>
* <span data-ttu-id="c16ab-1628">`PSApplicationPackage`에서 `Version` 이름이 `Name`으로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1628">Renamed `Version` to `Name` on `PSApplicationPackage`.</span></span>
* <span data-ttu-id="c16ab-1629">`PSResourceFile`에서 `BlobSource` 이름이 `HttpUrl`으로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1629">Renamed `BlobSource` to `HttpUrl` on `PSResourceFile`.</span></span>
* <span data-ttu-id="c16ab-1630">`PSVirtualMachineConfiguration`에서 `OSDisk` 속성이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1630">Removed `OSDisk` property from `PSVirtualMachineConfiguration`.</span></span>
* <span data-ttu-id="c16ab-1631">**Set-AzBatchPoolOSVersion** 이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1631">Removed **Set-AzBatchPoolOSVersion**.</span></span> <span data-ttu-id="c16ab-1632">이 작업은 더 이상 지원되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1632">This operation is no longer supported.</span></span>
* <span data-ttu-id="c16ab-1633">`PSCloudServiceConfiguration`에서 `TargetOSVersion`이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1633">Removed `TargetOSVersion` from `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="c16ab-1634">`PSCloudServiceConfiguration`에서 `CurrentOSVersion` 이름이 `OSVersion`으로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1634">Renamed `CurrentOSVersion` to `OSVersion` on `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="c16ab-1635">`PSPoolUsageMetrics`에서 `DataEgressGiB` 및 `DataIngressGiB`가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1635">Removed `DataEgressGiB` and `DataIngressGiB` from `PSPoolUsageMetrics`.</span></span>
* <span data-ttu-id="c16ab-1636">**Get-AzBatchNodeAgentSku** 가 제거되고 **Get-AzBatchSupportedImage** 로 대체되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1636">Removed **Get-AzBatchNodeAgentSku** and replaced it with  **Get-AzBatchSupportedImage**.</span></span>
  - <span data-ttu-id="c16ab-1637">**Get-AzBatchSupportedImage** 가 **Get-AzBatchNodeAgentSku** 와 동일한 데이터를 반환하지만 더 친숙한 형식이 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1637">**Get-AzBatchSupportedImage** returns the same data as **Get-AzBatchNodeAgentSku** but in a more friendly format.</span></span>
  - <span data-ttu-id="c16ab-1638">이제 확인되지 않은 이미지도 새롭게 반환됩니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1638">New non-verified images are also now returned.</span></span> <span data-ttu-id="c16ab-1639">각 이미지의 `Capabilities` 및 `BatchSupportEndOfLife`에 대한 추가 정보도 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1639">Additional information about `Capabilities` and `BatchSupportEndOfLife` for each image is also included.</span></span>
* <span data-ttu-id="c16ab-1640">**New-AzBatchPool** 의 새로운 `MountConfiguration` 매개 변수를 통해 풀의 각 노드에서 원격 파일 시스템을 마운트할 수 있는 기능이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1640">Added ability to mount remote file-systems on each node of a pool via the new `MountConfiguration` parameter of **New-AzBatchPool**.</span></span>
* <span data-ttu-id="c16ab-1641">이제 트래픽의 소스 포트를 기준으로 풀에 대한 네트워크 액세스를 차단하는 네트워크 보안 규칙이 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1641">Now support network security rules blocking network access to a pool based on the source port of the traffic.</span></span> <span data-ttu-id="c16ab-1642">이 작업은 `PSNetworkSecurityGroupRule`에서 `SourcePortRanges` 속성을 통해 수행됩니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1642">This is done via the `SourcePortRanges` property on `PSNetworkSecurityGroupRule`.</span></span>
* <span data-ttu-id="c16ab-1643">컨테이너를 실행할 때 Batch는 이제 컨테이너 작업 디렉터리 또는 일괄 처리 태스크 작업 디렉터리에서 작업 실행을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1643">When running a container, Batch now supports executing the task in the container working directory or in the Batch task working directory.</span></span> <span data-ttu-id="c16ab-1644">이 작업은 `PSTaskContainerSettings`에서 `WorkingDirectory` 속성에 의해 제어됩니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1644">This is controlled by the `WorkingDirectory` property on `PSTaskContainerSettings`.</span></span>
* <span data-ttu-id="c16ab-1645">새로운 `PublicIPs` 속성을 통해 `PSNetworkConfiguration`에서 공용 IP의 컬렉션을 지정할 수 있는 기능이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1645">Added ability to specify a collection of public IPs on `PSNetworkConfiguration` via the new `PublicIPs` property.</span></span> <span data-ttu-id="c16ab-1646">그 결과 사용자 제공 IP 목록의 IP가 풀에 있는 노드에 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1646">This guarantees nodes in the Pool will have an IP from the list user provided IPs.</span></span>
* <span data-ttu-id="c16ab-1647">지정하지 않은 경우 이제 `PSSTartTask`에서 `WaitForSuccess`의 기본값은 `$True`입니다(이전에는 `$False`).</span><span class="sxs-lookup"><span data-stu-id="c16ab-1647">When not specified, the default value of `WaitForSuccess` on `PSSTartTask` is now `$True` (was `$False`).</span></span>
* <span data-ttu-id="c16ab-1648">지정하지 않은 경우 이제 `PSAutoUserSpecification`에서 `Scope`의 기본값은 `Pool`입니다(이전에는 Windows의 경우 `Task`, Linux의 경우에는 `Pool`).</span><span class="sxs-lookup"><span data-stu-id="c16ab-1648">When not specified, the default value of `Scope` on `PSAutoUserSpecification` is now `Pool` (was `Task` on Windows and `Pool` on Linux).</span></span>

#### <a name="azcdn"></a><span data-ttu-id="c16ab-1649">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="c16ab-1649">Az.Cdn</span></span>
* <span data-ttu-id="c16ab-1650">RulesEngine에 UrlRewriteAction 및 CacheKeyQueryStringAction이 도입되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1650">Introduced UrlRewriteAction and CacheKeyQueryStringAction to RulesEngine.</span></span>
* <span data-ttu-id="c16ab-1651">New-AzDeliveryRuleCondition cmdlet에서 'Selector' 입력 누락과 같은 여러 버그가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1651">Fixed several bugs like missing 'Selector' Input in New-AzDeliveryRuleCondition cmdlet.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="c16ab-1652">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="c16ab-1652">Az.Compute</span></span>
* <span data-ttu-id="c16ab-1653">디스크 암호화 집합 기능</span><span class="sxs-lookup"><span data-stu-id="c16ab-1653">Disk Encryption Set feature</span></span>
    - <span data-ttu-id="c16ab-1654">새 cmdlet:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="c16ab-1654">New cmdlets:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span></span>
    - <span data-ttu-id="c16ab-1655">DiskEncryptionSetId 매개 변수가 다음 cmdlet에 추가되었습니다.   Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="c16ab-1655">DiskEncryptionSetId parameter is added to the following cmdlets:   Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span></span>
    - <span data-ttu-id="c16ab-1656">DiskEncryptionSetId 및 EncryptionType 매개 변수가 다음 cmdlet에 추가되었습니다.   New-AzDiskConfig   New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="c16ab-1656">DiskEncryptionSetId and EncryptionType parameters are added to the following cmdlets:   New-AzDiskConfig   New-AzSnapshotConfig</span></span>
* <span data-ttu-id="c16ab-1657">New-AzVmssIPConfig에 PublicIPAddressVersion 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="c16ab-1657">Add PublicIPAddressVersion parameter to New-AzVmssIPConfig</span></span>
* <span data-ttu-id="c16ab-1658">사용자 지정 스크립트 확장의 FileUris를 공용 설정에서 보호된 설정으로 이동</span><span class="sxs-lookup"><span data-stu-id="c16ab-1658">Move FileUris of custom script extension from public setting to protected setting</span></span>
* <span data-ttu-id="c16ab-1659">New-AzVmss, New-AzVmssConfig 및 Update-AzVmss cmdlet에 ScaleInPolicy 추가</span><span class="sxs-lookup"><span data-stu-id="c16ab-1659">Add ScaleInPolicy to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>
* <span data-ttu-id="c16ab-1660">주요 변경 내용</span><span class="sxs-lookup"><span data-stu-id="c16ab-1660">Breaking changes</span></span>
    - <span data-ttu-id="c16ab-1661">CreateOption이 업로드일 때 UploadSizeInBytes 매개 변수가 New-AzDiskConfig에 대해 DiskSizeGB 대신 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1661">UploadSizeInBytes parameter is used instead of DiskSizeGB for New-AzDiskConfig when CreateOption is Upload</span></span>
    - <span data-ttu-id="c16ab-1662">GalleryImageVersion 개체에서 PublishingProfile.Source.ManagedImage.Id가 StorageProfile.Source.Id로 바뀝니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1662">PublishingProfile.Source.ManagedImage.Id is replaced with StorageProfile.Source.Id in GalleryImageVersion object</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="c16ab-1663">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="c16ab-1663">Az.DataFactory</span></span>
* <span data-ttu-id="c16ab-1664">ADF .Net SDK 버전을 4.3.0으로 업데이트</span><span class="sxs-lookup"><span data-stu-id="c16ab-1664">Update ADF .Net SDK version to 4.3.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="c16ab-1665">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="c16ab-1665">Az.DataLakeStore</span></span>
* <span data-ttu-id="c16ab-1666">ADLS SDK 버전 업데이트(https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha) , 다음 수정 사항 제공</span><span class="sxs-lookup"><span data-stu-id="c16ab-1666">Update ADLS SDK version (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), brings following fixes</span></span>
* <span data-ttu-id="c16ab-1667">휴지통 또는 디렉터리 항목의 creationtime을 역직렬화할 수 없을 때 예외가 발생하지 않도록 방지합니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1667">Avoid throwing exception while unable to deserialize the creationtime of the trash or directory entry.</span></span>
* <span data-ttu-id="c16ab-1668">adlsclient에서 요청별 시간 제한 설정 노출</span><span class="sxs-lookup"><span data-stu-id="c16ab-1668">Expose setting per request timeout in adlsclient</span></span>
* <span data-ttu-id="c16ab-1669">badoffset 복구를 위한 원본 syncflag 전달 수정</span><span class="sxs-lookup"><span data-stu-id="c16ab-1669">Fix passing the original syncflag for badoffset recovery</span></span>
* <span data-ttu-id="c16ab-1670">응답이 확인된 후 연속 토큰을 검색하기 위한 EnumerateDirectory 수정</span><span class="sxs-lookup"><span data-stu-id="c16ab-1670">Fix EnumerateDirectory to retrieve continuation token once response is checked</span></span>
* <span data-ttu-id="c16ab-1671">Concat 버그 수정</span><span class="sxs-lookup"><span data-stu-id="c16ab-1671">Fix Concat Bug</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="c16ab-1672">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="c16ab-1672">Az.FrontDoor</span></span>
* <span data-ttu-id="c16ab-1673">모듈 간 기타 오타가 수정됨</span><span class="sxs-lookup"><span data-stu-id="c16ab-1673">Fixed miscellaneous typos across module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="c16ab-1674">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="c16ab-1674">Az.HDInsight</span></span>
* <span data-ttu-id="c16ab-1675">ADLSGen1 스토리지가 포함된 클러스터를 가져오기 위해 Get-AzHDInsightCluster를 사용할 때 고객에게 '올바른 Base-64 문자열이 아닙니다' 오류가 표시되는 버그가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1675">Fixed the bug that customer will get 'Not a valid Base-64 string' error when using Get-AzHDInsightCluster to get the cluster with ADLSGen1 storage.</span></span>
* <span data-ttu-id="c16ab-1676">고객이 Azure Data Lake에 액세스하기 위해 서비스 주체 애플리케이션 ID를 제공할 수 있도록 세 가지 cmdlet Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig 및 New-AzHDInsightCluster에 이름이 'ApplicationId'인 매개 변수를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1676">Add a parameter named 'ApplicationId' to three cmdlets Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig and New-AzHDInsightCluster so that customer can provide the service principal application id for accessing Azure Data Lake.</span></span>
* <span data-ttu-id="c16ab-1677">Microsoft.Azure.Management.HDInsight가 2.1.0에서 5.1.0으로 변경됨</span><span class="sxs-lookup"><span data-stu-id="c16ab-1677">Changed Microsoft.Azure.Management.HDInsight from 2.1.0 to 5.1.0</span></span>
* <span data-ttu-id="c16ab-1678">다음 5가지 cmdlet이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1678">Removed five cmdlets:</span></span>
    - <span data-ttu-id="c16ab-1679">Get-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="c16ab-1679">Get-AzHDInsightOMS</span></span>
    - <span data-ttu-id="c16ab-1680">Enable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="c16ab-1680">Enable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="c16ab-1681">Disable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="c16ab-1681">Disable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="c16ab-1682">Grant-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="c16ab-1682">Grant-AzHDInsightRdpServicesAccess</span></span>
    - <span data-ttu-id="c16ab-1683">Revoke-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="c16ab-1683">Revoke-AzHDInsightRdpServicesAccess</span></span>
* <span data-ttu-id="c16ab-1684">다음 3가지 cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1684">Added three cmdlets:</span></span>
    - <span data-ttu-id="c16ab-1685">Get-AzHDInsightOMS 대신 Get-AzHDInsightMonitoring</span><span class="sxs-lookup"><span data-stu-id="c16ab-1685">Get-AzHDInsightMonitoring to replace Get-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="c16ab-1686">Get-AzHDInsightOMS 대신 Get-AzHDInsightMonitoring</span><span class="sxs-lookup"><span data-stu-id="c16ab-1686">Enable-AzHDInsightMonitoring to replace Enable-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="c16ab-1687">Disable-AzHDInsightOMS 대신 Disable-AzHDInsightMonitoring</span><span class="sxs-lookup"><span data-stu-id="c16ab-1687">Disable-AzHDInsightMonitoring to replace Disable-AzHDInsightOMS.</span></span>
* <span data-ttu-id="c16ab-1688">특정 위치의 기능 정보 가져오기를 지원하도록 cmdlet Get-AzHDInsightProperties가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1688">Fixed cmdlet Get-AzHDInsightProperties to support get capabilities information from a specific location.</span></span>
* <span data-ttu-id="c16ab-1689">Add-AzHDInsightConfigValue에서 매개 변수 집합('Spark1', 'Spark2')이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1689">Removed parameter sets('Spark1', 'Spark2') from Add-AzHDInsightConfigValue.</span></span>
* <span data-ttu-id="c16ab-1690">cmdlet Add-AzHDInsightSecurityProfile의 도움말 문서에 예제를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1690">Add examples to the help documents of cmdlet Add-AzHDInsightSecurityProfile.</span></span>
* <span data-ttu-id="c16ab-1691">다음 cmdlet의 출력 유형이 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1691">Changed output type of the following cmdlets:</span></span>
*  - <span data-ttu-id="c16ab-1692">Get-AzHDInsightProperties의 출력 유형이 CapabilitiesResponse에서 AzureHDInsightCapabilities로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1692">Changed the output type of Get-AzHDInsightProperties from  CapabilitiesResponse to AzureHDInsightCapabilities.</span></span>
*  - <span data-ttu-id="c16ab-1693">Remove-AzHDInsightCluster의 출력 유형이 ClusterGetResponse에서 bool로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1693">Changed the output type of Remove-AzHDInsightCluster from ClusterGetResponse to bool.</span></span>
*  - <span data-ttu-id="c16ab-1694">Set-AzHDInsightGatewaySettings의 출력 유형이 HttpConnectivitySettings에서 GatewaySettings로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1694">Changed the output type of Set-AzHDInsightGatewaySettings HttpConnectivitySettings to GatewaySettings.</span></span>
* <span data-ttu-id="c16ab-1695">몇 가지 시나리오 테스트 사례가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1695">Added some scenario test cases.</span></span>
* <span data-ttu-id="c16ab-1696">일부 별칭 제거: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1696">Remove some alias: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="c16ab-1697">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="c16ab-1697">Az.IotHub</span></span>
* <span data-ttu-id="c16ab-1698">주요 변경 내용:</span><span class="sxs-lookup"><span data-stu-id="c16ab-1698">Breaking changes:</span></span>
    - <span data-ttu-id="c16ab-1699">'Add-AzIotHubEventHubConsumerGroup' cmdlet이 'EventHubEndpointName' 매개 변수를 더 이상 지원하지 않으며 원래 매개 변수 이름에 대해 별칭을 찾을 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1699">The cmdlet 'Add-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="c16ab-1700">'Add-AzIotHubEventHubConsumerGroup' cmdlet에 대한 매개 변수 집합 '__AllParameterSets'가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1700">The parameter set '__AllParameterSets' for cmdlet 'Add-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="c16ab-1701">'Get-AzIotHubEventHubConsumerGroup' cmdlet이 'EventHubEndpointName' 매개 변수를 더 이상 지원하지 않으며 원래 매개 변수 이름에 대해 별칭을 찾을 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1701">The cmdlet 'Get-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="c16ab-1702">'Get-AzIotHubEventHubConsumerGroup' cmdlet에 대한 매개 변수 집합 '__AllParameterSets'가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1702">The parameter set '__AllParameterSets' for cmdlet 'Get-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="c16ab-1703">'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' 유형의 'OperationsMonitoringProperties' 속성이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1703">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' has been removed.</span></span>
    - <span data-ttu-id="c16ab-1704">'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' 유형의 'OperationsMonitoringProperties' 속성이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1704">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' has been removed.</span></span>
    - <span data-ttu-id="c16ab-1705">'New-AzIotHubExportDevice' cmdlet이 더 이상 'New-AzIotHubExportDevices' 별칭을 지원하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1705">The cmdlet 'New-AzIotHubExportDevice' no longer supports the alias 'New-AzIotHubExportDevices'.</span></span>
    - <span data-ttu-id="c16ab-1706">'New-AzIotHubImportDevice' cmdlet이 더 이상 'New-AzIotHubImportDevices' 별칭을 지원하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1706">The cmdlet 'New-AzIotHubImportDevice' no longer supports the alias 'New-AzIotHubImportDevices'.</span></span>
    - <span data-ttu-id="c16ab-1707">'Remove-AzIotHubEventHubConsumerGroup' cmdlet이 'EventHubEndpointName' 매개 변수를 더 이상 지원하지 않으며 원래 매개 변수 이름에 대해 별칭을 찾을 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1707">The cmdlet 'Remove-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="c16ab-1708">'Remove-AzIotHubEventHubConsumerGroup' cmdlet에 대한 매개 변수 집합 '__AllParameterSets'가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1708">The parameter set '__AllParameterSets' for cmdlet 'Remove-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="c16ab-1709">'Set-AzIotHub' cmdlet이 'OperationsMonitoringProperties' 매개 변수를 더 이상 지원하지 않으며 원래 매개 변수 이름에 대해 별칭을 찾을 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1709">The cmdlet 'Set-AzIotHub' no longer supports the parameter 'OperationsMonitoringProperties' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="c16ab-1710">'Set-AzIotHub' cmdlet에 대한 매개 변수 집합 'UpdateOperationsMonitoringProperties'가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1710">The parameter set 'UpdateOperationsMonitoringProperties' for cmdlet 'Set-AzIotHub' has been removed.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="c16ab-1711">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="c16ab-1711">Az.RecoveryServices</span></span>
* <span data-ttu-id="c16ab-1712">Azure Site Recovery가 Azure-Azure를 위한 NSG, 공용 IP 및 내부 부하 분산 장치와 같은 네트워킹 리소스 구성을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1712">Azure Site Recovery support to configure networking resources like NSG, public IP and internal load balancers for Azure to Azure.</span></span>
* <span data-ttu-id="c16ab-1713">Azure Site Recovery가 vMWare-Azure를 위한 관리 디스크에 쓰기를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1713">Azure Site Recovery Support to write to managed disk for vMWare to Azure.</span></span>
* <span data-ttu-id="c16ab-1714">Azure Site Recovery가 vMWare-Azure를 위한 NIC 감소를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1714">Azure Site Recovery Support to NIC reduction for vMWare to Azure.</span></span>
* <span data-ttu-id="c16ab-1715">Azure Site Recovery가 Azure-Azure를 위한 가속 네트워킹을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1715">Azure Site Recovery Support to accelerated networking for Azure to Azure.</span></span>
* <span data-ttu-id="c16ab-1716">Azure Site Recovery가 Azure-Azure를 위한 에이전트 자동 업데이트를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1716">Azure Site Recovery Support to agent auto update for Azure to Azure.</span></span>
* <span data-ttu-id="c16ab-1717">Azure Site Recovery가 Azure-Azure를 위한 표준 SSD를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1717">Azure Site Recovery Support to Standard SSD for Azure to Azure.</span></span>
* <span data-ttu-id="c16ab-1718">Azure Site Recovery가 Azure-Azure를 위한 두 가지 Azure 디스크 암호화 전달을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1718">Azure Site Recovery Support to Azure Disk Encryption two pass for Azure to Azure.</span></span>
* <span data-ttu-id="c16ab-1719">Azure Site Recovery가 Azure-Azure를 위한 새로 추가된 디스크 보호를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1719">Azure Site Recovery Support to protect newly added disk for Azure to Azure.</span></span>
* <span data-ttu-id="c16ab-1720">VM을 위한 SoftDelete 기능 및 softdelete를 위한 테스트가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1720">Added SoftDelete feature for VM and added tests for softdelete</span></span>

#### <a name="azresources"></a><span data-ttu-id="c16ab-1721">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="c16ab-1721">Az.Resources</span></span>
* <span data-ttu-id="c16ab-1722">종속성 어셈블리 Microsoft.Extensions.Caching.Memory가 1.1.1에서 2.2로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1722">Update dependency assembly Microsoft.Extensions.Caching.Memory from 1.1.1 to 2.2</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="c16ab-1723">Az.Network</span><span class="sxs-lookup"><span data-stu-id="c16ab-1723">Az.Network</span></span>
* <span data-ttu-id="c16ab-1724">일반 서비스 공급자 지원을 위해 PrivateEndpointConnection에 대한 모든 cmdlet이 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1724">Change all cmdlets for PrivateEndpointConnection to support generic service provider.</span></span>
    - <span data-ttu-id="c16ab-1725">업데이트된 cmdlet:</span><span class="sxs-lookup"><span data-stu-id="c16ab-1725">Updated cmdlet:</span></span>
        - <span data-ttu-id="c16ab-1726">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="c16ab-1726">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="c16ab-1727">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="c16ab-1727">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="c16ab-1728">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="c16ab-1728">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="c16ab-1729">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="c16ab-1729">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="c16ab-1730">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="c16ab-1730">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="c16ab-1731">PrivateLinkResource에 대한 새 cmdlet이 추가되었고 일반 서비스 공급자도 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1731">Add new cmdlet for PrivateLinkResource and it also support generic service provider.</span></span>
    - <span data-ttu-id="c16ab-1732">새 cmdlet:</span><span class="sxs-lookup"><span data-stu-id="c16ab-1732">New cmdlet:</span></span>
        - <span data-ttu-id="c16ab-1733">Get-AzPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="c16ab-1733">Get-AzPrivateLinkResource</span></span>
* <span data-ttu-id="c16ab-1734">Proxy Protocol V2 기능에 대한 새 필드 및 매개 변수가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1734">Add new fields and parameter for the feature Proxy Protocol V2.</span></span>
    - <span data-ttu-id="c16ab-1735">PrivateLinkService에서 EnableProxyProtocol 속성 추가</span><span class="sxs-lookup"><span data-stu-id="c16ab-1735">Add property EnableProxyProtocol in PrivateLinkService</span></span>
    - <span data-ttu-id="c16ab-1736">PrivateEndpointConnection에서 LinkIdentifier 속성 추가</span><span class="sxs-lookup"><span data-stu-id="c16ab-1736">Add property LinkIdentifier in PrivateEndpointConnection</span></span>
    - <span data-ttu-id="c16ab-1737">새로운 선택적인 매개 변수인 EnableProxyProtocol을 추가하도록 New-AzPrivateLinkService가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1737">Updated New-AzPrivateLinkService to add a new optional parameter EnableProxyProtocol.</span></span>
* <span data-ttu-id="c16ab-1738">'New-AzApplicationGatewaySku' 참조 설명서의 잘못된 매개 변수 설명 수정</span><span class="sxs-lookup"><span data-stu-id="c16ab-1738">Fix incorrect parameter description in 'New-AzApplicationGatewaySku' reference documentation</span></span>
* <span data-ttu-id="c16ab-1739">Azure 방화벽 정책을 지원하는 새로운 cmdlet</span><span class="sxs-lookup"><span data-stu-id="c16ab-1739">New cmdlets to support the azure firewall policy</span></span>
* <span data-ttu-id="c16ab-1740">VirtualHub의 자식 리소스 RouteTables에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="c16ab-1740">Add support for child resource RouteTables of VirtualHub</span></span>
    - <span data-ttu-id="c16ab-1741">추가된 새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1741">New cmdlets added:</span></span>
        - <span data-ttu-id="c16ab-1742">Add-AzVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="c16ab-1742">Add-AzVirtualHubRoute</span></span>
        - <span data-ttu-id="c16ab-1743">Add-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="c16ab-1743">Add-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="c16ab-1744">Get-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="c16ab-1744">Get-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="c16ab-1745">Remove-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="c16ab-1745">Remove-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="c16ab-1746">Set-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="c16ab-1746">Set-AzVirtualHub</span></span>
* <span data-ttu-id="c16ab-1747">VirtualHub의 새로운 속성 Sku 및 VirtualWan의 VirtualWANType에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="c16ab-1747">Add support for new properties Sku of VirtualHub and VirtualWANType of VirtualWan</span></span>
    - <span data-ttu-id="c16ab-1748">선택적 매개 변수로 다음 cmdlet이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1748">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="c16ab-1749">New-AzVirtualHub: 추가된 매개 변수 Sku</span><span class="sxs-lookup"><span data-stu-id="c16ab-1749">New-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="c16ab-1750">Update-AzVirtualHub: 추가된 매개 변수 Sku</span><span class="sxs-lookup"><span data-stu-id="c16ab-1750">Update-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="c16ab-1751">New-AzVirtualWan: 추가된 매개 변수 VirtualWANType</span><span class="sxs-lookup"><span data-stu-id="c16ab-1751">New-AzVirtualWan : added parameter VirtualWANType</span></span>
        - <span data-ttu-id="c16ab-1752">Update-AzVirtualWan: 추가된 매개 변수 VirtualWANType</span><span class="sxs-lookup"><span data-stu-id="c16ab-1752">Update-AzVirtualWan : added parameter VirtualWANType</span></span>
* <span data-ttu-id="c16ab-1753">HubVnetConnection, VpnConnection 및 ExpressRouteConnection에 대한 EnableInternetSecurity 속성 지원 추가</span><span class="sxs-lookup"><span data-stu-id="c16ab-1753">Add support for EnableInternetSecurity property for HubVnetConnection, VpnConnection and ExpressRouteConnection</span></span>
    - <span data-ttu-id="c16ab-1754">추가된 새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1754">New cmdlets added:</span></span>
        - <span data-ttu-id="c16ab-1755">Update-AzureRmVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="c16ab-1755">Update-AzureRmVirtualHubVnetConnection</span></span>
    - <span data-ttu-id="c16ab-1756">선택적 매개 변수로 다음 cmdlet이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1756">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="c16ab-1757">New-AzureRmVirtualHubVnetConnection: 추가된 매개 변수 EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="c16ab-1757">New-AzureRmVirtualHubVnetConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="c16ab-1758">New-AzureRmVpnConnection: 추가된 매개 변수 EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="c16ab-1758">New-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="c16ab-1759">Update-AzureRmVpnConnection: 추가된 매개 변수 EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="c16ab-1759">Update-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="c16ab-1760">New-AzureRmExpressRouteConnection: 추가된 매개 변수 EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="c16ab-1760">New-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="c16ab-1761">Set-AzureRmExpressRouteConnection: 추가된 매개 변수 EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="c16ab-1761">Set-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
* <span data-ttu-id="c16ab-1762">TopLevel WebApplicationFirewall 정책 구성을 위한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="c16ab-1762">Add support for Configuring TopLevel WebApplicationFirewall Policy</span></span>
    - <span data-ttu-id="c16ab-1763">추가된 새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1763">New cmdlets added:</span></span>
        - <span data-ttu-id="c16ab-1764">New-AzApplicationGatewayFirewallPolicySetting</span><span class="sxs-lookup"><span data-stu-id="c16ab-1764">New-AzApplicationGatewayFirewallPolicySetting</span></span>
        - <span data-ttu-id="c16ab-1765">New-AzApplicationGatewayFirewallPolicyExclusion</span><span class="sxs-lookup"><span data-stu-id="c16ab-1765">New-AzApplicationGatewayFirewallPolicyExclusion</span></span>
        - <span data-ttu-id="c16ab-1766">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="c16ab-1766">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span></span>
        - <span data-ttu-id="c16ab-1767">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="c16ab-1767">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span></span>
        - <span data-ttu-id="c16ab-1768">New-AzApplicationGatewayFirewallPolicyManagedRule</span><span class="sxs-lookup"><span data-stu-id="c16ab-1768">New-AzApplicationGatewayFirewallPolicyManagedRule</span></span>
        - <span data-ttu-id="c16ab-1769">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="c16ab-1769">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span></span>
    - <span data-ttu-id="c16ab-1770">선택적 매개 변수로 다음 cmdlet이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1770">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="c16ab-1771">New-AzApplicationGatewayFirewallPolicy: 추가된 매개 변수 PolicySetting, ManagedRule</span><span class="sxs-lookup"><span data-stu-id="c16ab-1771">New-AzApplicationGatewayFirewallPolicy : added parameter PolicySetting, ManagedRule</span></span>
* <span data-ttu-id="c16ab-1772">CustomRule에서 Geo-Match 연산자를 위한 지원 추가됨</span><span class="sxs-lookup"><span data-stu-id="c16ab-1772">Added support for Geo-Match operator on CustomRule</span></span>
    - <span data-ttu-id="c16ab-1773">FirewallCondition에서 연산자에 GeoMatch 추가됨</span><span class="sxs-lookup"><span data-stu-id="c16ab-1773">Added GeoMatch to the operator on the FirewallCondition</span></span>
* <span data-ttu-id="c16ab-1774">perListener 및 perSite 방화벽 규칙에 대한 지원 추가됨</span><span class="sxs-lookup"><span data-stu-id="c16ab-1774">Added support for perListener and perSite Firewall policy</span></span>
    - <span data-ttu-id="c16ab-1775">선택적 매개 변수로 다음 cmdlet이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1775">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="c16ab-1776">New-AzApplicationGatewayHttpListener: 추가된 매개 변수 FirewallPolicy, FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="c16ab-1776">New-AzApplicationGatewayHttpListener : added parameter FirewallPolicy, FirewallPolicyId</span></span>
        - <span data-ttu-id="c16ab-1777">New-AzApplicationGatewayPathRuleConfig: 추가된 매개 변수 FirewallPolicy, FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="c16ab-1777">New-AzApplicationGatewayPathRuleConfig : added parameter FirewallPolicy, FirewallPolicyId</span></span>
* <span data-ttu-id="c16ab-1778">'PSBastion'에서 이름이 AzureBastionSubnet인 필수 서브넷의 수정은 대소문자를 구분하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1778">Fix required subnet with name AzureBastionSubnet in 'PSBastion' can be case insensitive</span></span>
* <span data-ttu-id="c16ab-1779">Azure Firewall을 위한 네트워크 규칙의 대상 FQDN 및 NAT 규칙의 번역된 FQDN 지원</span><span class="sxs-lookup"><span data-stu-id="c16ab-1779">Support for Destination FQDNs in Network Rules and Translated FQDN in NAT Rules for Azure Firewall</span></span>
* <span data-ttu-id="c16ab-1780">IpGroup의 최상위 리소스 RouteTables에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="c16ab-1780">Add support for top level resource RouteTables of IpGroup</span></span>
    - <span data-ttu-id="c16ab-1781">추가된 새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1781">New cmdlets added:</span></span>
        - <span data-ttu-id="c16ab-1782">New-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="c16ab-1782">New-AzIpGroup</span></span>
        - <span data-ttu-id="c16ab-1783">Remove-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="c16ab-1783">Remove-AzIpGroup</span></span>
        - <span data-ttu-id="c16ab-1784">Get-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="c16ab-1784">Get-AzIpGroup</span></span>
        - <span data-ttu-id="c16ab-1785">Set-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="c16ab-1785">Set-AzIpGroup</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="c16ab-1786">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="c16ab-1786">Az.ServiceFabric</span></span>
* <span data-ttu-id="c16ab-1787">Add-AzVmssSecret에서 지원되기 때문에 Add-AzServiceFabricApplicationCertificate cmdlet이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1787">Remove Add-AzServiceFabricApplicationCertificate cmdlet as this scenario is covered by Add-AzVmssSecret.</span></span>

#### <a name="azsql"></a><span data-ttu-id="c16ab-1788">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="c16ab-1788">Az.Sql</span></span>
* <span data-ttu-id="c16ab-1789">Managed Instances에서 삭제된 데이터베이스의 복원을 위한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1789">Added support for restore of dropped databases on Managed Instances.</span></span>
* <span data-ttu-id="c16ab-1790">이전의 감사 cmdlet 코드가 사용되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1790">Deprecated from code old auditing cmdlets.</span></span>
* <span data-ttu-id="c16ab-1791">사용되지 않는 별칭이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1791">Removed deprecated aliases:</span></span>
* <span data-ttu-id="c16ab-1792">Get-AzSqlDatabaseIndexRecommendations(대신 Get-AzSqlDatabaseIndexRecommendation 사용)</span><span class="sxs-lookup"><span data-stu-id="c16ab-1792">Get-AzSqlDatabaseIndexRecommendations (use Get-AzSqlDatabaseIndexRecommendation instead)</span></span>
* <span data-ttu-id="c16ab-1793">Get-AzSqlDatabaseRestorePoints(대신 Get-AzSqlDatabaseRestorePoint 사용)</span><span class="sxs-lookup"><span data-stu-id="c16ab-1793">Get-AzSqlDatabaseRestorePoints (use Get-AzSqlDatabaseRestorePoint instead)</span></span>
* <span data-ttu-id="c16ab-1794">Get-AzSqlDatabaseSecureConnectionPolicy cmdlet 제거</span><span class="sxs-lookup"><span data-stu-id="c16ab-1794">Remove Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="c16ab-1795">사용되지 않는 취약성 평가 설정 cmdlet에 대한 별칭 제거</span><span class="sxs-lookup"><span data-stu-id="c16ab-1795">Remove aliases for deprecated Vulnerability Assessment Settings cmdlets</span></span>
* <span data-ttu-id="c16ab-1796">지능형 위협 탐지 설정 cmdlet 사용 중단</span><span class="sxs-lookup"><span data-stu-id="c16ab-1796">Deprecate Advanced Threat Detection Settings cmdlets</span></span>
* <span data-ttu-id="c16ab-1797">데이터베이스의 열에 대한 민감도 권장 사항의 사용 여부를 제어하는 cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1797">Adding cmdlets to Disable and enable sensitivity recommendations on columns in a database.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="c16ab-1798">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="c16ab-1798">Az.Storage</span></span>
* <span data-ttu-id="c16ab-1799">스토리지 계정을 만들거나 업데이트할 때 큰 파일 공유 사용 지원</span><span class="sxs-lookup"><span data-stu-id="c16ab-1799">Support enable Large File share when create or update Storage account</span></span>
    -  <span data-ttu-id="c16ab-1800">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="c16ab-1800">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="c16ab-1801">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="c16ab-1801">Set-AzStorageAccount</span></span>
* <span data-ttu-id="c16ab-1802">파일 핸들을 닫거나/가져올 때, DeletePending 상태의 개체로 인한 오류를 방지하기 위해 입력 경로가 파일 디렉터리인지 또는 파일인지를 확인하는 과정을 건너뜁니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1802">When close/get File handle, skip check the input path is File directory or File, to avoid failure with object in DeletePending status</span></span>
    -  <span data-ttu-id="c16ab-1803">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="c16ab-1803">Get-AzStorageFileHandle</span></span>
    -  <span data-ttu-id="c16ab-1804">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="c16ab-1804">Close-AzStorageFileHandle</span></span>

## <a name="280---october-2019"></a><span data-ttu-id="c16ab-1805">2.8.0 - 2019년 10월</span><span class="sxs-lookup"><span data-stu-id="c16ab-1805">2.8.0 - October 2019</span></span>
### <a name="general"></a><span data-ttu-id="c16ab-1806">일반</span><span class="sxs-lookup"><span data-stu-id="c16ab-1806">General</span></span>
* <span data-ttu-id="c16ab-1807">Az.HealthcareApis 1.0.0 릴리스</span><span class="sxs-lookup"><span data-stu-id="c16ab-1807">Az.HealthcareApis 1.0.0 release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="c16ab-1808">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="c16ab-1808">Az.Accounts</span></span>
* <span data-ttu-id="c16ab-1809">생성된 모듈에 대한 원격 분석 및 URL 다시 작성이 업데이트되고, Windows 단위 테스트가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1809">Update telemetry and url rewriting for generated modules, fix windows unit tests.</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="c16ab-1810">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="c16ab-1810">Az.ApiManagement</span></span>
* <span data-ttu-id="c16ab-1811">**Set-AzApiManagementApi** - API 업데이트 지원이 ApiVersionSet에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1811">**Set-AzApiManagementApi** - Added support for Updating Api into ApiVersionSet</span></span>
    - <span data-ttu-id="c16ab-1812">문제 https://github.com/Azure/azure-powershell/issues/10068 수정</span><span class="sxs-lookup"><span data-stu-id="c16ab-1812">Fix for issue https://github.com/Azure/azure-powershell/issues/10068</span></span>

#### <a name="azautomation"></a><span data-ttu-id="c16ab-1813">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="c16ab-1813">Az.Automation</span></span>
* <span data-ttu-id="c16ab-1814">Linux 다시 부팅 설정 매개 변수에 대한 New-AzureAutomationSoftwareUpdateConfiguration cmdlet이 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1814">Fixed New-AzureAutomationSoftwareUpdateConfiguration cmdlet for Linux reboot setting parameter.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="c16ab-1815">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="c16ab-1815">Az.Batch</span></span>
* <span data-ttu-id="c16ab-1816">**Get-AzBatchNodeAgentSku** 가 더 이상 사용되지 않으며, 2.0.0 버전의 **Get-AzBatchSupportImage** 로 대체되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1816">**Get-AzBatchNodeAgentSku** is deprecated and will be replaced by **Get-AzBatchSupportImage** in version 2.0.0.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="c16ab-1817">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="c16ab-1817">Az.Compute</span></span>
* <span data-ttu-id="c16ab-1818">Priority, EvictionPolicy 및 MaxPrice 매개 변수가 New-AzVM 및 New-AzVmss cmdlet에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1818">Add Priority, EvictionPolicy, and MaxPrice parameters to New-AzVM and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="c16ab-1819">Add-AzVMAdditionalUnattendContent 및 Add-AzVMSshPublicKey cmdlet에 대한 경고 메시지와 도움말 문서가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1819">Fix warning message and help document for Add-AzVMAdditionalUnattendContent and Add-AzVMSshPublicKey cmdlets</span></span>
* <span data-ttu-id="c16ab-1820">Set-AzVMDiskEncryptionExtension의 관리 디스크가 있는 Linux VM에 대한 -skipVmBackup 예외가 해결되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1820">Fix -skipVmBackup exception for Linux VMs with managed disks for Set-AzVMDiskEncryptionExtension.</span></span>
* <span data-ttu-id="c16ab-1821">Set-AzVMDiskEncryptionExtension의 두 가지 패스 시나리오에서 발생하는 암호화 설정 업데이트의 버그가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1821">Fix bug in update encryption settings in Set-AzVMDiskEncryptionExtension, two pass scenario.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="c16ab-1822">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="c16ab-1822">Az.DataFactory</span></span>
* <span data-ttu-id="c16ab-1823">ADF V2 데이터 흐름에 대한 CRUD 명령으로 Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow 및 Get-AzDataFactoryV2DataFlow가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1823">Adding CRUD commands for ADF V2 data flow: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow, and Get-AzDataFactoryV2DataFlow.</span></span>
* <span data-ttu-id="c16ab-1824">ADF V2 데이터 흐름 디버그 세션에 대한 작업 명령으로 Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand 및 Stop-AzDataFactoryV2DataFlowDebugSession이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1824">Adding action commands for ADF V2 data flow debug Session: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand and Stop-AzDataFactoryV2DataFlowDebugSession.</span></span>
* <span data-ttu-id="c16ab-1825">ADF .Net SDK 버전이 4.2.0으로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1825">Update ADF .Net SDK version to 4.2.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="c16ab-1826">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="c16ab-1826">Az.DataLakeStore</span></span>
* <span data-ttu-id="c16ab-1827">도메인 없이 '-'가 있는 계정을 전달할 수 있도록 계정 유효성 검사가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1827">Fix account validation so that accounts with '-' can be passed without domain</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="c16ab-1828">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="c16ab-1828">Az.HealthcareApis</span></span>
* <span data-ttu-id="c16ab-1829">PowerShell 버전이 1.0.0으로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1829">Updated the powershell version to 1.0.0</span></span>
* <span data-ttu-id="c16ab-1830">SDK 버전이 1.0.2로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1830">Updated the SDK version to 1.0.2</span></span>
* <span data-ttu-id="c16ab-1831">새 SDK 버전을 참조하도록 테스트가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1831">Update in tests to refer to new SDK version</span></span>
* <span data-ttu-id="c16ab-1832">출력이 중첩 구조에서 평면화 구조로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1832">Updated the output structure from nested to flattened.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="c16ab-1833">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="c16ab-1833">Az.IotHub</span></span>
* <span data-ttu-id="c16ab-1834">새 라우팅 원본 추가: DigitalTwinChangeEvents</span><span class="sxs-lookup"><span data-stu-id="c16ab-1834">Add new routing source: DigitalTwinChangeEvents</span></span>
* <span data-ttu-id="c16ab-1835">사소한 버그 수정: Get-AzIothub에서 subscriptionId를 반환하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1835">Minor bug fix: Get-AzIothub not returning subscriptionId</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="c16ab-1836">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="c16ab-1836">Az.Monitor</span></span>
* <span data-ttu-id="c16ab-1837">작업 그룹에 대한 새 작업 그룹 수신기로 -ItsmReceiver, -VoiceReceiver, -ArmRoleReceiver, -AzureFunctionReceiver, -LogicAppReceiver, -AutomationRunbookReceiver, -AzureAppPushReceiver가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1837">New action group receivers added for action group   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span></span>
* <span data-ttu-id="c16ab-1838">수신기에 사용하도록 설정된 일반 경고 스키마가 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1838">Use common alert schema enabled for the receivers.</span></span> <span data-ttu-id="c16ab-1839">SMS, Azure 앱 푸시, ITSM 및 음성 수신기에는 적용되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1839">This is not applicable for SMS, Azure App push , ITSM and Voice recievers</span></span>
* <span data-ttu-id="c16ab-1840">웹후크에서 이제 Azure Active Directory 인증을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1840">Webhooks now supports Azure active directory authentication .</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="c16ab-1841">Az.Network</span><span class="sxs-lookup"><span data-stu-id="c16ab-1841">Az.Network</span></span>
* <span data-ttu-id="c16ab-1842">서비스 엔드포인트 정책에 사용할 수 있는 별칭을 가져오기 위해 호출할 수 있는 새 Get-AzAvailableServiceAlias cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1842">Add new cmdlet Get-AzAvailableServiceAlias which can be called to get the aliases that can be used for Service Endpoint Policies.</span></span>
* <span data-ttu-id="c16ab-1843">트래픽 선택기를 Virtual Network 게이트웨이 연결에 추가할 수 있는 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1843">Added support for the adding traffic selectors to Virtual Network Gateway Connections</span></span>
    - <span data-ttu-id="c16ab-1844">추가된 새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1844">New cmdlets added:</span></span>
        - <span data-ttu-id="c16ab-1845">New-AzureRmTrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="c16ab-1845">New-AzureRmTrafficSelectorPolicy</span></span>
    - <span data-ttu-id="c16ab-1846">cmdlet이 선택적인 -TrafficSelectorPolicies, -New-AzureRmVirtualNetworkGatewayConnection, -Set-AzureRmVirtualNetworkGatewayConnection 매개 변수로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1846">Cmdlets updated with optional parameter -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="c16ab-1847">ESP 및 AH 프로토콜 지원이 네트워크 보안 규칙 구성에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1847">Add support for ESP and AH protocols in network security rule configurations</span></span>
    - <span data-ttu-id="c16ab-1848">다음 Cmdlet이 업데이트 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1848">Updated cmdlets:</span></span>
        - <span data-ttu-id="c16ab-1849">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c16ab-1849">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="c16ab-1850">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c16ab-1850">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="c16ab-1851">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c16ab-1851">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="c16ab-1852">Cortex cmdlet의 예외 처리가 향상되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1852">Improve handling of exceptions in Cortex cmdlets</span></span>
* <span data-ttu-id="c16ab-1853">새 VirtualNetworkGateways 세대 및 SKU</span><span class="sxs-lookup"><span data-stu-id="c16ab-1853">New Generations and SKUs for VirtualNetworkGateways</span></span>
  - <span data-ttu-id="c16ab-1854">새 VirtualNetworkGateways 세대가 도입되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1854">Introduce new Generations for VirtualNetworkGateways.</span></span>
  - <span data-ttu-id="c16ab-1855">높은 처리량의 새 VirtualNetworkGateways SKU가 도입되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1855">Introduce new high throughput SKUs for VirtualNetworkGateways.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="c16ab-1856">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="c16ab-1856">Az.RedisCache</span></span>
* <span data-ttu-id="c16ab-1857">'-Size' 매개 변수에 대한 누락 값을 포함하도록 'Set-AzRedisCache' 참조 설명서가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1857">Updated 'Set-AzRedisCache' reference documentation to include missing values for '-Size' parameter</span></span>

#### <a name="azsql"></a><span data-ttu-id="c16ab-1858">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="c16ab-1858">Az.Sql</span></span>
* <span data-ttu-id="c16ab-1859">Managed Instance에서 Active Directory 관리자를 설정할 수 있는 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1859">Add support for setting Active Directory Administrator on Managed Instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="c16ab-1860">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="c16ab-1860">Az.Storage</span></span>
* <span data-ttu-id="c16ab-1861">스토리지 클라이언트 라이브러리가 11.1.0으로 업그레이드되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1861">Upgrade Storage Client Library to 11.1.0</span></span>
* <span data-ttu-id="c16ab-1862">관리 평면 API를 사용하여 컨테이너를 나열하면 NextPageLink를 통해 나열됩니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1862">List containers with Management plane API, will list with NextPageLink</span></span>
    -  <span data-ttu-id="c16ab-1863">Get-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="c16ab-1863">Get-AzRmStorageContainer</span></span>
* <span data-ttu-id="c16ab-1864">구독에서 스토리지 계정을 나열하면 NextPageLink를 통해 나열됩니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1864">List Storage accounts from subscription, will list with NextPageLink</span></span>
    -  <span data-ttu-id="c16ab-1865">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="c16ab-1865">Get-AzStorageAccount</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="c16ab-1866">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="c16ab-1866">Az.StorageSync</span></span>
* <span data-ttu-id="c16ab-1867">Reset-AzStorageSyncServerCertificate의 9810 문제가 해결되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1867">Fix Issue 9810 in Reset-AzStorageSyncServerCertificate.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="c16ab-1868">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="c16ab-1868">Az.Websites</span></span>
* <span data-ttu-id="c16ab-1869">앱의 ASP를 업데이트하는 Set-AzWebApp이 실패했습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1869">Set-AzWebApp updating ASP of an app was failing</span></span>

## <a name="270---september-2019"></a><span data-ttu-id="c16ab-1870">2.7.0 - 2019년 9월</span><span class="sxs-lookup"><span data-stu-id="c16ab-1870">2.7.0 - September 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="c16ab-1871">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="c16ab-1871">Az.ApiManagement</span></span>
* <span data-ttu-id="c16ab-1872">'Set-AzApiManagementPolicy' 참조 설명서에서 '-Format' 매개 변수 설명이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1872">Update '-Format' parameter description in 'Set-AzApiManagementPolicy' reference documentation</span></span>
* <span data-ttu-id="c16ab-1873">참조 설명서에서 사용되지 않는 cmdlet 'Update-AzApiManagementDeployment'의 참조를 제거했습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1873">Removed references of deprecated cmdlet 'Update-AzApiManagementDeployment' from reference documentation.</span></span> <span data-ttu-id="c16ab-1874">그 대신 'Set-AzApiManagement'를 사용하세요.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1874">Use 'Set-AzApiManagement' instead.</span></span>

#### <a name="azautomation"></a><span data-ttu-id="c16ab-1875">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="c16ab-1875">Az.Automation</span></span>
* <span data-ttu-id="c16ab-1876">'Register-AzAutomationDscNode'에 대한 참조 설명서의 예제 오타가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1876">Fixed example typo in reference documentation for 'Register-AzAutomationDscNode'</span></span>
* <span data-ttu-id="c16ab-1877">Register-AzAutomationDSCNode에 OS 제한에 대한 설명이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1877">Added clarification on OS restriction to Register-AzAutomationDSCNode</span></span>
* <span data-ttu-id="c16ab-1878">-Wait 옵션에 대한 Start-AzAutomationRunbook cmdlet Null 참조 예외가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1878">Fixed Start-AzAutomationRunbook cmdlet Null reference exception for -Wait option.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="c16ab-1879">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="c16ab-1879">Az.Compute</span></span>
* <span data-ttu-id="c16ab-1880">New-AzDiskConfig에 UploadSizeInBytes 매개 변수가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1880">Add UploadSizeInBytes parameter tp New-AzDiskConfig</span></span>
* <span data-ttu-id="c16ab-1881">New-AzSnapshotConfig에 증분 매개 변수가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1881">Add Incremental parameter to New-AzSnapshotConfig</span></span>
* <span data-ttu-id="c16ab-1882">다음과 같은 낮은 우선 순위의 가상 머신 기능이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1882">Add a low priority virtual machine feature:</span></span>
    - <span data-ttu-id="c16ab-1883">MaxPrice, EvictionPolicy 및 Priority 매개 변수가 New-AzVMConfig에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1883">MaxPrice, EvictionPolicy and Priority parameters are added to New-AzVMConfig.</span></span>
    - <span data-ttu-id="c16ab-1884">MaxPrice 매개 변수는 New-AzVmssConfig, Update-AzVM 및 Update-AzVmss cmdlet에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1884">MaxPrice parameter is added to New-AzVmssConfig, Update-AzVM and Update-AzVmss cmdlets.</span></span>
* <span data-ttu-id="c16ab-1885">구독의 모든 가용성 세트를 나열할 때 발생하는 Get-AzAvailabilitySet cmdlet에 대한 VM 참조 이슈가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1885">Fix VM reference issue for Get-AzAvailabilitySet cmdlet when it lists all availability sets in the subscription.</span></span>
* <span data-ttu-id="c16ab-1886">Get-AzRemoteDesktopFile에 대한 null 예외가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1886">Fix the null exception for Get-AzRemoteDesktopFile.</span></span>
* <span data-ttu-id="c16ab-1887">종료 상대 위치에 대한 VHD 검색 메서드가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1887">Fix VHD Seek method for end-relative position.</span></span>
* <span data-ttu-id="c16ab-1888">New-AzVM 및 Update-AzVM에 대한 UltraSSD 이슈가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1888">Fix UltraSSD issue for New-AzVM and Update-AzVM.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="c16ab-1889">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="c16ab-1889">Az.DataFactory</span></span>
* <span data-ttu-id="c16ab-1890">ADF V2에 대한 3가지 새 명령 Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription 및 Get-AzDataFactoryV2TriggerSubscriptionStatus가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1890">Adding 3 new commands for ADF V2 - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription, and Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>
* <span data-ttu-id="c16ab-1891">ADF .Net SDK 버전이 4.1.3으로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1891">Updated ADF .Net SDK version to 4.1.3</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="c16ab-1892">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="c16ab-1892">Az.HDInsight</span></span>
* <span data-ttu-id="c16ab-1893">호출 주요 변경 내용</span><span class="sxs-lookup"><span data-stu-id="c16ab-1893">Call out breaking changes</span></span>

#### <a name="aziothub"></a><span data-ttu-id="c16ab-1894">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="c16ab-1894">Az.IotHub</span></span>
* <span data-ttu-id="c16ab-1895">지역 쌍 재해 복구 지역에 IotHub에 대한 장애 조치(failover) 호출 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1895">Add support to invoke failover for an IotHub to the geo-paired disaster recovery region.</span></span>
* <span data-ttu-id="c16ab-1896">IotHub에 대한 메시지 보강 관리 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1896">Add support to manage message enrichment for an IotHub.</span></span> <span data-ttu-id="c16ab-1897">새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1897">New cmdlets are:</span></span>
    - <span data-ttu-id="c16ab-1898">Add-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="c16ab-1898">Add-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="c16ab-1899">Get-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="c16ab-1899">Get-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="c16ab-1900">Remove-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="c16ab-1900">Remove-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="c16ab-1901">Set-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="c16ab-1901">Set-AzIotHubMessageEnrichment</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="c16ab-1902">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="c16ab-1902">Az.Monitor</span></span>
* <span data-ttu-id="c16ab-1903">최신 모니터링 SDK, 즉, 0.24.1-preview를 가리킵니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1903">Pointing to the most recent Monitor SDK, i.e. 0.24.1-preview</span></span>
   - <span data-ttu-id="c16ab-1904">메트릭 cmdlet에 줄 바꿈하지 않는 변경 내용을 추가합니다. 즉, 단위 열거형은 여러 새 값을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1904">Adds non-braking changes to the Metrics cmdlets, i.e. the Unit enumeration supports several new values.</span></span> <span data-ttu-id="c16ab-1905">이러한 cmdlet은 읽기 전용이므로 cmdlet 입력이 변경되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1905">These are read-only cmdlets, so there would be no change in the input of the cmdlets.</span></span>
   - <span data-ttu-id="c16ab-1906">이제 **ActionGroups** 요청의 api 버전은 **2019-06-01** 이고, 이전에는 **2018-03-01** 였습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1906">The api-version of the **ActionGroups** requests is now **2019-06-01** , before it was **2018-03-01**.</span></span> <span data-ttu-id="c16ab-1907">시나리오 테스트가 이 변경 내용에 맞게 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1907">The scenario tests have been updated to accommodate for this change.</span></span>
   - <span data-ttu-id="c16ab-1908">**EmailReceiver** 및 **WebhookReceiver** 클래스에 대한 생성자가 새 필수 인수, 즉, **useCommonAlertSchema** 라는 부울 값을 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1908">The constructors for the classes **EmailReceiver** and **WebhookReceiver** added one new mandatory argument, i.e. a Boolean value called **useCommonAlertSchema**.</span></span> <span data-ttu-id="c16ab-1909">현재 이 값은 cmdlet의 주요 변경 사항을 숨기도록 **false** 로 고정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1909">Currently, the value is fixed to **false** to hide this breaking change from the cmdlets.</span></span> <span data-ttu-id="c16ab-1910">**참고** : 이 변경 사항은 경고 팀에서 유효성을 검사해야 하는 임시 변경 내용입니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1910">**NOTE** : this is a temporary change that must be validated by the Alerts team.</span></span>
   - <span data-ttu-id="c16ab-1911">이전 SDK에서 변경된 **Source** 클래스( **ScheduledQueryRuleSource** 클래스와 관련됨)의 생성자에 대한 인수 순서입니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1911">The order of the arguments for the constructor of the class **Source** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="c16ab-1912">이번 변화로 인해 두 개의 단위 테스트를 수정해야 했습니다. 즉, 두 단위 테스트가 컴파일되었지만 테스트를 통과하지 못했습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1912">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
   - <span data-ttu-id="c16ab-1913">이전 SDK에서 변경된 **AlertingAction** 클래스( **ScheduledQueryRuleSource** 클래스와 관련됨)의 생성자에 대한 인수 순서입니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1913">The order of the arguments for the constructor of the class **AlertingAction** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="c16ab-1914">이번 변화로 인해 두 개의 단위 테스트를 수정해야 했습니다. 즉, 두 단위 테스트가 컴파일되었지만 테스트를 통과하지 못했습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1914">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
* <span data-ttu-id="c16ab-1915">메트릭 경고 V2에 대한 동적 임계값 기준 지원</span><span class="sxs-lookup"><span data-stu-id="c16ab-1915">Support Dynamic Threshold criteria for metric alert V2</span></span>
    - <span data-ttu-id="c16ab-1916">AzMetricAlertRuleV2Criteria: 이제 동적 임계값 조건도 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1916">New-AzMetricAlertRuleV2Criteria: now creats dynamic threshold criteria also</span></span>
    - <span data-ttu-id="c16ab-1917">Add-AzMetricAlertRuleV2: 이제 동적 임계값 조건도 수락합니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1917">Add-AzMetricAlertRuleV2: now accept dynamic threshold criteria also</span></span>
* <span data-ttu-id="c16ab-1918">SQR(예약된 쿼리 규칙)의 향상된 기능</span><span class="sxs-lookup"><span data-stu-id="c16ab-1918">Improvements in Scheduled Query Rule cmdlets (SQR)</span></span>
 - <span data-ttu-id="c16ab-1919">Cmdlet이 'Location' 매개 변수를 두 가지 형식(eastus 같은 위치 또는 미국 동부 같은 위치 표시 이름)으로 모두 허용합니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1919">Cmdlets will accept 'Location' paramater in both formats, either the location (e.g. eastus) or the location display name (e.g. East US)</span></span>
 - <span data-ttu-id="c16ab-1920">도움말 파일에 적절하게 표시된 'Enabled' 매개 변수</span><span class="sxs-lookup"><span data-stu-id="c16ab-1920">Illustrated 'Enabled' parameter in help files properly</span></span>
 - <span data-ttu-id="c16ab-1921">선택적 매개 변수 'ActionGroup'에 대한 예제가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1921">Added examples for 'ActionGroup' optional parameter</span></span>
 - <span data-ttu-id="c16ab-1922">도움말 파일이 전체적으로 개선되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1922">Overall improved help files</span></span>
* <span data-ttu-id="c16ab-1923">'Set-AzActionRule'의 범위 유형 결정 버그를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1923">Fix bug in determining scope type for 'Set-AzActionRule'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="c16ab-1924">Az.Network</span><span class="sxs-lookup"><span data-stu-id="c16ab-1924">Az.Network</span></span>
* <span data-ttu-id="c16ab-1925">'New-AzApplicationGateway' 참조 설명서의 잘못된 예제가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1925">Fix incorrect example in 'New-AzApplicationGateway' reference documentation</span></span>
* <span data-ttu-id="c16ab-1926">'Get-AzNetworkWatcherPacketCapture' 참조 설명서에 패킷 캡처를 위한 모든 속성 검색과 관련된 메모가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1926">Add note in 'Get-AzNetworkWatcherPacketCapture' reference documentation about retrieving all properties for a packet capture</span></span>
* <span data-ttu-id="c16ab-1927">NIC를 올바르게 열거하도록 'Test-AzNetworkWatcherIPFlow' 참조 설명서의 예제가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1927">Fixed example in 'Test-AzNetworkWatcherIPFlow' reference documentation to correctly enumerate NICs</span></span>
* <span data-ttu-id="c16ab-1928">추가 세부 정보가 있는 경우 추가 세부 정보를 표시하도록 클라우드 예외 구문 분석이 향상되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1928">Improved cloud exception parsing to display additional details if they are present</span></span>
* <span data-ttu-id="c16ab-1929">더 많은 형식의 SDK 예외를 처리하도록 클라우드 예외 구문 분석이 향상되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1929">Improved cloud exception parsing to handle additional type of SDK exception</span></span>
* <span data-ttu-id="c16ab-1930">보안 규칙 모델의 잘못된 매핑이 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1930">Fixed incorrect mapping of Security Rule models</span></span>
* <span data-ttu-id="c16ab-1931">네트워크 인터페이스에 개인 IP 기능을 위한 속성이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1931">Added properties to network interface for private ip feature</span></span>
    - <span data-ttu-id="c16ab-1932">PSNetworkInterface에 'PrivateEndpoint' 속성이 PSResourceId 형식으로 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1932">Added property 'PrivateEndpoint' as type of PSResourceId to PSNetworkInterface</span></span>
    - <span data-ttu-id="c16ab-1933">PSNetworkInterfaceIPConfiguration에 'PrivateLinkConnectionProperties' 속성이 PSIpConfigurationConnectivityInformation 형식으로 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1933">Added property 'PrivateLinkConnectionProperties' as type of PSIpConfigurationConnectivityInformation to PSNetworkInterfaceIPConfiguration</span></span>
    - <span data-ttu-id="c16ab-1934">새 모델 클래스 PSIpConfigurationConnectivityInformation이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1934">Added new model class PSIpConfigurationConnectivityInformation</span></span>
* <span data-ttu-id="c16ab-1935">Azure Firewall 리소스에 대한 새 ApplicationRuleProtocolType 'mssql'이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1935">Added new ApplicationRuleProtocolType 'mssql' for Azure Firewall resource</span></span>
* <span data-ttu-id="c16ab-1936">Virtual WAN에서 멀티 링크를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1936">MultiLink support in Virtual WAN</span></span>
    - <span data-ttu-id="c16ab-1937">새로운 cmdlet</span><span class="sxs-lookup"><span data-stu-id="c16ab-1937">New cmdlets</span></span>
        - <span data-ttu-id="c16ab-1938">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="c16ab-1938">New-AzVpnSiteLink</span></span>
        - <span data-ttu-id="c16ab-1939">New-AzVpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="c16ab-1939">New-AzVpnSiteLinkConnection</span></span>
    - <span data-ttu-id="c16ab-1940">업데이트된 cmdlet:</span><span class="sxs-lookup"><span data-stu-id="c16ab-1940">Updated cmdlet:</span></span>
        - <span data-ttu-id="c16ab-1941">New-VpnSite</span><span class="sxs-lookup"><span data-stu-id="c16ab-1941">New-VpnSite</span></span>
        - <span data-ttu-id="c16ab-1942">Update-VpnSite</span><span class="sxs-lookup"><span data-stu-id="c16ab-1942">Update-VpnSite</span></span>
        - <span data-ttu-id="c16ab-1943">New-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="c16ab-1943">New-VpnConnection</span></span>
        - <span data-ttu-id="c16ab-1944">Update-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="c16ab-1944">Update-VpnConnection</span></span>
* <span data-ttu-id="c16ab-1945">AzureRM cmdlet 대신 Az cmdlet을 사용하도록 일부 PowerShell 예제의 문서가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1945">Fixed documents for some PowerShell examples to use Az cmdlets instead of AzureRM cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="c16ab-1946">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="c16ab-1946">Az.RecoveryServices</span></span>
* <span data-ttu-id="c16ab-1947">AzureVMpolicy 개체가 ProtectedItemsCount 특성으로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1947">Update AzureVMpolicy Object with ProtectedItemsCount Attribute</span></span>
* <span data-ttu-id="c16ab-1948">VM 정책 및 원래 스토리지 계정 복원에 대한 테스트가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1948">Added Tests for VM policy and Original Storage Account Restore</span></span>

#### <a name="azresources"></a><span data-ttu-id="c16ab-1949">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="c16ab-1949">Az.Resources</span></span>
* <span data-ttu-id="c16ab-1950">매개 변수 범위 없이 AzRoleAssignment를 호출할 수 없는 버그가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1950">Fix bug where New-AzRoleAssignment could not be called without parameter Scope.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="c16ab-1951">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="c16ab-1951">Az.ServiceFabric</span></span>
* <span data-ttu-id="c16ab-1952">'AzServiceFabricReliability' 참조 설명서에 대한 예제의 오타가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1952">Fixed typo in example for 'Update-AzServiceFabricReliability' reference documentation</span></span>
* <span data-ttu-id="c16ab-1953">애플리케이션 및 서비스를 관리하는 다음과 같은 새 cmdlet이 추가됩니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1953">Adding new cmdlets to manage appliaction and services:</span></span>
    - <span data-ttu-id="c16ab-1954">New-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="c16ab-1954">New-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="c16ab-1955">New-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="c16ab-1955">New-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="c16ab-1956">New-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="c16ab-1956">New-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="c16ab-1957">New-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="c16ab-1957">New-AzServiceFabricService</span></span>
    - <span data-ttu-id="c16ab-1958">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="c16ab-1958">Update-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="c16ab-1959">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="c16ab-1959">Get-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="c16ab-1960">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="c16ab-1960">Get-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="c16ab-1961">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="c16ab-1961">Get-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="c16ab-1962">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="c16ab-1962">Get-AzServiceFabricService</span></span>
    - <span data-ttu-id="c16ab-1963">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="c16ab-1963">Remove-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="c16ab-1964">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="c16ab-1964">Remove-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="c16ab-1965">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="c16ab-1965">Remove-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="c16ab-1966">Remove-AzServiceFabricServic</span><span class="sxs-lookup"><span data-stu-id="c16ab-1966">Remove-AzServiceFabricServic</span></span>
* <span data-ttu-id="c16ab-1967">Service Fabric SDK가 Service Fabric 리소스 공급자 api 버전 2019-03-01을 사용하는 1.2.0 버전으로 업그레이드되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1967">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2019-03-01.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="c16ab-1968">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="c16ab-1968">Az.SignalR</span></span>
* <span data-ttu-id="c16ab-1969">Update, Restart, CheckNameAvailability, GetUsage Cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1969">Add Update, Restart, CheckNameAvailability, GetUsage Cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="c16ab-1970">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="c16ab-1970">Az.Sql</span></span>
* <span data-ttu-id="c16ab-1971">'Get-AzSqlElasticPool'에 대한 참조 설명서의 예제가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1971">Update example in reference documentation for 'Get-AzSqlElasticPool'</span></span>
* <span data-ttu-id="c16ab-1972">탄력적 풀을 만드는 vCore 예제가 추가되었습니다(AzSqlElasticPool).</span><span class="sxs-lookup"><span data-stu-id="c16ab-1972">Added vCore example to creating an elastic pool (New-AzSqlElasticPool).</span></span>
* <span data-ttu-id="c16ab-1973">Set-AzSqlServerAdvancedThreatProtectionPolicy 및 Set-AzSqlDatabaseAdvancedThreatProtectionPolicy에서 EmailAddresses가 비어 있는 경우 EmailAddresses의 유효성을 검사하고 EmailAdmins가 false가 아닌지 확인하는 기능이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1973">Remove the validation of EmailAddresses and the check that EmailAdmins is not false in case EmailAddresses is empty in Set-AzSqlServerAdvancedThreatProtectionPolicy and Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="c16ab-1974">감사 범주를 사용하는 여러 진단 설정이 있는 경우 서버/데이터베이스 감사 설정을 제거하도록 설정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1974">Enabled removal of server/database auditing settings when multiple diagnostic settings that enable audit category exist.</span></span>
* <span data-ttu-id="c16ab-1975">여러 Sql 취약성 평가 cmdlet에서 이메일 주소 유효성 검사가 수정되었습니다(Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting 및 Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span><span class="sxs-lookup"><span data-stu-id="c16ab-1975">Fix email addresses validation in multiple Sql Vulnerability Assessment cmdlets (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting and Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span></span>

#### <a name="azstorage"></a><span data-ttu-id="c16ab-1976">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="c16ab-1976">Az.Storage</span></span>
* <span data-ttu-id="c16ab-1977">'Get-AzStorageAccountKey'에 대한 참조 설명서의 예제가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1977">Updated example in reference documentation for 'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="c16ab-1978">Azure 파일 업로드/다운에서, 원본 파일 SMB 속성(파일 특성, 파일 생성 시간, 파일을 마지막으로 쓴 시간)을 대상 파일에 보존하는 기능이 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1978">In upload/Downalod Azure File,support perserve the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the destination file</span></span>
    -  <span data-ttu-id="c16ab-1979">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="c16ab-1979">Set-AzStorageFileContent</span></span>
    -  <span data-ttu-id="c16ab-1980">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="c16ab-1980">Get-AzStorageFileContent</span></span>
* <span data-ttu-id="c16ab-1981">컨테이너가 사용되는 ImmutabilityPolicy에서 properties/metadate fail을 사용하여 블록 Blob 업로드가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1981">Fix Upload block blob with properties/metadate fail on container enabled ImmutabilityPolicy.</span></span>
    -  <span data-ttu-id="c16ab-1982">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="c16ab-1982">Set-AzStorageBlobContent</span></span>
* <span data-ttu-id="c16ab-1983">관리 평면 API를 사용하여 Azure 파일 공유 관리를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1983">Support manage Azure File shares with Management plane API</span></span>
    -  <span data-ttu-id="c16ab-1984">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="c16ab-1984">New-AzRmStorageShare</span></span>
    -  <span data-ttu-id="c16ab-1985">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="c16ab-1985">Get-AzRmStorageShare</span></span>
    -  <span data-ttu-id="c16ab-1986">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="c16ab-1986">Update-AzRmStorageShare</span></span>
    -  <span data-ttu-id="c16ab-1987">Remove-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="c16ab-1987">Remove-AzRmStorageShare</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="c16ab-1988">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="c16ab-1988">Az.Websites</span></span>
* <span data-ttu-id="c16ab-1989">앱을 새 ASP로 마이그레이션할 때 웹앱 태그가 삭제되는 이슈가 해결되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1989">Fixing issue where webapp Tags were getting deleted when migrating App to new ASPwhere webapp Tags were getting deleted when migrating App to new ASP</span></span>
* <span data-ttu-id="c16ab-1990">Linux와 Windows에서 모두 작동하도록 Publish-AzureWebapp이 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1990">Fixing the Publish-AzureWebapp to work across Linux and windows</span></span>
* <span data-ttu-id="c16ab-1991">'Get-AzWebAppPublishingProfile' 참조 설명서의 예제가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1991">Update example in 'Get-AzWebAppPublishingProfile' reference documentation</span></span>

## <a name="260---august-2019"></a><span data-ttu-id="c16ab-1992">2.6.0 - 2019년 8월</span><span class="sxs-lookup"><span data-stu-id="c16ab-1992">2.6.0 - August 2019</span></span>
#### <a name="general"></a><span data-ttu-id="c16ab-1993">일반</span><span class="sxs-lookup"><span data-stu-id="c16ab-1993">General</span></span>
* <span data-ttu-id="c16ab-1994">여러 모듈에서 기타 오타가 수정됨</span><span class="sxs-lookup"><span data-stu-id="c16ab-1994">Fixed miscellaneous typos across numerous modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="c16ab-1995">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="c16ab-1995">Az.Accounts</span></span>
* <span data-ttu-id="c16ab-1996">Azure Functions 인증에서 사용자가 할당한 MSI가 지원됨(# 9479)</span><span class="sxs-lookup"><span data-stu-id="c16ab-1996">Support user-assigned MSI in Azure Functiosn Authentication (#9479)</span></span>

#### <a name="azaks"></a><span data-ttu-id="c16ab-1997">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="c16ab-1997">Az.Aks</span></span>
* <span data-ttu-id="c16ab-1998">'Get-AzAks' 출력 관련 문제가 해결됨</span><span class="sxs-lookup"><span data-stu-id="c16ab-1998">Fix issue with output for 'Get-AzAks'</span></span>
    * <span data-ttu-id="c16ab-1999">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/9847 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="c16ab-1999">More information here: https://github.com/Azure/azure-powershell/issues/9847</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="c16ab-2000">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="c16ab-2000">Az.ApiManagement</span></span>
* <span data-ttu-id="c16ab-2001">문제 https://github.com/Azure/azure-powershell/issues/9351 수정</span><span class="sxs-lookup"><span data-stu-id="c16ab-2001">Fix for issue https://github.com/Azure/azure-powershell/issues/9351</span></span>
    - <span data-ttu-id="c16ab-2002">productId, apiId, groupId 및 userId에 대한 제한을 적용하지 않는 .Net NuGet 버전이 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="c16ab-2002">Update .net nuget version, which does not enforce restrictions on productId, apiId, groupId and userId</span></span>
* <span data-ttu-id="c16ab-2003">**Get-AzApiManagementProduct** - API를 사용하는 제품에 대한 쿼리 지원이 추가됨</span><span class="sxs-lookup"><span data-stu-id="c16ab-2003">**Get-AzApiManagementProduct** - Added support for querying products using Api.</span></span>
  https://github.com/Azure/azure-powershell/issues/9482
* <span data-ttu-id="c16ab-2004">**New-AzApiManagementApiRevision** - 새 API 수정(https://github.com/Azure/azure-powershell/issues/9752 )을 만들 때 ApiRevisionDescription이 설정되지 않은 문제가 해결됨</span><span class="sxs-lookup"><span data-stu-id="c16ab-2004">**New-AzApiManagementApiRevision** - Fix for issue where ApiRevisionDescription was not being set when creating new api revision https://github.com/Azure/azure-powershell/issues/9752</span></span>
* <span data-ttu-id="c16ab-2005">'PsApiManagementOAuth2AuthrozationServer' 모델의 오타가 'PsApiManagementOAuth2AuthorizationServer'로 수정됨</span><span class="sxs-lookup"><span data-stu-id="c16ab-2005">Fixed typo in model 'PsApiManagementOAuth2AuthrozationServer' to 'PsApiManagementOAuth2AuthorizationServer'</span></span>

#### <a name="azbatch"></a><span data-ttu-id="c16ab-2006">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="c16ab-2006">Az.Batch</span></span>
* <span data-ttu-id="c16ab-2007">도움말 메시지 및 설명서에서 Windows를 대문자로 시작하도록 오타가 수정됨</span><span class="sxs-lookup"><span data-stu-id="c16ab-2007">Fixed typo in help message and documentation to capitalize Windows</span></span>

#### <a name="azcdn"></a><span data-ttu-id="c16ab-2008">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="c16ab-2008">Az.Cdn</span></span>
* <span data-ttu-id="c16ab-2009">CDN 모듈 변환 도우미의 오타가 수정됨</span><span class="sxs-lookup"><span data-stu-id="c16ab-2009">Fixed a typo in CDN module conversion helper</span></span>

#### <a name="azcompute"></a><span data-ttu-id="c16ab-2010">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="c16ab-2010">Az.Compute</span></span>
* <span data-ttu-id="c16ab-2011">VmssId가 New-AzVMConfig cmdlet에 추가됨</span><span class="sxs-lookup"><span data-stu-id="c16ab-2011">Add VmssId to New-AzVMConfig cmdlet</span></span>
* <span data-ttu-id="c16ab-2012">TerminateScheduledEvents 및 TerminateScheduledEventNotBeforeTimeoutInMinutes 매개 변수가 New-AzVmssConfig 및 Update-AzVmss에 추가됨</span><span class="sxs-lookup"><span data-stu-id="c16ab-2012">Add TerminateScheduledEvents and TerminateScheduledEventNotBeforeTimeoutInMinutes parameters to New-AzVmssConfig and Update-AzVmss</span></span>
* <span data-ttu-id="c16ab-2013">HyperVGeneration 속성이 VM 이미지 개체에 추가됨</span><span class="sxs-lookup"><span data-stu-id="c16ab-2013">Add HyperVGeneration property to VM image object</span></span>
* <span data-ttu-id="c16ab-2014">Host 및 HostGroup 기능이 추가됨</span><span class="sxs-lookup"><span data-stu-id="c16ab-2014">Add Host and HostGroup features</span></span>
    - <span data-ttu-id="c16ab-2015">새 cmdlet:   New-AzHostGroup, New-AzHost, Get-AzHostGroup, Get-AzHost, Remove-AzHostGroup, Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="c16ab-2015">New cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span></span>
    - <span data-ttu-id="c16ab-2016">HostId 매개 변수가 New-AzVMConfig 및 New-AzVM 추가됨</span><span class="sxs-lookup"><span data-stu-id="c16ab-2016">HostId parameter is added to New-AzVMConfig and New-AzVM</span></span>
* <span data-ttu-id="c16ab-2017">'Invoke-AzVMRunCommand' 설명서의 예제에서 올바른 매개 변수 이름을 사용하도록 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="c16ab-2017">Update example in 'Invoke-AzVMRunCommand' documentation to use correct parameter name</span></span>
* <span data-ttu-id="c16ab-2018">'Set-AzVMDiskEncryptionExtension' 및 'Set-AzVmssDiskEncryptionExtension' 참조 설명서의 '-VolumeType' 설명이 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="c16ab-2018">Update '-VolumeType' description in 'Set-AzVMDiskEncryptionExtension' and 'Set-AzVmssDiskEncryptionExtension' reference documentation</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="c16ab-2019">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="c16ab-2019">Az.DataFactory</span></span>
* <span data-ttu-id="c16ab-2020">'New-AzDataFactoryEncryptValue' 설명서에서 'Windows'를 대문자로 시작하도록 오타가 수정됨</span><span class="sxs-lookup"><span data-stu-id="c16ab-2020">Fix typo to capitalize 'Windows' in 'New-AzDataFactoryEncryptValue' documentation</span></span>
* <span data-ttu-id="c16ab-2021">ADF .Net SDK 버전이 4.1.2로 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="c16ab-2021">Updated ADF .Net SDK version to 4.1.2</span></span>
* <span data-ttu-id="c16ab-2022">자체 호스팅 통합 런타임을 SSIS Integration Runtime의 프록시로 설정할 수 있도록 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' 및 'DataProxyStagingPath' 매개 변수가 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd에 추가됨</span><span class="sxs-lookup"><span data-stu-id="c16ab-2022">Add parameter 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' and 'DataProxyStagingPath' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable set up Self-Hosted Integration Runtime as a proxy for SSIS Integration Runtime</span></span>
* <span data-ttu-id="c16ab-2023">PSTriggerRun에서 트리거된 파이프라인, 메시지 및 속성을 표시하고, PSActivityRun에서 작업 유형을 표시하도록 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="c16ab-2023">Updated PSTriggerRun to show the triggered pipelines, message and properties, and PSActivityRun to show the activity type</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="c16ab-2024">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="c16ab-2024">Az.DataLakeStore</span></span>
* <span data-ttu-id="c16ab-2025">오류 또는 원격 예외에 대한 Get-DataLakeStoreDeletedItem 중단이 수정됨</span><span class="sxs-lookup"><span data-stu-id="c16ab-2025">Fix hanging of Get-DataLakeStoreDeletedItem for any errors or remote exceptions.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="c16ab-2026">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="c16ab-2026">Az.EventHub</span></span>
* <span data-ttu-id="c16ab-2027">#9658 문제 해결: Set-AzEventHubNetworkRuleSet의 VirtualNteworkRule 매개 변수에 대한 오타</span><span class="sxs-lookup"><span data-stu-id="c16ab-2027">Fix for issue #9658 : Typo VirtualNteworkRule parameter in Set-AzEventHubNetworkRuleSet</span></span>
* <span data-ttu-id="c16ab-2028">#9558 문제 해결: Set-AzEventHubNamespace에서 PUT 대신 PATCH가 사용됨</span><span class="sxs-lookup"><span data-stu-id="c16ab-2028">Fix for issue #9558 : Set-AzEventHubNamespace is using PATCH instead of PUT</span></span>
* <span data-ttu-id="c16ab-2029">EnableKafka 매개 변수가 Set-AzEventHubNamespace cmdlet에 추가됨</span><span class="sxs-lookup"><span data-stu-id="c16ab-2029">added EnableKafka parameter to Set-AzEventHubNamespace cmdlet</span></span>
* <span data-ttu-id="c16ab-2030">#9786 문제 해결: Listen(수신 대기) 전용 권한이 있는 규칙을 만들 수 없음</span><span class="sxs-lookup"><span data-stu-id="c16ab-2030">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>

#### <a name="azmarketplaceordering"></a><span data-ttu-id="c16ab-2031">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="c16ab-2031">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="c16ab-2032">'Azure'가 모두 소문자인 설명서의 오타가 수정됨</span><span class="sxs-lookup"><span data-stu-id="c16ab-2032">Fixed documentation typo where 'Azure' was all lowercase letters</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="c16ab-2033">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="c16ab-2033">Az.Monitor</span></span>
* <span data-ttu-id="c16ab-2034">도움말 설명서에서 잘못된 매개 변수 이름이 수정됨</span><span class="sxs-lookup"><span data-stu-id="c16ab-2034">Fixed incorrect parameter name in help documentation</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="c16ab-2035">Az.Network</span><span class="sxs-lookup"><span data-stu-id="c16ab-2035">Az.Network</span></span>
* <span data-ttu-id="c16ab-2036">New-AzPrivateLinkServiceIpConfig가 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="c16ab-2036">Updated New-AzPrivateLinkServiceIpConfig</span></span>
    - <span data-ttu-id="c16ab-2037">서버 쪽에서 사용되지 않으므로 'PublicIpAddress' 매개 변수가 사용되지 않음</span><span class="sxs-lookup"><span data-stu-id="c16ab-2037">Deprecated the paramster 'PublicIpAddress' since this is never used in the server side.</span></span>
    - <span data-ttu-id="c16ab-2038">현재 IP 구성이 기본 구성인지 여부를 나타내는 하나의 선택적 'Primary' 매개 변수가 추가됨</span><span class="sxs-lookup"><span data-stu-id="c16ab-2038">Added one optional parameter 'Primary' that indicate the current ip configuration is primary one or not.</span></span>
* <span data-ttu-id="c16ab-2039">SDK의 요청 오류 예외 처리가 향상됨 - 이전의 SDK 예외가 올바르게 처리되지 않아 주요 오류 세부 정보가 표시되지 않은 문제가 해결됨</span><span class="sxs-lookup"><span data-stu-id="c16ab-2039">Improved handling of request error exception from SDK   -Fixes the issue that previously SDK exceptions aren't handled correctly which results in key error details not being displayed</span></span>
* <span data-ttu-id="c16ab-2040">올바른 IPv6 접두사 길이를 확인하기 위해 Ipv6 IP 접두사에 대한 유효성 검사 논리가 조정됨</span><span class="sxs-lookup"><span data-stu-id="c16ab-2040">Adjusted validation logic for Ipv6 IP Prefix to check for correct IPv6 prefix length.</span></span>
* <span data-ttu-id="c16ab-2041">Get-AzVirtualNetworkSubnetConfig가 업데이트됨: 서브넷 리소스 ID별로 가져오도록 설정되는 매개 변수 세트가 추가됨</span><span class="sxs-lookup"><span data-stu-id="c16ab-2041">Updated Get-AzVirtualNetworkSubnetConfig: Added parameter set to get by subnet resource id.</span></span>
* <span data-ttu-id="c16ab-2042">AzNetworkServiceTag의 Location(위치) 매개 변수에 대한 설명이 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="c16ab-2042">Updated description of Location parameter for AzNetworkServiceTag</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="c16ab-2043">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="c16ab-2043">Az.OperationalInsights</span></span>
* <span data-ttu-id="c16ab-2044">'New-AzOperationalInsightsLinuxSyslogDataSource'에 대한 설명서가 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="c16ab-2044">Updated documentation for 'New-AzOperationalInsightsLinuxSyslogDataSource'</span></span>
    - <span data-ttu-id="c16ab-2045">예제가 추가됨</span><span class="sxs-lookup"><span data-stu-id="c16ab-2045">Added example</span></span>
    - <span data-ttu-id="c16ab-2046">'-Name' 매개 변수에 대한 설명이 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="c16ab-2046">Updated description for '-Name' parameter</span></span>
* <span data-ttu-id="c16ab-2047">New-AzOperationalInsightsWindowsEventDataSource에 대한 예제가 추가됨</span><span class="sxs-lookup"><span data-stu-id="c16ab-2047">Added an example for New-AzOperationalInsightsWindowsEventDataSource</span></span>
* <span data-ttu-id="c16ab-2048">New-AzOperationalInsightsWindowsEventDataSource의 -Name 매개 변수에 대한 설명이 변경됨</span><span class="sxs-lookup"><span data-stu-id="c16ab-2048">Changed the description of the -Name parameter for New-AzOperationalInsightsWindowsEventDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="c16ab-2049">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="c16ab-2049">Az.RecoveryServices</span></span>
* <span data-ttu-id="c16ab-2050">'Get-AzRecoveryServicesBackupJobDetail.md'가 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="c16ab-2050">Update 'Get-AzRecoveryServicesBackupJobDetail.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="c16ab-2051">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="c16ab-2051">Az.Resources</span></span>
* <span data-ttu-id="c16ab-2052">Microsoft 리소스에 대한 새 2019-05-10 API 버전 지원이 추가됨</span><span class="sxs-lookup"><span data-stu-id="c16ab-2052">Add support for new api version 2019-05-10 for Microsoft.Resource</span></span>
    - <span data-ttu-id="c16ab-2053">변수, 리소스 및 속성에 대한 'copy.count = 0' 지원이 추가됨</span><span class="sxs-lookup"><span data-stu-id="c16ab-2053">Add support for 'copy.count = 0' for variables, resources and properties</span></span>
    - <span data-ttu-id="c16ab-2054">'condition = false' 또는 'copy.count = 0'인 리소스가 완료 모드에서 삭제됨</span><span class="sxs-lookup"><span data-stu-id="c16ab-2054">Resources with 'condition = false' or 'copy.count = 0' will be deleted in complete mode</span></span>
* <span data-ttu-id="c16ab-2055">정책을 구독 수준에서 도움말 문서에 할당하는 예제가 추가됨</span><span class="sxs-lookup"><span data-stu-id="c16ab-2055">Add an example of assigning policy at subscription level to help doc</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="c16ab-2056">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="c16ab-2056">Az.ServiceBus</span></span>
* <span data-ttu-id="c16ab-2057">#9658 문제 해결: Set-AzServiceBusNetworkRuleSet의 VirtualNetworkRule 매개 변수에 대한 오타</span><span class="sxs-lookup"><span data-stu-id="c16ab-2057">Fix for issue #9658 : Typo VirtualNetworkRule parameter in Set-AzServiceBusNetworkRuleSet</span></span>
* <span data-ttu-id="c16ab-2058">#9786 문제 해결: Listen(수신 대기) 전용 권한이 있는 규칙을 만들 수 없음</span><span class="sxs-lookup"><span data-stu-id="c16ab-2058">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>
* <span data-ttu-id="c16ab-2059">큐 및 토픽에 대한 이름 가용성을 확인하는 새 'Test-AzServiceBusNameAvailability' 명령이 추가됨</span><span class="sxs-lookup"><span data-stu-id="c16ab-2059">Added new command 'Test-AzServiceBusNameAvailability' to check the name availability for queue and topic</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="c16ab-2060">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="c16ab-2060">Az.ServiceFabric</span></span>
* <span data-ttu-id="c16ab-2061">노드 유형 추가 cmdlet 버그 수정:</span><span class="sxs-lookup"><span data-stu-id="c16ab-2061">Fix add node type cmdlet bugs:</span></span>
    - <span data-ttu-id="c16ab-2062">서비스 패브릭 클러스터와 관련이 없는 다른 vmss가 리소스 그룹에 있을 때 발생하는 NullReferenceException 버그</span><span class="sxs-lookup"><span data-stu-id="c16ab-2062">NullReferenceException bug when resource group had other vmss not related to the service fabric cluster.</span></span> <span data-ttu-id="c16ab-2063">문제 해결: https://github.com/Azure/azure-powershell/issues/8681</span><span class="sxs-lookup"><span data-stu-id="c16ab-2063">Fixes issue: https://github.com/Azure/azure-powershell/issues/8681</span></span>
    - <span data-ttu-id="c16ab-2064">virtualNetwork가 클러스터의 다른 리소스 그룹에 있을 때 cmdlet이 실패하는 버그가 수정됨</span><span class="sxs-lookup"><span data-stu-id="c16ab-2064">Fix bug where cmdlet failed if virtualNetwork was in a different resource group that the cluster.</span></span> <span data-ttu-id="c16ab-2065">문제 해결: https://github.com/Azure/azure-powershell/issues/8407</span><span class="sxs-lookup"><span data-stu-id="c16ab-2065">fixes issue: https://github.com/Azure/azure-powershell/issues/8407</span></span>
    - <span data-ttu-id="c16ab-2066">Add-AzServiceFabricApplicationCertificate cmdlet이 사용되지 않음</span><span class="sxs-lookup"><span data-stu-id="c16ab-2066">Deprecating Add-AzServiceFabricApplicationCertificate cmdlet</span></span>

#### <a name="azsql"></a><span data-ttu-id="c16ab-2067">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="c16ab-2067">Az.Sql</span></span>
* <span data-ttu-id="c16ab-2068">이전의 Auditing(감사) cmdlet에 대한 설명서가 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="c16ab-2068">Update documentation of old Auditing cmdlets.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="c16ab-2069">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="c16ab-2069">Az.Storage</span></span>
* <span data-ttu-id="c16ab-2070">더 많은 시나리오를 cmdlet 예제에 추가하고 매개 변수 설명을 업데이트하여 Get/Close-AzStorageFileHandle에 대한 도움말이 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="c16ab-2070">Update help for Get/Close-AzStorageFileHandle, by add more scenarios to cmdlet examples and update parameter descriptions</span></span>
* <span data-ttu-id="c16ab-2071">Blob 업로드 및 Blob 복사에서 StandardBlobTier가 지원됨</span><span class="sxs-lookup"><span data-stu-id="c16ab-2071">Support StandardBlobTier in upload blob and copy blob</span></span>
    -  <span data-ttu-id="c16ab-2072">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="c16ab-2072">Set-AzStorageBlobContent</span></span>
    -  <span data-ttu-id="c16ab-2073">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="c16ab-2073">Start-AzStorageBlobCopy</span></span>
* <span data-ttu-id="c16ab-2074">Blob 복사에서 우선 순위 리하이드레이션이 지원됨</span><span class="sxs-lookup"><span data-stu-id="c16ab-2074">Support Rehydrate Priority in copy blob</span></span>
    -  <span data-ttu-id="c16ab-2075">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="c16ab-2075">Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="c16ab-2076">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="c16ab-2076">Az.Websites</span></span>
* <span data-ttu-id="c16ab-2077">Set-AzWebApp 및 Set-AzWebAppSlot에서 -AppSettings 매개 변수에 대한 설명이 추가됨</span><span class="sxs-lookup"><span data-stu-id="c16ab-2077">Add clarification around -AppSettings parameter in Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <a name="250---july-2019"></a><span data-ttu-id="c16ab-2078">2.5.0 - 2019년 7월</span><span class="sxs-lookup"><span data-stu-id="c16ab-2078">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="c16ab-2079">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="c16ab-2079">Az.Accounts</span></span>
* <span data-ttu-id="c16ab-2080">ClientRuntime의 최신 버전을 사용하도록 일반적인 코드를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2080">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="c16ab-2081">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="c16ab-2081">Az.ApplicationInsights</span></span>
* <span data-ttu-id="c16ab-2082">'Remove-AzApplicationInsightsApiKey' 설명서의 예제 오타 수정</span><span class="sxs-lookup"><span data-stu-id="c16ab-2082">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span>

#### <a name="azautomation"></a><span data-ttu-id="c16ab-2083">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="c16ab-2083">Az.Automation</span></span>
* <span data-ttu-id="c16ab-2084">리소스 문자열의 오타 수정</span><span class="sxs-lookup"><span data-stu-id="c16ab-2084">Fix typo in resource string</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="c16ab-2085">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="c16ab-2085">Az.CognitiveServices</span></span>
* <span data-ttu-id="c16ab-2086">NetworkRuleSet 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2086">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="c16ab-2087">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="c16ab-2087">Az.Compute</span></span>
* <span data-ttu-id="c16ab-2088">VM 인스턴스 보기 개체의 누락된 속성(ComputerName, OsName, OsVersion 및 HyperVGeneration)을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2088">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="c16ab-2089">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="c16ab-2089">Az.ContainerRegistry</span></span>
* <span data-ttu-id="c16ab-2090">복제 매개 변수의 Remove-AzContainerRegistryReplication에서 오타 수정</span><span class="sxs-lookup"><span data-stu-id="c16ab-2090">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="c16ab-2091">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/9633 을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2091">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="c16ab-2092">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="c16ab-2092">Az.DataFactory</span></span>
* <span data-ttu-id="c16ab-2093">ADF .Net SDK 버전을 4.1.0으로 업데이트</span><span class="sxs-lookup"><span data-stu-id="c16ab-2093">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="c16ab-2094">'Get-AzDataFactoryV2PipelineRun' 설명서의 오타 수정</span><span class="sxs-lookup"><span data-stu-id="c16ab-2094">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="c16ab-2095">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="c16ab-2095">Az.EventHub</span></span>
* <span data-ttu-id="c16ab-2096">SAS 토큰을 생성하기 위해 추가된 새로운 cmmdlet 추가: New-AzEventHubAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="c16ab-2096">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="c16ab-2097">'관리'만 지정된 경우 authorizationrules 권한에 대한 확인 및 오류 메시지 추가</span><span class="sxs-lookup"><span data-stu-id="c16ab-2097">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="c16ab-2098">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="c16ab-2098">Az.KeyVault</span></span>
* <span data-ttu-id="c16ab-2099">인증서 정책에 대한 KeySize 지정을 위한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="c16ab-2099">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="c16ab-2100">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="c16ab-2100">Az.LogicApp</span></span>
* <span data-ttu-id="c16ab-2101">모든 맵 유형을 나열하도록 Get-AzIntegrationAccountMap 수정</span><span class="sxs-lookup"><span data-stu-id="c16ab-2101">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="c16ab-2102">필터링을 위해 새 MapType 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="c16ab-2102">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="c16ab-2103">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="c16ab-2103">Az.ManagedServices</span></span>
* <span data-ttu-id="c16ab-2104">API 버전 2019-06-01(GA)에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="c16ab-2104">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="c16ab-2105">Az.Network</span><span class="sxs-lookup"><span data-stu-id="c16ab-2105">Az.Network</span></span>
* <span data-ttu-id="c16ab-2106">프라이빗 엔드포인트 및 프라이빗 링크 서비스에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="c16ab-2106">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="c16ab-2107">새로운 cmdlet</span><span class="sxs-lookup"><span data-stu-id="c16ab-2107">New cmdlets</span></span>
        - <span data-ttu-id="c16ab-2108">Set-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="c16ab-2108">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="c16ab-2109">Set-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="c16ab-2109">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="c16ab-2110">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="c16ab-2110">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="c16ab-2111">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="c16ab-2111">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="c16ab-2112">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="c16ab-2112">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="c16ab-2113">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="c16ab-2113">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="c16ab-2114">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="c16ab-2114">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="c16ab-2115">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="c16ab-2115">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="c16ab-2116">기능에 대한 새로운 명령이 업데이트됨: Virtualnetwork의 서브넷에 있는 PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies 플래그</span><span class="sxs-lookup"><span data-stu-id="c16ab-2116">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="c16ab-2117">업데이트된 New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="c16ab-2117">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="c16ab-2118">이 서브넷의 프라이빗 엔드포인트에 네트워크 정책을 적용할지 여부를 나타내는 선택적 매개 변수 -PrivateEndpointNetworkPoliciesFlag가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2118">Added optional parameter -PrivateEndpointNetworkPoliciesFlag that configures whether to apply network policies on private endpoint in this subnet.</span></span>
        - <span data-ttu-id="c16ab-2119">이 서브넷의 프라이빗 연결 서비스에 네트워크 정책을 적용할지 여부를 나타내는 선택적 매개 변수 -PrivateLinkServiceNetworkPoliciesFlag가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2119">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag that configures whether to apply network policies network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="c16ab-2120">AzPrivateLinkService의 cmdlet 매개 변수 'ServiceName'이 이전 버전과의 호환성을 위해 별칭 'ServiceName'을 사용한 'Name'으로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2120">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="c16ab-2121">네트워크 보안 규칙 구성에 ICMP 프로토콜 사용</span><span class="sxs-lookup"><span data-stu-id="c16ab-2121">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="c16ab-2122">다음 Cmdlet이 업데이트 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2122">Updated cmdlets</span></span>
        - <span data-ttu-id="c16ab-2123">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c16ab-2123">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="c16ab-2124">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c16ab-2124">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="c16ab-2125">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c16ab-2125">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="c16ab-2126">New-AzVirtualNetworkGatewayConnection에 대한 구성 가능한 매개 변수로 ConnectionProtocolType (Ikev1/Ikev2) 추가</span><span class="sxs-lookup"><span data-stu-id="c16ab-2126">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="c16ab-2127">LoadBalancerFrontendIpConfiguration에 PrivateIpAddressVersion 추가</span><span class="sxs-lookup"><span data-stu-id="c16ab-2127">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="c16ab-2128">업데이트된 cmdlet:</span><span class="sxs-lookup"><span data-stu-id="c16ab-2128">Updated cmdlet:</span></span>
        - <span data-ttu-id="c16ab-2129">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="c16ab-2129">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="c16ab-2130">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="c16ab-2130">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="c16ab-2131">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="c16ab-2131">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="c16ab-2132">프로브에서 사용자 지정 포트를 지원하기 위한 Application Gateway New-AzApplicationGatewayProbeConfig 명령 업데이트</span><span class="sxs-lookup"><span data-stu-id="c16ab-2132">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="c16ab-2133">업데이트된 New-AzApplicationGatewayProbeConfig: 백 엔드 서버 검색에 사용되는 선택적 매개 변수 포트가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2133">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="c16ab-2134">이 매개 변수는 Standard_V2 및 WAF_V2 SKU에 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2134">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="c16ab-2135">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="c16ab-2135">Az.OperationalInsights</span></span>
* <span data-ttu-id="c16ab-2136">저장된 검색의 기본 버전이 1로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2136">Updated default version for saved searches to be 1.</span></span>
* <span data-ttu-id="c16ab-2137">사용자 지정 로그 null regex 처리가 수정됨</span><span class="sxs-lookup"><span data-stu-id="c16ab-2137">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="c16ab-2138">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="c16ab-2138">Az.RecoveryServices</span></span>
* <span data-ttu-id="c16ab-2139">'Get-AzRecoveryServicesBackupJob.md' 업데이트</span><span class="sxs-lookup"><span data-stu-id="c16ab-2139">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="c16ab-2140">'Get-AzRecoveryServicesBackupContainer.md' 업데이트</span><span class="sxs-lookup"><span data-stu-id="c16ab-2140">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="c16ab-2141">'Get-AzRecoveryServicesVault.md' 업데이트</span><span class="sxs-lookup"><span data-stu-id="c16ab-2141">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="c16ab-2142">'Wait-AzRecoveryServicesBackupJob.md' 업데이트</span><span class="sxs-lookup"><span data-stu-id="c16ab-2142">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="c16ab-2143">'Set-AzRecoveryServicesVaultContext.md' 업데이트</span><span class="sxs-lookup"><span data-stu-id="c16ab-2143">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="c16ab-2144">'Get-AzRecoveryServicesBackupItem.md' 업데이트</span><span class="sxs-lookup"><span data-stu-id="c16ab-2144">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="c16ab-2145">'Get-AzRecoveryServicesBackupRecoveryPoint.md' 업데이트</span><span class="sxs-lookup"><span data-stu-id="c16ab-2145">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="c16ab-2146">'Restore-AzRecoveryServicesBackupItem.md' 업데이트</span><span class="sxs-lookup"><span data-stu-id="c16ab-2146">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="c16ab-2147">Azure 파일 공유용 컨테이너를 등록 취소하기 위해 서비스 요청 업데이트</span><span class="sxs-lookup"><span data-stu-id="c16ab-2147">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="c16ab-2148">'Set-AzRecoveryServicesAsrAlertSetting.md' 업데이트</span><span class="sxs-lookup"><span data-stu-id="c16ab-2148">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="c16ab-2149">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="c16ab-2149">Az.Resources</span></span>
- <span data-ttu-id="c16ab-2150">'New-AzResourceGroupDeployment' 설명서에서 참조된 누락 cmdlet 제거</span><span class="sxs-lookup"><span data-stu-id="c16ab-2150">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="c16ab-2151">새 API 버전 2019-01-01을 사용하도록 정책 cmdlet 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="c16ab-2151">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="c16ab-2152">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="c16ab-2152">Az.ServiceBus</span></span>
* <span data-ttu-id="c16ab-2153">SAS 토큰을 생성하기 위해 추가된 새로운 cmmdlet 추가: New-AzServiceBusAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="c16ab-2153">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="c16ab-2154">'관리'만 지정된 경우 authorizationrules 권한에 대한 확인 및 오류 메시지 추가</span><span class="sxs-lookup"><span data-stu-id="c16ab-2154">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="c16ab-2155">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="c16ab-2155">Az.Sql</span></span>
* <span data-ttu-id="c16ab-2156">Set-AzSqlDatabaseSecondary cmdlet에 대한 누락된 예제 수정</span><span class="sxs-lookup"><span data-stu-id="c16ab-2156">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="c16ab-2157">이메일 주소를 제공하지 않고 설정된 취약성 평가 반복 검색 수정</span><span class="sxs-lookup"><span data-stu-id="c16ab-2157">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="c16ab-2158">경고 메시지의 작은 오타를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2158">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="c16ab-2159">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="c16ab-2159">Az.Storage</span></span>
* <span data-ttu-id="c16ab-2160">'Get-AzStorageAccount'에 대한 참조 설명서의 예제를 업데이트하여 올바른 매개 변수 이름 사용</span><span class="sxs-lookup"><span data-stu-id="c16ab-2160">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="c16ab-2161">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="c16ab-2161">Az.StorageSync</span></span>
* <span data-ttu-id="c16ab-2162">Invoke-AzStorageSyncChangeDetection cmdlet을 추가하는 중입니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2162">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="c16ab-2163">TierFilesOlderThanDays를 기념하는 문제 9551 수정</span><span class="sxs-lookup"><span data-stu-id="c16ab-2163">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="c16ab-2164">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="c16ab-2164">Az.Websites</span></span>
* <span data-ttu-id="c16ab-2165">Get-AzWebApp 및 Set-AzWebApp에서 일부 SiteConfig 속성을 반환하지 않은 버그 수정</span><span class="sxs-lookup"><span data-stu-id="c16ab-2165">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="c16ab-2166">Get-AzDeletedWebApp 및 Restore-AzDeletedWebApp에 새 위치 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="c16ab-2166">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="c16ab-2167">AzWebApp-IncludeSourceWebAppSlots을 사용하여 웹앱 슬롯을 복제하는 버그를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2167">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="c16ab-2168">2.4.0 - 2019년 7월</span><span class="sxs-lookup"><span data-stu-id="c16ab-2168">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="c16ab-2169">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="c16ab-2169">Az.Accounts</span></span>
* <span data-ttu-id="c16ab-2170">프로필 cmdlet에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="c16ab-2170">Add support for profile cmdlets</span></span>
* <span data-ttu-id="c16ab-2171">생성된 cmdlet에서 환경 및 데이터 평면에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="c16ab-2171">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="c16ab-2172">Windows PowerShell의 데이터 평면 cmdlet에대해 일부 경우 잘못된 엔드포인트가 사용되는 버그 수정</span><span class="sxs-lookup"><span data-stu-id="c16ab-2172">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="c16ab-2173">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="c16ab-2173">Az.Advisor</span></span>
* <span data-ttu-id="c16ab-2174">Az.Advisor의 GA 릴리스</span><span class="sxs-lookup"><span data-stu-id="c16ab-2174">GA release of Az.Advisor</span></span>
* <span data-ttu-id="c16ab-2175">이 모듈은 이제 롤업 `Az` 모듈의 일부로 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2175">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="c16ab-2176">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="c16ab-2176">Az.ApiManagement</span></span>
* <span data-ttu-id="c16ab-2177">문제 https://github.com/Azure/azure-powershell/issues/8671 수정</span><span class="sxs-lookup"><span data-stu-id="c16ab-2177">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="c16ab-2178">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="c16ab-2178">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="c16ab-2179">사용자 및 제품별 구독을 쿼리하기 위한 지원이 추가됨</span><span class="sxs-lookup"><span data-stu-id="c16ab-2179">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="c16ab-2180">범위 '/', '/ api, '/ api/echo api'를 사용하여 쿼리하기 위한 지원이 추가됨</span><span class="sxs-lookup"><span data-stu-id="c16ab-2180">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="c16ab-2181">[https://github.com/Azure/azure-powershell/issues/9307](https://github.com/Azure/azure-powershell/issues/9307 ) 및 https://github.com/Azure/azure-powershell/issues/8432 문제 수정</span><span class="sxs-lookup"><span data-stu-id="c16ab-2181">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="c16ab-2182">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="c16ab-2182">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="c16ab-2183">Apis를 가져올 때 'ApiVersion' 및 'ApiVersionSetId'를 지정하기 위한 지원이 추가됨</span><span class="sxs-lookup"><span data-stu-id="c16ab-2183">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="c16ab-2184">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="c16ab-2184">Az.Automation</span></span>
* <span data-ttu-id="c16ab-2185">문자열 값을 처리하기 위해 Set-AzAutomationConnectionFieldValue cmdlet 버그를 수정했습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2185">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="c16ab-2186">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="c16ab-2186">Az.Compute</span></span>
* <span data-ttu-id="c16ab-2187">New-AzImageConfig에 HyperVGeneration 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="c16ab-2187">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="c16ab-2188">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="c16ab-2188">Az.DataFactory</span></span>
* <span data-ttu-id="c16ab-2189">get activity runs, get pipeline runs, get trigger runs ADF cmdlet의 출력을 업데이트하여 Select-Object pipe를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2189">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="c16ab-2190">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="c16ab-2190">Az.EventGrid</span></span>
* <span data-ttu-id="c16ab-2191">'New-AzEventGridSubcription' 설명서의 오타 수정</span><span class="sxs-lookup"><span data-stu-id="c16ab-2191">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="c16ab-2192">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="c16ab-2192">Az.IotHub</span></span>
* <span data-ttu-id="c16ab-2193">권한 부여 정책 키를 다시 생성하기 위한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="c16ab-2193">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="c16ab-2194">Az.Network</span><span class="sxs-lookup"><span data-stu-id="c16ab-2194">Az.Network</span></span>
* <span data-ttu-id="c16ab-2195">'RoutingPreference'를 공용 IP 태그에 추가함</span><span class="sxs-lookup"><span data-stu-id="c16ab-2195">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="c16ab-2196">'Get-AzNetworkServiceTag' 참조 설명서의 예제 개선</span><span class="sxs-lookup"><span data-stu-id="c16ab-2196">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="c16ab-2197">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="c16ab-2197">Az.PolicyInsights</span></span>
* <span data-ttu-id="c16ab-2198">Get-AzPolicyState의 null 참조 문제 해결</span><span class="sxs-lookup"><span data-stu-id="c16ab-2198">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="c16ab-2199">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/9446 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2199">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="c16ab-2200">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="c16ab-2200">Az.OperationalInsights</span></span>
* <span data-ttu-id="c16ab-2201">Get-AzOperationalInsightsDataSource에 반환된 CustomLog datasource 모델 수정됨</span><span class="sxs-lookup"><span data-stu-id="c16ab-2201">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="c16ab-2202">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="c16ab-2202">Az.RecoveryServices</span></span>
* <span data-ttu-id="c16ab-2203">IaaSVMs에 대한 get-policy 명령 수정</span><span class="sxs-lookup"><span data-stu-id="c16ab-2203">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="c16ab-2204">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="c16ab-2204">Az.Resources</span></span>
    - <span data-ttu-id="c16ab-2205">Get-AzPolicyState -Top 매개 변수에 대한 도움말 텍스트 수정</span><span class="sxs-lookup"><span data-stu-id="c16ab-2205">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="c16ab-2206">Get-AzPolicyAlias에 대한 클라이언트 쪽 페이징 지원 추가</span><span class="sxs-lookup"><span data-stu-id="c16ab-2206">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="c16ab-2207">Set-AzPolicyAssignment, -PolicyParameters 및 -PolicyParametersObject에 대한 새 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="c16ab-2207">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="c16ab-2208">Policy cmdlet에 대한 몇 가지 문서 및 예제 업데이트</span><span class="sxs-lookup"><span data-stu-id="c16ab-2208">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="c16ab-2209">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="c16ab-2209">Az.ServiceBus</span></span>
* <span data-ttu-id="c16ab-2210">문제 #4938 수정 - MaxSizeInMegabytes를 설정할 때 New-AzureRmServiceBusQueue가 BadRequest 반환</span><span class="sxs-lookup"><span data-stu-id="c16ab-2210">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="c16ab-2211">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="c16ab-2211">Az.Sql</span></span>
* <span data-ttu-id="c16ab-2212">미리 보기 릴리스에서 공개 릴리스로 인스턴스 장애 조치(Failover) 그룹 cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="c16ab-2212">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="c16ab-2213">새 cmdlet으로 Azure SQL Server\Database Auditing을 지원하세요.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2213">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="c16ab-2214">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="c16ab-2214">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="c16ab-2215">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="c16ab-2215">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="c16ab-2216">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="c16ab-2216">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="c16ab-2217">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="c16ab-2217">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="c16ab-2218">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="c16ab-2218">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="c16ab-2219">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="c16ab-2219">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="c16ab-2220">취약성 평가 설정에서 이메일 제약 조건 제거</span><span class="sxs-lookup"><span data-stu-id="c16ab-2220">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="c16ab-2221">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="c16ab-2221">Az.Storage</span></span>
* <span data-ttu-id="c16ab-2222">다음 cmdlet에서 2개의 매개 변수 '-IndexDocument' 및 '-ErrorDocument404Path'를 필수에서 선택으로 변경하세요.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2222">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="c16ab-2223">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="c16ab-2223">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="c16ab-2224">예제를 추가하여 Get-AzStorageBlobContent의 도움말 업데이트</span><span class="sxs-lookup"><span data-stu-id="c16ab-2224">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="c16ab-2225">StorageException으로 cmdlet이 실패한 경우 자세한 오류 정보 표시</span><span class="sxs-lookup"><span data-stu-id="c16ab-2225">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="c16ab-2226">Azure Files AAD DS 인증으로 스토리지 계정 생성 또는 업데이트 지원</span><span class="sxs-lookup"><span data-stu-id="c16ab-2226">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="c16ab-2227">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="c16ab-2227">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="c16ab-2228">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="c16ab-2228">Set-AzStorageAccount</span></span>
* <span data-ttu-id="c16ab-2229">파일 공유, 파일 디렉터리 또는 파일의 목록 지원 또는 파일 핸들 닫기</span><span class="sxs-lookup"><span data-stu-id="c16ab-2229">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="c16ab-2230">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="c16ab-2230">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="c16ab-2231">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="c16ab-2231">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="c16ab-2232">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="c16ab-2232">Az.StorageSync</span></span>
* <span data-ttu-id="c16ab-2233">이 모듈은 이제 롤업 `Az` 모듈의 일부로 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2233">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="c16ab-2234">2.3.2 - 2019년 6월</span><span class="sxs-lookup"><span data-stu-id="c16ab-2234">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="c16ab-2235">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="c16ab-2235">Az.Accounts</span></span>
* <span data-ttu-id="c16ab-2236">함수 호출에 대해 일부 경우 잘못된 URL이 사용되는 버그 수정</span><span class="sxs-lookup"><span data-stu-id="c16ab-2236">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="c16ab-2237">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/8983 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2237">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="c16ab-2238">AzureRM에서 Az cmdlet으로의 별칭 문제 해결</span><span class="sxs-lookup"><span data-stu-id="c16ab-2238">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="c16ab-2239">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="c16ab-2239">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="c16ab-2240">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="c16ab-2240">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="c16ab-2241">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="c16ab-2241">Az.Compute</span></span>
* <span data-ttu-id="c16ab-2242">New-AzVm 및 New-AzVmss 단순 매개 변수 집합은 이제 'ProximityPlacementGroup'매개 변수를 허용합니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2242">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="c16ab-2243">'New-AzVM' 참조 설명서에서 오타 수정</span><span class="sxs-lookup"><span data-stu-id="c16ab-2243">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="c16ab-2244">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="c16ab-2244">Az.Dns</span></span>
* <span data-ttu-id="c16ab-2245">'Set-AzDnsZone' 도움말 예제의 오타가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2245">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="c16ab-2246">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="c16ab-2246">Az.EventGrid</span></span>
* <span data-ttu-id="c16ab-2247">2019-06-01 API 버전을 사용하도록 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2247">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="c16ab-2248">새 cmdlet:</span><span class="sxs-lookup"><span data-stu-id="c16ab-2248">New cmdlets:</span></span>
    - <span data-ttu-id="c16ab-2249">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="c16ab-2249">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="c16ab-2250">새 Azure Event Grid 도메인을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2250">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="c16ab-2251">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="c16ab-2251">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="c16ab-2252">Event Grid 도메인의 세부 정보를 가져오거나 현재 Azure 구독의 모든 Event Grid 도메인 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2252">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="c16ab-2253">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="c16ab-2253">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="c16ab-2254">Azure Event Grid 도메인을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2254">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="c16ab-2255">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="c16ab-2255">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="c16ab-2256">Azure Event Grid 도메인에 대한 공유 액세스 키를 다시 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2256">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="c16ab-2257">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="c16ab-2257">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="c16ab-2258">Event Grid 도메인 이벤트를 게시하는 데 사용되는 공유 액세스 키를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2258">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="c16ab-2259">New-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="c16ab-2259">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="c16ab-2260">새 Azure Event Grid 도메인 토픽을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2260">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="c16ab-2261">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="c16ab-2261">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="c16ab-2262">Event Grid 도메인 토픽의 세부 사항을 가져오거나, 현재 Azure의 특정 Event Grid 도메인 아래의 모든 Event Grid 도메인 토픽 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2262">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span>
    - <span data-ttu-id="c16ab-2263">Remove-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="c16ab-2263">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="c16ab-2264">기존 Azure Event Grid 도메인 토픽을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2264">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="c16ab-2265">다음 Cmdlet이 업데이트 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2265">Updated cmdlets:</span></span>
    - <span data-ttu-id="c16ab-2266">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="c16ab-2266">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="c16ab-2267">새로운 Event Grid 도메인 및 Event Grid 도메인 토픽에 대한 파이핑을 지원하기 위해 새로운 필수 매개 변수를 추가하여 이러한 리소스 아래에 새 이벤트 구독을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2267">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="c16ab-2268">새로운 Event Grid 도메인 이름 및 Event Grid 도메인 토픽 이름을 지정하기 위해 새로운 필수 매개 변수를 추가하여 이러한 리소스 아래에 새 이벤트 구독을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2268">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="c16ab-2269">기존 매개 변수(예: EndPointType, SubjectBeginsWith 등)를 재사용할 수 있도록 도메인 및 도메인 토픽에 대한 새로운 매개 변수 집합을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2269">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="c16ab-2270">지정을 위한 새로운 선택적 매개 변수를 추가</span><span class="sxs-lookup"><span data-stu-id="c16ab-2270">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="c16ab-2271">이벤트 구독 만료 날짜,</span><span class="sxs-lookup"><span data-stu-id="c16ab-2271">Event subscription expiration date,</span></span>
            - <span data-ttu-id="c16ab-2272">고급 필터링 매개 변수.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2272">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="c16ab-2273">대상으로 servicebusqueue에 대한 새 열거형을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2273">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="c16ab-2274">-IncludedEventType 옵션에서 'All' 사용을 허용하지 않고 다음으로 대체함</span><span class="sxs-lookup"><span data-stu-id="c16ab-2274">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span>
    - <span data-ttu-id="c16ab-2275">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="c16ab-2275">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="c16ab-2276">결과 페이지 매김 및 필터링을 지원하는 새로운 선택적 매개 변수(Top, ODataQuery 및 NextLink)를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2276">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="c16ab-2277">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="c16ab-2277">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="c16ab-2278">Event Grid 도메인 및 Event Grid 도메인 토픽에 대한 파이핑을 지원하기 위해 새로운 필수 매개 변수를 추가하여 이러한 리소스 아래에 기존 이벤트 구독을 제거할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2278">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="c16ab-2279">Event Grid 도메인 이름 및 Event Grid 도메인 토픽 이름을 지정하기 위해 새로운 필수 매개 변수를 추가하여 이러한 리소스 아래에 기존 이벤트 구독을 제거할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2279">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="c16ab-2280">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="c16ab-2280">Az.FrontDoor</span></span>
* <span data-ttu-id="c16ab-2281">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="c16ab-2281">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="c16ab-2282">변환 지원 및 새 연산자 자동 완성 값(RegEx)을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2282">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="c16ab-2283">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="c16ab-2283">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="c16ab-2284">새 자동 완성 값 추가</span><span class="sxs-lookup"><span data-stu-id="c16ab-2284">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="c16ab-2285">Az.Network</span><span class="sxs-lookup"><span data-stu-id="c16ab-2285">Az.Network</span></span>
* <span data-ttu-id="c16ab-2286">Microsoft Azure Virtual Network 게이트웨이 리소스에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="c16ab-2286">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="c16ab-2287">새로운 cmdlet</span><span class="sxs-lookup"><span data-stu-id="c16ab-2287">New cmdlets</span></span>
        - <span data-ttu-id="c16ab-2288">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="c16ab-2288">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="c16ab-2289">AvailablePrivateEndpointType 추가</span><span class="sxs-lookup"><span data-stu-id="c16ab-2289">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="c16ab-2290">새로운 cmdlet</span><span class="sxs-lookup"><span data-stu-id="c16ab-2290">New cmdlets</span></span>
        - <span data-ttu-id="c16ab-2291">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="c16ab-2291">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="c16ab-2292">PrivatePrivateLinkService 추가</span><span class="sxs-lookup"><span data-stu-id="c16ab-2292">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="c16ab-2293">새로운 cmdlet</span><span class="sxs-lookup"><span data-stu-id="c16ab-2293">New cmdlets</span></span>
        - <span data-ttu-id="c16ab-2294">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="c16ab-2294">Get-AzPrivateLinkService</span></span>
        - <span data-ttu-id="c16ab-2295">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="c16ab-2295">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="c16ab-2296">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="c16ab-2296">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="c16ab-2297">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="c16ab-2297">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="c16ab-2298">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="c16ab-2298">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="c16ab-2299">PrivateEndpoint 추가</span><span class="sxs-lookup"><span data-stu-id="c16ab-2299">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="c16ab-2300">새로운 cmdlet</span><span class="sxs-lookup"><span data-stu-id="c16ab-2300">New cmdlets</span></span>
        - <span data-ttu-id="c16ab-2301">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="c16ab-2301">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="c16ab-2302">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="c16ab-2302">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="c16ab-2303">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="c16ab-2303">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="c16ab-2304">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="c16ab-2304">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="c16ab-2305">기능에 대한 새로운 명령이 업데이트됨: VpnConnection 상의 UseLocalAzureIpAddress 플래그</span><span class="sxs-lookup"><span data-stu-id="c16ab-2305">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="c16ab-2306">New-AzVpnConnection이 업데이트됨: 선택적 매개 변수 -UseLocalAzureIpAddress를 추가하여 로컬 Azure IP 주소가 연결을 시작하는 동안 소스 주소로 사용되어야 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2306">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="c16ab-2307">Set-AzVpnConnection이 업데이트됨: 선택적 매개 변수 -UseLocalAzureIpAddress를 추가하여 로컬 Azure IP 주소가 연결을 시작하는 동안 소스 주소로 사용되어야 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2307">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="c16ab-2308">ExpressRoute 피어링에 읽기 전용 필드 PeeredConnections가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2308">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="c16ab-2309">ExpressRoute에 읽기 전용 필드 GlobalReachEnabled가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2309">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="c16ab-2310">ExpressRouteCircuit 모델에서 AllowGlobalReach 필드의 사용 중단을 부르는 호환성이 손상되는 변경 속성이 추가됨</span><span class="sxs-lookup"><span data-stu-id="c16ab-2310">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="c16ab-2311">AzApplicationGatewayRedirectConfiguration cmdlet에서 TargetListenerID를 사용하는 중의 8756 오류 문제가 해결됨</span><span class="sxs-lookup"><span data-stu-id="c16ab-2311">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="c16ab-2312">다시 쓰기 규칙 세트가 설정되지 못하게 하는 New-AzApplicationGatewayPathRuleConfig의 버그를 수정했습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2312">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="c16ab-2313">NetworkInterfaceIpConfiguration에 VirtualNetworkTaps가 표시되는 방식이 수정됨</span><span class="sxs-lookup"><span data-stu-id="c16ab-2313">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="c16ab-2314">모든 파트를 나열하도록 Cortex Get cmdlet이 수정됨</span><span class="sxs-lookup"><span data-stu-id="c16ab-2314">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="c16ab-2315">ExpressRouteGateways, VpnGateway에 대한 VirtualHub 참조 생성 수정됨</span><span class="sxs-lookup"><span data-stu-id="c16ab-2315">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="c16ab-2316">AzureFirewall 및 NatGateway의 가용성 영역에 대한 지원 추가됨</span><span class="sxs-lookup"><span data-stu-id="c16ab-2316">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="c16ab-2317">Get-AzNetworkServiceTag cmdlet 추가됨</span><span class="sxs-lookup"><span data-stu-id="c16ab-2317">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="c16ab-2318">Azure Firewall에 대한 여러 공용 IP 주소에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="c16ab-2318">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="c16ab-2319">New-AzFirewall cmdlet이 업데이트됨:</span><span class="sxs-lookup"><span data-stu-id="c16ab-2319">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="c16ab-2320">하나 이상의 공용 IP 주소 개체를 허용하는 매개 변수 -PublicIpAddress 추가됨</span><span class="sxs-lookup"><span data-stu-id="c16ab-2320">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="c16ab-2321">Virtual Network 개체를 허용하는 매개 변수 -VirtualNetwork 추가됨</span><span class="sxs-lookup"><span data-stu-id="c16ab-2321">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="c16ab-2322">방화벽 개체에 AddPublicIpAddress 및 RemovePublicIpAddress 메서드 추가됨 - 공용 IP 주소 개체를 입력으로 허용</span><span class="sxs-lookup"><span data-stu-id="c16ab-2322">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="c16ab-2323">매개 변수 -PublicIpName 및 -VirtualNetworkName이 더 이상 사용되지 않음</span><span class="sxs-lookup"><span data-stu-id="c16ab-2323">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span>
* <span data-ttu-id="c16ab-2324">기능에 대한 새로운 명령이 업데이트됨: VpnClient AAD 인증 옵션을 가상 네트워크 게이트웨이 리소스로 설정했습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2324">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span>
    - <span data-ttu-id="c16ab-2325">New-AzVirtualNetworkGateway가 업데이트됨: 게이트웨이에서 VpnClient AAD 인증 옵션을 설정할 수 있도록 선택적 매개 변수 AadTenantUri, AadAudienceId, AadIssuerUri가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2325">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="c16ab-2326">Set-AzVirtualNetworkGateway가 업데이트됨: 게이트웨이에서 VpnClient AAD 인증 옵션을 설정할 수 있도록 선택적 매개 변수 AadTenantUri, AadAudienceId, AadIssuerUri가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2326">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="c16ab-2327">Set-AzVirtualNetworkGateway가 업데이트됨: 게이트웨이에서 VpnClient AAD 인증 옵션을 제거할 수 있도록 선택적인 스위치 매개 변수 RemoveAadAuthentication이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2327">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="c16ab-2328">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="c16ab-2328">Az.OperationalInsights</span></span>
* <span data-ttu-id="c16ab-2329">'New-AzureRmOperationalInsightsWorkspace' 명령에서 **pergb2018** 가격 책정 계층 사용</span><span class="sxs-lookup"><span data-stu-id="c16ab-2329">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="c16ab-2330">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="c16ab-2330">Az.Resources</span></span>
* <span data-ttu-id="c16ab-2331">추가 템플릿 내보내기 옵션 지원</span><span class="sxs-lookup"><span data-stu-id="c16ab-2331">Support for additional Template Export options</span></span>
    - <span data-ttu-id="c16ab-2332">Export-AzResourceGroup에 '-SkipResourceNameParameterization' 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="c16ab-2332">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="c16ab-2333">Export-AzResourceGroup에 '-SkipAllParameterization' 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="c16ab-2333">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="c16ab-2334">내보낸 리소스 필터링을 위해 Export-AzResourceGroup에 '-Resource' 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="c16ab-2334">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="c16ab-2335">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="c16ab-2335">Az.ServiceFabric</span></span>
* <span data-ttu-id="c16ab-2336">일부 경우 잘못된 지문을 가져오는 추가 인증서 ByExistingKeyVault 수정</span><span class="sxs-lookup"><span data-stu-id="c16ab-2336">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="c16ab-2337">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="c16ab-2337">Az.Sql</span></span>
* <span data-ttu-id="c16ab-2338">Advanced Threat Protection 스토리지 엔드포인트 접미사 수정</span><span class="sxs-lookup"><span data-stu-id="c16ab-2338">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="c16ab-2339">Advanced Data Security가 Advanced Threat Protection 정책을 재정의하는 것을 수정</span><span class="sxs-lookup"><span data-stu-id="c16ab-2339">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="c16ab-2340">고객이 TDE 키를 추가하고 관리되는 인스턴스에 TDE 보호기를 설정할 수 있도록 Management.Sql용 새 Cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="c16ab-2340">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="c16ab-2341">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="c16ab-2341">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="c16ab-2342">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="c16ab-2342">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="c16ab-2343">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="c16ab-2343">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="c16ab-2344">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="c16ab-2344">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="c16ab-2345">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="c16ab-2345">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="c16ab-2346">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="c16ab-2346">Az.Storage</span></span>
* <span data-ttu-id="c16ab-2347">스토리지 계정 생성 시 종류 FileStorage 및 SkuName Premium_ZRS 지원</span><span class="sxs-lookup"><span data-stu-id="c16ab-2347">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="c16ab-2348">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="c16ab-2348">New-AzStorageAccount</span></span>
* <span data-ttu-id="c16ab-2349">BLOB immutability cmdlet의 설명 명확화</span><span class="sxs-lookup"><span data-stu-id="c16ab-2349">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="c16ab-2350">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="c16ab-2350">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="c16ab-2351">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="c16ab-2351">Az.Websites</span></span>
* <span data-ttu-id="c16ab-2352">Get-AzWebAppCertificate를 클라이언트 대신 서버의 리소스 그룹별로 필터링하도록 최적화</span><span class="sxs-lookup"><span data-stu-id="c16ab-2352">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="c16ab-2353">Get-AzWebAppSnapshot에 -UseDisasterRecovery 스위치 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="c16ab-2353">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="c16ab-2354">2.2.0 - 2019년 6월</span><span class="sxs-lookup"><span data-stu-id="c16ab-2354">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="c16ab-2355">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="c16ab-2355">Az.Cdn</span></span>
* <span data-ttu-id="c16ab-2356">cmdlet에서 2019-04-15 API 버전 기반의 rulesEngine 기능을 지원하도록 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2356">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="c16ab-2357">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="c16ab-2357">Az.Compute</span></span>
* <span data-ttu-id="c16ab-2358">작업을 시작하여 완료되기 전에 즉시 반환하는 `NoWait` 매개 변수가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2358">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="c16ab-2359">다음 Cmdlet이 업데이트 되었습니다.   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="c16ab-2359">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="c16ab-2360">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="c16ab-2360">Az.EventHub</span></span>
* <span data-ttu-id="c16ab-2361">#9231 수정 - Get-AzEventHubNamespace에서 태그를 반환하지 않음</span><span class="sxs-lookup"><span data-stu-id="c16ab-2361">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="c16ab-2362">#9230 수정 - Get-AzEventHubNamespace에서 ResourceGroupName 대신 ResourceGroup을 반환함</span><span class="sxs-lookup"><span data-stu-id="c16ab-2362">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="c16ab-2363">Az.Network</span><span class="sxs-lookup"><span data-stu-id="c16ab-2363">Az.Network</span></span>
* <span data-ttu-id="c16ab-2364">Nat Gateway에 대한 ResourceId 및 InputObject 업데이트</span><span class="sxs-lookup"><span data-stu-id="c16ab-2364">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="c16ab-2365">ResourceId 및 InputObject에 대한 별칭 추가</span><span class="sxs-lookup"><span data-stu-id="c16ab-2365">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="c16ab-2366">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="c16ab-2366">Az.PolicyInsights</span></span>
* <span data-ttu-id="c16ab-2367">Get-AzPolicyEvent에서 Null 참조 문제 해결</span><span class="sxs-lookup"><span data-stu-id="c16ab-2367">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="c16ab-2368">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="c16ab-2368">Az.RecoveryServices</span></span>
* <span data-ttu-id="c16ab-2369">IaaSVM 정책 최소 보존 기간(일)이 1에서 7로 변경됨</span><span class="sxs-lookup"><span data-stu-id="c16ab-2369">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="c16ab-2370">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="c16ab-2370">Az.ServiceBus</span></span>
* <span data-ttu-id="c16ab-2371">#9182 문제 해결 - Get-AzServiceBusNamespace에서 ResourceGroupName 대신 ResourceGroup을 반환</span><span class="sxs-lookup"><span data-stu-id="c16ab-2371">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="c16ab-2372">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="c16ab-2372">Az.ServiceFabric</span></span>
* <span data-ttu-id="c16ab-2373">'Update-AzServiceFabricReliability' 오류 메시지의 오타 수정</span><span class="sxs-lookup"><span data-stu-id="c16ab-2373">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="c16ab-2374">Service Fabric 명령줄에서 누락된 문자 수정</span><span class="sxs-lookup"><span data-stu-id="c16ab-2374">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="c16ab-2375">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="c16ab-2375">Az.Sql</span></span>
* <span data-ttu-id="c16ab-2376">Managed Instance에 대한 AutoDr을 지원하기 위해 New-AzureSqlInstance cmdlet에 대한 DnsZonePartner 매개 변수를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2376">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="c16ab-2377">Get-AzSqlDatabaseSecureConnectionPolicy cmdlet 사용 중단</span><span class="sxs-lookup"><span data-stu-id="c16ab-2377">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="c16ab-2378">Threat Detection(위협 탐지) cmdlet 이름을 Advanced Threat Protection으로 변경함</span><span class="sxs-lookup"><span data-stu-id="c16ab-2378">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="c16ab-2379">새 AzSqlInstance -StorageSizeInGB 및 -LicenseType 매개 변수는 이제 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2379">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="c16ab-2380">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="c16ab-2380">Az.Websites</span></span>
* <span data-ttu-id="c16ab-2381">-WebApp 속성에서 Set-AzWebApp 및 Set-AzWebAppSlot을 사용하면 태그가 제거되는 문제를 해결함</span><span class="sxs-lookup"><span data-stu-id="c16ab-2381">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="c16ab-2382">2.1.0 - 2019년 5월</span><span class="sxs-lookup"><span data-stu-id="c16ab-2382">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="c16ab-2383">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="c16ab-2383">Az.ApiManagement</span></span>
* <span data-ttu-id="c16ab-2384">글로벌 및 API 범위에서 진단을 관리하기 위한 새 cmdlet을 만들었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2384">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="c16ab-2385">**Get-AzApiManagementDiagnostic** - 글로벌 또는 API 범위가 구성된 진단 가져오기</span><span class="sxs-lookup"><span data-stu-id="c16ab-2385">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="c16ab-2386">**New-AzApiManagementDiagnostic** - 글로벌 범위 또는 API 범위에서 새 진단 만들기</span><span class="sxs-lookup"><span data-stu-id="c16ab-2386">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="c16ab-2387">**New-AzApiManagementHttpMessageDiagnostic** - 기록할 Headers(헤더) 및 Body Bytes(본문 바이트 수) 크기에 대한 진단 설정 만들기</span><span class="sxs-lookup"><span data-stu-id="c16ab-2387">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="c16ab-2388">**New-AzApiManagementPipelineDiagnosticSetting** - 게이트웨이로 들어오고 나가는 HTTP 메시지에 대한 진단 설정 만들기</span><span class="sxs-lookup"><span data-stu-id="c16ab-2388">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="c16ab-2389">**New-AzApiManagementSamplingSetting** - 진단 요청/응답에 대한 샘플링 설정 만들기</span><span class="sxs-lookup"><span data-stu-id="c16ab-2389">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="c16ab-2390">**Remove-AzApiManagementDiagnostic** - 글로벌 또는 API 범위에서 진단 엔터티 제거</span><span class="sxs-lookup"><span data-stu-id="c16ab-2390">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="c16ab-2391">**Set-AzApiManagementDiagnostic** - 글로벌 또는 API 범위에서 진단 엔터티 업데이트</span><span class="sxs-lookup"><span data-stu-id="c16ab-2391">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="c16ab-2392">ApiManagement 서비스에서 캐시를 관리하기 위한 새 cmdlet을 만들었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2392">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="c16ab-2393">**Get-AzApiManagementCache** - 식별자 또는 모든 캐시로 지정된 캐시의 세부 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="c16ab-2393">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="c16ab-2394">**New-AzApiManagementCache** - 특정 Azure 'region'(지역)에 새 'default'(기본) 캐시 만들기</span><span class="sxs-lookup"><span data-stu-id="c16ab-2394">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="c16ab-2395">**Remove-AzApiManagementCache** - 캐시 제거</span><span class="sxs-lookup"><span data-stu-id="c16ab-2395">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="c16ab-2396">**Update-AzApiManagementCache** - 캐시 업데이트</span><span class="sxs-lookup"><span data-stu-id="c16ab-2396">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="c16ab-2397">API 스키마 관리하기 위한 새 cmdlet을 만들었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2397">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="c16ab-2398">**New-AzApiManagementSchema** - API에 대한 새 스키마 만들기</span><span class="sxs-lookup"><span data-stu-id="c16ab-2398">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="c16ab-2399">**Get-AzApiManagementSchema** - API에 구성된 스키마 가져오기</span><span class="sxs-lookup"><span data-stu-id="c16ab-2399">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="c16ab-2400">**Remove-AzApiManagementSchema** - API에 구성된 스키마 제거</span><span class="sxs-lookup"><span data-stu-id="c16ab-2400">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="c16ab-2401">**Set-AzApiManagementSchema** - API에 구성된 스키마 업데이트</span><span class="sxs-lookup"><span data-stu-id="c16ab-2401">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="c16ab-2402">사용자 토큰을 생성하기 위한 새 cmdlet을 만들었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2402">Created new Cmdlet for generating a User Token.</span></span>
    - <span data-ttu-id="c16ab-2403">**New-AzApiManagementUserToken** - 기본적으로 8시간 동안 유효한 새 사용자 토큰을 생성합니다. 'GIT' 사용자에 대한 토큰은 이 cmdlet을 사용하여 생성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2403">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="c16ab-2404">네트워크 상태를 검색하기 위한 새 cmdlet을 만들었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2404">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="c16ab-2405">**Get-AzApiManagementNetworkStatus** - API Management 서비스에서 사용하는 리소스의 네트워크 상태 연결을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2405">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="c16ab-2406">ApiManagement 서비스를 가상 네트워크에 배포하고 종속성이 손상되었는지 여부를 확인할 때 유용합니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2406">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="c16ab-2407">**New-AzApiManagement** cmdlet에서 ApiManagement 서비스를 관리하도록 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2407">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span>
    - <span data-ttu-id="c16ab-2408">새 '소비' SKU 지원이 추가됨</span><span class="sxs-lookup"><span data-stu-id="c16ab-2408">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="c16ab-2409">'소비' SKU에 대해 'EnableClientCertificate' 플래그를 설정하기 위한 지원이 추가됨</span><span class="sxs-lookup"><span data-stu-id="c16ab-2409">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="c16ab-2410">새 **New-AzApiManagementSslSetting** cmdlet을 사용하면 'Backend(백 엔드)' 및 'Frontend'(프런트 엔드)에서 'TLS/SSL' 설정을 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2410">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="c16ab-2411">또한 ApiManagement 서비스의 'Frontend'에서 '3DES'와 같은 'Ciphers'와 'Http2'와 같은 'ServerProtocols'를 구성하는 데 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2411">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="c16ab-2412">ApiManagement 서비스에서 'DeveloperPortal' 호스트 이름을 구성하기 위한 지원이 추가됨</span><span class="sxs-lookup"><span data-stu-id="c16ab-2412">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="c16ab-2413">**Get-AzApiManagementSsoToken** cmdlet에서 'PsApiManagement' 개체를 입력으로 사용하도록 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2413">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="c16ab-2414">cmdlet에서 오류 메시지를 인라인으로 표시하도록 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2414">Updated the cmdlet to display Error Messages inline</span></span>
     > <span data-ttu-id="c16ab-2415">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : 오류 코드: ValidationError 오류 메시지: 하나 이상의 필드에 잘못된 값이 있습니다. 오류 세부 정보:    [Code=ValidationError, Message=줄 3, 열 10의 'log-to-eventhub' 요소에 오류가 있습니다.: 로거를 찾지 못함, Target=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="c16ab-2415">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="c16ab-2416">**Export-AzApiManagementApi** cmdlet에서 API를 'OpenApi 3.0' 형식으로 내보내도록 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2416">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="c16ab-2417">**Import-AzApiManagementApi** cmdlet을 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2417">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="c16ab-2418">'OpenApi 3.0' 문서 사양에서 API 가져오기</span><span class="sxs-lookup"><span data-stu-id="c16ab-2418">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="c16ab-2419">문서('Swagger', 'Wadl', 'Wsdl', 'OpenApi')에 지정된 'PsApiManagementSchema' 속성 재정의</span><span class="sxs-lookup"><span data-stu-id="c16ab-2419">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="c16ab-2420">문서에 지정된 'ServiceUrl' 속성 재정의</span><span class="sxs-lookup"><span data-stu-id="c16ab-2420">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="c16ab-2421">**Get-AzApiManagementPolicy** cmdlet에서 'rawxml'을 사용하여 이스케이프된 비 Xml 'format'(형식)의 정책을 반환하도록 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2421">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="c16ab-2422">**Set-AzApiManagementPolicy** cmdlet에서 'rawxml'을 사용하여 이스케이프된 비 Xml 'format'의 정책을 수락하고, 'xml'을 사용하여 이스케이프된 Xml 'format'의 정책을 수락하도록 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2422">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="c16ab-2423">**New-AzApiManagementApi** cmdlet을 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2423">Updated cmdlet **New-AzApiManagementApi**</span></span>
    - <span data-ttu-id="c16ab-2424">'OpenId' 권한 부여 서버를 사용하여 API 구성</span><span class="sxs-lookup"><span data-stu-id="c16ab-2424">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="c16ab-2425">'ApiVersionSet'에서 API 만들기</span><span class="sxs-lookup"><span data-stu-id="c16ab-2425">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="c16ab-2426">'SourceApiId' 및 'SourceApiRevision'을 사용하여 API 복제</span><span class="sxs-lookup"><span data-stu-id="c16ab-2426">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="c16ab-2427">API 범위에서 'SubscriptionRequired' 구성 가능</span><span class="sxs-lookup"><span data-stu-id="c16ab-2427">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="c16ab-2428">**Set-AzApiManagementApi** cmdlet을 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2428">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="c16ab-2429">'OpenId' 권한 부여 서버를 사용하여 API 구성</span><span class="sxs-lookup"><span data-stu-id="c16ab-2429">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="c16ab-2430">API를 'ApiVersionSet'으로 업데이트</span><span class="sxs-lookup"><span data-stu-id="c16ab-2430">To updated an API into an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="c16ab-2431">API 범위에서 'SubscriptionRequired' 구성 가능</span><span class="sxs-lookup"><span data-stu-id="c16ab-2431">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="c16ab-2432">**New-AzApiManagementRevision** cmdlet을 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2432">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="c16ab-2433">'SourceApiRevision'을 사용하여 기존 수정 버전 복제(태그, 제품, 작업 및 정책 복사).</span><span class="sxs-lookup"><span data-stu-id="c16ab-2433">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="c16ab-2434">새 수정 버전은 부모의 'ApiId'를 가정합니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2434">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="c16ab-2435">'ApiRevisionDescription' 제공</span><span class="sxs-lookup"><span data-stu-id="c16ab-2435">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="c16ab-2436">API 복제 시 'ServiceUrl' 재정의</span><span class="sxs-lookup"><span data-stu-id="c16ab-2436">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="c16ab-2437">**New-AzApiManagementIdentityProvider** cmdlet을 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2437">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="c16ab-2438">'Authority'를 사용하여 'AAD' 또는 'AADB2C' 구성</span><span class="sxs-lookup"><span data-stu-id="c16ab-2438">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="c16ab-2439">'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' 및 'PasswordResetPolicy' 설정</span><span class="sxs-lookup"><span data-stu-id="c16ab-2439">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="c16ab-2440">**New-AzApiManagementSubscription** cmdlet을 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2440">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="c16ab-2441">'Scope' 및 'UserId'를 사용하여 새 SubscriptonModel 설명</span><span class="sxs-lookup"><span data-stu-id="c16ab-2441">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="c16ab-2442">'ProductId' 및 'UserId'를 사용하여 이전 구독 모델 설명</span><span class="sxs-lookup"><span data-stu-id="c16ab-2442">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="c16ab-2443">구독 수준에서 'AllowTracing'을 사용하도록 설정하는 지원 추가</span><span class="sxs-lookup"><span data-stu-id="c16ab-2443">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="c16ab-2444">**Set-AzApiManagementSubscription** cmdlet을 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2444">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="c16ab-2445">'Scope' 및 'UserId'를 사용하여 새 SubscriptonModel 설명</span><span class="sxs-lookup"><span data-stu-id="c16ab-2445">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="c16ab-2446">'ProductId' 및 'UserId'를 사용하여 이전 구독 모델 설명</span><span class="sxs-lookup"><span data-stu-id="c16ab-2446">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="c16ab-2447">구독 수준에서 'AllowTracing'을 사용하도록 설정하는 지원 추가</span><span class="sxs-lookup"><span data-stu-id="c16ab-2447">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="c16ab-2448">다음 cmdlet에서 'ResourceId'를 입력으로 수락하도록 업데이트했습니다</span><span class="sxs-lookup"><span data-stu-id="c16ab-2448">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="c16ab-2449">'New-AzApiManagementContext'</span><span class="sxs-lookup"><span data-stu-id="c16ab-2449">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="c16ab-2450">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="c16ab-2450">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="c16ab-2451">'Get-AzApiManagementApiRelease'</span><span class="sxs-lookup"><span data-stu-id="c16ab-2451">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="c16ab-2452">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="c16ab-2452">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="c16ab-2453">'Get-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="c16ab-2453">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="c16ab-2454">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="c16ab-2454">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="c16ab-2455">'Get-AzApiManagementAuthorizationServer'</span><span class="sxs-lookup"><span data-stu-id="c16ab-2455">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="c16ab-2456">'Get-AzApiManagementBackend'</span><span class="sxs-lookup"><span data-stu-id="c16ab-2456">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="c16ab-2457">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="c16ab-2457">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="c16ab-2458">'Get-AzApiManagementCertificate'</span><span class="sxs-lookup"><span data-stu-id="c16ab-2458">'Get-AzApiManagementCertificate'</span></span>
    - <span data-ttu-id="c16ab-2459">'Remove-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="c16ab-2459">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="c16ab-2460">'Remove-AzApiManagementSubscription'</span><span class="sxs-lookup"><span data-stu-id="c16ab-2460">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="c16ab-2461">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="c16ab-2461">Az.Automation</span></span>
* <span data-ttu-id="c16ab-2462">Get-AzAutomationJobOutputRecord에서 JSON 및 Text 레코드 값을 처리하도록 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2462">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="c16ab-2463">문제 https://github.com/Azure/azure-powershell/issues/7977 수정</span><span class="sxs-lookup"><span data-stu-id="c16ab-2463">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="c16ab-2464">문제 https://github.com/Azure/azure-powershell/issues/8600 수정</span><span class="sxs-lookup"><span data-stu-id="c16ab-2464">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="c16ab-2465">Start-AzAutomationDscCompilationJob에서 완료될 때까지 기다리지 않고 작업을 바로 시작하도록 변경했습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2465">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="c16ab-2466">문제 https://github.com/Azure/azure-powershell/issues/8347 수정</span><span class="sxs-lookup"><span data-stu-id="c16ab-2466">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="c16ab-2467">-Name을 사용하면 모든 노드를 반환하는 Get-AzAutomationDscNode 수정.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2467">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="c16ab-2468">이제 일치하는 노드만 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2468">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="c16ab-2469">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="c16ab-2469">Az.Compute</span></span>
* <span data-ttu-id="c16ab-2470">ProtectFromScaleIn 및 ProtectFromScaleSetAction 매개 변수를 Update-AzVmssVM cmdlet에 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2470">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="c16ab-2471">'East US'(미국 동부)가 지원되지 않는 경우 이제 New-AzVM wimple 매개 변수 집합에서 기본적으로 사용 가능한 위치를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2471">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="c16ab-2472">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="c16ab-2472">Az.DataLakeStore</span></span>
* <span data-ttu-id="c16ab-2473">ADLS SDK에서 httpclient를 사용하도록 업데이트하고, 데이터 평면 테스트를 Azure 프레임워크와 통합합니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2473">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="c16ab-2474">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="c16ab-2474">Az.Monitor</span></span>
* <span data-ttu-id="c16ab-2475">도움말 예제에서 잘못된 매개 변수 이름을 수정했습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2475">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="c16ab-2476">Az.Network</span><span class="sxs-lookup"><span data-stu-id="c16ab-2476">Az.Network</span></span>
* <span data-ttu-id="c16ab-2477">DisableBgpRoutePropagation 플래그를 유효 경로 테이블 출력에 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2477">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="c16ab-2478">업데이트된 cmdlet:</span><span class="sxs-lookup"><span data-stu-id="c16ab-2478">Updated cmdlet:</span></span>
        - <span data-ttu-id="c16ab-2479">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="c16ab-2479">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="c16ab-2480">New-AzApplicationGatewayTrustedRootCertificate 설명서에서 이중 파선을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2480">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="c16ab-2481">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="c16ab-2481">Az.Resources</span></span>
* <span data-ttu-id="c16ab-2482">할당 거부를 검색하기 위한 새 Get-AzureRmDenyAssignment cmdlet을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2482">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="c16ab-2483">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="c16ab-2483">Az.Sql</span></span>
* <span data-ttu-id="c16ab-2484">Advanced Threat Protection cmdlet의 이름을 Advanced Data Security로 변경하고, 취약성 평가를 기본적으로 사용하도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2484">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="c16ab-2485">2.0.0 - 2019년 5월</span><span class="sxs-lookup"><span data-stu-id="c16ab-2485">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="c16ab-2486">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="c16ab-2486">Az.Accounts</span></span>
* <span data-ttu-id="c16ab-2487">사용자 이름/비밀번호 인증을 사용하여 ADFS 문제를 해결하도록 인증 라이브러리 업데이트</span><span class="sxs-lookup"><span data-stu-id="c16ab-2487">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="c16ab-2488">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="c16ab-2488">Az.CognitiveServices</span></span>
* <span data-ttu-id="c16ab-2489">Bing Search 서비스에 대해서만 Bing 면책 조항을 표시하세요.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2489">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="c16ab-2490">계정 생성 실패 시 오류 개선.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2490">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="c16ab-2491">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="c16ab-2491">Az.Compute</span></span>
* <span data-ttu-id="c16ab-2492">근접 배치 그룹 기능</span><span class="sxs-lookup"><span data-stu-id="c16ab-2492">Proximity placement group feature.</span></span>
    - <span data-ttu-id="c16ab-2493">다음과 같은 새 cmdlet을 추가했습니다.   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="c16ab-2493">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="c16ab-2494">새 매개 변수 ProximityPlacementGroupId가 다음 cmdlet에 추가됩니다.   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="c16ab-2494">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="c16ab-2495">New-AzGalleryImageVersion에 StorageAccountType 매개 변수가 추가됩니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2495">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="c16ab-2496">New-AzGalleryImageVersion의 TargetRegion이 StorageAccountType를 포함할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2496">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="c16ab-2497">SkipShutdown 스위치 매개 변수가 Stop-AzVM 및 Stop-AzVmss에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2497">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>
* <span data-ttu-id="c16ab-2498">주요 변경 내용</span><span class="sxs-lookup"><span data-stu-id="c16ab-2498">Breaking changes</span></span>
    - <span data-ttu-id="c16ab-2499">Set-AzVMBootDiagnostics이 Set-AzVMBootDiagnostic으로 변경됩니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2499">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="c16ab-2500">Export-AzLogAnalyticThrottledRequests이 Export-AzLogAnalyticThrottledRequests로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2500">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="c16ab-2501">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="c16ab-2501">Az.DeploymentManager</span></span>
* <span data-ttu-id="c16ab-2502">Azure 배포 관리자 cmdlet의 일반적으로 사용 가능한 첫 번째 릴리스</span><span class="sxs-lookup"><span data-stu-id="c16ab-2502">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="c16ab-2503">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="c16ab-2503">Az.Dns</span></span>
* <span data-ttu-id="c16ab-2504">자동 DNS 이름 서버 위임</span><span class="sxs-lookup"><span data-stu-id="c16ab-2504">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="c16ab-2505">DNS 영역 만들기 cmdlet은 추가 선택적 매개 변수로 부모 영역 이름을 허용합니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2505">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="c16ab-2506">새로 생성 된 자식 영역의 부모 영역에 NS 레코드를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2506">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="c16ab-2507">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="c16ab-2507">Az.FrontDoor</span></span>
* <span data-ttu-id="c16ab-2508">Azure FrontDoor cmdlet의 일반적으로 사용 가능한 첫 번째 릴리스</span><span class="sxs-lookup"><span data-stu-id="c16ab-2508">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="c16ab-2509">'Waf'를 포함하도록 WAF cmdlet의 이름 바꾸기</span><span class="sxs-lookup"><span data-stu-id="c16ab-2509">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="c16ab-2510">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="c16ab-2510">Az.HDInsight</span></span>
* <span data-ttu-id="c16ab-2511">두 개의 cmdlet을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2511">Removed two cmdlets:</span></span>
    - <span data-ttu-id="c16ab-2512">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="c16ab-2512">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="c16ab-2513">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="c16ab-2513">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="c16ab-2514">Grant-AzHDInsightHttpServicesAccess를 대체할 새 cmdlet Set-AzHDInsightGatewayCredential을 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2514">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="c16ab-2515">reader 역할과 HDInsight 운영자 역할을 구분하도록 cmdlet Get-AzHDInsightJobOutput 업데이트:</span><span class="sxs-lookup"><span data-stu-id="c16ab-2515">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="c16ab-2516">reader 역할을 가진 사용자는 'DefaultStorageAccountKey'매개 변수를 명시적으로 지정해야 합니다. 그렇지 않으면 오류가 발생합니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2516">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="c16ab-2517">Hdinsight 운영자 역할을 가진 사용자를 영향을 받지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2517">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="c16ab-2518">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="c16ab-2518">Az.Monitor</span></span>
* <span data-ttu-id="c16ab-2519">SQR API(예약 쿼리 규칙)용 새 cmdlet</span><span class="sxs-lookup"><span data-stu-id="c16ab-2519">New cmdlets for SQR API (Scheduled Query Rule)</span></span>
    - <span data-ttu-id="c16ab-2520">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="c16ab-2520">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="c16ab-2521">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="c16ab-2521">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="c16ab-2522">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="c16ab-2522">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="c16ab-2523">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="c16ab-2523">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="c16ab-2524">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="c16ab-2524">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="c16ab-2525">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="c16ab-2525">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="c16ab-2526">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="c16ab-2526">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="c16ab-2527">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="c16ab-2527">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="c16ab-2528">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="c16ab-2528">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="c16ab-2529">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="c16ab-2529">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="c16ab-2530">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="c16ab-2530">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="c16ab-2531">SQR API에 대한 [자세한 내용](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules)</span><span class="sxs-lookup"><span data-stu-id="c16ab-2531">[More](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="c16ab-2532">GenV2(비 클래식) 메트릭 기반 경고 규칙에 대한 cmdlet을 포함하도록 Az.Monitor.md가 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="c16ab-2532">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="c16ab-2533">Az.Network</span><span class="sxs-lookup"><span data-stu-id="c16ab-2533">Az.Network</span></span>
* <span data-ttu-id="c16ab-2534">Nat 게이트웨이 리소스에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="c16ab-2534">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="c16ab-2535">새로운 cmdlet</span><span class="sxs-lookup"><span data-stu-id="c16ab-2535">New cmdlets</span></span>
        - <span data-ttu-id="c16ab-2536">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="c16ab-2536">New-AzNatGateway</span></span>
        - <span data-ttu-id="c16ab-2537">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="c16ab-2537">Get-AzNatGateway</span></span>
        - <span data-ttu-id="c16ab-2538">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="c16ab-2538">Set-AzNatGateway</span></span>
        - <span data-ttu-id="c16ab-2539">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="c16ab-2539">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="c16ab-2540">다음 Cmdlet이 업데이트 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2540">Updated cmdlets</span></span>
        - <span data-ttu-id="c16ab-2541">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="c16ab-2541">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="c16ab-2542">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="c16ab-2542">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="c16ab-2543">기능에 대한 새로운 명령이 업데이트됨: Brooklyn Gateway에서 사용자 지정 경로 설정/제거.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2543">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="c16ab-2544">New-AzVirtualNetworkGateway가 업데이트됨: 선택적 매개 변수 -CustomRoute를 추가하여 게이트웨이에서 설정할 사용자 지정 경로로 주소 접두사를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2544">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="c16ab-2545">Set-AzVirtualNetworkGateway가 업데이트됨: 선택적 매개 변수 -CustomRoute를 추가하여 게이트웨이에서 설정할 사용자 지정 경로로 주소 접두사를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2545">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="c16ab-2546">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="c16ab-2546">Az.PolicyInsights</span></span>
* <span data-ttu-id="c16ab-2547">정책 평가 세부 정보 쿼리 지원</span><span class="sxs-lookup"><span data-stu-id="c16ab-2547">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="c16ab-2548">Get-AzPolicyState에 '-Expand'매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="c16ab-2548">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="c16ab-2549">'-Expand PolicyEvaluationDetails' 지원</span><span class="sxs-lookup"><span data-stu-id="c16ab-2549">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="c16ab-2550">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="c16ab-2550">Az.RecoveryServices</span></span>
* <span data-ttu-id="c16ab-2551">크로스 구독 Azure에서 Azure 사이트 복구 지원</span><span class="sxs-lookup"><span data-stu-id="c16ab-2551">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="c16ab-2552">Azure Site Recovery에 대한 호환성이 손상되는 변경 표시</span><span class="sxs-lookup"><span data-stu-id="c16ab-2552">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="c16ab-2553">Azure Site Recovery 복구 계획 최종 실행 계획에 대한 수정</span><span class="sxs-lookup"><span data-stu-id="c16ab-2553">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="c16ab-2554">Azure에서 Azure에 대한 Azure Site Recovery 업데이트 네트워크 매핑 수정</span><span class="sxs-lookup"><span data-stu-id="c16ab-2554">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="c16ab-2555">관리 디스크에 대한 Azure에서 Azure에 대한 Azure Site Recovery 업데이트 보호 방향 수정</span><span class="sxs-lookup"><span data-stu-id="c16ab-2555">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="c16ab-2556">기타 사소한 수정.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2556">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="c16ab-2557">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="c16ab-2557">Az.Relay</span></span>
* <span data-ttu-id="c16ab-2558">고객 관련 메시지의 철자 오류 수정</span><span class="sxs-lookup"><span data-stu-id="c16ab-2558">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="c16ab-2559">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="c16ab-2559">Az.ServiceBus</span></span>
* <span data-ttu-id="c16ab-2560">네임스페이스의 NetworkRuleSet에 대한 새 cmdlet가 추가되었습니다</span><span class="sxs-lookup"><span data-stu-id="c16ab-2560">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="c16ab-2561">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="c16ab-2561">Az.Storage</span></span>
* <span data-ttu-id="c16ab-2562">저장소 클라이언트 라이브러리 10.0.1로 업그레이드(이 SDK의 모든 개체의 네임스페이스가 'Microsoft.WindowsAzure.Storage. *'에서 'Microsoft.Azure.Storage.* '로 변경됨)</span><span class="sxs-lookup"><span data-stu-id="c16ab-2562">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage. *' to 'Microsoft.Azure.Storage.* ')</span></span>
* <span data-ttu-id="c16ab-2563">새로운 API 버전 2019-04-01을 지원하기 위해 Microsoft.Azure.Management.Storage 11.0.0으로 업그레이드합니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2563">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="c16ab-2564">스토리지 생성 계정의 기본 스토리지 계정 종류가 'Storage'에서 'StorageV2'로 변경됩니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2564">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="c16ab-2565">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="c16ab-2565">New-AzStorageAccount</span></span>
* <span data-ttu-id="c16ab-2566">'StandardLRS'가 'Standard_LRS'로 변경되는 것과 같이 '-'을 추가하여 입력 SkuName과 정렬되도록 스토리지 계정 cmdlet 출력 Sku.Name을 변경합니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2566">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="c16ab-2567">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="c16ab-2567">New-AzStorageAccount</span></span>
    - <span data-ttu-id="c16ab-2568">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="c16ab-2568">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="c16ab-2569">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="c16ab-2569">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="c16ab-2570">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="c16ab-2570">Az.Websites</span></span>
* <span data-ttu-id="c16ab-2571">Get-AzWebApp에서 반환한 PSSite 개체에 대해 'Kind'속성이 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2571">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="c16ab-2572">Get-AzWebApp\* 메트릭 및 Get-AzAppServicePlanMetrics가 사용되지 않음으로 표시되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2572">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="c16ab-2573">1.8.0 - 2019년 4월</span><span class="sxs-lookup"><span data-stu-id="c16ab-2573">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="c16ab-2574">마지막 주 릴리스 이후의 주요 사항</span><span class="sxs-lookup"><span data-stu-id="c16ab-2574">Highlights since the last major release</span></span>
* <span data-ttu-id="c16ab-2575">`Az` 모듈 일반 공급</span><span class="sxs-lookup"><span data-stu-id="c16ab-2575">General availability of `Az` module</span></span>
* <span data-ttu-id="c16ab-2576">`Az` 모듈에 대한 자세한 내용은 https://aka.ms/azps-announce 를 방문하세요.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2576">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="c16ab-2577">Location, ResourceGroup 및 ResourceName 완성자가 추가되었습니다(https://azure.microsoft.com/blog/completers-in-azure-powershell/ ).</span><span class="sxs-lookup"><span data-stu-id="c16ab-2577">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="c16ab-2578">와일드카드 지원이 Az.Compute 및 Az.Network에 대한 Get cmdlet에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2578">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="c16ab-2579">Windows PowerShell 5.1 전용 대화형 사용자 이름/암호 인증이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2579">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="c16ab-2580">Python 2 Runbook 지원이 Az.Automation에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2580">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="c16ab-2581">Az.LogicApp: 통합 계정 어셈블리 및 일괄 처리 구성을 위한 새로운 cmdlet입니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2581">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="c16ab-2582">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="c16ab-2582">Az.Accounts</span></span>
* <span data-ttu-id="c16ab-2583">Mac에서 모듈을 올바르게 삭제하기 위해 Uninstall-AzureRm을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2583">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="c16ab-2584">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="c16ab-2584">Az.Batch</span></span>
* <span data-ttu-id="c16ab-2585">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2585">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="c16ab-2586">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="c16ab-2586">Az.Cdn</span></span>
* <span data-ttu-id="c16ab-2587">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2587">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="c16ab-2588">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="c16ab-2588">Az.CognitiveServices</span></span>
* <span data-ttu-id="c16ab-2589">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2589">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="c16ab-2590">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="c16ab-2590">Az.Compute</span></span>
* <span data-ttu-id="c16ab-2591">디스크의 리소스 ID에 리소스 ID의 소문자 resourcegroups가 있는 경우 AEM 설치 문제 수정</span><span class="sxs-lookup"><span data-stu-id="c16ab-2591">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="c16ab-2592">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2592">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="c16ab-2593">와일드 카드에 대한 설명서 수정</span><span class="sxs-lookup"><span data-stu-id="c16ab-2593">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="c16ab-2594">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="c16ab-2594">Az.DataFactory</span></span>
* <span data-ttu-id="c16ab-2595">NodeCount가 관리형 통합 런타임에 대해 Null이 아닌 경우 SsisProperties를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2595">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="c16ab-2596">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="c16ab-2596">Az.DataLakeStore</span></span>
* <span data-ttu-id="c16ab-2597">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2597">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="c16ab-2598">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="c16ab-2598">Az.EventGrid</span></span>
* <span data-ttu-id="c16ab-2599">이벤트 구독 cmdlet 만들기/업데이트를 사용하기 전에 리소스를 만들어야 함을 나타내기 위해 엔드포인트의 도움말 텍스트가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2599">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="c16ab-2600">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="c16ab-2600">Az.EventHub</span></span>
* <span data-ttu-id="c16ab-2601">네임스페이스의 NetworkRuleSet에 대한 새 cmdlet가 추가되었습니다</span><span class="sxs-lookup"><span data-stu-id="c16ab-2601">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="c16ab-2602">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="c16ab-2602">Az.HDInsight</span></span>
* <span data-ttu-id="c16ab-2603">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2603">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="c16ab-2604">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="c16ab-2604">Az.IotHub</span></span>
* <span data-ttu-id="c16ab-2605">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2605">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="c16ab-2606">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="c16ab-2606">Az.KeyVault</span></span>
* <span data-ttu-id="c16ab-2607">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2607">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="c16ab-2608">와일드 카드에 대한 설명서 수정</span><span class="sxs-lookup"><span data-stu-id="c16ab-2608">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="c16ab-2609">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="c16ab-2609">Az.MachineLearning</span></span>
* <span data-ttu-id="c16ab-2610">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2610">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="c16ab-2611">Az.Media</span><span class="sxs-lookup"><span data-stu-id="c16ab-2611">Az.Media</span></span>
* <span data-ttu-id="c16ab-2612">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2612">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="c16ab-2613">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="c16ab-2613">Az.Monitor</span></span>
  * <span data-ttu-id="c16ab-2614">GenV2(비 클래식) 메트릭 기반 경고 규칙에 대한 새 cmdlet</span><span class="sxs-lookup"><span data-stu-id="c16ab-2614">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="c16ab-2615">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="c16ab-2615">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="c16ab-2616">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="c16ab-2616">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="c16ab-2617">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="c16ab-2617">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="c16ab-2618">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="c16ab-2618">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="c16ab-2619">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="c16ab-2619">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="c16ab-2620">모니터 SDK가 버전 0.22.0-preview로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2620">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="c16ab-2621">Az.Network</span><span class="sxs-lookup"><span data-stu-id="c16ab-2621">Az.Network</span></span>
* <span data-ttu-id="c16ab-2622">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2622">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="c16ab-2623">와일드 카드에 대한 설명서 수정</span><span class="sxs-lookup"><span data-stu-id="c16ab-2623">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="c16ab-2624">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="c16ab-2624">Az.NotificationHubs</span></span>
* <span data-ttu-id="c16ab-2625">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2625">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="c16ab-2626">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="c16ab-2626">Az.OperationalInsights</span></span>
* <span data-ttu-id="c16ab-2627">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2627">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="c16ab-2628">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="c16ab-2628">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="c16ab-2629">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2629">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="c16ab-2630">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="c16ab-2630">Az.RecoveryServices</span></span>
* <span data-ttu-id="c16ab-2631">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2631">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="c16ab-2632">Azure VM의 SQL용 테이블 형식이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2632">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="c16ab-2633">AzureFileShare에서 위치를 가져오는 대체 메서드가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2633">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="c16ab-2634">시간대에 따라 SchedulePolicy 개체의 ScheduleRunDays가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2634">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="c16ab-2635">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="c16ab-2635">Az.RedisCache</span></span>
* <span data-ttu-id="c16ab-2636">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2636">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="c16ab-2637">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="c16ab-2637">Az.Resources</span></span>
* <span data-ttu-id="c16ab-2638">와일드 카드에 대한 설명서 수정</span><span class="sxs-lookup"><span data-stu-id="c16ab-2638">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="c16ab-2639">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="c16ab-2639">Az.Sql</span></span>
* <span data-ttu-id="c16ab-2640">Monitor SDK의 종속성을 공용 코드로 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2640">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="c16ab-2641">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2641">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="c16ab-2642">다중 열 분류 프로세스가 향상되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2642">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="c16ab-2643">기본적으로 Get-AzSqlServerServiceObjective의 응답으로 SKU 속성(SKU 이름, 제품군, 용량)과 테이블 형식을 포함합니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2643">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="c16ab-2644">해당 지역에 기존 서버 없이 위치별로 Get-AzSqlServerServiceObjective를 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2644">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="c16ab-2645">관리형 인스턴스 생성 시 표준 시간대 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2645">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="c16ab-2646">와일드 카드에 대한 설명서 수정</span><span class="sxs-lookup"><span data-stu-id="c16ab-2646">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="c16ab-2647">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="c16ab-2647">Az.Websites</span></span>
* <span data-ttu-id="c16ab-2648">실행 시 태그를 제거하지 않도록 Set-AzWebApp 및 Set-AzWebAppSlot를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2648">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="c16ab-2649">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2649">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="c16ab-2650">WebSites SDK가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2650">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="c16ab-2651">PSAppServicePlan에서 AdminSiteName 속성을 제거했습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2651">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="c16ab-2652">1.7.0 - 2019년 4월</span><span class="sxs-lookup"><span data-stu-id="c16ab-2652">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="c16ab-2653">마지막 주 릴리스 이후의 주요 사항</span><span class="sxs-lookup"><span data-stu-id="c16ab-2653">Highlights since the last major release</span></span>
* <span data-ttu-id="c16ab-2654">`Az` 모듈 일반 공급</span><span class="sxs-lookup"><span data-stu-id="c16ab-2654">General availability of `Az` module</span></span>
* <span data-ttu-id="c16ab-2655">`Az` 모듈에 대한 자세한 내용은 https://aka.ms/azps-announce 를 방문하세요.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2655">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="c16ab-2656">Location, ResourceGroup 및 ResourceName 완성자가 추가되었습니다(https://azure.microsoft.com/blog/completers-in-azure-powershell/ ).</span><span class="sxs-lookup"><span data-stu-id="c16ab-2656">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="c16ab-2657">와일드카드 지원이 Az.Compute 및 Az.Network에 대한 Get cmdlet에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2657">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="c16ab-2658">Windows PowerShell 5.1 전용 대화형 사용자 이름/암호 인증이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2658">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="c16ab-2659">Python 2 Runbook 지원이 Az.Automation에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2659">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="c16ab-2660">Az.LogicApp: 통합 계정 어셈블리 및 일괄 처리 구성을 위한 새로운 cmdlet입니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2660">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="c16ab-2661">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="c16ab-2661">Az.Accounts</span></span>
* <span data-ttu-id="c16ab-2662">매개 변수 AzureAnalysisServicesEndpointResourceId를 허용하도록 Add-AzEnvironment 및 Set-AzEnvironment 업데이트</span><span class="sxs-lookup"><span data-stu-id="c16ab-2662">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="c16ab-2663">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="c16ab-2663">Az.AnalysisServices</span></span>
* <span data-ttu-id="c16ab-2664">데이터 평면 cmdlet에서 ServiceClient 사용 및 원본 인증 논리 제거</span><span class="sxs-lookup"><span data-stu-id="c16ab-2664">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="c16ab-2665">호환성이 손상되는 변경을 방지하기 위해 Add-AzureASAccount를 Connect-AzAccount의 래퍼로 만듦</span><span class="sxs-lookup"><span data-stu-id="c16ab-2665">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="c16ab-2666">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="c16ab-2666">Az.Automation</span></span>
* <span data-ttu-id="c16ab-2667">포함에 대한 New-AzAutomationSoftwareUpdateConfiguration cmdlet 버그 수정</span><span class="sxs-lookup"><span data-stu-id="c16ab-2667">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="c16ab-2668">이제 매개 변수 IncludedKbNumber 및 IncludedPackageNameMask가 작동함</span><span class="sxs-lookup"><span data-stu-id="c16ab-2668">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="c16ab-2669">Azure 자동화 업데이트 관리 동적 그룹에 대한 버그 수정</span><span class="sxs-lookup"><span data-stu-id="c16ab-2669">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="c16ab-2670">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="c16ab-2670">Az.Compute</span></span>
* <span data-ttu-id="c16ab-2671">New-AzDiskConfig 및 New-AzSnapshotConfig에 HyperVGeneration 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="c16ab-2671">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="c16ab-2672">다른 테넌트의 갤러리 이미지를 사용하여 VM을 만들 수 있음</span><span class="sxs-lookup"><span data-stu-id="c16ab-2672">Allow VM creation with galley image from other tenants.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="c16ab-2673">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="c16ab-2673">Az.ContainerInstance</span></span>
* <span data-ttu-id="c16ab-2674">후행 빈 인수를 추가한 New-AzContainerGroup의 -Command 매개 변수의 문제 수정</span><span class="sxs-lookup"><span data-stu-id="c16ab-2674">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="c16ab-2675">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="c16ab-2675">Az.DataFactory</span></span>
* <span data-ttu-id="c16ab-2676">ADF .Net SDK 버전을 3.0.2로 업데이트</span><span class="sxs-lookup"><span data-stu-id="c16ab-2676">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="c16ab-2677">RepoConfiguration 관련 설정에 대한 추가 매개 변수로 Set-AzDataFactoryV2 cmdlet을 업데이트</span><span class="sxs-lookup"><span data-stu-id="c16ab-2677">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="c16ab-2678">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="c16ab-2678">Az.Resources</span></span>
* <span data-ttu-id="c16ab-2679">'-ResourceId' 또는 '-ResourceGroupName', '-Name' 및 '-ResourceType' 매개 변수를 제공할 때 'Get-AzResource'에 대한 공급자 처리 개선</span><span class="sxs-lookup"><span data-stu-id="c16ab-2679">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="c16ab-2680">'Test-AzDeployment' 및 'Test-AzResourceGroupDeployment'에 대한 오류 처리 개선</span><span class="sxs-lookup"><span data-stu-id="c16ab-2680">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="c16ab-2681">배포 유효성 검사 외부에서 발생한 오류를 처리하고 그 대신 명령의 출력에 포함</span><span class="sxs-lookup"><span data-stu-id="c16ab-2681">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="c16ab-2682">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/6856 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2682">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="c16ab-2683">배포 cmdlet 세트에 스크립트 및 작업 시나리오에서 프롬프트를 건너뛰는 '-IgnoreDynamicParameters' 스위치 추가</span><span class="sxs-lookup"><span data-stu-id="c16ab-2683">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="c16ab-2684">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/6856 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2684">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="c16ab-2685">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="c16ab-2685">Az.Sql</span></span>
* <span data-ttu-id="c16ab-2686">데이터베이스 데이터 분류 지원</span><span class="sxs-lookup"><span data-stu-id="c16ab-2686">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="c16ab-2687">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="c16ab-2687">Az.Storage</span></span>
* <span data-ttu-id="c16ab-2688">매개 변수 -UseConnectedAccount를 사용하여 스토리지 컨텍스트를 만들 때 자세한 오류 보고(단, 로그인 Azure 계정 없이)</span><span class="sxs-lookup"><span data-stu-id="c16ab-2688">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="c16ab-2689">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="c16ab-2689">New-AzStorageContext</span></span>
* <span data-ttu-id="c16ab-2690">관리 평면 API를 사용하여 지정한 스토리지 계정의 BLOB 서비스 속성 관리 지원</span><span class="sxs-lookup"><span data-stu-id="c16ab-2690">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="c16ab-2691">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="c16ab-2691">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="c16ab-2692">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="c16ab-2692">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="c16ab-2693">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="c16ab-2693">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="c16ab-2694">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="c16ab-2694">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="c16ab-2695">BLOB 및 파일 업로드/다운로드 cmdlet에 대한 -AsJob 지원</span><span class="sxs-lookup"><span data-stu-id="c16ab-2695">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="c16ab-2696">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="c16ab-2696">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="c16ab-2697">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="c16ab-2697">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="c16ab-2698">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="c16ab-2698">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="c16ab-2699">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="c16ab-2699">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="c16ab-2700">1.6.0 - 2019년 3월</span><span class="sxs-lookup"><span data-stu-id="c16ab-2700">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="c16ab-2701">마지막 주 릴리스 이후의 주요 사항</span><span class="sxs-lookup"><span data-stu-id="c16ab-2701">Highlights since the last major release</span></span>
* <span data-ttu-id="c16ab-2702">`Az` 모듈 일반 공급</span><span class="sxs-lookup"><span data-stu-id="c16ab-2702">General availability of `Az` module</span></span>
* <span data-ttu-id="c16ab-2703">`Az` 모듈에 대한 자세한 내용은 https://aka.ms/azps-announce 를 방문하세요.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2703">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="c16ab-2704">Location, ResourceGroup 및 ResourceName 완성자가 추가되었습니다(https://azure.microsoft.com/blog/completers-in-azure-powershell/ ).</span><span class="sxs-lookup"><span data-stu-id="c16ab-2704">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="c16ab-2705">와일드카드 지원이 Az.Compute 및 Az.Network에 대한 Get cmdlet에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2705">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="c16ab-2706">Windows PowerShell 5.1 전용 대화형 사용자 이름/암호 인증이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2706">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="c16ab-2707">Python 2 Runbook 지원이 Az.Automation에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2707">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="c16ab-2708">Az.LogicApp: 통합 계정 어셈블리 및 일괄 처리 구성을 위한 새로운 cmdlet입니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2708">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="c16ab-2709">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="c16ab-2709">Az.Automation</span></span>
* <span data-ttu-id="c16ab-2710">Azure 자동화 업데이트 관리에서 변경된 지원 기능은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2710">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="c16ab-2711">동적 그룹화</span><span class="sxs-lookup"><span data-stu-id="c16ab-2711">Dynamic grouping</span></span>
    * <span data-ttu-id="c16ab-2712">사전 스크립트</span><span class="sxs-lookup"><span data-stu-id="c16ab-2712">Pre-Post script</span></span>
    * <span data-ttu-id="c16ab-2713">다시 부팅 설정</span><span class="sxs-lookup"><span data-stu-id="c16ab-2713">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="c16ab-2714">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="c16ab-2714">Az.Compute</span></span>
* <span data-ttu-id="c16ab-2715">Get-AzVmBootDiagnosticsData의 경로 확인 문제가 해결되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2715">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="c16ab-2716">Compute 클라이언트 라이브러리가 25.0.0으로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2716">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="c16ab-2717">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="c16ab-2717">Az.KeyVault</span></span>
* <span data-ttu-id="c16ab-2718">와일드카드 지원이 KeyVault cmdlet에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2718">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="c16ab-2719">Az.Network</span><span class="sxs-lookup"><span data-stu-id="c16ab-2719">Az.Network</span></span>
* <span data-ttu-id="c16ab-2720">Azure Firewall에 대한 위협 인텔리전스 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2720">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="c16ab-2721">Application Gateway 방화벽 정책의 최상위 수준 리소스 및 사용자 지정 규칙이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2721">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="c16ab-2722">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="c16ab-2722">Az.RecoveryServices</span></span>
* <span data-ttu-id="c16ab-2723">인스턴트 RP를 지원하기 위해 SnapshotRetentionInDays가 Azure VM 정책에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2723">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="c16ab-2724">컨테이너 등록을 취소하는 파이프 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2724">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="c16ab-2725">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="c16ab-2725">Az.Resources</span></span>
* <span data-ttu-id="c16ab-2726">Get-AzResource 및 Get-AzResourceGroup에 대한 와일드카드 지원을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2726">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="c16ab-2727">ARM에 대한 일반 호출을 수행할 때 사용되는 자격 증명을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2727">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="c16ab-2728">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="c16ab-2728">Az.Sql</span></span>
* <span data-ttu-id="c16ab-2729">위협 탐지의 cmdlet 매개 변수(ExcludeDetectionType)가 DetectionType에서 string[]으로 변경되어 새 DetectionType이 추가되면 이후의 증명이 되고 자동 완성도 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2729">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="c16ab-2730">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="c16ab-2730">Az.Storage</span></span>
* <span data-ttu-id="c16ab-2731">스토리지 계정에 대한 관리 정책 가져오기/설정/제거를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2731">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="c16ab-2732">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="c16ab-2732">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="c16ab-2733">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="c16ab-2733">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="c16ab-2734">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="c16ab-2734">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="c16ab-2735">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="c16ab-2735">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="c16ab-2736">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="c16ab-2736">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="c16ab-2737">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="c16ab-2737">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="c16ab-2738">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="c16ab-2738">Az.Websites</span></span>
* <span data-ttu-id="c16ab-2739">'New-AzWebApp -IncludeSourceWebAppSlots'를 사용하여 모든 슬롯의 복제를 중단하는 ARM 템플릿 버그가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2739">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span>

## <a name="150---march-2019"></a><span data-ttu-id="c16ab-2740">1.5.0 - 2019년 3월</span><span class="sxs-lookup"><span data-stu-id="c16ab-2740">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="c16ab-2741">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="c16ab-2741">Az.Accounts</span></span>
* <span data-ttu-id="c16ab-2742">'Register-AzModule' 명령을 추가하여 AutoRest 생성 cmdlet을 지원</span><span class="sxs-lookup"><span data-stu-id="c16ab-2742">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="c16ab-2743">Connect-AzAccount 예제 업데이트</span><span class="sxs-lookup"><span data-stu-id="c16ab-2743">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="c16ab-2744">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="c16ab-2744">Az.Automation</span></span>
* <span data-ttu-id="c16ab-2745">몇몇 Azure Automation cmdlet에서 특정 월별 일정을 검색할 때 발생하는 문제 수정</span><span class="sxs-lookup"><span data-stu-id="c16ab-2745">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="c16ab-2746">상위 20개 노드를 반환하도록 Get-AzAutomationDscNode를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2746">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="c16ab-2747">이제 모든 노드 반환</span><span class="sxs-lookup"><span data-stu-id="c16ab-2747">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="c16ab-2748">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="c16ab-2748">Az.Cdn</span></span>
* <span data-ttu-id="c16ab-2749">사용자 지정 도메인 Https 사용/사용 안 함에 대한 새 Powershell cmdlet이 추가되었으며 기존의 것은 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2749">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="c16ab-2750">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="c16ab-2750">Az.Compute</span></span>
* <span data-ttu-id="c16ab-2751">Get cmdlet에 와일드 카드 지원 추가</span><span class="sxs-lookup"><span data-stu-id="c16ab-2751">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="c16ab-2752">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="c16ab-2752">Az.DataFactory</span></span>
* <span data-ttu-id="c16ab-2753">ADF.Net SDK 버전이 3.0.1로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2753">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="c16ab-2754">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="c16ab-2754">Az.LogicApp</span></span>
* <span data-ttu-id="c16ab-2755">첫 결과 페이지 검색 시에만 ListWorkflows 수정</span><span class="sxs-lookup"><span data-stu-id="c16ab-2755">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="c16ab-2756">Az.Network</span><span class="sxs-lookup"><span data-stu-id="c16ab-2756">Az.Network</span></span>
* <span data-ttu-id="c16ab-2757">Network cmdlet에 와일드 카드 지원 추가</span><span class="sxs-lookup"><span data-stu-id="c16ab-2757">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="c16ab-2758">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="c16ab-2758">Az.RecoveryServices</span></span>
* <span data-ttu-id="c16ab-2759">Azure VM 지원에 SQL 서버가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2759">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="c16ab-2760">SDK 업데이트</span><span class="sxs-lookup"><span data-stu-id="c16ab-2760">SDK Update</span></span>
* <span data-ttu-id="c16ab-2761">VMappContainer 체크 인 Get-ProtectableItem 제거</span><span class="sxs-lookup"><span data-stu-id="c16ab-2761">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="c16ab-2762">Get ProtectableItem의 매개 변수로 Name과 ServerName이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2762">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="c16ab-2763">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="c16ab-2763">Az.Resources</span></span>
* <span data-ttu-id="c16ab-2764">`-TemplateObject` 매개 변수를 추가하여 cmdlet을 배포</span><span class="sxs-lookup"><span data-stu-id="c16ab-2764">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="c16ab-2765">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/2933 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2765">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="c16ab-2766">`Get-AzResource`의 결과를 `Set-AzResource`(으)로 파이프할 때 발생하는 문제 수정</span><span class="sxs-lookup"><span data-stu-id="c16ab-2766">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="c16ab-2767">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/8240 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2767">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="c16ab-2768">실행 시 JSON 데이터 형식 문제 해결 `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="c16ab-2768">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="c16ab-2769">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/7930 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2769">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="c16ab-2770">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="c16ab-2770">Az.Sql</span></span>
* <span data-ttu-id="c16ab-2771">AuditingEndpointsCommunicator를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2771">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="c16ab-2772">새 진단 설정을 생성할 때 에지 사례의 동작을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2772">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="c16ab-2773">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="c16ab-2773">Az.Storage</span></span>
* <span data-ttu-id="c16ab-2774">스토리지 계정      - New-AzStorageAccount를 생성할 때 종류 BlockBlobStorage를 지원</span><span class="sxs-lookup"><span data-stu-id="c16ab-2774">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="c16ab-2775">1.4.0 - 2019년 2월</span><span class="sxs-lookup"><span data-stu-id="c16ab-2775">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="c16ab-2776">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="c16ab-2776">Az.AnalysisServices</span></span>
* <span data-ttu-id="c16ab-2777">사용되지 않는 AddAzureASAccount cmdlet</span><span class="sxs-lookup"><span data-stu-id="c16ab-2777">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="c16ab-2778">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="c16ab-2778">Az.Automation</span></span>
* <span data-ttu-id="c16ab-2779">Import-AzAutomationDscNodeConfiguration 도움말 업데이트</span><span class="sxs-lookup"><span data-stu-id="c16ab-2779">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="c16ab-2780">Import-AzAutomationDscConfiguration cmdlet 구성 이름 유효성 검사 추가</span><span class="sxs-lookup"><span data-stu-id="c16ab-2780">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="c16ab-2781">Import-AzAutomationDscConfiguration cmdlet 오류 처리 개선</span><span class="sxs-lookup"><span data-stu-id="c16ab-2781">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="c16ab-2782">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="c16ab-2782">Az.CognitiveServices</span></span>
* <span data-ttu-id="c16ab-2783">리소스의 하위 도메인을 지정하는 데 사용되는 New-AzCognitiveServicesAccount에 대한 새 선택적 매개 변수로 CustomSubdomainName이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2783">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="c16ab-2784">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="c16ab-2784">Az.Compute</span></span>
* <span data-ttu-id="c16ab-2785">ID 매개 변수 집합 문제 해결</span><span class="sxs-lookup"><span data-stu-id="c16ab-2785">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="c16ab-2786">Name 매개 변수를 제공하지 않으면 Get-AzVMExtension이 설치된 모든 확장을 열거하도록 업데이트</span><span class="sxs-lookup"><span data-stu-id="c16ab-2786">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="c16ab-2787">Update-AzImage cmdlet에 태그 및 ResourceId 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="c16ab-2787">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="c16ab-2788">인스턴스 ID가 없는 Get-AzVmssVM과 InstanceView를 사용하면 인스턴스 보기가 있는 VMSS VM을 나열할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2788">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="c16ab-2789">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="c16ab-2789">Az.DataLakeStore</span></span>
* <span data-ttu-id="c16ab-2790">ADL 삭제된 항목 열거 및 복원에 대한 cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="c16ab-2790">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="c16ab-2791">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="c16ab-2791">Az.EventHub</span></span>
* <span data-ttu-id="c16ab-2792">Eventhub의 CaptureDescription 클래스에서 빈 보관을 건너뛰는 새 부울 속성 SkipEmptyArchives가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2792">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="c16ab-2793">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="c16ab-2793">Az.KeyVault</span></span>
* <span data-ttu-id="c16ab-2794">Set-AzKeyVaultSecret 태그 지정 수정</span><span class="sxs-lookup"><span data-stu-id="c16ab-2794">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="c16ab-2795">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="c16ab-2795">Az.LogicApp</span></span>
* <span data-ttu-id="c16ab-2796">통합 계정에 대한 기본 sku 추가</span><span class="sxs-lookup"><span data-stu-id="c16ab-2796">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="c16ab-2797">XSLT 2.0, XSLT 3.0, Liquid 맵 형식 추가</span><span class="sxs-lookup"><span data-stu-id="c16ab-2797">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="c16ab-2798">통합 계정 어셈블리에 대한 새 cmdlet</span><span class="sxs-lookup"><span data-stu-id="c16ab-2798">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="c16ab-2799">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="c16ab-2799">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="c16ab-2800">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="c16ab-2800">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="c16ab-2801">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="c16ab-2801">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="c16ab-2802">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="c16ab-2802">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="c16ab-2803">통합 계정 일괄 처리 구성에 대한 새 cmdlet</span><span class="sxs-lookup"><span data-stu-id="c16ab-2803">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="c16ab-2804">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="c16ab-2804">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="c16ab-2805">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="c16ab-2805">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="c16ab-2806">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="c16ab-2806">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="c16ab-2807">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="c16ab-2807">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="c16ab-2808">논리 앱 SDK를 버전 4.1.0으로 업데이트</span><span class="sxs-lookup"><span data-stu-id="c16ab-2808">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="c16ab-2809">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="c16ab-2809">Az.Monitor</span></span>
* <span data-ttu-id="c16ab-2810">Get-AzMetric에 대한 도움말 업데이트</span><span class="sxs-lookup"><span data-stu-id="c16ab-2810">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="c16ab-2811">Az.Network</span><span class="sxs-lookup"><span data-stu-id="c16ab-2811">Az.Network</span></span>
* <span data-ttu-id="c16ab-2812">Add-AzApplicationGatewayCustomError에 대한 도움말 예제 업데이트</span><span class="sxs-lookup"><span data-stu-id="c16ab-2812">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="c16ab-2813">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="c16ab-2813">Az.OperationalInsights</span></span>
* <span data-ttu-id="c16ab-2814">New 및 Get ApplicationInsights 데이터 소스에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="c16ab-2814">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="c16ab-2815">지정된 작업 영역에 대한 특정 또는 전체 ApplicationInsights 데이터 원본 가져오기를 지원하기 위한 새로운 'ApplicationInsights' 종류가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2815">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span>
    - <span data-ttu-id="c16ab-2816">지정된 Application-Insights 리소스 매개 변수(구독 ID, resourceGroupName 및 이름)별로 데이터 원본을 만들기 위한 New-AzOperationalInsightsApplicationInsightsDataSource cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2816">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span>

#### <a name="azresources"></a><span data-ttu-id="c16ab-2817">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="c16ab-2817">Az.Resources</span></span>
* <span data-ttu-id="c16ab-2818">문제 https://github.com/Azure/azure-powershell/issues/8166 수정</span><span class="sxs-lookup"><span data-stu-id="c16ab-2818">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="c16ab-2819">문제 https://github.com/Azure/azure-powershell/issues/8235 수정</span><span class="sxs-lookup"><span data-stu-id="c16ab-2819">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="c16ab-2820">문제 https://github.com/Azure/azure-powershell/issues/6219 수정</span><span class="sxs-lookup"><span data-stu-id="c16ab-2820">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="c16ab-2821">KeyCredentials 반복 만들기를 방지하기 위해 버그 수정</span><span class="sxs-lookup"><span data-stu-id="c16ab-2821">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="c16ab-2822">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="c16ab-2822">Az.Sql</span></span>
* <span data-ttu-id="c16ab-2823">SQL DB 하이퍼스케일에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="c16ab-2823">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="c16ab-2824">복원 요청에서 불필요한 속성을 설정하여 복원이 실패할 수 있는 버그 수정</span><span class="sxs-lookup"><span data-stu-id="c16ab-2824">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="c16ab-2825">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="c16ab-2825">Az.Websites</span></span>
* <span data-ttu-id="c16ab-2826">Get-AzWebAppSlotMetrics 내 올바른 예제</span><span class="sxs-lookup"><span data-stu-id="c16ab-2826">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="c16ab-2827">1.3.0 - 2019년 2월</span><span class="sxs-lookup"><span data-stu-id="c16ab-2827">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="c16ab-2828">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="c16ab-2828">Az.Accounts</span></span>
* <span data-ttu-id="c16ab-2829">ClientRuntime 최신 버전 업데이트</span><span class="sxs-lookup"><span data-stu-id="c16ab-2829">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="c16ab-2830">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="c16ab-2830">Az.AnalysisServices</span></span>
<span data-ttu-id="c16ab-2831">Az.AnalysisServices 모듈의 전반적인 가용성.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2831">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="c16ab-2832">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="c16ab-2832">Az.Compute</span></span>
* <span data-ttu-id="c16ab-2833">AEM 확장: UltraSSD 및 P60, P70, P80 디스크에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="c16ab-2833">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="c16ab-2834">Set-AzVMBootDiagnostics에 대한 도움말 업데이트</span><span class="sxs-lookup"><span data-stu-id="c16ab-2834">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="c16ab-2835">Update-AzImage에 대한 도움말 및 예제 업데이트</span><span class="sxs-lookup"><span data-stu-id="c16ab-2835">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="c16ab-2836">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="c16ab-2836">Az.RecoveryServices</span></span>
<span data-ttu-id="c16ab-2837">Az.RecoveryServices 모듈의 전반적인 가용성.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2837">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="c16ab-2838">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="c16ab-2838">Az.Resources</span></span>
* <span data-ttu-id="c16ab-2839">리소스 그룹 관련 태그 수정</span><span class="sxs-lookup"><span data-stu-id="c16ab-2839">Fix tagging for resource groups</span></span>
    - <span data-ttu-id="c16ab-2840">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/8166 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2840">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="c16ab-2841">`Get-AzureRmRoleAssignment`이(가) -ErrorAction을 준수하지 않는 문제 수정</span><span class="sxs-lookup"><span data-stu-id="c16ab-2841">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span>
    - <span data-ttu-id="c16ab-2842">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/8235 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2842">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="c16ab-2843">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="c16ab-2843">Az.Sql</span></span>
* <span data-ttu-id="c16ab-2844">AzSqlDatabaseBackupShortTermRetentionPolicy 가져오기/설정하기 추가</span><span class="sxs-lookup"><span data-stu-id="c16ab-2844">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="c16ab-2845">SQL cmdlet을 실행할 경우 Azure 계정에 로그인되어 있지 않은 것이 nullref 예외를 초래하는 문제 수정</span><span class="sxs-lookup"><span data-stu-id="c16ab-2845">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="c16ab-2846">Get-AzSqlCapability의 nullref 예외 수정</span><span class="sxs-lookup"><span data-stu-id="c16ab-2846">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="c16ab-2847">1.2.1 - 2019년 1월</span><span class="sxs-lookup"><span data-stu-id="c16ab-2847">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="c16ab-2848">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="c16ab-2848">Az.Accounts</span></span>
* <span data-ttu-id="c16ab-2849">올바른 인증 버전을 사용하여 릴리스</span><span class="sxs-lookup"><span data-stu-id="c16ab-2849">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="c16ab-2850">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="c16ab-2850">Az.AnalysisServices</span></span>
* <span data-ttu-id="c16ab-2851">업데이트된 인증 종속성을 사용하여 릴리스</span><span class="sxs-lookup"><span data-stu-id="c16ab-2851">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="c16ab-2852">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="c16ab-2852">Az.RecoveryServices</span></span>
* <span data-ttu-id="c16ab-2853">업데이트된 인증 종속성을 사용하여 릴리스</span><span class="sxs-lookup"><span data-stu-id="c16ab-2853">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="c16ab-2854">1.2.0 - 2019년 1월</span><span class="sxs-lookup"><span data-stu-id="c16ab-2854">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="c16ab-2855">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="c16ab-2855">Az.Accounts</span></span>
* <span data-ttu-id="c16ab-2856">Windows PowerShell 5.1 전용 대화형 사용자 이름/암호 인증 추가</span><span class="sxs-lookup"><span data-stu-id="c16ab-2856">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="c16ab-2857">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="c16ab-2857">Update incorrect online help URLs</span></span>
* <span data-ttu-id="c16ab-2858">Uninstall-AzureRm 관련 PS Core에 경고 메시지 추가</span><span class="sxs-lookup"><span data-stu-id="c16ab-2858">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="c16ab-2859">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="c16ab-2859">Az.Aks</span></span>
* <span data-ttu-id="c16ab-2860">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="c16ab-2860">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="c16ab-2861">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="c16ab-2861">Az.Automation</span></span>
* <span data-ttu-id="c16ab-2862">Python 2 Runbook에 대한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2862">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="c16ab-2863">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="c16ab-2863">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="c16ab-2864">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="c16ab-2864">Az.Cdn</span></span>
* <span data-ttu-id="c16ab-2865">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="c16ab-2865">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="c16ab-2866">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="c16ab-2866">Az.Compute</span></span>
* <span data-ttu-id="c16ab-2867">Invoke-AzVMReimage cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="c16ab-2867">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="c16ab-2868">Set-AzVmss에 TempDisk 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="c16ab-2868">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="c16ab-2869">New-AzVM 경고 메시지 수정</span><span class="sxs-lookup"><span data-stu-id="c16ab-2869">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="c16ab-2870">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="c16ab-2870">Az.ContainerRegistry</span></span>
* <span data-ttu-id="c16ab-2871">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="c16ab-2871">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="c16ab-2872">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="c16ab-2872">Az.DataFactory</span></span>
* <span data-ttu-id="c16ab-2873">ADF.Net SDK 버전이 3.0.0으로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2873">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="c16ab-2874">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="c16ab-2874">Az.DataLakeStore</span></span>
* <span data-ttu-id="c16ab-2875">MSI를 사용할 때 ADLS 엔드포인트 문제 수정</span><span class="sxs-lookup"><span data-stu-id="c16ab-2875">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="c16ab-2876">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/7462 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2876">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="c16ab-2877">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="c16ab-2877">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="c16ab-2878">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="c16ab-2878">Az.IotHub</span></span>
* <span data-ttu-id="c16ab-2879">Add-IotHubRoutingEndpoint cmdlet에 인코딩 형식을 추가하세요.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2879">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="c16ab-2880">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="c16ab-2880">Az.KeyVault</span></span>
* <span data-ttu-id="c16ab-2881">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="c16ab-2881">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="c16ab-2882">Az.Network</span><span class="sxs-lookup"><span data-stu-id="c16ab-2882">Az.Network</span></span>
* <span data-ttu-id="c16ab-2883">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="c16ab-2883">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="c16ab-2884">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="c16ab-2884">Az.Resources</span></span>
* <span data-ttu-id="c16ab-2885">'New-AzADAppCredential' 및 'New-AzADSpCredential' 참조 설명서의 잘못된 예제 수정</span><span class="sxs-lookup"><span data-stu-id="c16ab-2885">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="c16ab-2886">리소스 그룹 배포 cmdlet 실행 전 '-TemplateFile' 매개 변수 경로가 확인되지 않는 문제 수정</span><span class="sxs-lookup"><span data-stu-id="c16ab-2886">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="c16ab-2887">Az.Resources: New-AzureRmPolicyDefinition -Mode 기본값에 대한 올바른 설명서</span><span class="sxs-lookup"><span data-stu-id="c16ab-2887">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="c16ab-2888">Az.Resources: 문제 https://github.com/Azure/azure-powershell/issues/7522 수정</span><span class="sxs-lookup"><span data-stu-id="c16ab-2888">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="c16ab-2889">Az.Resources: 문제 https://github.com/Azure/azure-powershell/issues/5747 수정</span><span class="sxs-lookup"><span data-stu-id="c16ab-2889">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="c16ab-2890">'PSResourceGroupDeployment' 개체의 서식 문제 수정</span><span class="sxs-lookup"><span data-stu-id="c16ab-2890">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="c16ab-2891">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/2123 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2891">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="c16ab-2892">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="c16ab-2892">Az.ServiceFabric</span></span>
* <span data-ttu-id="c16ab-2893">인증서가 VMSS 모델에 추가되었는데도 예외가 발생할 경우 롤백합니다. 이는 버그 https://github.com/Azure/service-fabric-issues/issues/932 를 수정하기 위함입니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2893">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="c16ab-2894">일부 오류 메시지를 수정하세요.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2894">Fix some error messages.</span></span>
* <span data-ttu-id="c16ab-2895">Az로의 마이그레이션을 통해서는 작동하지 않는 New-AzServiceFabriCluster를 위해 기본값 ARM 템플릿을 가진 클러스터 만들기를 수정하세요.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2895">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="c16ab-2896">확장에서 클러스터 id를 확인하여 클러스터에 해당하는 VMSS에만 추가되도록 클러스터/애플리케이션 인증서 추가를 수정하세요.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2896">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="c16ab-2897">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="c16ab-2897">Az.SignalR</span></span>
* <span data-ttu-id="c16ab-2898">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="c16ab-2898">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="c16ab-2899">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="c16ab-2899">Az.Sql</span></span>
* <span data-ttu-id="c16ab-2900">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="c16ab-2900">Update incorrect online help URLs</span></span>
* <span data-ttu-id="c16ab-2901">가능한 값을 가진 LicenseType 매개 변수에 대한 매개 변수 설명이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2901">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="c16ab-2902">유일하게 업데이트된 속성인데 작동하지 않는 관리되는 인스턴스 ID의 업데이트 수정</span><span class="sxs-lookup"><span data-stu-id="c16ab-2902">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="c16ab-2903">관리되는 인스턴스에서의 사용자 지정 데이터 정렬에 대한 지원</span><span class="sxs-lookup"><span data-stu-id="c16ab-2903">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="c16ab-2904">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="c16ab-2904">Az.Storage</span></span>
* <span data-ttu-id="c16ab-2905">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="c16ab-2905">Update incorrect online help URLs</span></span>
* <span data-ttu-id="c16ab-2906">Premium Storage 계정이 클래식 로깅/메트릭을 지원하지 않기 때문에, Premium Storage 계정의 클래식 로깅/메트릭을 가져올/설정할 때 상세한 오류 메시지를 제공해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2906">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="c16ab-2907">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="c16ab-2907">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="c16ab-2908">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="c16ab-2908">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="c16ab-2909">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="c16ab-2909">Az.TrafficManager</span></span>
* <span data-ttu-id="c16ab-2910">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="c16ab-2910">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="c16ab-2911">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="c16ab-2911">Az.Websites</span></span>
* <span data-ttu-id="c16ab-2912">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="c16ab-2912">Update incorrect online help URLs</span></span>
* <span data-ttu-id="c16ab-2913">앱이 ASE에 호스팅되면 'New-AzWebAppSSLBinding'을 수정하여 올바른 resourcegroup+location에 인증서를 업로드합니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2913">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="c16ab-2914">'New-AzWebAppSSLBinding'을 수정하여 SSL 인증서를 앱에 바인딩하는 데 붙는 태그를 덮어쓰지 않도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2914">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="c16ab-2915">1.1.0 - 2019년 1월</span><span class="sxs-lookup"><span data-stu-id="c16ab-2915">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="c16ab-2916">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="c16ab-2916">Az.Accounts</span></span>
* <span data-ttu-id="c16ab-2917">Enable-AzureRmAlias에 'Local' 범위 추가</span><span class="sxs-lookup"><span data-stu-id="c16ab-2917">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="c16ab-2918">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="c16ab-2918">Az.Compute</span></span>
* <span data-ttu-id="c16ab-2919">이름이 Restart/Start/Stop/Remove/Set-AzVM과 Save-AzVMImage에 설정된 ID 매개 변수에서 선택 사항이 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2919">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="c16ab-2920">도움말 파일의 ID에 대한 설명이 업데이트 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2920">Updated the description of ID in help files</span></span>
* <span data-ttu-id="c16ab-2921">Az.Accounts 모듈을 사용할 때의 이전 버전과의 호환성 문제를 해결합니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2921">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="c16ab-2922">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="c16ab-2922">Az.DataLakeStore</span></span>
* <span data-ttu-id="c16ab-2923">SDK 수정을 위해 데이터 평면의 SDK 버전을 1.1.14로 업데이트하세요.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2923">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="c16ab-2924">getfilestatus 및 liststatus에 대한 음수 acesstime 및 modificationtime 수정, 비동기 취소 토큰 수정</span><span class="sxs-lookup"><span data-stu-id="c16ab-2924">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="c16ab-2925">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="c16ab-2925">Az.EventGrid</span></span>
* <span data-ttu-id="c16ab-2926">2019-01-01 API 버전을 사용하도록 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2926">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="c16ab-2927">2019-01-01 API 버전에서 새 시나리오를 지원하도록 다음 cmdlet을 업데이트</span><span class="sxs-lookup"><span data-stu-id="c16ab-2927">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="c16ab-2928">New-AzureRmEventGridSubscription: 지정을 위한 새로운 선택적 매개 변수를 추가</span><span class="sxs-lookup"><span data-stu-id="c16ab-2928">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="c16ab-2929">이벤트 Time-to-Live</span><span class="sxs-lookup"><span data-stu-id="c16ab-2929">Event Time-To-Live,</span></span>
        - <span data-ttu-id="c16ab-2930">이벤트에 대한 최대 배달 시도</span><span class="sxs-lookup"><span data-stu-id="c16ab-2930">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="c16ab-2931">배달 못한 편지의 엔드포인트입니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2931">Dead letter endpoint.</span></span>
    - <span data-ttu-id="c16ab-2932">Update-AzureRmEventGridSubscription: 지정을 위한 새로운 선택적 매개 변수를 추가</span><span class="sxs-lookup"><span data-stu-id="c16ab-2932">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="c16ab-2933">이벤트 Time-to-Live</span><span class="sxs-lookup"><span data-stu-id="c16ab-2933">Event Time-To-Live,</span></span>
        - <span data-ttu-id="c16ab-2934">이벤트에 대한 최대 배달 시도</span><span class="sxs-lookup"><span data-stu-id="c16ab-2934">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="c16ab-2935">배달 못한 편지의 엔드포인트입니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2935">Dead letter endpoint.</span></span>
* <span data-ttu-id="c16ab-2936">New-AzureRmEventGridSubscription 및 Update-AzureRmEventGridSubscription cmdlet의 EndpointType 옵션에 새 열거형 값(즉, storageQueue 및 hybridConnection)을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2936">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="c16ab-2937">이벤트 구독을 생성 또는 업데이트할 때 사용자가 직접 조치를 취해야 할 경우 경고 메시지를 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2937">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="c16ab-2938">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="c16ab-2938">Az.IotHub</span></span>
* <span data-ttu-id="c16ab-2939">최신 버전의 Azure IotHub SDK로 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="c16ab-2939">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="c16ab-2940">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="c16ab-2940">Az.LogicApp</span></span>
* <span data-ttu-id="c16ab-2941">지정된 이름이 없는 모든 Get-AzLogicApp 목록</span><span class="sxs-lookup"><span data-stu-id="c16ab-2941">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="c16ab-2942">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="c16ab-2942">Az.Resources</span></span>
* <span data-ttu-id="c16ab-2943">'Get-AzResource'에 '-ODataQuery'및 '-ResourceId' 매개 변수를 제공할 때 매개 변수 집합 문제 수정</span><span class="sxs-lookup"><span data-stu-id="c16ab-2943">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="c16ab-2944">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/7875 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2944">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="c16ab-2945">New/Set-AzPolicyDefinition에서 -Custom 매개 변수 처리 문제 수정</span><span class="sxs-lookup"><span data-stu-id="c16ab-2945">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="c16ab-2946">New-AzDeployment 설명서에서 오타 수정</span><span class="sxs-lookup"><span data-stu-id="c16ab-2946">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="c16ab-2947">'New-AzADUser'에 '-MailNickname'매개 변수가 필수 항목으로 지정됨</span><span class="sxs-lookup"><span data-stu-id="c16ab-2947">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="c16ab-2948">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/8220 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2948">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="c16ab-2949">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="c16ab-2949">Az.SignalR</span></span>
* <span data-ttu-id="c16ab-2950">Az.Accounts 모듈을 사용할 때의 이전 버전과의 호환성 문제를 해결합니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2950">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="c16ab-2951">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="c16ab-2951">Az.Sql</span></span>
* <span data-ttu-id="c16ab-2952">Storage 관리 클라이언트 종속성을 일반적인 SDK 구현으로 변환했습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2952">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="c16ab-2953">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="c16ab-2953">Az.Storage</span></span>
* <span data-ttu-id="c16ab-2954">Sas Token, OAuth 또는 Anonymous를 사용하여 스토리지 컨텍스트의 StorageAccountName을 실제 스토리지 계정 이름으로 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2954">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="c16ab-2955">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="c16ab-2955">New-AzStorageContext</span></span>
* <span data-ttu-id="c16ab-2956">'-FullUri' 매개 변수를 사용하여 Blob 스냅샷 개체의 Sas Token을 생성하고 반환된 Uri를 스냅샷 Uri로 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2956">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="c16ab-2957">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="c16ab-2957">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="c16ab-2958">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="c16ab-2958">Az.Websites</span></span>
* <span data-ttu-id="c16ab-2959">'Get-AzDeletedWebApp'의 날짜 구문 분석 버그를 수정했습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2959">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="c16ab-2960">Az.Accounts 모듈을 사용할 때의 이전 버전과의 호환성 문제를 해결합니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2960">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="c16ab-2961">1.0.0 - 2018년 12월</span><span class="sxs-lookup"><span data-stu-id="c16ab-2961">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="c16ab-2962">일반</span><span class="sxs-lookup"><span data-stu-id="c16ab-2962">General</span></span>

- <span data-ttu-id="c16ab-2963">Az 모듈 일반 공급</span><span class="sxs-lookup"><span data-stu-id="c16ab-2963">General Availability of Az Module</span></span>
- <span data-ttu-id="c16ab-2964">각 모듈에 대 한 온라인 도움말</span><span class="sxs-lookup"><span data-stu-id="c16ab-2964">Online help for each module</span></span>
- <span data-ttu-id="c16ab-2965">자세한 내용과 로드맵은 [Az 알림 페이지](https://aka.ms/azps-announce)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2965">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="c16ab-2966">AzureRM에서 마이그레이션하는 것에 대한 정보는 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2966">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="c16ab-2967">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="c16ab-2967">Az.Accounts</span></span>
- <span data-ttu-id="c16ab-2968">Az.Profile에서 변경</span><span class="sxs-lookup"><span data-stu-id="c16ab-2968">Changed from Az.Profile</span></span>
- <span data-ttu-id="c16ab-2969">프로필 및 컨텍스트 형식에 대한 표 형식 수정</span><span class="sxs-lookup"><span data-stu-id="c16ab-2969">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="c16ab-2970">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="c16ab-2970">Az.ApiManagement</span></span>
- <span data-ttu-id="c16ab-2971">#7002에 대한 수정</span><span class="sxs-lookup"><span data-stu-id="c16ab-2971">Fixes for #7002</span></span>
- <span data-ttu-id="c16ab-2972">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2972">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="c16ab-2973">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="c16ab-2973">Az.Batch</span></span>
- <span data-ttu-id="c16ab-2974">`PSComputeNode`의 새로운 `NodeAgentInformation` 속성을 통해 풀의 각 VM에서 실행 중인 Azure Batch 노드 에이전트의 버전을 확인하는 기능이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2974">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="c16ab-2975">`PSDataDisk`에 대한 `Caching` 기본 값은 이제 `None` 대신 `ReadWrite`입니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2975">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="c16ab-2976">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2976">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="c16ab-2977">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="c16ab-2977">Az.Billing</span></span>
- <span data-ttu-id="c16ab-2978">청구, 소비 및 UsageAggregates cmdlet 결합 cmdlet에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2978">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="c16ab-2979">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="c16ab-2979">Az.CognitivServices</span></span>
- <span data-ttu-id="c16ab-2980">New-AzureRmCognitiveServicesAccount 작업에서 사용 가능한 SkuName 및 Typem에 대한 완성자 추가</span><span class="sxs-lookup"><span data-stu-id="c16ab-2980">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="c16ab-2981">Get-AzCognitiveServicesAccountSkus에서 GetSkusWithAccountParamSetName 매개 변수 집합을 제거</span><span class="sxs-lookup"><span data-stu-id="c16ab-2981">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="c16ab-2982">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="c16ab-2982">Az.ContainerInstance</span></span>
- <span data-ttu-id="c16ab-2983">ManagedIdentity 지원이 추가됨</span><span class="sxs-lookup"><span data-stu-id="c16ab-2983">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="c16ab-2984">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="c16ab-2984">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="c16ab-2985">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2985">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="c16ab-2986">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="c16ab-2986">Az.DataLakeStore</span></span>
- <span data-ttu-id="c16ab-2987">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2987">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="c16ab-2988">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="c16ab-2988">Az.Monitor</span></span>
- <span data-ttu-id="c16ab-2989">Az.Monitor 이름 변경 및 기타 사소한 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2989">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="c16ab-2990">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="c16ab-2990">Az.KeyVault</span></span>
- <span data-ttu-id="c16ab-2991">출력 형식에서 사용되지 않는 'PurgeDisabled' 속성 제거</span><span class="sxs-lookup"><span data-stu-id="c16ab-2991">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="c16ab-2992">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="c16ab-2992">Az.MachineLearning</span></span>
- <span data-ttu-id="c16ab-2993">Az.MachineLearningCompute 모듈의 cmdlet 포함</span><span class="sxs-lookup"><span data-stu-id="c16ab-2993">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="c16ab-2994">Az.Media</span><span class="sxs-lookup"><span data-stu-id="c16ab-2994">Az.Media</span></span>
- <span data-ttu-id="c16ab-2995">New-AzMediaService에서 사용되지 않는 -Tags 별칭이 제거됨</span><span class="sxs-lookup"><span data-stu-id="c16ab-2995">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="c16ab-2996">Az.Network</span><span class="sxs-lookup"><span data-stu-id="c16ab-2996">Az.Network</span></span>
<span data-ttu-id="c16ab-2997">Application Gateway에서 RewriteRuleSets를 구성하는 것에 대한 지원이 추가됨</span><span class="sxs-lookup"><span data-stu-id="c16ab-2997">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="c16ab-2998">추가된 새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-2998">New cmdlets added:</span></span>
        - <span data-ttu-id="c16ab-2999">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="c16ab-2999">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="c16ab-3000">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="c16ab-3000">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="c16ab-3001">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="c16ab-3001">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="c16ab-3002">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="c16ab-3002">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="c16ab-3003">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="c16ab-3003">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="c16ab-3004">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="c16ab-3004">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="c16ab-3005">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="c16ab-3005">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="c16ab-3006">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="c16ab-3006">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="c16ab-3007">선택적 매개 변수를 사용하도록 cmdlet이 업데이트됨 -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="c16ab-3007">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="c16ab-3008">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c16ab-3008">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="c16ab-3009">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="c16ab-3009">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="c16ab-3010">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="c16ab-3010">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="c16ab-3011">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c16ab-3011">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="c16ab-3012">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="c16ab-3012">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="c16ab-3013">New-AzureRmApplicationGatewayUrlPathMapConfig로 ID를 사용하여 Application Gateway에 KeyVault 지원을 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-3013">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="c16ab-3014">선택적 매개 변수를 사용하도록 cmdlet이 업데이트됨 -KeyVaultSecretId, -KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="c16ab-3014">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="c16ab-3015">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="c16ab-3015">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="c16ab-3016">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="c16ab-3016">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="c16ab-3017">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="c16ab-3017">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="c16ab-3018">New-AzApplicationGateway cmdlet이 선택적 매개 변수를 사용하도록 업데이트됨 -UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="c16ab-3018">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="c16ab-3019">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="c16ab-3019">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="c16ab-3020">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="c16ab-3020">Az.OperationalInsights</span></span>
- <span data-ttu-id="c16ab-3021">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="c16ab-3021">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="c16ab-3022">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="c16ab-3022">Az.Profile</span></span>
- <span data-ttu-id="c16ab-3023">Az.Accounts에 모듈 이름이 변경됨</span><span class="sxs-lookup"><span data-stu-id="c16ab-3023">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="c16ab-3024">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="c16ab-3024">Az.RecoveryServices</span></span>
- <span data-ttu-id="c16ab-3025">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="c16ab-3025">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="c16ab-3026">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="c16ab-3026">Az.Resources</span></span>
- <span data-ttu-id="c16ab-3027">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="c16ab-3027">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="c16ab-3028">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="c16ab-3028">Az.ServiceFabric</span></span>
- <span data-ttu-id="c16ab-3029">일반 이름과 지문으로 지정 인증서 지원</span><span class="sxs-lookup"><span data-stu-id="c16ab-3029">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="c16ab-3030">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="c16ab-3030">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="c16ab-3031">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="c16ab-3031">Az.SIgnalR</span></span>
- <span data-ttu-id="c16ab-3032">SIgnalR에 대한 PowerShell cmdlet에 대한 일반 공급</span><span class="sxs-lookup"><span data-stu-id="c16ab-3032">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="c16ab-3033">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="c16ab-3033">Az.Sql</span></span>
- <span data-ttu-id="c16ab-3034">위협 탐지의 cmdlet에 새로운 Data_Exfiltration 및 Unsafe_Action 검색 유형 추가</span><span class="sxs-lookup"><span data-stu-id="c16ab-3034">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="c16ab-3035">Sql 감사 cmdlet에 대한 설명서 예제 업데이트</span><span class="sxs-lookup"><span data-stu-id="c16ab-3035">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="c16ab-3036">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="c16ab-3036">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="c16ab-3037">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="c16ab-3037">Az.Storage</span></span>
- <span data-ttu-id="c16ab-3038">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="c16ab-3038">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="c16ab-3039">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="c16ab-3039">Az.Websites</span></span>
- <span data-ttu-id="c16ab-3040">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="c16ab-3040">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="c16ab-3041">0.7.0 - 2018년 12월</span><span class="sxs-lookup"><span data-stu-id="c16ab-3041">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="c16ab-3042">일반</span><span class="sxs-lookup"><span data-stu-id="c16ab-3042">General</span></span>

* <span data-ttu-id="c16ab-3043">AzureRM에서 Az 전환 예정에 대한 사소한 변경</span><span class="sxs-lookup"><span data-stu-id="c16ab-3043">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="c16ab-3044">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="c16ab-3044">Az.Compute</span></span>

* <span data-ttu-id="c16ab-3045">`New-AzVm(ss)` cmdlet에 대한 간단한 매개 변수 집합에 UltraSSD 및 갤러리 이미지에 대한 지원을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-3045">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="c16ab-3046">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="c16ab-3046">Az.DataLakeStore</span></span>

* <span data-ttu-id="c16ab-3047">ADLS 계정의 도메인의 후행 슬래시를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-3047">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="c16ab-3048">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="c16ab-3048">Az.FrontDoor</span></span>

* <span data-ttu-id="c16ab-3049">일부 끊어진 링크 수정</span><span class="sxs-lookup"><span data-stu-id="c16ab-3049">Fixed some broken links</span></span>
    - <span data-ttu-id="c16ab-3050">New-AzureRmFrontDoor 및 Set-AzureRmFrontDoor 아티클에서 New-AzureRmFrontDoorHealthProbeSettingObject cmdlet 아티클에 대한 링크가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-3050">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="c16ab-3051">New-AzureRmFrontDoorManagedRuleObject 아티클에서 New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet 아티클에 대한 링크가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-3051">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="c16ab-3052">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="c16ab-3052">Az.RecoveryServices</span></span>

* <span data-ttu-id="c16ab-3053">Azure File Share 복원 작업에 클라이언트 측 유효성 검사가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-3053">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="c16ab-3054">afs 복원의 경우 storageAccountName 및 storageAccountResourceGroupName을 선택적으로 만들었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-3054">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="c16ab-3055">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="c16ab-3055">Az.Resources</span></span>

* <span data-ttu-id="c16ab-3056"> https://github.com/Azure/azure-powershell/issues/7679 에 대한 수정</span><span class="sxs-lookup"><span data-stu-id="c16ab-3056">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="c16ab-3057">기본 관리자를 요청할 때 구독 범위가 제공되는 경우 Get-AzureRmRoleAssignment를 업데이트하여 구독 범위를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-3057">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="c16ab-3058">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="c16ab-3058">Az.Sql</span></span>

* <span data-ttu-id="c16ab-3059">AzureRM에서 Az 전환 예정에 대한 사소한 변경</span><span class="sxs-lookup"><span data-stu-id="c16ab-3059">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="c16ab-3060">DotNet 코어에서 Get-AzureRmSqlDatabaseVulnerabilityAssessment를 사용하는 문제 해결</span><span class="sxs-lookup"><span data-stu-id="c16ab-3060">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="c16ab-3061">SQL 감사 cmdlet과 관련된 도움말 메시지의 설명서가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-3061">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="c16ab-3062">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="c16ab-3062">Az.Storage</span></span>

* <span data-ttu-id="c16ab-3063">New-AzureRmStorageAccount에 -EnableHierarchicalNamespace 추가</span><span class="sxs-lookup"><span data-stu-id="c16ab-3063">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="c16ab-3064">파일 복사 cmdlet이 -DestContext 입력이 없을 때 대상의 원본 컨텍스트를 다시 사용할 수 없는 문제 수정</span><span class="sxs-lookup"><span data-stu-id="c16ab-3064">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="c16ab-3065">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="c16ab-3065">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="c16ab-3066">고정적인 웹 사이트 구성 지원</span><span class="sxs-lookup"><span data-stu-id="c16ab-3066">Support Static Website configuration</span></span>
    - <span data-ttu-id="c16ab-3067">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="c16ab-3067">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="c16ab-3068">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="c16ab-3068">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="c16ab-3069">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="c16ab-3069">Az.Websites</span></span>

* <span data-ttu-id="c16ab-3070">Set-AzureRmWebApp 및 Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="c16ab-3070">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span>
    - <span data-ttu-id="c16ab-3071">Windows 및 Linux 컨테이너 응용 프로그램에 탑재할 Azure Storage 경로를 지정하기 위해 새 매개 변수(-AzureStoragePath)가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-3071">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="c16ab-3072">새 cmdlet New-AzureRmWebAppAzureStoragePath의 출력을 매개 변수로 사용하여 Azure Storage 경로를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-3072">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="c16ab-3073">0.6.1 - 2018년 11월</span><span class="sxs-lookup"><span data-stu-id="c16ab-3073">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="c16ab-3074">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="c16ab-3074">Az.ApiManagement</span></span>
* <span data-ttu-id="c16ab-3075">형식 매핑 문제에 대한 종속성 업데이트</span><span class="sxs-lookup"><span data-stu-id="c16ab-3075">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="c16ab-3076">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="c16ab-3076">Az.Automation</span></span>
* <span data-ttu-id="c16ab-3077">Azure Automation cmdlet 기반 Swagger</span><span class="sxs-lookup"><span data-stu-id="c16ab-3077">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="c16ab-3078">업데이트 관리 cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="c16ab-3078">Added Update Management cmdlets</span></span>
* <span data-ttu-id="c16ab-3079">소스 제어 cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="c16ab-3079">Added Source Control cmdlets</span></span>
* <span data-ttu-id="c16ab-3080">Remove-AzureRmAutomationHybridWorkerGroup cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="c16ab-3080">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="c16ab-3081">DSC 노드 등록 명령 수정</span><span class="sxs-lookup"><span data-stu-id="c16ab-3081">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="c16ab-3082">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="c16ab-3082">Az.Compute</span></span>
* <span data-ttu-id="c16ab-3083">SystemAssigned ID에 대한 ID 문제 수정</span><span class="sxs-lookup"><span data-stu-id="c16ab-3083">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="c16ab-3084">형식 매핑 문제에 대한 종속성 업데이트</span><span class="sxs-lookup"><span data-stu-id="c16ab-3084">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="c16ab-3085">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="c16ab-3085">Az.ContainerInstance</span></span>
* <span data-ttu-id="c16ab-3086">형식 매핑 문제에 대한 종속성 업데이트</span><span class="sxs-lookup"><span data-stu-id="c16ab-3086">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="c16ab-3087">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="c16ab-3087">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="c16ab-3088">마켓플레이스 cmdlet에 대한 예제 설명 업데이트</span><span class="sxs-lookup"><span data-stu-id="c16ab-3088">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="c16ab-3089">Az.Network</span><span class="sxs-lookup"><span data-stu-id="c16ab-3089">Az.Network</span></span>
* <span data-ttu-id="c16ab-3090">New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="c16ab-3090">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="c16ab-3091">지원되는 AzureFirewall 네트워크 프로토콜에 ICMP 다시 추가</span><span class="sxs-lookup"><span data-stu-id="c16ab-3091">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="c16ab-3092">Test-AzureRmNetworkWatcherConnectivity cmdlet을 업데이트하여 대상 ID, 주소 및 포트 유효성 검사를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-3092">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span>
* <span data-ttu-id="c16ab-3093">VirtualNetwork 맵의 메모리 사용 문제 해결</span><span class="sxs-lookup"><span data-stu-id="c16ab-3093">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="c16ab-3094">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="c16ab-3094">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="c16ab-3095">보호된 파일 공유에 대한 정책을 수정하는 것에 대해 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-3095">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="c16ab-3096">정책 표준 시간대를 대문자로 변환했습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-3096">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="c16ab-3097">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="c16ab-3097">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="c16ab-3098">New-AzureRmRecoveryServicesAsrProtectableItem의 예제 정정</span><span class="sxs-lookup"><span data-stu-id="c16ab-3098">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="c16ab-3099">형식 매핑 문제에 대한 종속성 업데이트</span><span class="sxs-lookup"><span data-stu-id="c16ab-3099">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="c16ab-3100">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="c16ab-3100">Az.Relay</span></span>
* <span data-ttu-id="c16ab-3101">선택적 매개 변수 -KeyValue를 New-AzureRmRelayKey cmdlet에 추가하여 사용자가 KeyValue를 제공할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-3101">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="c16ab-3102">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="c16ab-3102">Az.Resources</span></span>
* <span data-ttu-id="c16ab-3103">`New-AzureRmPolicyAssignment` 및 `Set-AzureRmPolicyAssignment`의 자원 ID 관련 매개 변수에 대한 도움말 문서를 업데이트함</span><span class="sxs-lookup"><span data-stu-id="c16ab-3103">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="c16ab-3104">-Metadata를 사용하는 New-AzureRmPolicyDefinition에 대한 예제 추가</span><span class="sxs-lookup"><span data-stu-id="c16ab-3104">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="c16ab-3105">NetStandard의 태그 키에서 대소문자 보존을 허용하도록 수정: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="c16ab-3105">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="c16ab-3106">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="c16ab-3106">Az.ServiceFabric</span></span>
* <span data-ttu-id="c16ab-3107">향후 호환성이 손상되는 변경에 대한 사용 중단 메시지 추가</span><span class="sxs-lookup"><span data-stu-id="c16ab-3107">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="c16ab-3108">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="c16ab-3108">Az.Sql</span></span>
* <span data-ttu-id="c16ab-3109">Azure Sql Database Managed Instance 및 Azure Sql Managed Database에 CRUD 작업을 위한 새 cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="c16ab-3109">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="c16ab-3110">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="c16ab-3110">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="c16ab-3111">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="c16ab-3111">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="c16ab-3112">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="c16ab-3112">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="c16ab-3113">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="c16ab-3113">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="c16ab-3114">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="c16ab-3114">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="c16ab-3115">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="c16ab-3115">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="c16ab-3116">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="c16ab-3116">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="c16ab-3117">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="c16ab-3117">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="c16ab-3118">서버 또는 데이터베이스에서 확장 감사 정책 관리를 활성화했습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-3118">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="c16ab-3119">새 매개 변수(PredicateExpression)가 감사 로그 필터링을 사용하도록 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-3119">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="c16ab-3120">Cmdlet이 레거시 클라이언트 대신 SQL 클라이언트를 사용하도록 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-3120">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="c16ab-3121">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="c16ab-3121">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="c16ab-3122">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="c16ab-3122">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="c16ab-3123">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="c16ab-3123">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="c16ab-3124">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="c16ab-3124">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="c16ab-3125">스토리지 계정 이름 매개 변수가 설정된 Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings를 사용할 때의 문제 해결</span><span class="sxs-lookup"><span data-stu-id="c16ab-3125">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="c16ab-3126">0.5.0 - 2018년 11월</span><span class="sxs-lookup"><span data-stu-id="c16ab-3126">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="c16ab-3127">일반</span><span class="sxs-lookup"><span data-stu-id="c16ab-3127">General</span></span>
* <span data-ttu-id="c16ab-3128">많은 핵심 cmdlet에 Resource Completers를 추가하여 대화형으로 cmdlet을 호출할 때 기존 리소스 이름을 탭으로 이동할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-3128">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="c16ab-3129">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="c16ab-3129">Az.Profile</span></span>
* <span data-ttu-id="c16ab-3130">ClientRuntime의 최신 버전을 사용하도록 일반적인 코드를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-3130">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="c16ab-3131">Connect-AzAccount cmdlet의 매개 변수 TenantId 이름을 Tenant로 바꾸고 TenantId의 별칭을 추가합니다</span><span class="sxs-lookup"><span data-stu-id="c16ab-3131">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="c16ab-3132">Connect-AzAccount의 업데이트된 TenantId 설명</span><span class="sxs-lookup"><span data-stu-id="c16ab-3132">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="c16ab-3133">테넌트 도메인을 제공할 때 실패한 로그인에 대한 오류 메시지 수정</span><span class="sxs-lookup"><span data-stu-id="c16ab-3133">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="c16ab-3134">테넌트에 구독이 없는 계정의 컨텍스트 이름 충돌 문제 수정</span><span class="sxs-lookup"><span data-stu-id="c16ab-3134">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="c16ab-3135">MSI를 사용할 때 DataLake 엔드포인트 문제 수정</span><span class="sxs-lookup"><span data-stu-id="c16ab-3135">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="c16ab-3136">연결되지 않은 경우 'Disconnect-AzAccount'가 throw하는 문제 수정</span><span class="sxs-lookup"><span data-stu-id="c16ab-3136">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="c16ab-3137">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="c16ab-3137">Az.CognitiveServices</span></span>
* <span data-ttu-id="c16ab-3138">Get-AzCognitiveServicesAccountSkus 작업을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-3138">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="c16ab-3139">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="c16ab-3139">Az.Compute</span></span>
* <span data-ttu-id="c16ab-3140">Add-AzVmssVMDataDisk 및 Remove-AzVmssVMDataDisk cmdlet를 추가합니다</span><span class="sxs-lookup"><span data-stu-id="c16ab-3140">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="c16ab-3141">Get-AzVMImage는 AutomaticOSUpgradeProperties를 표시합니다</span><span class="sxs-lookup"><span data-stu-id="c16ab-3141">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="c16ab-3142">수정된 SetAzVMChefExtension -BootstrapOptions 및 -JsonAttribute option 값이 json 형식으로 설정하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-3142">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="c16ab-3143">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="c16ab-3143">Az.DataLakeStore</span></span>
* <span data-ttu-id="c16ab-3144">DataLake 패키지를 1.1.10으로 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-3144">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="c16ab-3145">기본 동시성을 다중 스레드 작업에 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-3145">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="c16ab-3146">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="c16ab-3146">Az.Insights</span></span>
* <span data-ttu-id="c16ab-3147">해결된 문제 #7267(자동 크기 조정 영역)</span><span class="sxs-lookup"><span data-stu-id="c16ab-3147">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="c16ab-3148">열거된 매개 변수를 제대로 설정하지 않은 새 자동 크기 조정 규칙을 만드는 데 문제가 있습니다(이를 항상 기본값으로 설정함).</span><span class="sxs-lookup"><span data-stu-id="c16ab-3148">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="c16ab-3149">해결된 문제 # 7513[자세한 정보] Set-AzDiagnosticSetting은 설정을 생성하는 동안 범주를 명시적으로 지정해야 합니다</span><span class="sxs-lookup"><span data-stu-id="c16ab-3149">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="c16ab-3150">이제 cmdlet은 생성 중에 사용할 범주를 명시적으로 표시할 필요가 없습니다. 즉, 문서화된대로 작동합니다</span><span class="sxs-lookup"><span data-stu-id="c16ab-3150">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="c16ab-3151">Az.Network</span><span class="sxs-lookup"><span data-stu-id="c16ab-3151">Az.Network</span></span>
* <span data-ttu-id="c16ab-3152">다음 cmdlet에 대해 PeeringType을 필수 매개 변수로 변경했습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-3152">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="c16ab-3153">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="c16ab-3153">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="c16ab-3154">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="c16ab-3154">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="c16ab-3155">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="c16ab-3155">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="c16ab-3156">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="c16ab-3156">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="c16ab-3157">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="c16ab-3157">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="c16ab-3158">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="c16ab-3158">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="c16ab-3159">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="c16ab-3159">Az.PolicyInsights</span></span>
* <span data-ttu-id="c16ab-3160">추가된 정책 재구성 cmdlet</span><span class="sxs-lookup"><span data-stu-id="c16ab-3160">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="c16ab-3161">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="c16ab-3161">Az.Resources</span></span>
* <span data-ttu-id="c16ab-3162"> https://github.com/Azure/azure-powershell/issues/7402 에 대한 수정</span><span class="sxs-lookup"><span data-stu-id="c16ab-3162">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="c16ab-3163">'Get-AzResource'에 대해 '-ResourceId' 매개 변수를 사용하여 리소스 나열 허용</span><span class="sxs-lookup"><span data-stu-id="c16ab-3163">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="c16ab-3164">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="c16ab-3164">Az.ServiceBus</span></span>
* <span data-ttu-id="c16ab-3165">마이그레이션 상태를 알 수 있도록 PSServiceBusMigrationConfigurationAttributes에 MigrationState 읽기 전용 속성 추가.</span><span class="sxs-lookup"><span data-stu-id="c16ab-3165">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="c16ab-3166">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="c16ab-3166">Az.ServiceFabric</span></span>
* <span data-ttu-id="c16ab-3167">Linux Vmss에 인증서 추가 수정.</span><span class="sxs-lookup"><span data-stu-id="c16ab-3167">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="c16ab-3168">Add-AzServiceFabricClusterCertificate 수정</span><span class="sxs-lookup"><span data-stu-id="c16ab-3168">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="c16ab-3169">새 인증서(Azure/service-fabric-issues#932)에서 올바른 지문을 사용.</span><span class="sxs-lookup"><span data-stu-id="c16ab-3169">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="c16ab-3170">올바르게 예외 표시(Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="c16ab-3170">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="c16ab-3171">Vmss CreateOrUpdate 작업을 시작하기 전에 'Update-AzServiceFabricDurability'를 수정하여 클러스터 구성 업데이트.</span><span class="sxs-lookup"><span data-stu-id="c16ab-3171">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="c16ab-3172">0.4.0 - 2018년 10월</span><span class="sxs-lookup"><span data-stu-id="c16ab-3172">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="c16ab-3173">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="c16ab-3173">Az.Profile</span></span>
* <span data-ttu-id="c16ab-3174">CloudShell에서 Get-AzSubscription을 사용하여 문제를 해결합니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-3174">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="c16ab-3175">ClientRuntime의 최신 버전을 사용하도록 일반적인 코드를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-3175">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="c16ab-3176">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="c16ab-3176">Az.Compute</span></span>
* <span data-ttu-id="c16ab-3177">'New-AzVm'에 대해 간단한 매개 변수를 사용하는 경우 가속화된 네트워킹을 설정하기 위해 새 크기가 VM 크기의 허용 목록에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-3177">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="c16ab-3178">모든 cmdlet에 ResourceName 인수 완성자가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-3178">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="c16ab-3179">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="c16ab-3179">Az.DataLakeStore</span></span>
* <span data-ttu-id="c16ab-3180">Virtual Network 규칙에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="c16ab-3180">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="c16ab-3181">Get-AzDataLakeStoreVirtualNetworkRule: Azure Data Lake Store 가상 네트워크 규칙을 가져오거나 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-3181">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="c16ab-3182">Add-AzDataLakeStoreVirtualNetworkRule: 지정된 Data Lake Store 계정에 가상 네트워크 규칙을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-3182">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="c16ab-3183">Set-AzDataLakeStoreVirtualNetworkRule: 지정된 Data Lake Store 계정에 지정된 가상 네트워크 규칙을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-3183">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="c16ab-3184">Remove-AzDataLakeStoreVirtualNetworkRule: Azure Data Lake Store 가상 네트워크 규칙을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-3184">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="c16ab-3185">Az.Network</span><span class="sxs-lookup"><span data-stu-id="c16ab-3185">Az.Network</span></span>
* <span data-ttu-id="c16ab-3186">Test-AzNetworkWatcherConnectivity cmdlet을 업데이트하고, 백 엔드에 프로토콜 값을 전달합니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-3186">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="c16ab-3187">모든 cmdlet에 ResourceName 인수 완성자가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-3187">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="c16ab-3188">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="c16ab-3188">Az.Resources</span></span>
* <span data-ttu-id="c16ab-3189">(기본 프로필에 구독이 없고 범위가 지정되지 않은 경우) 시나리오에서 의미 있는 예외를 추가하여 Get-AzRoleDefinition이 인식할 수 없는 예외를 throw하는 문제를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-3189">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="c16ab-3190">또한 기본 매개 변수 집합을 'RoleDefinitionNameParameterSet'으로 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-3190">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="c16ab-3191">0.3.0 - 2018년 10월</span><span class="sxs-lookup"><span data-stu-id="c16ab-3191">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="c16ab-3192">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="c16ab-3192">Azure.Storage</span></span>
* <span data-ttu-id="c16ab-3193">대상에 메타데이터가 있을 때 Blob/파일이 메타 데이터를 복사하지 않는 문제 수정</span><span class="sxs-lookup"><span data-stu-id="c16ab-3193">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="c16ab-3194">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="c16ab-3194">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="c16ab-3195">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="c16ab-3195">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="c16ab-3196">특정 위치의 스토리지 리소스 사용을 지원하고 글로벌 스토리지 리소스 사용 가져오기는 더 이상 사용되지 않는다는 경고 메시지를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-3196">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="c16ab-3197">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="c16ab-3197">Get-AzStorageUsage</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="c16ab-3198">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="c16ab-3198">Az.CognitiveServices</span></span>
* <span data-ttu-id="c16ab-3199">기존 계정이 없는 Get-AzCognitiveServicesAccountSkus를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-3199">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="c16ab-3200">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="c16ab-3200">Az.Compute</span></span>
* <span data-ttu-id="c16ab-3201">Get-AzVM -ResourceGroupName <rg>가 필요한 경우 50개가 넘는 결과를 반환하도록 수정</span><span class="sxs-lookup"><span data-stu-id="c16ab-3201">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="c16ab-3202">'SimpleParameterSet' 예제가 New-AzVmss cmdlet 도움말에 추가됨</span><span class="sxs-lookup"><span data-stu-id="c16ab-3202">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="c16ab-3203">Azure Disk Encryption 진행률 메시지의 오타를 수정</span><span class="sxs-lookup"><span data-stu-id="c16ab-3203">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="c16ab-3204">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="c16ab-3204">Az.DataFactoryV2</span></span>
* <span data-ttu-id="c16ab-3205">ADF.Net SDK 버전을 2.3.0으로 업데이트</span><span class="sxs-lookup"><span data-stu-id="c16ab-3205">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="c16ab-3206">Az.Network</span><span class="sxs-lookup"><span data-stu-id="c16ab-3206">Az.Network</span></span>
* <span data-ttu-id="c16ab-3207">NetworkProfile 기능 추가</span><span class="sxs-lookup"><span data-stu-id="c16ab-3207">Added NetworkProfile functionality.</span></span> <span data-ttu-id="c16ab-3208">추가된 새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-3208">new cmdlets added</span></span>
    - <span data-ttu-id="c16ab-3209">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="c16ab-3209">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="c16ab-3210">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="c16ab-3210">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="c16ab-3211">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="c16ab-3211">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="c16ab-3212">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="c16ab-3212">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="c16ab-3213">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="c16ab-3213">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="c16ab-3214">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="c16ab-3214">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="c16ab-3215">서브넷 모델에 서비스 연결 링크 추가</span><span class="sxs-lookup"><span data-stu-id="c16ab-3215">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="c16ab-3216">New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="c16ab-3216">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="c16ab-3217">Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="c16ab-3217">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="c16ab-3218">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="c16ab-3218">Az.RedisCache</span></span>
* <span data-ttu-id="c16ab-3219">모든 문자열을 Size 매개 변수로 진행되도록 허용</span><span class="sxs-lookup"><span data-stu-id="c16ab-3219">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="c16ab-3220">PSArgumentCompleter 팝업에 P5 추가</span><span class="sxs-lookup"><span data-stu-id="c16ab-3220">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="c16ab-3221">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="c16ab-3221">Az.Resources</span></span>
* <span data-ttu-id="c16ab-3222">-Mode 매개 변수를 Set-AzPolicyDefinition에 추가</span><span class="sxs-lookup"><span data-stu-id="c16ab-3222">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="c16ab-3223">사용자가 포함된 Origin 작업에서 Get-AzProviderOperation commandlet 버그 수정</span><span class="sxs-lookup"><span data-stu-id="c16ab-3223">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="c16ab-3224">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="c16ab-3224">Az.Sql</span></span>
* <span data-ttu-id="c16ab-3225">일부 백업 cmdlet이 현재 azure 구독을 인식하지 않는 문제 해결</span><span class="sxs-lookup"><span data-stu-id="c16ab-3225">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="c16ab-3226">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="c16ab-3226">Az.Websites</span></span>
* <span data-ttu-id="c16ab-3227">새 cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - 컨테이너 지속적인 배포 Webhook URL을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-3227">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="c16ab-3228">새 cmdlet New-AzWebAppContainerPSSession 및 Enter-WebAppContainerPSSession -  windows 컨테이너 앱에 PowerShell 원격 세션을 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="c16ab-3228">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="c16ab-3229">0.2.0 - 2018년 9월</span><span class="sxs-lookup"><span data-stu-id="c16ab-3229">0.2.0 - September 2018</span></span>
 <span data-ttu-id="c16ab-3230">초기 릴리스</span><span class="sxs-lookup"><span data-stu-id="c16ab-3230">Initial Release</span></span>
