---
title: Azure PowerShell 릴리스 정보
description: Azure PowerShell 모듈의 모든 최신 업데이트에 대해 알아봅니다.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 10/15/2019
ms.openlocfilehash: fb934ed0f8bef5e2aff715debe5d406d54abf24f
ms.sourcegitcommit: 2d0c3ffaa5246f680784fa7e15b0d2536c27ff80
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/07/2020
ms.locfileid: "75718987"
---
# <a name="azure-powershell-release-notes"></a><span data-ttu-id="e51e5-103">Azure PowerShell 릴리스 정보</span><span class="sxs-lookup"><span data-stu-id="e51e5-103">Azure PowerShell release notes</span></span>

## <a name="330---january-2020"></a><span data-ttu-id="e51e5-104">3.3.0 - 2020년 1월</span><span class="sxs-lookup"><span data-stu-id="e51e5-104">3.3.0 - January 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="e51e5-105">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e51e5-105">Az.Accounts</span></span>
* <span data-ttu-id="e51e5-106">AzureAttestationServiceEndpointResourceId 및 AzureAttestationServiceEndpointSuffix 매개 변수를 허용하도록 Add-AzEnvironment 및 Set-AzEnvironment가 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="e51e5-106">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameters AzureAttestationServiceEndpointResourceId and AzureAttestationServiceEndpointSuffix</span></span>

#### <a name="azcdn"></a><span data-ttu-id="e51e5-107">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="e51e5-107">Az.Cdn</span></span>
* <span data-ttu-id="e51e5-108">New-AzCdnEndpoint cmdlet에서 오류 응답 세부 정보 표시</span><span class="sxs-lookup"><span data-stu-id="e51e5-108">Display error response deatil in New-AzCdnEndpoint cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e51e5-109">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e51e5-109">Az.Compute</span></span>
* <span data-ttu-id="e51e5-110">OS 프로필이 없는 관리 OD 디스크가 있는 VM의 Set-AzVMCustomScriptExtension cmdlet을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-110">Fix Set-AzVMCustomScriptExtension cmdlet for a VM with managed OD disk which does not have OS profile.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="e51e5-111">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="e51e5-111">Az.ContainerInstance</span></span>
* <span data-ttu-id="e51e5-112">New-AzContainerGroup의 예에서 사용되는 고정 매개 변수 이름</span><span class="sxs-lookup"><span data-stu-id="e51e5-112">Fixed parameter names used by example of New-AzContainerGroup</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="e51e5-113">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="e51e5-113">Az.DataBoxEdge</span></span>
* <span data-ttu-id="e51e5-114">'Get-AzDataBoxEdgeStorageContainer' cmdlet 추가됨</span><span class="sxs-lookup"><span data-stu-id="e51e5-114">Added cmdlet 'Get-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="e51e5-115">Edge 스토리지 컨테이너 가져오기</span><span class="sxs-lookup"><span data-stu-id="e51e5-115">Get the Edge Stroage Container</span></span>
* <span data-ttu-id="e51e5-116">'New-AzDataBoxEdgeStorageContainer' cmdlet 추가됨</span><span class="sxs-lookup"><span data-stu-id="e51e5-116">Added cmdlet 'New-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="e51e5-117">Edge 스토리지 컨테이너 만들기</span><span class="sxs-lookup"><span data-stu-id="e51e5-117">Create new Edge Stroage Container</span></span>
* <span data-ttu-id="e51e5-118">'Remove-AzDataBoxEdgeStorageContainer' cmdlet 추가됨</span><span class="sxs-lookup"><span data-stu-id="e51e5-118">Added cmdlet 'Remove-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="e51e5-119">Edge 스토리지 컨테이너 제거</span><span class="sxs-lookup"><span data-stu-id="e51e5-119">Remove the Edge Stroage Container</span></span>
* <span data-ttu-id="e51e5-120">'Invoke-AzDataBoxEdgeStorageContainer' cmdlet 추가됨</span><span class="sxs-lookup"><span data-stu-id="e51e5-120">Added cmdlet 'Invoke-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="e51e5-121">Edge 스토리지 컨테이너에서 데이터를 새로 고치는 작업 호출</span><span class="sxs-lookup"><span data-stu-id="e51e5-121">Invoke action to refresh data on Edge Stroage Container</span></span>
* <span data-ttu-id="e51e5-122">'Get-AzDataBoxEdgeStorageAccount' cmdlet 추가됨</span><span class="sxs-lookup"><span data-stu-id="e51e5-122">Added cmdlet 'Get-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="e51e5-123">Edge 스토리지 계정 가져오기</span><span class="sxs-lookup"><span data-stu-id="e51e5-123">Get the Edge Stroage Account</span></span>
* <span data-ttu-id="e51e5-124">'New-AzDataBoxEdgeStorageAccount' cmdlet 추가됨</span><span class="sxs-lookup"><span data-stu-id="e51e5-124">Added cmdlet 'New-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="e51e5-125">새 Edge 스토리지 계정 만들기</span><span class="sxs-lookup"><span data-stu-id="e51e5-125">Create new Edge Stroage Account</span></span>
* <span data-ttu-id="e51e5-126">'Remove-AzDataBoxEdgeStorageAccount' cmdlet 추가됨</span><span class="sxs-lookup"><span data-stu-id="e51e5-126">Added cmdlet 'Remove-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="e51e5-127">Edge 스토리지 계정 제거</span><span class="sxs-lookup"><span data-stu-id="e51e5-127">Remove the Edge Stroage Account</span></span>
* <span data-ttu-id="e51e5-128">'Invoke-AzDataBoxEdgeShare' cmdlet 호출</span><span class="sxs-lookup"><span data-stu-id="e51e5-128">Invoke cmdlet 'Invoke-AzDataBoxEdgeShare'</span></span>
  - <span data-ttu-id="e51e5-129">공유에서 데이터를 새로 고치는 작업 호출</span><span class="sxs-lookup"><span data-stu-id="e51e5-129">Invoke action to refresh data on share</span></span>
* <span data-ttu-id="e51e5-130">'Set-AzDataBoxEdgeStorageAccountCredential' cmdlet 추가됨</span><span class="sxs-lookup"><span data-stu-id="e51e5-130">Added cmdlet 'Set-AzDataBoxEdgeStorageAccountCredential'</span></span>
  - <span data-ttu-id="e51e5-131">az databoxedge 스토리지 계정 자격 증명 설정</span><span class="sxs-lookup"><span data-stu-id="e51e5-131">Set the az databoxedge storage account credential</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="e51e5-132">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="e51e5-132">Az.DataFactory</span></span>
* <span data-ttu-id="e51e5-133">Get-AzDataFactoryV2IntegrationRuntime cmd에 AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId 및 VersionStatus 속성 추가</span><span class="sxs-lookup"><span data-stu-id="e51e5-133">Add AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId and VersionStatus properties for Get-AzDataFactoryV2IntegrationRuntime cmd</span></span>
* <span data-ttu-id="e51e5-134">ADF .Net SDK 버전을 4.6.0으로 업데이트</span><span class="sxs-lookup"><span data-stu-id="e51e5-134">Update ADF .Net SDK version to 4.6.0</span></span>
* <span data-ttu-id="e51e5-135">고정 공용 IP 주소로 Azure-SSIS IR을 만들 수 있도록 'Set-AzureRmDataFactoryV2IntegrationRuntime'cmd에 대해 'PublicIPs' 매개 변수를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-135">Add parameter 'PublicIPs' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable create Azure-SSIS IR with static public IP addresses.</span></span>

#### <a name="azdevtestlabs"></a><span data-ttu-id="e51e5-136">Az.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="e51e5-136">Az.DevTestLabs</span></span>
* <span data-ttu-id="e51e5-137">Get-AzDtlAllowedVMSizesPolicy.md에서 끊어진 링크 제거</span><span class="sxs-lookup"><span data-stu-id="e51e5-137">Remove the broken link in Get-AzDtlAllowedVMSizesPolicy.md</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="e51e5-138">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="e51e5-138">Az.EventHub</span></span>
* <span data-ttu-id="e51e5-139">10634 문제 해결: eventhubnamespace 제거에 대한 null 개체 참조 수정</span><span class="sxs-lookup"><span data-stu-id="e51e5-139">Fix for issue 10634 : Fix the null Object reference for remove eventhubnamespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="e51e5-140">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="e51e5-140">Az.HDInsight</span></span>
* <span data-ttu-id="e51e5-141">Invoke-AzHDInsightHiveJob.md 오류를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-141">Fix Invoke-AzHDInsightHiveJob.md error.</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="e51e5-142">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="e51e5-142">Az.MachineLearning</span></span>
* <span data-ttu-id="e51e5-143">MachineLearningCompute를 더 이상 사용할 수 없게 되어 아래 cmdlet이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-143">Removed below cmdlets because MachineLearningCompute is not available any longer</span></span>
  - <span data-ttu-id="e51e5-144">Get-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="e51e5-144">Get-AzMlOpCluster</span></span>
  - <span data-ttu-id="e51e5-145">Get-AzMlOpClusterKey</span><span class="sxs-lookup"><span data-stu-id="e51e5-145">Get-AzMlOpClusterKey</span></span>
  - <span data-ttu-id="e51e5-146">New-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="e51e5-146">New-AzMlOpCluster</span></span>
  - <span data-ttu-id="e51e5-147">Remove-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="e51e5-147">Remove-AzMlOpCluster</span></span>
  - <span data-ttu-id="e51e5-148">Set-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="e51e5-148">Set-AzMlOpCluster</span></span>
  - <span data-ttu-id="e51e5-149">Test-AzMlOpClusterSystemServicesUpdateAvailability</span><span class="sxs-lookup"><span data-stu-id="e51e5-149">Test-AzMlOpClusterSystemServicesUpdateAvailability</span></span>
  - <span data-ttu-id="e51e5-150">Update-AzMlOpClusterSystemService</span><span class="sxs-lookup"><span data-stu-id="e51e5-150">Update-AzMlOpClusterSystemService</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e51e5-151">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e51e5-151">Az.Network</span></span>
* <span data-ttu-id="e51e5-152">Microsoft.Azure.Management.Sql의 종속성을 1.36-preview에서 1.37-preview로 업그레이드</span><span class="sxs-lookup"><span data-stu-id="e51e5-152">Upgrade dependancy of Microsoft.Azure.Management.Sql from 1.36-preivew to 1.37-preivew</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="e51e5-153">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="e51e5-153">Az.RecoveryServices</span></span>
* <span data-ttu-id="e51e5-154">Azure Site Recovery는 Azure 간 공급자를 위해 고객 관리 키와 함께 유휴 상태에서 암호화된 관리 디스크 vms를 위해 변경 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-154">Azure Site Recovery change support for managed disk vms encrypted at rest with customer managed leys for Azure to Azure provider.</span></span>
* <span data-ttu-id="e51e5-155">Azure Site Recovery는 VMware에서 Azure로를 위해 보호를 사용할 때 선택적 입력으로서 디스크 암호화 집합 ID를 입력하도록 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-155">Azure Site Recovery support to input disk encryption Set Id as optional input at enabling protection for Vmware to Azure.</span></span>
* <span data-ttu-id="e51e5-156">Azure Site Recovery는 VMware에서 Azure로를 위해 보호를 사용하기 위해 디스크 수준의 선택적 입력으로서 디스크 암호화 집합 ID를 입력하도록 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-156">Azure Site Recovery support to input disk encryption Set Id as optional input at disk level to enable protection for Vmware to Azure.</span></span>
* <span data-ttu-id="e51e5-157">Azure Site Recovery는 HyperV에서 Azure로를 위해 디스크 암호화 집합 맵을 사용하여 복제 보호된 항목을 업데이트하도록 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-157">Azure Site Recovery support to update replication protected item with disk encryption set Map for HyperV to Azure.</span></span>

#### <a name="azresources"></a><span data-ttu-id="e51e5-158">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e51e5-158">Az.Resources</span></span>
* <span data-ttu-id="e51e5-159">'Remove-AzTag'의 도움말 문서에서 오류를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-159">Fix an error in help document of 'Remove-AzTag'.</span></span>

#### <a name="azsql"></a><span data-ttu-id="e51e5-160">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e51e5-160">Az.Sql</span></span>
* <span data-ttu-id="e51e5-161">Azure Database의 마스터 DB에서 작동하도록 취약성 평가 세트 기준 cmdlet 기능을 수정하고 관리형 인스턴스 시스템 데이터베이스에서 이를 제한합니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-161">Fix vulnerability assessment set baseline cmdlets functionality to work on master db for azure database and limit it on managed instance system databases.</span></span>
* <span data-ttu-id="e51e5-162">SQL 인스턴스 장애 조치(failover) 그룹을 만들 때 오류 수정</span><span class="sxs-lookup"><span data-stu-id="e51e5-162">Fix an error when creating SQL instance failover group</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="e51e5-163">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="e51e5-163">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="e51e5-164">올바른 새 라이선스 형식으로 DR 추가</span><span class="sxs-lookup"><span data-stu-id="e51e5-164">Add DR as a new valid License type</span></span>

#### <a name="azstorage"></a><span data-ttu-id="e51e5-165">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="e51e5-165">Az.Storage</span></span>
* <span data-ttu-id="e51e5-166">다음 릴리스에서 DefaultAction Value 변경에 대해 호환성이 손상되는 변경 경고 메시지 추가</span><span class="sxs-lookup"><span data-stu-id="e51e5-166">Add breaking change warning message for DefaultAction Value change in a future release</span></span>
    - <span data-ttu-id="e51e5-167">Update-AzStorageAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="e51e5-167">Update-AzStorageAccountNetworkRuleSet</span></span>
* <span data-ttu-id="e51e5-168">-IncludeGeoReplicationStats 매개 변수와 함께 get-AzureRMStorageAccount를 실행하여 스토리지 계정의 마지막 동기화 시간 가져오기 지원</span><span class="sxs-lookup"><span data-stu-id="e51e5-168">Support Get last sync time of Storage account by run get-AzureRMStorageAccount with parameter -IncludeGeoReplicationStats</span></span> 
    - <span data-ttu-id="e51e5-169">Get-AzureRMStorageAccount</span><span class="sxs-lookup"><span data-stu-id="e51e5-169">Get-AzureRMStorageAccount</span></span>

## <a name="320---december-2019"></a><span data-ttu-id="e51e5-170">3.2.0 - 2019년 12월</span><span class="sxs-lookup"><span data-stu-id="e51e5-170">3.2.0 - December 2019</span></span>

### <a name="general"></a><span data-ttu-id="e51e5-171">일반</span><span class="sxs-lookup"><span data-stu-id="e51e5-171">General</span></span>
* <span data-ttu-id="e51e5-172">모든 모듈의 상대 경로를 사용하기 위해 .psd1의 참조 업데이트</span><span class="sxs-lookup"><span data-stu-id="e51e5-172">Update references in .psd1 to use relative path for all modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="e51e5-173">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e51e5-173">Az.Accounts</span></span>
* <span data-ttu-id="e51e5-174">Az 4.0 미리 보기를 위해 클라이언트 측 원격 분석에 대해 UserAgent를 올바르게 설정</span><span class="sxs-lookup"><span data-stu-id="e51e5-174">Set correct UserAgent for client-side telemetry for Az 4.0 preview</span></span>
* <span data-ttu-id="e51e5-175">Az 4.0 미리 보기에서 컨텍스트가 null인 경우 사용자에게 친숙한 오류 메시지로 표시</span><span class="sxs-lookup"><span data-stu-id="e51e5-175">Display user friendly error message when context is null in Az 4.0 preview</span></span>

#### <a name="azbatch"></a><span data-ttu-id="e51e5-176">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="e51e5-176">Az.Batch</span></span>
* <span data-ttu-id="e51e5-177">**New-AzBatchPool**이 'VirtualMachineConfiguration.ContainerConfiguration' 또는 'VirtualMachineConfiguration.DataDisks'를 서버로 제대로 보내지 않는 [#10602](https://github.com/Azure/azure-powershell/issues/10602) 문제 수정</span><span class="sxs-lookup"><span data-stu-id="e51e5-177">Fix issue [#10602](https://github.com/Azure/azure-powershell/issues/10602), where **New-AzBatchPool** did not properly send 'VirtualMachineConfiguration.ContainerConfiguration' or 'VirtualMachineConfiguration.DataDisks' to the server.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="e51e5-178">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="e51e5-178">Az.DataFactory</span></span>
* <span data-ttu-id="e51e5-179">ADF .Net SDK 버전을 4.5.0으로 업데이트</span><span class="sxs-lookup"><span data-stu-id="e51e5-179">Update ADF .Net SDK version to 4.5.0</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="e51e5-180">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="e51e5-180">Az.FrontDoor</span></span>
* <span data-ttu-id="e51e5-181">WAF 관리 규칙 제외 지원 추가됨</span><span class="sxs-lookup"><span data-stu-id="e51e5-181">Added WAF managed rules exclusion support</span></span>
* <span data-ttu-id="e51e5-182">자동 완성에 SocketAddr 추가</span><span class="sxs-lookup"><span data-stu-id="e51e5-182">Add SocketAddr to auto-complete</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="e51e5-183">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="e51e5-183">Az.HealthcareApis</span></span>
* <span data-ttu-id="e51e5-184">예외 처리</span><span class="sxs-lookup"><span data-stu-id="e51e5-184">Exception Handling</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="e51e5-185">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="e51e5-185">Az.KeyVault</span></span>
* <span data-ttu-id="e51e5-186">잠재적으로 설정되지 않은 오류 액세스 값 수정</span><span class="sxs-lookup"><span data-stu-id="e51e5-186">Fixed error accessing value that is potentially not set</span></span>
* <span data-ttu-id="e51e5-187">타원 곡선 암호화 인증서 관리</span><span class="sxs-lookup"><span data-stu-id="e51e5-187">Elliptic Curve Cryptography Certificate Managment</span></span>
    - <span data-ttu-id="e51e5-188">인증서 정책에 대한 곡선 지정을 위한 지원 추가됨</span><span class="sxs-lookup"><span data-stu-id="e51e5-188">Added support to specify the Curve for Certificate Policies</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="e51e5-189">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="e51e5-189">Az.Monitor</span></span>
* <span data-ttu-id="e51e5-190">진단 설정 추가 명령에 선택적 인수 추가</span><span class="sxs-lookup"><span data-stu-id="e51e5-190">Adding optional argument to the Add Diagnostic Settings command.</span></span> <span data-ttu-id="e51e5-191">스위치 인수(있는 경우)는 Log Analytics로 내보내기가 고정 스키마(전용 데이터 유형)가 되어야 함을</span><span class="sxs-lookup"><span data-stu-id="e51e5-191">A switch argument that if present indicates that the export to Log Analytics must be to a fixed schema (a.k.a.</span></span> <span data-ttu-id="e51e5-192">나타냄</span><span class="sxs-lookup"><span data-stu-id="e51e5-192">dedicated, data type)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e51e5-193">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e51e5-193">Az.Network</span></span>
* <span data-ttu-id="e51e5-194">AzureFirewall 애플리케이션, NAT 및 네트워크 규칙에서 IpGroups 지원.</span><span class="sxs-lookup"><span data-stu-id="e51e5-194">Support for IpGroups in AzureFirewall Application,Nat & Network Rules.</span></span>

#### <a name="azresources"></a><span data-ttu-id="e51e5-195">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e51e5-195">Az.Resources</span></span>
* <span data-ttu-id="e51e5-196">이름이 일부 내장 매개 변수 이름과 충돌하는 경우 템플릿 배포가 템플릿 매개 변수를 읽지 못하는 문제 수정.</span><span class="sxs-lookup"><span data-stu-id="e51e5-196">Fix an issue where template deployment fails to read a template parameter if its name conflicts with some built-in parameter name.</span></span>
* <span data-ttu-id="e51e5-197">정책 세트 정의 내에 그룹화 지원을 도입하는 새로운 API 버전 2019-09-01을 사용하도록 정책 cmdlet 업데이트.</span><span class="sxs-lookup"><span data-stu-id="e51e5-197">Updated policy cmdlets to use new api version 2019-09-01 that introduces grouping support within policy set definitions.</span></span>

#### <a name="azsql"></a><span data-ttu-id="e51e5-198">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e51e5-198">Az.Sql</span></span>
* <span data-ttu-id="e51e5-199">취약성 평가 자동 활성화에서 스토리지 생성을 StorageV2로 업그레이드</span><span class="sxs-lookup"><span data-stu-id="e51e5-199">Upgraded storage creation in Vulnerability Assessment auto enablement to StorageV2</span></span>

#### <a name="azstorage"></a><span data-ttu-id="e51e5-200">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="e51e5-200">Az.Storage</span></span>
* <span data-ttu-id="e51e5-201">Oauth 인증을 기반으로 스토리지 컨텍스트를 사용하여 Blob/컨테이너 ID 기반 SAS 토큰 생성 지원</span><span class="sxs-lookup"><span data-stu-id="e51e5-201">Support generate Blob/Constainer Idenity based SAS token with Storage Context based on Oauth authentication</span></span>
    - <span data-ttu-id="e51e5-202">New-AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="e51e5-202">New-AzStorageContainerSASToken</span></span>
    - <span data-ttu-id="e51e5-203">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="e51e5-203">New-AzStorageBlobSASToken</span></span>
* <span data-ttu-id="e51e5-204">모든 Idenity SAS 토큰을 해지할 수 있도록 스토리지 계정 사용자 위임 키 해지 지원</span><span class="sxs-lookup"><span data-stu-id="e51e5-204">Support revoke Storage Account User Delegation Keys, so all Idenity SAS tokens are revoked</span></span>
    - <span data-ttu-id="e51e5-205">Revoke-AzStorageAccountUserDelegationKeys</span><span class="sxs-lookup"><span data-stu-id="e51e5-205">Revoke-AzStorageAccountUserDelegationKeys</span></span>
* <span data-ttu-id="e51e5-206">새로운 API 버전 2019-06-01을 지원하기 위해 Microsoft.Azure.Management.Storage 14.2.0으로 업그레이드.</span><span class="sxs-lookup"><span data-stu-id="e51e5-206">Upgrade to Microsoft.Azure.Management.Storage 14.2.0, to support new API version 2019-06-01.</span></span>
* <span data-ttu-id="e51e5-207">File Share cmdlet의 관리 평면에서 5120을 초과하는 값에 대해 QuotaGiB(Gibyby의 공유 할당량)를 지원하고 'Quota' 매개 변수 별칭을 'QuotaGiB' 매개 변수에 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-207">Support of QuotaGiB (Share Quota in Gibibye) for values of more than 5120 in the Management plane of File Share cmdlets and added the 'Quota' parameter alias to the 'QuotaGiB' parameter.</span></span> 
    - <span data-ttu-id="e51e5-208">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="e51e5-208">New-AzRmStorageShare</span></span>
    - <span data-ttu-id="e51e5-209">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="e51e5-209">Update-AzRmStorageShare</span></span>
* <span data-ttu-id="e51e5-210">매개 변수 'Quota'에 매개 변수 별칭 'QuotaGiB' 추가</span><span class="sxs-lookup"><span data-stu-id="e51e5-210">Add parameter alias 'QuotaGiB' to parameter 'Quota'</span></span>
    - <span data-ttu-id="e51e5-211">Set-AzStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="e51e5-211">Set-AzStorageShareQuota</span></span>
* <span data-ttu-id="e51e5-212">Set-AzStorageContainerAcl가 저장된 액세스 정책을 정리할 수 있는 문제 수정</span><span class="sxs-lookup"><span data-stu-id="e51e5-212">Fix the issue that Set-AzStorageContainerAcl can clean up the stored Access Policy</span></span>
    - <span data-ttu-id="e51e5-213">Set-AzStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="e51e5-213">Set-AzStorageContainerAcl</span></span>

## <a name="310---november-2019"></a><span data-ttu-id="e51e5-214">3.1.0 - 2019년 11월</span><span class="sxs-lookup"><span data-stu-id="e51e5-214">3.1.0 - November 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="e51e5-215">마지막 주 릴리스 이후의 주요 사항</span><span class="sxs-lookup"><span data-stu-id="e51e5-215">Highlights since the last major release</span></span>
* <span data-ttu-id="e51e5-216">Az.DataBoxEdge 1.0.0 릴리스됨</span><span class="sxs-lookup"><span data-stu-id="e51e5-216">Az.DataBoxEdge 1.0.0 released</span></span>
* <span data-ttu-id="e51e5-217">Az.SqlVirtualMachine 1.0.0 릴리스됨</span><span class="sxs-lookup"><span data-stu-id="e51e5-217">Az.SqlVirtualMachine 1.0.0 released</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e51e5-218">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e51e5-218">Az.Compute</span></span>
* <span data-ttu-id="e51e5-219">VM Reapply 기능</span><span class="sxs-lookup"><span data-stu-id="e51e5-219">VM Reapply feature</span></span>
    - <span data-ttu-id="e51e5-220">Set-AzVM cmdlet에 Reapply 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="e51e5-220">Add Reapply parameter to Set-AzVM cmdlet</span></span>
* <span data-ttu-id="e51e5-221">VM 확장 집합 AutomaticRepairs 기능:</span><span class="sxs-lookup"><span data-stu-id="e51e5-221">VM Scale Set AutomaticRepairs feature:</span></span>
    - <span data-ttu-id="e51e5-222">다음 cmdlet에 EnableAutomaticRepair, AutomaticRepairGracePeriod 및 AutomaticRepairMaxInstanceRepairsPercent 매개 변수를 추가합니다.   New-AzVmssConfig   Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="e51e5-222">Add EnableAutomaticRepair, AutomaticRepairGracePeriod, and AutomaticRepairMaxInstanceRepairsPercent parameters to the following cmdlets:   New-AzVmssConfig   Update-AzVmss</span></span>
* <span data-ttu-id="e51e5-223">New-AzVM에 대한 교차 테넌트 갤러리 이미지 지원</span><span class="sxs-lookup"><span data-stu-id="e51e5-223">Cross tenant gallery image support for New-AzVM</span></span>
* <span data-ttu-id="e51e5-224">New-AzVM, New-AzVMConfig 및 New-AzVmss cmdlet의 Priority 매개 변수의 인수 완성자에 'Spot' 추가</span><span class="sxs-lookup"><span data-stu-id="e51e5-224">Add 'Spot' to the argument completer of Priority parameter in New-AzVM, New-AzVMConfig and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="e51e5-225">Add-AzVmssDataDisk cmdlet에 DiskIOPSReadWrite 및 DiskMBpsReadWrite 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="e51e5-225">Add DiskIOPSReadWrite and DiskMBpsReadWrite parameters to Add-AzVmssDataDisk cmdlet</span></span>
* <span data-ttu-id="e51e5-226">New-AzGalleryImageVersion cmdlet의 SourceImageId 매개 변수를 선택 사항으로 변경</span><span class="sxs-lookup"><span data-stu-id="e51e5-226">Change SourceImageId parameter of New-AzGalleryImageVersion cmdlet to optional</span></span>
* <span data-ttu-id="e51e5-227">New-AzGalleryImageVersion cmdlet에 OSDiskImage 및 DataDiskImage 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="e51e5-227">Add OSDiskImage and DataDiskImage parameters to New-AzGalleryImageVersion cmdlet</span></span>
* <span data-ttu-id="e51e5-228">New-AzGalleryImageDefinition cmdlet에 HyperVGeneration 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="e51e5-228">Add HyperVGeneration parameter to New-AzGalleryImageDefinition cmdlet</span></span>
* <span data-ttu-id="e51e5-229">New-AzVmss, New-AzVmssConfig 및 Update-AzVmss cmdlet에 SkipExtensionsOnOverprovisionedVMs 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="e51e5-229">Add SkipExtensionsOnOverprovisionedVMs parameters to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="e51e5-230">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="e51e5-230">Az.DataBoxEdge</span></span>
* <span data-ttu-id="e51e5-231">cmdlet `Get-AzDataBoxEdgeOrder` 추가됨</span><span class="sxs-lookup"><span data-stu-id="e51e5-231">Added cmdlet `Get-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="e51e5-232">주문 가져오기</span><span class="sxs-lookup"><span data-stu-id="e51e5-232">Get the Order</span></span>
* <span data-ttu-id="e51e5-233">cmdlet `New-AzDataBoxEdgeOrder` 추가됨</span><span class="sxs-lookup"><span data-stu-id="e51e5-233">Added cmdlet `New-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="e51e5-234">새 주문 만들기</span><span class="sxs-lookup"><span data-stu-id="e51e5-234">Create new Order</span></span>
* <span data-ttu-id="e51e5-235">cmdlet `Remove-AzDataBoxEdgeOrder` 추가됨</span><span class="sxs-lookup"><span data-stu-id="e51e5-235">Added cmdlet `Remove-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="e51e5-236">주문 제거</span><span class="sxs-lookup"><span data-stu-id="e51e5-236">Remove the Order</span></span>
* <span data-ttu-id="e51e5-237">cmdlet `New-AzDataBoxEdgeShare` 변경</span><span class="sxs-lookup"><span data-stu-id="e51e5-237">Change in cmdlet `New-AzDataBoxEdgeShare`</span></span>
    - <span data-ttu-id="e51e5-238">이제 로컬 공유를 만듬</span><span class="sxs-lookup"><span data-stu-id="e51e5-238">Now creates Local Share</span></span>
* <span data-ttu-id="e51e5-239">cmdlet `Set-AzDataBoxEdgeRole` 추가됨</span><span class="sxs-lookup"><span data-stu-id="e51e5-239">Added cmdlet `Set-AzDataBoxEdgeRole`</span></span>
    - <span data-ttu-id="e51e5-240">이제 IotRole을 공유에 매핑할 수 있음</span><span class="sxs-lookup"><span data-stu-id="e51e5-240">Now IotRole can be mapped to Share</span></span>
* <span data-ttu-id="e51e5-241">cmdlet `Invoke-AzDataBoxEdgeDevice` 추가됨</span><span class="sxs-lookup"><span data-stu-id="e51e5-241">Added cmdlet `Invoke-AzDataBoxEdgeDevice`</span></span>
    - <span data-ttu-id="e51e5-242">스캔 업데이트 호출, 업데이트 다운로드, 디바이스에 업데이트 설치</span><span class="sxs-lookup"><span data-stu-id="e51e5-242">Invoke scan update, download update, install updates on the device</span></span>
* <span data-ttu-id="e51e5-243">cmdlet `Get-AzDataBoxEdgeTrigger` 추가됨</span><span class="sxs-lookup"><span data-stu-id="e51e5-243">Added cmdlet `Get-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="e51e5-244">트리거에 대한 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="e51e5-244">Gets the information about Triggers</span></span>
* <span data-ttu-id="e51e5-245">cmdlet `New-AzDataBoxEdgeTrigger` 추가됨</span><span class="sxs-lookup"><span data-stu-id="e51e5-245">Added cmdlet `New-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="e51e5-246">새 트리거 만들기</span><span class="sxs-lookup"><span data-stu-id="e51e5-246">Create new Triggers</span></span>
* <span data-ttu-id="e51e5-247">cmdlet `Remove-AzDataBoxEdgeTrigger` 추가됨</span><span class="sxs-lookup"><span data-stu-id="e51e5-247">Added cmdlet `Remove-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="e51e5-248">트리거 제거</span><span class="sxs-lookup"><span data-stu-id="e51e5-248">Remove the Triggers</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="e51e5-249">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="e51e5-249">Az.DataFactory</span></span>
* <span data-ttu-id="e51e5-250">ADF .Net SDK 버전을 4.4.0으로 업데이트</span><span class="sxs-lookup"><span data-stu-id="e51e5-250">Update ADF .Net SDK version to 4.4.0</span></span>
* <span data-ttu-id="e51e5-251">'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd에 'ExpressCustomSetup' 매개 변수를 추가하여 사용자 지정 설치 스크립트 없이 설치 구성 및 타사 구성 요소를 사용하도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-251">Add parameter 'ExpressCustomSetup' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable setup configurations and 3rd party components without custom setup script.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="e51e5-252">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="e51e5-252">Az.DataLakeStore</span></span>
* <span data-ttu-id="e51e5-253">Get-AzDataLakeStoreDeletedItem 및 Restore-AzDataLakeStoreDeletedItem의 설명서 업데이트</span><span class="sxs-lookup"><span data-stu-id="e51e5-253">Update documentation of Get-AzDataLakeStoreDeletedItem and Restore-AzDataLakeStoreDeletedItem</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="e51e5-254">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="e51e5-254">Az.EventHub</span></span>
* <span data-ttu-id="e51e5-255">10301 문제 해결: SAS 토큰 날짜 형식 수정</span><span class="sxs-lookup"><span data-stu-id="e51e5-255">Fix for issue 10301 : Fix the SAS Token date format</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="e51e5-256">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="e51e5-256">Az.FrontDoor</span></span>
* <span data-ttu-id="e51e5-257">Enable-AzFrontDoorCustomDomainHttps 및 New-AzFrontDoorFrontendEndpointObject에 MinimumTlsVersion 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="e51e5-257">Add MinimumTlsVersion parameter to Enable-AzFrontDoorCustomDomainHttps and New-AzFrontDoorFrontendEndpointObject</span></span>
* <span data-ttu-id="e51e5-258">New-AzFrontDoorHealthProbeSettingObject에 HealthProbeMethod 및 EnabledState 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="e51e5-258">Add HealthProbeMethod and EnabledState parameters to New-AzFrontDoorHealthProbeSettingObject</span></span>
* <span data-ttu-id="e51e5-259">BackendPoolsSettings 개체를 생성하여 Front Door 생성/업데이트에 전달하는 새 cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="e51e5-259">Add new cmdlet to create BackendPoolsSettings objec to pass into creation/update of Front Door</span></span>
    - <span data-ttu-id="e51e5-260">New-AzFrontDoorBackendPoolsSettingObject</span><span class="sxs-lookup"><span data-stu-id="e51e5-260">New-AzFrontDoorBackendPoolsSettingObject</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e51e5-261">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e51e5-261">Az.Network</span></span>
* <span data-ttu-id="e51e5-262">'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' 및 'Start-AzVirtualnetworkGatewayPacketCapture.md' FilterData 옵션 예제를 변경합니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-262">Change 'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' and 'Start-AzVirtualnetworkGatewayPacketCapture.md' FilterData option examples.</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="e51e5-263">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="e51e5-263">Az.PrivateDns</span></span>
* <span data-ttu-id="e51e5-264">PrivateDns .net sdk를 버전 1.0.0으로 업데이트함</span><span class="sxs-lookup"><span data-stu-id="e51e5-264">Updated PrivateDns .net sdk to version 1.0.0</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="e51e5-265">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="e51e5-265">Az.RecoveryServices</span></span>
* <span data-ttu-id="e51e5-266">보호를 사용하도록 설정할 때 디스크 유형을 선택하도록 Azure Site Recovery 지원</span><span class="sxs-lookup"><span data-stu-id="e51e5-266">Azure Site Recovery support to select disk type at enabling protection.</span></span>
* <span data-ttu-id="e51e5-267">복구 계획 동작 편집을 위한 Azure Site Recovery 버그 수정</span><span class="sxs-lookup"><span data-stu-id="e51e5-267">Azure Site Recovery bug fix for recovery plan action edit.</span></span>
* <span data-ttu-id="e51e5-268">파일 스트림 DB를 허용하도록 Azure Backup SQL 복원 지원</span><span class="sxs-lookup"><span data-stu-id="e51e5-268">Azure Backup SQL Restore support to accept filestream DBs.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="e51e5-269">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="e51e5-269">Az.RedisCache</span></span>
* <span data-ttu-id="e51e5-270">'New-AzRedisCache' 및 'Set-AzRedisCache' cmdlet에 'MinimumTlsVersion' 매개 변수가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-270">Added 'MinimumTlsVersion' parameter in 'New-AzRedisCache' and 'Set-AzRedisCache' cmdlets.</span></span> <span data-ttu-id="e51e5-271">'Get-AzRedisCache' cmdlet 출력에 'MinimumTlsVersion'도 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-271">Also, added 'MinimumTlsVersion' in the output of 'Get-AzRedisCache' cmdlet.</span></span>
* <span data-ttu-id="e51e5-272">'Set-AzRedisCache' 및 'New-AzRedisCache' cmdlet의 '-Size' 매개 변수에 대한 유효성 검사가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-272">Added validation on '-Size' parameter for 'Set-AzRedisCache' and 'New-AzRedisCache' cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="e51e5-273">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e51e5-273">Az.Resources</span></span>
- <span data-ttu-id="e51e5-274">정책 할당에 새로운 EnforcementMode 속성이 있는 새 api 버전 2019-06-01을 사용하도록 정책 cmdlet이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-274">Updated policy cmdlets to use new api version 2019-06-01 that has new EnforcementMode property in policy assignment.</span></span>
- <span data-ttu-id="e51e5-275">정책 정의 만들기 도움말 예제가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-275">Updated create policy definition help example</span></span>
- <span data-ttu-id="e51e5-276">Remove-AZADServicePrincipal -ServicePrincipalName 버그를 수정하고, 서비스 사용자 이름을 찾을 수 없으면 null 참조를 throw합니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-276">Fix bug Remove-AZADServicePrincipal -ServicePrincipalName, throw null reference when service principal name not found.</span></span>
- <span data-ttu-id="e51e5-277">New-AZADServicePrincipal 버그를 수정하고, 테넌트에 구독이 없으면 null 참조를 throw합니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-277">Fix bug New-AZADServicePrincipal, throw null reference when tenant doesn't have any subscription.</span></span>
- <span data-ttu-id="e51e5-278">연결된 애플리케이션에만 자격 증명을 추가하도록 New-AzAdServicePrincipal을 변경합니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-278">Change New-AzAdServicePrincipal to add credentials only to associated application.</span></span>

#### <a name="azsql"></a><span data-ttu-id="e51e5-279">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e51e5-279">Az.Sql</span></span>
* <span data-ttu-id="e51e5-280">데이터베이스 ReadReplicaCount에 대한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-280">Added support for database ReadReplicaCount.</span></span>
* <span data-ttu-id="e51e5-281">영역 중복이 설정되지 않은 경우 Set-AzSqlDatabase가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-281">Fixed Set-AzSqlDatabase when zone redundancy not set</span></span>

## <a name="300---november-2019"></a><span data-ttu-id="e51e5-282">3.0.0 - 2019년 11월</span><span class="sxs-lookup"><span data-stu-id="e51e5-282">3.0.0 - November 2019</span></span>
### <a name="general"></a><span data-ttu-id="e51e5-283">일반</span><span class="sxs-lookup"><span data-stu-id="e51e5-283">General</span></span>
* <span data-ttu-id="e51e5-284">Az.PrivateDns 1.0.0 릴리스</span><span class="sxs-lookup"><span data-stu-id="e51e5-284">Az.PrivateDns 1.0.0 released</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="e51e5-285">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e51e5-285">Az.Accounts</span></span>
* <span data-ttu-id="e51e5-286">'Resolve-Error' 별칭에 사용 중단 메시지를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-286">Add a deprecation message for 'Resolve-Error' alias.</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="e51e5-287">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="e51e5-287">Az.Advisor</span></span>
* <span data-ttu-id="e51e5-288">Get-AzAdvisorRecommendation cmdlet에 새로운 '운영 효율성' 범주가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-288">Added new category 'Operational Excellence' to Get-AzAdvisorRecommendation cmdlet.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="e51e5-289">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="e51e5-289">Az.Batch</span></span>
* <span data-ttu-id="e51e5-290">`BatchAccountContext`의 `CoreQuota` 이름이 `DedicatedCoreQuota`로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-290">Renamed `CoreQuota` on `BatchAccountContext` to `DedicatedCoreQuota`.</span></span> <span data-ttu-id="e51e5-291">또한 `LowPriorityCoreQuota`가 새로 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-291">There is also a new `LowPriorityCoreQuota`.</span></span>
  - <span data-ttu-id="e51e5-292">이 변경 사항은 **Get-AzBatchAccount**에 영향을 줍니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-292">This impacts **Get-AzBatchAccount**.</span></span>
* <span data-ttu-id="e51e5-293">이제 **New-AzBatchTask** `-ResourceFile` 매개 변수는 새로운 **New-AzBatchResourceFile** cmdlet을 사용하여 구성할 수 있는 `PSResourceFile` 개체의 컬렉션을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-293">**New-AzBatchTask** `-ResourceFile` parameter now takes a collection of `PSResourceFile` objects, which can be constructed using the new **New-AzBatchResourceFile** cmdlet.</span></span>
* <span data-ttu-id="e51e5-294">새로운 **New-AzBatchResourceFile** cmdlet을 통해 `PSResourceFile` 개체를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-294">New **New-AzBatchResourceFile** cmdlet to help create `PSResourceFile` objects.</span></span> <span data-ttu-id="e51e5-295">이들은 `-ResourceFile` 매개 변수의 **New-AzBatchTask**에 제공될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-295">These can be supplied to **New-AzBatchTask** on the `-ResourceFile` parameter.</span></span>
  - <span data-ttu-id="e51e5-296">그에 따라 기존 `HttpUrl` 방법 외에도 두 가지 종류의 리소스 파일이 새롭게 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-296">This supports two new kinds of resource file in addition to the existing `HttpUrl` way:</span></span>
    - <span data-ttu-id="e51e5-297">`AutoStorageContainerName` 기반 리소스 파일은 전체 자동 스토리지 컨테이너를 일괄 처리 노드에 다운로드합니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-297">`AutoStorageContainerName` based resource files download an entire auto-storage container to the Batch node.</span></span>
    - <span data-ttu-id="e51e5-298">`StorageContainerUrl` 기반 리소스 파일은 URL에 지정된 컨테이너를 일괄 처리 노드에 다운로드합니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-298">`StorageContainerUrl` based resource files download the container specified in the URL to the Batch node.</span></span>
* <span data-ttu-id="e51e5-299">**Get-AzBatchApplication**으로 반환되는 `PSApplication`의 `ApplicationPackages` 속성이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-299">Removed `ApplicationPackages` property of `PSApplication` returned by **Get-AzBatchApplication**.</span></span>
  - <span data-ttu-id="e51e5-300">이제 **Get-AzBatchApplicationPackage**를 사용하여 애플리케이션 내부의 특정 패키지를 검색할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-300">The specific packages inside of an application now can be retrieved using **Get-AzBatchApplicationPackage**.</span></span> <span data-ttu-id="e51e5-301">예: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`</span><span class="sxs-lookup"><span data-stu-id="e51e5-301">For example: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span></span>
* <span data-ttu-id="e51e5-302">**Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication** 및 **Set-AzBatchApplication**에서 `ApplicationId` 이름이 `ApplicationName`으로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-302">Renamed `ApplicationId` to `ApplicationName` on **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication**, and **Set-AzBatchApplication**.</span></span>
  - <span data-ttu-id="e51e5-303">이제 `ApplicationId`는 `ApplicationName`의 별칭입니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-303">`ApplicationId` now is an alias of `ApplicationName`.</span></span>
* <span data-ttu-id="e51e5-304">새로운 `PSWindowsUserConfiguration` 속성이 `PSUserAccount`에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-304">Added new `PSWindowsUserConfiguration` property to `PSUserAccount`.</span></span>
* <span data-ttu-id="e51e5-305">`PSApplicationPackage`에서 `Version` 이름이 `Name`으로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-305">Renamed `Version` to `Name` on `PSApplicationPackage`.</span></span>
* <span data-ttu-id="e51e5-306">`PSResourceFile`에서 `BlobSource` 이름이 `HttpUrl`으로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-306">Renamed `BlobSource` to `HttpUrl` on `PSResourceFile`.</span></span>
* <span data-ttu-id="e51e5-307">`PSVirtualMachineConfiguration`에서 `OSDisk` 속성이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-307">Removed `OSDisk` property from `PSVirtualMachineConfiguration`.</span></span>
* <span data-ttu-id="e51e5-308">**Set-AzBatchPoolOSVersion**이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-308">Removed **Set-AzBatchPoolOSVersion**.</span></span> <span data-ttu-id="e51e5-309">이 작업은 더 이상 지원되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-309">This operation is no longer supported.</span></span>
* <span data-ttu-id="e51e5-310">`PSCloudServiceConfiguration`에서 `TargetOSVersion`이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-310">Removed `TargetOSVersion` from `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="e51e5-311">`PSCloudServiceConfiguration`에서 `CurrentOSVersion` 이름이 `OSVersion`으로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-311">Renamed `CurrentOSVersion` to `OSVersion` on `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="e51e5-312">`PSPoolUsageMetrics`에서 `DataEgressGiB` 및 `DataIngressGiB`가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-312">Removed `DataEgressGiB` and `DataIngressGiB` from `PSPoolUsageMetrics`.</span></span>
* <span data-ttu-id="e51e5-313">**Get-AzBatchNodeAgentSku**가 제거되고 **Get-AzBatchSupportedImage**로 대체되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-313">Removed **Get-AzBatchNodeAgentSku** and replaced it with  **Get-AzBatchSupportedImage**.</span></span> 
  - <span data-ttu-id="e51e5-314">**Get-AzBatchSupportedImage**가 **Get-AzBatchNodeAgentSku**와 동일한 데이터를 반환하지만 더 친숙한 형식이 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-314">**Get-AzBatchSupportedImage** returns the same data as **Get-AzBatchNodeAgentSku** but in a more friendly format.</span></span>
  - <span data-ttu-id="e51e5-315">이제 확인되지 않은 이미지도 새롭게 반환됩니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-315">New non-verified images are also now returned.</span></span> <span data-ttu-id="e51e5-316">각 이미지의 `Capabilities` 및 `BatchSupportEndOfLife`에 대한 추가 정보도 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-316">Additional information about `Capabilities` and `BatchSupportEndOfLife` for each image is also included.</span></span>
* <span data-ttu-id="e51e5-317">**New-AzBatchPool**의 새로운 `MountConfiguration` 매개 변수를 통해 풀의 각 노드에서 원격 파일 시스템을 마운트할 수 있는 기능이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-317">Added ability to mount remote file-systems on each node of a pool via the new `MountConfiguration` parameter of **New-AzBatchPool**.</span></span>
* <span data-ttu-id="e51e5-318">이제 트래픽의 소스 포트를 기준으로 풀에 대한 네트워크 액세스를 차단하는 네트워크 보안 규칙이 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-318">Now support network security rules blocking network access to a pool based on the source port of the traffic.</span></span> <span data-ttu-id="e51e5-319">이 작업은 `PSNetworkSecurityGroupRule`에서 `SourcePortRanges` 속성을 통해 수행됩니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-319">This is done via the `SourcePortRanges` property on `PSNetworkSecurityGroupRule`.</span></span>
* <span data-ttu-id="e51e5-320">컨테이너를 실행할 때 Batch는 이제 컨테이너 작업 디렉터리 또는 일괄 처리 태스크 작업 디렉터리에서 작업 실행을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-320">When running a container, Batch now supports executing the task in the container working directory or in the Batch task working directory.</span></span> <span data-ttu-id="e51e5-321">이 작업은 `PSTaskContainerSettings`에서 `WorkingDirectory` 속성에 의해 제어됩니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-321">This is controlled by the `WorkingDirectory` property on `PSTaskContainerSettings`.</span></span>
* <span data-ttu-id="e51e5-322">새로운 `PublicIPs` 속성을 통해 `PSNetworkConfiguration`에서 공용 IP의 컬렉션을 지정할 수 있는 기능이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-322">Added ability to specify a collection of public IPs on `PSNetworkConfiguration` via the new `PublicIPs` property.</span></span> <span data-ttu-id="e51e5-323">그 결과 사용자 제공 IP 목록의 IP가 풀에 있는 노드에 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-323">This guarantees nodes in the Pool will have an IP from the list user provided IPs.</span></span>
* <span data-ttu-id="e51e5-324">지정하지 않은 경우 이제 `PSSTartTask`에서 `WaitForSuccess`의 기본값은 `$True`입니다(이전에는 `$False`).</span><span class="sxs-lookup"><span data-stu-id="e51e5-324">When not specified, the default value of `WaitForSuccess` on `PSSTartTask` is now `$True` (was `$False`).</span></span>
* <span data-ttu-id="e51e5-325">지정하지 않은 경우 이제 `PSAutoUserSpecification`에서 `Scope`의 기본값은 `Pool`입니다(이전에는 Windows의 경우 `Task`, Linux의 경우에는 `Pool`).</span><span class="sxs-lookup"><span data-stu-id="e51e5-325">When not specified, the default value of `Scope` on `PSAutoUserSpecification` is now `Pool` (was `Task` on Windows and `Pool` on Linux).</span></span>

#### <a name="azcdn"></a><span data-ttu-id="e51e5-326">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="e51e5-326">Az.Cdn</span></span>
* <span data-ttu-id="e51e5-327">RulesEngine에 UrlRewriteAction 및 CacheKeyQueryStringAction이 도입되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-327">Introduced UrlRewriteAction and CacheKeyQueryStringAction to RulesEngine.</span></span>
* <span data-ttu-id="e51e5-328">New-AzDeliveryRuleCondition cmdlet에서 'Selector' 입력 누락과 같은 여러 버그가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-328">Fixed several bugs like missing 'Selector' Input in New-AzDeliveryRuleCondition cmdlet.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e51e5-329">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e51e5-329">Az.Compute</span></span>
* <span data-ttu-id="e51e5-330">디스크 암호화 집합 기능</span><span class="sxs-lookup"><span data-stu-id="e51e5-330">Disk Encryption Set feature</span></span>
    - <span data-ttu-id="e51e5-331">새 cmdlet:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="e51e5-331">New cmdlets:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span></span>
    - <span data-ttu-id="e51e5-332">DiskEncryptionSetId 매개 변수가 다음 cmdlet에 추가되었습니다. Set-AzImageOSDisk Set-AzVMOSDisk Set-AzVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="e51e5-332">DiskEncryptionSetId parameter is added to the following cmdlets: Set-AzImageOSDisk Set-AzVMOSDisk Set-AzVmssStorageProfile</span></span>        
        <span data-ttu-id="e51e5-333">Add-AzImageDataDisk New-AzVMDataDisk Set-AzVMDataDisk Add-AzVMDataDisk Add-AzVmssDataDisk Add-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="e51e5-333">Add-AzImageDataDisk New-AzVMDataDisk Set-AzVMDataDisk Add-AzVMDataDisk Add-AzVmssDataDisk Add-AzVmssVMDataDisk</span></span>
    - <span data-ttu-id="e51e5-334">DiskEncryptionSetId 및 EncryptionType 매개 변수가 다음 cmdlet에 추가되었습니다.   New-AzDiskConfig   New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="e51e5-334">DiskEncryptionSetId and EncryptionType parameters are added to the following cmdlets:   New-AzDiskConfig   New-AzSnapshotConfig</span></span>
* <span data-ttu-id="e51e5-335">New-AzVmssIPConfig에 PublicIPAddressVersion 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="e51e5-335">Add PublicIPAddressVersion parameter to New-AzVmssIPConfig</span></span>
* <span data-ttu-id="e51e5-336">사용자 지정 스크립트 확장의 FileUris를 공용 설정에서 보호된 설정으로 이동</span><span class="sxs-lookup"><span data-stu-id="e51e5-336">Move FileUris of custom script extension from public setting to protected setting</span></span>
* <span data-ttu-id="e51e5-337">New-AzVmss, New-AzVmssConfig 및 Update-AzVmss cmdlet에 ScaleInPolicy 추가</span><span class="sxs-lookup"><span data-stu-id="e51e5-337">Add ScaleInPolicy to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>
* <span data-ttu-id="e51e5-338">주요 변경 내용</span><span class="sxs-lookup"><span data-stu-id="e51e5-338">Breaking changes</span></span>
    - <span data-ttu-id="e51e5-339">CreateOption이 업로드일 때 UploadSizeInBytes 매개 변수가 New-AzDiskConfig에 대해 DiskSizeGB 대신 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-339">UploadSizeInBytes parameter is used instead of DiskSizeGB for New-AzDiskConfig when CreateOption is Upload</span></span>
    - <span data-ttu-id="e51e5-340">GalleryImageVersion 개체에서 PublishingProfile.Source.ManagedImage.Id가 StorageProfile.Source.Id로 바뀝니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-340">PublishingProfile.Source.ManagedImage.Id is replaced with StorageProfile.Source.Id in GalleryImageVersion object</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="e51e5-341">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="e51e5-341">Az.DataFactory</span></span>
* <span data-ttu-id="e51e5-342">ADF .Net SDK 버전을 4.3.0으로 업데이트</span><span class="sxs-lookup"><span data-stu-id="e51e5-342">Update ADF .Net SDK version to 4.3.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="e51e5-343">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="e51e5-343">Az.DataLakeStore</span></span>
* <span data-ttu-id="e51e5-344">ADLS SDK 버전 업데이트(https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha) , 다음 수정 사항 제공</span><span class="sxs-lookup"><span data-stu-id="e51e5-344">Update ADLS SDK version (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), brings following fixes</span></span>
* <span data-ttu-id="e51e5-345">휴지통 또는 디렉터리 항목의 creationtime을 역직렬화할 수 없을 때 예외가 발생하지 않도록 방지합니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-345">Avoid throwing exception while unable to deserialize the creationtime of the trash or directory entry.</span></span>
* <span data-ttu-id="e51e5-346">adlsclient에서 요청별 시간 제한 설정 노출</span><span class="sxs-lookup"><span data-stu-id="e51e5-346">Expose setting per request timeout in adlsclient</span></span>
* <span data-ttu-id="e51e5-347">badoffset 복구를 위한 원본 syncflag 전달 수정</span><span class="sxs-lookup"><span data-stu-id="e51e5-347">Fix passing the original syncflag for badoffset recovery</span></span>
* <span data-ttu-id="e51e5-348">응답이 확인된 후 연속 토큰을 검색하기 위한 EnumerateDirectory 수정</span><span class="sxs-lookup"><span data-stu-id="e51e5-348">Fix EnumerateDirectory to retrieve continuation token once response is checked</span></span>
* <span data-ttu-id="e51e5-349">Concat 버그 수정</span><span class="sxs-lookup"><span data-stu-id="e51e5-349">Fix Concat Bug</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="e51e5-350">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="e51e5-350">Az.FrontDoor</span></span>
* <span data-ttu-id="e51e5-351">모듈 간 기타 오타가 수정됨</span><span class="sxs-lookup"><span data-stu-id="e51e5-351">Fixed miscellaneous typos across module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="e51e5-352">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="e51e5-352">Az.HDInsight</span></span>
* <span data-ttu-id="e51e5-353">ADLSGen1 스토리지가 포함된 클러스터를 가져오기 위해 Get-AzHDInsightCluster를 사용할 때 고객에게 '올바른 Base-64 문자열이 아닙니다' 오류가 표시되는 버그가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-353">Fixed the bug that customer will get 'Not a valid Base-64 string' error when using Get-AzHDInsightCluster to get the cluster with ADLSGen1 storage.</span></span>
* <span data-ttu-id="e51e5-354">고객이 Azure Data Lake에 액세스하기 위해 서비스 주체 애플리케이션 ID를 제공할 수 있도록 세 가지 cmdlet Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig 및 New-AzHDInsightCluster에 이름이 'ApplicationId'인 매개 변수를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-354">Add a parameter named 'ApplicationId' to three cmdlets Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig and New-AzHDInsightCluster so that customer can provide the service principal application id for accessing Azure Data Lake.</span></span>
* <span data-ttu-id="e51e5-355">Microsoft.Azure.Management.HDInsight가 2.1.0에서 5.1.0으로 변경됨</span><span class="sxs-lookup"><span data-stu-id="e51e5-355">Changed Microsoft.Azure.Management.HDInsight from 2.1.0 to 5.1.0</span></span>
* <span data-ttu-id="e51e5-356">다음 5가지 cmdlet이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-356">Removed five cmdlets:</span></span>
    - <span data-ttu-id="e51e5-357">Get-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="e51e5-357">Get-AzHDInsightOMS</span></span>
    - <span data-ttu-id="e51e5-358">Enable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="e51e5-358">Enable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="e51e5-359">Disable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="e51e5-359">Disable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="e51e5-360">Grant-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="e51e5-360">Grant-AzHDInsightRdpServicesAccess</span></span>
    - <span data-ttu-id="e51e5-361">Revoke-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="e51e5-361">Revoke-AzHDInsightRdpServicesAccess</span></span>
* <span data-ttu-id="e51e5-362">다음 3가지 cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-362">Added three cmdlets:</span></span>
    - <span data-ttu-id="e51e5-363">Get-AzHDInsightOMS 대신 Get-AzHDInsightMonitoring</span><span class="sxs-lookup"><span data-stu-id="e51e5-363">Get-AzHDInsightMonitoring to replace Get-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="e51e5-364">Get-AzHDInsightOMS 대신 Get-AzHDInsightMonitoring</span><span class="sxs-lookup"><span data-stu-id="e51e5-364">Enable-AzHDInsightMonitoring to replace Enable-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="e51e5-365">Disable-AzHDInsightOMS 대신 Disable-AzHDInsightMonitoring</span><span class="sxs-lookup"><span data-stu-id="e51e5-365">Disable-AzHDInsightMonitoring to replace Disable-AzHDInsightOMS.</span></span>
* <span data-ttu-id="e51e5-366">특정 위치의 기능 정보 가져오기를 지원하도록 cmdlet Get-AzHDInsightProperties가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-366">Fixed cmdlet Get-AzHDInsightProperties to support get capabilities information from a specific location.</span></span>
* <span data-ttu-id="e51e5-367">Add-AzHDInsightConfigValue에서 매개 변수 집합('Spark1', 'Spark2')이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-367">Removed parameter sets('Spark1', 'Spark2') from Add-AzHDInsightConfigValue.</span></span>
* <span data-ttu-id="e51e5-368">cmdlet Add-AzHDInsightSecurityProfile의 도움말 문서에 예제를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-368">Add examples to the help documents of cmdlet Add-AzHDInsightSecurityProfile.</span></span>
* <span data-ttu-id="e51e5-369">다음 cmdlet의 출력 유형이 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-369">Changed output type of the following cmdlets:</span></span>
*  - <span data-ttu-id="e51e5-370">Get-AzHDInsightProperties의 출력 유형이 CapabilitiesResponse에서 AzureHDInsightCapabilities로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-370">Changed the output type of Get-AzHDInsightProperties from  CapabilitiesResponse to AzureHDInsightCapabilities.</span></span>
*  - <span data-ttu-id="e51e5-371">Remove-AzHDInsightCluster의 출력 유형이 ClusterGetResponse에서 bool로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-371">Changed the output type of Remove-AzHDInsightCluster from ClusterGetResponse to bool.</span></span>
*  - <span data-ttu-id="e51e5-372">Set-AzHDInsightGatewaySettings의 출력 유형이 HttpConnectivitySettings에서 GatewaySettings로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-372">Changed the output type of Set-AzHDInsightGatewaySettings HttpConnectivitySettings to GatewaySettings.</span></span>
* <span data-ttu-id="e51e5-373">몇 가지 시나리오 테스트 사례가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-373">Added some scenario test cases.</span></span>
* <span data-ttu-id="e51e5-374">일부 별칭 제거: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span><span class="sxs-lookup"><span data-stu-id="e51e5-374">Remove some alias: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="e51e5-375">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="e51e5-375">Az.IotHub</span></span>
* <span data-ttu-id="e51e5-376">주요 변경 내용:</span><span class="sxs-lookup"><span data-stu-id="e51e5-376">Breaking changes:</span></span>
    - <span data-ttu-id="e51e5-377">'Add-AzIotHubEventHubConsumerGroup' cmdlet이 'EventHubEndpointName' 매개 변수를 더 이상 지원하지 않으며 원래 매개 변수 이름에 대해 별칭을 찾을 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-377">The cmdlet 'Add-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="e51e5-378">'Add-AzIotHubEventHubConsumerGroup' cmdlet에 대한 매개 변수 집합 '__AllParameterSets'가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-378">The parameter set '__AllParameterSets' for cmdlet 'Add-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="e51e5-379">'Get-AzIotHubEventHubConsumerGroup' cmdlet이 'EventHubEndpointName' 매개 변수를 더 이상 지원하지 않으며 원래 매개 변수 이름에 대해 별칭을 찾을 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-379">The cmdlet 'Get-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="e51e5-380">'Get-AzIotHubEventHubConsumerGroup' cmdlet에 대한 매개 변수 집합 '__AllParameterSets'가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-380">The parameter set '__AllParameterSets' for cmdlet 'Get-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="e51e5-381">'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' 유형의 'OperationsMonitoringProperties' 속성이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-381">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' has been removed.</span></span>
    - <span data-ttu-id="e51e5-382">'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' 유형의 'OperationsMonitoringProperties' 속성이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-382">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' has been removed.</span></span>
    - <span data-ttu-id="e51e5-383">'New-AzIotHubExportDevice' cmdlet이 더 이상 'New-AzIotHubExportDevices' 별칭을 지원하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-383">The cmdlet 'New-AzIotHubExportDevice' no longer supports the alias 'New-AzIotHubExportDevices'.</span></span>
    - <span data-ttu-id="e51e5-384">'New-AzIotHubImportDevice' cmdlet이 더 이상 'New-AzIotHubImportDevices' 별칭을 지원하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-384">The cmdlet 'New-AzIotHubImportDevice' no longer supports the alias 'New-AzIotHubImportDevices'.</span></span>
    - <span data-ttu-id="e51e5-385">'Remove-AzIotHubEventHubConsumerGroup' cmdlet이 'EventHubEndpointName' 매개 변수를 더 이상 지원하지 않으며 원래 매개 변수 이름에 대해 별칭을 찾을 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-385">The cmdlet 'Remove-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="e51e5-386">'Remove-AzIotHubEventHubConsumerGroup' cmdlet에 대한 매개 변수 집합 '__AllParameterSets'가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-386">The parameter set '__AllParameterSets' for cmdlet 'Remove-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="e51e5-387">'Set-AzIotHub' cmdlet이 'OperationsMonitoringProperties' 매개 변수를 더 이상 지원하지 않으며 원래 매개 변수 이름에 대해 별칭을 찾을 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-387">The cmdlet 'Set-AzIotHub' no longer supports the parameter 'OperationsMonitoringProperties' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="e51e5-388">'Set-AzIotHub' cmdlet에 대한 매개 변수 집합 'UpdateOperationsMonitoringProperties'가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-388">The parameter set 'UpdateOperationsMonitoringProperties' for cmdlet 'Set-AzIotHub' has been removed.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="e51e5-389">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="e51e5-389">Az.RecoveryServices</span></span>
* <span data-ttu-id="e51e5-390">Azure Site Recovery가 Azure-Azure를 위한 NSG, 공용 IP 및 내부 부하 분산 장치와 같은 네트워킹 리소스 구성을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-390">Azure Site Recovery support to configure networking resources like NSG, public IP and internal load balancers for Azure to Azure.</span></span>
* <span data-ttu-id="e51e5-391">Azure Site Recovery가 vMWare-Azure를 위한 관리 디스크에 쓰기를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-391">Azure Site Recovery Support to write to managed disk for vMWare to Azure.</span></span>
* <span data-ttu-id="e51e5-392">Azure Site Recovery가 vMWare-Azure를 위한 NIC 감소를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-392">Azure Site Recovery Support to NIC reduction for vMWare to Azure.</span></span>
* <span data-ttu-id="e51e5-393">Azure Site Recovery가 Azure-Azure를 위한 가속 네트워킹을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-393">Azure Site Recovery Support to accelerated networking for Azure to Azure.</span></span>
* <span data-ttu-id="e51e5-394">Azure Site Recovery가 Azure-Azure를 위한 에이전트 자동 업데이트를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-394">Azure Site Recovery Support to agent auto update for Azure to Azure.</span></span>
* <span data-ttu-id="e51e5-395">Azure Site Recovery가 Azure-Azure를 위한 표준 SSD를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-395">Azure Site Recovery Support to Standard SSD for Azure to Azure.</span></span>
* <span data-ttu-id="e51e5-396">Azure Site Recovery가 Azure-Azure를 위한 두 가지 Azure 디스크 암호화 전달을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-396">Azure Site Recovery Support to Azure Disk Encryption two pass for Azure to Azure.</span></span>
* <span data-ttu-id="e51e5-397">Azure Site Recovery가 Azure-Azure를 위한 새로 추가된 디스크 보호를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-397">Azure Site Recovery Support to protect newly added disk for Azure to Azure.</span></span>
* <span data-ttu-id="e51e5-398">VM을 위한 SoftDelete 기능 및 softdelete를 위한 테스트가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-398">Added SoftDelete feature for VM and added tests for softdelete</span></span>

#### <a name="azresources"></a><span data-ttu-id="e51e5-399">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e51e5-399">Az.Resources</span></span>
* <span data-ttu-id="e51e5-400">종속성 어셈블리 Microsoft.Extensions.Caching.Memory가 1.1.1에서 2.2로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-400">Update dependency assembly Microsoft.Extensions.Caching.Memory from 1.1.1 to 2.2</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e51e5-401">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e51e5-401">Az.Network</span></span>
* <span data-ttu-id="e51e5-402">일반 서비스 공급자 지원을 위해 PrivateEndpointConnection에 대한 모든 cmdlet이 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-402">Change all cmdlets for PrivateEndpointConnection to support generic service provider.</span></span>
    - <span data-ttu-id="e51e5-403">업데이트된 cmdlet:</span><span class="sxs-lookup"><span data-stu-id="e51e5-403">Updated cmdlet:</span></span>
        - <span data-ttu-id="e51e5-404">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="e51e5-404">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="e51e5-405">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="e51e5-405">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="e51e5-406">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="e51e5-406">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="e51e5-407">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="e51e5-407">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="e51e5-408">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="e51e5-408">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="e51e5-409">PrivateLinkResource에 대한 새 cmdlet이 추가되었고 일반 서비스 공급자도 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-409">Add new cmdlet for PrivateLinkResource and it also support generic service provider.</span></span>
    - <span data-ttu-id="e51e5-410">새 cmdlet:</span><span class="sxs-lookup"><span data-stu-id="e51e5-410">New cmdlet:</span></span>
        - <span data-ttu-id="e51e5-411">Get-AzPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="e51e5-411">Get-AzPrivateLinkResource</span></span>
* <span data-ttu-id="e51e5-412">Proxy Protocol V2 기능에 대한 새 필드 및 매개 변수가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-412">Add new fields and parameter for the feature Proxy Protocol V2.</span></span>
    - <span data-ttu-id="e51e5-413">PrivateLinkService에서 EnableProxyProtocol 속성 추가</span><span class="sxs-lookup"><span data-stu-id="e51e5-413">Add property EnableProxyProtocol in PrivateLinkService</span></span>
    - <span data-ttu-id="e51e5-414">PrivateEndpointConnection에서 LinkIdentifier 속성 추가</span><span class="sxs-lookup"><span data-stu-id="e51e5-414">Add property LinkIdentifier in PrivateEndpointConnection</span></span>
    - <span data-ttu-id="e51e5-415">새로운 선택적인 매개 변수인 EnableProxyProtocol을 추가하도록 New-AzPrivateLinkService가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-415">Updated New-AzPrivateLinkService to add a new optional parameter EnableProxyProtocol.</span></span>
* <span data-ttu-id="e51e5-416">'New-AzApplicationGatewaySku' 참조 설명서의 잘못된 매개 변수 설명 수정</span><span class="sxs-lookup"><span data-stu-id="e51e5-416">Fix incorrect parameter description in 'New-AzApplicationGatewaySku' reference documentation</span></span>
* <span data-ttu-id="e51e5-417">Azure 방화벽 정책을 지원하는 새로운 cmdlet</span><span class="sxs-lookup"><span data-stu-id="e51e5-417">New cmdlets to support the azure firewall policy</span></span>
* <span data-ttu-id="e51e5-418">VirtualHub의 자식 리소스 RouteTables에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="e51e5-418">Add support for child resource RouteTables of VirtualHub</span></span>
    - <span data-ttu-id="e51e5-419">추가된 새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-419">New cmdlets added:</span></span>
        - <span data-ttu-id="e51e5-420">Add-AzVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="e51e5-420">Add-AzVirtualHubRoute</span></span>
        - <span data-ttu-id="e51e5-421">Add-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="e51e5-421">Add-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="e51e5-422">Get-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="e51e5-422">Get-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="e51e5-423">Remove-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="e51e5-423">Remove-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="e51e5-424">Set-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="e51e5-424">Set-AzVirtualHub</span></span>
* <span data-ttu-id="e51e5-425">VirtualHub의 새로운 속성 Sku 및 VirtualWan의 VirtualWANType에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="e51e5-425">Add support for new properties Sku of VirtualHub and VirtualWANType of VirtualWan</span></span>
    - <span data-ttu-id="e51e5-426">선택적 매개 변수로 다음 cmdlet이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-426">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="e51e5-427">New-AzVirtualHub: 추가된 매개 변수 Sku</span><span class="sxs-lookup"><span data-stu-id="e51e5-427">New-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="e51e5-428">Update-AzVirtualHub: 추가된 매개 변수 Sku</span><span class="sxs-lookup"><span data-stu-id="e51e5-428">Update-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="e51e5-429">New-AzVirtualWan: 추가된 매개 변수 VirtualWANType</span><span class="sxs-lookup"><span data-stu-id="e51e5-429">New-AzVirtualWan : added parameter VirtualWANType</span></span>
        - <span data-ttu-id="e51e5-430">Update-AzVirtualWan: 추가된 매개 변수 VirtualWANType</span><span class="sxs-lookup"><span data-stu-id="e51e5-430">Update-AzVirtualWan : added parameter VirtualWANType</span></span>
* <span data-ttu-id="e51e5-431">HubVnetConnection, VpnConnection 및 ExpressRouteConnection에 대한 EnableInternetSecurity 속성 지원 추가</span><span class="sxs-lookup"><span data-stu-id="e51e5-431">Add support for EnableInternetSecurity property for HubVnetConnection, VpnConnection and ExpressRouteConnection</span></span>
    - <span data-ttu-id="e51e5-432">추가된 새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-432">New cmdlets added:</span></span>
        - <span data-ttu-id="e51e5-433">Update-AzureRmVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="e51e5-433">Update-AzureRmVirtualHubVnetConnection</span></span>
    - <span data-ttu-id="e51e5-434">선택적 매개 변수로 다음 cmdlet이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-434">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="e51e5-435">New-AzureRmVirtualHubVnetConnection: 추가된 매개 변수 EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="e51e5-435">New-AzureRmVirtualHubVnetConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="e51e5-436">New-AzureRmVpnConnection: 추가된 매개 변수 EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="e51e5-436">New-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="e51e5-437">Update-AzureRmVpnConnection: 추가된 매개 변수 EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="e51e5-437">Update-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="e51e5-438">New-AzureRmExpressRouteConnection: 추가된 매개 변수 EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="e51e5-438">New-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="e51e5-439">Set-AzureRmExpressRouteConnection: 추가된 매개 변수 EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="e51e5-439">Set-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
* <span data-ttu-id="e51e5-440">TopLevel WebApplicationFirewall 정책 구성을 위한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="e51e5-440">Add support for Configuring TopLevel WebApplicationFirewall Policy</span></span>
    - <span data-ttu-id="e51e5-441">추가된 새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-441">New cmdlets added:</span></span>
        - <span data-ttu-id="e51e5-442">New-AzApplicationGatewayFirewallPolicySetting</span><span class="sxs-lookup"><span data-stu-id="e51e5-442">New-AzApplicationGatewayFirewallPolicySetting</span></span>
        - <span data-ttu-id="e51e5-443">New-AzApplicationGatewayFirewallPolicyExclusion</span><span class="sxs-lookup"><span data-stu-id="e51e5-443">New-AzApplicationGatewayFirewallPolicyExclusion</span></span>
        - <span data-ttu-id="e51e5-444">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="e51e5-444">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span></span>
        - <span data-ttu-id="e51e5-445">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="e51e5-445">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span></span>
        - <span data-ttu-id="e51e5-446">New-AzApplicationGatewayFirewallPolicyManagedRule</span><span class="sxs-lookup"><span data-stu-id="e51e5-446">New-AzApplicationGatewayFirewallPolicyManagedRule</span></span>
        - <span data-ttu-id="e51e5-447">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="e51e5-447">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span></span>
    - <span data-ttu-id="e51e5-448">선택적 매개 변수로 다음 cmdlet이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-448">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="e51e5-449">New-AzApplicationGatewayFirewallPolicy: 추가된 매개 변수 PolicySetting, ManagedRule</span><span class="sxs-lookup"><span data-stu-id="e51e5-449">New-AzApplicationGatewayFirewallPolicy : added parameter PolicySetting, ManagedRule</span></span>
* <span data-ttu-id="e51e5-450">CustomRule에서 Geo-Match 연산자를 위한 지원 추가됨</span><span class="sxs-lookup"><span data-stu-id="e51e5-450">Added support for Geo-Match operator on CustomRule</span></span>
    - <span data-ttu-id="e51e5-451">FirewallCondition에서 연산자에 GeoMatch 추가됨</span><span class="sxs-lookup"><span data-stu-id="e51e5-451">Added GeoMatch to the operator on the FirewallCondition</span></span>
* <span data-ttu-id="e51e5-452">perListener 및 perSite 방화벽 규칙에 대한 지원 추가됨</span><span class="sxs-lookup"><span data-stu-id="e51e5-452">Added support for perListener and perSite Firewall policy</span></span>
    - <span data-ttu-id="e51e5-453">선택적 매개 변수로 다음 cmdlet이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-453">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="e51e5-454">New-AzApplicationGatewayHttpListener: 추가된 매개 변수 FirewallPolicy, FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="e51e5-454">New-AzApplicationGatewayHttpListener : added parameter FirewallPolicy, FirewallPolicyId</span></span>
        - <span data-ttu-id="e51e5-455">New-AzApplicationGatewayPathRuleConfig: 추가된 매개 변수 FirewallPolicy, FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="e51e5-455">New-AzApplicationGatewayPathRuleConfig : added parameter FirewallPolicy, FirewallPolicyId</span></span>
* <span data-ttu-id="e51e5-456">'PSBastion'에서 이름이 AzureBastionSubnet인 필수 서브넷의 수정은 대소문자를 구분하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-456">Fix required subnet with name AzureBastionSubnet in 'PSBastion' can be case insensitive</span></span>
* <span data-ttu-id="e51e5-457">Azure Firewall을 위한 네트워크 규칙의 대상 FQDN 및 NAT 규칙의 번역된 FQDN 지원</span><span class="sxs-lookup"><span data-stu-id="e51e5-457">Support for Destination FQDNs in Network Rules and Translated FQDN in NAT Rules for Azure Firewall</span></span>
* <span data-ttu-id="e51e5-458">IpGroup의 최상위 리소스 RouteTables에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="e51e5-458">Add support for top level resource RouteTables of IpGroup</span></span>
    - <span data-ttu-id="e51e5-459">추가된 새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-459">New cmdlets added:</span></span>
        - <span data-ttu-id="e51e5-460">New-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="e51e5-460">New-AzIpGroup</span></span>
        - <span data-ttu-id="e51e5-461">Remove-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="e51e5-461">Remove-AzIpGroup</span></span>
        - <span data-ttu-id="e51e5-462">Get-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="e51e5-462">Get-AzIpGroup</span></span>
        - <span data-ttu-id="e51e5-463">Set-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="e51e5-463">Set-AzIpGroup</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="e51e5-464">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="e51e5-464">Az.ServiceFabric</span></span>
* <span data-ttu-id="e51e5-465">Add-AzVmssSecret에서 지원되기 때문에 Add-AzServiceFabricApplicationCertificate cmdlet이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-465">Remove Add-AzServiceFabricApplicationCertificate cmdlet as this scenario is covered by Add-AzVmssSecret.</span></span>

#### <a name="azsql"></a><span data-ttu-id="e51e5-466">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e51e5-466">Az.Sql</span></span>
* <span data-ttu-id="e51e5-467">Managed Instances에서 삭제된 데이터베이스의 복원을 위한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-467">Added support for restore of dropped databases on Managed Instances.</span></span>
* <span data-ttu-id="e51e5-468">이전의 감사 cmdlet 코드가 사용되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-468">Deprecated from code old auditing cmdlets.</span></span>
* <span data-ttu-id="e51e5-469">사용되지 않는 별칭이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-469">Removed deprecated aliases:</span></span>
* <span data-ttu-id="e51e5-470">Get-AzSqlDatabaseIndexRecommendations(대신 Get-AzSqlDatabaseIndexRecommendation 사용)</span><span class="sxs-lookup"><span data-stu-id="e51e5-470">Get-AzSqlDatabaseIndexRecommendations (use Get-AzSqlDatabaseIndexRecommendation instead)</span></span>
* <span data-ttu-id="e51e5-471">Get-AzSqlDatabaseRestorePoints(대신 Get-AzSqlDatabaseRestorePoint 사용)</span><span class="sxs-lookup"><span data-stu-id="e51e5-471">Get-AzSqlDatabaseRestorePoints (use Get-AzSqlDatabaseRestorePoint instead)</span></span>
* <span data-ttu-id="e51e5-472">Get-AzSqlDatabaseSecureConnectionPolicy cmdlet 제거</span><span class="sxs-lookup"><span data-stu-id="e51e5-472">Remove Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="e51e5-473">사용되지 않는 취약성 평가 설정 cmdlet에 대한 별칭 제거</span><span class="sxs-lookup"><span data-stu-id="e51e5-473">Remove aliases for deprecated Vulnerability Assessment Settings cmdlets</span></span>
* <span data-ttu-id="e51e5-474">지능형 위협 탐지 설정 cmdlet 사용 중단</span><span class="sxs-lookup"><span data-stu-id="e51e5-474">Deprecate Advanced Threat Detection Settings cmdlets</span></span> 
* <span data-ttu-id="e51e5-475">데이터베이스의 열에 대한 민감도 권장 사항의 사용 여부를 제어하는 cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-475">Adding cmdlets to Disable and enable sensitivity recommendations on columns in a database.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="e51e5-476">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="e51e5-476">Az.Storage</span></span>
* <span data-ttu-id="e51e5-477">스토리지 계정을 만들거나 업데이트할 때 큰 파일 공유 사용 지원</span><span class="sxs-lookup"><span data-stu-id="e51e5-477">Support enable Large File share when create or update Storage account</span></span>
    -  <span data-ttu-id="e51e5-478">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="e51e5-478">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="e51e5-479">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="e51e5-479">Set-AzStorageAccount</span></span>
* <span data-ttu-id="e51e5-480">파일 핸들을 닫거나/가져올 때, DeletePending 상태의 개체로 인한 오류를 방지하기 위해 입력 경로가 파일 디렉터리인지 또는 파일인지를 확인하는 과정을 건너뜁니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-480">When close/get File handle, skip check the input path is File directory or File, to avoid failure with object in DeletePending status</span></span>
    -  <span data-ttu-id="e51e5-481">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="e51e5-481">Get-AzStorageFileHandle</span></span>
    -  <span data-ttu-id="e51e5-482">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="e51e5-482">Close-AzStorageFileHandle</span></span>
    
## <a name="280---october-2019"></a><span data-ttu-id="e51e5-483">2.8.0 - 2019년 10월</span><span class="sxs-lookup"><span data-stu-id="e51e5-483">2.8.0 - October 2019</span></span>
### <a name="general"></a><span data-ttu-id="e51e5-484">일반</span><span class="sxs-lookup"><span data-stu-id="e51e5-484">General</span></span>
* <span data-ttu-id="e51e5-485">Az.HealthcareApis 1.0.0 릴리스</span><span class="sxs-lookup"><span data-stu-id="e51e5-485">Az.HealthcareApis 1.0.0 release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="e51e5-486">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e51e5-486">Az.Accounts</span></span>
* <span data-ttu-id="e51e5-487">생성된 모듈에 대한 원격 분석 및 URL 다시 작성이 업데이트되고, Windows 단위 테스트가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-487">Update telemetry and url rewriting for generated modules, fix windows unit tests.</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="e51e5-488">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="e51e5-488">Az.ApiManagement</span></span>
* <span data-ttu-id="e51e5-489">**Set-AzApiManagementApi** - API 업데이트 지원이 ApiVersionSet에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-489">**Set-AzApiManagementApi** - Added support for Updating Api into ApiVersionSet</span></span>
    - <span data-ttu-id="e51e5-490">문제 https://github.com/Azure/azure-powershell/issues/10068 수정</span><span class="sxs-lookup"><span data-stu-id="e51e5-490">Fix for issue https://github.com/Azure/azure-powershell/issues/10068</span></span>

#### <a name="azautomation"></a><span data-ttu-id="e51e5-491">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="e51e5-491">Az.Automation</span></span>
* <span data-ttu-id="e51e5-492">Linux 다시 부팅 설정 매개 변수에 대한 New-AzureAutomationSoftwareUpdateConfiguration cmdlet이 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-492">Fixed New-AzureAutomationSoftwareUpdateConfiguration cmdlet for Linux reboot setting parameter.</span></span> 

#### <a name="azbatch"></a><span data-ttu-id="e51e5-493">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="e51e5-493">Az.Batch</span></span>
* <span data-ttu-id="e51e5-494">**Get-AzBatchNodeAgentSku**가 더 이상 사용되지 않으며, 2.0.0 버전의 **Get-AzBatchSupportImage**로 대체되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-494">**Get-AzBatchNodeAgentSku** is deprecated and will be replaced by **Get-AzBatchSupportImage** in version 2.0.0.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e51e5-495">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e51e5-495">Az.Compute</span></span>
* <span data-ttu-id="e51e5-496">Priority, EvictionPolicy 및 MaxPrice 매개 변수가 New-AzVM 및 New-AzVmss cmdlet에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-496">Add Priority, EvictionPolicy, and MaxPrice parameters to New-AzVM and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="e51e5-497">Add-AzVMAdditionalUnattendContent 및 Add-AzVMSshPublicKey cmdlet에 대한 경고 메시지와 도움말 문서가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-497">Fix warning message and help document for Add-AzVMAdditionalUnattendContent and Add-AzVMSshPublicKey cmdlets</span></span>
* <span data-ttu-id="e51e5-498">Set-AzVMDiskEncryptionExtension의 관리 디스크가 있는 Linux VM에 대한 -skipVmBackup 예외가 해결되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-498">Fix -skipVmBackup exception for Linux VMs with managed disks for Set-AzVMDiskEncryptionExtension.</span></span> 
* <span data-ttu-id="e51e5-499">Set-AzVMDiskEncryptionExtension의 두 가지 패스 시나리오에서 발생하는 암호화 설정 업데이트의 버그가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-499">Fix bug in update encryption settings in Set-AzVMDiskEncryptionExtension, two pass scenario.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="e51e5-500">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="e51e5-500">Az.DataFactory</span></span>
* <span data-ttu-id="e51e5-501">ADF V2 데이터 흐름에 대한 CRUD 명령으로 Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow 및 Get-AzDataFactoryV2DataFlow가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-501">Adding CRUD commands for ADF V2 data flow: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow, and Get-AzDataFactoryV2DataFlow.</span></span>
* <span data-ttu-id="e51e5-502">ADF V2 데이터 흐름 디버그 세션에 대한 작업 명령으로 Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand 및 Stop-AzDataFactoryV2DataFlowDebugSession이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-502">Adding action commands for ADF V2 data flow debug Session: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand and Stop-AzDataFactoryV2DataFlowDebugSession.</span></span>
* <span data-ttu-id="e51e5-503">ADF .Net SDK 버전이 4.2.0으로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-503">Update ADF .Net SDK version to 4.2.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="e51e5-504">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="e51e5-504">Az.DataLakeStore</span></span>
* <span data-ttu-id="e51e5-505">도메인 없이 '-'가 있는 계정을 전달할 수 있도록 계정 유효성 검사가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-505">Fix account validation so that accounts with '-' can be passed without domain</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="e51e5-506">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="e51e5-506">Az.HealthcareApis</span></span>
* <span data-ttu-id="e51e5-507">PowerShell 버전이 1.0.0으로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-507">Updated the powershell version to 1.0.0</span></span>
* <span data-ttu-id="e51e5-508">SDK 버전이 1.0.2로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-508">Updated the SDK version to 1.0.2</span></span>
* <span data-ttu-id="e51e5-509">새 SDK 버전을 참조하도록 테스트가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-509">Update in tests to refer to new SDK version</span></span>
* <span data-ttu-id="e51e5-510">출력이 중첩 구조에서 평면화 구조로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-510">Updated the output structure from nested to flattened.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="e51e5-511">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="e51e5-511">Az.IotHub</span></span>
* <span data-ttu-id="e51e5-512">새 라우팅 원본 추가: DigitalTwinChangeEvents</span><span class="sxs-lookup"><span data-stu-id="e51e5-512">Add new routing source: DigitalTwinChangeEvents</span></span>
* <span data-ttu-id="e51e5-513">사소한 버그 수정: Get-AzIothub에서 subscriptionId를 반환하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-513">Minor bug fix: Get-AzIothub not returning subscriptionId</span></span> 

#### <a name="azmonitor"></a><span data-ttu-id="e51e5-514">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="e51e5-514">Az.Monitor</span></span>
* <span data-ttu-id="e51e5-515">작업 그룹에 대한 새 작업 그룹 수신기로 -ItsmReceiver, -VoiceReceiver, -ArmRoleReceiver, -AzureFunctionReceiver, -LogicAppReceiver, -AutomationRunbookReceiver, -AzureAppPushReceiver가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-515">New action group receivers added for action group   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span></span>
* <span data-ttu-id="e51e5-516">수신기에 사용하도록 설정된 일반 경고 스키마가 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-516">Use common alert schema enabled for the receivers.</span></span> <span data-ttu-id="e51e5-517">SMS, Azure 앱 푸시, ITSM 및 음성 수신기에는 적용되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-517">This is not applicable for SMS, Azure App push , ITSM and Voice recievers</span></span>
* <span data-ttu-id="e51e5-518">웹후크에서 이제 Azure Active Directory 인증을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-518">Webhooks now supports Azure active directory authentication .</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e51e5-519">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e51e5-519">Az.Network</span></span>
* <span data-ttu-id="e51e5-520">서비스 엔드포인트 정책에 사용할 수 있는 별칭을 가져오기 위해 호출할 수 있는 새 Get-AzAvailableServiceAlias cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-520">Add new cmdlet Get-AzAvailableServiceAlias which can be called to get the aliases that can be used for Service Endpoint Policies.</span></span>
* <span data-ttu-id="e51e5-521">트래픽 선택기를 Virtual Network 게이트웨이 연결에 추가할 수 있는 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-521">Added support for the adding traffic selectors to Virtual Network Gateway Connections</span></span>
    - <span data-ttu-id="e51e5-522">추가된 새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-522">New cmdlets added:</span></span>
        - <span data-ttu-id="e51e5-523">New-AzureRmTrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="e51e5-523">New-AzureRmTrafficSelectorPolicy</span></span>
    - <span data-ttu-id="e51e5-524">cmdlet이 선택적인 -TrafficSelectorPolicies, -New-AzureRmVirtualNetworkGatewayConnection, -Set-AzureRmVirtualNetworkGatewayConnection 매개 변수로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-524">Cmdlets updated with optional parameter -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="e51e5-525">ESP 및 AH 프로토콜 지원이 네트워크 보안 규칙 구성에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-525">Add support for ESP and AH protocols in network security rule configurations</span></span>
    - <span data-ttu-id="e51e5-526">다음 Cmdlet이 업데이트 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-526">Updated cmdlets:</span></span>
        - <span data-ttu-id="e51e5-527">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e51e5-527">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="e51e5-528">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e51e5-528">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="e51e5-529">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e51e5-529">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="e51e5-530">Cortex cmdlet의 예외 처리가 향상되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-530">Improve handling of exceptions in Cortex cmdlets</span></span>
* <span data-ttu-id="e51e5-531">새 VirtualNetworkGateways 세대 및 SKU</span><span class="sxs-lookup"><span data-stu-id="e51e5-531">New Generations and SKUs for VirtualNetworkGateways</span></span>
  - <span data-ttu-id="e51e5-532">새 VirtualNetworkGateways 세대가 도입되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-532">Introduce new Generations for VirtualNetworkGateways.</span></span>
  - <span data-ttu-id="e51e5-533">높은 처리량의 새 VirtualNetworkGateways SKU가 도입되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-533">Introduce new high throughput SKUs for VirtualNetworkGateways.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="e51e5-534">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="e51e5-534">Az.RedisCache</span></span>
* <span data-ttu-id="e51e5-535">'-Size' 매개 변수에 대한 누락 값을 포함하도록 'Set-AzRedisCache' 참조 설명서가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-535">Updated 'Set-AzRedisCache' reference documentation to include missing values for '-Size' parameter</span></span>

#### <a name="azsql"></a><span data-ttu-id="e51e5-536">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e51e5-536">Az.Sql</span></span>
* <span data-ttu-id="e51e5-537">Managed Instance에서 Active Directory 관리자를 설정할 수 있는 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-537">Add support for setting Active Directory Administrator on Managed Instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="e51e5-538">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="e51e5-538">Az.Storage</span></span>
* <span data-ttu-id="e51e5-539">스토리지 클라이언트 라이브러리가 11.1.0으로 업그레이드되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-539">Upgrade Storage Client Library to 11.1.0</span></span>
* <span data-ttu-id="e51e5-540">관리 평면 API를 사용하여 컨테이너를 나열하면 NextPageLink를 통해 나열됩니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-540">List containers with Management plane API, will list with NextPageLink</span></span>
    -  <span data-ttu-id="e51e5-541">Get-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="e51e5-541">Get-AzRmStorageContainer</span></span>
* <span data-ttu-id="e51e5-542">구독에서 스토리지 계정을 나열하면 NextPageLink를 통해 나열됩니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-542">List Storage accounts from subscription, will list with NextPageLink</span></span>
    -  <span data-ttu-id="e51e5-543">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="e51e5-543">Get-AzStorageAccount</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="e51e5-544">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="e51e5-544">Az.StorageSync</span></span>
* <span data-ttu-id="e51e5-545">Reset-AzStorageSyncServerCertificate의 9810 문제가 해결되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-545">Fix Issue 9810 in Reset-AzStorageSyncServerCertificate.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="e51e5-546">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="e51e5-546">Az.Websites</span></span>
* <span data-ttu-id="e51e5-547">앱의 ASP를 업데이트하는 Set-AzWebApp이 실패했습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-547">Set-AzWebApp updating ASP of an app was failing</span></span>

## <a name="270---september-2019"></a><span data-ttu-id="e51e5-548">2.7.0 - 2019년 9월</span><span class="sxs-lookup"><span data-stu-id="e51e5-548">2.7.0 - September 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="e51e5-549">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="e51e5-549">Az.ApiManagement</span></span>
* <span data-ttu-id="e51e5-550">'Set-AzApiManagementPolicy' 참조 설명서에서 '-Format' 매개 변수 설명이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-550">Update '-Format' parameter description in 'Set-AzApiManagementPolicy' reference documentation</span></span>
* <span data-ttu-id="e51e5-551">참조 설명서에서 사용되지 않는 cmdlet 'Update-AzApiManagementDeployment'의 참조를 제거했습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-551">Removed references of deprecated cmdlet 'Update-AzApiManagementDeployment' from reference documentation.</span></span> <span data-ttu-id="e51e5-552">그 대신 'Set-AzApiManagement'를 사용하세요.</span><span class="sxs-lookup"><span data-stu-id="e51e5-552">Use 'Set-AzApiManagement' instead.</span></span>

#### <a name="azautomation"></a><span data-ttu-id="e51e5-553">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="e51e5-553">Az.Automation</span></span>
* <span data-ttu-id="e51e5-554">'Register-AzAutomationDscNode'에 대한 참조 설명서의 예제 오타가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-554">Fixed example typo in reference documentation for 'Register-AzAutomationDscNode'</span></span>
* <span data-ttu-id="e51e5-555">Register-AzAutomationDSCNode에 OS 제한에 대한 설명이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-555">Added clarification on OS restriction to Register-AzAutomationDSCNode</span></span>
* <span data-ttu-id="e51e5-556">-Wait 옵션에 대한 Start-AzAutomationRunbook cmdlet Null 참조 예외가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-556">Fixed Start-AzAutomationRunbook cmdlet Null reference exception for -Wait option.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e51e5-557">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e51e5-557">Az.Compute</span></span>
* <span data-ttu-id="e51e5-558">New-AzDiskConfig에 UploadSizeInBytes 매개 변수가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-558">Add UploadSizeInBytes parameter tp New-AzDiskConfig</span></span>
* <span data-ttu-id="e51e5-559">New-AzSnapshotConfig에 증분 매개 변수가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-559">Add Incremental parameter to New-AzSnapshotConfig</span></span>
* <span data-ttu-id="e51e5-560">다음과 같은 낮은 우선 순위의 가상 머신 기능이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-560">Add a low priority virtual machine feature:</span></span>
    - <span data-ttu-id="e51e5-561">MaxPrice, EvictionPolicy 및 Priority 매개 변수가 New-AzVMConfig에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-561">MaxPrice, EvictionPolicy and Priority parameters are added to New-AzVMConfig.</span></span>
    - <span data-ttu-id="e51e5-562">MaxPrice 매개 변수는 New-AzVmssConfig, Update-AzVM 및 Update-AzVmss cmdlet에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-562">MaxPrice parameter is added to New-AzVmssConfig, Update-AzVM and Update-AzVmss cmdlets.</span></span>
* <span data-ttu-id="e51e5-563">구독의 모든 가용성 세트를 나열할 때 발생하는 Get-AzAvailabilitySet cmdlet에 대한 VM 참조 이슈가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-563">Fix VM reference issue for Get-AzAvailabilitySet cmdlet when it lists all availability sets in the subscription.</span></span>
* <span data-ttu-id="e51e5-564">Get-AzRemoteDesktopFile에 대한 null 예외가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-564">Fix the null exception for Get-AzRemoteDesktopFile.</span></span>
* <span data-ttu-id="e51e5-565">종료 상대 위치에 대한 VHD 검색 메서드가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-565">Fix VHD Seek method for end-relative position.</span></span>
* <span data-ttu-id="e51e5-566">New-AzVM 및 Update-AzVM에 대한 UltraSSD 이슈가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-566">Fix UltraSSD issue for New-AzVM and Update-AzVM.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="e51e5-567">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="e51e5-567">Az.DataFactory</span></span>
* <span data-ttu-id="e51e5-568">ADF V2에 대한 3가지 새 명령 Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription 및 Get-AzDataFactoryV2TriggerSubscriptionStatus가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-568">Adding 3 new commands for ADF V2 - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription, and Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>
* <span data-ttu-id="e51e5-569">ADF .Net SDK 버전이 4.1.3으로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-569">Updated ADF .Net SDK version to 4.1.3</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="e51e5-570">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="e51e5-570">Az.HDInsight</span></span>
* <span data-ttu-id="e51e5-571">호출 주요 변경 내용</span><span class="sxs-lookup"><span data-stu-id="e51e5-571">Call out breaking changes</span></span>

#### <a name="aziothub"></a><span data-ttu-id="e51e5-572">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="e51e5-572">Az.IotHub</span></span>
* <span data-ttu-id="e51e5-573">지역 쌍 재해 복구 지역에 IotHub에 대한 장애 조치(failover) 호출 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-573">Add support to invoke failover for an IotHub to the geo-paired disaster recovery region.</span></span>
* <span data-ttu-id="e51e5-574">IotHub에 대한 메시지 보강 관리 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-574">Add support to manage message enrichment for an IotHub.</span></span> <span data-ttu-id="e51e5-575">새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-575">New cmdlets are:</span></span>
    - <span data-ttu-id="e51e5-576">Add-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="e51e5-576">Add-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="e51e5-577">Get-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="e51e5-577">Get-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="e51e5-578">Remove-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="e51e5-578">Remove-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="e51e5-579">Set-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="e51e5-579">Set-AzIotHubMessageEnrichment</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="e51e5-580">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="e51e5-580">Az.Monitor</span></span>
* <span data-ttu-id="e51e5-581">최신 모니터링 SDK, 즉, 0.24.1-preview를 가리킵니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-581">Pointing to the most recent Monitor SDK, i.e. 0.24.1-preview</span></span>
   - <span data-ttu-id="e51e5-582">메트릭 cmdlet에 줄 바꿈하지 않는 변경 내용을 추가합니다. 즉, 단위 열거형은 여러 새 값을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-582">Adds non-braking changes to the Metrics cmdlets, i.e. the Unit enumeration supports several new values.</span></span> <span data-ttu-id="e51e5-583">이러한 cmdlet은 읽기 전용이므로 cmdlet 입력이 변경되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-583">These are read-only cmdlets, so there would be no change in the input of the cmdlets.</span></span>
   - <span data-ttu-id="e51e5-584">이제 **ActionGroups** 요청의 api 버전은 **2019-06-01**이고, 이전에는 **2018-03-01**였습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-584">The api-version of the **ActionGroups** requests is now **2019-06-01**, before it was **2018-03-01**.</span></span> <span data-ttu-id="e51e5-585">시나리오 테스트가 이 변경 내용에 맞게 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-585">The scenario tests have been updated to accommodate for this change.</span></span>
   - <span data-ttu-id="e51e5-586">**EmailReceiver** 및 **WebhookReceiver** 클래스에 대한 생성자가 새 필수 인수, 즉, **useCommonAlertSchema**라는 부울 값을 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-586">The constructors for the classes **EmailReceiver** and **WebhookReceiver** added one new mandatory argument, i.e. a Boolean value called **useCommonAlertSchema**.</span></span> <span data-ttu-id="e51e5-587">현재 이 값은 cmdlet의 주요 변경 사항을 숨기도록 **false**로 고정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-587">Currently, the value is fixed to **false** to hide this breaking change from the cmdlets.</span></span> <span data-ttu-id="e51e5-588">**참고**: 이 변경 사항은 경고 팀에서 유효성을 검사해야 하는 임시 변경 내용입니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-588">**NOTE**: this is a temporary change that must be validated by the Alerts team.</span></span>
   - <span data-ttu-id="e51e5-589">이전 SDK에서 변경된 **Source** 클래스(**ScheduledQueryRuleSource** 클래스와 관련됨)의 생성자에 대한 인수 순서입니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-589">The order of the arguments for the constructor of the class **Source** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="e51e5-590">이번 변화로 인해 두 개의 단위 테스트를 수정해야 했습니다. 즉, 두 단위 테스트가 컴파일되었지만 테스트를 통과하지 못했습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-590">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
   - <span data-ttu-id="e51e5-591">이전 SDK에서 변경된 **AlertingAction** 클래스(**ScheduledQueryRuleSource** 클래스와 관련됨)의 생성자에 대한 인수 순서입니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-591">The order of the arguments for the constructor of the class **AlertingAction** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="e51e5-592">이번 변화로 인해 두 개의 단위 테스트를 수정해야 했습니다. 즉, 두 단위 테스트가 컴파일되었지만 테스트를 통과하지 못했습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-592">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
* <span data-ttu-id="e51e5-593">메트릭 경고 V2에 대한 동적 임계값 기준 지원</span><span class="sxs-lookup"><span data-stu-id="e51e5-593">Support Dynamic Threshold criteria for metric alert V2</span></span>
    - <span data-ttu-id="e51e5-594">AzMetricAlertRuleV2Criteria: 이제 동적 임계값 조건도 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-594">New-AzMetricAlertRuleV2Criteria: now creats dynamic threshold criteria also</span></span>
    - <span data-ttu-id="e51e5-595">Add-AzMetricAlertRuleV2: 이제 동적 임계값 조건도 수락합니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-595">Add-AzMetricAlertRuleV2: now accept dynamic threshold criteria also</span></span>
* <span data-ttu-id="e51e5-596">SQR(예약된 쿼리 규칙)의 향상된 기능</span><span class="sxs-lookup"><span data-stu-id="e51e5-596">Improvements in Scheduled Query Rule cmdlets (SQR)</span></span>
 - <span data-ttu-id="e51e5-597">Cmdlet이 'Location' 매개 변수를 두 가지 형식(eastus 같은 위치 또는 미국 동부 같은 위치 표시 이름)으로 모두 허용합니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-597">Cmdlets will accept 'Location' paramater in both formats, either the location (e.g. eastus) or the location display name (e.g. East US)</span></span>
 - <span data-ttu-id="e51e5-598">도움말 파일에 적절하게 표시된 'Enabled' 매개 변수</span><span class="sxs-lookup"><span data-stu-id="e51e5-598">Illustrated 'Enabled' parameter in help files properly</span></span>
 - <span data-ttu-id="e51e5-599">선택적 매개 변수 'ActionGroup'에 대한 예제가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-599">Added examples for 'ActionGroup' optional parameter</span></span>
 - <span data-ttu-id="e51e5-600">도움말 파일이 전체적으로 개선되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-600">Overall improved help files</span></span>
* <span data-ttu-id="e51e5-601">'Set-AzActionRule'의 범위 유형 결정 버그를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-601">Fix bug in determining scope type for 'Set-AzActionRule'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e51e5-602">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e51e5-602">Az.Network</span></span>
* <span data-ttu-id="e51e5-603">'New-AzApplicationGateway' 참조 설명서의 잘못된 예제가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-603">Fix incorrect example in 'New-AzApplicationGateway' reference documentation</span></span> 
* <span data-ttu-id="e51e5-604">'Get-AzNetworkWatcherPacketCapture' 참조 설명서에 패킷 캡처를 위한 모든 속성 검색과 관련된 메모가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-604">Add note in 'Get-AzNetworkWatcherPacketCapture' reference documentation about retrieving all properties for a packet capture</span></span>
* <span data-ttu-id="e51e5-605">NIC를 올바르게 열거하도록 'Test-AzNetworkWatcherIPFlow' 참조 설명서의 예제가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-605">Fixed example in 'Test-AzNetworkWatcherIPFlow' reference documentation to correctly enumerate NICs</span></span>
* <span data-ttu-id="e51e5-606">추가 세부 정보가 있는 경우 추가 세부 정보를 표시하도록 클라우드 예외 구문 분석이 향상되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-606">Improved cloud exception parsing to display additional details if they are present</span></span>
* <span data-ttu-id="e51e5-607">더 많은 형식의 SDK 예외를 처리하도록 클라우드 예외 구문 분석이 향상되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-607">Improved cloud exception parsing to handle additional type of SDK exception</span></span>
* <span data-ttu-id="e51e5-608">보안 규칙 모델의 잘못된 매핑이 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-608">Fixed incorrect mapping of Security Rule models</span></span>
* <span data-ttu-id="e51e5-609">네트워크 인터페이스에 개인 IP 기능을 위한 속성이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-609">Added properties to network interface for private ip feature</span></span>
    - <span data-ttu-id="e51e5-610">PSNetworkInterface에 'PrivateEndpoint' 속성이 PSResourceId 형식으로 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-610">Added property 'PrivateEndpoint' as type of PSResourceId to PSNetworkInterface</span></span>
    - <span data-ttu-id="e51e5-611">PSNetworkInterfaceIPConfiguration에 'PrivateLinkConnectionProperties' 속성이 PSIpConfigurationConnectivityInformation 형식으로 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-611">Added property 'PrivateLinkConnectionProperties' as type of PSIpConfigurationConnectivityInformation to PSNetworkInterfaceIPConfiguration</span></span>
    - <span data-ttu-id="e51e5-612">새 모델 클래스 PSIpConfigurationConnectivityInformation이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-612">Added new model class PSIpConfigurationConnectivityInformation</span></span>
* <span data-ttu-id="e51e5-613">Azure Firewall 리소스에 대한 새 ApplicationRuleProtocolType 'mssql'이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-613">Added new ApplicationRuleProtocolType 'mssql' for Azure Firewall resource</span></span>
* <span data-ttu-id="e51e5-614">Virtual WAN에서 멀티 링크를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-614">MultiLink support in Virtual WAN</span></span>
    - <span data-ttu-id="e51e5-615">새로운 cmdlet</span><span class="sxs-lookup"><span data-stu-id="e51e5-615">New cmdlets</span></span>
        - <span data-ttu-id="e51e5-616">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="e51e5-616">New-AzVpnSiteLink</span></span>
        - <span data-ttu-id="e51e5-617">New-AzVpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="e51e5-617">New-AzVpnSiteLinkConnection</span></span>
    - <span data-ttu-id="e51e5-618">업데이트된 cmdlet:</span><span class="sxs-lookup"><span data-stu-id="e51e5-618">Updated cmdlet:</span></span>
        - <span data-ttu-id="e51e5-619">New-VpnSite</span><span class="sxs-lookup"><span data-stu-id="e51e5-619">New-VpnSite</span></span>
        - <span data-ttu-id="e51e5-620">Update-VpnSite</span><span class="sxs-lookup"><span data-stu-id="e51e5-620">Update-VpnSite</span></span>
        - <span data-ttu-id="e51e5-621">New-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="e51e5-621">New-VpnConnection</span></span>
        - <span data-ttu-id="e51e5-622">Update-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="e51e5-622">Update-VpnConnection</span></span>
* <span data-ttu-id="e51e5-623">AzureRM cmdlet 대신 Az cmdlet을 사용하도록 일부 PowerShell 예제의 문서가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-623">Fixed documents for some PowerShell examples to use Az cmdlets instead of AzureRM cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="e51e5-624">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="e51e5-624">Az.RecoveryServices</span></span>
* <span data-ttu-id="e51e5-625">AzureVMpolicy 개체가 ProtectedItemsCount 특성으로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-625">Update AzureVMpolicy Object with ProtectedItemsCount Attribute</span></span>
* <span data-ttu-id="e51e5-626">VM 정책 및 원래 스토리지 계정 복원에 대한 테스트가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-626">Added Tests for VM policy and Original Storage Account Restore</span></span>

#### <a name="azresources"></a><span data-ttu-id="e51e5-627">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e51e5-627">Az.Resources</span></span>
* <span data-ttu-id="e51e5-628">매개 변수 범위 없이 AzRoleAssignment를 호출할 수 없는 버그가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-628">Fix bug where New-AzRoleAssignment could not be called without parameter Scope.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="e51e5-629">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="e51e5-629">Az.ServiceFabric</span></span>
* <span data-ttu-id="e51e5-630">'AzServiceFabricReliability' 참조 설명서에 대한 예제의 오타가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-630">Fixed typo in example for 'Update-AzServiceFabricReliability' reference documentation</span></span>
* <span data-ttu-id="e51e5-631">애플리케이션 및 서비스를 관리하는 다음과 같은 새 cmdlet이 추가됩니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-631">Adding new cmdlets to manage appliaction and services:</span></span>
    - <span data-ttu-id="e51e5-632">New-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="e51e5-632">New-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="e51e5-633">New-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="e51e5-633">New-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="e51e5-634">New-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="e51e5-634">New-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="e51e5-635">New-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="e51e5-635">New-AzServiceFabricService</span></span>
    - <span data-ttu-id="e51e5-636">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="e51e5-636">Update-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="e51e5-637">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="e51e5-637">Get-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="e51e5-638">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="e51e5-638">Get-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="e51e5-639">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="e51e5-639">Get-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="e51e5-640">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="e51e5-640">Get-AzServiceFabricService</span></span>
    - <span data-ttu-id="e51e5-641">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="e51e5-641">Remove-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="e51e5-642">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="e51e5-642">Remove-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="e51e5-643">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="e51e5-643">Remove-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="e51e5-644">Remove-AzServiceFabricServic</span><span class="sxs-lookup"><span data-stu-id="e51e5-644">Remove-AzServiceFabricServic</span></span>
* <span data-ttu-id="e51e5-645">Service Fabric SDK가 Service Fabric 리소스 공급자 api 버전 2019-03-01을 사용하는 1.2.0 버전으로 업그레이드되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-645">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2019-03-01.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="e51e5-646">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="e51e5-646">Az.SignalR</span></span>
* <span data-ttu-id="e51e5-647">Update, Restart, CheckNameAvailability, GetUsage Cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-647">Add Update, Restart, CheckNameAvailability, GetUsage Cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="e51e5-648">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e51e5-648">Az.Sql</span></span>
* <span data-ttu-id="e51e5-649">'Get-AzSqlElasticPool'에 대한 참조 설명서의 예제가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-649">Update example in reference documentation for 'Get-AzSqlElasticPool'</span></span>
* <span data-ttu-id="e51e5-650">탄력적 풀을 만드는 vCore 예제가 추가되었습니다(AzSqlElasticPool).</span><span class="sxs-lookup"><span data-stu-id="e51e5-650">Added vCore example to creating an elastic pool (New-AzSqlElasticPool).</span></span>
* <span data-ttu-id="e51e5-651">Set-AzSqlServerAdvancedThreatProtectionPolicy 및 Set-AzSqlDatabaseAdvancedThreatProtectionPolicy에서 EmailAddresses가 비어 있는 경우 EmailAddresses의 유효성을 검사하고 EmailAdmins가 false가 아닌지 확인하는 기능이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-651">Remove the validation of EmailAddresses and the check that EmailAdmins is not false in case EmailAddresses is empty in Set-AzSqlServerAdvancedThreatProtectionPolicy and Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="e51e5-652">감사 범주를 사용하는 여러 진단 설정이 있는 경우 서버/데이터베이스 감사 설정을 제거하도록 설정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-652">Enabled removal of server/database auditing settings when multiple diagnostic settings that enable audit category exist.</span></span>
* <span data-ttu-id="e51e5-653">여러 Sql 취약성 평가 cmdlet에서 이메일 주소 유효성 검사가 수정되었습니다(Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting 및 Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span><span class="sxs-lookup"><span data-stu-id="e51e5-653">Fix email addresses validation in multiple Sql Vulnerability Assessment cmdlets (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting and Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span></span>

#### <a name="azstorage"></a><span data-ttu-id="e51e5-654">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="e51e5-654">Az.Storage</span></span>
* <span data-ttu-id="e51e5-655">'Get-AzStorageAccountKey'에 대한 참조 설명서의 예제가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-655">Updated example in reference documentation for 'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="e51e5-656">Azure 파일 업로드/다운에서, 원본 파일 SMB 속성(파일 특성, 파일 생성 시간, 파일을 마지막으로 쓴 시간)을 대상 파일에 보존하는 기능이 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-656">In upload/Downalod Azure File,support perserve the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the destination file</span></span>
    -  <span data-ttu-id="e51e5-657">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="e51e5-657">Set-AzStorageFileContent</span></span>
    -  <span data-ttu-id="e51e5-658">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="e51e5-658">Get-AzStorageFileContent</span></span>
* <span data-ttu-id="e51e5-659">컨테이너가 사용되는 ImmutabilityPolicy에서 properties/metadate fail을 사용하여 블록 Blob 업로드가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-659">Fix Upload block blob with properties/metadate fail on container enabled ImmutabilityPolicy.</span></span>
    -  <span data-ttu-id="e51e5-660">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="e51e5-660">Set-AzStorageBlobContent</span></span>
* <span data-ttu-id="e51e5-661">관리 평면 API를 사용하여 Azure 파일 공유 관리를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-661">Support manage Azure File shares with Management plane API</span></span>
    -  <span data-ttu-id="e51e5-662">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="e51e5-662">New-AzRmStorageShare</span></span>
    -  <span data-ttu-id="e51e5-663">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="e51e5-663">Get-AzRmStorageShare</span></span>
    -  <span data-ttu-id="e51e5-664">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="e51e5-664">Update-AzRmStorageShare</span></span>
    -  <span data-ttu-id="e51e5-665">Remove-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="e51e5-665">Remove-AzRmStorageShare</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="e51e5-666">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="e51e5-666">Az.Websites</span></span>
* <span data-ttu-id="e51e5-667">앱을 새 ASP로 마이그레이션할 때 웹앱 태그가 삭제되는 이슈가 해결되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-667">Fixing issue where webapp Tags were getting deleted when migrating App to new ASPwhere webapp Tags were getting deleted when migrating App to new ASP</span></span>
* <span data-ttu-id="e51e5-668">Linux와 Windows에서 모두 작동하도록 Publish-AzureWebapp이 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-668">Fixing the Publish-AzureWebapp to work across Linux and windows</span></span>
* <span data-ttu-id="e51e5-669">'Get-AzWebAppPublishingProfile' 참조 설명서의 예제가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-669">Update example in 'Get-AzWebAppPublishingProfile' reference documentation</span></span>

## <a name="260---august-2019"></a><span data-ttu-id="e51e5-670">2.6.0 - 2019년 8월</span><span class="sxs-lookup"><span data-stu-id="e51e5-670">2.6.0 - August 2019</span></span>
#### <a name="general"></a><span data-ttu-id="e51e5-671">일반</span><span class="sxs-lookup"><span data-stu-id="e51e5-671">General</span></span>
* <span data-ttu-id="e51e5-672">여러 모듈에서 기타 오타가 수정됨</span><span class="sxs-lookup"><span data-stu-id="e51e5-672">Fixed miscellaneous typos across numerous modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="e51e5-673">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e51e5-673">Az.Accounts</span></span>
* <span data-ttu-id="e51e5-674">Azure Functions 인증에서 사용자가 할당한 MSI가 지원됨(# 9479)</span><span class="sxs-lookup"><span data-stu-id="e51e5-674">Support user-assigned MSI in Azure Functiosn Authentication (#9479)</span></span>

#### <a name="azaks"></a><span data-ttu-id="e51e5-675">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="e51e5-675">Az.Aks</span></span>
* <span data-ttu-id="e51e5-676">'Get-AzAks' 출력 관련 문제가 해결됨</span><span class="sxs-lookup"><span data-stu-id="e51e5-676">Fix issue with output for 'Get-AzAks'</span></span>
    * <span data-ttu-id="e51e5-677">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/9847 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="e51e5-677">More information here: https://github.com/Azure/azure-powershell/issues/9847</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="e51e5-678">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="e51e5-678">Az.ApiManagement</span></span>
* <span data-ttu-id="e51e5-679">문제 https://github.com/Azure/azure-powershell/issues/9351 수정</span><span class="sxs-lookup"><span data-stu-id="e51e5-679">Fix for issue https://github.com/Azure/azure-powershell/issues/9351</span></span>
    - <span data-ttu-id="e51e5-680">productId, apiId, groupId 및 userId에 대한 제한을 적용하지 않는 .Net NuGet 버전이 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="e51e5-680">Update .net nuget version, which does not enforce restrictions on productId, apiId, groupId and userId</span></span>
* <span data-ttu-id="e51e5-681">**Get-AzApiManagementProduct** - API를 사용하는 제품에 대한 쿼리 지원이 추가됨</span><span class="sxs-lookup"><span data-stu-id="e51e5-681">**Get-AzApiManagementProduct** - Added support for querying products using Api.</span></span>
  https://github.com/Azure/azure-powershell/issues/9482
* <span data-ttu-id="e51e5-682">**New-AzApiManagementApiRevision** - 새 API 수정(https://github.com/Azure/azure-powershell/issues/9752 )을 만들 때 ApiRevisionDescription이 설정되지 않은 문제가 해결됨</span><span class="sxs-lookup"><span data-stu-id="e51e5-682">**New-AzApiManagementApiRevision** - Fix for issue where ApiRevisionDescription was not being set when creating new api revision https://github.com/Azure/azure-powershell/issues/9752</span></span>
* <span data-ttu-id="e51e5-683">'PsApiManagementOAuth2AuthrozationServer' 모델의 오타가 'PsApiManagementOAuth2AuthorizationServer'로 수정됨</span><span class="sxs-lookup"><span data-stu-id="e51e5-683">Fixed typo in model 'PsApiManagementOAuth2AuthrozationServer' to 'PsApiManagementOAuth2AuthorizationServer'</span></span>

#### <a name="azbatch"></a><span data-ttu-id="e51e5-684">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="e51e5-684">Az.Batch</span></span>
* <span data-ttu-id="e51e5-685">도움말 메시지 및 설명서에서 Windows를 대문자로 시작하도록 오타가 수정됨</span><span class="sxs-lookup"><span data-stu-id="e51e5-685">Fixed typo in help message and documentation to capitalize Windows</span></span>

#### <a name="azcdn"></a><span data-ttu-id="e51e5-686">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="e51e5-686">Az.Cdn</span></span>
* <span data-ttu-id="e51e5-687">CDN 모듈 변환 도우미의 오타가 수정됨</span><span class="sxs-lookup"><span data-stu-id="e51e5-687">Fixed a typo in CDN module conversion helper</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e51e5-688">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e51e5-688">Az.Compute</span></span>
* <span data-ttu-id="e51e5-689">VmssId가 New-AzVMConfig cmdlet에 추가됨</span><span class="sxs-lookup"><span data-stu-id="e51e5-689">Add VmssId to New-AzVMConfig cmdlet</span></span>
* <span data-ttu-id="e51e5-690">TerminateScheduledEvents 및 TerminateScheduledEventNotBeforeTimeoutInMinutes 매개 변수가 New-AzVmssConfig 및 Update-AzVmss에 추가됨</span><span class="sxs-lookup"><span data-stu-id="e51e5-690">Add TerminateScheduledEvents and TerminateScheduledEventNotBeforeTimeoutInMinutes parameters to New-AzVmssConfig and Update-AzVmss</span></span>
* <span data-ttu-id="e51e5-691">HyperVGeneration 속성이 VM 이미지 개체에 추가됨</span><span class="sxs-lookup"><span data-stu-id="e51e5-691">Add HyperVGeneration property to VM image object</span></span>
* <span data-ttu-id="e51e5-692">Host 및 HostGroup 기능이 추가됨</span><span class="sxs-lookup"><span data-stu-id="e51e5-692">Add Host and HostGroup features</span></span>
    - <span data-ttu-id="e51e5-693">새 cmdlet:   New-AzHostGroup, New-AzHost, Get-AzHostGroup, Get-AzHost, Remove-AzHostGroup, Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="e51e5-693">New cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span></span>
    - <span data-ttu-id="e51e5-694">HostId 매개 변수가 New-AzVMConfig 및 New-AzVM 추가됨</span><span class="sxs-lookup"><span data-stu-id="e51e5-694">HostId parameter is added to New-AzVMConfig and New-AzVM</span></span>
* <span data-ttu-id="e51e5-695">'Invoke-AzVMRunCommand' 설명서의 예제에서 올바른 매개 변수 이름을 사용하도록 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="e51e5-695">Update example in 'Invoke-AzVMRunCommand' documentation to use correct parameter name</span></span>
* <span data-ttu-id="e51e5-696">'Set-AzVMDiskEncryptionExtension' 및 'Set-AzVmssDiskEncryptionExtension' 참조 설명서의 '-VolumeType' 설명이 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="e51e5-696">Update '-VolumeType' description in 'Set-AzVMDiskEncryptionExtension' and 'Set-AzVmssDiskEncryptionExtension' reference documentation</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="e51e5-697">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="e51e5-697">Az.DataFactory</span></span>
* <span data-ttu-id="e51e5-698">'New-AzDataFactoryEncryptValue' 설명서에서 'Windows'를 대문자로 시작하도록 오타가 수정됨</span><span class="sxs-lookup"><span data-stu-id="e51e5-698">Fix typo to capitalize 'Windows' in 'New-AzDataFactoryEncryptValue' documentation</span></span>
* <span data-ttu-id="e51e5-699">ADF .Net SDK 버전이 4.1.2로 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="e51e5-699">Updated ADF .Net SDK version to 4.1.2</span></span>
* <span data-ttu-id="e51e5-700">자체 호스팅 통합 런타임을 SSIS Integration Runtime의 프록시로 설정할 수 있도록 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' 및 'DataProxyStagingPath' 매개 변수가 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd에 추가됨</span><span class="sxs-lookup"><span data-stu-id="e51e5-700">Add parameter 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' and 'DataProxyStagingPath' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable set up Self-Hosted Integration Runtime as a proxy for SSIS Integration Runtime</span></span>
* <span data-ttu-id="e51e5-701">PSTriggerRun에서 트리거된 파이프라인, 메시지 및 속성을 표시하고, PSActivityRun에서 작업 유형을 표시하도록 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="e51e5-701">Updated PSTriggerRun to show the triggered pipelines, message and properties, and PSActivityRun to show the activity type</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="e51e5-702">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="e51e5-702">Az.DataLakeStore</span></span>
* <span data-ttu-id="e51e5-703">오류 또는 원격 예외에 대한 Get-DataLakeStoreDeletedItem 중단이 수정됨</span><span class="sxs-lookup"><span data-stu-id="e51e5-703">Fix hanging of Get-DataLakeStoreDeletedItem for any errors or remote exceptions.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="e51e5-704">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="e51e5-704">Az.EventHub</span></span>
* <span data-ttu-id="e51e5-705">#9658 문제 해결: Set-AzEventHubNetworkRuleSet의 VirtualNteworkRule 매개 변수에 대한 오타</span><span class="sxs-lookup"><span data-stu-id="e51e5-705">Fix for issue #9658 : Typo VirtualNteworkRule parameter in Set-AzEventHubNetworkRuleSet</span></span>
* <span data-ttu-id="e51e5-706">#9558 문제 해결: Set-AzEventHubNamespace에서 PUT 대신 PATCH가 사용됨</span><span class="sxs-lookup"><span data-stu-id="e51e5-706">Fix for issue #9558 : Set-AzEventHubNamespace is using PATCH instead of PUT</span></span>
* <span data-ttu-id="e51e5-707">EnableKafka 매개 변수가 Set-AzEventHubNamespace cmdlet에 추가됨</span><span class="sxs-lookup"><span data-stu-id="e51e5-707">added EnableKafka parameter to Set-AzEventHubNamespace cmdlet</span></span>
* <span data-ttu-id="e51e5-708">#9786 문제 해결: Listen(수신 대기) 전용 권한이 있는 규칙을 만들 수 없음</span><span class="sxs-lookup"><span data-stu-id="e51e5-708">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>

#### <a name="azmarketplaceordering"></a><span data-ttu-id="e51e5-709">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="e51e5-709">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="e51e5-710">'Azure'가 모두 소문자인 설명서의 오타가 수정됨</span><span class="sxs-lookup"><span data-stu-id="e51e5-710">Fixed documentation typo where 'Azure' was all lowercase letters</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="e51e5-711">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="e51e5-711">Az.Monitor</span></span>
* <span data-ttu-id="e51e5-712">도움말 설명서에서 잘못된 매개 변수 이름이 수정됨</span><span class="sxs-lookup"><span data-stu-id="e51e5-712">Fixed incorrect parameter name in help documentation</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e51e5-713">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e51e5-713">Az.Network</span></span>
* <span data-ttu-id="e51e5-714">New-AzPrivateLinkServiceIpConfig가 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="e51e5-714">Updated New-AzPrivateLinkServiceIpConfig</span></span>
    - <span data-ttu-id="e51e5-715">서버 쪽에서 사용되지 않으므로 'PublicIpAddress' 매개 변수가 사용되지 않음</span><span class="sxs-lookup"><span data-stu-id="e51e5-715">Deprecated the paramster 'PublicIpAddress' since this is never used in the server side.</span></span>
    - <span data-ttu-id="e51e5-716">현재 IP 구성이 기본 구성인지 여부를 나타내는 하나의 선택적 'Primary' 매개 변수가 추가됨</span><span class="sxs-lookup"><span data-stu-id="e51e5-716">Added one optional parameter 'Primary' that indicate the current ip configuration is primary one or not.</span></span>
* <span data-ttu-id="e51e5-717">SDK의 요청 오류 예외 처리가 향상됨 - 이전의 SDK 예외가 올바르게 처리되지 않아 주요 오류 세부 정보가 표시되지 않은 문제가 해결됨</span><span class="sxs-lookup"><span data-stu-id="e51e5-717">Improved handling of request error exception from SDK   -Fixes the issue that previously SDK exceptions aren't handled correctly which results in key error details not being displayed</span></span>
* <span data-ttu-id="e51e5-718">올바른 IPv6 접두사 길이를 확인하기 위해 Ipv6 IP 접두사에 대한 유효성 검사 논리가 조정됨</span><span class="sxs-lookup"><span data-stu-id="e51e5-718">Adjusted validation logic for Ipv6 IP Prefix to check for correct IPv6 prefix length.</span></span> 
* <span data-ttu-id="e51e5-719">Get-AzVirtualNetworkSubnetConfig가 업데이트됨: 서브넷 리소스 ID별로 가져오도록 설정되는 매개 변수 세트가 추가됨</span><span class="sxs-lookup"><span data-stu-id="e51e5-719">Updated Get-AzVirtualNetworkSubnetConfig: Added parameter set to get by subnet resource id.</span></span>
* <span data-ttu-id="e51e5-720">AzNetworkServiceTag의 Location(위치) 매개 변수에 대한 설명이 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="e51e5-720">Updated description of Location parameter for AzNetworkServiceTag</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="e51e5-721">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="e51e5-721">Az.OperationalInsights</span></span>
* <span data-ttu-id="e51e5-722">'New-AzOperationalInsightsLinuxSyslogDataSource'에 대한 설명서가 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="e51e5-722">Updated documentation for 'New-AzOperationalInsightsLinuxSyslogDataSource'</span></span>
    - <span data-ttu-id="e51e5-723">예제가 추가됨</span><span class="sxs-lookup"><span data-stu-id="e51e5-723">Added example</span></span>
    - <span data-ttu-id="e51e5-724">'-Name' 매개 변수에 대한 설명이 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="e51e5-724">Updated description for '-Name' parameter</span></span>
* <span data-ttu-id="e51e5-725">New-AzOperationalInsightsWindowsEventDataSource에 대한 예제가 추가됨</span><span class="sxs-lookup"><span data-stu-id="e51e5-725">Added an example for New-AzOperationalInsightsWindowsEventDataSource</span></span>
* <span data-ttu-id="e51e5-726">New-AzOperationalInsightsWindowsEventDataSource의 -Name 매개 변수에 대한 설명이 변경됨</span><span class="sxs-lookup"><span data-stu-id="e51e5-726">Changed the description of the -Name parameter for New-AzOperationalInsightsWindowsEventDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="e51e5-727">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="e51e5-727">Az.RecoveryServices</span></span>
* <span data-ttu-id="e51e5-728">'Get-AzRecoveryServicesBackupJobDetail.md'가 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="e51e5-728">Update 'Get-AzRecoveryServicesBackupJobDetail.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="e51e5-729">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e51e5-729">Az.Resources</span></span>
* <span data-ttu-id="e51e5-730">Microsoft 리소스에 대한 새 2019-05-10 API 버전 지원이 추가됨</span><span class="sxs-lookup"><span data-stu-id="e51e5-730">Add support for new api version 2019-05-10 for Microsoft.Resource</span></span>
    - <span data-ttu-id="e51e5-731">변수, 리소스 및 속성에 대한 'copy.count = 0' 지원이 추가됨</span><span class="sxs-lookup"><span data-stu-id="e51e5-731">Add support for 'copy.count = 0' for variables, resources and properties</span></span>
    - <span data-ttu-id="e51e5-732">'condition = false' 또는 'copy.count = 0'인 리소스가 완료 모드에서 삭제됨</span><span class="sxs-lookup"><span data-stu-id="e51e5-732">Resources with 'condition = false' or 'copy.count = 0' will be deleted in complete mode</span></span>
* <span data-ttu-id="e51e5-733">정책을 구독 수준에서 도움말 문서에 할당하는 예제가 추가됨</span><span class="sxs-lookup"><span data-stu-id="e51e5-733">Add an example of assigning policy at subscription level to help doc</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="e51e5-734">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="e51e5-734">Az.ServiceBus</span></span>
* <span data-ttu-id="e51e5-735">#9658 문제 해결: Set-AzServiceBusNetworkRuleSet의 VirtualNetworkRule 매개 변수에 대한 오타</span><span class="sxs-lookup"><span data-stu-id="e51e5-735">Fix for issue #9658 : Typo VirtualNetworkRule parameter in Set-AzServiceBusNetworkRuleSet</span></span>
* <span data-ttu-id="e51e5-736">#9786 문제 해결: Listen(수신 대기) 전용 권한이 있는 규칙을 만들 수 없음</span><span class="sxs-lookup"><span data-stu-id="e51e5-736">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>
* <span data-ttu-id="e51e5-737">큐 및 토픽에 대한 이름 가용성을 확인하는 새 'Test-AzServiceBusNameAvailability' 명령이 추가됨</span><span class="sxs-lookup"><span data-stu-id="e51e5-737">Added new command 'Test-AzServiceBusNameAvailability' to check the name availability for queue and topic</span></span> 

#### <a name="azservicefabric"></a><span data-ttu-id="e51e5-738">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="e51e5-738">Az.ServiceFabric</span></span>
* <span data-ttu-id="e51e5-739">노드 유형 추가 cmdlet 버그 수정:</span><span class="sxs-lookup"><span data-stu-id="e51e5-739">Fix add node type cmdlet bugs:</span></span>
    - <span data-ttu-id="e51e5-740">서비스 패브릭 클러스터와 관련이 없는 다른 vmss가 리소스 그룹에 있을 때 발생하는 NullReferenceException 버그</span><span class="sxs-lookup"><span data-stu-id="e51e5-740">NullReferenceException bug when resource group had other vmss not related to the service fabric cluster.</span></span> <span data-ttu-id="e51e5-741">문제 해결: https://github.com/Azure/azure-powershell/issues/8681</span><span class="sxs-lookup"><span data-stu-id="e51e5-741">Fixes issue: https://github.com/Azure/azure-powershell/issues/8681</span></span>
    - <span data-ttu-id="e51e5-742">virtualNetwork가 클러스터의 다른 리소스 그룹에 있을 때 cmdlet이 실패하는 버그가 수정됨</span><span class="sxs-lookup"><span data-stu-id="e51e5-742">Fix bug where cmdlet failed if virtualNetwork was in a different resource group that the cluster.</span></span> <span data-ttu-id="e51e5-743">문제 해결: https://github.com/Azure/azure-powershell/issues/8407</span><span class="sxs-lookup"><span data-stu-id="e51e5-743">fixes issue: https://github.com/Azure/azure-powershell/issues/8407</span></span>
    - <span data-ttu-id="e51e5-744">Add-AzServiceFabricApplicationCertificate cmdlet이 사용되지 않음</span><span class="sxs-lookup"><span data-stu-id="e51e5-744">Deprecating Add-AzServiceFabricApplicationCertificate cmdlet</span></span>

#### <a name="azsql"></a><span data-ttu-id="e51e5-745">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e51e5-745">Az.Sql</span></span>
* <span data-ttu-id="e51e5-746">이전의 Auditing(감사) cmdlet에 대한 설명서가 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="e51e5-746">Update documentation of old Auditing cmdlets.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="e51e5-747">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="e51e5-747">Az.Storage</span></span>
* <span data-ttu-id="e51e5-748">더 많은 시나리오를 cmdlet 예제에 추가하고 매개 변수 설명을 업데이트하여 Get/Close-AzStorageFileHandle에 대한 도움말이 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="e51e5-748">Update help for Get/Close-AzStorageFileHandle, by add more scenarios to cmdlet examples and update parameter descriptions</span></span>
* <span data-ttu-id="e51e5-749">Blob 업로드 및 Blob 복사에서 StandardBlobTier가 지원됨</span><span class="sxs-lookup"><span data-stu-id="e51e5-749">Support StandardBlobTier in upload blob and copy blob</span></span>
    -  <span data-ttu-id="e51e5-750">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="e51e5-750">Set-AzStorageBlobContent</span></span>
    -  <span data-ttu-id="e51e5-751">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="e51e5-751">Start-AzStorageBlobCopy</span></span>
* <span data-ttu-id="e51e5-752">Blob 복사에서 우선 순위 리하이드레이션이 지원됨</span><span class="sxs-lookup"><span data-stu-id="e51e5-752">Support Rehydrate Priority in copy blob</span></span>
    -  <span data-ttu-id="e51e5-753">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="e51e5-753">Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="e51e5-754">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="e51e5-754">Az.Websites</span></span>
* <span data-ttu-id="e51e5-755">Set-AzWebApp 및 Set-AzWebAppSlot에서 -AppSettings 매개 변수에 대한 설명이 추가됨</span><span class="sxs-lookup"><span data-stu-id="e51e5-755">Add clarification around -AppSettings parameter in Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <a name="250---july-2019"></a><span data-ttu-id="e51e5-756">2.5.0 - 2019년 7월</span><span class="sxs-lookup"><span data-stu-id="e51e5-756">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="e51e5-757">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e51e5-757">Az.Accounts</span></span>
* <span data-ttu-id="e51e5-758">ClientRuntime의 최신 버전을 사용하도록 일반적인 코드를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-758">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="e51e5-759">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="e51e5-759">Az.ApplicationInsights</span></span>
* <span data-ttu-id="e51e5-760">'Remove-AzApplicationInsightsApiKey' 설명서의 예제 오타 수정</span><span class="sxs-lookup"><span data-stu-id="e51e5-760">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span> 

#### <a name="azautomation"></a><span data-ttu-id="e51e5-761">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="e51e5-761">Az.Automation</span></span>
* <span data-ttu-id="e51e5-762">리소스 문자열의 오타 수정</span><span class="sxs-lookup"><span data-stu-id="e51e5-762">Fix typo in resource string</span></span> 

#### <a name="azcognitiveservices"></a><span data-ttu-id="e51e5-763">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="e51e5-763">Az.CognitiveServices</span></span>
* <span data-ttu-id="e51e5-764">NetworkRuleSet 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-764">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e51e5-765">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e51e5-765">Az.Compute</span></span>
* <span data-ttu-id="e51e5-766">VM 인스턴스 보기 개체의 누락된 속성(ComputerName, OsName, OsVersion 및 HyperVGeneration)을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-766">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="e51e5-767">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="e51e5-767">Az.ContainerRegistry</span></span>
* <span data-ttu-id="e51e5-768">복제 매개 변수의 Remove-AzContainerRegistryReplication에서 오타 수정</span><span class="sxs-lookup"><span data-stu-id="e51e5-768">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="e51e5-769">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/9633 을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="e51e5-769">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="e51e5-770">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="e51e5-770">Az.DataFactory</span></span>
* <span data-ttu-id="e51e5-771">ADF .Net SDK 버전을 4.1.0으로 업데이트</span><span class="sxs-lookup"><span data-stu-id="e51e5-771">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="e51e5-772">'Get-AzDataFactoryV2PipelineRun' 설명서의 오타 수정</span><span class="sxs-lookup"><span data-stu-id="e51e5-772">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="e51e5-773">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="e51e5-773">Az.EventHub</span></span>
* <span data-ttu-id="e51e5-774">SAS 토큰을 생성하기 위해 추가된 새로운 cmmdlet 추가: New-AzEventHubAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="e51e5-774">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="e51e5-775">'관리'만 지정된 경우 authorizationrules 권한에 대한 확인 및 오류 메시지 추가</span><span class="sxs-lookup"><span data-stu-id="e51e5-775">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="e51e5-776">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="e51e5-776">Az.KeyVault</span></span>
* <span data-ttu-id="e51e5-777">인증서 정책에 대한 KeySize 지정을 위한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="e51e5-777">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="e51e5-778">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="e51e5-778">Az.LogicApp</span></span>
* <span data-ttu-id="e51e5-779">모든 맵 유형을 나열하도록 Get-AzIntegrationAccountMap 수정</span><span class="sxs-lookup"><span data-stu-id="e51e5-779">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="e51e5-780">필터링을 위해 새 MapType 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="e51e5-780">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="e51e5-781">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="e51e5-781">Az.ManagedServices</span></span>
* <span data-ttu-id="e51e5-782">API 버전 2019-06-01(GA)에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="e51e5-782">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e51e5-783">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e51e5-783">Az.Network</span></span>
* <span data-ttu-id="e51e5-784">프라이빗 엔드포인트 및 프라이빗 링크 서비스에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="e51e5-784">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="e51e5-785">새로운 cmdlet</span><span class="sxs-lookup"><span data-stu-id="e51e5-785">New cmdlets</span></span>
        - <span data-ttu-id="e51e5-786">Set-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="e51e5-786">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="e51e5-787">Set-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="e51e5-787">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="e51e5-788">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="e51e5-788">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="e51e5-789">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="e51e5-789">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="e51e5-790">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="e51e5-790">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="e51e5-791">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="e51e5-791">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="e51e5-792">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="e51e5-792">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="e51e5-793">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="e51e5-793">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="e51e5-794">기능에 대한 새로운 명령이 업데이트됨: Virtualnetwork의 서브넷에 있는 PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies 플래그</span><span class="sxs-lookup"><span data-stu-id="e51e5-794">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="e51e5-795">업데이트된 New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="e51e5-795">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="e51e5-796">이 서브넷의 프라이빗 엔드포인트에 네트워크 정책을 적용할지 여부를 나타내는 선택적 매개 변수 -PrivateEndpointNetworkPoliciesFlag가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-796">Added optional parameter -PrivateEndpointNetworkPoliciesFlag that configures whether to apply network policies on private endpoint in this subnet.</span></span>
        - <span data-ttu-id="e51e5-797">이 서브넷의 프라이빗 연결 서비스에 네트워크 정책을 적용할지 여부를 나타내는 선택적 매개 변수 -PrivateLinkServiceNetworkPoliciesFlag가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-797">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag that configures whether to apply network policies network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="e51e5-798">AzPrivateLinkService의 cmdlet 매개 변수 'ServiceName'이 이전 버전과의 호환성을 위해 별칭 'ServiceName'을 사용한 'Name'으로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-798">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="e51e5-799">네트워크 보안 규칙 구성에 ICMP 프로토콜 사용</span><span class="sxs-lookup"><span data-stu-id="e51e5-799">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="e51e5-800">다음 Cmdlet이 업데이트 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-800">Updated cmdlets</span></span>
        - <span data-ttu-id="e51e5-801">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e51e5-801">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="e51e5-802">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e51e5-802">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="e51e5-803">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e51e5-803">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="e51e5-804">New-AzVirtualNetworkGatewayConnection에 대한 구성 가능한 매개 변수로 ConnectionProtocolType (Ikev1/Ikev2) 추가</span><span class="sxs-lookup"><span data-stu-id="e51e5-804">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="e51e5-805">LoadBalancerFrontendIpConfiguration에 PrivateIpAddressVersion 추가</span><span class="sxs-lookup"><span data-stu-id="e51e5-805">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="e51e5-806">업데이트된 cmdlet:</span><span class="sxs-lookup"><span data-stu-id="e51e5-806">Updated cmdlet:</span></span>
        - <span data-ttu-id="e51e5-807">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="e51e5-807">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="e51e5-808">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="e51e5-808">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="e51e5-809">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="e51e5-809">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="e51e5-810">프로브에서 사용자 지정 포트를 지원하기 위한 Application Gateway New-AzApplicationGatewayProbeConfig 명령 업데이트</span><span class="sxs-lookup"><span data-stu-id="e51e5-810">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="e51e5-811">업데이트된 New-AzApplicationGatewayProbeConfig: 백 엔드 서버 검색에 사용되는 선택적 매개 변수 포트가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-811">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="e51e5-812">이 매개 변수는 Standard_V2 및 WAF_V2 SKU에 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-812">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="e51e5-813">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="e51e5-813">Az.OperationalInsights</span></span>
* <span data-ttu-id="e51e5-814">저장된 검색의 기본 버전이 1로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-814">Updated default version for saved searches to be 1.</span></span> 
* <span data-ttu-id="e51e5-815">사용자 지정 로그 null regex 처리가 수정됨</span><span class="sxs-lookup"><span data-stu-id="e51e5-815">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="e51e5-816">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="e51e5-816">Az.RecoveryServices</span></span>
* <span data-ttu-id="e51e5-817">'Get-AzRecoveryServicesBackupJob.md' 업데이트</span><span class="sxs-lookup"><span data-stu-id="e51e5-817">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="e51e5-818">'Get-AzRecoveryServicesBackupContainer.md' 업데이트</span><span class="sxs-lookup"><span data-stu-id="e51e5-818">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="e51e5-819">'Get-AzRecoveryServicesVault.md' 업데이트</span><span class="sxs-lookup"><span data-stu-id="e51e5-819">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="e51e5-820">'Wait-AzRecoveryServicesBackupJob.md' 업데이트</span><span class="sxs-lookup"><span data-stu-id="e51e5-820">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="e51e5-821">'Set-AzRecoveryServicesVaultContext.md' 업데이트</span><span class="sxs-lookup"><span data-stu-id="e51e5-821">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="e51e5-822">'Get-AzRecoveryServicesBackupItem.md' 업데이트</span><span class="sxs-lookup"><span data-stu-id="e51e5-822">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="e51e5-823">'Get-AzRecoveryServicesBackupRecoveryPoint.md' 업데이트</span><span class="sxs-lookup"><span data-stu-id="e51e5-823">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="e51e5-824">'Restore-AzRecoveryServicesBackupItem.md' 업데이트</span><span class="sxs-lookup"><span data-stu-id="e51e5-824">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="e51e5-825">Azure 파일 공유용 컨테이너를 등록 취소하기 위해 서비스 요청 업데이트</span><span class="sxs-lookup"><span data-stu-id="e51e5-825">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="e51e5-826">'Set-AzRecoveryServicesAsrAlertSetting.md' 업데이트</span><span class="sxs-lookup"><span data-stu-id="e51e5-826">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="e51e5-827">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e51e5-827">Az.Resources</span></span>
- <span data-ttu-id="e51e5-828">'New-AzResourceGroupDeployment' 설명서에서 참조된 누락 cmdlet 제거</span><span class="sxs-lookup"><span data-stu-id="e51e5-828">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="e51e5-829">새 API 버전 2019-01-01을 사용하도록 정책 cmdlet 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="e51e5-829">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="e51e5-830">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="e51e5-830">Az.ServiceBus</span></span>
* <span data-ttu-id="e51e5-831">SAS 토큰을 생성하기 위해 추가된 새로운 cmmdlet 추가: New-AzServiceBusAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="e51e5-831">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="e51e5-832">'관리'만 지정된 경우 authorizationrules 권한에 대한 확인 및 오류 메시지 추가</span><span class="sxs-lookup"><span data-stu-id="e51e5-832">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="e51e5-833">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e51e5-833">Az.Sql</span></span>
* <span data-ttu-id="e51e5-834">Set-AzSqlDatabaseSecondary cmdlet에 대한 누락된 예제 수정</span><span class="sxs-lookup"><span data-stu-id="e51e5-834">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="e51e5-835">이메일 주소를 제공하지 않고 설정된 취약성 평가 반복 검색 수정</span><span class="sxs-lookup"><span data-stu-id="e51e5-835">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="e51e5-836">경고 메시지의 작은 오타를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-836">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="e51e5-837">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="e51e5-837">Az.Storage</span></span>
* <span data-ttu-id="e51e5-838">'Get-AzStorageAccount'에 대한 참조 설명서의 예제를 업데이트하여 올바른 매개 변수 이름 사용</span><span class="sxs-lookup"><span data-stu-id="e51e5-838">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="e51e5-839">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="e51e5-839">Az.StorageSync</span></span>
* <span data-ttu-id="e51e5-840">Invoke-AzStorageSyncChangeDetection cmdlet을 추가하는 중입니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-840">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="e51e5-841">TierFilesOlderThanDays를 기념하는 문제 9551 수정</span><span class="sxs-lookup"><span data-stu-id="e51e5-841">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="e51e5-842">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="e51e5-842">Az.Websites</span></span>
* <span data-ttu-id="e51e5-843">Get-AzWebApp 및 Set-AzWebApp에서 일부 SiteConfig 속성을 반환하지 않은 버그 수정</span><span class="sxs-lookup"><span data-stu-id="e51e5-843">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="e51e5-844">Get-AzDeletedWebApp 및 Restore-AzDeletedWebApp에 새 위치 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="e51e5-844">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="e51e5-845">AzWebApp-IncludeSourceWebAppSlots을 사용하여 웹앱 슬롯을 복제하는 버그를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-845">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="e51e5-846">2.4.0 - 2019년 7월</span><span class="sxs-lookup"><span data-stu-id="e51e5-846">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="e51e5-847">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e51e5-847">Az.Accounts</span></span>
* <span data-ttu-id="e51e5-848">프로필 cmdlet에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="e51e5-848">Add support for profile cmdlets</span></span>
* <span data-ttu-id="e51e5-849">생성된 cmdlet에서 환경 및 데이터 평면에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="e51e5-849">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="e51e5-850">Windows PowerShell의 데이터 평면 cmdlet에대해 일부 경우 잘못된 엔드포인트가 사용되는 버그 수정</span><span class="sxs-lookup"><span data-stu-id="e51e5-850">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="e51e5-851">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="e51e5-851">Az.Advisor</span></span>
* <span data-ttu-id="e51e5-852">Az.Advisor의 GA 릴리스</span><span class="sxs-lookup"><span data-stu-id="e51e5-852">GA release of Az.Advisor</span></span>
* <span data-ttu-id="e51e5-853">이 모듈은 이제 롤업 `Az` 모듈의 일부로 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-853">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="e51e5-854">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="e51e5-854">Az.ApiManagement</span></span>
* <span data-ttu-id="e51e5-855">문제 https://github.com/Azure/azure-powershell/issues/8671 수정</span><span class="sxs-lookup"><span data-stu-id="e51e5-855">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="e51e5-856">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="e51e5-856">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="e51e5-857">사용자 및 제품별 구독을 쿼리하기 위한 지원이 추가됨</span><span class="sxs-lookup"><span data-stu-id="e51e5-857">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="e51e5-858">범위 '/', '/ api, '/ api/echo api'를 사용하여 쿼리하기 위한 지원이 추가됨</span><span class="sxs-lookup"><span data-stu-id="e51e5-858">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="e51e5-859">[https://github.com/Azure/azure-powershell/issues/9307](https://github.com/Azure/azure-powershell/issues/9307 ) 및 https://github.com/Azure/azure-powershell/issues/8432 문제 수정</span><span class="sxs-lookup"><span data-stu-id="e51e5-859">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="e51e5-860">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="e51e5-860">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="e51e5-861">Apis를 가져올 때 'ApiVersion' 및 'ApiVersionSetId'를 지정하기 위한 지원이 추가됨</span><span class="sxs-lookup"><span data-stu-id="e51e5-861">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="e51e5-862">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="e51e5-862">Az.Automation</span></span>
* <span data-ttu-id="e51e5-863">문자열 값을 처리하기 위해 Set-AzAutomationConnectionFieldValue cmdlet 버그를 수정했습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-863">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e51e5-864">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e51e5-864">Az.Compute</span></span>
* <span data-ttu-id="e51e5-865">New-AzImageConfig에 HyperVGeneration 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="e51e5-865">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="e51e5-866">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="e51e5-866">Az.DataFactory</span></span>
* <span data-ttu-id="e51e5-867">get activity runs, get pipeline runs, get trigger runs ADF cmdlet의 출력을 업데이트하여 Select-Object pipe를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-867">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="e51e5-868">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="e51e5-868">Az.EventGrid</span></span>
* <span data-ttu-id="e51e5-869">'New-AzEventGridSubcription' 설명서의 오타 수정</span><span class="sxs-lookup"><span data-stu-id="e51e5-869">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="e51e5-870">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="e51e5-870">Az.IotHub</span></span>
* <span data-ttu-id="e51e5-871">권한 부여 정책 키를 다시 생성하기 위한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="e51e5-871">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e51e5-872">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e51e5-872">Az.Network</span></span>
* <span data-ttu-id="e51e5-873">'RoutingPreference'를 공용 IP 태그에 추가함</span><span class="sxs-lookup"><span data-stu-id="e51e5-873">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="e51e5-874">'Get-AzNetworkServiceTag' 참조 설명서의 예제 개선</span><span class="sxs-lookup"><span data-stu-id="e51e5-874">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="e51e5-875">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="e51e5-875">Az.PolicyInsights</span></span>
* <span data-ttu-id="e51e5-876">Get-AzPolicyState의 null 참조 문제 해결</span><span class="sxs-lookup"><span data-stu-id="e51e5-876">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="e51e5-877">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/9446 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="e51e5-877">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="e51e5-878">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="e51e5-878">Az.OperationalInsights</span></span>
* <span data-ttu-id="e51e5-879">Get-AzOperationalInsightsDataSource에 반환된 CustomLog datasource 모델 수정됨</span><span class="sxs-lookup"><span data-stu-id="e51e5-879">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="e51e5-880">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="e51e5-880">Az.RecoveryServices</span></span>
* <span data-ttu-id="e51e5-881">IaaSVMs에 대한 get-policy 명령 수정</span><span class="sxs-lookup"><span data-stu-id="e51e5-881">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="e51e5-882">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e51e5-882">Az.Resources</span></span>
    - <span data-ttu-id="e51e5-883">Get-AzPolicyState -Top 매개 변수에 대한 도움말 텍스트 수정</span><span class="sxs-lookup"><span data-stu-id="e51e5-883">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="e51e5-884">Get-AzPolicyAlias에 대한 클라이언트 쪽 페이징 지원 추가</span><span class="sxs-lookup"><span data-stu-id="e51e5-884">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="e51e5-885">Set-AzPolicyAssignment, -PolicyParameters 및 -PolicyParametersObject에 대한 새 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="e51e5-885">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="e51e5-886">Policy cmdlet에 대한 몇 가지 문서 및 예제 업데이트</span><span class="sxs-lookup"><span data-stu-id="e51e5-886">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="e51e5-887">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="e51e5-887">Az.ServiceBus</span></span>
* <span data-ttu-id="e51e5-888">문제 #4938 수정 - MaxSizeInMegabytes를 설정할 때 New-AzureRmServiceBusQueue가 BadRequest 반환</span><span class="sxs-lookup"><span data-stu-id="e51e5-888">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="e51e5-889">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e51e5-889">Az.Sql</span></span>
* <span data-ttu-id="e51e5-890">미리 보기 릴리스에서 공개 릴리스로 인스턴스 장애 조치(Failover) 그룹 cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="e51e5-890">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="e51e5-891">새 cmdlet으로 Azure SQL Server\Database Auditing을 지원하세요.</span><span class="sxs-lookup"><span data-stu-id="e51e5-891">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="e51e5-892">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="e51e5-892">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="e51e5-893">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="e51e5-893">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="e51e5-894">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="e51e5-894">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="e51e5-895">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="e51e5-895">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="e51e5-896">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="e51e5-896">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="e51e5-897">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="e51e5-897">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="e51e5-898">취약성 평가 설정에서 이메일 제약 조건 제거</span><span class="sxs-lookup"><span data-stu-id="e51e5-898">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="e51e5-899">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="e51e5-899">Az.Storage</span></span>
* <span data-ttu-id="e51e5-900">다음 cmdlet에서 2개의 매개 변수 '-IndexDocument' 및 '-ErrorDocument404Path'를 필수에서 선택으로 변경하세요.</span><span class="sxs-lookup"><span data-stu-id="e51e5-900">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="e51e5-901">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="e51e5-901">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="e51e5-902">예제를 추가하여 Get-AzStorageBlobContent의 도움말 업데이트</span><span class="sxs-lookup"><span data-stu-id="e51e5-902">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="e51e5-903">StorageException으로 cmdlet이 실패한 경우 자세한 오류 정보 표시</span><span class="sxs-lookup"><span data-stu-id="e51e5-903">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="e51e5-904">Azure Files AAD DS 인증으로 스토리지 계정 생성 또는 업데이트 지원</span><span class="sxs-lookup"><span data-stu-id="e51e5-904">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="e51e5-905">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="e51e5-905">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="e51e5-906">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="e51e5-906">Set-AzStorageAccount</span></span>
* <span data-ttu-id="e51e5-907">파일 공유, 파일 디렉터리 또는 파일의 목록 지원 또는 파일 핸들 닫기</span><span class="sxs-lookup"><span data-stu-id="e51e5-907">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="e51e5-908">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="e51e5-908">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="e51e5-909">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="e51e5-909">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="e51e5-910">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="e51e5-910">Az.StorageSync</span></span>
* <span data-ttu-id="e51e5-911">이 모듈은 이제 롤업 `Az` 모듈의 일부로 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-911">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="e51e5-912">2.3.2 - 2019년 6월</span><span class="sxs-lookup"><span data-stu-id="e51e5-912">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="e51e5-913">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e51e5-913">Az.Accounts</span></span>
* <span data-ttu-id="e51e5-914">함수 호출에 대해 일부 경우 잘못된 URL이 사용되는 버그 수정</span><span class="sxs-lookup"><span data-stu-id="e51e5-914">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="e51e5-915">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/8983 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="e51e5-915">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="e51e5-916">AzureRM에서 Az cmdlet으로의 별칭 문제 해결</span><span class="sxs-lookup"><span data-stu-id="e51e5-916">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="e51e5-917">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="e51e5-917">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="e51e5-918">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="e51e5-918">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e51e5-919">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e51e5-919">Az.Compute</span></span>
* <span data-ttu-id="e51e5-920">New-AzVm 및 New-AzVmss 단순 매개 변수 집합은 이제 'ProximityPlacementGroup'매개 변수를 허용합니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-920">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="e51e5-921">'New-AzVM' 참조 설명서에서 오타 수정</span><span class="sxs-lookup"><span data-stu-id="e51e5-921">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="e51e5-922">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="e51e5-922">Az.Dns</span></span>
* <span data-ttu-id="e51e5-923">'Set-AzDnsZone' 도움말 예제의 오타가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-923">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="e51e5-924">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="e51e5-924">Az.EventGrid</span></span>
* <span data-ttu-id="e51e5-925">2019-06-01 API 버전을 사용하도록 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-925">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="e51e5-926">새 cmdlet:</span><span class="sxs-lookup"><span data-stu-id="e51e5-926">New cmdlets:</span></span>
    - <span data-ttu-id="e51e5-927">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="e51e5-927">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="e51e5-928">새 Azure Event Grid 도메인을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-928">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="e51e5-929">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="e51e5-929">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="e51e5-930">Event Grid 도메인의 세부 정보를 가져오거나 현재 Azure 구독의 모든 Event Grid 도메인 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-930">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="e51e5-931">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="e51e5-931">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="e51e5-932">Azure Event Grid 도메인을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-932">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="e51e5-933">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="e51e5-933">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="e51e5-934">Azure Event Grid 도메인에 대한 공유 액세스 키를 다시 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-934">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="e51e5-935">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="e51e5-935">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="e51e5-936">Event Grid 도메인 이벤트를 게시하는 데 사용되는 공유 액세스 키를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-936">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="e51e5-937">New-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="e51e5-937">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="e51e5-938">새 Azure Event Grid 도메인 토픽을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-938">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="e51e5-939">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="e51e5-939">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="e51e5-940">Event Grid 도메인 토픽의 세부 사항을 가져오거나, 현재 Azure의 특정 Event Grid 도메인 아래의 모든 Event Grid 도메인 토픽 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-940">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span> 
    - <span data-ttu-id="e51e5-941">Remove-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="e51e5-941">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="e51e5-942">기존 Azure Event Grid 도메인 토픽을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-942">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="e51e5-943">다음 Cmdlet이 업데이트 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-943">Updated cmdlets:</span></span>
    - <span data-ttu-id="e51e5-944">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="e51e5-944">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="e51e5-945">새로운 Event Grid 도메인 및 Event Grid 도메인 토픽에 대한 파이핑을 지원하기 위해 새로운 필수 매개 변수를 추가하여 이러한 리소스 아래에 새 이벤트 구독을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-945">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="e51e5-946">새로운 Event Grid 도메인 이름 및 Event Grid 도메인 토픽 이름을 지정하기 위해 새로운 필수 매개 변수를 추가하여 이러한 리소스 아래에 새 이벤트 구독을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-946">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="e51e5-947">기존 매개 변수(예: EndPointType, SubjectBeginsWith 등)를 재사용할 수 있도록 도메인 및 도메인 토픽에 대한 새로운 매개 변수 집합을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-947">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="e51e5-948">지정을 위한 새로운 선택적 매개 변수를 추가</span><span class="sxs-lookup"><span data-stu-id="e51e5-948">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="e51e5-949">이벤트 구독 만료 날짜,</span><span class="sxs-lookup"><span data-stu-id="e51e5-949">Event subscription expiration date,</span></span>
            - <span data-ttu-id="e51e5-950">고급 필터링 매개 변수.</span><span class="sxs-lookup"><span data-stu-id="e51e5-950">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="e51e5-951">대상으로 servicebusqueue에 대한 새 열거형을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-951">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="e51e5-952">-IncludedEventType 옵션에서 'All' 사용을 허용하지 않고 다음으로 대체함</span><span class="sxs-lookup"><span data-stu-id="e51e5-952">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span> 
    - <span data-ttu-id="e51e5-953">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="e51e5-953">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="e51e5-954">결과 페이지 매김 및 필터링을 지원하는 새로운 선택적 매개 변수(Top, ODataQuery 및 NextLink)를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-954">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="e51e5-955">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="e51e5-955">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="e51e5-956">Event Grid 도메인 및 Event Grid 도메인 토픽에 대한 파이핑을 지원하기 위해 새로운 필수 매개 변수를 추가하여 이러한 리소스 아래에 기존 이벤트 구독을 제거할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-956">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="e51e5-957">Event Grid 도메인 이름 및 Event Grid 도메인 토픽 이름을 지정하기 위해 새로운 필수 매개 변수를 추가하여 이러한 리소스 아래에 기존 이벤트 구독을 제거할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-957">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="e51e5-958">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="e51e5-958">Az.FrontDoor</span></span>
* <span data-ttu-id="e51e5-959">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="e51e5-959">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="e51e5-960">변환 지원 및 새 연산자 자동 완성 값(RegEx)을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-960">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="e51e5-961">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="e51e5-961">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="e51e5-962">새 자동 완성 값 추가</span><span class="sxs-lookup"><span data-stu-id="e51e5-962">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e51e5-963">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e51e5-963">Az.Network</span></span>
* <span data-ttu-id="e51e5-964">Microsoft Azure Virtual Network 게이트웨이 리소스에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="e51e5-964">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="e51e5-965">새로운 cmdlet</span><span class="sxs-lookup"><span data-stu-id="e51e5-965">New cmdlets</span></span>
        - <span data-ttu-id="e51e5-966">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="e51e5-966">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="e51e5-967">AvailablePrivateEndpointType 추가</span><span class="sxs-lookup"><span data-stu-id="e51e5-967">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="e51e5-968">새로운 cmdlet</span><span class="sxs-lookup"><span data-stu-id="e51e5-968">New cmdlets</span></span> 
        - <span data-ttu-id="e51e5-969">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="e51e5-969">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="e51e5-970">PrivatePrivateLinkService 추가</span><span class="sxs-lookup"><span data-stu-id="e51e5-970">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="e51e5-971">새로운 cmdlet</span><span class="sxs-lookup"><span data-stu-id="e51e5-971">New cmdlets</span></span> 
        - <span data-ttu-id="e51e5-972">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="e51e5-972">Get-AzPrivateLinkService</span></span> 
        - <span data-ttu-id="e51e5-973">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="e51e5-973">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="e51e5-974">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="e51e5-974">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="e51e5-975">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="e51e5-975">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="e51e5-976">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="e51e5-976">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="e51e5-977">PrivateEndpoint 추가</span><span class="sxs-lookup"><span data-stu-id="e51e5-977">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="e51e5-978">새로운 cmdlet</span><span class="sxs-lookup"><span data-stu-id="e51e5-978">New cmdlets</span></span>
        - <span data-ttu-id="e51e5-979">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="e51e5-979">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="e51e5-980">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="e51e5-980">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="e51e5-981">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="e51e5-981">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="e51e5-982">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="e51e5-982">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="e51e5-983">기능에 대한 새로운 명령이 업데이트됨: VpnConnection 상의 UseLocalAzureIpAddress 플래그</span><span class="sxs-lookup"><span data-stu-id="e51e5-983">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="e51e5-984">New-AzVpnConnection이 업데이트됨: 선택적 매개 변수 -UseLocalAzureIpAddress를 추가하여 로컬 Azure IP 주소가 연결을 시작하는 동안 소스 주소로 사용되어야 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-984">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="e51e5-985">Set-AzVpnConnection이 업데이트됨: 선택적 매개 변수 -UseLocalAzureIpAddress를 추가하여 로컬 Azure IP 주소가 연결을 시작하는 동안 소스 주소로 사용되어야 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-985">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="e51e5-986">ExpressRoute 피어링에 읽기 전용 필드 PeeredConnections가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-986">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="e51e5-987">ExpressRoute에 읽기 전용 필드 GlobalReachEnabled가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-987">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="e51e5-988">ExpressRouteCircuit 모델에서 AllowGlobalReach 필드의 사용 중단을 부르는 호환성이 손상되는 변경 속성이 추가됨</span><span class="sxs-lookup"><span data-stu-id="e51e5-988">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="e51e5-989">AzApplicationGatewayRedirectConfiguration cmdlet에서 TargetListenerID를 사용하는 중의 8756 오류 문제가 해결됨</span><span class="sxs-lookup"><span data-stu-id="e51e5-989">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="e51e5-990">다시 쓰기 규칙 세트가 설정되지 못하게 하는 New-AzApplicationGatewayPathRuleConfig의 버그를 수정했습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-990">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="e51e5-991">NetworkInterfaceIpConfiguration에 VirtualNetworkTaps가 표시되는 방식이 수정됨</span><span class="sxs-lookup"><span data-stu-id="e51e5-991">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="e51e5-992">모든 파트를 나열하도록 Cortex Get cmdlet이 수정됨</span><span class="sxs-lookup"><span data-stu-id="e51e5-992">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="e51e5-993">ExpressRouteGateways, VpnGateway에 대한 VirtualHub 참조 생성 수정됨</span><span class="sxs-lookup"><span data-stu-id="e51e5-993">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="e51e5-994">AzureFirewall 및 NatGateway의 가용성 영역에 대한 지원 추가됨</span><span class="sxs-lookup"><span data-stu-id="e51e5-994">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="e51e5-995">Get-AzNetworkServiceTag cmdlet 추가됨</span><span class="sxs-lookup"><span data-stu-id="e51e5-995">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="e51e5-996">Azure Firewall에 대한 여러 공용 IP 주소에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="e51e5-996">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="e51e5-997">New-AzFirewall cmdlet이 업데이트됨:</span><span class="sxs-lookup"><span data-stu-id="e51e5-997">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="e51e5-998">하나 이상의 공용 IP 주소 개체를 허용하는 매개 변수 -PublicIpAddress 추가됨</span><span class="sxs-lookup"><span data-stu-id="e51e5-998">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="e51e5-999">Virtual Network 개체를 허용하는 매개 변수 -VirtualNetwork 추가됨</span><span class="sxs-lookup"><span data-stu-id="e51e5-999">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="e51e5-1000">방화벽 개체에 AddPublicIpAddress 및 RemovePublicIpAddress 메서드 추가됨 - 공용 IP 주소 개체를 입력으로 허용</span><span class="sxs-lookup"><span data-stu-id="e51e5-1000">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="e51e5-1001">매개 변수 -PublicIpName 및 -VirtualNetworkName이 더 이상 사용되지 않음</span><span class="sxs-lookup"><span data-stu-id="e51e5-1001">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span> 
* <span data-ttu-id="e51e5-1002">기능에 대한 새로운 명령이 업데이트됨: VpnClient AAD 인증 옵션을 가상 네트워크 게이트웨이 리소스로 설정했습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1002">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span> 
    - <span data-ttu-id="e51e5-1003">New-AzVirtualNetworkGateway가 업데이트됨: 게이트웨이에서 VpnClient AAD 인증 옵션을 설정할 수 있도록 선택적 매개 변수 AadTenantUri, AadAudienceId, AadIssuerUri가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1003">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="e51e5-1004">Set-AzVirtualNetworkGateway가 업데이트됨: 게이트웨이에서 VpnClient AAD 인증 옵션을 설정할 수 있도록 선택적 매개 변수 AadTenantUri, AadAudienceId, AadIssuerUri가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1004">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="e51e5-1005">Set-AzVirtualNetworkGateway가 업데이트됨: 게이트웨이에서 VpnClient AAD 인증 옵션을 제거할 수 있도록 선택적인 스위치 매개 변수 RemoveAadAuthentication이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1005">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="e51e5-1006">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="e51e5-1006">Az.OperationalInsights</span></span>
* <span data-ttu-id="e51e5-1007">'New-AzureRmOperationalInsightsWorkspace' 명령에서 **pergb2018** 가격 책정 계층 사용</span><span class="sxs-lookup"><span data-stu-id="e51e5-1007">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="e51e5-1008">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e51e5-1008">Az.Resources</span></span>
* <span data-ttu-id="e51e5-1009">추가 템플릿 내보내기 옵션 지원</span><span class="sxs-lookup"><span data-stu-id="e51e5-1009">Support for additional Template Export options</span></span>
    - <span data-ttu-id="e51e5-1010">Export-AzResourceGroup에 '-SkipResourceNameParameterization' 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="e51e5-1010">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="e51e5-1011">Export-AzResourceGroup에 '-SkipAllParameterization' 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="e51e5-1011">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="e51e5-1012">내보낸 리소스 필터링을 위해 Export-AzResourceGroup에 '-Resource' 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="e51e5-1012">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="e51e5-1013">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="e51e5-1013">Az.ServiceFabric</span></span>
* <span data-ttu-id="e51e5-1014">일부 경우 잘못된 지문을 가져오는 추가 인증서 ByExistingKeyVault 수정</span><span class="sxs-lookup"><span data-stu-id="e51e5-1014">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="e51e5-1015">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e51e5-1015">Az.Sql</span></span>
* <span data-ttu-id="e51e5-1016">Advanced Threat Protection 스토리지 엔드포인트 접미사 수정</span><span class="sxs-lookup"><span data-stu-id="e51e5-1016">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="e51e5-1017">Advanced Data Security가 Advanced Threat Protection 정책을 재정의하는 것을 수정</span><span class="sxs-lookup"><span data-stu-id="e51e5-1017">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="e51e5-1018">고객이 TDE 키를 추가하고 관리되는 인스턴스에 TDE 보호기를 설정할 수 있도록 Management.Sql용 새 Cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="e51e5-1018">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="e51e5-1019">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="e51e5-1019">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="e51e5-1020">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="e51e5-1020">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="e51e5-1021">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="e51e5-1021">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="e51e5-1022">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="e51e5-1022">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="e51e5-1023">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="e51e5-1023">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="e51e5-1024">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="e51e5-1024">Az.Storage</span></span>
* <span data-ttu-id="e51e5-1025">스토리지 계정 생성 시 종류 FileStorage 및 SkuName Premium_ZRS 지원</span><span class="sxs-lookup"><span data-stu-id="e51e5-1025">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="e51e5-1026">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="e51e5-1026">New-AzStorageAccount</span></span>
* <span data-ttu-id="e51e5-1027">BLOB immutability cmdlet의 설명 명확화</span><span class="sxs-lookup"><span data-stu-id="e51e5-1027">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="e51e5-1028">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="e51e5-1028">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="e51e5-1029">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="e51e5-1029">Az.Websites</span></span>
* <span data-ttu-id="e51e5-1030">Get-AzWebAppCertificate를 클라이언트 대신 서버의 리소스 그룹별로 필터링하도록 최적화</span><span class="sxs-lookup"><span data-stu-id="e51e5-1030">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="e51e5-1031">Get-AzWebAppSnapshot에 -UseDisasterRecovery 스위치 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="e51e5-1031">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="e51e5-1032">2.2.0 - 2019년 6월</span><span class="sxs-lookup"><span data-stu-id="e51e5-1032">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="e51e5-1033">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="e51e5-1033">Az.Cdn</span></span>
* <span data-ttu-id="e51e5-1034">cmdlet에서 2019-04-15 API 버전 기반의 rulesEngine 기능을 지원하도록 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1034">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e51e5-1035">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e51e5-1035">Az.Compute</span></span>
* <span data-ttu-id="e51e5-1036">작업을 시작하여 완료되기 전에 즉시 반환하는 `NoWait` 매개 변수가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1036">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="e51e5-1037">다음 Cmdlet이 업데이트 되었습니다.   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="e51e5-1037">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="e51e5-1038">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="e51e5-1038">Az.EventHub</span></span>
* <span data-ttu-id="e51e5-1039">#9231 수정 - Get-AzEventHubNamespace에서 태그를 반환하지 않음</span><span class="sxs-lookup"><span data-stu-id="e51e5-1039">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="e51e5-1040">#9230 수정 - Get-AzEventHubNamespace에서 ResourceGroupName 대신 ResourceGroup을 반환함</span><span class="sxs-lookup"><span data-stu-id="e51e5-1040">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e51e5-1041">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e51e5-1041">Az.Network</span></span>
* <span data-ttu-id="e51e5-1042">Nat Gateway에 대한 ResourceId 및 InputObject 업데이트</span><span class="sxs-lookup"><span data-stu-id="e51e5-1042">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="e51e5-1043">ResourceId 및 InputObject에 대한 별칭 추가</span><span class="sxs-lookup"><span data-stu-id="e51e5-1043">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="e51e5-1044">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="e51e5-1044">Az.PolicyInsights</span></span>
* <span data-ttu-id="e51e5-1045">Get-AzPolicyEvent에서 Null 참조 문제 해결</span><span class="sxs-lookup"><span data-stu-id="e51e5-1045">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="e51e5-1046">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="e51e5-1046">Az.RecoveryServices</span></span>
* <span data-ttu-id="e51e5-1047">IaaSVM 정책 최소 보존 기간(일)이 1에서 7로 변경됨</span><span class="sxs-lookup"><span data-stu-id="e51e5-1047">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="e51e5-1048">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="e51e5-1048">Az.ServiceBus</span></span>
* <span data-ttu-id="e51e5-1049">#9182 문제 해결 - Get-AzServiceBusNamespace에서 ResourceGroupName 대신 ResourceGroup을 반환</span><span class="sxs-lookup"><span data-stu-id="e51e5-1049">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="e51e5-1050">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="e51e5-1050">Az.ServiceFabric</span></span>
* <span data-ttu-id="e51e5-1051">'Update-AzServiceFabricReliability' 오류 메시지의 오타 수정</span><span class="sxs-lookup"><span data-stu-id="e51e5-1051">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="e51e5-1052">Service Fabric 명령줄에서 누락된 문자 수정</span><span class="sxs-lookup"><span data-stu-id="e51e5-1052">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="e51e5-1053">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e51e5-1053">Az.Sql</span></span>
* <span data-ttu-id="e51e5-1054">Managed Instance에 대한 AutoDr을 지원하기 위해 New-AzureSqlInstance cmdlet에 대한 DnsZonePartner 매개 변수를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1054">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="e51e5-1055">Get-AzSqlDatabaseSecureConnectionPolicy cmdlet 사용 중단</span><span class="sxs-lookup"><span data-stu-id="e51e5-1055">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="e51e5-1056">Threat Detection(위협 탐지) cmdlet 이름을 Advanced Threat Protection으로 변경함</span><span class="sxs-lookup"><span data-stu-id="e51e5-1056">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="e51e5-1057">새 AzSqlInstance -StorageSizeInGB 및 -LicenseType 매개 변수는 이제 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1057">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="e51e5-1058">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="e51e5-1058">Az.Websites</span></span>
* <span data-ttu-id="e51e5-1059">-WebApp 속성에서 Set-AzWebApp 및 Set-AzWebAppSlot을 사용하면 태그가 제거되는 문제를 해결함</span><span class="sxs-lookup"><span data-stu-id="e51e5-1059">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="e51e5-1060">2.1.0 - 2019년 5월</span><span class="sxs-lookup"><span data-stu-id="e51e5-1060">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="e51e5-1061">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="e51e5-1061">Az.ApiManagement</span></span>
* <span data-ttu-id="e51e5-1062">글로벌 및 API 범위에서 진단을 관리하기 위한 새 cmdlet을 만들었습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1062">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="e51e5-1063">**Get-AzApiManagementDiagnostic** - 글로벌 또는 API 범위가 구성된 진단 가져오기</span><span class="sxs-lookup"><span data-stu-id="e51e5-1063">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="e51e5-1064">**New-AzApiManagementDiagnostic** - 글로벌 범위 또는 API 범위에서 새 진단 만들기</span><span class="sxs-lookup"><span data-stu-id="e51e5-1064">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="e51e5-1065">**New-AzApiManagementHttpMessageDiagnostic** - 기록할 Headers(헤더) 및 Body Bytes(본문 바이트 수) 크기에 대한 진단 설정 만들기</span><span class="sxs-lookup"><span data-stu-id="e51e5-1065">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="e51e5-1066">**New-AzApiManagementPipelineDiagnosticSetting** - 게이트웨이로 들어오고 나가는 HTTP 메시지에 대한 진단 설정 만들기</span><span class="sxs-lookup"><span data-stu-id="e51e5-1066">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="e51e5-1067">**New-AzApiManagementSamplingSetting** - 진단 요청/응답에 대한 샘플링 설정 만들기</span><span class="sxs-lookup"><span data-stu-id="e51e5-1067">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="e51e5-1068">**Remove-AzApiManagementDiagnostic** - 글로벌 또는 API 범위에서 진단 엔터티 제거</span><span class="sxs-lookup"><span data-stu-id="e51e5-1068">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="e51e5-1069">**Set-AzApiManagementDiagnostic** - 글로벌 또는 API 범위에서 진단 엔터티 업데이트</span><span class="sxs-lookup"><span data-stu-id="e51e5-1069">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="e51e5-1070">ApiManagement 서비스에서 캐시를 관리하기 위한 새 cmdlet을 만들었습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1070">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="e51e5-1071">**Get-AzApiManagementCache** - 식별자 또는 모든 캐시로 지정된 캐시의 세부 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="e51e5-1071">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="e51e5-1072">**New-AzApiManagementCache** - 특정 Azure 'region'(지역)에 새 'default'(기본) 캐시 만들기</span><span class="sxs-lookup"><span data-stu-id="e51e5-1072">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="e51e5-1073">**Remove-AzApiManagementCache** - 캐시 제거</span><span class="sxs-lookup"><span data-stu-id="e51e5-1073">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="e51e5-1074">**Update-AzApiManagementCache** - 캐시 업데이트</span><span class="sxs-lookup"><span data-stu-id="e51e5-1074">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="e51e5-1075">API 스키마 관리하기 위한 새 cmdlet을 만들었습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1075">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="e51e5-1076">**New-AzApiManagementSchema** - API에 대한 새 스키마 만들기</span><span class="sxs-lookup"><span data-stu-id="e51e5-1076">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="e51e5-1077">**Get-AzApiManagementSchema** - API에 구성된 스키마 가져오기</span><span class="sxs-lookup"><span data-stu-id="e51e5-1077">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="e51e5-1078">**Remove-AzApiManagementSchema** - API에 구성된 스키마 제거</span><span class="sxs-lookup"><span data-stu-id="e51e5-1078">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="e51e5-1079">**Set-AzApiManagementSchema** - API에 구성된 스키마 업데이트</span><span class="sxs-lookup"><span data-stu-id="e51e5-1079">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="e51e5-1080">사용자 토큰을 생성하기 위한 새 cmdlet을 만들었습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1080">Created new Cmdlet for generating a User Token.</span></span> 
    - <span data-ttu-id="e51e5-1081">**New-AzApiManagementUserToken** - 기본적으로 8시간 동안 유효한 새 사용자 토큰을 생성합니다. 'GIT' 사용자에 대한 토큰은 이 cmdlet을 사용하여 생성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1081">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="e51e5-1082">네트워크 상태를 검색하기 위한 새 cmdlet을 만들었습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1082">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="e51e5-1083">**Get-AzApiManagementNetworkStatus** - API Management 서비스에서 사용하는 리소스의 네트워크 상태 연결을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1083">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="e51e5-1084">ApiManagement 서비스를 가상 네트워크에 배포하고 종속성이 손상되었는지 여부를 확인할 때 유용합니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1084">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="e51e5-1085">**New-AzApiManagement** cmdlet에서 ApiManagement 서비스를 관리하도록 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1085">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span> 
    - <span data-ttu-id="e51e5-1086">새 '소비' SKU 지원이 추가됨</span><span class="sxs-lookup"><span data-stu-id="e51e5-1086">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="e51e5-1087">'소비' SKU에 대해 'EnableClientCertificate' 플래그를 설정하기 위한 지원이 추가됨</span><span class="sxs-lookup"><span data-stu-id="e51e5-1087">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="e51e5-1088">새 **New-AzApiManagementSslSetting** cmdlet을 사용하면 'Backend(백 엔드)' 및 'Frontend'(프런트 엔드)에서 'TLS/SSL' 설정을 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1088">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="e51e5-1089">또한 ApiManagement 서비스의 'Frontend'에서 '3DES'와 같은 'Ciphers'와 'Http2'와 같은 'ServerProtocols'를 구성하는 데 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1089">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="e51e5-1090">ApiManagement 서비스에서 'DeveloperPortal' 호스트 이름을 구성하기 위한 지원이 추가됨</span><span class="sxs-lookup"><span data-stu-id="e51e5-1090">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="e51e5-1091">**Get-AzApiManagementSsoToken** cmdlet에서 'PsApiManagement' 개체를 입력으로 사용하도록 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1091">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="e51e5-1092">cmdlet에서 오류 메시지를 인라인으로 표시하도록 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1092">Updated the cmdlet to display Error Messages inline</span></span> 
     > <span data-ttu-id="e51e5-1093">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : 오류 코드: ValidationError 오류 메시지: 하나 이상의 필드에 잘못된 값이 있습니다. 오류 세부 정보:    [Code=ValidationError, Message=줄 3, 열 10의 'log-to-eventhub' 요소에 오류가 있습니다.: 로거를 찾지 못함, Target=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="e51e5-1093">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="e51e5-1094">**Export-AzApiManagementApi** cmdlet에서 API를 'OpenApi 3.0' 형식으로 내보내도록 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1094">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="e51e5-1095">**Import-AzApiManagementApi** cmdlet을 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1095">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="e51e5-1096">'OpenApi 3.0' 문서 사양에서 API 가져오기</span><span class="sxs-lookup"><span data-stu-id="e51e5-1096">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="e51e5-1097">문서('Swagger', 'Wadl', 'Wsdl', 'OpenApi')에 지정된 'PsApiManagementSchema' 속성 재정의</span><span class="sxs-lookup"><span data-stu-id="e51e5-1097">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="e51e5-1098">문서에 지정된 'ServiceUrl' 속성 재정의</span><span class="sxs-lookup"><span data-stu-id="e51e5-1098">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="e51e5-1099">**Get-AzApiManagementPolicy** cmdlet에서 'rawxml'을 사용하여 이스케이프된 비 Xml 'format'(형식)의 정책을 반환하도록 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1099">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="e51e5-1100">**Set-AzApiManagementPolicy** cmdlet에서 'rawxml'을 사용하여 이스케이프된 비 Xml 'format'의 정책을 수락하고, 'xml'을 사용하여 이스케이프된 Xml 'format'의 정책을 수락하도록 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1100">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="e51e5-1101">**New-AzApiManagementApi** cmdlet을 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1101">Updated cmdlet **New-AzApiManagementApi**</span></span> 
    - <span data-ttu-id="e51e5-1102">'OpenId' 권한 부여 서버를 사용하여 API 구성</span><span class="sxs-lookup"><span data-stu-id="e51e5-1102">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="e51e5-1103">'ApiVersionSet'에서 API 만들기</span><span class="sxs-lookup"><span data-stu-id="e51e5-1103">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="e51e5-1104">'SourceApiId' 및 'SourceApiRevision'을 사용하여 API 복제</span><span class="sxs-lookup"><span data-stu-id="e51e5-1104">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="e51e5-1105">API 범위에서 'SubscriptionRequired' 구성 가능</span><span class="sxs-lookup"><span data-stu-id="e51e5-1105">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="e51e5-1106">**Set-AzApiManagementApi** cmdlet을 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1106">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="e51e5-1107">'OpenId' 권한 부여 서버를 사용하여 API 구성</span><span class="sxs-lookup"><span data-stu-id="e51e5-1107">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="e51e5-1108">API를 'ApiVersionSet'으로 업데이트</span><span class="sxs-lookup"><span data-stu-id="e51e5-1108">To updated an API into an 'ApiVersionSet'</span></span>    
    - <span data-ttu-id="e51e5-1109">API 범위에서 'SubscriptionRequired' 구성 가능</span><span class="sxs-lookup"><span data-stu-id="e51e5-1109">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="e51e5-1110">**New-AzApiManagementRevision** cmdlet을 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1110">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="e51e5-1111">'SourceApiRevision'을 사용하여 기존 수정 버전 복제(태그, 제품, 작업 및 정책 복사).</span><span class="sxs-lookup"><span data-stu-id="e51e5-1111">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="e51e5-1112">새 수정 버전은 부모의 'ApiId'를 가정합니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1112">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="e51e5-1113">'ApiRevisionDescription' 제공</span><span class="sxs-lookup"><span data-stu-id="e51e5-1113">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="e51e5-1114">API 복제 시 'ServiceUrl' 재정의</span><span class="sxs-lookup"><span data-stu-id="e51e5-1114">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="e51e5-1115">**New-AzApiManagementIdentityProvider** cmdlet을 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1115">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="e51e5-1116">'Authority'를 사용하여 'AAD' 또는 'AADB2C' 구성</span><span class="sxs-lookup"><span data-stu-id="e51e5-1116">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="e51e5-1117">'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' 및 'PasswordResetPolicy' 설정</span><span class="sxs-lookup"><span data-stu-id="e51e5-1117">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="e51e5-1118">**New-AzApiManagementSubscription** cmdlet을 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1118">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="e51e5-1119">'Scope' 및 'UserId'를 사용하여 새 SubscriptonModel 설명</span><span class="sxs-lookup"><span data-stu-id="e51e5-1119">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="e51e5-1120">'ProductId' 및 'UserId'를 사용하여 이전 구독 모델 설명</span><span class="sxs-lookup"><span data-stu-id="e51e5-1120">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="e51e5-1121">구독 수준에서 'AllowTracing'을 사용하도록 설정하는 지원 추가</span><span class="sxs-lookup"><span data-stu-id="e51e5-1121">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="e51e5-1122">**Set-AzApiManagementSubscription** cmdlet을 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1122">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="e51e5-1123">'Scope' 및 'UserId'를 사용하여 새 SubscriptonModel 설명</span><span class="sxs-lookup"><span data-stu-id="e51e5-1123">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="e51e5-1124">'ProductId' 및 'UserId'를 사용하여 이전 구독 모델 설명</span><span class="sxs-lookup"><span data-stu-id="e51e5-1124">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="e51e5-1125">구독 수준에서 'AllowTracing'을 사용하도록 설정하는 지원 추가</span><span class="sxs-lookup"><span data-stu-id="e51e5-1125">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="e51e5-1126">다음 cmdlet에서 'ResourceId'를 입력으로 수락하도록 업데이트했습니다</span><span class="sxs-lookup"><span data-stu-id="e51e5-1126">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="e51e5-1127">'New-AzApiManagementContext'</span><span class="sxs-lookup"><span data-stu-id="e51e5-1127">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="e51e5-1128">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="e51e5-1128">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="e51e5-1129">'Get-AzApiManagementApiRelease'</span><span class="sxs-lookup"><span data-stu-id="e51e5-1129">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="e51e5-1130">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="e51e5-1130">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="e51e5-1131">'Get-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="e51e5-1131">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="e51e5-1132">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="e51e5-1132">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="e51e5-1133">'Get-AzApiManagementAuthorizationServer'</span><span class="sxs-lookup"><span data-stu-id="e51e5-1133">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="e51e5-1134">'Get-AzApiManagementBackend'</span><span class="sxs-lookup"><span data-stu-id="e51e5-1134">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="e51e5-1135">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="e51e5-1135">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="e51e5-1136">'Get-AzApiManagementCertificate'</span><span class="sxs-lookup"><span data-stu-id="e51e5-1136">'Get-AzApiManagementCertificate'</span></span> 
    - <span data-ttu-id="e51e5-1137">'Remove-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="e51e5-1137">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="e51e5-1138">'Remove-AzApiManagementSubscription'</span><span class="sxs-lookup"><span data-stu-id="e51e5-1138">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="e51e5-1139">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="e51e5-1139">Az.Automation</span></span>
* <span data-ttu-id="e51e5-1140">Get-AzAutomationJobOutputRecord에서 JSON 및 Text 레코드 값을 처리하도록 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1140">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="e51e5-1141">문제 https://github.com/Azure/azure-powershell/issues/7977 수정</span><span class="sxs-lookup"><span data-stu-id="e51e5-1141">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="e51e5-1142">문제 https://github.com/Azure/azure-powershell/issues/8600 수정</span><span class="sxs-lookup"><span data-stu-id="e51e5-1142">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="e51e5-1143">Start-AzAutomationDscCompilationJob에서 완료될 때까지 기다리지 않고 작업을 바로 시작하도록 변경했습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1143">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="e51e5-1144">문제 https://github.com/Azure/azure-powershell/issues/8347 수정</span><span class="sxs-lookup"><span data-stu-id="e51e5-1144">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="e51e5-1145">-Name을 사용하면 모든 노드를 반환하는 Get-AzAutomationDscNode 수정.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1145">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="e51e5-1146">이제 일치하는 노드만 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1146">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e51e5-1147">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e51e5-1147">Az.Compute</span></span>
* <span data-ttu-id="e51e5-1148">ProtectFromScaleIn 및 ProtectFromScaleSetAction 매개 변수를 Update-AzVmssVM cmdlet에 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1148">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="e51e5-1149">'East US'(미국 동부)가 지원되지 않는 경우 이제 New-AzVM wimple 매개 변수 집합에서 기본적으로 사용 가능한 위치를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1149">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="e51e5-1150">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="e51e5-1150">Az.DataLakeStore</span></span>
* <span data-ttu-id="e51e5-1151">ADLS SDK에서 httpclient를 사용하도록 업데이트하고, 데이터 평면 테스트를 Azure 프레임워크와 통합합니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1151">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="e51e5-1152">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="e51e5-1152">Az.Monitor</span></span>
* <span data-ttu-id="e51e5-1153">도움말 예제에서 잘못된 매개 변수 이름을 수정했습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1153">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e51e5-1154">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e51e5-1154">Az.Network</span></span>
* <span data-ttu-id="e51e5-1155">DisableBgpRoutePropagation 플래그를 유효 경로 테이블 출력에 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1155">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="e51e5-1156">업데이트된 cmdlet:</span><span class="sxs-lookup"><span data-stu-id="e51e5-1156">Updated cmdlet:</span></span>
        - <span data-ttu-id="e51e5-1157">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="e51e5-1157">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="e51e5-1158">New-AzApplicationGatewayTrustedRootCertificate 설명서에서 이중 파선을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1158">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="e51e5-1159">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e51e5-1159">Az.Resources</span></span>
* <span data-ttu-id="e51e5-1160">할당 거부를 검색하기 위한 새 Get-AzureRmDenyAssignment cmdlet을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1160">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="e51e5-1161">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e51e5-1161">Az.Sql</span></span>
* <span data-ttu-id="e51e5-1162">Advanced Threat Protection cmdlet의 이름을 Advanced Data Security로 변경하고, 취약성 평가를 기본적으로 사용하도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1162">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="e51e5-1163">2.0.0 - 2019년 5월</span><span class="sxs-lookup"><span data-stu-id="e51e5-1163">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="e51e5-1164">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e51e5-1164">Az.Accounts</span></span>
* <span data-ttu-id="e51e5-1165">사용자 이름/비밀번호 인증을 사용하여 ADFS 문제를 해결하도록 인증 라이브러리 업데이트</span><span class="sxs-lookup"><span data-stu-id="e51e5-1165">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="e51e5-1166">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="e51e5-1166">Az.CognitiveServices</span></span>
* <span data-ttu-id="e51e5-1167">Bing Search 서비스에 대해서만 Bing 면책 조항을 표시하세요.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1167">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="e51e5-1168">계정 생성 실패 시 오류 개선.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1168">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e51e5-1169">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e51e5-1169">Az.Compute</span></span>
* <span data-ttu-id="e51e5-1170">근접 배치 그룹 기능</span><span class="sxs-lookup"><span data-stu-id="e51e5-1170">Proximity placement group feature.</span></span>
    - <span data-ttu-id="e51e5-1171">다음과 같은 새 cmdlet을 추가했습니다.   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="e51e5-1171">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="e51e5-1172">새 매개 변수 ProximityPlacementGroupId가 다음 cmdlet에 추가됩니다.   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="e51e5-1172">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="e51e5-1173">New-AzGalleryImageVersion에 StorageAccountType 매개 변수가 추가됩니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1173">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="e51e5-1174">New-AzGalleryImageVersion의 TargetRegion이 StorageAccountType를 포함할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1174">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="e51e5-1175">SkipShutdown 스위치 매개 변수가 Stop-AzVM 및 Stop-AzVmss에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1175">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>       
* <span data-ttu-id="e51e5-1176">주요 변경 내용</span><span class="sxs-lookup"><span data-stu-id="e51e5-1176">Breaking changes</span></span>
    - <span data-ttu-id="e51e5-1177">Set-AzVMBootDiagnostics이 Set-AzVMBootDiagnostic으로 변경됩니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1177">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="e51e5-1178">Export-AzLogAnalyticThrottledRequests이 Export-AzLogAnalyticThrottledRequests로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1178">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="e51e5-1179">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="e51e5-1179">Az.DeploymentManager</span></span>
* <span data-ttu-id="e51e5-1180">Azure 배포 관리자 cmdlet의 일반적으로 사용 가능한 첫 번째 릴리스</span><span class="sxs-lookup"><span data-stu-id="e51e5-1180">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="e51e5-1181">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="e51e5-1181">Az.Dns</span></span>
* <span data-ttu-id="e51e5-1182">자동 DNS 이름 서버 위임</span><span class="sxs-lookup"><span data-stu-id="e51e5-1182">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="e51e5-1183">DNS 영역 만들기 cmdlet은 추가 선택적 매개 변수로 부모 영역 이름을 허용합니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1183">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="e51e5-1184">새로 생성 된 자식 영역의 부모 영역에 NS 레코드를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1184">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="e51e5-1185">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="e51e5-1185">Az.FrontDoor</span></span>
* <span data-ttu-id="e51e5-1186">Azure FrontDoor cmdlet의 일반적으로 사용 가능한 첫 번째 릴리스</span><span class="sxs-lookup"><span data-stu-id="e51e5-1186">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="e51e5-1187">'Waf'를 포함하도록 WAF cmdlet의 이름 바꾸기</span><span class="sxs-lookup"><span data-stu-id="e51e5-1187">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="e51e5-1188">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="e51e5-1188">Az.HDInsight</span></span>
* <span data-ttu-id="e51e5-1189">두 개의 cmdlet을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1189">Removed two cmdlets:</span></span>
    - <span data-ttu-id="e51e5-1190">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="e51e5-1190">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="e51e5-1191">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="e51e5-1191">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="e51e5-1192">Grant-AzHDInsightHttpServicesAccess를 대체할 새 cmdlet Set-AzHDInsightGatewayCredential을 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1192">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="e51e5-1193">reader 역할과 HDInsight 운영자 역할을 구분하도록 cmdlet Get-AzHDInsightJobOutput 업데이트:</span><span class="sxs-lookup"><span data-stu-id="e51e5-1193">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="e51e5-1194">reader 역할을 가진 사용자는 'DefaultStorageAccountKey'매개 변수를 명시적으로 지정해야 합니다. 그렇지 않으면 오류가 발생합니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1194">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="e51e5-1195">Hdinsight 운영자 역할을 가진 사용자를 영향을 받지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1195">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="e51e5-1196">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="e51e5-1196">Az.Monitor</span></span>
* <span data-ttu-id="e51e5-1197">SQR API(예약 쿼리 규칙)용 새 cmdlet</span><span class="sxs-lookup"><span data-stu-id="e51e5-1197">New cmdlets for SQR API (Scheduled Query Rule)</span></span>  
    - <span data-ttu-id="e51e5-1198">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="e51e5-1198">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="e51e5-1199">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="e51e5-1199">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="e51e5-1200">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="e51e5-1200">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="e51e5-1201">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="e51e5-1201">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="e51e5-1202">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="e51e5-1202">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="e51e5-1203">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="e51e5-1203">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="e51e5-1204">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="e51e5-1204">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="e51e5-1205">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="e51e5-1205">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="e51e5-1206">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="e51e5-1206">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="e51e5-1207">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="e51e5-1207">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="e51e5-1208">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="e51e5-1208">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="e51e5-1209">SQR API에 대한 [자세한 내용](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules)</span><span class="sxs-lookup"><span data-stu-id="e51e5-1209">[More](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="e51e5-1210">GenV2(비 클래식) 메트릭 기반 경고 규칙에 대한 cmdlet을 포함하도록 Az.Monitor.md가 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="e51e5-1210">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e51e5-1211">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e51e5-1211">Az.Network</span></span>
* <span data-ttu-id="e51e5-1212">Nat 게이트웨이 리소스에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="e51e5-1212">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="e51e5-1213">새로운 cmdlet</span><span class="sxs-lookup"><span data-stu-id="e51e5-1213">New cmdlets</span></span>
        - <span data-ttu-id="e51e5-1214">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="e51e5-1214">New-AzNatGateway</span></span>
        - <span data-ttu-id="e51e5-1215">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="e51e5-1215">Get-AzNatGateway</span></span>
        - <span data-ttu-id="e51e5-1216">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="e51e5-1216">Set-AzNatGateway</span></span>
        - <span data-ttu-id="e51e5-1217">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="e51e5-1217">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="e51e5-1218">다음 Cmdlet이 업데이트 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1218">Updated cmdlets</span></span>
        - <span data-ttu-id="e51e5-1219">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="e51e5-1219">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="e51e5-1220">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="e51e5-1220">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="e51e5-1221">기능에 대한 새로운 명령이 업데이트됨: Brooklyn Gateway에서 사용자 지정 경로 설정/제거.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1221">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="e51e5-1222">New-AzVirtualNetworkGateway가 업데이트됨: 선택적 매개 변수 -CustomRoute를 추가하여 게이트웨이에서 설정할 사용자 지정 경로로 주소 접두사를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1222">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="e51e5-1223">Set-AzVirtualNetworkGateway가 업데이트됨: 선택적 매개 변수 -CustomRoute를 추가하여 게이트웨이에서 설정할 사용자 지정 경로로 주소 접두사를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1223">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="e51e5-1224">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="e51e5-1224">Az.PolicyInsights</span></span>
* <span data-ttu-id="e51e5-1225">정책 평가 세부 정보 쿼리 지원</span><span class="sxs-lookup"><span data-stu-id="e51e5-1225">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="e51e5-1226">Get-AzPolicyState에 '-Expand'매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="e51e5-1226">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="e51e5-1227">'-Expand PolicyEvaluationDetails' 지원</span><span class="sxs-lookup"><span data-stu-id="e51e5-1227">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="e51e5-1228">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="e51e5-1228">Az.RecoveryServices</span></span>
* <span data-ttu-id="e51e5-1229">크로스 구독 Azure에서 Azure 사이트 복구 지원</span><span class="sxs-lookup"><span data-stu-id="e51e5-1229">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="e51e5-1230">Azure Site Recovery에 대한 호환성이 손상되는 변경 표시</span><span class="sxs-lookup"><span data-stu-id="e51e5-1230">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="e51e5-1231">Azure Site Recovery 복구 계획 최종 실행 계획에 대한 수정</span><span class="sxs-lookup"><span data-stu-id="e51e5-1231">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="e51e5-1232">Azure에서 Azure에 대한 Azure Site Recovery 업데이트 네트워크 매핑 수정</span><span class="sxs-lookup"><span data-stu-id="e51e5-1232">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="e51e5-1233">관리 디스크에 대한 Azure에서 Azure에 대한 Azure Site Recovery 업데이트 보호 방향 수정</span><span class="sxs-lookup"><span data-stu-id="e51e5-1233">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="e51e5-1234">기타 사소한 수정.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1234">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="e51e5-1235">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="e51e5-1235">Az.Relay</span></span>
* <span data-ttu-id="e51e5-1236">고객 관련 메시지의 철자 오류 수정</span><span class="sxs-lookup"><span data-stu-id="e51e5-1236">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="e51e5-1237">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="e51e5-1237">Az.ServiceBus</span></span>
* <span data-ttu-id="e51e5-1238">네임스페이스의 NetworkRuleSet에 대한 새 cmdlet가 추가되었습니다</span><span class="sxs-lookup"><span data-stu-id="e51e5-1238">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="e51e5-1239">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="e51e5-1239">Az.Storage</span></span>
* <span data-ttu-id="e51e5-1240">저장소 클라이언트 라이브러리 10.0.1로 업그레이드(이 SDK의 모든 개체의 네임스페이스가 'Microsoft.WindowsAzure.Storage. *'에서 'Microsoft.Azure.Storage.* '로 변경됨)</span><span class="sxs-lookup"><span data-stu-id="e51e5-1240">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="e51e5-1241">새로운 API 버전 2019-04-01을 지원하기 위해 Microsoft.Azure.Management.Storage 11.0.0으로 업그레이드합니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1241">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="e51e5-1242">스토리지 생성 계정의 기본 스토리지 계정 종류가 'Storage'에서 'StorageV2'로 변경됩니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1242">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="e51e5-1243">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="e51e5-1243">New-AzStorageAccount</span></span>
* <span data-ttu-id="e51e5-1244">'StandardLRS'가 'Standard_LRS'로 변경되는 것과 같이 '-'을 추가하여 입력 SkuName과 정렬되도록 스토리지 계정 cmdlet 출력 Sku.Name을 변경합니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1244">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="e51e5-1245">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="e51e5-1245">New-AzStorageAccount</span></span>
    - <span data-ttu-id="e51e5-1246">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="e51e5-1246">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="e51e5-1247">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="e51e5-1247">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="e51e5-1248">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="e51e5-1248">Az.Websites</span></span>
* <span data-ttu-id="e51e5-1249">Get-AzWebApp에서 반환한 PSSite 개체에 대해 'Kind'속성이 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1249">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="e51e5-1250">Get-AzWebApp\* 메트릭 및 Get-AzAppServicePlanMetrics가 사용되지 않음으로 표시되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1250">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="e51e5-1251">1.8.0 - 2019년 4월</span><span class="sxs-lookup"><span data-stu-id="e51e5-1251">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="e51e5-1252">마지막 주 릴리스 이후의 주요 사항</span><span class="sxs-lookup"><span data-stu-id="e51e5-1252">Highlights since the last major release</span></span>
* <span data-ttu-id="e51e5-1253">`Az` 모듈 일반 공급</span><span class="sxs-lookup"><span data-stu-id="e51e5-1253">General availability of `Az` module</span></span>
* <span data-ttu-id="e51e5-1254">`Az` 모듈에 대한 자세한 내용은 https://aka.ms/azps-announce 를 방문하세요.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1254">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="e51e5-1255">Location, ResourceGroup 및 ResourceName 완성자가 추가되었습니다(https://azure.microsoft.com/blog/completers-in-azure-powershell/ ).</span><span class="sxs-lookup"><span data-stu-id="e51e5-1255">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="e51e5-1256">와일드카드 지원이 Az.Compute 및 Az.Network에 대한 Get cmdlet에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1256">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="e51e5-1257">Windows PowerShell 5.1 전용 대화형 사용자 이름/암호 인증이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1257">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="e51e5-1258">Python 2 Runbook 지원이 Az.Automation에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1258">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="e51e5-1259">Az.LogicApp: 통합 계정 어셈블리 및 일괄 처리 구성을 위한 새로운 cmdlet입니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1259">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="e51e5-1260">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e51e5-1260">Az.Accounts</span></span>
* <span data-ttu-id="e51e5-1261">Mac에서 모듈을 올바르게 삭제하기 위해 Uninstall-AzureRm을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1261">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="e51e5-1262">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="e51e5-1262">Az.Batch</span></span>
* <span data-ttu-id="e51e5-1263">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1263">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="e51e5-1264">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="e51e5-1264">Az.Cdn</span></span>
* <span data-ttu-id="e51e5-1265">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1265">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="e51e5-1266">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="e51e5-1266">Az.CognitiveServices</span></span>
* <span data-ttu-id="e51e5-1267">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1267">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e51e5-1268">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e51e5-1268">Az.Compute</span></span>
* <span data-ttu-id="e51e5-1269">디스크의 리소스 ID에 리소스 ID의 소문자 resourcegroups가 있는 경우 AEM 설치 문제 수정</span><span class="sxs-lookup"><span data-stu-id="e51e5-1269">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="e51e5-1270">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1270">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="e51e5-1271">와일드 카드에 대한 설명서 수정</span><span class="sxs-lookup"><span data-stu-id="e51e5-1271">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="e51e5-1272">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="e51e5-1272">Az.DataFactory</span></span>
* <span data-ttu-id="e51e5-1273">NodeCount가 관리형 통합 런타임에 대해 Null이 아닌 경우 SsisProperties를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1273">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="e51e5-1274">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="e51e5-1274">Az.DataLakeStore</span></span>
* <span data-ttu-id="e51e5-1275">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1275">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="e51e5-1276">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="e51e5-1276">Az.EventGrid</span></span>
* <span data-ttu-id="e51e5-1277">이벤트 구독 cmdlet 만들기/업데이트를 사용하기 전에 리소스를 만들어야 함을 나타내기 위해 엔드포인트의 도움말 텍스트가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1277">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="e51e5-1278">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="e51e5-1278">Az.EventHub</span></span>
* <span data-ttu-id="e51e5-1279">네임스페이스의 NetworkRuleSet에 대한 새 cmdlet가 추가되었습니다</span><span class="sxs-lookup"><span data-stu-id="e51e5-1279">Added new cmdlets for NetworkRuleSet of Namespace</span></span> 

#### <a name="azhdinsight"></a><span data-ttu-id="e51e5-1280">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="e51e5-1280">Az.HDInsight</span></span>
* <span data-ttu-id="e51e5-1281">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1281">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="e51e5-1282">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="e51e5-1282">Az.IotHub</span></span>
* <span data-ttu-id="e51e5-1283">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1283">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="e51e5-1284">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="e51e5-1284">Az.KeyVault</span></span>
* <span data-ttu-id="e51e5-1285">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1285">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="e51e5-1286">와일드 카드에 대한 설명서 수정</span><span class="sxs-lookup"><span data-stu-id="e51e5-1286">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="e51e5-1287">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="e51e5-1287">Az.MachineLearning</span></span>
* <span data-ttu-id="e51e5-1288">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1288">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="e51e5-1289">Az.Media</span><span class="sxs-lookup"><span data-stu-id="e51e5-1289">Az.Media</span></span>
* <span data-ttu-id="e51e5-1290">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1290">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="e51e5-1291">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="e51e5-1291">Az.Monitor</span></span>
  * <span data-ttu-id="e51e5-1292">GenV2(비 클래식) 메트릭 기반 경고 규칙에 대한 새 cmdlet</span><span class="sxs-lookup"><span data-stu-id="e51e5-1292">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="e51e5-1293">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="e51e5-1293">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="e51e5-1294">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="e51e5-1294">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="e51e5-1295">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="e51e5-1295">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="e51e5-1296">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="e51e5-1296">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="e51e5-1297">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="e51e5-1297">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="e51e5-1298">모니터 SDK가 버전 0.22.0-preview로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1298">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e51e5-1299">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e51e5-1299">Az.Network</span></span>
* <span data-ttu-id="e51e5-1300">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1300">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="e51e5-1301">와일드 카드에 대한 설명서 수정</span><span class="sxs-lookup"><span data-stu-id="e51e5-1301">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="e51e5-1302">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="e51e5-1302">Az.NotificationHubs</span></span>
* <span data-ttu-id="e51e5-1303">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1303">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="e51e5-1304">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="e51e5-1304">Az.OperationalInsights</span></span>
* <span data-ttu-id="e51e5-1305">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1305">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="e51e5-1306">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="e51e5-1306">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="e51e5-1307">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1307">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="e51e5-1308">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="e51e5-1308">Az.RecoveryServices</span></span>
* <span data-ttu-id="e51e5-1309">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1309">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="e51e5-1310">Azure VM의 SQL용 테이블 형식이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1310">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="e51e5-1311">AzureFileShare에서 위치를 가져오는 대체 메서드가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1311">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="e51e5-1312">시간대에 따라 SchedulePolicy 개체의 ScheduleRunDays가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1312">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="e51e5-1313">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="e51e5-1313">Az.RedisCache</span></span>
* <span data-ttu-id="e51e5-1314">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1314">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="e51e5-1315">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e51e5-1315">Az.Resources</span></span>
* <span data-ttu-id="e51e5-1316">와일드 카드에 대한 설명서 수정</span><span class="sxs-lookup"><span data-stu-id="e51e5-1316">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="e51e5-1317">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e51e5-1317">Az.Sql</span></span>
* <span data-ttu-id="e51e5-1318">Monitor SDK의 종속성을 공용 코드로 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1318">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="e51e5-1319">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1319">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="e51e5-1320">다중 열 분류 프로세스가 향상되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1320">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="e51e5-1321">기본적으로 Get-AzSqlServerServiceObjective의 응답으로 SKU 속성(SKU 이름, 제품군, 용량)과 테이블 형식을 포함합니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1321">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="e51e5-1322">해당 지역에 기존 서버 없이 위치별로 Get-AzSqlServerServiceObjective를 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1322">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="e51e5-1323">관리형 인스턴스 생성 시 표준 시간대 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1323">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="e51e5-1324">와일드 카드에 대한 설명서 수정</span><span class="sxs-lookup"><span data-stu-id="e51e5-1324">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="e51e5-1325">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="e51e5-1325">Az.Websites</span></span>
* <span data-ttu-id="e51e5-1326">실행 시 태그를 제거하지 않도록 Set-AzWebApp 및 Set-AzWebAppSlot를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1326">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="e51e5-1327">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1327">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="e51e5-1328">WebSites SDK가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1328">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="e51e5-1329">PSAppServicePlan에서 AdminSiteName 속성을 제거했습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1329">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="e51e5-1330">1.7.0 - 2019년 4월</span><span class="sxs-lookup"><span data-stu-id="e51e5-1330">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="e51e5-1331">마지막 주 릴리스 이후의 주요 사항</span><span class="sxs-lookup"><span data-stu-id="e51e5-1331">Highlights since the last major release</span></span>
* <span data-ttu-id="e51e5-1332">`Az` 모듈 일반 공급</span><span class="sxs-lookup"><span data-stu-id="e51e5-1332">General availability of `Az` module</span></span>
* <span data-ttu-id="e51e5-1333">`Az` 모듈에 대한 자세한 내용은 https://aka.ms/azps-announce 를 방문하세요.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1333">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="e51e5-1334">Location, ResourceGroup 및 ResourceName 완성자가 추가되었습니다(https://azure.microsoft.com/blog/completers-in-azure-powershell/ ).</span><span class="sxs-lookup"><span data-stu-id="e51e5-1334">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="e51e5-1335">와일드카드 지원이 Az.Compute 및 Az.Network에 대한 Get cmdlet에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1335">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="e51e5-1336">Windows PowerShell 5.1 전용 대화형 사용자 이름/암호 인증이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1336">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="e51e5-1337">Python 2 Runbook 지원이 Az.Automation에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1337">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="e51e5-1338">Az.LogicApp: 통합 계정 어셈블리 및 일괄 처리 구성을 위한 새로운 cmdlet입니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1338">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="e51e5-1339">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e51e5-1339">Az.Accounts</span></span>
* <span data-ttu-id="e51e5-1340">매개 변수 AzureAnalysisServicesEndpointResourceId를 허용하도록 Add-AzEnvironment 및 Set-AzEnvironment 업데이트</span><span class="sxs-lookup"><span data-stu-id="e51e5-1340">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="e51e5-1341">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="e51e5-1341">Az.AnalysisServices</span></span>
* <span data-ttu-id="e51e5-1342">데이터 평면 cmdlet에서 ServiceClient 사용 및 원본 인증 논리 제거</span><span class="sxs-lookup"><span data-stu-id="e51e5-1342">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="e51e5-1343">호환성이 손상되는 변경을 방지하기 위해 Add-AzureASAccount를 Connect-AzAccount의 래퍼로 만듦</span><span class="sxs-lookup"><span data-stu-id="e51e5-1343">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="e51e5-1344">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="e51e5-1344">Az.Automation</span></span>
* <span data-ttu-id="e51e5-1345">포함에 대한 New-AzAutomationSoftwareUpdateConfiguration cmdlet 버그 수정</span><span class="sxs-lookup"><span data-stu-id="e51e5-1345">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="e51e5-1346">이제 매개 변수 IncludedKbNumber 및 IncludedPackageNameMask가 작동함</span><span class="sxs-lookup"><span data-stu-id="e51e5-1346">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="e51e5-1347">Azure 자동화 업데이트 관리 동적 그룹에 대한 버그 수정</span><span class="sxs-lookup"><span data-stu-id="e51e5-1347">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e51e5-1348">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e51e5-1348">Az.Compute</span></span>
* <span data-ttu-id="e51e5-1349">New-AzDiskConfig 및 New-AzSnapshotConfig에 HyperVGeneration 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="e51e5-1349">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="e51e5-1350">다른 테넌트의 갤러리 이미지를 사용하여 VM을 만들 수 있음</span><span class="sxs-lookup"><span data-stu-id="e51e5-1350">Allow VM creation with galley image from other tenants.</span></span> 

#### <a name="azcontainerinstance"></a><span data-ttu-id="e51e5-1351">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="e51e5-1351">Az.ContainerInstance</span></span>
* <span data-ttu-id="e51e5-1352">후행 빈 인수를 추가한 New-AzContainerGroup의 -Command 매개 변수의 문제 수정</span><span class="sxs-lookup"><span data-stu-id="e51e5-1352">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="e51e5-1353">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="e51e5-1353">Az.DataFactory</span></span>
* <span data-ttu-id="e51e5-1354">ADF .Net SDK 버전을 3.0.2로 업데이트</span><span class="sxs-lookup"><span data-stu-id="e51e5-1354">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="e51e5-1355">RepoConfiguration 관련 설정에 대한 추가 매개 변수로 Set-AzDataFactoryV2 cmdlet을 업데이트</span><span class="sxs-lookup"><span data-stu-id="e51e5-1355">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="e51e5-1356">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e51e5-1356">Az.Resources</span></span>
* <span data-ttu-id="e51e5-1357">'-ResourceId' 또는 '-ResourceGroupName', '-Name' 및 '-ResourceType' 매개 변수를 제공할 때 'Get-AzResource'에 대한 공급자 처리 개선</span><span class="sxs-lookup"><span data-stu-id="e51e5-1357">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="e51e5-1358">'Test-AzDeployment' 및 'Test-AzResourceGroupDeployment'에 대한 오류 처리 개선</span><span class="sxs-lookup"><span data-stu-id="e51e5-1358">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="e51e5-1359">배포 유효성 검사 외부에서 발생한 오류를 처리하고 그 대신 명령의 출력에 포함</span><span class="sxs-lookup"><span data-stu-id="e51e5-1359">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="e51e5-1360">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/6856 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1360">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="e51e5-1361">배포 cmdlet 세트에 스크립트 및 작업 시나리오에서 프롬프트를 건너뛰는 '-IgnoreDynamicParameters' 스위치 추가</span><span class="sxs-lookup"><span data-stu-id="e51e5-1361">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="e51e5-1362">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/6856 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1362">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="e51e5-1363">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e51e5-1363">Az.Sql</span></span>
* <span data-ttu-id="e51e5-1364">데이터베이스 데이터 분류 지원</span><span class="sxs-lookup"><span data-stu-id="e51e5-1364">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="e51e5-1365">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="e51e5-1365">Az.Storage</span></span>
* <span data-ttu-id="e51e5-1366">매개 변수 -UseConnectedAccount를 사용하여 스토리지 컨텍스트를 만들 때 자세한 오류 보고(단, 로그인 Azure 계정 없이)</span><span class="sxs-lookup"><span data-stu-id="e51e5-1366">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="e51e5-1367">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="e51e5-1367">New-AzStorageContext</span></span>
* <span data-ttu-id="e51e5-1368">관리 평면 API를 사용하여 지정한 스토리지 계정의 BLOB 서비스 속성 관리 지원</span><span class="sxs-lookup"><span data-stu-id="e51e5-1368">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="e51e5-1369">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="e51e5-1369">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="e51e5-1370">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="e51e5-1370">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="e51e5-1371">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="e51e5-1371">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="e51e5-1372">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="e51e5-1372">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="e51e5-1373">BLOB 및 파일 업로드/다운로드 cmdlet에 대한 -AsJob 지원</span><span class="sxs-lookup"><span data-stu-id="e51e5-1373">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="e51e5-1374">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="e51e5-1374">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="e51e5-1375">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="e51e5-1375">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="e51e5-1376">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="e51e5-1376">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="e51e5-1377">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="e51e5-1377">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="e51e5-1378">1.6.0 - 2019년 3월</span><span class="sxs-lookup"><span data-stu-id="e51e5-1378">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="e51e5-1379">마지막 주 릴리스 이후의 주요 사항</span><span class="sxs-lookup"><span data-stu-id="e51e5-1379">Highlights since the last major release</span></span>
* <span data-ttu-id="e51e5-1380">`Az` 모듈 일반 공급</span><span class="sxs-lookup"><span data-stu-id="e51e5-1380">General availability of `Az` module</span></span>
* <span data-ttu-id="e51e5-1381">`Az` 모듈에 대한 자세한 내용은 https://aka.ms/azps-announce 를 방문하세요.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1381">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="e51e5-1382">Location, ResourceGroup 및 ResourceName 완성자가 추가되었습니다(https://azure.microsoft.com/blog/completers-in-azure-powershell/ ).</span><span class="sxs-lookup"><span data-stu-id="e51e5-1382">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="e51e5-1383">와일드카드 지원이 Az.Compute 및 Az.Network에 대한 Get cmdlet에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1383">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="e51e5-1384">Windows PowerShell 5.1 전용 대화형 사용자 이름/암호 인증이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1384">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="e51e5-1385">Python 2 Runbook 지원이 Az.Automation에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1385">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="e51e5-1386">Az.LogicApp: 통합 계정 어셈블리 및 일괄 처리 구성을 위한 새로운 cmdlet입니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1386">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="e51e5-1387">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="e51e5-1387">Az.Automation</span></span>
* <span data-ttu-id="e51e5-1388">Azure 자동화 업데이트 관리에서 변경된 지원 기능은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1388">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="e51e5-1389">동적 그룹화</span><span class="sxs-lookup"><span data-stu-id="e51e5-1389">Dynamic grouping</span></span>
    * <span data-ttu-id="e51e5-1390">사전 스크립트</span><span class="sxs-lookup"><span data-stu-id="e51e5-1390">Pre-Post script</span></span>
    * <span data-ttu-id="e51e5-1391">다시 부팅 설정</span><span class="sxs-lookup"><span data-stu-id="e51e5-1391">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e51e5-1392">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e51e5-1392">Az.Compute</span></span>
* <span data-ttu-id="e51e5-1393">Get-AzVmBootDiagnosticsData의 경로 확인 문제가 해결되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1393">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="e51e5-1394">Compute 클라이언트 라이브러리가 25.0.0으로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1394">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="e51e5-1395">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="e51e5-1395">Az.KeyVault</span></span>
* <span data-ttu-id="e51e5-1396">와일드카드 지원이 KeyVault cmdlet에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1396">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e51e5-1397">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e51e5-1397">Az.Network</span></span>
* <span data-ttu-id="e51e5-1398">Azure Firewall에 대한 위협 인텔리전스 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1398">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="e51e5-1399">Application Gateway 방화벽 정책의 최상위 수준 리소스 및 사용자 지정 규칙이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1399">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="e51e5-1400">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="e51e5-1400">Az.RecoveryServices</span></span>
* <span data-ttu-id="e51e5-1401">인스턴트 RP를 지원하기 위해 SnapshotRetentionInDays가 Azure VM 정책에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1401">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="e51e5-1402">컨테이너 등록을 취소하는 파이프 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1402">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="e51e5-1403">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e51e5-1403">Az.Resources</span></span>
* <span data-ttu-id="e51e5-1404">Get-AzResource 및 Get-AzResourceGroup에 대한 와일드카드 지원을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1404">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="e51e5-1405">ARM에 대한 일반 호출을 수행할 때 사용되는 자격 증명을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1405">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="e51e5-1406">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e51e5-1406">Az.Sql</span></span>
* <span data-ttu-id="e51e5-1407">위협 탐지의 cmdlet 매개 변수(ExcludeDetectionType)가 DetectionType에서 string[]으로 변경되어 새 DetectionType이 추가되면 이후의 증명이 되고 자동 완성도 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1407">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="e51e5-1408">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="e51e5-1408">Az.Storage</span></span>
* <span data-ttu-id="e51e5-1409">스토리지 계정에 대한 관리 정책 가져오기/설정/제거를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1409">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="e51e5-1410">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="e51e5-1410">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="e51e5-1411">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="e51e5-1411">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="e51e5-1412">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="e51e5-1412">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="e51e5-1413">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="e51e5-1413">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="e51e5-1414">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="e51e5-1414">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="e51e5-1415">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="e51e5-1415">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="e51e5-1416">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="e51e5-1416">Az.Websites</span></span>
* <span data-ttu-id="e51e5-1417">'New-AzWebApp -IncludeSourceWebAppSlots'를 사용하여 모든 슬롯의 복제를 중단하는 ARM 템플릿 버그가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1417">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span> 

## <a name="150---march-2019"></a><span data-ttu-id="e51e5-1418">1.5.0 - 2019년 3월</span><span class="sxs-lookup"><span data-stu-id="e51e5-1418">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="e51e5-1419">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e51e5-1419">Az.Accounts</span></span>
* <span data-ttu-id="e51e5-1420">'Register-AzModule' 명령을 추가하여 AutoRest 생성 cmdlet을 지원</span><span class="sxs-lookup"><span data-stu-id="e51e5-1420">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="e51e5-1421">Connect-AzAccount 예제 업데이트</span><span class="sxs-lookup"><span data-stu-id="e51e5-1421">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="e51e5-1422">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="e51e5-1422">Az.Automation</span></span>
* <span data-ttu-id="e51e5-1423">몇몇 Azure Automation cmdlet에서 특정 월별 일정을 검색할 때 발생하는 문제 수정</span><span class="sxs-lookup"><span data-stu-id="e51e5-1423">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="e51e5-1424">상위 20개 노드를 반환하도록 Get-AzAutomationDscNode를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1424">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="e51e5-1425">이제 모든 노드 반환</span><span class="sxs-lookup"><span data-stu-id="e51e5-1425">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="e51e5-1426">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="e51e5-1426">Az.Cdn</span></span>
* <span data-ttu-id="e51e5-1427">사용자 지정 도메인 Https 사용/사용 안 함에 대한 새 Powershell cmdlet이 추가되었으며 기존의 것은 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1427">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e51e5-1428">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e51e5-1428">Az.Compute</span></span>
* <span data-ttu-id="e51e5-1429">Get cmdlet에 와일드 카드 지원 추가</span><span class="sxs-lookup"><span data-stu-id="e51e5-1429">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="e51e5-1430">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="e51e5-1430">Az.DataFactory</span></span>
* <span data-ttu-id="e51e5-1431">ADF.Net SDK 버전이 3.0.1로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1431">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="e51e5-1432">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="e51e5-1432">Az.LogicApp</span></span>
* <span data-ttu-id="e51e5-1433">첫 결과 페이지 검색 시에만 ListWorkflows 수정</span><span class="sxs-lookup"><span data-stu-id="e51e5-1433">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e51e5-1434">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e51e5-1434">Az.Network</span></span>
* <span data-ttu-id="e51e5-1435">Network cmdlet에 와일드 카드 지원 추가</span><span class="sxs-lookup"><span data-stu-id="e51e5-1435">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="e51e5-1436">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="e51e5-1436">Az.RecoveryServices</span></span>
* <span data-ttu-id="e51e5-1437">Azure VM 지원에 SQL 서버가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1437">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="e51e5-1438">SDK 업데이트</span><span class="sxs-lookup"><span data-stu-id="e51e5-1438">SDK Update</span></span>
* <span data-ttu-id="e51e5-1439">VMappContainer 체크 인 Get-ProtectableItem 제거</span><span class="sxs-lookup"><span data-stu-id="e51e5-1439">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="e51e5-1440">Get ProtectableItem의 매개 변수로 Name과 ServerName이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1440">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="e51e5-1441">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e51e5-1441">Az.Resources</span></span>
* <span data-ttu-id="e51e5-1442">`-TemplateObject` 매개 변수를 추가하여 cmdlet을 배포</span><span class="sxs-lookup"><span data-stu-id="e51e5-1442">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="e51e5-1443">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/2933 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1443">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="e51e5-1444">`Get-AzResource`의 결과를 `Set-AzResource`(으)로 파이프할 때 발생하는 문제 수정</span><span class="sxs-lookup"><span data-stu-id="e51e5-1444">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="e51e5-1445">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/8240 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1445">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="e51e5-1446">실행 시 JSON 데이터 형식 문제 해결 `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="e51e5-1446">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="e51e5-1447">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/7930 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1447">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="e51e5-1448">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e51e5-1448">Az.Sql</span></span>
* <span data-ttu-id="e51e5-1449">AuditingEndpointsCommunicator를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1449">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="e51e5-1450">새 진단 설정을 생성할 때 에지 사례의 동작을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1450">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="e51e5-1451">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="e51e5-1451">Az.Storage</span></span>
* <span data-ttu-id="e51e5-1452">스토리지 계정      - New-AzStorageAccount를 생성할 때 종류 BlockBlobStorage를 지원</span><span class="sxs-lookup"><span data-stu-id="e51e5-1452">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="e51e5-1453">1.4.0 - 2019년 2월</span><span class="sxs-lookup"><span data-stu-id="e51e5-1453">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="e51e5-1454">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="e51e5-1454">Az.AnalysisServices</span></span>
* <span data-ttu-id="e51e5-1455">사용되지 않는 AddAzureASAccount cmdlet</span><span class="sxs-lookup"><span data-stu-id="e51e5-1455">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="e51e5-1456">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="e51e5-1456">Az.Automation</span></span>
* <span data-ttu-id="e51e5-1457">Import-AzAutomationDscNodeConfiguration 도움말 업데이트</span><span class="sxs-lookup"><span data-stu-id="e51e5-1457">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="e51e5-1458">Import-AzAutomationDscConfiguration cmdlet 구성 이름 유효성 검사 추가</span><span class="sxs-lookup"><span data-stu-id="e51e5-1458">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="e51e5-1459">Import-AzAutomationDscConfiguration cmdlet 오류 처리 개선</span><span class="sxs-lookup"><span data-stu-id="e51e5-1459">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="e51e5-1460">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="e51e5-1460">Az.CognitiveServices</span></span>
* <span data-ttu-id="e51e5-1461">리소스의 하위 도메인을 지정하는 데 사용되는 New-AzCognitiveServicesAccount에 대한 새 선택적 매개 변수로 CustomSubdomainName이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1461">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e51e5-1462">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e51e5-1462">Az.Compute</span></span>
* <span data-ttu-id="e51e5-1463">ID 매개 변수 집합 문제 해결</span><span class="sxs-lookup"><span data-stu-id="e51e5-1463">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="e51e5-1464">Name 매개 변수를 제공하지 않으면 Get-AzVMExtension이 설치된 모든 확장을 열거하도록 업데이트</span><span class="sxs-lookup"><span data-stu-id="e51e5-1464">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="e51e5-1465">Update-AzImage cmdlet에 태그 및 ResourceId 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="e51e5-1465">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="e51e5-1466">인스턴스 ID가 없는 Get-AzVmssVM과 InstanceView를 사용하면 인스턴스 보기가 있는 VMSS VM을 나열할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1466">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="e51e5-1467">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="e51e5-1467">Az.DataLakeStore</span></span>
* <span data-ttu-id="e51e5-1468">ADL 삭제된 항목 열거 및 복원에 대한 cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="e51e5-1468">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="e51e5-1469">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="e51e5-1469">Az.EventHub</span></span>
* <span data-ttu-id="e51e5-1470">Eventhub의 CaptureDescription 클래스에서 빈 보관을 건너뛰는 새 부울 속성 SkipEmptyArchives가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1470">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span> 

#### <a name="azkeyvault"></a><span data-ttu-id="e51e5-1471">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="e51e5-1471">Az.KeyVault</span></span>
* <span data-ttu-id="e51e5-1472">Set-AzKeyVaultSecret 태그 지정 수정</span><span class="sxs-lookup"><span data-stu-id="e51e5-1472">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="e51e5-1473">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="e51e5-1473">Az.LogicApp</span></span>
* <span data-ttu-id="e51e5-1474">통합 계정에 대한 기본 sku 추가</span><span class="sxs-lookup"><span data-stu-id="e51e5-1474">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="e51e5-1475">XSLT 2.0, XSLT 3.0, Liquid 맵 형식 추가</span><span class="sxs-lookup"><span data-stu-id="e51e5-1475">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="e51e5-1476">통합 계정 어셈블리에 대한 새 cmdlet</span><span class="sxs-lookup"><span data-stu-id="e51e5-1476">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="e51e5-1477">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="e51e5-1477">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="e51e5-1478">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="e51e5-1478">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="e51e5-1479">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="e51e5-1479">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="e51e5-1480">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="e51e5-1480">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="e51e5-1481">통합 계정 일괄 처리 구성에 대한 새 cmdlet</span><span class="sxs-lookup"><span data-stu-id="e51e5-1481">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="e51e5-1482">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="e51e5-1482">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="e51e5-1483">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="e51e5-1483">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="e51e5-1484">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="e51e5-1484">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="e51e5-1485">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="e51e5-1485">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="e51e5-1486">논리 앱 SDK를 버전 4.1.0으로 업데이트</span><span class="sxs-lookup"><span data-stu-id="e51e5-1486">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="e51e5-1487">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="e51e5-1487">Az.Monitor</span></span>
* <span data-ttu-id="e51e5-1488">Get-AzMetric에 대한 도움말 업데이트</span><span class="sxs-lookup"><span data-stu-id="e51e5-1488">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e51e5-1489">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e51e5-1489">Az.Network</span></span>
* <span data-ttu-id="e51e5-1490">Add-AzApplicationGatewayCustomError에 대한 도움말 예제 업데이트</span><span class="sxs-lookup"><span data-stu-id="e51e5-1490">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="e51e5-1491">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="e51e5-1491">Az.OperationalInsights</span></span>
* <span data-ttu-id="e51e5-1492">New 및 Get ApplicationInsights 데이터 소스에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="e51e5-1492">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="e51e5-1493">지정된 작업 영역에 대한 특정 또는 전체 ApplicationInsights 데이터 원본 가져오기를 지원하기 위한 새로운 'ApplicationInsights' 종류가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1493">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span> 
    - <span data-ttu-id="e51e5-1494">지정된 Application-Insights 리소스 매개 변수(구독 ID, resourceGroupName 및 이름)별로 데이터 원본을 만들기 위한 New-AzOperationalInsightsApplicationInsightsDataSource cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1494">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span> 

#### <a name="azresources"></a><span data-ttu-id="e51e5-1495">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e51e5-1495">Az.Resources</span></span>
* <span data-ttu-id="e51e5-1496">문제 https://github.com/Azure/azure-powershell/issues/8166 수정</span><span class="sxs-lookup"><span data-stu-id="e51e5-1496">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="e51e5-1497">문제 https://github.com/Azure/azure-powershell/issues/8235 수정</span><span class="sxs-lookup"><span data-stu-id="e51e5-1497">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="e51e5-1498">문제 https://github.com/Azure/azure-powershell/issues/6219 수정</span><span class="sxs-lookup"><span data-stu-id="e51e5-1498">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="e51e5-1499">KeyCredentials 반복 만들기를 방지하기 위해 버그 수정</span><span class="sxs-lookup"><span data-stu-id="e51e5-1499">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="e51e5-1500">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e51e5-1500">Az.Sql</span></span>
* <span data-ttu-id="e51e5-1501">SQL DB 하이퍼스케일에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="e51e5-1501">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="e51e5-1502">복원 요청에서 불필요한 속성을 설정하여 복원이 실패할 수 있는 버그 수정</span><span class="sxs-lookup"><span data-stu-id="e51e5-1502">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="e51e5-1503">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="e51e5-1503">Az.Websites</span></span>
* <span data-ttu-id="e51e5-1504">Get-AzWebAppSlotMetrics 내 올바른 예제</span><span class="sxs-lookup"><span data-stu-id="e51e5-1504">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="e51e5-1505">1.3.0 - 2019년 2월</span><span class="sxs-lookup"><span data-stu-id="e51e5-1505">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="e51e5-1506">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e51e5-1506">Az.Accounts</span></span>
* <span data-ttu-id="e51e5-1507">ClientRuntime 최신 버전 업데이트</span><span class="sxs-lookup"><span data-stu-id="e51e5-1507">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="e51e5-1508">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="e51e5-1508">Az.AnalysisServices</span></span>
<span data-ttu-id="e51e5-1509">Az.AnalysisServices 모듈의 전반적인 가용성.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1509">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e51e5-1510">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e51e5-1510">Az.Compute</span></span>
* <span data-ttu-id="e51e5-1511">AEM 확장: UltraSSD 및 P60, P70, P80 디스크에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="e51e5-1511">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="e51e5-1512">Set-AzVMBootDiagnostics에 대한 도움말 업데이트</span><span class="sxs-lookup"><span data-stu-id="e51e5-1512">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="e51e5-1513">Update-AzImage에 대한 도움말 및 예제 업데이트</span><span class="sxs-lookup"><span data-stu-id="e51e5-1513">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="e51e5-1514">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="e51e5-1514">Az.RecoveryServices</span></span>
<span data-ttu-id="e51e5-1515">Az.RecoveryServices 모듈의 전반적인 가용성.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1515">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="e51e5-1516">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e51e5-1516">Az.Resources</span></span>
* <span data-ttu-id="e51e5-1517">리소스 그룹 관련 태그 수정</span><span class="sxs-lookup"><span data-stu-id="e51e5-1517">Fix tagging for resource groups</span></span> 
    - <span data-ttu-id="e51e5-1518">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/8166 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1518">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="e51e5-1519">`Get-AzureRmRoleAssignment`이(가) -ErrorAction을 준수하지 않는 문제 수정</span><span class="sxs-lookup"><span data-stu-id="e51e5-1519">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span> 
    - <span data-ttu-id="e51e5-1520">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/8235 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1520">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="e51e5-1521">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e51e5-1521">Az.Sql</span></span>
* <span data-ttu-id="e51e5-1522">AzSqlDatabaseBackupShortTermRetentionPolicy 가져오기/설정하기 추가</span><span class="sxs-lookup"><span data-stu-id="e51e5-1522">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="e51e5-1523">SQL cmdlet을 실행할 경우 Azure 계정에 로그인되어 있지 않은 것이 nullref 예외를 초래하는 문제 수정</span><span class="sxs-lookup"><span data-stu-id="e51e5-1523">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="e51e5-1524">Get-AzSqlCapability의 nullref 예외 수정</span><span class="sxs-lookup"><span data-stu-id="e51e5-1524">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="e51e5-1525">1.2.1 - 2019년 1월</span><span class="sxs-lookup"><span data-stu-id="e51e5-1525">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="e51e5-1526">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e51e5-1526">Az.Accounts</span></span>
* <span data-ttu-id="e51e5-1527">올바른 인증 버전을 사용하여 릴리스</span><span class="sxs-lookup"><span data-stu-id="e51e5-1527">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="e51e5-1528">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="e51e5-1528">Az.AnalysisServices</span></span>
* <span data-ttu-id="e51e5-1529">업데이트된 인증 종속성을 사용하여 릴리스</span><span class="sxs-lookup"><span data-stu-id="e51e5-1529">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="e51e5-1530">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="e51e5-1530">Az.RecoveryServices</span></span>
* <span data-ttu-id="e51e5-1531">업데이트된 인증 종속성을 사용하여 릴리스</span><span class="sxs-lookup"><span data-stu-id="e51e5-1531">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="e51e5-1532">1.2.0 - 2019년 1월</span><span class="sxs-lookup"><span data-stu-id="e51e5-1532">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="e51e5-1533">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e51e5-1533">Az.Accounts</span></span>
* <span data-ttu-id="e51e5-1534">Windows PowerShell 5.1 전용 대화형 사용자 이름/암호 인증 추가</span><span class="sxs-lookup"><span data-stu-id="e51e5-1534">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="e51e5-1535">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="e51e5-1535">Update incorrect online help URLs</span></span>
* <span data-ttu-id="e51e5-1536">Uninstall-AzureRm 관련 PS Core에 경고 메시지 추가</span><span class="sxs-lookup"><span data-stu-id="e51e5-1536">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="e51e5-1537">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="e51e5-1537">Az.Aks</span></span>
* <span data-ttu-id="e51e5-1538">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="e51e5-1538">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="e51e5-1539">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="e51e5-1539">Az.Automation</span></span>
* <span data-ttu-id="e51e5-1540">Python 2 Runbook에 대한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1540">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="e51e5-1541">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="e51e5-1541">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="e51e5-1542">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="e51e5-1542">Az.Cdn</span></span>
* <span data-ttu-id="e51e5-1543">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="e51e5-1543">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e51e5-1544">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e51e5-1544">Az.Compute</span></span>
* <span data-ttu-id="e51e5-1545">Invoke-AzVMReimage cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="e51e5-1545">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="e51e5-1546">Set-AzVmss에 TempDisk 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="e51e5-1546">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="e51e5-1547">New-AzVM 경고 메시지 수정</span><span class="sxs-lookup"><span data-stu-id="e51e5-1547">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="e51e5-1548">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="e51e5-1548">Az.ContainerRegistry</span></span>
* <span data-ttu-id="e51e5-1549">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="e51e5-1549">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="e51e5-1550">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="e51e5-1550">Az.DataFactory</span></span>
* <span data-ttu-id="e51e5-1551">ADF.Net SDK 버전이 3.0.0으로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1551">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="e51e5-1552">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="e51e5-1552">Az.DataLakeStore</span></span>
* <span data-ttu-id="e51e5-1553">MSI를 사용할 때 ADLS 엔드포인트 문제 수정</span><span class="sxs-lookup"><span data-stu-id="e51e5-1553">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="e51e5-1554">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/7462 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1554">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="e51e5-1555">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="e51e5-1555">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="e51e5-1556">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="e51e5-1556">Az.IotHub</span></span>
* <span data-ttu-id="e51e5-1557">Add-IotHubRoutingEndpoint cmdlet에 인코딩 형식을 추가하세요.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1557">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="e51e5-1558">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="e51e5-1558">Az.KeyVault</span></span>
* <span data-ttu-id="e51e5-1559">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="e51e5-1559">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e51e5-1560">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e51e5-1560">Az.Network</span></span>
* <span data-ttu-id="e51e5-1561">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="e51e5-1561">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="e51e5-1562">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e51e5-1562">Az.Resources</span></span>
* <span data-ttu-id="e51e5-1563">'New-AzADAppCredential' 및 'New-AzADSpCredential' 참조 설명서의 잘못된 예제 수정</span><span class="sxs-lookup"><span data-stu-id="e51e5-1563">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="e51e5-1564">리소스 그룹 배포 cmdlet 실행 전 '-TemplateFile' 매개 변수 경로가 확인되지 않는 문제 수정</span><span class="sxs-lookup"><span data-stu-id="e51e5-1564">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="e51e5-1565">Az.Resources: New-AzureRmPolicyDefinition -Mode 기본값에 대한 올바른 설명서</span><span class="sxs-lookup"><span data-stu-id="e51e5-1565">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="e51e5-1566">Az.Resources: 문제 https://github.com/Azure/azure-powershell/issues/7522 수정</span><span class="sxs-lookup"><span data-stu-id="e51e5-1566">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="e51e5-1567">Az.Resources: 문제 https://github.com/Azure/azure-powershell/issues/5747 수정</span><span class="sxs-lookup"><span data-stu-id="e51e5-1567">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="e51e5-1568">'PSResourceGroupDeployment' 개체의 서식 문제 수정</span><span class="sxs-lookup"><span data-stu-id="e51e5-1568">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="e51e5-1569">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/2123 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1569">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="e51e5-1570">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="e51e5-1570">Az.ServiceFabric</span></span>
* <span data-ttu-id="e51e5-1571">인증서가 VMSS 모델에 추가되었는데도 예외가 발생할 경우 롤백합니다. 이는 버그 https://github.com/Azure/service-fabric-issues/issues/932 를 수정하기 위함입니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1571">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="e51e5-1572">일부 오류 메시지를 수정하세요.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1572">Fix some error messages.</span></span>
* <span data-ttu-id="e51e5-1573">Az로의 마이그레이션을 통해서는 작동하지 않는 New-AzServiceFabriCluster를 위해 기본값 ARM 템플릿을 가진 클러스터 만들기를 수정하세요.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1573">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="e51e5-1574">확장에서 클러스터 id를 확인하여 클러스터에 해당하는 VMSS에만 추가되도록 클러스터/애플리케이션 인증서 추가를 수정하세요.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1574">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="e51e5-1575">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="e51e5-1575">Az.SignalR</span></span>
* <span data-ttu-id="e51e5-1576">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="e51e5-1576">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="e51e5-1577">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e51e5-1577">Az.Sql</span></span>
* <span data-ttu-id="e51e5-1578">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="e51e5-1578">Update incorrect online help URLs</span></span>
* <span data-ttu-id="e51e5-1579">가능한 값을 가진 LicenseType 매개 변수에 대한 매개 변수 설명이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1579">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="e51e5-1580">유일하게 업데이트된 속성인데 작동하지 않는 관리되는 인스턴스 ID의 업데이트 수정</span><span class="sxs-lookup"><span data-stu-id="e51e5-1580">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="e51e5-1581">관리되는 인스턴스에서의 사용자 지정 데이터 정렬에 대한 지원</span><span class="sxs-lookup"><span data-stu-id="e51e5-1581">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="e51e5-1582">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="e51e5-1582">Az.Storage</span></span>
* <span data-ttu-id="e51e5-1583">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="e51e5-1583">Update incorrect online help URLs</span></span>
* <span data-ttu-id="e51e5-1584">Premium Storage 계정이 클래식 로깅/메트릭을 지원하지 않기 때문에, Premium Storage 계정의 클래식 로깅/메트릭을 가져올/설정할 때 상세한 오류 메시지를 제공해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1584">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="e51e5-1585">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="e51e5-1585">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="e51e5-1586">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="e51e5-1586">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="e51e5-1587">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="e51e5-1587">Az.TrafficManager</span></span>
* <span data-ttu-id="e51e5-1588">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="e51e5-1588">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="e51e5-1589">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="e51e5-1589">Az.Websites</span></span>
* <span data-ttu-id="e51e5-1590">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="e51e5-1590">Update incorrect online help URLs</span></span>
* <span data-ttu-id="e51e5-1591">앱이 ASE에 호스팅되면 'New-AzWebAppSSLBinding'을 수정하여 올바른 resourcegroup+location에 인증서를 업로드합니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1591">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="e51e5-1592">'New-AzWebAppSSLBinding'을 수정하여 SSL 인증서를 앱에 바인딩하는 데 붙는 태그를 덮어쓰지 않도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1592">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="e51e5-1593">1.1.0 - 2019년 1월</span><span class="sxs-lookup"><span data-stu-id="e51e5-1593">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="e51e5-1594">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e51e5-1594">Az.Accounts</span></span>
* <span data-ttu-id="e51e5-1595">Enable-AzureRmAlias에 'Local' 범위 추가</span><span class="sxs-lookup"><span data-stu-id="e51e5-1595">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e51e5-1596">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e51e5-1596">Az.Compute</span></span>
* <span data-ttu-id="e51e5-1597">이름이 Restart/Start/Stop/Remove/Set-AzVM과 Save-AzVMImage에 설정된 ID 매개 변수에서 선택 사항이 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1597">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="e51e5-1598">도움말 파일의 ID에 대한 설명이 업데이트 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1598">Updated the description of ID in help files</span></span>
* <span data-ttu-id="e51e5-1599">Az.Accounts 모듈을 사용할 때의 이전 버전과의 호환성 문제를 해결합니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1599">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="e51e5-1600">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="e51e5-1600">Az.DataLakeStore</span></span>
* <span data-ttu-id="e51e5-1601">SDK 수정을 위해 데이터 평면의 SDK 버전을 1.1.14로 업데이트하세요.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1601">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="e51e5-1602">getfilestatus 및 liststatus에 대한 음수 acesstime 및 modificationtime 수정, 비동기 취소 토큰 수정</span><span class="sxs-lookup"><span data-stu-id="e51e5-1602">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="e51e5-1603">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="e51e5-1603">Az.EventGrid</span></span>
* <span data-ttu-id="e51e5-1604">2019-01-01 API 버전을 사용하도록 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1604">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="e51e5-1605">2019-01-01 API 버전에서 새 시나리오를 지원하도록 다음 cmdlet을 업데이트</span><span class="sxs-lookup"><span data-stu-id="e51e5-1605">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="e51e5-1606">New-AzureRmEventGridSubscription: 지정을 위한 새로운 선택적 매개 변수를 추가</span><span class="sxs-lookup"><span data-stu-id="e51e5-1606">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="e51e5-1607">이벤트 Time-to-Live</span><span class="sxs-lookup"><span data-stu-id="e51e5-1607">Event Time-To-Live,</span></span>
        - <span data-ttu-id="e51e5-1608">이벤트에 대한 최대 배달 시도</span><span class="sxs-lookup"><span data-stu-id="e51e5-1608">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="e51e5-1609">배달 못한 편지의 엔드포인트입니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1609">Dead letter endpoint.</span></span>
    - <span data-ttu-id="e51e5-1610">Update-AzureRmEventGridSubscription: 지정을 위한 새로운 선택적 매개 변수를 추가</span><span class="sxs-lookup"><span data-stu-id="e51e5-1610">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="e51e5-1611">이벤트 Time-to-Live</span><span class="sxs-lookup"><span data-stu-id="e51e5-1611">Event Time-To-Live,</span></span>
        - <span data-ttu-id="e51e5-1612">이벤트에 대한 최대 배달 시도</span><span class="sxs-lookup"><span data-stu-id="e51e5-1612">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="e51e5-1613">배달 못한 편지의 엔드포인트입니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1613">Dead letter endpoint.</span></span>
* <span data-ttu-id="e51e5-1614">New-AzureRmEventGridSubscription 및 Update-AzureRmEventGridSubscription cmdlet의 EndpointType 옵션에 새 열거형 값(즉, storageQueue 및 hybridConnection)을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1614">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="e51e5-1615">이벤트 구독을 생성 또는 업데이트할 때 사용자가 직접 조치를 취해야 할 경우 경고 메시지를 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1615">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="e51e5-1616">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="e51e5-1616">Az.IotHub</span></span>
* <span data-ttu-id="e51e5-1617">최신 버전의 Azure IotHub SDK로 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="e51e5-1617">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="e51e5-1618">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="e51e5-1618">Az.LogicApp</span></span>
* <span data-ttu-id="e51e5-1619">지정된 이름이 없는 모든 Get-AzLogicApp 목록</span><span class="sxs-lookup"><span data-stu-id="e51e5-1619">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="e51e5-1620">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e51e5-1620">Az.Resources</span></span>
* <span data-ttu-id="e51e5-1621">'Get-AzResource'에 '-ODataQuery'및 '-ResourceId' 매개 변수를 제공할 때 매개 변수 집합 문제 수정</span><span class="sxs-lookup"><span data-stu-id="e51e5-1621">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="e51e5-1622">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/7875 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1622">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="e51e5-1623">New/Set-AzPolicyDefinition에서 -Custom 매개 변수 처리 문제 수정</span><span class="sxs-lookup"><span data-stu-id="e51e5-1623">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="e51e5-1624">New-AzDeployment 설명서에서 오타 수정</span><span class="sxs-lookup"><span data-stu-id="e51e5-1624">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="e51e5-1625">'New-AzADUser'에 '-MailNickname'매개 변수가 필수 항목으로 지정됨</span><span class="sxs-lookup"><span data-stu-id="e51e5-1625">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="e51e5-1626">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/8220 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1626">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="e51e5-1627">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="e51e5-1627">Az.SignalR</span></span>
* <span data-ttu-id="e51e5-1628">Az.Accounts 모듈을 사용할 때의 이전 버전과의 호환성 문제를 해결합니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1628">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="e51e5-1629">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e51e5-1629">Az.Sql</span></span>
* <span data-ttu-id="e51e5-1630">Storage 관리 클라이언트 종속성을 일반적인 SDK 구현으로 변환했습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1630">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="e51e5-1631">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="e51e5-1631">Az.Storage</span></span>
* <span data-ttu-id="e51e5-1632">Sas Token, OAuth 또는 Anonymous를 사용하여 스토리지 컨텍스트의 StorageAccountName을 실제 스토리지 계정 이름으로 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1632">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="e51e5-1633">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="e51e5-1633">New-AzStorageContext</span></span>
* <span data-ttu-id="e51e5-1634">'-FullUri' 매개 변수를 사용하여 Blob 스냅샷 개체의 Sas Token을 생성하고 반환된 Uri를 스냅샷 Uri로 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1634">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="e51e5-1635">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="e51e5-1635">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="e51e5-1636">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="e51e5-1636">Az.Websites</span></span>
* <span data-ttu-id="e51e5-1637">'Get-AzDeletedWebApp'의 날짜 구문 분석 버그를 수정했습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1637">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="e51e5-1638">Az.Accounts 모듈을 사용할 때의 이전 버전과의 호환성 문제를 해결합니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1638">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="e51e5-1639">1.0.0 - 2018년 12월</span><span class="sxs-lookup"><span data-stu-id="e51e5-1639">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="e51e5-1640">일반</span><span class="sxs-lookup"><span data-stu-id="e51e5-1640">General</span></span>

- <span data-ttu-id="e51e5-1641">Az 모듈 일반 공급</span><span class="sxs-lookup"><span data-stu-id="e51e5-1641">General Availability of Az Module</span></span>
- <span data-ttu-id="e51e5-1642">각 모듈에 대 한 온라인 도움말</span><span class="sxs-lookup"><span data-stu-id="e51e5-1642">Online help for each module</span></span>
- <span data-ttu-id="e51e5-1643">자세한 내용과 로드맵은 [Az 알림 페이지](https://aka.ms/azps-announce)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1643">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="e51e5-1644">AzureRM에서 마이그레이션하는 것에 대한 정보는 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1644">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="e51e5-1645">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e51e5-1645">Az.Accounts</span></span>
- <span data-ttu-id="e51e5-1646">Az.Profile에서 변경</span><span class="sxs-lookup"><span data-stu-id="e51e5-1646">Changed from Az.Profile</span></span>
- <span data-ttu-id="e51e5-1647">프로필 및 컨텍스트 형식에 대한 표 형식 수정</span><span class="sxs-lookup"><span data-stu-id="e51e5-1647">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="e51e5-1648">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="e51e5-1648">Az.ApiManagement</span></span>
- <span data-ttu-id="e51e5-1649">#7002에 대한 수정</span><span class="sxs-lookup"><span data-stu-id="e51e5-1649">Fixes for #7002</span></span>
- <span data-ttu-id="e51e5-1650">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1650">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="e51e5-1651">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="e51e5-1651">Az.Batch</span></span>
- <span data-ttu-id="e51e5-1652">`PSComputeNode`의 새로운 `NodeAgentInformation` 속성을 통해 풀의 각 VM에서 실행 중인 Azure Batch 노드 에이전트의 버전을 확인하는 기능이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1652">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="e51e5-1653">`PSDataDisk`에 대한 `Caching` 기본 값은 이제 `None` 대신 `ReadWrite`입니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1653">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="e51e5-1654">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1654">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="e51e5-1655">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="e51e5-1655">Az.Billing</span></span>
- <span data-ttu-id="e51e5-1656">청구, 소비 및 UsageAggregates cmdlet 결합 cmdlet에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1656">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="e51e5-1657">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="e51e5-1657">Az.CognitivServices</span></span>
- <span data-ttu-id="e51e5-1658">New-AzureRmCognitiveServicesAccount 작업에서 사용 가능한 SkuName 및 Typem에 대한 완성자 추가</span><span class="sxs-lookup"><span data-stu-id="e51e5-1658">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="e51e5-1659">Get-AzCognitiveServicesAccountSkus에서 GetSkusWithAccountParamSetName 매개 변수 집합을 제거</span><span class="sxs-lookup"><span data-stu-id="e51e5-1659">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="e51e5-1660">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="e51e5-1660">Az.ContainerInstance</span></span>
- <span data-ttu-id="e51e5-1661">ManagedIdentity 지원이 추가됨</span><span class="sxs-lookup"><span data-stu-id="e51e5-1661">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="e51e5-1662">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="e51e5-1662">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="e51e5-1663">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1663">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="e51e5-1664">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="e51e5-1664">Az.DataLakeStore</span></span>
- <span data-ttu-id="e51e5-1665">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1665">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="e51e5-1666">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="e51e5-1666">Az.Monitor</span></span>
- <span data-ttu-id="e51e5-1667">Az.Monitor 이름 변경 및 기타 사소한 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1667">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="e51e5-1668">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="e51e5-1668">Az.KeyVault</span></span>
- <span data-ttu-id="e51e5-1669">출력 형식에서 사용되지 않는 'PurgeDisabled' 속성 제거</span><span class="sxs-lookup"><span data-stu-id="e51e5-1669">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="e51e5-1670">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="e51e5-1670">Az.MachineLearning</span></span>
- <span data-ttu-id="e51e5-1671">Az.MachineLearningCompute 모듈의 cmdlet 포함</span><span class="sxs-lookup"><span data-stu-id="e51e5-1671">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="e51e5-1672">Az.Media</span><span class="sxs-lookup"><span data-stu-id="e51e5-1672">Az.Media</span></span>
- <span data-ttu-id="e51e5-1673">New-AzMediaService에서 사용되지 않는 -Tags 별칭이 제거됨</span><span class="sxs-lookup"><span data-stu-id="e51e5-1673">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="e51e5-1674">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e51e5-1674">Az.Network</span></span>
<span data-ttu-id="e51e5-1675">Application Gateway에서 RewriteRuleSets를 구성하는 것에 대한 지원이 추가됨</span><span class="sxs-lookup"><span data-stu-id="e51e5-1675">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="e51e5-1676">추가된 새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1676">New cmdlets added:</span></span>
        - <span data-ttu-id="e51e5-1677">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="e51e5-1677">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="e51e5-1678">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="e51e5-1678">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="e51e5-1679">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="e51e5-1679">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="e51e5-1680">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="e51e5-1680">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="e51e5-1681">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="e51e5-1681">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="e51e5-1682">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="e51e5-1682">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="e51e5-1683">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="e51e5-1683">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="e51e5-1684">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="e51e5-1684">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="e51e5-1685">선택적 매개 변수를 사용하도록 cmdlet이 업데이트됨 -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="e51e5-1685">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="e51e5-1686">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e51e5-1686">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="e51e5-1687">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="e51e5-1687">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="e51e5-1688">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="e51e5-1688">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="e51e5-1689">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e51e5-1689">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="e51e5-1690">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="e51e5-1690">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="e51e5-1691">New-AzureRmApplicationGatewayUrlPathMapConfig로 ID를 사용하여 Application Gateway에 KeyVault 지원을 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1691">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="e51e5-1692">선택적 매개 변수를 사용하도록 cmdlet이 업데이트됨 -KeyVaultSecretId, -KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="e51e5-1692">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="e51e5-1693">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="e51e5-1693">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="e51e5-1694">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="e51e5-1694">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="e51e5-1695">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="e51e5-1695">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="e51e5-1696">New-AzApplicationGateway cmdlet이 선택적 매개 변수를 사용하도록 업데이트됨 -UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="e51e5-1696">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="e51e5-1697">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1697">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="e51e5-1698">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="e51e5-1698">Az.OperationalInsights</span></span>
- <span data-ttu-id="e51e5-1699">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1699">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="e51e5-1700">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="e51e5-1700">Az.Profile</span></span>
- <span data-ttu-id="e51e5-1701">Az.Accounts에 모듈 이름이 변경됨</span><span class="sxs-lookup"><span data-stu-id="e51e5-1701">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="e51e5-1702">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="e51e5-1702">Az.RecoveryServices</span></span>
- <span data-ttu-id="e51e5-1703">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1703">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="e51e5-1704">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e51e5-1704">Az.Resources</span></span>
- <span data-ttu-id="e51e5-1705">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1705">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="e51e5-1706">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="e51e5-1706">Az.ServiceFabric</span></span>
- <span data-ttu-id="e51e5-1707">일반 이름과 지문으로 지정 인증서 지원</span><span class="sxs-lookup"><span data-stu-id="e51e5-1707">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="e51e5-1708">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1708">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="e51e5-1709">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="e51e5-1709">Az.SIgnalR</span></span>
- <span data-ttu-id="e51e5-1710">SIgnalR에 대한 PowerShell cmdlet에 대한 일반 공급</span><span class="sxs-lookup"><span data-stu-id="e51e5-1710">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="e51e5-1711">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e51e5-1711">Az.Sql</span></span>
- <span data-ttu-id="e51e5-1712">위협 탐지의 cmdlet에 새로운 Data_Exfiltration 및 Unsafe_Action 검색 유형 추가</span><span class="sxs-lookup"><span data-stu-id="e51e5-1712">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="e51e5-1713">Sql 감사 cmdlet에 대한 설명서 예제 업데이트</span><span class="sxs-lookup"><span data-stu-id="e51e5-1713">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="e51e5-1714">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1714">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="e51e5-1715">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="e51e5-1715">Az.Storage</span></span>
- <span data-ttu-id="e51e5-1716">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1716">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="e51e5-1717">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="e51e5-1717">Az.Websites</span></span>
- <span data-ttu-id="e51e5-1718">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1718">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="e51e5-1719">0.7.0 - 2018년 12월</span><span class="sxs-lookup"><span data-stu-id="e51e5-1719">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="e51e5-1720">일반</span><span class="sxs-lookup"><span data-stu-id="e51e5-1720">General</span></span>

* <span data-ttu-id="e51e5-1721">AzureRM에서 Az 전환 예정에 대한 사소한 변경</span><span class="sxs-lookup"><span data-stu-id="e51e5-1721">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="e51e5-1722">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e51e5-1722">Az.Compute</span></span>

* <span data-ttu-id="e51e5-1723">`New-AzVm(ss)` cmdlet에 대한 간단한 매개 변수 집합에 UltraSSD 및 갤러리 이미지에 대한 지원을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1723">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="e51e5-1724">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="e51e5-1724">Az.DataLakeStore</span></span>

* <span data-ttu-id="e51e5-1725">ADLS 계정의 도메인의 후행 슬래시를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1725">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="e51e5-1726">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="e51e5-1726">Az.FrontDoor</span></span>

* <span data-ttu-id="e51e5-1727">일부 끊어진 링크 수정</span><span class="sxs-lookup"><span data-stu-id="e51e5-1727">Fixed some broken links</span></span>
    - <span data-ttu-id="e51e5-1728">New-AzureRmFrontDoor 및 Set-AzureRmFrontDoor 아티클에서 New-AzureRmFrontDoorHealthProbeSettingObject cmdlet 아티클에 대한 링크가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1728">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="e51e5-1729">New-AzureRmFrontDoorManagedRuleObject 아티클에서 New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet 아티클에 대한 링크가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1729">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="e51e5-1730">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="e51e5-1730">Az.RecoveryServices</span></span>

* <span data-ttu-id="e51e5-1731">Azure File Share 복원 작업에 클라이언트 측 유효성 검사가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1731">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="e51e5-1732">afs 복원의 경우 storageAccountName 및 storageAccountResourceGroupName을 선택적으로 만들었습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1732">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="e51e5-1733">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e51e5-1733">Az.Resources</span></span>

* <span data-ttu-id="e51e5-1734">[https://github.com/Azure/azure-powershell/issues/7402](https://github.com/Azure/azure-powershell/issues/7679 ) 에 대한 수정</span><span class="sxs-lookup"><span data-stu-id="e51e5-1734">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="e51e5-1735">기본 관리자를 요청할 때 구독 범위가 제공되는 경우 Get-AzureRmRoleAssignment를 업데이트하여 구독 범위를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1735">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="e51e5-1736">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e51e5-1736">Az.Sql</span></span>

* <span data-ttu-id="e51e5-1737">AzureRM에서 Az 전환 예정에 대한 사소한 변경</span><span class="sxs-lookup"><span data-stu-id="e51e5-1737">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="e51e5-1738">DotNet 코어에서 Get-AzureRmSqlDatabaseVulnerabilityAssessment를 사용하는 문제 해결</span><span class="sxs-lookup"><span data-stu-id="e51e5-1738">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="e51e5-1739">SQL 감사 cmdlet과 관련된 도움말 메시지의 설명서가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1739">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="e51e5-1740">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="e51e5-1740">Az.Storage</span></span>

* <span data-ttu-id="e51e5-1741">New-AzureRmStorageAccount에 -EnableHierarchicalNamespace 추가</span><span class="sxs-lookup"><span data-stu-id="e51e5-1741">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="e51e5-1742">파일 복사 cmdlet이 -DestContext 입력이 없을 때 대상의 원본 컨텍스트를 다시 사용할 수 없는 문제 수정</span><span class="sxs-lookup"><span data-stu-id="e51e5-1742">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="e51e5-1743">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="e51e5-1743">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="e51e5-1744">고정적인 웹 사이트 구성 지원</span><span class="sxs-lookup"><span data-stu-id="e51e5-1744">Support Static Website configuration</span></span>
    - <span data-ttu-id="e51e5-1745">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="e51e5-1745">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="e51e5-1746">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="e51e5-1746">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="e51e5-1747">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="e51e5-1747">Az.Websites</span></span>

* <span data-ttu-id="e51e5-1748">Set-AzureRmWebApp 및 Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="e51e5-1748">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span> 
    - <span data-ttu-id="e51e5-1749">Windows 및 Linux 컨테이너 응용 프로그램에 탑재할 Azure Storage 경로를 지정하기 위해 새 매개 변수(-AzureStoragePath)가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1749">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="e51e5-1750">새 cmdlet New-AzureRmWebAppAzureStoragePath의 출력을 매개 변수로 사용하여 Azure Storage 경로를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1750">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="e51e5-1751">0.6.1 - 2018년 11월</span><span class="sxs-lookup"><span data-stu-id="e51e5-1751">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="e51e5-1752">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="e51e5-1752">Az.ApiManagement</span></span>
* <span data-ttu-id="e51e5-1753">형식 매핑 문제에 대한 종속성 업데이트</span><span class="sxs-lookup"><span data-stu-id="e51e5-1753">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="e51e5-1754">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="e51e5-1754">Az.Automation</span></span>
* <span data-ttu-id="e51e5-1755">Azure Automation cmdlet 기반 Swagger</span><span class="sxs-lookup"><span data-stu-id="e51e5-1755">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="e51e5-1756">업데이트 관리 cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="e51e5-1756">Added Update Management cmdlets</span></span>
* <span data-ttu-id="e51e5-1757">소스 제어 cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="e51e5-1757">Added Source Control cmdlets</span></span>
* <span data-ttu-id="e51e5-1758">Remove-AzureRmAutomationHybridWorkerGroup cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="e51e5-1758">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="e51e5-1759">DSC 노드 등록 명령 수정</span><span class="sxs-lookup"><span data-stu-id="e51e5-1759">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="e51e5-1760">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e51e5-1760">Az.Compute</span></span>
* <span data-ttu-id="e51e5-1761">SystemAssigned ID에 대한 ID 문제 수정</span><span class="sxs-lookup"><span data-stu-id="e51e5-1761">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="e51e5-1762">형식 매핑 문제에 대한 종속성 업데이트</span><span class="sxs-lookup"><span data-stu-id="e51e5-1762">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="e51e5-1763">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="e51e5-1763">Az.ContainerInstance</span></span>
* <span data-ttu-id="e51e5-1764">형식 매핑 문제에 대한 종속성 업데이트</span><span class="sxs-lookup"><span data-stu-id="e51e5-1764">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="e51e5-1765">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="e51e5-1765">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="e51e5-1766">마켓플레이스 cmdlet에 대한 예제 설명 업데이트</span><span class="sxs-lookup"><span data-stu-id="e51e5-1766">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="e51e5-1767">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e51e5-1767">Az.Network</span></span>
* <span data-ttu-id="e51e5-1768">New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="e51e5-1768">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="e51e5-1769">지원되는 AzureFirewall 네트워크 프로토콜에 ICMP 다시 추가</span><span class="sxs-lookup"><span data-stu-id="e51e5-1769">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="e51e5-1770">Test-AzureRmNetworkWatcherConnectivity cmdlet을 업데이트하여 대상 ID, 주소 및 포트 유효성 검사를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1770">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span> 
* <span data-ttu-id="e51e5-1771">VirtualNetwork 맵의 메모리 사용 문제 해결</span><span class="sxs-lookup"><span data-stu-id="e51e5-1771">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="e51e5-1772">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="e51e5-1772">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="e51e5-1773">보호된 파일 공유에 대한 정책을 수정하는 것에 대해 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1773">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="e51e5-1774">정책 표준 시간대를 대문자로 변환했습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1774">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="e51e5-1775">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="e51e5-1775">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="e51e5-1776">New-AzureRmRecoveryServicesAsrProtectableItem의 예제 정정</span><span class="sxs-lookup"><span data-stu-id="e51e5-1776">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="e51e5-1777">형식 매핑 문제에 대한 종속성 업데이트</span><span class="sxs-lookup"><span data-stu-id="e51e5-1777">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="e51e5-1778">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="e51e5-1778">Az.Relay</span></span>
* <span data-ttu-id="e51e5-1779">선택적 매개 변수 -KeyValue를 New-AzureRmRelayKey cmdlet에 추가하여 사용자가 KeyValue를 제공할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1779">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="e51e5-1780">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e51e5-1780">Az.Resources</span></span>
* <span data-ttu-id="e51e5-1781">`New-AzureRmPolicyAssignment` 및 `Set-AzureRmPolicyAssignment`의 자원 ID 관련 매개 변수에 대한 도움말 문서를 업데이트함</span><span class="sxs-lookup"><span data-stu-id="e51e5-1781">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="e51e5-1782">-Metadata를 사용하는 New-AzureRmPolicyDefinition에 대한 예제 추가</span><span class="sxs-lookup"><span data-stu-id="e51e5-1782">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="e51e5-1783">NetStandard의 태그 키에서 대소문자 보존을 허용하도록 수정: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="e51e5-1783">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="e51e5-1784">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="e51e5-1784">Az.ServiceFabric</span></span>
* <span data-ttu-id="e51e5-1785">향후 호환성이 손상되는 변경에 대한 사용 중단 메시지 추가</span><span class="sxs-lookup"><span data-stu-id="e51e5-1785">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="e51e5-1786">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e51e5-1786">Az.Sql</span></span>
* <span data-ttu-id="e51e5-1787">Azure Sql Database Managed Instance 및 Azure Sql Managed Database에 CRUD 작업을 위한 새 cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="e51e5-1787">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="e51e5-1788">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="e51e5-1788">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="e51e5-1789">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="e51e5-1789">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="e51e5-1790">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="e51e5-1790">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="e51e5-1791">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="e51e5-1791">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="e51e5-1792">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="e51e5-1792">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="e51e5-1793">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="e51e5-1793">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="e51e5-1794">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="e51e5-1794">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="e51e5-1795">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="e51e5-1795">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="e51e5-1796">서버 또는 데이터베이스에서 확장 감사 정책 관리를 활성화했습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1796">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="e51e5-1797">새 매개 변수(PredicateExpression)가 감사 로그 필터링을 사용하도록 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1797">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="e51e5-1798">Cmdlet이 레거시 클라이언트 대신 SQL 클라이언트를 사용하도록 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1798">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="e51e5-1799">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1799">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="e51e5-1800">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1800">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="e51e5-1801">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1801">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="e51e5-1802">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1802">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="e51e5-1803">스토리지 계정 이름 매개 변수가 설정된 Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings를 사용할 때의 문제 해결</span><span class="sxs-lookup"><span data-stu-id="e51e5-1803">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="e51e5-1804">0.5.0 - 2018년 11월</span><span class="sxs-lookup"><span data-stu-id="e51e5-1804">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="e51e5-1805">일반</span><span class="sxs-lookup"><span data-stu-id="e51e5-1805">General</span></span>
* <span data-ttu-id="e51e5-1806">많은 핵심 cmdlet에 Resource Completers를 추가하여 대화형으로 cmdlet을 호출할 때 기존 리소스 이름을 탭으로 이동할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1806">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="e51e5-1807">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="e51e5-1807">Az.Profile</span></span>
* <span data-ttu-id="e51e5-1808">ClientRuntime의 최신 버전을 사용하도록 일반적인 코드를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1808">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="e51e5-1809">Connect-AzAccount cmdlet의 매개 변수 TenantId 이름을 Tenant로 바꾸고 TenantId의 별칭을 추가합니다</span><span class="sxs-lookup"><span data-stu-id="e51e5-1809">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="e51e5-1810">Connect-AzAccount의 업데이트된 TenantId 설명</span><span class="sxs-lookup"><span data-stu-id="e51e5-1810">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="e51e5-1811">테넌트 도메인을 제공할 때 실패한 로그인에 대한 오류 메시지 수정</span><span class="sxs-lookup"><span data-stu-id="e51e5-1811">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="e51e5-1812">테넌트에 구독이 없는 계정의 컨텍스트 이름 충돌 문제 수정</span><span class="sxs-lookup"><span data-stu-id="e51e5-1812">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="e51e5-1813">MSI를 사용할 때 DataLake 엔드포인트 문제 수정</span><span class="sxs-lookup"><span data-stu-id="e51e5-1813">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="e51e5-1814">연결되지 않은 경우 'Disconnect-AzAccount'가 throw하는 문제 수정</span><span class="sxs-lookup"><span data-stu-id="e51e5-1814">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="e51e5-1815">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="e51e5-1815">Az.CognitiveServices</span></span>
* <span data-ttu-id="e51e5-1816">Get-AzCognitiveServicesAccountSkus 작업을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1816">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e51e5-1817">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e51e5-1817">Az.Compute</span></span>
* <span data-ttu-id="e51e5-1818">Add-AzVmssVMDataDisk 및 Remove-AzVmssVMDataDisk cmdlet를 추가합니다</span><span class="sxs-lookup"><span data-stu-id="e51e5-1818">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="e51e5-1819">Get-AzVMImage는 AutomaticOSUpgradeProperties를 표시합니다</span><span class="sxs-lookup"><span data-stu-id="e51e5-1819">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="e51e5-1820">수정된 SetAzVMChefExtension -BootstrapOptions 및 -JsonAttribute option 값이 json 형식으로 설정하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1820">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="e51e5-1821">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="e51e5-1821">Az.DataLakeStore</span></span>
* <span data-ttu-id="e51e5-1822">DataLake 패키지를 1.1.10으로 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1822">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="e51e5-1823">기본 동시성을 다중 스레드 작업에 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1823">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="e51e5-1824">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="e51e5-1824">Az.Insights</span></span>
* <span data-ttu-id="e51e5-1825">해결된 문제 #7267(자동 크기 조정 영역)</span><span class="sxs-lookup"><span data-stu-id="e51e5-1825">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="e51e5-1826">열거된 매개 변수를 제대로 설정하지 않은 새 자동 크기 조정 규칙을 만드는 데 문제가 있습니다(이를 항상 기본값으로 설정함).</span><span class="sxs-lookup"><span data-stu-id="e51e5-1826">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="e51e5-1827">해결된 문제 # 7513[자세한 정보] Set-AzDiagnosticSetting은 설정을 생성하는 동안 범주를 명시적으로 지정해야 합니다</span><span class="sxs-lookup"><span data-stu-id="e51e5-1827">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="e51e5-1828">이제 cmdlet은 생성 중에 사용할 범주를 명시적으로 표시할 필요가 없습니다. 즉, 문서화된대로 작동합니다</span><span class="sxs-lookup"><span data-stu-id="e51e5-1828">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e51e5-1829">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e51e5-1829">Az.Network</span></span>
* <span data-ttu-id="e51e5-1830">다음 cmdlet에 대해 PeeringType을 필수 매개 변수로 변경했습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1830">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="e51e5-1831">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="e51e5-1831">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="e51e5-1832">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="e51e5-1832">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="e51e5-1833">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="e51e5-1833">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="e51e5-1834">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="e51e5-1834">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="e51e5-1835">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="e51e5-1835">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="e51e5-1836">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="e51e5-1836">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="e51e5-1837">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="e51e5-1837">Az.PolicyInsights</span></span>
* <span data-ttu-id="e51e5-1838">추가된 정책 재구성 cmdlet</span><span class="sxs-lookup"><span data-stu-id="e51e5-1838">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="e51e5-1839">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e51e5-1839">Az.Resources</span></span>
* <span data-ttu-id="e51e5-1840">[https://github.com/Azure/azure-powershell/issues/7402](https://github.com/Azure/azure-powershell/issues/7402 ) 에 대한 수정</span><span class="sxs-lookup"><span data-stu-id="e51e5-1840">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="e51e5-1841">'Get-AzResource'에 대해 '-ResourceId' 매개 변수를 사용하여 리소스 나열 허용</span><span class="sxs-lookup"><span data-stu-id="e51e5-1841">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="e51e5-1842">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="e51e5-1842">Az.ServiceBus</span></span>
* <span data-ttu-id="e51e5-1843">마이그레이션 상태를 알 수 있도록 PSServiceBusMigrationConfigurationAttributes에 MigrationState 읽기 전용 속성 추가.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1843">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="e51e5-1844">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="e51e5-1844">Az.ServiceFabric</span></span>
* <span data-ttu-id="e51e5-1845">Linux Vmss에 인증서 추가 수정.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1845">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="e51e5-1846">Add-AzServiceFabricClusterCertificate 수정</span><span class="sxs-lookup"><span data-stu-id="e51e5-1846">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="e51e5-1847">새 인증서(Azure/service-fabric-issues#932)에서 올바른 지문을 사용.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1847">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="e51e5-1848">올바르게 예외 표시(Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="e51e5-1848">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="e51e5-1849">Vmss CreateOrUpdate 작업을 시작하기 전에 'Update-AzServiceFabricDurability'를 수정하여 클러스터 구성 업데이트.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1849">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="e51e5-1850">0.4.0 - 2018년 10월</span><span class="sxs-lookup"><span data-stu-id="e51e5-1850">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="e51e5-1851">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="e51e5-1851">Az.Profile</span></span>
* <span data-ttu-id="e51e5-1852">CloudShell에서 Get-AzSubscription을 사용하여 문제를 해결합니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1852">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="e51e5-1853">ClientRuntime의 최신 버전을 사용하도록 일반적인 코드를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1853">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e51e5-1854">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e51e5-1854">Az.Compute</span></span>
* <span data-ttu-id="e51e5-1855">'New-AzVm'에 대해 간단한 매개 변수를 사용하는 경우 가속화된 네트워킹을 설정하기 위해 새 크기가 VM 크기의 허용 목록에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1855">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="e51e5-1856">모든 cmdlet에 ResourceName 인수 완성자가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1856">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="e51e5-1857">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="e51e5-1857">Az.DataLakeStore</span></span>
* <span data-ttu-id="e51e5-1858">Virtual Network 규칙에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="e51e5-1858">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="e51e5-1859">Get-AzDataLakeStoreVirtualNetworkRule: Azure Data Lake Store 가상 네트워크 규칙을 가져오거나 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1859">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="e51e5-1860">Add-AzDataLakeStoreVirtualNetworkRule: 지정된 Data Lake Store 계정에 가상 네트워크 규칙을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1860">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="e51e5-1861">Set-AzDataLakeStoreVirtualNetworkRule: 지정된 Data Lake Store 계정에 지정된 가상 네트워크 규칙을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1861">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="e51e5-1862">Remove-AzDataLakeStoreVirtualNetworkRule: Azure Data Lake Store 가상 네트워크 규칙을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1862">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e51e5-1863">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e51e5-1863">Az.Network</span></span>
* <span data-ttu-id="e51e5-1864">Test-AzNetworkWatcherConnectivity cmdlet을 업데이트하고, 백 엔드에 프로토콜 값을 전달합니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1864">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="e51e5-1865">모든 cmdlet에 ResourceName 인수 완성자가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1865">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="e51e5-1866">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e51e5-1866">Az.Resources</span></span>
* <span data-ttu-id="e51e5-1867">(기본 프로필에 구독이 없고 범위가 지정되지 않은 경우) 시나리오에서 의미 있는 예외를 추가하여 Get-AzRoleDefinition이 인식할 수 없는 예외를 throw하는 문제를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1867">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="e51e5-1868">또한 기본 매개 변수 집합을 'RoleDefinitionNameParameterSet'으로 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1868">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="e51e5-1869">0.3.0 - 2018년 10월</span><span class="sxs-lookup"><span data-stu-id="e51e5-1869">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="e51e5-1870">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="e51e5-1870">Azure.Storage</span></span>
* <span data-ttu-id="e51e5-1871">대상에 메타데이터가 있을 때 Blob/파일이 메타 데이터를 복사하지 않는 문제 수정</span><span class="sxs-lookup"><span data-stu-id="e51e5-1871">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="e51e5-1872">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="e51e5-1872">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="e51e5-1873">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="e51e5-1873">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="e51e5-1874">특정 위치의 스토리지 리소스 사용을 지원하고 글로벌 스토리지 리소스 사용 가져오기는 더 이상 사용되지 않는다는 경고 메시지를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1874">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="e51e5-1875">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="e51e5-1875">Get-AzStorageUsage</span></span>
    
#### <a name="azcognitiveservices"></a><span data-ttu-id="e51e5-1876">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="e51e5-1876">Az.CognitiveServices</span></span>
* <span data-ttu-id="e51e5-1877">기존 계정이 없는 Get-AzCognitiveServicesAccountSkus를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1877">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e51e5-1878">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e51e5-1878">Az.Compute</span></span>
* <span data-ttu-id="e51e5-1879">Get-AzVM -ResourceGroupName <rg>가 필요한 경우 50개가 넘는 결과를 반환하도록 수정</span><span class="sxs-lookup"><span data-stu-id="e51e5-1879">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="e51e5-1880">'SimpleParameterSet' 예제가 New-AzVmss cmdlet 도움말에 추가됨</span><span class="sxs-lookup"><span data-stu-id="e51e5-1880">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="e51e5-1881">Azure Disk Encryption 진행률 메시지의 오타를 수정</span><span class="sxs-lookup"><span data-stu-id="e51e5-1881">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="e51e5-1882">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="e51e5-1882">Az.DataFactoryV2</span></span>
* <span data-ttu-id="e51e5-1883">ADF.Net SDK 버전을 2.3.0으로 업데이트</span><span class="sxs-lookup"><span data-stu-id="e51e5-1883">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e51e5-1884">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e51e5-1884">Az.Network</span></span>
* <span data-ttu-id="e51e5-1885">NetworkProfile 기능 추가</span><span class="sxs-lookup"><span data-stu-id="e51e5-1885">Added NetworkProfile functionality.</span></span> <span data-ttu-id="e51e5-1886">추가된 새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1886">new cmdlets added</span></span>
    - <span data-ttu-id="e51e5-1887">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="e51e5-1887">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="e51e5-1888">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="e51e5-1888">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="e51e5-1889">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="e51e5-1889">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="e51e5-1890">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="e51e5-1890">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="e51e5-1891">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="e51e5-1891">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="e51e5-1892">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="e51e5-1892">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="e51e5-1893">서브넷 모델에 서비스 연결 링크 추가</span><span class="sxs-lookup"><span data-stu-id="e51e5-1893">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="e51e5-1894">New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="e51e5-1894">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="e51e5-1895">Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="e51e5-1895">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="e51e5-1896">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="e51e5-1896">Az.RedisCache</span></span>
* <span data-ttu-id="e51e5-1897">모든 문자열을 Size 매개 변수로 진행되도록 허용</span><span class="sxs-lookup"><span data-stu-id="e51e5-1897">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="e51e5-1898">PSArgumentCompleter 팝업에 P5 추가</span><span class="sxs-lookup"><span data-stu-id="e51e5-1898">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="e51e5-1899">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e51e5-1899">Az.Resources</span></span>
* <span data-ttu-id="e51e5-1900">-Mode 매개 변수를 Set-AzPolicyDefinition에 추가</span><span class="sxs-lookup"><span data-stu-id="e51e5-1900">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="e51e5-1901">사용자가 포함된 Origin 작업에서 Get-AzProviderOperation commandlet 버그 수정</span><span class="sxs-lookup"><span data-stu-id="e51e5-1901">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="e51e5-1902">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e51e5-1902">Az.Sql</span></span>
* <span data-ttu-id="e51e5-1903">일부 백업 cmdlet이 현재 azure 구독을 인식하지 않는 문제 해결</span><span class="sxs-lookup"><span data-stu-id="e51e5-1903">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="e51e5-1904">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="e51e5-1904">Az.Websites</span></span>
* <span data-ttu-id="e51e5-1905">새 cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - 컨테이너 지속적인 배포 Webhook URL을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1905">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="e51e5-1906">새 cmdlet New-AzWebAppContainerPSSession 및 Enter-WebAppContainerPSSession -  windows 컨테이너 앱에 PowerShell 원격 세션을 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="e51e5-1906">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="e51e5-1907">0.2.0 - 2018년 9월</span><span class="sxs-lookup"><span data-stu-id="e51e5-1907">0.2.0 - September 2018</span></span>
 <span data-ttu-id="e51e5-1908">초기 릴리스</span><span class="sxs-lookup"><span data-stu-id="e51e5-1908">Initial Release</span></span>
